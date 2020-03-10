> この記事は[Uuencode](https://ja.wikipedia.org/wiki/Uuencode)から翻訳されています。


**uuencode**は、バイナリデータをテキストデータに変換する[UNIX](../Page/UNIX.md "wikilink")及び[Unix系](../Page/Unix系.md "wikilink")OSのコマンド。或いは、それによって生成されるテキストデータのフォーマット。デコードには**uudecode**コマンドを用いる。[電子メール](../Page/電子メール.md "wikilink")や[ネットニュース](../Page/ネットニュース.md "wikilink")で多用され、現在でも多くのメーラーが対応しているが、[MIMEの](https://ja.wikipedia.org/wiki/Multipurpose_Internet_Mail_Extensions "wikilink")[Base64](https://ja.wikipedia.org/wiki/Base64 "wikilink")の方が一般的になっている。

## 概要

初期のUnix系OSでは[UUCPと呼ばれるプロトコルで電子メールやネットニュースの配送が行なわれた](../Page/Unix_to_Unix_Copy_Protocol.md "wikilink")。これらはテキストデータしか扱えないため、バイナリファイルをテキストデータに変換して送る手法として**uuencode**が提供された。uuencodeは**Unix to Unix ENCODE**の意である。

その後インターネットの環境が整備され、UUCPよりも[TCP/IPが一般的となるが](../Page/インターネット・プロトコル・スイート.md "wikilink")、電子メールやネットニュースは[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")、[NNTPといった](../Page/Network_News_Transfer_Protocol.md "wikilink") テキストベースの情報交換であったため、uuencodeは已然として広く使われた。

uuencodeはあくまでも添付のためのフォーマットであるため、[拡張子](../Page/拡張子.md "wikilink")は重要ではないが、単一のファイルとして保存する場合は拡張子は.uuか.uueが使われる場合が多い。

uuencodeにはいくつかの派生フォーマットがあるため、MIMEでは意図的にuuencodeを採用せず、新たにBase64を定義した。現在はこちらのBase64が広く使われている。

## 一般的な変換フォーマット

uuencodeのフォーマットは、一行のヘッダー、複数行のエンコード文字列、一行のフッターからなる。

ヘッダは次の書式である。ここで、<mode>は3桁の8進数であり、[UNIXのパーミッションを表す](https://ja.wikipedia.org/wiki/パーミッション#UNIX.E7.B3.BB.E3.81.AE.E3.83.91.E3.83.BC.E3.83.9F.E3.83.83.E3.82.B7.E3.83.A7.E3.83.B3 "wikilink")。<decode_pathname>はデコードされたときのファイル名である。パス名を含む事が出来るが一般にはファイル名のみである。

    <nowiki>
    begin <mode> <decode_pathname>
    </nowiki>

このあと、エンコードされた文字列が続き、以下のフッタで終わる。

    <nowiki>
    end
    </nowiki>

エンコードは3オクテット(24ビット)毎に行なわれる。これを4つの6ビット値に変換し、ASCII文字に割当てる。次は「Cat」という3オクテットのデータをASCIIの4文字に変換する例である。

|                |     |     |     |
| -------------- | --- | --- | --- |
| 元データ           | `C` | `a` | `t` |
| オクテット値         | 0   | 1   | 0   |
| エンコード後のASCII文字 | `0` | `V` | `%` |

6ビット値に0x20を加えたときの下位6ビットをASCII値とする。この変換を表にすると次のようになる。

|    |        |             |  |    |        |    |  |    |        |    |  |    |        |    |
| -- | ------ | ----------- |  | -- | ------ | -- |  | -- | ------ | -- |  | -- | ------ | -- |
|    | データ    | 文字          |  |    | データ    | 文字 |  |    | データ    | 文字 |  |    | データ    | 文字 |
|    |        |             |  |    |        |    |  |    |        |    |  |    |        |    |
| 0  | 000000 | スペース または \` |  | 16 | 010000 | 0  |  | 32 | 100000 | @  |  | 48 | 110000 | P  |
| 1  | 000001 | \!          |  | 17 | 010001 | 1  |  | 33 | 100001 | A  |  | 49 | 110001 | Q  |
| 2  | 000010 | "           |  | 18 | 010010 | 2  |  | 34 | 100010 | B  |  | 50 | 110010 | R  |
| 3  | 000011 | \#          |  | 19 | 010011 | 3  |  | 35 | 100011 | C  |  | 51 | 110011 | S  |
| 4  | 000100 | $           |  | 20 | 010100 | 4  |  | 36 | 100100 | D  |  | 52 | 110100 | T  |
| 5  | 000101 | %           |  | 21 | 010101 | 5  |  | 37 | 100101 | E  |  | 53 | 110101 | U  |
| 6  | 000110 | &           |  | 22 | 010110 | 6  |  | 38 | 100110 | F  |  | 54 | 110110 | V  |
| 7  | 000111 | '           |  | 23 | 010111 | 7  |  | 39 | 100111 | G  |  | 55 | 110111 | W  |
| 8  | 001000 | (           |  | 24 | 011000 | 8  |  | 40 | 101000 | H  |  | 56 | 111000 | X  |
| 9  | 001001 | )           |  | 25 | 011001 | 9  |  | 41 | 101001 | I  |  | 57 | 111001 | Y  |
| 10 | 001010 | \*          |  | 26 | 011010 | :  |  | 42 | 101010 | J  |  | 58 | 111010 | Z  |
| 11 | 001011 | \+          |  | 27 | 011011 | ;  |  | 43 | 101011 | K  |  | 59 | 111011 | \[ |
| 12 | 001100 | ,           |  | 28 | 011100 | \< |  | 44 | 101100 | L  |  | 60 | 111100 | \\ |
| 13 | 001101 | \-          |  | 29 | 011101 | \= |  | 45 | 101101 | M  |  | 61 | 111101 | \] |
| 14 | 001110 | .           |  | 30 | 011110 | \> |  | 46 | 101110 | N  |  | 62 | 111110 | ^  |
| 15 | 001111 | /           |  | 31 | 011111 | ?  |  | 47 | 101111 | O  |  | 63 | 111111 | _ |

元々「000000」はスペース文字であったが、かつて行末のスペースを取り去る転送系があったため、「\`」に置き換えられた。

デコードにおいては、変数 `c` にエンコードされた文字のASCIIコードが入っているとすると `(c XOR 0x20) AND 0x3f` でデコードできる（範囲外の文字が入っている可能性は考慮していない）。スペースの「\`」への置き換えには、このデコード法に全く変更を必要としないという利点があった。

次は「000000」にスペースを用いているuuencodeの一例である。これは[Solaris 10の](../Page/Solaris.md "wikilink")/usr/bin/uuencodeコマンドの出力である。

    <nowiki>
    begin 644 testimg.png
    MB5!.1PT*&@H    -24A$4@   "     @" 8   !S>GKT    !&=!34$  +&/
    M"_QA!0   $=)1$%46$?MUK$- " (!$#<?VA$W0 *FR/Y4OU<@RLBLM*>S-'Q
    M^^ZYH9TJ,!H%"! @0(  @1CMTO<9F$4! @0($"! X+? !I?UJM5MS!;U
    ) $E%3D2N0F""

    end
    </nowiki>

行の先頭はその行に含まれるオクテット数を示す。通常は45オクテットなので「M」であり、45オクテットに満たない行は別の文字となる。このケースでは「)」である。そのあとデータの終了を示すため、0オクテットを示す「スペース」のみの行が続き、「end」で終わる。

次は「000000」に「\`」を用いている一例である。これはGNU sharutils 4.2.1に含まるuuencodeコマンドの出力である。

    <nowiki>
    begin 644 testimg.png
    MB5!.1PT*&@H````-24A$4@```"`````@"`8```!S>GKT````!&=!34$``+&/
    M"_QA!0```$=)1$%46$?MUK$-`"`(!$#<?VA$W0`*FR/Y4OU<@RLBLM*>S-'Q
    M^^ZYH9TJ,!H%"!`@0(``@1CMTO<9F$4!`@0($"!`X+?`!I?UJM5MS!;U````
    )`$E%3D2N0F""
    `
    end
    </nowiki>

行末にスペースが現れない。この他に、スペースと「\`」が混在しているケースも存在する。

これらのフォーマットは多くのデコーダでデコード出来る。

## 派生フォーマット

（初期のフォーマットには）以下のような問題が存在した。

  - メールなどで行末などのスペースを削除するシステムがある
  - 転送エラーによる文字化けが検出できない
  - ASCIIを前提としているため、EBCDICなどのシステムで問題がある

これらの問題を解決するため、多くの派生フォーマットが誕生した。

スペースの問題は、スペースを「\`」に置き換える事で解決された。また、現在多用されているTCP/IPでは、転送エラーはTCPで検出される。同じく多用されているSMTPやNNTPも同様にASCIIを前提としている。よってそれらの環境で問題になることは稀である。

### 行末のスペースの問題を回避するもの

次は[MINIX 3.1.2aのuueコマンドの出力である](https://ja.wikipedia.org/wiki/MINIX "wikilink")。

    <nowiki>
    table
     !"#$%&'()*+,-./0123456789:;<=>?
    @ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_
    begin 644 testimg.png
    MB5!.1PT*&@H    -24A$4@   "     @" 8   !S>GKT    !&=!34$  +&/z
    M"_QA!0   $=)1$%46$?MUK$- " (!$#<?VA$W0 *FR/Y4OU<@RLBLM*>S-'Qy
    M^^ZYH9TJ,!H%"! @0(  @1CMTO<9F$4! @0($"! X+? !I?UJM5MS!;U    x
    ) $E%3D2N0F""w
     v
    end
    </nowiki>

行の最後に1文字追加する事で、行末のスペースの問題を回避している。また、追加された文字はアルファベットの小文字の逆順になっており、行を分割して転送した場合に元に戻すときの目印となる。行の先頭文字でオクテット数が示されているため、デコード時に最後に付加された文字が無視されれば、正常にデコードされる可能性がある。

最初のテーブルは、使っている文字を列挙することで、文字が正常に使えるかどうかを確認するためのものである。

### チェックサムの追加

次はMark Hortonによって書かれ、Alan J Rosenthatlによって行末に[チェックサム](../Page/チェックサム.md "wikilink")が追加されるようになったuuencode.c 5.3-2 (Berkeley) 3/1/88の出力である。最後に元データのオクテット数も追加している。

    <nowiki>
    begin 644 testimg.png
    MB5!.1PT*&@H````-24A$4@```"`````@"`8```!S>GKT````!&=!34$``+&/`
    M"_QA!0```$=)1$%46$?MUK$-`"`(!$#<?VA$W0`*FR/Y4OU<@RLBLM*>S-'QR
    M^^ZYH9TJ,!H%"!`@0(``@1CMTO<9F$4!`@0($"!`X+?`!I?UJM5MS!;U````!
    )`$E%3D2N0F""R
    ``
    end
    size 144
    </nowiki>

次はRichard Marksによる[DOS用のuuencodeに](../Page/DOS_\(OS\).md "wikilink")-Lオプションを付けて、チェックサムを追加した例である。チェックサムの演算方法が上記のものと異なるため、互換性がない。行単位だけでなく全体のチェックサムも追加している。

    <nowiki>
    section 1 of 1 of file testimg.png  < uuencode 96 (v50) by R.E.M. >

    begin 644 testimg.png
    MB5!.1PT*&@H````-24A$4@```"`````@"`8```!S>GKT````!&=!34$``+&/C
    M"_QA!0```$=)1$%46$?MUK$-`"`(!$#<?VA$W0`*FR/Y4OU<@RLBLM*>S-'Q9
    M^^ZYH9TJ,!H%"!`@0(``@1CMTO<9F$4!`@0($"!`X+?`!I?UJM5MS!;U````7
    )`$E%3D2N0F""?
    ``
    end
    sum -r/size 58653/233 section (from "begin" to "end")
    sum -r/size 18364/144 entire input file
    </nowiki>

### xxencode

次はxxencodeと呼ばれるフォーマットである。xxencode.c 5.3 (Berkeley) 1/22/85による出力である。

    <nowiki>
    begin 644 testimg.png
    hWJ-CFko84Uc++++BGIV2IU+++0+++++U0+M+++-nSbfo++++-4R-HI2++94D
    h0zlV-E+++2R7F23IK2Thpf2B+0+6-21QTqV2rE+8amDtIjpQUmgWgh8SnB5l
    hyyutcNoeA-c30-+UE6++UFXhojQNa2I-+UE620-+s9T+-dTpehJhn-Pp++++
    7+2Z3HYGiEa00
    +
    end
    </nowiki>

「000000」から「111111」を「+-0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz 」に割当てている。uuencodeはASCIIの文字を用いているが、[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")と呼ばれる[文字コード](../Page/文字コード.md "wikilink")を用いる実装では扱えない文字があったため、使う文字を入れ替えたのがxxencodeである。極めて古い転送路のための手法であり、インターネットではASCIIが使えないケースは稀であるため、xxencodeはほとんど使われない。uuencodeとの互換性は全くない。

### POSIX IEEE Std 1003.1

[POSIX](../Page/POSIX.md "wikilink")では、今迄のアルゴリズムを「歴史的なアルゴリズム (uuencode Historical Algorithm)」とし、新たなアルゴリズムを定義した。

    <nowiki>
    begin-base64 644 testimg.png
    iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAABGdBTUEAALGPC/xhBQAAAEdJREFU
    WEft1rENACAIBEDcf2hE3QAKmyP5Uv1cgysistKezNHx++65oZ0qMBoFCBAgQIAAgRjt0vcZmEUB
    AgQIECBA4LfABpf1qtVtzBb1AAAAAElFTkSuQmCC
    ====
    </nowiki>

先頭行は「begin-base64 <mode> <decode_pathname>」、最終行は「====」となっているため、今迄のuuencodeと区別出来る。変換アルゴリズムは[Base64](https://ja.wikipedia.org/wiki/Base64 "wikilink")をそのまま流用している。これはxxencodeと同様、EBCDIC等への対処である。 そもそもMIMEではuuencodeを除外した経緯があるが、逆にMIMEのBase64をuuencodeに取り込んだ形である。現在は通常のBase64が広く使われているため、この方式はあまり使われない。

## MIMEへの対応

電子メールやネットニュースでuuencodeを用いる場合、本文中にuuencode文字列を直接貼付ける方法が取られた。MIMEでは意図的にuuencodeを除外したので、uuencodeをマルチパートで扱う手法は定義されていない。しかしながら、マルチパートの枠組みで扱う実装が多数登場した。大きく分けて2つの手法がある。一方はContent-Transfer-Encodingでx-uuencodeを表す。もう一方はContent-Typeでapplication/x-uuencodeを表す。前者の方が実装が多い。

    <nowiki>
    Content-Type: image/png; name="testimg.png"
    Content-Transfer-Encoding: x-uuencode
    Content-Disposition: inline; filename="testimg.png"

    begin 644 testimg.png
    MB5!.1PT*&@H````-24A$4@```"`````@"`8```!S>GKT````!&=!34$``+&/
    M"_QA!0```$=)1$%46$?MUK$-`"`(!$#<?VA$W0`*FR/Y4OU<@RLBLM*>S-'Q
    M^^ZYH9TJ,!H%"!`@0(``@1CMTO<9F$4!`@0($"!`X+?`!I?UJM5MS!;U````
    )`$E%3D2N0F""
    `
    end
    </nowiki>

    <nowiki>
    Content-Type: application/x-uuencode; name="testimg.png"
    Content-Disposition: attachment; filename="testimg.png"
    Content-Transfer-Encoding: 7bit

    begin 644 testimg.png
    MB5!.1PT*&@H````-24A$4@```"`````@"`8```!S>GKT````!&=!34$``+&/
    M"_QA!0```$=)1$%46$?MUK$-`"`(!$#<?VA$W0`*FR/Y4OU<@RLBLM*>S-'Q
    M^^ZYH9TJ,!H%"!`@0(``@1CMTO<9F$4!`@0($"!`X+?`!I?UJM5MS!;U````
    )`$E%3D2N0F""
    `
    end
    </nowiki>

## 参照

  - [IEEE Std 1003.1 uuencode man page](http://www.opengroup.org/onlinepubs/009695399/utilities/uuencode.html)
  - [Online UUencoder/UUdecoder](http://www.webutils.pl/UUencode)

## 関連項目

  - [Base64](https://ja.wikipedia.org/wiki/Base64 "wikilink")
  - [ish](https://ja.wikipedia.org/wiki/ish "wikilink")
  - [BinHex](../Page/BinHex.md "wikilink")

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")