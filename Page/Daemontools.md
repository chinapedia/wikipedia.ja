> この記事は[Daemontools](https://ja.wikipedia.org/wiki/Daemontools)から翻訳されています。


**daemontools** (でーもんつーるず)は [ダニエル・バーンスタイン](../Page/ダニエル・バーンスタイン.md "wikilink") (djb) によって開発された、[Unix系](../Page/Unix系.md "wikilink")[OSにおけるサービス管理のためのツールのパッケージである](../Page/オペレーティングシステム.md "wikilink")。Unix系OSにおける、[rc.d、rc.local、inittab などの代替としてデーモンを起動させることができる](https://ja.wikipedia.org/wiki/init "wikilink")。[2007年](../Page/2007年.md "wikilink")11月よりパブリックドメインとなった。

## 概要

daemontools は、Unix系OSにおけるサービスの管理作業(プロセス監視、ロギングなど)をシンプルな手法で行うための支援ツールである。たとえば、**supervise** というプログラムは、フォアグラウンド起動させたデーモンプロセスの監視を行い、**multilog**というプログラムは、[パイプ経由で取りこぼしなくログの記録ができる](../Page/パイプ_\(コンピュータ\).md "wikilink")。daemontools においては [root権限の絞り込みが行われるため](../Page/スーパーユーザー.md "wikilink")、よりセキュアな運用が可能である。

daemontools では、設定により変更可能であるが、**/services** というルート直下のディレクトリに各種デーモン用のサービスディレクトリを個別に配置し、各サービスディレクトリに起動スクリプト等を配置する。また監視対象のプロセスは、フォアグラウンドで起動させる必要がある。たいていのデーモンはフォアグラウンドでの起動が可能だが、バックグラウンドでしか起動できないデーモンの場合は、daemontools に含まれる `fghack` ユーティリティを使用してフォアグラウンドで起動させる。

djbの開発した[inetd](https://ja.wikipedia.org/wiki/inetd "wikilink")代替ソフトウェアである[ucspi-tcp](https://ja.wikipedia.org/wiki/ucspi-tcp "wikilink")を併用することでさらにきめ細かい管理を行うことができる。

djbの開発した[djbdns](https://ja.wikipedia.org/wiki/djbdns "wikilink")や、[qmail](https://ja.wikipedia.org/wiki/qmail "wikilink")のみならず、[Apacheや](../Page/Apache_HTTP_Server.md "wikilink")[Postfix](../Page/Postfix.md "wikilink")、[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[IRCのボットなども](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink") daemontools の管理下におくことができる。工夫を凝らしたさまざまな起動スクリプトがインターネット上で公開されている。

## 主なツール

daemontools はパッケージの総称であり daemontool というプログラム自体は存在しない。この節では、daemontoolsに含まれるいくつかのユーティリティを用途別に紹介する。

### svscan - サービスディレクトリ群の監視

`svscan` は **/services** ディレクトリ直下を監視し、ディレクトリを発見すると、そのディレクトリ内でサービス管理デーモン `supervise` を起動する。

### supervise - プロセスの制御と監視

`supervise` は、カレントディレクトリ (**/service/サービスディレクトリ**) 直下の **run** という名称のプロセス起動用のコマンドを実行する。 多くの場合、**run** コマンドは[シェルスクリプトで記述されており](https://ja.wikipedia.org/wiki/シェル#シェルスクリプト "wikilink")、その中でデーモンの実行に必要な環境変数等を設定し、起動したいデーモンのコマンドを[execするという構造になっている](https://ja.wikipedia.org/wiki/Fork#Fork-Exec "wikilink")。 **run** プロセス ([exec](https://ja.wikipedia.org/wiki/Fork#Fork-Exec "wikilink") したデーモンプロセス) が何らかの理由で終了すると、`supervise` はその度に **run** を実行する。

デーモンの起動や停止 (プロセスへのシグナルを送信) をする場合は `svc` コマンドを使用して `supervise` に指示する。。 svc コマンドの使用により各種デーモンの停止、起動を統一的な方法で管理することができる。 また、プロセス番号を意識することなく TERM、KILL、HUP などのシグナルを送ることができる。

`supervise` で起動されたプロセスは、`svstat`で、死活や起動時間を確認することができる。

### multilog - ロギング

`multilog`は、[標準入力からのパイプを処理し](https://ja.wikipedia.org/wiki/入出力#コンピュータ処理における入出力 "wikilink")、指定したログファイルに出力する。ログの取得に[UDP](../Page/User_Datagram_Protocol.md "wikilink")[パケット](../Page/パケット.md "wikilink")ではなく、Unixパイプを使用するため高負荷時でも[syslogdのような取りこぼしがおきない](../Page/Syslog.md "wikilink")。ログの[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")は`tai64n` ユーティリティにより、[TAI64N (Temps Atomique International)フォーマットで記録される](../Page/国際原子時.md "wikilink")。このフォーマットは正確だが可読性が低いため、ログ閲覧時は、`tai64nlocal` フィルタを用いてひとの読める形式に変換する。

## 関連項目

  - [qmail](https://ja.wikipedia.org/wiki/qmail "wikilink")
  - [djbdns](https://ja.wikipedia.org/wiki/djbdns "wikilink")
  - [ダニエル・バーンスタイン](../Page/ダニエル・バーンスタイン.md "wikilink")
  - [init](https://ja.wikipedia.org/wiki/init "wikilink")
  - [国際原子時](../Page/国際原子時.md "wikilink")
  - [デーモン](../Page/デーモン_\(ソフトウェア\).md "wikilink")

## 外部リンク

  - [daemontools](http://cr.yp.to/daemontools.html)
  - [the djb way: daemontools](http://www.thedjbway.org/daemontools.html)
  - [runit - collection of run scripts](http://smarden.org/runit/runscripts.html) - run スクリプトのコレクション

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink")