> この記事は[PowerPC 604](https://ja.wikipedia.org/wiki/PowerPC_604)から翻訳されています。


**PowerPC 604**シリーズは[アップルコンピュータ](../Page/アップル_\(企業\).md "wikilink")、[モトローラ](../Page/モトローラ.md "wikilink")、[IBM](../Page/IBM.md "wikilink")が共同で開発した、[32ビット](../Page/32ビット.md "wikilink")の[RISC](../Page/RISC.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。[PowerPC 601の後継として演算能力に主眼を置いて開発された](../Page/PowerPC_601.md "wikilink")。アップルコンピュータの[Power Macintoshシリーズなどに広く採用された](../Page/Power_Macintosh.md "wikilink")。

PowerPC 604には発展系の604e及び604evがある。604evはMach5の名称でも知られている。

## 設計

PowerPC 604シリーズは601シリーズに比べ強力な演算能力を持つ。また、601シリーズと異なり[POWERアーキテクチャとの互換性はない](https://ja.wikipedia.org/wiki/Power_Architecture "wikilink")。主な仕様は以下の通りである。

  - 4命令実行の[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")可能な[スーパースカラ](https://ja.wikipedia.org/wiki/スーパースカラ "wikilink")コア
  - 36ビットのアドレスバス (うち4ビットはパリティ)
  - 内部[64ビット](../Page/64ビット.md "wikilink")/外部72ビットのデータバス (うち8ビットはパリティ)
  - 整数演算ユニット×3 (ALU×2、乗除算ユニット×1)
  - [浮動小数点演算ユニット](../Page/FPU.md "wikilink")×1
  - 604では32KB、604e及び604evでは64KBの[L1キャッシュ](../Page/キャッシュ.md "wikilink")
  - 604及び604eではシステムバスに[L2キャッシュ](../Page/キャッシュ.md "wikilink")、604evではインラインL2キャッシュに対応
  - コア1.9V、I/O3.3Vの動作電圧
  - 消費電力はPowerPC 604e 250MHzにおいて6W/10W（平均/最高)
  - パワーマネージメントシステム
  - [マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")対応

動作クロックは初期の604で120MHz、最終的には604eで350MHz、604evで400MHz（パソコンに搭載されたのは350MHzまで）。

## 特徴

PowerPC 604シリーズの特徴はその強力な演算能力にある。3つの整数演算ユニット、1つの浮動小数点ユニットを並列で動作させることができ、マルチプロセッサ構成にも対応していた。消費電力は、同世代の[PowerPC 603シリーズに比べ大きいものの](../Page/PowerPC_603.md "wikilink")、[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")シリーズと比べると小さく、比較的消費電力の少ないプロセッサであった。

アップルのPower MacintoshシリーズやIBMのRS/6000シリーズなど、ミッドレンジから[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")向けの据え置き型[パソコンや](../Page/パーソナルコンピュータ.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")に採用された。

卓越した演算能力は大きな特徴であったが、その一方で構造が複雑で高クロック化が難しいという欠点も抱えていた。また末期にはL2キャッシュシステムの旧弊化が目立ち、その打開策としてMach5で採用したインラインキャッシュは非常に複雑で部品点数も多く、価格の高騰を招いた。

Mach5登場の僅か数ヶ月後には、アップルはPowerPC 750を、新たに[PowerPC G3と名付けて採用した](../Page/PowerPC_G3.md "wikilink")。604はG3コアよりも多くの演算器、より強力なアウト・オブ・オーダー実行機構を持っていたが、整数演算性能についてはG3コアに対して大きな差を付けることができなかった\[1\]。その後IBMとモトローラは604ではなく、G3をベースにPowerPCファミリの開発を行なっていったため、直接の後継となるプロセッサは存在しない。ただし、604シリーズの強力な浮動小数点ユニットは後にモトローラの[PowerPC G4に採用された](../Page/PowerPC_G4.md "wikilink")。

## 製品

  - PowerPC 604
  - PowerPC 604e
  - PowerPC 604ev

## 脚注

## 関連項目

  - [PowerPC](../Page/PowerPC.md "wikilink")

[en:PowerPC 600\#PowerPC 604](https://ja.wikipedia.org/wiki/en:PowerPC_600#PowerPC_604 "wikilink")

[Category:IBMのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:IBMのマイクロプロセッサ "wikilink") [Category:アップルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:アップルのマイクロプロセッサ "wikilink") [Category:モトローラのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:モトローラのマイクロプロセッサ "wikilink")

1.  750の3way(うち1は分岐に限定)スーパースカラに対して604は4way、750の2つの整数演算ユニットに対して604は3つ、750の各整数演算につき1エントリのリザベーション・ステーションに対して604は2エントリ、750の6エントリのリオーダバッファに対して604は16エントリと、コアのスペック上は全ての面で604が上回っていた。しかし、SPECint95ベンチマークの比較では750の13.2@300MHzに対して604eの14.6@350MHzと大差なく、クロックあたりの性能では逆転されていた。これは、750のバックサイドキャッシュが強力であったことと、整数演算のパイプライン段数が750の4に対して604は6とやや長く、分岐ミス時のペナルティが大きかったことが要因として考えられる。