> この記事は[RamPhantom](https://ja.wikipedia.org/wiki/RamPhantom)から翻訳されています。


**RamPhantom**（ラムファントム）は[アイ・オー・データ機器](https://ja.wikipedia.org/wiki/アイ・オー・データ機器 "wikilink")より発売されている[RAMディスク](https://ja.wikipedia.org/wiki/RAMディスク "wikilink")を構築できる[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。 RamPhantom、RamPhantom2、RamPhantom3、RamPhantom7、RamPhantomEx と発売されてきた。 最新版は、RamPhantomEx。

また、本項目では類似ソフトウェアについても扱っている。

## 特徴

[PCに搭載された](../Page/パーソナルコンピュータ.md "wikilink")[メインメモリ](https://ja.wikipedia.org/wiki/メインメモリ "wikilink")の一部を仮想的に[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")として認識させることで、実際のハードディスクより何倍も高速な読み書きを実現する「RAMディスク」と呼ばれる仮想のハードディスクを構築することができる。ソフトウェア方式の[RAMディスク](https://ja.wikipedia.org/wiki/RAMディスク "wikilink")である。

メインメモリの一部をRAMディスクとして認識させるためにこのディスク分の容量が構築時に確保される。そのため、1GBのメインメモリを搭載している環境で512MBのRAMディスクを構築した場合、利用可能なメインメモリは512MBとなる。

RamPhantom3以降は、32ビットWindowsでのOS管理外領域を利用できるようになった。32ビットWindowsは、たとえ4GB以上のメモリを搭載したPCであっても約3.2GBを超える領域を利用できない(PCにより認識可能な領域は3.2～3.7GBと幅がある)。使われていない管理外領域を有効に活用する手段として「RAMディスク」を利用できることとなった。

[ハードウェア](../Page/ハードウェア.md "wikilink")方式のRAMディスクではRAMディスクにOS自体をインストールできる仕様の物が多いが、*RamPhantom*はソフトウェア方式という制約上、[BIOSからRAMディスクを認識することはできないし](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、RAMディスクにOS自体をインストールすることができない(ブートドライブとして用いることができない)。

## データのバックアップ機能

ソフトウェア方式のRAMディスクであるが故に、再起動やシャットダウン時などにプログラムが終了されるとRAMディスクのデータは消失してしまう。それを防ぐために、*RamPhantom*にはデータのバックアップ機能が実装されている。バックアップ機能には幾つかの設定があり、RAMディスクの使い方に合わせて変更することが可能。

  - バックアップを行わない

<!-- end list -->

  -
    プログラムの終了時にRAMディスクのデータを退避せず、破棄する。次に起動した時は何のデータもないRAMディスクを構築する。テンポラリドライブとして使用する場合に適している。

<!-- end list -->

  - ログオフ時に自動で保存

<!-- end list -->

  -
    Windowsの再起動やシャットダウン時にRAMディスクのデータをハードディスクに退避させ、プログラムを終了する。既定の設定であり、通常の使用には最も適している。

<!-- end list -->

  - WriteBack

<!-- end list -->

  -
    コンピュータのアイドル時間、すなわちCPU使用率が低い時間に隙を見てハードディスクにバックアップデータを書き込む。無駄なくバックアップすることができるが、アイドル時間を確保できなかった場合のバックアップ動作は保証されない。
      - RamPhantom3以降ではこのモードでも再起動・シャットダウン時に保存できるようになった。

<!-- end list -->

  - WriteThrough

<!-- end list -->

  -
    RAMディスクへのデータの書き込みと同時にハードディスクにもバックアップデータを書き込む。データが失われる危険性は他の設定と比べて最も低いが、書き込み時の速度はハードディスクと同じになってしまい、RAMディスクであるメリットが読み出し速度の向上のみとなる。

## エディション

  - RamPhantom7 (32bit) 製品版
  - RamPhantom7 (64bit) 製品版

<!-- end list -->

  -
    製品版であり、購入しないと利用することができない。直販価格2480円。機能制限はなく、どのメーカーのメモリーを使っていても利用できる。

<!-- end list -->

  - RamPhantom7 Free (32bit)
  - RamPhantom7 Free (64bit)

<!-- end list -->

  -
    両者とも無料体験版である。誰でも無償で利用することができる。ただし、RAMディスク容量は「256MBまで」、RAMディスクバックアップ機能に「非対応」という機能制限がある。

<!-- end list -->

  - RamPhantom7 32 LE (32bit)

<!-- end list -->

  -
    同社指定の対象メモリーの購入者がシリアルナンバーの入力で無償ダウンロードすることができる機能制限版。ただし、RAMディスク容量は「2GBまで」という機能制限がある。

## 類似ソフトウェア

  - RAMDISK ユーティリティー - [BuffaloのRAM](https://ja.wikipedia.org/wiki/バッファロー_\(パソコン周辺機器\) "wikilink") Disk構築ソフト。(RamPhantom製品版とは違い)[フリーウェア](../Page/フリーウェア.md "wikilink")である。ただし、「バッファロー製メモリ」をPCに取り付けていなければOS管理外領域を利用することができない。([BUFFALOの説明ページを参照](http://buffalo.jp/products/catalog/memory/speedup/ramdisk.html))
  - Gavotte Ramdisk - OS管理外領域を利用可能にした先駆者的なフリーウェア。有志のバッチファイル導入により多機能を実現可能。ただし、設定項目が多少複雑であり上級者向け。([Impress Watch掲載の](https://ja.wikipedia.org/wiki/Impress_Watch "wikilink")[記事を参照](http://pc.watch.impress.co.jp/docs/2008/0512/ramdisk.htm))
  - 最大192GB対応・RAMDisk「RAMDA」- 電机本舗のRAM Disk構築ソフト。有料版とフリー版が存在する。32bit版、64bit版が存在する。ソフトウェアハウスの作った製品なのでメモリカードの製造メーカなどの依存はない。(電机本舗の外部リンクは[こちら](https://dnki.co.jp/w2/2016/06/13/【フリーウェア】最大192gb対応・ramdisk「ramda」/))。
  - ほか、[:en:RAM diskの外部リンクも参照](https://ja.wikipedia.org/wiki/:en:RAM_disk "wikilink") (英語）

## 外部リンク

  - [I-O DATA](http://www.iodata.jp/)
  - [RamPhantom](http://www.iodata.jp/prod/memory/list/2004/ramphantom/index.htm)
  - [RamPhantom7](http://www.iodata.jp/product/hdd/soft/ramphantom7_32bit/index.htm)
  - [RamPhantomEX（現行品）](http://www.iodata.jp/product/soft/speed/ramphantomex/)

[Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink")