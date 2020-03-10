> この記事は[Layer By Layer](https://ja.wikipedia.org/wiki/Layer_By_Layer)から翻訳されています。


**Layer By Layer**(レイヤー・バイ・レイヤー、略称**LBL**)は、[ルービックキューブ](../Page/ルービックキューブ.md "wikilink")の解法の一つ。 3x3x3の立方体である[ルービックキューブ](../Page/ルービックキューブ.md "wikilink")を3つの層と見立てて、一層ずつ順番に揃えていくことから、Layer By Layer（日本語訳：層ごとに）という名前が付けられている。

## 歴史

David Singmasterが著書「Notes on Rubik's "Magic Cube" 」（1980年）の中で紹介したのが始まりとされる\[1\]\[2\]。また1981年にベストセラーとなったJames G. Nourseの著書「The Simple Solution to Rubik's Cube」の中でも、同様の考えが採用されている\[3\]。 現在ルービックキューブのスピード解法として最も普及している[CFOPメソッド](https://ja.wikipedia.org/wiki/CFOPメソッド "wikilink")（別名Fridrichメソッド）は、Layer By Layerの考えをベースとして発展させたものである。

## 完成までの流れ

Layer By Layerでは、以下の流れに従って6面を完成させる。各パーツの名称については[ルービックキューブ](../Page/ルービックキューブ.md "wikilink")を参照。

### クロス（一層目エッジ）

[01_lbl_cross.png](https://ja.wikipedia.org/wiki/File:01_lbl_cross.png "fig:01_lbl_cross.png") 一層目のエッジを揃える。4つのエッジが揃った状態がクロス（十字架）の形になるため、クロスと呼ばれる。ルービックキューブでは各面のセンターのパーツは移動しないため、クロスの側面と各センターの色が合っている必要がある。 {{-}}

### 完全一面（一層目コーナー）

[02_lbl_fl.png](https://ja.wikipedia.org/wiki/File:02_lbl_fl.png "fig:02_lbl_fl.png") 一層目のコーナーを揃える。一面の色と同時に、その側面の色も揃った状態のことを完全一面と呼ぶ。一方、一面の色が揃っているが側面の色は揃っていない状態のことを不完全一面と呼ぶが、そこからでは六面を揃えることはできない。 {{-}}

### 二層目（Middle Layer）エッジ

[03_lbl_f2l.png](https://ja.wikipedia.org/wiki/File:03_lbl_f2l.png "fig:03_lbl_f2l.png") 二層目のエッジを揃える。最終層にあるエッジを二層目の適切な位置に移動させるための手順として、最短8手の手順を2つ覚えれば揃えることが可能である。この工程が終わることで、三層のルービックキューブのうち下二層が揃う。 {{-}}

### 最終層（Last Layer）

#### エッジ向き - Edge Orientation(EO)

[04_lbl_eo.png](https://ja.wikipedia.org/wiki/File:04_lbl_eo.png "fig:04_lbl_eo.png") 最終層のエッジの向きを揃える。2つのエッジを反転させる最短6手の手順を1つ覚えれば処理可能。 {{-}}

#### コーナー向き - Corner Orientation(CO)

[05_lbl_co.png](https://ja.wikipedia.org/wiki/File:05_lbl_co.png "fig:05_lbl_co.png") 最終層のコーナーの向きを揃える。3つのコーナーを回転させる最短7手の手順を1つ覚えれば処理可能。 {{-}}

#### コーナー場所 - Corner Permutation(CP)

[06_lbl_cp.png](https://ja.wikipedia.org/wiki/File:06_lbl_cp.png "fig:06_lbl_cp.png") 最終層のコーナーの場所を揃える。 3つのコーナーを移動させる最短9手の手順を1つ覚えれば処理可能。 {{-}}

#### エッジ場所 - Edge Permutation(EP)

[07_lbl_ep.png](https://ja.wikipedia.org/wiki/File:07_lbl_ep.png "fig:07_lbl_ep.png") 最終層のエッジの場所を揃える。3つのエッジを移動させる最短9手の手順を1つ覚えれば処理可能。 {{-}}

### 補足

最終層のエッジ向き(EO)・場所(EP)、コーナー向き(CO)・場所(CP)は、前の工程に影響を及ばさない（COと同時に前工程で揃えたEOも変わる等）手順を使うのであれば、どの順番で処理をしても完成させることができる。 現在最も使われる順番は、それぞれの工程が6～9手と少ない手数で処理可能なEO→CO→CP→EPであるが、David Singmasterが最初にまとめた方法ではEO→EP→CP→COとなっている。

## 出典

[Category:ルービックキューブ](https://ja.wikipedia.org/wiki/Category:ルービックキューブ "wikilink")

1.
2.
3.