> この記事は[NetBurst](https://ja.wikipedia.org/wiki/NetBurst)から翻訳されています。


**NetBurstマイクロアーキテクチャ**（ネットバースト・マイクロアーキテクチャ、NetBurst Microarchitecture）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の8世代目の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系として開発された[CPU](../Page/CPU.md "wikilink")の基本設計である。

命令解釈を行う[フロントエンド](../Page/フロントエンド.md "wikilink")と命令処理を行うバックエンドとを完全に分離することでCPUの機能拡張への対応や高[クロック](../Page/クロック.md "wikilink")化が容易になるよう設計され、[2000年](../Page/2000年.md "wikilink")の[Pentium 4で初めて採用された](../Page/Pentium_4.md "wikilink")。しかしプロセスの微細化に伴い、高消費電力と高発熱という問題が深刻化し、[2006年](../Page/2006年.md "wikilink")以降、これらの問題を改善した[Coreマイクロアーキテクチャ](../Page/Coreマイクロアーキテクチャ.md "wikilink")に置き換えられ[2007年](../Page/2007年.md "wikilink")に生産を終了した。

## 概要

[2000年](../Page/2000年.md "wikilink")、インテルは[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")の[Pentium Pro以来続いてきた](../Page/Pentium_Pro.md "wikilink")[P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")を大幅に変更した**NetBurstマイクロアーキテクチャ**を採用した。従来から用いられてきたP5やP6という没個性的な呼称を踏襲せず**NetBurst**（ネットバースト）と命名されたことは、Pentium 4で実装した[SSE](../Page/ストリーミングSIMD拡張命令.md "wikilink")2命令などによってストリーミング・ビデオなどのインターネット利用シーンでパフォーマンスを発揮する、新たなマイクロアーキテクチャの誕生をユーザに印象づけるために行われたと推定される。

NetBurstマイクロアーキテクチャは、極端に小さいL1[キャッシュ](../Page/キャッシュ.md "wikilink")、比較的大きなL2キャッシュ、帯域の広い[FSBなど](../Page/フロントサイドバス.md "wikilink")、他社を含め従来のプロセッサのそれとは大きく異なる点を多数備えている。

L1キャッシュはデータと命令とを分離して格納するが、命令は命令解釈(デコード)され、より細かな操作の集まりであるμOPsに変換された状態でL1キャッシュに格納される。この命令を格納するL1キャッシュをトレース・キャッシュと呼ぶ。デコーダは、NetBurstマイクロアーキテクチャの柔軟性と拡張性の核となっている所でもありマイクロコードで機能変更や拡張を行うことが可能である。この柔軟性・拡張性を活かすことで比較的短い開発期間で[HTTや](../Page/ハイパースレッディング・テクノロジー.md "wikilink")[SSE3や](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE3 "wikilink")[Intel 64や](https://ja.wikipedia.org/wiki/x64 "wikilink")[Intel VT等を追加した](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink")。このデコーダは、同時に1命令までの[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[命令をμOPsに変換が可能であるが](../Page/命令セット.md "wikilink")、[P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")が同時に3命令まで変換可能だったのと比べると劣る。しかし、命令実行時にトレース・キャッシュに目的の命令が格納されていれば命令実行時間のおよそ1/3を占めるデコードを省くことが可能となる。

Pentium 4は命令実行を行う[パイプライン段数が同社の](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")[Pentium IIIや](../Page/Pentium_III.md "wikilink")[AMD社の](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[Athlon](../Page/Athlon.md "wikilink")に比べて大きく増加している。Pentium III が 10段であったのに対し、Pentium 4 では 20段(Prescottでは 31段)にも達し、Pentium 4 において命令実行パイプラインより分離された命令解釈(デコード)ステージを含めると更に段数は増える。パイプライン段数の増加は動作[クロック](../Page/クロック.md "wikilink")周波数を向上させやすいというメリットがあるが、条件分岐命令の予測ミスによりパイプラインがストールしてしまいCPUの動作密度が低下するというデメリットも伴う。そのため、NetBurstマイクロアーキテクチャはクロックあたりの処理性能が従来のアーキテクチャ（P6やAMD-K7など）と比較して劣る。

しかし、従来の条件分岐を多用するプログラムは現状より大幅な向上は求められておらず、それに代わって「[ストリーミングSIMD拡張命令](../Page/ストリーミングSIMD拡張命令.md "wikilink")2 (SSE2) 」など新たに実装した命令を用いることで動作クロックに比例して処理能力が向上するアプリケーションが主流になるとの予想に基づいてNetBurstマイクロアーキテクチャは開発されている。比較的苦手な条件分岐処理においても動作クロックの向上によって性能の向上が期待できる。また、[ALUのうち](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")2個はクロック周波数の2倍で動作する等、演算能力の強化が図られている。

そして次世代あるいは次々世代Pentium 4で実装されると一般に考えられていた「**[ハイパースレッディング・テクノロジー](../Page/ハイパースレッディング・テクノロジー.md "wikilink") (HTT)**」もNetBurstマイクロアーキテクチャの柔軟な構造を活用し、第一世代のWillametteでは使用できない状態で販売されていたものの完成されていたと見られる。HTTはCPU動作密度の低下を補い、CPU全体としての演算能力を向上させるためのものである。また後に、SSE3命令も追加される。

NetBurstマイクロアーキテクチャを採用したPentium 4は、その性格上必然的に動作クロック周波数が増加した。動作クロック=CPUの性能、そのCPUを搭載したコンピューターの性能だと大きく誤解している[消費者](../Page/消費者.md "wikilink")に対し高性能という印象を与えることもあった。しかし「高クロック＝高性能」とは一概に言えないことから、発熱や消費電力を増大させる高クロックの弊害が顕著になり、不満が漏れる事となる。

なお誤解される事が多いが、NetBurstアーキテクチャ向けにコンパイルされたアプリケーションに関しては、P6アーキテクチャ向けのアプリケーションで同様な処理を行うよりも高速ではある(特に、SSE命令を多用する場合)。

ただし、NetBurstアーキテクチャが登場した当初は、当然ながら、従来のP6アーキテクチャ向けにコンパイルされたアプリケーションが大半であった。 これらP6アーキテクチャ向けのアプリケーションを、NetBurstアーキテクチャで実行した際の実効性能は、同一クロックのP6プロセッサをほぼ下回っており、これが後々まで、NetBurstアーキテクチャの実行効率の悪さの印象として固定化された。

### 発熱と消費電力の深刻な問題

NetBurstマイクロアーキテクチャは、パイプライン段数を増やすことにより分岐予測ミスのペナルティが増加してクロック周波数あたりの性能が低下しても、それを上回るだけクロック周波数が向上すればトータルの性能は向上する、という理論\[1\]に基づき設計された。これは、半導体プロセスが微細化すれば動作周波数は向上し、消費電力は下がるというスケーリング則が成立し続けることを前提としたものであった。

一般的に、発熱や消費電力は動作クロックに比例して大きくなる。スケーリング則が成り立っていた2000年代初頭までは、製造プロセスを微細化することで動作電圧を低減し発熱や消費電力を抑えることができたが、微細化がより高度になることにより**[リーク（漏れ）電流](../Page/リーク電流.md "wikilink")**と呼ばれる電流が問題視されるようになった。

漏れ電流はどのような半導体でも発生する。コンピュータ以外も含むいかなる回路の中で、漏れ電流はその回路の動作に悪影響を与える存在として排除の対象となる。特にnm([ナノメートル](../Page/ナノメートル.md "wikilink"))単位で設計されるようになった集積度の極めて高いマイクロプロセッサ類では、それまで大きな問題にならなかった漏れ電流が、実際の動作による消費電力と大差ないところまで増えてしまい、半導体業界全体の問題となった。その中でも業界最大手のIntelは、業界の最先端を走っていたことからその問題に大きくつまずくことになる。

130nmプロセス世代では、その前世代の180nmプロセスからの移行で、漏れ電流の増加より電圧低減による省消費電力化の効果が勝っていたが、90nmプロセスになると漏れ電流が極端に増加してしまった。動作クロックを高めることで性能向上を図るPentium 4では、この問題が小型なコンピューター本体・CPU冷却装置の低コスト化や冷却騒音低減、低消費電力が求められるモバイル向けで顕著にあらわれた。同様の問題はAMDの[Athlon 64でも発生したが](../Page/Athlon_64.md "wikilink")、Athlon 64はクロックあたりの処理能力を高めるという従来の手法を踏襲したことと、製造技術に[SOI](../Page/SOI.md "wikilink")(Silicon on Insulator)を採用し、その影響を大きく抑えることに成功した。ただし、AMDの次世代マイクロアーキテクチャの開発には少なからずの影響を及ぼした。Pentium 4においても漏れ電流抑制技術が採用されたが、Intelは高コストで製造に手間が掛かるSOIを敬遠し、[歪みシリコン](https://ja.wikipedia.org/wiki/歪みシリコン "wikilink")と呼ばれる技術に留まった。その結果、消費電力の大きさがPentium 4の欠点としてクローズアップされた。

### 開発の終焉

最終的に10GHzへ到達することを予定していた動作クロックの向上による性能向上は断念せざるを得ず、4GHzの製品は予告だけで終わった。また、モバイル用途では絶対性能は高くないことから当初Pentium 4より格下に位置づけられていた[Pentium MをPentium](../Page/Pentium_M.md "wikilink") 4よりも高位の製品として販売することとなった。

Pentium 4の動作クロックは、2004年11月に発表された3.8GHzが最高となった。そしてさらに消費電力が増大すると見られたTejasと呼ばれる次世代製品の開発は中止され、CPUの性能向上はクロック数の向上から、処理効率の改善やデュアル・[マルチコア](../Page/マルチコア.md "wikilink")化へと大きな転換点を迎えることになる。そのためインテルはCoreマイクロアーキテクチャである[Coreシリーズの開発にシフトし](../Page/Intel_Core.md "wikilink")「NetBurstマイクロアーキテクチャ」の開発は2007年に事実上終了した（[外部リンク「Intel、Pentium D 945などを生産中止～NetBurstが終息へ」,PC watch 2007年8月10日記事も参照](http://pc.watch.impress.co.jp/docs/2007/0810/intel2.htm)）。このインテルの動きに対し、様子見をしていたAMDもデュアルコア版Athlon 64（[Athlon 64 X2](../Page/Athlon_64_X2.md "wikilink")）を前倒しして市場に投入した。

## 採用された製品

  - [Pentium 4](../Page/Pentium_4.md "wikilink")
      - [Pentium 4-M](../Page/Pentium_4-M.md "wikilink")
  - [Pentium D](../Page/Pentium_D.md "wikilink")
  - [Pentium Extreme Edition](../Page/Pentium_Extreme_Edition.md "wikilink")
      - Pentium 4 Extreme Edition
  - [Celeron D](https://ja.wikipedia.org/wiki/Celeron "wikilink")
  - [Mobile Celeron](https://ja.wikipedia.org/wiki/Celeron#モバイルCeleron "wikilink")（一部）
  - [Xeon](../Page/Xeon.md "wikilink")（一部）
      - Xeon MP

## 外部リンク

  - [インテルのプレスリリース](http://www.intel.co.jp/jp/intel/pr/press2000/000823c.htm)

## 脚注

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink") [Category:X86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:X86アーキテクチャ "wikilink")

1.  E. Sprangle and D. Carmean, [Increasing Processor Performance by Implementing Deeper Pipelines](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=1003559), Proc. ISCA-29, 2002. この文献では、周波数向上による性能向上が分岐予測ミスのペナルティを上回る52段まではパイプラインを深くできる、と予測している。