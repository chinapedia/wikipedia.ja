> この記事は[Extended Unix Code](https://ja.wikipedia.org/wiki/Extended_Unix_Code)から翻訳されています。


**Extended Unix Code**(EUC)は、[UNIX](../Page/UNIX.md "wikilink")上で使われてきた[文字コード](../Page/文字コード.md "wikilink")の[符号化方式である](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")。

  - [日本語](../Page/日本語.md "wikilink")EUC
      - [JIS X 0208ベース](../Page/JIS_X_0208.md "wikilink") ([EUC-JP](../Page/EUC-JP.md "wikilink"))
      - [JIS X 0213ベース](../Page/JIS_X_0213.md "wikilink") ([EUC-JIS-2004](../Page/EUC-JIS-2004.md "wikilink"))
  - [韓国語EUC](../Page/朝鮮語.md "wikilink") ([EUC-KR](https://ja.wikipedia.org/wiki/EUC-KR "wikilink"))
  - [簡体字](https://ja.wikipedia.org/wiki/簡体字 "wikilink")[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")EUC ([EUC-CN](https://ja.wikipedia.org/wiki/EUC-CN "wikilink"))
  - [繁体字](../Page/繁体字.md "wikilink")中国語EUC ([EUC-TW](https://ja.wikipedia.org/wiki/EUC-TW "wikilink"))

などがある。

## 概要

バイト単位の可変長コードであるEUC Packed Formatと、2バイト固定長のEUC Fixed Width Formatがある。前者は情報交換用、後者は内部処理用で、一般にEUCという場合前者を指す。ここでも前者について解説する。

[ISO/IEC 2022を基に](https://ja.wikipedia.org/wiki/ISO/IEC_2022 "wikilink")、以下のようなサブセット化を行った体系である。

  - G0に[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")（主コードセット）を、G1-G3に各言語の[文字集合](../Page/文字集合.md "wikilink")（補助コードセット1-3）を暗黙に指示する。指示のエスケープシーケンスは用いない。
  - GLにG0を、GRにG1を暗黙に呼び出す。G2/G3はシングルシフト2/3によりGRに呼び出す。ロッキングシフトは用いない。

補助コードセットが0x80-0xFFの範囲で表されるため、主コードセットと衝突することがない。すなわち[Shift_JIS](../Page/Shift_JIS.md "wikilink")における[2バイト目が5C等になりうることによる問題が起きないというメリットがある](https://ja.wikipedia.org/wiki/Shift_JIS#2バイト目が5C等になりうることによる問題 "wikilink")。

具体的に局所化したそれぞれの版について、日本語では「 - 語EUC」や「 - 語版EUC」のように呼ばれることが多い。

## 日本語EUC

[日本国](https://ja.wikipedia.org/wiki/日本国 "wikilink")の規格を応用したEUCである。

### JIS X 0208ベース

一般に日本語EUCという場合こちらを指す。EUC-JPともいう。ここで、`JP`は日本国を表す国・地域コードであって、日本語を表す言語コード (`ja`) でない。

UNIXの標準的な日本語コードとして広く使われてきた。UNIX SYSTEM V リリース 4 日本語環境共通規約において、JIS X 201 カタカナとJIS X 212 補助漢字は実装が必須ではないとされていた。このため、特にJIS X 0212は実装されていないことも多い。通信などで用いる場合はこの点に注意が必要である。

  - G0 - ASCII
  - G1 - [JIS X 0208](../Page/JIS_X_0208.md "wikilink")
  - G2 - [JIS X 0201カタカナ](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")
  - G3 - [JIS X 0212補助漢字](../Page/JIS_X_0212.md "wikilink")

なお、G2とG3を使わない場合はJIS X 0208:1997の「国際基準版・漢字用8ビット符号」と同一となる。

### JIS X 0213ベース

JIS X 0213:2004ベースのものをEUC-JIS-2004という（2000年版はEUC-JISX0213）。JIS X 0213の附属書3に記載がある。フリー/オープンソースソフトウェアなどで使われていることがある。

  - G0 - ASCII
  - G1 - [JIS X 0213](../Page/JIS_X_0213.md "wikilink") 1面
  - G2 - [JIS X 0201カタカナ](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")
  - G3 - [JIS X 0213](../Page/JIS_X_0213.md "wikilink") 2面

## 韓国語EUC

[韓国で広く使われている](../Page/大韓民国.md "wikilink")。EUC-KRともいう。ここで、`KR`は韓国の国・地域コードであって、[朝鮮語](../Page/朝鮮語.md "wikilink")の言語コード (`ko`) ではない。単にKS C 5601といった場合でも、文字集合としてのKS C 5601でなく、EUC-KRのことを指している場合が多い。

  - G0 - ASCII
  - G1 - [KS X 1001](../Page/KS_X_1001.md "wikilink") (KS C 5601)
  - G2 - なし
  - G3 - なし

EUC-KRを拡張した**UHC** (Unified Hangul Code) という体系も存在する。

## 簡体字中国語EUC

[中国](../Page/中国.md "wikilink")で広く使われている。EUC-CNともいう。ここで、`CN`は中国の国・地域コードであって、簡体字の用字系コード (`Hans`) でも[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")の言語コード (`zh`) でもない。単にGB 2312といった場合でも、文字集合としてのGB 2312でなく、EUC-CNのことを指している場合が多い。

  - G0 - ASCII
  - G1 - [GB 2312](../Page/GB_2312.md "wikilink")
  - G2 - なし
  - G3 - なし

EUC-CNを拡張した[GBK](https://ja.wikipedia.org/wiki/GBK "wikilink")という体系も存在する。

## 繁体字中国語EUC

EUC-TWともいう。ここで、`TW`は[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")の国・地域コードであって、繁体字の用字系コード (`Hant`) でも中国語の言語コード (`zh`) でもない。台湾の規格であるが、あまり使われておらず、一般には[Big5](../Page/Big5.md "wikilink")が使われる。

  - G0 - ASCII
  - G1 - [CNS 11643](https://ja.wikipedia.org/wiki/CNS_11643 "wikilink") 第一字面
  - G2 - [CNS 11643](https://ja.wikipedia.org/wiki/CNS_11643 "wikilink") 第二-第十六字面
  - G3 - なし

G2の文字は以下の4バイトで構成される。

  - シングルシフト2 (0x8E)
  - 字面を選択するコード(0xA2-0xB0)
  - 文字の第1バイト(0xA1-0xFE)
  - 文字の第2バイト(0xA1-0xFE)

## 課題

EUCの利用は、すべての文字コードを包含したり、複数の文字コードを切り替えて表示する機能の必要性を否定する場合があり、多くの文字を表示する流れに対して後ろ向きであった点が課題である。これは、文字コード自体の課題ではなく、EUCを利用しているプログラマ、利用者の課題である。

## 関連項目

  - [ISO/IEC 2022](https://ja.wikipedia.org/wiki/ISO/IEC_2022 "wikilink")
  - [ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")
  - [ISO 3166](../Page/ISO_3166.md "wikilink")

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink")