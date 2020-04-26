> この記事は[Guru Meditation](https://ja.wikipedia.org/wiki/Guru_Meditation)から翻訳されています。


**Guru Meditation**（グル・メディテーション）とは、[コモドール](../Page/コモドール.md "wikilink")のパーソナルコンピュータ[Amiga](../Page/Amiga.md "wikilink")の初期のバージョンが[クラッシュしたときに表示されるエラーメッセージである](https://ja.wikipedia.org/wiki/クラッシュ_\(コンピュータ\) "wikilink")。これは、[Microsoft Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ブルースクリーン](../Page/ブルースクリーン.md "wikilink")やUnixの[カーネルパニック](https://ja.wikipedia.org/wiki/カーネルパニック "wikilink")に相当するものである。

その後、[Varnish Cache](https://ja.wikipedia.org/wiki/Varnish_Cache "wikilink")\[1\]や[VirtualBox](../Page/VirtualBox.md "wikilink")\[2\]などのソフトウェアでも、回復不可能なエラーのメッセージとして使用されるようになった。

## 概要

Guru Meditationが表示されたとき、ユーザが取ることのできる選択肢は、マウスの左ボタンを押して装置を[再起動](../Page/再起動.md "wikilink")するか、マウスの右ボタンを押してROMWackを起動するかである（ROMWackはオペレーティングシステムに組み込まれた最小限の[デバッガ](../Page/デバッガ.md "wikilink")で、9600bpsの端末を[シリアルポート](../Page/シリアルポート.md "wikilink")に接続することでアクセスできる）。

[Guru_meditation.gif](https://ja.wikipedia.org/wiki/File:Guru_meditation.gif "fig:Guru_meditation.gif") [GuruMeditationErrorinDSOrganize_01.jpg](https://ja.wikipedia.org/wiki/File:GuruMeditationErrorinDSOrganize_01.jpg "fig:GuruMeditationErrorinDSOrganize_01.jpg")

アラート自体は、画面の上部にある黒い長方形のボックスとして表示される。その境界線とテキストは、通常のGuru Meditationの場合は赤色、別の種類のGuru Meditationである回復可能なアラート(recoverable alert)の場合は緑色または黄色である。画面が真っ暗になり、アラートが表示される直前に電源LEDとディスクアクティビティLEDが点滅する場合がある。ROMにプログラムされたAmigaOS 1.x（Kickstart 1.1、1.2、1.3として知られる）では、エラーは常に赤である。AmigaOS 2.x、3.xでは回復可能なアラートは黄色で表示されるが、2.xの最初期のバージョンでは緑色だった。

システムに致命的な問題が発生したときにこのアラートが発生した。システムに回復の手段がない場合、システムに多数の重大な欠陥がある場合であっても、アラートは表示できる。極端な場合、システムのメモリが完全に枯渇した場合にアラートが表示されることもある。

エラーコードは、ピリオドで区切られた2つのフィールドとして表示される。その形式は、CPUエラーの場合は＃0000000x.yyyyyyyy、システムソフトウェアエラーの場合は＃aabbcccc.ddddddddである。1つ目のフィールドは、システムソフトウェアエラーの場合、発生した[MC68000](../Page/MC68000.md "wikilink")例外番号（CPUエラーが発生した場合）または内部エラー識別子（「メモリ不足」コードなど）のいずれかである。2つ目は、タスク構造体のアドレス、または割り当てもしくは割り当て解除に失敗したメモリブロックのアドレスである。エラーの原因となったコードのアドレスではない。クラッシュの原因が不明な場合、この番号は48454C50と表示される。これは、16進[ASCII](../Page/ASCII.md "wikilink")コードで「HELP」を表す（48 = H、45 = E、4C = L、50 = P）。

アラートメッセージのテキストは、ほとんどのユーザにとっては完全に不可解なものだった。技術的に熟達したAmigaユーザならば、例えば例外3はアドレスエラーであり、プログラムが境界のない境界上の単語にアクセスしていることがわかる。この専門知識を持たないユーザは、「グル」を探すか、単にマシンを再起動して今度は正しく動作することを期待する以外に手段はない。

### Guru Meditationハンドラ

バージョン2.04より前のAmigaOSには、Hypertek/Silicon Springs Development corp製のGOMF(Get Outta My Face)と呼ばれる市販のエラーハンドラがあった。それは多くの種類のエラーに対処することができ、ユーザに問題のプロセスと関連する画面を削除するか、マシンがGuru Meditationを表示できるようにするかの選択をユーザができるようにした。多くの場合、問題のあるプロセスを削除すると、データを保存し、システムを再起動する前に実行中のプログラムを終了することができる。エラーが広範囲ではない場合は、マシンを使用し続けることができた。ただし、このエラーが時々発生する可能性があるため、ユーザーを全てのエラーから救うことはできなかった。

### 回復可能なアラート

回復可能なアラート(Recoverable Alert)は、コンピュータシステムの重大ではないクラッシュである。通常の赤色のGuru Meditationは常に即座に再起動するが、ほとんどの場合、回復可能なアラートが発生しても、作業を再開してファイルを保存することができる。ただし、システムが予測不可能な状態になってデータ破損を引き起こす可能性があるため、回復可能なアラートが発生した後はできるだけ早く再起動した方が良い。

## 起源

"Guru Meditation"（[グル](../Page/グル.md "wikilink")の[瞑想](../Page/瞑想.md "wikilink")）という言葉は、初期のAmigaの社内でのジョークとして始まったものである。当時のAmigaにはという製品があった。これは、足で操作する[ジョイスティック](../Page/ジョイスティック.md "wikilink")のようなものであり、現代の[バランスWiiボード](../Page/バランスWiiボード.md "wikilink")に似ている。AmigaのOSの開発の初期に、同社の開発者はシステムの頻繁なクラッシュに非常に不満を抱いた。そこで、リラックスのために、ジョイボードを使って、インドの宗教家のように瞑想する（すなわち[座禅](https://ja.wikipedia.org/wiki/座禅 "wikilink")を組む）ゲームを開発した\[3\]。プレーヤーは、座って静止し続けなければならない。プレイヤーが動きすぎると、"guru meditation"エラーが発生した\[4\]。[Wii Fitのバランスゲームには](../Page/Wii_Fit.md "wikilink")、同様のゲームが収録されている。

## レガシー

  - [AmigaOS](../Page/AmigaOS.md "wikilink")バージョン4.0以降では、"Guru Meditation"が"Grim Reaper"に置き換えられたが、プロンプトボックスにGuru Meditation番号が簡単に記載されている。

  - [MorphOS](https://ja.wikipedia.org/wiki/MorphOS "wikilink")は、"Application Is *Meditating*"（アプリケーションは「瞑想中」です）というエラーメッセージを表示する。アプリケーションを閉じるとオペレーティングシステムが復活する場合があるが、再起動した方が良い。

  - [Varnish Cacheは](https://ja.wikipedia.org/wiki/Varnish_Cache "wikilink")、重大なエラーのときにGuru Meditationを表示する\[5\]。

  - [マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")の[ESP8266](https://ja.wikipedia.org/wiki/ESP8266 "wikilink")と[ESP32](https://ja.wikipedia.org/wiki/ESP32 "wikilink")では、[コアダンプ](../Page/コアダンプ.md "wikilink")やに"Guru Meditation Error: Core X panic'ed"（Xはクラッシュしたコアに応じて0または1）と表示する\[6\]。

  - [VirtualBox](../Page/VirtualBox.md "wikilink")では、仮想マシンモニターの重大なエラーを表すのに"Guru Meditation"という言葉を使用している。

  - では、エラー報告に"Sorry, that should not have happened. Guru Meditation."と表示される。

## 脚注

## 外部リンク

  - [Joyboard Controller](http://www.atariage.com/controller_page.html?SystemID=2600&ControllerID=11)

[Category:AmigaOS](https://ja.wikipedia.org/wiki/Category:AmigaOS "wikilink") [Category:Amiga](https://ja.wikipedia.org/wiki/Category:Amiga "wikilink") [Category:コンピュータのエラー](https://ja.wikipedia.org/wiki/Category:コンピュータのエラー "wikilink")

1.
2.
3.
4.
5.
6.