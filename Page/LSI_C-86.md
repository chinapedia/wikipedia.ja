> この記事は[LSI C-86](https://ja.wikipedia.org/wiki/LSI_C-86)から翻訳されています。


**LSI C-86** とはエル・エス・アイ・ジャパン株式会社が提供する16[ビット](../Page/ビット.md "wikilink")[C](../Page/C言語.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")である。最新バージョンは 3.5.9である。

## 概要

LSI C-86 はエル・エス・アイ・ジャパン株式会社が[1988年](../Page/1988年.md "wikilink")に16ビット[CPU](../Page/CPU.md "wikilink")用の[クロスコンパイラ](https://ja.wikipedia.org/wiki/クロスコンパイラ "wikilink")として開発した。同社の[Intel 8080](../Page/Intel_8080.md "wikilink")/[Z80](../Page/Z80.md "wikilink")用コンパイラである LSI C-80 の兄弟版にあたる。[C89に準拠している](https://ja.wikipedia.org/wiki/C言語#C89 "wikilink")。ただし、C89 のうち、locale.h は未実装。また、[ワイド文字](../Page/ワイド文字.md "wikilink")などC89以降（ISO/IEC 9899/AMD1:1995 など）に[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")に追加になった機能は未実装。

サポートしているCPUは[Intel 8086](../Page/Intel_8086.md "wikilink")（およびコプロセッサ[Intel 8087](../Page/Intel_8087.md "wikilink")）で、[OSは](../Page/オペレーティングシステム.md "wikilink")、[Windowsの他に](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Solaris](../Page/Solaris.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")等に対応している。MS-DOS版は[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[2月19日](../Page/2月19日.md "wikilink")に販売終了。ただし、後述する試食版は MS-DOS版のみである。

コンパイラとしては特に[メモリや](../Page/主記憶装置.md "wikilink")[レジスタの割り当てに重点が置かれている](../Page/レジスタ_\(コンピュータ\).md "wikilink")。例えば当時の8086用のCコンパイラの多くは[変数に割り当てられるレジスタは](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")2つか3つしかなかったのに対し、LSI C-86では宣言される変数の生存期間を調べ全てのレジスタに対して可能な限りの最適な割り当てを行う。また 8086シリーズの特徴の一つでもある4つのメモリモデルを全てサポートしている。

8086用コンパイラとしては珍しく、デフォルトの[呼出規約](https://ja.wikipedia.org/wiki/呼出規約 "wikilink")において、可変長引数でない関数の引数についてレジスタ渡しを採用している。

商用ソフトだが、Ver 3.30のMS-DOS版ベースで[フリーウェア](../Page/フリーウェア.md "wikilink")扱いのサブセット「**試食版**」があり、[パソコン通信](../Page/パソコン通信.md "wikilink")や[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")、あるいは雑誌『[C MAGAZINE](https://ja.wikipedia.org/wiki/C_MAGAZINE "wikilink")』（[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")に休刊）の付録[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")や[CD-ROM](../Page/CD-ROM.md "wikilink")に収録されるというかたちで配布された。ライセンスとして、生成物はフリーウェアにしなければならない。スモールモデル（コード・データそれぞれ64[KB以内](https://ja.wikipedia.org/wiki/キロバイト "wikilink")）のみ対応、[デバッグ](../Page/デバッグ.md "wikilink")機能やROM化機能が削除されているなどの機能制限がある一方、マニュアルは添付されていた。

## 外部リンク

  - [LSI C-86 ver 3.5](https://www.lsi-j.co.jp/official/products/02/other/lsic86)
  - [エル・エス・アイ・ジャパン株式会社フリーソフトウェア集](http://www.lsi-j.co.jp/freesoft/index.html)

[Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink")