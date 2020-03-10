> この記事は[ \(Ada\)](https://ja.wikipedia.org/wiki/_\(Ada\))から翻訳されています。


この項目では[プログラミング言語](../Page/プログラミング言語.md "wikilink")**[Ada](../Page/Ada.md "wikilink")**における**[予約語](../Page/予約語.md "wikilink")**（よやくご）に関して説明する。

この項目ではプログラミング言語の詳細には立ち入らないが、Adaの特徴も踏まえつつ，[C言語](../Page/C言語.md "wikilink")など，他言語の予約語との比較・対照ができるような説明を目的としている。

## Adaの予約語の特徴

  - Adaには[72の予約語がある](https://ja.wikipedia.org/wiki/#予約語の一覧 "wikilink")。
  - Adaでは[C言語](../Page/C言語.md "wikilink")などに比べて記号の使用が少なく、例えば括弧のうち{}\[\]や，\!%^などは[字句要素](https://ja.wikipedia.org/wiki/字句要素 "wikilink")として用いられない。Adaの予約語のなかには、C言語などにおいて記号が用いられるような用途での予約語も多い(**begin**, **end**, **and**, **or**, **not**, **array**など)。
  - [識別子](../Page/識別子.md "wikilink")として既定義の語もある(Character, String, Integer, Float, Boolean, True, Falseなど)が、これらは予約語ではない。異なる[名前空間](../Page/名前空間.md "wikilink")とすることにより，ユーザ ([プログラマ](../Page/プログラマ.md "wikilink")) が別の定義を与えて使用することも可能である。
  - C言語などと異なり、大文字・小文字の区別がないため、例えば予約語**for**に対して、For・FORなどはユーザ定義の識別子としては使用できない。

## 用途別分類

ある予約語はここで分類する用途のみならず、種々の場合に用いられるので留意されたい。例えば**range**は整数型定義だけでなく，制御構造や，データ型の内部表現指定([ビットフィールド](https://ja.wikipedia.org/wiki/ビットフィールド "wikilink"))にも用いる。

### 型(クラス)定義に関する予約語

Adaでは、[プログラマ](../Page/プログラマ.md "wikilink")による[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")の生成が比較的自在にできるため、型自体ではなく，型の***定義***にかかわる予約語について分類する。 [Ada_types.png](https://ja.wikipedia.org/wiki/File:Ada_types.png "fig:Ada_types.png")

  - 型定義一般

<!-- end list -->

  -
    **type**，**is**

<!-- end list -->

  - [整数型](https://ja.wikipedia.org/wiki/整数型 "wikilink")定義

<!-- end list -->

  -
    **range**, **mod**

<!-- end list -->

  - [固定小数点型](https://ja.wikipedia.org/wiki/固定小数点型 "wikilink")定義

<!-- end list -->

  -
    **delta**

<!-- end list -->

  - [浮動小数点型](https://ja.wikipedia.org/wiki/浮動小数点型 "wikilink")定義

<!-- end list -->

  -
    **digits**

<!-- end list -->

  - [配列](../Page/配列.md "wikilink")型定義

<!-- end list -->

  -
    **array**, **of**

<!-- end list -->

  - レコード型([構造体](../Page/構造体.md "wikilink"))定義

<!-- end list -->

  -
    **record**

<!-- end list -->

  - アクセス型([ポインタ](../Page/ポインタ_\(プログラミング\).md "wikilink"))定義

<!-- end list -->

  -
    **access**

<!-- end list -->

  - 型定義の修飾

<!-- end list -->

  -
    **limited**, **private**, **tagged**, **interface**, **synchronized**

<!-- end list -->

  - 型の派生(継承)・部分型

<!-- end list -->

  -
    **new**, **subtype**, **with**

<!-- end list -->

  - タスク型(能動的クラス)定義

<!-- end list -->

  -
    **task**

<!-- end list -->

  - 保護型([排他制御](../Page/排他制御.md "wikilink")付き受動クラス)定義

<!-- end list -->

  -
    **protected**

### 演算に関する予約語

  - 論理演算

<!-- end list -->

  -
    **not**, **and**, **or**, **xor**

<!-- end list -->

  - 数値演算

<!-- end list -->

  -
    **abs**, **mod**, **rem**

### 構造に関する予約語

  - プログラム構造

<!-- end list -->

  -
    **begin**, **end**, **declare**

<!-- end list -->

  - [制御構造](https://ja.wikipedia.org/wiki/制御構造 "wikilink")

<!-- end list -->

  -
    **if**, **then**, **else**, **elsif**, **exit**, **case**, **when**, **others**, **loop**, **reverse**, **while**, **for**, **goto**, **return**

### 副プログラム([メソッド](https://ja.wikipedia.org/wiki/メソッド "wikilink"))の仕様に関する予約語

  -
    **procedure**, **function**, **in**, **out**, **entry**, **abstract**, **overriding**

### パッケージ([名前空間](../Page/名前空間.md "wikilink"))に関する予約語

  -
    **package**

### [例外処理](../Page/例外処理.md "wikilink")に関する予約語

  -
    **exception**, **raise**

### タスキング([並列処理](https://ja.wikipedia.org/wiki/並列処理 "wikilink"))に関する予約語

  -
    **abort**, **accept**, **do**, **delay**, **until**, **requeue**, **select**, **terminate**

### 変数(オブジェクト)に関する予約語

  -
    **all**, **constant**, **aliased**

### その他の予約語

  -
    **at**, **pragma**, **use**, **renames**

## 言語規格改訂にともなう増加

  - Ada83からAda95の改訂で予約された語: **abstract**, **aliased**, **protected**, **requeue**, **tagged**, **until**の6語
  - Ada95からAda2005の改訂で予約された語: **interface**, **overriding**, **synchronized**の3語

## 予約語の一覧

1.  abort
2.  abs
3.  abstract
4.  accept
5.  access
6.  aliased
7.  all
8.  and
9.  array
10. at
11. begin
12. body
13. case
14. constant
15. declare
16. delay
17. delta
18. digits
19. do
20. else
21. elsif
22. end
23. entry
24. exception
25. exit
26. for
27. function
28. generic
29. goto
30. if
31. in
32. interface
33. is
34. limited
35. loop
36. mod
37. new
38. not
39. null
40. of
41. or
42. others
43. out
44. overriding
45. package
46. pragma
47. private
48. procedure
49. protected
50. raise
51. range
52. record
53. rem
54. renames
55. requeue
56. return
57. reverse
58. select
59. separate
60. subtype
61. synchronized
62. tagged
63. task
64. terminate
65. then
66. type
67. until
68. use
69. when
70. while
71. with
72. xor

-----

[Category:プログラミング言語の構文](https://ja.wikipedia.org/wiki/Category:プログラミング言語の構文 "wikilink")