> この記事は[COBOL](https://ja.wikipedia.org/wiki/COBOL)から翻訳されています。


**COBOL**（**コボル**）は、1959年に事務処理用に開発された[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。名前は「」（共通事務処理用言語）に由来する。

## 概要

非[理系](../Page/理系.md "wikilink")の事務員や官吏でもプログラミングできる言語として設計されたため、[自然言語](../Page/自然言語.md "wikilink")である[英語](../Page/英語.md "wikilink")に近い記述をめざしたコマンド語彙や構文（シンタックス）が採用されている。特に金額計算など事務処理用に広く使われている。COBOLは自然言語（英語）に近い構文を持つため、そのソースコードは記述が冗長にはなるが、[可読性が高い](https://ja.wikipedia.org/wiki/可読性#プログラミング "wikilink")。本のように、部、節、段落、文という階層で記述される。人によっては関数や数式だらけの言語よりもハードルが低い。[リフレクションができないなど](../Page/リフレクション_\(情報工学\).md "wikilink")、モダンなプログラミング言語に比べて論理制御機能は貧弱である。一方、文字列解析や文字列編集、帳票、画面編集などの事務処理機能は豊富である。

COBOLは仕様の古い言語である。ただ、言語規格は拡張が続けられていて、2002年版以降では[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")にも対応して部品性を向上した。現実のプロジェクトで制約となるのは、COBOLの言語機能の不足よりは、稼働プラットフォーム、業務運用あるいは保守体制である場合も多い。

COBOLは、科学技術計算向けの[FORTRAN](../Page/FORTRAN.md "wikilink")に次いで国際的な標準化が行われた、初期のプログラミング言語である。過去のバージョンとの互換性を重視した国際標準規格にしたがって多くのプラットフォームでコンパイラが開発されてきたので、COBOL to COBOLの[マイグレーション](https://ja.wikipedia.org/wiki/マイグレーション "wikilink")（プラットフォームの更新）は比較的容易である。

膨大なCOBOLプログラムおよびそれらの処理するデータが、企業や政府機関に長年開発し続けられ稼働している。[ガートナー](../Page/ガートナー.md "wikilink")発という情報によれば、メインフレームが世界1万サイト以上あって3万8千の[レガシー](../Page/レガシー.md "wikilink")システムがあり、COBOLは全プログラム約3,100億行のうちの約65%の約2,000億行あって、毎年約50億行が増えているという \[1\] \[2\] \[3\]。これは[FORTRAN](../Page/FORTRAN.md "wikilink")と[アセンブラを合わせた資産の数十億行に比べて圧倒的に多い](../Page/アセンブリ言語.md "wikilink")。また、世界の商用データの約75%、商用トランザクションの80%以上（Google検索の200倍以上）である。COBOL開発者は85万人以上いるが、COBOL開発者の増加より減少がずっと速いという。

日本国内では、2004-2009年のプロジェクトデータ2,417件をまとめた[IPAのレポートによると](../Page/情報処理推進機構.md "wikilink")、1位の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")（25.4%）に次いでCOBOLは16.8%で2位\[4\]である。

このように、誕生から半世紀たってもなお主流言語のひとつの座を占めている点で、他の初期の言語を引き離している。

## 誕生経緯

[1950年代](../Page/1950年代.md "wikilink")、事務処理言語は開発メーカーごとに異なっていた。その統一の必要性を認識していた[アメリカ国防総省](../Page/アメリカ国防総省.md "wikilink")によって、事務処理用の共通言語の開発が提案され、[CODASYL](../Page/CODASYL.md "wikilink")（Conference on Data Systems Languages、データシステムズ言語協議会）が設立された。そうした背景の下、[1959年](../Page/1959年.md "wikilink")にCODASYLによって開発された共通事務処理用言語がCOBOLである。

その後、1960年1月に[CODASYL](../Page/CODASYL.md "wikilink")執行委員会によって最初の仕様書が承認され、[合衆国政府印刷局](https://ja.wikipedia.org/wiki/合衆国政府印刷局 "wikilink")に送られた。この最初の仕様書は1960年4月に発行され、通称COBOL-60と呼ばれている\[5\] \[6\]。

COBOLの開発により、アメリカ政府の事務処理システムは全てCOBOLのみで納品されることとなった。これに伴い、COBOLは事務処理用言語として世界中に普及することになる。

## 現状

[C言語](../Page/C言語.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などの登場後も、COBOLは主に商用計算記述用として、主に金融業界や行政サービスなどで広く使用されている\[7\]。

COBOL言語規格は、ローカル変数が作りにくく論理制御機能面が弱かった古典的言語からの脱皮を図っている。オブジェクト指向を採用し、入れ子プログラムを可能としたうえ、COBOLからCOBOLクラスライブラリのみならずJavaのクラスライブラリも呼べるようにするなど、相互運用性や共同開発容易性、安全性を改善してきている。

2019年現在、COBOL Cowboys社の調査では2000億行のCOBOLプログラムが現役で、[フォーチュン500](../Page/フォーチュン500.md "wikilink")企業の90%がCOBOLプログラムを使い続けている\[8\]。また[マイクロフォーカス](https://ja.wikipedia.org/wiki/マイクロフォーカス "wikilink")社のDerek Britton氏は「COBOLシステムを運用している組織が万単位で存在」「この言語が世界のトランザクション処理システムのうちの70％で用いられている」と述べた\[9\]。

## COBOLのエピソード

  - COBOLもモダン化を図っているが、COBOL技術者が**コボラー**と呼ばれるとき、モダンでないプログラミング言語を扱っていることを揶揄するニュアンスを伴っていることがある。
  - 「COBOLの冗長さ」は、時折[ハッカー](../Page/ハッカー.md "wikilink")ジョークのネタにされる。例えばCOBOLのオブジェクト指向拡張案「ADD 1 TO COBOL GIVING COBOL」（[C++](../Page/C++.md "wikilink")のもじり）などである。
  - [構造化プログラミング](../Page/構造化プログラミング.md "wikilink")を提唱した計算機科学者[エドガー・ダイクストラ](../Page/エドガー・ダイクストラ.md "wikilink")は、各種言語の欠点を挙げた中でCOBOLについて「COBOLを使っていると人は無能になってしまう。COBOLの教育は犯罪とみなすべきである。」と述べた\[10\]。これが書かれたのは、企業ではCOBOLで新人教育がされ、[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")も知らずにGO TO文だらけの巨大な[スパゲティプログラム](../Page/スパゲティプログラム.md "wikilink")を普通に書いていてレビューと障害修正が大変だった1975年である。
  - [2009年](../Page/2009年.md "wikilink")9月18日は「COBOL誕生50周年」とされ、[マイクロフォーカス](https://ja.wikipedia.org/wiki/マイクロフォーカス "wikilink")が50周年を祝うサイトを立ち上げた。これはCOBOLという名称が決定された1959年9月18日を、COBOLの誕生日としたものである\[11\]。また、国内主要COBOL[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")が設立した[非営利団体](../Page/非営利団体.md "wikilink")である[COBOLコンソーシアム](https://ja.wikipedia.org/wiki/COBOLコンソーシアム "wikilink")\[12\]は、最初の公的な仕様書であるCOBOL-60が発行された1960年4月をCOBOL誕生年月とし、2010年4月16日にCOBOL誕生50周年記念セミナーを行っている\[13\]。
  - [2009年](../Page/2009年.md "wikilink")11月、マイクロフォーカスのスチュアート・マギルは、「稼動中のCOBOLプログラムは全世界で2,400億行で、年間30億行が追加されている。全世界のCOBOLプログラマは200万人。[フォーチュン500](../Page/フォーチュン500.md "wikilink")の90%の企業はCOBOLプログラムを使用中。」との趣旨の発言をした\[14\]。
  - [日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の[国家資格](https://ja.wikipedia.org/wiki/国家資格 "wikilink")である[基本情報技術者試験](../Page/基本情報技術者試験.md "wikilink")（2000年度までは第二種情報処理技術者試験と呼ばれていた）の午後試験では2019年度まではCOBOLに関する内容が出題されていた（ただし自由選択制であり必須問題ではない）が、2020年度試験より廃止となる。代わりに[Python](../Page/Python.md "wikilink")が追加される予定。

## COBOLの言語仕様

年齢を表すageという変数の値を、一定の年数を表すyearsという変数の値の分だけ増やす手続きは、例えば普通のプログラミング言語では

  -

    ``` c
    age = age + years;
    ```

    （[C言語](../Page/C言語.md "wikilink")などでは

    ``` c
    age += years;
    ```

    のように略記できる）

と書かれる。COBOLでも同様にCOMPUTE文によって

  -

    ``` cobolfree
    COMPUTE AGE = AGE + YEARS.
    ```

と記述することもできるが、

  -

    ``` cobolfree
    ADD YEARS TO AGE.
    ```

    （英語でそのまま「年数を年齢に加える」）

という表現も可能である。

このように、数学やアルゴリズムの知識を豊富にもっていなくても、全て現在形、語尾変化なし、など、構文上の約束事さえ覚えて、英語による理路整然とした記述ができれば、COBOLのプログラムを書けるように考えられている。つまり事務処理の手順を逐一細かく英語で書き下せば事務処理が電算化できるということである。さらにプログラムのコードそのものがプログラムの機能を説明する仕組みになっているので、そのまま読み下したときに分かりやすい。

こういった特性を、まだ人工知能、自然言語処理の研究が浅い時期に追求してCOBOLを設計したのは、意義深く、産業的にも効果があった。ただ、ソフトウェアが大規模化し相互に絡み合うように接続されてきた現代、動詞や前置詞を明示するかどうかという命令記述の次元だけでは視点が不足である。モジュール性、処理の強力さを含めて可読性と保守性を総合評価しなおすと、場面によってはまたちがう結果も生じてくる。

自然言語指向な書き方が優れているといっても、複雜な数式、関数を扱う科学技術計算分野における制御・演算には向いていない。[二次方程式](../Page/二次方程式.md "wikilink") A X<sup>2</sup> + B X + C = 0 の解（の片方）を求める手続きは、COBOLでもCOMPUTE文を用いて簡潔に書こうとすれば、

  -

    ``` cobolfree
    COMPUTE X = (- B + (B ** 2 - 4 * A * C) ** 0.5) / (2 * A).
    ```

と一文で済む。ただし、数式を極力使わない書き方にこだわれば、

  -

    ``` cobolfree
    MULTIPLY B BY B GIVING B-SQUARED.
    ```

    （BをB倍し、B-SQUAREDに代入）

    ``` cobolfree
    MULTIPLY 4 BY A GIVING FOUR-A.
    ```

    （Aを4倍し、FOUR-Aに代入）

    ``` cobolfree
    MULTIPLY FOUR-A BY C GIVING FOUR-A-C.
    ```

    （CをFOUR-A倍し、FOUR-A-Cに代入）

    ``` cobolfree
    SUBTRACT FOUR-A-C FROM B-SQUARED GIVING D.
    ```

    （B-SQUAREDからFOUR-A-Cを引き、Dに代入）

    ``` cobolfree
    MOVE FUNCTION SQRT(D) TO ROOT-D.
    ```

    （Dの正の平方根を、ROOT-Dに代入）

    ``` cobolfree
    SUBTRACT B FROM ROOT-D GIVING NUMERATOR.
    ```

    （ROOT-DからBを引き、NUMERATORに代入）

    ``` cobolfree
    MULTIPLY 2 BY A GIVING TWO-A.
    ```

    （Aを2倍し、TWO-Aに代入）

    ``` cobolfree
    DIVIDE NUMERATOR BY TWO-A GIVING X.
    ```

    （NUMERATORをTWO-Aで割り、Xに代入）

と演算子1個あたり1文に膨れ上がって、見通しが明らかに悪くなる。もっとも、これほど複雑な式をこのように逐一書くプログラマはおよそ現代には存在しない。

COBOLでは同じ処理を書くのに、少なくとも「COMPUTE ～」と書く必要もあり、他節に述べるようにいろいろなDIVISIONの記述も必要となるなど、モダンな言語より長くなりがちである。また、パズルのように巧妙な制御機能がさほど多彩に備わっているわけではない。Eclipseなどの[統合開発環境](../Page/統合開発環境.md "wikilink")でCOBOLも使えるようになったが、Javaのような小粒度なモジュールに関してもインタフェースを明確に記述するスタイルの言語よりも、そこでされるサポートは少ない。

このようなことから、COBOLに習熟している人がモダンな言語でのプログラミング能力が高いとは限らない。それでも、世界的に蓄積され社会を動かしているCOBOL資産を保守・更新するという使命は重要である。他言語も習熟している技術者であっても、言語の欠点を多階層な共通モジュール作成やツール作成などでカバーしながら、社会基盤を支えるCOBOL関連プロジェクトで活動している。

## COBOLの文法の概要

主にANSI COBOL 1985の文法について述べる。

### 表記法

COBOLの文法は英語の表現に近い。たとえば、ある数値型変数W-NOに対し数値100、英字型変数W-CHARに文字列'ABC'を代入する場合は、以下のような表記をする。

  -

    ``` cobolfree
    MOVE 100 TO W-NO.
    ```

    （または

    ``` cobolfree
    COMPUTE W-NO = 100.
    ```

    ）

    ``` cobolfree
    MOVE 'ABC' TO W-CHAR.
    ```

このように、COBOLの文法は[自然言語](../Page/自然言語.md "wikilink")（英語）に類似した文章的なものであることから、その[可読性](https://ja.wikipedia.org/wiki/可読性 "wikilink")（ドキュメント性）の面で優れていると言われている。ただし、数学の定理を例にとれば、それを自然言語に直したところで理解が容易になるわけではないため、これは否定派にはCOBOLの冗長性と捉えられる部分でもある。

### プログラムの書式

典型的なCOBOLの原始（ソース）プログラムは、FORTRANと同様にカラム固定形式で記述する。

  - 1～6カラム目「一連番号」
    各行を識別するために、6桁のシーケンシャル番号を記述することができる。
  - 7カラム目「標識領域」
    その行の標識を記述する。例えば、アスタリスクを記述すると、その行は注記行となる。
  - 8～11カラム目「A領域」
    12～72カラム目「B領域」
    A領域およびB領域に、コードを記述する。ピリオドおよびその後に続くスペースを記述してコードの行末を示す。

最近のCOBOLコンパイラには、行の長さが固定である必要がなく、一連番号の不要な自由形式をサポートするものがある。

### COBOLプログラムの基本構造

COBOLのプログラムは、次の4つのDIVISIONをこの順番で記述するのが基本となっている。

  - IDENTIFICATION DIVISION……見出し部
  - ENVIRONMENT DIVISION……環境部
  - DATA DIVISION……データ部
  - PROCEDURE DIVISION……手続き部

#### IDENTIFICATION DIVISION

「PROGRAM-ID」（プログラム識別名）を記述する。

「AUTHOR」（作成者名）、「DATE-WRITTEN」（作成日）等の文法もあったが廃要素となった。

#### ENVIRONMENT DIVISION

プログラムが実行されるコンピュータの環境を記述する。「ENVIRONMENT DIVISION」は、「CONFIGURATION SECTION」（環境節）と「INPUT-OUTPUT SECTION」（I-O節）に大別される。

#### DATA DIVISION

プログラムで使用する変数及びデータ並びにその型について記述する。プログラムで使用する変数及びデータのすべては、DATA DIVISIONで定義しなければならない。

「DATA DIVISION」は、「FILE SECTION」と「WORKING-STORAGE SECTION」に大別される。データの型の宣言は、PICTURE(PIC)句によって行う。

呼ばれたプログラムが呼んだプログラムから引数でデータを受け取る場合は、それらの包含構造や基本項目の型を呼ばれたプログラムの「LINKAGE SECTION」で宣言する。

##### COBOLにおけるデータの分類

COBOLのデータは、次の3つに分類される。

  - 変数 (Variables)
  - 定数 (Literals)
  - 表意定数 (Figurative Constants) - あらかじめ名称が定められている特定の意味を持つ定数（表意定数）を利用できる。この定数の実体は、実行されるシステムよってその意味が有効になるように実現される。たとえば、HIGH-VALUES、LOW-VALUESがある。

##### COBOLの扱うデータの特徴とメンテナンス

COBOLの代表的な変数型（項類）に、次のものがある。

  - 数字項目 (numeric item) - 例：99999 または 9(5)
  - 英数字項目 (alphanumeric item) - 例：XXXXX または X(5)
  - 英字項目 (alphabetic item) - 例：AAAAA または A(5)
  - 数字編集項目 (numeric edited item) - 例：ZZZ,ZZ9
  - 英数字編集項目 (alphanumeric edited item) - 例：AXX/XX/XX

COBOLでは固定長のレコード（繰り返しデータ単位）の中に固定長でデータ項目を含むという使い方が多い。たとえば、

    00076543SHOUYURAMEN         20121013
    00076544SHIORAMEN           20111231

などである。データには包含関係の階層があり、領域再定義機能により同じメモリ領域を何通りかの構成で解釈できる。

他の多くの言語（VB、C、Javaなど）では、改行までが繰り返しデータ単位で、その中の項目は可変長でコンマやタブなどの区切り記号で区切るという使い方が多い。たとえば[CSV形式](../Page/Comma-Separated_Values.md "wikilink")

    76543,SHOUYURAMEN,20121013
    76544,SHIORAMEN,20111231

がある。最近のCOBOLコンパイラには、CSV形式の入出力をサポートするものもある。

COBOLでは基本項目を並べて集団項目を作る。レベル番号を用いて階層構造を作る。OCCURS句により多次元配列を作る。これらによる固定長や可変長の「[レコード](../Page/レコード.md "wikilink")」（C言語などの[構造体](../Page/構造体.md "wikilink")に相当）のレイアウトを定義する。なお、「レコード」という型はCOBOLによって初めて導入された概念である。

COBOLの階層的データの包含関係は、階層の深さを表すレベル番号"01"から"49"を各データ記述に付けることで記述される。

こうした階層や領域再定義などのデータ構造をもつファイルやレコードの定義と処理は、COBOLの得意とするところで、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")言語および従来のJavaのクラスライブラリによってはなかなかうまく再現できない。

COBOLでは、何百兆円という大きな金額の計算や、小数点以下何桁まで正確に複利計算をしても1円の誤差も出ない正確な小数計算が得意である。[固定小数点数](../Page/固定小数点数.md "wikilink")方式で整数とスケール（桁）を扱える数値項目は通常最大18桁（中間結果はそれ以上）あり、特に内部10進項目などの[2進化10進数](https://ja.wikipedia.org/wiki/2進化10進数 "wikilink")を用いれば、メモリを節約しつつ性能も確保できる。メインフレームではこれをサポートする専用のCPU命令まで設けられ、高速化が図られた。

このアプローチは、10進2進変換に伴う誤差が避けられない[浮動小数点数](../Page/浮動小数点数.md "wikilink")によって実数を近似値で表現しようとする他の言語の発想とは対照的である。[FORTRAN](../Page/FORTRAN.md "wikilink")には浮動小数点数はあっても内部10進項目などはなかった。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")では任意桁の整数、小数を扱えるBigInteger、BigDecimalというクラスが提供されているが、文字配列で処理しているために金額計算、利息計算をCOBOLほど少ないCPUステップでは行えていない。

COBOLでは無名の変数等として"FILLER"という名称を記述することができる。無名項目の"FILLER"は、COBOLにおける変数等の領域の定義は固定長となるため、そのような固定長領域内での予備的な領域の確保という意味合いも有している。たとえば

``` cobol
000100 01 PRODUCT-REC.
000200     03 PRODUCT-NO     PIC 9(8).
000300     03 ...
000400     03 PRODUCT-NAME   PIC X(20).
000500     03 FILLER         PIC X(500).
```

で予備項目500バイトを含む製品レコードPRODUCT-RECを定義して他のシステムとデータを交換しはじめる。年月が経ってこのレコードに追加項目AD-START-DATE（広告開始日）が発生したら、FILLERを削ってその新項目に宛てることで、授受データのレコード長を変更しなくて済む。

``` cobol
000100 01 PRODUCT-REC.
000200     03 PRODUCT-NO     PIC 9(8).
000300     03 ...
000400     03 PRODUCT-NAME   PIC X(20).
000500     03 AD-START-DATE  PIC 9(8).
000600     03 FILLER         PIC X(492).
```

FILLERによって、固定長レコードファイルの運用が円滑になった。ただ、この例で500バイトを使い切れば、やはりレコード長の変更が必要になる。だからといってむやみに長いFILLERを入れると、容量的な効率低下を招くのでバランスが必要である。

製品が多くなってPRODUCT-NO（製品番号）を8桁から12桁に拡張しようとすると、後続の項目群の開始番地が順繰りにずれてしまうので変更の影響が大きい。

COBOLが扱うデータベースの領域定義も、多くの場合同様に固定長の項目からなるレコードという考えで行われてきた。

システムが実際に入力したデータがプログラムが用意した桁数を1桁でも超えたとき、SIZE ERRORとしてエラー処理を行うのが普通である。オプションにより上を切り落として続行も可能。桁数が不足したときにデータのミスでなければ、プログラムとそのデータを授受するシステムのプログラムで一斉に桁数を増やす修正をしなければならない。データの変換も必要となる。

このように桁数やバイト数の変更は大変なため、COBOLプログラマやSEは常に桁数やバイト数の設定や変更を意識し、プログラムの使用されるのが何十年でもその間になるべく桁溢れが起こらないように目を配って作業している。

以上のような特徴は、固定長レコードやその中の文字列や数値を容易にかつ厳密に扱えるというCOBOLの大きな長所にともなう、保守、機能追加していく上での大きな短所である。

##### 補足

  - COBOLのデータ型の宣言で、COBOL85以前から可変長のデータ宣言も可能になっている。
  - COBOLの仕様拡張により、ポインタ操作も可能になっており、実装しているCOBOLコンパイラも複数、開発されている。
  - DBMSとの連携により、データベースを操作する場合、DBMS側でレコードの定義、ビューの定義などを行う。そのため、レコードのフィールド変更などがあっても、ビューなどで変更対象のフィールドを参照するアプリケーション以外は、修正や再コンパイルは必要ない。
  - RDBMSとの連携では、可変長データ、BLOBなど、多様なデータ型の扱いも可能となっている。ただし、COBOL側の受け渡しの変数の宣言は、COBOLコンパイラにより、COBOLの可変長データ型を使うものと、COBOLでは有効長を持つ固定長データ型を使うものなど、開発元による実装の違いがある。

#### PROCEDURE DIVISION

実行されるプログラムの内、実際の処理部分のコードを記述する。 引数を受け取る場合は、「PROCEDURE DIVISION USING 引数名 \[, 引数名……\]」という書き方をする。

上記3つのDIVISIONを記述したあとやっと「PROCEDURE DIVISION」で実行手順のコードを記述する文法であるため、COBOLは「前置きが長い」言語ともいえる。

[COBOLの予約語の数は膨大で](../Page/予約語_\(COBOL\).md "wikilink")、文字数の長いものが多い。

## コードの実例

### 実例1 ([Hello world](../Page/Hello_world.md "wikilink"))

``` cobol
000100 IDENTIFICATION DIVISION.
000200 PROGRAM-ID. HELLO.
000300 PROCEDURE DIVISION.
000400     DISPLAY 'HELLO, WORLD!'.
000500     STOP RUN.
```

出力

    HELLO, WORLD!

この例では DISPLAY命令を使って文字列をコンソールまたは標準出力に出力している。

COBOLはレコードレイアウトの決まったファイルの処理に使われることが多い。その場合はふつう、ファイル節（FILE SECTION）にレコードとそれを構成するデータ群の定義を書く。そして、実行部（PROCEDURE DIVISION）のREAD文、WRITE文などでそのレコードを読み書きする。

### 実例2 (Hello world)

作業領域節（WORKING-STORAGE SECTION）にデータを定義した例。

``` cobol
000100 IDENTIFICATION DIVISION.
000200 PROGRAM-ID. HELLO.
000300 DATA DIVISION.
000400 WORKING-STORAGE SECTION.
000500 01 HELLO1      PIC X(15).
000600 01 HELLO2.
000700     03 FILLER  PIC X(06) VALUE 'HELLO,'.
000800     03 FILLER  PIC X(01) VALUE SPACE.
000900     03 FILLER  PIC X(06) VALUE 'WORLD!'.
001000     03 FILLER  PIC X(01) VALUE SPACE.
001100     03 FILLER  PIC 9(01) VALUE 2.
001200 PROCEDURE DIVISION.
001300     MOVE 'HELLO, WORLD! 1' TO HELLO1.
001400     DISPLAY HELLO1.
001500     DISPLAY HELLO2.
001600     STOP RUN.
```

出力

    HELLO, WORLD! 1
    HELLO, WORLD! 2

### 実例3 ([Fizz Buzz](../Page/Fizz_Buzz.md "wikilink"))

``` cobol
000100 IDENTIFICATION DIVISION.
000200 PROGRAM-ID. FIZZBUZZ.
000300 DATA DIVISION.
000400 WORKING-STORAGE SECTION.
000500 01 I  PIC 9(3).
000600 PROCEDURE DIVISION.
000700     PERFORM VARYING I FROM 1 BY 1 UNTIL I > 100
000800       EVALUATE FUNCTION MOD(I 3) = ZERO
000900           ALSO FUNCTION MOD(I 5) = ZERO
001000       WHEN TRUE  ALSO TRUE
001100         DISPLAY 'FIZZBUZZ'
001200       WHEN TRUE  ALSO FALSE
001300         DISPLAY 'FIZZ'
001400       WHEN FALSE ALSO TRUE
001500         DISPLAY 'BUZZ'
001600       WHEN OTHER
001700         DISPLAY I(3 - FUNCTION INTEGER(FUNCTION LOG10(I)):)
001800       END-EVALUATE
001900     END-PERFORM.
002000     STOP RUN.
```

出力

    1
    2
    FIZZ
    4
    BUZZ
    FIZZ
    7
    8
    FIZZ
    BUZZ
    11
    　（中略）
    FIZZBUZZ
    91
    92
    FIZZ
    94
    BUZZ
    FIZZ
    97
    98
    FIZZ
    BUZZ

COBOLでは[剰余を求める際に](../Page/除法.md "wikilink")、[商](https://ja.wikipedia.org/wiki/商 "wikilink")・剰余それぞれを格納する変数を定義した上でDIVIDE文を用いることが多いが、商は不要で剰余のみが知りたい場合や、それを変数に格納しておく必要が無い場合は、組み込み関数の[MOD](https://ja.wikipedia.org/wiki/MOD "wikilink")を用いても良い。

また、COBOLの数字項目は定義された桁数よりも少ない桁数の値が格納された場合、[ゼロパディングした状態で扱うため](https://ja.wikipedia.org/wiki/ゼロサプレス "wikilink")、このまま表示させると001、002、…、098と先頭に0が補われて表示されてしまう。\(N\)桁で定義された数字項目に、正の整数\(n\)が格納された場合、その最上位桁の位置は左から\(N - \left \lfloor \log_{10} n \right \rfloor\)カラム目であるから、上記のように

``` cobolfree
DISPLAY I(3 - FUNCTION INTEGER(FUNCTION LOG10(I)):)
```

と記述することで、パディングされた0を除いた部分だけを表示させることが出来る。

なお、0、[負の数](https://ja.wikipedia.org/wiki/正の数と負の数 "wikilink")、[小数](../Page/小数.md "wikilink")を扱う場合は、下記のように数字編集項目による[ゼロサプレス](https://ja.wikipedia.org/wiki/ゼロサプレス "wikilink")とUNSTRING文を組み合わせることでパディングされた0を除いて表示させることが出来る。

``` cobol
000100 IDENTIFICATION DIVISION.
000200 PROGRAM-ID. FIZZBUZZ.
000300 DATA DIVISION.
000400 WORKING-STORAGE SECTION.
000500 01 I                                PIC S9(3).
000600 01 HENSHU-IKI                       PIC X(4).
000700 01 HENSHU-NUM REDEFINES HENSHU-IKI  PIC ---9.
000800 01 DUMMY-IKI                        PIC X(1).
000900 PROCEDURE DIVISION.
001000     PERFORM VARYING I FROM -100 BY 1 UNTIL I > 100
001100       EVALUATE FUNCTION MOD(I 3) = ZERO
001200           ALSO FUNCTION MOD(I 5) = ZERO
001300       WHEN TRUE  ALSO TRUE
001400         DISPLAY 'FIZZBUZZ'
001500       WHEN TRUE  ALSO FALSE
001600         DISPLAY 'FIZZ'
001700       WHEN FALSE ALSO TRUE
001800         DISPLAY 'BUZZ'
001900       WHEN OTHER
002000         COMPUTE HENSHU-NUM = I
002100         UNSTRING
002200           HENSHU-IKI DELIMITED BY ALL SPACE
002300           INTO DUMMY-IKI HENSHU-IKI
002400         END-UNSTRING
002500         DISPLAY HENSHU-IKI
002600       END-EVALUATE
002700     END-PERFORM.
002800     STOP RUN.
```

COBOLの数字編集項目によるゼロサプレスは、単純に0を空白に置き換えるだけであるから、先頭に空白が生じる（＝整数部分が右寄せになる）。ゼロサプレスを行い更に先頭の空白も除去したい（＝左寄せにしたい）場合は、空白を区切り文字に指定してUNSTRING文を用いれば良い。上記の例では、UNSTRING文実行後の変数DUMMY-IKIには常に空白が入り（対象の文字列がいきなり空白＝区切り文字から始まり、その前には何も無いため、何も入らない＝空白が入る）、変数HENSHU-IKIには数字の部分だけが入る。

### 実例4 (Fizz Buzz)

``` cobol
000100 IDENTIFICATION DIVISION.
000200 PROGRAM-ID. FIZZBUZZ.
000300 DATA DIVISION.
000400 WORKING-STORAGE SECTION.
000500 01 I           PIC 9(3).
000600 01 HENSHU-IKI  PIC X(8).
000700 PROCEDURE DIVISION.
000800     PERFORM VARYING I FROM 1 BY 1 UNTIL I > 100
000900       MOVE SPACE TO HENSHU-IKI
001000       IF FUNCTION MOD(I 3) = ZERO
001100         MOVE 'FIZZ' TO HENSHU-IKI
001200       END-IF
001300       IF FUNCTION MOD(I 5) = ZERO
001400         STRING
001500           HENSHU-IKI DELIMITED BY SPACE
001600           'BUZZ' DELIMITED BY SIZE
001700           INTO HENSHU-IKI
001800         END-STRING
001900       END-IF
002000       IF HENSHU-IKI = SPACE
002100         MOVE I(3 - FUNCTION INTEGER(FUNCTION LOG10(I)):)
002200           TO HENSHU-IKI
002300       END-IF
002400       DISPLAY HENSHU-IKI
002500     END-PERFORM.
002600     STOP RUN.
```

出力結果は実例3と同じであるが、STRING文による文字列の連結を利用することで、3の倍数かつ5の倍数（すなわち15の倍数）か否かの判定を無くしている。なお、上記の例におけるSTRING文は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")等における

``` java
henshu_iki = henshu_iki + "Buzz";
```

（あるいはこれを略記した

``` java
henshu_iki += "Buzz";
```

）と同様の動作をする。

## 標準化

CODASYLによって標準化が行われてきて、また、[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")や[ISO/IEC JTC 1](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink") SC22/WG4などによっても標準化されていた。 1992年1月にCODASYLのCOBOL委員会とANSIのCOBOL委員会は一本化された。

|          | 米国規格      | 国際規格      | 日本規格    | 主な改正点など                 |
| -------- | --------- | --------- | ------- | ----------------------- |
| 第1次規格    | 1968年制定   | 1972年制定   | 1972年制定 | 最初の規格                   |
| 第2次規格    | 1974年制定   | 1978年制定   | 1980年制定 | 相対・検索ファイル               |
| 第3次規格    | 1985年制定   | 1985年制定   | 1988年制定 | 構造化プログラミング              |
| 第3次追補1規格 | 1989年追補制定 | 1992年追補制定 | 1992年制定 | 組込関数                    |
| 第3次追補2規格 | 1993年追補制定 | 1994年追補制定 | 無し      | 誤り訂正                    |
| 第4次規格    | 2003年制定   | 2002年制定   | 2011年制定 | オブジェクト指向、マルチバイト文字\[15\] |
| 第5次規格    |           | 2014年制定   |         | TRIM組込関数、動的長基本項目        |
|          |           |           |         |                         |

なお、国際規格は ISO/IEC 1989\[16\]、日本規格は JIS X3002\[17\]（旧JIS C 6205）である。

## CODASYL COBOLの言語仕様の変遷

CODASYLでは常時言語仕様の改定をおこなっており、その成果を1～5年ごとにとりまとめてCOBOLの仕様書を発行していた。

  - COBOL-60
      - 最初の版
  - COBOL-61
      - 手続き部の構成の変更、4つの部が出揃う
  - 拡張COBOL-61（1963年）
      - （追加）ソート機能
      - （追加）報告書作成機能
      - （追加）算術文での複数の答え
      - （追加）CORRESPONDING機能
  - COBOL-65
      - 第1次規格の元になる。
      - （追加）大記憶ファイルの処理機能
      - （追加）指標による添字付け、表引き
      - （廃止）誤り診断メッセージへの要求
      - （廃止）必須機能と選択機能の区分
  - COBOL-68
      - この年から開発報告 (JOD) 形式になる。
      - （追加）プログラム間連絡機能
      - （追加）映像端末処理用のSUSPEND文
      - （追加）割り算の余りを求める機能
      - （追加）注釈行
      - （追加）一般化されたCOPY機能
      - （追加）論理的なページあふれ条件の指定と検出
      - （追加）略語による記法
      - （変更）EXAMINE文の機能拡張
      - （廃止）PICTURE句と重複する編集句
      - （廃止）NOTE文、REMARKS段落
      - （廃止）DEFINE文
      - （廃止）一部の略記法
  - COBOL-69
      - （追加）通信機能
      - （追加）翻訳印刷におけるページ送り
      - （追加）実行時の日付と時刻の呼び出し
      - （変更）文字列操作機能
          - （追加）STRING文
          - （追加）UNSTRING文
          - （追加）INSPECT文
          - （廃止）EXAMINE文
      - （追加）SIGN句
      - （廃止）データ部の定数節
  - COBOL-70
      - 第2次規格の元になる。
      - （追加）デバッグ機能
      - （追加）MERGE文
      - （追加）データ初期化のためのINITIALIZE文
      - （変更）報告書作成機能の全面的な改定
      - （廃止）RANGE句
  - COBOL-73
      - （追加）WRITE文によるページ送り
      - （追加）LINAGE句
      - （変更）INSPECT文の機能拡張
      - （変更）直接記憶装置アクセス機能を相対編成と索引編成に組み替え
      - （変更）登録集機能
      - （変更）再実行機能
      - （変更）独立項目記述と一連項目記述の相対位置の自由化
  - COBOL-76
      - （追加）データベース機能
      - （追加）ビット列操作
      - （変更）ファイル定義方法の整理
      - （廃止）独立項目（レベル番号77）
      - （廃止）ALTER
  - COBOL-78
      - 第3次規格の元になる。
      - （追加）構造化プログラミング機能
          - EVALUATE文
          - PERFORM文の機能拡張
          - 名前の有効範囲の規定の整備
      - （変更）プログラム間連絡機能
      - （変更）データベース機能
  - COBOL-81
      - （追加）浮動小数点
      - （追加）算術式による添字
      - （変更）正書法の改訂（自由書式の導入）
      - （廃止）デバッグ機能（デバッグ行以外）
      - （廃止）ENTER文
      - （廃止）CORRESPONDING機能
  - COBOL-84（25周年記念版）
      - 第3次規格（補追）の元になる。
      - （追加）組み込み関数
      - （追加）データ検証 (VALIDATE) 機能
      - （追加）行の一部分に注釈を書く方法
      - （廃止）RERUN機能
  - COBOL-88
      - （追加）表SORT機能
      - （追加）定数の連結
      - （追加）画面制御機能
      - （追加）いくつかの組み込み関数
      - （廃止）区分化機能
      - （変更）語の長さを60字以下までとする。
  - COBOL-93（最終版）
      - （追加）マルチオクテット処理
      - （追加）ファイルの排他共用制御
      - （追加）いくつかの組み込み関数
      - （変更）語の長さを30字以下までにもどす。

## 脚注

## 関連項目

  - [グレース・ホッパー](../Page/グレース・ホッパー.md "wikilink") - COBOLの開発者。俗に「COBOLの母」と呼ばれる。
  - [FORTRAN](../Page/FORTRAN.md "wikilink")
  - [COBOL/S](https://ja.wikipedia.org/wiki/COBOL/S "wikilink") - [NEC](https://ja.wikipedia.org/wiki/NEC "wikilink")の汎用機（[ACOS](https://ja.wikipedia.org/wiki/ACOS "wikilink")）用COBOL。

## 外部リンク

  - [COBOLコンソーシアム](http://www.cobol.gr.jp/)
  - [社会を支えるCOBOL、50年の歩み - 日経コンピュータ](http://itpro.nikkeibp.co.jp/article/COLUMN/20100319/345985/)
  - [GnuCOBOL (formerly OpenCOBOL)](https://sourceforge.net/projects/open-cobol/) 自由なソフトウェアとしてのコボル言語処理系

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:グレース・ホッパー](https://ja.wikipedia.org/wiki/Category:グレース・ホッパー "wikilink") [Category:COBOL](https://ja.wikipedia.org/wiki/Category:COBOL "wikilink") [Category:基本情報技術者試験](https://ja.wikipedia.org/wiki/Category:基本情報技術者試験 "wikilink")

1.  [Around 80% of the world's actively used code is none other than COBOL](http://www.uctcorp.com/cobol-programmers.asp)
2.  [20 Things You Might Not Know About COBOL (as the Language Turns 50)](http://want2change.wordpress.com/tag/cobol/) (Darryl Taft)
3.  [Platform Migration](http://www.cobug.com/cobug/docs/MicroFocusTorontoCratosSUMMARY-PresentationJan2006.pdf) (CRATOS; Andrew Wickett) p.9 "COBOL Facts"
4.   ([IPA](../Page/情報処理推進機構.md "wikilink")) 39ページ「図表4-4-1、4-4-2開発言語（第1回答）」
5.
6.  [社会を支えるCOBOL、50年の歩み - 誕生50周年、社会を支えつづけるCOBOL:ITpro](http://itpro.nikkeibp.co.jp/article/COLUMN/20100319/345985/)
7.  [COBOL誕生から60年--これからも生き続ける理由 - ZDNet](https://japan.zdnet.com/article/35142380/)
8.
9.
10.
11. [まだまだ現役：プログラミング言語のCOBOLが誕生50周年 - ITmedia](http://www.itmedia.co.jp/enterprise/articles/0909/19/news006.html)
12. [COBOLコンソーシアム](http://www.cobol.gr.jp/)
13. [COBOL誕生50周年記念セミナー 社会を支える“ことば”。これまでも、そしてこれからも](http://www.cobol.gr.jp/knowledge/material/100416_report.html)
14. [COBOLはクラウド時代も現役、09年は最も多くのコードが書かれた---英マイクロフォーカス CTO スチュアート・マギル氏 - ITpro](http://itpro.nikkeibp.co.jp/article/Interview/20091127/341216/)
15. [第4次COBOL規格 COBOL2002のご紹介](http://www.cobol.gr.jp/knowledge/next_standard/standard002.html)
16. [ISO/IEC 1989:2014 - Information technology -- Programming languages, their environments and system software interfaces -- Programming language COBOL](https://www.iso.org/standard/51416.html)
17. [日本工業標準調査会：データベース検索-JIS検索](http://www.jisc.go.jp/app/jis/general/GnrJISSearch.html)