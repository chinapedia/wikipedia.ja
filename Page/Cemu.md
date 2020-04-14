> この記事は[Cemu](https://ja.wikipedia.org/wiki/Cemu)から翻訳されています。


**Cemu**（シームー\[1\]）は[PC](../Page/PC.md "wikilink")上で動作する[Wii Uの](https://ja.wikipedia.org/wiki/Wii_U "wikilink")[エミュレーター](https://ja.wikipedia.org/wiki/エミュレーター "wikilink")である。「CaféEmulation」の略称であり、「Café」はWii Uのコードネームである\[2\]。開発は[クローズドソース](../Page/クローズドソース.md "wikilink")となっている。

[Microsoft Windows向けに](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")2015年10月13日にリリースされた\[3\]。2019年4月現在、2週間に一度、更新され、[Patreon](https://ja.wikipedia.org/wiki/Patreon "wikilink")を通じて寄付をしたユーザーは一般リリースの1週間前に最新版やベータ版を受け取ることができる。まだ開発中ではあるが、特定のゲームをスムーズに実行可能となっている\[4\]。2017年1月、Cemuがグラフィックパックを通じて[4K解像度](https://ja.wikipedia.org/wiki/4K解像度 "wikilink")でのゲームの実行に対応したことが発表された\[5\]。なお、このソフトウェアは[任天堂](../Page/任天堂.md "wikilink")によって公認されたものではない。

## 動作環境

  - [Windows7](../Page/Microsoft_Windows_7.md "wikilink")（x64）か、それ以降のOSバージョン
  - 4GB以上のRAM（8GB以上を推奨）
  - [OpenGL](../Page/OpenGL.md "wikilink")4.1以上（使用可能であれば4.6）
  - [Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") 2017 Microsoft Visual C++ 再頒布可能パッケージ (x64)

\[6\]

この4つの条件を満たす必要がある。

なお、[Intel](https://ja.wikipedia.org/wiki/インテル "wikilink") GPUは公式にはサポートされていない。

2020年3月現在、[Linux](../Page/Linux.md "wikilink")及び[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")版は存在しない。

## 特徴

Cemuはあくまで「PCでWii Uアプリケーションをエミュレートする実験的ソフトウェア」（原文：Experimental software to emulate Wii U applications on PC）として位置づけられている\[7\]。しかし数多くのゲームにおいてスムーズに動作可能になっており、公式サイトの互換性評価ではWiiUソフト全体の20%が「完璧（Perfect）」、35%が「プレイ可能（Playable）」と認定されている\[8\]。

### CPU

マルチスレッド処理を行い、パフォーマンスを高めている\[9\]。

### グラフィック

[OpenGL](../Page/OpenGL.md "wikilink")、または[Vulkan](https://ja.wikipedia.org/wiki/Vulkan "wikilink")で描画する。 [シェーダー](../Page/シェーダー.md "wikilink")の動的[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")に時間がかかってカクついたりフリーズする問題をクリアするため、一度使用したシェーダーを[キャッシュ](../Page/キャッシュ.md "wikilink")し、ゲーム起動前に予めコンパイルする。 しかし一部タイトル（『[ゼルダの伝説 ブレスオブザワイルド](https://ja.wikipedia.org/wiki/ゼルダの伝説_ブレスオブザワイルド "wikilink")』等）では膨大なキャッシュが必要になるため、必要なメモリ容量が膨れ上がり、起動に時間がかかる問題がある。

### サウンド

テレビとゲームパッドの両方のオーディオがサポートされている。サラウンドサウンドのサポートが計画されている。\[10\]

### コントローラー入力

2020年3月現在、WiiU GamePad、WiiU PRO コントローラ、およびWiiクラシックコントローラ/クラシックコントローラPROがエミュレートされている。また、Wiiリモコンも使用できる（ネイティブサポートを含む）。そして入力デバイスとしてのキーボード入力+ USBコントローラーがサポートされている。GamePadタッチ入力は、マウスの左クリックで制御でき、ジャイロ機能は制限付きでエミュレートされ、マウスの右ボタン及びホイールで制御可能である。\[11\]

GamePadの画面を表示するには、Tabキーを押す必要がある。CTRL + TABを押して画面を切り替えることもできる。さらに、GamePadビューは2番目のウィンドウに表示可能である。\[12\]

### オンライン接続（ニンテンドーネットワーク）

Cemuは[ニンテンドーネットワーク](https://ja.wikipedia.org/wiki/ニンテンドーネットワーク "wikilink")への接続をおおむねサポートしている。

公式サーバーへの接続には、一部のシステムファイルをWii U実機から[ダンプ](https://ja.wikipedia.org/wiki/ダンプ "wikilink")する必要がある。\[13\]

## 出典

## 関連項目

  - [ゲームエミュレータ](../Page/ゲームエミュレータ.md "wikilink")

## 外部リンク

  - （英語）

  - <http://compat.cemu.info/wiki/Main_Page>（公式Wiki/英語）

[Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink")

1.
2.
3.
4.
5.   WIRED UK|url=[https://web.archive.org/web/20170113152559/http://www.wired.co.uk/article/wii-u-cemu-emulator-4k-games|website=web.archive.org|date=2017-01-13|accessdate=2019-11-22](https://web.archive.org/web/20170113152559/http://www.wired.co.uk/article/wii-u-cemu-emulator-4k-games%7Cwebsite=web.archive.org%7Cdate=2017-01-13%7Caccessdate=2019-11-22)}}
6.
7.
8.
9.
10.
11.
12.
13.