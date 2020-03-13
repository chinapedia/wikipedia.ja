> この記事は[NS320xx](https://ja.wikipedia.org/wiki/NS320xx)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:National_NS32016D-6_S8520_top.jpg "wikilink") **320xx**または**ns32000**は[ナショナル セミコンダクター](../Page/ナショナル_セミコンダクター.md "wikilink") (NS) の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")シリーズである。320xxシリーズには[コプロセッサ](../Page/コプロセッサ.md "wikilink")インターフェイスがあり、[FPU](../Page/FPU.md "wikilink")や[MMU](https://ja.wikipedia.org/wiki/MMU "wikilink")といったコプロセッサを接続することができる。320xxシリーズは Swordfish CPUに受け継がれた。

## 始まり：32016と32032

このシリーズの最初のチップは**16032**である（後に**32016**と改称）。[1970年代](../Page/1970年代.md "wikilink")後半に完成したので、（少なくともナショナル セミコンダクターの言によれば）世界で最初の大量生産され販売された[32ビット](../Page/32ビット.md "wikilink")マイクロプロセッサと言えるかもしれない。このチップは[16ビット](../Page/16ビット.md "wikilink")外部データ[バスを持ち](../Page/バス_\(コンピュータ\).md "wikilink")、[24ビット](https://ja.wikipedia.org/wiki/24ビット "wikilink")外部アドレス[バスを持ち](../Page/バス_\(コンピュータ\).md "wikilink")、当初から完全な[32ビット](../Page/32ビット.md "wikilink")[命令セット](../Page/命令セット.md "wikilink")を持っていた。命令セットは非常に複雑ではあるが規則性があり、豊富なアドレッシングモードを持っていた。その設計思想は[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[VAX](../Page/VAX.md "wikilink")[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")の命令セットに近いものがある。

ナショナル セミコンダクターは関連するチップとして浮動小数点演算ユニット ([FPU](../Page/FPU.md "wikilink")) や[メモリ管理ユニット](../Page/メモリ管理ユニット.md "wikilink") (MMU）、[Direct Memory Access](../Page/Direct_Memory_Access.md "wikilink") (DMA) コントローラなどを製造した。これらのフルセットにメモリと周辺装置を加えることで32ビットコンピュータシステムを作ることができ、それまでミニコンピュータや[汎用コンピュータ](https://ja.wikipedia.org/wiki/汎用コンピュータ "wikilink")でしかできなかったマルチタスクOSを動作させることができた。

**32032**が直後にリリースされた。ほとんど完全な互換性があるが、32ビットデータバスを持っていて（アドレスバスは24ビットのまま）、若干の性能向上が見られた。これら32016と32032は信頼性に問題があると言われた。例えばCPU、FPU、MMU、DMACをセットにして動作確認した上でナショナル セミコンダクターから直接買えば、うまく動く可能性は高くなった。しかし、信頼性問題により320xxは一般化せず、ナショナル セミコンダクターは[MC68000](../Page/MC68000.md "wikilink")よりも低価格で売る破目に陥った。低価格化したことにより、32ビットシステムを安く作りたいホビーストがこれに集まったことは確かである。

32016の外部バスを8ビット化した低価格版の**32008**もある。考え方としては[MC68008](https://ja.wikipedia.org/wiki/MC68008 "wikilink")と同じで、同様に人気はなかった。

## 32332、32532、Swordfish、その他

[1980年代](../Page/1980年代.md "wikilink")、後継の**ns32332**と**ns32532**が登場した。これらは互換性を維持しつつ信頼性と性能を向上させたものである。しかし、悪評はすでに定まっており、これらが市場を得ることはなかった。

[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")、ナショナル セミコンダクターがリリースしたns32332は32032の後継バージョンである。強化点としては、アドレッシング専用ハード（高速ALUとバレルシフタとアドレスレジスタ）の追加と[命令プリフェッチ](https://ja.wikipedia.org/wiki/命令プリフェッチ "wikilink")機構、バスプロトコルの強化、コプロセッサインターフェイスの強化、マイクロコードの強化などである。同時にns32382 MMU、ns32381 FPU、そして非常に珍しい[Weitek](../Page/Weitek.md "wikilink")のFPAとのインターフェイスのためのns32310がリリースされた。

[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")春、ナショナル セミコンダクターはns32532をリリースした。動作周波数は20、25、30MHzで、MMUを内蔵してメモリ性能を向上させている。対応する新しいFPUはなく、ns32381を使った。ns32532は"パブリックドメイン"のハードウェアプロジェクト PC532 で使われた（実際に[MINIX](../Page/MINIX.md "wikilink")や[NetBSD](../Page/NetBSD.md "wikilink")の動作するマシンが作られた）。

**Swordfish**は実現しなかった**ns32732**（ときにns32764）とも呼ばれるns32532の高性能後継プロセッサである。これは市場にリリースされることはなかったが、派生物は[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")ごろ[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けにリリースされた（従来のns32000シリーズと共に低価格な製品としてNS32GX32、NS32FV16、NS32FX161、NS32FX164という名前でリリースされた）。これらのプロセッサは[レーザープリンター](../Page/レーザープリンター.md "wikilink")や[ファクシミリ](https://ja.wikipedia.org/wiki/ファクシミリ "wikilink")でそれなりに成功を収めた。

## NS32000シリーズの使用例

NS32000シリーズCPUを使用したマシンの実例である。

  - Whitechapel MG-1 - NS32016
  - Whitechapel MG200 - NS32332
  - Opus - NS16032 PC アドオンボード
  - [シークエント](../Page/シークエント・コンピュータ.md "wikilink") Balance - NS32016, NS32032 & NS32332 マルチプロセッサ
  - Heurikon VME532 - NS32532 VME カード
  - PC532 - NS32532
  - [National Semi](../Page/ナショナル_セミコンダクター.md "wikilink") ICM-3216 - NS32016
  - [National Semi](../Page/ナショナル_セミコンダクター.md "wikilink") ICM-332-1 - NS32332 w/ NS32016 I/O プロセッサ
  - [National Semi](../Page/ナショナル_セミコンダクター.md "wikilink") SYS32/20 - NS32016 PC アドオンボード w/ Unix
  - [アンコール](../Page/アンコールコンピュータ.md "wikilink") Multimax - NS32332 & NS32532 マルチプロセッサ
  - Trinity College Workstation - NS32332
  - ETH Ceres Workstation - NS32532
  - [シーメンス](../Page/シーメンス.md "wikilink") PC-MX2 - NS32016
  - Compupro 32016 - NS32016 S-100 カード
  - Symmetrics S/375 - NS32016
  - General Robotics Corp. Python - NS32032 & N32016 Q-Bus カード

## 名前の似ているプロセッサ

全く関係のない320xxという名前のプロセッサとしてWestern Digitalの作ったものがある（WE32000)。また、[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")の有名なDSPであるTMS320シリーズ（TMS32010など）もある。他にも色々な半導体企業が似たような名前を使っている。これはCPU設計者やマーケティング担当者が32ビットマイクロプロセッサに名前をつけるときに"32"という数字を入れたくなるためだろう。

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")