> この記事は[Haiku \(\)](https://ja.wikipedia.org/wiki/Haiku_\(\))から翻訳されています。


**Haiku**（ハイク）は、[オープンソース](../Page/オープンソース.md "wikilink")で開発されているデスクトップ向け[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")。Haiku R1のリリースに向けて[BeOS](../Page/BeOS.md "wikilink")を再現することを目指しており、以前は**OpenBeOS**と呼ばれていた。Haiku R1/Alpha 1では[x86と](https://ja.wikipedia.org/wiki/IA-32 "wikilink")[PowerPC](../Page/PowerPC.md "wikilink")をサポートしていたが、Haiku R1/Alpha 2以降のバージョンでは[x86のみをサポートしている](https://ja.wikipedia.org/wiki/IA-32 "wikilink")。

なおHaikuという名称は日本の**[俳句](https://ja.wikipedia.org/wiki/俳句 "wikilink")**に起因する（詳しくは英語版の[NetPositiveを参照のこと](https://ja.wikipedia.org/wiki/:en:NetPositive "wikilink")）

## Haikuの目的

Haikuは下記の特性を持ったデスクトップOSを目指している。

  - 面倒な管理を必要としない
  - 使いやすい
  - フリー＆オープン
  - 古いハードウエアでも高速
  - 複雑な用途にも適用できるぐらいの高性能
  - 使っていて楽しい

## システムの特徴

  - POSIXと高い互換性
  - オブジェクト指向APIを適用 (BeOS APIと互換性あり)
  - 高度なマルチスレッド・マルチタスク化による高性能パフォーマンス
  - データベースライクな OpenBFS ファイルシステム\*\*による高速検索
  - BeOSとのソース＆バイナリ互換性（Haiku R1 32 bitのみ）

## システム要件

  - プロセッサ：Pentium Ⅱ 400MHz相当、AMD AthlonのCPU以上（最大64コア）
  - 物理メモリ：最小で256MB以上、Haikuをソースからコンパイルする場合は1GB以上を推奨
  - モニタ： 800x600
  - HDD 空き容量：3GB以上

## 主なマイルストーン

  - 2001年 8月 OpenBeOSプロジェクト発足
  - 2004年 6月 第1回「WalterCon 2004」開催、新プロジェクト名「Haiku」が発表される
  - 2004年 10月 CannaIM for BeOSがHaikuに寄付される
  - 2005年 7月 日本語フォント[小夏を標準フォントとして採用](https://ja.wikipedia.org/wiki/小夏_\(書体\) "wikilink")
  - 2005年 8月 「WalterCon 2005」開催
  - 2006年 10月 「WalterCon 2006」開催
  - 2007年 2月[ロサンゼルス](../Page/ロサンゼルス.md "wikilink")にて「SCaLE 5x」(Southern California Linux Expo)オープンソース展に出展（[写真](http://haiku-os.org/index.php?q=gallery&g2_itemId=1249)、[ポッドキャスト](http://www.clickcaster.com/resource/audio/scale-5-linux-expo-haiku-os-interview.mp3)）
  - 2007年 2月 Google本社で「Haiku Tech Talk」を通してHaikuを披露（[ビデオ](http://video.google.com/videoplay?docid=236331448076587879)、[写真](http://haiku-os.org/index.php?q=gallery&g2_itemId=1288)、[プレゼンスライド](http://haiku-os.org/files/downloads/2007-02-13_haiku-tech-talk.pdf)）
  - 2007年 3月 Google社が主権する[Google Summer of CodeにMentor](https://ja.wikipedia.org/wiki/Google_Summer_of_Code "wikilink") Organizationとして選ばれ、[8人の学生をスポンサー](http://code.google.com/soc/haiku/about.html)
  - 2007年11月 [関西オープンソース2007](http://k-of.jp/2007/exhibition.html)に出展 ー 英語でのレポート[その１](http://haiku-os.org/news/2007-11-13/haiku_gets_featured_speaker_spot_booth_at_scale_6x_expo)、「Haikuってなに？」セミナのスライド（[PDF](http://myhaiku.org/wp-content/uploads/2007/11/kof-07_haiku-slides.pdf) 527KB）
  - 2008年 2月 ロサンゼルスにて「SCaLE 6x」オープンソース展に出展（[写真](http://picasaweb.google.com/haiku.inc/SCaLE6x)、[英語レポート](http://www.haiku-os.org/blog/koki/2008-02-11/haiku_at_scale_6x_overall_impressions)、[thebadapples.infoによるBruno G. Albuquerqueインタービュー](http://www.thebadapples.info/audiophile/209.mp3)）
  - 2009年9月14日 初公式リリース Haiku R1/Alpha 1 が公開される [公式サイトでの発表](http://www.haiku-os.org/news/2009-09-13_haiku_project_announces_availability_haiku_r1alpha_1)、[sourceforge.jp](http://sourceforge.jp/magazine/09/09/14/0439229)、[BeOS互換OS「Haiku」の初となる公式開発版「Haiku R1/Alpha」を試す](http://sourceforge.jp/magazine/09/09/26/0812219/2)
  - 2010年5月09日 公式リリース Haiku R1/Alpha 2 が公開される [公式サイトでの発表](http://www.haiku-os.org/news/2010-05-10_haiku_project_announces_availability_haiku_r1alpha_2)、Haiku Japan による [日本語発表](http://www.haiku-jp.org/%E3%83%8B%E3%83%A5%E3%83%BC%E3%82%B9/2010-05-09_haiku-r1alpha-2-%E3%81%8C%E5%85%AC%E9%96%8B) と [日本語リリースノート](http://www.haiku-jp.org/get-haiku/release-notes)
  - 2011年6月18日 公式リリース Haiku R1/Alpha 3 が公開される [公式サイトでの発表](http://haiku-os.org/news/2011-06-18_haiku_release_1_alpha_3)
  - 2012年11月12日 公式リリース Haiku R1/Alpha 4 が公開される [公式サイトでの発表](http://haiku-os.org/news/2012-11-12_haiku_release_1_alpha_4)
  - 2012年11月14日 公式リリース Haiku R1/Alpha 4.1 が公開される [公式サイトでの発表](http://haiku-os.org/news/2012-11-14_haiku_release_1_alpha_41)
  - 2018年9月28日 公式リリース Haiku R1/Beta 1 が公開される [公式サイトでの発表](http://www.haiku-os.org/news/2018_09_28_haiku_r1_beta1)

## 開発状況

2020年1月現在、Haikuは開発途中であり、Linux より移植されたアプリにて日本語表示はできるが、エンドユーザが日本語入力できる完成度には至っていない（標準アプリでは日本語入力は可能）。英語を使う限りは完成度が上がっている。

  - [Haiku CIA](http://cia.vc/stats/project/OpenBeOS) − ソースツリーへのコミットをリアルタイムで見ることが可能。

## コミュニティ

  - [Haiku IRCチャンネル（英語）](irc://irc.freenode.net:6667/haiku) (\#haiku@irc.freenode.net)
  - [日本語 IRCチャンネル（試験運用）](irc://irc.freenode.net:6667/haiku-jp) (\#haiku-jp@irc.freenode.net)

## 開発者向け資料

  - [Programming the Be Operating System](http://www.jpbe.net/program-be/work.php) ([原文の英語版](http://haiku-os.org/downloads.php?mode=download&id=8&mirror=1)) − JPBE.netによる日本語版 (作成中)
  - [Coding Guidelines](http://opentracker.sourceforge.net/guidelines.html) − Haikuに適用されるOpenTrackerのコーディングガイドライン
  - [Practical File System Design with the Be File System](http://www.nobius.org/~dbg/practical-file-system-design.pdf) (PDF) − Dominic GiampaoloによるBFSファイルシステムに関する書籍
  - [The BeBook](http://www.haiku-os.org/develop.php?mode=doc&id=12)（英語版）
  - [Art of BeOS Programming](http://www.stprec.co.jp/project/BeOSBook/)「Art of BeOS Programming BeOSで楽しむプログラミングの世界」(古賀信哉著)の Web 公開版

## 書籍

  - 「Be デベロッパーズガイド Vol.1 The official documentation for the BeOS」オライリー・ジャパン ISBN 4-900900-71-0
  - 「Be デベロッパーズガイド Vol.2 The official documentation for the BeOS」オライリー・ジャパン ISBN 4-900900-87-7
  - 「BeOS:ファイルシステム 実践ファイルシステム構築」オーム社 ISBN 4-274078-87-6
  - 「BeOS:UNIXアプリケーションの組込み」オーム社 ISBN 4-274078-82-5
  - 「BeOSバイブル〈Volume1〉」 ソフトバンクパブリッシング ISBN 4-797311-62-2
  - 「BeOSバイブル〈Volume2〉」 ソフトバンクパブリッシング ISBN 4-797311-63-0
  - 「BeOSプログラミング入門」プレンティスホール出版 ISBN 4-894710-35-8

## 関連項目

  - [BeOS](../Page/BeOS.md "wikilink")
  - [NewOS](https://ja.wikipedia.org/wiki/NewOS "wikilink") カーネルに採用されている。
  - [WebPositive](https://ja.wikipedia.org/wiki/WebPositive "wikilink") デフォルトウェブブラウザ。

## 外部リンク

  -
  - [Haiku へようこそ！](https://haiku-os.org/docs/welcome/welcome_jp.html)

  - [最新バージョンのダウンロード](http://haiku-os.org/get-haiku)

  - [テスト・開発用ナイトリービルドのダウンロード](http://haiku-files.org)

  - [Haiku画面スライドショー](http://www.haiku-os.org/slideshows/haiku-tour)

  - [Haiku Movies](http://haiku-os.org/about/movies)

  - [HaikuソースのSVNリポジトリ](http://svn.haiku-os.org)

  - [Haiku公式ロゴの画像データファイル](http://svn.haiku-os.org/haiku/haiku/trunk/data/artwork/)

  - [JPBE.net: 日本のユーザーコミュニティサイト](http://www.jpbe.net/) - 閉鎖

[Category:Haiku_(オペレーティングシステム)](https://ja.wikipedia.org/wiki/Category:Haiku_\(オペレーティングシステム\) "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:2009年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2009年のソフトウェア "wikilink") [Category:オブジェクト指向OS](https://ja.wikipedia.org/wiki/Category:オブジェクト指向OS "wikilink")