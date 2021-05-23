---
title: "【88】問題を解こうとするな"
---


イーベン・ヒューイット


　一部の例外を除き、アーキテクトはデベロッパーだった人たちです。デベロッパーは、プログラミング問題を解決すると評価されます。しかし、プログラミング問題のスコープは、アーキテクチャー問題と比べればかなり小さなものです。プログラミング問題の多くは、小さく、難しいアルゴリズムの問題です。プログラマーの面接、本、大学の授業などでは、純粋なプログラミング問題というようなものがあるかのように、よくこの手の問題が目の前に置かれます。難しさは魅力的で人の心を誘惑します。

　時間がたつにつれて、私たちは深く考えずにそれらの問題を受け入れるようになっていきます。この問題に意味があるのか、面白いのか、役に立つのか、倫理的にどうなのかといったことを考えません。大きな全体図と問題の関係を考えても、誰も評価してはくれません。私たちは、問題を解くことに集中するように訓練されていきます。難しい問題を解くのは大変なだけに、その傾向にはさらに拍車がかかります。面接では、まず任意の制約のもとでいくつかのゼリービーンズを並べ替えるような作業が待っています。私たちは制約について疑問を持たないように教育されます。制約は、教師、面接官、メンターがすでに知っていることを私たちが発見するように導くための教育手段なのです。

　アーキテクトとデベロッパーは、すぐに問題解決モードに入るように教育されています。しかし、最良の解決は解決しないことだという場合があります。多くのソフトウェア問題は、一切解決しなくてよいのです。それらが問題のように見えるのは、ただ現象だけを見ているからです。

　たとえば、マネージドメモリについて考えてみましょう。マネージドプラットフォームを使うデベロッパーは、メモリ問題を解決したことがありませんし、多くは要求されてもメモリ問題を解決できないでしょう。彼らには基本的にメモリ問題そのものがないからです。

　さまざまな標準や慣習に従いながら無数の絡み合ったスクリプトを書かなければならない複雑なビルドについて考えてみましょう。あなたは、自分のスクリプト作成能力と最良のプラクティスを駆使して問題を解き、すべてをうまく動かし、大きな満足感を得ます。同僚たちは感心してくれます。逆に問題を解かないことに感心してくれる人はいません。しかし、1 歩下がって、解決するのはビルドの問題ではなく、自動処理と移植性の問題だということに気付いたら、問題を抽象化してくれるツールを選べるはずです。

　アーキテクトはすぐに問題解決モードに入りがちなので、問題自体について考えてみることを忘れてしまいます。でなければ、最初から問題についてどう考えたらよいかを学んでいません。与えられたものをただ受け入れるのではなく、問題が本当に適切に立てられているかどうかを確かめるためには、望遠レンズのようにズームイン、ズームアウトを繰り返すことを覚えなければなりません。ペッツのディスペンサーのように、与えられた要件をため込み、もっとも賢いソリューションをはき出すような地位に満足していてはいけないのです。

　問題を与えられると同時にすぐに解きにかかるのではなく、問題を変えられないかどうかを考えてみましょう。この問題がなければ、アーキテクチャーがどのようになるのかを自問自答してみることです。こうすれば、よりエレガントで長持ちするソリューションが得られる場合があります。ビジネス問題は解決しなければなりませんが、与えられると同時に解決する必要はないのです。

　私たちは、「問題」中毒を治さなければなりません。ヨーロッパの橋の上で、ミッションが書かれた「自動的に消滅する」封筒を手渡されたばかりの秘密機関のエージェントのように、私たちは問題を与えられるのが好きです。問題に対する答えを考える前に、この問題がなければ、世界がどのように見えるのかを考えるようにしましょう。