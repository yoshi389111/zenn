---
title: "【14】コードレビュー"
---


マティアス・カールソン（Mattias Karlsson）


　コードレビューは一般に「実施すべきもの」とされています。なぜでしょうか。 **コードの質を上げ、欠陥を減らすため** でしょう。しかし、目的はそれだけとは限りません。

　プログラマの中には、コードレビューを毛嫌いする人が多くいます。おそらく過去に、コードレビューで何か嫌な経験をしたことがあるのでしょう。全コードが社会規定のレビューを通過しない限り、リリースを行わないという企業もあるようです。こういうレビューを担当するのはだいたいアーキテクトやリードデベロッパです。「アーキテクトが全てをレビューする」というプラクティスです。そうすることが企業の「ソフトウェア開発工程マニュアル」などで規定されていれば、プログラマはその規定に従う他ありません。

　そのような厳しく堅苦しいレビューが必要な企業も中にはあります。しかし、大半の企業ではそうではありません。どうしても非生産的になってしまうからです。この種のレビューを実施すると、レビューを受けている側は、まるで自分が軍法会議にでもかけられているように感じます。またレビュー担当者はコードを読むための時間を確保しなくてはならず、しかも対象システムの知識を細部に至るまで常に最新の状態に保つことを強いられます。レビューが工程の中でボトルネックとなってしまい、やがてプロセスそのものが瓦解してしまうことにもなりかねません。

　コードレビューの目的は、ただコードの誤りを修正するだけではありません。重要なのは、 **チーム全員に同じ知識を共有させること、またコーディングにおいて全員が守るべきガイドラインを確立すること** です。自分の書いたコードを他のプログラマと共有することで「コードの共同所有（collective code ownership）」が可能になります。レビュー実施にあたっては、担当者をチームのメンバーから無作為に選び、他のメンバーの協力も得て順にコードを確認していく、という方法を採るといいでしょう。レビュー担当者は単に誤りを探すのではなく、個々のコードについて学び、理解することを心がけましょう。

　レビューにおいては、みんな友好的な態度をとるべきです。コードについて何か意見を述べるときは **建設的であるように心がけ、辛辣な批判は絶対に避けましょう** 。また組織内での上下関係がレビュー結果に影響することがないよう、個々のレビュー担当者の役割、権限はあらかじめ明確に決めておきます。たとえば、ドキュメント担当、例外担当、機能担当といった具合に担当範囲を分けるのがいいでしょう。これは 1 人あたりの負担を減らすことにもつながります。

　コードレビューは曜日を決めて毎週実施するといいと思います。その曜日には、2 時間ほどかけてレビューミーティングをするのですが、レビューの対象者となる人はミーティングごとに順に変えていきます。一巡したらまた最初から、ということにすればいいでしょう。レビュー担当者の役割もミーティングごとに毎回変えるべきです。チームの中に新人がいる時は、その人も是非、レビューに参加してもらいます。新人には経験はありませんが、大学を卒業して日が浅い分、まだ学んだことがかなり記憶に残っているでしょう。その知識のおかげで違った視点が得られる場合もあります。もちろん、経験と知識の豊富な人にレビューに加わってもらうべきなのは言うまでもありません。彼らは、誤りの混入しやすいコードをいち早く、しかも正確に見つけることができます。さらに、コードレビューの進行をスムーズにするためには、コーディングが常に一定のルールに従って行われる体制作りも大切でしょう。ルールが守られているかどうかは、コーディング中にツールで自動的にチェックされるようにしておきます。その体制ができていれば、コードレビューでフォーマットについて議論する必要はなくなります。

　おそらくコードレビューを成功させるために最も有効な方法は、 **レビューを楽しいものにすること** です。レビューで最も大事なのは人です。もしレビューが辛く退屈なものだったとしたら、誰も進んでレビューに参加する気にはならないはずです。できるだけくだけた雰囲気になるよう心がけ、主目的をメンバー内で知識を共有することに置くようにするといいでしょう。厳しい言葉の飛び交うレビューより、昼食やお菓子を食べながらのレビューのほうがいいと思います。
