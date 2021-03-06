---
title: "【03】ローカライゼーションのせいで締め切りに遅れる"
---


パベル・シムサ（Pavel Simsa）PMP



アメリカ、ワシントン州ベルビュー


　どういったローカライゼーションのせいで締め切りに遅れるのでしょうか？　答えは「どんなローカライゼーションでも起こり得る」です。英語以外の言語でリリースされる製品を開発している場合、プロジェクトには新たなリスクと制約が多数加わっています。

　技術的なものもあれば自明なものもあります。例えば製品を日本語でリリースするなら、適切なフォントをサポートする必要があります。もしそれができていないと、たとえ英語版は完全に動作しても、日本語版はうまく動作しないでしょう。しかし、フォントの互換性はあなたが管理しているわけではありません。あなたとあなたのチームは、さまざまな注意事項があることを事前に認識し、コーディングに入る前に十分検討しておく必要があります。自分たちの開発プラクティスがそうした問題を取り除く国際的標準に準拠しているか確認しましょう。

　ローカライズ版が必要になるだけで、あなたが下せる判断とそのタイミングは制約されます。通常ローカライゼーション（日本語、スウェーデン語、ドイツ語など）は、ある一定の遅延をもって英語版の開発と並行して実施されます。その遅延は数日や数週間、場合によっては数か月になることもあります。しかし、どこかの時点で、ローカライズ版の翻訳が英語版に「追いつく」必要があります。

　テストやレビューでは、以下を確認しておく必要があります。

  - 英語版にあるものが適切に翻訳されていること

  - 翻訳されたものが正確に英語版と一致していること

  - 翻訳版が完全に機能すること

　ここで問題があります。これら 3 つのポイントは、英語版が完成して出荷判定された後に、テストされるかもしれません。ところが、ローカライズ版のテストとレビューをしているうちに、英語版を変更しないと解決困難な問題が少なくとも 1 つは見つかるものなのです。

　英語版に対する土壇場の変更が、たとえ文章の言い換えなど（数秒のコーディングで済むような）比較的単純でリスクの低いものであっても、それを実装してすべてのローカライズ版を再テストするためには、数日はかかってしまうことを認識しておきましょう。

　これは数千ドルもの余計なコストをもたらします。翻訳作業を外部委託しているなら、なおさらです。経験の浅いソフトウェア開発プロジェクト・マネジャーがよくやる間違いは単純です。英語版に対する予期せぬ変更の影響と重大さを、甘く見てしまっているのです。

　これを避けるために、あなたができることは大きく 2 つあります。

  - スケジュールの最後に「ローカライゼーション・バッファ」という予備期間を用意しておきましょう。スケジュールの最後というのは、プロジェクト全体のスケジュールにおける、英語版作業の事実上の締め切りを意味しています。目標とする最終日以後に必要になった変更は、非常に明確かつ厳格な基準を満たさない限り、スケジュールに追加してはいけません。また、英語版を変更するたびにローカライズ版も忘れずに変更する必要があります。

  - 機能の品質管理は、英文の品質レビューとは別に行われるよう、タスクを並べてください。すべての英文を校正用の表にコピーしてレビューするといったことは、簡単に実現できます。こうすることで製品を実際に動かしてテストするうちに不明瞭な言葉遣いを見つけるのではなく、英文の品質レビューにおいて事前に問題を発見できます。これによって必要な変更が早期にできるようになり、ほかのローカライズ版で変更し直す必要はなくなるでしょう。
