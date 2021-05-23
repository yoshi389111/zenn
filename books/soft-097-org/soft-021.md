---
title: "【21】日程による失敗を避けるために"
---


ノーマン・カーノベール


　プロジェクトが失敗する理由はいくつもありますが、もっとも多いのは、まともな計画もなしに途中でプロジェクトの日程を変えることによるものです。こういったことによる失敗は避けられるものですが、さまざまな人々に大きな負担を強いる場合があります。日程を調整することやプロジェクトにかけるリソースを増強することが問題を起こすことはまずありません。おかしくなってくるのは、同じ日程で元の予定よりも多くの仕事をしてくれとか、仕事量を減らさずに日程を短縮してくれというような話になったときです。

　日程を短縮すれば、コストを下げたり、引き渡しの時期を早めたりできるという考え方は大きな誤りです。引き渡しを早めるために残業を求め、「重要度の低い仕事」（単体テストなど）を犠牲にするとか、引き渡しの日付を変えないまま機能を増やそうとするといった発想はよく見かけます。こういった流れは、なにが何でも阻止しなければなりません。変更を要求する人々には、次のようなことを考えてもらうようにしましょう。

  - 設計をせかすと、設計の出来が悪くなったり、ドキュメントに問題が出たり、品質やユーザーの満足度に問題が出たりする。
  - コーディングをせかしたり、引き渡しを早めようとしたりすると、ユーザーに渡されたコードのバグの数がてきめんに増える。
  - テストの日程を短縮すると、コードが十分にテストされないままになり、テスト関連の問題が増える。
  - いずれにしても、本番システムで問題が起きるため、修正にかかるコストが大幅に上がる。

　最終的にコストは削減されるどころか、増えてしまうのです。失敗が起きる理由はここにあります。

　あなたはアーキテクトとして、成功する確率を上げるために行動力を示さなければならない立場にあります。ただちに行動に移らなければなりません。まず、もともとの日程を維持するように交渉して品質を確保しようと努力します。どうしても日程を短縮しなければならないのであれば、それほど重要ではない機能を将来のリリースに延期するよう説得します。当然ながら、このような交渉のためには、綿密な準備や交渉力が必要ですし、説得力を高めるテクニックが必要です。今のうちにこれらの分野のスキルを磨いて準備しておきましょう。交渉を成功させれば、大きな満足が得られます。