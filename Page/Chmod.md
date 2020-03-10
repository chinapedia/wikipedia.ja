> この記事は[Chmod](https://ja.wikipedia.org/wiki/Chmod)から翻訳されています。


**chmod**（change mode、チェンジモード）は、[UNIX](../Page/UNIX.md "wikilink")およびUNIX系[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")における[シェル](../Page/シェル.md "wikilink")コマンドの一種である。[ファイルや](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[ディレクトリ](../Page/ディレクトリ.md "wikilink")のファイルモード（[ファイルパーミッション](https://ja.wikipedia.org/wiki/ファイルパーミッション "wikilink")など）を変更するのに使われる。

## 歴史

`chmod` コマンドは、[AT\&T](../Page/AT&T.md "wikilink") の最初の [UNIX](../Page/UNIX.md "wikilink")（[Research Unix](https://ja.wikipedia.org/wiki/Research_Unix "wikilink") V1）に既に備わっており、今も UNIX 系オペレーティングシステムで使われている。

## 使用法

`chmod` コマンドのオプション形式は次の通り。

`$ chmod [`*`options`*`] `*`mode`*` `*`file1`*` ...`

現在のパーミッション設定を見るには、次のように入力する。

`$ ls -l`

## オプション

主なオプションとして、次のものがある。

  - `-R`: 再帰的にディレクトリとその配下のファイル群のモードを変更する。
  - `-v`: Verbose（冗長）モード。処理中の全ファイル名をリスト表示する。

## 文字列によるモード指定

`chmod` では、全パーミッションと特殊モードを mode パラメータで表現する。ファイルやディレクトリのモードを指定する1つの方法としてシンボリックモードがある。シンボリックモードは、3つの部分からなる文字列で表される。

`$ chmod [`*`references`*`][`*`operator`*`][`*`modes`*`] `*`file1`*` ...`

references はクラス（ユーザ、グループ、その他）を指定するのに使われる。references が指定されない場合、全クラスを意味する。以下の文字を使って指定する。

| Reference | クラス  | 説明                     |
| --------- | ---- | ---------------------- |
| `u`       | ユーザ  | ファイルの所有者               |
| `g`       | グループ | 所有者が属するグループ            |
| `o`       | その他  | グループ以外の全ユーザ            |
| `a`       | 全て   | 上記3つ全て。*ugo* と指定するのと同じ |

operator はモードの処理方法を指定する。

| Operator | 説明                                                                |
| -------- | ----------------------------------------------------------------- |
| `+`      | 指定されたモードを指定されたクラスに追加する。                                           |
| `-`      | 指定されたモードを指定されたクラスから削除する。                                          |
| `=`      | 指定されたモードが指定されたクラスの正確な内容となる。つまり、指定されなかったモードは削除され、指定されたモードだけが付与される。 |

modes はモードを指定する。基本パーミッションに対応して3つの基本モードがある。

| Mode | 名称         | 説明                                                                                                                                                                                |
| ---- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `r`  | リード        | ファイルを読み出し可能、ディレクトリ内容を参照可能                                                                                                                                                         |
| `w`  | ライト        | ファイルやディレクトリに書き込み可能                                                                                                                                                                |
| `x`  | 実行         | ファイルを実行可能、ディレクトリに移動可能                                                                                                                                                             |
| `X`  | 特殊実行       | パーミッション自体ではないが、x の代わりに使うことができる。ディレクトリについては現在のパーミッションに関係なく実行パーミッションを付与するが、ファイルについては（クラスに関係なく）現在のパーミッションで実行パーミッションが設定されている場合のみ実行パーミッションを付与する。operator が '+' で、-R オプションを使う場合のみ便利である。 |
| `s`  | setuid/gid | 後述                                                                                                                                                                                |
| `t`  | sticky     | 後述                                                                                                                                                                                |

これら3要素で構成される文字列がシンボリックモードでのパーミッション指定として認識される。複数の変更があるときは、それらをカンマで連結して指定すればよい。

### 例

次の例は、`sample` という名前のファイルまたはディレクトリについて、ユーザクラスおよびグループクラスのリードパーミッションとライトパーミッションを付与するものである。

``` console
$ chmod ug+rw sample
$ ls -ld sample
drw-rw----   2 unixguy  unixguy       96 Dec  8 12:53 sample
```

次の例は、全パーミッションを削除するもので、`sample` は読み出すことも書き込むことも実行することもできなくなる。

``` console
$ chmod a-rwx sample
$ ls -l sample
----------   2 unixguy  unixguy       96 Dec  8 12:53 sample
```

次の例は、ユーザおよびグループのパーミッションをリードと実行だけに設定する（ライトは不可とする）。

`コマンド実行前の sample のパーミッション`

``` console
$ ls -ld sample
drw-rw----   2 unixguy  unixguy       96 Dec  8 12:53 sample
$ chmod ug=rx sample
$ ls -ld sample
dr-xr-x---   2 unixguy  unixguy       96 Dec  8 12:53 sample
```

## 八進数によるモード指定

`chmod` コマンドは、三桁か四桁の[八進数でモードを指定できる](https://ja.wikipedia.org/wiki/八進記数法 "wikilink")。これを絶対モード指定と呼ぶ。例えば、次のように指定する。

`$ chmod 0664 sample`

sample というファイルの `setuid`、`setgid`、`sticky` ビットが設定されていない場合、これは以下と等価である。

`$ chmod 664 sample`

あるいは

`$ chmod +r,-x,ug+w sample`

## 特殊モード

`chmod` コマンドは、ファイルやディレクトリの追加パーミッション（あるいは特殊モード）も変更可能である。シンボリックモードでは `s` が *[setuid](https://ja.wikipedia.org/wiki/setuid "wikilink")* と *[setgid](https://ja.wikipedia.org/wiki/setgid "wikilink")* モードを表し、`t` が *[sticky](https://ja.wikipedia.org/wiki/スティッキービット "wikilink")* モードを表す。それぞれ、特定のクラスでのみ有効である。詳しくは[ファイルパーミッション](https://ja.wikipedia.org/wiki/ファイルパーミッション "wikilink")を参照されたい。

多くのオペレーティングシステムでは絶対モードでの特殊モード指定が可能だが、一部では不可能なOSもあり、その場合はシンボリックモードでしか指定できない。

## 例

  - `chmod +r file` – 全てのリードパーミッションを付与
  - `chmod -x file` – 全ての実行パーミッションを削除
  - `chmod u=rw,go= file` – 所有者にはリード/ライトパーミッションをセットし、グループおよびその他については全パーミッションを削除
  - `chmod +rw file` – 全てのリード/ライトパーミッションを付与
  - `chmod -R u+w,go-w docs/` – ディレクトリ docs とその配下の全ファイルについて、ユーザ（所有者）にはライトパーミッションを付与し、それ以外からはライトパーミッションを削除するよう変更
  - `chmod 666 file` – 全てのリード/ライトパーミッションを付与
  - `chmod 0755 file` – `u=rwx (4+2+1),go=rx (4+1 & 4+1)` と等価。`0` は特殊モードを指定しないことを意味する。
  - `chmod 4755 file` – `4` は *[setuid](https://ja.wikipedia.org/wiki/setuid "wikilink")* を意味する。
  - `find path/ -type d -exec chmod a-x {} \;` – path/ 配下の全ディレクトリについて、a-x を設定する（ファイルのみの場合は '-type f'）
  - `find path/ -type d -exec chmod 777 {} \;` – path/ 配下の全ディレクトリについて、全パーミッションを付与する
  - ` chmod -R u+rwX,g-rwx,o-rwx  `<directory> – 所有者パーミッションはディレクトリについては rwx、ファイルについては rw を設定し、それ以外のパーミッションは --- とする。

## 関連項目

  - [ファイルパーミッション](https://ja.wikipedia.org/wiki/ファイルパーミッション "wikilink")
  - [chown](https://ja.wikipedia.org/wiki/chown "wikilink") - ファイルやディレクトリの所有者（ユーザ）を変更するコマンド
  - [chgrp](https://ja.wikipedia.org/wiki/chgrp "wikilink") - ファイルやディレクトリのグループを変更するコマンド
  - [cacls](https://ja.wikipedia.org/wiki/cacls "wikilink") - [Microsoft Windows NTおよびその後継OSでの類似コマンド](../Page/Microsoft_Windows_NT.md "wikilink")。[アクセス制御リスト](https://ja.wikipedia.org/wiki/アクセス制御リスト "wikilink") (ACL) の変更を行う。
  - [ユーザー識別子](https://ja.wikipedia.org/wiki/ユーザー識別子 "wikilink")とグループ識別子

## 外部リンク

  - [GNU "Setting Permissions" manual](https://www.gnu.org/software/coreutils/manual/html_node/Setting-Permissions.html#Setting-Permissions)
  - [Solaris 9 chmod man page](https://docs.oracle.com/cd/E36784_01/html/E36870/chmod-1.html#scrolltoc)（英語）
  - [Mac OS X chmod man page](https://www.manpagez.com/man/1/chmod/) - [アクセス制御リスト](https://ja.wikipedia.org/wiki/アクセス制御リスト "wikilink")もサポートしている。
  - [CHMOD-Win 3.0](https://neosmart.net/CHMOD-Win/) — Windows の ACL と CHMOD のコンバーター（フリーウェア）

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink") [Category:1969年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1969年のソフトウェア "wikilink")