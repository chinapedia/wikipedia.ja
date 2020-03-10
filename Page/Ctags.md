> この記事は[Ctags](https://ja.wikipedia.org/wiki/Ctags)から翻訳されています。


**Ctags**（[英](../Page/英語.md "wikilink"): **Ctags**）はソース及びヘッダ内にある名前の[インデックス](https://ja.wikipedia.org/wiki/インデックス "wikilink")（又はタグ）ファイルを生成するプログラム。様々な[プログラミング言語](../Page/プログラミング言語.md "wikilink")に対応している。言語に依存するが、[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")(関数)、[変数](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")、[クラスのメンバ](../Page/クラス_\(コンピュータ\).md "wikilink")、[マクロ等がインデックス化される](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")。これらのタグにより[テキストエディタ](../Page/テキストエディタ.md "wikilink")などのツールで高速かつ容易に定義を参照できる。[相互参照ファイルを出力でき](https://ja.wikipedia.org/wiki/:en:cross_reference "wikilink")、また名前についての情報を[人が読みやすい形で列挙した言語ファイルを生成することもできる](https://ja.wikipedia.org/wiki/:en:human-readable "wikilink")。

**Ctags**は[Ken Arnoldが](https://ja.wikipedia.org/wiki/:en:Ken_Arnold "wikilink")[BSD Unix用に開発した](../Page/BSD.md "wikilink")。後に[Jim Klecknerにより](https://ja.wikipedia.org/wiki/Jim_Kleckner "wikilink")[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")がサポートされ、[ビル・ジョイ](../Page/ビル・ジョイ.md "wikilink")によりPascalがサポートされた。

## ctagsをサポートするエディタ

*タグインデックスファイル*は下記を含む数多くの[ソースコードエディタ](https://ja.wikipedia.org/wiki/ソースコードエディタ "wikilink")でサポートされている。

  - [AcroEdit](https://ja.wikipedia.org/wiki/AcroEdit "wikilink")
  - [BBEdit 8](https://ja.wikipedia.org/wiki/:en:BBEdit "wikilink")
  - [GNU Emacsと](https://ja.wikipedia.org/wiki/GNU_Emacs "wikilink")[XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink")
  - [EmEditor Professional](https://ja.wikipedia.org/wiki/EmEditor "wikilink")
  - [Gedit](https://ja.wikipedia.org/wiki/Gedit "wikilink") (リンク先のgedit-symbol-browser-pluginでサポート[1](http://www.micahcarrick.com/11-14-2007/gedit-symbol-browser-plugin.html))
  - [JED](https://ja.wikipedia.org/wiki/:en:JED_\(text_editor\) "wikilink")
  - [jEdit](https://ja.wikipedia.org/wiki/jEdit "wikilink") (CodeBrowser、Tags、ClassBrowser、CtagsSideKick、Jumpのプラグインでサポート。)
  - [JOE](https://ja.wikipedia.org/wiki/:en:Joe's_Own_Editor "wikilink")
  - [KDevelop](../Page/KDevelop.md "wikilink")
  - [KATE](https://ja.wikipedia.org/wiki/KATE "wikilink") (右記リンク先のkate-ctags-pluginでサポート[KDE-apps](http://www.kde-apps.org))
  - [NEdit](https://ja.wikipedia.org/wiki/:en:NEdit "wikilink")
  - [Notepad++](https://ja.wikipedia.org/wiki/Notepad++ "wikilink") (OpenCTagsプラグインでサポート)
  - [Programmer's Notepad](https://ja.wikipedia.org/wiki/:en:Programmer's_Notepad "wikilink")
  - [QDevelop](https://ja.wikipedia.org/wiki/QDevelop "wikilink")
  - [TextMate](https://ja.wikipedia.org/wiki/:en:TextMate "wikilink") (CodeBrowser-PlugInでサポート)
  - [UltraEdit](https://ja.wikipedia.org/wiki/:en:UltraEdit "wikilink")
  - [VEDIT](https://ja.wikipedia.org/wiki/:en:VEDIT "wikilink")
  - [Vi](../Page/Vi.md "wikilink") (及び[Elvis](https://ja.wikipedia.org/wiki/:en:Elvis_\(text_editor\) "wikilink")、[Nvi](https://ja.wikipedia.org/wiki/Nvi "wikilink")、[Vim](../Page/Vim.md "wikilink")、[vile等の派生版](https://ja.wikipedia.org/wiki/:en:Vile_\(editor\) "wikilink"))
  - [ViVi](https://ja.wikipedia.org/wiki/ViVi_\(エディタ\) "wikilink")
  - [Zeus IDE](https://ja.wikipedia.org/wiki/:en:Zeus_for_Windows "wikilink")

## ctagsの派生版

*ctags*にはいくつかの派生版が存在する。

### Etags

**Etags**はEmacs上で動作するctagsである。ctagsが生成する[Vi](../Page/Vi.md "wikilink")フォーマットのタグファイル用にのみ意味のあるオプションはetagsでは解釈されず無視される。

### Exuberant Ctags

[Darren Hiebertが開発した](https://ja.wikipedia.org/wiki/Darren_Hiebert "wikilink")**Exuberant Ctags**は元々[Vim](../Page/Vim.md "wikilink")と共に配布されていたが、Vim 6のリリースに合わせて独立したプロジェクトになった。\[1\] Emacs互換機能をサポートしている。

Exuberant Ctagsは[正規表現](../Page/正規表現.md "wikilink")を用いることにより数多くのプログラミング言語に対応でき、30以上の言語に対応している。

## タグファイルのフォーマット

複数のタグファイルフォーマットがある。その一部を以下で説明する。説明中の\<\\x\#\#\>は16進数でバイトを表している。

### Ctagsフォーマット及びExuberant Ctagsフォーマット

オリジナルの*ctags*フォーマットと**Exuberant Ctags**フォーマットはファイルフォーマットが似ている。\[2\]

#### Ctagsフォーマット

エディター「vi」系用のフォーマット。タグファイルは通常は `tags` という名前である。

タグファイルは行単位でフォーマットされている。

    {タグ名}<Tab>{タグファイル}<Tab>{タグアドレス}

各フィールドは以下のように定義される。

| 記述                | 定義                                                                                    |
| ----------------- | ------------------------------------------------------------------------------------- |
| nowrap|`{タグ名}`    | 識別子。空白は含まれない。                                                                         |
| nowrap|<Tab>      | [タブ文字](https://ja.wikipedia.org/wiki/タブキー "wikilink")。vi系では複数の空白を取り扱えるが、一文字のみしか許されない。 |
| nowrap|`{タグファイル}` | `{タグ名}` が定義されているファイルの名前であり、カレントディレクトリからの相対パス。                                         |
| nowrap|`{タグアドレス}` | エディタをタグ位置に移動するラインエディタ用の ex コマンド。*vi*のPOSIX実装では検索又は行番号となる。                             |

タグファイルの検索を高速にするためタグファイルは `{タグ名}` のフィールドでソートされる。

#### Exuberant Ctagsフォーマット

[Vim](../Page/Vim.md "wikilink")用のフォーマット。後方互換性のため出力フォーマットとしてオリジナルの*ctags*フォーマットと拡張フォーマットを選択できる。

各フィールドは以下のように定義される。

    {タグ名}<Tab>{タグファイル}<Tab>{タグアドレス}[;"<Tab>{タグフィールド}...]

{タグアドレス}までのフィールドは上記の[ctagsと同じである](https://ja.wikipedia.org/wiki/#Ctags "wikilink")。

拡張フィールド

  - `;"` – セミコロンとダブルコーテーション。vi のコメントと同じ表記により{タグアドレス}を終了させる。
  - `{タグフィールド}`

拡張フォーマットでは ex コマンドの後ろに ex コメントを続ける形でオリジナルの vi の実装との下位互換性を維持したままで{タグアドレス}フィールドを拡張できる。これらの拡張フィールドはタブで区切られたキー・バリューのペアである。詳細は[ctagsのマニュアル](http://ctags.sourceforge.net/ctags.html)を参照のこと。

### Etagsフォーマット

Emacs用の `etags` のフォーマット。タグファイルは通常は `TAGS` という名前である。

`etags` のファイルは複数のセクションで構成されている。入力ソースファイル毎に1つのセクションを持つ。各セクションはプレーンなテキストファイルであるが、特別な制御用にアスキー外の文字を使用する。以下の説明においてこれらの文字は\<\>で囲まれた16進数のコードで表す。

セクションは2行のヘッダで始まる。1行目は`<\x0c>`一文字のみを含む。2行目は次のようになる。

    {ソースファイル<},{タグ定義データのバイト数}

ヘッダの後にはタグの定義が続く。各定義毎に1行。フォーマットは以下の通り。

    {タグ定義テキスト}<\x7f>{タグ名}<\x01>{行番号},{バイトオフセット}

タグ定義よりタグの名称が導き出せる場合は`{タグ名}` とその後ろの `\x01` が無視される。

#### 例

ソースコードとして次のような1行だけのtest.cを読み込ませた場合、

``` c
#define CCC(x)
```

`TAGS` ファイルは次のようになる。

    <\x0c>
    test.c,21
    #define CCC(<\x7f>CCC<\x01>1,0

## 参考文献

<references />

## 外部リンク

  - [Exuberant ctagsのホームページ](http://ctags.sourceforge.net/)
  - [VMS用のCtags](http://polarhome.com/ctags/?lang=en)
  - [Emacsのvtags.elモジュールのソースコード](http://cvs.savannah.gnu.org/viewvc/vtags/vtags/vtags.el?view=markup)

[Category:フリープログラミングツール](https://ja.wikipedia.org/wiki/Category:フリープログラミングツール "wikilink") [Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")

1.  [:en:Template:Cite web](https://ja.wikipedia.org/wiki/:en:Template:Cite_web "wikilink")
2.  [:en:Template:Cite web](https://ja.wikipedia.org/wiki/:en:Template:Cite_web "wikilink")