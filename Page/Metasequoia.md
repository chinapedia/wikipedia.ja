> この記事は[Metasequoia](https://ja.wikipedia.org/wiki/Metasequoia)から翻訳されています。


**Metasequoia**（メタセコイア）は、株式会社テトラフェイスが[開発](../Page/開発.md "wikilink")・[販売](../Page/販売.md "wikilink")している[Windowsおよび](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用[3DCGソフトウェア](https://ja.wikipedia.org/wiki/3DCGソフトウェア "wikilink")である。略称は**メタセコ**または**metaseq**。無償で提供されているが、ライセンスを購入してシリアルIDを入力するまでは機能が制限される。

Metasequoia 4以降にはStandard版と高機能なEX版がある。Ver3.1以前は通常版と無償版のLEがあるが、現在はVer3.1のライセンスを購入することはできない。

本項では、開発・販売元の**株式会社テトラフェイス**についても解説する。

## 概要

[1999年](../Page/1999年.md "wikilink")5月の初版リリース時から**O.Mizno**（水野修）が個人事業で開発やサポートを行っていたが、[2012年](../Page/2012年.md "wikilink")5月から法人化の準備を進め、同年9月に株式会社テトラフェイスを設立\[1\]\[2\]。Metasequoia上の表記は2012年10月公開のVer3.1 Beta7から法人名となった。なお、公式[ブログ](../Page/ブログ.md "wikilink")では「法人になったからといって開発や販売体制など実質的な面では何も変わらない」（2012年10月時点）と説明している\[3\]。

ポリゴンメッシュによる3Dモデルの作成（[モデリング](https://ja.wikipedia.org/wiki/モデリング "wikilink")）に特化した3DCG[モデラー](../Page/モデラー.md "wikilink")である。

3DCGモデラーとしての機能性や扱いやすさ、入手のしやすさなど、日本における3DCGモデラーとして人気が高い。データ可搬性を重視しており、様々なファイル形式で入力・出力することができる。低価格であり、趣味で使用する個人ユーザーが多いが、プロが製作現場で使用することもある。採用段階でMetasequoiaの使用経験を認める企業もある\[4\]\[5\]。

開発者向けに[C++](../Page/C++.md "wikilink")用プラグインSDKを公開しているため、[シェアウェア](../Page/シェアウェア.md "wikilink")版では多くの開発者による[プラグイン](../Page/プラグイン.md "wikilink")を利用することができるようになっている。プラグインのインターフェイス自体は基本的に後方[互換性](../Page/互換性.md "wikilink")を持っているため、古いバージョンのSDKで作成されたプラグインであっても新しいバージョンのMetasequoiaでそのまま利用可能である。なお、Metasequoia 4では32bit版アプリケーションと64bit版アプリケーションの両方が提供されるようになったが、32bit版のプラグインは64bit版のアプリケーションでは使用することができない。その逆もまた然りである。

また、組込マクロ言語として[Python](../Page/Python.md "wikilink")を採用しており、簡単なバッチ処理などであればプラグインを作成・使用せずともPythonスクリプトを記述して実行することで素早く実現できるようになっている。Metasequoia Ver2.4.13時点でPython 2.2.3に対応、Ver4.5時点でPython 3.4.3に対応\[6\]。各種モジュールを使用するにはそれぞれ対応する日本語版Windows用Pythonを別途インストールする必要がある。

レンダリング機能としてスキャンラインが搭載されているが、本格的なレンダリングや動画の作成を行う場合は、他のレンダラーを併用するかプラグインを使う必要がある。Ver4.0で[レイトレーシング](../Page/レイトレーシング.md "wikilink")によるレンダリング機能が追加された。Ver4.5では[RenderMan](../Page/RenderMan.md "wikilink")との連携機能も追加されている\[7\]。

Metasequoia 4.3でボーン\[8\]に、4.5でモーフ\[9\]に標準対応するなど、これまでプラグインや別の統合ソフトと連携しなければ実現できなかった高度な機能も実装され始めている。なお、ボーンやモーフの追加情報は、モデルデータであるMQOファイルではなく、拡張用の外部MQXファイル（[XMLフォーマット](../Page/Extensible_Markup_Language.md "wikilink")）に保存される。

なお、Metasequoia自体は初版から[C++ Builderを使って開発されていることが](../Page/C++_Builder.md "wikilink")、公式ブログなどで言及されている\[10\]\[11\]。

## キャラクターアニメーション

Metasequoiaは長らくボーンやモーフなどのキャラクターアニメーション向け機能を搭載していなかった。アントラッドはMetasequoia向けキャラクターアニメーションツールとして[Mikoto](https://ja.wikipedia.org/wiki/Mikoto "wikilink")をリリースしたが、2003年のMikoto 0.4fを最後にその更新を停止した。その後、mqdlは、[Mikoto](https://ja.wikipedia.org/wiki/Mikoto "wikilink")の後継として、Metasequoia用のキャラクターアニメーションプラグインKeynoteをリリースした。

2008年、樋口優によりキャラクターアニメーションソフトウェアの[MikuMikuDance](https://ja.wikipedia.org/wiki/MikuMikuDance "wikilink") (MMD)がリリースされると、MMD用モデルの製作のためにMetasequoiaとPMDエディタ/PMXエディタの組み合わせが使われるようになった。2011年、MikuMikuDanceの開発終了が宣言され、MikuMikuDanceのクローンソフトウェアが多数登場した。

その後、Metasequoiaはバージョン4.xでボーンやモーフに直接対応し、MMD用のテンプレートも付属するようになった。

## バージョン変遷

  - 1999年5月10日 Metasequoia Ver1.0 \[12\]
  - 2000年5月3日 Metasequoia LE Ver2.0
  - 2000年5月4日 Metasequoia Ver2.0
  - 2000年10月17日 Metasequoia Ver2.1.0
  - 2001年7月22日 Metasequoia Ver2.2.0
  - 2003年10月11日 Metasequoia Ver2.3.0
  - 2006年7月25日 Metasequoia Ver2.4.0
  - 2012年4月29日 Metasequoia Ver3.0.0
  - 2012年10月25日 Metasequoia Ver3.1.0
  - 2013年9月30日 Metasequoia 4 \[13\]
  - 2014年1月24日 Metasequoia 4.1.0 \[14\]
  - 2014年1月29日 Metasequoia 3.1.6(バージョン3系最後のリリース) \[15\]
  - 2014年6月4日 Metasequoia 4.2.0 \[16\]
  - 2014年9月30日 Metasequoia 4.3.0 \[17\]
  - 2015年2月13日 Metasequoia 4.4.0 \[18\]
  - 2015年7月8日 Metasequoia 4.5.0 \[19\]
  - 2016年3月28日 Metasequoia 4.5.5(macOS版の初リリース) \[20\]
  - 2017年08月21日 Metasequoia 4.6.0 \[21\]

## モデルコンテスト

2004年7月に、Metasequoiaに収録するサンプル用モデルデータを募集するため、モデルコンテスト2004が開催された。告知から応募締め切りまで1か月しか無かった上、MQOファイルとテクスチャ用ファイルを圧縮して1MB以内であること等の制約があったが、40件近い応募があった。現在Metasequoiaに収録されているサンプルモデルの内、日本橋麒麟像(NihonbasiKirin)、Tank、魔道少女(witch)、violin、meka、kame の6つは、このコンテストの最優秀賞および入賞作品である。

なお、このモデルコンテストの表題には2004と付いているが、コンテストが行われたのは2010年現在、まだこの1回のみである。

## 関連ソフトウェア

### レンダラ

  - 現行

<!-- end list -->

  - [RenderMan](../Page/RenderMan.md "wikilink") - Metasequoia 4.xで標準対応

<!-- end list -->

  - 過去 (3.x以前)

<!-- end list -->

  - [vidro](https://ja.wikipedia.org/wiki/vidro "wikilink")

  - [Parthenon Renderer](https://ja.wikipedia.org/wiki/Parthenon_Renderer "wikilink") [1](http://www.bee-www.com/parthenon/)

  - [Warabi MP](https://ja.wikipedia.org/wiki/Warabi "wikilink")\[22\]

  - [POV-Ray](../Page/POV-Ray.md "wikilink")\[23\] - 関連ソフトウェアのMetaMegaを通して使用可能

  - \- 関連ソフトウェアのMetaSceneを通して使用可能

  - Lightflow - 関連ソフトウェアのMetalight2やMATSpiderを通して使用可能

  - [Redqueen](https://ja.wikipedia.org/wiki/Redqueen "wikilink")\[24\]\[25\]\[26\] - プラグインのrrtdlgMQを通して使用可能

### モーション / アニメーション

  - 現行

<!-- end list -->

  - [MikuMikuDance](https://ja.wikipedia.org/wiki/MikuMikuDance "wikilink") - Metasequoia 4.xでPMD形式のエクスポートに標準対応
  - Vixer Motion [2](https://vixar.jp/motion/index.html) / Vixar TransMotion [3](https://vixar.jp/transmotion/)

<!-- end list -->

  - 過去 (3.x以前)

<!-- end list -->

  - [Mikoto](https://ja.wikipedia.org/wiki/Mikoto "wikilink")\[27\]
  - エルフレイナ [4](http://sorceryforce.com/elfreina/)
  - [MechaStudio](https://ja.wikipedia.org/wiki/MechaStudio "wikilink")/ToyStudio

### ビューア

  - 過去 (3.x以前)

<!-- end list -->

  - [mini mqo Viewer](https://ja.wikipedia.org/wiki/mini_mqo_Viewer "wikilink") (mmViewer) [5](http://hheaven.net/mmViewer/)
  - BCView [6](http://www.vector.co.jp/soft/win95/art/se135421.html)
  - CelsView [7](http://sio29.sakura.ne.jp/celsview/celsview.html)

### その他

  - 現行

<!-- end list -->

  - [コミPo\!](https://ja.wikipedia.org/wiki/コミPo! "wikilink")

<!-- end list -->

  - 過去 (3.x以前)

<!-- end list -->

  - [imocea](https://ja.wikipedia.org/wiki/imocea "wikilink") (旧Rios)

## 関連項目

  - [モデラー](../Page/モデラー.md "wikilink")
  - [ニコニ立体](https://ja.wikipedia.org/wiki/ニコニ立体 "wikilink")：mqo形式の投稿に対応しておりビュアーで鑑賞可能。

## 出典

<references/>

## 外部リンク

  - [metaseq.net](http://www.metaseq.net/)（公式サイト）
  - [私家版 Metasequoia用プラグインリンク集](http://www.siobi.info/program/mq-pluginlink.htm)

[Category:3DCGソフトウェア](https://ja.wikipedia.org/wiki/Category:3DCGソフトウェア "wikilink") [Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink")

1.  [会社概要](http://www.tetraface.co.jp/jp/about.html)　tetraface　2014年11月28日確認
2.
3.
4.  [採用情報](http://ash.jp/job/)　ASH有限会社　2014年11月28日観覧
5.  [ゲームエフェクトデザイナー（アートディレクター候補）](http://jobinjapan.jp/job-listing/J24352.html)　JOBinJAPAN　2014年11月28日観覧
6.  [バージョンアップ履歴](http://www.metaseq.net/jp/release_note.html)
7.  [Metasequoia 4.5の新機能：RenderMan連携機能のチュートリアル | metaseq.net](http://www.metaseq.net/jp/archives/280/)
8.  [metaseq.net blog: Metasequoia 4.3の新機能(1) ボーン](http://blog.metaseq.net/2014/10/metasequoia-431.html)
9.  [Metasequoia 4.5の新機能：モーフ機能のチュートリアル | metaseq.net](http://www.metaseq.net/jp/archives/278/)
10. [C++Builder 2009](http://metaseq.sblo.jp/article/18463741.html)　metaseq.net blog（旧公式ブログ）　2008年08月27日
11. [C++BuilderXEへ移行中](http://metaseq.sblo.jp/article/45935261.html)　metaseq.net blog（旧公式ブログ）　2011年06月12日
12. [変形オブジェクトも楽々の国産3D CGモデリングソフト「Metasequoia」v1.0](http://www.forest.impress.co.jp/article/1999/05/13/metasequoia.html) 窓の杜 1999年5月13日
13. [Metasequoia 4を販売開始しました | metaseq.net](http://blog.metaseq.net/2013/09/metasequoia-4_30.html)
14. [Metasequoia Ver4.1.0 リリース | metaseq.net](http://blog.metaseq.net/2014/01/metasequoia-41-ver410.html)
15. [Metasequoia Ver3.1.6 リリース | metaseq.net](http://blog.metaseq.net/2014/01/metasequoia-ver316.html)
16. [Metasequoia 4.2 (Ver4.2.0) リリース | metaseq.net](http://blog.metaseq.net/2014/06/metasequoia-42-ver420.html)
17. [Metasequoia 4.3 (Ver4.3.0) リリース | metaseq.net](http://blog.metaseq.net/2014/09/metasequoia-43-ver430.html)
18. [Metasequoia 4.4 (Ver4.4.0) リリース | metaseq.net](http://blog.metaseq.net/2015/02/metasequoia-44-ver440.html)
19. [Metasequoia 4.5（Ver4.5.0）リリース | metaseq.net](http://www.metaseq.net/jp/archives/223/)
20. [Metasequoia 4.5（Ver4.5.5）for Windows・macOS/OS Xリリース | metaseq.net](http://www.metaseq.net/jp/archives/478/)
21. [Metasequoia 4.6（Ver4.6.0） for Windows・macOS/OS Xリリース | metaseq.net](http://www.metaseq.net/jp/archives/944/)
22. 『3D Character Animation Manual ローポリアニメーションのすべて』 K.KINO 2009年5月29日 ISBN 978-4797352283
23. 『メタセコイアとPOV-Rayで始める3D CG』 古俣信行 1999年12月 ISBN 978-4871937207
24. 『メタセコイアマスターガイド―Metasequoiaからつくる3DCG』 田崎進一 2004年5月15日 ISBN 978-4861000072
25. 『Metasequoia―3D CG メタセコイア入門』 横枕雄一郎、伊藤真健、むつきはつか 2004年7月 ISBN 978-4274065729
26. 『新 メタセコイアからはじめよう\! 』 原田大輔 2009年10月1日 ISBN 978-4774139982
27. 『Metasequoiaスーパーモデリングガイド』 P.212 かこみき 2007年9月10日 ISBN 978-4861004032