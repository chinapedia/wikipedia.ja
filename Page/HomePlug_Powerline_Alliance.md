> この記事は[HomePlug Powerline Alliance](https://ja.wikipedia.org/wiki/HomePlug_Powerline_Alliance)から翻訳されています。


**HomePlug Powerline Alliance** (**HomePlug**) は[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")における[電力線搬送通信](../Page/電力線搬送通信.md "wikilink")の[業界団体](../Page/業界団体.md "wikilink")である。約50の企業が参加し、電力線搬送通信の仕様を定義している。HomePlug 1.0とHomePlug AVという2種類の仕様があり、家庭内での電力線で各種機器を接続するのに使われる。HomePlug準拠の製品をさらに[イーサネット](../Page/イーサネット.md "wikilink")、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[IEEE 802.11などで](../Page/IEEE_802.11.md "wikilink")[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")と接続する。HomePlug準拠製品同士は単に壁のコンセントに接続するだけで相互に接続される。HomePlugの発生する高周波が各種機器に悪影響を及ぼす可能性があるため、HomePlug製品は延長コードなどを使わずに直接壁のコンセントに接続するのが望ましい。

## 概要

信号がユーザーの自宅やオフィスの外まで若干漏れる可能性があるため、他のネットワーク規格と同様、HomePlugには暗号化パスワードを設定する機能がある。他のネットワーク機器と同様、HomePlug機器の多くは *[Secure by default](https://ja.wikipedia.org/wiki/Secure_by_default "wikilink")*（デフォルト設定でセキュリティが確保されている）である。HomePlug規格では全ての機器にデフォルトの外部パスワードが設定される（同じものでもよい）。ユーザーはこのパスワードを変更する必要がある。

HomePlugネットワークでの[パスワード](../Page/パスワード.md "wikilink")設定処理を単純化するため、各機器には組み込みのマスターパスワードがあり、製造時に無作為に選択されて機器内に書き込まれ、暗号化パスワードの設定時にのみ使用される。マスターパスワードは機器上のラベルに印刷されている。

HomePlugでの暗号化はHomePlug機器間でのみ行われ、HomePlug機器に別の機器を接続する部分では暗号化されない（もちろん、[TLSや](../Page/Transport_Layer_Security.md "wikilink")[IPsec](../Page/IPsec.md "wikilink")のような上位プロトコルでの暗号化が使われている場合は別である）。

透過な[ブリッジとして働くため](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")、HomePlug機器に接続したコンピュータは特別な[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")などを必要としない。ただし、一部のベンダーは[Windows向けにパスワード設定ユーティリティを提供している](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。逆に言えばこの場合、暗号化を開始するにはWindowsの動作するコンピュータを必要とする[1](http://www.netgear.com/products/details/XE102.php)。一旦暗号化パスワードが設定されれば、Windowsは不要になるので、必要ならノート型パソコンを借りてきて設定することもできる。

北米での家庭やオフィスに供給される電力線では、コンセントの約半分が位相の問題で相互に通信できない。このため、部屋によってはHomePlugを使えない場合がある。

HomePlugはイーサネットをバス型トポロジーに戻すものと言え、[CSMA/CD](https://ja.wikipedia.org/wiki/CSMA/CD "wikilink")の本来の姿であり、場合によっては非常に好ましい。これは同じ線対に複数のデータ搬送波を共存させる[OFDM](https://ja.wikipedia.org/wiki/OFDM "wikilink")によって実現されている。

## 現存の規格と予定されている規格

HomePlug Powerline Allianceは以下の規格を定義してきた。

  - **HomePlug 1.0** — 2001年6月リリース — 家庭内の電力線を通して機器を接続する仕様。理論上の速度は14Mbps。
  - **HomePlug 1.0 Turbo** — 高速だが非公式の仕様。理論上の速度は85Mbps。
  - **HomePlug AV** — 2005年12月リリース — [HDTVや](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")[VoIP](../Page/VoIP.md "wikilink")を転送する仕様。理論上の速度は200Mbps。
  - **HomePlug Access BPL** (*BPL*) — 開発中 — 外の電力線を通信に使用する仕様。ワーキンググループが検討中。
  - **HomePlug Command & Control** (*HPCC*) — 開発中 — 低速で安価な技術であり、家庭内の照明、空調、その他の各種機器の制御を行うための仕様。

### 1.0

HomePlug 1.0は最高14Mビット/秒の半二重である。

85Mビット/秒 の機器をHomePlug 1.0と間違っているケースが多い。85MbpsのTurboモードには[Intellon](http://www.intellon.com/)の独自の技術が使われている。混同される原因は、IntellonのINT5500チップセットがTurboモードだけでなくHomePlug 1.0とも互換性があり、TurboモードもHomePlug 1.0 Turboと非常によく似た名前で呼ばれているためである。

### AV

HomePlug AVは最高200Mビット/秒の半二重である。HomePlug 1.0の機器とHomePlug AVの機器は何らかの[ブリッジを置かないと相互に通信できないが](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")、同じケーブル上に共存することは可能である。[誤り検出訂正](../Page/誤り検出訂正.md "wikilink")には[ターボ符号](../Page/ターボ符号.md "wikilink")を採用。

### BPL

現在策定中のHomePlug BPLは、いわゆるラストワンマイルを実現する[電力線搬送通信](../Page/電力線搬送通信.md "wikilink")である。

### Command & Control

Command & Controlは、空調や暖房の制御を行うもので低速で安価な点が特徴である。

### 相互運用性

HomePlug Powerline AllianceはHomePlug準拠製品の認証を行っている。認証マークを付与された機器は相互運用可能とされる。[ソニー](../Page/ソニー.md "wikilink")、[三菱電機](../Page/三菱電機.md "wikilink")、[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")が北米で新たに結成した[CEPCAは](https://ja.wikipedia.org/wiki/Consumer_Electronics_Powerline_Communications_Alliance "wikilink")170Mビット/秒の速度を電力線で実現しようとするもので、HomePlugとの相互運用はできない。

HomePlugはライバル団体でもあるHD-PLC Allianceや[UPAと共に](https://ja.wikipedia.org/wiki/Universal_Powerline_Association "wikilink")[IEEE P1901の開発に関与している](https://ja.wikipedia.org/wiki/IEEE_P1901 "wikilink")。これにより、将来的に[電力線搬送通信](../Page/電力線搬送通信.md "wikilink")の規格が統一される可能性も残されている。

## HomePlug機器

日本で入手可能なものを以下に挙げる。

  - [シャープ](../Page/シャープ.md "wikilink") - HN-VA10S、HN-VA40S
  - [ゼクセロン](http://www.zexelon.co.jp/text/product.html#plcadapter) - ZAX-100NS、ZAX-100NW
  - [住友電工](https://ja.wikipedia.org/wiki/住友電工 "wikilink")
  - [ザイセル](../Page/ザイセル.md "wikilink") - PLA-400
  - [ハロッズ](../Page/ハロッズ.md "wikilink") - HP7050/S
  - [NTTネオメイト](../Page/NTTネオメイト.md "wikilink") - SN-200HP

## 関連項目

  - [HomePNA](../Page/HomePNA.md "wikilink")

  -
  - (MoCA)

  - [電力線搬送通信](../Page/電力線搬送通信.md "wikilink")

  - [Power over Ethernet](../Page/Power_over_Ethernet.md "wikilink")

## 外部リンク

  - [HomePlug](http://www.homeplug.org)
      - [Technical whitepapers](http://www.homeplug.org/products/whitepapers/)
  - [IEEE 1901](http://grouper.ieee.org/groups/1901/)
  - [HD-PLC高速電力線通信（HD-PLCアライアンスの公式サイト）](http://www.hd-plc.org/)

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:業界団体](https://ja.wikipedia.org/wiki/Category:業界団体 "wikilink") [Category:スマートグリッド](https://ja.wikipedia.org/wiki/Category:スマートグリッド "wikilink")