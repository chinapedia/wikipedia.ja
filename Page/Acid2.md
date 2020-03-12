> この記事は[Acid2](https://ja.wikipedia.org/wiki/Acid2)から翻訳されています。


**Acid2**（アシッドツー）は[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")や[オーサリングツール](../Page/オーサリングツール.md "wikilink")における[ウェブページ](../Page/ウェブページ.md "wikilink")のレンダリング上の問題点を特定するために[ウェブスタンダードプロジェクト](../Page/ウェブスタンダードプロジェクト.md "wikilink")(WaSP)が作成した[テストケース](https://ja.wikipedia.org/wiki/テストケース "wikilink")である。Acid2は同様のテストケース・[Acid1](https://ja.wikipedia.org/wiki/Acid1 "wikilink")（1998年開発）を後継したが、ほぼ主流ブラウザの対応完了およびさらなる後継版である[Acid3](https://ja.wikipedia.org/wiki/Acid3 "wikilink")の公開（2008年3月）によって役目を終えつつある。

[HTML](../Page/HyperText_Markup_Language.md "wikilink") や [CSS](../Page/Cascading_Style_Sheets.md "wikilink") 2.1などの [W3C](../Page/World_Wide_Web_Consortium.md "wikilink") 勧告等に、どの程度準拠しているかを測るために用いられる。完全に準拠したレンダリングで描かれるはずの画像とそのソースがあり、レンダリングイメージと画像の相違によりどの程度準拠しているかを測る。正確に準拠していれば、[スマイリーが描かれる](../Page/スマイリーフェイス.md "wikilink")。

## 各ウェブブラウザでの状況

[Mozilla Firefox 3](../Page/Mozilla_Firefox.md "wikilink") などで用いられている [Gecko](../Page/Gecko.md "wikilink") は、バージョン 1.9 で Acid2 に合格している\[1\]\[2\]。Firefox 2 に代表される、Gecko 1.8以前では対応できていない。

[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 開発元の[マイクロソフト](../Page/マイクロソフト.md "wikilink")は、CSS の標準準拠度を高めることに取り組んでいるが Acid2 への合格を第一目標として取り組んではおらず、結局 Internet Explorer 7 はテストに合格しないという結果に終わった。Internet Explorer 8 では、現在動作中のコードにて Acid2 に合格したことが、開発チームのブログによって公表された\[3\]。（ただし、Acid2の文法ミスを修正したバージョンにてチェックすると、アドオン「Microsoft HTML Viewer」の追加が要求され、追加するとスマイリーの目の周りが黒くなる。）

## 合格したアプリケーション

[150px](https://ja.wikipedia.org/wiki/ファイル:Safariacid2.png "wikilink") Acid2テストは[2005年](../Page/2005年.md "wikilink")[4月13日](../Page/4月13日.md "wikilink")に公式発表された。テストに合格した代表的なソフトウェアリリースを時系列に沿って下記に示す（公式版初リリース時に既に合格していたアプリケーションは含んでいない）。 なお、下記に挙げられたブラウザでもページをスクロールさせたり、極端なフォントやウィンドウのサイズを設定するとスマイリーが不正確に表示される可能性がある。これは予期された振る舞いであり、ブラウザがテストに合格していないというわけではない。

<table>
<thead>
<tr class="header">
<th><p>日付</p></th>
<th><p>ソフトウェア</p></th>
<th><p>種別</p></th>
<th><p>注記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2005年<a href="../Page/4月27日.md" title="wikilink">4月27日</a></p></td>
<td><p><a href="../Page/Safari.md" title="wikilink">Safari</a></p></td>
<td><p>非公開版[4]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2005年<a href="../Page/5月18日.md" title="wikilink">5月18日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/iCab" title="wikilink">iCab</a></p></td>
<td><p>非公開版</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2005年<a href="../Page/5月20日.md" title="wikilink">5月20日</a></p></td>
<td><p>iCab</p></td>
<td><p>会員のみに公開</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2005年<a href="../Page/6月4日.md" title="wikilink">6月4日</a></p></td>
<td><p><a href="../Page/Konqueror.md" title="wikilink">Konqueror</a></p></td>
<td><p>非公開版[5]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2005年<a href="../Page/6月6日.md" title="wikilink">6月6日</a></p></td>
<td><p>iCab</p></td>
<td><p>公開開発版</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2005年<a href="../Page/10月31日.md" title="wikilink">10月31日</a></p></td>
<td><p>Safari</p></td>
<td><p>公式リリース版</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">Mac OS X</a> 10.4.3 上の Version 2.02 にて。公式リリース版ブラウザとして初の合格。</p></td>
</tr>
<tr class="odd">
<td><p>2005年<a href="../Page/11月29日.md" title="wikilink">11月29日</a></p></td>
<td><p>Konqueror</p></td>
<td><p>公式リリース版[6]</p></td>
<td><p><a href="../Page/KDE.md" title="wikilink">KDE</a> 3.5 上にて。 <a href="../Page/UNIX.md" title="wikilink">UNIX</a> や <a href="../Page/Linux.md" title="wikilink">Linux</a> ベースのブラウザとして初の合格。</p></td>
</tr>
<tr class="even">
<td><p>2005年<a href="../Page/12月7日.md" title="wikilink">12月7日</a></p></td>
<td><p>Prince</p></td>
<td><p>公式リリース版[7]</p></td>
<td><p>Version 5.1。<a href="../Page/Extensible_Markup_Language.md" title="wikilink">XML</a> を <a href="../Page/Portable_Document_Format.md" title="wikilink">PDF</a> に変換するコンバータ。ブラウザ以外のソフトウェアとして初の合格。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/2006年.md" title="wikilink">2006年</a><a href="../Page/3月10日.md" title="wikilink">3月10日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Opera" title="wikilink">Opera</a></p></td>
<td><p>公開weeklyビルド[8]</p></td>
<td><p>Opera9 Windows 版 Weelky build にて。<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows" title="wikilink">Windows上のブラウザとして初の合格</a>。公式ベータ版が<a href="https://ja.wikipedia.org/wiki/4月20日" title="wikilink">4月20日</a>にリリースされたが、これも同様に合格。</p></td>
</tr>
<tr class="even">
<td><p>2006年<a href="../Page/3月24日.md" title="wikilink">3月24日</a></p></td>
<td><p>iCab</p></td>
<td><p>会員のみに公開</p></td>
<td><p>iCab 3.0.2b400。スクロールバーが表示される問題を解決。</p></td>
</tr>
<tr class="odd">
<td><p>2006年<a href="../Page/3月28日.md" title="wikilink">3月28日</a></p></td>
<td><p>Konqueror</p></td>
<td><p>公式リリース版[9]</p></td>
<td><p>ていた、スクロールバーが表示される問題を解決。バージョン 3.5.2。</p></td>
</tr>
<tr class="even">
<td><p>2006年<a href="../Page/4月12日.md" title="wikilink">4月12日</a></p></td>
<td><p><a href="../Page/Mozilla_Firefox.md" title="wikilink">Firefox</a></p></td>
<td><p>半公開版[10]</p></td>
<td><p>ビルドを作るためのファイルは提供されたが、多少の組み立てが必要。</p></td>
</tr>
<tr class="odd">
<td><p>2006年<a href="../Page/5月24日.md" title="wikilink">5月24日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Opera" title="wikilink">Opera</a> Mobile</p></td>
<td><p>非公開版[11]</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/モバイル" title="wikilink">モバイル</a>向けブラウザとして初の合格。</p></td>
</tr>
<tr class="even">
<td><p>2006年<a href="../Page/6月20日.md" title="wikilink">6月20日</a></p></td>
<td><p>Opera 9.0</p></td>
<td><p>公式リリース版[12]</p></td>
<td><p><a href="../Page/クロスプラットフォーム.md" title="wikilink">クロスプラットフォーム</a>なブラウザとして初の合格。</p></td>
</tr>
<tr class="odd">
<td><p>2006年<a href="../Page/6月30日.md" title="wikilink">6月30日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Obigo_Browser" title="wikilink">Obigo Browser</a></p></td>
<td><p>非公開版[13]</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/モバイル" title="wikilink">モバイル</a>向けブラウザとして2つ目の合格。</p></td>
</tr>
<tr class="even">
<td><p>2006年<a href="../Page/8月17日.md" title="wikilink">8月17日</a></p></td>
<td><p>iCab 3.0.3</p></td>
<td><p>公式リリース版</p></td>
<td><p>スクロールバーを非表示にした最初の公式リリース。</p></td>
</tr>
<tr class="odd">
<td><p>2006年<a href="../Page/12月8日.md" title="wikilink">12月8日</a></p></td>
<td><p>Mozilla Firefox</p></td>
<td><p>公開nightlyビルド</p></td>
<td><p>「reflow-refactoringブランチ」が投入され通常の開発版にて合格。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/2007年.md" title="wikilink">2007年</a><a href="../Page/12月12日.md" title="wikilink">12月12日</a></p></td>
<td><p><a href="../Page/Internet_Explorer.md" title="wikilink">Internet Explorer 8</a></p></td>
<td><p>非公開版[14]</p></td>
<td><p>開発中のコードにてIEシリーズでは初の合格となる。ただし独自のmetaタグを記述し、IE8から導入されたモードで動作させなければならない[15]。(正式リリース版ではこの方針は撤回された)</p></td>
</tr>
<tr class="odd">
<td><p>2008年3月5日</p></td>
<td><p></p></td>
<td><p>公開ベータ版[16]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2008年<a href="../Page/6月18日.md" title="wikilink">6月18日</a></p></td>
<td><p>Firefox 3</p></td>
<td><p>公式リリース版</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2008年8月27日</p></td>
<td><p></p></td>
<td><p>公開ベータ版[17]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2008年12月8日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Antenna_House_Formatter" title="wikilink">Antenna House Formatter</a> </p></td>
<td><p>公開ベータ版[18]</p></td>
<td><p><a href="../Page/Extensible_Markup_Language.md" title="wikilink">XMLや</a><a href="../Page/HyperText_Markup_Language.md" title="wikilink">HTML文書を印刷または</a><a href="../Page/Portable_Document_Format.md" title="wikilink">PDFに出力する</a><a href="../Page/組版.md" title="wikilink">組版</a>ソフトウェア。</p></td>
</tr>
<tr class="odd">
<td><p>2009年3月20日</p></td>
<td><p>Internet Explorer 8</p></td>
<td><p>公式リリース版</p></td>
<td><p>IEの公式リリース版では初の合格。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 不合格のアプリケーション

[Internet Explorerも](../Page/Internet_Explorer.md "wikilink")、[CSS勧告への適合に向けて前進してはいるが](../Page/Cascading_Style_Sheets.md "wikilink")、Internet Explorer 7の時点では、テストに合格していない。Internet Explorerプラットフォームアーキテクトであるクリス・ウィルソンは、Acid2を真の標準適合性テストというより機能の「要望リスト」であるとしていた\[19\]。それにもかかわらず、Internet Explorer 8には「IE8標準モード」と呼ばれる新しい描画モードが含まれる予定である\[20\]。当初、IE8標準モードは既定では有効にされないが、Webページに特殊なフラグを挿入することで切り替えられるようにする予定であった\[21\]。IE8標準モードではIE8はAcid2テストに合格するが\[22\]、IE8標準モードは既定では有効にされていなかったので\[23\]、[オペラ・ソフトウェア](https://ja.wikipedia.org/wiki/オペラ・ソフトウェア "wikilink")の[CTOである](../Page/最高技術責任者.md "wikilink")[ホーコン・ウィウム・リー](../Page/ホーコン・ウィウム・リー.md "wikilink")はIE8が真にテストに合格したとはみなせないと主張していた\[24\]\[25\]。その後、マイクロソフトが同社の[相互運用性](https://ja.wikipedia.org/wiki/相互運用性 "wikilink")に関する方針を見直したことによってフル標準モードがデフォルトの[レンダリングモードに変更された](../Page/レンダリング_\(コンピュータ\).md "wikilink")\[26\]。[互換モード](https://ja.wikipedia.org/wiki/互換モード "wikilink")でのレンダリングには、利用者側でIE7エミュレートボタンを使用するか\[27\]、Webサイト側がmeta要素などで明示する必要がある\[28\]。

[Firefox 2など](../Page/Mozilla_Firefox.md "wikilink")、レイアウトエンジンに[Gecko](../Page/Gecko.md "wikilink")バージョン1.8を採用するブラウザは、テストに合格しない。その他[NetFront](https://ja.wikipedia.org/wiki/NetFront "wikilink")や、それを基にした[プレイステーション3のウェブブラウザもテストに失敗する](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")。

以下に各ブラウザの不合格であったバージョンにおける描画例を示す。

ファイル:Ieacid2.png|[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 6.0 ファイル:Ie7acid2.png|[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 7.0 ファイル:Acid2 NS72.png|[Firefox](../Page/Mozilla_Firefox.md "wikilink") 1.0、[Mozilla](../Page/Mozilla_Application_Suite.md "wikilink") 1.7.13、および[Netscape](../Page/Netscapeシリーズ.md "wikilink") 7.2 ファイル:Firefoxacid2.png|[Firefox](../Page/Mozilla_Firefox.md "wikilink") 1.5、2.0 および[Netscape](../Page/Netscapeシリーズ.md "wikilink") 9.0.0.6 ファイル:Konqueror 3.4.1 Acid2.png|[Konqueror](../Page/Konqueror.md "wikilink") 3.4 ファイル:Opera 8.0 Acid2.png|[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink") 8.0 ファイル:Opera 8.54 Acid2.png|[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink") 8.54 ファイル:Acid2 in Opera Mini 4.png|[Opera Mini](https://ja.wikipedia.org/wiki/Opera_Mini "wikilink") 4 ファイル:Acid2iPod.png|[iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink") 2.0 ファイル:Acid2iPod2 1.JPG|[iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink") 2.1

## 関連項目

  - [Comparison of layout engines](https://ja.wikipedia.org/wiki/:en:Comparison_of_layout_engines "wikilink")
  - [Acid3](https://ja.wikipedia.org/wiki/Acid3 "wikilink")

## 参考文献

<div class="references-small">

<references/>

</div>

## 外部リンク

  - [Acid2 Browser Test - The Web Standards Project（英語）](http://www.webstandards.org/action/acid2/)
      - [Acid2: The Guided Tour](http://www.webstandards.org/action/acid2/guide/)
      - [The Acid2 Test](http://www.webstandards.org/files/acid2/test.html)

[Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:ウェブデザイン](https://ja.wikipedia.org/wiki/Category:ウェブデザイン "wikilink") [Category:ウェブブラウザ](https://ja.wikipedia.org/wiki/Category:ウェブブラウザ "wikilink")

1.
2.  [mozillawiki:Gecko:Reflow_Refactoring](https://ja.wikipedia.org/wiki/mozillawiki:Gecko:Reflow_Refactoring "wikilink")
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
17. [IE8でWebサイト運営者は4回うれしい](http://ascii.jp/elem/000/000/168/168168/)Acsii.jp
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
28.