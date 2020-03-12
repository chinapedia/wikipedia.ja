> この記事は[XSL Transformations](https://ja.wikipedia.org/wiki/XSL_Transformations)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:XML_languages.svg "wikilink")

**XSL変換**（）は、[W3Cにより標準化された](../Page/World_Wide_Web_Consortium.md "wikilink")[XML文書の](../Page/Extensible_Markup_Language.md "wikilink")[変換用言語である](https://ja.wikipedia.org/wiki/変換言語 "wikilink")。3つの仕様から成る[XSLのうちの](../Page/Extensible_Stylesheet_Language.md "wikilink")、ひとつの仕様である。XSLT の仕様は[ジェームズ・クラークを中心とした人々が設計した](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")。XSLT と XSL-FO は[DSSSLをもとにして設計された](../Page/Document_Style_Semantics_and_Specification_Language.md "wikilink")。

XSLT 1.0 は1999年11月23日に[W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")となり、2007年には JIS X 4169 として[JIS規格へ翻訳された](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")。XSLT 2.0 は2007年1月23日に、3.0は2017年6月8日に[W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")となった。

XSLTはXML形式の文書を変換する。 による選択と検索にもとづき、XML文書全体または文書の一部に対して変換を行い、XML として出力する他、XML（整形式）ではないその他任意のテキスト形式としても出力できる。

例としては次のような応用がある。

  - 一定フォーマットのHTML用の、文書型宣言・ヘッダ情報の追加
  - テキストの移動
  - テキストのソート

変換の指定は[関数型言語](../Page/関数型言語.md "wikilink")として見ることもでき、実のところ[チューリング完全](../Page/チューリング完全.md "wikilink")であるため、コンピュータ・プログラムを書くようにしてどんな応用も可能である。裏返せば、その機能を十分に発揮させるためには利用者に通常のプログラミングと同様の能力と作業が必要であり、しばしばXMLに対して持たれている「プログラミングが不要」という期待を裏切るものではある。

変換の対象となるXML文書は[木構造であり](../Page/木構造_\(データ構造\).md "wikilink")、XSLTによる変換は宣言的に指定される。つまり、XSLTプログラムは、変換をどう行うべきか指定する**規則**をいくつか集めたものからなり、この規則を再帰的に適用することによって変換を行う。

XSLT処理系はまずどの規則が適用できるかチェックし、優先順にもとづいて該当する変換を行う。

XSLTプログラムは、以下のようにXML文書の形式をとる。

``` xslt
<?xml version="1.0" ?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
 ...
</xsl:stylesheet>
```

## データ変換

XML 形式のデータを様々な形式のデータに変換できる。ここではその例を示す。

変換前のXML

``` xml
<?xml version="1.0" ?>
<persons>
  <person username="JS1">
    <name>John</name>
    <family-name>Smith</family-name>
  </person>
  <person username="MI1">
    <name>Morka</name>
    <family-name>Ismincius</family-name>
  </person>
</persons>
```

<table>
<thead>
<tr class="header">
<th><p>変換後の形式</p></th>
<th><p>XSLTコード</p></th>
<th><p>変換結果</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>XML</p></td>
<td><div class="sourceCode" id="cb1"><pre class="sourceCode xslt"><code class="sourceCode xslt"><span id="cb1-1"><a href="#cb1-1"></a><span class="kw">&lt;?xml</span> version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;<span class="kw">?&gt;</span></span>
<span id="cb1-2"><a href="#cb1-2"></a><span class="kw">&lt;xsl:stylesheet</span><span class="ot"> xmlns:xsl=</span><span class="st">&quot;http://www.w3.org/1999/XSL/Transform&quot;</span><span class="ot"> version=</span><span class="st">&quot;1.0&quot;</span><span class="kw">&gt;</span></span>
<span id="cb1-3"><a href="#cb1-3"></a>  <span class="kw">&lt;xsl:output</span><span class="ot"> method=</span><span class="st">&quot;xml&quot;</span><span class="ot"> indent=</span><span class="st">&quot;yes&quot;</span><span class="kw">/&gt;</span></span>
<span id="cb1-4"><a href="#cb1-4"></a></span>
<span id="cb1-5"><a href="#cb1-5"></a>  <span class="kw">&lt;xsl:template</span><span class="ot"> match=&quot;/persons&quot;</span><span class="kw">&gt;</span></span>
<span id="cb1-6"><a href="#cb1-6"></a>    <span class="kw">&lt;root&gt;</span></span>
<span id="cb1-7"><a href="#cb1-7"></a>      <span class="kw">&lt;xsl:apply-templates</span><span class="ot"> select=&quot;person&quot;</span><span class="kw">/&gt;</span></span>
<span id="cb1-8"><a href="#cb1-8"></a>    <span class="kw">&lt;/root&gt;</span></span>
<span id="cb1-9"><a href="#cb1-9"></a>  <span class="kw">&lt;/xsl:template&gt;</span></span>
<span id="cb1-10"><a href="#cb1-10"></a></span>
<span id="cb1-11"><a href="#cb1-11"></a>  <span class="kw">&lt;xsl:template</span><span class="ot"> match=&quot;person&quot;</span><span class="kw">&gt;</span></span>
<span id="cb1-12"><a href="#cb1-12"></a>    <span class="kw">&lt;name</span><span class="ot"> username</span>=<span class="st">&quot;</span><span class="ot">{</span>@username<span class="ot">}</span><span class="st">&quot;</span><span class="kw">&gt;</span></span>
<span id="cb1-13"><a href="#cb1-13"></a>      <span class="kw">&lt;xsl:value-of</span><span class="ot"> select=&quot;</span><span class="kw">name</span><span class="ot">&quot; </span><span class="kw">/&gt;</span></span>
<span id="cb1-14"><a href="#cb1-14"></a>    <span class="kw">&lt;/name&gt;</span></span>
<span id="cb1-15"><a href="#cb1-15"></a>  <span class="kw">&lt;/xsl:template&gt;</span></span>
<span id="cb1-16"><a href="#cb1-16"></a></span>
<span id="cb1-17"><a href="#cb1-17"></a><span class="kw">&lt;/xsl:stylesheet&gt;</span></span></code></pre></div></td>
<td><div class="sourceCode" id="cb2"><pre class="sourceCode xml"><code class="sourceCode xml"><span id="cb2-1"><a href="#cb2-1"></a><span class="kw">&lt;?xml</span> version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;<span class="kw">?&gt;</span></span>
<span id="cb2-2"><a href="#cb2-2"></a><span class="kw">&lt;root&gt;</span></span>
<span id="cb2-3"><a href="#cb2-3"></a>  <span class="kw">&lt;name</span><span class="ot"> username=</span><span class="st">&quot;JS1&quot;</span><span class="kw">&gt;</span>John<span class="kw">&lt;/name&gt;</span></span>
<span id="cb2-4"><a href="#cb2-4"></a>  <span class="kw">&lt;name</span><span class="ot"> username=</span><span class="st">&quot;MI1&quot;</span><span class="kw">&gt;</span>Morka<span class="kw">&lt;/name&gt;</span></span>
<span id="cb2-5"><a href="#cb2-5"></a><span class="kw">&lt;/root&gt;</span></span></code></pre></div></td>
</tr>
<tr class="even">
<td><p>XHTML</p></td>
<td><div class="sourceCode" id="cb3"><pre class="sourceCode xslt"><code class="sourceCode xslt"><span id="cb3-1"><a href="#cb3-1"></a><span class="kw">&lt;?xml</span> version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;<span class="kw">?&gt;</span></span>
<span id="cb3-2"><a href="#cb3-2"></a><span class="kw">&lt;xsl:stylesheet</span></span>
<span id="cb3-3"><a href="#cb3-3"></a><span class="ot">  version=</span><span class="st">&quot;1.0&quot;</span></span>
<span id="cb3-4"><a href="#cb3-4"></a><span class="ot">  xmlns:xsl=</span><span class="st">&quot;http://www.w3.org/1999/XSL/Transform&quot;</span></span>
<span id="cb3-5"><a href="#cb3-5"></a><span class="ot">  ns=</span><span class="st">&quot;http://www.w3.org/1999/xhtml&quot;</span><span class="kw">&gt;</span></span>
<span id="cb3-6"><a href="#cb3-6"></a></span>
<span id="cb3-7"><a href="#cb3-7"></a>  <span class="kw">&lt;xsl:output</span><span class="ot"> method=</span><span class="st">&quot;xml&quot;</span><span class="ot"> indent=</span><span class="st">&quot;yes&quot;</span><span class="ot"> encoding=</span><span class="st">&quot;UTF-8&quot;</span><span class="kw">/&gt;</span></span>
<span id="cb3-8"><a href="#cb3-8"></a></span>
<span id="cb3-9"><a href="#cb3-9"></a>  <span class="kw">&lt;xsl:template</span><span class="ot"> match=&quot;/persons&quot;</span><span class="kw">&gt;</span></span>
<span id="cb3-10"><a href="#cb3-10"></a>    <span class="kw">&lt;html&gt;</span></span>
<span id="cb3-11"><a href="#cb3-11"></a>      <span class="kw">&lt;head&gt;</span> <span class="kw">&lt;title&gt;</span>Testing XML Example<span class="kw">&lt;/title&gt;</span> <span class="kw">&lt;/head&gt;</span></span>
<span id="cb3-12"><a href="#cb3-12"></a>      <span class="kw">&lt;body&gt;</span></span>
<span id="cb3-13"><a href="#cb3-13"></a>        <span class="kw">&lt;h1&gt;</span>Persons<span class="kw">&lt;/h1&gt;</span></span>
<span id="cb3-14"><a href="#cb3-14"></a>        <span class="kw">&lt;ul&gt;</span></span>
<span id="cb3-15"><a href="#cb3-15"></a>          <span class="kw">&lt;xsl:apply-templates</span><span class="ot"> select=&quot;person&quot;</span><span class="kw">&gt;</span></span>
<span id="cb3-16"><a href="#cb3-16"></a>            <span class="kw">&lt;xsl:sort</span><span class="ot"> select=&quot;family-name&quot; </span><span class="kw">/&gt;</span></span>
<span id="cb3-17"><a href="#cb3-17"></a>          <span class="kw">&lt;/xsl:apply-templates&gt;</span></span>
<span id="cb3-18"><a href="#cb3-18"></a>        <span class="kw">&lt;/ul&gt;</span></span>
<span id="cb3-19"><a href="#cb3-19"></a>      <span class="kw">&lt;/body&gt;</span></span>
<span id="cb3-20"><a href="#cb3-20"></a>    <span class="kw">&lt;/html&gt;</span></span>
<span id="cb3-21"><a href="#cb3-21"></a>  <span class="kw">&lt;/xsl:template&gt;</span></span>
<span id="cb3-22"><a href="#cb3-22"></a></span>
<span id="cb3-23"><a href="#cb3-23"></a>  <span class="kw">&lt;xsl:template</span><span class="ot"> match=&quot;person&quot;</span><span class="kw">&gt;</span></span>
<span id="cb3-24"><a href="#cb3-24"></a>    <span class="kw">&lt;li&gt;</span></span>
<span id="cb3-25"><a href="#cb3-25"></a>      <span class="kw">&lt;xsl:value-of</span><span class="ot"> select=&quot;family-name&quot;</span><span class="kw">/&gt;&lt;xsl:text&gt;</span>, <span class="kw">&lt;/xsl:text&gt;&lt;xsl:value-of</span><span class="ot"> select=&quot;</span><span class="kw">name</span><span class="ot">&quot;</span><span class="kw">/&gt;</span></span>
<span id="cb3-26"><a href="#cb3-26"></a>    <span class="kw">&lt;/li&gt;</span></span>
<span id="cb3-27"><a href="#cb3-27"></a>  <span class="kw">&lt;/xsl:template&gt;</span></span>
<span id="cb3-28"><a href="#cb3-28"></a></span>
<span id="cb3-29"><a href="#cb3-29"></a><span class="kw">&lt;/xsl:stylesheet&gt;</span></span></code></pre></div></td>
<td><div class="sourceCode" id="cb4"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb4-1"><a href="#cb4-1"></a><span class="kw">&lt;?xml</span> version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;<span class="kw">?&gt;</span></span>
<span id="cb4-2"><a href="#cb4-2"></a><span class="kw">&lt;html</span><span class="ot"> ns=</span><span class="st">&quot;http://www.w3.org/1999/xhtml&quot;</span><span class="kw">&gt;</span></span>
<span id="cb4-3"><a href="#cb4-3"></a>  <span class="kw">&lt;head&gt;</span> <span class="kw">&lt;title&gt;</span>Testing XML Example<span class="kw">&lt;/title&gt;</span> <span class="kw">&lt;/head&gt;</span></span>
<span id="cb4-4"><a href="#cb4-4"></a>  <span class="kw">&lt;body&gt;</span></span>
<span id="cb4-5"><a href="#cb4-5"></a>    <span class="kw">&lt;h1&gt;</span>Persons<span class="kw">&lt;/h1&gt;</span></span>
<span id="cb4-6"><a href="#cb4-6"></a>      <span class="kw">&lt;ul&gt;</span></span>
<span id="cb4-7"><a href="#cb4-7"></a>        <span class="kw">&lt;li&gt;</span>Ismincius, Morka<span class="kw">&lt;/li&gt;</span></span>
<span id="cb4-8"><a href="#cb4-8"></a>        <span class="kw">&lt;li&gt;</span>Smith, John<span class="kw">&lt;/li&gt;</span></span>
<span id="cb4-9"><a href="#cb4-9"></a>      <span class="kw">&lt;/ul&gt;</span></span>
<span id="cb4-10"><a href="#cb4-10"></a>  <span class="kw">&lt;/body&gt;</span></span>
<span id="cb4-11"><a href="#cb4-11"></a><span class="kw">&lt;/html&gt;</span></span></code></pre></div></td>
</tr>
<tr class="odd">
<td><p>CSV</p></td>
<td><div class="sourceCode" id="cb5"><pre class="sourceCode xslt"><code class="sourceCode xslt"><span id="cb5-1"><a href="#cb5-1"></a><span class="kw">&lt;?xml</span> version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;<span class="kw">?&gt;</span></span>
<span id="cb5-2"><a href="#cb5-2"></a><span class="kw">&lt;xsl:stylesheet</span></span>
<span id="cb5-3"><a href="#cb5-3"></a><span class="ot">  version=</span><span class="st">&quot;1.0&quot;</span></span>
<span id="cb5-4"><a href="#cb5-4"></a><span class="ot">  xmlns:xsl=</span><span class="st">&quot;http://www.w3.org/1999/XSL/Transform&quot;</span><span class="kw">&gt;</span></span>
<span id="cb5-5"><a href="#cb5-5"></a></span>
<span id="cb5-6"><a href="#cb5-6"></a>  <span class="kw">&lt;xsl:output</span><span class="ot"> method=</span><span class="st">&quot;text&quot;</span><span class="ot"> encoding=</span><span class="st">&quot;UTF-8&quot;</span><span class="kw">/&gt;</span></span>
<span id="cb5-7"><a href="#cb5-7"></a></span>
<span id="cb5-8"><a href="#cb5-8"></a>  <span class="kw">&lt;xsl:template</span><span class="ot"> match=&quot;/persons&quot;</span><span class="kw">&gt;</span></span>
<span id="cb5-9"><a href="#cb5-9"></a>    <span class="kw">&lt;xsl:apply-templates</span><span class="ot"> select=&quot;person&quot; </span><span class="kw">/&gt;</span></span>
<span id="cb5-10"><a href="#cb5-10"></a>  <span class="kw">&lt;/xsl:template&gt;</span></span>
<span id="cb5-11"><a href="#cb5-11"></a></span>
<span id="cb5-12"><a href="#cb5-12"></a>  <span class="kw">&lt;xsl:template</span><span class="ot"> match=&quot;person&quot;</span><span class="kw">&gt;</span></span>
<span id="cb5-13"><a href="#cb5-13"></a>    <span class="kw">&lt;xsl:value-of</span><span class="ot"> select=&quot;</span>@username<span class="ot">&quot; </span><span class="kw">/&gt;</span></span>
<span id="cb5-14"><a href="#cb5-14"></a>    <span class="kw">&lt;xsl:text&gt;</span>,<span class="kw">&lt;/xsl:text&gt;</span></span>
<span id="cb5-15"><a href="#cb5-15"></a>    <span class="kw">&lt;xsl:apply-templates</span><span class="ot"> select=&quot;*&quot; </span><span class="kw">/&gt;</span></span>
<span id="cb5-16"><a href="#cb5-16"></a>  <span class="kw">&lt;/xsl:template&gt;</span></span>
<span id="cb5-17"><a href="#cb5-17"></a></span>
<span id="cb5-18"><a href="#cb5-18"></a>  <span class="kw">&lt;xsl:template</span><span class="ot"> match=&quot;</span><span class="kw">name</span><span class="ot">&quot;</span><span class="kw">&gt;</span></span>
<span id="cb5-19"><a href="#cb5-19"></a>    <span class="kw">&lt;xsl:value-of</span><span class="ot"> select=&quot;.&quot; </span><span class="kw">/&gt;</span></span>
<span id="cb5-20"><a href="#cb5-20"></a>    <span class="kw">&lt;xsl:text&gt;</span>,<span class="kw">&lt;/xsl:text&gt;</span></span>
<span id="cb5-21"><a href="#cb5-21"></a>  <span class="kw">&lt;/xsl:template&gt;</span></span>
<span id="cb5-22"><a href="#cb5-22"></a></span>
<span id="cb5-23"><a href="#cb5-23"></a>  <span class="kw">&lt;xsl:template</span><span class="ot"> match=&quot;family-name&quot;</span><span class="kw">&gt;</span></span>
<span id="cb5-24"><a href="#cb5-24"></a>    <span class="kw">&lt;xsl:value-of</span><span class="ot"> select=&quot;.&quot; </span><span class="kw">/&gt;</span></span>
<span id="cb5-25"><a href="#cb5-25"></a>    <span class="kw">&lt;xsl:text&gt;</span></span>
<span id="cb5-26"><a href="#cb5-26"></a><span class="kw">&lt;/xsl:text&gt;</span></span>
<span id="cb5-27"><a href="#cb5-27"></a>  <span class="kw">&lt;/xsl:template&gt;</span></span>
<span id="cb5-28"><a href="#cb5-28"></a></span>
<span id="cb5-29"><a href="#cb5-29"></a><span class="kw">&lt;/xsl:stylesheet&gt;</span></span></code></pre></div></td>
<td><p><code>JS1,John,Smith</code><br />
<code>MI1,Morka,Ismincius</code></p></td>
</tr>
</tbody>
</table>

## テンプレート関数

XSLT はテンプレートの関数を再帰的な形で定義ができる純粋関数型言語でもある。

下記のものはテンプレート関数 `String_replaceAll`である。これは、パラメーター `this` で指定した文字列中にある、パラメーター `substring` で指定した部分文字列をすべて、パラメーター `replacement` で指定する文字列に置換した文字列を返す関数。これの例から以下の点が分かる。

  - テンプレート関数の定義の仕方（`xsl:template`、`xsl:param`）
  - 引数の値の参照の仕方（`$`<i>`引数名`</i>）
  - 条件分けの仕方（`xsl:if`、`xsl:choose`）
  - XSLT関数（`not`、`contains`、`substring-before`、`substring-after`）
  - XSLT関数の使い方（<xsl:value-of select="<i>`XSLT関数 (引数...)`</i>`" />`）
  - 定義されたテンプレート関数の呼び出し方（`xsl:call-template`、`xsl:with-param`：再帰呼び出しの箇所）

<!-- end list -->

``` xslt
<?xml version="1.0" encoding="ISO-8859-1" ?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:template name="String_replaceAll">
  <!-- 引数 -->
  <xsl:param name="this" select="''" />
  <xsl:param name="substring" />
  <xsl:param name="replacement" />

  <xsl:if test="not ($this='')">
    <xsl:choose>
      <!-- this に substring が含まれる場合の値 -->
      <xsl:when test="contains ($this, $substring)">
        <xsl:value-of select="substring-before ($this, $substring)" />
        <xsl:copy-of select="$replacement" />
        <xsl:call-template name="String_replaceAll"> <!-- 再帰呼び出し -->
          <xsl:with-param name="this" select="substring-after ($this, $substring)" />
          <xsl:with-param name="substring" select="$substring" />
          <xsl:with-param name="replacement" select="$replacement" />
        </xsl:call-template>
      </xsl:when>

      <!-- そうでない場合の値 -->
      <xsl:otherwise>
        <xsl:value-of select="$this" />
      </xsl:otherwise>
    </xsl:choose>
  </xsl:if>
</xsl:template>
</xsl:stylesheet>
```

## メディア型

XSLTの[メディア型](https://ja.wikipedia.org/wiki/メディア型 "wikilink")は、「`application/xslt+xml`」としてに登録されており\[1\]、「`application/xslt+xml`」または「`application/xml`」が望ましいMIMEタイプである。しかし、[Internet Explorerなど一部の](../Page/Internet_Explorer.md "wikilink")[ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")には、これらのMIMEではXSLTを認識しないものや、「`text/xsl`」などの独自に定めたMIMEのみを認識するものも多い\[2\]。

## 脚注

### 注釈

### 出典

## 関連項目

  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")
      - [プログラミング言語](../Page/プログラミング言語.md "wikilink")
          - [宣言型言語](https://ja.wikipedia.org/wiki/宣言型言語 "wikilink")
              - [関数型言語](../Page/関数型言語.md "wikilink")
      - [変換言語](https://ja.wikipedia.org/wiki/変換言語 "wikilink")

## 外部リンク

  - 実装
      - [Xalan-Java](https://xml.apache.org/xalan-j/)
      - [Xalan-C++](https://xml.apache.org/xalan-c/)
      - [libxslt](http://xmlsoft.org/XSLT/) the XSLT C library for Gnome
      - [Sablotron](http://www.gingerall.com/charlie/ga/xml/p_sab.xml)
      - [SAXON](http://saxon.sourceforge.net/) by Michael Kay
      - [XT](http://www.blnz.com/xt/index.html) by James Clark
      - \[<https://docs.microsoft.com/en-us/previous-versions/windows/desktop/ms759204(v=vs.85>) XSLT for MSXML | Microsoft Docs\]
          - [\[MS-XSLT](https://docs.microsoft.com/en-us/openspecs/ie_standards/ms-xslt/edf5c768-02cf-4dfd-9322-0516470216fa): Microsoft XSLTransformations (XSLT) Standards Support Document\]
      - [Mozillaは](../Page/Mozilla_Application_Suite.md "wikilink")[XSLTにネイティブ対応](https://developer.mozilla.org/en-US/docs/Web/XSLT)
      - [X-Smiles](http://www.xsmiles.org/)はXSLTにネイティブ対応している
      - [<oXygen/> XSLT editor and debugger](http://www.oxygenxml.com/xslt_editor.html)
  - 仕様書
      - [XSLT 1.0 W3C 勧告](https://www.w3.org/TR/xslt/all/)
          -
      - [XSLT 2.0 W3C 勧告](https://www.w3.org/TR/xslt20/)
      - [XSLT 3.0 W3C 勧告](https://www.w3.org/TR/xslt-30/)
      - [XSLTチュートリアル](https://www.data2type.de/xml-xslt-xslfo/xslt/) (ドイツ語)
      - [XSLT 2.0参照](https://www.data2type.de/xml-xslt-xslfo/xslt/xslt-referenz/) (ドイツ語)
      - [XSLTとXPathリファレンス](https://www.data2type.de/xml-xslt-xslfo/xslt/xsltundxpathreferenz) (ドイツ語)

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:スタイルシート言語](https://ja.wikipedia.org/wiki/Category:スタイルシート言語 "wikilink")

1.  [Media Types](https://www.iana.org/assignments/media-types/media-types.xhtml)
2.  [XMLデータの管理: XMLドキュメントの識別](http://www.ibm.com/developerworks/jp/xml/library/x-mxd2/)