> この記事は[Core](https://ja.wikipedia.org/wiki/Core)から翻訳されています。


**Coreマイクロアーキテクチャ**（コアマイクロアーキテクチャ）は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")のイスラエル・ハイファの開発チームが[NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")の後継として開発した[CPU](../Page/CPU.md "wikilink")の[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")である。性能と低消費電力の両立を目指して開発された。インテルは、このマイクロアーキテクチャにおいて、CPU史上に大きく残る程の革命的な技術的転換を果たした。

[Intel Core 2で採用された](https://ja.wikipedia.org/wiki/Intel_Core_2 "wikilink")。2008年末からは徐々に後継の[Nehalemマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Nehalemマイクロアーキテクチャ "wikilink")への移行が進んでいる。

## 概要

***Intel Core 2***は高クロック主義からクロック効率主義へのパラダイムシフトを目指して開発されたCPUである。インテルのシニアアーキテクトであるボブ・バレンタインの発言によると、「Coreマイクロアーキテクチャはもはや内部RISCプロセッサのアーキテクチャではない」とした。

[CISC](../Page/CISC.md "wikilink")である[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")は1命令で複雑な処理が可能であるが、その複雑さから処理の高速化は難しいと考えられた。そこで、CPUの内部でx86命令を複数の簡単な[RISC](../Page/RISC.md "wikilink")的命令(μOPs)に分解することによって性能の向上が可能となる、との考え方が生まれた。それによって処理の向上を図った製品が、[Pentium Proから](../Page/Pentium_Pro.md "wikilink")[Pentium IIIプロセッサに続く](../Page/Pentium_III.md "wikilink")[P6マイクロアーキテクチャ](https://ja.wikipedia.org/wiki/P6マイクロアーキテクチャ "wikilink")である。

当時、半導体の製造技術の順調な進歩に後押しされ、その設計思想は妥当だと考えられていた。また、処理能力の向上を支えるクロック速度向上に伴うダイナミック電流の増加、即ち[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")の増大については、半導体技術の進歩を受けて設計ルールを微細化することにより消費電力を削減して相殺できると楽観視されていた。それに続く[Pentium 4プロセッサに代表されるNetBurstマイクロアーキテクチャは](../Page/Pentium_4.md "wikilink")、その設計思想をさらに推し進めたものである。結果、NetBurstマイクロアーキテクチャは1個のx86命令を複数の極めて単純な命令に分解し、それを深いパイプラインに投入して高速に処理することで性能を稼ぐという手法を採用した。

しかし、半導体の製造技術の進歩により処理を高速化すると消費電力は級数的に増えてしまうことが予見されるようになり、加えて[プロセスルール](https://ja.wikipedia.org/wiki/プロセスルール "wikilink")の微細化に伴う[リーク電流](https://ja.wikipedia.org/wiki/リーク電流 "wikilink")の増加が顕著になり、その現象が2000年代前半に顕著になってきた。NetBurstマイクロアーキテクチャは分解した単純な命令を大量に処理することを前提とし、それによってさらなる処理の高速化を実現する製品であったため、消費電力の増大と共に発熱問題にも直面した。 結果として、複数のCPUを搭載するサーバ用途では放熱に苦心を強いられ、多数のCPUを搭載するブレードサーバ用途には向かないものとなった。また、熱設計的にはゆとりがあるはずの[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink")PCでもその対策に悩まされるようになった。[CPU放熱ファンは大型化し高速回転して唸りをあげ](https://ja.wikipedia.org/wiki/CPUクーラー "wikilink")、放熱フィンも大型化し、これらの大きなパーツを支える仕組みを備えなければならず、コストを押し上げる要因となった。また、CPUから奪った熱がこもらない様にケース内のレイアウトを適切に設計し、ケース・ファンを設けるなど設計に注意をはらう必要があり、[BTX](https://ja.wikipedia.org/wiki/BTX "wikilink")が策定された。

一方、同時期にモバイル用として登場した[Pentium Mは](https://ja.wikipedia.org/wiki/Pentium_M "wikilink")、良好な低消費電力と比較的高い処理性能によってモバイル分野では成功を収めた。しかし、モバイル用途に限定して設計していたため、デスクトップ/サーバ分野でNetBurstマイクロアーキテクチャを置き換える対象としては不向きであった。やがてPentium Mの後継として[Intel Coreに代替わりし](https://ja.wikipedia.org/wiki/Intel_Core "wikilink")、それをベースとしたデスクトップ/サーバにも適した次世代のマイクロアーキテクチャの開発が急がれた。

**Coreマイクロアーキテクチャ**の完成により、高性能と低消費電力の両立に成功し、モバイルと高密度サーバ、そしてデスクトップと大規模サーバというカテゴリごとにそれぞれ違うマイクロアーキテクチャで対応していた製品展開を、Coreマイクロアーキテクチャから派生した単一のマイクロアーキテクチャでの対応を可能とするに至った。

Intel 3,4 Series、975X Express、965 (963) Express、946 Express、945 Expressの各チップセットファミリが対応する。

## 機能

Core 2の新しい機能としては、インテルの[CTOにより大きく](../Page/最高技術責任者.md "wikilink")5つの技術が紹介されている。

  - インテル アドバンスト・スマート・キャッシュ
    2MB - 3MB - 4MB - 6MBの[L2キャッシュ](https://ja.wikipedia.org/wiki/L2キャッシュ "wikilink")は2つのコアで効率的に共有され、使用率は状況に応じて動的に変更される。従来は各コアごとにL2キャッシュを備えていたため、データの重複によるキャッシュ領域の無駄遣いが生じ、また[コヒーレンス制御](https://ja.wikipedia.org/wiki/コヒーレンス制御 "wikilink")にチップセットを経由する必要がありFSB帯域を無駄にしていた。コア間でL2キャッシュを共有することでより効率的なキャッシュ領域の使用ができ、またL2キャッシュのコヒーレンス制御がなくなるためFSB帯域が節約できるようになった。[L1キャッシュ](https://ja.wikipedia.org/wiki/L1キャッシュ "wikilink")のコヒーレンスもL2キャッシュ経由で行えるため極めて高速である。

  - インテル スマート・メモリー・アクセス
    メインメモリからの読み込みはL1キャッシュ・L2キャッシュの読み込みに比べて大変遅い。メインメモリにあるデータや命令のうち、予め必要となりそうなデータをキャッシュに取り込んで（[プリフェッチ](https://ja.wikipedia.org/wiki/プリフェッチ "wikilink")）おくことで、遅延を解消している。特にIPベースのプリフェッチャーをAMDに先がけて搭載しているのが特筆する点である。

    また、ロード命令が先行するストア命令に依存するかどうかを予測し、投機的にストア命令を追い越してロード命令を実行できる[Memory disambiguationをx](https://ja.wikipedia.org/wiki/:en:Memory_disambiguation "wikilink")86プロセッサとしては初めて実装している。

  - インテル アドバンスト・デジタル・メディア・ブースト
    YonahのMedia Boostを強化したもの。SSE演算器を128bit幅に拡大し、それまで128[ビット](../Page/ビット.md "wikilink")SSE命令は64bit単位のμOPが2つで処理されていたが、これを1μOPで処理可能にした。特に整数SIMD演算に関しては従来は64BitμOPを2つまで同時実行できたものが128bitμOPを2もしくは3つ同時実行できるようになったため、性能の向上は絶大であった。

  - インテル ワイド・ダイナミック・エグゼキューション

<!-- end list -->

  -
    Pentium Mを含むP6マイクロアーキテクチャにおいては、2シンプル+1コンプレックスの3デコーダ、3μOPs/clkのリネーム/リタイア、5つの命令発行ポートという構成が共通した仕様であった。Coreマイクロアーキテクチャにおいてはこれらを全て拡張し、3シンプル+1コンプレックスの4デコーダ、4μOPs/clkのリネーム/リタイア、6つの命令発行ポートという仕様になった。これによって、x86プロセッサ (内部[VLIW](https://ja.wikipedia.org/wiki/VLIW "wikilink")の[Transmeta](https://ja.wikipedia.org/wiki/Transmeta "wikilink")のプロセッサを除く) としては初めてクロックあたり4命令実行が持続可能なコアとなった。4つのデコーダは全てPentium Mで導入されたMicro-OPs Fusionをサポートしている他、連続する比較命令と条件分岐命令を1つのμOPとしてデコードするMacro Fusionが新たに導入された。このMacro Fusionが有効な場合の最大のデコード帯域は5 x86命令/clkとなる。命令発行ポートはALU/FPU/SIMD命令が発行可能なPort 5が新設され、3つの演算用ポート+3つのメモリアクセス用ポートという構成になった。
    [アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")のためのリソースも増加しており、P6マイクロアーキテクチャにおいては40エントリのリオーダ・バッファと20エントリのリザベーション・ステーションを備えていたが、それぞれ96エントリと32エントリに拡張されている。
  - Intel Intelligent Power Capability
    プロセッサの回路を細かく分割して管理し、使用されていない区画には電力を供給しないことで、消費電力を抑えている。
  - Intel Dynamic Acceleration
    他のコアがC3ステート以下の状態にある時、TDPの枠内でクロックを引き上げることでシングルスレッド性能を向上させる。

更に2007年7月27日のリリースでMerom（モバイル向け）特有の機能として以下の3つの技術が紹介された。

  - インテル ダイナミック・パワー・コーディネーション
    各コアをそれぞれ独立してスリープ（Cステート）させる機能。
  - インテル ダイナミック・バス・パーキング
    CPUと連動してチップセットの消費電力も減らす機能。
  - ダイナミック・キャッシュ・サイジング機能を備えた拡張版インテル ディーパー・スリープ
    キャッシュを利用しないことで、より消費電力を削減するスリープモード。

2007年3月28日に発表されたPenrynでは[プロセスルール](https://ja.wikipedia.org/wiki/プロセスルール "wikilink")の微細化による[リーク電流](https://ja.wikipedia.org/wiki/リーク電流 "wikilink")問題の解決のため、[トランジスタ](../Page/トランジスタ.md "wikilink")の[ゲート絶縁膜](https://ja.wikipedia.org/wiki/ゲート絶縁膜 "wikilink")にHigh-k（高誘電率ゲート絶縁膜材料）とメタルゲートを採用。プロセスルールも65nmから45nmに微細化され、さらなる消費電力低減と高クロック動作が可能となった。 L2キャッシュはダイ毎に最大で6MBに増加。デュアルダイ構成の場合は最大で12MBとなる。Meromに対し新たにSSE4と除算性能を約2倍に向上させるRadix-16 dividerの追加、[Intel VTの](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink")25～75％の性能向上が行われている。 また、Super Shuffle Engineによってシャッフルユニットが128Bit拡張されたことによりシャッフル/ パック/ アンパックなどの命令が1サイクルレイテンシーで実行できるようになった。これによってSSEユニットのフル128Bitを果たしたといえよう。

## 性能比較

Intelの前世代の主製品だったPentium 4 / [Pentium Dと](https://ja.wikipedia.org/wiki/Pentium_D "wikilink")、競合する[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[Athlon 64](https://ja.wikipedia.org/wiki/Athlon_64 "wikilink") / [Athlon 64 X2との間で](https://ja.wikipedia.org/wiki/Athlon_64_X2 "wikilink")、製品性能競争でつばぜり合いが行われていた。その為、Core 2が登場した時にも盛んにベンチマークテストが行われていた。  エンジニアリングサンプル品が幾つかのコンピューター関係プレス各社に配布され、プレス各社はベンチマークテストを行い、その結果を公表した。またAMDとIntelは[秋葉原](https://ja.wikipedia.org/wiki/秋葉原 "wikilink")にて互いに競合製品との比較を行うベンチマークテストのデモンストレーションを実施した。

  - Pentium 4との性能比較
    同じクロックのPentium 4に比べて圧倒的に高い性能を持つ事が明らかにされた。Merom New Instructions ([SSSE3](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSSE3 "wikilink")) をはじめとする、[ストリーミングSIMD拡張命令](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令 "wikilink")セットは極めて強力な能力がある事を示した。詳細はインテル アドバンスト・デジタル・メディア・ブーストの項を参照。

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink") [Category:X86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:X86アーキテクチャ "wikilink")