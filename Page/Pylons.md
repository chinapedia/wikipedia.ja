> この記事は[Pylons](https://ja.wikipedia.org/wiki/Pylons)から翻訳されています。


**Pylons** は [Python](../Page/Python.md "wikilink") 言語で書かれた [オープンソース](../Page/オープンソース.md "wikilink") の [webアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/webアプリケーションフレームワーク "wikilink")である。再利用性を促進し、機能を各モジュールに分割するために[WSGI](../Page/Web_Server_Gateway_Interface.md "wikilink") 標準を広い範囲にわたり採用している。

Pylons は、[Django](../Page/Django.md "wikilink") や [TurboGears](../Page/TurboGears.md "wikilink") などを含む昨今の [webアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/webアプリケーションフレームワーク "wikilink")の中でも最も新しいもののひとつである。[Ruby on Railsに強い影響を受けており](../Page/Ruby_on_Rails.md "wikilink")、主要なコンポーネントのうち[Routes](http://routes.groovie.org) と [WebHelpers](http://pylonshq.com/WebHelpers) は、Rails の機能を Python で再実装したものである。

Pylonsはメンテナンスモードに移行し実質的な開発は終了し、後継となるPyramidに移行している。

## 特徴

### 構造

Pylons は他社が開発したツールに基づくほぼ完成したスタックを持つことで知られており、明らかに [NIH](../Page/車輪の再発明.md "wikilink") シンドロームを避けている。

### インストール、依存ソフトウェア、設定

Pylons の公式なインストールの方法は、the [Python CheeseShop](http://cheeseshop.python.org) 経由で[EasyInstall](https://ja.wikipedia.org/wiki/EasyInstall "wikilink") を用いて行うことで、追加のツールもたいていは同じ方法でインストールされる。EasyInstall は必要に応じてパッケージの依存関係を解決する。Pylons と Paste を一緒にパッケージした配布系もあるが、配布系のパッケージは公式の配布物より遅れる傾向がある。Pylons は .egg ファイルを .zip ファイルに変更し、内容を展開することでもインストールできる。

[Pasteプロジェクトの設定](https://ja.wikipedia.org/wiki/Python_Pasete "wikilink")、テスト、配置に使用される。共通の [INI](https://ja.wikipedia.org/wiki/INI "wikilink")構成フォーマットを用いており、Paste では開発と配置の設定を、インタラクティブなデバッガなどの Pylons の複雑な部分を製品版のユーザーから隠蔽した状態で開発者が同じコードベースをもとに動作させられるよう、複数の"プロファイル"を用いることができる。

### URL のディスパッチ

[Selector](http://cheeseshop.python.org/pypi/selector)などの WSGI 互換の URL ディスパッチャであればどれでも使用可能だが、現在 Pylons 用に広く使われている唯一の URL ディスパッチャは[Ruby on Railsの](../Page/Ruby_on_Rails.md "wikilink") URL ディスパッチ機構を Python で再実装した[Routes](http://routes.groovie.org) である。

### HTML の生成

Pylonsでも採用された[Railsのもう一つの機構が](../Page/Ruby_on_Rails.md "wikilink")、Routes の設定に基づき URL のマッピング機能を提供する[WebHelpers](http://pylonshq.com/WebHelpers)である。WebHelpers は、[script.aculo.us](https://ja.wikipedia.org/wiki/script.aculo.us "wikilink") や [Prototype](https://ja.wikipedia.org/wiki/Prototype_JavaScript_Framework "wikilink") ライブラリを利用した[JavaScript](../Page/JavaScript.md "wikilink")コードを生成するためのユーティリティ的な機能も提供する。

HTML フォームの検証と生成のために、[FormEncode](http://formencode.org) と [FormBuild](http://formbuild.org/) が用いられている。Mako の継承モデルを用いてフォームの生成を行うために、Mako も一部で用いられている。

### テンプレート

[Myghty](http://myghty.org) がバージョン 0.9.5 まで Pylons のデフォルトのテンプレート言語であったが、バージョン 0.9.6 で [Mako](http://www.makotemplates.org/docs/) に置き換えられた。\[1\]いずれのテンプレート言語もインクルード、継承、任意の Python コードの埋め込みをサポートするテキストベース([XMLベースのものではない](../Page/Extensible_Markup_Language.md "wikilink"))のテンプレート言語である。

Pylons の緩く結合されたレイヤ構造により、それ以外のテンプレート言語も利用可能である。XML ベースのテンプレート言語[Genshi](http://genshi.edgewall.org/) もMako や Myghty いずれかの代わりに使用することができる。\[2\]

### データベースの抽象化 / [O/Rマッピング](../Page/オブジェクト関係マッピング.md "wikilink")

Pylons にはデフォルトのデータベースライブラリはない。[SQLObject](https://ja.wikipedia.org/wiki/SQLObject "wikilink") と [SQLAlchemy](https://ja.wikipedia.org/wiki/SQLAlchemy "wikilink") が知られている。

### repoze.bfgとのプロジェクト統合によるPylons終了とPyramidの誕生

フレームワークのPylons はPylons プロジェクトが開発してきたが、Pylons 2 の開発を進めるうちに repoze.bfg ([Zope](../Page/Zope.md "wikilink") 由来のコンポーネントをWSGIアプリケーションで利用できるようにしたコンポーネント集であるrepozeで構成されたフレームワーク) と似てきたことで、コードベース と開発コミュニティをマージする方向へとシフトする。2010年11月のrepoze.bfg とのプロジェクト統合の合意により、Pylonsの新しいバージョンはオリジナルのPylons 1.0 と大きく変わることとなる。こうしてPylonsプロジェクトはメンテナンスモードに移行し、Pyramidと銘打ったrepoze.bfgをコードベースとする新しいPylons プロジェクトが開始されることとなった\[3\]。

## Pyramid

**Pyramid** は、[WSGIベースの](../Page/Web_Server_Gateway_Interface.md "wikilink")[Python](../Page/Python.md "wikilink")で書かれた[オープンソースの](../Page/オープンソースソフトウェア.md "wikilink")[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")。[Zope](../Page/Zope.md "wikilink")・[Pylons](https://ja.wikipedia.org/wiki/#特徴 "wikilink")・[Django](../Page/Django.md "wikilink")に触発された、小さく速く堅実 (down-to-earth)なフレームワークである\[4\]。

Pylons 1.0は、WSGIベースのフレームワークとして代表的な存在であったが、PylonsApp とWSGIControllerメソッドは実質的にAPI として凍結されているなど、拡張性を取り入れるために改良しようとすることが困難であることが分かった\[5\]\[6\]

一方、repoze.bfgは、Zope 3のコンポーネントアーキテクチャを利用しており\[7\]、Zopeのコミュニティから大きな注目を集めていた\[8\]。 2010年に、Pylonsフレームワークは、repoze.bfgをベースとした開発に移行することを発表した\[9\]。それは結果として、repoze.bfgプロジェクトがPylonsプロジェクトに合流し、repoze.bfgがPyramidに改称することであった\[10\]。

バージョン1.3から、Python 3 互換となった。 Python 3.2 以上であれば、 Pyramidを使用できる\[11\]。

| バージョン | リリース日       |
| ----- | ----------- |
| 1.0   | 2011年1月30日  |
| 1.1   | 2011年7月22日  |
| 1.2   | 2011年9月12日  |
| 1.3   | 2012年3月21日  |
| 1.4   | 2012年12月18日 |
| 1.5   | 2014年4月8日   |
| 1.6   | 2016年1月3日   |
| 1.7   | 2016年5月19日  |
| 1.8   | 2017年1月21日  |
| 1.9   | 2017年6月26日  |
|       |             |

## 外部リンク

  - [Pylons Project home page](https://pylonsproject.org/)
      - [Pylons framework](https://pylonsproject.org/about-pylons-framework.html)
      - [Pyramid framework](https://trypyramid.com/)
          - [repoze.bfg framework](http://bfg.repoze.org/)
  - [Pylons Wiki](http://wiki.pylonshq.com)
  - [Sites using Pylons](http://wiki.pylonshq.com/display/pylonscommunity/Sites+Using+Pylons)
  - [Pylons に関連する文書の日本語訳](http://wiki.pylonshq.com/display/pylonsja/Home)

Pylons の標準インストールで用いられるパッケージ、および人気の高い追加パッケージ

  - [Myghty](http://myghty.org) - URL のディスパッチ、コントローラ、キャッシュ機構、テンプレート機能など
  - [Mako](http://www.makotemplates.org/docs/) - Myghty 以外のテンプレートエンジン
  - [Python Paste](http://pythonpaste.org/) - プロジェクトの設定、テスト、配置
  - [EasyInstall](http://peak.telecommunity.com/DevCenter/EasyInstall) - インストールとパッケージの依存関係
  - [Routes](http://routes.groovie.org) - Rails routes に基づく Routing の実装
  - [FormEncode](http://formencode.org) - フォームの検証と生成
  - [WebHelpers](http://pylonshq.com/WebHelpers) - HTML ヘルパー機能

### メーリングリスト

  - [pylons-discuss on Google Groups](http://groups.google.com/group/pylons-discuss)

Google Groups からの情報によると(2018年5月8日):

  - メンバー 2871 人
  - 月平均 25 メッセージ(過去3ヶ月間)

## 脚注

## 関連項目

  - [Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")
  - [Pythonを使っている製品あるいはソフトウェアの一覧](../Page/Pythonを使っている製品あるいはソフトウェアの一覧.md "wikilink")

[Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink")

1.  Haas, Christoph [Beginning Pylons](http://workaround.org/pylons/beginning-pylons.html). Retrieved July 5, 2007
2.  Genshi Wiki [Pylons with Genshi](http://genshi.edgewall.org/wiki/GenshiRecipes/PylonsWithGenshi) Retrieved July 5 2007
3.
4.
5.
6.
7.
8.
9.
10.
11.