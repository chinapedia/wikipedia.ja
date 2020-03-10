> この記事は[Files transferred over shell protocol](https://ja.wikipedia.org/wiki/Files_transferred_over_shell_protocol)から翻訳されています。


**Files transferred over shell protocol**（**FISH**）とは、[SSHや](../Page/Secure_Shell.md "wikilink")[RSHを使ってコンピュータ間でファイルを転送したり](../Page/リモートシェル.md "wikilink")、遠隔のファイルを管理するための[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

FISHの利点は、サーバ側で必要となるのがSSHまたはRSHと、[シェル](../Page/シェル.md "wikilink")および[UNIX](../Page/UNIX.md "wikilink")の標準ユーティリティ（[ls](https://ja.wikipedia.org/wiki/Ls_\(UNIX\) "wikilink")、[cat](https://ja.wikipedia.org/wiki/Cat_\(UNIX\) "wikilink")、[dd](https://ja.wikipedia.org/wiki/Dd_\(UNIX\) "wikilink")）だけという点である。オプションとして、FISHサーバ専用プログラム（*start_fish_server*）もあり、UNIXのシェルを使わずにFISHコマンドを実行するため、操作が高速化される。

このプロトコルは[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")、Pavel Machek が [Midnight Commander](https://ja.wikipedia.org/wiki/Midnight_Commander "wikilink") 向けに設計したものである。

## プロトコルのメッセージ

クライアントは、以下のようなテキスト形式の要求を送る。

`#FISH_COMMAND 引数列...`
`等価なシェルコマンド群`
`複数行にまたがることもある`

FISHコマンドには優先順位がある。サーバは理解できるFISHコマンドを実行する。理解できない場合は、等価なシェルコマンドを実行しようとする。専用サーバプログラムが動作していない場合、UNIXのシェルはFISHコマンドをコメント行として無視し、等価なシェルコマンドだけを実行する。

サーバの応答は複数行にまたがるが、常に以下の行が末尾に付く。

`### xyz`<オプションテキスト>

`###` はプレフィックス、`xyz` はリターンコードである。リターンコードは[ftpで使われているもののスーパーセットである](../Page/File_Transfer_Protocol.md "wikilink")。コード000と001は特殊で、その意味は最終行以前にサーバの出力があったかどうかで変わってくる。

## セッション開始

クライアントは ` echo  `<FISH:;/bin/sh> をリモートのマシンでコマンドとして実行することでSSHまたはRSHのコネクションを開始する。これにより、サーバ側で通常のRSHやSSHのコネクションとFISHのコネクションを区別することができる。

まず、サーバに対して `FISH` と `VER` という2つのコマンドを送る。

`#FISH`
`echo; start_fish_server; echo '### 200'`

`#VER 0.0.2 `<feature1>` `<feature2>` <...>`
`echo '### 000'`

サーバは VER コマンドに対して、次のような応答を返す。

`VER 0.0.0 `<feature2>` <...>`
`### 200`

これは、サポートされているFISHプロトコルのバージョンと、サポートされている拡張機能を示している。

## 実装

  - [Midnight Commander](https://ja.wikipedia.org/wiki/Midnight_Commander "wikilink")
  - [Lftp](https://ja.wikipedia.org/wiki/Lftp "wikilink")
  - <fish://> [KDE](../Page/KDE.md "wikilink") [kioslave](https://ja.wikipedia.org/wiki/KIO "wikilink") (with [Konqueror](../Page/Konqueror.md "wikilink"))

## 外部リンク

  - [README.fish from Midnight Commander](http://cvs.savannah.gnu.org/viewcvs/mc/mc/vfs/README.fish?view=markup)
  - [kio_fish page](http://www.garni.ch/fish/)
  - [KDE documentation](http://docs.kde.org/development/en/kdebase/kioslave/fish.html)
  - [Tutorial for the kioslave](http://www.linux.org/lessons/short/fish/index.html)

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:ファイル転送プロトコル](https://ja.wikipedia.org/wiki/Category:ファイル転送プロトコル "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")