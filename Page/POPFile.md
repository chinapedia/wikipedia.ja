> この記事は[POPFile](https://ja.wikipedia.org/wiki/POPFile)から翻訳されています。


**POPFile**は[Perl](../Page/Perl.md "wikilink")で記述された[オープンソース](../Page/オープンソース.md "wikilink")のメールフィルタソフト。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")として公開されており、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")な環境で動作する。最初のリリースは[2002年](../Page/2002年.md "wikilink")[9月](../Page/9月.md "wikilink")。

## 概要

POPFileのメールフィルタは[ベイズ理論による](../Page/ベイズの定理.md "wikilink")[ベイジアンフィルタ](../Page/ベイジアンフィルタ.md "wikilink")であり、メール受信時にはメールフィルタが内容を学習しながら自動的にメールを分類する。その際、バケツと呼ばれるカテゴリを分類用に用意しており、受信されたメールをバケツごとに分類させる仕様となっている。分類が違っていた場合にはユーザーの選択に従ってメールを再分類させることで再学習させることも可能である。機能上は様々な分類の仕方が可能であるが、一般的には[迷惑メール用のフィルタとして使われることが多い](../Page/スパム_\(メール\).md "wikilink")。

## 動作

POPFileは[POP3](https://ja.wikipedia.org/wiki/POP3 "wikilink")サーバと[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")の間で[プロキシ](../Page/プロキシ.md "wikilink")として動作する。POP3サーバからメールがダウンロードされると、POPFileのフィルタはメールを確認し、分類毎の印をメールのSubjectやメールヘッダなどに追記する。Subject等に追記された印はメールクライアントのフィルタで仕訳する際に利用することが可能である。

バケツ設定や再学習などは[HTMLベースの設定画面に](../Page/HyperText_Markup_Language.md "wikilink")[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")でアクセスすることで行う。メールに追記された印のカスタマイズを行うことも可能である。

日本語を単語単位に分割する処理には、[KAKASI](https://ja.wikipedia.org/wiki/KAKASI "wikilink")または[MeCab](../Page/MeCab.md "wikilink")を使うため、英語などスペースで単語を区切る言語にしか対応していないフィルタや、日本語の単語の分割を文字種の変わり目で行うフィルタに比べ、日本語のメールの分類の精度も良い。

## 関連項目

  - [ベイズ理論](../Page/ベイズの定理.md "wikilink")
  - [単純ベイズ分類器](../Page/単純ベイズ分類器.md "wikilink")
  - [ベイジアンフィルタ](../Page/ベイジアンフィルタ.md "wikilink")
  - [スパム (メール)](../Page/スパム_\(メール\).md "wikilink")

## 外部リンク

  - [POPFile Official website](http://getpopfile.org/)
  - [POPFile Official website (日本語)](http://getpopfile.org/docs/jp)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:電子メール](https://ja.wikipedia.org/wiki/Category:電子メール "wikilink") [Category:自然言語処理](https://ja.wikipedia.org/wiki/Category:自然言語処理 "wikilink") [Category:スパムフィルタリング](https://ja.wikipedia.org/wiki/Category:スパムフィルタリング "wikilink") [Category:2002年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2002年のソフトウェア "wikilink")