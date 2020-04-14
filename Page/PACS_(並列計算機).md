> この記事は[PACS \(並列計算機\)](https://ja.wikipedia.org/wiki/PACS_\(並列計算機\))から翻訳されています。


**PACS**（Processor Array for Continuum Simulation, パックス）及びPAXは、[1977年](../Page/1977年.md "wikilink")、当時[京都大学](../Page/京都大学.md "wikilink")[原子力](../Page/原子力.md "wikilink")研究所助教授であった[星野力に](https://ja.wikipedia.org/wiki/星野力_\(計算機科学\) "wikilink")、その頃普及し始めた[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を使ったアレイ型計算機の構築提案を[日立製作所](../Page/日立製作所.md "wikilink")の[川合敏雄](https://ja.wikipedia.org/wiki/川合敏雄 "wikilink")が行ったことがきっかけで開発が始まった、並列計算機である。

## 概要

当初の目的は、[原子炉](../Page/原子炉.md "wikilink")の炉心内における核熱水力現象を[シミュレートする炉心シミュレータの開発にあった](../Page/シミュレーション.md "wikilink")。このような処理は既存の一般的な汎用機でも可能であったが、開発主担当であった星野の回想によれば、[ILLIAC IVのような並列計算機を作ってみたいという夢から始まったものである](../Page/ILLIAC_IV.md "wikilink")。

具体的には、内部バスをそのままプロセッサ間通信用共有メモリへ接続し、自然の近接作用をそのままプロセッサ・アレイ上に投影する直接写像処理方式が、PACSの哲学であった。これは[フォン・ノイマン・ボトルネック](../Page/フォン・ノイマン・ボトルネック.md "wikilink")を解消するための最善の方法と考えられている。現在でも、いかにして内部バス幅を拡大し、メモリ-CPU間の通信帯域幅を保持するかという点について、継続して研究開発が進められている。

PACSシリーズそのものは、完全な専用計算機でなく、多目的汎用計算機となった。名称から推察できるように、[連続体](../Page/連続体力学.md "wikilink") (Continuum) のシミュレーションを主な応用とするが、隣接するCPU間を[トーラス](../Page/トーラス.md "wikilink")型[トポロジーで繋ぐ隣接結合](https://ja.wikipedia.org/wiki/ネットワーク構成 "wikilink")2次元トーラス型アーキテクチャ\[1\]を採用し、それ以外のアプリケーションにおいても高い性能を発揮した。近接作用を重視するアーキテクチャは、[IBM](../Page/IBM.md "wikilink")の[Blue Geneシリーズ等でも用いられている](../Page/Blue_Gene.md "wikilink")。

## 歴史

**表 PACSシリーズの系譜**

<table>
<thead>
<tr class="header">
<th><p>製作年</p></th>
<th><p>名称</p></th>
<th><p>理論演算性能</p></th>
<th><p>CPU数</p></th>
<th><p>CPU/FPU</p></th>
<th><p>使用OS</p></th>
<th><p>提供ベンダ</p></th>
<th><p>仕様作成元</p></th>
<th><p>研究補助</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/1978年" title="wikilink">1978年</a></p></td>
<td><p>PACS-9</p></td>
<td><p>7<a href="../Page/キロ.md" title="wikilink">K</a><a href="../Page/FLOPS.md" title="wikilink">FLOPS</a></p></td>
<td><p>9</p></td>
<td><p><a href="../Page/MC6800.md" title="wikilink">MC6800</a></p></td>
<td><p>－</p></td>
<td></td>
<td><p>京都大学　原子エネルギー研究所</p></td>
<td><p>校費</p></td>
<td><p>最初の試作機。ラッピング等で製作。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/1980年" title="wikilink">1980年</a></p></td>
<td><p>PAX-32</p></td>
<td><p>0.5<a href="../Page/メガ.md" title="wikilink">MFLOPS</a></p></td>
<td><p>32</p></td>
<td><p>MC6800/<a href="https://ja.wikipedia.org/wiki/AMD" title="wikilink">AM</a>9511</p></td>
<td><p>－</p></td>
<td></td>
<td><p>京都大学　原子エネルギー研究所</p></td>
<td><p>校費</p></td>
<td><p>32台のマイクロ<a href="../Page/プロセッサ.md" title="wikilink">プロセッサ</a>を搭載した最初の実用機。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/1983年" title="wikilink">1983年</a></p></td>
<td><p>PAX-128</p></td>
<td><p>4MFLOPS</p></td>
<td><p>128</p></td>
<td><p>MC68B00/AM9511-4</p></td>
<td><p>－</p></td>
<td></td>
<td><p>筑波大学　第3学群　星野研究室</p></td>
<td><p>校費・科研費</p></td>
<td><p>PACS-32のクロックを2倍に、台数を4倍にしたマシン。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/1984年.md" title="wikilink">1984年</a></p></td>
<td><p>PAX-32J</p></td>
<td><p>3MFLOPS</p></td>
<td><p>32</p></td>
<td><p><a href="../Page/ディジタル・イクイップメント・コーポレーション.md" title="wikilink">DCJ-11</a></p></td>
<td><p>－</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/三井造船" title="wikilink">三井造船</a></p></td>
<td><p>筑波大学　第3学群　星野研究室</p></td>
<td><p>科研費</p></td>
<td><p>製品型。<a href="https://ja.wikipedia.org/wiki/慶應義塾大学" title="wikilink">慶應義塾大学</a>と<a href="../Page/筑波大学.md" title="wikilink">筑波大学</a>での<a href="https://ja.wikipedia.org/wiki/並列プログラミング" title="wikilink">並列プログラミング</a>研究に生かされた。新技術開発事業団の委託で<a href="https://ja.wikipedia.org/wiki/三井造船" title="wikilink">三井造船</a>が開発した商用機「MiPAX」は<a href="https://ja.wikipedia.org/wiki/慶應義塾大学" title="wikilink">慶應義塾大学</a>等に納入された。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/1989年.md" title="wikilink">1989年</a></p></td>
<td><p>QCDPAX</p></td>
<td><p>14<a href="../Page/ギガ.md" title="wikilink">GFLOPS</a></p></td>
<td><p>480</p></td>
<td><p><a href="../Page/MC68020.md" title="wikilink">MC68020</a>/L64133</p></td>
<td><p>－</p></td>
<td><p><a href="../Page/アンリツ.md" title="wikilink">アンリツ</a></p></td>
<td><p>筑波大学　計算物理学研究センター</p></td>
<td><p><a href="../Page/文部科学省.md" title="wikilink">文部科学省</a>　科研費（特別推進）</p></td>
<td><p><a href="../Page/量子色力学.md" title="wikilink">量子色力学</a>専用計算機として開発。特に、格子<a href="https://ja.wikipedia.org/wiki/量子力学" title="wikilink">量子力学</a>計算に成果を残す。FPUとして<a href="https://ja.wikipedia.org/wiki/LSIコーポレーション" title="wikilink">LSIロジックのDSP</a>(L64133)を使用。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/1996年.md" title="wikilink">1996年</a></p></td>
<td><p>CP-PACS</p></td>
<td><p>614<a href="../Page/ギガ.md" title="wikilink">GFLOPS</a></p></td>
<td><p>2048</p></td>
<td><p><a href="../Page/PA-RISC.md" title="wikilink">PA-RISC</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/mach" title="wikilink">mach</a>3.0カーネル+<a href="https://ja.wikipedia.org/wiki/OSF/1" title="wikilink">OSF/1</a>(<a href="https://ja.wikipedia.org/wiki/HI-UX" title="wikilink">HI-UX</a>ベース)</p></td>
<td><p><a href="../Page/日立製作所.md" title="wikilink">日立製作所</a></p></td>
<td><p>筑波大学　計算物理学研究センター</p></td>
<td><p>文部科学省　研究助成費</p></td>
<td><p>CPは、Computational Physicsの略。<a href="https://ja.wikipedia.org/wiki/TOP500" title="wikilink">TOP500</a>において世界最高性能を記録（1996年11月）。商用機「<a href="https://ja.wikipedia.org/wiki/SR2201" title="wikilink">SR2201</a>」は<a href="https://ja.wikipedia.org/wiki/RWCP" title="wikilink">RWCP</a>, 東京大学等に納入された。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/2006年.md" title="wikilink">2006年</a></p></td>
<td><p>PACS-CS</p></td>
<td><p>14.3<a href="../Page/テラ.md" title="wikilink">TFLOPS</a></p></td>
<td><p>2560</p></td>
<td><p><a href="../Page/Xeon.md" title="wikilink">Xeon</a></p></td>
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a>/SCore</p></td>
<td><p><a href="../Page/日立製作所.md" title="wikilink">日立製作所</a><br />
<a href="../Page/日本電気.md" title="wikilink">NEC</a><br />
<a href="../Page/富士通.md" title="wikilink">富士通</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/筑波大学計算科学研究センター" title="wikilink">筑波大学計算科学研究センター</a></p></td>
<td><p>文部科学省　研究助成費</p></td>
<td><p>CSは、Computational Sciencesの略。 ハイパー<a href="https://ja.wikipedia.org/wiki/クロスバースイッチ" title="wikilink">クロスバー結合によるXeon</a><a href="../Page/コンピュータ・クラスター.md" title="wikilink">クラスター</a>。</p></td>
</tr>
</tbody>
</table>

PACSシリーズは、ユーザオリエンテッドな並列ソフトウエア研究開発の流れを作ったマシンとして、現在QCDPAXとCP-PACS、資料、日誌が[国立科学博物館](../Page/国立科学博物館.md "wikilink")に収蔵されている。

## 参考文献

  - T. Hoshino, T. Kawai, T. Shirakawa, J. Higashino, A. Yamaoka, H. Ito, T. Sato, and K. Sawada, PACS: a parallel microprocessor array for scientific calculations, ACM Transactions on Computer Systems, Volume 1 , Issue 3, pp. 195 - 221, 1983.
  - 星野力, 『PAXコンピュータ-高並列処理と科学計算』, オーム社, 1985年3月.
  - D. K. Kahaner, The Pax parallel computer, IEEE Micro, Volume 10, Issue 5, pp. 5-6, pp. 5-6, 91-3, 1990.

他

## 脚注

<references />

## 関連項目

  - [慶應義塾大学](https://ja.wikipedia.org/wiki/慶應義塾大学 "wikilink")
  - [筑波大学](../Page/筑波大学.md "wikilink")
  - [スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")

## 外部リンク

  - [筑波大学計算科学研究センター](http://www.ccs.tsukuba.ac.jp/ccs/)
  - [筑波大PACS](http://www1.accsnet.ne.jp/~hosinots/PACS-story.html)

[Category:計算科学](https://ja.wikipedia.org/wiki/Category:計算科学 "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink")

1.  隣接2次元トーラス型接続とは、隣接CPU間をトーラスバス（Blue Geneシリーズでは、[PowerPC](../Page/PowerPC.md "wikilink")に専用のポートを設けることによって実現）によって接続し、[パイプライン演算を効率良く行う仕組みのこと](../Page/パイプライン処理.md "wikilink")。具体的には、CPUの演算処理が終了すると、同時に隣接するCPUへ結果を受け渡すことによって、[SIMD](../Page/SIMD.md "wikilink")型の[ベクトルプロセッサを構築している](../Page/ベクトル計算機.md "wikilink")。[MIMD](../Page/MIMD.md "wikilink")型のアーキテクチャとしても利用可能。