> この記事は[Windows Driver Model](https://ja.wikipedia.org/wiki/Windows_Driver_Model)から翻訳されています。


**Windows Driver Model** (**WDM**) とは、[Windows 98と](../Page/Microsoft_Windows_98.md "wikilink")[Windows 2000で導入された](../Page/Microsoft_Windows_2000.md "wikilink")[デバイスドライバー](https://ja.wikipedia.org/wiki/デバイスドライバー "wikilink")のフレームワークであり、それ以前の[Windowsで使われていた](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[VxDなどを代替するものとして登場した](../Page/仮想デバイスドライバ.md "wikilink")。導入当時は**Win32 Driver Model**と呼ばれていた。

## 概要

WDMドライバーは複雑に階層化されており、\[1\] (I/O Request Packet, IRP) を使って相互に通信する。WDMは、各種要求を標準化し書くべきコード量を削減した統一的ドライバーモデルとして、Windows 98とWindows 2000向けに定義された。WDMドライバーは、それ以前のWindows（[Windows 95や](../Page/Microsoft_Windows_95.md "wikilink")[Windows 3.1](../Page/Microsoft_Windows_3.x.md "wikilink")、[Windows NT 4.0など](../Page/Microsoft_Windows_NT.md "wikilink")）では動作しない。WDMに従ったドライバーは、Windows 98 / Windows 98 Second Edition / [Windows Me](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink") / Windows 2000 / [Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") / [Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink") / [Windows Vistaが動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ベースの[コンピュータ](../Page/コンピュータ.md "wikilink")で[バイナリ互換と](../Page/Application_Binary_Interface.md "wikilink")[ソースコード互換を実現する](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")。WDMは[前方互換](https://ja.wikipedia.org/wiki/前方互換 "wikilink")を保つよう設計されている。すなわち、ある版のWDMはそれ以前の版のWDMに従って書かれたドライバーと互換性を有する。そのようなWDMドライバーは新たな[OS機能を利用することはできないが](../Page/オペレーティングシステム.md "wikilink")、新たなOS上でも動作自体は可能である。逆方向の互換性はない。すなわち、新しい版に従ったドライバーを古いOSで使おうとすると失敗する。例えば、Windows XPのWDMはWindows 2000向けドライバーをロード可能だが、Windows XPの新規機能は使えない。逆にWindows 2000のWDMはWindows XP向けドライバーをロードできない。

WDMはWindows 2000の[カーネルモード](https://ja.wikipedia.org/wiki/カーネルモード "wikilink")ドライバーの中間層として存在し、Windows向けドライバー作成に際しての機能を増やし、ドライバーを書きやすくすることを意図していた。WDMはWindows 98とWindows 2000の間でバイナリ互換性およびソースコード互換性を保つよう設計された。WDMドライバーは以下のように分類される。

### ファンクションドライバー

**ファンクションドライバー**は、デバイス用の主要なドライバーである。ファンクションドライバーはデバイスベンダーが作成するのが普通である。1つのドライバーが複数のデバイスを制御することもできる。

  - クラスドライバー
    他のクラスドライバーやミニポートドライバーをその上に構築できる、一種のフレームワークドライバー\[2\]。WDMアーキテクチャの異なる階層間の[インターフェイスを提供する](../Page/インタフェース_\(情報技術\).md "wikilink")。異なるクラス階層に属するドライバー間の共通機能はクラスドライバーとして書くことができ、それを他のクラスドライバーやミニポートドライバーから利用する。クラスドライバーの最下層側はミニポートドライバーとのインターフェイスを持ち、最上層側はOSとのインターフェイスを持つ。クラスドライバーは必要に応じて、動的にロード / アンロードできる。[ハードウェア](../Page/ハードウェア.md "wikilink")や[バス固有の機能というよりも](../Page/バス_\(コンピュータ\).md "wikilink")、クラス固有の機能を持つことが多く、場合によっては単なる列挙 (enumeration) のような機能しか持たないこともある。
  - ミニポートドライバー
    [USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[サウンドカード](../Page/サウンドカード.md "wikilink")、[SCSI](../Page/Small_Computer_System_Interface.md "wikilink")、[ネットワークカード](../Page/ネットワークカード.md "wikilink")などに対応したファンクションドライバー。これらはWindowsのバージョン間でバイナリおよびソースコード互換性があり、ハードウェア固有のものだが、ハードウェアへのアクセス制御を固有バスのクラスドライバー経由で行なう。

### バスドライバー

**バスドライバー**は、バスコントローラー、バスアダプター、バスブリッジなどを扱う。[マイクロソフト](../Page/マイクロソフト.md "wikilink")が提供しているバスドライバーとしては、[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")、[PnPISA](../Page/プラグアンドプレイ.md "wikilink")、SCSI、USB、[IEEE 1394などがある](../Page/IEEE_1394.md "wikilink")。各ベンダーは必要に応じて独自のバスドライバーを作成できる。バスドライバーは、同じタイプのバスが複数あれば、それらをまとめて制御できる。

### フィルタードライバー

**フィルタードライバー**はオプション的なドライバーであり、機能を付加したりデバイスの動作を変更したりするドライバーや、デバイスとは関係ないドライバーが属する。フィルタードライバーは同時に複数のサービスを提供できる。上位層のフィルタードライバーは、デバイス用ファンクションドライバーの上位に位置し、下位層のフィルタードライバーはファンクションドライバーとバスドライバーの中間に位置する。

  - ドライバーサービス
    カーネルレベルのフィルタードライバーであり、[Windowsサービス](../Page/Windowsサービス.md "wikilink")として実装され、アプリケーションからデバイスを使えるようにする。

## VxD、WDMとWindows 98

Windows 98系OS (98, 98SE, Me) は、WDMと[VxDの両標準をサポートしている](../Page/仮想デバイスドライバ.md "wikilink")。これらは同じハードウェアに対して異なる機能を提供するが、Windows Me登場以降の世代のハードウェアではWDMの方が機能が豊富なものがあった。例えば、[TVチューナー](../Page/TVチューナー.md "wikilink")カードをVxDドライバーで使うと画像の解像度が384×288ピクセルだったものが、同じカードをWDMドライバーで使うと768×576ピクセルが可能となることがある。これは、WDMの一部であるによる改善である。

しかし、改良された機能を使用するにはハードウェアベンダーの努力が不可欠である。 古いハードウェアではVxDドライバーでは持っていた機能の一部が、WDMドライバーには提供されずに開発が終了されたものも。また、[Windows 9x系のWDMは](../Page/Windows_9x系.md "wikilink")*Ntkern.vxd*という一種のVxDドライバーがNTカーネルをエミュレートする形であったため、逆にパフォーマンスや安定性で不利になることもあった。

## 批判

Windows Driver Modelは、それ以前の[VxDとWindows](../Page/仮想デバイスドライバ.md "wikilink") NTドライバーモデルを大幅に改良したが、以下のような点でドライバー開発者から批判されている\[3\]。

  - WDMは習熟が困難である。

  - イベントと[プラグアンドプレイ](../Page/プラグアンドプレイ.md "wikilink")の連携が難しい。これは、ドライバーコードにおけるバグのせいでWindowsマシンが正しくスリープあるいは復帰できないといった様々な状況を引き起こす。

  - [I/Oの取り消しがほぼ不可能である](../Page/入出力.md "wikilink")。

  - 全てのドライバーに似たような大量のサポートコードを書く必要がある。

  - 純粋な[ユーザーモード](https://ja.wikipedia.org/wiki/ユーザーモード "wikilink")ドライバーを書くためのサポートが存在しない。

また、マイクロソフトが提供する[文書やサンプルについてもいくつかの問題が指摘されている](../Page/ソフトウェアドキュメンテーション.md "wikilink")。

このような問題があるため、マイクロソフトはWDMの代替となる新たなフレームワーク[Windows Driver Foundationをリリースした](../Page/Windows_Driver_Foundation.md "wikilink")。これには、[Kernel-Mode Driver Framework](https://ja.wikipedia.org/wiki/Kernel-Mode_Driver_Framework "wikilink") (KMDF) と[User-Mode Driver Framework](https://ja.wikipedia.org/wiki/User-Mode_Driver_Framework "wikilink") (UMDF) が含まれる。[Windows VistaはWDMとWindows](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") Driver Foundationの両方をサポートしている。KMDFはWindows XPとWindows 2000向けにダウンロード可能であり、UMDFはWindows XP向けにダウンロード可能となっている。

## ドライバー署名

Windowsドライバーはセキュリティ上の配慮から、正式な作成者を確認することのできる[デジタル署名](../Page/デジタル署名.md "wikilink")を行なってリリースすることが推奨されている。デジタル署名の手段としては (Windows Hardware Quality Labs) 署名もしくは署名（自己署名）が存在する。Windows Vista以降の32bit版OSでは署名のないドライバーをインストールしようとした際に警告が表示されるものの、インストールおよび動作は可能となる。一方、64bit版OSでは署名のない[カーネルモード](https://ja.wikipedia.org/wiki/カーネルモード "wikilink")のドライバーを動作させることはできない\[4\]。署名のないドライバーをインストールおよび動作できるテストモードも用意されているが、これは開発者向けの内部テスト目的であり、エンドユーザー環境では推奨されない\[5\]。

[Windows 8では](https://ja.wikipedia.org/wiki/Windows_8 "wikilink")、64bit版においてカーネルモードだけでなく[ユーザーモード](https://ja.wikipedia.org/wiki/ユーザーモード "wikilink")のドライバーも署名が必須となった\[6\]。

[Windows 10では](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")2016年1月1日の[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")証明書廃止ポリシーを受けて、カーネルモードのドライバーは32bit/64bitにかかわらず[マイクロソフト](../Page/マイクロソフト.md "wikilink")社による署名が必須となることが予定されている。ユーザーモードのドライバーに関しては、[Windows 8.1同様にAuthenticode署名が利用可能である](https://ja.wikipedia.org/wiki/Windows_8.1 "wikilink")\[7\]。

## 関連項目

  - [Windows Driver Foundation](../Page/Windows_Driver_Foundation.md "wikilink") (WDF)
  - [Windows Display Driver Model](https://ja.wikipedia.org/wiki/Windows_Display_Driver_Model "wikilink") (WDDM)

## 脚注

## 参考文献

  - Finnel, Lynn (2000). *MCSE Exam 70-215, Microsoft Windows 2000 Server*. Microsoft Press. ISBN 1-57231-903-8.
  - Oney, Walter (2003). *Programming the Windows Driver Model*, Microsoft Press, ISBN 0-7356-1803-8.

## 外部リンク

  - [Windows driver API basics](http://www.staudio.de/kb/english/drivers/) - サウンドカード用ドライバーの基本（WDM、[ASIO](../Page/ASIO.md "wikilink")、[MME](https://ja.wikipedia.org/wiki/Windows_Multimedia_Extensions "wikilink")、[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")など）
  - [Channel 9 Video](http://channel9.msdn.com/Showpost.aspx?postid=156316) - マイクロソフトの Device Management and Installation チームへのインタビュー。主に[プラグアンドプレイ](../Page/プラグアンドプレイ.md "wikilink")について
  - [DirectX 8.1 の新機能](http://msdn.net/library/ja/default.asp?url=/library/ja/jpdndxgen/htm/WhatsNewDX81.asp) - [Broadcast Driver Architectureについて](https://ja.wikipedia.org/wiki/Broadcast_Driver_Architecture "wikilink")

[Category:デバイスドライバ](https://ja.wikipedia.org/wiki/Category:デバイスドライバ "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")

1.  [I/O 要求パケット (Windows Drivers)](https://msdn.microsoft.com/ja-jp/library/windows/hardware/hh439638.aspx)
2.  [ASCII.jp：Windowsを動かすデバイスドライバーの仕組み 前編 (1/4)｜基礎から覚える 最新OSのアーキテクチャー](http://ascii.jp/elem/000/000/633/633118/)
3.  [Introducing Driver Frameworks for Windows May 6](http://www.wd-3.com/archive/FrameworkIntro.htm)
4.  [64bit Windows時代到来：第4回　64bit版デバイス・ドライバ (1/3) - ＠IT](http://www.atmarkit.co.jp/ait/articles/1009/09/news112.html)
5.  [ドライバーのデジタル署名の基礎 - Japan WDK Support Blog - Site Home - MSDN Blogs](http://blogs.msdn.com/b/jpwdkblog/archive/2011/08/29/10201505.aspx)
6.  [ドライバーのデジタル署名の留意点 - Japan WDK Support Blog - Site Home - MSDN Blogs](http://blogs.msdn.com/b/jpwdkblog/archive/2013/04/25/10413859.aspx)
7.  [Windows 10 と SHA-1 廃止ポリシーによるドライバー署名への影響について - Japan WDK Support Blog - Site Home - MSDN Blogs](http://blogs.msdn.com/b/jpwdkblog/archive/2015/09/18/windows-10-sha-1.aspx)