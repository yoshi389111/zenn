---
title: "【32】デベロッパーに自己裁量を与えよ"
---


フィリップ・ネルソン


　ほとんどのアーキテクトは、デベロッパーとしてキャリアをスタートさせます。アーキテクトになると、システム構築方法の決定に関して新たな責任を負い、権限が重くなります。もっとも、アーキテクトという新しい役割を与えられでも、デベロッパーとしてやっていたことはなかなか止められないなあと思うかもしれません。それだけならまだいいのですが、デベロッパーが設計を実装するためにすべきことを厳しく管理することが自分の大切な仕事だと思うようなら、かなりまずいことになります。あなたとあなたのチームに成功をもたらすためには、チームメートに自己裁量を与えてそれぞれの創造力とコーディング能力を発揮させることがとても大切なのです。

　デベロッパーの頃のあなたは、1 歩下がってシステム全体がどのような仕組みになっているのかを本当の意味で見渡したことはまずなかったでしょう。しかし、アーキテクトになってからは、それがあなたのもっとも大切な仕事です。デベロッパーたちは、目を血走らせてクラス、メソッド、テスト、ユーザーインターフェイス、データベースを構築していきますが、あなたはそれらすべての部品が全体の中でうまく機能するように調整しなければなりません。それだけでなく、うまくいかないところを聞き出して、改善する必要があります。

　テスト担当が苦労していませんか？　それならインターフェイスを改良して、依存関係を減らさなければなりません。抽象化が必要なところとそうでないところが見分けられていますか？　そうでないならドメインをはっきりさせましょう。どの順序で部品を組み立てたらよいかわかっていますか？　そうでないならプロジェクトプランを立てましょう。あなたが設計した　API　を使っているデベロッパーたちが、同じ過ちを繰り返ししていませんか？　そうでないなら設計をよりわかりやすいものにしなければなりません。チームメンバーは本当に設計を理解していますか？　そうでないならコミュニケーションを取って、明確にしていきましょう。スケーラビリティが必要なところとそうでないところが見分けられていますか？　そうでないなら顧客と話し合って彼らのビジネスモデルを学ばなければなりません。

　アーキテクトとしてよい仕事をしているときには、デベロッパーの邪魔をしている時間はないはずです。確かに、設計が意図通りに実装されているかどうかを確かめる程度にはじっくりと見る必要はあります。しかし、その目標を達成するために、メンバーの仕事ぶりを監視する必要はありません。メンバーが苦しんでいるのを見かけたときにヒントを与えるのはよいことですが、彼らの方からあなたにヒントをもらいにくるような環境を築ければ、その方がなおよいでしょう。あなたがアーキテクトとしてよい仕事をしていれば、アーキテクチャーを成功に導くことと、デベロッパーやチームメートの創造力や知性を押さえつけることとの間に、明確な境界線を引けているはずです。