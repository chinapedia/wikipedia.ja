> この記事は[Synchronous Digital Hierarchy](https://ja.wikipedia.org/wiki/Synchronous_Digital_Hierarchy)から翻訳されています。


**同期デジタル・ハイアラーキ**（[英語](../Page/英語.md "wikilink")：synchronous digital hierarchy、略称：**SDH**）は、地域によって異なっていた[プレシオクロナス・デジタル・ハイアラーキ](../Page/Plesiochronous_Digital_Hierarchy.md "wikilink")（plesiochronous digital hierarchy、PDH）を世界的に統一する目的で、[1988年](../Page/1988年.md "wikilink")に[ITU-T](../Page/ITU-T.md "wikilink")が制定\[1\]した。[同期網の構成である](../Page/同期方式.md "wikilink")。Bellcore社によって提案され[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")（米国規格協会）で規格化された[SONET](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink")（Synchronous Optical NETwork）を元にしているため、SONET/SDHとも表記される。SONETとSDHは、伝送速度系列が違うなどいくつかの相違点がある。

## 特徴

[多重化](../Page/多重化.md "wikilink")は、ブロックフレームの周期を125μsに一定にして、内部の利用者データーの[ペイロードの入れ物であるバーチャルコンテナ](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")（VC : Virtual Container）の数を増やすことによって行われる。また、フレームには、バーチャルコンテナの他に網管理のためのセクションオーバーヘッド（SOH）、[周波数](../Page/周波数.md "wikilink")・[位相](../Page/位相.md "wikilink")同期のための管理ポインタ（AUPTR）、各パスを識別するためのパスオーバーヘッド（POH）が付加される。

このようにして、次のような機能を実現している。

  - 利用者データーから独立した網管理情報を持つため、信頼性の高い通信が可能である。
  - 管理ポインタを利用して周波数・位相の同期をとるため、交換機間のずれの補正が容易でより高速な通信に対応できる。
  - 管理ポインタ・パスオーバーヘッドを利用して、低速なチャネルから高速なハイアラーキへの多重化や、高速なハイアラーキから直に各チャネルの情報を取り出すことが可能である。

## 伝送速度系列

| 名称      | 伝送速度 M[bps](../Page/ビット毎秒.md "wikilink") | ペイロード Mbps |
| ------- | ---------------------------------------- | ---------- |
| SDH     | SONET                                    |            |
| STM-0   | OC-1                                     | 51.84      |
| STM-1   | OC-3                                     | 155.52     |
| STM-4   | OC-12                                    | 622.08     |
| STM-16  | OC-48                                    | 2488.32    |
| STM-64  | OC-192                                   | 9953.28    |
| STM-256 | OC-768                                   | 39813.12   |

## 脚注

## 関連項目

  - [SONET](https://ja.wikipedia.org/wiki/SONET "wikilink")
  - [Plesiochronous Digital Hierarchy](../Page/Plesiochronous_Digital_Hierarchy.md "wikilink")

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:光有線通信](https://ja.wikipedia.org/wiki/Category:光有線通信 "wikilink")

1.  ITU G.783 : Characteristics of synchronous digital hierarchy (SDH) equipment functional blocks <https://www.itu.int/rec/T-REC-G.783>