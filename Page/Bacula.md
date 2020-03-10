> この記事は[Bacula](https://ja.wikipedia.org/wiki/Bacula)から翻訳されています。


**Bacula**（バキュラ）とは、[ネットワークを基礎とした](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[バックアップ](https://ja.wikipedia.org/wiki/バックアップ "wikilink")・[プログラムである](../Page/プログラム_\(コンピュータ\).md "wikilink")。

## 概要

Baculaは[GPL2の改訂版の下で発表された](../Page/GNU_General_Public_License.md "wikilink")<sub>\[1\]</sub>。スローガンは「闇夜に来たりてコンピュータから命の髄を吸う」(*It comes by night and sucks the vital essence from your computers.*)。Baculaという名前は「**Bac**kup」（バックアップ）と「Drac**ula**」（[ドラキュラ](../Page/ドラキュラ.md "wikilink")）を合わせた造語であり、Baculaのマスコットである[コウモリ](https://ja.wikipedia.org/wiki/コウモリ "wikilink")やスローガンは吸血鬼ドラキュラを思わせる物である。

Baculaは、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[Tru64](https://ja.wikipedia.org/wiki/Tru64 "wikilink")および[IRIX](https://ja.wikipedia.org/wiki/IRIX "wikilink")に挙げられる、多数の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")での遠隔バックアップに対応できる[Bacula.org](http://www.bacula.org/dev-manual/Supported_Operating_Systems.html)。

バックアップ・データは、[磁気テープ](../Page/磁気テープ.md "wikilink")、[DVD](../Page/DVD.md "wikilink")またはネットワーク・ドライブなど、様々な媒体に保存できる。他の高機能なバックアップ・ソフトと比較しても、Baculaは[ファイアウォール](../Page/ファイアウォール.md "wikilink")にまつわる問題がほとんどない上、性能面でもひけをとらない。

## 構造

Baculaの構造は、バックアップ処理を制御するクライアント（バックアップ対象のファイルが有る機械）、ストレージ（バックアップ・データを保存する媒体が有る機械）、およびサーバ上で稼動する三種の[デーモン](../Page/デーモン.md "wikilink")を中心に展開される。三種のデーモンは以下のとおりである。

  - Director: 全てのバックアップ管理作業の制御、データベース・アクセスの制御、バックアップの初期化

<!-- end list -->

  - Storageデーモン: バックアップ媒体の処理とバックアップ・データの受信

<!-- end list -->

  - Fileデーモン: データ・アクセスの処理、クライアント側の暗号処理と圧縮処理、および実際のデータ読み込みまたは復旧

肝心な点は、どの作業を稼動させるか、いつ作業を稼動させるか、およびどのファイルをバックアップするか、という事に関する全ての情報は、Directorによって制御されるという事である。StorageおよびFileデーモンは、Directorが使うために資源へのアクセスを提供するだけである。それらはバックアップ処理の詳細な制御はしない。

この構造では、三種のデーモンは三台の別々のマシン上で稼動すべきという事を意味する一方で、等しく有効な構成は、バックアップ処理を制御するマシンで三種のデーモン全てを稼動し、FileやStorageデーモンがアクセスするため、どんな遠隔ファイルやストレージ資源も、[smbや](https://ja.wikipedia.org/wiki/Server_Message_Block "wikilink")[nfs上のファイル](https://ja.wikipedia.org/wiki/Network_File_System "wikilink")・システムにマウントする。

## 脚注

<references/>

## 外部リンク

  - [日本のBaculaコミュニティサイト。ユーザーズガイド（マニュアル）の翻訳等](http://www.bacula.jp/)
  - [Bacula home page](http://www.bacula.org/)
  - [The Current State of Bacula](http://www.bacula.org/7.0.x-manuals/en/main/Current_State_Bacula.html)
  - [SourceForge project page](http://sourceforge.net/projects/bacula)
  - [Bacula HP-UX Binaries](http://deranfangvomen.de/~floh/bacula/)
  - [FSFE becomes the legal guardian of the Bacula Project](http://mailman.fsfeurope.org/pipermail/press-release/2006q4/000161.html)
  - [OS Reviews: Workhorse for Network Backups](http://www.osreviews.net/reviews/admin/bacula)
  - [開発元Bacula Systemsホームページ　-　商用サポートサポート、カスタム開発、導入サービスを提供](http://www.baculasystems.com/)

[Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:2000年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2000年のソフトウェア "wikilink")

1.  [Bacula Copyright](http://www.bacula.org/dev-manual/Bacula_Copyri_Tradem_Licens.html)