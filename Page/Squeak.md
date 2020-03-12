> この記事は[Squeak](https://ja.wikipedia.org/wiki/Squeak)から翻訳されています。


**Squeak**（**スクイーク**）は[Smalltalk](../Page/Smalltalk.md "wikilink")環境のひとつで、[ゼロックス](../Page/ゼロックス.md "wikilink")が[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")当時の主要[コンピュータ](../Page/コンピュータ.md "wikilink")メーカー（[IBM](../Page/IBM.md "wikilink")、[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")、[アップルコンピュータ](../Page/アップル_\(企業\).md "wikilink")、[Tektronix](https://ja.wikipedia.org/wiki/テクトロニクス "wikilink")）にライセンス供与した[Smalltalk](../Page/Smalltalk.md "wikilink")-80の販売直前バージョン (v1) をベースに、アップルが自社の[Lisaおよび](../Page/Lisa_\(コンピュータ\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")用に開発したApple Smalltalkから派生したものである。なお、同環境に組み込まれた（Squeak Smalltalkで記述・構築されている）タイルスクリプティング言語・開発環境のSqueak [Etoys](https://ja.wikipedia.org/wiki/Etoys "wikilink")も略して「Squeak」と呼称され混同されることが多いが、両者（Squeak SmalltalkとSqueak Etoys）はプログラミング言語およびその処理系としてはまったくの別物である。

## 開発の経緯

[1970年代](../Page/1970年代.md "wikilink")の[パロアルト研究所](../Page/パロアルト研究所.md "wikilink")での俗に言う「[ダイナブック](../Page/ダイナブック.md "wikilink")プロジェクト」において、暫定Dynabook（[Alto](../Page/Alto.md "wikilink")の同チームにおける呼び名）の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) およびコンピュータ環境にあたる[Smalltalk](../Page/Smalltalk.md "wikilink")の開発にたずさわったメンバー、特にアイデアパーソンの[アラン・ケイ](../Page/アラン・ケイ.md "wikilink")、その実装者のダン・インガルスらが中心となり、当初アップルにおいて同プロジェクトは始動した。のちに[ウォルト・ディズニー・イマジニアリング](https://ja.wikipedia.org/wiki/ウォルト・ディズニー・イマジニアリング "wikilink")を経て、アラン・ケイが設立した[NPO](../Page/NPO.md "wikilink")であるに活動の拠点を移し現在も開発が続けられている。

開発の契機となる[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")ごろにはまだ[ライブラリ](../Page/ライブラリ.md "wikilink")が整っていなかった[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や、すでにいくつか存在した商業ベース[IDEとして認知](../Page/統合開発環境.md "wikilink")、発展を遂げた当時のSmalltalkには求めにくかった、自由で高度な移植性と小さいフットプリント、高機能な[マルチメディア](../Page/マルチメディア.md "wikilink")処理用ライブラリを持つことを特徴とし、それを動作させるためのOSや[プラットフォームに依存しない](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、ユーザーサイド[プログラミングを強力にサポートするコンピュータ環境を目指してその開発はスタートした](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")。

## 環境と言語

Squeakも他のSmalltalk環境同様、環境記述および[データ記述言語](../Page/データ記述言語.md "wikilink")、およびユーザースクリプティング言語としてSmalltalkを使用できるようになっている。また、非常に古い実装に基づいてはいるものの、Smalltalk環境が当初から備えていたクラスブラウザ、オブジェクトインスペクタ、[テキストエディタ](../Page/テキストエディタ.md "wikilink")、[デバッガ](../Page/デバッガ.md "wikilink")などを有機的に連動させる[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")プログラミングのための機構は、ベースとなったApple Smalltalkからそのまま環境内に引き継がれ、利用可能な状態にある。

Squeakの[仮想機械](../Page/仮想機械.md "wikilink")（Smalltalk[バイトコード](../Page/バイトコード.md "wikilink")[インタプリタ](../Page/インタプリタ.md "wikilink")）はSmalltalkのサブセットで記述されており、それを[C言語](../Page/C言語.md "wikilink")に変換するトランスレータを用いて生成される。この独特の仮想機械開発スタイルはSqueakに高い移植性をもたらしている。実際、Squeakは各種の[UNIX](../Page/UNIX.md "wikilink")、[Windowsをはじめ](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[MS-DOS](../Page/MS-DOS.md "wikilink")、[BeOS](../Page/BeOS.md "wikilink")、[TRONなど](../Page/TRONプロジェクト.md "wikilink")、[Palm OS以外のメジャーなプラットフォームに移植されており](https://ja.wikipedia.org/wiki/Palm_OS "wikilink")、めずらしいところでは、[シャープ](../Page/シャープ.md "wikilink")の[Zaurus](https://ja.wikipedia.org/wiki/Zaurus "wikilink")（旧Zaurus、もしくは最近の[Linux](../Page/Linux.md "wikilink") Zaurus）で動作するSqueak仮想機械も存在する。移植性を重視した初期の同仮想機械は、他の商用SmalltalkやJavaなどで行なわれる[動的コンパイル](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")（JITコンパイル）を欠いていたが、Eliot Miranda氏が新たに手がけたCogVMと呼ばれる次世代仮想機械では同機構も取り入れられ従来より5-10倍の性能向上を果たしている。

Squeak環境にはSmalltalkとは別に、Squeak [eToys](https://ja.wikipedia.org/wiki/Etoys "wikilink")（あるいは Etoy、SqueakToysなど）と呼ばれる[プロトタイプベース](../Page/プロトタイプベース.md "wikilink")[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")プログラミング言語・環境に近い仕組みを持つ非開発者向けプログラミング環境（タイルスクリプトシステム、あるいは単にスクリプトシステムと呼称）が実装されている。Morph（モーフ）と呼ばれる[可視化](../Page/可視化.md "wikilink")に適した機構を組み込んだオブジェクトに対し、その属性（動き、色、形、振る舞いなど）を変化させる手続きを、パネル状のパーツをドラッグ&ドロップで組み合わせで表現できる。

こうした特徴から同スクリプトシステムは、プログラミング未経験者のほかに、[キーボードの扱いに馴れていない低年齢層ユーザーにも容易に扱うことができる](../Page/キーボード_\(コンピュータ\).md "wikilink")。アラン・ケイの長年の共同研究者であるキム・ローズらは、この機構が低学年向けのコンピュータ・リテラシおよび自然科学教育に活用できることに早くから目を付け、米日独での教育機関との共同プロジェクトを立ち上げてその高い教育効果を示しつつある。

## 多言語化と日本語対応

大島が中心となって実装したSqueakの多言語拡張に基づき、阿部、梅澤、林、山宮らによってSqueakおよびSqueak eToysの[日本語](../Page/日本語.md "wikilink")化パッケージが作成された。多言語化拡張は正式版Squeakバージョン3.8以降、およびeToys用にカスタマイズされたSqueaklandバージョン2005以降に統合されており、ユーザーは正式版をダウンロードするだけで日本語を使用することができる。

## アプリケーション

Squeak（およびSmalltalk）環境においては、データもアプリケーションも、そして環境自体（つまりシステム）すら、すべてSmalltalk言語で記述されたオブジェクトで構成されているため、通常のコンピュータ環境でいうところのアプリケーションソフトという概念は希薄であるが、それでもそう呼ぶに相応しいオブジェクト群を見ることができる。

  - 開発者向け
      - Browser クラスやメソッド定義を閲覧したり、編集・追加するためのソフト
      - Inspector オブジェクトの属性を検査するためのソフト
      - Debugger インタプリタの内部状態やその推移を検査するためのソフト
      - Change Set クラスやメソッド定義に加えられた変更の履歴を管理するデータベース
      - Method Finder 任意の文字列を含むメソッド名やその定義を呼び出すツール
      - Processes プロセス閲覧・管理ツール
      - Transcript 通常の開発環境における標準出力的役割りを担うソフト
  - 一般向け
      - Workspace [WYSIWYG](../Page/WYSIWYG.md "wikilink")タイプの書き捨ての[メモ帳](../Page/メモ帳.md "wikilink")
      - GeeMail 文書と図版の共存が可能なメモ帳
      - PaintBox ペイントツール
      - Book カード型データベースおよびアクティブブック作成用のオーサリングツール
      - Stack HyperCardライクなオーサリングツール
      - File List ディレクトリ閲覧、テキストエディタ、gzip圧縮などの機能を持つファイラ
      - Zip Tool zip圧縮およびその展開を行なうためのツール
      - Scamper [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")（ただし多言語化時においても日本語使用不可）
      - Celeste メーラ（ただし多言語化時においても日本語使用不可）
      - ThreadNavigator プレゼンツール
      - Clock、Watch 時計
  - 教育向け
      - Squeak eToys タイルスクリプトシステム
      - Nebraska ネットを介した複数ユーザーのデスクトップ共有のためのシステム
      - Alice 3Dオブジェクトのオーサリングのためのシステム
  - ゲーム
      - Chess [チェス](../Page/チェス.md "wikilink")ゲーム
      - ChineseChecker
      - Cipher 暗号解読ゲーム
      - Crostic クロスワードゲーム
      - [FreeCell](../Page/フリーセル.md "wikilink") カードゲーム
      - Mines マインスイーパー
      - Same [さめがめ](../Page/さめがめ.md "wikilink")
      - Tetris [テトリス](../Page/テトリス.md "wikilink")

また、アプリケーションのような振る舞いをする大規模な機能性オブジェクト群とそれらを機能させるための最低限のオブジェクトを残して余計な部分を環境からそぎ落としてしまい、Smalltalk環境自体をまるでひとつのアプリケーションソフトであるかのように見せ、配布する形態をとることもある。Squeak公式サイトとは別に用意されたSqueaklandサイトで配布されているウェブブラウザプラグイン版のSqueakは、先のSqueak eToysに特化されたアプリケーションともいえる。

他に、Squeak環境により実現された代表的なアプリケーションと呼べるものとして有名なものにがある。SwikiはSqueak版[Wikiクローンというべきソフトの一つで](../Page/ウィキソフトウェア.md "wikilink")、同じくSqueak上にSmalltalkで書かれたHTTPサーバ（Webアプリケーションサーバ）である[Comanche](https://ja.wikipedia.org/wiki/Comanche "wikilink")上に構築されている。WikiクローンとしてのSwikiは、ファイルアップロード機能、無限差分の保持、静的[HTMLの生成などの他に](../Page/HyperText_Markup_Language.md "wikilink")、独自のフォーマットルール、キャピタルワードを自動的にリンクにする機構を持たないこと、ページ名の変更がページ作成後に可能なこと、ページソース記述にHTML表記の混在を許すことなど他の[Wikiとは一線を画す仕様を有する](../Page/ウィキ.md "wikilink")。

公式サイトである「Swiki Swiki」のダウンロードページより、Squeak eToysにおけるWebプラグイン版Squeakのように、Swikiに特化した仮想イメージと付随ファイルのアーカイブを得ることができる。日本語を扱うためには最低一箇所、修正を加えなければならないが、この仮想イメージを用いることでSmalltalk言語や環境に精通していなくとも、起動後、サーバスタートを意味するボタンを押すだけで手軽に運用を開始できる。

ただいずれも、Squeak環境としては前者はSqueak eToys、後者はSwikiに必要ないものを大幅に削除したサブセットに過ぎないので、Squeak eToysもしくはSwiki専用で、かつ、手を加えずあるがままの状態で使用するのでなければ、公式サイトより完全なSqueak環境を入手し（Swikiの場合、機能を拡張するためのパッケージをインストールした状態で）使用することが望ましい。

## 脚注

## 外部リンク

  -

  - [squeakland.org](http://squeakland.org/) Squeak eToysフィールドワークのための公式サイト

  - [squeakland.jp](http://squeakland.jp/) 上記サイトの日本語版 最新日本語版Squeakイメージが配布されている

  - [Swiki公式サイト](https://wiki.squeak.org/swiki/)Swiki公式サイト

  - 多言語化（日本語化）Squeakを[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")で使用するための情報ページ

  - [SqueakToys掲示板3](https://swikis.ddo.jp/abee/20) 日本語版Squeakで主に Squeak eToys を使用して制作された作品および情報交換のためのサイト

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:フリー教育ソフトウェア](https://ja.wikipedia.org/wiki/Category:フリー教育ソフトウェア "wikilink")