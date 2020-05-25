> この記事は[Uniform Resource Locator](https://ja.wikipedia.org/wiki/Uniform_Resource_Locator)から翻訳されています。


[thumbのURL](https://ja.wikipedia.org/wiki/ファイル:Opera_9_address_bar_when_at_Wikipedia_secure.png "wikilink")\]\] **Uniform Resource Locator**（ユニフォーム リソース ロケータ、**URL**）または、**統一資源位置指定子**（とういつしげんいちしていし）とは、[インターネット](../Page/インターネット.md "wikilink")上の[リソース](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")（資源）を特定するための形式的な記号の並び。[WWWをはじめとするインターネットアプリケーションにおいて提供されるリソースを](../Page/World_Wide_Web.md "wikilink")、主にその所在を表記することで特定する。なお、ここでいう、「**リソース**」とは、（主にインターネット上の）データやサービスを指し、例えば[ウェブページ](../Page/ウェブページ.md "wikilink")の保存場所や[電子メール](../Page/電子メール.md "wikilink")の宛先といったものがそうである。

[ティム・バーナーズ＝リー](../Page/ティム・バーナーズ＝リー.md "wikilink")が[1991年](../Page/1991年.md "wikilink")に発表した論文でUniversal Resource Locatorと命名し、初期はその名が使われたが\[1\]、現在の正式名称は、「**<u>Uniform</u> Resource Locator**」である。

URLを含む一般概念として[URIがある](../Page/Uniform_Resource_Identifier.md "wikilink")\[2\]。

URLはリソースの場所を特定する「[住所](../Page/住所.md "wikilink")」のようなものだと例えられることがある。また、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")ではURLのことを「**アドレス**」と呼ぶことがあるが、これは、[MACアドレス](../Page/MACアドレス.md "wikilink")や[IPアドレス](../Page/IPアドレス.md "wikilink")などと紛らわしく、**<u>技術用語としては**</u>、好まれてはいない。

## URLの形式

### 例

|                                                   |                                    |                                              |
| ------------------------------------------------- | ---------------------------------- | -------------------------------------------- |
| **http**:                                         | //**ja.wikipedia.org**             | **/wiki/Wikipedia**                          |
| ↑                                                 | ↑                                  | ↑                                            |
| ｜                                                 | ｜                                  | パス名                                          |
| ｜                                                 | [ホスト名](../Page/ホスト名.md "wikilink") | （[ディレクトリ](../Page/ディレクトリ.md "wikilink")名を含む） |
| スキーム（[プロトコル名ではない](../Page/通信プロトコル.md "wikilink")） |                                    |                                              |

「`http://ja.wikipedia.org/wiki/Wikipedia`」は典型的なURLの一例である。URLはこのような特徴的な形式の文字列であり、WWWが普及した今日にあっては頻繁に目にするものである。

上のURLは「[ウィキペディア日本語版](../Page/ウィキペディア日本語版.md "wikilink")の中にある[ウィキペディア](../Page/ウィキペディア.md "wikilink")について説明している項目」というリソースを特定する。

  - [スキーム](https://ja.wikipedia.org/wiki/スキーム "wikilink")名 `http`はこのリソース（項目）を入手する為には[HTTPを使うべきであることを表す](../Page/Hypertext_Transfer_Protocol.md "wikilink")。
  - `ja.wikipedia.org`はこのリソースが保管されている[ホストを表すホスト名である](../Page/ホスト名.md "wikilink")。
  - 残りの`/wiki/Wikipedia`の部分は最終的にリソースを特定するための詳細である。ホストの[ファイルシステム](../Page/ファイルシステム.md "wikilink")内での[ファイル名あるいは](../Page/ファイル_\(コンピュータ\).md "wikilink")[ディレクトリ](../Page/ディレクトリ.md "wikilink")名に対応する場合が多いが、そうでない場合もある。
  - 大まかに言えば、上のURLは「**ja.wikipedia.org**というコンピュータに接続して**HTTP**の決まり事に従って**/wiki/Wikipedia**という名前のデータを要求すれば目的の物が手に入る」と読むことができる。
  - なお、httpの後のダブルスラッシュ **//**の2文字は有意義に使われる機会が少ない。[2009年](../Page/2009年.md "wikilink")10月、URLの提案者であるティム・バーナーズ=リーは「できることなら取り除きたい」と発言している\[3\]。

### 一般形式

一般にURLは

`（スキーム名）`**`:`**`（スキームごとに定められた何かの表現形式）`

という形をしている。スキーム名としては[プロトコル名が用いられていることが多いがそれに限らない](../Page/通信プロトコル.md "wikilink")。RFC 1738には次のスキーム名が定義されている。

  - ftp - [FTPのためのスキーム](../Page/File_Transfer_Protocol.md "wikilink")
  - http - [HTTPのためのスキーム](../Page/Hypertext_Transfer_Protocol.md "wikilink")
  - gopher - [Gopher](https://ja.wikipedia.org/wiki/Gopher "wikilink")プロトコルのためのスキーム
  - [mailto](https://ja.wikipedia.org/wiki/mailto "wikilink") - [電子メール](../Page/電子メール.md "wikilink")の宛先を表すためのスキーム
  - news - [ネットニュース](../Page/ネットニュース.md "wikilink")（Usenet）のためのスキーム
  - nntp - [NNTP](https://ja.wikipedia.org/wiki/NNTP "wikilink")を使用したネットニュースのためのスキーム
  - telnet - [Telnet](../Page/Telnet.md "wikilink")接続を表すためのスキーム
  - wais - [Wide Area Information Servers](https://ja.wikipedia.org/wiki/Wide_Area_Information_Servers "wikilink")
  - file - [ファイルシステム](../Page/ファイルシステム.md "wikilink")の中のディレクトリやファイルを参照するためのスキーム
  - prospero - [Prospero Directory Service](https://ja.wikipedia.org/wiki/Prospero_Directory_Service "wikilink")

[IANAに登録されたスキーム](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")\[4\]が公式に認められたスキームであると見なされており、上記の他に20あまりある。この他にもjavascriptスキーム（この後ろに書かれた内容が[JavaScript](../Page/JavaScript.md "wikilink")言語によって書かれたスクリプトであることを示す）のように広く普及している非公式なスキームもある\[5\]。

URLの、スキーム名以降の部分はスキームごとに定められた規則に従う。例えば、電子メールの宛先を表すmailtoスキームのURLの場合、

`mailto:example@example.com`

のようになっており、先に挙げたhttpスキームの例とは大きく異なっている。

httpやftpのような特定のホストに[IP接続する類のスキームでは次のような共通の形式が使われている](../Page/Internet_Protocol.md "wikilink")。この表記では、接続するプロトコルは、呼び出している機能のプロトコルと同じものが使用される。

`//`<user>`:`<password>`@`<host>`:`<port>`/`<url-path>

  - <user> - ホストに接続するときに使うユーザー名。必要がなければ省略可。
  - <password> - ユーザー名に対応するパスワード。必要がなければ省略可。
  - <host> - [ホスト名](../Page/ホスト名.md "wikilink")、[FQDNまたは](../Page/Fully_Qualified_Domain_Name.md "wikilink")[IPアドレス](../Page/IPアドレス.md "wikilink")

`https://192.168.10.2/ <-- IPv4の場合`
`https://[fe80::a1b3:125d:c1f8:4781]/ <-- IPv6の場合`

  - <port> - 接続先ポート番号。ホストのどのポートに接続するかを表す。スキームが[デフォルトのポート番号を規定している場合は省略してもよい](../Page/デフォルト_\(コンピュータ\).md "wikilink")。
  - <url-path> - ホストに要求するパス。ホストのファイルシステムにおけるパスと対応する場合が多いが、そうでない場合もある。必要がなければ省略可。

## 標準

[WHATWG](https://ja.wikipedia.org/wiki/WHATWG "wikilink")が[URL Living Standard](https://url.spec.whatwg.org/)を策定している。これは、RFC 3986やその他URLに関係するRFCを置き換える標準仕様である。ただし、[cURL](https://ja.wikipedia.org/wiki/cURL "wikilink")作者のDaniel Steinbergはこれについても不十分という意見を発している\[6\]。

### RFC

URLに関連する[RFC](../Page/Request_for_Comments.md "wikilink")（およびその邦訳）には次のものがある。

  - RFC 1738 - Uniform Resource Locators（URL）
  - RFC 1808 - Relative Uniform Resource Locators
  - RFC 2396 - Uniform Resource Identifiers（URI）：Generic Syntax（旧）
      - [TS X 0097:2004](http://www.y-adagio.com/public/standards/tr_uri_2396/rfc2396-toc.htm) - 統一資源識別子（URI） 共通構文 標準仕様書（TS）
  - RFC 3305 - [URIs, URLs, and URNs: Clarifications and Recommendations 1.0](https://www.w3.org/TR/2001/NOTE-uri-clarification-20010921/)
  - RFC 3986 - Uniform Resource Identifier（URI）：Generic Syntax
  - RFC 1983 - Internet Users' Glossary
      - [TR X 0055:2002](http://www.y-adagio.com/public/standards/tr_interm_1983/rfc1983-toc.htm) - インターネット利用者のための用語 標準情報（TR）

RFC 1983による"**address**"の語釈は次の通り（[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")の原文に**太字**の効果を付与し、1行文字数などの体裁を調整）。

  -
    There are four types of **addresses** in common use within the Internet. They are email address; IP, internet or Internet address; hardware or MAC address; and **URL**. See also: email address, IP address, internet address, MAC address, **Uniform Resource Locator**.

先頭の2文の大意は、「インターネットにおける**アドレス**には主に4種類ある。[電子メール](../Page/電子メール.md "wikilink")アドレス、[IPアドレス](../Page/IPアドレス.md "wikilink")、[MACアドレス](../Page/MACアドレス.md "wikilink")、そして**URL**である」となるが、参考までに、TR X 0055:2002による訳を次に引用する（**太字**は引用者）。

  -
    インターネット（the Internet）内部で共通に使用する**アドレス**には4つの型がある。それらは、電子メールアドレス、IPアドレス又はインターネットアドレス、ハードウェアアドレス又はMACアドレス、及び**URL**とする。"2.147 email address"、"2.252 IP address"、"2.229 internet address"、"2.287 MAC address"及び"2.479 **Uniform Resource Locator**（**URL**）"も参照すること。

### W3C Documents

[W3C](https://ja.wikipedia.org/wiki/W3C "wikilink")が発行しているURLについての文書には次のものがある。

  - [URL](https://www.w3.org/TR/url/) （2017年、ワーキンググループノート）: WHATWG URL Standardのスナップショットとなっている。

##

**恒久リンク**\[7\]（）とは恒久的なURLのこと。主に[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink")、とりわけ[ブログ](../Page/ブログ.md "wikilink")ツールにおいて、個々の記事へのURLが更新作業を繰り返しても変わらないしくみを意味する。一般的に、URLは永久に変化しないことが好ましい\[8\]\[9\]。

特定の記事あるいはウエブページに対する直接リンク（[直リンク](../Page/直リンク.md "wikilink")とも呼ばれる）が増大するにつれ、一方で**[リンク切れ](../Page/リンク切れ.md "wikilink")**\[10\]（）の大量発生も大きな問題となっている。そのような事態を避けるためコンテンツの更新作業が行われ、なおかつ更新履歴が保存されるシステムにおいて、有効なコンテンツへのURLが変動しないように、データへの参照番号などを固定化するとともに参照方法を簡略化し、URLが冗長にならないことが望ましいとされる。

そのための特殊な手法として[Apacheウエブサーバの場合](../Page/Apache_HTTP_Server.md "wikilink")、**mod_rewrite**を使ってURLを書き換える、PATH_INFOからパラメータを取得してプログラムを動作させるなどがある。特にmod_rewriteの場合は、PHPによる動的コンテンツを静的なhtmlコンテンツに見せかけることが容易にできてしまう。またPATH_INFO方式の場合は動的コンテンツをサブディレクトリに見せかけることができる。このほかいわゆる[携帯サイトではURLを短縮化する様々な工夫が施されるようになっている](../Page/携帯電話.md "wikilink")。いずれにしてもURLのみならずオリジナルのファイル拡張子を隠蔽することで、[スクリプトを画像や音楽ファイルのように装うなど悪用のおそれもあるので](../Page/スクリプト言語.md "wikilink")、[ホスティングサーバ](../Page/ホスティングサーバ.md "wikilink")においては利用が制限されるケースが多い。

## 脚注

## 関連項目

  - [Internationalized Resource Identifier](../Page/Internationalized_Resource_Identifier.md "wikilink")（IRI）
  - [Uniform Resource Identifier](../Page/Uniform_Resource_Identifier.md "wikilink")（URI）
  - [Uniform Resource Name](https://ja.wikipedia.org/wiki/Uniform_Resource_Name "wikilink")（URN）
  - [短縮URL](https://ja.wikipedia.org/wiki/短縮URL "wikilink")
  - [名前空間](../Page/名前空間.md "wikilink")
  - [パーセントエンコーディング](../Page/パーセントエンコーディング.md "wikilink")
  - [メールアドレス](../Page/メールアドレス.md "wikilink")

## 外部リンク

  - [URL Living Standard](https://url.spec.whatwg.org/)
  - [URL Living Standard （日本語訳）](https://triple-underscore.github.io/URL-ja.html)

[Category:Uniform_Resource_Locator](https://ja.wikipedia.org/wiki/Category:Uniform_Resource_Locator "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink")

1.  高田敏弘、[World-Wide Web](http://www-linac.kek.jp/WWW.html#sec-url) 第2版、1994年1月21日
2.  RFC 1630
3.  [The Web's Inventor Regrets One Small Thing](http://bits.blogs.nytimes.com/2009/10/12/the-webs-inventor-regrets-one-small-thing/) - NYTimes.com
4.  [URI Schemes](http://www.iana.org/assignments/uri-schemes.html), IANA
5.  [インターネットドラフト](../Page/インターネットドラフト.md "wikilink"): [The 'javascript' resource identifier scheme draft-hoehrmann-javascript-scheme-03](http://tools.ietf.org/html/draft-hoehrmann-javascript-scheme-03)
6.
7.
8.
9.
10.