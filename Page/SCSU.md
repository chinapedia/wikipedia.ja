> この記事は[SCSU](https://ja.wikipedia.org/wiki/SCSU)から翻訳されています。


**SCSU**（英語: Standard Compression Scheme for Unicode）は[Unicode](../Page/Unicode.md "wikilink")のテキストを表すために必要なバイト数を削減するためのUnicode技術標準である\[1\]。特にテキストが1つまたは少数の言語ごとの文字ブロックの文字をほとんど使用している場合に用いられる。128以上255以下の範囲の値を128文字の特定のブロック内のオフセットに動的にマッピングすることにより行なわれる。符号化器の初期状態は、NULLやTAB、CR、LF以外のC0制御文字を含まない[ASCII](../Page/ASCII.md "wikilink")、および[ISO-8859-1](https://ja.wikipedia.org/wiki/ISO-8859-1 "wikilink")の既存の文字列をSCSU文字列として処理する。ほとんどのアルファベットは隣接するUnicode符号点のブロックに存在するため、アルファベットの小文字とASCII句読点、またはアルファベットの大文字の枠内に収まる句読点が用いられたテキストは1文字につき1バイトで符号化できる。他のほとんどの句読点は、非ロックシフトを介して1文字あたり2バイトで符号化できる。SCSUは、アルファベット以外の言語を処理するために内部でUTF-16に切り替えることもできる。

携帯電話やその他のモバイルデバイス用のオペレーティングシステムである[Symbian OSは](../Page/Symbian_OS.md "wikilink")、SCSUを使用して文字列をシリアル化する。

CSUの最初の提案を公開した組織は[ロイター](../Page/ロイター.md "wikilink")であり、内部でSCSUを使用していると考えられている。

[SQL Server 2008 R2はSCSUを使用して](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")、nchar（n）列とnvarchar（n）列に格納されているUnicodeの値を圧縮し、データの言語に応じて15％から50％の領域を節約している\[2\]。

## 比較

汎用的な圧縮方式と比較すると、SCSUを使用することは必ずしも有利であるとは言えない。多くのアプリケーションはUnicodeのテキストを圧縮する必要としていないため、広くサポートされていない専用の圧縮方式を使用することは珍しい。また、テキスト符号化として使用できる一方で、内部処理が難しい場合がある。

SCSUは純粋に圧縮アルゴリズムとして扱われるため、数キロバイトを超えるテキストに対して最も一般的に使用される汎用的なアルゴリズムよりも劣る。

SCSUには、数文字程度の長さのテキストを効果的に圧縮できるという利点がある一方で、ほとんどのフルスケール圧縮方式は、独自のオーバーヘッドを解消するために数百バイトのデータを必要とする。Symbian OSでは、SCSUはテキストの小さな文字列の切り取り、コピー、貼り付けといったクリップボード操作にも用いられる。

## 脚注

[Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink") [Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink")

1.
2.