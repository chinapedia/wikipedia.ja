> この記事は[Xcode](https://ja.wikipedia.org/wiki/Xcode)から翻訳されています。


**Xcode**（エックスコード）は、[ソフトウェア](../Page/ソフトウェア.md "wikilink")を開発するための[アップルの](../Page/アップル_\(企業\).md "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) であり、かつては[Mac OS Xに付属する形で配布されていた](https://ja.wikipedia.org/wiki/macOS "wikilink")。[Mac OS X v10.3のリリースと共に](../Page/Mac_OS_X_v10.3.md "wikilink")[2003年](../Page/2003年.md "wikilink")[10月24日](../Page/10月24日.md "wikilink")に初めて紹介されたこのソフトは、[NeXT](../Page/NeXT.md "wikilink")の資産を受け継ぐMac OS Xの初期IDE「**Project Builder**」を進化させる事となった。

[Macintosh](../Page/Macintosh.md "wikilink") (macOS) にてmacOSあるいは[iOS](https://ja.wikipedia.org/wiki/iOS "wikilink")用の[アプリケーションを開発する場合](../Page/アプリケーションソフトウェア.md "wikilink")、また[ソースコード](../Page/ソースコード.md "wikilink")で配布されている[UNIX](../Page/UNIX.md "wikilink")用ソフトウェアをインストールする場合に、Xcodeが必要になる。初期状態ではXcodeはインストールされておらず、[Mac App Storeからの無料ダウンロードでインストールを行う](https://ja.wikipedia.org/wiki/Mac_App_Store "wikilink")。

## 特徴

Xcodeでは[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")を作成するために使用するグラフィカルツール、[Interface Builder](../Page/Interface_Builder.md "wikilink")（[NeXT](../Page/NeXT.md "wikilink")社の資産）を用いて、UI画面の設計ができる。バージョン4.0以前は、Interface Builderは、Xcodeと独立したツールで、開発者は、XcodeとInterface Builderを行き来して、コーディングしていた。しかし、バージョン4.0で、Interface Builderは、Xcodeに統合された。

Xcode は[GNU Compiler Collection](../Page/GNUコンパイラコレクション.md "wikilink") (GCC) を含み、[Cocoa](../Page/Cocoa.md "wikilink"), [Carbon](../Page/Carbon.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に制限されることなく、多様なプログラミング・[モジュール](../Page/モジュール.md "wikilink")を含む[C](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[Objective C++](https://ja.wikipedia.org/wiki/Objective-C#Objective-C++ "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[AppleScript](../Page/AppleScript.md "wikilink")、そして[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")記述言語[Objective-C](../Page/Objective-C.md "wikilink")および[Swiftのソースコードをコンパイルできる](https://ja.wikipedia.org/wiki/Swift_\(プログラミング言語\) "wikilink")。[サードパーティー](../Page/サードパーティー.md "wikilink")は[GNU Pascal](../Page/GNU_Pascal.md "wikilink")、[Free Pascal](../Page/Free_Pascal.md "wikilink")、[Ada](../Page/Ada.md "wikilink")向けの追加サポートを行っている。

Xcodeは主にプロジェクト管理、コード編集、[デバッグを行う為のソフトである](../Page/バグ.md "wikilink")。この他に[クラスブラウザやドキュメントブラウザなどが統合されている](../Page/クラス_\(コンピュータ\).md "wikilink")。[Delphi](../Page/Delphi.md "wikilink")や[Visual Basicと異なり単体では](../Page/Visual_Basic.md "wikilink")[RAD的なツールではないが](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")、[Interface Builderとよく連携しており](../Page/Interface_Builder.md "wikilink")、簡易な[テキストエディタ](../Page/テキストエディタ.md "wikilink")などであれば一行のコードも書く事なく開発できる。

[distcc](https://ja.wikipedia.org/wiki/distcc "wikilink")による分散[ビルドをサポートし](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")、[Bonjour](../Page/Bonjour.md "wikilink")によるネットワーク検索及び構築を行う。

さらに10.4付属のVersion 2.0からは[Core Data](https://ja.wikipedia.org/wiki/Core_Data "wikilink")/[WebObjects](../Page/WebObjects.md "wikilink")で用いるUMLに準じたモデルエディタが統合された。

ファイル管理は同社の[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")などに準じた形式でやや癖があるが、全体としてはよく整理されており、比較的プログラマ臭のしないツールである。

その他の特徴として[ZeroLink](https://ja.wikipedia.org/wiki/ZeroLink "wikilink")が挙げられる。これは[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")後のリンク過程を実行時まで遅延することで高速なソフトの再起動を行なうもので、[Delphi](../Page/Delphi.md "wikilink")や[C\#ほどではないが](../Page/C_Sharp.md "wikilink")、かなりの速度でソフトを再構築できる。

## バージョン

### 2.X

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2.0</p></td>
<td><p>2005年4月29日</p></td>
<td><ul>
<li>Mac OS X 10.4 Tigerと同時リリース。</li>
<li>Mac OS X <a href="../Page/ソフトウェア開発キット.md" title="wikilink">SDKサポート利用による</a> <a href="../Page/Mac_OS_X_v10.1.md" title="wikilink">Mac OS X v10.1</a>、<a href="../Page/Mac_OS_X_v10.2.md" title="wikilink">Mac OS X v10.2</a> (Jaguar)、<a href="../Page/Mac_OS_X_v10.3.md" title="wikilink">Mac OS X v10.3</a> (Panther)、および<a href="../Page/Mac_OS_X_v10.4.md" title="wikilink">Mac OS X v10.4</a> (Tiger) 向け開発サポート。</li>
<li><a href="../Page/GNUコンパイラコレクション.md" title="wikilink">GCCコンパイラの新しいバージョン</a> (4.0) が含まれる。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>2.1</p></td>
<td><p>2005年6月6日</p></td>
<td><ul>
<li>WWDC 2005 にてリリース。</li>
<li>Mac OS X SDKサポート利用によるMac OS X v10.4.1 上での<a href="../Page/PowerPC.md" title="wikilink">PowerPC</a>および<a href="https://ja.wikipedia.org/wiki/インテル" title="wikilink">インテル</a>設計のためのユニバーサル・バイナリ (<a href="https://ja.wikipedia.org/wiki/:en:Universal_binary" title="wikilink">Universal binary</a>) 制作サポート。</li>
<li><a href="../Page/WebObjects.md" title="wikilink">WebObjects</a>開発ツールがオプションでのインストールでXcodeツールに追加される。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2.2</p></td>
<td><p>2005年11月11日</p></td>
<td><ul>
<li>gccが4.0.1にバージョンアップ。</li>
<li><a href="../Page/日本語.md" title="wikilink">日本語</a>リソースが再び含まれるようになった。</li>
<li>Deploymentビルドがクラッシュした際にもデバッガに接続してくれるようになった。ただしデバッグシンボルが存在しないため、<a href="../Page/スタックトレース.md" title="wikilink">スタックトレース</a>のみとなる。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>2.2.1</p></td>
<td><p>2006年1月10日</p></td>
<td><ul>
<li>バグ修正 : Xcode IDE、cctools、デバッガ、コンパイラのバグが修正された。</li>
<li>Mac OS X 10.4.4での開発のために10.4u SDKに更新された。</li>
<li>CHUDが4.3.0に更新された。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2.3</p></td>
<td><p>2006年5月23日</p></td>
<td><ul>
<li>DWARFデバッグフォーマットに対応し、デバッグ精度とディスク利用効率の向上を実現した。</li>
<li>新しい分散ネットワークビルド (New Distributed Network Build、DNB) によるスケーラブルなビルドアーキテクチャ。</li>
<li>Xcode IDE、ビルドシステム、Code Senseの安定性と性能の向上。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>2.4</p></td>
<td><p>2006年8月7日</p></td>
<td><ul>
<li><a href="../Page/64ビット.md" title="wikilink">64ビット</a>の<a href="../Page/Intel_Mac.md" title="wikilink">Intel Mac上での開発をサポートするようになり</a>、インテルとPowerPCの両<a href="../Page/CPU.md" title="wikilink">CPU</a>での<a href="../Page/32ビット.md" title="wikilink">32ビット</a>/64ビットの、計4つのアーキテクチャのアプリケーション開発を可能とするようになった。</li>
<li>DWARFバイナリのデバッグ時の著しい段階的な動作が切り詰められ、分散ネットワークビルドにも修正が加えられた。</li>
<li>Mac OS X v10.4.7での開発のために10.4u SDKも更新された。</li>
<li>CHUDが4.4.0に更新された。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2.4.1</p></td>
<td><p>2006年11月1日</p></td>
<td><ul>
<li>DWARFデバッグにおける幾つかの問題を解決し、総合的な安定性と安全性を向上させた。</li>
<li>CHUDが4.4.3に更新され、Xcodeとは独立してリリースされるようになった。</li>
<li>10.3.9 SDKと10.4u SDKも更新された。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>2.5</p></td>
<td><p>2007年9月5日</p></td>
<td><ul>
<li>Mac OS X v10.5 Leopardに先駆けてリリース。</li>
<li>Mac OS X v10.4と10.5において起動可能。しかしMac OS X v10.5上では一部の機能が制限を受ける。</li>
<li>Mac OS X v10.5をターゲットとした開発環境ではなく、Xcode 3.0へのプロジェクトの移行を目的とする。</li>
<li>Mac OS X v10.2.8とMac OS X v10.3.9、Mac OS X 10.4のOSにおけるユニバーサルアプリケーションを開発対象とする。</li>
</ul></td>
</tr>
</tbody>
</table>

### 3.X

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>3.0</p></td>
<td><p>2007年10月26日</p></td>
<td><ul>
<li>Mac OS X v10.5 Leopardと同時リリース。</li>
<li>Mac OS X v10.5において起動可能。それ以前では動作しない。</li>
<li>Objective-C 2.0での開発が可能となり、Xcode 3.0自体もObjective-C 2.0で開発されている。</li>
<li><a href="../Page/GarageBand.md" title="wikilink">GarageBand</a>と似たユーザインタフェースを持つInstruments というパフォーマンスツールが付属する。</li>
<li>Mac OS X v10.5からMac OS X v10.3.9までのOSを対象としたアプリケーション開発環境として推奨されている。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>3.1</p></td>
<td><p>2008年7月11日</p></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/iPhone" title="wikilink">iPhone</a> OSのようなMac OS X以外をターゲットとするSDKがサポートされた。</li>
<li>Mac OS X v10.5向けの開発においてGCC 4.2または<a href="../Page/LLVM.md" title="wikilink">LLVM</a> GCC 4.2がオプションで使用できる。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>3.1.2</p></td>
<td><p>2008年11月24日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.1.3</p></td>
<td><p>2009年6月17日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.1.4</p></td>
<td><p>2009年9月10日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.2</p></td>
<td><p>2009年8月27日</p></td>
<td><ul>
<li>Mac OS X v10.6においてのみ動作する。</li>
<li>Mac OS X v10.6からMac OS X v10.4までのOSを対象としたアプリケーションを開発できるが、デフォルトではMac OS X v10.4のサポートは有効にされない。</li>
<li>Mac OS X v10.6向けの開発においてGCC 4.2がデフォルトになった。</li>
</ul></td>
</tr>
</tbody>
</table>

### 4.X

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>4.0</p></td>
<td><p>2011年3月9日</p></td>
<td><ul>
<li>Mac App Storeで600円で販売される（Developer Programsの会費を払っている場合は無料でダウンロードできる）。</li>
<li>Mac App Store で Mac OS X v10.7 を購入した場合も無料となる。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>4.0.1</p></td>
<td><p>2011年3月25日</p></td>
<td><ul>
<li>起動に失敗する問題を修正。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>4.1</p></td>
<td><p>－</p></td>
<td><ul>
<li>デフォルトコンパイラがgccからllvm-gcc 4.2になった。値段が600円から無償になった。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>4.2</p></td>
<td><p>－</p></td>
<td><ul>
<li>デフォルトコンパイラがllvm-gccから<a href="https://ja.wikipedia.org/wiki/Clang" title="wikilink">llvm clang</a> 3.0になった。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>4.3</p></td>
<td><p>－</p></td>
<td><ul>
<li>各種ツールセットが単一のXcodeとして配布されるようになった。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>4.4</p></td>
<td><p>－</p></td>
<td><ul>
<li>OS X 10.8対応。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>4.5</p></td>
<td><p>－</p></td>
<td><ul>
<li>iOS 6対応。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>4.6</p></td>
<td><p>－</p></td>
<td><ul>
<li>iOS 6.1対応。</li>
</ul></td>
</tr>
</tbody>
</table>

### 5.X

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>5.0</p></td>
<td><p>2013年9月18日</p></td>
<td><ul>
<li>iOS 7.0 SDKのサポートが追加された。</li>
<li>ツールバーが小さくなってフラットデザインになるなどのユーザインタフェースの改良も行われた。</li>
<li>新規プロジェクトの作成からは<a href="../Page/ARC.md" title="wikilink">ARC</a>のメモリ管理がデフォルトで採用されるようになり、ARCがオプション扱いではなくなった。</li>
<li>実行時にデバッグエリアにメモリやCPUの使用状況が表示されるようになった。</li>
<li><a href="../Page/OpenGL_ES.md" title="wikilink">OpenGL ES</a> 3.0のサポートが追加された。</li>
<li>Xcode 4.xでは自動的に追加されていた<a href="https://ja.wikipedia.org/wiki/Auto_Layout" title="wikilink">Auto Layoutの制約が</a>、自動的には追加されなくなっている。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>5.1</p></td>
<td><p>2014年3月10日</p></td>
<td><ul>
<li>iOS 7.1 SDKのサポートが追加された。</li>
<li>全てのconstraintタイプをサポートする新しいAuto Layout constraint inspectorが追加された。</li>
<li>カスタムオブジェクトタイプのためのデバッガーの<a href="../Page/Quick_Look.md" title="wikilink">Quick Lookサポートが追加された</a>。</li>
<li>Instruments内でのsymbol解決能力が向上した。</li>
<li>iOS standard architecture settingsに64ビットを含むよう更新された。</li>
<li>不具合の解消により安定性が向上した。</li>
</ul></td>
</tr>
</tbody>
</table>

### 6.X

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>6.0</p></td>
<td><p>－</p></td>
<td><ul>
<li>OS X v10.10 Yosemiteのサポート</li>
<li>新たな開発言語として、<a href="https://ja.wikipedia.org/wiki/Swift_(プログラミング言語)" title="wikilink">Swiftがサポートされた</a>。</li>
<li>iOS 8.0 SDKがサポートされた。</li>
<li>iOS用には、ユニバーサル・ストーリーボードがサポートされた。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>6.1</p></td>
<td><p>－</p></td>
<td><ul>
<li>Xcode 6.0で問題のあった巨大なストーリーボードを取り扱えない、というバグが解消された。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>6.2</p></td>
<td><p>－</p></td>
<td><ul>
<li>iOS 8.2とWatchKitのサポート、セキュリティアップデート[1]。</li>
</ul></td>
</tr>
</tbody>
</table>

### 7.x

  - iOS 9とOS X El Capitan、Swift 2がサポートされた。

### 8.x

  - iOS 10と[macOS Sierra](https://ja.wikipedia.org/wiki/macOS_Sierra "wikilink")、Swift 3がサポートされた。

### 9.X

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>9.0</p></td>
<td><p>2017年9月19日</p></td>
<td><ul>
<li>iOS 11と<a href="https://ja.wikipedia.org/wiki/macOS_High_Sierra" title="wikilink">macOS High Sierra</a>、Swift 4がサポートされた。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>9.1</p></td>
<td><p>－</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>9.2</p></td>
<td><p>2017年12月5日</p></td>
<td><ul>
<li>iOS 11.2と<a href="https://ja.wikipedia.org/wiki/macOS_High_Sierra" title="wikilink">macOS High Sierra</a> 10.13.2、watchOS 4.2、tvOS 11.2がサポートされた。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>9.3</p></td>
<td><p>2018年3月29日</p></td>
<td><ul>
<li>Swift 4.1、iOS 11.3と<a href="https://ja.wikipedia.org/wiki/macOS_High_Sierra" title="wikilink">macOS High Sierra</a> 10.13.4、watchOS 4.3、tvOS 11.3がサポートされた。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>9.3.1</p></td>
<td><p>2018年5月11日</p></td>
<td><ul>
<li>Playgroundが遅くなる、 Apple ID再入力を要求する問題の修正。</li>
</ul></td>
</tr>
</tbody>
</table>

### 10.x

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10.0</p></td>
<td><p>2018年9月17日</p></td>
<td><ul>
<li>iOS 4.2、watchOS 5、tvOS 12、macOS Mojaveをサポート。</li>
</ul>
<dl>
<dt>macOS Mojaveのダークモード</dt>

</dl>
<p>:* XcodeとInstrumentsで、まったく新しいダークな外観(ダークモード)を追加。</p>
<p>:* アセットカタログは、カラーとイメージアセットをカスタマイズするために、ダーク及びライトのバリエーションを追加します。</p>
<p>:* Interface Builderは、アプリのインターフェースのダークモード/ライトモードを簡単に切り替えられる。</p>
<p>:* デバッガでは、OSの設定を変更せずにMacアプリをダークモード/ライトモードの間で切り替えることが可能。</p>
<dl>
<dt>ソースコントロール</dt>

</dl>
<p>:* リポジトリサーバー上のデータと異なっている部分は、以下のようにエディタ内で直接強調表示されます。</p>
<p>:**ローカルの変更はまだ共有リポジトリにプッシュされていません</p>
<p>:**他のユーザが行ったアップストリームの変更</p>
<p>:**コミット前に編集の競合に対処してください</p>
<p>:* Atlassian Bitbucket、GitLab、GitHubの自己ホスト型およびクラウドサーバとのアカウント統合が可能。</p>
<p>:* アカウントログインでは、必要に応じてSSHキーを生成し、サービスプロバイダにアップロードできます。</p>
<p>:* Rebaseは、コードの最新バージョンを取得する際のオプションとなります。</p>
<dl>
<dt>エディタの強化</dt>

</dl>
<p>:* エディタで複数のカーソルを使用すること、一度に多くの変更が可能になりました。</p>
<p>:* コード横の折りたたみリボンは、中括弧で囲まれた任意のコードブロックを非表示にできます。</p>
<p>:* オーバースクロールを使用すると、コードの最後の行を画面の中央に簡単に表示できます。</p>
<dl>
<dt>プレイグラウンドと機械学習</dt>

</dl>
<p>:* 完全に再設計されたREPLのようなプレイグラウンドは、はるかに速く、より安定しています。</p>
<p>:* SHIFT-RETURNキーを押してコードを実行するか、インライン実行ボタンをクリックして特定の行まで実行できます。</p>
<p>:* 対話形式でトレーニングを行い、プレイグラウンド内で直接MLモデルを作成できるようになりました。</p>
<dl>
<dt>テストとデバッグ</dt>

</dl>
<p>:* デバイスからのデバッグシンボルのダウンロードが以前より約5倍高速化されました。</p>
<p>:* すべてのCPUコアを最大限に活用するために、多数のシミュレータでテストを並行して実行できます。</p>
<p>:* カスタムインストゥルメントは、あらゆるコードのユニークなデータ可視化を提供します。</p>
<p>:* メモリデバッガのレイアウトが再設計され、アプリ全体のナビゲートと視覚化が容易になりました。</p>
<p>:* メタルシェーダデバッガでは、頂点、フラグメント、計算、およびタイルシェーダコードの実行を検査できます。</p></td>
</tr>
<tr class="even">
<td><p>10.1</p></td>
<td><p>2018年10月30日</p></td>
<td><ul>
<li>iOS 12.1、watchOS 5.1、tvOS 12.1、macOS Mojaveをサポート。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>10.2</p></td>
<td><p>2019年3月25日</p></td>
<td><ul>
<li>iOS 12.2、tvOS 12.2、watchOS 5.2、macOS Mojave 10.14 .4をサポート。</li>
<li>追加のバグ修正。</li>
</ul>
<dl>
<dt>Swift 5</dt>

</dl>
<p>:* Swift 5ランタイムは、最新のAppleプラットフォームリリースにOSの一部として含まれています。</p>
<p>:* App Storeでは、最新OSを実行するデバイスへのダウンロードを高速化するために、アプリからSwiftランタイムを削除します。</p>
<p>:* SIMDベクトル型は標準ライブラリに組み込まれています。</p>
<p>:* 文字列リテラルの構文が強化され、読み書きが容易になりました。</p>
<p>:* 新しい結果の列挙により、非同期操作でエラーを処理しやすくなりました。</p>
<dl>
<dt>Xcodeのその他の機能強化</dt>

</dl>
<p>:* デバッガコンソールには、 「p」 または「po」より高速な新しいフレーム変数コマンドのエイリアス 「v」 があります。</p>
<p>:* プレイグラウンドでの様々な安定性の向上やメモリの安全性チェックなど。</p></td>
</tr>
<tr class="even">
<td><p>10.2.1</p></td>
<td><p>2019年4月17日</p></td>
<td><ul>
<li>iOS 12.2、tvOS 12.2、watchOS 5.2、macOS Mojave 10.14 .4をサポート。</li>
<li>大規模なSwiftプロジェクトのビルド時間の問題を修正し、追加のバグ修正。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>10.3</p></td>
<td><p>2019年7月22日</p></td>
<td><ul>
<li>iOS 12.4、tvOS 12.4、watchOS 5.3、macOS Mojave 10.14 .6をサポート。</li>
</ul></td>
</tr>
</tbody>
</table>

### 11.X

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>11.0</p></td>
<td><p>2019年9月12日</p></td>
<td><ul>
<li>iOS13、tvOS13、watchOS 6、macOS Catalina 10.15をサポート。</li>
</ul>
<dl>
<dt>Swift UI[2]</dt>

</dl>
<p>:* SwiftUIフレームワークとデザインツールが連携して、ユーザーインターフェースを構築する新しい方法を実現。</p>
<p>:* (読みやすい)Swiftコードで、ユーザインターフェースを定義することができます。</p>
<p>:* デザインツールを使用すると、ドラッグアンドドロップと同じくらい簡単にビューを作成および編集できます。</p>
<p>:* コードは、デザイン及びプレビューのキャンバスと常に同期されています。</p>
<p>:* コントロールと修飾子のライブラリにより、複雑なインタフェースを簡単に構築できます。</p>
<p>:* アニメーションを、表示するアクションを記述する簡単なコマンドを使用して作成可能。</p>
<p>:* 複数のデバイスタイプ、向き、フォントサイズで実際のアプリケーションのプレビューが可能に。</p>
<p>:* すべてのAppleプラットフォームで共通のコードを共有し、各OSにカスタムのエクスペリエンスを追加可能。</p>
<dl>
<dt>「Mac Catalyst」</dt>

</dl>
<p>:*iPadアプリをMacでも利用可能にできます。</p>
<p>:* iPadプロジェクトから1クリックで、ネイティブMacアプリケーションを開発可能。</p>
<p>:* 1つのプロジェクトとソースコードによって、iPhone、iPad、およびMac用のアプリケーションが作成できるようになりました。</p>
<p>:* Mac独自の操作性を実現するために、アプリケーションの要素をカスタマイズすることが可能。</p>
<p>:* プロジェクト内の既存のUIKitコードに新しいSwiftUIコードを追加することが可能。</p>
<p>:* Mac App Storeに送信するか、外部配布用に公証することが可能。</p>
<dl>
<dt>SwiftとSwiftパッケージ</dt>

</dl>
<p>:* Swiftパッケージをビルド、デバッグ、SCMワークフローを含む全体でサポート。</p>
<p>:* GitHub、Bitbucket、GitLab、もしくは開発者自身のホストのSwiftパッケージを使用することが可能。</p>
<p>:* 依存性の分析に基づいて、パッケージを自動的にダウンロードすることが可能。</p>
<p>:* 独自のパッケージを作成して、すべてのアプリケーション間でコードを共有したり、コミュニティに公開したりすることが可能。</p>
<dl>
<dt>iOSダークモード</dt>

</dl>
<p>:* 開発およびデバッグ中に、明暗モードの切り替えが可能。</p>
<p>:* アセットカタログを使用すると、ダークモードとライトモードのイメージとカラーを簡単に制御可能。</p>
<dl>
<dt>エディタ</dt>

</dl>
<p>:* コードの全体像が表示されるエディタのミニマップを使って、任意の行にすばやくジャンプできます。</p>
<p>:* 各エディタビューには、独自のプレビュー、アシスタント、またはその他の補足的なビューが用意されています。</p>
<p>:* エディタペインを分割して、ワークスペースを希望どおりにレイアウトできます。</p>
<dl>
<dt>その他の改善点</dt>

</dl>
<p>:* スタンドアローンのwatchOSアプリを構築され、より速いデバッグが可能になりました。</p>
<p>:* シミュレータの迅速な起動により、GPUを使用してMetalコードを高速化できます。</p>
<p>:* テストプランによって、共有可能な結果のバンドルを使用し、テストハーネスをより詳細に制御できます。</p>
<p>:* テストプランの一環としてUIテストを使用し、ローカライズされたスクリーンショットを自動的に生成することが可能。</p>
<p>:* ソース制御により、stashおよびcherry-pick操作がサポートされるようになりました。</p>
<p>:* デバッグ中に、ネットワーク速度の低下や温度の警告などのデバイスの状態をシミュレートできます。</p>
<p>:* 整理ビューの 「メトリック」 タブには、ユーザーのデバイス上でのアプリケーションの実行効率が表示されます。</p></td>
</tr>
<tr class="even">
<td><p>11.1</p></td>
<td><p>2019年10月7日</p></td>
<td><ul>
<li>iOS 13.1、 iPadOS 13.1、 tvOS 13、 watchOS 6、 macOS Catalina 10.15をサポート。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>11.2</p></td>
<td><p>2019年10月31日</p></td>
<td><ul>
<li>iOS 13.2、iPadOS 13.2、tvOS 13.2、watchOS 6.1、macOS Catalina 10.15.1をサポート。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>11.2.1</p></td>
<td><p>2019年11月12</p></td>
<td><ul>
<li>iOS 13.2、iPadOS 13.2、tvOS 13.2、watchOS 6.1、macOS Catalina 10.15.1をサポート。</li>
<li>UITextViewを使用するアプリがクラッシュする可能性のある重大な問題を修正。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>11.3</p></td>
<td><p>2019年12月10日</p></td>
<td><ul>
<li>iOS 13.3、iPadOS 13.3、tvOS 13.3、watchOS 6.1.1、macOS Catalina 10.15.2をサポート。</li>
<li>Touch Barのシミュレータでのサポートを追加(第2世代)。</li>
<li>追加のバグ修正と安定性の改善。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>11.3.1</p></td>
<td><p>2020年1月13日</p></td>
<td><ul>
<li>iOS 13.3、iPadOS 13.3、tvOS 13.3、watchOS 6.1.1、macOS Catalina 10.15.2をサポート。</li>
<li>Xcodeをクラッシュさせる可能性がある、ストーリーボードのキャンバスのバグを修正。</li>
<li>追加のバグ修正と安定性の改善。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>11.4</p></td>
<td><p>2020年3月24日</p></td>
<td><ul>
<li>iOS 13.4、iPadOS 13.4、tvOS 13.4、watchOS 6.2、macOS Catalina 10.15.4をサポート。</li>
<li>Interface BuilderとSimulatorが、iPadOSの新しいカーソル機能をサポート。</li>
<li>macOSプロジェクトでApp Storeのユニバーサル購入をサポート。</li>
<li>シミュレータがリモートプッシュ通知をトリガー可能に。</li>
<li>Swiftのテストでは、エラーが発生したコードが強調表示される。</li>
<li>追加のバグ修正と安定性の改善。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>11.4.1</p></td>
<td><p>2020年4月15日</p></td>
<td><ul>
<li>iOS 13.4、iPadOS 13.4、tvOS 13.4、watchOS 6.2、macOS Catalina 10.15.4用をサポート。</li>
<li>バグ修正と安定性の改善。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>11.5</p></td>
<td><p>2020年5月20日</p></td>
<td><ul>
<li>iOS 13.5、iPadOS 13.5、tvOS 13.4、watchOS 6.2、macOS Catalina 10.15.4用をサポート。</li>
<li>Exposure Notification APIをサポート。</li>
<li>バグ修正と安定性の改善。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>11.6</p></td>
<td><p>2020年7月15日</p></td>
<td><ul>
<li>iOS 13.6、iPadOS 13.6、tvOS 13.4、watchOS 6.2、macOS Catalina 10.15.6用をサポート。</li>
<li>macOS SDKにおけるDriverKit APIの機能強化。</li>
<li>バグ修正と安定性の改善。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>11.7</p></td>
<td><p>2020年9月1日</p></td>
<td><ul>
<li>iOS 13.7、iPadOS 13.7、tvOS 13.4、watchOS 6.2、macOS Catalina 10.15.6用をサポート。</li>
</ul></td>
</tr>
</tbody>
</table>

### 12.X

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>12.0</p></td>
<td><p>2020年9月16日</p></td>
<td><ul>
<li>iOS 14、iPadOS 14、tvOS 14、watchOS 7、macOS Catalina 10.15.6用をサポート。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>12.0.1</p></td>
<td><p>2020年9月24日</p></td>
<td><ul>
<li>iOS 14、iPadOS 14、tvOS 14、watchOS 7、macOS Catalina 10.15.6用をサポート。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>12.1</p></td>
<td><p>2020年10月20日</p></td>
<td><ul>
<li>iOS 14.1、iPadOS 14.1、tvOS 14、watchOS 7、macOS Catalina 10.15.6用をサポート。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>12.2</p></td>
<td><p>2020年11月12日</p></td>
<td><ul>
<li>iOS 14.2、iPadOS 14.2、tvOS 14.2、watchOS 7.1、macOS Big Sur 11用をサポート。</li>
</ul></td>
</tr>
</tbody>
</table>

## 脚注

### 注釈

<references group="注">

\[3\]

</references>

### 出典

<references>

\[4\]

</references>

## 関連項目

  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
  - [Apple Developers Tools](../Page/Apple_Developers_Tools.md "wikilink")

## 外部リンク

  -
  -
  -
[Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")

1.
2.
3.  SwiftUIにはiOS 13、watchOS 6、tvOS 13、またはmacOS Catalinaが必要です。SwiftUIのデザインキャンバスを使用するには、秋にリリース予定のmacOS CatalinaでXcodeを実行する必要があります。
4.