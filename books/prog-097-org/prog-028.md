---
title: "【28】「魔法」に頼りすぎてはいけない"
---


アラン・グリフィス（Alan Griffiths）


　他人のする仕事というのは、どういうものであれ、遠くから見ているとどうしても実際より簡単に思えてしまうものです。自身が開発を経験していないマネージャは、プログラマの仕事を簡単だと思ってしまいますし、逆にマネージメントの経験のないプログラマは、マネージャの仕事を簡単だと思い込んでしまいがちです。

　厄介なのは、今は「プログラマ」でなくても、以前プログラミングをしたことがある人は意外にいるということです。しかし、「ちょっとやったことがある」という程度だと、プログラミング作業の中でも特に難しい部分——つまり自分の頭を使って考える部分——についてはよくわからないものです。少なくともそれをあまり重要とは思わないでしょう。これは、過去何十年もの間、「知識と経験を持った人でないとわからない部分」をプログラミングから排除する努力が続けられてきたおかげでもあります。最も早い時期からその努力をし、特によく知られている人物が Grace Hopper です。Hopper は、まるで暗号のようだったプログラミング言語を、よりわかりやすいものにすべく力を尽くしました。それができれば、専門のプログラマが不要になるのでは、という予測もありました。努力の結果生まれたのがプログラミング言語、“COBOL”ですが、COBOL の誕生により、専門家は不要になるどころか、その後数十年にわたり、プログラミングによって収入を得る専門のプログラマが多数生まれることになります。

　ソフトウェア開発がこのまま簡単になっていけば、いずれはプログラミングの作業はまったく不要になる、という見方はずっと以前からあり、現在もなくなっていません。この見方は、プログラミングをよく知っている人間から見ると、「あまりに無邪気」としか言いようがないものです。しかし、ついこういう見方をしてしまうのが人間である、ということも同時に言えます。そしてプログラマもやはり人間なので、同じようなことをする時はあるのです。

　プロジェクトには必ず、プログラマが積極的に関わるわけではない作業も多数発生します。たとえば、ユーザの要件を確認することや、予算申請、ビルドサーバのセットアップ、QA 環境や本番環境へのアプリケーションのデプロイなどもそうです。業務プロセスやプログラムを古いものから新しいものへ移行することなどもそうでしょう。

　自分が積極的に関わらない仕事に関しては、無意識のうちに簡単だと思ってしまうし、まるで「魔法」のように自動的にできるような錯覚に陥ってしまうのが人間の常です。すべて順調な時は、確かに魔法だと思っていてもさほど支障はありません。問題は「魔法が解けた」時です。魔法が解けてしまえば、途端にプロジェクトは頓挫し、混乱してしまいます。

　たとえば、私の関わったプロジェクトでは、常に正しいバージョンの DLL がロードされていなければシステムがまったく動かないのに、誰もそのことを理解していなかったということがありました。問題が頻繁に起こり始めてから見当違いの調査を繰り返し、誤ったバージョンの DLL がロードされているせいで動かないということに気づくまでに何週間もの時間が無駄になりました。

　対照的に、何もかもが常に順調に進む部署がありました。納期には絶対に遅れず、深夜までデバッグに追われるということも、顧客から緊急でバグ修正を求められるということもありませんでした。あまりにスムーズなので、会社の上層部は、物事がまるで自動的に回っているかのように思い込んでしまいました。そして「プロジェクトマネージャなど不要なのでは？」と考えるようになったのです。プロシェクトマネージャがいなくなった後、その部署の仕事ぶりは他と何ら変わらないものになってしまいました。納期には遅れ、バグは大量で、リリース後も絶えずパッチをあてているという有様になってしまいました。

　もちろん、プロジェクトに関わるすべての人の仕事を詳しく知る必要はありません。しかし、たとえその一部でも、知ろうとして損はないのではないかと思います。そして、自分の知らない仕事、自分の直接関わっていない仕事をしている人を尊重するということが大事です。

　忘れてはならないのは、「魔法が解けてしまった時は、誰かがかけなおさなくてはならない」ということです。
