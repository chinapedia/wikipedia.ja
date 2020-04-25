> この記事は[PictBridge](https://ja.wikipedia.org/wiki/PictBridge)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Canon_PIXUS_560i_expand.jpg "wikilink") **PictBridge**（ピクトブリッジ）は、[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")などのイメージングデバイスと[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")を直接接続して印刷を行なうための[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")である。2002年12月に[キヤノン](https://ja.wikipedia.org/wiki/キヤノン "wikilink")、[オリンパス](https://ja.wikipedia.org/wiki/オリンパス "wikilink")、[セイコーエプソン](../Page/セイコーエプソン.md "wikilink")、[ソニー](../Page/ソニー.md "wikilink")、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")、[富士フイルム](../Page/富士フイルム.md "wikilink")が共同提案した規格案をもとに、[2003年](../Page/2003年.md "wikilink")2月、[カメラ映像機器工業会](https://ja.wikipedia.org/wiki/カメラ映像機器工業会 "wikilink")(CIPA)が業界の標準規格とした。

## 概要

デジタルカメラは、撮影した静止画情報を[デジタル](../Page/デジタル.md "wikilink")データとして保持し出力するカメラである。デジタルカメラで撮影された画像は、デジタルカメラに搭載されているディスプレイや、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")などで閲覧されるのが一般的である。しかし、撮影した画像を印刷し、[銀塩写真](../Page/銀塩写真.md "wikilink")と同じように用いるという需要も多い。デジタルカメラで撮影した画像を印刷するためには、多くの場合、まずPCにデータを転送する必要があったことが、ユーザーの利便性を損なっていた。デジタルカメラとプリンタを直接接続できる機種もあったが、メーカー各社で独自の方式が採用されており、直接接続が可能な機種は限定されていたという問題があった。このような状況を解決するために提案された規格が**PictBridge**である。

PictBridgeでは、撮影装置と印刷装置との間の通信仕様が規格によって標準化されており、PictBridgeに対応している撮影装置と印刷装置であれば、異なるメーカー製であっても直接接続して印刷ができる。一般的なデジタルカメラの他の撮影装置では、[デジタルビデオカメラ](https://ja.wikipedia.org/wiki/デジタルビデオカメラ "wikilink")や[カメラ付携帯電話](../Page/携帯電話.md "wikilink")、[オシロスコープ](../Page/オシロスコープ.md "wikilink")などでも対応した機種が販売されており、デスクトッププリンターの他の印刷装置ではモバイル向けプリンター\[1\]が対応している。

## 仕様概略

PictBridgeの採用製品は、撮影装置とプリンター間の接続にUSBケーブルを用いるものが多い。USBを使う場合には\[2\]、PictBridgeソフトウェア側でUSBのPTPトランスポートレイヤー上に新たにDPSレイヤーを設け、プリントとストレージに関して、それぞれクライアントとサーバーの動作を行えるようになっている。 また、接続にはUSB以外にも[赤外線通信](https://ja.wikipedia.org/wiki/赤外線通信 "wikilink")を使うこと\[3\]も許される。

画像の転送には[PTP](https://ja.wikipedia.org/wiki/PTP "wikilink")(Picture Transfer Protcol)を用いている。PTPもデータ転送にUSBでなければならない訳ではないが、USB上で転送するための規格と実装が存在しており、その結果PictBridgeもUSBで転送ということになる。なお、イーサネット上で画像を転送するプロトコルであるPTP/IPはPTPの上位互換であるため、PTP/IPを使用したPictBridge通信も可能と思われるが、実装した機器は存在しない。

機器接続後、デジタルカメラ側に印刷設定などの画面が表示され、デジタルカメラ側の操作で印刷する。機種によっては、割付印刷や画像一覧の印刷など、様々な設定が可能となっている。これらの印刷設定は、デジタルカメラとプリンタの両方が対応している機能のみ使用することができる。

  - DC-001-2003 Revision 1.0
  - DC-001-2003 Revision 2.0

## 出典・脚注

## 関連項目

  - [PTP](https://ja.wikipedia.org/wiki/画像転送プロトコル "wikilink")(Picture Transfer Protcol)
  - [DPOF](https://ja.wikipedia.org/wiki/DPOF "wikilink")(Digital Print Order format)

## 外部リンク

  - [PictBridge](http://www.cipa.jp/pictbridge/index_j.html) (CIPA)

[Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink") [Category:デジタルカメラ](https://ja.wikipedia.org/wiki/Category:デジタルカメラ "wikilink") [Category:プリンター](https://ja.wikipedia.org/wiki/Category:プリンター "wikilink")

1.  PictBridge対応のモバイル向けプリンターの例としては、富士写真フイルムの[Pivi](../Page/Pivi.md "wikilink")及びポラロイドのPoGoなどがある。
2.  USB Revision 2.0を想定している。
3.  [富士フイルム Pivi MP-70](http://fujifilm.jp/personal/print/mobileprinter/pivi/index.html)