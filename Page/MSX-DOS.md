> この記事は[MSX-DOS](https://ja.wikipedia.org/wiki/MSX-DOS)から翻訳されています。


**MSX-DOS**（エムエスエックスドス）は、[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")規格向けに開発された、[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")上位互換の[DOSである](https://ja.wikipedia.org/wiki/DOS_\(OS\) "wikilink")。MSX-DOS1とMSX-DOS2がある。

## 開発

MSX-DOSは、[アスキーと](../Page/アスキー_\(企業\).md "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")、国内家電各社などを中心として1983年に策定されたホームコンピューター(家庭用テレビに接続し直ぐに使用できる安価で便利なコンピューターの事)の統一規格「MSX」のシステム環境、OS（オペレーティングシステム）環境としてMSX-BASICと共に開発された。1983年、マイクロソフトは、[MS-DOS](../Page/MS-DOS.md "wikilink")をMSXに移植する契約を[ティム・パターソン](https://ja.wikipedia.org/wiki/ティム・パターソン "wikilink")と交わした。パターソンは彼の会社に資金を助成するという契約を受け入れ、1984年にMSX-DOSオペレーティングシステムを完成させた\[1\]。

## 互換性

OSとしては、当時80系（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") [8080系](../Page/Intel_8080.md "wikilink")）CPUを搭載したコンピューターで広く利用されていた米[Digital Research社開発のCP](../Page/デジタルリサーチ.md "wikilink")/M80との上位互換性を確保したクローンOSの一種である。構造的には、CP/M 1.4相当の機能に加え当時すでに普及が始まっていた86系（インテル [8086](https://ja.wikipedia.org/wiki/8086 "wikilink")系）コンピューター向けのMS-DOSの Version 1.25 で用いられていた[FAT12](https://ja.wikipedia.org/wiki/FAT12 "wikilink")と[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")を持つファイルシステムを採用した。

フロントエンドとなる[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")[コマンドインタプリター](https://ja.wikipedia.org/wiki/コマンドインタプリター "wikilink")は、CP/MのCCPの代わりにMS-DOS環境で標準的に用いられていたCOMMAND.COM環境を移植したサブセットである。ただし、MSX-DOSとMS-DOSはシステムコールやバイナリーには互換性の無いまったく別のOSである。

MSX-DOSは、[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")との[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")([BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink"))および[バイナリー](https://ja.wikipedia.org/wiki/バイナリー "wikilink")互換を持っている。FAT12とほぼ同一のファイルシステムを採用しているが、[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")の[半角](https://ja.wikipedia.org/wiki/半角 "wikilink")[平仮名](../Page/平仮名.md "wikilink")（1[バイトの平仮名](../Page/バイト_\(情報\).md "wikilink")[文字](../Page/文字.md "wikilink")）などをサポートするために8bit透過性が確保されているなどの特色もある。

CP/Mとは[TPAの容量に注意すればバイナリーにも互換性があり](https://ja.wikipedia.org/wiki/CP/M#トランジェントコマンド "wikilink")、CP/M用の [Word Master](https://ja.wikipedia.org/wiki/Word_Master "wikilink")/[WordStar](https://ja.wikipedia.org/wiki/WordStar "wikilink") や [Turbo Pascal](../Page/Turbo_Pascal.md "wikilink") などの各種アプリケーションはファイルシステムをコンバートするとMSX-DOS上でそのまま動作する。

## MSX用のMSX-DOS

[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")[ドライブ](https://ja.wikipedia.org/wiki/ドライブ "wikilink")や[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")ー本体、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")に付属して配布された。使用には最低64KBのメインメモリがー必要。MSX-DOSだけが個別に[販売](../Page/販売.md "wikilink")されることはなかった。ただし、開発環境などが同梱された MSX-DOS Tools というパッケージはあった。

BIOSと拡張されたシステムコールは併せてBDOSと呼ばれ、ディスクドライブのインターフェースカートリッジの[ROMに内蔵されているものを呼び出して実行している](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")。このためDISK-BASICからもBDOSの実行ができる。またDOSのままMSXのROM-BIOSやスロットの使用もできる。システムファイルはMSXDOS.SYS・[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")・[AUTOEXEC.BAT](https://ja.wikipedia.org/wiki/AUTOEXEC.BAT "wikilink")であり、MS-DOSにある[CONFIG.SYS](https://ja.wikipedia.org/wiki/CONFIG.SYS "wikilink")や、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")ーを記述するコマンドなどはない。MSXの特徴として、その柔軟かつ強力なBIOSシステムによって拡張機器にはBIOSが搭載されており、接続すると自動的にBIOSが組み込まれるため、デバイスドライバー等の組み込みは構造上必要なかった。現在までに存在したほぼ唯一の、本来の意味での真のプラグ＆プレイを実現できていた環境と言われる所以である。

構造的な特徴としては、MSXの強力なBIOSシステムおよびそれらを共有するMSX-BASIC環境との間に、次のような親和性の高さがある。

  - コマンドプロンプトから互いの[環境](../Page/環境.md "wikilink")を行き来することが可能。
  - DOSとBASICの双方で単一のファイルフォーマット（FAT12ファイルシステム）を使用。
      - これにより MS-DOS を使用したパソコンと、同じフロッピー・ディスクでデータをやり取りできる。
        ただし、MS-DOS で作成されたディスクのサブディレクトリーは認識できるが（DIR コマンド等で表示可能）、アクセスは不可能である。したがって MS-DOS とデータをやり取りする場合は、ルート・ディレクトリーにファイルを置く必要がある。
      - なお、[MSX DISK-BASICでもファイルシステムにはFAT](https://ja.wikipedia.org/wiki/MSX_DISK-BASIC "wikilink")12を採用。
  - MSX-DOS上のアプリケーションからBIOSを、MSX-BASIC環境からMSX-DOSのBDOSを利用可能。
  - CP/M用のアセンブラー(M80)やコンパイラー等を用いてコーディングする際にもMSX用のBDOSやBIOSをシームレスに利用可能。

これにより、当時の8bitコンピューター用のDOS環境としては破格の機能と柔軟性を確保した上で、豊富なCP/Mのアプリケーションやデータおよび知見なども活かすことが可能だった。

ファイルの時刻の管理はパソコンの本体にカレンダー時計機能があればそれを利用し、なければ起動時に日付を入力するようになっている。

MSX-DOSは4台までのフロッピーディスクのほか[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")などにも対応。ただしファイルシステムが[FAT12](https://ja.wikipedia.org/wiki/FAT12 "wikilink")相当であるため、ドライブ1パーティションあたりの容量は最大32MBまでという限界がある。また[ドライブレター](https://ja.wikipedia.org/wiki/ドライブレター "wikilink")もワークエリアの容量の関係上、A:からH:までの最大8台分に限定され、MSX-DOSおよびMSX DISK-BASICで取り扱い可能なストレージの最大容量は32MB×8の256MBとなっている。なお、当時の[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")や[PC-9801](https://ja.wikipedia.org/wiki/PC-9801 "wikilink")などの一般的なMS-DOS環境に対応したESDIやSASIのHDDの容量は20～80MB程度であり、発売当時としてはこれだけの容量を管理できれば十分と言えた。

## MSX用以外のMSX-DOS

MSX-DOSは本来[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")用のオペレーティングシステムとして開発された[製品](../Page/製品.md "wikilink")である。しかし、マイクロソフトの[表計算](https://ja.wikipedia.org/wiki/表計算 "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である[マルチプラン](https://ja.wikipedia.org/wiki/マルチプラン "wikilink")を[日本電気](../Page/日本電気.md "wikilink")製の[PC-8800シリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")や[シャープ](../Page/シャープ.md "wikilink")製の[X1シリーズ](../Page/X1_\(コンピュータ\).md "wikilink")、[MZ-2500](https://ja.wikipedia.org/wiki/MZ-2500 "wikilink")シリーズに[移植する際にMS](https://ja.wikipedia.org/wiki/移植_\(ソフトウェア\) "wikilink")-DOSとの[ファイルの互換性が重視されたためMSX](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")-DOSは両[機種](https://ja.wikipedia.org/wiki/機種 "wikilink")にも[サブセット](https://ja.wikipedia.org/wiki/サブセット "wikilink")として移植され、専用の[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")ボードと組み合わせて販売された。MSX用のMSX-DOSと同様に、これらの移植版についてもMSX-DOSだけが個別に販売されることはなかった。

PC-8801とX1には、MS-DOS互換フォーマットやCP/Mをサポートする類似のOSとして[C-DOSがあった](https://ja.wikipedia.org/wiki/キャリーラボ "wikilink")。

パチンコ基板にも搭載された。MSXの総生産台数500万台に加え、パチンコ基板の年間生産台数420万台を握っていたことから、当時の日本のOSシェアのトップは実はMSX-DOSだったと元マイクロソフトの[古川享](https://ja.wikipedia.org/wiki/古川享 "wikilink")は指摘している\[2\]。

## 後継

### MSX-DOS2

**MSX-DOS2**（エム・エス・エックス・ドス・ツー）は[1988年](../Page/1988年.md "wikilink")に[MSX2](../Page/MSX2.md "wikilink")用にアスキーが開発し、OS単体（ディスク+カートリッジ）で販売したものである。因みに商品名は『日本語MSX-DOS2』

MSX-DOS2では、ファイルシステムにMS-DOS Version 2.11とほぼ同等の仕様の階層[ディレクトリ](../Page/ディレクトリ.md "wikilink")や[ファイルの特殊](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[属性](../Page/属性.md "wikilink")機能、[環境変数](https://ja.wikipedia.org/wiki/環境変数 "wikilink")と[パス](../Page/パス.md "wikilink")、[リダイレクトや](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")[パイプ](https://ja.wikipedia.org/wiki/パイプ "wikilink")などが追加されたほか、日本語表示(全角文字、漢字ROM)への対応や、マッパーRAM（[EMSに似た切り替え機構を備えた大容量](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink")[RAM](../Page/Random_Access_Memory.md "wikilink")）の管理ルーチンと、これを使用した[RAM DISKの機能が備え付けられた](https://ja.wikipedia.org/wiki/RAM_DISK "wikilink")。COMMAND.COMなどのヘルプ機能も充実した。同時に、MSX DISK-BASICの拡張もなされた。ファイルシステムはFAT12のままだが、後年ユーザー有志の手によるパッチを当てることによりFAT16のアクセスも一応可能となった。

専用の[ROMカートリッジには](../Page/ロムカセット.md "wikilink")、拡張されたBIOS/BDOSがROMに収められている。動作するために最低128KBのマッパーRAMが要求され、作業領域として32KBのRAMをマッパーRAMから確保する。そのため、内蔵増設RAMがあるものとないものの2つの[バージョン](https://ja.wikipedia.org/wiki/バージョン "wikilink")がある。RAMがあるものはカートリッジ内部でスロットを拡張しているため、セカンダリスロットでは動作しない。

なお、MSX-DOS2のROMカートリッジの内容は[MSXturboR](https://ja.wikipedia.org/wiki/MSXturboR "wikilink")では本体に内蔵された。

### MSX-DOS3

[2003年](../Page/2003年.md "wikilink")[11月30日](../Page/11月30日.md "wikilink")に行われた「MSXマガジンまつり」にて[西和彦](https://ja.wikipedia.org/wiki/西和彦 "wikilink")からコメントがあり、「[2HD](https://ja.wikipedia.org/wiki/2HD "wikilink")と[TCP/IPに対応し](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")にリリース予定」とされていた。1チップMSXのアスキーからの製品化が白紙になったこともあり、その後の状況は不明。

## MSX-DOSの主なアプリケーション

  - MSX-DOS TOOLS : CP/Mから移植したM80（[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")）、L80（[リンカ](../Page/リンケージエディタ.md "wikilink")）、MED（[エディタ](https://ja.wikipedia.org/wiki/エディタ "wikilink")）などの開発ツールをまとめたもの。
  - MSX-DOS2 TOOLS : MSX-DOS TOOLSの、DOS2専用の日本語（漢字）対応版。
  - MSX-SBUG : [シンボリックデバッガ](../Page/デバッガ.md "wikilink")
  - MSX-SBUG2 : MSX-SBUGの、DOS2専用の日本語（漢字）対応版。
  - MSX-C : MSX用の[C言語](../Page/C言語.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")（[LSI C](https://ja.wikipedia.org/wiki/LSI_C "wikilink")-80セルフ版相当）と、その[ライブラリ](../Page/ライブラリ.md "wikilink")。使用するにはDOS TOOLSが必要。

## MSX-DOS以外のMSX用DOS

MSXではMSX-DOS以外にも以下のOSが動作する。開発年順に列記する。

  - CP/M
  - [S-OS"SWORD"](https://ja.wikipedia.org/wiki/Oh!X#S-OS "wikilink")
  - UZIX
  - SymbOS
  - [Contiki](https://ja.wikipedia.org/wiki/Contiki "wikilink")
  - [Nextor](http://www.konamiman.com/msx/msx-e.html#nextor)

## 関連項目

  - [MSX-BASIC](../Page/MSX-BASIC.md "wikilink")
  - [HALNOTE](https://ja.wikipedia.org/wiki/HALNOTE "wikilink")
  - [MSX-VIEW](https://ja.wikipedia.org/wiki/MSX-VIEW "wikilink")

## 参照

[Category:マイクロソフト](https://ja.wikipedia.org/wiki/Category:マイクロソフト "wikilink") [Category:DOS](https://ja.wikipedia.org/wiki/Category:DOS "wikilink") [Category:MSX](https://ja.wikipedia.org/wiki/Category:MSX "wikilink") [Category:1984年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1984年のソフトウェア "wikilink")

1.
2.  [古川享のtweet](https://twitter.com/samfurukawa/status/4140922326)