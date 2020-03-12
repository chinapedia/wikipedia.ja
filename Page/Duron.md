> この記事は[Duron](https://ja.wikipedia.org/wiki/Duron)から翻訳されています。


**AMD Duron** （デュロン）は、[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[32ビット](../Page/32ビット.md "wikilink")・[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")と[機械語](../Page/機械語.md "wikilink")レベルでの互換性を持つ。

## 概要

**Duron**は同社の[Athlon](../Page/Athlon.md "wikilink")に対しての廉価版で、低価格帯[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") (PC) への採用目的にインテル社の[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")の対抗製品という位置付けで発売された。DuronはAthlonよりも性能が抑えられたCPUであるものの商品価格の設定は競合するCeleronより費用対効果が優れたものになるようにされており、Athlon相当程度の性能を必要としない主に企業事務向け及び一部の個人向けの各低価格系PCに採用され、費用対効果を重視する一般消費者にも支持された。

Athlonとの差別化を図り製造原価を抑える為にL2[キャッシュ容量を](../Page/キャッシュメモリ.md "wikilink")64KBに削減されている。64KBはL1キャッシュの128KBの半分量で、通常のキャッシュ構成ではL2キャッシュの内容が全てL1キャッシュに収まってしまう為にL2キャッシュが意味を成さない。そこでエクスクルーシブキャッシュ機能によってL1とL2キャッシュ内容が重複しないようになっており、実質容量L1とL2を総和した192KB相当の大きなものとなっている。その一方で命令セットはAthlonと同じく拡張命令セット「[Enhanced 3DNow\!](https://ja.wikipedia.org/wiki/Enhanced_3DNow! "wikilink")」と「3DNow\! Professional」も完全に対応しており、Athlonで使えるソフトウェアは性能はともかく全て利用できる。DuronのハードウェアインターフェースはThunderbirdコア以降のAthlon、Athlon XPと同じ[Socket A](https://ja.wikipedia.org/wiki/Socket_A "wikilink") (Socket 462) で、Athlon用のSocket Aを実装した[マザーボード](../Page/マザーボード.md "wikilink")に装着することができる。そのためDuron専用マザーボードは存在しない。高度な性能を除きAthlonに引けをとることが無く、極端に高い演算性能を求めるような特殊用途を除いて満足できる性能を持っていた。

## デスクトップ向けDuronの世代毎の概要

### Spitfire（スピットファイア）

[2000年](../Page/2000年.md "wikilink")[6月](../Page/6月.md "wikilink")、ThunderbirdコアのAthlonをベースとした"Spitfire"コアを採用した第一世代のDuronが発表される。その名前は同名の[戦闘機に由来する](../Page/スーパーマリン_スピットファイア.md "wikilink")。対応するFSBクロックは200MHz。[プロセスルール](https://ja.wikipedia.org/wiki/プロセスルール "wikilink")は0.18μm。

  - ラインナップ：600MHz , 650MHz , 700MHz , 750MHz , 800MHz , 850MHz , 900MHz , 950MHz

### Camaro（カマロ）

Spitfireにより性能を高める改良を加えた製品として開発されていた。しかし[自動車メーカーから](../Page/ゼネラルモーターズ.md "wikilink")[商標権](https://ja.wikipedia.org/wiki/商標権 "wikilink")の侵害のクレームにより、Morganに改称され計画は続行された。AMDはドイツの[ドレスデン](../Page/ドレスデン.md "wikilink")州に新工場を竣工したが、地域感情に配慮しそれまでのSpitfireなどの第2次世界大戦の連合国軍側の戦闘機の名称を使うのをやめ、自動車の名称を使用することにしたものである。

### Morgan（モーガン）

[2001年](../Page/2001年.md "wikilink")[8月](../Page/8月.md "wikilink")、"Morgan"コアを採用した第二世代のDuronが発表される。PalominoコアのAthlonを基本設計としてL2キャッシュそのものを削減した製品である。しかし初期の製品はAthlon 4のPalominoコアを流用しL2キャッシュを細工して減らしてあるとDuronブランドの発表会で述べている。この世代から3DNow\! Professionalに対応している。名前の由来は[自動車ではなく馬の品種である](../Page/モーガン_\(自動車\).md "wikilink")。しばしば戦闘機および自動車の名前の由来となった馬の品種を用いることで、商標権の問題を避けやすくなる。FSBクロックは200MHz、[プロセスルール](https://ja.wikipedia.org/wiki/プロセスルール "wikilink")はSpitfireと同じく0.18μm。

  - ラインナップ：900MHz , 950MHz , 1.0GHz , 1.1GHz , 1.2GHz , 1.3GHz

### Appaloosa（アパルーサ）

Palominoの[プロセスルール](https://ja.wikipedia.org/wiki/プロセスルール "wikilink")を0.13μm化したThoroughbredコアのAthlonをベースとした第三世代のDuronの発売がアナウンスされた。しかし[2002年](../Page/2002年.md "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")以来Morganコアの新製品も発売されず、AMDのCPUロードマップではDuronブランド自体がフェードアウトと記述されてしまっていた。Duronの上位CPUであるAthlon XP自身が[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")までカバーしてしまっている当時の市場状況から、Duronに入り込む余地が市場には無く計画中止になった。このAppaloosaも馬の品種に由来する。

  - ラインナップ：未発売

### Applebred（アップルブレッド）

[thumb](https://ja.wikipedia.org/wiki/ファイル:Duron_1600_Applebred_model_A_Front.jpg "wikilink") [2003年](../Page/2003年.md "wikilink")[8月](../Page/8月.md "wikilink")頃、再びApplebredコアの発売がアナウンスされ、再び新製品の発表が行われた。ApplebredはAppaloosaと違いDuron専用のではないものの性能機能ともにAppaloosaと仕様的には同等のものである。販売不振の不良在庫となっていたThoroughbredコアのAthlon XPの在庫整理としてL2キャッシュの一部を動作しないようAppaloosa相当に加工し、[発展途上国向けに特別価格で出荷された製品である](../Page/開発途上国.md "wikilink")。その為に日本国内では、大手メーカー製のPCは採用されず、部品として並行輸入品が僅かに出回るに留まった。Applebredの名称は、BartonからThoroughbred相当を製造したThortonの例からAppaloosaとThoroughbredからの造語と考えられている。一部ではApplebredをもじって「apple bread」の和訳である「[りんご](https://ja.wikipedia.org/wiki/りんご "wikilink")[パン](../Page/パン.md "wikilink")」の愛称で呼ばれた。FSBクロックは266MHz。[プロセスルール](https://ja.wikipedia.org/wiki/プロセスルール "wikilink")は0.13μm。また、「L2キャッシュの一部を動作しないようAppaloosa相当に加工」という素性を利用し、CPU上の切断されている部分を鉛筆やコンダクタペンを用いて通電させ、（Duronより高額で高性能の）Athlon XP（Thoroughbred）として認識・動作させる加工が流行した。Athlon XP（Thoroughbred）、特に1.46GHz (1700+)は日本では「苺皿」と呼ばれて愛好されたため、苺皿が入手できなかった場合にDuronを鉛筆加工して代用とする場合があった。後期の倍率固定の出荷品にはこの加工が無効のものがあった。

  - ラインナップ：1.4GHz、1.6GHz、1.8GHz

## モバイルDuronの世代毎の概要

[ノートPC用向けとして](../Page/ノートパソコン.md "wikilink")、モバイルAthlon 4やモバイルAthlon XPと同様に電源管理技術の"Power Now\!"を採用し、低電圧化、低消費電力化を実現したDuron。SpitfireコアとMorganコアの製品が出荷された。

### Spitfire

  - ラインナップ：600MHz , 700MHz , 800MHz

### Morgan

  - ラインナップ：800MHz , 850MHz , 900MHz , 950MHz , 1.0GHz , 1.1GHz , 1.2GHz

## Duronのその後

後継ブランドとして[Sempron](../Page/Sempron.md "wikilink")が発売されたことで、Duronブランドは幕を閉じた。Athlon XPとも違うCeleronに見劣りの無いモデルナンバーを新たに採用する為に、連続性を断ち切ることが目的だったと言われている。

## 関連項目

  - [アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")
  - [Athlon](../Page/Athlon.md "wikilink")
  - [Sempron](../Page/Sempron.md "wikilink") - Duronの後継CPU名称。
  - [Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")

## 外部リンク

  - [Advanced Micro Devices, Inc. - AMD Home Page](http://www.amd.com/jp-ja/)

[Category:AMDのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:AMDのマイクロプロセッサ "wikilink")