> この記事は[BBコード](https://ja.wikipedia.org/wiki/BBコード)から翻訳されています。


**BBコード**（びーびーこーど）は、 *Bulletin Board Code* の略で、[電子掲示板](../Page/電子掲示板.md "wikilink")や[ブログ](../Page/ブログ.md "wikilink")などで使用される[軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink")である。 キーワードを[角括弧](https://ja.wikipedia.org/wiki/角括弧 "wikilink")で囲んでタグとし、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")が理解して表示できるように[構文解析](../Page/構文解析.md "wikilink")して[HTML](../Page/HyperText_Markup_Language.md "wikilink")（[XHTML](https://ja.wikipedia.org/wiki/XHTML "wikilink")）に変換される。

## 目的と経緯

BBコードを初めて実装したのは1998年にリリースされた電子掲示板ソフトウェアの UBB (Ultimate Bulletin Board) v3 である。インターネットが普及し始めた頃の電子掲示板は書き込む内容に[HTMLや](../Page/HyperText_Markup_Language.md "wikilink")[JavaScript](../Page/JavaScript.md "wikilink")の使用が許容されていたため、不慣れな書き方による表示の破壊やそれを目的とした[荒らし](https://ja.wikipedia.org/wiki/荒らし "wikilink")の手段となっていた。これに対し、ユーザーが文書内容を整形する手段を限定させ、しかも容易に安全に行えるように考案されたのがBBコードである。文書のマークアップをBBコード限定で許可することで、インターネット・フォーラムでの表示破壊は見られなくなった。

その後BBコードは広く普及して、[phpBB](https://ja.wikipedia.org/wiki/phpBB "wikilink")やvBulletinなどの多くのソフトウェアで使用されるようになった。しかし定められた仕様が存在しないため、同じBBコードでありながら互換性がないものが存在する。

## BBコード タグ

以下は標準的なBBコードの一覧。ソフトウェアによってより多くのタグを実装する場合や、それぞれ細かい仕様や動作が異なる場合がある。

<table>
<thead>
<tr class="header">
<th><p>BBコード</p></th>
<th><p>XHTML</p></th>
<th><p>表示例</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="bbcode"><code>[b]太字 text[/b]</code></pre></td>
<td><div class="sourceCode" id="cb2"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb2-1"><a href="#cb2-1"></a><span class="kw">&lt;span</span><span class="ot"> style=</span><span class="st">&quot;font-weight: bold&quot;</span><span class="kw">&gt;</span>太字 text<span class="kw">&lt;/span&gt;</span></span></code></pre></div></td>
<td><p><span style="font-weight: bold">太字 text</span></p></td>
</tr>
<tr class="even">
<td><pre class="bbcode"><code>[i]斜体 text[/i]</code></pre></td>
<td><div class="sourceCode" id="cb4"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb4-1"><a href="#cb4-1"></a><span class="kw">&lt;span</span><span class="ot"> style=</span><span class="st">&quot;font-style: italic&quot;</span><span class="kw">&gt;</span>斜体 text<span class="kw">&lt;/span&gt;</span></span></code></pre></div></td>
<td><p><span style="font-style: italic">斜体 text</span></p></td>
</tr>
<tr class="odd">
<td><pre class="bbcode"><code>[u]下線付き text[/u]</code></pre></td>
<td><div class="sourceCode" id="cb6"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb6-1"><a href="#cb6-1"></a><span class="kw">&lt;span</span><span class="ot"> style=</span><span class="st">&quot;text-decoration: underline&quot;</span><span class="kw">&gt;</span>下線付き text<span class="kw">&lt;/span&gt;</span></span></code></pre></div></td>
<td><p><span style="text-decoration: underline">下線付き text</span></p></td>
</tr>
<tr class="even">
<td><pre class="bbcode"><code>[size=18]サイズ text[/size]</code></pre></td>
<td><div class="sourceCode" id="cb8"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb8-1"><a href="#cb8-1"></a><span class="kw">&lt;span</span><span class="ot"> style=</span><span class="st">&quot;font-size: 18px&quot;</span><span class="kw">&gt;</span>サイズ text<span class="kw">&lt;/span&gt;</span></span></code></pre></div></td>
<td><p><span style="font-size:18px">サイズ text</span></p></td>
</tr>
<tr class="odd">
<td><pre class="bbcode"><code>[color=red]赤色 text[/color]</code></pre>
<p>または</p>
<pre class="bbcode"><code>[color=#FF0000]赤色 text[/color]</code></pre></td>
<td><div class="sourceCode" id="cb11"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb11-1"><a href="#cb11-1"></a><span class="kw">&lt;span</span><span class="ot"> style=</span><span class="st">&quot;color: #FF0000&quot;</span><span class="kw">&gt;</span>赤色 text<span class="kw">&lt;/span&gt;</span></span></code></pre></div></td>
<td><p><span style="color: #FF0000">赤色 text</span></p></td>
</tr>
<tr class="even">
<td><pre class="bbcode"><code>以下は引用。
[quote]引用 text[/quote]</code></pre></td>
<td><div class="sourceCode" id="cb13"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb13-1"><a href="#cb13-1"></a><span class="kw">&lt;p&gt;</span>以下は引用。<span class="kw">&lt;/p&gt;&lt;blockquote&gt;&lt;p&gt;</span>引用 text<span class="kw">&lt;/p&gt;&lt;/blockquote&gt;</span></span></code></pre></div></td>
<td><p>以下は引用。</p>
<blockquote>
<p>引用 text</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><pre class="bbcode"><code>[code]整形済み code[/code]</code></pre></td>
<td><div class="sourceCode" id="cb15"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb15-1"><a href="#cb15-1"></a><span class="kw">&lt;pre&gt;</span>整形済み code<span class="kw">&lt;/pre&gt;</span></span></code></pre></div></td>
<td><pre><code>整形済み code</code></pre></td>
</tr>
<tr class="even">
<td><pre class="bbcode"><code>[list]
[*]順序なし list 1
[*]順序なし list 2
[*]順序なし list 3
[/list]</code></pre></td>
<td><div class="sourceCode" id="cb18"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb18-1"><a href="#cb18-1"></a><span class="kw">&lt;ul&gt;</span></span>
<span id="cb18-2"><a href="#cb18-2"></a><span class="kw">&lt;li&gt;</span>順序なし list 1<span class="kw">&lt;/li&gt;</span></span>
<span id="cb18-3"><a href="#cb18-3"></a><span class="kw">&lt;li&gt;</span>順序なし list 2<span class="kw">&lt;/li&gt;</span></span>
<span id="cb18-4"><a href="#cb18-4"></a><span class="kw">&lt;li&gt;</span>順序なし list 3<span class="kw">&lt;/li&gt;</span></span>
<span id="cb18-5"><a href="#cb18-5"></a><span class="kw">&lt;/ul&gt;</span></span></code></pre></div></td>
<td><ul>
<li>順序なし list 1</li>
<li>順序なし list 2</li>
<li>順序なし list 3</li>
</ul></td>
</tr>
<tr class="odd">
<td><pre class="bbcode"><code>[list=1]
[*]順序あり list 1
[*]順序あり list 2
[*]順序あり list 3
[/list]</code></pre></td>
<td><div class="sourceCode" id="cb20"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb20-1"><a href="#cb20-1"></a><span class="kw">&lt;ol&gt;</span></span>
<span id="cb20-2"><a href="#cb20-2"></a><span class="kw">&lt;li&gt;</span>順序あり list 1<span class="kw">&lt;/li&gt;</span></span>
<span id="cb20-3"><a href="#cb20-3"></a><span class="kw">&lt;li&gt;</span>順序あり list 2<span class="kw">&lt;/li&gt;</span></span>
<span id="cb20-4"><a href="#cb20-4"></a><span class="kw">&lt;li&gt;</span>順序あり list 3<span class="kw">&lt;/li&gt;</span></span>
<span id="cb20-5"><a href="#cb20-5"></a><span class="kw">&lt;/ol&gt;</span></span></code></pre></div></td>
<td><ol>
<li>順序あり list 1</li>
<li>順序あり list 2</li>
<li>順序あり list 3</li>
</ol></td>
</tr>
<tr class="even">
<td><pre class="bbcode"><code>:-)</code></pre>
<p>または</p>
<pre class="bbcode"><code>:smile:</code></pre></td>
<td><div class="sourceCode" id="cb23"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb23-1"><a href="#cb23-1"></a><span class="kw">&lt;img</span><span class="ot"> src=</span><span class="st">&quot;Smile.svg&quot;</span><span class="ot"> alt=</span><span class="st">&quot;smile&quot;</span> <span class="kw">/&gt;</span></span></code></pre></div></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ファイル:Smile.svg" title="wikilink">smile</a></p></td>
</tr>
<tr class="odd">
<td><pre class="bbcode"><code>[url]http://www.wikipedia.org/[/url]</code></pre></td>
<td><div class="sourceCode" id="cb25"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb25-1"><a href="#cb25-1"></a><span class="kw">&lt;a</span><span class="ot"> href=</span><span class="st">&quot;http://www.wikipedia.org/&quot;</span><span class="kw">&gt;</span>http://www.wikipedia.org/<span class="kw">&lt;/a&gt;</span></span></code></pre></div></td>
<td><p><span class="plainlinks"><a href="http://www.wikipedia.org/"><a href="http://www.wikipedia.org/">http://www.wikipedia.org/</a></a></span></p></td>
</tr>
<tr class="even">
<td><pre class="bbcode"><code>[url=http://www.wikipedia.org/]Wikipedia[/url]</code></pre></td>
<td><div class="sourceCode" id="cb27"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb27-1"><a href="#cb27-1"></a><span class="kw">&lt;a</span><span class="ot"> href=</span><span class="st">&quot;http://www.wikipedia.org/&quot;</span><span class="kw">&gt;</span>Wikipedia<span class="kw">&lt;/a&gt;</span></span></code></pre></div></td>
<td><p><span class="plainlinks"><a href="http://www.wikipedia.org/">Wikipedia</a></span></p></td>
</tr>
<tr class="odd">
<td><pre class="bbcode"><code>[img]http://upload.wikimedia.org/wikipedia/commons/6/6c/Bouncywikilogo.gif[/img]</code></pre></td>
<td><div class="sourceCode" id="cb29"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb29-1"><a href="#cb29-1"></a><span class="kw">&lt;img</span><span class="ot"> src=</span><span class="st">&quot;http://upload.wikimedia.org/wikipedia/commons/6/6c/Bouncywikilogo.gif&quot;</span> <span class="kw">/&gt;</span></span></code></pre></div></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ファイル:Bouncywikilogo.gif" title="wikilink">ファイル:Bouncywikilogo.gif</a></p></td>
</tr>
</tbody>
</table>

## 関連項目

  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")
      - [データ記述言語](../Page/データ記述言語.md "wikilink")
          - [マークアップ言語](../Page/マークアップ言語.md "wikilink")
              - [軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink")

[Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:コンピュータ言語](https://ja.wikipedia.org/wiki/Category:コンピュータ言語 "wikilink")