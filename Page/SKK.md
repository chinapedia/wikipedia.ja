> この記事は[SKK](https://ja.wikipedia.org/wiki/SKK)から翻訳されています。


**SKK**（エスケイケイ、**Simple Kana to Kanji conversion program**）は、[Emacs](../Page/Emacs.md "wikilink")上で動く、[日本語入力システム](../Page/日本語入力システム.md "wikilink")の一つである。

## 概要

[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に、[東北大学](https://ja.wikipedia.org/wiki/東北大学 "wikilink")[教授](../Page/教授.md "wikilink")（当時）[佐藤雅彦によって開発された](https://ja.wikipedia.org/wiki/佐藤雅彦_\(コンピュータ\) "wikilink")\[1\]。本家での開発終了が[2000年](../Page/2000年.md "wikilink")11月頃に宣言され\[2\]、現在はSKK Openlabが開発を行っている。SKK OpenlabがリリースするSKKには、**Daredevil SKK**(**ddskk**)の名が付けられている。

SKKが他の日本語[インプットメソッド](../Page/インプットメソッド.md "wikilink")と大きく異なるのは、[かな漢字変換](https://ja.wikipedia.org/wiki/かな漢字変換 "wikilink")において[形態素解析](../Page/形態素解析.md "wikilink")に基づいた変換を行わないことである。[かな](../Page/かな.md "wikilink")と[漢字](../Page/漢字.md "wikilink")の境界をユーザが指定することになるため、形態素解析を行うシステムではどうしても避けられない解析ミスを回避し、意図した通りの変換を行うことができる。話し言葉や[方言](../Page/方言.md "wikilink")を記述する際、その表記のぶれのほとんどはかな文字で表記される部分であるので、SKKでは変換ミスにつながらない。 また、前者は再変換のために文節の選択を（例えば、右から左へ）変更する必要性があり、打鍵のコストが多くかかるが、SKKの場合は入力と変換を逐一行うことによって、ペンで文字を描くように自然に左から右へ文章を書いていくことが可能である。カーソルキーを多用しないということはそれだけホームポジションから手を離す機会が減るため、高速な入力も可能となる。

SKKでは、ローマ字を直接入力するとそのままひらがなに変換される。かなを漢字に変換する場合は、漢字の開始部分を大文字で指定する。[活用](../Page/活用.md "wikilink")のある場合には[送りがな](../Page/送りがな.md "wikilink")の開始部分を、活用のない場合は空白を入力することで漢字へ変換する。例えば、「彼は足が速い」という文を入力する場合、「<kbd>**K**are␣ha**A**si␣ga**H**aya**I**</kbd>」と入力する(但し左の例では空白を<kbd>␣</kbd>で表わし,一度目の変換で望む候補が出たことを仮定している)。

他の特徴として、シームレスな辞書登録が挙げられる。辞書に登録されていない単語を変換しようとした場合はミニバッファで変換結果の入力が促され、その結果は個人用の辞書に登録される。辞書の登録は再帰的に行うことができる。そのため、使っているうちに自然と辞書が成長していき、より快適な変換を実行することができるようになる。

SKKの大きな欠点のひとつは大文字を入力するためのシフトキーの多用、すなわち小指の酷使である。このため長時間の入力には向かないという意見もある。設定によりシフトキーを押しやすい別のキーにアサインしてこの小指問題を回避する方法もある。

SKKはローマ字かな変換に基づいた入力方式だが、漢字の始点と終点を指定できれば、直接かな入力に対応できる。多少のインストールと設定の追加により、[親指シフト](../Page/親指シフト.md "wikilink")配列やJISかな入力、[T-Code](https://ja.wikipedia.org/wiki/T-Code "wikilink")や[TUT-Code](https://ja.wikipedia.org/wiki/TUT-Code "wikilink")での使用が可能である。親指シフト配列では漢字変換の始点を大文字で指定するのではなく、ホームポジションの両人差し指のキーである「f」と「j」の同時打鍵を使用する。

SKKでの日本語入力は、ほかのインプットメソッドと大きく異なるため、初めてのものは戸惑いを感じさせる。[形態素解析](../Page/形態素解析.md "wikilink")を利用した変換では送りがなの開始位置を変換のたびに明示的に指定することはないからだ。しかし、手書きの際には、送り仮名の開始位置で戸惑うことなく記述できているので、慣れてくると（あるいは戸惑いの原因であるシフトキーに慣れさえすれば）手書きと同じ感覚で入力することができるとされている。

## SKKのバリエーション

SKKは[Emacs Lispで実装されているため](../Page/Emacs_Lisp.md "wikilink")、Emacsが動く環境ならばどこでも使うことができる。一方、Emacs以外で使いたい場合は、何らかの手段を講じる必要がある。様々な環境の[インプットメソッド](../Page/インプットメソッド.md "wikilink")に対応したSKKライクな変換エンジンが開発されており、それらを利用してSKK方式の入力を行うことができる。

[Unix系](../Page/Unix系.md "wikilink")環境においては、[X Window System上で動作する伝統的な](../Page/X_Window_System.md "wikilink")[X Input Method](https://ja.wikipedia.org/wiki/X_Input_Method "wikilink") (XIM) のために**skkinput**が開発された。skkinputには現在**skkinput2**と**skkinput3**のふたつの実装が存在する。

また、XIMにかわるインプットメソッドとして開発された、多言語対応のインプットメソッドの[IIIMF](https://ja.wikipedia.org/wiki/IIIMF "wikilink") (Internet/Intranet Input Method Framework)、 [uim](https://ja.wikipedia.org/wiki/uim "wikilink") (Universal Input Method)、[SCIM](../Page/SCIM.md "wikilink") (Smart Common Input Method)、[iBus](https://ja.wikipedia.org/wiki/iBus "wikilink") (Intelligent Input Bus) においてもSKKを使用することができる。

IIIMFは、XIM開発者自身によりウィンドウシステム非依存としてXIMを置き換えるべく開発されたフレームワークである。複数の言語エンジンを切り替えて使用できることを特徴としており、SKKに似た言語エンジンとして **iiimf-skk** が開発されている。

uim は、インプットメソッドサーバを用いず[ライブラリ](../Page/ライブラリ.md "wikilink")として実装された多言語インプットメソッドで、**uim-skk**というモジュールを使用することでSKK方式の入力が可能となる。コンソールや、GUIフレームワーク、インプットメソッドサーバへのブリッジが提供されている。

SCIMは、できるだけ多くのインプットメソッドに対応することを目標にしている、インプットメソッド・プラットホームである。**scim-skk** はSCIM上でDaredevil SKKと同等の機能を実装することを目標に開発されている。

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")では**AquaSKK**および**MacUIM/SKK**が利用できる。AquaSKKはその名のとおりmacOSに特化したSKKライクなインプットメソッドである。SKK辞書のほか[ことえり](../Page/ことえり.md "wikilink")のユーザ辞書を使用することができる。MacUIMはuimをmacOSで使用するためのパッケージである。

[Windows上でSKKライクな入力を実現するには](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")**skkime**や**corvus-skk**や**SKK日本語入力FEP**がある。これらはOS付属の[MSIMEを含めて全て同時にインストールでき](../Page/Microsoft_IME.md "wikilink")、言語バーおよび入力言語のホットキー操作によりアプリケーション実行中でも自由に切り替えて使用することが可能である。skkime と corvus-skk はコントロールパネルからGUIを用いて設定を行うことができる。

[Vim](../Page/Vim.md "wikilink")上でSKKライクな入力を実現するには**eskk.vim**と**skk.vim**でどちらも[Vim scriptで実装されている](https://ja.wikipedia.org/wiki/Vim_script "wikilink")。 eskk.vimはskk.vimの後継を目指して活発に開発されており、 skk.vimは2006年以降開発が停止している状況であったが、2010年にメンテナが変わって以降パッチなども精力的に取り入れている。

こうした他実装は、Daredevil SKKと独立に開発・保守されている。したがって、機能的に劣ることや、独自の拡張機能を持つこともある。

## SKKの辞書とSKKサーバ

SKKの使用する辞書は、複数のユーザによって共有する書き換えられない辞書と、ユーザの[ホームディレクトリ](../Page/ホームディレクトリ.md "wikilink")に置かれ、登録した単語や変換の履歴が追加されていく個人用の辞書がある。どちらも、かな（送りがなのある場合はかな+送りがなの最初のローマ字）と変換対象のひとつ以上の漢字とを対応させたテキストファイルである。基本語を集めた辞書は、サイズ別に、S、M、ML、Lの4つが公開されている。また、人名、地名などの固有名詞や専門用語は別のファイルとして配布されており、環境や目的に応じ複数の辞書を自由に組み合わせて使うことができる。

SKKは、辞書をバッファにとりこんで検索を行うため、最初の読み込みの際若干時間がかかることがある。また、emacs 毎に大きな辞書をとりこむのは非効率でもある。そうした欠点を補うため、共有の辞書を辞書サーバで置き換えることができる。これをSKKサーバと呼ぶ。SKKサーバへは skkserv という独自の簡易なプロトコルを用いて問い合わせを行い、入力文字列から変換結果を受け取る。SKKサーバはSKKの辞書ファイルの形式に依存しないため、様々な方式で高速化、効率化を図った実装が存在する。

SKKにはskkserv以外にも多数の辞書サーバが存在する。主なSKK辞書サーバプログラムとその特徴を下記に示す。

  - skkserv
    オリジナルのSKKサーバ。
  - skkipserv
    辞書をメモリ上にハッシングすることで検索を高速化したSKKサーバ。
  - dbskkd-cdb
    辞書形式として[cdb](https://ja.wikipedia.org/wiki/cdb "wikilink")を利用したSKKサーバ。
  - multiskkserv
    複数辞書の管理が可能なSKKサーバ。
  - rskkserv
    [Rubyで実装されたSKKサーバ](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")。EPWING形式の辞書も利用可能。
  - fskkserv
    [OCaml](../Page/OCaml.md "wikilink")で実装されたSKKサーバ。内部の索引構造に[パトリシア木](https://ja.wikipedia.org/wiki/パトリシア木 "wikilink")を用いている。
  - mecab-skkserv
    MeCabを利用して、擬似的に連文節変換を可能にするSKKサーバ。

また、[入力予測](https://ja.wikipedia.org/wiki/入力予測 "wikilink")システムである[POBox](../Page/POBox.md "wikilink")の変換サーバプロトコルは、skkservプロトコルをもとに拡張を加えたものである。 辞書サーバのフロントエンドによっては、[Google日本語入力](https://ja.wikipedia.org/wiki/Google日本語入力 "wikilink")と通信することによって、より多くのキーワードを利用できるものもある。

## 名前

[SKIコンビネータ計算](https://ja.wikipedia.org/wiki/SKIコンビネータ計算 "wikilink")において、SKKという式は[恒等関数と同じ結果となる](../Page/恒等写像.md "wikilink")。作者の佐藤自身も、SKK=Iを念頭に置いて、「ユーザの頭の中にある日本語のテキストを，なるべくストレスなしに，そのままディスプレイに出力するプログラムにしたいという気持ちが込められている」としている\[3\]。また、東北大学の教授により開発されていたわけであるが、新制東北大学の工学部の母体のひとつ[仙台高等工業学校](../Page/仙台高等工業学校.md "wikilink")の略称もSKKである。

## 脚注

## 外部リンク

  - [SKK Openlab](http://openlab.jp/skk/index-j.html)

  - [ddskk(github)](https://github.com/skk-dev/ddskk)

  - [CorvusSKK(A SKK-like Input Method Editor and some miscellaneous tools for Windows)](https://nathancorvussolis.github.io/)

  - [SKK日本語入力FEP](http://coexe.web.fc2.com/programs.html#skkfep)

  - [AquaSKK プロジェクト - 日本語を快適に](http://aquaskk.sourceforge.jp/)

  - [skkinput2's page](http://skkinput2.sourceforge.jp/)

  - [skkinput3](http://sourceforge.jp/projects/skkinput3)

  - [iiimf-skk](http://sourceforge.jp/projects/iiimf-skk/)

  - [uim](https://code.google.com/p/uim/)

  -
  - [tyru/eskk.vim - GitHub](https://github.com/tyru/eskk.vim)

  - [skk.vim - Japanese SKK : vim online](http://www.vim.org/scripts/script.php?script_id=1589)

  - [skk.vim - Japanese SKK（改良版） : vim online](http://www.vim.org/scripts/script.php?script_id=3118)

  - [jj1bdx/dbskkd-cdb - GitHub](https://github.com/jj1bdx/dbskkd-cdb/)

[Category:日本語入力ソフト](https://ja.wikipedia.org/wiki/Category:日本語入力ソフト "wikilink") [Category:1987年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1987年のソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.  [SKK = I](http://openlab.ring.gr.jp/skk/SKK.html) SKK Openlab（佐藤雅彦）、2002年（2015年6月21日閲覧）。