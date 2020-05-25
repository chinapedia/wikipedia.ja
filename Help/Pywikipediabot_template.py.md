> この記事は[Help:Pywikipediabot/template.py](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/template.py)から翻訳されています。


*In other languages:* [en](https://ja.wikipedia.org/wiki/:mediawikiwiki:Manual:Pywikipediabot/template.py "wikilink") - [ja](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/template.py "wikilink")

-----

**template.py** はテンプレートを他のテンプレートに置き換えたり、古い MediaWiki 書式のテンプレートを新しいテンプレート書式に変換します。

## 使い方

`python template.py [-remove] [xml[:filename]] "oldTemplate" ["newTemplate"]`

コマンドラインでテンプレートを指定します。プログラムはテンプレートページを拾い上げ、それが使われている全てのページを見ます。その後、自動的にそれらを巡回し、テンプレートを置き換えるでしょう。

## 引数

| | 引数        | 説明                                                                                                       |
| ----------- | -------------------------------------------------------------------------------------------------------- |
| \-remove    | 全ての記事から、指定したテンプレートを除去します。                                                                                |
| \-subst     | 指定したテンプレートのテキストを記事に展開します。                                                                                |
| \-assubst   |                                                                                                          |
| \-xml       | ローカルのダンプファイルから情報を取り寄せます。もしこの引数が与えられなければ、情報はウィキのメンテナンスページから読み込まれます。引数は "-xml:filename.xml" として与えることもできます。 |
| \-namespace | 処理の対象とする名前空間を指定します。複数の名前空間を指定する時は、複数回使用する事ができます。                                                         |
| \-summary   | 要約欄を指定します。空白文字が含まれる時は、引用符で括ってください。                                                                       |
| \-always    | 変更の際、確認のプロンプトを表示しません。                                                                                    |
| \-page      | 特定のページを処理の対象とします。複数のページを対象とする時は、複数回使用する事ができます。ページタイトルに空白文字が含まれる時は、引用符で括ってください。                           |
| \-category  | 編集するページにカテゴリを追加します。                                                                                      |
| oldTemplate | 旧テンプレート名。                                                                                                |
| newTemplate | 新テンプレート名。テンプレート名に空白文字が含まれる時は、引用符で括るか、アンダースコアを使用してください。                                                   |

## 関連項目

  - [Help:Pywikipediabot](https://ja.wikipedia.org/wiki/Help:Pywikipediabot "wikilink")

[Category:Pywikipedia](https://ja.wikipedia.org/wiki/Category:Pywikipedia "wikilink")