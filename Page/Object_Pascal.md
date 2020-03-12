> この記事は[Object Pascal](https://ja.wikipedia.org/wiki/Object_Pascal)から翻訳されています。


**Object Pascal**（**オブジェクト パスカル**）は、[コンピュータ](../Page/コンピュータ.md "wikilink")の[プログラミング言語](../Page/プログラミング言語.md "wikilink")のひとつ。広義には[Pascal](../Page/Pascal.md "wikilink")言語に[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の概念を導入したものを指し、狭義には[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) である[Delphi](../Page/Delphi.md "wikilink")や、[コンパイラ](../Page/コンパイラ.md "wikilink")である[Free Pascalで使用される言語仕様を指す](../Page/Free_Pascal.md "wikilink")。

## 沿革

Object Pascalは1980年代に登場したPascalのオブジェクト指向拡張に端を発する。Pascalは当時[アップルコンピュータ](https://ja.wikipedia.org/wiki/アップルコンピュータ "wikilink")（現[アップル](../Page/アップル_\(企業\).md "wikilink")）の主要な開発言語として利用されており、と呼ばれる処理系の実装が存在した。[Apple LisaにおいてもLisa](../Page/Lisa_\(コンピュータ\).md "wikilink") Pascalと呼ばれる開発環境が使われていた。1983年、アップルコンピュータの[ラリー・テスラー](https://ja.wikipedia.org/wiki/ラリー・テスラー "wikilink")率いるチームはPascal言語の発明者である[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")を招き、Lisa Pascalにオブジェクト指向のための拡張を導入し、これをと名付けた。このClascalが[Macintosh](../Page/Macintosh.md "wikilink")上のObject Pascalにつながっていくことになる。

Object Pascalは、現在ではクラスライブラリと呼ばれる拡張可能なMacintoshアプリケーションフレームワークであるをサポートするために必要だった。Object Pascalをサポートするソフトウェア開発環境である (MPW) の開発は1985年に始まり、1986年に製品となった。しばらくの間、Object PascalはアップルやMacintoshの主要な開発言語の1つになった。MPW Pascalのサポートは1995年11月まで続いた。後にMPW Pascal (Apple Object Pascal) は遡って**Mac Pascal**と命名された\[1\]。また、Object Pascal拡張は[Symantec](https://ja.wikipedia.org/wiki/Symantec "wikilink")社のTHINK Pascalや社の[CodeWarrior](../Page/CodeWarrior.md "wikilink") Pascalにも実装された。

1990年にリリースされた[ボーランド](../Page/ボーランド.md "wikilink")社の[Turbo Pascal](../Page/Turbo_Pascal.md "wikilink") 5.5でも類似のObject Pascal拡張が実装されており、Object Pascalを最大限に利用したTurbo Vision等の[CUI](../Page/キャラクタユーザインタフェース.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")が製品に付属するようになった。これらのObject Pascalクラスライブラリの技術は後の[Delphi](../Page/Delphi.md "wikilink")とDelphiに付属する**[Visual Component Library](../Page/Visual_Component_Library.md "wikilink")** (VCL) へと引き継がれていった。

1995年にリリースされたボーランド社のWindows用[Rapid Application Development](../Page/Rapid_Application_Development.md "wikilink") (RAD) ツールである[Delphi](../Page/Delphi.md "wikilink")は、当初難解だったWindows [GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[アプリケーション開発](../Page/アプリケーションソフトウェア.md "wikilink")\[2\]の難易度を下げるだけでなく効率も高めることで成功を収め、また無償の個人向けエディションも配布されていたことから、多くの一般ホビープログラマにObject Pascalが認知されることとなった。[Microsoft Visual Basicと異なり](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")、Delphiでは当初から高速な[機械語](../Page/機械語.md "wikilink")コードを実行可能なネイティブバイナリを出力する方式であったこと、またC++と比べてコンパイルが高速であったことも人気に影響した。

[Delphi](../Page/Delphi.md "wikilink")のバージョンXE2以降には従来のクラスライブラリ (VCL) に加え、[マルチプラットフォーム](https://ja.wikipedia.org/wiki/マルチプラットフォーム "wikilink")用クラスライブラリである**** (FMX) と各プラットフォーム向けのクロスコンパイラが付属する。

なお、開発環境としてのDelphiで使用されるプログラミング言語は、Delphi 6まではObject Pascalと呼ばれていたが、Delphi 7より**Delphi言語** (**Delphi Language**) と改称された。その後、ボーランドの開発ツール部門[CodeGear](https://ja.wikipedia.org/wiki/CodeGear "wikilink")は2008年に[エンバカデロ・テクノロジーズ](https://ja.wikipedia.org/wiki/エンバカデロ・テクノロジーズ "wikilink")に合併され、DelphiおよびDelphi言語はエンバカデロに移管された。[Appmethod](https://ja.wikipedia.org/wiki/Appmethod "wikilink")が登場してからは再びObject Pascalと呼ばれるようになっているが、ドキュメント類にはDelphi言語という表記も依然として残っている。

同じくWindows用RADツールとして[Visual Basicをリリースしていた](../Page/Visual_Basic.md "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")社は、[Delphi](../Page/Delphi.md "wikilink")のプログラミングスタイルおよびVCLの完成度の高さに着目し、Object Pascalのように言語に依存しないものとして、[.NET Frameworkと呼ばれるアプリケーション開発](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")・実行環境を開発した。[.NET](https://ja.wikipedia.org/wiki/.NET "wikilink")の主要言語である[C\#の言語仕様](../Page/C_Sharp.md "wikilink")、.NETの[基本クラスライブラリ](https://ja.wikipedia.org/wiki/基本クラスライブラリ "wikilink")の設計思想、およびRADとしての[Visual C\#は](../Page/Microsoft_Visual_C_Sharp.md "wikilink")、それぞれObject Pascal、VCL、およびRADとしてのDelphiに強く影響を受けている。なお、C\#の開発者[アンダース・ヘルスバーグ](../Page/アンダース・ヘルスバーグ.md "wikilink")は、もともとボーランドに在籍しており、Delphiの開発者でもあった\[3\]。

ボーランド社の.NET用 Object Pascal コンパイラは、Delphi 8から始まり[RAD Studio](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink") 2007まで存在していた。これらは**Delphi for .NET**と呼ばれた。代替製品として[RAD Studioには](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink")[RemObjects社の](https://ja.wikipedia.org/wiki/:en:RemObjects "wikilink")[Oxygeneが](https://ja.wikipedia.org/wiki/:en:Oxygene "wikilink")**Delphi Prism**という名称で[RAD Studio](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink") 2009からXE3まで付属した。[Oxygeneの開発は現在も継続されており](https://ja.wikipedia.org/wiki/:en:Oxygene "wikilink")、言語名もOxygene言語となっている。

一方、[オープンソース](../Page/オープンソース.md "wikilink")のObject Pascal実装としては[Free Pascalや](../Page/Free_Pascal.md "wikilink")[GNU Pascalがある](https://ja.wikipedia.org/wiki/GNU_Pascal "wikilink")。[Free Pascalは当初](../Page/Free_Pascal.md "wikilink")[Turbo Pascalの言語仕様をベースにして作られた](../Page/Turbo_Pascal.md "wikilink")。現在ではApple互換モードやDelphi互換モードも実装され、さらにはクロスプラットフォームのための独自の仕様追加や、[C言語](../Page/C言語.md "wikilink")のようなマクロ等の拡張も行われている。[Delphi](../Page/Delphi.md "wikilink")のような[統合開発環境](../Page/統合開発環境.md "wikilink")を[マルチプラットフォーム](https://ja.wikipedia.org/wiki/マルチプラットフォーム "wikilink")で実現するための[Lazarus](../Page/Lazarus.md "wikilink")やクラスライブラリ**** (LCL) の開発もオープンソースの元で進められている。[GNU Pascalは標準Pascal](https://ja.wikipedia.org/wiki/GNU_Pascal "wikilink") ([ISO/IEC 7185](https://ja.wikipedia.org/wiki/ISO/IEC_7185 "wikilink")) や拡張Pascal (ISO/IEC 10206) をメインに実装されているが、[Delphi](../Page/Delphi.md "wikilink")の機能も部分的に実装している。また、[GNU Pascalにも](https://ja.wikipedia.org/wiki/GNU_Pascal "wikilink")[Dev-Pascalと呼ばれる](https://ja.wikipedia.org/wiki/:en:Dev-Pascal "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink")が存在する。

## Pascalからの拡張

Object Pascalは（[C++](../Page/C++.md "wikilink")系統の）オブジェクト指向言語の三大要素である、[カプセル化](../Page/カプセル化.md "wikilink")、[継承](../Page/継承_\(プログラミング\).md "wikilink")、および[多態性](https://ja.wikipedia.org/wiki/多態性 "wikilink")（ポリモーフィズム）をサポートしている。Object Pascalにおける、従来のPascalからの主な拡張点は次のような点が挙げられる。

### クラス

[クラスの定義構文は](../Page/クラス_\(コンピュータ\).md "wikilink")、従来のPascalにおけるrecord（[C言語](../Page/C言語.md "wikilink")の[構造体](../Page/構造体.md "wikilink")に相当）の定義構文を拡張したものである。クラス型の要素として変数以外にも手続きや関数を書けるようになっている。クラスに属する変数は[フィールド](../Page/フィールド_\(計算機科学\).md "wikilink")（C++のメンバ変数に相当）、また手続きおよび関数は[メソッド](../Page/メソッド_\(計算機科学\).md "wikilink")（C++のメンバ関数に相当）と呼ばれ、通常の変数、手続きおよび関数と区別される。

また、クラスの属性であるフィールドにアクセスする際に、冗長なメソッドを用いるのではなく、より簡潔に記述するための仕組みとして、[プロパティと呼ばれる構文が用意されている](https://ja.wikipedia.org/wiki/プロパティ_\(プログラミング\) "wikilink")。プロパティを用いることで、オブジェクト指向のカプセル化を維持しつつ、あたかもフィールドに直接アクセスしているかのような直感的な記述でクラスの属性を操作することが可能となる。

メソッドの実装は(クラス名).(メソッド名)という形で記述する。

例:

``` pascal
program MyObjectPascalTest;

type
  TMyBaseClass = class
  private
    Fa: Integer;
    Fb: Integer;
  public
    procedure SetValueA(v: Integer);
    function GetValueA: Integer;
    property ValueB: Integer read Fb write Fb; // 読み書き両方が可能なプロパティ。
    procedure DoSomething; virtual; abstract;
  end;

  TMySubClass = class(TMyBaseClass)
  public
    procedure DoSomething; override;
  end;

procedure TMyBaseClass.SetValueA(v: Integer);
begin
  Fa := v
end;

function TMyBaseClass.GetValueA: Integer;
begin
  Result := Fa
end;

procedure TMySubClass.DoSomething;
begin
  WriteLn('TMySubClass.DoSomething is called.');
  WriteLn('ValueA = ', GetValueA);
  WriteLn('ValueB = ', ValueB)
end;

var
  obj: TMyBaseClass;
begin
  obj := TMySubClass.Create; // オブジェクトの生成。
  obj.SetValueA(100);
  obj.ValueB := -5;
  obj.DoSomething; // 派生クラスでオーバーライドされたメソッドが実行される（ポリモーフィズム）。
  obj.Free; // オブジェクトの解放。
  obj := Nil
end.
```

クラス名は慣例的にTypeを意味する 'T' で始められることが多く、フィールド名は慣例的に 'F' で始められることが多い。

**type** TX = **class** の構文は、Systemユニットで定義されている基底クラスTObjectから暗黙的に派生することを意味する。**type** TB = **class**(TA) の構文において、クラスTAはTObjectそのものであるか、あるいはTObjectから派生している必要がある\[4\]。一方、**type** TB = **object**(TA) の構文を使用することで、TObjectから派生せず、組み込みのコンストラクタやデストラクタなどのメソッドをサポートしない**オブジェクト型**の宣言を行なうことができるが、DelphiやAppmethodにおいては下位互換性を保つ目的でのみ残されており、オブジェクト型の使用は推奨されていない\[5\]\[6\]\[7\]。

クラスの定義にユニット (unit) を用いる場合、クラスの宣言は interface 部に、メソッドの実装は implementation 部に記述する。

例:

``` pascal
unit MyUnit;

interface

type
  TMyClass = class
  public
    procedure Proc;
  end;

implementation

procedure TMyClass.Proc;
begin
  { ここに実装を記述 }
end;

end.
```

### インターフェイス

Object PascalはC++と異なり、実装の[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")をサポートしない。その代わりに、[インターフェイスを実装することによる型の多重継承をサポートする](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")。インターフェイス名は慣例的にInterfaceを意味する 'I' で始められることが多い。

Object Pascalにおける継承の機能やメカニズムは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")とよく似ており、のちにC\#にも受け継がれることになった。

### クラス参照型

C++などのオブジェクト指向言語と比較して、Object Pascalが優れている点として、[クラス参照型](https://ja.wikipedia.org/wiki/クラス参照型 "wikilink")のサポートが挙げられる。クラス参照型の変数には、実体ではないクラス自体を変数に代入することができる。これは、設計図をもとに作られた製品ではなく、設計図自体を格納する変数を定義できると考えれば分かりやすい。クラス参照型は[メタクラス](../Page/メタクラス.md "wikilink")とも呼ばれ、[実行時型情報](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink") (RTTI) によって実現される。クラス参照型は、その実際の型がコンパイル時にわからないクラスまたはオブジェクトでクラスメソッドまたは仮想コンストラクタを呼び出したい場合（例えば逆[シリアライズ](../Page/シリアライズ.md "wikilink")など）に便利である。

### 例外

Object Pascalは、エラーハンドリング機構として[例外をサポートしている](../Page/例外処理.md "wikilink")。例外オブジェクトは、エラーやその他のイベントによりプログラムの通常の実行が中断された場合に生成される。例外を用いることで、整数値エラーコードを用いるよりも多くの情報を呼び出し側に伝播させることができる。

例外処理の構文には **try...except** および **try...finally** がある。

## 言語としての特徴

Object Pascalはそのコンパクトで明快な言語仕様ゆえに、オブジェクト指向言語の学習に適していると言われる（C++の演算子オーバーロード、[テンプレートや](../Page/テンプレート_\(プログラミング\).md "wikilink")[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")のような便利だが比較的難解で複雑な機能を持たない）。反面、近年多くのプログラミング言語が導入している[ジェネリクス](https://ja.wikipedia.org/wiki/ジェネリクス "wikilink")や[ラムダ式](https://ja.wikipedia.org/wiki/ラムダ式 "wikilink")をサポートしていなかったため、[ジェネリックプログラミング](../Page/ジェネリックプログラミング.md "wikilink")や[関数型プログラミング](https://ja.wikipedia.org/wiki/関数型プログラミング "wikilink")には不向きだった。

DelphiではDelphi 2006で演算子のオーバーロードが、Delphi 2009でジェネリクスおよび[無名メソッド](https://ja.wikipedia.org/wiki/無名関数 "wikilink")（匿名メソッド）が、Delphi 10.3 Rioで[型推論](../Page/型推論.md "wikilink")可能なインライン変数宣言が実装された\[8\]ため、柔軟な記述が可能になっている。また、Delphi 2005以降ではインライン関数がサポートされ、実行速度面での強化も図られている。Delphi 2010ではRTTIが強化され、[リフレクションをサポートするようになった](../Page/リフレクション_\(情報工学\).md "wikilink")。

また、DelphiのVCLやFMXは単なるクラスライブラリにとどまらず、[コンポーネントと呼ばれるソフトウェア部品の集合で構成され](../Page/ソフトウェアコンポーネント.md "wikilink")、このコンポーネントを組み合わせて視覚的にアプリケーションを開発する方式となっている。Delphiではユーザー[プログラマ](../Page/プログラマ.md "wikilink")が[コンポーネントを自由に作成して開発環境自体に組み込むことができるため](../Page/ソフトウェアコンポーネント.md "wikilink")、「**コンポーネント指向言語**」と呼ばれることもある。

## 出典・脚注

## 関連項目

  - [Pascal](../Page/Pascal.md "wikilink")
  - [Delphi](../Page/Delphi.md "wikilink")
  - [C\#](../Page/C_Sharp.md "wikilink")

## 外部リンク

  - [Delphi Downloads](https://www.embarcadero.com/jp/products/delphi/downloads) - Delphi Architect Edition（30日評価版）のダウンロードページ
  - [Delphi Community Edition](https://www.embarcadero.com/jp/products/delphi/starter) - Delphi Community Edition（無償版）のダウンロードページ
  - [Free Pascal](http://www.freepascal.org/) - [Free Pascal](../Page/Free_Pascal.md "wikilink") はオープンソースの Pascal コンパイラ。Object Pascal もサポートしている。
  - [GNU Pascal](http://www.gnu-pascal.de/gpc/h-index.html) - [GNU Pascal](https://ja.wikipedia.org/wiki/GNU_Pascal "wikilink") はオープンソースの Pascal コンパイラ。Object Pascal も一部サポートしている。
  - [Lazarus](http://www.lazarus.freepascal.org/) - [Lazarus](../Page/Lazarus.md "wikilink") は [Free Pascal](../Page/Free_Pascal.md "wikilink") の[統合開発環境](../Page/統合開発環境.md "wikilink")。

[Category:Pascal](https://ja.wikipedia.org/wiki/Category:Pascal "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:ボーランド](https://ja.wikipedia.org/wiki/Category:ボーランド "wikilink")

1.  [Mac Pascal - Free Pascal wiki](https://wiki.freepascal.org/Mac_Pascal)
2.  [Windows APIおよび](../Page/Windows_API.md "wikilink")[C言語](../Page/C言語.md "wikilink")あるいは[C++](../Page/C++.md "wikilink")の知識を必要とし、またVisual Basic以外のRADは十分にサポートされていなかった。
3.  [主な機能 - Embarcadero Website](https://www.embarcadero.com/jp/products/delphi/features/delphi)
4.  `TObject`は、Javaにおける暗黙の最上位基底クラスである[オブジェクト型](../Page/オブジェクト型.md "wikilink")や、.NETにおける`System.Object`に相当するが、Object Pascalにおける「オブジェクト型」という用語は意味が異なるので注意されたい。
5.
6.  [クラスとオブジェクト（Object Pascal） - Appmethod Topics](http://docwiki.appmethod.com/appmethod/1.16/topics/ja/%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%A8%E3%82%AA%E3%83%96%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88)
7.  [クラスとオブジェクト（Delphi） - Embarcadero DocWiki](http://docwiki.embarcadero.com/RADStudio/ja/%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%A8%E3%82%AA%E3%83%96%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88%EF%BC%88Delphi%EF%BC%89)
8.  [インライン変数宣言 - RAD Studio](http://docwiki.embarcadero.com/RADStudio/Rio/ja/%E3%82%A4%E3%83%B3%E3%83%A9%E3%82%A4%E3%83%B3%E5%A4%89%E6%95%B0%E5%AE%A3%E8%A8%80)