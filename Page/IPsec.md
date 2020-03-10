> この記事は[IPsec](https://ja.wikipedia.org/wiki/IPsec)から翻訳されています。


**IPsec**（Security Architecture for Internet Protocol、アイピーセック）は、 [暗号技術を用いることで](../Page/暗号理論.md "wikilink")、[IP](../Page/Internet_Protocol.md "wikilink") パケット単位で[改竄](../Page/改竄.md "wikilink")検知や秘匿機能を提供する[プロトコル](../Page/プロトコル.md "wikilink")である。これによって、暗号化をサポートしていない[トランスポート層](../Page/トランスポート層.md "wikilink")や[アプリケーションを用いても](../Page/アプリケーションソフトウェア.md "wikilink")、[通信](../Page/通信.md "wikilink")路の途中で、通信内容を覗き見られたり改竄されることを防止できる。

IPsecは、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では必須とされた時期\[1\]があり、専用の拡張ヘッダが定義されている。一方、[IPv4](../Page/IPv4.md "wikilink")では、利用可能だが必須ではなく、IP ヘッダオプションを利用する。

## バージョン

IPsecの規格は[IETFの](../Page/Internet_Engineering_Task_Force.md "wikilink") ipsec wg にて策定し、[RFCとして公開している](../Page/Request_for_Comments.md "wikilink")。IETF ではIPsecにバージョン番号を与えていないが、非公式に下記のバージョンが与えられて\[2\]おり、2016年現在のバージョンはIPsec-v3である：

  - IPsec-v1：RFC182x 形式のもの
  - IPsec-v2：RFC240x 形式のもの
  - IPsec-v3：RFC430x 形式のもの

## プロトコル概要

### 構成

IPsecは、2つの**ピア**の間に**SA** ([Security Association](https://ja.wikipedia.org/wiki/Security_Association "wikilink"))という単方向コネクションを確立することで、ピア間にセキュアな通信を確立する（詳細後述）。なお、SAは、単方向であるため、双方向通信を行う場合には、上りと下りの2つのSAを確立する必要がある。

ピアは、**ホスト**と**セキュリティ・ゲートウェイ**の二種類に分類できる。前者は、個人端末やサーバのようなIP通信の端点に相当する機器である。後者は、ルータのようなIP通信の中継を担う機器である。

IPsecは、原理的にはピアがどちらのタイプであるのかを問わない。したがって、ホストからホストまでの通信全体を直接1つのSAで保護することもできるし、2つの中継地点間毎に別々のSAを確立して通信を保護するリレー形態の運用も可能である。しかし後述するように、ピアがどちらのタイプであるかによって推奨される通信モードが存在する。

IPsecの各ピアは、**SPD**（security policy database）、**SAD**（security association database）という2つのデータベースを管理する。

SPDは、IPアドレス、プロトコル(TCP/UDP/ICMP等)、TCPポートといった情報に応じて、パケットを破棄（discard）するのか、IPsecを使わずに送信（bypass IPsec）するのか、IPsecを使って送信（apply IPsec）するのかを決める**セキュリティポリシー**のデータベースである。

一方、SADは、各ピアとSAを確立する際に用いるパラメータのデータベースである。

### プロトコルの流れ

ピアSがピアRに向けてIPsecで通信するには、以下の3ステップを踏む。

  - SからRへのSAを確立する。
  - SAを使ってパケットをSがRに暗号通信する。
  - Rがデータを受信し、復号などの必要処理を行う。

第一ステップであるSAを確立する段階では、鍵共有プロトコルが実行される。このときに共有された鍵を用いて、第二ステップで通信を暗号化し、第三ステップで復号する。 以下では、この3つのステップの概略を述べる。

#### SAの確立

ピアSは、自身のSPDを参照することで、上位レイヤのプロトコルがRに送ることを要求したパケットを廃棄するのか、そのまま送るのか、それともIPsecで保護して送るのかを決定する。

IPsecで保護して送ることに決定した場合、ピアSは、SAの確立に必要なデータがすでにSADに存在するかどうかを確認する。データが揃っていれば、それらのデータをSADから読み込む。

一方、SAの確立に必要なデータがSADにすべて揃っていない場合は、SAに必要な情報を確立するプロトコルである**IKE**（Internet Key Exchange）をピアRとともに実行する。2016年現在、IKEの最新版はIKEv2である。

IKEは、上述のように、SAに必要な情報を確立するプロトコルであるが、その中でメインとなるのはその名称が示す通り、ピアRとの鍵共有である。

なお、SAに必要な情報を確立するプロトコルとして、IKEの代わりに (KINK)やIPSECKEY DNS recordsを使用することもできる\[3\]\[4\]\[5\]\[6\]。

#### 暗号通信

SAが確立された後、ピアSとRは、以下の2つのうちいずれかのプロトコル用いて、通信を行う（原理的には、両方のプロトコルを適用することも可能である）：

  - **AH** (Authentication Header) ：IPパケットに[メッセージ認証子](https://ja.wikipedia.org/wiki/メッセージ認証符号 "wikilink")(MAC)をつけるが暗号化は行わない。[IPプロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号一覧 "wikilink") 51。
  - **ESP** (Encapsulated Security Payload) ：IPパケットに[認証暗号を施す](https://ja.wikipedia.org/wiki/認証付き暗号 "wikilink")。[IPプロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号一覧 "wikilink") 50。

AHやESPの暗号処理に必要な共通鍵は、SAの確立の際に生成もしくは読み込んだものを用いる。

認証暗号は、平文の暗号化とメッセージ認証の両方を実行できる共通鍵暗号方式である。したがって、ESPを用いた場合、パケットの秘匿性と改竄検知の両方が担保される。一方、AHを用いた場合、改竄検知しか担保されない。

通信は、以下の2つのいずれかの動作モードに従って行う：

  - **トランスポートモード**：パケットデータ部のみを暗号処理を施す。
  - **トンネルモード**：ヘッダを含めたパケット全体を丸ごと「データ」として暗号処理を施し新たな[IPヘッダ](https://ja.wikipedia.org/wiki/IPヘッダ "wikilink")を付加。

トランスポートモードは、主に2つのホスト間の通信で使われ、トンネルモードは、主にセキュリティ・ゲートウェイとセキュリティ・ゲートウェイ、およびセキュリティ・ゲートウェイとホストの間の通信で使われる。

#### 受信時の処理

ピアRは、パケットを受け取り、SADの記載に従って、パケットを破棄するか否かを決める。そして、パケットがIPsecのものであれば、パケットを復号し（暗号化されている場合）、さらにメッセージ認証の検証を行った上で、上位レイヤーのプロトコルにパケットを渡す。パケットがIPsecではなく通常のIPのものである場合、復号などの処理を施さず、直接上位レイヤーのプロトコルにパケットを渡す。

## 利用する暗号方式

特に断りがない限り本節の記述はRFC 7321 2.3-2.4節で要求レベルがSHOULD以上のものに基づいた。

AHのMACとして[AES](../Page/Advanced_Encryption_Standard.md "wikilink")-[GMACがSHOULD](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink")+、AES-XCBC-MAC の出力を96ビットに切り詰めたもの（AES-XCBC-MAC-96）がSHOULDである。NULL（＝MAC無し）もMAYである。

ESPの認証暗号として[AES](../Page/Advanced_Encryption_Standard.md "wikilink")-[GCMがSHOULD](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink")+である。Encryption-then-Mac (EtM)型の認証暗号としては、暗号部分はNULL （＝暗号化しない）とAES-CBCがMUSTであり、MAC部分はHMAC-SHA1の出力を96ビットに切り詰めたもの(HMAC-SHA1-96)がMUST、鍵長128ビットのAES-GMACがSHOULD+、AES-XCBC-MAC の出力を96ビットに切り詰めたもの（AES-XCBC-MAC-96）がSHOULDである。

ただし以上の要求レベルは過去の経緯にも基づいており、安全性や効率の観点から見た場合はAHにはAES-GMAC、ESPにはAES-GCMを推奨している(RFC 7321 4.1節、4.3節)。

## 各プロトコルの詳細

### AH

**AH** (Authentication Header) は、認証および改竄防止機能を提供する。データそのものは暗号化されないので、盗聴防止には利用できない。RFC 1826 形式の AH には再送防止機能 (Anti Replay Counter) が無いが、RFC 2402 では 32 bit の、RFC 4302 では 64 bit のカウンタが付けられており、過去に送信されたパケットがコピー再送されても多重受信しない機能がオプションとして利用できる。

<center>

<table>
<caption>style="background:#781549; color:white;" |<em>Authentication （AH）ヘッダー</em> フォーマット （RFC2402/RFC4302形式）</caption>
<thead>
<tr class="header">
<th><p><em>Offsets</em></p></th>
<th><p>Octet<sub>16</sub></p></th>
<th><p>0</p></th>
<th><p>1</p></th>
<th><p>2</p></th>
<th><p>3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Octet<sub>16</sub></p></td>
<td><p>Bit<sub>10</sub></p></td>
<td><p>0</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td><p>0</p></td>
<td><p><em>Next Header</em></p></td>
<td><p><em><a href="https://ja.wikipedia.org/wiki/ペイロード_(コンピュータ)" title="wikilink">ペイロード長</a></em></p></td>
<td><p><em>予約済み</em></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p>32</p></td>
<td><p><em>Security Parameters Index (SPI)</em></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>64</p></td>
<td><p><em>順序番号</em></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>C</p></td>
<td><p>96</p></td>
<td><p><em>Integrity Check Value (ICV)</em><br />
…</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>…</p></td>
<td><p>…</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

</center>

### ESP

**ESP** (Encapsulated Security Payload) は [ペイロード部を暗号化する](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")。正確には、IP ヘッダ、経路ヘッダ、ホップバイホップオプションヘッダを除いた部分が暗号化される。RFC 1827 形式の ESP には認証機能が無いが、RFC 2406 / RFC 4303 形式の ESP にはオプションとして「認証トレイラー」機能があり、AH を併用せずとも改竄防止機能を利用することが可能となっている (ただし保証されるのはデータ部分だけで、IP ヘッダ部分の改竄を検出することはできない)。また後者には AH 同様に再送防止機能も追加されている。

RFC 1826 / RFC 1827 形式の AH/ESP はそれ以降の RFC とヘッダ長が異なるため互換性がない。RFC 4302 / RFC 4303 形式の 64 bit カウンタは ESN (Extended Sequence Number) とも呼ばれるが、実際にパケットに付加されるのは下位 32 bit だけで、見た目は RFC 2402 形式のパケットと区別が付かない。ただし認証ベクタ (ICV) の算出には全 64 bit が使用されるため、RFC 2402 / RFC 2406 形式の IPsec と RFC 4302 / RFC 4303 形式の IPsec の間にも直接の互換性はない。RFC 4302 / RFC 4303 仕様の IPsec 実装で RFC 2402 / RFC 2406 形式と通信するためには、32 bit の互換カウンタ使用を明示指定する必要がある。

<center>

<table>
<caption>style="background:#781549; color:white;" |<em>Encapsulating Security Payload</em>（ESP） フォーマット （RFC2406/RFC4303形式）</caption>
<thead>
<tr class="header">
<th><p><em>Offsets</em></p></th>
<th><p>Octet<sub>16</sub></p></th>
<th><p>0</p></th>
<th><p>1</p></th>
<th><p>2</p></th>
<th><p>3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Octet<sub>16</sub></p></td>
<td><p>Bit<sub>10</sub></p></td>
<td><p>0</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td><p>0</p></td>
<td><p><em>Security Parameters Index (SPI)</em></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p>32</p></td>
<td><p><em>順序番号</em></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>64</p></td>
<td><p><em><a href="https://ja.wikipedia.org/wiki/ペイロード_(コンピュータ)" title="wikilink">ペイロード</a></em></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>…</p></td>
<td><p>…</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>…</p></td>
<td><p>…</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>…</p></td>
<td><p>…</p></td>
<td><p> </p></td>
<td><p><em>Padding (0-255 octets)</em></p></td>
<td><p> </p></td>
<td></td>
</tr>
<tr class="even">
<td><p>…</p></td>
<td><p>…</p></td>
<td><p> </p></td>
<td><p><em>Pad Length</em></p></td>
<td><p><em>Next Header</em></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>…</p></td>
<td><p>…</p></td>
<td><p><em>Integrity Check Value (ICV)</em><br />
…</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>…</p></td>
<td><p>…</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

</center>

### IKE

**IKE** (Internet Key Exchange protocol) は SAを構築するのに必要な情報の交換を安全に行うプロトコル。IKEv1 (RFC 2409) と IKEv2 (RFC 4306) が定義されており、2016年現在の最新版は後者である。

また IKEv1/v2 以外にも Photuris (RFC 2522), KINK (RFC 4430) などの鍵交換プロトコルが提案されている。

#### IKEv2

#### IKEv1

IKEv1は Internet Key Exchange protocol version 1 の意味であり、[UDP](../Page/User_Datagram_Protocol.md "wikilink")[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")500上で通信される[鍵交換](https://ja.wikipedia.org/wiki/鍵交換 "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")である。開発時には ISAKMP/Oakley と呼ばれた過去があり、これはISAKMP(Internet Security Association and Key Management Protocol)プロトコルの上で Oakley 鍵交換手順を実装したものという意味である。すなわち、IKEv1 は ISAKMP と必ずしも同じものではない。

IKEv1 はフェーズ1、フェーズ2と呼ばれる二段階の手順で鍵交換を行う。まずフェーズ1で IKE プロトコル同士の認証と暗号交換を行い（これをISAKMP SA交換とも呼ぶ）、フェーズ2で IPsec の適用条件と鍵情報の交換を行う（IPsec SA 交換とも呼ぶ）。 フェーズ1には Main Mode,Aggressive Mode と呼ばれる2つの手順がある。前者は ISAKMP 仕様における Identity Protection Exchange 手順の呼び名であり、後者は ISAKMP 仕様における Aggressive Exchange 手順の呼び名である。（用語定義の錯綜と難解さも IKE の理解を難しくしている理由の一つである）。 フェーズ2の通信はフェーズ1において成立した共有鍵を用いて暗号化される。フェーズ2の手順は Quick Mode と呼ばれ、これは ISAKMP にはなく IKEv1 で新たに定義されたものである。IKEv1 の規格上では New Group Mode という手順も定義されているが、実際には殆ど使われていない。

Oakley 鍵交換手順は[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")を用いた鍵交換手順のアルゴリズムとパラメータのセットをいくつか定めたもので、アルゴリズムは大きく分けて [Diffie-Hellman鍵共有](https://ja.wikipedia.org/wiki/Diffie-Hellman鍵共有 "wikilink") (DH-MODP) と[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink") (EC2N) の2種がある。鍵長は DH-MODP で768,1024,1536,2048,3072,4096,6144,8192bit、EC2N で155,188,163,283,409,571bit が定義されている。

IKE の通信を行う[ノードを](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink") IKE ピアと呼び、IKE 要求を発行する側をイニシエータ、受信した側をレスポンダと呼ぶ。Oakley のパラメータや IPsec SA の詳細はイニシエータ側が使用可能な組み合わせを提示し（これをプロポーザルと呼ぶ）、レスポンダ側が最も適切と判断したものを選択して合意を取るという手順を踏む。何をもって「適切」とみなすかは実装と設定に依存し、これを「ポリシー」と呼ぶ場合もあるが、狭義の意味における IPsec Security Policy とは必ずしも同じニュアンスではないので混同しないよう注意が必要である。用語の混同を避けるため、RFC 4301 においてはこれら「鍵交換時の挙動を定めるパラメータの一覧」を Peer Authorization Database (PAD) と呼んでいる。

Aggressive Mode はフェーズ1におけるプロポーザル手順の一部を削減し、パラメータの一部を決め打ちとすることで Main Mode にくらべパケット交換回数を減らし（3往復6パケット → 1.5往復3パケット）通信効率を向上している。ただし Main Mode では最後に交換される ID パケットが暗号化されるのに対し、Agressive ModeではID情報が暗号化されないまま送信されるので、盗聴によるセキュリティホールを招きかねないというリスクもある。フェーズ1にどちらのモードを用いるかはイニシエータに依存し、やはりそのネットワークにおけるポリシー (PAD) によって決定される。

IKEv1 では鍵交換と同時に相手ピアの[認証](../Page/認証.md "wikilink")を行う。認証アルゴリズムもフェーズ1において提示-合意のプロセスを踏んで実行され、認証方式には事前鍵共有方式 (PSK:Pre Shared Key)、デジタル署名方式 (Digital Signatures)、公開鍵暗号方式 (Public Key Encryption) などがある。

フェーズ2で生成される IPsec SA の鍵情報は、原則としてフェーズ1で生成された共有鍵情報から生成される。しかし複数個の IPsec SA をまとめて生成するような使用法の場合、全ての IPsec SA 情報が1つの秘密情報に依存することは好ましくない場合がある。このような場合、IKEv1 では [Perfect Forward Secrecy](https://ja.wikipedia.org/wiki/Forward_secrecy "wikilink") (PFS) と呼ばれるオプション機能の利用が（通信ピア双方に実装されていれば）可能である。PFS は個々のフェーズ2交換時に新たな Oakley 鍵交換を行い、個々に異なった共有鍵を生成して IPsec SA の秘密鍵生成時に適用するものである。PFSは一般に通信秘匿性を向上させるがピアの処理負荷も向上させるため、これを適用すべきか否かもポリシー（あるいはPAD）に応じて決定すべきとされている。

なお1回のフェーズ1交換に付随するフェーズ2の回数を1回かぎりに制限することにより、結果的に全てのフェーズ2生成鍵を異なったものにすることで PFS と同等の秘匿性を得る実装もあり、これを Master PFS と呼ぶこともある。この場合、上記の「狭義のPFS」は Session PFS と呼ばれて区別される。

このように IKEv1 には数多くのモードとパラメータとオプションの組み合わせがあり、さらに多くの拡張仕様が存在する。その中には標準案として提案されたもののドラフトを通過できず、正式な [RFC](../Page/Request_for_Comments.md "wikilink") として記載されずに終わったものも少なくない。また IKEv1 仕様には難解で紛らわしい用語が錯綜しているため、実装系において独自の名前を与えている場合もある（例えば Microsoft Windows では IPsec におけるセレクタをフィルタと呼び、ポリシーをアクションと呼んでいる)。このため「IETF標準」であるはずの IKEv1 同士でも異機種間接続のためにはプロトコルおよび製品実装の深遠な理解が必要になってしまい、「IPsec でネットワークを組む場合は同じメーカーの同じ機器を使用することが最も確実」という慣習を生むことになってしまった。

IETF は混沌としてしまった IKEv1 の整理を諦め、[IKEv2](https://ja.wikipedia.org/wiki/IKEv2 "wikilink") をもって標準化の仕切り直しを図っている。

## IPsec の特徴

### 暗号化する層

IPsecは[ネットワーク層](../Page/ネットワーク層.md "wikilink")でセキュリティを実現するプロトコルであるため、アプリケーションなどの上位層が暗号化をサポートしていない場合でも通信全体としてのセキュリティを担保することが出来る。なおセキュリティをネットワーク層で実現しているため、アプリケーション層でセキュリティを実現している[TLSのように暗号化がどのプロトコルで行われているかをユーザーが容易に知ることはできない](../Page/Transport_Layer_Security.md "wikilink")(TLSではwebブラウザに鍵マークが表示されるなど一見してそれが分かる表示がされる場合がある)。 PCやスマートフォンなどのコンシューマ端末でもIPsecを利用することは可能であるが、現状は専門の技術者が管理するGateway間で[VPN](https://ja.wikipedia.org/wiki/VPN "wikilink")として利用されることが多い。IPsecをVPNで利用する場合はIPアドレスを二重に付加するトンネルモードが利用できるが、[IP以外のパケットも伝達するため](../Page/Internet_Protocol.md "wikilink")[L2TPなどのプロトコルと併用される場合もある](../Page/Layer_2_Tunneling_Protocol.md "wikilink")。

### 柔軟さと設定の複雑さ

IPsecはAHの認証機能、ESPの暗号機能を組み合わせて使うことができ、AH/ESPそれぞれに様々なアルゴリズムを指定することができる。この柔軟さが IPsec の利点ではあるが、設定可能な組み合わせは膨大となり、通信する二点間で全ての設定が一致していなければ通信が成立しない。多台数間のIPsec情報を手動で設定することは非常に手間がかかる上に、手動設定の場合は同じ鍵情報を長期間使い続けることになるため、セキュリティ強度の観点からも好ましくない。IPsecが上述したVPNで利用されることが多いのはこのためである。 この手間を軽減するためネットワークで自動鍵交換を行う[IKEv](https://ja.wikipedia.org/wiki/Internet_Key_Exchange "wikilink")1,IKEv2,[KINK](https://ja.wikipedia.org/wiki/Kerberized_Internet_Negotiation_of_Keys "wikilink"),[Photuris](https://ja.wikipedia.org/wiki/Photuris "wikilink")などのプロトコルも提案されているが、各プロトコルには互換性が無い。最も普及しているIKEv1でも動作モード、認証パラメータ、認証方式、鍵交換アルゴリズム、暗号アルゴリズム及び認証アルゴリズムなど設定項目の組み合わせは多岐に渡り、IPsecを使いこなすには総じて高度な専門知識が要求される。

## IPsec が使えるシステム

  - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") - [Windows2000](../Page/Microsoft_Windows_2000.md "wikilink") / [XP](../Page/Microsoft_Windows_XP.md "wikilink") は IPv4, IPv6 で利用可能であるが、IPv6はESP暗号化に対応していない。[Windows VistaはIPv](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")4、IPv6で利用可能である。
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") - [KAME](https://ja.wikipedia.org/wiki/KAME "wikilink")由来のIPsecが利用可能。OS標準のGUIで利用出来るのはL2TP / IPsecのみである。
  - BSD - [FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")では[KAME](https://ja.wikipedia.org/wiki/KAME "wikilink")で作られた実装が取り込まれており、[OpenBSD](../Page/OpenBSD.md "wikilink")では独自に実装を行っている。
  - Linux - IPv4、IPv6で利用可能。IKEは[KAME](https://ja.wikipedia.org/wiki/KAME "wikilink")由来のipsec-toolsのracoonを利用する。他に[FreeS/WAN](https://ja.wikipedia.org/wiki/FreeS/WAN "wikilink")プロジェクトから派生した[Openswan](https://ja.wikipedia.org/wiki/Openswan "wikilink")と[strongSwan](https://ja.wikipedia.org/wiki/strongSwan "wikilink")がある。

## 歴史

In December 1993, the Software IP Encryption protocol [swIPe (protocol)](https://ja.wikipedia.org/wiki/swIPe_\(protocol\) "wikilink") was researched at [Columbia University](https://ja.wikipedia.org/wiki/Columbia_University "wikilink") and [AT\&T Bell Labs](https://ja.wikipedia.org/wiki/AT&T_Bell_Labs "wikilink") by John Ioannidis and others.

Based on the funding from the [Clinton administration](https://ja.wikipedia.org/wiki/Presidency_of_Bill_Clinton "wikilink") in hosting whitehouse.gov email (from June 1 of 1993 to January 20 of 1995) at [Trusted Information Systems](https://ja.wikipedia.org/wiki/Trusted_Information_Systems "wikilink"), Wei Xu started in July 1994 the research on IP Security, enhanced the IP protocols, developed the IPSec product on the [BSDI](https://ja.wikipedia.org/wiki/BSDI "wikilink") platform, and quickly extended it on to [Sun OS](https://ja.wikipedia.org/wiki/Sun_OS "wikilink"), [HP UX](https://ja.wikipedia.org/wiki/HP_UX "wikilink"), and other UNIX systems. Upon the success, Wei was facing another challenge by the slow performance of computing [DES](../Page/Data_Encryption_Standard.md "wikilink") and [Triple DES](https://ja.wikipedia.org/wiki/Triple_DES "wikilink"). The assembly software encryption was unable to support even a [T1](https://ja.wikipedia.org/wiki/Digital_Signal_1 "wikilink") speed under the [Intel 80386](../Page/Intel_80386.md "wikilink") architecture. By exporting the Crypto cards from Germany, Wei further developed an automated device driver, known as [plug-and-play](https://ja.wikipedia.org/wiki/plug-and-play "wikilink") today, in integrating with the hardware Crypto. After achieving the throughput much higher than a T1s, Wei Xu finally made the commercial product practically feasible, that was released as a part of the well-known Gauntlet firewall. In December 1994, it was deployed for the first time in production for securing some remote sites between east and west coastal states of the United States.

Another IP Encapsulating Security Payload (ESP)\[7\] was researched at the [Naval Research Laboratory](https://ja.wikipedia.org/wiki/Naval_Research_Laboratory "wikilink") as part of a [DARPA](https://ja.wikipedia.org/wiki/DARPA "wikilink")-sponsored research project, with openly published by [IETF](https://ja.wikipedia.org/wiki/IETF "wikilink") SIPP\[8\] Working Group drafted in December 1993 as a security extension for SIPP. This [ESP](https://ja.wikipedia.org/wiki/#Encapsulating_Security_Payload "wikilink") was originally derived from the US Department of Defense [SP3D](https://ja.wikipedia.org/wiki/SP3D "wikilink") protocol, rather than being derived from the ISO Network-Layer Security Protocol (NLSP). The SP3D protocol specification was published by [NIST](https://ja.wikipedia.org/wiki/NIST "wikilink"), but designed by the Secure Data Network System project of the US Department of Defense. The Security Authentication Header ([AH](https://ja.wikipedia.org/wiki/#Authentication_Header "wikilink")) is derived partially from previous IETF standards work for authentication of the [Simple Network Management Protocol](../Page/Simple_Network_Management_Protocol.md "wikilink") (SNMP) version 2.

In 1995, The IPsec working group in the IETF was started to create an open freely available and vetted version of protocols that had been developed under NSA contract in the [Secure Data Network System](https://ja.wikipedia.org/wiki/Secure_Data_Network_System "wikilink") (SDNS) project. The SDNS project had defined a Security Protocol Layer 3 (SP3) that had been published by NIST and was also the basis of the ISO Network Layer Security Protocol (NLSP).\[9\] Key management for SP3 was provided by the Key Management Protocol (KMP) that provided a baseline of ideas for subsequent work in the IPsec committee.

IPsec is officially standardised by the [Internet Engineering Task Force](../Page/Internet_Engineering_Task_Force.md "wikilink") (IETF) in a series of [Request for Comments](../Page/Request_for_Comments.md "wikilink") documents addressing various components and extensions. It specifies the spelling of the protocol name to be *IPsec*.\[10\]

## 関連するRFC

### 標準化過程(Standards Track)

  - RFC 1829: The ESP DES-CBC Transform
  - RFC 2403: The Use of HMAC-MD5-96 within ESP and AH
  - RFC 2404: The Use of HMAC-SHA-1-96 within ESP and AH
  - RFC 2405: The ESP DES-CBC Cipher Algorithm With Explicit IV
  - RFC 2410: The NULL Encryption Algorithm and Its Use With IPsec
  - RFC 2451: The ESP CBC-Mode Cipher Algorithms
  - RFC 2857: The Use of HMAC-RIPEMD-160-96 within ESP and AH
  - RFC 3526: More Modular Exponential (MODP) Diffie-Hellman groups for Internet Key Exchange (IKE)
  - RFC 3602: The AES-CBC Cipher Algorithm and Its Use with IPsec
  - RFC 3686: Using Advanced Encryption Standard (AES) Counter Mode With IPsec Encapsulating Security Payload (ESP)
  - RFC 3947: Negotiation of NAT-Traversal in the IKE
  - RFC 3948: UDP Encapsulation of IPsec ESP Packets
  - RFC 4106: The Use of Galois/Counter Mode (GCM) in IPsec Encapsulating Security Payload (ESP)
  - RFC 4301: Security Architecture for the Internet Protocol
  - RFC 4302: IP Authentication Header
  - RFC 4303: IP Encapsulating Security Payload
  - RFC 4304: Extended Sequence Number (ESN) Addendum to IPsec Domain of Interpretation (DOI) for Internet Security Association and Key Management Protocol (ISAKMP)
  - RFC 4307: Cryptographic Algorithms for Use in the Internet Key Exchange Version 2 ([IKEv2](https://ja.wikipedia.org/wiki/IKEv2 "wikilink"))
  - RFC 4308: Cryptographic Suites for IPsec
  - RFC 4309: Using Advanced Encryption Standard (AES) CCM Mode with IPsec Encapsulating Security Payload (ESP)
  - RFC 4543: The Use of Galois Message Authentication Code (GMAC) in IPsec ESP and AH
  - RFC 4555: IKEv2 Mobility and Multihoming Protocol (MOBIKE)
  - RFC 4806: Online Certificate Status Protocol (OCSP) Extensions to IKEv2
  - RFC 4868: Using HMAC-SHA-256, HMAC-SHA-384, and HMAC-SHA-512 with IPsec
  - RFC 4945: The Internet IP Security PKI Profile of IKEv1/ISAKMP, IKEv2, and PKIX
  - RFC 5282: Using Authenticated Encryption Algorithms with the Encrypted Payload of the Internet Key Exchange version 2 (IKEv2) Protocol
  - RFC 5386: Better-Than-Nothing Security: An Unauthenticated Mode of IPsec
  - RFC 5529: Modes of Operation for Camellia for Use with IPsec
  - RFC 5685: Redirect Mechanism for the Internet Key Exchange Protocol Version 2 (IKEv2)
  - RFC 5723: Internet Key Exchange Protocol Version 2 (IKEv2) Session Resumption
  - RFC 5857: IKEv2 Extensions to Support Robust Header Compression over IPsec
  - RFC 5858: IPsec Extensions to Support Robust Header Compression over IPsec
  - RFC 7296: Internet Key Exchange Protocol Version 2 (IKEv2)
  - RFC 7321: Cryptographic Algorithm Implementation Requirements and Usage Guidance for Encapsulating Security Payload (ESP) and Authentication Header (AH)
  - RFC 7383: Internet Key Exchange Protocol Version 2 (IKEv2) Message Fragmentation
  - RFC 7427: Signature Authentication in the Internet Key Exchange Version 2 (IKEv2)
  - RFC 7634: ChaCha20, Poly1305, and Their Use in the Internet Key Exchange Protocol (IKE) and IPsec

### 実験的（Experimental）

  - RFC 4478: Repeated Authentication in Internet Key Exchange (IKEv2) Protocol

### 情報（Informational）

  - RFC 2367: PF_KEY Interface
  - RFC 2412: The OAKLEY Key Determination Protocol
  - RFC 3706: A Traffic-Based Method of Detecting Dead Internet Key Exchange (IKE) Peers
  - RFC 3715: IPsec-Network Address Translation (NAT) Compatibility Requirements
  - RFC 4621: Design of the IKEv2 Mobility and Multihoming (MOBIKE) Protocol
  - RFC 4809: Requirements for an IPsec Certificate Management Profile
  - RFC 5387: Problem and Applicability Statement for Better-Than-Nothing Security (BTNS)
  - RFC 5856: Integration of Robust Header Compression over IPsec Security Associations
  - RFC 5930: Using Advanced Encryption Standard Counter Mode (AES-CTR) with the Internet Key Exchange version 02 (IKEv2) Protocol
  - RFC 6027: IPsec Cluster Problem Statement
  - RFC 6071: IPsec and IKE Document Roadmap
  - RFC 6467: Secure Password Framework for Internet Key Exchange Version 2 (IKEv2)

### Best Current Practice RFCs

  - RFC 5406: Guidelines for Specifying the Use of IPsec Version 2

### 廃止（Obsolete）/歴史的（Historic）

  - RFC 1825: Security Architecture for the Internet Protocol (obsoleted by RFC 2401)
  - RFC 1826: IP Authentication Header (obsoleted by RFC 2402)
  - RFC 1827: IP Encapsulating Security Payload (ESP) (obsoleted by RFC 2406)
  - RFC 1828: IP Authentication using Keyed MD5 (historic)
  - RFC 2401: Security Architecture for the Internet Protocol (IPsec overview) (obsoleted by RFC 4301)
  - RFC 2406: IP Encapsulating Security Payload (ESP) (obsoleted by RFC 4303 and RFC 4305)
  - RFC 2407: The Internet IP Security Domain of Interpretation for ISAKMP (obsoleted by RFC 4306)
  - RFC 2409: The Internet Key Exchange (obsoleted by RFC 4306)
  - RFC 4305: Cryptographic Algorithm Implementation Requirements for Encapsulating Security Payload (ESP) and Authentication Header (AH) (obsoleted by RFC 4835)
  - RFC 4306: Internet Key Exchange (IKEv2) Protocol (obsoleted by RFC 5996)
  - RFC 4718: IKEv2 Clarifications and Implementation Guidelines (obsoleted by RFC 7296)
  - RFC 4835: Cryptographic Algorithm Implementation Requirements for Encapsulating Security Payload (ESP) and Authentication Header (AH) (obsoleted by RFC 7321)
  - RFC 5996: Internet Key Exchange Protocol Version 2 (IKEv2) (obsoleted by RFC 7296)
  - RFC 6379: Suite B Cryptographic Suites for IPsec
  - RFC 6380: Suite B Profile for Internet Protocol Security (IPsec)

## 関連項目

  - [Virtual Private Network](../Page/Virtual_Private_Network.md "wikilink")
  - [情報セキュリティ](https://ja.wikipedia.org/wiki/情報セキュリティ "wikilink")
  - [NAT traversal](../Page/NAT_traversal.md "wikilink")
  - [日和見暗号化](https://ja.wikipedia.org/wiki/日和見暗号化 "wikilink")

## 外部リンク

  - [IETF ipsec WG](https://datatracker.ietf.org/wg/ipsec/about/) ("IP Security Protocol" Working Group)

  -
  - [IETFの全てのアクティブなセキュリティWG](http://www.ietf.org/html.charters/wg-dir.html#Security%20Area)

      - [IETF ipsecme WG](http://datatracker.ietf.org/wg/ipsecme/) ("IP Security Maintenance and Extensions" Working Group)
      - [IETF btns WG](http://www.ietf.org/html.charters/btns-charter.html) ("Better-Than-Nothing Security" Working Group)\]

## 脚注

[Category:IPsec](https://ja.wikipedia.org/wiki/Category:IPsec "wikilink") [Category:トンネリング](https://ja.wikipedia.org/wiki/Category:トンネリング "wikilink") [Category:暗号化プロトコル](https://ja.wikipedia.org/wiki/Category:暗号化プロトコル "wikilink") [Category:インターネット層プロトコル](https://ja.wikipedia.org/wiki/Category:インターネット層プロトコル "wikilink") [Category:ネットワーク層プロトコル](https://ja.wikipedia.org/wiki/Category:ネットワーク層プロトコル "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:セキュア通信](https://ja.wikipedia.org/wiki/Category:セキュア通信 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:VPN](https://ja.wikipedia.org/wiki/Category:VPN "wikilink")

1.  『RFC6434』「Previously, IPv6 mandated implementation of IPsec and recommended the key management approach of IKE. This document updates that recommendation by making support of the IPsec Architecture \[RFC4301\] a SHOULD for all IPv6 nodes.」
2.  RFC6071等の記述に使用されている。
3.
4.
5.
6.
7.
8.
9.  <http://www.toad.com/gnu/netcrypt.html>
10.