---
title: "【61】ビルドをおろそかにしない"
---


スティーブ・P・バーチャック（Steve Berczuk）


　コーディングプラクティスについての規約は厳格に守っているのに、ビルドスクリプトに関しては無頓着、そんな開発チームは実はそう珍しくありません。その背後には、ビルドスクリプトなどさほど重要でないので、細かいことまで気にする必要はない、という思い込みがあるようです。あるいは、ビルドスクリプトはあまりにも複雑なので、難しいことはリリースエンジニアリングの専門家に任せた方がよい、と考えている人も多いかもしれません。どちらにしろ、適切な保守がなされず、重複やエラーを多く含んだビルドスクリプトを使用し続けていると、大きな問題を引き起こすことになります。その問題の深刻さは、汚いコードがそのままになっている場合と変わりません。

　技術力もあり、ルールを守って質の高いコードを書くプログラマが、ビルドのこととなると意外に無頓着になる。そうなってしまう原因は、ビルドスクリプトが、開発するソフトウェアそのもののコードとは違う言語で書かれるからなのかもしれません。彼らの頭の中では、ビルドスクリプトのコードは「コードではない」ということなのでしょうか。もしそうだとすれば、それはおかしな話です。最近では多くのプログラマが複数の言語を積極的に学ぶようになりました。ビルドスクリプトを書く言語も言語の一種ならば、積極的に学んでもいいはずです。それに、プログラマやエンドユーザが実行やテストをするための実行ファイルを作るのはビルドスクリプトなのです。コードはビルドされなければ何の役にも立たないし、アプリケーションのコンポーネントアーキテクチャを定義するのもビルドです。ビルドは開発プロセスの中でも特に重要な部分と言えるでしょう。ビルドプロセス次第で、コードをシンプルにし、コーディング作業にかかる労力を減らすこともできるのです。

　ビルドスクリプトは、不適切な書き方をしてしまうと保守が困難になる上、後で改善することも容易ではなくなります。そういうビルドスクリプトをどうすれば良いものに変えられるかを、時間を多少かけてでも是非学ぶべきでしょう。ビルドスクリプトのバグが顕在化するのは、誤ったバージョンのコードに依存してしまっている場合や、ビルド時の環境設定が不適切な場合です。

　以前はコードのテストというと、品質管理（QA）チームに任せておけばよいものとされていました。しかし今日では「質の高いコードを確実に提供するためには、コーディングとテストを並行して行うべき」という考え方が常識になってきています。それと同じように、ビルドプロセスも、これからは開発チームの仕事と考えるべきではないでしょうか。

　ビルドについて正しく理解すれば、開発のライフサイクル全体にかかる労力を減らしコストの削減をはかることもできるでしょう。ビルドが簡単に実行できるようになっていれば、入って日の浅い新人に担当してもらうこともできます。また、ビルドの設定を自動化しておけば、プロジェクトに関わる人の数が増えても、得られる結果がまちまちということがなくなります。「A さんのマシンでは動くのに B さんのマシンではダメ」というようなことが起きなくなるのです。コードの品質についてレポートするツールも数多くあるので、そうしたツールを使えば問題の存在をいち早く察知できるでしょう。ビルドについて深く学べば、自分自身だけでなく、必ず開発チーム全員のためになるはずです。質の高いビルドスクリプトを作り、ビルドにかかる手間を省くことができれば、皆がコーディングの作業に集中することができ、作業がより楽しいものになるからです。それは関係者全員にとって喜ばしいことです。

　ビルドプロセスについての理解が十分ならば、それに変更を加える時期や方法などもよくわかります。ビルドスクリプトも、開発するソフトウェアのコードと同様、やはりコードです。しかも非常に重要なコードですから、とても他人に任せるわけにはいきません。そもそもビルドなしではどんなアプリケーションも完成しません。プログラミングの仕事は、動作するソフトウェアを提供するまで決して終わらないのです。
