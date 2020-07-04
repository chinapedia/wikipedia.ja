> この記事は[Sunオーディオファイル](https://ja.wikipedia.org/wiki/Sunオーディオファイル)から翻訳されています。


**Sunオーディオファイル**（サン - ）別名：**Au file format**は、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が策定した[音声ファイルフォーマット](../Page/音声ファイルフォーマット.md "wikilink")。[NeXT](../Page/NeXT.md "wikilink")のシステムや初期のWebでよく使われた。当初はヘッダ部分がなく、8ビットの[μ-lawで符号化された形式で固定されていた](../Page/G.711.md "wikilink")（サンプリングレートは8000Hz）。他のベンダーのハードウェアは、ビデオクロック信号の関連でサンプリングレート 8192Hz とされていることが多かった。その後、6個の32ビットワードで構成されるヘッダ部が追加され、さらにオプション的情報格納域があって、データがあるという形式になった（[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")はビッグ）。

現在では様々な[デジタルオーディオ](../Page/デジタルオーディオ.md "wikilink")形式をサポートしているが、[μ-lawアルゴリズム](https://ja.wikipedia.org/wiki/μ-lawアルゴリズム "wikilink")による符号化が使われることが多い。これは、[SPARCstation](https://ja.wikipedia.org/wiki/SPARCstation "wikilink") 1 で採用された方式で、[SunOS](../Page/SunOS.md "wikilink") は `/dev/audio` を通してアプリケーションに符号化機能を提供していた。このため、これが[UNIX](../Page/UNIX.md "wikilink")での音声の符号化方式の[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となった。

## フォーマット

<table>
<thead>
<tr class="header">
<th><p>32ビットワード</p></th>
<th><p>フィールド</p></th>
<th><p>説明/<a href="../Page/C言語.md" title="wikilink">C言語</a>の記法でのコンテンツの<a href="../Page/十六進法.md" title="wikilink">16進表記</a> |- valign = top</p></th>
<th><p>0</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/マジックナンバー_(フォーマット識別子)" title="wikilink">マジックナンバー</a></p></th>
<th><p><code>0x2e736e64</code> という値（ASCII文字の ".snd"） |- valign = top</p></th>
<th><p>1</p></th>
<th><p>データオフセット</p></th>
<th><p>データまでのオフセット（<a href="../Page/バイト_(情報).md" title="wikilink">バイト数</a>）。最小は24（10進）。これは、ヘッダが最小の場合。 |- valign = top</p></th>
<th><p>2</p></th>
<th><p>データサイズ</p></th>
<th><p>データの大きさ（バイト数）。分からない場合は <code>0xffffffff</code> を使う。 |- valign = top</p></th>
<th><p>3</p></th>
<th><p>エンコーディング</p></th>
<th><p>データの符号化形式:</p>
<ul>
<li>1 = 8ビット G.711 μ-law</li>
<li>2 = 8ビット線形<a href="../Page/パルス符号変調.md" title="wikilink">PCM</a></li>
<li>3 = 16ビット線形<a href="../Page/パルス符号変調.md" title="wikilink">PCM</a></li>
<li>4 = 24ビット線形<a href="../Page/パルス符号変調.md" title="wikilink">PCM</a></li>
<li>5 = 32ビット線形<a href="../Page/パルス符号変調.md" title="wikilink">PCM</a></li>
<li>6 = 32ビット<a href="../Page/IEEE_754.md" title="wikilink">IEEE浮動小数点数</a></li>
<li>7 = 64ビット<a href="../Page/IEEE_754.md" title="wikilink">IEEE浮動小数点数</a></li>
<li>8 = 断片化されたサンプルデータ</li>
<li>9 = DSPプログラム</li>
<li>10 = 8ビット<a href="../Page/固定小数点数.md" title="wikilink">固定小数点数</a></li>
<li>11 = 16ビット<a href="../Page/固定小数点数.md" title="wikilink">固定小数点数</a></li>
<li>12 = 24ビット<a href="../Page/固定小数点数.md" title="wikilink">固定小数点数</a></li>
<li>13 = 32ビット<a href="../Page/固定小数点数.md" title="wikilink">固定小数点数</a></li>
<li>18 = 16ビット線形（強調あり）</li>
<li>19 = 16ビット線形（圧縮）</li>
<li>20 = 16ビット線形（強調と圧縮）</li>
<li>21 = MusicKit DSP コマンド</li>
<li>23 = 4ビット ISDN μ-law圧縮。<a href="https://ja.wikipedia.org/wiki/G.726" title="wikilink">ITU-T G.721</a> <a href="../Page/パルス符号変調.md" title="wikilink">ADPCM</a> 音声データ符号化法を使用</li>
<li>24 = <a href="https://ja.wikipedia.org/wiki/G.722" title="wikilink">ITU-T G.722</a> <a href="../Page/パルス符号変調.md" title="wikilink">ADPCM</a></li>
<li>25 = <a href="https://ja.wikipedia.org/wiki/G.723" title="wikilink">ITU-T G.723</a> 3ビット <a href="../Page/パルス符号変調.md" title="wikilink">ADPCM</a></li>
<li>26 = <a href="https://ja.wikipedia.org/wiki/G.723" title="wikilink">ITU-T G.723</a> 5ビット <a href="../Page/パルス符号変調.md" title="wikilink">ADPCM</a></li>
<li>27 = 8ビット <a href="../Page/G.711.md" title="wikilink">G.711</a> <a href="https://ja.wikipedia.org/wiki/A-lawアルゴリズム" title="wikilink">A-law</a></li>
</ul>
<p>|- valign = top</p></th>
<th><p>4</p></th>
<th><p>サンプルレート</p></th>
<th><p>秒当たりのサンプル数（例えば、8000） |- valign = top</p></th>
<th><p>5</p></th>
<th><p>チャンネル</p></th>
<th><p>インターリーブされているチャンネル数（モノラルは1、ステレオは2、さらに多くのチャンネルも可能だが、対応していないソフトが多い）</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

符号化方式は第三ワードの「エンコーディング」で指定される。2 から 7 は非圧縮の[PCMであり](../Page/パルス符号変調.md "wikilink")、[可逆圧縮](../Page/可逆圧縮.md "wikilink")である。23 から 26 はADPCMであり、[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")である（圧縮比は約4:1）。1 と 27 はそれぞれ μ-law と A-law であり、どちらも非可逆である。他には[DSPコマンドやデータもあり](../Page/デジタル信号処理.md "wikilink")、[NeXT](../Page/NeXT.md "wikilink") の MusicKit というソフトウェアで処理されるよう設計されている。

なお、PCMデータは符号付で符号化される（符号なしではない）。

## 外部リンク

  - [Sun .au sound file format](http://www.opengroup.org/public/pubs/external/auformat.html)

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")