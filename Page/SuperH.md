> この記事は[SuperH](https://ja.wikipedia.org/wiki/SuperH)から翻訳されています。


**SuperH**（スーパーエイチ）は、[日立製作所](../Page/日立製作所.md "wikilink")（後の[ルネサスエレクトロニクス](../Page/ルネサスエレクトロニクス.md "wikilink")）が開発した[組み込み機器用](../Page/組み込みシステム.md "wikilink")32[ビット](../Page/ビット.md "wikilink")[RISC](../Page/RISC.md "wikilink")[マイクロコンピュータである](../Page/マイクロプロセッサ.md "wikilink")。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:Denso-SH2.jpg "wikilink") 主に[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")タイプのSH-1/[SH-2](../Page/SH-2_\(プロセッサ\).md "wikilink")、[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")タイプのSH-3/SH-4の4シリーズが製品化されている。現在はそれぞれ上位シリーズであるSH-2A, SH-4Aが追加されている。また派生シリーズとして[携帯電話](../Page/携帯電話.md "wikilink")のアプリケーションプロセッサ向けSH-Mobile、64ビットCPUコアであるSH-5がラインナップされている。

立ち上げ当初から消費電力あたりの性能 (MIPS/W)の向上を標榜していたことが特徴の一つである（現在で言う[ユビキタスコンピューティング](../Page/ユビキタスコンピューティング.md "wikilink")社会における普及を目指した）。

[1992年](../Page/1992年.md "wikilink")に最初の製品であるSH-1 (SH-7034:HD6417034)が発表され、組み込み用途の32ビットRISCマイクロコンピュータとして先鞭をつけた。その後SH-2が[家庭用ゲーム機](https://ja.wikipedia.org/wiki/家庭用ゲーム機 "wikilink")の**[セガサターン](../Page/セガサターン.md "wikilink")**、自動車用ECUなどに、SH-3が[クラリオン](../Page/クラリオン.md "wikilink")のカーナビゲーション、や**[小惑星探査機はやぶさ](../Page/はやぶさ_\(探査機\).md "wikilink")**などに、SH-4が**[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")**に採用されたこともあり、メジャープロセッサとして認知された。また、[DSPを含む製品を発表した](../Page/デジタルシグナルプロセッサ.md "wikilink")。

[STマイクロエレクトロニクス](../Page/STマイクロエレクトロニクス.md "wikilink")と共同開発したSH-5をIPコアで発表した後、性能を向上させる方向から一転（[Windows CEベースの](https://ja.wikipedia.org/wiki/Windows_CE "wikilink")[PDAが](../Page/携帯情報端末.md "wikilink")[Pocket PC 2002よりのち](https://ja.wikipedia.org/wiki/PocketPC#Pocket_PC_2002 "wikilink")[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")に一本化されたことと、セガ（後の[セガゲームス](https://ja.wikipedia.org/wiki/セガゲームス "wikilink")）が家庭用ゲーム機のハードの開発から撤退したこと、RISCプロセッサのブームが一段落したこと、等も挙げられる）、携帯電話を中心にターゲットを絞ったSH-Mobileシリーズを展開し、日本の[携帯電話](../Page/携帯電話.md "wikilink")各キャリアや[ウィルコム](../Page/ウィルコム.md "wikilink")の機器に採用されている。

## 特徴

CPUコアは[アドレス長](../Page/メモリアドレス.md "wikilink")、[データ](../Page/データ.md "wikilink")長はともに32ビットだが、インストラクションセットは16ビット固定長命令であり、32ビットCPUでありながらコード効率を向上、組み込み用32ビットマイコンとして成功させた（その後[ARMや](../Page/ARMアーキテクチャ.md "wikilink")[MIPSなどもこれに倣い](../Page/MIPSアーキテクチャ.md "wikilink")、[Thumb命令などの](https://ja.wikipedia.org/wiki/ARMアーキテクチャ#Thumb "wikilink")16ビット命令体系を取り込んだ）。ビットフィールドを削減し16ビット語長に抑えるため、汎用[レジスタは](../Page/レジスタ_\(コンピュータ\).md "wikilink")16本、2[オペランド命令が基調となる](https://ja.wikipedia.org/wiki/被演算子 "wikilink")。またインデックス修飾の[オフセットは](https://ja.wikipedia.org/wiki/オフセット_\(コンピュータ\) "wikilink")[バイト単位ではなく命令で指定するデータ長でスケーリングされ](../Page/バイト_\(情報\).md "wikilink")、さらに32ビット絶対アドレスや16 / 32ビット相対アドレスの指定は4bit / 8bitのディスプレースメント相対によるロード命令によって値を取得する必要がある。

CPUコアには汎用レジスタ16本のほかにグローバルベースレジスタ、ベクタベースレジスタ、[サブルーチン](../Page/サブルーチン.md "wikilink")呼び出し用のプロシジャレジスタなどを持つ。

周辺ユニットとして、タイマや割り込みコントローラ、[シリアルインタフェース](../Page/シリアルポート.md "wikilink")、[ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink") / [RAM](../Page/Random_Access_Memory.md "wikilink")、[DMAコントローラ](https://ja.wikipedia.org/wiki/DMAコントローラ "wikilink")、[I/Oポートなどが内蔵されている](https://ja.wikipedia.org/wiki/Input/Outputポート "wikilink")。

各SHシリーズは基本的に数字の若いシリーズとオブジェクトレベルで互換性がある。ただし、

  - ハードウェアレベルではSH-1 / SH-2とSH-3以上ではMMU等の関係で[例外処理](../Page/例外処理.md "wikilink")（[割り込み](../Page/割り込み_\(コンピュータ\).md "wikilink")）などの実装が異なっている。
  - SH-3（SH-4以外）とSH-4間のオブジェクトには完全な上位互換性はなく、コードを共有するにはSH-3のオブジェクトのリンク時に[アラインメントを](https://ja.wikipedia.org/wiki/データ構造アライメント "wikilink")4KBに指定する必要がある(WindowsCEの場合)。ただしSH-3ベースで[コンパイルしたオブジェクトコードは](../Page/コンパイラ.md "wikilink")、SH-4の[浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")レジスタを使用しない。

条件分岐は1bitのT（真 / 偽）[フラグを比較命令でセットし](../Page/フラグ_\(コンピュータ\).md "wikilink")、条件分岐命令で分岐する。 これは演算毎に自動でキャリーやゼロなどの複数のフラグがセットされ、条件分岐命令ではそのフラグを参照するアーキテクチャと、条件分岐命令で指定したレジスタのゼロ / 非ゼロや偶数・奇数によって直接分岐するアーキテクチャの折衷案といえる。また、分岐命令は多くが[遅延スロット](https://ja.wikipedia.org/wiki/遅延スロット "wikilink")をもつ遅延分岐命令となっている。

## シリーズ展開

シリーズ番号は初期の番号を記す。

### コントローラタイプ

[thumb](https://ja.wikipedia.org/wiki/ファイル:HD6417095_01.jpg "wikilink")

  - SH-1 （SH7032/7034 - 動作周波数20MHz）
    [1992年](../Page/1992年.md "wikilink")に最初に出たSHシリーズで、他社の組み込み系[マイコンチップが](../Page/マイクロコンピュータ.md "wikilink")16ビット[CISC](../Page/CISC.md "wikilink")に留まる中、いち早く32ビットRISCマイコンとして製品化された。
  - [SH-2](../Page/SH-2_\(プロセッサ\).md "wikilink") （SH7604 - 動作周波数28.7MHz） 104MIPS/80MHz
    [1994年](../Page/1994年.md "wikilink")にSH-1の後継品種として、当初から家庭用ゲーム機の[メガドライブ](../Page/メガドライブ.md "wikilink")の拡張機器である[スーパー32X](../Page/スーパー32X.md "wikilink")や[セガサターン](../Page/セガサターン.md "wikilink")に搭載することを想定して製品化された（セガサターン搭載品番はHD6417095）。そのため32ビット乗算回路の搭載や当時出たばかりの[シンクロナスDRAM](https://ja.wikipedia.org/wiki/シンクロナスDRAM "wikilink")インタフェースなどを新規搭載した。セガサターン用ではない一般用の型番は,HD6417604。
  - SH-DSP （SH7410 - 動作周波数60MHz）
    SH-2をベースに独立した[DSPデータパスを追加し](../Page/デジタル信号処理.md "wikilink")、乗算命令など信号処理性能を強化したシリーズ。[1996年](../Page/1996年.md "wikilink")開発、翌年6月出荷。
  - SH2-DSP
    SH-2A Core （SH7206 (No Fpu)- Dhrystone 480MIPS/200MHz）(SH7262 (with fpu) 345MIPS/144MHz)
    SH-2をベースに最大2命令/1クロックに[スーパースカラ](https://ja.wikipedia.org/wiki/スーパースカラ "wikilink")方式を導入して高速化。命令長が32bitのものが追加されている。割り込み時のレジスタ退避をHW化することによってリアルタイム性向上。

### プロセッサタイプ

[thumb](https://ja.wikipedia.org/wiki/ファイル:HD6417709A_02.jpg "wikilink") [thumbに搭載されているSH](https://ja.wikipedia.org/wiki/ファイル:SH7091_01.jpg "wikilink")-4 HD6417091\]\]

  - SH-3 （SH7702/7708 - 動作周波数60MHz）
    [マイクロソフト](../Page/マイクロソフト.md "wikilink")社の[Windows CEに対応したシリーズ](https://ja.wikipedia.org/wiki/Windows_CE "wikilink")。高速化と共にMMUなどのマルチタスクOSに必要な機能を追加し、PDAへの搭載を目的にした。またWindows CEに向け割込み機構を変更した。[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")にも変更可能（SH-1、SH-2は[ビッグエンディアン](https://ja.wikipedia.org/wiki/ビッグエンディアン "wikilink")）。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")3月出荷。Windows CEのほか[Zaurus](https://ja.wikipedia.org/wiki/Zaurus "wikilink")（MIシリーズ）などにも使用された。
  - SH-3E （SH7718 - 動作周波数100MHz）
    SH7708に浮動小数点演算ユニットを追加したもの
  - SH-3 （SH7709 - 動作周波数80MHz）
    8KBキャッシュ内蔵,電源電圧3.3V,MMU,シリアル×3ch,タイマー×3ch,RTC,DMAC,A/Dコンバータ,D/Aコンバータ,I/Oポート,オンチップデバッグ機能,メモリインターフェイス
  - SH-3 （SH7709A - 動作周波数100MHz/133MHz）
    16KBキャッシュ内蔵,CPU部電源電圧1.8V,I/O部電源電圧3.3V,MMU,シリアル×3ch,タイマー×3ch,RTC,DMAC,A/Dコンバータ,D/Aコンバータ,I/Oポート,オンチップデバッグ機能,メモリインターフェイス
  - SH-4 （SH7750 - 動作周波数200MHz）
    360MIPSの性能とベクトル型浮動小数点演算ユニットを搭載することで、マルチメディア機能を充実させた。SH-2と同様、当初から家庭用ゲーム機の[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")に搭載することを想定して開発され、[RTC](https://ja.wikipedia.org/wiki/RTC "wikilink")をも内蔵した。SuperH Inc.からIPコアとしても提供された（現在はルネサスエレクトロニクスに移管）。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")12月出荷。一部のWindowsCE機にも使用された。
  - SH3-DSP （SH7729R - 最大動作周波数200MHz）
    SH-3コアにDSP機能を追加したマイコン。その他USBホスト機能などを内蔵する。[2000年](../Page/2000年.md "wikilink")12月出荷。
  - SH-5 （SH5-101 - 動作周波数340MHz～500MHz）
    日立（当時）とSTマイクロエレクトロニクスが共同で開発した64ビットマイコン。従来はSuperH Inc.からIPコアとしてのみ提供されていたが、現在はルネサス エレクトロニクスに移管されている。新しい命令セットとして64ビット拡張命令モード（SHmedia、従来[互換モード](https://ja.wikipedia.org/wiki/互換モード "wikilink")はSHcompact）を持ち、SIMD系命令が拡充されている。FPUファミリでは128ビットのベクトル型浮動小数点演算ユニットを搭載する。
  - SH-4A （SH7780 - 最大動作周波数400MHz / SH7785 - 最大動作周波数600MHz / SH7786 - SH-4A[デュアル](../Page/マルチコア.md "wikilink") 最大動作周波数533MHz 開発中)
    SH-4の[パイプラインを](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")7段にし、高速化。キャッシュ命令の強化・拡張モード（32bit物理アドレス空間）を追加。
  - SH-X3 （最大動作周波数800MHz）
    SH-4Aを元に[パイプラインを](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")8段にし[マルチコア](../Page/マルチコア.md "wikilink")化したもの。2007年第1四半期登場予定。

### その他展開

  - F-ZTAT (Flexible Zero Turn Around Time)
    フラッシュメモリを内蔵した品種。顧客がプログラムを固定化しマイコンを専用機能部品として扱った場合に、固定化プログラムの格納場所をフラッシュメモリとすることで顧客側から見た改修のターンアラウンドタイムを0とする意味から付けられた。
  - SH/Tiny シリーズ
    SH-2コアを少ピンで小型のQFPパッケージに封止し、搭載するシステムの裾野を広げることを目的とした。
  - SH-Ether
    IEEE 802.3u準拠の[イーサネット](../Page/イーサネット.md "wikilink")コントローラを1～2チャンネル内蔵し、ネットワーク家電や[FA向けに作られた](../Page/ファクトリーオートメーション.md "wikilink")。

### SH-Mobile

SH-Mobileは、SuperHアーキテクチャのCPUコアに加え、マルチメディア処理回路や基地局とのデジタル信号を処理するベースバンド回路を加えた携帯電話向けのシステムLSI製品である。

  - SH7290 - 動作周波数200MHz
    SH3-DSPをコアに持ち、外部ベースバンド回路とのインタフェースやデジタルカメラ用機能、LCD表示機能などを搭載する携帯電話用コアの初版。[2002年](../Page/2002年.md "wikilink")4月出荷。

以後は、[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")・ミドルレンジ・[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")向けと分離したシリーズ展開を行っている。

  - SH7300(SH-Mobile V)
    SH7290の機能に加え、[MPEG4](https://ja.wikipedia.org/wiki/MPEG4 "wikilink")のハードウェアアクセラレータを搭載し、さらにSXGAカメラ対応のインタフェースを内蔵しているため、TV電話機能や高精細カメラを備える次世代携帯電話に適したコア。ハイエンド向けコアの初版に位置する。

<!-- end list -->

  - SH-Mobile V2
    従来のSH-Mobile　Vから、画像処理機能を大幅に強化。TFTカラー液晶に対応したLCDコントローラを内蔵、カメラインタフェースをUXGA対応に強化。またMPEG-4のフル・ハードウェアアクセラレータを搭載したことにより、CPU負荷を低減すると共に低消費電力化を図っている。

<!-- end list -->

  - SH-Mobile3
    この製品より、新コアのSH-Mobile　Xコア(SH4AL-DSP)を採用。7段[パイプラインと](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")[ハイパースケーラ](https://ja.wikipedia.org/wiki/ハイパースケーラ "wikilink")の採用で、アプリケーションの並列処理を余裕を持って可能にし、従来のハイエンド向けの製品から約2.3倍の性能向上を図っている。300万画素のカメラモジュールにも対応。

このほかにもSH-Mobile3Aなどの製品があり、[ワンセグ](../Page/ワンセグ.md "wikilink")の送受信に最適化するなどの機能強化が図られている。

また、携帯電話以外での使用を前提としたSH-MobileRもあり、これは[PND](../Page/PND.md "wikilink")などで使用されている。

#### SH-Mobile Gシリーズ

SH-Mobileをベースに[W-CDMA](../Page/W-CDMA.md "wikilink")および[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")対応のベースバンド回路を統合した製品で、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")および複数の携帯電話メーカーと共同で開発された。ベースバンドプロセッサおよびOSが動作するアプリケーションプロセッサには[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")を採用し、SH-4および[PowerVR](../Page/PowerVR.md "wikilink")等の各種[IPはマルチメディア等の高負荷処理を担当する](../Page/IPコア.md "wikilink")\[1\]。

最初のバージョンの**SH-Mobile G1**は[2006年](../Page/2006年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")に量産出荷が始まった。[富士通](../Page/富士通.md "wikilink")、[三菱電機](../Page/三菱電機.md "wikilink")、[シャープ](../Page/シャープ.md "wikilink")の3社が2006年のドコモの[夏](../Page/夏.md "wikilink")モデルから採用し、1年2カ月で1000万個を出荷した。

第二世代となる**SH-Mobile G2**は、下り最大3.6Mbpsの[HSDPA](https://ja.wikipedia.org/wiki/HSPA#HSDPA "wikilink")、[GPRS](https://ja.wikipedia.org/wiki/GSM#GPRS "wikilink")、[EDGEの対応に加え](https://ja.wikipedia.org/wiki/GSM#EDGE "wikilink")、[OSやミドルウェア](../Page/オペレーティングシステム.md "wikilink")、ドライバなどの一体化を行った。このバージョンのものから、富士通、三菱電機、シャープの3社が開発に加わった。2006年[9月](../Page/9月.md "wikilink")にサンプル出荷を開始し、[2007年](../Page/2007年.md "wikilink")第3四半期から量産出荷を行っている。

第三世代**SH-Mobile G3**は、下り最大7.2MbpsのHSDPA（カテゴリー8）に対応し、このバージョンのものから[ソニー エリクソンが開発に参加した](https://ja.wikipedia.org/wiki/ソニー・エリクソン・モバイルコミュニケーションズ#.E6.97.A5.E6.9C.AC.E6.B3.95.E4.BA.BA "wikilink")。2007年[10月](https://ja.wikipedia.org/wiki/10月 "wikilink")にサンプル出荷を開始している\[2\]。

2008年10月には、**SH-Mobile G4**の開発開始を発表している\[3\]。45nmプロセスを採用し、新たに[HSUPA](https://ja.wikipedia.org/wiki/HSPA#HSUPA "wikilink")、[HD画像処理への対応を予定している](https://ja.wikipedia.org/wiki/ハイディフィニション "wikilink")。

### SH-Navi

  - SH-Navi

<!-- end list -->

  - SH7770 400MHz

<!-- end list -->

  -
    SH4Aコアを採用、[カーナビ用のグラフィックエンジンとして](../Page/カーナビゲーション.md "wikilink")[PowerVR](../Page/PowerVR.md "wikilink") MBXコアを内蔵している。

<!-- end list -->

  - SH7786 533MHz

<!-- end list -->

  -
    65 [nm](../Page/ナノメートル.md "wikilink") [プロセスとなった](https://ja.wikipedia.org/wiki/集積回路#プロセス "wikilink")、[デュアルコア](../Page/マルチコア.md "wikilink")（SH-4A × 2）[マイコン](../Page/マイクロコンピュータ.md "wikilink")。車載用では世界で初めて[DDR3 SDRAMに対応した](../Page/DDR3_SDRAM.md "wikilink")。

## オープンソース実装「J Core」

2014年、SH-2関連の特許が期限切れとなるのに合わせ、[μClinux](https://ja.wikipedia.org/wiki/μClinux "wikilink")の初期開発者Jeff Dionneなどが[クリーンルーム設計](https://ja.wikipedia.org/wiki/クリーンルーム設計 "wikilink")で実装したもの。回路が[VHDL](../Page/VHDL.md "wikilink")で記述されており、BSDライセンスで公開されている。\[4\]\[5\]

## 脚注

<references/>

## 外部リンク

  - [ルネサス エレクトロニクス.SuperHファミリ](http://japan.renesas.com/products/mpumcu/superh/index.jsp)
  - [ルネサス エレクトロニクス.SH-Mobile](http://japan.renesas.com/products/soc/assp/mobile/index.jsp)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink") [Category:日立製作所](https://ja.wikipedia.org/wiki/Category:日立製作所 "wikilink")

1.
2.
3.
4.  <http://lwn.net/Articles/647636/>
5.  <http://j-core.org/>