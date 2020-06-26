> この記事は[UART](https://ja.wikipedia.org/wiki/UART)から翻訳されています。


**UART** (Universal Asynchronous Receiver/Transmitter, ユーアート) は、[調歩同期方式による](https://ja.wikipedia.org/wiki/同期方式#調歩同期式 "wikilink")[シリアル信号を](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")[パラレル](../Page/パラレル.md "wikilink")信号に変換したり、その逆方向の変換を行うための[集積回路](../Page/集積回路.md "wikilink")である。本機能のみがパッケージングされたICで供給されるものと、[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の[ペリフェラル](https://ja.wikipedia.org/wiki/ペリフェラル "wikilink")の一部として内蔵されるものとがある。[マキシムのMAX](https://ja.wikipedia.org/wiki/マキシム・インテグレーテッド "wikilink")232のような、[RS-232](../Page/RS-232.md "wikilink")C規格に準拠する信号レベルに変換するICと組み合わせて、外部機器との[インタフェースとして利用されるのが一般的である](../Page/インタフェース_\(情報技術\).md "wikilink")。UARTに、[同期方式のシリアル信号を変換するための回路を追加したものを](https://ja.wikipedia.org/wiki/同期方式#同期式 "wikilink")、**USART** (Universal Synchronous Asynchronous Receiver/Transmitter) と呼ぶ。

## 代表的なUART

代表的なUARTとしては、[ナショナル セミコンダクターの開発した](../Page/ナショナル_セミコンダクター.md "wikilink")**[16550A](https://ja.wikipedia.org/wiki/16550_UART "wikilink")**がある。[IBM](../Page/IBM.md "wikilink")の発売した[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")では、**16450**というUARTが採用されたが、これに[FIFO](../Page/FIFO.md "wikilink")を内蔵したものが**16550A**である。現在でも[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")の[シリアルポート](../Page/シリアルポート.md "wikilink")では、**16550A**と互換性のあるUARTが使用されている。**16450**と互換性を保つため基準発振周波数1.8432MHzな最大通信速度115.2kbpsが標準だが、この基準発振周波数を変更するか、互換性のある拡張機能を使用する事により、より高速なデータ通信速度が設定できるUARTが多い。**16550A**からの拡張機能を使う事で、**16950**系で460.8kbps、**16750**系で921.6kbpsなどと、**16550A**と速度設定条件の互換性を保ったまま高速化できる。拡張機能を使わず基準発振周波数のみ最大周波数を供給する事で、**16550A**に8MHzで0.5Mbps、**16550AF**に24MHzで1.5Mbps、**OX16C950B**に60MHzで3.75Mbpsなどと、ソフトウェア制御設定を変えずに高速化できる。拡張機能を使い基準発振周波数を最大にする事で、**OX16C950B**に60MHzで15Mbps、**XR16M255x** & **XR16M265x** & **XR20M117x** & **XR20V217x** シリーズに64MHzで16Mbpsなどと、高速化できる。**16550A**との互換性を無くし、更に高速化したUARTもある。

**16550**より以前に存在していた[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") **8251**、ナショナルセミコンダクター**[8250](https://ja.wikipedia.org/wiki/8250_UART "wikilink")**も広く使われていた。[Z80](../Page/Z80.md "wikilink")ファミリではZ80 SIO (**Z84C40**) やZ80 SCC (**Z85C30**) が存在する。Z80SCCは[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")をはじめとする多くの[UNIX](../Page/UNIX.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")で使われた。

[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けの[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")では、UARTまたはUSARTは内蔵していない品種を探す方が難しいほど一般的なペリフェラルである。例として、[フリースケール](https://ja.wikipedia.org/wiki/フリースケール "wikilink")や[ルネサス エレクトロニクスでは](https://ja.wikipedia.org/wiki/ルネサス_エレクトロニクス "wikilink")、SCI (Serial Communication Interface) という名前でUSARTの機能が内蔵されている。現在でも、[8](../Page/8ビット.md "wikilink")〜[16ビット](../Page/16ビット.md "wikilink")のローコストのマイクロコントローラではUSARTが唯一の通信インタフェースであることも多いが、一方で[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")ではシリアルポートを搭載しない機種が大勢を占めるようになった。このため、このようなマイクロコントローラとパーソナルコンピュータ間でデータ通信を行うために、市販の[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")－シリアル変換ケーブルがよく用いられる。

## UARTの原型

[DEC社の](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")に使われたテレタイプライター[ASR-33](../Page/ASR-33.md "wikilink")は一個だけの円盤状[ディストリビュータ](https://ja.wikipedia.org/wiki/ディストリビュータ "wikilink")\[1\]に**摺動子**を回転させ直列・並列相互変換を行い四線式非同期（調歩同期/スタート・ストップ方式、20mA カレントループ）[半二重](https://ja.wikipedia.org/wiki/半二重 "wikilink")通信方式でつながった。DEC社のコンピュータ側のこの変換機能に相応するのは発振器を搭載したエラー検出機能のない[トランジスタ](../Page/トランジスタ.md "wikilink")による簡素な独自回路の専用**モジュール**（フリップチップモジュール）であり、ジャンパー線で通信速度110[bpsと](../Page/ビット毎秒.md "wikilink")300bpsを選べ、初期のUARTはクロックと通信速度選択入力を除けばその基本的回路機能をそのまま踏襲IC化したものである。以後USART、[SDLC](https://ja.wikipedia.org/wiki/SDLC "wikilink")/[HDLC](https://ja.wikipedia.org/wiki/HDLC "wikilink")や[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")などの直列転送の集積回路や通信制御[プロトコル](../Page/プロトコル.md "wikilink")へと進化してゆく。

## UARTが検出するエラー

UARTはデータの信頼性を保つために、エラーを検出する機能を持つ。UARTは、[割り込みや内蔵](../Page/割り込み_\(コンピュータ\).md "wikilink")[レジスタによって](../Page/レジスタ_\(コンピュータ\).md "wikilink")、マイクロプロセッサにエラーが発生したことを伝える。以下に、UARTが検出するエラーを示す。

  - パリティエラー
    受信した[キャラクタの](../Page/キャラクタ_\(コンピュータ\).md "wikilink")[パリティビット](../Page/パリティビット.md "wikilink")が誤っていたときに発生するエラー。[パリティ](../Page/パリティ.md "wikilink")無効の設定にしているときは発生しない。
  - オーバランエラー
    受信バッファに格納されたキャラクタをマイクロプロセッサが取り出さないうちに、[シフトレジスタ](../Page/シフトレジスタ.md "wikilink")に次のキャラクタが揃ってしまったときに発生するエラー。取り出されなかったキャラクタは失われる。
  - フレーミングエラー
    ストップビットを受信すべきタイミングで、信号がストップビットの[論理値](https://ja.wikipedia.org/wiki/論理値 "wikilink")ではなかったときに発生するエラー。

## 関連項目

  - [シリアルケーブル](https://ja.wikipedia.org/wiki/シリアルケーブル "wikilink")
  - [EIA-574](../Page/EIA-574.md "wikilink")
  - [RS-232](../Page/RS-232.md "wikilink")
  - [8250 UART](https://ja.wikipedia.org/wiki/8250_UART "wikilink")
  - [16550 UART](https://ja.wikipedia.org/wiki/16550_UART "wikilink")

## 脚注

<references />

[Category:制御工学](https://ja.wikipedia.org/wiki/Category:制御工学 "wikilink") [Category:データ転送](https://ja.wikipedia.org/wiki/Category:データ転送 "wikilink")

1.  [ASR-33のディストリビュータ（分配器）写真（手前）](http://www.flickr.com/photos/twylo/128712274/in/photostream/)；スタート、情報8ビット、ストップの計10本線の信号が回転によって直列・並列変換される。接触圧力が偏在しないように時計の12時4時8時の3位置に摺動子が配置される。写真は「ストップ」信号の位置。