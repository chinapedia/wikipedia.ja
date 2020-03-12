> この記事は[Plain Old Documentation](https://ja.wikipedia.org/wiki/Plain_Old_Documentation)から翻訳されています。


**Plain Old Documentation**（**POD**）は、[Perl](../Page/Perl.md "wikilink") における単純でプラットフォームに依存しない[ドキュメンテーションツールである](../Page/ソフトウェアドキュメンテーション.md "wikilink")。

## 特徴

POD は必要十分な文法を持つ単純で明快な言語として設計された。[書体](../Page/書体.md "wikilink")、[画像](../Page/画像.md "wikilink")、[色](../Page/色.md "wikilink")、[表](https://ja.wikipedia.org/wiki/表 "wikilink")などの機構を意図的に排除し、必要な機能だけを持つようにしている。その目的は以下の通りである。

  - 構文解析が簡単である。
  - 他の言語（[HTML](../Page/HyperText_Markup_Language.md "wikilink") や [TeX](../Page/TeX.md "wikilink")）への変換が簡単である。
  - サンプルコードを含めるのが簡単である。
  - フォーマッタで整形しなくても（ソースコードのままで）読むのが簡単である。
  - 書くのが簡単である。さもなくばプログラマは文書を書きたがらない。

[perlpod](http://www.perldoc.com/perl5.8.0/pod/perlpod.html) の筆者は「POD形式は本を書くのには不十分である」と書いているが、PODを拡張した書式で本が実際に書かれている。この拡張版PODには表や脚注の機能があり、[オライリーメディア](../Page/オライリーメディア.md "wikilink")から出ているいくつかのPerlに関する本で使われた。例えば、[ラリー・ウォール](../Page/ラリー・ウォール.md "wikilink")、ジョン・オーワント、トム・クリスチャンセンの *Programming Perl*（邦題は『プログラミング Perl』）が有名である。POD を若干拡張修正した版として[MOD](http://hop.perl.plover.com/book/#MOD) があり、Mark Jason Dominus による *Higher-Order Perl* で使われた。

## 利用

POD は Perl 関連での文書作成に使われている。Perl 自身、ほとんど全ての公開されている Perl モジュール、多くの[スクリプト言語](../Page/スクリプト言語.md "wikilink")、多くの設計文書、[Perl.com](http://www.perl.com/) などの Perl 関連 Webサイトにある多くの記事、[Parrot](../Page/Parrot.md "wikilink")仮想機械などで使われている。

POD形式のソースコードをそのまま読むことは少ないが、そのままでも読めるように設計されている。一般に、perldoc ツールを使って読んだり、[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")形式に変換したり、HTML形式に変換したりする。

純粋な POD ファイルの拡張子は `.pod` だが、POD は通常 Perl のソースコードに埋め込んで使われるため、拡張子は `.pl` または `.pm` であることが多い。Perl [インタプリタ](../Page/インタプリタ.md "wikilink")の[構文解析器](../Page/構文解析器.md "wikilink")はソースコード内の POD 部分を無視するよう設計されている。

## POD文書例

これは文法的に正しい POD であり、節の題名についても規約に従っている。

<table>
<thead>
<tr class="header">
<th><p>POD文書ソース</p></th>
<th><p>HTML変換結果[1]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&lt;nowiki&gt;
=head1 名前

podsample - POD文書のサンプル

=head1 概要

    $here-&gt;isa(Piece::Of::Code);
    print &lt;&lt;&quot;END&quot;;
    このインデントされたブロックはフォーマットされた
    コードか指示のため、走査されずに、スペースは保持
    されるでしょう。
    END

=head1 記述

これは標準テキストです。これはB&lt;ボールド&gt;、I&lt;イタリック&gt;、
C&lt;$リテラルコード&gt;のテキスト書式を
内部に含んでいます。

=head2 例の一覧

=over 4

=item * これは正丸リストです。

=item * ここに別口があります。

=back

=begin html

&lt;img src=&quot;Example.png&quot; align=&quot;right&quot; alt=&quot;範例&quot; /&gt;
&lt;p&gt;
    ここに、何らかの埋め込まれたHTMLがあります。
    このブロックでは、画像を入れたり、
    &lt;span style=&quot;color: green&quot;&gt;スタイル&lt;/span&gt;を
    適用するか、HTMLで記述しています。PODパーサは
    HTML出力中にそれを完全に無視することはありません。
&lt;/p&gt;

=end html

=head1 参照

L&lt;perlpod&gt;, L&lt;perldoc&gt;, L&lt;Pod::Parser&gt;.

=head1 著作権

Copyright 2005 J. Random Hacker &lt;jrh@cpan.org&gt;.

Permission is granted to copy, distribute and/or modify this
document under the terms of the GNU Free Documentation
License, Version 1.2 or any later version published by the
Free Software Foundation; with no Invariant Sections, with
no Front-Cover Texts, and with no Back-Cover Texts.

=cut
&lt;/nowiki&gt;</code></pre>
<ul>
<li>ActivePerl 5.8.8に最初からインストールされている構文解析器の<strong>pod2html</strong>では、U<アンダーライン>、C&lt;$コード&gt; には対応していません。</li>
<li>変換ツールによってHTML変換の結果は変わってきます。</li>
</ul></td>
<td><div style="overflow:auto; margin-left:0">
<p><span style="font-size:188%">名前</span><br />
</p>
<p>podsample - POD文書のサンプル</p>
<hr />
<div style="font-size:188%; padding-top: .5em; padding-bottom:.17em;">
<p>概要</p>
</div>
<p>    $here-&gt;isa(Piece::Of::Code);<br />
    print &lt;&lt;"END";<br />
    このインデントされたブロックはフォーマットされた<br />
    コードか指示のため、走査されずに、スペースは保持<br />
    されるでしょう。<br />
    END</p>
<hr />
<div style="font-size:188%; padding-top: .5em; padding-bottom:.17em;">
<p>記述</p>
</div>
<p>これは標準テキストです。これは<strong>ボールド</strong>、 <em>イタリック</em>、<code>リテラルコード</code>の テキスト書式を内部に含んでいます。</p>
<div style="font-size:150%; font-weight:bold; padding-top: .5em; padding-bottom:.17em;">
<p>例の一覧</p>
</div>
<ul>
<li><strong>これは正丸リストです。</strong></li>
<li><strong>ここに別口があります。</strong></li>
</ul>
<p><a href="https://ja.wikipedia.org/wiki/ファイル:Example.png" title="wikilink">範例</a></p>
<p><code>   ここに、何らかの埋め込まれたHTMLがあります。 </code><br />
<code>   このブロックでは、画像を入れたり、</code><br />
<code>   </code><span style="color: green"><code>スタイル</code></span><code>を</code><br />
<code>   適用するか、HTMLで記述しています。PODパーサは</code><br />
<code>   HTML出力中にそれを完全に無視することはありません。</code></p>
<hr />
<div style="font-size:188%; padding-top: .5em; padding-bottom:.17em;">
<p>参照</p>
</div>
<p><em>perlpod</em>, <em>perldoc</em>, <a href="https://ja.wikipedia.org/wiki/Plain_Old_Documentation/Pod/Parser" title="wikilink">the Pod::Parser manpage</a>.</p>
<hr />
<div style="font-size:188%; padding-top: .5em; padding-bottom:.17em;">
<p>著作権</p>
</div>
<p>Copyright 2005 J. Random Hacker &lt;<a href="mailto:jrh@cpan.org">jrh@cpan.org</a>&gt;.</p>
<p>Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.2 or any later version published by the Free Software Foundation; with no Invariant Sections, with no Front-Cover Texts, and with no Back-Cover Texts.</p>
</div></td>
</tr>
<tr class="even">
<td><pre><code>&lt;nowiki&gt;&lt;h1&gt;&lt;span id=&quot;name&quot;&gt;名前&lt;/span&gt;&lt;/h1&gt;&lt;/nowiki&gt;
&lt;nowiki&gt;&lt;p&gt;podsample - POD文書のサンプル&lt;/p&gt;&lt;/nowiki&gt;
&lt;nowiki&gt;&lt;p&gt;&lt;/nowiki&gt;
&lt;nowiki&gt;&lt;/p&gt;&lt;/nowiki&gt;
&lt;nowiki&gt;&lt;hr /&gt;&lt;/nowiki&gt;
&lt;nowiki&gt;&lt;h1&gt;&lt;span id=&quot;synopsis&quot;&gt;概要&lt;/span&gt;&lt;/h1&gt;&lt;/nowiki&gt;
&lt;nowiki&gt;&lt;pre&gt;&lt;/nowiki&gt;
&lt;nowiki&gt;    $here-&gt;isa(Piece::Of::Code);&lt;/nowiki&gt;
&lt;nowiki&gt;    print &lt;&lt;&quot;END&quot;;&lt;/nowiki&gt;
&lt;nowiki&gt;    このインデントされたブロックはフォーマットされた&lt;/nowiki&gt;
&lt;nowiki&gt;    コードか指示のため、走査されずに、スペースは保持&lt;/nowiki&gt;
&lt;nowiki&gt;    されるでしょう。&lt;/nowiki&gt;
&lt;nowiki&gt;    END</code></pre>
<p></nowiki> &lt;p&gt; &lt;/p&gt; &lt;hr /&gt; &lt;h1&gt;&lt;span id="description"&gt;記述&lt;/span&gt;&lt;/h1&gt; &lt;p&gt;これは標準テキストです。これは&lt;strong&gt;ボールド&lt;/strong&gt;、 &lt;em&gt;イタリック&lt;/em&gt;、&lt;ins&gt;アンダーライン&lt;/ins&gt;、&lt;code&gt;リテラルコード&lt;/code&gt;の テキスト書式を内部に含んでいます。&lt;/p&gt; &lt;p&gt; &lt;/p&gt; &lt;h2&gt;&lt;span id="an_example_list"&gt;例の一覧&lt;/span&gt;&lt;/h2&gt; &lt;ul&gt; &lt;li&gt;&lt;strong&gt;&lt;span id="item_this_is_a_bulleted_list_2e"&gt;これは正丸リストです。&lt;/span&gt;&lt;/strong&gt;</p>
<p>&lt;li&gt;&lt;strong&gt;&lt;span id="item_here_27s_another_item_2e"&gt;ここに別口があります。&lt;/span&gt;&lt;/strong&gt;</p>
<p>&lt;/ul&gt; [[ファイル:Example.png|範例]] &lt;p&gt; ここに、何らかの埋め込まれたHTMLがあります。 このブロックでは、画像を入れたり、 &lt;span style="color: green"&gt;スタイル&lt;/span&gt;を 適用するか、HTMLで記述しています。PODパーサは HTML出力中にそれを完全に無視することはありません。 &lt;/p&gt;&lt;p&gt; &lt;/p&gt; &lt;hr /&gt; &lt;h1&gt;&lt;span id="see_also"&gt;参照&lt;/span&gt;&lt;/h1&gt; &lt;p&gt;&lt;em&gt;perlpod&lt;/em&gt;, &lt;em&gt;perldoc&lt;/em&gt;, &lt;a href="/Pod/Parser.html"&gt;the Pod::Parser manpage&lt;/a&gt; &lt;p&gt; &lt;/p&gt; &lt;hr /&gt; &lt;h1&gt;&lt;span id="copyright"&gt;著作権&lt;/span&gt;&lt;/h1&gt; &lt;p&gt;Copyright 2005 J. Random Hacker &lt;jrh@cpan.org&gt;.&lt;/p&gt; &lt;p&gt;Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.2 or any later version published by the Free Software Foundation; with no Invariant Sections, with no Front-Cover Texts, and with no Back-Cover Texts.&lt;/p&gt;</p>
</pre></td>
<td></td>
</tr>
</tbody>
</table>

## POD における書式の詳細

PODファイルは [ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")互換の[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")（例えば [Latin-1](https://ja.wikipedia.org/wiki/Latin-1 "wikilink") や [UTF-8](../Page/UTF-8.md "wikilink")）で書かれる。POD の構文解析器はファイルの先頭から POD 形式であるとは見なさず、最初に POD の[ディレクティブ](../Page/ディレクティブ.md "wikilink")が出て来るところまでは無視する。POD のディレクティブは行の先頭に書かれ、必ず先頭に等号(=)がつく。構文解析器はその後の行がPOD形式であると見なし、"=cut" ディレクティブが先頭にある行までをPOD形式として[解釈](../Page/解釈.md "wikilink")する。その後、再び別のPODディレクティブが出現するまでは無視する。このため、実行可能なコードを解釈するインタプリタが POD 形式部分を無視するなら、POD 形式と実行可能コードを混在させることができる。

POD の内容は空行で段落分けされる。段落の先頭に空白文字（スペースやタブ）がある場合、その段落は "verbatim paragraphs" として解釈され、中身を整形しない。これはサンプルコードや[アスキーアート](../Page/アスキーアート.md "wikilink")に使われる。等号記号で始まる段落は "command paragraphs" である。等号の直後に続く文字列が POD ディレクティブとして解釈され、残りの部分はディレクティブに従って整形される。ディレクティブによってはその後の段落にも影響を与える。等号や空白以外で始まる段落は "ordinary paragraphs" として[解釈](../Page/解釈.md "wikilink")される。

ordinary paragraphs や command paragraphs の中身の構文解析では書式に従って整形が行われる。POD による書式指定は非常に単純である。ボールド、イタリック、アンダーライン、等幅といった書式しかない。また、同一文書内の別の節や他のPOD文書へのリンクも可能である。書式符号には以下の形式がある。

  - 1文字の大文字の後に不等号(\<)が続き、その後に整形すべき内容、さらにその後に不等号(\>)が続く。例えば、`B`<bolded text> となる。
  - 1文字の大文字の後に2つ以上の不等号(\<\<)が続き、その後に整形すべき内容、さらにその後に同じ個数の不等号(\>\>)が続く。例えば、`B<< bolded text >>` となる。これは内容に不等号が含まれる場合に使われる。

POD 内のコマンド（ディレクティブ）には、4段階の節、番号なしと番号つきのリスト、他の言語の節などがある。他の言語の節は、その言語を解釈する構文解析器による特殊な整形を可能にする。

## 参考文献

  - Wall, Larry; Christiansen, Tom; & Orwant, Jon (2000). *Programming Perl* (3rd ed.). Sebastopol: O'Reilly & Associates. ISBN 0-12-345678-9.

## 脚注

<references />

## 関連項目

  - [Perl](../Page/Perl.md "wikilink")
  - [ラリー・ウォール](../Page/ラリー・ウォール.md "wikilink")
  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")
      - [データ記述言語](../Page/データ記述言語.md "wikilink")
          - [マークアップ言語](../Page/マークアップ言語.md "wikilink")
              - [軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink")

## 外部リンク

  - [Perlの小技](http://homepage3.nifty.com/hippo2000/perltips/)
      - \[<http://homepage3.nifty.com/hippo2000/perltips/podread.htm#2>. Perlドキュメントの読み方\]
  - [氷魚.jp](http://hio.jp/)
      - [perlpod](http://hio.jp/tips/perl/perldoc-5.8.0-old/pod/perlpod.html) - <span style="font-size:90%;">Perlに標準インストールされているPODの書き方マニュアル（和訳）</span>
      - [pod2html](http://hio.jp/tips/perl/perldoc-5.8.0-old/pod/pod2html.html) - <span style="font-size:90%;">POD→HTMLに変換するツールのマニュアル（和訳）</span>
      - [index of /Pod](http://hio.jp/tips/perl/perldoc-5.8.0/lib/Pod/) - <span style="font-size:90%;">Perlに標準搭載されているPOD関連のモジュールマニュアル。Pod::××なので該当する配下モジュールをクリック。(Pod::)Htmlなどを参照。（和訳）</span>
  - [The CPAN search site](http://search.cpan.org/) - <span style="font-size:90%;">Perlで一番信頼のおけるモジュール配布サイト。 (英語)</span>
      - [perlpod](http://search.cpan.org/~nwclark/perl-5.8.8/pod/perlpod.pod) - <span style="font-size:90%;">POD形式の<span style="text-decoration:underline;">文書</span>を書く人向けの説明。</span>
      - [perlpodspec](http://search.cpan.org/~nwclark/perl-5.8.8/pod/perlpodspec.pod) - <span style="font-size:90%;">POD形式の<span style="text-decoration:underline;">構文解析器</span>を書く人向けの説明。</span>
      - [pod2html](http://search.cpan.org/~rgarcia/perl-5.10.0/pod/pod2html.PL) - <span style="font-size:90%;">POD→HTMLに変換するツールのマニュアル</span>
      - [Pod::Html](http://search.cpan.org/~dland/Pod-Html-1.09_01/Html.pm) - <span style="font-size:90%;">POD→HTMLに変換する標準モジュールのマニュアル</span>
      - [Getopt::Euclid module](http://search.cpan.org/perldoc?Getopt%3A%3AEuclid) - <span style="font-size:90%;">入力を POD タグに基づいて自動的に構文解析する。</span>
      - [Index of /src/NWCLARK/perl-5.8.8/pod/](http://search.cpan.org/src/NWCLARK/perl-5.8.8/pod/) - <span style="font-size:90%;">Perl のマニュアルページの解釈前のPOD形式を公開。</span>
      - [Index of /src/NWCLARK/perl-5.8.7/lib/](http://search.cpan.org/src/NWCLARK/perl-5.8.7/lib/) - <span style="font-size:90%;">ディレクトリにPOD書式が埋め込まれたモジュールが多数存在する。</span>

[Category:Perl](https://ja.wikipedia.org/wiki/Category:Perl "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink")

1.  上段はHTML表示イメージ（ウィキペディアに適した形に修正しています）、下段はHTMLソース。実際には、ヘッダタグ、節の目次リスト（デフォルト）、フッタタグも出力される。