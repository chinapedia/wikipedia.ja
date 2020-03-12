> この記事は[PlaceEngine](https://ja.wikipedia.org/wiki/PlaceEngine)から翻訳されています。


**PlaceEngine**（**プレイスエンジン**）は、[Wi-Fi](../Page/Wi-Fi.md "wikilink")機器を用いて現在位置を測定する技術のことである。短時間かつ[リアルタイム](../Page/リアルタイム.md "wikilink")にできることが特徴とされる。

## 概要

GPSは、カーナビや航空機・船舶において既に普及していた。しかし都心のビルの谷間や地下ではＧＰＳの電波を受け取ることが出来ない上、現在地取得に時間がかかるなどのデメリットがあった。 そこで、株式会社[ソニーコンピュータサイエンス研究所](../Page/ソニーコンピュータサイエンス研究所.md "wikilink")インタラクションラボラトリー室長の[暦本純一](https://ja.wikipedia.org/wiki/暦本純一 "wikilink")が、実世界指向インターフェイス研究の一環においてPlaceEngineを発案し,当時ソニーCSL研究員であった末吉隆彦 、塩野崎敦らと共に開発した。

PlaceEngineは、ユーザーによる位置検索や位置登録によりデータベースが更新され、それによって対応地域の拡大や推定精度の向上する仕組み。屋内や地下街のような[GPSが機能しない場所でも位置測定できることが特徴](../Page/グローバル・ポジショニング・システム.md "wikilink")。[地図ナビゲーション](https://ja.wikipedia.org/wiki/地図ナビゲーション "wikilink")だけではなく、様々な方法にこの技術が活用されている。

近年では、GPSとPlaceEngineを組み合わせたハイブリッド測位が開発されている。片方が測位不可能でも、もう片方で予測して現在地を出すもの。GPSで取得したデータをPlaceEngineサーバーに送信して、精度向上とエリア拡大を図る機能もある。

自分の知っている土地は、位置登録をして他ユーザーが利用できるようにし、逆に自分の知らない土地では、他ユーザーが登録してくれた位置情報で現在地を割り出す。このように、両者互いに補いあうのが本来の姿である。しかし、利用可能エリアはまだ少なく、ユーザーによる位置登録の協力が求められる。

## 現在地測位

### 位置を取得する

位置の測定には、周囲にある[無線LANアクセスポイント](../Page/アクセスポイント_\(無線LAN\).md "wikilink") (AP) からの電測情報（各アクセスポイントに固有の[MACアドレス](../Page/MACアドレス.md "wikilink")および電波強度の情報）を得て、各アクセスポイントからの電波強度のバランスをもとに現在地を算出する。

取得の際にはPlaceEngineサーバーというAPの位置情報を蓄えたシステムと通信するため、インターネットに接続できる環境を整えておく必要がある。 [PSPのソフトでは](../Page/PlayStation_Portable.md "wikilink")、APデータを[メモリースティック](../Page/メモリースティック.md "wikilink")に保存するためは、測定のみインターネット環境は不要である。ただし放っておくとメモリースティック内の情報が古くなってしまうため、毎週月曜日午前6時に更新される最新データを取得してメモリースティック内のAP情報を更新する必要がある。（みんなの地図シリーズはインターネット接続されたパソコンを用いる必要があるが、X-rader potableはPSPから直接取り込みが可能）

### 位置を教える

PlaceEngineサーバーに現在地周辺のAP情報が登録されておらず位置が取得できない場合や、APの所有者が転居したなどの理由で測定位置が大幅にずれている場合には、位置情報を登録する必要がある。略して位置登録という。

位置登録は位置取得時と同様に電測を行い、その後地図上から自分の現在位置を示唆するか、GPSから取得した現在位置を送信することによって行う。AP情報未登録により位置測定ができなかった場合は、測定できなかった地点だけでなくその周囲数ヶ所の情報を登録することで、新規に発見したAPの位置測定制度が向上する。 現在位置の付随情報として、住所の他に、建物の名前や階数の入力ができる。登録の際もインターネットに接続できる環境を整えておく必要がある。

## 歴史

  - [2002年](../Page/2002年.md "wikilink")
      - 全国の政令都市よりスタート、[Windows XPパソコンで利用可能](../Page/Microsoft_Windows_XP.md "wikilink")
  - [2007年](../Page/2007年.md "wikilink")
      - [Mac](../Page/Macintosh.md "wikilink")、[Windows Vistaに対応](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")
      - [gooラボ](https://ja.wikipedia.org/wiki/gooラボ "wikilink")に対応
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")
      - [名古屋大学](../Page/名古屋大学.md "wikilink")の[名古屋市営地下鉄](../Page/名古屋市営地下鉄.md "wikilink")における無線LAN位置推定利用の実証実験のために技術協力
      - 地図情報検索サービス「[マピオン](https://ja.wikipedia.org/wiki/マピオン "wikilink")」のトップページがPlaceEngineに対応
      - [Skype](../Page/Skype.md "wikilink")で位置を交換するコミュニケーションツール「おともだちレーダーPlaceEngine for Skype」を公開
  - [2009年](../Page/2009年.md "wikilink")
      - [Windows 7に対応](../Page/Microsoft_Windows_7.md "wikilink")
      - ソニー[VAIO](../Page/VAIO.md "wikilink") XシリーズにPlaceEngine（GPS+Wi-Fiハイブリッド版）を搭載
      - PSPソフト「[みんなのナビ](https://ja.wikipedia.org/wiki/みんなのナビ "wikilink")」に搭載
  - [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")
      - ソニー VAIO Pシリーズ(2010年夏モデル以降)に搭載
  - [2011年](../Page/2011年.md "wikilink")
      - x-Radar ＜Xperia特別版＞にPlaceEngine技術を提供
  - [2012年](../Page/2012年.md "wikilink")
      - x-Radar Powered by PetaMapにPlaceEngine技術を提供

## 利用形態

PlaceEngineは現在、クウジット株式会社がライセンスを行っており、公式サイトよりダウンロードして使えるようになる。 その他、そのクライアントは多くのwebサイトやソフトに活用されている。

  - ウェブサイト
      - [Mapion](../Page/Mapion.md "wikilink")
      - [ペタマップ](../Page/ペタマップ.md "wikilink")
      - [ここから周辺検索](https://ja.wikipedia.org/wiki/ここから周辺検索 "wikilink")

<!-- end list -->

  - PCソフトウェア
      - [Skype](../Page/Skype.md "wikilink")

<!-- end list -->

  - [PlayStation Portable用PlaceEngine対応ソフト](../Page/PlayStation_Portable.md "wikilink")　　
      - [みんなの地図2](../Page/みんなの地図2.md "wikilink")（地域版も含む）
      - [みんなの地図3](https://ja.wikipedia.org/wiki/みんなの地図3 "wikilink")
      - [プロアトラストラベルガイド](https://ja.wikipedia.org/wiki/プロアトラストラベルガイド "wikilink")
      - [ニッポンのあそこで](https://ja.wikipedia.org/wiki/ニッポンのあそこで "wikilink")
      - [MAPLUS ポータブルナビ3](https://ja.wikipedia.org/wiki/MAPLUS_ポータブルナビ3 "wikilink")
      - [みんなのナビ](https://ja.wikipedia.org/wiki/みんなのナビ "wikilink")
      - [x-Radar Portable](https://ja.wikipedia.org/wiki/x-Radar_Portable "wikilink")

<!-- end list -->

  - [Android](../Page/Android.md "wikilink")用ソフトウェア
      - x-Radar Powered by PetaMap
      - [セカイカメラ](https://ja.wikipedia.org/wiki/セカイカメラ "wikilink")（現在は使用されていない）

<!-- end list -->

  - [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")用ソフトウェア
      - [セカイカメラ](https://ja.wikipedia.org/wiki/セカイカメラ "wikilink")（現在は使用されていない）
      - [Y\!地図](https://ja.wikipedia.org/wiki/Y!地図 "wikilink")（現在は使用されていない）

## 動作環境

  - [パソコン](../Page/パーソナルコンピュータ.md "wikilink")
      - [Microsoft Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") / [Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") / [7](../Page/Microsoft_Windows_7.md "wikilink") / [8](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")(確認中)
      - [Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink")
      - [Linux](../Page/Linux.md "wikilink")（法人向け）
  - ゲーム機
      - PSP/PSP go
  - スマートフォン
      - Android
      - iPhone
      - Windows Mobile
  - [Mylo](../Page/Mylo.md "wikilink")
  - [デジタルカメラ](../Page/デジタルカメラ.md "wikilink")
      - [ソニー・サイバーショット DSC-G1](https://ja.wikipedia.org/wiki/ソニー・サイバーショットシリーズ#G.E3.82.B7.E3.83.AA.E3.83.BC.E3.82.BA "wikilink")（期間限定ファームウェアアップグレード後）

## 関連項目

  - [スカイフック・ワイアレス](https://ja.wikipedia.org/wiki/スカイフック・ワイアレス "wikilink")

## 外部リンク

  - [PlaceEngine](http://www.placeengine.com/)
  - [ペタマップ](http://petamap.jp/)
  - [x-Radar Portable](http://petamap.jp/contents/radar/psp/)

[Category:PlaceEngine](https://ja.wikipedia.org/wiki/Category:PlaceEngine "wikilink")