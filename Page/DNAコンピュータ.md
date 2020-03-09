> この記事は[DNA](https://ja.wikipedia.org/wiki/DNA)から翻訳されています。


**DNAコンピュータ**（ディーエヌエーコンピュータ）の記事では、DNAコンピューティングについて記述する。2018年現在ではまだ「コンピュータ」とはっきり言えるほどに形のあるものではなく、いかにして計算をおこなうか、といったことの研究段階にあり、（英語版の記事名が DNA computing であることからも明らかなように）日本語版のこの記事の記事名は不適当である。4種類の[塩基](../Page/塩基.md "wikilink")の配列から成る[デオキシリボ核酸](../Page/デオキシリボ核酸.md "wikilink") (DNA) を利用して[コンピューティング](https://ja.wikipedia.org/wiki/コンピューティング "wikilink")をおこなうものである。

## 概要

[デオキシリボ核酸](../Page/デオキシリボ核酸.md "wikilink")（DNA）の、アデニン (A) とチミン (T)、グアニン (G) とシトシン (C) が対をなして結合する特性と、DNA鎖を操作する[酵素](../Page/酵素.md "wikilink")（様々な[制限酵素](https://ja.wikipedia.org/wiki/制限酵素 "wikilink")や、[DNAリガーゼ](https://ja.wikipedia.org/wiki/DNAリガーゼ "wikilink")、[DNAポリメラーゼ](../Page/DNAポリメラーゼ.md "wikilink")）を利用する。解答候補となる多数のDNA鎖を同時に生成するという意味で一種の[超並列計算をする系である](../Page/超並列マシン.md "wikilink")、と見る向きもある。

2000年前後に広まった研究のきっかけとなった論文は、[南カリフォルニア大学](https://ja.wikipedia.org/wiki/南カリフォルニア大学 "wikilink")のコンピューター科学者で、[RSA暗号](../Page/RSA暗号.md "wikilink")の「A」として知られる[レオナルド・エーデルマン](../Page/レオナルド・エーデルマン.md "wikilink")によるものである。彼は[ジェームズ・ワトソン](https://ja.wikipedia.org/wiki/ジェームズ・ワトソン "wikilink")の『遺伝子の分子生物学』を読んでいて[DNAによるコンピューティングの可能性に気付いたと言われている](../Page/デオキシリボ核酸.md "wikilink")。エーデルマンは1994年に初めてDNA鎖を用いて、[NP完全な問題の](../Page/NP完全問題.md "wikilink")1例としてよく知られている「[ハミルトン路問題](https://ja.wikipedia.org/wiki/ハミルトン閉路問題 "wikilink")」を解いた。ハミルトン路問題は一筆書きの一種\[1\]であり、グラフ上のすべてのノードを1回ずつ通るような路（パス）が存在するかどうか、存在する場合は具体的な解を示せ、という問題である。エーデルマンの実験ではノード7、パス14という規模だった。問題を21本 (7+14) のDNA鎖に翻訳し、解を示した。

2018年現在、いくつかの問題点も指摘されている。そのうちのひとつに、解を取り出す[アウトプット](https://ja.wikipedia.org/wiki/アウトプット "wikilink")がボトルネックとなっている、という点がある。たとえば、エーデルマンの実験では演算自体は数秒で終了したが、解を取り出すのに2日間を要している。これは以下のような操作を手動で進めたためだった。まず、開始ノードで始まり、終了ノードで終わるDNA鎖を[PCR](../Page/ポリメラーゼ連鎖反応.md "wikilink") (polymerase chain reaction) 法で増幅する。次に、解として適切な長さを持つDNA鎖（エーデルマン実験では6）を[電気泳動](../Page/電気泳動.md "wikilink")で分離する。最後に、全ての点を経由しているDNA鎖を鉄粉と結合した特殊な相補DNA鎖と混合し、ノードの数だけ精製を繰り返した。つまり、DNAコンピュータは演算は速いのだが、問題をDNA鎖の形に翻訳（入力）し、解をデジタルデータの形に変換する（出力）工程に問題がある。

また、複雑な問題をやらせようとすると、必要なDNAの量が指数関数的に増加するという問題もある。

その後、電子コンピュータとDNA反応装置を組み合わせて[プログラミング可能にした汎用型コンピュータも試作され](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、[2002年](../Page/2002年.md "wikilink")には[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")の陶山らと[オリンパス](https://ja.wikipedia.org/wiki/オリンパス "wikilink")が実用タイプの装置を共同で開発した。また[イスラエル](../Page/イスラエル.md "wikilink")・ワイツマン研究所のシャピロらはDNAや酵素の分子だけからなる分子コンピュータを現在開発中で、医学的応用を目指している。

## 本文注釈

## 参考文献

  - L. Adleman, *“Molecular Computation of Solutions to Combinatorial Problems,”* Science, vol. 266, pp. 1021–1024, Nov. 11, 1994.

## 関連項目

  - [ニューロコンピュータ](https://ja.wikipedia.org/wiki/ニューロコンピュータ "wikilink")
  - [量子コンピュータ](https://ja.wikipedia.org/wiki/量子コンピュータ "wikilink")
  - [生体コンピュータ](https://ja.wikipedia.org/wiki/生体コンピュータ "wikilink")
  - [分子コンピュータ](https://ja.wikipedia.org/wiki/分子コンピュータ "wikilink")

[Category:コンピュータ](https://ja.wikipedia.org/wiki/Category:コンピュータ "wikilink") [Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink") [Category:コンピュータの形態](https://ja.wikipedia.org/wiki/Category:コンピュータの形態 "wikilink") [Category:デオキシリボ核酸](https://ja.wikipedia.org/wiki/Category:デオキシリボ核酸 "wikilink")

1.  「一筆書き」とはすべてのエッジを1回ずつ通るような路のことなので、ハミルトン路は正確にはその「一種」ではない。