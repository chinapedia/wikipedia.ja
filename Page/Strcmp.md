> この記事は[Strcmp](https://ja.wikipedia.org/wiki/Strcmp)から翻訳されています。


**strcmp**は2つの文字列を比較 (compare) する[C言語](../Page/C言語.md "wikilink")の[関数である](../Page/サブルーチン.md "wikilink")。 [標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")の文字列操作関数群が宣言されている[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink") `string.h` に含まれる。 **ストリングコンペア**、**ストリングコンプ**などと呼ばれることが多い。

## 書式

``` c
#include <string.h>
int strcmp(const char *s1, const char *s2);
```

## 説明

strcmp() 関数は2つの文字列 s1 と s2 を[辞書式順序](../Page/辞書式順序.md "wikilink")で比較する。この関数は、s1 が s2 に比べて

1.  小さい場合
2.  等しい場合
3.  大きい場合

に、それぞれ

1.  ゼロよりも小さい整数（負数）
2.  ゼロに等しい整数（ゼロ）
3.  ゼロよりも大きい整数（正数）

を返す。

## 関連関数

``` c
#include <string.h>
int strncmp(const char *s1, const char *s2, size_t n);
```

strncmp() 関数は2つの文字列s1とs2を最大n文字比較する。

### 大文字・小文字を区別しない比較関数

規格や処理系によっては、比較時に大文字・小文字を区別しない関数を独自の拡張として実装しているものもある。

  - [POSIX](../Page/POSIX.md "wikilink")

\[1\]

``` c
#include <strings.h>
int strcasecmp(const char *s1, const char *s2);
int strncasecmp(const char *s1, const char *s2, size_t n);
```

  - [IBM i](../Page/IBM_i.md "wikilink")

\[2\]\[3\]\[4\]\[5\]\[6\]

``` c
#include <string.h>
int stricmp(const char *string1, const char *string2);
int strnicmp(const char *string1, const char *string2, int n);
int strcmpi(const char *string1, const char *string2);
int srtcasecmp(const char *string1, const char *string2);
int strncasecmp(const char *string1, const char *string2, size_t count);
```

  - [Microsoft Visual C++](../Page/Microsoft_Visual_C++.md "wikilink")

\[7\]\[8\]

``` c
#include <string.h>
int _stricmp(const char *string1, const char *string2);
int _strnicmp(const char *string1, const char *string2, size_t count);
```

## 脚注

## 関連項目

  - [strcpy](https://ja.wikipedia.org/wiki/strcpy "wikilink")
  - [strcat](https://ja.wikipedia.org/wiki/strcat "wikilink")

## 外部リンク

  -
[en:Strcmp](https://ja.wikipedia.org/wiki/en:Strcmp "wikilink")

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")

1.  [Man page of STRCASECMP](https://linuxjm.osdn.jp/html/LDP_man-pages/man3/strcasecmp.3.html)
2.  [IBM Knowledge Center - stricmp() — 大/小文字を区別しないストリングの比較](https://www.ibm.com/support/knowledgecenter/ja/ssw_ibm_i_73/rtref/stricmp.htm)
3.  [IBM Knowledge Center - strnicmp() — 大/小文字の区別をしないサブストリングの比較](https://www.ibm.com/support/knowledgecenter/ja/ssw_ibm_i_73/rtref/strnicmp.htm)
4.  [IBM Knowledge Center - strcmpi() — 大/小文字を区別しないストリングの比較](https://www.ibm.com/support/knowledgecenter/ja/ssw_ibm_i_73/rtref/strcmpi.htm)
5.  [IBM Knowledge Center - strcasecmp() — 大/小文字を区別しないストリングの比較](https://www.ibm.com/support/knowledgecenter/ja/ssw_ibm_i_73/rtref/strcasecmp.htm#strcasecmp)
6.  [IBM Knowledge Center - strncasecmp() — 大/小文字を区別しないストリングの比較](https://www.ibm.com/support/knowledgecenter/ja/ssw_ibm_i_73/rtref/strncasecmp.htm#strncasecmp)
7.  [_stricmp, _wcsicmp, _mbsicmp, _stricmp_l, _wcsicmp_l, _mbsicmp_l | MSDN](https://msdn.microsoft.com/en-us/library/k59z8dwe.aspx)
8.  [_strnicmp, _wcsnicmp, _mbsnicmp, _strnicmp_l, _wcsnicmp_l, _mbsnicmp_l | MSDN](https://msdn.microsoft.com/en-us/library/chd90w8e.aspx)