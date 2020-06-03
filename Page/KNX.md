> この記事は[KNX](https://ja.wikipedia.org/wiki/KNX)から翻訳されています。


[KNX_logo.svg](https://ja.wikipedia.org/wiki/File:KNX_logo.svg "fig:KNX_logo.svg") **KNX** とは、[インテリジェントビル](../Page/インテリジェントビル.md "wikilink")のための[OSIベースの](../Page/OSI参照モデル.md "wikilink")[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")であり、**EN 50090** および **ISO/IEC 14543** として標準化されている。既存の3つの標準、European Home Systems Protocol（**EHS**）、**BatiBUS**、European Installation Bus（**EIB**）の後継として策定された。

KNX は KNX Association が管理している。

## 概要

EIB の[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")を基本として、物理層、構成モード、アプリケーション層などを BatiBUS や EHS から取り入れて拡張している。

物理通信媒体としては、次のようなものが定義されている。

  - [ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")（BatiBUS と EIB Instabus を継承）
  - 電力線ネットワーク（EIB と EHS を継承。[X10と類似](../Page/X10_\(工業規格\).md "wikilink")）
  - 無線
  - 赤外線
  - [イーサネット](../Page/イーサネット.md "wikilink")（EIBnet/IP または KNXnet/IP とも呼ぶ）

KNX は特定のハードウェアプラットフォームとは独立したものとして設計されている。KNX ネットワークは8ビットの[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")や[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")で、適当な実装をすることで制御できる。

KNX の一部は、[C-Bus](https://ja.wikipedia.org/wiki/C-Bus "wikilink")（オーストラリア発祥の[ホームオートメーション](../Page/ホームオートメーション.md "wikilink")規格）や[ECHONET](https://ja.wikipedia.org/wiki/ECHONET "wikilink")（日本発祥の同様の規格）とも競合している。

[Embedded_World_KNX_TP_Demo_Board.jpg](https://ja.wikipedia.org/wiki/File:Embedded_World_KNX_TP_Demo_Board.jpg "fig:Embedded_World_KNX_TP_Demo_Board.jpg")

## 構成モード

KNX 機器は二種類に分類される。

  - **E-mode**（Easy mode、簡易モード） - 取り付けに基本的な訓練が必要。ユーザーの環境に合わせたパラメータ設定が必要である。
  - **S-mode**（System mode、システムモード） - [インテリジェントビル](../Page/インテリジェントビル.md "wikilink")として建築時に実装される機器。個々のビルの環境に合わせてプログラミングする必要がある。

## 日本におけるKNX

日本ではまだ商業物件への採用実績は少ないが、2014年に日本KNX協会が日本におけるKNXを代表するナショナルグループ(国別支部)として設立され、KNXの啓蒙及び普及活動を行っている。

## 関連項目

  - [インテリジェントビル](../Page/インテリジェントビル.md "wikilink")
  - [ホームオートメーション](../Page/ホームオートメーション.md "wikilink")
  - [タッチパネル](../Page/タッチパネル.md "wikilink")

## 外部リンク

  - [KNX Association 公式サイト](http://www.knx.org/)
  - [KNX UK 公式サイト](http://www.knxuk.org/)
  - [日本KNX協会 公式サイト](http://www.knx.org/jp/)

[cs:EIBA](https://ja.wikipedia.org/wiki/cs:EIBA "wikilink") [sq:EIB sistemet](https://ja.wikipedia.org/wiki/sq:EIB_sistemet "wikilink")

[Category:制御工学](https://ja.wikipedia.org/wiki/Category:制御工学 "wikilink") [Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink") [Category:ビルオートメーション](https://ja.wikipedia.org/wiki/Category:ビルオートメーション "wikilink") [Category:ホームオートメーション](https://ja.wikipedia.org/wiki/Category:ホームオートメーション "wikilink")