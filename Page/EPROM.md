> この記事は[EPROM](https://ja.wikipedia.org/wiki/EPROM)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Eprom.jpg "wikilink") **EPROM** (Erasable Programmable Read Only Memory)は、[半導体メモリ](https://ja.wikipedia.org/wiki/半導体メモリ "wikilink")の一種で、デバイスの利用者が書き込み・消去可能な[ROMである](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")。電源を切っても記憶内容が保持される[不揮発性メモリ](https://ja.wikipedia.org/wiki/不揮発性メモリ "wikilink")の一種でもある。[フローティングゲートMOSFET](https://ja.wikipedia.org/wiki/フローティングゲートMOSFET "wikilink")のアレイで構成されており、通常のデジタル回路よりも印加する電圧が高い専用機器を使って個々のMOSFETに書き込むことができる。データやプログラムの書き込みを行ったEPROMは、強い[紫外線](https://ja.wikipedia.org/wiki/紫外線 "wikilink")光を照射することでその記憶内容を消去できる。そのため、[パッケージ中央上部に](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\) "wikilink")[石英ガラス](https://ja.wikipedia.org/wiki/石英ガラス "wikilink")の窓があって[シリコンチップが見えているので](https://ja.wikipedia.org/wiki/ケイ素 "wikilink")、容易にEPROMだとわかる。このようなEPROMを特に[UV-EPROM](https://ja.wikipedia.org/wiki/UV-EPROM "wikilink")と呼ぶこともある。

消去方式の異なる[EEPROM](https://ja.wikipedia.org/wiki/EEPROM "wikilink")（電気的に消去可能なPROM, Electrically Erasable PROM）などもある。[コンピュータ](../Page/コンピュータ.md "wikilink")制御機器の試作品や製品をはじめ、[パソコンの](../Page/パーソナルコンピュータ.md "wikilink")[BIOS ROMなど](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、多くの機器に搭載されている。近年は、[フラッシュメモリ](https://ja.wikipedia.org/wiki/フラッシュメモリ "wikilink")に置き換わりつつある。

## 動作

[thumb](https://ja.wikipedia.org/wiki/ファイル:Uv_prom.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Floating_gate_transistor.png "wikilink") EPROMメモリセルの開発は、トランジスタのゲートの配線が壊れた集積回路を調査することから始まった。配線のない孤立したゲートに溜まった電荷により、その特性が変化したのである。EPROMは1971年に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の [Dov Frohman](https://ja.wikipedia.org/wiki/:en:Dov_Frohman "wikilink") が発明し、1972年にアメリカ合衆国特許第3660189号を取得した。

EPROMで1ビットのデータが格納される場所は、1個の[電界効果トランジスタ](https://ja.wikipedia.org/wiki/電界効果トランジスタ "wikilink")である。それぞれの電界効果トランジスタは、デバイスの半導体本体中のチャネルで構成される。ソースとドレインはチャネルの両端に形成される。絶縁酸化層がチャネル上を覆い、伝導性（ケイ素またはアルミニウム）のゲート電極がその上に配置され、さらに分厚い酸化層がゲート電極の上に形成される。フローティングゲートには配線がなく集積回路内の他の部品とは繋がっておらず、周囲は酸化層によって完全に絶縁されている。コントロールゲートがその上に配置され、それをさらに酸化層で覆う\[1\]。

EPROMからデータを読み出すには、EPROMのアドレスピンにアドレスを表す値を入力する。するとEPROM内でそれをデコードし、対応する1ワード（通常、8ビット）のメモリセルを出力バッファ増幅回路に接続する。ワード内の各ビットに対応するトランジスタがオン状態かオフ状態かによって1または0を示す。

電界効果トランジスタのスイッチング状態は、トランジスタのコントロールゲート上の電圧によって制御される。ゲートに電圧がかかっているとトランジスタ内に伝導経路ができ、スイッチがオンとなる。フローティングゲートに電荷を蓄えるとゲートに電圧をかけるのと同じ効果が得られ、それによってデータを記憶することができる。

データを書き込むには、アドレスを指定しつつ、トランジスタに通常よりも高い電圧を印加する。それによって電子のなだれ放出が起き、絶縁酸化物層を通過してゲート電極上に電荷を蓄積するのに十分なエネルギーが与えられる。高い電圧の印加をやめると、電荷が電極上に閉じ込められる\[2\]。ゲートを取り囲む酸化ケイ素の層は絶縁値が高いため、蓄えられた電荷は簡単には漏れ出すことができず、データは数十年間保持できる。書き込み時の高電圧がシリコンにストレスを与えるため、書き換え可能な回数はおおよそ20回前後である。

[EEPROM](https://ja.wikipedia.org/wiki/EEPROM "wikilink")とは異なり、書き込みは電気的に何度も行えるというわけではない。トランジスタのアレイに格納されたデータを消去するには、[ダイに直接](https://ja.wikipedia.org/wiki/ダイ_\(集積回路\) "wikilink")[紫外線](https://ja.wikipedia.org/wiki/紫外線 "wikilink")(UV)をあてる。UV光の光子によって酸化ケイ素中で電離が発生し、フローティングゲートに蓄積された電荷が絶縁膜を通って拡散する。メモリアレイの一部のみ選択的に紫外線を当てるということはできないため、全メモリが同時に消去される。一般的な大きさのUVランプを使うと、消去には数分かかる。太陽光の場合数週間でメモリが消去され、室内の[蛍光灯](https://ja.wikipedia.org/wiki/蛍光灯 "wikilink")にさらした場合は消去に数年以上かかる\[3\]。一般にEPROMを使用する回路にUVランプを組み込むことは実用的ではないため、内容を消去したいEPROMは装置から外される。遮光シールを貼って適切な取り扱いをすれば、十年単位で記憶を保持できると言われる。しかし、シールを貼らずにおくと、[太陽光](https://ja.wikipedia.org/wiki/太陽光 "wikilink")や[蛍光灯](https://ja.wikipedia.org/wiki/蛍光灯 "wikilink")の光に含まれる紫外線で短期のうちに内容が消えてしまう。また、動作中に[カメラ](../Page/カメラ.md "wikilink")の[フラッシュのような](https://ja.wikipedia.org/wiki/エレクトロニックフラッシュ "wikilink")、強烈な光を浴びせると読み出し時に誤った値を出力する事がある。

## 詳細

石英ガラスの窓は高価だったため、廉価版の[ワンタイムPROM](https://ja.wikipedia.org/wiki/PROM#OTPROM "wikilink")(OTP:One-Time Programmable ROM)として窓のないパッケージにダイを収めた製品も作られたが、これは消去ができないため一度書き込むと書き換えられない。また、こうすると消去機能のテストを省略できるため、そういった面でもコストが低減された。OTP版のEPROMやEPROM内蔵型マイクロコントローラが製造された。しかし、OTP EPROM は少量生産用途ではコストが問題とならないため[EEPROM](https://ja.wikipedia.org/wiki/EEPROM "wikilink")に徐々に置き換えられていき、大量生産用途では[フラッシュメモリ](https://ja.wikipedia.org/wiki/フラッシュメモリ "wikilink")に置き換えられていった。

EPROMは書き込まれた内容を約10年から20年保持するとされている\[4\]。また、読み出し回数に制限はない。消去用の窓は太陽光などにさらされて内容が消去されることを防ぐため、不透明なシールを貼ってカバーする必要がある。古いPCの[BIOSチップにEPROMを使っていることが多く](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、消去用の窓はそのBIOSを作ったメーカー名、BIOSのリビジョン、コピーライト表示などが書かれたシールで覆っていることが多かった。BIOSチップは消去窓のないEEPROMやフラッシュメモリに置き換えられているが、今でもそのようなラベルが貼ってあることが多い。

EPROMの消去は400[nmより短い波長の光によって起きる](https://ja.wikipedia.org/wiki/ナノメートル "wikilink")。太陽光では1週間から3週間、室内の蛍光灯では3年ほど光を当て続けるとメモリの内容が消去されることになる。推奨される消去方法は、波長 253.7 nm で最低でも15WのUVランプを20から30分照射するというもので、ランプとEPROMの距離は約1インチ（2.54cm）とする。

[X線](https://ja.wikipedia.org/wiki/X線 "wikilink")でも記憶内容を消去でき、5×10<sup>4</sup> ( = 500 [J](https://ja.wikipedia.org/wiki/ジュール "wikilink")/kg) [ラド](https://ja.wikipedia.org/wiki/ラド "wikilink") 以上のX線照射（商用のX線発生装置で容易に達成される量）で消去される\[5\]。このとき石英ガラスの窓を必要としない。しかし、X線によって半導体が変質する可能性があるため、X線照射後にオーブンで焼きなましたり、詳細に検査する必要がある。そのため石英ガラスの窓を設ける方法が選択された\[6\]。

EPROMは限度はあるが、何度も消去可能である。ゲートのまわりの酸化ケイ素には消去のたびにダメージが蓄積され、数千回の消去でチップの信頼性が低下する。EPROMの書き換えは他のメモリに比べると時間がかかる。集積度を高めると酸化絶縁層に紫外線が当たりにくくなるため、紫外線による消去が難しくなる。パッケージ内の小さなゴミでさえ、一部のメモリセルを消去するのを妨げることがある\[7\]。

## 用途

大量生産する場合は[マスクROM](https://ja.wikipedia.org/wiki/マスクROM "wikilink")が最もコストが低くなる。しかし、ICマスク層を格納するデータに従って設計するため、数週間の準備期間が必要となる。当初EPROMは大量生産用途には高価すぎて使えないと見られ、開発途中でしか使われないと見られていた。間もなく、少量生産ならEPROMでもコスト的に見合うことが判明し、[ファームウェア](https://ja.wikipedia.org/wiki/ファームウェア "wikilink")を素早く更新できるという利点も判明した。なお、多品種少量生産向けに、パッケージの窓を廃して廉価なプラスチックモールドとし、[ワンタイムPROM](https://ja.wikipedia.org/wiki/PROM#OTPROM "wikilink")(OTP:One-Time Programmable ROM)とした製品もあったが、メモリチップ自体は普通のUV-EPROMであり、プログラミングにはUV-EPROM用のライタ等をそのまま流用できる。

[EEPROM](https://ja.wikipedia.org/wiki/EEPROM "wikilink")や[フラッシュメモリ](https://ja.wikipedia.org/wiki/フラッシュメモリ "wikilink")が登場する以前、プログラム格納用EPROMを内蔵した[マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")も存在した。例えば、[Intel 8048](https://ja.wikipedia.org/wiki/Intel_8048 "wikilink")、[Freescale 68HC11](https://ja.wikipedia.org/wiki/Freescale_68HC11 "wikilink")、[PICマイクロコントローラの](https://ja.wikipedia.org/wiki/PIC_\(コントローラ\) "wikilink")"C"バージョンなどがある。これらのマイクロコントローラにはやや高価な石英ガラスの窓付きのバージョンがあり、EPROMのように内蔵プログラムを消去できるのでプログラム開発・デバッグに便利だった。開発後の生産用に窓のない廉価版もあった。

## EPROM の容量と機種

EPROMはパッケージの大きさの面でも記憶容量の面でも様々なものがある。メーカーが異なっていても機種番号が同じものは、少なくとも読み出しに関しては互換性がある。ただし書き込み方法はメーカーによって微妙に異なる。

ほとんどのEPROMは、A9ピンに12Vを印加して "signature mode" にすると2バイトの識別データを読み出せる。ただしこれは普遍的ではないので、メーカーと機種を手動で確認してから、適切な書き込み手段を選択すべきである\[8\]。

最初のEPROMはIntel 1702Aであり、これはP-MOS構造のため、負電圧が必要など、使いにくいものであった。その後、2716以降、5V単一電源になり、使いやすさが向上した。その後は、ピン配置の互換を出来るだけ保ちながら、容量を増やしたものが提供されている。

| EPROMの機種       | 容量 — [ビット](https://ja.wikipedia.org/wiki/ビット "wikilink")数 | 容量 — [バイト数](https://ja.wikipedia.org/wiki/バイト_\(情報\) "wikilink") | 容量 - [16進](https://ja.wikipedia.org/wiki/十六進法 "wikilink") | 最終アドレス（[16進](https://ja.wikipedia.org/wiki/十六進法 "wikilink")） |
| -------------- | --------------------------------------------------------- | ---------------------------------------------------------------- | --------------------------------------------------------- | ------------------------------------------------------------ |
| 1702, 1702A    | 2 [Kbit](https://ja.wikipedia.org/wiki/キロビット "wikilink")  | 256                                                              | 100                                                       | FF                                                           |
| 2704           | 4 Kbit                                                    | 512                                                              | 200                                                       | 1FF                                                          |
| 2708           | 8 Kbit                                                    | 1 [KB](https://ja.wikipedia.org/wiki/キロバイト "wikilink")           | 400                                                       | 3FF                                                          |
| 2716, 27C16    | 16 Kbit                                                   | 2 KB                                                             | 800                                                       | 7FF                                                          |
| 2732, 27C32    | 32 Kbit                                                   | 4 KB                                                             | 1000                                                      | FFF                                                          |
| 2764, 27C64    | 64 Kbit                                                   | 8 KB                                                             | 2000                                                      | 1FFF                                                         |
| 27128, 27C128  | 128 Kbit                                                  | 16 KB                                                            | 4000                                                      | 3FFF                                                         |
| 27256, 27C256  | 256 Kbit                                                  | 32 KB                                                            | 8000                                                      | 7FFF                                                         |
| 27512, 27C512  | 512 Kbit                                                  | 64 KB                                                            | 10000                                                     | FFFF                                                         |
| 27C010, 27C100 | 1 [Mbit](https://ja.wikipedia.org/wiki/メガビット "wikilink")  | 128 KB                                                           | 20000                                                     | 1FFFF                                                        |
| 27C020         | 2 Mbit                                                    | 256 KB                                                           | 40000                                                     | 3FFFF                                                        |
| 27C040, 27C400 | 4 Mbit                                                    | 512 KB                                                           | 80000                                                     | 7FFFF                                                        |
| 27C080         | 8 Mbit                                                    | 1 [MB](https://ja.wikipedia.org/wiki/メガバイト "wikilink")           | 100000                                                    | FFFFF                                                        |
| 27C160         | 16 Mbit                                                   | 2 MB                                                             | 200000                                                    | 1FFFFF                                                       |
| 27C320         | 32 Mbit                                                   | 4 MB                                                             | 400000                                                    | 3FFFFF                                                       |

\[9\]

## ギャラリー

ファイル:EPROMdie.jpg|EPROMのダイのクローズアップ image:ST Microelectronics M27C256B (2006).jpg|32KB (256Kbit) EPROM image:Eprom60x.jpg|60倍にクローズアップしたEPROM image:NEC D8749HD.png|[8749](https://ja.wikipedia.org/wiki/Intel_8048 "wikilink") [マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")。内蔵EPROMにプログラムを格納する。

## EEPROM

フローティングゲートからドレインに[トンネル効果](https://ja.wikipedia.org/wiki/トンネル効果 "wikilink")を利用して電子を引き抜くことにより、電気的な操作のみで消去を行うようにしたもの。EEPROMは回路基板に実装したままで書込み・消去ができる[不揮発性メモリ](https://ja.wikipedia.org/wiki/不揮発性メモリ "wikilink")なので、利用時に書き換えが必要な用途、例えば機器の動作設定データや、利用者固有の情報を保存するのに適する。初期には容量が小さく、デバイスも高価であり、また書込み・消去の所要時間が[RAMに比べて長かったが](../Page/Random_Access_Memory.md "wikilink")、[フラッシュメモリ](https://ja.wikipedia.org/wiki/フラッシュメモリ "wikilink")の登場により改良され、広く普及した。

## 脚注・出典

## 関連項目

  - [ROMプログラマ](https://ja.wikipedia.org/wiki/ROMプログラマ "wikilink")（ROMライタ）
  - [マスクROM](https://ja.wikipedia.org/wiki/マスクROM "wikilink")
  - [PROM](../Page/PROM.md "wikilink")
  - [EEPROM](https://ja.wikipedia.org/wiki/EEPROM "wikilink")
  - [フラッシュメモリ](https://ja.wikipedia.org/wiki/フラッシュメモリ "wikilink")

## 外部リンク

  - [Detailed information about EPROMs types and EPROM programming](http://www.progshop.com/shop/electronic/eprom-programming.html)

[Category:半導体メモリ](https://ja.wikipedia.org/wiki/Category:半導体メモリ "wikilink") [Category:不揮発性メモリ](https://ja.wikipedia.org/wiki/Category:不揮発性メモリ "wikilink") [Category:集積回路](https://ja.wikipedia.org/wiki/Category:集積回路 "wikilink")

1.  Chih-Tang Sah ,'' Fundamentals of solid-state electronics '' World Scientific, 1991 ISBN 9810206372, page 639
2.  Vojin G. Oklobdzija, *Digital Design and Fabrication*, CRC Press, 2008 ISBN 0849386020, page 5-14 through 5-17
3.  John E. Ayers ,*Digital integrated circuits: analysis and design*, CRC Press, 2004 , ISBN 084931951X, page 591
4.  [Paul Horowitz](https://ja.wikipedia.org/wiki/:en:Paul_Horowitz "wikilink") and Winfield Hill, ''The Art of Electronics 2nd Ed. '' Cambridge University Press, Cambridge, 1989 ISBN 0521370957 page 817
5.  May 10, 1971 issue of [Electronics Magazine](https://ja.wikipedia.org/wiki/:en:Electronics_\(magazine\) "wikilink") in an article written by Dov Frohman
6.   090508 jmargolin.com
7.  Sah 1991 page 640
8.   The details of SEEQ's Silicon Signature method of a device programmer reading an EPROM's ID.
9.  注: 1702 EPROM は[PMOS](https://ja.wikipedia.org/wiki/:en:PMOS_logic "wikilink")、27xシリーズのEPROMで名称に "C" とあるものは[CMOS](https://ja.wikipedia.org/wiki/CMOS "wikilink")ベースで、"C"がないものは[NMOSである](https://ja.wikipedia.org/wiki/:en:NMOS_logic "wikilink")。