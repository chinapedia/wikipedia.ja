> この記事は[EDVAC](https://ja.wikipedia.org/wiki/EDVAC)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Edvac.jpg "wikilink") **EDVAC**（エドバック、の略称）は、最初期の[電子](../Page/電子工学.md "wikilink")[計算機](../Page/計算機.md "wikilink")（[コンピュータ](../Page/コンピュータ.md "wikilink")）の一つであった。その前身の[ENIAC](../Page/ENIAC.md "wikilink")とは異なり、十進数ではなく[二進数を使用しており](../Page/二進法.md "wikilink")、[プログラム内蔵方式](../Page/プログラム内蔵方式.md "wikilink")コンピュータとして設計された。

## 計画

[ENIAC](../Page/ENIAC.md "wikilink")を開発した[ジョン・モークリー](../Page/ジョン・モークリー.md "wikilink")と[ジョン・プレスパー・エッカート](../Page/ジョン・プレスパー・エッカート.md "wikilink")はENIACがまともに動作するようになる前の1944年8月、EDVACの設計と構築を提案した。その設計はENIAC構築中に考案された多くの重要なアーキテクチャ上または論理上の改良を取り入れるもので、高速な[遅延記憶装置](../Page/遅延記憶装置.md "wikilink")を採用することにしていた\[1\]。ENIACと同様、EDVACは[ペンシルベニア大学](../Page/ペンシルベニア大学.md "wikilink")が[米陸軍の](../Page/アメリカ陸軍.md "wikilink")[アバディーン実験場](https://ja.wikipedia.org/wiki/アバディーン実験場 "wikilink")にある[弾道研究所](https://ja.wikipedia.org/wiki/弾道研究所 "wikilink")のために製作した。エッカートとモークリーを含むENIAC設計者らはコンサルタントという立場の[ジョン・フォン・ノイマン](../Page/ジョン・フォン・ノイマン.md "wikilink")と合流して設計を開始した。1945年、フォン・ノイマンは論理設計について話し合った結果を 『[EDVACに関する報告書の第一草稿](https://ja.wikipedia.org/wiki/EDVACに関する報告書の第一草稿 "wikilink")』という報告書にまとめた\[2\]。

新しいコンピュータの開発契約は[1946年](../Page/1946年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")に結ばれ、当初予算は10万米[ドル](../Page/アメリカ合衆国ドル.md "wikilink")、コンピュータの名前はElectronic Discrete Variable Automatic *Calculator*とされた。EDVACに実際かかった費用はENIACとほぼ同額の50万米ドル弱であった。

## 仕様

開発されたコンピュータは二進数を使用し、加算、減算、乗算、プログラムによる除算などが可能で、メモリは[遅延記憶装置](../Page/遅延記憶装置.md "wikilink")で\[3\]1000ワード（後に1024ワードに拡張）であった（1ワードは44ビット）。

物理的には以下のような部品から構成されている。

  - [磁気テープ](../Page/磁気テープ.md "wikilink")読取/書込装置（Wilkes 1956:36\[4\] では、針金記録装置とされている）
  - [オシロスコープ](../Page/オシロスコープ.md "wikilink")付制御ユニット
  - メモリや制御部から命令を受け取って適切な装置に命令を伝える分配装置
  - ふたつの数値に対して演算を行いチェック後にメモリに格納する演算装置
  - タイマー
  - [水銀遅延管を](../Page/遅延記憶装置.md "wikilink")64本使用したメモリ装置2台（各水銀遅延管は8ワードを格納、また補助タンクが3つあってそれぞれ1ワード格納\[5\]）

加算にかかった時間は846マイクロ秒で乗算は2900マイクロ秒である。開発する上での重要な問題は信頼性と経済性であった。

物理的には約6,000本の[真空管](../Page/真空管.md "wikilink")と約12,000個の[ダイオード](../Page/ダイオード.md "wikilink")が使われていて、消費電力は56 [kWである](../Page/ワット.md "wikilink")。設置面積は45.5平方mで7,850 kgの重量だった。運用には30人が8時間[交代で張り付いていた](../Page/シフト勤務.md "wikilink")。

## 実装と運用

EDVACは[1949年](../Page/1949年.md "wikilink")[8月](../Page/8月.md "wikilink")に弾道研究所に運び込まれ、いくつかの問題に対処した後、[1951年](https://ja.wikipedia.org/wiki/1951年 "wikilink")に部分的に稼動した。完成までに時間がかかったのは、ペンシルベニア大学とエッカート&モークリーとの間で[特許](../Page/特許.md "wikilink")権を巡る争いがあったためと言われている。このためエッカートとモークリーは大学を離れ、[エッカート・モークリー・コンピュータ社を設立しEDVACに関わった技術者も引き抜いていった](https://ja.wikipedia.org/wiki/エッカート・モークリー・コンピュータ・コーポレーション "wikilink")。

[1960年](../Page/1960年.md "wikilink")には、EDVACは一日に20時間エラー無しで動作した。平均では一日8時間動作していたという。[1953年](https://ja.wikipedia.org/wiki/1953年 "wikilink")には[パンチカード](../Page/パンチカード.md "wikilink")装置を追加、[1954年](../Page/1954年.md "wikilink")には[磁気ドラムメモリ](../Page/磁気ドラムメモリ.md "wikilink")を外部記憶装置として追加し、[1958年](../Page/1958年.md "wikilink")には[浮動小数点演算装置が追加された](../Page/FPU.md "wikilink")。

EDVACは[1961年](https://ja.wikipedia.org/wiki/1961年 "wikilink")に[BRLESC](https://ja.wikipedia.org/wiki/BRLESC "wikilink")に置き換えられるまで動作した。それまでの実績をみると、当時としては非常に高い信頼性と生産性であったと言える。

## プログラム内蔵方式の功績は誰のものか

[プログラム内蔵方式](../Page/プログラム内蔵方式.md "wikilink")、いわゆる[ノイマン型](../Page/ノイマン型.md "wikilink")の着想は、主要メンバーの[ジョン・モークリー](../Page/ジョン・モークリー.md "wikilink")と[ジョン・プレスパー・エッカート](../Page/ジョン・プレスパー・エッカート.md "wikilink")が考案していたとされる。しかし、EDVAC開発チームの後から加わった[ジョン・フォン・ノイマン](../Page/ジョン・フォン・ノイマン.md "wikilink")の名前で広まってしまっており、今もノイマンの名で参照されることも多い（ただし、以下のような経緯からあえてその名を使わない研究者もいる）。

ENIACの主要開発メンバーであるモークリーとエッカートは技術面で優れており、開発メンバーのノイマンは理論的側面で優れていた。「ノイマン型」などと呼ばれる理由としては、有名な文献『EDVACに関する報告書の第一草稿』\[6\]の著者がノイマン単独となっていることと、当時のコンピュータ関連の他の多くの資料が[軍事機密](../Page/軍事機密.md "wikilink")であったのに対し、この文献は部外者への配布などが行われたという理由が大きい。これは、一流数学者の名前を利用してEDVACの名声をあげたい[ペンシルベニア大学](../Page/ペンシルベニア大学.md "wikilink")側の思惑があったともされる。モークリーとエッカートの開発メンバーからの離脱は、このことへの反発があるとされることもある。主要メンバーが離脱したEDVAC開発は大きく遅れ、世界初の実用的に稼働したプログラム内蔵方式コンピュータは1949年の[EDSAC](../Page/EDSAC.md "wikilink")となってしまった。EDVACは1951年になって完成する。

## 脚注

## 関連項目

  - [真空管式コンピュータ](../Page/真空管式コンピュータ.md "wikilink") - [真空管式コンピュータ一覧](../Page/真空管式コンピュータ一覧.md "wikilink")

## 外部リンク

  - [Oral history interview with J. Presper Eckert](http://conservancy.umn.edu/handle/107275), [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota.
  - [Oral history interview with Carl Chambers](http://conservancy.umn.edu/handle/107216), [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota.
  - [Oral history interview with Irven A. Travis](http://conservancy.umn.edu/handle/107688), [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota.
  - [Oral history interview with S. Reid Warren](http://conservancy.umn.edu/handle/107704), [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota.
  - [Oral history interview with Frances E. Holberton](http://conservancy.umn.edu/handle/107363), [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota.

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:1950年代のコンピュータ](https://ja.wikipedia.org/wiki/Category:1950年代のコンピュータ "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink") [Category:真空管式コンピュータ](https://ja.wikipedia.org/wiki/Category:真空管式コンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink")

1.
2.  ["First Draft of a Report on the EDVAC"](http://www.virtualtravelog.net/entries/2003-08-TheFirstDraft.pdf) ([PDF](../Page/Portable_Document_Format.md "wikilink")) by John von Neumann, Contract No.W-670-ORD-4926, 米陸軍兵站部とペンシルベニア大学との間の契約。ペンシルベニア大学電気工学科ムーア校、1945年6月30日。次の書籍にもある。
3.
4.
5.
6.