---
title: "【09】移り気な利用者を捉える"
---


牧野友紀


　われわれアーキテクトが挑戦しなければならない課題が顕在化しつつあります。それは、事前に想定しきれない多様な利用者、どう変わるか予想できない利用者を相手に、柔軟に対応するアーキテクチャを考えることです。

　我々が対象とするアーキテクチャとは、ソフトウェアの構造と制御のことであり、情報システムが時間と空間の観点で安定的に機能する仕組みです。時間の観点では、長期にわたり変わらず機能する安定性を実現することであり、アプリケーションが変わっても、トランザクション量が増えてもアーキテクチャは不変であることが求められます。空間の観点では、情報システムの利用者と情報源の関係に柔軟性を実現することであり、これをおろそかにすると一度は利用者の要求に応えるものの直ぐに老朽化します。

　今、チャレンジしなければならないのは、空間的な問題を解くことです。例えば旅行商品の販売における利用者を考えてみましょう。店頭では販売員が情報システムを利用し、旅行者に対してサービスを提供します。一方、オンラインになれば、旅行者自らは情報システムを利用し、セルフサービスで旅行商品を申し込むことになります。重要なのは、どこにいようが旅行者は「旅行会社が提供するサービスの利用者」だということです。たとえ直接は情報システムを利用していない場合でも、広い意味で利用者として定義されるべき存在なのです。

　インターネットの登場を境に、情報システム開発で意識する利用者の比率が年々変わっているのです。以前は、開発を依頼するクライアント（旅行会社）の情報システム部門がイニシアティブを持ち要求を定義できました。その後、クライアント内の利用者（店頭販売員）がイニシアティブを持ち、今ではクライアントの顧客である利用者（旅行者）のイニシアティブが強くなりました。そのため、情報システムに対する要求の範囲が広がり、多様で変化し続けるようになったのです。先の例では、旅行者の要求は、「予算内で満足度が高い旅程を立てる」ことです。この要求は、旅行者の旅の目的や好みなどに分解され、その内容は多様です。露天風呂付、ペットと泊まれる、子供が楽しめる、グループ旅行に最適、空港の近くなどあげればきりがありません。当然ながら、これらを組み合せることもあります。利用者全員の全ての要求を、事前に定義することは現実的には不可能でしょう。

　情報システム開発者には要求分析を厳密に行えば、暖昧性を排除し、抜けをなくせるという「幻想」があります。私は、これを捨てねばならないと考えています。なぜなら要求を聞く相手がいないからです。前述の通り、全ての利用者に話を聞くことは不可能でしょうし、現実的な人数で聞くとしても誰に聞けばいいのか分からないのです。クライアント内の利用者（店頭販売員）に話を聞いたとしても、その要求が正しいという保証はないでしょう。とはいえ、これは要求分析をしないということではありません。

　ではどうするか？　クライアントが関わりたい利用者を想定し、その目的と振る舞いを仮定し、検証を行うことを繰り返すのです。仮説に基づき情報システムを開発し、運用することで検証します。利用者は、なぜそのサービスを利用したのか、なぜそのサービスを使って特定の情報を得たのかなど、利用者の目的や意図の一部を形式化することです。蓄積した新たな形式知により、利用者の目的にサービスをフィットさせることができます。また、新サービスや新製品を考える種を与えることもできるのです。

　そのために、我々情報システムの開発者ができることは、利用者の動向を観測し、適応することが可能なアーキテクチャを提供することです。こんなことができれば、情報システムの利用者は初めて、われわれアーキテクトの存在と意義に気付くかもしれません。