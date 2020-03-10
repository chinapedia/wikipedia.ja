> この記事は[Windows Media](https://ja.wikipedia.org/wiki/Windows_Media)から翻訳されています。


**Windows Mediaメタファイル** (Windows Media Metafile) は、[Windows Media Player](https://ja.wikipedia.org/wiki/Windows_Media_Player "wikilink") (WMP) 用の[ストリーミング](../Page/ストリーミング.md "wikilink")・[メディア](../Page/メディア.md "wikilink")・[メタファイル](https://ja.wikipedia.org/wiki/メタファイル "wikilink")。

## 内容

[ASF](https://ja.wikipedia.org/wiki/Advanced_Systems_Format "wikilink")、[WMA](https://ja.wikipedia.org/wiki/Windows_Media_Audio "wikilink")、[WMVなど](https://ja.wikipedia.org/wiki/Windows_Media_Video "wikilink")[メディアファイル](https://ja.wikipedia.org/wiki/メディアファイル "wikilink")（[音声ファイル](https://ja.wikipedia.org/wiki/音声ファイル "wikilink")、[動画ファイル](https://ja.wikipedia.org/wiki/動画ファイル "wikilink")）の[URLが](../Page/Uniform_Resource_Locator.md "wikilink")、[XMLで記述されている](../Page/Extensible_Markup_Language.md "wikilink")。URLは複数記述することができ、順に再生されたり、条件選択されたりする。

メディアファイルのURL以外に、再生制御のための情報、[ウェブページ](../Page/ウェブページ.md "wikilink")のURL、[著作権](../Page/著作権.md "wikilink")情報、タイトルなど[テキスト情報](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")、[バナー](../Page/バナー.md "wikilink")や[アイコン](../Page/アイコン.md "wikilink")（メタデータではなく実体）などを記述することができる。

## 用途

[ストリーミング](../Page/ストリーミング.md "wikilink")配信で使われる。メタファイルを開いたWMPなどの[プレイヤは](https://ja.wikipedia.org/wiki/メディアプレイヤ "wikilink")、メタファイルに記載されたURLにアクセスし、メディアファイルをストリームとして[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")し再生する。

ただし通常は、プレイヤでメタファイルを直接開くことは少ない。メタファイルは[ウェブ上で公開される](https://ja.wikipedia.org/wiki/ワールドワイドウェブ "wikilink")。[ブラウザがメタファイルにアクセスすると](../Page/ウェブブラウザ.md "wikilink")、ブラウザはプレイヤを起動し、メタファイルの（またはローカルに保存したそのコピーの）URLを与える。

もちろん、ブラウザの右クリックなどで保存したメタファイルをプレイヤで開いたり、プレイヤの「URLを開く」メニューを使うなどしても、同様に再生できる。

送信側では、[HTMLで](../Page/HyperText_Markup_Language.md "wikilink")<a>タグを使って

    <a href="metafile.asf">ストリームの説明</a>

のように記述する。ほかに、

<embed>

タグを使う方法もある。

## 拡張子の違い

ASX (Advanced Stream Redirector) 、WAX (Windows Media Audio Redirector)、WVX (Windows Media Video Redirector)の3種類の[規格がある](../Page/ファイルフォーマット.md "wikilink")。

|     | 拡張子  | MIMEタイプ        | ASF | WMA | WMV | 対応WMP  |
| --- | ---- | -------------- | --- | --- | --- | ------ |
| ASX | .asx | video/x-ms-asf | ○   | ×   | ×   |        |
| WAX | .wax | audio/x-ms-wax | ○   | ○   | ×   | WMP7以降 |
| WVX | .wvx | video/x-ms-wvx | ○   | ○   | ○   | WMP7以降 |

ただし、使用できるメディアファイルの種類以外に違いはない。また実際は、メディアファイルの種類が拡張子やMIMEタイプと食い違っていても、ほとんどのプレイヤーは正常に再生できる。このためこれらの規格は、事実上同一とみなされ、一括して論じられることが多い。

なお、ASXのMIMEタイプはvideo/x-ms-asxではなく、（ASFと同じ）video/x-ms-asfである。

## 脆弱性

一部のタグを悪用することで、WMPに任意のウェブページを表示させることができる。これは、不審なメタファイルであり、このようなメタファイルはいったんローカルに保存し、[テキストエディタ](../Page/テキストエディタ.md "wikilink")で確認することで回避できる。

## 外部リンク

  - [Windows Media™ メタファイルの活用](http://www.microsoft.com/japan/msdn/windowsmedia/production/asx.aspx)（マイクロソフト）
  - [Windows Media Playerのメタファイルに危険性](http://www.itmedia.co.jp/news/articles/0709/20/news018.html)

[Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:Windows_Media](https://ja.wikipedia.org/wiki/Category:Windows_Media "wikilink")