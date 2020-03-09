> この記事は[GNU Lesser General Public License](https://ja.wikipedia.org/wiki/GNU_Lesser_General_Public_License)から翻訳されています。


**GNU Lesser General Public License**（以前は、**GNU <u>Library</u> General Public License**だった）または*' GNU LGPL**、単に**LGPL**は、[フリーソフトウェア財団](https://ja.wikipedia.org/wiki/フリーソフトウェア財団 "wikilink")（Free Software Foundation、以下FSFと略称）が公開している[コピーレフト](../Page/コピーレフト.md "wikilink")型の[フリーソフトウェアライセンス](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス "wikilink")である。[八田真行](https://ja.wikipedia.org/wiki/八田真行 "wikilink")による[日本語](../Page/日本語.md "wikilink")訳では**GNU 劣等一般公衆利用許諾書*'と呼称している。

## 概要

以前の名前から分かる通り、これは他の[プログラムにリンクされることを前提とした](https://ja.wikipedia.org/wiki/プログラム_\(コンピュータ\) "wikilink")[ライブラリ](https://ja.wikipedia.org/wiki/ライブラリ "wikilink")のためのライセンスとして作成された。当ライセンスは、*強い[コピーレフト](../Page/コピーレフト.md "wikilink")*(*strong copyleft*)を持つライセンスである[GNU General Public Licenseすなわち**GPL**と](../Page/GNU_General_Public_License.md "wikilink")[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")・[MIT Licenseのような](https://ja.wikipedia.org/wiki/MIT_License "wikilink")[パーミッシブ・ライセンス](https://ja.wikipedia.org/wiki/パーミッシブ・ライセンス "wikilink")との妥協の産物として設計されている。LGPLが最初にその略称を示していたGNU Library General Public Licenseは[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")に公開され、GPLv2との対等性を表すため同じバージョン2が付されることとなった。のちに小規模な改訂によりバージョン2.1という小数点リリース(ポイントリリース)となり、[1999年](../Page/1999年.md "wikilink")に公開されたが、同時にライブラリにこのライセンスを利用すると限るべきではないというFSFの立ち位置を反映させるため、GNU *Lesser* General Public Licenseと改名された。LGPLv3は[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")に公開された。これは、[GPLv](../Page/GNU_General_Public_License.md "wikilink")3と[完全な互換性があり](https://ja.wikipedia.org/wiki/GNU_General_Public_License#両立性とマルチライセンス "wikilink")、GPLv3にいくつか*追加的（許諾）条項*（*Additional permissions*。GPLv3第7項で許されている。）を加えた相補的形式を採用している。よって以前のバージョンよりも条文はかなり簡略化されており、GNU GPLv3への参照が条文に頻繁に現れる。しかしこれは[GPLリンク例外](https://ja.wikipedia.org/wiki/GPLリンク例外 "wikilink")を採用しているその他ソフトウェアよりも若干要件は多い。次のセクション"[GPLとの違い](https://ja.wikipedia.org/wiki/#GPLとの違い "wikilink")"を参照。

LGPLはLGPLに従う限り、プログラム自身に[コピーレフト](../Page/コピーレフト.md "wikilink")の「保護」（立ち位置が異なるものからは、「制限」とも言われるが）を与えるが、単にLGPLで保護されたプログラムとリンクする、他のソフトウェアへこれら「制限」を適用することはない。しかしながら、当該ソフトウェアへ影響を与えるある種のその他の「制限」は存在する。

LGPLは主に[ソフトウェア・ライブラリに採用されるが](https://ja.wikipedia.org/wiki/ライブラリ "wikilink")、スタンドアローンな[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")にも採用されるいくつかの例が存在し、もっとも有名な例は、[Mozilla](https://ja.wikipedia.org/wiki/Mozilla "wikilink")と[OpenOffice.org](https://ja.wikipedia.org/wiki/OpenOffice.org "wikilink")である。

## GPLとの違い

GPLとLGPLの主な相違点は、後者が、[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")か[プロプライエタリ・ソフトウェア](https://ja.wikipedia.org/wiki/プロプライエタリ・ソフトウェア "wikilink")かどうかに関わらず、非(L)GPLなプログラムにリンクされ得る（ライブラリの場合は「そのようなプログラムによって利用され得る」）というものである\[1\]\[2\]。この非(L)GPLプログラムはそれが[二次的著作物](https://ja.wikipedia.org/wiki/二次的著作物 "wikilink")([derivative work](https://ja.wikipedia.org/wiki/:en:derivative_work "wikilink"))ではない場合、任意の条項のもと*頒布*(*distribution*; 配布)してもよい。二次的著作物である場合は、LGPLv2.1第6節またはLGPLv3第4項の条項により、「**[顧客](https://ja.wikipedia.org/wiki/顧客 "wikilink")(カスタマー)自身の利用のための改変ならびにそのような改変を[デバッグ](https://ja.wikipedia.org/wiki/デバッグ "wikilink")するための[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")**」を許諾する必要がある\[3\]。 これは、[GPLのように](../Page/GNU_General_Public_License.md "wikilink")**常に**二次的著作物を同一の許諾条項に置くライセンスとは異なり、常に同一の許諾条件に置くとは*限らない*ことを示している。LGPLなプログラムを利用する著作物が二次的著作物か否かは法的な問題である\[4\]。ライブラリに[動的リンク](https://ja.wikipedia.org/wiki/動的リンク "wikilink")（すなわち[共有ライブラリや](https://ja.wikipedia.org/wiki/ライブラリ#共有ライブラリ "wikilink")[ダイナミックリンクライブラリ](https://ja.wikipedia.org/wiki/ダイナミックリンクライブラリ "wikilink")などによるリンク）する単体の[実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")は、法的に二次的著作物ではないと解釈される可能性がある\[5\]。その場合、ライブラリにリンクするプログラムは、LGPLv2.1における第5パラグラフ（Section 5. 第5節）、または同等の内容のLGPLv3第4項（Section 4.）に定義されている「ライブラリを利用する著作物」に該当する。次の文はLGPLv2.1第5節の第1段落にある条文の引用である。

  -
    A program that contains no derivative of any portion of the Library, but is designed to work with the Library by being compiled or linked with it, is called a "work that uses the Library". Such a work, in isolation, is not a derivative work of the Library, and therefore falls outside the scope of this License.<ref>

</ref>

LGPL の一つの特徴は、（LGPLv2.1では第3節、LGPLv3では第2項の条項により）ソフトウェアのLGPLで保護された任意の部分をGPLで保護することも可能にさせる。この特徴により、GPLで保護されたライブラリやアプリケーションにおいて、LGPLで保護されたコードを直接再利用することや、また、プロプライエタリなソフトウェア製品に利用されないようにするコードのバージョンを作成したいと考える場合、有益となる。

## ライブラリのライセンスにGPLとLGPLのどちらを選択するか

以前の名前が"GNU Library General Public License"だったこともあり、FSFはライブラリはLGPLを採用することを望んでいるという印象を受ける人は多かった。[1999年](../Page/1999年.md "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")、[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")は、*Why you shouldn't use the Lesser GPL for your next library*\[6\](*なぜ次のライブラリには劣等GPLを利用するべきでないのか*\[7\])という評論を執筆し、この中でなぜこのことが当てはまらないケースがあるのかということと、LGPLをライブラリに適用することは*必ずしも*適切とは限らないことを説明した。

  -
    Which license is best for a given library is a matter of strategy, and it depends on the details of the situation. At present, most GNU libraries are covered by the Library GPL, and that means we are using only one of these two strategies \[allowing/disallowing proprietary programs to use a library\], neglecting the other. So we are now seeking more libraries to release under the ordinary GPL.\[8\]

このことは、LGPLがなのではなく、単に、LGPLを*全ての*ライブラリに適用するべきではないと述べており、例えば[GNU CライブラリはLGPLを利用するべきライブラリの一例として引き合いに出されるが](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")、LGPLである理由は[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")などをはじめとするライブラリの実装が既に幾つか存在し、プロプライエタリ・ソフトウェアからなる著作物が、GPLなライブラリを飛び越えて、競合するBSDライセンスなどの[パーミッシブ・ライセンス](https://ja.wikipedia.org/wiki/パーミッシブ・ライセンス "wikilink")により許諾されるライブラリとリンクする可能性が単に存在するからである。— ストールマンは続けて次のことを主張している。

  -
    Using the ordinary GPL is not advantageous for every library. There are reasons that can make it better to use the Lesser GPL in certain cases.\[9\]

事実、ストールマンとFSFは時折、（利用者の[自由](https://ja.wikipedia.org/wiki/自由 "wikilink")を拡大するため、）戦略的事項として、意外なことだが、LGPLより制限の少ないライセンスの利用を強く主張している。有名な例は、[Vorbis](https://ja.wikipedia.org/wiki/Vorbis "wikilink")音声[コーデック](https://ja.wikipedia.org/wiki/コーデック "wikilink")プロジェクトのライブラリに[BSD形式のライセンスを採用したことをストールマンが支持したというケースである](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")\[10\]\[11\]。

## プログラミング言語による特異性

本ライセンスの条文は、[C言語](../Page/C言語.md "wikilink")やその近縁言語により作成されたアプリケーションを主に意図している用語の使われ方が見られる。Franz Inc.は、[Lispのコンテキストにおいて用語を明確化するため](https://ja.wikipedia.org/wiki/LISP "wikilink")、当ライセンスに同社が独自に作成した*前文*(*preamble*)を加えた形で公開した。この独自の前文が付記されたLGPLは時折LLGPLと呼ばれる\[12\]。

加えて別の事例として、[Ada](../Page/Ada.md "wikilink")は[ジェネリクスという特別な性質を持つ言語であり](https://ja.wikipedia.org/wiki/ジェネリックプログラミング "wikilink")\[13\]、このことに対応するためGPLの改変版ライセンス[MGPLが作成されている](https://ja.wikipedia.org/wiki/GNAT_Modified_General_Public_License "wikilink") 。

## 「継承」にまつわるLGPLの話題

LGPLで保護されたソフトウェアが非(L)GPLコードにより[継承する場合](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")[クラスの適合性について若干の懸念が惹起している](https://ja.wikipedia.org/wiki/クラス_\(コンピュータ\) "wikilink")。明確な説明が[GNU](../Page/GNU.md "wikilink")の公式ウェブサイト上に与えられている。

  -
    The LGPL contains no special provisions for inheritance, because none are needed. Inheritance creates derivative works in the same way as traditional linking, and the LGPL permits this type of derivative work in the same way as it permits ordinary function calls.<ref name="lgpl-java">

全文は次の通り。LGPLv2.1を対象に記述されているが、そのページの最上部に記載の通り、LGPLv3では条文の節番号が異なる点を除いて同じ内容が適用され得る。 </ref>

参考訳

  -
    LGPLは、[継承についての特殊な規定を含めていない](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")。なぜなら、何も必要とされないからである。継承は、古きよきリンクと同じ方法で二次的著作物を作成する。そして、LGPLが通常の（訳注: [ライブラリ](https://ja.wikipedia.org/wiki/ライブラリ "wikilink")の）関数呼び出しを許諾しているのと同様に二次的著作物のこの形式も許諾しているのである。

## LGPLの特徴

以上をまとめると概ね次の内容になる。

LGPLは次のことを保証する。この内容はGPLでも保証されている権利の一部である（このことからGPLよりも弱いコピーレフト性を持つ）。

  - 社内など*私的組織内部*や*個人で*(*private*)利用するにあたってのソースコード改変、再コンパイルには制限がない。
  - LGPLで頒布されたプログラムを再頒布する際にはソースコードを公開する必要がある。

LGPLで頒布されたライブラリAについて、

  - コンパイル時にライブラリAに（*[動的](https://ja.wikipedia.org/wiki/動的リンク "wikilink")・[静的に関わらず](https://ja.wikipedia.org/wiki/静的リンク "wikilink")*）**リンク**される可能性のあるプログラムBのソースコードについてはLGPLを適用する必要は無く、その頒布の制限にも関与しない）<ref group="注釈">

たとえば[GNU/Linuxシステム](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")などでは標準的なC言語のソースコードをコンパイルすると、LGPLである[glibcに](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")**リンク**される。このときコンパイルしたソースコードが[独占的であったとしても](https://ja.wikipedia.org/wiki/プロプライエタリ・ソフトウェア "wikilink")、LGPLの条項を適用しなくてよい。） </ref>。

  - ライブラリAに**リンク**したプログラムBを頒布する場合、Bのライセンスに[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")を禁止する条項を含めてはならない。(LGPLv2第6節、LGPLv3第4節)<ref group="注釈">

ライブラリAに[静的リンク](https://ja.wikipedia.org/wiki/静的リンク "wikilink")した場合に加えて、[動的リンク](https://ja.wikipedia.org/wiki/動的リンク "wikilink")したプログラムが二次的著作物と見なされる場合も、リバースエンジニアリングを許可しなければならない。 </ref>

  - ライブラリAに[静的リンク](https://ja.wikipedia.org/wiki/静的リンク "wikilink")したプログラムBを頒布する場合、Bのソースコードまたは[オブジェクトコードの頒布に制限があってはならない](https://ja.wikipedia.org/wiki/オブジェクトファイル "wikilink")。(LGPLv2第6節a、LGPLv3第4節d0)
  - ライブラリAを改変して作成されたライブラリA'を頒布する場合、A'のライセンスはLGPLまたはGPLである必要がある。

## 脚注

### 注釈

### 出典

## 関連項目

  - [GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL)
  - [GNU Affero General Public License](https://ja.wikipedia.org/wiki/GNU_Affero_General_Public_License "wikilink") (AGPL)
  - [GPLリンク例外](https://ja.wikipedia.org/wiki/GPLリンク例外 "wikilink")
  - [GNU Free Documentation License](../Page/GNU_Free_Documentation_License.md "wikilink") (GFDL)
  - [GNAT Modified General Public License](https://ja.wikipedia.org/wiki/GNAT_Modified_General_Public_License "wikilink") (GMGPL)
  - [GNUプロジェクト](https://ja.wikipedia.org/wiki/GNUプロジェクト "wikilink")
  - [フリーソフトウェアライセンス](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス "wikilink")
  - [BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")
  - [パブリックドメインソフトウェア](https://ja.wikipedia.org/wiki/パブリックドメインソフトウェア "wikilink")

## 外部リンク

  - [The GNU Lesser General Public License](https://www.gnu.org/licenses/lgpl.html) (原文)
      - [GNU 劣等一般公衆利用許諾書 バージョン3](https://ja.osdn.net/projects/opensource/wiki/licenses%2FGNU_Lesser_General_Public_License_version_3.0) ([八田真行](https://ja.wikipedia.org/wiki/八田真行 "wikilink")による非公式日本語翻訳)
  - [The GNU Lesser General Public License, version 2.1](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html) (原文)
      - [GNU 劣等一般公衆利用許諾契約書 バージョン2.1](https://ja.osdn.net/projects/opensource/wiki/licenses%2FGNU_Library_or_Lesser_General_Public_License) ([八田真行](https://ja.wikipedia.org/wiki/八田真行 "wikilink")による非公式日本語翻訳)
  - [Derivative Works](https://www.linuxjournal.com/article/6366) - [ライブラリ](https://ja.wikipedia.org/wiki/ライブラリ "wikilink")がGPLである場合の[二次的著作物](https://ja.wikipedia.org/wiki/二次的著作物 "wikilink")の定義に関する[ローレンス・ローゼンの評論](https://ja.wikipedia.org/wiki/ローレンス・ローゼン_\(弁護士\) "wikilink")。

[Category:オープンソースライセンス](https://ja.wikipedia.org/wiki/Category:オープンソースライセンス "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink")

1.
2.
3.
4.  二次的著作物の範囲の問題は[ライセンス](https://ja.wikipedia.org/wiki/ライセンス "wikilink")に関わらず[ソフトウェア](../Page/ソフトウェア.md "wikilink")、そしてあらゆる[著作物](https://ja.wikipedia.org/wiki/著作物 "wikilink")全てにおいて法的な問題であり、明確な判例はない。GPLについても同様であり、その見解についての詳細は、記事"[GNU General Public License\#リンクと派生物](https://ja.wikipedia.org/wiki/GNU_General_Public_License#リンクと派生物 "wikilink")"に若干記載されている。
5.  ライブラリに動的リンクされた実行ファイルがライブラリの二次的著作物か否かは法的な問題であり、LGPLとGPLで扱いに差はない。これは、LGPLやGPLが適用されたライブラリに動的リンクされた単体の実行ファイルが、LGPLにおいてライブラリの二次的著作物とみなされないなら、すなわちリバースエンジニアリングを許可する必要がないならば、GPLにおいてもライブラリの二次的著作物とみなされない、すなわち実行ファイルをGPLにする必要がないことを意味する。逆もまた然りである。
6.
7.
8.
9.
10.
11. のち、FSFは、プロプライエタリ音声フォーマットに対し[Ogg](https://ja.wikipedia.org/wiki/Ogg "wikilink")+[Vorbis](https://ja.wikipedia.org/wiki/Vorbis "wikilink")への置き換えを推奨する運動、PlayOggを開始している。
12.
13. [generics](https://ja.wikipedia.org/wiki/wikibooks:en:Ada_Programming/Generics "wikilink")