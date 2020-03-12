> この記事は[Apache Flex](https://ja.wikipedia.org/wiki/Apache_Flex)から翻訳されています。


（アパッチ・フレックス）は、[リッチインターネットアプリケーション](../Page/リッチインターネットアプリケーション.md "wikilink")のライブラリ。[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink")としては Apache Flex SDK があり、[統合開発環境](../Page/統合開発環境.md "wikilink")としては [Adobe Flash Builder](https://ja.wikipedia.org/wiki/Adobe_Flash_Builder "wikilink") がある。デザインには [MXML](https://ja.wikipedia.org/wiki/MXML "wikilink") を利用し、[プログラミング言語](../Page/プログラミング言語.md "wikilink")には  を利用し、 上で実行する swf ファイルを生成する。 からは  上でも実行可能。Flex SDK は 4.6 までは **Adobe Flex SDK** だったが、4.7 がなく、4.8.0 から Apache Flex SDK。

## 概要

ブームの火付け役となったのが[グーグルマップと言われており](../Page/Google_マップ.md "wikilink")、今日の  を利用した代表的なウェブサービスであるが、ウェブブラウザに依存する  による記述である  と、 内部で実行している  がどちらも  の応用系であることから、この二つをひとつにすることで開発コストを削減し、開発環境を整備という狙いがある。

は  という  と類似した[プログラミング言語](../Page/プログラミング言語.md "wikilink")を内包しており、これまでも[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")上で[{{langと同様の目的に使われてきた](../Page/Javaアプレット.md "wikilink")。[{{langに見られるような問題点が解消されているため](https://ja.wikipedia.org/wiki/Javaアプレット#アプレットの基本動作制限 "wikilink")、重宝されている。その意味では、アプレット以上に[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語による[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")な実行環境を実現している。

はその長所をさらに拡げ、 の弱点であるウェブブラウザ毎の実装の相違やバグ、挙動の差異に左右されずに動的なページを作成することができるため、 よりもクロスプラットフォームでの開発が容易な[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink")として注目されている。ただし、現実には、 はオペレーティングシステム間の挙動の相違の問題を抱えていて、 以外のオペレーティングシステムではバグが多い。

。

また、Adobe Flex SDK 2.0.1 からは、の下でソースコードを公開し、 のコンパイラや  のライブラリの部分がオープンソース化された\[1\]。Apache Flex SDK 4.8.0 から Apache ライセンス。ただし、 や  のソースコードは非公開である。

##

で開発したクライアントとのデータ通信ミドルウェア。バージョン2までは と称したが、バージョン2.5から と改称した。アドビシステムズの製品戦略上、名前に  を冠したが、 で開発したクライアントとのデータ通信に特化しており、系列と考えてよい。

## 歴史

<table>
<caption>Adobe Flex SDK</caption>
<thead>
<tr class="header">
<th><p>版</p></th>
<th><p>公開日</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>2004年3月</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.5</p></td>
<td><p>2004年10月</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2.0</p></td>
<td><p>2006年7月28日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2.0.1</p></td>
<td><p>2007年1月5日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2.0.1 オープンソース化</p></td>
<td><p>2007年4月26日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.0</p></td>
<td><p>2008年2月12日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.0.2</p></td>
<td><p>2008年6月17日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.1.0</p></td>
<td><p>2008年8月15日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.2</p></td>
<td><p>2008年11月17日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.3</p></td>
<td><p>2009年2月5日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.4</p></td>
<td><p>2009年8月19日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.5</p></td>
<td><p>2010年1月5日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.0</p></td>
<td><p>2010年3月22日</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.1</p></td>
<td><p>2010年6月30日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.5</p></td>
<td><p>2011年4月11日</p></td>
<td><p>SDK 2.6.0.19120を含む</p></td>
</tr>
<tr class="even">
<td><p>4.5.1</p></td>
<td><p>2011年6月19日</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.6</p></td>
<td><p>2011年11月30日</p></td>
<td></td>
</tr>
</tbody>
</table>

4.7 はリリースされなかった。

| 版      | 公開日         |
| ------ | ----------- |
| 4.8.0  | 2012年7月26日  |
| 4.9.0  | 2013年1月11日  |
| 4.9.1  | 2013年2月28日  |
| 4.10.0 | 2013年8月6日   |
| 4.11.0 | 2013年10月28日 |
| 4.12.1 | 2014年5月3日   |
| 4.13.0 | 2014年7月28日  |
| 4.14.0 | 2015年2月3日   |
| 4.14.1 | 2015年3月31日  |
| 4.15   | 2016年1月11日  |
| 4.16   | 2017年3月14日  |
| 4.16.1 | 2017年11月22日 |

Apache Flex SDK

## 関連項目

  - [Adobe Flash Builder](https://ja.wikipedia.org/wiki/Adobe_Flash_Builder "wikilink")
  - [Adobe AIR](https://ja.wikipedia.org/wiki/Adobe_AIR "wikilink")

## 脚注

## 外部リンク

  -
[Category:アドビシステムズのソフトウェア](https://ja.wikipedia.org/wiki/Category:アドビシステムズのソフトウェア "wikilink") [Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ソフトウェア開発キット](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発キット "wikilink") [Category:2004年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2004年のソフトウェア "wikilink")

1.  [ITmedia News 「AdobeのFlex 3、公開β版が提供開始」](http://www.itmedia.co.jp/news/articles/0706/11/news043.html)