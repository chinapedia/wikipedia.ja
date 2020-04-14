> この記事は[Java仮想マシン](https://ja.wikipedia.org/wiki/Java仮想マシン)から翻訳されています。


[thumb概要](https://ja.wikipedia.org/wiki/ファイル:Java_virtual_machine_architecture.svg "wikilink")。ソースコードは一旦[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")へとコンパイルされ、さらに[インタプリタ](../Page/インタプリタ.md "wikilink")または[JITコンパイラにより](../Page/実行時コンパイラ.md "wikilink")[ネイティブコードに変換されて実行される](../Page/機械語.md "wikilink")。Java APIとJVMの両者でJava実行環境 (JRE) を構成する。\]\]

**Java仮想マシン** (、、JVM) は、[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")として定義された命令セットを実行する[スタック](../Page/スタック.md "wikilink")型の[仮想マシン](../Page/仮想機械.md "wikilink")。[APIやいくつかのツールとセットで](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[Java実行環境](../Page/Java_Runtime_Environment.md "wikilink") (JRE) としてリリースされている。この環境を移植することで、さまざまな環境でJavaの[プログラムを実行することができる](../Page/プログラム_\(コンピュータ\).md "wikilink")。

## 命令セット仕様

### ニーモニック表

（12、C6 などの数値は16進法表記）

<table>
<thead>
<tr class="header">
<th><p> </p></th>
<th><p>-0</p></th>
<th><p>-1</p></th>
<th><p>-2</p></th>
<th><p>-3</p></th>
<th><p>-4</p></th>
<th><p>-5</p></th>
<th><p>-6</p></th>
<th><p>-7</p></th>
<th><p>-8</p></th>
<th><p>-9</p></th>
<th><p>-A</p></th>
<th><p>-B</p></th>
<th><p>-C</p></th>
<th><p>-D</p></th>
<th><p>-E</p></th>
<th><p>-F</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0-</p></td>
<td><p>00<br />
nop</p></td>
<td><p>01<br />
aconst_null</p></td>
<td><p>02<br />
iconst_m1</p></td>
<td><p>03<br />
iconst_0</p></td>
<td><p>04<br />
iconst_1</p></td>
<td><p>05<br />
iconst_2</p></td>
<td><p>06<br />
iconst_3</p></td>
<td><p>07<br />
iconst_4</p></td>
<td><p>08<br />
iconst_5</p></td>
<td><p>09<br />
lconst_0</p></td>
<td><p>0A<br />
lconst_1</p></td>
<td><p>0B<br />
fconst_0</p></td>
<td><p>0C<br />
fconst_1</p></td>
<td><p>0D<br />
fconst_2</p></td>
<td><p>0E<br />
dconst_0</p></td>
<td><p>0F<br />
dconst_1</p></td>
</tr>
<tr class="even">
<td><p>1-</p></td>
<td><p>10<br />
bipush</p></td>
<td><p>11<br />
sipush</p></td>
<td><p>12<br />
ldc</p></td>
<td><p>13<br />
ldc_w</p></td>
<td><p>14<br />
ldc2_w</p></td>
<td><p>15<br />
iload</p></td>
<td><p>16<br />
lload</p></td>
<td><p>17<br />
fload</p></td>
<td><p>18<br />
dload</p></td>
<td><p>19<br />
aload</p></td>
<td><p>1A<br />
iload_0</p></td>
<td><p>1B<br />
iload_1</p></td>
<td><p>1C<br />
iload_2</p></td>
<td><p>1D<br />
iload_3</p></td>
<td><p>1E<br />
lload_0</p></td>
<td><p>1F<br />
lload_1</p></td>
</tr>
<tr class="odd">
<td><p>2-</p></td>
<td><p>20<br />
lload_2</p></td>
<td><p>21<br />
lload_3</p></td>
<td><p>22<br />
fload_0</p></td>
<td><p>23<br />
fload_1</p></td>
<td><p>24<br />
fload_2</p></td>
<td><p>25<br />
fload_3</p></td>
<td><p>26<br />
dload_0</p></td>
<td><p>27<br />
dload_1</p></td>
<td><p>28<br />
dload_2</p></td>
<td><p>29<br />
dload_3</p></td>
<td><p>2A<br />
aload_0</p></td>
<td><p>2B<br />
aload_1</p></td>
<td><p>2C<br />
aload_2</p></td>
<td><p>2D<br />
aload_3</p></td>
<td><p>2E<br />
iaload</p></td>
<td><p>2F<br />
laload</p></td>
</tr>
<tr class="even">
<td><p>3-</p></td>
<td><p>30<br />
faload</p></td>
<td><p>31<br />
daload</p></td>
<td><p>32<br />
aaload</p></td>
<td><p>33<br />
baload</p></td>
<td><p>34<br />
caload</p></td>
<td><p>35<br />
saload</p></td>
<td><p>36<br />
istore</p></td>
<td><p>37<br />
lstore</p></td>
<td><p>38<br />
fstore</p></td>
<td><p>39<br />
dstore</p></td>
<td><p>3A<br />
astore</p></td>
<td><p>3B<br />
istore_0</p></td>
<td><p>3C<br />
istore_1</p></td>
<td><p>3D<br />
istore_2</p></td>
<td><p>3E<br />
istore_3</p></td>
<td><p>3F<br />
lstore_0</p></td>
</tr>
<tr class="odd">
<td><p>4-</p></td>
<td><p>40<br />
lstore_1</p></td>
<td><p>41<br />
lstore_2</p></td>
<td><p>42<br />
lstore_3</p></td>
<td><p>43<br />
fstore_0</p></td>
<td><p>44<br />
fstore_1</p></td>
<td><p>45<br />
fstore_2</p></td>
<td><p>46<br />
fstore_3</p></td>
<td><p>47<br />
dstore_0</p></td>
<td><p>48<br />
dstore_1</p></td>
<td><p>49<br />
dstore_2</p></td>
<td><p>4A<br />
dstore_3</p></td>
<td><p>4B<br />
astore_0</p></td>
<td><p>4C<br />
astore_1</p></td>
<td><p>4D<br />
astore_2</p></td>
<td><p>4E<br />
astore_3</p></td>
<td><p>4F<br />
iastore</p></td>
</tr>
<tr class="even">
<td><p>5-</p></td>
<td><p>50<br />
lastore</p></td>
<td><p>51<br />
fastore</p></td>
<td><p>52<br />
dastore</p></td>
<td><p>53<br />
aastore</p></td>
<td><p>54<br />
bastore</p></td>
<td><p>55<br />
castore</p></td>
<td><p>56<br />
sastore</p></td>
<td><p>57<br />
pop</p></td>
<td><p>58<br />
pop2</p></td>
<td><p>59<br />
dup</p></td>
<td><p>5A<br />
dup_x1</p></td>
<td><p>5B<br />
dup_x2</p></td>
<td><p>5C<br />
dup2</p></td>
<td><p>5D<br />
dup2_x1</p></td>
<td><p>5E<br />
dup2_x2</p></td>
<td><p>5F<br />
swap</p></td>
</tr>
<tr class="odd">
<td><p>6-</p></td>
<td><p>60<br />
iadd</p></td>
<td><p>61<br />
ladd</p></td>
<td><p>62<br />
fadd</p></td>
<td><p>63<br />
dadd</p></td>
<td><p>64<br />
isub</p></td>
<td><p>65<br />
lsub</p></td>
<td><p>66<br />
fsub</p></td>
<td><p>67<br />
dsub</p></td>
<td><p>68<br />
imul</p></td>
<td><p>69<br />
lmul</p></td>
<td><p>6A<br />
fmul</p></td>
<td><p>6B<br />
dmul</p></td>
<td><p>6C<br />
idiv</p></td>
<td><p>6D<br />
ldiv</p></td>
<td><p>6E<br />
fdiv</p></td>
<td><p>6F<br />
ddiv</p></td>
</tr>
<tr class="even">
<td><p>7-</p></td>
<td><p>70<br />
irem</p></td>
<td><p>71<br />
lrem</p></td>
<td><p>72<br />
frem</p></td>
<td><p>73<br />
drem</p></td>
<td><p>74<br />
ineg</p></td>
<td><p>75<br />
lneg</p></td>
<td><p>76<br />
fneg</p></td>
<td><p>77<br />
dneg</p></td>
<td><p>78<br />
ishl</p></td>
<td><p>79<br />
lshl</p></td>
<td><p>7A<br />
ishr</p></td>
<td><p>7B<br />
lshr</p></td>
<td><p>7C<br />
iushr</p></td>
<td><p>7D<br />
lushr</p></td>
<td><p>7E<br />
iand</p></td>
<td><p>7F<br />
land</p></td>
</tr>
<tr class="odd">
<td><p>8-</p></td>
<td><p>80<br />
ior</p></td>
<td><p>81<br />
lor</p></td>
<td><p>82<br />
ixor</p></td>
<td><p>83<br />
lxor</p></td>
<td><p>84<br />
iinc</p></td>
<td><p>85<br />
i2l</p></td>
<td><p>86<br />
i2f</p></td>
<td><p>87<br />
i2d</p></td>
<td><p>88<br />
l2i</p></td>
<td><p>89<br />
l2f</p></td>
<td><p>8A<br />
l2d</p></td>
<td><p>8B<br />
f2i</p></td>
<td><p>8C<br />
f2l</p></td>
<td><p>8D<br />
f2d</p></td>
<td><p>8E<br />
d2i</p></td>
<td><p>8F<br />
d2l</p></td>
</tr>
<tr class="even">
<td><p>9-</p></td>
<td><p>90<br />
d2f</p></td>
<td><p>91<br />
i2b</p></td>
<td><p>92<br />
i2c</p></td>
<td><p>93<br />
i2s</p></td>
<td><p>94<br />
lcmp</p></td>
<td><p>95<br />
fcmpl</p></td>
<td><p>96<br />
fcmpg</p></td>
<td><p>97<br />
dcmpl</p></td>
<td><p>98<br />
dcmpg</p></td>
<td><p>99<br />
ifeq</p></td>
<td><p>9A<br />
ifne</p></td>
<td><p>9B<br />
iflt</p></td>
<td><p>9C<br />
ifge</p></td>
<td><p>9D<br />
ifgt</p></td>
<td><p>9E<br />
ifle</p></td>
<td><p>9F<br />
if_icmpeq</p></td>
</tr>
<tr class="odd">
<td><p>A-</p></td>
<td><p>A0<br />
if_icmpne</p></td>
<td><p>A1<br />
if_icmplt</p></td>
<td><p>A2<br />
if_icmpge</p></td>
<td><p>A3<br />
if_icmpgt</p></td>
<td><p>A4<br />
if_icmple</p></td>
<td><p>A5<br />
if_acmpeq</p></td>
<td><p>A6<br />
if_acmpne</p></td>
<td><p>A7<br />
goto</p></td>
<td><p>A8<br />
jsr</p></td>
<td><p>A9<br />
ret</p></td>
<td><p>AA<br />
tableswitch</p></td>
<td><p>AB<br />
lookupswitch</p></td>
<td><p>AC<br />
ireturn</p></td>
<td><p>AD<br />
lreturn</p></td>
<td><p>AE<br />
freturn</p></td>
<td><p>AF<br />
dreturn</p></td>
</tr>
<tr class="even">
<td><p>B-</p></td>
<td><p>B0<br />
areturn</p></td>
<td><p>B1<br />
return</p></td>
<td><p>B2<br />
getstatic</p></td>
<td><p>B3<br />
putstatic</p></td>
<td><p>B4<br />
getfield</p></td>
<td><p>B5<br />
putfield</p></td>
<td><p>B6<br />
invokevirtual</p></td>
<td><p>B7<br />
invokespecial</p></td>
<td><p>B8<br />
invokestatic</p></td>
<td><p>B9<br />
invokeinterface</p></td>
<td><p>BA<br />
invokedynamic</p></td>
<td><p>BB<br />
new</p></td>
<td><p>BC<br />
newarray</p></td>
<td><p>BD<br />
anewarray</p></td>
<td><p>BE<br />
arraylength</p></td>
<td><p>BF<br />
athrow</p></td>
</tr>
<tr class="odd">
<td><p>C-</p></td>
<td><p>C0<br />
checkcast</p></td>
<td><p>C1<br />
instanceof</p></td>
<td><p>C2<br />
monitorenter</p></td>
<td><p>C3<br />
monitorexit</p></td>
<td><p>C4<br />
wide</p></td>
<td><p>C5<br />
multianewarray</p></td>
<td><p>C6<br />
ifnull</p></td>
<td><p>C7<br />
ifnonnull</p></td>
<td><p>C8<br />
goto_w</p></td>
<td><p>C9<br />
jsr_w</p></td>
<td><p>CA<br />
breakpoint</p></td>
<td><p>CB<br />
未定義</p></td>
<td><p>CC<br />
未定義</p></td>
<td><p>CD<br />
未定義</p></td>
<td><p>CE<br />
未定義</p></td>
<td><p>CF<br />
未定義</p></td>
</tr>
<tr class="even">
<td><p>D-</p></td>
<td><p>D0<br />
未定義</p></td>
<td><p>D1<br />
未定義</p></td>
<td><p>D2<br />
未定義</p></td>
<td><p>D3<br />
未定義</p></td>
<td><p>D4<br />
未定義</p></td>
<td><p>D5<br />
未定義</p></td>
<td><p>D6<br />
未定義</p></td>
<td><p>D7<br />
未定義</p></td>
<td><p>D8<br />
未定義</p></td>
<td><p>D9<br />
未定義</p></td>
<td><p>DA<br />
未定義</p></td>
<td><p>DB<br />
未定義</p></td>
<td><p>DC<br />
未定義</p></td>
<td><p>DD<br />
未定義</p></td>
<td><p>DE<br />
未定義</p></td>
<td><p>DF<br />
未定義</p></td>
</tr>
<tr class="odd">
<td><p>E-</p></td>
<td><p>E0<br />
未定義</p></td>
<td><p>E1<br />
未定義</p></td>
<td><p>E2<br />
未定義</p></td>
<td><p>E3<br />
未定義</p></td>
<td><p>E4<br />
未定義</p></td>
<td><p>E5<br />
未定義</p></td>
<td><p>E6<br />
未定義</p></td>
<td><p>E7<br />
未定義</p></td>
<td><p>E8<br />
未定義</p></td>
<td><p>E9<br />
未定義</p></td>
<td><p>EA<br />
未定義</p></td>
<td><p>EB<br />
未定義</p></td>
<td><p>EC<br />
未定義</p></td>
<td><p>ED<br />
未定義</p></td>
<td><p>EE<br />
未定義</p></td>
<td><p>EF<br />
未定義</p></td>
</tr>
<tr class="even">
<td><p>F-</p></td>
<td><p>F0<br />
未定義</p></td>
<td><p>F1<br />
未定義</p></td>
<td><p>F2<br />
未定義</p></td>
<td><p>F3<br />
未定義</p></td>
<td><p>F4<br />
未定義</p></td>
<td><p>F5<br />
未定義</p></td>
<td><p>F6<br />
未定義</p></td>
<td><p>F7<br />
未定義</p></td>
<td><p>F8<br />
未定義</p></td>
<td><p>F9<br />
未定義</p></td>
<td><p>FA<br />
未定義</p></td>
<td><p>FB<br />
未定義</p></td>
<td><p>FC<br />
未定義</p></td>
<td><p>FD<br />
未定義</p></td>
<td><p>FE<br />
impdep1</p></td>
<td><p>FF<br />
impdep2</p></td>
</tr>
</tbody>
</table>

### オペコード解説

#### スタック

  - `bipush`、 `sipush` - `byte`値、 `short`値をスタックに積む。
  - `ldc` - コンスタントプール内の4バイトの定数(`int`値、`float`値、`java.lang.String`)の内1バイト以内でエントリ番号を指定できるものをスタックに積む。
  - `ldc_w` - エントリ番号が1バイトでは足りないときに使う。
  - `ldc2_w` - コンスタントプール内の8バイトの定数(`long`値、`double`値)をスタックに積む。
  - `iconst_m1`、 `iconst_0`、 `iconst_1`、 `iconst_2`、 `iconst_3`、 `iconst_4`、 `iconst_5` - `int`の`-1`、`0`、`1`、`2`、`3`、`4`、`5`をスタックに積む。
  - `lconst_0`、 `lconst_1` - `long`の`0`、`1`をスタックに積む
  - `fconst_0`、 `fconst_1`、 `fconst_2` - `float`の`0`、`1`、`2`をスタックに積む
  - `dconst_0`、 `dconst_1` - `double`の`0`、`1`をスタックに積む。
  - `aconst_null` - スタックに`null`を積む。
  - `pop`、 `pop2` - スタックから1、2ワード取り除く
  - `dup`、 `dup2`
  - `dup_x1`、 `dup2_x1`
  - `dup_x2`、 `dup2_x2`
  - `swap`

#### 局所変数

  - `iload`、 `lload`、 `fload`、 `dload`、 `aload` - 局所変数から`int`値、 `long`値、 `float`値、 `double`値、 参照値を取り出してスタックに積む。
  - `iload_0`、 `iload_1`、 `iload_2`、 `iload_3` - 0、1、2、3番目の局所変数から`int`値を取り出してスタックに積む。
  - `lload_0`、 `lload_1`、 `lload_2`、 `lload_3` - 0、1、2、3番目の局所変数から`long`値を取り出してスタックに積む。
  - `fload_0`、 `fload_1`、 `fload_2`、 `fload_3` - 0、1、2、3番目の局所変数から`float`値を取り出してスタックに積む。
  - `dload_0`、 `dload_1`、 `dload_2`、 `dload_3` - 0、1、2、3番目の局所変数から`double`値を取り出してスタックに積む。
  - `aload_0`、 `aload_1`、 `aload_2`、 `aload_3` - 0、1、2、3番目の局所変数から参照値を取り出してスタックに積む。
  - `istore`、 `lstore`、 `fstore`、 `dstore`、 `astore` - `int`値、 `long`値、 `float`値、 `double`値、 参照値を局所変数に格納。
  - `istore_0`、 `istore_1`、 `istore_2`、 `istore_3` - `int`値を0、1、2、3番目の局所変数に格納する。
  - `lstore_0`、 `lstore_1`、 `lstore_2`、 `lstore_3` - `long`値を0、1、2、3番目の局所変数に格納する。
  - `fstore_0`、 `fstore_1`、 `fstore_2`、 `fstore_3` - `float`値を0、1、2、3番目の局所変数に格納する。
  - `dstore_0`、 `dstore_1`、 `dstore_2`、 `dstore_3` - `double`値を0、1、2、3番目の局所変数に格納する。
  - `astore_0`、 `astore_1`、 `astore_2`、 `astore_3` - 参照値を0、1、2、3番目の局所変数に格納する。

#### 条件付きジャンプ

  - `ifeq`、 `ifnull`、 `iflt`、 `ifle`、 `ifne`、 `ifnonnull`、 `ifgt`、 `ifge` - スタックの値が0、 `null`、 0未満、 0以下、 0以外、 `null`以外、 `0`より大きい、 `0`以上の場合に指定の番地に制御を移す。
  - `if_icmpeq`、 `if_icmpne`、 `if_icmplt`、 `if_icmpgt`、 `if_icmple`、 `if_icmpge` - 2つの`int`値が等しい、等しくない、＜、＞、≦、≧の場合に指定の番地に制御を移す。
  - `if_acmpeq`、 `if_acmpne` - 2つの参照値が等しい、等しくない場合に指定の番地に制御を移す。

#### ジャンプ

  - `goto`、 `goto_w` - それぞれ2バイト形式（符号付き16ビット）、4バイト形式（符号付き32ビット）でもつ相対番地をこの命令の番地に加えた番地に制御を移す（JavaにGO TO命令はなくても、このようにJava仮想マシンにgoto命令はある）。
  - `jsr`、 `jsr_w` - サブルーチンの先頭に制御を移す。`goto`と違い、戻り番地を保存する。戻り番地の値はそれぞれ、制御を移す前の番地+3、制御を移す前の番地+5となる。
  - `ret` - サブルーチンから呼び出し元の戻り番地に制御を移す。番地が格納されている局所変数を指定する。
  - `lookupswitch` - `switch`文の`case`式の値が不連続である場合に、値を探しながら飛び越し先を探し、飛び越しを行う。
  - `tableswitch` - `switch`文の`case`式の値が連続である場合に、（キーがインデクス値、値が飛び越し先番地の）表を使って飛び越しを行う。（高速である）

#### メソッド呼び出し・復帰

  - `invokevirtual` - インスタンスメソッドを呼び出す。
  - `invokespecial` - インスタンス初期化メソッド、プライベートメソッド、スーパークラスのインスタンスメソッドを呼び出す。
  - `invokestatic` - クラスメソッドを呼び出す
  - `invokeinterface` - インターフェイスメソッドを呼び出す。

<!-- end list -->

  - `return` - スタックに値を残さずに、呼び出し元の戻り番地に制御を移す。
  - `ireturn`、 `lreturn`、 `freturn`、 `dreturn`、 `areturn` - スタックに `int`値、 `long`値、 `float`値、 `double`値を残して、サブルーチンの呼び出し元の戻り番地に制御を移す。

#### 型キャスト

  - `checkcast` - 参照値が指し示すインスタンスの型を確認。
  - `instanceof` - スタックから参照値を`pop`し、それが指定された型と同じであれば`1`を、異なれば`0`をスタックに積む。
  - `i2l`、 `i2f`、 `i2d`、 `i2b`、 `i2c`、 `i2s` - `int`値を`long`値、 `float`値、 `double`値、 `byte`値、 `char`値、 `short`値に変換したものをスタックに残す。
  - `l2i`、 `l2f`、 `l2d` - `long`値を`int`値に、 `float`値に、 `double`値に変換したものをスタックに残す。
  - `f2i`、 `f2l`、 `f2d` - `float`値を`int`値に、 `long`値に、 `double`値に変換したものをスタックに残す。
  - `d2i`、 `d2l`、 `d2f` - `double`値を`int`値に、 `long`値に、 `float`値に変換したものをスタックに残す。

#### 比較演算

  - `dcmpg`、 `dcmpl` - `double`同士を比較し、`1`（大きい）、`0`（等しい）または`-1`（小さい）をスタックに残す。「-g」と「-l」の違いはオペランドがNaNだったときの扱いの差。（以下同様）
  - `fcmpg`、 `fcmpl` - `float`同士を比較する。
  - `lcmp` - `long`同士を比較する。

#### 算術演算

  - `iinc` - `int`の値を、符号付き1バイト（値の範囲は-128～127）の直接記述した定数だけ（符号付きで32ビットに拡張したうえで）増減する。
  - `iadd`、 `ladd`、 `fadd`、 `dadd` - `int`値、 `long`値、 `float`値、 `double`値 で、スタックから取りだした第一の値に第二の値を加え、スタックに積む。
  - `isub`、 `lsub`、 `fsub`、 `dsub` - `int`値、 `long`値、 `float`値、 `double`値 で、スタックから取りだした第一の値から第二の値を引き、スタックに積む。
  - `imul`、 `lmul`、 `fmul`、 `dmul` - `int`値、 `long`値、 `float`値、 `double`値 で、スタックから取りだした第一の値に第二の値を掛け、スタックに積む。
  - `idiv`、 `ldiv`、 `fdiv`、 `ddiv` - `int`値、 `long`値、 `float`値、 `double`値 で、スタックから取りだした第一の値を第二の値で割った商を、スタックに積む。
  - `irem`、 `lrem`、 `frem`、 `drem` - `int`値、 `long`値、 `float`値、 `double`値 で、スタックから取りだした第一の値を第二の値で割った余り（value1 - (value1 / value2) \* value2）を、スタックに積む。
  - `ineg`、 `lneg`、 `fneg`、 `dneg` - `int`値、 `long`値、 `float`値、 `double`値 で、スタックから取りだした値の符号を反転した値（たとえば入力が123なら-123、-123なら123、0なら0）（すなわち[2の補数](../Page/2の補数.md "wikilink")）をスタックに積む。

#### 論理演算

  - `ishl`、 `lshl` - `int`値、 `long`値 を指定ビットだけ左にシフトした値をスタックに残す。
  - `ishr`、 `lshr` - `int`値、 `long`値 を指定ビットだけ右に算術シフトした値をスタックに残す。負数はシフト後も負に維持される。
  - `iushr`、 `lushr` - `int`値、 `long` を指定ビットだけ右に論理シフトした値をスタックに残す。
  - `iand`、 `land` - `int`値、 `long`値 の2オペランドの`AND`（ビットごとの論理積）を求め、スタックに残す。
  - `ior`、 `lor` - `int`値、 `long` の2オペランドの `OR`（ビットごとの論理和）を求め、スタックに残す。
  - `ixor`、 `lxor` - `int`値、 `long` の2オペランドの`XOR`（ビットごとの排他的論理和）を求め、スタックに残す。

#### オブジェクト

  - `new` - インスタンスの生成
  - `putfield`、 `getfield` - メンバ変数への値の代入、値の取り出し
  - `putstatic`、 `getstatic` - クラス変数への値の代入、値の取り出し

#### 配列

  - `iaload`、 `laload`、 `faload`、 `daload`、 `aaload`、 `baload`、 `caload`、 `saload` - 配列の指定された位置にある`int`値、 `long`値、 `float`値、`double`値、参照値、`byte`または`boolean`値、`char`値、 `short`値をスタックに残す。
  - `iastore`、 `lastore`、 `fastore`、 `dastore`、 `aastore`、 `bastore`、 `castore`、 `sastore` - 配列に`int`値、 `long`値、 `float`値、 `double`値、 参照値、 `byte`または`boolean`値、 `char`値、 `short`値を格納する。
  - `newarray` - 数値や文字の配列を作成し、その参照値をスタックに残す。
  - `anewarray` - 参照値の配列を作成し、その参照値をスタックに残す。
  - `multianewarray` - 多次元配列を作成し、その参照値をスタックに残す。
  - `arraylength` - 配列の長さを求め、スタックに残す。

#### その他

  - `athrow` - `java.lang.Throwable`のインスタンスで例外やエラーを発生させる。
  - [`nop`](../Page/NOP.md "wikilink") - 何もしない ()。
  - `breakpoint` - デバッガがブレークポイントの実装に使える命令。
  - `monitorenter` - オブジェクトのモニタをロックする。既に他のスレッドにロックされていれば待たされる。
  - `monitorexit` - オブジェクトのモニタをアンロックする。他のスレッドのロック待ちは再度試行される。
  - `wide` - ロード／ストア系命令や`ret`、`iinc`のインデックスを16ビットに拡張する。`iinc`では定数も16ビットに拡張する。

## 実装系

エンタープライズ用（デスクトップ用を包含）としては、[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、[IBM](../Page/IBM.md "wikilink")、[HPなどの各社から実装系がリリースされている](../Page/ヒューレット・パッカード.md "wikilink")。[OS上でアプリケーションとして動作する形態が一般的である](../Page/オペレーティングシステム.md "wikilink")。

[Windowsにも標準でJava仮想マシンが実装されていたが](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")との契約に反して自社仕様の拡張機能を付加したため、[Windows XP以降のOSではJavaの技術使用ライセンスを失った](../Page/Microsoft_Windows_XP.md "wikilink")。

また、オープンソースコミュニティの手によって[IKVM.NET](../Page/IKVM.NET.md "wikilink")という[共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink")上で動作するJava仮想マシンの実装も進められている。

変わった試みとしてGNU SmalltalkのVM上で構築されたJava仮想マシンが存在する。\[1\]

picoJava, Jazelle などJava仮想マシンの命令がハードウェア実装されたプロセッサ、すなわちバイトコードを直接実行可能なプロセッサも存在する。

### JITコンパイル

最初のJava仮想マシンの実装 (JDK 1.0) は[インタプリタ](../Page/インタプリタ.md "wikilink")型であったため、動作速度が他の[アプリケーションに比べて遅い場合があった](../Page/アプリケーションソフトウェア.md "wikilink")。そのため、メソッドの実行直前 (Just in Time) にバイトコードを[CPU](../Page/CPU.md "wikilink")のネイティブコードに[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")して実行する形式（[JITコンパイラ](../Page/実行時コンパイラ.md "wikilink")）を、[ボーランド](../Page/ボーランド.md "wikilink")や [IBM](../Page/IBM.md "wikilink")などがリリースした。サン・マイクロシステムズの実装もJDK 1.1からJITコンパイラを搭載した。

加えて、JDK 1.2から、サン・マイクロシステムズは[HotSpot](../Page/HotSpot.md "wikilink")という高速化技術を導入した。[HotSpot](../Page/HotSpot.md "wikilink")はJITコンパイラの一種だが、常にJITコンパイルを行うのではなく、実行回数が規定回数を超えたメソッド (Hotspot) のみをJITコンパイルする。これにより、JITコンパイルによる無駄なリソースの消費を防いだり、インタプリタ実行時のプロファイリング情報をJITコンパイル利用できる利点がある。[HotSpot](../Page/HotSpot.md "wikilink")には用途別に、クライアントVM（コンパイルは高速だが生成されるネイティブコードが相対的にあまり最適化されない）と、サーバVM（コンパイルは低速だが生成されるネイティブコードが相対的により最適化される）がある。

### スレッド

  - [グリーンスレッド](https://ja.wikipedia.org/wiki/グリーンスレッド "wikilink") - [pthread](https://ja.wikipedia.org/wiki/pthread "wikilink")等、OSが提供する[スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")を直接使わずJavaで仮想的なスレッドを作り実行する形式。現在はあまり利用されていない。
  - ネイティブスレッド - OSが提供するスレッドライブラリとJavaスレッドが1x1で対応する形式。

### ガベージコレクション

  - 世代別GC - [ヒープを](../Page/ヒープ領域.md "wikilink")2つ以上の世代に分割し、それぞれに異なるアルゴリズム（およびデータ構造）を適用する方式。

#### GCアルゴリズム（データ構造）

  - コピーGC
  - Mark & Sweep
  - Mostly Concurrent Mark & Sweep
  - Mark & Compact

## 脚注

## 関連項目

  - [動作環境](https://ja.wikipedia.org/wiki/動作環境 "wikilink")
  - [Apache Harmony](../Page/Apache_Harmony.md "wikilink")
  - [Dalvik仮想マシン](../Page/Dalvik仮想マシン.md "wikilink")
  - [HotSpot](../Page/HotSpot.md "wikilink")
  - [IcedTea](https://ja.wikipedia.org/wiki/IcedTea "wikilink")
  - [IKVM.NET](../Page/IKVM.NET.md "wikilink")
  - [Kaffe](https://ja.wikipedia.org/wiki/Kaffe "wikilink")
  - [leJOS](https://ja.wikipedia.org/wiki/leJOS "wikilink")
  - [SableVM](https://ja.wikipedia.org/wiki/SableVM "wikilink")

## 外部リンク

  - [The Java Virtual Machine Specification -Java SE 7 Edition-](http://docs.oracle.com/javase/specs/jvms/se7/html/)

[\*](https://ja.wikipedia.org/wiki/カテゴリ:Java仮想マシン "wikilink") [カテゴリ:Java](https://ja.wikipedia.org/wiki/カテゴリ:Java "wikilink") [カテゴリ:Java specification requests](https://ja.wikipedia.org/wiki/カテゴリ:Java_specification_requests "wikilink")

1.  <https://github.com/gnu-smalltalk/smalltalk/tree/master/packages/java>