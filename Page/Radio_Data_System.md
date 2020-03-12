> この記事は[Radio Data System](https://ja.wikipedia.org/wiki/Radio_Data_System)から翻訳されています。


**Radio Data System**（ラジオ・データ・システム、RDS）とは、従来の[FMラジオ](https://ja.wikipedia.org/wiki/FMラジオ "wikilink")放送に少量のデジタル情報を埋め込むための[通信プロトコル](../Page/通信プロトコル.md "wikilink")規格である。 RDSは、時間、放送局、番組情報を含め、複数種類の送信情報を規格化している。この規格は[欧州放送連合](../Page/欧州放送連合.md "wikilink")(EBU)の事業として始まり、やがて[国際電気標準会議](../Page/国際電気標準会議.md "wikilink")(IEC)の国際標準規格となった。

米国版のRDSは正式名称がRadio Broadcast Data System(RBDS)で、両者の規格には僅かばかりの差異がある。

日本では、RDSに類似したデジタルデータ放送規格[Data Radio Channel](https://ja.wikipedia.org/wiki/Data_Radio_Channel "wikilink")(DARC)をほぼ同時期に開発\[1\]、実用化した経緯から、RDSには未対応である。

## 概要

RDSもRBDSも、57kHzの[副搬送波で](https://ja.wikipedia.org/wiki/周波数変調#FMステレオ方式 "wikilink")1187.5[ビット毎秒](../Page/ビット毎秒.md "wikilink")のデータを伝送するため、各データビット間には正確に48サイクルの副搬送波がある。

データ信号、ステレオ、および38kHzの[DSB-SCステレオ差信号間の干渉と相互変調を最小限に抑えるため](https://ja.wikipedia.org/wiki/振幅変調#抑圧搬送波両側波帯 "wikilink")、RBDSやRDSの副搬送波は19kHzでのFMステレオパイロット信号の第3[高調波](../Page/高調波.md "wikilink")に設定されている（ステレオ差信号は最大で38kHz+15kHz = 53kHzまで拡張され、RDS信号の下側波帯に4kHzを残す）。

このデータは[エラー訂正付きで送信される](../Page/誤り検出訂正.md "wikilink")。 RDSは、プライベートまたはその他の未定義な機能を未使用のプログラムグループに「パッケージ化」させる方法など、様々な機能を定義している。

## 開発

RDSは、ドイツにある放送技術研究所([IRT](https://ja.wikipedia.org/wiki/:en:InstitutfürRundfunktechnik "wikilink"))およびラジオ製造業者の[ブラウプンクト](https://ja.wikipedia.org/wiki/ブラウプンクト "wikilink")による運転者用ラジオ交通情報システム([ARI](https://ja.wikipedia.org/wiki/:en:Autofahrer-Rundfunk-Informationssystem "wikilink"))の開発から着想を得たものである\[2\]。ARIはFMラジオ放送における交通情報の存在を示すために57kHzの副搬送波を使用していた\[3\]。

欧州放送連合の技術委員会は1974年のパリ会合で、ARIと似た目的の技術を開発するプロジェクトを発足した。ただしこちらはより柔軟で、放送ネットワークが同じラジオ番組をいくつかの異なる周波数で送信した場合の受信機の自動再同調を可能にするものであった。変調方式はスウェーデンの[ページング方式](../Page/ページング方式.md "wikilink")で使われたものに基づいており、[ベースバンド符号化は新たな設計で主に](https://ja.wikipedia.org/wiki/伝送路符号 "wikilink")[英国放送協会](../Page/英国放送協会.md "wikilink")(BBC)とIRTによって開発された。1984年に欧州放送連合は最初のRDS仕様を発行した\[4\]。

代替周波数機能の強化が規格に追加されると、RDSはその後1990年に[欧州電気標準化委員会](https://ja.wikipedia.org/wiki/欧州電気標準化委員会 "wikilink")(CENELEC)規格として発行された\[5\]。1992年、米国ラジオシステム委員会([NRSC](https://ja.wikipedia.org/wiki/:en:National_Radio_Systems_Committee "wikilink"))はラジオ放送データシステム(Radio Broadcast Data System)と呼ばれるRDS規格の北米版を発行した。 CENELEC規格は1992年に交通メッセージチャンネル([TMC](https://ja.wikipedia.org/wiki/:en:Traffic_Message_Channel "wikilink"))の追加と共に更新され、1998年には[オープンデータ](https://ja.wikipedia.org/wiki/オープンデータ "wikilink")のアプリケーション\[6\]が付随し、そして2000年にはRDSがIEC標準規格62106として世界的に公開された\[7\]。

### RDS 2.0

RDSフォーラム（スイス・[ジュネーブ](https://ja.wikipedia.org/wiki/ジュネーブ "wikilink")）は、2015年6月の年次総会において新たな標準規格RDS2を運用することを決定した。 この規格は、米国ラジオシステム委員会のRBDS小委員会から来た（同じ技術を扱う）仲間と緊密に協力して作成されたもので、世界中のFM放送とデータサービスのための統一された[プラットフォームを提供するものとなっている](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。 [RDS1_RDS2.png](https://ja.wikipedia.org/wiki/File:RDS1_RDS2.png "fig:RDS1_RDS2.png")

  - 主な特徴

<!-- end list -->

  - 64MHzから108MHzまでの周波数を切れ目なくサポート(AF、[EON](https://ja.wikipedia.org/wiki/:en:Enhanced_other_networks "wikilink"))。
  - 新たな[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")として[UTF-8](../Page/UTF-8.md "wikilink")（古いEBU文字セットは古い0A/2Aグループの互換モードのために残っている）。
  - 新しいODA処理 - "B"グループは 信号伝送グループとして"A"グループに割り当てられる。
  - 長いPS名 - UTF-8文字セットで最大32バイト（インド語、中国語、アラビア語など）。
  - 128バイト長のラジオテキスト(eRT)をUTF-8で表示。
  - 11.4毎秒から最大57"A"グループ毎秒まで容量を増加（シングル変調型マルチサブキャリア(SMMS)技術による2109ビット毎秒の純容量）。
  - グラフィカル・ラジオテキスト - HTML/CSSテンプレートの動作サポート（スマートフォン、カーラジオ、コンピュータ/タブレット用）。
  - 受信機にIPまたはSMS機能がある場合、gRTを超えてのチャンネル復帰をサポート。
  - 放送局のグラフィックロゴ - 最大4キロバイトの画像（JPEGかPNGかGIF）。
  - ハイブリッドラジオ機能（一部を[ラジオ・フランス](https://ja.wikipedia.org/wiki/ラジオ・フランス "wikilink")の開発に基づく）。

## コンテンツと実装

RDSデータには通常、次のような情報分野が含まれている。 [TomTom_Navigation_System_with_RDS-TMC.jpg](https://ja.wikipedia.org/wiki/File:TomTom_Navigation_System_with_RDS-TMC.jpg "fig:TomTom_Navigation_System_with_RDS-TMC.jpg")社のナビゲーションシステムに接続された交通メッセージチャンネル(RDS-TMC)の受信機（左）\[8\]\]\]

  - AF（代替周波数リスト）

これは第一信号が弱くなり過ぎた場合（例えば範囲外に移動したとき）に、同じ局を提供している別の周波数に受信機が再同調できるよう、受信機に提供される周波数のリスト。切り替えを実行する前に、ラジオはPIコード（後述）の一致を確認してAFが同じ局であることを保証している。これはカーステレオ・システムでよく使われていて、移動中にヘッドユニットがより強い信号に自動的に同調できるようにしており、オプションで同じ地域コードにもできる（したがって全国放送局の場合、利用者はオリジナルのラジオ番組を聞き続けられる）。

  - CT（時計の日時）

受信機内部の時計または車のメイン時計を同期させることが可能。送信ブレのため、CTは[UTC](https://ja.wikipedia.org/wiki/UTC "wikilink")の100ミリ秒以内での精度まで可能である。RDSエンコーダ内で時計を定期的に同期させる方法が放送装置にない場合、一般的にCTは送信されない。

  - EON（その他ネットワーク情報の強化）

交通番組が放送されていることで、ある瞬間に周波数をネットワークの特定放送局に合わせるTAフラグのようなデータを動的に変更するため、聞いている人につながった他のネットワークや放送局について受信者に通知し、自動的かつ一時的にラジオがその局に同調できるようにしている。

  - PI（プログラム識別）

これは放送局を識別する固有の[16進法](https://ja.wikipedia.org/wiki/16進法 "wikilink")コード4文字である。国内すべての放送局は正しい国の接頭文字が入った固有の3文字コードを使用する必要がある。米国では、局の[コールサイン](https://ja.wikipedia.org/wiki/コールサイン "wikilink")に式を適用してPIが決定される。 PIコードは最も重要なRDSのパラメータであり、RDSデータ構造内で最も頻繁に送信される。 米国以外で使うRDS規格では、あらゆる国の国番号が定義されているため、一般的な国境のある場所で同じコードを使用することはできない。これにより、他国間でコードを調整する必要がなくなっている。同一コードを運ぶ送信は受信側によって全て同じと見なされるも、受信を改善するための代替周波数として切り替えることは可能である（たとえ代替周波数として特に記載されていなくても）。

  - PS（プログラムサービス名）

これは単に[呼出符号](https://ja.wikipedia.org/wiki/呼出符号 "wikilink")または放送局のID名を表す8文字の静的表示である。ほとんどのRDS対応受信機はこの情報を表示し、もしその局が受信機の事前設定（プリセット）に保存されていれば、PIコード、周波数、およびそのプリセットに関連する他の詳細と共にこの情報を[キャッシュする](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。一部の国では、PSを使用して放送局が他の情報を動的に送信している。これは一部の国では禁止されており、RDSシステム内での使用は意図されていなかったものである。

  - PTY（プログラムタイプ）

予め定義された最大31の番組種類コード（例えばヨーロッパでは、PTY1ニュース、PTY6ドラマ、PTY11ロック音楽）は、利用者がジャンルによって同様の番組を見つけることができるようにしている。PTY31は、自然災害やその他の重大な災害が発生した場合に備えた緊急アナウンス用に予約されている。

  - REG（地域）

これは主に、全国放送局がその地域の[オプトアウト](https://ja.wikipedia.org/wiki/オプトアウト "wikilink")など「地域固有の」番組を一部の送信機で実行している国で使用されている。この機能は利用者が他の地域に移動する際に、設定を現在の地域に「固定」したり、ラジオが他の地域固有の番組に同調できるようにするものである。

[Radio_Data_System_(RDS)_on_95.9_KFSH_La_Mirada.jpg](https://ja.wikipedia.org/wiki/File:Radio_Data_System_\(RDS\)_on_95.9_KFSH_La_Mirada.jpg "fig:Radio_Data_System_(RDS)_on_95.9_KFSH_La_Mirada.jpg")

  - RT（ラジオテキスト）

この機能で、ラジオ局は64文字（一部では32文字）の自由な文章メッセージを送信できるようになっており、それは静的なもの（局のスローガンなど）でも番組プログラムと同期するもの（現在放送中の番組タイトルやアーティストなど）でも構わない。

  - RT+（ラジオテキストプラス）

アーティスト、タイトル、その他の[メタデータ](../Page/メタデータ.md "wikilink")を受信者に送れるようにした、以前のラジオテキストの強化版。

  - TA、TP（[交通情報](../Page/交通情報.md "wikilink")、交通番組）

このフラグは特に注意が必要で、交通ニュース速報を受信するために例えばCDを一時停止したり、再調整をしたりする。TPフラグは定期的に交通ニュース速報を放送する局のみを利用者が見つけられるようにするために使用され、一方でTAフラグは今起きている実際の交通ニュース速報を知らせるために使用される。この機能は（利用者に交通情報をより知らせるため）ラジオユニットがCD/MP3を一時停止したり、交通ニュース速報中に音量を上げるなど、一緒に他の操作も行なわれている可能性がある。

  - TMC（交通メッセージチャンネル）

デジタル符号化された交通情報。全てのRDS機器がこれをサポートしているわけではないが、[カーナビゲーション](../Page/カーナビゲーション.md "wikilink")では利用可能なことが多い。多くの国では暗号化された交通データのみが放送されるので、交通データを使用するには恐らく定額制サービスに関連付けられた適切なデコーダが必要となる。その定額料金は自動車メーカーによって支払われることが多く、したがって利用者は意識しなくともよい。

## RDSの互換性

57 kHzのRDS副搬送波は、理論的には53kHzにおけるステレオ副搬送波の上限遮断よりも上にあり続ける[複合スペクトルの](https://ja.wikipedia.org/wiki/周波数スペクトル "wikilink")±2 kHzを占有している。ただし、53kHz遮断はステレオエンコーダーの前に使用されていた15kHz[ローパスフィルタ](../Page/ローパスフィルタ.md "wikilink")の性能に完全に左右される。旧式の機器では、これらのフィルタは19kHzパイロット信号を保護するためだけに設計されており、大量のステレオ情報が存在する場合にはRDS副搬送波の十分な保護をしなかったりもする。こうした状況では、積極的な音声処理と組み合わさったステレオ増強装置がRDS副搬送波を受信不能にしてしまう恐れがある。

複合クリッピングシステムは、クリッピング（ピーク周波数部分のカット）により生じる高調波のためにRDS副搬送波を劣化させる可能性がある。最近の複合クリッパーには、RDS副搬送波を保護するためのフィルタリングが含まれている。

RDS副搬送波は一般的に2-4kHzの搬送波偏移を使用する。そのため、通常75kHzの偏移制限を超えないとするなら、プログラム素材に使用できる偏移はこの量だけ減少する。

## RDSの使用例

次の3つの画像は、FMラジオ局でどのようにRDSが使用されるかを図示している。2番目以降は、ラジオを[トレントFM](https://ja.wikipedia.org/wiki/トレントFM "wikilink")という[ノッティンガム](../Page/ノッティンガム.md "wikilink")のラジオ放送局に合わせた時に撮影されたもの。画像は全てソニーXDR-S1 DAB / FM / MW / LW携帯ラジオのディスプレイ。

[`Sony_no_rds.JPG`](https://ja.wikipedia.org/wiki/File:Sony_no_rds.JPG "fig:Sony_no_rds.JPG")

[Sony_rds_pi.JPG](https://ja.wikipedia.org/wiki/File:Sony_rds_pi.JPG "fig:Sony_rds_pi.JPG") [Sony_now_playing.JPG](https://ja.wikipedia.org/wiki/File:Sony_now_playing.JPG "fig:Sony_now_playing.JPG")'s *[Save a Prayer](https://ja.wikipedia.org/wiki/:en:Save_a_Prayer "wikilink")*- が表示される。一番下の行はスクロールして残りのテキストを表示していく。\]\] 注）下の2つは、RDS導入地域で使用した場合に限る。日本国内では、RDSと類似する[Data Radio Channel](https://ja.wikipedia.org/wiki/Data_Radio_Channel "wikilink")(DARC)を運用している。

## RDSチップセット

[JVC_MX-J950R_-_antenna_tuner_module_-_Sanyo_LC72723-3896.jpg](https://ja.wikipedia.org/wiki/File:JVC_MX-J950R_-_antenna_tuner_module_-_Sanyo_LC72723-3896.jpg "fig:JVC_MX-J950R_-_antenna_tuner_module_-_Sanyo_LC72723-3896.jpg")、SANYO LC72723\]\] [STマイクロエレクトロニクス](../Page/STマイクロエレクトロニクス.md "wikilink")、[シリコン・ラボラトリーズ](https://ja.wikipedia.org/wiki/シリコン・ラボラトリーズ "wikilink") 、[NXPセミコンダクターズ](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink") (旧 [フィリップス](../Page/フィリップス.md "wikilink")) などの企業が、これらの装置に見られるチップセットを提供している。

低価格で設置面積の小さいチップソリューションのおかげで、ポータブルオーディオおよびナビゲーションデバイスにおけるRDSの実装が増えている。

## 関連項目

[RDS_vs_DirectBand_FM-spectrum2.svg](https://ja.wikipedia.org/wiki/File:RDS_vs_DirectBand_FM-spectrum2.svg "fig:RDS_vs_DirectBand_FM-spectrum2.svg")信号の典型的なスペクトル\]\]

  - [Data Radio Channel](https://ja.wikipedia.org/wiki/Data_Radio_Channel "wikilink")(DARC) - 日本で開発された、RDSと類似のデジタルデータ放送標準規格。
  - [ALERT FM](https://ja.wikipedia.org/wiki/:en:ALERT_FM "wikilink") - RDSを活用した緊急広報システム。
  - [デジタルラジオ](../Page/デジタルラジオ.md "wikilink")
  - [FM放送](https://ja.wikipedia.org/wiki/FM放送 "wikilink")
  - [インターネットラジオ](../Page/インターネットラジオ.md "wikilink")
  - [文字多重放送](https://ja.wikipedia.org/wiki/文字多重放送 "wikilink")

## 脚注

## 外部リンク

  - [Specification of the RDS standard, available via the RDS Forum](http://www.rds.org.uk/2010/RDS-Specification.htm)
  - ["NRSC-4 National Radio Systems Committee United States RBDS Standard - Specification of the radio broadcast data system (RBDS)"](https://www.nrscstandards.org/standards-and-guidelines/accept.asp?name=documents/standards/nrsc-4-b.pdf)
  - [RDS Features Serving as Tuning Aids](https://web.archive.org/web/20100331064554/http://www.rds.org.uk/rds98/pdf/RDS_book_sample.pdf)
  - [RDSList.com](http://www.rdslist.com/)

[Category:通信工学](https://ja.wikipedia.org/wiki/Category:通信工学 "wikilink") [Category:ラジオ用語](https://ja.wikipedia.org/wiki/Category:ラジオ用語 "wikilink") [Category:デジタルラジオ](https://ja.wikipedia.org/wiki/Category:デジタルラジオ "wikilink")

1.  「\[<https://www.nhk.or.jp/strl/aboutstrl/evolution-of-tv/p17col_2.html>　技研がリードしたニューメディア\]」、NHK放送技術研究所『テレビは進化する』、2010年3月19日。2019年4月14日閲覧。
2.
3.
4.
5.
6.
7.
8.