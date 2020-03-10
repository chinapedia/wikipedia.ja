> この記事は[Intel 740](https://ja.wikipedia.org/wiki/Intel_740)から翻訳されています。


**Intel 740** (i740) は、1998年2月に発表された[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が初めて製品化したPC向けグラフィックスアクセラレータチップ\[1\]。Real3D社（[ロッキード・マーティン](../Page/ロッキード・マーティン.md "wikilink")社のグラフィック部門が分社化された会社）と共同開発された。

本製品は**Intel Graphics Technology** (IGT)のブランド名で展開され、[Intel 810](https://ja.wikipedia.org/wiki/Intel_810 "wikilink")/[815にも同様のコアが搭載された](https://ja.wikipedia.org/wiki/Intel_815 "wikilink")。その後は[Intel Extreme Graphicsに引き継いでいる](https://ja.wikipedia.org/wiki/Intel_Extreme_Graphics "wikilink")。

本項では、Intel 740の後継製品として発表された**Intel 752**についても取り扱う。

[thumb](https://ja.wikipedia.org/wiki/ファイル:i740.jpg "wikilink")

## 概要

### Intel 740

**Intel 740** (i740) は、インテルがReal3D社と共同開発した初のPC向け3Dグラフィックスアクセラレータチップである。開発コードネームは**Auburn**。

0.35μmプロセスルールで製造されるグラフィックスコアはパイプライン構成をとり、ビデオメモリは64bitのメモリバスで接続されたSDRAMまたはSGRAMを最大8MBまで対応する。またメインメモリをビデオメモリとして扱える**Direct Memory Execution**により小容量のVRAMしか搭載しない製品でも3D描画が可能である。ただし[MCなどの動画再生支援機能は搭載していない](https://ja.wikipedia.org/wiki/フレーム間予測 "wikilink")。

インターフェースは[AGP 2xにまで対応し](https://ja.wikipedia.org/wiki/AGP "wikilink")、外部トランスミッタを搭載することで[DVIなどのデジタル出力にも対応している](https://ja.wikipedia.org/wiki/Digital_Visual_Interface "wikilink")。サブピクセル単位でデータ補完を行えるPrecise-Pixel Interpolation の採用により高精度の映像表現が可能であるとしている。

これらの技術を採用したIntel 740のグラフィックスコアは**Intel Graphics Technology** (IGT) のブランドネームが与えられている。

### Intel 752

1999年4月に発表\[2\]された**Intel 752** (i752) は、i740以来のIGTファミリ第二世代製品である。開発コードネームは**Portola**。

基本的な部分はi740と共通であるが、MCによる動画再生支援機能を搭載している。またマザーボード上にオンボード搭載される用途を見越し、インテル アップグレーダブルAGPとして[オンボード](https://ja.wikipedia.org/wiki/オンボード "wikilink")搭載されたi752とAGP 4xスロットを共存させることも可能としている。

i752は実際には発売されないままキャンセルとなり、i752の後継製品として**Intel 754**が開発されているという噂も存在したが、i752のキャンセル以降[Larrabee](https://ja.wikipedia.org/wiki/Larrabee "wikilink")に至るまで、インテルは単体のグラフィックチップを手がけていない。

## IGTコア搭載チップセット

[thumb](https://ja.wikipedia.org/wiki/ファイル:Intel_82815_GMCH.jpg "wikilink")）\]\] i752・i754がともにキャンセルとなりインテルの単体グラフィックチップはi740を以って終了したが、IGTコア自体はその後もインテルのチップセットに統合される[オンボードグラフィック](https://ja.wikipedia.org/wiki/オンボードグラフィック "wikilink")コアとして採用された。IGTコアを搭載したチップセットには[Intel 810](https://ja.wikipedia.org/wiki/Intel_810 "wikilink")・[Intel 815が存在する](https://ja.wikipedia.org/wiki/Intel_815 "wikilink")。

これらチップセットに搭載されたIGTコアはi752コアをベースとしている。単体のグラフィックチップと異なり、フレームバッファとして専用のビデオメモリをサポートせず、メインメモリ領域の一部をビデオメモリとして利用する[UMA方式を採用している](https://ja.wikipedia.org/wiki/オンボードグラフィック#Unified_Memory_Archtechture "wikilink")。この為、性能的にはi752よりさらに劣り、さらに32bitカラーもサポートしなかったものの、一般的なオフィス・インターネット用途程度には十分な性能を有しており、安価かつ省スペースを実現できる為に広く採用された。 また性能向上技術として、Intel 810DCおよびIntel 815では[Zバッファ](https://ja.wikipedia.org/wiki/Zバッファ "wikilink")専用の[Display Cacheに対応している](https://ja.wikipedia.org/wiki/オンボードグラフィック#Display_Cache "wikilink")。

[Intel 830および](https://ja.wikipedia.org/wiki/Intel_830 "wikilink")[Intel 845G以降では後継の](https://ja.wikipedia.org/wiki/Intel_845 "wikilink")[Intel Extreme Graphicsコアが採用されている](https://ja.wikipedia.org/wiki/Intel_Extreme_Graphics "wikilink")。

## Intel 740の評価と影響

[thumb](https://ja.wikipedia.org/wiki/ファイル:Intel_i740_on_EP-BXT.JPG "wikilink") i740の発表当時、世界最大の半導体企業であるインテルがグラフィックチップ市場に参入するという点に注目が集まり、グラフィックチップベンダの淘汰・市場の再編成が進むのではないかという予想が多く見られた。

しかし実際に登場したIntel 740は同世代の他社製品を脅かすほどの性能を持たないだけでなく、当時対応が進みつつあった32ビットカラーにも対応していないなど機能的にも見劣りするものであった。さらに、AGPの普及を進めるインテルのAGP対応製品ということでAGPのリファレンス的存在となることも期待されていたが、実際にはインテル製チップセット以外では動作しないことも多かった。これらの様々な要因が積み重なり市場では廉価品の位置づけに留まり、後継製品であるi752も発表のみでキャンセルとなった。そのため、i740そのものは失敗作だったという評価が一般的になっている。

だがi752をベースとしたIGTコアを搭載した[Intel 810チップセットは市場で爆発的な成功を収め](https://ja.wikipedia.org/wiki/Intel_810 "wikilink")、結果的にはi740発表当時に予想されたように多くのグラフィックチップベンダのみならずチップセットベンダまで含めて淘汰と市場の再編へと結びついていくことになる。

## 脚注

## 関連項目

  - [Intel 810](https://ja.wikipedia.org/wiki/Intel_810 "wikilink")
  - [Intel 815](https://ja.wikipedia.org/wiki/Intel_815 "wikilink")
  - [Intel Extreme Graphics](https://ja.wikipedia.org/wiki/Intel_Extreme_Graphics "wikilink")
  - [Intel Graphics Media Accelerator](https://ja.wikipedia.org/wiki/Intel_Graphics_Media_Accelerator "wikilink")
  - [オンボードグラフィック](https://ja.wikipedia.org/wiki/オンボードグラフィック "wikilink")
  - [ビデオカード](../Page/ビデオカード.md "wikilink")

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:インテル](https://ja.wikipedia.org/wiki/Category:インテル "wikilink")

1.
2.