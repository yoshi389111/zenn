---
title: "【77】偶然の仕様ではなく本物の仕様のためのテストを書く"
---


ケブリン・ヘニー（Kevlin Henney）


　ソフトウェアをテストする際の典型的な落とし穴は、現状の実装コードのやっていることを、あまりに細部にいたるまで厳密にテストしてしまうことです。「細部にいたるまで厳密に」というと一見良いことのようですが、言い方を少し変えれば、なぜ問題なのか分かってきます。テストの典型的な落とし穴は、実装の詳細にテストを強結合してしまうことです。実装コードには、元々の設計でそうしようと意図したわけではなく、実装の都合でたまたまそうしている、という部分が多くあります。そういう、いわば「偶然の仕様」までテスト対象としてしまうのは問題なのです。その仕様が守られているどうかを確かめても意味はありません。

　そういう実装コードの偶然の仕様がテスト対象となっていると、本来の仕様に沿うよう改良を加えることがテストを失敗させてしまうような、テストの誤検出を引き起こします。その時の対処としては、テストの方を修正するのが正しいのですが、コードの方を修正してしまうプログラマもいるでしょう。誤検出されたテストの失敗が本当のエラーだったりすることが何度もあると、不安や疑念を招いてしまいます。テストを修正するにしても、本物の仕様に合っているかを確認するよう修正すれば良いのですが、コードの改良より新たに生じた偶然の仕様に合わせて修正してしまっては何にもなりません。テストはきめの細かい、厳密なものでなくてはなりませんが、同時に、本当にテストすべきことは何かをよく考え、的確なものにする必要があるのです。

　たとえば、Java の `String.compareTo` や C の `strcmp` の結果値は、左側引数が右側引数より小さいと負の数になり、左側引数が右側引数より大きいと正の数になり、左側引数、右側引数が等しいとみなされれば 0 になります。このスタイルの比較は、多くの API で採用されています。C の `qsort` 関数の比較関数や、Java の `Comparable` インタフェースの `compareTo` などもその例です。「より小さい」や「より大きい」を表す値としては、実際には「-1」「+1」が使われるのが一般的なので、絶対にこの値でなくてはならないと思い込み、その前提でテストを書くプログラマが多いのです。また、そのテストを皆で共有することもよくあります。

　同様の問題は、テキストの形式や内容を比較する際にもよく起きます。文字の間のスペースや、文字の構成に関して、「同じ」とみなす基準が色々に考えられるからです。しかし、たとえば設定変更可能なフォーマッティング機能を持った XML ジェネレータを書いているような場合を除いて、テキストに入っているスペースに重要な意味はないことが多いのです。その他、UI コントロールにおけるボタンやラベルの配置などについても同様のことが言えます。偶然その配置になっているだけにもかかわらず、それを絶対に守るべき仕様のようにみなしてテストをしたりすれば、将来、変更や改良を加える余地が減ってしまいます。実装に加えた些細な変更、重要でない変更によって、突然ビルドが中断してしまうということにもなるのです。

　厳密すぎる仕様にとらわれる傾向は、ホワイトボックスアプローチのユニットテストでよく見られます。ホワイトボックステストでは、どのようなテストケースが必要か判断する際、コードの構造を手がかりにします。そのため、現状のコードがしていることを、正しい仕様であると判断してしまいやすいのです。単に現状のものを良しとするテストでは、そもそも実施する意味があまりありません。「テストを実施した」というだけで、作業が進行したような錯覚、不当な安心感を持ってしまうこともあります。

　テストを効果的なものにするには、実装で生じた偶然の仕様を確認するのではなく、あくまでコードが元々の要求に合っているかを確認すべきです。それには、ブラックボックステストが有効です。テスト対象のコードの中身ではなく、外から見た動きに注目してテストを書くのです。動きが元々の要求に合っているかを見るのです。
