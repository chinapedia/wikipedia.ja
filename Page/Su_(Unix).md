> この記事は[Su \(Unix\)](https://ja.wikipedia.org/wiki/Su_\(Unix\))から翻訳されています。


[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")コマンドである**su**（エスユー、ス）は、再ログインすることなく、[シェル](../Page/シェル.md "wikilink")のユーザを切り替えるために利用される。[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")において、マシンの管理作業を行う際に[root権限を得るために頻繁に使用されるコマンドである](../Page/スーパーユーザー.md "wikilink")。[KDE](../Page/KDE.md "wikilink")や[GNOME](../Page/GNOME.md "wikilink")等のようなデスクトップ環境において、root権限が必要なコマンドを実行しようとすると、一般的にパスワード用の入力フィールドがポップアップする。

## 概要

suは一般的に、コマンドラインのターミナルから実行される。suを実行すると、切り替え先ユーザのパスワードが要求され、認証が成功した場合は、そのアカウントへのアクセス権限が与えられる。

``` console
johndoe@klinger:~$ su
Password:
root@klinger# exit
exit
johndoe@klinger:~$
```

関連するコマンドとして[sudo](https://ja.wikipedia.org/wiki/sudo "wikilink")がある。[sudo](https://ja.wikipedia.org/wiki/sudo "wikilink")を用いれば、別のユーザの権限でコマンドを実行できる。

あるユーザが、どのユーザの権限で、どのコマンドを実行されるかというは、一般的に/etc/sudoersで設定されている。 suを実行する際には切り替え先の権限のパスワードが要求されるのに対して、sudoを実行する際には自分のパスワードが要求される。 そのため、sudoを利用して作業をする人に対して切り替え先のユーザのパスワードを伝える必要がなく、ユーザーパスワードと管理者パスワードの両方を管理する必要がなく、パスワードが漏洩する危険性も軽減できる。[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")によっては、suを利用してroot権限になることを禁止しており、root権限でコマンドを実行する場合は常に[sudo](https://ja.wikipedia.org/wiki/sudo "wikilink")を先頭につけることもある。

システム管理者は、不正な利用者によってroot権限を取得されないように、[root](https://ja.wikipedia.org/wiki/root "wikilink")のパスワードを慎重に決定しなければならない。 [Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")システムによっては[Wheel](https://ja.wikipedia.org/wiki/Wheel "wikilink")グループが存在し、[Wheel](https://ja.wikipedia.org/wiki/Wheel "wikilink")グループに所属していないユーザはsuコマンドでroot権限を得ることができない。 この仕組みによって、侵入者がroot権限を得る可能性を軽減できる。 しかしながら、[GNU](../Page/GNU.md "wikilink") suは思想的な理由により[Wheel](https://ja.wikipedia.org/wiki/Wheel "wikilink")グループをサポートしない。

[Windows XPにもrunasという類似コマンドが存在する](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")\[1\]。

## 脚注

## 外部リンク

  - [Manpage of SU](https://linuxjm.osdn.jp/html/GNU_sh-utils/man1/su.1.html) GNU 版 su、JM Project
  - [su Command](https://docs.oracle.com/cd/E19253-01/819-1211/6n3j834aq/index.html) man page（SunOS リファレンスマニュアル）
  - [su(1)](https://nixdoc.net/man-pages/HP-UX/man1/su.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink")

1.  [runas](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/runas.mspx)