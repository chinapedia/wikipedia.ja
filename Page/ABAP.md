> この記事は[ABAP](https://ja.wikipedia.org/wiki/ABAP)から翻訳されています。


**ABAP**（Advanced Business Application Programming, アバップ）とは、[R/3や](https://ja.wikipedia.org/wiki/SAP_R/3 "wikilink")[S/4HANAなど](https://ja.wikipedia.org/wiki/SAP_S/4HANA "wikilink")[SAPシステムの製作やアドオン開発に用いられる](https://ja.wikipedia.org/wiki/SAP_AG "wikilink")[高級言語](https://ja.wikipedia.org/wiki/高級言語 "wikilink")である。

## 言語の特徴

[SAP SEの製品でのみ用いられるSAP独自の](../Page/SAP_\(企業\).md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")。もともとは[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")言語であったが、後に[オブジェクト指向言語として拡張された](../Page/オブジェクト指向プログラミング.md "wikilink")。

SAPアプリケーション群はABAPを開発言語とし、BASIS（[SAP NetWeaver](https://ja.wikipedia.org/wiki/SAP_NetWeaver "wikilink")）をアプリケーションサーバに利用することで特定のオペレーティングシステムやデータベース管理システムなどのプラットフォームに依存することなく、開発、運用することができる。また、ABAPをSAPアプリケーション開発に採用することで、Javaや.NET C\#などの他のITベンダーが提供するプログラミング言語を利用する場合に比べて言語仕様の変更やランタイムのアップデートの影響を受けることなく、自社でリリースやアップグレードサイクルをコントロールできるメリットがある。

## 文法

文の終了記号は、"."(ピリオッド)である。 IF文の等値判断は"="である。

### テーブル

[SAP R/3では](https://ja.wikipedia.org/wiki/SAP_R/3 "wikilink")「テーブル」といわれる[データベースシステムを用いている](../Page/データベース管理システム.md "wikilink")。テーブルの種類は「標準テーブル」「アドオンテーブル」「内部テーブル」の3種類が存在する。標準テーブルはSAP R/3にはじめから実装されているテーブルであり、アドオンテーブルはエンジニアやコンサルタントが後から追加して作成するテーブル、内部テーブルは特定のプログラム内でのみデータを保存するテーブルである。

ABAPでは、これらのテーブルからデータを取得したり、テーブルにデータ（レコード）を挿入したり、テーブルからデータを削除する際、[SQL](../Page/SQL.md "wikilink")を用いることが可能である。

プログラム上でデータを入れるハコとしての役割を持つものとしては、内部テーブル以外に「作業領域」と「変数」が存在している。

### データの宣言

以下の方法で変数を宣言することができる。

DATA : 変数名 TYPE 型名 \[LENGTH 長さ\].

### 定数の宣言

以下の方法で定数を宣言することができる。

CONSTANTS : 定数名 TYPE 型名 VALUE {値|IS INITIAL}.

### イベント

ABAPでは、それぞれの処理に対して、[イベントが用意されている](../Page/イベント_\(プログラミング\).md "wikilink")。イベントを用いて、ABAP言語を用いて処理を行う。

なお、レポートプログラムを作成する場合には以下のイベントが存在する。

  - INITIALIZATION …… 初期設定を行うイベントを記述する。
  - AT SELECTION-SCREEN …… 画面などで入力された結果に対してイベントを記述する。
  - START-OF-SELECTION …… 主処理を記述する。
  - END-OF-SELECTION …… 処理結果として処理するイベントを記述する。

### 内部テーブル

標準テーブル、ソートテーブル、ハッシュテーブルの3種類がある。

### トランザクションコード

SAPでは、EASY ACCESSやIMG以外に、各処理画面へ移動する方法として、トランザクションコードが存在している。アドオン開発に用いられるトランザクションコードには、以下のものが存在している。

  - SE09 移送オーガナイザ
  - SE11 テーブルやデータエレメントなどの追加・照会
  - SE24 クラスの作成・照会
  - SE37 汎用モジュールの作成・照会
  - SE38 プログラムの作成
  - SE80 オブジェクトナビゲータ
  - SE81 アプリケーション階層
  - SE84 リポジトリ情報システム
  - SE91 メッセージ
  - SE93 トランザクションコードの作成・照会

## 関連項目

  - [SAP SE](../Page/SAP_\(企業\).md "wikilink")
  - [SAPジャパン](../Page/SAPジャパン.md "wikilink")
  - [SAP S/4HANA](https://ja.wikipedia.org/wiki/SAP_S/4HANA "wikilink")
  - [SAP R/3](https://ja.wikipedia.org/wiki/SAP_R/3 "wikilink")
  - [SAP NetWeaver](https://ja.wikipedia.org/wiki/SAP_NetWeaver "wikilink")

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")