> この記事は[XCute](https://ja.wikipedia.org/wiki/XCute)から翻訳されています。


**XCute**（エックスキュート） は、[Microsoft Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink") をベースに開発する[Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")[サーバ](../Page/サーバ.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")。

## 表記

マイクロラボのウェブサイトでは「X・Cute」「Xcute」「XCute」の表記が混在しており統一されていないように見受けられるが、製品ロゴには「X・Cute」と「X」と「Cute」の間に中点「・」が入る。文章中に表記される場合は概ね「XCute」とされており、「・」は入らず「C」は大文字である。 2009年7月に商標登録されている。\[1\]

## 概要

[Excelのワークシートに作成した画面に対し](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、[データベース](../Page/データベース.md "wikilink")の値を展開するセル位置を定義することで[プログラミング言語](../Page/プログラミング言語.md "wikilink")を使用せず[Webアプリケーションを開発できる](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")。

Excelのワークシートに作成した画面を「ひな型」と呼び、データベースを展開するセル位置を決める作業を「マッピング」と呼んでいる。

接続できるデータベースは、[Oracle Databaseや](../Page/Oracle_Database.md "wikilink")[Microsoft SQL Serverなどの](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[ODBC対応データベースと](../Page/Open_Database_Connectivity.md "wikilink")、[Microsoft AccessのMDB形式のファイルに対応しており](../Page/Microsoft_Access.md "wikilink")、多くのデータベースソフトウェアと接続可能である。 また、バージョン10からはOracle、SQL Server、[Db2において各データベースに特化したネイティブ接続に対応しており高速なデータアクセスを実現している](../Page/IBM_Db2.md "wikilink")。

「ひな型」に作成した画面はそのまま[HTML化されるため](../Page/HyperText_Markup_Language.md "wikilink")、グラフやピボットテーブルを使用したグラフィカルな画面もWeb化でき、Excelの自由度と相まって独自の社内Webシステムを開発・運用するツールとして多くの企業で使用されている。\[2\] しかしその反面、社内システムとして閉鎖的に使われることが多いため、XCuteの知名度はあまり高くない。 また、XCuteの開発手法は[プログラミング言語](../Page/プログラミング言語.md "wikilink")での開発手法と大きく異なり、[Javaや](../Page/Javaプラットフォーム.md "wikilink")[PHPを使い慣れた](../Page/PHP_\(プログラミング言語\).md "wikilink")[プログラマ](../Page/プログラマ.md "wikilink")には敬遠されることもある。 Excelを使用しているとはいえ、実態はIF関数などを使用した条件分岐でロジックを組み立てる必要があり、広い意味ではプログラミング言語に近い考え方であると言える

とはいえ作成する機能・画面によってはプログラミングコードを使った開発の10倍以上の開発効率があるという開発事例\[3\]も報告されており、使い所を間違わなければ非常に有効なソフトウェアと言える。

また、マイクロラボではエンドユーザコンピューティングを前面に打ち出し販売を展開しているが、XCuteを使用したソリューション販社も多く存在し、数千万円に及ぶ規模の案件で使用されることもある。\[4\]

開発は株式会社マイクロラボ代表取締役[宮森勝彌](https://ja.wikipedia.org/wiki/宮森勝彌 "wikilink")。 マイクロラボが[東京電力](https://ja.wikipedia.org/wiki/東京電力 "wikilink")のソフトウェアを請け負い開発していた頃、当時のパソコンに必ずインストールされていた[ジャストシステム](../Page/ジャストシステム.md "wikilink")のワードプロセッサ[一太郎](../Page/一太郎.md "wikilink")を[インタフェースにデータベースと入出力する仕組みを開発した](../Page/インタフェース_\(情報技術\).md "wikilink")。 時代の流れとともに、一太郎からプラットフォームをExcelに移しXCuteの原型であるProles（プログラミングレスが語源）に発展し、現在のXCuteに至っている。

## 特徴

まず第一にExcelをベースにするため、プログラミングコードを記述する必要が無い。そのためプログラミングの経験がない者でもWebアプリケーションを手軽に開発できる。 数値の計算や文字列の操作、条件の分岐などもExcelのシート関数で制御することで実現する。 [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")に送出するHTMLの生成は基本的にExcelのHTML生成エンジンを使用しているが、ExcelのHTML生成機能で表現できないフォームやテキストエリアなどのHTMLタグは開発者が記述する必要があり、それらのタグをひな型の特定の位置に記述するよう決められている。 これは「タグ差し込み機能」と呼ばれ、自由なHTMLタグを記述できるためフレームやスタイルを使ったデザインを重視した画面を作成したり、JAVAスクリプトを組み合わせることも可能である。 なお、XCuteのユーザは必ずしもWebシステムの開発に精通した者ばかりではないため、XCute Ver8から「ナビゲーション機能」が追加されタグ差し込みを補助する工夫がされている。

Excelをベースに開発するところから簡単なアプリケーションしか作れないと思われる側面もあるが、親子孫といった階層構造をもつデータの表現やクロス集計の入出力が可能であるなどDBツールとしての実力もかなり高い。

他にもWebアプリケーションを開発する上で必要な機能が用意されている

  - メールの送受信
  - バイナリファイルの添付
  - Excelファイルのダウンロード
  - 排他機能
  - 負荷分散機能
  - [Cookie対応](../Page/HTTP_cookie.md "wikilink")
  - [SSL対応](../Page/Transport_Layer_Security.md "wikilink")
  - マクロ（Excel VBA）の実行
  - いたずら（[DoS攻撃](../Page/DoS攻撃.md "wikilink")・不正コード投入）防止機能

## ExcelOpen

Excelのワークシートをインタフェースにしてデータの入出力を行う機能がExcelOpen機能である。 通常Webアプリケーションのインタフェースには[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")を使用するが、ウェブブラウザの中に操作性の良いインタフェースを作成するためにはjavaスクリプト等のプログラムを使用することになる。 しかしExcelと同等の仕組みを作成することは困難であり、それならばExcel自体を入出力のインタフェースにしてしまおうという考え方である。データの閲覧はXCuteサーバからExcelのブックを配信し、入力はセルの値のみをXcuteサーバに送る仕組みとすることで機能面とセキュリティ面の両立を図っている。 Excelの持つ機能をそのまま使用していることから、数式や入力規則、印刷範囲やマクロなどExcel固有の機能を組み合わせた多機能なインタフェースを作成することができるが、クライアントにExcelがインストールされていないと利用できないことや、Excelのバージョンによる機能差が生じる場合があるなど留意すべき点もある。

## 歴史

当初は、[Microsoft Excelと](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")[データベース](../Page/データベース.md "wikilink")のデータを入出力する[デスクトップアプリケーション](https://ja.wikipedia.org/wiki/デスクトップアプリケーション "wikilink")として開発された。 Webアプリケーションの将来性を見越し、[1999年](../Page/1999年.md "wikilink")、Excel 2000のHTML生成機能を利用したWebアプリケーションサーバソフトウェアに方針を転換した。 その後、1-2年に1度のペースでバージョンアップを行い現在に至っている。 バージョンアップでの主な変更は次の通り。

  - XCute Ver7

<!-- end list -->

  -
    新入力規則
      -
        Excelの書式や入力規則を設定したひな形を、以前のバージョンより忠実にHTML化できるようになる。

<!-- end list -->

  - XCute Ver8

<!-- end list -->

  -
    XCuteナビゲーション　
      -
        HTMLタグの差し込みを補完する機能が搭載される。

<!-- end list -->

  - XCute Ver9

<!-- end list -->

  -
    Excel Open
      -
        ウェブブラウザ ([Internet Explorer](../Page/Internet_Explorer.md "wikilink")) にExcelをインラインもしくは単独で表示し、データを入出力する機能が搭載される。

<!-- end list -->

  - XCute Ver10

<!-- end list -->

  -
    英語環境対応
      -
        英語版WindowsとExcelでの動作に対応。
    データベースネイティブ接続対応
      -
        Oracle Database・Microsoft SQL Server・IBM DB2では各DBに特化したデータ接続が可能になる。

<!-- end list -->

  - XCute Ver11

<!-- end list -->

  -
    多国語 ([UTF-8](../Page/UTF-8.md "wikilink")) 対応
      -
        海外拠点の現地語入出力が可能になる。
    帳票自動生成ツール「コンバーター」
      -
        Excelのシートに作成した画面からDBテーブルの生成やマッピングを自動的に行うツールを添付。
    ITpro Active Contents Grand Prix 2013 「カタログ部門賞」受賞。\[5\]

<!-- end list -->

  - XCute Ver12

<!-- end list -->

  -
    内部コードの[.NET Framework化](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
      -
        プラットフォーム変更による可汎性とパフォーマンスの向上。
    最新OS・Excelへの対応
      -
        [Microsoft Windows 8](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")・Excel 2013をサポートし、HTMLとExcelブックのほか[PDFや](../Page/Portable_Document_Format.md "wikilink")[CSVの出力も可能になる](../Page/Comma-Separated_Values.md "wikilink")。

## サポート

XCuteのサポートは、マイクロラボの運営するXcuteユーザーフォーラムで行われており誰でも利用することができる。また、製品を購入しサポートに加入したユーザに対しては電子メールや電話などで開発者によるサポートを直接受けることができ、ソフトウェアバージョンアップにも無償で対応している。

## 脚注

<div class="references-small">

<references/>

</div>

## 関連項目

  - [Webサーバ](../Page/Webサーバ.md "wikilink")
  - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")
  - [HTML](../Page/HyperText_Markup_Language.md "wikilink")
  - [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")
  - [リッチインターネットアプリケーション](../Page/リッチインターネットアプリケーション.md "wikilink")

## 外部リンク

  - [株式会社マイクロラボ](http://www.microlab.jp/)

[Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink")

1.  登録番号 第５２５１１５５号
2.  マイクロラボ社[納入企業一覧](http://www.microlab.jp/jirei/xuc.htm)より
3.  マイクロラボ[導入事例](http://www.microlab.jp/jirei/casehigh.htm)より
4.  日経コンピュータ2008年7月1日号特集記事「"Officeレガシー"は宝に変わる」より
5.  日経BP社[Webサイト](http://corporate.nikkeibp.co.jp/information/newsrelease/newsrelease20131203.shtml)より