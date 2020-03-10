> この記事は[Wc \(UNIX\)](https://ja.wikipedia.org/wiki/Wc_\(UNIX\))から翻訳されています。


**wc**（ダブリューシー、**W**ord **C**ount の略）は[UNIX](../Page/UNIX.md "wikilink")系[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のコマンドの一種。

標準入力か指定されたファイルのリストを読み込み、各種統計情報を生成する。出力情報としては、バイト数、単語数、行数（改行文字の個数）などがある。複数のファイル名を指定した場合、各ファイルの情報と合計が表示される。

wc の実行例を以下に示す。

`$ wc ideas.txt excerpt.txt `
`     40     149     947 ideas.txt`
`   2294   16638   97724 excerpt.txt`
`   2334   16787   98671 total`

最初のカラムは行数、2番目のカラムは単語数、最後のカラムは文字数である。

最近の wc は[バイトと](../Page/バイト_\(情報\).md "wikilink")[文字を区別できる](../Page/キャラクタ_\(コンピュータ\).md "wikilink")。これは[Unicode](../Page/Unicode.md "wikilink")の多バイト文字を含む場合に差が生じる。どちらを表示させるかはオプションで *-c* か *-m* を使うことで指定できる。

[GNU](../Page/GNU.md "wikilink") wcはかつてGNU textutilsパッケージに含まれていたが、現在では[GNU Core Utilitiesに含まれている](https://ja.wikipedia.org/wiki/GNU_Core_Utilities "wikilink")。

## 使用法

`   wc -l `<ファイル名>` 行数を表示`
`   wc -c `<ファイル名>` バイト数を表示`
`   wc -m `<ファイル名>` 文字数を表示`
`   wc -L `<ファイル名>` 最長行を表示（GNU 拡張）`
`   wc -w `<ファイル名>` 単語数を表示`

## 外部リンク

  - [wc(1)](https://linuxjm.osdn.jp/html/GNU_textutils/man1/wc.1.html) wcコマンドの[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink") JM Project
  - [wc(1)](https://docs.oracle.com/cd/E19253-01/819-1210/6n3j74jvr/index.html) man page（SunOS リファレンスマニュアル）
  - [wc(1)](https://nixdoc.net/man-pages/HP-UX/man1/wc.1.html) man page（HP-UX リファレンス）



[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")