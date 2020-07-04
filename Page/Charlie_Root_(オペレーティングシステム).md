> この記事は[Charlie Root \(オペレーティングシステム\)](https://ja.wikipedia.org/wiki/Charlie_Root_\(オペレーティングシステム\))から翻訳されています。


**Charlie Root**は、[BSD系オペレーティングシステムの](../Page/BSDの子孫.md "wikilink")[管理者](../Page/管理者.md "wikilink")[ユーザ](https://ja.wikipedia.org/wiki/ユーザ "wikilink")(→[スーパーユーザー](../Page/スーパーユーザー.md "wikilink"))の初期設定値である。

## 基本仕様

[UNIX](../Page/UNIX.md "wikilink")系[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の管理者権限を持つユーザは**root**である。これは、管理者ユーザが**root**(最上層)ディレクトリをユーザディレクトリとするためである。 [UNIX](../Page/UNIX.md "wikilink")系のログイン情報を記録するpasswdファイルの仕様として、ユーザID、パスワードの他に**GECOS Field**が存在する。本フィールド\[1\]は、歴史的にGECOSシステムを制御するための制御情報等を含むものであったが、以後、フルネームや電話番号等、人間が読む(fingerで取得する)情報を記入するために使われている。→[GECOS](https://ja.wikipedia.org/wiki/GECOS#こぼれ話 "wikilink")。GECOS Fieldの仕様として、"&"(アンパサンド)はユーザIDを反映する。

## 実装

[BSD](../Page/BSD.md "wikilink")系オペレーティングシステムの管理者ユーザは、初期状態でGECOS Fieldは**Charlie &**であるため、'&'(アンパサンド)が管理者IDである"root"に置換され、自動的に管理者ユーザは**Charlie Root**となる。 [FreeBSD](../Page/FreeBSD.md "wikilink")および[NetBSD](../Page/NetBSD.md "wikilink")の最古(各バージョン1.0)のコードは取得可能であり、[CVS](../Page/Concurrent_Versions_System.md "wikilink") repositoryから内容を確認することができる。\[2\]\[3\] \[4\] FreeBSD, NetBSDともに[386BSD](../Page/386BSD.md "wikilink")patchkitからの派生物(OpenBSDはNetBSDからの派生)であるため、同一のファイルがインポートされている。(以下に抜粋)

``` fortran
root::0:10::0:0:Charlie &:/root:/bin/csh

dmr:*:10:31::0:0:Dennis Ritchie:/usr/guest/dmr:
ken:*:11:31::0:0:& Thompson:/usr/guest/ken:
bill::12:10::0:0:& Jolitz:/usr/bill:/bin/csh
lynne::14:10::0:0:& Jolitz:/usr/lynne:/bin/csh
```

管理者ユーザのGECOS Fieldは**"Charlie &"**であり、各UIDのGECOS Fieldに[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")、[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")、[ビル・ジョリッツ](https://ja.wikipedia.org/wiki/ウィリアム・ジョリッツ "wikilink")、[リン・ジョリッツ](../Page/リン・ジョリッツ.md "wikilink")のユーザ名が、全て「名」・「姓」の形式で記入されていることが確認できる。つまり管理者ユーザの**Root**は[苗字](https://ja.wikipedia.org/wiki/苗字 "wikilink")として扱われていることがわかる。

## 疑問

### いつから管理者は"Charlie Root" なのか

386BSD Patchkit以前ということになるが、4.2BSDも同一である。\[5\]

### "Charlie Root" とは誰？

[米国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[メジャーリーグ](https://ja.wikipedia.org/wiki/メジャーリーグ "wikilink")の野球[投手](../Page/投手.md "wikilink")に[Charlie Rootがいる](https://ja.wikipedia.org/wiki/チャーリー・ルート "wikilink")。選手登録された[1926年](../Page/1926年.md "wikilink") から[1941年](https://ja.wikipedia.org/wiki/1941年 "wikilink")の間に勝利数201勝を上げており、優秀な成績を残している。しかし、BSDが開発されている1990年代から見て約50年前に引退した選手である上、彼が在籍していたのは[シカゴ・カブス](../Page/シカゴ・カブス.md "wikilink")であり、所在地は中西部[イリノイ州](../Page/イリノイ州.md "wikilink")のチームである。一方、[BSD](../Page/BSD.md "wikilink")が開発されている[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の所在地は、西部[カリフォルニア州](../Page/カリフォルニア州.md "wikilink")であり、[ビル・ジョリッツがよほどのカブス狂いであったとは考えにくい](https://ja.wikipedia.org/wiki/ウィリアム・ジョリッツ "wikilink")。 FreeBSDの/usr/bin/calendar/calendars/calendar.freebsd には**Charlie Root氏**の誕生日が記入されている\[6\](1993年6月19日)が、これはFreeBSDの名称が提案された日\[7\]であり、calendar.freebsd rev=1.36\[8\]ではFreeBSDプロジェクト開始日として登録されたものの名称を、rev=1.39で変更したものであるため、人物としてのCharlie Rootと直接の関係はない。

### なんで姓なの？

GECOS Fieldに**&**が記入された時点で、そこには姓・名を入れるルールがあったために**Charlie**が追加されたもの思われるが、姓ではなく名でも良かったはずである。もっとも、前述の[Charlie Root氏をはじめ](https://ja.wikipedia.org/wiki/:en:Charlie_Root "wikilink")、[Rootを姓に持つ人は存在するが](https://ja.wikipedia.org/wiki/:en:Root_\(surname\) "wikilink")、名に持つ人は少ないためかもしれない。 米国国勢調査の結果(1990年度)では、\[9\]、**Root**姓は1834位(参考:1位はSmith姓)であるが、**Root**を名とする人はいない。

[BSD](../Page/BSD.md "wikilink")系オペレーティングシステムでは、一般ユーザが/bin/[sh](https://ja.wikipedia.org/wiki/sh "wikilink")を使う一方で、管理者ユーザは/bin/[csh](https://ja.wikipedia.org/wiki/csh "wikilink")を使うよう初期設定されている。「cshを利用する人たち」という意味合いで、**c**shの1文字目[C](https://ja.wikipedia.org/wiki/C "wikilink")の[フォネティックコード](https://ja.wikipedia.org/wiki/フォネティックコード "wikilink")である**Charlie**を割り当てたという可能性がある。そこに冗談をからめて「Root一族」という扱いにしたものかもしれない。

## まとめ

なぜ[BSD](../Page/BSD.md "wikilink")系OSの管理者IDが**Charlie Root**であるのかは、[BSD](../Page/BSD.md "wikilink")の歴史上最大の謎の一つであり、未解決の問題となっている。調査の結果、[野球選手Charlie Root説](https://ja.wikipedia.org/wiki/:en:Charlie_Root "wikilink")、[フォネティックコード](https://ja.wikipedia.org/wiki/フォネティックコード "wikilink")説の2つが有力であると考えられるが、いずれも決定的な証拠に欠けるため、正確な意味を把握するためには、今後の関係者の証言を待つ必要がある。

FreeBSD ProjectのSecurity Teamメンバーで、かつCommercial Gallery Editorである**Remko Lodder**のコメント\[10\]によると、「知らないよ。Kirk([マーシャル・カーク・マキュージック](../Page/マーシャル・カーク・マキュージック.md "wikilink"))が知っているんじゃない？:-)」という回答であった。

## 脚注

<div class="references-small">

<references/>

</div>

## 関連項目

  - [tcshのt](https://ja.wikipedia.org/wiki/tcshのt "wikilink")
  - [South Ryukyu Islands時間](https://ja.wikipedia.org/wiki/日本標準時#South_Ryukyu_Islands時間 "wikilink")

[Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:コンピュータの文化](https://ja.wikipedia.org/wiki/Category:コンピュータの文化 "wikilink")

1.  [Linux manpage(passwd): **GCOS**と呼ばれることもあるが、これはGE社のシステム部門がHoneywell社に売却された際に変更されたものである](http://linuxjm.osdn.jp/html/LDP_man-pages/man5/passwd.5.html)
2.  [FreeBSD1.0の/etc/master.passwd](http://www.jp.freebsd.org/cgi/cvsweb.cgi/~checkout~/src/etc/master.passwd?rev=1.1&content-type=text/plain)
3.  [NetBSD1.0の/etc/master.passwd](http://cvsweb2.jp.netbsd.org/cvsweb.cgi/~checkout~/src/etc/master.passwd?rev=1.1&content-type=text/plain&cvsroot=netbsd&only_with_tag=MAIN)
4.  [OpenBSDの初期/etc/master.passwd](http://www.openbsd.org/cgi-bin/cvsweb/~checkout~/src/etc/master.passwd?rev=1.1)
5.
6.  [FreeBSD calendar.freebsd rev=1.39](http://www.freebsd.org/cgi/cvsweb.cgi/~checkout~/src/usr.bin/calendar/calendars/calendar.freebsd?rev=1.39;content-type=text%2Fplain)
7.  [FreeBSDの名称の提案](http://www.freebsd.org/news/1993/freebsd-coined.html)
8.  [FreeBSD calendar.freebsd rev=1.36](http://www.freebsd.org/cgi/cvsweb.cgi/~checkout~/src/usr.bin/calendar/calendars/calendar.freebsd?rev=1.36;content-type=text%2Fplain)
9.  [米国名前ランキング検索](http://www.census.gov/genealogy/www/namesearch.html)
10. [FreeBSD-Advocacy メーリングリスト](http://lists.freebsd.org/pipermail/freebsd-advocacy/2007-June/003254.html)