---
title: "【11】説明責任を果たす"
---


萩本順三


　複雑怪奇なソフトウェアを、システムに課せられる要件をクリアしつつ、わかりやすくシンプルに構築することはソフトウェア・アーキテクトとしての課題です。そのためには、タイトルに上げた説明責任を果たすことが重要です。

　この説明責任とは、たとえば開発者に対する責任です。しっかりとソフトウェア・アーキテクチャを設計し、そのコンセプトとデザインを的確に開発者に伝えなければなりません。その為には、アーキテクチャの説明書を書く際にも、誰に向けて書いているかを意識しなければなりません。たとえばドメインフレームワーク的なアーキテクチャを設計し自ら作成をする場合は、そのフレームワークを利用する開発者にわかりやすい利用説明書とチュートリアルを作りましょう。また、とにかくお手本となる利用するソースコードを示して一緒にプログラムすることも有用です。

　アーキテクチャについて、詳しいドキュメントを書いていながらも、利用してもらおうという意識が少ないものが多いように思います。理解し利用してもらうためには、工夫が必要となります。それは、最初の取りかかりの敷居を低くするために、シンプルでわかりやすい利用例を載せることです。また、ソフトウェア保守の局面で必要とされるドキュメントについては、アーキテクチャを保守の観点で仕組みの部分も含めて説明しなければなりません。

　開発中に保守ドキュメントの観点で、大量のアーキテクチャ・ドキュメントを書く人（プロジェクト）を見かけます。そのようなケースは、開発中にデザインが大きく変わった段階からドキュメントのメンテに追われ、挙げ句の果てには、開発したものとは異なるドキュメントになってしまいます。

　このような問題もあるため、開発中に必要とされるアーキテクチャ・ドキュメントと開発後の保守で使われるアーキテクチャ・ドキュメントは明確に分けて、作成することをプロジェクトで考えてみましょう。開発中のドキュメントは必要最低限にしつつ、しっかりと説明責任を果たすことが重要です。このことは、ソフトウェア・システムのオーナーにもしっかりと説明し、開発中のドキュメントと保守ドキュメントを明確に区別することが重要となります。

　また、開発関係者への説明だけではなく、技術者以外の人にも、ソフトウェア・システムのコンセプトを分かりやすい比ゆ（抽象的な図など）を使って表し説明できる能力を持てば、ソフトウェア・アーキテクトの価値は高まります。例えば、スポンサー、ユーザーにもソフトウェア・システムの有用性を含めてアーキテクチャを分かりやすく説明できる能力を持ちましょう。
