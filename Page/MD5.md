> この記事は[MD5](https://ja.wikipedia.org/wiki/MD5)から翻訳されています。


**MD5**（エムディーファイブ、）は、[暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")のひとつである。ハッシュ値は128ビット。

## 概要

[MD4](../Page/MD4.md "wikilink")が前身であり、安全性を向上させたものとされている（いずれにしろ2018年現在、暗号学的ハッシュ関数として必要な強度が要求される目的に使ってはいけない）。1991年に開発された。開発者もMD4と同じく[ロナルド・リベスト](../Page/ロナルド・リベスト.md "wikilink")。

システムにもよるが、`md5sum` や `md5` というような名前のコマンドで、

> `d41d8cd98f00b204e9800998ecf8427e` （入力データ長が0バイトの場合）

のようにハッシュ値が得られる。

## 用途

一般的な[暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")の用途と同じであり、MD5として特筆事項は無い。ただし後述の脆弱性について確認のこと。いずれにしても2018年現在において、弱点が発見されていることを筆頭に暗号学的ハッシュ関数として必要な強度は既に残っていないので、強度が必要な場合には使ってはいけない（あるいは、それが判断できないならば単純に、使ってはいけない）。

## 実際の使用例

FreeBSDはインストール可能なCDイメージと、それのMD5値を同時に配布している。（MD5値の改変はないと仮定して）インストール可能なCDイメージが、途中で改変されていないことを確認してみる。

1.  md5 コマンドを、イメージファイルに実行する。
      -
        localhost% md5 5.1-RELEASE-i386-miniinst.iso
        MD5 (5.1-RELEASE-i386-miniinst.iso) = 646da9ae5d90e6b51b06ede01b9fed67
2.  CHECKSUM.MD5の中身を確認し、一致していれば破損の可能性は極めて低いことが分かる。
      -
        localhost% cat CHECKSUM.MD5
        MD5 (5.1-RELEASE-i386-disc1.iso) = 3b6619cffb5f96e1acfa578badae372f
        MD5 (5.1-RELEASE-i386-disc2.iso) = 2cfa746974210d68e96ee620bf842fb6
        MD5 (5.1-RELEASE-i386-miniinst.iso) = 646da9ae5d90e6b51b06ede01b9fed67

## 安全性

MD5、および[RIPEMD](https://ja.wikipedia.org/wiki/RIPEMD "wikilink")とよばれるハッシュ関数には理論的な弱点が存在することが明らかとなっている（外部リンク参照）。

2004年8月、暗号の国際会議 CRYPTO （のランプセッション）にて、MD5のコリジョンを求めることができたという報告があった。理論的可能性として、MD5を用いて改竄されないことを確認する場合、あらかじめ正規のファイルと不正なファイルを用意しておき、正規のファイルを登録しておきながら、実際には同じMD5を持つ不正なファイルに摩り替える攻撃がありえることを意味する。また2007年11月、2つの全く異なる実行ファイルを元に、各々の末尾にデータブロックを付加し、その部分を変更しながら探索を行うことにより、同一のMD5を持たせることに成功したという報告があった。この攻撃方法は実証されたことになる。

[アメリカ合衆国政府](https://ja.wikipedia.org/wiki/アメリカ合衆国政府 "wikilink")では、MD5ではなく、[Secure Hash Algorithm](../Page/Secure_Hash_Algorithm.md "wikilink") (SHA)を標準のハッシュとして使用している。 日本の[CRYPTREC](../Page/CRYPTREC.md "wikilink")では、MD5を政府推奨暗号リストから外し、SHA-256 ([SHA-2](https://ja.wikipedia.org/wiki/SHA-2 "wikilink")のバリエーション) 以上を推奨している。

### ハッシュの衝突耐性について

MD5 のハッシュ値については、パソコンレベルでも数10分程度で、同一ハッシュ値の非ユニークなデータ列を生成できる実装が広まっている。すなわち、強衝突耐性は容易に突破されうる状態にある（[SHA-0](https://ja.wikipedia.org/wiki/SHA-0 "wikilink")/[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")アルゴリズムについても、MD5ほど容易ではないが突破される脆弱性が発見されている）。

ただし、任意に与えられたハッシュ値に対して、（何らかの別の）データを生成する実装が広まっているわけではないので、弱衝突耐性が容易に突破されうる訳ではない。また、任意に与えられたハッシュ値に対して、改竄者の意図どおりのデータ列を容易に生成できる訳でもない（もしそうならば、それは既に暗号ではない）。

強衝突耐性の突破とは例えば、同一のハッシュ値を持つ非ユニークな2つのデータ列D1とD2のペアを1つ発見できた、ということである。なお、この場合D1やD2が意味を持つデータであるかどうかは問われない。また、データ列D3のハッシュ値がHであったとして、この"特定の"ハッシュ値Hに対して、同一のハッシュ値を持つような他のデータ列D4を発見できたとしたら、それは弱衝突耐性を突破された事を意味する（即ち、D3とHの組み合わせで無[改竄](../Page/改竄.md "wikilink")性を証明できなくなる）。

そのため、直ちにこれらのハッシュアルゴリズムを用いている暗号化通信が盗聴・改竄されたり、電子署名の有効性が無くなると言うわけではない。しかし、強衝突耐性が突破されたという事は、将来的には攻撃手法や計算能力の進化により、弱衝突耐性も突破されうるという事を暗示する。もし弱衝突耐性が突破されたとしたら、もはや暗号化通信や電子署名の無改竄性を証明できなくなり、その暗号化・署名システムは（半ば）死を意味する。

また、暗号化・署名システムのintegrity（例えば最良攻撃手法に対して十分に頑強であるという事）にハッシュ強衝突耐性の突破が困難であるという前提がもし有った場合には、そのシステムのintegrityも当然に失われる事になる。Integrityを要求されるシステムでは、その再検証が最低限必要となる。

### APOPの脆弱性

2007年4月IPAは[APOP](https://ja.wikipedia.org/wiki/APOP "wikilink")の脆弱性について警告した\[1\]。これは[電気通信大学](../Page/電気通信大学.md "wikilink")の太田和夫（[暗号理論](../Page/暗号理論.md "wikilink")）らが発見したもので\[2\]、APOPのプロトコル上の弱点を利用して、MD5ハッシュから理論的に元のパスワードを求めることが出来るというものである。これの対策としては、SSLの利用が推奨されている。（総当たり攻撃法によるツールは既に公表されている）

### Flame攻撃に関して

[2012年](../Page/2012年.md "wikilink")4月に発覚した「Flame攻撃」（[Microsoft Updateに対するなりすまし攻撃](../Page/Microsoft_Update.md "wikilink")）において、一部の[デジタル証明書](https://ja.wikipedia.org/wiki/デジタル証明書 "wikilink")の署名アルゴリズムにMD5が使われていたことから、MD5 の衝突耐性に関する脆弱性をついて、デジタル証明書の偽造が行われたように一部媒体では報道されている\[3\]。

しかし、米[ソフォス](../Page/ソフォス.md "wikilink") (Sophos) 社の記事によると\[4\]、[マイクロソフト](../Page/マイクロソフト.md "wikilink")がコード署名に使用できるデジタル証明書であって、ターミナルサーバーライセンスインフラストラクチャ（中間Certificate Authenticity）上で使用できるものを、誤って発行していた事が原因とされている。また、Flameマルウェアが攻撃に使用したデジタル証明書を入手した経路、また前述の MD5 で署名された証明書をクラックして偽造したものであるか否かは明らかになっていないとしている。一方マイクロソフトは、[Windows Vista以降のバージョンにおけるコード署名の検証を回避するためには攻撃者が](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") MD5 の衝突を利用して特定の拡張フィールドを削除する必要があったとしている\[5\]。

マイクロソフトは2012年[6月5日](https://ja.wikipedia.org/wiki/6月5日 "wikilink")に、問題となったターミナルサーバーライセンスインフラストラクチャの中間Certificate Authenticityを無効化するセキュリティアップデートを公開している\[6\]。

## アルゴリズム

[MD5_algorithm.svg](https://ja.wikipedia.org/wiki/File:MD5_algorithm.svg "fig:MD5_algorithm.svg")<sub>*s*</sub>は左への*s*ビットのローテーション操作であり、*s*は操作ごとに異なる。[Addition](https://ja.wikipedia.org/wiki/File:Boxplus.png "fig:Addition")は2<sup>32</sup>を法とした加算である。\]\]

MD5は可変長の入力を処理して、128ビット固定長の値を出力する。入力メッセージは512ビット（32ビットのワードが16個）ごとに切り分けられるが、長さが512の倍数となるように[パディング](https://ja.wikipedia.org/wiki/パディング "wikilink")が行われる。 パディングとしてはまずメッセージの最後に1ビットの1を足して、その後には長さが512で割って448余る（つまり、512の倍数に64足りない）長さになるようにひたすら0を付け足していく。そして、残った64ビットには元のメッセージの長さ（の下位64ビット）を入れることとなる。

MD5のメイン部分のアルゴリズムは32ビット×4ワード（それぞれのワードを*A*、*B*、*C*、*D*と表す） = 128ビットの状態を持って進行していく。初期状態では、この4ワードは決まった定数で初期化されており、 512ビットのブロックを順次使ってこの状態を変化させていくのがMD5の中核となっている。1回の処理では非線形な関数*F*、2<sup>32</sup>を[法とした加算](https://ja.wikipedia.org/wiki/合同式 "wikilink")、左への[ビットローテート](https://ja.wikipedia.org/wiki/ビットローテート "wikilink")が行われる。 そして、16回の操作を1ラウンドとして、512ビットの入力ブロックを処理するのに4ラウンドの処理が行われる。*F*には4通りの関数があり、ラウンドごとに異なるものが使われる。

\[F(B,C,D) = (B\wedge{C}) \vee (\neg{B} \wedge{D})\]

\[G(B,C,D) = (B\wedge{D}) \vee (C \wedge \neg{D})\]

\[H(B,C,D) = B \oplus C \oplus D\]

\[I(B,C,D) = C \oplus (B \vee \neg{D})\]

\(\oplus, \wedge, \vee, \neg\)はそれぞれ[XOR](../Page/排他的論理和.md "wikilink")、[AND](../Page/論理積.md "wikilink")、[OR](../Page/論理和.md "wikilink")、[NOT演算を意味する](../Page/否定.md "wikilink")。

### 擬似コード

MD5ハッシュは、以下の擬似コードで書いたアルゴリズムで算出される。値はすべて[リトルエンディアンとする](https://ja.wikipedia.org/wiki/エンディアンネス "wikilink")。

**`function`**` md5 (message : `**`array`**`[0..*] `**`of`**` bit) `**`returns`**` `**`array`**`[0..15] `**`of`**` unsignedInt8 `**`is`**
`    `<span style="color:green">`//`*`左ローテート関数`*</span>
`    `**`function`**` leftRotate (x : unsignedInt32, c : integer `**`range`**` 0..31) `**`returns`**` unsignedInt32 `**`is`**
`    `**`begin`**` leftRorate := (x `**`leftShift`**` c) `**`bitOr`**` (x `**`rightShift`**` (32-c)) `**`end`**` ;`

`    `**`function`**` makeK (i : integer `**`range`**` 0..63) `**`returns`**` unsignedIt32 `**`is`**
`    `**`begin`**` makeK := floor(2`<sup>`32`</sup>`×abs(sin(i + 1))) `**`end`**` ;`

**`begin`**
<span style="color:green">`//`*`注:``   ``すべての変数は符号なし32ビット値で、桁があふれた時は2`<sup>`32`</sup>`を法として演算されるものとする。`*</span>

<span style="color:green">`//`*`ラウンドごとのローテート量``   ``sを指定する`*</span>
**`const`**` s : `**`array`**`[0..63] `**`of`**` unsignedInt32 :=`
`  {`
`   7, 12, 17, 22,  7, 12, 17, 22,  7, 12, 17, 22,  7, 12, 17, 22,`
`   5,  9, 14, 20,  5,  9, 14, 20,  5,  9, 14, 20,  5,  9, 14, 20,`
`   4, 11, 16, 23,  4, 11, 16, 23,  4, 11, 16, 23,  4, 11, 16, 23,`
`   6, 10, 15, 21,  6, 10, 15, 21,  6, 10, 15, 21,  6, 10, 15, 21`
`  } ;`

<span style="color:green">`//`*`整数ラジアンのときの三角関数からKの値を生成する`*</span>
**`const`**` K : `**`array`**`[0..63] `**`of`**` unsignedInt32 := `**`range`**` 0..63 `**`map`**` makeK  ;`

<span style="color:green">`//`*`（Kを事前に計算して、テーブルとしておくこともできる）`*</span>
<span style="color:green">`//`</span>
<span style="color:green">`//`**`const`**` K : `**`array`**`[0..63] `**`of`**` unsignedInt32 :=`</span>
<span style="color:green">`//  {`</span>
<span style="color:green">`//  D76AA478`<sub>`(16進数)`</sub>`, E8C7B756`<sub>`(16進数)`</sub>`, 242070DB`<sub>`(16進数)`</sub>`, C1BDCEEE`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  F57C0FAF`<sub>`(16進数)`</sub>`, 4787C62A`<sub>`(16進数)`</sub>`, A8304613`<sub>`(16進数)`</sub>`, FD469501`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  698098D8`<sub>`(16進数)`</sub>`, 8B44F7AF`<sub>`(16進数)`</sub>`, FFFF5BB1`<sub>`(16進数)`</sub>`, 895CD7BE`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  6B901122`<sub>`(16進数)`</sub>`, FD987193`<sub>`(16進数)`</sub>`, A679438E`<sub>`(16進数)`</sub>`, 49B40821`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  F61E2562`<sub>`(16進数)`</sub>`, C040B340`<sub>`(16進数)`</sub>`, 265E5A51`<sub>`(16進数)`</sub>`, E9B6C7AA`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  D62F105D`<sub>`(16進数)`</sub>`, 02441453`<sub>`(16進数)`</sub>`, D8A1E681`<sub>`(16進数)`</sub>`, E7D3FBC8`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  21E1CDE6`<sub>`(16進数)`</sub>`, C33707D6`<sub>`(16進数)`</sub>`, F4D50D87`<sub>`(16進数)`</sub>`, 455A14ED`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  A9E3E905`<sub>`(16進数)`</sub>`, FCEFA3F8`<sub>`(16進数)`</sub>`, 676F02D9`<sub>`(16進数)`</sub>`, 8D2A4C8A`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  FFFA3942`<sub>`(16進数)`</sub>`, 8771F681`<sub>`(16進数)`</sub>`, 6D9D6122`<sub>`(16進数)`</sub>`, FDE5380C`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  A4BEEA44`<sub>`(16進数)`</sub>`, 4BDECFA9`<sub>`(16進数)`</sub>`, F6BB4B60`<sub>`(16進数)`</sub>`, BEBFBC70`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  289B7EC6`<sub>`(16進数)`</sub>`, EAA127FA`<sub>`(16進数)`</sub>`, D4EF3085`<sub>`(16進数)`</sub>`, 04881D05`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  D9D4D039`<sub>`(16進数)`</sub>`, E6DB99E5`<sub>`(16進数)`</sub>`, 1FA27CF8`<sub>`(16進数)`</sub>`, C4AC5665`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  F4292244`<sub>`(16進数)`</sub>`, 432AFF97`<sub>`(16進数)`</sub>`, AB9423A7`<sub>`(16進数)`</sub>`, FC93A039`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  655B59C3`<sub>`(16進数)`</sub>`, 8F0CCC92`<sub>`(16進数)`</sub>`, FFEFF47D`<sub>`(16進数)`</sub>`, 85845DD1`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  6FA87E4F`<sub>`(16進数)`</sub>`, FE2CE6E0`<sub>`(16進数)`</sub>`, A3014314`<sub>`(16進数)`</sub>`, 4E0811A1`<sub>`(16進数)`</sub>`,`</span>
<span style="color:green">`//  F7537E82`<sub>`(16進数)`</sub>`, BD3AF235`<sub>`(16進数)`</sub>`, 2AD7D2BB`<sub>`(16進数)`</sub>`, EB86D391`<sub>`(16進数)`</sub></span>
<span style="color:green">`//  } ;`</span>

<span style="color:green">`//`*`A、B、C、Dの初期値`*</span>
**`var`**` a0 : unsignedInt32 := 67452301`<sub>`(16進数)`</sub>` ; `<span stylE="Color:green">`// A`</span>
**`var`**` b0 : unsignedInt32 := EFCDAB89`<sub>`(16進数)`</sub>` ; `<span stylE="Color:green">`// B`</span>
**`var`**` c0 : unsignedInt32 := 98BADCFE`<sub>`(16進数)`</sub>` ; `<span stylE="Color:green">`// C`</span>
**`var`**` d0 : unsignedInt32 := 10325476`<sub>`(16進数)`</sub>` ; `<span stylE="Color:green">`// D`</span>

<span style="color:green">`//`*`パディング処理:``   ``1ビットのデータ「1」を追加する`*</span>
`message[message.length] = (bit) 1 ;`
<span style="color:green">`//`*`注:``   ``入力のバイト値は、最高位ビットが先のビットであるビット列として解釈するものとする`\[7\]`。`*</span>

**`const`**` initial_message_length : integer := message.length ;`

<span style="color:green">`//`*`パディング処理:``   ``残りは「0」で埋める`*</span>
**`repeat`**
`    message[message.length] := (bit) 0`
**`until`**` (message.length `**`mod`**` 512) ＝ 448 ; `<span style="color:green">`//`*`448``   ``＝``   ``512``   ``－``   ``64`*</span>
`message[message.length .. message.length+63] := split (initial_message_length `**`mod`**` 2`<sup>`64`</sup>`, 1bit) ;`
</span>

<span style="color:green">`//`*`入力を512ビットのブロックに切って、順次処理する`*</span>
<span style="color:green">`//`*`chunk``   ``のバイトオーダーは``   ``message``   ``のバイトオーダーのままである`*</span>
**`var`**` chunk : bits512 ;`
**`for``   ``each`**` chunk `**`of`**` split (message, 512bit) `**`do`**
`    `**`var`**` M : `**`array`**` [0..15] `**`of`**` unsignedInt32 := split (chunk, 32bit) ;`
<span style="color:green">`//`*`内部状態の初期化`*</span>
`    `**`var`**` A : unsignedInt32 := a0 ;`
`    `**`var`**` B : unsignedInt32 := b0 ;`
`    `**`var`**` C : unsignedInt32 := c0 ;`
`    `**`var`**` D : unsignedInt32 := d0 ;`
<span style="color:green">`//`*`メインループ`*</span>
`    `**`var`**` F : unsignedInt32 ;`
`    `**`var`**` g : integer `**`range`**` 0..15 ;`
`    `**`for`**` i `**`from`**` 0 `**`to`**` 63`
`        `**`switch`**
`            `**`case`**` 0 ≦ i ≦ 15 `**`do`**
`                F := (B `**`bitAnd`**` C) `**`bitOr`**` ((`**`bitNot`**` B) `**`bitAnd`**` D) ;`
`                g := i`
`            `**`end``   ``case`**
`            `**`case`**` 16 ≦ i ≦ 31 `**`do`**
`                F := (D `**`bitAnd`**` B) `**`bitOr`**` ((`**`bitNot`**` D) `**`bitAnd`**` C) ;`
`                g := (5×i + 1) `**`mod`**` 16`
`            `**`end``   ``case`**
`            `**`case`**` 32 ≦ i ≦ 47 `**`do`**
`                F := (B `**`bitXor`**` C) `**`bitXor`**` D ;`
`                g := (3×i + 5) `**`mod`**` 16`
`            `**`end``   ``case`**
`            `**`case`**` 48 ≦ i ≦ 63 `**`do`**
`                F := C `**`bitXor`**` (B `**`bitOr`**` (`**`bitNot`**` D)) ;`
`                g := (7×i) `**`mod`**` 16`
`            `**`end``   ``case`**
`        `**`end``   ``switch`**
`        F := F + A + K[i] + M[g] ;`
`        (D, C, A) := (C, B, D) ;`
`        B := B + leftRotate(F, s[i]) ;`
`    `**`end``   ``for`**` ;`
<span style="color:green">`//`*`今までの結果にこのブロックの結果を足す`*</span>
`    a0 := a0 + A ;`
`    b0 := b0 + B ;`
`    c0 := c0 + C ;`
`    d0 := d0 + D`
**`end``   ``for`**` ;`

`//`<span style="color:green">`16個の8ビット符号なし整数型データ列がMD5値である。`</span>
`//`<span style="color:green">*`リトルエンディアンでの出力`*</span>
`md5[ 0.. 3] := split (a0, 8bit) ;`
`md5[ 4.. 7] := split (b0, 8bit) ;`
`md5[ 8..11] := split (c0, 8bit) ;`
`md5[12..15] := split (d0, 8bit) ;`
**`end`**`.`

なお、RFC 1321 にある本来の式に代えて、以下のように計算するほうが効率的な場合がある（高級言語で書いている場合、コンパイラの最適化に任せるほうがよい。 NANDとANDが並行して計算できる環境であれば、並列演算のできない以下の式に比べて、元のままのほうが速いことも多々ある）。

`( 0 ≦ i ≦ 15): F := D `**`bitXor`**` (B `**`bitAnd`**` (C `**`bitXor`**` D))`
`(16 ≦ i ≦ 31): F := C `**`bitXor`**` (D `**`bitAnd`**` (B `**`bitXor`**` C))`

## 実装ライブラリ

MD5をサポートしているライブラリは以下の通り。

  - [Botan](https://ja.wikipedia.org/wiki/:en:Botan_\(programming_library\) "wikilink")
  - [Bouncy Castle](https://ja.wikipedia.org/wiki/:en:Bouncy_Castle_\(cryptography\) "wikilink")
  - [cryptlib](https://ja.wikipedia.org/wiki/:en:Cryptlib "wikilink")
  - [Crypto++](https://ja.wikipedia.org/wiki/:en:Crypto++ "wikilink")
  - [Libgcrypt](https://ja.wikipedia.org/wiki/:en:Libgcrypt "wikilink")
  - [Nettle](https://ja.wikipedia.org/wiki/:en:Nettle_\(cryptographic_library\) "wikilink")
  - [OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")
  - [wolfSSL](https://ja.wikipedia.org/wiki/wolfSSL "wikilink")

## 参考文献

  - R. Rivest, "The MD5 Message-Digest Algorithm", RFC 1321, April 1992.
  - Hans Dobbertin, "The Status of MD5 After a Recent Attack", CryptoBytes Volume 2, Number 2, pp.1,3-6, Summer 1996. [1](ftp://ftp.rsa.com/pub/cryptobytes/crypto2n2.pdf)
  - Xiaoyun Wang, Dengguo Feng, Xuejia Lai, Hongbo Yu, "Collisions for Hash Functions MD4, MD5, HAVAL-128 and RIPEMD", IACR ePrint \#199, Augst 17 2004. [2](http://eprint.iacr.org/2004/199.pdf)

## 脚注

<references />

## 関連項目

  - [ハッシュ関数](../Page/ハッシュ関数.md "wikilink")
  - [MD2](../Page/MD2.md "wikilink")
  - [MD4](../Page/MD4.md "wikilink")
  - [Secure Hash Algorithm](../Page/Secure_Hash_Algorithm.md "wikilink") - [SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink") - [SHA-2](https://ja.wikipedia.org/wiki/SHA-2 "wikilink") (SHA-224, SHA-256, SHA-384, SHA-512) - [SHA-3](../Page/SHA-3.md "wikilink")
  - [HMAC](../Page/HMAC.md "wikilink")
  - [巨大数](../Page/巨大数.md "wikilink")

## 外部リンク

  - RFC 1321
      - [MD5 メッセージダイジェストアルゴリズム (The MD5 Message-Digest Algorithm)](https://www.ipa.go.jp/security/rfc/RFC1321JA.html)（[IPAによる日本語訳](../Page/情報処理推進機構.md "wikilink")）
  - RFC 6151: RFC 1321のsecurity considerationsについて置き換えるものであると規定している。
  - [MD2, MD4, MD5 Online Calculator](http://www.webutils.pl/MD5_Calculator) Calculate file hashes using an on-line web form.
  - [Online MD5 crack](http://passcracking.ru) – Rainbow Tables + big hash database (md5, md5(md5), sha1, mysql)
  - [MD5 cracking by RainbowTables](http://passcrack.spb.ru)
  - [Simple hash calculator](http://www.hash.spugesoft.com)
  - [高速にMD5ハッシュの元の文字を見つけ出すツール](http://www.vector.co.jp/soft/unix/util/se365582.html)
  - [Online MD5 Reverser | Hash cracker](http://ice.breaker.free.fr/)
  - [マイクロソフト セキュリティ アドバイザリ (961509): 研究機関によるMD5対する衝突攻撃(collision attack)の実現可能性にの実証に関して](http://www.microsoft.com/japan/technet/security/advisory/961509.mspx)
  - [Secure hash calculator](http://neuage.biz/tools/md5.html)

[Category:ハッシュ関数](https://ja.wikipedia.org/wiki/Category:ハッシュ関数 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  [IPA:APOP におけるパスワード漏えいの脆弱性](http://www.ipa.go.jp/security/vuln/documents/2007/JVN_19445002.html)
2.  [Software Integrity Checksum and Code Signing Vulnerability](http://www.win.tue.nl/hashclash/SoftIntCodeSign/)
3.  [MS、Flameによる偽造証明書発生で多重対策を実施 - 証明書のルート分離やWUなど強化](http://www.security-next.com/031519)
4.  [Flame malware used man-in-the-middle attack against Windows Update](http://nakedsecurity.sophos.com/2012/06/04/flame-malware-used-man-in-the-middle-attack-against-windows-update/)
5.  [Flame malware collision attack explained](http://blogs.technet.com/b/srd/archive/2012/06/06/more-information-about-the-digital-certificates-used-to-sign-the-flame-malware.aspx)
6.  [マイクロソフト セキュリティ アドバイザリ (2718704)](http://technet.microsoft.com/ja-jp/security/advisory/2718704)
7.  `RFC``   ``1321,``   ``section``   ``2,``   ``"Terminology``   ``and``   ``Notation",``   ``Page``   ``2.`