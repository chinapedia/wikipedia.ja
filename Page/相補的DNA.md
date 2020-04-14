> この記事は[相補的DNA](https://ja.wikipedia.org/wiki/相補的DNA)から翻訳されています。


**相補的DNA**（そうほてきDNA、complementary DNA）は、[mRNA](../Page/伝令RNA.md "wikilink") から[逆転写酵素](../Page/逆転写酵素.md "wikilink")を用いた逆転写反応によって合成された二本鎖 [DNA](../Page/デオキシリボ核酸.md "wikilink")。一般には「相補的」を意味する英語、complementary の頭文字をとって、**cDNA** と省略される。遺伝子の上でタンパク質に翻訳される領域の配列が開始コドンから終止コドンまで一続きに含まれているため、タンパク質の一次構造（アミノ酸配列）を解明する出発点として、また人工的にタンパク質を発現させる目的でも単離される。

ヒトを始めとする[真核生物](../Page/真核生物.md "wikilink")では、[遺伝子](https://ja.wikipedia.org/wiki/遺伝子 "wikilink")は[ゲノム](../Page/ゲノム.md "wikilink")上にコードされているものの、多くはそこから[転写](https://ja.wikipedia.org/wiki/転写 "wikilink")された [mRNA前駆体](https://ja.wikipedia.org/wiki/mRNA前駆体 "wikilink")が[スプライシング](https://ja.wikipedia.org/wiki/スプライシング "wikilink")を受けて[イントロン](../Page/イントロン.md "wikilink")が除去されるまでは[蛋白質](https://ja.wikipedia.org/wiki/蛋白質 "wikilink")に翻訳されない情報も含んでいる。 そこで、スプライシング済みの成熟[mRNA](https://ja.wikipedia.org/wiki/mRNA "wikilink") から cDNA を合成すればイントロンを含まない状態の遺伝子（塩基配列）を知ることができることから、遺伝子の[クローニング](../Page/クローニング.md "wikilink")に広く利用されている。

また、[mRNA](../Page/伝令RNA.md "wikilink") はスプライシング以外にも [RNAエディティング](https://ja.wikipedia.org/wiki/RNAエディティング "wikilink")という加工が起こるため、対応する[ゲノム](../Page/ゲノム.md "wikilink")DNA と cDNA の比較を行うことによって、エディティングサイトの特定が可能となる。

cDNA合成を逆転写酵素によって行ったのち、

1.  λ[ファージベクター](https://ja.wikipedia.org/wiki/ファージベクター "wikilink")や[プラスミド](../Page/プラスミド.md "wikilink")に[クローニング](../Page/クローニング.md "wikilink")し、[cDNAライブラリー](https://ja.wikipedia.org/wiki/cDNAライブラリー "wikilink")を作製。標識プロープや抗体などにより cDNA ライブラリーを[スクリーニングして](../Page/スクリーニング_\(生物学\).md "wikilink")、特定遺伝子の cDNA を単離する。
2.  [PCR法により](../Page/ポリメラーゼ連鎖反応.md "wikilink")、既知の塩基配列の情報をもとに、特定配列を増幅する（RT-PCRという）。それを直接解析するか、[プラスミド](../Page/プラスミド.md "wikilink")等にクローニングした後、解析を行う。この方法を工夫して、未知の 5'側配列、3'側配列を増幅するのに、RACE法（Rapid Amplification of cDNA end) と呼ばれる cDNA増幅法がある。
3.  [サブトラクション](https://ja.wikipedia.org/wiki/サブトラクション "wikilink")法などによって、未知であるが、遺伝子発現量に差がある cDNA のみを増幅し、それを単離する。

といった解析が行われる。

## cDNAの合成法

cDNA の合成には、(1) 全RNA（リボソームRNA、mRNAを含む）、または (2) polyA-RNA（mRNA）を鋳型とする方法がある。

また、[逆転写酵素](../Page/逆転写酵素.md "wikilink")の反応開始には、RNA上に反応の開始となる[プライマーを](../Page/プライマー_\(生物\).md "wikilink")[アニールさせ](../Page/ハイブリダイゼーション.md "wikilink")、3'から5’方向にcDNAを合成する必要がある。プライマーには、

1.  polyA構造を狙ったオリゴdTプライマーにより mRNA の 3'側から選択的に cDNA を作る。
2.  既知の cDNA配列に特異的な遺伝子特異的なプライマーを用いる。
3.  ランダムプライマー（通常、6塩基から8塩基程度の長さのものが使われる）を用いて、mRNA のすべての領域から cDNA合成を開始させる。

といった方法がある。

cDNAの合成に用いられる逆転写酵素の種類としては、AMV（トリmyeloblastosisウイルス）、あるいは MoMuLV（モロニーマウス白血病ウイルス）由来の[酵素](../Page/酵素.md "wikilink")が用いられることが多い。従来は、AMV由来の酵素が熱安定性が高かったため、mRNA の高次構造の存在を回避する手段として用いられていたが、近年、MoMuLV由来酵素の改良が進み、熱安定性の高い変異型酵素が市販されるようになったので、多くの研究者によって利用されている。なお、ある種の熱耐性型 DNAポリメラーゼ（[PCR](../Page/ポリメラーゼ連鎖反応.md "wikilink") に用いられる）には、RNA を鋳型としてDNAを合成する逆転写酵素活性を有するものがあり、それを利用する方法もある。

逆転写酵素反応は、mRNA が高次構造を取った場合に伸長しない。また、5'側から cDNA の相補鎖（mRNA と同じ方向をした DNA鎖）を作る際に、5'側にできるヘアピン構造を利用するため、本当の 5'末端が失われる。前者の解決法には、mRNA の熱変性や、上記に記載した高温度での逆転写反応が利用される。後者の解決法には、ピロリン酸ホスファターゼを利用した方法などがあり、[理化学研究所](https://ja.wikipedia.org/wiki/理化学研究所 "wikilink")の[完全長cDNA塩基配列決定プロジェクト](https://ja.wikipedia.org/wiki/完全長cDNA塩基配列決定プロジェクト "wikilink")で利用されている cDNAライブラリーは、このような方法で作製されたものである。

## EST

**EST** とは expressed sequence tag の略であり、遺伝子転写産物 (RNA) の一部（普通5'末端か3'末端）に当たる短い配列で、転写産物の“目印”として使われる。cDNAライブラリーからランダムに多数のクローンを選び、それから簡単なシークエンシングによって長さ 500 - 800[ヌクレオチド](https://ja.wikipedia.org/wiki/ヌクレオチド "wikilink")程度の配列を決定したものが EST であり、それらをまとめて[データベース](../Page/データベース.md "wikilink")を作製し利用する。まとめる方法としては [ESTクラスタリング](https://ja.wikipedia.org/wiki/ESTクラスタリング "wikilink")という手法が用いられる。特定の遺伝子の解析から断片的な配列が判明した場合、ESTデータベースからそれに対応する EST を探索し、これを手がかりにして段階的に RNA 全体の配列を得ることができる。現在は[ゲノムプロジェクト](../Page/ゲノムプロジェクト.md "wikilink")の補助的技術（あるいは ESTプロジェクト）として盛んに用いられている。また EST は [DNAマイクロアレイ](../Page/DNAマイクロアレイ.md "wikilink")用のプローブとして用いることもできる。最近では初めから完全長cDNA（RNA全長に相当する cDNA）を得て解析する技術も進歩しつつあるが、EST は依然として遺伝子解析における有用な技術である。

## FANTOM

Functional Annotation of Mouse for the RIKEN full-length cDNA clones

<http://fantom.gsc.riken.jp/jp/>

FANTOMは、理化学研究所のマウスゲノム百科事典プロジェクトで収集された完全長cDNAのアノテーション（機能注釈）を行うことを目的に、林崎良英博士が中心となり2000年に結成された国際研究コンソーシアムです。その役割はトランスクリプトーム解析の分野を軸に発展・拡大してきました。また、プロジェクトの研究対象は、ゲノムの転写産物という「要素」の理解から、転写制御ネットワークという「システム」つまり「生命体のシステム」の理解へ、より高次の階層に向けて着実に進められています。

## マイクロアレイ

GeneChips

## SAGE

遺伝子解析法 SAGE は(Serial Analysis of Gene Expression)から英語の[頭字語](../Page/頭字語.md "wikilink")をとった略称。遺伝子転写産物 (RNA) を逆転写した相補的DNA(cDNA)の一部(10-20bp)を識別用配列(5-10bp?)をはさんで直列に連結したものをDNAシーケンサーで読み取ることにより、多くの転写産物の発現量を調べることができる。相補的DNAの一部を網羅的にシーケンシングする手法としては、SAGE法を改良したSuperSAGE, オリゴキャップ法と併用したCAGE、MPSS, HiCEP等がある。

## 外部リンク

[The NCBI Handbook, Part 3, Chapter 21](http://www.ncbi.nlm.nih.gov/books/bv.fcgi?rid=handbook.section.858)

[Category:デオキシリボ核酸](https://ja.wikipedia.org/wiki/Category:デオキシリボ核酸 "wikilink")