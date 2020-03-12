> この記事は[ETL Mark III](https://ja.wikipedia.org/wiki/ETL_Mark_III)から翻訳されています。


**ETL Mark III**は、1950年代に当時の電気試験所（電総研を経て現・[産総研](../Page/産業技術総合研究所.md "wikilink")）が開発した、日本初の[トランジスタ式コンピュータ](https://ja.wikipedia.org/wiki/トランジスタ式コンピュータ "wikilink")である。

## 歴史

### ETL Mark III

1954年、電気試験所に米国留学から帰国した和田弘 を部長とする電子部が創設された。1948年に発明された[トランジスタ](../Page/トランジスタ.md "wikilink")を研究する部門であったが、その中の回路技術研究室の[高橋茂](../Page/高橋茂.md "wikilink")、[西野博二](https://ja.wikipedia.org/wiki/西野博二 "wikilink")らは1955年からトランジスタによるコンピュータの開発に着手した。

当時はトランジスタ自体が開発初期の時代であり、使用するトランジスタ数を抑えるため、トランジスタ数の多くなる静的論理方式ではなく動的論理方式を採用した。また論理演算は[ダイオード](../Page/ダイオード.md "wikilink")論理で行い、トランジスタは増幅のみに使う[Diode-transistor logic](https://ja.wikipedia.org/wiki/Diode-transistor_logic "wikilink")（DTL）方式である。これは真空管式という違いはあるが[SEAC](../Page/SEAC.md "wikilink")と同様の方式である。また、研究試作ということで16ビットワードとし、除算回路も浮動小数点演算回路も持たない構成でトランジスタ数を減らした。[記憶装置](../Page/記憶装置.md "wikilink")としては、[水銀遅延線](https://ja.wikipedia.org/wiki/水銀遅延線 "wikilink")の扱いにくさを回避するため、光学ガラスを媒質とした遅延線メモリ（128ワード）を使用している。

1956年7月には動作するようになり、日本での電子計算機としては[FUJIC](../Page/FUJIC.md "wikilink")に次いで二番目、トランジスタ計算機としては日本初であった。世界的に見ても最初期のトランジスタ計算機である（[トランジスタ・コンピュータ\#その他の初期の装置](https://ja.wikipedia.org/wiki/トランジスタ・コンピュータ#その他の初期の装置 "wikilink")等を参照）。

### ETL Mark IV

Mark III は[点接触型トランジスタ](https://ja.wikipedia.org/wiki/点接触型トランジスタ "wikilink")を使用していて、動作は高速（加算時間は0.56ms）だったが、点接触型トランジスタの信頼性の低さに由来する故障が多かった。そこで、速度は犠牲になるが、信頼性を高めるために接合型トランジスタを使用した Mark IV の開発が始められた（すぐに接合型トランジスタの性能は向上したが、この時にはまだ接合型トランジスタは点接触型トランジスタより遅かった）。商用化を考慮し、事務用途で使われることを想定して、[BCDを基本方式としている](../Page/二進化十進表現.md "wikilink")。メモリアドレスまでBCD三桁で表現していた。メモリは、クロックが遅いため不利になる遅延式は止め、[磁気ドラムメモリ](../Page/磁気ドラムメモリ.md "wikilink")を使用した。機械部分は[ジャイロコンパス](https://ja.wikipedia.org/wiki/ジャイロコンパス "wikilink")で高速回転体の経験のある[北辰電機製作所](../Page/北辰電機製作所.md "wikilink")に、磁性体は[テープレコーダー](../Page/テープレコーダー.md "wikilink")の[東通工に開発させた](../Page/ソニー.md "wikilink")。容量は1000ワード（1ワードはBCD6桁、つまり24ビット）とした。[1957年](../Page/1957年.md "wikilink")11月に完成し、これをもとに電機メーカー各社が製品化している（後述）。また、Mark IV を利用した[機械翻訳](../Page/機械翻訳.md "wikilink")機「やまと」が開発された。その過程で[文字認識](https://ja.wikipedia.org/wiki/文字認識 "wikilink")装置も開発されている。

  - ETL Mark IVベースで製品化されたマシン

<!-- end list -->

  - [日本電気](../Page/日本電気.md "wikilink")
      - [NEAC](../Page/NEAC.md "wikilink")-2201 （[1958年](../Page/1958年.md "wikilink")）
      - NEAC-2202 （[1959年](../Page/1959年.md "wikilink")）
      - NEAC-2203 （1959年）
  - [日立製作所](../Page/日立製作所.md "wikilink")
      - [HITAC](../Page/HITAC.md "wikilink") 301 （1959年）
      - HITAC 501 （[1960年](../Page/1960年.md "wikilink")）
  - [松下通信工業](https://ja.wikipedia.org/wiki/松下通信工業 "wikilink")
      - MADIC-1 （1959年）

<!-- end list -->

  - 同機からの技術導入で製作されたマシン

<!-- end list -->

  - [北辰電機製作所](../Page/北辰電機製作所.md "wikilink")
      - HOC 100 （1958年）
      - HOC 200 （1960年）

### ETL Mark V以降

  - ETL Mark V
    電気試験所内の計算機需要が高まって、浮動小数点演算回路を持つマシンとして設計。製造は[日立製作所](../Page/日立製作所.md "wikilink")が担当し、[1960年](../Page/1960年.md "wikilink")5月に完成している。HITAC 102は、これをベースで製品化されたマシンである。
  - ETL Mark 4A
    さらに改良が続けられ、後に[第五世代コンピュータ](../Page/第五世代コンピュータ.md "wikilink")計画の中心となった[渕一博](https://ja.wikipedia.org/wiki/渕一博 "wikilink")が加わり、ワード長をBCD6桁から8桁に拡大し[インデックスレジスタ](https://ja.wikipedia.org/wiki/インデックスレジスタ "wikilink")を追加。さらに記憶装置を[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")にして[1959年](../Page/1959年.md "wikilink")開発され、性能が十倍になった。
  - ETL Mark 4B
    各種入出力装置を接続するための専用計算機として[1961年](https://ja.wikipedia.org/wiki/1961年 "wikilink")開発。Mark 4A と接続して[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")システムを構成している。
  - ETL Mark VI
    超大型コンピュータの研究のため、[1959年](../Page/1959年.md "wikilink")ごろから研究開始。この過程で様々な新方式を生み出し、後の日本のコンピュータ産業の礎となった。[1965年](../Page/1965年.md "wikilink")に完成し、電気試験所でのコンピュータ開発は役目を終えた。

### Mark I, II

[ETL_Mark_II.jpg](https://ja.wikipedia.org/wiki/File:ETL_Mark_II.jpg "fig:ETL_Mark_II.jpg")の展示。\]\] 数字としてはMark III以前にMark IとMark IIがあることになるが、ETL Mark IとMark IIはリレーを利用しており「電子」計算機ではない。リレーの特性のために非同期論理回路を採用するなど、Mark III以降とは繋がらない点も多い。

## 参考文献

  - 『国産コンピュータはこうして作られた』相磯秀夫(他編）、共立出版（1985年）、ISBN 4-320-02278-5

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:1950年代のコンピュータ](https://ja.wikipedia.org/wiki/Category:1950年代のコンピュータ "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink")