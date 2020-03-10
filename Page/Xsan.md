> この記事は[Xsan](https://ja.wikipedia.org/wiki/Xsan)から翻訳されています。


**Xsan**（エックスサン）は、[アップルが開発](../Page/アップル_\(企業\).md "wikilink")・発売する[SAN用共有](../Page/ストレージエリアネットワーク.md "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。

## 概要

Xsanは、[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink")上にある[ストレージを複数のサーバ](../Page/補助記憶装置.md "wikilink")、クライアントから直接に読み書き可能とすることで、ファイルアクセスの高速化を図ったファイルシステムである。 1台以上のXsanメタデータコントローラ、1台以上のストレージ、1台以上のXsan クライアントと、それらを接続するストレージアクセス用のファイバーチャネルネットワークおよび2系統イーサネットワークで構成される。

Xsanは、[クアンタムの](../Page/クアンタム_\(企業\).md "wikilink")[StorNext File Systemをベースに開発されている](https://ja.wikipedia.org/wiki/:en:StorNext_File_System "wikilink")。\[1\] このため、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[UNIX](../Page/UNIX.md "wikilink")、[Linux](../Page/Linux.md "wikilink")環境のStorNextとの相互接続も可能となっている。\[2\]

主な用途としては、大規模な計算クラスターや[Final Cut Proを用いた映像プロジェクトなどを想定している他](../Page/Final_Cut_Pro.md "wikilink")、[Time Machine Serverや](../Page/Time_Machine_\(ソフトウェア\).md "wikilink")[カレンダーServer等](https://ja.wikipedia.org/wiki/iCal "wikilink")、[macOS Serverの様々なサービスでの利用も想定されている](https://ja.wikipedia.org/wiki/macOS_Server "wikilink")。

## バージョンごとの変遷

### Ver.1系列

  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")1月 - Xsan 1.0:16[TBのストレージボリュームをサポート](../Page/テラバイト.md "wikilink")
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")6月 - Xsan 1.1：ストレージボリュームのサポートを最大2[PB](https://ja.wikipedia.org/wiki/ペタバイト "wikilink") (2048TB) に拡張
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")11月 - Xsan 1.2：[バグ](../Page/バグ.md "wikilink")修正、全体的な信頼性の改善
  - [2006年](../Page/2006年.md "wikilink")4月 - Xsan 1.3：バグ修正、2TBを超えるLUNのサポート、全体的な信頼性の改善
  - [2006年](../Page/2006年.md "wikilink")8月 - Xsan 1.4：[Universal Binary化](https://ja.wikipedia.org/wiki/Universal_Binary "wikilink")、セキュリティアップデート、[ACLのサポート](../Page/アクセス制御リスト.md "wikilink")、[フェイルオーバー](https://ja.wikipedia.org/wiki/フェイルオーバー "wikilink")やクオータ等の機能改善
  - [2006年](../Page/2006年.md "wikilink")12月 - Xsan 1.4.1：バグ修正、フェイルオーバーや信頼性等の機能改善
  - [2007年](../Page/2007年.md "wikilink")10月 - Xsan 1.4.2：Mac OS X v10.5 Leoprad対応、バグ修正、フェイルオーバーや互換性・信頼性等の機能改善\[3\]

### Ver.2系列

  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")2月 - Xsan 2発表。[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")の改良、[Spotlight](https://ja.wikipedia.org/wiki/Spotlight "wikilink")対応、MultiSAN対応、動作保証ストレージにPromise VTrak E-Class RAIDを公式認定\[4\]\[5\]。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")6月 - Xsan 2.1：Xsan Adminのバグ修正、フェイルオーバーや互換性・信頼性等の機能改善\[6\]
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")10月 - Xsan 2.1.1：ファイルシステムの信頼性の向上、Xsan Adminの信頼性向上、ファイルシステムのパフォーマンスの向上等、機能改善\[7\]
  - [2009年](../Page/2009年.md "wikilink")9月 - Xsan 2.2：Mac OS XおよびMac OS X Server v10.5.8以降v10.6 Snow Leopard対応、[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")化、[拡張属性](https://ja.wikipedia.org/wiki/拡張ファイル属性 "wikilink")(extended attributes)対応\[8\]、信頼性の向上、セキュリティアップデート\[9\]など\[10\]。このバージョンからIntel Macのみの対応となった。
  - [2009年](../Page/2009年.md "wikilink")12月 - Xsan 2.2.1：ファイルシステムの信頼性の向上、cvfsckの向上など\[11\]
  - [2011年](../Page/2011年.md "wikilink")7月 - Xsan 2.3：OS X Lion/Lion Serverに標準添付(実質無償化)。システム環境設定にXsanクライアント向けペインが含まれるようになった。

### Ver.3系列

  - [2012年](../Page/2012年.md "wikilink")7月 - Xsan 3：OS X Mountain Lion/Mountain Lion Serverに標準添付
  - [2013年](../Page/2013年.md "wikilink")10月 - Xsan 3.1：OS X Mavericks/ Mavericks Serverに標準添付。

### Ver.4系列

  - [2014年](../Page/2014年.md "wikilink")10月 - Xsan 4：OS X Yosemite/Yosemite Server 4.0に標準添付
  - [2015年](../Page/2015年.md "wikilink")9月 - Xsan 4.1：[OS X El Capitan](https://ja.wikipedia.org/wiki/OS_X_El_Capitan "wikilink")/Server 5.0に標準添付

### Ver.5系列

  - [2016年](../Page/2016年.md "wikilink")9月 - Xsan 5：[macOS Sierra](https://ja.wikipedia.org/wiki/macOS_Sierra "wikilink")/macOS Server 5.2に標準添付
  - [2017年](../Page/2017年.md "wikilink")9月 - Xsan 5.0.1：[macOS High Sierra](https://ja.wikipedia.org/wiki/macOS_High_Sierra "wikilink")/macOS Server 5.4に標準添付

## 脚注

### 出典

## 外部リンク

  - [Xsan](http://www.apple.com/jp/xsan/)
  - [Xsan](http://www.apple.com/xsan)
  - [Xsan ヘルプ](https://help.apple.com/serverapp/mac/5.0/#/apd6ec9abf60)
  - [Xsan ガイド](https://itunes.apple.com/jp/book/xsan-5-%E3%82%AC%E3%82%A4%E3%83%89/id1156563299?mt=11)
  - [Xsan サポート](https://support.apple.com/ja-jp/xsan)
  - [IMAGICA　湾岸スタジオ：湾岸スタジオと品川プロダクションセンター　30kmの距離をつないだXsan](https://web.archive.org/web/20110330053831/http://www.apple.com/jp/pro/profiles/imagica/)
  - [株式会社アイネックス：Final Cut Studioが開くポストプロダクションの領域](https://web.archive.org/web/20110309044416/https://www.apple.com/jp/pro/profiles/i-nex/)

[Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:MacOS_Server](https://ja.wikipedia.org/wiki/Category:MacOS_Server "wikilink")

1.
2.
3.  [Xsan 1.4.2 について](http://support.apple.com/kb/TA24560?viewlocale=ja_JP)
4.  [アップル - Server - ストレージ](http://www.apple.com/jp/server/storage/)
5.  [promise mac support](http://jp.promise.com/apple/index.asp)
6.  [Xsan 2.1 のアップデートについて](http://support.apple.com/kb/HT1282?viewlocale=ja_JP)
7.  [Xsan 2.1.1 のアップデートについて](http://support.apple.com/kb/HT3171?viewlocale=ja_JP)
8.  [Xsan 2.2：\[拡張属性を有効にする](http://support.apple.com/kb/HT3791?viewlocale=ja_JP)
9.  [Xsan 2.2 のセキュリティコンテンツについて](http://support.apple.com/kb/HT3797?viewlocale=ja_JP)
10. [Xsan 2.2 のアップデートについて](http://support.apple.com/kb/HT3172?viewlocale=ja_JP)
11. [Xsan 2.2.1 ファイルシステムアップデートについて](http://support.apple.com/kb/HT3927?viewlocale=ja_JP)