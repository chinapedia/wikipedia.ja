> この記事は[Video Graphics Array](https://ja.wikipedia.org/wiki/Video_Graphics_Array)から翻訳されています。


**Video Graphics Array**（ビデオ グラフィックス アレイ、略称:**VGA**）は、[IBM](../Page/IBM.md "wikilink")が[EGAの後継として](../Page/Enhanced_Graphics_Adapter.md "wikilink")、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に発表した表示回路規格である。代表的な表示モードに 640×480 [ピクセル](../Page/ピクセル.md "wikilink")・16色がある。転じて、640×480 ピクセルの[画面解像度](../Page/画面解像度.md "wikilink")を俗に「VGA」と呼ぶようにもなった。

## 歴史

[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")にIBMの[パーソナルコンピューター](https://ja.wikipedia.org/wiki/パーソナルコンピューター "wikilink")である[IBM PS/2に初めて搭載された](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")。PS/2では[マザーボード](../Page/マザーボード.md "wikilink")上に搭載されていたが、その後、[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")用に[ATバス用VGAカードも発売された](../Page/Industry_Standard_Architecture.md "wikilink")。各社の[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")でも、VGAおよび[SVGA](../Page/Super_Video_Graphics_Array.md "wikilink")（VGA上位互換の表示回路規格の総称）が普及し、事実上の標準となった。

## 機能

[サムネイル](https://ja.wikipedia.org/wiki/File:Birds_VGA16.png "fig:サムネイル") [サムネイル](https://ja.wikipedia.org/wiki/File:Birds_VGA256.png "fig:サムネイル") VGAは英数テキストモードおよびAPA（*All Points Addressable*、全点アドレス割り当て可能）グラフィックモードをサポートする。

### グラフィックモード

標準のグラフィックモードは次の4つが存在する。このうち、640×480の縦横比は当時のテレビの縦横比に近く、[マルチメディア](../Page/マルチメディア.md "wikilink")を想定した設計と言われている。

  - 640×480ドット、16色またはモノクロ\[1\]。（後者はIBM [MCGA規格と同等](../Page/Multicolor_Graphics_Adapter.md "wikilink")。）
  - 640×350または640×200ドット16色またはモノクロ（[EGA互換モード](../Page/Enhanced_Graphics_Adapter.md "wikilink")）
  - 320×200ドット、4色または16色
  - 320×200ドット、256色（モード13h）

640×480ドット16色および320×200ドット256色モードは完全に再定義可能なパレットを持ち、それぞれ18ビット（262,144色）のRGBテーブルから色を選択する。もっとも、高解像度モードは[Microsoft Windows上の固定パレットでの使用をきっかけに一般化した](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[2\]。他のカラーモードはEGAまたは[CGA互換のパレット](../Page/Color_Graphics_Adapter.md "wikilink")（プログラム用に64色テーブルから16色EGAパレットを再定義する機能を含む）に準じるが、VGA特有のプログラム手法を用いることで再定義することも可能である。

今日ではCGA/EGAとの互換機能は忘れ去られ、変換アダプタが用途不明の商品として出回っていたこともある\[3\]。 なお、規格制定者の意図は不明だが9ピンのVGA端子とCGA/EGAはピンアサインが異なり変換アダプタも相互利用は出来ない\[4\]。

### テキストモード

  - 80字×25行、9×16ドットフォント、有効解像度は720×400ドット、16色またはモノクロ。後者は旧来の[MDAベースのアプリケーションと互換性がある](../Page/Monochrome_Display_Adapter.md "wikilink")。
  - 40字×25行、同じフォントサイズを持ち、有効解像度は360×400ドット。
  - 80字×43行、80字×50行（8×8ドットフォント）16色、有効解像度は640×344（EGA互換）または640×400ドット。

この他にも画面解像度や画面モードをカスタマイズすることで様々な表示モードの画面信号を生成できる。

## 技術詳細

[サムネイルのVGAとその周辺回路](https://ja.wikipedia.org/wiki/ファイル:IBM_VGA_90X8941_on_PS55.jpg "wikilink")\]\]

### 回路設計

VGAの"A"は従来の"adapter"に代わって"array"を指しており、初めからシングルチップ（[ASIC](../Page/ASIC.md "wikilink")）として実装された。これは[Motorola 6845ビデオアドレス発生器だけでなくMDA](../Page/CRTC_\(LSI\).md "wikilink")、CGAおよびEGAのフルサイズ[ISAボードの機能をカバーするいくつものディスクリート論理チップを置き換えるものであった](../Page/Industry_Standard_Architecture.md "wikilink")。このシングルチップ実装によってVGA機能は、[ビデオメモリ](../Page/VRAM.md "wikilink")、タイミング発生器（[クロック発振器](../Page/発振回路.md "wikilink")）、外部[RAMDAC](https://ja.wikipedia.org/wiki/RAMDAC "wikilink")だけ用意すれば、PC本体の[マザーボード](../Page/マザーボード.md "wikilink")に最小限の労力で搭載することができ、部品点数が減ったことで信頼性も向上した\[5\]。その結果、最初の[IBM PS/2モデルはマザーボード上にVGAが搭載された](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")。これは、全てのIBM PCデスクトップモデル（[PC](../Page/IBM_PC.md "wikilink")、[PC/XT](https://ja.wikipedia.org/wiki/PC/XT "wikilink")、[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")）がモニターに接続するためにディスプレイアダプターをスロットに装着する必要があったことに比べると、対照的であった。

### 仕様

[サムネイル](https://ja.wikipedia.org/wiki/File:Vector_Video_Standards2.svg "fig:サムネイル") オリジナルのVGAの仕様は次の通りである。

  - 256KBのビデオメモリ（初期のVGAカードは64KB、128KBのRAMを搭載し、いくつか、または全ての高解像度16色モードが省略された。）
  - 16色および256色パレットの表示モード
  - 262,144色グローバルパレット（赤・緑・青各色が6ビット・64階層のRAMDACを使用）
  - 25.175MHz\[6\]または28.322MHzから選択可能なマスターピクセルクロック
  - 通常の水平同期周波数は31.469kHz固定
  - 最大800水平ピクセル\[7\]
  - 最大600垂直ライン\[8\]
  - 最高70Hz\[9\]の[リフレッシュレート](../Page/リフレッシュレート.md "wikilink")（垂直同期）
  - 垂直ブランク[割り込み](../Page/割り込み_\(コンピュータ\).md "wikilink")（全ての互換カードがサポートしているわけではない。）
  - プレーンモード、最高16色（4ビットプレーン）
  - パックドピクセルモード、256色（モード13h）
  - ハードウェアスムーススクロールサポート
  - ハードウェア[スプライトは非搭載](../Page/スプライト_\(映像技術\).md "wikilink")
  - ブリッターは非搭載だが、VGAラッチレジスタによる高速データ転送をサポート
  - いくつかの"Raster Ops"をサポート
  - [バレルシフタ](../Page/バレルシフタ.md "wikilink")をサポート
  - 分割画面をサポート
  - 0.7Vピーク電圧幅\[10\]
  - 75Ω二重終端[インピーダンス](../Page/インピーダンス整合.md "wikilink")

標準モードと同様に、VGAはそれまでのEGA、CGA、MDAの様々なモードをエミュレートするよう設定することができる。互換性は[BIOSレベルで完全に持っているが](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、[レジスタレベルでもなお高い互換性を持っている](../Page/レジスタ_\(コンピュータ\).md "wikilink")。VGAは[IBM PCjrまたは](https://ja.wikipedia.org/wiki/IBM_PCjr "wikilink")[Herculesの特殊な表示モードとは](../Page/Hercules_Graphics_Card.md "wikilink")（解像度・色・リフレッシュレート・メモリが十分であっても）直接の互換性はなく、これらのモードのエミュレーションはソフトウェアによって代替された。

### 信号タイミング

VGAの水平同期周波数の標準値は[NTSC](../Page/NTSC.md "wikilink")-M表示システムで使われている数値のちょうど2倍である。これはVGAの開発時点ではオプションのテレビ出力機構やVGA-TV変換ボックスの提供を容易にする意図があった。VGA水平同期周波数の公式は (60 ÷ 1001) × 525 kHz = 4500 ÷ 143 kHz ≈ 31.4685 kHz。VGAカードで使われる全ての他の周波数はこの値の整数倍または分周数で供給される。[水晶振動子](../Page/水晶振動子.md "wikilink")の精度の限界により、実際のカードはこれより若干高く、あるいは低くなる。

全てのVGA供給タイミング（つまり、25.2MHzまたは28.3MHzのマスタクロックと31.5kHzの水平レートを使用するもの）はVGAファームウェアインターフェースを介さずにVGAハードウェアに直接アクセスすることで、ソフトウェアによって幅広く変化させることができた。多くの[MS-DOS](../Page/MS-DOS.md "wikilink")ベースのゲームソフトがこれを行っていた。しかし、標準モードのみ、または最低でも標準モードの一つと同じ水平同期・垂直同期タイミングを使用しているモードのみが、1980年代後期から1990年代前期のオリジナルのVGAモニターで動作すると保証されていた。他のタイミングを使用すると、そのモニターに損傷を与える恐れがあり、故に基本的にソフトウェアメーカーはこれを避けていた。後のマルチシンク[CRTモニターはより柔軟で](../Page/ブラウン管.md "wikilink")、[SVGAグラフィックカードとの組み合わせによって](../Page/Super_Video_Graphics_Array.md "wikilink")、完全に任意の同期周波数とピクセルクロック周波数でより幅広い解像度やリフレッシュレートを表示することができた\[11\]。

最も一般的なVGAモード（640x480ドット、60Hzノン[インターレース](../Page/インターレース.md "wikilink")）について、水平同期タイミングは次のようになっている。\[12\]\[13\]

| パラメーター        | 値      | 単位                                                          |
| ------------- | ------ | ----------------------------------------------------------- |
| ピクセルクロック周波数   | 25.175 | [MHz](https://ja.wikipedia.org/wiki/Hertz "wikilink")\[14\] |
| 水平周波数         | 31.469 | [kHz](https://ja.wikipedia.org/wiki/Hertz "wikilink")       |
| 水平ピクセル数       | 640    |                                                             |
| 水平同期信号の極性     | 負極性    |                                                             |
| 1ラインあたりの合計時間  | 31.778 | [µs](https://ja.wikipedia.org/wiki/1_E-6_s "wikilink")      |
| フロントポーチ (A)   | 0.636  | µs                                                          |
| 同期パルス長 (B)    | 3.813  | µs                                                          |
| バックポーチ (C)    | 1.907  | µs                                                          |
| アクティブピクセル (D) | 25.422 | µs                                                          |

水平同期と空白時間の合計 = 6.356us、A=16、B=96、C=48、D=640で、1ライン=800ピクセル。この画像に示されている図は正確ではなく、上の表とは完全には一致しない。

これらのタイミングは高周波数モードでも同じだが、全てのピクセルは9/8倍になる。つまり、アクティブ720ピクセル、1ラインあたり900ピクセル、バックポーチ54ピクセル。

| パラメーター        | 値      | 単位                                                 |
| ------------- | ------ | -------------------------------------------------- |
| 垂直ライン数        | 480    |                                                    |
| 垂直同期信号の極性     | 負極性    |                                                    |
| 垂直周波数         | 59.94  | Hz                                                 |
| 1フレームあたり合計時間  | 16.683 | ms                                                 |
| フロントポーチ (A)   | 0.318  | [ms](https://ja.wikipedia.org/wiki/ミリ秒 "wikilink") |
| 同期パルス長 (B)    | 0.064  | ms                                                 |
| バックポーチ (C)    | 1.048  | ms                                                 |
| アクティブピクセル (D) | 15.253 | ms                                                 |

垂直同期と空白時間の合計は1.43ms、A=10、B=2、C=33、D=480で、1フレーム=525ライン。

### コネクタ

[Vga-cable.jpg](https://ja.wikipedia.org/wiki/File:Vga-cable.jpg "fig:Vga-cable.jpg")）\]\]  VGAはDE-15コネクタを使用している。

VGA機器と接続する別の方法として、信号品質を維持できる[BNCコネクタがある](https://ja.wikipedia.org/wiki/コネクタ#BNCコネクタ "wikilink")。これは赤、緑、青、水平同期、垂直同期の5本のケーブルをセットにして使う。BNCでは信号線が端から端まで完全にシールドされた状態になるので、[クロストーク](https://ja.wikipedia.org/wiki/クロストーク "wikilink")や外部ノイズの影響を受けにくい。

しかしながら、BNCコネクタはDE-15コネクタに比べると場所を取ってしまう。また、各ケーブルのコネクタを正しいソケットに接続するように注意しなければならない。BNCコネクタでは[VESA DDCがサポートされないため](https://ja.wikipedia.org/wiki/VESA_Display_Data_Channel "wikilink")、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")側でモニターの情報を得ることができない。従って、ユーザーはモニターがサポートする画面モードを把握した上で、オペレーティングシステムに適切な設定を施す必要がある。

BNCコネクタがVESA DDCに対応出来ない問題を解決するため、[カナレ電気](../Page/カナレ電気.md "wikilink")など各社から変換ケーブルに専用のコネクタを設けて対応している\[15\]ほか、EDIDエミュレータという機器を使うことで疑似的にVESA DDCと同じ信号を生成することで対処する\[16\]。

### アドレス割り当ての詳細

VGAのビデオメモリはPCの[リアルモード](../Page/リアルモード.md "wikilink")アドレス空間の[セグメント](../Page/セグメント方式.md "wikilink")0xA0000 - 0xBFFFF（セグメント:オフセット表記でA000:0000 - B000:FFFF）間の範囲にウィンドウとして割り当てられる。一般的に、これらの開始セグメントは次のようになっている。

  - 0xA0000 - [EGA](../Page/Enhanced_Graphics_Adapter.md "wikilink")/VGAグラフィックモード（64KB）
  - 0xB0000 - モノクロテキストモード（32KB）
  - 0xB8000 - カラーテキストモードおよび[CGA互換グラフィックモード](../Page/Color_Graphics_Adapter.md "wikilink")（32KB）

各モードで異なるアドレス割り当てを使用しているため、同じシステムに装着したモノクロアダプター（[MDAまたは](../Page/Monochrome_Display_Adapter.md "wikilink")[Hercules](../Page/Hercules_Graphics_Card.md "wikilink")）およびVGA、EGA、CGAカラーアダプターは共存できた。1980年代初めは、これはモノクロディスプレイで高解像度テキストに[Lotus 1-2-3シートを表示すると同時に低解像度CGAディスプレイ上に関連するグラフィックを表示するために使われた](../Page/Lotus_1-2-3.md "wikilink")。多くのプログラマーは、他のカードのグラフィックモードでプログラムを動かしている間、モノクロカードでデバッグ情報を表示させるといった構成を利用することもあった。[ボーランド](../Page/ボーランド.md "wikilink")の、、および[マイクロソフト](../Page/マイクロソフト.md "wikilink")のといった[デバッガ](../Page/デバッガ.md "wikilink")はデュアルモニター構成で動作させることができた。Turbo DebuggerまたはCodeViewはWindowsのデバッグにも使われていた。それらにはWindowsをデバッグするために使うox.sys（モノクロディスプレイ上の[シリアルインターフェースシミュレーション機能を実装している](../Page/シリアルポート.md "wikilink")）というDOSデバイスドライバーが存在し、実際の端末を使わずともデバッグ版Windowsからクラッシュメッセージを受け取ることができた。また、DOSプロンプトで「MODE MONO」コマンドを使うと出力をモノクロディスプレイに[リダイレクトすることができた](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")。モノクロアダプターが使われていないとき、0xB000-0xB7FFアドレス空間は他のプログラム用の追加メモリとして使うことができた。（例えば、[CONFIG.SYS](../Page/CONFIG.SYS.md "wikilink")に`DEVICE=EMM386.EXE I=B000-B7FF`を加えると、プログラムはこのメモリを[アッパーメモリブロックとして使用することができた](https://ja.wikipedia.org/wiki/Upper_Memory_Area "wikilink")。）

## 影響

### 世界

当時の[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")および[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")では、[CAD](../Page/CAD.md "wikilink")や[Lotus 1-2-3などの表計算など](../Page/Lotus_1-2-3.md "wikilink")、高解像度が必要とされる用途のために、IBM自身の[8514/A](https://ja.wikipedia.org/wiki/8514/A "wikilink")の他、EGAに独自の画面モードを追加した各種グラフィックチップや、EGAと共存できる高解像度グラフィックチップ（[Herculesなど](../Page/Hercules_Graphics_Card.md "wikilink")）が発売されていた。これらは独自の画面モード間の互換性は無く、それぞれ専用の（DOSまたはWindowsの）ドライバが必要だった。

VGAの登場により、VGA互換およびVGA上位互換のグラフィックチップ (Super VGA、SVGAとも言う) が普及し、VGAは[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")での事実上の業界標準となった。

このため、各種の[OSでもVGAを最小要件としたものが多い](../Page/オペレーティングシステム.md "wikilink")。また、表示関連の問題が発生した場合でもメーカーや機種を問わず表示できる共通画面モードのため、インストール時や非常用の画面で使われている。

PC/AT互換機用の[WindowsをセーフモードやVGAモードで起動すると](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、VGAの640×480ピクセル 16色画面モードで表示が行われる。

しかしディスプレイの高精細化が進んだこともあり、[Windows XP以上はSVGAにより表示される](../Page/Microsoft_Windows_XP.md "wikilink")。パソコン用ディスプレイとしては最低1024×768ピクセル、いわゆる[XGA相当の画面解像度が](../Page/Extended_Graphics_Array.md "wikilink")、最低ラインとして一般化した。[PDAのような小型の端末にもVGAと同等の画素数を搭載する例が見られる](../Page/携帯情報端末.md "wikilink")。[携帯電話](../Page/携帯電話.md "wikilink")端末では[SoftBank 904SHを皮切りとして](https://ja.wikipedia.org/wiki/SoftBank_904SH "wikilink")、高級機種を中心に高精細な液晶ディスプレイが搭載されている。

### 日本

日本では[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")の登場までは[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")自体が普及しておらず、VGAもDOS/Vと共に普及した。なお「DOS/V」の「V」は「VGA」から来ている。

日本語をグラフィック表示する[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")や、日本語Windowsの標準機能では、VGAの640×480ピクセル 1677万7216色中16色の表示モードを利用している。

この際に「[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")などの大半は640×400ピクセルだが、[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")は640×480なので、DOS画面では行間が開き、Windows上でも画面が広い」という比較が盛んに行われた。また、日本では最初からVGAが普及したため、DOS/V登場以前よりAT互換機に触っていたユーザーを除けば、VGAが下位の各種の画面モードを持っている事は余り知られていない。

[東芝](../Page/東芝.md "wikilink")の[J-3100](https://ja.wikipedia.org/wiki/J-3100 "wikilink")・[ダイナブックや](https://ja.wikipedia.org/wiki/ダイナブック_\(東芝\) "wikilink")、[AX](../Page/AX.md "wikilink")協議会の各社AXパソコン（[JEGAボードを搭載](../Page/Japanese_Enhanced_Graphics_Adapter.md "wikilink")）は、当初はEGAをベースに独自に日本語化していたが、後にVGAを採用し、更に[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")に移行した。

## 一般化した誤用

転じて、[画面解像度](../Page/画面解像度.md "wikilink")として640×480ピクセル表示のことをVGAと言うようになった。これは、誤用が一般化したものである。

例えば、[日本電気](../Page/日本電気.md "wikilink") (NEC) の[PC-9821シリーズ](../Page/PC-9821シリーズ.md "wikilink")や[富士通](../Page/富士通.md "wikilink")の[FM TOWNSも](../Page/FM_TOWNS.md "wikilink")、640×480ピクセルの解像度のモードを持っていたが、これらは別規格であり、「VGA」とは言わない。

また本来のVGAでは640×480画素での表示色数は16色のため、「640×480 256色」などは「VGA互換画面モード」と呼ぶのも正確ではなく、単に「VGAと同じ解像度」「VGA互換画素数表示」などと呼ぶのが妥当である。

[ビデオカード](../Page/ビデオカード.md "wikilink")一般を「VGAカード」と称するなど、コンピューターの画面出力＝VGAという誤用も散見される。VGAはあくまで、複数の画面モードを持っている、特定の画面表示規格であり、「VGAカード」という語は（本来であれば）その規格に沿っており、それらの画面モード（のみ）を持つビデオカード、を特に指して使われるべきである。

## 画像解像度としてのVGAの派生用語

  - VGA+（ブイジーエープラス）
    690×480ドットで、アスペクト比は23:16。NECが開発。自社製携帯電話端末に採用している。
  - ワイドVGA（ワイドブイジーエー、WVGA）
    800×480ドットで、アスペクト比は5:3。[日立製作所](../Page/日立製作所.md "wikilink")、東芝、[カシオ計算機](../Page/カシオ計算機.md "wikilink")、[シャープ](../Page/シャープ.md "wikilink")などが自社製携帯電話端末に採用している。
  - ワイドVGA+（ワイドブイジーエープラス、WVGA+）
    854×480ドットで、アスペクト比は16:9。VGA+と同じくNECが開発。NEC、[パナソニック モバイルコミュニケーションズ](../Page/パナソニック_モバイルコミュニケーションズ.md "wikilink")、シャープなどが自社製携帯電話端末に採用している。フルワイドVGAと長辺方向が10ドットしか違わないため、フルワイドVGAと記述されることがある。
  - フルワイドVGA（フルワイドブイジーエー、FWVGA）
    864×480ドットで、アスペクト比は16.2:9。[ソニー・エリクソン・モバイルコミュニケーションズ](https://ja.wikipedia.org/wiki/ソニー・エリクソン・モバイルコミュニケーションズ "wikilink")が開発。同社のほか、[三菱電機](../Page/三菱電機.md "wikilink")、富士通が自社製携帯電話端末に採用している。
  - フルワイドVGA++（FWVGA++）
    960×480ドット。アスペクト比は2:1。シャープの[IS01](https://ja.wikipedia.org/wiki/IS01 "wikilink")や[SH-10B](https://ja.wikipedia.org/wiki/SH-10B "wikilink")等に採用されている。

## 参考文献

  - IBM Part Number 68X2330.

  -
  -
## 脚注

### 注釈

<references group="注" />

### 出典

## 関連項目

  - [VGA端子](../Page/VGA端子.md "wikilink")
  - [DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")
  - [画面解像度](../Page/画面解像度.md "wikilink")
  - [Quarter Video Graphics Array](../Page/Quarter_Video_Graphics_Array.md "wikilink")（QVGA）
  - [DisplayPort](../Page/DisplayPort.md "wikilink")
  - [ブルースクリーン](../Page/ブルースクリーン.md "wikilink")

## 外部リンク

  - [今回のターゲット！ PC-TV454](http://www.saturn.dti.ne.jp/~p8490261/syuuri.htm) - 日本で9ピン規格VGA入力端子を実装した商品の例。ピンアサインを記した説明書のスキャンを含む。

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")

1.
2.  日本ではVGAの高解像度モードを標準的に使用する[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")が登場し、その後からPC/AT互換機が普及したため、経緯がこれとは少し異なる。
3.  [シリコンハウスへようこそ発掘\!\!あるあ・・・ねーよww](http://blog.siliconhouse.jp/archives/51451342.html)
4.  [EGA/CGA/VGA9 DB9 Connector](http://info-coach.fr/atari/hardware/interfaces.php#EGA_DB9_Connector)
5.
6.
7.  PS/2 Video Subsystem Technical Reference Manual 1992
8.  PS/2 Video Subsystem Technical Reference Manual 1992
9.
10.
11. 後の[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")ではその仕組み上の制限により対応可能なタイミングが絞られているため、標準でない画面モードは表示できないことが多い。
12.
13. HP D1194A Super VGA Display & HP D1195A Erognomic Super VGA Display Installation Guide, Hewlett Packard
14. Article ["Re: VGA specifications ,where ?"](http://groups.google.com/group/sci.electronics.design/msg/b8ee15d937e50fa1) posted 19 November 1997 to sci.electronics.design newsgroup by Jeroen Stessen
15. [CANARE HDR15F-EJ1.5CA VESA DDC対応D-sub15メス-BNC×5変換の紹介 ( その他趣味 ) - 音響・映像・電気設備が好き - Yahoo\!ブログ](http://blogs.yahoo.co.jp/linear_pcm0153/38019256.html)
16. [VESA DDC(EDID)ってなんだ？ ( その他趣味 ) - 音響・映像・電気設備が好き - Yahoo\!ブログ](http://blogs.yahoo.co.jp/linear_pcm0153/35170391.html)