> この記事は[FEAL](https://ja.wikipedia.org/wiki/FEAL)から翻訳されています。


**FEAL**（the **Fast Data Encipherment Algorithm**）とは、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に、[NTTにいた清水明宏と宮口庄司が提案した](https://ja.wikipedia.org/wiki/日本電信電話 "wikilink")64bit[ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")である。[DES](../Page/Data_Encryption_Standard.md "wikilink")（Data Encryption Standard）の代替品となることを目的として開発された。

## 概要

FEALは、DESと同じく[Feistel構造](../Page/Feistel構造.md "wikilink")を採用したブロック長64ビットのブロック暗号である。

1987年当初は、FEAL-4 としてラウンド数4、鍵長64ビットで、その後、1988年にFEAL-8（ラウンド数 8）を経て、1990年にFEAL-N（Nは可変、32以上が望ましい)と鍵長を128ビットに拡張した FEAL-NX に改定された。

ソフトウェアで効率的に実装できるようにビット単位の転置やテーブル参照による[Sボックス](../Page/Sボックス.md "wikilink")は採用せずに、あみだ構造のラウンド関数と、8ビット単位の算術演算やシフト演算等、CPUで容易に実装可能な演算のみを使用している点に特徴がある。その結果、FEAL-8は8ビットCPUでのソフトウェア実装時の処理速度がDESよりも高い。

あみだ構造のラウンド関数は、設計者たちの評価によれば、DESのラウンド関数よりもデータ攪拌効果が高く、安全であると主張されていた。しかし、このアルゴリズムは発表直後から様々な[暗号解読](https://ja.wikipedia.org/wiki/暗号解読 "wikilink")を試みられ、暗号学者たちが[差分解読法](../Page/差分解読法.md "wikilink")や[線形解読法](../Page/線形解読法.md "wikilink")を発見するきっかけとなった。

1994年に、ISO/IEC9979にもとづく暗号アルゴリズム登録制度に登録されている（登録番号10）。

## 構造

FEAL のブロック長は64ビットで、Feistel構造を採用し、FEAL-4はラウンド段数４、FEAL-8はラウンド段数８、そしてFEAL-N/NXはラウンド段数は可変である(Nは32以上)。

鍵長は、FEAL-Nは64ビット、FEAL-NXは128ビットである。FEAL-NXで鍵128ビットうち、右64ビットをすべて0とした場合、FEAL-Nと等価になる。

最初と最後に拡大鍵との排他的論理和（XOR、whitening と呼ばれる処理）と、左32ビットと右32ビットをXORし、右32ビットを更新する処理が設けられている。

[thumb](https://ja.wikipedia.org/wiki/ファイル:FEAL_InfoBox_Diagram.png "wikilink") FEALのラウンド関数は、拡大鍵16ビットを用いて、32ビットの入力を[スクランブル](https://ja.wikipedia.org/wiki/スクランブル "wikilink")して32ビットを出力する。ラウンド関数の内部を右図に示す。入力32ビットを8ビット単位にわけ、8ビット単位で隣の8ビットを用いてXORやS関数による変換を順番に行う構造になっている。この構造を開発者は「[阿弥陀籤](https://ja.wikipedia.org/wiki/阿弥陀籤 "wikilink")」からヒントを得たと述べており、"あみだ構造" と呼ばれることもある。

S関数は、8ビットCPUで容易に実装可能なように、法256での加算とビットシフトからなり、DESのようにテーブル参照をしなくてすむ分、コードサイズを小さく出来る。

鍵スケジューラでは、メインのデータスクランブルで使用されるラウンド関数を少し変形した関数を用いて、またFeistel構造とは異なる構造で、鍵64ビットを更新し、中間データを拡大鍵として出力する。

## 性能

FEAL-32Xは、Z80(5MHz)で6169ステート(51.8kbps）で実行できる。 PentiumIII(650MHz)では、117.8Mbps。

## 安全性

FEAL-4は、[線形解読法](../Page/線形解読法.md "wikilink")により、5つの[既知平文](https://ja.wikipedia.org/wiki/既知平文 "wikilink")で解読可能 (Matsui and Yamagishi, 1992)。

FEAL-NXは、[差分解読法](../Page/差分解読法.md "wikilink")により、31ラウンドまで解読可能 (Biham and Shamir, 1991)。線形解読法では、25ラウンドまで解読可能。これはFEAL-32Xは2^{99}の計算量で解読可能であることを意味する。また、[CRYPTREC](../Page/CRYPTREC.md "wikilink")の報告書では、FEAL-32X は学術的に解読可能であり、長期の使用を考えた場合、推薦できない。とされている．

## 参考文献

  - Eli Biham, Adi Shamir: Differential Cryptanalysis of Feal and N-Hash. EUROCRYPT 1991: 1–16
  - Bert den Boer, Cryptanalysis of F.E.A.L., EUROCRYPT 1988: 293–299
  - Henri Gilbert, Guy Chassé: A Statistical Attack of the FEAL-8 Cryptosystem. CRYPTO 1990: 22–33.
  - Shoji Miyaguchi: The FEAL Cipher Family. CRYPTO 1990: 627–638
  - Shoji Miyaguchi: The FEAL-8 Cryptosystem and a Call for Attack. CRYPTO 1989: 624–627
  - Mitsuru Matsui, Atsuhiro Yamagishi: A New Method for Known Plaintext Attack of FEAL Cipher. EUROCRYPT 1992: 81–91
  - Sean Murphy, The Cryptanalysis of FEAL-4 with 20 Chosen Plaintexts. *J. Cryptology* **2**(3): 145–154 (1990)
  - A. Shimizu and S. Miyaguchi, Fast data encipherment algorithm FEAL, Advances in Cryptology — Eurocrypt '87, Springer-Verlag (1988), 267–280.
  - Anne Tardy-Corfdir, Henri Gilbert: A Known Plaintext Attack of FEAL-4 and FEAL-6. CRYPTO 1991: 172–181
  - 清水明宏, 宮口庄司：高速データ暗号アルゴリズムFEAL. 電子情報通信学会論文誌, Vol. J70-D, No. 7, pp. 1413-1423, July 1987.

## 関連項目

  - [ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")
  - [共通鍵暗号](../Page/共通鍵暗号.md "wikilink")
  - [Feistel構造](../Page/Feistel構造.md "wikilink")
  - [Camellia](../Page/Camellia.md "wikilink")
  - [信頼性の低い暗号アルゴリズム](../Page/信頼性の低い暗号アルゴリズム.md "wikilink")

## 外部リンク

  - [The FEAL home page](http://info.isl.ntt.co.jp/feal-nx/)
  - [A sci.crypt article by Peter Gutmann describing FEAL](http://groups.google.com/groups?selm=54gq4q%242d7%40scream.auckland.ac.nz)
  - [US patent 4850019](http://patft.uspto.gov/netacgi/nph-Parser?TERM1=4850019&u=/netahtml/srchnum.htm&Sect1=PTO1&Sect2=HITOFF&p=1&r=0&l=50&f=S&d=PALL)