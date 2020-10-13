> この記事は[Quality of Service](https://ja.wikipedia.org/wiki/Quality_of_Service)から翻訳されています。


**QoS**（Quality of Service、クオリティ・オブ・サービス）とは、[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")において、重要な通信パケットにマークを付け、優先的に処理する等の方法により、ネットワークの可用性を適切に管理するための技術である\[1\]。サービス品質とも呼ばれる\[2\]日経NETWORK 2004年1月号 「特集2 QoS」p84-p85</ref>\[3\]日経NETWORK 2007年8月号 「特集2 通信品質」p74-p75</ref>。LANスイッチ（レイヤー2スイッチ）等により実現される。

## 概要

QoSの機能を有効化することにより、運ばれるデータの内容に応じて、扱いに差をつけることができる。例えば、[IP電話](../Page/IP電話.md "wikilink")では通話が、動画配信では映像が切れぎれになることは利用者に不快を感じさせるため、同時にネットワークを流れる他のデータよりも優先的に運ばれるようにすると、そのネットワーク回線での利便性が向上する。QoSは主に、**優先制御**と**[帯域制御](../Page/帯域制御.md "wikilink")**に分けられる。\[4\]\[5\]

## 優先制御

### 優先度の決定

[thumb](https://ja.wikipedia.org/wiki/ファイル:ToS\(IP_Precedence\)とDSCPのフォーマット.PNG "wikilink") ルーターやレイヤー3スイッチにおいて実行される優先制御と帯域制御のいずれの機能もパケットの処理順に差を付けるという点では同じである。ルーターがパケットの優先度を決める方法には大きく分けて2つあり、1つは送信元や送信先のIPアドレス、使用プロトコル、ポート番号で決める方法。もう1つはパケットの優先度を明示的にパケット内のフィールドで指定する方法である。後者の場合にはIPヘッダーの中に**[TOS](https://ja.wikipedia.org/wiki/Type_of_service "wikilink")**や**[DSCP](https://ja.wikipedia.org/wiki/DSCP "wikilink")**といったQoS指定の専用フィールドを持つ。

  - **TOS**（Type of service）はIPヘッダーの9～16ビット目のフィールド。先頭の3ビットを「IPプレシデンス」と呼ばれ、8段階の転送優先順位を指定する。
  - **DSCP**（Differentiated services code point）はTOSフィールドの中の先頭の6ビットを使って64段階の転送優先順位を指定する\[6\]\[7\]。

### 優先制御の動作

優先度の低いパケットがいくらキューに溜まっても、優先度の決定に従って、優先度の高いパケットから早く送り出す。このような機能をPQ（Priority queuing）と呼ぶ。

回線が混雑した状況で優先度の高いパケットだけが流れる状況が続けば、優先度の低いパケットは全く流れなくなる場合があり、優先度の低いパケットを送り出したアプリケーションは通信をあきらめてしまうことが起きる。多くのアプリケーションでは、パケットが少しでも流れれば通信を継続するので、優先順位の低いパケットも一定の割合で少しだけ流すことが行なわれる。高機能なルーターでは、こういった低い優先順位に対する送信の重み付けを設定できる**CQ**（Custom queuing、重み付けキュー）や、重み付けしながらなおかつ同じ優先順位のパケット同士での送信を平等化するためにコネクション単位でパケットの行列を細分化して扱う**WFQ**（Weighted fair queuing）という機能が備わっている\[8\]。

## 帯域制御

帯域制御はWAN回線への入り口等で、使用帯域が限られる場合や最低保証の値を指定するために用いられることが多い。

優先度の低いパケットがキューからあふれるとパケットの廃棄が起こる。TCPパケットが廃棄されると再送が発生するため、他のパケットの廃棄にも繋がる。廃棄が多くなると再送によってパケット量が膨れ上がり輻輳（ふくそう）が発生する。これを避けるために、ルーターはある程度、パケットがキューに溜まった時点で、受け取ったTCPパケットの廃棄を行なう。これによってTCPの機能である[フロー制御](https://ja.wikipedia.org/wiki/フロー制御 "wikilink")が働き、パケットの送出端末からの送出量が抑えられる。このような事前廃棄による[輻輳制御](https://ja.wikipedia.org/wiki/輻輳制御 "wikilink")機能を**RED**（Random Early Detection）機能（[ランダム初期検知](https://ja.wikipedia.org/wiki/ランダム初期検知 "wikilink")）と呼ぶ。ルーターが実行するこういった機能も全ての通信を識別している訳ではないので、さらに細かな制御が必要な場合には帯域制御装置が使用される\[9\]\[10\]。

## 優先制御と帯域制御の限界

優先制御と帯域制御はルーターでの機能であるため、ルーターで区分されたインターネット内部では機能しない。パケットの優先度を指定しても[L2スイッチ](https://ja.wikipedia.org/wiki/L2スイッチ "wikilink")や[L3スイッチ](https://ja.wikipedia.org/wiki/L3スイッチ "wikilink")は無視するだけである。

固定的な帯域制御の指定値設定も、実効帯域からずれがあると回線の使用に悪影響が出る。実効帯域が広がっても帯域制御が狭いままでは、回線使用に無駄が生じる。実効帯域が狭くなって帯域制御の設定値上限値以下になれば、帯域制御が機能しなくなりパケット廃棄が起こりやすくなる。こういった固定設定の問題を回避するために、一部の新しいルーターでは、拠点側ルーターから測定用の[UDPパケットをいくつかセンター](../Page/User_Datagram_Protocol.md "wikilink")・ルーターに送って受信間隔や損失情報を送り返してもらい、回線の状況に合わせて帯域制御の指定を動的に変更する機能が備わっているものもある\[11\]。

## その他

### QoS保証の必要性

QoSの保証が必要になる最大の理由は[輻輳](../Page/輻輳.md "wikilink")（ふくそう、Congestion）である。ネットワーク・[トラフィック](https://ja.wikipedia.org/wiki/トラフィック "wikilink")の量が限られていれば、特別の工夫をしなくてもQoSに関する問題はほとんどおこらないからである。輻輳を避けるため[電話網](../Page/電話網.md "wikilink")においては、第1に[アドミッション制御](https://ja.wikipedia.org/wiki/アドミッション制御 "wikilink")が行われる。すなわち QoS が保証できないときには新しいサービス要求を拒絶する。電話網においては第2に個々の呼（Call）を確立する際に、輻輳が起こらないルートを検索して使用する。一方、[インターネット](../Page/インターネット.md "wikilink")をはじめとする [IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")においては、従来、ネットワーク・レベルではこのような制御が行われなかった。そのため、IPネットワークは緊急通信をはじめとする高信頼性が要求される通信用途に使用するのが困難だった。IPネットワークの用途がひろがるにつれて、そこでも QoS保証へのニーズが高まっている。

また、IPネットワーク固有の要因として、近年しだいに QoS保証を必要とする[アプリケーションが増加してきていることがその必要性を高めている](../Page/アプリケーションソフトウェア.md "wikilink")。すなわち、1990年代にはいってからインターネット上で[音声通話](https://ja.wikipedia.org/wiki/音声通話 "wikilink")や動画配信といったリアルタイム・アプリケーションが使われるようになり、またビジネス向けの高品質なサービスも求められるようになってきた。また、データ通信が音声通信を量的に上回り、電話網に匹敵する品質をインターネットにおいて実現することが必要となってきている。これはインターネットからみた表現であるが、電話網の側からみればインターネットに匹敵する（あるいはそれ以上の）柔軟さを新しい通信網すなわち NGN（[Next Generation Network](https://ja.wikipedia.org/wiki/Next_Generation_Network "wikilink")）において実現することが目標となっている。

### IPネットワークにおけるQoS保証

インターネットの標準化は [IETF](../Page/Internet_Engineering_Task_Force.md "wikilink")（Internet Engineering Task Force：インターネット・エンジニアリング・タスク・フォース）において進められているが、QoSに関してもIETFにおいて次のような技術が標準化されている。

  - [IntServ](../Page/IntServ.md "wikilink") (イントサーブ) - 個々の[通信フロー](https://ja.wikipedia.org/wiki/通信フロー "wikilink")ごとにQoSを保証するための技術あるいは枠組みである。
  - [DiffServ](../Page/DiffServ.md "wikilink") (ディフサーブ) - 複数の通信フローをまとめたサービスクラス（Class of service, **CoS**）ごとにQoSを保証するための技術あるいは枠組みである。

### 使用例

QoSは、他者と差別化し優先させることで安定した[スループット](../Page/スループット.md "wikilink")や低遅延を実現している。CoSの使い方としては、[IP電話](../Page/IP電話.md "wikilink")やビデオ会議/[テレビ電話](../Page/テレビ電話.md "wikilink")といった[リアルタイム](../Page/リアルタイム.md "wikilink")系トラフィックを最優先。[SNAといった遅延に弱い基幹系トラフィックや](../Page/Systems_Network_Architecture.md "wikilink")、重要度の高い業務系トラフィックを2番目に優先。[電子メール](../Page/電子メール.md "wikilink")や[Webへの](../Page/World_Wide_Web.md "wikilink")[アクセス](../Page/アクセス.md "wikilink")等遅延が生じても問題にならない情報系トラフィックを最も低い優先度とする。

[300px](https://ja.wikipedia.org/wiki/ファイル:LANスイッチ（レイヤー2スイッチ）の優先度情報.PNG "wikilink")

## LANスイッチでの優先度制御

LANスイッチ（レイヤー2スイッチ）でも、IEEE 802.1Qの[VLAN](https://ja.wikipedia.org/wiki/VLAN "wikilink")で使用される拡張MACフレームのヘッダーに含まれる情報を使って優先度の制御を行なう。拡張MACフレームのヘッダー部の4番目にある「Tag Control Information」フィールドの先頭3ビットが優先度を示す数値になっている\[12\]那須野洋一、岡田孝博著「スイッチ・ネットワーク 不要なパケットは止めて重要なパケットを優先する」　日経NETWORK 2005年8月号　p.171</ref>。

## 参考図書

<references/>

## 関連項目

  - [帯域制御](../Page/帯域制御.md "wikilink")
  - [IntServ](../Page/IntServ.md "wikilink") (イントサーブ)
  - [DiffServ](../Page/DiffServ.md "wikilink") (ディフサーブ)
  - [Class of Service](https://ja.wikipedia.org/wiki/Class_of_Service "wikilink") （CoS）
  - [Type of Service](https://ja.wikipedia.org/wiki/Type_of_Service "wikilink") （ToS）
  - [IP電話](../Page/IP電話.md "wikilink")
  - [IPマルチキャスト](https://ja.wikipedia.org/wiki/IPマルチキャスト "wikilink")
  - [Quality of Experience](https://ja.wikipedia.org/wiki/Quality_of_Experience "wikilink")（QoE）
  - [Resource Reservation Protocol](../Page/Resource_Reservation_Protocol.md "wikilink") （リソース予約プロトコル）
  - [ポリシーベースQoS保証](../Page/ポリシーベースQoS保証.md "wikilink")
  - [トラフィックシェーピング](../Page/トラフィックシェーピング.md "wikilink") - [リーキーバケット](https://ja.wikipedia.org/wiki/リーキーバケット "wikilink")、[トークンバケット](https://ja.wikipedia.org/wiki/トークンバケット "wikilink")

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:ネットワーク技術](https://ja.wikipedia.org/wiki/Category:ネットワーク技術 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.