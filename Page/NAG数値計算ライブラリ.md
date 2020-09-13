> この記事は[NAG数値計算ライブラリ](https://ja.wikipedia.org/wiki/NAG数値計算ライブラリ)から翻訳されています。


**NAG** ライブラリは、[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")、[C言語](../Page/C言語.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、などで使用可能な[数値計算](https://ja.wikipedia.org/wiki/数値計算 "wikilink")、[統計解析](https://ja.wikipedia.org/wiki/統計解析 "wikilink")用[ライブラリ](../Page/ライブラリ.md "wikilink")であり、[Numerical Algorithms Group](https://ja.wikipedia.org/wiki/Numerical_Algorithms_Group "wikilink")（NAG社）により販売されている。線型方程式、[固有値](../Page/固有値.md "wikilink")問題、[補間](https://ja.wikipedia.org/wiki/補間 "wikilink")、[微積分](https://ja.wikipedia.org/wiki/微積分 "wikilink")、非線型方程式、[微分方程式](../Page/微分方程式.md "wikilink")などの[数学関数のほかに](../Page/関数_\(数学\).md "wikilink")、[相関係数](../Page/相関係数.md "wikilink")、[共分散](../Page/共分散.md "wikilink")、[多変量解析](https://ja.wikipedia.org/wiki/多変量解析 "wikilink")、[乱数](https://ja.wikipedia.org/wiki/乱数 "wikilink")発生などの統計計算や[金融工学](../Page/金融工学.md "wikilink")に必要な[関数を多く取り揃えている](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[IBM](../Page/IBM.md "wikilink") [AIX](../Page/AIX.md "wikilink")、[SGI](../Page/シリコングラフィックス.md "wikilink") [IRIX](../Page/IRIX.md "wikilink"), その他[NEC](https://ja.wikipedia.org/wiki/NEC "wikilink")や[富士通](../Page/富士通.md "wikilink")の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")などの[プラットフォームで動作する](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。英国 [The Numerical Algorithms Group Ltd.](https://ja.wikipedia.org/wiki/Numerical_Algorithms_Group "wikilink") が開発、日本国内では日本ニューメリカルアルゴリズムズグループ株式会社が販売、サポートを行なっている。 NAG数値計算ライブラリでは利用言語や環境などにより以下の5種類のライブラリが用意されている。

1.  「NAG Fortran Library」：すでに40年以上の歴史を持ち1700以上の関数より構成される。（※最新バージョンMark24）
2.  「NAG C Library」：C／C++言語の他、C\#、VBA、Java等より利用可能（最新バージョン　Mark24）
3.  「NAG Library for SMP & Multicore」：（[並列計算ライブラリとして](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")[SMP環境用並列ライブラリ](../Page/対称型マルチプロセッシング.md "wikilink")）（最新バージョンMark24）
4.  「NAG Parallel Library」：（[PCクラスタなどの分散メモリ環境用並列計算ライブラリ](../Page/コンピュータ・クラスター.md "wikilink")）

また各ライブラリのルーチンを組み込んだソフトウェアを販売できるコンポーネントライセンスも提供されている。

他のソフトウェアとの連携もはらかれており、2007年には数式処理ソフトウエア [Maple](../Page/Maple.md "wikilink") に NAG C library の使用を可能にするコネクター Maple-NAGConnector\[1\] が発売され、また [MATLAB](../Page/MATLAB.md "wikilink") のための NAG Toolbox for MATLAB\[2\]や、グラフ作成・データ解析パッケージ [Origin内蔵のOrigin](../Page/Origin_\(グラフ作成ソフト\).md "wikilink") C言語よりアクセス可能なNAGライブラリ\[3\]がある。

## 提供される関数

<table>
<thead>
<tr class="header">
<th><p>分類</p></th>
<th><p>関数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>特殊関数</p></td>
<td><ul>
<li><a href="../Page/双曲線.md" title="wikilink">双曲線</a>関数</li>
<li><a href="../Page/ガンマ関数.md" title="wikilink">ガンマ関数</a></li>
<li><a href="https://ja.wikipedia.org/wiki/誤差関数" title="wikilink">誤差関数</a></li>
<li><a href="../Page/ベッセル関数.md" title="wikilink">ベッセル関数</a></li>
<li><a href="https://ja.wikipedia.org/wiki/フレネル関数" title="wikilink">フレネル関数</a></li>
<li><a href="../Page/楕円積分.md" title="wikilink">楕円積分</a></li>
<li><a href="https://ja.wikipedia.org/wiki/楕円関数" title="wikilink">楕円関数</a></li>
<li><a href="../Page/エアリー関数.md" title="wikilink">エアリー関数</a></li>
<li><a href="https://ja.wikipedia.org/wiki/ケルビン関数" title="wikilink">ケルビン関数</a></li>
<li>Hankel関数</li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/行列" title="wikilink">行列</a>、<a href="../Page/ベクトル.md" title="wikilink">ベクトル</a>操作</p></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/逆行列" title="wikilink">逆行列</a></li>
<li><a href="../Page/疎行列.md" title="wikilink">疎行列</a>ユーティリティー</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>線型方程式</p></td>
<td><ul>
<li>一般連立線型方程式</li>
<li>対称連立方程式</li>
<li>三角連立方程式</li>
<li>一般帯連立方程式</li>
<li>対象帯連立方程式</li>
<li><a href="../Page/LU分解.md" title="wikilink">LU分解</a></li>
<li>コレスキー分解</li>
<li>疎行列連立方程式</li>
<li>大規模スパース線型連立方程式ソルバー</li>
</ul></td>
</tr>
<tr class="even">
<td><p>固有値問題</p></td>
<td><ul>
<li><a href="../Page/固有値.md" title="wikilink">固有値</a></li>
<li><a href="https://ja.wikipedia.org/wiki/固有ベクトル" title="wikilink">固有ベクトル</a></li>
<li><a href="https://ja.wikipedia.org/wiki/シューア分解" title="wikilink">シューア分解</a></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/特異値分解.md" title="wikilink">特異値分解</a> (SVD)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>最小二乗問題</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/高速フーリエ変換.md" title="wikilink">高速フーリエ変換</a> (FFT)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/畳み込み積分" title="wikilink">畳み込み積分</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>曲線、曲面フィッティング、補間</p></td>
<td><ul>
<li>エルミート補間</li>
<li>1次元スプラインフィット</li>
<li>2次元スプラインフィット</li>
<li>修正シェパード法</li>
<li><a href="https://ja.wikipedia.org/wiki/チェビシェフ級数" title="wikilink">チェビシェフ級数</a></li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/最適化" title="wikilink">最適化</a></p></td>
<td><ul>
<li><a href="../Page/線型計画法.md" title="wikilink">線型計画法</a> (LP)</li>
<li>2次計画法 (QP)</li>
<li><a href="https://ja.wikipedia.org/wiki/非線型最小二乗法" title="wikilink">非線型最小二乗法</a></li>
<li>非線型計画法</li>
<li>一変量最小化</li>
<li>拘束条件付き大規模<a href="https://ja.wikipedia.org/wiki/スパース" title="wikilink">スパース</a>最適化問題</li>
<li>拘束条件付き規模スパース二次計画問題 (QP)</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>非線型方程式</p></td>
<td><ul>
<li>多項式の根</li>
<li>非線型方程式の根</li>
<li>連立方程式の根</li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/数値積分" title="wikilink">数値積分</a></p></td>
<td><ul>
<li>有限区間の数値積分</li>
<li>無限区間の数値積分</li>
<li>多次元積分</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>積分方程式</p></td>
<td><ul>
<li>線型フレッドホルム積分方程式</li>
<li>非線型ヴォルテラ畳み込み方程式</li>
<li>アーベル型方程式</li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="../Page/常微分方程式.md" title="wikilink">常微分方程式</a>の数値解法</p></td>
<td><ul>
<li>ルンゲクッタ法</li>
<li>初期値問題</li>
<li>アダムス法</li>
<li>後退差分方程式 (BDF)</li>
<li>境界値問題</li>
</ul></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/偏微分方程式.md" title="wikilink">偏微分方程式</a></p></td>
<td><ul>
<li>ヘルムホルツ方程式 (Helmholtz)</li>
<li>マルチグリッド</li>
<li>楕円微分方程式</li>
<li>放物型偏微分方程式</li>
<li>ブラックショールズ (Black Scholes) モデル</li>
<li>Bond</li>
</ul></td>
</tr>
<tr class="even">
<td><p>メッシュ生成</p></td>
<td><ul>
<li>反復法</li>
<li>Delaunay</li>
<li>Advancing-Front</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>オペレーションズリサーチ (OR)</p></td>
<td><ul>
<li>整数計画</li>
<li>最短経路問題</li>
</ul></td>
</tr>
<tr class="even">
<td><p>統計分散関数 (偏差、確率)</p></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/正規分布" title="wikilink">正規分布</a></li>
<li>スチューデントの<a href="https://ja.wikipedia.org/wiki/t分布" title="wikilink">t分布</a></li>
<li>χ二乗分布 (<a href="../Page/カイ二乗分布.md" title="wikilink">カイ二乗分布</a>)</li>
<li><a href="../Page/F分布.md" title="wikilink">F分布</a></li>
<li><a href="../Page/ベータ分布.md" title="wikilink">ベータ分布</a></li>
<li><a href="../Page/ガンマ分布.md" title="wikilink">ガンマ分布</a></li>
<li><a href="https://ja.wikipedia.org/wiki/離散分布" title="wikilink">離散分布</a></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>乱数発生</p></td>
<td><ul>
<li>準乱数系列</li>
<li><a href="../Page/一様分布.md" title="wikilink">一様分布</a></li>
<li><a href="https://ja.wikipedia.org/wiki/正規分布" title="wikilink">正規分布</a></li>
<li><a href="https://ja.wikipedia.org/wiki/多変量正規分布" title="wikilink">多変量正規分布</a></li>
<li><a href="../Page/ベータ分布.md" title="wikilink">ベータ分布</a></li>
<li><a href="../Page/指数分布.md" title="wikilink">指数分布</a></li>
<li><a href="../Page/ガンマ分布.md" title="wikilink">ガンマ分布</a></li>
<li><a href="../Page/二項分布.md" title="wikilink">二項分布</a></li>
<li><a href="../Page/超幾何分布.md" title="wikilink">超幾何分布</a></li>
<li><a href="https://ja.wikipedia.org/wiki/フォン・ミーゼス分布" title="wikilink">フォン・ミーゼス分布</a></li>
<li>離散分布</li>
</ul></td>
</tr>
<tr class="even">
<td><p>一変量推定</p></td>
<td><ul>
<li><a href="../Page/二項分布.md" title="wikilink">二項分布</a>信頼区間</li>
<li><a href="../Page/ポアソン分布.md" title="wikilink">ポアソン分布</a>信頼区間</li>
<li><a href="../Page/ワイブル分布.md" title="wikilink">ワイブル分布</a>信頼区間</li>
<li><a href="https://ja.wikipedia.org/wiki/ロバスト推定" title="wikilink">ロバスト推定</a></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/回帰分析.md" title="wikilink">回帰分析</a></p></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/線型回帰" title="wikilink">線型回帰</a>分析</li>
<li>多重線型回帰分析</li>
<li><a href="https://ja.wikipedia.org/wiki/相関分析" title="wikilink">相関分析</a></li>
<li>ピアソン積率<a href="../Page/相関係数.md" title="wikilink">相関係数</a></li>
<li><a href="https://ja.wikipedia.org/wiki/共分散行列" title="wikilink">共分散行列</a></li>
<li>偏相関行列</li>
<li>偏共分散行列</li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/多変量解析" title="wikilink">多変量解析</a></p></td>
<td><ul>
<li><a href="../Page/因子分析.md" title="wikilink">因子分析</a></li>
<li><a href="../Page/主成分分析.md" title="wikilink">主成分分析</a> (PCA)</li>
<li>正準分析</li>
<li>クラスタ分析</li>
<li>判別分析</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>一般化線型モデル (GLM)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/分散分析.md" title="wikilink">分散分析</a> (ANOVA)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>時系列分析</p></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/ARIMA" title="wikilink">ARIMA</a>モデルフィット</li>
<li><a href="https://ja.wikipedia.org/wiki/ARMA" title="wikilink">ARMA</a>モデルフィット</li>
<li>予測</li>
<li><a href="https://ja.wikipedia.org/wiki/伝達関数" title="wikilink">伝達関数</a></li>
<li>スペクトル解析</li>
<li>ACF</li>
<li>PACF</li>
</ul></td>
</tr>
<tr class="even">
<td><p>生存解析</p></td>
<td><ul>
<li>カプランマイヤ推定値</li>
<li>コックス・ハザード・モデル</li>
<li>危険集合</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>ノンパラメトリック統計</p></td>
<td><ul>
<li>コックススチュアート検定</li>
<li><a href="https://ja.wikipedia.org/wiki/ウィルコクソン検定" title="wikilink">ウィルコクソン検定</a></li>
<li>ラン検定</li>
<li>マクネマー検定</li>
<li><a href="https://ja.wikipedia.org/wiki/マン・ホイットニー検定" title="wikilink">マン・ホイットニー検定</a></li>
<li>フリードマン検定</li>
<li>クラスカルウォリス検定</li>
<li>コクランQ検定</li>
<li><a href="https://ja.wikipedia.org/wiki/コルモゴロフ・スミルノフ検定" title="wikilink">コルモゴロフ・スミルノフ検定</a></li>
<li><a href="../Page/ケンドール.md" title="wikilink">ケンドール</a>の合致係数</li>
<li>ケンドールの階数相関</li>
</ul></td>
</tr>
</tbody>
</table>

## 脚注

<references/>

## 関連項目

  - [数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")
  - [アルゴリズム](../Page/アルゴリズム.md "wikilink")
  - [計算科学](../Page/計算科学.md "wikilink")
  - [シミュレーション](../Page/シミュレーション.md "wikilink")
  - [数値解析ソフトウェア](https://ja.wikipedia.org/wiki/数値解析ソフトウェア "wikilink")
  - [金融工学](../Page/金融工学.md "wikilink")

## 外部リンク

  - [NAG社](https://www.nag.co.uk/)
  - [日本NAG社 日本法人](https://www.nag-j.co.jp/)
  - [NAG数値計算ライブラリ](https://www.nag-j.co.jp/naglib/)

[Category:数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:数値解析ソフトウェア "wikilink") [Category:数値計算ライブラリー](https://ja.wikipedia.org/wiki/Category:数値計算ライブラリー "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  [Maple-NAGConnector 製品紹介ページ](http://www.nag-j.co.jp/nagmaple/maple-nag.htm)
2.  [NAG Toolbox for MATLAB 製品紹介ページ](http://www.nag-j.co.jp/nagtoolbox/index.htm)
3.  [OriginにおけるNAGライブラリ紹介ページ](http://www.originlab.com/index.aspx?go=Products/Origin/Programming/NAGLibrary)