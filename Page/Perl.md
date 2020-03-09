> この記事は[Perl](https://ja.wikipedia.org/wiki/Perl)から翻訳されています。


**Perl**（パール）とは、[ラリー・ウォール](https://ja.wikipedia.org/wiki/ラリー・ウォール "wikilink")によって開発された[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。実用性と多様性を重視しており、[C言語](../Page/C言語.md "wikilink")や[sed](https://ja.wikipedia.org/wiki/sed_\(コンピュータ\) "wikilink")、[awk](https://ja.wikipedia.org/wiki/AWK "wikilink")、[シェルスクリプトなど他のプログラミング言語の優れた機能を取り入れている](https://ja.wikipedia.org/wiki/シェル#シェルスクリプト "wikilink")。[ウェブ・アプリケーション](https://ja.wikipedia.org/wiki/ウェブ・アプリケーション "wikilink")、システム管理、テキスト処理などのプログラムを書くのに広く用いられている。

言語処理系としてのperlは[フリーソフトウェア](https://ja.wikipedia.org/wiki/フリーソフトウェア "wikilink")である。[Artistic Licenseおよび](https://ja.wikipedia.org/wiki/Artistic_License "wikilink")[GPLのもとで配布されており](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")、誰でもどちらかのライセンスを選択して利用することができる。[UNIX](https://ja.wikipedia.org/wiki/UNIX "wikilink")や[Windowsなど多くのプラットフォーム上で動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 特徴

  - 強力な[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")処理。[正規表現](https://ja.wikipedia.org/wiki/正規表現 "wikilink")をサポート
  - 日本語をはじめとして世界中の言語を処理可能
  - [連想配列](https://ja.wikipedia.org/wiki/連想配列 "wikilink")（ハッシュ）をサポート
  - 多次元データ構造が利用可能
  - 自由度の高い文法。簡潔にプログラムを記述できる
  - 高い[後方互換](https://ja.wikipedia.org/wiki/後方互換 "wikilink")性を持つ
  - 数多くの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で利用可能
  - プログラムの実行には事前コンパイルは不要
  - [スクリプト言語](https://ja.wikipedia.org/wiki/スクリプト言語 "wikilink")の中では高い処理速度を持つ
  - [Unicode](https://ja.wikipedia.org/wiki/Unicode "wikilink")のサポート
  - モジュールによる拡張が可能
  - 有志によって開発された豊富なモジュール（[CPAN](https://ja.wikipedia.org/wiki/CPAN "wikilink")を参照）
  - [オブジェクト指向](https://ja.wikipedia.org/wiki/オブジェクト指向 "wikilink")プログラミングのサポート
  - [リファレンスカウント方式によるガーベッジコレクション](https://ja.wikipedia.org/wiki/参照カウント "wikilink")
  - [例外処理](https://ja.wikipedia.org/wiki/例外処理 "wikilink")のサポート
  - [クロージャ](https://ja.wikipedia.org/wiki/クロージャ "wikilink")のサポート
  - [リフレクションのサポート](https://ja.wikipedia.org/wiki/リフレクション_\(情報工学\) "wikilink")

## Hello world

``` perl
print "Hello, world!\n";
```

## モジュール

Perlプログラムには、[モジュール](https://ja.wikipedia.org/wiki/モジュール "wikilink")によって機能を付加することができる。たとえば、他のプログラムやネットワークとの通信、各種ファイル形式の取り扱い、数学的な計算など、数多くのモジュールが存在する。PerlにはCPANというモジュールを体系的に管理する[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上のシステムがある。インターネットに接続しているならば、CPANにアクセスして、モジュールをインストールすることが可能である。

### 標準モジュール

Perlには標準で利用できるモジュールが数多く存在する。

  - [base](https://metacpan.org/pod/distribution/base/lib/base.pm) - クラスの継承
  - [Benchmark](https://metacpan.org/pod/distribution/perl/lib/Benchmark.pm) - ベンチマーク
  - [Carp](https://fastapi.metacpan.org/source/SHAY/perl-5.30.1/lib/Carp.pm) - 呼び出し元の観点で例外を発生
  - [Cwd](https://metacpan.org/pod/distribution/PathTools/Cwd.pm) - カレントディレクトリのパスを取得
  - [<Data::Dumper>](https://metacpan.org/pod/distribution/Data-Dumper/Dumper.pm) - 変数の内容を出力
  - [Digest::MD5](https://metacpan.org/pod/distribution/Digest-MD5/MD5.pm) - MD5値
  - [Digest::SHA](https://metacpan.org/pod/distribution/Digest-SHA/lib/Digest/SHA.pm) - SHA-1/224/256/384/512
  - [Encode](https://metacpan.org/pod/distribution/Encode/Encode.pm) - 文字列のエンコード・デコード
  - [utf8](https://metacpan.org/pod/distribution/perl/lib/utf8.pm) - utf8プラグマ
  - [Exporter](https://metacpan.org/pod/distribution/Exporter/lib/Exporter.pm) - 関数のエクスポート
  - [<File::Basename>](https://metacpan.org/pod/distribution/perl/lib/File/Basename.pm) - ファイルのベース名とディレクトリ名の取得
  - [<File::Copy>](https://metacpan.org/pod/distribution/perl/lib/File/Copy.pm) - ファイルの移動とコピー
  - [<File::Path>](https://metacpan.org/pod/distribution/File-Path/Path.pm) - 複数階層のディレクトリの作成と削除
  - [<File::Spec>](https://metacpan.org/pod/distribution/PathTools/lib/File/Spec.pm) - ファイル名に対する移植性のある処理
  - [<File::Temp>](https://metacpan.org/pod/distribution/File-Temp/Temp.pm) - 一時ファイルの生成
  - [FindBin](https://metacpan.org/pod/distribution/perl/lib/FindBin.pm) - スクリプトが存在するディレクトリのパスの取得
  - [Getopt::Long](https://metacpan.org/pod/distribution/Getopt-Long/lib/Getopt/Long.pm) - コマンドライン引数の処理
  - [lib](https://metacpan.org/pod/distribution/lib/lib_pm.PL) - モジュールの検索パスを追加
  - [List::Util](https://metacpan.org/pod/distribution/Scalar-List-Utils/lib/List/Util.pm) - 配列に対する処理
  - [Net::FTP](https://metacpan.org/pod/distribution/libnet/Net/FTP.pm) - FTPクライアント
  - [Scalar::Util](https://metacpan.org/pod/distribution/Scalar-List-Utils/lib/List/Util.pm) - スカラ値のユーティリティ
  - [Storable](https://metacpan.org/pod/distribution/Storable/Storable.pm) - データの直列化
  - [Sys::Hostname](https://metacpan.org/pod/distribution/perl/ext/Sys-Hostname/Hostname.pm) - ホスト名の取得
  - [Time::Piece](https://metacpan.org/pod/distribution/Time-Piece/Piece.pm) - 日付・時刻の扱い
  - [IO::Socket::INET](https://metacpan.org/pod/distribution/IO/lib/IO/Socket/INET.pm) - ソケット

### 代表的なCPANモジュール

  - テキスト処理

:\* [Text::CSV](https://metacpan.org/pod/distribution/Text-CSV/lib/Text/CSV.pm) - CSVファイルの解析

:\* [Text::Diff](https://metacpan.org/pod/distribution/Text-Diff/lib/Text/Diff.pm) - diffコマンド

:\* [Template Toolkit](https://metacpan.org/pod/distribution/Template-Toolkit/lib/Template.pm) - テンプレートシステム

  - データベース

:\* [DBI](https://metacpan.org/pod/distribution/DBI/DBI.pm) - 汎用[データベース](../Page/データベース.md "wikilink")インタフェース

  -

  - Webアプリケーション

:\* [CGI](https://metacpan.org/pod/distribution/CGI/lib/CGI.pm) - CGIプログラミング

:\* [Plack](https://metacpan.org/pod/distribution/Plack/) - [PSGI](https://ja.wikipedia.org/wiki/PSGI "wikilink")のリファレンス実装

:\* [Mojolicious](https://mojolicious.org/) - Webフレームワーク

:\* [Catalyst](https://metacpan.org/pod/distribution/Catalyst-Runtime/lib/Catalyst.pm) - Webアプリケーションフレームワーク

  -

  - Webアクセス

:\* [LWP::UserAgent](https://metacpan.org/pod/distribution/libwww-perl/lib/LWP/UserAgent.pm) - WWWクライアント

  -

  - データ記述言語の処理

:\* [XML::Simple](https://metacpan.org/pod/distribution/XML-Simple/lib/XML/Simple.pm) - XMLをPerlのデータ構造に変換

:\* [XML::LibXML](https://metacpan.org/pod/distribution/XML-LibXML/LibXML.pod) - XMLのサポート

:\* [JSON](https://metacpan.org/pod/distribution/JSON/lib/JSON.pm) - [JSONのサポート](https://ja.wikipedia.org/wiki/JavaScript_Object_Notation "wikilink")

:\* [YAML](https://metacpan.org/pod/distribution/YAML/lib/YAML.pm) - [YAML](https://ja.wikipedia.org/wiki/YAML "wikilink")のサポート

## 歴史

<table>
<caption>Perlの歴史</caption>
<thead>
<tr class="header">
<th></th>
<th></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>1987年12月18日</p></td>
<td><ul>
<li>6台の  機と6台の  機のためのコンフィギュレーション管理制御システムのレポート作成ツールとして誕生した。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>2.0</p></td>
<td><p>1988年6月05日</p></td>
<td><ul>
<li>ヘンリー・スペンサー作の美しい正規表現ライブラリを  風にアレンジし、導入した。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>3.0</p></td>
<td><p>1989年10月18日</p></td>
<td><ul>
<li>バイナリデータを処理できるようになった。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>4.0</p></td>
<td><p>1991年3月21日</p></td>
<td><ul>
<li><p>より  が発売されたのに合わせて公開された。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>5.0</p></td>
<td><p>1994年10月17日</p></td>
<td><ul>
<li>レキシカル変数 my の導入</li>
<li>リファレンスおよびオブジェクト指向に対応。</li>
<li><code>use</code>が導入され追加モジュールの取扱いが大幅に強化された。</li>
<li>strictプラグマの導入</li>
</ul></td>
</tr>
<tr class="even">
<td><p>5.5.0</p></td>
<td><p>1998年7月22日</p></td>
<td><ul>
<li>正規表現の拡張、<code>B::*</code>モジュールによるフックのサポート、<code>qr//</code> 正規表現演算子の追加がなされた。</li>
<li><p>を含む幅広いオペレーティングシステムに移植された。</p></li>
<li>日本語圏で最も重要なことは、このバージョンが  がサポートする最後のバージョンということである。したがって、日本語情報処理において今なお使われている。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>5.6.0</p></td>
<td><p>2000年5月22日</p></td>
<td><ul>
<li><code>our</code>文やウィークリファレンス、<code>warnings</code>プラグマの導入など、言語コアが大きく拡張された。</li>
<li>試験的ながら  のサポートを開始した最初のバージョン。</li>
<li>バージョン番号の構造を変更。サブバージョン（5.6.0の6に相当）が偶数のものが安定版、奇数のものが開発版を意味する。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>5.8.0</p></td>
<td><p>2002年7月18日</p></td>
<td><ul>
<li>5.8系列の最新版は5.8.9（2008年12月14日）。</li>
<li>汎用文字エンコーディング操作モジュール <code>Encode</code> が標準ライブラリに加えられ、および  などの様々な文字エンコーディングに正式に対応した。</li>
<li>スレッドや<code>PerlIO</code>レイヤが導入された。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>5.10.0</p></td>
<td><p>2007年12月18日</p></td>
<td><ul>
<li>公開日は  の公開からちょうど20年目にあたる。</li>
<li>静的変数を宣言する <code>state</code> 文や、<a href="https://ja.wikipedia.org/wiki/switch文" title="wikilink">{{langに相当する</a> <code>given</code> 文、<code>say</code> などの言語拡張が導入された。</li>
<li>新しいキーワードの導入による<a href="https://ja.wikipedia.org/wiki/互換性" title="wikilink">互換性</a>の問題に対処するため、新しいキーワードの導入を <code>feature</code> プラグマで制御できるようになった。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>5.12.0</p></td>
<td><p>2010年4月13日</p></td>
<td><ul>
<li><code>package</code> のバージョン指定構文や未実装部分を表す<code>...</code>演算子（<a href="https://ja.wikipedia.org/wiki/ヤダヤダ演算子" title="wikilink">ヤダヤダ演算子</a>）、後置の <code>when</code> 修飾子などが導入された。</li>
<li>日付と時刻に関するコアモジュールが<a href="https://ja.wikipedia.org/wiki/2038年問題" title="wikilink">2038年問題</a>に対応した。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>5.14.0</p></td>
<td><p>2011年5月14日</p></td>
<td><ul>
<li><p>6.0 にほぼ完全に対応。</p></li>
<li>IPv6サポートの改善。</li>
<li><code>push</code>、<code>pop</code>、<code>unshift</code>、<code>shift</code>、<code>each</code>、<code>keys</code>、<code>values</code> などの配列やハッシュを受け取る関数が、リファレンスを受け取ることができるようになった。</li>
<li><code>package パッケージ名 { ... }</code>構文の追加。</li>
<li>値を破壊せずに戻り値として返す正規表現オプション<code>r</code>が追加。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>5.16.0</p></td>
<td><p>2012年5月20日</p></td>
<td><ul>
<li><code>use バージョン番号</code>文の動作が変更された。以前はスクリプトの実行に必要なPerlのバージョンを示すものだったが、「指定したバージョンよりも新しいバージョンの  で新たに実装された機能を無効化する」という動作になった。</li>
<li><code>__SUB__</code>は現在実行中のサブルーチンに対する参照を返す。</li>
<li><code>feature</code> プラグマで<code>unicode_eval</code>を有効にすると、文字列に対する <code>eval</code> は常に文字列を  として扱う。また<code>evalbytes</code>を有効にすると、引数をバイト列として評価する<code>evalbytes</code>関数が利用できる。</li>
<li><code>substr</code> は、左辺値もしくは潜在的に左辺値とみられるコンテキストで2つもしくは3つの引数付きで呼び出された場合、第一引数を変更する特殊な左辺値スカラを返す。</li>
<li><p>6.1 対応も強化された。</p></li>
<li>デバッガ、<code>CORE</code>名前空間、<code>XS</code>インターフェイスなどでさまざまな機能強化が加わっている。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>5.18.0</p></td>
<td><p>2013年5月18日</p></td>
<td><ul>
<li>実験的機能を利用するための新しい警告カテゴリ<code>experimental::feature_name</code>が追加され、 5.10 で加わったスマートマッチ演算子、レキシカルな<code>$_</code>がそのカテゴリに変更された。</li>
<li>ハッシュの際に使われるシードがランダム化され、<code>keys</code> や <code>values</code>、<code>each</code> といったハッシュを利用する関数が返すキー／値の並び順が実行毎に異なるようになった。</li>
<li><p>6.2 への対応、新しい<code>DTrace</code>プローブの追加、実験的機能としてレキシカルサブルーチンの追加などが行われた。<code>\N{...}</code>表現の扱いがいくつか変わっているほか、垂直タブがホワイトスペースとして扱われなくなっている点など、文字の扱いについていくつかの変更が加わった。</p></li>
<li><code>encoding</code>、<code>CPANPLUS</code>、<code>Log::Message</code>、<code>Log::</code><a href="Message::Config"><code>Message::Config</code></a>、<code>Log::</code><a href="Message::Handlers"><code>Message::Handlers</code></a>、<code>Log::</code><a href="Message::Item"><code>Message::Item</code></a>、<code>Log::</code><a href="Message::Simple"><code>Message::Simple</code></a>、<code>Object::Accessor</code>などが廃止予定のモジュールとなった。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>5.20.0</p></td>
<td><p>2014年5月27日</p></td>
<td><ul>
<li>実験的機能として<code>use feature 'signature'</code>によるサブルーチンシグネチャ、<code>use feature 'postderef'</code>によるPostfix Dereferencingと呼ばれる機能が追加された。Postfix Dereferencingを利用すると、いままで<code>${ $sref }</code>のように表記していたものが<code>$sref-&gt;$*</code>のように表記できるようになる。</li>
<li>新たなスライス表記として、キーと値のペアを戻す<code>%hash{…}</code>と<code>%array[…]</code>というスライス表記が加わった。</li>
<li>subキーワードのprototype属性がサポートされ、プロトタイプパーシングの一貫性も強化された。</li>
<li>64ビットプラットフォーム対応が改善され、Perl配列が2**31以上の要素を保持できるようになった。</li>
<li>正規表現エンジンは2**31以上の文字列に対応できるようになった。</li>
<li><p>6.3 に対応した。</p></li>
<li>コアモジュールとして<code>IO::Socket::IP</code>が追加された。</li>
<li>rand関数の仕様が変更された。</li>
<li>一部のコマンドラインオプションの挙動が変更された。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>5.22.0</p></td>
<td><p>2015年6月1日</p></td>
<td><ul>
<li>ビット単位の演算子が導入された。</li>
<li>ダブルダイアモンド演算子が導入された。</li>
<li>正規表現の<code>\b</code>バウンダリの機能が強化された。</li>
<li>正規表現のキャプチャしない修飾子が追加された。</li>
<li><code>use re 'strict'</code>がサポートされた。</li>
<li>Unicode 7.0がサポートされた。</li>
<li>POSIX 2008のロケール、通貨がサポートされた。</li>
<li>古いプラットフォーム上のUTF-8判定が改善された。</li>
<li>リファレンスのエイリアスがサポートされた。</li>
<li>引数なしのプロトタイプがサポートされた。</li>
<li>サブルーチンの<code>const</code>アトリビュートがサポートされた。</li>
<li><code>fileno</code>にディレクトリハンドルも指定可能になった。</li>
<li>Win32でリスト形式のパイプオープンが可能になった。</li>
<li>リスト代入の繰返し指定が可能になった。</li>
<li><code>Inf</code>と<code>Nan</code>の扱いが強化された。</li>
<li>浮動小数点数の扱いが強化された。</li>
<li><code>Inf</code>と<code>NaN</code>の文字列化は致命的エラーになった。</li>
<li>実験的なCバックトレースAPIがサポートされた。</li>
</ul></td>
</tr>
<tr class="even">
<td><p>5.24.0</p></td>
<td><p>2016年5月9日</p></td>
<td><ul>
<li>サブルーチンと数値計算が高速化された。</li>
<li>Unicode 8.0のサポートされた。</li>
<li>実験的な扱いだった前方デリファレンスが本格サポートされた。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>5.30.0</p></td>
<td><p>2019年5月22日</p></td>
<td><ul>
<li>Unicode 12.1をサポート。</li>
</ul></td>
</tr>
</tbody>
</table>

## エピソード

Perlは当初、[新約聖書](https://ja.wikipedia.org/wiki/新約聖書 "wikilink")の[マタイによる福音書](https://ja.wikipedia.org/wiki/マタイによる福音書 "wikilink")13章46節の「高価な真珠」にちなんで[真珠](https://ja.wikipedia.org/wiki/真珠 "wikilink")を意味する「pearl」と名付けられた。ラリー・ウォールは肯定的な意味を持つ短い名前を選びたいと考えていて、彼によれば3文字および4文字の単語を辞書から探したが良いのが見つからなかったということである。また、彼は妻のグロリアにちなんで名前を付けることも考えたが、家族の会話でまぎらわしいために却下となった。

Perlの正式なリリースの前に、すでに「pearl」という名前のプログラミング言語が存在する\[[http://www.irt.uni-hannover.de/pearl/index_en.html\]ことに気づき、綴りを変更して「Perl」とした。このようにPerlは略語ではなく、もともと意味はないが、あとからいくつかの意味が考えられている。開発者ラリー自身によると](http://www.irt.uni-hannover.de/pearl/index_en.html%5Dことに気づき、綴りを変更して「Perl」とした。このようにPerlは略語ではなく、もともと意味はないが、あとからいくつかの意味が考えられている。開発者ラリー自身によると)、「」（実用的なデータ取得レポート作成言語）という意味を持ち、同時に 「」（病的折衷主義のガラクタ出力装置）\[1\]という少し皮肉な意味も込められている。

## 処理系

Perlという名称の記述においては、若干の注意が必要である。プログラミング言語としてのPerlを示すときは「Perl」というように、頭文字を大文字にして固有名詞であることをはっきりさせる。この「Perl」という表記では処理系のことは含まれない。Perl 5の現在開発されている唯一の処理系は「perl」という、すべて小文字で記述される名前の処理系である。一般に「perlだけがPerlを解釈することができる」という表現がなされる。「PERL」のようにすべてを大文字にするのは誤りである。

このようにPerl 5現在において、Perlとは言語の名前であると同時に唯一の処理系の名前でもある。この処理系はC言語で書かれている。スクリプトは実行前に[仮想機械](https://ja.wikipedia.org/wiki/仮想機械 "wikilink")向けにコンパイルされ、コンパイルされたバイトコードが実行される（ランタイムコンパイル）。そのため、厳密にはインタプリタとは異なる。

[Python](../Page/Python.md "wikilink")のように一旦生成したバイトコードを保存して再利用することは少ないが、これは現在のPerlのランタイムコンパイルが高速で、バイトコードから実行するメリットがあまりないことが理由の一つである。コンパイル済みコードの[再利用としてはむしろ](https://ja.wikipedia.org/wiki/コードの再利用 "wikilink")[mod_perl](https://perl.apache.org/)のような形式が好まれている。

[PAR](https://metacpan.org/release/PAR) (Perl Archive Toolkit) というPerlスクリプトを実行環境ごとアーカイブし、単一のファイルにまとめるためのツールキットも存在する。[JARのPerl版と考えてよい](https://ja.wikipedia.org/wiki/Jar "wikilink")。実行可能ファイルを作ることもできるため、アプリケーションの配布に適する。しかしその場合はPerl実行環境をまるごと含むため、ファイルサイズが大きくなる傾向にある。

Perlの姉妹言語として[Raku](https://ja.wikipedia.org/wiki/Raku "wikilink")が存在する。Rakuは[Parrot](https://ja.wikipedia.org/wiki/Parrot "wikilink")というバーチャルマシンの上で動作する。現在、ParrotCodeへのコンパイルを行うRakudo Starという処理系や[Haskell](https://ja.wikipedia.org/wiki/Haskell "wikilink")で書かれた[Pugs](https://ja.wikipedia.org/wiki/Pugs "wikilink")という処理系などの複数の実装が公開されている。なおRakuはPerlと互換性を持たない。

## Perlが利用されているアプリケーション

Perlが利用されている代表的なWeb アプリケーションや管理ツール。

### Webアプリケーション

  - [Movable Type](https://ja.wikipedia.org/wiki/Movable_Type "wikilink")
  - [TWiki](https://ja.wikipedia.org/wiki/TWiki "wikilink")
  - [Bugzilla](https://ja.wikipedia.org/wiki/Bugzilla "wikilink")
  - [cPanel](https://ja.wikipedia.org/wiki/cPanel "wikilink")

### Webサービス

  - [DuckDuckGo](https://ja.wikipedia.org/wiki/DuckDuckGo "wikilink")

### 管理ツール

  - [git](https://ja.wikipedia.org/wiki/git "wikilink")
  - [openssl](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")
  - [autoconf](https://ja.wikipedia.org/wiki/autoconf "wikilink")
  - [automake](https://ja.wikipedia.org/wiki/Autotools#automake "wikilink")
  - [SpamAssassin](https://ja.wikipedia.org/wiki/SpamAssassin "wikilink")
  - VmwareTools
  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink") innotop

## 脚注

<references />

## 参考文献

  - [ラリー・ウォール](https://ja.wikipedia.org/wiki/ラリー・ウォール "wikilink")、ジョン・オーワント、トム・クリスチャンセン著、[近藤嘉雪](https://ja.wikipedia.org/wiki/近藤嘉雪 "wikilink")訳『プログラミング [Perl](https://www.oreilly.co.jp/books/perl/)』VOLUME 1 (ISBN 4-87311-096-3), 2 (ISBN 4-87311-097-1), [オライリー・ジャパン](https://ja.wikipedia.org/wiki/オライリー・ジャパン "wikilink")、2002年

## 関連項目

  - [ラリー・ウォール](https://ja.wikipedia.org/wiki/ラリー・ウォール "wikilink")
  - [Artistic License](https://ja.wikipedia.org/wiki/Artistic_License "wikilink")
  - [グルー言語](https://ja.wikipedia.org/wiki/グルー言語 "wikilink")
  - [スクリプト言語](https://ja.wikipedia.org/wiki/スクリプト言語 "wikilink")
  - [軽量プログラミング言語](https://ja.wikipedia.org/wiki/軽量プログラミング言語 "wikilink")

## 外部リンク

  -
  - [Perl programming documentation](https://perldoc.perl.org/) - Perlの公式ドキュメント

  - [perldoc.jp](https://perldoc.jp/) - Perlの公式ドキュメントの日本語訳

  - [CPAN](https://www.cpan.org/) - Perlのモジュールの配布を行うサイト

  - [Perl.com](https://www.perl.com/) - [オライリー](https://ja.wikipedia.org/wiki/オライリー "wikilink")によるPerlのウェブサイト

  - [ActivePerl](https://www.activestate.com/products/activeperl/) - [ActiveState](https://ja.wikipedia.org/wiki/ActiveState "wikilink")社のPerlディストリビューション。[Win32版は](https://ja.wikipedia.org/wiki/Windows_API#Win32 "wikilink")[Windows環境で最も利用される](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

  - [Chocolate Perl](https://metacpan.org/release/Perl-Dist-Chocolate) - Perlのディストリビューションのひとつ

  - [Vanilla Perl](http://vanillaperl.com/) - Perlのディストリビューションのひとつ

  - [Strawberry Perl](http://strawberryperl.com/) - Perlのディストリビューションのひとつ

  - [PSGI/Plack](https://plackperl.org/) - [WSGIのPerlによる実装](https://ja.wikipedia.org/wiki/Web_Server_Gateway_Interface "wikilink")

  - [Japan Perl Association](https://japan.perlassociation.org/) - YAPC::Asiaを主催する一般社団法人

[Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Perl](https://ja.wikipedia.org/wiki/Category:Perl "wikilink") [Category:1987年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1987年のソフトウェア "wikilink")

1.  プログラミング Perl VOLUME 1 ISBN 4-87311-096-3