> この記事は[Mutt](https://ja.wikipedia.org/wiki/Mutt)から翻訳されています。


**Mutt**（マット）は[テキストベースの](https://ja.wikipedia.org/wiki/テキストユーザインタフェース "wikilink")[UNIX](../Page/UNIX.md "wikilink")向け[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")である。マイケル・エルキンスが[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に作成し、[GNU GPLライセンスで公開した](../Page/GNU_General_Public_License.md "wikilink")。始めはメーラ[elmと似たインタフェースであったが](https://ja.wikipedia.org/wiki/Elm_\(電子メールクライアント\) "wikilink")、その後の開発の方向性により、現在では[slrn](https://ja.wikipedia.org/wiki/slrn "wikilink")に良く似たものになっている。

Muttは大半のメールファイル形式に対応しており、特に[mbox](https://ja.wikipedia.org/wiki/mbox "wikilink")と[Maildir](https://ja.wikipedia.org/wiki/Maildir "wikilink")との親和性が高い。また、[POP3](../Page/Post_Office_Protocol.md "wikilink")・[IMAP](../Page/Internet_Message_Access_Protocol.md "wikilink")・[NNTPなど各種の受信](../Page/Network_News_Transfer_Protocol.md "wikilink")・配送プロトコルにも対応している。[MIME対応もあり](https://ja.wikipedia.org/wiki/Multipurpose_Internet_Mail_Extensions "wikilink")、特に[PGP](../Page/Pretty_Good_Privacy.md "wikilink")/[GPGや](https://ja.wikipedia.org/wiki/GNU_Privacy_Guard "wikilink")[S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink")へは完全対応している。

Muttは基本的にメール・ユーザ・エージェント (MUA) であり、1.5.14 までメール送信の機能を持っていなかったが、Brendan Cully が主導する 1.5.15 以降では SMTP 機能が追加された。

設定可能な項目が多いことでも知られる。数百の設定用の指定項目やコマンドがあり、色付けの設定、レイアウト指定から始まり、[キーバインド](https://ja.wikipedia.org/wiki/キーバインド "wikilink")の変更や、複雑な動作を行うキーボード[マクロの作成など多岐に渡る](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")。また、標準装備されていない機能を実現するための[パッチ](../Page/パッチ.md "wikilink")や拡張が多く存在する。例えば、NNTP対応やサイドバー機能などがある。

Muttは[キーボードのみで操作できる](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink")。また、[メーリングリスト](../Page/メーリングリスト.md "wikilink")等での長い議論の流れを追うための[スレッド](../Page/スレッド.md "wikilink")表示機能もある。メッセージの作成にはデフォルトでは外部の[テキストエディタ](../Page/テキストエディタ.md "wikilink")を使う。これは[pine](https://ja.wikipedia.org/wiki/pine "wikilink")のような内部エディタ（pineの場合は[pico](https://ja.wikipedia.org/wiki/pico "wikilink")）を起動するタイプのメーラと異なる。

## 日本語対応

初期公開されたMuttでは、[文字コード](../Page/文字コード.md "wikilink")をはじめとする[日本語](../Page/日本語.md "wikilink")メールの慣習への対応が十分ではなく、付随する[端末制御シーケンス](https://ja.wikipedia.org/wiki/端末制御シーケンス "wikilink")や[文字幅](https://ja.wikipedia.org/wiki/文字幅 "wikilink")認識などの点でもそのままでは、日本語メールの扱いに使えない状況であった。その後、日本語対応パッチが[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")頃に作成され使われるようになってきた。その後、公式版のMuttでも開発版1.3系列以降、日本語文字コードを始めとする[マルチバイト](https://ja.wikipedia.org/wiki/マルチバイト "wikilink")機能が追加され、公式版をそのまま使っても日本語メールが扱えるようになった。しかしながら、日本語圏におけるメールやりとりの慣習が欧米向けに設計されたMutt標準のものとは異なる面が残っていたり、MIME等の国際標準に準拠しない設定でメッセージのやりとりを行うMUAがあることから、本家での取り扱いが難しい日本語パッチが一部あり、日本語対応パッチとしての提供はまだ続いている。ただ、その主要部分である assumed_charset 機能は 2007年2月に Brendan Cully が主導権を継いだ途端に取り入れられた。

## Mutt Sucks Less

Muttのスローガンに、「*All mail clients suck. This one just sucks less* （あらゆるメールクライアントはクソだが、こいつのクソ度はちょっとだけマシ）」というものがある。Muttの開発者たちは、あらゆるメールクライントにはなんらかの点でダメなものであるとし、muttのダメ度は他のものよりは低いと主張している。「*[foo](https://ja.wikipedia.org/wiki/foo "wikilink") sucks less* （[foo](https://ja.wikipedia.org/wiki/foo "wikilink")のクソ度はちょっとマシ）」というような用法は主要なハッカーコミュニティの[ジャーゴン](https://ja.wikipedia.org/wiki/ジャーゴン "wikilink")として一種の敬意を払ったものとみなされている。

## 外部リンク

  - [Mutt（日本語版）](http://www.emaillab.org/mutt/)
  - [Mutt公式サイト](http://www.mutt.org/)
      - [Mutt公式サイト内のWiki](http://wiki.mutt.org/)
  - [comp.mail.mutt Usenetのニュースグループ](news:comp.mail.mutt)
  - [Mutt Primer](http://www.linux.ie/articles/tutorials/mutt.php)
  - [Mutt on Windows](http://www.geocities.com/win32mutt/)

[Category:電子メールソフト](https://ja.wikipedia.org/wiki/Category:電子メールソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")