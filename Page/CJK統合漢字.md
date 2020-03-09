> この記事は[CJK](https://ja.wikipedia.org/wiki/CJK)から翻訳されています。


**CJK統合漢字**（シージェーケーとうごうかんじ、（idiographs は「[表意文字](https://ja.wikipedia.org/wiki/表意文字 "wikilink")」の意））は、[ISO/IEC 10646](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")（略称：UCS\[1\]）およびにて採用されている符号化用[漢字](../Page/漢字.md "wikilink")集合およびその符号表である。CJK統合漢字の名称は、[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")(<u>C</u>hinese)、[日本語](../Page/日本語.md "wikilink")(<u>J</u>apanese)、[朝鮮語](../Page/朝鮮語.md "wikilink")(<u>K</u>orean) で使われている漢字をひとまとめにしたことからきている。

CJK統合漢字の初版であるUnified Repertoire and Ordering第二版は1992年に制定されたが、1994年に[ベトナム](https://ja.wikipedia.org/wiki/ベトナム "wikilink")で使われていた漢字も含めることにしたため、[CJKV](https://ja.wikipedia.org/wiki/CJKV "wikilink")と呼ばれる事もある。**CJKV**は、[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")・[日本語](../Page/日本語.md "wikilink")・[朝鮮語](../Page/朝鮮語.md "wikilink")・[ベトナム語](../Page/ベトナム語.md "wikilink")(<u>V</u>ietnamese) を表す英語の頭文字である。特に、その4つの言語で共通して使われる、または使われていた[文字体系](https://ja.wikipedia.org/wiki/文字体系 "wikilink")である[漢字](../Page/漢字.md "wikilink")（[チュノム](../Page/チュノム.md "wikilink")を含む）のこと。[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[国際化](../Page/国際化と地域化.md "wikilink")、中でも[文字コード](../Page/文字コード.md "wikilink")に関する分野で用いられる。

CJK統合漢字は、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")・[中国](../Page/中華人民共和国.md "wikilink")・[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")・[北朝鮮](https://ja.wikipedia.org/wiki/朝鮮民主主義人民共和国 "wikilink")・[韓国](https://ja.wikipedia.org/wiki/大韓民国 "wikilink")・[ベトナム](https://ja.wikipedia.org/wiki/ベトナム "wikilink")の各漢字コードとの対応表も定めているが、事情によりCJK統合漢字との対応を持たない各国・各地域の漢字コードをUCSに適切に変換できるよう、互換用の領域が別途定められている。この領域の漢字は**[CJK互換漢字](https://ja.wikipedia.org/wiki/CJK互換漢字 "wikilink")**\[2\]と呼ばれる。

## 歴史

[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")、日本によって世界で最初の[ISO 2022に基づく漢字コード規格](https://ja.wikipedia.org/wiki/ISO_2022 "wikilink")[JIS C 6226が制定された](../Page/JIS_X_0208.md "wikilink")。1980年代には中国・台湾・韓国にて次々と各国・地域用の漢字コード規格が制定されていったが、これらは互いに関連性がなく、混在させて使用するには[ISO 2022のエスケープ](https://ja.wikipedia.org/wiki/ISO_2022 "wikilink")・シーケンスで漢字コード表を切り替えるしかなかった。

[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")、国会図書館の[高橋徳太郎](https://ja.wikipedia.org/wiki/高橋徳太郎 "wikilink")が主に書誌学の観点から、東アジアの統一漢字コードの必要性を指摘した。同年、台湾で制定された3バイト漢字コード規格[CCCII](https://ja.wikipedia.org/wiki/CCCII "wikilink")は、おそらく日本・中国・台湾の漢字を統一的に扱うことを目的とした最初の規格の一つである。この規格は東アジアの文献情報用にアメリカでも[ANSI Z 39.64として採用された](https://ja.wikipedia.org/wiki/ANSI_Z_39.64 "wikilink")。

[1984年](../Page/1984年.md "wikilink")、ISOの文字コード規格委員会 ([ISO/TC 97](https://ja.wikipedia.org/wiki/ISO/TC_97 "wikilink") - SC2) は文字セットの切り替えを行わずに世界中の文字を単一の文字集合として扱える文字コード規格 (ISO 10646) を作成することを決定し、専門のワークグループ (WG2) を設置した。当初、この文字コード規格は16ビットを想定し、その中に日本や中国など各国の漢字コード表をそのまま入れることを想定していた。、[1989年](../Page/1989年.md "wikilink")、各国の漢字コードを統合した漢字集合HCC\[3\]のアイデアを提案した。

[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")、完成したISO 10646の初版ドラフト ([DIS 10646](https://ja.wikipedia.org/wiki/DIS_10646 "wikilink")) では、漢字コードは32ビットで表現され、各国の漢字コードはそのまま入れることになった。しかし中国は漢字を各国でばらばらに符号化するのではなく、あくまで統一して扱うことを求めてこのドラフトには当初から反対しており、今後の漢字コードの方針を決めるため、ワークグループは[CJK-JRGと呼ばれるグループを別途設置し](https://ja.wikipedia.org/wiki/Ideographic_Rapporteur_Group "wikilink")、そこで引き続き検討することにした。

一方、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")頃から、[ゼロックス](https://ja.wikipedia.org/wiki/ゼロックス "wikilink")のジョー・ベッカー\[4\]とリー・コリンズ\[5\]は世界中の文字を統一して扱える文字コードUnicodeを開発していた。[1989年](../Page/1989年.md "wikilink")に発表されたUnicodeの概要では、その基本ポリシーとして、16ビットで全ての文字を扱えることを目指しており、そのために日本・中国・韓国の漢字を統一することとしていた。[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")にはこの方針に基づいた最終ドラフトが完成、それに賛同する企業によって、翌[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")1月には[Unicodeコンソーシアム](https://ja.wikipedia.org/wiki/Unicodeコンソーシアム "wikilink")が設立された。このドラフトでは、日本・中国・韓国の漢字の類似する漢字を統合することで2万弱の漢字コードを入れ、さらに将来の拡張用に、3万程度の漢字の空き領域が別に用意されていた。

[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")、ISO/IEC 10646の初版ドラフトはUnicodeとの一本化を求める各国により否決され、また中国およびUnicodeコンソーシアムの要請により、CJK-JRGにおいて、ISO 10646とUnicodeの一本化が図られることになった。CJK-JRGは各国の漢字コードに基づき独自の統合規準を定め、ISO 10646とUnicode用の統合漢字コード表を作成した。1991年末、この文字表はUnified Repertoire and Ordering (URO) として完成した。

[1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink")、UROを取り込んだISO 10646の二版ドラフトが完成し、賛成多数で国際規格化された。ただしUROには若干の間違いが発見されており、それらの修正が行われている。

[1993年](../Page/1993年.md "wikilink")5月、U+4E00-U+9FFFのブロックに最初のCJK統合漢字、20,902字が割り当てられたISO/IEC 10646が正式に制定され、その一ヶ月後には同じ内容を持つUnicode 1.1が制定された。

[1999年](../Page/1999年.md "wikilink")、Unicode 3.0で、ISO/IEC 10646の修正案17において、拡張漢字A集合として、U+3400-U+4DFFのブロックに6,582字が追加された\[6\]。当初は6,584文字の予定であったが、そのうち2文字が互換漢字領域にあったため、互換領域の2文字を[拡張漢字](https://ja.wikipedia.org/wiki/拡張漢字 "wikilink")A集合として扱うことにして、この2文字は追加集合からは削除された\[7\]。また、同時期に発行された修正案13において、URO漢字のうち中国に原規格がない文字に対して、GB 16500に基づく新規に原規格の割り当てが行われ\[8\]、またベトナムの文字欄が追加されCTJKVの5欄併記となった\[9\]。

[2001年](../Page/2001年.md "wikilink")、Unicode 3.1で、ISO/IEC 10646-2として、拡張漢字B集合42,711字が、U+20000-U+2A6FFのブロックに追加された。しかしながら、非常に膨大な漢字集合を極めて短期間のうちに定めたため、漢字の重複や字形の誤りが多数発生した。

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")、Unicode 4.1で、ISO/IEC 10646:2003修正案1として、[基本多言語面](https://ja.wikipedia.org/wiki/基本多言語面 "wikilink") (BMP) のU+9FA6-U+9FBBに22文字の漢字が追加されて20,924文字になった。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")、Unicode 5.1で、基本多言語面のU+9FBC-U+9FC3に8文字が追加されて20,932文字になった、

[2009年](../Page/2009年.md "wikilink")、Unicode 5.2で、拡張Cの4,149文字がU+2A700-U+2B734に、また基本多言語面でもU+9FC4-U+9FCBに8文字が追加されて20,940文字になった。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")、Unicode 6.0で、拡張Dの222文字がU+2B740-U+2B81Fに追加された。

[2012年](../Page/2012年.md "wikilink")、Unicode 6.1で、基本多言語面のU+9FCCに1文字が追加されて20,941文字になった。

[2015年](../Page/2015年.md "wikilink")、Unicode 8.0で、拡張Eの5,762文字がU+2B820-U+2CEAFに追加された。また基本多言語面でもU+9FCD-U+9FD5に9文字が追加されて20,950文字になった。

[2017年](../Page/2017年.md "wikilink")、Unicode 10.0で、拡張Fの7,473文字がU+2CEB0-U+2EBE0に追加された。また基本多言語面でもU+9FD6-U+9FEAに21文字が追加されて20,971文字になった。

[2018年](../Page/2018年.md "wikilink")、Unicode 11.0で、基本多言語面のU+9FEB-U+9FEFに5文字が追加されて20,976文字になった。

Unicode 11.0 段階での文字数は以下のとおりである（互換漢字のうち、統合漢字扱いされる12字を加えると87,887文字になる）。

| 範囲                | 名称                                 | 字数     |
| ----------------- | ---------------------------------- | ------ |
| U+4E00 - U+9FEA   | CJK Unified Ideographs             | 20,976 |
| U+3400 - U+4DFF   | CJK Unified Ideographs Extension A | 6,582  |
| U+20000 - U+2A6FF | CJK Unified Ideographs Extension B | 42,711 |
| U+2A700 - U+2B734 | CJK Unified Ideographs Extension C | 4,149  |
| U+2B740 - U+2B81F | CJK Unified Ideographs Extension D | 222    |
| U+2B820 - U+2CEAF | CJK Unified Ideographs Extension E | 5,762  |
| U+2CEB0 - U+2EBE0 | CJK Unified Ideographs Extension F | 7,473  |
| 合計                | 87,887                             |        |

## CJK統合漢字の特徴と問題点

[CJKV_variant_glyphs.png](https://ja.wikipedia.org/wiki/File:CJKV_variant_glyphs.png "fig:CJKV_variant_glyphs.png")、[簡体字](https://ja.wikipedia.org/wiki/簡体字 "wikilink")、[韓国の漢字](https://ja.wikipedia.org/wiki/韓国における漢字 "wikilink")、[ベトナムの漢字](../Page/チュノム.md "wikilink")、[日本の漢字](https://ja.wikipedia.org/wiki/日本における漢字 "wikilink")。\]\]

### 配列

原則として登録される毎に[部首](../Page/部首.md "wikilink")画数順で配列されている。但し一部に乱れが存在している上追加が相次いだために検索が困難になってきており、Unihanデータベースでは割り当てられたUnicode値と部首番号、部首別画数から導出される値をソートキーとして規格化している。

### 類似漢字の統合

漢字には「形・音・義」の3つの側面があるといわれる。CJK統合漢字は日本・中国・台湾・韓国の漢字コード表の漢字のうち由来が同一\[10\]であり、かつ字形が同一または類似するものを、一定の基準のもとに統合することにした。統合規準については、[ISO/IEC 10646の補遺Sに詳述されている](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")。由来が同一であっても国・地域によって漢字の意味や発音が大きく変化しているため、現代の各国間でも音・義が同一であるとは限らない。このため統合漢字では日本の「机」（つくえ）と中国の「」（機の簡化字）が統一されたり、現代の日本語と中国語で大きく意味が異なる「届」等の漢字に同一の符号が割り当てられている。（英語版[Han unification参照](https://ja.wikipedia.org/wiki/:en:Han_unification "wikilink")）

統合漢字は、字形が同一でなくても、「同じ抽象字形を持つ漢字」も統合することにしている。同一とされる抽象字形には、「為」と「爲」や、「単」と「」などがある。その結果、「僧」と「」、「廐」と「」、「」と「」なども同一符号化され、符号のみでは字形や画数を明確に定めることが困難である。

### 原規格分離規則

日本・中国・台湾・韓国の国内規格とUCSとの間で[ラウンドトリップ変換](https://ja.wikipedia.org/wiki/ラウンドトリップ変換 "wikilink")を実現するため、統合漢字の最初のURO 20,902文字に限り、日本・中国・台湾・韓国の国内規格で区別されている漢字は統合漢字でも必ず分離することとした。たとえばJISの間違いにより別符号化されていた「飲」と「飮」は統合漢字でもやはり分離され（他のすべての「飠」と「𩙿」の違いしかない漢字は統合されている）、また「」と「」は、「」や「」等の漢字では統合される一方、「」と「」や、「」と「」などは台湾のでは区別しているとの理由により別符号化されている。

### 統合における矛盾

CJK統合漢字は上記のような「統合原則」および「原規格分離規則」を定めたにも関わらず、これらに適合しない統合・分離の例を幾つか抱えている。

一例を挙げると、「戋」と「㦮」は統合原則では統合されることになっている。具体的にはたとえば、「」と「」や、「」と「」、「」と「」は統合漢字では同一符号である。しかしなぜか「桟」と「栈」は、日本・中国・韓国・台湾のいずれの国内規格でも区別しているものはないのに、統合漢字ではU+685FとU+6808に分離されている\[11\]。

### CNS 11643:1992規格との非互換性

UROの制定作業の直前に、台湾が[CNS 11643](https://ja.wikipedia.org/wiki/CNS_11643 "wikilink"):1992規格として、[康煕字典](https://ja.wikipedia.org/wiki/康煕字典 "wikilink")や[大漢和辞典](../Page/大漢和辞典.md "wikilink")の漢字を含む4万7千文字の漢字コードを制定した。この漢字集合は、多数の異体字を規定しているが、その異体字の中には統合漢字では統合されているものも多く含まれていた。そのため、CNS規格はUnicodeとの間でラウンドトリップ変換が不可能となった。

一例として、CNS 11643:1992では従来の「」（1面4E7E）に加えて、「」（6面2D45）を新たに規定した。しかし統合漢字では両方の字形は76F4として符号化された（「」は日本字形、「」は中国・台湾字形）。その結果、原規格分離まで行って維持しようとしたラウンドトリップ変換が、CNS 11643:1992との間では不可能となった（この問題は[2001年](../Page/2001年.md "wikilink")のISO/IEC 10646-2:2001の制定によりようやく解消された）\[12\]。

### 幽霊漢字

[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")7月にCJK-JRGは、CJK統合漢字の対象となる漢字は1991年の時点における各国・各地域で公式に制定された規格のみに限定することで合意した。これにより、日本からは[JIS X 0208](../Page/JIS_X_0208.md "wikilink"):1990、[JIS X 0212](../Page/JIS_X_0212.md "wikilink"):1990、韓国からは[KS C 5601](https://ja.wikipedia.org/wiki/KS_X_1001 "wikilink")、KS C 5657、台湾からは[CNS 11643](https://ja.wikipedia.org/wiki/CNS_11643 "wikilink"):1987、そして中国からは[GB 2312](../Page/GB_2312.md "wikilink")、GB 7589、GB 7590、GB/T 12345、GB 8565で規定されている漢字が統合の対象となった（実際にはGB 7589、GB 7590そのものではなく、それらに記載されている字体の繁体字が統合の対象として提出された）。しかし中国は、この合意では入れることのできない、[現代漢語通用字表](https://ja.wikipedia.org/wiki/現代漢語通用字表 "wikilink")やCCITT Chinese Primary Setの漢字、標準電碼本の漢字をCJK統合漢字に含めようとし、上記の規格に含まれない多数の漢字を既存の規格の空き符号位置に混入させて、統合対象の漢字として提出した。その結果、一見由来の不明な多数の[幽霊漢字](https://ja.wikipedia.org/wiki/幽霊漢字 "wikilink")が、CJK統合漢字に紛れ込むこととなった\[13\]。

### 重複漢字

CJK統合漢字の中には、全く同じ文字が複数の符号位置に重複して登録されているものや、本来統合されるはずの文字が別字として登録されているものなどが発見されている。とりわけ、拡張Bの追加の際には、かつてBMPで統合されたはずの「点なしの『器』」（U+5668で点の有無を包摂）に新たな符号位置 (U+20F96) を与えるといった、不整合な例が多数見られる\[14\]。

### 誤って統合された漢字

CJK統合漢字の中には、字形が似ているだけで統合された物が1例確認されている。拡張Aに含まれるU+4039（）がそれである。この訂正のためにCJK統合漢字U+9FC3（）にU+FAD4を割り当て直した (Unicode 5.1)。[大漢和辞典](../Page/大漢和辞典.md "wikilink")における23381番 (U+4039) と23380番 (U+FAD4 = U+9FC3) である。

  -

    ⇔ の右側が、の右側と同じ。

    U+4039 ⇔ U+9FC3

花園明朝フォントでは訂正に対応している。<span style="font-family:HanaMinA"> ⇔ </span>

### サロゲートペア

CJK統合漢字拡張B以降の拡張漢字集合は、[追加漢字面](https://ja.wikipedia.org/wiki/追加漢字面 "wikilink")に存在するため、[UTF-16](../Page/UTF-16.md "wikilink")を採用したシステムでは、Unicode 2.0で追加された[サロゲートペア（代用対）という](https://ja.wikipedia.org/wiki/Unicode#サロゲートペア "wikilink")2つの代用符号位置を組み合わせて1文字として認識させる手法を取らないと符号化できない。そのため、アプリケーションによってはいまだに対応ができていないケースがある。[JIS X 0213の漢字のうち一部はこの拡張Bに含むため](../Page/JIS_X_0213.md "wikilink")、文字列をUTF-16で処理するシステムに於いてJIS X 0213の全ての文字に対応する場合はサロゲートペアを正しく処理できる必要がある。

## 将来の予定

中国は『[康熙字典](https://ja.wikipedia.org/wiki/康熙字典 "wikilink")』や、[古壮字](../Page/古壮字.md "wikilink")をはじめとする少数民族で使われている特殊漢字などの文字をすべてUCSに収録させようとしており、また日本や韓国、ベトナムでも漢字（[国字](../Page/国字.md "wikilink")、[韓国国字](https://ja.wikipedia.org/wiki/韓国国字 "wikilink")、[チュノム](../Page/チュノム.md "wikilink")など）の追加提案があるため、Unicodeの今後のバージョンでは、拡張Gとしての追加漢字や、[甲骨文](https://ja.wikipedia.org/wiki/甲骨文 "wikilink")などの古代の文字を、U+30000以降（[第三漢字面](https://ja.wikipedia.org/wiki/第三漢字面 "wikilink")）へ追加することが検討されている。

## CJK互換漢字

U+F900～U+FAFFのブロックである。Unicode 3.1では補助集合として第2面（[追加漢字面](https://ja.wikipedia.org/wiki/追加漢字面 "wikilink")）にU+2F800～U+2FA1Fのブロックが追加された。基本的にCJK統合漢字と重複する漢字が割り当てられている。

CJK統合漢字には、基本的に1つの漢字に付き1つの符号位置しか与えられないため、[KS X 1001など各国の規格で全く同じ形の漢字が重複して収録されていた場合](https://ja.wikipedia.org/wiki/KS_X_1001 "wikilink")、Unicodeとの相互変換を行った際可逆性が失われる事となる。（KS X 1001の場合、読みにより分離している為、読みがわからなくなって困ることがある）。この問題を解決する為に、このブロックが作られた。[Big5](../Page/Big5.md "wikilink")で誤って重複してしまった2字もこのブロックにある。IBM拡張漢字のうちCJK統合漢字に入れなかったものもあり、その中にはU+FA1F（﨟）やU+FA24（﨤）などCJK統合漢字に同じ漢字が存在しない為、CJK統合漢字と同じ扱いをするものが12字ある。

Unicode 3.2では、[JIS X 0213で包摂基準が変更され分離されたもののうち](../Page/JIS_X_0213.md "wikilink")、「侮󠄁󠄁」や「僧󠄁󠄁」、「社󠄁」などUnicodeでは包摂されるものがこのブロックに追加された。これは、CJK統合漢字は日本以外にも中国と韓国の漢字を含めたものであり、日本だけの為に包摂基準を変更して包摂分離して追加すると、他の国が国内規格と対応するUnicodeのコード値を変更しなければならないことがあるからである。例えば、「社󠄁」など⽰偏の漢字は[GB 18030では偏が](https://ja.wikipedia.org/wiki/GB_18030 "wikilink")「⺭」の形を採用しているが、KS X 1001では偏が「⺭」でなく「⺬」の形を採用している。もし「社󠄁」を包摂分離してCJK統合漢字の新たな符号位置に追加したとすると、GB 18030はそのままでよいが、KS X 1001の「社󠄀」のコードとの対応は新たに追加された方に変更しなければならなくなる。

## 原規格

漢字のそれぞれの文字には，少なくとも一つの原典参照がある。\[15\]

注記 原典が更新されても，原典参照は，更新しない。更新された原典は，古い版に含まれていない文字の識別だけに用いてもよい。

### 原典 G

原典 G は，次のとおりに識別する。

  - GB 2312-80

  - GB 12345-90

  - GB 7589-87 繁体字

  - GB 7590-87 繁体字

  - 現代漢語通用字表及び簡化字総表

  - シンガポールの漢字

  - GB 8565-88

  - GB 18030-2000

  - GB 16500-95

  - GB 15564-1995 香港の一部の文字放送用の漢字体系

  - GB 12052-89 情報交換用ハングル文字符号化文字情報

  - 四庫全書

  - 中国大百科全書

  - 辞海

  - 辞源

  - 中国測絵科学院用字

  - 方正排版系統

  - 古代漢語詞典

  - 漢語大詞典

  - 漢語大字典

  - 中国公安省 ID システム

  - 商務印書館用字

  - 康熙字典及び康熙字典補遺

  - 現代漢語詞典

  - 古代漢語詞典

  - 中華字海

  - 殷周金文集成引得

注記 康煕字典（GKX）として参照されている文字に対する符号表上での図形記号は，現在中国で使用されているものであり，康煕字典に示されている図形記号とは僅かに異なる場合がある。

### 原典 H

原典 H は，次のとおりに識別する。

  - 香港増補字符集 2008

  - Big-5:計算機での中国語字形と文字符号との対応表, Technical Report C-26, 電脳用中文字型与字碼対照表, 技術通報 C-26, 1984, Symbols

  - Big-5, Level 1

  - Big-5, Level 2

### 原典 M

原典 M は，次のとおりに識別する。

  - Macao Information System Character Set（澳門資訊系統字集）

### 原典 T

原典 T は，次のとおりに識別する。

  - TCA-CNS 11643-1992 第 1 面

  - TCA-CNS 11643-1992 第 2 面

  - TCA-CNS 11643-1992 第 3 面及び幾つかの追加文字

  - TCA-CNS 11643-1992 第 4 面

  - TCA-CNS 11643-1992 第 5 面

  - TCA-CNS 11643-1992 第 6 面

  - TCA-CNS 11643-1992 第 7 面

  - TCA-CNS 11643-2007 第 11 面

  - TCA-CNS 11643-2007 第 12 面

  - TCA-CNS 11643-2007 第 13 面

  - TCA-CNS 11643-2007 第 14 面

  - TCA-CNS 11643-2007 第 15 面

### 原典 J

原典 J は，次のとおりに識別する。

  - JIS X 0208-1990

  - JIS X 0212-1990

  - JIS X 0213:2000 第 3 水準

  - JIS X 0213:2004 第 3 水準

  - JIS X 0213:2000 第 4 水準

  - [国内5社漢字統合表](https://ja.wikipedia.org/wiki/国内5社漢字統合表 "wikilink")，1993

  - [汎用電子情報交換環境整備プログラム](https://ja.wikipedia.org/wiki/汎用電子情報交換環境整備プログラム "wikilink") 2002〜2009

  - [日本国字集](https://ja.wikipedia.org/wiki/日本国字集 "wikilink")

  - [電波産業会](https://ja.wikipedia.org/wiki/電波産業会 "wikilink") [ARIB STD-B24](https://ja.wikipedia.org/wiki/ARIB_STD-B24 "wikilink") 第 5.1 版，2007 年 3 月 14 日

### 原典 K

原典 K は，次のとおりに識別する。

  - KS X 1001:2004（以前は，KS C 5601-1987 であった。）

  - KS X 1002:2001（以前は，KS C 5657-1991 であった。）

  - PKS C 5700-1 1994

  - PKS C 5700-2 1994

  - PKS 5700-3:1998

  - Korean IRG Hanja Character Set 5th Edition: 2001

注記 K2，K3，K4 及び K5 に含まれる漢字は，新しい韓国規格群において改正作業が進んでいる。

### 原典 KP

原典 KP は，次のとおりに識別する。

  - KPS 9566-97

  - KPS 10721:2000及び KPS 10721:2003

### 原典 V

  - TCVN 5773:1993

  - TCVN 6056:1995

  - VHN 01:1998

  - VHN 02:1998

  - Dictionary on Nom 2006, Dictionary on Nom of Tay ethnic 2006, Lookup Table for Nom in the South 1994

### 原典 U

  - ユニコード技術報告書 UTR \#45, U-source Ideographs, May 2010

## 参考文献

  -
  -
## 関連項目

  - [IICORE](https://ja.wikipedia.org/wiki/IICORE "wikilink")
  - [符号点](https://ja.wikipedia.org/wiki/符号点 "wikilink")（コードポイント）
  - [書記素](https://ja.wikipedia.org/wiki/書記素 "wikilink")
  - 書記素クラスタ (grapheme cluster) - 漢字は、UTF-16で可変（16、32、48、64ビット）\[16\]
  - [基本多言語面](https://ja.wikipedia.org/wiki/基本多言語面 "wikilink")
      - [CJK統合漢字 (Unicodeのブロック)](https://ja.wikipedia.org/wiki/CJK統合漢字_\(Unicodeのブロック\) "wikilink")

      - [CJK互換漢字](https://ja.wikipedia.org/wiki/CJK互換漢字 "wikilink")

      -
  - [追加面](https://ja.wikipedia.org/wiki/追加面 "wikilink")（[サロゲートペア](https://ja.wikipedia.org/wiki/サロゲートペア "wikilink")に対応したアプリケーションで処理）
      - [追加漢字面](https://ja.wikipedia.org/wiki/追加漢字面 "wikilink")
          -
          -
          -
          -
          -
          - [CJK互換漢字補助](https://ja.wikipedia.org/wiki/CJK互換漢字補助 "wikilink")
      - [第三漢字面](https://ja.wikipedia.org/wiki/第三漢字面 "wikilink")
          - CJK統合漢字拡張G
  - [異体字セレクタ](https://ja.wikipedia.org/wiki/異体字セレクタ "wikilink")（IVD/IVSに対応したアプリケーションで処理）\[17\]

## 脚注

## 外部リンク

  - [Chinese Japanese Korean Characters in Unicode](http://www.sungwh.freeserve.co.uk/uni/)
  - [Windowsの多言語フォント・リスト](http://mlang1.osaka-gaidai.ac.jp/multi/win_font_list.html)
  - [CJK-CODE](http://cjk-code.com/)
  - [BabelMap](http://www.babelstone.co.uk/Software/BabelMap.html) - Unicode Character Map for Windows

[Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink") [Category:中国語](https://ja.wikipedia.org/wiki/Category:中国語 "wikilink") [Category:朝鮮語](https://ja.wikipedia.org/wiki/Category:朝鮮語 "wikilink") [Category:漢字](https://ja.wikipedia.org/wiki/Category:漢字 "wikilink") [Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13. 安岡孝一・安岡素子『[「唡」はなぜJIS X 0221に含まれているのか ―Unicode幽霊字研究―](http://kanji.zinbun.kyoto-u.ac.jp/~yasuoka/publications/1997-08-29.pdf)』[情報処理学会](https://ja.wikipedia.org/wiki/情報処理学会 "wikilink")研究報告
14.
15. [JIS X 0221:2014 国際符号化文字集合（ＵＣＳ）](http://kikakurui.com/x0/X0221-2014-01.html)
16. [経済産業省 改元を目前に今すぐ実施すべき準備、対応とは 13ページ](https://www.meti.go.jp/policy/it_policy/kaigen/20190412_kaigen_2.pdf)
17. [IPAmj明朝フォント符号化の状況](https://mojikiban.ipa.go.jp/1309.html)