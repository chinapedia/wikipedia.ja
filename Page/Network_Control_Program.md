> この記事は[Network Control Program](https://ja.wikipedia.org/wiki/Network_Control_Program)から翻訳されています。


**Network Control Program**（ネットワーク コントロール プログラム、**NCP**）とは、[ARPANET](../Page/ARPANET.md "wikilink")ホストコンピュータ上で動作する[プロトコルスタックの共通要素を提供するものである](../Page/通信プロトコル.md "wikilink")。NCPは遠隔に存在するホストコンピュータ間でプロセス間接続と[フロー制御](https://ja.wikipedia.org/wiki/フロー制御 "wikilink")を行う。電子メールやファイル転送などのアプリケーションサービスは他のホストコンピュータへの接続を制御するためにNCPのインターフェイスを使用する。

ARPANETの物理層・データリンク層・ネットワーク層のプロトコルはホストコンピュータとは別の [Interface Message Processor](../Page/Interface_Message_Processor.md "wikilink")(IMP) に実装されていた。ホストコンピュータの持つプロトコルスタックの下に IMP の高信頼パケット転送システムが接続されている。IMPの仕様は BBN Report 1822 の Host/IMP Protocol で示されている。

NCP はホストコンピュータ上のプロトコルスタック常駐部の共通層である。低レベルプロトコルはIMPで提供されるので、NCP は基本的にトランスポート層に相当する *ARPANET Host-to-Host Protocol* (AHHP) と *Initial Connection Protocol* (ICP) から構成されている。AHHP はホスト間の単方向のフロー制御されたデータストリームに関するプロトコルである。ICP はそのようなデータストリームを2本接続して双方向通信を確立するプロトコルである。アプリケーション層プロトコル（[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[SMTPなど](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")）は NCP を通してネットワークサービスにアクセスする。これは後のソケットに相当するものである。

[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")[1月1日](../Page/1月1日.md "wikilink")、ARPANET はネットワークプロトコルを NCP からもっと柔軟で強力な [TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink") に切り替えた。すなわち、この日に今日[インターネット](../Page/インターネット.md "wikilink")と呼ばれているネットワークが起動したのである。

## 参考文献

<div class="references-small">

  -
  -
  -

</div>

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:インターネットの歴史](https://ja.wikipedia.org/wiki/Category:インターネットの歴史 "wikilink")