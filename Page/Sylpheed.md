> この記事は[Sylpheed](https://ja.wikipedia.org/wiki/Sylpheed)から翻訳されています。


**Sylpheed**（シルフィード）は、[Linux](../Page/Linux.md "wikilink")、[BSD](../Page/BSD.md "wikilink")などの[PC-UNIX](https://ja.wikipedia.org/wiki/PC-UNIX "wikilink")上、及び[Windows上で動く](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")\[1\]。開発者は[山本博之](https://ja.wikipedia.org/wiki/山本博之_\(プログラマ\) "wikilink") \[2\]\[3\]\[4\]\[5\]\[6\]。

## 概要

大学在学中に[Linux](../Page/Linux.md "wikilink")を使い始めた山本が、実用レベルで使える電子メールクライアントがなかったことを理由として大学4年生のときに開発をはじめた\[7\]。3ヶ月後の[2000年](../Page/2000年.md "wikilink")（平成12年）1月にバージョン0.1をリリース\[8\]。Sylpheedの機能に関しては[Becky\!などの既存の電子メールクライアントを参考に実装された](../Page/Becky!_Internet_Mail.md "wikilink")\[9\]。最初に入社した会社 (株式会社グッデイ) やその次の会社 (後述するSRA OSS) でも開発を全面的に支援していたと述べている\[10\]。

Sylpheedは[2000年](../Page/2000年.md "wikilink")（平成12年）より、長らくLinuxを中心とするPC-UNIX上で開発され、発展を遂げてきた。バージョン1.0未満から1.0.5までは、[GTK](https://ja.wikipedia.org/wiki/GTK "wikilink")1のライブラリを利用して開発されてきたが、1.9.0以降からはGtk2のライブラリを利用するようになり、現在デスクトップ環境として広く使われている[GNOME](../Page/GNOME.md "wikilink")との親和性、[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")によるフォント品質の向上などが計られている。ライセンスは[GNU GPLを採用している](https://ja.wikipedia.org/wiki/GNU_GPL "wikilink")\[11\]。

バージョン1.0.x時代にもGtk2のライブラリを使ったものがあった (sylpheed-gtk2) が、現在は、その成果がSylpheed本家に取り込まれたため、sylpheed-gtk2は開発を終了した。

Windows版については、バージョン1.0未満のバージョンでは別作者によるものがあったが\[12\]、バージョン2.1.3からは山本によるバージョンが提供されている。正式リリース版としては2.2.0以降となる\[13\]。

[2006年](../Page/2006年.md "wikilink")（平成18年）9月6日には、[SRA OSSがSylpheedの開発を全面的に支援することを発表](../Page/SRA.md "wikilink")\[14\]\[15\]\[16\]。SRA OSSは山本を雇用し、自由にSylpheedの開発ができる環境などを作った\[17\]\[18\]\[19\]。山本は同社でSylpheedのコアライブラリを独立させたLibSylphプロジェクトに携わることとなる\[20\]\[21\]\[22\]。

### 特徴

Sylpheedの特徴は、以下の通りである。

  - [3ペインの](https://ja.wikipedia.org/wiki/ペインド・ウィンドウ "wikilink")[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")\[23\]
  - 全面GUIの実装である
  - PC-UNIX上のGUIソフトウェアとしては、非常に軽い
  - 動作設定が細かく、さまざまなシチュエーションに対応できる
  - 1ファイル1メールの[MH形式を採用している](https://ja.wikipedia.org/wiki/:en:MH_Message_Handling_System "wikilink")\[24\]。このためメールデータに障害が発生しても対処しやすい
  - 外部フィルタとの連携が可能で、スパムなどの対処がしやすい
  - [国際化対応されており](../Page/国際化と地域化.md "wikilink")、各種言語によるメールの利用が可能である
  - バージョン3.5.1からは添付ファイルの自動暗号化機能プラグインがバンドルされるようになった。日本国内でよく利用される添付ファイルをZIPで暗号化して、別なメールでパスワードを知らせる機能がワンタッチで利用できる

### 名前の由来

風の妖精「[Sylph](https://ja.wikipedia.org/wiki/シルフ "wikilink")」(シルフ) が由来\[25\]。風のように軽快で、空気のように自然な動作を、という意味が込められている\[26\]。

「シルフィード」は本来「Sylphid」と綴るべきだが、作者の誤解により「Sylpheed」という名前が採用されてしまった。その後、誤解に気付いたが、既に多くのディストリビューションによって採用されてしまっており、取り返しがつかなくなったので、そのままになったという。

## バージョン履歴

  - [2000年](../Page/2000年.md "wikilink")（平成12年）[1月1日](../Page/1月1日.md "wikilink") - バージョン0.1.0 αがリリースされる
  - [2004年](../Page/2004年.md "wikilink")（平成16年）[12月24日](../Page/12月24日.md "wikilink") - バージョン1.0.0がリリースされる\[27\]
  - [2005年](../Page/2005年.md "wikilink")（平成17年）[7月29日](../Page/7月29日.md "wikilink") - バージョン2.0.0がリリースされる
  - [2006年](../Page/2006年.md "wikilink")（平成18年）[2月14日](../Page/2月14日.md "wikilink") - バージョン2.2.0がリリースされる\[28\]。このバージョンからMicrosoft Windows版が正式にリリースされた\[29\]。
  - [2006年](../Page/2006年.md "wikilink")（平成18年）[12月24日](../Page/12月24日.md "wikilink") - バージョン2.3.0がリリースされる
  - [2007年](../Page/2007年.md "wikilink")（平成19年）[4月20日](https://ja.wikipedia.org/wiki/4月20日 "wikilink") - バージョン2.4.0がリリースされる
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")（平成20年）[6月17日](../Page/6月17日.md "wikilink") - バージョン2.5.0がリリースされる
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")（平成20年）[12月19日](https://ja.wikipedia.org/wiki/12月19日 "wikilink") - バージョン2.6.0がリリースされる
  - [2009年](../Page/2009年.md "wikilink")（平成21年）[7月21日](../Page/7月21日.md "wikilink") - バージョン2.7.0がリリースされる
  - [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")（平成22年）[2月24日](https://ja.wikipedia.org/wiki/2月24日 "wikilink") - バージョン3.0.0がリリースされる
  - [2011年](../Page/2011年.md "wikilink")（平成23年）[1月31日](../Page/1月31日.md "wikilink") - バージョン3.1.0がリリースされる
  - [2012年](../Page/2012年.md "wikilink")（平成24年）[6月29日](../Page/6月29日.md "wikilink") - バージョン3.2.0がリリースされる
  - [2012年](../Page/2012年.md "wikilink")（平成24年）[11月9日](../Page/11月9日.md "wikilink") - バージョン3.3.0がリリースされる
  - [2014年](../Page/2014年.md "wikilink")（平成26年）[3月31日](../Page/3月31日.md "wikilink") - バージョン3.4.0がリリースされる
  - [2016年](../Page/2016年.md "wikilink")（平成28年）[1月25日](../Page/1月25日.md "wikilink") - バージョン3.5.0がリリースされる
  - [2016年](../Page/2016年.md "wikilink")（平成28年）[7月29日](../Page/7月29日.md "wikilink") - バージョン3.5.1がリリースされる
  - [2017年](../Page/2017年.md "wikilink")（平成29年）[6月29日](../Page/6月29日.md "wikilink") - バージョン3.6.0がリリースされる
  - [2018年](../Page/2018年.md "wikilink")（平成30年）[1月31日](../Page/1月31日.md "wikilink") - バージョン3.7.0がリリースされる

## Claws Mail

Paul Manganらによって、Sylpheedから[フォークした](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")[Claws Mailがある](https://ja.wikipedia.org/wiki/Claws_Mail "wikilink")\[30\]。フォーク当時のSylpheedにない機能を独自に追加している。

## 脚注

### 注釈

### 出典

## 外部リンク

  - [Sylpheed 公式サイト](https://sylpheed.sraoss.jp/ja/)
      - [公式サイト](https://sylpheed.sraoss.jp/en/)
  - [作者による開発日記](https://sylpheed.sraoss.jp/diary/)
  - [Claws Mail 公式サイト](https://www.claws-mail.org/)
  - [Sylpheed Wiki](https://sylpheed.sraoss.jp/wiki/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:電子メールソフト](https://ja.wikipedia.org/wiki/Category:電子メールソフト "wikilink") [Category:GTK+を使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:GTK+を使用するソフトウェア "wikilink") [Category:2000年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2000年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.  エンタープライズ {{\!}} マイコミジャーナル|author=海上忍|publisher=マイコミジャーナル|date=2006-02-14|accessdate=2009-02-27}}
29.
30. フォーク当初の名称は「Sylpheed Claws」。後に「Claws Mail」と改名。