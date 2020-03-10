> この記事は[OpenAFS](https://ja.wikipedia.org/wiki/OpenAFS)から翻訳されています。


**OpenAFS**は、[分散ファイルシステム](https://ja.wikipedia.org/wiki/分散ファイルシステム "wikilink") [Andrew File System](https://ja.wikipedia.org/wiki/Andrew_File_System "wikilink") (AFS) の[オープンソース](../Page/オープンソース.md "wikilink")実装の1つ。AFSは[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")で開発されたもので、商用版は[トランザーク](https://ja.wikipedia.org/wiki/トランザーク "wikilink")が開発した（同社は後に[IBM](../Page/IBM.md "wikilink")に買収された）。[2000年](../Page/2000年.md "wikilink")[8月15日](../Page/8月15日.md "wikilink")の*LinuxWorld*誌で、IBMは商用AFS製品を[IBM Public Licenseでリリースする計画であることを発表した](https://ja.wikipedia.org/wiki/IBM_Public_License "wikilink")\[1\]。これが OpenAFS となった。その後活発な開発が行われ、多数の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に移植された（[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Darwin](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[IRIX](https://ja.wikipedia.org/wiki/IRIX "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink") など）。

## プロジェクト運営

運営は、今後の戦略的方向性を考える委員会と、ソースリポジトリの管理部門とに分かれている。実際には、ソースリポジトリ管理者は全て委員会のメンバーである。

## ライセンス

OpenAFS のソースコードを所有する法的実体は存在しないが、多くのファイルにはIBMのコピーライトが記述されている。ソースの多くはIPLでカバーされるが、一部のファイルは元の大学のライセンスなどに従う。適用される全てのライセンスはソースリポジトリ内の[openafs/doc/LICENSE](http://www.openafs.org/cgi-bin/cvsweb.cgi/openafs/doc/LICENSE)というファイルにある。

## 開発

オープンソース化後、開発には多数のコントリビュータ\[2\]が参加して多大な改良が行われ\[3\]、従来版との相互運用性を保ちつつ AFS3 プロトコルも実装された。また、大掛かりな移植プロジェクトも行われ（[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")版Windowsサポート、[Windows Vistaサポート](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、[Mac OS X v10.4](../Page/Mac_OS_X_v10.4.md "wikilink")/[v10.5サポート](../Page/Mac_OS_X_v10.5.md "wikilink")）、デマンドアタッチ型ファイルサーバの開発プロジェクトも行われている\[4\]。

他にも様々な開発プロジェクトが進行している。以下はその一部である。

  - ファイルサーバのバックエンドにオブジェクトデータベースを使用するプロジェクト
  - [rxtcp](http://workshop.openafs.org/afsbpw06/talks/kenh-rxtcp.pdf)
  - [rxgk](http://workshop.openafs.org/afsbpw07/talks/lha.pdf)
  - rxk5
  - [instrumentation framework](http://workshop.openafs.org/afsbpw07/talks/tkeiser.pdf)
  - [byte-range locking support](http://workshop.openafs.org/afsbpw07/talks/matt.pdf)

## 配布

現存のユーザーベースには、単一サーバセルから大規模な国際的学究システム、各種研究所、政府機関、企業など様々な組織が含まれる。運用されているAFSセルのごく一部のスナップショットとして、OpenAFSのパッケージに含まれている[CellServDB](http://dl.central.org/dl/cellservdb/CellServDB)ファイルがある。

## 商用サポート

OpenAFSの商用サポートや開発を請け負う企業として[Sine Nomine Associates](http://www.sinenomine.net/)や[Secure Endpoints Inc.](https://www.secure-endpoints.com)などがある。

## 脚注

## 外部リンク

  - [OpenAFS web site](http://www.openafs.org/)
  - [AFS Wiki](http://www.dementia.org/twiki/bin/view/AFSLore/)

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink")

1.  [Opening up AFS](http://www-128.ibm.com/developerworks/opensource/library/os-afs.html) IBM、2000年9月1日
2.  [OpenAFS Contributors](http://www.openafs.org/credits.html) openafs.org
3.  [OpenAFS celebrates its 5th birthday by releasing OpenAFS 1.4.0](http://lists.openafs.org/pipermail/openafs-announce/2005/000129.html) Jeffrey Altman、2005年11月1日
4.  [Demand Attach / Fast-Restart Fileserver](http://workshop.openafs.org/afsbpw06/talks/tkeiser-dafs.pdf)