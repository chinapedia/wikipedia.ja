> この記事は[WordBASIC](https://ja.wikipedia.org/wiki/WordBASIC)から翻訳されています。


**WordBASIC**は、ワープロ用にカスタマイズされた[Microsoft](../Page/マイクロソフト.md "wikilink") [QuickBASIC](../Page/QuickBASIC.md "wikilink")のサブセットである。 Windows 版 Word 6.0 または Word 95 で利用できたが、Word 97のリリース時に、 [Visual Basic for Applications（VBA）に置き換えられた](../Page/Visual_Basic_for_Applications.md "wikilink")。 VBAとは対照的に、WordBasicは[オブジェクト指向ではなく](../Page/オブジェクト指向プログラミング.md "wikilink")、約900のコマンドのフラットリストで構成されていた\[1\]。

Word 2000 では、WordBasic のマクロを含む Windows 版 Word 6.0 または Word 95 のテンプレートを開くと、マクロは Visual Basic のモジュールに自動的に変換される\[2\]。 マクロ内の各 WordBasic ステートメントおよび関数は、対応する WordBasic メソッドに変換される。

## サンプルコード

次のコードスニペットは、「Hello、World！」の例でWordBasicとVBAの違いを示している。

例： \[3\]

WordBasic：

``` vb
Sub MAIN
FormatFont .Name = "Arial", .Points = 10
Insert "Hello, World!"
End Sub
```

VBA：

``` vb
Public Sub Main()
  With Selection.Font
    .Name = "Arial"
    .Size = 10
  End With
  Selection.TypeText Text:="Hello, World!"
End Sub
```

## 脚注

[Category:Microsoft_Office](https://ja.wikipedia.org/wiki/Category:Microsoft_Office "wikilink") [Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink")

1.  [WordBasic と Visual Basic の概念上の違い](https://docs.microsoft.com/ja-jp/office/vba/word/concepts/customizing-word/conceptual-differences-between-wordbasic-and-visual-basic), 07/11/2006, Microsoft Docs \[<https://web.archive.org/web/20181201005818/https://docs.microsoft.com/en-us/previous-versions/office/developer/office-2003/aa211963(v=office.11>) Archived\]
2.  [WordBasic プロパティ (Word)](https://docs.microsoft.com/ja-jp/office/vba/api/word.application.wordbasic)
3.  [Converting WordBasic Macros to Visual Basic](https://msdn.microsoft.com/en-us/library/office/aa211926%28v=office.11%29.aspx), 07/11/2006, Microsoft Docs \[<https://web.archive.org/web/20181201005937/https://docs.microsoft.com/en-us/previous-versions/office/developer/office-2003/aa211926(v=office.11>) Archived\]