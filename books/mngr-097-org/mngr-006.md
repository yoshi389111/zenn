---
title: "【06】負債を支払う"
---


ブライアン・スレッテン（Brian Sletten）



アメリア、カリフォルニア州ビバリーヒルズ


　うまく管理できている限り、借入金（負債）は一般市民にとっても、成功している組織にとっても、有用な資金確保手段です。借入金を利用することで、将来の余剰金を借用して、現在の不足分を清算できます。賢く使えば、短期的借入金は現金の増減の凹凸をなだらかにする効果的なツールとなります。しかし使い方を間違うと、時が経つにつれて徐々に負担が大きくなり、やっかいな重荷となります。

　ソフトウェア開発の世界において、時間を借用するということは、やるべきことを何とかやり遂げながら、リスクのあるマイルストーンを達成するのに役立つ戦略です。ワード・カニンガムは、イテレーションの終わりや締め切りに向かいつつ、時間が足らないときに開発者が負担するものとして、「技術的負債」という考えを取り入れました。その時点では、完璧なコードは書けないかもしれませんが、いくぶん手抜きをすれば、開発者は完了基準に「十分適合した」コードなら書けるかもしれません。

　たとえソフトウェアが一時的に不完全な状態になっても、負担した技術的負債が責任をもって管理されているなら、これはまったく理にかなっています。しかし、技術的負債が支払えないでいると、やがてこれは苦痛になってきます。負債を返済せずに将来を担保にして借用し続けると、プロジェクトはさらに危険にさらされていきます。

　技術的負債を支払う一番よい方法は、各イテレーションの終わりにどんな「ローン」を組むか評価することです。開発者に依頼しましょう。やり直したいハックを具体的に特定して、それをやり直すのにどれくらいの時間が必要になりそうか、数値化してもらうのです。今すぐに負債を支払う必要はありませんが、どんな近道をしたのか開発者の頭の中に残っているうちに、今後必要になる修正範囲を調べておくのはよいことです。

　時間を好きなだけ要求するのではなく、コード上で書き直すべき問題が具体的にあるか確認しましょう。これはサボるチャンスではありません。コードベースをきれいにしておくための規律あるアプローチなのです。

　また、コードカバレッジ、カップリング分析、スタイル違反検出といったソフトウェア分析ツールがいろいろと出てきていますが、こうしたツールは負債が生じたところを自動的に特定するのに役立ちます。おそらく専門的な知識はほとんど必要ないはずです。こうして見つけた案件は課題管理システムに投入しておき、将来のイテレーションで実施するようスケジュールを立てましょう。新しいビジネス機能の開発とローンの支払いを盛り込み負荷のバランスをとることによって、顧客の機能要求を満足させながらも、技術的負債が手に負えなくなるのを防ぐことができます。

　ソフトウェアはいろいろな理由から不恰好になっていきます。しかし、ほとんどの責任は、ハックや不十分なドキュメント、不適切な依存関係、近道、意図した設計からの逸脱といったところにあります。開発者が降参してしまい、もう一度最初からやり直す必要があると言うときは、未払いの技術的負債が手に負えなくなったときです。彼らはソフトウェアを「破産同然だ」と宣言する必要性を感じたのです。

　そういう状態に陥る前に、負債を特定してすばやく対処しましょう。そうすることで、頻繁に「最低限の支払い」ができるようになり、次なる混沌を避けることができます。時間がたつにつれ、ソフトウェアがどのように手に負えなくなるのか、なぜコードをきれいにしておくことに投資すべきなのかを、ビジネス関係のステークホルダーに説明するとき、このたとえは驚くほど役に立つでしょう。
