> この記事は[Apache HTTP Server](https://ja.wikipedia.org/wiki/Apache_HTTP_Server)から翻訳されています。


**Apache HTTP Server**（アパッチ エイチティーティーピー サーバ）は、[Apache License](../Page/Apache_License.md "wikilink")2.0の条件でリリースされる[フリーで](../Page/フリーソフトウェア.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の[Webサーバ](../Page/Webサーバ.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。Apache は[Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")の支援のもと、開発者のオープンコミュニティによって開発・保守されている。

Apache HTTP サーバのインスタンスの大部分は [Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")上で動作するが、現在のバージョンは [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") や様々な [Unixライクなシステム上でも動作する](../Page/Unix系.md "wikilink")。過去のバージョンでは、[OpenVMS](../Page/OpenVMS.md "wikilink")、[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、[メインフレーム](../Page/メインフレーム.md "wikilink")への移植を含む他のオペレーティングシステムでも動作した。

元々は [NCSA HTTPdサーバをベースにしていたが](../Page/NCSA_HTTPd.md "wikilink")、NCSAコードの作業が停滞した後、1995 年初頭にApache の開発が始まった。Apache は[World Wide Webの最初の成長において重要な役割を果たし](../Page/World_Wide_Web.md "wikilink")、支配的な HTTP サーバとしてすぐに NCSA HTTPd を追い抜き、1996 年 4 月以来、最も人気のあるサーバであり続けている。2009年には、1億以上のウェブサイトにサービスを提供する最初のウェブサーバーソフトウェアとなった。2020年4月現在、Netcraftの推定では、Apacheは最もアクセスの多い100万のウェブサイトの29.12％のサーバーで利用され、[Nginx](https://ja.wikipedia.org/wiki/Nginx "wikilink")は25.54％で利用されている。W3Techsによると、Apacheは上位1000万サイトの39.5％で利用され、Nginxは31.7％で利用されている。

## 歴史

  - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")
    [Webサーバ](../Page/Webサーバ.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")は[欧州原子核研究機構](../Page/欧州原子核研究機構.md "wikilink") (CERN) の[ティム・バーナーズ＝リー](../Page/ティム・バーナーズ＝リー.md "wikilink")が開発した[CERN httpdと](https://ja.wikipedia.org/wiki/CERN_httpd "wikilink")[米国立スーパーコンピュータ応用研究所](../Page/米国立スーパーコンピュータ応用研究所.md "wikilink") (NCSA) が開発した[NCSA HTTPdの](../Page/NCSA_HTTPd.md "wikilink")2種類があった。NCSA HTTPdは初めてCGIを採用するなど、非常に普及していたが、その後ほとんどメンテナンスが行われなくなり、放置されていた。そこで、何人かの有志が改良とサポートを行うためのグループを作り、自分たちを「**Apache Group**」と名付けた。しかし、彼等もその後プロジェクトに興味を失ってしまい、再度放置されかけた。
  - [1999年](../Page/1999年.md "wikilink")以降
    放置されかけたのち、1999年にユーザーの一人だった[Brian Behlendorfが自分のサーバを使ってユーザーのための](https://ja.wikipedia.org/wiki/Brian_Behlendorf "wikilink")[メーリングリスト](../Page/メーリングリスト.md "wikilink")を立ち上げた。これが現在のApacheソフトウェア財団の母体になっている。ただし、現在のApacheのソースコードはApacheソフトウェア財団によって完全に書き換えられており、NCSA HTTPdのコードは残っていない。

## 特徴

### サポート

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>初版</p></th>
<th><p>最新版</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>scope="row" </p></td>
<td><p>1998-06-06[1]</p></td>
<td><p>2010-02-03 (1.3.42)[2]</p></td>
</tr>
<tr class="even">
<td><p>scope="row" </p></td>
<td><p>2002-04-06[3]</p></td>
<td><p>2013-07-10 (2.0.65)[4]</p></td>
</tr>
<tr class="odd">
<td><p>scope="row" </p></td>
<td><p>2005-12-01[5]</p></td>
<td><p>2017-07-11 (2.2.34)[6]</p></td>
</tr>
<tr class="even">
<td><p>scope="row" </p></td>
<td><p>2012-02-21[7]</p></td>
<td><p>2020-08-07 (2.4.46)[8]</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

2018年3月現在、Apacheの公式ページでは2.4系のみを推奨リリースとしている \[9\]。

1.3系、2.0系、2.2系を含む古い系列は、アーカイブ・サイト\[10\]からダウンロードできる。

### モジュールによる機能追加

Apacheの機能はモジュールを追加することで拡張できる。Apacheの核となる「Core」がまずあり、そこへモジュールを追加して機能を拡張する。モジュール名は慣習的に「mod_XXX」と付けられる。XXXは機能の概要名である。例えば「mod_dir」「mod_alias」「mod_setenvif」などとなる。

モジュールは「[静的リンク](../Page/静的リンク.md "wikilink")」または「[動的リンク](../Page/動的リンク.md "wikilink")」により追加できる。**静的リンク**とは、Apacheの実行ファイルそのものにモジュールを組み込む方式である。つまりApacheとモジュールはバイナリ的に一体化して動作する。**動的リンク**とは、モジュールを別ファイルとして作成し、必要に応じてモジュールのファイルから機能を呼び出す方式である。この機能を「DSO（Dynamic Shared Object＝動的共有オブジェクト）」と呼ぶ。動的リンクの機能を利用するためには、あらかじめ「mod_so」モジュールを静的リンクしておく必要がある。

動的リンクはモジュール機能の呼び出しで静的リンクよりも負荷が高くなる（オーバーヘッドがかかる）デメリットがあるが、再起動のみでモジュールを組み入れたり外したりできるメリットがある。 逆に静的リンクは高速にモジュール機能を呼び出せるが、モジュールを入れたり外すためにはApache本体を再コンパイルする必要がある。

### プロセスの挙動 (MPM)

Apacheは数多くのOSをサポートするために、MPM（マルチ プロセッシング モジュール）という仕組みをとっている。これにより、利用するOSに最適化されたApacheを容易に組み込むことができる。

[Unix系](../Page/Unix系.md "wikilink")においては、[プロセス](../Page/プロセス.md "wikilink")・[スレッドの挙動が異なる](../Page/スレッド_\(コンピュータ\).md "wikilink")3つのMPMが利用できる。

  - prefork
    preforkは「スレッドを使わず、先行して [fork](https://ja.wikipedia.org/wiki/fork "wikilink") を行なうウェブサーバ」である。Apacheは伝統的に親プロセスを1つ持ち、クライアントからリクエストが来ると自分自身をコピーして子プロセスを起動する（これをforkという）。実際の通信は子プロセスが受け持つ。そのため、通信している数だけ子プロセスが起動することになる。この時、クライアントからリクエストを受けたあとでforkするとfork完了までに待ち時間が出来て通信のパフォーマンスが遅くなる。そのため、あらかじめいくつかの子プロセスをforkしておき、forkの待ち時間をなくす方式をとっている。この方式が「prefork」である。すなわち“pre（＝前もって・先行して）”forkしておく、という意味である。
    preforkのメリットは、forkされた子プロセス1つ1つが対応する通信を受け持つため、ある子プロセスが何らかの原因でフリーズしたとしても、他の子プロセスには影響を及ぼすことが無く通信を継続できる。このため安定した通信を行うことが出来る。一方、クライアントが多くなればなるほど子プロセスの数も増えるため、使用メモリ量やCPU負荷が比例的に増大していく。preforkで多数のクライアントをさばくには、それに応じた大量のメモリと高速なCPUが必要となる。
  - worker
    workerは「マルチスレッドとマルチプロセスのハイブリッド型サーバ」である。Apacheの子プロセス1つ1つがマルチスレッドで動作し、スレッド1つが1つのクライアントを受け持つ方式である。すなわち、1つのプロセスがマルチスレッドを利用して複数の通信の面倒を見る。この点で1つのプロセスが1つの通信をみるpreforkとは異なる。また多くの子プロセスを起動せずに済むため、メモリの使用量も減らすことが出来る。
  - event
    eventはworkerの一種でマルチスレッドで動作する。workerとの違いはKeep-Alive（[持続的接続](https://ja.wikipedia.org/wiki/HTTPの持続的接続 "wikilink")）の処理方法である。workerやpreforkは、Keep-Aliveの持続性を保つために一度利用したスレッド・プロセスをそのまま待機させている。しかしクライアントからの接続が持続的に行われる可能性は保証されているわけではないから、待機していること自体が無駄になる可能性もある。そこで、Keep-Aliveの処理を別のスレッドに割り振って通信を処理する。
    この方式は長らく実験的サポートであったが、2.4.1にて正式に採用された\[11\]。

このほか、Netware、OS/2、Windows向けにそれぞれ専用のMPMが用意されている。

## 利用形態

Apacheは、主に[ワールドワイドウェブ上で静的または動的なコンテンツを公開するために使われる](../Page/World_Wide_Web.md "wikilink")。多くの[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")は、Apacheが提供する環境と機能を想定して設計されている。また、Apacheは[LAMP](https://ja.wikipedia.org/wiki/LAMP_\(ソフトウェアバンドル\) "wikilink") ([Linux](../Page/Linux.md "wikilink")、Apache、[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")/[Perl](../Page/Perl.md "wikilink")/[Python](../Page/Python.md "wikilink")) や [LAPP](https://ja.wikipedia.org/wiki/LAPP "wikilink") (Linux、Apache、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")、PHP/Perl/Python) と呼ばれる非常に人気のあるウェブサーバコンポーネントの一つでもある。読み方はそれぞれLAMP（ランプ）、LAPP（ラップ）である。さらに、Apacheはいろいろな商用パッケージ、例えば[Oracle Databaseに組み込まれており](../Page/Oracle_Database.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink") 6.5の標準[Webサーバ](../Page/Webサーバ.md "wikilink")にもなっている。

### 特殊な形態

Apacheでは、[FreeBSD](../Page/FreeBSD.md "wikilink")のカーネルと連動し、最高の性能を引き出す特殊な動作形態をサポートしている\[12\]\[13\]。 これはFreeBSDをHTTPサーバに特化するという運用形態を想定したもので、FreeBSD及びApacheの両者に設定が必要であり、共にインストール直後の標準設定ではサポートされない。

基本的な動作は、Linuxの[TUX web serverやWindowsの](https://ja.wikipedia.org/wiki/TUX_web_server "wikilink")[Internet Information Servicesなどに近い実装であり](../Page/Internet_Information_Services.md "wikilink")、通信バッファのカーネルからの直接的な読込や[kqueue](https://ja.wikipedia.org/wiki/kqueue "wikilink")など多岐にわたり、一部のみ利用ということも可能になっている。

## 脚注

## 関連項目

  - [IBM HTTP Server](https://ja.wikipedia.org/wiki/IBM_HTTP_Server "wikilink")
  - [nginx](https://ja.wikipedia.org/wiki/nginx "wikilink")
  - [Microsoft Internet Information Services](https://ja.wikipedia.org/wiki/Microsoft_Internet_Information_Services "wikilink")
  - [オープンストリートマップ](https://ja.wikipedia.org/wiki/オープンストリートマップ "wikilink") (OpenStreetMap) - Apacheのモジュールmod_tileの機能を利用している。
  - [Webサーバ](../Page/Webサーバ.md "wikilink")

## 外部リンク

  -

[Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1995年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1995年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.