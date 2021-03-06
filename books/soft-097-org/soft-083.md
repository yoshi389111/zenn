---
title: "【83】設計した通りにはならない"
---


ピーター・ジラードモス


　システムは、設計した通りにはならないものです。設計に非常に長い時間をかけたから、その通りに実装できると思うのは、あまりにも引っかかりやすい落とし穴です。細かく設計すると、すべてのアングルを網羅したと勘違いしがちです。細かく設計し、深く調査すればするほど、設計に対する自信は大きくなりますが、それは幻想です。システムが設計した通りになることは決してありません。

　どんなに深く、綿密に調査し、どんなによく考え抜いて設計したとしても、現実にできるものは、頭の中にあったものとは同じにはなりません。何かが起きて設計が狂うのです。間違った情報、何らかの制限、他のコードの変な動作といった外部要因、見落とし / 誤った前提 / 微妙な誤解といったあなた自身の誤り、その他、要件やテクノロジーの変化、誰かが思いついたよい方法をなど、設計が狂う原因はいくらもあります。

　設計の中の小さな変更はあっと言う間に積み重なり、早晩大きな変更を加えなければならなくなります。そのうちに最初のコンセプトはばらばらになってしまい、再びホワイトボードの前に集まらなければならなくなります。そこでは前の設計よりも詳しく、しっかりとした設計を作るという決意のもと、より明確で、根源的で、完璧な新しいアーキテクチャーのビジョンが生まれます。

　しかし、早晩同じことが起きます。設計変更が姿を現し始め、設計はずれていきます。デベロッパーたちは、設計の壊れた部分をつくろうためにますます力を入れてベストを尽くしますが、設計はさらに壊れていきます。あなたはついに叫びます。「もちろんバグのせいだよ、こんな風に設計したはずはない！」

　設計は発見的なプロセスです。実装を進めていくと、新しい情報を発見します。その多くは、あらかじめ知ることのできないものです。変化し統ける世界のもとでは設計は継続的で経験的なプロセスになることを受け入れなければなりません。そうすれば、設計が柔軟で継続的なプロセスにならなければならないことが学べます。最初の設計に固執し、そのままの方針で突き進んでは、いつも同じ結果になるだけです。システムは、設計した通りにはならない、と理解しなければなりません。
