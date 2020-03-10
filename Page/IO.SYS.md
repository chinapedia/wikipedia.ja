> この記事は[IO.SYS](https://ja.wikipedia.org/wiki/IO.SYS)から翻訳されています。


**IO.SYS** は、[MS-DOS](../Page/MS-DOS.md "wikilink")の[カーネル](../Page/カーネル.md "wikilink")のうち、機種依存する部分（のファイル名）である。デフォルト（カーネル内蔵）の[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")等の他、初期化プログラムも含むため、MS-DOSのカーネルのうちで最初に動作する部分のコードも含む。なお、[Windows 9x系では](https://ja.wikipedia.org/wiki/Windows_9x系 "wikilink")[MSDOS.SYS](https://ja.wikipedia.org/wiki/MSDOS.SYS "wikilink")はコードを含まないものとなっており、全てのコードがIO.SYSに移動されている。通常、「隠し」「読み取り専用」「システム」の属性がオンにされている。

[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")は[ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")されると、セルフチェック等の後、最後に[ブートセクタ](../Page/ブートセクタ.md "wikilink")をメモリに読み込み、実行する。それがDOSのブートセクタだった場合、IO.SYS の最初の3セクタをメモリにロードし、それに制御を移す。以下は次のような流れになる。

1.  自分自身の残りの部分をメモリにロードする。
2.  デフォルトの[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")群を1つずつ初期化する（[コンソール](https://ja.wikipedia.org/wiki/コンソール "wikilink")、ディスク、[シリアルポート](../Page/シリアルポート.md "wikilink")など）。この時点でこれらのデバイスを利用可能になる。
3.  DOSカーネルをロードし、その初期化ルーチンを呼び出す。カーネルは MS-DOS の場合は [MSDOS.SYS](https://ja.wikipedia.org/wiki/MSDOS.SYS "wikilink") にあり、Windows 9x系では IO.SYS 内にある。この時点で、通常のファイルアクセスが可能になる。
4.  Windows 9x系の場合、MSDOS.SYS ファイルの処理をする。
5.  MS-DOS 2.0以降および Windows 9x系の場合、[CONFIG.SYS](https://ja.wikipedia.org/wiki/CONFIG.SYS "wikilink") ファイルの処理をする。
6.  [COMMAND.COM](../Page/COMMAND.COM.md "wikilink") をロードする（他のシェルが指定されている場合はそれをロードする）。
7.  Windows 9x系では、[ブートスプラッシュ](https://ja.wikipedia.org/wiki/ブートスプラッシュ "wikilink")を表示する。Logo.sys がある場合、それをブートスプラッシュとして使う。ない場合は IO.SYS 内のブートスプラッシュを使う。

[PC DOSおよび](https://ja.wikipedia.org/wiki/IBM_PC_DOS "wikilink")[DR-DOS](https://ja.wikipedia.org/wiki/DR-DOS "wikilink")では IBMBIO.COM という名前である。

## 外部リンク

  - [MS-DOS Device Driver Names Cannot be Used As File Names](http://support.microsoft.com/kb/74496/en-us) — IO.SYS内のデフォルトのデバイスドライバの一覧がある。
  - [SYS.COM Requirements in MS-DOS Versions 2.0-6.0](http://support.microsoft.com/kb/66530/en-us) — ロードすべき IO.SYS の要求仕様がある。

[Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink")