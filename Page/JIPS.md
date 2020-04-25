> この記事は[JIPS](https://ja.wikipedia.org/wiki/JIPS)から翻訳されています。


**JIPS**（ジップス　Japanese Information Processing System）は[NECが開発した日本語処理システムの名前である](../Page/日本電気.md "wikilink")。実際上は、『JIPS』という用語は、そのシステム上で使われる漢字コードの事を指していることが多いため、本稿ではその漢字コードについて説明する。

## 概要

『JIPS』にて使われる漢字コードは、[JIS C 6226](https://ja.wikipedia.org/wiki/JIS_C_6226 "wikilink")-1978をベースに拡張文字を9区〜13区に登録し、さらにGR域に『G1集合』と呼ばれる拡張文字群を登録した符号化文字集合である。

  - 上記そのものを表す**JIPS(J)**
  - JIPS(J)の上1バイト、下1バイトをそれぞれ[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")に変換して得られる**JIPS(E)**
  - JIPS(J)の上1バイトを[ASCII](../Page/ASCII.md "wikilink")文字と被らないようにシフトした**NEC内部コード(J)**
  - NEC内部コード(J)の上1バイト、下1バイトをそれぞれ[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")に変換して得られる**NEC内部コード(E)**

の4つのバリエーションがある。

  - JIPS(J)は『[ACOS-6](../Page/ACOS-6.md "wikilink")』
  - JIPS(E)は『[ACOS-2](../Page/ACOS-2.md "wikilink")』、『[ACOS-4](../Page/ACOS-4.md "wikilink")』
  - NEC内部コード(E)は『[ITOS](https://ja.wikipedia.org/wiki/ITOS "wikilink")』、『[A-VX](https://ja.wikipedia.org/wiki/A-VX "wikilink")』等のオフコン

でそれぞれ用いられる。

なお、NEC内部コード(J)を使用していた業務用マシンとして、『[NTOS](https://ja.wikipedia.org/wiki/NTOS "wikilink")』および『[PTOS](https://ja.wikipedia.org/wiki/PTOS "wikilink")』がかつて存在した。

## JIPSの外字

1面(G0)84〜94区と2面(G1)64区〜94区に1,034+2,914=3,948文字をユーザ外字領域として利用できる。これは[eucJP-MS](https://ja.wikipedia.org/wiki/eucJP-MS "wikilink")が、1面(G1)84〜94区と2面(G3)84〜94区に合計2,068文字のユーザ外字領域を持っていることと似ている。

ただし、JIPSの1面(GO)はGL表現であり、eucJP-MSの1面(G1)はGR表現である。そして、JIPSの2面(G1)はG0からシフト符号無しで面切り替え出来るのに対し、eucJP-MSの2面(G3)はG1からシングルシフトで切り替える点が違う。

## 脚注

## 関連項目

  - [文字コード](../Page/文字コード.md "wikilink")
  - [Microsoftコードページ932](../Page/Microsoftコードページ932.md "wikilink")
  - [EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")
  - [IBM漢字システム](../Page/IBM漢字システム.md "wikilink")
  - [JEF漢字コード](https://ja.wikipedia.org/wiki/JEF漢字コード "wikilink")
  - [KEIS](https://ja.wikipedia.org/wiki/KEIS "wikilink")

## 外部リンク

[Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink")