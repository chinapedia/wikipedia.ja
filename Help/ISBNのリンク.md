> この記事は[Help:ISBN](https://ja.wikipedia.org/wiki/Help:ISBN)から翻訳されています。


ウィキペディアでは、[ウィキテキスト中にある](https://ja.wikipedia.org/wiki/Wikipedia:チュートリアル_整形 "wikilink")、**国際的な書籍番号である [ISBN](https://ja.wikipedia.org/wiki/ISBN "wikilink") の番号が識別されます**。これは[:のページと組み合わさり](https://ja.wikipedia.org/wiki/{{ns:Project}}:{{MediaWiki:Booksources}} "wikilink")、利用者はその文献を図書館などの書籍のデータベースや書店で簡便に探すことができます。

この機能は、ウィキペディアで使用しているシステムの MediaWiki の開発者の一人である[エリック・メーラー](https://ja.wikipedia.org/wiki/:en:User:Eloquence "wikilink")（Erik Möller）によって、2003年5月ごろに追加されました\[1\]。

この機能は[マジックリンクであり](https://ja.wikipedia.org/wiki/Help:マジックリンク "wikilink")、将来的に廃止される可能性があります。などで置き換えることを検討してください。

## 表記法と注意点

ウィキテキスト中に例えば `ISBN 978-0-12-345678-9` と書くと、ISBN 978-0-12-345678-9 のようなリンクが生成されます。`ISBN`とコードの間は半角スペースを入れてください。コロン (:) では機能しません。また、コードのあとに文を続ける場合には、コード直後にも半角スペースが必要です。

ハイフンを省略してもリンクは生成されますが、読みやすいよう、ハイフンを用いてなるべくコードを区切るようにしてください\[2\]。区切りの位置は出版物ごとに異なるので、正しい区切りをご確認ください。10桁の場合は4つ、13桁の場合は5つの要素に区切られているはずです。

コードは 10 桁のものも 13 桁のものも使えます\[3\]。しかし、文献を参照する上では 10 桁のISBN も用いられていますし、10桁のものと13桁のものが両方表記されている書籍であっても <s>[10 桁でしか参照できない場合](http://www.ndl.go.jp/jp/library/data/japanmarc_isbn.html)もあります。</s>(現在は国立国会図書館の蔵書検索でも13桁で検索可能\[4\])そこで、記事編集の年月にかかわらず、10 桁の ISBN が与えられている書籍については 10 桁の ISBN でリンクし、更に 13 桁の ISBN も併記されている書籍の場合には ISBN-13 として 13 桁の ISBN も表記してください (両方をリンクする必要はありません)。なお、10 桁から 13 桁への[変換用テンプレートが用意されています](https://ja.wikipedia.org/wiki/Template:13桁ISBN "wikilink")。

このような ISBN リンクは、例えば [特別:文献資料/9780123456789](https://ja.wikipedia.org/wiki/特別:文献資料/9780123456789 "wikilink") と同等のリンクになり、[特別ページである](https://ja.wikipedia.org/wiki/Help:特別ページ "wikilink")[:文献資料へリンクします](https://ja.wikipedia.org/wiki/Special:BookSources "wikilink")。

[:文献資料では](https://ja.wikipedia.org/wiki/Special:BookSources "wikilink")、[:の内容を元に](https://ja.wikipedia.org/wiki/{{ns:Project}}:{{MediaWiki:Booksources}} "wikilink")、あらかじめ登録されているOPACや書店における当該書籍のページへのリンクをリストします\[5\]。これは、「MAGICNUMBER」をすべて当該の ISBN に置き換えることで行われており、つまりパラメータを一つとる[テンプレートの一種と言えますが](https://ja.wikipedia.org/wiki/Help:テンプレート "wikilink")、この用途に限った特別な文法に従っています\[6\]。

リンク先の外部サイトでは、その本の最安値を探したり、批評や読者の反応など、その本に関する様々な情報にアクセスできます。しかし、ISBN は本の特定の版を指すので、販売されているその本の全ての版の情報を見ることができません。ですから、本を指定するのに ISBN 「だけ」を用いず、ISBN と共に適切な情報も記載して下さい。[Wikipedia:スタイルマニュアルや](https://ja.wikipedia.org/wiki/Wikipedia:スタイルマニュアル "wikilink")[Wikipedia:出典を明記するも参照して下さい](https://ja.wikipedia.org/wiki/Wikipedia:出典を明記する "wikilink")。

[:文献資料へのサイトの追加登録は](https://ja.wikipedia.org/wiki/Special:BookSources "wikilink")、[:で提案してください](https://ja.wikipedia.org/wiki/{{ns:Project_talk}}:{{MediaWiki:Booksources}} "wikilink")。

## 関連項目

  - [:Category:ISBNマジックリンクを使用しているページ](https://ja.wikipedia.org/wiki/Category:ISBNマジックリンクを使用しているページ "wikilink") - このリンクを使用しているページの追跡カテゴリ

## 脚注

[Category:Wikipedia:マジックリンク](https://ja.wikipedia.org/wiki/Category:Wikipedia:マジックリンク "wikilink")

1.  Erik Moeller, (Mon May 19 21:12:00 UTC 2003), "[\[Wikitech-l\] Support for booksources page added](http://lists.wikimedia.org/pipermail/wikitech-l/2003-May/003943.html)". - 本機能追加の告知。Erik Moeller, (Wed Jun 11 14:50:00 UTC 2003), "[\[WikiEN-l\] Please edit \[\[Wikipedia:Book_sources|Wikipedia:Book sources\]\]](http://lists.wikimedia.org/pipermail/wikien-l/2003-June/004404.html)". - 英語版コミュニティーへの告知。
2.  国際ISBN機関の発行するでは、人間可読の形式で表記される場合は各要素をハイフンまたはスペースで区切らなければならないとされています。
3.  2006年までに発行された書籍には10桁のISBNが付いています。ISBNの規格改定により、流通段階での 10 桁表記の ISBN は 2007 年以降廃止されました (過去の10桁ISBNは、13桁へ変換し、変換後の数字のほうをISBNとして使用する。[詳細](https://ja.wikipedia.org/wiki/ISBN#2007年以降（現行規格） "wikilink"))。
4.  例えば1988年8月発行の『四番目の恐怖』は以下のように13桁のISBNで検索できる。
    <https://ndlopac.ndl.go.jp/F/?func=find-a&find_code=ISBN&request=9784062039284>
5.  「:文献資料」の元になるテンプレートページ（現在は「:」）は Project 名前空間「」(ns:4, ns:Project) に置かれています。テンプレートページの名前空間名を除くページ名は固定ではなく、[MediaWiki:Booksources](https://ja.wikipedia.org/wiki/MediaWiki:Booksources "wikilink") の内容で[地域化](https://ja.wikipedia.org/wiki/地域化 "wikilink")されています。
6.  Erik Moeller, (Tue May 20 01:16:00 UTC 2003), "[\[Wikitech-l\] ISBN update](http://lists.wikimedia.org/pipermail/wikitech-l/2003-May/003952.html)". - パラメーターを表す文字列を「MAGICNUMBER」に変更した件。