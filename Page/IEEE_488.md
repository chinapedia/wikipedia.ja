> この記事は[IEEE 488](https://ja.wikipedia.org/wiki/IEEE_488)から翻訳されています。


**IEEE 488**とは、短距離デジタル通信[バス仕様である](../Page/バス_\(コンピュータ\).md "wikilink")。元々は自動テスト設備に用いられることを目的として作られたが、現在でもその分野では広い範囲で使われている。IEEE 488はまたHP-IB (Hewlett-Packard Instrument Bus) やGPIB (General Purpose Interface Bus) としてよく知られている。

## 設計

IEEE 488は、[デイジーチェーン](https://ja.wikipedia.org/wiki/デイジーチェーン "wikilink")接続により、1つの8bitパラレル電気バスを15個までのデバイスで共有できるものである。最も低速のデバイスが制御に参加するので、データ転送速度を決定するためにデータを[ハンドシェイク](https://ja.wikipedia.org/wiki/ハンドシェイク "wikilink")して送る。最初の標準では最大データ速度は約1MByte/sであったが、IEEE 488.1-2003 (HS-488) では8MByte/secになっている。

IEEE 488バスは16本の信号線を使っていて、8本を双方向データ通信用に、3本をハンドシェイクに、そして5本をバス管理に用いている。さらに8本をグランドとしている。

## 歴史

[1960年代](../Page/1960年代.md "wikilink")後半、[Hewlett-Packard (HP)](../Page/ヒューレット・パッカード.md "wikilink") は、[デジタルマルチメーターやロジックアナライザのような試験および測定装置メーカーであった](../Page/回路計.md "wikilink")。HPはコンピュータのような試験装置や制御装置をより簡単に相互接続できるようにするために、HP Interface Bus (HP-IB) を開発した。このバスはその当時の技術を用いて比較的簡単に実装できた。このバスは単純なパラレルの電気バスといくつかの独立した制御線を用いていた。

他のメーカーはHP-IBをコピーして、General Purpose Interface Bus (GPIB) を作った。

[1975年](../Page/1975年.md "wikilink")、このバスは[IEEE](../Page/IEEE.md "wikilink")によって **IEEE Standard Digital Interface for Programmable Instrumentation, IEEE 488**-1975（今は 488.1になっている）として標準化された。IEEE 488.1は、GPIBのメカニカル仕様、電気仕様、基本的なプロトコルなどのパラメータは形式化したが、コマンドやデータのフォーマットについては何も触れなかった。**IEEE 488.2** 標準、つまり **Codes, Formats, Protocols, and Common Commands for IEEE 488.1**（[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")6月）では、基本的な文法とフォーマット規約を提供し、同様にデバイス独立コマンドやデータ構造、エラープロトコルなども定めた。IEEE 488.1の上に立っているIEEE 488.2はIEEE 488.1に取り込まれていない。各種装置は488.2に従わなくても488.1の仕様を満足することができる。

IEEE 488.1がハードウェアを定義しIEEE 488.2が文法を定義したが、そこには装置固有のコマンドの標準はなかった。同じ装置のクラス（例えばマルチメーター）を制御するコマンドは、メーカー同士、また種々のモデル間でさえ様々であった。デバイスコマンドの標準であるSCPIは[1990年代](../Page/1990年代.md "wikilink")に導入された。ただ導入が遅かったため、広く実装されることはなかった。

National Instrumentsは、元々**HS-488**として知られたIEEE 488.1の上位互換規格を導入した。これはデータ速度を最大8MByte/secにまで増やした。ただ、バスにより多くのデバイスを接続するとこの速度は減少した。この規格は[2003年](../Page/2003年.md "wikilink")に標準として加えられ、IEEE 488.1-2003になった。

IEEEに加えて、他のいくつかの[標準化団体はHP](../Page/標準化団体_\(コンピュータと通信\).md "wikilink")-IBを採用していた。[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")（米国規格協会）での相当する規格はANSI Standard MC 1.1。[IEC（国際電気標準会議）ではIEEEからの提案を受け](../Page/国際電気標準会議.md "wikilink")、IEEE/IEC 60488-1-2004 Ed.1 \[1\]として国際規格になっている。

## 適用分野

最初、HP-IBの設計者らはIEEE 488を汎用コンピュータの標準周辺機器インタフェースとして特別に計画したのではなかった。[1977年](../Page/1977年.md "wikilink")までには、教育・家庭・個人用コンピュータである[Commodore PET/CBMが](../Page/PET_2001.md "wikilink")、IEEE 488バスを使ってディスクドライブやプリンタ、[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")などを接続した。CommodoreのPET/CBM後継の8bitマシンは、[VIC-20からC](../Page/VIC-1001.md "wikilink")128まで周辺機器用に独自の「シリアルのIEEE 488」を利用していた。これは大きくて重いHP-IBのプラグや（PETコンピュータ用の）マザーボードに指すカード型コネクタの代わりに、丸い[DINコネクタ](../Page/DINコネクタ.md "wikilink")を用いていた。

Hewlett-PackardとTektronixもまたIEEE 488をディスクドライブや[テープドライブ](../Page/テープドライブ.md "wikilink")、プリンタ、プロッタなどを接続する周辺機器用インタフェースとして使用していた。これらは彼らのワークステーション製品や、HPのミニコンピュータである[HP3000](https://ja.wikipedia.org/wiki/HP3000 "wikilink")に利用していた。このような用途のために10MBytes/sまでバス速度を増やしたが、コマンドプロトコルの標準がないために、サードパーティからの製品供給は少なく、互換性も限られていた。最終的には、周辺機器アクセスには、[SCSIのようなより速くオープンな規格が使われるようになった](../Page/Small_Computer_System_Interface.md "wikilink")。

加えて、HPの1980年代の高機能[電卓](../Page/電卓.md "wikilink")・[ポケットコンピュータ](../Page/ポケットコンピュータ.md "wikilink")のいくつか、例えば[HP-41](https://ja.wikipedia.org/wiki/HP-41 "wikilink")やHP-71のようなものはオプションであるHP-IBインタフェースを通して様々な計測を行うことができた。インタフェースはオプションである[HP-IL](https://ja.wikipedia.org/wiki/HP-IL "wikilink")モジュールを通して計算機に接続した。

## 信号

データ・ハンドシェーク・管理用のすべての信号は、0 がHighレベル (≧2.0V)、1がLowレベル(≦0.8V)となる。

<table>
<thead>
<tr class="header">
<th><p>種類</p></th>
<th><p>方向</p></th>
<th><p>名称</p></th>
<th><p>データ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>データ</p></td>
<td><p>トーカ <strong>→</strong> リスナ</p></td>
<td><p><strong>DIO1–DIO8</strong></p></td>
<td><p>8bit データ</p></td>
<td><p>データ入出力ビット。これら8本の線はバスを通して送られる8bitのデータやコマンドバイトを読み書きするのに使われる。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/ハンドシェーク" title="wikilink">ハンドシェーク</a></p></td>
<td><p>トーカ <strong>→</strong> リスナ</p></td>
<td><p><strong>DAV</strong><br />
(Data Valid)</p></td>
<td><p>1(L) = データ有効<br />
0(H) = データ無効</p></td>
<td><p>データが正当である。これはハンドシェイクラインであって、DIO1-DIO8で送られた値が正当であることを示す信号として使われる。転送用データがDIO1-DIO8のラインにセットされている間、DAVラインは「T1時間」と呼ばれる時間の後にアサートされる。T1時間後、データが読まれる前にデータラインは安定な値になる。</p></td>
</tr>
<tr class="odd">
<td><p>トーカ <strong>←</strong> リスナ</p></td>
<td><p><strong>NRFD</strong><br />
(Not Ready For Data)</p></td>
<td><p>1(L) = ビジー<br />
0(H) = レディ</p></td>
<td><p>データの準備ができていない。NRFDは受信側によって新しいデータバイトを受信する準備ができていないことを知らせるためにアサートされる、ハンドシェイク用ラインである。</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>NDAC</strong><br />
(Not Data Accepted)</p></td>
<td><p>1(L) = 未受信<br />
0(H) = 受信完了</p></td>
<td><p>データ未受信。NDACは受信側がDIOラインに乗っているデータをまだ読んでいないことを示すために、受信側によってアサートされるハンドシェイクラインである。</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>管理用</p></td>
<td><p>コントローラ<br />
<strong>→</strong> デバイス</p></td>
<td><p><strong>ATN</strong><br />
(Attention)</p></td>
<td><p>1(L) = コマンド<br />
0(H) = データ転送</p></td>
<td><p>ATNは（1バイトのデータとは逆に）1バイトのコマンドバイトがDIOラインにあることを示すためにアサートされる。また、パラレルポール使用時はEOIもアサートされる。</p></td>
</tr>
<tr class="even">
<td><p><strong>EOI</strong><br />
(End-or-identify)</p></td>
<td><p>1(L) = 最終バイト</p></td>
<td><p>このラインは、データの最終バイトが書き込まれるとアサートされる。つまりメッセージの最後を示す。パラレルポールの時はATNと一緒にアサートされる。</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><strong>IFC</strong><br />
(Interface Clear)</p></td>
<td><p>1(L) = 初期化</p></td>
<td><p>インタフェース初期化。システムコントローラは、バスをリセットしコントローラ管理下におくためこのラインを（少なくとも100us以上）アサートする。</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>REN</strong><br />
(Remote Enable)</p></td>
<td><p>1(L) = リモートモード<br />
0(H) = ローカルモード</p></td>
<td><p>システムコントローラによってアサートされ、RENがデバイスをリモートモードに入れる。つまり、コントローラによってRENがアサートされると、デバイスはリモートモードに入る。RENが偽(H)であれば、すべてのデバイスは即座にローカルモードに戻る。</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>コントローラ<br />
<strong>←</strong> デバイス</p></td>
<td><p><strong>SRQ</strong><br />
(Service Request)</p></td>
<td><p>1(L) = サービス要求</p></td>
<td><p>バス上にあるデバイスは、コントローラ管理下からサービスを要求するためにアサートする。コントローラはデバイスがサービス要求するまで監視し、必要に応じてなんらかのアクションを起こす。</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 通信方法

### トーカとリスナの決定

コントローラは、データを送信するトーカを1つと、データを受信するリスナを1つ以上選択する。コントローラは ATN=L とし、 UNL (Unlisten) コマンドを発行後、トーカアドレスとリスナアドレスを送信し、 ATN を H に戻すと、トーカとリスナが決定することができる。

### データの送受信

トーカが 8bitデータをデータバスに設定後に DAV=L とすると、リスナは まず NRFD=H としてビジー状態とし、データ受信が完了すると NDAC=H とする。データ受信完了後にトーカが DAV=H とすると、リスナは NDAC=L とし、リスナが次のデータを受信できる状態になると NRFD を L に戻す。これにより1byteのデータ送受信が完了する。

複数byteのデータの送受信では、最終のデータであることを示す**デリミタ**をトーカからリスナに対して送信する必要がある。一般的には、バイナリデータの場合には EOI=L とし、文字列データの場合には CR+LF, CR, LF をデリミタとする場合が多い。

### サービスリクエスト

デバイスからコントローラに対して割り込みをかける場合、デバイスはSRQ信号を1(L)としてサービス要求を行う。その後、コントローラはどのデバイスから要求が来ているかを調べる必要があるが、調べる方法として、**パラレルポール**と**シリアルポール**の手法がある。

## コネクタ

### IEEE 488

[thumb](https://ja.wikipedia.org/wiki/ファイル:IEEE-488-Stecker2.jpg "wikilink") IEEE 488はが設計した24ピンのマイクロリボンコネクタを採用している（しばしば[セントロニクス](https://ja.wikipedia.org/wiki/セントロニクス "wikilink")タイプと誤って呼ばれている）。オス／メスのコネクタが対になっているので積み重ね（スタック）て簡単にデイジーチェインが可能である（これを[ピギーバック](../Page/ピギーバック.md "wikilink")コネクタとも言う）。スタック可能なコネクタの数の機械的な限界は4つ以下となっている。これらはUTS（いまやほとんど廃止されている）やメートル (M3.5 x 0.6) ねじによって固定される。慣例的によりメートルねじは黒く塗られ、UTSねじとは合わないようになっている。総ケーブル長は20mが限界になっているが、非標準の「バスエクステンダ」デバイスも使える。

#### ピン配列

[ファイル:IEEE 488 Connector.JPG](https://ja.wikipedia.org/wiki/ファイル:IEEE_488_Connector.JPG "wikilink")

### IEC-625

IEC-625標準では25pin D-subコネクタ（[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")のパラレルポートに使われているもの）の使用を規定している。この標準は24pinコネクタの採用に反して市場の多くの支持を得られなかった。

## 脚注

## 外部リンク

  - IEEE Standards
      - [IEEE 488.1: Standard Digital Interface for Programmable Instrumentation](http://standards.ieee.org/reading/ieee/std_public/description/im/488.1-1987_desc.html)
      - [IEEE 488.2: Standard Codes, Formats, Protocols, and Common Commands for Use With IEEE 488.1](http://standards.ieee.org/reading/ieee/std_public/description/im/488.2-1992_desc.html)
      - [Press release on IEEE 488.1-2003, which allows for higher speeds](http://standards.ieee.org/announcements/pr_4881upgrade.html)

<!-- end list -->

  - 解説ページ
      - [ＧＰＩＢインターフェースのハンドシェーク](http://www.nextftp.com/susumu_oiso/GPIB_IF.htm)
      - [GPIB(General Purpose Interface Bus: IEEE488)/HPIBとは](http://www.htbasic.jp/support/d_gpib.html)

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink") [Category:IEEE標準](https://ja.wikipedia.org/wiki/Category:IEEE標準 "wikilink")

1.  IEEE/IEC 60488-1-2004(IEEE Std 488.1-2003): Higher Performance Protocol for the Standard Digital Interface for Programmable Instrumentation - Part 1: General