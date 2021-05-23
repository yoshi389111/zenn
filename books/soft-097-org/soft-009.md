---
title: "【09】それは交渉だということに気付け"
---


マイケル・ナイガード


　予算削減は誰もが経験する試練です。このモードになると、コスト削減のために技術的にまともな選択肢は吹っ飛んでしまいます。会話のトーンは一色になり、スポンサーは「X は本当に必要なのか？」としか言わなくなります。

　「X」の部分は、ソフトウェアライセンス、冗長サーバー、遠隔地バックアップ、冗長電源など、システムを動かすために絶対欠かすことのできない何かです。ところが、スポンサーが「本当に必要なのか？」と言うときの口調は、マンガとガムでお小遣いを使い果たした子供に対する親のようです。まともな大人なら、収益を上げるために必要なものは無理をしても買うべきではないでしょうか。

　ですから、「はい、必要です」と答えるのが正解なのですが、なかなか、そう答えられません。

　私たちはエンジニアとして訓練されています。そのため、エンジニアリングとはトレードオフだということがよくわかっています。ですから、データセンターに発電用の自転車がたくさんあって、安く働いてくれるインターンがいれば、予備電源のようなぜいたくはいらないということを知っています。そこで、「はい、必要です」と言う代わりに、「確かに待機サーバーがなくてもなんとかなります。ただし、定期メンテナンスとメモリパリティエラーによるクラッシュが起きたときに、システムがダウンしてもかまわなければの話です。まあ、後者はパリティビット付きメモリーを買えばいいので、あと心配なのは、OS のクラッシュだけです。これは 3.9 日に 1 回起きるので、夜間リスター卜が必要になってしまいます。でも、インターンたちが自転車を下りて休憩している間にやれば問題ありません」などと言ってしまうのです。

　これは正しいことですが、言ってはいけないことです。スポンサーは、「なんとかなります」の後は何も聞いていません。

　何が問題なのでしょうか。あなたは自分の役割をエンジニアだと思っていますが、スポンサーの方はあなたと交渉をしているつもりでいます。私たちは、協力し合って問題を解決する方法を探そうとしていますが、あちらの人たちは、勝利を収めるための戦術を探しているのです。交渉では、絶対に最初の要求を取り下げてはいけません。「本当に必なのか？」という問いには、次のように答えるのです。

　「待機サーバーがなければ、1 日に少なくとも 3 回はシステムがクラッシュすることになります。しかも、負荷が高いときや、役員会のためにデモをしているときに限ってクラッシュします。本当は 4 台必要なんです。冗長ペアの片方がダウンした状態で、残った 2 台のうちの片方が突然クラッシュしても、まだシステムを維持するためには、それだけのものが必要なんです」

　もちろん、私たちは 3 台目、4 台目のサーバーなどいらないことはわかっています。これは、スポンサーを次の話題に進ませるための交渉術です。すでにあなたが危険で崖から落ちそうなギリギリのところを、かろうじて走っているのだということを示して、交渉のハードルを引き上げているのです。もしこれで本当にサーバーを手に入れることができたら、3 台目は本番システムと同じ環境でテストするために使い、残りはビルド用にすればいいのです。