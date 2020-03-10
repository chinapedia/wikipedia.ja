> この記事は[ROM-BASIC](https://ja.wikipedia.org/wiki/ROM-BASIC)から翻訳されています。


**ROM-BASIC**（ロムベーシック）とは、8[ビット](../Page/ビット.md "wikilink")[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")のほとんどと、初期の16ビットパーソナルコンピュータに搭載されていた、[ROMに書き込まれた](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")[スタンドアロンBASIC](../Page/スタンドアロンBASIC.md "wikilink")である。

ROM-BASICという概念は、[コンパクトカセット](../Page/コンパクトカセット.md "wikilink")や[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")などの[補助記憶装置](../Page/補助記憶装置.md "wikilink")に格納した処理系をシステム起動時にロードして使用する方式と対立していう場合と、フロッピーディスクを利用できるように機能拡張した[DISK-BASIC](https://ja.wikipedia.org/wiki/DISK-BASIC "wikilink")と対立していう場合とがある。

## 概要

[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")における[BASIC](../Page/BASIC.md "wikilink")の実装は、最初期には処理系を紙テープに格納して起動時にロードして使用する形態であったが、すぐに数KBのROMに格納して電源投入と共に使用できる形態となった。著名なものは[Apple IIの整数型BASICと](../Page/Apple_II.md "wikilink")、引き続きMicrosoftがApple II向けに開発した10KByte BASICがある。日本では[TK-80](https://ja.wikipedia.org/wiki/TK-80 "wikilink")等のキットのオプションとしてROM-BASICのキットが販売され、次いで[PC-8001](https://ja.wikipedia.org/wiki/PC-8001 "wikilink")がROM-BASICを標準搭載して販売された。以後はパーソナルコンピュータがROM-BASICを搭載し、補助記憶装置として[データレコーダ](../Page/データレコーダ.md "wikilink")を接続して[オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")用[コンパクトカセット](../Page/コンパクトカセット.md "wikilink")でプログラムのセーブやロードを行う使用方法となった。そして、外部補助記憶装置として[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")を接続する時には、その入出力機能を拡張した[DISK-BASIC](https://ja.wikipedia.org/wiki/DISK-BASIC "wikilink")を使用するという形態が暫く続いた。

ROM-BASICは、プログラムを編集する、プログラムをコンパクトカセットにセーブ・ロードする、プログラムを実行・停止するという、OSのごく基本的な機能も備えており、CP/MやMS-DOS等の[OSが普及する以前にはごく簡便なOSとしての役割も担った](../Page/オペレーティングシステム.md "wikilink")。

一方で、パーソナルコンピュータにサウンド機能やグラフィック機能を備えたものでは、それをサポートする命令も備えていた。

### メリット

  - 起動時に[OSやBASICの処理系をロードする時間を要さず](../Page/オペレーティングシステム.md "wikilink")、すぐに使用を開始できる。
  - ROM内部に置かれた[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")をアプリケーション、システムなどからコールすることによって、あらかじめ持っている機能であればスクラッチから書かずとも、それを流用することができる。

### デメリット

  - メリットで挙げたサブルーチンのエントリやデータの受け渡し方法がメーカーによって公開されていることはまれで、[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")開発業者などが解析した結果を[ドキュメント](https://ja.wikipedia.org/wiki/ドキュメント "wikilink")化して[出版](../Page/出版.md "wikilink")したものを入手して参照するか、自力でROM内部を[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")せざるを得なかった。当然[バグフィックス](https://ja.wikipedia.org/wiki/バグフィックス "wikilink")が行われるなどで、ROMの[リビジョン](https://ja.wikipedia.org/wiki/リビジョン "wikilink")が変わってしまうと使えなくなる可能性があった。
  - 互換性維持のために、実用にならない状況にあっても、後継機もまた同じプログラムを本体に持ち続けなければならない。
  - ROM-BASICでサポートされていた[外部記憶装置](https://ja.wikipedia.org/wiki/外部記憶装置 "wikilink")は[オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")用[コンパクトカセット](../Page/コンパクトカセット.md "wikilink")を流用した[データレコーダ](../Page/データレコーダ.md "wikilink")であり、読み書きの速度は300～1600[bpsであり](../Page/ビット毎秒.md "wikilink")、主記憶を越える量のデータの取り扱いに対して低速であった。また、シーケンシャルデバイスであるため、外部記憶装置からの特定のデータの呼び出しなどは実用的ではなかった。

なお、ROM-BASICを搭載しているからという理由ではなく、メモリへの配置の都合で、0番地から配置されたうえで、切り替える方法を持たない機種では、同じ領域を使用する[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")など、先頭部分のアドレスを使用するプログラムの使用には制限が発生する。バンク切り替えなどにより、これらのページを変更できる実装の場合はその限りではない。

多くの機種ではROMはメモリ空間に直接マッピングされたが、[クリーン設計思想で作られていた](https://ja.wikipedia.org/wiki/MZ_\(コンピュータ\)#クリーン設計 "wikilink")[シャープ](../Page/シャープ.md "wikilink")の[X1に用意されていたオプションボードであるCZ](../Page/X1_\(コンピュータ\).md "wikilink")-8RB01は、ROM-BASICでありながら直接マッピングされるわけではなく、拡張ボード上のROMからIPLが読み込みを行い、RAMにBASICを展開する形になっている。そのため、起動後はRAM上のBASICやモニタ部分の書き換えも可能になっており、標準添付のCZ-8CB01と同じように使用することが可能である。同社[MZ (コンピュータ)でも同様の仕組みが存在し](../Page/MZ_\(コンピュータ\).md "wikilink")、サードパーティーのROMボードが存在する。これらの機種では補助記憶装置からのシステムの読み込みを必要とし、こういったボードが装備されていないシステムでは、コールドスタートに際して本体にROM-BASICを内蔵した機種と比較し、時間が掛かった。

[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")では後年までROM-BASICが搭載され続け、起動可能だったが、途中の機種からカセットインタフェースが省略されて単独での使用は実質不可能であった。ただし、ROM内のサブルーチンを利用しているプログラムの互換性を維持するため、ROM自体は必要なものであった。[PC-9821シリーズ](../Page/PC-9821シリーズ.md "wikilink")の初期の機種でも起動できたが、途中の頃から起動できなくなった。[EPSON PCシリーズでは](https://ja.wikipedia.org/wiki/EPSON_PCシリーズ "wikilink")、初期にはROMを搭載していない機種もあったが、搭載している機種でも起動はできないようになっていた。

## 関連項目

  - [DISK-BASIC](https://ja.wikipedia.org/wiki/DISK-BASIC "wikilink")
  - [クリーン設計](https://ja.wikipedia.org/wiki/MZ_\(コンピュータ\)#クリーン設計 "wikilink")

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink")