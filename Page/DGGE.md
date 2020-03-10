> この記事は[DGGE](https://ja.wikipedia.org/wiki/DGGE)から翻訳されています。


[16S_PCR_DGGE.jpg](https://ja.wikipedia.org/wiki/File:16S_PCR_DGGE.jpg "fig:16S_PCR_DGGE.jpg")で[染色したDGGE](https://ja.wikipedia.org/wiki/染色_\(生物学\) "wikilink")[ゲル](../Page/ゲル.md "wikilink")（ネガ像）\]\] **DGGE**とは(**D**enaturing **G**radient **G**el **E**lectrophoresis 変性剤濃度勾配ゲル電気泳動法)のこと。

この方法では、変性剤の濃度勾配があるゲルを用いて二本鎖[DNAを電気泳動する](../Page/デオキシリボ核酸.md "wikilink")。通常は[ポリアクリルアミド](https://ja.wikipedia.org/wiki/ポリアクリルアミド "wikilink")ゲルを用い、尿素とホルムアミドを変性剤として用いる。ゲル中に変性剤の濃度勾配があると、二本鎖DNAは分子量の違いだけではなく、変性しやすさの違いによってもバンドがあらわれる位置が異なるため、高い分離能が得られる。

変性したDNAはリン酸基の負荷電がバッファによって中和されて移動しにくくなるため、二本鎖DNAが変性する位置の近傍にバンドが現れる。しかし、この方法（原法）ではG-Cが豊富な二本鎖DNAのミスマッチを十分に検出できなかったため、 GC clamp（Sheffield et al., 1989）と呼ばれる40塩基程度のG-Cが豊富な（安定な）配列が[PCRの際に一方の](../Page/ポリメラーゼ連鎖反応.md "wikilink")[プライマー](https://ja.wikipedia.org/wiki/プライマー "wikilink")の5'側に付加される。この方法では、負荷電がclamp部分で維持されるため、分離能が向上し、よりG-Cが豊富で長いDNAを試料とすることができる。しかし、GC clampの付いたプライマーは60塩基程度となるため、通常のプライマーと比較して高価となる。

本来は、二本鎖[DNAの](../Page/デオキシリボ核酸.md "wikilink")[塩基配列](../Page/塩基配列.md "wikilink")の部分的な違いを比較的容易に検出する手法として、FisherとLerman(1983)によって提案された。しかし、分離能の高さから、微生物群集の解析（[メタゲノム](https://ja.wikipedia.org/wiki/メタゲノム "wikilink")解析）にも応用されている。環境中の微生物群集は多数の種を含み、その大部分が培養不可能であるため、培養することなく多数の微生物を一斉に検出するための重要な手法の一つとなっている。複雑な微生物群集の混合物を試料とした場合であっても、良好に分離したバンドから切り出された産物は[シークエンス](../Page/シークエンス.md "wikilink")反応に流用できる。しかし、複雑な微生物群集に由来するDNAをPCRで増幅すると、[キメラ](../Page/キメラ.md "wikilink")産物が生じたり、[DNAポリメラーゼ](../Page/DNAポリメラーゼ.md "wikilink")の増幅エラーによって間違った微生物種に帰属される可能性があるため、増幅エラーの少ない[φ29DNAポリメラーゼ](https://ja.wikipedia.org/wiki/φ29DNAポリメラーゼ "wikilink")による予備増幅、3'→5'校正活性のあるDNAポリメラーゼの使用、[S1ヌクレアーゼ](https://ja.wikipedia.org/wiki/S1ヌクレアーゼ "wikilink")による[heteroduplex](https://ja.wikipedia.org/wiki/heteroduplex "wikilink")の検出、キメラチェックプログラムによる配列の確認、などが併用されている。

## 手順

プライマーの設計：GC clampは通常最も開裂し易い領域に隣接するように、また増幅した100〜400bpsの配列中に開裂する領域が少なくても1つ、多くても2つの領域になるように設計する。

濃度勾配ゲルの作成：適当な変性剤濃度のグラジエントゲルを作成する。このとき、電気泳動の進行方向に向かって変性剤濃度が高くなるようにする。一定の温度に暖めたTAE中で15分程度プレランを行う。

電気泳動：サンプルをロード後、一定電圧で行う。分離能を高めるため、低電圧（50〜60V程度）で一晩泳動することが多い。

染色：[臭化エチジウム](../Page/臭化エチジウム.md "wikilink")だけではなく、より感度の高いSYBR GoldやSYBR Green Iなども用いられている。

バンドの切り出し：非常に密集した細いバンドになることが多いため、メスではなく滅菌したパスツールピペットやピペットチップが用いられることが多い。切り出したゲルからTAEバッファなどでDNAを溶出させ、PCRを行った後、シークエンシングに用いられる。バンドが十分に分離していることが期待できない場合には、[TAクローニング](https://ja.wikipedia.org/wiki/TAクローニング "wikilink")なども併用される。

## 変法

  - TGGE(Temperature Gradient Gel Electrophoresis　温度勾配ゲル電気泳動法)変性剤ではなく温度勾配を用いる。
  - CDGE(Constant Denaturant Gel Electrophoresis)勾配をつけない一定濃度の変性剤を用いて行う。既知の変異の有無を判定する簡便法。

[Category:電気泳動](https://ja.wikipedia.org/wiki/Category:電気泳動 "wikilink") [Category:分子生物学](https://ja.wikipedia.org/wiki/Category:分子生物学 "wikilink")