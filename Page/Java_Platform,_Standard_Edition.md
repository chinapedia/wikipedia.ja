> この記事は[Java Platform, Standard Edition](https://ja.wikipedia.org/wiki/Java_Platform,_Standard_Edition)から翻訳されています。


**Java Platform, Standard Edition** または **Java SE**（バージョン5.0までは Java 2 Platform, Standard Edition または J2SEと呼ばれていた）は多くの[Javaプラットフォーム](https://ja.wikipedia.org/wiki/Javaプラットフォーム "wikilink")プログラムで役立つ[Java](https://ja.wikipedia.org/wiki/Java "wikilink") [APIの集合体である](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[Java仮想マシン](https://ja.wikipedia.org/wiki/Java仮想マシン "wikilink")、[APIなどから構成される](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。 J2SE1.4バージョン (Merlin) 以降、Java SEプラットフォームは[Java Community Process](https://ja.wikipedia.org/wiki/Java_Community_Process "wikilink") (JCP) の下で開発されている。JSR 59 はJ2SE1.4の包括仕様であり、JSR 176はJ2SE 5.0 (Tiger) を、JSR 270はJava SE 6 (Mustang) を規定している。Java SE 7 (Dolphin) はJSR 336の下でリリースされた。

Java SEでは標準的な機能のみが定められており、[サーバ](https://ja.wikipedia.org/wiki/サーバ "wikilink")向けの機能についてはJava SEを拡張した企業向けの[Java Platform, Enterprise Edition](https://ja.wikipedia.org/wiki/Java_Platform,_Enterprise_Edition "wikilink") (Java EE) にて定義されている。

下記は主要なJava SEパッケージの説明である。全てのパッケージリストはを参照。

## 一般的なパッケージ

###

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の基本的なパッケージ。

[パッケージ](https://ja.wikipedia.org/wiki/パッケージ_\(Java\) "wikilink") `java.lang` は、言語と[ランタイム（実行）システムに緊密な基本的な](https://ja.wikipedia.org/wiki/ランタイムライブラリ "wikilink")[クラスと](https://ja.wikipedia.org/wiki/クラス_\(コンピュータ\) "wikilink")[インタフェースを含む](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")。これは[クラス階層を形成する基底クラス](https://ja.wikipedia.org/wiki/階層構造 "wikilink")、言語仕様に密接な型、基本的な[例外](https://ja.wikipedia.org/wiki/例外処理 "wikilink")、数学関数、[スレッド](https://ja.wikipedia.org/wiki/スレッド_\(コンピュータ\) "wikilink")、セキュリティ関数、下位にあるネイティブシステムに関する情報も含む。

`java.lang`の主なクラス:

  - – 全てのクラス階層の頂点に立つクラス。関連項目として、[Javaの文法\#Objectクラスのメソッド](https://ja.wikipedia.org/wiki/Javaの文法#Objectクラスのメソッド "wikilink")を参照。

  - – [列挙クラスの基本クラス](https://ja.wikipedia.org/wiki/列挙型 "wikilink") (J2SE 5.0以降)。

  - – Javaの根幹となるクラス。 [リフレクションシステム](https://ja.wikipedia.org/wiki/リフレクション_\(情報工学\) "wikilink")。

  - – 例外クラス階層の基底クラスとなるクラス。

  - , ,  – 各例外型の[基底クラス](https://ja.wikipedia.org/wiki/スーパークラス_\(計算機科学\) "wikilink")。`RuntimeException`はthrowやthrows宣言をせずとも実行時に起こる例外を指すクラスの[スーパークラスであり](https://ja.wikipedia.org/wiki/スーパークラス_\(計算機科学\) "wikilink")、`Exception`の[サブクラスでもある](https://ja.wikipedia.org/wiki/サブクラス_\(計算機科学\) "wikilink")。`Exception`、`Error`は`Throwable`のサブクラス。

  - – Javaにおいてスレッドを使用することができるクラス。

  - – [文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")と[文字列リテラルを表現するクラス](https://ja.wikipedia.org/wiki/リテラル "wikilink")。

  - ,  – 文字列操作機能を提供するクラス。`StringBuilder`はJ2SE 5.0以降。

  - – 総称的な比較とオブジェクトの大小関係を判定することができる[インタフェース](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink") (J2SE 1.2以降)。

  - – 総称的な反復子とで[拡張`for`](https://ja.wikipedia.org/wiki/foreach文 "wikilink")[ループを使用可能にするインタフェース](https://ja.wikipedia.org/wiki/ループ_\(プログラミング\) "wikilink") (J2SE 5.0以降)。

  - , , , ,  – クラスの[動的ロード](https://ja.wikipedia.org/wiki/ライブラリ#動的リンク "wikilink")、外部[プロセス](https://ja.wikipedia.org/wiki/プロセス "wikilink")の生成、時刻などを問い合わせるホスト環境、[情報セキュリティポリシー](https://ja.wikipedia.org/wiki/情報セキュリティポリシー "wikilink")の執行などを管理する「システムオペレーション」を提供するクラス。

  - ,  – `sin` ([正弦](https://ja.wikipedia.org/wiki/正弦 "wikilink"))、`cos` ([余弦](https://ja.wikipedia.org/wiki/余弦 "wikilink"))、`sqrt` ([平方根](https://ja.wikipedia.org/wiki/平方根 "wikilink")) などの数学関数を提供するクラス。実行環境に依存しない演算結果を保証する`StrictMath`はJ2SE 1.3以降。

  - [プリミティブ型](https://ja.wikipedia.org/wiki/プリミティブ型 "wikilink")を[オブジェクトとして](https://ja.wikipedia.org/wiki/オブジェクト_\(プログラミング\) "wikilink")[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")された[プリミティブラッパークラス](https://ja.wikipedia.org/wiki/プリミティブラッパークラス "wikilink")。

  - 言語レベル若しくは他の共通例外としてスローされる例外基底クラス。

`java.lang`のクラスは[ソースファイル](https://ja.wikipedia.org/wiki/ソースファイル "wikilink")でimport宣言をせずとも自動的にインポートされる。

####

`java.lang.ref`パッケージは、他の可能な許可するアプリケーションと[Java仮想マシン](https://ja.wikipedia.org/wiki/Java仮想マシン "wikilink") (JVM) [ガベージコレクタとの間の限定的な相互関係よりも柔軟な](../Page/ガベージコレクション.md "wikilink")[参照型を提供する](https://ja.wikipedia.org/wiki/参照_\(情報工学\) "wikilink")。それは重要なパッケージであり、それに"java.lang"で始まる名前を与えた言語設計者のための言語として十分に中核をなしたが、それはいくぶん特殊目的であり多くの開発者は使わない。このパッケージはJ2SE1.2から追加された。

Javaは多くのガベージコレクトされた[プログラミング言語](../Page/プログラミング言語.md "wikilink")より柔軟な[参照システムを持ち](https://ja.wikipedia.org/wiki/参照_\(情報工学\) "wikilink")、ガベージコレクションに特別な振る舞いを許可する。Javaにある通常の（言語組み込みの）参照は「強参照(**)」として知られている。`java.lang.ref`パッケージは3つの[弱い参照](https://ja.wikipedia.org/wiki/弱い参照 "wikilink")型（**ソフト参照**`SoftReference`、**弱参照**`WeakReference`、**ファントム参照**`PhantomReference`）を定義している。各々の参照型は特殊な用途のために設計されている。

**** は[キャッシュを実装するために使われている](https://ja.wikipedia.org/wiki/キャッシュ_\(コンピュータシステム\) "wikilink")。オブジェクトは強参照によって到達不可能であるが(*強到達可能)*ではない)、*ソフト到達可能()*と呼ばれるソフト参照によって参照されている。ソフト到達可能なオブジェクトはガベージコレクタの自由裁量によってガベージコレクトされるかもしれない。これは一般的にソフト到達可能なオブジェクトは空きメモリが少ないときのみガベージコレクトされるだろうということを意味する。ところが、それはガベージコレクタの自由裁量にある。意味的に言えば、ソフト参照は「メモリが必要とされなくなるまでこのオブジェクトを保持せよ」ということを意味する。

**** は弱マップを実装するために使われている。強到達可能またはソフト到達可能でなく弱参照によって参照されているオブジェクトは、*[弱到達可能](https://ja.wikipedia.org/wiki/弱到達可能 "wikilink")({{Lang*と呼ばれる。弱到達可能なオブジェクトは次の回収サイクルの間にガベージコレクトされる。この振る舞いはクラスによって使われている。プログラマは弱マップにキー/値ペアを挿入でき、キーがどこからも到達可能でなくなるかどうかを心配する必要がなく、オブジェクトがメモリを占有する可能性を心配しなくてよい。意味的に言えば、弱参照は「他にそれを参照するものが無いときはこのオブジェクトを除去せよ。」を意味する。

**** はガベージコレクションにマークされているオブジェクトを参照するために使われており、[ファイナライズされているが](https://ja.wikipedia.org/wiki/ファイナライザ "wikilink")、未だに再利用されていない。オブジェクトは強、ソフト、弱到達可能でないが、*ファントム到達可能()*と呼ばれるファントム参照によって参照されている。これはファイナライゼーションメカニズムのみによって可能なものよりもより柔軟なクリーンナップを可能にする。意味的に言えば、ファントム参照は「このオブジェクトは長い間必要とされなくなりコレクトされる準備をしている状態でファイナライズされている。」を意味する。

これらの各々の参照型はクラスを継承し、リファレント（指示対象オブジェクト）（または、もし参照がクリアされているか参照型がファントムであるならば`null`)への強参照を返す[メソッド](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\) "wikilink") および、リファレンスをクリアするメソッドを提供する。

`java.lang.ref` もまた参照型が変わるオブジェクトを保持するために上記で検討された各々のアプリケーションが使われるクラスを定義する。 `Reference`が生成されるとき、それは任意にリファレンスキューに登録される。アプリケーションは到達可能性状態の変化した参照を得るためのリファレンスキューを監視する。

参照型とリファレンスキューのより首尾よい説明は*"[Reference Objects and Garbage Collection](http://java.sun.com/developer/technicalArticles/ALT/RefObj/index.html)"* を参照。

####

[リフレクションはJavaコード調査や](https://ja.wikipedia.org/wiki/リフレクション_\(情報工学\) "wikilink")、実行時のJavaコンポーネントやリフレクトされたメンバを使用する上での「リフレクト」を可能にする[Java](https://ja.wikipedia.org/wiki/Java "wikilink") APIの構成要素である。このパッケージにあるクラスは、`java.lang.Class`とに加えて、[デバッガ](https://ja.wikipedia.org/wiki/デバッガ "wikilink")や[インタプリタ](../Page/インタプリタ.md "wikilink")、オブジェクト[インスペクタ](https://ja.wikipedia.org/wiki/インスペクタ "wikilink")（調査）、[クラスブラウザ](https://ja.wikipedia.org/wiki/クラスブラウザ "wikilink")のようなアプリケーション、オブジェクト[シリアライゼーションや](https://ja.wikipedia.org/wiki/シリアライズ "wikilink")[JavaBeans](https://ja.wikipedia.org/wiki/JavaBeans "wikilink")のようなサービスに適合し、（その実行クラスを基礎とする）ターゲットとなるオブジェクトのpublicメンバまたは与えられたクラスによって宣言されたメンバにアクセスする必要がある。このパッケージはJDK1.1より追加された。

リフレクションはインスタンスによって使われ、それらの名前を使ってメソッドを呼び出す、[動的プログラミングを許可する着想である](https://ja.wikipedia.org/wiki/動的プログラミング言語 "wikilink")。クラス、インタフェース、メソッド、[フィールド](https://ja.wikipedia.org/wiki/フィールド_\(計算機科学\) "wikilink")、[コンストラクタ](https://ja.wikipedia.org/wiki/コンストラクタ "wikilink")はすべて実行時に見つけて利用することができる。[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")によってサポートされているリフレクションはそのプログラムの近くにあるJVMである。そこにはリフレクションによって呼び出された二つの技術がある。

1.  *Discovery* はオブジェクトやクラスの取得に関わり、メンバ、スーパークラス、実装されたインタフェースとそのとき発見された要素を使う可能性の発見に関わる。
2.  *Use by name* は要素のシンボル名呼び出し始めて、名付けられた要素を使用する。

##### Discovery

Discoveryはだいたいオブジェクトから始まり、`Class`のオブジェクトを取得するメソッドを呼び出す。`Class`オブジェクトはクラスの中身を発見する数種のメソッドを持つ。以下にその例を示す:

  - – クラスまたはインタフェースのpublicメソッドすべてをオブジェクトの配列として返す。

  - – クラスのpublicコンストラクタすべてをの配列として返す。

  - – クラスまたはインタフェースのpublicフィールドすべてをオブジェクトの配列として返す。

  - – クラスまたはインタフェースのメンバ(e.g. [内部クラス](https://ja.wikipedia.org/wiki/内部クラス "wikilink"))としてのpublicなクラスまたはインタフェースすべてを`Class`の配列として返す。

  - – クラスまたはインタフェースのスーパークラスを`Class`オブジェクトを返す。インタフェースの場合は常に`null`を返す。

  - – クラスまたはインタフェースによって実装されているすべてのインタフェースを`Class`オブジェクトの配列として返す。

##### Use by name

`Class`オブジェクトは「クラス[リテラル](https://ja.wikipedia.org/wiki/リテラル "wikilink")」(e.g. `MyClass.class`) を使用すること、またはメンバのシンボル名を使うことで得られる (e.g. )。`Class`オブジェクト、メンバ`Method`、`Constructor`、`Field`オブジェクト、などの名前による発見を通して得られる。例:

  - – `Method`オブジェクトを返す。`Class...`引数によって特定される引数を受け入れるクラスまたはインタフェースの"methodName"という名のpublicメソッドを表現する。

  - – `Class...`引数によって特定される引数を受け入れるクラスのpublicコンストラクタを表現する`Constructor`オブジェクトを返す。

  - – クラスまたはインタフェースの名前が"fieldName"であるpublicフィールドを表現する`Field`オブジェクトを返す。

`Method`、`Constructor`、`Field`オブジェクトはクラスのメンバを表現した動的アクセスで利用することができる。例:

  - – `get()`に渡したオブジェクトのインスタンスからフィールドの値を含む`Object`を返す。もし`Field`オブジェクトがstaticフィールドを表現するときは、`Object`引数は無視されて`null`となることがある。)

  - – `invoke()`に渡した第一`Object`引数をインスタンスとしてメソッド呼び出しの結果を含む`Object`を返す。

`Object...`引数に留まるものはメソッドによって渡される。(もし`Method`オブジェクトが[静的メソッド](https://ja.wikipedia.org/wiki/静的メソッド "wikilink")である場合は第一`Object`引数が無視されて`null`となることがある。)

  - – コンストラクタによって呼び出されて新たに作られた`Object`インスタンスを返す。`Object...`引数はコンストラクタへ渡される。(によって呼び出されることもできるクラスとしての引数無しコンストラクタに注意すること。)

##### [配列](https://ja.wikipedia.org/wiki/配列 "wikilink")と[プロキシ](https://ja.wikipedia.org/wiki/プロキシ "wikilink")

`java.lang.reflect`パッケージもまた静的メソッドを含み配列オブジェクトを巧みに扱うクラスと、J2SE1.3以降登場した、特定のインタフェースを実装したプロキシクラスの動的生成をサポートするクラスを提供する。

`Proxy`クラスの実装はインタフェースを実装した補給オブジェクトによって提供される。

`InvocationHandler`の  メソッドはプロキシオブジェクトで呼び出された各々のメソッドに呼ばれる。—第一引数はプロキシオブジェクト、第二引数はプロキシによって実装されたインタフェースメソッド`Method`オブジェクト、第三引数はインタフェースメソッドへ渡す引数の配列である。`invoke()`メソッドはプロキシインタフェースメソッドを飛ぶコードを戻り値として含む`Object`を戻り値として返す。

###

`java.io`パッケージは[入出力](https://ja.wikipedia.org/wiki/入出力 "wikilink")(I/O)をサポートするクラスを含む。 パッケージにあるクラスは本来[ストリーム指向である](https://ja.wikipedia.org/wiki/ストリーム_\(プログラミング\) "wikilink")。; しかしながら、[ランダムアクセス](https://ja.wikipedia.org/wiki/ランダムアクセス "wikilink")[ファイル (コンピュータ)としてのクラスもまた提供されている](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")。パッケージで中心となるクラスはそれぞれ[バイトストリーム](https://ja.wikipedia.org/wiki/バイトストリーム "wikilink")の読み書きを行う抽象[クラスである](https://ja.wikipedia.org/wiki/クラス_\(コンピュータ\) "wikilink")とである。このパッケージもまた多数の[ファイルシステム](../Page/ファイルシステム.md "wikilink")との相互作用をサポートする多少の様々なクラスを持っている。

#### ストリーム

ストリームクラスはストリームクラスに特色を加えたベースとなるサブクラスを拡張した[Decoratorパターン](https://ja.wikipedia.org/wiki/Decoratorパターン "wikilink")に沿っている。ベースとなるストリームクラスのサブクラスはたいてい以下の特質を用いて名付けられる。:

  - ストリームデータの送信元/送信先
  - ストリームへ書き込まれた/読み込むデータ型
  - ストリームデータ上で行われる追加処理やフィルタリング

ストリームサブクラスは*`Xxx`*が特色を記述し*`StreamType`*が`InputStream`、`OutputStream`、`Reader`、`Writer`のような名前をもつ[パターン](https://ja.wikipedia.org/wiki/パターン "wikilink")*`XxxStreamType`*を使って名付けられる。

以下の表は`java.io`パッケージが直にサポートする送信元/送信先を示す:

<table>
<caption>java.ioパッケージが直にサポートする送信元/送信先</caption>
<thead>
<tr class="header">
<th style="text-align: left;"><p>送信元/送信先</p></th>
<th><p>接頭辞</p></th>
<th><p>ストリーム型</p></th>
<th><p>入出力</p></th>
<th><p>クラス</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><p><a href="https://ja.wikipedia.org/wiki/バイト_(情報)" title="wikilink">バイト (情報)</a> <a href="https://ja.wikipedia.org/wiki/配列" title="wikilink">配列</a> (<code>byte[]</code>)</p></td>
<td><p><code>ByteArray</code></p></td>
<td><p>byte</p></td>
<td><p>in, out</p></td>
<td><p>, </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>文字配列 (<code>char[]</code>)</p></td>
<td><p><code>CharArray</code></p></td>
<td><p>char</p></td>
<td><p>in, out</p></td>
<td><p>, </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><a href="https://ja.wikipedia.org/wiki/ファイル_(コンピュータ)" title="wikilink">ファイル</a></p></td>
<td><p><code>File</code></p></td>
<td><p>byte, char</p></td>
<td><p>in, out</p></td>
<td><p>, , , </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><a href="https://ja.wikipedia.org/wiki/文字列" title="wikilink">文字列</a> (<a href="https://ja.wikipedia.org/wiki/StringBufferとStringBuilder" title="wikilink"><code>StringBuffer</code></a>)</p></td>
<td><p><code>String</code></p></td>
<td><p>char</p></td>
<td><p>in, out</p></td>
<td><p>, </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><a href="https://ja.wikipedia.org/wiki/スレッド_(コンピュータ)" title="wikilink">スレッド</a> (<code>Thread</code>)</p></td>
<td><p><code>Piped</code></p></td>
<td><p>byte, char</p></td>
<td><p>in, out</p></td>
<td><p>, , , </p></td>
</tr>
</tbody>
</table>

他の標準ライブラリパッケージは、メソッドやJava EEのクラスが返す`InputStream`のような他の送信先としてストリーム実装を提供する。

データ型ハンドリング、ストリームデータのプロセッシングやフィルタリングはストリーム[フィルタを通してできあがっている](https://ja.wikipedia.org/wiki/フィルタ_\(ソフトウェア\) "wikilink")。フィルタクラスはすべて、コンストラクタの引数としてもう一つの互換ストリームオブジェクトを受け入れ、追加された特色とともに囲まれたストリームをデコレート(*decorate*)する。ベースとなるフィルタクラス、、、を拡張することでフィルタは生成される。

`Reader`と`Writer`クラスは真に、バイトを文字にコンバートするためのデータストリームで追加処理を行うバイトストリームである。それらはJ2SE5.0から登場した静的メソッドによって返されるを使う。クラスは`InputStream`を`Reader`へとコンバートし、クラスは`OutputStream`を`Writer`へコンバートする。これら双方のクラスは特別に役立つ文字エンコーディングを許可するコンストラクタを持っている—もしエンコーディングが指定されていなければ、プラットフォームにあるデフォルトエンコーディングを使用する。

以下の表は`java.io`パッケージを直にサポートする他の処理、フィルタを示す。これらのクラスはすべて`Filter`クラスに相当するものを継承している。

<table>
<caption>java.ioパッケージを直にサポートする他の処理、フィルタ</caption>
<thead>
<tr class="header">
<th style="text-align: left;"><p>命令</p></th>
<th><p>接頭辞</p></th>
<th><p>ストリーム型</p></th>
<th><p>入出力</p></th>
<th><p>クラス</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><p><a href="https://ja.wikipedia.org/wiki/バッファ" title="wikilink">バッファ</a>リング</p></td>
<td><p><code>Buffered</code></p></td>
<td><p>byte, char</p></td>
<td><p>in, out</p></td>
<td><p>, , , </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>「プッシュバック」 最後の値を読む</p></td>
<td><p><code>Pushback</code></p></td>
<td><p>byte, char</p></td>
<td><p>in</p></td>
<td><p>, </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>読込/書込 <a href="https://ja.wikipedia.org/wiki/プリミティブ型" title="wikilink">プリミティブ型</a></p></td>
<td><p><code>Data</code></p></td>
<td><p>byte</p></td>
<td><p>in, out</p></td>
<td><p>, </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><a href="https://ja.wikipedia.org/wiki/直列化" title="wikilink">直列化</a>(シリアライズ) (読込/書込オブジェクト)</p></td>
<td><p><code>Object</code></p></td>
<td><p>byte</p></td>
<td><p>in, out</p></td>
<td><p>, </p></td>
</tr>
</tbody>
</table>

#### ランダムアクセス

クラスはファイルの*[ランダムアクセス](https://ja.wikipedia.org/wiki/ランダムアクセス "wikilink")*読み書きをサポートする。このクラスはファイル内の次の読込または書込命令を行うバイトオフセットを表現する*[ファイルポインタ](https://ja.wikipedia.org/wiki/ファイルポインタ "wikilink")*を使用する。ファイルポインタは読み書きによって無条件に動かされ、 またはメソッドによって明確になる。 ファイルポインタのカレントポジションはメソッドによって返される。

#### ファイルシステム

クラスは[ファイルシステム](../Page/ファイルシステム.md "wikilink")の[ファイルや](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[ディレクトリ](https://ja.wikipedia.org/wiki/ディレクトリ "wikilink")[パス](https://ja.wikipedia.org/wiki/パス "wikilink")を表現する。 `File`オブジェクトはファイル、ディレクトリの生成、削除、リネームや「読み取り専用」や「最終更新[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")」のような[ファイル属性](https://ja.wikipedia.org/wiki/ファイル属性 "wikilink")操作をサポートする。`File` オブジェクトはファイルとディレクトリを含むすべてのリストを得るために使われるディレクトリを表現することができる。  クラスはバイトの送信元または廃棄先(送信先)を表現する[ファイル記述子](https://ja.wikipedia.org/wiki/ファイル記述子 "wikilink")である。一般的にこれはファイルであるが、[コンソール](https://ja.wikipedia.org/wiki/コンソール "wikilink")や[ネットワークソケット](https://ja.wikipedia.org/wiki/ネットワークソケット "wikilink")にすることもできる。 `FileDescriptor` オブジェクトは`File` ストリームを生成するために使われている。それらは `File` ストリーム、`java.net` ソケットや[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")ソケットから得られる。

###

J2SE 1.4では、パッケージ`java.nio` (NIO または New I/O) が[メモリマップドI/O](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")、ときどき劇的にベターなパフォーマンスを得る基本ハードウェアと、よりいっそう親密な[入出力](https://ja.wikipedia.org/wiki/入出力 "wikilink")命令を容易にするサポートが追加された。`java.nio` パッケージはバッファ型サポートを提供する。サブパッケージ  は文字データとは異なる[文字エンコーディングサポートを提供する](../Page/文字コード.md "wikilink")。サブパッケージ  はファイルやソケットのようなI/O命令演算能力がある資格を与える接続を表現する「[チャネル](https://ja.wikipedia.org/wiki/チャネル・コントローラ "wikilink")」サポートを提供する。`java.nio.channels` パッケージもまたファイルのきめ細かい[ロックサポートを提供する](https://ja.wikipedia.org/wiki/ロック_\(情報工学\) "wikilink")。

###

[java.math package](https://ja.wikipedia.org/wiki/java.math "wikilink") ([剰余](https://ja.wikipedia.org/wiki/剰余 "wikilink")演算を含む)多倍長精度の演算をサポートし[暗号](../Page/暗号.md "wikilink")鍵を生成するための多倍長の[素数](https://ja.wikipedia.org/wiki/素数 "wikilink")生成を提供する。 以下にパッケージのメインクラスを示す:

  - – 任意精度の符号付き10進数を提供する。 `BigDecimal` は`RoundingMode`を通して誤差の揺るまいをコントロールすることができる。

  - – 任意精度の整数を提供する。 `BigInteger`による演算は、約21億桁もの巨大な数値を扱わない限り、[算術オーバーフロー](https://ja.wikipedia.org/wiki/算術オーバーフロー "wikilink")や[桁落ち](https://ja.wikipedia.org/wiki/桁落ち "wikilink")を生じない。標準数値演算に加えて、これは[剰余演算](https://ja.wikipedia.org/wiki/除法#剰余演算 "wikilink")、[GCD計算](https://ja.wikipedia.org/wiki/最大公約数 "wikilink")、[素数判定](https://ja.wikipedia.org/wiki/素数判定 "wikilink")、[素数](https://ja.wikipedia.org/wiki/素数 "wikilink")生成、[ビット演算](https://ja.wikipedia.org/wiki/ビット演算 "wikilink")など他様々な演算を提供する。

  - – 数値演算の精度などのルール設定を[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")する。

  - – 8つの丸め誤差を提供する[列挙型](https://ja.wikipedia.org/wiki/列挙型 "wikilink")である。

###

`java.net` パッケージは他の共通トランザクションと同じくらい良質の[HTTPリクエストネットワーク向けに特別なI](../Page/Hypertext_Transfer_Protocol.md "wikilink")/Oルーチンを提供する。

###

`java.text` パッケージは文字列をパースするルーチンを実装し、様々な自然言語、ロケールに依存したパースをサポートする。

###

`java.util`パッケージの中心である集約したオブジェクト[データ構造](../Page/データ構造.md "wikilink")。 パッケージに含まれているものは、[デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン "wikilink")を非常に考慮したデータ構造階層、[コレクションAPI](https://ja.wikipedia.org/wiki/コンテナ_\(データ型\) "wikilink")([コンテナ](https://ja.wikipedia.org/wiki/コンテナ_\(データ型\) "wikilink"))である。

## 特殊パッケージ

###

[Javaアプレット](../Page/Javaアプレット.md "wikilink")生成をサポートするために作られた`java.applet`パッケージはネットワーク越しにダウンロードされた保護された[サンドボックス上で動くアプリケーションを許可する](https://ja.wikipedia.org/wiki/サンドボックス_\(セキュリティ\) "wikilink")。セキュリティ制約は簡単にサンドボックスに適用される。開発者は、例えば、それが安全であることを示すために、アプレットに[電子署名](https://ja.wikipedia.org/wiki/電子署名 "wikilink")を適用することができる。(ローカルハードドライブにアクセスするような)制限された処理を行うアプレットの許可を認めるため、そういう行為をユーザに許し、サンドボックスの制限を部分的または全て取り払う。デジタル証明書は[Thawte](https://ja.wikipedia.org/wiki/Thawte "wikilink")や[Entrust](https://ja.wikipedia.org/wiki/Entrust "wikilink")のような機関によって発行される。

###

`java.beans`パッケージに含まれているものは開発やbean操作のための様々なクラスであり、[JavaBeans](https://ja.wikipedia.org/wiki/JavaBeans "wikilink")アーキテクチャによって定義された再利用コンポーネントである。アーキテクチャはコンポーネントのプロパティ操作やそれらのプロパティが変更されたときの発火イベントのメカニズムを提供する。

`java.beans`にあるAPIの多くはbeanが結合、カスタマイズ、操作されうるbean編集ツールによる使用として書かれている。beanエディタのとあるタイプは、[IDEにある](https://ja.wikipedia.org/wiki/統合開発環境 "wikilink")[GUIデザイナである](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。

###

The [Abstract Windowing Toolkit](https://ja.wikipedia.org/wiki/Abstract_Windowing_Toolkit "wikilink")(AWT)は基本的な[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")命令をサポートするルーチンを含み、 基礎を成すネィティブシステムから基本的なウィンドウズを使用する。Java API（GNUの[libgcj](https://ja.wikipedia.org/wiki/libgcj "wikilink")のような）多くの独自実装は何もかも実装しているがしかし、AWTは多くの[サーバサイド](https://ja.wikipedia.org/wiki/サーバサイド "wikilink")アプリケーションで使われていない。このパッケージもまた[Java 2DグラフィックAPIを含んでいる](https://ja.wikipedia.org/wiki/Java_2D "wikilink")。

###

`java.rmi` パッケージは異なるJVM上にある2つのJavaアプリケーション間での[RPCをサポートする](https://ja.wikipedia.org/wiki/遠隔手続き呼出し "wikilink") [Java Remote Method Invocationを提供する](https://ja.wikipedia.org/wiki/Java_Remote_Method_Invocation "wikilink")。

###

メッセージダイジェストアルゴリズムを含んでいるセキュリティサポートは`java.security` に含まれている。

###

[JDBC](https://ja.wikipedia.org/wiki/JDBC "wikilink") API ([SQL](https://ja.wikipedia.org/wiki/SQL "wikilink")[データベース](../Page/データベース.md "wikilink")接続で使用)の実装は`java.sql`パッケージにまとめられている。

###

アプリケーション間のリモート間通信を提供し、[RMI](https://ja.wikipedia.org/wiki/RMI "wikilink") over [IIOP](https://ja.wikipedia.org/wiki/IIOP "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")を使用する。このプロトコルはRMIと[CORBA](https://ja.wikipedia.org/wiki/CORBA "wikilink")と連携させる。

###

[general inter ORB protocolを使用するアプリケーション間のリモート間通信をサポートし](https://ja.wikipedia.org/wiki/GIOP "wikilink")、[CORBA](https://ja.wikipedia.org/wiki/CORBA "wikilink")の他の[フィーチャー](https://ja.wikipedia.org/wiki/フィーチャー "wikilink")をサポートする。[RMIと](https://ja.wikipedia.org/wiki/Java_Remote_Method_Invocation "wikilink")[RMI-IIOP](https://ja.wikipedia.org/wiki/RMI-IIOP "wikilink")と同じく、このパッケージは(通常、ネットワーク経由で)他の[仮想マシン上で動いているオブジェクトのリモートメソッドを呼ぶためにある](https://ja.wikipedia.org/wiki/仮想機械 "wikilink")。 すべての通信可能性からCORBAは様々なプログラミング言語でもっともポータブルである。しかしながら、それはCORBAを理解することをもいくぶん難しくしている。

###

[Swing](https://ja.wikipedia.org/wiki/Swing "wikilink")はプラットフォーム非依存の[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")を提供する`java.awt`を基礎とするルーチンの集合である。Swingは下層のネイティブ[OS独自の](../Page/オペレーティングシステム.md "wikilink")[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")サポートに頼る代わりに、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")をレンダリングするために2次元描画ルーチンを使用する。

GUI上のウィジェットが下層のネイティブシステムから模倣することができるように、Swingは着脱可能な[ルック・アンド・フィール](https://ja.wikipedia.org/wiki/ルック・アンド・フィール "wikilink") () をサポートする。システム全体に行き渡っている[デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン "wikilink")、特に[MVCパターンの改良版は](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink")、機能と外観との間の[結合度](https://ja.wikipedia.org/wiki/結合度 "wikilink")を緩めている。1点、統一されていないのは、(J2SE 1.3現在において) フォントがJavaではなく下層のネイティブシステムによって描画されるということであり、これによりテキスト移植性を限定してしまっている。次善策としては、[ビットマップ](https://ja.wikipedia.org/wiki/ビットマップ "wikilink")フォントを使うことが挙げられる。一般的に「[レイアウト](https://ja.wikipedia.org/wiki/レイアウト "wikilink")」が使用され、これは要素をクロスプラットフォームかつ審美眼的に一貫したGUIに保つ。

###

様々な[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")や[ウェブボットの記述に関して使われる](https://ja.wikipedia.org/wiki/インターネットボット "wikilink")、エラー耐性のある[HTMLパーサを提供する](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink")。

## 関連項目

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink") 、[Java\#Javaのエディション](https://ja.wikipedia.org/wiki/Java#Javaのエディション "wikilink")（Java SE、Java EE、Java MEなど）、[Java\#バージョン履歴](https://ja.wikipedia.org/wiki/Java#バージョン履歴 "wikilink")（JDK 1.0からJ2SE 1.2、Java SE 8、Java SE 9など）
  - [Java Platform, Enterprise Edition](https://ja.wikipedia.org/wiki/Java_Platform,_Enterprise_Edition "wikilink") (Java EE) - Java の大規模システム向けエディション（J2EEから、Java EE 5、Java EE8など）
  - [Java Platform, Micro Edition](https://ja.wikipedia.org/wiki/Java_Platform,_Micro_Edition "wikilink") (Java ME) - Java の[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けエディション

## 外部リンク

  - [Oracle - Java SE](http://www.oracle.com/technetwork/jp/java/javase/overview/)
      - [JDK Oracle JDK 9ドキュメント](http://docs.oracle.com/javase/jp/9/)
      - [API仕様](https://docs.oracle.com/javase/jp/9/docs/api/overview-summary.html)
  - [JSR 336](https://www.jcp.org/en/jsr/detail?id=336) (Java SE 7)
  - [JSR 270](https://www.jcp.org/en/jsr/detail?id=270) (Java SE 6)
  - [JSR 176](https://www.jcp.org/en/jsr/detail?id=176) (J2SE 5.0)
  - [JSR 59](https://www.jcp.org/en/jsr/detail?id=59) (J2SE 1.4)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink")