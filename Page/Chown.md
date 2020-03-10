> この記事は[Chown](https://ja.wikipedia.org/wiki/Chown)から翻訳されています。


**`chown`**（シーエイチオウン、チェンジオーナー）は、[Unix系](../Page/Unix系.md "wikilink")システムでファイルの所有者（<span style="text-decoration:underline;">own</span>er）を変更（<span style="text-decoration:underline;">ch</span>ange）するコマンド。多くの実装では、[スーパーユーザー](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")でないと実行できない。一般ユーザーは [`chgrp`](https://ja.wikipedia.org/wiki/chgrp "wikilink") でグループを変更することができる。

## 使用法

`chown` コマンドの大まかな構文は以下の通り。

  -
    chown \[-hHLPR\] \[*user*\]\[:*group*\] *target1* \[*target2* ..\]

<!-- end list -->

  - オプションの *`user`* パラメータは、対象ファイル群の新たな所有ユーザーを指定する。
  - オプションの *`group`* パラメータ（コロン `:` が必ず前置される）は、対象ファイル群を関連付ける新たなグループを指定する。
  - *`target`* パラメータ（複数指定可）はユーザーやグループを変更したいファイルまたはディレクトリを指定する。

### オプション

  - `-h`
    システムがシンボリックリンクの[ユーザー識別子](https://ja.wikipedia.org/wiki/ユーザー識別子 "wikilink")をサポートしている場合、指定された対象ファイルが[シンボリックリンク](https://ja.wikipedia.org/wiki/シンボリックリンク "wikilink")なら、シンボリックリンク自身のユーザー識別子をセットしようとする。同様にシステムがシンボリックリンクの[グループ識別子](https://ja.wikipedia.org/wiki/グループ識別子 "wikilink")をサポートしている場合、指定された対象ファイルがシンボリックリンクなら、シンボリックリンク自身のグループ識別子をセットしようとする。システムがシンボリックリンクのユーザー識別子やグループ識別子をサポートしていない場合、指定されたファイルがシンボリックリンクなら、chown はそのファイルについては何も行わず、それ以降の対象ファイルの操作も行わない。ちなみに、このオプションが指定されていない場合は、シンボリックリンクが参照しているファイルを操作する。
  - `-H`
    `-R` と共に指定されると、指定されたファイルがディレクトリを参照しているシンボリックリンクの場合、そのディレクトリと配下の全ファイルの所有者（およびグループ）を変更する。配下にディレクトリへのシンボリックリンクがあっても再帰しない。
  - `-L`
    `-R` と共に指定されると、指定されたファイルがディレクトリを参照しているシンボリックリンクの場合、そのディレクトリと配下の全ファイルの所有者（およびグループ）を変更する。配下にディレクトリへのシンボリックリンクがあったら再帰する。
  - `-P`
    `-R` と共に指定されると、コマンド行で指定されたファイルやディレクトリを走査していった先で遭遇したシンボリックリンクについて、シンボリックリンク自身の所有者（およびグループ）を変更する（システムがそのような機能をサポートしている場合）。シンボリックリンクを再帰的に追うことはしない。
  - `-R`
    再帰的にファイルの所有者とグループを変更する。コマンド行でディレクトリが指定されると、そのディレクトリとその配下の全ファイルを操作する。`-H`、`-L`、`-P` のどれも指定しない場合、どのオプションの動作をデフォルトとするかは規定されておらず、システムによって異なる。

### 注意点

  - *`user`* または *`group`* のどちらかは必ず指定する必要がある。どちらも指定されないと `chown` コマンドは正しく動作しない。
  - *`user`* および *`group`* はシンボル名でも識別子（すなわち、[ユーザー識別子](https://ja.wikipedia.org/wiki/ユーザー識別子 "wikilink")や[グループ識別子](https://ja.wikipedia.org/wiki/グループ識別子 "wikilink")）でもよい。

## 使用例

このコマンドは、[スーパーユーザー](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")として実行する必要がある。一般ユーザーは[sudo](https://ja.wikipedia.org/wiki/sudo "wikilink")コマンドを用いて実行するべきであろう。

`# chown root /var/run/httpd.pid`

これは、 `/var/run/httpd.pid` の所有者を 'root' （スーパーユーザーの標準的なシンボル名）に変更している。

`# chown nobody:nobody /tmp /var/tmp`

`/tmp` と `/var/tmp` の所有者とグループを 'nobody' に変更している（よいことではない）。

`# chown :512 /home`

`/home` のグループ識別子を 512 に変更している（512 にグループ名が対応しているかどうかは関知しない）。

`# chown -R us base`

`base` の所有者を 'us' にし、それを再帰的(`-R`)に適用する。

## 関連項目

  - [chmod](https://ja.wikipedia.org/wiki/chmod "wikilink")
  - [chgrp](https://ja.wikipedia.org/wiki/chgrp "wikilink")

## 外部リンク

  - [The chown Command](http://www.linfo.org/chown.html) by The Linux Information Project (LINFO)

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")