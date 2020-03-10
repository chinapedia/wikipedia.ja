> この記事は[GNU Core Utilities](https://ja.wikipedia.org/wiki/GNU_Core_Utilities)から翻訳されています。


**GNU Core Utilities**または**Coreutils**は[Unix系](../Page/Unix系.md "wikilink")の[OSで中心的](../Page/オペレーティングシステム.md "wikilink") (core) な[cat](https://ja.wikipedia.org/wiki/Cat_\(UNIX\) "wikilink")、[ls](https://ja.wikipedia.org/wiki/Ls_\(UNIX\) "wikilink")、[rmなどのユーティリティ群のパッケージ](https://ja.wikipedia.org/wiki/rm_\(UNIX\) "wikilink")、ないし、その開発とメンテナンスを行う[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の1サブプロジェクトである。以前はfileutils、textutils、shellutilsに分かれていた。

## オプション

Coreutilsに含まれるコマンドに共通の[オプション](https://ja.wikipedia.org/wiki/オプション "wikilink")として、以下のものがある。

  - \--help そのコマンドのヘルプを表示する
  - \--version バージョンを出力する
  - \-- これ以降の引数をオペランドとして扱う。

Coreutilsコマンドは、環境変数`POSIXLY_CORRECT`が設定されていないかぎり、引数がどのような順序で書かれていても、オプションを先に解釈し、オペランドを後で解釈する。例として "ls /usr -l" と "ls -l /usr" は同じ意味であり、どちらも /usr の内容が長い形式でリスティングされる。（これは、オプションを後に書くことでオプションの解釈が後になったりしない、この例では -l の効果が /usr の表示に及ばなくなったりはしない、という意味である。[UNIX](../Page/UNIX.md "wikilink")のツールでは、このような場合のふるまいはまちまちであることが多い）

## コマンド

Coreutilsにはバージョン5.2.1の段階で以下のコマンドが含まれる:

**File Utilities**

  - [chgrp](https://ja.wikipedia.org/wiki/chgrp "wikilink") ファイルの所有グループを変更する
  - [chown](https://ja.wikipedia.org/wiki/chown "wikilink") ファイルの所有者を変更する
  - [chmod](https://ja.wikipedia.org/wiki/chmod "wikilink") ファイル、またはディレクトリのアクセス権を変更する
  - [cp](https://ja.wikipedia.org/wiki/cp_\(UNIX\) "wikilink") ファイル、またはディレクトリをコピーする
  - [dd](https://ja.wikipedia.org/wiki/dd_\(UNIX\) "wikilink") ファイルのコピーと変換を行う
  - df ディスクの空き容量を表示する
  - dir lsと同等
  - dircolors lsの表示色を設定する
  - install ファイルをコピーし、属性を設定する
  - [ln](https://ja.wikipedia.org/wiki/ln_\(UNIX\) "wikilink") リンクを作成する
  - [ls](https://ja.wikipedia.org/wiki/Ls_\(UNIX\) "wikilink") ディレクトリに含まれるファイル一覧を表示する
  - [mkdir](https://ja.wikipedia.org/wiki/mkdir "wikilink") ディレクトリを作成する
  - mkfifo FIFO(名前付きパイプ)を作成する
  - mknod 特殊ファイル([デバイスファイル](../Page/デバイスファイル.md "wikilink")など)を作成する
  - [mv](https://ja.wikipedia.org/wiki/mv_\(UNIX\) "wikilink") ファイルを移動する
  - [rm](https://ja.wikipedia.org/wiki/rm_\(UNIX\) "wikilink") ファイルを削除する
  - [rmdir](https://ja.wikipedia.org/wiki/rmdir "wikilink") 空のディレクトリを削除する
  - shred ファイルの内容を破壊し、復旧できなくする
  - sync ファイルのキャッシュを物理的に書き込む
  - [touch](https://ja.wikipedia.org/wiki/touch_\(UNIX\) "wikilink") ファイルの時刻を変更する
  - vdir 詳細なディレクトリ内容を表示する(ls -lと同等)

**Text utilities**

  - [cat](https://ja.wikipedia.org/wiki/Cat_\(UNIX\) "wikilink") ファイルの中身を表示する、またはファイルを連結して表示する
  - cksum ファイルのチェックサムとファイルサイズを計算する
  - comm 2つのファイルについて行ごとに比較する
  - csplit ファイルを文脈ベースで分割する
  - [cut](https://ja.wikipedia.org/wiki/cut "wikilink") 各行から選択した部分を表示する
  - expand タブをスペースに変換する
  - [fmt](https://ja.wikipedia.org/wiki/fmt "wikilink") テキストを段落に整形する
  - fold 入力行を指定された幅にあわせて折りたたむ
  - [head](https://ja.wikipedia.org/wiki/head "wikilink") ファイルの最初の部分を表示する
  - join 二つのファイルを読み、フィールドが共通な行を結合する
  - md5sum [MD5](../Page/MD5.md "wikilink") ハッシュチェックサムを計算・チェックする
  - nl 行番号を付けてファイルを出力する
  - od ファイルを 8 進数 (または他の形式) で出力する
  - paste ファイルを行単位でマージする
  - pr 印刷用にファイルのページづけ・段組みを行う
  - ptx 整列済み索引を作成する
  - [sha1sum](https://ja.wikipedia.org/wiki/sha1sum "wikilink") [SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink") ハッシュチェックサムの計算と検証を行う
  - [sort](../Page/Sort_\(UNIX\).md "wikilink") テキストファイルを行単位でソートする
  - [split](https://ja.wikipedia.org/wiki/split "wikilink") ファイルを決まった大きさに分割する
  - sum チェックサムとブロック数を表示する
  - tac ファイルを結合して逆順に表示する
  - [tail](https://ja.wikipedia.org/wiki/tail "wikilink") ファイルの末尾の部分を表示する
  - [tr](../Page/Tr_\(UNIX\).md "wikilink") 文字の変換・削除や、連続する文字の圧縮を行う
  - tsort 有向グラフのトポロジカルなソートを行う
  - unexpand スペースをタブに変換する
  - [uniq](https://ja.wikipedia.org/wiki/uniq "wikilink") ソートされたファイルから重複する行を削除する
  - [wc](https://ja.wikipedia.org/wiki/wc_\(UNIX\) "wikilink") ファイルのバイト数・単語数・行数を表示する

**Shell utilities**

  - [basename](https://ja.wikipedia.org/wiki/basename "wikilink") ファイル名からディレクトリと拡張子を取り去る
  - [chroot](https://ja.wikipedia.org/wiki/chroot "wikilink") ルートディレクトリを変更する
  - [date](https://ja.wikipedia.org/wiki/Date_\(UNIX\) "wikilink") 現在のOS日時を表示、または変更する
  - [dirname](https://ja.wikipedia.org/wiki/dirname "wikilink") パスからディレクトリ名以外の部分を除去する
  - du ファイルのディスク使用量を見積もる
  - [echo](https://ja.wikipedia.org/wiki/エコー_\(コンピュータ\)#echo.E3.82.B3.E3.83.9E.E3.83.B3.E3.83.89 "wikilink") 1行のテキストを表示する
  - [env](https://ja.wikipedia.org/wiki/env "wikilink") 環境変数を一時的に設定、または表示する
  - [expr](https://ja.wikipedia.org/wiki/expr "wikilink") 式を評価する
  - factor 数値を素因数分解して素数の約数を表示する
  - [false](https://ja.wikipedia.org/wiki/false_\(UNIX\) "wikilink") 何もせずに失敗の値を返す
  - groups ログインしているユーザーのグループを表示する
  - hostid 現在のホストの識別値を表示する
  - [id](https://ja.wikipedia.org/wiki/id_\(UNIX\) "wikilink") 現在のユーザID名とグループID名を表示する
  - link ファイルの新しい名前を作成する
  - logname ユーザーのログイン名を表示する
  - [nice](https://ja.wikipedia.org/wiki/nice_\(UNIX\) "wikilink") プロセスの優先度を変更する
  - nohup ログアウト後もコマンドの実行が継続することを許可する
  - pathchk ファイル名の可搬性 (portability) をチェックする
  - pinky fingerコマンドの軽量版
  - printenv 環境変数の全部あるいは一部を表示する
  - printf データの表示形式を変換して表示する
  - [pwd](https://ja.wikipedia.org/wiki/pwd "wikilink") カレントディレクトリの名前を表示する
  - readlink シンボリックリンクの値を表示する
  - seq 通し番号を表示する
  - [sleep](https://ja.wikipedia.org/wiki/sleep_\(UNIX\) "wikilink") 指定された時間休止する
  - stat ファイルの状態を得る
  - stty 端末の行設定を変更、表示する
  - [tee](https://ja.wikipedia.org/wiki/tee_\(UNIX\) "wikilink") 標準入力から読んだ内容を標準出力とファイルとに書き出す
  - test ファイル形式のチェックや値の比較を行う
  - [true](https://ja.wikipedia.org/wiki/true_\(UNIX\) "wikilink") 何もせずに成功の値を返す
  - [tty](https://ja.wikipedia.org/wiki/tty "wikilink") 端末名を表示する
  - [uname](https://ja.wikipedia.org/wiki/uname "wikilink") システムの情報を表示する
  - unlink 名前を削除し、場合によってはそれが参照しているファイルも削除する
  - users 現在ログインしているユーザーを表示する
  - [who](https://ja.wikipedia.org/wiki/who_\(UNIX\) "wikilink") 現在ログインしているユーザーを詳細に表示する
  - [whoami](https://ja.wikipedia.org/wiki/whoami "wikilink") ユーザーのログイン名を表示する
  - [yes](https://ja.wikipedia.org/wiki/yes_\(UNIX\) "wikilink") killシグナルが送られるまで文字を表示し続ける

他に、UNIXの慣例により、testの別名として \[ がある。シェルのコマンドとして if \[ *expression* \] といったように書くためのものである。

## 関連項目

  - [BusyBox](https://ja.wikipedia.org/wiki/BusyBox "wikilink") - （Coreutilsと直接の関連は全く無い、汎用のシステムであるが）多数のプログラムを単一のバイナリに「詰め込む」システム。
  - [GNU Binutils](../Page/GNU_Binutils.md "wikilink")

## 外部リンク

  - [GNUのページ](https://www.gnu.org/software/coreutils/coreutils.html)

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")