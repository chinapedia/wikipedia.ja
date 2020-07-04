> この記事は[FM-7](https://ja.wikipedia.org/wiki/FM-7)から翻訳されています。


**FM-7**（エフ・エム・セブン）は[富士通](../Page/富士通.md "wikilink")が発売した8[ビット](../Page/ビット.md "wikilink")[パソコンであり](../Page/パーソナルコンピュータ.md "wikilink")、正式名称はFUJITSU MICRO 7。富士通はこのFM-7のヒットにより、[シャープ](../Page/シャープ.md "wikilink")、[NECと共に](../Page/日本電気.md "wikilink")[パソコン御三家](https://ja.wikipedia.org/wiki/パソコン御三家 "wikilink")と呼ばれる様になる。

## FM-7

FM-7は[1982年](../Page/1982年.md "wikilink")11月、[FM-8](../Page/FM-8.md "wikilink")の[廉価版](../Page/廉価版.md "wikilink")後継機種として発売された。開発時の名称はFM-8Jr.（ジュニア）。FM-8と一定の[互換性](../Page/互換性.md "wikilink")があり、[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")、[OS](../Page/オペレーティングシステム.md "wikilink")（[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")、[FLEX](https://ja.wikipedia.org/wiki/:en:FLEX_\(operating_system\) "wikilink")、[UCSD Pascal](../Page/UCSD_Pascal.md "wikilink")、[OS-9](../Page/OS-9.md "wikilink")）、開発言語、ツール、周辺機器の資産継承が考慮されていた。FM-8を含んで、FM-7/8シリーズと呼ばれ、CPUの高速化等、実質的にはFM-8の性能が向上した後継機にあたる。

モトローラ社のMPU [68B09をメインCPUとグラフィックを独立制御するディスプレイサブシステムへそれぞれ搭載する](../Page/MC6809.md "wikilink")2CPUのアーキテクチャを採用。FM-8と同様にオプションの[Z80](../Page/Z80.md "wikilink")カードが搭載可能になっており、[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")や、[Oh\!X](../Page/Oh!X.md "wikilink")で使われた[S-OS"SWORD"など](https://ja.wikipedia.org/wiki/Oh!X#S-OS "wikilink")、Z80CPUベースのシステムを動作させることも可能になっている。このZ80カード用スロットは後にユーザベースで63C09を搭載するのにも使われた。F-BASIC V3.0がROMに搭載されている。[漢字](../Page/漢字.md "wikilink")ROMカード、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")ドライブはオプション。

発売当初の[イメージキャラクター](https://ja.wikipedia.org/wiki/イメージキャラクター "wikilink")は[タモリ](https://ja.wikipedia.org/wiki/タモリ "wikilink")。キャッチコピーは「青少年は興奮する」。

競合機種と同等のカラー表示にPSGがつき価格が安かったことから、FM-7は一定の普及をみて、富士通をパソコン御三家の地位にまで押し上げた。FM-7に端を発する低価格・高性能という路線はPCユーザ拡大に貢献し、'80年代パソコン[ブームの原動力となった](../Page/流行.md "wikilink")。

FM-7が販売面で成功したのは本体価格が126,000円という低価格にも関わらず、当時の最新機能を盛り込み1クラス上のPCに匹敵または凌駕する性能を備えていたことにある。同時期の人気機種は、NEC [PC-8801](https://ja.wikipedia.org/wiki/PC-8801 "wikilink")（228,000円）、[PC-9801](https://ja.wikipedia.org/wiki/PC-9801 "wikilink")（298,000円）、日立 [ベーシックマスター](../Page/ベーシックマスター.md "wikilink")レベル3（298,000円、後に価格改定）。学生を中心に人気があった「パピコン」ことNEC [PC-6001](https://ja.wikipedia.org/wiki/PC-6001 "wikilink")（89,800円）や[コモドール](../Page/コモドール.md "wikilink")[VIC-1001](../Page/VIC-1001.md "wikilink")（69,800円）などの初心者PCのユーザー層にも大きな影響を与え、その成功から、FM-7を引き継ぐ形で、後継機が完全上位互換で作られていく形になる。

FM-8から引き続き、広いメモリ領域と[VRAM](../Page/VRAM.md "wikilink")領域の確保と処理速度向上のためにメイン（演算部）、サブ（グラフィック部）に独立した6809を搭載する贅沢なアーキテクチャを採用した。FM-8を祖とするこの設計は、マルチCPUとしてではなく、ホストCPUとグラフィック端末の関係にあり、サブCPUに処理の大きな表示周りの作業をさせることによるメインCPUの負担を軽減することに目的があった。また、このグラフィックスサブシステムの実装では、キャラクターコードをハードウェア的にフォントに展開するテキストVRAMを持たなかったため、ハードウェアによるスクロールが使えない画面モードでは、当時の処理速度と比較して広大なグラフィックVRAMを再描画する必要があり、リスト表示などでのスクロールのもたつきや、カーソルを移動するとその通り道にあったグラフィックも消えてしまうという制限も引き継いでいる。また、[リアルタイムゲームが流行すると両システム間の転送容量に制限やタイムラグがあったこと](../Page/アクションゲーム.md "wikilink")、キーボードのスキャンを専用CPUに任せ、チャタリング除去なども行っているためにBREAK以外のキーでは押下した結果しか認識できず、ユーザの間ではリアルタイムゲーム向きではないとされ、議論になった。前述のとおり、任意のコードの実行を想定して設計されているわけではないサブシステムではあったが、サブシステムモニタ開発時、デバッグ用に実装されたメンテナンスコマンドの利用や、そのノウハウの蓄積、後述する内部技術資料の積極的な公開により、サブシステムで任意のプログラムを実行することで、描画の高速化や、高速にデータを転送するテクニックなどが考案され、ハードウェア的なキー入力の制限を除けば、競合機種と同等のゲームが発売されるようになっていった。

他社と同様、富士通も本体添付品や別売マニュアルという形で[BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、I/Oアドレス、ファームウェア、システムコマンド等を積極的に公開した。また富士通の支援により、FMシリーズ専門誌『[Oh\!FM](../Page/Oh!FM.md "wikilink")』（[日本ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")、後の『Oh\!FM TOWNS』）をはじめとして、[技術評論社](../Page/技術評論社.md "wikilink")や[工学社](../Page/工学社.md "wikilink")などから『活用マニュアル』などと呼ばれる良質なリファレンスマニュアルが多く出版された。またショウルームやサポートセンター経由では、内部技術資料なども必要に応じて比較的簡単に入手できた。

回路設計の問題としては、同等の音源を搭載した他機種に比較して、サウンド出力にデジタル回路からリークしたノイズも多く、音割れも見られた。

1985年、スペインのSECOINSA社という富士通に近い会社より FM-7 が販売されている\[1\]\[2\]\[3\]。

### 従来機種との互換性

  - FM-8との主な共通点。

<!-- end list -->

  - [キーボード一体型筐体](../Page/キーボード_\(コンピュータ\).md "wikilink")。
  - メモリマップ、[I/Oマップ等の設計](../Page/入出力.md "wikilink")。
  - サブシステムに関する機能、設計。
      - メイン側とは128バイトの共有RAMを通じてコマンドやデータをやりとりする。
      - 表示画面（640×200ドット、8色。グラフィックスサブシステムによって、テキストもグラフィック画面へ描画される。）
          - ハードウェアで画面の2ライン単位での縦スクロール並びに、256ドット単位と実用的ではないが横スクロールも可能。
      - キースキャンに専用4ビットマイコンを使用したキーボード。

<!-- end list -->

  - FM-8との主な差異。

<!-- end list -->

  - MPUクロックの高速化（メイン1.2MHz→2MHz、サブ1MHz→2MHz）。
      - FM-8と同じ速度にするモードもある。
  - ソフトウェア制御可能なF-BASIC ROMとRAMの[バンク切替](https://ja.wikipedia.org/wiki/バンク切替 "wikilink")機能の追加。
      - これはFM-8でROM-BASIC以外のOSを利用するためにDIP-SWにてBASIC ROMを切り離し全メモリ領域をRAMとして利用するために用意されていた機構がソフトウェア制御にて可能になったもの。データレコーダからソフトウェアをロードする当時のシステムで32KB多くRAM領域を確保できることは非常に有効であり、FM-7専用ゲームソフトがFM-8で動作しない大きな原因の一つにもなった。
  - サウンド機能（PSG3声）、[カラーパレット機能](../Page/インデックスカラー.md "wikilink")、マルチページ機能の追加。
  - キーボードのメインCPU側からのBREAKキー以外のキーコード読み取り機能、メインCPU側へのキーボード及びタイマ割り込み機能を追加。
  - 拡張スロットを内蔵し、工具を使用せずにオプションカードの増設が可能。
      - 拡張スロット用カードとして、漢字ROMカード（JIS第一水準のみ搭載）、FDDインタフェースカード、RS-232Cカード、Z80 CPUカード、音声合成ボードなどが発売された。
  - 使用頻度の低い[RS-232](../Page/RS-232.md "wikilink")C、アナログ入力ポート、[バブルカセットホルダ等の機能を削除](../Page/磁気バブル.md "wikilink")。
      - プリンタポート（パラレルポート）に接続する[ジョイスティック](../Page/ジョイスティック.md "wikilink")がいくつかの[サードパーティー](../Page/サードパーティー.md "wikilink")から発売されていた。
      - ごく初期にはFM-8互換のアナログ入力ポートを増設して接続する[ジョイスティック](../Page/ジョイスティック.md "wikilink")も発売されていた。
      - 後にFM音源カードが富士通[純正](../Page/純正.md "wikilink")のオプションとして発売され、これには[ATARI仕様のジョイスティック端子も装備していた](https://ja.wikipedia.org/wiki/Atari_2600#コントローラ "wikilink")。
      - RS-232Cインタフェース+漢字ROM+辞書ROMを搭載した日本語通信カードも、FM77AVシリーズ末期の時代に純正オプションとして発売された。
  - キーボード専用マイコンの仕様改善。
  - 富士通から発売された[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")規格パソコンである[FM-X](../Page/FM-X.md "wikilink")と連携動作を可能とするインタフェイスボードが発売されていた。

### 基本仕様

  - FM-7

<!-- end list -->

  - [CPU](../Page/CPU.md "wikilink"): メイン [MBL68B09](../Page/MC6809.md "wikilink")（入力外部周波数4.9/8MHz切換機能付）、サブ MC6809（入力外部周波数4/8MHz切換機能付）
  - ROM: F-BASIC 32KB、ブートローダ 2KB、サブシステムモニタ 8KB、キャラクタ 2KB
  - RAM: メイン64KB（BASICでのフリーエリアは32KB）、コンソール処理用4KB\[4\]、[VRAM](../Page/VRAM.md "wikilink") 48KB
  - Text Mode: 80×20/25、40×20/25
  - Graphic Mode: 640×200モノクロ3プレーン若しくはカラー1プレーン。パレット機能付き。
  - Sound: PSG([AY-3-8910あるいはAY](https://ja.wikipedia.org/wiki/Programmable_Sound_Generator#AY-3-8910の仕様 "wikilink")-3-8913などの相当品); 入力クロックは 1.2288 MHz
  - 電源(消費電力): AC100V 50/60Hz(最大70W)
  - 使用条件: 温度 0〜35℃,湿度 20〜80%,(ただし結露しない事)

<!-- end list -->

  - 本体添付品

<!-- end list -->

  - 簡易言語 NEW VIPカセットテープ（表計算ソフト）
  - 簡易言語 NEW VIP操作マニュアル
  - FM-7 ユーザーズマニュアル システム解説書
  - FM-7 ユーザーズマニュアル システム仕様書
  - FM-7 F-BASIC 文法書
  - FM-7 F-BASIC ポケットブック
  - FMシリーズ F-BASIC入門

<!-- end list -->

  - オプション

<!-- end list -->

  - 本体内蔵オプション:
      - MB22405 漢字ROMカード（[JIS第一水準漢字ROM](https://ja.wikipedia.org/wiki/JIS_X_0208#漢字集合 "wikilink")）
      - MB22435 ひらがなROMカード
      - MB22407 [ミニフロッピィインタフェースカード](../Page/フロッピーディスク.md "wikilink")
      - MB28021 [Z80](../Page/Z80.md "wikilink")カード（5"版 CP/M-80とのセット）
      - MB22406 [RS-232C](https://ja.wikipedia.org/wiki/RS-232C "wikilink")カード
      - MB22436 [マウスセット](../Page/マウス_\(コンピュータ\).md "wikilink")
      - MB22437 音声合成カード
      - MB22459 [FM音源](../Page/FM音源.md "wikilink")カード（[YM2203](../Page/YM2203.md "wikilink")搭載）
      - FM77-101 日本語通信カード（[RS-232C](https://ja.wikipedia.org/wiki/RS-232C "wikilink")インタフェース、JIS第一水準漢字ROM、辞書ROMを搭載）
  - 外部オプション:
      - MB26002 I/O拡張ユニット
      - MB22439 [MIDI](../Page/MIDI.md "wikilink")アダプタ
      - FM-8用ミニフロッピィアダプタ。本体I/O拡張コネクタへ接続\[5\]。
  - 動作する主要OS:
      - [OS-9](../Page/OS-9.md "wikilink")/6809 Level 1
      - [FLEX](https://ja.wikipedia.org/wiki/:en:FLEX_\(operating_system\) "wikilink")
      - [CP/M-80](https://ja.wikipedia.org/wiki/CP/M-80 "wikilink")（Z80カード使用時）

### FM-7シリーズ

他のモデルのように実装機器による商品バリエーションは無いが、後期にリファインされた同等の機種が発売された。

  - FM-7 \[MB25010\]（[1982年](../Page/1982年.md "wikilink")11月発売）126,000円。

[thumb](https://ja.wikipedia.org/wiki/ファイル:FM-New7,_May_2013.jpg "wikilink")

  - FM-NEW7 \[MB25015\]（[1984年](../Page/1984年.md "wikilink")5月発売）99,800円。
      - FM-7の廉価モデル。ゲートアレイの利用により集積率を上げ、基板のサイズ、レイアウトは大幅に変更された他、ROM BASICなどでバグが修正されている等の違いはあるが機種としてはほぼ等価である。簡易言語 NEW VIPの添付がなくなった。初期ロットではフロッピィディスクのステップレートを変更できる新ブートROMを搭載していたが、いくつかの市販ソフトが動作しない問題があったためすぐにFM-7のブートROMに戻された。

## FM-77

**FM-77**（エフ・エム・セブン・セブン）は[1984年](../Page/1984年.md "wikilink")、FM-7後継機種としてFM-NEW7とともに発売された。[FM-11](../Page/FM-11.md "wikilink")と同様にキーボードを分離し、3.5インチ[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")ドライブ、[JIS第一水準漢字ROMを本体に内蔵したモデルである](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")。ディスク版F-BASIC V3.0L2.0と[FM Logoが付属した](../Page/LOGO.md "wikilink")。

キーボードはパラレルインターフェースで、コードは黄色い（D1/D2のみ。L2/L4は本体同色）カールコードとなっているが太い。本体色はオフホワイト。

本体の発熱量が高く、長時間使用し続けているとフロッピードライブに入れたディスクまで熱くなるという特徴があった。

拡張性がFM-7に比べ大きく向上し、[メモリ管理ユニット](../Page/メモリ管理ユニット.md "wikilink")（MMU）であるメモリ・マネージメント・レジスタ（MMR）を搭載してメイン側の[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")アドレス空間が256KiBに広がったほか、サブシステムが改良され、[サイクルスチール](https://ja.wikipedia.org/wiki/サイクルスチール "wikilink")によりVRAMアクセスのタイミングなどが向上し、表示が高速化された。ただし、MMR使用時にはMPUクロックが2MHzから1.6MHzに低下した。

専用オプションとして、400ラインセット、1MBフロッピィコントロールカード、スーパーインポーズユニットなども用意された。

400ラインセットは99,800円と大変高価であったため、後にRAM容量と日本語ワードプロセッサが削られた廉価版の400ラインセットIIが49,800円で用意された。

1MBフロッピィコントロールカードは当初F-BASIC V3.5とOS-9 Level II（OS-9 Level IIの起動にはRAMが最低128KB必要だが、400ラインカードはなくても可能）でしかサポートされていなかったが、後に400ラインセット不要で使用できるようにF-BASIC V3.1が用意された。

スーパーインポーズユニットは200ラインでしか使用できないため、400ラインセットとは排他的に使用する必要があった。

### 従来機種との互換性

FM-7とはほぼ完全上位互換であるが、MPUクロックをFM-8相当に落とす機能は削除されている。

ブートモードは従来機種のディップスイッチ方式からボタン式スイッチ方式に変更され、BOOT1、BOOT2、BASICの3種類から選択できる。 BOOT1スイッチは1MBフロッピィDOSモード、BOOT2スイッチは320KBフロッピィDOSモード、BASICスイッチはF-BASICモードになっており、FM-7/NEW7と比較して1MBフロッピィDOSモードが追加された。なお、FM-NEW7と異なり全ロットでフロッピィディスクのステップレートの変更はできない。

また、グラフィックモードスイッチで[サイクルスチール](https://ja.wikipedia.org/wiki/サイクルスチール "wikilink")のON/OFFが選択でき、OFF時にはFM-7/NEW7同等の描画速度となる。

内蔵オプションは互換スロットが用意されていたため、FM-7用の各種増設カードはほぼそのまま使用可能になっているが、ミニフロッピィディスクインタフェースカード、漢字ROMカード等、すでに実装済の機能と等価の一部周辺機器については利用できない（利用する必要がない）。

外部オプションはインタフェースコネクタが変更されたため同じケーブルでは接続できなくなったが、信号線は変更されなかったため、ケーブルさえ用意できればFM-7用の各種外部オプションは使用可能。

### 基本仕様

  - FM-77D1/D2

<!-- end list -->

  - CPU: メインMC6809(2MHz)、サブ[MBL68B09E](../Page/MC6809.md "wikilink")(2MHz)
  - ROM: F-BASIC 32KB、ブートローダ 4KB、サブシステムモニタ 8KB、キャラクタ 2KB、JIS第一水準漢字 128KB
  - RAM: メイン64KB（最大256KB）、サブ5KB、[VRAM](../Page/VRAM.md "wikilink") 48KB
  - [FDD](../Page/フロッピーディスク.md "wikilink"): 3.5"2D×2(D2),3.5"2D(D1)
  - OS: F-BASIC V3.0L2.0、FM Logo
  - Text Mode: 80×20/25、40×20/25
  - Graphic Mode: 640×200モノクロ3プレーン若しくはカラー1プレーン。パレット機能付き。
  - Sound: PSG([AY-3-8910](https://ja.wikipedia.org/wiki/Programmable_Sound_Generator#AY-3-8910の仕様 "wikilink"))
  - 電源(消費電力):AC100V 50/60Hz(最大100W)
  - 使用条件:温度 5〜35℃、湿度 20〜80%(ただし結露しない事)

<!-- end list -->

  - 本体添付品

<!-- end list -->

  - FM Logo（作図言語）
  - FM-77 77をつかおう
  - FM-77 ユーザーズマニュアル F-BASIC入門
  - FM-77 ユーザーズマニュアル ファームウェア解説
  - FM-77 ユーザーズマニュアル ハードウェア解説
  - FM-77 F-BASIC 文法書
  - FM-77 ディスクユーティリティ操作手引書
  - FMシリーズ FM Logo プログラミング入門
  - FMシリーズ FM Logo V2.0 リファレンスマニュアル

<!-- end list -->

  - 追加オプション（基本はFM-7に準ずる）

<!-- end list -->

  - 本体内蔵オプション:
      - MB28121 400ラインセット（400ラインカード、192KB [RAM](https://ja.wikipedia.org/wiki/RAM "wikilink")カード、F-BASIC V3.5、日本語[ワードプロセッサ](../Page/ワードプロセッサ.md "wikilink")FM-JWP/77 のセット）
      - MB28122 400ラインセットII（400ラインカード、64KB [RAM](https://ja.wikipedia.org/wiki/RAM "wikilink")カード、F-BASIC V3.5 のセット）
      - MB22454 1MBフロッピィコントロールカード
      - MB28021J Z80カード（3.5"版 CP/M-80とのセット）
  - 外部オプション:
      - MB22610 スーパーインポーズユニット
      - MB26002J I/O拡張ユニット（接続ケーブルがFM-7と異なる）
      - MB22439J MIDIアダプタ（接続ケーブルがFM-7と異なる）
  - 動作する主要OS:
      - F-BASIC V3.5（400ラインセット使用時）
      - [OS-9](../Page/OS-9.md "wikilink")/6809 Level 2（400ラインセット使用時）

### FM-77シリーズ

  - 初代（[1984年](../Page/1984年.md "wikilink")5月発売）カールコード黄色。
      - FM-77D1 \[MB25240\] FDD1基搭載。198,000円。
      - FM-77D2 \[MB25250\] FDD2基搭載。228,000円。1984年度グッドデザイン賞受賞\[6\]
  - 二代目 FDD2基搭載。カールコード白色。
      - FM-77L4 \[MB25260\]（[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")2月発売）400ラインセットII搭載。F-BASIC V3.5付属。238,000円。
      - FM-77L2 \[MB25255\]（[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")5月発売）[FM音源](../Page/FM音源.md "wikilink")カード搭載。193,000円。

## FM77AV

**FM77AV**はFM-7/FM-77シリーズの上位機種となるシリーズ。[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に初代機が発売され、[FM TOWNSシリーズの発売される直前の](../Page/FM_TOWNS.md "wikilink")[1988年](../Page/1988年.md "wikilink")秋までマイナーチェンジが繰り返された。初代FM77AVはメタリックダークグレーに近い色であるが、基本的に黒に近い色を基調としたデザインでシリーズは展開されている。イメージキャラは[南野陽子](https://ja.wikipedia.org/wiki/南野陽子 "wikilink")。

FM16βSD/FM16π等と同様、FM-7の系譜では本機より、正式な機種名からは「FM」と「77」との間のハイフンは無くなった。しかし、従来機種の流れから、ソフトウェアパッケージや、雑誌記事、Webの記述などでは、ハイフンを入れて記述されることも多く見られる。

従来の640ドット×200ライン8色が2画面持てるようになったほか、320ドット×200ライン4096色という当時では画期的な色数の同時発色を可能とし、キャッチコピーではカラー化した映画などで使われた語である「総天然色」にかけて「総、天、然、ショック。」とうたった。セットの専用[モニターは](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")[テレビ](../Page/テレビ.md "wikilink")[チューナー](https://ja.wikipedia.org/wiki/チューナー "wikilink")内蔵で、単体でも[テレビ放送が受信可能で](../Page/NTSC.md "wikilink")[ビデオ入力端子も装備](../Page/コンポジット映像信号.md "wikilink")（[スピーカー](../Page/スピーカー.md "wikilink")は[モノラル](https://ja.wikipedia.org/wiki/モノラル "wikilink")）。

AV40シリーズでは全てのピクセルに対し26万色から任意の色を表示できるようになっているが、選択可能な色数が画素数を上回ったため、広告から同時発色の記述はなくなっている。

オプションのビデオディジタイズカード(現在でいうビデオキャプチャカード)増設で専用テレビを通じて[テレビ](../Page/テレビ.md "wikilink")放送・[ビデオ入力などからの画像取り込みもできた](../Page/ビデオ信号記録装置.md "wikilink")。

4096色モードではパレットの割り当てにより、重ね合わせ付きの64色2画面・16色3画面・8色4画面・単色12画面モードなどにすることができた。また、VRAMのオフセット指定による横8ドット/縦1ドットごとのハードウェアスクロール機能があり、オフセットは2画面別々に設定できた。このため、[家庭用ゲーム機](https://ja.wikipedia.org/wiki/家庭用ゲーム機 "wikilink")並みの[ゲーム](../Page/ゲーム.md "wikilink")画面も実現可能だった。アナログRGBディスプレイのコネクタおよびケーブルは[EIAJ](https://ja.wikipedia.org/wiki/EIAJ "wikilink")規格の[RGB21ピン](../Page/RGB21ピン.md "wikilink")のクロスケーブルが使われた。

また、サブシステム側MPUを停止することにより、メインMPUからVRAMなどサブシステム側の資源に直接アクセスすることが可能になったほか、新サブシステムの機能としてハードウェアによる直線補間・論理演算機能付きのLINEコマンドやPAINTコマンドなどを搭載した。FM-8/7/77では1ドット単位で描画していたSYMBOLコマンドも直線補間機能を利用するようになり高速化している。キーボードは押下だけではなく開放も認識できるようになった。

キーボードは初代FM77AVでは電話の受話器と同じ4ピン[モジュラージャックを使用した細いカールコードによる接続](../Page/Registered_jack.md "wikilink")\[7\]で、初代FM77AVのキーボードは[赤外線](../Page/赤外線.md "wikilink")によるワイヤレス接続やnキーロールオーバーもサポートしていたが、これらの機能は後継機種ではコストダウンのため段階的に撤廃される。AV20/AV40では電話回線と同じ6ピンモジュラージャック、AV20EX/AV40EX/AV40SXは[S端子](../Page/S端子.md "wikilink")と同形状の4ピン[ミニDINコネクタ](https://ja.wikipedia.org/wiki/ミニDINコネクタ "wikilink")を使用している。

キーボードエンコーダには仕掛けがあり、特定の操作をするとマニュアルに無い機能があったり、隠しメッセージが表示されるようになっている。

### 従来機種との互換性

FM-7/77シリーズとは高い互換性を持つ。

内蔵オプションは、[Z80](../Page/Z80.md "wikilink")カード用スロットが削除されたためメインCPUの切替が不可能になり[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")などのOSはサポートされなくなったが、FM-7互換スロットは用意されたため各種増設カードはほぼそのまま使用可能だった。

外部オプションは、一部インタフェースが仕様変更されたためモジュール方式のI/O拡張ユニットやFM-77に用意された専用オプションなどは使用できなくなったが、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")などはケーブルさえ用意すればそのまま使用可能だった。

起動時のBASICモード/DOSモードを選択するブートモードスイッチおよび[サイクルスチール](https://ja.wikipedia.org/wiki/サイクルスチール "wikilink")のON/OFFを選択するグラフィックモードスイッチなど従来機種と同等のスイッチは用意されており、FM-7/77同様BASICモードでディスクを入れずに起動するとF-BASIC V3.0(ROMモード)が起動する。

これはブート機構に工夫がなされており、リセットがかかると先ずイニシエータROMが表に出てそこから起動。画面モード、アナログパレットなど、新規デバイスの初期化を行い、モードスイッチを読み取ってBASIC ROMを有効化させたりRAM領域にするかなどの設定を行った後、従来のブート機構に制御を移すという2段構えの初期化機構が採用されており、これによって新たなモードスイッチを用いない上位互換を確保している。

このため、FM77AV専用ではないアプリケーションソフトやゲームソフトにも、リアルタイムキースキャン・DMACに対応する「リバイバー」([アルシスソフトウェア](../Page/サイバーヘッド_\(ゲーム会社\).md "wikilink"))、DMACに対応する「キス・オブ・マーダー　殺意の接吻」([リバーヒルソフト](../Page/リバーヒルソフト.md "wikilink"))など、FM77AVで拡張されたハードウェアの機能を使用出来るようになっているものが存在する。

### 基本仕様

  - FM77AV-1/2

<!-- end list -->

  - CPU: MC6809(2MHz)×2（メイン、サブ）
  - ROM: F-BASIC 32KB、イニシエータ 8KB、サブシステムモニタ 28KB、キャラクタ 4KB、JIS第一水準漢字 128KB
  - RAM: メイン128KB（最大192KB）、サブ5KB、[VRAM](../Page/VRAM.md "wikilink") 96KB
  - FDD: 3.5"2D×2(AV-2),3.5"2D(AV-1)
  - OS: F-BASIC V3.3L10
  - Text Mode: 80×20/25(3bit color),40×20/25(3bit color/12bit color) character
  - Graphic Mode: 640×200(3bit color)×2,320×200(12bit color) pixel
  - Sound: [YM2203](../Page/YM2203.md "wikilink")による[FM音源](../Page/FM音源.md "wikilink")、SSGを各々8オクターブの音域で3音同時出力可能。
  - キーボード: シリンドリカル・ステップドスカルプチャキーボード、nキーロールオーバー機能、ワイヤレス機能搭載
  - ジョイスティック: アタリ規格9pin端子×2

<!-- end list -->

  - 追加オプション（基本はFM-7に準ずる）

<!-- end list -->

  - 内部オプション
      - FM77MD201/FM77MD202 モデムカード-1200
      - FM77-121 SCSIカード
      - FM77EM64 拡張RAMカード-64（AV用）
      - FM77EM64A 拡張RAMカード-64（AV20/AV20EX用）
      - FM77EM256 拡張RAMカード-256（AV40/AV40EX/AV40SX用）
      - FM77-211 日本語カード（AV/AV20/AV20EX用、JIS第二水準漢字ROM、辞書ROM、64KB RAMを搭載。学習RAMのバッテリーバックアップ機能付き）
      - FM77-411 ビデオディジタイズカード（AV用）
      - FM77-412 ビデオディジタイズカード（AV40/AV20用）
      - FM77-413 ビデオディジタイズカード（AV40EX/AV20EX用）
      - FM77-414 ビデオカード（AV20EX/AV40EX用。ビデオディジタイズカードにビデオコンバート機能を追加したもの）
      - FM77-171 文字放送カード
      - FM77-143 ハンディイメージスキャナインタフェースカード
      - FM77-421 音声認識カード
      - FM77-431 音声合成カード
  - 外部オプション
      - FM77-601 I/O拡張ユニット（FM-7/77のものとは異なり、内部オプションの32ピンカードが3枚装着できるユニット。FM-7/77でも使用可能）
      - FM77-401 MIDIアダプタ
      - FMAV-401 ステレオミュージックボックス（本体と別にMML解析用のCPUや[FM音源を搭載したインテリジェントな](../Page/YM2151.md "wikilink")[MIDI](../Page/MIDI.md "wikilink")楽器。FM-7/77でも使用可能。）
  - 動作する主要OS:
      - [OS-9](../Page/OS-9.md "wikilink")/6809 Level 2

### FM77AVシリーズ

  - 初代（[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")10月発売）ワイヤレスキーボード、nキーロールオーバー対応。F-BASIC V3.3L10添付。
      - FM77AV-1 FDD1基搭載。128,000円。
      - FM77AV-2 FDD2基搭載。158,000円。
  - 二代目（[1986年](../Page/1986年.md "wikilink")発売）2DD/2D兼用FDD搭載、ワイヤレスキーボード、[2キーロールオーバー](https://ja.wikipedia.org/wiki/nキーロールオーバー "wikilink")。
      - FM77AV20-1 FDD1基搭載。138,000円。F-BASIC V3.3L20添付。
      - FM77AV20-2 FDD2基搭載。168,000円。F-BASIC V3.3L20添付。
      - FM77AV40 FDD2基搭載。228,000円。日本語カード搭載。VRAM144KB（320×200×262,144色1画面・640×400×8色1画面）、[DMAC追加](../Page/Direct_Memory_Access.md "wikilink")。F-BASIC V3.4L10添付。
  - 三代目（[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")発売）2DD/2D兼用FDD2基搭載。MMR使用時にクロックスピードが2MHz→1.6MHzに落ちないモードを追加。
      - FM77AV20EX 128,000円。カセットインターフェースが廃止。[DMAC追加](../Page/Direct_Memory_Access.md "wikilink")。F-BASIC V3.3L30添付。
      - FM77AV40EX 168,000円。VRAM192KB、640×400×8色・320×200×4096色 2画面・640×200×8色 4画面。F-BASIC V3.4L20添付。MMUのアドレス空間が1MiBに拡張され、最大搭載メモリが、960KBとなっている。
  - 最終機（[1988年](../Page/1988年.md "wikilink")11月発売）本体色変更（黒色→マーブル色）
      - FM77AV40SX 178,000円。F-BASIC V3.4L21添付。
          - ビデオディジタイズ、スーパーインポーズ等ができる機能を標準で搭載したFM77AV40EXのマイナーチェンジモデル。RGB出力端子はそれまでのEIAJ-21ピン端子から、D-sub25ピンに変更されている。また、FM77AV40EXでは隠し機能だったアップスキャンコンバータ(HSYNC 15kHzから24kHzへの変換)が正式な機能となった他、カセットインターフェースが廃止されている。ビデオディジタイズ・ビデオコンバート機能（FM77-414相当）を標準装備。グレー色の本体の前面とキーボードの上面に大理石のような塗装が施されており、[墓石](../Page/墓石.md "wikilink")パソコンと呼ばれることもあった。FM-7シリーズの最終機となった。

## 脚注

### 注釈

### 出典

## 関連項目

  - [FM-8](../Page/FM-8.md "wikilink")
  - [FM-11](../Page/FM-11.md "wikilink")シリーズ
  - [FM-X](../Page/FM-X.md "wikilink")
  - [FM-16β](https://ja.wikipedia.org/wiki/FM-16β "wikilink")シリーズ
  - [FM-16π](https://ja.wikipedia.org/wiki/FM-16π "wikilink")
  - [FMRシリーズ](../Page/FMRシリーズ.md "wikilink")
  - [FM TOWNSシリーズ](../Page/FM_TOWNS.md "wikilink")
  - [FMV](../Page/FMV.md "wikilink")シリーズ

## 外部リンク

  - [Oh\!FM-7](http://fm-7.com/)
  - [コンピュータ博物館：日本のコンピュータ：パーソナルコンピュータ：富士通：FM77AV（エフエム セブン セブン エー ブイ）](http://museum.ipsj.or.jp/computer/personal/0017.html)

[Category:富士通のパーソナルコンピュータ](https://ja.wikipedia.org/wiki/Category:富士通のパーソナルコンピュータ "wikilink") [Category:グッドデザイン賞](https://ja.wikipedia.org/wiki/Category:グッドデザイン賞 "wikilink")

1.  [フジツウ・エスパーニャ (FESA) 同窓会](http://terrytak.web.fc2.com/0407.html)
2.  [Fujitsu / Secoinsa FM-7](http://museo8bits.com/ficha.php?nombre=fm7)
3.  [Fujitsu FM-7 (Fujitsu Micro 7)](http://zonadepruebas.org/deepfb/ordenadores/fm7/fm7.htm)
4.  富士通 FM-7 ユーザーズマニュアル システム解説書
5.  富士通 FM-7 ユーザーズマニュアル システム解説書
6.  [受賞番号:59K1044（受賞対象:FM-77D2(MB-25250)）](http://www.g-mark.org/award/describe/10619)
7.  [FM77 | クラシックPC研究会](https://classicpc.org/jp/category/item/itemgenre/fm77/)