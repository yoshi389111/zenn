---
title: "【08】ボーイスカウト・ルール"
---


ロバート・C・マーティン（Robert C. Martin アンクル・ボブ）


　ボーイスカウトには大切なルールがあります。それは、「来た時よりも美しく」です。たとえ自分が来た時にキャンプ場が汚くなっていたとしても、そしてたとえ汚したのが自分ではなかったとしても、きれいにしてからその場を去る、というルールです。そうやって、次にキャンプに来る人たちが気持ち良く過ごせるようにするのです（このルールは元々、ボーイスカウトの父と呼ばれるロバート・スティーブンソン・スミス・ベーデン=パウエルの「自分が最初に見た時よりも、世界を良い場所にすべく努力しよう」という言葉から来ています）。

　これに倣ってコーディングに関しても同じルールを定めるとしたら **「モジュールをチェックインする際には、必ずチェックアウト時よりも美しくする」** となります。最初にそのモジュールを書いたのが誰であるかに関係なく、皆がそうやって、たとえ少しずつでもモジュールを改善する努力を続けたとしたら、その結果どういうことが起きると思いますか？

　この簡単なルールを皆が守るだけで、少なくとも今よりシステムの品質が低下することは防げるでしょう。逆に、時間が経つごとにシステムの品質は徐々に向上していくはずです。これは開発に関わるチームの全員が、自分の担当する小さな部分だけでなく、システム全体の質に目を向けるということにもつながるでしょう。

　私はこのルールをとても守れないような難しいものだとは思っていません。何もすべてのモジュールをチェックイン前に完璧なものにせよと言っているのではなく、チェックアウト時より少しでも良いものにしようと言っているだけなのです。モジュールに新たなコードを加える場合には、もちろんそのコードを「美しく」します。既存のコードを触る場合には、チェックイン前にどこか 1 箇所でいいので改善しましょう。変数名をより適切なものに変えたり、大きい関数を 2 つの小さくよりシンプルな関数に分割する、というのでもいいのです。循環参照を解消するというのでもいいですし、インターフェースを追加することでポリシーと実装を切り離すというのでもいいでしょう。

　正直に言うならば、これは誰もが守るべき当然の礼儀ではないかと思います。——トイレに行ったら手を洗う、ゴミは床に散らかさずにゴミ箱にきちんと捨てる、というのと同じ類のことではないでしょうか。実際、コードに「汚い」部分を残したままにすることは、ゴミをまき散らすのと同じくらい、社会的に受け入れがたいことです。誰から見ても「してはならないこと」なのです。

　そしてこれは礼儀以上の話でもあります。他人が書いたコードを改善しようと思えば、自分の担当部分のコードを改善する場合とはまったく違った配慮が必要になります。チームのメンバーが互いに助け合い、そして互いのコードをきれいにするのです。ボーイスカウト・ルールを守るのは、それが自分だけではなく、皆のためになるからです。
