> この記事は[OneSpace Designer](https://ja.wikipedia.org/wiki/OneSpace_Designer)から翻訳されています。


**OneSpace Designer**（ワンスペース デザイナー）は、ドイツ製の機械設計製造業向け[CAD](../Page/CAD.md "wikilink")[ソフトである](../Page/ソフトウェア.md "wikilink")。

## 概要

開発は[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")に本社を置くCoCreate Software GmbH（コクリエイト・ソフトウェア）社。 日本ではPTCジャパン株式会社コクリエイト事業本部（東京都府中市）が販売・サポートを行う。

OneSpace Designerは3次元CADソフトのModelingと2次元CADソフトのDraftingを含む総称。

2007年12月に独CoCreate Softwareは、Pro/ENGINEER（現[PTC Creo](https://ja.wikipedia.org/wiki/PTC_Creo_Parametric "wikilink")）で著名な米[PTCに買収され](https://ja.wikipedia.org/wiki/パラメトリック・テクノロジー・コーポレーション "wikilink")、OneSpaceはPTCの許で機械設計CADのラインナップとなった。

2007年12月の米PTCによる買収以降、製品総称は[OneSpace](https://ja.wikipedia.org/wiki/OneSpace "wikilink")から[CoCreate](https://ja.wikipedia.org/wiki/CoCreate "wikilink")に変更された。これにより、3次元CADソフトはCoCreate Modeling、2次元CADソフトはCoCreate Draftingという名称になった。

## OneSpace Designer Modeling

OneSpace Designer Modelingはコクリエイト・ソフトウェア社の前身であった[Hewlett-Packard社のMechanical](../Page/ヒューレット・パッカード.md "wikilink") Design Divisionが1992年に当初SolidDesingerという名称でリリース、特徴は現在の3次元CADの多くが採用するヒストリーやフィーチャーによる間接的な形状モデルの操作でなく、ダイナミックモデリングと呼称する直接的な操作性が特徴。

OneSpaceが踏襲しているのは3次元形状モデリングの古典とも言える立体のブール集合演算である。「立体から立体を引く」や「立体を足す」などを繰り返すこの手法の問題は、設計の後期では立体構造が複雑になるほど計算に時間がかかり、場合によっては立体計算ができなくなる問題であった。これには初期のハードウエアの性能の処理能力の限界も起因した。

この問題を解決したのは1984年に現れたPTCのPro/ENGINEERであり、Pro/ENGINEER以後の[CAD](../Page/CAD.md "wikilink")多くがフィーチャベース、パラメトリックドリブンを踏襲するが、OneSpaceはフィーチャーベースに依存することなく、伝統的な手法をソフトウエアとして精度を高めることにより、ソリッド・データの破綻を回避した。「削ったり、捻ったり、加工に近い感覚で」「粘土でモデリングするように」と表現される「ダイナミック・モデリング」（直感的なモデリング）の起源である。

「ダイナミック」はフィーチャーベースが、形状の変更にはフィーチャーとその依存関係の把握という、ソフトウエアのプログラミングのようなわずらわしいモデリング手法の反語としてCoCreateにより表現された。

伝統的なモデリング手法を精錬で高めることで、製品が複雑化した現在の設計に適用まで具現化した数少ないの3次元CADであり、PTCを含め、以後の製造業を起源としないソフトウエアハウス製のフィチャーベース3次元CADの「理論と実務のギャップ」を感じた利用企業のエンジニアが、設計のあり方へ回帰するかたちでOneSpace Modeling の採用を行ってきた。

その手法の正当性は、多くのフィーチャーベースのCADが後付で「直感的」「ダイナミック」という形状変更の機能を跡付けで追加することにあらわされている。

反証の対象はPTCのPro/ENGINEERであり、そのPTCに買収されたことは、業界やユーザにおいて驚愕を与えた。

カスタマイズはKyoto Common Lisp(詳しくは[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")の項を参照)をベースとしたLisp言語を用いて行う。LispはMEマクロに代わり採用されたが、プログラマが日本では少ないのが難点とも言える。同様の理由でサードパーティ製のプラグインの専門モジュールが少ない。

2D同様、開発期間が短いなど、緊急性の高い速いモデリングを必要とする企業利用者に評価が高い。

2007年12月の米PTCによる買収以降、モデリング手法の名称が「ダイナミックモデリング」から「エクスプリシット モデリング」に変更された。

## OneSpace Designer Drafting

OneSpace Designer DraftingはModeling同様、コクリエイト・ソフトウェア社の前身であった Hewlett-Packard社のMechanical Design Divisionが1985年に 当初ME10(Mechanical Engineering series 10)という名称でリリースした。 当時の2次元CADの不満を研究した、下書き線機能やマクロ・メニューカスタマイズ機能の斬新さが特徴。

なお、カスタマイズはME10マクロとよばれる独自のインタプリタ言語を用いて行う。コンパイル、リンケージの必要がなくユーザが容易に自社用の機能を追加できる。

ハードウエアベンダーがハードウエアの販売目的に開発・販売したアプリケーションソフトの例に漏れず、脱UNIXに遅れ大手企業向けの高額な価格設定、ハードウエア然としたソフトウエア保守契約などから、後発のPC/Windows 系CADのシェア拡大には追従できていない。

利用者の評価は高く、2次元で設計する上での機械設計に適した機能に愛着を持つ設計者は多い。「下書き線と清書」の機能、「コ・パイロット」と言われる作図のアシスト機能。レイヤーではなく「パーツ」に近い階層構造の図形管理など。総合すると「手書きに近い」手順が評価が高い。

## 稼働OS

  - [Microsoft](../Page/マイクロソフト.md "wikilink") [Windows2000](../Page/Microsoft_Windows_2000.md "wikilink")/[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")/Windows XP x64 Edition
  - 開発当初は[HP-UX](../Page/HP-UX.md "wikilink")等のUNIXで動作したが、バージョン2005を最後にMicrosoft Windowsのみでの動作となっている。

## 外部リンク

  - [コクリエイト・ソフトウェア株式会社](http://japan.cocreate.com/)

[Category:CADソフト](https://ja.wikipedia.org/wiki/Category:CADソフト "wikilink")