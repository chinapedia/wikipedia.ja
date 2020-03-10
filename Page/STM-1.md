> この記事は[STM-1](https://ja.wikipedia.org/wiki/STM-1)から翻訳されています。


**STM-1** （ **Synchronous Transport Module level-1** 、同期転送モジュールレベル1）は、 [SDH](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink") [ITU-T](../Page/ITU-T.md "wikilink") [光ファイバー](../Page/光ファイバー.md "wikilink") ネットワーク伝送規格である。 ビットレートは155.52 Mbit / sである。 より高いレベルは一度に4倍になる。現在サポートされている他のレベルはSTM-4 、 [STM-16](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink") 、 [STM-64および](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink")[STM-256である](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink")。 上記の[STM-256](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink") [波長分割多重](../Page/光波長多重通信.md "wikilink") （WDM）は、海底ケーブルで一般的に使用されている。 \[1\] \[2\]

## フレーム構造

STM-1フレームは、 [SDH](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink") （Synchronous Digital Hierarchy）の基本的な伝送形式に基づいている。 STM-1フレームのバイト指向構造は、9行270列のバイトで、合計2,430バイト（9行\* 270列= 2430バイト）である。 各バイトは64kbit / sチャネルに対応する。 \[3\]

[770x770ピクセル](https://ja.wikipedia.org/wiki/File:SDH-Frame-STM1.png "fig:770x770ピクセル")

**TOH** ：輸送オーバーヘッド（  +  +  ）

  - : Multiplex Section Overhead

  - : Regeneration Section Overhead

  - : AU-4 Pointers

**VC4** ：仮想コンテナ4ペイロード（  +  ）

  - : Path Overhead

## フレーム特性

STM-1ベースフレームは、次の特性で構成されている。

  - **長さ** ：270列×9行= 2430バイト
  - **バイト** ：1バイト= 8ビット
  - **継続時間** （フレーム繰り返し時間）：125μs、つまり8000フレーム/秒
  - **レート** （フレーム容量）：2430×8×8000 = 155.5200 Mbit / s
  - **ペイロード** = 2349bytes×8bits×8000frames / sec = 150.336 Mbit / s

## RSOH（再生器セクションのオーバーヘッド）

[リンク=Special:FilePath/Regenerator_Section_OverHead_in_the_STM-1_frame.jpg](https://ja.wikipedia.org/wiki/File:Regenerator_Section_OverHead_in_the_STM-1_frame.jpg "fig:リンク=Special:FilePath/Regenerator_Section_OverHead_in_the_STM-1_frame.jpg")

  - 最初の行=スクランブルされていないバイト。 したがって、その内容を監視する必要がある
  - X =国内使用のために予約されたバイト
  - D =媒体に応じたバイト数（衛星、無線中継システム、。 。 。 ）

Regenerator Section OverHeadは、STM-1フレームの最初の3行と9列を使用する

  - **A1、A2**フレームアラインメントワードは、STM-Nフレームの開始を認識するために使用される。
  - **A1** ：1111 0110 = F6（HEX）
  - **A2** ：0010 1000 = 28（HEX）
  - **J0** ：パストレース。 SDHネットワークを通るパスに「名前」を付けるために使用される。 このメッセージ（名前）により、受信者は目的の送信機との接続の連続性を確認できる。
  - **B1** ：ビットエラー監視。 B1バイトには、実際のSTMフレームのスクランブル後の、前のSTMフレームのパリティチェックの結果が含まれる。 このチェックは、ビットインターリーブパリティチェック（ BIP-8 ）で実行される。
  - **E1**エンジニアリングオーダーワイヤ（EOW）。 運用および保守の目的で、再生器セクション間で音声信号を送信するために使用できる。
  - **F1**ユーザーチャネル。 サービスとメンテナンスのためにデータと音声を送信するために使用される。
  - 192キロビット/秒で**D3**データ通信チャネル**へのD1（DCCR）。** このチャネルは、STM-Nフレームを介して管理情報を送信するために使用される。

## MSOH（多重化セクションのオーバーヘッド）

[リンク=Special:FilePath/Multiplex_Section_OverHead_in_the_STM-1_frame.jpg](https://ja.wikipedia.org/wiki/File:Multiplex_Section_OverHead_in_the_STM-1_frame.jpg "fig:リンク=Special:FilePath/Multiplex_Section_OverHead_in_the_STM-1_frame.jpg")

X =国内使用のために予約されているバイト。

Multiplex Section OverHeadは、STM-1フレームの5〜9行目と最初の9列を使用する。

  - **B2** ：ビットエラーの監視。 B2バイトには、実際のSTMフレームをスクランブルする前の、RSOHを除く前のSTMフレームのパリティチェックの結果が含まれる。 このチェックは、ビットインターリーブパリティチェック（BIP24）で実行される。
  - **K1、K2**自動保護スイッチング（APS）。 障害が発生した場合、STMフレームは、SDHネットワークを介してK1、K2バイトを使用して新たにルーティングできる。 多重化セクション保護（MSP）プロトコルに割り当てられる。
  - **K2** （Bit6,7,8）MS_RDI：多重化セクションリモート障害表示（以前のMS_FERF：多重化セクション遠端受信障害）
  - 576 kbit / s（DCCM）の**D4からD12**データ通信チャネル。 （上記のRSOHのD1-D3も参照）
  - **S1** （ビット5-8）同期品質レベル：
      - 0000品質不明
      - 0010 G.811 10-11 /日周波数ドリフト
      - 0100 G.812Tトランジット10-9 /日周波数ドリフト
      - 1000 G.812Lローカル2 \* 10-8 /日周波数ドリフト
      - 1011 G.813 5 \* 10-7 /日周波数ドリフト
      - 1111同期には使用される
  - **E2**エンジニアリングオーダーワイヤ（EOW）。 RSOHのE1と同じ機能
  - **M1** MS_REI：多重化セクションのリモートエラーインジケータ、受信したB2バイトでエラーが検出されたインターリーブビットの数。 （以前のMS_FEBE：多重化セクションの遠端ブロックエラー）
  - **Z1、Z2**スペアバイト

## 参考文献

[de:Synchrone Digitale Hierarchie\#SDH_Hierarchiestufen](https://ja.wikipedia.org/wiki/de:Synchrone_Digitale_Hierarchie#SDH_Hierarchiestufen "wikilink")

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:光有線通信](https://ja.wikipedia.org/wiki/Category:光有線通信 "wikilink") [Category:物理層プロトコル](https://ja.wikipedia.org/wiki/Category:物理層プロトコル "wikilink") [Category:光通信](https://ja.wikipedia.org/wiki/Category:光通信 "wikilink") [Category:標準](https://ja.wikipedia.org/wiki/Category:標準 "wikilink")

1.  [Chapter 8](https://books.google.com/books?id=eq1kRHdyXSUC&pg=PA238&dq=STM-1&as_brr=3&ei=D47kS4jTHqqEkATw1uDfCQ&hl=en&cd=4#v=onepage&q=STM-1&f=false) Voice & data communications handbook By Regis J. Bates, Donald W. Gregory
2.  [Table 2 Basic SONET Levels](https://books.google.com/books?id=N-1YbhMKsBUC&pg=PA778&dq=STM-1&as_brr=3&ei=D47kS4jTHqqEkATw1uDfCQ&hl=en&cd=10#v=onepage&q=STM-1&f=false) The Internet encyclopedia, Volume 1 By Hossein Bidgoli
3.  [3.3 Basic principles of SDH](https://books.google.com/books?id=Oq8SEUW1wdQC&pg=PT168&dq=STM-1&as_brr=3&ei=D47kS4jTHqqEkATw1uDfCQ&hl=en&cd=1#v=onepage&q=STM-1&f=false) Networks: internet, telephony, multimedia : convergences and complementarities By Daniel Hardy, Guy Malléus, Jean-Noël Méreur