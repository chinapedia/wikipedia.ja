> この記事は[Sun SPOT](https://ja.wikipedia.org/wiki/Sun_SPOT)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Sun_Spot.jpg "wikilink") Sun SPOT () は、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が開発した[IEEE 802.15.4に準拠した](https://ja.wikipedia.org/wiki/:en:IEEE_802.15.4 "wikilink")[無線センサーネットワーク](https://ja.wikipedia.org/wiki/無線センサーネットワーク "wikilink")デバイスである。

他の無線センサーデバイスと異なり、Sun SPOTは組み込み向けの[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")[Squawk上で動作している](https://ja.wikipedia.org/wiki/Squawk_virtual_machine "wikilink")。

## ハードウェア

このデバイスは手のひらにちょうどフィットする大きさをしている。

Sun SPOT はプロセッサボードとオプションのセンサーボードから構成されている。

### プロセッサボード

  - 180MHz 32ビット [ARM](../Page/ARMアーキテクチャ.md "wikilink")920T コア
  - 512KB RAM/4MB [フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")
  - 2.4GHz IEEE 802.15.4無線（アンテナ付）
  - [USBインタフェース](../Page/ユニバーサル・シリアル・バス.md "wikilink")（ミニUSB B 端子）

### センサーボード

  - 2G/6G 3軸[加速度センサー](https://ja.wikipedia.org/wiki/加速度センサー "wikilink")
  - 温度センサー
  - 照度センサー
  - フルカラーLED x 8
  - タクトスイッチ x 2
  - アナログ入力ピン x 6
  - 汎用IOピン x 6
  - 高出力ピン x 4

### 電源

  - 3.7V 750mAh [リチウムイオンバッテリ](../Page/リチウムイオン二次電池.md "wikilink")
  - 30 μA スリープモード
  - ソフトウェアによるバッテリ管理

## ネットワーク

Sun SPOTはIEEE 802.15.4に準拠したネットワーク機能を有している。

## ソフトウェア

Sun SPOT は J2ME の Squawk virtual machine を搭載し、OSなしにプロセッサで直接実行する。Squawk VM と Sun SPOT のソースコードはどちらもオープンソースになっている [1](http://spots.dev.java.net)。

## 開発キット

[NetBeans](../Page/NetBeans.md "wikilink") のような標準的な Java IDE を使用してアプリケーションを作成する。Solarium(以前はSPOTWorldという名称だった) というアプリケーションを通してデバイスの管理や開発を行う。新品デフォルトでは[センサネットワーク](https://ja.wikipedia.org/wiki/センサネットワーク "wikilink")機能は無く、関連プログラムを書込みする必要がある。2008年4月時点では説明書は英文のみ。

## 入手

最初の制限付の Sun SPOT 開発キットは数ヶ月遅れて[2007年](../Page/2007年.md "wikilink")4月2日にリリースされた。この入門キットは、2つの Sun SPOT デモセンサーボードと、1つの Sun SPOT ベースステーション、とソフトウェア開発キット (そしてUSBケーブル) が含まれていた。このソフトウェアは[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、[Mac OS X v10.4](../Page/Mac_OS_X_v10.4.md "wikilink")、そして多くの [Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")で動作する。プロジェクト、ハードウェア、OS、Java仮想マシン、ドライバ、アプリケーションはオープンソースとして入手できる\[1\]\[2\]。

## 出典・脚注

## 関連項目

  - [センサネットワーク](https://ja.wikipedia.org/wiki/センサネットワーク "wikilink")
  - [モバイルアドホックネットワーク](https://ja.wikipedia.org/wiki/モバイルアドホックネットワーク "wikilink")
  - [メッシュネットワーク](https://ja.wikipedia.org/wiki/メッシュネットワーク "wikilink")

## 外部リンク

  - [Sun SPOT 製品情報](http://jp.sun.com/products/software/sunspot/) （日本語）
  - [Official website](http://www.sunspotworld.com/)（英語）
  - [Open Source](http://spots.dev.java.net/)（英語）
  - [Flocking blimps powered by "B" SPOTs](http://www.alavs.com/)（英語）
  - [Rob Tow's Sun SPOT page](http://tauzero.com/Rob_Tow/Sun-SPOTS-Sensor-Networks.html)（英語）
  - [David G. Simmons' Sun SPOT blog](http://blogs.sun.com/davidgs/)（英語）
  - [Sun SPOTs In Action at jazoon 2007](http://parleys.com/display/PARLEYS/Sun+SPOTs+In+Action?showComments=true)（英語）
  - [eBones: information to create add-on boards for the eSPOT](http://spots-ebones.dev.java.net/)（英語）
  - [IEEE 802.15.4](https://ja.wikipedia.org/wiki/:en:IEEE_802.15.4 "wikilink")（英語）

[Category:モバイルネットワーク](https://ja.wikipedia.org/wiki/Category:モバイルネットワーク "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink")

1.  [SPOTs project](http://spots.dev.java.net/)
2.  <http://jp.sun.com/products/software/sunspot/>