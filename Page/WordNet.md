> この記事は[WordNet](https://ja.wikipedia.org/wiki/WordNet)から翻訳されています。


**WordNet**（ワードネット）は[英語](../Page/英語.md "wikilink")の[概念辞書](https://ja.wikipedia.org/wiki/概念辞書 "wikilink")（[意味辞書](https://ja.wikipedia.org/wiki/意味辞書 "wikilink")）である。WordNetでは英単語が**synset**と呼ばれる[同義語](https://ja.wikipedia.org/wiki/同義語 "wikilink")のグループに分類され、簡単な 定義や、他の同義語のグループとの関係が記述されている。 WordNetの目的は直感的に使うことのできる[辞書](https://ja.wikipedia.org/wiki/辞書 "wikilink")と[シソーラス](../Page/シソーラス.md "wikilink")が組み合わされた成果物を作ること、および自動的文書解析や人工知能のアプリケーションの実現を支援することにある。WordNetのデータベースやソフトウェアは[BSDライセンス](../Page/BSDライセンス.md "wikilink")によって公開され、自由にダウンロードして用いることができる。データベースはオンラインで参照することもできる。

WordNetは[プリンストン大学](https://ja.wikipedia.org/wiki/プリンストン大学 "wikilink")の[認知科学](../Page/認知科学.md "wikilink")研究所によって[心理学者](../Page/心理学者.md "wikilink")である同大学[教授](../Page/教授.md "wikilink")の[ジョージ・ミラー](../Page/ジョージ・ミラー_\(心理学者\).md "wikilink")(George A. Miller)の主導のもとで運営されている。開発は[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に始められ、この間、主に[機械翻訳](../Page/機械翻訳.md "wikilink")に取り組む米国の政府機関から3百万ドルの支援を受けた。

## データベースの内容

[2005年](../Page/2005年.md "wikilink")現在、WordNetのデータベースは約11万5000のsynsetに分類された約15万語を収録し、全体で20万3000の単語と意味の組み合わせがある。データベースは圧縮された状態で約12[メガバイト](../Page/メガバイト.md "wikilink")のサイズがある。

WordNetでは名詞、動詞、形容詞、副詞を文法上の扱いが異なることから、区別して収蔵している。synsetは同義の単語あるいはコロケーション（[熟語](../Page/熟語.md "wikilink")、[連語](https://ja.wikipedia.org/wiki/連語 "wikilink"); コロケーションとは"car pool"のように単語が連なって一つの意味をなしている句）をグループにまとめている。

意味の異なる語句は別のsynsetに分類される。synsetの持つ意味は注釈として以下のような形式で記載されている。（訳注：synsetに属する単語がgood, right, ripeであり、注釈は括弧の中に記載されている。）

  -
    good, right, ripe -- (most suitable or right for a particular purpose; "a good time to plant tomatoes"; "the right time to act"; "the time is ripe for great sociological changes")

ほとんどのsynsetは他のsynsetとの意味的な関係が番号によって示されている。この関係の種類は品詞によって異なっており、以下に示す通りになっている。

  - 名詞
      - **[上位語](https://ja.wikipedia.org/wiki/上位語 "wikilink")(hypernym)**: すべての**X**が**Y**の種類の一であるなら**Y**は**X**の上位語である。
      - **[下位語](https://ja.wikipedia.org/wiki/下位語 "wikilink")(hyponym)**: すべての**Y**が**X**の種類の一であるなら**Y**は**X**の下位語である。
      - **同族語(coordinate term)**: **X**と**Y**の上位語が同じなら、**Y**は**X**の同族語である。
      - **[全体語](https://ja.wikipedia.org/wiki/全体語 "wikilink")(holonym)**: **X**が**Y**の一部であるなら、**Y**は**X**のholonymである。
      - **[部分語](https://ja.wikipedia.org/wiki/部分語 "wikilink")(meronym)**: **Y**が**X**の一部であるなら、**Y**は**X**のmeronymである。
  - 動詞
      - **[上位語](https://ja.wikipedia.org/wiki/上位語 "wikilink")(hypernym)**: **X**という行動が**Y**の種類の一であるなら動詞**Y**は動詞**X**の上位語である。 （「移動(movement)」は「旅行(travel)」の上位語）
      - **[トロポニム](https://ja.wikipedia.org/wiki/トロポニム "wikilink")(troponym)**: もし**Y**という行動が**X**を行う際の様態であるなら動詞**Y**は動詞**X**のtroponymである。（「片言で話す(lisp)」は「話す(talk)」のtroponym）
      - **[含意](../Page/論理的帰結.md "wikilink")(entailment)**: **X**している場合必然的に**Y**しているなら動詞**Y**は動詞**X**にentail（ひきおこすこと）されている。 （X:「いびきをかく(snoring)」はY:眠る(sleeping)」ことによって引きおこされる。）
      - **同族語(coordinate terms)**: **X**と**Y**の上位語が同じなら、**Y**は**X**の同族語である。
  - 形容詞
      - **関係のある名詞**
      - **動詞の分詞**
  - 副詞
      - **原形の形容詞**

synsetに含まれる語句は同じ意味を持った同義語であるため意味的な関係はsynset内全体に適用されるが、 単独の語句が他の語句と[反意語](https://ja.wikipedia.org/wiki/反意語 "wikilink")や[派生語](https://ja.wikipedia.org/wiki/派生語 "wikilink")などの関係を結ぶこともある。

WordNetには語句の多義性の度合い（polysemy count; 語句が属するsynsetの数）の情報も含まれている。ある単語がいくつかのsynsetに属している（いくつかの意味を持っている）場合、ある意味は他の意味よりも一般的に用いられているという関係を持っていることが多い。WordNetではこのような関係を**頻度点**(frequency score)と呼ぶ数値で表している。サンプルの文書の中には全ての単語にsynset等の意味を表すタグを付与しているものがあり、単語が特定の意味で出現している頻度によって頻度点が計算されている。

単語から語幹（root form）や原型（lemma）を推定するための形態素解析ツールはデータベースと一緒に配布されている。屈折形を含む語の場合をのぞいて語幹のみがデータベースに格納されている。

## 知識構造

名詞と動詞は上位・下位の関係（IS Aの関係）によって定義される階層構造にまとめられている。たとえば**dog**の第一義は以下のような上位語階層を持っている。 同じ階層にある単語はそれぞれ同義語の関係にある。**dog**の示すある意味の同義語には*domestic dog*や*Canis familiaris*がある。 同義語のグループ(synset)は一意の索引によってポイントされ、同じ属性や注釈を持っている。

`dog, domestic dog, Canis familiaris`
`=> canine, canid`
`=> carnivore`
`=> placental, placental mammal, eutherian, eutherian mammal`
`=> mammal`
`=> vertebrate, craniate`
`=> chordate`
`=> animal, animate being, beast, brute, creature, fauna`
`=> ...`

階層の頂点ではこの階層構造は25の名詞の基礎グループと15の動詞の基礎グループにまとめられている。このグループが編集用のファイル一つにそれぞれ対応している。この基礎グループは、WordNetを利用するアプリケーションが抽象的な[ルート](../Page/ルート.md "wikilink")[ノード](https://ja.wikipedia.org/wiki/ノード "wikilink")として用いるノードに対応している。

形容詞の場合、二つの反対する主要な意味が極となって、その他の同義語が形容詞の場合における同義性の関係によって極を取り囲む形をとっている。したがって階層構造や編集用のファイルは名詞や動詞の場合と異なった構造をとっている。

名詞のネットワーク構造は他の品詞と比べてはるかに深い構造を持っており、動詞は他の品詞よりもはるかに入り組んだ構造をしている。 形容詞ははっきり区別された別々の固まりに組織されており、副詞はそれぞれの語が由来する形容詞に従って定義されており、形容詞と似た構造をとっている。

## 心理学的な正当性

WordNetの目的は、人間が言語を処理する方法について年月をかけて得られた知見と一致するシステムを開発することだった。 例えば[失語症](../Page/失語症.md "wikilink")は患者が物の名前を思い出すのを選択的に（該当する物とそうでない物が入り交じって）妨げる状況を作り出すということが分かっている。 そのため、品詞をはっきりした階層構造へ分類する、より理にかなった分類方法が採られた。

下位語の場合、 人間が名詞の属性を見つけることのできる早さは、その特徴を定義している階層を見つける早さに依存していることが心理学実験で明らかになっている。 したがってカナリアは鳴き鳥の一種である（直下の下位語となっている）ため、人は「カナリアは歌う」かどうかをすぐに判断することができるが、 「カナリアは飛ぶ」かどうかを判断するにはもう少し時間がかかり（二層の隔たりがある）、「カナリアは皮膚を持っている」かどうかを判断するにはより多くの時間を要する（複数の階層の隔たりがある）。これは、人間はある概念と他の似た概念を区別するのに必要なもっとも明確な情報のみを保持していることから、 人間がWordNetに似た方法で意味の情報を記憶しているということを示唆している。

## 制限事項

他の辞書とは異なり、語源に関する情報はWordNetに含まれていない。発音や不規則動詞についての説明はごく簡単なものにとどまっている。

辞書編集上の意味の情報は編集用のファイルにおいて管理されており、grind と呼ばれるツールによって配布用のデータベースを生成する処理が行われている。 grind と編集用のファイルも自由に利用することができるが、それでもデータベースの変更を行うことは難しい。

WordNetでは似た意味の単語を単一の一般的な定義によるsynsetにまとめているため、個々の単語の定義は必ずしも正確ではない。

## 関連するプロジェクト

[EuroWordNet](https://ja.wikipedia.org/wiki/EuroWordNet "wikilink")プロジェクトはそれぞれ相互にリンクされたヨーロッパの言語のWordNetを開発しているが、フリーのライセンスで利用することはできない。[Global Wordnetプロジェクトは](https://ja.wikipedia.org/wiki/Global_Wordnet "wikilink") 全ての言語WordNetを接続し、統合を行おうとしているプロジェクトである。[オックスフォード英語辞典](../Page/オックスフォード英語辞典.md "wikilink")(Oxford English Dictionary)の出版社の[オックスフォード大学](../Page/オックスフォード大学.md "wikilink")出版は独自のWordNetをオンライン上で構築することを発表している。 2009年には日本語WordNetが英語WordNetと同じライセンスで公開された。\[1\]

[eXtended WordNetは](https://ja.wikipedia.org/wiki/eXtended_WordNet "wikilink")[テキサス大学ダラス校](https://ja.wikipedia.org/wiki/テキサス大学ダラス校 "wikilink")のプロジェクトである。WordNetの注釈を意味的に解析し、定義に含まれる情報を知識処理システムで利用可能とすることでWordNetを改良することをねらっている 。eXtended WordNetはWordNetと似たライセンスで自由に利用することができる。

[GCIDE](https://ja.wikipedia.org/wiki/GCIDE "wikilink")プロジェクトは[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")の[1913年](../Page/1913年.md "wikilink")版の[ウェブスター辞典](https://ja.wikipedia.org/wiki/ウェブスター辞典 "wikilink")をWordNetの単語の定義およびボランティアによって提供された情報と組み合わせた辞書を作成している。これは[コピーレフト](../Page/コピーレフト.md "wikilink")ライセンスの[GPLで公開されている](../Page/GNU_General_Public_License.md "wikilink")。

名詞のsynset間の上位語・下位語の関係は概念のカテゴリ同士の特化した関係として理解することができる。 言い換えれば、WordNetは[情報科学](https://ja.wikipedia.org/wiki/情報科学 "wikilink")における意味での、語彙の[オントロジー](../Page/オントロジー.md "wikilink")として用いることができる。 しかし、こうしたオントロジーは非常に多くの意味的な不整合、たとえば、(1)排他的なカテゴリ付けを行うために多数の語句をまとめて限定的な意味を付与していることや(2)意味付けの階層構造に冗長性があるため、通常、使用される前に修正が行われる。

さらに、WordNetを知識表現に利用可能なオントロジーに変換するには、通常 (1) WordNet上で行われている意味付けをsubtypeOfとinstanceOfの関係に区別して記述することと、 (2) 一意の識別子をそれぞれのカテゴリに関連づけることを必要とする。 このような修正と変換は[integration of WordNet 1.7 into the cooperatively updatable knowledge base of WebKB-2](http://www.webkb.org/doc/wn/)に記されている例があるが、ほとんどのプロジェクトはWordNetを知識処理アプリケーション（知識情報処理による情報検索等）に再利用する場合には単純にWordNetそのものを利用する方法を採っている。

WordNetはWordNetのカテゴリと他のオントロジーに由来するカテゴリとの写像にも広く利用されている。 たいていの場合、WordNetの最上位レベルのカテゴリのみが写像に用いられるが、オントロジー[SUMOの作者は](https://ja.wikipedia.org/wiki/Suggested_Upper_Merged_Ontology "wikilink") WordNetのsynset（名詞、動詞、形容詞、副詞）と[SUMO classとの写像を作成した](https://ja.wikipedia.org/wiki/SUMO_class "wikilink")。 [2006年](../Page/2006年.md "wikilink")現在の写像はSUMOを拡張したMId-Level Ontology (MILO)の特定の用語へのより多くのリンクを提供している。 [OpenCyc](https://ja.wikipedia.org/wiki/OpenCyc "wikilink")の上層のオントロジーにはWordNetのノードにリンクが設定されている。

WordNetをオントロジーに組み込もうとしている多くのプロジェクトでは、WordNetの内容は意味的な不整合の問題が起きた場合に単純に訂正されるのではなく、 WordNetを発想の種として使ってきたが、必要があるときには大規模に書き換えて用いている。 たとえば、[OntoClean](https://ja.wikipedia.org/wiki/OntoClean "wikilink")を基盤にしたアプローチによって[WordNetの最上位のオントロジーが再構築された例](http://citeseer.ist.psu.edu/oltramari02restructuring.html)やSENSUSオントロジーの下位の分類を構築するのにWordNetを出発点のソースとして用いた例などがある。

[FrameNet](https://ja.wikipedia.org/wiki/FrameNet "wikilink")はWordNetに近いプロジェクトである。10万以上の文に加えられた意味的な属性の注釈をもとにした語彙集であり、ねらいとなっている単位は、語彙フレーム(lexical frame)である。語彙フレームとは語句に関連づけられた属性に加えて、状態あるいは事象の種類（訳注:フレームについては\[[http://c1105067.uniblogs.org/2006/06/09/%e3%83%95%e3%83%ac%e3%83%bc%e3%83%a0/\]などが参考になる](http://c1105067.uniblogs.org/2006/06/09/%e3%83%95%e3%83%ac%e3%83%bc%e3%83%a0/%5Dなどが参考になる)。）を表したものである。

## 参考文献

  - [\`\`Five Papers on WordNet''](ftp://ftp.cogsci.princeton.edu/pub/wordnet/5papers.ps) by Miller, George A., Christiane Fellbaum, Katherine J. Miller. August, 1993, retrieved May 4, 2005

<references/>

## 関連項目

  - [Semantic Web](https://ja.wikipedia.org/wiki/Semantic_Web "wikilink")
  - [分類学](../Page/分類学.md "wikilink")
  - [Synonym Ring](https://ja.wikipedia.org/wiki/Synonym_Ring "wikilink")

## 外部リンク

  - [The WordNet Home Page](http://wordnet.princeton.edu/)
  - [WordNet 2.0 - Dictionary & Thesaurus](http://www.vector.co.jp/soft/data/writing/se323658.html) - ベクター社によってホストされているWordNet2.0の[EPWING](../Page/EPWING.md "wikilink")電子辞書
  - [Wordnet Related Projects](http://wordnet.princeton.edu/links) - WordNetにアクセスするためのインターフェースおよび拡張機能の一覧
  - [Global Wordnet](http://www.globalwordnet.org/)
  - [The SENSUS ontology](http://www.isi.edu/natural-language/projects/ONTOLOGIES.html)
  - [日本語 WordNet](http://compling.hss.ntu.edu.sg/wnja/index.ja.html) WordNetの日本語版
  - [WordNet EPWING](http://wordnetepwing.osdn.jp/) WordNet 3.1のEPWINGデータ

[Category:辞典](https://ja.wikipedia.org/wiki/Category:辞典 "wikilink") [Category:言語資源](https://ja.wikipedia.org/wiki/Category:言語資源 "wikilink") [Category:知識表現](https://ja.wikipedia.org/wiki/Category:知識表現 "wikilink") [Category:シソーラス](https://ja.wikipedia.org/wiki/Category:シソーラス "wikilink")

1.  Hitoshi Isahara, Francis Bond, Kiyotaka Uchimoto, Masao Utiyama and Kyoko Kanzaki (2008) **[Development of Japanese WordNet](http://compling.hss.ntu.edu.sg/wnja/pubs/2008-lrec-wn-ja-isahara.pdf)**. In LREC-2008, Marrakech.