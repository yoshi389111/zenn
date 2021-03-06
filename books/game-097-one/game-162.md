---
title: "【62】応用力を高めるために基礎を学ぼう"
---


五反田 義治


　ゲーム開発は幸せな仕事だ。様々な技術や学問が、ここに集まり交錯する。そして、ビジネスになっている。お金が集まるところには才能が集まり、技術が進展する。

　私は、もともと数学が好きだった。ある日、高校時代の恩師は、受験勉強に集中するのが普通の３年生の授業だというのに、話が脱線してオイラー方程式の証明をいきなり黒板に書き出した。有名なという重要な定数や関数がひとつの式で統合される最も美しい方程式の一つだ。この式は直感だけでは捉えられない世界を教えてくれただけでなく、数式のもつ言葉で説明するのが難しい新しい感覚を与えてくれた。例えば数学が苦手な人に、ベクトル空間の概念を幾何学的に教える場合がある。確かに教える手段としては便利だ。しかし、それは人間の感覚の限界に閉じ込められることでもある。論理的な式の変形によって、様々な新しい概念が導出されて行く事を知ると、幾何学的な説明がまだるっこしくなる。100 次元、N 次元などを、感覚的に 3 次元に落とすことは難しい。もし、3 次元のユークリッド幾何学的な理解だけに頼れば問題の本質を見失ってしまう危険性がある。

　私はゲーム業界外の専門性のある人の話を聞くのが好きだ。例えば、CEDEC の講演者レセプションで、将棋 AI の Bonanza を開発した保木邦仁氏と話をする機会に恵まれた。Bonanza は機械学習という手法で、将棋 AI の世界に革命を起こしたソフトウェアだ。そして、開発者の保木氏自身は、もともと AI の専門家ではなく化学者出身であるところも面白い。私が Bonanza の実装について質問をしたり、レンダリングやアニメーションにおける最小自乗法の活用の話をすると、保木氏はそれに驚かれた。我々からすると当たり前でも、まさか CG の世界でそのようなテクニックを用いるとは思っておられなかったということだった。

　例えば、PRT（PrecomputedRadianceTransfer）と呼ばれるレンダリング手法がある。この手法では事前計算した大量の放射輝度データを圧縮するために様々な手法を利用するが、そのひとつに直交基底変換と CPCA（ClusteredPrincipleComponentAnalysis;クラスタ化主成分分析）を組み合わせる方法がある。PCA は統計解析の基本的なテクニックの一つで、大量のデータの次元を下げて計算量とデータ量を大幅に減らすことができる。同じテクニックが、各種データ圧縮やデータドリブンのプロシージャルアニメーション、データマイニングにも応用されている。一見して異なる技術のように見えるものが、根っこは同じテクニックで支えられているのだ。他にも CG で用いられるクオータニオンは、元々は純粋数学や物理学で用いられるテクニックだし、球面調和関数は量子力学で使われるテクニックだ。異分野を複数に渡り極めた者によって、理論のクロスオーバーが発生して、応用技術を大きく進展させる。

　このように、基礎を学ぶことによって新しい応用が拓ける。今、日本ではモバイルオンラインゲームが勢いを持っている。ここで使われている技術は、基礎まで掘り下げれば、他の分野にも応用出来る。繰り返しになるが、逆から見ればソーシャルグラフを捉えるためのビッグデータ解析で使われる PCA は、レンダリングやアニメーションにも応用できるのだ。

　そして今、日本のソーシャルゲーミングは世界の先端を走っている。お金と才能が集結している分野だ。ここで進展する各種技術は、この先、より高品質な、様々なゲームを開発するために応用できる。そのためには、表面的な実装や API の使い方を覚えるだけではなく、その理論的な基礎を学ぶことが重要だ。そして、ゲーム開発者は、それを「仕事」として行うことができる。何て幸せな職業なんだろう！
