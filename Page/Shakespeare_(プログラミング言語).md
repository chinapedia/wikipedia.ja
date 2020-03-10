> この記事は[Shakespeare \(\)](https://ja.wikipedia.org/wiki/Shakespeare_\(\))から翻訳されています。


**Shakespeare Programming Language** (**SPL**) は、ヨン・オースルンド (Jon Åslund) とカール・ハッセルストローム (Karl Hasselström) によって創られた[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。[Chef言語と同じように](https://ja.wikipedia.org/wiki/:en:Chef_\(programming_language\) "wikilink")、Shakespeare言語はあたかもプログラムではないもの（この場合は[シェイクスピアの演劇](../Page/ウィリアム・シェイクスピア.md "wikilink")）に見えるよう設計されている。

プログラムの冒頭にある登場人物のリストによって、[スタック](../Page/スタック.md "wikilink")（もちろん「ロミオ」「ジュリエット」のような名前になっている）を宣言する。これらの登場人物の会話を通じて、それぞれの先頭にある値をプッシュ・ポップしたり[入出力](../Page/入出力.md "wikilink")を実行したりする。登場人物が質問を投げかけることで、[条件文としての振る舞いをさせることもできる](../Page/If文.md "wikilink")。全体的にプログラミングのモデルはかなり[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")に近いが、それよりも相当に冗長である。

「台本」のようなコードを記述するコンピューター言語には他に、プログラミング言語の「[Mana](https://ja.wikipedia.org/wiki/Mana_\(プログラミング言語\) "wikilink")」や データ記述言語の「[TVML](../Page/TV_program_Making_language.md "wikilink")」がある。

## Shakespeareによるプログラミング

### 演目

Shakespeare言語プログラムの最初の行は「演目」(title) と呼ばれ、コンパイラは最初の行から最初のピリオドまでをコメントとみなす。

### 配役表

変数を宣言するセクションである。変数は符号付き整数を保持する。宣言は以下の形式で記述する。

`Name, Description`

ここで`Name`は変数の名前であり、`Description`はコンパイラによって無視される。 変数名は全てシェイクスピアの演劇中に登場する人物の名前でなければならない。

### 幕と場

Shakespeare言語のコードは「幕」(Act) とその中に含まれる「場」(Scene) に分けられる。各々の「幕」と「場」は[ローマ数字](../Page/ローマ数字.md "wikilink")で番号が振られ、GOTO文のラベルとして機能する。コロンの後のコードはコメントとみなされる。形式は以下の通り。

`Act I: Hamlet's insults and flattery.`
`Scene I: The insulting of Romeo.`

### 登場と退場

「登場人物」(変数) は演じる前に「舞台」に上がらなければならない。変数を舞台に上がらせるには、`Enter` (登場) コマンドを使用する。 登場人物を退場させるには、`Exit` (退場) コマンドを使用する。`Exeunt` (一同退場) コマンドは2名以上の登場人物を退場させるが、登場人物が指定されていない場合は全ての人物が退場する。形式は以下の通り。

`[Enter Juliet] `
`[Enter Romeo and Juliet]`
`[Exit Romeo]`
`[Exeunt Romeo and Juliet]`
`[Exeunt]`

各行は登場人物の名前、コロン、そして台詞から構成される。

## コード例

これはSPLによる[Hello Worldプログラムの一部である](https://ja.wikipedia.org/wiki/Hello_World "wikilink")。各台詞によって相手の人物に数値が設定され、"Speak your mind"によって相手の人物の値が出力される。

`Romeo, a young man with a remarkable patience.`
`Juliet, a likewise young woman of remarkable grace.`
`Ophelia, a remarkable woman much in dispute with Hamlet.`
`Hamlet, the flatterer of Andersen Insulting A/S.`

`                    Act I: Hamlet's insults and flattery.`
`                    Scene I: The insulting of Romeo.`
` [Enter Hamlet and Romeo]`
` Hamlet:`
`You lying stupid fatherless big smelly half-witted coward! You are as`
`stupid as the difference between a handsome rich brave hero and thyself!`
`Speak your mind!`
` You are as brave as the sum of your fat little stuffed misused dusty`
`old rotten codpiece and a beautiful fair warm peaceful sunny summer's`
`day. You are as healthy as the difference between the sum of the`
`sweetest reddest rose and my father and yourself! Speak your mind!`
` You are as cowardly as the sum of yourself and the difference`
`between a big mighty proud kingdom and a horse. Speak your mind.`
` Speak your mind!`
` [Exit Romeo]`
`                    Scene II: The praising of Juliet.`
` [Enter Juliet]`
` Hamlet:`
`Thou art as sweet as the sum of the sum of Romeo and his horse and his`
`black cat! Speak thy mind!`
` [Exit Juliet]`
`                    Scene III: The praising of Ophelia.`
` [Enter Ophelia]`
` Hamlet:`
`Thou art as lovely as the product of a large rural town and my amazing`
`bottomless embroidered purse. Speak thy mind!`
` Thou art as loving as the product of the bluest clearest sweetest sky`
`and the sum of a squirrel and a white horse. Thou art as beautiful as`
`the difference between Juliet and thyself. Speak thy mind!`
` [Exeunt Ophelia and Hamlet]`

`                    Act II: Behind Hamlet's back.`
`                    Scene I: Romeo and Juliet's conversation.`
` [Enter Romeo and Juliet]`
` Romeo:`
`Speak your mind. You are as worried as the sum of yourself and the`
`difference between my small smooth hamster and my nose. Speak your`
`mind!`
` Juliet:`
`Speak YOUR mind! You are as bad as Hamlet! You are as small as the`
`difference between the square of the difference between my little pony`
`and your big hairy hound and the cube of your sorry little`
`codpiece. Speak your mind!`
` [Exit Romeo]`
`                    Scene II: Juliet and Ophelia's conversation.`
` [Enter Ophelia]`
` Juliet:`
`Thou art as good as the quotient between Romeo and the sum of a small`
`furry animal and a leech. Speak your mind!`
` Ophelia:`
`Thou art as disgusting as the quotient between Romeo and twice the`
`difference between a mistletoe and an oozing infected blister! Speak`
`your mind!`
` [Exeunt]`

## 関連項目

  - [Mana (プログラミング言語)](https://ja.wikipedia.org/wiki/Mana_\(プログラミング言語\) "wikilink")
  - [TVML](../Page/TV_program_Making_language.md "wikilink")

## 外部リンク

  - [ホームページ](http://shakespearelang.sourceforge.net/)
  - [SourceForgeのサイト](http://sourceforge.net/projects/shakespearelang/)
  - [GCCのフロントエンド](http://people.csa.iisc.ernet.in/sreejith/frontends/spl/)
  - [The Shakespeare Programming Languageとは (日本語の解説)](http://kara.ifdef.jp/program/spl/spl01.html)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:シェイクスピア](https://ja.wikipedia.org/wiki/Category:シェイクスピア "wikilink")