> この記事は[Comma-Separated Values](https://ja.wikipedia.org/wiki/Comma-Separated_Values)から翻訳されています。


（略称：**CSV**）は、いくつかのフィールド（項目）を[区切り文字](https://ja.wikipedia.org/wiki/区切り文字 "wikilink")である[カンマ](https://ja.wikipedia.org/wiki/コンマ "wikilink")「`,`」で区切った[テキスト](../Page/テキスト.md "wikilink")データおよび[テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")。[拡張子](../Page/拡張子.md "wikilink")は `.csv`、[MIMEタイプ](https://ja.wikipedia.org/wiki/MIMEタイプ "wikilink")は `text/csv`。

「」とも言う。広く普及した訳語はないが、「**カンマ区切り**」などとも呼ばれる。[Microsoft Excelでは](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")「CSV (カンマ区切り)」としている。

データ交換用の[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")として、古くから多くの[表計算ソフト](https://ja.wikipedia.org/wiki/表計算ソフト "wikilink")や[データベース](../Page/データベース.md "wikilink")ソフトで使われているが、細部の[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")はソフトによって異なる。それらを追認する形で、2005年10月、RFC 4180 で （[IESGの外部で決定された有用な情報の提供](https://ja.wikipedia.org/wiki/Internet_Engineering_Steering_Group "wikilink")）として仕様が成文化された。

類似したフォーマットとして、タブで区切られた  (**TSV**)や、欧文間隔 (いわゆる[半角スペース](https://ja.wikipedia.org/wiki/スペース#コンピュータにおけるスペース "wikilink")) で区切られた  (**SSV**) などがあり、これらをまとめて  (**CSV**)、 (**DSV**) とも呼ばれることも多い。

## 仕様

RFC 4180に述べられた仕様について述べる。

ファイルは1つ以上のレコードからなる。レコードは[改行](https://ja.wikipedia.org/wiki/改行コード "wikilink")（CRLF、U+000D U+000A）で区切られる。最後のレコードの後には改行はあってもなくてもいい。

レコードは1つ以上の同じ個数のフィールドからなる。フィールドはコンマ「,」(U+002C) で区切られる。最後のフィールドの後にはコンマは付けない。

（以下の例では、読みやすさのためにCRLFの前にスペースを書くが、実際はないものと思って読んで欲しい）

`日本国,東京,127767944 CRLF`
`アメリカ合衆国,ワシントン,300007997 CRLF`
`…`

なお、最後のフィールドの後にはコンマはないので、もしレコードがコンマで終わっているように見えれば、実際はその後に[空文字列](https://ja.wikipedia.org/wiki/空文字列 "wikilink")（長さ0の[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")）からなるフィールドがある。次のレコードは、「日本国」「東京」「」の3つのフィールドからなる。

`日本国,東京, CRLF`

ファイルの先頭には、オプションとして、通常のレコードと同一の書式の「ヘッダ行」があってもいい。ヘッダ行は、他のレコードと同じ個数のフィールドを持ち、フィールドの名称が書かれている。

`国,首都,人口(2006) CRLF`
`日本国,東京,127767944 CRLF`
`アメリカ合衆国,ワシントン,300007997 CRLF`
`…`

フィールドは、[ダブルクォート](https://ja.wikipedia.org/wiki/ダブルクォート "wikilink")「"」(U+0022) で囲んでも囲まなくてもよい。次の3つのレコードは、（文字列としては）同じ内容である。（ただし、RFCはフィールドの解釈までは規定していない。一部のソフトはダブルクォートで囲まれているかどうかで解釈を変える）

`日本国,東京,127767944 CRLF`
`"日本国","東京","127767944" CRLF`
`"日本国","東京",127767944 CRLF`

フィールドがコンマ、ダブルクォート、改行を含む場合は、かならずダブルクォートで囲む。また、フィールドに含まれるダブルクォートは2つ並べて[エスケープする](https://ja.wikipedia.org/wiki/エスケープ文字 "wikilink")。次のレコードの内容は、「日本\[改行\]国」「"東京"」「127,767,944」である。なお、ここでいう「コンマ」「ダブルクォート」はU+002CとU+0022のことで、他のもの（たとえば全角コンマ）は関係ない。ただし、「改行」にはCR (U+000D) とLF (U+000A) を含む。

`"日本 CRLF`
`国","""東京""","127,767,944" CRLF`

## 背景

コンピュータ内部において、[データベース](../Page/データベース.md "wikilink")内の[テーブルや](https://ja.wikipedia.org/wiki/表_\(データベース\) "wikilink")[表計算ソフト](https://ja.wikipedia.org/wiki/表計算ソフト "wikilink")の表の内容は、それぞれの[ソフトウェア](../Page/ソフトウェア.md "wikilink")が処理可能な独自の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")で保存されていることがあり、そのような場合は別のソフトウェアへ[データ](../Page/データ.md "wikilink")を移そうにも基本的には[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")はないため読み込むことはできない。

カンマ区切りテキストは、テキスト形式で保存されるので、[テキストエディタ](../Page/テキストエディタ.md "wikilink")でも閲覧や編集ができる。さらに、使用するソフトウェアが、カンマ区切りテキストの出力 (エクスポート) と、読み込みから表への生成 (インポート) に対応していれば、別製品のデータベースソフトや表計算ソフトからのデータ交換が可能となる。

しかし、「テキスト形式」や「日付形式」といった各項目に設定している[属性](https://ja.wikipedia.org/wiki/属性 "wikilink")は出力されないので、インポートする側のソフトウエアがインポートする際に設定しなくてはいけない。

[Microsoft Excelに代表される](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")[パソコンの表計算ソフトが流行して以降](../Page/パーソナルコンピュータ.md "wikilink")、非常によく利用されるようになった。[大型コンピュータとのデータのやりとりでは固定長データフォーマットがよく利用される](https://ja.wikipedia.org/wiki/メインフレーム "wikilink")。現在では、[XMLを使おうという動きもあるが](../Page/Extensible_Markup_Language.md "wikilink")、主流にはなっていない。

## 問題点と回避策

レコードにコンマやダブルクォートが含まれている場合、エスケープされている場合でも、ソフトによって解釈が異なり、区切り方が変わることがある。その結果、データが破壊されることや、修正の手間が生じることがある。レコードにタブ文字が含まれている場合よりも、レコードにコンマやダブルクォートが含まれている場合のほうが多い。従って、CSVの代わりに、タブ区切りテキスト形式（TSV）を使うことで問題を避けられることがある。

## 実装

CSVの実装には、各社独自の拡張や制約がある。ただし、歴史的に見れば、これらの実装のほうが RFC 4180以前 から存在している。

  - レコード区切り文字列
    CR LF を区切り文字列として扱わない処理系がある。
  - フィールド区切り文字
    [全角](https://ja.wikipedia.org/wiki/全角 "wikilink")コンマ「，」を区切りとみなす処理系がある。
  - ダブルクオート文字の表現
    ダブルクォート文字を表現する方法として「ダブルクォートで重ねる」処理系と、「[バックスラッシュ](https://ja.wikipedia.org/wiki/バックスラッシュ "wikilink")を前につける」処理系が存在する。
  - ダブルクオート文字の有無
    多くのソフトは、必要なときのみフィールドをダブルクォートで囲む。ただし、そうでないファイルも読み取れる。
  - フィールド数
    読み取りファイルのフィールド数が一定でない場合、ほとんどのソフトは、[空文字列](https://ja.wikipedia.org/wiki/空文字列 "wikilink")（長さ0の文字列）からなるフィールドを適宜追加して数をそろえる。
  - 空行、フィールド数が0個のレコード
    空行を全てのフィールドが空文字列であるとして処理する処理系と、空行を無視する処理系がある。
  - 注釈
    特定の書式の文字列を注釈行として扱う処理系がある。

##

コンマの代わりに別の文字を区切りに使ったフォーマットもあり、まとめて 、 と呼ぶ。

代表的なものに以下のようなものがある。

  - [タブ](https://ja.wikipedia.org/wiki/タブキー "wikilink") -  (TSV) - MIME type は `text/tab-separated-values`
  - [スペース](https://ja.wikipedia.org/wiki/スペース "wikilink") -  (SSV)
  - [セミコロン](https://ja.wikipedia.org/wiki/セミコロン "wikilink") - （SSV）

## 関連項目

  - [フラットファイルデータベース](https://ja.wikipedia.org/wiki/フラットファイルデータベース "wikilink")
  - [区切り文字](https://ja.wikipedia.org/wiki/区切り文字 "wikilink")

## 外部リンク

  - [RFC4180](http://www.ietf.org/rfc/rfc4180.txt) (Common Format and MIME Type for Comma-Separated Values (CSV) Files)
  - [RFC4180・日本語訳](http://www.kasai.fm/wiki/rfc4180jp)
  - [疑似テーブル等をTSVに変換するアプリ](https://web.archive.org/web/20160310002658/http://over.6pb.info/bin/x2tsv.html)

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")