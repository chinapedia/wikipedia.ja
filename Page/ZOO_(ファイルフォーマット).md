> この記事は[ZOO \(\)](https://ja.wikipedia.org/wiki/ZOO_\(\))から翻訳されています。


**ZOO**は、Rahul Deshiが1980年代半ばに開発した[データ圧縮](../Page/データ圧縮.md "wikilink")[プログラムおよび](../Page/プログラム_\(コンピュータ\).md "wikilink")[フォーマットである](../Page/ファイルフォーマット.md "wikilink")。[LZW圧縮アルゴリズムを元にしたフォーマットであり](../Page/Lempel–Ziv–Welch.md "wikilink")、.zooの拡張子が使用されている。ZOOは現状ではほとんど使用されることはない。

プログラムソースコードは[Usenet](https://ja.wikipedia.org/wiki/Usenet "wikilink")の comp.sources.miscニュースグループで最初に公開され、多くの[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")OSで動作した。[実行形式は](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")、[MS-DOS](../Page/MS-DOS.md "wikilink")ユーザ・コミュニティにも公開された。解凍の機能だけを提供する**booz**という名前の補助的なプログラムも開発された。

ZOOファイルフォーマットは、[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")(現在の[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink"))の[VAX](https://ja.wikipedia.org/wiki/VAX "wikilink")コンピュータで動作する[OpenVMS](https://ja.wikipedia.org/wiki/OpenVMS "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")でよく使用された。[コモドール](https://ja.wikipedia.org/wiki/コモドール "wikilink")の[Amiga](../Page/Amiga.md "wikilink")のコミュニティでも、ある期間使用された。

## 技術的仕様

<table>
<caption>.zoo アーカイブは、以下のような34バイトのヘッダで始まる。</caption>
<thead>
<tr class="header">
<th><p>オフセット<br />
10進数</p></th>
<th><p>オフセット<br />
16進数</p></th>
<th><p>サイズ<br />
(バイト)</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>000-019</p></td>
<td><p>000-013</p></td>
<td><center>
<p>20</p>
</center></td>
<td><p>アーカイブヘッダ文字列、NULL詰め、^Zで終端</p></td>
</tr>
<tr class="even">
<td><p>020-023</p></td>
<td><p>014-017</p></td>
<td><center>
<p>4</p>
</center></td>
<td><p>16進数 A7DCFDC4</p></td>
</tr>
<tr class="odd">
<td><p>024-027</p></td>
<td><p>018-01B</p></td>
<td><center>
<p>4</p>
</center></td>
<td><p>アーカイブ中の最初のファイルオフセット</p></td>
</tr>
<tr class="even">
<td><p>028-031</p></td>
<td><p>01C-019</p></td>
<td><center>
<p>4</p>
</center></td>
<td><p>アーカイブ中の最初のファイルオフセット - 1</p></td>
</tr>
<tr class="odd">
<td><p>032</p></td>
<td><p>020</p></td>
<td><center>
<p>1</p>
</center></td>
<td><p>このアーカイブを作成したZOOのバージョン</p></td>
</tr>
<tr class="even">
<td><p>033</p></td>
<td><p>021</p></td>
<td><center>
<p>1</p>
</center></td>
<td><p>このアーカイブからファイルを取り出すのに必要な、(最低の)ZOOのバージョン</p></td>
</tr>
</tbody>
</table>

<table>
<caption>格納されているそれぞれのファイルは、以下のようなヘッダを持つ。</caption>
<thead>
<tr class="header">
<th><p>オフセット<br />
10進数</p></th>
<th><p>オフセット<br />
16進数</p></th>
<th><p>サイズ<br />
(バイト)</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>000-003</p></td>
<td><p>000-003</p></td>
<td><center>
<p>4</p>
</center></td>
<td><p>16進数 A7DCFDC4</p></td>
</tr>
<tr class="even">
<td><p>004</p></td>
<td><p>004</p></td>
<td><center>
<p>1</p>
</center></td>
<td><p>ディレクトリエントリの形式</p></td>
</tr>
<tr class="odd">
<td><p>005</p></td>
<td><p>005</p></td>
<td><center>
<p>1</p>
</center></td>
<td><p>圧縮形式; 0 - 非圧縮格納; 1 - 圧縮 (LZW)</p></td>
</tr>
<tr class="even">
<td><p>006-009</p></td>
<td><p>006-009</p></td>
<td><center>
<p>4</p>
</center></td>
<td><p>次のディレクトリエントリへのオフセット</p></td>
</tr>
<tr class="odd">
<td><p>010-013</p></td>
<td><p>00A-00C</p></td>
<td><center>
<p>4</p>
</center></td>
<td><p>次のヘッダへのオフセット</p></td>
</tr>
<tr class="even">
<td><p>014-016</p></td>
<td><p>00D-011</p></td>
<td><center>
<p>2</p>
</center></td>
<td><p>オリジナルファイルの作成日時</p></td>
</tr>
<tr class="odd">
<td><p>017-018</p></td>
<td><p>012-013</p></td>
<td><center>
<p>2</p>
</center></td>
<td><p>ファイルのCRC-16値</p></td>
</tr>
<tr class="even">
<td><p>019-022</p></td>
<td><p>014-017</p></td>
<td><center>
<p>4</p>
</center></td>
<td><p>非圧縮でのファイルサイズ</p></td>
</tr>
<tr class="odd">
<td><p>023-026</p></td>
<td><p>018-01B</p></td>
<td><center>
<p>4</p>
</center></td>
<td><p>圧縮後のファイルサイズ</p></td>
</tr>
<tr class="even">
<td><p>027</p></td>
<td><p>01C</p></td>
<td><center>
<p>1</p>
</center></td>
<td><p>このファイルを圧縮したZOOのバージョン</p></td>
</tr>
<tr class="odd">
<td><p>028</p></td>
<td><p>01D</p></td>
<td><center>
<p>1</p>
</center></td>
<td><p>このファイルを解凍するのに必要な（最低の）ZOOのバージョン</p></td>
</tr>
<tr class="even">
<td><p>029</p></td>
<td><p>01E</p></td>
<td><center>
<p>1</p>
</center></td>
<td><p>削除フラグ: 0-ファイルは存在する; 1-ファイルが削除されたことのしるし</p></td>
</tr>
<tr class="odd">
<td><p>030</p></td>
<td><p>01F-022</p></td>
<td><center>
<p>4</p>
</center></td>
<td><p>ファイルコメントへのオフセット。0の場合はコメント無し。</p></td>
</tr>
<tr class="even">
<td><p>031-032</p></td>
<td><p>023-024</p></td>
<td><center>
<p>2</p>
</center></td>
<td><p>コメントフィールドの長さ</p></td>
</tr>
<tr class="odd">
<td><p>033+</p></td>
<td><p>025+</p></td>
<td><p>可変</p></td>
<td><p>ファイル名。パス名を含むこともある。NULLで終端</p></td>
</tr>
</tbody>
</table>

## 他での拡張子の利用

ファイル拡張子の**.zoo**は[マイクロソフト](../Page/マイクロソフト.md "wikilink")のゲームである、[ズー タイクーンの保存データとしても使用される](https://ja.wikipedia.org/wiki/ズー_タイクーン "wikilink")。

## 外部リンク

  - [zoo 2.10 source](http://www.ibiblio.org/pub/Linux/utils/compress/zoo-2.10-3.src.rpm)
  - [unzoo](http://archives.math.utk.edu/software/multi-platform/gap/util/) - ZOOアーカイブ解凍ツール。ソース付き。

[Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink")