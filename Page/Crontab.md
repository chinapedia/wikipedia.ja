> この記事は[Crontab](https://ja.wikipedia.org/wiki/Crontab)から翻訳されています。


**`crontab`**（**クロンタブ**、あるいはクローンタブ、クーロンタブとも）コマンドは[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) において、[コマンドの定時実行のスケジュール管理を行うために用いられるコマンドである](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。標準入力からコマンド列を読み取り、crontabと呼ばれるファイルにそれを記録する。この記録を元に定時になると、その命令内容を読み取り、実行が行われる。cronという名称はギリシア語の[クロノス](https://ja.wikipedia.org/wiki/クロノス_\(時間の神\) "wikilink") () に由来するという説がある（Command Run ON の略という説も）。日本語ではクーロンという読みが慣習的に広く用いられているが、英語では通常クロンまたはクローンと発音する\[1\]。

一般に**`crontab`**コマンドで編集されたスケジュール内容は、`crond`[デーモンにより実行される](../Page/デーモン_\(ソフトウェア\).md "wikilink")。`crond`はバックグラウンドで稼動し、毎分ごとに実行すべきスケジュールがないか確認し、もし実行すべきジョブがあれば、それを実行する。このジョブは「cron job」とも呼ばれる。

## crontabファイル

crontabファイルには、ジョブのリストおよびcronデーモンへの命令が書かれる。各ユーザは自身の個人用crontabファイルを持つ。さらに、システム全体用のcrontabファイルも存在する（/etc またはそのサブディレクトリ下）。このシステム全体用のcrontabはシステム管理者のみが編集可能なものとなっている。

crontabファイルの各行は、空白またはタブで区切られたフィールド列から構成される特有の形式となっている。各フィールドには単一もしくは複数の値が書かれる。

### 特殊記号

一フィールド中で複数の値を指定するには、いくつかの方法がある:

  - コンマ (,) で値のリストを指定する: 例) "1,3,4,7,8"
  - ダッシュ (-) で値の範囲を指定する: 例) "1-6" （"1,2,3,4,5,6"という指定と同じ意味）
  - アスタリスク (\*) でそのフィールドで取りうる全ての値を表現する。例えば、時をあらわすフィールドでは「毎時」という意味となる。

cron実装によっては、いくつかの追加拡張をおこなっているものもある。スラッシュ (/) で一定値ごとの間隔を表現する: 例) 時フィールドでの"\*/3"指定は"0,3,6,9,12,15,18,21"と同じ意を示す。つまり、"\*"の場合は毎時をあらわすが、"/3"を指定すると、\*で適用される値の範囲内における1番目・4番目・7番目...といった意を表す。

### フィールド

    # （行頭の # マークはコメント行を示す）
    # +------------ 分 (0 - 59)
    # | +---------- 時 (0 - 23)
    # | | +-------- 日 (1 - 31)
    # | | | +------ 月 (1 - 12)
    # | | | | +---- 曜日 (0 - 6) (日曜日=0)
    # | | | | |
    # * * * * * 実行されるコマンド

注:

1.  「曜日」（第5フィールド）では0, 7の両方とも日曜日の意となる。
2.  直感にあわないものの、「日」（第3フィールド）および「曜日」（第5フィールド）が同時に指定された場合、どちらかが満たされた場合両方でコマンドが実行される。以下の例も参照のこと。

第6フィールド以降の行の残りの箇所には実行すべきコマンドを指定する。

### 例

#### AIX システムにおけるadm ユーザのcrontabファイル

`#{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}`
`# SYSTEM ACTIVITY REPORTS`
`# 平日・午前8時-午後5時の活動履歴は20分おき`
`# 土曜日・日曜日の活動履歴は毎時`
`# 平日・午後6時-午前7時の活動履歴は毎時`
`# 平日 18:05 に概要報告を準備する`
`#{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}{{=}}`
`0,20,40 8-17 * * 1-5 /usr/lib/sa/sa1 1200 3 &`
`0 * * * 0,6 /usr/lib/sa/sa1 &`
`0 18-7 * * 1-5 /usr/lib/sa/sa1 &`
`5 18 * * 1-5 /usr/lib/sa/sa2 -s 8:00 -e 18:01 -i 3600 -ubcwyaqvm &`

#### よくあるミス

  - 最もよく見られるミスの一つは、cron ジョブのテストの際に見られる。テストの際には、少なくとも2分以上先の時刻を実行時刻として指定する必要がある。これはcrontabファイルの再読み込みは、編集後の次の分時にのみ行われるためである。例えば、現在時刻が12:05である場合、crontabファイルの再読み込みが12:06:01に行われるため、次のジョブをスケジュールするには少なくとも12:07以降を指定する必要がある。これに対処してテストをすぐに行うには、cronサービス自体を再起動する方法もある。
  - crontabからX Window Systemアプリケーションを起動するというミスも多く見受けられる。この問題は、cronからはX環境が実行可能かどうかが不明であり、crontabは主としてコンソールのみを対象としたプログラムの実行を意図しているためもあり、Xの情報を受け渡すことができない点にある。これに対応するには2つの方法がある。crontabの冒頭に`DISPLAY=:0.0`というような環境変数設定を行うか、アプリケーション実行引数に`--display :0.0`オプションを付けるかである。:0.0 は一例であり、どのディスプレイに出力すべきかは、`echo $DISPLAY` といったコマンドを実行して確認しておく必要がある。
  - よくあるミスのひとつは、コマンド指定においてエスケープせずに「%」記号を使うことで、これはエスケープする必要がある。

`# ミス:`
``1 2 3 4 5 touch ~/error_`date "+%Y%m%d"`.txt``

この場合、デーモンからは右のような[エラーメッセージ](https://ja.wikipedia.org/wiki/エラーメッセージ "wikilink")がメール送信される:「/bin/sh: unexpected EOF while looking for \`」

以下のように修正すると良い

`# エスケープしたもの:`
`1 2 3 4 5 touch ~/right_$(date +\%Y\%m\%d).txt`

  - 以下も別のよくあるミスのひとつである:

`# 夏時間移行時に備える`
`59 1 1-7 4 0 /root/shift_my_times.sh`

一見すると、上記は4月第一日曜日の午前1時59分にコマンドshift_my_times.shを実行するように見えるが、そうではなく、4月1日から4月7日までの毎日、および、4月中の日曜日全てで実行されてしまう。

これを書き直すとすれば、以下のようにするのが一つの方法である。

`# 夏時間移行に備える`
``59 1 1-7 4 * test `date +\%w` = 0 && /root/shift_my_times.sh``

  - また、別のミスの例としては、2時間毎にジョブを実行しようとして、以下のように書くと、

`# ログファイルに日付を追加`
`* 0,2,4,6,8,10,12,14,16,18,20,22 * * * date >> /var/log/date.log`

これは、各偶数時に毎分実行されてしまう。

この意図を表現するには以下のようにする:

`# 毎2時間おきに date コマンドを実行`
`0 0,2,4,6,8,10,12,14,16,18,20,22 * * * date >> /var/log/date.log`

`# もっと簡潔に書くと:`
`0 */2 * * * date >> /var/log/date.log`

### Emailの抑止

crontab により実行されたコマンドから出力が行われると、cron デーモンは通常その出力結果をユーザにメールで配送する。

  - ある特定のコマンドの出力を抑止するには、その出力を [`Crontab//dev/null`](https://ja.wikipedia.org/wiki/Crontab/dev/null "wikilink") へのリダイレクトとすることでできる。crontab 経由の実行コマンド出力のメールを完全に止めるには、実行コマンド全てに、[標準出力](https://ja.wikipedia.org/wiki/標準出力 "wikilink")を`/dev/null`にリダイレクトした上で標準エラー出力も標準出力へのリダイレクトとするような、以下のリダイレクトを加える。ただし、何らかのエラーが発生したとしても、何の出力も得られない。

`>/dev/null 2>&1`

  - 現在広く使われている[Vixie cronでは](https://ja.wikipedia.org/wiki/Vixie_cron "wikilink")、crontabファイルの冒頭に以下の記述を加えるだけで、全てのメール通知を止めることができる。

`MAILTO=""`

## crontabコマンド

ジョブのスケジュールを実際にcronデーモンに伝えるには**crontabコマンド**を使う。crontabファイル（例:**example.crontab**）を作成して、crontabコマンドの引数として指定する（`crontab example.crontab`）。もしくは、引数無しで起動した上で、標準入力からコマンドを直接指定することもできる。

## 脚注

<div class="references-small">

<references/>

</div>

## 関連項目

  - [at](../Page/At_\(UNIX\).md "wikilink"): ある時刻に一回だけコマンドを実行する
  - [anacron](https://ja.wikipedia.org/wiki/anacron "wikilink"): 一定時間の経過を見て、周期的にジョブを実行する
  - [launchd](https://ja.wikipedia.org/wiki/launchd "wikilink"): [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") / [Darwin上のcron代替デーモン](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")

## 外部リンク

  - **マニュアル**
      - [Crontab : Scheduling Tasks](https://math-linux.com/linux/tip-of-the-day/article/crontab-scheduling-tasks)
      - [Computer Hope](https://www.computerhope.com/unix/ucrontab.htm) Linux / UNIX の crontab コマンドの情報
      - [Opengroupの crontab 仕様](https://pubs.opengroup.org/onlinepubs/009695399/utilities/crontab.html) - 公式の [UNIX 03](https://ja.wikipedia.org/wiki/UNIX_03 "wikilink") 文書
      - [Crontab - Reference and Examples at mkaz.com](https://gist.github.com/mkaz/69066bd0c5e45515a264)
      - [crontab(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvqu7/index.html) man page（SunOS リファレンスマニュアル）
      - [crontab(1)](https://nixdoc.net/man-pages/HP-UX/man1/crontab.1.html) man page（HP-UX リファレンス）
  - **ソフトウェア**
      - [Cron for Windows](http://www.kalab.com/freeware/cron/cron.htm)
      - [CVSweb for FreeBSD's cron](https://svnweb.freebsd.org/base/head/usr.sbin/cron/) - 1993年の[ポール・ヴィクシー](../Page/ポール・ヴィクシー.md "wikilink")による[Vixie cron](https://ja.wikipedia.org/wiki/Vixie_cron "wikilink") 3.0 リリース
      - [fcron](http://fcron.free.fr/) - vixiecron および anacron の拡張代替実装 ([GPL](../Page/GNU_General_Public_License.md "wikilink"))

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")

1.  [YouTube - crontab](http://www.youtube.com/results?search_query=crontab) プレゼンテーション等