> この記事は[Intel 8086](https://ja.wikipedia.org/wiki/Intel_8086)から翻訳されています。


**Intel 8086**（インテル8086）は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が開発した[16ビット](https://ja.wikipedia.org/wiki/16ビット "wikilink") [マイクロプロセッサ](https://ja.wikipedia.org/wiki/マイクロプロセッサ "wikilink")([CPU](../Page/CPU.md "wikilink"))。[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")(80x86)アーキテクチャの最初のマイクロプロセッサで、[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")に発表された。

[日本電気](../Page/日本電気.md "wikilink")の[PC-9801など](https://ja.wikipedia.org/wiki/PC-9800シリーズ "wikilink")[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")に広く採用された。対応する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に、[MS-DOS](../Page/MS-DOS.md "wikilink")、PC-DOS、[CP/M-86](https://ja.wikipedia.org/wiki/CP/M-86 "wikilink")があった。

シリーズには、外部データバスを[8ビット](https://ja.wikipedia.org/wiki/8ビット "wikilink")にした低価格版の[8088があり](https://ja.wikipedia.org/wiki/Intel_8088 "wikilink")、初代の[IBM PCにも採用された](https://ja.wikipedia.org/wiki/IBM_PC "wikilink")。協調して働くように準備されていた[数値演算コプロセッサに](https://ja.wikipedia.org/wiki/FPU "wikilink")[8087があった](https://ja.wikipedia.org/wiki/Intel_8087 "wikilink")。また、使われる機会は少なかったが、8089というI/Oプロセッサも存在した。

当時ライバルとされた製品には、[モトローラ](../Page/モトローラ.md "wikilink")の[68000系プロセッサがある](../Page/MC68000.md "wikilink")\[1\]。

## アーキテクチャ

8086は8ビットアーキテクチャであった[8080を](../Page/Intel_8080.md "wikilink")16ビットに拡張し、乗除算などの命令を強化したCPUである。アドレスバスは20ビットに、データバスは16ビットに拡張された(姉妹品に外部データバスを8ビットに留めた8088もある)。8080とバイナリーレベルの[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")はないが、開発にあたってIntelは、8080からの速やかな移行を最重点事項に置き、8080の[アセンブラ](https://ja.wikipedia.org/wiki/アセンブリ言語 "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")に一切の手を加えることなく再アセンブルするだけで、8086用のバイナリを生成する事も出来た\[2\]。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Register_8086.PNG "wikilink") 8080のアーキテクチャと大きく異なるのは、演算用のアドレス[レジスタのほかに](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\) "wikilink")、**セグメントレジスタ**という、アドレス変換のための16ビットのレジスタを持っていることである。実際にCPUがアクセスするアドレスは、16ビット幅のレジスタによって指定された64KBのアドレスに、さらに16ビット幅のセグメントレジスタの値を16倍（左に4ビットシフト）して加算したアドレスとするため、1MBのメモリ空間を利用できた。

8086のアーキテクチャでは、プログラム内で通常表現されるアドレスの値は16ビット幅で64KBのメモリ空間である。当時、64KBのメモリ空間は1つのプログラムにとっては十分に広大であり\[3\]、セグメント機構はマルチタスクのために用意された。(8086には保護がないので、アプリケーションがセグメントレジスタを操作できるが、本来はOSが操作するものである。) 内蔵する4本のセグメントレジスタの値を全て同一にすると、8ビットの8080と同等の環境となり、8080用ソースを8086へ移植するのが容易であるほか、実行バイナリのリロケータブル化が容易であるといったメリットもあった。

しかし、8086や、その互換品・後継品がロングセラーになって使われ続けた結果、より大規模なプログラムが作られる様になると、64KBのメモリ空間は狭くなってしまい、アプリケーションのプログラムが自力でセグメントレジスタを操作して64KB以上のメモリ空間にアクセスする手法が用いられるようになった。しかし、頻繁にセグメントレジスタを操作することはプログラムを煩雑にし、実行時のオーバーヘッドも増えるため、プログラマからは非常に嫌われた。

後に批判の的となってしまったセグメント方式だが、互換性を重視しつつ開発が短期間で完了でき、かつコストパフォーマンスに優れた選択肢であった。これは、当時[モトローラ](../Page/モトローラ.md "wikilink")と激しいシェア争いを演じていたintelにとって極めて重大な要素だった。

メモリ空間を1MBとしたのは、当時使われていた40DIPパッケージにアドレス・データバスを割り当てる際に、アドレスピンを効率良く増やして割り当てられる値であったとも言われる。

また、より大容量のアプリケーションを担い、高性能を発揮する次世代のプロセッサとしては、当時計画中であった32ビットCPU、[iAPX432を充てる事が考えられていた](https://ja.wikipedia.org/wiki/Intel_iAPX_432 "wikilink")。当初、8086は8ビットアーキテクチャから次世代のiAPX 432プロセッサへのつなぎとして考えられていたため、後に大規模な拡張を行う事は一切考えられていなかった\[4\]。

演算に使えるレジスタが限定的だったり、メモリを直線的に使うのが面倒等の問題があったものの8080とのソースレベルでの互換性を重視し、既存の8080環境や[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")などのアプリケーションの移植、プログラマの移行などにも積極的であったことから、[IBM-PCへ採用され](https://ja.wikipedia.org/wiki/IBM_PC "wikilink")、現在のx86アーキテクチャの商業的な成功へとつながったと評価されている。

ハードウェア的には、供給クロックの[デューティ比](https://ja.wikipedia.org/wiki/デューティ比 "wikilink")が1:2になっている。クロックジェネレータi8284に3倍のクロックを供給し、それを3分周することにより1:2のクロックを得る。\[5\]

## プログラミングモデル

[C言語](../Page/C言語.md "wikilink")から生成されたプログラムにおいて、コードとデータのそれぞれで、デフォルトのアクセスをセグメント内のオフセットのみとするか、セグメントも併用してアクセスするか、の違いにより「コード・データともセグメント内」「コードのみセグメント内」「データのみセグメント内」「コード・データともセグメント併用」といったパターンが存在し、ライブラリ等はそれぞれ異なるものを使うため煩雑であった。デフォルトでないアドレッシングには、ポインタに `far` や `near` という修飾を付ける。プログラミングモデルあるいはメモリモデル等ともいう。

詳細は以下の通り。

  - Tiny
    コードセグメントとデータセグメントが共通で、両者合わせて64Kバイト以内。拡張子が"COM"の実行ファイルがこのモデルである。
  - Small
    コードセグメント、データセグメントのどちらも64Kバイト以内。
  - Compact
    コードセグメントは64Kバイト以内、データセグメントはfarポインタ。コードは小さいが、扱うデータが大きいときに用いられる。
  - Medium
    コードセグメントはfarポインタ、データセグメントは64Kバイト以内。コードが大きくても、扱うデータが小さい場合に利用される。
  - Large
    コードセグメント、データセグメントのどちらもfarポインタ。変数（配列）のサイズは64Kバイトに制限される。
  - Huge
    基本的にLargeと同じだが、配列などのメモリオブジェクトのサイズが64Kバイトに制限されない。

効率などの理由から、コンパイルはSmallモデルとし、必要に応じて明示的にセグメント操作をプログラマが指示する（適宜farまたはhugeポインタを使用し、また動的なメモリ確保によって64KBの制限を超える）ような作りのプログラムも多い。

## データバスについて

8086の外部データバスは16ビットであるが、アドレッシングは8ビット単位で行われ、データバスの下位8ビットが偶数アドレス、上位8ビットが奇数アドレスとなる。

8086でシステムを構築する上で、従来からある8ビットCPU用の周辺チップ（[8251](https://ja.wikipedia.org/wiki/Intel_8251 "wikilink")、[8255](https://ja.wikipedia.org/wiki/Intel_8255 "wikilink")、[8257](https://ja.wikipedia.org/wiki/Intel_8257 "wikilink")、[8259など](https://ja.wikipedia.org/wiki/Intel_8259 "wikilink")）が多用されたが、これらのデータバスは8ビットであるため、8086に接続するには、8086のデータバスの上位もしくは下位8ビットのどちらかに接続することになった。

そのため、このような構成では、8086 CPUから見ると、周辺チップの連続するレジスタが偶数アドレスもしくは奇数アドレスのみにとびとびに割り当てられる格好となる。

[PC-9800シリーズ](https://ja.wikipedia.org/wiki/PC-9800シリーズ "wikilink")では実際に上記のような構成になっており、I/Oマップが偶数アドレスと奇数アドレスで分断されている。 一方、外部データバスが8ビットの[8088を採用した](https://ja.wikipedia.org/wiki/Intel_8088 "wikilink")[IBM PCではそのようなことはなく](https://ja.wikipedia.org/wiki/IBM_PC "wikilink")、8ビットの周辺チップは連続したアドレスに存在する。XTバスの拡張カードにより増設した機器も同様である。

そのため、後に[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")で16ビットの[ISAを採用した際に](https://ja.wikipedia.org/wiki/Industry_Standard_Architecture "wikilink")、8ビットの周辺機器をサポートするために[バス・サイジング](https://ja.wikipedia.org/wiki/バス・サイジング "wikilink")の必要性が生じた。

また、PC-9800シリーズでも、[PCカード](https://ja.wikipedia.org/wiki/PCカード "wikilink")のモデムなど、IBM PCシリーズ用に開発された8ビットの周辺機器をサポートする際に、バス・サイジングの必要性が生じた。

## 脚注

<references />

## 関連項目

  - [Intel 80186](https://ja.wikipedia.org/wiki/Intel_80186 "wikilink")
      - [NEC](../Page/日本電気.md "wikilink") [V30](https://ja.wikipedia.org/wiki/NEC_Vシリーズ#V30 "wikilink") - 互換製品。
  - [Intel 80286](../Page/Intel_80286.md "wikilink")
  - [Intel 80386](../Page/Intel_80386.md "wikilink")
  - [x86-32](https://ja.wikipedia.org/wiki/x86-32 "wikilink")
  - [x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink")

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.  MC68000は8086よりも2年遅く登場し2倍以上のトランジスタを使っており、本来は同じ土俵で比べられるものではないが、しばしばライバル視される。
2.  詳細は[86-DOS\#PC DOS の誕生及び](https://ja.wikipedia.org/wiki/86-DOS#PC_DOS_の誕生 "wikilink")[CP/M-86](https://ja.wikipedia.org/wiki/CP/M-86 "wikilink")も参照のこと。
3.  参考までに、初代IBM PCはRAM 64KB(16KBモデルもあったが売れず)、初代NEC PC-9801はRAM 128KBだった。
4.  ティム ジャクソン著 翔泳社刊 「インサイド インテル」より。
5.  [沖電気製MSM](https://ja.wikipedia.org/wiki/沖電気工業 "wikilink")80C86A-10(10MHz版)は1:1になっているなど、セカンドソースのメーカやクロック周波数によっては異なる場合もある。なお、インテルのi8086-1(10MHz版)では1:2である。