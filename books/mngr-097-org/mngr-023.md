---
title: "【23】巧妙なコードはメンテナンスが困難"
---


デイビッド・ウッド（David Wood）



アメリカ、バージニア州フレデリックスバーグ


　開発者は奇跡を求められるものです。現在のプロジェクトのコードを多数のパッチを含んだ時代遅れのレガシーソフトウェアとともに動かすため、開発者は巧妙な方法を見つけなくてはなりません。開発者のスキルと創造力をもってすれば、最終的にその仕事をやり遂げる巧妙なコードが作れるかもしれません。しかし、巧妙なコードはその長さや複雑さのために、将来のメンテナンス問題を引き起こしかねません。

　あなたがソフトウェア開発に不慣れなプロジェクト・マネジャーであれば、ためらわずに開発者に新しい言語や開発ツールを調べさせましょう。開発者に自由を与えるのです。これは開発者のコーディング実務や成果物を改善する革新的な手段になるためです。レガシーなインターフェイスに対して、開発者はもっと高速で、テストやメンテナンスすべきコードが少なくて済むソリューションを設計できるかもしれません。プロジェクトにとって、これは間違いなく有益です。

　現在のコードと同じ機能を大幅に少ないコードで実現できるような、革新的な新しいプログラミング言語もあるかもしれません。こうした言語を利用すると、コードの構造がはるかにシンプルになり、テストしやすく、自己定義可能で、保守すべきものも小さくなり、メンテナンスしやすくなるといった利点があります。

　もちろん、新しい言語やプラットフォームを導入する際には懸念もあります。新しいコードは現在開発中のソフトウェアやアップグレードにとって、本当に解決策になり得るのでしょうか？　これまで投資してきたレガシーなデータベース、ユーザーインターフェイス、サードパーティ製ソフトウェアで使われている既存のソフトウェアとの整合性は、長期にわたってとれるのでしょうか？　チーム内や部門内に、この新しい言語やプラットフォームを使ってソフトウェアを作れる開発者がほかにいるのでしょうか？　その言語の作者から適切な製品サポートを受けられるのでしょうか？　タイムリーにアップデートや改良がなされるのでしょうか？

　たとえあなたがプログラミングに詳しくなくても、プログラマが新しい言語を導入するのを渋ってはいけません。もし新しい言語が C や Java の流れをくむものであれば（あるいは、よくある一般的な処理方法のものであれば）、それを現在のやり方にマージするのはそれほど苦痛ではないでしょう。

　ただし、コードに新たに変更点がある場合には、必ずドキュメント化しておきましょう。そうしておかないと、コードとドキュメントが枝分かれしてしまい、システムを理解するにはコードを見るのが一番、ということになってしまいます。これはソフトウェアコンポーネントとシステムメタデータの「結合の喪失」とも呼ばれます。また、ソフトウェアをメンテナンスする上で不適切なドキュメントがあれば、それを置き換えなくてはなりません。

　プロジェクトチームにいる開発者が革新的になれるよう後押ししましょう。ただし、複雑すぎるほど巧妙であってはいけません。あまりに巧妙にやってしまうと、あとに続く人が苦労します。もしあとに続く開発者がコードを読めなければ、どうやってメンテナンスすればよいのでしょう？　プログラマはみな自らの雇用確保のために巧妙にやろうとしますが、プロジェクト・マネジャーはそこから得られるものはありません。

　巧妙すぎるコードは結局のところ、メンテナンスを困難にします。最終的に、ソフトウェアはメンテナンス不能になり、作り直しのために高くつくことになるでしょう。
