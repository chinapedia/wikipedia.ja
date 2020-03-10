> この記事は[AN HTTPD](https://ja.wikipedia.org/wiki/AN_HTTPD)から翻訳されています。


**AN HTTPD**とは、[1996年](../Page/1996年.md "wikilink")に中田昭雄が開発した、[Windowsで動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Webサーバ](../Page/Webサーバ.md "wikilink")[アプリケーションである](../Page/アプリケーションソフトウェア.md "wikilink")。[プロキシ](https://ja.wikipedia.org/wiki/プロキシ "wikilink")/[キャッシュサーバとしても動作可能である](https://ja.wikipedia.org/wiki/キャッシュ_\(コンピュータシステム\) "wikilink")。

1996年[7月13日](../Page/7月13日.md "wikilink")から[フリーウェア](../Page/フリーウェア.md "wikilink")として一般に配布されていたが、2015年2月頃に公式サイトが閉鎖された。

## 概要

公式にアナウンスされているWindowsの対応バージョンは、[Windows 95](https://ja.wikipedia.org/wiki/Windows_95 "wikilink")/[98](https://ja.wikipedia.org/wiki/Windows_98 "wikilink")/[Me](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")/[NT](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")/[2000](https://ja.wikipedia.org/wiki/Windows_2000 "wikilink")/[XPである](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")。[Windows Vistaやそれ以降の対応状況については正式に発表](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")・サポートされなかった。

ソフトウェア本体である[EXEファイルを実行すると](https://ja.wikipedia.org/wiki/EXEフォーマット "wikilink")、Webサーバーとして起動する。開発者が[日本人](https://ja.wikipedia.org/wiki/日本人 "wikilink")であるため、メニューや設定画面の表記が標準で[日本語](../Page/日本語.md "wikilink")である。各種設定作業を[GUI上で行える一方](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[CUIで設定を行うことはできなかった](../Page/キャラクタユーザインタフェース.md "wikilink")。

その他、基本的な機能は以下の通りであった。

  - [マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")（最大50スレッド）に対応している。
  - [Perl](../Page/Perl.md "wikilink")や[Ruby](../Page/Ruby.md "wikilink")、[PHPなどがインストールされていれば](../Page/PHP_\(プログラミング言語\).md "wikilink")、[CGIや](../Page/Common_Gateway_Interface.md "wikilink")[SSIも利用可能である](https://ja.wikipedia.org/wiki/Server_Side_Includes "wikilink")。

<!-- end list -->

  -
    （[UNIX](../Page/UNIX.md "wikilink")用に書かれた物は動かない場合もある\[1\]）

<!-- end list -->

  - [バーチャルホスト](https://ja.wikipedia.org/wiki/バーチャルホスト "wikilink")に対応している。
  - Windows NT/2000/XP では、[サービスに登録して動作させることができる](https://ja.wikipedia.org/wiki/Windowsサービス "wikilink")。

[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[4月2日](../Page/4月2日.md "wikilink")にバージョン1.42pの公開を行った時点で、今後対応予定の[バグ](https://ja.wikipedia.org/wiki/バグ "wikilink")や機能追加予定として170個以上の懸案が「対応中または対応予定」とされていたが\[2\]、それ以降のバージョンは公開されず、今後の開発やサポート状況についても表明されることはなかった。2015年2月頃に公式サイトが閉鎖された\[3\]。

ソフトウェアの開発には[Borland C++を使用していたほか](https://ja.wikipedia.org/wiki/C++_Builder "wikilink")、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")[圧縮に](../Page/データ圧縮.md "wikilink")[zlib](https://ja.wikipedia.org/wiki/zlib "wikilink")を使用していた\[4\]。

## 歴史

作者（中田昭雄）は勤務する会社\[5\]で、[HP-UX](../Page/HP-UX.md "wikilink")で[CERN](https://ja.wikipedia.org/wiki/CERN_httpd "wikilink")（W3C）を使用したWebサーバを構築していたが、社内の要望に合わせ、Windows 95で動作するWebサーバアプリケーションとして開発した\[6\]。[1996年](../Page/1996年.md "wikilink")[3月17日](../Page/3月17日.md "wikilink")に初版0.1alpha1が完成したが、一般には公開されなかった。

[1996年](../Page/1996年.md "wikilink")[7月13日](../Page/7月13日.md "wikilink")、0.2beta1が作者個人の製作物として公開され、以降はフリーウェアとして一般に公開される。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[9月20日](../Page/9月20日.md "wikilink")に正式版が公開され、メッセージウィンドウや設定ダイアログが日本語で表示できるようになった\[7\]。

[1999年](../Page/1999年.md "wikilink")[5月16日](../Page/5月16日.md "wikilink")に公開された1.16で、初めて[セキュリティホール](../Page/セキュリティホール.md "wikilink")が発覚、[5月20日](../Page/5月20日.md "wikilink")に対策版として1.16bが公開された。その後も次々とセキュリティホールが発見され\[8\]、バージョンアップや対策版による対応が行われた。

[2000年](../Page/2000年.md "wikilink")[3月4日](../Page/3月4日.md "wikilink")公開された1.33は、[3月7日](../Page/3月7日.md "wikilink")に「バグが多く、対応にしばらく時間が必要と思われる」と発表し\[9\]、公開が中止された。

[2002年](../Page/2002年.md "wikilink")、[オンラインソフトウェア大賞に入賞した](https://ja.wikipedia.org/wiki/フリーソフトウェア大賞 "wikilink")。

[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")4月、結果的に最終版となるバージョン1.42pが公開された\[10\]。

その後は更新されず、[2015年](../Page/2015年.md "wikilink")2月頃に公式サイトが閉鎖された\[11\]。

## 関連書籍

一般公開された1996年から、多数の関連書籍で紹介・解説された。

  - フリーソフトを使ってWindowsで自分のWebサーバを立てる ISBN 4-7973-2055-9
  - 自宅サーバ for Windows XP ISBN 4-89977-028-6
  - 家庭内ネットワークパーフェクトマニュアル ISBN 4-8443-1556-0
  - 自宅に置けるぞWebサーバ ISBN 4-8163-3012-7
  - 最新HTML\&CGI入門 ISBN 4-87193-679-1
  - Windows NT 武装化計画 ISBN 4-87966-893-1
  - パソコンとパソコンをつなぐ法 ISBN 4-534-03009-6
  - Windows XP で作る スマート自宅サーバー ISBN 4-774-12603-9

## 脚注・出典

## 外部リンク

  -
[Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")

1.
2.
3.   - "[403 Forbidden](https://ja.wikipedia.org/wiki/HTTP_403 "wikilink")"と表示される。
4.
5.  会社名などの詳細は公表されていない。
6.
7.  [窓の杜 - フリーのWWWサーバーソフト「AN HTTPD」v1.00正式版がリリース](http://www.forest.impress.co.jp/article/1998/09/21/anhttpd.html)
8.
9.
10.
11.