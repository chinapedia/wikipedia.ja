> この記事は[NaverBot](https://ja.wikipedia.org/wiki/NaverBot)から翻訳されています。


**NaverBot**（ネイバーボット）は、[ネイバー](../Page/ネイバー.md "wikilink")が過去に使用していた[クローラ](../Page/クローラ.md "wikilink")の名称である。

## 概要

[韓国](https://ja.wikipedia.org/wiki/韓国 "wikilink")の大手[検索エンジン](../Page/検索エンジン.md "wikilink")であるネイバーが2005年1月まで使用していた、Web文書収集目的のクローラーである。2005年以降は使用されなくなり、[Yetibot](https://ja.wikipedia.org/wiki/Yetibot "wikilink")という新しいクローラーが使用されるようになった。

NaverBotは、当初は韓国語のサイトを中心にアクセスしていた。しかし、ネイバーが日本での事業を開始した2000年以降は日本語ウェブサイトにアクセスする機会が増え、日本でも知られるようになった。

日本では、国際基準への対応不備などの問題が一部のWebサイト管理者らに指摘され、アクセスを拒否するサイトも見られた。これに対して、ネイバー側は公式のコメントを出してはいないが、後継のクローラー（YetiBot）では当時指摘された以下のような問題はすべて解決されている。\[1\]

  - 主な指摘
      - 秒間隔で次々リクエストを行うため、[DoS攻撃](../Page/DoS攻撃.md "wikilink")のようにサーバーを不安定にさせる。
      - 全ての[ディレクトリ](../Page/ディレクトリ.md "wikilink")に対し、default.htm, default.html, home.php等インデックスに使われそうな名前のページを、ページの有無を確認せずにリクエストする。
      - セッションを識別せず、同じURLに対してセッションだけ変えて何度もリクエストを行う。
      - サイト管理者が用意する[robots.txt](https://ja.wikipedia.org/wiki/robots.txt "wikilink")（クローラのアクセスを制御するファイル）を読み込みながらも無視。あるいは、robots.txtを短時間に何度も読み込む。
      - [HTMLのMETAエンティティを使ったロボットのアクセス制御を無視する](../Page/HyperText_Markup_Language.md "wikilink")。
      - [HTTP](https://ja.wikipedia.org/wiki/HTTP "wikilink")リクエストの[UserAgentフィールドを次々に変える](../Page/ユーザーエージェント.md "wikilink")。変名はNABOT/5.0、nhnbot、minibot(NaverRobot)、dloader(NaverBot)、nabot、Cowbot、NaverBot-1.0+(NHN+Corp.+/++82-2-3011-1954+/+nhnbot@naver.com)等さまざまな名前が確認されている。また、robots.txtへのアクセス時に[Google](../Page/Google.md "wikilink")のクローラGooglebotに似たGoogleBotというユーザーエージェント名を用いたことも確認されている。

## 関連項目

  - [Yetibot](https://ja.wikipedia.org/wiki/Yetibot "wikilink")

## 関連サイト

  - [ネイバー（韓国語）](http://naver.com)
  - [NAVERヘルプセンター（日本語）](http://help.naver.com/robots/yetibot.html)
  - [YetiBot@Naver.com対策](http://www.syuhari.jp/blog/archives/197)

## 脚注欄

[Category:検索エンジン](https://ja.wikipedia.org/wiki/Category:検索エンジン "wikilink")

1.  [NAVER Web Robot Support Center](http://help.naver.com/robots/yetibot.html)