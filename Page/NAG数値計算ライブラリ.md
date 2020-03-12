> この記事は[NAG](https://ja.wikipedia.org/wiki/NAG)から翻訳されています。


**NAG** ライブラリは、[Numerical Algorithms Group](https://ja.wikipedia.org/wiki/Numerical_Algorithms_Group "wikilink")（NAG社）により販売されている[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")、[C言語](../Page/C言語.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、などで使用可能な[数値計算](https://ja.wikipedia.org/wiki/数値計算 "wikilink")、[統計解析](https://ja.wikipedia.org/wiki/統計解析 "wikilink")用[ライブラリ](../Page/ライブラリ.md "wikilink")である。線型方程式、[固有値](../Page/固有値.md "wikilink")問題、[補間](https://ja.wikipedia.org/wiki/補間 "wikilink")、[微積分](https://ja.wikipedia.org/wiki/微積分 "wikilink")、非線型方程式、[微分方程式](../Page/微分方程式.md "wikilink")などの[数学関数のほかに](../Page/関数_\(数学\).md "wikilink")、[相関係数](../Page/相関係数.md "wikilink")、[共分散](../Page/共分散.md "wikilink")、[多変量解析](https://ja.wikipedia.org/wiki/多変量解析 "wikilink")、[乱数](https://ja.wikipedia.org/wiki/乱数 "wikilink")発生などの統計計算や[金融工学](../Page/金融工学.md "wikilink")に必要な[関数を多く取り揃えている](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[IBM](../Page/IBM.md "wikilink") [AIX](../Page/AIX.md "wikilink")、[SGI](../Page/シリコングラフィックス.md "wikilink") [IRIX](../Page/IRIX.md "wikilink"), その他[NEC](https://ja.wikipedia.org/wiki/NEC "wikilink")や[富士通](../Page/富士通.md "wikilink")の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")などの[プラットフォームで動作する](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。英国 [The Numerical Algorithms Group Ltd.](https://ja.wikipedia.org/wiki/Numerical_Algorithms_Group "wikilink") が開発、日本国内では日本ニューメリカルアルゴリズムズグループ株式会社が販売、サポートを行なっている。 NAG数値計算ライブラリでは利用言語や環境などにより以下の5種類のライブラリが用意されている。

1.  「NAG Fortran Library」：すでに40年以上の歴史を持ち1700以上の関数より構成される。（※最新バージョンMark24）
2.  「NAG C Library」：C／C++言語の他、C\#、VBA、Java等より利用可能（最新バージョン　Mark24）
3.  「NAG Library for SMP & Multicore」：（[並列計算ライブラリとして](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")[SMP環境用並列ライブラリ](../Page/対称型マルチプロセッシング.md "wikilink")）（最新バージョンMark24）
4.  「NAG Parallel Library」：（[PCクラスタなどの分散メモリ環境用並列計算ライブラリ](../Page/コンピュータ・クラスター.md "wikilink")）

また各ライブラリのルーチンを組み込んだソフトウェアを販売できるコンポーネントライセンスも提供されている。

他のソフトウェアとの連携もはらかれており、2007年には数式処理ソフトウエア [Maple](../Page/Maple.md "wikilink") に NAG C library の使用を可能にするコネクター Maple-NAGConnector\[1\] が発売され、また [MATLAB](../Page/MATLAB.md "wikilink") のための NAG Toolbox for MATLAB\[2\]や、グラフ作成・データ解析パッケージ [Origin内蔵のOrigin](../Page/Origin_\(グラフ作成ソフト\).md "wikilink") C言語よりアクセス可能なNAGライブラリ\[3\]がある。

## 提供される関数

  - 特殊関数
      - [双曲線](../Page/双曲線.md "wikilink")関数、[ガンマ関数](../Page/ガンマ関数.md "wikilink")、[誤差関数](https://ja.wikipedia.org/wiki/誤差関数 "wikilink")、[ベッセル関数](../Page/ベッセル関数.md "wikilink")、[フレネル関数](https://ja.wikipedia.org/wiki/フレネル関数 "wikilink")、[楕円積分](../Page/楕円積分.md "wikilink")、[楕円関数](https://ja.wikipedia.org/wiki/楕円関数 "wikilink")、[エアリー関数](../Page/エアリー関数.md "wikilink")、[ケルビン関数](https://ja.wikipedia.org/wiki/ケルビン関数 "wikilink")、Hankel関数
  - [行列](https://ja.wikipedia.org/wiki/行列 "wikilink")、[ベクトル](../Page/ベクトル.md "wikilink")操作
      - [逆行列](https://ja.wikipedia.org/wiki/逆行列 "wikilink")、[疎行列](../Page/疎行列.md "wikilink")ユーティリティー
  - 線型方程式
      - 一般連立線型方程式、対称連立方程式、三角連立方程式、一般帯連立方程式、対象帯連立方程式、[LU分解](../Page/LU分解.md "wikilink")、コレスキー分解、疎行列連立方程式、大規模スパース線型連立方程式ソルバー
  - 固有値問題
      - [固有値](../Page/固有値.md "wikilink")、[固有ベクトル](https://ja.wikipedia.org/wiki/固有ベクトル "wikilink")、[シューア分解](https://ja.wikipedia.org/wiki/シューア分解 "wikilink")
  - [特異値分解](../Page/特異値分解.md "wikilink") (SVD)
  - 最小二乗問題
  - [高速フーリエ変換](../Page/高速フーリエ変換.md "wikilink") (FFT)
  - [畳み込み積分](https://ja.wikipedia.org/wiki/畳み込み積分 "wikilink")
  - 曲線、曲面フィッティング、補間
      - エルミート補間、1次元スプラインフィット、2次元スプラインフィット、修正シェパード法、[チェビシェフ級数](https://ja.wikipedia.org/wiki/チェビシェフ級数 "wikilink")
  - [最適化](https://ja.wikipedia.org/wiki/最適化 "wikilink")
      - [線型計画法](../Page/線型計画法.md "wikilink") (LP)、2次計画法 (QP)、[非線型最小二乗法](https://ja.wikipedia.org/wiki/非線型最小二乗法 "wikilink")、非線型計画法、一変量最小化、拘束条件付き大規模[スパース](https://ja.wikipedia.org/wiki/スパース "wikilink")最適化問題、拘束条件付き規模スパース二次計画問題 (QP)
  - 非線型方程式
      - 多項式の根、非線型方程式の根、連立方程式の根
  - [数値積分](https://ja.wikipedia.org/wiki/数値積分 "wikilink")
      - 有限区間の数値積分、無限区間の数値積分、多次元積分
  - 積分方程式
      - 線型フレッドホルム積分方程式、非線型ヴォルテラ畳み込み方程式、アーベル型方程式
  - [常微分方程式](../Page/常微分方程式.md "wikilink")の数値解法
      - ルンゲクッタ法、初期値問題、アダムス法、後退差分方程式 (BDF)、境界値問題
  - [偏微分方程式](../Page/偏微分方程式.md "wikilink")
      - ヘルムホルツ方程式 (Helmholtz)、マルチグリッド、楕円微分方程式、放物型偏微分方程式、ブラックショールズ (Black Scholes) モデル、Bond
  - メッシュ生成
      - 反復法、Delaunay、Advancing-Front
  - オペレーションズリサーチ (OR)
      - 整数計画、最短経路問題
  - 統計分散関数 (偏差、確率)
      - [正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")、スチューデントの[t分布](https://ja.wikipedia.org/wiki/t分布 "wikilink")、χ二乗分布 ([カイ二乗分布](../Page/カイ二乗分布.md "wikilink"))、[F分布](../Page/F分布.md "wikilink")、[ベータ分布](https://ja.wikipedia.org/wiki/ベータ分布 "wikilink")、[ガンマ分布](../Page/ガンマ分布.md "wikilink")、[離散分布](https://ja.wikipedia.org/wiki/離散分布 "wikilink")
  - 乱数発生
      - 準乱数系列、[一様分布](https://ja.wikipedia.org/wiki/一様分布 "wikilink")、[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")、[多変量正規分布](https://ja.wikipedia.org/wiki/多変量正規分布 "wikilink")、[ベータ分布](https://ja.wikipedia.org/wiki/ベータ分布 "wikilink")、[指数分布](../Page/指数分布.md "wikilink")、[ガンマ分布](../Page/ガンマ分布.md "wikilink")、[二項分布](../Page/二項分布.md "wikilink")、[超幾何分布](https://ja.wikipedia.org/wiki/超幾何分布 "wikilink")、[フォン・ミーゼス分布](https://ja.wikipedia.org/wiki/フォン・ミーゼス分布 "wikilink")、離散分布
  - 一変量推定
      - [二項分布](../Page/二項分布.md "wikilink")信頼区間、[ポアソン分布](../Page/ポアソン分布.md "wikilink")信頼区間、[ワイブル分布](../Page/ワイブル分布.md "wikilink")信頼区間、[ロバスト推定](https://ja.wikipedia.org/wiki/ロバスト推定 "wikilink")
  - [回帰分析](../Page/回帰分析.md "wikilink")
      - [線型回帰](https://ja.wikipedia.org/wiki/線型回帰 "wikilink")分析、多重線型回帰分析
      - [相関分析](https://ja.wikipedia.org/wiki/相関分析 "wikilink")
      - ピアソン積率[相関係数](../Page/相関係数.md "wikilink")、[共分散行列](https://ja.wikipedia.org/wiki/共分散行列 "wikilink")、偏相関行列、偏共分散行列
  - [多変量解析](https://ja.wikipedia.org/wiki/多変量解析 "wikilink")
      - [因子分析](../Page/因子分析.md "wikilink")、[主成分分析](../Page/主成分分析.md "wikilink") (PCA)、正準分析、クラスタ分析、判別分析
  - 一般化線型モデル (GLM)
  - [分散分析](../Page/分散分析.md "wikilink") (ANOVA)
  - 時系列分析
      - [ARIMA](https://ja.wikipedia.org/wiki/ARIMA "wikilink")モデルフィット、[ARMA](https://ja.wikipedia.org/wiki/ARMA "wikilink")モデルフィット、予測、[伝達関数](https://ja.wikipedia.org/wiki/伝達関数 "wikilink")、スペクトル解析、ACF、PACF
  - 生存解析
      - カプランマイヤ推定値、コックス・ハザード・モデル、危険集合
  - ノンパラメトリック統計
      - コックススチュアート検定、[ウィルコクソン検定](https://ja.wikipedia.org/wiki/ウィルコクソン検定 "wikilink")、ラン検定、マクネマー検定、[マン・ホイットニー検定](https://ja.wikipedia.org/wiki/マン・ホイットニー検定 "wikilink")、フリードマン検定、クラスカルウォリス検定、コクランQ検定、[コルモゴロフ・スミルノフ検定](https://ja.wikipedia.org/wiki/コルモゴロフ・スミルノフ検定 "wikilink")、[ケンドール](../Page/ケンドール.md "wikilink")の合致係数、ケンドールの階数相関

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

  - [NAG社](http://www.nag.co.uk/)
  - [日本NAG社 日本法人](http://www.nag-j.co.jp/index.htm)
  - [NAG数値計算ライブラリ](http://www.nag-j.co.jp/nag_lib.htm)

[Category:数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:数値解析ソフトウェア "wikilink") [Category:数値計算ライブラリー](https://ja.wikipedia.org/wiki/Category:数値計算ライブラリー "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  [Maple-NAGConnector 製品紹介ページ](http://www.nag-j.co.jp/nagmaple/maple-nag.htm)
2.  [NAG Toolbox for MATLAB 製品紹介ページ](http://www.nag-j.co.jp/nagtoolbox/index.htm)
3.  [OriginにおけるNAGライブラリ紹介ページ](http://www.originlab.com/index.aspx?go=Products/Origin/Programming/NAGLibrary)