> この記事は[PECL](https://ja.wikipedia.org/wiki/PECL)から翻訳されています。


**PECL**（ピクル、PHP Extension Community Library）は、[PHPで利用できる拡張](../Page/PHP_\(プログラミング言語\).md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")（パッケージ）を提供しているサービス。

PECLで提供されるライブラリは[Cで記述されているため](../Page/C言語.md "wikilink")、PHPで記述された[PEAR](../Page/PEAR.md "wikilink")のライブラリよりも高速に動作する。PECLにより提供されるライブラリはPHPの拡張モジュールとしてインストールされる。一方で、PEARライブラリはPHPのバージョンアップに伴う再インストールが原則として不要なのに対し、PECL拡張モジュールはPHP内部の[APIに依存する部分があるため](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、PHPのバージョンアップに伴いAPIが変更された場合は再コンパイルを必要とする。

PECLのインストール用には、PEAR同様に「pecl」コマンドが提供されている。インストール方法もほぼPEARと同じだが、インストール後に設定ファイル（php.ini）の「extension」でインストールしたモジュールを指定する必要がある点が異なる。なお[Windows版では](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、手動でphp.iniを修正して、あらかじめコンパイル済みのPECL [DLLを組み込むのが一般的な方法である](../Page/ダイナミックリンクライブラリ.md "wikilink")。

## 外部リンク

  - [PECL - The PHP Extension Community Library](http://pecl.php.net/)
  - [PECLの読み方 (What is PEAR?)](http://pear.php.net/manual/en/about.pear.php)

[de:PHP Extension and Application Repository\#PECL](https://ja.wikipedia.org/wiki/de:PHP_Extension_and_Application_Repository#PECL "wikilink") [en:PEAR\#PECL](https://ja.wikipedia.org/wiki/en:PEAR#PECL "wikilink") [it:PHP Extension and Application Repository\#PECL](https://ja.wikipedia.org/wiki/it:PHP_Extension_and_Application_Repository#PECL "wikilink") [pt:PEAR\#PECL](https://ja.wikipedia.org/wiki/pt:PEAR#PECL "wikilink")

[Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:パッケージ管理システム](https://ja.wikipedia.org/wiki/Category:パッケージ管理システム "wikilink")