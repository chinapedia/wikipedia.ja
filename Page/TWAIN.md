> この記事は[TWAIN](https://ja.wikipedia.org/wiki/TWAIN)から翻訳されています。


**TWAIN**（トウェイン）は[イメージスキャナ](../Page/イメージスキャナ.md "wikilink")や[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")などから[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")に[画像](../Page/画像.md "wikilink")を入力するための技術標準の一つである。

[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") や [Macintosh](../Page/Macintosh.md "wikilink") など、パーソナルコンピュータの代表的プラットフォームにおいて、画像を取り込む [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") を定めている。

## 概要

TWAIN は主に、[画像処理ソフトウェア](https://ja.wikipedia.org/wiki/画像処理ソフトウェア "wikilink")（[グラフィックソフトウェア](../Page/グラフィックソフトウェア.md "wikilink")）と、スキャナやデジタルカメラとの間の[インタフェース](https://ja.wikipedia.org/wiki/インタフェース "wikilink")として使われている。

TWAIN 標準仕様の初版は[1992年](../Page/1992年.md "wikilink")に発行された。 [2005年](../Page/2005年.md "wikilink")[11月28日](../Page/11月28日.md "wikilink")にバージョン 2.0 が承認され、TWAIN ワーキンググループによって管理されている。

## 欠点

TWAIN の欠点として、**[ユーザーインターフェイス](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")が機器の[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")と一体不可分**になっていることが挙げられる。 [アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")が機器の TWAIN ドライバを読み込むとき、機器メーカー製の [GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink") がどうしても付きまとう。このような形態のために、透過的なネットワークアクセスが困難になっている。（ネットワーク接続のオフィス用[複合機](https://ja.wikipedia.org/wiki/複合機 "wikilink")から画像を取り込む場合、複合機内に共有ドライブを設定するか、特定のクライアントやデータサーバの共有ドライブに[JPEG](../Page/JPEG.md "wikilink")や[PDF](https://ja.wikipedia.org/wiki/PDF "wikilink")などの画像ファイルとして書き込みを行った後でクライアントのアプリケーションから読ませる形を取らざるを得ない）

ただし、そのようなドライバは TWAIN 完全準拠とはいえないため、正確に言えばこれは TWAIN 仕様のせいではなく、ドライバの問題である。

TWAIN制御を行う場合は、TWAINドライバ([DLL](https://ja.wikipedia.org/wiki/DLL "wikilink"))の先頭にある関数を[エントリポイント](https://ja.wikipedia.org/wiki/エントリポイント "wikilink")として使用する。関数名に依存すべきではない。 前述の関数に対し、3つの引数を渡して制御を行うため、各制御命令をトリプレットを発行すると言う。 小数値の取り扱いには注意が必要である。TWAIN内部では小数は[構造体](../Page/構造体.md "wikilink")として扱うため、一般的な言語では変換が必要になる。

## 手順

通常、スキャナや複合機などのデバイスドライバをインストールする際にTWAINドライバもインストールされる。アプリケーション側からは、インストール済みのTWAINデータソース（スキャナ）を選択すると、各機器ごとのGUIが呼び出されるため、各種の設定や操作を行い、本スキャンを指示するとアプリケーションへ画像データが渡される。

## 名前の由来

TWAIN という名前は、公式には略語ではないにもかかわらず、"**T**echnology（Toolkit）**W**ithout **A**n（Any）**I**nteresting（Important）**N**ame"の略語として広く知られている。

TWAIN という語は、[キップリングの詩](../Page/ラドヤード・キップリング.md "wikilink") "The Ballad of East and West" （東と西の歌）に由来する英語の成句 "...and never the **twain** shall meet..." （この**両者**は決して出会うことはない）から取られ、当時のスキャナとパーソナルコンピュータを接続する困難さを暗示した。 ワーキンググループ黎明期の活動の中で "Technology Without An Interesting Name" というフレーズが生まれたが、これは TWAIN に略される元の名前として採用されるには至らなかった\[1\]。

## 関連項目

  - [Image and Scanner Interface Specification](https://ja.wikipedia.org/wiki/Image_and_Scanner_Interface_Specification "wikilink")

  - [WIA](https://ja.wikipedia.org/wiki/Windows_Image_Acquisition "wikilink")（Windows Image Acquisition）[英語版記事](https://ja.wikipedia.org/wiki/:en:Windows_Image_Acquisition "wikilink")

  -
  - [ICCプロファイル](https://ja.wikipedia.org/wiki/ICCプロファイル "wikilink")

## 脚注

<references/>

## 外部リンク

  - [TWAIN Working Group](http://www.twain.org/)

[Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink") [Category:入力機器](https://ja.wikipedia.org/wiki/Category:入力機器 "wikilink") [Category:パソコンの周辺機器](https://ja.wikipedia.org/wiki/Category:パソコンの周辺機器 "wikilink") [Category:画像処理](https://ja.wikipedia.org/wiki/Category:画像処理 "wikilink")

1.  [What is TWAIN an acronym for?](http://twain.org/faq.htm#What%20is%20TWAIN%20an%20acronym%20for)