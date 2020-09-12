> この記事は[Defense4All](https://ja.wikipedia.org/wiki/Defense4All)から翻訳されています。


**Defense4All**は、[OpenDaylight](https://ja.wikipedia.org/wiki/OpenDaylight "wikilink")に統合された最初のオープン[SDN](https://ja.wikipedia.org/wiki/Software_Defined_Networking "wikilink")[セキュリティ](https://ja.wikipedia.org/wiki/ネットワーク・セキュリティ "wikilink")[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")である\[1\]。

## 歴史

2014年、仮想およびクラウドデータセンター向けのアプリケーション配信およびアプリケーションセキュリティソリューションのプロバイダーであるラドウェアは、OpenDaylightに統合されたオープンSDNセキュリティアプリケーションであるDefense4Allを使用して、OpenDaylightプロジェクトへの貢献を発表した。

## 概要

Defense4Allは、クラウドプロバイダーに、ネイティブネットワークサービスとして分散型サービス拒否（[DDoS](https://ja.wikipedia.org/wiki/DoS攻撃#DDoS攻撃 "wikilink")）の検出と緩和を提供する。 [DoS](https://ja.wikipedia.org/wiki/DoS "wikilink") / DDoS保護サービス自体の一部になるようにSDN対応ネットワークをプログラムするOpenDaylight SDNコントローラーを使用して、Defense4Allはオペレーターが仮想ネットワークセグメントごとまたは顧客ごとにDoS / DDoS保護サービスをプロビジョニングできるようにする。Defense4AllはOpenDaylightコントローラー（ODC）ノースバウンドAPIを介してコントローラーと相互作用するアプリケーションとして動作する。 Defense4Allは、コマンドラインインターフェースまたは[RESTful](../Page/Representational_State_Transfer.md "wikilink") [API](https://ja.wikipedia.org/wiki/API "wikilink")のいずれかであることができるネットワークマネージャーのための[ユーザーインターフェース](https://ja.wikipedia.org/wiki/ユーザーインターフェース "wikilink")をサポートしている。最後に、Defense4Allには1つ以上の攻撃軽減装置（AMS）と通信するためのAPIがある。

管理者は、Defense4Allを構成して、保護されたネットワーク（PN）および保護されたオブジェクト（PO）と呼ばれる特定のネットワークおよびサーバーを保護できる。アプリケーションは、対象のPOのトラフィックが流れるすべてのネットワークロケーションに、構成された各POの各[プロトコル](../Page/プロトコル.md "wikilink")のトラフィックカウントフローをインストールするようにコントローラーに指示する。次に、Defense4Allは、構成されたすべてのPOのトラフィックを監視し、関連するすべてのネットワークロケーションからの読み取り値、レート、および平均を要約する。特定のPOのプロトコル（[ICMP](https://ja.wikipedia.org/wiki/ICMP "wikilink")、[TCP](https://ja.wikipedia.org/wiki/TCP "wikilink")、[UDP](https://ja.wikipedia.org/wiki/UDP "wikilink")など）で通常学習されたトラフィック動作からの逸脱を検出した場合、Defense4Allは対象のPOでそのプロトコルに対する攻撃を宣言する。具体的には、Defese4Allは、[OpenFlow](https://ja.wikipedia.org/wiki/OpenFlow "wikilink")を使用して測定したリアルタイムトラフィックの平均を継続的に計算する。リアルタイムトラフィックが平均から80％逸脱すると、攻撃が想定される。

## 防御技法

Defense4Allは、DDoS攻撃を防御するための一般的な手法を使用する。これは、次の三つの要素で構成されている:

  - 疑わしいトラフィックを通常のパスから攻撃軽減装置（AMS）に迂回させ、トラフィックのスクラビング、選択的なソースブロックなどを行う。スクラビングセンターから出るクリーンなトラフィックは、パケットの元の宛先に再注入される。

<!-- end list -->

  - 通常のベースラインから逸脱したトラフィック異常としてのDDoS攻撃パターンの検出。

<!-- end list -->

  - トラフィック統計の収集、および平時における保護オブジェクトの統計動作の学習。保護されたオブジェクトの通常のトラフィックベースラインは、これらの収集された統計から構築される。

検出された攻撃を軽減するために、Defense4Allは次の手順を実行する：

1\. 攻撃軽減装置(AMS)デバイスが有効であることを検証し、AMSデバイスへのライブ接続を選択する。 現在、Defense4Allは、DefenseProと呼ばれるラドウェアのAMSと連携するように構成されている。

2\. 攻撃軽減装置(AMS)をセキュリティポリシーと攻撃されたトラフィックの通常のレートで構成する。これにより、トラフィックが通常の速度に戻るまで緩和策を実施するために必要な情報がAMSに提供される。

3\. 攻撃軽減装置(AMS)から受信した対象トラフィックのSyslogの監視とロギングを開始する。 Defense4Allがこの攻撃に関するAMSからのSyslog攻撃通知を引き続き受信している限り、Defense4Allは、このPOのフローカウンターがそれ以上の攻撃を示さなくても、トラフィックをAMSに誘導し続ける。

4.選択した物理AMS接続を関連するPOリンクにマッピングする。これには通常、OpenFlowを使用して仮想ネットワーク上のリンク定義を変更することが含まれる。

5.優先順位の高いフローテーブルエントリをインストールして、攻撃トラフィックフローをAMSにリダイレクトし、AMSからのトラフィックを通常のトラフィックフロールートに再注入する。 Defense4Allが攻撃が終了したと判断すると（フローテーブルカウンターまたはAMSからの攻撃の兆候はありません）、以前のアクションを元に戻す。対象のトラフィックに関する監視を停止し、トラフィックの宛先変更フローテーブルエントリを削除する。 AMSからのセキュリティ構成。その後、Defense4Allは平時監視に戻る。

## 関連項目

  - [OpenDaylight](https://ja.wikipedia.org/wiki/OpenDaylight "wikilink")
  - [Software Defined Networking](https://ja.wikipedia.org/wiki/Software_Defined_Networking "wikilink")
  - [ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/ネットワーク・セキュリティ "wikilink")
  - [DDoS攻撃](https://ja.wikipedia.org/wiki/DDoS攻撃 "wikilink")
  - [Representational State Transfer](../Page/Representational_State_Transfer.md "wikilink")
  - [OpenFlow](https://ja.wikipedia.org/wiki/OpenFlow "wikilink")

## 脚注

## 参考文献

ウィリアム・スターリングス『Foundations of Modern Networking: SDN, NFV, QoE, IoT, and Cloud』Addison-Wesley Professional、2015年 ISBN 0134175395

## 外部リンク

  - [日本ラドウェア](http://www.radware.co.jp/)
  - [Radware](http://www.radware.com/)
  - [OpenDaylightlight](http://www.opendaylight.org/)

[Category:クラウドコンピューティング](https://ja.wikipedia.org/wiki/Category:クラウドコンピューティング "wikilink") [Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink")

1.  \[<https://support.radware.com/app/answers/answer_view/a_id/16287/~/how-to-download-defense4all-documentation>　How to download Defense4All documentation\]*Redware*