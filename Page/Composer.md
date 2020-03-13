> この記事は[Composer](https://ja.wikipedia.org/wiki/Composer)から翻訳されています。


**Composer**は、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")向けの[ソフトウェア](../Page/ソフトウェア.md "wikilink")および必要な[ライブラリ](../Page/ライブラリ.md "wikilink")の依存関係を管理する標準形式を提供するアプリケーションレベルの[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")である。 Nils AdermannとJordi Boggianoにより開発され、現在も両氏によってプロジェクトの管理が継続されている。両氏は2011年4月に開発を開始し、2012年3月1日に初めてリリースされた\[1\]。[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")の『[npm](https://ja.wikipedia.org/wiki/npm_\(パッケージ管理ツール\) "wikilink")』および[Ruby](../Page/Ruby.md "wikilink")の『[bundler](https://ja.wikipedia.org/wiki/:en:Bundler_\(software\) "wikilink")』から強い影響を受けている\[2\]。

[コマンドライン上で動作し](../Page/キャラクタユーザインタフェース.md "wikilink")、アプリケーションが依存するライブラリなどをインストールする。 また、利用可能なパッケージを含んでいるメインリポジトリ『Packagist』\[3\] で利用可能なPHPアプリケーションをインストールすることも可能であるほか、ライブラリ向けに[サードパーティー](../Page/サードパーティー.md "wikilink")のコードを容易に利用出来る[オートロード](https://ja.wikipedia.org/wiki/オートロード "wikilink")情報を指定できる機能も提供されている。

また、[Laravel](https://ja.wikipedia.org/wiki/Laravel "wikilink")を含めた有名な[オープンソース](../Page/オープンソース.md "wikilink")のPHPプロジェクトの重要な機能の一部として利用されている\[4\]。

## Composerに対応するフレームワーク

  - [Symfony](https://ja.wikipedia.org/wiki/Symfony "wikilink") バージョン 2 以降
  - [Laravel](https://ja.wikipedia.org/wiki/Laravel "wikilink") バージョン 4 以降
  - [CodeIgniter](https://ja.wikipedia.org/wiki/CodeIgniter "wikilink") バージョン 3.0 以降
  - [CakePHP](../Page/CakePHP.md "wikilink") バージョン 3.0 以降
  - [FuelPHP](https://ja.wikipedia.org/wiki/FuelPHP "wikilink") バージョン 2.0 以降
  - [Drupal](../Page/Drupal.md "wikilink") バージョン 8 以降
  - [Silex](https://ja.wikipedia.org/wiki/Silex "wikilink")

## composer.json

Composerでクラスのオートローディングなどをするためには composer.json というファイルを記述しなければならない。以下の示すcomposer.jsonはPHPのPHP-FIGが提供しているコーディング規約「PSR-4」に準じたオートローディングをするためのファイルである。ユーザーは MyAppという名前空間を使ってコーディングしなければならない。

``` json
{
    "autoload" : {
        "psr-4" : {
            "MyApp\\" : "folder/"
        }
    }
}
```

以下はサンプルコードである。

``` php
<?php

namespace MyApp;

class ClassName
{
    ..
}
```

## 参考文献

## 外部リンク

  -
  - [Composer on GitHub](https://github.com/composer/composer)

  - [Composer documentation](https://getcomposer.org/doc/)

  - [Composer Tutorial](http://php.codeindepth.com/composer-for-beginners/)

  - [Packagist - the main Composer repository](https://packagist.org/)

  -
[Category:フリーパッケージ管理システム](https://ja.wikipedia.org/wiki/Category:フリーパッケージ管理システム "wikilink") [Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink")

1.  [Software CHANGELOG](https://raw.github.com/composer/composer/1.0.0-alpha1/CHANGELOG.md), github.com, Retrieved November 28, 2013.
2.  [Getting Started/Dependency management](https://getcomposer.org/doc/00-intro.md#dependency-management), getcomposer.org, Retrieved November 28, 2013.
3.  See [packagist.org](https://packagist.org/)
4.