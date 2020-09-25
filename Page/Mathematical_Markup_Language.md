> この記事は[Mathematical Markup Language](https://ja.wikipedia.org/wiki/Mathematical_Markup_Language)から翻訳されています。


****（マスマティカル マークアップ ランゲージ 略：**MathML**（マスエムエル））は、[XMLアプリケーションの一つで](../Page/Extensible_Markup_Language.md "wikilink")、[数式](../Page/数式.md "wikilink")を記述するための[マークアップ言語](../Page/マークアップ言語.md "wikilink")である。単体では数式の記述しかできないため、文書として利用するには[XHTMLに埋め込んでXHTML文書として扱うなどする](../Page/Extensible_HyperText_Markup_Language.md "wikilink")。

## 歴史

コンピュータ上で数式を記述する要求は[ウェブが普及する前からあった](../Page/World_Wide_Web.md "wikilink")。なかでも[は有名でかつよく使われており](../Page/TeX.md "wikilink")、数式の表記方法としてもテキストのみで表記せざるを得ないときなどに用いられる他、ウィキペディアを含む[ウィキ](../Page/ウィキ.md "wikilink")等での数式を表現する手段として今日でもよく使われている。しかし、[HTML上で数式を表現する手段がなく](../Page/HyperText_Markup_Language.md "wikilink")、ウェブで数式を表現するには[画像](../Page/画像.md "wikilink")にするか、[PDFなどHTML以外の形式にすることが多い](../Page/Portable_Document_Format.md "wikilink")。

なお、[HTML 3.0では数式を表現できるようにしていた](https://ja.wikipedia.org/wiki/HyperText_Markup_Language#HTML_3.0 "wikilink")。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")の案ではMATH要素が入れられることになっていた\[1\]。これは[Mathematica](../Page/Mathematica.md "wikilink")で有名な Wolfram Research の提案をもとにしたものである。しかしHTML3.0は後に破棄され、またほとんどのブラウザはMATH要素に対応しなかった。HTMLに数式を載せること自体は果たせなかったものの、後の[W3CのMathワーキンググループの前身といえる](../Page/World_Wide_Web_Consortium.md "wikilink") HTML Math Editorial Review Board が設立されるなどした。ちなみに、これは現在のMathMLとは違い、[の数式表記に似た表記法であった](../Page/TeX.md "wikilink")。

[1999年](../Page/1999年.md "wikilink")7月にMathML規格バージョン1.01がW3CのMathワーキンググループから勧告された。そして[2001年](../Page/2001年.md "wikilink")2月にバージョン2.0が勧告され、[2003年](../Page/2003年.md "wikilink")10月にバージョン2.0第2版が勧告された。その後、[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")10月にバージョン3.0が勧告された。

MathMLのオリジナルのバージョンでは名前空間が決められていなかった。というのも、まだXML名前空間の仕様自体が決まっていなかったからである。こうした事情から名前空間を指定されないことが多いが、名前空間を <http://www.w3.org/1998/Math/MathML> と指定しないとMathMLと認識しない実装も多い。

## 表示と意味論

MathMLは数式の要素のその*表示*をもってだけでなくその*意味*もまた処理する（MathMLの後者のものは「内容MathML」として知られる\[2\]）。その内容が利用者にたいして通じるかどうかは、（方程）式の意味がその表示から離れて保たれるかどうかによる。例えば、それらにおいてMathMLが埋め込まれたウェブページは多くのブラウザーで自然なウェブページとして見ることができる、しかし視覚障害の利用者はそれらを[スクリーンリーダー](../Page/スクリーンリーダー.md "wikilink")（例えば、[Internet Explorer](../Page/Internet_Explorer.md "wikilink")、(あるいは)9656+ビルトの[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")9.5のためのMathPlayer[プラグイン](../Page/プラグイン.md "wikilink")、またはFirefoxのための拡張版）の利用を通して同じようにMathMLを読むこともできる。

### 表現MathML

表現MathMLは（方程）式の（視覚的）表示に向けて用途を絞る、そしておおよそ30 個の構成要素をもつ。構成要素の名前はすべて`m`から始まる。ひとつの表現MathMLの表示は、それらのレイアウトを制御するものである（主に細部を細かく制御するものである、おおよそ50個の標識がまたある）、上位レベルの構成要素を使って組み合わされたところの*トークン*から組み立てられる。

### 内容MathML

内容MathMLは意味論においてまたは意味について、またはそれのレイアウトよりもむしろ表現に向いて用途を絞る。内容MathMLの中心は関数の適用を表示するところの構成要素である。適用されるその関数はのもとの最初の子の構成要素であり、そしてそれのオペランドまたはパラメーターは子の構成要素を保持する。内容MathMLはわずかな標識しか用いない。
識別子のようなものや数は、表現MathMLと比べて多量に、しかし`ci`と`cn`のようなものの構成要素をもって、個別にマークアップされる。トークンの単なる他のタイプの存在よりもむしろ、`times`、`power`などの、数学的な意味をMathMLが認めるものである、明確な構成要素によってオペレーターは表示される。いろいろな関数とオペレーターのために100個を超えるいろいろな構成要素がある（\[[http://www.w3.org/TR/MathML3/chapter4.html\#contm.opel\]を見よ](http://www.w3.org/TR/MathML3/chapter4.html#contm.opel%5Dを見よ)）。

## 例

よく知られた[二次方程式](../Page/二次方程式.md "wikilink")の解の公式を例にする:

\[x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\]

これを[で記述すると以下のようになる](../Page/TeX.md "wikilink"):

``` tex
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
```

MathMLで記述すると以下のようになる:

``` xml
<math>
 <mrow>
  <mi>x</mi>
  <mo>=</mo>
  <mfrac>
   <mrow>
    <mrow>
     <mo>-</mo>
     <mi>b</mi>
    </mrow>
    <mo>&PlusMinus;</mo>
    <msqrt>
     <mrow>
      <msup>
       <mi>b</mi>
       <mn>2</mn>
      </msup>
      <mo>-</mo>
      <mrow>
       <mn>4</mn>
       <mo>&InvisibleTimes;</mo>
       <mi>a</mi>
       <mo>&InvisibleTimes;</mo>
       <mi>c</mi>
      </mrow>
     </mrow>
    </msqrt>
   </mrow>
   <mrow>
    <mn>2</mn>
    <mo>&InvisibleTimes;</mo>
    <mi>a</mi>
   </mrow>
  </mfrac>
 </mrow>
</math>
```

このように人間の[可読性](../Page/可読性.md "wikilink")を求めるならばのほうが優れている。しかし、XMLアプリケーションであるMathMLは本来コンピュータによる数式の意味認識において有利となるよう設計されたものであり、人間がMathMLを直接書いたり編集したりすることは意図していない\[3\]。

## ソフトウェアでの対応状況

2015年現在、普及はしているとは言い難いが、MathML出力をサポートしているソフトは増えつつある。

### エディタ

MathMLをサポートする[ネイティブ](https://ja.wikipedia.org/wiki/ネイティブ "wikilink")なエディタにはからのMathFlowと[MathType](https://ja.wikipedia.org/wiki/MathType "wikilink")、[ウルフラム・リサーチ](../Page/ウルフラム・リサーチ.md "wikilink")からの、、そして[WIRIS](https://ja.wikipedia.org/wiki/WIRIS "wikilink")がある。\[4\][W3CにMathMLのエディタのリストがある](../Page/World_Wide_Web_Consortium.md "wikilink")。\[5\]
[Mathematica](../Page/Mathematica.md "wikilink")、[Maple](../Page/Maple.md "wikilink")およびのウィンドウズ版のようなものの数学のソフトウェア製品と同様に、（[OpenOffice Mathによる](https://ja.wikipedia.org/wiki/OpenOffice_Math "wikilink")）[Apache OpenOffice](https://ja.wikipedia.org/wiki/Apache_OpenOffice "wikilink")、（[LibreOffice Mathによる](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")）[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")、（以前の[KOfficeの](../Page/Calligra_Suite.md "wikilink")）[Calligra Suite](../Page/Calligra_Suite.md "wikilink")、そして[MS Office 2007のような主要な製品によってもMathMLはサポートされている](https://ja.wikipedia.org/wiki/Microsoft_Office_2007 "wikilink")。
[Mozilla Firefoxのアドオンの](https://ja.wikipedia.org/wiki/Firefox "wikilink")は、[WYSIWYG](../Page/WYSIWYG.md "wikilink")のMathMLエディタを提供する。
たいていのエディタは表現MathMLだけを作り出す。MathDoxの数式エディタは表現だけでなく内容MathMLもまた提供するOpenMathエディタである。MathMLの表現、内容、ならびにそれらの混ざったマークアップを編集するのにFormulator MathML WeaverはWYSIWYGスタイルを使う。
[TeXmacs](https://ja.wikipedia.org/wiki/TeXmacs "wikilink")などの[WYSIWYG](../Page/WYSIWYG.md "wikilink")なエディタでMathML出力をすることができるものや、MathMLをネイティブに読込・保存できるソフトとしてFormulator\[6\]、[Amaya](../Page/Amaya.md "wikilink")などがある。

他の数式表現形式からMathMLに変換するソフトもあり、例えば[からの変換ソフトとして](../Page/TeX.md "wikilink")[やMathType](../Page/ConTeXt.md "wikilink")、itex2mmlなどがある。またウェブ上で変換をするページもある。

### ブラウザ

ブラウザでのMathMLネイティブサポート（ブラウザのレンダリングエンジンによるMathMLのレンダリング）は進んでいない。対応しているのは、[Gecko](../Page/Gecko.md "wikilink") を採用している [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") などのブラウザ\[7\]、[Safari](../Page/Safari.md "wikilink") 5.1 以降にとどまる。[Google ChromeではChrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink") 24で対応したが、実装上の問題からChrome 25で非対応になり、それ以降実装されていない\[8\]。[Presto](../Page/Presto.md "wikilink") を採用している、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink") 9.50\[9\]〜12.1 においては単体でほとんどの数式の表示が可能となったが、Opera 14 よりレンダリングエンジンが WebKit そして Blink になり非対応となった。

[Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、[Microsoft Edge](https://ja.wikipedia.org/wiki/Microsoft_Edge "wikilink")、[Internet Explorer](../Page/Internet_Explorer.md "wikilink") は対応していない。ただし[JavaScriptライブラリ](https://ja.wikipedia.org/wiki/JavaScriptライブラリ "wikilink")の[MathJax](https://ja.wikipedia.org/wiki/MathJax "wikilink")\[10\]や、[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 用のプラグイン[MathPlayer](http://www.dessci.com/en/products/mathplayer/)などを使うと、Math ML非対応ブラウザでも表示することができる。

ブラウザでのMath MLのレンダリングの品質はインストールされているフォントに依存する。[STIXフォント事業](https://ja.wikipedia.org/wiki/STIXフォント事業 "wikilink")はオープンライセンスの数学フォントをリリースしている。Microsoft Windows付属の[Cambria](https://ja.wikipedia.org/wiki/Cambria_\(フォント\) "wikilink") Mathフォントもサポートしている。

### その他

アンテナハウスの[AH FormatterはXMLまたはHTML中に埋め込まれたMathMLを可視化して印刷したり](../Page/XSL_Formatter.md "wikilink")、PDFやSVGなどに出力できる\[11\]。

[JAWS](https://ja.wikipedia.org/wiki/JAWS "wikilink")は[2015年](../Page/2015年.md "wikilink")に発売されたVersion 16.0よりMathMLに対応している\[12\]。

### ソフトウェア開発のサポート

コンピューター・エイデッド・エデュケーション（遠隔教育、電子教科書、そして他の教材）；魅力的なレポートの自動作成；[数式処理システム](../Page/数式処理システム.md "wikilink")；著作、教育、出版ツール（ウェブとデスクトップ・オリエンテッドの両方）、そして数学、科学、ビジネス、経済、その他の多くの他のアプリケーションのような多様なものにおいてMathMLフォーマットのサポートはソフトウェア・アプリケーションの開発を加速する。ソフトウェア開発者らにたいして彼らのアプリケーションにおいて機能的で数学的なレンダリング／編集／処理を組み入れるように簡易な方法の提供を行って、幾つかのソフトウェア・ベンダーらは彼らのMathMLエディタのコンポーネント・エディションを提案する。例えば、Hermitech LaboratoryからのFormulator ActiveX ControlはMathMLのエディタと同じようになるようにアプリケーションへ合併するようできる、はインタラクティブな数式を含むものであるウェブ・ページを組み立てるためのツールキットを提供する（MathFlow DEvelopers Suite、\[13\]）。

## 註

<references />

### 訳注

## 外部リンク

  - [W3C Math Home](http://www.w3.org/Math/) 規格書、FAQ、ソフトウェアの一覧がある

<!-- end list -->

  -
  - [MathML 数式組版入門](http://www.antenna.co.jp/AHF/ahf_publication/index.html#MathML)

  - [wiris - 数学教育のグローバルソリューション](http://www.wiris.com/editor/demo/ja/mathml-latex) エディタの使用を体験できるデモンストレーション

  - [MathMLの未来を考える―（1）現状の整理](http://blog.cas-ub.com/?p=11986)

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:数学マークアップ言語](https://ja.wikipedia.org/wiki/Category:数学マークアップ言語 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")

1.  [HTML Math](http://www.w3.org/MarkUp/html3/maths.html)
2.  Presentation MathMLをPMathML、Content MathMLをCMathMLのように略記することも一案だが、ここでは文献に倣った。
3.
4.  [WIRIS editor page describing the use of MathML](http://www.wiris.com/en/editor/discover/reach-the-highest-standard-mathml).Wiris.com.Retrieved on 9 May 2012.
5.  [MathML Software - Editors at W3C](http://www.w3.org/Math/Software/mathml_software_cat_editors.html). W3C.org (24 April 2012). Retrieved on 9 May 2012.
6.  [Hermitech Laboratory - Formulator Mathml Weaver](http://www.hermitech.ic.zt.ua/projects/formulator/index.html)
7.  [Authoring MathML for Mozilla](http://www.mozilla.org/projects/mathml/authoring.html)
8.  「[WebKitの数式（MathML）でSafariはボランティアの努力を採用し、数式を表示できる。Chromeは同じものを不採用として批判を浴びる。](http://blog.cas-ub.com/?p=6495)」『電子書籍、電子出版のCAS-UBブログ』 アンテナハウス株式会社、2014年3月8日
9.  [Opera Desktop Team - Even more work](https://web.archive.org/web/20071118141611/http://my.opera.com/desktopteam/blog/2007/11/16/even-more-work)
10. [MathJax](http://www.mathjax.org/)
11. [MathML で記述した数式を PDF に変換](http://www.antenna.co.jp/AHF/mathmloption.html)
12. [JAWS16.0日本語版](http://www.extra.co.jp/jaws/)
13. [MathFlow](http://www.dessci.com/en/products/mathflow), Dessci.com. Retrieved on 9 May 2012.