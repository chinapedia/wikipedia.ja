> この記事は[S](https://ja.wikipedia.org/wiki/S)から翻訳されています。


暗号技術において、**Sボックス** (**substitution box** or **S-box**) とは、[共通鍵暗号](https://ja.wikipedia.org/wiki/共通鍵暗号 "wikilink")の基本部品の一つである関数のことである。典型的には[ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")で、[平文](https://ja.wikipedia.org/wiki/平文 "wikilink")と[暗号文](https://ja.wikipedia.org/wiki/暗号文 "wikilink")の相関（線形性）を壊すための仕組みとして使用され、[暗号解読](https://ja.wikipedia.org/wiki/暗号解読 "wikilink")に耐性を有するように注意深く選択する必要がある部品である。

## 概要

S-boxは、m ビットの入力を n ビット出力に変換する関数であり、2<sup>m</sup> の[ルックアップテーブル](https://ja.wikipedia.org/wiki/ルックアップテーブル "wikilink")によって実装できる。

通常は、[DESのように固定テーブルとして定義されるが](../Page/Data_Encryption_Standard.md "wikilink")、暗号によっては[鍵によってテーブルを動的に生成して使用するものもある](https://ja.wikipedia.org/wiki/鍵_\(暗号\) "wikilink")。動的に生成する例として、[Blowfishや](https://ja.wikipedia.org/wiki/Blowfish_\(暗号\) "wikilink")[Twofish](https://ja.wikipedia.org/wiki/Twofish "wikilink") がある。

1970年代に設計されたDESでは6ビット入力 4ビット出力の S-box を8種類使用しているが、2000年代に設計された[AESや](../Page/Advanced_Encryption_Standard.md "wikilink")[Camellia](https://ja.wikipedia.org/wiki/Camellia "wikilink")では8ビット入出力のS-boxを1種類使用している（Camelliaでは4種の S-box を持つが、三つのS-boxは一つのS-boxの単純な変換となっている）。これはソフトウェアやハードウェアでの実装時に、スピード優先だけではなく、サイズ縮小を優先させた実装も考慮したためである。

S-boxの設計は、[DES作成時にはIBM大型コンピュータを何ヶ月か使ったほど設計は難しい](../Page/Data_Encryption_Standard.md "wikilink")、と言われている。Lucifer暗号はSボックスがとても弱いため、40個の選択平文で破れた。DESは設計時に差分解読法への耐性を持つことを設計方針にしていたことが後に公開された。

1990年代前半に[差分解読法](https://ja.wikipedia.org/wiki/差分解読法 "wikilink")・[線形解読法](https://ja.wikipedia.org/wiki/線形解読法 "wikilink")が見つかり、これらの解読法に耐性を持つことが安全なS-boxの必要条件と認識された。（証明されていないが）nビット入出力のS-boxの場合、2の拡大体 GF(2<sup>m</sup>)での逆変換が差分・線形解読に対して最も強いテーブルと考えられている。このとき、差分確率及び線形確率は、 n が奇数の場合 2<sup>-n+1</sup> 、偶数の場合 2<sup>-n+2</sup> となる。AESやCamelliaではそれを線形変換したものが採用されており、差分確率及び線形確率は、 2<sup>-6</sup> である。

近年では、実装サイズの縮小を目的に小さいS-Boxを複数組み合わせて大きなS-Boxを構成する方法がとられることがある。この場合上記のような最善の最大差分(あるいは線形)確率を持たないが、暗号全体で十分な最大特性差分(あるいは線形)確率を持つように設計される。

## DESのS-box

具体例としてDESの 6ビット入力 4ビット出力の S-box の一つ S<sub>5</sub> を示す:

| S<sub>5</sub> | 入力の中間4ビット |
| ------------- | --------- |
| 0000          | 0001      |
| MSBLSB        | 00        |
| 01            | 1110      |
| 10            | 0100      |
| 11            | 1011      |

入力6ビットを中間の4ビットと、MSB,LSBの2ビットに分けて、行・列を選択して、出力4ビットを得る。 例えば、入力 "**0**1101**1**" のとき、MSB,LSBは "**01**" で、中間の4ビットは "1101" である。そして出力として選択される4ビットは "1001" となる。

DESは、規格作成時に8個あるS-boxの設計方針が公開されなかったため、設計者だけが知っているバックドアが仕組まれているのではないかという点について多年に渡る研究がなされた。そして、差分解読法が(再)発見され、線形解読法によるDESの解読実験が成功した1994年になってS-boxの設計方針について公開された。それによるとS-boxは差分解読について耐性を有するように注意深く設計されていたが、線形解読法に対しては考慮されていなかった。

## 参考文献

  - Coppersmith, Don. (1994). The data encryption standard (DES) and its strength against attacks. *IBM Journal of Research and Development*, **38**(3), 243–250. [1](http://www.research.ibm.com/journal/rd/383/coppersmith.pdf)
  - S. Mister and C. Adams, "Practical S-Box Design," Workshop on Selected Areas in Cryptography (SAC '96) Workshop Record, Queens University, 1996, pp. 61–76
  - B.SCHNEIER "Applied Cryptography" p.296-298

## 関連項目

  - [ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")
  - [ブール関数](https://ja.wikipedia.org/wiki/ブール関数 "wikilink")

## 外部リンク

  - [A literature survey on S-box design](http://www.ciphersbyritter.com/RES/SBOXDESN.HTM)
  - [John Savard's "Questions of S-Box Design"](http://www.quadibloc.com/crypto/co4513.htm)
  - [Practical S-Box Design](http://adonis.ee.queensu.ca:80/sac/sac96/papers.html) by S. Mister and C. Adams (PDF)

[Category:暗号技術](https://ja.wikipedia.org/wiki/Category:暗号技術 "wikilink")