> この記事は[Scribes](https://ja.wikipedia.org/wiki/Scribes)から翻訳されています。


**Scribes**（スクライブス）は、[GNOME](../Page/GNOME.md "wikilink")デスクトップの[テキストエディタ](../Page/テキストエディタ.md "wikilink")。その他フリーのデスクトップ環境（[KDE](../Page/KDE.md "wikilink")、[Enlightenment](https://ja.wikipedia.org/wiki/Enlightenment "wikilink")、[XFCE](https://ja.wikipedia.org/wiki/XFCE "wikilink")など）でも使用できる。

## 設計思想

仕事の流れの阻害を最小限にすること、おもしろみのない作業を自動化すること、不要な設定変更をなくすこと、シンプルさに基づいた理性的な編集作業を達成することを目標にしている。この目標を達成するために必要のない慣習は守っていない。

## 特徴

以下に Scribes の特徴の一部を挙げる：

  - Snippet （[スニペット](https://ja.wikipedia.org/wiki/スニペット "wikilink")）と呼ばれる動的なテンプレートシステム
  - 自動的に単語を補完する
  - 自動的にカッコを補完、スマートな挿入
  - 自動保存
  - 自動インデント
  - ブックマーク機能
  - いくつかの言語のエンコーディングをサポート
  - ドラッグ・ドロップ
  - 外国語テキストのフルサポート
  - 30 以上の言語のハイライト表示
  - パワフルな GNOME との連携
  - ドイツ語、ロシア語、フランス語、イタリア語、ポルトガル語の翻訳

## 必要なソフトウェア

Scribes を使用するには、以下のソフトが必要：

  - Yelp
  - Python
  - GNOME Python Extras

Scribes は [Python](../Page/Python.md "wikilink") により実装されている。

## 使い方

### ファイル操作

#### 新規ファイル

新規ファイルを開くには、ツールバーから New ボタンを押すか、Ctrl-N 。 名前を付けて保存するには、Save As ボタンを押すか、Ctrl-Shift-S。

#### ファイルを開く

既存のファイルを開くには、ツールバーから Open ボタンを押すか、Ctrl-O。

#### ファイルを保存

ファイルを保存するには、Ctrl-S。ファイルに変更があったとき、ウィンドウを閉じるときには自動で保存される。

#### 印刷

ファイルを印刷するには、ツールバーから Print ボタンを押すか、Ctrl-P。

### テキスト操作

#### 元に戻す

元に戻すには、ツールバーから Undo ボタンを押すか、Ctrl-Z。

#### やり直し

やり直すには、ツールバーから Redo ボタンを押すか、Ctrl-Shift-Z。

#### 選択

下のショートカット・キーを参照。

#### 切り取り

Ctrl-X。

#### コピー

Ctrl-C。

#### 貼り付け

Ctrl-V。

#### 検索

テキストを検索するには、[ツールバー](https://ja.wikipedia.org/wiki/ツールバー "wikilink")から Search ボタンを押し、[ステータスバー](../Page/ステータスバー.md "wikilink")の上に現れるボックスに検索したいテキストを入力する。Next ボタンと Previous ボタンでそれぞれ次の候補、前の候補に移動できる。

#### 置換

テキストを置換するには、ツールバーから Replace ボタンを押し、ステータスバーの上に現れる Search for ボックスに置換したいテキストを入力する。Enter を押すと、すべての候補がハイライトされる。Next ボタンと Previous ボタンでそれぞれ次の候補、前の候補に移動できる。置換したいテキストを Replace with ボックスに入力して、置換したい候補のところで、Replace with ボタンを押すとテキストの置換が行われる。すべての候補を置換したい場合は、Replace all ボタンを押す。

#### 指定行にカーソルを移動

指定行にカーソルを移動するには、ツールバーから GOTO ボタンを押し、指定行を入力する。

### 設定

エディタの設定を行うには、ツールバーから Preferences ボタンを押すか、Ctrl-Alt-P。

#### フォント

使用したいフォントを選択。

#### タブ

Tab キーを押したときのタブ幅を指定。

#### ラッピング

Enable text wrapping をオンにするとウィンドウの境界にテキストが来たときにラッピングを行う。

#### 右のマージン

Display right margin をオンにすると右のマージンを示す縦のラインが表示される。

#### スペルチェック

Enable spell checking をオンにするとスペルチェックができるようになる。

### ショートカット・キー

#### ファイル操作のショートカット・キー

  - Ctrl-N 新規ファイルの作成
  - Ctrl-O ファイルを開く
  - Ctrl-S ファイルの保存
  - Ctrl-Shift-S 名前を付けて保存
  - Ctrl-P 印刷
  - Ctrl-W ファイルを閉じる
  - F1 ヘルプを表示
  - F6 スペルチェックを有効にする
  - F12 設定を表示

#### テキスト操作のショートカット・キー

  - Ctrl-X 切り取り
  - Ctrl-C コピー
  - Ctrl-V 貼り付け
  - Ctrl-Z 元に戻す
  - Ctrl-Shift-Z やり直し
  - Ctrl-T 行のインデント
  - Ctrl-Shift-T 行のアンインデント（ディデント）
  - Ctrl-A すべて選択
  - Ctrl-B 対応するカッコを探す
  - Ctrl-D 行をブックマーク
  - Alt-Delete ブックマークの解除
  - Alt-Left 前のブックマークに移動
  - Alt-Right 次のブックマークに移動
  - Alt-Shift-Delete すべてのブックマークを削除
  - Alt-D 行の削除
  - Alt-J 行をつなぐ
  - Alt-W 単語を選択
  - Alt-L 行を選択
  - Alt-S 一文を選択
  - Alt-B カッコの中のテキストを選択
  - Alt-Up 選択されたテキストを小文字から大文字に変更
  - Alt-Down 選択されたテキストを大文字から小文字に変更
  - Alt-Shift-Down 選択されたテキストの大文字と小文字をスワップする
  - Alt-Shift-Up 選択されたテキストを大文字にする
  - Alt-P パラグラフを選択
  - Alt-R 行末の不要なスペースを削除
  - Alt-Shift-R 行頭の不要なスペースを削除
  - Alt-End カーソルから行末までのテキストを削除
  - Alt-Home カーソルから行頭までのテキストを削除
  - Alt-Shift-T タブをスペースに変換
  - Alt-O 現在の行の上に新しい行を挿入
  - Alt-Shift-O 現在の行の下に新しい行を挿入
  - Shift-End カーソルから行末までのテキストを選択
  - Shift-Home カーソルから行頭までのテキストを選択
  - Shift-F10 エディタのポップアップ・メニューを表示

#### 一般操作のショートカット・キー

  - Home カーソルを行頭に移動
  - End カーソルを行末に移動
  - Ctrl-Home カーソルを最終行に移動
  - Ctrl-End カーソルを一行目に移動
  - Ctrl-Right カーソルを次の単語まで移動
  - Ctrl-Left カーソルを前の単語まで移動
  - Page Up カーソルを一ページ上に移動
  - Page Down カーソルを一ページ下に移動
  - Delete カーソルの後の文字を削除
  - Insert エディタのモードを変更。挿入モードか上書きモードになる。
  - Backspace カーソルの前の文字を削除

#### ウィンドウ操作のショートカット・キー

  - Alt-F4 エディタのウィンドウを閉じる
  - Alt-F5 エディタのウィンドウを非最大化する
  - Alt-F7 エディタのウィンドウを移動する
  - Alt-F8 エディタのウィンドウの大きさを変える
  - Alt-F9 エディタのウィンドウを最小化する
  - Alt-F10 エディタのウィンドウを最大化する
  - Alt-Space エディタのウィンドウ・メニューを有効にする
  - Alt-Tab ポップ・アップでウィンドウ間の移動
  - Alt-Shift-Tab ポップ・アップでウィンドウ間を逆方向に移動

## ライセンス

Scribes は [GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") でリリースされている。

## 関連項目

  - [テキストエディタの一覧](../Page/テキストエディタの一覧.md "wikilink")

## 外部リンク

  -
  - [Scirbes バグ報告ページ](http://sourceforge.net/tracker/?group_id=143967&atid=757280)

  - [Scribes フォーラム](http://sourceforge.net/forum/forum.php?forum_id=481790)

  - [Scribes メーリングリスト](https://lists.sourceforge.net/lists/listinfo/scribes-discussion)

[Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink")