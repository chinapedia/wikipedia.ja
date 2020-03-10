> この記事は[Sieve](https://ja.wikipedia.org/wiki/Sieve)から翻訳されています。


**Sieve** は、[電子メールフィルタリング](https://ja.wikipedia.org/wiki/電子メールフィルタリング "wikilink")のための[プログラミング言語](../Page/プログラミング言語.md "wikilink")。[Cyrus IMAP server](../Page/Cyrus_IMAP_server.md "wikilink") を開発した[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の Cyrus Project で開発された。

特定の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")やメールアーキテクチャに依存していない。RFC 2822 準拠メッセージである必要はある。Sieve の基本仕様は RFC 5228 （2008年1月発行）で概説されている。

Sieve は普通のプログラミング言語とは違ってフィルタリングに限定されており、基本仕様では変数もループもない。拡張として、変数を導入したり、限定的なループを導入したりしているが、まだ言語としては非常に制限されており、メールシステムの一部としてユーザーが記述したプログラムを導入するのに適している。

言語の文法には多数の制限があり、[構文解析](../Page/構文解析.md "wikilink")を単純化しているが、文字列の[地域化もいくつかの方法でサポートしていて](../Page/国際化と地域化.md "wikilink")、[Unicode](../Page/Unicode.md "wikilink")も完全に扱える。

## 例

Sieve のスクリプトの例を以下に示す。

    # example script
    # de.wikipedia.org
    #
    require ["fileinto", "reject"];

    # 100KB以上のメッセージは拒否し、エラーメッセージを表示
    #

    if size :over 100K {
       reject "I'm sorry, I do not accept mail over 100kb in size.
    Please upload larger files to a server and send me a link.
    Thanks.";
    }

    # メーリングリストからのメールは "mailinglist" というフォルダに格納
    #

    elsif address :is ["From", "To"] "mailinglist@blafasel.invalid" {
       fileinto "INBOX.mailinglist";
    }

    # スパム規則: To, CC, Bcc ヘッダに自分のアドレスがないメッセージ
    # および、subject に "money" や "Viagra" という単語のあるメッセージ
    #

    elsif anyof (not address :all :contains ["To", "Cc", "Bcc"] "me@blafasel.invalid",
    header :matches "Subject" ["*money*","*Viagra*"]) {
          fileinto "INBOX.spam";
    }

    # 他はキープする。
    # この部分はなくてもよい（デフォルトでキープされる）

    else {
         keep;
    }

## 外部リンク

  - [Sieve.Info, a Wiki Site about Sieve](http://sieve.info/)
  - [The old Sieve Home Page on web.archive.org](http://web.archive.org/web/20041126062029/http://www.cyrusoft.com/sieve/)
  - RFC 5228 (Base Specification about Sieve)
  - [Sieve IETF Working Group Charter](http://www.ietf.org/html.charters/sieve-charter.html)

[Category:電子メール](https://ja.wikipedia.org/wiki/Category:電子メール "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")