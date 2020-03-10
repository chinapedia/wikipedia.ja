> この記事は[Systems Network Architecture](https://ja.wikipedia.org/wiki/Systems_Network_Architecture)から翻訳されています。


**Systems Network Architecture** ( **SNA** ) は、[IBM](../Page/IBM.md "wikilink") が[1974年](../Page/1974年.md "wikilink")に作った[コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")・[アーキテクチャであり](../Page/コンピュータ・アーキテクチャ.md "wikilink")、更にはそれに基づいた[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")である。

## 概要

SNAは、[コンピュータ](../Page/コンピュータ.md "wikilink")とその[資源](../Page/資源.md "wikilink")を結ぶ、完全な[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")である。SNA は[プロトコル](../Page/プロトコル.md "wikilink")の体系（仕様）であり、それ自身には[プログラム](../Page/プログラム_\(コンピュータ\).md "wikilink")（製品）は含まない。SNA の実装については、様々な形の[コミュニケーション](../Page/コミュニケーション.md "wikilink")パッケージが出ており、最も有名なものは、[メインフレーム](../Page/メインフレーム.md "wikilink")環境において SNAコミュニケーションを実現する [VTAM](https://ja.wikipedia.org/wiki/VTAM "wikilink") である。

SNA は、[政府](../Page/政府.md "wikilink")の機関、[銀行](../Page/銀行.md "wikilink")、[金融機関](../Page/金融機関.md "wikilink")の[トランザクション](../Page/トランザクション.md "wikilink")ネットワークなど広く使われ、特に企業向けの大規模ネットワークでは[事実上の標準](https://ja.wikipedia.org/wiki/事実上の標準 "wikilink")となった。また最新の[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")、[z/VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink")、[z/VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")にもVTAMは含まれている。しかし現在は[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")に移行しつつある。

## 利点と不利点

SNA は[アプリケーションプログラムからリンクコントロールを除去した](../Page/アプリケーションソフトウェア.md "wikilink")。その機能を、ネットワークコントロール専用のプログラムへ移した。このことは、以下に記す利点と不利点を生んだ。

### 利点

  - テレコミュニケーションネットワークにおける問題の局地化が容易になった。これは、コミュニケーションリンクに関わるソフトウェアの量が、相対的に少なくなったからである。
  - アプリケーションプログラムにコミュニケーションに関する機能を付け加えることが容易になった。ソフトウェアタイマーやプロセッサーへの割込みを要求する手に負えないリンクコントロールの部分を[システムソフトウェア](../Page/システムソフトウェア.md "wikilink")や NCP へ移したからである。

### 不利点

  - SNA ではないネットワークへの接続が困難なこと。SNA の「現在のバージョン」でサポートされないコミュニケーションの仕組みを持つアプリケーションは、困難に直面した。IBM が [X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink") を SNA のサポートに含める前は、X.25 ネットワークへの接続は困難であった。X.25 と SNA [プロトコル](../Page/プロトコル.md "wikilink")のコンバージョンは、NCP ソフトウェアの修正または外部にプロトコルコンバーターを設置することによって可能となった。
  - 一見して、SNA ネットワークは、TCP/IP ネットワークと比較して非常に高価なものとして登場した。小さなネットワークにとっては、それは本当に高価なものだった。しかし成長していく大きなネットワークの複合体にとっては、SNA ストラクチャーは安価なネットワークパスを提供するものだった。

### TCP/IPとの比較

  - VTAMを中心とした中央集権型である(Peer to Peerを謳ったLU6.2は普及しなかった)
  - 同一回線内の複数セッション間で優先順位がつけられる
  - コマンドで特定の接続先(PU、LU)を通信開始や通信切断できる
  - 接続先(PU、LU)とのセッションを常時監視している(ポーリング)
  - 標準で暗号化できる
  - 必要な回線速度が高い精度で見積もりできる
  - 機器が専用であり高価である
  - 専用のスキル・要員が必要である

## 論理ユニットタイプ ( Logical Unit Types )

SNA は、様々な種類の[デバイス](https://ja.wikipedia.org/wiki/デバイス "wikilink")を、各々 a Logical Unit grouping として同定する。LU0 は定義されていないデバイスまたはユーザーが自身で定義したプロトコルを意味する。LU1 は[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")を意味する。LU2 は[ダム端末](../Page/ダム端末.md "wikilink")を意味する。LU3 は[3270プロトコルを用いるプリンターを意味する](../Page/IBM_3270.md "wikilink")。LU4 は[バッチ](https://ja.wikipedia.org/wiki/バッチ処理 "wikilink")[端末](../Page/端末.md "wikilink")を意味する。LU5 は定義されたことがない。LU6 は2つのアプリケーション間のプロトコルを意味する。LU7 は 5250 端末を用いたセッションのために用意されている。使われる最初の LU は、LU1 と LU2、そして [w:LU6.2](https://ja.wikipedia.org/wiki/w:LU6.2 "wikilink") である（ LU6.2 は、アプリケーションとアプリケーションの会話のための進歩したプロトコルである）。

## SNAとOSI参照モデル

SNAは7階層の考え方がある。

また、IBMだけでなく、国際標準としても、通信の考え方を規程する必要が出てきた為、[ISOにより](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、1983年に[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")が制定された。このときISOはIBMのSNAを参考にしたと云われているため、SNAとOSI参照モデルは似た構成になっているが、細部は異なる。

  -
    SNA

  - 第7層　トランザクションサービス層
    第6層　プレゼンテーションサービス層
    第5層　データフローコントロール層
    第4層　トランスミッションコントロール層
    第3層　経路制御層
    第2層　データリンクコントロール層
    第1層　物理制御層

<!-- end list -->

  -
    OSI参照モデル

  - 第7層　アプリケーション層
    第6層　プレゼンテーション層
    第5層　セッション層
    第4層　トランスポート層
    第3層　ネットワーク層
    第2層　データリンク層
    第1層　物理層

## 実装と発表

SNAは1974年9月に「通信の高度化機能」（Advanced Function for Communications）の発表の一部として全世界で発表され、そのSNAの[Synchronous Data Link Control](https://ja.wikipedia.org/wiki/Synchronous_Data_Link_Control "wikilink")（SDLC）[プロトコール](https://ja.wikipedia.org/wiki/プロトコール "wikilink")の実装が次の新製品に行なわれた：

  - [IBM 3767](https://ja.wikipedia.org/wiki/IBM_3767 "wikilink") コミュニケーション端末機（プリンター）
  - IBM 3770 データ・コミュニケーション・システム

これらはIBM/3704/3705通信制御装置のネットワーク・コントロール・プログラム（NCP）やシステム/360とシステム/370の[VTAM](https://ja.wikipedia.org/wiki/VTAM "wikilink")やその他[CICS](../Page/CICS.md "wikilink")、[IMS](../Page/IMS.md "wikilink")などのソフトウェアでサポートされている。このあと、1974年7月にIBM 3760データ・エントリー・ステーション、IBM 3790コミュニケーション・システム。[IBM 3270の新しいモデルとSNAの実装は続いている](../Page/IBM_3270.md "wikilink")。

SNAはおもに米国[IBM](../Page/IBM.md "wikilink")のシステムズ開発部門（Systems Development Division）の[ノースカロライナ](https://ja.wikipedia.org/wiki/ノースカロライナ "wikilink")州[リサーチ・トライアングル・パーク](https://ja.wikipedia.org/wiki/リサーチ・トライアングル・パーク "wikilink")（R.T.P.）製品開発研究所のデザイン部署で行なわれ、それを実装した他の製品開発研究所（IBM 3767は[藤沢研究所](../Page/藤沢市.md "wikilink")、のちの[大和研究所](https://ja.wikipedia.org/wiki/日本IBM大和事業所#IBM大和開発研究所 "wikilink")；IBM 3770はR.T.P.研究所）も援助して行なわれたので、日本人も数人がSNAのデザインに参加している。詳細はのちにIBMのシステム・リファレンス・ライブラリー（SRL）マニュアル、IBM Systems Journalなどで主要部分が公開された。

## 関連項目

  - [通信プロトコル](../Page/通信プロトコル.md "wikilink")
  - [プロトコルスタック](../Page/プロトコルスタック.md "wikilink")
  - [VTAM](https://ja.wikipedia.org/wiki/VTAM "wikilink")
  - [OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")
  - [OSI参照モデル](../Page/OSI参照モデル.md "wikilink")
  - [IBM 3767](https://ja.wikipedia.org/wiki/IBM_3767 "wikilink")

## 外部リンク

  - [Cisco article on SNA](http://www.cisco.com/univercd/cc/td/doc/cisintwk/ito_doc/ibmsna.htm)
  - [APPN Implementers Workshop](http://www.networking.ibm.com/app/aiwhome.htm) Architecture Document repository

[Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")