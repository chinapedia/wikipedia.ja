> この記事は[FileMaker](https://ja.wikipedia.org/wiki/FileMaker)から翻訳されています。


**FileMaker**（ファイルメーカー）は、[クラリス社](../Page/クラリス_\(企業\).md "wikilink")（旧ファイルメーカー社）が開発しているクロスプラットフォームの[データベース](../Page/データベース.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。最新版は**19**。

当初は[カード型であったが](https://ja.wikipedia.org/wiki/カード型データモデル "wikilink")、バージョンアップ毎に様々な機能を追加してきた。

FileMaker Proとなった後に大きなものでは、3.0にて[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")機能、4.0ではプラグイン機能及びWeb公開機能、7.0では多テーブル構造を取り入れファイル形式を変更し、データベースのキャパシティーが増大した。現バージョンではカード型の平易さを残したまま、かなりの規模のデータベースを構築できる。また、簡易DTP機能を備えており、ページデザインの自由度もデータベースソフトとしては高い。

日本語版はバージョン6までがカタカナ表記、バージョン7以降は英字表記が正式となる。

## 製品と概要

  - FileMaker Pro Advanced
    FMPと同様の機能を有し、さらに開発専用ツールやセキュリティ（AES256ビット暗号化）を付加した上位版。ユーザが FileMaker Pro を持っていなくても使える、スタンドアロン型ランタイムソリューションを作成できるほか、計算式の使い廻しが容易となるカスタム関数が作成できる（FMPでも使用可能）。スクリプトデバッガを用いてステップごとにスクリプトを確認することにより、問題のある箇所を特定できるようになった。バージョン7までの名称はFileMaker Developer。
    FileMaker 17 以後は Windows Mac OSにインストールできるクライアントソフトとして FileMaker Pro Advanced のみとなる。
  - FileMaker Server
    FMPで作成したデータベースを[LANネットワークへ公開し](../Page/Local_Area_Network.md "wikilink")、共有する事に特化したサーバーソフトウエア。バックアップ機能等がある。単体ではデータベースの参照・作成は出来ない。使用方法は、FileMaker Server (FMS) をサーバマシンにインストールしてデータベースを公開し、クライアントマシンにインストールしたFMPからネットワーク越しにFMSで公開されたデータベースにアクセスする。なおバージョン9からはPHPおよび[XSLTを利用したカスタムWeb公開も](../Page/XSL_Transformations.md "wikilink")、通常版FileMaker Serverで可能となった。バージョン11のときに発売されたFileMaker Go（iOSアプリ）により、データベースソリューションにiOSデバイスからアクセスすることが可能となった。パッケージ製品の販売はバージョン12にて終了。以後ボリュームライセンスのみとなる。バージョン13から搭載されたFileMaker WebDirectにより、データベースソリューションにWebブラウザからアクセスすることが可能となった。
  - FileMaker Go
    [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink") / [iPod touchや](https://ja.wikipedia.org/wiki/iPod_touch "wikilink")[iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")用のユニバーサルアプリ。機能制限はあるが、FMPで作成したデータベースを使用できる。開発機能は無い。2010年7月発売（当初は有償だったがバージョン12から無償）。
    データベース共有（FileMaker CloudかFileMaker Server、FileMaker Pro/Advancedでアクセス権を設定）されたデータベースソリューションに、[Wi-Fi](../Page/Wi-Fi.md "wikilink")または携帯電話回線経由でアクセスする。または、データベースファイルをiTunesのファイル共有でデバイスにコピーしてオフラインでの使用も可能。

### FileMaker Cloud

  - 日本では2017年7月から東京リージョンでサービス開始。
  - アマゾンウェブサービス（Amazon Web Services）を使用して、クラウド上にFileMaker Pro Advancedで作成したユーザ独自のデータベースソリューション（クラリス社では"カスタム App"と呼称）を共有できるクラウドサービス。
  - FileMaker Pro Advanced、FileMaker Go、および FileMaker WebDirect のいずれもクライアントとしてアクセス可能。
  - AWS Marketplaceを通じて利用人数（ユーザ数）分のFileMakerソフトウェアごと購入する方法と、クラリス社からソフトウェアライセンスを購入し、BYOL（Bring Your Own License）でFileMaker Cloudに持ち込んで稼働させる方法がある。
  - オンプレミスのFileMaker Serverと比較した場合のメリットは、サーバーマシン用のHD/OSの調達コストや管理コストが不要、時間単位課金を選択可能、スケーラビリティの拡張や縮小が容易、など。デメリットはESSアダプタやカスタムWeb公開がサポートされないこと。

## 販売終了製品

### FileMaker Pro

  -
    ユーザ独自のビジネスアプリケーション（クラリス社では"カスタム App"と呼称）の作成、変更、利用、共有ができるデスクトップソフトウエア（Mac/Windows）。以下FMPと記す。FMP11より、「FileMaker グラフ」(垂直棒グラフ、水平棒グラフ、面グラフ、線グラフ、円グラフなどを作成できるグラフ機能)、「クイックレポート」(スプレッドシートのような形式でレポートが作成できる機能)「スナップショットリンク」(ある時点での特定の対象レコードを保存し情報共有可能な機能)が追加された。2018年5月16日に発売された FileMaker 17 を以て FileMaker Proは FileMaker Pro Advanced に統合されたため、FileMaker Pro 16 にて販売を終了。

### FileMaker Server Advanced

  -
    FileMaker Serverの上位バージョンにあたる製品。FileMaker Serverの機能に加えて[ODBC](../Page/Open_Database_Connectivity.md "wikilink")/[JDBC](../Page/JDBC.md "wikilink")データソースとなる機能と、インスタントWeb公開機能を備えた。同時接続できる FileMaker Pro クライアント数の制限が無くなり(ただし、使用するハードウェアとオペレーティングシステムによって制限あり)、同時接続250ユーザまで可能となった。Server／Server Advanced間の差違が、バージョン8までとは異なっている[1](http://www.filemaker.com/jp/products/filemaker-server/version-comparison.html)。バージョン13でFileMaker Serverと統合され、販売終了した。
  - FileMaker Mobile
    [Palm](../Page/Palm.md "wikilink") や [Pocket PCとFMPで作成したデータベースを連動させるソフトウエア](../Page/Pocket_PC.md "wikilink")。FMPと併用する。2001年にバージョン1が登場（当時はPalmのみ対応）。バージョン2.1でPocket PCに対応した。
    バージョン7よりFMPとナンバーが統一されるも、バージョン8版をもって開発終了となり、販売・サポートは終了した[2](http://www.filemaker.co.jp/support/fmm_eol.html)。
  - ファイルメーカー Mobile for i-mode
    ファイルメーカーPro で作成したデータベースから、[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")対応サイトを作るサーバソフトウェア。[2002年](../Page/2002年.md "wikilink")3月に日本のみで発売された。[2005年](../Page/2005年.md "wikilink")9月に出荷終了。

## 主な機能

  - FileMaker Data API
    FMS 16から追加された機能。FMS 17では API フォーマットがさらに標準化され、より簡単に作業できるようになった。FileMaker Data API は、共有データベースのデータに Web サービスからアクセスできるようにするアプリケーションプログラミングインターフェース (API) で、REST (Representational State Transfer) アーキテクチャを使用しており、FileMaker Data API は REST API である。この REST API を使用して FileMaker のデータを他のアプリケーションや Web サービスに接続することができる。

### FileMaker WebDirect機能

  -
    FMS 13から追加された機能。多少の制限はあるが、FileMaker Pro/FileMaker Pro Advancedで作成したデータベースの画面そのものを、Webブラウザで表示し、CGIやSQLを使わずにデータの入力、検索などが出来る。使用するには、FileMaker Serverだけでなく「ユーザ接続ライセンス」または「同時接続ライセンス」の購入が必要。
  - カスタムWeb公開機能
    FileMaker Server/FileMaker Server Advancedを利用して、PHP/XSLTを使ったWebページと連携する機能。
  - ランタイム生成機能
    FileMaker Pro Advancedのみの機能。作成したデータベースをアプリケーション化し、FileMakerがインストールされていない環境でも利用可能にする。Mac用アプリ生成にはMac版FileMakerが、Windows版生成にはWindows版FileMakerが必要だが、FileMaker 8.5以降では「1ユーザが同時使用しない限り、2台のマシンへのインストールが可能」というライセンス形態となったため、1ライセンスで両バージョンの生成ができる。
  - FileMaker グラフ
    FMP 11から追加された機能。垂直棒グラフ、水平棒グラフ、面グラフ、線グラフ、円グラフという5種類の形式でグラフを作成することが可能。
  - クイックレポート機能
    FMP 11から追加された機能。スプレッドシートのような形式でレポートを作成することができる。

#### iOS App SDK (ソフトウェア開発キット)

  -
    FileMaker で作成したカスタム App を iOS アプリに変換するツールキット。プッシュ通知、HealthKit、HomeKit、および Apple Pay などの iOS テクノロジーに接続する iOS アプリを作成できる。経験豊富な FileMaker 開発者向けで、FileMaker Developer Subscription (年間サブスクリプション) 購入者の特典。

## バージョン履歴

バージョンアップ時には、ファイルの互換性を保った形とそうでない物があり、互換性の無いバージョンアップの際には、使用する拡張子を変更している。

バージョンと拡張子は以下の通りである。

  - .fmp = 2
  - .fp3 = 3
  - .fmj = 3 / 4.0 / 4.1（日本語版）
  - .fp4 = 4
  - .fp5 = 5 / 5.5 / 6
  - .fp7 = 7 / 8 / 8.5 / 9 / 10 / 11
  - .fmp12 = 12 / 13 / 14 / 15 / 16 / 17 / 18

| 年月                                                         | バージョン                                               | 開発元                                                                                                                                                                                                   | 備考                |
| ---------------------------------------------------------- | --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- |
| [1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")4月  | FileMaker, v1.0                                     | Forethought Inc.                                                                                                                                                                                      |                   |
| [1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")10月 | FileMaker Plus, v2.1                                |                                                                                                                                                                                                       |                   |
| [1988年](../Page/1988年.md "wikilink")7月                     | FileMaker 4, v4                                     | Nashoba Systems                                                                                                                                                                                       |                   |
| 1988年8月                                                    | FileMaker II, v 1.0                                 | Claris Corporation                                                                                                                                                                                    |                   |
| 1989年4月                                                    | FileMaker II, v 1.0（日本語版）                           |                                                                                                                                                                                                       |                   |
| [1989年](../Page/1989年.md "wikilink")7月                     | FileMaker II, version 1.1v2                         |                                                                                                                                                                                                       |                   |
| [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")10月 | FileMaker Pro 1.0v1                                 |                                                                                                                                                                                                       |                   |
| [1991年](../Page/1991年.md "wikilink")3月                     | FileMaker Pro 1.0v2                                 |                                                                                                                                                                                                       |                   |
| [1992年](../Page/1992年.md "wikilink")3月                     | FileMaker Pro 1.0v3                                 |                                                                                                                                                                                                       |                   |
| 1992年9月                                                    | FileMaker Pro 2.0v1                                 | Windows対応                                                                                                                                                                                             |                   |
| 1992年10月                                                   | FileMaker Pro 2.0v2                                 |                                                                                                                                                                                                       |                   |
| [1993年](../Page/1993年.md "wikilink")3月                     | FileMaker Pro 2.0v3                                 |                                                                                                                                                                                                       |                   |
| 1993年4月                                                    | FileMaker Pro 2.0v4                                 |                                                                                                                                                                                                       |                   |
| 1993年8月                                                    | FileMaker Pro 2.1v1                                 |                                                                                                                                                                                                       |                   |
| [1994年](../Page/1994年.md "wikilink")2月                     | FileMaker Pro 2.1v2                                 |                                                                                                                                                                                                       |                   |
| 1994年7月                                                    | FileMaker Pro 2.1v3/SDK 2.1                         |                                                                                                                                                                                                       |                   |
| 1994年7月                                                    | FileMaker Pro Server 2.0v                           |                                                                                                                                                                                                       |                   |
| 1994年7月                                                    | FileMaker Pro SDK 2.1v1                             |                                                                                                                                                                                                       |                   |
| [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")3月  | FileMaker Pro Server 2.1v1                          |                                                                                                                                                                                                       |                   |
| 1995年10月                                                   | FileMaker Pro 3.0v1                                 | TCP/IPネットワーク、関係データベース機能追加                                                                                                                                                                             |                   |
| [1996年](../Page/1996年.md "wikilink")1月                     | FileMaker Pro Server 3.0v1                          |                                                                                                                                                                                                       |                   |
| 1996年1月                                                    | FileMaker Pro 3.0v2                                 |                                                                                                                                                                                                       |                   |
| 1996年6月                                                    | FileMaker Pro 3.0v3                                 |                                                                                                                                                                                                       |                   |
| 1996年6月                                                    | FileMaker Pro 3.0v4                                 |                                                                                                                                                                                                       |                   |
| 1996年6月                                                    | FileMaker Pro SDK 3.0v1                             |                                                                                                                                                                                                       |                   |
| [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")9月  | FileMaker Pro 4.0v1                                 |                                                                                                                                                                                                       |                   |
| [1999年](../Page/1999年.md "wikilink")6月                     | FileMaker Pro 4.1v2                                 | FileMaker, Inc.                                                                                                                                                                                       | プラグイン機能、Web公開機能追加 |
| 1999年9月                                                    | FileMaker Pro 5.0v1                                 |                                                                                                                                                                                                       |                   |
| 1999年11月                                                   | FileMaker Server 5.0v1                              |                                                                                                                                                                                                       |                   |
| [2001年](../Page/2001年.md "wikilink")3月                     | ファイルメーカー Mobile                                     |                                                                                                                                                                                                       |                   |
| 2001年5月                                                    | FileMaker Pro 5.5v1                                 |                                                                                                                                                                                                       |                   |
| 2001年7月                                                    | FileMaker Server 5.5v1                              |                                                                                                                                                                                                       |                   |
| [2002年](../Page/2002年.md "wikilink")3月                     | ファイルメーカー Mobile for i-mode                          | 日本のみでの発売                                                                                                                                                                                              |                   |
| 2002年5月                                                    | ファイルメーカー Mobile 2                                   |                                                                                                                                                                                                       |                   |
| 2002年9月                                                    | FileMaker Pro 6.0v1                                 |                                                                                                                                                                                                       |                   |
| 2002年12月                                                   | ファイルメーカー Mobile 2.1                                 |                                                                                                                                                                                                       |                   |
| [2004年](../Page/2004年.md "wikilink")3月                     | FileMaker Pro 7.0v1                                 |                                                                                                                                                                                                       |                   |
| 2004年5月                                                    | FileMaker Server 7.0v1                              |                                                                                                                                                                                                       |                   |
| 2004年5月                                                    | FileMaker Pro 7.0v2                                 |                                                                                                                                                                                                       |                   |
| 2004年6月                                                    | FileMaker Mobile 7                                  |                                                                                                                                                                                                       |                   |
| 2004年9月                                                    | FileMaker Server 7.0v2                              |                                                                                                                                                                                                       |                   |
| 2004年10月                                                   | FileMaker Pro 7.0v3                                 |                                                                                                                                                                                                       |                   |
| [2005年](../Page/2005年.md "wikilink")5月                     | FileMaker Mobile 7v1                                |                                                                                                                                                                                                       |                   |
| 2005年8月                                                    | FileMaker Pro 8.0v1                                 |                                                                                                                                                                                                       |                   |
| 2005年8月                                                    | FileMaker Pro Advanced 8.0v1                        |                                                                                                                                                                                                       |                   |
| 2005年9月                                                    | FileMaker Server 8.0v1                              |                                                                                                                                                                                                       |                   |
| 2005年12月                                                   | FileMaker Pro 8.0v2                                 |                                                                                                                                                                                                       |                   |
| 2005年12月                                                   | FileMaker Pro Advanced 8.0v2                        |                                                                                                                                                                                                       |                   |
| [2006年](../Page/2006年.md "wikilink")1月                     | FileMaker Server Advanced 8.0v1                     |                                                                                                                                                                                                       |                   |
| 2006年1月                                                    | FileMaker Mobile 8                                  |                                                                                                                                                                                                       |                   |
| 2006年4月                                                    | FileMaker Pro 8.0v3                                 |                                                                                                                                                                                                       |                   |
| 2006年4月                                                    | FileMaker Pro Advanced 8.0v3                        |                                                                                                                                                                                                       |                   |
| 2006年4月                                                    | FileMaker Server 8.0v3                              |                                                                                                                                                                                                       |                   |
| 2006年4月                                                    | FileMaker Server Advanced 8.0v3                     |                                                                                                                                                                                                       |                   |
| 2006年8月                                                    | FileMaker Server 8.0v4                              |                                                                                                                                                                                                       |                   |
| 2006年8月                                                    | FileMaker Server 8.0v4 Advanced                     |                                                                                                                                                                                                       |                   |
| 2006年9月                                                    | FileMaker Pro 8.5                                   |                                                                                                                                                                                                       |                   |
| 2006年9月                                                    | FileMaker Pro 8.5 Advanced                          |                                                                                                                                                                                                       |                   |
| 2007年3月                                                    | FileMaker Pro 8.5v2                                 |                                                                                                                                                                                                       |                   |
| 2007年3月                                                    | FileMaker Pro 8.5v2 Advanced                        |                                                                                                                                                                                                       |                   |
| 2007年9月                                                    | FileMaker Pro 9                                     |                                                                                                                                                                                                       |                   |
| 2007年9月                                                    | FileMaker Pro 9 Advanced                            |                                                                                                                                                                                                       |                   |
| 2007年9月                                                    | FileMaker Server 9                                  |                                                                                                                                                                                                       |                   |
| 2007年9月                                                    | FileMaker Server 9 Advanced                         |                                                                                                                                                                                                       |                   |
| 2009年1月                                                    | FileMaker Pro 10, Pro 10 Advanced                   |                                                                                                                                                                                                       |                   |
| 2009年1月                                                    | FileMaker Server 10, Server 10 Advanced             |                                                                                                                                                                                                       |                   |
| 2010年4月                                                    | FileMaker Pro 11, Pro 11 Advanced                   |                                                                                                                                                                                                       |                   |
| 2010年4月                                                    | FileMaker Server 11, Server 11 Advanced             |                                                                                                                                                                                                       |                   |
| 2010年7月                                                    | FileMaker Go                                        |                                                                                                                                                                                                       |                   |
| 2012年4月                                                    | FileMaker Pro 12, Pro 12 Advanced                   |                                                                                                                                                                                                       |                   |
| 2012年4月                                                    | FileMaker Server 12, Server 12 Advanced             |                                                                                                                                                                                                       |                   |
| 2012年4月                                                    | FileMaker Go 12 for iPad, for iPhone                |                                                                                                                                                                                                       |                   |
| 2013年12月                                                   | FileMaker Pro 13, Pro 13 Advanced                   |                                                                                                                                                                                                       |                   |
| 2015年5月                                                    | FileMaker Pro 14, Pro 14 Advanced, Go 14, Server 14 | スクリプトワークスペース, 起動センター, ボタンアイコン, スタンバイサーバー, WebDirectのタブレットブラウザ対応                                                                                                                                       |                   |
| 2016年5月                                                    | FileMaker Pro 15, Pro 15 Advanced, Go 15, Server 15 | iBeacon対応, Touch ID/3D Touch/App Extensions対応, WebDirectのスマートフォンブラウザ対応, 基本のStarter Solution, マスク付き編集ボックス, ESSアダプタ                                                                                     |                   |
| 2017年5月                                                    | FileMaker Pro 16, Pro 16 Advanced, Go 16, Server 16 | レイアウトオブジェクトウインドウ、カード、Windows OS 上での新しい FileMaker Pro インターフェース、値一覧のコピーと貼り付け、FileMaker データソース参照内の変数、cURL オプションの機能強化、JSON 関数、外部スクリプトステップ、クリック可能なセキュリティロックアイコン、OAuth 2.0 によるアカウントをサポート、フィールドレベルでのテキストの暗号化 |                   |
| 2018年5月                                                    | FileMaker Pro 17 Advanced, Go 17, Server 17         | iOSセンサー情報収集、Goが実行されていない環境でのローカル通知、アカウントのロックアウト、電子メールへの複数ファイルの添付、ボリュームライセンス販売形態をデバイスライセンスからユーザライセンスモデルへ変更。FileMaker data migration tool をFDSメンバー向けに公開。                                                 |                   |

## 関連項目

  - [Bento](../Page/Bento.md "wikilink")
  - [Microsoft Access](../Page/Microsoft_Access.md "wikilink")
  - [Open Database Connectivity (ODBC)](../Page/Open_Database_Connectivity.md "wikilink")

## 外部リンク

  - [Claris International Inc.](https://www.claris.com/)
  - [クラリス・ジャパン株式会社](https://www.claris.com/jp/)

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink")