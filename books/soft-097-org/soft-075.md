---
title: "【75】設計するならコーディングできなければならない"
---


マイク・ブラウン


　アーキテクチャーでは、目の前の問題をエレガントに解決してくれる凝った設計や抽象化を作りたくなるものです。プロジェクトに新しいテクノロジーをちりばめたいという気持ちは、さらに抑え難いでしょう。しかし、最後は誰かがあなたの設計を実装しなければなりません。アクロバティックなアーキテクチャは、プロジェクトに影響を与えます。

　アーキテクチャーを設計するときには、設計の個々の要素を実装するために必要な作業量がどのくらいになるか、見当が付いていなければなりません。それらの要素を開発したことがあるなら、必要な作業量の見積もりは大幅に楽になるでしょう。

　設計の中で、自分では実装したことのないパターンを使うのは避けましょう。また、使ったことのないフレームワークに頼るのもよくありません。あなた自身が使ったことのない設計要素がアーキテクチャーで必要とされている場合、次のような困った副作用が発生します。

  - デベロッパーたちが直面する学習の苦しさをあなたが経験しない。新しいテクノロジーを修得するのにどれだけの時間がかかるのかを知らなければ、実装にかかる時間を見積もることはできないでしょう。
  - それを使うときに避けなければならない落とし穴がわからなくなる。そのテクノロジーの訓練を受けたエキスパートがやって見せたデモと同じようには、作業は進みません。そのテクノロジーがあなたの使ったことのないものなら、落とし穴にはまったときに戸惑ってしまいます。
  - デベロッパーたちからの信頼を失う。彼らが設計について質問してきたときに、はっきりとした答えを返せないようなら、彼らはあなたと設計に対して急速に不信感を持つようになるでしょう。
  - 不必要なリスクを持ち込んでしまう。使っているテクノロジーがわからなければ、ソリューションの重要な要素に大きな疑問符が付きます。余分な大きいリスクを抱えたプロジェクトに取りかかろうと思う人はいません。

　では、新しいフレームワーク、パターン、サーバー・プラットフォームの学習にはどのようにして取り組めばよいのでしょうか。これは、独立したもう1つの格言になります。「アーキテクトは何よりもまずデベロッパーであれ」（【63】を参照）。
