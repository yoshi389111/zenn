---
title: "【46】すべきことは常に明確に"
---


ダン・バーグ・ヨーンソン（Dan Bergh Johnsson）


　たとえば、私が 3 人のプログラマの肩を叩いて、「今、どんな仕事をしているんですか」と尋ねたとしましょう。すると 1 人は、「ああ、今、このメソッドのリファクタリングをしているところですよ」と答えました。もう 1 人は「この Web アクションにパラメータをいくつか追加しているところです」と答えました。そしてもう 1 人は「このユーザストーリを扱っています」と答えました。

　この場合、最初の 2 人は細部にばかりとらわれていて、3 人目のプログラマだけが大局を見ている、自分の仕事の目的がよくわかっている、そういうふうにも見えます。しかし、3 人に作業の具体的内容と所要時間を聞いてみると、様子がまったく違ってきたのです。最初の 2 人は、自分がいま取り組んでいる作業の内容を完全に把握していました。作業ではどのファイルについて何をするのか、何時間で完了する予定なのか、それがすべて明確になっていました。ところが、3 人目のプログラマはそうではありませんでした。細かいことを尋ねたら、「検討中」という答えが返ってきました。何日か模索してみないと細かいことはどうなるかわからないと言うのです。わかるのは、せいぜい「クラスをいくつか追加して、サービスに少し変更を加えることになるだろう」ということくらいでした。

　最初の 2 人は、何も大局を見ていなかったわけではないのです。最終的な目標が何なのかはよくわかっていました。その目標に向かって前進するために、今どんな作業をすべきかを明確に決めていただけです。すべきことをはっきりと定め、それを何時間で完了させるのかも定めていました。また、1 つの作業が完了したら、すぐに次に何をすればいいかを決めます。次の作業は、新しい機能の追加かもしれないし、既存のコードのリファクタリングかもしれません。ただ、どの作業でも必ず目的を明確に定め、それを充分短い時間（たとえば 2 時間）で区切るというのは同じです。

　それに対し、3 人目のプログラマは、大目標を小目標に分解するということは一切していません。いきなり大目標に向かって作業を始め、漠然と作業を進めていました。目標達成までに具体的にどういう作業が必要になるのか、それぞれにどのくらい時間がかかるのかはまったく見えておらず、次にどうすればいいかは手探りで何となく決めている、という状態です。そうしているうちに視界が開け、すべきことが明確になり始めるだろう、とは思っていますが、それがいつになるか確信はありません。おそらく最初の方に書いたコードは、長い時間が経って全体像が見えてくる頃には、まったく的外れなものだったことがわかるでしょう。

　最初の 2 人のプログラマは、たとえば 2 時間で完了させる予定だった作業にそれ以上の時間がかかりそうだと途中でわかってしまったらどうするでしょうか。その場合、彼らはまず、その作業で書いたコード、加えた変更をすべて破棄するでしょう。そして目標をさらに細かく分割して、再び新たな小目標達成のための作業を開始するのです。時間どおり終わらない作業をそのまま続けても、それが妥当なものかどうかはわからないし、本当に有効かどうかわからないコードがレポジトリに入ってしまうのは良いことではありません。それよりは、いったん作業を白紙に戻した方がいいのです。コードは白紙に戻りますが、直前の作業から得た教訓、ひらめきは頭に残っているはずです。

　3 人目のプログラマは、「多分、これで妥当だろう」という推測だけでコードを少しずつ書いていきます。そうしたコードの断片をあとで無理につなぎ合わせようとします。つなぎ合わせれば、それが大目標に添ったものになるはず、と信じて。せっかく書いたコード、加えた変更を途中で破棄するなど、あり得ないことです。それまでにかけた時間や労力が無駄になってしまう、と思うからです。しかし、そういうやり方をしていると、有効かどうかわからない中途半端なコードがレポジトリに多く入り込むことになってしまいます。

　最初の 2 人のプログラマも、場合によっては、一定の時間内に完了できる有効な作業がすぐに見つからないということがあり得ます。そんなときは、コードを見たり、書いたりしながら、次にすべき作業を「ああでもない、こうでもない」と模索するモードに入ります。そして最終的に次の作業の内容が固まったら、模索中に書いたコード、加えた変更はすべて破棄します。作業が無駄になってしまうように見えますが、そうではありません。明確な目的もわからないのに闇雲に先を急ぐよりも、少し遠回りのようでも、確実に有効とわかる作業を探した方が、結局は最終目標に向かって着実に前に進むことになるからです。

　大事なのは、常に自分が何をすべきかを明確にするということです。完了する期限も必ず決めます。もし、期限内に予定の作業が終わらないようであれば、その間に書いたコード、コードに加えた変更はすべて破棄します。再度、小目標を立て直して作業内容を検討し、はじめからやり直すのです。次に何をすればいいかがすぐにわからない時は、やはりあれこれと模索するのですが、大事なのは「いつの間にか手探り状態になっていた」ということを絶対に避けるということです。模索段階で書いたコードを決してレポジトリに入れてはいけません。
