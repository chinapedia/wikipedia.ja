> この記事は[Microsoft Virtual Server](https://ja.wikipedia.org/wiki/Microsoft_Virtual_Server)から翻訳されています。


**Microsoft Virtual Server** は[仮想サーバを構築するソフトウェアである](../Page/仮想機械.md "wikilink")。オリジナルの Virtual Server は[コネクティクス](https://ja.wikipedia.org/wiki/コネクティクス "wikilink")が開発し、リリース前に[マイクロソフト](../Page/マイクロソフト.md "wikilink")に買収された。

利用目的としては、アクセス率の低いサーバ同士の集約やゲストサーバ上でのアプリケーションやシステムの開発などがある。仮想マシンの作成と管理は [IIS](../Page/Internet_Information_Services.md "wikilink") 上のウェブベースの[インタフェースを使用するか](../Page/インタフェース_\(情報技術\).md "wikilink")、VMRCplus といったクライアント アプリケーションでおこなう。Windows XPとWindows VistaがホストOSとしてサポートされているが、実運用を目的としない用途の利用に限定されている。正式サポートされている[Linux](../Page/Linux.md "wikilink")は、[Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") 2.1から5.0、[Red Hat Linux](../Page/Red_Hat_Linux.md "wikilink") 9.0、[SUSE LinuxとSUSE](https://ja.wikipedia.org/wiki/SUSE_Linux "wikilink") Linux Enterprise Server 9.0と10.0である。

## 動作上の制限

Virtual Server 2005 R2 SP1時点での制限は以下の通り。

  - ゲストOSの同時動作数は最大64個に限られている。
  - ホストOSが64ビットで動作していても、ゲストOSは64ビットとして動作することが出来ない。
  - [SMPのサポートはホストOSのみであって](../Page/対称型マルチプロセッシング.md "wikilink")、ゲストOSはSMPを利用できない。

## 履歴

2004年12月、Virtual Server 2005発売。(Standard Edition, Enterprise Edition)

2005年1月、Virtual Server 2005 R2発売。

2006年4月、Virtual Server 2005 R2を無償化。（Enterprise Edition のみ公開）

2007年6月、Virtual Server 2005 R2 SP1公開。Windows VistaとWindows Server 2008のサポート、[Intel VT](https://ja.wikipedia.org/wiki/Intel_VT "wikilink") (VT) と[AMD Virtualization](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink") (AMD-V) の仮想化技術に対応し、Virtual Disk Precompactor、ホストOSでのSMP、ホストOSの 64ビット等がサポートされた。Linuxに対応した。

## 関連項目

  - [x86仮想化](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")
  - [仮想アプライアンス](../Page/仮想アプライアンス.md "wikilink")
  - [Microsoft Virtual PC](https://ja.wikipedia.org/wiki/Microsoft_Virtual_PC "wikilink")
  - [Hyper-V](../Page/Hyper-V.md "wikilink")

## 外部リンク

  - [Microsoft Virtual Server 2005](http://www.microsoft.com/japan/windowsserversystem/virtualserver/)
  - [Microsoft Virtual Server 2005 R2 必要システム](http://www.microsoft.com/japan/windowsserversystem/virtualserver/evaluation/sysreqs.mspx)

[Category:マイクロソフトのソフトウェア](https://ja.wikipedia.org/wiki/Category:マイクロソフトのソフトウェア "wikilink") [Category:Microsoft_server_technology](https://ja.wikipedia.org/wiki/Category:Microsoft_server_technology "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")