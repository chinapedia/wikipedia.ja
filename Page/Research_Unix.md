> この記事は[Research Unix](https://ja.wikipedia.org/wiki/Research_Unix)から翻訳されています。


**Research Unix**は、[ベル研究所](../Page/ベル研究所.md "wikilink")（の、Computer Science Research Center）によって開発された[Unixのことで](../Page/UNIX.md "wikilink")、特にUnixの起原である初期バージョンとその直系にあたるシリーズを指す。後の時代においては、商用化された[System Vとは別に](../Page/UNIX_System_V.md "wikilink")、研究所においてトンプソンら当初の開発者らによって実験的な機能が実装されたバージョン8等のUnixを指して使われた。[Plan 9はその後継にあたる](../Page/Plan_9_from_Bell_Labs.md "wikilink")。

## 概要

Research Unix という用語は Version 8 Unix まであまり使われなかったが、その後遡って適用されるようになった。V8 以前、この系統は単に UNIX か UNIX Time-Sharing System と呼ばれていた。

初期のバージョンと後の方のいくつかのバージョンはベル研究所以外にリリースされることがなかった。また、コード系統が単純ではないため、Research Unix のバージョンは対応する[マニュアルの版によって識別される](../Page/Manページ.md "wikilink")。従って、最初の Research Unix は First Edition であり、最後は Tenth Edition である。他の呼び方としては Version *x* (または V*x*)もある(*x*はマニュアルの版数)。

### Research Unix のバージョン履歴

<table>
<caption>Research Unix のバージョン履歴</caption>
<thead>
<tr class="header">
<th><p>マニュアルエディション</p></th>
<th><p>リリース</p></th>
<th><p>特徴</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>V1</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1971年" title="wikilink">1971年</a></p></td>
<td><p>最初のUNIX、内部で使用された。</p></td>
</tr>
<tr class="even">
<td><p>V2</p></td>
<td><p><a href="../Page/1972年.md" title="wikilink">1972年</a>6月</p></td>
<td><p>マニュアルの序文によると、当時のインストール総数は10台。</p></td>
</tr>
<tr class="odd">
<td><p>V3</p></td>
<td><p><a href="../Page/1973年.md" title="wikilink">1973年</a>2月</p></td>
<td><p><a href="../Page/C言語.md" title="wikilink">C言語</a>と<a href="../Page/パイプ_(コンピュータ).md" title="wikilink">pipe(2)が導入された</a>。当時のインストール総数は16台。</p></td>
</tr>
<tr class="even">
<td><p>V4</p></td>
<td><p>1973年11月</p></td>
<td><p>C言語で書かれた最初のUNIX。</p></td>
</tr>
<tr class="odd">
<td><p>V5</p></td>
<td><p><a href="../Page/1974年.md" title="wikilink">1974年</a>6月</p></td>
<td><p><a href="../Page/スティッキービット.md" title="wikilink">スティッキービット</a>導入。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Version_6_Unix.md" title="wikilink">V6</a></p></td>
<td><p><a href="../Page/1975年.md" title="wikilink">1975年</a></p></td>
<td><p>ベル研究所外に広くリリースされた最初のUNIX、<a href="../Page/PDPシリーズ.md" title="wikilink">PDPシリーズ</a>以外に移植された最初のUNIX。</p></td>
</tr>
<tr class="odd">
<td><p> MINI-UNIX</p></td>
<td><p><a href="../Page/1977年.md" title="wikilink">1977年</a>5月</p></td>
<td><p>ローエンドの PDP-11/10向けの簡易版 V6</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Version_7_Unix.md" title="wikilink">V7</a></p></td>
<td><p><a href="../Page/1979年.md" title="wikilink">1979年</a></p></td>
<td><p>多くのUNIXシステムの祖先となったバージョン。外部に広くリリースされた最後のResearch Unix。</p></td>
</tr>
<tr class="odd">
<td><p> <a href="https://ja.wikipedia.org/wiki/UNIX/32V" title="wikilink">32V</a></p></td>
<td><p>1979年</p></td>
<td><p><a href="../Page/VAX.md" title="wikilink">VAX</a>ハードウェア用の最初のUNIX。</p></td>
</tr>
<tr class="even">
<td><p>V8</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1985年" title="wikilink">1985年</a></p></td>
<td><p><a href="../Page/BSD.md" title="wikilink">4.1cBSDを改造したもの</a>。<a href="../Page/ソケット_(BSD).md" title="wikilink">socketは</a><a href="../Page/STREAMS.md" title="wikilink">STREAMS</a>で置き換えられ、<a href="https://ja.wikipedia.org/wiki/procfs" title="wikilink">procfs</a>などが新たな機能として追加された。内部で使用。</p></td>
</tr>
<tr class="odd">
<td><p>V9</p></td>
<td><p><a href="../Page/1986年.md" title="wikilink">1986年</a></p></td>
<td><p>4.3BSD のコードを導入。V8のSTREAMSを強化。内部で使用。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="../Page/1989年.md" title="wikilink">1989年</a></p></td>
<td><p>最後の Research Unix。<a href="https://ja.wikipedia.org/wiki/roff" title="wikilink">troff用グラフィックス</a><a href="../Page/組版.md" title="wikilink">組版</a>ツール、<a href="../Page/C言語.md" title="wikilink">C言語</a><a href="../Page/インタプリタ.md" title="wikilink">インタプリタ</a>、後の Plan 9 に導入されたいくつかのツールが導入されている。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Plan_9_from_Bell_Labs.md" title="wikilink">Plan 9</a> First Edition</p></td>
<td><p><a href="../Page/1993年.md" title="wikilink">1993年</a></p></td>
<td><p>Research Unix の開発チームが手がけた新たなOS(ユーティリティの多くが V10 と共通)。</p></td>
</tr>
</tbody>
</table>

他の様々なUNIX([BSD](../Page/BSD.md "wikilink")や[System V](../Page/UNIX_System_V.md "wikilink"))は Research Unix から派生したものである。

[Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:1971年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1971年のソフトウェア "wikilink")