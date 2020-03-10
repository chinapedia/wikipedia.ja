> この記事は[TTSneo](https://ja.wikipedia.org/wiki/TTSneo)から翻訳されています。


**TTSneo**（ティーティーエス・ネオ）は[スクリプト型](../Page/スクリプト言語.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")のひとつ。開発者はゆうと。動作可能[OSは](../Page/オペレーティングシステム.md "wikilink")、[Windows98](../Page/Microsoft_Windows_98.md "wikilink")/[Me](https://ja.wikipedia.org/wiki/Microsoft_Windows_Me "wikilink")/[2000](../Page/Microsoft_Windows_2000.md "wikilink")/[XP](../Page/Microsoft_Windows_XP.md "wikilink")。[NTや](../Page/Microsoft_Windows_NT.md "wikilink")[95でも一部機能制限があるものの](../Page/Microsoft_Windows_95.md "wikilink")、使用可能である。[Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")/[7にもほとんど対応している](../Page/Microsoft_Windows_7.md "wikilink")。旧称は**Technology Terminal Script**（テクノロジ・ターミナル・スクリプト）。

## 概要

[日本語](../Page/日本語.md "wikilink")ベースのため、日本語に近い形で[プログラムの](../Page/プログラム_\(コンピュータ\).md "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")を作成することができる。また、言語作成にあたって、[ロゴライターのソースコードを基調としているため](https://ja.wikipedia.org/wiki/LOGO "wikilink")、主に図形関係を得意とするが、最近は他の[関数や](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")[命令を重点に強化されているため](../Page/命令_\(コンピュータ\).md "wikilink")、徐々に衰退している。

本体は[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")6.0で作成されており、そのソースコードは公開されていない。[インタープリタ](https://ja.wikipedia.org/wiki/インタープリタ "wikilink")型なので実行速度は遅い。

Visual Basicに用意されているほとんどの[GUI部品を利用でき](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")、外部[DLLや](../Page/ダイナミックリンクライブラリ.md "wikilink")[APIとの連携も可能なため](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、既存の機能よりもさらに高度な[アプリケーションを作成することができる](../Page/アプリケーションソフトウェア.md "wikilink")。

また、Visual Basicの様な、[RADを搭載し](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")、アプリケーションの開発を安易に行うことが出来る。

2008年7月27日には、[開発言語を](../Page/プログラミング言語一覧.md "wikilink")[.NET Frameworkに変え](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、[文法](../Page/文法.md "wikilink")や仕様などを刷新した新言語「[プロデル](../Page/プロデル.md "wikilink")」のベータ版がリリースされた。

## 言語仕様

### 基本

[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語ではなく、[手続き型言語](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")である。このためこれによって作られた[プログラムは](../Page/プログラム_\(コンピュータ\).md "wikilink")、一行目から順番に実行されていく形で、[BASIC](../Page/BASIC.md "wikilink")によく似ている。

基本的には[命令や](../Page/命令_\(コンピュータ\).md "wikilink")[代入をおいて](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")[改行して](../Page/改行コード.md "wikilink")、また命令か代入がきてまた改行してという形に、一行に一命令が入るのが基本的な文法であるが、「。」で一行に複数の命令を入れることもできる。

ウィンドウを表示して動く、一般的な[アプリケーションを作る際は](../Page/アプリケーションソフトウェア.md "wikilink")、ウィンドウを表示する命令を実行した後、「待機」命令で[メッセージループ](https://ja.wikipedia.org/wiki/メッセージループ "wikilink")に入る。この後、「待機」命令の後に記述された「手順」が、TTSneoがウィンドウメッセージを受けたときに実行され、[GUIによるユーザーからの入力に対応する](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")。といったようにプログラムが成り立つ。

なにも必ずウィンドウを生成しなければならないわけではない。ただそうしたほうが**見栄えは**よい。

命令と[関数といった風に分離されている](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。関数は処理をして値を返すもの、命令は値を返さず処理のみという仕組みである。しかし、文法は異なる。

具体的なプログラムの中身は、命令や代入などをなんども記述していく形で構成される。関数は単独では使用しない。

### 命令

「○○を□□」という形で、動詞が後に来るように命令する。文末の表現が自由にできる（「変えろ」を、「変えてください」など）。

### 関数

「△△は、□□（○○、●●、...）」という形になる。 処理を行い、必ず[値](https://ja.wikipedia.org/wiki/値 "wikilink")を返すものが関数である。関数は命令や代入の補助的な役割で、単独で使用はできない。 また、必ず変数に代入する形で使う。 しかし、バージョン1.67.1963から、オリジナル命令・関数の単独使用が可能になった。 ただ、これはあくまでも**オリジナル命令**だけである。 文体は、以下のとおりである。

`’今までどおりの文体`
`変数は、手順名（「A」）`
`手順名（「A」）を表示`

`’新しい文体`
`手順名（「A」）`

### 手順

手順を使って、処理をたらい回しにすることもできる。これを使うことにより、ソースコードは小さくなり、速度も速く無駄のないプログラムが作れる。

手順の始まりは「手順は　*\[手順名\]*」（*\[手順名\]*は好きなものに変えられる）、手順の終わりは「終わり」と書いて表現する。

手順を呼び出すには、命令のように手順名を書くだけでよい。

手順を使って、自作の命令や関数を作ることもできる。

### 変数と命名規則

[日本語](../Page/日本語.md "wikilink")ベースのため、当然[変数名には日本語を使用することができる](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")。 変数は、すべて文字列によって管理され、宣言は必要ない。[代入は](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")「～は　～」「～=～」といった形ですることができ、代入する際定義されていない変数は自動的に生成される。なお、「は」を使って代入する際には、「は」の後にスペースや読点（、）、全角カンマ（，）を書く必要がある。（＝の場合は必要ない）

### その他の文法

命令が終わった印として「。」を利用できるが、これは無視される。しかし、「。」を使うことで一行に複数の命令をおくことができる。

[コメント (コンピュータ)は](../Page/コメント_\(コンピュータ\).md "wikilink")[BASIC](../Page/BASIC.md "wikilink")のような「’」（[アポストロフィー](../Page/アポストロフィー.md "wikilink")）の記号([半角](https://ja.wikipedia.org/wiki/半角 "wikilink")または[全角](https://ja.wikipedia.org/wiki/全角 "wikilink"))、「//」または「ーー」に続けて次の改行までで表すことができる。TTSneo1.5より[ブロックコメントに対応し](https://ja.wikipedia.org/wiki/コメント_\(コンピュータ\)#ブロックコメント "wikilink")、/\*と\*/で括って表す。

## TTSneoのHello\!worldの例

    「Hello!［改行］world」を表示
    ーー"［改行］" の "［］"は全角。

## 外部リンク

  - [TTSneo公式サイト](http://tts.utopiat.net/)

[Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:日本語プログラミング言語](https://ja.wikipedia.org/wiki/Category:日本語プログラミング言語 "wikilink")