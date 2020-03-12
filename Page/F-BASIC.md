> この記事は[F-BASIC](https://ja.wikipedia.org/wiki/F-BASIC)から翻訳されています。


**F-BASIC**（エフベーシック）は、[富士通](../Page/富士通.md "wikilink")が自社の[パソコンブランドである](../Page/パーソナルコンピュータ.md "wikilink")[FMシリーズに搭載した](https://ja.wikipedia.org/wiki/富士通#パーソナルコンピュータ "wikilink")[BASIC](../Page/BASIC.md "wikilink")言語。マイクロソフト系BASICに由来する命令セットを持つ。

## 8ビット機用

  - F-BASIC V1.0 （[FM-8](../Page/FM-8.md "wikilink")）
    マイクロソフト製6809用BASICをベースに開発された最初のF-BASIC。当時は「FUJITSU MICRO 8 BASIC」と称していた。
  - F-BASIC V2.0 （FM-8）
    8インチ/5.25インチ[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")版でのみ提供されたバージョン。変数の内容を保持したままでのプログラム連結実行のための`CHAIN`文/`COMMON`文、配列を消去する`ERASE`文、プリンタ出力のための`LLIST`文/`LPRINT`文/`LPRINT USING`文/`LPOS`関数、`PRINT USING`文/`LPRINT USING`文での書式制御文字列の追加、`OPEN`文でのプリンタに対するオプション指定の追加、ユーザープログラムの自動スタート機能などが追加された。また、文字列領域のガベージコレクションが改良され、文字変数1つあたり2バイト余計にメモリを必要とするようになったが、ガベージコレクション処理は大幅に高速化された。バリエーションとして128KBバブルカセットに対応したF-BASIC V2.2（128KBバブルカセットにより供給）が存在する。
  - F-BASIC V3.0 （[FM-7](../Page/FM-7.md "wikilink")/77シリーズ）
    F-BASIC V2.0を基にしたFM-7シリーズの標準BASIC。このバージョンから起動メッセージが「FUJITSU F-BASIC」となる。カラーパレット機能を制御する`COLOR=`文、マルチページ機能を制御する`SCREEN`文、[MMLによる音楽演奏を行う](../Page/Music_Macro_Language.md "wikilink")`PLAY`文、[PSGの直接制御を行う](../Page/Programmable_Sound_Generator.md "wikilink")`SOUND`文などが拡張された。バブルカセットに対する`BUBINI/BUBR/BUBW`文及びアナログポートに対する`ANPORT`関数は削除された\[1\]。バリエーションとして1MBフロッピーディスクに対応したF-BASIC V3.1（3.5インチフロッピーディスクにより供給）が存在する。
  - F-BASIC V4.0 （[FM-11](../Page/FM-11.md "wikilink")ST/AD/EX）
    メモリマッピングレジスタを活用するようになり、F-BASICインタプリタが巨大化し、テキストエリアも拡大された。画面編集の方式が今までのスクリーンエディタ的な編集のほか、他メーカー機同様にRETURNキーを押した行が入力したのと同じ効果をもつようになった。640x400ピクセルのグラフィックモードの追加、[BREAKキー](https://ja.wikipedia.org/wiki/BREAKキー "wikilink")をコントロールする`STOP ON/OFF`文、漢字表示のための`KANJI`文、外字登録のための`DEF KANJI`文、式の評価をファイルに出力する`WRITE/WRITE#`文、テキスト画面の色やアトリビュートを設定する`COLOR@`文、漢字のグラフィック画面への拡大描画を行える`SYMBOL@`文、グラフィック画面のハードウェアスクロールが可能な`ROLL`文、テキスト画面上に時刻を表示する`CLOCK ON/OFF`文、ライトペン割り込み制御の`PEN`文/`ON PEN GOSUB`文、`PEN ON/OFF/STOP`文が追加された。また、`AUTO`文での注釈行自動発生機能、`HARDC`文でのテキスト画面・グラフィック画面個別のハードコピー、`SCREEN`文での画面モード指定、`LINE`文でのラインスタイル指定、`PAINT`文でのタイルペイント対応、`SIN/COS/TAN`などの数学関数の倍精度演算化が行われた。このバージョンから文字列領域とスタックバッファの扱いが逆になり（文字列領域はメモリがある限り確保、スタックバッファは`CLEAR`文で確保される）、それに伴い`CLEAR`文の文法も変更された。基本的にBASICインタプリタはフロッピーディスクからRAM領域に展開されるが、ディスクドライブを標準装備していないFM-11STでは起動時に専用のROMカードからRAM領域にBASICインタプリタを展開する方式となった。バリエーションとして128KBバブルカセットに対応したF-BASIC V4.2、ハードディスクに対応したF-BASIC V4.3が存在する。
  - F-BASIC V5.0 （FM-11AD2/AD2+）
    F-BASIC V4.0の日本語文字列対応版。プログラムに（JISコードではなく）直接日本語文字列を記述できるようになる。また、それに関連した日本語文字列操作関数も追加された。このバージョンからアナログポートに対する`ANPORT`関数が正式に削除された。
  - F-BASIC V3.5 （[FM-77](https://ja.wikipedia.org/wiki/FM-7#FM-77 "wikilink")、FM-77L4）
    FM-77用400ラインカード（オプション。FM-77L4は標準装備）に対応したBASIC。ほぼF-BASIC V5.0のFM-77版といえるもので、画面モードは単色のみながら日本語文字列にも対応された。FM-77はライトペンに対応していないため`PEN`文は削除された。400ラインセット付属の192KB RAMカードを装着した場合には、RAMディスクが使用できる。
  - F-BASIC V3.3L10〜L12 （[FM77AVシリーズ](https://ja.wikipedia.org/wiki/FM-7#FM77AV "wikilink")）
    F-BASIC V3.5をベースに開発されたFM77AV専用のF-BASICでAudio/Visual機能が強化されており、320x200ピクセル4,096色モードやスーパーインポーズ機能、ビデオディジタイズ機能などが使えるようになり、`PLAY`文/`SOUND`文のFM音源やMIDIへの対応などが行われた。画面編集の方式がF-BASIC V3.0までと同様のものに戻ったほか、日本語文字列にも対応していないため、F-BASIC V5.0/V3.5に存在した`KANJI/ROLL/CLOCK`文および日本語文字列操作関数などは削除された\[2\]。FM-77+拡張RAMカードでも起動できたが、FM77AV独自機能が使用出来ないよう制限がかけられていた。
  - F-BASIC V3.3L20 （FM77AVシリーズ）
    F-BASIC V3.3L10に2DDフロッピーディスクサポート、日本語文字列対応機能、内蔵RS-232Cインタフェースのボーレート制御機能などを追加したバージョン。日本語モード切り換えのための`KANJI ON/OFF`文、RS-232Cインタフェースのボーレート制御のための`BAUD`文が追加された\[3\]。日本語モード対応に伴い、F-BASIC V3.3L10で削除された日本語文字列操作関数および`SYMBOL@`文が復活した。
  - F-BASIC V3.4L10 （FM77AV40）
    F-BASIC V3.3L20に640x400ピクセル8色モード、320x200ピクセル262,144色モードを追加したバージョン。このバージョンから日本語モードでの各種メッセージが日本語化されるようになる。オプションの拡張RAMカード-256を搭載したうえでセットアップユーティリティにより所定の設定を行うと、RAMディスクが使用できる。
  - F-BASIC V3.3L30 （FM77AVシリーズ）、V3.4L20〜21 （FM77AV40シリーズ）
    F-BASIC V3.4L10をベースに開発されたF-BASIC。日本語モードでの漢字表示が従来比約2倍に高速化され、FM77AV20EX/40EXでのMMR使用時のクロックダウンが抑制されるほか、FM77AV40/20EX/40EXではフロッピーディスクアクセスにDMAコントローラを利用するようになり、音楽演奏中のディスクアクセスによるテンポ遅れが解消された。また、リセットせずに使用ドライブ/ファイル数を切り替えられる`NEW ON`文が追加された。FM77AV40/40EXでRAMディスクを使用している場合、V3.4L10ではリセットごとに内容が初期化されていたが、V3.4L20では内容が保持されるようになった。なお、このバージョンからデータレコーダのサポートが削除された。この2つのバージョンは起動プロセス、起動メッセージおよびバージョンスタンプ情報を除き、極力コードの統一化が図られた。バリエーションとして、レベルアップサービスによって提供された400ラインモードおよび262,144色モード用サブシステムコードを含むFM77AV40専用版のF-BASIC V3.4L20\[4\]、FM77AV40SXに付属したF-BASIC V3.4L21が存在した。F-BASIC V3.4L21はF-BASIC V3.4L20のバグ修正版にして8ビット機F-BASICの最終バージョン。F-BASICインタプリタ内部のエントリアドレスが一部異なるため、F-BASIC V3.4L20の拡張BASICが使えない場合が存在した。

当時としては画像や音声を扱う機能が豊富であった。

共通点として、コマンド画面では行ごとにRETURNキーを押さなくても画面上の全変更行が更新されたため、比較的スクリーンエディタ風の編集が出来た。

F-BASIC V1.0/V3.0では、本体内蔵のROM BASICにはフロッピーディスク用の命令等が含まれておらず、ディスク使用時には別売の[DISK-BASIC](https://ja.wikipedia.org/wiki/DISK-BASIC "wikilink")を購入して起動時に読み込ませる必要があった。このディスク拡張部分は本体RAMの上位アドレス部分（ROM領域の直前）に展開され、ROM BASICの命令と同じように使用することができた。F-BASIC V2.0以降で拡張された命令も同様の仕組みで実装されている。

後にこの部分の仕様が解析されると、ユーザが独自に新たな命令を定義してBASICを拡張することが可能であることが判明したため、『[I/O](https://ja.wikipedia.org/wiki/I/O_\(雑誌\) "wikilink")』（[工学社](../Page/工学社.md "wikilink")）や『[Oh\!FM](../Page/Oh!FM.md "wikilink")』（[日本ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンククリエイティブ "wikilink")）等の専門誌ではユーザやライターらが開発した拡張命令等がほぼ毎月のように掲載されるようになった。

## 16ビット機用

  - F-BASIC86 V1.0 （FM-11）
    16ビット化（[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")-86上で動作）。F-BASIC V5.0の8086コード版といえるもので、CPUやOSの違いから`DEF SEG`文や`INP`関数、`OUT`文、`SYSTEM`文などが追加されているが、`PLAY`文・`SOUND`文は割愛されているほか、データレコーダのサポートが削除されている。
  - F-BASIC86 V2.0/V2.1 （[FM16βシリーズ](https://ja.wikipedia.org/wiki/FM-16β "wikilink")）
    [CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")-86上で動作。日本語モードへの切り替え命令が`SCREEN 6`文から`KANJI ON/OFF`文に変更されている。日本語モードでの各種メッセージが日本語化されている。ワールド座標に対応したほか、`CIRCLE`文のアルゴリズムが変更され従来よりきれいな円を描画することができるようになっており、`LINE`文、`CIRCLE`文の塗りつぶしを枠と別の色（タイルパターンも使用可能）で塗りつぶす機能に対応した。`OPEN`文の文法としてNECのN88-BASIC同様の書式が使用可能となっている。8ビット機用F-BASICフォーマットのフロッピーディスクの読み書きにも対応している。後に発売されたFM16βSDではフリーエリアの減少を最低限にとどめるため、F-BASIC86 V2.1をCPUカード上のROMに搭載しており、FM-16βFD/HDにおいても同バージョンのフロッピーディスクによる供給が行われた。
  - F-BASIC86 V2.1 （[FM16π](https://ja.wikipedia.org/wiki/FM16π "wikilink")）
    FM16β用F-BASIC V2.1のサブセット仕様。ROMカートリッジにより供給される。
  - F-BASIC86 V3.1 （FM16βシリーズ、[FMRシリーズ](../Page/FMRシリーズ.md "wikilink")）
    MS-DOS上で動作。基本的にF-BASIC86 V2.1のMS-DOS版といった感じだが、日本語変数名への対応、BASICの文法を国語化する`KOKUGO ON/OFF`文、チャイルドプロセスを呼び出す`CHILD`文などが追加されている。8ビット機用F-BASICフォーマットのフロッピーディスクの読み書き機能は削除され、外部ツールを利用する形となった。
  - F-BASIC86HG （FM16βシリーズ、FMRシリーズ）
    MS-DOS上で動作。F-BASIC86 V3.1を大幅に拡張しサブプログラムの概念を導入したものだが、中間コードに互換性がないためF-BASIC86 V3.1のプログラムを実行するには付属のユーティリティを使用する必要がある。

## 32ビット機用

  - F-BASIC386 （[FM TOWNS](../Page/FM_TOWNS.md "wikilink")）
    実行画面とは独立したスクリーンエディタを装備。[スプライトや](../Page/スプライト_\(映像技術\).md "wikilink")[サウンド](https://ja.wikipedia.org/wiki/サウンド "wikilink")などの機能が拡張された。[コンパイラ](../Page/コンパイラ.md "wikilink")（V1.1L21〜）も発売された。V2.1からは構造化に対応した。
    [隠しコマンド](../Page/隠しコマンド.md "wikilink")のほか、`BEEP &HFB386`というコマンドを実行すると隠しドキュメントが表示されるという[イースター・エッグがある](../Page/イースター・エッグ_\(コンピュータ\).md "wikilink")\[5\]（V2.1L20で実行すると、前述の隠しコマンドの解説が表示される\[6\]）。
  - GearBASIC （FM TOWNS用のGUI式の開発環境。[TownsGEAR](../Page/TownsGEAR.md "wikilink")のスクリプト）
    行番号がない。
    TownsGEARのV2.1L20以後には付属マニュアルに記載されていない拡張命令が存在し、[TownsシステムソフトウェアのCD](https://ja.wikipedia.org/wiki/FM_TOWNS#Townsシステムソフトウェア "wikilink")-ROMに収録されているドキュメントファイルにそれに関する記述がある\[7\]。

『[Oh\!FM TOWNS](../Page/Oh!FM.md "wikilink")』1992年8月号のアンケートの集計結果によると、FM TOWNSユーザーのF-BASIC386所有率は半数以上に達していた\[8\]。

## Windows用

特定の機種用の言語であったF-BASICだったが、Windows上で動作するバージョンも登場した。

  - F-BASIC コンパイラ for [Windows 3.1](https://ja.wikipedia.org/wiki/Windows_3.1 "wikilink")
    Microsoft Windows環境でコンパイルして使用可能。Visual Basicでは必須だった[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")を必要としない実行ファイルを生成できた。
  - F-BASIC V4.1 ([Windows 95](https://ja.wikipedia.org/wiki/Windows_95 "wikilink"))
    F-BASIC97 V5.0 (Windows 95、[Windows NT4.0](https://ja.wikipedia.org/wiki/Windows_NT4.0 "wikilink"))
    F-BASIC V6.0 (Windows 95、[Windows 98](https://ja.wikipedia.org/wiki/Windows_98 "wikilink")、Windows NT4.0)
    F-BASIC V6.3 (Windows 95、Windows 98、Windows NT4.0、[Windows 2000](https://ja.wikipedia.org/wiki/Windows_2000 "wikilink")、[Windows Me](https://ja.wikipedia.org/wiki/Windows_Me "wikilink"))
    [MS-DOS](../Page/MS-DOS.md "wikilink") BASIC（[N88-BASIC](../Page/N88-BASIC.md "wikilink")）のプログラムをWindowsに移行でき、[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")コントロールで構成されている。F-BASIC97 V5.0のみ名称に「97」が入っているのは、FM-11用F-BASIC V5.0とのバージョン番号の重複を回避するためである。

何度かバージョンアップが行われたものの、[Windows XPはサポートされないまま](../Page/Microsoft_Windows_XP.md "wikilink")、[2006年](../Page/2006年.md "wikilink")3月末をもって販売を終了した\[9\]。最終バージョンは6.3\[10\]。

従来のF-BASICに近い「手続き型」のほか、[Microsoft Visual Basicに近く](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")、Windowsの[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")を使った「イベント駆動型」での開発が可能。

しかし設計はあまり洗練されておらず、GUIの部品にアクセスするには、ATTACH命令で変数と部品を接続しなければならないうえ、Visual BASICのような「プロパティ」の概念がなく、複雑な名前の命令を呼ぶ必要があるなど、煩雑で扱いにくいプログラムになりがちであった。例としてテキストボックスのテキストを変更するプログラムは、Visual BASICでは`Text1.Text = "Wikipedia"`と書くだけで良いのに対して、F-BASICでは以下のように書く必要がある。

``` vb
COMMON SHARED TEXT1 AS OBJECT
TEXT1.ATTACH GETDLGITEM("TEXT1")
TEXT1.SETWINDOWTEXT "Wikipedia"
```

## 脚注

<references />

## 参考文献

  - 『[Oh\!FM](../Page/Oh!FM.md "wikilink")』 1988年3月号 [日本ソフトバンク](../Page/SBクリエイティブ.md "wikilink") 特集:比較F-BASIC学 入門 こんなにあったF-BASICのバージョン F-BASICの変遷を考える〔緒方 渉〕

## 外部リンク

  - [F-BASIC V6.3 情報](http://www.fmworld.net/product/soft/fbasic/) - 富士通株式会社

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:富士通の製品](https://ja.wikipedia.org/wiki/Category:富士通の製品 "wikilink")

1.  ただし予約語としては残っている。公式発表ではANPORT関数は削除されたことになっているが、実際は処理も残っている。
2.  ただし予約語としては残っている。
3.  BAUDの中間コードにBUBINIと同じコードを使用したため、BUBINIはV3.3L20/L3.4L10以降予約語からも削除されている。
4.  FM77AV40は本体に400ラインモードおよび262,144色モード用サブシステムをROMとして持っていなかったため、FM77AV40EX版とは別に用意された
5.  「F-BASIC386の隠し機能\!」『[Oh\!FM TOWNS](../Page/Oh!FM.md "wikilink")』1994年12月号、75頁。
6.
7.  『Oh\!FM TOWNS』1993年11月号（表記上は「秋の特別号」）、54頁。
8.  『Oh\!FM TOWNS』1993年10月号、49頁。
9.
10.