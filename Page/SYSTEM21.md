> この記事は[SYSTEM21](https://ja.wikipedia.org/wiki/SYSTEM21)から翻訳されています。


**SYSTEM21**（しすてむ21）は、[1989年](../Page/1989年.md "wikilink")に[ナムコ](https://ja.wikipedia.org/wiki/ナムコ "wikilink")がリリースした、3DCGに特化した[アーケードゲーム基板](../Page/アーケードゲーム基板.md "wikilink")である。別名「**ポリゴナイザー**」（Polygonizer）。

## 概要

従来はグラフィックス表示に[PCGや](https://ja.wikipedia.org/wiki/プログラマブル・キャラクタ・ジェネレータ "wikilink")[スプライトを使用した](../Page/スプライト_\(映像技術\).md "wikilink")[ビットマップグラフィックスが主流であったのに対し](https://ja.wikipedia.org/wiki/ビットマップ画像 "wikilink")、本基板はビットマップ表示に加え、[ポリゴン](../Page/ポリゴン.md "wikilink")を使用した3Dグラフィックス表示を特徴とし、『[ウイニングラン](https://ja.wikipedia.org/wiki/ウィニングラン_\(コンピューターゲーム\) "wikilink")』ほかアーケードゲーム機がよりリアルな3D表示に移行するに至った存在である。なお、3Dポリゴン表示に特化して設計されたアーケードゲーム基板は本基板が初めてではなく、先行する基板として、米国[ATARI社の](../Page/アタリ_\(企業\).md "wikilink")1984年の作品である[I, Robotに用いられた専用基板がある](https://ja.wikipedia.org/wiki/:en:I,_Robot_\(arcade_game\) "wikilink")。

基板構成はメインプログラムやサブプログラム、通信制御、サウンドなどを担当する基板1枚と、画像用ワークRAM等が実装されている基板1枚、ビットマップグラフィックス表示を担当する基板1枚、ポリゴン表示計算などを行う基板1枚で、合計4枚となっている。音源周りやメインCPU、サブCPU周辺は[SYSTEM IIを踏襲した構成となっている](../Page/SYSTEM_II.md "wikilink")。

アーケードゲームで最初期の3DCG基板であるが、レスポンスが重要なシューティングゲームを中心に60fpsを実現した作品が幾つか見られた。2DCG基板を用いた擬似3Dよりも、遥かに正確な3次元空間を実現可能であったため、[VRを志向した作品ばかりであった](https://ja.wikipedia.org/wiki/バーチャルリアリティ "wikilink")。

基盤に搭載されているC140はアーケードゲームでも最初期のPCM音源であり、当時最先端の技術を結集して作られた専用のカスタムチップである。同時発音数24chという、当時としては非常に豪華な仕様であった。C140には、シンセサイザーメーカーのENSONIQが売り込んできた音源チップを見て、[ナムコが同等品を自社開発したという逸話が残っている](../Page/バンダイナムコアミューズメント.md "wikilink")。

## SYSTEM21B

[thumb](https://ja.wikipedia.org/wiki/ファイル:system21b_cpu_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:system21b_video_01.jpg "wikilink")**SYSTEM21B**は、基板4枚で構成されていたSYSTEM21の機能を基板を2枚に収めたもので、POINT ROMなど一部実装できる[ROM容量が少ないが性能は同じである](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")。ウイニングランシリーズのみに特化した仕様といえる。 基板はバックパネルの基板を経由せずに[CPU](../Page/CPU.md "wikilink")ボードと[VIDEOボードを重ねて直接接続する構成となっている](https://ja.wikipedia.org/wiki/グラフィックボード "wikilink")。

### メインボード

メインプログラム、音源制御、画像合成、各種入出力機能を有する。

メインボードにはメインプログラム、サブプログラム、データROM、サウンドプログラムROM(SND0～1)、PCMデータROM(VOI0～3)、POINT ROM(不明)、KEYCUS(コピー防止カスタムIC)が実装されている。

  - 基板型番 ：8622963102
  - シルク型番：8622961101

### CPU

  - メインプログラムMPU：68HC000-12
  - サブプログラムMPU ：68HC000-12
  - ポリゴン座標計算用[DSP](https://ja.wikipedia.org/wiki/デジタルシグナルプロセッサ "wikilink")：TMS320C25

<!-- end list -->

  - メインプログラムシルク表示(MPRL、MPRU)
  - メインプログラムROMラベル表示(MPL、MPL)

<!-- end list -->

  - サブプログラムシルク表示(SPRL、SPRU1)
  - サブプログラムROMラベル表示(SPL、SPU)

<!-- end list -->

  - データROMシルク表示(D0L、D0U、D1L,D1U）
  - データROMラベル表示(DATA0L、DATA0U、DATA1L、DATA1U)

<!-- end list -->

  - ポリゴン座標計算用ROMシルク表示(POINTL、POINTU)
  - ポリゴン座標計算用ROMラベル表示(PTL、PTU)

<!-- end list -->

  - KEYCUS：コピー防止用カスタムチップ

### サウンド

[thumbのものである](https://ja.wikipedia.org/wiki/ファイル:C140_3.jpg "wikilink")\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:Yamaha_YM2151.PNG "wikilink")

  - サウンド制御：68B09E
  - [FM音源](../Page/FM音源.md "wikilink")：[YM2151](https://ja.wikipedia.org/wiki/YM2151 "wikilink")(OPM)
  - FM音源用D/Aコンバータ：YM3012(ステレオ出力)
  - [PCM音源](../Page/PCM音源.md "wikilink")：C140(カスタムチップ)
  - PCM音源用D/Aコンバータ：LC7880

### 通信機能

  - 通信制御用CPU：HD63B05Z (C65)

### VIDEOボード

ビデオボードにはグラフィックプログラムROMとグラフィックデータROMが実装されている。映像信号はこのボードで生成され、コネクタを介しメインボードから出力される。

  - 基板型番 ：8622963202
  - シルク型番：8622961201
  - グラフィックプログラムMPU：68HC000-12

<!-- end list -->

  - グラフィックプログラムROMシルク表示：GPR0L、GPR0U、GPR1L、GPR1U
  - グラフィックプログラムROMラベル表示：GP0L 、GP0U 、GP1L 、GP1U

<!-- end list -->

  - グラフィックデータROMシルク表示：GDT0L、GDT0U、GDT1L、GDT1U
  - グラフィックデータROMラベル表示：GD0L 、GD0U 、GD1L 、GD1U

## SYSTEM21C

**SYSTEM21C**は、ソルバルウ・スターブレード・エアコンバット・サイバースレッドで使用されたもので、4枚基板構成である。大きな変更点はポリゴンボード上のDSPが、TI社TMS320C25からピン互換のカスタム品となっており、1+4基の合計5基に増やされていること。ビデオボードもSYSTEM21/21Bとは大きく異なり、基板上に68000は見受けられない。CPUボードも後期型SYSTEMIIと同じく、通信制御用コントローラがC65からC68になっている。

## 使用ゲーム

  - [ウイニングラン](https://ja.wikipedia.org/wiki/ウイニングラン_\(コンピューターゲーム\) "wikilink") (1989年)
      - ウイニングラン 鈴鹿グランプリ (1989年)
      - ウイニングラン'91 ([1991年](../Page/1991年.md "wikilink"))
  - ドライバーズアイ (1991年?)
  - [ソルバルウ](../Page/ソルバルウ.md "wikilink") (1991年)
  - [スターブレード](https://ja.wikipedia.org/wiki/スターブレード "wikilink") (1991年)
  - [ギャラクシアン<sup>3</sup> プロジェクトドラグーン（シアター6筐体版）](https://ja.wikipedia.org/wiki/ギャラクシアン3 "wikilink") (1993年) -ゲーム部分のみに使用\[1\]。
      - ギャラクシアン<sup>3</sup> アタック オブ ザ ゾルギア ([1994年](../Page/1994年.md "wikilink")) -同上。
  - [エアーコンバット](https://ja.wikipedia.org/wiki/エアーコンバット "wikilink") ([1993年](../Page/1993年.md "wikilink"))
  - [サイバースレッド](https://ja.wikipedia.org/wiki/サイバースレッド "wikilink") (1993年)

## 脚注

### 注釈

### 出典

[Category:バンダイナムコのアーケードゲーム基板](https://ja.wikipedia.org/wiki/Category:バンダイナムコのアーケードゲーム基板 "wikilink")

1.  背景映像には別途で接続された[レーザーディスク](../Page/レーザーディスク.md "wikilink")（LD）を使用。