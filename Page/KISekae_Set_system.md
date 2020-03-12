> この記事は[KISekae Set system](https://ja.wikipedia.org/wiki/KISekae_Set_system)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:fkiss.png "wikilink") **KISekae Set system** (着せ替えセットシステム、**KISS**)\[1\] とは当初仮想「[紙人形](https://ja.wikipedia.org/wiki/着せ替え人形#紙製のもの "wikilink")」を作るために設計された、[アートと](../Page/芸術.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")の融合である。コンピュータを通じて作成したり表示したりする伝統的なアートである「[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")」とは異なり、KISSはコンピュータを[メディアとして使い](../Page/メディア_\(媒体\).md "wikilink")、[アニメーション](../Page/アニメーション.md "wikilink")するばかりでなく、双方向のアートを可能にする。

## 動作環境

KISSは[オープンスタンダード](https://ja.wikipedia.org/wiki/オープンスタンダード "wikilink")であり、何種類かの[PDAを含むほとんどすべての](../Page/携帯情報端末.md "wikilink")[プラットフォームにある程度実装されてきた](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")やWebページ\[2\]による実装も存在する。

## 歴史

KISSは1991年、[少女漫画](../Page/少女漫画.md "wikilink")の[キャラクター](../Page/キャラクター.md "wikilink")に基づく"人形"とともに[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")で始まった。

最初の人形は互いの周囲や前後に重ねて動かすことができ、あたかも人形の画像が服を着ているように見える、単純で静的な画像の集まりだった。コンピュータグラフィックスを使うことにより、視覚的には離れた部品を含む複数の[レイヤを同時に動かして物理的な紙では不可能な奥行きがあるように見せかけられるという点で](../Page/レイヤー_\(DTP\).md "wikilink")、伝統的な紙人形より優れていた。

初期の表示ソフトウェアは[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")向けに設計されており、16色の[パレットで人形を表示していた](../Page/インデックスカラー.md "wikilink")。ほどなく、[VGA](../Page/Video_Graphics_Array.md "wikilink")[ビデオカード](../Page/ビデオカード.md "wikilink")と256色や複数の16色パレットのサポートを含む、機能強化された標準 ('KISS/GS2'として知られる**General Specification 2**\[3\]) が提唱された。この標準はまだKISSに基づいていたが、その後いくつかの追加仕様、とくに双方向性とアニメーションを制御する "French KISS" (通称fkiss\[4\]) と32[ビット](../Page/ビット.md "wikilink")[トゥルーカラーをサポートする](../Page/フルカラー.md "wikilink") "Cherry Kiss" (通称ckiss\[5\]) がビューアに組み込まれた。

1990年代後半に、KISSは日本の[BBS](../Page/電子掲示板.md "wikilink")[コミュニティ](https://ja.wikipedia.org/wiki/コミュニティ "wikilink")から[インターネット](../Page/インターネット.md "wikilink")を通して「人形」を作成するアーティスト、サポートツールを作成するプログラマ、そして世界中に現れたファンとともに国際的に広がった。

KISSセットはしばしば '人形' と一般に呼ばれるが、着せ替えとは限らないことに注意されたい。実際にはあらゆるものが可能であり、[福笑い](../Page/福笑い.md "wikilink")、ウェディングケーキ、[ドールハウス](../Page/ドールハウス.md "wikilink")、[戦艦](https://ja.wikipedia.org/wiki/戦艦 "wikilink")、そればかりか[パズル](../Page/パズル.md "wikilink")、[ゲーム](../Page/ゲーム.md "wikilink")、他にもたくさんのものが存在する。このような人形以外のセットを、英語圏では 「aberrant KiSS」（異常なKISS）と呼ぶことがある。

## 形式

KISSセットはさまざまな異なった形式の、多数の[ファイルからなる](../Page/ファイル_\(コンピュータ\).md "wikilink")。これらは[LZH](https://ja.wikipedia.org/wiki/LZH "wikilink")形式 (日本における推奨[アーカイブ](../Page/アーカイブ.md "wikilink")形式) で単独の「人形」として配布用にパッケージされる。ビューアプログラムはLZH形式から個々のファイルをまとめて取得できる。

ほとんどのファイルはアニメーション[セルに似た生の未](../Page/セル画.md "wikilink")[圧縮画像](../Page/データ圧縮.md "wikilink")[データ](../Page/データ.md "wikilink")'セル'ファイルである。 KISS/GS2仕様のセルはKCF (KISSカラーファイル) もパレットとして必要とするが、ckiss仕様セルには必要ない。KCFは背景色の制御もでき、明るさと色を変化させる効果のために入れ替え可能な複数のパレットを含む。KISS/GS2以降のすべてのKISS[バイナリ](../Page/バイナリ.md "wikilink")ファイル (KCF、標準セル、ckissセル) は共通の32バイトバイナリヘッダレコードを持ち、サイズ、種類、および含まれているKISSデータの形式を識別する。

フィールドサイズ、重ね合わせ、セルの位置、パレットの使用、そして対話的操作やアニメーションの[イベントを制御するために](../Page/イベント_\(プログラミング\).md "wikilink")[設定ファイル](../Page/設定ファイル.md "wikilink")も必要である。

加えて音楽用の[MIDI](../Page/MIDI.md "wikilink")ファイルと効果音用の[WAV](../Page/WAV.md "wikilink")ファイルが使え、一般には何らかの形で作者が[テキスト](../Page/テキストファイル.md "wikilink")[文書](../Page/文書.md "wikilink")も含めている。

### 追加セット

KISSセットは「追加セット」と呼ばれる過程により、他のKISSセットから[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")を獲得することが許されている。これによりもとのセルを新しいセットに組み込むことなく、新しい[バージョン](https://ja.wikipedia.org/wiki/バージョン "wikilink")の人形が作れるようになった。これは以前のバージョンを置き換える必要がなくなり、原作者が誰であるかの混乱を招くことなく異なる作者が人形にデータを追加できるということを意味する。この機能はもっとも初期のビューアまでさかのぼれるが、追加セットの読み込みの詳細には多少ビューア依存の点が残っている。

## 拡張

多数の機能がKISSに追加されてきたが、メインKISS[形式へ公式に組み込まれたものは](../Page/ファイルフォーマット.md "wikilink")1つもない。[互換性](../Page/互換性.md "wikilink")を維持するためと未サポートのビューアから隠すために、これらの機能は設定ファイル内で[コメントに見せかけられてきた](../Page/コメント_\(コンピュータ\).md "wikilink")。各種の拡張は (ユーザーグルーピングを除き) まず日本で導入されたが、 (Cherry Kissを除き) すべて後に国際ビューアで拡張された。

### French KISS

'French' KISS (もしくは'fkiss') はKISS/GS2仕様への実験的な追加機能として作成された[イベント駆動](https://ja.wikipedia.org/wiki/イベント駆動 "wikilink")の[スクリプト言語](../Page/スクリプト言語.md "wikilink")である。fkissはアニメーションとより優れた双方向性をKISSで可能にするため、日本で導入された。fkissは最初の拡張であり、テスト目的だけを意図していたが、そのまま有名になって固定化された。すべてのfkiss命令はその設定ファイル内の行で以下の文字列から始まる:

`;@`

";"は通常コメントの開始を示し、当初はビューアがfkissを処理しない場合に備えて処理指令を隠していたが、fkissは今やすべてのビューアで標準である。

fkiss自身も何度か拡張されてきた:

  - 'FKiSS2'\[6\]は代替プラットフォーム用のビューアを作成している国際的なプログラマによって最初に実装された。FKiSS2では衝突の検出、相対移動、および単純な条件テストが追加された。このレベルのFKiSSは非常に古いものを除き、すべてのビューアでサポートされている。これは日本でサポートされた最後のレベルとなった。
  - 'FKiSS3'\[7\]は[変数](../Page/変数_\(プログラミング\).md "wikilink")、[計算](../Page/計算.md "wikilink")、および[制御構造](../Page/制御構造.md "wikilink")を追加し、より完全なスクリプト言語に近くなった。
  - 'FKiSS4'\[8\]は、とくにユーザーグループ化のサポートによりFKiSSの能力を単純化して拡張したが、今までのところサポートしているビューアはほとんどない。

### 初期化タグ

これらは初期[プロパティ](../Page/プロパティ.md "wikilink")を制御するためのセル定義の拡張である。これらはセル定義の末尾にコメントとして現れ、直後に **%** と[コードが続く](../Page/符号.md "wikilink")。 最初の機能 (**%t** - 初期透明度の制御) は最初のレベルのfkissの最終仕様で追加された。FKiSS4で追加された他のプロパティには表示状態 (**%u**)、[クリック](../Page/クリック.md "wikilink")できるかどうか (**%g**)、およびオフセットの上書き (**%x**と**%y**)がある。

### プラグマ

これらは設定ファイルに追加されるコメントで、セットを自動表示する最善の方法をビューアプログラムに提示する。当初は日本で他のKISSセットの追加セットであることを示すために使われ (**;INCLUDE** -- すなわち、セットに含まれないリソースの検索場所)、後のビューアは読み込もうとしているセットの最適設定を示すために使った (**;HINT**)。

### Cherry Kiss

通称 'ckiss'。これはバイナリデータヘッダレコードの拡張であり、他の拡張と異なり設定ファイルには変更を加えない。ckissはセルファイルが生の24ビット色データと可変透明度のために8ビットの[アルファチャネル](https://ja.wikipedia.org/wiki/アルファチャネル "wikilink")を含めるようにする仕様である。ckissセルはパレットベースのセルと比べてディスク容量を多く使う傾向があり、圧縮もないため、ほとんどの作者は慎重に使っている。

### グループ化

テストとアニメーションのために多数のセルを制御するのを簡略化するため (もしくは特定のセルを一意に識別するため) ユーザーグループ化がFKiSS4とともに追加された。

## KISSの作成

ほとんどのプラットフォーム上に、標準的な[画像形式](https://ja.wikipedia.org/wiki/画像形式 "wikilink") (通常[BMP](../Page/Windows_bitmap.md "wikilink")、[GIF](../Page/Graphics_Interchange_Format.md "wikilink")、もしくは[PSDファイル](../Page/Adobe_Photoshop.md "wikilink")) からKISSセルとKCFファイルへの変換が可能なプログラムが多数存在する。作者はもととなる画像を任意の[フリーウェア](../Page/フリーウェア.md "wikilink")や市販の[グラフィックソフトウェア](../Page/グラフィックソフトウェア.md "wikilink")で作成できる。設定ファイルは (あらゆる[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")ソフトウェアに標準で付属する) [テキストエディタ](../Page/テキストエディタ.md "wikilink")で書かれる。ひとたび基本的なファイルを作成したら、KISSビューアが表示とセットの微調整に使われ、それからパッケージングにLZH対応の[アーカイバ](https://ja.wikipedia.org/wiki/アーカイバ "wikilink")が使われる。必要なソフトウェアはすべて、KISS作成の詳細な[チュートリアル](https://ja.wikipedia.org/wiki/チュートリアル "wikilink")と同様インターネットから無償で入手可能である。

## コミュニティ

現代のインターネット上のKISSコミュニティは[Dollz](https://ja.wikipedia.org/wiki/Dollz "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Dollz "wikilink")) コミュニティに類似していてある程度重なり合う部分もあるが、両者ははっきりと異なっており、互いに自らの作品を保護している。しかしながらKISSアートはより特殊化しているので、英語圏のKISSコミュニティはインターネットで最大の人形アーカイブであるthe BiG KiSS Pageに集中している。ただし2000年以降、回線料金のためBKPはほとんどの人形の[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")を購読者だけに認めることを余儀なくされており、アクティブなコミュニティのサイズに負の影響を与えている。

人形に服を着せられることは服を**脱がせ**られることも暗示するため、メインコミュニティとは独立に'アダルト' KISSのサブ[ジャンル](../Page/ジャンル.md "wikilink")が常に存在してきた。

[Eric Zimmermanは](https://ja.wikipedia.org/wiki/:en:Eric_Zimmerman "wikilink")、以下のようなKISSの設計が原因でKISSは脱衣ゲームになりがちであると分析している\[9\]。

  - 紙の着せ替えとは異なり、多くの人形は初期状態で衣装一式を身につけている。したがって最初の操作は必然的に服を脱がせることになる。
  - 服の移動は[ドラッグ・アンド・ドロップ](../Page/ドラッグ・アンド・ドロップ.md "wikilink")で行われる。ドラッグ・アンド・ドロップで服を脱がせるのは簡単だが、服を着せるには[ピクセル](../Page/ピクセル.md "wikilink")単位で画像の位置を合わせる必要があり非常に面倒である。しかもボタンを押すだけで10組までの衣装の組み合わせを切り替えできるので、着せ替えのために面倒な操作をする必要はない。これらの理由からドラッグ・アンド・ドロップはほとんど服を脱がせることが目的となる。

## 脚注

<references/>

## 関連書籍

  - メガハードネットワーク、「はじめてのKISS (フリーソフトライブラリ)」、[秀和システム](../Page/秀和システム.md "wikilink")（1995年4月）、ISBN 978-4879664389。

## 外部リンク

  - [Web KiSSページ](http://www.nurs.or.jp/~h_ozawa/kiss/index.html) - オンライン版のKiSSページ。（IE対応）
  - [Otaku World's Big KiSS Page](http://otakuworld.com/kiss/) - 最大のKiSS人形アーカイブと コミュニティの中心地 (英語)
  - [Kisekae World](http://kisekaeworld.com/) - Windows、Mac OS X、およびLinux用のKiSSソフトウェア開発システムKisekae UltraKissのサポートと配布サイト。(英語)
  - [KissXpress](http://www.literateweb.com/kiss/index.htm) - Web上の古い英語KISSサイトの1つ。サンプル人形、ソフトウェア、およびフリーウェアのKISS作成セットがある。 (英語)
  - [KiSSデータリスト](http://hpcgi1.nifty.com/emk/list/list.cgi)

[Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:コンピュータアート](https://ja.wikipedia.org/wiki/Category:コンピュータアート "wikilink")

1.  日本国外ではKisekae Set System (略称KiSS) とされることが多いが、正式なものではない。\[[http://www.oersted.co.jp/\~yav/sohonzan/shz.cgi?f=kisstalk\&n=770\]参照](http://www.oersted.co.jp/~yav/sohonzan/shz.cgi?f=kisstalk&n=770%5D参照)。
2.  [Web KiSSページ](http://www.nurs.or.jp/~h_ozawa/kiss/index.html) (IE対応)
3.  [KISS/GS仕様書](http://www2s.biglobe.ne.jp/~yav/kiss/kissgsj.html)
4.  [fkiss命令解説書](http://www2s.biglobe.ne.jp/~yav/soft/fkiss/tt/INDEX.HTM)
5.  [Cherry Kiss解説](http://www.oersted.co.jp/~yav/sohonzan/shz.cgi?f=kissq%26a&n=208)
6.  [FKiSS2命令リファレンス](http://www.msen.com/~crandall/fkiss.html) (英語)
7.  [FKiSS3仕様書](http://www.msen.com/~crandall/fkiss3.html) (英語)
8.  [FKiSS4リファレンス](http://tigger.orpheusweb.co.uk/KISS/fkref4.html) (英語)
9.