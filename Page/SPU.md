> この記事は[SPU](https://ja.wikipedia.org/wiki/SPU)から翻訳されています。


**SPU** (Sound Processing Unit)は、[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")によって設計・製造され、同社ゲーム機に搭載された[PCM](https://ja.wikipedia.org/wiki/PCM "wikilink")音源につけられた名称である。[プレイステーションに搭載されたSPU](../Page/PlayStation_\(ゲーム機\).md "wikilink")、[プレイステーション2に搭載されたSPU](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")2がある。[スーパーファミコン](../Page/スーパーファミコン.md "wikilink")の音源に使用されたSPC700に由来している。

## SPC700

[thumb](https://ja.wikipedia.org/wiki/ファイル:S-DSP_A_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:S-SMP_01.jpg "wikilink") 任天堂のスーパーファミコンに搭載された音源は、[DSPと](../Page/デジタルシグナルプロセッサ.md "wikilink")、制御用チップS-SMP（SPC700コア）から構成される。SPC700は[6502](https://ja.wikipedia.org/wiki/6502 "wikilink")を拡張した命令セットを持ち（オブジェクトの互換性はない）、本体のCPUとは別に動作する。

当時[ソニー](../Page/ソニー.md "wikilink")のハードウェアエンジニアであった[久夛良木健](../Page/久夛良木健.md "wikilink")が設計を手がけた。当初スーパーファミコンでは別の音源が採用される予定であったが、任天堂の担当者の前で久夛良木がSPC700のデモンストレーションを行いその性能をアピールし、その能力が認められたため、スーパーファミコンに採用されることとなった。\[1\]

スーパーファミコンの音源の性能は以下の通り。

  - スペック

<!-- end list -->

  - SRAM: 64KB
  - サンプリング周波数: 32kHz
  - 同時発音数: 8チャンネル
  - 16bit PCM ステレオ（[ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink")）
  - SPC700クロック周波数: 2.048MHz
  - DSP（エフェクター）の機能:
      - [BRR圧縮された波形データの復元](https://ja.wikipedia.org/wiki/Bit_Rate_Reduction "wikilink")
      - [ADSR](../Page/ADSR.md "wikilink")
      - [ガウス分布](https://ja.wikipedia.org/wiki/ガウス分布 "wikilink")[補間](../Page/内挿.md "wikilink")
      - [エコー](../Page/エコー_\(音響機器\).md "wikilink")
      - [ディレイ](../Page/ディレイ_\(音響機器\).md "wikilink")（最大240ms）
      - [リバーブ](https://ja.wikipedia.org/wiki/リバーブ_\(音響機器\) "wikilink")（次数8の[FIRフィルタ付](https://ja.wikipedia.org/wiki/有限インパルス応答 "wikilink")）
      - [ピッチモジュレーション](https://ja.wikipedia.org/wiki/ピッチモジュレーション "wikilink")（1チャンネルのみ不可）
      - [ノイズ](../Page/ノイズ.md "wikilink")（発生周波数: 0～32kHz）
      - [ピッチベンド](../Page/ピッチベンド.md "wikilink")

スーパーファミコンの仕様が正式発表された1988年当時のスペックとしては非常に高性能なものであった。1990年にスーパーファミコン発売後には、SPC700の性能を生かして、スーパーファミコンでは数々の良質なゲーム音楽が誕生することとなった。

しかしながら、メモリの容量や同時発音数、データサイズの制限、初期のライブラリの音源ドライバー（かんきちくん）の使い辛さや、スーパーファミコンの標準の開発機材だったソニーの[NEWSの](https://ja.wikipedia.org/wiki/NEWS_\(ソニー\) "wikilink")[UNIX](../Page/UNIX.md "wikilink")環境に製作側が慣れていないなど、初期は製作ノウハウ面で敷居が高かったこともあり、SPC700の能力を発揮するためには、ドライバの自作や改造ができる高度な技術を持ったプログラマーや、それに対応できるサウンドコンポーザーの腕が必要であった。そのためスーパーファミコンのゲームのサウンドは製作側の能力いかんによって大きく音質が異なる。

SPC700の性能を生かした究極の作品に[サテラビュー](../Page/サテラビュー.md "wikilink")のゲーム「Rの書斎」がある。これはサテラビューから受信したデータをメモリーパックへ一時蓄積しつつSPC700によって再生するという手法を用い、CD-ROM機以外では不可能と思われていた音声の分岐を実現したものである。

後売のプレイステーションシリーズのSPU、SPU2はこのSPC700を発展・改良させたものである。

## SPU

[thumb](https://ja.wikipedia.org/wiki/ファイル:CXD2938Q_02.JPG "wikilink") SPUは[プレイステーションに搭載されたPCM音源である](../Page/PlayStation_\(ゲーム機\).md "wikilink")。性能は以下の通り。

  - スペック

<!-- end list -->

  - メモリ：512KB
  - サンプリング周波数：44.1kHz(CD-DAと同じ)
  - 同時発音数：ステレオ、24チャンネル

SPC700に比べ、性能が大幅に強化されている。また、メディアにCD-ROMが用いられるためファイルサイズの制限がSPC700よりも緩くなったことから、様々な音色を用いるゲーム音楽が誕生した。

## SPU2

SPU2は[プレイステーション2に搭載されたPCM音源である](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")。性能は以下の通り。

  - スペック

<!-- end list -->

  - メモリ：2MB
  - サンプリング周波数：48kHz(DVD-Videoと同じ)または44.1kHz
  - 同時発音数：ステレオ、48チャンネル

## 脚注

<references/>

[Category:ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/Category:ソニー・コンピュータエンタテインメント "wikilink") [Category:通信工学](https://ja.wikipedia.org/wiki/Category:通信工学 "wikilink") [Category:音声処理](https://ja.wikipedia.org/wiki/Category:音声処理 "wikilink") [Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink") [Category:任天堂の半導体チップ](https://ja.wikipedia.org/wiki/Category:任天堂の半導体チップ "wikilink")

1.