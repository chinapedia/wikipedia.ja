> この記事は[AIM-65](https://ja.wikipedia.org/wiki/AIM-65)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Aim65.JPG "wikilink") **AIM-65** は、[ロックウェル・インターナショナル](../Page/ロックウェル・インターナショナル.md "wikilink")が[1976年](../Page/1976年.md "wikilink")に発売した高機能の[ワンボードマイコン](../Page/ワンボードマイコン.md "wikilink")であり、[MOS 6502](../Page/MOS_6502.md "wikilink") を搭載していた。

## 概要

AIM-65 は基本的に [KIM-1](../Page/KIM-1.md "wikilink") を拡張したものである。利用可能なソフトウェアとしては、[機械語モニタ](https://ja.wikipedia.org/wiki/機械語モニタ "wikilink")、[BASIC](../Page/BASIC.md "wikilink")インタプリタ、[アセンブラ](../Page/アセンブリ言語.md "wikilink")、[Pascal](../Page/Pascal.md "wikilink")、PL/65、[Forth](../Page/Forth.md "wikilink")処理系があった。拡張部品として[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")コントローラもあった。

機械語モニタを含むROM上の標準ソフトウェアは Advanced Interactive Monitor と呼ばれ、ラインアセンブラ、逆アセンブラ、メモリおよびレジスタの内容表示機能、他のプログラムの起動機能などを備えていた。マスク不可[割り込み](../Page/割り込み_\(コンピュータ\).md "wikilink")（NMI）を使ったステップ実行も可能であった。コマンドプロンプトは "\<" で、1文字のコマンドを受け付け、その文字と "\>" を表示する。熱転写プリンタがONになっていると、それが一行として印字される。機械語モニタには各種サービスルーチンがあり、ソースコードと説明文書が添付されていた。

カセットテープ2台を制御可能で、大規模なアセンブリ言語プログラムを2パスのアセンブラROMを使って書くことが可能である。テキスト内のソースコードが入力テープに2回連続して書かれ、アセンブラが呼び出される。入力カセットテープはモーター制御によって起動・停止される。1回目のパスでは、[シンボルテーブル](../Page/シンボルテーブル.md "wikilink")が作成され RAM に格納される。2回目のパスでシンボルテーブルが翻訳され、出力用テープにコードが書かれ、このときもモーター制御が使われる。コードを RAM 上に格納せずに済むので、大きなプログラムでもアセンブル可能であった。しかし、RAM は4KBしかないため、シンボル名を短くする必要があった。

1981年、ロックウェルは表示を40桁に拡張した **AIM-65/40** を発売した。

MTU は1978年、KIM-1 と AIM-65 で使える "Visible Memory" を発売した。これは、グラフィックディスプレイ機能を提供するものである。また、MTU は KIM-1 と AIM-65 でリアルタイム動作する[シンセサイザー](../Page/シンセサイザー.md "wikilink")も発売している。これは[デジタル-アナログ変換回路](../Page/デジタル-アナログ変換回路.md "wikilink")とソフトウェアによる4声の[wavetable synthesisを組み合わせたものであった](https://ja.wikipedia.org/wiki/:en:wavetable_synthesis "wikilink")。

## 仕様

  - [QWERTY配列](../Page/QWERTY配列.md "wikilink")のフルキーボード装備
  - 20桁の英数字LEDディスプレイ（16セグメント）
  - 20桁の熱転写プリンタ装備
  - RS-232 シリアル・インタフェース
  - 拡張コネクタ
  - [6522 VIA](https://ja.wikipedia.org/wiki/MOS_6522 "wikilink") チップによるアプリケーションコネクタ（パラレル・インタフェース）
  - 4 KB [RAM](https://ja.wikipedia.org/wiki/ランダムアクセスメモリ "wikilink")
  - 4 KB [ROM](https://ja.wikipedia.org/wiki/読み出し専用メモリ "wikilink")/[EPROM](../Page/EPROM.md "wikilink")チップ用のソケットを5個装備

## プログラミング

*PL/65* は、ロックウェル・インターナショナルが AIM-65 向けに設計・実装した[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。\[1\]。[ALGOL](../Page/ALGOL.md "wikilink") と [PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink") の混合に基づき、6502 の使えるリソース量の限界に合わせるように単純化した言語であった。

## 脚注

## 外部リンク

  - [Rockwell AIM 65](http://www.oldcomputers.net/AIM-65.html) Old Computers
  - [AIM-65](http://www.oldcomputermuseum.com/aim_65.html) Old Computer Museum
  - [Rockwell AIM 65](http://www.obsoletecomputermuseum.org/aim65/) Obsolete Computer Museum
  - [AIM 65](http://www.old-computers.com/museum/computer.asp?st=1&c=58) OLD-COMPUTERS.COM
  - [MTU Digital Audio Products 1977 to 1995](http://www.mtu.com/support/mtuaudioproducts.htm) MTU.com

[Category:第一世代のマイクロコンピュータ](https://ja.wikipedia.org/wiki/Category:第一世代のマイクロコンピュータ "wikilink")

1.