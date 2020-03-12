> この記事は[MODX](https://ja.wikipedia.org/wiki/MODX)から翻訳されています。


**MODX**（モドエックス,モッドエックス）とは、MODX LLCまたはMODX JAPANによって開発されている[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink") (CMS) の一種で、そのシリーズの総称を指す。[PHPおよび](../Page/PHP_\(プログラミング言語\).md "wikilink")[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")環境にて動作する。

[MODX Evolutionと](https://ja.wikipedia.org/wiki/MODX_Evolution "wikilink")[MODX Revolutionに分類され](https://ja.wikipedia.org/wiki/MODX_Revolution "wikilink")、それぞれ別々のCMSとなっている。

## 歴史

EtomiteがMODXの前身となっている。2004年9月、Etomite用の機能拡張である「DocVar」がリリースされる。現在のMODXに備わっている「テンプレート変数」機能の元祖となったもので、これにより投稿画面上のカスタムフィールドの自由な拡張が可能になった。これに興味を示したRyan Thrashは、DocVarの開発を受け継ぎ、フォーラム内で意見交換を深める。

その一方でEtomite本体はAlex（原作者）のアクティビティが低下し、開発の停滞と共にプロジェクト継続に限界が感じられるようになった。2005年3月19日を境に、Ryanが関連する話題はEtomiteフォーラムから削除される。これを契機にプロジェクトの独立を決意、Etomiteに代わるCMSとして、Raymond Irving と共にMODXの開発が始まった。

2ヶ月後、有能な設計技術者であるJason Cowardを開発チームに迎え、開発においては彼がリーダーシップをとる形でMODXプロジェクトは大きな推進力を得る。同年夏に「プレビューテック版」としてMODXが初めてリリースされる。この時点では見た目はEtomiteとほとんど変わらなかったが、DocVarをネイティブにコアに組み込んだ「テンプレート変数」やプラグイン仕様などが追加され、シンプルさを損なわないままさらに高度な拡張が可能となった。小粒で扱いやすいCMSであるEtomiteをベースとしながらも、拡張性の高さが加わったことで、MODXはフレームワーク的なサイト管理ツールを志向することとなる。

その後、数回のプレビューテック版のリリースを通じてコミュニティ参加者との意思疎通を図り、基礎的な仕様をまとめ、秋に初のベータ版がリリースされた。ベータ版としての期間はその後4年に及び、この間にMODXは２つのシリーズに分かれて開発されることが正式に決定した。2009年8月1日、Evolutionシリーズが最初に正式版としてリリース。さらに翌年2010年7月、Revolutionシリーズ正式版がリリースされた。

EvolutionシリーズはDmytro Lukianenko、RevolutionシリーズはJason Cowardがコミットリーダーとしてそれぞれ開発を進めている。

2012年5月25日、新シリーズ「MODX 3」の開発開始が宣言される。2013年中のリリースを目指す。

2012年6月頃より、RevolutionシリーズコミットリーダーであるShaunのアクティビティが大幅に低下。

2013年3月、Evolutionシリーズの開発が再開される。

2013年4月、Shaunなど複数の開発メンバーがSiphonLabs社に移籍。

## 特徴

MODXは共通して以下の特徴を兼ね備えている。

  - ツリー状にサイトを管理
  - HTML基準のテンプレート
  - ページのキャッシュ機能

## 種類

MODXの種類は以下の通りである。

### MODX

ベータバージョン。

正式版は、[MODX Evolutionと](https://ja.wikipedia.org/wiki/MODX_Evolution "wikilink")[MODX Revolutionに分かれた](https://ja.wikipedia.org/wiki/MODX_Revolution "wikilink")。

### [MODX Evolution](https://ja.wikipedia.org/wiki/MODX_Evolution "wikilink")

省メモリ・高速動作が特徴。 2013年3月より開発体制が刷新された。日本版開発者・ウクライナ版開発者・ドイツ人デベロッパーの3人で構成される。

### [MODX Revolution](https://ja.wikipedia.org/wiki/MODX_Revolution "wikilink")

管理画面のインターフェイスや内部コアが一新された。全面的にExtJSが採用され、Evolutionと比べ操作性が格段に向上している。内部構造的にはPDOノウハウを意識しており、新しくxPDO (OpenExpedio) と呼ばれるライブラリ（開発の進捗についてはフォーラム参照）が導入される。スニペットコールなどの書式がEvolutionと異なるため、デザインワークに影響する。これを考慮し、書式変換ツールが提供される予定。

Revolutionは、本格的な管理画面を持つフレームワークとして、他に見られない独特の存在感を示す。管理画面も枠組みとして提供され、サイトの目的に応じてメニュー構成や機能を自在に組み立てるものとなる。

### MODX3

2012年5月25日に開発が宣言された。 管理画面の大幅なインターフェイスを一新して、EvolutionとRevolutionそれぞれの長所を兼ね備えることを目指している。

2014年2月現在、リリースされる目処は立っていない。

## クラウド版

MODX Revolutionのクラウド版として[MODX Cloudが提供されている](https://ja.wikipedia.org/wiki/MODX_Cloud "wikilink")。

オンライン上で手軽にMODXサイトを構築することができ、簡単にバックアップやバージョンアップを行うことができる。

無料版と有料版が提供されている。

## テンプレート

MODXのテンプレートは基本的にHTMLがベースとなっている。

HTMLのテンプレートにMODXタグを加えることによってMODXのテンプレートを作ることができる。

### MODXタグ

MODXテンプレート作成に主に使われる主なMODXタグは以下の通りである。

| 名前      | Evolution           | Revolution                          |
| ------- | ------------------- | ----------------------------------- |
| サイトの名前  | \[(site_name)\]    | \[\[++site_name|++site_name\]\]   |
| サイトURL  | \[(site_url)\]     | \[\[++site_url|++site_url\]\]     |
| ページタイトル | \[\*pagetitle\*\]   | \[\[\*pagetitle|\*pagetitle\]\]     |
| 概要      | \[\*description\*\] | \[\[\*description|\*description\]\] |
| 本文      | \[\*content\*\]     | \[\[\*content|\*content\]\]         |

## 日本公式サイト

  - [日本公式MODX JAPAN 設立に向けて](http://modxcms.com/forums/index.php/topic,28139.0.html)

2008年7月18日、日本コミュニティモデレータチームと本家開発チームのライアンとの音声対談が実現（Skype利用）。これをきっかけに、公式拠点を国内に整備する流れが加速。対談を通じて、日本の開発者による数々のリソースやセキュリティ対策が海外で大きく評価されていることも知ることができた。

2009年1月11日に[MODX日本公式サイト](http://modx.jp/)、同年9月1日に[日本公式フォーラム](http://forum.modx.jp/)がオープン。

2014年2月現在、モデレータ権限などは特に関係なく、Xoops Cubeなどと同様、組織としての形を持たないインフラ的な活動となっている。

## 関連項目

  - [MODX Evolution](https://ja.wikipedia.org/wiki/MODX_Evolution "wikilink")
  - [MODX Revolution](https://ja.wikipedia.org/wiki/MODX_Revolution "wikilink")

## 外部リンク

  - [MODX日本公式サイト](http://modx.jp/)（日本公式ページ）
  - [MODX JAPAN 日本公式フォーラム](http://forum.modx.jp/)（日本公式フォーラム）
  - [MODX デモサイト 管理サイト](http://mng.demo.modx.jp/)（MODXデモサイト）
  - [RixaR-Project](http://www.rixar-project.com/)（MODXユーザーによる解説サイト）
  - [MODX](http://modx.com/)（本家公式ページ）
  - [The MODX Blog](http://modx.com/blog/)（本家公式ブログ）
  - [MODX Community Forums](http://forums.modx.com/)（本家公式フォーラム）
  - [MODX Cloud](https://modxcloud.com/) (MODX Cloud)
  - [modmore.com](https://www.modmore.com/) (modmore)

[Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")