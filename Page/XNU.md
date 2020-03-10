> この記事は[XNU](https://ja.wikipedia.org/wiki/XNU)から翻訳されています。


**XNU**は、[アップルが取得](../Page/アップル_\(企業\).md "wikilink")・開発した[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")[カーネル](../Page/カーネル.md "wikilink")である。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")に用いられ、[オープンソース](../Page/オープンソース.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[Darwinの一部として公開されている](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")。XNUはX is Not [Unixの略](../Page/UNIX.md "wikilink")\[1\]。

## デザイン

XNUは[モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink")と[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")の特徴を併せもつ[ハイブリッドカーネルで](https://ja.wikipedia.org/wiki/カーネル#ハイブリッドカーネル "wikilink")、マイクロカーネルが可能にする[メッセージパッシングのモジュール性やより広範な](https://ja.wikipedia.org/wiki/メッセージ_\(コンピュータ\) "wikilink")[メモリ保護](https://ja.wikipedia.org/wiki/メモリ保護 "wikilink")、モノリシックカーネルがもつ実行速度の保持など、両方の技術を有効に利用することを試みている。

XNUは現在、[ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")\[2\]、[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")、[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")ベースのプロセッサにおいて、シングルプロセッサと[SMPの両方で動作する](../Page/対称型マルチプロセッシング.md "wikilink")。

### Mach

XNUの基礎である[Mach](../Page/Mach.md "wikilink")はシンプルなマイクロカーネルであり、OSのコアを分割された柔軟なプロセスとして実行することができる（Machコアの上でいくつかのOSを平行して実行できる）。しかし、これはカーネル/ユーザモードの切り替えに時間を消費し、またマイクロカーネルのアドレス空間とデーモンとのあいだで行われるメッセージのマッピングやコピーによってオーバーヘッドを生じることから、しばしばパフォーマンスが低下してしまう。macOSでは効率化のために、[BSD](../Page/BSD.md "wikilink")の機能はMachのコアの中に組み込まれた。その結果、Machと古典的なBSDカーネル両方の利点と欠点を併せもつものとなった。

Machは、カーネル[スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")、[プロセス](../Page/プロセス.md "wikilink")管理、[プリエンプティブ・マルチタスク](https://ja.wikipedia.org/wiki/プリエンプティブ・マルチタスク "wikilink")、メッセージパッシング（[プロセス間通信](../Page/プロセス間通信.md "wikilink")）、[メモリ保護](https://ja.wikipedia.org/wiki/メモリ保護 "wikilink")、[仮想記憶](../Page/仮想記憶.md "wikilink")、[ソフトリアルタイム処理のサポート](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")、カーネル[デバッグ](../Page/デバッグ.md "wikilink")のサポート、コンソール[I/Oを提供する](../Page/入出力.md "wikilink")。

### BSD

カーネルの[BSD](../Page/BSD.md "wikilink")の部分は、[POSIX](../Page/POSIX.md "wikilink") [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")（BSDシステムコール）、Machタスク上での[Unixプロセスモデル](../Page/UNIX.md "wikilink")、基本的なセキュリティーポリシー、ユーザIDとグループID、アクセス権、[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")、[仮想ファイルシステム](../Page/仮想ファイルシステム.md "wikilink")、[HFS](../Page/Hierarchical_File_System.md "wikilink") / [HFS+などいくつかのローカルファイルシステム](https://ja.wikipedia.org/wiki/HFS_Plus "wikilink")、[Network File System](https://ja.wikipedia.org/wiki/Network_File_System "wikilink") (NFS) クライアントとサーバ、暗号化フレームワーク、[UNIX System V](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")[プロセス間通信](../Page/プロセス間通信.md "wikilink")、auditサブシステム、[強制アクセス制御](https://ja.wikipedia.org/wiki/強制アクセス制御 "wikilink")、いくつかのlocking primitivesを提供する。

### I/O Kit

は[C++](../Page/C++.md "wikilink")のサブセットで書かれたデバイスドライバフレームワークである。[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")設計を用いており、ドライバのクラスに共通する機能を提供し、ドライバをより早くより少ないコードで書けるようにする。I/O Kitはマルチスレッド化されており、[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")を保証し、ホットプラグや動的なデバイスの配置を可能にする。

システムの安定性を高めるため、多くのドライバはユーザ空間で実行されるように書くことができる。（もしユーザ空間のドライバがクラッシュしてもカーネルはクラッシュしないが、カーネル空間のドライバがクラッシュするとカーネルもクラッシュする。）カーネル空間のドライバの例として、ディスクアダプタやネットワークアダプタのドライバ、グラフィックドライバ、[USBや](../Page/ユニバーサル・シリアル・バス.md "wikilink")[FireWireのコントローラのドライバ](../Page/IEEE_1394.md "wikilink")、[仮想機械](../Page/仮想機械.md "wikilink")のドライバなどがある。

## 共有資源の保護

マルチプロセッサのマシンを安全に動かすために（ファイル、データ構造など）[共有資源](https://ja.wikipedia.org/wiki/共有資源 "wikilink")へのアクセスは、同一時間のうちにリソースが改変されないように直列化しなければならない。同時発生的なアクセスを防ぐための手法として[不可分操作](../Page/不可分操作.md "wikilink")、[スピンロック](../Page/スピンロック.md "wikilink")、[クリティカルセクション](https://ja.wikipedia.org/wiki/クリティカルセクション "wikilink")、[排他制御](../Page/排他制御.md "wikilink")、serializing tokenを用いることができる。

## 歴史

### NeXT社時代

もともと[NeXTSTEP](https://ja.wikipedia.org/wiki/NeXTSTEP "wikilink") [OSのために](../Page/オペレーティングシステム.md "wikilink")[NeXT](../Page/NeXT.md "wikilink")によって開発されたXNUは、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")が開発した**[Mach](../Page/Mach.md "wikilink")カーネル2.5**に**[4.3BSDコンポーネント](https://ja.wikipedia.org/wiki/BSD#4.3BSD "wikilink")**を付加し、**Driver Kit**と呼ばれるドライバを記述するためのオブジェクト指向APIを組み合わせたハイブリッドカーネルであった。

### アップル買収後

NeXTがアップルに買収された後、**Machコンポーネント**は3.0へ、**BSDコンポーネント**は[FreeBSD](../Page/FreeBSD.md "wikilink")プロジェクトに由来するコードへとアップグレードされ、Driver Kitは**I/O Kit**と呼ばれるドライバを記述するための[C++](../Page/C++.md "wikilink") APIに置き換えられた。

### K32/K64

XNUは[Mac OS X 10.6 Snow Leopard](../Page/Mac_OS_X_v10.6.md "wikilink")（Darwinバージョン10）から、K32と呼ばれる[32ビット](../Page/32ビット.md "wikilink")のバージョンとK64と呼ばれる[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")のバージョンの2つになった\[3\]。K32は64ビットアプリケーションをユーザランドで実行できる。Mac OS X 10.6で新しくなったのは、XNUが64ビットのカーネル空間で実行できるようになったことである。K64はK32と比べていくつかの利点がある\[4\]。

  - より大きい32GBのRAMを扱うことができる。
  - より大きなキャッシュバッファが扱え、潜在的なI/Oパフォーマンスが向上する。
  - 非常に大きな[DMAバッファがいくつかあっても](../Page/Direct_Memory_Access.md "wikilink")、すべてのデバイスを64ビット空間に配置でき、高性能なネットワークデバイスや複数の[GPUを使ったときのパフォーマンスが向上する](../Page/Graphics_Processing_Unit.md "wikilink")。

64ビットカーネルをサポートする機種で、6と4キーを押し続けて起動するとK64で起動できる\[5\]。K64は32ビットアプリケーションを実行できるが、32ビット[カーネル機能拡張](https://ja.wikipedia.org/wiki/ローダブル・カーネル・モジュール "wikilink") (KEXT) は実行できないので、これらを読み込めるようにするにはK64に移植しなければならない。

## 出典

## 外部リンク

  - [XNU: The Kernel](http://www.kernelthread.com/mac/osx/arch_xnu.html) - kernelthread.comによる、XNUコンポーネントの概要
  - [Inside the Mac OS X Kernel](http://chaosradio.ccc.de/24c3_m4v_2303.html) - 'This talk intends to clear up the confusion by presenting details of the Mac OS X kernel'

[Category:OSのカーネル](https://ja.wikipedia.org/wiki/Category:OSのカーネル "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink")

1.
2.
3.  [Mac OS X 10.6 Snow Leopard: the Ars Technica review, page 5](http://arstechnica.com/apple/reviews/2009/08/mac-os-x-10-6.ars/5)
4.  [What's New in Mac OS X: Mac OS X v10.6](http://developer.apple.com/mac/library/releasenotes/MacOSX/WhatsNewInOSX/Articles/MacOSX10_6.html)
5.  [Mac OS X Server v10.6: Starting up with the 32-bit or 64-bit kernel](http://support.apple.com/kb/HT3773)