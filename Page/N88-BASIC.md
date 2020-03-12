> この記事は[N88-BASIC](https://ja.wikipedia.org/wiki/N88-BASIC)から翻訳されています。


**N88-BASIC**（エヌはちはちベーシック）は、[NECの](../Page/日本電気.md "wikilink")[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")である[PC-8800シリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")および[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")に搭載され、標準[プログラミング言語](../Page/プログラミング言語.md "wikilink")として使用された[BASIC](../Page/BASIC.md "wikilink")言語の[処理系](https://ja.wikipedia.org/wiki/処理系 "wikilink")である。ロゴやマニュアル上では「N<small>88</small>-BASIC」と「88」を小さく書いており、これは各種バリエーションにおいても同様である。

[ブート](../Page/ブート.md "wikilink")時に[ROMから自動的に起動するものを](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")「[ROM-BASIC](../Page/ROM-BASIC.md "wikilink")」、専用[ディスクから起動してフロッピーディスクドライブ](../Page/ディスクメディア.md "wikilink")（[FDD](https://ja.wikipedia.org/wiki/フロッピーディスクドライブ "wikilink")）やハードディスクドライブ（[HDD](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")）を扱えるように機能拡張したものを「[DISK-BASIC](https://ja.wikipedia.org/wiki/DISK-BASIC "wikilink")」と呼んだ。また、俗称だが[MS-DOS](../Page/MS-DOS.md "wikilink")上で動作するものを「DOS-BASIC」と呼ぶこともあった。初期はROM-BASICのみでDISK-BASICは別売りだったが、FDDの普及によってDISK-BASICも標準添付されるようになり、MS-DOSの普及に伴ってDOS-BASICが開発され、MS-DOSが一般化するとDISK-BASICは再び別売り（末期にはサポート外）になった。MS-DOSが普及する以前は、DISK-BASICが簡易な[DOSとしての役割も担っていた](../Page/DOS_\(OS\).md "wikilink")。

## PC-8800シリーズ用

[N88BASIC_tenkey.gif](https://ja.wikipedia.org/wiki/File:N88BASIC_tenkey.gif "fig:N88BASIC_tenkey.gif") N88-BASICは、[1981年](../Page/1981年.md "wikilink")（昭和56年）に発表されたPC-8801に初めて搭載された[スタンドアロン](https://ja.wikipedia.org/wiki/スタンドアロン "wikilink")BASICで、[PC-8001に搭載されていた](../Page/PC-8000シリーズ.md "wikilink")[N-BASIC](../Page/N-BASIC.md "wikilink")の機能を大幅に拡張して作られた。一般的には[M-BASIC](../Page/Microsoft_BASIC.md "wikilink") 4.5として知られている[マイクロソフト](../Page/マイクロソフト.md "wikilink")のLevel-3 BASICインタプリタが基本設計（ベース）となっている。

N-BASICに対してある程度の[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")性を持ち、PC-8001で作られた[プログラムを実行させることも出来たが](../Page/プログラム_\(コンピュータ\).md "wikilink")、完全互換ではなかった。N-DISK BASICと[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")にも互換性があるが、[BASIC](../Page/BASIC.md "wikilink")の[中間コードは異なるので](../Page/中間言語.md "wikilink")、プログラムを交換する際には[アスキー形式で保存する必要があった](https://ja.wikipedia.org/wiki/ASCII "wikilink")。

N88-BASICには、PC-8800シリーズの機能拡張に合わせて、V1、V2のメジャーバージョンがある。V1は、V2の出現時に遡って付けられた呼称であり、もともとは「無印」であった。V2はPC-8801mkIISRから新規に搭載されたものである。アナログRGB採用によって表示色が大幅に増えた他、[FM音源](../Page/FM音源.md "wikilink")などの新機能も扱えるようになった。V1に対し、ほぼ完全な上位互換性を保っているが、ハードウェアの初期状態の違いにより、V1用のプログラムをV2で実行するとグラフィックの色が変わるなどの不都合が生じることがあった。

「タートルグラフィックス命令」も用意され、拡張モジュールをロードすると、[LOGO](../Page/LOGO.md "wikilink")を簡略化したような文法でグラフィックスを描画させる命令などが追加された。しかし、対応したソフトウェアが少ないもしくは利用頻度が低かったことなどから、PC-8801MH/FH以降の機種には搭載（バンドル）されなくなった。

V1およびV2対応の日本語拡張として、NECからN88-漢字BASICとN88-日本語BASICが、[システムソフト](../Page/システムソフト.md "wikilink")から8801漢字BASICと新8801漢字BASICが発売された。それぞれの間では2バイト文字の内部表現形式が異なっており、変換にはコンバータを必要とした。 これらはいずれも命令は通常のBASICコマンドで、日本語を文字列として扱えるようにしたものである。なお、N88-日本語BASICはPC-8801mkIIFR/MR以降の機種に標準添付されたが、PC-8800シリーズのCRTコントローラ([CRTC](../Page/CRTC_\(LSI\).md "wikilink"))はテキストVRAM上の2バイト文字に対応しておらず、従ってグラフィックVRAMにビットマップグラフィックとして文字を描画することになるため、動作が遅くプログラムを組む上ではあまり使われなかった。

### PC-88VA用

PC-88VAシリーズには、専用に新規開発された「N88-日本語BASIC V3」が標準添付された。V2までのN88-BASICに対し、ある程度の上位互換性を保っているが、完全上位互換ではない。ROM-BASICは無く、PC-Engineと呼ばれる独自OSから起動して使うもので、その意味ではスタンドアロンBASICでもない。機能的にもN88-BASICよりは、むしろN88-日本語BASIC(86)に近い。V3モードのCRTCは2バイト文字テキストに対応しているため、PC-88VA用のBASICとして広く使われるようになった。

標準で表示やファイル入出力などのデータとして[日本語](../Page/日本語.md "wikilink")を扱うことができ（[ぴゅう太](../Page/ぴゅう太.md "wikilink")の『G-BASIC』のように日本語でプログラミング出来る訳では無い。）、ハードウェア・[スクロール](../Page/スクロール.md "wikilink")や[スプライト](../Page/スプライト_\(映像技術\).md "wikilink")、[マウスや](../Page/マウス_\(コンピュータ\).md "wikilink")[メニューバー等も利用できた](../Page/メニュー_\(コンピュータ\).md "wikilink")。また、[音楽](../Page/音楽.md "wikilink")作成ソフト「インスタント・ミュージック」で作成した[ファイルを](../Page/ファイル_\(コンピュータ\).md "wikilink")[BGMとして鳴らしたり](../Page/バックグラウンドミュージック.md "wikilink")、[アニメ](../Page/アニメ.md "wikilink")作成ソフト「アニメフレーマー」で作成した[コンピュータアニメーション](https://ja.wikipedia.org/wiki/コンピュータアニメーション "wikilink")を再生することもできた。

## PC-9800シリーズ用

N88-BASIC(86)は、[1982年](../Page/1982年.md "wikilink")（昭和57年）から発売された[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")の[ROM-BASIC](../Page/ROM-BASIC.md "wikilink")で、PC-8800シリーズのN88-BASICと、高いレベルで互換性がある。名称の(86)は、採用した[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系[プロセッサ](../Page/プロセッサ.md "wikilink")に由来する。8ビット機時代のN-BASICとN88-BASICはNECとマイクロソフトの共同開発であったが、N88-BASIC(86)はNECのみによる独自開発である。

当初NECはマイクロソフトに開発を打診したが、8ビット機時代の「方言」の氾濫に手を焼き[標準化](../Page/標準化.md "wikilink")を画策していたマイクロソフトは、同社が16ビット機用の決定版として開発した[GW-BASICの採用を強く働きかけてきた](https://ja.wikipedia.org/wiki/Microsoft_BASIC#インタプリタ系 "wikilink")。しかし、GW-BASICは[IBM PC](../Page/IBM_PC.md "wikilink")[互換](https://ja.wikipedia.org/wiki/互換 "wikilink")[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")を前提としている上、[ラベルすら使えない旧態依然としたBASICであったため](https://ja.wikipedia.org/wiki/ラベル_\(プログラミング\) "wikilink")、N88-BASICで蓄積された膨大なソフトウェア資産を継承することは困難であり、NECはBASICを自社開発することによって独自路線を堅持する道を選択した。開発にあたってNECは、互換性を高めるためにN88-BASICの[リバースエンジニアリング](../Page/リバースエンジニアリング.md "wikilink")を行っている。当然ながら、完成したBASICにはN88-BASICと限りなく似た部分が存在し、マイクロソフトと衝突する可能性もあったわけであるが、最終的にはマイクロソフトから相当額の別の製品を購入することと、著作権の表示にマイクロソフトとNECの両社名を併記することで折り合った\[1\]。

N88-DISK BASIC(86)も発売され、N88-DISK BASICとディスクフォーマットは互換性がある。しかし、BASICの中間コードが異なるため、プログラム交換の際はアスキー形式で保存する必要があった。

その後、[日本語入力システム](../Page/日本語入力システム.md "wikilink")が追加されてN88-日本語BASIC(86)という名称になった。漢字の内部表現形式はN88-日本語BASICと異なっており、変換にはコンバータを必要とした。PC-9800シリーズのCRTCは2バイト文字テキストに対応しているため、N88-日本語BASIC(86)は広く使われるようになった。

PC-8800シリーズ用ほどバージョンは意識されないが、サポート対象ハードウェアの追加、日本語処理などのシステム拡張が行われている。最終バージョンは6.3。

### MS-DOS版

PC-9800シリーズのMS-DOSへの移行に伴い、N88-日本語BASIC(86)のMS-DOS版が発売された。MS-DOSでの[文字コード](../Page/文字コード.md "wikilink")の扱いに合わせるため、スタンドアロン版では同時に扱うことができたPC-9800シリーズ独自のセミグラフィック文字と2バイト文字が、CONSOLE命令で切り替える排他仕様になった。MS-DOS上でDISK-BASICとファイルを交換するためのコンバータがあったが、DISK-BASICでセミグラフィック文字と2バイト文字の両方を扱ったファイルをMS-DOSへ変換すると文字化けが発生した。

MS-DOS版にはBASIC[コンパイラ](../Page/コンパイラ.md "wikilink")も用意されたが、全てのプログラムがコンパイル可能というわけではなかった。またいわゆるネイティブコードを吐くコンパイラではなく、外見としては[実行ファイル](../Page/実行ファイル.md "wikilink")になるものの内部的には[中間表現](../Page/中間表現.md "wikilink")で、実行にはその中間表現のインタプリタを含んだ200KB近い[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")が必要であった。

MS-DOS版の最終バージョンは6.2で、6.3は発売されていない。DISK-BASICにおける6.2と6.3の違いは、（当時における）新しい規格のハードディスクへの対応であり、ディスクアクセスをMS-DOS経由で行うDOS-BASICは拡張の必要がなかったためである。

## MS-Windows版

MS-Windows版であるN88-BASIC(WN)インタプリタも発売されたが、極端に動作速度が遅く、画面周りの互換性も乏しかったため、実用的とはいえず普及しなかった。MS-Windows 2.xx向けのものであり、MS-Windows 3.0以降ではスタンダードモードでもエンハンストモードでも動作しない。[リアルモードではかろうじて動作したが](https://ja.wikipedia.org/wiki/リアルモード_\(Windows_3.0\) "wikilink")、フリーエリアがほとんど無かった。

## 互換BASIC

  - EPSON DISK BASIC
    PC-9800[互換機](../Page/互換機.md "wikilink")であった[EPSON製PCで](../Page/EPSON_PCシリーズ.md "wikilink")、N88-BASIC[ソフトウェア](../Page/ソフトウェア.md "wikilink")資産を利用できるよう開発された処理系。
  - BASIC/98
    有限会社 電脳組が販売するWindowsベースのインタプリタ。互換性はかなり高い。
  - 99Basic
    Windowsベースの[フリーウェア](../Page/フリーウェア.md "wikilink")。互換性は高い方ではないが、インタプリタとしては高速。
  - N88互換BASIC
    Windowsベースのフリーウェア。互換性は高い方だが、動作は遅い。
    「[N88互換BASIC for Windows(3.1)](http://www.vector.co.jp./soft/win31/prog/se025866.html)」と「[N88互換BASIC for Windows95](http://www.vector.co.jp./soft/win95/prog/se055956.html)」がある。

## 脚注

[Category:日本電気の製品](https://ja.wikipedia.org/wiki/Category:日本電気の製品 "wikilink") [Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink")

1.