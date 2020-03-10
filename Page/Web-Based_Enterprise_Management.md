> この記事は[Web-Based Enterprise Management](https://ja.wikipedia.org/wiki/Web-Based_Enterprise_Management)から翻訳されています。


**Web-Based Enterprise Management**（**WBEM**）は、[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")環境の管理を統合するために開発された[システム管理](https://ja.wikipedia.org/wiki/システム管理 "wikilink")技術群の名称である。WBEM は各種[インターネット標準](https://ja.wikipedia.org/wiki/インターネット標準 "wikilink")や[DMTFの](https://ja.wikipedia.org/wiki/Distributed_Management_Task_Force "wikilink")[オープン標準](https://ja.wikipedia.org/wiki/オープン標準 "wikilink")に基づいている（[CIMインフラストラクチャとスキーマ](https://ja.wikipedia.org/wiki/Common_Information_Model "wikilink")、CIM-[XML](../Page/Extensible_Markup_Language.md "wikilink")、CIM over [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[WS-Management](https://ja.wikipedia.org/wiki/WS-Management "wikilink")）。その他のシステム管理手法として、[リモートシェル](https://ja.wikipedia.org/wiki/リモートシェル "wikilink")、独自ソリューション、[SNMPなどを使った](../Page/Simple_Network_Management_Protocol.md "wikilink")[ネットワーク管理](../Page/ネットワーク管理.md "wikilink")などがある。

## アーキテクチャ

WBEMアーキテクチャを解説するため、デバイスを管理しようとしている操作者と、実際のデバイスのハードウェアやソフトウェアの間に WBEM コンポーネントがあると想定する。操作者はデバイスの設定を行い、起動/停止を行い、警告を収集するなどの管理を行う。

1.  操作者には、[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")(GUI)、ブラウザユーザインタフェース(BUI)、[キャラクタユーザインタフェース](../Page/キャラクタユーザインタフェース.md "wikilink")(CUI)のいずれかが与えられるだろう。WBEM にはユーザインタフェースに関する規定がほとんど全くない（一部アプリケーションのCUIは定義されている）。これはWBEMの長所でもあり、システム本体とは無関係にユーザインタフェースを変更することが可能である。
2.  GUI/BUI/CUI は小規模な[APIを経由して](../Page/アプリケーションプログラミングインタフェース.md "wikilink") WBEM クライアントに接続されている。このクライアントは管理しようとしているデバイスのWBEMサーバ（通常そのデバイス自身のある装置上で動作）を探し、XML で要求メッセージを作る。
3.  クライアントは WBEM サーバに HTTP（またはHTTPS）プロトコルで要求を送る。エンコードは CIM-XML 形式である。
4.  WBEM サーバは要求メッセージをデコードし、必要な認証チェックをして、事前に生成された管理対象デバイスのモデルを参照して要求の処理方法を調べる。このモデルが WBEM の中核である。いってみれば、クライアントはモデルとやり取りし、モデルが実際の管理対象（ハードウェアやソフトウェア）とやり取りする。モデルは CIM標準で書かれており、DMTF は典型的な管理対象デバイスやサービスについてのモデルをいくつも公表している（IPルータ、ストレージサーバ、デスクトップコンピュータなど）。
5.  多くの操作では、WBEMサーバは実際のハードウェアやソフトウェアと通信する必要があるか、モデルを使って判断する。その通信は "provider" と呼ばれるWBEMサーバと管理対象との小さなインタフェース用コードで行われる（CMPI という標準インタフェースを使用）。インタフェースがきちんと決まっていて、呼び出しの種類も少ないので、provider を書くのは容易である。特に、provider を書くに当たって GUI/BUI/CUI を気にする必要はない。

## 実装サポート

WBEM は各種コンポーネントから構成されるが、デバイス製造業者やサービス提供業者はどの部分を実装すればよいのか?

  - 第一にモデルを実装する。DMTF が公表している標準モデルを必要に応じて拡張するのが一般的である。
  - 第二にBUI/GUI/CUIを実装する。WBEMのクライアントとサーバは[オープンソース](../Page/オープンソース.md "wikilink")も商用も含め、様々なものが既にあるので、改めて実装する必要はほとんどない。
  - 第三に provider を実装する。

以上のように、WBEMアーキテクチャを用いれば、デバイス製造業者やサービス提供業者は、簡単に標準管理インタフェースに対応することができる。

## 実装

### オペレーティングシステム内の WBEM

  - [OpenWBEM](http://www.novell.com/coolsolutions/feature/14625.html): [ノベルによるオープンソース実装](../Page/ノベル_\(企業\).md "wikilink")。[SUSE Linux Enterprise Serverに実装されている](../Page/SUSE.md "wikilink")
  - [Solaris WBEM Services](http://jp.sun.com/products/software/solaris/seas/wbem/): [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[Solaris](../Page/Solaris.md "wikilink")に実装されている
  - [WMI](https://ja.wikipedia.org/wiki/Windows_Management_Instrumentation "wikilink"): [マイクロソフト](../Page/マイクロソフト.md "wikilink") の[Windowsに実装されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - HP WBEM Services for [HP-UX](../Page/HP-UX.md "wikilink"): [ヒューレットパッカード](https://ja.wikipedia.org/wiki/ヒューレットパッカード "wikilink")のHP-UX 11iv1以降より実装
  - [CimBiote](http://cimbiote.et.redhat.com/): [レッドハット](../Page/レッドハット.md "wikilink")

### WBEM クライアント

  - [PyWBEM](http://pywbem.sourceforge.net/) [Python](../Page/Python.md "wikilink")で書かれたオープンソース WBEM ライブラリ
  - [Purgos](http://www.softulz.net) Windows向けの[C++](../Page/C++.md "wikilink")で書かれたオープンソースクライアント
  - [SBLIM CIM Client for Java](http://sblim.sourceforge.net/)

### クライアントとサーバ

  - [OpenPegasus](http://www.openpegasus.org) オープンソースのクライアントサーバ（C++）
  - [OpenWBEM](http://sourceforge.net/projects/openwbem/) オープンソースのクライアントサーバ（C++）

## 関連項目

  - [SMI-S](https://ja.wikipedia.org/wiki/SMI-S "wikilink")

## 外部リンク

  - [Official WBEM page](http://www.dmtf.org/standards/wbem) （DMTF）標準文書あり

[Category:ネットワーク管理](https://ja.wikipedia.org/wiki/Category:ネットワーク管理 "wikilink") [Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink") [Category:マネジメント・システム](https://ja.wikipedia.org/wiki/Category:マネジメント・システム "wikilink")