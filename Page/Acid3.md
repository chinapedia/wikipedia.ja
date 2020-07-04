> この記事は[Acid3](https://ja.wikipedia.org/wiki/Acid3)から翻訳されています。


**Acid3**（アシッドスリー）は[ウェブスタンダードプロジェクト](../Page/ウェブスタンダードプロジェクト.md "wikilink")によるテストページである。[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")が特定の[ウェブ標準](../Page/ウェブ標準.md "wikilink")にどれだけ従っているのかを調べることを目的にしている。特に[DOMと](../Page/Document_Object_Model.md "wikilink")[JavaScript](../Page/JavaScript.md "wikilink")に関連した[ウェブ標準](../Page/ウェブ標準.md "wikilink")を対象にしている。

このページは2007年4月から開発され\[1\]、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[3月3日](../Page/3月3日.md "wikilink")にリリースされた\[2\]。主な開発者は[Acid2](../Page/Acid2.md "wikilink")テストを書いた[イアン・ヒクソン](https://ja.wikipedia.org/wiki/イアン・ヒクソン "wikilink")である。Acid2が主に[CSSに焦点を当てているのに対し](../Page/Cascading_Style_Sheets.md "wikilink")、Acid3テストでは[ECMAScript](../Page/ECMAScript.md "wikilink")やDOM Level 2といった、現代的で双方向性の高いウェブサイトで使われる技術にも焦点を当てている。いくつかのテストは [SVG](../Page/Scalable_Vector_Graphics.md "wikilink")、[XMLや](../Page/Extensible_Markup_Language.md "wikilink")[data URIにも関連している](https://ja.wikipedia.org/wiki/data_URI_scheme "wikilink")。2004年時点での仕様における要素のみが含まれている\[3\]。

成功したとき、背景に色の付いた長方形とともに、Acid3テストは次第に上昇するパーセンテージカウンタを表示する。パーセンテージは合格した部分テストの数に基づいている。これに加え、ブラウザは参照ページでレンダリングした通りにテストページをレンダリングしなければならない。Acid2テストとは異なり、フォントのレンダリングにおける若干の違いを考慮に入れるため、参照レンダリングはビットマップではない。

## 合格したアプリケーション

スコアが満点（100/100）で正しくレンダリング出来たもの。

<table>
<thead>
<tr class="header">
<th><p>日付</p></th>
<th><p><br />
エンジン</p></th>
<th><p>ソフトウェア</p></th>
<th><p>種別</p></th>
<th><p>注記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/2008年" title="wikilink">2008年</a><a href="../Page/9月25日.md" title="wikilink">9月25日</a></p></td>
<td><p><a href="../Page/WebKit.md" title="wikilink">WebKit</a></p></td>
<td></td>
<td><p>公開評価版</p></td>
<td><p>r36882。合格したものとして最初に公開された<a href="https://ja.wikipedia.org/wiki/レンダリングエンジン" title="wikilink">レンダリングエンジン</a>[4]。</p></td>
</tr>
<tr class="even">
<td><p>2008年<a href="../Page/12月3日.md" title="wikilink">12月3日</a></p></td>
<td><p><a href="../Page/Presto.md" title="wikilink">Presto</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Opera" title="wikilink">Opera</a></p></td>
<td><p>公開評価版</p></td>
<td><p>10.0 アルファ版にて[5]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/2009年.md" title="wikilink">2009年</a><a href="https://ja.wikipedia.org/wiki/3月14日" title="wikilink">3月14日</a></p></td>
<td><p>Webkit</p></td>
<td><p>Iris Browser</p></td>
<td><p>公開版</p></td>
<td><p>1.1.4 正式版にて。モバイル向けおよび正式版のブラウザとして初の合格。</p></td>
</tr>
<tr class="even">
<td><p>2009年<a href="https://ja.wikipedia.org/wiki/3月26日" title="wikilink">3月26日</a></p></td>
<td><p>Presto</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Opera_Mobile" title="wikilink">Opera Mobile</a></p></td>
<td><p>9.7 正式版にて。</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2009年<a href="../Page/6月7日.md" title="wikilink">6月7日</a></p></td>
<td><p>WebKit</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/iCab" title="wikilink">iCab</a></p></td>
<td><p>4.6 正式版にて。iCab 4.6はAcid3を100/100で通過した初めてのウェブブラウザとなった。</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2009年<a href="../Page/6月8日.md" title="wikilink">6月8日</a></p></td>
<td><p>WebKit</p></td>
<td><p><a href="../Page/Safari.md" title="wikilink">Safari</a></p></td>
<td><p>4.0 正式版にて。デスクトップ向けの正式版のブラウザとして初の合格。</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2009年<a href="../Page/9月1日.md" title="wikilink">9月1日</a></p></td>
<td><p>Presto</p></td>
<td><p>Opera</p></td>
<td><p>10.0 正式版にて。</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2009年<a href="../Page/12月7日.md" title="wikilink">12月7日</a></p></td>
<td><p>Webkit</p></td>
<td><p>BOLT Browser</p></td>
<td><p>1.6 正式版にて。</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/2010年" title="wikilink">2010年</a><a href="https://ja.wikipedia.org/wiki/1月26日" title="wikilink">1月26日</a></p></td>
<td><p>Webkit</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Google_Chrome" title="wikilink">Google Chrome</a></p></td>
<td><p>4.0.249.78 正式版にて。</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/2011年.md" title="wikilink">2011年</a><a href="../Page/9月17日.md" title="wikilink">9月17日</a></p></td>
<td><p><a href="../Page/Trident.md" title="wikilink">Trident</a></p></td>
<td><p><a href="../Page/Internet_Explorer.md" title="wikilink">Internet Explorer</a></p></td>
<td><p>9.0 正式版にて。Acid3のアップデートにより合格。</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2011年9月17日</p></td>
<td><p><a href="../Page/Gecko.md" title="wikilink">Gecko</a></p></td>
<td><p><a href="../Page/Mozilla_Firefox.md" title="wikilink">Mozilla Firefox</a></p></td>
<td><p>6.0.2 正式版にて。Acid3のアップデートにより合格。</p></td>
<td></td>
</tr>
</tbody>
</table>

## 不合格のアプリケーション

<table>
<thead>
<tr class="header">
<th><p>ソフトウェア</p></th>
<th><p><br />
エンジン</p></th>
<th><p>点数</p></th>
<th><p>種別</p></th>
<th><p>注記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Android 2.2</p></td>
<td><p>WebKit</p></td>
<td><p>93</p></td>
<td><p>公開版</p></td>
<td></td>
</tr>
</tbody>
</table>

## 各ブラウザの適合状況

2010年4月現在（モバイル向けに関しては2009年9月1日時点、ゲーム機向けに関しては2010年1月6日）の各ブラウザの適合状況は以下のようになっている。 なお、各ブラウザの適合状況は2010年4月現在公開されている最新の安定版のものとする。

### デスクトップ向けブラウザ

#### Internet Explorer

2010年3月に9.0のプレビュー版がリリースされるにあたり、[マイクロソフト](../Page/マイクロソフト.md "wikilink")側から初めてAcid3についての言及があった\[6\]。プレビュー版（1.9.7.7.45.6019）の時点でスコアは55/100で、プレビュー2（1.9.7.7.66.6000）の時点でスコアは68/100、プレビュー3（1.9.7.8.74.6000)の時点でスコアは83/100、プレビュー4（1.9.7916.6000）の時点でスコアは95/100と上昇した。開発が進むにつれAcid3準拠を進めていくとしているが、100点を取ることを優先目標とはしていない。9.0正式版では2011年9月17日にAcid3のアップデートにより合格した。

#### Mozilla Firefox

3.6ではスコアは94/100。 6.0.2の正式版は2011年9月17日にAcid3のアップデートにより合格した。

#### Opera

オペラ・ソフトウェアは[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[3月26日](https://ja.wikipedia.org/wiki/3月26日 "wikilink")に開発者向けのバージョンにてAcid3に対応したと発表し、[3月28日](../Page/3月28日.md "wikilink")にWindows版のWingogiとLinux版のLingogiが一般に公開された。しかし、不完全であり環境によっては正しくレンダリングされなかった。その後、2008年[12月3日](../Page/12月3日.md "wikilink")にバージョン10.0のアルファ版にてAcid3に合格し、[2009年](../Page/2009年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink")に公開されたバージョン10.0正式版でも合格した。

#### Safari

2008年3月26日にWebKit Nightly Builds r31342にてAcid3に合格したと発表した\[7\]。その後、アニメーション再生の滑らかさを含めたテストを合格し、Acid3を完全にパスしたr36882が2008年[9月25日](../Page/9月25日.md "wikilink")に公開され、2009年6月8日に公開されたSafari 4.0で正式版のブラウザとして最初に合格したブラウザとなった。

#### Google Chrome

V2.0の時からスコアは100/100となっていたが、画像右上にゴミが表示され、完全な合格とはいえない状態だった。[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[1月26日](https://ja.wikipedia.org/wiki/1月26日 "wikilink")に公開された4.0.249.78正式版ではゴミが表示されなくなり合格した。

#### Konqueror

スコアは89/100

### モバイル向けブラウザ

#### Mobile Safari（iPhone, iPod touch, iPad）

スコアは100/100となっているが、画像上にゴミが表示されており、完全な合格とはいえない状態である。

#### Opera Mobile

2009年3月26日に公開された9.7正式版で合格した（10.00のβ版の場合、β2uが99/100、β3は77/100であった）。

#### Opera Mini

スコアは98/100であるが、画像のレイアウトが崩れている。

#### Internet Explorer Mobile

IE Mobile 8.12（Windows Mobile 6.5 Professionalに添付のもの）で14/100であった。IE9 MobileではPC版同様95/100であったが、Acid3の仕様変更により100/100となった。

### ゲーム機搭載ブラウザ

#### PlayStation 3

スコアは100/100（システムソフトウェア バージョン4.20）

#### PlayStation Portable

スコアは11/100

#### PlayStation Vita

スコアは100/100(システムソフトウェア バージョン2.00)

#### Wii インターネットチャンネル

バージョン9.30でスコア40/100

#### ニンテンドーDSi

スコアは60/100

#### ニンテンドー3DS

スコアは92/100(ブラウザバージョン1.74987)

#### Wii U

スコアは100/100(ブラウザバージョン3.0.0.9561)

## 参照

## 外部リンク

  - [The Acid3 Test](http://acid3.acidtests.org/)
  - [The Acid3 Test (Reference Rendering)](http://acid3.acidtests.org/reference.html)
  - [The Acid3 test at Web standards Project](http://www.webstandards.org/action/acid3/)
  - [Acid3 - Browserscope](http://www.browserscope.org/?category=acid3)

[de:Acid (Browsertests)\#Acid3](https://ja.wikipedia.org/wiki/de:Acid_\(Browsertests\)#Acid3 "wikilink") [sv:Acid webbläsartester\#Acid3](https://ja.wikipedia.org/wiki/sv:Acid_webbläsartester#Acid3 "wikilink")

[Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:ウェブデザイン](https://ja.wikipedia.org/wiki/Category:ウェブデザイン "wikilink") [Category:ウェブブラウザ](https://ja.wikipedia.org/wiki/Category:ウェブブラウザ "wikilink")

1.
2.
3.
4.  [WebKitが「Acid3」に満点で合格 - ITmedia](http://www.itmedia.co.jp/enterprise/articles/0809/27/news010.html)
5.  [Opera Desktop Team - Peregrine takes flight... Opera 10.0 Alpha 1 is here\!](http://web.archive.org/web/20081205192034/http://my.opera.com/desktopteam/blog/2008/12/03/peregrine-takes-flight-opera-10-0-alpha-is-here)
6.  [HTML5, Hardware Accelerated: First IE9 Platform Preview Available for Developers](http://blogs.msdn.com/ie/archive/2010/03/16/html5-hardware-accelerated-first-ie9-platform-preview-available-for-developers.aspx) - IEBlog、2010年3月16日
7.  [WebKit achieves Acid3 100/100 in public build](http://webkit.org/blog/173/webkit-achieves-acid3-100100-in-public-build/)