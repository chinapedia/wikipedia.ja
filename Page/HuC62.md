> この記事は[HuC62](https://ja.wikipedia.org/wiki/HuC62)から翻訳されています。


**HuC62**は、株式会社[ハドソン](../Page/ハドソン.md "wikilink")がゲーム機などの用途向けに設計し、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink")に発表したCPUと周辺LSIのチップセットである。正式名称はC62システム。[日本電気ホームエレクトロニクス](../Page/日本電気ホームエレクトロニクス.md "wikilink")より発売された[PCエンジン](../Page/PCエンジン.md "wikilink")や[PC-FX](../Page/PC-FX.md "wikilink")に採用されていた。製造は多くは[セイコーエプソン](../Page/セイコーエプソン.md "wikilink")が担当している。

  - 名前の由来はハドソン社長であった工藤裕司が趣味としていた[蒸気機関車](../Page/蒸気機関車.md "wikilink")、通称シロクニと呼ばれた"[C62](../Page/国鉄C62形蒸気機関車.md "wikilink")"による。命名の理由は[ハドソン\#社長の趣味と企業風土](https://ja.wikipedia.org/wiki/ハドソン#社長の趣味と企業風土 "wikilink")の項目を参照。

## HuC62システム チップセット一覧

  - HuC6201
      - 天の声2などに搭載されている外部メモリ制御チップ。[シャープ](../Page/シャープ.md "wikilink")製。
  - HuC6202：VPC (Video Priority Controller)[thumb](https://ja.wikipedia.org/wiki/ファイル:HuC6202_01.jpg "wikilink")
      - SUPER GRAFXに搭載されているチップ、二つのVDCから送られてくるビデオデータ信号を合成しVCEへ出力する。
      - CPUのST0、ST1、ST2命令実行時、どちらのVDCに送るか設定する機能を持つ。
  - HuC6230：音源チップ、HuC6280のPSG部に[ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink")を追加した物。[thumb](https://ja.wikipedia.org/wiki/ファイル:HuC6230_01A.jpg "wikilink")
  - HuC6260：VCE (Video Color Encoder)[thumb](https://ja.wikipedia.org/wiki/ファイル:HuC6260A_01.jpg "wikilink")
      - VDCのビデオデータ出力ポートから出力されたデータを元に、VCE内のカラーパレットとつき合わせてD/Aコンバートし、アナログRGB信号及び映像色信号を出力する。VDCとVPCへドットクロック信号、水平同期信号、垂直同期信号の供給も行っている。
          - 同期信号発生回路内蔵
          - RGB8段階計512色発色
          - RGBカラー帯域 7MHz
          - カラーパレットはデータバスからREAD/WRITE可能
          - 製造プロセス [CMOS](../Page/CMOS.md "wikilink")
          - 電源電圧 +5V
          - 80ピン[QFP](https://ja.wikipedia.org/wiki/QFP "wikilink")
  - HuC6261：ビデオ管理機能を持つ。HuC6260の次世代チップにあたる。[thumb](https://ja.wikipedia.org/wiki/ファイル:HuC6261_01A.jpg "wikilink")
  - HuC6270：VDC (Video Display Controller)[thumb](https://ja.wikipedia.org/wiki/ファイル:HuC6270A_01.jpg "wikilink")
      - VCEからのドットクロック信号に同調して[スプライトと背景](../Page/スプライト_\(映像技術\).md "wikilink") (Backbound) を重ね合わせて合成し、9ビットビデオデータとして出力する。VDCの出力するビデオデータはパレット情報、カラーインデックス情報、スプライト背景情報で構成され、それ自体は色情報にはなっていない。
          - 外部同期可能な同期信号発生回路（PCエンジンでは外部同期）
          - バックグラウンドカラーのパターンサイズは8×8ドット、色指定256色中16色
          - スプライトサイズは16×16ドット、色指定256色中16色
          - デジタルカラー映像信号 9ビット並列[TTLコンパチブル](../Page/Transistor-transistor_logic.md "wikilink")
          - DMA機能 CPU-VRAM間、VRAM-VRAM間、VDC内のSATB (Sprite Attribute Table Buffer) - VRAM間の転送
          - CPU接続用2ビットアドレスバス
          - CPU接続用16ビットデータバス
          - VRAM接続用16ビットアドレスバス
          - VRAM接続用16ビットデータバス
          - VRAM制御機能。
              - 製造プロセス CMOS
              - 電源電圧 +5V
              - 80ピンQFP
  - HuC6271：Motion JPEGデコーダ[thumb](https://ja.wikipedia.org/wiki/ファイル:HuC6271_02.jpg "wikilink")
  - HuC6272：メモリコントローラ[thumb](https://ja.wikipedia.org/wiki/ファイル:HuC6272_01A.jpg "wikilink")
  - HuC6273：3D表示用チップ[thumb](https://ja.wikipedia.org/wiki/ファイル:HuC6273_01A.jpg "wikilink") [PC-FXGA](../Page/PC-FXGA.md "wikilink")に搭載されている。[クボタ](../Page/クボタ.md "wikilink")コンプスとの共同開発。
  - HuC6280：[6502](../Page/MOS_6502.md "wikilink")[CPU](../Page/CPU.md "wikilink")をカスタマイズしたもの。[波形メモリ音源も含まれる](https://ja.wikipedia.org/wiki/波形メモリ音源#PCエンジン音源の特徴 "wikilink")。[thumb](https://ja.wikipedia.org/wiki/ファイル:HuC6280A_01.jpg "wikilink")
      - CPU部
          - 65C02を元に独自に命令を変更 / 拡張している。ADC命令にBCD機能を付加、ストア命令をHuC6270へのストアに変更など。
      - 音源部
          - メロディ6チャンネルまたはメロディ4チャンネル+ノイズ2音
          - 音量設定 5ビット[対数](../Page/対数.md "wikilink")変換方式
          - メイン音量制御レジスタ内蔵
          - 1周期32アドレス[波形メモリ方式](../Page/波形メモリ音源.md "wikilink")
          - [LFO内蔵](../Page/LFO_\(電子楽器\).md "wikilink")
          - 製造プロセス CMOS
          - 電源電圧 +5V
          - 80ピンQFP

## 参考資料

  - PC Engineユーザー開発システム でべろスターターキット アセンブラ編 - 徳間書店インターメディア（株）発行、1996

## 関連項目

  - [PCエンジン](../Page/PCエンジン.md "wikilink")
  - [PC-FX](../Page/PC-FX.md "wikilink")
  - [PC-FXGA](../Page/PC-FXGA.md "wikilink")
  - [国鉄C62形蒸気機関車](../Page/国鉄C62形蒸気機関車.md "wikilink")- 名称の由来

[Category:PCエンジン](https://ja.wikipedia.org/wiki/Category:PCエンジン "wikilink") [Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink") [Category:セイコー](https://ja.wikipedia.org/wiki/Category:セイコー "wikilink") [Category:ハドソン](https://ja.wikipedia.org/wiki/Category:ハドソン "wikilink")