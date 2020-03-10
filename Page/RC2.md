> この記事は[RC2](https://ja.wikipedia.org/wiki/RC2)から翻訳されています。


**RC2** は[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に[ロナルド・リベスト](../Page/ロナルド・リベスト.md "wikilink")が設計した[ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")。"RC" は "Ron's Code" または "Rivest Cipher" の略。リベストの設計した他の暗号として [RC4](../Page/RC4.md "wikilink")、[RC5](https://ja.wikipedia.org/wiki/RC5 "wikilink")、[RC6](https://ja.wikipedia.org/wiki/RC6 "wikilink") がある。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:RC2_InfoBox_Diagram.png "wikilink") RC2 の開発資金は、[Lotus Notesソフトウェアの一部として輸出可能な独自の](https://ja.wikipedia.org/wiki/Lotus_Notes "wikilink")[暗号](../Page/暗号.md "wikilink")を探していた[ロータス社が資金提供した](../Page/ロータス_\(ソフトウェア\).md "wikilink")（輸出以前に[NSAの評価が必要だった](../Page/アメリカ国家安全保障局.md "wikilink")）。NSA はいくつかの修正を示唆し、リベストはそれを取り入れた。さらなる交渉の末、この暗号は[1989年](../Page/1989年.md "wikilink")に輸出が許可された。RC4と同様 40ビットのキーを持つ RC2 は[アメリカ合衆国の暗号輸出規制の中では重宝された](https://ja.wikipedia.org/wiki/アメリカ合衆国からの暗号の輸出規制 "wikilink")。

当初、アルゴリズムの詳細は秘密とされたが（[RSAセキュリティ](../Page/RSAセキュリティ.md "wikilink")が権利を保有）、[1996年](../Page/1996年.md "wikilink")1月29日、RC2 のソースコードが匿名で[ネットニュース](../Page/ネットニュース.md "wikilink")の sci.crypt にポストされてしまった。似たような機密開示は RC4 で既に発生していた。ポストした者が仕様にアクセスする権限を持っていたのか、[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")でソースを作成したのかは不明である。

RC2 は 64 ビットブロック暗号で任意長の[鍵が可能である](../Page/鍵_\(暗号\).md "wikilink")。18ラウンドの変形[Feistel構造](../Page/Feistel構造.md "wikilink")で、うち 16 ラウンドが1つのタイプ(*MIXING*)、2ラウンドがもう1つのタイプ(*MASHING*)である。MIXING ラウンドは 4 種類のMIX変換から構成される。

RC2 は 2<sup>34</sup> 個の[選択平文を使った](https://ja.wikipedia.org/wiki/選択平文攻撃 "wikilink")[関連鍵攻撃](https://ja.wikipedia.org/wiki/関連鍵攻撃 "wikilink")に対して無防備である（Kelsey 他、1997年）。

## 参考文献

  - Steven Levy, Crypto: How the Code Rebels Beat the Government — Saving Privacy in the Digital Age, ISBN 0-14-024432-8, 2001.
  - Lars R. Knudsen, Vincent Rijmen, Ronald L. Rivest, Matthew J. B. Robshaw: On the Design and Security of RC2. Fast Software Encryption 1998: 206–221
  - John Kelsey, Bruce Schneier, David Wagner: Related-key cryptanalysis of 3-WAY, Biham-DES, CAST, DES-X, NewDES, RC2, and TEA. ICICS 1997: 233–246

## 外部リンク

  - RFC 2268: A Description of the RC2(r) Encryption Algorithm
  - [RSA FAQ: What is RC2?](http://www.rsasecurity.com/rsalabs/node.asp?id=2249)
  - [sci.crypt posting revealing the RC2 algorithm](http://groups.google.com/groups?selm=4ehmfs%246nq%40utopia.hacktic.nl)

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")