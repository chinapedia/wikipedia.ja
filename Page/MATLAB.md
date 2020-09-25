> この記事は[MATLAB](https://ja.wikipedia.org/wiki/MATLAB)から翻訳されています。


**MATLAB**（マトラボ）は、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の[MathWorks](https://ja.wikipedia.org/wiki/MathWorks "wikilink")社が開発している[数値解析ソフトウェア](https://ja.wikipedia.org/wiki/数値解析ソフトウェア "wikilink")であり、その中で使う[プログラミング言語](../Page/プログラミング言語.md "wikilink")の名称でもある。MATLABは、[数値線形代数](https://ja.wikipedia.org/wiki/数値線形代数 "wikilink")、関数とデータの可視化、[アルゴリズム](../Page/アルゴリズム.md "wikilink")開発、グラフィカルインターフェイスや、他言語([C言語](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")/[Java](https://ja.wikipedia.org/wiki/Java "wikilink")/[Python](../Page/Python.md "wikilink"))とのインターフェイスの機能を有している。MATLABは、主に、数値計算を扱う事ができるが、追加のオプション[Symbolic Math Toolbox](http://jp.mathworks.com/products/symbolic/)を使うことで、数式処理の能力を得ることができる。2019年時点でMATLABのユーザー数は400万人を超えており、100,000 以上の企業・政府・大学で、工学・理学・経済学など幅広い分野に利用されている。

## 概要

MATLABは、**MAT**rix **LAB**oratoryを略したものであり、[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")計算、[ベクトル演算](https://ja.wikipedia.org/wiki/ベクトル演算 "wikilink")、[グラフ化や](../Page/グラフ_\(関数\).md "wikilink")3次元表示などの豊富な[ライブラリ](../Page/ライブラリ.md "wikilink")を持った、インタプリタ形式の高性能なテクニカルコンピューティング言語、環境としての機能を持つ。標準で数多くのライブラリを有しているが、それ以上のデータ解析や統計、アプリケーション展開などが必要な場合には**Toolbox**と呼ばれる拡張パッケージをインストールすることで、MATLABの機能拡張を図ることができる。MATLABとToolboxは総合して**MATLABプロダクトファミリ**と呼ばれる。

MATLABを用いると、[C言語](../Page/C言語.md "wikilink")や[FORTRAN](../Page/FORTRAN.md "wikilink")といった従来のプログラミング言語よりも短時間で簡単に科学技術計算を行うことができる。類似フリーウェアに[Scilab](../Page/Scilab.md "wikilink")、[GNU Octave](../Page/GNU_Octave.md "wikilink")、[FreeMat](https://ja.wikipedia.org/wiki/FreeMat "wikilink")などがある。

また、[iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")、[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink") ([iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink"))、[Androidで動作するアプリ](../Page/Android_\(オペレーティングシステム\).md "wikilink")[「MATLAB Mobile」](http://jp.mathworks.com/products/matlab-mobile/)がある。\[1\]Webブラウザで動作する\[<http://jp.mathworks.com/products/matlab-online/>　「MATLAB Online」\]も提供されている。

MATLABで使われるデータ型には数値型や文字列型、時刻・日付、構造体、cell配列、テーブル、カテゴリカル配列などがある。数値型はint64型、single型、double型などに、 文字列型はchar型やstring型にそれぞれ細分化される \[2\]。

## 歴史

"MATrix LABoratory"の略であるMATLABは、1970年代後半、後に[ニューメキシコ大学](https://ja.wikipedia.org/wiki/ニューメキシコ大学 "wikilink")コンピュータ科学学科長となる[クリーブ・モラー](https://ja.wikipedia.org/wiki/クリーブ・モラー "wikilink")によって開発された。彼は、学生が[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")を学ぶことなく[LINPACK](../Page/LINPACK.md "wikilink")や[EISPACK](https://ja.wikipedia.org/wiki/EISPACK "wikilink")にアクセスできるようにこのソフトを設計した。これはすぐに他の大学に広まってゆき、[応用数学](../Page/応用数学.md "wikilink")コミュニティの間で話題となった。エンジニアであるが1983年にモラーを訪ねた際に、これを見せられてその商用的可能性に気づいた。彼らはMATLABを[C言語](../Page/C言語.md "wikilink")で書き直し、開発を継続させるために[MathWorks](https://ja.wikipedia.org/wiki/MathWorks "wikilink")社を[1984年](../Page/1984年.md "wikilink")に設立した。これらの書き直されたライブラリは愛情を込めてJACKPACとして知られていた。MATLABは初めLittleの専門分野である制御工学で採用されたが、すぐに他の分野へと広まっていった。現在では、教育にも使用され、特に[線形代数](https://ja.wikipedia.org/wiki/線形代数 "wikilink")・[数値線形代数](https://ja.wikipedia.org/wiki/数値線形代数 "wikilink")や[数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")の講義に使用される。

MATLAB R2008a より、[インストール](../Page/インストール.md "wikilink")の際に、[インターネット](../Page/インターネット.md "wikilink")を通じた[ライセンス認証](https://ja.wikipedia.org/wiki/ライセンス認証 "wikilink")を導入した。

### 日本での展開

[1988年](../Page/1988年.md "wikilink")より、日本での販売展開は[サイバネットシステム](https://ja.wikipedia.org/wiki/サイバネットシステム "wikilink")株式会社が代理店業務を行っていた。しかし、2009年7月1日から販売代理店業務がMathWorks Japan(MathWorks社の日本法人)に移管された。

毎年11月から12月にサイバネットシステムが「MATLAB EXPO」を開催していたが、上記の移管により、2009年からはMathWorks Japanがその開催を主催する。近年では会場として[東京都](../Page/東京都.md "wikilink")[港区](https://ja.wikipedia.org/wiki/港区_\(東京都\) "wikilink")[台場地区の](../Page/お台場.md "wikilink")[ホテル グランパシフィック LE DAIBAにて開催されている](https://ja.wikipedia.org/wiki/ホテル_グランパシフィック_LE_DAIBA "wikilink")。その規模はMATLABユーザカンファレンスとしては世界最大の規模を誇り、一日の来場者は2000人を超える。単一ツールとしてのカンファレンスとしても他に類を見ないほどの規模である。

### バージョン

R2006a以降、MathWorks社は、MATLABプロダクトファミリーのリリースを3月と9月の年2回定期的に行っている（2015年現在）。バージョン名の付け方は、3月もしくは4月のリリースは"西暦"+"a"、9月もしくは10月のリリースは"西暦"+"b"である\[3\]。

自分が使用しているMATLABプロダクトファミリーのバージョンを確かめる場合、コマンドウィンドウ上で「verコマンド」を使用すればよい。これによって、現在使用しているMATLABプロダクトファミリーのバージョン、ライセンスナンバー、簡単なパソコンの状況、インストールされているTooloxとBlocksetおよび[Simulink](../Page/Simulink.md "wikilink")の一覧とバージョンが表示される。

| リリース名    | MATLAB本体 | Simulink, Stateflow | 年    |
| -------- | -------- | ------------------- | ---- |
| Volume 8 | 5.0      |                     | 1996 |
| Volume 9 | 5.1      |                     | 1997 |
| R9.1     | 5.1.1    |                     | 1997 |
| R10      | 5.2      |                     | 1998 |
| R10.1    | 5.2.1    |                     | 1998 |
| R11      | 5.3      |                     | 1999 |
| R11.1    | 5.3.1    |                     | 1999 |
| R12      | 6.0      |                     | 2000 |
| R12.1    | 6.1      |                     | 2001 |
| R13      | 6.5      |                     | 2002 |
| R13SP1   | 6.5.1    |                     | 2003 |
| R13SP2   | 6.5.2    |                     |      |
| R14      | 7        | 6.0                 | 2004 |
| R14SP1   | 7.0.1    | 6.1                 |      |
| R14SP2   | 7.0.4    | 6.2                 | 2005 |
| R14SP3   | 7.1      | 6.3                 |      |
| R2006a   | 7.2      | 6.4                 | 2006 |
| R2006b   | 7.3      | 6.5                 |      |
| R2007a   | 7.4      | 6.6                 | 2007 |
| R2007b   | 7.5      | 7.0                 |      |
| R2008a   | 7.6      | 7.1                 | 2008 |
| R2008b   | 7.7      | 7.2                 |      |
| R2009a   | 7.8      | 7.3                 | 2009 |
| R2009b   | 7.9      | 7.4                 |      |
| R2010a   | 7.10     | 7.5                 | 2010 |
| R2010b   | 7.11     | 7.6                 |      |
| R2011a   | 7.12     | 7.7                 | 2011 |
| R2011b   | 7.13     | 7.8                 |      |
| R2012a   | 7.14     | 7.9                 | 2012 |
| R2012b   | 8.0      | 8.0                 |      |
| R2013a   | 8.1      | 8.1                 | 2013 |
| R2013b   | 8.2      | 8.2                 |      |
| R2014a   | 8.3      | 8.3                 | 2014 |
| R2014b   | 8.4      | 8.4                 |      |
| R2015a   | 8.5      | 8.5                 | 2015 |
| R2015b   | 8.6      | 8.6                 |      |
| R2016a   | 9.0      | 8.7                 | 2016 |
| R2016b   | 9.1      | 8.8                 |      |
| R2017a   | 9.2      | 8.9                 | 2017 |
| R2017b   | 9.3      | 9.0                 |      |
| R2018a   | 9.4      |                     | 2018 |
| R2018b   | 9.5      |                     |      |
| R2019a   | 9.6      |                     | 2019 |
| R2019b   | 9.7      |                     |      |
| R2020a   | 9.8      |                     | 2020 |

**MATLABプロダクトファミリー バージョン**

## 構文

MATLABのMコード（もしくは単に*m*）は主に値指向である。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や[C++](../Page/C++.md "wikilink")といった静的型付けされる言語とは異なり、[PHPや](../Page/PHP_\(プログラミング言語\).md "wikilink")[JavaScript](../Page/JavaScript.md "wikilink")と同様に変数自体は型を持たず、実行時に代入される値のみが型を持つ。

### 変数

変数は代入演算子 '='で定義される。例として、

``` matlab
x = 17
```

はxという名の変数を定義すると同時に、その値に17という定数を代入した。型宣言はしていないが[double型として扱われる](https://ja.wikipedia.org/wiki/倍精度 "wikilink")。この例のような即値（数字で決め打ちされた定数）のほか、文字列定数、他の変数の値、または関数の出力を代入することができる。

### ベクトル/行列

MATLABは "Matrix Laboratory"であるので、様々な次元の配列を作成するための多くの便利な方法を用意している。他のプログラミング言語では一次元の行列（1×*N* or *N*×1）を一般的に「配列」として表現し、*N*×*M*、*N*×*M*×*L*（*N*、*M*、*L*は1より大きい）のような多次元行列は「配列の配列」、「配列の配列の配列」として扱うが、MATLABでは区別なく「多次元配列」として表現するため、前者を特に「ベクトル」と呼び分けている（[Pascal](../Page/Pascal.md "wikilink")や[Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")のように、多次元配列的表記をサポートする汎用言語もある）。

MATLABには簡単な配列を定義する単純な構文がある。*始端*`:`*増加値*`:`*終端*がそれである。例えば、

``` matlab
 array = 1:2:9

 array =
 1 3 5 7 9
```

は`array`という名の変数を定義し、これは1、3、5、7、9という数値からなる配列である。すなわち、配列は1（*始端*値）から始まり、それぞれの値は1つ前の値より2（*増加*値）増加し、9（*終端*値）以下に到達した時点で終了する。次の例のような代入文により、既に存在する変数`array`の値を変更できる。要素数（配列のサイズ）も変更される。

``` matlab
 array = 1:3:9

 array =
 1 4 7
```

*増加*値に1を使用する場合は、構文から（コロン1つとともに）省略することが出来る。

``` matlab
 ari = 1:5

 ari =
 1 2 3 4 5
```

これは1、2、3、4、5という数値からなる配列である変数`ari`を定義する。これは、増加値に初期値である1が使用されたためである。

### セミコロン

セミコロン（';'）はJavaやC++などとは違い、コマンドの終わりは改行するだけでよく、セミコロンをつける必要は**無い**。その代わり、セミコロンをつけると各行からの出力を抑えることが出来る。セミコロンを行末につけなければ、標準出力に実行結果が表示される。実行結果の表示の必要な複数のコマンドを、改行せずに表現する場合はカンマ（','）を使用する。

逆に、一つのコマンドを複数行にまたがって記述する場合は、次の行へ続くことを意味する（'...'）を行末に付ける必要がある。

### オブジェクト指向プログラミング

MATLABは、オブジェクト指向プログラミングをサポートしている。しかし、シンタックスと呼出規約が他言語と大きく異なる。MATLABは、値参照と、参照クラスを用意しています。 メソッドを呼ぶ方法の一例です。

``` matlab
object.method();
```

object がクラスのインスタンスであれば、object　のメンバーを選択することで、メソッドを呼ぶことができます。

``` matlab
classdef hello
    methods
        function greet(this)
            disp('Hello!')
        end
    end
end
```

hello.m 名のファイルを配置した後、次のコマンドを実行します。

``` matlab
>> x = hello;
>> x.greet();
Hello!
```

## コード例

*magic.m*から引用した以下のコードは奇数値*n*の[魔方陣](../Page/魔方陣.md "wikilink")*M*を作成する。

``` matlab
 [J,I] = meshgrid(1:n);
 A = mod(I+J-(n+3)/2,n);
 B = mod(I+2*J-2,n);
 M = n*A + B + 1;
```

このコードは"for"ループを使用することなくベクトルや行列の操作を行っているということに注意するべきである。慣用的に、MATLAB言語はふつう配列全体を同時に処理する。上記MESHGRIDユーティリティ機能は以下のような配列を作成する。

``` matlab
J =

     1     2     3
     1     2     3
     1     2     3

I =

     1     1     1
     2     2     2
     3     3     3
```

多くの[スカラー](https://ja.wikipedia.org/wiki/スカラー "wikilink")関数は配列に使用することができ、配列の要素毎に並行して作用する。そのため、mod(2\*J,n)は、配列 J に2をスカラー的に乗算（各要素を2倍）した後、要素毎に *n*の剰余を計算する。

MATLABには標準的な"for"や"while"が実装されているが、MATLABのベクトル式記法を使用する方がしばしばコードの可読性をあげ実行速度を速くする。

## 脚注

## 関連項目

  - [数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")
      - [数値線形代数](https://ja.wikipedia.org/wiki/数値線形代数 "wikilink")
      - [数値解析ソフトウェア](https://ja.wikipedia.org/wiki/数値解析ソフトウェア "wikilink")
      - [数値解析ソフトの比較](https://ja.wikipedia.org/wiki/数値解析ソフトの比較 "wikilink")
      - [数値解析の項目一覧](https://ja.wikipedia.org/wiki/数値解析の項目一覧 "wikilink")
  - Toolboxesとその他のアドオン
      - [Simulink](../Page/Simulink.md "wikilink")
      - [Psychtoolbox](../Page/Psychtoolbox.md "wikilink")
      - [NAG](https://ja.wikipedia.org/wiki/NAG "wikilink")
  - [NVIDIA](../Page/NVIDIA.md "wikilink")
      - [CUDA](../Page/CUDA.md "wikilink") - R2010bより、オプション製品 Parallel Computing Toolbox が直接サポートを提供している。
      - [NVIDIA Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink")
  - 類似のソフトウェア
      - [FreeMat](https://ja.wikipedia.org/wiki/FreeMat "wikilink")
      - [GNU Octave](../Page/GNU_Octave.md "wikilink")
      - [Scilab](../Page/Scilab.md "wikilink")
      - [Julia](https://ja.wikipedia.org/wiki/Julia_\(プログラミング言語\) "wikilink")
  - [INTLAB](https://ja.wikipedia.org/wiki/INTLAB "wikilink") (Matlabで開発された[区間演算](https://ja.wikipedia.org/wiki/区間演算 "wikilink")ライブラリ)

## 参考文献

### 和書

  - [大石進一](https://ja.wikipedia.org/wiki/大石進一 "wikilink")、MATLABによる数値計算、[培風館](../Page/培風館.md "wikilink")、2001年。
  - 桜井鉄也. (2003). MATLAB/[Scilab](../Page/Scilab.md "wikilink") で理解する数値計算. [東京大学出版会](../Page/東京大学出版会.md "wikilink").

### 洋書

  - Gander, W., & Hrebicek, J. (Eds.). (2011). Solving problems in scientific computing using Maple and Matlab®. [:en:Springer Science & Business Media](https://ja.wikipedia.org/wiki/:en:Springer_Science_&_Business_Media "wikilink").
  - Quarteroni, A., Saleri, F., & Gervasio, P. (2006). Scientific computing with MATLAB and Octave. Berlin: Springer.
  - Wallisch, P., Lusignan, M. E., Benayoun, M. D., Baker, T. I., Dickey, A. S., & Hatsopoulos, N. G. (2014). MATLAB for neuroscientists: an introduction to scientific computing in MATLAB. [:en:Academic Press](https://ja.wikipedia.org/wiki/:en:Academic_Press "wikilink").
  - Gander, W., Gander, M. J., & Kwok, F. (2014). Scientific computing-An introduction using Maple and MATLAB. [:en:Springer Science & Business Media](https://ja.wikipedia.org/wiki/:en:Springer_Science_&_Business_Media "wikilink").
  - Linz, P., & Wang, R. (2003). Exploring numerical methods: An introduction to scientific computing using MATLAB. Jones & Bartlett Learning.

## 外部リンク

  - [MathWorks社の日本語MATLAB製品ページ](http://www.mathworks.co.jp/products/matlab/)
  - [MATLABのオブジェクト指向プログラミング](http://www.mathworks.co.jp/products/matlab/object_oriented_programming.html)
  - [MATLAB & Simulink Student Version (日本語版) 製品ページ](http://www.mathworks.co.jp/academia/student_version/)
  - [MATLAB Central（MATLABユーザコミュニティ）](http://www.mathworks.co.jp/matlabcentral/)
  - [MathWorks社の日本語技術資料ライブラリ](http://www.mathworks.co.jp/programs/techkits/technical_literature_conf.html)
  - [MathWorks社の日本語マニュアル](http://www.mathworks.co.jp/access/helpdesk_ja_JP/help/helpdesk.html)
  - [MathWorks社の日本語マニュアルのアーカイブ](http://www.mathworks.co.jp/access/helpdesk_archive_ja_JP/japanDocArchives.html)
  - [MATLAB/Simulink関連日本語書籍一覧](http://www.mathworks.co.jp/support/books/)
  - [MathWorks社の日本語サポートページ (日本語技術ヘルプは「リソースを探す\>製品を選ぶ」)](http://www.mathworks.co.jp/support/)
  - [MathWorks社の日本語アクティベーション、インストール、およびスタートアップのトラブルシューティング](http://www.mathworks.co.jp/support/install.html)
  - [Open Directory ProjectのMATLABカテゴリ](http://dmoz.org/Science/Math/Software/MATLAB/)
  - [Cleve Molerによって書かれた、MATLABの歴史に関する追加の情報](http://www.mathworks.com/company/newsletters/news_notes/clevescorner/)
  - [MATLAB EXPO JAPAN](http://www.matlabexpo.com/jp/)
  - [comp.soft-sys.matlab](news://comp.soft-sys.matlab)
  - [literateprograms.orgのMATLAB](http://en.literateprograms.org/Category:Programming_language:Matlab)
  - [Freematを使おう！](https://sites.google.com/site/freematjapan/)

[Category:数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:数値解析ソフトウェア "wikilink") [Category:Linux向け数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:Linux向け数値解析ソフトウェア "wikilink") [Category:Linux向け数式処理システム](https://ja.wikipedia.org/wiki/Category:Linux向け数式処理システム "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:iOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:iOSのソフトウェア "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  。
2.  シングルクオテーションで囲まれた単語はchar型に、ダブルクオテーションで囲まれた単語はstringとなる。ダブルクオテーションの使用はR2017aから導入された。
3.  [MathWorks 製品リリース スケジュール](http://www.mathworks.co.jp/products/new_products/release_model.html)