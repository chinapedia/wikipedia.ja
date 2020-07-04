> この記事は[Another HTML-lint](https://ja.wikipedia.org/wiki/Another_HTML-lint)から翻訳されています。


**Another HTML-lint**は[HTML](../Page/HyperText_Markup_Language.md "wikilink")([XHTML](https://ja.wikipedia.org/wiki/XHTML "wikilink"))の[文法](../Page/文法.md "wikilink")チェックを行う[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。作者は石野恵一郎。[Perl](../Page/Perl.md "wikilink")5で作成されている。公開は[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")。

## 特徴

[DTDに則した文法のみをチェックするのではなく](../Page/Document_Type_Definition.md "wikilink")、[アクセシビリティ](../Page/アクセシビリティ.md "wikilink")[ガイドライン](https://ja.wikipedia.org/wiki/ガイドライン "wikilink")に準拠した項目や作者が望ましくないとした項目([大文字](../Page/大文字.md "wikilink")[小文字](../Page/小文字.md "wikilink")の統一についてなど)までチェックを行う。またチェック結果が点数で出力されるのも特徴の一つである。

[ウェブサイト](../Page/ウェブサイト.md "wikilink")上で公開されている[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")[サービス](../Page/サービス.md "wikilink")と[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")版を利用可能。利用料は、非営利目的なら[無料](../Page/フリーウェア.md "wikilink")(寄付歓迎)、営利目的で利用する場合は利用料が必要となる\[1\]。

## チェックについて

対象の[ソースコード](../Page/ソースコード.md "wikilink")の指定については以下の3つの方法が用意されている。

  - [URL](https://ja.wikipedia.org/wiki/URL "wikilink")を指定する。
  - 入力欄に直接ソースコードを記述する。
  - [ローカル](../Page/ローカル.md "wikilink")[ファイルを](../Page/ファイル_\(コンピュータ\).md "wikilink")[アップロード](../Page/アップロード.md "wikilink")する。

[ホスティングサーバ](../Page/ホスティングサーバ.md "wikilink")等の設定よっては本来のソースコードには無い[バナー](../Page/バナー.md "wikilink")広告等を挿入されることがあり、その場合正しいチェックを行うにはURLを指定する方法が確実である。

採点は100点からの減点制で行われ、[エラー](../Page/エラー.md "wikilink")の重要度(0から9まで)が高いほど減点数も高くなる(ただし重要度=減点数では無い)。点数に下限は存在せず[マイナスと採点される事もある](https://ja.wikipedia.org/wiki/正の数と負の数 "wikilink")。また重要度が0のエラー([警告](../Page/警告.md "wikilink"))は減点の対象にはならない。

## その他

[HTML5](../Page/HTML5.md "wikilink")には対応していない為、HTML5によるページの正確な検証は不可能。

減点にならない警告を残した状態でも100点を取る事が可能である。ちなみに、警告も含めて完全にエラーを無くした100点は結果の[メッセージ](../Page/メッセージ.md "wikilink")等が異なる。

100点満点でも[論理マークアップ](https://ja.wikipedia.org/wiki/論理マークアップ "wikilink")・[アクセシビリティ](../Page/アクセシビリティ.md "wikilink")等において正しいことを保証するものではない、という事が注意されている。これはチェッカーでは[要素の内容まで判断しないためである所が大きい](../Page/HTML要素.md "wikilink")。そのため、点数を上げることを目的とした異常な記述でエラーを抜けることも可能だが、推奨していない。

## 関連項目

  - [W3C Markup Validation Service](https://ja.wikipedia.org/wiki/W3C_Markup_Validation_Service "wikilink") - [WWWの標準化団体である](../Page/World_Wide_Web.md "wikilink")[W3Cが提供するHTML文書の検証サービス](../Page/World_Wide_Web_Consortium.md "wikilink")
  - [lint](https://ja.wikipedia.org/wiki/lint "wikilink")

## 脚注

<references/>

## 外部リンク

  - [I'm k16](http://www.asahi-net.or.jp/~rh5k-isn/) - 作者サイト
  - [Another HTML-lintのウェブサイト](http://openlab.ring.gr.jp/k16/htmllint/)
  - [Another HTML-lint 5](http://www.htmllint.net/) - [ハートコア](https://ja.wikipedia.org/wiki/ハートコア "wikilink")株式会社（)が提供する無償のサービスで、Another HTML-lintを拡張してHTML5のチェックも可能にしたもの。

[Category:HTML](https://ja.wikipedia.org/wiki/Category:HTML "wikilink") [Category:ウェブアクセシビリティ](https://ja.wikipedia.org/wiki/Category:ウェブアクセシビリティ "wikilink")

1.