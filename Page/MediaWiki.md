> この記事は[MediaWiki](https://ja.wikipedia.org/wiki/MediaWiki)から翻訳されています。


**MediaWiki**（メディアウィキ）は、[GNU General Public Licenseで配布される](../Page/GNU_General_Public_License.md "wikilink")[ウィキ](../Page/ウィキ.md "wikilink")ソフトウェアである。[PHPで書かれており](../Page/PHP_\(プログラミング言語\).md "wikilink")、[データベース](../Page/データベース.md "wikilink")として[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")または[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")を使用する。非公式だが[MariaDB](https://ja.wikipedia.org/wiki/MariaDB "wikilink")にも対応している\[1\]\[2\]。

## 概要

MediaWikiは、[ウィキペディア](../Page/ウィキペディア.md "wikilink")の為にらによって作成された。最初はUseModWiki (別名"Phase I") を使用していたが、[2002年](../Page/2002年.md "wikilink")[1月25日](../Page/1月25日.md "wikilink")に新しいバージョン ("Phase II") に切替えられた。その日は、ウィキペディアコミュニティー内では、新ソフトウェアの原作者にちなんで[Magnus Manske Day](https://ja.wikipedia.org/wiki/:en:Wikipedia:Magnus_Manske_Day "wikilink")（マグナス・マンスキーの日）と呼ばれている。

Phase IIソフトウェアを書き直して改良したものは、一時「Phase III」と呼ばれていた。このソフトウェアは、それがウィキペディアだけでなく他のプロジェクトにも使用可能であり、バージョン番号の必要性があるという背景により、MediaWikiと改名された。この名前は、ウィキペディアの母組織である[ウィキメディア財団](../Page/ウィキメディア財団.md "wikilink")をもじったものである。プロジェクトに新たに参加した人を混乱に招くという理由で、この名称のウィキメディアとの類似性がしばしば非難されている。

## 開発史

[Magnus_Manske.png](https://ja.wikipedia.org/wiki/File:Magnus_Manske.png "fig:Magnus_Manske.png") [Lee_Daniel_Crocker.JPG](https://ja.wikipedia.org/wiki/File:Lee_Daniel_Crocker.JPG "fig:Lee_Daniel_Crocker.JPG") [Brion_Vibber_May_2008.JPG](https://ja.wikipedia.org/wiki/File:Brion_Vibber_May_2008.JPG "fig:Brion_Vibber_May_2008.JPG") ウィキペディア立ち上げ当初の2001年1月は、という既存のソフトウェアで駆動しており、記述は[Perl](../Page/Perl.md "wikilink")を採用してすべてのウィキページをテキスト形式で保存していた。ところがすぐに機能面でもパフォーマンスでも制約の多さが目につき始めた。2001年半ばにはという当時ウィキペディアの編集者で[ケルン大学](../Page/ケルン大学.md "wikilink")在籍の大学生開発者が、ウィキペディアに使うUseModWikiの代替となるソフトウェアを書き始める。[PHP](https://ja.wikipedia.org/wiki/PHP "wikilink")を使用し情報はすべて[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")データベースに保存、英語版ウィキペディアには2002年1月に実装し、他の言語版ウィキペディアのサイトでも徐々に実装が進んでいく。このソフトウェアが「PHPスクリプト」あるいは「phase II」と呼ばれたことから、UseModWikiには「phase I」という別名が与えられた。

利用者が増えるにつれて読みこみ速度の問題が再燃したことから、ふたたびソフトウェアの書き換えが始まり、が主導して「phase III」という名前で進行した。この新しいソフトウェアは「phase II」時代の基本的なインターフェースを踏襲しながら、よりスケーラブルになるように記述にPHPを採用、バックエンドにMySQLを置いている。こうして2002年7月にウィキペディアとして動き始めた。

[ウィキメディア財団](../Page/ウィキメディア財団.md "wikilink")の発足は2003年6月20日で7月にはウィキペディアの寄稿者ダニエル・メイヤーからソフトウェアの名称として財団名をもじった「MediaWiki」が提案され\[3\]、その名前は同年8月ごろから徐々に定着した。ただ（意図的とはいえ）財団名に似ているため、しばしば混乱を引き起こしている（財団名そのものも製品である「ウィキペディア」に酷似）\[4\]。「ウィキメディア」という呼称を発案したのはウィキペディア寄稿者で、WikiEN-lメーリングリストに2003年3月6日付に投稿している\[5\]。

製品ロゴは[フロランス・ドゥヴアール](../Page/フロランス・ドゥヴアール.md "wikilink")が撮影した写真に基づいてが制作しており、本来は2003年中盤に行われたウィキペディアの新しいロゴを募集する国際コンテストに提出したもので\[6\]3位に入賞、ウィキペディアではなくMediaWikiの商標として、財団第2のロゴ採用が決定した\[7\]。 ヒマワリを挟む角括弧はMediaWikiが他のウィキページへの[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")作成に用いる[syntaxの象徴で](https://ja.wikipedia.org/wiki/:en:Syntax_of_programming_languages "wikilink")、[ヒマワリ](../Page/ヒマワリ.md "wikilink")が象徴するのはウィキペディアの多様性、たゆまぬ成長と枠にとらわれない面を表す\[8\]。

その後、[ウィキメディア財団](../Page/ウィキメディア財団.md "wikilink")[最高技術責任者](../Page/最高技術責任者.md "wikilink")ブリオン・ヴィッバー（Brion Vibber）\[9\]が更新管理者ならびに最も活発な開発者の役を引き受ける\[10\]\[11\]。

MediaWiki開発の主要なマイルストーンは順に、カテゴリ・システム（2004年追加）、[構文解析](../Page/構文解析.md "wikilink")（2006年追加）、拡張機能[Flagged revisions](https://ja.wikipedia.org/wiki/:en:flagged_revisions "wikilink")（2008年追加）\[12\]、「ResourceLoader」という[CSSならびにJavaScriptの配置システム](../Page/Cascading_Style_Sheets.md "wikilink")（2011年追加）\[13\]、さらに2013年に編集機能の[VisualEditor](https://ja.wikipedia.org/wiki/VisualEditor "wikilink")と[WYSIWYG](../Page/WYSIWYG.md "wikilink")（What You See Is What You Getの頭文字）が追加される\[14\]。

## 利用

[PoweredBy_MediaWiki.svg](https://ja.wikipedia.org/wiki/File:PoweredBy_MediaWiki.svg "fig:PoweredBy_MediaWiki.svg")   MediaWikiは[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であり、誰でもダウンロードして自由に利用できる。

MediaWikiはその当初のターゲットである[ウィキペディア](../Page/ウィキペディア.md "wikilink")、そしてその姉妹プロジェクトである各種の[ウィキメディア・プロジェクト](https://ja.wikipedia.org/wiki/ウィキメディア・プロジェクト "wikilink")群で利用されている。また[Wikia](https://ja.wikipedia.org/wiki/Wikia "wikilink")という、[wikiHow](https://ja.wikipedia.org/wiki/wikiHow "wikilink")、[WikiLeaks](https://ja.wikipedia.org/wiki/WikiLeaks "wikilink")も同様。[チャクウィキ](../Page/チャクウィキ.md "wikilink")といった様々なウェブサイトの構築に使用されている。

ウィキペディアの他にウィキ形式の百科事典でMediaWikiを採用するものを挙げると[アンサイクロペディア](https://ja.wikipedia.org/wiki/アンサイクロペディア "wikilink")、[Citizendium](../Page/Citizendium.md "wikilink")（シチズンジアム）、[スカラーペディア](../Page/スカラーペディア.md "wikilink") 、、[コンサーヴァペディア](https://ja.wikipedia.org/wiki/コンサーヴァペディア "wikilink")がある。また[Novell](https://ja.wikipedia.org/wiki/Novell "wikilink")や[Intel](https://ja.wikipedia.org/wiki/Intel "wikilink")の例のように企業内での採用も多い\[15\]\[16\]

アメリカ政府内部でもMediaWikiを使用し、顕著な例として（採用）、（[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[内務省](../Page/内務省.md "wikilink")採用）ならびに[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[国防総省](https://ja.wikipedia.org/wiki/国防総省 "wikilink")が採用するの一部milWikiにも使われている。[国連機関](https://ja.wikipedia.org/wiki/国連機関 "wikilink")では[国連開発計画](https://ja.wikipedia.org/wiki/国連開発計画 "wikilink")及びが独自ウィキをMediaWikiで駆動すると決定した理由は「ウィキペディアが動くソフトウェアであることから試験が行き届き、将来的にも開発活動が持続可能で、未来の技術者はおそらくどんなウィキソフトウェアよりもMediaWikiに最も触れて育つと予測されるため」だという\[17\]。

[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")は[LibrePlanet](../Page/LibrePlanet.md "wikilink")ウェブサイトの運営にMediaWikiを使っている\[18\]。

### バージョンの履歴

| 色 | 定義           |
| - | ------------ |
| 赤 | サポートされないリリース |
| 緑 | サポートされるリリース  |
| 青 | リリース予定       |

<table>
<thead>
<tr class="header">
<th><p>バージョン数</p></th>
<th><p>リリース日</p></th>
<th><p>リンク</p></th>
<th><p>主な変更点</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.1</p></td>
<td><p><a href="../Page/2003年.md" title="wikilink">2003年</a><a href="../Page/12月8日.md" title="wikilink">12月8日</a></p></td>
<td><p><a href="http://sourceforge.net/project/shownotes.php?release_id=202383&amp;group_id=34373">リリースノート全文</a></p></td>
<td><ul>
<li>あたらしい表組みのウィキマークアップ導入</li>
<li>MediaWiki名前空間の導入により、利用者がインターフェースメッセージ編集可能に</li>
<li><a href="../Page/Extensible_Markup_Language.md" title="wikilink">XML形式のソース出力</a>、履歴のオプション選択付き</li>
<li>マジックワード（特別な機能を持つ文字列や変数）</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1.2</p></td>
<td><p><a href="../Page/2004年.md" title="wikilink">2004年</a><a href="../Page/3月24日.md" title="wikilink">3月24日</a></p></td>
<td><p><a href="http://sourceforge.net/project/shownotes.php?release_id=226003&amp;group_id=34373">リリースノート全文</a></p></td>
<td><ul>
<li>ウェブ上でのインストーラー（実験導入）</li>
<li>画像のリサイズとサムネイルの生成</li>
<li>ウィキマークアップを支援する編集ツールバー</li>
<li>ウィキ内での利用者権限の設定</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1.3</p></td>
<td><p>2004年<a href="../Page/8月11日.md" title="wikilink">8月11日</a></p></td>
<td><p><a href="http://sourceforge.net/project/shownotes.php?release_id=259965&amp;group_id=34373">リリースノート全文</a></p></td>
<td><ul>
<li><a href="../Page/Cascading_Style_Sheets.md" title="wikilink">CSSを多く用い</a>、WWW基準により合致した新しい外装（MonoBookスキン）</li>
<li>引数のとれるテンプレート</li>
<li>カテゴリ機能</li>
<li>可能な場合、編集競合を自動的に統合</li>
<li>インストールの改善</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1.4</p></td>
<td><p><a href="../Page/2005年.md" title="wikilink">2005年</a><a href="../Page/3月20日.md" title="wikilink">3月20日</a></p></td>
<td><p><a href="http://sourceforge.net/project/shownotes.php?release_id=314389&amp;group_id=34373">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.4" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>利用者毎に使用言語が設定可能</li>
<li>パフォーマンスを大幅に改善</li>
<li>ストレージの必要容量を圧縮するための、古い版の圧縮機能</li>
<li>画像ギャラリー（新規アップロードファイルのリスト）の生成</li>
<li>SVG表示のサポート（外部サポートツールが必要）</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:ログ" title="wikilink">特別:ログ</a> (log) 機能の追加</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1.5<br />
<span style="font-weight:normal">(MySQL 3をサポートする最終版)</span></p></td>
<td><p>2005年<a href="../Page/10月5日.md" title="wikilink">10月5日</a></p></td>
<td><p><a href="http://sourceforge.net/project/shownotes.php?release_id=361506&amp;group_id=34373">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.5" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>データベースの大規模な再設計。データベーススキーマを再設計して、堅牢に</li>
<li>リビジョン管理をテキストストレージから分離。これにより
<ul>
<li>ページの移動、ページの履歴の生成など一部の操作のパフォーマンスが大幅に改善</li>
<li>全ての版への固定リンクを提供</li>
<li>データの大部分をデータベースの外に保管可能に</li>
</ul></li>
<li>電子メールを用いた変更通知機能</li>
<li>ページのエンコーディングは必ず<a href="../Page/UTF-8.md" title="wikilink">UTF-8</a>を使用</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:Listadmins" title="wikilink">特別:Listadmins</a>（管理者一覧）を<a href="https://ja.wikipedia.org/wiki/特別:Listusers" title="wikilink">特別:Listusers</a>（登録利用者一覧）へ統合</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1.6<br />
<span style="font-weight:normal">(PHP 4をサポートする最終版)</span></p></td>
<td><p><a href="../Page/2006年.md" title="wikilink">2006年</a><a href="../Page/4月5日.md" title="wikilink">4月5日</a></p></td>
<td><p><a href="http://sourceforge.net/project/shownotes.php?release_id=407308&amp;group_id=34373">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.6" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>MySQLの場合4以降が必須。</li>
<li>利用者のログイン画面とアカウント作成画面を分離</li>
<li><a href="https://ja.wikipedia.org/wiki/mw:Help:Protected_pages/ja" title="wikilink">ページの保護および保護解除の画面を再設計</a>。半保護機能が追加。</li>
<li>バックグラウンドのアップデートに「<a href="https://ja.wikipedia.org/wiki/mw:Manual:Job_queue/ja" title="wikilink">ジョブ・キュー</a>」を使用</li>
<li>テンプレートの使用の追跡を改善</li>
<li>スパム対策の強化として、外部リンクの追跡を導入</li>
<li>テンプレートの引数に初期値設定可能</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:Preferences" title="wikilink">特別:Preferences</a>（個人設定、オプション）の再設計</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1.7</p></td>
<td><p>2006年<a href="https://ja.wikipedia.org/wiki/7月7日" title="wikilink">7月7日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/tags/REL1_7_0/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.7" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>MediaWiki 1.7 以降は PHP 5 が必須 (5.1 推奨)。 PHP 4 はサポート対象外。</li>
<li>削除したファイルが復帰可能に</li>
<li>インポート（取り込み）の操作が<a href="https://ja.wikipedia.org/wiki/特別:ログ" title="wikilink">特別:ログ</a>に記録されるように</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1.8</p></td>
<td><p>2006年<a href="../Page/10月10日.md" title="wikilink">10月10日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/tags/REL1_8_0/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.8" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/PostgreSQL" title="wikilink">PostgreSQL</a> (8.1以降)データベース・バックエンドを完全サポート</li>
<li><a href="../Page/DjVu.md" title="wikilink">DjVu</a>によるサムネイル生成とマルチページ・ナビゲーションをサポート</li>
<li>利用者の投稿ブロック機能の改善。未登録利用者へのブロックに特定のIPアドレスを使用</li>
<li>設定により、公開されているURLからの直接のファイルアップデートが可能に</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1.9</p></td>
<td><p><a href="../Page/2007年.md" title="wikilink">2007年</a><a href="../Page/1月10日.md" title="wikilink">1月10日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/tags/REL1_9_0/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.9" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>版の編集取り消し「Undo」機能</li>
<li>ブロックおよび特別ページのキャッシュを改善</li>
<li>ソータブルテーブル</li>
<li>利用者データベースに編集カウンタ追加</li>
<li>ウォッチリストおよび最近更新したページに版のサイズを表示</li>
<li>「特別」(Special) 名前空間のローカライズが可能に</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1.10</p></td>
<td><p>2007年<a href="../Page/5月9日.md" title="wikilink">5月9日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/tags/REL1_10_0/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.10" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>「カスケード保護」機能の追加</li>
<li>パトロール（巡回）機能の操作が<a href="https://ja.wikipedia.org/wiki/特別:ログ" title="wikilink">特別:ログ</a>に記録されるように</li>
<li>ツールチップおよびアクセスキー機能の改善</li>
<li>ブロックおよび特別ページのキャッシュを改善</li>
<li><a href="https://ja.wikipedia.org/wiki/IPv6" title="wikilink">IPv6</a>をサポート</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1.11</p></td>
<td><p>2007年<a href="../Page/9月10日.md" title="wikilink">9月10日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/tags/REL1_11_0/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.11" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/mw:Manual:$wgAddGroups/ja" title="wikilink">$wgAddGroups</a> および <a href="https://ja.wikipedia.org/wiki/mw:Manual:$wgRemoveGroups/ja" title="wikilink">$wgRemoveGroups</a> の追加。これにより利用者権限のより洗練された設定が可能に</li>
<li>AJAXを用いた閲覧が修正され、デフォルトで使用可能に</li>
<li>ユーザーの投稿記録を年月で抽出できるように</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1.12</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2008年" title="wikilink">2008年</a><a href="../Page/3月20日.md" title="wikilink">3月20日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/tags/REL1_12_0/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.12" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li><a href="../Page/国際化と地域化.md" title="wikilink">国際化と地域化</a>を大幅に促進。多言語対応が進み、<a href="https://ja.wikipedia.org/wiki/特別:Version" title="wikilink">特別:Version</a>（バージョン情報ページ）がローカライズ可能に。またヘブライ暦、タイ暦、イラン暦をサポート。</li>
<li>パーサーの書き換え (<a href="https://ja.wikipedia.org/wiki/meta:Migration_to_the_new_preprocessor" title="wikilink">meta:Migration to the new preprocessor参照</a>)</li>
<li>利用者権限関連のさまざまな変更。 <a href="https://ja.wikipedia.org/wiki/mw:Manual:$wgAddGroups/ja" title="wikilink">$wgAddGroups</a> および <a href="https://ja.wikipedia.org/wiki/mw:Manual:$wgRemoveGroups/ja" title="wikilink">$wgRemoveGroups</a> の振る舞いが変更され、<a href="https://ja.wikipedia.org/wiki/mw:Manual:$wgGroupsAddToSelf/ja" title="wikilink">$wgGroupsAddToSelf</a> および <a href="https://ja.wikipedia.org/wiki/mw:Manual:$wgGroupsRemoveFromSelf/ja" title="wikilink">$wgGroupsRemoveFromSelf</a> が追加。</li>
<li>未作成ページに対する直接保護機能及び、<a href="https://ja.wikipedia.org/wiki/特別:Protectedtitles" title="wikilink">特別:Protectedtitles</a>（作成保護されているページ名）の特別ページ追加</li>
<li>拡張機能の<a href="https://ja.wikipedia.org/wiki/mw:Extension:Filepath" title="wikilink">Filepathがデフォルトで追加される</a></li>
<li>ページの履歴統合機能の追加（デフォルトでは使用不可）</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1.13</p></td>
<td><p>2008年<a href="../Page/8月14日.md" title="wikilink">8月14日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/tags/REL1_13_0/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.13" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>新しい特別ページ：<a href="https://ja.wikipedia.org/wiki/特別:FileDuplicateSearch" title="wikilink">特別:FileDuplicateSearch</a>（重複ファイル検索）、<a href="https://ja.wikipedia.org/wiki/特別:ListGroupRights" title="wikilink">特別:ListGroupRights</a>（利用者グループの権限）</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:UserRights" title="wikilink">特別:UserRights</a>（利用者グループ権限操作ページ）がチェックボックス式に仕様変更。</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:SpecialPages" title="wikilink">特別:SpecialPages</a>（特別ページ一覧）がカテゴリ分けされる。</li>
<li>隠しカテゴリ (<code>__HIDDENCAT__</code>) の導入。カテゴリページに記述するとカテゴリに含まれる記事にそのカテゴリが表示されなくなる。</li>
<li>二重リダイレクトの自動修正</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:ログ" title="wikilink">特別:ログ</a>機能を年月で抽出できるように</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1.14</p></td>
<td><p><a href="../Page/2009年.md" title="wikilink">2009年</a><a href="../Page/2月22日.md" title="wikilink">2月22日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/branches/REL1_14/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.14" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>検索エンジンのインデックスを各ページごとに制御可能なマジックワード (<code>__NOINDEX__</code>・<code>__INDEX__</code>)の導入。</li>
<li>リダイレクトページのプレビューがリダイレクトとして表示されるように</li>
<li>モバイルデバイスのためのよりよいCSSサポート</li>
<li>ページの履歴版を年月で抽出できるように</li>
<li>アップロードされたファイルの履歴ページにすべてのファイルバージョンのサムネイルを表示</li>
<li>特別ページの名前のエイリアス表示をローカライズで表示可能に。</li>
<li>パスワード変更の特別ページ（<a href="https://ja.wikipedia.org/wiki/特別:パスワードの変更" title="wikilink">特別:パスワードの変更</a>）追加</li>
<li>ブロックされているユーザーの期間設定をそのまま変更できるように</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:Statistics" title="wikilink">特別:Statistics</a>（サイトの統計）の仕様変更</li>
<li>個人設定で「初期設定に戻す」の追加</li>
<li>拡張機能の<a href="https://ja.wikipedia.org/wiki/mw:Extension:Newuserlog" title="wikilink">Newuserlog</a>、<a href="https://ja.wikipedia.org/wiki/mw:Extension:LinkSearch" title="wikilink">LinkSearch</a>、<a href="https://ja.wikipedia.org/wiki/mw:Extension:DeletedContributions" title="wikilink">DeletedContributionsをコアへ導入</a>。</li>
<li>ページ移動の際に移動元のページ（リダイレクト）を非作成にするsuppressredirect機能追加。</li>
<li>ファイルページが移動可能に</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1.15</p></td>
<td><p>2009年<a href="../Page/6月10日.md" title="wikilink">6月10日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/branches/REL1_15/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.15" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>個人設定に性別指定機能とユーザーCSSのリンクを追加</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:登録利用者一覧" title="wikilink">登録利用者一覧に利用者が登録された年月と時間が追加</a></li>
<li><a href="https://ja.wikipedia.org/wiki/特別:タグ一覧" title="wikilink">有効な変更タグ特別ページの追加</a></li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.16" title="wikilink">1.16</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2010年" title="wikilink">2010年</a><a href="../Page/7月28日.md" title="wikilink">7月28日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/branches/REL1_16/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.16" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>個人設定内のレイアウトが変更</li>
<li>ベクター (Vector) スキンの追加</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:活動中の利用者" title="wikilink">活動中の利用者一覧の特別ページ追加</a></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.17" title="wikilink">1.17</a></p></td>
<td><p><a href="../Page/2011年.md" title="wikilink">2011年</a><a href="../Page/6月22日.md" title="wikilink">6月22日</a></p></td>
<td><p><a href="https://svn.wikimedia.org/viewvc/mediawiki/branches/REL1_17/phase3/RELEASE-NOTES?view=markup">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.17" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>利用者がすべてのスキンで共通に利用できるCSSとJavascriptを設置できるようになった。</li>
<li>インストーラーが刷新される。</li>
<li><a href="https://ja.wikipedia.org/wiki/mw:ResourceLoader" title="wikilink">ResourceLoaderの追加</a>。</li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.18" title="wikilink">1.18</a><br />
<span style="font-weight:normal">(MySQL 4をサポートする最終版)</span></p></td>
<td><p>2011年<a href="../Page/11月28日.md" title="wikilink">11月28日</a></p></td>
<td><p><a href="https://gerrit.wikimedia.org/r/gitweb?p=mediawiki/core.git;a=blob;f=RELEASE-NOTES-1.18;hb=REL1_18">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.18" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>いくつかのExtensionが標準のパッケージに同封される。</li>
<li>Mathのサポートがコアより切り離される。</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:ブロック一覧" title="wikilink">ブロック一覧の特別ページ仕様変更</a></li>
<li>パスワード再発行のための特別ページ（<a href="https://ja.wikipedia.org/wiki/特別:パスワード再設定" title="wikilink">特別:パスワード再設定</a>）追加</li>
<li>特別ページ一覧のカテゴリ分け表示をセクションに変更</li>
<li>ページ新規作成の際に「細部の編集」のチェックができなくなる。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.19" title="wikilink">1.19</a> (LTS)<br />
<span style="font-weight:normal">(PHP 5.2.3をサポートする最終版)</span></p></td>
<td><p><a href="../Page/2012年.md" title="wikilink">2012年</a><a href="../Page/5月2日.md" title="wikilink">5月2日</a></p></td>
<td><p><a href="https://gerrit.wikimedia.org/r/gitweb?p=mediawiki/core.git;a=blob;f=RELEASE-NOTES-1.19;hb=REL1_19">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.19" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>MySQLバージョン5.0.2が必要</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:投稿記録" title="wikilink">特別:投稿記録</a>、ページの履歴にもバイトの変更(増減)数が表示</li>
<li>署名のデフォルト表示に、トークページのリンクも表示</li>
<li>投稿記録ページに「対応付けられた名前空間」のチェックが追加</li>
<li>メールアドレス変更の特別ページ（<a href="https://ja.wikipedia.org/wiki/特別:メールアドレスの変更" title="wikilink">特別:メールアドレスの変更</a>）追加。またこれによりメールアドレスの変更には必ずパスワードの入力が必要となった。</li>
<li>ページ移動の際、新しいページ名の入力部分に名前空間のドロップダウンが追加。</li>
<li>利用者名秘匿のブロックを行う際、「ブロックの確認」のチェックが必須となる。</li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.20" title="wikilink">1.20</a></p></td>
<td><p><a href="../Page/2012年.md" title="wikilink">2012年</a><a href="../Page/11月6日.md" title="wikilink">11月6日</a></p></td>
<td><p><a href="https://gerrit.wikimedia.org/r/gitweb?p=mediawiki/core.git;a=blob;f=RELEASE-NOTES-1.20;hb=REL1_20">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/translatewiki:Translating:MediaWiki/statistics/1.20" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>PHPバージョン5.3.2が必要。</li>
<li>差分表示の色の変更。またページタイトルに「:版間の差分」が追加される</li>
<li>右上のログインページリンクに、アカウント作成ページへのリンクも直接表示</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:バージョン情報" title="wikilink">特別:バージョン情報</a>に、エントリーポイントのURL(パス、api,load.php)のリンクが表示</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:登録利用者一覧" title="wikilink">特別:登録利用者一覧</a>に、利用者のトークページと投稿記録のリンクが表示</li>
<li>編集ページの要約入力欄が、細部編集やウォッチリスト追加のチェックボックスより少し上に。</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:MostInterwikis" title="wikilink">特別:MostInterwikis</a>(ウィキ間リンクの多いページ)の特別ページ追加</li>
<li>現在のページIDを表示するマジックワード<code>{{PAGEID}}</code>の追加</li>
</ul></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.21" title="wikilink">1.21</a></p></td>
<td><p><a href="../Page/2013年.md" title="wikilink">2013年</a><a href="../Page/5月25日.md" title="wikilink">5月25日</a></p></td>
<td><p><a href="https://gerrit.wikimedia.org/r/gitweb?p=mediawiki/core.git;a=blob;f=RELEASE-NOTES-1.21">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localisation_statistics" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>新しい<a href="https://ja.wikipedia.org/wiki/mw:ContentHandler" title="wikilink">ContentHandler</a></li>
<li>1.18で同封があったExtensionで、さらに9つのExtensionが標準のパッケージに同封される。</li>
<li>ツールボックスにページ情報（基本情報、保護状態、編集履歴など）の特別ページ(&amp;action=info)追加。さらに利用者ページにアクセスした場合、ツールボックスに<a href="https://ja.wikipedia.org/wiki/特別:利用者権限" title="wikilink">特別:利用者権限</a>のリンクが直接表示され、利用者名を指定せずに権限が操作できるようになった。</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:PagesWithProp" title="wikilink">ページプロパティがあるページ</a>（マジックワード使用状況）の特別ページ追加</li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.22" title="wikilink">1.22</a></p></td>
<td><p>2013年<a href="../Page/12月6日.md" title="wikilink">12月6日</a></p></td>
<td><p><a href="https://gerrit.wikimedia.org/r/gitweb?p=mediawiki/core.git;a=blob;f=RELEASE-NOTES-1.22">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localisation_statistics" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>Chick, Classic, MySkin, Nostalgia, Simpleの五つのスキンと、「曖昧さ回避ページにリンクしているページ」の特別ページをそれぞれ廃止</li>
<li>ベクタースキンのアップグレード。</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:ResetTokens" title="wikilink">特別:ResetTokens</a>（トークンの再設定）、<a href="https://ja.wikipedia.org/wiki/特別:転送" title="wikilink">特別:転送</a>（ファイル名、利用者ID、版IDでの転送）の特別ページ追加</li>
<li>バージョン情報ページにMediaWikiの開発者を列挙した特別ページのサブページを追加</li>
<li>ログインページとアカウント作成の特別ページの画面を大幅に変更。アカウント作成ページにはサイトのページ数や編集数、活動利用者数が表示されるようになった。</li>
<li>編集機能の改善。編集ページ下部の著作権メッセージ及び編集ボタン周辺にグレーの背景色を指定。またプレビュー時に「パーサーのプロファイリングデータ」が最下部に追加された。</li>
<li>拡張機能の<a href="https://ja.wikipedia.org/wiki/mw:Extension:PostEdit" title="wikilink">PostEdit</a>、<a href="https://ja.wikipedia.org/wiki/mw:Extension:Vector" title="wikilink">Vectorをコアへ導入</a>。これによりページ保存後には、メッセージが表示されるようになった。</li>
<li>左のサイドバーの案内リンクが標準でメインページ、<a href="https://ja.wikipedia.org/wiki/特別:最近の更新" title="wikilink">特別:最近の更新</a>、<a href="https://ja.wikipedia.org/wiki/特別:おまかせ表示" title="wikilink">特別:おまかせ表示</a>のみになった。</li>
<li>カテゴリページの下位カテゴリリンク左に矢印のアイコンを付加</li>
</ul></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.23" title="wikilink">1.23</a> (LTS)</p></td>
<td><p><a href="../Page/2014年.md" title="wikilink">2014年</a><a href="https://ja.wikipedia.org/wiki/6月5日" title="wikilink">6月5日</a></p></td>
<td><p><a href="https://git.wikimedia.org/blob/mediawiki%2Fcore.git/master/RELEASE-NOTES-1.23">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localisation_statistics" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>ベクターのCSSの更新。ページタイトルの文字の大きさが若干変更したりしている。</li>
<li>スパム対策とカウンタ荒らしの改善</li>
<li>通知機能の追加</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:バージョン情報" title="wikilink">特別:バージョン情報</a>の表が若干変更。拡張機能のライセンス情報等が追加</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:投稿記録" title="wikilink">特別:投稿記録</a>にページ作成（初版）投稿のみを抽出するチェックボックスの追加</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:最近の更新" title="wikilink">特別:最近の更新</a>のオプション項目に、ページ内の各種記号やページサイズの増減を解説する「凡例」の追加</li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.24" title="wikilink">1.24</a></p></td>
<td><p>2014年<a href="https://ja.wikipedia.org/wiki/11月26日" title="wikilink">11月26日</a></p></td>
<td><p><a href="https://git.wikimedia.org/blob/mediawiki%2Fcore.git/master/RELEASE-NOTES-1.24">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localization_statistics" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>ページタイトルやセクションの文字フォントが若干変更</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:バージョン情報" title="wikilink">特別:バージョン情報</a>に「インストール済み外装」の表を追加。またサブページにライセンス情報の詳細が明記されている特別ページを追記。</li>
<li>これまでデフォルトで無効になっていたページの履歴統合機能が管理者に対してのみ有効化。</li>
<li>カテゴリページが移動可能に。</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:メディア統計" title="wikilink">特別:メディア統計</a>の特別ページを追加</li>
<li>スキンの設定仕様を変更</li>
</ul></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.25" title="wikilink">1.25</a></p></td>
<td><p><a href="../Page/2015年.md" title="wikilink">2015年</a><a href="../Page/5月25日.md" title="wikilink">5月25日</a></p></td>
<td><p><a href="https://git.wikimedia.org/blob/mediawiki%2Fcore.git/master/RELEASE-NOTES-1.25">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localization_statistics" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>PHPバージョン5.3.3が必要。</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:タグ一覧" title="wikilink">タグの操作が可能に</a></li>
<li>閲覧回数機能を廃止。これに伴い人気ページ一覧の特別ページも廃止され、<a href="https://ja.wikipedia.org/wiki/特別:統計" title="wikilink">特別:統計</a>からも「最も閲覧されているページ」が無くなった。</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:最近の更新" title="wikilink">特別:最近の更新</a>の仕様を大幅に変更。拡張版 (<a href="https://ja.wikipedia.org/wiki/meta:Help:Enhanced_recent_changes" title="wikilink">meta:Help:Enhanced recent changes</a>) がデフォルトになった。</li>
<li><a href="https://ja.wikipedia.org/wiki/特別:バージョン情報" title="wikilink">特別:バージョン情報</a>に「インストールされているライブラリー」の表を追加</li>
<li>特別ページ一覧の右上に機能についてのMediaWiki公式サイトへのヘルプページのリンクを追加</li>
</ul></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.26" title="wikilink">1.26</a></p></td>
<td><p>2015年<a href="../Page/11月25日.md" title="wikilink">11月25日</a></p></td>
<td><p><a href="https://git.wikimedia.org/blob/mediawiki%2Fcore.git/master/RELEASE-NOTES-1.26">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localization_statistics" title="wikilink">多言語対応状況</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.27" title="wikilink">1.27</a></p></td>
<td><p><a href="../Page/2016年.md" title="wikilink">2016年</a><a href="../Page/6月28日.md" title="wikilink">6月28日</a></p></td>
<td><p><a href="https://git.wikimedia.org/blob/mediawiki%2Fcore.git/master/RELEASE-NOTES-1.27">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localization_statistics" title="wikilink">多言語対応状況</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.28" title="wikilink">1.28</a></p></td>
<td><p>2016年<a href="../Page/11月28日.md" title="wikilink">11月28日</a></p></td>
<td><p><a href="https://git.wikimedia.org/blob/mediawiki%2Fcore.git/master/RELEASE-NOTES-1.28">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localization_statistics" title="wikilink">多言語対応状況</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.29" title="wikilink">1.29</a></p></td>
<td><p><a href="../Page/2017年.md" title="wikilink">2017年</a><a href="../Page/7月13日.md" title="wikilink">7月13日</a></p></td>
<td><p><a href="https://git.wikimedia.org/blob/mediawiki%2Fcore.git/master/RELEASE-NOTES-1.29">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localization_statistics" title="wikilink">多言語対応状況</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.30" title="wikilink">1.30</a></p></td>
<td><p>2017年<a href="../Page/12月12日.md" title="wikilink">12月12日</a></p></td>
<td><p><a href="https://git.wikimedia.org/blob/mediawiki%2Fcore.git/master/RELEASE-NOTES-1.30">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localization_statistics" title="wikilink">多言語対応状況</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/mw:MediaWiki_1.31" title="wikilink">1.31</a></p></td>
<td><p><a href="../Page/2018年.md" title="wikilink">2018年</a><a href="../Page/6月13日.md" title="wikilink">6月13日</a></p></td>
<td><p><a href="https://git.wikimedia.org/blob/mediawiki%2Fcore.git/master/RELEASE-NOTES-1.31">リリースノート全文</a><br />
<a href="https://ja.wikipedia.org/wiki/mw:Localization_statistics" title="wikilink">多言語対応状況</a></p></td>
<td><ul>
<li>PHP7 または HHVM が必要</li>
<li>拡張機能が増加。<a href="https://ja.wikipedia.org/wiki/mw:Extension:CategoryTree/ja" title="wikilink">CategoryTree</a>、<a href="https://ja.wikipedia.org/wiki/mw:Extension:CodeEditor/ja" title="wikilink">CodeEditor</a><a href="https://ja.wikipedia.org/wiki/mw:Extension:MultimediaViewer/ja" title="wikilink">MultimediaViewer</a>、<a href="https://ja.wikipedia.org/wiki/mw:Extension:OATHAuth/ja" title="wikilink">OATHAuth</a>、<a href="https://ja.wikipedia.org/wiki/mw:Extension:Replace_Texth/ja" title="wikilink">Replace Text</a></li>
<li>Timeless 外装を追加</li>
<li><a href="https://ja.wikipedia.org/wiki/mw:Parsing/Replacing_Tidy/FAQ/Ja" title="wikilink">TidyからHTML 5 構文解析アルゴリズムに置換</a></li>
<li>「ウィキ間」利用者名をサポート</li>
<li>環境設定の変更（<a href="https://ja.wikipedia.org/wiki/mw:Manual:$wgEnableAPI/ja" title="wikilink">$wgEnableAPIおよび</a><a href="https://ja.wikipedia.org/wiki/mw:Manual:$wgEnableWriteAPI/ja" title="wikilink">$wgEnableWriteAPIは</a>1.32.0で完全に除去、<a href="https://ja.wikipedia.org/wiki/mw:Manual:$wgUsejQueryThree/ja" title="wikilink">$wgUsejQueryThreeは</a>1.31.0で完全に除去。）</li>
</ul></td>
</tr>
</tbody>
</table>

## 脚注

### 注釈

### 出典

## 関連項目

  - [ウィキツリー](https://ja.wikipedia.org/wiki/ウィキツリー "wikilink") - 派生したもの
  - [Semantic MediaWiki](https://ja.wikipedia.org/wiki/Semantic_MediaWiki "wikilink")
  - [FCKeditor](https://ja.wikipedia.org/wiki/FCKeditor "wikilink")
  - [translatewiki.net](https://ja.wikipedia.org/wiki/translatewiki.net "wikilink")
  - [List of content management systems](https://ja.wikipedia.org/wiki/:en:List_of_content_management_systems "wikilink") – コンテンツ管理システムの一覧
  - [List of wiki software](https://ja.wikipedia.org/wiki/:en:List_of_wiki_software "wikilink") – ウィキソフトウェアの一覧
  - [BlueSpice MediaWiki](https://ja.wikipedia.org/wiki/:en:BlueSpice_MediaWiki "wikilink") – 企業アプリケーション向けに開発
  - [XOWA](https://ja.wikipedia.org/wiki/:en:XOWA "wikilink") – オフラインでウィキペディアその他のウィキを閲覧するJavaソフトウェア (iOS未対応)

## 外部リンク

  - **[MediaWikiメインページ（英語）](https://ja.wikipedia.org/wiki/mw:MediaWiki "wikilink")**

  -
  - [MediaWikiメインページ（日本語）](https://ja.wikipedia.org/wiki/mw:MediaWiki/ja "wikilink") - [利用者ハブ](https://ja.wikipedia.org/wiki/mw:User_hub/ja "wikilink")、[システム管理者ハブ](https://ja.wikipedia.org/wiki/mw:ysadmin_Hub/Ja "wikilink")、[開発者ハブ](https://ja.wikipedia.org/wiki/mw:Developer_hub/ja "wikilink")

  - [MediaWiki on Sourceforge](https://sourceforge.net/projects/wikipedia/)

  - [MediaWiki Download](https://ja.wikipedia.org/wiki/mw:Download/ja "wikilink") - MediaWiki をダウンロードできる

  - [メディアウィキ](https://ja.wikipedia.org/wiki/m:メディアウィキ "wikilink") - [メタウィキメディア上のMediaWikiの解説](https://ja.wikipedia.org/wiki/m:メインページ "wikilink")

  - [Help:コンテンツ](https://ja.wikipedia.org/wiki/m:Help:Contents/ja "wikilink") - MediaWikiのマニュアル

  - [Sites using MediaWiki](https://ja.wikipedia.org/wiki/mw:Sites_using_MediaWiki/ja "wikilink") - MediaWikiを使用しているサイトの一覧

[Category:MediaWiki](https://ja.wikipedia.org/wiki/Category:MediaWiki "wikilink") [Category:ウィキペディア](https://ja.wikipedia.org/wiki/Category:ウィキペディア "wikilink") [Category:ウィキクローン](https://ja.wikipedia.org/wiki/Category:ウィキクローン "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink") [Category:2002年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2002年のソフトウェア "wikilink")

1.  [Wikipedia Adopts MariaDB - Wikimedia Blog](https://blog.wikimedia.org/2013/04/22/wikipedia-adopts-mariadb/)
2.  [英語版およびドイツ語版Wikipedia、MySQLからMariaDBへ移行 - SourceForge.JP Magazine](http://sourceforge.jp/magazine/13/04/25/141500)
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.  Intelの採用について。
17.
18.