> この記事は[MPC5xx](https://ja.wikipedia.org/wiki/MPC5xx)から翻訳されています。


[200px](https://ja.wikipedia.org/wiki/ファイル:PPC-ECM.jpg "wikilink") **MPC5xx**ファミリのプロセッサ、例えば**MPC555**や**MPC565**は、[32ビット](../Page/32ビット.md "wikilink")[PowerPC](../Page/PowerPC.md "wikilink")アーキテクチャの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。

## 概要

40～66[MHzで動作する](https://ja.wikipedia.org/wiki/メガヘルツ "wikilink")。[エンジンコントローラ](https://ja.wikipedia.org/wiki/エンジンコントロールユニット "wikilink")・トランスミッションコントローラなどの自動車向けでよく利用されている。これらは、組み込まれた周辺インタフェースと、[MMUなし](https://ja.wikipedia.org/wiki/メモリ管理ユニット "wikilink")、大きなオンチップ[SRAM](../Page/Static_Random_Access_Memory.md "wikilink")、1[MBにも達する非常に大きく遅延の小さいオンチップ](https://ja.wikipedia.org/wiki/メガバイト "wikilink")[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")で構成され、[アーキテクチャが制御用アプリケーションに適応していることを意味する](../Page/コンピュータ・アーキテクチャ.md "wikilink")。この変わった構成のため、MPC5xxは一般的には[マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")とみなされている。最初のPowerPC仕様で定められた、ハードウェアが固定ページアドレスを変換するブロックアドレス変換の代わりに、MPC5xxコアは可変ページサイズをサポートする、ソフトウェアによるアドレス変換機構を提供している。このアドレス変換のモデルは、Power命令セット仕様の組み込み型[MMUモデルの基盤である](https://ja.wikipedia.org/wiki/メモリ管理ユニット "wikilink")。

**MPC5xx** - すべてのPowerPC 5xxシリーズのプロセッサは、この名前を持っている。

より柔軟で強力な[PowerPC 55xxシリーズに人気が出たため](https://ja.wikipedia.org/wiki/PowerPC_e200 "wikilink")、PowerPC 5xxシリーズの開発は終了している。

## 特徴

周辺デバイスインタフェースはモデルにより異なるが、[AD変換器](../Page/アナログ-デジタル変換回路.md "wikilink")(ADC)、タイム・プロセッサ・ユニット(TPU)、[GPIO](https://ja.wikipedia.org/wiki/GPIO "wikilink")、[UART](../Page/UART.md "wikilink")／[シリアルポート](../Page/シリアルポート.md "wikilink")(QSMCM)を備えていることが多い。MPC5xxファミリーはMPC8xx [PowerQUICC](../Page/PowerQUICC.md "wikilink")ファミリーの後継であり、このことは[ハーバード・アーキテクチャ](https://ja.wikipedia.org/wiki/ハーバード・アーキテクチャ "wikilink")のシングルコアを採用していることを意味している。MPC8xxファミリと異なり、MPC5xxファミリは[浮動小数点コプロセッサを備えている](../Page/FPU.md "wikilink")。MPC509のような初期のチップは[命令キャッシュを持っているが](../Page/キャッシュメモリ.md "wikilink")、最近のチップはプロセッサから命令をバーストアクセス可能な、大量のオンボード[NORフラッシュメモリを持っている](https://ja.wikipedia.org/wiki/NOR型フラッシュメモリ "wikilink")。フラッシュメモリは、ダイの広い領域を必要としチップの価格を上昇させるため、いくつかの低コストチップでは省略されている。多くのコントローラアプリケーションは、あまり大きくないデータセットと遅延の少ない非常に長い制御ループを持っている。この場合データと命令に対する直接的なアクセスが重要になる。もし、ほとんどのデータを、プロセッサが1クロックでアクセスできるオンチップのSRAMに格納できるならば、性能は非常に良くなる。チップの外部のデータに頻繁にアクセスする必要がある場合は、チップは外部RAMからバーストアクセスできず、非常に遅い[バスアクセスプロトコルを使用するため](../Page/バス_\(コンピュータ\).md "wikilink")、性能は低下する。デフォルトのメモリアドレスを決め、いくつかのベースレジスタを書くことでプログラムが可能な、単純なメモリインタフェースのため、このチップは自動車向けや産業機器向けだけでなく、ホビー用としても人気がある。

## 関連項目

  - [PowerPC](../Page/PowerPC.md "wikilink")
  - [Powerアーキテクチャ](https://ja.wikipedia.org/wiki/Powerアーキテクチャ "wikilink") ([:en:Power Architecture](https://ja.wikipedia.org/wiki/:en:Power_Architecture "wikilink"))

## 外部リンク

  - [Website on the MPC555 and MPC5554 microcontrollers](http://www.ee.ualberta.ca/~jasmith/mpc555/)
  - [Freescale's MPC5xx page](http://www.freescale.com/webapp/sps/site/taxonomy.jsp?nodeId=0162468rH3bTdG06C18648)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")