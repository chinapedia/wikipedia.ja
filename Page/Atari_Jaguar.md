> この記事は[Atari Jaguar](https://ja.wikipedia.org/wiki/Atari_Jaguar)から翻訳されています。


**Atari Jaguar**（アタリ ジャガー）とは、[アタリが](../Page/アタリ_\(企業\).md "wikilink")[1993年](../Page/1993年.md "wikilink")に発売した[家庭用ゲーム機](../Page/ゲーム機.md "wikilink")。

[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")では[1994年](../Page/1994年.md "wikilink")[12月8日](../Page/12月8日.md "wikilink")に発売された。全世界累計販売台数は推定で25万台と少なく、世界で3番目に売れなかったゲーム機である\[1\]。

## 概要

64ビットシステムバスを採用し、CPU（MPU）には[MC68000](../Page/MC68000.md "wikilink")が使われている。64ビットの能力を持ったグラフィックスカードを搭載した32ビットマシンとして、アメリカでは250ドル（約3万円）で発売された。

コントローラーは、方向キーとA・B・Cボタン（のちに6ボタンコントローラーも登場する）、Option、Pauseスイッチ（他機種でのSELECT、STARTに相当）、その下にテンキー様のボタンが12個付いている。テンキーにはゲームソフト付属のオーバーレイを被せ、補助的な操作を担う。コントローラの評価は高くなく、また本体との接続に利用された[D-sub端子が抜け落ちやすかった](../Page/D-subminiature.md "wikilink")。そのため、[IGN](https://ja.wikipedia.org/wiki/IGN "wikilink")が2006年に掲載した「最悪なゲームコントローラー TOP10」のトップに選ばれた。「ネズミが家のどこかで屁をしたら抜け落ちる」ともいわれた\[2\]。

ソフトウェアは、[ファミリーコンピュータ](https://ja.wikipedia.org/wiki/ファミリーコンピュータ "wikilink")や[メガドライブ](../Page/メガドライブ.md "wikilink")の[カートリッジとほぼ同じ大きさのカートリッジで供給された](../Page/ロムカセット.md "wikilink")。のちに後付けの[CD-ROM](../Page/CD-ROM.md "wikilink")ドライブも発売される（Atari Jaguar CD）。本体にVLM（Virtual Light Machine）というソフトが内蔵されている。TEMPEST2000の作者[Jeff Minterによるもので](https://ja.wikipedia.org/wiki/:en:Jeff_Minter "wikilink")、CD再生させながら連動してCDデータを映像変換して表示するという映像ドラッグソフトである。

## スペック

[thumb](https://ja.wikipedia.org/wiki/ファイル:Jaguar_Controller.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Jaguarcd.jpg "wikilink") ジャガーは3つのチップに都合5つのプロセッサを装備したマシンである。これらは全て並列に動作できる。

  - **CPU**
      - "Tom"（主に画像処理）, 25.59 MHz
          - [32ビット](../Page/32ビット.md "wikilink") [RISC](../Page/RISC.md "wikilink") [Graphics Processing Unit](../Page/Graphics_Processing_Unit.md "wikilink")（GPU）（\#1） - 4Kキャッシュ。実質的にはCPU扱いされる。
          - [64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink") Object processor（\#2） - プログラマブル。[スプライト処理](../Page/スプライト_\(映像技術\).md "wikilink")、ピクセル処理など、様々な画像処理ユニットとして振る舞える。
          - 64ビット [Blitter](https://ja.wikipedia.org/wiki/:en:Blitter "wikilink") processor（\#3） - [コプロセッサ](../Page/コプロセッサ.md "wikilink")。[zバッファ](https://ja.wikipedia.org/wiki/zバッファ "wikilink")と[グーローシェーディング](https://ja.wikipedia.org/wiki/グーローシェーディング "wikilink")をハードウェアサポートしている。
          - 64ビット [DRAM](../Page/Dynamic_Random_Access_Memory.md "wikilink") コントローラ
      - "Jerry" 26.6Mhz
          - 32ビット [RISC](../Page/RISC.md "wikilink") Digital Signal Processor（\#4） - 8kキャッシュ。GPUと同じもので汎用に振る舞える。
          - CD音質サウンド（[16ビット](../Page/16ビット.md "wikilink")ステレオ）
          - Wavetableシンセ、FMシンセ、 FMサンプリング、AMシンセ
          - クロック、タイマー、UART制御
          - ジョイスティック制御
      - [モトローラ](../Page/モトローラ.md "wikilink") [68000](../Page/MC68000.md "wikilink")（\#5）
          - 汎用用途 13.295MHz
  - *その他*
      - メインメモリ: 2メガバイト[DRAM](../Page/Dynamic_Random_Access_Memory.md "wikilink")
      - カートリッジROM 最大6メガバイト
      - ComLynx [I/Oをサポート](../Page/入出力.md "wikilink")

いずれのプロセッサもDRAMへのアクセス機能を持ち、DSP、GPUについては直接メモリ上のコードを実行できる。

他のゲーム機とは異なり、Jaguarの設計ではどれが正式なCPUという判断は付けにくい。68000は汎用用途となっているが、起動後はGPU・DSPともに汎用に使えるため、メインCPU基準で見るなら16ビット機、32ビット機、64ビット機、いずれの見方も可能である。

ただ、Object ProcessorとBlitterについては完全に64ビットで、その意味では「Jaguarは64ビット機」という表現は適切となる。汎用に使えるレジスタは、GPU・DSPの32ビット幅が最大なので「64ビットは単なるグラフィックス処理機能で実質32ビット機」という表現もまた正しい。基本的にはメモリアクセスの速度を稼ぐために、システムバス及び直結する演算用プロセッサを64ビットとし、制御系は32ビットでよいという設計方針である。

アタリはあくまでも「64Bits System」であるとし、「64Bits CPU」という表現は使っていない。

## Jaguar VR

ヘッドトラッキングによる十分な没入感を実現しており、Atariの名作ゲームを3D化してリリースする予定だったJaguar VRが[Virtuality](https://ja.wikipedia.org/wiki/Virtuality "wikilink")社と提携してJaguar向けのヘッドセットとして開発されていたが、AtariがJaguarの販売に苦戦する内に経営状態が悪化して開発プロジェクトも中止された\[3\]。

## その他

日本では[Atari Lynx同様](../Page/Atari_Lynx.md "wikilink")、ムーミンが輸入代行を行ったが、ハード・ソフトともに取り扱っている店舗が[秋葉原](https://ja.wikipedia.org/wiki/秋葉原 "wikilink")やトイザらスなど、一部地域や一部店舗に限られたため、日本でのセールスは非常に少なかった。輸入代行の総代理店であった[メッセサンオー](../Page/メッセサンオー.md "wikilink")では3,000台しか売れなかったという\[4\]。アメリカ本国でも1995年の時点での本体販売台数は15万台ほどだったという。

Jaguarの生産が終了した後、Imagin Systemsという歯科用光学機器メーカーがJaguarのケーシング用成形板を購入し、Jaguarの形をした歯科用カメラを製造・販売した。カートリッジ端子はメモリの拡張スロットとして使用されていた。

これ以降、[アタリは](../Page/アタリ_\(企業\).md "wikilink")[2020年](../Page/2020年.md "wikilink")に[Atari VCSを発表できるようになるまでおよそ四半世紀に渡りハードウェア事業から撤退し](https://ja.wikipedia.org/wiki/Atari_VCS "wikilink")、ブランドの身売りをするなど迷走状態が続いた。

## 脚注

## 関連項目

  - [Atari Lynx](../Page/Atari_Lynx.md "wikilink") - 前世代(又は同世代)機。
  - [Atari VCS (2018年のゲーム機)](https://ja.wikipedia.org/wiki/Atari_VCS_\(2018年のゲーム機\) "wikilink") - 次世代機。本機発売後に27年ぶりに、2020年初頭のハードウェア事業に再参入するマシンであるとしている。
  - [レイマン](../Page/レイマン.md "wikilink") - [ユービーアイソフト](../Page/ユービーアイソフト.md "wikilink")のゲーム、およびマスコット。元々はAtari Jaguar独占タイトルとしてリリースされた。
  - [東京エンカウント](https://ja.wikipedia.org/wiki/東京エンカウント "wikilink") - [AT-X](https://ja.wikipedia.org/wiki/AT-X "wikilink")にて過去に放映されていたテレビ番組。メインMC2人がゲームをプレイする部屋に背景として実機または箱に入った状態で展示されていた。番組中で起動された事はない。

## 外部リンク

  - [アタリ公式サイト](https://atari.com/)
  - [周辺機器情報](http://www.atariage.com/Jaguar/archives/hardware/index.html)（英文）

[Category:ゲーム機](https://ja.wikipedia.org/wiki/Category:ゲーム機 "wikilink") [Category:1993年のコンピュータゲーム](https://ja.wikipedia.org/wiki/Category:1993年のコンピュータゲーム "wikilink") [Category:アタリ](https://ja.wikipedia.org/wiki/Category:アタリ "wikilink") [Category:1990年代の玩具](https://ja.wikipedia.org/wiki/Category:1990年代の玩具 "wikilink")

1.
2.  [最悪なゲームコントローラー TOP10 GameSpark - 国内・海外ゲーム情報サイト](http://www.gamespark.jp/article/2007/07/28/13178.html)
3.
4.  『洋ゲー通信 Airport51』([須田剛一](../Page/須田剛一.md "wikilink") マスク・ド・UH著　[エンターブレイン](https://ja.wikipedia.org/wiki/エンターブレイン "wikilink")発行)148p