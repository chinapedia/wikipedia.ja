> この記事は[Programmable Sound Generator](https://ja.wikipedia.org/wiki/Programmable_Sound_Generator)から翻訳されています。


**Programmable Sound Generator**（プログラマブル・サウンド・ジェネレーター、PSG）は、音を作り出す[電子回路](../Page/電子回路.md "wikilink")の一種。狭義には、[ゼネラル・インスツルメンツ](https://ja.wikipedia.org/wiki/ゼネラル・インスツルメンツ "wikilink")（GI）のAY-3-8910および相当品。広義には、それらと基本原理が同じ回路の総称。単一の[音源](../Page/音源.md "wikilink")[チップないし](../Page/集積回路.md "wikilink")、より多機能なチップの機能の一つとして供給される。

複数の基本[波形](../Page/波形.md "wikilink")（AY-3-8910では[矩形波](../Page/矩形波.md "wikilink")×3+[ホワイトノイズ](../Page/ホワイトノイズ.md "wikilink")）を合成してさまざまな音色を出し、エンベロープ・ジェネレーターで[ADSR](../Page/ADSR.md "wikilink")（立ち上がりや余韻などのパターン）を変化させる。

[1980年代](../Page/1980年代.md "wikilink")の[アーケードゲーム](../Page/アーケードゲーム.md "wikilink")や[パソコン](../Page/パーソナルコンピュータ.md "wikilink")、携帯用[ゲーム機](../Page/ゲーム機.md "wikilink")に採用された。

[thumb](https://ja.wikipedia.org/wiki/ファイル:AY-3-8910_01.png "wikilink") [AY-3-8910.jpg](https://ja.wikipedia.org/wiki/File:AY-3-8910.jpg "fig:AY-3-8910.jpg")

## 概要

本来のPSGは、GI社（現在は[モトローラ](../Page/モトローラ.md "wikilink")が吸収合併）およびGIからスピンオフした[マイクロチップ・テクノロジー](https://ja.wikipedia.org/wiki/マイクロチップ・テクノロジー "wikilink")のAY-3-8910、およびその後継製品のAY-3-8912 / AY-3-8913相当品を指す。

[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")（TI）の**SN76489**も同様に扱われることが多い。しかし仕様は全く異なっており、本来は区別される。SN76489は厳密にはPSGではなくDigital Complex Sound Generator（DCSG）である 。

[thumb](https://ja.wikipedia.org/wiki/ファイル:YM2149_01.jpg "wikilink") [ヤマハ](../Page/ヤマハ.md "wikilink")は、同社のMSXマシンに使用する目的でAY-3-8910の互換チップとしてYM2149を開発し、後に他社にも販売している。また、同等の機能を同社の一部の[FM音源](../Page/FM音源.md "wikilink")チップ（[YM2203](../Page/YM2203.md "wikilink")/[YM2608](../Page/YM2608.md "wikilink")など）、MSXシステムチップセット（[MSX-SYSTEM](../Page/MSX-SYSTEM.md "wikilink")/[MSX-SYSTEMII](../Page/MSX-SYSTEMII.md "wikilink")など）にも内蔵している。 YM2149はAY-3-8910相当機能に加え、AY-3-8910のTEST2端子（26番ピン）をSEL\#（\#はローアクティブを示す）に変更し、この端子をLowレベルにすることによって、発音基準周波数を外部入力周波数の2分周に設定できるように変更したものである。さらに内部的な音量が32段階（AY-3-8910は16段階）になっており、ハードウェアエンベロープが滑らかになっている。 後継・派生製品として、YM3439（CMOS版）、YMZ284（小パッケージ版）、YMZ294（小パッケージ/クロック分周比可変）などがある。

この、FM音源によるPSG互換機能をSSG（Software-controlled Sound Generator）音源、単純にSSGとも呼ぶ。 広義では、矩形波の出る安価なチップ音源をまとめて「PSG」と呼ぶことがある。

## AY-3-8910の仕様

[AY-8912_Chip.jpg](https://ja.wikipedia.org/wiki/File:AY-8912_Chip.jpg "fig:AY-8912_Chip.jpg") [AY-3-8910A_Sound_Chip.png](https://ja.wikipedia.org/wiki/File:AY-3-8910A_Sound_Chip.png "fig:AY-3-8910A_Sound_Chip.png") [AY-3-8912A.jpg](https://ja.wikipedia.org/wiki/File:AY-3-8912A.jpg "fig:AY-3-8912A.jpg") [AY-3-8910_pinout.JPG](https://ja.wikipedia.org/wiki/File:AY-3-8910_pinout.JPG "fig:AY-3-8910_pinout.JPG") AY-3-8910は3つのパッケージで販売されていた。

代表的なPSGチップであるAY-3-8910は次のような仕様である。

  - [矩形波](../Page/矩形波.md "wikilink")発生装置 3系統（音量16段階、周波数4095段階8オクターブ、[デューティ比](https://ja.wikipedia.org/wiki/デューティ比 "wikilink")1:1固定）
  - ノイズ発生装置 1系統（[擬似乱数](../Page/擬似乱数.md "wikilink")雑音 = [ホワイトノイズ](../Page/ホワイトノイズ.md "wikilink")、乱数発生周期31段階）
  - [エンベロープ](https://ja.wikipedia.org/wiki/エンベロープ "wikilink")発生装置 1系統（パターン8種類、周波数65535段階）
  - ミキサー
  - 8bit汎用入出力ポート×2（[ジョイスティック](../Page/ジョイスティック.md "wikilink")、[タッチパネル](../Page/タッチパネル.md "wikilink")など）
      - [ATARI仕様の台形](https://ja.wikipedia.org/wiki/Atari_2600#コントローラ "wikilink")9ピン(D-Sub)インターフェース実装に用いられることが多かった。
      - AY-3-8913では、この入出力ポートが省略されている。
  - 備考
      - チャンネルごとに、出力のモードを「ミュート」「矩形波を出力」「ノイズを出力」「矩形波とノイズをmix出力」から選べる。
          - 出力系統は3系統しかないため、mix出力モードでは矩形波とノイズの音量は独立制御することはできず、同じ値がセットされる。
          - また、MIXモードは合成されて出力されているわけではなく、内部的には高速にトーンとノイズが切り替わっているため、双方の出力音は濁ってしまう。
          - 多くの実装では全チャンネルをミキシングして使われることが多かったものの、チップからの出力はチャンネルごとに独立しており、定位する位置を変えることでステレオ出力としている実装\[1\]もある。

### AY-3-8910相当品を搭載した主な[コンピューター](https://ja.wikipedia.org/wiki/パソコン "wikilink")

  - [PC-6001・PC-6001mkII](../Page/PC-6000シリーズ.md "wikilink")
  - [PC-6601](../Page/PC-6600シリーズ.md "wikilink")
  - [X1シリーズ](../Page/X1_\(コンピュータ\).md "wikilink")（X1F以降のモデルからYM2149）
  - [FM-7](../Page/FM-7.md "wikilink")（一部ロットはAY-3-8913（8bit汎用入出力ポートなし））
  - [FM-77](https://ja.wikipedia.org/wiki/FM-77 "wikilink")（FM-77L2には[FM音源](../Page/FM音源.md "wikilink")：[YM2203](../Page/YM2203.md "wikilink")（[OPN](https://ja.wikipedia.org/wiki/OPN "wikilink")）も搭載）
  - [MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")
  - [MZ-5500](../Page/MZ_\(コンピュータ\).md "wikilink")
  - 1980年代前半～中盤のアーケードゲーム

### SSGを搭載した主な[コンピューター](https://ja.wikipedia.org/wiki/パソコン "wikilink")

[FM音源](../Page/FM音源.md "wikilink"):[YM2203](../Page/YM2203.md "wikilink")（OPN）/[YM2608](../Page/YM2608.md "wikilink")（OPNA）を搭載

  - [PC-6001mkIISR](../Page/PC-6000シリーズ.md "wikilink")
  - [PC-6601SR](../Page/PC-6600シリーズ.md "wikilink")
  - [PC-8001mkIISR](../Page/PC-8000シリーズ.md "wikilink")
  - PC-8801mkIISR以降の[PC-8800シリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")
  - [PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")（オプション: PC-9801-14(PSG: TMS3631)、PC-9801-26K(OPN)、PC-9801-73・PC-9801-86(OPNA)）
  - [MZ-2500](https://ja.wikipedia.org/wiki/MZ-2500 "wikilink")
  - [MZ-2861](../Page/MZ-2861.md "wikilink")
  - [FM-77L2](https://ja.wikipedia.org/wiki/FM-7#FM-77 "wikilink")
  - [FM77AVシリーズ](https://ja.wikipedia.org/wiki/FM-7#FM77AV "wikilink")
  - [MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")
  - [Atari Falcon](https://ja.wikipedia.org/wiki/Atari_Falcon "wikilink") CMOS版のYM3439Cが搭載された。

### AY-3-8910の互換チップ

  - [KC89C72](https://ja.wikipedia.org/wiki/KC89C72 "wikilink")\[2\]\[3\] 台湾FILE社製で、中東向けMSX等に使用例が見られる。
  - [AY8930](https://ja.wikipedia.org/wiki/AY8930 "wikilink")(APSG) AY-3-8910の[セカンドソース](../Page/セカンドソース.md "wikilink")を製造していた[マイクロチップ社が独自に機能を拡張した上位互換チップ](https://ja.wikipedia.org/wiki/マイクロチップ・テクノロジー "wikilink")。ハードウェアエンベロープが各チャンネルごとに設定できる、出力波形のデューティ比を選択できるなどの機能拡張がされている。
  - [YMZ705](https://ja.wikipedia.org/wiki/YMZ705 "wikilink")(SSGS) SSGを2つとADPCMを集積したヤマハ製上位互換チップ。各チャンネルに対し16段階のパンポットを設定できる。
  - 東芝はSSG互換品をPSC（Programmable Sound Controller）という名称で設計し、ゲートアレイなどの特定用途向けLSIに使用した。[MSX-ENGINE](../Page/MSX-ENGINE.md "wikilink")、MSX-ENGINE2などがこれにあたり、ハードマクロセル名はSM7766A\[4\]である。ハードウェアエンベロープの周期などがAY-3-8910とは異なる。

## SN76489の仕様

[SN76489_01.jpg](https://ja.wikipedia.org/wiki/File:SN76489_01.jpg "fig:SN76489_01.jpg") SN76489（DCSGとも呼ばれる）のPSGとの大きな違いは、矩形波チャンネル3つ+ノイズ発生チャンネル1の合計4チャンネルで構成されているところである。PSG（SSG）はその構造上ノイズの音量制御が3つのチャンネルのどれかに依存してしまうが、SN76489（やpAPU)にはこの制限はなく、独立したノイズチャンネル単体で自由に音量制御できる。また、ハードウェアエンベロープも持たない。

通常音色はデューティ比50/50のみであるが、3チャンネル目を同期ノイズ出力にすることでデューティ比6.25/93.75の音となる。トーン周波数に対し音程は半音ずれるが、ギターに似た音色となるため、若干弱い低音部をカバーする事が出来た。

### SN76489を搭載した主な[コンピューター](https://ja.wikipedia.org/wiki/パソコン "wikilink")

  - [MZ-1500](../Page/MZ-1500.md "wikilink")（同時6音）：SN76489×2
      - 2つのチップは別々に出力され、左右の出力とすることでステレオと称していた。
  - [MZ-800](https://ja.wikipedia.org/wiki/MZ-800 "wikilink")：SN76489AN
  - [セガ（初代～マスターシステム、メガドライブ、ゲームギア）](https://ja.wikipedia.org/wiki/セガゲームス "wikilink")：SN76489
  - [M5](../Page/M5_\(コンピュータ\).md "wikilink")（ゲームパソコンM5）：SN76489A
  - [パソピア](../Page/パソピア.md "wikilink")7（同時6音）：SN76489A×2
  - [SMC-777](../Page/SMC-777.md "wikilink")：SN76489
  - 1980年代前半～中盤のアーケードゲーム
      - セガ [System 1](https://ja.wikipedia.org/wiki/:en:List_of_Sega_arcade_system_boards#Sega_System_1 "wikilink")(アーケード基板)

## SAA1099の仕様

6チャンネルステレオ出力を持ち、エンベロープジェネレータとノイズジェネレータを2セット内蔵するなど、ほぼPSGの2倍のキャパシティを持つ。 ハードウェアエンベロープの出力波形を楽音波形とすることで矩形波以外に三角波・鋸歯状波での出力が可能。(後述のようにAYでも可能であるが、ハードウェアエンベロープの周波数精度が低いため、メロディを演奏するにはかなり音域に制限が生じた。SAAでは楽音周波数と同じ精度であるので、通常の演奏と同等となる。)

### SAA1099を搭載した主な[コンピューター](https://ja.wikipedia.org/wiki/パソコン "wikilink")

  - [Sam Coupe](https://ja.wikipedia.org/wiki/Sam_Coupe "wikilink") [ZX Spectrumのクローン](../Page/ZX_Spectrum.md "wikilink")。本家ZX Spectrumにも同等の機能を追加するオプションハードウェアが作られた。
  - [Game Blaster](https://ja.wikipedia.org/wiki/Game_Blaster "wikilink") [Sound Blasterの前にクリエイティブ社が発売したIBM](../Page/Sound_Blaster.md "wikilink") [PC/XT](https://ja.wikipedia.org/wiki/PC/XT "wikilink")用サウンドカード。SAA1099を2つ搭載していた。

## ファミコン音源（pAPU）の仕様

[thumb](https://ja.wikipedia.org/wiki/ファイル:RP2A03E.jpg "wikilink") [ファミリーコンピュータ](https://ja.wikipedia.org/wiki/ファミリーコンピュータ "wikilink")に搭載されている音源は次のような仕様である。

  - [パルス波](https://ja.wikipedia.org/wiki/パルス波 "wikilink")（矩形波）発生装置 2系統（[デューティ比](https://ja.wikipedia.org/wiki/デューティ比 "wikilink")3:1、1:1、1:3、1:7切り替え）
  - [三角波発生装置](https://ja.wikipedia.org/wiki/三角波_\(波形\) "wikilink") 1系統（4bit波形、音量は仕様上固定だが、DPCMと絡んだ[バグ](../Page/バグ.md "wikilink")に近い挙動が存在し、これを利用するといじることが出来る）
  - ノイズ発生装置 1系統（擬似乱数雑音・短周期ノイズ切り替え、周波数変更が可能。ただし、最初期型（コントローラのボタンが四角いゴム）のファミコンでは短周期ノイズは出せない）
  - DPCM 1系統
  - ミキサー

この音源はファミコンのCPU [RP2A03](https://ja.wikipedia.org/wiki/Ricoh_2A03 "wikilink")（[6502](https://ja.wikipedia.org/wiki/6502 "wikilink")カスタム）に組み込まれた機能の一つであり、[pAPU](https://ja.wikipedia.org/wiki/pAPU "wikilink")（pseudo Audio Processing Unit）と呼ばれている。 pAPUのパルス波発生装置は[ゲームボーイ](../Page/ゲームボーイ.md "wikilink")、[ゲームボーイアドバンス](../Page/ゲームボーイアドバンス.md "wikilink")にも搭載され、矩形波だけでなく[デューティ比](https://ja.wikipedia.org/wiki/デューティ比 "wikilink")1:7[パルス波](https://ja.wikipedia.org/wiki/パルス波 "wikilink")などの独特な音色も出せる表情の豊かさがPSGの矩形波との大きな違いである。

## PSGと誤解されやすいその他の音源

[日本電気ホームエレクトロニクス](../Page/日本電気ホームエレクトロニクス.md "wikilink")から発売された[家庭用ゲーム機](https://ja.wikipedia.org/wiki/家庭用ゲーム機 "wikilink")[PCエンジン](../Page/PCエンジン.md "wikilink")ではスペック表にPSGとの記載されることがあるが、実際に使われているのは[波形メモリ音源](../Page/波形メモリ音源.md "wikilink")（変調機能つき）であり、一般的に言われる本項で説明のPSGとは異なるものである。また、1980年代の[ナムコ](https://ja.wikipedia.org/wiki/ナムコ "wikilink")の多くのアーケードタイトルで使われていた音源も波形メモリ音源である。

ただ、当時のマニア間では「ナムコPSG」という俗称が広まっていたり、メーカーの開発側でも他の音源と分類する際に、便宜上PSGと区分していた場合もあった。ナムコのアーケード基板『[SYSTEM I](../Page/SYSTEM_I.md "wikilink")』のサウンドテストモードでは、波形メモリ音源のパートはPSGと表記されている。

## PSGによるPCM再生

PSGによって[PCM](https://ja.wikipedia.org/wiki/PCM "wikilink")を再生する技法が存在し、**PSGPCM**や**SSGPCM**等と呼ぶ。[DACを持たないパソコン向けのソフトウェアで使われることがあった](../Page/デジタル-アナログ変換回路.md "wikilink")。

ただし、ボリューム調節機能を使っているため、DACとしては指数関数的な非線形量子化となることから、再生音声の品質は悪く、「無線による交信を演出する」といった演出など、用途は限定されていた。

1Chのみを用いた出力は解像度の低いものであったが、実際の出力を計測し、そのテーブルとPSG 3Ch各々のアッテネータを組み合わせて利用することで、音質の改善を試みる手法が生み出された。ソフトウェアメーカーによる実装もいくつか見られたが、個人が作成した同様のプログラムでは、[Oh\!FM](../Page/Oh!FM.md "wikilink") 1990年4月号に掲載された戸田浩による「しゃべるんどすえ」のドキュメントと音量テーブルは、その後、同様のプログラムの作成の参考にされた。\[5\]

現在では、上記の方法に加え、出力特性に合わせて再生するデータを変換することで、よりよい出力にする技法も開発され、S/N比が比較的高い再生を可能にしているソフトウェアも存在している。指数性のために音量域によって解像度にばらつきが出るが、平均すると、9bit程度の解像度を持つ出力を行うことが可能である。

### PSGPCMの原理

PSGで発声されるのは矩形波である。これはロー（=0）とハイ（=1）の2値しかとらない。これに音量レジスタ（4bit）の値を掛けたものが1チャンネル分の出力である。

AY-3-8910相当品では、あるチャンネルの発声を停止すると矩形波出力はハイ（=1）で固定される。従って、そのチャンネルの出力は、音量レジスタそのものとなる（1×音量レジスタ=音量レジスタ）。

この仕様を利用し、発声を停止した状態でそのチャンネルの音量を操作することで、PSGをDACとして利用するというのが大まかな原理である。

## エンベロープ

一般的なPSGチップではエンベロープ機能により、時間的な音量変化をハードウェアレベルで自動的に行える。エンベロープパターンには一般的な[減衰波](https://ja.wikipedia.org/wiki/減衰波 "wikilink")や、周期的な[鋸波](https://ja.wikipedia.org/wiki/鋸波 "wikilink")、[三角波など](https://ja.wikipedia.org/wiki/三角波_\(波形\) "wikilink")、8種類が用意されており、周期も自由に設定できる。しかし、エンベロープジェネレータは1系統しか用意されていないため、3チャンネルで楽曲を演奏しようものなら、エンベロープが同期してしまい、まったく聞くに堪えない物になってしまう上、音量の調節も不可能である。そのため、ソフトウェアの側でこまめにPSGの各チャンネルの音量レジスタを変更して、ソフトウェアレベルでエンベロープを再現する技術があった。この手法は「ソフトウェアエンベロープ」と呼ばれることがある。

ハードウェアエンベロープ機能の応用として、周期的なタイプのエンベロープパターンを「音量変化としてではなく楽音の波形として」選択し、エンベロープ速度（周期）をその楽音の音程とみなして設定することで、PSGの通常の発音方法では出せない鋸波や三角波を出すことができる。ただしエンベロープ周期を設定するレジスタ幅は狭く、楽音の音程を表現するには精度が低いため「音痴」になりやすい。また原理上、こうして発音した音の音量制御はできない。この手法はYM2203やYM2608のSSG音源部でも使用が可能である。

## 脚注

<references />

## 関連項目

  - [:en:Sound chip](https://ja.wikipedia.org/wiki/:en:Sound_chip "wikilink")（PSG/[FM音源](../Page/FM音源.md "wikilink")）
      - [:en:Texas Instruments SN76477](https://ja.wikipedia.org/wiki/:en:Texas_Instruments_SN76477 "wikilink")
  - [シンセサイザー](../Page/シンセサイザー.md "wikilink")
  - [内蔵音源](../Page/内蔵音源.md "wikilink")
  - [波形メモリ音源](../Page/波形メモリ音源.md "wikilink")
  - [PCM音源](../Page/PCM音源.md "wikilink")
  - [SID音源](https://ja.wikipedia.org/wiki/SID音源 "wikilink")
  - [沖電気](https://ja.wikipedia.org/wiki/沖電気 "wikilink")[MSM5232](https://ja.wikipedia.org/wiki/MSM5232 "wikilink")
  - [チップチューン](../Page/チップチューン.md "wikilink")

[Category:電子音源の合成方式](https://ja.wikipedia.org/wiki/Category:電子音源の合成方式 "wikilink") [Category:音源チップ](https://ja.wikipedia.org/wiki/Category:音源チップ "wikilink") [Category:MSX](https://ja.wikipedia.org/wiki/Category:MSX "wikilink")

1.  東芝製のパソピアIQシリーズなど。
2.  [1](https://garoa.net.br/wiki/Placa_KC89C72)
3.  [:en:General Instrument AY-3-8910](https://ja.wikipedia.org/wiki/:en:General_Instrument_AY-3-8910 "wikilink")
4.  東芝データブック「スーパーインテグレーション（S.I.）スーパーマクロセルライブラリ1992（非売品）462D1AA」より
5.  Oh\!X 1995年12月号 BREEZEには参考文献として明示されている。