> この記事は[Darwin \(オペレーティングシステム\)](https://ja.wikipedia.org/wiki/Darwin_\(オペレーティングシステム\))から翻訳されています。


**Darwin**（ダーウィン）は[アップルが開発する](../Page/アップル_\(企業\).md "wikilink")[Unix系](../Page/Unix系.md "wikilink")の[POSIX](../Page/POSIX.md "wikilink")準拠[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。技術的には[NEXTSTEP](../Page/NEXTSTEP.md "wikilink")から[OPENSTEP](../Page/OPENSTEP.md "wikilink")に続く流れを汲み、[Mach 3.0](../Page/Mach.md "wikilink")+[BSD](../Page/BSD.md "wikilink")をベースとし、一部の機能は他の[BSD](../Page/BSD.md "wikilink")系OSからも取り入れている。Darwinは[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、さらには[watchOS](https://ja.wikipedia.org/wiki/watchOS "wikilink")と[tvOS](https://ja.wikipedia.org/wiki/tvOS "wikilink")の基礎となる部分でもある。

Darwinは[オープンソース](../Page/オープンソース.md "wikilink")及び[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")として公開されており、他のフリーなUnix系同様に特定のライセンス、[Apple Public Source License](https://ja.wikipedia.org/wiki/Apple_Public_Source_License "wikilink") (APSL) 下で入手、インストール、運用が可能であり、[PowerPC](../Page/PowerPC.md "wikilink")ベースの[Macintosh](../Page/Macintosh.md "wikilink")だけでなく、サポートされているハードウェアドライバの問題からハードウェア構成は限定されるが、[Intel Macではない](../Page/Intel_Mac.md "wikilink")[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")機でも動作する。

しかし、この公開されていた[ソースコード](../Page/ソースコード.md "wikilink")では当初Intel Macには対応していなかったためインテル製[CPU](../Page/CPU.md "wikilink")に移行後は[クローズドソース](../Page/クローズドソース.md "wikilink")になるのではないかという憶測も流れたが、Intel Mac発売から半年後に対応のソースコードが公開された。

なお、2005年4月にリリースされた Darwin 8.0以降、インストール用CDイメージは公開されていないが、後継プロジェクト**PureDarwin**のサイトからダウンロードできる。

## テクノロジー

カーネルは**[XNU](../Page/XNU.md "wikilink")**\[1\]と呼ばれ、Machを採用してはいるものの、macOSを動作させる場合には複数のサーバを組み込む必要はない。またパフォーマンス上の問題が懸念されたため、Darwinカーネル自体に[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")構造は採用されていない。

[ドライバ](https://ja.wikipedia.org/wiki/ドライバ "wikilink")モデルには、**[I/OKit](https://ja.wikipedia.org/wiki/I/OKit "wikilink")**と呼ばれる[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")のフレームワークを採用している。NEXTSTEPで採用されたDriverKitの後継のライブラリで、DriverKitの[Objective-C](../Page/Objective-C.md "wikilink")での実装を機能限定版の[C++](../Page/C++.md "wikilink")での実装に置き換えたもの。開発ツールは[Xcode](../Page/Xcode.md "wikilink")に含まれる。

Darwin (macOS) を立ち上げると最初に起動し端末の初期化を行うプロセスは**[launchd](https://ja.wikipedia.org/wiki/launchd "wikilink")**という[デーモンであり](../Page/デーモン_\(ソフトウェア\).md "wikilink")、他のUnix系システムの[init](https://ja.wikipedia.org/wiki/init "wikilink")に相当する機能を担う。またinetd / xinetdと同じようにネットワークのポートを監視したり、[cron](https://ja.wikipedia.org/wiki/cron "wikilink")のように指定時刻ごとにプロセスを立ち上げる機能も担当する（採用は[Darwin 8.0から](../Page/Mac_OS_X_v10.4.md "wikilink")）。

## 歴史

Darwinは[1989年](../Page/1989年.md "wikilink")に最初にリリースされた、[NeXT](../Page/NeXT.md "wikilink")の[NeXTSTEP](https://ja.wikipedia.org/wiki/NeXTSTEP "wikilink") [OS](../Page/OS.md "wikilink")（バージョン4.0からはOPENSTEPとして知られる）に起源を持つ。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")の[Apple](https://ja.wikipedia.org/wiki/Apple "wikilink")によるNeXTの買収後、次期のOSはOPENSTEPをベースに開発されることがアナウンスされた。これは同年に[Rhapsodyとなり](https://ja.wikipedia.org/wiki/Rhapsody_\(オペレーティングシステム\) "wikilink")、[1999年](../Page/1999年.md "wikilink")には、[Mac OS X Server 1.0](https://ja.wikipedia.org/wiki/Mac_OS_X_Server_1.0 "wikilink")、[2000年](../Page/2000年.md "wikilink")には、[Mac OS X](https://ja.wikipedia.org/wiki/Mac_OS_X "wikilink") Public Beta、そして[2001年](../Page/2001年.md "wikilink")にはMac OS X 10.0に開発された。Mac OS Xのコアコンポーネントは、Apple Public Source Licenseの下、Darwinとして[オープンソース](../Page/オープンソース.md "wikilink")でリリースされているが、[Cocoa](../Page/Cocoa.md "wikilink")や[Carbon](../Page/Carbon.md "wikilink")のようなより高次のコンポーネントは[クローズドソース](../Page/クローズドソース.md "wikilink")のままとまっている。

Darwin 8.0.1までのバージョンでは、Appleは、[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")の形で[バイナリ](../Page/バイナリ.md "wikilink")インストーラーを提供していた\[2\]。これはMac OS Xのメジャーリリース後に、[PowerPC](../Page/PowerPC.md "wikilink")と[Intel](https://ja.wikipedia.org/wiki/Intel "wikilink") [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")システムでDarwinをスタンドアロンのOSとしてインストールできるものであった。Darwinは現在、ソースコードとしてのみ利用できる\[3\]。ただしこれは、[ARM](https://ja.wikipedia.org/wiki/ARM "wikilink")アーキテクチャによるものを除いてであり、ARM向けDarwinは[iOS](https://ja.wikipedia.org/wiki/iOS "wikilink")、[watchOS](https://ja.wikipedia.org/wiki/watchOS "wikilink")、[tvOS](https://ja.wikipedia.org/wiki/tvOS "wikilink")から分離されてはリリースされていない。ただし、趣味的な開発者が公式のDarwinのソースコードをARMにポートした*winocm*がある\[4\]。

## リリース履歴

以下は主なDarwinのリリースと、それに対応するmacOS (Mac OS X / OS X) の表である。\[5\] 対応するmacOSは異なる日にリリースされたかもしれないことに留意し、それらのリリース日についてはmacOSの個別ページを参照。

<table>
<thead>
<tr class="header">
<th><p>|バージョン</p></th>
<th><p>|リリース日</p></th>
<th><p>|対応するリリース</p></th>
<th><p>|説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0.1</p></td>
<td><p>1999年3月16日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Mac_OS_X_Server_1.0" title="wikilink">Mac OS X Server 1.0</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.0.2</p></td>
<td><p>1999年11月10日</p></td>
<td><p>Mac OS X DP2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.1</p></td>
<td><p>2000年4月5日</p></td>
<td><p>Mac OS X DP4</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.2.1</p></td>
<td><p>2000年11月15日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Mac_OS_X_Public_Beta" title="wikilink">Mac OS X Public Beta</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.3.1</p></td>
<td><p>2001年4月13日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.0.md" title="wikilink">Mac OS X v10.0</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.4.1</p></td>
<td><p>2001年10月2日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.1.md" title="wikilink">Mac OS X v10.1</a></p></td>
<td><p>"起動時間、リアルタイムスレッド、スレッド管理、キャッシュフラッシング、プリエンプションハンドリング"に対するパフォーマンスの改善。<a href="../Page/Server_Message_Block.md" title="wikilink">SMB</a>、<a href="https://ja.wikipedia.org/wiki/Wget" title="wikilink">Wget</a>を置き換える<a href="https://ja.wikipedia.org/wiki/cURL" title="wikilink">cURL</a>のサポート。[6]</p></td>
</tr>
<tr class="odd">
<td><p>6.0.1</p></td>
<td><p>2002年9月23日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.2.md" title="wikilink">Mac OS X v10.2</a> <small>(Darwin 6.0.2)</small></p></td>
<td><p><a href="../Page/GNUコンパイラコレクション.md" title="wikilink">GCCを</a>2から3.1にアップグレード、 <a href="https://ja.wikipedia.org/wiki/IPv6" title="wikilink">IPv6</a>と<a href="https://ja.wikipedia.org/wiki/IPSec" title="wikilink">IPSec</a>のサポート、mDNSResponder service discovery<a href="../Page/デーモン_(ソフトウェア).md" title="wikilink">デーモン</a>(<a href="../Page/Bonjour.md" title="wikilink">Rendezvous</a>)、<a href="../Page/Common_Unix_Printing_System.md" title="wikilink">CUPS</a>, <a href="../Page/Ruby.md" title="wikilink">Ruby</a>, <a href="../Page/Python.md" title="wikilink">Python</a>の追加、<a href="https://ja.wikipedia.org/wiki/HFS+" title="wikilink">HFS+</a>での<a href="../Page/ジャーナリングファイルシステム.md" title="wikilink">ジャーナリングのサポート</a><small>(Darwin 6.2)</small>、プログラムをより速く起動するためのアプリケーションプロファイル("pre-heat files")の追加。[7]</p></td>
</tr>
<tr class="even">
<td><p>7.0</p></td>
<td><p>2003年10月24日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.3.md" title="wikilink">Mac OS X v10.3</a></p></td>
<td><p><a href="../Page/FreeBSD.md" title="wikilink">FreeBSD</a> 5に対応したBSDレイヤー、自動<a href="../Page/デフラグメンテーション.md" title="wikilink">デフラグメンテーション</a>、hot-file clustering、HFS+でのcase sensitivityオプション、read-onlyな<a href="../Page/NT_File_System.md" title="wikilink">NTFSのサポート</a>。デフォルトのシェルを<a href="https://ja.wikipedia.org/wiki/tcsh" title="wikilink">tcsh</a>から<a href="https://ja.wikipedia.org/wiki/bash" title="wikilink">bash</a>に変更。<small>(Darwin 7.9)</small>.[8]</p></td>
</tr>
<tr class="odd">
<td><p>8.0</p></td>
<td><p>2005年4月29日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.4.md" title="wikilink">Mac OS X v10.4</a><br />
Mac OS X for <a href="../Page/Apple_TV.md" title="wikilink">Apple TV</a> <small>(Darwin 8.8.2)</small></p></td>
<td><p>安定的なカーネル<a href="../Page/アプリケーションプログラミングインタフェース.md" title="wikilink">プログラミングインターフェース</a>、よりきめ細かいカーネル<a href="../Page/ロック_(情報工学).md" title="wikilink">ロック</a>、64ビットBSDレイヤー、<a href="https://ja.wikipedia.org/wiki/launchd" title="wikilink">launchd</a>サービス管理フレームワーク、<a href="https://ja.wikipedia.org/wiki/拡張ファイル属性" title="wikilink">拡張ファイル属性</a>、<a href="../Page/アクセス制御リスト.md" title="wikilink">アクセス制御リスト</a>、<a href="https://ja.wikipedia.org/wiki/Cp_(UNIX)" title="wikilink">cpや</a><a href="../Page/Mv_(UNIX).md" title="wikilink">mvなどのコマンドを拡張属性や</a><a href="../Page/リソースフォーク.md" title="wikilink">リソースフォーク</a>が保持できるようにアップデート。[9]</p></td>
</tr>
<tr class="even">
<td><p>9.0</p></td>
<td><p>2007年10月26日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/iOS_(アップル)" title="wikilink">iOS 1.0</a> <small>(Darwin 9.0.0d1)</small><br />
<a href="../Page/Mac_OS_X_v10.5.md" title="wikilink">Mac OS X v10.5</a></p></td>
<td><p>完全な<a href="../Page/POSIX.md" title="wikilink">POSIX</a>準拠、階層的プロセス<a href="../Page/スケジューリング.md" title="wikilink">スケジューリング</a>モデルの改善、<a href="../Page/動的メモリ確保.md" title="wikilink">動的メモリ確保</a>の<a href="../Page/ページング方式.md" title="wikilink">スワップファイル</a>、（<a href="../Page/ファイル_(コンピュータ).md" title="wikilink">ファイルや</a><a href="../Page/プロセス.md" title="wikilink">プロセス</a>に対する）動的なリソース制限、プロセスの<a href="../Page/サンドボックス_(セキュリティ).md" title="wikilink">サンドボックス化</a>、<a href="https://ja.wikipedia.org/wiki/アドレス空間配置のランダム化" title="wikilink">アドレス空間配置のランダム化</a>、<a href="../Page/DTrace.md" title="wikilink">DTrace</a> tracing framework、<a href="../Page/ファイルシステム.md" title="wikilink">ファイルシステム</a>イベントデーモン、<a href="../Page/ディレクトリ.md" title="wikilink">ディレクトリ</a><a href="../Page/ハードリンク.md" title="wikilink">ハードリンク</a>、<a href="../Page/Apache_HTTP_Server.md" title="wikilink">Apache</a> 1.3と<a href="../Page/PHP_(プログラミング言語).md" title="wikilink">PHP</a> 4をそれぞれApache 2.2とPHP 5にアップデート、<a href="../Page/ZFS.md" title="wikilink">ZFS</a>のサポート。[10]</p></td>
</tr>
<tr class="odd">
<td><p>10.0</p></td>
<td><p>2009年8月28日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.6.md" title="wikilink">Mac OS X v10.6</a></p></td>
<td><p>PowerPCの公式サポートの終了（ただしカーネルなどいくつかの<a href="../Page/ファットバイナリ.md" title="wikilink">ファットバイナリ</a>がPPCイメージをまだ含んでいる）、64ビットのカーネルとドライバ、<a href="https://ja.wikipedia.org/wiki/Grand_Central_Dispatch" title="wikilink">libdispatch</a><a href="https://ja.wikipedia.org/wiki/タスク並列性" title="wikilink">タスク並列化フレームワーク</a>、<a href="../Page/OpenCL.md" title="wikilink">OpenCL</a>ヘテロジニアスコンピューティングフレームワーク、<a href="../Page/C言語.md" title="wikilink">C言語</a>のBlocks（<a href="../Page/クロージャ.md" title="wikilink">クロージャ</a>を作るために<a href="../Page/ラムダ計算.md" title="wikilink">ラムダ式のような構文を用いる非標準の言語拡張</a>）のサポート、HFS+における透過的な<a href="https://ja.wikipedia.org/wiki/ファイル圧縮" title="wikilink">ファイル圧縮</a>。[11]</p></td>
</tr>
<tr class="even">
<td><p>10.1.0</p></td>
<td><p>2009年9月10日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.6.md" title="wikilink">Mac OS X v10.6.1</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>10.2.0</p></td>
<td><p>2009年11月9日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.6.md" title="wikilink">Mac OS X v10.6.2</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>10.3.0</p></td>
<td><p>2010年3月29日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/iOS_(アップル)" title="wikilink">iOS 4.0</a> <small>(Darwin 10.3.1)</small><br />
<a href="../Page/Mac_OS_X_v10.6.md" title="wikilink">Mac OS X v10.6.3</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>10.4.0</p></td>
<td><p>2010年6月15日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.6.md" title="wikilink">Mac OS X v10.6.4</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>10.5.0</p></td>
<td><p>2010年11月11日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.6.md" title="wikilink">Mac OS X v10.6.5</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>10.6.0</p></td>
<td><p>2011年1月6日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.6.md" title="wikilink">Mac OS X v10.6.6</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>10.7.0</p></td>
<td><p>2011年3月21日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.6.md" title="wikilink">Mac OS X v10.6.7</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>10.8.0</p></td>
<td><p>2011年6月23日</p></td>
<td><p><a href="../Page/Mac_OS_X_v10.6.md" title="wikilink">Mac OS X v10.6.8</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>11.0.0</p></td>
<td><p>2011年7月20日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Mac_OS_X_Lion" title="wikilink">OS X v10.7</a></p></td>
<td><p>XNUがPPCをサポートせず（i386, x86_64のためだけのファットバイナリ）、x86_64プロセッサを必要とする。アプリケーションのサンドボックス化の改善。</p></td>
</tr>
<tr class="odd">
<td><p>11.1.0</p></td>
<td><p>2011年8月16日</p></td>
<td><p>OS X v10.7.1</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>11.4</p></td>
<td><p>2012年5月9日</p></td>
<td><p>OS X v10.7.4</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>11.4.2</p></td>
<td><p>2012年9月12日</p></td>
<td><p>OS X v10.7.5</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>12.0</p></td>
<td><p>2012年2月16日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/OS_X_Mountain_Lion" title="wikilink">OS X v10.8</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>13.0.0</p></td>
<td><p>2013年6月11日</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/OS_X_Mavericks" title="wikilink">OS X v10.9</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>13.1</p></td>
<td><p>2014年2月25日</p></td>
<td><p>OS X v10.9.2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>13.3.0</p></td>
<td><p>2014年6月30日</p></td>
<td><p>iOS 7<br />
OS X v10.9.4</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>14.0.0</p></td>
<td><p>2014年9月18日</p></td>
<td><p>iOS 7.1-7.1.2, iOS 8<br />
<a href="https://ja.wikipedia.org/wiki/OS_X_Yosemite" title="wikilink">OS X v10.10</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>14.5.0</p></td>
<td><p>2015年8月13日</p></td>
<td><p>OS X v10.10.5</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>15.0.0</p></td>
<td><p>2015年9月16日</p></td>
<td><p>iOS 9.0<br />
<a href="https://ja.wikipedia.org/wiki/OS_X_El_Capitan" title="wikilink">OS X v10.11.0</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>15.4.0</p></td>
<td><p>2016年3月21日</p></td>
<td><p>OS X v10.11.4</p></td>
<td></td>
</tr>
</tbody>
</table>

Mac OS X v10.1.1のリリースで、バージョン番号がDarwin 1.4.1から5.1へ飛んでいるのは、DarwinをmacOSのバージョンとビルド番号の体系に結びつけたためである。macOSのビルド番号の体系では、すべてのバージョンが固有のビルド番号ではじまり、macOSのバージョンの全体の中のどの部分であるかわかるようになっている。Mac OS X v10.0は4ではじまるビルド番号があり、10.1には5ではじまるビルド番号があった（初期のビルド番号は開発者リリースを表していた）。Darwinのバージョンにあるピリオド以下の番号は、Mac OS Xのバージョンにある二つめのピリオド以下の番号とおなじである。Mac OS X v10.1.1（バージョン番号が飛んだときのバージョン）の場合は、ビルド5M28および10.1.1リリースであり、バージョン番号の5.1はこれに由来する。\[12\]

[ターミナルで](../Page/ターミナル_\(macOS\).md "wikilink")[`uname`](https://ja.wikipedia.org/wiki/uname "wikilink")`  -r `のコマンドを実行するとDarwinのバージョン番号が表示され、`uname -v`とするとDarwinのバージョン番号をふくんだ[XNU](../Page/XNU.md "wikilink")のビルドバージョンが表示される。

## 派生プロジェクト

Darwinは[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であるため、修正や強化を目的とする多くのプロジェクトがある。

### OpenDarwin

[thumb](https://ja.wikipedia.org/wiki/ファイル:GNOME_2_running_on_openDarwin_\(2004\).png "wikilink")。\]\] OpenDarwinはDarwinシステムをもとにしたコミュニティ主導のOSである。[アップルの開発者とフリーソフトウェアコミュニティとの協調を高めることを目指して](../Page/アップル_\(企業\).md "wikilink")、2002年4月にアップルと[Internet Systems Consortiumによって設立された](https://ja.wikipedia.org/wiki/Internet_Systems_Consortium "wikilink")。このプロジェクトはアップルによるDarwinのリリースに恩恵を与えたが、しかし独立したDarwin OSを作成する試みは達成できず、プロジェクトは停止した。\[13\]

### PureDarwin

2007年、[PureDarwin](http://www.puredarwin.org)プロジェクトがOpenDarwinの後継としてはじまり、現在Darwin 9にもとづいたリリースの制作が進められている。「PureDarwin XMas」と呼ばれる、Darwin 9にもとづいたデベロッパープレビューが入手できる。このリリースは[X11](../Page/X_Window_System.md "wikilink")、[DTrace](../Page/DTrace.md "wikilink")、[ZFS](../Page/ZFS.md "wikilink")をもつ。\[14\] 「PureDarwin nano」は最小限のコンポーネントだけをもつ、別のリリースである。

### その他

  - [MacPorts](https://ja.wikipedia.org/wiki/MacPorts "wikilink")（かつてのDarwinPorts）、[Fink](https://ja.wikipedia.org/wiki/Fink "wikilink")、[HomebrewはUNIXプログラムをDarwin](https://ja.wikipedia.org/wiki/Homebrew_\(パッケージ管理システム\) "wikilink") OSに移植し、[パッケージ管理を提供する](../Page/パッケージ管理システム.md "wikilink")、よく知られたプロジェクトである。さらに、[RPM](../Page/RPM_Package_Manager.md "wikilink")、[pkgsrc](https://ja.wikipedia.org/wiki/pkgsrc "wikilink")、[Portage](../Page/Portage.md "wikilink")などいくつかの標準的なUNIXパッケージ管理システムもDarwin portsをもっている。これらの中にはベースとなるシステムに干渉しないよう、独自の名前空間で動くものもある。
  - [GNU-Darwin](https://ja.wikipedia.org/wiki/GNU-Darwin "wikilink")はフリーソフトウェアのパッケージをDarwinに移植するプロジェクトである。
  - [Darwine](https://ja.wikipedia.org/wiki/Darwine "wikilink")プロジェクトは[Wine](../Page/Wine.md "wikilink")の移植で、[Microsoft WindowsソフトウェアをDarwin上で実行できるようにする](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。
  - [SEDarwin](https://ja.wikipedia.org/wiki/SEDarwin "wikilink")は[TrustedBSD](https://ja.wikipedia.org/wiki/TrustedBSD "wikilink")の[強制アクセス制御](https://ja.wikipedia.org/wiki/強制アクセス制御 "wikilink")フレームワークと、[SELinuxフレームワークの一部をDarwinに移植する](../Page/Security-Enhanced_Linux.md "wikilink")。\[15\] これは[Mac OS X v10.5に組み込まれた](../Page/Mac_OS_X_v10.5.md "wikilink")。\[16\]
  - [Darbat](https://ja.wikipedia.org/wiki/Darbat "wikilink")プロジェクトは[L4マイクロカーネルへのDarwinの実験的な移植である](../Page/L4マイクロカーネルファミリー.md "wikilink")。既存のDarwinバイナリと互換であることを目指している。\[17\]
  - ドライバのサポートに主眼を置いたさまざまなプロジェクトがある。ワイヤレスドライバ、\[18\]\[19\] 有線[NICドライバ](../Page/ネットワークカード.md "wikilink")、\[20\]\[21\]\[22\] モデムドライバ、\[23\] カードリーダ、\[24\] [ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")や[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")ファイルシステム\[25\]\[26\] など。

## 脚注

<references/>

## 外部リンク

  - [AppleのOpen Sourceページ](http://developer.apple.com/opensource/index.html)
  - [Darwin Releases](http://www.opensource.apple.com/darwinsource/)
  - [Apple Public Source License](http://www.opensource.apple.com/apsl/)
  - [Source Browser](https://opensource.apple.com/static/iso/)
  - [Mac OS Forge](http://www.macosforge.org/)
  - [PureDarwin](http://www.puredarwin.org/)

[Category:アップルのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:アップルのオペレーティングシステム "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:1999年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1999年のソフトウェア "wikilink")

1.  X is Not Unixの略とされる。
    [Porting UNIX/Linux Applications to Mac OS X: Glossary](http://developer.apple.com/documentation/Porting/Conceptual/PortingUnix/glossary/chapter_998_section_1.html)
2.
3.
4.
5.  ["Darwin Releases."](http://www.opensource.apple.com/darwinsource/) [Apple Developer Connection](../Page/Apple_Developer_Connection.md "wikilink"). Retrieved on 2007-10-24.
6.  ["Technical Note TN2029: Mac OS X v10.1."](http://developer.apple.com/technotes/tn/tn2029.html) [Apple Developer Connection](../Page/Apple_Developer_Connection.md "wikilink"). Retrieved on 2008-06-02.
7.  [Siracusa, John](https://ja.wikipedia.org/wiki/John_Siracusa "wikilink") (September 5, 2002). ["Mac OS X 10.2 Jaguar."](http://arstechnica.com/reviews/os/macosx-10-2.ars) *[Ars Technica](https://ja.wikipedia.org/wiki/Ars_Technica "wikilink")*. Retrieved on 2008-05-31.
8.  Siracusa, John (November 9, 2003). ["Mac OS X 10.3 Panther."](http://arstechnica.com/reviews/os/macosx-10-3.ars) *[Ars Technica](https://ja.wikipedia.org/wiki/Ars_Technica "wikilink")*. Retrieved on 2008-05-31.
9.  Siracusa, John (April 28, 2005). ["Mac OS X 10.4 Tiger."](http://arstechnica.com/reviews/os/macosx-10-4.ars) *[Ars Technica](https://ja.wikipedia.org/wiki/Ars_Technica "wikilink")*. Retrieved on 2008-05-30.
10. Siracusa, John (October 28, 2007). ["Mac OS X 10.5 Leopard: the Ars Technica review."](http://arstechnica.com/reviews/os/mac-os-x-10-5.ars) *[Ars Technica](https://ja.wikipedia.org/wiki/Ars_Technica "wikilink")*. Retrieved on 2008-05-30.
11. Siracusa, John (August 31, 2009). ["Mac OS X 10.6 Snow Leopard: the Ars Technica review."](http://arstechnica.com/apple/reviews/2009/08/mac-os-x-10-6.ars) *[Ars Technica](https://ja.wikipedia.org/wiki/Ars_Technica "wikilink")*. Retrieved on 2009-11-29.
12. Prabhakar, Ernie (November 9, 2001). ["Darwin Version - New Scheme in Software Update 1."](http://lists.apple.com/archives/darwin-development/2001/Nov/msg00189.html) Apple Mailing Lists. Retrieved on 2008-06-02.
13. OpenDarwin Core Team and Administrators (July 25, 2006). ["OpenDarwin Shutting Down."](http://web.archive.org/web/20070409155747/http://www.opendarwin.org/en/news/shutdown.html) OpenDarwin Project. Retrieved on 2007-04-16.
14. [PureDarwin Download Page](http://www.puredarwin.org/downloads).
15.
16.
17.
18.
19.
20.
21.  *Project inactive since 2006-03-15.*
22.
23.
24.
25.
26.