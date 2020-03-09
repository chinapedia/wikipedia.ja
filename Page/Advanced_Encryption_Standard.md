> この記事は[Advanced Encryption Standard](https://ja.wikipedia.org/wiki/Advanced_Encryption_Standard)から翻訳されています。


**Advanced Encryption Standard** (**AES**) は、[DESに代わる新しい標準暗号となる](https://ja.wikipedia.org/wiki/Data_Encryption_Standard "wikilink")[共通鍵暗号](https://ja.wikipedia.org/wiki/共通鍵暗号 "wikilink")アルゴリズムである。[アメリカ国立標準技術研究所](https://ja.wikipedia.org/wiki/アメリカ国立標準技術研究所 "wikilink")（NIST）の主導により公募され、Rijndael（ラインダール）がAESとして採用された\[1\]。

## 概要

以前の標準暗号であった「[DES](https://ja.wikipedia.org/wiki/Data_Encryption_Standard "wikilink")」は、

  - 時代の経過による相対的な強度の低下
  - [NSAの関与がある](../Page/アメリカ国家安全保障局.md "wikilink")**その設計の不透明性**（詳細は[DESの記事を参照](https://ja.wikipedia.org/wiki/Data_Encryption_Standard "wikilink")）

が問題であることから、新しい標準暗号として[アメリカ国立標準技術研究所](https://ja.wikipedia.org/wiki/アメリカ国立標準技術研究所 "wikilink")（NIST）の主導により公募され、AESが選出された。2001年3月に **FIPS PUB 197** として公表された。

厳密には「AES」は、選出された以外の暗号も含む、手続き中から使われた「新しい標準暗号」の総称であり、選出された暗号方式自体の名としてはRijndael（ラインダール）である。

AESは[SPN構造](https://ja.wikipedia.org/wiki/SPN構造 "wikilink")の[ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")で、ブロック長は128[ビット](../Page/ビット.md "wikilink")、鍵長は128ビット・192ビット・256ビットの3つが利用できる。AESの元となった **Rijndael** では、ブロック長と鍵長が可変で、128ビットから256ビットまでの32ビットの倍数が選べる。NISTが公募した際のスペックに従い、米国標準となったAESではブロック長は128ビットに固定、鍵長も3種類に限られた。\[2\]。

## 経緯

### AESの選定

旧規格 DES ([FIPS](https://ja.wikipedia.org/wiki/FIPS "wikilink") 46) の安全性が低下したため、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")9月にNIST（[アメリカ国立標準技術研究所](https://ja.wikipedia.org/wiki/アメリカ国立標準技術研究所 "wikilink")）が後継の暗号標準AES (Advanced Encryption Standard) とすべく共通鍵ブロック暗号を公募した。公募要件には下記のような条件が挙げられた\[3\]。

  - 米国に限らず世界中で、制限なく無料で利用できなければならないこと。
  - 詳細なアルゴリズム仕様を公開すること。
  - [ANSI C及び](https://ja.wikipedia.org/wiki/ANSI_C "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")による実装を行うこと。
  - 暗号強度評価を公開すること。

### AESの最終候補

世界から応募された21方式から、公募要件を満たした15方式に対する評価が行われ、安全性と実装性能に優れた5方式が最終候補として残った。最終候補および設計者は以下の通りである\[4\]。

  - [Rijndael](https://ja.wikipedia.org/wiki/Rijndael "wikilink") - 、[フィンセント・ライメン](https://ja.wikipedia.org/wiki/フィンセント・ライメン "wikilink")

  - [Serpent](https://ja.wikipedia.org/wiki/Serpent_\(暗号\) "wikilink")（サーペント、または、サーパン）- 、[エリ・ビーハム](https://ja.wikipedia.org/wiki/エリ・ビーハム "wikilink")、[ラーズ・ヌードセン](https://ja.wikipedia.org/wiki/ラーズ・ヌードセン "wikilink")

  - [RC6](https://ja.wikipedia.org/wiki/RC6 "wikilink") - [ロナルド・リヴェスト](https://ja.wikipedia.org/wiki/ロナルド・リヴェスト "wikilink")、[マット・ロブショー](https://ja.wikipedia.org/wiki/マット・ロブショー "wikilink")、[レイ・シドニー](https://ja.wikipedia.org/wiki/レイ・シドニー "wikilink")、[イーチュン・リサ・イン](https://ja.wikipedia.org/wiki/イーチュン・リサ・イン "wikilink")

  - [Twofish](https://ja.wikipedia.org/wiki/Twofish "wikilink") - [ブルース・シュナイアー](https://ja.wikipedia.org/wiki/ブルース・シュナイアー "wikilink")、[ジョン・ケルシー](https://ja.wikipedia.org/wiki/ジョン・ケルシー "wikilink")、[ダグ・ホワイティング](https://ja.wikipedia.org/wiki/ダグ・ホワイティング "wikilink")、[デーヴィッド・ワグナー](https://ja.wikipedia.org/wiki/デーヴィッド・ワグナー "wikilink")、[クリス・ホール](https://ja.wikipedia.org/wiki/クリス・ホール "wikilink")、[ニールス・ファーガソン](https://ja.wikipedia.org/wiki/ニールス・ファーガソン "wikilink")

  - \- [カロリン・バーウィック](https://ja.wikipedia.org/wiki/カロリン・バーウィック "wikilink")、[ドン・カッパースミス](https://ja.wikipedia.org/wiki/ドン・カッパースミス "wikilink")、[エドワード・ダヴィニョン](https://ja.wikipedia.org/wiki/エドワード・ダヴィニョン "wikilink")、[ロザリオ・ジェンナロ](https://ja.wikipedia.org/wiki/ロザリオ・ジェンナロ "wikilink")、[シャイ・ハレヴィ](https://ja.wikipedia.org/wiki/シャイ・ハレヴィ "wikilink")、[チャランジット・ジュトラ](https://ja.wikipedia.org/wiki/チャランジット・ジュトラ "wikilink")、[ステファン・マテリアス Jr.](https://ja.wikipedia.org/wiki/ステファン・マテリアス_Jr. "wikilink")、[ルーク・オコーナー](https://ja.wikipedia.org/wiki/ルーク・オコーナー "wikilink")、[モハンマド・ペイラヴィアン](https://ja.wikipedia.org/wiki/モハンマド・ペイラヴィアン "wikilink")、[デヴィド・サフォード](https://ja.wikipedia.org/wiki/デヴィド・サフォード "wikilink")、[ネヴェンコ・ズニコフ](https://ja.wikipedia.org/wiki/ネヴェンコ・ズニコフ "wikilink")

### AESの決定

最終選考の結果、あらゆる実装条件で優れた実装性能を発揮した[ベルギー](https://ja.wikipedia.org/wiki/ベルギー "wikilink")の[ルーヴェン・カトリック大学](https://ja.wikipedia.org/wiki/ルーヴェン・カトリック大学 "wikilink")の研究者 (Joan Daemen) と [フィンセント・ライメン](https://ja.wikipedia.org/wiki/フィンセント・ライメン "wikilink") (Vincent Rijmen) が設計した **Rijndael** （ラインダール）が[2000年](../Page/2000年.md "wikilink")[10月](https://ja.wikipedia.org/wiki/10月 "wikilink")に採用された。

ちなみに、Rijndaelという名称のうち、RijnはRijmen、daeはDaemenから取られたことは明白だが、lはどこから来たのかが不明だった。指導教授だった から取ったのではという説があり、Rijmenが講演した際に質問を受けたが、その答えは "**It's a conjecture.**（それは憶測に過ぎないね）" だった。

## 暗号化の方法

AESは[SPN構造](https://ja.wikipedia.org/wiki/SPN構造 "wikilink")の[ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")で、ブロック長は128[ビット](../Page/ビット.md "wikilink")、鍵長は128ビット・192ビット・256ビットの3つが利用できる\[5\]。

暗号化処理は始めに鍵生成を行う。AES暗号の鍵長によって変換のラウンド数が異なる。次の通りである。

  - 鍵長128ビットのとき、ラウンド数は10回である。
  - 鍵長192ビットのとき、ラウンド数は12回である。
  - 鍵長256ビットのとき、ラウンド数は14回である。

暗号化は下記の４つの処理から構成される\[6\]。

1.  SubBytes - [換字表](https://ja.wikipedia.org/wiki/換字式暗号 "wikilink")（Sボックス）による１バイト単位の置換。
2.  ShiftRows - 4バイト単位の行を一定規則で左シフトする。
3.  MixColumns - ビット演算による４バイト単位の行列変換。
4.  AddRoundKey - ラウンド鍵との[XORをとる](../Page/排他的論理和.md "wikilink")。

これら４つの処理を１ラウンドとして暗号化を行う。

なお、復号は上記処理の逆変換を逆順で実行する。

1.  AddRoundKey
2.  InvMixColumns
3.  InvShiftRows
4.  InvSubBytes

## 安全性

[関連鍵攻撃](https://ja.wikipedia.org/wiki/関連鍵攻撃 "wikilink")により、256ビットのAES暗号の第9ラウンドまでが解読可能である。また、[選択平文攻撃により](https://ja.wikipedia.org/wiki/暗号解読 "wikilink")、192ビットおよび256ビットのAES暗号の第8ラウンドまで、128ビットのAES暗号の第7ラウンドまでが解読可能である (Ferguson et al., 2000)。シュナイアーはAESの「代数的単純さに疑問」を感じているが、AESは欧州の暗号規格[NESSIE](https://ja.wikipedia.org/wiki/NESSIE "wikilink")や日本の暗号規格[CRYPTREC](https://ja.wikipedia.org/wiki/CRYPTREC "wikilink")でも採用された。AESの数学的構造は他のブロック暗号と異なり、きちんとした記述もある\[7\]\[8\]。

この暗号はまだどんな攻撃にも屈していないが、何人かの研究者がこの数学的な構造を利用した攻撃方法が存在するかもしれないと指摘している\[9\]\[10\]。

## 関連項目

  - [ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")
  - [有限体](https://ja.wikipedia.org/wiki/有限体 "wikilink")
  - [Transport Layer Security](../Page/Transport_Layer_Security.md "wikilink") - 暗号化として128ビットおよび256ビットのAES-CBC、AES-[GCM](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink")、AES-[CCMを使用可能](https://ja.wikipedia.org/wiki/Counter_with_CBC-MAC "wikilink")
  - ディスク暗号化
      - [HFS+](https://ja.wikipedia.org/wiki/HFS+ "wikilink") - セキュリティ機能「[FileVault](https://ja.wikipedia.org/wiki/FileVault "wikilink")」が128ビットAES暗号を使用
      - [BitLocker](https://ja.wikipedia.org/wiki/BitLocker "wikilink")
  - [Wii](https://ja.wikipedia.org/wiki/Wii "wikilink") - 暗号化に128ビットAESを使用
  - [アーカイブファイル形式](https://ja.wikipedia.org/wiki/アーカイブ_\(コンピュータ\) "wikilink")
      - [ZIP](../Page/ZIP_\(ファイルフォーマット\).md "wikilink") - 256ビットAESを使用可能
      - [7z](../Page/7z.md "wikilink") - 256ビットAESを使用可能
      - [RAR](../Page/RAR.md "wikilink") - 256ビットAESを使用可能
  - [CCMP](https://ja.wikipedia.org/wiki/Counter_mode_with_Cipher-block_chaining_Message_authentication_code_Protocol "wikilink") - [WEPで用いられていた](https://ja.wikipedia.org/wiki/Wired_Equivalent_Privacy "wikilink")[RC4](https://ja.wikipedia.org/wiki/RC4 "wikilink")、[WPAで用いられていた](https://ja.wikipedia.org/wiki/Wi-Fi_Protected_Access "wikilink")[TKIP](https://ja.wikipedia.org/wiki/Temporal_Key_Integrity_Protocol "wikilink")（本質的にRC4と同等）に代わり、[WPA2で採用された暗号化プロトコル](https://ja.wikipedia.org/wiki/Wi-Fi_Protected_Access#WPA2 "wikilink")。128ビットAESを[CCMモードで利用](https://ja.wikipedia.org/wiki/Counter_with_CBC-MAC "wikilink")
  - [AACS](https://ja.wikipedia.org/wiki/Advanced_Access_Content_System "wikilink") - 128ビットAESを使用
  - [CRYPTREC](https://ja.wikipedia.org/wiki/CRYPTREC "wikilink")
  - [NESSIE](https://ja.wikipedia.org/wiki/NESSIE "wikilink")
  - CPUの[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")
      - [AES-NI](https://ja.wikipedia.org/wiki/AES-NI "wikilink")
      - [CLMUL instruction set](https://ja.wikipedia.org/wiki/CLMUL_instruction_set "wikilink")

## 脚注

<references />

## 参考文献

  - 、NIST発行、2001年

  - 、1999年発行-2003年補追

  -
  -
## 外部リンク

  - 公式サイト
  - [リファレンスコード](https://embeddedsw.net/Cipher_Reference_Home.html)
  - 解説 [AES概説](https://web.archive.org/web/20090503235219/http://www-ailab.elcom.nitech.ac.jp/security/aes/overview.html)（2009年5月3日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
  - 選定過程
  - [Report on the Development of the Advanced Encryption Standard](https://www.nist.gov/publications/report-development-advanced-encryption-standard-aes)

[Category:FIPS](https://ja.wikipedia.org/wiki/Category:FIPS "wikilink")

1.  [岡本 暗号理論入門 第2版(2002:51-52)](https://ja.wikipedia.org/wiki/#okamoto2002 "wikilink")
2.  [結城 暗号技術入門 第3版(2003: 69-71)](https://ja.wikipedia.org/wiki/#yuki2003 "wikilink")
3.
4.
5.
6.
7.  [A simple algebraic representation of Rijndael](http://web.archive.org/web/20030606080156/http://macfergus.com/pub/rdalgeq.html) (Niels Ferguson, Richard Schroeppel, and Doug Whiting)（2003年6月6日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
8.  [Sean Murphy](http://www.isg.rhul.ac.uk/~sean/)
9.  角尾幸保 , 久保博靖, 茂真紀, 辻原悦子, 宮内宏, "", SCIS2003
10.   - (Daniel J. Bernstein)