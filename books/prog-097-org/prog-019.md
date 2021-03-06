---
title: "【19】誰にとっての「利便性」か"
---


グレゴー・ホーペ（Gregor Hohpe）


　優れた API の設計の重要性、そして難しさについては、これまで多くのことが語られてきました。最初から適切な API を作ることは難しく、しかし後から API に変更を加えることはもっと難しい。まるで子育てのような難しさ、と言っていいでしょう。経験を積んだプログラマならほぼ皆知っていることでしょうが、優れた API とは、まず抽象度がどこをとっても一様であり、その上で整合性、対称性を備えているものです。優れた API はプログラミング言語のボキャブラリーを充実させ、言語に豊かな表現力を与えるものでもあります。しかし、そうした原則を十分に意識していたとしても、適切な API ができるとは限りません。甘い物は身体に必要だが食べ過ぎると健康によくない、というのと同様に、原則にとらわれすぎるとかえって悪い結果を招くことがあるのです。

　こう書いただけだと暖昧でよくわからないと思いますので、具体例をあげることにしましょう。以下の 3 つは、どれも API を設計する人が実際の作業時に言いそうなことです。そして、どの意見も「その方が利便性が高い」という理由で正当化されやすいのです。

  - ほとんど同じ目的の呼び出しコードがクラス A にすでに存在するのに、クラス B に新たに呼び出しコードを持たせる必要はないのではないか。
  - 目的がほぼ同じメソッドがすでに存在するのであれば、わざわざ新たなメソッドを作る必要はないのではないか。switch 文を追加するくらいでいいのではないか。
  - 2 番目の文字列パラメータが“.txt”となっていれば、自動的に、第 1 パラメータはファイル名であるとみなして構わない。したがって、メソッドを 2 つ作る必要はない。簡単な話だ。

　どれも善意から出た意見なのは確かです。しかし、こういう意見に従って API を作ると困ったことが起こります。それは、「API を使用したコードが非常に読みにくくなってしまう」ということです。たとえば、メソッド呼び出しのコードがこんなふうになります。

``` java
parser.processNodes(text, false);
```

　このコードが何を意味するのか、API の内部の実装を知らない人にはおそらくわからないはずです。ドキュメントを調べて何とかわかればまだ良い方でしょう。このメソッドは、たしかに利便性を考えて設計されているのですが、それはメソッドを「実装する側にとっての利便性」であり、決して「呼び出す側にとっての利便性」ではないのです。「することはほとんど同じなのに、2 種類の呼び出しを使うのは不便ではないか」というのは、要するに呼び出す側にとって不便というのではなく、コードを書く自分が、内容のほとんど同じメソッドを 2 つ書くのが「面倒」という意味なのです。冗長で、不整合で、美しくないものを作りたくない、という意図は、基本的に間違っていません。しかし落ち着いてより深く考えるならば、それらの対偶にあるのは効率的、整合性、美しさです。必ずしも「利便性」ではありません。API を作るというのは、複雑な処理を隠蔽するということです。これは正確には、API を作る側が、複雑な処理を隠すために面倒な作業を引き受けなくてはならないということです。そうしなくては優れた API などできません。作る側にとってみれば、考え抜かれたメソッドをいくつも書くよりも、大きなメソッドを 1 つ書く方が「便利」です。しかしそれは使う側にとって「便利」でしょうか？

　より良い API を作るには、API を 1 つの言語だと考えるといいと思います。API を表現力豊かな言語にするにはどうすればいいかを考えるのです。基本的な言語なら「意味のある問いを立て、それに答える」ということができれば十分ですが、API はさらに上のレイヤーの言語にするのです。つまり API では、1 つの問いに対応する動詞、つまりメソッドが必ず 1 つとは限らない、ということです。ボキャブラリーに多様性を持たせれば、微妙な意味の違いが容易に表現できます。たとえば、`walk(true)` というようなコードを書されるよりは、単に `run` と書ける方が間違いなく使いやすいでしょう。walk（歩く）とrun（走る）は本質的には同じ動作で、ただスピードが違うだけとみなすこともできるのですが、言葉が 2 つある方が使う側にとっては便利なのです。このように、一つ一つ考え抜かれ、整合性と豊富なボキャブラリーを兼ね備えた API を上のレイヤーとして追加すれば、言語の表現力が高まり、コードも読みやすく、理解しやすくなります。API を利用して、プログラマが自ら新たなボキャブラリーを作れるようになっているとさらにいいでしょう。API を作った人間がまったく予期していなかったような使い方を、プロクラマが自由に考えられるということです。それができれば API を使う側にとっては非常に便利です。API の開発をしていて、複数の要素を 1 つのメソッドに詰め込みたい衝動にかられたら、是非思い出しください。英語には、たとえば「部屋を片づけて、静かに宿題をやりなさい（Make up your room, be quiet and do your homework）」ということを一語で伝えるような単語はないのです。たとえ同じことを何度も繰り返し言っていて、一語にまとめられれば便利だと思っても、それはしないほうが賢明なのです。
