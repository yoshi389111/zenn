---
title: "【56】たとえ話の使いすぎに注意"
---


デビッド・イング


　アーキテクトは、メタファー、比喩を好んで使います。メタファーは、抽象的で複雑でじっとしていない対象を理解するための具体的な手がかりになります。チームメンバーと話をする場合でも、エンドユーザーにアーキテクチャーを説明する場合でも、構築しようとしているものを表すために、何か手応えのある具体的なものを探したくなる気持ちはよくわかります。

　最初は、共通の言葉ができたことにより、プロジェクトが正しい方向に進んでいるという感じを持ってもらえるので、上々の効果が得られるのですが、メタファーは時間がたつうちに独自の生命を持つところまで成長してきます。メタファーの中でいい感じであれば、うまくいっていると思われてしまうのです。

　こうなってくると、アーキテクチャーのメタファーは危険になってきます。メタファーが次のような形でアーキテクトに牙をむいてくるのです。

  - ビジネスサイドの顧客たちが、提案されたシステムよりもメタファーを気に入ってしまうと、もっとも明るい解釈が共有されてしまって、現実の制約が見えなくなってしまう。

例：「今作っているのは、あちこちに寄港しながら長い旅をする大型船のような感じの輸送システムなんだ」  
顧客がイメージしているのは太平洋を横断するコンテナ船ですが、アーキテクトが考えていたのはプール用のオールが 1 本しかない手こぎボートだとしたら、どうなるでしょうか。

  - 開発チームが、実際のビジネス問題よりもメタファーの方が大切なように錯覚し出す。メタファーに振り回されておかしな判断をおかしいと思わないようになってくるのです。

例：「ファイリングキャビネットのようなものだと言った以上、ユーザーには当然それをアルファベット順で見せなければいけないよね。6 次元で長さが無限で時計が付いているキャビネットなんだけど、今できているのはアイコンだけか。キャビネットでなければいけないんだから……」

  - 引き渡されたシステムの中に、使い物にならなくなって捨てたメタファーに由来する名前が残ってしまう。これではまるでリファクタリングされ、掘り尽くされたコンセプトの考古学資料のようなものです。

例：「なぜ、課金ファクトリーオブジェクトが手こぎボートシステムのポートチャネルを作っているのだろう」「ハブバスの“ザクロ”ビューを返しているんでしょ」「え、何のこと？」

　ですから、メタファーにあまりのめり込まないようにすべきです。メタファーを使うのはコミュニケーションが手探り状態のときだけにして、メタファーに振り回されないようにしなければなりません。
