> この記事は[ABINIT](https://ja.wikipedia.org/wiki/ABINIT)から翻訳されています。


**ABINIT**は、[材料科学のための](../Page/材料工学.md "wikilink")[オープンソースプログラム](../Page/オープンソースソフトウェア.md "wikilink")[スイートである](https://ja.wikipedia.org/wiki/ソフトウェアスイート "wikilink")。[GNU General Public Licenseの下で配布されている](../Page/GNU_General_Public_License.md "wikilink")。ABINITは[分子](../Page/分子.md "wikilink")から、表面、固体まで様々な材料の電子密度と導出特性を計算するために、平面波[基底関数系および](https://ja.wikipedia.org/wiki/基底関数系_\(化学\) "wikilink")[擬ポテンシャル](../Page/擬ポテンシャル.md "wikilink")を使って[密度汎関数理論](../Page/密度汎関数理論.md "wikilink")を実装している。世界中の研究者が協力してABINITを開発している\[1\]\[2\]\[3\]\[4\]。

ウェブベースの使いやすいグラフィカル版（ABINITの完全な機能のうち一部にアクセスできる）がを通じて無料で利用できる。

## 概要

ABINITは、材料中の電子を記述する[コーン–シャム方程式](https://ja.wikipedia.org/wiki/コーン–シャム方程式 "wikilink")を解くことによって[密度汎関数理論](../Page/密度汎関数理論.md "wikilink")を実装する。平面波基底関数系によって拡張され、[自己無撞着共役勾配法を使ってエネルギー最小構造を決定する](https://ja.wikipedia.org/wiki/セルフコンシステント "wikilink")。計算効率性は[高速フーリエ変換](../Page/高速フーリエ変換.md "wikilink")\[5\]および内殻電子を記述するための[擬ポテンシャル](../Page/擬ポテンシャル.md "wikilink")を使用することで達成される。標準的な[ノルム保存型擬ポテンシャル](../Page/ノルム保存型擬ポテンシャル.md "wikilink")の代替として、[PAW法](../Page/PAW法.md "wikilink")\[6\]（projector augmented-wave method）を使うことができる。全エネルギーに加えて、幾何最適化および*[ab initio](https://ja.wikipedia.org/wiki/ab_initio "wikilink")*[分子動力学](https://ja.wikipedia.org/wiki/分子動力学 "wikilink")を実行できるように力および応力を計算することもできる。ABINITによって扱うことのできる材料としては、絶縁体、金属、ならびに[モット-ハバード絶縁体を含む磁気的に秩序化した系がある](https://ja.wikipedia.org/wiki/モット絶縁体 "wikilink")。

## 導出特性

材料の電子的基底状態を計算することに加えて、ABINITは以下の項目を含む応答関数を計算するための密度汎関数摂動理論を実装する。

  - [フォノン](../Page/フォノン.md "wikilink")
  - 誘電応答
  - ボルン有効電荷およびIR絶縁体強度テンソル
  - ひずみに対する応答ならびに弾性特性
  - 圧電応答、ラマン断面、および[電気光学応答を含む非線形応答](../Page/電気光学効果.md "wikilink")

ABINITは

  - [時間依存密度汎関数法](../Page/時間依存密度汎関数法.md "wikilink")
  - [GW近似](../Page/GW近似.md "wikilink")および[ベーテ・サルピータ方程式](https://ja.wikipedia.org/wiki/ベーテ・サルピータ方程式 "wikilink")を使った多体摂動理論

によって励起状態特性を計算することもできる。

## 出典

<references/>

## 外部リンク

  -
  - [Graphical version (web-based) of ABINIT](http://nanohub.org/resources/ABINIT)

[Category:計算化学ソフトウェア](https://ja.wikipedia.org/wiki/Category:計算化学ソフトウェア "wikilink") [Category:密度汎関数理論](https://ja.wikipedia.org/wiki/Category:密度汎関数理論 "wikilink") [Category:フリー科学ソフトウェア](https://ja.wikipedia.org/wiki/Category:フリー科学ソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.