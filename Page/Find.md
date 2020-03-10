> この記事は[Find](https://ja.wikipedia.org/wiki/Find)から翻訳されています。


ここでは主に[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")プラットフォームで利用できるディレクトリ検索プログラムである**`find`**（ファインド）について記述する。[ファイルシステム](../Page/ファイルシステム.md "wikilink")の1つ以上の[ディレクトリ](../Page/ディレクトリ.md "wikilink")ツリー上で[検索](../Page/検索.md "wikilink")を行い、ユーザーの指定した基準にマッチする[ファイルを探す](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")。既定の動作としては現在の[ワーキングディレクトリ配下にある全ファイルをリストアップする](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")。さらに `find` はマッチした各ファイルに対して何らかのアクションを実行するよう指定できるため、大量のファイルを操作することができる非常に強力なプログラムであるといえる。[正規表現](../Page/正規表現.md "wikilink")によるマッチングもサポートしている。

## find における正規表現文法について

find は評価式「`-regex`」や「`-iregex`」などを用いることで正規表現によるパス名のマッチングを行うことが可能であるが、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")版のfindは複数の正規表現文法に対応している。そこで、GNU findは、既定では正規表現を[GNU Emacsの正規表現として解釈し](https://ja.wikipedia.org/wiki/GNU_Emacs "wikilink")、他の異なる文法についてはコマンドラインオプション「`-regextype`」の引数によって解釈を切り替えて対応している。

## 例

  - カレントディレクトリでの検索

`find . -name 'my*'`

  -
    この例では、カレントディレクトリ（ピリオドで表されている）とその配下にあるファイルとディレクトリについて名前が「*my*」で始まるものを探す。クォートはfindに渡す前のシェルパターン「my\*」をシェルが解釈して、カレントディレクトリにある *my* で始まるファイル名リストに置き換えてしまうのを防ぐために必要となる。

  - ファイルのみの検索

`find . -name my\* -type f`

  -
    この場合、上の例での検索結果から通常のファイルのみを絞り込む。従ってディレクトリや[スペシャルファイル](https://ja.wikipedia.org/wiki/スペシャルファイル "wikilink")やパイプやシンボリックリンクなどは除外される。シェルパターン中で「*\**」の前にバックスラッシュを付けているのは、前の例と同じ理由を回避する別の書き方である。また、式は左から順に処理されるため、通常のファイルだけに絞り込んでから検索を行うには式の順序を並び替えて「`-type f -name my\*`」とする。当然、結果は同じになる。
  - アクション指定
    これまでの例は検索結果をリスト表示するだけであった。これは既定のアクションとして `-print` を実行するようになっているためである。なお、初期の `find` コマンドには既定のアクションが存在しなかったため、何も指定しないと検索をするだけでその結果は表示されなかった。

`find . -type f -name 'my*' -ls`

  -
    この場合、単にファイル名だけでなく、[lsコマンド相当の情報を表示する](https://ja.wikipedia.org/wiki/ls_\(UNIX\) "wikilink")。

  - 全ディレクトリ検索

`find / -type f -iname myfile -print`

  -
    この場合、そのコンピュータ上の通常ファイルから名前が「*myfile*」や「*MyFile*」などとなっているものをすべて検索する。「`-iname`」は大文字小文字を区別しない検索式。単にデータファイルを探すだけなら、「/」を指定するのは非常に時間がかかる可能性があり、賢い方法ではない。

  - ディレクトリ指定

`find /home/brian -type f -name myfile -print`

  -
    この場合、*/home/brian* ディレクトリ（ユーザー *brian* の[ホームディレクトリ](https://ja.wikipedia.org/wiki/ホームディレクトリ "wikilink")）配下にある通常ファイルの中から、*myfile* という名前のものを探す。このように可能な限り範囲を狭めてコマンドを実行すべきである。

  - 複数ディレクトリの検索

`find local /tmp -type d -name mydir -print`

  -
    この場合、検索範囲はカレントディレクトリにある「*local*」というサブディレクトリと「*/tmp*」ディレクトリである。その中からディレクトリのみを対象とし、名前が「*mydir*」であるもの探して表示する。
  - エラーを無視する
    ユーザーが[rootではない場合](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")、アクセス権限などによるエラーを表示させたくない場合がある。その場合は、以下のようにしてシェルで標準エラー出力を捨てればよい。

`find / -type f -name myfile -print 2> /dev/null`

  - 異なるファイル名のいずれかを探す

`find . -type f `\(-name '*jsp' -or -name \*java\)` -ls`

  -
    この例では名前が 'jsp' または 'java' で終わるファイルを探す。括弧が必要であることに注意。また、"or" を "o" と略記することも可能。大抵のシェルでは丸括弧を "\(" や "\)" のようにエスケープする必要がある（シェルの特殊文字として解釈されないようにするため）。`-ls` と `-or` は全てのバージョンの `find` で使えるわけではない。

  - コマンド実行

`find /var/ftp/mp3 -type f -iname '*.mp3' -exec chmod 744 {} \;`

  -
    この場合、ディレクトリ */var/ftp/mp3* にあって名前が「*.mp3*」や「*.MP3*」などで終わるすべてのMP3ファイルについて、[ファイルパーミッション](https://ja.wikipedia.org/wiki/ファイルパーミッション "wikilink")を変更する。アクションは ` -exec  `[`chmod`](https://ja.wikipedia.org/wiki/chmod "wikilink")`  744 {} \; ` の部分で指定されている。MP3ファイルそれぞれについて、`chmod 744 {}` というコマンドの `{}` の部分をファイル名に置き換えたものが実行される。セミコロン（シェルが解釈するのを防ぐためエスケープされている）がコマンドの終わりを示している。なお、`744` というパーミッションは普通に記せば `rwxr--r--` であり、ファイル所有者は完全なアクセス（読み書きと実行）が可能だが、それ以外のユーザーは読むことしかできない。

  - [xargs](https://ja.wikipedia.org/wiki/xargs "wikilink")との連携

`find /var/ftp/mp3 -type f -iname '*.mp3' -print | xargs chmod 744`

  -
    上の`-exec`では、該当するファイル1つにつき一度ずつプロセスを起動することとなり、効率が悪い。いったん`-print`で出力し、[`xargs`](https://ja.wikipedia.org/wiki/xargs "wikilink")によってコマンドラインとして渡せるだけの量をまとめて渡すことで、効率化することができる。なお、GNUプロジェクト版のfindには、ファイル名を[ヌル文字](https://ja.wikipedia.org/wiki/ヌル文字 "wikilink")区切りで出力する`-print0`オプションがあり、`xargs -0`で解釈させることで、[ホワイトスペース](https://ja.wikipedia.org/wiki/ホワイトスペース "wikilink")の入ったファイル名についても正常に処理可能となる。
  - 文字列検索
    以下の例では、/tmp 配下にある全ファイルについて、ファイルの中身に "search string" という文字列がないか検索するものである。

`find /tmp -exec grep "search string" '{}' /dev/null \; -print`

  -
    `/dev/null` は、ファイル名を表示するために必要となる。そうしないと、[grep](https://ja.wikipedia.org/wiki/grep "wikilink")でマッチしたテキスト部分しか表示されない。等価な機能として grep の "-H" オプションや "--with-filename" オプションを使うことも出来る。

`find /tmp -exec grep -H "search string" '{}' \; -print`

  -
    GNU grep では、同等の処理を単独で以下のように行うこともできる。

`grep -R /tmp "search string"`

  -
    次の例は、jsmith というユーザーのホームディレクトリで "LOG" という文字列を検索したものである。

`find ~jsmith -exec grep "LOG" '{}' /dev/null \; -print`
`/home/jsmith/scripts/errpt.sh:cp $LOG $FIXEDLOGNAME`
`/home/jsmith/scripts/errpt.sh:cat $LOG`
`/home/jsmith/scripts/title:USER=$LOGNAME`

  -
    次の例では、カレントディレクトリ配下で全ての XML ファイルについて "ERROR" という文字列を検索する。

`find . -type f -iname '*.xml' -exec grep "ERROR" '{}' \; -print`

  -
    検索文字列を囲むダブルクオート (" ") やファイル名に対応する括弧を囲むシングルクオート (' ') はこの例では無くてもよいが、空白を含む文字列や特殊文字を含む文字列を指定する際に必要となる。

  - あるユーザーの所有するファイルを検索する

`find . -user `<userid>

## Windows/MS-DOSコマンドとしてのfind

[Windowsコマンド](https://ja.wikipedia.org/wiki/cmd.exe "wikilink")（[MS-DOS](../Page/MS-DOS.md "wikilink")[コマンド](../Page/COMMAND.COM.md "wikilink")）としての[findは](https://ja.wikipedia.org/wiki/find_\(DOS\) "wikilink")、ちょうどUnixコマンドでいうところの[fgrepのような文字列検索を行う](https://ja.wikipedia.org/wiki/grep "wikilink")。実行すると検索文字列が含まれる行が標準出力に出力される。ちなみにgrepに相当するコマンドはfindstrである。

## 外部リンク

  - [find(1L)](https://linuxjm.osdn.jp/html/GNU_findutils/man1/find.1.html) JM Project
  - [find(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvr0c/index.html) man page（SunOS リファレンス・マニュアル）
  - [find(1)](https://nixdoc.net/man-pages/HP-UX/man1/find.1.html) man page（HP-UX リファレンス）
  - [Official webpage for GNU find](https://www.gnu.org/software/findutils/manual/html_mono/find.html)

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink") [Category:情報検索システム](https://ja.wikipedia.org/wiki/Category:情報検索システム "wikilink")