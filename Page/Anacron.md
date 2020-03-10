> この記事は[Anacron](https://ja.wikipedia.org/wiki/Anacron)から翻訳されています。


**anacron** は、[cron](../Page/Crontab.md "wikilink") が行うような周期的コマンドスケジューリングを実施する[プログラムであるが](../Page/プログラム_\(コンピュータ\).md "wikilink")、システムが連続的に動作し続けることを前提としない。したがって、毎日24時間動作し続けるわけではないシステムでも、日単位・週単位・月単位などのジョブの制御を行える。anacron は、Christian Schwarz が考案し、[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")向けに[Perl](../Page/Perl.md "wikilink")で実装したのが最初である。現在は Itai Tzur が [C言語](../Page/C言語.md "wikilink")で実装したものになっており、Sean 'Shaleh' Perry が活発に保守している。

anacron は、起動されると自身を将来の日時に起動されるよう自動的に設定し、それによって定期的にスケジュールされたタスクがあれば、その実行を保証できる。システムが深夜0時を過ぎてリブートされ起動した場合、通常5分後にその日に実行すべきタスクが実行される。これに対して cron は、設定された時間にシステムが起動済みでないとタスクを実行できない。

## 利点

UNIXには、ログ・ローテーション、不要なファイルの削除、検索エンジン向けにローカルファイルにインデックス付けするなど、定期的に行う必要のある処理が多数存在する。[cron](../Page/Crontab.md "wikilink") を使って、それらのタスクを深夜に行ったり、負荷の低い時間帯に行ったりする。しかし、スケジュールされた時間にシステムがOFFになっていると、そのタスクは実行されないことになる。

これに対して、anacron を使うと、システムが動作している間に、なるべくスケジュールされた間隔に近くなるようにタスクを実行することが保証される。

## 欠点

anacron のタスクは[システムアドミニストレータ](https://ja.wikipedia.org/wiki/システムアドミニストレータ "wikilink")だけが設定できる。それに対して cron は一般ユーザーでもタスクをスケジュールすることが可能である。必要なら、[at](https://ja.wikipedia.org/wiki/at_\(UNIX\) "wikilink") コマンドを使って一般ユーザーがタスクをスケジュールすることもできる。

anacron は、タスクの実行頻度を1日1回より多くできない。それに対して cron は毎分でもタスクを反復実行できる（ただし、システムがダウンしている間は実行されない）。しかし、1日の間に何度も実行すべきタスクをシステムが動作していなかった間のぶんだけ後で反復しなければならないという状況はあまり想定できないので、この制限はそれほど重大ではない。

## 外部リンク

  - [Anacron on SourceForge](http://anacron.sourceforge.net/)
  - [anacron(8)](http://linux.die.net/man/8/anacron) 英語版 Linux manページ
  - [anacron](http://www.jp.redhat.com/manual/Doc80/RH-DOCS/rhl-cg-ja-8.0/s1-autotasks-anacron.html) – Red Hat Linux 8.0:オフィシャルカスタマイズガイド

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")