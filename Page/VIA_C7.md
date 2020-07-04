> この記事は[VIA C7](https://ja.wikipedia.org/wiki/VIA_C7)から翻訳されています。


[VIA_C7-D_Processer_1.5GHz_NanoBGA2.jpg](https://ja.wikipedia.org/wiki/File:VIA_C7-D_Processer_1.5GHz_NanoBGA2.jpg "fig:VIA_C7-D_Processer_1.5GHz_NanoBGA2.jpg") **VIA C7**（ヴィア　シー・セブン）は[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")[VIA Technologiesが販売する](../Page/VIA_Technologies.md "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換プロセッサである。同社[VIA C3の後継製品である](../Page/VIA_C3.md "wikilink")。

## 概要

**VIA C7**は2005年5月にVIA Technologiesが発表したx86互換プロセッサである。開発コードは**Esther (C5J)**。設計はCyrixIIIおよびC3同様、わずか100人足らずの技術者からなる旧[Centaurチームが担当した](https://ja.wikipedia.org/wiki/セントールテクノロジー "wikilink")。

従来の同社CPU同様、低価格・低消費電力・使用頻度の高いアプリケーションにフォーカスした性能設計となっており、トータル性能では競合他社製品に劣る面も多い。しかし省電力性については中国標準化認証センターから[省エネ認定](http://www.viatech.co.jp/jp/resources/pressroom/pressrelease.jsp?press_release_no=1407)を受けるなど評価がされており、**カーボンフリープロセッサ**として省エネ面でのアピールも行われている。

C7は[CPU](../Page/CPU.md "wikilink")単体では販売されず、主に21mm四方のNanoBGA2パッケージで[マザーボード](../Page/マザーボード.md "wikilink")に[オンボード](../Page/オンボード.md "wikilink")搭載された状態で販売されているが、VIA EPIA PNシリーズにおいて例外的にMicro PGA479パッケージのC7が搭載された。しかしこれは同マザーボードのオンボード扱いであり、他の[Socket 479対応マザーボードでの動作は想定されていない](https://ja.wikipedia.org/wiki/Socket_479 "wikilink")。

C7は公式には[2005年](../Page/2005年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")に出荷開始となっていたが、市場調査によると、量産品はその時には出荷していなかった。[2006年](../Page/2006年.md "wikilink")5月にVIAと[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")とのクロスライセンスの期限が切れたが更新されなかった。これは、2006年[5月31日](../Page/5月31日.md "wikilink")にはC3の出荷を終了しなければならなかったからである。またこれにより、VIAは[Socket 370に対する製品化の権利を失った](https://ja.wikipedia.org/wiki/Socket_370 "wikilink")。

### 設計方法論

競合他社は一般的にはトランジスタ増大による性能向上策を採用するが消費電力の増加も招く。一方、VIA/Centaurは同社の伝統であるバランスの取れたパフォーマンスを目指す手法をとった。

  - C3シリーズの設計哲学の基本は、もし効果的な「フロントエンド」すなわちプリフェッチやキャッシュ、分岐予測機構などを取り入れたならば、複雑な[スーパスカラやアウトオブオーダーを備えたコアに対して](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")、インオーダーのシンプルなコアの方がリーズナブルな性能がでる、というものだった。
  - [この記事](http://www.digit-life.com/articles2/cpu/rmma-via-c7.html)に書かれている通り、C7の場合、設計チームはより一層チップの「フロントエンド」、すなわち[プリフェッチ](../Page/プリフェッチ.md "wikilink")機構と同様にキャッシュのサイズやウェイ数、スループットに注力するようになった。

## 特徴

[VIAC7_1500B.jpg](https://ja.wikipedia.org/wiki/File:VIAC7_1500B.jpg "fig:VIAC7_1500B.jpg")

  - クロック周波数2GHzにして20W以下の低TDP。それに対して、インテルDothanコアの2.0GHz [Pentium Mでは](../Page/Pentium_M.md "wikilink")、21W (FSB 400MHz) ないし27W (FSB 533MHz) のTDPである。
  - L2キャッシュは64kBから128kBに増え、C3では16ウェイセットアソシエイティブだったのがC7では32ウェイセットアソシエイティブに増加。
  - VIAはC7バスは物理的にはPentium MのSocket479パッケージをベースとしているが、法的侵害を避けるためにIntelの[AGTL+](https://ja.wikipedia.org/wiki/GTL_%28デジタル回路%29 "wikilink") [Quad Pump式バスの代わりに独自の信号形式のVIA](../Page/P4バス.md "wikilink") V4バスを使用している、と[VIAは発表している](http://www.xbitlabs.com/news/mobile/display/20050518045045.html)。評論家たちは同じマザーボードにPentiumMとC7両方を挿すことができることに気づいた。これは報道によればVIAの[Flexi-Bus technology](http://www.viatech.co.jp/jp/products/chipsets/v-series/vn800/)によるもので、CPUを自動判別するものだとしている。
  - **Twin Turbo**テクノロジーは2つの[PLLから構成され](../Page/位相同期回路.md "wikilink")、一つが高速なクロックで動作し、もう一方が低速なクロックで動作している。これによりプロセッサのクロックをたった1クロックで調整できる。これはインテルの[SpeedStep テクノロジと比べて非常に速く](../Page/Intel_SpeedStep_テクノロジ.md "wikilink")、より高度な電力管理ができる。
  - 拡張命令である[SSE2とSSE](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE2 "wikilink")3をサポート。
  - [バッファオーバーフローの低減やウィルス攻撃に対する防御として](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")[NXビット](../Page/NXビット.md "wikilink")を導入。
  - [SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")とSHA-256のハードウェアレベルでサポート。
  - [公開鍵暗号](../Page/公開鍵暗号.md "wikilink")のために32k長までの鍵サイズをサポートする[モンゴメリ乗算](https://ja.wikipedia.org/wiki/モンゴメリ乗算 "wikilink")をハードウェアレベルでサポート。
  - [IBM](../Page/IBM.md "wikilink")[半導体](../Page/半導体.md "wikilink")部門によって開発された90nmの[SOI](../Page/SOI.md "wikilink")製造プロセスへの移行。

## バリエーション

販売されているC7には3つの主なバージョンがある。ただしこれらを総称し単にC7と呼称されることが多い。

<table>
<thead>
<tr class="header">
<th><p>種別</p></th>
<th><p>用途</p></th>
<th><p>クロック</p></th>
<th><p>FSB</p></th>
<th><p>パッケージ</p></th>
<th><p>省電力技術</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>C7<br />
C7 Eden</p></td>
<td><p>デスクトップPC・組込</p></td>
<td><p>533MHz-2.0GHz</p></td>
<td><p>400/533/800MHz</p></td>
<td><p>MicroPGA479<br />
NanoBGA2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>C7-D</p></td>
<td><p>デスクトップPC・組込</p></td>
<td><p>1.5-2.0GHz</p></td>
<td><p>400/533MHz</p></td>
<td><p>MicroPGA479<br />
NanoBGA2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>C7-M</p></td>
<td><p>ノートPC・組込</p></td>
<td><p>1.5-2.0GHz</p></td>
<td><p>400MHz</p></td>
<td><p>NanoBGA2</p></td>
<td><p>Enhanced PowerSaver</p></td>
</tr>
<tr class="even">
<td><p>C7-M ULV</p></td>
<td><p>ノートPC・組込</p></td>
<td><p>1.0-1.5GHz</p></td>
<td><p>400MHz</p></td>
<td><p>NanoBGA2</p></td>
<td><p>Enhanced PowerSaver</p></td>
</tr>
<tr class="odd">
<td><p>PV530</p></td>
<td><p>デスクトップPC・組込</p></td>
<td><p>1.8GHz+</p></td>
<td><p>800MHz</p></td>
<td><p>NanoBGA2</p></td>
<td><p>Enhanced PowerSaver</p></td>
</tr>
</tbody>
</table>

## 採用例

VIA C3同様、主にVIA社製[Mini-ITX](../Page/Mini-ITX.md "wikilink")[マザーボード](../Page/マザーボード.md "wikilink")にオンボード搭載されて組込市場で利用されている他、英国Evesham Technology、 Tranquil PCのカーボンフリーPC、米国Everex Systemsのノートパソコン、[OQO](../Page/OQO.md "wikilink") model 02や一部の[UMPC](https://ja.wikipedia.org/wiki/UMPC "wikilink")にも採用がされた。 さらに[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")には[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")がC7-Mを採用した**[HP2133](https://ja.wikipedia.org/wiki/HP2133 "wikilink")** Mini-NotePCを発表。VIA社プロセッサが大手PCメーカーの機種に採用された初の例となり、国内でも注目を集めた。

従来の同社CPUと比較し、着実にPC市場での存在感を高めている。

## 外部リンク

  - [VIA](http://www.viatech.co.jp/jp/index.jsp) - [VIAのプロセッサ](http://www.viatech.co.jp/jp/products/processors/)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")