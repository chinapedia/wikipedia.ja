> この記事は[LAN](https://ja.wikipedia.org/wiki/LAN)から翻訳されています。


**LANアナライザ**（ラン アナライザ）は[プロトコルアナライザ](https://ja.wikipedia.org/wiki/プロトコルアナライザ "wikilink")の一種で、[LAN上を通過する](../Page/Local_Area_Network.md "wikilink")[トラフィック](https://ja.wikipedia.org/wiki/トラフィック "wikilink")を監視したり記録するための[ハードウェア](../Page/ハードウェア.md "wikilink") や[ソフトウェア](../Page/ソフトウェア.md "wikilink")のことである。データの流れがネットワーク上を行き来している際に用いると、特定の[RFCや他の仕様に従っているようなコンテンツならそれを解読したり分析できる](../Page/Request_for_Comments.md "wikilink")。

「**パケットアナライザ**」や「**ネットワークアナライザ**」と呼ばれる事もある。また、俗に「**Sniffer**（スニファ）」とも呼ばれる（この語は、英語のスニッフ（sniff、においなどを嗅ぐ）に由来しており、ネットワークを通過する[トラフィック](https://ja.wikipedia.org/wiki/トラフィック "wikilink")を嗅ぎ取ることから命名されている）。

「**Sniffer**」は[NetScout Systems](https://ja.wikipedia.org/wiki/NetScout_Systems "wikilink")(旧：Network General)が1991年5月28日米国で登録商標を取得している。

## 概要

有線ネットワークでは、LANアナライザは同一ネットワーク内（あるいはその一部）にある他のマシンに出入りするトラフィックを監視することができる。ネットワークの配置や構造（[イーサネット・ハブや](https://ja.wikipedia.org/wiki/ハブ_\(ネットワーク機器\) "wikilink")[ネットワーク・スイッチなど](../Page/スイッチングハブ.md "wikilink")）によって監視できる範囲は制限されると考えられているが、この制限を迂回する方法が存在する。その一例は、「ネットワーク・スイッチ」に虚偽の情報を送りつけることで同一ネットワーク上の他のマシン宛の[パケット](../Page/パケット.md "wikilink")を不正受信する[ARPスプーフィング](../Page/ARPスプーフィング.md "wikilink")と呼ばれる方法である。ネットワークを監視するために[LAN上の全てのパケットを監視したいという要望が強い場合には](../Page/Local_Area_Network.md "wikilink")、ネットワーク・スイッチにいわゆるモニタリングポート（スイッチ上の[ポートを通過する全てのパケットを分配して流すための特定ポート](https://ja.wikipedia.org/wiki/ポート番号 "wikilink"))を設ける場合もある。

有線ネットワーク、無線ネットワークともに、他のマシンに出入りするトラフィックを受け取るためには、全てのデータを受信可能とする[プロミスキャス・モード](../Page/プロミスキャス・モード.md "wikilink")（無差別モード）で動作させる必要がある。ネットワーク[デバイス・ドライバーによって](../Page/デバイスドライバ.md "wikilink")、このモードをサポートしていないものもある。

初期には単にパケットの内容を直接出力するものが多かったが、後にパケットの内容を解析してより理解しやすい形で表示するものが登場している。どこまでがプロトコルヘッダであるかといった情報を視覚的に表示するもの、[DNS関連のパケットであれば名前解決の要求であるのか応答であるのかなど](../Page/Domain_Name_System.md "wikilink")、[SNMP関連のパケットであれば](../Page/Simple_Network_Management_Protocol.md "wikilink")[ASN.1の解析と表示などが代表例として挙げられる](../Page/Abstract_Syntax_Notation_One.md "wikilink")。

## LANアナライザの利用用途

LANアナライザは次のような用途に活用できる。

  - ネットワークに関する[トラブルシューティング](../Page/トラブルシューティング.md "wikilink")
  - あるネットワークに侵入する試みを阻止する
  - あるネットワークに侵入するための情報・詳細を収集する
  - （ユーザーの）ネット利用を調査し、怪しいコンテンツを[フィルタリング](https://ja.wikipedia.org/wiki/フィルタリング "wikilink")する
  - 他のネットユーザの行動を監視し、[パスワード](https://ja.wikipedia.org/wiki/パスワード "wikilink")等の秘密の情報を盗む（これはあくまでも[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")されていない情報に限られる）
  - ネットワーク上で用いられる[プロトコル](../Page/プロトコル.md "wikilink")を[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")する

## 代表的なLANアナライザ

  - [Sniffer Portable Professional](https://ja.wikipedia.org/wiki/Sniffer_Portable_Professional "wikilink")
  - [Sniffer Adaptive Application Analyzer](https://ja.wikipedia.org/wiki/Sniffer_Adaptive_Application_Analyzer "wikilink")
  - [tcpdump](https://ja.wikipedia.org/wiki/tcpdump "wikilink")
  - [Wireshark](https://ja.wikipedia.org/wiki/Wireshark "wikilink")
      - [Ethereal](https://ja.wikipedia.org/wiki/Ethereal "wikilink")
  - [Ettercap](https://ja.wikipedia.org/wiki/Ettercap_\(computing\) "wikilink")
  - [dSniff](https://ja.wikipedia.org/wiki/dSniff "wikilink")
  - [OmniPeek](https://ja.wikipedia.org/wiki/OmniPeek "wikilink")
      - [EtherPeek](https://ja.wikipedia.org/wiki/EtherPeek "wikilink")
      - [AiroPeek](https://ja.wikipedia.org/wiki/AiroPeek "wikilink")
  - [PRTG](https://ja.wikipedia.org/wiki/PRTG "wikilink")
  - [Ngrep](https://ja.wikipedia.org/wiki/Ngrep "wikilink")
  - [Xplico](https://ja.wikipedia.org/wiki/Xplico "wikilink")
  - [Narus](https://ja.wikipedia.org/wiki/Narus "wikilink")
  - [NetVCR](https://ja.wikipedia.org/wiki/NetVCR "wikilink")　(アプライアンス型)
  - [ClearSight](https://ja.wikipedia.org/wiki/ClearSight "wikilink")　(ソフトウェアもしくはアプライアンス型)
  - [Colasoft Capsa](https://ja.wikipedia.org/wiki/Colasoft_Capsa "wikilink")

## 外部リンク

  - [Packet Sniffing FAQ (Robert Grahamによる)(英語)](http://www.robertgraham.com/pubs/sniffing-faq.html)
  - [PacketDefense(英語)](http://www.packetdefense.com)
  - [Sniffer - Basics and Detection(英語)](http://www.rootshell.be/~dhar/downloads/Sniffers.pdf)

<!-- end list -->

  - 各アナライザの公式サイト:
      - [NetScout – Sniffer (the original packet sniffer)](http://www.netscout.com)
      - [Ethereal](http://www.ethereal.com/)
      - [CommView](http://www.tamos.com/products/commview/)
      - [Ultra Network](http://www.gjpsoft.com/UltraNetSniffer)
      - [Packet sniffer](http://www.sniff-em.com)
      - [WinDump](http://www.winpcap.org/windump/)
      - [Analyzer](http://analyzer.polito.it/)
      - [Packetyzer](http://www.packetyzer.com/)
      - [IPDump2, a portable packet sniffer](http://www.cr0.net:8040/code/network/)
      - [WildPackets EtherPeek and AiroPeek](http://www.wildpackets.com/products/)
      - [WildPackets EtherPeek and AiroPeek](http://www.wildpackets.com/products/)
      - [PacMon公式サイト](http://www.layer.co.jp/)
      - [Freepeek公式サイト](http://hp.vector.co.jp/authors/VA015591/)
      - [NiKSUN NetVCR ネットワークアナライザ](http://www.scs.co.jp/niksun/sales/netvcr_index.html)
      - [ClearSight公式サイト](http://www.toyo.co.jp/clearsight/)
      - [Colasoft Capsa公式サイト](http://www.colasoft.com/jp/)

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:ネットワーク・アナライザ](https://ja.wikipedia.org/wiki/Category:ネットワーク・アナライザ "wikilink")