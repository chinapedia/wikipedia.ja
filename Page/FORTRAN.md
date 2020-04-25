> この記事は[FORTRAN](https://ja.wikipedia.org/wiki/FORTRAN)から翻訳されています。


**FORTRAN**（**フォートラン**）は、[1954年](../Page/1954年.md "wikilink")に[IBM](../Page/IBM.md "wikilink")の[ジョン・バッカス](../Page/ジョン・バッカス.md "wikilink")によって考案された、[コンピュータ](../Page/コンピュータ.md "wikilink")において広く使われた世界最初の[高水準言語](../Page/高水準言語.md "wikilink")である。

## 概要

[1956年](../Page/1956年.md "wikilink")に最初のマニュアルが、[1957年](../Page/1957年.md "wikilink")に[IBM 704用の最初の](../Page/IBM_704.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")がリリースされた。名前「FORTRAN」は「」に由来し、FORTRAN 77やFortran 90などの末尾の数字は規格が制定された年を示している。

FORTRANは[科学技術計算に向いた](../Page/計算科学.md "wikilink")[手続き型プログラミング](../Page/手続き型プログラミング.md "wikilink")[言語であり](../Page/プログラミング言語.md "wikilink")、その長い歴史の間に開発された非常に多くの[数学関数](https://ja.wikipedia.org/wiki/数学関数 "wikilink")や[サブルーチン](../Page/サブルーチン.md "wikilink")を[数値解析ソフトウェア](https://ja.wikipedia.org/wiki/数値解析ソフトウェア "wikilink")の形で持っている。また、[並列計算](../Page/並列計算.md "wikilink")の並列性を明示的に書くことができ[最適化が行いやすく](../Page/コンパイラ最適化.md "wikilink")、そのため他の言語より高速である等の理由から\[1\]、[数値予報](../Page/数値予報.md "wikilink")および[気候モデル](../Page/気候モデル.md "wikilink")、[構造力学](../Page/構造力学.md "wikilink")における[有限要素法](../Page/有限要素法.md "wikilink")、[計算流体力学](https://ja.wikipedia.org/wiki/計算流体力学 "wikilink")、[計算物理学](../Page/計算物理学.md "wikilink")、[計算機化学](https://ja.wikipedia.org/wiki/計算機化学 "wikilink")、[計量経済学](../Page/計量経済学.md "wikilink")、動物と植物の[品種改良](../Page/品種改良.md "wikilink")などの大規模な計算を行う分野において、[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")で使われている\[2\]。

また、ちょうど[C言語](../Page/C言語.md "wikilink")に対する[C++言語](https://ja.wikipedia.org/wiki/C++言語 "wikilink")のように、Fortran 90/Fortran 95の言語仕様は、FORTRAN 77の頃と比べればかなり拡張され進歩したものとなっている。最新の[ソースコード](../Page/ソースコード.md "wikilink")は初期のものと比較すると、ほとんど別の言語のように見える。初期の頃は、[変数名が大文字](../Page/変数_\(プログラミング\).md "wikilink")6文字までで、[動的な記憶領域の確保ができないなど多くの制約があったが](../Page/動的メモリ確保.md "wikilink")、それらの制限は無くなり、Fortran77から[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")が、Fortran 90から[モジュラープログラミング](https://ja.wikipedia.org/wiki/モジュール#ソフトウエア "wikilink")、[配列演算とユーザー定義総称関数が](https://ja.wikipedia.org/wiki/ベクトル演算 "wikilink")、Fortran 95から[High Performance Fortranが](https://ja.wikipedia.org/wiki/High_Performance_Fortran "wikilink")、Fortran 2003から[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")が、Fortran 2008 からはコンカレント・コンピューティング（[並行計算](../Page/並行計算.md "wikilink")）が導入された。

なお、大文字でFORTRANと表記した場合、FORTRAN 77以前のFORTRANを指し、Fortranと表記した場合、Fortran 90以降を指すことがある。

## FORTRANの特徴

### Fortran 90/95の特徴

Fortran 90/95の特徴は、以下のように要約される\[3\] 。

  - 数値計算プログラムを簡単かつ簡潔に記述できる。
  - プログラムの誤りを犯しにくい言語である。
  - 数値計算のための便利な道具があらかじめ用意されている。
  - 作成したプログラムを大規模高速演算に使用できる。
  - 無料のコンパイラが公開されている。

### FORTRAN 77の特徴

広く使われていたFORTRAN 77 の特徴は、以下のように要約される。

  - 数式の計算が簡便に記述できる

<!-- end list -->

  -
    ほぼ数学の数式通りに計算式を記述できる。もっともこの特徴は他に計算向きの高級言語がなかった時代の話であり、現代の水準では「プログラミング言語における標準数式表現の始祖」といった方が当たっている。

<!-- end list -->

  - 入出力が容易

<!-- end list -->

  -
    簡単に出力形式を定義できるFORMAT文や、実際の出力デバイスを意識しないで済む[入出力](../Page/入出力.md "wikilink")文がある（[C言語](../Page/C言語.md "wikilink")の[標準入出力と似た概念である](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")）。

<!-- end list -->

  - スタック指向/構造化指向の言語ではない

<!-- end list -->

  -
    COMMON文、BLOCK DATA文やSAVE文など、データを静的に割り当てることを前提としている。

<!-- end list -->

  - プログラムの書式が固定形式である

<!-- end list -->

  -
    プログラム記述の方法がカラム位置に依存している（一部の実装では拡張されている）

## FORTRANの歴史

[FortranCardPROJ039.agr.jpg](https://ja.wikipedia.org/wiki/File:FortranCardPROJ039.agr.jpg "fig:FortranCardPROJ039.agr.jpg")に記されたFORTRANのコード。カラム1～5、6、73～80が制御用に確保されている。\]\] [ジョン・バッカス](../Page/ジョン・バッカス.md "wikilink")は1953年末、メインフレームコンピュータ[IBM 704のプログラムを開発するにあたり](../Page/IBM_704.md "wikilink")、[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")に代わるものを開発することを[IBM](../Page/IBM.md "wikilink")の上司に提案した。歴史的なFORTRAN開発チームはRichard Goldberg、Sheldon F. Best、Harlan Herrick、Peter Sheridan、[Roy Nutt](https://ja.wikipedia.org/wiki/Roy_Nutt "wikilink")、 Robert Nelson、Irving Ziller、[Lois Haibt](https://ja.wikipedia.org/wiki/Lois_Haibt "wikilink")、David Sayreというメンバーで構成された\[4\]。

*The IBM Mathematical Formula Translating System* のドラフト仕様は[1954年](../Page/1954年.md "wikilink")中旬に作成された。1956年10月にFORTRANの最初のマニュアルが作成され、[コンパイラ](../Page/コンパイラ.md "wikilink")は1957年4月に完成した。顧客はアセンブリ言語で記述されたコードに匹敵するパフォーマンスが得られない限り[高級言語を採用しないので](../Page/高水準言語.md "wikilink")、最初から[最適化コンパイラが開発された](../Page/コンパイラ最適化.md "wikilink")。

この新しい方法がハンドアセンブルより高速に動作するかどうかには疑いの目があったが、プログラム中の命令数を1/20に削減できるので急速に受け入れられていった。IBMの社内誌であるThinkに掲載された1979年のインタビューでバッカスは「私がこの仕事をしたのは面倒くさがりだったからです。私はプログラムを書くことが好きではなかったので、[IBM 701でミサイルの軌道計算プログラムを開発したときに](https://ja.wikipedia.org/wiki/IBM_701 "wikilink")、プログラムの開発を簡単にするためにプログラミングシステムを作り始めました。」\[5\]と語っている。

FORTRANは科学者の間で数学を応用したプログラムの記述に広く用いられたことから、より高速で効率的なコードを出力しようとする原動力となった。またライブラリでなく言語として[複素数](../Page/複素数.md "wikilink")[型をサポートしたことは](../Page/データ型.md "wikilink")、電気電子工学における動的特性の計算などに代表される科学や工学分野のプログラムを書きやすくした。

1960年までに様々なバージョンのFORTRANが[IBM 709](../Page/IBM_709.md "wikilink")、[IBM 650](../Page/IBM_650.md "wikilink")、[IBM 1620](../Page/IBM_1620.md "wikilink")、[IBM 7090で動作していた](../Page/IBM_7090.md "wikilink")。FORTRANのユーザー数は急増し、コンピューターメーカーがFORTRANコンパイラをこぞって提供したので、1963年までには40を超えるFORTRANコンパイラが存在していた。こうしたことから、FORTRANはアーキテクチャの異なる様々なコンピュータで広くサポートされた最初の言語と言える。

FORTRAN開発の歴史は、初期の[コンパイラ](../Page/コンパイラ.md "wikilink")技術の歴史そのものといえる。FORTRANで効率的なコードを出力したいという強い要求からコンパイラによる最適化技術が大きく進歩した。

### FORTRAN

[IBM_704_mainframe.gif](https://ja.wikipedia.org/wiki/File:IBM_704_mainframe.gif "fig:IBM_704_mainframe.gif") [メインフレーム](../Page/メインフレーム.md "wikilink") \]\] IBM 704用に開発された最初のFORTRANは32の命令をもっていた。

### IBM 1401版FORTRAN

IBM 1401版は革新的な65パスのコンパイラであり、わずか8k語の[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")で動作する。コアに記録されたプログラムが段階的に実行可能なコードへと変換されて上書きされる。変換されたコードは[機械語](../Page/機械語.md "wikilink")ではなく、[UCSD PascalのPコードが生まれるよりも](https://ja.wikipedia.org/wiki/UCSD_p-System "wikilink")20年も前ながら、中間コードを利用していた。

### FORTRAN II

IBMの*FORTRAN II*は1958年に開発された。主な改良点は[手続き型プログラミング](../Page/手続き型プログラミング.md "wikilink")のサポートであり、サブルーチンや関数を定義できるようになった。

その後、FORTRAN IIのデータ型として、`DOUBLE PRECISION`（倍精度型）と`COMPLEX`（複素数型）が追加された。

### FORTRAN III

IBMは1958年に*FORTRAN III*を開発していた。いくつかの新機能に加えインラインアセンブラが可能であった。しかしながらこのバージョンは販売されなかった。704 FORTRANやFORTRAN IIと同様に、FORTRAN IIIにも移植の妨げになるような機種依存の機能があった。他のベンダーから販売されていたFORTRANも初期は同様の問題を抱えていた。

### FORTRAN IV

IBMは1961年に顧客の要望を受け*FORTRAN IV*の開発を開始した。`READ INPUT TAPE`のようなFORTRAN IIの機種依存部分を削除したほか、`LOGICAL`（論理型）、[論理演算](../Page/論理演算.md "wikilink")、算術[IF文の代替となる](../Page/If文.md "wikilink")**論理IF文**が加えられた。この時のターゲットマシンは36ビットのワードマシンだったので、[整数](../Page/整数.md "wikilink")値は2<sup>35</sup>の大きさの範囲で定義されていた。また、[実数](../Page/実数.md "wikilink")の精度は2<sup>27</sup>、倍精度実数の精度は2<sup>54</sup>までだった。FORTRAN IVは1962年に[IBM 7030](../Page/IBM_7030.md "wikilink")（通称ストレッチ）用がリリースされ、後に[IBM 7090版と](../Page/IBM_7090.md "wikilink")[IBM 7094版がリリースされた](https://ja.wikipedia.org/wiki/IBM_7094 "wikilink")。

1965年には[国家規格であるANSI](../Page/国際規格.md "wikilink") X3.4.3 FORTRANに準拠した。

### FORTRAN 66

*American Standards Association*（現[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")）がFORTRANの米国規格を委員会で制定するようになったことはFORTRANの歴史の要である。[1966年](../Page/1966年.md "wikilink")に2つの異なる言語が制定された。一つは当時既に[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")であったFORTRAN IVを基にした*FORTRAN*であり、もう一つはFORTRAN IIを基にして機種依存部分を取り除いた*Basic FORTRAN*である。最初に制定されたFORTRANの規格は後に*FORTRAN 66*と呼ばれた。

### FORTRAN 77

FORTRAN 66 規格のリリース後、コンパイラ・ベンダーは多くの拡張を"標準Fortran"に導入し、1966の規格の改訂を始めるようにANSIを促した。この改訂は1977年に制定され、最終的な改訂案は1978年4月に新しいFORTRAN標準として承認された。この新しい標準は*FORTRAN 77*として知られ、FORTRAN 66後の多くの変更を追加し、多くの重要な機能を加えた:

  - ブロック `IF`と`END IF` ステートメント、オプショナルな`ELSE`と`ELSE IF` ステートメント。改善された言語サポートのための[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")。
  - DOループ機能拡張、パラメータ記述を含む、負の増分とゼロのトリップ・カウント（これ以前のFORTRANではDOループは繰り返しを必ず１回は行うことになっていたのを廃止した）。
  - 改良されたI/Oのための`OPEN`, `CLOSE`, と `INQUIRE`文。
  - ダイレクト-アクセス ファイル I/O。
  - `IMPLICIT` 文。
  - `CHARACTER` データ・タイプ。文字の入出力と処理のための大幅な増補。
  - `PARAMETER` 定数を指定するためのステートメント。
  - 永続的なローカル変数`SAVE`ステートメント。
  - 内部関数のための総称関数。
  - [ASCII](../Page/ASCII.md "wikilink") 文字列シーケンスにベースをおく、文字列比較のための内部命令セット(`LGE, LGT, LLE, LLT`)。

この規格の改訂において、多くの機能は除去されるか変えられ、以前の標準に合致していたプログラムの多くはおそらく無効になった。この時点で除去はX3J3の代替だけが許容された。だからコンセプト "不賛成"はANSI標準においては利用できなかった。しかし、コンフリクトリストの24アイテム（Appendix A2 of X3.9-1978を見よ）ループホールスとパスロジカルケースは以前の標準規格から許容されたが、しかし滅多に使用されない。少数の機能は慎重に除去された

  - ホレリス定数とホレリス・データ、すなわち：

<!-- end list -->

  -

      -
        `GREET = 12HHELLO THERE!`

<!-- end list -->

  - FORMAT 記述子におけるH編集（ホレリス・フィールド）の読み込み（以前はホレリスで確保された文字列データの領域に入力文で文字列を読み込めた（データが上書きされる））。
  - アレイの添え字における境界のオーバーインデクシング。

<!-- end list -->

  -

      -
        `DIMENSION A(10,5)`
        `Y= A(11,1)`

<!-- end list -->

  - DOループから、ループ外への移動と帰還（"エクステンデット・レンジ"（DOループの拡張範囲）として知られる）。
  - 以前の規格では文字型(CHARACTER型)がなかったので、文字データや文字列データを整数や実数の変数や配列に格納することが行われていたが、Fortran77ではそれを廃止した。

### Fortran 90

一般に*Fortran 90* として知られている規格は、大幅に発表が遅れたもののFORTRAN 77の正当な継承者であり、最終的に1991年にISO規格、1992年にANSI規格としてリリースされた。この抜本的な改訂では1978年のFORTRAN 77規格制定からのプログラミング技術における大幅な変化を反映するために、以下の多くの新しい機能が加えられた

  - フリーフォームソース入力と小文字のFortranキーワード。プログラム本文を7桁目から書かなくても良く、80桁の制限も無い。

<!-- end list -->

``` fortran
if (x<0) then
x=0
end if
```

  - 最長31文字までの識別子。

<!-- end list -->

``` fortran
abcdefghijklmnopqrstuvwxyz12345=0.0e0
```

  - インラインコメント。

<!-- end list -->

``` fortran
! これは"!"を用いたコメントです
```

  - 配列演算（あるいは部分配列演算）。これは数学とエンジニアリングの計算を大幅に簡素化する。
  - 全部または部分マスクされた、配列の指定と配列の表現、例えば、

<!-- end list -->

``` fortran
x(1:n)=r(1:n)*cos(a(1:n))
```

  - 選択的配列のアサインのためのwhere文。

<!-- end list -->

``` fortran
integer::a(10)
real(8)::b(10)
a=f(x)
where(a>0)
b=-1.0
elsewhere
b=1.0
end where
```

  - 配列の定数と式による初期化。
  - ユーザ定義の配列を返す関数と配列コンストラクタ。

<!-- end list -->

``` fortran
function sample(x) result(y) !配列yを返す
integer,parameter::nn=4
real::y(nn)=(/ 1,2,3,4 /) !配列のコンストラクタと定数による初期化
....
end function sample
```

  - 再帰手続き。
  - モジュラープログラム、すなわち関係するサブルーチンとデータのグループ化と、他のプログラムユニットで使用、モジュールの内の指定した部分だけの使用を含む。
  - interface文を使用してコンパイル時に型がチェックされる大幅に改善された引数渡しメカニズム。

<!-- end list -->

``` fortran
module my_lib !モジュール
interface
function sample(x)
real,intent(in)::x(:)!コンパイル時に変数の型の整合性とデータの入出力方向がチェックされる。
....
end function sample
end interface
end module
```

  - ユーザー定義総称関数(同じ関数名で、引数の数とタイプを自動的に識別して異なる内部関数を呼び出す)のインターフェース。
  - 演算子('+'、'-'、など)のオーバーローディング（多重定義）。
  - 派生型データタイプ。
  - 変数のデータタイプと他の属性を指定するための新たなデータタイプの宣言シンタックス、
  - allocatable属性と allocateとdeallocate文を用いたダイナミックメモリアロケーション。

<!-- end list -->

``` fortran
real,allocatable::temp(:)
allocate(temp(nn))
deallocate(temp)
```

  - ポインター属性とポインターアサイン、nullify文によるダイナミックデータ構造の扱い。
  - do 文の end do による終端。
  - do while 文
  - exit文によるdo文からの脱出と、cycle文によるdo文の次の繰り返しへの移行。

<!-- end list -->

``` fortran
do i=1,nn
if (b(i) /= 0) then
a(i) = 1.0 / b(i)
else
exit
end if
end do
```

  - select文。

<!-- end list -->

``` fortran
select case (sw)
case ('++')
a = a + 1
case ('--')
a = a - 1
case default
a = 0
end select
```

  - ユーザがコントロールできる数値精度の移植性の良い指定方法。

<!-- end list -->

``` fortran
a=1.0e0_kind(1.0d0)
```

  - 新しく導入された内部関数。それに伴い従来の文関数(statement function)は廃止予定に。

#### 削除または時代遅れとされた機能の一覧

以前のバージョンとは異なり、Fortran 90は、何の機能も削除しなかった。（Appendix B.1には、「この規格の、削除した機能のリストは空である。」と記載されている）つまり、FORTRAN 77に準拠したプログラムは、Fortran 90にもまた準拠している。そして、両方の規格で、その動作が定義づけられた項目は使用可能でなければならない。一部の機能はFortran 95で「削除」され、また機能の小さな部分は「時代遅れ」と認定されて将来の規格で除去されることが予定された。

<table>
<thead>
<tr class="header">
<th><p>時代遅れの機能</p></th>
<th><p>例</p></th>
<th><p>状態 / Fortran 95での予定</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>算術 IF-statement</p></td>
<td><p><code>    IF (X) 10, 20, 30</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>非-整数 DO パラメータ あるいは制御変数</p></td>
<td><p><code>    DO 9 X= 1.7, 1.6, -0.1</code></p></td>
<td><p>削除</p></td>
</tr>
<tr class="odd">
<td><p>Shared DO-loop termination or<br />
termination with a statement<br />
other than END DO or CONTINUE  </p></td>
<td><p><code>    DO 9 J= 1, 10</code><br />
<code>        DO 9 K= 1, 10</code><br />
<code>9   L= J + K</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ブロック外部からの<br />
END IFへのブランチ</p></td>
<td><p><code>66  GO TO 77 ; . . .</code><br />
<code>    IF (E) THEN ;     . . .</code><br />
<code>77  END IF</code></p></td>
<td><p>削除</p></td>
</tr>
<tr class="odd">
<td><p>Alternate return</p></td>
<td><p><code>    CALL SUBR( X, Y *100, *200 )</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>PAUSE文</p></td>
<td><p><code>    PAUSE 600</code></p></td>
<td><p>削除</p></td>
</tr>
<tr class="odd">
<td><p>ASSIGN statement<br />
  と assigned GO TO statement</p></td>
<td><p><code>100  . . .</code> <code>    ASSIGN 100 TO H</code><br />
<code>    . . .</code><br />
<code>    GO TO H . . .</code></p></td>
<td><p>削除</p></td>
</tr>
<tr class="even">
<td><p>Assigned FORMAT specifiers</p></td>
<td><p><code>    ASSIGN F TO 606</code></p></td>
<td><p>削除</p></td>
</tr>
<tr class="odd">
<td><p>H edit descriptors</p></td>
<td><p><code>606 FORMAT ( 9H1GOODBYE. )</code></p></td>
<td><p>削除</p></td>
</tr>
<tr class="even">
<td><p>Computed GO TO statement</p></td>
<td><p><code>    GO TO (10, 20, 30, 40), index</code></p></td>
<td><p>(時代遅れ)</p></td>
</tr>
<tr class="odd">
<td><p>文関数</p></td>
<td><p><code>    FOIL( X, Y )= X**2 + 2*X*Y + Y**2</code></p></td>
<td><p>(時代遅れ)</p></td>
</tr>
<tr class="even">
<td><p>DATA statements<br />
  among executable statements</p></td>
<td><p><code>    X= 27.3</code><br />
<code>    DATA A, B, C / 5.0, 12.0. 13.0 /    . . .</code></p></td>
<td><p>(時代遅れ)</p></td>
</tr>
<tr class="odd">
<td><p>CHARACTER* form of CHARACTER declaration</p></td>
<td><p><code>    CHARACTER*8 STRING   ! Use CHARACTER(8)</code></p></td>
<td><p>(時代遅れ)</p></td>
</tr>
<tr class="even">
<td><p>Assumed character length functions</p></td>
<td><pre class="fortranfixed"><code>      CHARACTER*(*) STRING</code></pre></td>
<td></td>
</tr>
<tr class="odd">
<td><p>固定フォームソースコード</p></td>
<td><p>* Column 1 contains * or ! or C for comments.<br />
C       Column 6 for continuation.</p></td>
<td></td>
</tr>
</tbody>
</table>

#### "Hello world"の例

``` fortran
program helloworld
print *, "Hello, world."
end program helloworld
```

### Fortran 95

[right](https://ja.wikipedia.org/wiki/画像:Earth_simulator_ES2.jpg "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")\]\] *Fortran 95*は、マイナーな改訂版である。ほとんどは、Fortran 90規格の、いくつかの大きな問題を解決するためのものである。それにも係わらず、Fortran 95もまた年号を付加されている。それは、Fortranの拡張として定義される並列言語、HPF（[High Performance Fortran](https://ja.wikipedia.org/wiki/High_Performance_Fortran "wikilink")：ハイ・パフォーマンスFortran）の一部導入によることは明白である。なお、本格的なHPFは、[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")等で使用されている\[6\]。

  - `forall`と階層化された`where`がベクトル化のために追加された。
  - ユーザ定義の `pure` と `elemental` プロセジャーが追加された。
  - 派生タイプコンポーネントのデフォルト初期化、これはポインターの初期化を含むが追加された。
  - データオブジェクトの初期化表記を使うための拡張が追加された。
  - `allocatable` アレイがスコープから出た時に自動的に`deallocate`されることの明確な定義が追加された。

多くの内部関数は拡張された。一例として`maxloc` 内部関数に`dim`引数が追加された

Fortran 90で時代遅れとされた、いくつかの機能はFortran 95から削除された。

  - `REAL`と`DOUBLE PRECISION`変数を使用した`DO` ステートメントは削除された。
  - `END IF`ステートメントへのブロック外部からのブランチは削除された。
  - `PAUSE` ステートメントは削除された。
  - `ASSIGN`と`ASSIGN`型`GOTO` ステートメント、`ASSIGN`フォーマット指定は削除された。
  - `H` edit descriptor（いわゆるホレリス定数（[:en:Hollerith constant](https://ja.wikipedia.org/wiki/:en:Hollerith_constant "wikilink")））は削除された。

Fortran 95への重要な追加は、一般には*Allocatable TR*として知られる、*ISO technical report、TR-15581: Enhanced Data Type Facilities*である。この仕様は、Fortran 2003準拠のFortran コンパイラより前に、`ALLOCATABLE` アレイの強化した用法を定義した。そのような用法は、プロセジャーのダミー引数リストとしての派生タイプコンポーネント`ALLOCATABLE`アレイと、関数の返し値を含む。`ALLOCATABLE`アレイは、`POINTER`-ベース・アレイより好ましいものである。なぜなら、`ALLOCATABLE` アレイは、スコープから抜けたとき、Fortran 95による自動的なdeallocateを保証しメモリリークの可能性をなくすからである。

[エイリアシング](https://ja.wikipedia.org/wiki/エイリアシング "wikilink")はarrayの参照において最適化の障害にならず、Fortranコンパイラがポインタ-ベース・アレイより高速なコードを生成することを可能にする。

他の重要なFortran 95への追加は、ISO technical report *TR-15580: 浮動小数点例外ハンドリング*である。一般にはIEEE TRとして知られており、この仕様はIEEE 浮動小数点演算と例外ハンドリングを定義する。

#### 条件付コンパイルと可変長文字列

必須のベース言語（ISO/IEC 1539-1:1997に定義）以外に、Fortran 95言語も以下の2つのオプショナルなモジュールを含む。

  - 可変文字列（ISO/IEC 1539-2 : 2000）
  - 条件付コンパイル（ISO/IEC 1539-3 : 1998）

両者は、マルチパート国際標準を構成する（ISO/IEC 1539）。規格の開発者は、「オプショナル・パートは必要なものを完備した機能を記述している、それは多くのコンパイラ・インプリメンターとユーザーから要求されてきたものである。しかし、それらは、全てのFortran標準に合致するコンパイラは十分な一般性を持たないと考えられていた。それにも係わらず、もし標準に合致したFortranがそのようなオプションを提供するなら、『それらの機能は、標準規格の適切なパートに記述に従って提供されなければならない。』」と述べている。

### Fortran 2003

*Fortran 2003*はメジャーな改訂であり、たくさんの新しい機能を導入した。 Fortran2003における新しい機能の包括的なサマリーは、Fortran Working Group (WG5)のオフィシャルWebサイトから得ることができる\[7\]。

この記事によれば、このバージョンが含む大幅な強化は以下の通りである。

  - 派生タイプの強化：使用法が進歩したコントロール、パラメータ化された[派生型](../Page/派生型.md "wikilink")、改善された構造化[コンストラクタ](../Page/コンストラクタ.md "wikilink")とファイナライザー。
  - オブジェクト指向プログラミングのサポート：[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")のタイプの拡張と[インヘリタンス](https://ja.wikipedia.org/wiki/インヘリタンス "wikilink")、[ポリモーフィズム](../Page/ポリモーフィズム.md "wikilink")、ダイナミック・タイプアロケーション、タイプ-バウンド・プロセジャー。
  - データマニピュレーション・エンハンスメント：allocatable コンポーネント (TR 15581の組み入れ)、遅延タイプパラメータ、ボラタイル・アトリビュート、ポインタ-の強化、初期化拡張、内蔵関数の強化。
  - 入出力の強化：非同期転送、ストリーム・アクセス、派生タイプのためのユーザ定義転送オペレーション、ユーザ指定のフォーマット変換時の丸めの制御、接続前のユニットの名前付定数、`FLUSH` ステートメント、キーワードの規則化、エラーメッセージへのアクセス。
  - プロセジャーのポインター。
  - IEEE 浮動小数点と浮動小数点例外処理のサポート(TR 15580の組み入れ)。
  - C言語との相互運用。
  - 国際的な慣習のサポート：ISO 10646（国際文字セット）の4バイト文字の利用、数値形式の入出力でのデシマル(.)とコンマ(,)の選択。
  - ホスト・オペレーティングシステムとの一体化の強化。コマンドライン引数、環境変数とプロセッサーエラーメッセージ。

Fortran 2003 への重要な追加は、ISO technical report TR-19767である。

Fortranにおけるモジュール機能の強化。このレポートは、*submodules*を提供する。これは、Fortranのモジュールをより[Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")のモジュールに近づける。これらは、Adaのプライベート・チャイルド・サブユニットに似ている。これは分離したプログラムユニットとして表現すべきモジュールの仕様と実装を可能にし、大規模なライブラリのパッケージ化を改善し、インターフェース定義を公開しても企業秘密を保持することを可能にし、コンパイレーション・カスケードを防ぐ。

### Fortran 2008

最新の規格であり一般にはFortran 2008として知られているISO/IEC 1539-1:2010は2010年9月に承認された\[8\]。Fortran 95と同様に、これはマイナー・アップグレードである。Fortran 2003の明確化と訂正と共に、新しい特長も導入された。新しい特長は、以下を含む

  - モジュール構造の追加、ISO/IEC TR 19767:2005にとってかわるサブモジュール。
  - [Co-array Fortran](https://ja.wikipedia.org/wiki/Co-array_Fortran "wikilink")―並列計算モデル。
  - do concurrent―相互依存のない繰返しループのための並列DOループ。
  - メモリ上のレイアウトを指定するためのCONTIGUOUS（隣接）属性。
  - コンストラクト・スコープ付のオブジェクトの宣言を含むブロック・コンストラクト。
  - 派生タイプにおける再帰的ポインターの代替としての再帰的アロケータブル・コンポーネント。

ファイナル・ドラフト・スタンダード（FDIS）は、ドキュメントN1830として利用できる\[9\]。

Fortran 2008における重要な追加は、[ISO](https://ja.wikipedia.org/wiki/ISO "wikilink")テクニカルスペシフィケーション(TS) 29113のFortranにおけるC言語とのより高いインターオペラビリティであり\[10\]\[11\]、2012年5月のISOの承認に向けてまとめられた。C言語の配列へのFortranアクセスに関してタイプとランクを無視する仕様が加えられた。

### Fortran 2018

Fortran 2018の最新版は、以前はFortran 2015と呼ばれていた\[12\]。大きな改訂が行われ、2018年11月28日にリリースされた\[13\]。

Fortran 2018には、それ以前に公開された以下の2つの技術仕様が含まれている。

  - ISO/IEC TS 29113:2012 Further Interoperability with C\[14\]
  - ISO/IEC TS 18508:2015 Additional Parallel Features in Fortran\[15\]

追加の変更と新機能には、ISO/IEC/IEEE 60559:2011（2019年時点の[IEEE浮動小数点数仕様の最新版](../Page/IEEE_754.md "wikilink")）のサポート、16進の入出力、IMPLICIT NONE拡張など、様々な変更が含まれている\[16\]\[17\]\[18\]\[19\]。

## 科学分野と工学分野での利用

1968年に[BASIC](../Page/BASIC.md "wikilink")の作者等によって書かれた専門雑誌の記事でもすでに「旧式の（old-fashioned）プログラミング言語」と記述されていたが\[20\]、Fortranは現在でも数十年に渡って使用されており、特に科学や工学のコミュニティでは、Fortranで書かれたソフトウェアが日常的に幅広く利用されている\[21\]。は1984年に「物理学と気象学の学生はFORTRANを必ず学ぶ必要がある。大部分の成果がFORTRANで書かれており、科学者たちがPascalやModula-2などの他の言語に移行する可能性は極めて低い。」と書いている\[22\]。1993年、[Cecil E. Leithは](https://ja.wikipedia.org/wiki/Cecil_E._Leith "wikilink")、FORTRANを「科学計算の母語」であると評し、他の言語によって置き換えられる可能性は「永遠の希望であり続けるだろう」と述べている\[23\]。

## 言語仕様の変遷

FORTRAN 66以降、[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")、[JISで仕様が制定されている](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")。Fortranの言語仕様は、年代によってかなり変化して来ている。他の[プログラミング言語](../Page/プログラミング言語.md "wikilink")で[実装](../Page/実装.md "wikilink")された[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")の機能などがどんどん取り入れられて来ているからである。

  - FORTRAN 66とFORTRAN 77の言語仕様の詳細は、[FORTRAN 77の言語仕様を参照のこと](https://ja.wikipedia.org/wiki/FORTRAN_77の言語仕様 "wikilink")。
  - Fortran 90以降の言語仕様の詳細は、[Fortranの言語仕様](https://ja.wikipedia.org/wiki/Fortranの言語仕様 "wikilink")を参照のこと。

### 初期 (FORTRAN 66)

1966年にANSI X3.9-1966が制定され、JISとしては1967年に制定された。この時は、以下の3つの水準ごとに独立したJISが制定された。共通したタイトルは「電子計算機プログラム用言語 FORTRAN」だった。以下に水準間のおおよその違いを記す。

  - JIS C 6201（水準7000）
      - [複素数](../Page/複素数.md "wikilink")型と[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")[実数](../Page/実数.md "wikilink")型がある
      - DATA[文と初期値設定副プログラム](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")（BLOCK DATA文）がある
      - FORMAT文中の欄記述子にD,G,Aが定義できる
      - [変数](../Page/変数_\(プログラミング\).md "wikilink")、[配列](../Page/配列.md "wikilink")手続き名は最大6文字
  - JIS C 6202（水準5000）
      - 変数、配列手続き名は最大6文字
  - JIS C 6203（水準3000）
      - 変数、配列、手続き名は最大5文字
      - [論理型](https://ja.wikipedia.org/wiki/論理型 "wikilink")のデータ、論理式、関係式、論理[IF文は使えない](../Page/If文.md "wikilink")。
      - [型宣言文がない](../Page/データ型.md "wikilink")。
      - EXTERNAL文がない。
      - 3[次元](../Page/次元.md "wikilink")の配列がない。
      - 名前付きCOMMON文がない。
      - 文番号は4桁
      - COMMON文に配列宣言が使えない。
      - 整合配列がない。

なお、1971、1976年に若干の改訂がなされている。

### FORTRAN 77時代

国際標準化機構（[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")）は、米国規格協会（[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")）の X3J3 が作成した FORTRAN の規格 X3.9-1978 を ISO 1539-1980 として定めた。基本水準（subset language）と上位水準（full language）の2種類の水準からなっていた。これを基にして、同じく2水準の JIS C 6201-1982 が制定された。なお、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に、JISの分類が変更になり、この規格は JIS X 3001-1982 となった。内容には変更はない。

### Fortran 90時代

FORTRAN 77を基に他の言語の特徴を組み込み、言語仕様を近代化しようとしたが、そのため仕様がなかなか決まらず、1991年に ISO/[IEC](../Page/国際電気標準会議.md "wikilink") 1539:1991として制定された。JISではそれを受け、JIS X 3001:1994が制定された。

### Fortran 95時代

JIS X 3001:1998では，Fortran 95と通称される規格が引用されている。該規格は一部例外を除きJIS X 3001 1-1994の上位互換拡張である。

### Fortran 2003時代

JIS X 3001:2009（2019年現在の最新改正版）では，Fortran 2003と通称される規格が引用されている。該規格は一部例外を除きJIS X 3001-1:1998の上位互換拡張である\[24\]。

### Fortran 2008時代

## FORTRANと教育

### 教育向けコンパイラ

FORTRANは、[情報処理](../Page/情報処理.md "wikilink")分野で広く使われていたため、学校や会社の教育（情報処理技術者向け教育）で利用された。教育向けには、より詳細なエラー情報を出すための拡張がWaterloo大学でWATFOR（後にWATFIV）[コンパイラ](../Page/コンパイラ.md "wikilink")として実装された。この実装は日本の大学でも使われた。

## Fortranとスーパーコンピュータ

Fortranは科学技術計算用の言語なので、[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")での[プログラミング言語](../Page/プログラミング言語.md "wikilink")としてよく用いられる。実際、多くのスーパーコンピュータで提供されている言語は、C/C++およびFortranである。

[C言語](../Page/C言語.md "wikilink")と比較すると、Fortranは[スタック](../Page/スタック.md "wikilink")等を使わず、コンパイル時に静的に記憶領域を確保するのが基本である。そのため、自由度が高くあらゆる状況を想定しなければならない[C言語](../Page/C言語.md "wikilink")と比べると[コンパイラ](../Page/コンパイラ.md "wikilink")はコードを最適化しやすいという利点がある。

Fortranは、いまでも科学技術用[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")演算での使用が基本であり、ベクトル型[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")は、Fortranを使った[プログラムで使用することが多い](../Page/プログラム_\(コンピュータ\).md "wikilink")。そこで、スーパーコンピュータの高速演算機能を有効に使うための工夫がなされた。その1つの例としては、自動[ベクトル化](../Page/ベクトル化.md "wikilink")機能である。[ベクトル](../Page/ベクトル.md "wikilink")型のスーパーコンピュータは、多くの演算を同時に行うベクトル演算機能が[ハードウェア](../Page/ハードウェア.md "wikilink")で提供されている。この機能を有効に使うために、FortranのDO[ループをベクトル演算装置で演算させるために](../Page/ループ_\(プログラミング\).md "wikilink")、自動的にベクトル[命令にする機能が提供された](../Page/命令_\(コンピュータ\).md "wikilink")。また、DOループ内のベクトル演算に適さないものをDOループ外に追い出す機能などもある。たとえば、

``` fortran
DO 100 I=1,N
A(I) = B(I) * C(I)
100 CONTINUE
```

のようなDO構文は、ほとんどの場合、1から数個のベクトル演算命令に[コンパイルされる](../Page/コンパイラ.md "wikilink")。そのほかにもDOループの中にIF文を含むような例、たとえば、

``` fortran
DO 110 I=1,N
IF (A(I) .LE. LIMIT) THEN
B(I) = A(I) * Z
END IF
110 CONTINUE
```

のようなものもベクトル化できる場合がある。これは、いったんAの各要素がLIMIT以下かどうかを示すマスクベクトルを作成し、Aという配列（=ベクトル）に、変数Zをかけるとき、マスクベクトルを参照してベクトル演算を行うことによって、DOループをベクトル化する。

このような作業は、すべて[コンパイラ](../Page/コンパイラ.md "wikilink")が行い、利用者にはできるだけ負担をかけないようにしている。しかし、より高度なベクトル化を行うために、[最適化を行う支援ツールが用意されている場合もある](../Page/最適化_\(情報工学\).md "wikilink")。

## FORTRANと日本語

コンピュータ上で[日本語](../Page/日本語.md "wikilink")の文字を扱えるようになると、FORTRANでも日本語を扱う需要が出てきた。そのため、各社（[メインフレーム](../Page/メインフレーム.md "wikilink")を作成していたメーカ）では、独自に言語仕様に日本語の文字を扱えるように拡張した。そのため、各社で日本語の扱い方が異なる事態になった。そこで、[JEIDA](https://ja.wikipedia.org/wiki/JEIDA "wikilink")では1985年に、JEIDA-42で日本語FORTRANを策定した。

FORTRANで日本語の文字を扱う場合、識別子である[変数名](../Page/変数_\(プログラミング\).md "wikilink")､仮引数名、プログラム名、関数名、サブルーチン名、共通ブロック名等には日本語の文字は使えず、データとしての日本語の文字列を扱うための専用の型（日本語型）、日本語の文字列を入出力するためのFORMAT文の編集子の拡張が行われた。

（Fortranプログラムのすべての識別子に日本語の文字を許すように拡張するとなると、コンパイラだけではなくて、リンカー、ローダー、デバッガー、アセンブラ、OS上でのファイル名の扱いなどにおいて、日本語の文字例を受け付けるように拡張する必要があろう。 また､FORTRAN文法上の単語であるIF, DO, END, ELSE, WHILE, RETURN, SUBROUTINE などにも半角文字と全角文字を同じ文字として扱うかどうかなど。 また、識別子として全角の英文字と半角の英文字を同一と見なすかどうか､全角の空白文字と半角の空白文字を同一とみなすかどうか、またプログラム中に書かれた記号文字や数字の全角文字と半角文字の区別をどうするかなど曖昧なところがあるであろう。 もちろんそれらは文字列データーとしては区別がされなければならない。）

## FORTRANベースの言語

FORTRAN 77に先立つFORTRANベースの[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")は使いやすい言語を提供するために広く使われた。プリプロセスされたコードは、任意のマシンの標準のFORTRANコンパイラでコンパイルすることができるという利点を持つ。これらのプリプロセッサは通常、構造化プログラミング、6文字よりも長い変数名、追加のデータ型、条件付きコンパイル、さらにはマクロ機能をサポートしていた。

ポピュラーなプリプロセッサとしてFLECSとiftran、MORTRAN、SFtran、S-Fortran、[Ratfor](https://ja.wikipedia.org/wiki/Ratfor "wikilink")、Ratfivがあった。例えば、RatforとRatfivはCライクな言語を実装し、プリプロセスにより標準的なFORTRAN 66コードを出力した。Fortran言語の進歩にもかかわらず、プリプロセッサは条件付きコンパイルとマクロ置換のために使用され続けている。

LRLTRANは、ローレンス放射線研究所で、ベクトル演算および動的な記憶、システムのプログラミングをサポートする他の拡張機能を提供するために開発され、ディストリビューションにはLTSSオペレーティングシステムが含まれていた。Fortran 95規格は、任意の条件付きコンパイルの機能を定義するオプションパート3を備えている。この機能は、しばしば 『CoCo』と呼ばれている。多くのFORTRANコンパイラは、それらのシステムにCプリプロセッサのサブセットを取り込んだ。

SIMSCRIPTは、大規模な離散システムのモデリングとシミュレーションのためのアプリケーションに特化したFortranのプリプロセッサである。

プログラミング言語Fは、FORTRANのEQUIVALENCE文などの、冗長、非構造化、非推奨な機能を削除したFortran 95のクリーンなサブセットとして設計された。 FはFortran 90で追加された配列演算の機能を使い、FORTRAN 77とFortran 90で追加された制御文を用い、構造化プログラミングで廃止された制御文を削除した。設計者はFを 『特に教育や科学技術計算に適した、構造化された配列プログラミング言語である。』 と述べている\[25\]。

## 主な処理系

### Windows

  - フリーソフト

<!-- end list -->

  - [GFortran](https://ja.wikipedia.org/wiki/GFortran "wikilink") - Fortran95/77処理系、[GCCのバージョン](../Page/GNUコンパイラコレクション.md "wikilink")4.0.0以降より標準
  - [G95](https://ja.wikipedia.org/wiki/G95 "wikilink") - [GNU](../Page/GNU.md "wikilink")のFortran95処理系
  - FTN95 [Silverfrost FTN95: Fortran for Windows](https://www.silverfrost.com/default.aspx)
  - Open Watcom [Open Watcom](http://www.openwatcom.org/index.php/Main_Page)

<!-- end list -->

  - 商用ソフト

<!-- end list -->

  - Absoft Pro Fortran
  - Intel Visual Fortran
  - NAG Fortran
  - Lahey Fortran

### Linux

  - フリーソフト

<!-- end list -->

  - [GFortran](https://ja.wikipedia.org/wiki/GFortran "wikilink")
  - [G95](https://ja.wikipedia.org/wiki/G95 "wikilink")
  - Open Watcom [Open Watcom](http://www.openwatcom.org/index.php/Main_Page)
  - Intel Fortran Composer XE 2011 for Linux - 非商用利用に限りフリーで使用可

<!-- end list -->

  - 商用ソフト

<!-- end list -->

  - Absoft Pro Fortran
  - Intel Visual Fortran
  - NAG Fortran
  - Open64
  - PGI Fortran
  - Sun Studio

### その他

  - [f2c](http://netlib.bell-labs.com/netlib/f2c/) - [ベル研究所](../Page/ベル研究所.md "wikilink")のFortran77を[C言語](../Page/C言語.md "wikilink")に変換するトランスレータ

## 脚注

<references/>

## 参考文献

  - [Valmer Norrod, et al:"A self-study course in FORTRAN programing - Volume I - textbook", Computer Science Corporation El Segundo, California, (April,1970). NASA(N70-25287).](https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/19700015982.pdf)
  - [Valmer Norrod, Sheldom Blecher, and Martha Horton: "A self-study course in FORTRAN programing - Volume II - workbook", NASA CR-1478, Vol.II (April,1970), NASA(N70-25288).](https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/19700015983.pdf)
  - [History of FORTRAN and FORTRAN II](http://www.softwarepreservation.org/projects/FORTRAN/)
  - [Fortran入門](http://www.nag-j.co.jp/fortran)
  - [Fortran2003入門](http://www.nag-j.co.jp/fortran/fortran2003/index.html)
  - [JTC1/SC22/WG5 The official home of Fortran Standards](http://www.nag.co.uk/SC22WG5/)
  - [陰山聡『Fortran90/95入門』神戸大学、大学院システム情報学研究科計算科学専攻、教授](http://www.research.kobe-u.ac.jp/csi-viz/members/kageyama/lectures/H22_FY2010_former/ComputationalScience/2_1_f95a.html)
  - [Fortran90を用いたプログラミングの記述方法(JAMSTEC)](http://www.jamstec.go.jp/es/jp/simschool/f90learning/index.html)　※ これはユーザー向けの解説書で、言語規格の記述としては厳密ではないところが多少ある。
  - [今時の Fortran 入門 ( Introduction to Modern Fortran )](https://qiita.com/cure_honey/items/795bd0e048ffeadc3e63)

<!-- end list -->

  - [浦昭二](../Page/浦昭二.md "wikilink")、近藤頌子、土居範久、原田賢一『FORTRAN 77入門』[培風館](../Page/培風館.md "wikilink")、（1982年）。
  - 森口繁一:「JIS FORTRAN入門 (上)」第3版、東京大学出版会、ISBN978-4130620307、(1984年1月)。
  - 西村恕彦, 酒井俊夫, 高田正之:「岩波FORTRAN辞典」、岩波書店、ISBN978-4000098816、(1986年12月8日)。※ Fortran77（まで）の規格を記述した辞典。
  - [森正武](https://ja.wikipedia.org/wiki/森正武 "wikilink")：「FORTRAN77数値計算プログラミング」増補版、[岩波書店](../Page/岩波書店.md "wikilink")、（1987年）。
  - 秋冨勝：「学生のためのFORTRAN―JIS上位水準による」、東京電機大学出版局、ISBN978-4501515300、 (1990年4月1日)。
  - M. Metcalf, J. Reid: bit 別冊「詳解Fortran90」、共立出版（1993年12月1日）。※ 原著は "Fortran 90 Explained"、Oxford Univ. Press(1990年)。
  - Walter S. Brainerd, Charles H. Goldberg, Jeanne C. Adams: "Programmer's guide to Fortran 90"(3rd Ed.)、Springer、(1996年)。
  - 竹澤照：「Fortran II 数値計算」、共立出版、ISBN 4-320-02868-6、（1997年5月10日）。
  - 新井親夫：「Fortran90入門－基礎から再帰手続きまで－」、森北出版、ISBN978-4627839816、 (1998年9月1日)。
  - 冨田博之､齋藤泰洋：「Fortran90/95プログラミング」､培風館 (1999年2月26日)｡ ※ 2011年4月に改訂新版が出ている。
  - 竹澤照：「Forran III データ構造とアルゴリズム」、共立出版、ISBN 4-320-02937-2、 (1999年7月10日)。
  - Ed Akin: "Object-Oriented Programming via Fortran 90/95"、Cambridge Univ Press、ISBN 978-0-521-52408-7、(2003年1月13日)。
  - 牛島省：『数値計算のためのFortran 90/95プログラミング入門』[森北出版](../Page/森北出版.md "wikilink")、ISBN 978-4-627-84721-7、(2007年)。※ 第2版が2020年1月に出版。
  - 竹澤照：「Fortran I 基礎」（第2版）、共立出版、ISBN 4-320-02977-1、（2000年8月20日）※ 初版は（1995年4月25日）。
  - Walter S. Brainerd: "Guide to Fortran 2003 Programming"、Springer、ISBN 978-1-84882-542-0、(2009年)。
  - Jeanne C. Adams, Walter S. Brainerd, Richard A. Hendrickson, Richard E. Maine, Jeanne T. Martin, Brian T. Smith: "The Fortran 2003 Handbook - The Complete Syntax, Features and Procedures"、Springer、ISBN 978-1-84628-378-9、(2009年)。
  - 冨田博之, 齋藤泰洋:「Fortran90/95プログラミング」改訂新版、培風館、ISBN978-4-563-01587-9、(2011年4月1日)。
  - Michael Metcalf, John Reid, Malcolm Cohen: "Modern Fortran Explained" (Numerical Mathematics and Scientific Computation) (4th Ed.)、Oxford Univ Press、ISBN978-0199601417、(2011年5月19日）。
  - Norman S. Clerman, Walter Spector: "Modern Fortran: Style and Usage"、Cambridge University Press、ISBN978-0-521-51453-8、(2012年2月23日)。
  - 安田清和, 水野正隆, 小野 英樹:「Fortran90/95による実践プログラミング」、大阪大学出版会、ISBN978-4872594737、（2014年3月28日）。
  - 田口俊弘：「Fortran ハンドブック」、技術評論社、ISBN978-4774175065、(2015年7月10日)。
  - Walter S. Brainerd: "Guide to Fortran 2008 Programming"(2nd Ed.)、Springer、ISBN978-1447167587、(2015年9月25日)。
  - 日向俊二:「Fortran 2008入門」、カットシステム、ISBN978-4-87783-399-2、(2016年4月）。
  - Michael Metcalf, John Reid, Malcolm Cohen: "Modern Fortran Explained: Incorporating Fortran 2018" (5th Ed.)、Oxford Univ. Press、ISBN978-0198811886、(2018年11月6日）。
  - Mark Jones Lorenzo: "Abstracting Away the Machine: The History of the FORTRAN Programming Language (FORmula TRANslation)"、Independently published、ISBN978-1082395949、(2019年8月22日)。
  - 牛島省：「数値計算のためのFortran90/95プログラミング入門(第2版)」、森北出版、ISBN 978-4627847224 (2020年1月28日）。

## 関連項目

  - [FORTRAN 77の言語仕様](https://ja.wikipedia.org/wiki/FORTRAN_77の言語仕様 "wikilink")
  - [Fortranの言語仕様](https://ja.wikipedia.org/wiki/Fortranの言語仕様 "wikilink")-(Fortran 90以降の言語仕様)
  - [Co-array Fortran](https://ja.wikipedia.org/wiki/Co-array_Fortran "wikilink")
  - [High Performance Fortran](https://ja.wikipedia.org/wiki/High_Performance_Fortran "wikilink")

## 外部リンク

  - [Fortran Wiki](http://fortranwiki.org/fortran/show/HomePage)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:JIS](https://ja.wikipedia.org/wiki/Category:JIS "wikilink") [Category:FORTRAN](https://ja.wikipedia.org/wiki/Category:FORTRAN "wikilink")

1.  [陰山聡『Fortran90/95入門』、なぜFortran90/95か？](http://www.research.kobe-u.ac.jp/csi-viz/members/kageyama/lectures/H22_FY2010_former/ComputationalScience/2_1_f95a.html)
2.  [HPF推進協議会 (HPFPC)](http://www.hpfpc.org/)
3.  牛島省『数値計算のためのFortran 90/95プログラミング入門』森北出版、2007年、はじめに
4.  [History of FORTRAN and FORTRAN II — Software Preservation Group](http://www.softwarepreservation.org/projects/FORTRAN/index.html#By_FORTRAN_project_members)
5.  [Fortranの開発者ジョン・バッカスが死亡 - Gadgets - MSNBC.com](http://www.msnbc.msn.com/id/17704662/)
6.
7.  [Fortran Working Group (WG5)](http://www.nag.co.uk/sc22wg5/).It may also be downloaded as a [PDF file](ftp://ftp.nag.co.uk/sc22wg5/N1551-N1600/N1579.pdf) or [`gzip`ped PostScript file](ftp://ftp.nag.co.uk/sc22wg5/N1551-N1600/N1579.ps.gz), FTP.nag.co.uk
8.  N1836, Summary of Voting/Table of Replies on ISO/IEC FDIS 1539-1, Information technology - Programming languages - Fortran - Part 1: Base language
9.  N1830, Information technology, Programming languages, Fortran, Part 1: Base language
10. ISO page to [ISO/IEC DTS 29113, Further Interoperability of Fortran with C](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=45136)
11. Draft of the Technical Specification (TS) 29113
12.
13.
14.
15.
16.
17.
18.
19. [Fortran 2018 Interpretation Document](http://j3-fortran.org/doc/year/18/18-007r1.pdf), 9 October 2018
20.
21.
22.
23.
24.
25. [F Programming Language Homepage](http://www.fortran.com/F/index.html)