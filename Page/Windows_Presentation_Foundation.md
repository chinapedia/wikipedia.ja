> この記事は[Windows Presentation Foundation](https://ja.wikipedia.org/wiki/Windows_Presentation_Foundation)から翻訳されています。


**Windows Presentation Foundation** (**WPF**) は[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した、[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 3.0以降に含まれる[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")[サブシステムである](../Page/システム.md "wikilink")。開発時の[コードネーム](../Page/コードネーム.md "wikilink")は*Avalon*であった\[1\] \[2\]。

## 概要

WPFは、ユーザインタフェースと[ロジック](https://ja.wikipedia.org/wiki/ロジック "wikilink")を明確に区別する一貫した[プログラミング](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")[モデル](https://ja.wikipedia.org/wiki/モデル "wikilink")を提供する。 WPF[アプリケーションは](../Page/アプリケーションソフトウェア.md "wikilink")[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink")で実行するだけでなく[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")上で配置・実行することもできる（ただし類似技術の[Silverlightとは違い](https://ja.wikipedia.org/wiki/Microsoft_Silverlight "wikilink")、[Windowsのみがターゲット環境となる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")）。 WPFによって、ユーザインタフェース、[2Dおよび](https://ja.wikipedia.org/wiki/2次元コンピュータグラフィックス "wikilink")[3Dオブジェクトの描画](../Page/3次元コンピュータグラフィックス.md "wikilink")、[ベクトルグラフィックス](https://ja.wikipedia.org/wiki/ベクトル画像 "wikilink")、[ラスターグラフィックス](https://ja.wikipedia.org/wiki/ビットマップ画像 "wikilink")、[アニメーション](../Page/アニメーション.md "wikilink")、音声および動画の再生などといった表現手法を統一的に利用することができる。WPF以前のWindowsアプリケーション開発では、それらを実現するためには[GDI](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink")/GDI+、[DirectX Graphics](https://ja.wikipedia.org/wiki/DirectX "wikilink") ([Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")他)、[DirectX Audio](https://ja.wikipedia.org/wiki/DirectX "wikilink") ([DirectSound](https://ja.wikipedia.org/wiki/DirectSound "wikilink")他)\[3\] \[4\] 、WindowsマルチメディアAPI、[DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")といった個別の[Windows APIを使って実装しなければならなかった](https://ja.wikipedia.org/wiki/Windows_API "wikilink")。

.NET Framework 3.0は[Windows Vistaに](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[プリインストール](https://ja.wikipedia.org/wiki/プリインストール "wikilink")されており、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") SP2および[Windows Server 2003でも利用できる](../Page/Microsoft_Windows_Server_2003.md "wikilink")。また、[Windows 7には](../Page/Microsoft_Windows_7.md "wikilink").NET Framework 3.5 SP1がプリインストールされている。WPFのバージョン番号は、それが含まれる.NET Frameworkのバージョンと同列に扱われることが多い。例えば.NET 3.0上で動作するものはWPF 3.0、.NET 3.5/3.5 SP1で機能拡張されたものはWPF 3.5、そして.NET 4で機能拡張されたものはWPF 4といった具合である。 なお、[Windows 8には](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink").NET 4.5が、Windows 8.1には.NET 4.5.1が、そして[Windows 10には](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink").NET 4.6がプリインストールされており、WPF 4.5以降を標準的に利用できるが、逆に.NET 3.5以前のコンポーネントは標準で有効になっていないため、WPF 3.0/3.5アプリケーションを動作させるためには明示的なインストールが必要である\[5\]。

## 特徴

次に示すのはWPFの特徴の一部である。

### グラフィックス

全てのグラフィックスは[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")を介して描画される。 また、可能であれば[GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")による[ハードウェアアクセラレーション](https://ja.wikipedia.org/wiki/ハードウェアアクセラレーション "wikilink")が使用される。 これにより、高速かつ高度なグラフィックを統一されたインタフェースで実現・利用することができる。

  - Direct3Dを通して描画することにより、グラフィックスハードウェア上の[GPUに描画処理の一部を任せることが可能になる](../Page/Graphics_Processing_Unit.md "wikilink")。これは（[GDI](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink")/[GDI+](https://ja.wikipedia.org/wiki/GDI+ "wikilink")で問題となっていた）[CPU](../Page/CPU.md "wikilink")の負荷を軽減することにつながる。
  - [ベクトルグラフィックスをサポートする](https://ja.wikipedia.org/wiki/ベクトル画像 "wikilink")。これは損失のない拡大縮小を可能にする。
  - 3Dモデルの[レンダリングや](https://ja.wikipedia.org/wiki/レンダリング_\(コンピュータ\) "wikilink")[相互作用](../Page/相互作用.md "wikilink")をサポートする。`Viewport3D`のようなWPFフレームワーク自体に組み込まれた機能のほか、`D3DImage`のようなDirect3D相互運用性も備えている。
  - 高[DPI環境に標準対応している](https://ja.wikipedia.org/wiki/dpi "wikilink") (System DPI Aware)\[6\]。Per-Monitor DPI Awareに関しては、.NET 4.6.2およびWindows 10 Anniversary Update以降の環境で利用可能である\[7\]\[8\]。

#### Rendering Tier

WPFではグラフィックスハードウェア（[グラフィックスカード](../Page/ビデオカード.md "wikilink")/グラフィックスチップ）のDirectX (Direct3D) 対応レベルに応じて、GPUアクセラレーションの有無が決定される。

WPF 3.5までは下記のようになっている\[9\]。

  - Rendering Tier 0: GPUアクセラレーションなし。DirectX 7.0未満。
  - Rendering Tier 1: 一部GPUアクセラレーションあり。DirectX 7.0以上、DirectX 9.0未満。
  - Rendering Tier 2: ほとんどの機能がGPUアクセラレーションを使う。DirectX 9.0以上（[VRAM](../Page/VRAM.md "wikilink")搭載量120MB以上、[頂点シェーダー](https://ja.wikipedia.org/wiki/頂点シェーダー "wikilink")2.0以上など）。

一方、WPF 4以降は下記のように変更されている\[10\]。

  - Rendering Tier 0: GPUアクセラレーションなし。DirectX 9.0未満。
  - Rendering Tier 1: いくつかの機能はGPUアクセラレーションを使う。DirectX 9.0以上。
  - Rendering Tier 2: ほとんどの機能がGPUアクセラレーションを使う。DirectX 9.0以上（VRAM搭載量120MB以上、頂点シェーダー2.0以上など）。

### 印刷

WPFは標準で[XPSフォーマット](https://ja.wikipedia.org/wiki/XML_Paper_Specification "wikilink") (XPS API) をサポートし、画面に表示されている`UIElement`ツリーをそのまま印刷に使用することができる ([WYSIWYG](../Page/WYSIWYG.md "wikilink"))。なお、WPF同様に、画面描画をGPUアクセラレートする技術に[Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")が存在するが、Direct2D 1.0は印刷デバイスへの出力を直接サポートしないので、こちらはGDI/GDI+などを併用する必要がある。Direct2D 1.1ではメタデータ出力による印刷機能が追加されている。

### 配置

WPFは通常の[スタンドアローン](https://ja.wikipedia.org/wiki/スタンドアローン "wikilink")アプリケーションだけでなく、 (XBAP) として配置することもできる。

  - スタンドアローンアプリケーションは[ClickOnce](https://ja.wikipedia.org/wiki/ClickOnce "wikilink")や[Microsoft Windows Installer](../Page/Microsoft_Windows_Installer.md "wikilink") (MSI) などの[インストーラによって](https://ja.wikipedia.org/wiki/インストール#インストーラ "wikilink")[ローカル](https://ja.wikipedia.org/wiki/ローカル "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")上に配置されるアプリケーションである。
  - XAMLブラウザーアプリケーション (XBAP) は[Internet Explorerなどの](../Page/Internet_Explorer.md "wikilink")[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")によってホストされるアプリケーションである\[11\]。[コンピュータリソースへのアクセスやWPFの機能は一部制限される](https://ja.wikipedia.org/wiki/計算資源 "wikilink")。

### 相互運用性

  - WPFは[Win32](https://ja.wikipedia.org/wiki/Windows_API "wikilink")（ネイティブコード）との相互運用機能を提供する。Win32のコード内からWPFを利用する（例：`HwndHost`クラスの[合成](https://ja.wikipedia.org/wiki/コンポジション "wikilink")、アセンブリの[COM公開など](../Page/Component_Object_Model.md "wikilink")）ことも、WPFからWin32のコードを利用する（例：`HwndHost`クラスの[継承](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")、`D3DImage`クラスなど）ことも可能である。
  - [Windows Formsとの相互運用も可能である](https://ja.wikipedia.org/wiki/Windows_Forms "wikilink")（`ElementHost`、`WindowsFormsHost`クラス）。

なお、WPFのUI上に配置されたWin32あるいはWindows FormsによるレガシーなUIコントロールの描画に対しては、GPUアクセラレーションが効かない（GDI/GDI+によって描画される）ので注意が必要である。

### マルチメディア

  - WPFはブラシ、ペン、幾何図形、変形などの基本的な2Dグラフィックス機能を提供する。
  - WPFで提供される3D機能はDirect3Dのサブセットである。しかし、WPFではよりユーザインタフェースなどの要素に密接に利用することができる。これによって3DのUI、文書、メディアなどが可能になる。
  - 一般的な[ラスター画像](https://ja.wikipedia.org/wiki/ラスター画像 "wikilink")フォーマットをサポートする。
  - [WMV](https://ja.wikipedia.org/wiki/WMV "wikilink")、[MPEG](https://ja.wikipedia.org/wiki/MPEG "wikilink")、[AVI](https://ja.wikipedia.org/wiki/AVI "wikilink")フォーマットの動画をサポートする。
  - 時間ベースのアニメーションをサポートする。これはシステムのパフォーマンスに依存せずアニメーションのスピードを一定に保つ。
  - [ClearType](../Page/ClearType.md "wikilink")を利用したテキストレンダリングをサポートする。また、[OpenType](../Page/OpenType.md "wikilink")フォントの機能もサポートする。WPF 4以降は[DirectWrite](https://ja.wikipedia.org/wiki/DirectWrite "wikilink")コンポーネントとの統合が図られており、縦方向のClearTypeアンチエイリアスが有効となる。

### データバインディング

WPFは次に示す3種類の[データバインディング](https://ja.wikipedia.org/wiki/データバインディング "wikilink")をサポートする。

  - one time: クライアントはサーバ上のアップデートを無視する。
  - one way: クライアントはデータに対して書込み禁止の権限をもつ。
  - two way: クライアントは読み込みと書き込み両方の権限をもつ。

### ユーザインタフェース (UI)

WPFのUIは[XAMLと呼ばれる](../Page/Extensible_Application_Markup_Language.md "wikilink")[XMLベースの](../Page/Extensible_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")で記述され、対応するイベントハンドラなどを[C\#あるいは](../Page/C_Sharp.md "wikilink")[VB.NET](https://ja.wikipedia.org/wiki/VB.NET "wikilink")などの.NET系言語で記述することになる（）。これはWPFの強力な利点のひとつであり、[ロジック](https://ja.wikipedia.org/wiki/ロジック "wikilink")と[インターフェイスを完全に切り離すことができる](https://ja.wikipedia.org/wiki/インタフェース_\(情報技術\) "wikilink")。

  - [ボタン](https://ja.wikipedia.org/wiki/ボタン_\(GUI\) "wikilink")、[メニュー](https://ja.wikipedia.org/wiki/メニュー_\(コンピュータ\) "wikilink")、リストボックスなどといった基本的な組み込み[コントロール](https://ja.wikipedia.org/wiki/コントロール "wikilink")が提供される。
  - UI要素の機能拡張や外観のカスタマイズ（カスタムテンプレートの作成）が、Win32あるいはWindows Formsと比べて容易である。
  - XAML拡張構文（Bindingマークアップ拡張\[12\]）を用いたデータバインディングにより、コードビハインドを記述することなくデータソースもしくはユーザインタフェース変更の反映や連動を実現することもできる。

なお、XAMLを使わずにC\#、VB.NET、[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")などの.NET言語を使い、UIをコードベースで組み立てていくことも可能ではあるが、IDE搭載のXAMLエディターおよびXAMLデザイナーを利用してXAMLベースでUIを記述するほうが直感かつ効率的に階層構造を構築できる。

### 入力

WPFはマウスおよびキーボード入力をサポートするほか、Windows Formsでは標準対応されていないWindowsタッチAPI（[マルチタッチ](https://ja.wikipedia.org/wiki/マルチタッチ "wikilink")）に対するラッパーを提供する。

## 類似技術

[XAML](https://ja.wikipedia.org/wiki/XAML "wikilink")ファミリーとして、いくつかのWPF類似技術がマイクロソフトによって開発されている。

### Silverlight

[Silverlightはマイクロソフトによって](https://ja.wikipedia.org/wiki/Microsoft_Silverlight "wikilink")[Adobe Flashの競合技術として開発された](../Page/Adobe_Flash.md "wikilink")。Silverlightは主にブラウザ上での実行を想定しているのに対し、WPFはよりクライアントPC環境に密着した[スタンドアローン](https://ja.wikipedia.org/wiki/スタンドアローン "wikilink")向け技術である。また、Silverlightで使用される.NET Frameworkは基本的に[.NET Compact Frameworkのような機能制限付きサブセットであるが](https://ja.wikipedia.org/wiki/.NET_Compact_Framework "wikilink")、WPFで使用される.NET FrameworkはWindows PC環境向けのフルセットである点も異なる。

### Windowsストアアプリ

Windows 8/Windows RTにおいて導入された[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリ（[WinRTアプリ](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink")、[Modern UIアプリケーション](https://ja.wikipedia.org/wiki/Modern_UI "wikilink")）はWPF同様XAMLによってユーザインタフェース要素を記述し、WPFに類似したプログラミングモデルを提供する。Windows 10においてWindowsストアアプリの後継として導入された、[ユニバーサルWindowsプラットフォーム](https://ja.wikipedia.org/wiki/ユニバーサルWindowsプラットフォーム "wikilink") (Universal Windows Platform, UWP) アプリケーションも基本は同様である。

## 関連項目

  - [Microsoft Silverlight](https://ja.wikipedia.org/wiki/Microsoft_Silverlight "wikilink")
  - [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") - 従来からWPFアプリケーションの統合開発環境であったが、Visual Studio 2010ではそれ自体がWPFで実装されるに至っている\[13\]。
  - [XAML](https://ja.wikipedia.org/wiki/XAML "wikilink")
  - [Windowsランタイム](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink")
  - [Windows API](https://ja.wikipedia.org/wiki/Windows_API "wikilink")
  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [MVVM](https://ja.wikipedia.org/wiki/MVVM "wikilink")

## 脚注

## 外部リンク

  - [WPF技術情報](http://msdn.microsoft.com/ja-jp/netframework/aa663326.aspx)
  - [Windows Presentation Foundation ホーム](http://www.microsoft.com/products/expression/ja/wpf/default.mspx)
  - [MSDNフォーラム - Windows Presentation Foundation](http://forums.microsoft.com/MSDN-JA/ShowForum.aspx?ForumID=797&SiteID=7)
  - [WPF Tutorial.net](http://www.wpftutorial.net)

{{.NET}}

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink")

1.  [Beta Experience - Avalon](https://www.microsoft.com/betaexperience/nlarchive/bexp2_jajp/issue_1/avalon.aspx)
2.  [WPF（Windows Presentation Foundation）＋XAML入門 前編 (1/4)：CodeZine（コードジン）](https://codezine.jp/article/detail/910)
3.  [DirectX 8.0 の紹介](https://msdn.microsoft.com/ja-jp/library/dd148689.aspx)
4.  [オーディオのリファレンス](https://msdn.microsoft.com/ja-jp/library/cc308058.aspx)
5.  [Windows 8、Windows 8.1、および Windows 10 への .NET Framework 3.5 のインストール](https://msdn.microsoft.com/ja-jp/library/hh506443.aspx)
6.  [アプリの高DPI(High DPI)対応について 第2回 ～ アプリケーションの高DPIへの対応レベル ～ - 田中達彦のブログ - Site Home - MSDN Blogs](http://blogs.msdn.com/b/ttanaka/archive/2014/07/24/dpi-high-dpi-2-dpi.aspx)
7.  [Announcing .NET Framework 4.6.2 | .NET Blog](https://blogs.msdn.microsoft.com/dotnet/2016/08/02/announcing-net-framework-4-6-2/)
8.  [.NET Framework 4.6.2 を発表 – Visual Studio 日本チーム Blog](https://blogs.msdn.microsoft.com/visualstudio_jpn/2016/08/02/net-framework-4-6-2-%E3%82%92%E7%99%BA%E8%A1%A8/)
9.  [Graphics Rendering Tiers: .NET Framework 3.5 - MSDN](https://msdn.microsoft.com/en-us/library/vstudio/ms742196%28v=vs.90%29.aspx)
10. [Graphics Rendering Tiers: .NET Framework 4 - MSDN](https://msdn.microsoft.com/en-us/library/vstudio/ms742196%28v=vs.100%29.aspx)
11. [Windows Presentation Foundation XAML ブラウザ アプリケーションの概要](https://msdn.microsoft.com/ja-jp/library/aa970060%28v=vs.90%29.aspx)
12. [バインディングのマークアップ拡張機能](https://msdn.microsoft.com/ja-jp/library/ms750413%28v=vs.90%29.aspx)
13. [WPF UIを使ったVisual Studio 2010のスクリーンショットが初披露](http://www.infoq.com/jp/news/2009/03/VisualStudio2010-WPF)