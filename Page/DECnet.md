> この記事は[DECnet](https://ja.wikipedia.org/wiki/DECnet)から翻訳されています。


**DECnet** は、[1975年](../Page/1975年.md "wikilink")、[DECが](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")同士の接続のために開発した一連の[通信プロトコル](../Page/通信プロトコル.md "wikilink")群である。初期の [Peer to Peer](../Page/Peer_to_Peer.md "wikilink") ネットワークアーキテクチャの1つで、[1980年代](../Page/1980年代.md "wikilink")にはDECはこれを武器としてネットワーク市場に参入した。

当初4階層で構成されていたが、後（[1982年](../Page/1982年.md "wikilink")）に[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")に準拠して7層のネットワークプロトコルとなった。

DECnet は、当初からDECの主要[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である[VAX/VMS向けに構築された](https://ja.wikipedia.org/wiki/OpenVMS "wikilink")。DECはこれを自社製[UNIX](../Page/UNIX.md "wikilink")である[Ultrix](https://ja.wikipedia.org/wiki/Ultrix "wikilink")にも移植した。また、**DEC Pathworks** の名称で[Macintosh](../Page/Macintosh.md "wikilink")や[DOSおよび](../Page/DOS_\(OS\).md "wikilink")[Windowsを搭載した](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")向けの実装も販売した。これにより、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")を [VAX](https://ja.wikipedia.org/wiki/VAX "wikilink") を中心としたネットワークの端末として使えるようにした。最近では、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")向けのオープンソース版が開発されている\[1\]。

## DECnet の変遷

DECnet という呼称は、**DIGITAL Network Architecture** (DNA) を実装したネットワーク製品についてハードウェア・ソフトウェアを問わず使用された。DIGITAL Network Architecture とは、ネットワークアーキテクチャ全般を定義した文書群を指し、アーキテクチャの各層について仕様が記述され、[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")の各層の操作・運用が記述されているものである。[LANアナライザ](https://ja.wikipedia.org/wiki/LANアナライザ "wikilink")などは、DEC発祥のプロトコルを全て "DECnet" と分類することが多いが、厳密に言えばDECが規格策定したプロトコルであっても LAT、SCS、AMDS、LAST/LAD などは DECnet には含まれず、DIGITAL Network Architecture の一部ではない。

DECnet の変遷は、DNA の歴史に他ならない。DNA の起源は1970年代初めである。DEC が最初のDNA仕様を発表したころ、[IBM](../Page/IBM.md "wikilink")は [Systems Network Architecture](https://ja.wikipedia.org/wiki/Systems_Network_Architecture "wikilink") (SNA) を発表した。それ以来、DNA は次のように発展してきた。

### フェーズI（1974年）

2台の[PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")（OSは [RSX-11](https://ja.wikipedia.org/wiki/RSX-11 "wikilink")）のみをサポート。通信方法はDDCMP（Digital Data Communications Message Protocol）という一対一リンクであった。

### フェーズII（1976年）

最大32ノードのネットワークをサポート。各ノードの実装が異なっていても相互運用可能。実装としては、[RSTS](https://ja.wikipedia.org/wiki/RSTS/E "wikilink")、[TOPS-10](https://ja.wikipedia.org/wiki/TOPS-10 "wikilink")、[TOPS-20](https://ja.wikipedia.org/wiki/TOPS-20 "wikilink") が加わったが、通信は依然として一対一リンクのみであった。ファイル転送（FAL）、遠隔ファイルアクセス（DAP）、タスク間プログラミングインタフェース、ネットワーク管理機能などが導入された。

### フェーズIII（1980年）

最大255ノードのネットワークをサポート。一対一リンク以外にマルチドロップ型リンクもサポート。適応型ルーティング機能、ダウンライン・ローディング（MOP）、レコードアクセス、ネットワーク管理アーキテクチャ、IBMのSNAや[CCITT勧告](../Page/ITU-T.md "wikilink")[X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")などの他のネットワークとのゲートウェイなどが導入された。

### フェーズIVとフェーズIV+（1982年）

<div style="float:right;margin:15px;margin-top:0px;padding:0px;border: 1px solid #aaa;">

<table>
<caption><strong>DECnet フェーズIV プロトコルスイート</strong></caption>
<thead>
<tr class="header">
<th><p>アプリケーション層</p></th>
<th><p>DAP: Data Access Protocol<br />
CTERM: Command Terminal</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ネットワーク管理層</p></td>
<td><p>NICE: Network Information (and) Control Exchange<br />
MOP: Maintenance Operation Protocol</p></td>
</tr>
<tr class="even">
<td><p>セッション層</p></td>
<td><p>SCP: Session Control Protocol</p></td>
</tr>
<tr class="odd">
<td><p>トランスポート層</p></td>
<td><p>NSP: Network Service Protocol</p></td>
</tr>
<tr class="even">
<td><p>ネットワーク層</p></td>
<td><p>DRP: DECnet Routing Protocol</p></td>
</tr>
<tr class="odd">
<td><p>データリンク層</p></td>
<td><p>DDCMP: Digital Data Communications Message Protocol<br />
<a href="../Page/イーサネット.md" title="wikilink">イーサネット</a>、<a href="https://ja.wikipedia.org/wiki/トークンリング" title="wikilink">トークンリング</a>、<a href="https://ja.wikipedia.org/wiki/High-Level_Data_Link_Control" title="wikilink">HDLC</a>、<a href="https://ja.wikipedia.org/wiki/Fiber_distributed_data_interface" title="wikilink">FDDI</a>、…</p></td>
</tr>
<tr class="even">
<td><p>物理層</p></td>
<td><p><a href="../Page/イーサネット.md" title="wikilink">イーサネット</a>、<a href="https://ja.wikipedia.org/wiki/トークンリング" title="wikilink">トークンリング</a>、<a href="https://ja.wikipedia.org/wiki/Fiber_distributed_data_interface" title="wikilink">FDDI</a>、…</p></td>
</tr>
</tbody>
</table>

</div>

フェーズIVは、当初 [RSX-11](https://ja.wikipedia.org/wiki/RSX-11 "wikilink") と VMS 向けにリリースされ、続いて TOPS-20、TOPS-10、Ultrix、VAXELN、[RSTS/E](https://ja.wikipedia.org/wiki/RSTS/E "wikilink") もサポートされた。最大64,449ノードまで（1023ノード×63エリア）のネットワークをサポートし、データリンクはDDCMP以外に[イーサネット](../Page/イーサネット.md "wikilink")もサポートされ、階層型ルーティング、VMSクラスターサポート、ホストサービス（CTERM）などが導入された。CTERMは、あるコンピュータ上のユーザーが他のコンピュータにログインできる機能で、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")プロトコルスタックでの [Telnet](../Page/Telnet.md "wikilink") と同等の機能を実現している。また、PATHWORKS（あるいは PATHWORKS 32）と呼ばれる製品もリリースし、DECnet フェーズIV の機能の大部分を DOS および Microsoft Windows 向けに実装した。

フェーズIV では[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の7層に類似した8層アーキテクチャを実装している。当時、OSI参照モデルは完成していなかったため、フェーズIVのプロトコルの大部分は独自のものだった。

イーサネットの実装も普通とは異なり、[MACアドレス](../Page/MACアドレス.md "wikilink")をソフトウェアが変更し、AA-00-04-00-xx-yy の xx-yy の部分が DECnet のホスト毎のネットワークアドレスそのものになっている。このため、[LAN上のルーティングが簡便になっていた](../Page/Local_Area_Network.md "wikilink")。ただし、そのために同じホストから同じLANに複数のNICで接続することができない。

DECnet のプロトコルスタックは Linux や SunOS といったプラットフォームにも移植され、[シスコシステムズ](https://ja.wikipedia.org/wiki/シスコシステムズ "wikilink")などのネットワーク機器企業もDECnet対応製品をリリースした。

フェーズIVがリリースされたころ、[ターミナルサーバ](https://ja.wikipedia.org/wiki/ターミナルサーバ "wikilink")経由のシリアル端末アクセスのための Local Area Transport（LAT）と呼ばれる独自プロトコルもリリースしている。LAT 自体は DECnet とは全く無関係だが、LATターミナルサーバは DECnet の MOP を使って端末へのダウンロードやブート処理を行っていた。

フェーズIV への拡張は DECnet フェーズIV+ と呼ばれたが、フェーズIV との相互運用性は完全に保たれていた。

### フェーズVとフェーズV+（1987年）

アーキテクチャ上無制限のノード数のネットワークをサポートし、ネットワーク管理モデルを一新し、ネームサービスが追加され、性能向上が図られている。独自プロトコルからOSIに移行し、マルチベンダー接続性を確保すると共に、フェーズIVとの互換性も維持している。従って、アーキテクチャ的には DNA と OSI のハイブリッド型となっていて、トランスポート層以下が共通になっている。透過的なトランスポート層レベルでの[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")とのリンクが、[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") [RFC](../Page/Request_for_Comments.md "wikilink") 1006 (OSI over IP) と RFC 1859 (NSP over IP) として追加された。

その後、OSI準拠であることを強調するために **DECnet/OSI** と改称し、さらに TCP/IP も利用可能となったときに **DECnet-Plus** と改称した。

## 利用可能性

DECnet のプロトコル設計はDECが全て行った。ただし、DECnet フェーズII からプロトコル仕様が公表されている。したがって、誰でも実装可能であるという意味で[オープン標準](../Page/オープン標準.md "wikilink")となっている。実際DEC以外での実装もいくつか行われており、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")への実装もある。

## 脚注

## 参考文献

  - Carl Malamud, *Analyzing DECnet/OSI Phase V*. Van Hostrand Reinhold, 1991. ISBN 0-442-00375-7.
  - James Martin, Joe Leben, *DECnet Phase V: An OSI Implementation*. Digital Press, 1992. ISBN 1-55580-769-0.

## 外部リンク

  - [HECnet](http://www.update.uu.se/~bqt/hecnet.html) ホビーストによるDECnet
  - [DECnet-Plus マニュアル](http://www.hp.com/go/openvms/doc/) [ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink") OpenVMS 公式サイト
  - [HP OpenVMS Freeware](http://www.hp.com/go/openvms/freeware) DECnet フェーズIV のマニュアルが OpenVMS Freeware V5.0 ディストリビューションにある。

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink")

1.  [Linux-DECnet on Sourceforge](http://linux-decnet.sourceforge.net/)