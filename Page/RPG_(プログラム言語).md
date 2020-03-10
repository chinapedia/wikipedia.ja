> この記事は[RPG \(\)](https://ja.wikipedia.org/wiki/RPG_\(\))から翻訳されています。


**RPG** は、[ビジネスソフトウェア](https://ja.wikipedia.org/wiki/ビジネスソフトウェア "wikilink")向けの[高水準言語](../Page/高水準言語.md "wikilink")に位置づけられる[プログラム言語](https://ja.wikipedia.org/wiki/プログラム言語 "wikilink")である。[IBM](../Page/IBM.md "wikilink")独自の言語であり、[IBM-iまたは](https://ja.wikipedia.org/wiki/IBM_i "wikilink")[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")のシステム上で動作する。

RPGというプログラム名は**Report Program Generator**の[アクロニム](https://ja.wikipedia.org/wiki/アクロニム "wikilink")である。[ILE](https://ja.wikipedia.org/wiki/ILE "wikilink") (Integrated Language Environment) の[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")機能を取り入れた RPG IVが現行である（ILE RPGとしても知られている）。最初期の[4GL](https://ja.wikipedia.org/wiki/4GL "wikilink")（第四世代言語）とされる。

IBMによって[1959年](../Page/1959年.md "wikilink")に開発された言語であり、高水準言語としては[FORTRAN](../Page/FORTRAN.md "wikilink")、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、[ALGOL](../Page/ALGOL.md "wikilink")58に次いで古い歴史を持つ。

## 概観

[IBM](../Page/IBM.md "wikilink") [System i](https://ja.wikipedia.org/wiki/System_i "wikilink")（以前のAS/400）の主力[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。元はクエリー用ツールとして設計されたものだが、IBMが力を入れたことで、一人前の強力な言語になった。

典型的なRPGプログラムは File Specification から始まる。ここでは[入出力](../Page/入出力.md "wikilink")用[ファイルを全て列挙する](../Page/ファイル_\(コンピュータ\).md "wikilink")。続いて Data Definition Specification である。これは[データ構造](../Page/データ構造.md "wikilink")や[配列](../Page/配列.md "wikilink")を定義する部分で、[COBOL](../Page/COBOL.md "wikilink")の Working-Storage セクションや[Pascal](../Page/Pascal.md "wikilink")の変数定義(var)セクションに大変よく似ている。次はプログラムの動作をコードする Calculation Specification である。出力する[レポート](https://ja.wikipedia.org/wiki/レポート "wikilink")のレイアウトを決定する Output Specification を加えてもいいし、外部でそれを決定してもいい。

初期のRPGの売り物は**program cycle**であった。これは、[レコード](../Page/レコード.md "wikilink")をファイルから読み込む毎にいくつかのRPGプログラムが一つの暗黙の[ループの中で実行されるというものであり](../Page/ループ_\(プログラミング\).md "wikilink")、別の見方をすれば、暗黙のうちに相互作用する一つのプログラムが作り上げられるということになる。現在では、[プログラムフローを通常のループで制御しようとする](../Page/プログラム_\(コンピュータ\).md "wikilink")[プログラマ](../Page/プログラマ.md "wikilink")が多いため、この機能は避けられる傾向にある。

## 歴史

RPGは[パンチカード](https://ja.wikipedia.org/wiki/パンチカード "wikilink")時代から現代まで常用され続けてきた数少ない言語の一つである。[IBM](../Page/IBM.md "wikilink")がRPGを開発したのは1960年代のことであった。RPGは *Report Program Generator* の[アクロニム](https://ja.wikipedia.org/wiki/アクロニム "wikilink")で、この名前が目的を表している: データ[ファイルを読み](../Page/ファイル_\(コンピュータ\).md "wikilink")、小計や検算を含んだ会計報告を生成する。

RPGの前身は[FARGO](https://ja.wikipedia.org/wiki/FARGO "wikilink") (Fourteen-o-one Automatic Report Generation Operation) である。FARGOとRPGはユニットレコード装置（以下PCS、[タビュレーティングマシン](https://ja.wikipedia.org/wiki/タビュレーティングマシン "wikilink")参照）から当時新開発だった[IBM 1401シリーズへの移行を容易ならしめることを目的としていた](https://ja.wikipedia.org/wiki/IBM_1401 "wikilink")。PCS技術者は、[プラグボード](https://ja.wikipedia.org/wiki/プラグボード "wikilink")[:en:plug-board](https://ja.wikipedia.org/wiki/:en:plug-board "wikilink")上で配線することで入出力やカウンタ操作（四則演算）を行うことに慣れていた。PCSのプログラムは1マシンサイクル中にいくつかのパルスを発生することで実行されていたので、FARGOとRPGは*program cycle*の名でこれを[エミュレート](https://ja.wikipedia.org/wiki/エミュレート "wikilink")したのである。RPGはFARGOより優れており、会計報告作成言語としてのFARGOを駆逐した。

当時、他に広く用いられていた言語に[COBOL](../Page/COBOL.md "wikilink")と[FORTRAN](../Page/FORTRAN.md "wikilink")があった。COBOLは饒舌な（訳注: 自然言語に近づけるため、ソースコードの記述量が多くなった — 省略しても構わない部分も多いが）ビジネス向け言語で、FORTRANは科学計算向けであった。この時代の他の言語としては、[PL/1](https://ja.wikipedia.org/wiki/PL/I "wikilink")、[ALGOL](../Page/ALGOL.md "wikilink")、[Autocoder](https://ja.wikipedia.org/wiki/Autocoder "wikilink")がある。COBOLは[メインフレーム](../Page/メインフレーム.md "wikilink")/汎用機のビジネス応用ではより一般的であり、RPGはPCSから移行した店舗でより一般的だった（[System/360モデル20](https://ja.wikipedia.org/wiki/System/360モデル20 "wikilink")）。

**RPG II**は[System/3](https://ja.wikipedia.org/wiki/System/3 "wikilink")と同時に導入され、後には[System/32](https://ja.wikipedia.org/wiki/System/32 "wikilink")、[System/34](https://ja.wikipedia.org/wiki/System/34 "wikilink")、[System/36](https://ja.wikipedia.org/wiki/System/36 "wikilink")上でも利用されたが、[System/38](https://ja.wikipedia.org/wiki/System/38 "wikilink")向けには改良版の**RPG III**が作られた。同機の後継機[AS/400](https://ja.wikipedia.org/wiki/AS/400 "wikilink")（ミッドレンジ機で、現在では[System iに進化した](https://ja.wikipedia.org/wiki/System_i "wikilink")）の登場に伴い、文法を洗練し、統合[データベース](../Page/データベース.md "wikilink")といっそう緊密に統合された **RPG/400** が作られた。RPG/400はAS/400上の主力開発言語となり、それぞれの specification （命令の種類）に応じたプロンプトが出るラインエディタが用いられた。

RPG IIIは元のRPGから格段に変化しており、[IF-ENDIFブロック](../Page/If文.md "wikilink")、DO[ループ](../Page/ループ_\(プログラミング\).md "wikilink")、[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")といった近代的な構造を持っている。

1994年に、RPG IV（あるいはRPGLE、RPG/ILE）がリリースされ、もはやRPGはReport Program Generatorのアクロニムではないことが公式に告げられた。RPG IVは新しい Extended Factor-2 Calculation Specification をサポートし、さらに広範な表現を可能としている。

2001年、[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink") V5R1 のリリースと共にRPG IVは Extended Factor-2 Calculation Specification すら超える自由を得た: 従来のコラム依存のコーディングの代わりに自由書式のソースコードを受け入れるようになったのである。"/FREE"計算を用いるとこれまでのように特定のコラムに命令コードを書く必要がなくなり、EVAL及びCALLP命令の命令コードがオプションになり、一般に行われる汎用言語によく似た構文になった。

今日、RPG IVはより堅固な言語になっている。昔と同様単純なエディタでプログラムを編集してもいいし、IBMのWebsphere Development Studioを通してPCで編集してもいい。IBMはRPGの機能拡張を続けており、内蔵された機能 (BIF) も増加している。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のオブジェクトとのリンク可能性、OS/400の[APIのコールなどである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。IBMの[Cgidev2](https://ja.wikipedia.org/wiki/Cgidev2 "wikilink")ツールキットやRPG xTools [1](http://www.rpgxtools.com/) CGILIB 他の商用パッケージを用いれば、[CGIを書くこともできる](../Page/Common_Gateway_Interface.md "wikilink")。これらの改良の一方ではこれまでとの互換性も考慮されており、35年前に書かれたRPGプログラムが現在でもほとんど修正なしで実行可能である。

## データ型

RPGは以下の[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")を使用することができる。

<table>
<thead>
<tr class="header">
<th><p>データ型</p></th>
<th><p>名称</p></th>
<th><p>長さ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>A</code></p></td>
<td><p>英数字</p></td>
<td><p>1 ～ 16,773,104 バイト (固定)<br />
1 ～ 16,773,100 バイト(可変長)</p></td>
<td><p>英数字</p></td>
</tr>
<tr class="even">
<td><p><code>B</code></p></td>
<td><p>バイナリ数値</p></td>
<td><p>1 バイト (8ビット)<br />
2 バイト (16ビット)<br />
4 バイト (32ビット)<br />
8 バイト (64ビット)</p></td>
<td><p>符号付き2進整数</p></td>
</tr>
<tr class="odd">
<td><p><code>C</code></p></td>
<td><p>UCS-2（文字）</p></td>
<td><p>1 ～ 8,386,552 文字 (固定)<br />
1～8,386,550 文字 (可変)</p></td>
<td><p>16ビット UCS-2(<a href="https://ja.wikipedia.org/wiki/DBCS" title="wikilink">DBCS</a>・EGCS)</p></td>
</tr>
<tr class="even">
<td><p><code>D</code></p></td>
<td><p>日付</p></td>
<td><p>10 バイト</p></td>
<td><p>日付: 年, 月, 日</p></td>
</tr>
<tr class="odd">
<td><p><code>F</code></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/浮動小数点" title="wikilink">浮動小数点</a></p></td>
<td><p>4 バイト (32ビット)<br />
8 バイト (64ビット)</p></td>
<td><p>符号付きバイナリ浮動小数点実数</p></td>
</tr>
<tr class="even">
<td><p><code>G</code></p></td>
<td><p>Graphic character</p></td>
<td><p>1～8,386,552 文字 (固定)<br />
1～8,386,550 文字 (可変)</p></td>
<td><p>16ビット graphic character (<a href="https://ja.wikipedia.org/wiki/DBCS" title="wikilink">DBCS</a>・EGCS)</p></td>
</tr>
<tr class="odd">
<td><p><code>I</code></p></td>
<td><p>整数値</p></td>
<td><p>1 バイト (8ビット)<br />
2 バイト (16ビット)<br />
4 バイト (32ビット)<br />
8 バイト (64ビット)</p></td>
<td><p>符号付き2進整数</p></td>
</tr>
<tr class="even">
<td><p><code>N</code></p></td>
<td><p><a href="../Page/ブーリアン型.md" title="wikilink">ブーリアン型</a></p></td>
<td><p>1 バイト</p></td>
<td><p>'1' = TRUE<br />
'0' = FALSE</p></td>
</tr>
<tr class="odd">
<td><p><code>O</code></p></td>
<td><p>オブジェクト</p></td>
<td><p>不定</p></td>
<td><p>オブジェクト（参照）</p></td>
</tr>
<tr class="even">
<td><p><code>P</code></p></td>
<td><p><a href="../Page/二進化十進表現.md" title="wikilink">パック10進数</a></p></td>
<td><p>1～63 桁,<br />
2 桁/バイト ＋ 符号</p></td>
<td><p>整数と小数点付きの固定小数点10進数の符号付き</p></td>
</tr>
<tr class="odd">
<td><p><code>S</code></p></td>
<td><p><a href="../Page/二進化十進表現.md" title="wikilink">ゾーン10進数</a></p></td>
<td><p>1～63 桁,<br />
1 桁/バイト</p></td>
<td><p>整数と小数点付きの固定小数点10進数の符号付き</p></td>
</tr>
<tr class="even">
<td><p><code>T</code></p></td>
<td><p>時刻</p></td>
<td><p>8 バイト</p></td>
<td><p>時刻: 時, 分, 秒</p></td>
</tr>
<tr class="odd">
<td><p><code>U</code></p></td>
<td><p>整数値</p></td>
<td><p>1 バイト (8ビット)<br />
2 バイト (16ビット)<br />
4 バイト (32ビット)<br />
8 バイト (64ビット)</p></td>
<td><p>符号なし2進整数</p></td>
</tr>
<tr class="even">
<td><p><code>Z</code></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/タイムスタンプ" title="wikilink">タイムスタンプ</a></p></td>
<td><p>26 バイト</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/システム時刻" title="wikilink">日時</a>:<br />
  年, 月, 日, 時, 分, 秒, マイクロ秒</p></td>
</tr>
<tr class="odd">
<td><p><code>*</code></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ポインタ" title="wikilink">ポインタ</a></p></td>
<td><p>16 バイト</p></td>
<td><p>データ・標識・オブジェクトへのアクセス</p></td>
</tr>
</tbody>
</table>

## コードの例

次の[プログラムは入力として顧客番号を受け取って名前と住所を出力する](../Page/プログラム_\(コンピュータ\).md "wikilink")。 [コメントの訳は次の通り](../Page/コメント_\(コンピュータ\).md "wikilink")。

1.  「自由書式が許される環境もあるが、歴史的にRPGはコラムに従って記述する。第7コラムの星印(\*)はコメント行を意味する。行の目的は第6コラムの文字で決まる。」
2.  「'F'は[ファイルその他の](../Page/ファイル_\(コンピュータ\).md "wikilink")[入出力](../Page/入出力.md "wikilink")装置の仕様を示す。」
3.  「'D'は変数定義である。」
4.  「'C'は実行すべき文を示す。パラメタは plist 及び parm 命令で定義される。」
5.  「'chain' コマンドは（検索用）キーのあるファイルのランダムアクセスを行う。」
6.  「RPGはスイッチを利用する。その一つ'LR'＜最終レコード＞の意味で、プログラムの実行を停止する。」

### RPG3

```
      F* F仕様書はI/Oファイルなどを定義する
      FARMSTF1UF  E                    DISK
      F            ARMST                             KRENAMERARMST
      C* パラメータの定義
      C          *ENTRY    PLIST
      C                    PARM           PCUSNO  60
      C                    PARM           PNAME  30
      C                    PARM           PADDR1 30
      C                    PARM           PADDR2 30
      C                    PARM           PCITY  25
      C                    PARM           PSTATE  2
      C                    PARM           PZIP   10
      C*
      C* "CHAIN"命令を使用してキーファイルをランダムアクセスする
      C* ファイルに存在しないときは、標識90がオンになる。
      C          PCUSNO    CHAINARMSTF1              90
      C*
      C* レコードが存在する場合はその値をパラメータにセットする
      C          *IN90     IFEQ *OFF
      C                    Z-ADDARNM01    PNAME
      C                    MOVELARAD01    PADDR1
      C                    MOVELARAD02    PADDR2
      C                    MOVELARCY01    PCITY
      C                    MOVELARST01    PSTATE
      C                    MOVELARZP15    PZIP
      C                    ENDIF
      C* RPGのプログラム終了時には標識LRをオンにする。
      C                    MOVE '1'       *INLR
```

### RPG4（ILE）

```

      * Historically RPG is columnar in nature, though free-formatting
      * is allowed under particular circumstances.
      * The purpose of various lines code are determined by a
      * letter code in column 6.
      * An asterisk (*) in column 7 denotes a comment line

      * "F" (file) specs define files and other i/o devices
     FARMstF1   UF   E             Disk    Rename(ARMST:RARMST)

      * "D" specs are used to define variables
     D pCusNo          S              6p 0
     D pName           S             30a
     D pAddr1          S             30a
     D pAddr2          S             30a
     D pCity           S             25a
     D pState          S              2a
     D pZip            S             10a

      * "C" (calculation) specs are used for executable statements
      * Parameters are defined using plist and parm opcodes
     C     *entry        plist
     C                   parm                    pCusNo
     C                   parm                    pName
     C                   parm                    pAddr1
     C                   parm                    pAddr2
     C                   parm                    pCity
     C                   parm                    pState
     C                   parm                    pZip

      * The "chain" command is used for random access of a keyed file
     C     pCusNo        chain     ARMstF1

      * If a record is found, move fields from the file into parameters
     C                   if        %found
     C                   eval      pName  = ARNm01
     C                   eval      pAddr1 = ARAd01
     C                   eval      pAddr2 = ARAd02
     C                   eval      pCity  = ARCy01
     C                   eval      pState = ARSt01
     C                   eval      pZip   = ARZp15
     C                   endif

      * RPG makes use of switches.  One switch "LR" stands for
      * "last record".  This ends program execution.
     C                   eval      *InLR = *On

```

### RPG4（フリーフォーマット）

```
      * "F" (file) specs define files and other i/o devices
     FARMstF1   UF   E             Disk    Rename(ARMST:RARMST)

      * "D" specs are used to define variables and parameters
      * The "prototype" for the program is in a separate file
      * allowing other programs to call it
      /copy cust_pr
      * The "procedure interface" describes the *ENTRY parameters
     D getCustInf      PI
     D  pCusNo                        6p 0   const
     D  pName                        30a
     D  pAddr1                       30a
     D  pAddr2                       30a
     D  pCity                        25a
     D  pState                        2a
     D  pZip                         10a
      /free
        // The "chain" command is used for random access of a keyed file
        chain pCusNo ARMstF1;

        // If a record is found, move fields from the file into parameters
        if %found;
           pName  = ARNm01;
           pAddr1 = ARAd01;
           pAddr2 = ARAd02;
           pCity  = ARCy01;
           pState = ARSt01;
           pZip   = ARZp15;
        endif;

        // RPG makes use of switches.  One switch "LR" stands for
        // "last record".  This ends program execution.
        *InLR = *On;
      /end-free
```

## プラットホーム

前述のように、RPGはもともと[IBM](../Page/IBM.md "wikilink")によって 1401, [System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink"), /3, /32, /34, /36, /38, AS/400, 及び [System i](https://ja.wikipedia.org/wiki/System_i "wikilink") システム用に導入された。だが、IBMの計算機の他にも、[Digital](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") [VAX](https://ja.wikipedia.org/wiki/VAX "wikilink"), Sperry Univac BC/7, Univac system 80, Siemens BS2000, Burroughs B1700, Hewlett Packard HP3000, ICL 2900 series, 及び WANG VS に移植され、[UNIX](../Page/UNIX.md "wikilink")ベースのシステム (Unibol) 及び PC (Baby/400, Lattice-RPG) にも[コンパイラ](../Page/コンパイラ.md "wikilink")が存在した。RPG IIは今でもサードパーティ製のコンパイラがあり（[Migration RPG](http://www.migrationspecialties.com/Migration-RPG.html) 参照）、[HP](../Page/ヒューレット・パッカード.md "wikilink") [OpenVMS](https://ja.wikipedia.org/wiki/OpenVMS "wikilink") operating system on [VAX](https://ja.wikipedia.org/wiki/VAX "wikilink"), [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink"), 及びIntegrity processorをサポートしている。

## 関連項目

  - [プログラミング言語年表](https://ja.wikipedia.org/wiki/プログラミング言語年表 "wikilink")
  - [RPG](https://ja.wikipedia.org/wiki/RPG "wikilink")（曖昧さ回避ページ）

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink")