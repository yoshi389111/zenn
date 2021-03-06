---
title: "【66】解決策が 1 つしかない場合には、セカンドオピニオンを求めよ"
---


ティモシー・ハイ


　あなたもたぶん聞いたことがあるはずです。そして、あなたがベテランのアーキテクトなら、それが正しいことも知っています。「解決策が 1 つしか思いつかないなら、何か問題がある」ということを。

　ソフトウェア・アーキテクチャーとは、いくつかの制約がある中で、問題に対する最良の解決策を見つけることです。最初に思いついた解決策ですべての条件と制約を満足させられることは、まずありません。ですから、優先順位に従ってトレードオフを解決し、もっともうまく要件を満たす解決策を選ばなければなりません。

　問題に対する手持ちの解決策が 1 つしかない場合、トレードオフについてはもう交渉の余地がないということです。その解決策にシステムの利害関係者が満足できない可能性は十分にあります。また、ビジネス環境の変化により、優先順位が変わった場合でも、新しい要件に適応する余地がないということになります。

　本当に選択肢がなくて、解決策が 1 つしか見つからないことはまれです。おそらく、アーキテクトがそのドメインでは経験不足なのでしょう。自分でそうだとわかっている場合には、自分を抑えて経験のある他の人に助けを求めた方がよいです。

　アーキテクチャーが惰性で設計されている場合、問題はもっと悪質です。特定のスタイルのアーキテクチャー（たとえば 3 階層クライアント・サーバーシステム）でしか経験を積んでいないアーキテクトは、どういうときにそのスタイルが適合しなくなるかがわからないことがあります。他のアプローチと比較することもなく、自動的に解決策がわかってしまうような時は、立ち止まって 1 歩下がり、本当に他の方法はないかよく考えてみた方がよいでしょう。思いつかない場合には、助けを求めた方がよいかもしれません。

　私の友だちが、小さいながらも成長しつつあるインターネット企業で技術職をしていたことがありました。ユーザーベースが成長し始めていたので、システムの負荷に対する要件も厳しくなってきていました。パフォーマンスがまったく出なくなり、その企業は得難いユーザーベースの一部を失いかけていました。

　そこで、上司が彼にたずねました。「パフォーマンスを上げるにはどうすればよいかね？」

　友人は答えました。「もっと大きいマシンを買いましょう！」

　「他にできることはないのかね？」

　「ええと、私が知る限り、それだけです」

　友だちはその場でクビになりました。

　もちろん、その上司が正しかったのです。
