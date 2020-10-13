> この記事は[IronPython](https://ja.wikipedia.org/wiki/IronPython)から翻訳されています。


**IronPython**とは、[.NET Frameworkおよび](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[Mono上で動作する](../Page/Mono_\(ソフトウェア\).md "wikilink")[Python](../Page/Python.md "wikilink")の実装である。Jim Huguninによって開発が進められ、[2006年](../Page/2006年.md "wikilink")[9月5日](../Page/9月5日.md "wikilink")に初版がリリースされた。バージョン1.x系のIronPythonはPython 2.4.3と互換している。IronPython 2.7はPython 2.7互換である\[1\]。

.NET Frameworkの持つ豊富なクラスライブラリを[Python](../Page/Python.md "wikilink")の文法でシームレスに利用できるだけでなく、従来のPython（CPython）のコード資産さえもある程度そのまま利用できることが特徴である。また、.NETの実行環境に対応した各種ツールが、そのまま利用できる点もメリットといえる。

もともとPythonはスクリプト言語であるが、IronPythonコンパイラサービスによって[.NETアセンブリにコンパイルすることも可能である](../Page/アセンブリ_\(共通言語基盤\).md "wikilink")。これは、[スクリプト言語](../Page/スクリプト言語.md "wikilink")として利用する場合はバイトコードに動的コンパイルし、アセンブリの場合は、それが事前コンパイルされたものと考えることができる。

IronPython自身は[C\#で実装されている](../Page/C_Sharp.md "wikilink")。

## 開発の歴史

IronPythonの起源は、「[CLIの設計は](../Page/共通言語基盤.md "wikilink")[動的言語](https://ja.wikipedia.org/wiki/動的言語 "wikilink")との相性が悪い」という.NET Frameworkの問題点を検証するために作成された検証用のプロトタイプであった。IronPythonの作者であるJim Huguninは2003年に、この論文を発表した。その後、「何故、.NET Frameworkは動的言語として駄目なプラットフォームなのか?」という短い論文を書くために、Pythonの移植を試みたところ、彼の意に反して良く動くものができてしまった。そこで、彼は開発を継続することとし、Open Source Conference 2004 でIronPython 0.6を[Common Public Licenseでリリースした](../Page/Common_Public_License.md "wikilink")。2003年の論文が間違いであったことを、彼自身の手で証明したことになる。

その後、Jim Huguninはマイクロソフトに合流してIronPythonの開発を継続、.NET Framework 2.0に対応したバージョンを作成し、現在では[Shared Source Licensing Programとしてリリースしている](https://ja.wikipedia.org/wiki/Shared_Source_Licensing_Program "wikilink")。

現在の最新版であるIronPython 2.x系列は.NET 4に対応し、DLR（[動的言語ランタイム](../Page/動的言語ランタイム.md "wikilink")）上に実装されている。なお、IronPython 2.7までは、対話環境であるIronPython Interactiveや、IronPython用の各種プロジェクト テンプレートを[Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") 2010に統合する"*IronPython Tools for Visual Studio*"がインストーラに含まれていたが\[2\]、2.7.1以降は"*Python Tools for Visual Studio*" (PTVS) への将来的な移行を見越して、"*IronPython Tools～*"は廃止されている\[3\]。PTVS 2.2はVisual Studio 2013と2015に対応する\[4\]。Visual Studio 2015のインストーラーには、PTVSをインストールするオプションが正式に含まれている。

2018年12月現在、Python 3.xをサポートするためのIronPython 3が開発中である。IronPython 3は.NET 4.5と[.NET Core](https://ja.wikipedia.org/wiki/.NET_Core "wikilink") 2.0/2.1をターゲットにしている。

## コード例

### Hello, World

CPythonの機能と.NET Frameworkの機能を併用する例を示す。

``` python
# -*- coding: utf-8 -*-
# CPython 2.x の組み込み命令を使って標準出力する。
print '%d, %f, %s' % (10 * 10, 2 + .3, '"Hello, CPython"')
# .NET Framework の基本クラスライブラリを使って標準出力する。
import System
System.Console.WriteLine('{0}, {1}, {2}', 10 * 10, 2 + .3, '"Hello, IronPython"')
```

## 脚注

## 関連項目

  - [CPython](https://ja.wikipedia.org/wiki/CPython "wikilink") - オリジナルのPython。Cで書かれていることからCPythonとも呼ばれる。
  - [Jython](../Page/Jython.md "wikilink") - CPythonを[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")に移植したもの。
  - [IronRuby](../Page/IronRuby.md "wikilink")

## 外部リンク

  -
  -
{{.NET}}

[Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:Pythonライブラリ](https://ja.wikipedia.org/wiki/Category:Pythonライブラリ "wikilink") [Category:Pythonの実装](https://ja.wikipedia.org/wiki/Category:Pythonの実装 "wikilink")

1.  [IronPython.net / Documentation](http://ironpython.net/documentation/)
2.
3.
4.  [「Visual Studio 2015」に対応した「Python Tools for Visual Studio 2.2」が正式版に - 窓の杜](http://www.forest.impress.co.jp/docs/news/20150723_712926.html)