> この記事は[Help:Pywikipediabot/blockpageschecker.py](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/blockpageschecker.py)から翻訳されています。


**blockpageschecker.py** はもはや保護（半保護）されていない記事から、保護（半保護）のテンプレートを除去するための、[Python](../Page/Python.md "wikilink") で書かれたスクリプトです。Wikihermit によって作成され、後に Filnik によって書き直されました。当初は Botwiki で配布されていましたが、2007年のリビジョン4634より [Pywikipediabot](https://ja.wikipedia.org/wiki/Help:Pywikipediabot "wikilink") に含まれるようになりました\[1\]。

## 文法

``` text
 python blockpageschecker.py [-xml:filename] [-page:pagetitle] [-protectedpages:namespace] [-always] [-debug] [-move]
```

[:Category:編集保護中のページ](https://ja.wikipedia.org/wiki/Category:編集保護中のページ "wikilink")、[:Category:編集半保護中のページ](https://ja.wikipedia.org/wiki/Category:編集半保護中のページ "wikilink")、[:Category:移動保護中のページを走査して](https://ja.wikipedia.org/wiki/Category:移動保護中のページ "wikilink")、もはや保護されていない記事からテンプレートを除去するとともに、保護のタイプとテンプレートが合致していなければ、テンプレートを貼り替えます。もちろん、編集保護されたページを編集するためには、Bot アカウントに管理者権限が必要です。

## 引数

| 引数               | 説明                                                                               |
| ---------------- | -------------------------------------------------------------------------------- |
| \-xml            | ローカルの XML ダンプから情報を取得します。                                                         |
| \-page           | カテゴリを探索するのではなく、特定のページを対象としてテンプレート除去を試みます。                                        |
| \-protectedpages | 全ての保護されたページをチェックします。「保護中の記事」のカテゴリが使えない時に便利です。コロンに続けて、チェックを行う名前空間を数字で指定することもできます。 |
| \-always         | テンプレートを除去する際に、プロンプトを表示しません。                                                      |
| \-debug          | デバッグオプション。Botがテンプレートを除去できない時、ブラウザでそのページを開くかどうかを尋ねます。                             |
| \-move           | 編集保護だけでなく、移動保護のチェックを行います。                                                        |

## 運用

[荒らしや突発的な](https://ja.wikipedia.org/wiki/Wikipedia:荒らし "wikilink")[編集合戦によって保護され](https://ja.wikipedia.org/wiki/Wikipedia:編集合戦 "wikilink")、置き捨てられた記事のメンテナンスに良いでしょう。標準の動作では、チェックする記事の名前空間を意識しません。このため、利用者ページや利用者会話ページからもテンプレートの除去を試みます。

## 脚注

## 関連項目

  - [Help:Pywikipediabot](https://ja.wikipedia.org/wiki/Help:Pywikipediabot "wikilink")
  - [Wikipedia:保護の方針](https://ja.wikipedia.org/wiki/Wikipedia:保護の方針 "wikilink")
  - [Wikipedia:半保護の方針](https://ja.wikipedia.org/wiki/Wikipedia:半保護の方針 "wikilink")

## 外部リンク

  - [Botwiki - Python:Blockpageschecker.py](http://botwiki.sno.cc/wiki/Python:Blockpageschecker.py)

[Category:Pywikipedia](https://ja.wikipedia.org/wiki/Category:Pywikipedia "wikilink")

1.  [Pywikipedia-l SVN: 4634 trunk/pywikipedia/blockpageschecker.py](http://lists.wikimedia.org/pipermail/pywikipedia-l/2007-December/001336.html)