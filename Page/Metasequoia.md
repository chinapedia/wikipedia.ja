> この記事は[Metasequoia](https://ja.wikipedia.org/wiki/Metasequoia)から翻訳されています。


**Metasequoia**（メタセコイア）は、株式会社テトラフェイスが[開発](../Page/開発.md "wikilink")・[販売](../Page/販売.md "wikilink")している[Windowsおよび](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用[3DCGソフトウェア](https://ja.wikipedia.org/wiki/3DCGソフトウェア "wikilink")である。略称は**メタセコ**または**metaseq**。無償で提供されているが、ライセンスを購入してシリアルIDを入力するまでは機能が制限される。

Metasequoia 4以降にはStandard版と高機能なEX版がある。Ver3.1以前は通常版と無償版のLEがあるが、現在はVer3.1のライセンスを購入することはできない。

本項では、開発・販売元の**株式会社テトラフェイス**についても解説する。

## 概要

[1999年](../Page/1999年.md "wikilink")5月の初版リリース時から**O.Mizno**（水野修）が個人事業で開発やサポートを行っていたが、[2012年](../Page/2012年.md "wikilink")5月から法人化の準備を進め、同年9月に株式会社テトラフェイスを設立\[1\]\[2\]。Metasequoia上の表記は2012年10月公開のVer3.1 Beta7から法人名となった。なお、公式[ブログ](../Page/ブログ.md "wikilink")では「法人になったからといって開発や販売体制など実質的な面では何も変わらない」（2012年10月時点）と説明している\[3\]。

ポリゴンメッシュによる3Dモデルの作成（[モデリング](https://ja.wikipedia.org/wiki/モデリング "wikilink")）に特化した3DCG[モデラー](../Page/モデラー.md "wikilink")である。

3DCGモデラーとしての機能性や扱いやすさ、入手のしやすさなど、日本における3DCGモデラーとして人気が高い。データ可搬性を重視しており、様々なファイル形式で入力・出力することができる。低価格であり、趣味で使用する個人ユーザーが多いが、プロが製作現場で使用することもある。採用段階でMetasequoiaの使用経験を認める企業もある\[4\]\[5\]。

Metasequoia 4.3でボーン\[6\]に、4.5でモーフ\[7\]に標準対応するなど、これまでプラグインや別の統合ソフトと連携しなければ実現できなかった高度な機能も実装され始めている。なお、ボーンやモーフの追加情報は、モデルデータであるMQOファイルではなく、拡張用の外部MQXファイル（[XMLフォーマット](../Page/Extensible_Markup_Language.md "wikilink")）に保存される。

なお、Metasequoia自体は初版から[C++ Builderを使って開発されていることが](../Page/C++_Builder.md "wikilink")、公式ブログなどで言及されている\[8\]\[9\]。

## プラグイン/スクリプト

開発者向けに[C++](../Page/C++.md "wikilink")用プラグインSDKを公開しており、[シェアウェア](../Page/シェアウェア.md "wikilink")版では外部開発者による[プラグイン](../Page/プラグイン.md "wikilink")を利用することができるようになっている。32bit版のプラグインは64bit版のアプリケーションでは使用することができない。その逆もまた然りである。

プラグインのインターフェイス自体は基本的に後方[互換性](../Page/互換性.md "wikilink")を持っているため、古いバージョンのSDKで作成されたプラグインであっても新しいバージョンのMetasequoiaで利用可能である。しかしMetasequoia 3.x以前は64bit版が存在しなかったり\[10\]、多角形ポリゴン (NGon)に未対応であった\[11\]ため、3.x以前のプラグインにもその制限が引き継がれている。

また、組込マクロ言語として[Python](../Page/Python.md "wikilink")を採用しており、簡単なバッチ処理などであればプラグインを作成・使用せずともPythonスクリプトを記述して実行することで素早く実現できるようになっている。Ver4.6.9時点でPython 3.6.7に対応\[12\]。各種モジュールを使用するにはそれぞれ対応する日本語版Windows用Pythonを別途インストールする必要がある。

## レンダリング

Metasequoiaにはレンダリング機能としてスキャンライン及び[レイトレーシング](../Page/レイトレーシング.md "wikilink") (Ver4.0以降) が搭載されているものの、本格的なレンダリングや動画の作成を行う場合には外部のレンダラーを使用する必要がある。

Metasequoia Ver4.5以降は[ピクサーの提供するレンダラーである](https://ja.wikipedia.org/wiki/ピクサー・アニメーション・スタジオ "wikilink")[RenderMan](../Page/RenderMan.md "wikilink")との連携機能を使うことができる\[13\]。RenderManは非商用に限って無料で使用することが可能となっている\[14\]。

またオープンソースのレンダラーである[LuxCoreRenderのメタセコイア用プラグインのテスト版もテトラフェイスより提供されている](https://ja.wikipedia.org/wiki/LuxRender "wikilink")\[15\]。

### 過去のレンダラー

以前は以下の外部提供レンダラーが使われていた。

  - [vidro](https://ja.wikipedia.org/wiki/vidro "wikilink")\[16\]

  - [Parthenon Renderer](https://ja.wikipedia.org/wiki/Parthenon_Renderer "wikilink") [1](http://www.bee-www.com/parthenon/)

  - [Warabi MP](https://ja.wikipedia.org/wiki/Warabi "wikilink")\[17\]

  - [POV-Ray](../Page/POV-Ray.md "wikilink")\[18\] - 関連ソフトウェアのMetaMegaを通して使用可能

  - \- 関連ソフトウェアのMetaSceneを通して使用可能

  - Lightflow - 関連ソフトウェアのMetalight2やMATSpiderを通して使用可能

  - [Redqueen](https://ja.wikipedia.org/wiki/Redqueen "wikilink")\[19\]\[20\]\[21\] - プラグインのrrtdlgMQを通して使用可能

## キャラクターアニメーション

Metasequoiaは長らくボーンやモーフなどのキャラクターアニメーション向け機能を搭載していなかった。アントラッドはMetasequoia向けキャラクターアニメーションツールとして[Mikoto](https://ja.wikipedia.org/wiki/Mikoto "wikilink")をリリースしたが、2003年のMikoto 0.4fを最後にその更新を停止した。その後、mqdlは、[Mikoto](https://ja.wikipedia.org/wiki/Mikoto "wikilink")の後継として、Metasequoia用のキャラクターアニメーションプラグインKeynoteをリリースした。

2008年、樋口優によりキャラクターアニメーションソフトウェアの[MikuMikuDance](https://ja.wikipedia.org/wiki/MikuMikuDance "wikilink") (MMD)がリリースされると、MMD用モデルの製作のためにMetasequoiaとPMDエディタ/PMXエディタの組み合わせが使われるようになった。2011年、MikuMikuDanceの開発終了が宣言され、MikuMikuDanceのクローンソフトウェアが多数登場した。

その後、Metasequoiaはバージョン4.xでボーンやモーフに直接対応し、MMD用のテンプレートも付属するようになった。

## バージョン変遷

  - 1999年5月10日 Metasequoia Ver1.0 \[22\]
  - 2000年5月3日 Metasequoia LE Ver2.0
  - 2000年5月4日 Metasequoia Ver2.0
  - 2000年10月17日 Metasequoia Ver2.1.0
  - 2001年7月22日 Metasequoia Ver2.2.0
  - 2003年10月11日 Metasequoia Ver2.3.0
  - 2006年7月25日 Metasequoia Ver2.4.0
  - 2012年4月29日 Metasequoia Ver3.0.0
  - 2012年10月25日 Metasequoia Ver3.1.0
  - 2013年9月30日 Metasequoia 4\[23\]
  - 2014年1月24日 Metasequoia 4.1.0\[24\]
  - 2014年1月29日 Metasequoia 3.1.6(バージョン3系最後のリリース)\[25\]
  - 2014年6月4日 Metasequoia 4.2.0\[26\]
  - 2014年9月30日 Metasequoia 4.3.0\[27\]
  - 2015年2月13日 Metasequoia 4.4.0\[28\]
  - 2015年7月8日 Metasequoia 4.5.0\[29\]
  - 2016年3月28日 Metasequoia 4.5.5(macOS版の初リリース)\[30\]
  - 2017年08月21日 Metasequoia 4.6.0\[31\]
  - 2019年04月24日 Metasequoia 4.7.0\[32\]
  - 2020年05月18日 Metasequoia 4.7.4b\[33\]
  - 2020年07月7日 Metasequoia 4.7.4c\[34\]

## モデルコンテスト

2004年7月に、Metasequoiaに収録するサンプル用モデルデータを募集するため、モデルコンテスト2004が開催された。告知から応募締め切りまで1か月しか無かった上、MQOファイルとテクスチャ用ファイルを圧縮して1MB以内であること等の制約があったが、40件近い応募があった。現在Metasequoiaに収録されているサンプルモデルの内、日本橋麒麟像(NihonbasiKirin)、Tank、魔道少女(witch)、violin、meka、kame の6つは、このコンテストの最優秀賞および入賞作品である。

なお、このモデルコンテストの表題には2004と付いているが、コンテストが行われたのは2010年現在、まだこの1回のみである。

## 関連ソフトウェア

### モーション / アニメーション

  - 現行

<!-- end list -->

  - [MikuMikuDance](https://ja.wikipedia.org/wiki/MikuMikuDance "wikilink") - Metasequoia 4.xでPMD形式のエクスポートに標準対応
  - Vixer Motion [2](https://vixar.jp/motion/index.html) / Vixar TransMotion [3](https://vixar.jp/transmotion/)

<!-- end list -->

  - 過去 (3.x以前)

<!-- end list -->

  - [Mikoto](https://ja.wikipedia.org/wiki/Mikoto "wikilink")\[35\]
  - エルフレイナ [4](https://sorceryforce.net/elfreina/)
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

1.
2.
3.
4.
5.  [ゲームエフェクトデザイナー（アートディレクター候補）](http://jobinjapan.jp/job-listing/J24352.html)　JOBinJAPAN　2014年11月28日観覧
6.  [metaseq.net blog: Metasequoia 4.3の新機能(1) ボーン](http://blog.metaseq.net/2014/10/metasequoia-431.html)
7.  [Metasequoia 4.5の新機能：モーフ機能のチュートリアル | metaseq.net](http://www.metaseq.net/jp/archives/278/)
8.  [C++Builder 2009](http://metaseq.sblo.jp/article/18463741.html)　metaseq.net blog（旧公式ブログ）　2008年08月27日
9.  [C++BuilderXEへ移行中](http://metaseq.sblo.jp/article/45935261.html)　metaseq.net blog（旧公式ブログ）　2011年06月12日
10.
11. [エディション間比較](https://www.metaseq.net/jp/feature/version/)
12.
13. [Metasequoia 4.5の新機能：RenderMan連携機能のチュートリアル | metaseq.net](http://www.metaseq.net/jp/archives/280/)
14. [Pixar ships RenderMan 23.3](http://www.cgchannel.com/2020/05/pixar-ships-renderman-23-0/) CG Channel 2020年5月20日
15. [LuxCoreRender Bridge for Metasequoia 4](https://metaseq.net/software/luxcore.html) テトラフェイス
16. 『メタセコイア4 マスターブック 3DCGモデリングの基本と応用』 海川メノウ 2013年12月20日 ISBN 978-4877833190
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.