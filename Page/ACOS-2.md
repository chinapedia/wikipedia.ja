> この記事は[ACOS-2](https://ja.wikipedia.org/wiki/ACOS-2)から翻訳されています。


**ACOS-2**（エイコスツー）は、[日本電気](../Page/日本電気.md "wikilink")の[メインフレーム](../Page/メインフレーム.md "wikilink")およびそのOSである[ACOS](https://ja.wikipedia.org/wiki/ACOS "wikilink")の一系列である。

## 概要

ACOS-2は、ハネウェル社が当初から開発していたOSを基に初期版が開発されたOSである。2015年時点での名称はACOS-2/MP、対象となるハードウェアはi-PX7300GXである。

ACOS-2の兄弟分は[ACOS-4](../Page/ACOS-4.md "wikilink")であり、[ACOS-6](../Page/ACOS-6.md "wikilink")とは、その構造が大きく異なっている（理由については、[ACOS](https://ja.wikipedia.org/wiki/ACOS "wikilink")の項を参照）。他の2つのOSともども同社のメインフレーム事業草創期にハネウェル社から導入した技術が基となっている。

## メモリ管理方式

### メモリ管理方式の変遷

初期のACOS-2（および搭載ハードウェア）においては、[仮想メモリ](https://ja.wikipedia.org/wiki/仮想メモリ "wikilink")機構は採用されておらず、実装しているメモリ空間のみで動作していた。その後、プログラム格納部分とデータ格納部分が1つのプログラム毎に1つずつ与えられる形式の[セグメント方式](../Page/セグメント方式.md "wikilink")へ経て、[ACOS-4](../Page/ACOS-4.md "wikilink")と共通なセグメント化[ページング方式](../Page/ページング方式.md "wikilink")のメモリ管理へと移行していった。

。

## 使用文字コード

内部、外部ともに、1バイトを8ビットで扱う[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")-カタカナコードである。[ACOS-4](../Page/ACOS-4.md "wikilink")とは共通するが、[ACOS-6](../Page/ACOS-6.md "wikilink")とは異なるため、データ交換を行なうためには、文字コードの変換が必要となる。

日本語は、[JIPS](../Page/JIPS.md "wikilink")(E)コードと呼ばれるコードを使用する。これはNEC独自のコード体系であり、JIS C 6226 1978の上位下位各バイトに対して『[EBCDIC変換](https://ja.wikipedia.org/wiki/EBCDIC変換 "wikilink")』という特殊な変換をして得られる符号化体系である。また、[ACOS-4](../Page/ACOS-4.md "wikilink")もこのJIPS(E)を標準の文字コードとして利用する。

## ファイルシステム

ACOS-2の[ファイルシステム](../Page/ファイルシステム.md "wikilink")（ハードディスク上のファイル管理方式）は、[UNIX](../Page/UNIX.md "wikilink")などで採用されている[ディレクトリ](../Page/ディレクトリ.md "wikilink")（階層）構造を持たず、実装されているハードディスク毎に存在する[VTOC](https://ja.wikipedia.org/wiki/VTOC "wikilink")と呼ばれる管理領域に、当該ハードディスクに格納されている全てのファイルが登録される仕組みになっている。ディレクトリ構造に慣れた者にとっては、ハードディスク毎にルートディレクトリが存在し、その直下に全ファイルが登録されている状態に見えるかもしれない（実際の記録方式は異なる）。

ファイル名は英字大文字と数字、さらに"@"文字がファイル名の先頭と最後を除く位置に使用できる。ファイル名の最大長は16文字。なお、"@"文字の直後に特定の文字列を含むファイル名は、含めた特定の文字列ごとに使用目的が対応づけられているファイル（通常、[ライブラリ](../Page/ライブラリ.md "wikilink")ファイル）として、ACOS-2に予約されている。この仕組みを含めて、[ACOS-4](../Page/ACOS-4.md "wikilink")とはファイル名の仕組みは異なる。

### 標準入力および標準出力

ACOS-2には[ACOS-4と同じく](https://ja.wikipedia.org/wiki/ACOS-4#標準入力および標準出力 "wikilink")、SYSINと呼ばれる標準入力およびSYSOUTと呼ばれる標準出力が装備されている。ただし、JCLに同梱されている入力データとSYSINからデータを読み込むプログラムとの関連付け方（JCLの記述方法）や、SYSOUTを使用する為のJCLなどの記述方法に違いがある。

1つのプログラムが使用できる標準入力は1つのみ。標準出力も通常1つ。

## 使い勝手の異なる兄弟OS

現在では改善されたと思われるが、同じ[ハネウェル](../Page/ハネウェル.md "wikilink")社で当初から開発された技術を元に、日本電気にて開発されたOSであるにも関わらず、小型機用OSであるACOS-2と、中型機（およびそれ以上）用OSである[ACOS-4](../Page/ACOS-4.md "wikilink")には、いくつか使い勝手の異なる部分があった（単なる規模や処理能力の大小などの差に拠るものではない、説明し難い仕様の差異）。

  - バッチ（一括処理）型システム（→[コンピュータシステム](../Page/コンピュータシステム.md "wikilink")）として使用する際、一括処理を行なう単位の概念が、[ACOS-4](../Page/ACOS-4.md "wikilink")に比べて1階層多い。ACOS-2はアクティビティ→ジョブ→ジョブステップの3階層なのに対し、ACOS-4は、ジョブ→ジョブステップの2階層となっている。
  - TSS（[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")）の操作作法（端末の操作の手順など）や、遠隔地からのオペレータ制御卓の操作などの使い勝手の差異に習熟する必要がある。

など。

。

[ACOS-4](../Page/ACOS-4.md "wikilink")が、当初の中型機から大型以上へとハードウェア展開した理由も、[ACOS-6](../Page/ACOS-6.md "wikilink")との間にある、操作・運用・プログラム作成上の習熟の壁が影響した為と考えられる（使用[文字コードや](../Page/ACOS-6.md "wikilink")[ファイルシステムなど根幹の部分から異なる為](https://ja.wikipedia.org/wiki/ACOS-6#ファイルシステム "wikilink")、移行を阻む壁は、ACOS-2からACOS-4へ移行する場合より、はるかに高い）。

## 歴史

  - ACOS-2
  - ACOS-2/EF （R1.1 - R4.1）
  - ACOS-2/EVP （R1.1 - R5.1）
  - ACOS-2/XP （R1.1（1994年6月末に公開）- R13.1（2001年4月末に公開；2005年3月31日付で保守停止））
  - ACOS-2/MP （R1.1（2000年7月末に公開）- R11.1（2015年7月17日に公開；最新版））

## 関連項目

  - [GCOS](../Page/GCOS.md "wikilink")

## 参考文献

本項目 (ACOS-2) に関する記述は、外部リンクの項に示した情報以外に、実機に付属していた複数の説明書、および、実機を使用する事により得た情報を元に作成している（特に、[ACOS-4](../Page/ACOS-4.md "wikilink")や[ACOS-6](../Page/ACOS-6.md "wikilink")と関連付けて記述している部分）。

記述の一部が、現行機種とは異なる古い内容になっている場合があり得る事をご了承願いたい。

## 外部リンク

  - [ACOS-2 : ACOSシリーズ](http://www.nec.co.jp/products/acosclub/acos2.html) - NEC
  - [【日本電気】 ACOS-2](http://museum.ipsj.or.jp/computer/os/nec/0005.html) - コンピュータ博物館（[情報処理学会](../Page/情報処理学会.md "wikilink")）

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:日本電気の製品](https://ja.wikipedia.org/wiki/Category:日本電気の製品 "wikilink")