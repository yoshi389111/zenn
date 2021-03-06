---
title: "【67】待ち時間を無くせ"
---


中嶋 謙互


　プログラマの時間を奪うすべての要素を、ゲーム開発の作業場から取り除くべきです。ビルドを待つ時間から、ファイルを探してデスクトップをうろつく時間まで、可能な限りすべての要素を取り除く努力をすべきです。

　フロー理論によると、作業環境が「直接的で即座な反応」を欠いたり、「本質的な価値がない活動」をしている状態が続くと、集中が途切れ、注意力が散漫になるといいます。脳のワーキングメモリも、約 20 秒たつと大きく失われるといいます。実際に、ビルドが長かったり、必要なドキュメントがなかなか見つからなかったりが数十秒でも続くと、次に入力する予定だったコマンドラインを忘れたり、例外が起きていた位置を忘れたりといった経験がおありでしょう。人間の脳の性質上、このような小さな待ち時間が生産性に与える影響は極めて大きいのです。

　このことは、みんな、何となくわかっています。しかし、実際の自分のプロジェクトでこれを調査し、制作の仕方に反映することは、どの程度できているでしょうか？ 本質的な価値がない、20 秒以上かかる活動を全部リストアップし、その回数を数えてみたらどうでしょう。

　例えば開発環境の構築は 1 回ですが、更新作業は頻繁です。より多くのライブラリやサブモジュールに依存するほど、全体の更新頻度が上がります。ソースやデータの取得。バージョン管理システムや SSD の性能。ビルド。エミュレータやバーチャルマシンの起動。アーカイブ。パッケージスクリプト。起動の遅い外部ツール。不必要にバイナリ形式で保存したり通信したりして、デバッグがしづらくなっていないか。複数のサーバプロセスが必要な場合の再起動と初期化の自動化。教科書に書いてあるようなことですが、十分にできているでしょうか？

　開発中のゲームプレイでの「価値を産まない時間」を減らすのも、プログラマの腕の見せ所です。ローディングを速くする。必要になってから動的にデータをロードする。どこへでもワープできるようにする、スキップできるようにする、状態を保存して途中から再開する、リピートを自動化する、データを途中で変更できるようにする、などなど、作業時間を「即座に反応のある価値のある活動」だけにしていくには、プログラマとして本物の技術を発揮する必要があるのです。

　さらにチーム全体ではどうでしょうか。プレイアブルバイナリをチームメンバに配布する作業の自動化。チームメンバがプレイ開始してから、目的の操作をするまでに何秒かかるか。試して欲しいポイントに一発で飛べるか。説明不要になっているか。開発用サーバなのに毎回パスワードを打っていたりしていないか。クラッシュレポート。動作ログ。レポートの内容からコードにすぐ飛べるか。クラッシュ時のサーバなど他システムの状態。

　さらに運用を開始している場合はどうでしょうか。例外が起きたバージョンのコードがレポートに添付されているか。エラーが起きたときのサーバの状態記録をすぐ見れるか。企画調査の統計レポートを瞬間的に出せるか。

　待ち時間が徹底的に排除された環境は、プログラマだけでなくチームの全体が開発に集中できる環境でもあります。2 時間に 1 回しか試行できないチームより、1 時間に 10 回試行できるチームのほうが優れているのです。

　こうして待ち時間を減らすことで、全員が常に集中でき、多い回数の試行ができ、最終的には製品のクオリティに大きく貢献します。待ち時間のない環境をつくる努力を、決して惜しまないようにしましょう。
