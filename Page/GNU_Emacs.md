> この記事は[GNU Emacs](https://ja.wikipedia.org/wiki/GNU_Emacs)から翻訳されています。


**GNU Emacs**（グヌー・イーマックス）は最も有名で、かつ最も多く移植されている[Emacs](../Page/Emacs.md "wikilink")[テキストエディタ](../Page/テキストエディタ.md "wikilink")であり、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")創設者の[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")により作成された。GNU Emacsは他のEmacs系エディタと同様に、[チューリング完全](../Page/チューリング完全.md "wikilink")な[プログラミング言語](../Page/プログラミング言語.md "wikilink")で拡張可能である。GNU Emacsは「今日利用できる最もパワフルなテキストエディタ」と称されている\[1\]。GNU Emacsは基盤となるシステムからの適切なサポートにより、複数の[文字集合](../Page/文字集合.md "wikilink")を含む[ファイルを表示することが可能だが](../Page/ファイル_\(コンピュータ\).md "wikilink")、1999年の時点で既にほとんどの人間言語を同時に表示することが可能であった\[2\]。GNU Emacsはその歴史を通じて[GNU](../Page/GNU.md "wikilink")プロジェクトの中心となるコンポーネントであり、さらに[フリーソフトウェア運動](../Page/フリーソフトウェア運動.md "wikilink")の[フラグシップ](https://ja.wikipedia.org/wiki/フラグシップ "wikilink")である\[3\]\[4\]。GNU Emacsは、他のEMACS派生と区別する場合に**GNUMACS**と略されることがある\[5\]。GNU Emacsのうたい文句は「拡張可能で自己説明的なテキストエディタ」である\[6\]。

## 歴史

[Richard_Stallman_-_Fête_de_l'Humanité_2014_-_010.jpg](https://ja.wikipedia.org/wiki/File:Richard_Stallman_-_Fête_de_l'Humanité_2014_-_010.jpg "fig:Richard_Stallman_-_Fête_de_l'Humanité_2014_-_010.jpg")の創設者であり、GNU Emacsの作者である[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")\]\]

リチャード・ストールマンは1976年に初代のEmacs ("Editor MACroS") を書き、1984年に[プロプライエタリである](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[Gosling Emacsの](../Page/Gosling_Emacs.md "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")による代替物を作成するため、GNU Emacsの作業を開始した。GNU Emacsは当初Gosling Emacsをベースとしていたが、ストールマンがGosling EmacsのMocklisp[インタプリタ](../Page/インタプリタ.md "wikilink")を本物の[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")インタプリタへと置き換えようとしたところ、Gosling Emacsのコードの大半を書き換える必要があった。GNU Emacsは創生期のGNUプロジェクトがリリースした最初の[プログラムとなった](../Page/プログラム_\(コンピュータ\).md "wikilink")。GNU Emacsは[C言語](../Page/C言語.md "wikilink")で書かれており、拡張用言語として[Emacs Lisp](../Page/Emacs_Lisp.md "wikilink") (ELisp) を提供する。Emacs LispもまたC言語で実装されている。最初の公式リリースであるバージョン13は1985年3月20日に発表された。最初に広く頒布されたGNU Emacsのバージョンは1985年に登場した15.34であった。GNU Emacsのバージョン番号は"1.x.x"のように、最初の桁がC coreのバージョンを表すよう採番されていたが、バージョン1.12が出された後でもC coreのメジャー番号が変わりそうにないため、先頭の1をなくすことにした。このため、バージョン番号は1から13にスキップした。そしてユーザーサイトによる変更を表すため、3番目のバージョン番号が新規に追加された\[7\]。現在の採番スキームでは、2番目の数はリリースバージョンを表し、3つ目の数は開発バージョンを表している\[8\]。

GNU Emacsは後に[UNIX](../Page/UNIX.md "wikilink")へと移植され、Gosling Emacsよりも多くの機能を提供した。その中でも特に代表的な機能は、GNU Emacsの拡張言語としてフル機能搭載LISPである。それから瞬く間にGNU EmacsはGosling Emacsに取って代わり、UNIX Emacsエディタのデファクトスタンダードとなった。は彼の1986 cracking spreeで、GNU Emacs電子メールサブシステムのセキュリティ上の弱点を悪用し、UNIXコンピュータ上でスーパーユーザーアクセス権を取得した\[9\]。

1999年まで、ユーザーがパッチやElispコードをnet.emacs[ニュースグループ](../Page/ニュースグループ.md "wikilink")に提出することが多かったが、現在と比べGNU Emacs開発への参加は制限されており、『[伽藍とバザール](../Page/伽藍とバザール.md "wikilink")』において「伽藍」開発スタイルの例として挙げられた。それ以降、GNU Emacsプロジェクトは公開された開発メーリングリストと、匿名[CVSアクセスを採用した](../Page/Concurrent_Versions_System.md "wikilink")。開発は2008年まで単一のCVSトランクで行われていたが、現在では[分散型バージョン管理システムである](../Page/バージョン管理システム.md "wikilink")[git](https://ja.wikipedia.org/wiki/git "wikilink")が使われている\[10\]。

リチャード・ストールマンはGNU Emacsの主要なメンテナのままだったが、時代が進むにつれ役割から後退していった。2008年以降はStefan MonnierとChong Yidongがメンテナンスを監督するようになった\[11\]。2015年9月21日にMonnierはEmacs 25の機能凍結をもって事実上のメンテナのまま辞任することをアナウンスした\[12\]。2015年11月5日、長期に渡り貢献してきたJohn Wiegleyが新しいメンテナとなることがアナウンスされた\[13\]。

## ライセンス

CとEmacs Lispから成るGNU Emacsの[ソースコード](../Page/ソースコード.md "wikilink")は、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) 規約の下で調査、修正、再頒布のため自由に入手できる。

古い版のGNU Emacsのドキュメントは、修正版の複製にあるテキストの挿入を必要とする個別のライセンスの下でリリースされた。例えば、GNU Emacs user's manualにはGNU Emacsの入手方法と、リチャード・ストールマンの政治的エッセー「GNU宣言」が含まれていた。フォーク時に古いGNU Emacsのマニュアルを継承した[XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink")のマニュアルも同じライセンスである。 一方、新しい版のGNU Emacsのドキュメントは、GNU Free Documentation Licenseを用い「不変部分」を利用して、同じドキュメントの包含を要求しつつ、マニュアルが*GNU Manuals*であることも宣言している。

GNU Emacs（や他のGNUパッケージ一般）では[コピーレフト](../Page/コピーレフト.md "wikilink")の強制を容易にするため、すなわちFSFが係争に入ったときに法廷でソフトウェアを守れるようにするため、著しい量のコード寄贈は著作権者が自身の[著作権](../Page/著作権.md "wikilink")を適切に放棄またはフリーソフトウェア財団に委譲したときだけ受理する方針になっている。 この方針の唯一の例外はMule（MULtilingual Extension、Unicodeや、他の言語の用字系を処理する高度なメソッドがある）のコードで、著作権者が日本国政府で著作権の委譲が不可能であった\[14\] 。 些細なコード寄贈やバグ修正には、この方針は適用されない。 些細かどうかの厳密な定義はないが、指針として10行未満のコードは些細とみなされている。

2011年、GPLにより意図された精神に反して、該当するソースコードが存在しないバイナリを2年間に渡りリリースしていたことが発覚した\[15\]\[16\]\[17\]。ストールマンは*「大変重大な誤り」*としてこの事件について述べ\[18\]、この誤りはすぐに修正された。当然のことだが、下流の再頒布者が技術的にGPL違反をしたのは彼ら自身の過ちではないため、FSFは誰も訴えなかった。

## 使用法

[Emacs_Dired_buffers.png](https://ja.wikipedia.org/wiki/File:Emacs_Dired_buffers.png "fig:Emacs_Dired_buffers.png")バッファの編集\]\] [Colorsyntax.png](https://ja.wikipedia.org/wiki/File:Colorsyntax.png "fig:Colorsyntax.png")[ソースコード](../Page/ソースコード.md "wikilink")の編集\]\] [Cpp_in_GNU_emacs.png](https://ja.wikipedia.org/wiki/File:Cpp_in_GNU_emacs.png "fig:Cpp_in_GNU_emacs.png")コードの編集と[コンパイル](../Page/コンパイラ.md "wikilink")\]\]

### 基本的な操作

基本的な操作は、GNU Emacsからのフォークとして始まったXEmacsとその後継版は、GNU Emacsとおおむね互換性がある。

カーソル移動などは矢印キーをつかって行うこともできるが、主要な大部分の操作は、[コントロールキー](../Page/コントロールキー.md "wikilink")・[メタキー](../Page/メタキー.md "wikilink")（Windowsでは通常[Altキー](https://ja.wikipedia.org/wiki/Altキー "wikilink")を使用する）・[スーパーキーなどを押し下げたまま別のキーを打鍵することで行うことができる](https://ja.wikipedia.org/wiki/スーパーキー_\(キーボード\) "wikilink")。[vi](https://ja.wikipedia.org/wiki/vi "wikilink")と比較した場合、viが編集モード、カーソル移動モードの2つのモードを持つのに対し、Emacsはそのようなモードを持たない。ただしEmacs上でviの操作をエミュレートするエミュレータもいくつかある (vip-mode, viper-mode) 。

なお、Emacsではコントロールキーを押しながら「a」を押す事を「C-a」と表記し、メタキーを押しながら「a」を押す事を「M-a」と表記する。本稿でも以下この表記を用いる。 キーの多くは英語の頭文字にしたがって割り振られているので、どのキーがどの操作に対応しているのかを比較的簡単に覚えることができる。たとえばカーソルを右、左、上、下に動かす操作はそれぞれC-f、C-b、C-p、C-nであるが、これはそれぞれforward、backward、previous、nextの略である。

Emacsでは、2ストローク以上のキー操作も多数用意している。たとえば「C-xC-s」(＝コントロールキーを押し下げたままx、sと打鍵する)でファイルを保存する。キーの割り当てられていないコマンドも多くあり、それらは M-x を押してからコマンドを入力することで実行する。

なお、C-h t（英語）あるいはC-h T（翻訳）でチュートリアルを表示させることができ、そのまま操作方法を学習することができる。

[GUIでEmacsを使っているとき](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、キーボードの代わりにメニューバーやツールバーからもコマンドを呼び出せる。しかし、経験豊富なEmacsの利用者には、必要なキー操作をいったん記憶してしまえばより速く操作でき便利なキーボードからのコマンド呼び出しのほうが好まれている。

全ての編集コマンドは、実際はEmacs Lisp環境の関数を呼び出す。文字*a*を挿入するコマンドの`a`をたたいただけでも、関数を（この場合`self-insert-command`を）呼び出す。一部のEmacsコマンドは、外部プログラム（つづりのチェックに[ispell](https://ja.wikipedia.org/wiki/ispell "wikilink")や、プログラムのコンパイルに[gcc](../Page/GNUコンパイラコレクション.md "wikilink")）を呼び出し、プログラムの出力を解析し、Emacsに結果を表示することで、機能している。

### コマンド

GNU Emacsは、通常の編集モードにおいては他のテキストエディタと同じように振る舞うため、ユーザーは対応する[キーで文字を挿入でき](../Page/キーボード_\(コンピュータ\).md "wikilink")、さらに矢印キーで編集場所を移動できる。[エスケープキーシーケンスを入力するか](https://ja.wikipedia.org/wiki/Escキー "wikilink")、またはコントロールキー、メタキー、Altキー、スーパーキーのうち1つ以上のキーを通常キーと同時に押すことにより、[修飾キー](../Page/修飾キー.md "wikilink")ストロークを発生させてEmacs Lisp環境から関数を呼び出す。`save-buffer`や`save-buffers-kill-emacs`などのコマンドでは、複数の修飾キーストロークを組み合わせる。

GNU Emacsのコマンドの中には、[スペルチェック用の](../Page/スペルチェッカ.md "wikilink")[Ispell](https://ja.wikipedia.org/wiki/Ispell "wikilink")やプログラム[コンパイル用の](../Page/コンパイラ.md "wikilink")[gccなどのように外部プログラムを呼び出して処理を行うものも存在する](../Page/GNUコンパイラコレクション.md "wikilink")。GNU Emacsはこれら外部プログラムの出力を[パースして](../Page/構文解析.md "wikilink")、GNU Emacsに結果を出力する。Emacsは「下位プロセス」もサポートする。下位プロセスとは、Emacsバッファと相互に影響しあう長寿命な[プロセス](../Page/プロセス.md "wikilink")であり、<span style="font-family: monospace, monospace;">shell-mode</span>の実装に使われる。このモードでは各種プログラミング言語用の[Read–eval–print loopモードや](https://ja.wikipedia.org/wiki/REPL "wikilink")[Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")を、下位プロセスで起動する。GNU Emacsは外部プロセスをサポートしているため、[Interlisp](../Page/Interlisp.md "wikilink")や[SmallTalk](https://ja.wikipedia.org/wiki/SmallTalk "wikilink")の行に沿った対話型プログラミング用環境としてGNU Emacsは魅力的なものである\[19\]。

[IBM](../Page/IBM.md "wikilink") [Common User Accessスタイルのキーを好むユーザーは](../Page/Common_User_Access.md "wikilink")<span style="font-family: monospace, monospace;">cua-mode</span>を使うことができる。このモードは元々[サードパーティー](../Page/サードパーティー.md "wikilink")の[アドオンであったが](https://ja.wikipedia.org/wiki/機能拡張 "wikilink")、バージョン22以降のGNU Emacsに含まれるようになったパッケージである。

### ミニバッファ

Emacsは状態を表したり情報を要求するために「ミニバッファ」を利用する。通常、ミニバッファは一番下の行に存在する。ミニバッファが果たす機能は、ほとんどのGUIでは一般的に[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")が果たす機能である。ミニバッファは、検索対象となるテキストや、読み込みや保存を行うファイル名などの情報を保持している。該当する場合、[タブキー](../Page/タブキー.md "wikilink")や[スペースキー](https://ja.wikipedia.org/wiki/スペースキー "wikilink")でができる。

### ファイル管理と表示

Emacsは[バッファ](../Page/バッファ.md "wikilink")と呼ばれる[データ構造](../Page/データ構造.md "wikilink")でテキストを保持する。バッファは画面に表示することも非表示にすることもでき、さらにEmacs Lispプログラムや[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")から全てのバッファ機能にアクセスできる\[20\]。ユーザーは新しいバッファを作成したり不要なバッファを消去することができ、複数のバッファを同時に存在させることもできる。Emacsが使えるバッファ数はハードウェアメモリが許す限り増やすことができる。上級ユーザーは自身の作業と関係のある様々なタイプの開かれたバッファを数百個蓄えることもある\[21\]。

バッファの中には[テキストファイル](../Page/テキストファイル.md "wikilink")から読み込まれたテキストバッファなどのように、ユーザーが編集したり永続ストレージに保存することができるものもある。このようなバッファを、ファイルを「訪問している」バッファと呼ぶ。バッファはこれ以外にも、Emacsコマンドの出力、[Dired](../Page/Dired.md "wikilink")[ディレクトリ](../Page/ディレクトリ.md "wikilink")一覧表示、「ヘルプ」ライブラリが表示するドキュメントの文字列、およびEmacs以外のエディタではダイアログボックスに表示される通知メッセージなどのデータを表示する役割も果たす。GNU Emacsはこれらの通知をミニバッファへ簡潔に表示し、さらにそれら通知の最新履歴を保持するために<span style="font-family: monospace, monospace;">\*Messages\*</span>バッファを提供する。バッファは[シェル](../Page/シェル.md "wikilink")やREPLなどの外部プロセスに対する入出力エリアとしての役割も果たす。ユーザーバッファと区別するため、Emacsが独自に作成するバッファ名には最初と最後に[アスタリスク](../Page/アスタリスク.md "wikilink")が付くことが多い。開かれているバッファの一覧は、それ自体がこのタイプのバッファに表示される。

Emacsキーシーケンスのほとんどは、どのバッファでも機能する。例えば、標準Ctrl-s `isearch`機能はDiredバッファでファイル検索のために使うことができ、さらにそのファイル一覧を他の全てのバッファと同様にテキストファイルへと保存することもできる。Diredバッファを書き込み可能モードに切り替えると、ファイル名や属性をテキストベースで編集することができ、さらにその場合にDiredバッファを保存すると変更した箇所がファイルシステムに書き込まれる。これにより、Emacsの検索および置換機能を利用して複数のファイルを改名することができる。さらに装備すると、GNU Emacsはバッファに画像ファイルを表示する。GNU Emacsはバイナリセーフで8ビットクリーンである\[22\]。

Emacsは編集領域を「ウィンドウ」と呼ばれるエリアに分割できる。EmacsではGUIが普及するよりも前の1975年から、既にウィンドウ機能を使えるようになっていた。Emacs用語における「ウィンドウ」とは、他のシステムでは「」や「[ペイン](https://ja.wikipedia.org/wiki/ペインド・ウィンドウ "wikilink")」と呼ばれるものと類似している。ウィンドウは独自に更新や対話ができる、プログラムによる表示の矩形部分である。Emacsでは各ウィンドウにそれぞれ「モードライン」と呼ばれるステータスバーが存在し、デフォルトではウィンドウの最下端に表示される。Emacsウィンドウはテキスト端末でもグラフィカルモードでも使うことができ、さらにウィンドウにより複数のバッファや、1つのバッファにおける複数の部分を同時に見ることが可能となる。一般的なウィンドウの応用例としては、[カレントディレクトリ](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")のファイル一覧に加えて[Dired](../Page/Dired.md "wikilink")バッファを表示したり（ファイルバッファをDiredでハイライトされたファイルに従わせる特殊なモードが存在する）、あるウィンドウでプログラムの[ソースコード](../Page/ソースコード.md "wikilink")を表示しながら別のウィンドウにプログラムをコンパイルした結果の[シェル](../Page/シェル.md "wikilink")バッファを表示してプログラムを起動しているシェルバッファと一緒にデバッガを起動したり、[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")や（Emacsのビルトインウェブブラウザの一種を使って[World Wide Web全体からロードされたものなどの](../Page/World_Wide_Web.md "wikilink")）他のドキュメントを表示しながらコードを処理したり、Cベースの言語用[ヘッダとその実装ファイルなどを同時に編集するため複数のファイルを表示したりなどができる](../Page/ヘッダファイル.md "wikilink")。加えて、バッファの重複しない部分を表示するようウィンドウを連鎖させる<span style="font-family: monospace, monospace;">follow-mode</span>が存在する。<span style="font-family: monospace, monospace;">follow-mode</span>を使うと、1つのファイルを[スクロール](../Page/スクロール.md "wikilink")時に適切に更新される複数の並列ウィンドウに表示する。Emacsウィンドウは[タイル型であるため](https://ja.wikipedia.org/wiki/タイル型ウィンドウマネージャ "wikilink")、ウィンドウが「前面」や「背面」になることはない。Emacsは複数の「フレーム」を起動することができる。フレームはグラフィカル環境で個々の[ウィンドウ](../Page/ウィンドウ.md "wikilink")を表示するためのものである。テキスト端末上で複数のフレームを作ることができる。テキスト端末において、複数フレームは端末全体を満たすよう積み重ねられて表示され、標準Emacsコマンドを使うことでフレームを切り替えることが可能である\[23\]。

### 主モード

GNU Emacsは様々な異なるタイプのテキストを編集でき、「主モード（メジャーモード、major-mode）」と呼ばれる[アドオンモードに入ることで](../Page/プラグイン.md "wikilink")、編集するテキストの種類に応じて振舞いを適用させる。普通のテキストファイル、多くのプログラミング言語のソースコード、[HTMLドキュメント](../Page/HyperText_Markup_Language.md "wikilink")、[TeX](../Page/TeX.md "wikilink")や[LaTeX](../Page/LaTeX.md "wikilink")ドキュメントや、多くの他種の[ファイルタイプ用に主モードが定義されている](../Page/ファイルフォーマット.md "wikilink")。各主モードはEmacs Lisp変数を調節するなどして固有の型のテキストに都合よく振る舞うように作られている。 主モードは通常、以下のような共通機能の一部または全てを提供する:

  - シンタックス強調表示（「フォントロック」）:「フェイス」と呼ばれる、[キーワードや](../Page/予約語.md "wikilink")[コメントといったドキュメント要素の差異を示す](../Page/コメント_\(コンピュータ\).md "wikilink")、フォントと色の組み合わせ<ref>

</ref>

  - ファイル内で一貫した書式設定を維持するための自動インデント
  - 空白、新しい行、および括弧のようなドキュメントの構造に必要な要素の自動挿入
  - プログラミングファイルの編集中に関数の先頭や末尾へ飛ぶコマンドや、[XMLのような](../Page/Extensible_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")の作業中にドキュメントを検証したり終了タグを挿入するコマンドのような特殊編集コマンド

### 副モード

「副モード（マイナーモード、minor-mode）」でGNU Emacsの振る舞いをさらにカスタム化することもできる。バッファを編集するGNU Emacsは1つの主モードしか使えないが、副モードは複数同時に操作できる。C言語用の主モードへ人気のある[字下げスタイル](../Page/字下げスタイル.md "wikilink")毎に個別の副モードを定義するなどのような方法により、副モードをドキュメント上で直接操作したり、副モードで編集環境を変更することができる。後者の例としてはウィンドウ構成の変更をアンドゥする能力を追加するモードや、オンザフライなシンタックスチェックを実行するモードなどが挙げられる。複数のプログラミング言語が埋め込まれたドキュメントを編集する際に便利なため、複数の主モードを単一のファイルで使えるようにする副モードもある。

### 「バッチモード」

GNU Emacsは、テキストエディタユーザインタフェースを表示しないElisp言語用インタープリタとしての使用もサポートしている。バッチモードではユーザー設定はロードされず、端末[割り込み文字のC](../Page/割り込み_\(コンピュータ\).md "wikilink")-cとC-zは、Emacsのキーバインディングを呼び出す効果ではなく、プログラム終了や実行中断をする通常の効果をもたらす。GNU Emacsは、ロードおよび実行するためのファイルや、コマンドラインから渡せるEmacs Lisp関数を指定するための[コマンドラインオプションを持つ](../Page/キャラクタユーザインタフェース.md "wikilink")。Emacsが開始されると渡されたファイルや関数を実行し、結果を出力してから終了する\[24\]。`#!/usr/bin/emacs --script`という[シバンの行でEmacs](../Page/シバン_\(Unix\).md "wikilink") Lispのスタンドアロンスクリプトを作成できる\[25\]。バッチモードはEmacsのモード「そのもの」ではないが、Emacsプログラムの代替実行モードとして説明される。

## マニュアル

ビルトインドキュメントとは別に、GNU Emacsには異常に長くて詳細な[マニュアル](../Page/マニュアル.md "wikilink")がある。リチャード・ストールマンによって書かれた*GNU Emacs Manual*の電子コピーはGNU Emacsにバンドルされ、ビルトインブラウザで閲覧できる。Bil Lewis、リチャード・ストールマンそしてDan Laliberteによる*Emacs Lisp Reference Manual*とによる*An Introduction to Programming in Emacs Lisp*の2つの追加マニュアルも含まれる。これらのマニュアルは全てフリーソフトウェア財団により書籍形式でも発行されている。XEmacsのマニュアルは*GNU Emacs Manual*と類似しているが、XEmacsのソフトウェアはGNU Emacsからフォークされたと同時にマニュアルもフォークされたからである。

## 国際化

GNU Emacsは多種のアルファベット、[文字体系](https://ja.wikipedia.org/wiki/文字#文字体系と表記体系 "wikilink")、[表記体系および文化的慣習をサポートしており](https://ja.wikipedia.org/wiki/文字#文字体系と表記体系 "wikilink")、[Ispell](https://ja.wikipedia.org/wiki/Ispell "wikilink")のような外部プログラムを呼ぶことで多数の言語の[スペルチェックを提供している](../Page/スペルチェッカ.md "wikilink")。バージョン24にはアラビア語、ペルシア語、そしてヘブライ語といった言語のため、[横書きにおいて左横書きと右横書きとを混在して書く機能のサポートが追加された](../Page/縦書きと横書き.md "wikilink")。

[UTF-8](../Page/UTF-8.md "wikilink")を含む多数の[文字コード](../Page/文字コード.md "wikilink")をサポートしている。GNU Emacsはバージョン23から文字コードにUTF-8を使うが、それ以前のバージョンでは固有の内部文字コードを使い、読み書き時に変換していた。XEmacsが使う内部文字コードは以前のバージョンのGNU Emacsのものと類似しているが、詳細は異なる。

GNU Emacsユーザインタフェースはビギナーのチュートリアルを除き英語で開始され、それ以外の言語には翻訳されていない。

**と呼ばれるサブシステムにより、視覚障害のあるユーザーや盲目のユーザーがオーディオフィードバックを通じてエディタをコントロールできる。

### 日本語化

GNU Emacsの[日本語](../Page/日本語.md "wikilink")版としてNemacs (Nihongo Emacs) が、多国語対応版として[Mule](../Page/Mule.md "wikilink") (MULtilingual Enhancement to GNU Emacs) が開発された。NemacsおよびMuleは電子技術総合研究所（電総研:現在の[産業技術総合研究所](../Page/産業技術総合研究所.md "wikilink")）の[半田剣一](../Page/半田剣一.md "wikilink")らによるものである。

#### Mule

Muleは[アラビア文字](../Page/アラビア文字.md "wikilink")などの右から左へ記述する文字をふくめた複数の文字集合の1ファイル中での混在と編集が可能であり、中国や、タイ等多くの国や地域で規格化された文字集合をサポートするなど、先進的かつ実用的な多用字系処理系であった（しばしば[多言語](../Page/多言語.md "wikilink")処理系ともいわれる）。

#### 日本語 GNU Emacs

日本語 GNU Emacs (Nemacs:Nihongo Emacs) は[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")の[平野聡と](../Page/平野聡_\(計算機科学者\).md "wikilink")[大阪大学](https://ja.wikipedia.org/wiki/大阪大学 "wikilink")の[東田学](https://ja.wikipedia.org/wiki/東田学 "wikilink")によって、フリーな[DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")のgo32/djgppを用いて[MS-DOS](../Page/MS-DOS.md "wikilink")上に移植され（後にemxにも対応）、demacsと呼ばれた。

## 拡張性

[Emacs+AucTeX.png](https://ja.wikipedia.org/wiki/File:Emacs+AucTeX.png "fig:Emacs+AucTeX.png")を利用しているGNU Emacs。AUCTeXは[TeX](../Page/TeX.md "wikilink")や[LaTeX](../Page/LaTeX.md "wikilink")ドキュメントを編集するツールのセットである。\]\] GNU Emacsの振る舞いは、新しいコマンド、新しいバッファモード、新しいキーマップなどを定義したり、コマンドラインオプション\[26\]を追加するための組み込みEmacs Lispプログラムにより、ほぼ制限なく修正したり拡張することができる。ユーザー向け機能を提供する拡張の多くは主モードを定義する（新しいファイルタイプ用の主モードか、テキスト編集させないユーザインタフェースを構築する主モードのどちらかとなる）。その他の拡張には、コマンドや副モードのみを定義するものや、別の拡張を補強する機能を提供するものなどがある。

GNU Emacsのインストールには多くの拡張がバンドルされている。バンドルされていない拡張はルーズファイル（[Usenet](../Page/ネットニュース.md "wikilink") [newsgroup](../Page/ニュースグループ.md "wikilink") gnu.emacs.sourcesが伝統的なソースであった）として、ダウンロードされ使用されていたが、バージョン24より管理されたパッケージやパッケージダウンロードサイトが発展してきている。これらのパッケージは、拡張をダウンロードしてインストールし、さらに最新の状態に維持するためのビルトインパッケージマネージャ（これ自体が拡張である）を利用する。

以下に主な拡張の例を示す:

  - : [TeX](../Page/TeX.md "wikilink")および[LaTeX](../Page/LaTeX.md "wikilink")ドキュメントを編集し処理するためのツール

  - Calc : パワフルな[RPN数値](../Page/逆ポーランド記法.md "wikilink")[計算機](../Page/計算機.md "wikilink")

  - Calendar-mode : 予定表や日記の維持

  - [Dired](../Page/Dired.md "wikilink") : ファイルマネージャ

  - [Dissociated press](https://ja.wikipedia.org/wiki/四散新聞 "wikilink") : テキストジェネレータ風の

  - Doctor : [ELIZA](../Page/ELIZA.md "wikilink")にインスパイアされた[精神分析シミュレーション](../Page/精神分析学.md "wikilink")

  - [Dunnet](https://ja.wikipedia.org/wiki/Dunnet "wikilink") : [テキストアドベンチャー](https://ja.wikipedia.org/wiki/インタラクティブフィクション "wikilink")

  - Ediff / Emerge : インタラクティブにファイルの比較と統合を行うためのもの

  - : 主にWilliam M. PerryによってEmacs Lispで書かれた[テキストブラウザ](https://ja.wikipedia.org/wiki/テキストブラウザ "wikilink")。Emacs/W3はXEmacs用のSumoパッケージの一部であり、[URLを取得するためのサブモジュールは現在GNU](../Page/Uniform_Resource_Locator.md "wikilink") Emacs [CVSリポジトリの一部である](../Page/Concurrent_Versions_System.md "wikilink")。HTML+と呼ばれた[HTML](../Page/HyperText_Markup_Language.md "wikilink") 2の後継に取り組んでいる間、Emacs/W3とはをサポートしていた\[27\]

  - (ESS) : RやSASなど統計言語の編集モード

  - (EWW) : 組み込みウェブブラウザ

  - /  / Circe : [IRCクライアント](../Page/Internet_Relay_Chat.md "wikilink")\[28\]

  - [Eshell](https://ja.wikipedia.org/wiki/Eshell "wikilink") : Emacs Lispで書かれたコマンドラインシェル。[Bash](../Page/Bash.md "wikilink")や[PowerShell](../Page/PowerShell.md "wikilink")などの標準的なシェルはEmacsからも利用できるが、Eshellはそれら標準的なシェルよりもさらに緊密なEmacs環境との統合を可能にする

  - Exwm : [X11アプリをEmacsウィンドウで起動できる](../Page/X_Window_System.md "wikilink")[Xウィンドウマネージャ](https://ja.wikipedia.org/wiki/Xウィンドウマネージャ "wikilink")\[29\]

  - [Gnus](../Page/Gnus.md "wikilink") : フル装備の兼[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")で、[Zawinskiの法則に対する初期の証拠](https://ja.wikipedia.org/wiki/:en:Jamie_Zawinski "wikilink")

  - [howm](https://ja.wikipedia.org/wiki/howm "wikilink") : メモ取り環境兼ToDo管理

  - JDE: [Java](https://ja.wikipedia.org/wiki/Java "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink")

  - Magit : バージョン制御システムである[git](https://ja.wikipedia.org/wiki/git "wikilink")と連携を可能にする\[30\]\[31\]

  - [Mediawiki-mode](https://ja.wikipedia.org/wiki/Meta:Mediawiki.el "wikilink") : [MediaWiki](../Page/MediaWiki.md "wikilink")プロジェクトのページ編集モード

  - [Mew](../Page/Mew.md "wikilink"), [mh-e](https://ja.wikipedia.org/wiki/mh-e "wikilink"), [Wanderlust](https://ja.wikipedia.org/wiki/Wanderlust "wikilink"): [電子メールクライアント](../Page/電子メールクライアント.md "wikilink")

  - MULtilingual Enhancement to Emacs ([MULE](../Page/Mule.md "wikilink")) : Unicodeにやや類似した方法で多言語のテキストを編集できる拡張

  - : 要約を維持しながら、様々なタイプのリストを整理し、プロジェクトを見積もり、そして（[PDF](../Page/Portable_Document_Format.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[OpenDocument](../Page/OpenDocument.md "wikilink")などの）多数のフォーマットのドキュメントを組み合わせる。Org-modeを使う静的サイトジェネレータだけではなく、[文芸的プログラミング](../Page/文芸的プログラミング.md "wikilink")のために利用できるBabelが存在する\[32\]

  - : Emacsを使った[Personal Information Manager](../Page/Personal_Information_Manager.md "wikilink")

  - Pong : [ポン](../Page/ポン_\(ゲーム\).md "wikilink")

  - Simple Emacs Spreadsheet (SES) : [スプレッドシート](../Page/表計算ソフト.md "wikilink")

  - [SKK](../Page/SKK.md "wikilink") : [かな漢字変換](https://ja.wikipedia.org/wiki/かな漢字変換 "wikilink")

  - SQL Interaction Mode : [SQL](../Page/SQL.md "wikilink")データベースサーバの様々な流儀でやり取りするためのモード

  - \[33\] (SLIME) : [Common Lisp用開発環境にGNU](../Page/Common_Lisp.md "wikilink") Emacsを拡張する。（Emacs Lispで書かれた）SLIMEによりGNU Emacsエディタは特殊な通信プロトコルを通じて（SWANKバックエンドを利用している）Common Lispシステムと通信し、さらにRead–eval–print loop、データ検査器、および[デバッガ](../Page/デバッガ.md "wikilink")などのツールを提供する

  - Tetris : [テトリス](../Page/テトリス.md "wikilink")

  - [Texinfo](../Page/Texinfo.md "wikilink") (Info) : オンラインヘルプブラウザ

  - Twittering-mode: [ツイッターのクライアント](../Page/Twitter.md "wikilink")

  - VC : [バージョン管理システム](../Page/バージョン管理システム.md "wikilink")

  - View Mail (VM) : フル装備の電子メールクライアント

  - Viper : viエミュレーション層\[34\]。Vimエミュレーション層であるEvilも存在する\[35\]

  - W3M : ウェブブラウザで、[w3m](https://ja.wikipedia.org/wiki/w3m "wikilink")スタンドアローンブラウザをベースとして利用する

  - Wanderlust : 多目的用途の電子メール/ニュースクライアント

  - [wikipedia-mode](https://ja.wikipedia.org/wiki/Wikipedia:Wikipedia-mode.el "wikilink") : Wikipediaの記事を編集する

  - Zone : 様々ななテキスト効果を組み込むためのモード

## パフォーマンス

GNU EmacsはLispベースのコードをロードし[解釈することによるパフォーマンスのオーバーヘッドが発生するため](../Page/インタプリタ.md "wikilink")、初期の実装時点では競合するテキストエディタよりもシステム上における実行が著しく遅かった。現在のコンピュータはスローダウンせずにGNU Emacsを起動するほどパワフルであるが、19.29以前のバージョンでは8MB以上のファイルを編集できなかった。このファイルサイズ制限はバージョンを通じて存在したが、GNU Emacs 23.2以降の[32ビット](../Page/32ビット.md "wikilink")バージョンでは512MBまでのサイズのファイルを編集できる。[64ビット](../Page/64ビット.md "wikilink")マシンでコンパイルされたEmacsではさらに大きいバッファを処理できる\[36\]。

## プラットフォーム

GNU Emacsは最も[移植された非商用コンピュータプログラムの](../Page/移植_\(ソフトウェア\).md "wikilink")1つであり、[DOS](https://ja.wikipedia.org/wiki/DOS "wikilink")、[Microsoft Windowsそして](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[OpenVMS](../Page/OpenVMS.md "wikilink")を含む様々な[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上で動作する\[37\]\[38\]\[39\]。Emacs 23.1でサポートが削除された時代遅れのプラットフォームの中には、VMSや（Linuxベースのもを除く）大半のUnix派生など、既に開発が終了していたものもある\[40\]。GNU Emacsは[Linux](../Page/Linux.md "wikilink")、[BSD](../Page/BSD.md "wikilink")派生、[Solaris](../Page/Solaris.md "wikilink")、[AIX](../Page/AIX.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")および[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")などのほとんどの[Unix系](../Page/Unix系.md "wikilink")オペレーティングシステムで利用可能であり\[41\]\[42\]、システムインストールパッケージに含まれていることが多い。[Android](../Page/Android.md "wikilink")\[43\]やノキアの[Maemo](https://ja.wikipedia.org/wiki/Maemo "wikilink")用\[44\]のGNU Emacsネイティブ移植が存在する。

GNU Emacsは[テキスト端末とGUI環境の両方で動作する](https://ja.wikipedia.org/wiki/端末#テキスト端末 "wikilink")。GNU EmacsはUnix系オペレーティングシステム上で[X Window Systemを利用できるため](../Page/X_Window_System.md "wikilink")、を直接利用したり、[Motif](../Page/Motif_\(GUI\).md "wikilink")、[LessTif](https://ja.wikipedia.org/wiki/LessTif "wikilink")、または[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")などの「ウィジットツールキット」を利用することでGUIを作成することができる。GNU EmacsはmacOSやWindowsといった各プラットフォームの[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")に、より密接に適合した[メニュー](https://ja.wikipedia.org/wiki/メニュー "wikilink")バー、[ツールバー](https://ja.wikipedia.org/wiki/ツールバー "wikilink")、[スクロールバー](../Page/スクロールバー.md "wikilink")および[コンテキストメニュー](../Page/コンテキストメニュー.md "wikilink")を提供するため、macOSやWindowsのネイティブなグラフィックスシステムを利用することもできる。

### GUIへの対応

Emacsはもとは文字端末での利用を前提に設計されていたものであるが、少なくともGNU Emacsバージョン18では[X Window Systemアプリケーションとしてコンパイルすることもできた](../Page/X_Window_System.md "wikilink")。しかし、その実装方法は、自前の[端末エミュレータ](../Page/端末エミュレータ.md "wikilink")を立ち上げ、その中で動くというものであり、ウィンドウシステムの持つ機能を十分に発揮するには至っていなかった。このためXEmacsなどのプロジェクトが生まれたが、GNU Emacs自身も徐々にGUIに対応していった。

Emacsバージョン21およびXEmacsではグラフィックス機能が強化されており、1バッファ中で複数のサイズやスタイルのフォントを混在させることもできる。また、画像を表示させることもでき、[ImageMagick](../Page/ImageMagick.md "wikilink")と連携してさまざまな画像ファイルを開くことができるようになった。

2009年のGNU Emacs 23ではフォントの扱いが大きく変わり、[TrueType](../Page/TrueType.md "wikilink")フォントが自由に使えるようになった。

#### Windows

現在はGNU Emacs自体を[Visual C++または](../Page/Microsoft_Visual_C++.md "wikilink")[Cygwin](../Page/Cygwin.md "wikilink")でコンパイルすることが可能である\[45\]。バイナリ形式でも配布されているので、zipを展開するだけでWindows上でEmacsが使用可能である\[46\]。

日本では、かつて宮下尚によりWin32アプリケーションとしてMule 2.3をベースにした[Mule for Win32](../Page/Mule.md "wikilink")、そしてGNU Emacs 20をベースにした[Meadow](../Page/Meadow.md "wikilink")がWindows上に移植・開発され、広く使われていた。2004年7月7日にはGNU Emacs 21をベースにしたMeadow2がリリースされたが、GNU Emacs 22以降には対応していない。一方、上記のバイナリは[日本語IMEからの入力に問題があるため](../Page/日本語入力システム.md "wikilink")、パッチをあててCygwinでビルドしたgnupack\[47\]が使われるようになってきている。

[SKK](../Page/SKK.md "wikilink")のようなGNU Emacs上の入力システムを使い、Windows上の日本語IMEを使用しない場合は、公式のバイナリをそのまま使えばよい。

Win32で動くEmacsをNTEmacsとよぶこともある。

#### macOS

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")は最初からGNU Emacsがインストール済みだが、標準ではGUIが使えない。銭谷誠司がGNU Emacs 22をmacOSの[Carbon](../Page/Carbon.md "wikilink") APIを使ってGUI対応したCarbon Emacsが使われてきたが、GNU Emacs 23からはGNU Emacsそのものが[Cocoa](../Page/Cocoa.md "wikilink") APIを使ったGUIで動くようになり、configureに `--with-ns` （nsは[NEXTSTEP](../Page/NEXTSTEP.md "wikilink")）オプションをつけるだけでGUIで動くEmacsをソースからビルドすることもできる。そのほか、GUIを[AquaとしたAquamacsなど](../Page/Aqua_\(コンピュータ\).md "wikilink")、多数のバリエーションが存在する。

macOSでは、コントロールキーのほかに[コマンドキー](../Page/コマンドキー.md "wikilink")と[オプションキー](../Page/オプションキー.md "wikilink")が用意されており、そのどちらかをMetaキー・もう片方をSuperキーとして使うことができる。Superキーの割り当ての一部はmacOSの標準のキー割り当てとよく似ている（s-x でカット・s-c でコピー・s-n で新しいフレームが開くなど）。ただし、その副作用として本来のオプションキーとしての機能は使えなくなってしまう。たとえば日本語キーボードでは[バックスラッシュ](../Page/バックスラッシュ.md "wikilink")をオプション+円記号で入力する必要があるので、特別な対応が必要となる。

## フォーク

### XEmacs

[Xemacs-21.5.b29.png](https://ja.wikipedia.org/wiki/File:Xemacs-21.5.b29.png "fig:Xemacs-21.5.b29.png")上の[XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink") 21.5\]\]  1991年初頭、GNU Emacs 19の初期α版をベースとしてと社の人達によりLucid Emacsが開発された。コードベースはすぐに2つに分割され、開発チームは単一プログラムとして併合しようとすることをあきらめた\[48\] 。これはフォークしたフリーソフトウェアのうち初期の最も有名な例の1つである。Lucid EmacsはXEmacsと名前を変え、Emacsの中でGNU Emacsに次いで2番目に有名な派生となった。XEmacsの開発は2009年[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")に最新の安定版であるバージョン21.4.22がリリースされてから遅くなっていき、その一方でGNU Emacsは以前はXEmacsにしかなかった機能の多くを実装していった。このため一部のユーザーはXEmacsの死を宣言するようになった\[49\]。

### その他のGNU Emacsのフォーク

XEmacsほど有名ではないGNU Emacsのフォークには、以下のものがある:

  - [Meadow](../Page/Meadow.md "wikilink") - [Microsoft Windows用の日本語バージョン](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[50\]。

  - \- Steve YoungsによるXEmacsのフォーク\[51\]。

  - [Aquamacs](../Page/Aquamacs.md "wikilink") - GNU Emacsをベースとし、[Macintosh](../Page/Macintosh.md "wikilink")[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")と統合することに焦点を当てている。

  - Remacs - [Rustプログラミング言語によるGNU](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink") Emacsの移植\[52\]。

## リリース履歴

Emacsを新しいリリースに「*アップグレード*」して得られる変更は、Emacsと一緒に配布されるNEWSファイルにリストされる\[53\]。以前のリリースへ「*ダウングレード*」して得られる変更は、*Antinews* ファイルにリストされる\[54\]。

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>大幅な変更[55]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>25.1</p></td>
<td><p>2016年9月17日</p></td>
<td><p>共有・動的ライブラリ（モジュール）のロード、TLS/SSL証明書の検証のサポート。曲線型引用符のための新規 'electric-quote-mode' 副モードの追加。isearch.elにおける文字折り畳みのサポート。Emacsバッファ内にネイティブウイジェットを組み込む機能のサポート。Unicode文字の挿入における新規機能の追加および機能の改善[56]。</p></td>
</tr>
<tr class="even">
<td><p>24.5</p></td>
<td><p>2015年8月10日</p></td>
<td><p>主にバグ修正のリリース[57][58]。</p></td>
</tr>
<tr class="odd">
<td><p>24.4</p></td>
<td><p>2014年10月20日</p></td>
<td><p>Emacs LispパッケージのACL（アクセスコントロールリスト）とデジタル署名のサポート、フルスクリーンとマルチモニターサポートの改善、フレームとウインドウの状態の保存と復元のサポート、テキスト端末上のメニューサポートの改善、別のビルトインウェブブラウザ (<kbd>M-x eww</kbd>)、新しい長方形のマークモード (<kbd>C-x SPC</kbd>)、ファイル通知サポート[59]。</p></td>
</tr>
<tr class="even">
<td><p>24.3</p></td>
<td><p>2013年3月10日</p></td>
<td><p>コアEmacs Lisp内、Common Lispエミュレーションライブラリの更新、Python用の新しいメジャーモードにおける一般変数[60]。</p></td>
</tr>
<tr class="odd">
<td><p>24.2</p></td>
<td><p>2012年8月27日</p></td>
<td><p>バグ修正のリリース[61]</p></td>
</tr>
<tr class="even">
<td><p>24.1</p></td>
<td><p>2012年6月10日</p></td>
<td><p>Emacs Lisp Package Archive、ネイティブ、オプションでGTK+3のカラーテーマ、双方向入力のサポート、emacs lispのレキシカルスコープのサポート[62]。</p></td>
</tr>
<tr class="odd">
<td><p>23.4</p></td>
<td><p>2012年1月29日</p></td>
<td><p>セキュリティフローの修正[63]。</p></td>
</tr>
<tr class="even">
<td><p>23.3</p></td>
<td><p>2011年3月10日</p></td>
<td><p>バージョン管理システムでEmacsを使う機能の改善。</p></td>
</tr>
<tr class="odd">
<td><p>23.2</p></td>
<td><p>2010年5月8日</p></td>
<td><p><a href="../Page/統合開発環境.md" title="wikilink">IDEとしてEmacsを使うための新しいツール</a>、JavaScriptソース編集用の新しい主モード、GUIでユーザーがタイプしている間に隠れるカーソル。</p></td>
</tr>
<tr class="even">
<td><p>23.1</p></td>
<td><p>2009年7月29日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Xft" title="wikilink">Xft</a>を通じたX上のアンチエイリアスフォントのサポート[64]、さらなる<a href="../Page/Unicode.md" title="wikilink">Unicode</a>のサポート、<a href="../Page/Portable_Document_Format.md" title="wikilink">PDFと</a><a href="../Page/PostScript.md" title="wikilink">PostScript</a>ファイル閲覧用のDoc-viewモードと新しいパッケージ、<a href="../Page/D-Bus.md" title="wikilink">D-Bus</a>経由のプロセス接続 (dbus)、<a href="../Page/GNU_Privacy_Guard.md" title="wikilink">GNU Privacy Guardによる接続</a> (EasyPG)、<a href="../Page/Extensible_Markup_Language.md" title="wikilink">XMLドキュメント編集用nXMLモード</a>、<a href="../Page/Ruby.md" title="wikilink">Ruby</a>プログラム編集用Rubyモードなど。Mac OS X上の<a href="../Page/Carbon.md" title="wikilink">Carbon</a>GUIライブラリの利用をより近代的な<a href="../Page/Cocoa.md" title="wikilink">Cocoa</a>GUIライブラリ利用に置き換え。</p></td>
</tr>
<tr class="odd">
<td><p>22.3</p></td>
<td><p>2008年9月5日</p></td>
<td><p>GTK+ツールキットサポート、強化マウスサポート、新しいキーボードマクロシステム、改善されたUnicodeサポート、X上のドラッグアンドドロップ操作、GDBへのグラフィカルユーザーインタフェースを含む多くの新しいモードとパッケージ、Pythonモード、数学ツールCalc、リモートファイル編集システムTramp ("Transparent Remote (file) Access, Multiple Protocol")[65]</p></td>
</tr>
<tr class="even">
<td><p>22.2</p></td>
<td><p>2008年3月26日</p></td>
<td><p>Bazaar、Mercurial、MonotoneおよびGit<a href="../Page/バージョン管理システム.md" title="wikilink">バージョン管理システム</a>の新しいサポート、CSS、Verilog、およびBibTeX編集用の新しい主モード、Imageモードのスクロールサポートの改善</p></td>
</tr>
<tr class="odd">
<td><p>22.1</p></td>
<td><p>2007年6月2日</p></td>
<td><p>GTK+グラフィカルツールキットのサポート、X上のドラッグアンドドロップのサポート、Mac OS X Carbon UIのサポート、org-modeバージョン4.67d[66]</p></td>
</tr>
<tr class="even">
<td><p>21.1</p></td>
<td><p>2001年10月20日</p></td>
<td><p>端末上のカラー表示およびそれ以外の属性のサポート、ビルトイン水平方向スクロール、サウンドサポート、ホイールマウスサポート、改善されたメニューバーレイアウト、画像、ツールバー、ツールチップのサポート、Unicodeサポート</p></td>
</tr>
<tr class="odd">
<td><p>20.1</p></td>
<td><p>1997年9月17日</p></td>
<td><p>多言語サポート</p></td>
</tr>
<tr class="even">
<td><p>19.34</p></td>
<td><p>1996年8月22日</p></td>
<td><p>ユーザーには見えない変更を伴うバグ修正リリース[67]</p></td>
</tr>
<tr class="odd">
<td><p>19.31</p></td>
<td><p>1996年5月25日[68]</p></td>
<td><p>Emacsがデフォルトで<a href="../Page/X_Window_System.md" title="wikilink">X11フレームをオープンする</a>。<a href="../Page/Microsoft_Windows_95.md" title="wikilink">Windows 95および</a><a href="../Page/Microsoft_Windows_NT.md" title="wikilink">NT上のスクロールバー</a>、Windows 95上でのサブプロセス、クラッシュ後の複数ファイル回復のための<span style="font-family: monospace, monospace;">recover-session</span>、米国準拠のためいくつかのdoctor.el機能の削除[69]</p></td>
</tr>
<tr class="even">
<td><p>19.30</p></td>
<td><p>1995年11月24日</p></td>
<td><p>MS Windows上の複数フレームのサポート、テキスト端末上でメニューバーが利用可能に、 WindowsとMacintoshで共通なキーバインディングをエミュレートするための<span style="font-family: monospace, monospace;">pc-select</span>パッケージ[70]</p></td>
</tr>
<tr class="odd">
<td><p>19.29</p></td>
<td><p>1995年6月19日[71]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>19.28</p></td>
<td><p>1994年11月1日</p></td>
<td><p>最初の公式v19リリース。X Window Systemと利用した複数フレームのサポート。バージョン管理システム用の新しいインタフェースであるVC、font-lockモード、<a href="../Page/バイナリエディタ.md" title="wikilink">バイナリ編集用のhexlモード</a></p></td>
</tr>
<tr class="odd">
<td><p>19.7</p></td>
<td><p>1993年5月22日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>18.59</p></td>
<td><p>1992年10月31日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>18.53</p></td>
<td><p>1989年2月23日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>18.52</p></td>
<td><p>1988年8月17日</p></td>
<td><p>いくつかの「<a href="../Page/アメリカ国家安全保障局.md" title="wikilink">NSAをそらす</a>」キーワードを送信する各メッセージに追加するための<span style="font-family: monospace, monospace;">spook.el</span>ライブラリ[72]</p>
<p>RL counter terrorism Red Cross TWA Human to Human CIA al-Qaida Smuggling sneakers Ansar al-Islam Burst Morwenstow Sears Tower Sick HRT</p></td>
</tr>
<tr class="odd">
<td><p>18.24</p></td>
<td><p>1986年10月2日</p></td>
<td><p>サーバーモード[73]、<kbd>M-x disassemble</kbd>、EmacsはTCP接続をオープン可能に、<a href="https://ja.wikipedia.org/wiki/xterm" title="wikilink">xterm</a>のコンソールモード内でEmacsをオープンするための<kbd>emacs -nw</kbd></p></td>
</tr>
<tr class="even">
<td><p>17.36</p></td>
<td><p>1985年12月20日</p></td>
<td><p>Backup file version numbers</p></td>
</tr>
<tr class="odd">
<td><p>16.56</p></td>
<td><p>1985年7月15日</p></td>
<td><p>最初のEmacs 16リリース。Emacs-lisp-modeがlisp-modeから分離[74]、著作権問題のため<a href="../Page/Gosling_Emacs.md" title="wikilink">Gosling Emacs由来のコードを全て除去</a>[75]</p></td>
</tr>
<tr class="even">
<td><p>15.10</p></td>
<td><p>1985年8月11日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>13.0?</p></td>
<td><p>1985年3月20日</p></td>
<td></td>
</tr>
</tbody>
</table>

## 脚注

## 参考文献

  -
  -
  -
  -
  -
## 外部リンク

  -
[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:ファイル比較ツール](https://ja.wikipedia.org/wiki/Category:ファイル比較ツール "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:Linuxのソフトウェア](https://ja.wikipedia.org/wiki/Category:Linuxのソフトウェア "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink") [Category:1985年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1985年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. \]
11. ; see also ["Stallman on handing over GNU Emacs, its future and the importance of nomenclature"](http://www.networkworld.com/community/node/25360)
12. <https://lists.gnu.org/archive/html/emacs-devel/2015-09/msg00849.html>
13.
14. <http://mail.gnu.org/archive/html/bug-gnu-emacs/2000-09/msg00065.html>
15.
16. [License revoked: Applying Section 4 of the GPL and the lessons of Best Buy to Google’s Android](http://brownrudnick.com/blog/emerging-technologies/license-revoked-applying-section-4-of-the-gpl-and-the-lessons-of-best-buy-to-googles-android/) by Edward J. Naughton (Aug 8, 2011)
17. [スラッシュドット](../Page/スラッシュドット.md "wikilink")における[Emacs-Has-Been-Violating-the-GPL-Since-2009](http://developers.slashdot.org/story/11/07/29/1445252/Emacs-Has-Been-Violating-the-GPL-Since-2009) (2011)
18. [Re: Compiled files without sources????](http://lists.gnu.org/archive/html/emacs-devel/2011-07/msg01155.html) Richard Stallman (28 Jul 2011)
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29. <https://github.com/ch11ng/exwm/wiki>
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40. <https://www.gnu.org/software/emacs/MACHINES>
41.
42.
43.
44.
45. [GNU Emacs FAQ for MS Windows](https://www.gnu.org/software/emacs/manual/html_mono/efaq-w32.html#Compiling)
46. <http://ftp.gnu.org/gnu/emacs/windows/>
47. <http://en.sourceforge.jp/projects/gnupack/>
48.
49.
50. [FrontPage - Meadow Wiki](http://www.meadowy.org/meadow/pukiwiki-en/)
51.
52.
53.
54.
55. [Emacs Timeline](http://www.jwz.org/doc/emacs-timeline.html). Jwz.org. Retrieved on 2013-07-17.
56.
57.
58.
59.
60.
61.
62.
63.
64.
65.
66.
67.
68.
69.
70.
71.
72.
73.
74.
75.