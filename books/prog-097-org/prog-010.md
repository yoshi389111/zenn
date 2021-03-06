---
title: "【10】ツールの選択は慎重に"
---


ジョヴァンニ・アスプローニ（Giovanni Asproni）


　昨今では、アプリケーションをまったくのゼロから開発することは稀です。通常は、既存のツール——コンポーネント、ライブラリ、フレームワークなど——を組み合わせて作ります。それは次のような理由からです。

  - アプリケーションの規模は以前に比べて大きくなり、複雑で高度になってきている。対照的に、開発にかけられる時間は短くなる一方である。プログラマの時間と能力は、最大限有効に活かす必要がある。つまり、インフラのコードよりも、ビジネスドメインのコードに、時間と能力をできる限り振り向けるべきである。
  - 広く使用されているコンポーネントやフレームワークの方が、自前で開発しているものに比べ、バグが少ない傾向にある。
  - 多くの高品質のソフトウェアを Web から無料で入手できるようになった。これは、開発コスト削減につながるだけでなく、然るべき知識と技術を備えた技術者と出会う機会を増加させた。
  - ソフトウェアの開発や保守は多くの人手を要し、人件費の掛かる仕事である。一般的に言って、新しいものをゼロから作るよりは、すでに存在するものを買ったほうが安く上がる。

　ただ、既存のツールを適切に組み合わせることは、実は容易なことではありません。事前に十分な検討が必要でしょう。その際には、以下のようなことに留意すべきです。

  - コンテキストに関する前提条件はツールごとに違っている——たとえば、どういうインフラ、制御モデル、データモデル、通信プロトコルなどを前提とするかが、ツールごとに違う。注意しないと、アプリケーションと前提条件が一致しないツールを使ってしまう。そのような不一致があると、対処策、回避策を数多く講じる必要が生じ、コードが必要以上に複雑になってしまう。
  - ツールによってそのライフサイクルは異なる。利用しているツールを 1 つだけアップグレードするというのは、極めて困難で長い時間を要する。機能の追加、設計の変更、あるいはバグ修正などによって、他のツールとの齟齬が生じるおそれがある。利用するツールの数が多くなればなるほど、この問題は深刻になる。
  - ツールによっては、複雑な設定作業が必要になる場合がある。いくつもの XML ファイルを使用した設定が必要なツールも多い。そういうツールは、十分に注意をしなければすぐに制御不能に陥る危険性がある。多数の XML ファイルで設定を行うツールばかりを組み合わせてアプリケーションを作ると、結果的に大部分が XML で構成されていて、プログラミング言語で書いたわずかな量のコードを加えただけ、というようなアプリケーションができあがってしまうこともある。設定作業は極めて煩雑になってしまい、アプリケーションの保守や拡張も困難になる。
  - 特定のベンダのツールに過度に依存すると、いわゆる「ベンダロックイン」に陥ってしまう。そうなると、保守性、パフォーマンス、拡張性、価格などに制約が生じてしまう。ベンダの動向にどうしても影響されるからだ。
  - フリーソフトウェアを利用するからといって、全てが無料になるわけではない。商用サポートを受ける場合には、フリーソフトウェアだからといって、サポート費用が安いとは限らない。
  - ライセンスに関する条件の確認も重要で、それはフリーソフトウェアを利用する場合でもあてはまる。企業によっては、GPL ソフトウェアの利用が認められないこともある。GPL ソフトウェアの派生物は必ずソースコードとともに配布しなければならないという（ウイルスにたとえられる）条項が忌避される。

　ここまで挙げてきたような問題の発生を防ぐために、私は「まずは最低限のツールだけを導入する」という戦略を採っています。よく検討して、どうしても必要と判断したものだけに絞り込んで導入するのです。通常、初期の段階で重視するのは、「インフラ関連の低水準プログラミングの手間を省き、問題の発生を防ぐ」ということです。たとえば分散アプリケーションを開発するなら直接ソケットを扱うのではなくミドルウェアを利用する、ということです。その後も必要になったタイミングで新たなツールを追加していきます。新たにツールを追加する際には、ツールをビジネスドメインオブジェクトから隔離するためのインターフェースやレイヤを導入すれば、ツールの変更が必要になった時の手間が最小限に抑えられるでしょう。最後に、ここまで話してきたアプローチには良い副作用があります。当初の予測よりも導入するツールが少なくて済み、アプリケーションも肥大せずに済むのです。
