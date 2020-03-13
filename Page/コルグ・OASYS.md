> この記事は[OASYS](https://ja.wikipedia.org/wiki/OASYS)から翻訳されています。


**OASYS**（オアシス）とは[2005年](../Page/2005年.md "wikilink")[5月28日](../Page/5月28日.md "wikilink")発売の[コルグ](https://ja.wikipedia.org/wiki/コルグ "wikilink")の[シンセサイザー](../Page/シンセサイザー.md "wikilink")。 [thumb](https://ja.wikipedia.org/wiki/ファイル:KORG_OASYS.jpg "wikilink") [ミュージックワークステーション](../Page/ミュージックワークステーション.md "wikilink")と呼ばれる、シンセサイザー1台だけで音楽制作のほとんどの作業を行える多機能型シンセサイザーで、演奏の他に[MIDI](../Page/MIDI.md "wikilink")データの作成、生音の録音、CDの書き込みまで行える。外部から音を取り込むサンプリング、[アナログシンセサイザー](../Page/アナログシンセサイザー.md "wikilink")、[オルガン](../Page/オルガン.md "wikilink")のモデリング機能を持ち、音色合成可能である。最大同時発音数は172音。88鍵タイプが定価882,000円、76鍵タイプが定価840,000円のプロユース用のシンセサイザーである。現在は生産完了しているが、この機種の流れを組む[KRONOS(クロノス)が](https://ja.wikipedia.org/wiki/コルグ・KRONOS "wikilink")[2011年](../Page/2011年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")に発売されている。 {{-}}

## 主な特徴

これまで発売されてきたデジタル・シンセサイザーは処理演算のために専用の[DSPを用いていた](../Page/デジタルシグナルプロセッサ.md "wikilink")。そのため、新機能の追加が難しく、次の製品にアップデートが反映されるという形をとってきたが、OASYSでは[Pentium 4と独自にカスタマイズされた](../Page/Pentium_4.md "wikilink")[Linux](../Page/Linux.md "wikilink")やその上で動く専用ソフトウェアを用いて処理演算を行う、Open Architecture Synthesis Studioと呼ばれるシステムを採用した。これによりソフトウェアの拡張やバグフィックスなどが容易に出来、発音数やエフェクト数も向上している。コルグの技術の集大成とも言える内容であり、[コルグ・WAVESTATIONシリーズ](../Page/コルグ・WAVESTATIONシリーズ.md "wikilink")のウェーブ・シーケンスやKARMAのKARMA機能を2.0にバージョンアップして搭載するなどしている。なお、76鍵盤タイプは[ヤマハ](../Page/ヤマハ.md "wikilink")から[OEM](../Page/OEM.md "wikilink")供給されたFS鍵盤を使用した最後のシンセサイザーであり、[M3以降は自社製のセミウェイテッド鍵盤に切り替えている](../Page/コルグ・Mシリーズ.md "wikilink")。

## OASYSの歴史

本ページで紹介されているコルグOASYSは、実はOASYSとしては3世代目である。

初代は1994年、プロトタイプとして制作された。NAMMショーに出品されたのみで発売されなかったが、タッチビューや複数の音源方式、リボンコントローラーやシルバーの筐体など、翌年発売の[コルグ・TRINITYシリーズ](../Page/コルグ・TRINITYシリーズ.md "wikilink")や[コルグ・Prophecy](../Page/コルグ・Prophecy.md "wikilink")に生かされた。そして、それ以降に発売されるコルグシンセの基準となるものである。

2世代目は2000年に「OASYS PCI」という名前でNAMMショーに出品され、海外のみで発売された。DSP付きのPCIオーディオインターフェイスとソフトウェアで構成され、音源方式やフィルター、その他のあらゆるモディファイアーを言語レベルから組み上げる事ができると言う、[MAX/MSP](https://ja.wikipedia.org/wiki/MAX/MSP "wikilink")と同じような概念のモデルであった(ちなみにこの時期、日本ではオーディオインターフェイス機能のみを搭載したPCIボード「1212I/O」が発売された)。

## 音源の構成

  - HD-1 High Definition Synthesizer
    OASYSに標準搭載されている[PCM音源](../Page/PCM音源.md "wikilink")。従来機の[コルグ・TRITONシリーズ](../Page/コルグ・TRITONシリーズ.md "wikilink")では最大で2段階までしかベロシティ・スイッチを組めなかったが、4段階まで組むことが出来るようになり、TRITONと同様1音色につき2つオシレータを持つことが出来る。工場出荷時の状態では、拡張PCMライブラリーが2つ付属し、Ver.1.0xのときは、どちらか一つの排他使用しか出来なかったが、Ver 1.1より、メモリの拡張が出来るようになったため、同時に二つをロードできるようになった。
  - CX-3 Tonewheel Organ
    同社が発売している[CX-3のモデリング音源](https://ja.wikipedia.org/wiki/コルグ・コンボオルガンシリーズ "wikilink")。本体に搭載されているスライダーにドローバーの機能を割り当て、演奏中にコントロールすることが可能になっている。
  - AL-1 Analog Synthesizer
    [アナログモデリング音源](../Page/バーチャルアナログ音源.md "wikilink")。フルデジタル演算ながらエイリアスノイズを抑え、LFOも高速域で処理が破綻しないなど、ただのモデリングに終始しない高いポテンシャルを持っている。
  - STR-1 Plucked String
    ソフトウェア・バージョン1.1から追加された打弦/撥弦系の[物理モデル音源](../Page/物理モデル音源.md "wikilink")。ギターやハープシコードなどのモデリングを得意とする。EGやLFOのフィルタの構成はAL-1と同一となっている。

さらに、オプションであるエクスパンジョン・インストゥルメントを搭載することにより、以下の音源も追加可能である。

  - LAC-1 Legacy Analog Collection
    コルグ独自のモデリング技術CMT（Component ModelingTechnology）を駆使した、真のモデリング・サウンドを実現したKORG Legacy Collection のMS-20、PolysixをOASYS上で再現し、さらにOASYSならではのチューンナップを行ったMS-20EX、PolysixEX として再構成した音源。
  - EXi MOD-7 Waveshaping VPM Synthesizer
    コルグの物理モデルシンセサイザーProphecy、Z1などのVPM(Variable Phase Modulation)アルゴリズムのテクノロジーをベースにした最新のVPMシンセシス音源。音作りの自由度は[ヤマハ](../Page/ヤマハ.md "wikilink")の[RCM音源](../Page/RCM音源.md "wikilink")をも凌駕する。
  - EXs3 Brass & Woodwinds
    高品位BrassとWoodWindのPCMサンプルとプログラム、コンビネーション。

これらの音源はEXs3を除く全てが[KRONOSに継承され標準搭載されている](https://ja.wikipedia.org/wiki/コルグ・KRONOS "wikilink")。

[Category:シンセサイザー](https://ja.wikipedia.org/wiki/Category:シンセサイザー "wikilink") [Category:コルグ](https://ja.wikipedia.org/wiki/Category:コルグ "wikilink")