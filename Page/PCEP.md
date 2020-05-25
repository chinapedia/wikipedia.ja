> この記事は[PCEP](https://ja.wikipedia.org/wiki/PCEP)から翻訳されています。


**PCEP**（Path computation element protocol、ピーセップ）は[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")において、[帯域を確保した経路を探すための経路計算を](../Page/帯域幅.md "wikilink")**PCE**（Path computation element）に対してリクエストを行う[プロトコル](../Page/プロトコル.md "wikilink")である。

送信元のルーターが、PCEに対して経路計算のリクエストをすることで、送信先までの通信路に必要な帯域を指定した経路の探索を行なうことができる。PCEを採用することで数百台や数千台ものルーターや光クロスコネクトを含む大規模なネットワークでも、効率的な経路計算を行うことができる。

## 仕組み

### 準備

1.  ネットワークをいくつかのエリアに分け、各エリアごとに**PCE**を1つ配置する
2.  各PCEはOSPF-TEなどで自分のエリア内のネットワーク情報を収集しておく

### サービス

1.  経路を知りたいルーターがPCEPを利用して、自エリアのPCEに帯域条件を含めて送信先までの経路をたずねる
2.  自エリアのPCEから、送信先ルーターに向けた隣接エリアのPCEに対して、PCEPを利用して経路探索要求を送る
3.  経路探索要求を受け取ったPCEが、送信先ルーターに向けた隣接エリアのPCEに対して、PCEPを利用して経路探索要求を順次送ることで経路計算要求が伝達されてゆく
4.  送信先エリアのPCEが経路探索要求を受け取ると、経路を逆にたどる形で担当エリア内での帯域条件に合う経路を探す。送信先からのツリー状に経路を探していく
5.  送信先エリアのPCEや経路中のPCEは、経路探索要求への回答として自エリアの経路候補情報を送り、経路候補情報をリレーしてゆく
6.  最初にルーターからの要求を受け付けたPCEまで経路探索要求が届けば、複数候補から1つを選び、要求を出したルーターに回答を伝える。

### 経路確定後

1.  回答を受けたルーターは帯域予約用の[RSVP](../Page/Resource_Reservation_Protocol.md "wikilink")（Resource reservation protocol）を拡張した**RSVP-TE**等を使用して通信路の設定を行なう

## 規格

RFC 5440: Path Computation Element (PCE) Communication Protocol (PCEP) として標準化されている。

## 出典

  - 日経NETWORK 2007年12月号 『PCEP』 p.80

## 関連項目

  - [IETF (Internet Engineering Task Force)](../Page/Internet_Engineering_Task_Force.md "wikilink")
  - [OSPF](https://ja.wikipedia.org/wiki/OSPF "wikilink")
  - [RSVP](https://ja.wikipedia.org/wiki/RSVP "wikilink")

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")