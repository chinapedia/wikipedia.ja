> この記事は[HAL \(ソフトウェア\)](https://ja.wikipedia.org/wiki/HAL_\(ソフトウェア\))から翻訳されています。


**HAL**（ハル）は [デーモン型の](../Page/デーモン_\(ソフトウェア\).md "wikilink")[Hardware Abstract Layerの一種であり](https://ja.wikipedia.org/wiki/Hardware_Abstract_Layer "wikilink")、[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")[アプリケーションがハードウェア情報に容易にアクセスできるようにすることで](../Page/アプリケーションソフトウェア.md "wikilink")[バスやデバイスの種類に寄らずに各種デバイスを利用できるようにする](../Page/バス_\(コンピュータ\).md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトである。これにより、[GUIが一貫した形式で全ての](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[リソースをユーザーに提示できる](../Page/計算資源.md "wikilink")。

例えば、HAL は[リムーバブルメディア](../Page/リムーバブルメディア.md "wikilink")ドライブの情報を収集し、メディアの出し入れをユーザーの[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")に通知する。

従来、デスクトップアプリケーションであってもハードウェアへのアクセスは直接[カーネル](../Page/カーネル.md "wikilink")を使って行うしかなかった。しかし、カーネルはデバイスについて全てを知っているわけではないため、この方式では正確さに難点があり、かつ面倒だった。例えば、[MP3](../Page/MP3.md "wikilink")プレイヤーや[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")などはユーザインタフェースでは単なる[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")として示されることがあった。従って、システムに接続されている周辺機器を一覧するようなデスクトップのユーザインタフェースはほとんどなかった。

HAL を使うと、ハードウェアの種類毎の重要な情報が一貫した形式で利用可能となる。新たなデバイスが追加されたとき、追加されたデバイスの種類などの情報を伴って非同期シグナルがシステムのメッセージバス上にブロードキャストされる。このメッセージバスに接続しておくことで、デスクトップアプリケーションが新たなハードウェアを見つけることが可能となる。システムレベルのスクリプトでデバイスを設定することもできる。事実上、HAL は[プラグアンドプレイ](../Page/プラグアンドプレイ.md "wikilink")を可能とする。

HAL [デーモンはデバイスのリストを実際のハードウェアの状態に合わせて維持する](../Page/デーモン_\(ソフトウェア\).md "wikilink")。各デバイスの状態は事前に定義されたキーと値の組で表される。各デバイスオブジェクトの識別には Unique Device Identifier (UDI) という識別子が使われる。キーと値のペアには型があり、HAL の仕様で定義されている。従って、HAL のユーザーはそれらの意味を知ることができる。

## 移行

HALはすでに旧態化しており、現在は単にメンテナンスのみが行われている。HALの機能は[DeviceKit](https://ja.wikipedia.org/wiki/DeviceKit "wikilink")や[udev](https://ja.wikipedia.org/wiki/udev "wikilink")等に移行している。

## 外部リンク

  - [HAL - Hardware Abstraction Layer](http://www.freedesktop.org/wiki/Software/hal) at [freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink")
  - [Making Hardware Just Work](http://ometer.com/hardware.html) by Havoc Pennington （2003年7月）

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink") [Category:ユーザインタフェース](https://ja.wikipedia.org/wiki/Category:ユーザインタフェース "wikilink") [Category:人間とコンピュータの相互作用](https://ja.wikipedia.org/wiki/Category:人間とコンピュータの相互作用 "wikilink")