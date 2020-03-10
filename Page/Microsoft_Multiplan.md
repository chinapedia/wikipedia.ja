> この記事は[Microsoft Multiplan](https://ja.wikipedia.org/wiki/Microsoft_Multiplan)から翻訳されています。


**Microsoft Multiplan**（マイクロソフト マルチプラン）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した初期の[表計算ソフト](../Page/表計算ソフト.md "wikilink")の名称である。

## 概要

[1982年](../Page/1982年.md "wikilink")に登場した当時は[Apple IIおよび](../Page/Apple_II.md "wikilink")[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")向け\[1\]だった。その後[MS-DOS](../Page/MS-DOS.md "wikilink")や[XENIX](../Page/XENIX.md "wikilink")を含むいくつかの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上に[移植された](https://ja.wikipedia.org/wiki/移植_\(ソフトウェア\) "wikilink")。また、[コモドール64](https://ja.wikipedia.org/wiki/コモドール64 "wikilink")、[TI-99/4A](https://ja.wikipedia.org/wiki/TI-99/4A "wikilink")、[TRS-80](https://ja.wikipedia.org/wiki/TRS-80 "wikilink") Model II、[バロース](https://ja.wikipedia.org/wiki/バロース "wikilink") B-20、[日本IBMの](../Page/日本アイ・ビー・エム.md "wikilink")[マルチステーション5550](https://ja.wikipedia.org/wiki/マルチステーション5550 "wikilink")といった[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")、[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")にも移植された。

[Macintosh](../Page/Macintosh.md "wikilink")向けのMultiplanは、マイクロソフト初の[GUI式表計算ソフトであった](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")（他機種版はテキストベース）。

表計算のマルチプラン (Multiplan)、グラフのマルチチャート（[Multi-Chart](https://ja.wikipedia.org/wiki/Multi-Chart "wikilink")、機種や販売元によってはMS-チャート）、簡易データベースのマルチファイル（[Multi-File](https://ja.wikipedia.org/wiki/Multi-File "wikilink")、機種や販売元によっては存在しない）の3種類でマルチツールファミリー (Multi-Tool Family) を構成した。

## 特徴

セル位置の指定はR1C1参照形式（行をR1, R2, R3…、桁をC1, C2, C3…で表す）が採用された。[8ビット](https://ja.wikipedia.org/wiki/8ビット "wikilink")パーソナルコンピュータでベストセラーとなった[VisiCalc](../Page/VisiCalc.md "wikilink")や、MS-DOS用としてベストセラーとなった[Lotus 1-2-3はA](../Page/Lotus_1-2-3.md "wikilink")1参照形式（行を1, 2, 3…、桁をA, B, C…で表す）であり、[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")はそれを「戦艦方式」と称して嫌っていたためにこの方式が採用された。しかし利用者の多くはA1参照形式に慣れており、R1C1参照形式は判りづらいと評された。そのため、後継ソフトである[Microsoft Excelでは初期状態がA](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")1参照形式となり、利用者が好みに応じてR1C1参照形式に切り替えることができるようになった。

[ファイル形式は](../Page/ファイルフォーマット.md "wikilink")[テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")の\[2\]\[3\]で、当時は多くのツールが当形式をサポートしていた。

VisiCalcやLotus 1-2-3では“/”（スラッシュ）を押すことによってメニューが表示されてコマンド入力モードになるが、Multiplanでは画面下部に常時メニューが表示されている。設定によって常時文字・数字・数式入力モードになり、[Escキー](https://ja.wikipedia.org/wiki/Escキー "wikilink")を押すことでメニューを呼び出すようにすることもできるバージョンもある。どのキーがどの編集コマンドに対応するかはコマンドメニューに表示されており、対応するアルファベットのキーを押すことでコマンドを選択する。

初版のバージョン1.0はIBMの要望に基づき、[IBM PCの標準的な](https://ja.wikipedia.org/wiki/IBM_PC "wikilink")[メモリである](../Page/Random_Access_Memory.md "wikilink")64[KBでも動作するよう作られた](https://ja.wikipedia.org/wiki/キロバイト "wikilink")。ワークシートのサイズは256行×64桁。バージョン1.1ではメモリの上限までワークシートを拡張できる。

バージョン2.0はマウス対応となった。

バージョン3.0はマルチユーザーに対応し、最大8枚のワークシートを扱えるようになった。

## 歴史

開発が始められたのは[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")。開発中のコードネームは**“EP”（エレクトロニック・ペーパー）**。先行していた同カテゴリーの表計算ソフト[VisiCalc](../Page/VisiCalc.md "wikilink")は[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書かれており、移植が困難という欠点があった。Multiplanはより多くの機種に移植できるよう、多様な環境への対応が容易な[C言語](../Page/C言語.md "wikilink")を使った。さらに[中間言語も利用し](https://ja.wikipedia.org/wiki/pコードマシン "wikilink")、移植時に変更点が少なくて済む設計となっていた。ただし、この特徴が動作を遅くする結果にもつながった。

開発責任者は[チャールズ・シモニー](https://ja.wikipedia.org/wiki/チャールズ・シモニー "wikilink")。かつて[ゼロックス](../Page/ゼロックス.md "wikilink")の[パロアルト研究所](https://ja.wikipedia.org/wiki/パロアルト研究所 "wikilink")で働いていたシモニーは、[Alto](../Page/Alto.md "wikilink")で採用されていたGUIの使い勝手の良さを知っており、またAlto上で動作するBravoという[ワードプロセッサを開発した経験もあり](../Page/ワープロソフト.md "wikilink")、その利点を取り入れるべくインターフェイスをデザインした。常時表示されるメニューやプロパティシートは、マウスによる操作を想定したものである。Altoの存在を知っていたビル・ゲイツもその思想に賛同していた。\[4\]

1982年に販売開始された当初の売れ行きは好調だったが、翌年にLotus 1-2-3が販売開始されると、[IBM PC/ATおよびその](https://ja.wikipedia.org/wiki/PC/AT "wikilink")[互換機用アプリケーション市場においては苦戦を強いられた](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")。1-2-3はMultiplanよりも多くのメモリを必要としたが、C言語で書かれたものよりも高速に動作するアセンブリ言語で書かれていた。Multiplanはバージョンアップのたびに機能を強化して1-2-3を追撃しようとしたが、すでに1-2-3は利用者の絶大な信頼を得ており、その牙城を崩すことはできなかった。\[5\]ただし、1-2-3の他言語対応が遅れたこともあり、[欧州や](../Page/ヨーロッパ.md "wikilink")[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の市場では比較的善戦した。これは、移植性が高くローカライズが容易であったこと、8ビット機等マシンパワーの低い環境でも動作したことが大きい。なお日本の8ビットパソコン向けには、[8080](https://ja.wikipedia.org/wiki/8080 "wikilink")/[Z80](../Page/Z80.md "wikilink")向け[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")クローンでありMS-DOSのファイルシステムと互換性のある[MSX-DOS](../Page/MSX-DOS.md "wikilink")のサブセットがバンドルされていた。

Macintosh版は初代機（[Macintosh 128K](https://ja.wikipedia.org/wiki/Macintosh_128K "wikilink")）の発売日1984年1月24日と同時に出荷された\[6\]、サードパーティー製としては唯一のアプリケーションソフトウェアであった（プログラミング言語である[Microsoft BASICも同時出荷](https://ja.wikipedia.org/wiki/Microsoft_BASIC "wikilink")）。アップルよりMacintoshの開発段階から移植を依頼され、発売前から開発環境が整えられていた為にそれが可能だった。基本となる部分のプログラムはコンバーターを通して変換でき、また当初よりマウス操作を考慮したデザインであったことからGUI対応も容易であった。アップルおよびロータス・デベロップメントが力を入れていた[Lotus Jazzは市場に受け入れられず](https://ja.wikipedia.org/wiki/Lotus_Jazz "wikilink")、初期のMacintosh市場においてはMultiplanが標準的な表計算ソフトの地位を確保した。

しかし、マイクロソフトにおいては、最重要拠点である北米市場において[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となったIBM PC/ATおよびその互換機市場で1-2-3との競争に敗れたことを問題視していた。マイクロソフトは、後にGUIに特化した表計算ソフトとしてMicrosoft Excelを生み出すこととなった（Macintosh版は[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")、[Windows版は](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")）。

[right](https://ja.wikipedia.org/wiki/ファイル:Multiplan.jpg "wikilink")。[表計算ソフト](../Page/表計算ソフト.md "wikilink")を意味する語として現在一般的な“Spreadsheet”（スプレッドシート）ではなく、“Electronic Worksheet Program”と記載されている。\]\]

## バージョン履歴

マイクロソフト（日本法人）発売分のみを挙げている。

  - 1986年2月：Multiplan 2.0（[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")、[J-3100シリーズ](https://ja.wikipedia.org/wiki/J-3100シリーズ "wikilink")）
  - 1987年7月：Multiplan 3.1（PC-9800シリーズ、J-3100シリーズ、[AX](../Page/AX.md "wikilink")シリーズ）
  - 1989年11月：Multiplan 4.1（PC-9800シリーズ、J-3100シリーズ、AXシリーズ）

## 参考文献

  - ダニエル・イクビア、スーザン・L・ネッパー、訳：椋田直子『マイクロソフト —ソフトウェア帝国誕生の軌跡—』アスキー、1992年 ISBN 4-7561-0118-6
  - 相田洋、大墻敦『新・電子立国 第3巻 世界を変えた実用ソフト』日本放送出版協会、1996年 ISBN 4-14-080273-1
  - 脇英世『ビル・ゲイツの野望 マイクロソフトのマルチメディア戦略』講談社、1994年 ISBN 4-06-207261-0
  - ジェームズ・ウォレス、ジム・エリクソン、監訳：奥野卓司、訳：SE編集部『ビル・ゲイツ -巨大ソフトウェア帝国を築いた男-』翔泳社、1995年 ISBN 4-88135-207-5
  - スティーブン・レヴィ、訳：武舎広幸『マッキントッシュ物語』翔泳社、1994年 ISBN 4-88135-085-4
  - 岩淵明男『マイクロソフト・ウィンドウズ戦略のすべて』ティビーエス・ブリタニカ、1993年 ISBN 4-484-93228-8

## 関連項目

  - [MULTI 16シリーズ](https://ja.wikipedia.org/wiki/MULTI_16シリーズ "wikilink") - 「MULTI」の名称は Multiplan に由来するともされる。

## 脚注

### 注釈

### 出典

[Category:表計算ソフト](https://ja.wikipedia.org/wiki/Category:表計算ソフト "wikilink") [Category:DOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:DOSのソフトウェア "wikilink") [Category:マイクロソフトのソフトウェア](https://ja.wikipedia.org/wiki/Category:マイクロソフトのソフトウェア "wikilink") [Category:1982年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1982年のソフトウェア "wikilink")

1.  Ichbiah, Knepper 1992, p. 184
2.
3.  日本語では「シルク」と読むことが多い。
4.  相田、大墻 1996, p. 101
5.  脇 1994, p. 137
6.  岩淵 1993, p. 127