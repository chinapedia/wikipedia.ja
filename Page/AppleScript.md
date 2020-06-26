> この記事は[AppleScript](https://ja.wikipedia.org/wiki/AppleScript)から翻訳されています。


**AppleScript**（アップルスクリプト）は、[アップルが開発した](../Page/アップル_\(企業\).md "wikilink")[Classic Mac OS](../Page/Classic_Mac_OS.md "wikilink")/[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用の[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の[スクリプト言語](../Page/スクリプト言語.md "wikilink")。System 7（Mac OS 7にあたる）から採用されている。

標準環境で利用でき、ある程度[自然言語](../Page/自然言語.md "wikilink")（[英語](../Page/英語.md "wikilink")）に似た構文を持つ。[制御構文](https://ja.wikipedia.org/wiki/制御構文 "wikilink")、[ハンドラや](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")[変数](../Page/変数_\(プログラミング\).md "wikilink")、[オブジェクトや](../Page/オブジェクト_\(プログラミング\).md "wikilink")[プロパティ](../Page/プロパティ.md "wikilink")の記述といった[プログラミング](../Page/プログラミング.md "wikilink")の基本機能を言語に備えており、Mac OSの[プロセス間通信](../Page/プロセス間通信.md "wikilink")機能の一つである[Apple eventによって](../Page/Apple_event.md "wikilink")、システムや様々な対応アプリケーションにまたがって制御できる。

AppleScriptはMac OSのスクリプティング機構[Open Scripting Architecture](https://ja.wikipedia.org/wiki/Open_Scripting_Architecture "wikilink") (OSA) に対応した言語（OSA言語）のひとつであり、[OS X v10.10よりJavaScript](https://ja.wikipedia.org/wiki/OS_X_Yosemite "wikilink") for Automation (JXA) も標準搭載されるようになった\[1\]。

## 特徴

### カバーエリアの広さ

[アプリケーション操作の自動化](../Page/アプリケーションソフトウェア.md "wikilink")、[シェル](../Page/シェル.md "wikilink")、[コマンドの呼び出し](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")、画面上の部品の強制操作にWebコンテンツの強制コントロール、[Cocoa](../Page/Cocoa.md "wikilink")[フレームワークの呼び出しに](../Page/アプリケーションフレームワーク.md "wikilink")[iCloud](https://ja.wikipedia.org/wiki/iCloud "wikilink")経由のコンテンツ更新など、[マクロ言語](../Page/マクロ言語.md "wikilink")としてはカバーできる範囲がとても広い。そのうえ、[GUIベースのアプリケーション開発まで行えるため](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、いったん覚えるとMacを用いた作業の生産性が向上する。ただし、他のアプリケーションを他の[コンピュータ](../Page/コンピュータ.md "wikilink")からも操作できるため、[セキュリティを考慮しさまざまな抑止機能がOSに用意されつつある](../Page/コンピュータセキュリティ.md "wikilink")(詳細は[\#制限機能](https://ja.wikipedia.org/wiki/#制限機能 "wikilink")を参照)。

Classic Mac OSからmacOSを通じて継承された唯一のテクノロジーであり\[2\]、海外を中心に古くから開発者コミュニティが形成され\[3\]、GUIベースのアプリケーションのコントロールについての知見が蓄積されている。

### 仕組み

AppleScriptは[OSAに準拠したスクリプト言語の一つであり](https://ja.wikipedia.org/wiki/Open_Scripting_Architecture "wikilink")、アプリケーション等の[プロセス](../Page/プロセス.md "wikilink")に[Apple eventを送ることにより自動操作を実現する](../Page/Apple_event.md "wikilink")。通常は[コンパイル済みの](../Page/コンパイラ.md "wikilink")[バイトコード](../Page/バイトコード.md "wikilink")が保存され実行される。このため、基本的にはOSのバージョンや[CPU](../Page/CPU.md "wikilink")の形式 ([68000](../Page/MC68000.md "wikilink"), [PowerPC](../Page/PowerPC.md "wikilink"), [x86](https://ja.wikipedia.org/wiki/x86 "wikilink"), [x64](https://ja.wikipedia.org/wiki/x64 "wikilink"))、記述した言語（AppleScript英語、AppleScriptフランス語、AppleScript日本語）などに依存しないコードが生成される。

AppleScriptの言語そのものが定義している[予約語](../Page/予約語.md "wikilink")（複数の単語による連語から構成される）は数十程度と少なく\[4\]、標準では絶対値を求める機能や三角関数の機能すら持たないが、Scripting Additions/OSAX（Open Scripting Architecture eXtension）\[5\]と呼ばれる機能拡張書類、あるいはAppleScriptそのもので記述したAppleScript Librariesによって命令を増やすことが可能となっている（サードパーティのOSAXはmacOS 10.14で廃止になった\[6\]）。

AppleScriptはMac OS上のアプリケーション間通信を基礎技術として用いているため、アプリケーションがApple eventに対応していればそのアプリケーションに処理を委ね、その処理結果を別のアプリケーションに対して用いることも可能である。また、現在のバージョンではUser Interface Scripting\[7\]あるいはGUI Scripting\[8\]\[9\]あるいはUI Element Scripting\[10\]と呼ばれる機能を用いて、スクリプトからアプリケーションにメニュー操作やキー入力を伝達することも可能になっている。アプリケーションは、システム経由で送られてきたApple eventメッセージを解釈して対応した処理を行い、処理結果を再びシステムを経由してApple eventメッセージとして返す。

バイトコードインタプリタ型の逐次実行で処理されるため、ネイティブコードに比べると実行速度は劣るものの、アプリケーションの機能呼び出しを行わない場合にはスクリプト言語としては十分な速度で実行される。ただし、アプリケーションの機能呼び出しはコストも高く、前述のGUI Scriptingを用いたメニューなどの強制操作を行うと、さらに処理コストが増加し、時間がかかる。

### ユーザインタフェース

AppleScriptは、簡素なダイアログ (display dialog、display alert)、ノーティフィケーションセンターへのノーティファイ (display notification)、ポップアップメニューからの項目選択ダイアログ (choose from list)、ファイル選択 (choose file)、フォルダ選択 (choose folder)、新規ファイル保存先パス選択 (choose file name) 、プログレスバー表示（Mac OS X v10.10以降。アプレット動作時のみ）などの、目的に特化した簡単なユーザインタフェースを提供している。

これら以外のユーザインタフェースを利用するために、現在利用できる手段で一番簡単なやり方は、Mac OS X標準搭載の「スイッチコントロール」でパネルを作成し、パネル内のボタンに対してアクション「AppleScript」を割り当てておくというものである。

Adobe InDesignなどの一部のアプリケーションでは、簡易的なユーザーインタフェースをAppleScriptのプログラムから動的に生成する機能を備えている。

本格的な、自由度の高い自作のインタフェースを持たせるには、[Xcode](../Page/Xcode.md "wikilink")上で「AppleScript App」プロジェクトを作成し、その中にAppleScriptコード（AppleScriptObjC）を記述する。Xcode上で一般のアプリケーション開発と同様にユーザインタフェースを作成できる。コントロール（GUIの部品）が操作されると、AppleScriptコード中の対応するイベントハンドラが呼び出される。

### 開発環境

macOSにはスクリプトの編集・実行ツールである[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")（[Mac OS X v10.0](../Page/Mac_OS_X_v10.0.md "wikilink")〜[v10.4は](../Page/Mac_OS_X_v10.4.md "wikilink")[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")、[Mac OS X v10.5](../Page/Mac_OS_X_v10.5.md "wikilink")〜[v10.9はAppleScriptエディタ](https://ja.wikipedia.org/wiki/OS_X_Mavericks "wikilink")（[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")の名称が変更されたもの）、[Mac OSでは](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")『スクリプト編集プログラム』）が付属する。

[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")にAppleScript対応アプリケーションの[アイコン](../Page/アイコン.md "wikilink")を[ドラッグ・アンド・ドロップ](../Page/ドラッグ・アンド・ドロップ.md "wikilink")するとAppleScript用語辞書が表示され、これを参照しつつアプリケーションのコントロールを行う処理を記述する\[11\]。

[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")にはブレークポイント設定や変数内容のモニタリングなどの機能はないため、これらの機能を利用したいユーザーは[Late Night Software社の「Script Debugger」](http://www.latenightsw.com)を用いる必要がある。また、Cocoaオブジェクトのログ表示やAppleScript Librariesに添付するAppleScript用語辞書の編集についても[「Script Debugger」](http://www.latenightsw.com)で行える。

AppleScriptへのコードサインはApple純正の[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")およびScript Debuggerで行うことができる。Mac App StoreにAppleScriptで作成したアプリケーションを提出するには、Xcode上で記述・コードサインする必要がある。

その他、テキストで書いたスクリプトをコマンドラインからosascriptコマンドでコンパイル・実行することも可能である。

アップル純正の[統合開発環境](../Page/統合開発環境.md "wikilink")[Xcode](../Page/Xcode.md "wikilink")（旧Project Builder）上でAppleScriptによるアプリケーション開発を行うこともできる。AppleScriptから直接Cocoaの機能を呼び出せる「AppleScriptObjC」\[12\]が提供されている（Mac OS X v10.1〜v10.5ではAppleScript Studio）。ユーザーインタフェース作成について[Interface Builderを用いる点は以前のAppleScript](../Page/Interface_Builder.md "wikilink") Studio（Mac OS X v10.6で廃止）とかわりないが、AppleScript用語辞書を用いて各種GUI部品にアクセスするのではなく、[Interface Builder上でバインディングによりAppleScriptプログラム中のプロパティ値にひもづけしたり](../Page/Interface_Builder.md "wikilink")、Cocoaの各種フレームワーク内のメソッドを呼び出す方式に変更された。

### 異なるOSバージョン間の互換性

AppleScript書類のフォーマットは維持されているため、基本的には互換性が確保されている。これまでMac OS X v10.4の[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")[CPU](../Page/CPU.md "wikilink")への移行や、[Mac OS X v10.7の](https://ja.wikipedia.org/wiki/Mac_OS_X_Lion "wikilink")[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")への移行などのOSの基盤の大変革期があったが、AppleScriptそのものについてはほぼ影響はなかった。AppleScriptの処理系そのものの変更が小刻みであったため、15年前に作られたソートルーチンがそのまま使えたりもする。

ただし、AppleScriptだけでなくOSAXや外部のアプリケーションの機能を利用していた場合には、部品ごとに確認が必要となる。

まず、macOS標準添付のアプリケーションの機能がOSバージョンごとに異なる。これらを呼び出す処理を行っている場合にはチェックが必要である。とくに、AppleScriptにOSの機能を提供するために用意されている補助アプリケーションはOSバージョンによって変更されることがあるため、その存在および代替機能を確認する必要がある。一般的に、古いバージョンから新バージョンへの移行は、それなりに手間はかかるものの確認作業レベルで済む。

逆に、新しいバージョンのOSから古いバージョンのOSにScriptを移植する場合には大幅に作業量が増える。古いOSには固有のバグもあるため（Mac OS X v10.5以前は日本語のパスの扱いに問題があった）、それらを考慮した処理に変更する必要も生じる。古いmacOSが動作する実機と関連アプリケーションを用意し、きちんと動作検証や書き換え作業が必要になる。

GUI Scriptingを利用している場合には、メニュー構成やボタンの文字を変えただけで動かなくなる可能性があるため、そもそも異なるOSバージョン間でそのまま動く可能性は低い（ただし単純な修正で対応できる）。

OS X v10.10以降ではAppleScript側が想定するAppleScript処理系のバージョン（≒ macOSそのもののバージョン）をuseコマンドを使って表記できるようになった。

| AppleScript version | macOS version        | useコマンド記述                     |
| ------------------- | -------------------- | ----------------------------- |
| 2.4                 | 10.10                | use AppleScript version "2.4" |
| 2.5                 | 10.11, 10.12         | use AppleScript version "2.5" |
| 2.7                 | 10.13, 10.14 , 10.15 | use AppleScript version "2.7" |
|                     |                      |                               |

また、macOS 10.14以降でサードパーティ製のOSAXが使用できなくなったため、それらを使用しているScriptをmacOS 10.14以降で動かす場合には代替機能を探す必要もある（Cocoaの機能を呼び出したり、shellコマンドの機能を呼び出したりするのが一般的）。

### 構文

[HyperCard](../Page/HyperCard.md "wikilink")用のスクリプト言語である[HyperTalk](../Page/HyperTalk.md "wikilink")に似た、英語に近い構文が採用されており、基本的には習得しやすい。機能の異なるアプリケーションを操作するためには、それぞれアプリケーションごとに異なる命令やオブジェクト構造を知る必要があり、AppleScript対応アプリケーションのアイコンを[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")でオープンすることで表示される「AppleScript用語辞書」を参照しつつ記述することになる。

初期は日本語表現形式を含む英語以外の言語による記述も可能だったが、Mac OS 8.5以降は英語表現形式のみが採用されている。英語表現形式の場合も[変数名は](../Page/変数_\(プログラミング\).md "wikilink") | で囲むことで日本語などを使用できる。

Mac OS X v10.10でAppleScriptObjCがXcode上のみならず、[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上でも利用できるようになったため、Objective-C風の表記も標準採用された。

**スクリプトの例**（変数「持ち物=myItem」の中身が0だったらダイアログを表示する）

**英語**

``` applescript
if myItem = 0 then
    display dialog "持ち物がありません" buttons {"OK"} default button "OK"
end if
```

通常は上記のように記述するが、より英文に近い以下のようなコードも記述できる。ただし複数の処理を一行の[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")に組み込むことはできないので、先ほどの構文を使用することになる。下記のコードでは[比較演算子](https://ja.wikipedia.org/wiki/比較演算子 "wikilink")の“等価”を表す = が is に置き換えられている（is は is equal to と書くこともできる。このような同義語が数多く存在するのもAppleScriptの特徴のひとつ）。

``` applescript
if myItem is 0 then display dialog "持ち物がありません" buttons {"OK"} default button "OK"
```

**変数名に日本語を用いた例**

``` applescript
if |持ち物| is 0 then display dialog "持ち物がありません" buttons {"OK"} default button "OK"
```

**日本語**（現在は利用できない）

``` applescript
もし「持ち物」が0ならば
    “持ち物がありません”をボタンリスト：｛“OK”｝、デフォルトボタン：“OK”で表示する
以上
```

### AppleScriptObjC構文

Mac OS X v10.6で部分的に導入され（Xcode上のみ）、Mac OS X v10.10で[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")でもCocoaの機能を利用するAppleScriptObjCが導入された。このため、現行のmacOS上ではどのマシンでも、どのAppleScriptランタイム環境上でもCocoaの機能を利用できる状態になっている。

AppleScriptObjCは従来のAppleScriptと比べて10倍以上の高速処理が可能である\[13\]。ただし、それはCocoaのメソッドを呼び出した場合であり、従来型のAppleScriptをAppleScriptObjC環境で記述しても速度は変わらない。

また、AppleScriptObjCではObjective-CのBlocks構文やprotocolをサポートしていないため、Cocoaのフレームワークすべてが利用できるわけではない。Cocoaのクラス名やメソッド名でAppleScriptの予約語とコンフリクトするものについては「|」で囲う必要がある（例：NSURL、URL、document、count、propertiesなど）。ドットシンタックスもサポートしていないため、現行のObjective-C 2.0にくらべるとやや冗長な表記になる。

Cocoaオブジェクトの結果表示やログ表示については、macOS標準添付の[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")ではサポートしていない。Cocoaオブジェクトのログ表示などを利用するためには[サードパーティー](../Page/サードパーティー.md "wikilink")の開発ツール「[Script Debugger](http://latenightsw.com)」の利用が必要である。

**スクリプトの例**（変数「aString」のアルファベット大文字を小文字に変換する）

*Objective-C*

``` objective-c
NSString *aString = @"123/abc/ABC.txt";
[aString lowercaseString];
```

*AppleScriptObjC*

``` applescript
use AppleScript version "2.4"
use scripting additions
use framework "Foundation"

set aString to current application's NSString's stringWithString:"123/abc/ABC.txt"
(aString's lowercaseString()) as string
```

AppleScript対応アプリケーションへのtellブロック内でAppleScriptObjCの命令を呼び出すとエラーになる。このため、たとえばAdobe InDesignの書類から得られたデータをAppleScriptObjCを用いて高速にソートしたい場合などは、AppleScriptObjCの機能部分をサブルーチンとして分離し、InDesignへの命令ブロックと明示的に分ける必要がある。

なお、AppleScriptObjCで実行されるCocoa機能呼び出しはARC環境下で実行されるため、releaseなどのメソッドを呼び出すと実行環境ごとクラッシュする。

### 独特な挙動

スクリプトエディタ上でのコンパイル（構文確認）時に演算の優先順位を指定するため、AppleScript処理系がソースコード内にカッコ（「（」「）」）を自動的に補う動作を行う。ユーザーはこのカッコが自分の意図に合うかどうかを判断し、適宜カッコを補ったり移動させる必要がある。

カッコが自動で付加されるのは、主に四則演算や文字列の連結演算、Cocoaオブジェクトへのメソッド実行などの記述時である。

### 独特な要素

英文風に記述するため、「無意味句」を入れることができる。無意味句の代表的なものに「the」がある。theはプログラム内で何もプログラム的な動作を行わない。実行時に無視される。

``` applescript
set end of aList to 1
```

のような配列変数の末尾に数値を追加する記述を行なった場合、英文風に読みやすくするため、

``` applescript
set the end of aList to 1
```

のように無意味句を補うことができる。

無意味句はプログラム的な動作を何も行わないが、それら自体が存在し、無意味句同士は別物として識別される。そのため、無意味句を補助的に用いてサブルーチン（ハンドラ）の宣言を行うことも可能。

AppleScriptが定義している無意味句には、

``` applescript
about, above, against, apart from, around, aside from, at, below, beneath, beside, between, by, for, from, instead of, into, on, onto, out of, over, since, thru (throughも可), under
```

などがあり、サブルーチンのパラメータを指定する装飾子としてこれらの無意味句を利用できる。

``` applescript
set a to aSub for 10 at 20
--> 30

on aSub for aInt at bInt
      return (aInt + bInt)
end aSub
```

## アプリケーション操作対象

アプリケーションの操作による作業の自動化や、複数のアプリケーションの操作によるソフトウェア・ロボットの構築が可能であるが、操作対象の種類によって利用する技術や手法が変わる。

### ローカルアプリケーション

[Safari](../Page/Safari.md "wikilink")やコンタクト、カレンダーなどのmacOS標準添付アプリケーションの多くがAppleScriptからのコントロールに対応しており、主要機能にアクセスできる。

ただし、対応アプリケーションであっても機能のすべてがAppleScriptに解放されているわけではない。AppleScript用語辞書に定義されている範囲のみである。

そのため、前述のGUI Scriptingによるメニューやボタンなどの強制操作が時と場合によって必要になる。この強制操作機能はOSのデフォルト設定ではオフになっているほか、アプリケーション/アプレット/Scriptごとに許可/禁止するようになっている。

### UNIXコマンド

do shell scriptコマンドでBSD (UNIX) レイヤー上のコマンドを呼び出すことができる\[14\]。ただし、Terminal.app上とdo shell scriptコマンドでは設定されている環境変数が異なるため、Terminal.app上で実行できていた処理ができなくなる場合がある。特に、指定したコマンドにパスが通っていないことや、カレントディレクトリが異なること等はエラーの原因となる。これは環境変数の内容を明示的に指定することや、利用コマンドをフルパスで表記することで回避できる（環境変数内容はenvコマンドを実行して確認できる）。

### リモートアプリケーション

macOS標準装備の「リモート[Apple events](../Page/Apple_event.md "wikilink")」の機構を用いて、TCP/IPネットワーク（主にLAN）内の他のMac上のアプリケーションをコントロールできるようになっている。ただし、セキュリティ確保のためmacOS標準装備のアプリケーションの多くは、この機能が禁止されているほか、OSのデフォルト設定ではリモート[Apple eventsはオフになっている](../Page/Apple_event.md "wikilink")。

1台のMacでは処理が追いつかない場合、この機構を用いて複数台のMacに仕事を割り振り分散処理を行うことができる。また、Mac上で稼働する仮想環境上でmacOSを動作させ、仮想環境との間での分散処理も可能である\[15\]。

### Webサービス

SOAP、XML-RPCを呼び出すための命令が標準で装備されている（call soap、call xmlrpc）\[16\]\[17\]\[18\]\[19\]\[20\]。Cocoaの機能を用いてRESTful APIを呼び出すことも可能である\[21\]。

これらのサービスが存在しないサイトに対しても、Safariのdo JavaScriptコマンド経由で操作したり、GUI Scriptingで強制的に操作することで、Webサービスにログインして必要な情報を取得するなどの処理が可能である。

### iOSアプリケーション

[iOS上でAppleScriptが動くわけでも](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、iOSのアプリケーションを直接コントロールできるわけでもないが、iCloudを経由して間接的にデータの変更を行える。たとえば、macOS上のリマインダーを更新するとiOS上のリマインダーも更新される。これを利用して、iOS側に大量のデータを登録したい場合にMac上でAppleScriptなどによってデータを追加するといった方法が可能である。また、iPhoneとひもづけされたMacからAppleScriptを用いて電話をかけたりSMSメッセージを送信したりもできる\[22\]。

iOSシミュレータ上で動くiOSアプリケーションもGUI Scriptingにより操作や情報の取得などが可能である。そのため、AppleScriptからシミュレータ上のiOSアプリを操作し、操作テストを実施して段階ごとに画面キャプチャを記録することも行われている。

### 各種フレームワーク

Mac OS X v10.10以降では、Apple純正およびサードパーティー製CocoaフレームワークをAppleScriptから直接呼び出すことが可能となっている\[23\]。また、コンタクト（住所録）やカレンダーの情報をフレームワーク経由で検索・操作できるようになった\[24\]。iTunes Libraryの検索もiTunes.app経由やiTunes Music Library.xmlを検索するよりも高速に行える。

### AppleScript Libraries

Mac OS X v10.9以降で、AppleScript自体をライブラリ化して再利用できるようになった。さらに、このライブラリにはAppleScript用語辞書を持たせることが可能なため、AppleScriptの命令語をAppleScriptで記述したライブラリによって拡張することが可能である。

## さまざまな実行環境

AppleScriptは中間コードに翻訳されて逐次実行されるが、以下のようなさまざまな保存・実行環境（ランタイム環境）を持つため、実行環境によって動作が微妙に異なり、想定していた通りに動かない場合がある。

また、実行中のログ表示が行えるのは[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")でオープンして[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")で実行させた場合、およびXcode上で作成してデバッグビルドを行なっている場合の２つのケースにかぎられる。フォルダアクションで実行中のAppleScript書類を[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")でオープンさせたからといって、フォルダアクションで実行中のAppleScriptのログが[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上にログ表示されることはない。

### スクリプトエディタ上で実行

[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上に記述して、[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上で実行する形態である。この際の実行環境は[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")であり、途中でAppleScriptの実行を停止させたり、ログ表示させた内容を確認したりできる（ログ表示させると実行速度がいちじるしく低下する）。セキュリティ上の制約がもっとも少ない実行環境でもあり、他の実行環境では動かせないコードもこの環境で動くケースが多い。

### アプレット/ドロップレットとして保存して実行

[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上で記述して、アプリケーションとして保存、あるいはアプリケーションとして書き出したものである。この形態のものをアプレットと呼ぶ。アプレット実行時にはアプレット用のランタイム環境が用意されている。この環境で実行すると、on idleによるタイマー割り込み、ファイルやフォルダをドラッグ＆ドロップ受信する機能、ハンドラの実行後に終了しない、プログレスバーの表示機能（Mac OS X v10.10より）などの機能が利用できる。ファイル/フォルダのドラッグ＆ドロップを受け付けるアプレットをドロップレットと呼んで区別する（アイコンが異なる）が、ランタイム環境は同じである。

アプレット実行時にログ表示などの機能は利用できないため、この実行形態のままではバグの確認や修正が困難である。アプレットとして書き出す前に[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上で内容に問題がないことを確認する必要がある。

### Automator上で実行

[Automator](https://ja.wikipedia.org/wiki/Automator "wikilink")のワークフロー記述の一部としてAppleScriptを使用することもできる。Automator上のアクション「AppleScriptを実行」が[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")に近い機能（ログ表示、結果表示）を持つが、他のAppleScript対応アプリケーションのAppleScript用語辞書をブラウズしたり、途中で実行を停止させるなどの機能はない。

### Cocoa-AppleScript Appletとして保存して実行

Mac OS X v10.7で導入された。[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上で「ファイル」＞「テンプレートから新規作成」＞「Cocoa-AppleScript Applet」を選択することで新規作成できる。AppleScriptObjCによるプログラムを[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上で記述できるが、Interface Builderによるユーザーインタフェースの作成が行えず、デバッグ機能も乏しい。実行はアプレット形式でのみ行う。

### Xcode上でAppleScript Appとして作成してビルドして実行

Xcode上で「File」＞「Project」＞「Other」＞「AppleScript App」を呼び出すと作成される。Mac App Store上でのアプリケーション販売が可能な形式である。一般的なCocoaアプリケーションをAppleScriptで開発する環境であり、一般的なCocoaアプリケーションに近いものが作れるが、一般的なCocoaアプリケーションを作成するレベルの知識が必要とされる。Xcode内蔵のエディタ上で編集するAppleScriptは、文法要素に応じた構文色分け機能が利用できず、デバッグも行いにくい。複数のスクリプトファイルにプログラムを分割した場合のハンドラ呼び出し方法にクセがある。

### スクリプトメニューに登録して実行

macOSのメニューバーから所定のフォルダ内のAppleScriptを実行できる、macOS標準装備の「スクリプトメニュー」に登録・実行した場合の実行環境も、OSのバージョンに応じてさまざまな変更が加わってきた。Mac OS X v10.10からはosascriptコマンドで実行する実装になった。このため、スクリプトメニューから複数のAppleScriptを同時に実行させることが可能になったが、実行するScript同士で共通のアプリケーションにアクセスした場合のバッティングまでは面倒を見てくれない。スクリプトメニューから実行中のScriptの停止を行えるが、実行中のログ表示はできない。

### フォルダアクションに登録して実行

指定のフォルダ内容を数秒間隔で監視し、変更が加わるとAppleScriptの実行を行う機構である。ランタイムの差異が問題を生むというよりも、このフォルダアクションの機構そのものがmacOSのバージョンによってはうまく動作していない（Mac OS X v10.10）ことが問題である\[25\]。

### Terminalからosascriptコマンドで実行

OSバージョンによっては、display dialogなどのコマンドが利用できなかったが、Mac OS X v10.10以降は[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上での実行にきわめて近いランタイム環境が提供されている。全く同一ではないため、[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上で記述すれば発生しないような問題に直面する場合がある。一例として、AppleScript中からNSWindowを動的に生成し、そのウィンドウ上の各種GUI部品でユーザーからの操作を受け付けたい場合、操作が処理されないといった問題がある。

### Switch Control上の「AppleScript」アクションから実行

macOSのアクセシビリティ系の機能に、フローティングパレット上に配置したボタンからキーボードショートカットやAppleScriptの実行を行えるSwitch Controlがある。バンドル形式のScriptを読み込んで実行できない、Scriptのバンドル内に実行ファイルを入れて呼び出すことがない、ユーザーディレクトリ下のAppleScriptライブラリを認識しない、といった運用上の制約がある。

### 「音声入力コマンド」の「高度なコマンド」＞「ワークフローを実行」でAppleScript実行

日本語音声認識でAppleScriptを実行できる。実行可能形式は、AppleScriptのフラット形式（.scpt）およびAppleScriptアプレット。Siriとは別の音声認識コマンドであり、あらかじめ指定しておいた固定文字列を日本語音声認識して、合致すればコマンドを実行する。

### アプリケーション内のScript実行機能で実行

FileMaker Proを外部からAppleScriptでコントロールするよりも、FileMaker Proスクリプトの「AppleScriptを実行」スクリプトステップ中にAppleScriptをコピー＆ペーストで入れて実行する方が数倍高速に実行される。画面の再描画などを抑止するほか、高速実行するための仕組みを備えている。

Microsoft OfficeのVBAスクリプト内でも、AppleScriptを呼び出す仕組みが用意されている。Excel v.14.xまでは「MacScript」コマンドにより文字列で与えたAppleScriptが、Excel v.15.xでは「AppleScriptTask」コマンドによりファイル名を指定して外部のAppleScriptを実行できるようになっている。

同様に、Adobe InDesignの「スクリプト」パレット中からAppleScriptを呼び出すことが出来、この際に画面の再描画を抑止できるため高速実行（おおよそ2倍）が可能となっている。ただし、Adobe InDesignについては大量のデータ処理時にクラッシュが発生するため、処理速度より安定稼働を重視すると外部からのコントロールも選択肢に入る。

### Script Debugger上でデバッグ実行

AppleScript専用のサードパーティー統合開発環境といえる[Script Debugger](http://www.latenightsw.com)では、デバッグ時にAppleScript互換の「AppleScript Debugger」というAppleScriptとは別のOSA言語を実行することになる。厳密にいえばAppleScriptそのものを実行するわけではないため、振る舞いが異なる箇所が出てくることは否定できない。ただし、以前（Classic Mac OS時代）に比べると純正AppleScript環境との互換性は大幅に高まっている。強力で便利な環境であるが、「デバッグ時以外はScript Debuggerを使うべきではない」という方針の開発現場もあるのは、この「互換性問題」ゆえである。

## 運用上、注意すべき項目

` `

### 構文チェックが甘いので間違っている箇所を見つけにくい

[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")上でのコンパイル（実質的には構文チェック＋中間コードへの置き換え）時には、AppleScriptの基本的な文法を外れなければ、それがたとえ実行できない命令の組み合わせであってもエラーにならない。実行時にエラーとなる。FinderのAppleScript用語辞書を見ていると「make new application」といったできそうもないプログラムを組めそうに見え、実際にFinderへのtellブロック内に記述するとコンパイルを通ってしまう。

``` applescript
tell application "Finder"
    make new application
end tell
```

実際には、アプリケーション側が想定している命令語の組み合わせは限定されたものである。また、想定された条件下によっては実行できるが、条件がそろわないと実行してもエラーになったり無意味な結果になるものもある。このため、アプリケーションが備えている機能を逸脱しない表記、アプリケーションの用語辞書で実現可能な記述パターンの情報を収集することには大いに意義がある（Appleが主催するメーリングリストのアーカイブの検索がこれに適している）。また、Scriptはこまめに実行して想定どおりの実行結果が得られているかを確認するとよい。

### 機能の分布が不均一

たとえば、printコマンドでプリンタを指定して書類を印刷する機能が存在していても、LAN内に存在するプリンタ名一覧を取得する機能はデフォルトでは用意されていない。同様に、テキストの音声読み上げを行うsayコマンドで音声キャラクタの名称を指定できるのに、現在システムにインストールされている音声名称の一覧を取得する機能が存在していない。このため、shell scriptやCocoaのサービスを呼び出して、取得する手段を別途用意する必要がある\[26\]\[27\]。

### 特定オブジェクトの抽出にフィルタ参照が重要

何らかの条件に基づいてオブジェクトを抽出する処理が、アプリケーションコントロールでは日常的に発生する。たとえば、リマインダーで名称（name）に「発売日」を含む項目のみ抽出するといった処理である。そのような場合に、オブジェクトの抽出をせずに「とりあえずすべてのオブジェクトを取得して、ループで条件一致するものを抽出する」ようなコードでは処理が遅くなってしまう。フィルタ参照\[28\]を使って対象オブジェクトのしぼりこみを行うと速度を向上できる。

### 記述方法によって処理速度が大幅に変わる

何らかのオブジェクトの属性値を取得したい場合に、複数の属性値を何回かに分けて取得するよりもpropertiesでまとめて属性を取得した方が速いケースなどがある。アプリケーションをコントロールするために存在しているAppleScriptであるが、アプリケーションとの通信回数を減らすことが処理の高速化につながる。

例えば、指定フォルダ以下の全てのファイルを処理する場合、Classic Mac OS時代にはFinderに対して再帰処理で取得するように書いていたが、現代のmacOSではSpotlightを用いてファイル一覧を取得するとずっと速く処理できる。このように、macOSの機能の移り変わりを意識していないと処理速度が大幅に変わる。

### アプリケーションの過度のローカライズにともなう互換性問題

iTunes、Keynote、Pages、Numbersなどアップル純正アプリケーションに固有の問題が存在する。アプリケーションのローカライズをやりすぎて、AppleScript関連の機能までローカライズされてしまうことが多々ある。このため、海外で流布しているAppleScriptの、主にオブジェクト名称を英語名表記から日本語名表記に変更しないと日本語環境上では実行できない（エラーになる）ケースが存在する\[29\]。

## 制限機能

あまりに拡張され、できることが増えすぎたため、AppleScriptの一部機能を抑止するための機構がmacOSに用意されつつある。以下の機能についてはデフォルトでは禁止状態になっているが、管理者パスワードを入力すれば実行を許可するようになっている。

### リモートApple Eventsへの応答禁止

ネットワーク上の他のMacからのコントロールを行うリモートApple Eventsに対し、macOS標準装備の各アプリケーションは応答しないようになっている。また、出荷時のデフォルト設定で、リモートApple Eventsはオフになっている。

### GUI Scriptingの実行禁止

画面上のメニューやボタンなどを操作するGUI Scriptingについては、「システム環境設定」の「セキュリティとプライバシー」＞「アクセシビリティ」で個別に許可を行うようになっている。デフォルト設定では、どのプログラムに対しても許可していない。

### Safari上でのdo javascript命令の実行禁止

Safari 9.1.1より、「開発」メニューに「Apple EventsからのJavaScriptを許可」の項目が新設され、これにチェックを入れないとAppleScriptからSafariに対してdo javascript命令を実行できなくなった\[30\]。いったん許可すれば、その状態は継続される。

### FileMaker Pro上での拡張アクセス権におけるApple Eventによる操作許可設定

FileMaker Pro v16より、FileMaker Script中におけるAppleScriptの実行（正確にいえば、AppleScriptからFileMaker Pro自身を操作すること）がデフォルトの権限セットのままでは許可されない状態になっている。そのため、より以前のバージョンで作成したFileMaker ProデータベースをFileMaker Pro v16でオープンすると、FileMaker Script Step実行時に「実行権限エラー」ダイアログが表示され、Script Stepの実行が行われないという現象に直面することがある。このような場合には、拡張アクセス権で「Apple EventおよびActive-XによるFileMaker操作の実行を許可」にチェックを入れれば実行できるようになる。

### 「セキュリティとプライバシー」による権限設定（macOS 10.14より）

macOS 10.14より、システム環境設定の「セキュリティとプライバシー」＞「プライバシー」項目にセキュリティ度を調整するための各種機能が追加され、AppleScriptもその影響を受けるようになった。

「フルディスクアクセス」項目では、動作中のMacのすべてのユーザーに対して、ユーザー自身のメール、メッセージ、Safari、ホーム、Time Machineバックアップなどのデータや特定の管理設定へのアクセスを許可する。AppleScriptを利用するユーザーはこの項目に「[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")」と「スクリプトメニュー」を登録しておく必要がある。

「オートメーション」項目では、他のアプリケーション制御の許可、および取り消しを行える。[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")以外のアプリケーションで、他のアプリケーションを制御する場合には、動作中の最初の要求時にユーザーに対して承認を求めるダイアログを表示する。承認されたアプリケーションはこの「オートメーション」項目に表示されるようになる。実行したユーザーが承認しなかった場合にも、本項目にチェックボックスがオフになった状態で表示されるため、あとからシステム環境設定上の本項目において承認を行う（チェックボックスをオンにする）ことが可能である。

なお、一度「オートメーション」項目に登録され、ユーザーの承認を得ていれば、毎回ユーザーの承認ダイアログが表示されることはない。

逆に、本「オートメーション」項目に意図的に登録させたい場合、アプリケーションのバージョン番号を確認したり最前面に表示させる（activate）コマンドを実行させる程度ではシステムが反応しない。他のアプリケーションを操作するAppleScriptアプレット/AppleScriptアプリケーションにおいて、初回起動時に「オートメーション」項目に登録される程度の簡単な（害のない）アプリケーション操作を意図的に行う必要が生じるようになった。AppleScript側から任意のアプリケーションに対する操作が許可されているかを知ることは、サードパーティのフレームワークを呼び出すことで可能となっている\[31\]。

### SIPによる機能制限（macOS 10.14より）

macOS 10.11以降、SIPによる機能制限が段階的に強化され、macOS 10.14においてはApple純正の[スクリプトエディタ](../Page/スクリプトエディタ.md "wikilink")にも制限が加わった。ホームディレクトリ下の「ライブラリ」フォルダ中の「Frameworks」フォルダ（デフォルトでは存在しない）へのアクセスがSIPにより禁止された。macOS 10.14上でこの制限を回避するには、サードパーティの開発環境「Script Debugger」を利用するか、SIPそのものを解除する必要がある。

### リモートApple Eventsの応答ユーザー名制限（macOS 10.15より）

macOS 10.15以降、リモートApple Eventsでネットワーク上の他のMac上のAppleScriptから命令を受け付ける場合、呼び出す側と受け付ける側のユーザー名が同じである必要があるようになった。なお、簡単なシェルコマンドでこの制限は無効にすることができる。

## バグ

### macOS 10.12, Sierra

macOS側のセキュリティ機能とAppleScriptの処理系のすり合わせが不十分なままOSがリリースされてしまったために、macOS 10.12, SierraにおいてはAppleScriptをドロップレットとして保存し、ファイルをドラッグ＆ドロップした場合には、ファイルの処理が行われなかったりファイル処理の順序が以前のOSのとおりに行われなかったりする。

これは、ファイルの拡張属性（Xattr）の１つ「com.apple.quarantine」により発生する。インターネット上からダウンロードしたファイルなどは、その安全性が担保されていない状態であると（macOSが）みなし、この「com.apple.quarantine」属性が添付される。

ユーザーの操作によりファイルのオープンを許可された（「ダウンロードされたファイルですが、オープンしてもよいですか？」という確認ダイアログでユーザーに承認）場合には処理されるが、同属性がついたままだとドロップレットによる処理が行われない。一応回避手段は存在するが、初心者には理解が難しいものとなっている。 \[32\]。

sayコマンドで日本語読み上げ音声を指定して「もげる」「捥げる」を読み上げると正常に読み上げられない（NSSpeechManagerのバグで、SwiftやObjective-Cでも同様のバグが発生し、iOSでも状況は同じ）。\[33\]\[34\]。

Enum「NSNotFound」の定義が間違っており、-1ではない値を返す（10.13.1にて修正）。

``` applescript
use AppleScript version "2.4"
use scripting additions
use framework "Foundation"

current application's NSNotFound
--> 9.22337203685478E+18 --macOS 10.12.x
--> -1--macOS 10.13.1など通常の挙動
```

### macOS 10.13, High Sierra

AppleScriptからCocoaの機能を呼び出す際にScripting Bridgeの仕組みが利用されているが、このScripting Bridgeの定義ファイルに問題があり、いくつかの機能が正常に呼び出せない状況が確認されている。\[35\]。

NSRectが属性ラベルつきのレコード型ではなくリスト型に変換されるようになっている。

``` applescript
use AppleScript version "2.4"
use scripting additions
use framework "Foundation"

current application's NSMakeRect(0, 0, 100, 100)
--> {origin:{x:0.0, y:0.0}, size:{width:100.0, height:100.0}}--通常の挙動（macOS 10.12.x)
--> {{0.0, 0.0}, {100.0,100.0}}--macOS 10.13.xの挙動
```

PDFViewに対してcurrentPage()を実行してもPDFPageが返ってこない。このため、PDFView上でPDFを表示させるGUIプログラムに影響が出ている。\[36\]

## 脚注

## 参考文献

  - 「アップルスクリプトBasic Magazine Vol.2」, Empty Party (2020）
  - 「AppleScriptの穴Blogアーカイブvol.6」, Piyomaru Software (2020）
  - 「AppleScriptの穴Blogアーカイブvol.5」, Piyomaru Software (2020）
  - 「AppleScriptの穴Blogアーカイブvol.4」, Piyomaru Software (2019）
  - 「アップルスクリプトBasic Magazine Vol.1」, Empty Party (2019）
  - 「AppleScriptの穴Blogアーカイブvol.3」, Piyomaru Software (2018）
  - 「AppleScriptの穴Blogアーカイブvol.2」, Piyomaru Software (2018）
  - 「AppleScriptの穴Blogアーカイブvol.1」, Piyomaru Software (2018）
  - 「Keynote Control with AppleScript 1」, Piyomaru Software (2017）
  - 「Keynote Control with AppleScript 2」, Piyomaru Software (2017）
  - 「iTunes Control」, Piyomaru Software (2017）
  - 「AppleScript最新リファレンス」, Piyomaru Software (2016）
  - 「最新事情がわかるAppleScript 最新10大技術」, Piyomaru Software (2016）
  - 「AppleScript Studioでぜんまいびゅんびゅん」, 掌田津耶乃 (2003）ISBN 4-7561-4279-6
  - 「AppleScriptリファレンス」, こばやしゆたか／AppleScriptリファレンス制作委員会 (1999）ISBN 4-7973-1011-1
  - 「AppleScript言語ガイド　英語表現形式」, Apple Computer Inc. (1997） ISBN 4-7952-9669-3
  - 「AppleScriptでぜんまいびゅんびゅん」, 掌田津耶乃 (1995）ISBN 4-7561-1068-1

## 関連項目

  - [Xcode](../Page/Xcode.md "wikilink")
  - [Automator](https://ja.wikipedia.org/wiki/Automator "wikilink")
  - [Apple event](../Page/Apple_event.md "wikilink")
  - [OSA](https://ja.wikipedia.org/wiki/Open_Scripting_Architecture "wikilink")

## 外部リンク

  - [Mac Automation Scripting Guide](https://developer.apple.com/library/mac/documentation/LanguagesUtilities/Conceptual/MacAutomationScriptingGuide/index.html#//apple_ref/doc/uid/TP40016239-CH56-SW1) - Appleによる初心者向けの自動化ガイド
  - [AppleScript Overview](https://developer.apple.com/library/mac/documentation/AppleScript/Conceptual/AppleScriptX/AppleScriptX.html) - 開発者向け概要
  - [AppleScript Release Notes](https://developer.apple.com/library/mac/releasenotes/AppleScript/RN-AppleScript/Introduction/Introduction.html) - 各OSバージョンのAppleScriptの変更点が書かれているリリースノート
  - [AppleScript Language Guide](https://developer.apple.com/library/mac/documentation/AppleScript/Conceptual/AppleScriptLangGuide/introduction/ASLR_intro.html) - 開発者向け言語ガイド（リファレンス含む）
  - [API Reference Apple Event Manager](https://developer.apple.com/reference/applicationservices/1651363-apple_event_manager) - AppleのAppleEvent Managerについてのリファレンス。Apple担当者の手違いでしばらくの間「Retired」扱いになっていたが、手違いであったことが2016年２月に判明し、修正された。
  - [The Open Scripting Architecture:Automating, Integrating, and Customizing Applications](http://www.cs.utexas.edu/~wcook/papers/AppleScript/AppleScript95.pdf) - AppleScriptの初期プロダクトマネージャーのWilliam R. CookとWarren H,HarrisによるAppleScriptの企画時の意図がまとめられている論文

[Category:Mac_OS](https://ja.wikipedia.org/wiki/Category:Mac_OS "wikilink") [Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink")

1.  [JavaScript for Automation Release Note](https://developer.apple.com/library/mac/releasenotes/InterapplicationCommunication/RN-JavaScriptForAutomation/Articles/Introduction.html)
2.  [林信行の「Leopard」に続く道　第5回：System 7で幕をあけた激動の1990年代（後編）](http://www.itmedia.co.jp/pcuser/articles/0710/29/news021_3.html)
3.  [AppleScript Users ML](https://lists.apple.com/mailman/listinfo/applescript-users)
4.  [AppleScript Language Guide Keywords](https://developer.apple.com/library/mac/documentation/AppleScript/Conceptual/AppleScriptLangGuide/conceptual/ASLR_lexical_conventions.html#//apple_ref/doc/uid/TP40000983-CH214-SW7)
5.  [Scripting Additions for Mac OS X](https://developer.apple.com/library/mac/technotes/tn1164/_index.html)
6.  [macOS Mojave 10.14 Release Notes](https://developer.apple.com/documentation/macos_release_notes/macos_mojave_10_14_release_notes?language=objc#overview)
7.
8.
9.
10. [“GUI Scripting”と”UI element Scripting”](http://piyocast.com/as/archives/4092)
11. [【基礎】アプリケーションの操作は、用語辞書に書いてあるとおり記述しないと動かない](http://piyocast.com/as/archives/1963)
12. [AppleScriptObjC Release Notes](https://developer.apple.com/library/mac/releasenotes/ScriptingAutomation/RN-AppleScriptObjC/)
13. [AppleScript sorting performance comparison](http://piyocast.com/as/archives/2071)
14. [Technical Note TN2065: do shell script in AppleScript](https://developer.apple.com/library/mac/technotes/tn2065/_index.html). *Mac Developer Library*. Apple, 2006-03-23.
15. [ParallelesにゲストOSとしてインストールしたOS XをAppleScriptで制御](http://piyocast.com/as/archives/2521)
16. [郵便専門ネットでバージョン番号を取得](http://piyocast.com/as/archives/1318)
17. [郵便専門ネットでXML-RPC経由でJISコード（5桁、6桁どちらでも）から、その市区町村に属している郵便番号のリストを取得](http://piyocast.com/as/archives/1320)
18. [郵便専門ネットで道府県のコード（地方公共団体コードの先頭2文字）から都道府県名を返す](http://piyocast.com/as/archives/1328)
19. [郵便専門ネットで引数に指定した郵便番号で何件ヒットするのかをint型で返す](http://piyocast.com/as/archives/1326)
20. [郵便専門ネットでXML-RPC経由で郵便番号を6桁（チェックデジット付き）の全国地方公共団体コード／JISコード／市町村コードに変換](http://piyocast.com/as/archives/1338)
21. [REST APIに対してGET、POST、PUT、DELETEのmethodを呼び出す](http://piyocast.com/as/archives/4017)
22. [AppleScriptから電話にアクセスする](http://piyocast.com/as/archives/4058)
23. [ZipZap frameworkを使ってZipアーカイブ内の情報を取得](http://piyocast.com/as/archives/1938)
24. [Contactsに登録してある自分の写真をPNGでデスクトップに保存する](http://piyocast.com/as/archives/3350)
25. [AppleScript Release Notes 10.11 Changes Folder Actions](https://developer.apple.com/library/mac/releasenotes/AppleScript/RN-AppleScript/RN-10_11/RN-10_11.html#//apple_ref/doc/uid/TP40000982-CH111-DontLinkElementID_5)
26. [プリンタ一覧の情報を取得する v2](http://piyocast.com/as/archives/3105)
27. [TTS Voice名一覧を取得](http://piyocast.com/as/archives/354)
28.
29. [Keynoteスライドの末尾にQRコードのスライドを追加](http://piyocast.com/as/archives/3307)
30. [OS X 10.11.5＋Safari 9.1.1以降で、新たなAS制限機能が増える](http://piyocast.com/as/archives/3352)
31. [tccKitで指定Bundle IDのアプリケーションの「オートメーション」認証状況を取得](http://piyocast.com/as/archives/4819)
32. [com.apple.quarantineがドロップレットに与える影響](http://piyocast.com/as/archives/4465)
33. [macOS 10.12のsayコマンドにバグ](http://piyocast.com/as/archives/4521)
34. [macOS 10.12のsayコマンドのバグはNSSpeechSynthesizerのレベルで発生](http://piyocast.com/as/archives/4569)
35. [（- LateNight SoftwareのShane StanleyによるmacOS 10.13のScripting Bridge系のバグ解説記事](http://latenightsw.com/high-sierra-applescriptobjc-bugs/)
36. [macOS 10.13でPDFViewのcurrentPageにバグ](http://piyocast.com/as/archives/4916)