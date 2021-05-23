---
title: "【57】アプリケーションの保守に力を入れよ"
---


ムセディシ・カスパー


　アプリケーションの保守をその場の思いつきでごまかすのは、絶対してはならないことです。アプリケーションのライフサイクルの 80% 以上はメンテナンスのために費やされるのですから、最初の設計段階からサポートとメンテナンスの問題に十分注意を払っていなければなりません。これを怠ると、アプリケーションはアーキテクトの夢どころか、恐ろしい死に方をするとんだ化け物になり、失敗として永遠に記憶されることになります。

　ほとんどのアーキテクトがアプリケーションを設計するときにイメージしているのは、IDE とデバッガをすぐに使えるデベロッパーです。何か問題が起きれば、スキルの高いソフトウェアエンジニアがデバッグしてバグを見つけてくれるはずです。大半のアーキテクトは、ほとんどのキャリアをシステム管理者ではなく、デベロッパーとして過ごしてきていますので、ついこのように考えがちです。しかし、開発 / テスト環境と本番環境では目的が異なるのと同じように、デベロッパーと保守担当ではスキルセットが異なります。

　システム管理者がアーキテクトと比べて不利な点は、たとえば次のようなことです。

  - システム管理者は、問題を再現するためにリクエストメッセージをサブミットし直すわけにはいかない。本番システムでは、何がまずいのかを調べるために「生きた」データベースに対して金銭が動くトランザクションを再発行するわけにはいかないのです。
  - アプリケーションが本番稼働に移ると、プロジェクトマネージャーやテストチームではなく、顧客と経営者からバグを修正しろという圧力を受けるようになる。怒った CEO の方が、脅威としてははるかに大きいでしょう。
  - 本番システムにはデバッガがない。
  - システムを本番に回すと、デプロイに日程調整が必要になる。稼働しているアプリケーションを数分間止めて、バグフィックスをテストするというわけにはいきません。
  - 本番システムの環境ではロギングレベルが開発環境よりもはるかに低く設定されている。

　保守計画が立てられていない兆候は、次のようなところに現れます。

  - ほとんどの障害がデベロッパーの関与を必要とする。
  - 開発チームと保守チームの関係が冷ややかで、開発チームが保守チームをバカだと思っている。
  - 保守チームが新しいアプリケーションをいやがる。
  - アーキテクトと開発チームが本番システムで多くの時間を費やしている。
  - 問題解決の手段としてアプリケーションが頻繁にリスタートされる。
  - システム管理者がいつもトラブルを抱えているため、システムのチューニングに時間を使えない。

　デベロッパーの手を離れた後のアプリケーションを成功させるためには、アーキテクトは次のことをしなければなりません。

  - 開発と保守では、必要とするスキルセットが異なることを理解する。
  - プロジェクトのできる限り早い段階で保守リーダーの参加を求める。
  - 保守リーダーを開発チームの中心メンバーに据える。
  - アプリケーションのサポート計画に保守リーダーを参加させる。

　保守チームにとって習得しやすい設計をしましょう。トレース、監査、ログの機能は、とても重要です。システム管理者が幸せになれば、誰もが（特にあなたの上司が）幸せになれます。