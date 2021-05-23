---
title: "【80】動的言語を併用しよう"
---


中嶋 謙互


　C/C++/ObjectiveC（以下 C 族言語）を使うときは、Lua や Ruby,Python などの動的言語を併用しましょう。

　ゲームプログラミングは「変えて、試しに遊び、また変える」という作業の連続です。動的言語は、これを速く行うのに有利な特徴を備えています。

　動的言語の極めて重要な特徴は、スクリプトの読み込みがとても速いことです。Lua や JavaScript では、毎秒数十万行以上を読み込み、実行できます。C 族言語では、コードを 1 文字でも修正するとコンパイルとリンクが必要で、場合によっては耐え難い時間がかかります。

　また、動的言語ではコードを速く書くことができます。

　メモリの管理を GC に任せられる、クラスのメンバの宣言を書かずに直接代入できる、関数の型宣言を書かずに非同期のコールバック関数を駆使できることがあります。C 族言語におけるコールバック関数の宣言や型の修正はひどく大変です。

　C 族言語への組み込み可能な動的言語の中でも、特に Lua はゲーム開発に最適です。Lua は実行速度が速く、文法などの仕様もクリーンで、co-routine など便利な機能も備えているのですが、そうした「スペック表」からは見えにくい Lua のよい点を紹介します。

　まず、C 族言語で以下のように 4 行ほど書けば、Lua の処理系を組みこめます:

    lua_State *l;
    l = lua_open();
    lua_dofile(l, "yourscript.lua");
    lua_close();

`lua_State` が、Lua の処理系です。当然ながら、「Lua/C から Lua/C の関数を呼ぶ」ことも、数行の単純なコードで実現できます。

　そして、Lua の処理系は数十 KB 程度におさまります。初期化も極めて速く、1 万行のスクリプトでも数ミリ秒で読み込んで実行できるので、ゲームで敵が出現するごとに処理系を生成したり破棄したりといったことも可能です。このため、データをメモリに保持したまま、処理のロジックだけを入れ替えてプレイを試せます。これによって、音声や画像データが多いゲームや、毎回の起動が遅いモバイル環境での開発効率が改善されます。

　Lua の処理系がここまで小さく軽いのは、機能が最小限だからです。例えば、Lua には正規表現が含まれていません。組み込み用の Ruby である mruby ですら、ソースコード 7 万行のうち、何と 60% 程度が正規表現のために割り当てられています。また、Lua のパーザは C で 1,600 行しかありません。mruby では、yacc で 100KB、C に変換すると 1 万行もあります。複雑な文法規約と、強力な文字列処理を含む必要があるため、どうしても大きくなってしまうのです。

　次は JavaScript エンジンと比較してみましょう。最近のものは、Gmail のように JavaScript のみで書かれた大きいアプリケーションを高速に動作させるために高度な最適化 JIT コンパイラを装備しています。例えば V8 の場合、20 万行以上あるソースの大部分が JIT で占められています。Lua の場合、高速性が必要な処理は C 族で書くことができるので、JIT は不要です。

　技術以外の面はどうでしょうか。Lua は、AngryBirds から WorldofWarcraft まで、多くのゲームで実際に使われていて、米国の大手のゲーム会社が開発のスポンサーになっています（会社名は非公開）。書籍やウェブ上の記事も多く、非常に大きな利用者規模をもちます。

　このように現時点では、フルオープンソースで、十分に動的で、小さく、軽く、組み込みに適し、十分な利用者規模を持つ軽量言語は Lua 以外にはありません。

　C 族言語を使っているならば、一度は Lua を試し、特性を把握しておくべきです。