> この記事は[AMD Am2900](https://ja.wikipedia.org/wiki/AMD_Am2900)から翻訳されています。


**Am2900** は、[AMDが](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")1975年に発売した[集積回路](../Page/集積回路.md "wikilink")（ICチップ）のファミリである\[1\]。これらのICは、機能的には[ビットスライス](../Page/ビットスライス.md "wikilink")方式で[プロセッサ](../Page/プロセッサ.md "wikilink")のセットを構成するものであり、プロセステクノロジは[バイポーラトランジスタ](../Page/バイポーラトランジスタ.md "wikilink")である。それぞれがコンピュータ[制御装置](../Page/制御装置.md "wikilink") (CCU) の異なる側面を表すモジュラーコンポーネントとして使用できるように設計された。Am2900ファミリは、ビットスライス方式であるため、データ/アドレス/命令を4ビットの任意の倍数になるようにCCUを実装することができた。このモジュール方式の大きな欠点は、単一のCPU ICでできることを実装するために、より多くのICを必要とすることであった。Am2901チップは、[演算論理ユニット](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")(ALU)であり、シリーズのコアである。4ビットでカウントし、バイナリ操作やさまざまな[ビットシフト演算を実装していた](../Page/ビット演算.md "wikilink")。

2901とファミリの他のいくつかのチップは、1975年のMotorolaとRaytheonを皮切りに、Cypress Semiconductor、National Semiconductor、NEC、Thomson、およびSigneticsなど、非常に多くの他のメーカーから[セカンド・ソースとして供給された](../Page/セカンドソース.md "wikilink")。ソビエト連邦とその後のロシアでは、Am2900ファミリーは1804シリーズとして製造されていた (例: Am2901はKR1804VS1と指定/) が\[2\]\[3\]、2016年現在も生産されている\[4\]。

## 採用例

例えばALUのみ使用、というものもあれば、システム全体として本系列を採用しているものもある。以下では特に識別はしていない。

  - [アポロ・コンピュータ](../Page/アポロコンピュータ.md "wikilink") Tern ファミリー: DN460, DN660, DSP160. すべて同じシステムボードを使用しておりMC68010命令セットをエミュレートする\[5\]。

  - 木星探査機[ガリレオの姿勢制御コンピュータやNASA製航空機で使われた](../Page/ガリレオ_\(探査機\).md "wikilink") [Itek](https://ja.wikipedia.org/wiki/:en:Itek "wikilink") Advanced Technology Airborne Computer (ATAC)。Am2900ファミリを使った16ビットで16本のレジスタを持つコンピュータである。ガリレオに搭載されたATACには4つの特殊な命令が追加され、2901の放射線耐性を強化したバージョンも使われた\[6\]。

  - [データゼネラル Nova 4](https://ja.wikipedia.org/wiki/データゼネラルNova "wikilink"): Am2901 [ALUを並列に構成して](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")16ビットワードを扱えるようにしていた。基板には15個の Am2901 ALU が搭載されたものもある\[7\]。

  - [DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") [PDP-11](../Page/PDP-11.md "wikilink")の機種 PDP-11/23、PDP-11/34、PDP-11/44 の浮動小数点オプション（それぞれ FPF11、FP11-A、FP11-F）\[8\]\[9\]

  - DEC [VAX 11/730](https://ja.wikipedia.org/wiki/VAX#VAXシステム "wikilink"): CPUにAM2901を8個使用した\[10\]。

  - [Hewlett-Packard](https://ja.wikipedia.org/wiki/Hewlett-Packard "wikilink") (現在は[Keysight](https://ja.wikipedia.org/wiki/:en:Keysight "wikilink")) HP 1000 [A-series](https://ja.wikipedia.org/wiki/:en:HP_2100#1000_series "wikilink") model A600: 16ビットプロセッサに4つのAM2901 ALUを使用した\[11\]。

  - [ゼロックス](../Page/ゼロックス.md "wikilink") Dandelion: [Xerox Star](../Page/Xerox_Star.md "wikilink") と[LISPマシン](../Page/LISPマシン.md "wikilink") Xerox 1108 で使われた。\[12\]

  - イギリスの [GEC 4000シリーズミニコンピュータ](https://ja.wikipedia.org/wiki/:en:GEC_4000_series "wikilink"): 4060/4150/4160（いずれもAm2901を使った16ビット構成）と 4090/418x/419x（Am2901を18個使って、32ビット整数ALUと64ビット倍精度FPUを構成）\[13\]

  - [DEC](https://ja.wikipedia.org/wiki/デジタル・イクイップメント・コーポレーション "wikilink") [PDP-10](../Page/PDP-10.md "wikilink") の KS10 モデル\[14\]

  - NCRの [Joel McCormack](https://ja.wikipedia.org/wiki/:en:Joel_McCormack "wikilink") が設計した [UCSD Pascal](../Page/UCSD_p-System.md "wikilink") P-machine プロセッサ

  - [MAI Basic Four](https://ja.wikipedia.org/wiki/:en:MAI_Basic_Four "wikilink") の一部マシン\[15\]

  - グラフィックスコンピュータ

  - [SM-1420](https://ja.wikipedia.org/wiki/:en:SM-1420 "wikilink") - ソ連のPDP-11クローン\[16\]。他のクローンでも使われていたと見られている\[17\]。

  - [Lilith](../Page/Lilith.md "wikilink") - [ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")（[チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")）

  - [アタリの](../Page/アタリ_\(企業\).md "wikilink")[ベクターグラフィックス](https://ja.wikipedia.org/wiki/ベクターグラフィックス "wikilink")・[アーケードマシン](../Page/アーケードゲーム.md "wikilink"): [Tempest](https://ja.wikipedia.org/wiki/:en:Tempest_\(arcade_game\) "wikilink"), [Battlezone](https://ja.wikipedia.org/wiki/:en:Battlezone_\(1980_video_game\) "wikilink"), [Red Baron](https://ja.wikipedia.org/wiki/:en:Red_Baron_\(arcade_game\) "wikilink") ではそれぞれ数学ボックスの補助回路基板に4個のAm2901 ICが使用された。

  - アタリのラスターグラフィックス・アーケードマシン: [I, Robot](https://ja.wikipedia.org/wiki/:en:I,_Robot_\(video_game\) "wikilink") はポリゴンを塗りつぶした最初の商用ゲームで\[18\]、4個のAMD 2901チップを中心に構築された演算プロセッサを搭載した\[19\]。

  - [Pixar Image Computer](https://ja.wikipedia.org/wiki/Pixar_Image_Computer "wikilink"): それぞれ4つのAm2900を搭載した4つのチャネルプロセッサ

  - Simulation Excel (Sim-X), [Oslo, Norway](https://ja.wikipedia.org/wiki/:en:Oslo,_Norway "wikilink"): 文字書体ワークステーション/タイプセッター。4つのプロセッサのうちの1つは、4つの2901スライスと1つの2910アドレスシーケンサから構築された16ビットマイクロコード化された計算・変換エンジンであった。Sim-Xマシンは、16ビットの整数乗算器を使用してグラフィカル変換を最適化した\[20\]。

  - Eventide H949 Harmonizer: 4つのAm2901チップ(といくつかのマイクロコードPROM)がアドレス生成とDACシステムの基準電圧の生成に使用された。オーディオは2901 ALUセクションでは処理されなかった。

  - 多くのSiemens TelepermとS5 PLCは、産業用制御で使用され、2900シリーズを使用して構築された。

  - [AT\&T](../Page/AT&T.md "wikilink") [3B20D](https://ja.wikipedia.org/wiki/3Bシリーズ_\(コンピュータ\) "wikilink") : 通信制御用の多重化された高可用性プロセッサで、4個のAMD 2901を用いた\[21\]。

  - Metheus / Barco Omega 400および500シリーズのグラフィックシステム: 1982年のディスプレイプロセッサで、4つのAm2901チップ(および8個のマイクロコードPROM)が使用された。

  - [Geac Computer Corporation](https://ja.wikipedia.org/wiki/:en:Geac_Computer_Corporation "wikilink") 2000, 6000, 8000, 9000はすべて4個のAM2901チップをベースとした。2000は薬局で、その他のモデルは図書館、銀行、保険の自動化に使用された。

  - [Ferranti Argus 700](https://ja.wikipedia.org/wiki/:en:Ferranti_Argus#Argus%20600%20and%20700 "wikilink") (700F、700G): AM2901デバイスが使用され、A700の周辺チャネルコントローラの一部ではハードドライブやフロッピードライブなどに使用された。

  - [High Level Hardware Limited Orion](https://ja.wikipedia.org/wiki/:en:HLH_Orion "wikilink"): Unixが動作するユーザ・マイクロコード可能なミニコンピュータ。書き込み可能なマイクロコードで、命令セットを再定義してカスタマイズできた\[22\]。

## ファミリ

[thumb](https://ja.wikipedia.org/wiki/ファイル:KL_AMD_2901.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:KL_AMD_Am2903.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Ic-photo-AMD--AM2909DC-\(AM2900\).png "wikilink") Am2900 Family Data Book に掲載されているものは以下の通り\[23\]。

  - Am2901 – 4ビットスライス[ALU](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")（1975年）
  - Am2902 – [ルックアヘッド・キャリー生成器](https://ja.wikipedia.org/wiki/加算器#キャリー先読み "wikilink")
  - Am2903 – 4ビットスライスALU、[乗算器](../Page/乗算器.md "wikilink")付き
  - Am2904 – ステータス/シフト制御装置
  - Am2905 – バス・トランシーバー
  - Am2906 – [パリティビット](../Page/パリティビット.md "wikilink")付きバス・トランシーバー
  - Am2907 – [パリティビット](../Page/パリティビット.md "wikilink")付きバス・トランシーバー
  - Am2908 – [パリティビット](../Page/パリティビット.md "wikilink")付きバス・トランシーバー
  - Am2909 – 4ビットスライス・アドレスシーケンサ
  - Am2910 – 12ビットアドレスシーケンサ
  - Am2911 – 4ビットスライス・アドレスシーケンサ
  - Am2912 – バス・トランシーバー
  - Am2913 – 優先度付き[割り込みエキスパンダー](../Page/割り込み_\(コンピュータ\).md "wikilink")
  - Am2914 – 優先度付き割り込みコントローラ
  - Am2915 – 4ビット 3状態バス・トランシーバー
  - Am2916 – 4ビット 3状態バス・トランシーバー
  - Am2917 – 4ビット 3状態バス・トランシーバー
  - Am2918 – [命令レジスタ](https://ja.wikipedia.org/wiki/命令レジスタ "wikilink"), 4ビット D レジスタ
  - Am2919 – [命令レジスタ](https://ja.wikipedia.org/wiki/命令レジスタ "wikilink"), 4ビット レジスタ
  - Am2920 – 8ビット [D型フリップフロップ](https://ja.wikipedia.org/wiki/フリップフロップ#D型 "wikilink")
  - Am2921 – 1-to-8 [デコーダ](https://ja.wikipedia.org/wiki/デコーダ "wikilink")
  - Am2922 – 8-入力 [マルチプレクサ](../Page/マルチプレクサ.md "wikilink") (MUX)
  - Am2923 – 8-入力 MUX
  - Am2924 – 3-ラインから 8-ラインの[デコーダ](https://ja.wikipedia.org/wiki/デコーダ "wikilink")
  - Am2925 – [システムクロック](../Page/クロック.md "wikilink")・ジェネレータおよびドライバ
  - Am2926 – ショットキー 4ビット3状態バスドライバ
  - Am2927/Am2928 – 4ビット3状態バス・トランシーバ
  - Am2929 – ショットキー 4ビット3状態バスドライバ
  - Am2930 – 主記憶プログラム制御
  - Am2932 – 主記憶プログラム制御
  - Am2940 – [DMAジェネレータ](../Page/Direct_Memory_Access.md "wikilink")
  - Am2942 – プログラマブル・タイマー/[カウンタ](../Page/カウンタ_\(電子回路\).md "wikilink")/DMAジェネレータ
  - Am2946/Am2947 – 8ビット 3状態 双方向バス・トランシーバー
  - Am2948/Am2949 – 8ビット 3状態 双方向バス・トランシーバー
  - Am2950/Am2951 – 8ビット 双方向 I/Oポート
  - Am2954/Am2955 – 8ビット・レジスタ
  - Am2956/Am2957 – 8ビット・ラッチ
  - Am2958/Am2959 – 8ビット・バッファ/ラインドライバ/ラインレシーバー
  - Am2960 – カスケード接続可能な16ビット・エラー検出/訂正装置
  - Am2961/Am2962 – 4ビット エラー訂正・複数バス・バッファ
  - Am2964 – ダイナミックメモリ・コントローラ
  - Am2965/Am2966 – 8ビット・ダイナミックメモリ・ドライバ

74F2960 / Am2960 のように7400シリーズの名称も持つチップも多い。

## 脚注

## 参考文献

  - [Am2900 Family Data Book](http://www.bitsavers.org/pdf/amd/_dataBooks/1979_AMD_2900family.pdf) Accessed 12 Nov, 2005.

## 外部リンク

  - [Introduction to Designing with the Am2900 Family of Microprogramable Bipolar Devices Vol 1](http://www.bitsavers.org/pdf/amd/ED2900A_vol1_Jan85.pdf) Bitsavers' PDF Document Archive
  - [Introduction to Designing with the Am2900 Family of Microprogramable Bipolar Devices Vol 2](http://www.bitsavers.org/pdf/amd/ED2900A_vol2_Jan85.pdf) Bitsavers' PDF Document Archive
  - [Am29C300/29300 Data Book](http://www.bitsavers.org/pdf/amd/_dataBooks/1988_29C3xx_Series.pdf) Bitsavers' PDF document archive
  - [CPU-World](http://www.cpu-world.com/CPUs/2901/) チップの写真あり
  - [Bit-Slice Design: micro-controllers and ALUs. an Introduction to the Am2900 Family](http://www10.dacafe.com/book/parse_book.php?article=BITSLICE/bitslcP.html)
  - [Bit-Sliced Microprocessor of the Am2900 Family](http://research.microsoft.com/users/gbell/Computer_Structures_Principles_and_Examples/csp0184.htm)

[Category:アドバンスト・マイクロ・デバイセズの製品](https://ja.wikipedia.org/wiki/Category:アドバンスト・マイクロ・デバイセズの製品 "wikilink") [Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.
2.
3.
4.
5.
6.  ["Computers in Spaceflight: The NASA Experience" - Chapter Six - - Distributed Computing On Board Voyager and Galileo -](http://history.nasa.gov/computers/Ch6-3.html)
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22. <http://hlhco.info/OrionBrochure.pdf>
23.