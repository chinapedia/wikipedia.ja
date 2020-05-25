> この記事は[Help:Pywikipediabot/pagefromfile.py](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/pagefromfile.py)から翻訳されています。


*In other languages:* [en](https://ja.wikipedia.org/wiki/meta:Pagefromfile.py "wikilink") - [it](https://ja.wikipedia.org/wiki/meta:Pagefromfile.py/it "wikilink") - [ja](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/pagefromfile.py "wikilink")

-----

**pagefromfile.py** は [Pywikipediabot](https://ja.wikipedia.org/wiki/Help:Pywikipediabot "wikilink") フレームワークの一部です。このスクリプトで、テキストファイルからページを作成することができます。ファイルは [UTF-8](../Page/UTF-8.md "wikilink") で書かれていなければならず、もし一つのファイルから複数のページを作成したいのであれば、**-start** と **-end** 引数によって明示的に記事を分割しなければいけません。

ページ名はテキストファイル中の最初の見出し語となります（`''' '''`で括られた最初の語）。それはアップロードされたページに自動的に挿入されます。

**警告**: スクリプトは[再帰的な方法で入力テキストを解析します](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")。このため、テキストが複数ページで構成されていれば、容易にメモリ不足を起こします。入力テキストを単一のページに割って、個別にアップロードするのが得策です。

## 文法

``` text
pagefromfile.py [global-arguments] [specific-arguments]
```

## 引数

| | 引数             | 説明                                     | 既定値           |
| ---------------- | -------------------------------------- | ------------- |
| \-start:xxxx     | ページの開始となる文字列を指定します。                    | `{{-start-}}` |
| \-end:yyyy       | ページの終了となる文字列を指定します。                    | `{{-stop-}}`  |
| \-file:zzz       | 素材となるテキストファイル名を指定します。                  | `dict.txt`    |
| \-include        | 開始および終了文字列がページに含まれます。                  |               |
| \-titlestart:xxx | ページの表題の開始を示す文字列です。                     | '''           |
| \-titleend:xxx   | ページの表題の終了を示す文字列です。                     | '''           |
| \-summary:xxx    | ページをウィキペディアにアップロードする際の要約欄を示す文字列です。     |               |
| \-minor          | ページの編集を「細部の編集」として行います。                 |               |
| \-debug          | デバッグモードです。メッセージのみを表示し、実際のアップロードを行いません。 |               |
| \-safe           | ページがすでに存在するとき、何も行いません（デフォルト）。          |               |
| \-appendtop      | ページがすでに存在するとき、ページの最上部に追記します。           |               |
| \-appendbottom   | ページがすでに存在するとき、ページの最下部に追記します。           |               |
| \-force          | ページがすでに存在するとき、ページを上書きします。              |               |
| \-notitle        | ページに記事名の行を含めません。                       |               |

## 例

以下は、記事の素材となるテキストファイルの例です。

``` text
{{-start-}}
'''PageName'''
記事テキストをここに

{{-stop-}}
{{-start-}}
'''AnotherPageName'''
他の記事テキストをここに
{{-stop-}}
```

[Category:Pywikipedia](https://ja.wikipedia.org/wiki/Category:Pywikipedia "wikilink")