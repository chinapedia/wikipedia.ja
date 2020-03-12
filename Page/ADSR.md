> この記事は[ADSR](https://ja.wikipedia.org/wiki/ADSR)から翻訳されています。


**ADSR** は、[シンセサイザー](../Page/シンセサイザー.md "wikilink")等、電子楽器の制御信号を設定する機能のひとつ。**エンベロープ・ジェネレーター** (Envelope Generator) によってコントロールされるパラメータで、**Attack**、**Decay**、**Sustain**、**Release**の頭文字である。

## 概要

シンセサイザー（[アナログシンセサイザー](../Page/アナログシンセサイザー.md "wikilink")の場合）の3つの音声信号の機能 ([VCO](https://ja.wikipedia.org/wiki/VCO "wikilink")/[VCF](../Page/VCF.md "wikilink")/[VCA](https://ja.wikipedia.org/wiki/VCA "wikilink")) は、任意の電圧で制御する事により作動する。また、ノートオン・ノートオフ（鍵盤楽器にたとえると、鍵盤の鍵を押す／離す事に相当する）に応じて、楽器音的な時間的変化をする制御信号を作り出し、それを音声信号の機能に送るのがエンベロープ・ジェネレーターの役目になっている。

## 機能

シンセイザーは、発振機(オシレーター)の生成した波形に対して、別入力チャンネルによる制御機構をもつ。一般的に「ADSR」として体系を為す4つの要素は、多くのシンセイザーのインターフェースによって、備わっており、しばし視覚的に説明される。例えば、波形の山と山の頂点をつないだ「[包絡線](../Page/包絡線.md "wikilink")」やその形状のことを時間軸の変化の中でこれを指示する。

楽器としてのシンセサイザの場合、次のような、[アコースティック楽器](https://ja.wikipedia.org/wiki/アコースティック楽器 "wikilink")の音に見られる特徴的な形状をモデル化・パラメータ化し制御するものが多く、これらを含めてまとめて「ADSR」と呼ばれて定着している。 [thumb](https://ja.wikipedia.org/wiki/ファイル:Adsr3.png "wikilink")

  - Attack（立ち上がり）
    演奏開始からその音声の最大音量に到達するまでの時間を設定するパラメータ。0秒に設定すればいきなり最大音量になり、ピアノやギター、或いは打楽器の音声と同じになる。
  - Decay（減衰）
    Attackで到達した最大音量から、Sustainレベルに移行するまでの時間を設定するパラメータ。
  - Sustain（減衰後の保持）
    Decayの後、演奏が続いている限り出る音量を設定するパラメータ（これだけは時間的変化ではなく量の設定パラメータとなっている）。
  - Release（余韻）
    演奏を終了した（鍵盤の鍵を離した）時点から、音が鳴り終わるまでの時間を設定するパラメータ。[ピアノ](../Page/ピアノ.md "wikilink")などの生楽器でのSustainに相当する。

## ADSR以外のパターン

パラメーターの数はA、D、S、Rの4つという場合が多いが、[コルグ](https://ja.wikipedia.org/wiki/コルグ "wikilink")の一部の機種のように5つのものや、[オーバーハイム](../Page/オーバーハイム.md "wikilink")の初期の機種では3つというものもあり、必ずしも4つではない。

[Category:シンセサイザー](https://ja.wikipedia.org/wiki/Category:シンセサイザー "wikilink") [Category:電子音源の合成方式](https://ja.wikipedia.org/wiki/Category:電子音源の合成方式 "wikilink")