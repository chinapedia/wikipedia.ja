> この記事は[AMD Am2900](https://ja.wikipedia.org/wiki/AMD_Am2900)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:KL_AMD_2901.jpg "wikilink") **Am2900** は[アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")(AMD)が[1975年](../Page/1975年.md "wikilink")に開発した[集積回路](../Page/集積回路.md "wikilink")（ICチップ）のファミリである。[バイポーラトランジスタ](https://ja.wikipedia.org/wiki/バイポーラトランジスタ "wikilink")を使用した[ビットスライス](https://ja.wikipedia.org/wiki/ビットスライス "wikilink")方式のチップファミリであり、複数のチップを組み合わせることで[CPU](../Page/CPU.md "wikilink")を構成することができる。[ビットスライス](https://ja.wikipedia.org/wiki/ビットスライス "wikilink")技術を使うことにより、Am2900 ファミリではデータ/アドレス/命令のビット幅を4ビットの任意の倍数長に設計することが可能である。この方式の難点はCPUに機能を詰め込もうとするとチップ数が膨大になる点であった。Am2901 は[演算装置](../Page/演算装置.md "wikilink")(ALU)であり、ファミリの中核となっている。これには4ビットの各種二進演算機能が盛り込まれている（[ビットシフトを含む](https://ja.wikipedia.org/wiki/ビット演算#ビットシフト "wikilink")）。

## Am2900 ファミリのチップで構成されたコンピュータ

以下に Am2900 を使用していたと判明しているコンピュータを列挙する。

  - 木星探査機[ガリレオの姿勢制御コンピュータやNASA製航空機で使われた](https://ja.wikipedia.org/wiki/ガリレオ_\(探査機\) "wikilink") [Itek](https://ja.wikipedia.org/wiki/:en:Itek "wikilink") Advanced Technology Airborne Computer (ATAC)。Am2900ファミリを使った16ビットで16本のレジスタを持つコンピュータである。ガリレオに搭載されたATACには4つの特殊な命令が追加され、2901の放射線耐性を強化したバージョンも使われた\[1\]。

  - [データゼネラル](https://ja.wikipedia.org/wiki/データゼネラル "wikilink") Nova 4: Am2901 [ALUを並列に構成して](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")16ビットワードを扱えるようにしていた。基板には15個の Am2901 ALU が搭載されたものもある。\[2\]

  - [DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") [PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")の機種 PDP-11/23、PDP-11/34、PDP-11/44 の浮動小数点オプション（それぞれ FPF11、FP11-A、FP11-F）\[3\]\[4\]

  - [ゼロックス](../Page/ゼロックス.md "wikilink") Dandelion: [Xerox Star](https://ja.wikipedia.org/wiki/Xerox_Star "wikilink") と[LISPマシン](https://ja.wikipedia.org/wiki/LISPマシン "wikilink") Xerox 1108 で使われた。\[5\]

  - イギリスの GEC 4060/4150/4160（いずれもAm2901を使った16ビット構成）と 4090/418x/419x（Am2901を18個使って、32ビット整数ALUと64ビット倍精度FPUを構成）\[6\]

  - [DEC](https://ja.wikipedia.org/wiki/デジタル・イクイップメント・コーポレーション "wikilink") [PDP-10](https://ja.wikipedia.org/wiki/PDP-10 "wikilink") の KS10 モデル\[7\]

  - NCRの [Joel McCormack](https://ja.wikipedia.org/wiki/:en:Joel_McCormack "wikilink") が設計した [UCSD Pascal](https://ja.wikipedia.org/wiki/UCSD_p-System "wikilink") P-machine プロセッサ

  - [MAI Basic Four](https://ja.wikipedia.org/wiki/:en:MAI_Basic_Four "wikilink") の一部マシン\[8\]

  - グラフィックスコンピュータ

  - [SM-1420](https://ja.wikipedia.org/wiki/:en:SM-1420 "wikilink") - ソ連のPDP-11クローン\[9\]。他のクローンでも使われていたと見られている\[10\]。

  - [Lilith](https://ja.wikipedia.org/wiki/Lilith "wikilink") - [ニクラウス・ヴィルト](https://ja.wikipedia.org/wiki/ニクラウス・ヴィルト "wikilink")（[チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")）

  - [AT\&T](../Page/AT&T.md "wikilink") [3B20D](https://ja.wikipedia.org/wiki/:en:3B_series_computers "wikilink") コンピュータ\[11\]

## Am2900 ファミリ

[thumb](https://ja.wikipedia.org/wiki/ファイル:KL_AMD_Am2903.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Ic-photo-AMD--AM2909DC-\(AM2900\).png "wikilink") Am2900 Family Data Book に掲載されているものは以下の通り\[12\]。

  - Am2901 – 4ビットスライス[ALU](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")（1975年）
  - Am2902 – [ルックアヘッド・キャリー生成器](https://ja.wikipedia.org/wiki/加算器#キャリー先読み "wikilink")
  - Am2903 – 4ビットスライスALU、[乗算器](https://ja.wikipedia.org/wiki/乗算器 "wikilink")付き
  - Am2904 – ステータス/シフト制御装置
  - Am2905 – バス・トランシーバー
  - Am2906 – [パリティビット](https://ja.wikipedia.org/wiki/パリティビット "wikilink")付きバス・トランシーバー
  - Am2907 – [パリティビット](https://ja.wikipedia.org/wiki/パリティビット "wikilink")付きバス・トランシーバー
  - Am2908 – [パリティビット](https://ja.wikipedia.org/wiki/パリティビット "wikilink")付きバス・トランシーバー
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
  - Am2922 – 8-入力 [マルチプレクサ](https://ja.wikipedia.org/wiki/マルチプレクサ "wikilink") (MUX)
  - Am2923 – 8-入力 MUX
  - Am2924 – 3-ラインから 8-ラインの[デコーダ](https://ja.wikipedia.org/wiki/デコーダ "wikilink")
  - Am2925 – [システムクロック](../Page/クロック.md "wikilink")・ジェネレータおよびドライバ
  - Am2926 – ショットキー 4ビット3状態バスドライバ
  - Am2927/Am2928 – 4ビット3状態バス・トランシーバ
  - Am2929 – ショットキー 4ビット3状態バスドライバ
  - Am2930 – 主記憶プログラム制御
  - Am2932 – 主記憶プログラム制御
  - Am2940 – [DMAジェネレータ](../Page/Direct_Memory_Access.md "wikilink")
  - Am2942 – プログラマブル・タイマー/[カウンタ](https://ja.wikipedia.org/wiki/カウンタ_\(電子回路\) "wikilink")/DMAジェネレータ
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

74F2960 / Am2960 のように7400シリーズの名称も持つチップが多い。

## 脚注

## 参考文献

  - [Am2900 Family Data Book](http://www.bitsavers.org/pdf/amd/_dataBooks/1979_AMD_2900family.pdf) Accessed 12 Nov, 2005.

## 関連項目

  - [AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")
  - [ビットスライス](https://ja.wikipedia.org/wiki/ビットスライス "wikilink")

## 外部リンク

  - [Introduction to Designing with the Am2900 Family of Microprogramable Bipolar Devices Vol 1](http://www.bitsavers.org/pdf/amd/ED2900A_vol1_Jan85.pdf) Bitsavers' PDF Document Archive
  - [Introduction to Designing with the Am2900 Family of Microprogramable Bipolar Devices Vol 2](http://www.bitsavers.org/pdf/amd/ED2900A_vol2_Jan85.pdf) Bitsavers' PDF Document Archive
  - [Am29C300/29300 Data Book](http://www.bitsavers.org/pdf/amd/_dataBooks/1988_29C3xx_Series.pdf) Bitsavers' PDF document archive
  - [CPU-World](http://www.cpu-world.com/CPUs/2901/) チップの写真あり
  - [Bit-Slice Design: micro-controllers and ALUs. an Introduction to the Am2900 Family](http://www10.dacafe.com/book/parse_book.php?article=BITSLICE/bitslcP.html)
  - [Bit-Sliced Microprocessor of the Am2900 Family](http://research.microsoft.com/users/gbell/Computer_Structures_Principles_and_Examples/csp0184.htm)

[Category:アドバンスト・マイクロ・デバイセズの製品](https://ja.wikipedia.org/wiki/Category:アドバンスト・マイクロ・デバイセズの製品 "wikilink") [Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.  ["Computers in Spaceflight: The NASA Experience" - Chapter Six - - Distributed Computing On Board Voyager and Galileo -](http://history.nasa.gov/computers/Ch6-3.html)
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.