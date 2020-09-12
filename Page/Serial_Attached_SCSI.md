> この記事は[Serial Attached SCSI](https://ja.wikipedia.org/wiki/Serial_Attached_SCSI)から翻訳されています。


[代替文=](https://ja.wikipedia.org/wiki/ファイル:SFF-8484-internal-connector-0a.jpg "wikilink") **Serial Attached SCSI**（**SAS**; サス）は、[コンピュータ](../Page/コンピュータ.md "wikilink")に[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")等のデバイスを接続するための[インターフェースである](../Page/インタフェース_\(情報技術\).md "wikilink")。[SCSI規格の一種であり](../Page/Small_Computer_System_Interface.md "wikilink")、それまでは[パラレル](../Page/パラレル.md "wikilink")伝送であったSCSI規格を、その名の通り[シリアル化したものである](../Page/シリアル通信.md "wikilink")。

"Ultra-320 SCSI"の後継にあたる規格であり、パラレルSCSI同様、[サーバ](../Page/サーバ.md "wikilink")マシン用HDDの接続に用いられることが主体である。コンシューマ向けには[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")の方がよく使われている。

[INCITS](https://ja.wikipedia.org/wiki/:en:International_Committee_for_Information_Technology_Standards "wikilink") ()のT10技術委員会がプロトコルの開発・維持を行い、[SCSITA](https://ja.wikipedia.org/wiki/:en:SCSI_Trade_Association "wikilink")（SCSI Trade Association）が普及活動を行っている。

## 経緯

それまでSCSIはパラレル・インターフェースであったが、2000年3月に規格が策定されたUltra-320でも16組の差動信号線を80 MHzのDDRで駆動することは難しく、既にこの時点でもかなりの限界が来ていた\[1\]。2000年から2003年の段階では、より高速な次世代パラレルSCSI規格を策定して製品に実装し出荷することは可能であったが、市場において相互接続した場合に安定的な動作に対する不安要素が多く、そういった規格を製品に実装する事はハードウェアベンダーにとって大きなリスクであった。また、もう1つのHDDインターフェース規格であったパラレルATAが同様の問題を回避するために2000年にシリアルATAへと舵を切り始めたことも、パラレル技術を継続する妥当性が問われた。結局、ATA側と同様にSCSI側でも、太い接続コードと大きなコネクタ類から開放されて、今後の高速化への余地が得られるシリアル化を模索することにした。パラレルSCSIとしては次のステップであった"Ultra-640"が2003年に規格として策定されたが、あまり普及していない。

最初の仕様である"SAS-1.0"が2003年5月8日に正式に標準となり\[2\]、2006年頃から本格的に普及し始めている。

## 特徴

[コネクタ](../Page/コネクタ.md "wikilink")の形状は[SATAとの互換性があり](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")、SATA規格のデバイスをそのままSASコネクタに嵌合することが可能である。ただしその逆の、SATAインターフェースにSASデバイスを嵌合することは不可能である。

従来のパラレルSCSIと比べてコネクタのサイズが小さくできたため、サーバー用途で望まれていたHDDの小型化が実現でき、SCSI-HDDのサイズがそれまでの3.5インチから2.5インチへと主流サイズが移行しつつある。

## 規格

### SAS-1.0

  - 全2重通信のポイント・ツウ・ポイント接続である
  - 3 Gb/sの信号帯域幅である\[3\]（実効データレート 300 MB/秒）
  - [8b/10b](https://ja.wikipedia.org/wiki/8b/10b "wikilink")エンコード方式
  - 1ポートあたりの最大接続数は128台まで（ただし後述のSAS Expanderを用いる事により約16,384台まで接続が可能）
  - デュアルポート接続が可能である
  - [マルチレーン](https://ja.wikipedia.org/wiki/マルチレーン "wikilink")に対応\[4\]

### SAS 2.0

### SAS 2.1

  - 6 Gb/s（実効データレート600 MB/秒）

### SAS 3.0

  - 12 Gb/s（実効データレート1200 MB/秒）

### SAS 4.0

  - 2017年に策定予定
  - 22.5 Gb/s（実効データレート2400 MB/秒）
  - 128b/150bエンコード方式

## SAS Expander

SASポート数以上のデバイスを接続可能にするためのもの。主な機能は[LANや](../Page/Local_Area_Network.md "wikilink")[USBの](../Page/ユニバーサル・シリアル・バス.md "wikilink")[ハブのようなものであるが](../Page/ハブ_\(ネットワーク機器\).md "wikilink")、それらに加えてSAS Expanderを多重化する等のことが可能である。

## 脚注・出典

### 注釈 

## 出典 

## 関連項目

  - [SCSI (Small Computer System Interface)](../Page/Small_Computer_System_Interface.md "wikilink")
  - [シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")（SATA）
  - [World Wide Name](../Page/World_Wide_Name.md "wikilink")（WWN）

## 外部リンク

  - [International Committee for Information Technology Standards](http://www.incits.org/)
  - [SCSI Trade Association](http://www.scsita.org/)

[Category:SCSI](https://ja.wikipedia.org/wiki/Category:SCSI "wikilink") [Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink")

1.
2.
3.
4.