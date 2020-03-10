> この記事は[At \(UNIX\)](https://ja.wikipedia.org/wiki/At_\(UNIX\))から翻訳されています。


**`at`**（アット）は、[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のコマンドであり、任意のコマンドを任意の指定した時間に1回実行するようスケジュールする。

より正確に言えば、一連のコマンド行を[標準入力](https://ja.wikipedia.org/wiki/標準入力 "wikilink")から読み込み、後日実行される "at-job" としてそれらをまとめる。at-jobは現在の環境を継承するので、[ワーキングディレクトリや](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")[環境変数](https://ja.wikipedia.org/wiki/環境変数 "wikilink")をスケジュール設定時と同じにして実行される。

[`cron`](../Page/Crontab.md "wikilink")は、これとは異なり、繰り返し実行する場合に使われる（一時間おきとか、毎週火曜日とか、毎年1月1日など）。。

**`at`**はスケジュールされた一連のジョブを実行したときにユーザーに[電子メール](../Page/電子メール.md "wikilink")を送信することができ、ジョブキューを複数使ったり、標準入力以外のファイルからジョブのリストを読み込んだりできる。例えば、[C言語](../Page/C言語.md "wikilink")のプログラムを午前11:45に[コンパイルするコマンドを実行し](../Page/コンパイラ.md "wikilink")、結果（標準出力と標準エラー出力）をユーザーIDに対してメールで通知するには、以下のようにする。

`echo "cc -o foo foo.c" | at 1145`

**`at`**がスケジュールしたジョブの実行のため、**`atd`**という[デーモンが定期的にジョブリストをチェックし](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")、実行すべき時刻がきたジョブを起動する。

`at`の代わりに**`batch`**コマンドを使うと、[ロードアベレージがある値より低い場合のみ](https://ja.wikipedia.org/wiki/ワークロード "wikilink")、スケジュールされたジョブを実行するようになる（高負荷の場合は実行しない）。

[Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") / [2000](../Page/Microsoft_Windows_2000.md "wikilink") / [XPには](../Page/Microsoft_Windows_XP.md "wikilink")[`cron`](../Page/Crontab.md "wikilink")に類似した[`at`](https://ja.wikipedia.org/wiki/:en:at_\(Windows\) "wikilink")コマンドがあるが、[タスクスケジューラ](https://ja.wikipedia.org/wiki/タスクスケジューラ "wikilink")の方が有名である。

## 関連項目

  - [cron](../Page/Crontab.md "wikilink")
  - [launchd](https://ja.wikipedia.org/wiki/launchd "wikilink") - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")におけるat

## 外部リンク

  -
  -
  -
  - [at(1)](https://nixdoc.net/man-pages/HP-UX/man1/at.1.html) man page（HP-UX リファレンス）

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")