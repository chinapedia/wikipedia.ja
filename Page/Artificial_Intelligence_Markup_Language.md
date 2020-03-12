> この記事は[Artificial Intelligence Markup Language](https://ja.wikipedia.org/wiki/Artificial_Intelligence_Markup_Language)から翻訳されています。


**Artificial Intelligence Markup Language**（アーティフィシャル・インテリジェンス・マークアップ・ランゲージ、**AIML**、エーアイエムエル）とは、[自然言語](../Page/自然言語.md "wikilink")[ソフトウェアエージェント](../Page/ソフトウェアエージェント.md "wikilink")構築のための [XML](../Page/Extensible_Markup_Language.md "wikilink") を応用した[マークアップ言語](../Page/マークアップ言語.md "wikilink")である。

## 背景

AIML は Richard Wallece と世界的なフリーソフトウェア・コミュニティにより、1995年から2002年にかけて開発された。当初の目的は[ELIZA](../Page/ELIZA.md "wikilink")を高度に拡張した "[A.L.I.C.E.](../Page/Artificial_Linguistic_Internet_Computer_Entity.md "wikilink")" と呼ばれるシステム向けであり、同システムは[ローブナー賞](../Page/ローブナー賞.md "wikilink")を3回受賞し、2004年には[Chatterbox Challenge](http://www.chatterboxchallenge.com/)で優勝している。

A.L.I.C.E. のAIMLは[GNU GPLライセンスでリリースされたため](../Page/GNU_General_Public_License.md "wikilink")、多数のAIMLインタプリタが[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")または[オープンソース](../Page/オープンソース.md "wikilink")で作られ、A.L.I.C.E. のクローンも多数作成された。いくつかの言語用のセット（[Free AIML sets](http://aitools.org/Free_AIML_sets)）も作られ、ユーザーコミュニティによって利用可能となっている。最近では、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ベースの[Program D](http://aitools.org/programd)というAIMLインタプリタの開発が活発である。他にも、[Ruby](../Page/Ruby.md "wikilink")、[Python](../Page/Python.md "wikilink")、[C++](../Page/C++.md "wikilink")、[C\#](../Page/C_Sharp.md "wikilink")、[Pascal](../Page/Pascal.md "wikilink")などの言語向けにフリーまたはオープンソースのAIMLインタプリタが開発されている。

## AIMLの要素

AIML はいくつかの要素からなる。以下にその主な部分の詳細を解説する。

### カテゴリ

AIMLにおけるカテゴリは、知識の基本単位である。カテゴリには少なくとも、「パターン」と「テンプレート」という要素が含まれる。以下に単純なカテゴリの例を示す。

` `<category>
`   `<pattern>`WHAT IS YOUR NAME`</pattern>
`   `<template>`My name is John.`</template>
` `</category>

このカテゴリをロードすると、AIMLボットは "What is your name" という入力に対して "My name is John." と応答する。

### パターン

パターンは、1つまたは複数のユーザー入力とマッチすることを意図した文字列である。以下のパターン

` WHAT IS YOUR NAME`

は大文字/小文字を無視して、"what is your name" といった入力とマッチする。パターンにはワイルドカードを使用できる。例えば、次のパターン

` WHAT IS YOUR *`

は、"what is your name" にも "what is your shoe size" にも "what is your purpose in life" にもマッチする。

AIMLのパターンの文法は非常に単純であり、[正規表現](../Page/正規表現.md "wikilink")のような複雑な表現はできない。対話用に特化した設計であり、省略表現への対応や誤記への対応は AMILインタプリタ側で対応することができる。

### テンプレート

テンプレートはマッチしたパターンに対する応答を指定する。テンプレートには以下のような単純なテキストを使うこともできる。

`  My name is John.`

テンプレートには変数を使って以下のように表記することもできる。

` My name is `<bot name="name"/>`.`

こうすると、ボット名が文の中に組み込まれる。

` You told me you are `<get name="user-age"/>` years old.`

この場合、ユーザーの年齢が既にわかっていれば、それを応答の中で使うことができる。

テンプレートでは基本的なテキスト形式が使え、条件付応答（if-then/else）やランダムな応答も設定できる。

テンプレートで **srai** という要素を使って他のパターンにリダイレクトすることができる。これは、意味が同じで表現が異なる場合に対応する。以下に例を示す。

` `<category>
`   `<pattern>`WHAT IS YOUR NAME`</pattern>
`   `<template>`My name is `<bot name="name"/>`.`</template>
` `</category>
` `<category>
`   `<pattern>`WHAT ARE YOU CALLED`</pattern>
`   `<template>
`     `<srai>`what is your name`</srai>
`   `</template>
` `</category>

1つめのカテゴリは単に "what is your name" という質問に答えている。2番目のカテゴリでは "what are you called" と入力されたときに "what is your name" と入力されたときと同じ応答をするように指定している。つまり、この2つの文はこのシステムでは等価に扱われる。

テンプレートは応答を指定しているものであるため、表示形式などをHTMLで指定するといったことも可能である。

## 外部リンク

  - [aitools.org: AIML schema and specification, free AIML sets, Program D](http://aitools.org)
  - [alicebot.org: Richard Wallace's "ALICE Foundation"](http://www.alicebot.org)
  - [A.I.Nexus: A Showcase for Alicebots on the Web](http://www.knytetrypper.com/ain.html)
  - [Virtual Humans Forum](http://www.vhumanforum.com/)
  - [AIML Forum](http://www.vrconsulting.it/aiml/)
  - [AutoAiml - A Free Online Aiml file creator](http://aiml.harrybailey.com)
  - [GaitoBot AIML Editor](http://www.gaito.de/content/produkte_gaitobot/editor.asp?language=en)

### AIML実装（フリーまたはオープンソース）

開発進行中:

  - [Program D](http://aitools.org/programd) (Java, J2EE)
  - [RebeccaAIML](http://rebecca-aiml.sourceforge.net/) (C++)
  - [ChatterBean](http://www.geocities.com/phelio/chatterbean/) (Java)
  - [Program R](http://aiml-programr.rubyforge.org/) (Ruby)
  - [Program Q](http://sourceforge.net/projects/qaiml) (C++, Qt)
  - [AIMLbot (Program \#)](http://aimlbot.sourceforge.net/) (.NET/C\#)

冬眠状態:

  - [J-Alice](http://j-alice.sourceforge.net/) (C++)
  - [libaiml](http://www.alicebot.org/downloads/programs.html) (C++)
  - [Program E](http://sourceforge.net/projects/programe/) (PHP)
  - [Program N](http://www.aimlpad.com/)

<!-- end list -->

  - [Program V](http://www.virtualitas.net/perl/aiml/) (Perl)
  - [Program Y/PyAIML](http://pyaiml.sourceforge.net/) (Python)

### AIMLボット

  - [パンドラボット](http://www.pandorabots.com/botmaster/ja/home) 日本語版サイト
  - [The Original A.L.I.C.E.](http://www.pandorabots.com/pandora/talk?botid=f5d922d97e345aa1)
  - [Dawnstar](http://www.pandorabots.com/pandora/talk?botid=c1776ae8ce354d1f)
  - [Ailysse](http://www.pandorabots.com/pandora/talk?botid=829713883e34f760)
  - [Lilith](http://www.pandorabots.com/pandora/talk?botid=b9b96b247e34f4f2)
  - [Incognita - An artificial intelligence conversationalist chatting globally](http://www.pandorabots.com/pandora/talk?botid=f7634aec7e3652ed)
  - [Phile Knowledge](http://www.pandorabots.com/pandora/talk?botid=ef0d13991e361e05)
  - [iGod](http://www.titane.ca/concordia/dfar251/igod/main.html)
  - [Talk to William Shakespeare](http://www.shakespearebot.com)
  - [Chat with Ailis in English (Italian website)](http://ai-tech.com/showcase/)
  - [Prelude - a self learning chatbot with AIML support](http://prelude.lennart-lopin.de/)

[Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:フリー人工知能アプリケーション](https://ja.wikipedia.org/wiki/Category:フリー人工知能アプリケーション "wikilink")