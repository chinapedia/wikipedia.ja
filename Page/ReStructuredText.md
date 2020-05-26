> この記事は[ReStructuredText](https://ja.wikipedia.org/wiki/ReStructuredText)から翻訳されています。


**reStructuredText** は、[軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink")のひとつ。[ソースコード](../Page/ソースコード.md "wikilink")の状態で高い[可読性](../Page/可読性.md "wikilink")を持つように設計されている。reStructuredText [パーサ](https://ja.wikipedia.org/wiki/パーサ "wikilink")は、テキスト処理フレームワークである [Docutils](https://ja.wikipedia.org/wiki/Docutils "wikilink") のコンポーネントのひとつであり、[Python](../Page/Python.md "wikilink") で実装されている。

reStructuredText は、RST、reST、ReST と略されることもある。

## マークアップの例

ヘッダ:

``` ReST
セクション・ヘッダ
==================

サブセクション・ヘッダ
----------------------
```

リスト:

``` ReST
- 箇条書きリストの項目

- 2つ目

  - サブ項目

- 3つ目
```

``` ReST
1) 数字つきリスト項目

2) 2つ目

   a) サブ項目

      i) サブ-サブ項目

3) 3つ目
```

名前つきのリンク:

``` ReST
Google_ と `Linux カーネル・アーカイブ`_ へのリンクを含んだ文章。

.. _Google: http://www.google.com/
.. _Linux カーネル・アーカイブ: http://www.kernel.org/
```

名前なしのリンク:

``` ReST
`Python のサイト`__ への名前なしのリンクを含んだ文章。

__ http://www.python.org/
```

## 関連項目

  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")
      - [データ記述言語](../Page/データ記述言語.md "wikilink")
          - [マークアップ言語](../Page/マークアップ言語.md "wikilink")
              - [軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink")

## 外部リンク

  - [reStructuredText](http://docutils.sourceforge.net/rst.html)
  - [rest2web](http://www.voidspace.org.uk/python/rest2web/index.html)
  - [ReStructuredText 入門](http://www.planewave.org/translations/rst/quickstart.ja.html)
  - [はやわかり reStructuredText](http://www.planewave.org/translations/rst/quickref.html)
  - [reStructuredText (lowlife.jp)](http://lowlife.jp/yasusii/wiki/restructuredtext.html)

[Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink")