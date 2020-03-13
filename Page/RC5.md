> この記事は[RC5](https://ja.wikipedia.org/wiki/RC5)から翻訳されています。


**RC5** はその単純さが特徴の[ブロック暗号](../Page/ブロック暗号.md "wikilink")の一種。[1994年](../Page/1994年.md "wikilink")、[ロナルド・リベスト](../Page/ロナルド・リベスト.md "wikilink")が設計した。*RC* は "Rivest Cipher" または "Ron's Code" の略（[RC2](../Page/RC2.md "wikilink")、[RC4](../Page/RC4.md "wikilink")参照）。[AESの候補となった](../Page/Advanced_Encryption_Standard.md "wikilink")[RC6](../Page/RC6.md "wikilink")はRC5をベースとしている。

## 概要

RC5は、ラウンド関数で使用する演算に関する研究と評価を促進することを目的として設計された、非常にシンプルな構造をしたブロック暗号である。

RC5 は、データ依存の回転(data-dependent rotation)という目新しい演算を採用したことと、アルゴリズムの単純さによって[暗号解読者](https://ja.wikipedia.org/wiki/暗号解読者 "wikilink")らにとって魅力的な研究対象となった。データによってローテーション数が変化することは最大差分(線形)確率の上界の評価が複雑になることを意味する。

## 構造

[right](https://ja.wikipedia.org/wiki/ファイル:RC5_InfoBox_Diagram.png "wikilink") 他のブロック暗号と異なり、RC5 のブロック長は 32、64、128ビットの3つ、キー長は任意（0 から 2040ビット）、ラウンド回数も任意（0 から 255）である。本来のパラメータ推奨値は、ブロック長 64ビット、キー長 128ビット、12 ラウンドである。

アルゴリズムの基本構造は Feistel 風のネットワークである。最初に拡大鍵でWhiteningした後、ラウンド関数を指定回数繰り返す。暗号化ルーチンと復号ルーチンのコードはほんの数行であるが、鍵のスケジュールはもっと複雑である。

ラウンド関数は、[XOR（排他的論理和）](../Page/排他的論理和.md "wikilink")、RC5の特徴となっているデータ依存の回転(rotation)、そして、拡大鍵との[剰余加算の](https://ja.wikipedia.org/wiki/合同式 "wikilink")3つの組み合わせで構成される。

## 安全性

12ラウンドの RC5（ブロック長 64ビット）は 2<sup>44</sup> 個の選択平文を使った[差分攻撃で破られることが示された](../Page/差分解読法.md "wikilink")\[1\]。18 から 20 ラウンドでは解読できないと言われている。

このアルゴリズムの特許を保有する[RSAセキュリティ](../Page/RSAセキュリティ.md "wikilink")は RC5 で作成した[暗号文](../Page/暗号文.md "wikilink")を解読できた者に 1万ドルを提供する暗号解読コンテストをいくつか発表している。この暗号解読コンテストのうち56ビットと64ビットの鍵の暗号については、[distributed.net](https://ja.wikipedia.org/wiki/distributed.net "wikilink")が組織した[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")によって解読された。なお、その後の状況の変化により、2007年9月、RSAセキュリティは暗号解読コンテストの中止を発表した（distributed.netでは 引き続き72ビットの鍵の暗号解読を継続している）。

## 脚注

<references/>

## 参考文献

  - Biryukov A. and Kushilevitz E. (1998). Improved Cryptanalysis of RC5. EUROCRYPT 1998.
  - Rivest, R. L. (1998). Block Encryption Algorithm with Data Dependent Rotation. Patent No. 5,724,428 issued 3rd March 1998.
  - Rivest, R. L. (1994). The RC5 Encryption Algorithm. In the *Proceedings of the Second International Workshop on Fast Software Encryption (FSE) 1994*, p86–96 [(PDF)](http://theory.lcs.mit.edu/~rivest/Rivest-rc5rev.pdf).
  - Rivest, R. L, "Block Encryption Algorithm With Data Dependent Rotation", US patent \#5,724,428, issued on 3 March 1998.

## 関連項目

  - [RC6](../Page/RC6.md "wikilink") / [ブロック暗号](../Page/ブロック暗号.md "wikilink") / [暗号](../Page/暗号.md "wikilink")
  - [Madryga](https://ja.wikipedia.org/wiki/Madryga "wikilink")
  - [Red Pike](https://ja.wikipedia.org/wiki/Red_Pike "wikilink")

## 外部リンク

  - [SCAN's entry for the cipher](http://www.users.zetnet.co.uk/hopwood/crypto/scan/cs.html#RC5)
  - [RSA Laboratories FAQ — What are RC5 and RC6?](http://www.rsasecurity.com/rsalabs/node.asp?id=2251)
  - [Helger Lipmaa's links on RC5](http://www.cs.ut.ee/~helger/crypto/link/block/rc5.php)
  - [RSA's patent via Google.](http://www.google.com/search?q=Patent+5724428)

<!-- end list -->

1.  Biryukov A. and Kushilevitz E. (1998). Improved Cryptanalysis of RC5. EUROCRYPT 1998.