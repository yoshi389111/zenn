---
title: "【09】No といえることの大事さ"
---


宮川 達彦


　自分でつくったソフトウェアを公開し、利用してもらうことはとてもうれしいものです。利用しているユーザからのフィードバックに耳を傾けることはソフトウェアをよりよいものにしていくためにもとても重要なことです。

　一方、ソフトウェアのデザインにおける究極の美しさはシンプルさにあると言われます。有名な UNIX 哲学では“Write program that do one thing and do it well”（1 つのことをうまくやるプログラムを書け）といわれるように、複数の機能をつめ込まず、単一の機能をもったプログラムを組み合わせて使うことが美とされます。

　ここにギャップが生じます。ソフトウェアが人気になり、ユーザが増えるにつれ、「あの機能を追加してくれ」「ここの動作をオプションで On/Off できるようにしてくれ」という要望が出てきます。実際にそうした機能やオプションが欲しいとおもっているのは、ごく一部であるにもかかわらず、声の大きいユーザからの要望を無視することができず、忠実に応えようとするあまり、あなたはそれをすべて実装してしまいます。ユーザからのフィードバックはうれしいものですからね。はじめて公開したソフトウェアで特におこりがちなことです。

　こうしてあなたのソフトウェアは、ほとんどのユーザが使わないようなニッチな機能と、それを有効にするための複雑怪奇な設定画面または設定ファイルが必要になり、またそれによってメンテナンスがしづらく、バグのでやすいソフトウェアになってしまいました。こうしたソフトウェアは Feature Creep（creep：いつの間にか忍び寄る、からみつく）とよばれ、ソフトウェアが破滅に向かう第一歩（あるいはもう手遅れ）の状態になっているといえます。

　こうした悲劇を避けるポイントはただひとつ、そうした要望に「No」といえる勇気です。ソフトウェアのコアではないもの、他のソフトウェアと組み合わせて実装できるものに関しては、明確に No といえることが、結果としてよいデザインやシンプルさを達成する原動力になります。

　とはいえ、顧客からの要望で、No ということはできない、というケースも多々あるでしょう。そうした場合にも、ソフトウェア本体で実装するのではなく、本体をラップする形の拡張で実装したり、プラグインのようにコアのコードを変更することなく動作を変更できるようなデザインにする、というやり方も考えられます。

　ビジネス上の理由で、そうしたこともできない、というのであれば、そこはそれとあきらめて、業務外でオープンソースのソフトウェアプロジェクトに参加するモチベーションにする、というのもありかもしれません :-)