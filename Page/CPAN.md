> この記事は[CPAN](https://ja.wikipedia.org/wiki/CPAN)から翻訳されています。


**CPAN**（シーパン、**C**omprehensive **P**erl **A**rchive **N**etwork）とは、[Perl](../Page/Perl.md "wikilink")の[ライブラリ](../Page/ライブラリ.md "wikilink")・[モジュール](../Page/モジュール.md "wikilink")やその他のPerlで書かれたソフトウェアを集めた巨大な[アーカイブ](../Page/アーカイブ.md "wikilink")で、世界中の[サーバ](../Page/サーバ.md "wikilink")にその内容が[ミラーリング](../Page/ミラーリング.md "wikilink")されている。再利用性・汎用性の高いモジュールが登録されており、Perlプログラマができるだけ[車輪の再発明](../Page/車輪の再発明.md "wikilink")をせずに済むための支援環境となっている。登録モジュールの検索システムも提供されているため、Perlプログラマは望む機能を持ったモジュールを容易に入手することができる。

CPANには大小さまざまなモジュールが登録されており、それらの依存関係もデータベース化されている。目的のモジュールと同時に、それに依存するほかのモジュールを芋づる式にダウンロードし、インストールすることが可能である。[Unix系](../Page/Unix系.md "wikilink")OSおよび[Windowsで利用できるCPANシェルという専用のソフトウェアが存在する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。このシェルはユーザの手持ちのライブラリの管理、CPANミラーへの問い合わせ、モジュールの[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")を行うものであり、ユーザは少ないコマンド操作によってモジュールの検索・導入を行うことができる。

## CPANシェル

CPANシェルを初めて使う場合、いくつかの設定が行われる。これには、モジュールのビルド・ダウンロード先のミラー指定などが含まれる。基本的に自動で最適なものが選択されるが、必要に応じてユーザが変更可能になっている。

実行には

`cpan`

と入力するが、モジュールインストール時のパーミッションの関係で

`sudo cpan`

と入力されることが多い。

設定の変更を行う場合は、一度CPANシェルを実行した上で

`o conf オプション 変更値`

の組み合わせによる入力を行う。変更を一時的なものにしないためには

`o conf commit`

にて反映を行う。オプションについては同じくCPANシェルを実行した上で

`o conf`

と入力することで表示される。

権限が与えられていないアカウントではモジュールを標準のインストールディレクトリに入れることができないケースがあるため、その際はインストール先を変更する必要がある。モジュールの個別インストールにて、インストール時にディレクトリをオプションで指定することもできるが、現在はCPANのモジュールlocal::libを利用して、あらかじめインストール先を指定しておくケースが多い。

## 関連項目

  - [CTAN](https://ja.wikipedia.org/wiki/CTAN "wikilink")
  - [:en:CEAN](https://ja.wikipedia.org/wiki/:en:CEAN "wikilink")

## 外部リンク

  - [CPAN](http://www.cpan.org/)
      - [The CPAN Search Site](http://search.cpan.org/) - CPANの検索サイト
  - [PAUSE](http://pause.perl.org/) - モジュール開発者用のアップロードサーバ

[Category:技術のウェブサイト](https://ja.wikipedia.org/wiki/Category:技術のウェブサイト "wikilink") [Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:パッケージ管理システム](https://ja.wikipedia.org/wiki/Category:パッケージ管理システム "wikilink") [Category:Perl](https://ja.wikipedia.org/wiki/Category:Perl "wikilink")