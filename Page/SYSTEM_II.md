> この記事は[SYSTEM II](https://ja.wikipedia.org/wiki/SYSTEM_II)から翻訳されています。


**SYSTEM II**（システムツー）は、[1988年](../Page/1988年.md "wikilink")に[ナムコ](https://ja.wikipedia.org/wiki/ナムコ "wikilink")（現・[バンダイナムコエンターテインメント](../Page/バンダイナムコエンターテインメント.md "wikilink")）が開発した[アーケードゲーム基板](../Page/アーケードゲーム基板.md "wikilink")。

## 概要

画像出力はハードウェアで[ビットマップ画像](https://ja.wikipedia.org/wiki/ビットマップ画像 "wikilink")の拡大・縮小・回転機能を有し、これらの機能を効果的に利用したゲームが多く開発されている。基板はメインボード上にビデオボード（サブボード）や、必要によりオブジェクトボードを重ねて接続する構成となっている。ゲームROMはメインボード、ビデオボードそれぞれのROMソケットに実装する。交換にはマイナスドライバーでも行えるが、安全に行うためにはROM抜き用の工具が必要であるため、基板の取り扱いになれたオペレータが交換作業を行う必要があった。

なお、柔軟な拡張性や知名度がある割りに、他社の同時期のシステム基板と比較して作品数が少ない。これは、1990年代初頭にこの基板の製造を請け負っていた企業が倒産したために、ナムコが新作ゲームの開発プラットフォームを他のシステム基板に移したからである。そのため、故障の種類によっては、軽度であってもメーカー修理が不可能な場合がある。

ナムコが次に開発したシステム基板は、主に3Dポリゴンを得意とした大型専用筐体向けの[SYSTEM21](https://ja.wikipedia.org/wiki/SYSTEM21 "wikilink")である。ドット絵やスプライトによる2Dと擬似3Dを得意とした本基板の後継的存在は[NA-1](https://ja.wikipedia.org/wiki/NA-1_\(アーケードゲーム基板\) "wikilink")、[NA-2](https://ja.wikipedia.org/wiki/NA-2 "wikilink")である。

## ハードウェア

画像:System ii main 01.jpg|SYSTEM II MAIN BOARD 画像:System_ii_video_01.jpg|SYSTEM II VIDEO BOARD 画像:System ii main 02.jpg|SYSTEM II MAIN BOARD（二代目） 画像:System_ii_v56_video_01.jpg|SYSTEM II V56 VIDEO BOARD 画像:System_ii_obj_01.jpg|SYSTEM II OBJECT BOARD

### メインボード

メインプログラム、音源制御、画像合成、各種入出力機能を有する。初期型と二代目があり、通信制御CPUが日立製(C65)から三菱製(C68)に変更されたほか、多少の改良が行われている。

メインボードにはメインプログラム (MPR0〜1)、サブプログラム (SPR0〜1)、文字キャラクターROM (CHR0〜7)、データROM (DATA0〜3)、サウンドROM (SND0〜1)、PCMデータROM (VOICE0〜2)、SHAPE（不明）が実装されている。

  - 初期型
      - 基板型番 ：8618963200
      - シルク型番：8618961200
  - 二代目
      - 基板型番 ：8618963905
      - シルク型番：8618961805
  - CPU
      - メインプログラム：[MC68000](../Page/MC68000.md "wikilink")
      - サブプログラム ：[MC68000](../Page/MC68000.md "wikilink")

[thumb](https://ja.wikipedia.org/wiki/ファイル:C140_3.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Yamaha_YM2151.PNG "wikilink")

  - サウンド
      - サウンド制御：[68B09](../Page/MC6809.md "wikilink")
      - [FM音源](../Page/FM音源.md "wikilink")：[YM2151](https://ja.wikipedia.org/wiki/YM2151 "wikilink")(OPM)
      - FM音源用D/Aコンバータ：YM3012（ステレオ出力）
      - [PCM音源](../Page/PCM音源.md "wikilink")：C140（カスタムチップ 24ch）
      - PCM音源用D/Aコンバータ：LC7880またはLC7881
  - 入出力
      - JAMMA準拠ジョイスティック、ボタン入力端子類
      - アナログ入力：8ch（=8軸）
  - 通信機能
      - 通信制御用：HD63B05Z(C65)（初期型）、またはC68（二代目）

### VIDEOボード

VIDEOボードは画像効果の機能を担当する。ゲームにより標準タイプのものと専用タイプのものがある。下記は標準タイプである。

ビデオボードには背景等の拡大・縮小・回転用データROM (ROZ0〜7)、スプライトキャラクターなどのオブジェクトROM (OBJ0〜7) が実装される。

  - 基板型番 ：8618963300（半田面）
  - シルク型番：8618961200

### V56 VIDEOボード

V56 VIDEOボードは[ラスタースクロール](../Page/ラスタースクロール.md "wikilink")機能を提供するカスタムチップ「C107」を搭載しており、同機能を必要とする[ファイナルラップ](../Page/ファイナルラップ.md "wikilink")シリーズなどに使用されている。拡大・回転・縮小機能は持たない。このボードにはスプライトキャラクターのオブジェクトROMとして4Mビットが4つ実装できるようにICソケットが設けられているが、ファイナルラップではこのICソケットは使用されておらず、後述のオブジェクトボード上に実装されている。なおカスタムチップ「C107」は[サンダーセプター](https://ja.wikipedia.org/wiki/サンダーセプター "wikilink")でハイパーウェイを表示するために2つ使用されており、この流用といえる。

  - 構成
      - 基板型番 ：2272961200
      - シルク型番：2272963100
      - 64KビットOTPROM,70ns(LH5762-70)×1
      - 64KビットSRAM,100ns(TMM2063P-10)×2
      - 16KビットSRAM,25ns(TMM2018AP-25)×4
      - 16KビットSRAM,45ns(TMM2018AP-45)×2
      - 256KビットDRAM(4ビット(ニブル)構成),120ns(HM50464P-12)×4
      - カスタムチップ C45
      - カスタムチップ C106
      - カスタムチップ C107
      - カスタムチップ C134
      - カスタムチップ C135
      - カスタムチップ C137
      - カスタムチップ C146
      - PAL FL1-1
      - PAL FL1-2
      - PAL FL1-3

### オブジェクトボード

ゲームの内容により、ビデオボードに実装しきれず、大容量のROMチップを使用することがコスト面で不利な場合、別基板でオブジェクトROMを実装する際に用いられる。スプライトキャラクターのオブジェクトROM(OBJ0〜3)を実装可能。

  - 基板型番 ：2294963201（『[ファイナルラップ](../Page/ファイナルラップ.md "wikilink")3』の例）
  - シルク型番：2294961301（『ファイナルラップ3』の例）

## タイトル一覧

  - [アサルト](../Page/アサルト.md "wikilink")・[アサルト](../Page/アサルト.md "wikilink")プラス (SYSTEM II 第1弾)
  - [オーダイン](../Page/オーダイン.md "wikilink") (SYSTEM II 第2弾)
  - [未来忍者](https://ja.wikipedia.org/wiki/未来忍者 "wikilink") (SYSTEM II 第3弾)
  - [フェリオス](https://ja.wikipedia.org/wiki/フェリオス "wikilink") (SYSTEM II 第4弾)
  - [ワルキューレの伝説](../Page/ワルキューレの伝説.md "wikilink") (SYSTEM II 第5弾)
  - [ファイネストアワー](https://ja.wikipedia.org/wiki/ファイネストアワー "wikilink") (SYSTEM II 第6弾)
  - [バーニングフォース](../Page/バーニングフォース.md "wikilink") (SYSTEM II 第7弾)
  - [マーベルランド](https://ja.wikipedia.org/wiki/マーベルランド "wikilink") (SYSTEM II 第8弾)
  - [球界道中記](../Page/球界道中記.md "wikilink") (SYSTEM II 第9弾)
  - [ドラゴンセイバー](https://ja.wikipedia.org/wiki/ドラゴンセイバー "wikilink") (SYSTEM II 第10弾)
  - [ローリングサンダー2](https://ja.wikipedia.org/wiki/ローリングサンダー_\(コンピュータゲーム\) "wikilink") (SYSTEM II 第11弾)
  - [スーパーワールドスタジアム](../Page/SUPERワールドスタジアム.md "wikilink") (SYSTEM II 第12弾)
  - [コズモギャング・ザ・ビデオ](https://ja.wikipedia.org/wiki/コズモギャング・ザ・ビデオ "wikilink") (SYSTEM II 第13弾)
  - スーパーワールドスタジアム'92 (SYSTEM II 第14弾)
  - スーパーワールドスタジアム'92激闘版 (SYSTEM II 第15弾)
  - スーパーワールドスタジアム'93激闘版 (SYSTEM II 第16弾)

　以下は、SYSTEM IIをベースとしたカスタム基板を使用した作品である。

  - [ファイナルラップ](../Page/ファイナルラップ.md "wikilink")
  - [メタルホーク](https://ja.wikipedia.org/wiki/メタルホーク "wikilink")
  - [ダートフォックス](https://ja.wikipedia.org/wiki/ダートフォックス "wikilink")
  - [フォートラックス](https://ja.wikipedia.org/wiki/フォートラックス "wikilink")
  - [ファイナルラップ](../Page/ファイナルラップ.md "wikilink")2
  - [ゴーリーゴースト](https://ja.wikipedia.org/wiki/ゴーリーゴースト "wikilink")
  - [スティールガンナー](../Page/スティールガンナー.md "wikilink") （SYSTEM IIを2枚使用）
  - [スティールガンナー2](https://ja.wikipedia.org/wiki/スティールガンナー2 "wikilink") （SYSTEM IIを2枚使用）
  - [コカコーラ スズカエイトアワーズ](https://ja.wikipedia.org/wiki/コカコーラ_スズカエイトアワーズ "wikilink")
  - [ファイナルラップ](../Page/ファイナルラップ.md "wikilink")3
  - [ラッキー＆ワイルド](https://ja.wikipedia.org/wiki/ラッキー＆ワイルド "wikilink")
  - [スズカエイトアワーズ2](https://ja.wikipedia.org/wiki/スズカエイトアワーズ2 "wikilink")

## その他

音源チップのC140は、システムIIの開発時にENSONIQ（エンソニック）からナムコへ音源の売り込みがあった。この音源を見たハードの開発陣が、「これだったら自分たちでも作れる」と自社でサンプリング音源を製作した。C140が24チャンネル発声なのは、ENSONIQからの売り込みの音源が24チャンネルだったためである\[1\]。

またFM音源のライトの遅さからくる、チップに指示を出してから実行されるまでのラグ（遅延）を解消するために、[FIFO](https://ja.wikipedia.org/wiki/FIFO "wikilink")用に専用のカスタムICとデュアルポートのRAMをこの為だけにボード上に実装している。バッファからCPUが直接データを取って行くことによりラグを解消していた\[2\]。

## 脚注

[Category:バンダイナムコのアーケードゲーム基板](https://ja.wikipedia.org/wiki/Category:バンダイナムコのアーケードゲーム基板 "wikilink")

1.  OBS（おにたま放送局）「FM音源ドライバーズサミット2」[細江慎治](https://ja.wikipedia.org/wiki/細江慎治 "wikilink")のコメントより。
2.