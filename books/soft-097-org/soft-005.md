---
title: "【05】パフォーマンスの決め手はアーキテクチャー"
---


ランディ・スタッフォード


　アプリケーションのパフォーマンスの決め手になるのは、アプリケーションのアーキテクチャーです。そんなのは当たり前だと思われるかもしれませんが、現実の世界ではそうでもないのです。たとえば、ミドルウェアの製品を変えるだけで、パフォーマンスの問題が解決すると思っているソフトウェア・アーキテクトは山ほどいます。たぶん、ベンダーが宣伝する「ベンチマークテストの結果は、ライバルと比べて 25% も上回っています」という言葉に踊らされているんでしょう。しかし、アーキテクチャーの効率がとてつもなく悪く、それがパフォーマンスの悪さの根本的な原因になっている場合、ライバル製品なら 4 ミリ秒かかるところを、わずか 3 ミリ秒で処理できると言っても、その 1 ミリ秒、25% の差は、焼け石に水です。

　これは IT マネージャーやベンダーのベンチマーク・チームの言い分ですが、ベンダーのサポート部門やパフォーマンス管理について書くライターには別の言い分があります。メモリー割り当て量、コネクションプール数、スレッドプール数といったものを調整してソフトウェアを「チューニング」すればパフォーマンスが上がるというのです。しかし、予想される負荷と比べてアプリケーションの配備環境が貧弱だったり、そもそものアーキテクチャーがリソースを効率的に使えていなければ、いかにアーキテクトがチューニングしても、パフォーマンスやスケーラビリティは、要求水準にとうてい及ばないでしょう。

　ベンダー製品もアプリケーション・アーキテクチャーも結局のところ、分散コンピューティングの基本原則と物理資源の制約を受けます。アプリケーションにしても、ベンダー製品にしても、ある性能のコンピューターの上でプロセスとして実行され、ネットワークやメモリを介して連携するときにはかならず遅れが生じます。ですから、アプリケーションのパフォーマンスとスケーラビリティを左右する最大の要因は、アプリケーションのアーキテクチャーだということを肝に銘じなければなりません。パフォーマンスやスケーラビリティは、ブランドとか「チューニング」だけでスイッチを押すように改善されるような代物ではないのです。これらを改善したければ、根本的なロジックか配備環境そのもの、あるいはその両方の（再）設計が必要なのです。
