> この記事は[EC-CUBE](https://ja.wikipedia.org/wiki/EC-CUBE)から翻訳されています。


**EC-CUBE**（イーシーキューブ）は、**株式会社イーシーキューブ**（*EC-CUBE CO.,LTD.*）が開発する[オープンソース](../Page/オープンソース.md "wikilink")の[EC向け](../Page/電子商取引.md "wikilink")[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink")（CMS）である。

## 歴史

ロックオン（現・[イルグルム](https://ja.wikipedia.org/wiki/イルグルム "wikilink")）が開発してきたECサイト構築システム[ECKit](https://ja.wikipedia.org/wiki/ECKit "wikilink")を元に、[2006年](../Page/2006年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink")にオープンソースとして公開（[デュアルライセンス](../Page/デュアルライセンス.md "wikilink")の採用により、[GPLの他](../Page/GNU_General_Public_License.md "wikilink")、商用ライセンスも選択可能）。同社（2019年1月以降は完全子会社の株式会社イーシーキューブ\[1\]）を主導として開発が続けられている。

2019年2月26日にはEC-CUBEの[SaaS](../Page/SaaS.md "wikilink")版となる[クラウドECプラットフォーム](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink")「ec-cube.co」がリリースされた\[2\]\[3\]。

## 特徴

  - 主に日本国内で開発されている、ECサイト構築用プログラム。海外で開発され、日本語化されたソフトと比較すると、自然な日本語表記になっている。[開発コミュニティ](http://xoops.ec-cube.net/)や[公式マニュアルサイト](http://wiki.ec-cube.net/)なども日本語で提供されている。
  - 同じオープンソースである[osCommerceや](https://ja.wikipedia.org/wiki/:en:OsCommerce "wikilink")[Zen Cart](https://ja.wikipedia.org/wiki/:en:Zen_Cart "wikilink")、[Magento](https://ja.wikipedia.org/wiki/:en:Magento "wikilink")\[4\]と比較するとEC-CUBEの機能は少なく\[5\]、また取り扱う商品数の増加に伴う速度劣化が著しい。しかし、[ドラッグ&ドロップによるレイアウト編集など独特な機能もある](../Page/ドラッグ・アンド・ドロップ.md "wikilink")。また、日本の主要携帯電話キャリアに対応したページ生成機能を実装している。

<!-- end list -->

  - 日本語文字コードは[UTF-8](../Page/UTF-8.md "wikilink")をデフォルトでサポートしている。
  - [ホスティングサーバ](../Page/ホスティングサーバ.md "wikilink")へのインストールに際しては、[ディレクトリ](../Page/ディレクトリ.md "wikilink")やファイルに対する[パーミッション設定を丁寧に行う必要がある](../Page/ファイルパーミッション.md "wikilink")。（コミュニティ版には、パーミッションの自動設定を行うプログラムが付属する。）
  - 携帯電話向けのページが自動で生成される。携帯電話からアクセスすると自動的に携帯電話向けのページに転送される。2.11系からは、スマートフォンにも対応している。
  - 2.11系は詳細な仕様が存在せず、コード品質のばらつきや実装予定で中断している箇所、修正されていないエラーやコメント等が多く見受けられるため、カスタマイズを行う場合は情報収集や推測、ある程度の割り切りを要する。

## 動作環境

**[スクリプト言語](../Page/スクリプト言語.md "wikilink")**

  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink") 7.1 〜
      - 必須PHPライブラリ
          - pgsql / mysqli (利用するデータベースに合わせること)
          - pdo_pgsql / pdo_mysql / pdo_sqlite (利用するデータベースに合わせること)
          - pdo
          - phar
          - mbstring
          - zlib
          - ctype
          - session
          - JSON
          - xml
          - libxml
          - OpenSSL
          - zip
          - cURL
          - fileinfo
          - intl
      - 推奨PHPライブラリ(決済モジュール等で使用)
          - hash
          - APCu / WinCache(利用する環境に合わせること)
          - Zend OPcache

**[Webサーバ](../Page/Webサーバ.md "wikilink")**

  - [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink") 2.4.x

**[データベース](../Page/関係データベース管理システム.md "wikilink")**

  - [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink") 9.2.x / 10.x
  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink") 5.5.x / 5.6.x / 5.7.x

## 脆弱性など

  - JVN\#06372244 「EC-CUBE ペイメント決済モジュール」および ECCUBE 用「GMO-PG 決済モジュール (PG マルチペイメ ントサービス)」における複数の脆弱性（2018 年8月9日）
  - JVN\#59436681 「EC-CUBE 用モジュール「ルミーズ決済モジュール(2.11系・2.12系・2.13系)」における複数の脆弱性」
  - JVN\#29343839 「EC-CUBE 用プラグイン「Amazon Payプラグイン2.12、2.13」におけるクロスサイトスクリプティングの脆弱性」
      - 「EC-CUBEをCMSとして採用した通販サイト」からの流出として、2019年において約14万件のクレジットカード情報がEC-CUBEの一部のバージョンから流出したと2019年12月20日に経済産業省が発表\[6\]。
      - インターネット通販サイトから流出したクレジットカード情報は34万件に登り、その4分の3以上が「EC-CUBEをCMSとして採用した通販サイト」であるとしている（2019年12月28日、産経新聞）\[7\]。

## EC-Cubeの派生プラットフォーム

  - [EC Orange](https://ja.wikipedia.org/wiki/EC_Orange "wikilink")

## 出典

## 関連項目

  - [イルグルム](https://ja.wikipedia.org/wiki/イルグルム "wikilink")

## 外部リンク

  - [EC-CUBE公式サイト](https://www.ec-cube.net/)

  - [株式会社イーシーキューブ](https://www.ec-cube.co.jp/)

  - [株式会社ロックオン](https://www.lockon.co.jp/)

  - [EC-CUBE開発コミュニティ](https://xoops.ec-cube.net/) - 公式開発コミュニティサイト

  - [ネットショップの壺](https://tsubo.ec-cube.net/) - 公式ブログ

  -
  -
[Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:大阪市北区の企業](https://ja.wikipedia.org/wiki/Category:大阪市北区の企業 "wikilink") [Category:2018年設立の企業](https://ja.wikipedia.org/wiki/Category:2018年設立の企業 "wikilink")

1.
2.
3.
4.
5.
6.
7.