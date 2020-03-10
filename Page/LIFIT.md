> この記事は[LIFIT](https://ja.wikipedia.org/wiki/LIFIT)から翻訳されています。


**LIFIT(ライフィット)**とは、株式会社ターボデータラボラトリーが開発し、販売しているオンメモリ型データ処理エンジン[DayDa.Laboo](https://ja.wikipedia.org/wiki/DayDa.Laboo "wikilink")に接続するための、[スプレットシート](https://ja.wikipedia.org/wiki/スプレットシート "wikilink")型[データベース接続クライアント](https://ja.wikipedia.org/wiki/データベース接続クライアント "wikilink")ソフトである。

[Oracle Databaseにおける](../Page/Oracle_Database.md "wikilink")[SQL\*Plus](https://ja.wikipedia.org/wiki/SQL*Plus "wikilink")にあたるGUIアプリケーションである。

## 特性

### 特性(GUI側)

  - 「お化けエクセル」と一部で評されるように[Microsoft Excelと似たような操作感覚](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")。(若干違う箇所もあり)
  - 操作オペレーションが[マクロ](../Page/マクロ言語.md "wikilink")[ログとして](../Page/データログ.md "wikilink"),GUI上に生成・表示される。又自動出力ログとして記録される。
  - [マクロ](../Page/マクロ言語.md "wikilink")[ログを使って実行することにより](../Page/データログ.md "wikilink")、[Microsoft Excelの](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")「マクロの自動記録・実行」と同様な処理が可能。
  - Javaで作成されたGUIである。\[1\]
  - [DayDa.Laboo](https://ja.wikipedia.org/wiki/DayDa.Laboo "wikilink")エンジンとの接続タイプには、「Nタイプ\[2\]」「Sタイプ\[3\]」の二種類が存在する。

### 特性(DAYDA.Labooエンジン側)

  - [x64](https://ja.wikipedia.org/wiki/x64 "wikilink")(Win64)版のみ「[共有メモリ](../Page/共有メモリ.md "wikilink")」というJOB間テーブル共有機能がある。
  - 操作行が[Microsoft Excelに比べ著しく多く](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")(データ操作行は200万以上)、また
  - [Microsoft Excelより高速に計算処理を行うことができる](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")。
  - エンジン処理自体が高速な為、実行結果をリアルタイムに確認しながら操作を行うことができる。(思考を途切れさせない)

## GUI的にできること・できないこと

### できること

  - 専用データ形式\[4\]を使わないのであれば、基本的にCSVを読込んでクレンジング処理してCSVを再出力する用途に使われる。
  - 1操作ごとに1LIFITマクロが生成される。(操作オペレーションが完全に再現される)
  - GUI上に生成・表示されたLIFIYマクロは、LIFIT上で編集・ファイル保存することができる。
  - 保存済みLIFITマクロファイルをコマンドライン引数として、コマンドライン実行を行うことができる。
  - コマンドライン実行時にマクロ実行エラーが発生した場合、エラーコードを出力するので、それに基づいてバッチ連携処理を組むことができる。
  - カンマ区切り、TAB区切りのCSVを読み込んで処理を行うことができる。(GUIに操作ビューが存在)
  - ODBCIOⅡプラグインを追加する事により[Microsoft SQL Serverと](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[Oracle Databaseとの連携が可能](../Page/Oracle_Database.md "wikilink")。

### ODBCIOⅡプラグイン

  - 他のデータベースと連携するための**LIFIT**の追加オプション製品。
  - [Microsoft SQL Serverと](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[Oracle Database上のテーブルに対してインポートまたはエクスポートを行うことができる](../Page/Oracle_Database.md "wikilink")。

### できないこと

  - [SQL](../Page/SQL.md "wikilink")を使うことができない。
  - 固定長の[ファイル読込をエンジン側はサポートしているが](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")、[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")に操作ビューが存在しない。
  - グラフを作成、表示する事や、印刷ができない。\[5\]。
  - [マクロ](../Page/マクロ言語.md "wikilink")[ファイルの文法が](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")、VBAのような構造化プログラミングに適した形式ではない。\[6\]
  - コマンドライン実行時の終了コードが、正常終了(0)と異常終了(-1)のみ。(異常発生時は自動出力ログの解析が前提)
  - エラー発生時に、単体で障害[メール等を送信してユーザーにエラーを通知する機能はない](../Page/電子メール.md "wikilink")。\[7\]
  - 実行時のエラーログが、自動出力ログ上に混合出力されているので障害分析がしづらい。

## LIFITマクロ(ファイル)の特徴・制限

  - 頭から順に再生する直列羅列形式。
  - 基本的に[DayDa.Laboo](https://ja.wikipedia.org/wiki/DayDa.Laboo "wikilink")のエンジンを操作する[マクロのみ用意されている](../Page/マクロ言語.md "wikilink")。\[8\]
  - ユーザ独自の[マクロを作成することができない](../Page/マクロ言語.md "wikilink")。\[9\]
  - [BASIC](../Page/BASIC.md "wikilink")のような関数コールの記述ができない
  - FOR、WHILE、IF文等の制御系マクロが存在しない。
  - 変数(単純変数・[COBOL](../Page/COBOL.md "wikilink")で使用されるような構造体変数)を別途宣言したり、使うことができない。
  - 変数が使えないので、変数を引数としたマクロ実行ができない。

`(文法的制限に関しては、Java生成機能である程度代用できるとのこと)`

## 各タイプの特徴

### NタイプとSタイプの相違

  - Sタイプ:ローカルフルアクセス
  - Nタイプ:指定ディレクトリのみ(セキュリティ設定ファイルの設定に依存)

### サーバー版DayDa.Labooエンジンの特徴

サーバー版[DayDa.Laboo](https://ja.wikipedia.org/wiki/DayDa.Laboo "wikilink")エンジンはSタイプに比べ

  - 　処理行が多い。
  - 　計算処理で使用される[CPU](../Page/CPU.md "wikilink")数が多い。
  - 　計算処理で使用される[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")数が多い。
  - 　同時接続数が多い。

という特徴がある。

### 新製品(200709版)と旧製品(2006版)との差異

  - マウスの操作履歴がそのまま[デバッグ](../Page/デバッグ.md "wikilink")済みの[Java](https://ja.wikipedia.org/wiki/Java "wikilink")[プログラムとなり](../Page/プログラム_\(コンピュータ\).md "wikilink")、PC上で[バッチプログラムとして実行できる](https://ja.wikipedia.org/wiki/バッチ処理 "wikilink")。
  - GUIアプリケーションの動作の高速化(マルチスレッド対応\[10\])
  - GUI操作周り・表示の改善(D\&D読込等)
  - コンソールに実行状況出力するexeを別途提供([eclipseのeclipsec](../Page/Eclipse_\(統合開発環境\).md "wikilink").exeのようなもの)\[11\]
  - 新規Lifitマクロの追加(下位互換\[12\]はあるが、上位互換はない)

## 脚注

<div class="references-small">

<references />

</div>

[Category:データベース接続クライアント](https://ja.wikipedia.org/wiki/Category:データベース接続クライアント "wikilink")

1.  前身に、[Delphi](../Page/Delphi.md "wikilink")版ザ・ターボ(The Turbo)という製品が存在
2.  サーバー版[DayDa.Laboo](https://ja.wikipedia.org/wiki/DayDa.Laboo "wikilink")エンジン接続のネットワークタイプ
3.  ローカル版[DayDa.Laboo](https://ja.wikipedia.org/wiki/DayDa.Laboo "wikilink")エンジン接続のシングルタイプ([Aktblitz](https://ja.wikipedia.org/wiki/Aktblitz "wikilink")[パッケージ](../Page/パッケージ.md "wikilink"))
4.  D5D(ワークスペース単位),D5T(テーブル単位)
5.  [Microsoft Excelとの連係機能で代用](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")
6.  Java生成機能で代用
7.  [日立製作所](../Page/日立製作所.md "wikilink")の[JP1](../Page/JP1.md "wikilink")等の統合システム運用管理ツールと組み合わせて運用する事が前提
8.  運用に適した[マクロが全て用意されているわけではない](../Page/マクロ言語.md "wikilink")
9.  ただし既存のマクロの組み合わせは可能
10. 旧版、Delphi版ザ・ターボ(The Turbo)はどちらもシングルスレッド実行
11. 体験版では提供されていない模様
12. 既存マクロは同一仕様,ほぼ同一動作(動作の中身自体はエンジンに依存)