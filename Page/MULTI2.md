> この記事は[MULTI2](https://ja.wikipedia.org/wiki/MULTI2)から翻訳されています。


**MULTI2**（マルチツー）とは、[1988年](../Page/1988年.md "wikilink")に[日立製作所](../Page/日立製作所.md "wikilink")により開発された[ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")である。日本の衛星・[地上デジタル放送](https://ja.wikipedia.org/wiki/地上デジタル放送 "wikilink")の標準暗号として採用されている。

## 概要

MULTI2は、[ブロック長](https://ja.wikipedia.org/wiki/ブロック長 "wikilink")64ビット、鍵長64ビットで、4種類ある[ラウンド](https://ja.wikipedia.org/wiki/ラウンド "wikilink")関数の繰り返しによりスクランブルする[積和型](https://ja.wikipedia.org/wiki/積和型 "wikilink")ブロック暗号である。ラウンド数は可変である。

ISO/IEC 9979にもとづく暗号アルゴリズム登録制度に[アルゴリズム](../Page/アルゴリズム.md "wikilink")を公開して登録されている（登録番号9、[1994年](../Page/1994年.md "wikilink")）。MULTI2 はアルゴリズムが完全に公開されているが、これ以外のMULTIX （MULTI3やMULTI4などが存在するとされる）はアルゴリズムが秘匿されている。

MULTI2は、日本の[デジタル放送](https://ja.wikipedia.org/wiki/デジタル放送 "wikilink")用[限定受信方式](https://ja.wikipedia.org/wiki/限定受信システム "wikilink")（[B-CAS](https://ja.wikipedia.org/wiki/B-CAS "wikilink")）の標準暗号として採用されている。[衛星デジタル放送](https://ja.wikipedia.org/wiki/衛星デジタル放送 "wikilink")や[東経110度CSデジタル放送](https://ja.wikipedia.org/wiki/東経110度CSデジタル放送 "wikilink")、[地上デジタルテレビジョン放送](https://ja.wikipedia.org/wiki/地上デジタルテレビジョン放送 "wikilink")などの放送波は、MULTI2で暗号化されてチューナにて受信、復号される。ブロック長が64ビットと少ないため、次世代の放送サービスでは、[AESや](../Page/Advanced_Encryption_Standard.md "wikilink")[Camellia](../Page/Camellia.md "wikilink")といった128ビットブロック暗号の採用も検討されている\[1\]。

## 構造

入力64ビットを左右32ビットに分割したのち、ラウンド関数 Π1～Π4 の繰り返しでスクランブルを行う。Π1とΠ3は右32ビットを変換し、Π2とΠ4は左32ビットを変換する[Feistel構造](../Page/Feistel構造.md "wikilink")に類似した構造になっている。

鍵スケジューラでは、鍵（=データ鍵）64ビットと、システム固定値（=システム鍵）256ビットを使用して拡大鍵256ビットを生成する。メインのスクランブラと同じラウンド関数 Π1～Π4 を使用して、データ鍵をシステム鍵で "暗号化" したときの各ラウンドの出力を拡大鍵とする。1ラウンド毎に32ビットの出力があり、8ラウンド繰り返して256ビットを得る。

ラウンド関数は、32ビットCPUでの実装効率を意識して、S-BOXやビット単位の転置は使用せずに、論理和・排他的論理和、加算・減算、ビットシフトのみで構成されている。

## 性能

MULTI2はラウンド数が可変であり、スループットはラウンド数によって変化する。

[1989年](../Page/1989年.md "wikilink")の開発者による報告によると、ワークステーション2050/32(MC68020,20MHz)で、[ソフトウェア](../Page/ソフトウェア.md "wikilink")実装（[C言語](../Page/C言語.md "wikilink")）すると278Kbpsの[スループット](../Page/スループット.md "wikilink")がある。 ISO/IEC 9979のレジスト文書では、ラウンド数32のとき、1[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")のマシンで約1[Mbps](https://ja.wikipedia.org/wiki/Mbps "wikilink")と主張されている。

## 安全性

12段以下では、[選択平文攻撃](https://ja.wikipedia.org/wiki/選択平文攻撃 "wikilink")により現実的な時間で攻撃可能である。 32段以上で[DESと同等とされる](../Page/Data_Encryption_Standard.md "wikilink")。

## 標準化

MULTI2は、[1996年](../Page/1996年.md "wikilink")に開始されたCSデジタル放送で使用されるスクランブルの標準暗号として採用された。 デジタル放送のトランスポート・ストリーム（TSパケットのペイロード部分）の暗号化に使用されている。その後、BSデジタル放送、地上デジタル放送での同様に採用された。(stub)

デジタル放送のコンテンツ権利保護方式として、ストリーム型のTYPE1コンテンツに対するアクセス制御方式には互換性を重視してMULTI2を使用し、ファイル型（蓄積型）のTYPE2コンテンツには用途に応じて堅牢なアルゴリズムを選択可能とすることが検討されている。

## 歴史

  - [1988年](../Page/1988年.md "wikilink") 日立製作所にて開発（4月28日に特許出願）
  - [1989年](../Page/1989年.md "wikilink") 情報処理学会 DPS研究会で発表
  - [1994年](../Page/1994年.md "wikilink") ISO/IEC 9979 暗号アルゴリズム登録（登録番号 9 ）
  - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink") CSデジタル衛星放送用のスクランブルの標準暗号に採用
  - [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink") MULTI2に関する出願が特許登録される（第2760799号）
  - [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink") ISO/IEC 9979 暗号アルゴリズム登録制度が廃止される
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink") [特許](https://ja.wikipedia.org/wiki/特許 "wikilink")の期限が切れる

## 脚注

## 参考文献

  - 特許公報, 第2760799号, 名称:暗号方式, 発明者:宝木和夫, 中川聡夫, 佐々木良一, 出願日:昭和63年4月28日.
  - 宝木和夫, 佐々木良一, 中川聡夫, "マルチメディア向け高速暗号方式 Multi - Media Encryption Alogorithm", 情報処理学会, マルチメディア通信と分散処理, Vol.1989 No.11, pp.1-8, 1989-1-19.

<!-- end list -->

  - , 登録日：1994-11-14.

  - , 登録制度の廃止日：2006-02-09

  - 松井充, 山岸篤弘, "秘密鍵暗号方式の確率的解読法に関する考察", 電子情報通信学会論文誌 A, Vol.J77-A No.3, pp.476-484, 1994.

<!-- end list -->

  - 電波産業会, ARIB STD-B25, "デジタル放送におけるアクセス制御方式", 平成11年10月26日策定, 1999.
  - 電波産業会, ARIB TR-B15, "BS/広帯域CSデジタル放送運用規定", 平成11年10月26日制定, 1999.
  - 電波産業会, ARIB TR-B14, "地上デジタルテレビジョン放送運用規定", 平成14年1月24日制定, 2002.

## 関連項目

  - [ブロック暗号](https://ja.wikipedia.org/wiki/ブロック暗号 "wikilink")
  - [共通鍵暗号](../Page/共通鍵暗号.md "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")

## 外部リンク

  - \- MULTI2の開発は1988年、CSデジタル放送への採用は1995年としている。

  - <http://www.chrismitchell.net/ISO-register/0009.pdf>: ISO 9979への登録情報

[Category:日立製作所](https://ja.wikipedia.org/wiki/Category:日立製作所 "wikilink")

1.