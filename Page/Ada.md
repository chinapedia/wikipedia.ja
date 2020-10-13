> この記事は[Ada](https://ja.wikipedia.org/wiki/Ada)から翻訳されています。


Ada 95{{-}}Ada 2005{{-}}Ada 2012 | typing = nominative, [安全な](https://ja.wikipedia.org/wiki/型システム#型の安全性 "wikilink")[強い](https://ja.wikipedia.org/wiki/型システム#強い型付けと弱い型付け "wikilink")[静的型付け](https://ja.wikipedia.org/wiki/静的型付け "wikilink") | implementations = [GNAT](https://ja.wikipedia.org/wiki/GNAT "wikilink") ([GCC](../Page/GNUコンパイラコレクション.md "wikilink")) 他 | influenced = [C++](../Page/C++.md "wikilink"), [PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink"), [VHDL](../Page/VHDL.md "wikilink"), [Java](https://ja.wikipedia.org/wiki/Java "wikilink"), [C言語](../Page/C言語.md "wikilink") ([C99](../Page/C99.md "wikilink")) | operating system = 多数 | website =  | file ext = .adb, .ads }}

**Ada**（エイダ）は、[構造化](../Page/構造化プログラミング.md "wikilink")・[静的型付け](https://ja.wikipedia.org/wiki/静的型付け "wikilink")・[命令型](../Page/命令型プログラミング.md "wikilink")・[オブジェクト指向の](../Page/オブジェクト指向プログラミング.md "wikilink")[パラダイムを持つ汎用](../Page/プログラミングパラダイム.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")の一つである。構文は[Algol](https://ja.wikipedia.org/wiki/Algol "wikilink")系である。

史上初の [プログラマ](../Page/プログラマ.md "wikilink")とされる[エイダ・ラブレス](../Page/エイダ・ラブレス.md "wikilink")の名前にちなんで**Ada**と命名されている。**ADA**と表記するのは誤り。

フリーの[コンパイラ](../Page/コンパイラ.md "wikilink")としては、[GNAT](https://ja.wikipedia.org/wiki/GNAT "wikilink")などがある。

## 特徴

[thumb](https://ja.wikipedia.org/wiki/ファイル:Ada_types.png "wikilink") 1979年、[米国国防総省](https://ja.wikipedia.org/wiki/米国国防総省 "wikilink")が信頼性・保守性に優れた、主として[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けの言語を作りたいという意図のもと、国際競争入札を行い4社に発注、各設計仕様書の表紙が赤、青、黄、緑だったことから、そのままそれぞれの言語名称としてRED、BLUE、YELLOW、GREENと呼ばれた。この入札で優勝したのはフランス人チームで、公平を期すため選定時にはGREENと名付けられた。そのような理由から、イメージカラーは緑である。特徴的な要件としては、大規模開発や長期保守性の観点から、

  - コーディング効率よりも可読性を重視すること
  - [プリプロセッサ](../Page/プリプロセッサ.md "wikilink")マクロを持たないこと

などがあった。

プログラム言語としての機能としては、

  - 強い型検査（コンパイル時および実行時）。属性によって型に関する情報が取得できる。
  - 複雑な型を持つ定数。
  - 手続き・関数・演算子の多重定義。
  - プラグマを使った処理系依存の機能の指定。
  - パッケージ（後に[C++](../Page/C++.md "wikilink")が[namespaceとして追従](../Page/名前空間.md "wikilink")）
  - 汎用プログラミング（後にC++が[テンプレートとして追従](../Page/テンプレート_\(プログラミング\).md "wikilink")）
  - 並行プログラミング（タスク、entry/accept/select文など）
  - [例外](../Page/例外処理.md "wikilink")

など、当時としては先進的な機能\[1\]を意欲的に取り入れたため、[米国国防総省](https://ja.wikipedia.org/wiki/米国国防総省 "wikilink")は大きなものとなってしまった言語仕様をまとめるのに、初版のStrawman（わら男、[案山子の意味もある](../Page/かかし.md "wikilink")）からWoodenman（木男）、Tinman（ブリキ男、前述の案山子とともに『[オズの魔法使い](../Page/オズの魔法使い.md "wikilink")』に出てくる）、Ironman（鉄男）、最終版のSteelman（鋼鉄男）に至るまで5つのバージョンに分けて策定を行った。

言語仕様の大きさや厳密さのため、当時のコンピュータが持っていた資源では、処理系の実装に[ミニコンや](../Page/ミニコンピュータ.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")程度を必要とし、16ビット[パソコンには市場性といった事情もあり実装はほとんどない](../Page/パーソナルコンピュータ.md "wikilink")。実際にはAdaは、大企業において、主として信頼性や保守性を要求されるシステムの開発でのみ普及した。というよりも、実際にどの程度徹底されたかは不明だが、策定の主体であった米国国防総省が発注するようなもの、即ち[兵器](../Page/兵器.md "wikilink")の開発において条件とされたと言われる。

この時期としては先進的であった、その他の特徴としては、

  - コンパイラの認定制度
    仕様準拠か否かの検証プログラムキットが規定され、合格しない処理系は「Adaコンパイラ」と称することができない。
  - 自動ビルド
    複数モジュールの依存性から、再コンパイルの要否を自動判定する（いわゆる[Makefile](https://ja.wikipedia.org/wiki/Makefile "wikilink")の記述が不要）

などがあげられる。

策定作業中に仕様が大きくなっていった際には、仕様が高度に巨大化した言語が、兵器のように高度な信頼性を要求される分野に、国防総省の「お墨付き」として使用されることを危ぶむ向きもあった。たとえば[アントニー・ホーア](../Page/アントニー・ホーア.md "wikilink")は1980年度の[チューリング賞](../Page/チューリング賞.md "wikilink")受賞者だが\[2\]、その受賞記念講演 (Turing Award Lecture) *"The Emperor's Old Clothes"* において、自身のALGOL 68（[:en:ALGOL 68](https://ja.wikipedia.org/wiki/:en:ALGOL_68 "wikilink")、やはり仕様の巨大化で知られる）に関する経験などに触れたうえで、Adaへの憂慮で締めくくっている\[3\]。

## 標準

言語仕様は、最初に1983年に[MIL規格](../Page/MIL規格.md "wikilink")として規格化され、[エイダ・ラブレス](../Page/エイダ・ラブレス.md "wikilink")の生年である1815年に因んで、**MIL-STD-1815**と採番された。この規格は[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")標準、1987年に[ISO標準](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") ISO/IEC 8652:1987 として標準化された。

1990年より、主としてタスキング仕様の改善および[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の導入を目的として、ISO標準 (ISO/IEC 8652:1987) の改訂作業が開始された。1995年2月15日にISO標準として改訂が承認され、[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")のうち、史上初の国際標準となった。1995年の規格は、オブジェクト指向の他、下記のような仕様も標準化されている。

  - 他言語 ([C](../Page/C言語.md "wikilink")/[FORTRAN](../Page/FORTRAN.md "wikilink")/[COBOL](../Page/COBOL.md "wikilink")) との相互運用インターフェイス
      -
        この時点でC++との相互運用インターフェイスが標準化できなかったのは、C++の標準化がまだだったからである（C++の標準は、紛糾を経て約3年半後の1998年9月1日に承認された）
  - [分散処理](https://ja.wikipedia.org/wiki/分散処理 "wikilink") (RPC)

2000年にTechnical Amendmentが発行された（ISO/IEC 8652:1995/COR1:2000）。同改訂版は、JISでは2002年版 (JIS X 3009:2002) に対応する。JIS X 3009は本文の翻訳はしていない「要約JIS」であった。2012年1月20日を以って「国際規格周知を目的として要約JISを発行したが，周知としての目的は終了したため。」として廃止されている。

Ada の ISO 規格は、その後、2005年と2012年にも改訂されている。

## コード例

Adaのソースコードは各パッケージの宣言部を .ads ファイル (specification file) に、実装部を .adb ファイル (body file) に記述する。

リファレンスマニュアルなどでは慣例的に3スペース（空白3個）の[インデント](https://ja.wikipedia.org/wiki/インデント "wikilink")が使われている。大文字と小文字を区別しないが、識別子は慣例的に単語の先頭を大文字にして、さらに単語間を[アンダースコア](../Page/アンダースコア.md "wikilink")でつなぐ（[キャメルケース](../Page/キャメルケース.md "wikilink")とスネークケースの併用）。

### Hello World

``` ada
-- Ada.Text_IO パッケージを取り込む。
with Ada.Text_IO;
-- use 節で指定することでパッケージ名の修飾を省略することも可能。
--use Ada.Text_IO;

procedure Program is
begin
   Ada.Text_IO.Put_Line("Hello, world!");
   --Put_Line("Hello, world!");
end Program;
```

### ループと条件分岐

``` ada
with Ada.Text_IO, Ada.Integer_Text_IO, Ada.Float_Text_IO;
use Ada.Text_IO;

procedure Program is
   I : Integer := 0;
   F : Float;
begin
   for I in 0 .. 10 loop
      -- 左寄せで出力。
      Ada.Integer_Text_IO.Put(I, 0);
      if I mod 2 = 0 then
         Put_Line(": even number.");
      else
         Put_Line(": odd number.");
      end if;
      F := Float(I) * 0.1;
      Ada.Float_Text_IO.Put(F, 0, 1, 0);
      Put_Line("");
   end loop;
end Program;
```

## 利用例

の利用例としては[F-22戦闘機や](../Page/F-22_\(戦闘機\).md "wikilink")[97式魚雷](../Page/97式魚雷.md "wikilink")などがある。ただしこの分野でもAdaの陳腐化が進んでおり、[F-35戦闘機以降はC](../Page/F-35_\(戦闘機\).md "wikilink")++へ移行している。

民生品ではあまり利用されていないが、信頼性を重視する航空機の制御ソフトウェアに利用されることがある。例としては[ボーイング777](../Page/ボーイング777.md "wikilink")など。

## 注釈・出典

## 外部リンク

  - [Ada Information Clearing House](http://www.adaic.com)
  - [Ada規格](http://www.ada-auth.org/arm.html)
  - [Steelman仕様](http://archive.adaic.com/docs/reports/steelman/intro.htm)
  - [About Ada - Adacore](https://www.adacore.com/about-ada)

## 関連項目

  - [予約語 (Ada)](../Page/予約語_\(Ada\).md "wikilink")
  - [ジェネリックプログラミング](../Page/ジェネリックプログラミング.md "wikilink")

[カテゴリ:プログラミング言語](https://ja.wikipedia.org/wiki/カテゴリ:プログラミング言語 "wikilink") [カテゴリ:並行計算](https://ja.wikipedia.org/wiki/カテゴリ:並行計算 "wikilink") [カテゴリ:ISO/IEC標準](https://ja.wikipedia.org/wiki/カテゴリ:ISO/IEC標準 "wikilink") [カテゴリ:JIS](https://ja.wikipedia.org/wiki/カテゴリ:JIS "wikilink") [カテゴリ:エポニム](https://ja.wikipedia.org/wiki/カテゴリ:エポニム "wikilink")

1.  先進的ということは、言い換えれば「こなれていない」ということであり、兵器のようなシステムでは冒険的過ぎると言えなくもない。
2.  [C. Antony R. Hoare - A.M. Turing Award Laureate](http://amturing.acm.org/award_winners/hoare_4622167.cfm)
3.  この講演は、二通りのソフトウェアの設計構築法について述べた *"One way is to make it so simple that there are obviously no deficiencies and the other way is to make it so complicated that there are no obvious deficiencies."*; 「ひとつめの方法は**あきらかに**欠陥が無いようにso simpleにするというもので、もうひとつの方法は**あきらかな**欠陥が無いようにso complicatedにするというものである」という文章でも知られる。