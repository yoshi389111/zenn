---
title: "【62】シリアスゲームのつくりかた"
---


古市 昌一


　28 年間電機メーカーの研究所で人工知能（AI）と並列処理の研究を行い，その間に超並列コンピュータを存分に使える環境を求めてイリノイ大学へ留学、その後ウォーゲームシミュレーションシステムの事業化経験を経て、私は現在「シリアスゲームのつくりかた」を日本大学で教えている。

　そもそも私がウォーゲームを開発するきっかけとなったのは「第五世代コンピュータプロジェクト」で並列推論計算機の開発に約 10 年間従事したことである。私はオペレーティングシステム等の開発を担当し、本プロジェクトでの最後の仕事は CPU の利用効率を向上するための負荷バランサーの開発であった。その時やり残した仕事が、赤ずきんちゃんのような物語を自動的にコンピュータ上で生成できるような、マルチエージェントシミュレーションの実現であった。すなわち自律的に行動することができるさまざまなキャラクタをコンピュータ上に再現することで、仮想空間上で互いに会話や移動等を繰り返して物語が進行するシステムの実現であるが、その機会はやってこなかった。

　その後米国留学後に声がかかったのが、ミクロ交通シミュレーター開発プロジェクトへの参画だった。このシミュレーターはドライバーの意思決定モデルを搭載した多数の車を仮想空間上で再現し、次世代の交通管制装置等の開発に活かすことを目的としていた。個性を持ったドライバーが道路上を走行し、さまざまな要因で渋滞の発生が再現される様子は、かつてやりたかった物語の自動生成のようで、仕事が大変楽しかった。この課題は並列計算機の応用としても興味ある課題で、この仕事を通して我々は「時空間オブジェクトモデル」という並列計算機上で実行するマルチエージェントシミュレーションのための計算モデルを確立した。

　交通で成功したならば、もっと複雑な問題へも応用可能だと思っていたところ声がかかったのが、防衛を目的としたウォーゲームであったが、この開発には準備段階から数えて 10 年以上を費やした。現実世界での実験が不可能である戦闘を忠実に再現することが困難だったからである。そのために私が選んだ手段は、ウォーゲーム開発の先進国である米国の研究者から学ぶべく「シリアスゲームのつくりかた」を策定するための国際標準化委員会の委員になることだった。

　この委員会は当初米国防総省の下に作られた研究機関により運営され、その後学会組織 SISO となった。策定した標準化仕様は IEEE Std 1516.3，IEEE Recommended Practicefor High Level Architecture（HLA） Federation Development and Execution Process（FEDEP）となって欧米およびアジア各国の防衛用シリアスゲームの開発に利用されている。

　「シリアスゲームのつくりかた」の中核となった考え方は、そのシリアスゲーム（以後ゲームと呼ぶ）によって解決すべき課題と目的を明確にし、その範囲内でゲームを開発することである。また JIS 規格にもなっている SLCP（ソフトウェアライフサイクルプロセス）と同様に、ゲームの開発プロセスをフェーズに分けて、誰もが実行可能なように手順と必要な成果物等を明確化したことである。例えば指揮官の意思決定訓練で用いるウォーゲームに登場するレーダーであれば、ビーム幅やアンテナの回転速度等を考慮しなくてもよいといったことが、開発プロセスの中の概念モデル設計フェーズを実施することで、自動的に可能となる。

　各国の防衛用シリアスゲームは現在 IEEE Std 1516 に準拠したものが多数派を占めている。日本大学では教育や医療等を目的としたシリアスゲームの構築法を教え、多数の学部学生が毎年継続的にシリアスゲームを開発して学会発表している。遊びではないシリアスなゲーム。日本の大学で情報工学を学ぶ大学生がシリアスゲームのつくりかたを習得して社会に出て、国際会議でその学術的成果を発表するようになれば、日本のシリアスゲームソフト産業は世界一になれる。そう私は信じている。
