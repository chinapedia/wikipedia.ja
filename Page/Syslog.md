> この記事は[Syslog](https://ja.wikipedia.org/wiki/Syslog)から翻訳されています。


**Syslog** は、[ログメッセージを](../Page/データログ.md "wikilink")[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上で転送するための標準規格である。"Syslog" という用語は、その[通信プロトコル](../Page/通信プロトコル.md "wikilink")を指すだけでなく、Syslog メッセージを送信するアプリケーションやライブラリに対しても使われる。

Syslog プロトコルは[クライアント/サーバ型プロトコルである](https://ja.wikipedia.org/wiki/クライアントサーバモデル "wikilink")。Syslog 送信側は短い（1024バイト以下）テキストメッセージを Syslog 受信側に送信する。受信側を一般に "syslogd"、"syslog デーモン"、"syslog サーバ" などと呼ぶ。Syslog メッセージは [UDP](../Page/User_Datagram_Protocol.md "wikilink") または [TCP](../Page/Transmission_Control_Protocol.md "wikilink") 上で送信される。送信されるデータは一般に[クリアテキスト](https://ja.wikipedia.org/wiki/クリアテキスト "wikilink")であるが、[Stunnel](https://ja.wikipedia.org/wiki/Stunnel "wikilink")、sslio、sslwrap といった SSL ラッパーを使って SSL/[TLS](../Page/Transport_Layer_Security.md "wikilink") による暗号化が可能である。

Syslog は一般に、コンピュータシステムの管理とセキュリティ監視を目的として使われる。いくつか問題はあるものの、syslog は各種プラットフォーム上で広くサポートされている。そのため、Syslog を使って様々なシステムのログデータを1つの集中リポジトリで管理することも可能である。

Syslog は現在、[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") の Syslog working group で標準化されている。

## 歴史

Syslog は 1980年代に[エリック・オールマン](../Page/エリック・オールマン.md "wikilink")が [sendmail](https://ja.wikipedia.org/wiki/sendmail "wikilink") プロジェクトの一部として開発したもので、当初は sendmail だけで使われていた。非常に便利であったため、他のアプリケーションでも使うようになっていった。そして syslog は、[UNIX](../Page/UNIX.md "wikilink") や [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") でのロギング方法の標準となっていった。同様に、他の様々な[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上でも syslog が実装されている。

最近まで syslog は[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")であって、何らかの規格があるわけではなく、個々の実装には非互換も存在していた。セキュリティ強化のため、[Internet Engineering Task Force](../Page/Internet_Engineering_Task_Force.md "wikilink") はワーキンググループを結成した。2001年、その成果は RFC 3164 としてまとめられた。その後、syslog への機能追加作業が行われてきた。メッセージ内容とトランスポート層の機構の標準化された仕様は 2005年に予定されていたが、延期された。

また、様々な企業が syslog について特許権を主張している。しかし、これはプロトコルの利用と標準化にはあまり影響を及ぼしていない。例えば、以下のような例がある。

:\* [HUAWEI TECHNOLOGIES CO.,LTD's statement about IPR claimed in draft-ietf-syslog-transport-tls-02.txt](http://datatracker.ietf.org/public/ipr_detail_show.cgi?ipr_id=724) HUAWEI の主張についての IETF IPR 開示

:\* [Patent application jeopardizes IETF syslog standard](http://trends.newsforge.com/article.pl?sid=06/06/28/2320232&from=rss) syslog 特許紛争についての NewsForge の記事

:\* [LXer: Patent jeopardizes IETF syslog standard](http://lxer.com/module/newswire/view/64026/index.html) syslog 特許紛争についての LXer の記事

## 今後の展望

syslog の利用は拡大し続けている。様々なグループが syslog の拡張の標準化を行っており、例えば医療関係での応用などが提案されている。

アメリカでは、[SOX法やHIPPA法](https://ja.wikipedia.org/wiki/上場企業会計改革および投資家保護法 "wikilink")（医療保険の相互運用性と説明責任に関する法律）などの規制により、企業は包括的なセキュリティ強化を迫られており、それには各種ソースからのログを集め、解析することも含まれている。ログを収集するには syslog は最適なフォーマットであり、その解析を行うツールは数多く存在する。最近では、企業全体の syslog 記録を集め、解析するサービス（Managed Security Service Provider、MSSP）が登場している。そのようなサービスでは[人工知能](../Page/人工知能.md "wikilink")的アルゴリズムを適用してパターンを検出し、顧客に対して問題を通報する。

## 関連項目

  - [コンソールサーバ](https://ja.wikipedia.org/wiki/コンソールサーバ "wikilink")
  - [データログ](../Page/データログ.md "wikilink")
  - [NETCONF](https://ja.wikipedia.org/wiki/NETCONF "wikilink")
  - [サーバログ](https://ja.wikipedia.org/wiki/サーバログ "wikilink")
  - [Simple Network Management Protocol](../Page/Simple_Network_Management_Protocol.md "wikilink") (SNMP)

## 関連 RFC とワーキンググループ

  - [IETF syslog working group](http://www.ietf.org/html.charters/syslog-charter.html)
  - RFC 3164 - The BSD syslog Protocol(RFC 5424に発展移行)
  - RFC 3195 - Reliable Delivery for syslog
  - RFC 5424 - The Syslog Protocol
  - RFC 5425 - TLS Transport Mapping for Syslog
  - RFC 5426 - Transmission of Syslog Messages over UDP
  - RFC 5427 - Textual Conventions for Syslog Management
  - RFC 5848 - Signed Syslog Messages
  - RFC 6012 - Datagram Transport Layer Security (DTLS) Transport Mapping for Syslog
  - RFC 6587 - Transmission of Syslog Messages over TCP

## 外部リンク

  - [SANS Paper](http://www.sans.org/rr/whitepapers/logging/1168.php) The Ins and Outs of System Logging Using Syslog
  - [Windows to Syslog](http://www.loganalysis.org/sections/syslog/windows-to-syslog)
  - [Syslog Anomaly Detection](http://devialog.org/)
  - [Syslog Help and Information](http://www.syslog.org/)

## 実装例

  - UNIX:
      - [sysklogd](http://www.infodrom.org/projects/sysklogd/)
      - [rsyslog](http://www.rsyslog.com/): TCP上の syslog 実装、RFC 3195 をサポート
      - [syslog-ng](http://www.balabit.com/network-security/syslog-ng/)
      - [metalog](http://metalog.sourceforge.net/)
      - [msyslog](http://sourceforge.net/projects/msyslog/)
      - [socklog](http://smarden.org/socklog/)

<!-- end list -->

  - Windows 2000, 2003, XP:
      - [TheOne SysLog Manager](http://www.theonesoftware.com/syslog_manager.php)
      - [Kiwi Syslog Daemon](http://www.kiwisyslog.com/)
      - [MonitorWare Products: MonitorWare Agent, WinSyslog](http://www.monitorware.com/en/Product/product_comparision.php)
      - [NetDecision LogVision](http://www.netmechanica.com/products/?prod_id=1016)
      - [NTsyslog](http://ntsyslog.sourceforge.net/)
      - [Syslserve](http://syslserve.com)
      - [syslog-ng Agent for Windows](http://www.balabit.com/network-security/syslog-ng/central-syslog-server/)
      - [Syslog Watcher](http://www.snmpsoft.com/syslogwatcher/)

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink") [Category:ネットワーク管理](https://ja.wikipedia.org/wiki/Category:ネットワーク管理 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")