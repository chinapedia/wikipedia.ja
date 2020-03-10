> この記事は[Serial Attached SCSI](https://ja.wikipedia.org/wiki/Serial_Attached_SCSI)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:SASHardDriveComparsion.jpg "wikilink") **Serial Attached SCSI**（**SAS**; サス）は、[コンピュータ](../Page/コンピュータ.md "wikilink")に[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")等のデバイスを接続するための[インターフェースである](../Page/インタフェース_\(情報技術\).md "wikilink")。[SCSI規格の一種であり](../Page/Small_Computer_System_Interface.md "wikilink")、それまでは[パラレル](https://ja.wikipedia.org/wiki/パラレル "wikilink")伝送であったSCSI規格を、その名の通り[シリアル化したものである](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")。

"Ultra-320 SCSI"の後継にあたる規格であり、パラレルSCSI同様、[サーバ](../Page/サーバ.md "wikilink")マシン用HDDの接続に用いられることが主体である。コンシューマ向けには[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")の方がよく使われている。

[INCITS](https://ja.wikipedia.org/wiki/:en:International_Committee_for_Information_Technology_Standards "wikilink")（International Committee for Information Technology Standards）のT10技術委員会がプロトコルの開発・維持を行い、[SCSITA](https://ja.wikipedia.org/wiki/:en:SCSI_Trade_Association "wikilink")（SCSI Trade Association）が普及活動を行っている。

## 経緯

それまでSCSIはパラレル・インターフェースであったが、2000年3月に規格が策定されたUltra-320でも16組の差動信号線を80MHzのDDRで駆動することは難しく\[1\]、既にこの時点でもかなりの限界が来ていた。2000年から2003年の段階では、より高速な次世代パラレルSCSI規格を策定して製品に実装し出荷することは可能であったが、市場において相互接続した場合に安定的な動作に対する不安要素が多く、そういった規格を製品に実装する事はハードウェアベンダーにとって大きなリスクであった。また、もう1つのHDDインターフェース規格であったパラレルATAが同様の問題を回避するために2000年にシリアルATAへと舵を切り始めたことも、パラレル技術を継続する妥当性が問われた。結局、ATA側と同様にSCSI側でも、太い接続コードと大きなコネクタ類から開放されて、今後の高速化への余地が得られるシリアル化を模索することにした\[2\]。パラレルSCSIとしては次のステップであった"Ultra-640"が2003年に規格として策定されたが、あまり普及していない。

最初の仕様である"SAS-1.0"が2003年5月8日に正式に標準となり\[3\]、2006年頃から本格的に普及し始めている。

## 特徴

[コネクタ](https://ja.wikipedia.org/wiki/コネクタ "wikilink")の形状は[SATAとの互換性があり](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")、SATA規格のデバイスをそのままSASコネクタに嵌合することが可能である（通信が成立するか否かは別問題）。ただしその逆の、SATAインターフェースにSASデバイスを嵌合することは不可能である。

従来のパラレルSCSIと比べてコネクタのサイズが小さくできたため、サーバー用途で望まれていたHDDの小型化が実現でき、SCSI-HDDのサイズがそれまでの3.5インチから2.5インチへと主流サイズが移行しつつある\[4\]。

## 規格

### SAS-1.0

  - 全2重通信のポイント・ツウ・ポイント接続である
  - 3Gb/sの信号帯域幅である（実効データレート 300MB/秒）\[5\]
  - [8b/10b](https://ja.wikipedia.org/wiki/8b/10b "wikilink")エンコード方式
  - 1ポートあたりの最大接続数は128台まで（ただし後述のSAS Expanderを用いる事により約16,384台まで接続が可能）
  - デュアルポート接続が可能である
  - [マルチレーン](https://ja.wikipedia.org/wiki/マルチレーン "wikilink")に対応

### SAS 2.0

### SAS 2.1

  - 6Gb/s（実効データレート600MB/秒）

### SAS 3.0

  - 12Gb/s（実効データレート1200MB/秒）

### SAS 4.0

  - 2017年に策定予定
  - 22.5Gb/s（実効データレート2400MB/秒）
  - 128b/150bエンコード方式

## SAS Expander

SASポート数以上のデバイスを接続可能にするためのもの。主な機能は[LANや](../Page/Local_Area_Network.md "wikilink")[USBの](../Page/ユニバーサル・シリアル・バス.md "wikilink")[ハブのようなものであるが](https://ja.wikipedia.org/wiki/ハブ_\(ネットワーク機器\) "wikilink")、それらに加えてSAS Expanderを多重化する等のことが可能である。

## 脚注・出典

<references />

## 関連項目

  - [SCSI (Small Computer System Interface)](../Page/Small_Computer_System_Interface.md "wikilink")
  - [シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")（SATA）
  - [World Wide Name](https://ja.wikipedia.org/wiki/World_Wide_Name "wikilink")（WWN）

## 外部リンク

  - [International Committee for Information Technology Standards](http://www.incits.org/)
  - [SCSI Trade Association](http://www.scsita.org/)
  - [今年夏に本格始動する次世代のSerial Attached SCSI \[前編\] - SAS HDDとSATA HDDの混在が可能なSASシステム](http://enterprise.watch.impress.co.jp/cda/storage/2005/06/27/5579.html)
  - [今年夏に本格始動する次世代のSerial Attached SCSI \[中編\] - SASのコネクタ仕様と物理層の電気特性](http://enterprise.watch.impress.co.jp/cda/storage/2005/07/04/5640.html)
  - [今年夏に本格始動する次世代のSerial Attached SCSI \[後編\] - HBAやRAIDコントローラの登場が待たれるSASシステム](http://enterprise.watch.impress.co.jp/cda/storage/2005/07/11/5698.html)

[Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink")

1.  プリエンファシスやトレーニングといったシグナルスキューを抑える機能やマルチドロップによる影響を押さえ込む努力はなされたが、回路規模が大きくなるなど弊害が無視出来ない。
2.  現状のSAS-1でもSASのコネクタをSATA-HDDに直接差し込むことができる。SASコントローラの中には、接続されたSATA-HDDを正しく認識してSATAモードに切り替わりSATAコントローラとして機能するものがある。"SAS-2"では、SASとSATAの信号線は電気的に全く同一となり、異なるのは信号を生成・解釈する上位プロトコルである。
3.  [SCSI Trade Association "STA ANNOUNCES COMPLETION OF SERIAL ATTACHED SCSI SPECIFICATION"](http://www.scsita.org/news_events/dirReleases/STA_pr_051603.html) 英語
4.  サーバー用途で小型HDDが求められる理由を説明する。PC-AT互換機を始祖とするサーバー用x86系コンピュータは、CPUとメモリ、HDDの1セットを1台の19インチラック内にどれだけ組み込めるかが重要な要素となり、多くの場合、1U:1.75インチ=44.45mmやその整数倍の厚みで50cm×70-80cmほどの中に、4基や20基ほどのPC相当のサーバー機が詰め込まれ、3.5インチより2.5インチが歓迎される傾向がある。磁気を帯びた回転円盤（プラッタ）は、同じ回転数であれば大型の方が線速度が速くなり転送速度が向上するが、小型の方がヘッドの移動が早くシーク速度が向上する一方で、容易に高速回転化できるので線速度と回転待ち時間も相殺できる。[RAID](../Page/RAID.md "wikilink")化する場合が多いので、大規模ファイルサーバーを除けば、小型HDDのほうが比較的好まれる。
5.  2009年4月に"SAS-2"のドラフトが決まった。SAS-2では1.5/3/6Gb/s (gigatransfers per second) になる予定であり、2010年9月現在は"SAS-2.1"と"SAS-3"が作業中である。"SAS-3"では、12Gb/sを実現する予定。