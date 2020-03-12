> この記事は[Visual Component Library](https://ja.wikipedia.org/wiki/Visual_Component_Library)から翻訳されています。


**Visual Component Library** (VCL) とは、視覚化された（ビジュアルな）[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")を元にして、[Microsoft Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[アプリケーションを作成するためのソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")および[フレームワークである](../Page/アプリケーションフレームワーク.md "wikilink")。[ボーランド](../Page/ボーランド.md "wikilink")が、自社のソフトウェア[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) である[Delphi](../Page/Delphi.md "wikilink")と[C++ Builderのために開発した](../Page/C++_Builder.md "wikilink")。[Object Pascalで記述されている](../Page/Object_Pascal.md "wikilink")。

VCLはボーランドの[RADツールと密接に統合されており](../Page/Rapid_Application_Development.md "wikilink")、プログラミング言語でコードを記述することなく[GUI部品の配置や外観設定をGUI](https://ja.wikipedia.org/wiki/ウィジェット_\(GUI\) "wikilink")（フォームデザイナー）で視覚的かつ直感的に行なうこともできるようになっている\[1\]。これが人気の元である。

後に、同等の機能を持つ[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")のライブラリとして[Component Library for Cross Platform](../Page/Component_Library_for_Cross_Platform.md "wikilink") (CLX) がDelphi、C++ Builder、[Kylix](../Page/Kylix.md "wikilink")用に開発されたが、VCLの人気の前には太刀打ちできなかった。

VCLは[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の[クラスライブラリであり](../Page/クラス_\(コンピュータ\).md "wikilink")、`System.TObject`クラス\[2\]を最上位基底クラスとする単一[継承のオブジェクト階層をもっている](../Page/継承_\(プログラミング\).md "wikilink")。Object Pascalは（[C++](../Page/C++.md "wikilink")と異なり）実装の[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")をサポートしておらず、代わりに[インターフェイスを実装することによる型の多重継承をサポートする](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")\[3\]。VCLでもインターフェイスによる[ポリモーフィズム](../Page/ポリモーフィズム.md "wikilink")が利用されている。例えば`System.Classes.TComponent`クラス\[4\]は、

``` pascal
TComponent = class(TPersistent, IInterface, IInterfaceComponentReference)
```

というように`TPersistent`クラスから派生し、さらに`IInterface`および`IInterfaceComponentReference`インターフェイスを実装する。

Object Pascalにおける継承の機能やメカニズムは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")とよく似ており、のちに[C\#にも受け継がれることになった](../Page/C_Sharp.md "wikilink")。

## 派生

1999年6月8日、インプライズ（ボーランド）は[マイクロソフト](../Page/マイクロソフト.md "wikilink")に対し12,500万ドルでその特許使用を認める契約をし\[5\]、後にVCLの派生ライブラリとして[.NET Frameworkの](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[基本クラスライブラリ](https://ja.wikipedia.org/wiki/基本クラスライブラリ "wikilink")が公開され、現在では[C\#や](../Page/C_Sharp.md "wikilink")[Visual Basic .NETを中心としたWindowsアプリケーション開発における主力ライブラリとなっているほか](../Page/Visual_Basic_.NET.md "wikilink")、[Monoや](../Page/Mono_\(ソフトウェア\).md "wikilink")[.NET CoreによりWindows以外のプラットフォームにも広がりを見せている](https://ja.wikipedia.org/wiki/.NET_Core "wikilink")。特に[Windows Formsは](../Page/Windows_Forms.md "wikilink")、VCLの設計や開発スタイルを強く受け継いでいる。

## 問題点

VCLはWindows専用であり、他プラットフォームへの[移植性](../Page/移植性.md "wikilink")はない。また、Delphi側の仕様起因で[Unicode](../Page/Unicode.md "wikilink")対応が遅れていたが、Delphi 2009でUnicode対応が強化された\[6\]。

## 関連項目

  - [Component Library for Cross Platform](../Page/Component_Library_for_Cross_Platform.md "wikilink") (CLX)

  -
  - [Delphi](../Page/Delphi.md "wikilink")

  - [ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")

  - [Microsoft Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")

  - [基本クラスライブラリ](https://ja.wikipedia.org/wiki/基本クラスライブラリ "wikilink")

  - [Windows Forms](../Page/Windows_Forms.md "wikilink")

## 脚注

## 外部リンク

  - [Delphi 1.0 Visual Component Library Reference](ftp://ftpc.borland.com/pub/delphi/devsupport/general/delphi1/vclref.zip)
  - [JEDI Visual Component Library](http://homepages.borland.com/jedi/jvcl/) (JVCL) and [JEDI Code Library](http://homepages.borland.com/jedi/jcl/) (JCL) - huge open source collection of components based on VCL
  - [CodePedia C++ VCL page](http://www.codepedia.com/1/CppVcl) (no Pascal page yet)

[Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:ボーランド](https://ja.wikipedia.org/wiki/Category:ボーランド "wikilink")

1.  Object Pascalが言語機能としてサポートしている[プロパティが](https://ja.wikipedia.org/wiki/プロパティ_\(プログラミング\) "wikilink")、IDEと親和性が高いことも寄与している。
2.  `TObject`は、Javaにおける暗黙の最上位基底クラスである[オブジェクト型](../Page/オブジェクト型.md "wikilink")に相当するが、Object Pascalにおけるオブジェクト型という用語は意味が異なるので注意されたい。
3.  C++であっても、[Microsoft Foundation Class](../Page/Microsoft_Foundation_Class.md "wikilink") (MFC) などのように単一継承のクラス階層で設計されているライブラリもある。
4.  [System.Classes.TComponent - RAD Studio API Documentation](http://docwiki.embarcadero.com/Libraries/XE7/en/System.Classes.TComponent)
5.
6.  [Delphiにおける一般的なUnicodeへの移行テクニック](https://www.embarcadero.com/images/jp/dm/technical-papers/delphi_unicode_wp_jp.pdf)