> この記事は[Time Machine \(\)](https://ja.wikipedia.org/wiki/Time_Machine_\(\))から翻訳されています。


**Time Machine**（タイムマシン）とは、[アップルが開発する](../Page/アップル_\(企業\).md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用の[バックアップ](https://ja.wikipedia.org/wiki/バックアップ "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。[Mac OS X v10.5以降に搭載されている](https://ja.wikipedia.org/wiki/Mac_OS_X_v10.5 "wikilink")。

## 概要

macOSに内蔵されているバックアップ機能であり、ユーザーのファイル・フォルダに加えてシステムファイル・[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")・環境設定など、コンピュータ全体を自動的にバックアップする。バックアップのための専用のボリューム（外付け[ハードディスクや](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")[NASなど](../Page/ネットワークアタッチトストレージ.md "wikilink")）が必要になるが、バックアップ用に使用していない分はTime Machine以外に使用可能である\[1\]\[2\]。

バックアップは、1時間ごとの[増分バックアップ](https://ja.wikipedia.org/wiki/増分バックアップ "wikilink")で行われるが、[ハードリンク](https://ja.wikipedia.org/wiki/ハードリンク "wikilink")によりファイル構成上は毎回フルバックアップのような見かけになっており、バックアップの高速化とディスク容量の低消費などを実現している\[3\]。バックアップデータは24時間〜1ヶ月までは1日単位、1ヶ月以降は週単位と自動的に間引かれ、さらに、バックアップに使用する容量が不足する場合には、自動で古いバックアップから順にデータが削除され、必要な容量が確保される。個別にバックアップ対象外のファイルを指定することもできる\[4\]。

リストア作業は[Finder](https://ja.wikipedia.org/wiki/Finder "wikilink")や[Spotlight](https://ja.wikipedia.org/wiki/Spotlight "wikilink")から操作できるほか、特徴的な[GUIを利用することもできる](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")\[5\]。コンピュータ全体をバックアップしているため、Time Machineからシステムを復元することや、新規インストール後に移行アシスタントを使ってバックアップ元の環境を引き継ぐことも可能である\[6\]。

[Mac OS X Lion以降で実装された](https://ja.wikipedia.org/wiki/Mac_OS_X_Lion "wikilink")[FileVault](../Page/FileVault.md "wikilink")2により、Time Machineのバックアップ先ドライブを[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")することもできるようになった。

なお、アップルはTime Machineのバックアップ先として、[無線LAN](../Page/無線LAN.md "wikilink")[ルーター](../Page/ルーター.md "wikilink")に大容量[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")を組み合わせた[Time Capsuleを発売している](https://ja.wikipedia.org/wiki/Time_Capsule "wikilink")。

## 類似するバックアップツール

  - Windows 8 ファイル履歴 (File History)
    ユーザーのファイル・フォルダを一定の時間間隔でバックアップする[Windows 8の新機能](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")\[7\]。登場前よりTime Machineに類似するバックアップ機能と言われていた\[8\]。
  - FlyBack
    [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")向けのバックアップソフト。[UNIX](../Page/UNIX.md "wikilink")コマンド[rsync](https://ja.wikipedia.org/wiki/rsync "wikilink")を利用してバックアップを作成しており、Time Machine同様にファイルシステム全体の自動バックアップを実現している\[9\]。
  - Dumpfs / pdumpfs
    pdumpfsは毎日のバックアップを[スナップショットで保存するバックアップシステム](../Page/スナップショット_\(ファイルシステム\).md "wikilink")。[Plan 9のために開発されたDumpfsから派生している](../Page/Plan_9_from_Bell_Labs.md "wikilink")。pdumpfsにはWindows版も開発されている\[10\]。

## 脚注

## 関連項目

  - [macOS Server](https://ja.wikipedia.org/wiki/macOS_Server "wikilink")
  - [Backup](https://ja.wikipedia.org/wiki/Backup_\(ソフトウェア\) "wikilink") - アップルがTime Machine以前に提供していたバックアップソフト。
  - [AirMac](https://ja.wikipedia.org/wiki/AirMac "wikilink")
  - [Apple Filing Protocol](https://ja.wikipedia.org/wiki/Apple_Filing_Protocol "wikilink")

## 外部リンク

  - [Time Machineサポート](http://www.apple.com/jp/support/timemachine/) - アップル
      - [Mac ハンドブック：Time Machine](http://support.apple.com/kb/HT1427?viewlocale=ja_JP)
  - [Leopard標準バックアップツール「Time Machine」を使いこなす](https://news.mynavi.jp/articles/2009/01/29/timemachine/) - マイナビニュース
  - [もっと知りたい！ Snow Leopard - 第8回 Macのバックアップ、Time Machineで始めよう！](http://ascii.jp/elem/000/000/457/457960/) - ASCII.jp

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:2007年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2007年のソフトウェア "wikilink")

1.  [Laopard標準バックアップツール「Time Machine」を使いこなす](https://news.mynavi.jp/articles/2009/01/29/timemachine/) - [マイナビニュース](https://ja.wikipedia.org/wiki/マイナビニュース "wikilink")（2009年1月29日）
2.  [もっと知りたい！ Snow Leopard - 第8回 Macのバックアップ、Time Machineで始めよう！](http://ascii.jp/elem/000/000/457/457960/) - [ASCII.jp](https://ja.wikipedia.org/wiki/ASCII.jp "wikilink")（[アスキー・メディアワークス](https://ja.wikipedia.org/wiki/アスキー・メディアワークス "wikilink")）
3.  [あのTime MachineをLinuxで? - バックアップツール「FlyBack」が登場](https://news.mynavi.jp/news/2007/11/12/003/) - マイナビニュース（2007年11月12日）
4.
5.
6.
7.  [Windows 8レボリューション：第9回 ファイルを自動バックアップするファイル履歴機能](http://www.atmarkit.co.jp/ait/articles/1211/22/news092.html) - @IT（[ITmedia](https://ja.wikipedia.org/wiki/ITmedia "wikilink")）
8.  [せかにゅ：Windows 8にMac OS X「Time Machine」似の機能搭載か](http://www.itmedia.co.jp/news/articles/1103/31/news059.html) - ITmedia ニュース（ITmedia）
9.
10. [pdumpfs: Plan9もどきのバックアップシステム](http://0xcc.net/pdumpfs/) - 0xcc.net