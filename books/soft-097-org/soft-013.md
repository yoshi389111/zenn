---
title: "【13】パフォーマンスの検討に早過ぎるということはない"
---


レベッカ・パーソンズ


　ビジネスユーザーは、主に機能要件を通じてニーズを説明します。パフォーマンス、安定性、稼働時間、サポートニーズなどの非機能要件は、アーキテクトからしか見えません。しかし、非機能要件のテストは、開発サイクルの非常に後の工程まで放置されていることが多く、場合によっては運用チームに完全に委ねられています。こういったことが当たり前のように起きていますが、間違っているのは明らかです。

　こうなってしまう理由はさまざまですが、おそらく、必要な機能をまだ実現できていないのに、スピードとか障害復旧性などと言っても無意味な感じがするからでしょう。環境やテスト自体が非常に複雑なことや、稼働システムでも初期バージョンならそれほど酷使されないだろうということもあるかもしれません。

　しかし、開発工程の後までパフォーマンスを意識しなければ、いつパフォーマンスに変化が見られたかについての膨大な情報をみすみす失ってしまいます。アーキテクチャー的にも設計的にもパフォーマンスが重要な基準になるのであれば、パフォーマンステストはできる限り早い段階で開始した方がいい。2 週間のイテレーションを基本とするアジャイルの方法論を使っている場合、パフォーマンステストは、第 3 イテレーションまでに始めるべきでしょう。

　なぜ、パフォーマンステストがそんなに大切なのでしょうか。最大の理由は、どのような変更を加えた時にパフォーマンスが急降下したかがわかることです。これならパフォーマンス問題に直面した時に、アーキテクチャー全体を相手にせず、最近に加えた変更に焦点を絞り込んでいけるのです。パフォーマンステストを早い段階から頻繁に行えば、検討すべき変更の範囲を狭めていくことができます。

　初期のテストでは、パフォーマンスの診断など、してみようと思いもしないかもしれませんが、作業の出発点とすべきパフォーマンスの基準線はあるはずです。この経過情報は、パフォーマンスを低下させている原因を診断し、問題を解決するために非常に重要な情報となるのです。

　このアプローチを取れば、実際のパフォーマンス要件に基づいてアーキテクチャー、設計上の選択をチェックすることもできます。厳しい条件を抱えたシステムでは特に、早い段階でのチェックが納品を遅らせないようにする上で重要な意味を持ちます。

　技術的なテストは実施が難しいことで知られています。適切な環境をセットアップし、適切なデータセットを生成し、必要なテストケースを定義するのは、いずれも時間のかかる仕事です。早い段階でパフォーマンステストに取り組めば、テスト環境を少しずつ整備していくことができますし、パフォーマンス問題が見つかったときにもコストを抑えられるでしょう。