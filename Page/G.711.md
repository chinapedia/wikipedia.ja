> この記事は[G.711](https://ja.wikipedia.org/wiki/G.711)から翻訳されています。


**G.711**はCCITT（現在の[ITU-T](../Page/ITU-T.md "wikilink")）によって策定された[音声符号化](https://ja.wikipedia.org/wiki/音声符号化 "wikilink")の規格で、[1972年](../Page/1972年.md "wikilink")に制定された。符号化方式は非線形[パルス符号変調](../Page/パルス符号変調.md "wikilink")であり、[標本化周波数は](../Page/サンプリング周波数.md "wikilink")8000Hzである。固定電話網内の音声信号の伝送などに広く用いられている。

## 圧伸特性

信号レベルが小さいときに量子化雑音を低減するため（i.e. 音量が小さいときのノイズを少なくするため）、非直線量子化が行われる。圧伸特性として、**[μ-law](https://ja.wikipedia.org/wiki/μ-lawアルゴリズム "wikilink")**（北米・日本で使用）および**[A-law](https://ja.wikipedia.org/wiki/A-lawアルゴリズム "wikilink")**（欧州その他で使用）の二つが規定されているが、そのうち後者はコンピュータによる処理の容易性を特に考慮している。また、音声レベル0dBを定義するための符号化サンプルも規格に含まれている。

**[μ-law](https://ja.wikipedia.org/wiki/μ-lawアルゴリズム "wikilink")**は、14ビット符号付き線形PCMの1標本を対数的に8ビットに符号化する。**[A-law](https://ja.wikipedia.org/wiki/A-lawアルゴリズム "wikilink")**では13ビット符号付き線形PCMの1標本を対数的に8ビットに符号化する。標本化周波数が8000Hzなので、符号化器の出力ビットレートは64kbpsとなる。

## A-law

**[A-law](https://ja.wikipedia.org/wiki/A-lawアルゴリズム "wikilink")**符号化器の入力・出力対照表は以下の通り。

|                  |          |
| ---------------- | -------- |
| **線形の入力値**       | **出力値**  |
| s0000000wxyza... | s000wxyz |
| s0000001wxyza... | s001wxyz |
| s000001wxyzab... | s010wxyz |
| s00001wxyzabc... | s011wxyz |
| s0001wxyzabcd... | s100wxyz |
| s001wxyzabcde... | s101wxyz |
| s01wxyzabcdef... | s110wxyz |
| s1wxyzabcdefg... | s111wxyz |

*s*は符号部。例をあげると、入力値1000000010101111は表の1行目に従い10001010に変換され、0000000110101111は2行目に従い00011010に変換される。このように、A-lawの符号化後の値は仮数部4ビット・指数部3ビットの[浮動小数点数](../Page/浮動小数点数.md "wikilink")とみなすことができる。

## 特徴

  - 標本化周波数 - 8kHz
  - ビットレート - 64kbps（標本化周波数8kHz × 8ビット符号）
  - アルゴリズムによる遅延は通常0.125ms。先読み遅延はない。

## 関連項目

  - [コンパンディング](https://ja.wikipedia.org/wiki/コンパンディング "wikilink")
  - [音声符号化](https://ja.wikipedia.org/wiki/音声符号化 "wikilink")

## 外部リンク

  - \[<http://www.itu.int/rec/dologin_pub.asp?lang=e&id=T-REC-G.711-198811-I>\!\!PDF-E\&type=items ITU-T Recommendation G.711\] - (STD.ITU-T RECMN G.711-ENGL 1989)
  - [G.711 codec process](http://www.en.voipforo.com/codec/codecs-g711-alaw.php)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink")