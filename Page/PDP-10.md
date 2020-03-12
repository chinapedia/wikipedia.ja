> この記事は[PDP-10](https://ja.wikipedia.org/wiki/PDP-10)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:PDP-10_1090.jpg "wikilink") とメモリモジュール6台\]\] **PDP-10**は、[1960年代](../Page/1960年代.md "wikilink")後半から[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")(DEC)が製造した[メインフレーム](../Page/メインフレーム.md "wikilink")ファミリ\[1\]。[PDPシリーズ](../Page/PDPシリーズ.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")のひとつ。1966年に最初の機種が出荷された\[2\]。[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")を一般に浸透させたマシンであり、多くの大学や研究機関で採用されたことから[1970年代](../Page/1970年代.md "wikilink")の[ハッカー文化](../Page/ハッカー文化.md "wikilink")に大きな影響を与えた。PDP-10を導入した主な大学/研究機関としては、[MITの](../Page/マサチューセッツ工科大学.md "wikilink")[人工知能研究所および](../Page/MIT人工知能研究所.md "wikilink")[Project MAC](https://ja.wikipedia.org/wiki/Project_MAC "wikilink")、[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")の[SAIL](../Page/スタンフォード人工知能研究所.md "wikilink")、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")などがある。

PDP-10の[アーキテクチャは](../Page/コンピュータ・アーキテクチャ.md "wikilink")[PDP-6](../Page/PDP-6.md "wikilink")とほぼ同じで、[36ビット](https://ja.wikipedia.org/wiki/36ビット "wikilink")[ワード](../Page/ワード.md "wikilink")である。[命令セット](../Page/命令セット.md "wikilink")は若干拡張されており、[ハードウェア](../Page/ハードウェア.md "wikilink")の実装は進歩している。命令セットは未だに卓越しているという見方もあり、特に "byte"命令は任意の[ビットフィールド](https://ja.wikipedia.org/wiki/ビットフィールド "wikilink")を操作することができた（この場合の [byte](../Page/バイト_\(情報\).md "wikilink") は必ずしも[8ビット](../Page/8ビット.md "wikilink")を意味せず「固定ビット数の連続の並び」という意味である）。

## 機種と技術的進展

[thumb](https://ja.wikipedia.org/wiki/ファイル:KA10_mod_end.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:DEC-10_Memory_Bus_Terminator_H866_top_view.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:KL10-backplane.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:KS10-open.jpg "wikilink") 最初のPDP-10のプロセッサは[1968年](https://ja.wikipedia.org/wiki/1968年 "wikilink")に登場したKA10である。[トランジスタ](../Page/トランジスタ.md "wikilink")をDECの技術でパッケージし、半自動化された工程によって[バックプレーン](../Page/バックプレーン.md "wikilink")の[ワイヤラッピング](../Page/ワイヤラッピング.md "wikilink")が行われている。サイクルタイムは1μ秒、加算命令にかかる時間は2.1μ秒である\[3\]。[1973年](../Page/1973年.md "wikilink")、KI10が新たに登場した。これは[TTL](../Page/Transistor-transistor_logic.md "wikilink")[集積回路](../Page/集積回路.md "wikilink")を使っている。さらに[1975年](../Page/1975年.md "wikilink")には高性能なKL10（さらに後にはKL20）が登場。こちらは[ECLで構成され](../Page/エミッタ結合論理.md "wikilink")、[マイクロプログラム方式](../Page/マイクロプログラム方式.md "wikilink")を導入し、[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")を搭載している。低価格版のKS10も[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")に登場し、TTLと[Am2901](../Page/AMD_Am2900.md "wikilink")[ビットスライス](../Page/ビットスライス.md "wikilink")チップで構成され、[PDP-11](../Page/PDP-11.md "wikilink")の[Unibus](../Page/Unibus.md "wikilink")を使って周辺機器を接続するようになっていた。

### KA10

KA10の最大[メモリ容量は](../Page/主記憶装置.md "wikilink")256[K](../Page/キロ.md "wikilink")[ワード](../Page/ワード.md "wikilink")（1152K[バイト](../Page/バイト_\(情報\).md "wikilink")）である。[ページング機構は持たず](../Page/ページング方式.md "wikilink")、2本のプロテクション/リロケーションレジスタ（base and bounds レジスタとも呼ぶ）で[メモリ管理](../Page/メモリ管理.md "wikilink")を行っている。これによりユーザーの[アドレス空間](../Page/アドレス空間.md "wikilink")の半分を[メインメモリの指定した領域に限定できる](../Page/主記憶装置.md "wikilink")。従って、リードオンリーで共有可能なテキストセグメント（high segmentとも呼ばれた）とリード/ライト可能なデータセグメントおよび[スタック](../Page/スタック.md "wikilink")セグメント（low segmentとも呼ばれた）という後の[UNIX](../Page/UNIX.md "wikilink")でも使われた[プロセス](../Page/プロセス.md "wikilink")モデルが可能であった。[MITや](../Page/マサチューセッツ工科大学.md "wikilink")[BBNでは](../Page/BBNテクノロジーズ.md "wikilink")、KA10 に改造を加えて物理メモリ容量を増やし、ページング機構を追加して方式の[仮想記憶](../Page/仮想記憶.md "wikilink")をサポートした。

### KI10 と KL10

KI10およびその後のプロセッサでは[ページング方式](../Page/ページング方式.md "wikilink")が採用され、最大4[Mワードの大容量物理アドレス空間をサポートした](../Page/メガ.md "wikilink")。KI10の機種としては1060、1070、1077があり、特に1077は2CPUを搭載している。

最初のKL10の機種（1080, 1088など。DECsystem-10とも称した）はオリジナルのPDP-10のメモリバスを使用し、拡張メモリモジュールを追加していた。この場合のモジュールとは筐体（キャビネット）を意味し、高さ180cm、幅と奥行きが70cm程度であり、32kワードから256kワードの[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")を搭載できる（本項目冒頭右端にある写真にはそのようなキャビネットが6台写っている）。 [DECSYSTEM-20](https://ja.wikipedia.org/wiki/:en:DECSYSTEM-20 "wikilink") (2040, 2050, 2060, 2065) のプロセッサは KL20 と（間違って）呼ばれているが、[CPU](../Page/CPU.md "wikilink")と同じ筐体内のメモリを使用していた。10xxモデルの構成はこれとは異なり、DECSYSTEM-20の背の低い筐体ではなくオリジナルのPDP-10と同じ背の高い筐体を使用していた。10xx と 20xx のモデル間の差異は見た目の問題が大きく、10xx系であっても20xx系のような[メモリおよび](../Page/記憶装置.md "wikilink")[I/Oの構成のものもあったし](../Page/入出力.md "wikilink")、20xx系でも10xx系のような構成のものもあった。どちらの系列でも[TOPS-10](../Page/TOPS-10.md "wikilink")と[TOPS-20](../Page/TOPS-20.md "wikilink")のマイクロコードが実行できたため、どちらの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")も実行できた。

### MASSbus

20xxシリーズKLマシンのI/OアーキテクチャはDECの新たなバス MASSbus に基づいていた。[Unibus](../Page/Unibus.md "wikilink")をオープンアーキテクチャとしたことが[PDP-11](../Page/PDP-11.md "wikilink")成功の要因のひとつだが、KLにおいてはDECはMASSbusをプロプライエタリとし、従来の方針に戻している。結果としてMASSbus向けの周辺機器を製造するサードパーティは登場せず、DECは例えばRP06ディスクドライブの価格を同等のIBM互換機器よりかなり高く設定することができた。[CompuServe](../Page/CompuServe.md "wikilink")はMASSbusに接続可能なディスクコントローラを独自開発したことがあるが、接続したのは IBM 3330 ディスク装置だった。

### Model B

後に2060プロセッサの Model B 版では仮想アドレス空間の256Kワードという制限を取り払い、最大32個の256Kワードまでの「セクション」を構成可能にして[命令セット](../Page/命令セット.md "wikilink")もそれに応じて変更した。従って同じKL10でも、従来の Model A と Model B は全く別のCPUとみなすことができる。Model B の機能を生かした最初のオペレーティングシステムは TOPS-20 release 3 であり、ユーザーモードのアドレッシング拡張は TOPS-20 release 4 でサポートされた。TOPS-20 release 4.1 は Model B プロセッサでのみ動作し、Model A では動作できなかった。

### KS10

困ったことに、KS10は Model B [アーキテクチャを実装するだけの余裕があったにも関わらず](../Page/コンピュータ・アーキテクチャ.md "wikilink") Model A アーキテクチャであった。明らかに市場価格帯をにらんでの決定だが、このためにKS10の製品寿命は非常に短かったのである。

### MCA25

最後のアップグレードはMCA25と呼ばれ、2060 から 2065 へのアップグレードであった。これにより複数セクションで動作する[プログラムの性能が向上した](../Page/プログラム_\(コンピュータ\).md "wikilink")。

### フロントエンドシステム

[thumb](https://ja.wikipedia.org/wiki/ファイル:KL10-front-end.jpg "wikilink") KLクラスのマシンを立ち上げるには、内蔵されているフロントエンドコンピュータ PDP-11/40 が必須である。PDP-11はデュアルポートのRP06ディスクドライブ（または8インチ[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")ドライブまたは）から[ブート](../Page/ブート.md "wikilink")し、PDP-11にメインプロセッサを起動するコマンドを入力すると、同じRP06ディスクドライブからブートさせることになる。このPDP-11はメインプロセッサが運用状態に入るとそれを監視する機能を果たす。

KSシステムでも似たようなブート手順を採用していた。[Intel 8080](../Page/Intel_8080.md "wikilink") がメインプロセッサのマイクロコードを外部記憶装置からロードする方式である。メインプロセッサが立ち上がると、8080はコンソールと遠隔監視ポートの制御を担当した。

## 命令セットアーキテクチャ

最初のPDP-6から KL-10 の Model A まで、ユーザーモードの[命令セット](../Page/命令セット.md "wikilink")アーキテクチャはほぼ変わっていない。本節ではその部分のアーキテクチャを解説する。

### アドレッシング

PDP-10のワード長は36ビットで、アドレスは18ビットである。スーパーバイザモードでは、命令アドレスは直接物理アドレスとなっている。ユーザーモードでは、アドレスは物理メモリアドレスに変換される。初期の機種ではユーザープロセスはアドレス空間の先頭と最後尾、0番地付近と最も大きなアドレスの付近から使用した。どちらのセグメントも連続である。後期アーキテクチャではページング方式となり、不連続なアドレス空間が可能となった。CPUの汎用レジスタにもメモリアドレスがふられており、0番地から15番地に対応していた。

### レジスタ

汎用の36ビットレジスタが16本ある。0番のレジスタ以外では、右半分がインデックスに使われる。一部の命令はレジスタを組み合わせて使用する。条件レジスタ（[ステータスレジスタ](../Page/ステータスレジスタ.md "wikilink")）もあり、算術命令の結果（オーバーフローなど）を示すビット群を保持していて、一部の命令からアクセスできる。

### スーパーバイザモード

動作モードとしては、スーパーバイザモードとユーザーモードの2つがある。メモリ参照に上述の差異がある他に、スーパーバイザモードでは入出力操作が可能である。

ユーザーモードからスーパーバイザモードへの移行には、未実装ユーザー命令 (UUO) を使用して例外を発生させ、スーパーバイザがそれをトラップして処理を行うようになっていた。安価な機種でハードウェア実装を省略した場合も同様の機構でスーパーバイザによるエミュレーションを行っていた。

### データ型

アーキテクチャ上直接サポートしていた主なデータ型は[2の補数](../Page/2の補数.md "wikilink")形式の36ビット整数、36ビット浮動小数点数、ハーフワードである。拡張された72ビットの浮動小数点数は複数命令連鎖で使うよう設計された特別な命令でサポートされる。バイト単位のポインタも特別な命令でサポートしている。1ワードの半分をカウンタ、半分をポインタとしてメモリ範囲を指すことができ、[スタック](../Page/スタック.md "wikilink")などに使われた。

### 命令

命令セットは非常に直交性が高い。命令のフォーマットは、9ビットの命令コード、4ビットのレジスタ番号、23ビットの実効アドレスフィールドからなる。実効アドレスフィールドは、1ビットの間接ビット、4ビットのレジスタ番号、18ビットのオフセットからなる。命令実行は実効アドレスの計算から始まる。指定されたレジスタが0番でなければ、その中身とオフセットを加算する。間接ビットが1なら、計算で求めたアドレスにあるワードをフェッチし、その中身の間接ビットが1でなくなるまで、同様の処理を続ける。こうして得られた実効アドレスを命令がメモリ内容のフェッチに使ったり、そのまま定数として使ったりする。例えば、MOVEI A,3(C) という命令は、レジスタCの下位18ビットに3を加算し、レジスタAにその結果を格納するもので、メモリには全くアクセスしない。

命令は、算術・論理・転送、条件分岐、条件スキップの3種類に分類される。さらに細かい分類もある。

算術・論理・転送命令は、即値からレジスタ、メモリからレジスタ、レジスタからメモリ、レジスタとメモリからレジスタとメモリ、メモリからメモリという操作の種類がある。レジスタもメモリの一部としてアドレスを持っているので、レジスタからレジスタという操作も事実上存在する。例えばADD命令には、ADDI（18ビット即値定数をレジスタに加算）、ADDM（レジスタの内容を指定したメモリ位置に加算）、ADDB（レジスタの内容を指定したメモリ位置に加算し、その結果をレジスタに格納）といった種類がある。精巧な例として HLROM (*H*alf *L*eft to *R*ight, *O*nes to *M*emory) 命令がある。これはレジスタの中身の左半分を取り出して、メモリ位置の右半分に置き、メモリ位置の左半分を全て1にするという命令である。

条件分岐命令はレジスタの内容を調べ、その結果によって指定されたアドレスに分岐するか否かを決める。ニーモニックはJUMPで始まり、JUMPAは「無条件分岐」、JUMPは「無条件で分岐しない」という意味である。命令セットの対称性を重視したため、一部の命令は何もしない命令になっている。例えば JUMPN A,LOC という命令は、レジスタAの中身がゼロでない場合LOCというアドレスに分岐する。条件（ステータス）レジスタの内容に従って判断する条件分岐命令として、JRST命令がある。KA10とKI10では、JRSTの方がJUMPAより高速だったため、標準の無条件分岐としてJRSTを使っていた。

条件スキップ命令は、レジスタの内容とメモリの内容を比較し、その結果によって次の命令（無条件分岐であることが多い）をスキップするか否かを決める。単純な例として CAMN A,LOC という命令では、レジスタAとLOCという位置の内容を比較し、等しくなければ次の命令をスキップする。より複雑な例として TLCE A,LOC という命令では、LOCの内容をマスクとしてレジスタAに適用して対応するビット群を取り出し、取り出したビットが全てゼロなら次の命令をスキップする。そしてスキップするか否かに関わらず、それらのビットを反転させる。

シフトやローテート命令、プロシージャコール命令などもある。特筆すべき命令としてスタック操作のためのPUSHとPOP、それらに対応するスタックコール命令PUSHJとPOPJがある。バイト操作命令はワード内の任意長のビットフィールドを操作し、同時にポインタをそのフィールドのぶんだけ進めることができる。

## ソフトウェア

当初のPDP-10の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)は単に "Monitor" と呼ばれたが、後に[TOPS-10](../Page/TOPS-10.md "wikilink")と改称され、システム全体も DECsystem-10 と呼ばれるようになった。MonitorとTOPS-10はスタンフォードのオペレーティングシステムや[CompuServe](../Page/CompuServe.md "wikilink")の[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")の基盤となった。

後に一部のPDP-10はDEC以外で開発されたコンポーネントを中心に構築されたOSを動作させ始めた。例えば、主スケジューラはこちらの大学製、ディスクサービスはあちらの大学製といった具合である。[CompuServe](../Page/CompuServe.md "wikilink")などの商用タイムシェアリングサービスは自前のシステムプログラミング部門を持っており、独自にOSを改造して自社の事業のニーズに合わせていた。またなどの強力なユーザーコミュニティがあり、ユーザーが自身で開発したソフトウェアを共有することができた。

[BBNは独自のOSである](../Page/BBNテクノロジーズ.md "wikilink")[TENEX](https://ja.wikipedia.org/wiki/TENEX "wikilink")を開発し、これが様々な研究機関で使われ一種のデファクトスタンダードとなった。DECはTENEXをKL10に移植して大幅に機能強化し、[TOPS-20](../Page/TOPS-20.md "wikilink")と名づけ、DECSYSTEM-20のOSとした。[MITも](../Page/マサチューセッツ工科大学.md "wikilink")[ITSと呼ばれる独自OSを開発した](../Page/Incompatible_Timesharing_System.md "wikilink")（名称はMITが [IBM 7094](../Page/IBM_7090.md "wikilink") 上で開発した[CTSS](../Page/CTSS.md "wikilink") (Compatible Time-Sharing System) のパロディ）。

[Tymshareは](https://ja.wikipedia.org/wiki/:en:Tymshare "wikilink") [TOPS-10](../Page/TOPS-10.md "wikilink") をベースとして[TOPS-20](../Page/TOPS-20.md "wikilink")のようなページング機構を採用した TYMCOM-X を開発した。

## クローン

1970年代初め、[パロアルト研究所](../Page/パロアルト研究所.md "wikilink")の研究者たちは経営陣がPDP-10購入を許可しなかったため不満がたまっていた。というのも[ゼロックス](../Page/ゼロックス.md "wikilink")は社を買収したところで、パロアルト研究所にもそのマシンを使ってほしかったのである。しかし[チャック・サッカー](../Page/チャック・サッカー.md "wikilink")率いるチームは、PDP-10のクローンシステム "MAXC"（SDS社をゼロックスに売った Max Palevsky にちなんだ名称）を自前で設計し、2台構築して使用した。MAXCという名称は[バクロニム](../Page/バクロニム.md "wikilink")として Multiple Access Xerox Computer の略とされた。OSは[TENEX](https://ja.wikipedia.org/wiki/TENEX "wikilink")を移植して使用した\[4\]。

PDP-10のクローンを販売しようというサードパーティ（[Foonly](https://ja.wikipedia.org/wiki/:en:Foonly "wikilink")、[Systems Concetps](https://ja.wikipedia.org/wiki/:en:Systems_Concepts "wikilink")、[XKLなど](https://ja.wikipedia.org/wiki/:en:XKL "wikilink")）もあったが、あまり成功していない。[ディズニーのSF映画](../Page/ウォルト・ディズニー・カンパニー.md "wikilink") *[トロン](../Page/トロン_\(映画\).md "wikilink")* では[CGIにPDP](../Page/Computer_Generated_Imagery.md "wikilink")-10クローンの Foonly F-1 が使われている。

## CompuServe での使用

DECsystem-10アーキテクチャのシステムを最も多く所有していたのが[CompuServe](../Page/CompuServe.md "wikilink")で、ピーク時にはオハイオ州[コロンバスの](../Page/コロンバス_\(オハイオ州\).md "wikilink")3つのデータセンターにて200台以上が運用されていた。CompuServeはそれらシステムを「ホスト」とし、商用アプリケーションへのアクセスを提供すると同時に CompuServe Information Service も提供していた。当初はDECからシステムを購入していたが、DECが[VAX](../Page/VAX.md "wikilink")に集中するためにPDP-10を販売終了としたため、CompuServeや他の顧客は Systems Concepts から[互換機](../Page/互換機.md "wikilink")を購入し始めた。2007年1月現在、CompuServeは数台のPDP-10アーキテクチャのマシンを稼働させている。

KLシリーズの主電源は非常に効率が悪く、CompuServeでは自社の技術者が設計した電源に置き換え、消費電力を半分に抑えた。CompuServeはその電源の設計をDECに無償で提供し、CompuServeがその後購入するKLシリーズの電力消費を抑えることをDECに約束させようとした。DECはこの申し出を断わっている。 [thumbを使ったパネル](https://ja.wikipedia.org/wiki/ファイル:MF10-Panel.jpg "wikilink")\]\]

CompuServeがPDP-10に施したもう1つの改造は、KI10プロセッサ筐体にある数百個のインジケーターランプをLEDに置換することだった。置換にかかったコストは電力消費量を抑えたことですぐに回収でき、同時に発熱も減り、切れた電球を交換する手間も省けた。DECはこれを全世界に適用した。右の写真は KI10 CPU と同時代のMF10メモリのパネルである。博物館に展示されているものだが、2008年にLEDに置換している。後継のKLやKSプロセッサでは、このような多数のインジケータランプは存在しない。

## 開発中止と影響

[Altair_BASIC_Paper_Tape.jpg](https://ja.wikipedia.org/wiki/File:Altair_BASIC_Paper_Tape.jpg "fig:Altair_BASIC_Paper_Tape.jpg")。PDP-10によって原本が作成された。\]\]

PDP-10と（[PDP-11](../Page/PDP-11.md "wikilink")の後継である）[VAX](../Page/VAX.md "wikilink")[スーパーミニコンピュータ](https://ja.wikipedia.org/wiki/スーパーミニコンピュータ "wikilink")製品ラインが競合するようになったことから、DECはより高収益が望めるVAXに[ソフトウェア開発](../Page/ソフトウェア開発.md "wikilink")を集中することに決定した。PDP-10製品ラインの開発中止は[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に発表され、開発中だった[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")プロセッサ (Jupitor) も同時に中止となった。また、デスクトップ型PDP-10開発プロジェクト Minnow はプロトタイプ製作段階にまで到達していた\[5\]。

この出来事は[ITSや](../Page/Incompatible_Timesharing_System.md "wikilink")[ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")を生んだ文化の終焉を招くきっかけとなったが、[1990年代](../Page/1990年代.md "wikilink")になるとPDP-10をかじったことがあるというのが古い[ハッカー](../Page/ハッカー.md "wikilink")の勲章のように扱われるようになった。

PDP-10の[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")[命令であるLDB](../Page/命令_\(コンピュータ\).md "wikilink")(load byte)およびDPB(deposite byte)は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")[Common Lispの](../Page/Common_Lisp.md "wikilink")[関数として生き残っている](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。また、[PDP-6](../Page/PDP-6.md "wikilink")やPDP-10の36[ビット](../Page/ビット.md "wikilink")[ワード](../Page/ワード.md "wikilink")は18ビットのLISPポインタを2つ格納することができ、これは[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")処理系を考慮したものと言われている。

はPDP-10上に世界初の[アドベンチャーゲーム](../Page/アドベンチャーゲーム.md "wikilink")「[コロッサル・ケーブ・アドベンチャー](https://ja.wikipedia.org/wiki/コロッサル・ケーブ・アドベンチャー "wikilink")」を開発した。そのほかにもPDP-10上では、世界初のコンピュータ[野球](../Page/野球.md "wikilink")ゲーム（Don Daglow作、1971年）、初期の[コンピュータRPG](../Page/コンピュータRPG.md "wikilink") *Dungeon*（1975年）が作られた。[ウォルター・ブライト](https://ja.wikipedia.org/wiki/ウォルター・ブライト "wikilink")はPDP-10上で最初の[ウォー・シミュレーションゲーム](../Page/ウォー・シミュレーションゲーム.md "wikilink") *Empire* を作成した。Roy Trubshaw と Richard Bartle はPDP-10上で世界初のマルチユーザーダンジョンゲーム（[MUD](../Page/MUD.md "wikilink")）を作成した。さらにパソコンで人気となったテキストアドベンチャー『[ゾーク](../Page/ゾーク.md "wikilink")』もオリジナルはPDP-10で作られ、[インフォコムは開発用にPDP](https://ja.wikipedia.org/wiki/インフォコム_\(アメリカ合衆国の企業\) "wikilink")-10を数台使用していた。

1967年にシアトルの私立中学に入学した[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")は、学校で触れたゼネラル・エレクトリックの[GE-635でコンピュータに興味を持ち](../Page/GE-600シリーズ.md "wikilink")、その後CCCという会社でPDP-10に慣れ親しんだ。その後、友人の[ポール・アレン](../Page/ポール・アレン.md "wikilink")とともに[トラフォデータという名称で交通量計測システムを開発するが](https://ja.wikipedia.org/wiki/:en:Traf-O-Data "wikilink")、その際に、当時アルバイトをしていた電力事業団にあったPDP-10を用いた。また、1975年に[Altair 8800用](../Page/Altair_8800.md "wikilink")[BASIC](../Page/BASIC.md "wikilink")[インタプリタ](../Page/インタプリタ.md "wikilink")を開発した際には、ポール・アレンがPDP-10上に構築した Altair 8800 [エミュレータを用いた](../Page/エミュレータ_\(コンピュータ\).md "wikilink")。

## エミュレーションとシミュレーション

歴史的コンピュータのシミュレーションソフトウェアには、KS10 CPU をWindowsやUnix系マシンでエミュレートするモジュールが含まれている。DECが配布したテープのコピーもインターネット上にあってダウンロード可能であり、SIMH上でTOPS-10やTOPS-20、さらにはITSを動作させることは可能である。

Ken Harrenstien の KLH10 は[Unix系](../Page/Unix系.md "wikilink")システム上で、KL10B および KS10 プロセッサをエミュレートでき、KL10BではTOPS-10とTOPS-20の最終版が動作し、KS10ではITSとTOPS-10とTOPS-20の最終版が動作する\[6\]。

## 脚注

## 参考文献

  - [*DECsystem-10/DECSYSTEM-20 Processor Reference Manual* (DEC, 1982)](http://bitsavers.org/pdf/dec/pdp10/TOPS10_softwareNotebooks/vol05/AA-H391A-TK_DECsystem-10_DECSYSTEM-20_Processor_Reference_Jun1982.pdf)

  -
  - [C. Gordon Bell](../Page/ゴードン・ベル.md "wikilink"), [Alan Kotok](../Page/アラン・コトック.md "wikilink"), Thomas N. Hastings, Richard Hill, [*The Evolution of the DECsystem-10*](http://research.microsoft.com/users/GBell/Computer_Engineering/00000511.htm), in C. Gordon Bell, J. Craig Mudge, John E. McNamara, [*Computer Engineering: A DEC View of Hardware Systems Design*](http://research.microsoft.com/users/GBell/Computer_Engineering/contents.html) (Digital, Bedford, 1979)

## 関連項目

  - [PDPシリーズ](../Page/PDPシリーズ.md "wikilink") - [PDP-1](../Page/PDP-1.md "wikilink"), [PDP-6](../Page/PDP-6.md "wikilink"), [PDP-7](../Page/PDP-7.md "wikilink"), [PDP-8](../Page/PDP-8.md "wikilink"), **PDP-10**, [PDP-11](../Page/PDP-11.md "wikilink"), [PDP-12](https://ja.wikipedia.org/wiki/PDP-12 "wikilink")
  - [ITS](../Page/Incompatible_Timesharing_System.md "wikilink")
  - [TOPS-10](../Page/TOPS-10.md "wikilink"), [TOPS-20](../Page/TOPS-20.md "wikilink")

## 外部リンク

  - [36 Bits Forever\!](http://www.inwap.com/pdp10/)
  - [PDP-10 stuff](http://pdp10.nocrew.org/)
  - [PDP10 Miscellany Page](http://www.ultimate.com/phil/pdp10/)
  - [Life in the Fast AC's](http://www.ultimate.com/phil/pdp10/Fast-ACs)
  - [Columbia University DEC PDP-10 page](http://www.columbia.edu/acis/history/pdp10.html)
  - [Panda Programming TOPS-20 page](http://panda.com/tops-20/)
  - [Living Computer Museum](http://www.livingcomputermuseum.org/), [ポール・アレン](../Page/ポール・アレン.md "wikilink")によるPDP-10を含むDECマシンに関するコレクションへのポータル
  - [Empire](ftp://ftp.classicempire.com/pdp10.zip) PDP-10用FORTRAN-10ソースのzipファイル from [Classic Empire](http://www.classicempire.com)
  - [PDP-10 software archive at Trailing Edge](http://pdp-10.trailing-edge.com/)
  - Computer World [ad for Personal Mainframe](http://www.computerworld.com/action/article.do?command=viewArticleBasic&articleId=9024559&pageNumber=6)

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink")

1.  , "It was large—even DEC's own literature called \[the PDP-10\] a mainframe."
2.
3.  Digital Equipment Corporation, *The digital small computer handbook*, p. 376
4.
5.  ["DEC 36-bit Computers"](http://www.36bit.org/dec/) Retrieved on April 4, 2009.
6.  Tim Shoppa ["Announcing KLH10"](http://www.columbia.edu/kermit/ftp/e/klh10.txt), November 10, 2001. Retrieved April 4, 2009.