> この記事は[WordPress](https://ja.wikipedia.org/wiki/WordPress)から翻訳されています。


**WordPress**（ワードプレス）は、[オープンソース](../Page/オープンソース.md "wikilink")の[ブログ](../Page/ブログ.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。[PHPで開発されており](../Page/PHP_\(プログラミング言語\).md "wikilink")、[データベース管理システム](../Page/データベース管理システム.md "wikilink")として[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")を利用している（後述の[プラグイン](../Page/プラグイン.md "wikilink")より[SQLite](../Page/SQLite.md "wikilink")での使用も可能）。単なるブログではなく[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink") (CMS) としてもしばしば利用されている。b2/cafelogというソフトウェアの[フォーク](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")（後継）として開発、2003年5月27日に初版がリリースされた\[1\]。[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) の下で配布されている。

## 主な特徴

  - [PHPによる動的なページ生成](../Page/PHP_\(プログラミング言語\).md "wikilink")
  - 標準添付の[テンプレート](../Page/テンプレート.md "wikilink")等が[ウェブ標準](../Page/ウェブ標準.md "wikilink")に準拠
  - 記事への複数カテゴリー設定に対応
  - カスタマイズ可能で[検索エンジン](../Page/検索エンジン.md "wikilink")フレンドリーなURL
  - テーマによる簡単なデザインの切り替え
  - プラグインによる拡張機能
  - [WYSIWYG](../Page/WYSIWYG.md "wikilink")によるエントリ編集
  - 投稿スラッグによるパーマリンク[URL作成](../Page/Uniform_Resource_Locator.md "wikilink")

### ライセンス

WordPressは、[GPLに従い配布される](../Page/GNU_General_Public_License.md "wikilink")、[オープンソース](../Page/オープンソース.md "wikilink")のソフトウェアである。誰もがWordPressの開発に参加できる、という利点がある\[2\]。

### テンプレート、テーマ

WordPressの[テンプレート](../Page/テンプレート.md "wikilink")はすべてPHPであるため、PHPとHTMLをある程度知っていれば容易にテンプレートを[カスタマイズ](https://ja.wikipedia.org/wiki/カスタマイズ "wikilink")できる。テンプレートは多くの場合、ヘッダー部とサイドバー部、コンテンツ部、フッター部、に分けて記述され、1ページはそれらの組み合わせで表示される。WordPressでは、PHPテンプレートにスタイルシートを組み合わせたセットを[テーマ](https://ja.wikipedia.org/wiki/テーマ "wikilink")と呼ぶ。多くの無料テーマが、公式サイトのほか[サードパーティー](../Page/サードパーティー.md "wikilink")から提供されている。テーマの中には、ページを構成する要素をメニューから選択できるウイジェットという機能が使えるものがある。

### プラグイン

様々な機能をプラグインとして追加でき、サードパーティーからも多くのプラグインが開発されている。プラグインはPHPで開発できる。

### 国際化

WordPressは[gettext](https://ja.wikipedia.org/wiki/gettext "wikilink")を利用した[i18n](../Page/国際化と地域化.md "wikilink") (internationalization) をサポートしている。では日本語を含む160以上の地域と言語のプロジェクトが進められており、その半数以上の地域と言語ではコアのほとんどまたは全ての地域化がなされている。同サイトではWordPressのコア以外にもWordPress.orgの各地域・言語毎のサイトやプラグインディレクトリ、テーマディレクトリに掲載されているプラグインやテーマの翻訳なども行われている。

[RTLのような特殊な言語への対応や](https://ja.wikipedia.org/wiki/:en:Right-to-left "wikilink")[CJK圏などにおいて単語数ではなく文字数でカウントするような言語事情考慮も行われるようになっているが](../Page/CJKV.md "wikilink")、対応不十分な部分があるため[日本語](../Page/日本語.md "wikilink")版や[中国語](../Page/中国語.md "wikilink")（[簡体字](https://ja.wikipedia.org/wiki/簡体字 "wikilink")）版などの一部のパッケージでは[パッチ](../Page/パッチ.md "wikilink")プラグインを同梱しているものがある\[3\]。なお、こういったプラグインの有無を除けば英語版とローカライズ版の違いはほぼ言語ファイルの有無のみである\[4\]。

### 動作環境

WordPress 5.2 より動作環境が変更された。

  - PHP バージョン 5.6.20以上（PHP 7.3以上を推奨）
  - MySQL バージョン 5.0以上（MySQL 5.6以上、または[MariaDB](https://ja.wikipedia.org/wiki/MariaDB "wikilink") 10.0以上を推奨）

## リリース

ファイル:WordPress Administration.png|WordPress 1系の管理画面 ファイル:Wordpress27cap.png|WordPress 2系の管理画面 ファイル:WordPress Administration 34 ja.png|WordPress 3.0 - 3.7の管理画面 ファイル:WordPress Administration 38 ja.png|WordPress 3.8 - の管理画面

1.0以降のWordPressの各バージョンでは著名[ジャズ](../Page/ジャズ.md "wikilink")ミュージシャンの名前にちなんだ[コードネーム](../Page/コードネーム.md "wikilink")を採用している。

| バージョン | コードネーム                                                                    | リリース日       | ノート                                                                                                                                                                                                                                                                                                         |
| ----- | ------------------------------------------------------------------------- | ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0.70  |                                                                           | 2003年5月27日  | 前身であるb2/cafelogとおなじファイル構造でリリースされた。現在WordPress Release Archiveのページからダウンロードできる最古の版は0.71-goldである。                                                                                                                                                                                                              |
| 1.2   | *[Mingus](../Page/チャールズ・ミンガス.md "wikilink")*                              | 2004年5月22日  | この版ではプラグインがサポートされた。このときに採用されたのと同じ構造のプラグイン識別ヘッダーが以降のWordPressでも使われている。                                                                                                                                                                                                                                       |
| 1.5   | *[Strayhorn](https://ja.wikipedia.org/wiki/ビリー・ストレイホーン "wikilink")*       | 2005年2月17日  | この版ではいくつかの重要な機能が追加された。そのひとつは静的なページの機能が追加されたことである。これは通常の時系列で管理されるブログ記事とは別のページを生成し管理することを可能としたもので、WordPressが単なるブログ管理ソフトからコンテンツ管理システムへと移行するはじめの一歩であった。この版で追加されたもうひとつの重要な機能は、新しいテンプレート/テーマの機構である。これによって、ユーザーが簡単に外観を切り替えることが可能になった。また、Michel Heilemannによってデザインされたあたらしいデフォルトのテンプレート（コードネーム: Kubrick）が同梱されるようになった。 |
| 2.0   | *[Duke](../Page/デューク・エリントン.md "wikilink")*                                | 2005年12月31日 | この版ではシステムのバックエンドが大幅に書き換えられたのに加え、WYSIWYG編集、管理ツールの改善、画像のアップローダー、投稿速度の改善、インポート機構の改善など多数の改善が行われた。またプラグインの開発者向けの様々な改善が行われた。                                                                                                                                                                                      |
| 2.1   | *[Ella](../Page/エラ・フィッツジェラルド.md "wikilink")*                              | 2007年1月22日  | セキュリティ面での改善に加え、内蔵のスペルチェッカーとオートセーブ機能などを備えた編集機能の強化や、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")のデザインの修正が行われた。検索エンジンに対するプライバシーオプションや、データベースの最適化なども含まれる。                                                                                                                                                     |
| 2.2   | *[Getz](../Page/スタン・ゲッツ.md "wikilink")*                                   | 2007年5月16日  | この版ではウィジェットがサポートされた。また、完全なAtomフィードの機能の追加や、速度的な改善が行われた。                                                                                                                                                                                                                                                      |
| 2.3   | *[Dexter](../Page/デクスター・ゴードン.md "wikilink")*                              | 2007年9月24日  | この版ではタグ機能、新しいカテゴリーの分類法、アップデートの通知機能などが追加された。                                                                                                                                                                                                                                                                 |
| 2.5   | *[Brecker](../Page/マイケル・ブレッカー.md "wikilink")*                             | 2008年3月29日  | 2.4のリリースはされなかったため、この版にはメジャーリリース2回分の新しいコードが含まれている。この版では管理インタフェースの大幅な改善や、個別のページを含む検索機能などが追加された。                                                                                                                                                                                                               |
| 2.6   | *[Tyner](../Page/マッコイ・タイナー.md "wikilink")*                                | 2008年7月15日  | この版ではWordPressがより強力なCMSとなるためのいくつかの新しい機能が追加された。そのひとつは編集履歴を追跡する機能で、[ウィキ](../Page/ウィキ.md "wikilink")のように投稿やページに加えられた変更点を知ることができるようになった。また、「Press This」投稿ブックマークレットを用いて、Webのどこからでも記事を書くことができるようになった。ほかにも2.5で導入された機能に対する多数の改善が含まれる。                                                                               |
| 2.7   | *[Coltrane](../Page/ジョン・コルトレーン.md "wikilink")*                            | 2008年12月11日 | この版では再び管理インターフェースの全面的な改善が行われ、ユーザーによる自由なカスタマイズが可能となった。またWordPress本体の自動アップグレードの機能が追加され、手動でファイルを展開しなくても、管理インターフェースからの操作によりアップグレードが可能となった。                                                                                                                                                                      |
| 2.8   | *[Baker](../Page/チェット・ベイカー.md "wikilink")*                                | 2009年6月10日  |                                                                                                                                                                                                                                                                                                             |
| 2.9   | *[Carmen](https://ja.wikipedia.org/wiki/カーメン・マクレエ "wikilink")*            | 2009年12月19日 | この版で追加された主な機能は、記事や画像を復元可能な状態として残すゴミ箱機能、画像のリサイズや切抜きを行える編集機能、プラグインの互換性の自動通知機能、[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")をはじめとする動画の埋め込み補助機能の4つである。この他に報告されていた500以上の不具合が解消された。しかし、公開直後に予約投稿機能が正常に機能しない重大な不具合が発見され、即座に2.9.1が公開された。                                                              |
| 3.0   | *[Thelonious](../Page/セロニアス・モンク.md "wikilink")*                           | 2010年6月17日  | この版でWordPressとWordPress MUが統合され、複数のユーザでブログを管理できるようになった。                                                                                                                                                                                                                                                     |
| 3.1   | *[Reinhardt](../Page/ジャンゴ・ラインハルト.md "wikilink")*                          | 2011年2月14日  | 管理バーが搭載されたり、ネットワーク管理画面が変更されたり、インポート・エクスポートシステムの大幅な改良がされたり、タクソノミーやカスタムフィールドクエリの機能に対応されたりした。                                                                                                                                                                                                                  |
| 3.2   | *[Gershwin](../Page/ジョージ・ガーシュウィン.md "wikilink")*                          | 2011年7月5日   | 動作のための最低要件がPHP 5.2.4以上・MySQL 5.0以上になり、IE6以前のブラウザをサポートしなくなった。それにより、ダッシュボードのデザインを変更したり、管理バーのボタンがいくつか追加されたり、デフォルトのテーマがHTML5でつくられたTwenty Elevenに変更されたりした。自動アップグレードの機能では、新しいリリースで変更されたファイルのみをダウンロードするようになったため、自動アップデートが高速化した。また、「自由について」・「クレジット」の画面が管理画面に追加された。                                                  |
| 3.3   | *[Sonny](https://ja.wikipedia.org/wiki/ソニー・スティット "wikilink")*             | 2011年12月13日 | 新しいユーザーエクスペリエンスや、ナビゲーション、アップロード機能、インポート機能などを向上した。                                                                                                                                                                                                                                                           |
| 3.4   | *[Green](../Page/グラント・グリーン.md "wikilink")*                                | 2012年6月14日  | テーマカスタマイザーが追加された。使用中のテーマや使用を検討しているテーマを、実際の変更を適用することなく見栄えや設定の変更を試すことができるようになった。                                                                                                                                                                                                                              |
| 3.5   | *[Elvin](../Page/エルビン・ジョーンズ.md "wikilink")*                               | 2012年12月12日 | 画像アップロードやギャラリー作成のフローを大幅に更新した。Twenty Twelveが新しいデフォルトテーマになった。ダッシュボードのスタイルが更新された。管理画面がRetinaディスプレイ対応した。カラーピッカーが新しくなった。管理画面にてあまり使われない機能は目立たないように整理された。                                                                                                                                                          |
| 3.6   | *[Oscar](../Page/オスカー・ピーターソン.md "wikilink")*                              | 2013年8月2日   | 投稿内容の損失を防ぐ自動保存および投稿ロック機能、音声および動画ファイルへのネイティブサポート、そしてSpotify、Rdio、SoundCloudへの対応改善などが追加された。また、Twenty Thirteenが新しいデフォルトテーマになった。                                                                                                                                                                                |
| 3.7   | *[Basie](../Page/カウント・ベイシー.md "wikilink")*                                | 2013年10月24日 | 本体や翻訳ファイルの自動アップデート機能が搭載された。他にも、パスワードの強度確認のアルゴリズムを強化した。                                                                                                                                                                                                                                                      |
| 3.8   | *[Parker](../Page/チャーリー・パーカー.md "wikilink")*                              | 2013年12月14日 | 管理画面のスタイルの大幅な変更がされた。また、Twenty Fourteenが新しいデフォルトテーマになった。                                                                                                                                                                                                                                                     |
| 3.9   | *[Jimmy](../Page/ジミー・スミス.md "wikilink")*                                  | 2014年4月16日  | 画像編集機能の改善、[ドラッグ・アンド・ドロップ](../Page/ドラッグ・アンド・ドロップ.md "wikilink")への対応、音楽・映像のギャラリー対応・ウィジェット及びヘッダーのライブプレビュー機能の追加等が行われた。                                                                                                                                                                                          |
| 4.0   | *[Benny](../Page/ベニー・グッドマン.md "wikilink")*                                | 2014年9月4日   | メディア管理の改善、埋め込み機能の改善、エディターの改善、プラグイン検索機能の改善、英語版との言語切替が容易になる機能の組み込み等。                                                                                                                                                                                                                                          |
| 4.1   | *[Dinah](../Page/ダイナ・ワシントン.md "wikilink")*                                | 2014年12月19日 | 新しいブログテーマTwenty Fifteenの追加、集中執筆モードの追加、言語切替が容易になる機能の追加、ログインセクションの管理、[Vine動画への対応等](https://ja.wikipedia.org/wiki/Vine_\(アプリケーション\) "wikilink")。                                                                                                                                                               |
| 4.2   | *[Powell](../Page/バド・パウエル.md "wikilink")*                                 | 2015年4月24日  | Press Thisの機能強化、[絵文字](../Page/絵文字.md "wikilink")などの拡張文字への対応、[Tumblr](../Page/Tumblr.md "wikilink")や[Kickstarter](https://ja.wikipedia.org/wiki/Kickstarter "wikilink")への対応等。                                                                                                                                |
| 4.3   | *[Billie](../Page/ビリー・ホリデイ.md "wikilink")*                                | 2015年8月18日  | メニューの作成、更新、位置の管理をカスタマイザーでライブプレビューできる機能、特定の記号入力による書式設定機能の追加等。                                                                                                                                                                                                                                                |
| 4.4   | *[Clifford](../Page/クリフォード・ブラウン.md "wikilink")*                           | 2015年12月8日  | 新しいデフォルトテーマ Twenty Sixteen、新しい oEmbed プロバイダの追加、タームのメタデータをサポート、コメントクエリの改善等。                                                                                                                                                                                                                                  |
| 4.5   | *[Coleman](../Page/コールマン・ホーキンス.md "wikilink")*                            | 2016年4月12日  | 編集機能の改善等。                                                                                                                                                                                                                                                                                                   |
| 4.6   | *[Pepper](https://ja.wikipedia.org/wiki/ペッパー・アダムス "wikilink")*            | 2016年8月16日  | アップデート機能の合理化、ネイティブフォントのサポート、インラインリンクチェッカー、コンテンツリカバリーによるエディタの改善等。                                                                                                                                                                                                                                            |
| 4.7   | *[Vaughan](../Page/サラ・ヴォーン.md "wikilink")*                                | 2016年12月6日  | 新しいデフォルトテーマ Twenty Seventeen、ライブプレビューにおいて動画ヘッダー、カスタムCSS、PDFプレビューなどをサポート等。                                                                                                                                                                                                                                   |
| 4.8   | *[Evans](../Page/ビル・エヴァンス.md "wikilink")*                                 | 2017年6月8日   | 画像、音声、動画、リッチテキストのウィジェット機能改善など。Internet Explorerバージョン8,9、および10のサポートを終了。                                                                                                                                                                                                                                      |
| 4.9   | *[Tipton](https://ja.wikipedia.org/wiki/:en:Billy_Tipton "wikilink")*     | 2017年12月16日 | カスタマイザーワークフローの改善、シンタックスハイライトとエラーチェックなどコーディング機能の強化等。                                                                                                                                                                                                                                                         |
| 5.0   | *[Bebo](https://ja.wikipedia.org/wiki/:en:Bebo_Valdés "wikilink")*        | 2018年12月7日  | 新しいブロックベースのエディター等。                                                                                                                                                                                                                                                                                          |
| 5.1   | *[Betty](https://ja.wikipedia.org/wiki/:en:Betty_Carter "wikilink")*      | 2019年2月22日  | サイトヘルス機能の導入、エディターの改善等。                                                                                                                                                                                                                                                                                      |
| 5.2   | *[Jaco](../Page/ジャコ・パストリアス.md "wikilink")*                                | 2019年5月7日   | サイトヘルスチェックの追加、PHPエラーからの保護、プラグイン互換性チェック等。                                                                                                                                                                                                                                                                    |
| 5.3   | *[Kirk](../Page/ローランド・カーク.md "wikilink")*                                 | 2019年11月12日 | ブロックエディタの刷新等。                                                                                                                                                                                                                                                                                               |
| 5.4   | *[Adderley](../Page/ナット・アダレイ.md "wikilink")*                              | 2020年3月31日  |                                                                                                                                                                                                                                                                                                             |
| 5.5   | *[Eckstine](https://ja.wikipedia.org/wiki/:en:Billy_Eckstine "wikilink")* | 2020年8月11日  |                                                                                                                                                                                                                                                                                                             |

## WordPress MU

WordPress MUは複数のユーザでブログを管理できるバージョンのWordPressである。これは主にブログホスティングの業者向けに作られている。MUは「Multi-User」の略で、ギリシャ文字μ（ミュー）が用いられることもある。サブブログはサイトのサブディレクトリまたはサブドメインのいずれかに設置でき、メインブログにはサイト内の全てのブログの最新記事や、更新情報などをリスト表示できる。インストールについてはWindows版とMac OS X版、Linux版がある。デフォルトの言語は英語のみであるが、標準版のlanguagesフォルダを流用、またはMUの日本語リソースサイトからja.moとja.poをダウンロードすれば、インストール後の主要な処理メニューを日本語化できる。なおMUのバージョンアップは標準版に準じて行われていた。WordPress 3.0でWordPress MU（マルチサイト）とWordPressを統合。2008年3月28日に配布元のWordPress Japanが同月末のウェブサイト閉鎖を宣言、現在はWordPressへの移行を推奨している。

## わぷー

**わぷー** (Wapuu) はWordPress日本公式[キャラクター](../Page/キャラクター.md "wikilink")。カネウチカズコにより制作され、2011年2月19日に開催されたWordCamp Fukuoka 2011で初公開された\[5\]。WordPressロゴがある丸い物体を好むように抱えている。テーマ・プラグインにわぷーを含めても問題がないよう、わぷーはWordPressと同じく[GPLでライセンスされている](../Page/GNU_General_Public_License.md "wikilink")\[6\]。

キャラクターの名称は投票によって決定した。得票数1位は「ワッピー」だったが、既に[GMOクラウドWEST](https://ja.wikipedia.org/wiki/GMOクラウドWEST "wikilink")が経営しているレンタルサーバのサービス名「@WAPPY」として使われていたため、2位のわぷーが採用される事になった\[7\]。

## 脚注

## 関連項目

  - [ブログ](../Page/ブログ.md "wikilink")
  - [Movable Type](../Page/Movable_Type.md "wikilink")
  - [Local (ソフトウェア)](https://ja.wikipedia.org/wiki/Local_\(ソフトウェア\) "wikilink") - WordPressをローカル環境にインストールするソフトウェア

## 外部リンク

  - [WordPress](https://wordpress.org/)
  - [WordPress](https://ja.wordpress.org/)
  - [WordPress MU](https://mu.wordpress.org/)
  - [WordPress.com](https://wordpress.com/) [Automattic](https://ja.wikipedia.org/wiki/Automattic "wikilink")社によるWordPressのレンタルサービス ([en](https://ja.wikipedia.org/wiki/:en:WordPress.com "wikilink"))
  - [WordPress.com](https://ja.wordpress.com/)
  - [WordPress \> Showcase](https://wordpress.org/showcase/)
  - [わぷーアーカイブ](https://jawordpressorg.github.io/wapuu/)

[Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:Webオーサリングソフト](https://ja.wikipedia.org/wiki/Category:Webオーサリングソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ブログソフト](https://ja.wikipedia.org/wiki/Category:ブログソフト "wikilink") [Category:ウェブサイトの構成](https://ja.wikipedia.org/wiki/Category:ウェブサイトの構成 "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")

1.  すばらしき10年間 - [WordPress › Ten Good Years](https://ja.wordpress.org/2013/06/05/ten-good-years/)
2.  WordPress Codex 日本語版 - [WordPress への協力](https://ja.wordpress.org/support/article/contributing-to-wordpress/)
3.
4.
5.  *[WordPress 日本公式キャラクター名が決定しました](https://ja.wordpress.org/2011/08/10/wordpress-japanese-character-name/)* WordPress 日本語 ブログ, 2012年7月27日参照
6.  *[WordPress 日本公式キャラクターが登場](https://ja.wordpress.org/2011/02/19/wordpress-japan-character/)* WordPress 日本語 ブログ, 2012年7月27日参照
7.