> この記事は[スタンドアロンBASIC](https://ja.wikipedia.org/wiki/スタンドアロンBASIC)から翻訳されています。


**スタンドアロンBASIC** (standalone BASIC) は、1980年代ごろの8ビット・16ビット[パソコンに内蔵もしくは添付されていた](../Page/パーソナルコンピュータ.md "wikilink")、[OSを必要としない](../Page/オペレーティングシステム.md "wikilink")（それ自体がOS的な役割を備えている）[BASIC](../Page/BASIC.md "wikilink")言語プログラミング環境のこと。 OSを必要とせず単独で動作することからスタンドアロンと呼ばれる。

大別して、[ROMに内蔵されているものと](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、[カセットテープ](../Page/コンパクトカセット.md "wikilink")・[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")などからロードして起動するものとがある。 ROMに内蔵されているものは[ROM-BASIC](../Page/ROM-BASIC.md "wikilink")とも呼ばれる。

## 概要

BASIC言語は、1970年代後半から始まったパソコン黎明期を支えた、コンピュータプログラミング開発・実行環境である。 当時のパソコンは主記憶容量・外部記憶装置とも非常に限られたものであり、本格的なOSを動作させることは困難であったため、BASIC処理系に最低限のOS的な機能（入出力管理など）を持たせたものを搭載することが広く行われた。 当時、パソコンを使うということは、プログラミングをするにせよ、市販のソフトウェアをロードして利用するにせよ、スタンドアロンBASIC環境を利用することとほぼ同義であった。

また、当時は[フロッピーディスクドライブ](https://ja.wikipedia.org/wiki/フロッピーディスクドライブ "wikilink") (FDD) が高価であり別売りが一般的だったため、FDD関連の機能はほとんど搭載しておらず、FDDを使用するにはFDDから起動してBASICの拡張部分をロードすることが必要だった。このように、FDDを扱えるように拡張したBASICのことを[DISK-BASIC](https://ja.wikipedia.org/wiki/DISK-BASIC "wikilink")というが、これもスタンドアロンBASICの範疇に入る。

多くのパソコンメーカーは[Microsoft BASICを採用していたため](../Page/Microsoft_BASIC.md "wikilink")、基本的なプログラミングの様式・言語仕様は同じであった。しかし、パソコンのメーカーや機種ごとに命令語や引数などの細かな言語仕様が異なっていたため、BASICプログラムの相互互換性はほとんどなかった。さらに、カセットテープやフロッピーディスクの[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")もメーカーごとに異なっており、他社製品とのデータ交換もほとんど不可能であった。

なお、ROMで搭載されているものの場合、ROM内の[機械語](../Page/機械語.md "wikilink")サブルーチンには画面表示やキー入力など、今日でいう[BIOSに相当する機能も含まれていた](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")。このような機能は機械語でプログラミングする上でも有用であったため、盛んに利用された。多くのメーカーはROM内ルーチンの仕様を公開していなかったため、有力な機種については独自に内部を解析した結果をまとめた書籍（いわゆる解析本）が出版され、機械語でプログラミングする上で必須の資料となっていた。

スタンドアロンBASICは[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")など16ビットパソコンの初期にも引き続き使われていたが、やがてパソコンの性能や容量の向上に伴って1980年代末頃から[MS-DOS](../Page/MS-DOS.md "wikilink")などの汎用OSを利用することが一般的となり、前記のように互換性が乏しく閉鎖的なスタンドアロンBASIC環境は徐々に使われなくなっていった。 しかし、スタンドアロンBASICで構築されたプログラムやデータファイルの資産を活用したいというニーズは根強く、[NEC](https://ja.wikipedia.org/wiki/NEC "wikilink")や[富士通](../Page/富士通.md "wikilink")などから汎用OS上で動作するBASICインタプリタ・コンパイラやファイルコンバータなどが提供された。

## 主なスタンドアロンBASIC処理系

  - [N-BASIC](../Page/N-BASIC.md "wikilink") - 日本における本格的なスタンドアロンBASIC環境の元祖。
  - [N88-BASIC](../Page/N88-BASIC.md "wikilink")
  - [F-BASIC](../Page/F-BASIC.md "wikilink")
  - [Hu-BASIC](../Page/Hu-BASIC.md "wikilink") - 国産処理系の代表的存在。
  - [MSX-BASIC](../Page/MSX-BASIC.md "wikilink")

## 関連項目

  - [クリーンコンピュータ](https://ja.wikipedia.org/wiki/クリーンコンピュータ "wikilink")
  - [方言 (プログラミング言語)](../Page/方言_\(プログラミング言語\).md "wikilink")

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink")