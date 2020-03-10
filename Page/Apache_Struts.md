> この記事は[Apache Struts](https://ja.wikipedia.org/wiki/Apache_Struts)から翻訳されています。


**Apache Struts**（アパッチ・ストラッツ）は、[Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Apacheソフトウェア財団 "wikilink")のApache Strutsプロジェクトにて開発されている[オープンソース](../Page/オープンソース.md "wikilink")の[Java](https://ja.wikipedia.org/wiki/Java "wikilink") [Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")である。

## 概要

元々はの作成したソフトウェアであり、[2000年](../Page/2000年.md "wikilink")5月にApacheソフトウェア財団に寄付された。当初は[Jakarta Projectに位置しており](https://ja.wikipedia.org/wiki/Jakarta_Project "wikilink")、**Jakarta Struts**（ジャカルタ・ストラッツ）と呼ばれていた。[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")にApacheのトップレベルプロジェクトに昇格した。

[Apache Tomcatなどの](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")[サーブレットコンテナ](https://ja.wikipedia.org/wiki/サーブレットコンテナ "wikilink")上で動かすことができる。[サーブレットと](../Page/Java_Servlet.md "wikilink")[JSPによる開発環境下に登場したStruts](../Page/JavaServer_Pages.md "wikilink")1は広く受け入れられ、2005年頃にはJava Webフレームワークの[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")と呼ばれるほどの普及を見せていた\[1\]\[2\]。しかしソフトウェア技術の進歩とともに欠点も多く指摘されるようになり、[2007年](../Page/2007年.md "wikilink")にリリースされたStruts2ではそれまでの仕組みを捨て、[WebWork](https://ja.wikipedia.org/wiki/WebWork "wikilink")2として開発されていた別のフレームワークをベースとしたものへと置き換えられている\[3\]。

フレームワークには[Model View Controllerアーキテクチャが適用されている](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink")。類似したフレークワークとして[JSF](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink") (Java Server Faces) や [Spring MVCフレームワークがある](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")。

## 特徴 (Struts1)

整備された[JSPカスタムタグによって](../Page/JavaServer_Pages.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")コードは[JSPファイルと分離され](../Page/JavaServer_Pages.md "wikilink")、従来のJSPのように[HTMLタグの中に](../Page/HyperText_Markup_Language.md "wikilink")`<%`と`%>`で囲まれたスクリプトレットであるJavaソースコードを混在させる必要なく読みやすく洗練されたコーディングができるようになっていた。

主なStrutsのタグライブラリ

  - HTML
      -
        HTMLのフォーム部分で利用する
  - Logic
      -
        条件分岐や繰り返しなどの制御ロジックを提供
  - Beans
      -
        Modelで定義されたJavaBeansにアクセスする機能を提供
  - Nested
      -
        属性名の記述を省略可能にする
  - Tiles
      -
        複数のJSPで利用する記述を共通化するテンプレート機能を提供

またStrutsでは`ActionServlet`が用意されており、画面の遷移をコントロールする設定ファイル（`struts-config.xml`）を変更するだけで容易に遷移先を変えることができる機能を提供していた。 アクションサーブレットでは画面で入力された内容を検査する Validator の機能が用意されており、設定ファイル（`validator-rules.xml`）を変更するだけで入力チェックの仕様を変更することが可能であった。入力チェックするデータは一旦アクションフォームと呼ばれるBeansに格納された。

最終リリースは[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")10月4日の1.3.10で、[2013年](../Page/2013年.md "wikilink")4月5日にサポート終了を迎えた\[4\]。[2014年](../Page/2014年.md "wikilink")現在でも多くのサイトがStruts1を使用しているが\[5\]、同年4月には深刻な脆弱性も発見されている\[6\]。

## 特徴 (Struts2)

Struts2では、Struts1と比べて下記のような改善がなされている\[7\]。

  - [アノテーション](../Page/アノテーション.md "wikilink")や[設定より規約](https://ja.wikipedia.org/wiki/設定より規約 "wikilink")による設定ファイルの削減
  - [依存性の注入](../Page/依存性の注入.md "wikilink") (DI)
  - [POJO](../Page/Plain_Old_Java_Object.md "wikilink")

また、OGNL (Object-Graph Navigation Language) と呼ばれる式言語が搭載されており、これにより動的なパラメータを扱うことを可能としている\[8\]。一方、この機能ではたびたび深刻な[セキュリティホール](../Page/セキュリティホール.md "wikilink")が発見されており、利便性の反面セキュリティ面の脆弱さも指摘されている\[9\]。

### セキュリティーホール

Struts2の多数のセキュリティーホールが攻撃対象になり、多数の被害を出している。

  - [GMOペイメントゲートウェイ](../Page/GMOペイメントゲートウェイ.md "wikilink")（[東京都](../Page/東京都.md "wikilink") ・[住宅金融支援機構](../Page/住宅金融支援機構.md "wikilink")） - クレジットカード番号36万件流出\[10\]\[11\]
  - [JETRO](https://ja.wikipedia.org/wiki/JETRO "wikilink") - メールアドレス2万件流出\[12\]\[13\]
  - [日本郵便](../Page/日本郵便.md "wikilink") - メールアドレス2万件流出\[14\]\[15\]
  - [ぴあ](https://ja.wikipedia.org/wiki/ぴあ "wikilink") - クレジットカード番号3万件流出\[16\]
  - [国土交通省](../Page/国土交通省.md "wikilink")土地総合情報システム - 不動産取引価格アンケート回答4,335件、所有権移転登記情報194,834件が流出した可能性あり\[17\]

## 派生版

  - Super Agile Struts (SAStruts)
    [Seasar](../Page/Seasar.md "wikilink")プロジェクトが公開している、Struts1と独自のDIコンテナであるSeasar2をベースに、より素早い開発を行うことを目指したフレームワーク。
  - [TERASOLUNA Server Framwork for Java](https://ja.wikipedia.org/wiki/TERASOLUNA "wikilink")
    [NTTデータ](../Page/NTTデータ.md "wikilink")が公開している、Struts1と[Spring](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink"), [iBATIS](https://ja.wikipedia.org/wiki/iBATIS "wikilink")をベースに、独自の拡張を行ったサーバサイドフレームワーク。

## 競合するMVCフレームワーク

Strutsは、よくドキュメント化され、成熟し、普及したフロントエンドのフレームワークであるが、「軽量」フレームワークとして分類される[Spring MVC](https://ja.wikipedia.org/wiki/Spring_Framework#Model-View-Controller_フレームワーク "wikilink")、[Stripes](https://ja.wikipedia.org/wiki/Stripes "wikilink")、[Apache Wicket](https://ja.wikipedia.org/wiki/Apache_Wicket "wikilink")、[Play Framework](https://ja.wikipedia.org/wiki/Play_Framework "wikilink")、[Apache Tapestryといったものがある](../Page/Apache_Tapestry.md "wikilink")。

Strutsからスピンオフした[WebWork](https://ja.wikipedia.org/wiki/WebWork "wikilink")フレームワークは、Strutsオリジナルと同じアーキテクチャを保持したうえでの強化と洗練を目的としていたが、StrutsとWebWorkは再びマージされ、Struts2としてリリースされた。

その他のJavaベースのMVCフレームワークとして、[WebObjects](https://ja.wikipedia.org/wiki/WebObjects "wikilink")や[Grails](https://ja.wikipedia.org/wiki/Grails "wikilink")もある。

## 脚注

## 関連項目

  - [JavaServer Faces](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink") (JSF)
  - [WebWork](https://ja.wikipedia.org/wiki/WebWork "wikilink")
  - [Spring Framework](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")

## 外部リンク

  - [Apache Struts](http://struts.apache.org/)
  - [Super Agile Struts (SAStruts)](http://sastruts.seasar.org/)
  - [TERASOLUNA Server Framework for Java](http://sourceforge.jp/projects/terasoluna/wiki/Server_Framework_for_Java_Web)

[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink")

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
11. 井上英明「[日経 xTECH　猛威振るうStruts2脆弱性への攻撃、どうすれば防げたか](http://tech.nikkeibp.co.jp/it/atcl/column/14/346926/032100893/)」、日経BP社、2017年3月22日
12.
13.
14.
15.
16.
17.