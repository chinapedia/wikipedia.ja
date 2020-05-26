> この記事は[IASマシン](https://ja.wikipedia.org/wiki/IASマシン)から翻訳されています。


**IASマシン**とは、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[ニュージャージー州](../Page/ニュージャージー州.md "wikilink")の[プリンストン高等研究所](../Page/プリンストン高等研究所.md "wikilink")(IAS)が開発した初期の電子式[コンピュータ](../Page/コンピュータ.md "wikilink")である。IASマシンは1945年末ごろから開発が開始され、1951年稼動している\[1\]。いわゆる[ノイマン型](../Page/ノイマン型.md "wikilink")の最初期のコンピュータの一つである。また、本機と、他に複数作られた同構成のコンピュータ\[2\]を特に指してvon Neumann-architecture computersとすることがある。なお、ノイマン型の考案の功績はノイマン1人に帰すのは正しくない、とされている（[ノイマン型](../Page/ノイマン型.md "wikilink")の記事を参照）。

## 歴史

1946年5月、主任技術者としてが雇われた\[3\]。プロジェクト参加者としては他に、[ハーマン・ゴールドスタイン](https://ja.wikipedia.org/wiki/ハーマン・ゴールドスタイン "wikilink")、、[アーサー・バークス](https://ja.wikipedia.org/wiki/アーサー・バークス "wikilink")がいる\[4\]。マシンは1951年夏に部分稼動し、[1952年](../Page/1952年.md "wikilink")6月10日に完全稼動している。

1958年7月15日まで使用されていた\[5\]。

## 概要

このマシンは[二進コンピュータであり](../Page/二進法.md "wikilink")、ワード長は40ビットで、1ワードに20ビットの命令がふたつ格納される。メモリは1024ワード（5.1キロバイト）。負の整数は「[2の補数](../Page/2の補数.md "wikilink")」で表現されている。[レジスタは](../Page/レジスタ_\(コンピュータ\).md "wikilink")2本（アキュムレータ(AC)、乗除算用レジスタ(MQ)）。

重要な点として、IASマシンはプログラムとデータをひとつのメモリに混在させることを意図したほぼ最初の設計である。稼働したコンピュータとしては、実験的な機であるが[Small Scale Experimental Machine](https://ja.wikipedia.org/wiki/Manchester_Small-Scale_Experimental_Machine "wikilink") の1948年\[6\]、実用的なものと認められているものとしては[EDSAC](../Page/EDSAC.md "wikilink")の1949年が先行している。ノイマンが関与したコンピュータとしては[EDVAC](../Page/EDVAC.md "wikilink")の稼働はIASマシンと同時期であった。

[プログラム内蔵方式](../Page/プログラム内蔵方式.md "wikilink")により、ループを実現する方法が示された。ループの終了条件が成立したときに分岐命令を書きかえるというものなどである。当時の第一世代コンピュータではメモリを如何に節約するかが主題であり、命令を書きかえながら実行することでそれを実現していた。IASマシンの命令の[アドレッシングモード](../Page/アドレッシングモード.md "wikilink")には直接アドレッシングしかなく、例えば配列状に並んだデータそれぞれに同じ処理をする場合、命令の[オペランドを書き換えることでループを使った配列処理を実現していたのである](https://ja.wikipedia.org/wiki/被演算子 "wikilink")。

命令を書きかえることはプログラムの再利用性を損ない、可読性を下げる（[自己書き換えコード](../Page/自己書き換えコード.md "wikilink")参照）ので、すぐに[インデックスレジスタ](https://ja.wikipedia.org/wiki/インデックスレジスタ "wikilink")や、間接参照などのアドレッシングが発明され、このような技法は多用されるものではなくなった。

当初のデザインではメモリとして[RCA](../Page/RCA.md "wikilink")の[セレクトロン管](../Page/セレクトロン管.md "wikilink")という[真空管](../Page/真空管.md "wikilink")を使おうとしていたが、非常に複雑な真空管であるために開発が遅れ、[ウィリアムス管](https://ja.wikipedia.org/wiki/ウィリアムス管 "wikilink")を代替として使用することになった。全体としては約2300本の真空管を使っている。加算には 62マイクロ秒、乗算には 713マイクロ秒かかった。[非同期マシンであり](https://ja.wikipedia.org/wiki/非同期回路 "wikilink")、命令のタイミングを規定するクロックは存在しない。前の命令が完了したら次の命令をスタートさせるようになっている。

## IASマシンからの派生

IASマシンの設計に関する論文は世界中に流布された。その結果IASマシンと同じ構成のコンピュータが世界中で開発されたのである\[7\]。

IASマシンの派生の例：

  - \- 1953年1月、アメリカ [アルゴンヌ国立研究所](../Page/アルゴンヌ国立研究所.md "wikilink")

  - [BESK](../Page/BESK.md "wikilink") - 1953年、ストックホルム

  - [BESM](https://ja.wikipedia.org/wiki/BESM "wikilink") - 1953年、モスクワ\[8\]

  - \- 1959年、[アイオワ州立大学](../Page/アイオワ州立大学.md "wikilink")

  - [ILLIAC I](../Page/ILLIAC_I.md "wikilink") - 1952年、[イリノイ大学アーバナ・シャンペーン校](../Page/イリノイ大学アーバナ・シャンペーン校.md "wikilink")

      - [MUSASINO-1](../Page/MUSASINO-1.md "wikilink") - 1957年、[日本電信電話公社](../Page/日本電信電話公社.md "wikilink")

  - \- 1957年、[アルゴンヌ国立研究所](../Page/アルゴンヌ国立研究所.md "wikilink")

  - \- 1953年、[ランド研究所](../Page/ランド研究所.md "wikilink")

  - \- 1952年、[ロスアラモス国立研究所](../Page/ロスアラモス国立研究所.md "wikilink")

  - \- 1957年、[ミシガン州立大学](../Page/ミシガン州立大学.md "wikilink")

  - \- 1961年?、アメリカ [オークリッジ国立研究所](../Page/オークリッジ国立研究所.md "wikilink")

  - [ORDVAC](../Page/ORDVAC.md "wikilink") - 1951年、米陸軍 [アバディーン性能試験場](../Page/アバディーン性能試験場.md "wikilink")

  - [SARA](https://ja.wikipedia.org/wiki/SARA_\(コンピュータ\) "wikilink") - 1956年、[スウェーデン](https://ja.wikipedia.org/wiki/スウェーデン "wikilink") [SAAB](../Page/SAAB.md "wikilink")

  - [SILLIAC](https://ja.wikipedia.org/wiki/SILLIAC "wikilink") - 1956年、[オーストラリア](../Page/オーストラリア.md "wikilink") [シドニー大学](../Page/シドニー大学.md "wikilink")

  - \- 19??年、[スウェーデン](https://ja.wikipedia.org/wiki/スウェーデン "wikilink") [ルンド大学](../Page/ルンド大学.md "wikilink")

  - \- 1955年、[イスラエル](../Page/イスラエル.md "wikilink") [ワイツマン科学研究所](../Page/ワイツマン科学研究所.md "wikilink")

## 脚注

## 参考文献

  - Gilchrist, Bruce, ["Remembering Some Early Computers, 1948-1960"](http://web.archive.org/web/20061212200023/http://www.columbia.edu/cu/epic/gilchrist_3.07.06.pdf), *Columbia University EPIC*, 2006, pp.7-9. (archived 2006) Contains some autobiographical material on Gilchrist's use of the IAS computer beginning in 1952.

## 関連項目

  - [ノイマン型](../Page/ノイマン型.md "wikilink")

## 外部リンク

  - [チャールズ・バベッジ研究所](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink")（ミネソタ大学）にあるIASマシン関連のインタビュー記録

      - [Willis H. Ware](http://purl.umn.edu/107699)
      - [Arthur Burks](http://purl.umn.edu/107206)
      - [Herman Goldstine](http://purl.umn.edu/107333)
      - [Martin Schwarzschild](http://purl.umn.edu/107629)

  -
  - [First Draft of a Report on the EDVAC](http://cva.stanford.edu/classes/cs99s/papers/vonneumann-firstdraftedvac.pdf) - by [John Von Neumann](../Page/ジョン・フォン・ノイマン.md "wikilink")

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:真空管式コンピュータ](https://ja.wikipedia.org/wiki/Category:真空管式コンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.