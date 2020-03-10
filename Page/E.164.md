> この記事は[E.164](https://ja.wikipedia.org/wiki/E.164)から翻訳されています。


**E.164**は、[ITU-T](../Page/ITU-T.md "wikilink")による[公衆交換電話網](https://ja.wikipedia.org/wiki/公衆交換電話網 "wikilink")などの[電話網](https://ja.wikipedia.org/wiki/電話網 "wikilink") の[電話番号計画](https://ja.wikipedia.org/wiki/電話番号計画 "wikilink")の勧告である。「+」が頭に付けられた、国番号を除いた部分が15桁以下の[電話番号](https://ja.wikipedia.org/wiki/電話番号 "wikilink")として表記される。多くの国の一般の電話からは、国際電話識別番号を付加してダイヤルされる。

初版と改定1版の表題は、「[ISDN](../Page/ISDN.md "wikilink")時代のための電話番号計画」であった。

## カテゴリー

この勧告は、3つのカテゴリーの国際交換電話網の電話番号の機能とその構造に関するものである。

Annex Aは、構造に関する追加情報とE.164番号の機能を勧告する。 Annex Bは、地理的番号のISDN呼び出しのためのネットワーク識別、サービスパラメータ、呼ぶ/関連している回線の識別、ダイヤル方法、およびアドレシングに関する情報を勧告する。使用法において異なる特定のE.164ベースのアプリケーションは別々の勧告で定義される。

番号は、15桁以下である（識別用符号を除く; 1997年より前は、12桁以下のみ許容）。 それぞれのカテゴリのための、割り当て原則とその構造を以下に示す。

### 国別割り当て電話番号

| [国番号](../Page/国際電話番号の一覧.md "wikilink") | 地域番号（オプション） | 加入者番号 |
| -------------------------------------- | ----------- | ----- |
| 国内電話番号                                 |             |       |
| cc=1–3 桁                               | 最大 15-cc 桁  |       |
| 国別割り当て電話番号（最大 15桁）                     |             |       |

### 国際的サービス用電話番号

| [国番号](../Page/国際電話番号の一覧.md "wikilink") | 国際加入者番号 |
| -------------------------------------- | ------- |
| cc=3 桁                                 | 最大 12 桁 |
| 国際的サービス用電話番号（最大**15**桁）                |         |

### 網識別用電話番号

| [国番号](../Page/国際電話番号の一覧.md "wikilink") | [事業者識別番号](https://ja.wikipedia.org/wiki/電気通信事業者 "wikilink") | 加入者番号     |
| -------------------------------------- | ----------------------------------------------------------- | --------- |
| cc=3 桁                                 | x=1–4 桁                                                     | 最大 12–x 桁 |
| 国別割り当て網識別電話番号（最大 15桁）                  |                                                             |           |

### 国家連合への割り当て電話番号

| [国番号](../Page/国際電話番号の一覧.md "wikilink") | [グループ](https://ja.wikipedia.org/wiki/グループ "wikilink")識別番号 | 加入者番号   |
| -------------------------------------- | --------------------------------------------------------- | ------- |
| cc=3 桁                                 | GIC=1 桁                                                   | 最大 11 桁 |
| 国家連合への割り当て電話番号（最大 15桁）                 |                                                           |         |

## E.164に含まれる勧告

### E.164.1

ITU-T 勧告 E.164.1は、E.164国番号と関連識別符号との予約・割当・および再利用のために手順と判断基準について解説する。 利用可能なE.164付番資源の有効で効率的な利用の基礎として評価基準と手順とを提供する。 そのような課題は課題が国際電気通信連合の需要を満たすのを保証するためのITU-TSBと適切なITU-T Study Groupの間の共同作業を必要する。 E.190に含まれた原則とE.164で詳細な付番プラン形式に従って、これらの評価基準と手順の開発がある。

### E.164.2

ITU-T 勧告 E.164.2は、国際的な非営利的な実験を行う目的のために共有されたE.164の3ケタの国番号991を一時的に応募者に割り当てる評価基準と手順とを含んでいる。

### E.164.3

ITU-T 勧告 E.164.2は、国家連合に共有されたE.164国番号の中で資源の課題と改善のための原則・評価基準・および手順について解説する。 これらの共有された国番号はITUによって割り当てられる他のすべてのE.164ベースの国番号に共存する。 共有された国番号に関する資源は、国番号とグループ識別番号と（CC+GIC）から成って、国のグループの中で構成国家が電気通信サービスを提供する能力を提供する。 TSBはCC+GICの課題に責任がある。

## ENUM

E.164電話番号は、[DNSのなかの](../Page/Domain_Name_System.md "wikilink")**e164.arpa**の[ENUM](https://ja.wikipedia.org/wiki/ENUM "wikilink")で使用される。例えば、+1 555 42 42 は、ドットでそれらを切り離して、e164.arpa接尾語を加えて、数を逆にすることによってホストネームに変換できる。

  -
    2.4.2.4.5.5.5.1.e164.arpa

そして、[SIPの](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink")[IP電話](../Page/IP電話.md "wikilink")などのサービスのための[IPアドレス](../Page/IPアドレス.md "wikilink")を調べるためにDNSを使用することができる。 代替方法はDUNDiである。（DUNDiはENUM(\[1\]の[P2P実装](../Page/Peer_to_Peer.md "wikilink")）。 DUNDiはIETFによってまだ規格化されていない。

E.163は、公衆交換電話網の電話番号について勧告した古いITU-T規格であった。[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")では、これが以前、ディレクトリ番号と呼ばれていた。E.163は削除されて、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")のE.164の改定1版に組み入れた。

## 脚注

## 関連項目

  - [電話番号計画](https://ja.wikipedia.org/wiki/電話番号計画 "wikilink") - [電話番号](https://ja.wikipedia.org/wiki/電話番号 "wikilink") - [国際電話番号の一覧](../Page/国際電話番号の一覧.md "wikilink")
  - [単位料金区域](https://ja.wikipedia.org/wiki/単位料金区域 "wikilink") - [電話加入区域](https://ja.wikipedia.org/wiki/電話加入区域 "wikilink") - [市外局番](https://ja.wikipedia.org/wiki/市外局番 "wikilink")
  - [電話番号逼迫対策](https://ja.wikipedia.org/wiki/電話番号逼迫対策 "wikilink")

## 外部リンク

  - <http://www.itu.int>
  - [Downloadable List of International Calling Codes](http://www.aggdata.com/free/international-calling-codes)

[Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:電話番号](https://ja.wikipedia.org/wiki/Category:電話番号 "wikilink") [Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink") [Category:国名コード](https://ja.wikipedia.org/wiki/Category:国名コード "wikilink")

1.  [dundi](http://www.dundi.com/)