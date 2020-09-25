> この記事は[Dpi](https://ja.wikipedia.org/wiki/Dpi)から翻訳されています。


**dpi**（ディーピーアイ、**DPI**とも表記）とは、の略で、[ドット密度](https://ja.wikipedia.org/wiki/ドット密度 "wikilink")の[単位](../Page/単位.md "wikilink")である。1[インチ](../Page/インチ.md "wikilink")（1[平方インチ](../Page/平方インチ.md "wikilink")ではない）の幅の中にどれだけの[ドット](../Page/ドット.md "wikilink")を表現できるかを表す。なお、dpiで表したドット密度の数値を、単にdpiと呼ぶことがある。

[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")や[走査](../Page/走査.md "wikilink")（スキャン）の性能表示として用いられる。また、プリントサイズと対にすることで[コンピュータ](../Page/コンピュータ.md "wikilink")上で用いる[画像](../Page/画像.md "wikilink")[データ](../Page/データ.md "wikilink")の精度を表す単位としても用いられる。ピクセル数を表すppi（）と区別して用いられる。

## 概要

通常、良好な視認結果を得られるドット密度としては、[コンピュータ](../Page/コンピュータ.md "wikilink")用[ディスプレイ](https://ja.wikipedia.org/wiki/ディスプレイ "wikilink")においては72dpiから96dpi程度が想定されている場合が多い。この数字は、[1981年](../Page/1981年.md "wikilink")発売の[Xerox Starで](../Page/Xerox_Star.md "wikilink")72dpi（1984年発売の初代[Macintosh](../Page/Macintosh.md "wikilink")が同じ72dpi）、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")発売の初代[Microsoft Windowsで](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")96dpiが標準とされたことに由来する。[Adobe PhotoshopなどMacintosh由来のソフトウェアが多用されるグラフィック業界では特に](../Page/Adobe_Photoshop.md "wikilink")72dpiが標準とされる場合が多い。

[雑誌](../Page/雑誌.md "wikilink")など印刷物においては、最低300dpiが必要である\[1\]。特に、漢字の字形は英語のアルファベットよりも一般に緻密であるため、視認性を高めるには高い解像度が必要となる。また、カラーと違って[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")効果が期待できないモノクロ印刷では、通例600dpi以上が推奨されている。

印刷物に用いるデータのdpiが低い場合は、実際に印刷した場合に[ジャギー](https://ja.wikipedia.org/wiki/ジャギー "wikilink")あるいはボケとなって現れるため、「コンピュータの画面で見た場合はちょうどよく見えても、印刷してみるとギザギザしたりボケたりして見える」といった事態を招くことになる。

[プリンターの性能表示におけるdpi値は](../Page/インクジェットプリンター.md "wikilink")、あくまでも紙上でドットが重なっても良いのでドットの中心をずらすことが可能な最小単位（多くの場合インクやトナーを吹き付ける印字ヘッド同士の間隔）の数字に過ぎず、人間の目では300dpi以上の違いはほとんどわからないといわれる。このためスキャナやディスプレイおよび商業印刷における独立したドットを数えるdpiと単純に比較することはできない。

## 高DPI環境

従来のディスプレイ製品は、解像度の向上に伴い、ドット密度はそのままで画面の物理サイズが大型化されることが多かった。

しかし、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")など、利用者の視点から画面までの距離が近く、また比較的画面の物理面積が小さいモバイル機器では、[Retinaディスプレイ](https://ja.wikipedia.org/wiki/Retinaディスプレイ "wikilink")に代表される高精細（高DPI）ディスプレイが早くから導入されてきた。一方、[ノートPC](https://ja.wikipedia.org/wiki/ノートPC "wikilink")や[デスクトップPC](https://ja.wikipedia.org/wiki/デスクトップPC "wikilink")などでも、[Full HD](https://ja.wikipedia.org/wiki/Full_HD "wikilink")/[4K解像度では画面の物理サイズを解像度に比例してそのまま大きくするのではなく](https://ja.wikipedia.org/wiki/2160p "wikilink")、物理サイズは据え置きとする代わりに従来製品よりも高いDPIを持つ高精細ディスプレイが利用されるようになっている。

なお、ソフトウェアシステム側の[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) の高DPI対応状況は、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) や[GUIツールキット](https://ja.wikipedia.org/wiki/GUIツールキット "wikilink")、あるいはアプリケーションにより様々である。このような高精細ディスプレイを従来の低DPI設定のまま利用すると、ボタンやラベルおよびそれらの内部に含まれるテキストのフォントといったGUI要素の物理サイズが小さくなってしまい、視認性や操作性が低下する。例えば100dpiディスプレイで1インチの物理サイズを持っていたGUI要素は、200dpiディスプレイだと約半分の物理サイズすなわち0.5インチしか持たないことになる。Windowsは、OSのDPI設定に応じてアプリケーションごとにウィンドウ描画内容を拡大表示することができるDPIスケーリング機能を持つが、[Windows Vistaで追加されたDPI仮想化モードでは](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、オフスクリーン描画結果を[Desktop Window Managerによって強制的に拡大するので描画内容がボケて表示されてしまうなどの問題点がある](https://ja.wikipedia.org/wiki/Desktop_Window_Manager "wikilink")。後発のモダンなGUIツールキットでは、ディスプレイDPIに依存した物理ピクセル（デバイス依存ピクセル）ではなく、ディスプレイDPIに依存せず物理的なサイズが常に一定となる論理ピクセル（デバイス非依存ピクセル）の概念を導入し、OSのDPI設定と連動することで高精細ディスプレイに対応している。

## 脚注・出典

## 関連項目

  - [lpi](https://ja.wikipedia.org/wiki/lpi "wikilink") (lines per inch)
  - [ppi](https://ja.wikipedia.org/wiki/ppi "wikilink") (pixels per inch)
  - [解像度](../Page/解像度.md "wikilink")
  - [分解能](../Page/分解能.md "wikilink")
  - [スクリーン線数](../Page/スクリーン線数.md "wikilink")

[Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink") [Category:密度の単位](https://ja.wikipedia.org/wiki/Category:密度の単位 "wikilink")

1.