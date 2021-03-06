---
title: "【83】UNIX ツールを友にする"
---


ディオミディス・スピネリス（Diomidis Spinellis）


　もし無人島に IDE か UNIX ツールのどちらかしか持って行けないとしたら、私は迷うことなく UNIX ツールを選びます。なぜそうなのか、ここではその理由を説明することにしましょう。

　まず、IDE はどれも、特定の言語をターゲットとしています。一方 UNIX ツールなら、テキスト形式になっているものは何でも扱えます。今日の開発環境には毎年のように新しい言語や表記法が追加されるので、UNIX ツールの使い方を学ぶのに時間を投資してもすぐに回収できるでしょう。UNIX ツールが使えれば、新しい IDE を導入することなく新しい言語や表記法に対応できるからです。

　また、IDE の場合は、その IDE を開発した人の考えたコマンド以外は使えませんが、UNIX ツールなら、自分の発想次第で何でもできます。UNIX ツールを、レゴブロック（今の子供たちにはバイオニクルの方が有名かもしれません）のようなもの、と考えることもできます。シンプルな部品の組み合わせによってどんなコマンドでも自分で作り出せる万能のツールです。たとえば、Ward Cunningham のシグネチャ調査をテキストベースで実装すると次のようになります。これにより、個々のファイル中のセミコロンや、中括弧、引用符などの並び方を見て、そのファイルの内容について知ることができます。

``` shell
for i in *.java; do
    echo -n "$i: "
    sed 's/[^"{};]//g' $i | tr -d '\n'
    echo
done
```

　IDE の場合、特定の作業をするための方法はあらかじめ決まっていて、他の方法を使うことはできません。たとえば、デバッグビルドの設定にステップを新たに追加する方法は、あらかじめ決まっています。それに対し UNIX ツールの場合は、自分の工夫次第で同じ作業をより効率的に行うことが可能です。たとえば UNIX ツールで今の例と同じ作業をする場合には、私は sed を利用して、ビルドをマルチプロセッサアーキテクチャでのクロスコンパイルに対応させています。

　元々 UNIX ツールは、マルチユーザのコンピュータの RAM が 128KB しかない時代に開発されたものです。少ない RAM を効率的に利用するために工夫が凝らされているので、それを現在のような大容量 RAM のコンピュータで使えば、素晴らしく効率的な処理が可能でしょう。ほとんどの UNIX ツールは、フィルタのように 1 度に 1 行だけを処理します。これは、UNIX ツールが扱えるデータの量に、事実上「上限がない」ことを意味します。たとえば、データ量 500MB ほどある英語版 Wikipedia のダンプの中を解析して、編集が何回なされたかを調べたい時は、以下のコマンドを実行します。

``` shell
grep '<revision>' | wc -l
```

　これであっという間に答えがでます。何度も同じコマンドの組み合わせを使うようならば、それをシェルスクリプトにまとめることも簡単にできます。シェルスクリプトなら、パイプを使ってコマンドの処理結果をループや条件文に渡すこともでき、非常に便利です。さらに素敵なことに、UNIX コマンドはパイプライン処理として動作するので、現在のマルチコア CPU の場合は、複数のコアに負荷が自然に分散されます。

　「スモール・イズ・ビューティフル」の発想で設計され、オープンソースで書かれた UNIX ツールは、今やいたるところで利用されています。たとえばセットトップボックスや DSL ルータといったリソースの限られたプラットフォームでも使われています。その種のデバイスでパワフルな GUI が提供されることはまずなく、多くの場合、BusyBox アプリケーションが使われています。BusyBox は、UNIX ツールの中でも特に利用頻度の高いもので構成されたアプリケーションです。Windows で開発をしている場合も、Cygwin 環境を導入すれば、UNIX ツールと聞いて思いつくようなものが利用できます。Cygwin 環境では、UNIX ツールが実行ファイルとソースコードの両方の形態で提供されています。

　既存のツールがどれも自分の希望に合わないという場合も、UNIX ツールなら簡単に拡張ができます。いくつか簡単なルールを守ってプログラムを書けばいいのです（言語はどれでもかまいません）。そのルールとは、シングルタスクのプログラムにすること、標準入力からテキスト行としてデータを読み込むこと、実行結果は標準出力に書き込み、その際ヘッダなどの余計な飾りはつけないこと、です。ツールの動作に影響するパラメータはすべてコマンドラインに指定するようにしましょう。これらのルールを守れば、「この世界とそこにあるものはすべて君のもの」、必要十分な機能を持ち、応用範囲の広いツールができるでしょう。
