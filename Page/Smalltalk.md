> この記事は[Smalltalk](https://ja.wikipedia.org/wiki/Smalltalk)から翻訳されています。


（スモールトーク）は、 の[オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")（および[クラス](https://ja.wikipedia.org/wiki/クラス_\(コンピュータ\) "wikilink")）、の徹底した[動的性](https://ja.wikipedia.org/wiki/動的プログラミング言語 "wikilink")、 のタートル操作や描画機能に、アラン・ケイの「メッセージング」というアイデアを組み合わせて作られた[クラスベース](https://ja.wikipedia.org/wiki/クラスベース "wikilink")で手続き型の純粋[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")、および、それによって記述構築された[統合化プログラミング環境](https://ja.wikipedia.org/wiki/統合化プログラミング環境 "wikilink")の呼称。

で一語であり、「」「」などは誤りである。

大規模な開発実績としてはCargill Lynx Project\[1\]があり、国産製品の開発実績としては[MCFrame](https://ja.wikipedia.org/wiki/MCFrame "wikilink")がある。

## 概要

### 開発の経緯

[ゼロックス](https://ja.wikipedia.org/wiki/ゼロックス "wikilink")の[パロアルト研究所](https://ja.wikipedia.org/wiki/パロアルト研究所 "wikilink")（）で[1970年代](https://ja.wikipedia.org/wiki/1970年代 "wikilink")に約10年かけ3世代（-72、76、）を経て整備された。当初は、[ダイナブック](https://ja.wikipedia.org/wiki/ダイナブック "wikilink")である  の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")的位置付けだったが、 のゼロックス社製品としての販売の可能性が同社上層部決定により完全に排除されたこと、発案者である[アラン・ケイ](https://ja.wikipedia.org/wiki/アラン・ケイ "wikilink")の研究開発グループ離脱などを受けてダイナブック色は失せ、 のハードウェア技術を基にした商用マシン上で動作するプロの開発者向け[統合化プログラミング環境](https://ja.wikipedia.org/wiki/統合開発環境 "wikilink")「80」として[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に発売されることになる。現在はシンコム\[2\]より という製品名で主要なオペレーティングシステム向けに販売されている。

### Smalltalkの変遷

<small>※この節は\[3\]\[4\]を元に執筆されている。</small>

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>-71</p></td>
<td><p>最初にSmalltalkの名前を冠した言語だが、文法など一部仕様が定められただけで実装はされていない。</p></td>
</tr>
<tr class="even">
<td><p>-72</p></td>
<td><p>メッセージングの機構により最初に動作したSmalltalk。初期のGUIはタートルグラフィックスで表現されたウインドウやメニューなど原始的な構成で、言語仕様的にもクラスが関数であったり、メソッド定義がリーダーマクロのようであったりと、現在のSmalltalkとは異なる点が多い。</p></td>
</tr>
<tr class="odd">
<td><p>-74</p></td>
<td><p>Smalltalk-72に対し、処理系の高速化、GUIの整備、オブジェクト指向仮想メモリー（OOZE）を導入したバージョン。</p></td>
</tr>
<tr class="even">
<td><p>-76</p></td>
<td><p>現在のメッセージ式に近い文法（特にキーワードメッセージ式）を取り入れたSmalltalk。メタクラス、第一級オブジェクトとしてのブロックなどはまだない。</p></td>
</tr>
<tr class="odd">
<td><p>-78</p></td>
<td><p>Smalltalk-76を、可搬式の試作機「<a href="https://ja.wikipedia.org/wiki/:en:Xerox_NoteTaker" title="wikilink">NoteTaker</a>」で動作するよう<a href="https://ja.wikipedia.org/wiki/8086" title="wikilink">8086</a>向けに<a href="https://ja.wikipedia.org/wiki/BitBlt" title="wikilink">BitBlt</a>等を再構築し、小さく整理したバージョン。</p></td>
</tr>
<tr class="even">
<td><p>-80</p></td>
<td><p>現在に知られる仕様となったSmalltalk。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-80を一般に普及させるために開発・販売されたSmalltalk。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>ObjectWorksを引き継ぎ開発されたSmalltalk。Smalltak直系の子孫で現代に至るSmalltalkの中で本家と言える存在である。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-80 v1（リリース前バージョン）を元に、XEROX社に許諾および指導を受けて<a href="https://ja.wikipedia.org/wiki/アップル_(企業)" title="wikilink">アップルが開発したSmalltalk</a>。同時期に<a href="https://ja.wikipedia.org/wiki/ディジタル・イクイップメント・コーポレーション" title="wikilink">DEC社</a>、<a href="https://ja.wikipedia.org/wiki/テクトロニクス" title="wikilink">テクトロニクス</a>社、<a href="https://ja.wikipedia.org/wiki/ヒューレット・パッカード" title="wikilink">ヒューレット・パッカード</a>社でも同様の試みがなされている。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>アップルに移籍したアラン・ケイ、ダン・インガルスらによってを元に開発された。の設計者により開発されており、いわば分家と言える存在である。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>Squeakから派生した実装。大胆で実験的な機能追加の試みが多いが、2017年現在精力的かつ活発に開発が進められているSmalltalk処理系のひとつ。</p></td>
</tr>
</tbody>
</table>

###  とオブジェクト指向

豊富で整備されたクラスライブラリーは、特に[オブジェクト指向プログラミング](https://ja.wikipedia.org/wiki/オブジェクト指向プログラミング "wikilink")の手本とされ、[デザインパターンの宝庫と称されるまで洗練されたものになっている](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")。また、後世の多くのオブジェクト指向[プログラミング言語](../Page/プログラミング言語.md "wikilink")に直接間接的に多大な影響を与えた。

アラン・ケイが「[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")」という言葉を創った当初は、 システムが体現した「パーソナルコンピューティングに関わる全てを『[オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")』とそれらの間で交わされる『メッセージ送信』によって表現すること」を意味していた。しかしのちに、 の設計者として知られる[ビャーネ・ストロヴストルップ](https://ja.wikipedia.org/wiki/ビャーネ・ストロヴストルップ "wikilink")が（自身、 の影響は受けていないと主張する） の設計を通じて整理し発表した「『[継承](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")』機構と『[多態性](https://ja.wikipedia.org/wiki/多態性 "wikilink")』を付加した『[抽象データ型](https://ja.wikipedia.org/wiki/抽象データ型 "wikilink")』のスーパーセット」という考え方として広く認知されるようになった（[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")、[継承](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")、[多態性](https://ja.wikipedia.org/wiki/多態性 "wikilink")）。現在は、両者の渾然一体化した曖昧な概念として語られることが多い。

###  の独自性

は、オブジェクトへのメッセージ送信を率直に記述する表記の特殊性や、制御構造をもたずオブジェクトへのメッセージ送信の形で記述する徹底ぶりとも併せて、[C言語](../Page/C言語.md "wikilink")や  などの流れを強く受け継ぐ言語、およびその開発手法に慣れた開発者にとって極めてとっつきにくい言語・環境であるといわれている。このことは、 が単なるプログラミング言語ではなく、従来のオペレーティングシステムの概念をも包括する「環境」であることが一つの理由である。 を単なる言語としてとらえると、他の言語と比較したとき、使用するオペレーティングシステムの[グラフィカルユーザインターフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")に全く従わないなど、その独自性が大きな「欠点」として映る場合もある。

これは  や  など、旧来の  環境、つまりダイナブックコンピュータ環境の要素を引き継ぐ統合開発環境を通じて  言語や処理系を学ぶなら、多かれ少なかれ新たなオペレーティングシステムに接するような心構えを持つべきことを意味する。

## 環境および処理系としてのSmalltalk

###  環境から見た 言語

環境から見た  言語は、いわば  などの[シェル](https://ja.wikipedia.org/wiki/シェル "wikilink")に近い。 環境内であればどこでもマウスで選択した文字列を  のソースコードとして実行できるためシェルにコマンドを打ち込んだ時の様に簡単な問い合わせをすぐ実行できるようになっている。

例えばオブジェクト(クラスやメソッドも含む)の構造を調べたければ、そのオブジェクトにセレクターあるいはセレクターを使ったメッセージ式を書き、そのメッセージ式をマウスで選択してdo it(WindowsであればCtrl+Dを押す)すれば良い。

また、設定値の指定に  言語のメッセージ式が使われる。現在設定されている値がメッセージ式として取得でき、値の設定をメッセージ式として指定する。この設定値を指定するメッセージ式は  環境の実行中に設定用のウィンドウから入力される。

### 仮想機械方式

#### 仮想機械による実行

環境は、 環境の実行方法として現実のハードウェアに依存している機械語命令を使わず、現実のハードウェアから独立した中間言語命令(仮想機械に対する機械語命令)を[仮想機械](https://ja.wikipedia.org/wiki/仮想機械 "wikilink")により実行する仮想機械方式を採用している。  の中間言語命令は、全てイメージファイルというファイルに書き込まれ  の仮想機械はそのイメージファイルを読み込んで 環境を実行する。

この仮想機械方式による  の実行方法は  の言語仕様にも含まれている。\[5\] なお、 が導入したこの仮想機械方式はの[pコードマシン](https://ja.wikipedia.org/wiki/pコードマシン "wikilink")から[アラン・ケイ](https://ja.wikipedia.org/wiki/アラン・ケイ "wikilink")が着想を得たものである。\[6\]

#### イメージファイル

イメージファイルは、 環境の実行状態をそのまま保存したファイルである。イメージファイルは  環境実行中に生成された全てのオブジェクトを直列化して保存することで 環境の実行状態を保存している。この直列化されたオブジェクトには、 の中間言語も含まれている。イメージファイルに含まれる中間言語命令は、 自身によって記述されたコンパイラーによってソースコードから翻訳された、バイト列のオブジェクトである。

#### 仮想機械とブートストラップ

の実行環境が全く存在しない初期の状況ではコンパイラーも仮想機械も  で用意する事はできない。このため  の初期段階では[ALTOの](https://ja.wikipedia.org/wiki/Alto "wikilink")[アセンブリ言語](https://ja.wikipedia.org/wiki/アセンブリ言語 "wikilink")によりコンパイラーや仮想機械が実装されていた。\[7\]

### 実行時書き換え

環境は翻訳方式を使う処理系としては珍しくプログラムの実行時書き換えを基本とする。例えば後述のClass Browserに入力したプログラムはソースコードを中間言語に変換したあと環境の一部として取り込まれ、環境を再起動したり読み込み操作をしなくても起動中の環境内で実行することができる。C++のような翻訳式の言語であれば原則、ソースコードを書き換えた場合は原則プログラムの再起動が必要となる。またPythonの様な言語ではソースコードを再読み込みする処理を予め書き換えたい処理の呼び出し元に組み込んでおかなければソースコードをいくら書き換えても動作に反映できない。ではその再起動や再読み込み処理の組み込みが必要ない。このため環境をソースコードを書き換える都度環境全体を再起動しなくて済むのはもちろん、Windowを表示するプログラムを作った場合であれば、Window内のButtonの動作を変更する時もWindowを表示したままソースコードを書き換えて動作を変更できる。このためButtonを押すまでに複数の手順が必要なプログラムやWindowの表示に時間がかかるプログラムでもButtonを表示した状態から再起動せず何度でもやり直しができ効率的なソースコード変更が可能になっている。

### 環境の種類

<table>
<thead>
<tr class="header">
<th><p>環境</p></th>
<th><p>使用している仮想機械</p></th>
<th><p>有償版</p></th>
<th><p>無償版</p></th>
<th><p>CPU</p></th>
<th><p>OS</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>-</p></td>
<td><p>○</p></td>
<td><p>○[8]</p></td>
<td><p>-</p></td>
<td><p>Win</p></td>
<td><p>2017年現在VisualWorksを販売するCincomのWindows向け製品となっている。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>○</p></td>
<td><p>○[9]</p></td>
<td><p>x86/x64</p></td>
<td><p>Unix/Linux/OSX/Win</p></td>
<td><p>ゼロックス時代のSmalltalkを引き継ぐSmalltalk環境。名前空間[10]やイメージファイルからモジュールを切り離せるパーセル[11]、OSのデスクトップ上に表示できるウィンドウ等以前のSmalltalkより大きく拡張されている。2017年現在も活発に開発されている。</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>x86</p></td>
<td><p>Unix/Linux/OSX/Win</p></td>
<td><p>Apple Smalltalkから派生したプラットフォーム非依存やマルチメディア対応を強化したSmalltalk環境。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Pharo" title="wikilink">Pharo</a></p></td>
<td></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>x86/x64</p></td>
<td><p>Unix/Linux/OSX/Win</p></td>
<td><p>Squeakから開発向けに派生したSmalltalk環境。[12]</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>x86/x64</p></td>
<td><p>Unix/Linux/OSX/Win</p></td>
<td><p>データベース管理システムとしての用途に特化したSmalltalk環境。その用途からGUIは無い。2017年現在GemTalk systemにて無償版が配布されている。[<a href="https://gemtalksystems.com/%5D2017年現在も活発に開発されている">https://gemtalksystems.com/]2017年現在も活発に開発されている</a>。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/GNU_Smalltalk" title="wikilink">GNU Smalltalk</a></p></td>
<td><p>-</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>x86/x64/arm</p></td>
<td><p>Unix/Linux/Android/OSX/Win</p></td>
<td><p>GUI無しでの開発に特化しており他の環境ではGUIを前提としている機能をCUIで実行できる。ただしGUI環境も用意されている。[<a href="https://www.gnu.org/software/smalltalk/manual/gst.html%5DCと連携するための機能が他の処理系と比較して特に強力であり、関数のポインターを指定すべき引数にブロックを渡したり、関数呼出もできる各種ポインター操作ができるようになっている。しかも、関数のポインターとして渡すブロックは変数を束縛した状態で渡す事が可能になっている">https://www.gnu.org/software/smalltalk/manual/gst.html]Cと連携するための機能が他の処理系と比較して特に強力であり、関数のポインターを指定すべき引数にブロックを渡したり、関数呼出もできる各種ポインター操作ができるようになっている。しかも、関数のポインターとして渡すブロックは変数を束縛した状態で渡す事が可能になっている</a>。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>-</p></td>
<td><p>Win</p></td>
<td><p>言語仕様に静的型検査を追加したSmalltak環境。Hot spotによる最適化を初めて実装したVMで極めて高速に動作する。Strongtalkで開発されたHot spot技術はJavaVMなどにも移植された[13]</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>x64</p></td>
<td><p>Unix/Linux/OSX/Win</p></td>
<td><p>Pharoの環境を元に言語仕様に静的型検査と動的型検査を追加したSmalltak環境。[14]</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>Web Browserに依存</p></td>
<td><p>Web Browserに依存</p></td>
<td><p>Web Browser上で動作するSmalltalk環境。[15]</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>Win</p></td>
<td><p>Windowsに特化しておりOS固有の機能やOS固有のGUIを使用できる。OSとの親和性が高い。[16][17]SmalltalkからJavaを呼び出すJNIPortを最初に実装した処理系であり、JNIPortが使える処理系ではDolphin Smalltalkの名前を目にする機会が多い。[18]</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>Java VMに依存</p></td>
<td><p>Java VMに依存</p></td>
<td><p>Java VMを使用する。[19]</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/共通言語基盤" title="wikilink">共通言語基盤</a>に依存</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/共通言語基盤" title="wikilink">共通言語基盤</a>に依存</p></td>
<td><p>.NET Frameworkを使用する。[20]</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>Unix</p></td>
<td><p>Unixで動作するSmalltalk環境。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>pc98で動作するSmalltalk環境。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/VisualAge" title="wikilink">VisualAge</a></p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>から<a href="https://ja.wikipedia.org/wiki/IBM" title="wikilink">IBM</a>が派生させて開発したSmalltalkベースの統合開発環境。Javaで記述された<a href="https://ja.wikipedia.org/wiki/Eclipse_(統合開発環境)" title="wikilink">Eclipseの原型でもある</a>。 VA Smalltalkは</p></td>
</tr>
<tr class="even">
<td><p>VA Smalltalk</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>IBMが開発を停止したVisualAgeの派生製品。[21]2018年現在も開発が継続されている。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>Win</p></td>
<td><p>Windowsに特化しActive Xを生成できる。[22]</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>Smalltalk環境として稼働する上で必要最低限の機能だけを備えるSmalltalk環境。</p></td>
</tr>
<tr class="odd">
<td><p>（）</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/アクターモデル" title="wikilink">アクターモデル</a>による分散処理を導入した環境。<a href="http://ci.nii.ac.jp/naid/110003743373">1</a></p></td>
</tr>
<tr class="even">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
</tr>
</tbody>
</table>

### GUIツール

[Linux上で稼働するSmalltalk環境(VisualWorks)。 左上:Class Browser, 右上:Transcript, 左下:Workspace, 右中段:Debugger/Notifier, 中央下段:Inspector, 右下段:変数を表示したWorkspace](https://ja.wikipedia.org/wiki/File:VisualWorks.png "fig:Linux上で稼働するSmalltalk環境(VisualWorks)。 左上:Class Browser, 右上:Transcript, 左下:Workspace, 右中段:Debugger/Notifier, 中央下段:Inspector, 右下段:変数を表示したWorkspace")

#### 準標準的なGUIツール

GUIを使わないような特殊なものを除き、大半のSmalltalk環境では次のようなGUIツールが用意されている。

  - Class Browser(System Browser)
  - Transcript
  - Workspace
  - Debugger/Notifier
  - Inspector

Smalltalkの開発ではこれらのツールを使って開発する事が半ば前提となっている。

#### Class Browser(System Browser)

Smalltalk環境内に存在する全てのクラスを(存在する場合は名前空間も)表示/編集できるツールで、Smalltalk開発において中核となるツールである。

#### Transcript

言うなれば出力しかできないコンソールといったツールで、プログラムの実行結果を簡易的に表示したいときに使われるツールである。Smalltalk環境内でTranscript変数に書き込まれたメッセージは、全てこのTranscriptに表示される。

#### Workspace

言うなればコンソールの入力側とテキストエディターを組み合わせた様なツールである。一見すれば書いたコードを実行できるだけの簡易的なテキストエディターにしか見えないが、WorkspaceはWorkspace変数というWorkspace固有の変数を持っており、Workspace内で実行されたSmalltalkコードの実行結果を保持することができる。このため、長いコードを書くような用途では使わず、Smalltalk環境に対するパッケージの追加や、環境設定、ファイルの一時的な操作など一時的な操作を実行する場所として使われる。

#### Debugger/Notifier

#### Inspector

オブジェクトの内部構造を再帰的に表示するツールである。また、多くの場合オブジェクトの編集が可能でありWorkspaceと組み合わせてオブジェクトを組み立てていくことが可能である。例えば画面部品をWindowを表すオブジェクトに組み込み、クラス変数に格納するといった具合である。Inspectorに限らずSmalltalk環境全体に共通することであるが、オブジェクト内の変数を表示するときは内部構造そのままではなくオブジェクトの文字列表現で表示する。このため内部がHash map等複雑な構造になっている場合でも`Dictionary (#key -> 'value' )`といった読み易い表示となる。

## 言語としてのSmalltalk

### 言語としての設計思想

言語として  が目指したもの。それは計算機を計算機の集合体として構築し、さらに計算機を構成する個々の計算機も計算機の集合体で構築するというように、再帰的な計算機を構築することであった。この再帰的な計算機を構築している無数の計算機は、個々の内部には干渉せずメッセージによる通信のみによって相互作用を発生させ目的の計算を完遂させる。

ここでいう計算機が  ではオブジェクトという形で実装された。

この設計思想の誕生は、と[B5000の設計者らが会談した際の次の発言をアラン](https://ja.wikipedia.org/wiki/バロース_B5000 "wikilink")・ケイが聞き「計算機の全体を計算機とみなした場合、その計算機の構成要素を計算機に分解するのではなく関数やデータ構造に分解したいと誰が思うのか」と疑問を浮かべた事がきっかけとなっている。 \[23\]

ここで言及された再帰という概念は、オブジェクトの成立以外にも  の至るところに影響を与えている。

  - 反復はメソッドの再帰呼び出し。

  - インスタンスオブジェクトを生成しているクラスオブジェクトも、クラスオブジェクトに所属するインスタンスオブジェクトであり再帰関係を持つ。

  - `Metaclass`は`Metaclass class`のインスタンスオブジェクトであり`Metaclass class`は、`Metaclass`であり再帰関係を持つ。

  - 基本的な派生元となる`Object`や`ProtoObject`は、それらから派生した`UndefinedObject`のインスタンスオブジェクトである`nil`を継承しており再帰関係を持つ。

  - 言語は  言語自身によりメッセージ送信等の言語機能が制御される。

  - 言語の翻訳や仮想機械は  言語により実装される。

  - 言語の大域変数は`Smalltalk`変数に格納されたオブジェクトにより管理されるが、`Smalltalk`変数自体も大域変数である。

### 言語仕様の種類

の言語仕様は原則として非常に単純なため、環境もしくは処理系の相違による互換の有無は、クラスライブラリーの差異程度に由来するもの（ある意味、バージョンの違いもこれも含まれる）から、言語仕様自体の改変に由来のものまで空間的に連続で多岐にわたる。このため、単に  として語弊のある場合、一般にその環境および処理系の呼称もしくは商標（必要ならそのバージョン）をして他と区別するために用いる慣習がある。

### 文法

#### コメント

「`"～"`」のようにダブルクオーテーションでくくった文字列がコメントとして扱われる。

#### 定数表現

主な定数表現には次のようなものがある。

| 型                    | 例                        |
| -------------------- | ------------------------ |
| 整数                   | `3`                      |
| 整数(16進数)             | `16r3`                   |
| 小数                   | `3.4`                    |
| 浮動小数点数               | `3.4e5`                  |
| 文字                   | `$a`                     |
| 文字列                  | `'abc'`                  |
| シンボル                 | `#abc`                   |
| 記号を含むシンボル            | `#'*abc'`                |
| 配列（要素は定数限定）          | `#( 'This' #is $a 10 )`  |
| バイト配列（要素は0〜255の定数限定） | `#[ 0 255 16r0 16r255 ]` |
| ブロック（引き数なし）          | `[ 3 + 4 ]`              |
| ブロック（引き数付き）          | `[ :x \| x + 1 ]`        |

定数ではないが、よく用いられるオブジェクトの生成式には次のようなものがある。

| 型   | 例          |
| --- | ---------- |
| 分数  | `3 / 4`    |
| 複素数 | `3 + 4i`   |
| 座標  | `3 @ 4`    |
| 共同体 | `'a' -> 0` |

言語機能の様に見えるが「`/`」や「`@`」などはただのセレクターであり、 の使用者も同様の機能を作ることが出来る。

#### 変数

一時変数は宣言が必要で、「`|`」で挿むように記述する。変数への代入は「`:=`」。古い処理系では「`_`」が使用された（字形は「←」）。変数に型はなく全て[ハンドル](https://ja.wikipedia.org/wiki/ハンドル "wikilink")になっている。

``` smalltalk
| a b |
a := 3.
b := 4.
```

#### 擬変数

他の言語で予約語にあたる擬変数は `self`、`super`、`nil`、`true`、`false`、`thisContext` の6つ。`self` と `super` はそのメソッドを呼び出したメッセージの受け手（レシーバー）を、`nil` と `true` と `false` はそれぞれ `UndefinedObject`、`True`、`False` に属するソルインスタンス（唯一の実体）を、`thisContext` は実行中のコンテキスト（スタックフレーム）を参照するのに使える。

`self` と `super` は同種のオブジェクトだが、メッセージ式でメッセージレシーバーに指定されたときのメソッド検索の起点が異なり、`self` ではオブジェクトが属するクラス、`super` ではその基底クラスである。

#### メッセージ式

では「メッセージ式」と呼ばれる書式でコードを記述する。メッセージ式は「レシーバー」に「メッセージ」を送ることを表すためのもので、そのまま

``` smalltalk
receiver message
```

と記述する。メッセージはさらに、呼び出されるされるメソッド（処理手順）の名前を表す「メッセージセレクター」\[24\]と0個以上の引数の組み合わせからなる。ただし  の場合必ずしもセレクターとメソッド名は一致しない。また、メッセージの送り先はメソッドではなくブロックや外部の関数になっている場合もある。セレクターは引数の数だけコロンを自身に含まなければならず、メッセージとして記述する際にはコロンの直後に引数を挿入する。

<table>
<thead>
<tr class="header">
<th><p>メッセージ式</p></th>
<th><p>セレクター</p></th>
<th><p>引数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>receiver noArg</code></p></td>
<td><p><code>noArg</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><code>receiver oneArg: arg</code></p></td>
<td><p><code>oneArg:</code></p></td>
<td><p><code>arg</code></p></td>
</tr>
<tr class="odd">
<td><p><code>receiver firstArg: arg1 secondArg: arg2</code></p></td>
<td><p><code>firstArg:secondArg:</code></p></td>
<td><p><code>arg1</code>、<code>arg2</code></p></td>
</tr>
</tbody>
</table>

引数なしのメッセージを**単項メッセージ**、そのセレクターを**単項セレクター**と呼び、引数ありのメッセージを**キーワードメッセージ**、そのセレクターを**キーワードセレクター**と呼ぶ。メッセージ記述の際に引数の挿入により分断されたキーワードセレクター断片（例えば `firstArg:secondArg:` なら `firstArg:` と `secondArg:`）を**キーワード**と呼ぶが、あくまで便宜的な呼び名に過ぎず、そうした言語要素は存在しない。他の言語に見られる「キーワード引数」のように省略できるものではなく、また引数順を入れ替えられるものでもない。

セレクターは原則としてアルファベットと数字と0個以上（かつ、引数と同数）のコロンから成るが、例外として二項演算を模した記述が可能となるように記号のみから成る引数1つのセレクターを使ってメッセージ式を記述することもできる。これを**[二項メッセージ](https://ja.wikipedia.org/wiki/利用者定義演算子 "wikilink")**、そのセレクターを**二項セレクター**と呼ぶ。

| メッセージ式                 | セレクター | 引数         |
| ---------------------- | ----- | ---------- |
| `3 + 4`                | `+`   | `4`        |
| `#( 1 2 3 ), #( 4 5 )` | `,`   | `#( 4 5 )` |

この場合、上の「`3 + 4`」では、「`3`」がレシーバーで「`+ 4`」がメッセージである。

通常の処理系では、単項メッセージ、二項メッセージ、キーワードメッセージの順で評価される。二項メッセージ間で乗除の優先はない。

| メッセージ式                       | 結合性を明示した等価の表現                            |
| ---------------------------- | ---------------------------------------- |
| `3 + 4 * 5 min: 6 factorial` | `( ( 3 + 4 ) * 5 ) min: ( 6 factorial )` |

セミコロン「`;`」でメッセージ式を区切る事により、1個のレシーバーに対して複数のメッセージを送ることが出来る。これをカスケード式という。

``` smalltalk
| collection |

collection := OrderedCollection
    new
    add: 0;
    add: 1;
    add: 2;
    add: 3;
    add: 4;
    yourself.
```

カスケード式を用いて書いた上記の文は、カスケード式を用いない次の文と等価である。

``` smalltalk
| collection |

collection := OrderedCollection new.
collection add: 0.
collection add: 1.
collection add: 2.
collection add: 3.
collection add: 4.
```

#### 制御構文

複数の式を順次実行する場合は、式をピリオドで区切る。メソッドを中断し戻り値を指定するには**復帰文**「`^ 戻り値式`」を使う。言語機能として持つ制御構文は復帰文を除いて存在せず、復帰文以外の制御は制御構文と同等の機能を持ったメッセージ式で代用する。

##### ブロック

ブロックは、他の言語で言えば無名関数やクロージャーに該当する機能である。ただし  のブロックは関数ではなくオブジェクトである事に加え、無名関数というより制御構文としての性格が強くなっている。並列実行の基本単位にもなる。

ブロックは、引き数の数毎に複数定義された「`value`」を含むメッセージを送る事で、ブロック内に記述されたメッセージ式を実行し結果を返す。

``` smalltalk
[                 　0               ] value.             "-> 0"
[ :value1         | value1          ] value: 1.          "-> 1"
[ :value1 :value2 | value1 + value2 ] value: 1 value: 1. "-> 2"
```

ブロック内の`:value1 :value2`は引き数であり、「`|`」以降は「`value`」を含むメッセージが送られた際実行するメッセージ式である。「`value`」を複数ならべたセレクターは4個程度まで( `#value:value:value:value:` )しか定義されておらず。5個以上引き数を取る場合は、配列を引き数とする`#valueWithArguments:`を使う必要がある。メソッドが値を返す際は、復帰文の記述が必要となるがブロックの場合は値を返すのに復帰文は必要ない。最後に実行されたメッセージ送信の結果あるいは、最後に書かれた値が戻り値となる。ブロックは制御の基本となるオブジェクトであるため、「`value`」を含むメソッド以外にも膨大なメソッドを持っている。ただし、後述する他の制御構文はブロックに対し`#value`セレクターまたは、`#value:`セレクターを使ったメッセージしか送らない。

ブロックには`value`と合わせてよく使われるセレクターとして「`cull`」がある。`cull`の振る舞いは、ほぼ`value`と同じであるが、ブロックがメッセージに含まれる引き数を無視できるという違いがある。

``` smalltalk
[ :value1 | value1 ] cull: 1 cull: 2. "-> 1"
```

`cull`はブロックによる分岐制御が主目的であるが、分岐の基準になったオブジェクトを参照する場合もあるようなセレクターで使われる。典型的な例は、オブジェクトがnilで無いときだけブロックを実行する`#ifNotNil:`である。

``` smalltalk
| block value1 value2 |

block := [ :value | value ].

value1 := 1.
value2 := 2.

value1 ifNotNil: [ 9 ]. "-> 9"
value1 ifNotNil: block. "-> 1"
value2 ifNotNil: block. "-> 2"
```

##### 条件分岐

条件分岐は `#ifTrue:ifFalse:` セレクターを用いたメッセージ式として、条件式の結果の真偽値へのメッセージ送信の形で次のように記述する。

``` smalltalk
3 < 4 ifTrue: [ 5 ] ifFalse: [ 6 ].
```

では `nil` がオブジェクトである。これを利用した `nil` 専用の条件式も存在する。

``` smalltalk
object := nil.
object ifNil: [ 5 ] ifNotNil: [ 6 ].
object ifNotNilDo: [ :value | value inspect. ].
```

条件分岐の制御において、他の言語でいう`switch`に直接該当する文は存在しない。多態性を利用して分岐するか、次のように連想配列を利用して分岐するため不要である。

``` smalltalk
something: aNumber
    | switch |

    "速度が求められる場合は、初期化済みのDictionaryのオブジェクトをインスタンス変数やクラス変数にキャッシュする。"
    switch := Dictionary
        new
        at: 1 put: [ #a ];
        at: 2 put: [ #b ];
        at: 3 put: [ #c ];
        yourself.

    ^ ( switch at: aNumber ifAbsent: [ #z ] ) value.
```

但し一部の処理系では、次のような`switch`に類似した書き方ができるものも存在する。

``` smalltalk
something: aNumber

    ^ aNumber caseOf:
    {
        [ 1 ]->[ #a ].
        [ 2 ]->[ #b ].
        [ 3 ]->[ #c ].
    }.
```

##### 反復

反復制御において`for` に直接該当する文は存在しない。代わりに回数を指定した反復がある。回数を指定した反復は、整数型へのメッセージ送信の形で次の様に記述する。

``` smalltalk
 "100回の反復処理を実行する"
100 timesRepeat:
[
    "反復実行する処理"
].
```

現在の反復回数を参照しながら反復する事も出来る。

``` smalltalk
 "100回の反復処理を実行する"
1 to: 100 do:
[ :each |
    "eachは現在の反復回数"
].
```

`for`　に該当する文は存在しないものの、`while` に該当する文は存在する。`while` に該当する反復は、ブロックに対するメッセージ送信の形で次の様に記述する。

``` smalltalk
[ true "真偽値を返す式" ] whileTrue:
[
    "反復実行する処理"
].
```

`#whileTrue:` セレクターは、条件が真である間反復する事を意味している。逆に条件が偽である間反復する `#whileFalse:` というセレクターも存在する。

また `do`-`while` に該当する文も存在する。`do`-`while` に該当する反復は、ブロックに対するメッセージ送信の形で次の様に記述する。

``` smalltalk
[
    "反復実行する処理"
    "このブロックの実行結果が真である間反復を繰り返す"
] whileTrue.
```

では条件なしの反復も存在する。無条件反復は、ブロックに対するメッセージ送信の形で次の様に記述する。

``` smalltalk
[
    "反復実行する処理"
] repeat.
```

では、反復方法が複数存在するが、実は全てメソッドの再帰呼び出しによって実装されているという事になっている。ただし、こちらも `#ifTrue:ifFalse` 同様実際にメソッドの再帰呼び出しとして実行されていない事が多い。

##### 反復からの脱出

C言語の `break` や  の `last` に相当する反復脱出は `thisContext` に対し `#return` セレクターを使ったメッセージを送る。

``` smalltalk
[
    thisContext return. "反復を抜ける"
] repeat.
```

`thisContext` には、引き数を取り、引き数を脱出するブロックの戻り値として返す `#return:` セレクターや、戻り先のメソッドを指定する `#return:to:` セレクターなど多数の `return` 系セレクターに対応するメソッドが定義されており、他の言語には珍しい多様な反復の脱出方法を備えている。

##### 例外処理機構

にも例外処理機構が存在する。こちらも、その他の構文と同じくメッセージ式とブロックによって実現されている。例外処理は次の様に記述する。

``` smalltalk
[
    [
        Exception signal: '処理失敗'. "例外発生"
    ]
        ensure:
        [
            "例外の有無に関わらず実行したい処理"
        ].
]
    on: Exception "補足する例外の種類"
    do:
    [ :exception |
        "例外を補足した際の処理"
    ].
```

なお`#ensure:`は後述の[ブロックによる資源の開放があるため多用されることはない](https://ja.wikipedia.org/wiki/Smalltalk#ブロックによる資源の開放 "wikilink")。

例外の制御はメッセージ送信毎に連結リストとして積み上げられたコンテキスト情報の末端のコンテキスト（メソッドスタック）を表す `thisContext` オブジェクトを操作し、コンテキストを巻き戻す事で実現されている。 複数の例外は、`#on:do:on:do`・・と`on:do:`を繰り返し(処理系が定義している限りの数で)記述して補足する事もできるが、次の様に例外の型を`,`で並べて補足する事も出来る。

``` smalltalk
[
    Notification signal: '接続準備完了'.
]
    on: Error, Notification
    do:
    [ :exception |
        "エラーと通知両方の例外を1度に補足"
    ].
```

なお、では正常な結果を返せないエラー(間違い)と通知両方を合わせたものが例外である。例外は正常な戻り値を返せない場合と割り込みの様に非同期な通知に利用される。

##### 並列処理

では、標準で並列処理が存在する。並列処理は次の様に記述する。

``` smalltalk
| process semaphore |

semaphore := Semaphore new.
process :=
[
    Process yield. "他のProcessに切り替える切り替え点"
    "並列実行される子処理"

    semaphore signal. "親処理への終了通知"
] newProcess.

process resume. "子処理の起動。Blockに対し#forkを送る場合はnewProcessとresumeは省略できる"
"並列実行される親処理"

semaphore wait. "子処理の終了待機"
```

並列処理はスレッドに類似するプロセスという仕組みにより実装されている。プロセスは環境内で構築された並列処理の仕組みであり、グリーンスレッドで実装されている事が多い。このため、プロセスは論理的に非[プリエンプティブなスレッド](https://ja.wikipedia.org/wiki/プリエンプション "wikilink")([グリーンスレッド](https://ja.wikipedia.org/wiki/グリーンスレッド "wikilink"))を前提しており、現在実行している処理を切り替える切り替え点を必要とする。論理的な前提は非プリエンプティブではあるものの、POSIX環境で動作させたGNU Smalltalkの様に実際はプリエンプティブなスレッドで実装されている場合もある。\[25\]プロセスは他のプロセスから割り込みとして任意の例外を投げる機能があり(記述方法は環境によって異なる)、切り替え点はプリエンプティブなスレッドを使う場合でも例外の発生地点として機能する。

#### クラスオブジェクトの登録

は、クラスの定義をメッセージ式による実行環境へのクラスオブジェクトの登録として実現する。他の言語と異なりクラスオブジェクトの登録は単なる定義ではなく実行環境に対する操作である。1度クラスオブジェクトを登録してイメージファイルを保存すると、明示的にクラスオブジェクトを削除しないかぎりはクラスオブジェクトがイメージファイルに残り続ける。 環境に対するクラスオブジェクトの登録は次の様に記述する。

``` smalltalk
"DerivedクラスをSmalltalk環境に登録する例"
Object                      "基底クラスオブジェクト"
    subclass:               #Derived    "Objectクラスの派生として登録するクラスオブジェクト名の指定"
    instanceVariableNames:  'ia ib ic'  "インスタンス(実体)オブジェクトに所属する変数名(インスタンス変数)の指定(空白区切り)"
    classVariableNames:     'ca cb cc'  "クラスオブジェクトと共有する変数名(クラス変数)の指定(空白区切り)"
    poolDictionaries:       'pa pb pc'  "クラスに所属する変数(プール変数)を取り込む辞書の指定(空白区切り)"
    category:               'example'.  "Smalltalk環境上でクラス名を表示する際にクラスが所属する分類の指定"
```

`poolDictionaries` と `category` を除いては、 から派生した言語のクラス定義と概ね同じである。インスタンス変数はインスタンスメソッドのみから参照でき、クラス変数はクラスメソッドとインスタンスメソッドから参照できる。他の言語と異なりインスタンス変数をクラスメソッドから参照することはできない。

におけるクラスの作成は、特殊構文ではなく単なるメッセージ送信である。クラスを登録する際のメッセージは、上記の例のように次のセレクターを使用することが多い。

``` smalltalk
#subclass:instanceVariableNames:classVariableNames:poolDictionaries:category:
```

しかし、クラスの登録はあくまでメッセージであり自由に作れるため、実行環境には大抵その他のメソッドが用意されている。例えば、近代的な  環境の一つ  では、次のセレクターに対応したメソッドが用意されている。

``` smalltalk
#subclass:
#subclass:category:
#subclass:instanceVariableNames:
#subclass:instanceVariableNames:classVariableNames:poolDictionaries:category:
#subclass:uses:
#subclass:uses:instanceVariableNames:classVariableNames:poolDictionaries:category:
#variableByteSubclass:instanceVariableNames:classVariableNames:poolDictionaries:category:
#variableByteSubclass:uses:ginstanceVariableNames:classVariableNames:poolDictionaries:category:
#variableSubclass:instanceVariableNames:classVariableNames:poolDictionaries:category:
#variableSubclass:uses:ginstanceVariableNames:classVariableNames:poolDictionaries:category:
#variableWordSubclass:instanceVariableNames:classVariableNames:poolDictionaries:category:
#variableWordSubclass:uses:ginstanceVariableNames:classVariableNames:poolDictionaries:category:
#weakSubclass:instanceVariableNames:classVariableNames:poolDictionaries:category:
#weakSubclass:uses:ginstanceVariableNames:classVariableNames:poolDictionaries:category:
```

クラスオブジェクトには、クラス変数とは別途、クラスオブジェクトが `Class` クラスから派生したインスタンスとして状態を持つためのインスタンス変数がある。このクラスオブジェクトのインスタンス変数はクラスオブジェクト内だけで共有され、インスタンスオブジェクトからは直接使用できない。

環境に対するクラスオブジェクトのインスタンス変数の登録は次の様に記述する。

``` smalltalk
Derived class instanceVariableNames: 'ia ib ic'. "クラスオブジェクトのインスタンス変数名(空白区切り)"
```

クラスオブジェクトがもつインスタンス変数には変数を登録した基底クラスと派生クラスで別々の変数領域が確保されるという特筆すべき点がある。これを使用して下記の様にクラスに所属するオブジェクトだけを保持する変数としてつかったりする事ができる。

``` smalltalk
Object subclass: #Super.
Super class instanceVariableNames: 'objects'.

Super class methodsFor: 'accessing'
!
objects

    ^ objects ifNil: [ objects := OrderedCollection new ].
!!

Super class methodsFor: 'instance creation'
!
new
    | object |

    object := super new.
    self objects add: object.
    ^ object.
!!

Super subclass: #Derived.

Derived new.
Derived objects size. "-> 1"
Super objects size. "-> 0"
```

#### メソッドの登録

メソッド（処理方法）の登録は、コード文字列を引数として与えたクラスへのメッセージ送信でも行えるが、通常は環境に組み込まれたクラスブラウザ（システムブラウザ）と呼ばれるGUIツールを用いる。

メソッドは、「メッセージパターン」と呼ばれるメッセージ式のメッセージ部分を模した書式に続けて0個以上のメッセージ式を連ねることで記述する。例えば、前出の、レシーバーか引数を比べてより小さな方を返す「`min:`」というメソッドの登録は次のようなものになる。

``` smalltalk
min: anOtherObject
    ^ self < anOtherObject ifTrue: [ self ] ifFalse: [ anOtherObject ].
```

一行目の「`min: anOtherObject`」がメッセージパターンで、メソッド名（セレクター）と仮引数となる擬変数の宣言を兼ねる。念のためここでメソッド名は「min:」、仮引数となる擬変数名は「`anOtherObject`」である。メッセージパターンのあとに処理を続けて書くこともできるが、通常は行を改めて（さらに、ここでは省いたが慣習としてメソッドの説明をするコメントを書き、それに続けて）処理を記述する。

なお、メッセージパターンのみで具体的な処理を記述せずにメソッドを登録した場合を含め、復帰文による明示的な戻り値の指定が無い場合、メソッドは戻り値として常に `self` を返す。したがって  では値を返さないメソッドを書くことはできない。

#### クラスオブジェクト

は、多くの動的型付け言語やの様にクラスがオブジェクトである。このためではインスタンスオブジェクトと同様にクラスオブジェクトを変数に束縛してメッセージを送ることができる。

``` smalltalk
| object |

object := Something new.
object value. "インスタンスオブジェクトにvalueメッセージを送信"
object := Something.
object value. "クラスオブジェクトにvalueメッセージを送信"
```

クラスオブジェクトは、オブジェクトに`class`メッセージを送ることでも取得できる。

``` smalltalk
' ' class. "-> ByteString"
```

#### 復帰文とブロック

のブロックは一種の制御構文であるという性質上、復帰文が他の言語と比べ極めて異質な振る舞いをする。

``` smalltalk
example
    | block |

    block := [ ^ 1 ].
    block value. "ブロックを実行"
    ^ 0.
```

上記のメソッドを登録したオブジェクトに`#example` セレクターを使ったメッセージを送ると結果としては何が返ってくるか。 以外の言語では `0` が返ってくるのが一般的であるが  では `1` が返ってくる。 はブロック内の復帰文からでもメソッド自体を抜けることができるようになっている。この例では、「`block value.`」を評価し、`block` 中の「`^ 1.`」で制御が戻ると `example` 自体も中断して結果を返す。そして `example` は戻り値として `block` が戻した `1` を戻すようになっている。

``` smalltalk
callee: aBlock
    aBlock value.
    ^ 2.
```

``` smalltalk
caller
    | block |

    block := [ ^ 1 ].
    self callee: block.
    ^ 0.
```

上記の様なメソッドをまたいでブロックを評価する場合はどうなるだろうか、この場合も  は `example` の戻り値として `block` の戻り値である1を返す。 はブロック内で復帰文が実行された際、ブロックの生成地点の呼び出し元までコンテキストを巻き戻すようになっている。この特性により  では、`#ifTrue:ifFalse:` セレクターを使った分岐でメソッドを中断したり `#repeat` セレクター等を使った反復処理を復帰文だけで中断する事ができるようになっている。

``` smalltalk
exampleBlock
    ^ [ ^ 1 ].
```

``` smalltalk
callee: aBlock
    aBlock value.
    ^ 2.
```

``` smalltalk
caller
    | block |

    block := self exampleBlock.
    self callee: block.
    ^ 0.
```

ただし、上記の様にブロックを生成したコンテキストと、ブロックを評価する際のコンテキストが枝分かれする様な場合は復帰文を実行する事はできない。この場合は `BlockContext` が例外を出力し処理が停止してしまう。

#### メソッドに対する注釈

メソッドに対する注釈(Pragma)は、メッセージ式だけではどうしても実現が難しい機械語でしか記述できない演算子の実装や主記憶領域の確保、仮想機械外部との入出力等の実現や、特定の目的のメソッドを自動で列挙するといった目的で使用される特殊構文である。いくつかの注釈はSmalltalk環境に組み込まれているが、利用者やライブラリーの提供者が注釈を定義する事も出来る。

メソッドに対する注釈はメソッドの翻訳時に評価されるため、メソッドにしか記述でない。Behaviorの`evaluate:`による評価などメッセージ式をメソッドの外部で評価する場合は、評価対象の式に注釈を含める事はできない。具体的にはSmalltalk環境のWorkspaceに注釈を記述して評価するとエラーとなる。

メソッドに対する注釈は次の様に記述する。

``` smalltalk
< keyword1: arg1 ... keywordN: argN >
```

`<`と`>`で囲まれた範囲は、メッセージ式のメッセージ部分と同じになる。但し引き数を取らない注釈の記述はできない。

次にメソッドに対する注釈の具体例を挙げる。注釈はSmalltalk環境によって異なり、どの環境でも次の注釈が使えるわけでない事に注意すること。

| コード                                                       | 意味                                                        |
| --------------------------------------------------------- | --------------------------------------------------------- |
| `<primitive: 1>`                                          | 数値演算など原子的機能の呼び出し。引き数の値は呼び出す機能の番号。                         |
| `<apicall: int 'GetLastError' () module: 'kernel32.dll'>` | FFIによる外部関数の呼び出し。先頭のapicallは呼び出し規約であり注釈の名前ではない。cdeclなどもある。 |

#### 大域変数

Smaltallkでは、Smalltalk環境全体で参照できる大域変数を作成する事が出来る。大域変数は同じく大域変数であるSmalltalk変数に格納された`SmalltalkImage`のインスタンスオブジェクトにメッセージを送って作成する。また、大域変数の削除も`SmalltalkImage`のインスタンスオブジェクトに対するメッセージ送信となっている。

``` smalltalk
Smalltalk at: #GlobalVariable put: 100.
GlobalVariable. "->100"

globalVariable := 10.
Smalltalk at: #GlobalVariable. "->10"

Smalltalk removeAt: #GlobalVariable.
GlobalVariable. "->nil"
```

`SmalltalkImage`は一種の連想配列であり、Smalltalkの大域変数は、Smalltalk変数を介す事で連想配列として操作する事が出来るようになっている。 なお、Smalltalkのクラス名と大域変数は同じものであり、クラス名にオブジェクトを代入すれば、そのクラスを破壊してしまうことが出来る。また、Smalltalkオブジェクトが格納されたSmalltlak変数もオブジェクトを代入し破壊する事が出来る。このように大域変数を代入により破壊してしまった場合は、最悪Smalltalk環境が起動しなくなる事態に陥り非常に危険である。このためSmalltalkではよほどの理由がなければ大域変数を使うべきではない。

#### プール辞書

プール辞書は、クラスの変数として連想配列または、他のクラスオブジェクトのクラス変数を取り込むという機能である。取り込む連想配列の要素やクラスオブジェクトのクラス変数はプール変数と呼ばれる。連想配列やクラスオブジェクトは大域変数でなくてはならない。

``` smalltalk
"プール辞書で使用する連想配列の登録"
Smalltalk at: #UserPoolA put: Dictionary new.
UserPoolA at: #ExamplePoolValueA put: 1.

"プール辞書で使用するクラスオブジェクトの登録"
Object
    subclass:       #UserPoolB
    instanceVariableNames:  ''
    classVariableNames: 'ExamplePoolValueB'
    poolDictionaries:   ''
    category:       'example'.

"UserPoolAとUserPoolBをプール変数として利用するクラスオブジェクト"
Object
    subclass:       #Someone
    instanceVariableNames:  ''
    classVariableNames: ''
    poolDictionaries:   'UserPoolA UserPoolB'   "UserPoolAとUserPoolBを辞書に記述しプール変数を取り込む"
    category:       'example'.

Someone methodsFor: 'accessing'
!
valueA
    ^ ExamplePoolValueA. "UserPoolAのExamplePoolValueAを参照"
!
valueB

    ^ ExamplePoolValueB. "UserPoolBのExamplePoolValueBを参照"
!!
```

プール辞書には複数の連想配列やクラスオブジェクトを指定できるが、プール変数が重複した場合は、先に指定した連想配列やクラスオブジェクトのプール変数が使われる。

### 準標準的な文法

#### 非定数要素配列

Pharo, GNU Smalltalkといった近代の環境では、定数以外に式の結果を指定可能な非定数要素の配列定数を使用できる。配列の要素は空白ではなく`.`で区切る。

``` smalltalk
array := { 1. 1 + 1 }. "1と2を要素に持つ配列を作る。"
```

#### 継続

継続渡し形式を支援する機能として継続があり、PharoやGNU Smalltalkで使用できる。もっぱら反復の中断や、メソッド内の処理を飛ばすために使われる。継続の使用は次の様に記述する。

``` smalltalk
result := Continuation currentDo:
[ :break |

    aCondition1 ifTrue: [ break value: 1 ]. "aCondition1がtrueなら以降の処理を中断しresultに1を代入する。"
    aCondition2 ifTrue: [ break value: 2 ]. "aCondition2がtrueなら以降の処理を中断しresultに2を代入する。"

    3 "aCondition1, aCondition2両方trueならresultに3を代入する。"
].
```

#### 生成器

遅延評価を支援する機能として生成器があり、PharoやGNU Smalltalkで使用できる。生成器はCoroutineにも利用できる。生成器の使用は次の様に記述する。

``` smalltalk
stream := Generator on:
[ :each |
    each yield: 1.
    each yield: 2. "stream nextを1回呼ぶまで実行しない。"
    each yield: 3. "stream nextを2回呼ぶまで実行しない。"
].

stream next. "-> 1"
stream next. "-> 2"
stream next. "-> 3"
```

生成器を使って処理を作ることは多くないが、配列などを使用する際、間接的に使用していることが多い。

``` smalltalk
| readStream grater2 total |

readStream := #( 1 2 3 4 5 ) readStream. "#readStreamにより#select:を遅延実行する生成器が作られる。"
grater2 := ( ( readStream select: [ :each | 1 < each ] ) collect: [ :each | each * 2 ] ) reject: [ :each | 8 > each ].
total := grater2 inject: 0 into: [ :value :each | value + total ]. "#inject:into:でeachに代入するとき初めて#select:と#collect:と#reject:が実行される。"
```

### ファイル用構文

のプログラムは基本的に中間言語としてイメージファイルの中に格納され、ソースコードの編集は  のGUI環境から行われる。このため基本的にファイルという形で  のソースコードやプログラムを目にすることはない。しかし、ソースコードの交換目的などでどうしても  環境外でソースコードを管理する必要がある場合に備えファイル用の構文が存在する。ファイル用の構文は次のようになる。

``` smalltalk
Object
    subclass:       #Example
    instanceVariableNames:  ''
    classVariableNames: ''
    poolDictionaries:   ''
    category:       'example'.

Example methodsFor: 'Instance Methods A'
!
selectorA1
    "処理"
    ^ 0.
!
selectorA2: anArgument
    "処理"
    ^ 0.
!!

Example methodsFor: 'Instance Methods B'
!
selectorB1
    "処理"
    ^ 0.
!
selectorB2: anArgument
    "処理"
    ^ 0.
!!

Example class methodsFor: 'Class Methods'
!
selector1
    "処理"
    ^ 0.
!
selector2: anArgument
    "処理"
    ^ 0.
!!
```

本来他の言語の様なブロックが存在しないため、ブロックとして「`!`」が使用される。クラスの登録は「`!`」の一組で囲まれる。メソッドはプロトコル毎に「`クラス名 methodsFor: 'プロトコル' ! 〜 !!`」というブロックで囲まれる。一つのプロトコルには複数のメソッドを定義でき、メソッド同士は一個の「`!`」によって区切られる。

ちなみに、クラス登録は単なるメッセージ送信であり特別な文ではないため、登録用ブロック外にも次のように単純なメッセージ送信の記述に使用する事が出来る。

``` smalltalk
Example methodsFor: 'Instance Methods A'
!
selector1
!!

'hello' displayNl.
'world' displayNl.

Example2 methodsFor: 'Instance Methods A'
!
selector
!!
```

ファイル用構文で記述されたメソッドの登録は、可読性や記述性の面からメッセージ式からかけ離れた変則的な構文が使用される。しかし、この変則的な構文を用いなければメソッドを登録できないわけではなく、次のように通常のメッセージ式でメソッドを登録する事も出来る。

``` smalltalk
Example
    compile:
        '
        selectorC: anArgument
            ^ 0.
        '
    classified: 'Instance Methods C'.
```

上記では、クラスオブジェクト`Example`のプロトコル`Instance Methods C`に対し、メソッド`selectorC`を登録している。

### 委譲と継承

において、継承とは特殊な委譲に過ぎない。

``` smalltalk
Object
    subclass:       #Derived    "DerivedはObjectクラスから派生させる"
    instanceVariableNames:  ''      "オブジェクトに所属する変数は定義しない"
    classVariableNames: ''      "クラスオブジェクトと共有する変数は定義しない"
    poolDictionaries:   ''      "クラスに所属する変数は定義しない"
    category:       'example'.  "クラスの分類はexampleとする(今回の名前に意味はない)"
```

このため、例えば上記のクラスオブジェクトの生成では、`Derived` クラスオブジェクトの基底クラスオブジェクトとして `Object` を指定しているが、処理系によっては下記の様に `#superclass:` メッセージを送る事で、基底クラスに別のクラスオブジェクトを指定する事が出来る。

``` smalltalk
"superclass: NewBase. メッセージを送り基底クラスを NewBase に変更する事が出来る。"
Derived superclass: NewBase.
```

処理系により不可能な事もあるがクラスオブジェクトだけでなく、インスタンスオブジェクトから派生することも出来る。

``` smalltalk
"インスタンスオブジェクトの nil から派生した Derived クラスを Smalltalk 環境に登録する"
nil
    subclass:       #Derived
    instanceVariableNames:  ''
    classVariableNames: ''
    poolDictionaries:   ''
    category:       'example'.
```

なお通常、派生元の基本となるProtoObjectやObjectはnilから派生しており継承関係は再帰的に循環している。

### メッセージ

において、メッセージ、セレクター、メソッドはそれぞれ別物である。 系統の言語の様にオブジェクトに対しメッセージを送るという事は単なる比喩ではない。

あるオブジェクトに対し `#hello` というセレクターを使ったメッセージを送る事を考える。この時、 においては `hello` というメソッドが必ず呼ばれる保証はない。例えば「hello」メッセージを受け取るオブジェクトが `hello` メソッドを実装していなければレシーバーに指定されたオブジェクトの `doesNotUnderstand:` メソッドが呼ばれる事になる。

なお、多くの  の処理系では `doesNotUnderstand:` の引き数で得られたメッセージを返すだけのクラスが用意されている。例えば  環境のひとつである  ではメッセージ作成用クラス `MessageCatcher` が用意されており\[26\]次のようにメッセージを拾い、他のオブジェクトに渡すことが出来る。

``` smalltalk
message := MessageCatcher new show: 'text'. "「show: 'text'」がmessageに代入される。"
message sendTo: Transcript. "「Transcript show: 'text'」が実行される。"
```

また、セレクターとメソッドが独立していることを利用して一つのメソッドを複数のセレクターに結びつける事もできる。

``` smalltalk
"#onClick:を使ったメッセージをopen:メソッドに転送させる。"
FileEventHandler
    addSelector:    #onClick:
    withMethod: FileEventHandler >> #open:.
```

メッセージにはセレクターと引き数が含まれている。このため受け取ったセレクターと引き数を編集する事も出来る。

``` smalltalk
message := MessageCatcher
    new
        bold: true
        text: 'example'.

message selector keywords keysAndValuesDo:
[ :key :each |
        Transcript
                show: each, ':=', ( message arguments at: key ) printString;
                cr.
].
"
以下が出力される。

bold:=true
text:=example
"
```

#### 型付け

プログラミング言語一般の概念として型検査をソースコードの翻訳時に実行するか、実行時に実行するかにより[静的型付けと](https://ja.wikipedia.org/wiki/型システム "wikilink")[動的型付けという区分が存在するが](https://ja.wikipedia.org/wiki/型システム "wikilink")、は、そのどちらでもなく型なし言語（）に区分される\[27\]。 の場合、変数に対する操作は全てメッセージ送信であり、変数の種類(型)毎にできる操作は決まっていない。また、オブジェクトに対しメッセージを送った場合、そのオブジェクトがメッセージに対応するメソッドを持っていなくとも実行環境がエラーを発生させる事はない。メッセージに対応するメソッドが存在しない場合、例外を出すか無視するかは、クラスに実装されたメソッドの内容次第である。したがって  には型付けの概念はない。例えば、 の `MessageCatcher` は全てのメッセージを拾うため、どんなメッセージを与えられても例外が発生することはない。また、GNU Smalltalkではnilから派生したクラスのオブジェクトに存在しないメソッドに対するメッセージを送ると何も反応しない。ただし高速化のため後述の特殊セレクターを使用した場合実行時に型検査する処理系が多い。ちなみに  は基本的に中間言語に翻訳され、翻訳時にエラーを発生させるため構文検査は静的である。

#### メッセージと制御構文

制御構文の節で述べた通り、の殆どの制御構文はメッセージ式である。に明るくないプログラマーからは言い方や見方を変えただけと捉えられがちである。の制御構文は実際にメッセージであるがゆえに究極には制御構文の構文要素を次のように変数に分解してしまうことが出来る。

変数に分解した分岐制御の例：

``` smalltalk
| then else message condition |

then := [ 1 ].
else := [ 2 ].

message := MessageCatcher
    new
        ifTrue:  then
        ifFalse: else.

condition := 2 = 2.
^ message sendTo: condition.
```

これらの変数に分解された構文要素は、どのクラスのオブジェクトで無いといけないという制限はない。送られたメッセージを処理することさえ出来ればあらゆるオブジェクトに置き換える事が出来る。

#### 特殊セレクター

Smalltalkでは高速化のためいくつかのメッセージを特別扱いする。これを特殊セレクター（）という。 典型的な例は`#ifTrue:ifFalse:`である。下記のコードはでは「ifTrue: \[5\] ifFalse: \[6\]」を評価した時にメッセージが送られる訳ではなく、バイトコードレベルでインライン展開され飛越し命令の表現に置き換えられる。このため実際に`ifTrue:ifFalse:` という名のメソッドが呼ばれることもない。また、trueやfalse以外に上記のようなBoolean用のメッセージを送ると処理系によってはMustBeBoolean例外を発生させる。このように頻繁に使用する分岐や反復を特別扱いすることで性能低下を防いでいる。

``` smalltalk
3 < 4 ifTrue: [ 5 ] ifFalse: [ 6 ].
```

セレクターと名がつくが特殊セレクターは、特別扱いする条件が引数の状態を含んでおり、たとえ同じセレクターを使ったメッセージでも引数が条件に一致しなければ特別扱いしない。例えば下記のように引数に直接ブロックを指定していない場合では多くの処理系(VisualWorks, GNU Smalltalk等)は特別扱いせずメッセージ送信を実行する。

``` smalltalk
| then else |
then := [ 5 ].
else := [ 6 ].
true ifTrue: then ifFalse: else.
```

特殊セレクターはあくまで高速化の手段であるため種類は処理系によって異る。どの処理系が何を特殊セレクターとして扱うかは処理系ごとに提供される説明資料に記述されている。\[28\]\[29\]

### クラスオブジェクトとMetaclass

クラスオブジェクトもオブジェクトであるため、所属するクラスが存在している。クラスオブジェクトが所属するクラスは`Metaclass`というクラスのインスタンスオブジェクトである。

``` smalltalk
ByteString.                   "-> ByteString"
ByteString class.             "-> ByteString class"
ByteString class class.       "-> Metaclass"
```

`Metaclass`も当然ながらクラスに所属しており、再帰的に`Metaclass`に属するようになっている。

``` smalltalk
' ' class.                               "-> ByteString"
' ' class class.                         "-> ByteString class"
' ' class class class.                   "-> Metaclass"
' ' class class class class.             "-> Metaclass class"
' ' class class class class class.       "-> Metaclass"
' ' class class class class class class. "-> Metaclass class"
```

クラスオブジェクトが所属する`Metaclass`のインスタンスオブジェクトは特殊なオブジェクトであり、クラスの継承階層と同様に継承階層を持っている。

``` smalltalk
Collection  class superclass. "-> Object class"
Object      class superclass. "-> ProtoObject class"
ProtoObject class superclass. "-> Class"
```

クラスオブジェクトはMetaclassから生成された単なるオブジェクトで有ることから、Smalltalkが標準で提供するクラスオブジェクトとは異なる独自の構造をもったクラスオブジェクトを作ることができる。

例えば以下のようにメソッドの変わりにブロックを持つ無名クラスを作成することも出来る。

``` smalltalk
| class object |

"Metaclassからクラスオブジェクトを生成"
class :=
    Class
        new
            superclass: Object;
            methodDictionary: MethodDictionary new.

"生成したクラスオブジェクトのセレクターにメソッドではなくブロックを紐付け"
class
    methodDictionary
        add:    #something1: -> [ :value | value ] block;
        add:    #something2 -> [ 2 ] block.

"生成したクラスオブジェクトをインスタンスオブジェクトの生成に使用"
object := class new.

Transcript
    show: ( object something1: 1 ) printString;
    nl.

"生成したクラスオブジェクトを基底クラスとして使用"
class
    subclass:       #Example
    instanceVariableNames:  ''
    classVariableNames: ''
    poolDictionaries:   ''
    category:       ''.
```

### 定数とオブジェクト

文法の節で述べた通りでは定数も全てオブジェクトである。どんな定数であれ`#class`や`#inspect`といった基本的なセレクターを使ったメッセージを受け取ることが出来るため、基本的な操作であれば定数と他のオブジェクトを区別する必要はない。

``` smalltalk
| showClass |

showClass :=
[ :object |
    Transcript
        show: object class name;
        cr.
].

showClass
    value: Object new; "-> Object"
    value: Object;     "-> Object class"
    value: nil;        "-> UndefinedObject"
    value: 0;          "-> SmallInteger"
    value: 0.0;        "-> Float"
    value: 0.0e1;      "-> Float"
    value: $0;         "-> Character"
    value: '';         "-> ByteString"
    value: #a;         "-> ByteSymbol"
    value: #'a';       "-> ByteSymbol"
    value: #();        "-> Array"
    value: [].         "-> BlockClosure"
```

### 可変長オブジェクト

は、任意の広さで確保した領域を持つ可変長オブジェクトを作ることが出来る。には配列を表わすためArray等が存在するが、これらのクラスオブジェクトは可変長オブジェクトを使って構築されている。可変長オブジェクトの領域は、オブジェクトの生成したときの一度だけしか広さを指定できない。また、クラスオブジェクトの登録時に`variable〜`で始まるセレクターを使っている必要がある。

``` smalltalk
Object
    variableSubclass:   #ExampleArray
    instanceVariableNames:  ''
    classVariableNames: ''
    poolDictionaries:   ''
    category:       'example'.

| array |

array := ExampleArray new: 100. "要素100個分の領域を確保した可変長オブジェクトを生成する。"
array at: 1 put: 0.     "1番目の要素に0を入れる。"
array at: 1.            "1番目の要素を取り出す。"
```

### 記憶領域の管理

は、ハンドルとごみ回収機能([ガーベッジコレクター](https://ja.wikipedia.org/wiki/ガベージコレクタ "wikilink"))の全面的な導入によりハンドルテーブルの書き換えを利用した特殊な制御を提供している。\[30\]

#### ハンドルテーブルの書き換え\[31\]

ハンドルが参照している記憶領域上のテーブルを書き換えることによりは、あるオブジェクトを参照している全ハンドルの参照先を一気に変更することができる。ハンドルテーブルの書き換えには`#become:`を用いる。ただし、数字や文字列といった定数オブジェクトは置き換えることはできず、定数を置き換える際は定数を保持しているオブジェクトを置き換える必要がある。

``` smalltalk
| value1 value2 |

value1 := 'hello' asValue.
value2 := value1. "この時点ではvalue2はValueHolder('hello')"
value1 become: 'こんにちは' asValue. "この時点でvalue2はValueHolder('こんにちは')になる"
```

`#become:`を使っている良い例はクラスオブジェクトの再登録である。Smalltalkではクラスオブジェクトはインスタンスオブジェクトが生きている間でも再登録可能でなければならず、インスタンスオブジェクトを生きたままクラスオブジェクトを再登録するために使われている。

#### 弱参照

弱参照は[参照カウント](https://ja.wikipedia.org/wiki/参照カウント "wikilink")方式を使う言語でよくライブラリーとして実装されるがではハンドルの制御を用いた言語機能として用意されており相互参照しているが不要になっているオブジェクトを迅速に解放するために使われている。弱参照には`#makeWeak`を用い、`#makeWeak`を受け取ったオブジェクトは弱参照となる。

``` smalltalk
| holder object |
holder := ValueHolder new.
holder makeWeak. "holderが弱参照になる。"
object := Object new.
holder value: object.
ObjectMemory compact. "ごみ回収。この時点ではholder valueはnilではない。"
object := nil.
ObjectMemory compact. "ごみ回収。この時点でholder valueはnilとなる。"
```

#### カゲロウ(蜉蝣)

カゲロウ()は、どこからも参照されなくなった連想配列の要素を解放するために導入された記憶領域の管理機構でありSmalltalkで初めて実装された。例えば連想配列の添字として\#keyがあったとして、\#keyが連想配列以外の変数で参照されていなければ連想配列の要素は必要ない。このように不要となった要素を解放するために用いる。オブジェクトをカゲロウ状態にするには`#makeEphemeron`を用いる。

``` smalltalk
| association key |
key := Object new.
association :=
    Association
        key: key
        value: Object new.
association makeEphemeron. "associationがカゲロウになる。"
ObjectMemory compact. "ごみ回収。この時点ではassociation keyとassociation valueは共にnilではない。"
key := nil.
ObjectMemory compact. "ごみ回収。この時点ではassociation keyとassociation valueは共にnilとなる。"
```

ここでは連想配列の要素としてよく使われるAssociationを例としているが、カゲロウが消滅する基準は最初のインスタンス変数でクラスに依存しないためどんなクラスでもカゲロウにすることができる。

###  の慣習

#### 大文字からはじめる識別子と小文字からはじめる識別子

##### 変数名

変数を表す識別子については、1文字目に大文字と小文字のどちらを使うか、大域変数か否かを基準にして決めることが慣習になっている。 環境自体も大文字小文字の使い分けを認識しておりメソッドを翻訳する際小文字の変数は局所変数かメンバーとして定義していないと、警告が発生したり翻訳失敗になる。

|               |           |
| ------------- | --------- |
| 大域変数          | 大文字からはじめる |
| 大域変数以外(局所変数等) | 小文字からはじめる |

クラス名が大文字から始まるのは、クラス名が大域変数だからである。

よく使われるクラス以外の大域変数:

  - Smalltalk
  - Processor
  - Transcript

##### セレクター

セレクターを表す識別子については、基本的に1文字目に小文字を使うが、メソッドが存在するセレクターを避けたい場合は大文字を使う事が慣習になっている。 GNU SmalltakやVisualWorksで用意されている名前空間は、大文字のセレクターを使う典型的な例である。

``` smalltalk
Smalltalk SystemExceptions InvalidValue signalOn: 0. "「Smalltalk」以外は全てセレクター"
```

なお、名前空間が使える環境の多くは、翻訳時に名前空間の名前解決できる「.」区切りの拡張構文が用意されており、実際にはこちらの構文が使われることが多いため、セレクターを使った名前空間の指定を見る機会は少ない。

#### オブジェクトの生成と初期化

オブジェクトの生成には `#new` セレクターを使ったメッセージを使う。他の言語と違い、`new` は演算子ではない。

``` smalltalk
|object|

object := Example new. "Exampleクラスオブジェクトに「new」メッセージを送りオブジェクトを生成。"
```

ではクラスオブジェクトのメソッドもインスタンスオブジェクトのメソッドと同様に派生クラスによる再定義が可能である。このため `new` メソッドを再定義し初期化処理を記載する事が出来る。`new` メソッドを再定義してしまうとオブジェクトの生成自体が不可能になるように思われるが、本来 `new` メソッドは `#basicNew` セレクターを使ったメッセージを`Behavior` に送ってオブジェクトを生成しているためオブジェクトの生成手段がなくなるわけではない。このため `new` メソッドを再定義しても 「basicNew」メッセージを`Behavior`に送ることでインスタンスオブジェクト生成することが出来る。

ただし、実際の初期化に `new` メソッドが使われる事は多くない。実際には慣習としてクラスの作者が新たに登録した**インスタンス・クリエイション**と呼ばれる `new` とは別の初期化用メソッドが使用される。インスタンス・クリエイションは一般的なクラスオブジェクトのメソッドであり、そのメソッドの内部で 「`new`」メッセージやその他のインスタンス・クリエイションを使って初期化済みのオブジェクトを生成する役割を持っているだけで基本的にその他のメソッドと変わらない。一般的に`instance creation`というプロトコルに登録される。

``` smalltalk
| number |

number := Number readFrom: '10'. "readFrom:がインスタンス・クリエイション".
```

では1個のセレクターに対し1個のオブジェクトから複数のメソッドを関連付けられない\[32\]ため 「`new`」メッセージの送信によりできる初期化は1個のオブジェクトにつき一通りの初期化だけである。このため複数のインスタンス・クリエイションを用意することで用途に応じた複数の初期化方法を提供しているのである。インスタンス・クリエイションは一般的なメソッドのひとつでしかない。このためインスタンス・クリエイション持つクラスオブジェクトは[アブストラクト・ファクトリーとして機能する](https://ja.wikipedia.org/wiki/Abstract_Factory_パターン "wikilink")。

具体的には次のように使われる。

``` smalltalk
defaultDatabase
    "既定のデータベースのクラスオブジェクトを定義した派生クラスで再定義可能なメソッド。
     オーバーライドされた際は、必ずしもクラスオブジェクトが返されるとは限らず、インスタンス
     オブジェクトが返される場合もある。"
    ^ PostgreSQL.
```

``` smalltalk
database
    "databaseへの接続を返すメソッド。
     defaultDatabaseにより返されたPostgreSQLに対し、インスタンス・クリエイションである
     #connect:セレクターを使ったメッセージが送られ、PostgreSQLのインスタンスオブジェクトが生成される。
     ただし、defaultDatabaseは、派生クラスによって再定義できるため、#connect:セレクターを使ったメッセージが
     必ずしもPostgreSQLクラスオブジェクトに送られるとは限らない。"
    ^ self defaultDatabase connect: self configuration.
```

また、 はクラスメソッドを上書きできるため、インスタンス・クリエイションを次の様に実装する事で基本的な初期化処理を派生元のクラスに任せることができる。

``` smalltalk
x: aX y: aY
    ^ self new
        x: aX;
        y: aY.
```

上記は、2次元座標用のクラスオブジェクトのインスタンスオブジェクトを初期化する派生元のクラスオブジェクトに実装されたインスタンス・クリエイションである。このクラスオブジェクトを継承した2次元座標用のクラスオブジェクトでは`#x:y:`セレクターを使ったメッセージに対応するメソッドを実装する必要はない。インスタンス・クリエイションを利用したパターンは  では広く利用され、いたる所で見ることが出来る。

#### アクセッサー

では、単一の値を出し入れするメッセージの事を特にアクセッサ―\[33\]と呼ぶ。引き数の有無により値の入出の方向を区別する。

例：

| コード                 | 意味             |
| ------------------- | -------------- |
| `object value.`     | オブジェクトから値を取得する |
| `object value: 10.` | オブジェクトに値を渡す    |

においてアクセッサーはその他のメソッドと役割に違いはなく特別な意味を持たないが、プロトコルとして明示的に として登録される点が特徴的である。

においてアクセッサーはインスタンス変数の出し入れや、クラス変数の単純な出し入れに使用される事は多くない。 においてアクセッサーは次の用途でよく使われる。

| 目的                          | 詳細                                                                                                                                                              |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| nowrap|インスタンス変数やクラス変数の初期化   | インスタンス変数やクラス変数からの値の取得時にインスタンス変数やクラス変数が `nil` であればそれらの変数を初期化する。                                                                                                  |
| nowrap|使用するクラス・オブジェクトの抽象化   | クラス・オブジェクトあるいはファクトリーオブジェクトを取得できるアクセッサ―を用意し、アクセッサ―を派生クラスでオーバーライドする事で派生クラスからオブジェクトの生成に使うクラス・オブジェクトを自由に切り替えられるようにする。                                               |
| nowrap|保管場所の抽象化             | オブジェクトが、インスタンス・クラス・プールのどこで管理されているかを抽象化する意味がある。例えばクラス変数やプール辞書の操作では、クラス変数やプール辞書の操作目的であってもインスタンスオブジェクトのメソッドとしてアクセッサーを用意する。                                         |
| nowrap|インスタンス変数やクラス変数に対する委譲 | インスタンス変数やクラス変数に対しメッセージを送るアクセッサ―を定義し、複数の箇所でインスタンス変数やクラス変数に対する同じメッセージ送信をしないようにする。これにより`self object value value: 1.`というような複雑なメッセージを`self value: 1.`というメッセージに単純化する。 |

#### 定数

定数は、単に定数を返すアクセッサ―で定義する。C言語の影響を受けた言語のように定数を\#defineや変数で定義するという慣習はない。

#### 附帯情報

では、非常に利用頻度の低いインスタンス変数やクラス変数を管理する方法として附帯情報（）というパターンが使用される。附帯情報はインスタンス変数やクラス変数などの内部変数の代わりに連想配列によりオブジェクトを保持する仕組みである。

附帯情報の使用例：

``` smalltalk
Tag methodsFor: 'accessing'
!
id
    ^ self valueOfProperty: #id.
!
id: aString
    self setProperty: #id toValue: aString.
!!
```

附帯情報が有効な身近な例としては[XMLや](https://ja.wikipedia.org/wiki/Extensible_Markup_Language "wikilink")[HTMLのタグ属性が挙げられる](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink")。例えばHTMLの `id` 属性や `onClick` といったイベント属性は、必ずしも全てのタグで使用されることはない。特にイベント属性については一つのHTML上に一切記述されない事もよくある。この様な使用頻度の低い属性のためにオブジェクトに一個一個変数を定義するのは記憶領域の無駄である。ましてや `onClick`、`onMouseDown`、`onMouseUp`等大量に属性があればこの無駄は馬鹿にならない。この様な無駄を省くために  では附帯情報というパターンがよく使用される。

全てのインスタンス変数やクラス変数は原理的に全て附帯情報によって表現することが出来る。この点に着目しオブジェクトに所属する変数を全て附帯情報に置き換えた言語が後の  であり、 である。これらの言語でオブジェクトに所属する変数をプロパティーと表現するのは、この  における附帯情報(プロパティー)に由来するもので、附帯情報の仕組みの有無に関わらずインスタンス変数やクラス変数をプロパティーと表現するのは間違いである。

附帯情報は  や  においては当たり前の様に使用されている。しかし、 においては附帯情報を多用する事はデバックを著しく困難にするため不適切な作法とされており、HTMLの属性の様に本当に使用頻度の低い変数だけを附帯情報で扱い、常用する変数に附帯情報を乱用すべきではないと言われている。例えば変数は統合開発環境の機能で使用箇所を把握できるが附帯情報では使用箇所をアクセッサーに限定しない限り追跡不可能になる。また、附帯情報では変数の変化に反応するブレークポイントを仕掛けることも難しい。\[34\]

#### 単純な例外処理

以外の言語において、配列の範囲外にある配列要素の操作や、値の代入されていない連想配列の操作は、次の例のように操作の前に一旦判定を行なって例外処理するか、例外機構を利用する方法が一般的である。

``` smalltalk
| key |
key := #phoneNumber.
( map contain: key ) ifTrue: [ ^ map at: key ] ifFalse: [ ^ nil ].
```

一方  では、配列の範囲外操作の様に単純で頻発するような処理では、次のように予めメッセージに例外処理をブロックとして渡してしまう方法が一般的である。

``` smalltalk
"#phoneNumber に対応する値が無ければ常に nil を返す。map 自身に #phoneNumber が追加される事はない。"
^ map at:#phoneNumber ifAbsent: [ ^ nil ].
```

予め例外処理をメッセージに含めることで、単純な例外処理をより簡潔なものとしている。

この方法は、 独自の復帰文と組み合わせる事でより柔軟な制御をする事ができる。

次の処理は、連想配列に値が見つかればそれを表示し、値が無ければ何もしないという処理であるが、処理の中断の判定と連想配列からの値の取り出しを一度のメッセージ送信だけで実現している。

``` smalltalk
| value |

value := map at:#phoneNumber ifAbsent: [ ^ self ].
Transcript
    show: value;
    cr.
```

#### ブロックによる資源の開放

では、ブロック内だけ資源を確保しブロックの終了後に資源を開放するというブロックによる資源の開放が行われる。ブロックによる資源の開放では、資源の確保と同時に資源の開放を強制できるため開放忘れや例外による開放漏れを防ぐことができる。の`using`に類似するが、`using`を書き忘れたまま`new`できない分さらに強力である。

``` smalltalk
"Pharo"
'example.txt' asFileReference writeStreamDo: "example.txtを開く"
[ :writeStream |

    writeStream nextPutAll: 'text'.

]. "example.txtを閉じる(例外発生時も閉じる)"
```

``` smalltalk
"GNU Smalltalk"
'example.txt' asFile withWriteStreamDo: "example.txtを開く"
[ :writeStream |

    writeStream nextPutAll: 'text'.

]. "example.txtを閉じる(例外発生時も閉じる)"
```

#### 要素の列挙

は反復処理のための基本構文を備えているが、ある値の生成器（入出力等）やある集合要素から要素を取得するときに基本的な反復構文を使う事は稀である。 では、値を列挙するために値の生成器や集合要素に送るべきメッセージが概ね決まっており、値を取り出す際は極力、列挙メッセージ（）を使用する事が作法となっている。

次に列挙メッセージの送信例を示す。

配列に対する列挙メッセージの例：

``` smalltalk
#( 4 3 2 1 0 ) do:
[ :each |
    "配列の要素が1個ずつ each に代入され表示領域（Transcript）に表示される"
    Transcript
        show: each;
        cr.
].
```

実行結果:

``` smalltalk
4
3
2
1
0
```

数値に対する列挙メッセージの例：

``` smalltalk
( 0 to: 4 ) do:
[ :each |
    "配列の要素が1個ずつ each に代入され表示領域（Transcript）に表示される"
    Transcript
        show: each;
        cr.
].
```

実行結果:

``` smalltalk
0
1
2
3
4
```

列挙メッセージで使えるセレクターは `#do:` の様に全ての要素にブロックを適用するだけの単純なセレクターだけでなく、現在の集合要素の要素を操作した上で新しい集合要素を作成する `#collect:` や、集合要素から条件に一致する要素だけを抜き出し、新しい集合要素を作り出す `#select:`、集合要素の中から特定の要素を見つけ出す `#detect:ifNone:` など様々なセレクターがある。処理系によっては `#groupBy:having:` などSQLに類似したセレクターに対応するメソッドを多数用意しているものもある。 では集合要素や値の生成器自体にこれらのメッセージを受け取れるよう実装する事で、集合要素のデータ構造や、生成器の入力元などの構造に依存せず最適な反復処理を実現できるようになっている。これらの列挙機能は近年の言語において `foreach` や`yeild`、LINQ等言語機能として賄われつつあるが  においては、単にライブラリーの慣習として実現されている所が特徴的である。

#### オブジェクトの変換

Smalltalkでは一般的にオブジェクトに`#as〜`というセレクターを使ったメッセージが送られた場合、オブジェクトを別のクラスのオブジェクトに変換する。例えば次の様な変換がある。

Stringの変換による具体例(変換結果は処理系依存)：

``` smalltalk
'abcd' asSymbol.　　　　　　"→Symbolクラスのオブジェクト"
'10' asInteger.　　　　　　 "→SignedIntegerクラスのオブジェクト"
'10:00' asTime.　　　　　　 "→Timeクラスのオブジェクト"

"以下は処理系によっては存在しない"
'/home' asPath.　　　　　　 "→AbsolutePathクラスのオブジェクト"
'http://example.com' asUrl. "→Urlクラスのオブジェクト"
```

オブジェクトを別のオブジェクトに変換するメソッドやメンバー関数が用意されている事は、Smalltalkに限らず他の言語でも一般的であり珍しい事ではない。Smalltalkの慣習として特徴的なところは、既存のクラスにこのオブジェクトの変換をユーザーやライブラリーの作者が自由に組み込んでいる所である。例えばSmalltalkの処理系であるPharoでは、初期状態で基本的なクラスであるStringに54個もの`as〜`で始まるメソッドが定義されている。この大量の変換メソッドは、メソッド追加した際すぐに影響を判断できるためメソッド追加に対し寛容的なSmalltalk独特の空気を象徴している。しかし、既存のクラスにメソッドを追加すればライブラリーを併合した際、意図しない衝突を生むため多用は避けるべきであるとの意見も存在する。\[35\]

オブジェクトの変換はただオブジェクトの内部表現の変換だけでなく情報の加工にも使われる。

オブジェクト変換による具体例：

``` smalltalk
#( 2 1 2 3 1 3 ) asSortedCollection asSet. "-> #( 1 2 3 )"
```

#### セレクターとオブジェクトを指定したイベント処理

イベントハンドラーを定義する方法として、では次のようにセレクターと、レシーバーとなるオブジェクトを指定する方法が一般的である。

``` smalltalk
| view controller |
view := Morph new.
controller := FileControlHandler withOwnerView: view.

"#click:イベントが発生すると、controllerに対し#open:を使ったメッセージを送る。"
view
    handler
        on: #click:
        send:   #open:
        to: controller.
```

同様にイベントハンドラーを指定する別の方法としては、ブロックを指定する方法が考えられる。しかし、イベントハンドラーにブロックを使う方法は、セレクターとオブジェクトを指定する方法のように`inspect`だけでブロックを抱えたオブジェクトがどんな処理を実行するか判断できないうえ、ほとんどの環境はブロックの直列化に対応しておらず直列化もできなくなってしまうため、の文化においては避けるべきとされる。\[36\]

このセレクターとオブジェクトを指定したイベント処理の方法は、Objective-Cの文化にも引き継がれており等のライブラリーにて頻繁に目にすることができる。

### MVCとMVCから派生した設計方式

[Model View Controller](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink")（MVC）は  から生まれた、制御（コントローラー）と情報（モデル）、そして情報の表現方法（ビュー）の3つを分離しクラスオブジェクトの再利用性を高め、実行時に情報と表現の組み合わせを変更できるようにした設計方針である。 の世界でMVCは更に表現を担当するクラスに既定の制御を取り込む仕組みを持たせることで  へと発展した。

#### モデル支援機構

はクラスライブラリーの基礎部分からMVCやMVCから派生した設計方式で使用されるモデルの構築を支援する仕組みを持っており、 以外の言語と比べモデルの構築が格段に楽になっている。次にモデルの動作を確認する最低限のコードを示す。

モデルの登録:

``` smalltalk
"単純なモデルのクラスオブジェクトを登録"
Object
    subclass:       #ValueHolderModel
    instanceVariableNames:  'value'
    classVariableNames: ''
    poolDictionaries:   ''
    category:       'Models'.

ValueHolderModel class methodsFor: 'accessing'
!
defaultValue
    ^ 0.
!!

ValueHolderModel methodsFor: 'accessing'
!
value
    value isNull: [ model := self class defaultValue. ].
    ^ value.
!
value: aValue
    value := aValue.
    self changed: #value.
!!
```

モデルの監視側登録

``` smalltalk
"モデルを監視する単純なクラスオブジェクトを登録"
Object
    subclass:       #ValueHolderObserver
    instanceVariableNames:  'model getSelector'
    classVariableNames: ''
    poolDictionaries:   ''
    category:       'Models'.

ValueHolderObserver class methodsFor: 'accessing'
!
defaultModel
    "model が nil の場合に使用する既定のモデルを返す"
    ^ ValueHolderModel.
!!

ValueHolderObserver methodsFor: 'accessing'
!
value
    model ifNil: [ ^ nil ].
    "modelから指定のセレクターで値を取り出す"
    ^ model perform: getSelector.
!
getState: aGetSelector
    "モデルから値を取り出す際のセレクターはシンボルにより外部から指定する"
    getSelector := aGetSelector.
!
model
    "現在監視対象となっているモデルを返す"
    model isNull:
    [
        model := self class defaultModel new.
        model addDependent: self.
        ].
    ^ model.
!
model: aModel
    "現在監視対象となっているモデルを監視対象から除去し、
     aModelに指定されたオブジェクトを監視対象として追加する。"
    self model removeDependent: self.
    model := aModel.
    self model addDependent: self.

    "また、通常は新しいモデルからValueHolderObserverにとっての初期値の読み取りを行う。
     ここでは、初期値の読み取りの代わりにモデルが持つvalueオブジェクトの内容を表示Window(Transcript)に表示する。"
    Transcript
        show: self value asString;
        cr.
!!

ValueHolderObserver methodsFor: 'updating'
!
update: anAspect
    "モデルが存在しないときは更新しない"
    model ifNil: [ ^ nil ].

    "モデルが更新されると呼び出され、モデルが持つvalueオブジェクトの内容を表示Window(Transcript)に表示する。"
    getSelector = anAspect ifTrue:
    [
        Transcript
            show: self value asString;
            cr.
    ].
!!

ValueHolderObserver class methodsFor: 'instance creation'
!
on: aModel getState: aGetSelector
    ^ self
        getState:   aGetSelector;
        model:      aModel.
!!
```

動作の確認：

``` smalltalk
| model observer |

model := ValueHolderModel new.

"監視対象にmodelを指定してobserverを生成。
 on:getState:内にてmodel valueが返す値、0が表示Window(Transcript)に表示される。"
observer := ValueHolderObserver
    on:     model
    getState:   #value.

"modelの値を更新。observerの#update:が実行されmodel valueが返す値、100が表示Window(Transcript)に表示される。"
model value: 100.
```

モデルの支援機構は全て `Object` クラスオブジェクトに実装されており、全てのオブジェクトはモデルとして動作する。つまりクラスオブジェクトもモデルとして使用できるようになっている。

#### Morphic方式

は  へと場を移し、表現と制御そして、表現対象となる情報を1個のオブジェクトで兼任する  として再設計された。 によって発展した  は  に移植され系統の  環境で基本GUIシステムを構築している。 の  はウェブブラウザ―の[DOM](https://ja.wikipedia.org/wiki/DOM "wikilink")や  に大きな影響を与えている。

## 脚注

## 関連項目

  - [SUnit](https://ja.wikipedia.org/wiki/SUnit "wikilink")
  - [メッセージ](https://ja.wikipedia.org/wiki/メッセージ_\(コンピュータ\) "wikilink")
  - [メッセージ転送](https://ja.wikipedia.org/wiki/メッセージ転送 "wikilink")
  - [利用者定義演算子](https://ja.wikipedia.org/wiki/利用者定義演算子 "wikilink")

## 外部リンク

  -
  -
  -
  -
  - [Reviving Smalltalk-78](http://freudenbergs.de/bert/publications/Ingalls-2014-Smalltalk78.pdf)

[Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:フリー教育ソフトウェア](https://ja.wikipedia.org/wiki/Category:フリー教育ソフトウェア "wikilink")

1.  <https://www.infoq.com/jp/news/2010/07/objects-smalltalk-erlang>
2.
3.  <http://smalltalk.cincom.jp/main/about-us/smalltalks-past/>
4.  <http://www.smalltalk.org/smalltalk/history.html>
5.  <http://stephane.ducasse.free.fr/FreeBooks/BlueBook/Bluebook.pdf>
6.  <http://worrydream.com/EarlyHistoryOfSmalltalk/>
7.  [Reviving Smalltalk-78](http://freudenbergs.de/bert/publications/Ingalls-2014-Smalltalk78.pdf)
8.  <http://www.cincomsmalltalk.com/main/developer-community/trying-cincom-smalltalk/try-cincom-smalltalk/>
9.  <http://www.cincomsmalltalk.com/main/developer-community/trying-cincom-smalltalk/try-cincom-smalltalk/>
10. <http://smalltalk.cincom.jp/tutorials/primers/Introduction/Namespace.ssp>
11. <http://smalltalk.cincom.jp/tutorials/vw7.7/tutorial2/vwparcels2.ssp>
12. <http://www.pharo-project.org/about>
13. <http://strongtalk.org/>
14. <http://pleiad.cl/research/software/gradualtalk>
15. <http://amber-lang.net/>
16. <http://www.object-arts.com/downloads/docs/index.html>
17. <http://www.object-arts.com>
18. <https://sites.google.com/site/jniport/documentation/jniport-for-visualworks>
19. <http://missionsoft.com/>
20. <http://www.refactory.com/tools/sharp-smalltalk>
21.
22. <http://www.objectconnect.com/stmtvc_info.htm>
23. <http://worrydream.com/EarlyHistoryOfSmalltalk/>
24. あるいは単に「セレクター」。
25. [2](https://www.gnu.org/software/smalltalk/manual-base/html_node/ProcessorScheduler_002dbasic.html#ProcessorScheduler_002dbasic)
26.
27. <http://web.cecs.pdx.edu/~harry/musings/SmalltalkOverview.html>
28. <https://www.gnu.org/software/smalltalk/manual/gst.html#Performance>
29. ImplementationLimits7x.pdf(VisualWorks付録)
30. <https://www.gnu.org/software/smalltalk/manual/html_node/Special-objects.html#Special-objects>
31. <https://www.gnu.org/software/smalltalk/manual-base/html_node/Object_002dbuilt-ins.html#Object_002dbuilt-ins>
32. 他の言語でいうメソッドの多重定義はできない。
33.
34. ケント・ベックの  ベストプラクティス・パターン―シンプル・デザインへの宝石集 ISBN 978-4894717541
35. ケント・ベックの  ベストプラクティス・パターン―シンプル・デザインへの宝石集 ISBN 978-4894717541
36. ケント・ベックの  ベストプラクティス・パターン―シンプル・デザインへの宝石集 ISBN 978-4894717541