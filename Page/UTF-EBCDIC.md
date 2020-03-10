> この記事は[UTF-EBCDIC](https://ja.wikipedia.org/wiki/UTF-EBCDIC)から翻訳されています。


**UTF-EBCDIC**は[Unicode](../Page/Unicode.md "wikilink")文字の表現に使われる[文字コード](../Page/文字コード.md "wikilink")である。[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")と親和性があり、[メインフレーム](../Page/メインフレーム.md "wikilink")上で動作する従来の[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")アプリケーションが大きな困難なしに文字を処理できるようにすることを意図している。既存のEBCDICベースのシステムにとっての利点は、既存の[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")ベースシステムにとっての[UTF-8](../Page/UTF-8.md "wikilink")の利点に類似する。UTF-EBCDICの詳細はUnicode技術報告 \#16で定義されている。

UTF-EBCDICで符号化されたUnicode符号位置の並びを得るには、UTF-8に基づいた符号化 (UTF-8-Modと呼ばれる仕様) をまず適用する。この符号化がUTF-8と主に異なる点は、Unicode符号位置の0080からU+009Fまで ([C1制御文字](https://ja.wikipedia.org/wiki/C1制御文字 "wikilink")) を、後で対応するEBCDICの制御文字へマップするため1バイトで表現できるようにしている点である。これを達成するため、10XXXXXXの代わりに101XXXXXがマルチバイトシーケンスにおける後続バイトの形式として使われる。これは1バイトあたり6ビット保持できるUTF-8と異なり5ビットしか保持できないため、一般にUTF-EBCDICは同じ入力データに対してUTF-8よりも大きな出力を生成する。

この変換ではデータはまだASCIIベースの形式であるため、[表索引を用いて可逆なバイト単位の変換をこのデータに適用し](https://ja.wikipedia.org/wiki/ルックアップテーブル "wikilink")、可能な限り通常のEBCDICコードページに近づける。 これらの手順を逆にたどることにより容易にUnicode符号位置へ復元できる。

一般に、設計対象であったEBCDICベースのメインフレームにおいてさえ、この符号化形式は滅多に使われない。[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")のような、[IBM](../Page/IBM.md "wikilink")製のEBCDICベースのメインフレームの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は、通常完全なUnicodeサポートに[UTF-16](../Page/UTF-16.md "wikilink")を使用する。たとえば、[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink") UDB、[COBOL](../Page/COBOL.md "wikilink")、[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")および[IBM](../Page/IBM.md "wikilink") [XMLツールキットはIBMのメインフレーム上でUTF](../Page/Extensible_Markup_Language.md "wikilink")-16をサポートする。

## 参考資料

用語の日本語表記は原則として次にならった。

## 外部リンク

  - [Unicode Technical Report \#16](http://www.unicode.org/reports/tr16/): UTF-EBCDICの定義

[Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink") [Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:Unicode変換形式](https://ja.wikipedia.org/wiki/Category:Unicode変換形式 "wikilink")