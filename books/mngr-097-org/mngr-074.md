---
title: "【74】スコープ変更に慣れよう"
---


パベル・シムサ（Pavel Simsa）PMP



アメリカ、ワシントン州ベルビュー


　ソフトウェア開発プロジェクトとほかのプロジェクトに違いがあるとしたら、スコープ変更の発生がどれだけ不可避かという点でしょう。ほかのプロジェクトでもスコープ変更が決してないわけではありませんが、ソフトウェア開発ほど絶えずスコープが変動する業界はなかなか思いつきません。

　プロジェクトは 3 つの制約に支配されています。すなわち、コスト、時間、スコープです。

  - **コスト**：プロジェクトが困難に陥っているときには、さらに資金やリソースを追加投入しても助けになることはまずありません。作業員を 2 倍にすれば、半分の時間で穴は掘れるでしょう。しかし、ソフトウェア開発者を 2 倍にすることでプロジェクトが再び軌道に乗ることを期待するのは、有益どころか有害です。だれがどのコードに取り組むのか、どのようにするべきなのか、大きな混乱を招きます。したがって、コストは現状を維持する必要があります。
  - **時間**：プロジェクトには必ず「期日」があります。これはスケジュールに示された納期を意味しているとは限りません。公式にはだれも口には出しませんが、11 月にリリース予定の大規模セキュリティ製品を開発している場合、たとえ納品が 1 月まで延びたとしても、あなたの職はまだ大丈夫でしょう。チームは内心では、本当の「期日」は 2 月の、例えば「新しいリリースが発表される Black Hat セキュリティカンファレンスのとき」だと知っています。納期にはある程度の柔軟性があります。しかし、それもほんのわずかです。時間には制約があるのです。
  - **スコープ**：変化し続けるもの、それはスコープです。不思議なことに、スコープは最も柔軟性のある制約のひとつです。特定の顧客向けに構築したり、カスタマイズしたソフトウェアでなく、商用ソフトウェアを開発しているのであれば、なおさらです。理由は単純です。新しいソフトウェア製品のフィーチャーや機能には、「なくてはならない」ものと「あったらいいな」というものの 2 種類があります。通常「あったらいいな」というフィーチャーは「なくてはならない」フィーチャーの数倍以上あるものです。

　幸運なことに、「あったらいいな」というフィーチャーは最も削減しやすいものでもあります。もしあなたが超高層ビルを建設しているなら、プロジェクトの途中で「プロジェクトを再び軌道に乗せるために、アーキテクチャ計画にあった 60 個のストーリーのうち 40 個だけを構築することにしましょう。後で時間があるときに、残りの 20 個を追加すればよいでしょう」とは言えません。

　ソフトウェアの場合、「計画を変更しましょう。リリース 1 では 2 つの OS だけをサポートします。後でもともとサポートする予定だった残り 2 つを追加しましょう」と言うのは、比較的容易です。

　ただし、これは理想的な解決策とは言えません。では、どうすればこれを避けられるのでしょうか？

　正直に言うと、おそらく避けることはできません。これがソフトウェア開発プロジェクトの性質なのです。あなたにできることは、スコープをもっと具体的に計画することです。「あったらいいな」というフィーチャーと他のフィーチャーとの相互関係を最初から特定しておきましょう。相互関係は重要です。「あったらいいな」というフィーチャーを削減するとき、それが「なくてはならない」ものと関係があると、開発アーキテクチャの変更を余儀なくされるおそれがあるためです。

　最初から実行可能なスコープ削減を計画しておくことで、いざというときに何を削減すればよいのか、どうすれば簡単に削減できるのか、適切な判断を下せるでしょう。
