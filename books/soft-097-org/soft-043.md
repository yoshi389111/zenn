---
title: "【43】状況がなによりも大切"
---


エドワード・ガーソン


　理想などないという前提からスタートしたいと思っている私が、アーキテクチャーの理想について何かを書こうとしているのは、何とも皮肉な感じです。理想が本当にないのなら、書くべきことはないはずです。私は矛盾しており、こんなことをすれば宇宙が爆発するのではないかと恐くなります。

　しかし、「これはパイプではない」（ルネ・マグリット）

　私がソフトウェアアーキテクトとして学んだことの中で特に役に立ったのは、何よりも大切なのは状況で、シンプルはそのために必要なものだということです。実際的な言葉で言えば、アーキテクチャー上の決定を下すときに、シンプルよりも優先すべきものは状況だけだということです。

　ここで言う**状況**には、企業の主要行動要因のようなハイレベルの直接的な力学だけではなく、新技術やさまざまなトピックでの優位性といった周辺的な要素も含まれます。実際、優れたアーキテクトは、変動の激しい複数のターゲットを視野に入れておかなければなりません。

　では、優れたアーキテクチャーとは何でしょうか。それは、複数の競合する優先項目にまみれた状況下での意思決定の産物です。複数の競合する優先項目という言い方をしたのは、何を入れるかではなく、何を省くかかがもっとも重要な基準になることがあるからです。優れたアーキテクチャーとは、単純に抜け目のない意思決定のことです（あなたの意図を伝えるのは、意思決定の産物だけですが）。

　歴史を振り返ると、状況がアーキテクチャーに影響を与えた面白い例がいくつかあります。私が気に入ってる例は、新しい戦車用ソフトウェアシステムをサポートするために選択されたデータベースの話です（どのデータベースを使うかがアーキテクチャー上重要な意味を持つことは普通ありません。この例から読み取っていただきたいのは、状況が大切だということだけです）。

　開発チームは、データベースを選択するという段階に入ってから、多くのものを評価しました。戦車は、目標の追尾中、凹凸の激しい地面を高速に移動しますが、ナビゲーションや目標の追尾のために必要な最大限のスループットは、ほとんどのデータベースが確保していることがわかりました。しかし、戦車が主砲を発射すると、強力な電磁波が発生し、データベースはもちろん、オンボードシステム全体を完全にクラッシュさせてしまうことがわかったときには、チームはあわてました。現代の戦場では、ソフトウェアなしで戦車を走行させることは、闇夜を走らせるのと同じことです。この状況のもとで、データベース選択の圧倒的な決定要因となったのは、修復にかかる時間でした。そして、当時はその点で InterBase 以上のデータベースはありませんでした。M1 エイブラムスで InterBase が選ばれたのは、そのためだったのです。

　ニュースグループは X か Y かの技術論争で大荒れになることがありますが、そんなものはただの暇つぶしにしかなりません。これらの論争が激しくなるのは、技術的な長所に大きな差があるからではありません。決定的な切り札となる状況の中での問題が設定されていないのに、それぞれの論者が評価するポイントがまちまちで、しかもそれらの間には微妙な差しかないからです。

　あなたのチームは理想から自由でなければなりません。まず何よりも状況について考え、そこからもっともシンプルなソリューションにたどり着くようにすべきです。