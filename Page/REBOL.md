> この記事は[REBOL](https://ja.wikipedia.org/wiki/REBOL)から翻訳されています。


**REBOL** は、[データ交換言語](https://ja.wikipedia.org/wiki/データ交換言語 "wikilink")であり、通信や分散処理に特化した[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。*Relative Expression Based Object Language* の略。設計者[カール・サセンラス](https://ja.wikipedia.org/wiki/カール・サセンラス "wikilink")はこれをメッセージング言語と呼び、「REBOL の主なアイデアは、サーバ、クライアント、その間の通信やそれらのストレージで使える言語にするというものであった。REBOLの能力は、プログラミング言語の概念とメタデータ言語の概念を統合したことに由来する。REBOLの究極の目的は、インターネット上のあらゆる機器間で情報がどのように格納され、交換され、処理されるかを表す新たなアーキテクチャを提供することである。すなわち、人間と機械の間の情報の意味論的交換に使われることを意味する」と述べている。

## 歴史

1997年にリリースされたREBOLは、[カール・サセンラス](https://ja.wikipedia.org/wiki/カール・サセンラス "wikilink")が20年に渡って設計したものである。サセンラスは [AmigaOS](https://ja.wikipedia.org/wiki/AmigaOS "wikilink") の主要アーキテクトであり、REBOLの設計にあたっては、[表示的意味論](../Page/表示的意味論.md "wikilink")の知識に基づいて、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、[Forth](../Page/Forth.md "wikilink")、[LOGO](https://ja.wikipedia.org/wiki/LOGO "wikilink")、[Self](../Page/Self.md "wikilink") といったプログラミング言語の概念を利用した。

REBOO/Command は2000年9月にリリースされ、暗号化機能、[ODBCアクセスなどが追加されている](../Page/Open_Database_Connectivity.md "wikilink")。REBOL/View は2001年4月にリリースされ、グラフィックス機能が追加されている。2001年8月にリリースされた REBOL/IOS は、拡張可能な共同作業環境である。2002年12月には、[ソフトウェア開発キット](https://ja.wikipedia.org/wiki/ソフトウェア開発キット "wikilink")がリリースされた。

2012年9月、R3（REBOL 3）[オープンソース](../Page/オープンソース.md "wikilink")として公開されることが発表される\[1\]。2012年12月には、安定版がリリースされた\[2\]\[3\]。ライセンスは[Apache License 2.0](https://ja.wikipedia.org/wiki/Apache_License "wikilink")\[4\]。

## 言語としての特徴

### プログラミング

REBOL は[インタプリタ](../Page/インタプリタ.md "wikilink")型[高級言語](https://ja.wikipedia.org/wiki/高級言語 "wikilink")であり、[マルチプラットフォームで](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[マルチパラダイムであり](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")、[動的リフレクションをサポートした言語である](https://ja.wikipedia.org/wiki/リフレクション_\(情報工学\) "wikilink")。同図像性（Homoiconicity）があり、コードとデータが同じ形式で表現され、[メタプログラミング](https://ja.wikipedia.org/wiki/メタプログラミング "wikilink")に最適である。

[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")、[関数型プログラミング](../Page/関数型言語.md "wikilink")、[プロトタイプベース](https://ja.wikipedia.org/wiki/プロトタイプベース "wikilink")プログラミングをサポートしている。REBOLは純粋関数型言語ではなく、[副作用のある](https://ja.wikipedia.org/wiki/副作用_\(プログラム\) "wikilink")[命令型プログラミング](../Page/命令型プログラミング.md "wikilink")の要素もある。また、純粋オブジェクト指向言語でもなく、オブジェクトでないデータ型も持っていて、他の[プログラミングパラダイム](https://ja.wikipedia.org/wiki/プログラミングパラダイム "wikilink")もサポートしている。REBOLは特に[言語指向プログラミング](https://ja.wikipedia.org/wiki/言語指向プログラミング "wikilink")に適しており、さらに言えば[ダイアレクティング](https://ja.wikipedia.org/wiki/ダイアレクティング "wikilink")（方言派生）に適している。

REBOLは[動的プログラミング言語](../Page/動的プログラミング言語.md "wikilink")であり、[動的型付け](https://ja.wikipedia.org/wiki/動的型付け "wikilink")（値は[強い型付けだが](https://ja.wikipedia.org/wiki/型システム "wikilink")、変数はそうではない）である。[メモリ管理](../Page/メモリ管理.md "wikilink")には[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")を使い、[例外処理](../Page/例外処理.md "wikilink")と[動的名前解決](https://ja.wikipedia.org/wiki/動的名前解決 "wikilink")をサポートしている。

### データ定義とその交換

データ交換言語としての利用を可能とするため、REBOLには以下のような最小限の構文がある。

  - 文の概念はない。構文の基本単位は式である。
  - キーワードは存在しない。
  - 空白と **\[**, **\]**, **(**, **)**, **"**, **{**, **}** を区切り記号として用いる。
  - 数々の[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")が備わっていて、その多くは字句形式（後述）で定義されている。

データ言語としてのREBOLは強く型付けされた値を持つ。30以上のデータ型が元から備わっている。多くの他の言語と同様、整数、10進数、文字列といった基本的な値がある。REBOLではさらに字句形式で識別されるデータ型があり、例えば、電子メールアドレス型 (name@host.dom)、URL型 (http://www.rebol.com)、マークアップタグ型 (<b>, <font size="2" color="blue">)、価格型 ($100.00, USD$25.25)、日付型 (30-Nov-2005, 1-Dec-2005/10:30-7:00)、時刻型 (12:00:00)、座標対型 (5x5)、タプル型 (255.255.255, 192.168.100.1)、単語列型 (how are you?) などがある。これらのデータ型はプログラマ以外にもわかりやすい字句形式を使っていて、それによってデータ交換言語として使えるようになっている。REBOLにおいて値をグループ化するのに使われる主なデータ構造を「ブロック」と呼び、これはLISPの「リスト」にある意味で似ている。

## 実装

REBOLインタプリタにはいくつかのエディションがある（/Core、/View、/Command、/Base、/Face、/Pro）。本稿執筆時点では、/Core が /Base 以外の他のエディションのサブセットになっていて、43 の[プラットフォームで利用可能になっている](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。

REBOLインタプリタのソースコードは非公開である。REBOL/Core と REBOL/View で開発したアプリケーションは有償配布しても課金されない。REBOL/Pro などの拡張エディションではライセンス料の支払いが必要である。これにはODBCアクセス、[ダイナミックリンクライブラリ](../Page/ダイナミックリンクライブラリ.md "wikilink")の利用、スタンドアロンのEXEファイル生成といった機能がある。

ランタイム環境は、現状では単一の実行ファイルとなっている。REBOL/Core では約300kB、REBOL/View（[GUIエディション](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")）は約650kBである。アプリケーションのスクリプトは数[キロバイト](https://ja.wikipedia.org/wiki/キロバイト "wikilink")を超えることは少ないため、インタプリタ本体とスクリプトを一枚の[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")に格納できるし、電子メールでスクリプトを送るのも容易で、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上で転送して実行することもできる。

インターネット上の各種プロトコルをサポートしており、[電子メール](../Page/電子メール.md "wikilink")エージェント、[Webアプリケーションといったインターネット](../Page/World_Wide_Web.md "wikilink")・アプリケーションも容易に書ける。

REBOL/View はプラットフォーム独立なグラフィック/サウンド・アクセスを提供しており、独自のウィンドウツールキットと拡張可能な[ウィジェット群を持つ](https://ja.wikipedia.org/wiki/ウィジェット_\(GUI\) "wikilink")。これにより、分散GUIアプリケーションが容易に構築できる。REBOLのダイアレクティング・モデルにより、軽量な[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")アプリケーションの開発もできる。

REBOLコミュニティは、"REBOL [desktop](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")" を通してリンクしている。REBOL desktop はインターネット上のREBOL関連ファイルをグラフィカルに表現したもので、REBOLインタプリタに付随してインストールされる。REBOL desktop 自体は[オープンソース](../Page/オープンソース.md "wikilink")のREBOLアプリケーションである。

## 例

コンソールに [Hello world](../Page/Hello_world.md "wikilink") と表示するだけなら、次のように打ち込めばよい。

``` rebol
  print "Hello World!"
```

クロスプラットフォームのGUI版では、次のようになる。

``` rebol
 REBOL [
   Title: "Hello World in a Window"
   File: %hello-view.r
   Date: 12-January-2002
]

view layout [
    text "Hello world!"
    button "Quit" [quit]
]
```

さらに、[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") と [SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink") を使った単純なインターネットアプリケーションの例を示す。

``` rebol
 REBOL [
   Title: "Web Page Emailer"
   File:  %sendwebpage.r
   Date:  12-January-2002
   Purpose: "Get an HTML document from the web and send it through e-mail"
]

send branko@collin.example read http://www.rebol.com
```

REBOL という単語で始まるヘッダ部は、インタプリタがスクリプトの開始を知るために必要とされる。ヘッダは単に `REBOL []` でもよいのだが、一般に例にあるような説明的記述をするのがよいとされている。

## 方言（ダイアレクト）

REBOLはコンテンツ依存言語であり、ダイアレクト（dialect）と呼ばれるドメイン固有サブ言語をサポートしている。例えば、*return* という単語の解釈がコンテンツによって変わることを見てみよう。通常、*return* は関数を完了して呼び出し元に値を返すのに使われる。しかし、*Visual Interface Dialect* (VID) では、*return* という単語があるとレイアウトエンジンが改行（carriage return）と解釈し、レンダリングペンを次行の先頭に持っていく。REBOLプログラマは独自のダイアレクトを生成でき、既存のREBOLの単語に別の意味を付与することができる。

ダイアレクトは、REBOLブロックを特定の方法で処理する関数で実装されるのが一般的である（後述の例のように文字列処理での実装もある）。同様に他の関数でも、ネイティブのダイアレクトとREBOLで書かれたダイアレクトを識別可能である。

ダイアレクトの例:

  - **do** ダイアレクト - REBOLの通常の **do** 関数が理解し解釈できる（ネイティブ）。
  - **reduce** ダイアレクト - **do**ダイアレクトで結果を集めるよう変更したもの（ネイティブ）
  - **compose** ダイアレクト - **reduce**ダイアレクトで括弧だけを評価するよう変更したもの（ネイティブ）
  - **function spec** ダイアレクト - 関数ヘッダ記述に使われるダイアレクト（ネイティブ）
  - **parse** ダイアレクト - [バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink")風の文法規則を記述するためのツール（ネイティブ）
  - *VID* - GUI用ダイアレクトで、**layout**関数として実装されている（mezzanine）。

ユーザーは任意のREBOL関数を使ってダイアレクトを生成できるが、**reduce** 関数と **compose** 関数がよく使われており、**parse** 関数はダイアレクト生成に最適化されている。

**parse**関数の目的は、[BNF風の形式の](../Page/バッカス・ナウア記法.md "wikilink")[Parsing Expression Grammarの構文規則を指定することでダイアレクトの解釈を与えることであり](../Page/Parsing_Expression_Grammar.md "wikilink")、[yacc](https://ja.wikipedia.org/wiki/yacc "wikilink")や[Bison](https://ja.wikipedia.org/wiki/Bison "wikilink")のような[構文解析](../Page/構文解析.md "wikilink")ツールに似ている。REBOLは実行時にそういった規則を解釈する。構文解析中に実行すべきことも指定できる。

**parse**関数は、REBOLブロックまたはREBOL文字列を処理するのに使われる。

**parse**による文字列処理は非常に柔軟性があるが、低レベルな手法であるため、手間がかかる。ブロック解析のほうが簡単だが、制限がある。ブロック解析では、ROBOLは書かれている規則をREBOLの値の並びとして[字句解析](../Page/字句解析.md "wikilink")する（文字列解析では文字と[区切り文字](https://ja.wikipedia.org/wiki/区切り文字 "wikilink")として解釈する）。そのため、より[抽象化された規則として記述できるが](../Page/抽象化_\(計算機科学\).md "wikilink")、通常のREBOLの字句形式にマッチしていなければならない。

### 構文規則

*parse* 関数に解釈させる規則群自体も REBOL のダイアレクトで書く。文字列として解析する場合、REBOLのデータ型の一部を規則に使用できる。ブロックとして解析する場合、全てのREBOLデータ型が使え、他にもダイアレクト構築を容易にする機能が使える。

#### 文字列解析例

最初の例は、文字列を解析して特定の単語を探し、関連するデータの一部を変数としてコピーし、他の場所でそれを使う。この例では、文字列からコピーされた部分も文字列である。具体的に言えば、"write" または "send" で始まる命令文型の文字列を入力として、簡単な構文解析で「何を」「誰が」「どうする」のかを把握する処理が記述されている。

``` rebol

 strings: [
    "write Graham a thank-you note"
    "send Allen the new source code"
]

foreach string strings [
    print string
    ; 規則はブロックで表され、角括弧で囲まれている。
    parse string [
        ; 各文字列は次のいずれかの単語で始まる。COPY は
        ; テキストの一部をコピーし、後でそれを使う。
        copy how ["write" | "send"] (print ["How:" how])
        ; ここで、次の空白までをコピーする。その後には "a" または
        ; "the" が続く。ここでは括弧を使って規則が一致したときに
        ; とるべき動作を定義している。
        copy who to " " ["a" | "the"] (print ["Who:" who])
        ; 最後に、文字列の最後までをコピーする。
        copy what to end (print ["What:" what])
    ]
    print ""
]
```

"parse string" ブロックの最後の行を見てみると、"copy what" は現在パーサが見ている位置（"a" または "the" の後）からのテキストをコピーすることを意味し、それを変数 "what" に代入する。また、ダイアレクトは "to end" を指定しているので、文字列の最後尾まで全てをコピーすることを意味する。従って "what" には第一の文字列なら "thank-you note"、第二の文字列なら "new source code" が代入される。

``` rebol
Print ["What:" what ]
```

と打ち込むと、以下のように出力される:

What: thank-you note

What: new source code

#### ブロック解析例

ファイル解析ユーティリティがあり、ユーザーが操作すべきファイルを指定し、それをいつ実行し、結果をどこに送り、誰に通知するかということを簡単に指定できるようにしたいとする。ダイアレクトは、この種のタスクに対して、柔軟なテキストベースのインタフェースを提供できる。

ダイアレクトは複数のアイテムを許容し、語順が変動しても問題なく、可読性のために人間が余分な単語を追加してもプログラムの動作には影響を与えない。

ここでは、ユーザーがアプリケーションに送るコマンドセットを2種類定義している。

``` rebol
 command-blocks: [
    [
        analyze %test-1.txt %test-2.txt
        post results to http://www.wikipedia.org/results.dat
        notify rebol-xyz@wikipedia.org at 10:00 and again at 10:00pm
    ]
    [
        at 10:00 and at 10:00pm analyze %test-1.txt notify
        rebol-xyz@wikipedia.org and reb-guy@wikipedia.org
        post to ftp://wikipedia.org/results.dat
    ]
]

; アポストロフィが前置された単語はマッチさせたいリテラル単語列である。
; 感嘆符が後置された単語はマッチさせたいデータ型である。
; SOME は "one or more" を意味する。正規表現の "+" に似ている。
; OPT はオプションを意味し、ゼロ個でも1個でもよい。
; SET マッチした値を後で参照できるよう単語と結びつける。
; ちょうど、変数への代入に相当する。

foreach block command-blocks [
    print mold block
    parse block [
        some [
            ['analyze some [set file file! (print file)]]
            | ['notify some [set who email! opt 'and (print who)]]
            | ['at set when time! (print when)]
            | ['post opt 'results 'to set target url! (print target)]
            | 'again
            | 'and
        ] to end
    ]
    print ""
]
```

この例で、file、email、time、url といったものは全てREBOLにおけるネイティブなデータ型であり、構文解析中にそれらの値を抽出して、直接 REBOL の式に適用可能である。例えば、 *who* の値は *send* 関数で電子メール送信に使われ、*target* の値は *write* 関数によるデータのポストに使われる。

## 関連項目

  - [Boo](https://ja.wikipedia.org/wiki/Boo_\(プログラミング言語\) "wikilink") - 同様の用途の言語だが、[共通言語基盤](https://ja.wikipedia.org/wiki/共通言語基盤 "wikilink")上で動作する。
  - [Oz (プログラミング言語)](../Page/Oz_\(プログラミング言語\).md "wikilink")
  - [Curl (プログラミング言語)](https://ja.wikipedia.org/wiki/Curl_\(プログラミング言語\) "wikilink")
  - [XL (プログラミング言語)](https://ja.wikipedia.org/wiki/XL_\(プログラミング言語\) "wikilink") - ダイアレクティング機能を持つコンパイラ言語

## 外部リンク

  - [REBOL Technologies](http://www.rebol.com) - 公式サイト。ダウンロードあり。
  - [REBOL Script Library](http://www.rebol.org) - 学習用のコード例がある。
  - [REBOL Essentials](http://www.plain.at/vpavlu/REBOL/tutorial/) - 言語入門書
  - [Carl Sassenrath's REBOL blog](http://www.rebol.com/cgi-bin/blog.r) - 開発者のブログ。開発予定などがある。
  - [Carl's Rebol 3.0 blog](http://www.rebol.net/cgi-bin/r3blog.r) - 次期リリースに関するブログ。
  - [REBOLWeek](http://rebolweek.blogspot.com) - REBOLコミュニティのニュースサイト
  - [RIX - the Rebol IndeXer](http://babelserver.org/rix) - REBOLコミュニティのニュースサイト
  - [Rebol Programming for the Absolute Beginner](http://musiclessonz.com/rebol_tutorial.html) - チュートリアル
  - [Liquid Rebol](http://www.pointillistic.com/open-REBOL/moa/steel/liquid/index.html) - REBOLベースの[データフロー言語](https://ja.wikipedia.org/wiki/データフロー言語 "wikilink")
  - [RebGUI](http://www.dobeash.com/rebgui.html) REBOL用UIフレームワーク

## 脚注

### 出典

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink")

1.
2.
3.
4.