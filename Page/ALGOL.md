> この記事は[ALGOL](https://ja.wikipedia.org/wiki/ALGOL)から翻訳されています。


（**アルゴル**）は、[命令型](https://ja.wikipedia.org/wiki/命令型プログラミング "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")ファミリーの1つ\[1\]。名前「」は「アルゴリズム言語」を意味する英語「」に由来する。1950年代中ごろに開発され、多くの言語に影響を及ぼし、[ACMや教科書や学術論文などで](../Page/Association_for_Computing_Machinery.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")記述の[デファクトスタンダード](https://ja.wikipedia.org/wiki/デファクトスタンダード "wikilink")として30年以上使われた\[2\]。現代の多くの言語が「ALGOL系」あるいは「ALGOL風」(algol-like) とされているという意味で\[3\]、ほぼ同世代の[高水準言語](../Page/高水準言語.md "wikilink")である [FORTRAN](../Page/FORTRAN.md "wikilink")、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、[COBOL](https://ja.wikipedia.org/wiki/COBOL "wikilink") に比べて最も成功したと言うこともできる。[FORTRAN](../Page/FORTRAN.md "wikilink")で明らかとなった問題を防ぐよう設計され、[BCPL](https://ja.wikipedia.org/wiki/BCPL "wikilink")、[B](../Page/B言語.md "wikilink")、[Pascal](../Page/Pascal.md "wikilink")、[Simula](../Page/Simula.md "wikilink")、[Cといった様々なプログラミング言語に影響を与えた](../Page/C言語.md "wikilink")。ALGOLは\[4\]「`begin` と `end` で囲む」という構文による[ブロック構造を導入し](https://ja.wikipedia.org/wiki/ブロック_\(プログラミング\) "wikilink")、[制御構造](https://ja.wikipedia.org/wiki/制御構造 "wikilink")を自在に入れ子（[ネスト](https://ja.wikipedia.org/wiki/ネスティング "wikilink")）にできる初の広まった言語となった\[5\]。また構文の形式的定義を真剣に検討した最初のプログラミング言語でもあり、"Algol 60 Report"\[6\] で導入された[バッカス・ナウア記法](https://ja.wikipedia.org/wiki/バッカス・ナウア記法 "wikilink")は、その後のコンピュータ言語等の構文の形式的定義を示す手法として（プログラミング言語だけに限られず）定番の記法となっている。

## 主なバージョン

次の3つの主要な仕様が存在する。後ろについている数は最初に発表された年を表している。

  -
    当初 **IAL** (**I**nternational **A**lgorithmic **L**anguage) という名称で提案された。
  -
    1960年中ごろに *X1 ALGOL 60* として実装されたのが最初で、1963年に改訂された\[7\]\[8\]。
  -
    1968年に発表され、1973年に改訂された\[9\]。可変配列、スライス、並列性、演算子識別、その他の拡張可能な機能などが新たに導入されている。

IAL (ALGOL 58) は後の様々なプログラミング言語（いわゆるALGOL系言語）に大きな影響を及ぼし、一般にそれらの先祖とみなされている。また、ALGOLの仕様で示された[中間コード](https://ja.wikipedia.org/wiki/中間コード "wikilink")は **ALGOL object code** と呼ばれ、単純でコンパクトなスタックベースの[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")アーキテクチャであり、[計算機科学](../Page/計算機科学.md "wikilink")の分野で[コンパイラ](../Page/コンパイラ.md "wikilink")構築の教育に使われ、他の高水準言語の実装にも使われた。

## 歴史

1950年代後半、等の言語が[米国で作られていたのに対抗して](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")、[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")の学術研究者が世界共通のプログラミング言語として開発した。ALGOLは[1958年](../Page/1958年.md "wikilink")に[チューリッヒ工科大学](https://ja.wikipedia.org/wiki/チューリッヒ工科大学 "wikilink")で行われた国際会議で提案されたものが起源とされる。現代のプログラミング言語と比べて著しく異なる点のひとつに、reference syntax、publication syntax、implementation syntax という3種類の構文がある、ということが挙げられる。当時は[文字コード](../Page/文字コード.md "wikilink")の標準化以前であり、また数学の数式のように印刷したいという要望などもあったため、そのようなことになっている（違いは具象の違いであり、抽象構文は共通である）。これにより、キーワード名や小数点に使用する記号（カンマかピリオドか）を選ぶことなどもできた。

ALGOL 58 は主に欧米の計算機科学者が[アルゴリズム](../Page/アルゴリズム.md "wikilink")の[研究開発](https://ja.wikipedia.org/wiki/研究開発 "wikilink")に用いた。商用アプリケーションにはあまり採用されていない。その原因は[入出力](https://ja.wikipedia.org/wiki/入出力 "wikilink")機能が標準仕様に含まれていなかったためであり、また[バロース](https://ja.wikipedia.org/wiki/バロース "wikilink")以外の大手コンピュータメーカーがこの言語に興味を示さなかったためである。

[ジョン・バッカス](../Page/ジョン・バッカス.md "wikilink")は ALGOL 58 を主たる対象としてプログラミング言語の文法を記述する[バッカス正規記法](https://ja.wikipedia.org/wiki/バッカス・ナウア記法 "wikilink") (Bakus normal form) を開発した。[ピーター・ナウア](https://ja.wikipedia.org/wiki/ピーター・ナウア "wikilink")はそれを ALGOL 60 向けに拡張・改訂。[ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink")が[バッカス・ナウア記法](https://ja.wikipedia.org/wiki/バッカス・ナウア記法 "wikilink") (Bakus-Naur Form) と改称することを提案した\[10\]。

ピーター・ナウアは *ALGOL Bulletin* という学術誌の編集者としてこの言語の国際的議論に参加し、1959年11月にヨーロッパの言語設計グループの一員に選ばれた。そして "Algol 60 Report" の編集者となり、1960年1月にパリで開催された ALGOL 60 についての国際会議の結果を発表した\[11\]。

このパリでの会議（1960年1月1日から16日まで開催）には以下の人々が参加している。

  - ヨーロッパからの参加者

    、[ピーター・ナウア](https://ja.wikipedia.org/wiki/ピーター・ナウア "wikilink")、[ハインツ・ルティシュハウザー](https://ja.wikipedia.org/wiki/ハインツ・ルティシュハウザー "wikilink")、、Bernard Vauquois、、Michael Woodger

  - アメリカからの参加者
    [ジョン・バッカス](../Page/ジョン・バッカス.md "wikilink")、Julien Green、Charles Katz、[ジョン・マッカーシー](../Page/ジョン・マッカーシー.md "wikilink")、[アラン・パリス](https://ja.wikipedia.org/wiki/アラン・パリス "wikilink")、Joseph Henry Wegstein

アラン・パリスはこの会議について、「会合は疲れさせるもので、果てしなく、活発だった。ある人のよいアイデアが悪いアイデアと共に却下されると、その人は機嫌を損ねた。それにもかかわらず、期間中ずっと勤勉さが持続した。13人の作用は素晴らしいものだった」と評している。

ALGOL 60 はその後の多数の言語に影響を与えた。[アントニー・ホーア](../Page/アントニー・ホーア.md "wikilink")は ALGOL 60 を「時代に先行していて、それまでの言語の改良だっただけでなく、その後のほぼ全ての後継者の先駆者となった言語」と評している\[12\]。[Scheme](../Page/Scheme.md "wikilink")というLisp方言の設計者は、その[静的スコープ](https://ja.wikipedia.org/wiki/静的スコープ "wikilink")は ALGOL からの影響だと述べている\[13\]。またSchemeの仕様の名称 "Revised Report on the Algorithmic Language Scheme" もALGOLへのオマージュである\[14\]。

1968年には、後継として ** 68** が開発された。 68 では、2段階文法のワインハールデン記法で文法が記述された。 60 の後継言語制定に至るまでの候補として[ニクラウス・ヴィルト](https://ja.wikipedia.org/wiki/ニクラウス・ヴィルト "wikilink")の 、日本で設計された  等もあったが最終的に  68 が後継として制定された。しかし、あまりに複雑かつ巨大な仕様のため  68 コンパイラの実装は難しく、またワインハールデン記法が難解なこともあり実用的には、ほとんど普及しなかった。そのため単に ALGOL と言った場合にはALGOL 68 ではなくて ALGOL 60 やその方言を指すのが一般的である。

言語の標準化としては、IFIP TC2/WG2.1 において  60 が制定された。その後、遅々として標準化作業はすすまず、1984年になって、[ISOで](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")  60 相当の言語が標準化されたのみである。日本では、かつて  60 の言語規格と入出力ライブラリ規格をそれぞれ[JIS規格で制定していたが](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink") (JIS C 6210-6219)、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")（昭和58年）[9月1日](../Page/9月1日.md "wikilink")付で廃止された。

### ALGOLとプログラミング言語研究

が指摘したように、ALGOLは命令型の[副作用と](https://ja.wikipedia.org/wiki/副作用_\(プログラム\) "wikilink")（[名前渡しの](https://ja.wikipedia.org/wiki/評価戦略 "wikilink")）[ラムダ計算](../Page/ラムダ計算.md "wikilink")を一体に結合した初の言語である。この言語の最も見事な定式化はおそらくによるもので、その文法および意味論の純粋さをよく表している。レイノルズの「理想化した」ALGOLも名前渡しの言語のコンテキストにおける「ローカル」な副作用の適切さについて説得力のある方法論的主張を行っており、[MLのような値渡しの言語が使用する](../Page/ML_\(プログラミング言語\).md "wikilink")「グローバル」な副作用と対比される。ALGOLの概念的完全性により、やMLと共に意味論研究の主な対象とされるようになった\[15\]。

### 実装例

これまでに ALGOL 60 の強化版、拡張版、派生版、サブ言語などが少なくとも70ほど存在した\[16\]。

ALGOL 60 の実装に関する問題は、Nicholas Enticknap と Pat Woodroffe の書いた "[The early days of Algol](http://www.cs.man.ac.uk/CCS/res/res04.htm#d)" で詳しく議論されている。

<table>
<thead>
<tr class="header">
<th><p>|名称</p></th>
<th><p>|年</p></th>
<th><p>|作者</p></th>
<th><p>|国</p></th>
<th><p>|説明</p></th>
<th><p>|対象CPU</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ZMMD-implementation</p></td>
<td><p>1958年</p></td>
<td><p>Bauer, Rutishauser, Samelson, Bottenbruch</p></td>
<td><p>ドイツ</p></td>
<td><p>ALGOL 58 の実装</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Z22_(computer)" title="wikilink">Z22</a><br />
（後に<a href="https://ja.wikipedia.org/wiki/コンラート・ツーゼ" title="wikilink">ツーゼのZ</a>23[17]向けに ALGOL 60 コンパイラを提供している）</p></td>
</tr>
<tr class="even">
<td><p>X1 ALGOL 60</p></td>
<td><p>1960年8月[18]</p></td>
<td><p><a href="../Page/エドガー・ダイクストラ.md" title="wikilink">エドガー・ダイクストラ</a>、 Jaap A. Zonneveld</p></td>
<td><p>オランダ</p></td>
<td><p>ALGOL 60 の世界初の実装[19]</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Electrologica_X1" title="wikilink">Electrologica X1</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Elliott_ALGOL" title="wikilink">Elliott ALGOL</a></p></td>
<td><p>1960年代</p></td>
<td><p><a href="../Page/アントニー・ホーア.md" title="wikilink">アントニー・ホーア</a></p></td>
<td><p>イギリス</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Elliott_803" title="wikilink">Elliott 803</a> &amp; Elliott 503</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/:en:JOVIAL" title="wikilink">JOVIAL</a></p></td>
<td><p>1960年</p></td>
<td><p>Jules Schwarz</p></td>
<td><p>アメリカ</p></td>
<td><p><a href="../Page/Ada.md" title="wikilink">Ada</a>以前の <a href="https://ja.wikipedia.org/wiki/アメリカ国防総省" title="wikilink">DOD</a> <a href="../Page/高水準言語.md" title="wikilink">HOL</a></p></td>
<td><p>各種</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/バロース_B5000#ALGOL" title="wikilink">Burroughs Algol</a><br />
（いくつか派生がある）</p></td>
<td><p>1961年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/バロース" title="wikilink">バロース</a>（ホーアや<a href="../Page/エドガー・ダイクストラ.md" title="wikilink">ダイクストラも参加</a>）</p></td>
<td><p>アメリカ</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/バロース" title="wikilink">バロース</a>のメインフレーム（および<a href="https://ja.wikipedia.org/wiki/ユニシス" title="wikilink">ユニシス</a>の後継シリーズ）の基盤</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/バロース_B5000" title="wikilink">バロースの大型機</a><br />
および中型機</p></td>
</tr>
<tr class="even">
<td><p>Case ALGOL</p></td>
<td><p>1961年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ケース・ウェスタン・リザーブ大学" title="wikilink">ケース・ウェスタン・リザーブ大学</a>[20]</p></td>
<td><p>アメリカ</p></td>
<td><p><a href="../Page/Simula.md" title="wikilink">Simula</a>は Case ALGOL のシミュレーション向け拡張として開発された。</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:UNIVAC_1107" title="wikilink">UNIVAC 1107</a></p></td>
</tr>
<tr class="odd">
<td><p>GOGOL</p></td>
<td><p>1961年</p></td>
<td><p>Bill McKeeman</p></td>
<td><p>アメリカ</p></td>
<td><p>ODIN<a href="https://ja.wikipedia.org/wiki/タイムシェアリングシステム" title="wikilink">タイムシェアリングシステム</a>向け</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PDP-1" title="wikilink">PDP-1</a></p></td>
</tr>
<tr class="even">
<td><p>RegneCentralen ALGOL</p></td>
<td><p>1961年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ピーター・ナウア" title="wikilink">ピーター・ナウア</a>、Jørn Jensen</p></td>
<td><p>デンマーク</p></td>
<td><p>ALGOL 60 の完全実装</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/DASK" title="wikilink">DASK</a> (<a href="https://ja.wikipedia.org/wiki/:en:Regnecentralen" title="wikilink">Regnecentralen</a>)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Dartmouth_ALGOL_30" title="wikilink">Dartmouth ALGOL 30</a></p></td>
<td><p>1962年</p></td>
<td><p>他</p></td>
<td><p>アメリカ</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:LGP-30" title="wikilink">LGP-30</a></p></td>
</tr>
<tr class="even">
<td><p>USS 90 Algol</p></td>
<td><p>1962年</p></td>
<td><p>L. Petrone</p></td>
<td><p>イタリア</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Algol Translator</p></td>
<td><p>1962年</p></td>
<td><p>G. van der Mey, <a href="https://ja.wikipedia.org/wiki/:en:Willem_van_der_Poel" title="wikilink">W.L. van der Poel</a></p></td>
<td><p>オランダ</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/KPN" title="wikilink">オランダ国営電話会社</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:ZEBRA_(computer)" title="wikilink">ZEBRA</a></p></td>
</tr>
<tr class="even">
<td><p>Kidsgrove Algol</p></td>
<td><p>1963年</p></td>
<td><p>F. G. Duncan</p></td>
<td><p>イギリス</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/イングリッシュ・エレクトリック" title="wikilink">イングリッシュ・エレクトリック</a> <a href="https://ja.wikipedia.org/wiki/:en:English_Electric_KDF9" title="wikilink">KDF9</a></p></td>
</tr>
<tr class="odd">
<td><p>VALGOL</p></td>
<td><p>1963年</p></td>
<td><p>Val Schorre</p></td>
<td><p>アメリカ</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:META_II" title="wikilink">META II</a> <a href="https://ja.wikipedia.org/wiki/コンパイラジェネレータ" title="wikilink">コンパイラジェネレータ</a>のテストとして開発</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Whetstone" title="wikilink">Whetstone</a></p></td>
<td><p>1964年</p></td>
<td><p>Brian Randell, L J Russell</p></td>
<td><p>イギリス</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/イングリッシュ・エレクトリック" title="wikilink">イングリッシュ・エレクトリック</a> <a href="https://ja.wikipedia.org/wiki/:en:English_Electric_KDF9" title="wikilink">KDF9</a></p></td>
</tr>
<tr class="odd">
<td><p>NU ALGOL</p></td>
<td><p>1965年</p></td>
<td></td>
<td><p>ノルウェー</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/UNIVAC" title="wikilink">UNIVAC</a></p></td>
</tr>
<tr class="even">
<td><p>ALGEK</p></td>
<td><p>1965年</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ソビエト連邦" title="wikilink">ソビエト連邦</a></p></td>
<td><p>ALGOL 60 と<a href="https://ja.wikipedia.org/wiki/COBOL" title="wikilink">COBOL</a>に基づいた経済タスク用</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Minsk_family_of_computers" title="wikilink">Minsk-22</a></p></td>
</tr>
<tr class="odd">
<td><p>MALGOL</p></td>
<td><p>1966年</p></td>
<td><p>publ. A. Viil, M Kotli &amp; M. Rakhendi</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/エストニア・ソビエト社会主義共和国" title="wikilink">エストニア・ソビエト社会主義共和国</a></p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Minsk_family_of_computers" title="wikilink">Minsk-22</a></p></td>
</tr>
<tr class="even">
<td><p>ALGAMS</p></td>
<td><p>1967年</p></td>
<td><p>GAMS（中型機のための自動プログラミング）グループとコメコン科学アカデミーの共同開発</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/経済相互援助会議" title="wikilink">コメコン</a></p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Minsk_family_of_computers" title="wikilink">Minsk-22</a>、後に <a href="https://ja.wikipedia.org/wiki/:en:ES_EVM" title="wikilink">ES EVM</a>、<a href="https://ja.wikipedia.org/wiki/BESM" title="wikilink">BESM</a></p></td>
</tr>
<tr class="odd">
<td><p>ALGOL/ZAM</p></td>
<td><p>1967年</p></td>
<td></td>
<td><p>ポーランド</p></td>
<td></td>
<td><p>ZAM（ポーランド製）</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Simula.md" title="wikilink">Simula 67</a></p></td>
<td><p>1967年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/オーレ＝ヨハン・ダール" title="wikilink">オーレ＝ヨハン・ダール</a>、<a href="https://ja.wikipedia.org/wiki/クリステン・ニゴール" title="wikilink">クリステン・ニゴール</a></p></td>
<td><p>ノルウェー</p></td>
<td><p>ALGOL 60 にオブジェクト指向を導入</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:UNIVAC_1107" title="wikilink">UNIVAC 1107</a></p></td>
</tr>
<tr class="odd">
<td><p>Chinese Algol</p></td>
<td><p>1972年</p></td>
<td></td>
<td><p>中国</p></td>
<td><p>漢字を表示可能</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/:en:DG/L" title="wikilink">DG/L</a></p></td>
<td><p>1972年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/データゼネラル" title="wikilink">データゼネラル</a></p></td>
<td><p>アメリカ</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Eclipse_(コンピュータ)" title="wikilink">Eclipseファミリ</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/:en:S-algol" title="wikilink">S-algol</a></p></td>
<td><p>1979年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Ron_Morrison" title="wikilink">Ron Morrison</a></p></td>
<td><p>イギリス</p></td>
<td><p>直交データ型を追加。教育向け</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PDP-11" title="wikilink">PDP-11</a>（後に <a href="../Page/Java仮想マシン.md" title="wikilink">Java VM</a> 上にも実装）</p></td>
</tr>
</tbody>
</table>

## 特徴

同時期の 、 と比べると、これらの言語が特定のハードウェア上で特定の目的を効率良くこなすための一種のドメイン特化型言語から始まったのに対し、 はいったんハードウェアの特性は置いておき、抽象的なアルゴリズムを手続きとして記述する事を目指している。初期の  60 仕様では入出力手続きすら標準化されていなかった点から見ても、できる限り言語コアの抽象度を上げようとしていたことは想像に難くない。、 が直系子孫以外に余り枝分かれをしていないのに対して、 系が大きな多様性を獲得したのもこの抽象性による所が大と言える。従って  の策定をもって、ソフトウェアのモジュール化、計算機の汎用化が始まった瞬間と捉えても差し支えないであろう。

60 は、[手続き型言語](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")として[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")が可能な初めてのプログラミング言語である。

公式の  60 では[入出力](https://ja.wikipedia.org/wiki/入出力 "wikilink")機能が定義されていなかったため、実際の処理系ではそれぞれに互換性のない方法で実装された。それに対して、 68では `transput`\[21\]のための豊富な[ライブラリ](../Page/ライブラリ.md "wikilink")が提供された。

60 では[引数](https://ja.wikipedia.org/wiki/引数 "wikilink")渡しに2種類の[評価戦略](https://ja.wikipedia.org/wiki/評価戦略 "wikilink")が定義されている。一般的な**値渡し**と  に特徴的な\[22\]**名前渡し**である。名前渡しは実際のところ、手続き型言語では扱いがかなり難しい。例えば、2つの引数の値を入れ替える手続きを書いたとき、ある整数変数とその整数変数を添え字とする配列要素をその引数として渡すことができない\[23\]。すなわち swap(i, A\[i\]) という場合である（詳しくは[引数\#名前渡し](https://ja.wikipedia.org/wiki/引数#名前渡し "wikilink")を参照）。乱数関数を渡す場合にも問題が生じる。

しかし、ALGOLの設計者は名前渡しをデフォルトとした。また、言語処理系実装者たちは名前渡しの実現に「サンク」（[:en:Thunk (functional programming)](https://ja.wikipedia.org/wiki/:en:Thunk_\(functional_programming\) "wikilink")）という興味深い技法を編み出した。現在、素朴な（ALGOLのような）名前渡しは完全に廃れたが、サンクは[遅延（非正格）評価を実装する一般的な手法として知られる](https://ja.wikipedia.org/wiki/遅延評価 "wikilink")。[ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink")は処理系が「[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")と非局所的参照」を正しく実装しているかを評価するman or boy test（[:en:Man or boy test](https://ja.wikipedia.org/wiki/:en:Man_or_boy_test "wikilink")）を考案した。このテストには名前呼び出しの例が含まれている（クヌースらは他にも、名前渡しの「悪用」とでも言うべきJensen's Device（[:en:Jensen's Device](https://ja.wikipedia.org/wiki/:en:Jensen's_Device "wikilink")）と後に呼ばれるようになるような技法の一例を示した "ALGOL 60 Confidential"\[24\]など、仕様のコーナーケースを暴き、コンピュータ・プログラミング言語設計の難しさをあらわにした）。

の影響として、後の言語のうちの最も多くに影響があるものは、`BEGIN`/`END`（C 言語などでは`{` `}`）の[入れ子によるブロック構造化](https://ja.wikipedia.org/wiki/ネスティング "wikilink")、つまり次のような典型的な形の記法であろう。

```
 BEGIN
   X := 1 ;
   IF (X > 0) THEN
     BEGIN
       :
     END
 END
```

俗に「 文法」といった場合は、このブロック構造化記法のことを指していることがある（C言語のように他の記号を使うものも含めて指していることもあれば、そうではなくてBEGIN/ENDのようにキーワードを使う、という意味で言っていることもある）。 後の[静的スコープ](https://ja.wikipedia.org/wiki/静的スコープ "wikilink")の言語についても、ALGOLからの影響と言われることがある。

## 例と移植性問題

### コード例の比較

#### ALGOL 60

次のコードは  60 で `n × m` の2次元配列の中から絶対値が最大の要素を求め、その絶対値を`y`に、添え字を`i`と`k`に格納する手続きを記述したものである。なお、コード中で強調表示されている[予約語](../Page/予約語.md "wikilink")の記法は処理系に依存する。例えば "INTEGER" は "integer" と書かれることもある（）。

```
 PROCEDURE Absmax(a) Size:(n, m) Result:(y) Subscripts:(i, k) ;
     VALUE n, m ; ARRAY a ; INTEGER n, m, i, k ; REAL y ;
 COMMENT The absolute greatest element of the matrix a, of size n by m
     is transferred to y, and the subscripts of this element to i and k ;
 BEGIN
     INTEGER p, q ;
     y := 0 ; i := k := 1 ;
     FOR p := 1 STEP 1 UNTIL n DO
         FOR q := 1 STEP 1 UNTIL m DO
             IF abs (a[p, q]) > y THEN
                 BEGIN
                     y := abs (a[p, q]) ;
                     i := p; k := q
                 END
 END Absmax
```

次の例は Elliott 803 ALGOL\[25\] で表を生成する方法を示したものである。

` FLOATING POINT ALGOL TEST'`
` BEGIN REAL A,B,C,D'`
` `
` READ D'`
` `
` FOR A:= 0.0 STEP D UNTIL 6.3 DO`
` BEGIN`
`   PRINT PUNCH(3),££L??'`
`   B := SIN(A)'`
`   C := COS(A)'`
`   PRINT PUNCH(3),SAMELINE,ALIGNED(1,6),A,B,C'`
` END'`
` END'`

PUNCH(3) は紙テープのさん孔装置ではなくテレタイプ端末のプリンターへ出力を送るものである。SAMELINE は引数間で通常行われる復帰改行を抑制する。ALIGNED(1,6) は出力を小数点以上を1文字、小数点以下を6文字とするようフォーマットする。

#### ALGOL 68

次のコード例は上掲の ALGOL 60 のコード例の ALGOL 68 版である。

ALGOL 68 でも ALGOL 60 のを再利用している。

```
 PROC ABS max = ([,]real a, REF real y, REF int i, k)real:
 COMMENT The absolute greatest element of the matrix a, of size ⌈a by 2⌈a
 is transferred to y, and the subscripts of this element to i and k; COMMENT
 BEGIN
    real y := 0; i := ⌊a; k := 2⌊a;
    FOR p FROM ⌊a TO ⌈a DO
      FOR q FROM 2⌊a TO 2⌈a DO
        IF ABS a[p, q] > y THEN
            y := ABS a[p, q];
            i := p; k := q
        FI
      OD
    OD;
    y
 END # abs max #
```

なお、lower (⌊) と upper (⌈) は配列の境界を示し、配列を走査する際の添え字の範囲指定に使える。

```
 floating point algol68 test:
 (
   real a,b,c,d;

   printf(($pg$,"Enter d:"));
   read(d);

   FOR step FROM 0 WHILE a:=step*d; a <= 2*pi DO
     printf($l$);
     b := sin(a);
     c := cos(a);
     printf(($z-d.6d$,a,b,c))
   OD
 )
```

*printf* はファイル *stand out* に出力を送る。*printf($p$);* は改頁、*printf($l$);* は改行である。*printf(($z-d.6d$,a,b,c))* は小数点以上を1桁、小数点以下を6桁にフォーマットして出力する。

### Hello world の変遷

ALGOLの各種実装における移植性の無さは、[Hello World](https://ja.wikipedia.org/wiki/Hello_World "wikilink") プログラムで簡単に示すことができる。

#### ALGOL 58 (IAL)

ALGOL 58 には入出力機能が存在しないので、例示できない。

#### ALGOL 60 ファミリ

ALGOL 60 にも入出力機能がないので、Hello World プログラムの移植性はない。以下に示すのは[ユニシス](https://ja.wikipedia.org/wiki/ユニシス "wikilink")のメインフレームで今も使用可能なALGOLの実装に対応したもので、[ミシガン大学](https://ja.wikipedia.org/wiki/ミシガン大学 "wikilink")の [The Language Guide](http://www.engin.umd.umich.edu/CIS/course.des/cis400/index.html) にあるコード例を単純化したものである\[26\]。

```
 BEGIN
   FILE F(KIND=REMOTE);
   EBCDIC ARRAY E[0:11];
   REPLACE E BY "HELLO WORLD!";
   WRITE(F, *, E);
 END.
```

インラインフォーマットを使ったさらに単純なプログラムは次のようになる。

```
 BEGIN
   FILE F(KIND=REMOTE);
   WRITE(F, <"HELLO WORLD!">);
 END.
```

Display文を使うとさらに次のように単純化される。

```
 BEGIN DISPLAY("HELLO WORLD!") END.
```

もう1つの例として Elliott Algol のコード例を示す。Elliott Algol は引用開始符号と引用終了符号とで異なる文字を使用する。

` `**`program`**` HiFolks;`
` `**`begin`**
`    `**`print`**` ‘Hello world’;`
` `**`end`**`;`

次は Elliott 803 Algol (A104) の例である。Elliott 803 は標準では5孔の紙テープを使用するので、大文字しか使えない。引用符として使える文字もないため、ポンド記号 (£) を引用開始、疑問符 (?) を引用終了に使用している。特殊シーケンスは二重引用内に置かれる（例えば、££L?? は改行指示である）。

`  HIFOLKS'`
`  BEGIN`
`     PRINT £HELLO WORLD£L??'`
`  END'`

[ICT 1900シリーズのALGOLでは](https://ja.wikipedia.org/wiki/:en:ICT_1900_series "wikilink")、紙テープまたはパンチカードを入力として利用可能である。紙テープは小文字も使用可能である。出力はラインプリンターに対して行う。

`  'BEGIN'`
`     'WRITE TEXT'("HELLO WORLD");`
`  'END'`

#### ALGOL 68

ALGOL 68 のコードは一般に太字または下線つきの小文字で予約語を表す（ただし、以下の例はシンタックスハイライトのために大文字にしている）。

```
 BEGIN
   printf(($gl$,"Hello, world!"))
 END
```

"Algol 68 Report" では、入出力を "transput" と称している。

### ALGOLの特殊文字の変遷

ALGOLは文字セットが急速に発展し多様化していた時代に登場した。また、ALGOLは大文字だけで記述できるよう定義されていた。

1960年の[情報処理国際連合](https://ja.wikipedia.org/wiki/情報処理国際連合 "wikilink") (IFIP) で発表された ALGOL 60 では、当時のほとんどのコンピュータではサポートされていない数学記号がいくつか使われていた。例えば、×, ÷, ≤, ≥, ≠, ¬, ∨, ∧, ⊂, ≡, ␣, <span style="font-family:'DejaVu Sans',Quivira,Symbola,'和田研中丸ゴシック2004絵文字','和田研細丸ゴシック2004絵文字','Nishiki-teki';">⏨</span>\[27\] などである。

1961年9月、初期の[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")文字セットが登場し、ALGOLの[ブーリアン演算子](https://ja.wikipedia.org/wiki/ブーリアン型 "wikilink") "/" と "/" をサポートするために[バックスラッシュ](https://ja.wikipedia.org/wiki/バックスラッシュ "wikilink") () が初期段階で追加された\[28\]。

1962年、は2つの珍しい文字、"᛭" (iron/runic cross) と "⏨" ([Decimal Exponent Symbol](https://unicode.org/charts/PDF/U2300.pdf)) を浮動小数点形式で使用するためにALGOLの文字セットに加えた\[29\]\[30\]\[31\]。

1964年、ソビエト連邦が策定した[GOST規格](https://ja.wikipedia.org/wiki/GOST規格 "wikilink") [GOST 10859](https://ja.wikipedia.org/wiki/:en:GOST_10859 "wikilink") で、ALGOL用の4ビット、5ビット、6ビット、7ビットの文字セットを定義した\[32\]。

1968年の "Algol 68 Report" では既存のALGOL用文字セットに加えて、[IBM 2741](https://ja.wikipedia.org/wiki/:en:IBM_2741 "wikilink") 端末（1965年に登場した[APL](https://ja.wikipedia.org/wiki/APL "wikilink")対応端末）で使用可能な  という文字を加えた。このレポートはロシア語、ドイツ語、フランス語、ブルガリア語に翻訳され、それぞれの言語向けに文字セットが拡張された。例えばソビエト連邦の[BESM](https://ja.wikipedia.org/wiki/BESM "wikilink")-4は[キリル文字](../Page/キリル文字.md "wikilink")が使用可能だった。ALGOLの使用する全ての文字は[Unicode](../Page/Unicode.md "wikilink")規格の一部になっており、その大部分は主要な[フォント](../Page/フォント.md "wikilink")が対応している。

2009年10月、浮動小数点形式記述のための "<span style="font-family:'DejaVu Sans',Quivira,Symbola,'和田研中丸ゴシック2004絵文字','和田研細丸ゴシック2004絵文字','Nishiki-teki';">⏨</span>" ([Decimal Exponent Symbol](https://unicode.org/charts/PDF/U2300.pdf)) が Unicode 5.2 に追加された\[33\]。これは[ブランで使われたALGOLソフトウェアとの後方互換を保つためである](https://ja.wikipedia.org/wiki/ブラン_\(オービタ\) "wikilink")。

## 脚注

## 出典

## 参考文献

  - F.L. Bauer, R. Baumann, M. Feliciano, K. Samelson, *Introduction to Algol*. Prentice Hall, 1964, ISBN 0-13-477828-6
  - [B. Randell and L.J. Russell, *ALGOL 60 Implementation: The Translation and Use of ALGOL 60 Programs on a Computer*. Academic Press, 1964](http://www.softwarepreservation.org/projects/ALGOL/book/Randell_ALGOL_60_Implementation_1964.pdf). The design of the **Whetstone Compiler**. コンパイラの実装についての初期の解説の1つ。関連する論文として次がある。
      - [Whetstone Algol Revisited](http://www.cs.ncl.ac.uk/research/pubs/articles/papers/427.pdf) by B. Randell
      - [The Whetstone KDF9 Algol Translator](http://www.cs.ncl.ac.uk/publications/books/papers/124.pdf) by B. Randell
  - E. W, Dijkstra, *Algol 60 translation: an algol 60 translator for the x1 and making a translator for algol 60*, report MR 35/61. Mathematisch Centrum, Amsterdam, 1961. [1](http://www.cs.utexas.edu/users/EWD/MCReps/MR35.PDF)

## 関連図書

  - 森口繁一（編）：「ＡＬＧＯＬ入門」、日本科学技術連盟、（1962年10月1日）。
  - Eric Foxley and Henry R. Neave:"A FIRST COURCE IN ALGOL60", Addison-Wesley Pub., (1968).
  - エリック フォクスレイ、ヘンリイ Ｒ．ニーヴ、岸田孝一（訳）：「プログラミングＡＬＧＯＬ入門」、日本生産性本部（1970年3月30日）。

## 関連項目

  - [ISWIM](https://ja.wikipedia.org/wiki/ISWIM "wikilink")
  - [Simula](../Page/Simula.md "wikilink")
  - [Scheme](../Page/Scheme.md "wikilink")

## 外部リンク

  - [Algol 68 Genie](http://www.xs4all.nl/~jmvdveer/algol.html) - [GPL配布によるフリーの](../Page/GNU_General_Public_License.md "wikilink") 68 [インタプリタ](../Page/インタプリタ.md "wikilink")
  - [](http://www.angelfire.com/biz/rhaminisys/algol60.html) - [MS-DOS](../Page/MS-DOS.md "wikilink")上で動くフリーのALGOL60コンパイラが配布されている。
  - [](http://www.masswerk.at/algol60/report.htm) by Peter Naur, et al. ALGOLの定義
  - [Execute ALGOL-68 Script Online](http://www.compileonline.com/execute_algol_online.php) ブラウザ上でオンラインで ALGOL 68 を実行 by Mohtashim
  - ALGOL 60 のBNFによる [syntax summary](http://bernhard.userweb.mwn.de/Algol-BNF.html)
  - [History of ALGOL](http://www.softwarepreservation.org/projects/ALGOL/) at the [Computer History Museum](https://ja.wikipedia.org/wiki/コンピュータ歴史博物館 "wikilink")
  - [MARST](http://www.gnu.org/software/marst/) - フリーなALGOLからCへのトランスレータ ([User Guide](http://www.sfr-fresh.com/unix/misc/marst-2.6.tar.gz:a/marst-2.6/doc/marst.texi))
  - [AN IMPLEMENTATION OF ALGOL 60 FOR THE FP6000](http://rogerdmoore.ca/JOUR/) 実装上の問題についての議論がある。
  - ["The European Side of the Last Phase of the Development of ALGOL 60" by Peter Naur](http://portal.acm.org/ft_gateway.cfm?id=808370&type=pdf&coll=&dl=ACM&CFID=15151515&CFTOKEN=6184618)
  - [エリック・レイモンド](../Page/エリック・レイモンド.md "wikilink")の [Retrocomputing Museum](http://www.catb.org/retro/) には、C言語で書かれた NASE Algol-60 インタプリタへのリンクがある。
  - [STORIES ABOUT THE B5000 AND PEOPLE WHO WERE THERE](http://ed-thelen.org/comp-hist/B5000-AlgolRWaychoff.html) By Richard Waychoff
  - [TrueType font containing U+23E8 Decimal Exponent Symbol](http://mailcom.com/unicode/DecimalExponent.ttf)（ttfファイル）

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.  ファミリー名は大文字/小文字をまじえて表記される場合 ([*Algol 60*](http://www.masswerk.at/algol60/report.htm)) と、全て大文字で表記される場合 (*ALGOL 68*) がある。本項目では *ALGOL* で統一する。
2.  [*Collected Algorithms of the ACM*](http://calgo.acm.org/) [ACMによるアルゴリズム集](../Page/Association_for_Computing_Machinery.md "wikilink")
3.
4.  Lisp以外としては
5.  FORTRANにはそのような構造は無い。COBOLではピリオドで全ての入れ子が終端するという仕様だったため（現在は`end-if`などを使う）、入れ子で書ける論理に制限があり、酷いバグの原因にもなりやすかった。
6.
7.
8.
9.
10.
11. [ACM Award Citation / Peter Naur](http://awards.acm.org/citation.cfm?id=1024454&srt=all&aw=140&ao=AMTURING&yr=2005), 2005
12. ["Hints on Programming Language Design"](http://www.eecs.umich.edu/~bchandra/courses/papers/Hoare_Hints.pdf), C.A.R. Hoare, December 1973. Page 27. （なお、この言葉は間違って[エドガー・ダイクストラ](../Page/エドガー・ダイクストラ.md "wikilink")のものとされることがある。ダイクストラも ALGOL 60 [コンパイラ](../Page/コンパイラ.md "wikilink")の実装に参加していた）
13. ALGOL自身（ALGOL 60）にはFUNARG問題（[:en:Funarg problem](https://ja.wikipedia.org/wiki/:en:Funarg_problem "wikilink")）などは無いため、静的スコープにまつわる難しい点などもないことから、強い関連を求めるならばおそらくALGOL 68になる。
14.
15. Peter O'Hearn and Robert D. Tennent. 1996. Algol-Like Languages. Birkhauser Boston Inc., Cambridge, MA, USA.
16.
17. [Computer Museum History](http://www.computerhistory.org/core/backissues/pdf/core_1_1.pdf), Historical Zuse-Computer Z23, restored by the Konrad Zuse Schule in Hünfeld, for the Computer Museum History Center in Mountain View (California) USA
18.
19.
20.
21.  68 の用語で入出力を意味する。
22. 手続き型言語ではなく、理論的に純粋なラムダ計算などであれば「値渡し」と「名前渡し」は基本的には等価である（ので、設計者たちは楽観的に考えていたのかもしれない）。しかし、手続き型言語では色々と面倒があり、その後、「参照渡し」か、[無名関数](https://ja.wikipedia.org/wiki/無名関数 "wikilink")を「[第一級関数](https://ja.wikipedia.org/wiki/第一級関数 "wikilink")」として渡す、という形に整理された（この2通りが、名前渡しが必要・有用な場合のほとんどのユースケースである）。
23. , Section 7.5, and references therein
24. <https://doi.org/10.1145/366573.366599>
25. ["803 ALGOL"](http://www.billp.org/ccs/A104/), the manual for Elliott 803 ALGOL
26. [Hello world\! ALGOL Example Program page](http://www.engin.umd.umich.edu/CIS/course.des/cis400/algol/hworld.html)
27. 対応フォントが少ない。フリーフォントでは、[DejaVu Sans](https://ja.wikipedia.org/wiki/DejaVuフォント "wikilink")、Quivira、[Symbola](http://users.teilar.gr/~g1951d/)、[和田研2004フォントの絵文字対応版](https://ja.wikipedia.org/wiki/和田研フォント "wikilink")、にしき的フォントなど。JIS X 0208の表記に置き換えるなら「<span style="font-size:40%;">10</span>」のような外見となる。
28. [How ASCII Got Its Backslash](http://www.bobbemer.com/BACSLASH.HTM), Bob Bemer
29.
30.
31.
32.
33.