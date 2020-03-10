> この記事は[Uniscribe](https://ja.wikipedia.org/wiki/Uniscribe)から翻訳されています。


**Uniscribe**は、[Microsoft Windowsにおいて](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Unicode](../Page/Unicode.md "wikilink")によって符号化されたテキストを描画するためのレンダリングサービスである。「USP10.DLL」という[ダイナミックリンクライブラリ](../Page/ダイナミックリンクライブラリ.md "wikilink")として実装されている。USP10.dllは、[Windows 2000および](../Page/Microsoft_Windows_2000.md "wikilink")[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 5.0以降、一般に利用できるようになった。さらに、[Windows CE環境ではバージョン](https://ja.wikipedia.org/wiki/Windows_CE "wikilink")5.0からUniscribeに対応した。

## 解説

Uniscribeの主な目的は以下のとおり:

1.  テキストの入力列を表示列にする。
2.  文脈に応じてグリフの置換を行う (例えばアラビア文字での、語中の位置に依存する字形など)。
3.  テキストの書字方向 (LTR \[左から右\] かRTL \[右から左\] か、横書きか縦書きか、など) に基づき、表示されるテキストを並べ替える。

## USP10.dll

USPは、**U**nicode **S**cripts **P**rocessor の略号である。以下に、usp10.dllの主なバージョンと、それぞれの配布の形態を示す。

<table>
<thead>
<tr class="header">
<th><p>バージョン番号</p></th>
<th><p>ファイルサイズ</p></th>
<th><p>ファイル日付</p></th>
<th><p>バンドルされたソフトウェア</p></th>
<th><p>このバージョンでの新仕様</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.626.7601.17105</p></td>
<td><p>611 KiB</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2010年" title="wikilink">2010年</a><a href="../Page/9月30日.md" title="wikilink">9月30日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_7" title="wikilink">Windows 7</a> SP1 RC</p></td>
<td><p><a href="../Page/追加多言語面.md" title="wikilink">追加多言語面</a>で未定義のコードポイントおよび<a href="https://ja.wikipedia.org/wiki/私用面" title="wikilink">私用面</a>が表示されない問題を修正[1]。</p></td>
</tr>
<tr class="even">
<td><p>1.626.7600.20602</p></td>
<td><p>623 KiB</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2010年" title="wikilink">2010年</a><a href="../Page/1月7日.md" title="wikilink">1月7日</a></p></td>
<td><p><a href="../Page/Microsoft_Office.md" title="wikilink">Microsoft Office</a> 2010</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.626.7600.16385</p></td>
<td><p>612 KiB</p></td>
<td><p><a href="../Page/2009年.md" title="wikilink">2009年</a><a href="../Page/7月14日.md" title="wikilink">7月14日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_7" title="wikilink">Windows 7</a> RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/異体字セレクタ" title="wikilink">異体字セレクタ</a>に対応。一方、どういうわけか<a href="../Page/追加多言語面.md" title="wikilink">追加多言語面</a>の当時（Unicode 5.1の時点で）未定義であったコードポイントの文字、および<a href="https://ja.wikipedia.org/wiki/私用面" title="wikilink">私用面</a>（Unicodeの第15面、第16面）の文字が表示できなくなってしまっている。そのためUnicode 5.2以降に完全対応できない[2]。</p></td>
</tr>
<tr class="even">
<td><p>1.626.7100.0</p></td>
<td><p>612 KiB</p></td>
<td><p><a href="../Page/2009年.md" title="wikilink">2009年</a><a href="../Page/4月22日.md" title="wikilink">4月22日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_7" title="wikilink">Windows 7</a> RC</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.626.6001.16510</p></td>
<td><p>491 <a href="https://ja.wikipedia.org/wiki/キビバイト" title="wikilink">KiB</a></p></td>
<td><p><a href="../Page/2007年.md" title="wikilink">2007年</a><a href="../Page/4月18日.md" title="wikilink">4月18日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_Server_2008" title="wikilink">Windows Server "Longhorn"</a> Beta 3</p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>1.626.6000.20581</p></td>
<td><p>491 KiB<br />
(502,784 バイト)</p></td>
<td><p>2007/04/19 02:15:55 <a href="../Page/協定世界時.md" title="wikilink">UTC</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista" title="wikilink">Windows Vista</a> <a href="https://ja.wikipedia.org/wiki/:en:Hotfix" title="wikilink">Hotfix</a> <a href="http://support.microsoft.com/kb/936176">KB936176</a></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>1.626.6000.16386</p></td>
<td><p>491 KiB<br />
(502,784 バイト)</p></td>
<td><p>2006/11/02 09:44:03 UTC</p></td>
<td><p>Windows Vista RTM</p></td>
<td><p>PR-37に対応: インド系文字におけるZero Width Joinerの使用を明確化[3]</p></td>
</tr>
<tr class="even">
<td><p>1.626.5756.0</p></td>
<td><p>491 KiB</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2006年" title="wikilink">2006年</a><a href="https://ja.wikipedia.org/wiki/10月13日" title="wikilink">10月13日</a></p></td>
<td><p><a href="../Page/Microsoft_Office.md" title="wikilink">Microsoft Office</a> 2007 RTM</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.615.5384.4</p></td>
<td><p>484 KiB</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2006年" title="wikilink">2006年</a><a href="../Page/6月17日.md" title="wikilink">6月17日</a></p></td>
<td><p>Windows Vista Beta 2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.614.5315.0</p></td>
<td><p>454 KiB</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2006年" title="wikilink">2006年</a><a href="../Page/3月13日.md" title="wikilink">3月13日</a></p></td>
<td><p>Microsoft Office 2007 Beta 2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.613.5291.0</p></td>
<td><p>481 KiB<br />
(492,544 バイト)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2006年" title="wikilink">2006年</a><a href="../Page/1月4日.md" title="wikilink">1月4日</a></p></td>
<td><p>Microsoft VOLT 1.2 <a href="http://groups.msn.com/MicrosoftVOLTuserscommunity/homepage.msnw?pgmarket=en-us">1</a> - Windows Vistaに同梱</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.609.5219.0</p></td>
<td><p>469 KiB</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2005年" title="wikilink">2005年</a><a href="../Page/8月17日.md" title="wikilink">8月17日</a></p></td>
<td><p>Microsoft Office 12 Professional beta 1</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.601.5022.8</p></td>
<td><p>428 KiB</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2005年" title="wikilink">2005年</a><a href="../Page/1月7日.md" title="wikilink">1月7日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:si:Wikipedia:Sinhala_font#How_to_write_Sinhala" title="wikilink">Sinhala Enabling Pack for XP 0.42</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/シンハラ語" title="wikilink">シンハラ語</a>対応</p></td>
</tr>
<tr class="even">
<td><p>1.473.4067.0</p></td>
<td><p>415 KiB<br />
(424,960 バイト)</p></td>
<td><p><a href="../Page/2004年.md" title="wikilink">2004年</a><a href="../Page/10月22日.md" title="wikilink">10月22日</a></p></td>
<td><p>MSN groupsのMicrosoft VOLT discussion forum</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.471.4063.0</p></td>
<td><p>415 KiB<br />
(424,960 バイト)</p></td>
<td><p><a href="../Page/2004年.md" title="wikilink">2004年</a><a href="../Page/2月4日.md" title="wikilink">2月4日</a></p></td>
<td><p>Microsoft Office 2003</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/クメール文字" title="wikilink">クメール文字</a>サポートを提供。</p></td>
</tr>
<tr class="even">
<td><p>1.471.4030.0</p></td>
<td><p>404 KiB<br />
(413,184 バイト)</p></td>
<td><p><a href="../Page/2004年.md" title="wikilink">2004年</a><a href="../Page/4月15日.md" title="wikilink">4月15日</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Google_Earth" title="wikilink">Google Earth</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.453.3665.0</p></td>
<td><p>? KiB<br />
(? バイト)</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p><a href="../Page/チベット語.md" title="wikilink">チベット語</a>サポートを提供。</p></td>
</tr>
<tr class="even">
<td><p>1.422.3790.1830</p></td>
<td><p>355 KiB<br />
(364,032 バイト)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2005年" title="wikilink">2005年</a><a href="../Page/3月30日.md" title="wikilink">3月30日</a></p></td>
<td><p><a href="../Page/Microsoft_Windows_Server_2003.md" title="wikilink">Windows Server 2003</a> SP1</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.421.3790.0</p></td>
<td><p>353,280 バイト</p></td>
<td><p><a href="../Page/2003年.md" title="wikilink">2003年</a><a href="https://ja.wikipedia.org/wiki/3月25日" title="wikilink">3月25日</a></p></td>
<td><p>Windows Server 2003</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.420.2600.2180</p></td>
<td><p>397 KiB<br />
(406,528 バイト)</p></td>
<td><p><a href="../Page/2004年.md" title="wikilink">2004年</a><a href="../Page/8月12日.md" title="wikilink">8月12日</a></p></td>
<td><p><a href="../Page/Microsoft_Windows_XP.md" title="wikilink">Windows XP</a> SP2 Build 2180</p></td>
<td><p><a href="../Page/ベンガル語.md" title="wikilink">ベンガル語</a>と<a href="https://ja.wikipedia.org/wiki/マラヤーラム語" title="wikilink">マラヤーラム語</a>に対応</p></td>
</tr>
<tr class="odd">
<td><p>1.409.2600.1106</p></td>
<td><p>331 KiB<br />
(339,456 バイト)</p></td>
<td><p><a href="../Page/2002年.md" title="wikilink">2002年</a><a href="../Page/8月29日.md" title="wikilink">8月29日</a></p></td>
<td><p>Windows XP SP1 Build 1106</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.0408.2600.1020</p></td>
<td><p>331 KiB (339,456 バイト)</p></td>
<td><p><a href="../Page/2002年.md" title="wikilink">2002年</a><a href="../Page/4月17日.md" title="wikilink">4月17日</a></p></td>
<td><p>Internet Explorer 6.0.2800.1106 (SP1)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.407.2600.0</p></td>
<td><p>331 KiB<br />
(339,456 バイト)</p></td>
<td><p><a href="../Page/2001年.md" title="wikilink">2001年</a><a href="../Page/8月17日.md" title="wikilink">8月17日</a></p></td>
<td><p>Windows XP</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ターナ文字" title="wikilink">ターナ文字</a>、<a href="https://ja.wikipedia.org/wiki/グジャラーティー文字" title="wikilink">グジャラーティー文字</a>、<a href="https://ja.wikipedia.org/wiki/カンナダ文字" title="wikilink">カンナダ文字</a>、<a href="https://ja.wikipedia.org/wiki/グルムキー文字" title="wikilink">グルムキー文字</a> (<a href="https://ja.wikipedia.org/wiki/パンジャーブ語" title="wikilink">パンジャーブ語</a>)、<a href="../Page/シリア文字.md" title="wikilink">シリア文字</a>および<a href="https://ja.wikipedia.org/wiki/テルグ文字" title="wikilink">テルグ文字</a></p></td>
</tr>
<tr class="even">
<td><p>1.405.2416.1</p></td>
<td><p>317 KiB<br />
(325,120 バイト)</p></td>
<td><p><a href="../Page/2001年.md" title="wikilink">2001年</a><a href="../Page/1月15日.md" title="wikilink">1月15日</a></p></td>
<td><p>Microsoft Office XP</p></td>
<td><p><a href="../Page/ヘブライ語.md" title="wikilink">ヘブライ語</a>サポート</p></td>
</tr>
<tr class="odd">
<td><p>1.400.2411.1 <a href="http://support.microsoft.com/kb/298624">2</a></p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>Internet Explorer 6</p></td>
<td><p>1.325.2195.6692から<a href="../Page/アラビア語.md" title="wikilink">アラビア語</a>サポート</p></td>
</tr>
<tr class="even">
<td><p>1.325.2195.6692</p></td>
<td><p>308 KiB<br />
(315,664 バイト)</p></td>
<td><p><a href="../Page/2003年.md" title="wikilink">2003年</a><a href="../Page/6月19日.md" title="wikilink">6月19日</a></p></td>
<td><p><a href="../Page/Microsoft_Windows_2000.md" title="wikilink">Windows 2000</a> SP4 (?)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.325.2195.1340</p></td>
<td><p>308 KiB<br />
(315,664 バイト)</p></td>
<td><p><a href="../Page/2000年.md" title="wikilink">2000年</a><a href="../Page/7月21日.md" title="wikilink">7月21日</a></p></td>
<td><p>Windows 2000 SP1</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.325.2180.1</p></td>
<td><p>316 KiB<br />
(323,584 バイト)</p></td>
<td><p><a href="../Page/2000年.md" title="wikilink">2000年</a><a href="../Page/6月8日.md" title="wikilink">6月8日</a></p></td>
<td><p><a href="../Page/Microsoft_Windows_Millennium_Edition.md" title="wikilink">Windows Me</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>307 KiB<br />
(315,152 バイト)</p></td>
<td><p><a href="../Page/2000年.md" title="wikilink">2000年</a><a href="../Page/4月26日.md" title="wikilink">4月26日</a></p></td>
<td><p>Microsoft Global IME for Office XP</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>307 KiB<br />
(315,152 バイト)</p></td>
<td><p><a href="../Page/1999年.md" title="wikilink">1999年</a><a href="../Page/11月30日.md" title="wikilink">11月30日</a></p></td>
<td><p>Internet Explorer 5.5 release, SP1 &amp; SP2</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.175.0.1</p></td>
<td><p>268 KiB<br />
(274,432 バイト)</p></td>
<td><p><a href="../Page/1999年.md" title="wikilink">1999年</a><a href="../Page/5月5日.md" title="wikilink">5月5日</a></p></td>
<td><p><a href="../Page/Microsoft_Windows_98.md" title="wikilink">Windows 98</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>258 KiB<br />
(264,976 バイト)</p></td>
<td><p><a href="../Page/1999年.md" title="wikilink">1999年</a><a href="../Page/1月28日.md" title="wikilink">1月28日</a></p></td>
<td><p>Internet Explorer 5.01</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.163.1890.1</p></td>
<td><p>262 KiB<br />
(268,288 バイト)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1998年" title="wikilink">1998年</a><a href="../Page/9月22日.md" title="wikilink">9月22日</a></p></td>
<td><p>Multilanguage Text Layout and Complex Scripts (MTLCS) のスナップショット</p></td>
<td></td>
</tr>
</tbody>
</table>

## 更新するには

UniscribeはWindows 2000以上で利用可能だが、その後のバージョンアップでさらに機能が追加されている。つまり、さらに多くの用字系 ([文字体系](https://ja.wikipedia.org/wiki/文字体系 "wikilink")) に対応できる。初期の更新では、[アラビア語](../Page/アラビア語.md "wikilink")と[ヘブライ語](../Page/ヘブライ語.md "wikilink")に、その後[タイ語](../Page/タイ語.md "wikilink")と[ベトナム語](../Page/ベトナム語.md "wikilink")に対応した。[Windows XP以降は](../Page/Microsoft_Windows_XP.md "wikilink")、さらに南アジアおよびアッシリアの音素文字に対応した。

より新しいusp10.dllを特定のアプリケーションでだけ使えればよいのであれば、より新しいバージョンのファイルをそのアプリケーションのディレクトリにコピーすればよい。

## 参考資料

<references />

  - [Uniscribe](http://www.microsoft.com/typography/developers/uniscribe/default.htm) (英語)
  - [Microsoft Typography](http://www.microsoft.com/typography) (英語)
  - [Uniscribe at MSDN](http://msdn.microsoft.com/library/en-us/intl/uniscrib_35k5.asp) (英語)
  - [国際SIL](https://ja.wikipedia.org/wiki/国際SIL "wikilink"). [Uniscribe versions](http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&item_id=UniscribeVersions) (英語)

## 外部リンク

  - [How to update usp10.dll at Windows 2000](http://www.aksharamala.com/help/chm/Installation/win2k.html) (英語)
  - [FAQ about usp10.dll](http://www.unimm.org/cms/node/13) (英語)
  - [Uniscribe versions](https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&item_id=UniscribeVersions) (英語)

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink")

1.
2.
3.  <http://unicode.org/review/pr-37.pdf>