---
title: "【12】フリーサイズのソリューションを求めるな"
---


ランディ・スタッフォード


　問題とは多様なもので、すべてを解決するようなソリューションは存在しません。ですから、アーキテクトは、いつも「場の感覚」を育て、働かせる必要があります。「場の感覚」という鋭い表現は、エバーハルト・レクティンが 1991 年に出した『システムアーキテクト設計：複雑なシステムの創造と構築』からの引用で、彼はその意味について次のように示唆に富むことを書いています。

> （複雑なシステムを構築するための「発見的アプローチ」の着想は、）ベテランアーキテクトにややこしい問題をいかに解決するかをたずねて得たものである。ベテランのアーキテクトやデザイナーは、たいてい「常識を働かせればいい」と答えるはずだ。……　これは、「常識」というよりも「場の感覚」といったほうが正確だろう。つまり、特定の場で意味を持つ知恵ということである。アーキテクトは教育、経験、実例を通じて「場の感覚」を磨き、10 年ほど経験を積んでシステム全体に影響があるような問題の解決を任される頃には、「場の感覚」が十分に蓄積されているのだ。

　ソフトウェア産業の大きな問題は、未熟なアーキテクトが、蓄積されている以上の「場の感覚」が必要とされる問題にたびたびぶつかっていかなければならないことです。おそらくこれは、ソフトウェア産業が、生まれてからせいぜい 2 世紀しかたっていないのに、爆発的な成長を遂げたからでしょう。この問題がなくなれば、ソフトウェア産業は成熟したということだと思います。

　私は、コンサルタントの仕事をしていて、この問題の実例をたびたび目にしています。よく見るのは、ドメイン駆動設計の適用に失敗するものです。現実的な視点から逸脱して、本来のニーズを満たすには大げさすぎるソリューションを作ったあげく、性能問題に陥り、問題解決とは無関係な提案や非合理な提案をしてしまうのです。

　ソフトウェアパターンのもっとも重要な知識は、いつ使うべきで、いつ使わないべきかということです。同じことが、要件分析における根本原因の特定や、問題の対処法を考えるときにも当てはまります。システムアーキテクチャーの設計でも、問題分析でも、いつでも使えるソリューションなどないということは明白です。アーキテクトは、アーキテクチャーの策定においても、トラブルシューティングにおいても、「場の感覚」を育て、働かせていかなければなりません。