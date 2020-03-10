> この記事は[Wi-Fi Protected Access](https://ja.wikipedia.org/wiki/Wi-Fi_Protected_Access)から翻訳されています。


**Wi-Fi Protected Access（WPA）**とは、[Wi-Fi Alliance](../Page/Wi-Fi_Alliance.md "wikilink") の監督下で行われている[認証](../Page/認証.md "wikilink")プログラム。Wi-Fi Alliance が策定したセキュリティ[プロトコル](../Page/プロトコル.md "wikilink")にその[ネットワーク機器が準拠していることを示すものである](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")。また、そのセキュリティプロトコルそのものも指す。これまでに**WPA**、**WPA2**、**WPA3**の3つのプログラム及びプロトコルが策定された。

## 概要

WPAプロトコルは、それ以前の [Wired Equivalent Privacy](../Page/Wired_Equivalent_Privacy.md "wikilink") (WEP) に対して脆弱性を指摘されたため、その対策として策定された。[IEEE 802.11i](https://ja.wikipedia.org/wiki/IEEE_802.11 "wikilink") の主要部分を実装したプロトコルであり、802.11i が完成するまでの間、WEP の代替として一時的に使うために策定された。WPA対応以前の無線LANカードでも（[ファームウェア](../Page/ファームウェア.md "wikilink")の更新で）機能するよう設計されているが、第一世代の[アクセスポイントでは必ずしも機能しない](../Page/アクセスポイント_\(無線LAN\).md "wikilink")。

WPA2 認証マークは、その機器が拡張プロトコル規格に完全準拠していることを示す。この拡張プロトコルは古い無線LANカードでは機能しない\[1\]。

基本的に、WPA は [Wi-Fi Alliance](../Page/Wi-Fi_Alliance.md "wikilink") による認証プログラムである。Wi-Fi Alliance は、[Wi-Fi](../Page/Wi-Fi.md "wikilink") の[商標](../Page/商標.md "wikilink")の権利者であり、機器にその商標を付けることを認証している[業界団体](https://ja.wikipedia.org/wiki/業界団体 "wikilink")である。

### 歴史

## バージョン

### WPA

WPA 認証マークは、無線ネットワークのセキュリティ強化のために策定したセキュリティプロトコルへの準拠を示す。このプロトコルには Enterprise と Personal の2種類がある。Enterprise は、各ユーザに別々のキーを配布する [IEEE 802.1X](https://ja.wikipedia.org/wiki/IEEE_802.1X "wikilink") 認証サーバを使う方式である。Personal WPA はスケーラビリティのない「 (PSK)」モードを使い、アクセス可能なコンピュータには全て同じパスフレーズを与える。PSKモードでは、セキュリティはパスフレーズの秘密性と強度に依存する。このプロトコルの設計は、IEEE 802.11i 規格のドラフト3版に基づいている。

Wi-Fi Alliance は、この標準に基づいたセキュアな無線ネットワーク製品を普及させるべく、IEEE 802.11i の策定が完了する前にこのプロトコルを策定した。その時点で既に Wi-Fi Alliance は IEEE 802.11i 規格の最終ドラフト版に基づいた WPA2 仕様を考慮していた。従って、フレームフィールド上のタグ（Information Elements、IE とも呼ぶ）が 802.11i と違っているのは意図的であって、プロトコルの2種類のバージョンが実装されたときの混乱を避けるために変更した。

データは[RC4](https://ja.wikipedia.org/wiki/RC4 "wikilink")[ストリーム暗号](https://ja.wikipedia.org/wiki/ストリーム暗号 "wikilink")で暗号化され、鍵は128ビット、[初期化ベクトル](https://ja.wikipedia.org/wiki/初期化ベクトル "wikilink") (IV) は48ビットである。[WEP](../Page/Wired_Equivalent_Privacy.md "wikilink") からの主要な改善点は [Temporal Key Integrity Protocol](https://ja.wikipedia.org/wiki/Temporal_Key_Integrity_Protocol "wikilink") (TKIP) である。これはシステム運用中に動的に鍵を変更するプロトコルである。それに大きな初期化ベクトルを組合せることで、WEP での[関連鍵攻撃](https://ja.wikipedia.org/wiki/関連鍵攻撃 "wikilink")に対する脆弱性への対策とした。

認証と暗号化に加えて、このプロトコルではペイロード完全性を大幅に強化している。WEP で使われていた本質的にセキュアでない[巡回冗長検査](../Page/巡回冗長検査.md "wikilink") (CRC) は、WEP の鍵を知らなくともペイロードを書き換えて、CRC を更新することが可能であった。WPA ではよりセキュアな[メッセージ認証符号](https://ja.wikipedia.org/wiki/メッセージ認証符号 "wikilink")（通常 MAC と略記されるが、ここでは MIC = Message Integrity Code とする）を使い、"Michael" というアルゴリズムを使っている。MIC にはフレームカウンタが含まれ、[反射攻撃](https://ja.wikipedia.org/wiki/反射攻撃 "wikilink")を防ぐことができる。

鍵とIVのサイズを大きくすることで、関連鍵で送るパケット数を減らし、セキュアなメッセージ認証システムを加え、無線LANへの侵入は従来より遥かに困難になった。Michael アルゴリズムは、古い無線LANカードでも機能するものとしては Wi-Fi Alliance の設計者らが到達した最も強度の高いアルゴリズムである。Michael も完全ではないため、TKIP は Michael のチェックに合格しないフレームが2個見つかると、ネットワークを1分間閉鎖する。そして、新たな世代の鍵を要求し、再認証によってネットワークを再開する。

### WPA2

Wi-Fi Alliance の WPA2 プログラムで認証される拡張プロトコルは、802.11i の必須部分を実装したものである。特に新たに[AES](../Page/Advanced_Encryption_Standard.md "wikilink")（[共通鍵暗号](../Page/共通鍵暗号.md "wikilink")方式）ベースのアルゴリズム [CCMP](https://ja.wikipedia.org/wiki/Counter_mode_with_Cipher-block_chaining_Message_authentication_code_Protocol "wikilink") を導入している。[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[3月13日](../Page/3月13日.md "wikilink")から、WPA2 認証を受けないと "Wi-Fi CERTIFIED" を名乗れなくなった。

### WPA3

2018年6月25日発表\[2\]。2018年後半より対応機器がリリースされる予定\[3\]。

WPA2のセキュリティ拡張として提供される。WPA2に対して、下記の新機能が追加されるとアナウンスされた。

  - Simultaneous Authentication of Equals 総当たり攻撃からの保護\[4\]

  - 設定のないデバイスに対するセキュリティ機能

  - Opportunistic Wireless Encryption 子機 - 親機間で個別にデータを暗号化

  - に準拠した192ビット暗号化を採用

  - Wi-Fi Easy Connect

WPA3はWPA3-Personal、WPA3-Enterpriseに分けられる。

WPA3-Personal ではWPA-Personal、WPA2-Personalで使用していたPSKに代わり、ユーザの入力したパスワードをSAE (Simultaneous Authentication of Equals)で処理したPMKを利用する。

PMK算出後は、従来のWPA/WPA2と同様に4-way handshakeによる鍵交換が実施される。

## セキュリティ

[TKIPもしくは](https://ja.wikipedia.org/wiki/Temporal_Key_Integrity_Protocol "wikilink")[CCMPによる暗号化が提供されている](https://ja.wikipedia.org/wiki/Counter_mode_with_Cipher-block_chaining_Message_authentication_code_Protocol "wikilink")。

### WPAパーソナルモード

モード（PSK、またはパーソナルモード）は、個人宅や小規模の会社向けに設計されたもので、[IEEE 802.1X](https://ja.wikipedia.org/wiki/IEEE_802.1X "wikilink") 認証サーバを必要としない。

各ユーザーはネットワークにアクセスする際に[パスフレーズ](https://ja.wikipedia.org/wiki/パスフレーズ "wikilink")を入力しなければならない。パスフレーズは8文字から63文字の[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")の印字可能文字か、64桁の[16進数](../Page/十六進法.md "wikilink")（256ビット）である。ASCII文字を選択した場合、[ハッシュ関数](../Page/ハッシュ関数.md "wikilink")で最大約420.5ビットの情報（63文字×6.6ビット/文字）を256ビットに縮小する（[SSIDも使う](../Page/サービスセット識別子.md "wikilink")）。パスフレーズは何度もユーザーに入力させることを避けるために、ユーザーのコンピュータに記憶させておくことが多い。パスフレーズはアクセスポイントにも記憶させておく必要がある。

セキュリティ強化のためには[鍵導出関数](https://ja.wikipedia.org/wiki/鍵導出関数 "wikilink")を使うべきだが、ユーザーが一般に利用する弱いパスフレーズは、[パスワードクラック](https://ja.wikipedia.org/wiki/パスワードクラック "wikilink")に対して脆弱である。[総当り攻撃](https://ja.wikipedia.org/wiki/総当り攻撃 "wikilink")への対策としては、13文字のランダムなパスフレーズ（文字種は95文字）で十分と言われている\[5\]。Church of WiFi は上位1,000位までのSSID\[6\]について[レインボーテーブル](../Page/レインボーテーブル.md "wikilink")を計算した\[7\]。侵入を確実に防ぐには、ネットワークのSSIDは上位1,000位のSSIDと同じにしないよう設定すべきである。

半導体製造業者によっては、無線LAN機器をネットワークに追加する際にソフトウェアまたはハードウェアによる独自のインタフェースを使って、自動的にパスフレーズを生成して配布する方式を採用し、ユーザーが弱いパスフレーズを選択するのを防いでいる。これには例えば、ボタンを押下する方式（[ブロードコム](https://ja.wikipedia.org/wiki/ブロードコム "wikilink")のSecureEasySetup\[8\]、[AirStation](https://ja.wikipedia.org/wiki/AirStation "wikilink")の[AOSS](https://ja.wikipedia.org/wiki/AirStation_One-Touch_Secure_System "wikilink")、[Aterm](https://ja.wikipedia.org/wiki/Aterm "wikilink")の[らくらく無線スタート](https://ja.wikipedia.org/wiki/らくらく無線スタート "wikilink")）やソフトウェア経由で短い語句を入力する方式（[AtherosのJumpStart](https://ja.wikipedia.org/wiki/アセロス・コミュニケーションズ "wikilink")\[9\]や[ザイセル](https://ja.wikipedia.org/wiki/ザイセル "wikilink")のOTIST）がある。Wi-Fi Alliance はこれらの方式についても標準化を行い、[Wi-Fi Protected Setupというプログラムで認証をおこなっている](https://ja.wikipedia.org/wiki/Wi-Fi_Protected_Setup "wikilink")。

### WPAエンタープライズモード

ユーザ認証に従来のIEEE802.1Xを利用。[RADIUS](../Page/RADIUS.md "wikilink")サーバが必要になる。

## WPA Enterprise と WPA2 Enterprise における EAP 拡張

Wi-Fi Alliance は、WPA Enterprise および WPA2 Enterprise の認証プログラムに追加の EAP ([Extensible Authentication Protocol](https://ja.wikipedia.org/wiki/Extensible_Authentication_Protocol "wikilink")) を含めることを発表した。これにより、WPA Enterprise 認証を受けた機器が相互運用可能であることを保証できる。それ以前は EAP-TLS ([Transport Layer Security](../Page/Transport_Layer_Security.md "wikilink")) のみを認証していた。

認証されている EAP は以下の通り。

  - [EAP-TLS](https://ja.wikipedia.org/wiki/Extensible_Authentication_Protocol "wikilink") （従来から）

  - [EAP-TTLS](https://ja.wikipedia.org/wiki/Extensible_Authentication_Protocol "wikilink")/MSCHAPv2

  - v0/EAP-MSCHAPv2

  - PEAPv1/EAP-GTC

  - [EAP-SIM](https://ja.wikipedia.org/wiki/Extensible_Authentication_Protocol "wikilink")

他のEAP方式を使う機器もある。この認証は主要なEAP方式の相互運用を保証しようとする試みである。

## ハードウェアサポート

"Wi-Fi CERTIFIED" 付きの機器では、上述のセキュリティプロトコルをサポートしているものがほとんどである\[10\]。

WPAプログラムが策定される以前の機器でも WPA が使えるよう考慮されている\[11\]。その場合、[ファームウェア](../Page/ファームウェア.md "wikilink")の更新が必要である。全ての古い機器でファームウェアが更新可能というわけではない。

## 脆弱性

WPAに採用されている[TKIPには脆弱性があることが知られており](https://ja.wikipedia.org/wiki/Temporal_Key_Integrity_Protocol "wikilink")（同項目参照）、[AESをベースとするより強力な](../Page/Advanced_Encryption_Standard.md "wikilink")[CCMPを使用する](https://ja.wikipedia.org/wiki/Counter_mode_with_Cipher-block_chaining_Message_authentication_code_Protocol "wikilink")**WPA2**か、またはWPAにおいてTKIPの代わりにCCMPを使用することが推奨される\[12\]\[13\]\[14\]。

しかしながら2017年10月16日、セキュリティ面でより強力とされたWPA2についても脆弱性（[KRACK](https://ja.wikipedia.org/wiki/KRACK "wikilink")）の発表を予告する情報が記載され\[15\]、現状この規格が無線環境で広く用いられているだけに、研究者やITコンサルタント等をはじめ、多くの利用者に波紋を広げていた。

WPA3においても、2019年4月15日に脆弱性が公開されたが\[16\]、ソフトウェア(ファームウェア)アップデートで対処可能である。

## 脚注

### 注釈

### 出典

## 外部リンク

  - [Wi-Fi Alliance's WPA page](http://www.wi-fi.org/knowledge_center/wpa/)
  - [Wi-Fi Alliance's Interoperability Certificate page](http://certifications.wi-fi.org/wbcs_certified_products.php)
  - [Weakness in Passphrase Choice in WPA Interface](http://wifinetnews.com/archives/002452.html), by Robert Moskowitz. Retrieved March 2, 2004.
  - [IEEE Std. 802.11i-2004](http://standards.ieee.org/getieee802/download/802.11i-2004.pdf)

[Category:Wi-Fi](https://ja.wikipedia.org/wiki/Category:Wi-Fi "wikilink") [Category:暗号化プロトコル](https://ja.wikipedia.org/wiki/Category:暗号化プロトコル "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:コンピュータセキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータセキュリティ "wikilink") [Category:モバイルネットワーク](https://ja.wikipedia.org/wiki/Category:モバイルネットワーク "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink")

1.
2.   Wi-Fi Alliance|accessdate=2018-06-28|website=www.wi-fi.org|language=en}}
3.
4.   カミアプ|accessdate=2018-06-28|website=www.appps.jp|language=ja-JP}}
5.  [Weakness in Passphrase Choice in WPA Interface](http://wifinetnews.com/archives/002452.html) by Robert Moskowitz. Retrieved March 2, 2004.
6.  [SSID Stats](http://www.wigle.net/gps/gps/Stat) WiGLE.net
7.  [Church of Wifi WPA-PSK Rainbow Tables](http://www.renderlab.net/projects/WPA-tables/)
8.  [Broadcom Corporation - SecureEasySetup Software](http://www.broadcom.com/products/secureeasysetup.php)
9.  [JumpStart Whitepaper](http://www.atheros.com/pt/whitepapers/atheros_JumpStart_for_wireless_whitepaper.pdf)
10.
11.
12. <http://slashdot.jp/security/article.pl?sid=09/08/07/0028228>
13. <http://gigazine.net/index.php?/news/comments/20081107_wpa_tkip/>
14. <http://trendy.nikkeibp.co.jp/article/qa/yougo/20041116/110091/>
15. <http://www.blackhat.com/eu-17/briefings/schedule/#key-reinstallation-attacks-breaking-the-wpa2-protocol-8861>
16.