> この記事は[MSX-ENGINE](https://ja.wikipedia.org/wiki/MSX-ENGINE)から翻訳されています。


**MSX-ENGINE**とは、[ホームコンピューターとして製品化された](../Page/ホビーパソコン.md "wikilink")[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")用途向けに設計された[カスタムチップ](https://ja.wikipedia.org/wiki/カスタムチップ "wikilink")の名称。

MSX1相当向けにはT7775やT7937、MSX2以降の用途向けにはT9769(**MSX-ENGINE2**(別名MSX2-ENGINE))があり、共に[東芝](../Page/東芝.md "wikilink")が製造を担当した。CPUを内蔵しない[MSX-SYSTEM](../Page/MSX-SYSTEM.md "wikilink")という別のチップも存在する。

## 特徴

  - T7775\[1\] MSX-ENGINE
      - MSX1の機能を1チップに凝縮したCMOS-LSI。
      - クロックジェネレーターを内蔵し、RUNモード、IDOLモード、HOLDモードなどの各モードをプログラムから設定可能。

<!-- end list -->

  - T7937\[2\]
      - [Z80](../Page/Z80.md "wikilink")A相当の[CPU](../Page/CPU.md "wikilink")、[TMS9918](../Page/TMS9918.md "wikilink")相当の[VDP](../Page/VDP.md "wikilink")、[PSG](../Page/Programmable_Sound_Generator.md "wikilink")（AY-3-8910相当）、PPI（i8255相当）を内蔵。
      - スーパーインテグレーション／スーパーマクロセルライブラリーによる設計、1.5um設計ルール、チップダイサイズ10.5×8.6mm、素子数約41000。
      - パッケージは144ピン[QFP](https://ja.wikipedia.org/wiki/QFP "wikilink")

<!-- end list -->

  - T9763
      - パッケージは144ピンQFP

[thumb](https://ja.wikipedia.org/wiki/ファイル:T9769A_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:T9769C_01.jpg "wikilink")

  - T9769 MSX-ENGINE2(もしくはMSX2-ENGINE\[3\])
      - [Z80](../Page/Z80.md "wikilink")相当のCPU、[AY-3-8910](https://ja.wikipedia.org/wiki/AY-3-8910 "wikilink")A相当のPSG、その他各種ポートやインターフェース等、[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")を構成するのに必要な周辺回路を[ワンチップ](https://ja.wikipedia.org/wiki/ワンチップ "wikilink")化。
      - 主に[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")製や[三洋電機](../Page/三洋電機.md "wikilink")製のMSX2と、MSX2+、MSX turboRで使用された。
      - CPUは3.58MHz駆動で使用しているが、パナソニック製のMSX2+では同社のカスタムチップとの協調により5.38MHz駆動させることも出来た。
      - turboRでは、本LSIのほかにシステムLSIとして[S1990](../Page/S1990.md "wikilink")が搭載され、[R800](../Page/R800.md "wikilink")の動作中にはT9769内部のZ80A相当CPUの動作が停止する排他制御が行われた。
  - また、これらに内蔵された、AY-3-8910相当の回路は、東芝のハードマクロセル名はSM7766Aと呼ばれ、ソフトウェアから見た場合は、互換品であるものの、ハードウェアエンベロープの周期などがAY-3-8910とは異なる。

## 位置づけ

本チップのような統合[LSI](https://ja.wikipedia.org/wiki/LSI "wikilink")の登場により、従来は74シリーズなどを多数使用して構成しなければならなかったMSX内部の論理回路や周辺LSIがほぼワンチップに置き換えられ、安価かつ小型に[MSX2](../Page/MSX2.md "wikilink")が製造出来るようになった。

東芝自身は[MSX2](../Page/MSX2.md "wikilink")をもってMSX規格からは撤退したが、東芝がMSX規格から撤退後にMSX参入各社と共同開発した次世代チップのMSX-ENGINE2は、MSX2から最終規格の[MSXturboR](https://ja.wikipedia.org/wiki/MSXturboR "wikilink")までソニー製を除く各社のハードに搭載され続けた。MSX-ENGINEはパチンコ基板や東芝のワープロ『[Rupo](https://ja.wikipedia.org/wiki/Rupo "wikilink")』などにも転用された為、その出荷数はMSX自身の出荷数を遥かに上回ったとされ、「MSXでいちばん儲けたのは東芝だ」と[西和彦](../Page/西和彦.md "wikilink")が言及したといううわさもあるほどであった\[4\]。

## 脚注

<references />

[Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink") [Category:MSX](https://ja.wikipedia.org/wiki/Category:MSX "wikilink")

1.  「ソフトウェアを知りつくしたアスキーの、LSI。」トランジスタ技術 1987年4月号および1986年12月号 広告 CQ出版社
2.  「スーパーインテグレーションの適用事例　東芝　半導体第二応用技術部　平井誠一」エレクトロニクス別冊 超LSI TECHNOLOGY\&APPLICATION No.5
3.  「MSX ハード&ソフト テクニカルデータノート 」月刊HACKER 1989年8/15日号
4.  [実はいちばん儲けた\!? MSX陰の立役者はあのメーカーだった！：MSX30周年](http://weekly.ascii.jp/elem/000/000/152/152761/)　週刊アスキー