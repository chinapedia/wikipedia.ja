> この記事は[Help:Pywikipediabot/featured.py](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/featured.py)から翻訳されています。


**featured.py** は、他言語版ウィキペディアの[秀逸な記事の状況を調べ](https://ja.wikipedia.org/wiki/Wikipedia:秀逸な記事 "wikilink")、ホーム・ウィキの対応する記事に  のタグを貼る、[Python](../Page/Python.md "wikilink") で書かれたスクリプトです。

## 文法

``` text
python featured.py [-interactive] [-nocache] [-top] [-after:zzzz] [-fromlang:xx,yy--zz|-fromall]
```

## 引数

| | 引数                 | 説明                                                                                   | 既定値                   |
| -------------------- | ------------------------------------------------------------------------------------ | --------------------- |
| \-interactive        | 編集を行う際に、コンソールにプロンプトを表示します。                                                           | プロンプトを表示しません。         |
| \-nocache            | 作業時に前回の検証結果を記憶しているキャッシュを読み込みません。処理時間は短縮されません。                                        | キャッシュを読み込みます。         |
| \-top                | （r8455以前で有効）Link FA/GA などのタグを、言語間リンクの上に並べます。                                         | タグをその言語へのリンクの右側に置きます。 |
| \-side               | （r8456以後で有効）Link FA/GA などのタグを、その言語へのリンクの右側に置きます。                                     | 言語間リンクの上に並べます。        |
| \-after:ZZZZ         | 指定した記事名から処理を始めます。                                                                    |                       |
| \-fromlang:xx,yy--zz | 指定した言語コードのウィキを対象として検証を行います。yy--zz の "-" は2つ並びです。この -fromlang は、-fromall によって上書きされます。 |                       |
| \-fromall            | すべての言語コードのウィキを対象として検証を行います。                                                          |                       |

### その他の引数

| | 引数    | 説明                                                                        | 既定値           |
| ------- | ------------------------------------------------------------------------- | ------------- |
| \-count | 対象の言語で秀逸な/良質な記事に含まれる記事数を数えます。（書き込みは行いません）                                 |               |
| \-good  | [良質な記事を対象にします](https://ja.wikipedia.org/wiki/Wikipedia:良質な記事 "wikilink")。 | 秀逸な記事を対象にします。 |
| \-lists | [秀逸な一覧を対象にします](https://ja.wikipedia.org/wiki/Wikipedia:秀逸な一覧 "wikilink")。 | 秀逸な記事を対象にします。 |
|         |                                                                           |               |

## 注意点

各言語版の設定がスクリプト内に記してあります。これらの設定は、間違っている可能性もあります。特に、秀逸な記事を取得する先が間違っている場合には、関係ないページを編集することになります。

## 関連項目

  - [Help:Pywikipediabot](https://ja.wikipedia.org/wiki/Help:Pywikipediabot "wikilink")

## 外部リンク

  - [Log of /trunk/pywikipedia/featured.py](http://svn.wikimedia.org/viewvc/pywikipedia/trunk/pywikipedia/featured.py?view=log)

[Category:Pywikipedia](https://ja.wikipedia.org/wiki/Category:Pywikipedia "wikilink")