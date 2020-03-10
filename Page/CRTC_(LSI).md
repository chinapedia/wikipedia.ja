> この記事は[CRTC \(LSI\)](https://ja.wikipedia.org/wiki/CRTC_\(LSI\))から翻訳されています。


**CRTC**（シーアールティーシー）は[CRT](../Page/ブラウン管.md "wikilink") Controller の略称であり、コンピュータの映像機能のうち、その名の通り映像信号の生成など比較的出力端に近い機能を持つLSIである。[VDP](https://ja.wikipedia.org/wiki/VDP "wikilink")(Video Display Processor)や[GPU](../Page/Graphics_Processing_Unit.md "wikilink")(Graphic Processing Unit)、GDC(Graphics Display Controller)など各種のLSIの呼称があるが、例えばPC-9801では使い分けられているにもかかわらず、混同する者のほうが多い。

主に[ラスタースキャン](../Page/ラスタースキャン.md "wikilink")型ディスプレイのキャラクター（文字）表示制御用として発展してきたが、上位品種にはビットマップ表示の転送、回転、拡大、縮小、反転表示などもできる機能が追加されている。

## 種類　

[thumb](https://ja.wikipedia.org/wiki/ファイル:MC68A45_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:HD68B45SP_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:uPD3301_01.jpg "wikilink")

  - 6845系CRTC
      - MC6845　[モトローラ](../Page/モトローラ.md "wikilink")　（バスタイミング1MHz,CRT表示タイミング3MHz）
          - モトローラ系6800ファミリーであり、インターフェイスは同期バス形式。
          - x86系であるIBM-PC/XTのモノクロームディスプレイアダプター(MDA)でも使用された。
          - 最大256×64キャラクター
          - 1文字のドット構成設定可
          - 水平/垂直同期信号制御可
          - 表示タイミング信号制御可
          - カーソル制御（形状変更、ブリンク）
          - ページング、スクロール機能
          - 14ビットVRAMリフレッシュ生成（最大16Kワードアクセス）
          - [ライトペン](../Page/ライトペン.md "wikilink")インターフェイス内蔵
          - インタレース、ノンインタレース設定可
          - 本CRTC単体ではモノクロキャラクター表示機能のみだが、外部にカラーマルチプレクサやグラフィックパターンジェネレータ、画像合成回路を設けることにより[パックドピクセル](https://ja.wikipedia.org/wiki/パックドピクセル "wikilink")構成のカラービットマップキャラクターの表示が可能。
      - MC68A45　モトローラ
          - バスタイミング1.5MHz改良版。CRT表示タイミングは3.0MHz。
      - MC68B45　モトローラ
          - バスタイミング2.0MHz改良版。CRT表示タイミングは3.0MHz。
      - HD6845　[日立製作所](../Page/日立製作所.md "wikilink")CRTC　MC6845互換CRTC。CRT表示タイミングは3MHz。
          - セラミックパッケージ版
              - HD6845 （バスタイミング1.0MHz）
              - HD68A45（バスタイミング1.5MHz）
              - HD68B45（バスタイミング2.0MHz）
          - プラスチックパッケージ版
              - HD6845P (HD46505R)　 （バスタイミング1.0MHz）
              - HD68A45P(HD46505R-1)（バスタイミング1.5MHz）
              - HD68B45P(HD46505R-2)（バスタイミング2.0MHz）
      - HD6845S　[日立製作所](../Page/日立製作所.md "wikilink")CRTC　MC6845上位互換CRTC。CRT表示タイミングは3.7MHz。
          - セラミックパッケージ版
              - HD6845S （バスタイミング1.0MHz）
              - HD68A45S（バスタイミング1.5MHz）
              - HD68B45S（バスタイミング2.0MHz）
          - プラスチックパッケージ版
              - HD6845SP (HD46505SP) （バスタイミング1.0MHz）
              - HD68A45SP(HD46505SP-1)（バスタイミング1.5MHz）
              - HD68B45SP(HD46505SP-2)（バスタイミング2.0MHz）
      - HD6345,6345xxJ(動作温度拡張版)　[日立製作所](../Page/日立製作所.md "wikilink")CRTC-II
          - HD6845SのCMOS化および上位コンパチブル版、6800系インターフェイス、CRTディスプレイタイミング4.5MHz動作、画面分割、スムーススクロール、外部同期、2つのカーソル制御、メモリ幅設定、マルチポートメモリ制御などの機能を有する。
      - HD6445,6445xxJ(動作温度拡張版)　[日立製作所](../Page/日立製作所.md "wikilink")CRTC-II
          - HD6845SのCMOS化および上位コンパチブル版、80系インターフェイス、CRTディスプレイタイミング4.5MHz動作、画面分割、スムーススクロール、外部同期、2つのカーソル制御、メモリ幅設定、マルチポートメモリ制御などの機能を有する。
      - MB89321　 [富士通](../Page/富士通.md "wikilink")　MC6845上位互換、CMOS版CRTC。6800系インターフェイス。
          - スキャンモードはインタレース、ノンインタレース、ノンインタレース&ビデオ設定可能
          - 垂直ブランキング/ライトペン割込み機能
          - 4分割スクリーンの独立ページング/スクローリング可能
          - 最大4画面までの同時スムーススクロール機能
          - 外部同期、テレビ放送との重畳表示、他のCRTCとの同期化
      - MB89321A　[富士通](../Page/富士通.md "wikilink")　MB89321の高速版
      - MB89321B　[富士通](../Page/富士通.md "wikilink")　MB89321の高速版
      - MB89322　 [富士通](../Page/富士通.md "wikilink")　MB89321の80系インターフェイス版
      - MB89322A　[富士通](../Page/富士通.md "wikilink")　MB89322の高速版
      - MB89322B　[富士通](../Page/富士通.md "wikilink")　MB89322の高速版
      - HD63484　[日立製作所](../Page/日立製作所.md "wikilink")　ACRTC（アドバンストCRTC）
          - オンチップ上に円やペイントなど23種のグラフィック描画機能と、重ね合わせ表示やズーム、スクロールなどの機能が有る。データバス幅は8/16bitで68/68K系に使われる。

<!-- end list -->

  - 3301系（[日本電気](../Page/日本電気.md "wikilink")製）
      - μPD3301 [PC-8001などで使われた](https://ja.wikipedia.org/wiki/PC-8000シリーズ "wikilink")。
  - 7220系（日本電気製。これはGDCであってCRTCではない（98で使用していてCRTCと呼んでるのは別の石で、GDCとCRTCでは役割が異なる））
      - [μPD7220](https://ja.wikipedia.org/wiki/μPD7220 "wikilink")(GDC:Graphic Display Controller) [PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")などに使われた。
      - μPD7220A(HGDC:High-performance Graphic Display Controller) [PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")などに使われた。
      - μPD72020(EGDC:Enhanced Graphic Display Controller)
      - μPD72120(AGDC:Advanced Graphic Display Controller)
      - μPD72123(AGDCII:Advanced Graphic Display Controller II)
          - 直線や四辺形など7種のグラフィック描画機能を持つ。データバス幅は8bitでX86系に使われる。

<!-- end list -->

  - RP5C16（64ピンDIP）/RP5C16A（64ピンQFP）　[リコー](../Page/リコー.md "wikilink")製
      - キャラクターグラフィックス(PCG)とビットマップグラフィックステーブルを持ち、同時合成表示可能なCRTC。
      - 16色カラー表示
      - グラフィックはカラー指定R,G,B,L/D(LIGHT/DARK)の各1ビットのパックドピクセルで構成され、8ビットで1ブロックを構成する。
      - 4つのカラー表示モードを持つ。それぞれフォアグラウンド画面が手前（最優先）表示、バックグラウンド画面はフォアグラウンド画面の後ろに表示される。バックグラウンド画面の後ろにさらにバックドロップ画面がある。
      - 表示モード1:80×25文字1画面のバックグラウンド画面
      - 表示モード2:640×200ドットのバックグラウンド画面
      - 表示モード3:40×25文字2画面のバックグラウンドとフォアグラウンド合成画面
      - 表示モード4:320×200ドットのバックグラウンドと40×25文字フォアグラウンド画面の合成表示
      - 2画面合成同時表示（表示モード3,4）
      - 仮想スクリーン（320,512,640,1024ドット）：表示画面は最大320×200ドット固定だが、表示開始アドレスと表示終了アドレスを変更することにより一画面をサイズ自体はそのままで、スクロールさせて擬似的に連続する画面があるように見せる機能。128KB接続時に320×200ドット画面4枚を横一列に並べて一枚とし、連続した領域をスクロールさせることが可能。
      - 文字のアトリビュート表示機能（前後反転:フォアグラウンドとバックグラウンドの優先表示切り替え）、左右反転、上下反転、白黒反転）
      - 水平、垂直スムーススクロール機能
      - クロスヘアカーソル（十時マーク）表示機能（マウス用）
      - MASTER/SLAVEモード（スーパーインポーズ可能）
      - Z80,86系インターフェイス、6502インターフェイス直結可能
      - VRAMリフレッシュ用アドレスバッファレジスタ/アドレスカウンタ内蔵
      - 60Hzノンインタレース表示
      - CMOSプロセス

<!-- end list -->

  - RP5C16Y（60ピンQFP）　[リコー](../Page/リコー.md "wikilink")製CRTC
      - RP5C16/RP5C16Aから文字表示機能を削除し、かわりにビットマップグラフィックス表示に特化したもの。
      - カラー16色、320×200ドットのビットマップグラフィックス表示可能
      - ×2,×4倍拡大表示機能
      - クロスヘアカーソルはブリンク機能を追加
      - NTSCインタレース表示によるコンポジットビデオ出力を追加

<!-- end list -->

  - RP5C56（64ピンSDIP）　[リコー](../Page/リコー.md "wikilink")製CRTC

## 関連項目

  - [CRT](../Page/ブラウン管.md "wikilink")
  - [Graphics Processing Unit](../Page/Graphics_Processing_Unit.md "wikilink")
  - [VRAM](../Page/VRAM.md "wikilink")
  - [ウィンドウアクセラレータ](https://ja.wikipedia.org/wiki/ウィンドウアクセラレータ "wikilink")
  - [グラフィックアクセラレータ](https://ja.wikipedia.org/wiki/グラフィックアクセラレータ "wikilink")
  - [ディスプレイ](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")

[Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink") [Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")