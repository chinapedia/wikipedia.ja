> この記事は[Morris worm](https://ja.wikipedia.org/wiki/Morris_worm)から翻訳されています。


**Morris worm**（モリスワーム）とは、[インターネット](../Page/インターネット.md "wikilink")上で拡散した初期の[ワームの](../Page/ワーム_\(コンピュータ\).md "wikilink")1つ。単に**インターネットワーム**と呼ばれることもある。

数千台の[マシン](https://ja.wikipedia.org/wiki/マシン "wikilink")を[サービス](../Page/サービス.md "wikilink")不能に追い込み、[報道](../Page/報道.md "wikilink")によって注目された世界初のワームと見なされている。当時、[コーネル大学](../Page/コーネル大学.md "wikilink")の学生であった[ロバート・T・モリス](https://ja.wikipedia.org/wiki/ロバート・T・モリス "wikilink")によって作られ、[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")（MIT）から[1988年](../Page/1988年.md "wikilink")[11月2日](../Page/11月2日.md "wikilink")に放たれた。MITから放たれたのは、コーネル大学が起源であることを隠すためであった。ちなみにロバート・T・モリスは現在 MIT の[准教授](../Page/准教授.md "wikilink")である。

## アーキテクチャ

作成者によれば、モリスワームは損害を与える意図で書かれたのではなく、インターネットの大きさを測る目的で書かれたとされている。しかし、意図していなかった[コードの性質から危険性が増すこととなった](../Page/プログラム_\(コンピュータ\).md "wikilink")。それは、1つのコンピュータに複数回に渡って侵入し、それぞれの侵入で起動された[プロセス](../Page/プロセス.md "wikilink")がマシンに[負荷](https://ja.wikipedia.org/wiki/負荷 "wikilink")を与え、利用不可能な状態にしてしまったことである。モリスワームは[UNIX](../Page/UNIX.md "wikilink")の[sendmail](https://ja.wikipedia.org/wiki/sendmail "wikilink")、[Fingerプロトコル](../Page/Fingerプロトコル.md "wikilink")、rsh/rexecなどの既知の[脆弱性](../Page/脆弱性.md "wikilink")や、推測しやすい[パスワード](../Page/パスワード.md "wikilink")などを利用して動作する。ワーム本体が侵入できるのは、[BSD](../Page/BSD.md "wikilink") 4.x の動作する[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[VAX](../Page/VAX.md "wikilink")と[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の [Sun-3](../Page/Sun-3.md "wikilink") だけであった。[C言語](../Page/C言語.md "wikilink")で書かれた移植性の高い "grappling hook" と呼ばれる[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")がワーム本体をそのマシンに侵入させるために使われ、grappling hook 自体は VAX と Sun 3 以外でも動作したため、ワーム本体を[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")する操作が行われ、[ネットワークや](../Page/コンピュータネットワーク.md "wikilink")[ディスクを圧迫した](../Page/補助記憶装置.md "wikilink")。

## 誤算

拡散機構に致命的な誤りがあったため、害のない知的[実験](../Page/実験.md "wikilink")のつもりが、悪意に満ちた[DoS攻撃](../Page/DoS攻撃.md "wikilink")のようなものに変貌してしまった。モリスワームは新たなコンピュータを見つけたとき、そこに既に自分の[コピー](../Page/コピー.md "wikilink")が動作しているかを問い合わせて侵入するかどうかを決めるようになっていた。しかし単純にこれを行うと、侵入されないようにするのは容易である。ワームの問合せに対して "yes" と答えるプロセスを走らせておけばよい。そうすれば、ワームはそのマシンには侵入しない。これに対する対策は、[マイケル・ラビン](../Page/マイケル・ラビン.md "wikilink")のモットーである "Randomization" からヒントを得たもので、そのような可能性に対処するため、モリスは応答が "yes" だった場合でも7回のうち一回はワーム本体をコピーするようにした\[1\]。この仕様は異常な増殖率を生み出してしまった。一部のコンピュータには複数回の[感染](../Page/感染.md "wikilink")が見られ、ワームは急速に広がっていった。ラビンはこの誤算を耳にしたとき、「最初に[シミュレータでそれを試すべきだった](../Page/シミュレーション.md "wikilink")」と指摘した。

## 影響

約6,000台のUNIXマシンがモリスワームに侵入されたと言われている。[ポール・グレアム](../Page/ポール・グレアム.md "wikilink")はこれについて次のように主張している\[2\]。

  -
    私はこの統計量がでっち上げられた場にいた。誰かがインターネットには約6万台のコンピュータが接続されていると言い、このワームはそのうち10%に侵入しただろうということになった。

[アメリカ政府説明責任局](https://ja.wikipedia.org/wiki/アメリカ政府説明責任局 "wikilink")（GAO）は損害額を1000万ドルから1億ドルと見積もった。

Gene Spafford は、この緊急事態の連絡用として [Phage mailing list](http://securitydigest.org/phage/) を作成した。

ロバート・T・モリスは、1986年に成立したばかりの[コンピュータ詐欺および不正使用取締法](https://ja.wikipedia.org/wiki/コンピュータ詐欺および不正使用取締法 "wikilink")で初めて告発された人物となった。[有罪](https://ja.wikipedia.org/wiki/有罪 "wikilink")を宣告された（3年間の[保護観察](../Page/保護観察.md "wikilink")、400時間の[労働奉仕](https://ja.wikipedia.org/wiki/労働奉仕 "wikilink")、10,050ドルの[罰金](../Page/罰金.md "wikilink")）。

モリスワームは、当時のインターネットに与えた損害（ダウンタイム）の大きさとインターネットの[セキュリティ](https://ja.wikipedia.org/wiki/セキュリティ "wikilink")問題を明らかにしたという点で "Great Worm" と呼ばれることもある。"Great Worm" の由来は、[J・R・R・トールキン](https://ja.wikipedia.org/wiki/J・R・R・トールキン "wikilink")の作品に登場するドラゴン Scatha と Glaurung である\[3\]。

この事件後、[CERT/CC](https://ja.wikipedia.org/wiki/CERT/CC "wikilink")をはじめとする[CSIRT](../Page/CSIRT.md "wikilink")が各国に生まれ、インターネットセキュリティの研究が活発化するきっかけとなった。

モリスはこれ以降の一時期、名前がネットに出ることを避けたため、Yahooによる買収直前のViawebのスナップショットではJohn McArtyemという名前が載っている。その後あまり気にかけなくなり、今は普通に名前を出している\[4\]。

## 関連項目

  - [バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")
  - [CERT/CC](https://ja.wikipedia.org/wiki/CERT_Coordination_Center "wikilink")
  - 『[カッコウはコンピュータに卵を産む](https://ja.wikipedia.org/wiki/カッコウはコンピュータに卵を産む "wikilink")』（[クリフォード・ストール](https://ja.wikipedia.org/wiki/クリフォード・ストール "wikilink")） - 最後の章で本件に触れている。

## 出典・脚注

## 外部リンク

  - [Archive of worm material, incl. papers and code](http://ftp.cerias.purdue.edu/pub/doc/morris_worm/)
  - [An analysis of the worm by Eugene Spafford](http://homes.cerias.purdue.edu/~spaf/tech-reps/823.pdf)
  - [An analysis of the worm by Mark Eichin and Jon Rochlis](http://citeseer.ist.psu.edu/eichin89with.html)
  - ["The Morris Internet Worm" by Charles Schmidt and Tom Darby](http://www.snowplow.org/tom/worm/worm.html)
  - RFC 1135 - "Helminthiasis of the Internet" - ワームに関する分析
  - ["A Tour of the Worm"](http://world.std.com/~franl/worm.html), Don Seeley, Department of Computer Science, University of Utah (as posted by Francis Litterio)
  - [The Morris Worm](http://www.morrisworm.com)
  - [A Report On The Internet Worm, by Bob Page, University of Lowell](http://www.ee.ryerson.ca/~elf/hack/iworm.html)

[Category:マルウェア](https://ja.wikipedia.org/wiki/Category:マルウェア "wikilink") [Category:コンピュータ・ワーム](https://ja.wikipedia.org/wiki/Category:コンピュータ・ワーム "wikilink")

1.  [Court Appeal of Morris](http://www.morrisworm.com/morris_appeal.txt)
2.  <http://www.paulgraham.com/submarine.html#f4n>
3.  [Great Worm](http://www.catb.org/~esr/jargon/html/G/Great-Worm.html) from The [Jargon File](../Page/ジャーゴンファイル.md "wikilink")
4.  ポール・グレアムのアーティクル <http://www.aoky.net/articles/paul_graham/vw.htm> より