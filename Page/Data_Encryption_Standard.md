> この記事は[Data Encryption Standard](https://ja.wikipedia.org/wiki/Data_Encryption_Standard)から翻訳されています。


（データ暗号化標準）、略して**DES**（）は、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の旧国家暗号規格、もしくはその[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")で規格化されている[共通鍵暗号](../Page/共通鍵暗号.md "wikilink")である。[ブロック暗号](../Page/ブロック暗号.md "wikilink")の一種であり、1976年[国立標準局](../Page/アメリカ国立標準技術研究所.md "wikilink") (NBS) が[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の公式[連邦情報処理標準](https://ja.wikipedia.org/wiki/Federal_Information_Processing_Standards "wikilink") (FIPS) として採用し、その後国際的に広く使われた。56[ビット](../Page/ビット.md "wikilink")の鍵を使った[共通鍵暗号](../Page/共通鍵暗号.md "wikilink")を基盤としている。その[アルゴリズム](../Page/アルゴリズム.md "wikilink")は、機密設計要素、比較的短い鍵長、[アメリカ国家安全保障局](../Page/アメリカ国家安全保障局.md "wikilink") (NSA) が[バックドア](../Page/バックドア.md "wikilink")を設けたのではないかという疑いなどで、当初物議をかもしていた。結果としてDESは、現代の[ブロック暗号](../Page/ブロック暗号.md "wikilink")とその[暗号解読](../Page/暗号解読.md "wikilink")の理解に基づいて学究的に徹底した精査を受けた。

DESは今では多くの用途において[安全](../Page/安全.md "wikilink")ではないと見なされている。これは主に56ビットという鍵長が短すぎることに起因する。1999年1月、[distributed.net](https://ja.wikipedia.org/wiki/distributed.net "wikilink")と[電子フロンティア財団](../Page/電子フロンティア財団.md "wikilink")は共同で、22時間15分でDESの鍵を破ったことを公表した。この[暗号](../Page/暗号.md "wikilink")の理論上の弱さを示した解析結果もあるが、そのような弱さを実際に利用することが可能というわけではない。アルゴリズム自体は実用上安全であるとされ、[トリプルDES](../Page/トリプルDES.md "wikilink")という形で使われているが、[理論的攻撃方法は存在する](../Page/暗号理論.md "wikilink")。近年、 (AES)に取って代わられた。

なお、標準としてのDESとアルゴリズムを区別することがあり、アルゴリズムを  (**DEA**)と称することがある。

## DESが制定されるまでの経緯

DESの起源は[1970年代](../Page/1970年代.md "wikilink")初めに遡る。1972年、アメリカ政府は[コンピュータセキュリティ](../Page/コンピュータセキュリティ.md "wikilink")が重要であるという研究結果を得た。そこでNBS（National Bureau of Standard。合衆国標準局。現在の[NIST（アメリカ国立標準技術研究所）](../Page/アメリカ国立標準技術研究所.md "wikilink")）が、政府全体で機密情報を暗号化するための標準規格が必要だと判断した\[1\]。それに応じて1973年5月15日、[NSAと相談の上](../Page/アメリカ国家安全保障局.md "wikilink")、NBSが厳しい[設計](../Page/設計.md "wikilink")基準を満たした暗号を公募した。しかし応募のいずれも条件を満たしていなかったため、1974年8月27日に2回目の公募を行った。今回は[IBM](../Page/IBM.md "wikilink")の応募した案が条件を満たしていると思われた。それは、以前からあったアルゴリズムに基づき1973年から1974年に開発された[ホルスト・ファイステル](https://ja.wikipedia.org/wiki/ホルスト・ファイステル "wikilink")の[Lucifer暗号だった](https://ja.wikipedia.org/wiki/Lucifer_\(暗号\) "wikilink")。IBMでこの暗号の設計と解析を行ったチームにはファイステルの他に、ウォルト・タックマン (Walt Tuchman)、ドン・コッパースミス (Don Coppersmith)、アラン・コンハイム (Alan Konheim)、カール・メイヤー (Carl Meyer)、マイク・マーチャーシュ (Mike Matyas)、ロイ・アドラー (Roy Adler)、エドナ・グロスマン (Edna Grossman)、ビル・ノッツ (Bill Notz)、リン・スミス (Lynn Smith)、ブライアント・タッカーマン (Bryant Tuckerman) らがいた。

Lucifer・DESはホルスト・ファイステルらの考えた[Feistel構造](../Page/Feistel構造.md "wikilink")と呼ばれる構造をなしている。この事は後の共通鍵暗号研究に多大な影響を与え、後に提案された多くの共通鍵暗号方式がFeistel構造に基づいて設計された。

### NSAの設計への関与

1975年3月17日、規格案としてのDESが *[Federal Register](https://ja.wikipedia.org/wiki/連邦官報 "wikilink")* に発表された。そしてコメントが募集され、翌年には2回ワークショップを開催してこの規格案について議論した。各所から様々な批判が寄せられた。中には[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")の先駆者である[マーティン・ヘルマン](https://ja.wikipedia.org/wiki/マーティン・ヘルマン "wikilink")と[ホイットフィールド・ディフィー](../Page/ホイットフィールド・ディフィー.md "wikilink")の批判があり、鍵長が短いという点と謎めいた「[Sボックス](../Page/Sボックス.md "wikilink")」がNSAによる不適切な干渉を意味しているのではないかと指摘した。それは、このアルゴリズムを諜報機関が密かに弱め、その諜報機関だけが暗号化されたメッセージを容易に解読できるようにしたのではないかという疑いが持たれたのである\[2\]。アラン・コンハイム（DES設計者の1人）はそれについて「我々はSボックスをワシントンに送った。戻ってきたものは送ったものとは全く異なっていた」と述べた\[3\]。アメリカ合衆国上院諜報特別委員会がNSAの行為に不適切な干渉があったかどうかを調査した。調査結果の公開された要約には次のように書かれている。

  -
    「DESの開発において、NSAは[IBM](../Page/IBM.md "wikilink")に対して鍵長が短くても大丈夫だと納得させ、Sボックスの開発を間接的に支援し、最終的なDESアルゴリズムが統計学的にも数学的にも考えられる最高のものだと保証した」\[4\]

しかし、同時に次のようなことも判明している。

  -
    「NSAはいかなる形でもアルゴリズムの設計を改変していない。[IBM](../Page/IBM.md "wikilink")はこのアルゴリズムを発明・設計し、関連する設計上の意思決定は全てIBMが行い、鍵長もDESのあらゆる商用の用途にとって十分な長さとして決定した」\[5\]

DES設計チームのウォルト・タックマンは「我々はIBM内でIBMの人員だけでDESアルゴリズム全体を開発した。NSAに命じられて変更した部分は1つもない」と述べた\[6\]。一方、機密解除されたNSAの暗号史に関する本には次のように書かれている。

  -
    「1973年、NBSはDESを民間企業に求めた。最初の応募案は満足のいくものではなかったため、NSAは独自にアルゴリズムの研究を始めた。そして、工学研究部門の代表であるハワード・ローゼンブラムは、IBMのウォルト・タックマンがLuciferを汎用化する修正を行っていることに気づいた。NSAはタックマンに人物証明を与え、当局と共にLuciferを修正する作業を行わせた」\[7\]

Sボックスに関する嫌疑の一部は1990年に鎮められることになった。同年、[エリ・ビハム](https://ja.wikipedia.org/wiki/エリ・ビハム "wikilink")と[アディ・シャミア](../Page/アディ・シャミア.md "wikilink")（[RSAのS](../Page/RSA暗号.md "wikilink")）が[差分解読法](../Page/差分解読法.md "wikilink")を独自に発見して公表した。差分解読法はブロック暗号を破る汎用技法である。DESのSボックスは無作為に選ばれた場合よりもこの攻撃法にずっと抵抗力があり、IBMが1970年代にこの攻撃法を知っていたことを強く示唆していた。1994年、ドン・コッパースミスがSボックスの元々の設計基準について一部を公表したことで、それが裏付けられた\[8\]。[スティーブン・レビー](https://ja.wikipedia.org/wiki/スティーブン・レビー "wikilink")によれば、IBMでは1974年に差分解読法を発見していたが、NSAがそれを秘密にするよう要請していたという\[9\]。コッパースミスはIBMの方針について「（差分解読法）は非常に強力なツールであり、様々な方式に応用でき、これを公にすると国家の安全に悪い影響を及ぼすことが懸念された」と述べている。レビーはタックマンの言葉として「彼らは我々のあらゆる文書に極秘というスタンプを押させようとした…それらは合衆国政府の機密と見なされたので、我々は実際にそれらに番号を振り、金庫に入れた。彼らがそうしろと言ったから、そうしたまでだ」と書いている\[10\]。

### 標準暗号としてのDES

批判はあったがDESは1976年11月[連邦規格](https://ja.wikipedia.org/wiki/連邦規格 "wikilink")として承認され、1977年1月15日には **[FIPS](https://ja.wikipedia.org/wiki/Federal_Information_Processing_Standards "wikilink") PUB 46** として公表され、非機密政府通信での利用が承認された。さらに1981年に [ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")として制定され、民間標準規格にもなった。1983年、1988年（**FIPS-46-1** に更新）、1993年 (**FIPS-46-2**)、1999年 (**FIPS-46-3**) と再承認され、最後には[トリプルDES](../Page/トリプルDES.md "wikilink")が定められた。2002年5月26日、DESは公開のコンペティションで選ばれた [Advanced Encryption Standard](../Page/Advanced_Encryption_Standard.md "wikilink") (AES) で置き換えられた。2005年5月19日、FIPS 46-3は公式に廃止となったが、[NISTは](../Page/アメリカ国立標準技術研究所.md "wikilink")[トリプルDES](../Page/トリプルDES.md "wikilink")については政府の重要情報用に使うことを2030年まで承認している\[11\]。

このアルゴリズムは ANSI X3.92\[12\]、NIST SP 800-67\[13\]、ISO/IEC 18033-3\[14\] でも指定されている（[TDEAの要素として](../Page/トリプルDES.md "wikilink")）。

もう1つの理論的攻撃法である線形解読法は1994年に公表された。1998年には[総当り攻撃](https://ja.wikipedia.org/wiki/総当り攻撃 "wikilink")で実用的な時間でDESを破れることが実証され、アルゴリズムの更新の必要性が高まった。これら攻撃法については後の節で詳述する。

DESの登場は暗号研究、特に暗号解読法の研究を活発化させる触媒の役割を果たした。NISTは後にDESについて次のように述べている。

  -
    DESは暗号アルゴリズムの非軍事的研究と開発を「ジャンプスタート」させたと言える。1970年代、[暗号学者](https://ja.wikipedia.org/wiki/暗号学者 "wikilink")は[軍隊](../Page/軍隊.md "wikilink")や[諜報機関](https://ja.wikipedia.org/wiki/諜報機関 "wikilink")以外にはほとんどおらず、暗号の学問的研究は限定的だった。今では多数の学者が暗号を研究し、数学関係の学科で暗号を教え、情報セキュリティ企業やコンサルタントが商売をしている。暗号解読者はDESアルゴリズムを解析することで経験を積んだ。暗号研究者[ブルース・シュナイアー](https://ja.wikipedia.org/wiki/ブルース・シュナイアー "wikilink")は「DESは暗号解読というフィールドを大いに活気付けた。今では研究すべきアルゴリズムのひとつだ」と述べている\[15\]。1970年代から1980年代にかけて、暗号に関する多くの書籍がDESを扱っており、公開鍵暗号を比較する際の基準となっている\[16\]。

### 年表

<table>
<thead>
<tr class="header">
<th><p>日付</p></th>
<th><p>出来事</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>nowrap|1973年5月15日</p></td>
<td><p>NBSが標準暗号アルゴリズムの要求仕様を公開（1回目）。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1974年8月27日</p></td>
<td><p>NBSが標準暗号アルゴリズムの要求仕様を公開（2回目）。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1975年3月17日</p></td>
<td><p>コメントを求めるため、DESが  で公表された。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1976年8月</p></td>
<td><p>DESに関する最初のワークショップ開催。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1976年9月</p></td>
<td><p>2回目のワークショップ。DESの数学的基盤について議論。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1976年11月</p></td>
<td><p>DESを標準として承認。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1977年1月15日</p></td>
<td><p>DESを  46 として公表。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1983年</p></td>
<td><p>DESについて、1回目の再承認を実施。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1986年</p></td>
<td><p><a href="../Page/HBO.md" title="wikilink">HBO</a>がDESをベースとした衛星テレビ放送のスクランブリングシステム  を実用化。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1988年1月22日</p></td>
<td><p>DES について2回目の再承認を行い、 46 を置き換える  46-1 を制定。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1990年7月</p></td>
<td><p>ビハムとシャミアが<a href="../Page/差分解読法.md" title="wikilink">差分解読法</a>を再発見し、DESに似た15ラウンドの暗号に適用。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1992年</p></td>
<td><p>ビハムとシャミアが総当り攻撃よりも計算量が少ない理論上の攻撃法（<a href="../Page/差分解読法.md" title="wikilink">差分解読法</a>）があることを発表。ただし、必要とする選択平文数は非現実的な2<sup>47</sup>だった。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1993年12月30日</p></td>
<td><p>DES について3回目の承認を行い、 46-2 とした。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1994年</p></td>
<td><p><a href="../Page/線形解読法.md" title="wikilink">線形解読法</a>を用いた<a href="https://ja.wikipedia.org/wiki/暗号解読#解読法の分類" title="wikilink">既知平文攻撃によって</a>、DESの解読が初めて実際に行われた (<a href="https://ja.wikipedia.org/wiki/松井充" title="wikilink">松井充</a>)。平文と暗号文の組数は、2<sup>43</sup>だった。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1997年6月</p></td>
<td><p>によりDESで暗号化されたメッセージの解読が行われ、初めて一般に公表。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1998年7月</p></td>
<td><p><a href="../Page/電子フロンティア財団.md" title="wikilink">電子フロンティア財団</a>のが56時間でDESの鍵を破った。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|1999年1月</p></td>
<td><p>と  が共同で22時間15分でDESの鍵を破った。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|1999年10月25日</p></td>
<td><p>DESについて4回目の承認を行い FIPS 46-3としたが、<a href="../Page/トリプルDES.md" title="wikilink">トリプルDES</a>の使用を推奨し、シングルDESは古いシステムでのみ使用することとした。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|2001年11月26日</p></td>
<td><p><a href="../Page/Advanced_Encryption_Standard.md" title="wikilink">{{langを</a>  197として公表。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|2002年5月26日</p></td>
<td><p>AES規格が発効。</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|2004年7月26日</p></td>
<td><p>46-3（および関連する規格群）の廃止が  で提案された[17]。</p></td>
</tr>
<tr class="even">
<td><p>nowrap|2005年5月19日</p></td>
<td><p>NISTがFIPS 46-3を廃止[18]</p></td>
</tr>
<tr class="odd">
<td><p>nowrap|2006年4月</p></td>
<td><p><a href="../Page/ルール大学ボーフム.md" title="wikilink">ルール大学ボーフム</a>と<a href="https://ja.wikipedia.org/wiki/キール大学_(ドイツ)" title="wikilink">キール大学で</a><a href="../Page/FPGA.md" title="wikilink">FPGA</a>を使った並列マシンを開発し、1万ドルのハードウェアコストで9日間をかけてDESを破った[19]。 その後1年以内にソフトウェアを改良し、平均で6.4日で破れるようになった。</p></td>
</tr>
</tbody>
</table>

## 詳細

[thumb](https://ja.wikipedia.org/wiki/ファイル:DES-main-network.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:DES-f-function.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:DES-key-schedule.png "wikilink") DESは原型ともいうべき[ブロック暗号](../Page/ブロック暗号.md "wikilink")であり、固定ビット長の[平文](../Page/平文.md "wikilink")を入力とし、一連の複雑な操作によって同じ長さの[暗号文](../Page/暗号文.md "wikilink")を出力する[アルゴリズム](../Page/アルゴリズム.md "wikilink")である。DESの場合、ブロック長は64ビットである。また、変換をカスタマイズする[鍵を使うため](../Page/鍵_\(暗号\).md "wikilink")、暗号化に使った鍵を知っている者だけが復号できる。鍵は見た目は64ビットだが、そのうち8ビットは[パリティチェックに使うため](../Page/パリティビット.md "wikilink")、アルゴリズム上の実際の鍵の長さは56ビットである。

他のブロック暗号と同様、DES自体は暗号化の安全な手段ではなく、[暗号利用モード](../Page/暗号利用モード.md "wikilink")で使う必要がある。FIPS-81 はDES用のいくつかのモードを示している\[20\]。その他のDESの利用法については FIPS-74 に詳しい\[21\]。

### 全体構造

アルゴリズムの全体構造を図1に示す。16の処理工程があり、それらを「ラウンド」と呼ぶ。また、最初と最後に[並べ替え処理があり](../Page/順列.md "wikilink")、それぞれ *IP* および *FP* と呼ぶ。*IP* と *FP* はちょうど逆の処理を行う。*IP* と *FP* は暗号化にはほとんど関係ないが、1970年代の[ハードウェア](../Page/ハードウェア.md "wikilink")でブロックの入出力を行う部分として含まれており、同時にそれによって[ソフトウェア](../Page/ソフトウェア.md "wikilink")によるDESの処理が遅くなる原因にもなっている。

ラウンドでの処理の前にブロックは半分（32ビット）ずつに分けられ、それぞれ異なる処理を施される。この十字交差構造を[Feistel構造](../Page/Feistel構造.md "wikilink")と呼ぶ。Feistel構造を使うと、暗号化と復号は非常に良く似た処理になる。違いは、復号ではラウンド鍵を逆の順序で適用するという点だけであり、アルゴリズムは同一である。このため実装が単純化でき、特にハードウェアで実装する場合に両者を別々に実装する必要が無い。

⊕ という記号は[排他的論理和](../Page/排他的論理和.md "wikilink") (XOR) を意味する。*F-関数*はブロックの半分を何からの鍵でかき混ぜる。F-関数の出力をブロックの残り半分と結合し、次のラウンドに行く前にその半分同士を入れ替える。最後のラウンドの後は入れ替えを行わない。これは、暗号化と復号を似たプロセスで行うFeistel構造の特徴である。

### Feistel(F)関数

図2にあるF-関数はブロックの半分（32ビット）を一度に動作する。以下の4段階がある。

1.  *Expansion* - *expansion permutation* と呼ばれる方式で32ビットを48ビットに拡張する。図では *E* で示されている部分である。入力のうち半分のビットの複製をビット列に加える。出力は6ビットの部分が8個あり、そのうち真ん中の4ビットは入力の対応する4ビットの部分と同じで、両端のビットは入力上で隣接する部分のビットの複製である。
2.  *Key mixing* - ラウンド鍵と上の出力結果をXOR操作で結合する。ラウンド鍵は48ビットで、もともとの鍵から「鍵スケジュール」（後述）によって16個のラウンド鍵が生成される。
3.  *Substitution* - ラウンド鍵を混ぜた後、6ビットずつに分けて[Sボックス](../Page/Sボックス.md "wikilink") (substitution box) に入力する。8個のSボックスは入力の6ビットから4ビットの出力を生成し、このとき[ルックアップテーブル](../Page/ルックアップテーブル.md "wikilink")の形で提供される非線形な変換を行う。SボックスがDESの安全性の根幹であり、これがないと暗号は線形なものとなって容易に破ることができることになる。
4.  *Permutation* - Sボックス群の出力である32ビットに固定の[並べ替えを施す](../Page/順列.md "wikilink")。図では *P* で示した部分である。このとき、各Sボックスの出力が次のラウンドでSボックスに展開されるとき、6個の異なるSボックスに分散するよう並べ替える。

Sボックスでの置換とPボックスでの並べ替えとEでの拡張を交互に行うことで、[クロード・シャノン](../Page/クロード・シャノン.md "wikilink")が安全で実用的な暗号に必要な条件とした「[拡散とかく乱](https://ja.wikipedia.org/wiki/拡散とかく乱 "wikilink")」を提供する。

### 鍵スケジュール

図3は暗号化での「鍵スケジュール」、すなわちラウンド鍵を生成するアルゴリズムを示している。まず64ビットの入力から56ビットを選択して並べ替えを行う *Permuted Choice 1* (*PC-1*) がある。選ばれなかった8ビットは単に捨ててもよいし、[パリティビット](../Page/パリティビット.md "wikilink")として鍵のチェックに使ってもよい。その56ビットは2つの28ビットに分割され、その後別々に処理される。ラウンドを次に進める際にそれぞれを左に1ビットか2ビット[ローテートする](https://ja.wikipedia.org/wiki/ビット演算#\(キャリーなし\)ローテート "wikilink")（ラウンドによってローテートするビット数が異なる）。そして、それらを *Permuted Choice 2* (*PC-2*) に入力して48ビットのラウンド鍵を出力する。このときそれぞれの半分（28ビット）から24ビットずつを選び、並べ替えも左右別々に行う。ローテートを行うことでラウンドごとに選択するビットが変化する（PC-2自体は固定であり、毎回同じ位置のビットを選んで同じ順序で並べ替える）。各ビットは16ラウンドのうち、だいたい14回使われる。

復号の際の鍵スケジュールもほぼ同様である。ラウンド鍵は暗号化のときとは逆順に適用される。その点を除けば暗号化と全く同じ工程で処理される。

## DESに代わるアルゴリズム

DESについては安全性と[ソフトウェア](../Page/ソフトウェア.md "wikilink")処理が相対的に遅い点が懸念され、[1980年代](../Page/1980年代.md "wikilink")末から[1990年代](../Page/1990年代.md "wikilink")初めごろから研究者らが様々な[ブロック暗号](../Page/ブロック暗号.md "wikilink")を代替案として提案してきた。例えば、[RC5](../Page/RC5.md "wikilink")、[Blowfish](../Page/Blowfish.md "wikilink")、[IDEA](https://ja.wikipedia.org/wiki/International_Data_Encryption_Algorithm "wikilink")、[NewDES](https://ja.wikipedia.org/wiki/NewDES "wikilink")、[SAFER](https://ja.wikipedia.org/wiki/SAFER "wikilink")、[CAST5](../Page/CAST-128.md "wikilink")、[FEAL](../Page/FEAL.md "wikilink")などがある。その多くはDESと同じ64ビットのブロック長で、そのまま代替として使えるようになっているが、鍵には64ビットか128ビットを使っているものが多い。[ソビエト連邦](https://ja.wikipedia.org/wiki/ソビエト連邦 "wikilink")では[GOSTアルゴリズムが導入された](https://ja.wikipedia.org/wiki/GOST_\(ブロック暗号\) "wikilink")。これはブロック長64ビットで256ビットの鍵を使っており、後に[ロシア](../Page/ロシア.md "wikilink")でも使われた。

DES自身をもっと安全な形にして再利用することもできる。かつてDESを使っていたところでは、DESの特許権保持者の1人が考案した[トリプルDES](../Page/トリプルDES.md "wikilink") (TDES) を使っている（[FIPS](https://ja.wikipedia.org/wiki/Federal_Information_Processing_Standards "wikilink") Pub 46-3 参照）。この方式では2つ (2TDES) ないし3つ (3TDES) の鍵を用いて、暗号‐復号‐暗号の順でDESを3回行なう事で暗号化する。TDESは十分安全だが、極めて時間がかかる。それほど計算量が増えない代替方式として[DES-X](https://ja.wikipedia.org/wiki/DES-X "wikilink")があり、鍵長を長くしてDESの処理の前後で外部鍵をXORする。[GDES](https://ja.wikipedia.org/wiki/GDES "wikilink")はDESの暗号処理を高速にする方式だが、差分解読法に弱いことが分かっている。

その後NISTがDESに代わる米国標準暗号方式 Advanced Encryption Standard (AES) を公募した。そして2000年10月、ベルギーのと[フィンセント・ライメン](https://ja.wikipedia.org/wiki/フィンセント・ライメン "wikilink")により提案されたRijndael（ラインデール）が新しい米国標準暗号方式[AESに選ばれた](../Page/Advanced_Encryption_Standard.md "wikilink")。[トリプルDES](../Page/トリプルDES.md "wikilink")のような[ad-hocな方法で設計された暗号方式とは異なり](../Page/アドホック.md "wikilink")、AESは[SPN構造](https://ja.wikipedia.org/wiki/SPN構造 "wikilink")と呼ばれるより整備された構造を持つ暗号方式である。公募には他に[RC6](../Page/RC6.md "wikilink")、[Serpent](https://ja.wikipedia.org/wiki/Serpent_\(暗号\) "wikilink")、[MARS](https://ja.wikipedia.org/wiki/MARS_\(暗号\) "wikilink")、[Twofish](../Page/Twofish.md "wikilink")も応募したが選ばれなかった。AESは2001年11月に FIPS 197 として正式に公表された。

## セキュリティと解読

DESの解読法については他のブロック暗号よりも多数の情報があるが、今も最も実用的な攻撃法は総当り攻撃である。暗号解読上の各種特性が知られており、3種類の理論上の攻撃方法が知られている。それらは総当り攻撃よりも理論上は計算量が少ないが、非現実的な量の既知平文か選択平文を必要とし、実用化はされていない。

### 総当り攻撃

[thumbが](https://ja.wikipedia.org/wiki/ファイル:Board300.jpg "wikilink")25万ドルで製作したDES解読機。1,856のカスタムチップで構成され、DESの鍵を総当りで数日間で破ることができる。写真は Deap Crack チップをいくつか装備したDES解読機用回路基板。\]\]

どんな暗号についても、最も基本となる攻撃法は[総当り攻撃](https://ja.wikipedia.org/wiki/総当り攻撃 "wikilink")、すなわち鍵のとりうる値を全て試す方法である。鍵の長さが鍵のとりうる値の個数に直接関係してくるため、総当りが現実的かどうかも鍵の長さで決まる。DESについては標準として採用される以前から鍵の短さが懸念されていた。NSAを含む外部コンサルタントを交えた議論の結果、1つのチップで暗号化できるよう鍵の長さを128ビットから56ビットに減らすことになった\[22\]。

学界では様々なDES解読機が提案されてきた。1977年、ディフィーとヘルマンは1日でDESの鍵を見つけることができるマシンのコストを2000万ドルと見積もった。1993年になると、ウィーナーは7時間で鍵を見つけることができる機械のコストを100万ドルと見積もった。しかし、そのような初期の提案に基づいて実際に解読機を製作した例はないし、少なくともそのような実例が公表されたことはなかった。DESの脆弱性が実際に示されたのは1990年代後半のことである。1997年、[RSAセキュリティ](../Page/RSAセキュリティ.md "wikilink")は一連のコンテストを主催し、DESで暗号化されたメッセージを最初に解読したチームに1万ドルを賞金として提示した。このコンテストで優勝したのは、Rocke Verser、Matt Curtin、Justin Dolske が主導する [DESCHALL Project](https://ja.wikipedia.org/wiki/:en:DESCHALL_Project "wikilink") で、インターネット上の数千台のコンピュータのアイドル時間（何もしていない時間）を利用したプロジェクトだった。1998年には[電子フロンティア財団](../Page/電子フロンティア財団.md "wikilink") (EFF) が約25万ドルをかけてDES解読機を製作した。EFFの意図は、DESを理論上だけでなく実際に破ることができるということを示すことであり、「多くの人々は実際に自分の目で見るまで真実を信じようとしない。DESを数日間で破ることができるマシンを実際に示すことで、DESによるセキュリティが信用できないことを明らかにできる」と述べている。この機械は2日強かけて総当り攻撃で鍵を見つけることができる。1999年1月に行われた3回目のコンテストでは、22時間で[distributed.net](https://ja.wikipedia.org/wiki/distributed.net "wikilink")によりDESが解読された\[23\]。この解読にはEFFのDES解読機とインターネット経由で募集された10万台の計算機が用いられた。

もう1つのDES解読機として[COPACOBANA](http://www.copacobana.org/)（cost-optimized parallel code breaker の略）が2006年、[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")の[ルール大学ボーフム](../Page/ルール大学ボーフム.md "wikilink")と[キール大学のチームで開発された](https://ja.wikipedia.org/wiki/キール大学_\(ドイツ\) "wikilink")。EFFの解読機とは異なり、COPACOBANAは一般に入手可能な部品（集積回路）のみを使っている。20個のDIMMモジュールで構成され、それぞれに6個の[FPGA](../Page/FPGA.md "wikilink")（[XILINX](../Page/ザイリンクス.md "wikilink") Spartan3-1000）を装備し、それらが並列に動作する。FPGAを使っているため、DES以外の暗号解読にも応用可能である。COPACOBANAはその低コストが重要な特徴で、1台を約1万ドルで製作できる。EFFのDES解読機に比べると約25分の1であり、8年間の物価上昇を考慮すると約30分の1ということができる。

### 総当り攻撃よりも高速な攻撃法

総当り攻撃よりも少ない計算量で16ラウンドのDESを破ることができる攻撃法が3種類知られている。[差分解読法](../Page/差分解読法.md "wikilink") (DC)、[線形解読法](../Page/線形解読法.md "wikilink") (LC)、[Davies' attack](https://ja.wikipedia.org/wiki/:en:Davies'_attack "wikilink") である。しかし、これらの攻撃法は理論上のものであって、実際に応用するのは現実的ではない。これらを certificational weaknesses と呼ぶこともある。

  - 差分解読法
    [1980年代](../Page/1980年代.md "wikilink")末に[エリ・ビハム](https://ja.wikipedia.org/wiki/エリ・ビハム "wikilink")と[アディ・シャミア](../Page/アディ・シャミア.md "wikilink")が再発見した。IBMとNSAには以前から知られていたが、秘密にされていた。16ラウンドのDESを破るには、2<sup>47</sup>の選択平文を必要とする。DESはDCへの耐性を考慮して設計されている。
  - 線形解読法
    1993年、[松井充](https://ja.wikipedia.org/wiki/松井充 "wikilink")が発見。2<sup>43</sup>の既知平文を必要とする。これを実際に実装して(Matsui, 1994)、DESの解読実験が行われている。DESがこの解読法への耐性を考慮して設計されたという証拠はない。1994年には、これを拡張した *multiple linear cryptanalysis* (Kaliski and Robshaw) が提案され、その後も改良が Biryukov らによって行われている。研究によると、複数の線形近似を用いることで必要なデータ量が4分の1になる（つまり、2<sup>43</sup>を2<sup>41</sup>に減らせる）ことが示唆されている。また、選択平文を使った線形解読法でも同様にデータ量を削減できる (Knudsen and Mathiassen, 2000)。Junod (2001) は実験によって線形解読法の時間計算量を測定し、DESの解読は予想よりも時間がかからず 2<sup>39</sup> から 2<sup>41</sup> になるとした。
  - Davies' attack
    差分解読法も線形解読法もDESに限らず任意の暗号解読に使えるが、Davies' attack はDES専用の解読法で、[ドナルド・デービスが](https://ja.wikipedia.org/wiki/ドナルド・ワッツ・デービス "wikilink")1980年代に提案し、ビハムと[Biryukov](https://ja.wikipedia.org/wiki/:en:Alex_Biryukov "wikilink") (1997) が改良を施した。最も強力な形式の攻撃には 2<sup>50</sup> の既知平文を必要とし、計算量も 2<sup>50</sup>、成功率は51%である。

ラウンド数を減らした暗号（DESの16ラウンドを減らしたもの）への攻撃法も提案されている。そのような研究によってラウンド数がどれだけあれば安全かという考察も行われている。また、16ラウンドのDESにどれだけ安全マージンがあるかも研究されてきた。1994年にはラングフォードとヘルマンが差分解読法と線形解読法を組み合わせた[差分線形解読法](https://ja.wikipedia.org/wiki/差分線形解読法 "wikilink")を提案した。改良版の解読法では、9ラウンドのDESを 2<sup>15.8</sup> の既知平文を使って 2<sup>29.2</sup> の時間計算量で破ることができる (Biham et al., 2002)。

### その他の暗号解読上の特性

DESには相補性がある。すなわち次が成り立つ。

  -
    *E<sub>k</sub>(P) = C ⇔ E<sub><span style="text-decoration:overline">K</span></sub>(<span style="text-decoration:overline">P</span>) = <span style="text-decoration:overline">C</span>*

ここで \(\overline{x}\) は \(x\) のビット毎の反転である。\(E_K\) は鍵 \(K\) を使った暗号化を意味する。\(P\) は平文、\(C\) は暗号ブロック列である。相補性があるということは、[総当り攻撃](https://ja.wikipedia.org/wiki/総当り攻撃 "wikilink")に必要な試行回数は2分の1で済むことを意味する。

DESには4つのいわゆる「弱い鍵」がある。暗号化 (*E*) と復号 (*D*) で弱い鍵を使うと、どちらも同じ効果がある。

\[E_K(E_K(P))=P\] または \(E_K=D_K\) また、6組の「やや弱い鍵」もある。弱い鍵の1つ \(K_1\) を使った暗号化は、ペアのもう一方の \(K_2\) を使った復号と等価である。

\[E_{K_1}(E_{K_2}(P))=P\] または \(E_{K_2}=D_{K_1}\) 弱い鍵ややや弱い鍵を実装で使わないようにするのは容易である。もともと無作為に鍵を選んでも、それらを選ぶ確率は極めて低い。それらの鍵は理論上は他の鍵より弱いわけではなく、攻撃に際しても特に利用できるわけでもない。

DESは[群にならないことが証明されている](https://ja.wikipedia.org/wiki/群_\(数学\) "wikilink")。つまり、集合 \(\{E_K\}\)（鍵 \(K\) がとりうる全ての値の集合）は[関数合成](https://ja.wikipedia.org/wiki/関数合成 "wikilink")において群ではないし、1つの群に閉じていない (Campbell and Wiener, 1992)。これがもし群であるならば、DESは容易に破ることができ、トリプルDESにしても安全性は向上しなかったとされている。

DESの暗号学的安全性は最大でも約64ビットである。例えば、個々のラウンド鍵を元の1つの鍵から生成せずそれぞれ独立に供給すれば、安全性は768ビットになりそうなものだが、この限界によりそうならないことが知られている。

## 関連項目

  - [暗号理論](../Page/暗号理論.md "wikilink")
  - [スキップジャック (暗号)](../Page/スキップジャック_\(暗号\).md "wikilink")
  - [共通鍵暗号](../Page/共通鍵暗号.md "wikilink")

## 脚注・出典

## 参考文献

  - ([preprint](http://nfotemple.free.fr/site_cryptokg/site_roy/differential%20cryptanalysis%20of%20des-like%20cryptosystems.pdf))

  - Biham, Eli and Adi Shamir, Differential Cryptanalysis of the Data Encryption Standard, Springer Verlag, 1993. ISBN 0-387-97930-1, ISBN 3-540-97930-1.

  - Biham, Eli and Alex Biryukov:An Improvement of Davies' Attack on DES. J. Cryptology 10(3):195–206 (1997)

  - Biham, Eli, Orr Dunkelman, Nathan Keller:Enhancing Differential-Linear Cryptanalysis. ASIACRYPT 2002:pp254–266

  - Biham, Eli. A Fast New DES Implementation in Software [Cracking DES:Secrets of Encryption Research, Wiretap Politics, and Chip Design](http://cryptome.org/jya/cracking-des/cracking-des.htm), [Electronic Frontier Foundation](../Page/電子フロンティア財団.md "wikilink")

  - ([preprint](http://www.esat.kuleuven.ac.be/~abiryuko/mla.pdf)).

  - Campbell, Keith W., Michael J. Wiener:DES is not a Group. CRYPTO 1992:pp512–520

  - Coppersmith, Don. (1994). [The data encryption standard (DES) and its strength against attacks](https://web.archive.org/web/20070316233309/http://www.research.ibm.com/journal/rd/383/coppersmith.pdf). *IBM Journal of Research and Development*, **38**(3), 243–250.

  - [Diffie, Whitfield](../Page/ホイットフィールド・ディフィー.md "wikilink") and [Martin Hellman](https://ja.wikipedia.org/wiki/マーティン・ヘルマン "wikilink"), "Exhaustive Cryptanalysis of the NBS Data Encryption Standard" IEEE Computer 10(6), June 1977, pp74–84

  - Ehrsam et al., Product Block Cipher System for Data Security, , Filed February 24, 1975

  - [Gilmore, John](../Page/ジョン・ギルモア.md "wikilink"), "Cracking DES:Secrets of Encryption Research, Wiretap Politics and Chip Design", 1998, O'Reilly, ISBN 1-56592-520-3.

  - Junod, Pascal.  Selected Areas in Cryptography, 2001, pp199–211.

  - Kaliski, Burton S., Matt Robshaw:Linear Cryptanalysis Using Multiple Approximations. CRYPTO 1994:pp26–39

  - Knudsen, Lars, John Erik Mathiassen:A Chosen-Plaintext Linear Attack on DES. Fast Software Encryption - FSE 2000:pp262–272

  - Langford, Susan K., Martin E. Hellman:Differential-Linear Cryptanalysis. CRYPTO 1994:17–25

  - Levy, Steven, Crypto:How the Code Rebels Beat the Government—Saving Privacy in the Digital Age, 2001, ISBN 0-14-024432-8.

  -
  -
  - National Bureau of Standards, Data Encryption Standard, FIPS-Pub.46. National Bureau of Standards, U.S. Department of Commerce, Washington D.C., January 1977.

## 外部リンク

  - [FIPS 46-3:DES標準についての公式文書](https://csrc.nist.gov/csrc/media/publications/fips/46/3/archive/1999-10-25/documents/fips46-3.pdf) (PDF);[やや古いHTML版](http://www.itl.nist.gov/fipspubs/fip46-2.htm)
  - [COPACOBANA](https://www.copacobana.org/) 1万ドルでDESを破るマシン。ルール大学ボーフムとキール大学がFPGAを使って製作。
  - [RFC4772 :Security Implications of Using the Data Encryption Standard (DES)](https://tools.ietf.org/html/rfc4772)

[Category:アメリカ国家安全保障局](https://ja.wikipedia.org/wiki/Category:アメリカ国家安全保障局 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  Levy, *Crypto*, p. 55
10.
11.
12. [American National Standards Institute](https://ja.wikipedia.org/wiki/ANSI "wikilink"), ANSI X3.92-1981 *American National Standard, Data Encryption Algorithm*
13.
14.
15. Bruce Schneier, Applied Cryptography, Protocols, Algorithms, and Source Code in C, Second edition, John Wiley and Sons, New York (1996) p. 267
16. William E. Burr, "Data Encryption Standard", in NIST's anthology "A Century of Excellence in Measurements, Standards, and Technology:A Chronicle of Selected NBS/NIST Publications, 1901–2000. [HTML](http://nvl.nist.gov/pub/nistpubs/sp958-lide/html/250-253.html) [PDF](http://nvl.nist.gov/pub/nistpubs/sp958-lide/250-253.pdf)
17.
18.
19. S. Kumar, C. Paar, J. Pelzl, G. Pfeiffer, A. Rupp, M. Schimmler, "How to Break DES for Euro 8,980". 2nd Workshop on Special-purpose Hardware for Attacking Cryptographic Systems — SHARCS 2006, Cologne, Germany, April 3-4, 2006.
20.
21.
22. Stallings, W. *Cryptography and network security:principles and practice*. Prentice Hall, 2006. p. 73
23.