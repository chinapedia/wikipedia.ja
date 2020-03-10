> この記事は[VERITAS File System](https://ja.wikipedia.org/wiki/VERITAS_File_System)から翻訳されています。


**VERITAS File System**（**VxFS**）は、ベースの[ファイルシステム](../Page/ファイルシステム.md "wikilink")。[VERITAS](../Page/VERITAS.md "wikilink")ソフトウェアが開発した\[1\]。[OEM](../Page/OEM.md "wikilink")契約により、VxFSは[HP-UX](../Page/HP-UX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の主要ファイルシステムとして使われている（ただし、HP-UXでは **JFS** と呼ばれている）。また、ライセンスに基づきオンラインの[デフラグメンテーション](../Page/デフラグメンテーション.md "wikilink")とリサイズをサポートしたものは **Online JFS** と呼ばれている\[2\]。他にも[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")、[Linux](../Page/Linux.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[OpenSolaris](../Page/OpenSolaris.md "wikilink")、[UnixWare](https://ja.wikipedia.org/wiki/UnixWare "wikilink")、[OpenServer](https://ja.wikipedia.org/wiki/OpenServer "wikilink") などでサポートされている。VxFSは、本来[AT\&T](../Page/AT&T.md "wikilink")の [UNIX Systems Laboratories](https://ja.wikipedia.org/wiki/UNIX_Systems_Laboratories "wikilink") のために開発された。VxFSは [Veritas Storage Foundation](https://ja.wikipedia.org/wiki/:en:Veritas_Storage_Foundation "wikilink")（他に [Veritas Volume Manager](https://ja.wikipedia.org/wiki/:en:Veritas_Volume_Manager "wikilink") を含む）の一部としてパッケージ化されている。

## 歴史

ベンダーによれば、VxFSは世界初の商用[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")だという\[3\]。これは、商用製品として初めてのジャーナリングファイルシステムとも解釈できるし、ハードウェアにバンドルされていない製品として初めてとも解釈できる。

VxFSの最初の開発者の1人として Dan Koren が挙げられる\[4\]。彼はあるメーリングリストで、1990年に[AT\&T](../Page/AT&T.md "wikilink")との契約でVxFSの開発を開始し、約1年で release 1.0 を完成させたと記している\[5\]。他の文献でも1991年に最初の製品をリリースしたという点で一致している\[6\]\[7\]。

1990年代初めにはインターネットは広く利用可能というわけではなかったため、[Unix系](../Page/Unix系.md "wikilink")OSに新たなファイルシステムを導入するのは今よりも難しく、リリースと商用化の間に1、2年の遅延が生じることも珍しくなかった。

## バージョン履歴

VxFS のディスク上のレイアウトにはバージョンがあり、ファイルシステムがマウントされた状態でアップグレード可能である。バージョンは今のところ7まで存在する。

  - バージョン2 - ファイルセット、動的[inode](https://ja.wikipedia.org/wiki/inode "wikilink")割り当て、[ACLを追加サポート](../Page/アクセス制御リスト.md "wikilink")。VxFS 4.0 では、バージョン1から3までが既にサポートされていない。
  - バージョン4 - ストレージ・チェックポイントを追加サポートし、[Veritas Cluster File System](https://ja.wikipedia.org/wiki/:en:Veritas_Cluster_File_System "wikilink") をサポート。VxFS 3.2.1 で導入された。VxFS 5.1 ではバージョン4のレイアウトは既にサポートされていない\[8\]。
  - バージョン5 - 最大32[TB](https://ja.wikipedia.org/wiki/テラバイト "wikilink") () までのファイルシステムをサポート。個々のファイルは最大 2TB までである。VxFS 3.5 で導入されたが、VxFS 5.1 ではバージョン5のレイアウトは既にサポートされていない\[9\]。
  - バージョン6 - ファイルシステムもファイルも最大 8[EB](https://ja.wikipedia.org/wiki/エクサバイト "wikilink") () までサポートしている。バージョン6 では、複数ボリュームでの[名前付きストリーム/リソースフォーク](https://ja.wikipedia.org/wiki/フォーク_\(ファイルシステム\) "wikilink")、ファイル変更ログもサポートしている。バージョン6 は VxFS 4.0 で導入された。
  - バージョン7 - ダイナミックストレージティアリング機能をサポート。異なるボリューム間でファイルを移動でき、ファイル生成時にポリシーに基づいて異なるボリューム群にアロケートでき、ボリュームを個別に復旧してもファイルシステムの名前空間を変化させない。バージョン7は VxFS 5.0 で導入された。

バージョン8または9で、透過的圧縮と透過的暗号化が追加サポートされる予定。

## パラレルアクセスモード

VxFSには、シングルインスタンスモードとパラレルアクセスモード（クラスタモード）という動作モードがある。パラレルアクセスモードは複数のサーバが同時に同じファイルシステムにアクセスできるモードである。このモードで動作するVxFSは [Veritas Cluster File System](https://ja.wikipedia.org/wiki/:en:Veritas_Cluster_File_System "wikilink") と呼ばれる。

どちらのモードでもVxFSとしてのディスク上のレイアウトは同じであり、モードの切り替えに際して変換などは不要である。

## 脚注

## 外部リンク

  - [Veritas File System documentation](http://sort.symantec.com/documents)
  - [VERITAS Storage Foundation](http://www.symantec.com/enterprise/products/overview.jsp?pcid=1020&pvid=203_1)
  - [VxFS Quick Reference](http://eval.veritas.com/downloads/van/fs_quickref.pdf)
  - [VERITAS Cluster File System](http://www.symantec.com/Products/enterprise?c=prodinfo&refId=209&cid=1020)
  - [Symantec Operations Readiness Tools](http://sort.symantec.com) (SORT)

[Category:シマンテック](https://ja.wikipedia.org/wiki/Category:シマンテック "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:1991年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1991年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  [Veritas File Systems with Disk Layout Version 4 or Version 5 Cannot be Mounted or Upgraded with Veritas File System Release 5.1](http://www.symantec.com/business/support/index?page=content&id=TECH78028) Symantec
9.