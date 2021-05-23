---
title: "【67】変化の影響を把握せよ"
---


ダグ・クロフォード


　優れたアーキテクトは、複雑さを最小限に圧縮し、システムの構築のしっかりとした基礎を提供するような抽象化を実現するとともに、変化に適応できる実用性も備えた設計を編み出します。

　優れたアーキテクトは、変化の影響を把握しています。個々で言う変化には、個別のソフトウェアモジュールの変更にかぎらず、人と人との間、システムとシステムの間の変化も含まれます。

　変化は、さまざまな形で姿を表します。

  - 基本要件の変更
  - スケーラビリティに対するニーズの拡大
  - システムインターフェイスの変更
  - チーム内の人の出入り
  - その他多数……

　ソフトウェア・プロジェクト内での変化の範囲の複雑さは、あらかじめ読めるものではありませんし、通る前に道のすべての「こぶ」に対処しようとしても実りはありません。しかし、そのような「こぶ」がプロジェクトにプラス・マイナスのどのような影響をあたえるかを見極めるために、アーキテクトは非常に重要な役割を果たすことができます。

　そのようなアーキテクトの役割とは、必ずしも変化をコントロールすることではありません。むしろ、変化をコントロール可能なものにすると言ったほうがよいでしょう。

　たとえば、多くのアプリケーションを抱え、部品の統合のためにさまざまなミドルウェアを使って高度に分散化されたソリューションについて考えてみましょう。ビジネスプロセスに変化が生じた時に、依存関係を正しく追跡できなかったり、何らかのビジュアルモデルで正確に表現できなかったりすると、破壊的な影響が及ぶ場合があります。変化によってデータモデルが影響を受けたり、既存のインターフェイスが役に立たなくなったりする場合、あるいは、既存の成長実行中のステートフルなトランザクションを古いバージョンのプロセスのもとで成功させて完了させなければならない場合には、末端への影響はとりわけ大きくなります。

　この例は極端に感じるかもしれませんが、今はこのように高度に統合されたソリューションが主流になっています。それは、統合のための標準群、フレームワーク使えるパターンなどで何が選ばれているかを見れば明らかです。システムの外郭が変わることの意味を理解することは、顧客に対して持続的なサポートを維持するためにとても大切な意味を持ちます。

　幸い、変化の影響を緩和できるツールやテクニックがいくつもあります。

  - 変更は小幅に差を把握できるように行う。
  - 繰り返し使えるテストケースを作り、それを頻繁に実行する。
  - テストケースの構築を楽にする。
  - 依存関係を追跡する。
  - 作用、反作用を系統的にする。
  - 反復的な仕事を自動化する。

　アーキテクトは、プロジェクトのスコープ、日程、予算のさまざまな側面に対して変化が及ぼす影響を見積もり、「道のこぶ」のためにもっとも大きな影響を受けそうな部分により多くの時間を割けるよう準備を怠らないようにしなければなりません。貴重な時間をどこに費やさなければならなくなるかを知るためには、リスク計測が役に立ちます。

　複雑さを圧縮することは大切ですが、複雑さを圧縮したからといって、単純になるとは限りません。しかし、ソリューションにどのような変化が起き、それがどれくらいの影響を及ぼすかを把握することには、中長期的に計り知れない効果があります。