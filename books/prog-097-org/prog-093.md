---
title: "【93】エラーを無視するな"
---


ピート・グッドリフ（Pete Goodlife）


> 　ある夜、私は、バーに向かって街を歩いていました。友人たちと会うことになっていたのです。彼らと一緒に飲むのも久しぶりだったので、楽しみにしていました。でも早く行かねばと焦り、周りがよく見えていなかったのでしょう。縁石につまずいて、見事に転んでしまいました。注意力散漫だったわけですから、まあ自業自得です。
> 
> 　脚が痛みましたが、早く友達に会いに行かねばと思っていたので、立ち上がり、歩き続けました。しかし、歩くほどに、痛みがひどくなってきます。はじめのうちは転んだショックの方が大きく、よくわかっていなかったのですが、どうもこれは、ただごとではないぞという痛みでした。
> 
> 　私はそれでも構わずバーへと急ぎました。着く頃には、痛みは激痛になっていました。痛みにばかり気を取られ、せっかく来たのに結局はあまり楽しめませんでした。朝になって医者に行ってみると、脚の骨が折れているとの診断です。痛みを感じた時、そこで止まっていれば、歩き続けなければ、もっと軽く済んだでしょう。それは私のこれまでの人生で最悪の朝でした。

　実を言えば、コードを書くときに同じようなことをしているプログラマはとても多いのではないかと思います。

**エラーが起きているのに、大したことはないと思い込もうとする。大丈夫だと自分に言い聞かせて無視する。** そんなことをしても**何も良いことはない**のです。これでは品質の高いコードはとても書けないでしょう。これは単なる怠惰（良い「怠惰」ではなく、ひどい方の「怠惰」）です。たとえどんなに問題の起きにくいコードでも、エラーチェックとエラーハンドリングは常に必要です。省略しても時間の節約には決してなりません。後でもっと大きな問題が起きる原因を作っているだけです。

　コードからエラーを通知する方法は数多くあります。その例をいくつか挙げておきましょう。

  - **戻り値を使う。** 関数が正しく実行されなかった時、そのことを示す値が戻るようにしておく。ただし、戻り値は無視されやすく、たとえ重大な問題が潜んでいても、戻り値だけでは伝わりにくい。実際 C の関数の戻り値には「無視するのが普通」とされているものさえある。たとえば、printf の戻り値をこまめにチェックしている、という人が果たしてどのくらいいるだろうか。

  - **errnoを使用する。** errnoはエラー通知の役割だけを担うグローバル変数で、C の中でも特異な存在である。やはり、無視されやすく、使いづらく、そして数々の厄介な問題の原因にもなる。たとえば、複数のスレッドが同じ関数を同時に呼び出したとしたらどうなるだろうか。プラットフォームによっては、その際に発生する問題を回避できる仕組みがあらかじめ用意されている場合もあるが、そうとは限らない。

  - **例外を使用する。** 例外は構造化されたエラー通知・処理の仕組みである。エラー通知とハンドリングの方法は言語仕様で定められている。例外が無視されることを防ぐことも可能だが、絶対に無視されないというわけではない。何度か見たことがあるが、たとえば次のようなコードを書かれてしまう。
    
    ``` java
    try {
        // …何かの機能のためのコード…
    } catch () {} // 例外は無視する
    ```
    
    この方法で例外は握りつぶされてしまう。ただこの場合の救いは、こういう類のコードが書かれているときは、書き手の姿勢に問題があるとすぐにわかることだ。

　エラーが起きているのに、無視する、見て見ぬふりをする、何も起きていないことにする、そういう態度では、リスクが非常に大きくなってしまいます。私が痛みを感じても歩き続け、脚の状態を悪化させてしまったのと同じです。警告を無視して進むと、事態が余計に面倒になってしまうのです。問題の存在を察知したら、できるだけ早く対処すべきです。先延ばしは禁物です。

　エラーを放置すると、次のようなことが起きます。

  - **不安定なコードができる。** 大きな問題を引き起こすバグを多く抱えたコードができる。しかも、修正しにくいバグが多い。
  - **セキュリティ上問題のあるコードができる。** クラッカーがシステムに侵入する際は、エラー処理に不備がある箇所を利用することが多い。
  - **貧弱な構造とインタフェース。** 利用側のエラーハンドリングが煩雑で面倒なコードを書いてしまったときには、そのコードのインタフェースが良くない可能性がある。発生し得るエラーを明示し、重大でない場合の対処は少しでも楽になるような工夫をする必要がある。

　自分の書いたコードから発生し得るエラーを丹念にチェックするだけでなく、発生し得るエラーとその条件をインタフェースに明示しましょう。エラーを隠蔽し、何も問題なく動いているかのように見せかけてはいけません。

　なぜエラーチェックをしないのでしょうか？　やらない理由（言い訳）も色々あるので、その例を以下に挙げておきます。「自分に当てはまる」というものがあるでしょうか。なぜ、この言い訳が通用しないかわかるでしょうか。

  - エラー処理のコードを入れると、コードの流れが追いにくくなる。正常系の制御の流れが追いにくく、コードを読むのが難しくなってしまう。
  - 納期が迫っているのに、余分な仕事を増やすわけにはいかない。
  - エラーが戻ることが絶対にない関数を使う場合はエラー処理のコードは要らないのではないか（たとえば、`printf` は必ず正しく出力をするし、`malloc` も必ず正しくメモリを確保する。そうでなければ、エラー処理のコードくらいでは解決できない大きな問題を抱えていることになる……。そういう理屈をこねる）。
  - 遊びで書いただけのプログラムで、製品にするわけではないから、そこまで高い質は必要ない。
