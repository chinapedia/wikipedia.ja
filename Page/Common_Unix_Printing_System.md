> この記事は[Common Unix Printing System](https://ja.wikipedia.org/wiki/Common_Unix_Printing_System)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Cups-1.4-web-interface.png "wikilink") **Common Unix Printing System**（**コモン・ユニックス・プリンティング・システム**）は[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) 用のモジュール化された印刷システムである。普通**CUPS**（**カップス**）と略称される。CUPSは、[Mac OSや](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[Windowsの印刷機構に遅れをとっていたUnix系OSに強力な印刷機能をもたらすことになった](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。CUPSではUnix系OSでプリンタの形式・型ごとに独自に書き上げねばならなかったデバイスドライバの作成が極めて容易になり、過去にUnix系OSが対応していた特殊なラインプリンタと[PostScript](../Page/PostScript.md "wikilink")プリンタのみならず、Macintosh/Windows向けに市販されているプリンタのほぼ全てがUnix系OS上から利用できるようになるとされている。

CUPSを運用しているコンピュータは、[クライアントのコンピュータから印刷ジョブを受け取る](../Page/クライアント_\(コンピュータ\).md "wikilink")[サーバ](../Page/サーバ.md "wikilink")となり、それらのジョブを処理して適切な[プリンタへと送る](https://ja.wikipedia.org/wiki/プリンター "wikilink")。また、その際には[HTTPの](../Page/Hypertext_Transfer_Protocol.md "wikilink")[Basic認証](../Page/Basic認証.md "wikilink")および[Digest認証](../Page/Digest認証.md "wikilink")、[ローカル認証](https://ja.wikipedia.org/wiki/ローカル認証 "wikilink")、128ビットTLS/[SSL暗号化などを用いることもできる](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")。

CUPSはUnixの印刷スプーラとスケジューラ、フィルタ・システム、およびバックエンド・システムからなる。このうち、フィルタ・システムは印刷データをプリンタが理解可能な形式へ変換することを受け持ち、バックエンド・システムはそのデータをプリンタへと送ることを受け持つ。CUPSは印刷ジョブと[キューを取り扱う基盤として](../Page/キュー_\(コンピュータ\).md "wikilink")[IPP](../Page/Internet_Printing_Protocol.md "wikilink") (Internet Printing Protocol) を用いている。またCUPSはUnixで伝統的な[System V形式と](../Page/UNIX_System_V.md "wikilink")[BSD](../Page/BSD.md "wikilink")（バークレー）形式のコマンド・ラインのインターフェースもサポートしており、さらに[SMBプロトコル](https://ja.wikipedia.org/wiki/SMBプロトコル "wikilink")も部分的にサポートしている。CUPSが提供するデバイス・ドライバは、[アドビの](../Page/アドビシステムズ.md "wikilink")[PPD](../Page/PostScript_Printer_Description.md "wikilink") (PostScript Printer Description) 形式のテキスト・ファイルを用いて設定が可能である。CUPSを設定するためCUPS自身はウェブ (HTTP) を用いた組込みのインターフェースを有している。また多くのユーザ・インターフェースがさまざまなプラットフォームに対して用意されており、ESP Print Proといった商用パッケージだけでなく、KUPS、GtkLP、QtKUPS、XPPなどのオープンソースライセンスで開発されているGUIがいくつも存在する。CUPSはmacOS版のみ[プロプライエタリライセンス](../Page/プロプライエタリ・ソフトウェア.md "wikilink")、その他のOS向けには[Apache License](../Page/Apache_License.md "wikilink")\[1\]の元で配布されている。以前は[GNU General Public Licenseと](../Page/GNU_General_Public_License.md "wikilink")[GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink"), Version 2で配布されていた。

## 歴史

CUPSはまず、Easy Software Productsのマイケル・スイート とアンドルー・ゼンフト によって[1999年](../Page/1999年.md "wikilink")の秋に作成された\[2\]。最初のリリース・バージョンが公開されるまでのアルファとベータ・バージョンに2年間を要している。初期にはlpd (line printer daemon) を用いるよう開発努力が傾けられたが、ときとしてプリンタとの相性が悪いために[IPPも代替としてサポートされた](../Page/Internet_Printing_Protocol.md "wikilink")。CUPSはすぐさま、[Red Hat Linuxなどいくつかの](../Page/Red_Hat_Linux.md "wikilink")[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")で標準の印刷システムとして採用された。[アップルコンピュータは](../Page/アップル_\(企業\).md "wikilink")[Mac OS Xのデフォルトの印刷システムとして](https://ja.wikipedia.org/wiki/macOS "wikilink")[2002年](../Page/2002年.md "wikilink")3月にCUPSを採用している\[3\]。2007年2月にアップル社は主たる開発者であるマイケル・スイートを雇用し、CUPSのソース・コードを取得している\[4\]。

## 概要

[150px](https://ja.wikipedia.org/wiki/ファイル:Cups_simple.svg "wikilink") CUPSは、標準的な方法で印刷ジョブをプリンタに送ることを可能とする機構を与えるものである。印刷データはまず*スケジューラ* へと送られ、スケジューラはジョブをプリンタが理解できる形式へと変換するため*フィルタ・システム* に送る。さらにフィルタ・システムはデータを、デバイスやネットワークへと送るための特殊なフィルタである*バックエンド* へと受け渡す。CUPSのシステムはデータをプリンタが理解できる言葉へと変換するのに[PostScript](../Page/PostScript.md "wikilink")と[ラスタ・グラフィックス](https://ja.wikipedia.org/wiki/ラスタ・グラフィックス "wikilink")をフルに活用している。

CUPSの最大の利点は、それが、印刷サーバ上で様々なデータ様式を処理できる標準的でモジュール化された印刷システムであることである。CUPS以前には、それぞれ独自の言語と形式を用いていた様々な市場のプリンタに対応している標準的なプリンタの処理システムは見当たらなかった。例えば、System Vとバークレイの印刷システムは互いの互換性がほとんどなく、しかもプログラムのデータ形式からプリンタが理解できる形式へと変換するための複雑なスクリプトと急場しのぎの手段とを用意する必要があった。さらにこれらはしばしばプリンタへと送られているファイル形式を検出する手段を持たないために、データ列を正しく自動的に変換することができなかった。また中心となるサーバ上ではなく各ワークステーション上でデータの変換を行っていた。

CUPSでは、プリンタのメーカーやドライバの開発者が印刷用サーバで専用に動くドライバを製作することが以前よりもはるかに容易なものとなっている。また、サーバ上で処理が成されることによって、他のUnixの印刷システムで行われていたことと較べネットワークを介する印刷も非常に容易なものとなる。ひとつの利点は[Samba](../Page/Samba.md "wikilink")を用いるときで、プリンタはリモートの[Windowsコンピュータで用いられ](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、しかも一般的なPostScriptドライバをネットワークを介する印刷に用いることができる。

### スケジューラ

*CUPSスケジューラ*は[IPP](../Page/Internet_Printing_Protocol.md "wikilink") (Internet Printing Protocol) もしくはlpd (line printer daemon) プロトコルのどちらかを用いることができる。スケジューラは[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")/1.1のリクエストを解釈し印刷ジョブの管理、サーバの設定、およびCUPS自体の説明資料のためにウェブを用いたインターフェースを提供している。

スケジューラは、IPPとHTTPのどのメッセージがシステムに受け渡せるかを制御するための*承認モジュール* を有している。IPP/HTTPパケットは一旦承認されると、やって来る接続を監視しそれを処理している*クライアント・モジュール* に送られる。クライアント・モジュールはまた、必要に応じてウェブ基盤のプリンタ、「クラス」、ジョブの実行状況のモニタと管理をサポートするための外部CGIプログラムの実行を受け持っている。クライアント・モジュールがリクエストを処理すると、次にデータはさらなる処理のために*IPPモジュール* へと送られる。このモジュールは、クライアントがHTTPサーバ上のアクセス制限または認証を回避することを防ぐために[URI](../Page/Uniform_Resource_Identifier.md "wikilink") (Uniform Resource Identifier) の検証を行う。

スケジューラではプリンタが*クラス* を持つことを認めている。これは複数のプリンタをグループ化するひとつの方法であり、ジョブをあるクラスへと送るような用い方を可能としている。すなわち、スケジューラはクラス内で最初に利用できるプリンタを選び出してジョブをそのプリンタへと送る。*ジョブ・モジュール* は、最終的な変換と印刷のために印刷ジョブをフィルターやバックエンドの処理へと送ることで印刷ジョブを管理する。またそれらフィルターやバックエンドからのステータス・メッセージも監視している。

スケジューラの*コンフィギュレーション・モジュール* はCUPSのデータ構造を初期化するとともに設定ファイルを解析し、CUPSプログラムをスタートさせる。コンフィギュレーション・モジュールは設定ファイルを処理している間はCUPSサービスを停止させ、処理が完了するとサービスを再開させる。

*ログ・モジュール* はアクセス、エラー、ログ・ファイル操作のスケジューラの事象のログを取り扱い、一方*メイン・モジュール* はタイムアウトとクライアントからの接続に対するI/Oリクエストの送出を受け持ち、またシグナルを監視し、必要に応じサーバの設定ファイルの再読み込み、さらに子プロセスのエラーと終了を取り扱う。

スケジューラで用いられているその他のモジュールには、印刷デバイスが理解できる形式に印刷データを変換するときのフィルター処理に用いられる[MIME型と変換データベースを取り扱う](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")*MIMEモジュール* 、[PPD](../Page/PostScript_Printer_Description.md "wikilink") (Postscript Printer Description) ファイルのリストを扱う*PPDモジュール* 、システムで利用可能なデバイスのリストを扱う*デバイス・モジュール* 、CUPS内のプリンタとPPDを扱う*プリンタ・モジュール* がある。

### フィルタ・システム

CUPSの大きな利点のひとつは、様々なデータ形式を印刷サーバ上で処理できるということである。印刷ジョブは一連の*フィルター* を介してプリンタの最終的な言語・形式へと変換される。このデータ形式と変換方法は[MIME型を利用して抽象化されている](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")。CUPSは`mime.types`と`mime.convs`の2つのMIMEデータのファイルを使用する。`mime.types`はCUPSがファイルのMIME型を決定するために用いられ、`mime.convs`はあるMIME型を別のMIME型に処理するためのプログラムを定義している。

例えば、[HTMLファイルを検出するための](../Page/HyperText_Markup_Language.md "wikilink")`mime.types`の行は、

`text/html       html htm \`
`      printable(0,1024) + (string(0,"<HTML>") string(0,"<!DOCTYPE"))`

となっている。これは、ファイルのサフィックス（拡張子）が`html`もしくは`htm`であるか、ファイルのテキストの始めの1KiBが印刷可能な文字からなっていて、かつ`<HTML>`か`<!DOCTYPE`から始まっているなら、ファイルはMIME型text/htmlであるものと見なされることを意味している。一方、`mime.convs`ファイルは以下のような行からなっている。

`text/plain application/postscript 50 texttops`

1番目のカラムと2番目のカラムはともにMIME型であり、それぞれ変換前のMIME型と変換後のMIME型とを表している。3番目のカラムはファイルを変換するために支払うべき「コスト」を表し、フィルタ・システムがファイルを変換するときに別々のフィルタの組合せの中からどれを選ぶかを決定するための評価基準とされる。最後のカラムはデータを変換するためのフィルタ・プログラムを表す。よって、`text/plain`型のファイルはフィルタ`texttops`によってコスト50で`application/postscript`型に変換できることになる。

フィルタ・システムは、プリンタ・キューまたは印刷フィルタの名前、印刷ジョブのジョブ番号、ユーザ名、ジョブ名、印刷部数、その他印刷のオプション、ファイル名（[標準入力](https://ja.wikipedia.org/wiki/標準入力 "wikilink")から[リダイレクトされた場合は不要](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")）の引数とともに入力データを受け取る。その後、上述のようにMIMEデータベースを用いて入力データの型と使用されるフィルタを決定する。例えば、画像データが検出されればそれ用の特定のフィルタで処理され、HTMLのデータならまた別の特定のフィルタで処理される。これらのデータはその後[PostScript](../Page/PostScript.md "wikilink")データに変換されるか、直接ラスタ・データに変換しうる。PostScriptデータへ変換された場合には、*プレフィルタ* と呼ばれるさらなるフィルタが適用され、これは印刷するページ範囲の指定や、複数のページを1ページに埋め込むN-Upモードの設定などプリンタに特定のオプションを加えることができるようにPostScriptデータにたいして別のPostScript変換プログラムを適用する。

プレフィルタによる処理が終わると、PostScriptプリンタを用いている場合にはそのままデータはCUPSのバックエンドに送られ、そうでない場合には（[linuxprinting.orgのFoomaticのような](../Page/Linux_Foundation.md "wikilink")）別のフィルタか[Ghostscript](../Page/Ghostscript.md "wikilink")で処理される。これはPostScriptをプリンタに依存しない中間形式の*CUPS-raster*フォーマット (MIME 型 `application/vnd.cups-raster`) へと変換する。最後にこの中間ラスタ形式はプリンタ個別の形式へと最終フィルタで処理される。

このラスタ形式からのフィルタとしてCUPSにデフォルトで含まれているものは、[PCL](https://ja.wikipedia.org/wiki/Printer_Command_Language "wikilink") (Printer Command Language)、[ESC/P](https://ja.wikipedia.org/wiki/ESC/P "wikilink")または[ESC/P2](https://ja.wikipedia.org/wiki/ESC/P2 "wikilink")、および[Dymo](https://ja.wikipedia.org/wiki/Dymo "wikilink")へのフィルタである。ただし、CUPSで用いることができるいくつかの代替フィルタもある。CUPSの開発元であるEasy Software Productsは独自のCUPSフィルタをリリースしている。Gimp-Printは幅広い範囲の（主として）インクジェット・プリンタに対する高精度なドライバであり、LinuxのTurbo-Printはやはり様々な種類のプリンタに対しての種々のドライバを有している。

### バックエンド

バックエンドはデータをプリンタに送る手段である。CUPSで有効なバックエンドには、[パラレルポート](../Page/パラレルポート.md "wikilink")、[シリアルポート](../Page/シリアルポート.md "wikilink")、および[USBポートのプリンタとともに](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[IPP](../Page/Internet_Printing_Protocol.md "wikilink") (Internet Printing Protocol)、[JetDirect](https://ja.wikipedia.org/wiki/JetDirect "wikilink") (AppSocket)、lpd (line printer daemon)、SMB (Server Message Block) プロトコルを介して処理されるネットワーク・バックエンドがある。

## 互換性

伝統的な印刷コマンドがCUPSでも用いることができるようにCUPSは[System V形式と](../Page/UNIX_System_V.md "wikilink")[BSD](../Page/BSD.md "wikilink")形式の両方の印刷コマンドを与えている。CUPSは伝統的なlpdポートであるポート515を監視し、それを「バックエンド」として取り扱う。CUPSをインストールすると、System Vの印刷システムに対応する`lp`コマンドとBSDの印刷システムに対応する`lpr`コマンドとが互換プログラムとしてインストールされる。これらはCUPSへの標準的なインターフェースとなり、これらの印刷システムに依存する現存するアプリケーションとの最大限の互換性を保つ。

## 注釈

## 外部リンク

  -
  - [Project: Gimp-Print - Top Quality Printer Drivers: Summary](http://sourceforge.net/projects/gimp-print/)

  - [2ch Linux Beginners 印刷関連FAQ集](http://www12.atwiki.jp/linux2ch/pages/50.html)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:プリンター](https://ja.wikipedia.org/wiki/Category:プリンター "wikilink")

1.
2.  Michael Sweet (June 9, 1999), ["A Bright New Future for Printing on Linux"](http://linuxtoday.com/news_story.php3?ltsn=1999-06-09-014-10-NW-SM), *[Linux Today](https://ja.wikipedia.org/wiki/Linux_Today "wikilink")*, および続報記事 Michael Sweet (June 11, 1999), ["The Future Brightens for Linux Printing"](http://linuxtoday.com/news_story.php3?ltsn=1999-06-11-018-10-NW-SM), *Linux Today*
3.  *Easy Software Products*, [CUPS Licensed for Use in Apple Operating Systems\!](http://www.cups.org/articles.php?L68+I10+T+P1+Qapple) ([press release](https://ja.wikipedia.org/wiki/press_release "wikilink")), March 1, 2002
4.  [CUPS Purchased by Apple Inc.](http://www.cups.org/articles.php?L475) ([press release](https://ja.wikipedia.org/wiki/press_release "wikilink")), July 11, 2007