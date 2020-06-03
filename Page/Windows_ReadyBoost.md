> この記事は[Windows ReadyBoost](https://ja.wikipedia.org/wiki/Windows_ReadyBoost)から翻訳されています。


**Windows ReadyBoost**（ウィンドウズ レディブースト） は、[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、および[Windows 7](../Page/Microsoft_Windows_7.md "wikilink")、[Windows 8/8.1](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")、[Windows 10の一機能](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")。[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")などの外部メモリーを、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")の[キャッシュとして利用することで](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")、ソフトウェアなどの読み込みを高速化する機能のこと。

## 概要

Windows ReadyBoostを使用すると、[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")の記憶領域を[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")として使用し、総合的なパフォーマンスを向上させる \[1\] \[2\]。

ハードディスクはディスク上のデータをヘッドを使って読み書きしている。この時、数キロバイトといった小さなデータが散らばっていると、ヘッドの物理的な移動量が増え、実転送以外の動作によって、アクセス速度が極端に低下する。Windows ReadyBoostはこの小さなデータ群を、物理的なヘッドの存在しないフラッシュメモリにキャッシュすることで、ハードディスクのランダムアクセス時の性能低下という弱点を補助しようという技術である。そのため、使用するフラッシュメモリにはこれまで重視されてきた[シーケンシャルアクセス](../Page/シーケンシャルアクセス.md "wikilink")速度ではなく、[ランダムアクセス](../Page/ランダムアクセス.md "wikilink")速度が重視される。

PCに搭載している[メインメモリと同じ容量か](../Page/主記憶装置.md "wikilink")、それよりも多いものを使用することが推奨されているが、小容量でも効果が出ないわけではない。[マイクロソフト](../Page/マイクロソフト.md "wikilink")によると、搭載されたメインメモリの「3倍の容量\[3\]のフラッシュメモリ」を使用することで、最も優れたパフォーマンスを得ることができるとされる\[4\]。

## 対応メディア

使用するUSBメモリなどの外部記録メディアには、最低でも4kBデータのランダムリードで2.5MB/s、512kBデータのランダムライトで1.75MB/sの速度が必要である。前述のとおり、ランダムアクセス性能を補完するための仕組みであるため、高速タイプ（4kBデータのランダムリードを5MB/s、512kBデータのランダイムライトを3MB/s）のメディアを用いれば更に効果が大きくなる\[5\]。USB2.0のバスは高速とは言い難いが、データは暗号化だけではなく、最大1/3に圧縮されて処理される事で、転送量そのものを減らす努力がされている。市販のUSBメモリやSDメモリーカード等は然程高速ではないバスに繋がれることもあり、必ずしも使用可能な性能を持っているわけではなく、対応可能や、高速性をうたった製品以外では利用できない可能性が高いことにも注意が必要である。

|          | Windows Vista                                                                                                                                                                       | Windows 7                                                                | Windows 8 / 8.1 | Windows 10 |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | --------------- | ---------- |
| 対応デバイス   | [USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")、[SDメモリーカード](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")等のフラッシュメモリ（[リムーバブルメディア](../Page/リムーバブルメディア.md "wikilink")） |                                                                          |                 |            |
| 最大容量     | 4GB                                                                                                                                                                                 | 256GB\*                                                                  |                 |            |
| 最低容量     | 230MB（1GB以上を推奨）                                                                                                                                                                     |                                                                          |                 |            |
| 最大デバイス数  | 1                                                                                                                                                                                   | 8                                                                        |                 |            |
| 対応フォーマット | [FAT16](../Page/File_Allocation_Table.md "wikilink")、FAT32、（[NTFS](../Page/NT_File_System.md "wikilink")）                                                                           | FAT16、FAT32、NTFS、[exFAT](https://ja.wikipedia.org/wiki/exFAT "wikilink") |                 |            |

Windows ReadyBoostの対応メディア

  - 2014年3月現在、64GB以上の外部ストレージ接続時にWindows ReadyBoostを有効にできない現象が確認されている<ref group="注釈">[Windows 7 に 64 GB より大きいパーティションが存在する外部ストレージを接続すると、ReadyBoost 機能を使用できない](http://support.microsoft.com/kb/980421/ja)

</ref>。Windows 8/8.1とWindows 10では設定できるものの、1デバイスあたりに設定できる最大容量は32GB。

フラッシュメモリの容量が多いほど効果を得られると思われがちであるが、実際には容量よりも速度性能を重視すべき仕組みである。システムの制限で\[6\]、Windows Vista環境下では4GB以上のフラッシュメモリを接続しても4GBまでの使用となるが、Windows 7、およびWindows 8の環境下ではexFATによるフォーマットをした大容量フラッシュメモリにおいて4GBを超えた使用が可能になった \[7\]。 またWindows Vistaでは、1台のPCに複数のフラッシュメモリを接続しても1つしか利用できなかったが、Windows 7、およびWindows 8/8.1、Windows 10では複数のフラッシュメモリを利用できるようになった。

## 機能

### 基本

ReadyBoostは、HDDの読み出し時の物理的な[シークタイムを隠蔽する事で](https://ja.wikipedia.org/wiki/シーク_\(コンピュータ\) "wikilink")、体感速度を改善する。

HDDとの読み書きのデータが全てフラッシュメモリにキャッシングされるわけではない。高速なHDDでの大量のシーケンシャルアクセスの場合には、フラッシュメモリよりも高スループットでアクセスできることが多く、そのような場合はフラッシュメモリへのキャッシング処理はなされない。

ランダムアクセスのように、HDDではヘッドのシーク待ちやディスクの回転待ちが原因で極端にスループットが落ちる場合、フラッシュメモリへのキャッシング処理がなされ、ReadyBoostとして機能する\[8\]。

フラッシュメモリの書き換え回数に上限がある特性を考慮し、ReadyBoostではデータを書き込む位置を非局在化（[ウェアレベリング](../Page/ウェアレベリング.md "wikilink")）しており、フラッシュメモリの寿命にも配慮されているが、管理領域の不良や、故障の影響は使用領域以外にも出ることになるので、データを保存する物とは別で用意することが望ましい。

### ライトスルーキャッシュ

基本的に、書き込みデータについてはハードディスクに対してデータ書き込みコマンドを送信した後で、フラッシュメモリにキャッシュするために（ライトスルー）、突然フラッシュメモリがUSB端子から抜けるといったような不測の事態が起きても、システムが不安定になることはない。また、シャットダウン後の取り外しなど、改変の可能性があるため、書き込まれたデータは、ReadyBoostとしては保持、記憶、蓄積はされない。 なお、書き込まれるデータは[AES](../Page/Advanced_Encryption_Standard.md "wikilink")128ビットによる[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")処理がされているため、万が一盗難にあった時にメモリやHDDの一部が閲覧されることは無いとされている。

### SuperFetchとの関係

なお、[Windows SuperFetchは](https://ja.wikipedia.org/wiki/Windows_SuperFetch "wikilink")、未使用のメインメモリを利用して、ReadyBoostと似たディスクキャッシュを行っている\[9\]。両者の違いは、Superfetch はプロセスのページプール（コード、データなど）のキャッシングを制御するのに対して、ReadyBoostはHDDストレージへの読み書き全般をキャッシングすると言う点である。ReadyBoostサービスは、キャッシングの効率化（プリフェッチ等）に関して、SuperFetchサービスの助けを借りる\[10\]。

大量のメインメモリを搭載し空きメモリ容量\[11\]が潤沢にある状況では、SuperFetchの方にヒットする確率が高くなるので、ReadyBoost自体の貢献度は小さくなる。また、システムドライブに[SSDを利用する環境では](../Page/ソリッドステートドライブ.md "wikilink")、もともと高速なドライブであるため、ReadyBoostを利用できないことがある\[12\]。

ReadyBoost、Superfetchのいずれも、[仮想記憶](../Page/仮想記憶.md "wikilink")・プロセスを邪魔しないように、バックグラウンドで最も低い優先度でキャッシング処理を行う。ReadyBoostが[仮想記憶](../Page/仮想記憶.md "wikilink")をフラッシュメモリに対し行うというのは誤解である\[13\]。

一部のメディアの論評などでは、ReadyBoostにはメモリ増設と同様の効果があるかのような記述がみられるが、もともと、[ノート型パソコン](https://ja.wikipedia.org/wiki/ノート型パソコン "wikilink")のような、

  - ハードディスクへのアクセスが遅い。
  - 搭載メインメモリが少ない。
  - メモリの拡張に高いコストがかかる。

等の条件にあたる環境で、「低コストで体感するレスポンスを改善する手段」であるとマイクロソフト自身が事前にプレゼンテーションでも述べており\[14\]、実際には仮想記憶やメモリに関わる仕組みではなく、ストレージのアクセス性能を補助する仕組みであり、公式な説明や事実とは大きく異なるニュアンスの記述であるといえる。

### Windows ReadyBoot

ReadyBoostサービスは、OSの起動時、起動直後にも稼動する。ただし、キャッシングのデバイスはフラッシュメモリではなくメインメモリ（700MB以上の場合に限る）である。

これは Windows Ready**Boot** と名づけられた機能で、OSの起動直後に、起動中に読み込まれるファイルを分析して、予めキャッシング計画をする。次回のOS起動時に、その計画に基づきReadyBoostがシステム読み込みに対してキャッシングを行い、起動を高速化する。

## 備考

Windows ReadyBoostは、Windowsがシステムとして提供する機能の一つであるが、同様の機能を提供するソフトウェアとして [eBoostr](https://ja.wikipedia.org/wiki/eBoostr "wikilink") がある。これは、ReadyBoost 及び [Windows SuperFetchの代替機能を提供するシステムソフトウェアであり](https://ja.wikipedia.org/wiki/Windows_SuperFetch "wikilink")、[Windows 2000](https://ja.wikipedia.org/wiki/Windows_2000 "wikilink") や [Windows XP](https://ja.wikipedia.org/wiki/Windows_XP "wikilink") など、Vista以外のWindows OSにも対応するなどの特徴を持つ。

Windows Vistaには[Windows ReadyDriveという機能も実装されているが](https://ja.wikipedia.org/wiki/Windows_ReadyDrive "wikilink")、これは別の仕組みである。

ReadyBoostの解説にはあたかもキャッシュデバイスは外付けUSBスティックに限るような表現がみられるが、そのようなことはなく内部SSDを含めてどのようなデバイスでも良い。例えば、30GB程度の小容量（=低価格）のSSDを恒久的に追加しても効果がある。

[SanDisk](https://ja.wikipedia.org/wiki/SanDisk "wikilink")には小容量の汎用SSDとドライバソフトウェアを組み合わせた[ReadyCache](https://ja.wikipedia.org/wiki/ReadyCache "wikilink")と言う似たような原理と効果の製品があるが、こちらはSSD全体を（Windowsがドライブとして認識しない）ハードウェア・キャッシュデバイスとして扱い、しかも適用はWindowsのソフトウェア[RAID](../Page/RAID.md "wikilink")**ではない**「シンプル・ボリューム」に限られるが、Windows ReadyBoostはWindowsが認識してマウントするドライブ上の[ファイルをキャッシュデバイスとして扱い](../Page/ファイル_\(コンピュータ\).md "wikilink")、RAIDの「ダイナミック・ボリューム」にも適用可能な違いがある。

## 関連項目

  - [Windows SuperFetch](https://ja.wikipedia.org/wiki/Windows_SuperFetch "wikilink")
  - [Windows ReadyDrive](https://ja.wikipedia.org/wiki/Windows_ReadyDrive "wikilink")
  - [eBoostr](https://ja.wikipedia.org/wiki/eBoostr "wikilink")
  - [ハイブリッドHDD](../Page/ハイブリッドHDD.md "wikilink")

## 脚注

<references group="注釈"/>

## 参考文献

<references/>

[Category:Windows_7](https://ja.wikipedia.org/wiki/Category:Windows_7 "wikilink") [Category:Windows_8](https://ja.wikipedia.org/wiki/Category:Windows_8 "wikilink")

1.
2.
3.  発表当時おもな対象とされたノートPCなどの搭載メモリは1GB前後
4.
5.
6.
7.  [Windows 7 の機能 - ReadyBoost - Microsoft Windows](http://windows.microsoft.com/ja-JP/windows7/products/features/readyboost)
8.  <http://technet.microsoft.com/ja-jp/windows/ff467971.aspx>
9.
10.
11. OSやアプリケーションが使用していないメモリは、SuperFetchがキャッシュに利用する。
12. [記憶装置のメモリを使用してコンピューターの速度を向上する](http://windows.microsoft.com/ja-JP/windows7/Using-memory-in-your-storage-device-to-speed-up-your-computer)
13. リムーバブルメディアにページファイルを置くことはできない。スワップアウトされたページがシステムから取り外された場合、システムは通常停止する。
14. [「Aero無しでもVistaは魅力的」Windows Vistaのビジネス向け新機能説明会](http://internet.watch.impress.co.jp/cda/news/2006/06/12/12293.html)