> この記事は[RC6](https://ja.wikipedia.org/wiki/RC6)から翻訳されています。


**RC6** は [RC5](../Page/RC5.md "wikilink") から派生した[共通鍵を使用した](../Page/共通鍵暗号.md "wikilink")[ブロック暗号](../Page/ブロック暗号.md "wikilink")。[ロナルド・リベスト](../Page/ロナルド・リベスト.md "wikilink")、Matt Robshaw、Ray Sidney、Yiqun Lisa Yin が[AESの公募の要求仕様を満たすよう設計したものである](../Page/Advanced_Encryption_Standard.md "wikilink")。この暗号は最終選考の5作品に選ばれた。また、[NESSIE](../Page/NESSIE.md "wikilink") や [CRYPTREC](../Page/CRYPTREC.md "wikilink") プロジェクトにも送られた。[RSAセキュリティ](../Page/RSAセキュリティ.md "wikilink")が権利を所有している。

RC6 はブロック長 128ビット、キー長 128/192/256ビットとされているが、実際には RC5 のようにブロック長、キー長、ラウンド回数がパラメータ化されており、任意の値に設定可能である。RC6 の構造は RC5 とよく似ており、データ依存の回転、[合同加算](https://ja.wikipedia.org/wiki/合同式 "wikilink")、[XORなど共通の特徴がある](../Page/排他的論理和.md "wikilink")。実際、RC6 は RC5 の暗号化プロセスを2つ並列に並べて処理するものと言える。しかし、RC6 では RC5 にはない乗算処理が追加で使われており、回転(rotation)をワード内の各ビット毎に依存させるようになっている（一部のビットだけではない）。

## 参考文献

  - R.L. Rivest, M.J.B. Robshaw, R.Sidney, and Y.L. Yin. [The RC6 Block Cipher](http://theory.lcs.mit.edu/~rivest/rc6.pdf). v1.1, August 1998.
  - J. Beauchat [FPGA Implementations of the RC6 Block Cipher](http://perso.ens-lyon.fr/jean-luc.beuchat/Publications/fpl2003.pdf).

## 外部リンク

  - [リファレンスコード](http://embeddedsw.net/Cipher_Reference_Home.html)
  - [SCAN's entry on RC6](http://www.users.zetnet.co.uk/hopwood/crypto/scan/cs.html#RC6)
  - [RSA Security's RC6 page](http://www.rsasecurity.com/rsalabs/node.asp?id=2512)