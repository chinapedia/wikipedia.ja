> この記事は[Qt](https://ja.wikipedia.org/wiki/Qt)から翻訳されています。


**Qt**（キュート）とは、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")である。とによって開発されている。

## 性能

キュー・ティーと発音されることもあるが公式にはキュートである。[GUIツールキットとして広く知られているQtであるが](../Page/ウィジェット・ツールキット.md "wikilink")、コンソールツールやサーバのような非GUIプログラムでも広く使用されている。

ライセンスには商用版とオープンソース版があり、現在のオープンソース版のライセンスは[LGPLおよび](../Page/GNU_Lesser_General_Public_License.md "wikilink")[GPLである](../Page/GNU_General_Public_License.md "wikilink")。商用版を購入するとQt商用ライセンス（Qt Commercial License）でソフトウェアを開発することができる。LGPL版は、2009年3月にリリースされたQt 4.5から提供され始めた。これによりQtは営利企業にとってもより使いやすいライブラリーとなった。

QtはC++で開発されており、単独のソースコードにより[X Window System](../Page/X_Window_System.md "wikilink")（Linux、UNIX等）、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[組み込みシステム](../Page/組み込みシステム.md "wikilink")といった様々な[プラットフォーム上で稼働するアプリケーションの開発が可能である](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。またコミュニティーにより多言語の[バインディングが開発されており](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")からQtを利用できるようにしたQt Jambi、さらにQtを[Ruby](../Page/Ruby.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[C\#などから利用できるようにした](../Page/C_Sharp.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[APIが存在する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

このように開発が容易であり高速、スタイリッシュなQtはライセンスが多様なこともあり、[KDE](../Page/KDE.md "wikilink")を始めとするオープンソースのアプリケーションに限らず、商業アプリケーションでの採用例も多く様々な分野で使用されている。

[OpenGL](../Page/OpenGL.md "wikilink")や[SVG](../Page/Scalable_Vector_Graphics.md "wikilink")、[XMLといった最新技術にも対応している他](../Page/Extensible_Markup_Language.md "wikilink")、日本語を含む多バイト文字入力フレームワークへも対応している。

## オープンソース版

GPLまたはLGPLが適用される。LGPLは、バージョン4.5から適用できる。Windowsや多くの[Unix系](../Page/Unix系.md "wikilink")OS、macOS向け、あるいはEmbedded Linux、Windows CE、Symbian（Qt4.6より）向けにパッケージが配布されている。

## 設計

### モジュール

Qt 5のモジュール群の一部を以下に示す\[1\]。

#### Qt Essentials

  - Qt Core
    [GUI向け以外のコアとなる](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[クラス](../Page/クラス.md "wikilink")を保持する。
  - Qt Gui
    GUIのメインとなるクラスを保持する。[OpenGL](../Page/OpenGL.md "wikilink")を含む。
  - Qt Multimedia
    音楽、動画、ラジオ、カメラなどのマルチメディア機能を実装する。
  - Qt Multimedia Widgets
    マルチメディア機能を実現するウィジェット群。
  - Qt Network
    ネットワークプログラミングを簡単にするためのクラス群。
  - Qt QML
    QMLと[JavaScript](../Page/JavaScript.md "wikilink")に関するクラスを保持している。
  - Qt Quick
    カスタムユーザーインターフェイスを備えた高度に動的なアプリケーションを構築するためのフレームワーク。
  - Qt Quick Controls
    デスクトップ風のユーザーインターフェイスを作るためのQt QuickベースのUIコントロール群。
  - Qt Quick Dialogs
    Qt Quickアプリケーションにシステムダイアログを提供する。
  - Qt Quick Layouts
    ユーザーインターフェイスにQt Quick 2ベースのアイテムを使用するアイテムのレイアウト。
  - Qt SQL
    [SQL](../Page/SQL.md "wikilink")を使うデータベースのためのクラス群。
  - Qt Test
    Qtアプリケーションとライブラリのユニットテストのためのクラス群。
  - Qt Widgets
    Qt GuiをC++ウィジェットで拡張するためのクラス群。

#### Qt Add-Ons

  - Active Qt
    Windowsで[ActiveX](../Page/ActiveX.md "wikilink")やCOMを使うアプリケーションのためのクラス群。
  - Qt 3D
    2Dや3Dレンダリングをサポートする近リアルタイムシミュレーションシステムのための機能。
  - Qt Android Extras
    [Android](../Page/Android.md "wikilink")固有の機能を使うためのAPI。
  - Qt Bluetooth
    [Bluetooth](../Page/Bluetooth.md "wikilink")ハードウェアへのアクセスを提供する。
  - Qt Canvas 3D
    JavaScriptを使ったQt QuickアプリケーションからOpenGL風の3D描画を可能にする。
  - Qt Concurrent
    低レベルな操作なしに[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")プログラムを書くためのクラス群。
  - Qt D-Bus
    [D-Bus](../Page/D-Bus.md "wikilink")プロトコルを使用した[プロセス間通信](../Page/プロセス間通信.md "wikilink")のためのクラス群。
  - Qt Gamepad
    Qtアプリケーションの[ゲームパッド](../Page/ゲームパッド.md "wikilink")ハードウェアのサポートを可能にする。
  - Qt Graphical Effects
    Qt Quick 2で使うためのグラフィカルエフェクト。
  - Qt Image Formats
    Qt Guiでサポートされていない画像フォーマットのためのプラグイン群。
  - Qt Location
    QMLアプリケーションで地図の表示や道案内やコンテンツの配置をする。
  - Qt Mac Extras
    [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")固有の機能を使うためのAPI。
  - Qt NFC
    [NFCハードウェアへのアクセスを提供する](../Page/近距離無線通信.md "wikilink")。
  - Qt Positioning
    スマートフォンなどで位置情報を提供する。
  - Qt Print Support
    印刷を簡単にするためのクラス群。
  - Qt Purchasing
    Qtアプリケーションのアプリ内課金を可能にする。
  - Qt Sensors
    センサーハードウェアへのアクセスとモーションジェスチャーの認識を提供する。
  - Qt Serial Port
    ハードウェアと仮想シリアルポートへのアクセスを提供する。
  - Qt SVG
    [SVGファイルの内容を表示するクラスを保持する](../Page/Scalable_Vector_Graphics.md "wikilink")。SVG 1.2 Tinyの機能をサポートする。
  - Qt WebEngine
    アプリケーションにウェブコンテンツを埋め込むためのクラスと関数群。
  - Qt WebView
    QMLアプリケーションでウェブコンテンツをプラットフォームのネイティブAPIを使い、アプリケーションに完全な[ウェブレンダリングエンジンを含むことなく表示する](https://ja.wikipedia.org/wiki/HTMLレンダリングエンジン "wikilink")。
  - Qt Windows Extras
    [Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")固有の機能を使うためのAPI。
  - Qt X11 Extras
    [X11](https://ja.wikipedia.org/wiki/X11 "wikilink")固有の機能を使うためのAPI。
  - Qt XML
    [SAXおよび](../Page/Simple_API_for_XML.md "wikilink")[DOMインターフェイスを実装](../Page/Document_Object_Model.md "wikilink")。

### ネイティブUI描画APIの使用

かつてQtはプラットフォームのネイティブの見た目をエミュレートしていたため、ときどきエミュレーションが不完全な場合に微妙な不一致が発生することもあったが、最近のバージョンのQtはそれぞれのプラットフォームのネイティブAPIでQtコントロールの描画を行うため、そのような問題に苦しめられることもなくなった\[2\]。

### メタオブジェクトコンパイラ

**moc**と呼ばれるメタオブジェクトコンパイラは、Qtプログラムのソースコードを入力として実行されるツールである。C++のソースコードにマクロを1、2行記述するだけで、mocがそれを解釈しプログラムで使用されるクラスについての「メタ情報」とともに追加のC++コードを挿入して出力する。このシステムにより、ネイティブのC++では利用できなかったり実現しようとすると煩雑なシグナル&スロットシステムやメタプログラミング、非同期関数呼び出しなどを簡単に利用できる。

### シグナル&スロット

オブジェクト間でコミュニケーションする時に[Observer パターンを簡単に使えるようにするための仕組み](../Page/Observer_パターン.md "wikilink")。あるオブジェクトがシグナルを発信するとそのシグナルに接続してあるオブジェクトのスロット(関数)が呼ばれる。発信側は受信側を知る必要がなく、インクルード関係をシンプルに保つことができる。

### バインディング

Qtはさまざまな言語用の[バインディングを持っており](https://ja.wikipedia.org/wiki/束縛_\(情報工学\)#言語束縛 "wikilink")\[3\]、機能セットの一部または全部を実装している。

### Qtによるhello world

``` cpp
#include <QtGui>

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);
    QLabel label("Hello, world!");
    label.show();
    return app.exec();
}
```

### Qt hello world プログラムのコンパイルおよび実行

1.  Helloフォルダを作る
2.  上のプログラムをHello.cppとしてHelloフォルダに保存する
3.  Helloフォルダで以下を実行
    1.  qmake -project
    2.  qmake
    3.  make（または gmake や nmake 等。OSおよびコンパイラごとに異なる）
4.  実行する ./release/Hello (Windowsなら release\\Hello.exe)

## 開発環境・デザインツールなど

クロスプラットフォームの統合開発環境、GUI エディタのQt Designer、翻訳支援ツールのQt Linguist、リファレンスドキュメントビューアのQt Assistant等の開発支援ツールが付属しており、これらを使用することで高速な開発が可能となっている。その他のものとしてWindowsの[Visual Studioでの開発を可能にするプラグインVisual](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") Studio Add-inが用意されている。また[Eclipse上で開発を可能にするQt](../Page/Eclipse_\(統合開発環境\).md "wikilink") Eclipse Integrationも用意されている。また、Unix/X11（Linuxなど）では、[KDevelop](../Page/KDevelop.md "wikilink")が使用できる。

Qt/UNIX上では[GCC](../Page/GNUコンパイラコレクション.md "wikilink")、Qt/Windowsでは[Microsoft Visual Studio上のコンパイラが使える他](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")、[MinGW](../Page/MinGW.md "wikilink")等のコンパイラでの開発も可能である。

## 歴史

Quasar Technologies社のHaavard Nord と Eirik Chambe-Eng（Qtの開発者であり、現在TrolltechのCEO、および社長）は、1991年にQtの開発をはじめた（Quasar Technologies社はその後Troll Tech社、Trolltech社へと社名を変更していく）。

Qtと名づけられたのは、Qという文字がHaavardの使っていた[Emacs](../Page/Emacs.md "wikilink")のフォントの中でもっとも美しく見えたという理由からである。tはtoolkitの略語である。

KDEがLinuxで主要なデスクトップ環境になることが明確になった1998年頃、KDEがQtベースで開発されていることから、フリーソフトウェアであるKDEがライセンス上、Trolltech社のQPLに抵触する可能性が懸念された。

背景は以下の通りである。

まずバージョン1.45まではQtのソースコードは、FreeQt licenseでリリースされていた。しかしバージョン2.0からは、このライセンスはQ Public License (QPL) に変更された。Free Software Foundationによると、QPLはGPLとは矛盾するライセンスであった。この問題はKDE側とTrolltech社との間で協議されることになり、結果、KDE Free Qt Foundationが発足されることになった。結果、QtはQPLとGPLの[デュアルライセンス](../Page/デュアルライセンス.md "wikilink")で配布されることが決まり、この問題は完全に解決した。さらに、将来、Trolltechが何らかの理由で新しいオープンソース版を作成することができなくなった場合でも、KDE Free Qt FoundationによりQtの開発を続けることが保証されることになった。

最初の二つのバージョンでは、プラットフォームはUNIX及びWindowsプラットホームがサポートされた。当初はQt/X11上でのプロプライエタリライセンスはWindowsプラットホームでは使用できず、WindowsでQtを使用するときはQPLエディションのQtを購入する必要があった。

2001年の終わりにTrolltech社はバージョン3.0をリリースした。バージョン3.0からは[Mac OS Xプラットフォームもサポート対象となった](https://ja.wikipedia.org/wiki/macOS "wikilink")。Mac OS X上ではGPLで配布されている。

2005年6月にTrolltech社はQtバージョン4をリリースした。Qt4では Windows上でも、QtをGPLでソースコードを公開することになった。これにより、Windows, Mac OS, Unixの全てのプラットフォームでGPLのフリーオープンソースアプリケーションが開発できるようになった。またこのバージョンからコア、GUI、ネットワーク、XML、OpenGLなど、機能別にモジュールが分割された。不要な機能は読み込まれないため、メモリの節約になる。その一方、Qt4はQt2および3とソースコードに互換性がない。このため現在でもQt3を使い続けるユーザーは多い。またKDEは3から4へバージョンアップする際、ソースコードの全面的な書き直しが必要となったためリリースが大幅に遅れた。

2009年3月にLGPLが適用となるバージョン4.5が発表された。これはTrolltech社がNOKIA社に買収されたことにともなうもので、組み込み実績の多いQtを[プロプライエタリなソフトウェアでもより使用しやすくするためである](../Page/プロプライエタリ・ソフトウェア.md "wikilink")。バージョン4.5においても、Qtの商用ライセンスは存続し、LGPLですら許容できない（[リバースエンジニアリング](../Page/リバースエンジニアリング.md "wikilink")禁止条項を含むなど）場合は商用ライセンスを使用する必要がある。

2009年5月には、[Git](../Page/Git.md "wikilink")リポジトリが公開され、ユーザからのパッチのコミットがより簡易になった。

なお、初期のバージョンにおいては日本語固有の処理にバグがあり、ライセンス上それを修正し配付することが困難であったため、QtおよびKDEの普及が日本語圏において遅れることとなった。この問題はTrolltech社（当時）が日本語パッチを特別に認めることにより解決した。

Chromiumを援用することがQt5.6で決まったものの、その性能の悪さからすぐに批判され、現在ではQtWebEngineとQtWebKitが混在している。Qt WebBrowser\[4\]も思ったほどの普及になっていない。これはChromiumの採用バージョンが最新よりかなり遅れることが原因である。

2012年8月9日にがノキアからQtを買収した\[5\]。[Android](../Page/Android.md "wikilink")や[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、[Windows 8へのQtの早急な対応を目標に](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")、約125人のQt開発者たちがディジアに移籍された\[6\]\[7\]。

## Qtを使用している主なソフトウェア

  - [Autodesk Maya](https://ja.wikipedia.org/wiki/Autodesk_Maya "wikilink") 2011以降 - [3DCGソフトウェア](https://ja.wikipedia.org/wiki/3DCGソフトウェア "wikilink")
  - [Avidemux](https://ja.wikipedia.org/wiki/Avidemux "wikilink") - [動画編集ソフトウェア](https://ja.wikipedia.org/wiki/動画編集ソフトウェア "wikilink")
  - [FreeCAD](https://ja.wikipedia.org/wiki/FreeCAD "wikilink") - [CAD](../Page/CAD.md "wikilink")ソフトウェア
  - [Google Earth](https://ja.wikipedia.org/wiki/Google_Earth "wikilink") - [仮想地球](https://ja.wikipedia.org/wiki/仮想地球 "wikilink")ソフトウェア
  - [KDE](../Page/KDE.md "wikilink") - [デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")
  - [Muse](../Page/Muse.md "wikilink") - シーケンサ
  - [MuseScore](https://ja.wikipedia.org/wiki/MuseScore_\(楽譜作成ソフト\) "wikilink") - [楽譜作成ソフトウェア](../Page/楽譜作成ソフトウェア.md "wikilink")
  - [Nuke](https://ja.wikipedia.org/wiki/Nuke "wikilink") - [デジタル合成](../Page/デジタル合成.md "wikilink")ソフト
  - [ParaView](https://ja.wikipedia.org/wiki/ParaView "wikilink") - [データ可視化](https://ja.wikipedia.org/wiki/データ可視化 "wikilink")ソフト
  - [QGIS](https://ja.wikipedia.org/wiki/QGIS "wikilink") - [GISソフト](../Page/地理情報システム.md "wikilink")
  - [Rosegarden](../Page/Rosegarden.md "wikilink") - [DAWソフトウェア](../Page/デジタル・オーディオ・ワークステーション.md "wikilink")
  - [Skype](../Page/Skype.md "wikilink") - コミュニケーションソフト
  - [モバイルWnn](../Page/Wnn.md "wikilink") - [日本語入力](https://ja.wikipedia.org/wiki/日本語入力 "wikilink")システム
  - [QMP3Gain](https://ja.wikipedia.org/wiki/sourceforge:projects/qmp3gain/ "wikilink") - mp3音量均一化ソフト
  - [Qt Brynhildr](https://github.com/funfun-dc5/qtbrynhildr/) - [リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")ソフト

## Qtを利用できるプログラミング言語

QtはGUIツールキットとして広く使われているため、メイン開発言語であるC++以外の多数のプログラミング言語バインディングが存在する。

  - [node-qt](https://ja.wikipedia.org/wiki/node-qt "wikilink") - Node.jsバインディング
  - [PyQt](https://ja.wikipedia.org/wiki/PyQt "wikilink") - 古くから使われているPythonバインディング。GPL。
  - [PySide](https://ja.wikipedia.org/wiki/PySide "wikilink") - ノキア社が開発したPythonバインディング。LGPL。
  - [QtRuby](https://ja.wikipedia.org/wiki/QtRuby "wikilink") - Rubyバインディング
  - [RingQt](https://ja.wikipedia.org/wiki/RingQt "wikilink") - [Ring用のQt](https://ja.wikipedia.org/wiki/Ring_\(プログラミング言語\) "wikilink") バインディングと Ring 向けの Qt 関連のフォームデザイナ、ツールが処理系に標準添付されている。

## 脚注

<references/>

## 関連項目

  - [ウィジェット・ツールキット](../Page/ウィジェット・ツールキット.md "wikilink")

## 外部リンク

  - [The Qt Company 公式サイト](https://www.qt.io/jp)
  - [Qt Blog (日本語ページ）](https://blog.qt.io/jp/)
  - [日本 Qt ユーザー会](http://qt-users.jp/)
  - [（代理店）SRAのQtサイト](http://www.sra.co.jp/qt/)
  - [（代理店）アイ・エス・ビーのQtサイト](http://www.isb.co.jp/qt/)

[Category:Qt](https://ja.wikipedia.org/wiki/Category:Qt "wikilink") [Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:1992年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1992年のソフトウェア "wikilink")

1.
2.
3.  [Language Bindings - Qt Wiki](http://wiki.qt.io/Language_Bindings)
4.  [Qt WebBrowser | Qt WebBrowser Manual](https://doc.qt.io/QtWebBrowser/)
5.  [Digia to acquire Qt from Nokia](https://web.archive.org/web/20151012094731/http://www.digia.com/en/Home/Company/News/Digia-to-acquire-Qt-from-Nokia/)
6.  <http://blog.qt.nokia.com/2012/08/09/investment-in-qt-planned-to-continue-digia/>
7.  <http://blog.qt.nokia.com/2012/08/09/digia-extends-its-commitment-to-qt-with-plans-to-acquire-full-qt-software-technology-and-business-from-nokia/>