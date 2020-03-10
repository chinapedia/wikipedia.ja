> この記事は[ALOHA](https://ja.wikipedia.org/wiki/ALOHA)から翻訳されています。


**ALOHA**（アロハ）は、1972年に[ハワイ大学で開発された](../Page/ハワイ大学システム.md "wikilink")[無線通信](../Page/無線通信.md "wikilink")用の[通信プロトコル](../Page/通信プロトコル.md "wikilink")であり、[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")のMAC副層に位置づけられる。

ALOHAは、多重ランダムアクセス方式を採用しており、この種の通信プロトコルとしては初めての方式である。 この通信プロトコルを元に様々な改良がなされ、最初のものは後に"Pure ALOHA"と呼ばれることになる。

## 背景

1970年代、[コンピュータ](../Page/コンピュータ.md "wikilink")は中央の[汎用コンピュータ](https://ja.wikipedia.org/wiki/汎用コンピュータ "wikilink")にアクセスして処理をしてもらうという形態で使用されていた。 施設が各島に点在しているハワイ大学では、それぞれの施設から中央にアクセスするためのネットワーク化を実現する必要があった。 しかしながら、当時の[ハワイ諸島](https://ja.wikipedia.org/wiki/ハワイ諸島 "wikilink")の[電話回線](https://ja.wikipedia.org/wiki/電話回線 "wikilink")の信頼性は低く、無線通信によるネットワークを形成することになった。 このプロジェクトは**ALOHAプロジェクト**と呼ばれた。（詳細は[ALOHAnet](../Page/ALOHAnet.md "wikilink")を参照のこと）

## 種類

### Pure ALOHA

1972年に開発された、最も古く、最も単純なプロトコル。 最大スループットは18.4%。

1.  送信者は任意のタイミングで[パケット](../Page/パケット.md "wikilink")を送信することができる
2.  パケットが正常に受信されたら、受信者は受信確認パケット (ACK; Acknowledgment packet) を送信する
3.  送信者は一定時間経過後もACKが帰ってこない場合には、ランダムな時間後に再送する
      - 受信側がACKを送信していても、送信側が正常にACKを受信できない場合には再送することになる

この方式では、ノード数の増加にしたがって衝突が発生する確率が高くなり、パケットの一部が衝突しただけで再送する必要が出てくる。

`|Packet of Node A|<-送信成功         |Packet of Node A|<-送信失敗（衝突）`
`                       |Packet of Node B|<-送信失敗（衝突）`

### Slotted ALOHA

Pure ALOHAの改良版のプロトコルで、Pure ALOHAが任意のタイミングでの送信を許可していたのに対し、一定間隔でタイムスロットを設けて送信タイミングを制御している。 それ以外はPure ALOHAと同様の手順で送受信が行われる。 これによりパケットの一部だけが衝突しても再送しなければならないという制約が無くなり、最大スループット36.8%と通信効率が飛躍的に向上した。

`|    Timeslot    |    Timeslot    |    Timeslot    |    Timeslot    |`
`|Packet of Node A|<-送信成功                        |Packet of Node A|<-送信失敗（衝突）`
`                 |Packet of Node B|<-送信成功       |Packet of Node B|<-送信失敗（衝突）`

### r-ALOHA

r-ALOHA（予約ALOHA, Reservation ALOHA）は、Slotted ALOHA方式を用いて予約情報を載せて送信し、それ以降のフレーム（複数からなるスロット）を予約する方式である。 予約に成功した場合は、そのフレーム（後に続くスロット）はすでに予約済みとみなされ、予約に成功したノード以外は送信を行わない。

`|rsrv/data|rsrv/data|rsrv/data|rsrv/data|rsrv/data|rsrv/data|rsrv/data|・・・`
`|<-------------------- Frame -------------------->|`

### ALOHA-Reservation

r-ALOHAとの違いは、各フレームに予約のためのスロットが設けられていて、そのタイミングで予約を行うことである。

`| reserve |data-slot|data-slot|data-slot|data-slot| reserve |data-slot|・・・`
`|<-------------------- Frame -------------------->|`

## 関連項目

  - [CSMA/CA](https://ja.wikipedia.org/wiki/CSMA/CA "wikilink")
  - [IEEE 802.11](https://ja.wikipedia.org/wiki/IEEE_802.11 "wikilink")
  - [無線LAN](../Page/無線LAN.md "wikilink")

[en:ALOHAnet\#The ALOHA protocol](https://ja.wikipedia.org/wiki/en:ALOHAnet#The_ALOHA_protocol "wikilink")

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")