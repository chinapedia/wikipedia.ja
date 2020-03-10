> この記事は[DataScope](https://ja.wikipedia.org/wiki/DataScope)から翻訳されています。


**DataScope**（**データスコープ**）は、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に[京セラ](../Page/京セラ.md "wikilink")が発売した[PHS](../Page/PHS.md "wikilink")端末。後に[PDC](../Page/PDC.md "wikilink")モデルも発売された。320×200ドットのモノクロ液晶画面を持ち、[ユーザーアプリケーション](https://ja.wikipedia.org/wiki/ユーザーアプリケーション "wikilink")を登録できるなど、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")のはしりと考えられている。

## 外形

二つ折りタイプ。一方のほぼ全面が緑地に黒のモノクロ[STN液晶](https://ja.wikipedia.org/wiki/STN液晶 "wikilink")画面となっており、320×200ドットの表示領域を実現している。もう一方はキーボードで、カバーを外すとType IIの[PCカード](../Page/PCカード.md "wikilink")となり、ノートPC等に直接接続できる。この形状は、開発のベースとなった [IBM](../Page/IBM.md "wikilink") の [ChipCard](https://ja.wikipedia.org/wiki/ChipCard "wikilink") VW-200 と共通しているが、厚みや重量は大幅に異なる。

サイズは 55×108×27 mmで、重量は175g。1998 年当時の基準で見ても、PHS端末としては破格の大きさである。

## モデル

  - DS-110: DataScopeシリーズ最初の製品。DDIポケット（現 [Y\!mobile](https://ja.wikipedia.org/wiki/Y!mobile "wikilink")）のPHS端末として使える。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink") 発売。

<!-- end list -->

  - DS-320: DS-110ではオプション扱いだった[PIAFS](https://ja.wikipedia.org/wiki/PIAFS "wikilink")やαデータが標準装備されている。またメニューがアイコン化されるなど、細部の変更も行われている。ただしDS-110に比べてシステムで使用するメモリ領域が大きくなり、空き領域が減少している。

<!-- end list -->

  - DataScope for DoCoMo: 通信部を PHS から[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の携帯電話に変更したモデル。

## 通信機能

### DS-110

PHS音声通信が可能である。公衆モードのほか、室内モードとトランシーバーモード、それらの自動切換えモードをサポートしている。

データ通信は、PCカード型の[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")として使う形態と、DS-110単体で[パソコン通信](../Page/パソコン通信.md "wikilink")に接続する形態がある。当初単体では [TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink") に未対応。

発売当初は2400bpsみなし音声のみだった。

[PIAFS](https://ja.wikipedia.org/wiki/PIAFS "wikilink")には別売りソフトウェアで対応したが、当初はDS-110のハードウェアでは処理が追いつかないとして、モデムとしての使用時にノートPCのCPUでPIAFS処理を行う方式のため、専用のデバイスドライバを使う必要があった。後にDS-110のCPU だけで実現できるようになり、単体使用時もPIAFS通信が可能となった。またモデムとして使用する際も標準モデムのインターフェイスでPIAFSを提供できるようになり、専用のドライバが提供されないOSからも使用できるようになっている。

別売りでα-DATA用アダプタが提供された。これを接続することで、DDI ポケット独自の通信方式であるα-DATAに対応した。

[ショートメッセージサービス](https://ja.wikipedia.org/wiki/ショートメッセージサービス "wikilink")である [Pメール](https://ja.wikipedia.org/wiki/Pメール "wikilink") は、販売時には受信のみが可能で、京セラが配布したユーザーアプリケーションを導入することで送受信可能となる。後継規格であるライトメールには対応していない。

### DS-320

DS-110と同様、PHS端末である。

データ通信において、2400bpsみなし音声が廃止され、PIAFSとα-DATAが標準搭載された。

### DataScope for DoCoMo

通信方式を[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の9600bps携帯電話に変更している。[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")、[Eメール](https://ja.wikipedia.org/wiki/Eメール "wikilink")、のほかにNTTドコモが当時展開していた[10円メール](https://ja.wikipedia.org/wiki/10円メール "wikilink")が利用できた。その後登場する[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")や[iモードメール](https://ja.wikipedia.org/wiki/iモードメール "wikilink")には対応していない。

## ユーザーアプリケーション

標準搭載のソフトウェアに加えて、ユーザーアプリケーションを4つまで導入できる。導入は、PCカードとして[Windows 3.1機および](https://ja.wikipedia.org/wiki/Microsoft_Windows_3.1 "wikilink")[Windows 95機に接続した状態で](../Page/Microsoft_Windows_95.md "wikilink")、専用の制御プログラムを使って行う。

アプリケーション開発キットは、無償で希望者に配布された。また、前述のPメール・アプリケーションのように、京セラが作成・配布したものもある。

アプリケーションはインストール・イメージの段階で物理アドレスを固定する必要があり、同時に使用するアプリケーションのアクセス範囲が衝突しないよう、事前に調整する必要があった。これは、自作アプリケーションだけを使うならともかく、第三者が公開しているアプリケーションを使う際には大きな障害となる。この制約を回避するため、アプリケーションを独自のフォーマットでデータとして導入し、メニューで選択されたアプリケーションをメモリ上に展開してから起動するユーザーアプリケーションが、有志によって公開された。

## オプション

### ID セパブルシステム

バイブレーション機能を本体ではなく、独立したユニットとしたもの。着信時に本体から微弱な電波を発し、バイブレーションユニットがその電波に反応して振動する。本体をバッグ等に入れた場合でも、バイブレーションユニットだけを身につけることで、無音で着信を知ることができる。

バイブレーションユニットは単4[乾電池](../Page/乾電池.md "wikilink")1本を電源とし、ベルトに装着するための着脱可能な金具が付属している。57×38×13mmで、外見は[歩数計](../Page/歩数計.md "wikilink")に似ている。

本体から約1mの範囲で動作する。他人のユニットが反応することを防ぐため、バイブレーションユニットには3桁の数字からなるIDが割り当てられている。本体にこのIDを設定し、対応するユニットだけを振動させる。

当時の京セラ製PHS・携帯電話端末で標準装備されていた。DataScope全モデルでも採用されており、for DoCoMo のものは若干形状が異なる。本体には振動する機能がないので、このユニットを紛失した場合はバイブレーション機能を使えない。

## 参考文献

  - MC研編 『データスコープ徹底活用ガイド』 毎日コミュニケーションズ、1997年、ISBN 4-89563-385-3。

## 外部リンク

  - 「[京セラ製PHSデータ通信端末「データスコープ」が2月20日に発売](http://www.watch.impress.co.jp/pc/docs/article/970214/ds110.htm)」 [PC Watch](https://ja.wikipedia.org/wiki/Impress_Watch "wikilink")、1997年2月14日。
  - 「[京セラ、データスコープシリーズ新機種、専用テレビ電話アダプタも](http://pc.watch.impress.co.jp/docs/article/971030/kyocera.htm) 」 PC Watch、1997年10月30日。

[Category:スマートフォン](https://ja.wikipedia.org/wiki/Category:スマートフォン "wikilink") [Category:PHS端末_(ウィルコム)](https://ja.wikipedia.org/wiki/Category:PHS端末_\(ウィルコム\) "wikilink") [Category:携帯電話端末_(NTTドコモ_第二世代)](https://ja.wikipedia.org/wiki/Category:携帯電話端末_\(NTTドコモ_第二世代\) "wikilink") [Category:携帯電話端末_(京セラ)](https://ja.wikipedia.org/wiki/Category:携帯電話端末_\(京セラ\) "wikilink") [Category:拡張カード](https://ja.wikipedia.org/wiki/Category:拡張カード "wikilink") [Category:1998年のハードウェア](https://ja.wikipedia.org/wiki/Category:1998年のハードウェア "wikilink")