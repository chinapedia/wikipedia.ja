> この記事は[UNIVAC 1103](https://ja.wikipedia.org/wiki/UNIVAC_1103)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:UNIVAC-1103-BRL61-0905.jpg "wikilink") **UNIVAC 1103**（ユニバック1103）または **ERA 1103**は、[UNIVAC 1101の後継](../Page/UNIVAC_1101.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")である。[1953年](https://ja.wikipedia.org/wiki/1953年 "wikilink")10月、[Engineering Research Associates](https://ja.wikipedia.org/wiki/:en:Engineering_Research_Associates "wikilink") の設計の基に[レミントン・ランド](https://ja.wikipedia.org/wiki/レミントン・ランド "wikilink")社が製造した。[シーモア・クレイ](../Page/シーモア・クレイ.md "wikilink")が設計した最初のコンピュータである\[1\]。

## 歴史

*Atlas*（UNIVAC 1101）が完成する以前から、[海軍は](../Page/アメリカ海軍.md "wikilink") Engineering Research Associates にさらに高性能な[暗号解読](../Page/暗号解読.md "wikilink")用マシンの設計を依頼した。プロジェクト名は Task 29、コンピュータ名は *Atlas II*とされた。

[1952年](../Page/1952年.md "wikilink")、ERAは[NSAの前身である](../Page/アメリカ国家安全保障局.md "wikilink") Armed Forces Security Agency から *Atlas II*の商用化の承認を願い出た。特別な命令をいくつか削除するという条件で許可が得られた。この商用バージョンが UNIVAC 1103 となった。機密保持のため、レミントン・ランド経営陣にはこのマシンの来歴を知らせなかったという。

レミントン・ランドは[1953年](https://ja.wikipedia.org/wiki/1953年 "wikilink")2月に UNIVAC 1103 を発表した。科学技術計算市場で [IBM 701](https://ja.wikipedia.org/wiki/IBM_701 "wikilink") と競合した。1954年初め、[アメリカ統合参謀本部](../Page/アメリカ統合参謀本部.md "wikilink")の委員会が[数値予報](../Page/数値予報.md "wikilink")プロジェクトでどちらを採用するか判断するため、比較評価を要求した。評価してみると両者の計算性能はほぼ同等であり、IBMの方が入出力装置が高性能だったため満場一致でIBMが選ばれた\[2\]。

後継機種 UNIVAC 1103A （別名 *Univac Scientific*）は、不安定なウィリアムス管メモリを[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")に置き換え、浮動小数点演算命令をハードウェアに追加し、[割り込み機構を備えている](../Page/割り込み_\(コンピュータ\).md "wikilink")。

## 技術的詳細

UNIVAC 1103 は 1024ビットの[ウィリアムス管](https://ja.wikipedia.org/wiki/ウィリアムス管 "wikilink")メモリを36本使用しており、1024[ワード](../Page/ワード.md "wikilink")×36ビットの[RAMを備えている](../Page/Random_Access_Memory.md "wikilink")。36本のウィリアムス管はそれぞれ直径5インチ（約13cm）であったという。また[磁気ドラムメモリ](../Page/磁気ドラムメモリ.md "wikilink")は 16,384[ワード](../Page/ワード.md "wikilink")の容量を持つ。この静電メモリとドラムメモリには直接[アドレスが振られている](../Page/メモリアドレス.md "wikilink")。アドレス 0～01777（[八進数](../Page/八進法.md "wikilink")）には静電メモリが配置され、040000～077777（八進数）には磁気ドラムメモリが配置されている。

[固定小数点数](../Page/固定小数点数.md "wikilink")は 1ビットの符号と 35ビットの値からなり、負数は[1の補数形式で表現する](../Page/符号付数値表現.md "wikilink")。[命令は](../Page/命令セット.md "wikilink") 6ビットの命令コードと 15ビットのオペランドアドレスからなる。

プログラミング言語としてはいくつかの[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")（レミントン・ランド製の RECO、[Ramo-Wooldridge Corporation](../Page/TRW.md "wikilink") の RAWOOP）と、いくつかの[浮動小数点変換システム](../Page/浮動小数点数.md "wikilink")（Ramo-Wooldridge Corporation の SNAP、[Consolidated Vultee Aircraft](../Page/コンベア.md "wikilink") の FLIP、[ライト・パターソン空軍基地](https://ja.wikipedia.org/wiki/ライト・パターソン空軍基地 "wikilink")で開発された CHIP）があった。

## 1103A

後継の **UNIVAC 1103A** は1956年3月に登場した。最大の変更点は、磁気コアメモリの採用と[割り込み機能の追加である](../Page/割り込み_\(コンピュータ\).md "wikilink")\[3\] 。[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")は最大12,288ワード×36ビットを搭載可能で、4,096ワード×3バンク構成となっている。

[固定小数点数](../Page/固定小数点数.md "wikilink")は 1ビットの符号と 35ビットの値からなり、負数は[1の補数形式で表現する](../Page/符号付数値表現.md "wikilink")。[浮動小数点数](../Page/浮動小数点数.md "wikilink")は1ビットの符号、8ビットの指数、27ビットの仮数からなる。[命令は](../Page/命令セット.md "wikilink") 6ビットの命令コードと 15ビットのオペランドアドレスからなる。

1103Aは [IBM 704](../Page/IBM_704.md "wikilink") と競合した。どちらも真空管による論理回路、磁気コアメモリ、浮動小数点数のハードウェアサポートとなっている。

## 1104

UNIVAC 1104は、[ボマークミサイルプログラムで使用するために](../Page/ボマーク_\(ミサイル\).md "wikilink")、1957年に[ウェスティングハウス・エレクトリック](../Page/ウェスティングハウス・エレクトリック.md "wikilink")用に構築されたUNIVAC 1103の30ビット版である。しかし、1960年代にボマークが展開されるよりも前に、より新しいコンピューター（の改良版でG-40と呼ばれる）により置き換えられた\[4\]。

## 脚注

## 参考文献

  - Oral history interviews on ERA 1103, [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota. Interviewees include [William W. Butler](http://purl.umn.edu/107209); [Arnold A. Cohen](http://purl.umn.edu/107221); [William C. Norris](http://purl.umn.edu/107551); [Frank C. Mullaney](http://purl.umn.edu/107538); [Marvin L. Stein](http://purl.umn.edu/107639); and [James E. Thornton](http://purl.umn.edu/107673).

## 関連項目

  - [UNIVAC](../Page/UNIVAC.md "wikilink")
  - [計算機の歴史](https://ja.wikipedia.org/wiki/計算機の歴史 "wikilink")

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:真空管式コンピュータ](https://ja.wikipedia.org/wiki/Category:真空管式コンピュータ "wikilink") [Category:UNIVACのメインフレーム](https://ja.wikipedia.org/wiki/Category:UNIVACのメインフレーム "wikilink")

1.
2.  Emerson W. Pugh, Lyle R. Johnson, John H. Palmer, *IBM's 360 and early 370 systems*, MIT Press, 1991, ISBN 0-262-16123-0 pp. 23-34
3.  Rául Rojas, Ulf Hashagen *The first computers: history and architectures* MIT Press, 2002 ISBN 0-262-68137-4, page 198
4.