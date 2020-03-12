> この記事は[Standard Performance Evaluation Corporation](https://ja.wikipedia.org/wiki/Standard_Performance_Evaluation_Corporation)から翻訳されています。


**Standard Performance Evaluation Corporation**（**SPEC**、標準性能評価法人）は、コンピュータの公平で意味のある[ベンチマーク](../Page/ベンチマーク.md "wikilink")を作成することを目指して設立された[非営利団体](../Page/非営利団体.md "wikilink")である。SPECは[1988年](../Page/1988年.md "wikilink")に設立され、全ての主要なコンピュータ企業やソフトウェア製造業者などのメンバー企業が資金提供している。SPECのベンチマークはコンピュータシステムの性能評価に今日広く使われていて、その測定結果はSPECのウェブサイト上で公表されている。

そのベンチマークは「現実の」状況をテストすることを目指している。例えば SPECweb2005 は[Webサーバ](../Page/Webサーバ.md "wikilink")の性能評価のために様々なタイプの[HTTPリクエストを並行していくつも行う](../Page/Hypertext_Transfer_Protocol.md "wikilink")。SPEC CPU は[CPU](../Page/CPU.md "wikilink")性能を評価するために、[GCCコンパイラや](../Page/GNUコンパイラコレクション.md "wikilink")[チェスプログラム](../Page/コンピュータチェス.md "wikilink") crafty などのいくつかのプログラムの実行時間を測定する。様々なタスクにはそれぞれ現実での重要性を考慮した重み付けがされており、その重み付けを使用して最終的にひとつのベンチマーク結果を得るようになっている。

SPECベンチマークはプラットフォームに依存しない[プログラミング言語](../Page/プログラミング言語.md "wikilink")（通常、[C言語](../Page/C言語.md "wikilink")または[FORTRAN](../Page/FORTRAN.md "wikilink")）で書かれていて、利用者は自分のプラットフォームで動作する任意のコンパイラでコンパイルすることができる。ただし、ソースコードを変更することはできない。製造業者はSPECベンチマークの結果を改善するためのコンパイラの最適化手法を適用していると言われている。

ベンチマークを使うためには、ライセンスをSPECから購入する必要がある。その費用はテストの種類によって数百ドルから数千ドルまである。ベンチマークには[GPLによりライセンスされるソフトウェアが含まれるため](../Page/GNU_General_Public_License.md "wikilink")、この支払いモデルは[GPL違反であるとして批判されてきた](../Page/GNU_General_Public_License.md "wikilink")。

## ベンチマーク一覧

### 現在のベンチマーク

  - SPEC CPU2006：CPU、メモリ、コンパイラの総合的な性能評価
      - CINT2006 ("[SPECint](https://ja.wikipedia.org/wiki/SPECint "wikilink")")：[整数](../Page/整数.md "wikilink")演算を評価する。コンパイラ、インタープリタ、ワードプロセッサ、チェスプログラムなどを実行。
      - CFP2006 ("[SPECfp](https://ja.wikipedia.org/wiki/SPECfp "wikilink")")：[浮動小数点数](../Page/浮動小数点数.md "wikilink")演算を評価する。物理現象のシミュレーション、三次元グラフィックス、画像処理、化学計算などを実行。
  - SPECweb2005：PHPおよび（または）JSPの性能評価
  - SPECviewperf：[OpenGL](../Page/OpenGL.md "wikilink")三次元グラフィックスシステムの性能評価。実アプリケーションの各種レンダリングタスクを実行。
  - SPECapc：いくつかの一般的な三次元指向のアプリケーションの性能評価
  - SPEC HPC2002：高性能[並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")システムの性能を気象予測や化学計算のプログラムで評価
  - SPEC OMP V3.1：[OpenMP](../Page/OpenMP.md "wikilink")ベースのアプリケーションの性能評価
  - SPECjvm98：[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")の動作するJavaクライアントシステムの性能評価
  - SPECjAppServer2004：Java 2 Enterprise Edition (J2EE)ベースのアプリケーションサーバを中心とした多層システムの性能を評価するベンチマーク
  - SPECjbb2005：三層クライアント・サーバシステムをエミュレートしサーバサイドJavaの性能を評価（主に中間層の評価）
  - SPEC MAIL2001：メールサーバの性能評価。[SMTPと](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")[POPプロトコルを実行](../Page/Post_Office_Protocol.md "wikilink")。
  - SPEC SFS97_R1：[NFSファイルサーバのスループットと応答時間の測定](../Page/Network_File_System.md "wikilink")

### 今後登場予定のベンチマーク

  - SPECappPlatform：Web向けエンタープライズプラットフォームの性能評価（[Java EEと](https://ja.wikipedia.org/wiki/Java_EE "wikilink")[.NET](https://ja.wikipedia.org/wiki/.NET "wikilink")など）
  - SPECimap2003：エンタープライズレベルのメールサーバの性能評価（[SMTPと](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")[IMAP4](https://ja.wikipedia.org/wiki/IMAP4 "wikilink")プロトコル）
  - SPEC MPI：MPI ([Message Passing Interface](../Page/Message_Passing_Interface.md "wikilink")) ベースのアプリケーションの性能評価

### 過去のベンチマーク

  - SPECjAppServer2001
  - SPECjAppServer2002
  - SPECjbb2000
  - SPECweb96
  - SPECweb99
  - SPECweb99_SSL
  - SPEC CPU92
  - SPEC CPU95
  - SPEC CPU2000
  - SPEC HPC96
  - SPEC SFS97

## 日本国内会員

2007年3月現在。アルファベット順。

### 正式会員

  - [富士通](../Page/富士通.md "wikilink")
  - [日立製作所](../Page/日立製作所.md "wikilink")
  - [日本電気](../Page/日本電気.md "wikilink")

### 協賛（準）会員

  - [JAIST](https://ja.wikipedia.org/wiki/JAIST "wikilink")
  - [九州大学](../Page/九州大学.md "wikilink")
  - [会津大学](../Page/会津大学.md "wikilink")
  - [筑波大学](../Page/筑波大学.md "wikilink")

## 外部リンク

  - [Official SPEC website](http://www.spec.org/)（英語）

[Category:ベンチマーク](https://ja.wikipedia.org/wiki/Category:ベンチマーク "wikilink")