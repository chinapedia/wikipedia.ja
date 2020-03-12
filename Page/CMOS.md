> この記事は[CMOS](https://ja.wikipedia.org/wiki/CMOS)から翻訳されています。


**CMOS**（シーモス、Complementary MOS; 相補型MOS）とは、P型とN型の[MOSFET](../Page/MOSFET.md "wikilink")を[ディジタル回路](https://ja.wikipedia.org/wiki/ディジタル回路 "wikilink")（[論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")）の論理ゲート等で相補的に利用する回路方式（論理方式）\[1\]、およびそのような電子回路やICのことである。また、そこから派生し多義的に多くの用例が観られる（『[\#その他の用例](https://ja.wikipedia.org/wiki/#その他の用例 "wikilink")』参照）。

## 原理

[thumb](https://ja.wikipedia.org/wiki/ファイル:CMOS_Inverter.svg "wikilink") p[チャネルとnチャネル](https://ja.wikipedia.org/wiki/電界効果トランジスタ#チャネル "wikilink") の[MOSFET](../Page/MOSFET.md "wikilink")を、相補的に利用する。

最も基本的な論理ゲートである[NOTゲート](https://ja.wikipedia.org/wiki/NOTゲート "wikilink")（論理反転）を右図に示す。この回路において、VddとVssは電源線（VddはVssに対して3〜15V程度の電位差を持つ）で、Aが入力信号線である。Vdd側（図中上側）がPMOS-FETでありVss側（図中下側）がNMOS-FETである。

AがVssと同じ電位を持つとき、上のFETがオンになり、下のFETがオフになる。このため、出力Qの電位はVddとほぼ等しくなる。また、AがVddと同じ電位を持つとき、上のFETがオフになり、下のFETがオンになる。このため、出力Qの電位はVssとほぼ等しくなる。つまり、Aと反対の電位がQに現れる事になる。

## 特徴

[thumbのCMOS回路構成](https://ja.wikipedia.org/wiki/ファイル:NAND_gate_\(CMOS_circuit\).PNG "wikilink")
<small>Q1,Q2はNMOS、Q3,Q4はPMOSのトランジスタで構成されている。</small>\]\] [thumbのCMOS回路構成](https://ja.wikipedia.org/wiki/ファイル:NOR_gate_\(CMOS_circuit\).PNG "wikilink")
<small>Q1,Q2はNMOS、Q3,Q4はPMOSのトランジスタで構成されている。</small>\]\]

[TTLや](../Page/Transistor-transistor_logic.md "wikilink")、NMOSやPMOSのように片方だけを利用する方式では、常に回路に電流が流れつづけるのに対し、CMOSでは論理が反転する際にMOSFETのゲートを飽和させる（あるいは飽和状態のゲートから電荷を引き抜く）ための電流しか流れないため、消費電力の少ない[論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")を実現できる。

さらに、[微細化](https://ja.wikipedia.org/wiki/微細化 "wikilink")することにより、単一のMOSFETをスイッチングさせるのに要する電力量を減少させることができる。これにより、集積度を向上させるだけで、高速化と消費電力の低減も同時に得られる（[デナード則](https://ja.wikipedia.org/wiki/ロバート・デナード "wikilink")。[ムーアの法則](../Page/ムーアの法則.md "wikilink")も参照）。電力消費の大半はスイッチングの際に行われるため、[回路設計](https://ja.wikipedia.org/wiki/回路設計 "wikilink")時にスイッチング回数を減らす工夫をすることでも、消費電力の削減ができる。

しかし、商用[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の生産に使われる最先端の集積回路プロセスでは、21世紀に入った頃から、微細化による漏れ電流の増加による非スイッチング時の消費電力の上昇により、前述の消費電力の低減がキャンセルされ、さらにはそちらの消費電力の上昇のほうが支配的になってしまっている（いわゆる「ムーアの法則の限界」として知られる現象のひとつ）。

過去には、CMOSはMOSFETのゲートを飽和させる状態まで電流を流しつづけなければスイッチングが行われないため、TTLやNMOSと比較し動作が遅いという弱点があった。しかし、微細化によるゲート容量の低下とVdd-Vssの低減、さらにはゲート誘電体の変更によってこの欠点は克服されている。

[TTLに比べて入力インピーダンスが非常に高いため](../Page/Transistor-transistor_logic.md "wikilink")、入力端子に[静電気](../Page/静電気.md "wikilink")が蓄積しやすい。また、MOSFETの構造自体が高電圧に対して非常にデリケート（入力ゲートの絶縁層が放電によって破壊されると回復不能となる）であるため、静電気による破損が起きやすい。そのため、通常、静電気による破損を防ぐためのクランプダイオードなどの保護回路が設けられているが、近年の[集積回路](../Page/集積回路.md "wikilink")の微細化によって、静電耐性の低下と静電保護対象の入力端子の増加が問題となっている。

MOSFETの動作領域における直流伝達特性は、線形領域における[出力](https://ja.wikipedia.org/wiki/出力 "wikilink")[電圧](../Page/電圧.md "wikilink")が[入力](../Page/入力.md "wikilink")電圧にほぼ等しいのに対して、[飽和](https://ja.wikipedia.org/wiki/飽和 "wikilink")領域における出力電圧はゲート電圧からVth「しきい値電圧」を引いた値となる。p-MOSFET が飽和領域のとき n-MOSFET は線形領域であり、n-MOSFET が飽和領域のとき p-MOSFET は線形領域であることより、CMOSの動作領域の殆どを線形領域とすることができる。

CMOS構造にすると、出力電圧範囲は電源電圧範囲に概ね等しくなる。入力信号の[しきい値](../Page/しきい値.md "wikilink")はHの時とLの時で対称となるので、[論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")設計が[負論理](https://ja.wikipedia.org/wiki/負論理 "wikilink")でも[正論理](https://ja.wikipedia.org/wiki/正論理 "wikilink")でも電気的な特性に違いがなくなり論理設計の自由度が増す。同時に、電源電圧（動作電圧）の許容範囲も広くなり電気的な設計をしやすくなる。

CMOSは、電源電圧を低くすると消費電力が少なくなる反面、伝達遅延時間が大きくなる性質を持つ。これは、単純な乗除算やせいぜい開平算を、人間のキー操作速度に合わせて行えば良く消費電力は抑えたい[電卓](../Page/電卓.md "wikilink")などにはもってこいである。一方でその動作の遅さが嫌われるような、たとえば過去には性能第一の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")や[メインフレーム](../Page/メインフレーム.md "wikilink")は[ECLが使われていた](../Page/エミッタ結合論理.md "wikilink")。しかし、拡大する[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")市場による後押しによって微細化が進み、低電圧動作と高速化の両立が図られたことと、集積度の向上や必要な冷却能力の緩和によるトータルコストの低下等の要因によって、コストパフォーマンス的にもECLを凌駕するようになり、今日ではメインフレーム、さらにはスーパーコンピュータ向け[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")市場でもCMOSが主流となっている。

また、同じような理由で[半導体メモリ](../Page/半導体メモリ.md "wikilink")などをはじめとするロジック[ICもほとんどがCMOS構造で製造されており](../Page/集積回路.md "wikilink")、近年は小容量[電源回路](../Page/電源回路.md "wikilink")・[アナログ-デジタル変換回路](../Page/アナログ-デジタル変換回路.md "wikilink")・[デジタル-アナログ変換回路](../Page/デジタル-アナログ変換回路.md "wikilink")などを含むものまで製作されるようになっている。

## 使用上の注意点

CMOS構造では、P型半導体とN型半導体が共存するので寄生素子（寄生[ダイオード](../Page/ダイオード.md "wikilink")・寄生[サイリスタ](../Page/サイリスタ.md "wikilink")など）が生じてしまう。このため、何らかの原因で[電源](../Page/電源.md "wikilink")電圧範囲を入力電圧が外れると、MOSFETがオンのままとなるラッチアップ現象が発生する。このため、一瞬でも電源電圧範囲を超える可能性がある入力端子には、[ダイオード](../Page/ダイオード.md "wikilink")などによる保護回路を設ける必要がある。なお、これらの保護回路を内蔵したICも存在する（入力トレラント機能)。

入力電圧をHとLの中間にすると、本来両方が同時にオン状態になってはいけない、電源側と接地側の両方のMOSFETがオンになってしまう（かもしれない。電源電圧とMOSFETのスレッショルドに依る）。これにより、最悪の場合電源が接地に[ショートした格好となり](../Page/短絡.md "wikilink")、大[電流](../Page/電流.md "wikilink")（貫通電流）が流れる。このとき発生する熱によって、自身が破損してしまうことも多い。このため、入力として使わない（論理的にはどこにも接続する必要がない）入力端子は、電位を不定にしてそのようなことを起こす可能性が無いように、HかLに固定して電位を安定させる必要がある。

## CMOS標準ロジックIC

[汎用ロジックIC](../Page/汎用ロジックIC.md "wikilink")（標準ロジックIC）の一群として、CMOSで実装されたICのシリーズがある。この節ではそれらについて説明する。初のシリーズ製品は1968年に[RCA](../Page/RCA.md "wikilink")から発売された4000シリーズ（CD4000シリーズ）\[2\]だが、既存の74シリーズをベースとしたピン配列などに互換性がある74HCシリーズがメジャーである。

4000シリーズは、基本的なゲート回路においてさえ既存のTTLの標準ロジックICとピン配置等が異なったものであるなど\[3\]、置換えを考慮した設計ではなかった。それでも、多くの会社から[セカンドソース](../Page/セカンドソース.md "wikilink")が売り出された\[4\]。4000シリーズの時代には、既にTTL標準ロジックICで設計された[基板が多数開発されていたことと](../Page/プリント基板.md "wikilink")、TTL標準ロジックICは量産による低価格化が進んでいたことから、CMOS標準ロジックICは低消費電力や許容幅の広い電源電圧などの、CMOSの特性が生かされる用途に使われるのみにとどまった。

しかし、互換ピン配置等、（電気的な設計にもよるが）TTLとの置き換えが可能な74HCシリーズ（74シリーズと互換性のある**H**igh Speed **C**MOSを表す）が出現し、さらに74HCT（High Speed CMOS TTL compatible)や74ACTのように入力信号の電位条件がTTL互換であり、TTLと直接接続できるタイプが出現するに至った。これによりCMOS標準ロジックは一気に普及し価格も下落したため、現在ではTTL標準ロジックICよりも多く用いられるようになった。

<table>
<caption>CMOS標準ロジックIC</caption>
<thead>
<tr class="header">
<th><p>シリーズ型名表示</p></th>
<th><p>電源電圧範囲<br />
(V)</p></th>
<th><p>遅延<br />
(ns)</p></th>
<th><p>静止時電流<br />
(μA/Gate)</p></th>
<th><p>特徴</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>4000</p></td>
<td><p>3 - 15</p></td>
<td><p>30</p></td>
<td><p>200</p></td>
<td><p><a href="../Page/RCA.md" title="wikilink">RCA</a>がオリジナルの標準品</p></td>
</tr>
<tr class="even">
<td><p>4500</p></td>
<td><p>3 - 15</p></td>
<td><p>30</p></td>
<td><p>200</p></td>
<td><p><a href="../Page/モトローラ.md" title="wikilink">モトローラ</a></p></td>
</tr>
<tr class="odd">
<td><p>74HC</p></td>
<td><p>2 - 6</p></td>
<td><p>10</p></td>
<td><p>23</p></td>
<td><p>74シリーズとピン配置互換</p></td>
</tr>
<tr class="even">
<td><p>74AC</p></td>
<td><p>2 - 5.5</p></td>
<td><p>8.5</p></td>
<td><p>40</p></td>
<td><p>HCを高速化したもの</p></td>
</tr>
<tr class="odd">
<td><p>74VHC</p></td>
<td><p>2 - 5.5</p></td>
<td><p>8.5</p></td>
<td><p>20</p></td>
<td><p>HCを高速化したもの</p></td>
</tr>
<tr class="even">
<td><p>74LVX</p></td>
<td><p>2 - 3.6</p></td>
<td><p>12</p></td>
<td><p>20</p></td>
<td><p>3.3V専用</p></td>
</tr>
<tr class="odd">
<td><p>74LCX</p></td>
<td><p>2 - 3.6</p></td>
<td><p>6.5</p></td>
<td><p>10</p></td>
<td><p>3.3V専用高速版</p></td>
</tr>
<tr class="even">
<td><p>74VCX</p></td>
<td><p>1.8 - 3.6</p></td>
<td><p>2.5</p></td>
<td><p>20</p></td>
<td><p>2.0V対応</p></td>
</tr>
</tbody>
</table>

### CMOS入出力レベル電圧 (V)

  - Hiレベル入力電圧 : 0.7×Vdd
  - Lowレベル入力電圧 : 0.2×Vdd
  - Hiレベル出力電圧 : Vdd-0.8
  - Lowレベル出力電圧 : 0.4

Vdd : 電源電圧（TTL回路の慣例に倣い、Vccと記述されることもある。）

## その他の用例

[固体撮像素子](../Page/固体撮像素子.md "wikilink")の一種である[CMOSイメージセンサ](../Page/CMOSイメージセンサ.md "wikilink")を単にCMOSと言う場合がある。固体撮像素子としては、従来はほぼ[CCDイメージセンサ](../Page/CCDイメージセンサ.md "wikilink")が使われてきたが、近年はCMOSイメージセンサも多用されつつある。

[パソコンや](../Page/パーソナルコンピュータ.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")などの利用者の間では、[BIOSの現在時刻やハードウェア設定情報などを保持するための不揮発性メモリ](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、またはそのメモリに保持されているデータそのものを指して、単にCMOSと呼ぶこともある。たとえば「[マザーボード](../Page/マザーボード.md "wikilink")が起動しなくなったときはCMOSをクリアする」などと使う（[不揮発性メモリ\#NVRAM](https://ja.wikipedia.org/wiki/不揮発性メモリ#NVRAM "wikilink")も参照）。

これは[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")の分野からの慣習で、[IBM PCシリーズではじめて](../Page/IBM_PC.md "wikilink")[リアルタイムクロック](../Page/リアルタイムクロック.md "wikilink")IC（RTC）が搭載された[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")の、[モトローラ](../Page/モトローラ.md "wikilink")製RTC ICであるMC146818に由来する。BIOSの設定は、このICの内蔵[SRAMに記憶していた](../Page/Static_Random_Access_Memory.md "wikilink")。このICは、電源切断時も[ボタン型電池](../Page/ボタン型電池.md "wikilink")などによる[バッテリーバックアップ](../Page/バッテリーバックアップ.md "wikilink")で動作し続けられるよう、消費電力を低減する必要があったため、時計や電卓などの極省電力機器以外では当時まだ珍しかったCMOSプロセスで製造されていたことから、MC146818自体がCMOSと呼ばれるようになった。さらにこれが転じてBIOSの情報を記憶するメモリのことをCMOSと呼ぶようになった。

## 関連項目

  - [CMOSイメージセンサ](../Page/CMOSイメージセンサ.md "wikilink")
  - [デジタル回路](../Page/デジタル回路.md "wikilink")

## 出典

<references />

[Category:半導体](https://ja.wikipedia.org/wiki/Category:半導体 "wikilink") [Category:ロジック・ファミリ](https://ja.wikipedia.org/wiki/Category:ロジック・ファミリ "wikilink")

1.  [TTLなどのデンで言うなら](../Page/Transistor-transistor_logic.md "wikilink")「CMOSL」という感じであろうか
2.  [1963-Complementary MOS Circuit Configuration is Invented](http://www.computerhistory.org/semiconductor/timeline.html#1960s)（英文）
3.  [科学用語の基礎知識 電子部品編 (NELECP)、CD4000 series](http://www.wdic.org/w/SCI/4000%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA)
4.  [CMOS IC 4000シリーズ、電子工作のページ](http://www.cypress.ne.jp/f-morita/parts/ic/cmos.html)