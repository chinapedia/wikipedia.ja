> この記事は[OSGi](https://ja.wikipedia.org/wiki/OSGi)から翻訳されています。


**OSGi Alliance**（従来の名称は Open Services Gateway initiative）は、1999年3月に設立された[標準化団体](../Page/標準化団体.md "wikilink")。遠隔から管理できる[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ベースのサービスプラットフォームを定義している。この仕様の中心となるのは、アプリケーションライフサイクルの[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")と[サービスレジストリ](https://ja.wikipedia.org/wiki/サービスレジストリ "wikilink")である。そのフレームワークに基づいて、多数のOSGiサービスが定義された（[ログ](../Page/データログ.md "wikilink")、[構成管理](../Page/構成管理.md "wikilink")、[HTTPサービス](../Page/Hypertext_Transfer_Protocol.md "wikilink")（[Java Servlet](../Page/Java_Servlet.md "wikilink")）、[XML構文解析](../Page/Extensible_Markup_Language.md "wikilink")、機器アクセス、[パッケージソフトウェア](../Page/パッケージソフトウェア.md "wikilink")管理、基本パーミッション管理、ユーザー管理、I/O接続、結線管理、[Jini](../Page/Jini.md "wikilink")、[UPnP](../Page/Universal_Plug_and_Play.md "wikilink") エクスポート、アプリケーション監視、宣言型サービス、消費電力管理、機器管理、セキュリティポリシー、診断/監視、フレームワーク階層化など）。

## OSGi フレームワークの範囲

このフレームワークは、スタンドアロンの Java/VM 環境に欠けている完全で動的なコンポーネントモデルを実装している。[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")や（「バンドル; bundle」形式で配布される）コンポーネントは遠隔からインストール・起動・停止・（[リブートせずに](../Page/再起動.md "wikilink")）アンインストールできる。Javaのパッケージや[クラスの管理は詳細に規定されている](../Page/クラス_\(コンピュータ\).md "wikilink")。ライフサイクル管理は、遠隔から管理ポリシーを[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")することで[APIを経由して行われる](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。サービスレジストリにより、バンドルが新たなサービスや消滅したサービスを自動検出して適切に対応する。

当初の目的はサービスゲートウェイの仕様だったが、適用範囲が広がっていった。OSGi の仕様は、[携帯電話](../Page/携帯電話.md "wikilink")からオープンソースの[Eclipse IDEまで幅広く応用されている](../Page/Eclipse_\(統合開発環境\).md "wikilink")。他にも、[自動車](../Page/自動車.md "wikilink")、[ファクトリーオートメーション](../Page/ファクトリーオートメーション.md "wikilink")、[ビル管理システム](../Page/インテリジェントビル.md "wikilink")、[携帯情報端末](../Page/携帯情報端末.md "wikilink")、[グリッド・コンピューティング](../Page/グリッド・コンピューティング.md "wikilink")、[エンターテインメント](../Page/エンターテインメント.md "wikilink")（例えば [iPronto](http://archive.is/BSVT9) ）、[アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")などに応用されている。

## 仕様策定プロセス

OSGi の仕様はメンバーによりオープンな形で開発され、[OSGi Specification License](http://bundles.osgi.org/Main/OSGiSpecificationLicense) により配布後の変更も自由となっている。OSGi Alliance はメンバー企業向けに認証プログラムを実施している。2010年11月現在、認証されたOSGi[実装](../Page/実装.md "wikilink")は R4.0で6 例、R4 V4.2で3例である（[list of certified](http://www.osgi.org/Specifications/Certified)）。

## 組織

OSGi Alliance は1999年3月、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、[IBM](../Page/IBM.md "wikilink")、[エリクソン](../Page/エリクソン.md "wikilink")などにより設立された（それ以前に母体となった Connected Alliance という提携関係が存在した）。

2006年現在、25社以上が様々な業種から参加している（IBM、Bosh Software、[ドイツテレコム](../Page/ドイツテレコム.md "wikilink")、[NTT](../Page/日本電信電話.md "wikilink")、[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、[レッドハット](../Page/レッドハット.md "wikilink")、[日立製作所](../Page/日立製作所.md "wikilink")、 Adobe、[Huawei](https://ja.wikipedia.org/wiki/Huawei "wikilink")など）。

各分野に委員会を設置しており、それぞれの分野の役員が選出されている。商業化に関しては別に委員会を設けており、それとは別に仕様策定は専門グループが行っている。

専門グループは、エンタープライズ、IoT、中核プラットフォームが現在活動中である。

## コミュニティ

2003年10月、[ノキア](../Page/ノキア.md "wikilink")、[モトローラ](../Page/モトローラ.md "wikilink")、[ProSyst](https://ja.wikipedia.org/wiki/ProSyst "wikilink") などのOSGiメンバー企業が新たにモバイル専門グループ（Mobile Expert Group）を結成し、[MIDPに基づいた新世代携帯電話向けのサービスプラットフォームの策定を行っている](../Page/Mobile_Information_Device_Profile.md "wikilink")。ここでは、[CLDCが管理できない部分への対応を行っている](../Page/Connected_Limited_Device_Configuration.md "wikilink")。この仕様は OSGi Release 4 の一部として公表されている。

2003年、[Eclipseは](../Page/Eclipse_\(統合開発環境\).md "wikilink")、IDEプラットフォームおよび[Eclipse Rich Client Platform](http://wiki.eclipse.org/index.php/Rich_Client_Platform)でのプラグイン・アーキテクチャの実行環境として OSGi 仕様を採用した。Eclipse には OSGi バンドル開発用ツールが含まれており、そのためのプラグインも各種用意されている（特に [ProSyst](https://ja.wikipedia.org/wiki/ProSyst "wikilink") と [Knopflerfish](https://ja.wikipedia.org/wiki/Knopflerfish "wikilink") が OSGi開発者向けの Eclipse プラグインを提供している）。

OSGi 仕様に関連したフリーソフトウェアの開発もされている。例えば、[Equinox OSGi](http://eclipse.org/equinox/)、[Apache Felix](http://incubator.apache.org/projects/felix.html)、 [mBS Equinox Edition](http://www.e-sysware.co.jp/product/freedl.html)など。

## 仕様バージョン履歴

  - 中核仕様
      - OSGi Release 1 (R1): 2000年5月
      - OSGi Release 2 (R2): 2001年10月
      - OSGi Release 3 (R3): 2003年3月
      - OSGi Release 4, Version 4.0: 2005年10月
      - OSGi Release 4, Version 4.0.1: 2006年9月
      - OSGi Release 4, Version 4.1: 2007年5月
      - OSGi Release 4, Version 4.2: 2009年9月
      - OSGi Release 5 (R5): 2012年6月
      - OSGi Release 6 (R6): 2015年8月
      - OSGi Release 7: 2018年4月

<!-- end list -->

  - モバイル仕様
      - OSGi Release 4, Version 4.0.1: 2006年9月

## 関連情報入手先

  - [Frequently Asked Questions](https://www.osgi.org/about-us/faq/)
  - [ProSyst](http://www.prosyst.com)
  - [aQute: OSGi Info](http://www.aqute.biz/)
  - [OSGi Users' Forums](http://www.osgiusers.org/)
  - [Makewave Japan](http://jp.makewave.com/)

## 関連RFCおよびJava標準

  - RFC 2608 ([Service Location Protocol](../Page/サービス・ロケーション・プロトコル.md "wikilink"))
  - Sun [Jini](../Page/Jini.md "wikilink")™ (Java Intelligent Network Infrastructure)
  - Sun JCP [JSR-8](http://www.jcp.org/en/jsr/detail?id=8) (Open Services Gateway Specification)
  - Sun JCP [JSR-232](http://www.jcp.org/en/jsr/detail?id=232) (Mobile Operational Management)
  - Sun JCP [JSR-246](http://www.jcp.org/en/jsr/detail?id=246) (Device Management API)
  - Sun JCP [JSR-249](http://www.jcp.org/en/jsr/detail?id=249) (Mobile Service Architecture for CDC)
  - Sun JCP [JSR-277](http://www.jcp.org/en/jsr/detail?id=277) (JavaTM Module System)
  - Sun JCP [JSR-291](http://www.jcp.org/en/jsr/detail?id=291) (Dynamic Component Support for JavaTM SE)

## 関連標準規格

  - [MHP](../Page/Multimedia_Home_Platform.md "wikilink") / [OCAP](https://ja.wikipedia.org/wiki/OpenCable_Application_Platform "wikilink")
  - [Universal Plug and Play](../Page/Universal_Plug_and_Play.md "wikilink") (UPnP)
  - [Universal Powerline Association](https://ja.wikipedia.org/wiki/Universal_Powerline_Association "wikilink")
  - [HomePlug](../Page/HomePlug_Powerline_Alliance.md "wikilink")
  - [LONWORKS](../Page/LONWORKS.md "wikilink")
  - [CORBA](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")
  - [CEBus](https://ja.wikipedia.org/wiki/CEBus "wikilink")
  - [EHS](https://ja.wikipedia.org/wiki/European_Home_Systems_Protocol "wikilink") / [CECED](https://ja.wikipedia.org/wiki/欧州家電機器委員会 "wikilink") CHAIN
  - [X10](../Page/X10_\(工業規格\).md "wikilink")
  - [Java Management Extensions](../Page/Java_Management_Extensions.md "wikilink")

## 書籍

  - <cite>OSGi Service Platform, Release 3</cite>, IOS Press, ISBN 1-58603-311-5

## 関連項目

  - [Knopflerfish](https://ja.wikipedia.org/wiki/Knopflerfish "wikilink")
  - [Apache Felix](https://ja.wikipedia.org/wiki/Apache_Felix "wikilink")
  - [JPOX](../Page/JPOX.md "wikilink")
  - [EasyBeans](../Page/EasyBeans.md "wikilink")
  - [DataNucleus](https://ja.wikipedia.org/wiki/DataNucleus "wikilink")

## 外部リンク

  - [OSGi ユーザフォーラムJapan](http://www.japan.osgiusers.org/Main/HomePage)
  - [OSGi web site General Information](http://www.osgi.org/)
      - [Specification Download](http://www.osgi.org/osgi_technology/download_specs.asp?section=2)
      - [OSGi Alliance Developer Site](http://www2.osgi.org/)
      - [Javadoc for Release 6](https://www.osgi.org/osgi-release-6-javadoc/)
  - [OSGi enRoute](http://enroute.osgi.org)
  - [OSGi Tutorial: A Step by Step Introduction to OSGi Programming Based on Knopflerfish](http://www.knopflerfish.org/tutorials/osgi_tutorial.pdf)
  - [Getting started with OSGi: tutorials from EclipseZone](http://neilbartlett.name/blog/osgi-articles/)
  - [Belgian Java User Group video presentation on Spring OSGi by Costin Leau](http://www.bejug.org/confluenceBeJUG/display/PARLEYS/Spring+OSGi)
  - [OSGi and Gravity Service Binder Tutorial](http://oscar-osgi.sourceforge.net/tutorial/)
  - [ApacheCon EU 2006 presentation about OSGi best practices by Marcel Offermans.](http://cwiki.apache.org/FELIX/presentations.data/best-practices-apachecon-20060628.pdf)
  - [Enterprise OSGi Professional Services (www.4enterprise.org)](http://www.4enterprise.org)

[Category:標準化団体](https://ja.wikipedia.org/wiki/Category:標準化団体 "wikilink")