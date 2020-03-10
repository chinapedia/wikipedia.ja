> この記事は[ILLIAC IV](https://ja.wikipedia.org/wiki/ILLIAC_IV)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:ILLIAC_4_parallel_computer.jpg "wikilink") **ILLIAC IV**（イリアック・フォー）は、[イリノイ大学アーバナ・シャンペーン校](https://ja.wikipedia.org/wiki/イリノイ大学アーバナ・シャンペーン校 "wikilink")の一連の研究から生み出された最後の[コンピュータ](../Page/コンピュータ.md "wikilink")である。パターソン＆ヘネシーは本機を「間違いなく、スーパーコンピューター・プロジェクトの歴史上で最も不名誉なものであろう。」としている\[1\]。ILLIAC IV の設計の鍵は、256 プロセッサによる高い[並列性で](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")、後に[SIMD](https://ja.wikipedia.org/wiki/SIMD "wikilink")と呼ばれる、同時に多数のデータセットを処理することを指向していた。マシンは十年の開発期間を経て1975年に完全に稼働した。

## 背景

1960年代初頭、コンピュータの設計は[収穫逓減](https://ja.wikipedia.org/wiki/収穫逓減 "wikilink")の時期に差し掛かっていた。ハードウェアが直接実行する命令を増やせば性能が上がることは判っていたが、それにはコストがかかり過ぎるのである。実際、性能は電気信号の速度に限定されるため、ある速度を維持するには信号経路長が問題となり、ハードウェアを追加すると全体の速度は若干低下したのである。当時の[先端技術](https://ja.wikipedia.org/wiki/先端技術 "wikilink")である[トランジスタ](../Page/トランジスタ.md "wikilink")を使った論理回路設計では回路の増加はマシンのサイズの増加に直結していた。[CPU](../Page/CPU.md "wikilink")の速度は安定期に達しつつあったのである。

1960年代、それらの問題を解決する手法がいくつか研究された。当時オーバーラップ（*overlap*）と呼ばれた[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")は、ひとつの[CPU](../Page/CPU.md "wikilink")がいくつかの命令を同時に実行するものである。通常、CPUは命令をメモリからフェッチして、デコードして、実行し、結果をメモリに書き戻す。従来のCPUでは、たとえばデコードをしている最中にはCPUのその他の部分は全く働いていなかった。パイプラインは[シーモア・クレイ](https://ja.wikipedia.org/wiki/シーモア・クレイ "wikilink")が[CDC 6600で初めて実現した限界を破る手法であった](https://ja.wikipedia.org/wiki/CDC_6600 "wikilink")。そのマシンが登場したとき、他のマシンに対して約十倍の性能を発揮した。

別の解決方法は[並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")である。多数の汎用CPUを使ってコンピュータを構築する手法である。このタイプのコンピュータは各CPUが同時並行して動作して初めて効果を発揮する。そのためには処理を小さな部分に分割して並列に実行し、結果を集めて答えを出さなければならない。どんな問題でもこのような手法が使えるとは限らない。プログラムから並列性を引き出して並列実行することは現在でも問題として残っており、この並列コンピューティングという手法はCPUを追加しさえすれば性能が（理論的には無限に）向上するのが魅力である。汎用CPUは非常に高価であるため、[超並列](https://ja.wikipedia.org/wiki/超並列 "wikilink")マシンは非常に高価になるか、単純な設計のCPUを使用してコストを抑えるのが通例である。

[ウェスティングハウス・エレクトリック](https://ja.wikipedia.org/wiki/ウェスティングハウス・エレクトリック "wikilink")は後者の解決策を採用した**Solomon**プロジェクトを実施した。高性能を要求されているコンピュータは科学技術演算用途であることから、彼らはCPUの設計を数値演算の高速化に特化させた。"control unit" (CU)と呼ばれるひとつのメインCPUが命令の流れを処理し、単純な "processing element" (PE、現在で言うところの[実行ユニット](https://ja.wikipedia.org/wiki/実行ユニット "wikilink")) を複数配置して、演算を並行して実行するようにした。各PEは同じ命令をそれぞれ異なるデータに対して実行する。今日では[SIMD](https://ja.wikipedia.org/wiki/SIMD "wikilink")として知られている手法である。全体はCUが制御するマスタークロックにしたがって動作する。[アメリカ空軍](https://ja.wikipedia.org/wiki/アメリカ空軍 "wikilink")の[ローム研究所](https://ja.wikipedia.org/wiki/ローム研究所 "wikilink")(RADC)との契約により、[ブレッドボード](https://ja.wikipedia.org/wiki/ブレッドボード "wikilink")を使ったプロトタイプが 1964 年に製作されたが、RADCとの契約期間が終了するとウェスティングハウスは研究を打ち切った。

## 開発と運用

Solomonプロジェクトの研究者ダニエル・スロトニックは[イリノイ大学](../Page/イリノイ大学.md "wikilink")に移り、プロジェクトを続行した。1964年、イリノイ大学は[DARPAと契約を結び](../Page/国防高等研究計画局.md "wikilink")、ILLIAC IV の開発資金を得た。その名称はイリノイ大学でそれまで研究開発されたマシンの名称を受け継いだものである。[バロース](https://ja.wikipedia.org/wiki/バロース "wikilink")が共同開発に加わり、高速[ハードディスクシステムと装置自体の製作を担当した](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")。同社のメインフレーム Burroughs B6500 がフロントエンドとして使用されている。[テキサス・インスツルメンツ](https://ja.wikipedia.org/wiki/テキサス・インスツルメンツ "wikilink")社は様々な[ECL](../Page/エミッタ結合論理.md "wikilink") [集積回路](../Page/集積回路.md "wikilink")の開発を請け負い、ILLIACは ECL を全面的に採用した最初のマシンとなった。開発は1965年に開始され、第一段階の設計は1966年に完成している。

設計目標は毎秒10億命令を実行する性能を達成することであり、今風に言えば 1G[FLOPS](../Page/FLOPS.md "wikilink") である。これを達成するために 13MHzで動作する256個のPEを4つのCUで制御する構成が基本となっている。ILLIAC IV は 64ビット設計で、各PEには 2048ワードの 240ns [薄膜メモリ](https://ja.wikipedia.org/wiki/薄膜メモリ "wikilink")（後に[半導体](../Page/半導体.md "wikilink")メモリに置換された）が装備されている。PEは自身に接続されたメモリにのみアクセスできるのに対して、CUは全部のメモリにアクセスできた。この単純化によってPEのコストをさらに抑えている。各PEには6個の汎用[レジスタがあり](../Page/レジスタ_\(コンピュータ\).md "wikilink")、別途用意した特別なレジスタを周りの8個のPEと共有することができる。

もともとは、256個のPEをひとつの大きな筐体に入れることを想定していたが、プロジェクトはどんどん遅延し、64個のPEとひとつのCUをひとつの筐体に収めるように変更された。さらに、現実的な時間内では筐体ひとつ（64PE+1CU）を完成させるのがやっとであることが判明する。このため、達成可能な性能は 1GFLOPS から 200MFLOPS にダウンした。

大学で研究したことは、いかにしてデータをPEにばらまくかである。この問題（SIMD設計）を解決しなければ、ILLIAC IV の存在価値はない。これをなるべく容易にするためにいくつかの[プログラミング言語](../Page/プログラミング言語.md "wikilink")が開発された。IVTRAN と TRANQUIL は[FORTRAN](../Page/FORTRAN.md "wikilink")を並列化した言語であり、Glypnir は[ALGOL](../Page/ALGOL.md "wikilink")を並列化したものである。これらの言語は配列データをPEにばらまき、並列に処理をするもので、配列に対するループ処理を並列実行するように展開する機能を持つものもあった。

1960年代後半に製作が開始されたとき、大学と国防総省との関係が問題視され始め、抗議活動が始まった。1970年5月9日、"Illiaction" と呼ばれるこの日に抗議活動が頂点に達した。ウィスコンシン大学での[8月24日の爆破事件](http://www.leemark.com/featuredcontent/sterling/sterling.html)をきっかけとしてイリノイ大学は ILLIAC IV の開発をもっと安全な場所に移すことを決定した。これには[NASAが手を挙げた](../Page/アメリカ航空宇宙局.md "wikilink")。NASAは[アポロ後で金が余っていて](../Page/アポロ計画.md "wikilink")、様々な先端技術に興味を持っていた。NASAは新たにコンピュータ部門を立ち上げ、ILLIAC IV を[カリフォルニア州](../Page/カリフォルニア州.md "wikilink")の[エイムズ研究センター](https://ja.wikipedia.org/wiki/エイムズ研究センター "wikilink")に移した。

この移転でさらに開発は遅れて、1972年までに完成しなかった。この時点で1966年の当初予算 800万ドルは、性能目標が低下したにも関わらず 3100万ドルにまで膨れ上がっていた（この時点の性能目標はピークで 150MFLOPS、平均で 100MFLOPS 程度）。並列性の問題があってもその性能は当時の世界最高速であり、[CDC 7600の二倍から六倍である](https://ja.wikipedia.org/wiki/CDC_7600 "wikilink")。NASAから見れば、このマシンは[計算流体力学](https://ja.wikipedia.org/wiki/計算流体力学 "wikilink")に最適のアーキテクチャだった。

1972年に ILLIAC IV が動作したとき、非常に不安定でほとんど連続して使うことができなかった。信頼性向上の努力の結果、1974年に連続して動作しプログラムを最後まで動かすことができるようになり、1975年に完全動作するようになった。ただし「完全動作」といっても制限されたもので、使えるのは月曜から金曜までで、週に40時間のメンテナンスを必要とした。完全なアプリケーションが動作したのは1976年で、同じ年に[Cray-1](https://ja.wikipedia.org/wiki/Cray-1 "wikilink")がリリースされ、ほぼ同じ性能を発揮した。ILLIAC IV はその後数年間使われ、エイムズ研究センターでは独自のFORTRANコンパイラである　CFD を開発したりもしている。1982年、マシンはついに廃棄された。

## 影響

ILLIAC IV は良い結果を残せなかったが、何故うまくいかなかったのかを理解することで並列コンピューティングの研究が進んだ。それによって[シンキングマシンズ](../Page/シンキングマシンズ.md "wikilink")社の[CM-1 と CM-2](../Page/コネクションマシン.md "wikilink") のような超並列マシンの成功例が出てきたのである。

商用のスーパコンピュータは、ILLIAC IVの開発と同時期およびその後10年ほどは、複数の演算装置を並列化するのではなく、高速動作するパイプラインによりベクトル演算を行う[ベクトル計算機](../Page/ベクトル計算機.md "wikilink")として発達した。[CDC Star](https://ja.wikipedia.org/wiki/CDC_STAR-100 "wikilink")、TI ASC（[:en:TI Advanced Scientific Computer](https://ja.wikipedia.org/wiki/:en:TI_Advanced_Scientific_Computer "wikilink")）、そして有名な [Cray-1](https://ja.wikipedia.org/wiki/Cray-1 "wikilink") はベクトル型（パイプライン型）の高性能マシンである。

## 参照・脚注

<references/>

## 関連項目

  - [アムダールの法則](https://ja.wikipedia.org/wiki/アムダールの法則 "wikilink")
  - [ORDVAC](https://ja.wikipedia.org/wiki/ORDVAC "wikilink")
  - [ILLIAC I](https://ja.wikipedia.org/wiki/ILLIAC_I "wikilink")
  - [ILLIAC II](https://ja.wikipedia.org/wiki/ILLIAC_II "wikilink")
  - [ILLIAC III](https://ja.wikipedia.org/wiki/ILLIAC_III "wikilink")

## 外部リンク

すべて英文。

  - [The ILLIAC IV System 307](http://research.microsoft.com/users/GBell/Computer_Structures_Principles_and_Examples/csp0322.htm) – *Computer Structures Principles and Examples* (C. Gordon Bell 他)より
  - [ILLIAC IV CFD](http://www.hpjava.org/talks/beijing/hpf/introduction/node4.html)

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink")

1.  『コンピュータの構成と設計 第3版 別冊 歴史展望』p. 142