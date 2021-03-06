---
title: "【70】「完璧」は、「十分よい」の敵"
---


グレッグ・ナイバーグ


　ソフトウェア・デザイナーやアーキテクトは、与えられた問題に対してどれだけエレガントでどれだけ最適な解決策になっているかという基準でソリューションを評価しがちです。まるでミスコンの審査員のように設計や実装を見てしまい、変更、リファクタリングのためのイテレーションを数回追加すれば取り除けるような小さな欠点がすぐに気になります。ドメインモデルをあと 1 回点検すれば、基底クラスに移せる共通の属性や関数があるかどうかはわかるでしょう。複数の実装で重複しているサービスはウェブサービスにすべきでしょうし、クエリーが「バッファ読み出し」と一意でないインデックスについて警告を返してくるなら注意が必要でしょう。

　しかし、ちょっと待ってください。設計や実装を完璧なものにしたいという誘惑に負けてはなりません。「十分よい」レベルを狙い、そこまで達したら立ち止まるのです。

　「十分よい」というのはどこのことなのでしょうか？　それは、不備が残っていても、システムの機能、メンテナンス性、パフォーマンスにこれといった影響を与えないことです。アーキテクチャーと設計にずれがなく、実装は正しく動作してパフォーマンス要件を満たし、コードが簡潔明快でドキュメント化されていれば十分よいと言えます。もっとよくすることはできないのかと言われれば、もちろんできるのですが、十分よい状態なので、そこで止めるのです。勝利を宣言し、次の仕事に移りましょう。

　私の見るところでは、設計や実装で完璧を求めると、つい設計しすぎたりソリューションが混乱したりして、かえってメンテナンスが難しくなります。

　この本の他の項でも、さまざまなデザイナーたちが不要な抽象化、複雑さを避けよと言っています。なぜ、単純な状態を保てないのでしょうか。それは、完璧なソリューションを求めるからです。なぜ、きちんと動作するソリューションに余分な複雑さを持ち込む必要があるのでしょうか。単純な設計に残された不備を正したいという以外に理由はありません。

　アプリケーション開発はミスコンではありません。欠点を正して完墜にしようなどと考えて時間を浪費するのは止めることです。
