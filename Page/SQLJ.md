> この記事は[SQLJ](https://ja.wikipedia.org/wiki/SQLJ)から翻訳されています。


**SQLJ**（えすきゅーえるじぇい）は、[コンピュータ](../Page/コンピュータ.md "wikilink")の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[プログラムに](../Page/プログラム_\(コンピュータ\).md "wikilink")[SQL](../Page/SQL.md "wikilink")文を埋め込む方法 ([埋め込みSQL](../Page/埋め込みSQL.md "wikilink")) を定めた[ISO標準](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")（ISO/IEC 9075-10）である。

[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[JDBC](../Page/JDBC.md "wikilink")とは異なり、SQLJは[プログラミング言語](../Page/プログラミング言語.md "wikilink")Javaを拡張したものである。そのため、SQLJプログラムを実行するためには、プログラムを[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")する前に[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")（SQLJトランスレータ）で変換しなければならない。

SQLJがJDBCより優れている点は、次のとおりである。

  - SQLJプログラムは、JDBCを使ったJavaプログラムより短くなることが多い。
  - プリプロセス時にSQLの文法をチェックできる。

逆に劣っている点は、次のとおりである。

  - プリプロセスが必要である。
  - SQLJをサポートしている[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) が少ない。
  - [Hibernate](../Page/Hibernate.md "wikilink")のような[永続化](https://ja.wikipedia.org/wiki/永続化 "wikilink")フレームワーク ([オブジェクトリレーショナルマッピング](https://ja.wikipedia.org/wiki/オブジェクトリレーショナルマッピング "wikilink")) でSQLJがサポートされていない。

## 例

以下の例では、SQLJの文法と[JDBC](../Page/JDBC.md "wikilink")の用法を対比させる。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><a href="../Page/JDBC.md" title="wikilink">JDBC</a></p></th>
<th><p>SQLJ</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>複数行の<a href="https://ja.wikipedia.org/wiki/クエリ" title="wikilink">クエリ</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode java"><code class="sourceCode java"><span id="cb1-1"><a href="#cb1-1"></a> <span class="bu">PreparedStatement</span> statement = conn.<span class="fu">prepareStatement</span>(</span>
<span id="cb1-2"><a href="#cb1-2"></a>    <span class="st">&quot;SELECT LASTNAME&quot;</span></span>
<span id="cb1-3"><a href="#cb1-3"></a>  + <span class="st">&quot; , FIRSTNME&quot;</span></span>
<span id="cb1-4"><a href="#cb1-4"></a>  + <span class="st">&quot; , SALARY&quot;</span></span>
<span id="cb1-5"><a href="#cb1-5"></a>  + <span class="st">&quot; FROM DSN8710.EMP&quot;</span></span>
<span id="cb1-6"><a href="#cb1-6"></a>  + <span class="st">&quot; WHERE SALARY BETWEEN ? AND ?&quot;</span>);</span>
<span id="cb1-7"><a href="#cb1-7"></a> statement.<span class="fu">setBigDecimal</span>(<span class="dv">1</span>, min);</span>
<span id="cb1-8"><a href="#cb1-8"></a> statement.<span class="fu">setBigDecimal</span>(<span class="dv">2</span>, max);</span>
<span id="cb1-9"><a href="#cb1-9"></a> <span class="bu">ResultSet</span> rs = statement.<span class="fu">executeQuery</span>();</span>
<span id="cb1-10"><a href="#cb1-10"></a> <span class="kw">while</span> (rs.<span class="fu">next</span>()) {</span>
<span id="cb1-11"><a href="#cb1-11"></a>   lastname = rs.<span class="fu">getString</span>(<span class="dv">1</span>);</span>
<span id="cb1-12"><a href="#cb1-12"></a>   firstname = rs.<span class="fu">getString</span>(<span class="dv">2</span>);</span>
<span id="cb1-13"><a href="#cb1-13"></a>   salary = rs.<span class="fu">getBigDecimal</span>(<span class="dv">3</span>);</span>
<span id="cb1-14"><a href="#cb1-14"></a>   <span class="co">// 行を表示させる...</span></span>
<span id="cb1-15"><a href="#cb1-15"></a> }</span>
<span id="cb1-16"><a href="#cb1-16"></a> rs.<span class="fu">close</span>();</span>
<span id="cb1-17"><a href="#cb1-17"></a> statement.<span class="fu">close</span>();</span></code></pre></div></td>
<td><div class="sourceCode" id="cb2"><pre class="sourceCode java"><code class="sourceCode java"><span id="cb2-1"><a href="#cb2-1"></a> #sql <span class="kw">private</span> <span class="dt">static</span> iterator <span class="fu">EmployeeIterator</span>(<span class="bu">String</span>, <span class="bu">String</span>, <span class="bu">BigDecimal</span>);</span>
<span id="cb2-2"><a href="#cb2-2"></a> ...</span>
<span id="cb2-3"><a href="#cb2-3"></a> EmployeeIterator iter;</span>
<span id="cb2-4"><a href="#cb2-4"></a> #sql [ctx] iter = {</span>
<span id="cb2-5"><a href="#cb2-5"></a>   SELECT LASTNAME</span>
<span id="cb2-6"><a href="#cb2-6"></a>        , FIRSTNME</span>
<span id="cb2-7"><a href="#cb2-7"></a>        , SALARY</span>
<span id="cb2-8"><a href="#cb2-8"></a>     FROM DSN8710.<span class="fu">EMP</span></span>
<span id="cb2-9"><a href="#cb2-9"></a>    WHERE SALARY BETWEEN :min AND :max</span>
<span id="cb2-10"><a href="#cb2-10"></a> };</span>
<span id="cb2-11"><a href="#cb2-11"></a> <span class="kw">while</span> (<span class="kw">true</span>) {</span>
<span id="cb2-12"><a href="#cb2-12"></a>   #sql {</span>
<span id="cb2-13"><a href="#cb2-13"></a>     FETCH :iter</span>
<span id="cb2-14"><a href="#cb2-14"></a>      INTO :lastname, :firstname, :salary</span>
<span id="cb2-15"><a href="#cb2-15"></a>   };</span>
<span id="cb2-16"><a href="#cb2-16"></a>   <span class="kw">if</span> (iter.<span class="fu">endFetch</span>()) <span class="kw">break</span>;</span>
<span id="cb2-17"><a href="#cb2-17"></a>   <span class="co">// 行を表示させる...</span></span>
<span id="cb2-18"><a href="#cb2-18"></a> }</span>
<span id="cb2-19"><a href="#cb2-19"></a> iter.<span class="fu">close</span>();</span></code></pre></div></td>
</tr>
<tr class="odd">
<td><p>単一行のクエリ</p></td>
<td></td>
</tr>
<tr class="even">
<td><div class="sourceCode" id="cb3"><pre class="sourceCode java"><code class="sourceCode java"><span id="cb3-1"><a href="#cb3-1"></a> <span class="bu">PreparedStatement</span> statement = conn.<span class="fu">prepareStatement</span>(</span>
<span id="cb3-2"><a href="#cb3-2"></a>     <span class="st">&quot;SELECT MAX(SALARY), AVG(SALARY)&quot;</span></span>
<span id="cb3-3"><a href="#cb3-3"></a>   + <span class="st">&quot; FROM DSN8710.EMP&quot;</span>);</span>
<span id="cb3-4"><a href="#cb3-4"></a> rs = statement.<span class="fu">executeQuery</span>();</span>
<span id="cb3-5"><a href="#cb3-5"></a> <span class="kw">if</span> (!rs.<span class="fu">next</span>()) {</span>
<span id="cb3-6"><a href="#cb3-6"></a>   <span class="co">// エラー -- 該当行なし</span></span>
<span id="cb3-7"><a href="#cb3-7"></a> }</span>
<span id="cb3-8"><a href="#cb3-8"></a> maxSalary = rs.<span class="fu">getBigDecimal</span>(<span class="dv">1</span>);</span>
<span id="cb3-9"><a href="#cb3-9"></a> avgSalary = rs.<span class="fu">getBigDecimal</span>(<span class="dv">2</span>);</span>
<span id="cb3-10"><a href="#cb3-10"></a> <span class="kw">if</span> (rs.<span class="fu">next</span>()) {</span>
<span id="cb3-11"><a href="#cb3-11"></a>   <span class="co">// エラー -- 複数行が存在</span></span>
<span id="cb3-12"><a href="#cb3-12"></a> }</span>
<span id="cb3-13"><a href="#cb3-13"></a> rs.<span class="fu">close</span>();</span>
<span id="cb3-14"><a href="#cb3-14"></a> statement.<span class="fu">close</span>();</span></code></pre></div></td>
<td><div class="sourceCode" id="cb4"><pre class="sourceCode java"><code class="sourceCode java"><span id="cb4-1"><a href="#cb4-1"></a> #sql [ctx] {</span>
<span id="cb4-2"><a href="#cb4-2"></a>   SELECT <span class="fu">MAX</span>(SALARY), <span class="fu">AVG</span>(SALARY)</span>
<span id="cb4-3"><a href="#cb4-3"></a>     INTO :maxSalary, :avgSalary</span>
<span id="cb4-4"><a href="#cb4-4"></a>     FROM DSN8710.<span class="fu">EMP</span></span>
<span id="cb4-5"><a href="#cb4-5"></a> };</span></code></pre></div></td>
</tr>
<tr class="odd">
<td><p>挿入</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><div class="sourceCode" id="cb5"><pre class="sourceCode java"><code class="sourceCode java"><span id="cb5-1"><a href="#cb5-1"></a> statement = conn.<span class="fu">prepareStatement</span>(</span>
<span id="cb5-2"><a href="#cb5-2"></a>    <span class="st">&quot;INSERT INTO DSN8710.EMP &quot;</span> +</span>
<span id="cb5-3"><a href="#cb5-3"></a>    <span class="st">&quot;(EMPNO, FIRSTNME, MIDINIT, LASTNAME, HIREDATE, SALARY) &quot;</span></span>
<span id="cb5-4"><a href="#cb5-4"></a>  + <span class="st">&quot;VALUES (?, ?, ?, ?, CURRENT DATE, ?)&quot;</span>);</span>
<span id="cb5-5"><a href="#cb5-5"></a> statement.<span class="fu">setString</span>(<span class="dv">1</span>, empno);</span>
<span id="cb5-6"><a href="#cb5-6"></a> statement.<span class="fu">setString</span>(<span class="dv">2</span>, firstname);</span>
<span id="cb5-7"><a href="#cb5-7"></a> statement.<span class="fu">setString</span>(<span class="dv">3</span>, midinit);</span>
<span id="cb5-8"><a href="#cb5-8"></a> statement.<span class="fu">setString</span>(<span class="dv">4</span>, lastname);</span>
<span id="cb5-9"><a href="#cb5-9"></a> statement.<span class="fu">setBigDecimal</span>(<span class="dv">5</span>, salary);</span>
<span id="cb5-10"><a href="#cb5-10"></a> statement.<span class="fu">executeUpdate</span>();</span>
<span id="cb5-11"><a href="#cb5-11"></a> statement.<span class="fu">close</span>();</span></code></pre></div></td>
<td><div class="sourceCode" id="cb6"><pre class="sourceCode sql"><code class="sourceCode sql"><span id="cb6-1"><a href="#cb6-1"></a> #sql [ctx] {</span>
<span id="cb6-2"><a href="#cb6-2"></a>   <span class="kw">INSERT</span> <span class="kw">INTO</span> DSN8710.EMP</span>
<span id="cb6-3"><a href="#cb6-3"></a>     (EMPNO,  FIRSTNME,   MIDINIT,  LASTNAME,  HIREDATE,     SALARY)</span>
<span id="cb6-4"><a href="#cb6-4"></a>   <span class="kw">VALUES</span></span>
<span id="cb6-5"><a href="#cb6-5"></a>     (<span class="ch">:empno</span>, <span class="ch">:firstname</span>, <span class="ch">:midinit</span>, <span class="ch">:lastname</span>, <span class="kw">CURRENT</span> <span class="dt">DATE</span>, <span class="ch">:salary</span>)</span>
<span id="cb6-6"><a href="#cb6-6"></a> };</span></code></pre></div></td>
</tr>
</tbody>
</table>

## 外部リンク

  - [IBM Redbook: DB2 for z/OS and OS/390: Ready for Java](http://www.redbooks.ibm.com/abstracts/sg246435.html) (英文)

[Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:SQL](https://ja.wikipedia.org/wiki/Category:SQL "wikilink") [Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink")