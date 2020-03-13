> この記事は[Power over Ethernet](https://ja.wikipedia.org/wiki/Power_over_Ethernet)から翻訳されています。


**Power over Ethernet** (PoE) は、[イーサネット](../Page/イーサネット.md "wikilink")の配線で利用される[カテゴリ5以上の](../Page/カテゴリー5ケーブル.md "wikilink")[UTPケーブル](../Page/ツイストペアケーブル.md "wikilink")（より対線）を通じて[電力](../Page/電力.md "wikilink")を供給する技術。

## 概要

[2003年](../Page/2003年.md "wikilink")[6月](../Page/6月.md "wikilink")に[IEEE 802.3afとして標準化された](https://ja.wikipedia.org/wiki/IEEE_802.3af "wikilink")。主に電力供給の困難な場所に設置された、[Webカメラ](../Page/Webカメラ.md "wikilink")、[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")、[無線LAN](../Page/無線LAN.md "wikilink")[アクセスポイント](../Page/アクセスポイント_\(無線LAN\).md "wikilink")、[IP電話機](https://ja.wikipedia.org/wiki/IP電話機 "wikilink")などで利用される。

給電側機器を「**PSE**」（Power sourcing equipment）、受電側機器を**PD**（Powered device）と呼ぶ。

電力の供給には、[データ](../Page/データ.md "wikilink")線と電力供給線が共用であるため[1000BASE-Tでも使用できる](https://ja.wikipedia.org/wiki/ギガビット・イーサネット "wikilink")「**オルタナティブA**（**TypeA**）」と、UTPケーブル上の[10BASE-T](https://ja.wikipedia.org/wiki/10メガビット・イーサネット "wikilink")/[100BASE-TXでは使われていない](https://ja.wikipedia.org/wiki/100メガビット・イーサネット "wikilink")4本のピンを利用する「**オルタナティブB**（**TypeB**）」の方式がある。TypeAでは1・2・3・6番のピンを、TypeBでは4・5・7・8番のピンを利用する。[IEEE 802.3afではどちらも](https://ja.wikipedia.org/wiki/IEEE_802.3af "wikilink")、給電側機器 (**PSE**、Power sourcing equipment) は最大44–57(一般的には48)[V](../Page/ボルト_\(単位\).md "wikilink")/15.4[Wで供給し](../Page/ワット.md "wikilink")、受電側機器 (**PD**、Powered device) は12.95Wを使えることになっている\[1\]日経エレクトロニクス 2007年10月8日号「25～70Wの大電流対応品が登場」</ref>。給電側機器は製品仕様としてどちらかのタイプを選択する事が出来るが、受電側機器はどちらのタイプからでも受電できる仕様にしなければならない。

基本的にはPoEに対応した機器同士でなければ利用できないが、給電ユニットや受電ユニットといった外部機器を併設する事により、PoE非対応の機器でも電力供給の恩恵を受ける事は可能である。

## 弱点

1\) PoEでは[活線挿抜](https://ja.wikipedia.org/wiki/活線挿抜 "wikilink")をすると接合部に火花（放電）が発生するおそれがあり、機器トラブルや故障について注意が必要である。（そもそも[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")による[イーサネット](../Page/イーサネット.md "wikilink")自体、活線挿抜を積極的には認めていない）

2\) PoEの規格に回路保護が盛り込まれていないのは高速通信と電力送信を両立させるためと推察されるが、パルストランスの中点からPoEの電源回路（PSE/PD共）へ直接接続されることが大きな弱点となる。このためPoE機器を屋外で使用したり、或いはPoE機器に屋外から引き込んだケーブルを接続すると、雷サージなど異常電圧がPoEの電源部を直撃するため、容易に損傷する。

### 内線規程に対するPoEの立場

そもそも日本において電力線（強電流回路）と信号線（弱電流回路）は[内線規程](../Page/内線規程.md "wikilink")により区別されているため、信号線を電力線代わりにするPoEは規程外の使用方法にあたることに注意しなければならない。

なお、海外においては[TN-C接地](https://ja.wikipedia.org/wiki/TN-C接地 "wikilink")や[TN-S接地](https://ja.wikipedia.org/wiki/TN-S接地 "wikilink")が多く用いられているため、PoE機器を始め通信機器がサージで壊れる可能性は低いが、日本では[内線規程](../Page/内線規程.md "wikilink")により[TT接地](https://ja.wikipedia.org/wiki/TT接地 "wikilink")が標準であるため[等電位ボンディング](https://ja.wikipedia.org/wiki/等電位ボンディング "wikilink")が難しく、PoE機器など海外製通信機器が壊れやすい環境であることに留意しなければならない。\[出展のCIAJの記事を参照\]

## 拡張規格

IEEE802.3afを拡張し、2009年9月に標準化されたIEEE 802.3at (PoE Plus) では、1ポートから最大34.20Wを給電し、25.50Wを受電できる。

[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")は、2011年、1ポートから最大60W給電を可能とする、Cisco Universal Power Over Ethernet (UPoE) を発表。

## PoE給電仕様

| | クラス | 受電機器 (PD) の最大電力 | 給電機器 (PSE) の電力 | ケーブル  | 規格                 |
| ----- | --------------- | -------------- | ----- | ------------------ |
| 0     | 13.0 W          | 15.4 W         | Cat5e | IEEE802.3af        |
| 1     | 3.84 W          | 4.0 W          | Cat5e | IEEE802.3af        |
| 2     | 6.49 W          | 7.0 W          | Cat5e | IEEE802.3af        |
| 3     | 12.95 W         | 15.4 W         | Cat5e | IEEE802.3af        |
| 4     | 25.5 W          | 30.0 W         | Cat5e | IEEE802.3at (PoE+) |
| \-    | 51 W            | 60.0 W         | Cat5e | UPoE (シスコ独自)       |

## 出典

  - [CPDV100: Control Poe by Internet, www.reset.cl](http://www.reset.cl/index.php?categoria=Electronica)
  - [POE供电技术：以太网POE供电技术剖析](http://www.poesw.com/poepowersupply/7.html)
  - [CIAJ「雷過電圧に対する通信機器の保護ガイドライン ＣＥＳ－００４０－２」](https://www.ciaj.or.jp/ciaj-wp/wp-content/uploads_sec/2014/06/CES_0040_2.pdf)

## 関連項目

  - [HomePlug Powerline Alliance](../Page/HomePlug_Powerline_Alliance.md "wikilink")

[Category:IEEE_802](https://ja.wikipedia.org/wiki/Category:IEEE_802 "wikilink") [Category:ネットワークハードウェア](https://ja.wikipedia.org/wiki/Category:ネットワークハードウェア "wikilink") [Category:電源回路](https://ja.wikipedia.org/wiki/Category:電源回路 "wikilink") [Category:電力](https://ja.wikipedia.org/wiki/Category:電力 "wikilink")

1.