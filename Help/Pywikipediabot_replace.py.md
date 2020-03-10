> この記事は[Help:Pywikipediabot/replace.py](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/replace.py)から翻訳されています。


*In other languages:* [en](https://ja.wikipedia.org/wiki/meta:Replace.py "wikilink") - [it](https://ja.wikipedia.org/wiki/meta:Replace.py/it "wikilink") - [ja](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/replace.py "wikilink")

-----

**replace.py** は、直接文字の置換を行う汎用性の高い [Bot](https://ja.wikipedia.org/wiki/Wikipedia:Bot "wikilink") スクリプトです。XMLのダンプデータ、リストファイル、指定されたページに対して処理を行います。

このスクリプトの使用になれていない場合は、[こちらを参照してください](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/replace.py/使い方 "wikilink")。基本的な事項が書かれています。

## 引数

| 引数                 | 説明                                                                                                                                                                                           |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \-xml              | ローカルのXMLダンプから情報を取得します（[Wikipedia:データベースダウンロード](https://ja.wikipedia.org/wiki/Wikipedia:データベースダウンロード "wikilink") *を参照*）。例、「-xml:ファイル名」                                                        |
| \-page             | 特定のページを対象に追加します。複数回使用できます。例、「-page:卵かけご飯」。                                                                                                                                                   |
| \-cat              | 指定したカテゴリの全ページを対象に追加します。例、「-cat:主要カテゴリ」。                                                                                                                                                      |
| \-subcat           | 指定したカテゴリとサブカテゴリ以下の全ページを対象に追加します。例、「-subcat:主要カテゴリ」。                                                                                                                                          |
| \-uncat            | [カテゴリ未導入のページを対象に追加します](https://ja.wikipedia.org/wiki/特別:Uncategorizedpages "wikilink")。                                                                                                      |
| \-uncatcat         | [カテゴリ未導入のカテゴリを対象に追加します](https://ja.wikipedia.org/wiki/特別:Uncategorizedcategories "wikilink")。                                                                                                |
| \-uncatfiles       | [カテゴリ未導入の画像を対象に追加します](https://ja.wikipedia.org/wiki/特別:Uncategorizedimages "wikilink")。                                                                                                      |
| \-file             | 指定したテキストファイルから対象リストを読み込みます。例、「-file:list.txt」。なお、このテキストファイルは使用する[文字コード](../Page/文字コード.md "wikilink")（例えばUTF-8）で保存しておかなければなりません。                                                              |
| \-filelinks        | 指定したメディアファイルを使用したページを対象に追加します。例、「-filelinks:画像です.jpeg」                                                                                                                                       |
| \-yahoo            | Yahoo検索で見つかったページを対象に追加します。処理は、Pythonモジュールの「pYsearch」に依存します。使用するには、config.py の yahoo_appid で設定が必要です。                                                                                         |
| \-google           | Google検索で見つかったページを対象に追加します。使用するには、config.py の google_key で設定が必要です。                                                                                                                          |
| \-search           | メディアウィキの検索で見つかったページを対象に追加します。対象は、全名前空間です。                                                                                                                                                    |
| \-interwiki        |                                                                                                                                                                                              |
| \-withoutinterwiki | 言語間リンクがないページを対象に追加します。例、「-withoutinterwiki:10」のように処理するページ数を指定できます。                                                                                                                           |
| \-links            | 指定したページ内でリンクされているページを対象に追加します。例、「-links:トイレ」。                                                                                                                                                |
| \-new              | [新しいページの](https://ja.wikipedia.org/wiki/特別:Newpages "wikilink")60ページを対象に追加します。「-new:100」のようにページ数は変更できます。                                                                                     |
| \-ref              | 指定したページにリンクしたページを対象に追加します。例、「-ref:ツル」（[特別:Whatlinkshere/ツル](https://ja.wikipedia.org/wiki/特別:Whatlinkshere/ツル "wikilink") *を参照*）。<small>なお、やや古いバージョンにはバグがあるので正しく動作しません。最新版で実行してください。</small> |
| \-start            | 指定したページからASCII順に処理することを指定します。例、「-start:カメ」（[特別:Allpages/カメ](https://ja.wikipedia.org/wiki/特別:Allpages/カメ "wikilink") *を参照*）。                                                                 |
| \-prefixindex      | 指定した文字で始まるページを対象に追加します。名前空間も指定できます。例、「-prefixindex:Wikipedia:あいさつ」（[特別:Prefixindex/Wikipedia:あいさつ](https://ja.wikipedia.org/wiki/特別:Prefixindex/Wikipedia:あいさつ "wikilink") *を参照*）。           |
| \-transcludes      | 指定したテンプレートにリンクしたページを対象に追加します。例、「-transcludes:Aimai」（[特別:Whatlinkshere/Template:Aimai](https://ja.wikipedia.org/wiki/特別:Whatlinkshere/Template:Aimai "wikilink") *を参照*）。                      |
| \-unusedfiles      | [使われていない画像を対象に追加します](https://ja.wikipedia.org/wiki/特別:Unusedimages "wikilink")。例、「-unusedfiles:10」のように処理するページ数を指定できます。                                                                       |
| \-unwatched        |                                                                                                                                                                                              |
| \-usercontribs     | 指定した利用者の投稿記録を対象に追加します。例、「-usercontribs:Example」。                                                                                                                                             |
| \-weblink          | 指定したURLへの外部リンクをしているページを対象に追加します。例、「-weblink:google.co.jp」。                                                                                                                                   |

処理対象を指定する引数

| 引数                | 説明                                                                                                                                                          |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \-always          | 処理毎の確認メッセージを非表示にします。                                                                                                                                        |
| \-regex           | [正規表現](../Page/正規表現.md "wikilink")を有効にします。この引数を指定しないなら、単純な文字置換のみの処理がなされます。                                                                                  |
| \-nocase          | 正規表現で大文字と小文字を区別しなくする。                                                                                                                                       |
| \-dotall          | ドット(.)が改行を含むすべてのキャラクタにマッチします。このオプションを指定しない場合、ドットは改行にマッチしません。                                                                                                |
| \-multiline       | 表現 ^ と $ が、それぞれ各行の先頭と末尾にマッチするようになります。                                                                                                                       |
| \-summary         | 要約欄に記述されるメッセージをオリジナルのものと置き換えます。例、「-summary:ボットですよ」。                                                                                                         |
| \-namespace       | 処理する[名前空間の名前または変数を指定します](https://ja.wikipedia.org/wiki/Help:名前空間 "wikilink")。複数回使用できます。他の引数と組み合わせて使用します。ただ、-start 引数は、「-start:Category:カメ」のように指定しなければなりません。 |
| \-xmlstart        | (-xml 指定時のみ有効） XMLダンプから情報を取得する際、指定したページが現れるまでページをスキップします。                                                                                                   |
| \-addcat          | 対象ページすべてに指定したカテゴリを追加します。                                                                                                                                    |
| \-excepttitle     | 指定した文字列がタイトルに含まれるページを処理をスキップします。-regex 引数が指定されているなら、正規表現が有効になります。                                                                                           |
| \-requiretitle    | 指定した文字列がタイトルに含まれるページのみ処理します。-regex 引数が指定されているなら、正規表現が有効になります。                                                                                               |
| \-excepttext      | 指定した文字列が含まれるページの処理をスキップします。-regex 引数が指定されているなら、正規表現が有効になります。                                                                                                |
| \-exceptinside    |                                                                                                                                                             |
| \-exceptinsidetag |                                                                                                                                                             |
| \-fix             | あらかじめ定義されているタスクを実行します。タスクの詳細は fixes.py で定義されています。-fix を指定した場合、-regex や -nocase、通常の置換処理は無視されます。                                                              |
| \-recursive       | 置換処理を再帰的に行います。無限ループを引き起こす可能性があるので注意してください。                                                                                                                  |
| \-allowoverlap    |                                                                                                                                                             |
| その他               | 第1引数には置換対象の文字列、第2引数には置換する文字列を指定します。-regex 引数が指定されているなら、正規表現が有効になります。新旧文字列のペアは複数指定することができます。                                                                 |

その他の引数

## 使用例

テンプレート指定の古い文法（例：{{msg:Stub}}）を新しい文法（例：{{Stub}}）に変更する：

`   python replace.py -xml -regex "{{msg:(.*?)}}" "{{\1}}"`

複数行にマッチさせる例：

`   python replace.py -regex -start:! "First line\nSecond line" ""`

ローカルのXMLダンプ foobar.xml から情報を取得し、"Errror" という typo を "Error"に修正する：

`   python replace.py -xml:foobar.xml "Errror" "Error"`

「John Doe」というページで、HTML タグを wiki 文法に変換する：

`   python replace.py -page:John_Doe -fix:HTML`

引数なしで bot を実行し、置換処理が必要になるたびに確認メッセージを表示させる：

`   python replace.py -file:blah.txt`

## 関連項目

  - [Help:Pywikipediabot](https://ja.wikipedia.org/wiki/Help:Pywikipediabot "wikilink")

[Category:Pywikipedia](https://ja.wikipedia.org/wiki/Category:Pywikipedia "wikilink")