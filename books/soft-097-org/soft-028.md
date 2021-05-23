---
title: "【28】地上 300m からの目"
---


エリック・ドーネンバーグ


　私たちは、アーキテクトとして、開発中のソフトウェアがどのくらい優れたものになっているかを知りたいと思っています。ソフトウェアの品質には、ユーザーにとってありがたいものになっているかどうかという外から見た当然の基準があります。しかし、それよりもわかりにくい内側の基準もあります。それは設計の明快性に関連したもので、ソフトウェアの理解、メンテナンス、拡張がどれくらい簡単かということです。あえて定義するなら、「見ればわかる」と言えるかどうかです。しかし、どうすればそのような品質が得られるのでしょうか。

　アーキテクチャーの図表には、システム全体を表現する小さいボックスとそれらを結ぶさまざまな線が描かれています。それらの線は、依存関係、データフロー、あるいはバスなどの共有リソースを表しています。これらの図表は、いわば 1 万メートル上空からの目、飛行機から見た風景です。普通は、システムに対する視点はあと 1 つ、すなわちソースコードしかありません。これは地上の目ということができるでしょう。しかし、これら 2 つの視点は、ソフトウェアの品質について、多くの情報を取りこぼしてしまいます。片方は単純化しすぎており、もう片方は情報過多なので、これらだけでは構造が見えないのです。必要なのは、上空 300m からの目です。

　この上空 300m の目は、適切なレベルでの情報を与えてくれます。このレベルでは、メソッド数、クラスから利用されている他のクラス数（Funout）、循環的複雑度など、さまざまなデータと指標が提供されます。実際の視界は、ソフトウェア品質のどの部分に着目するかによって変わります。依存グラフの視覚的表現、クラスレベルでの指標を示す棒グラフ、複数の入力値の相関関係を示す高度な複合図など、さまざまな形を取ります。

　このような図表を手作業で作って、ソフトウェアの変化に合わせて維持修正していくことは、とてもではありませんが不可能なことです。唯一の情報源であるソースコードからこのような図表を作るツールが必要です。たとえば DSM（デザイン構造マトリックス）などは、市販ツールで作れますが、データや指標を抽出する小さなツールと汎用のビジュアライズソフトウェアを組み合わせれば、特殊な図表も驚くほど簡単に作ることができます。たとえば、クラス、メソッドレベルの指標群である CheckStyle からの出力をスプレッドシートに取り込みし、グラフ化するようなことです。InfoViz ツールキットを使えば、同じ指標をツリーマップで表示できます。また、GraphViz は、複雑な依存グラフを図示できる優れたツールです。

　適切な図表が得られるようになれば、ソフトウェアの品質をわずかながらも、より客観的に評価できるようになります。たとえば、開発中のソフトウェアと同様のシステムを比較するのもよいでしょう。同じシステムの別のリビジョンを比較すれば、品質がどちらの方向に変化していこうとしているかがわかりますし、サブシステム間で比較すれば、突出した数値を示しているサブシステムがあぶり出されます。たった 1 つのグラフがあるだけでも、私たちは美的センスを駆使してパターンを見つけ出すことができます。たとえば、バランスのよいツリーは、クラス階層がうまく作られていることを表します。ボックスの配置が調和の取れたものになっていれば、適切な規模のクラスからコードが構成されていることがわかります。ほとんどの場合、図表と実際のシステムの間には非常にシンプルな関係があります。図表が美しければ、おそらくシステムもよいものになっているということです。