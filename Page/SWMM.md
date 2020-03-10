> この記事は[SWMM](https://ja.wikipedia.org/wiki/SWMM)から翻訳されています。


[アメリカ合衆国環境保護庁](../Page/アメリカ合衆国環境保護庁.md "wikilink")の**SWMM**(*Storm Water Management Model*、[雨水](../Page/雨水.md "wikilink")管理モデル）は、主に[都市](../Page/都市.md "wikilink")および[郊外](https://ja.wikipedia.org/wiki/郊外 "wikilink")の表面流出および[地下](https://ja.wikipedia.org/wiki/地下 "wikilink")流出の質と量に関する長期間の[シミュレーション](../Page/シミュレーション.md "wikilink")を用いた動学的降雨水量流出モデルである。SWMMに含まれる流出水や水系は、[シミュレーション](../Page/シミュレーション.md "wikilink")によって、[蒸発](https://ja.wikipedia.org/wiki/蒸発 "wikilink")や[浸透によって部分集水域から失われた量を計算した後の](https://ja.wikipedia.org/wiki/浸透_\(水文学\) "wikilink")、降水や流出、汚染物質負荷を受容する部分集水域における集積量に作用している。SWMMのルートや水文学的構成は、流水や全ての水系を運搬しているが、閉管、開水路、貯蔵／処理装置、ポンプ、開口部、[堰](https://ja.wikipedia.org/wiki/堰 "wikilink")、調整施設などの[システム](../Page/システム.md "wikilink")を通じたものである。SWMMは部分集水域で生まれた[水質](../Page/水質.md "wikilink")と水量を描き、流速、水系の深さおよび[パイプ](../Page/パイプ.md "wikilink")を流れる[水](../Page/水.md "wikilink")の[水質](../Page/水質.md "wikilink")は、可変速の時間ステップである。[ベストプラクティス](../Page/ベストプラクティス.md "wikilink")やLIDなどの手法を用いて水域系にある部分集水域からシミュレートされたSWMMは、[アメリカ環境保護庁](https://ja.wikipedia.org/wiki/アメリカ環境保護庁 "wikilink")などの機関において幅広く使用されている。

## SWMMの歴史

SWMMは、初期に[1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")-[1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")に運用された。その後、[1975年](../Page/1975年.md "wikilink")、[1981年](../Page/1981年.md "wikilink")、[1988年](../Page/1988年.md "wikilink")の3回の改訂を経た後に、[FORTRAN](../Page/FORTRAN.md "wikilink")から[C言語](../Page/C言語.md "wikilink")へのリライトがされた。 [アメリカ環境保護庁](https://ja.wikipedia.org/wiki/アメリカ環境保護庁 "wikilink")のSWMMは、水域的な流域データや[リアルタイム](../Page/リアルタイム.md "wikilink")[コントロール](https://ja.wikipedia.org/wiki/コントロール "wikilink")、[水質](../Page/水質.md "wikilink")[シミュレーション](../Page/シミュレーション.md "wikilink")を[Microsoft Windows XPと](../Page/Microsoft_Windows_XP.md "wikilink")[Microsoft Windows Vistaの下で動かし](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、地理環境の統合的情報を与える。 最近リライトされた[アメリカ環境保護庁](https://ja.wikipedia.org/wiki/アメリカ環境保護庁 "wikilink")SWMMは、[アメリカ環境保護庁](https://ja.wikipedia.org/wiki/アメリカ環境保護庁 "wikilink")の国家リスクマネージメントリサーチ研究室の水供給および水資源部門において生み出され、ここにはCRADA(Cooperative Research and Development Agreement)の下のCDM Incのコンサルトを受けている。 [アメリカ環境保護庁](https://ja.wikipedia.org/wiki/アメリカ環境保護庁 "wikilink")のSWMMのアップデートの歴史については、その[ホームページ](../Page/ホームページ.md "wikilink")を参照されたい。

## 統合的解決

例えば、SWMM5での大きな進歩は、[都市](../Page/都市.md "wikilink")・[郊外](https://ja.wikipedia.org/wiki/郊外 "wikilink")における表面と[地下](https://ja.wikipedia.org/wiki/地下 "wikilink")における水域を、排水ネットワークの水文学的コンピューティングを使って行うことであろう。水文学と水力学の2つのコンピューティングを分ける著しい改善を見る進歩であり、実際の[環境](../Page/環境.md "wikilink")で[物理](https://ja.wikipedia.org/wiki/物理 "wikilink")的に発生する相互の作用をモデル化することがコンセプトとして可能になった。SWMM5の[数値](https://ja.wikipedia.org/wiki/数値 "wikilink")[エンジン](../Page/エンジン.md "wikilink")は、表面流出や[地下](https://ja.wikipedia.org/wiki/地下 "wikilink")の水域を計算し、乾湿の水域的時間進行を[気候](../Page/気候.md "wikilink")[データ](../Page/データ.md "wikilink")から課すことができる。水域のリンク、結節点、[コントロール](https://ja.wikipedia.org/wiki/コントロール "wikilink")[ルール](https://ja.wikipedia.org/wiki/ルール "wikilink")および[ネットワーク](../Page/ネットワーク.md "wikilink")の[境界条件](https://ja.wikipedia.org/wiki/境界条件 "wikilink")を導出する水文学的計算法では、[補間](https://ja.wikipedia.org/wiki/補間 "wikilink")法ルーチンを用いた水域の時間ステップを固定速度／可変速度で計算し、水域の[始値](https://ja.wikipedia.org/wiki/始値 "wikilink")・[終値](https://ja.wikipedia.org/wiki/終値 "wikilink")を[シミュレート](https://ja.wikipedia.org/wiki/シミュレート "wikilink")することで得られる。

## 関連項目

  - [水文学](https://ja.wikipedia.org/wiki/水文学 "wikilink")
  - [水理学](../Page/水理学.md "wikilink")
  - [表面流出](https://ja.wikipedia.org/wiki/表面流出 "wikilink")
  - [降水](https://ja.wikipedia.org/wiki/降水 "wikilink")
  - [水質汚染](https://ja.wikipedia.org/wiki/水質汚染 "wikilink")

## 外部リンク

  - [アメリカ環境保護庁ホームページ](http://www.epa.gov/ednnrmrl/)
  - [アメリカ環境保護庁ホームページ内　SWMM 5 page](http://www.epa.gov/ednnrmrl/models/swmm/index.htm)

[Category:環境](https://ja.wikipedia.org/wiki/Category:環境 "wikilink") [Category:コンピュータの利用](https://ja.wikipedia.org/wiki/Category:コンピュータの利用 "wikilink") [Category:水文学のモデル](https://ja.wikipedia.org/wiki/Category:水文学のモデル "wikilink")