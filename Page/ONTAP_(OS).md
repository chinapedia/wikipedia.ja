> この記事は[ONTAP \(OS\)](https://ja.wikipedia.org/wiki/ONTAP_\(OS\))から翻訳されています。


**ONTAP**（オンタップ）または**Data ONTAP**（データ・オンタップ）は、[ネットアップ](../Page/ネットアップ.md "wikilink")の[NAS装置で使用されている](../Page/ネットワークアタッチトストレージ.md "wikilink")[アプライアンス](https://ja.wikipedia.org/wiki/コンピュータ・アプライアンス "wikilink")[OS](../Page/オペレーティングシステム.md "wikilink")。

## 概要

同社はData ONTAPを「プラットフォームOS」と呼び、柔軟な管理と高い可用性を実現するとしている\[1\]。

Data ONTAPは、[NetBSD](../Page/NetBSD.md "wikilink")や[Linux](../Page/Linux.md "wikilink")を基にカスタマイズされたもので、コマンドや[CIFS](https://ja.wikipedia.org/wiki/Common_Internet_File_System "wikilink")/[NFS](../Page/Network_File_System.md "wikilink")/[FTP](../Page/File_Transfer_Protocol.md "wikilink")/[iSCSI](https://ja.wikipedia.org/wiki/iSCSI "wikilink")/[FCP](https://ja.wikipedia.org/wiki/FCP "wikilink")などの統合[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")管理機能は、ONTAP用にRFCや規定を準拠した独自の動作仕様及び、設定体系となっている。基本的なNAS機能としてのNFSやCIFSベースの機能だけでなく、一般に他サーバで提供される各種機能などをオプションベースで提供できる。

[ファイルシステム](../Page/ファイルシステム.md "wikilink")は独自のフル[ジャーナルファイルシステム](https://ja.wikipedia.org/wiki/ジャーナルファイルシステム "wikilink")である[WAFL](https://ja.wikipedia.org/wiki/WAFL "wikilink")(Write Anywhere File Layout)を採用しており、ダブルパリティ[RAID 6であるRAID](../Page/RAID.md "wikilink")-DPや、オンライン[バックアップ](../Page/バックアップ.md "wikilink")機能である[snapshot](https://ja.wikipedia.org/wiki/snapshot "wikilink")や[SnapRestore](https://ja.wikipedia.org/wiki/SnapRestore "wikilink")といった[リストア](https://ja.wikipedia.org/wiki/リストア "wikilink")機能や、[ディザスタリカバリ](https://ja.wikipedia.org/wiki/ディザスタリカバリ "wikilink")にも使用できる[SnapMirror](https://ja.wikipedia.org/wiki/SnapMirror "wikilink")などの機能を持つ。同社はこれら機能を、柔軟な運用管理性、設定の容易さ、安定性、広い実績を持つと主張している。

動作は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") [Xeon](../Page/Xeon.md "wikilink")を対象にしており、単一[ABIをサポートする](../Page/Application_Binary_Interface.md "wikilink")[ELF形式の](../Page/Executable_and_Linkable_Format.md "wikilink")[オブジェクトフォーマット](https://ja.wikipedia.org/wiki/オブジェクトフォーマット "wikilink")を使用している。また、最近では[プロセッサ](../Page/プロセッサ.md "wikilink")に[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")を採用するなど全製品ラインの強化が進められている。

## 状況

[LENOVO、IBM](../Page/IBM.md "wikilink")、[富士通](../Page/富士通.md "wikilink")、[日立製作所](../Page/日立製作所.md "wikilink")など、多くのベンダがNASゲートウェイとしてNetApp製品を[OEM](../Page/OEM.md "wikilink")販売しているが、その全てで内部的にはData ONTAPが稼働している。

## 参照

<references />

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink")

1.  [NetApp プラットフォームOS](http://www.netapp.com/jp/products/platform-os/)