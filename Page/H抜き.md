> この記事は[H抜き](https://ja.wikipedia.org/wiki/H抜き)から翻訳されています。


**h抜き**（エイチぬき、エッチぬき）とは、[ウェブ上の](../Page/World_Wide_Web.md "wikilink")[電子掲示板](../Page/電子掲示板.md "wikilink")などにおいて、[ウェブサイト](../Page/ウェブサイト.md "wikilink")の[URLを書き込む際に先頭の](../Page/Uniform_Resource_Locator.md "wikilink")"**h**"などを抜いて書き込む行為を指す。

「**http://**」で始まるアドレスから先頭の"**h**"が抜かれるために「h抜き」と呼ばれている。

## 概要

インターネット上の掲示板や[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink") (CMS) 等のシステムでは、URL文字列を書き込むと、自動的に[リンクとして扱う](../Page/ハイパーリンク.md "wikilink")=リンクタグを補完する「自動リンク機能」が実装されている場合が多い（[ウィキペディア](../Page/ウィキペディア.md "wikilink")のサーバーで使用されている[Wikiプログラム](../Page/ウィキ.md "wikilink")[MediaWiki](../Page/MediaWiki.md "wikilink")もそうである）。しかし、ユーザーが自動リンクされるのを避けたいケースもあり、h抜きはその回避手段として編み出されたと言える。

h抜きが発生したのは上記自動リンク機能の一般化とほぼ同時期と考えられる。

h抜きを用いると検索エンジンに対象URLがクロールされなくなったり、[リファラ](https://ja.wikipedia.org/wiki/リファラ "wikilink")を使用したリンク元解析が不可能になる点が一部ユーザーに重視され、その目的で使用されることもある。

また、自動リンク先をURLそのものでなくプレリンクページ（ime.nu等）にする仕様が普及し、さらにそこに大量のアダルト広告バナーが貼られるようになるとその表示を防ぐため、それまでh抜きを行っていなかったりhの有無に無頓着だった層にもh抜きは普及することになった。

## h抜きの例

以下はハイパーリンク及びh抜きされたただの文字列の例である。

  - h抜きをしない場合
    <http://ja.wikipedia.org/>
  - h抜きをした場合
    ttp://ja.wikipedia.org/

## h抜きの亜種

ttp://とする以外にも、以下のような手段が使われている。

  - http自体を省略（例：ja.wikipedia.org/）
  - ht_tpとする
  - h ttpとする
  - （h）ttpとする
  - hxxpとする
      - 特にセキュリティ界隈で使われるということで、hxxpsと併せてIETFドラフトとして提案されている\[1\]。
  - h++pとする
  - h\*\*pとする
  - htpとする
  - httとする
  - tpとする
  - URLの一部を全角にする（例：http://ja.ｗｉｋipedia.org）
  - URLの一部を日本語に翻訳する
  - URLの中間や最後尾を省く（例：～.co.j）

## "h"抜きと呼ばれる理由

電子掲示板の仕様により異なるが、プログラムが文字列にURLが含まれていると判断する材料に「[http](../Page/Hypertext_Transfer_Protocol.md "wikilink")://」がよく利用される。つまり、hを抜いた「ttp://」ならばプログラムに認識されず通常の文字列として処理される。厳密には「http://」という文字列でURLが含まれているか否かを判断しているため、hから/までのどの文字を抜いてもh抜きとなる。また、[スパムトラックバック対策でhttpが禁止されている場合に有効である](https://ja.wikipedia.org/wiki/トラックバック#トラックバックスパム "wikilink")。

## クライアント側での自動リンク機能とh抜き

クライアント側（ブラウザ）の拡張機能として文書中のURL文字列を自動的にハイパーリンクとして扱うものもあり、その多くはttpをhttpと同等に処理する。

  - [Sleipnir](../Page/Sleipnir.md "wikilink")
    アドレスバーにh抜きで打ち込んだ場合、自動的にhttpに補完する。
  - [2ちゃんねるブラウザ](../Page/2ちゃんねるブラウザ.md "wikilink")各種
    レス中のh抜きを補完してリンクを作成するものが多い。

## h抜きの弊害

  - ttpとすることで、
      - IE6までのブラウザでftp://と誤認識される。
      - アドレスバー検索ツールが反応したりする。
    <!-- end list -->
      -
        等の弊害がある。
  - [亜種の場合](https://ja.wikipedia.org/wiki/#h抜きの亜種 "wikilink")、http自体を省略した場合には問題が無いが、他のパターンでは[デッドリンクになったり](../Page/リンク切れ.md "wikilink")、思いがけないサイトにアクセスされる場合がある。

## 脚注

## 関連項目

  - [HTML要素](../Page/HTML要素.md "wikilink")
  - [ハイパーリンク](../Page/ハイパーリンク.md "wikilink")
  - [無断リンク](../Page/無断リンク.md "wikilink")

[Category:インターネットの文化](https://ja.wikipedia.org/wiki/Category:インターネットの文化 "wikilink") [Category:Uniform_Resource_Locator](https://ja.wikipedia.org/wiki/Category:Uniform_Resource_Locator "wikilink")

1.