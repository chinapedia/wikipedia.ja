> この記事は[InstallShield](https://ja.wikipedia.org/wiki/InstallShield)から翻訳されています。


**InstallShield**（インストールシールド）は、

1.  Viresh Bhatiaとリック・ハロルドが設立した企業。[2004年](../Page/2004年.md "wikilink")に[マクロビジョン](https://ja.wikipedia.org/wiki/マクロビジョン "wikilink")に買収された。
2.  上記の企業が開発した、[インストーラまたは](../Page/インストール.md "wikilink")[ソフトウェアパッケージを生成する](../Page/パッケージソフトウェア.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")。

ここでは後者について説明する。

## 概要

当初の名称はInstallShield。開発元がマクロビジョンに買収された[2004年](../Page/2004年.md "wikilink")、同社のソフトウェアブランドである"FLEXnet"を冠して、FLEXnet InstallShieldとして提供された。[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")に同社のソフトウェア部門が（現）として独立し、名称もInstallShieldに戻して開発が行われている。

[Windows版のInstallShieldは主に](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、

1.  [MSIと独自の](../Page/Microsoft_Windows_Installer.md "wikilink")[スクリプト言語](../Page/スクリプト言語.md "wikilink")であるInstallScriptの、いずれかを用いた[Windows Installer](../Page/Microsoft_Windows_Installer.md "wikilink") (MSI) 形式のインストーラ
2.  InstallScriptを用いて[イベントベースの](../Page/イベント_\(プログラミング\).md "wikilink")[スクリプト](../Page/スクリプト.md "wikilink")またはsetup.exeの実行可能な[ファイルを生成する独自のインストーラ](../Page/ファイル_\(コンピュータ\).md "wikilink")

の2種類のインストーラを作成できる。

## バージョンの変遷

オリジナル製品の各種バージョンの変遷は以下の通り\[1\]。

  - INSTALLSHIELD 2015
  - INSTALLSHIELD 2016
  - INSTALLSHIELD 2018
  - INSTALLSHIELD 2018 R2
  - INSTALLSHIELD 2019
  - INSTALLSHIELD 2019 R3

[Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") 2012以降には、無償版のLimited Editionを用いたインストーラのプロジェクトテンプレートが同梱されている。使用を開始するにはユーザー登録とInstallShieldのインストールおよびアクティベーションが必要となる。Visual Studio Communityエディションはサポートされていない。

## Windows10でのInstallShield旧バージョンの挙動

Windows10では、WindowsXPの頃に各社のパッケージソフトウェア製品のインストーラとして採用されていた（一部に16bitコードが含まれる）InstallShield 3やInstallShield 5でパッケージされたインストーラからのインストールが（セキュリティ上の安全を確保するなどの目的もあって、当該の各社パッケージソフトウェア製品の正規ライセンス保持者であっても）できないように仕様変更された。

このため、例えばWindows95,98,ME,2000,XP,Vistaなどでは正常にインストールできていたゲームなどの製品でも、Windows10ではインストーラが起動しない（動かないのはインストーラであって、インストールに成功すれば当該ソフトウェア製品そのものは動く）という事態が発生することがある。このためのバイパス用インストーラとして、Windows互換のオープンソースOSとして開発されている[ReactOS](../Page/ReactOS.md "wikilink")用に32bitコードに書き換えた汎用インストーラ（Windows上でも動作する）がNathan Linebackによって開発され、オンラインで無償配布されている\[2\]。

  - **InstallSheild Engine 3.0** … InstallShield 3でパッケージ化されたアプリケーション向け。
  - **InstallShield Launcher 5** … InstallShield 5でパッケージ化されたアプリケーション向け。

## 関連項目

  - [NSIS](https://ja.wikipedia.org/wiki/Nullsoft_Scriptable_Install_System "wikilink")
  - [Inno Setup](https://ja.wikipedia.org/wiki/Inno_Setup "wikilink")
  - [Microsoft Windows Installer](../Page/Microsoft_Windows_Installer.md "wikilink")
  - [WiX](https://ja.wikipedia.org/wiki/WiX "wikilink")
  - [Windows10](https://ja.wikipedia.org/wiki/Windows10 "wikilink")
  - [インストーラ](https://ja.wikipedia.org/wiki/インストール#共通のインストーラ "wikilink")

## 脚注

## 外部リンク

  - [InstallShieldNew and Enhanced Features Added by Release](https://www.flexerasoftware.com/install/products/installshield.html) - 開発元Flexera社によるInstallShieldの製品情報
  - [InstallShieldの製品情報](https://www.networld.co.jp/product/is/) - 日本代理店による製品情報
  - [32-Bit setup Files(Nathan's Toasty Technology page)](http://toastytech.com/files/setup.html) - InstallShield 3,5でパッケージされたソフトウェアをWindows10などでもインストール可能にする汎用インストーラ
  - [unshield (DOS/DJGPP)](http://blairdude.googlepages.com/unshield) InstallShieldの独自の圧縮アルゴリズムを用いた[CAB](../Page/CAB.md "wikilink")ファイルの展開を行うプロジェクト。

[Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink")

1.  2015-2019 R3に関する情報はより
2.