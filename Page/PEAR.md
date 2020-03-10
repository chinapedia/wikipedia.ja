> この記事は[PEAR](https://ja.wikipedia.org/wiki/PEAR)から翻訳されています。


**PEAR** (**PHP Extension and Application Repository**) は[PHPで利用する事ができるライブラリ](../Page/PHP_\(プログラミング言語\).md "wikilink")（パッケージ）を提供しているサービス。 PEARは[PHPで書かれたライブラリを提供しているが](../Page/PHP_\(プログラミング言語\).md "wikilink")、C言語で書かれた拡張ライブラリ (extension) を提供する[PECL](https://ja.wikipedia.org/wiki/PECL "wikilink")というサービスも存在する。

## PEARのインストール

PEARは通常PHP4、PHP5に最初から同梱されているが、ビルドオプションの指定などでインストールしなかった場合でも後からインストールする事ができる。

インストールが完了すると、pearという同名のコマンドが利用できるようになっている。Debianのapt-getやRed Hat Linuxなどで利用されているyumに似たインターフェイスでこのコマンドを利用する事でPEARのライブラリ群を自動的にインストール、アンインストール、アップグレード、作成できるようになっている。

  - 共有ホスト（レンタルサーバ等）へのインストール
    レンタルサーバなど、PEARがインストールされていない場合、[php.netにあるgo-pear.php](http://pear.php.net/go-pear)のソースをgo-pear.phpというファイル名で保存して実行するとインストールできる。
    また、共有ホストにインストールされているPEARが持っているパッケージ以外のパッケージを利用したい場合も、ユーザーローカルにPEARをインストールすることができる。詳細は[PEAR公式マニュアル](http://pear.php.net/manual/ja/installation.shared.php)による。

## PEARパッケージの管理（Linux、FreeBSDでの例）

PHPでPEARパッケージを用いるには、そのパッケージをあらかじめシステム（Webサーバ側）にインストールしておく必要がある。その時に利用されると思われるパッケージ管理のコマンド例を次に示す。（これらのコマンドは、システムのシェルで実行する）

パッケージ一覧の表示

``` bash
pear list
```

パッケージのインストール

``` bash
pear install [パッケージ名]
```

## PEARパッケージのPHPからの利用

PHPソースコードの例

``` php
<?php

require_once("Auth/Auth.php"); // 利用するパッケージを最初に指定
```

## PEAR標準コーディング規約

PEARにはPHPのコード作成に関する標準スタイル**PEAR標準コーディング規約**が定義されており、PEAR上で公開されているすべてのライブラリはこのPEAR標準コーディング規約にそって書かれている。

## PEARの発音について

[PEAR :: Manual :: はじめに](http://pear.php.net/manual/ja/introduction.php)に書かれているように果物の梨と同じように（「ペア」と）発音する。

## 関連項目

  - [Composer](https://ja.wikipedia.org/wiki/Composer "wikilink")

## 外部リンク

  - [PEAR - PHP Extension and Application Repository](http://pear.php.net/)

[Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:パッケージ管理システム](https://ja.wikipedia.org/wiki/Category:パッケージ管理システム "wikilink")