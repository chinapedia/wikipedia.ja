> この記事は[Intel 8259](https://ja.wikipedia.org/wiki/Intel_8259)から翻訳されています。


**Intel 8259**は[Programmable Interrupt Controller](https://ja.wikipedia.org/wiki/Programmable_Interrupt_Controller "wikilink")(PIC)の一種であり、[Intel 8080や](../Page/Intel_8080.md "wikilink")[Intel 8085](../Page/Intel_8085.md "wikilink")、[Intel 8086のような](../Page/Intel_8086.md "wikilink")8bitや16bitの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の周辺LSIとして、同社により設計・開発された。8259はIntel 8080, 8085用で、8259Aは、Intel 8086, 8088にも対応した。今日では多くのメーカーから幅広く互換チップが提供されている。8259は[マルチプレクサ](https://ja.wikipedia.org/wiki/マルチプレクサ "wikilink")、つまり一つのデバイスに割り込みをかけるため、複数の割り込み入力を一つの割り込み出力に束ねるように振舞う。

## 歴史

8259は1980年に初代PCに採用され、1983年に開発されたPC/XTでも引き続き採用された。2番目の8259は[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")の開発の際に追加された。8259は[対称型マルチプロセッサ](https://ja.wikipedia.org/wiki/対称型マルチプロセッサ "wikilink")PCでも採用されたので、[APIC](../Page/APIC.md "wikilink")と共存している。

8259は元々単体のチップであったが、いまや最近のx86マザーボードでは[サウスブリッジ](../Page/サウスブリッジ.md "wikilink")([ICH](https://ja.wikipedia.org/wiki/I/O_コントローラー・ハブ "wikilink"))やプラットフォームコントローラーハブ(PCH)の一部となっている。

## 特徴

8259での主要な接続ピンは以下のようなものである。8本の割り込み要求入力(IRQ0～IRQ7)、1本の割り込み出力(INTR)、割り込みACK(INTA)、割り込みレベルないし割り込みベクタオフセット用通信ライン(D0-D7)である。CAS0からCAS2を使って8259同士を[カスケード](https://ja.wikipedia.org/wiki/カスケード "wikilink")接続することができる。

マスターとなる8259に8個までの8259をスレーブ接続できるので、全部で64個のIRQを提供できる。つまり、マスターの8259のIRQにスレーブの8259のINTをカスケード接続する。

8259には3つのレジスタ、**Interrupt Mask Register**(IMR)、**Interrupt Request Register**(IRR)、**In-Service Register**(ISR)がある。IRRはACKを未処理の現在の割り込み[マスクを保持し](https://ja.wikipedia.org/wiki/マスク_\(情報工学\) "wikilink")、ISRはEOIを未処理の割り込みマスクを保持し、IMRはACKを送信してはならない割り込みのマスクを保持する。

[End Of Interrupt](https://ja.wikipedia.org/wiki/:en:End_of_interrupt "wikilink")(EOI)は指定EOI、非指定EOI、自動EOIをサポートしている。指定EOIはISRのACKを返すIRQレベルを指定する。非指定EOIはISRのIRQレベルをリセットする。自動EOIは割り込みにACKが返ってきた後、すぐにISRのIRQレベルをリセットする。

エッジおよびレベル割り込みトリガモードをサポートしている。

優先度設定および優先度回転モードもサポートしている。

## プログラミング上の考慮点

### DOSとWindows

[MS-DOS](../Page/MS-DOS.md "wikilink")や[Microsoft Windowsで](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")8259を使う際には、後方互換性、つまり1981年に採用された初代PCと互換性を残しつつ拡張してきたため、多くの面倒な問題が持ち込まれる。

最初の問題は2番目の問題の根っこになっている。DOSのデバイスドライバは8259に対してデバイスの処理を終了したときに非指定EOIを送ることを期待されている。つまりDOSでは8259の他のEOIモードは使用を禁止されている。そして、マスターの8259からスレーブの8259に対して再接続されている複数のデバイス割り込みの間には違いはない。

2番目の問題はPC/ATでスレーブの8259が採用されてからIRQ2からIRQ9までの扱いについてである。スレーブの8259のINT出力はマスターのIR2につながっている。ISAバスのIRQ2は元々このIR2につながっていたが、スレーブのIR1に再接続されている。このように古いIRQ2は今やCPUのIRQ9割り込みを発生させる。IRQ2を使用するように設定された装置との後方互換性を維持するために、IRQ9の[割り込みハンドラ](https://ja.wikipedia.org/wiki/割り込みハンドラ "wikilink")として、IRQ2の割り込みハンドラを呼び出すものがBIOSによってインストールされる。

### エッジ／レベルトリガモード

ISAバスはレベルトリガ割り込みをサポートしていない。レベルトリガモードはISAデバイスに接続された割り込みを使うことができないかもしれない。これはPC/XT、PC/ATそしてMCAシステムでは8259は必ずエッジトリガモードに設定しなければならないことを意味する。より新しいEISA、PCI、その他後継のシステムでは、エッジ／レベルコントロールレジスタ(ELCRs)がIRQラインを制御し、ISAバスのあるようなシステムに対して、8259のモードとは無関係に効果的に制御を行う。正しく制御を行うためにELCRはBIOSによってシステム起動時に設定される。

x86のI/Oアドレス空間のELCRは0x4d0と0x4d1に配置されている。そのレジスタは8bit幅であって8259から出ているIRQとそれぞれのビットが一致している。あるビットをセットするとそのIRQはレベルトリガモードになり、リセットするとエッジトリガモードになる。

### スプリアス割り込み

8259はいろいろな条件に対して反応できるようにスプリアス割り込みを発生する。

最初、IRQはACKを返す前にLからHに変位する。これはひょっとしてIRQラインにノイズが入ったせいかもしれない。エッジトリガモードでは、このノイズは100nsの間Lの状態に保持されなければならない。もしノイズが小さくなれば、[プルアップ抵抗](https://ja.wikipedia.org/wiki/プルアップ抵抗 "wikilink")がIRQラインをHに押し上げ、誤った割り込みが発生したことになる。レベルトリガモードでは、ノイズはシステムのINTRラインでH信号を引き起こしているかもしれない。もし、システムがACK要求を投げると、8259はどの割り込みが発生したかを返すことができず、例えばIRQ7を送ってしまう。この場合はIRQ7のスプリアス割り込みが発生する。

2つ目は、スレーブのIRQラインが割り込みACKの立ち下がりエッジでアクティブになっていない時、マスターの8259のIRQ2がアクティブHになることがある。この場合はIRQ15のスプリアス割り込みが発生するが、非常にまれである。

## PC/XTとPC/AT

PC/XTのISAシステムは8259コントローラを1個だけ持っていたが、一方PC/AT及びその後のシステムはマスター、スレーブと2つの8259コントローラを持っていた。IRQ0からIRQ7までがマスターの8259の割り込みラインで、IRQ8 からIRQ15はスレーブの8259の割り込みラインである。8259のピンの実際の名前はIR0からIR7である。IRQ0からIRQ15という名前は、8259に歴史的に接続されていたISAバスのラインによるものである。

  - Master 8259
      - IRQ0 – [Intel 8253](https://ja.wikipedia.org/wiki/:en:Intel_8253 "wikilink") or [Intel 8254](https://ja.wikipedia.org/wiki/:en:Intel_8253 "wikilink") [Programmable interval timer](https://ja.wikipedia.org/wiki/:en:Programmable_interval_timer "wikilink")、すなわちシステムタイマ
      - IRQ1 – [キーボード](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink")
      - IRQ2 – PC/XTでは割り当てなし。PC/ATではスレーブの8259のINTにカスケード接続されている。
      - IRQ3 – [シリアルポート](../Page/シリアルポート.md "wikilink")COM2及びCOM4
      - IRQ4 – シリアルポートCOM1及びCOM3
      - IRQ5 – PC/XTではハードディスクコントローラ。PC/ATでは[LPT](https://ja.wikipedia.org/wiki/LPT "wikilink")2。
      - IRQ6 – [フロッピーディスク](../Page/フロッピーディスク.md "wikilink")コントローラ
      - IRQ7 – LPT1

<!-- end list -->

  - Slave 8259 (PC/AT及びその後継のみ)
      - IRQ8 – [リアルタイムクロック](https://ja.wikipedia.org/wiki/リアルタイムクロック "wikilink") (RTC)
      - IRQ9 – 割り当てなし
      - IRQ10 – 割り当てなし
      - IRQ11 – 割り当てなし
      - IRQ12 – [PS/2](https://ja.wikipedia.org/wiki/PS/2コネクタ "wikilink")[マウス](../Page/マウス_\(コンピュータ\).md "wikilink")
      - IRQ13 – 数値演算[コプロセッサ](https://ja.wikipedia.org/wiki/コプロセッサ "wikilink")
      - IRQ14 – ハードディスクコントローラ1
      - IRQ15 – ハードディスクコントローラ2

最初、IRQ7はサウンドカード用によく使われていたが、後にIRQ7はプリンタポート(LPT1)に使われるようになってから、IRQ5が使われるようになった。シリアルポートは他のデバイスのためにIRQを開放するため、しばしば無効にされた。

## 外部リンク

  - [8259A Programmable Interrupt Controller](http://pdos.csail.mit.edu/6.828/2005/readings/hardware/8259A.pdf)
  - [パソコンのレガシィI/O活用大全(桑野　雅彦) CQ出版](http://www.cqpub.co.jp/column/books/2001a/34331PC_Legacy/default.htm)

[Category:インテル](https://ja.wikipedia.org/wiki/Category:インテル "wikilink") [Category:割り込み_(コンピュータ)](https://ja.wikipedia.org/wiki/Category:割り込み_\(コンピュータ\) "wikilink")