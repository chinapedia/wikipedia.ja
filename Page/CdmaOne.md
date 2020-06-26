> この記事は[CdmaOne](https://ja.wikipedia.org/wiki/CdmaOne)から翻訳されています。


**cdmaOne**（シーディーエムエーワン）は、[米国クアルコム社が開発し](../Page/クアルコム.md "wikilink")1995年に発表した通信技術である。多重化に[CDMA方式を用いている](https://ja.wikipedia.org/wiki/Code_Division_Multiple_Access "wikilink")。TIAの規格名称は**IS-95**。

## 概要

[PDC](../Page/PDC.md "wikilink")や[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")と比べより新しい方式である。その間の技術進歩により、音質が良く高速なデータ通信ができる。現在の第3世代携帯電話[W-CDMA](../Page/W-CDMA.md "wikilink")や[CDMA2000](../Page/CDMA2000.md "wikilink")とcdmaOneは、CDMA方式を利用する点が共通する。このことから、**[2.5世代](../Page/第2世代移動通信システム.md "wikilink")**とも言われている。

[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")、[韓国](../Page/大韓民国.md "wikilink")、[香港](https://ja.wikipedia.org/wiki/香港 "wikilink")のほか、[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")、[メキシコ](../Page/メキシコ.md "wikilink")、[イスラエル](../Page/イスラエル.md "wikilink")と[ベネズエラ](../Page/ベネズエラ.md "wikilink")で普及している。

日本国内では、[IDOと](../Page/日本移動通信.md "wikilink")[DDIセルラーグループ](../Page/DDIセルラーグループ.md "wikilink")各社（現・[au](../Page/Au_\(携帯電話\).md "wikilink")（[KDDI](../Page/KDDI.md "wikilink")・[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")[連合](https://ja.wikipedia.org/wiki/連合 "wikilink")））が導入したものの、後継の[CDMA 1X](../Page/CDMA_1X.md "wikilink")（当初は[CDMA2000 1x](../Page/CDMA2000_1x.md "wikilink")）に移行している。

## 技術

### レイク受信

レイク (rake) 受信とは、[マルチパス](../Page/マルチパス.md "wikilink")による[フェージング](../Page/フェージング.md "wikilink")への対策として開発された技術。複数のサブ受信機を使い、別々に[デコード](https://ja.wikipedia.org/wiki/デコード "wikilink")する。各受信機の位相差を検出・補正し再合成する事により、マルチパス環境下においても[S/N比](https://ja.wikipedia.org/wiki/S/N比 "wikilink")の良好な受信を実現する。

この、レイク受信は[携帯電話](../Page/携帯電話.md "wikilink")や[無線LAN](../Page/無線LAN.md "wikilink")で用いられている。

cdmaOneでは、通信中、自セルの[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")以外に、隣接セルの基地局からの電波が受信できる場合は、レイク受信により電波を同時受信できるため、[フェージング](../Page/フェージング.md "wikilink")に強く切れにくいなどの特徴をもつ。但し、レイク受信できるのは周辺セルの基地局からの電波に限られるため、遠く離れたセルからの電波が受信される環境では妨害波を受けたのと同じであり、切れやすくなる。また、実際の電波環境は非常に過酷であるため、レイク受信がいつも成功するわけではなく、失敗すれば切れやすくなる。

### パワーコントロール

CDMAでは各移動局が同一周波数で被せて送信するため、[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")から見て強い局や弱い局があると、電波の遠近問題により、弱い局が強い局につぶされて基地局では弱い局が受信できなくなる（スペクトル拡散は、このような状態でも逆拡散で受信可能というのは誤解である）。そこで、基地局から強い局に対して送信パワーを下げろと言う指示を飛ばし、弱い局に対して送信パワーを上げろと言う指示を飛ばし、結果的にすべての局は、同じ強さとなって基地局で受信される。同じ強さであれば、被っていても逆拡散により、受信可能である。パワーコントロールは一番弱い局に合わされるため、通常、移動局の送信パワーの平均は、[PHS](../Page/PHS.md "wikilink")よりも小さくなる。クアルコムの[ギルハウゼン](https://ja.wikipedia.org/wiki/ギルハウゼン "wikilink") (Klein Gilhousen) によって実用化された。

### ソフトハンドオフ

ソフトハンドオフとは、現在通信中の基地局（ハンドオフ元）と新しく通信したい基地局（ハンドオフ先）を一時的に同時通信状態にした後、切り替えるハンドオフのことである。穏やか（ソフト）に切り替わっていくことからソフトハンドオフと呼ばれる。PDC方式など従来方式では、2組以上の送受信機を内蔵しないとソフトハンドオフは不可能であったので、実用化されなかった。cdmaOneの場合、ハンドオフ元もハンドオフ先も同一周波数であるので、単一の送受信機でハンドオフ元とハンドオフ先が同時に通信できる。そのため実用化できた。

cdmaOneにおいて、PDC方式の周波数の概念に相当するのがPNオフセット番号（PN位相）である。cdmaOneではハンドオフ元が使っているPNオフセット番号の信号とハンドオフ先が使っているPNオフセット番号の信号を一時的に同時通信状態にすることでソフトハンドオフを実現している。ソフトハンドオフは、一種のサイト[ダイバーシティ](../Page/ダイバーシティ.md "wikilink")でもあるので、ハンドオフの失敗が少ないと言われている。なお、PNオフセット番号は[相対値](https://ja.wikipedia.org/wiki/相対値 "wikilink")であり、その基準となるのは[GPSの時間である](../Page/グローバル・ポジショニング・システム.md "wikilink")（そのため同期式と呼ばれる）。通話しながら、地上から地下に移動した際、どちらもcdmaOneがサービスされているにもかかわらず、ハンドオフできずに切れるのは、地下局にGPSが実装されていないためである。

なお、PNオフセット番号は0～511までの有限の値であるため、重複しないように各基地局に割り当てる必要がある。

## プロトコル

IS-95 (Interim Standard 95, [TIA](https://ja.wikipedia.org/wiki/Telecommunications_Industry_Association "wikilink")) の規格上の用語。

  - P_REV (Protocol Revision)
      - P_REV =1
          - [ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink") J-STD-008, 1995
      - P_REV =2
          - IS-95A
      - P_REV =3
          - Technical Services Bulletin 74 (TSB-74)
      - P_REV =4
          - Interim Standard 95B (IS-95B) Phase I,
      - P_REV =5
          - Interim Standard 95B (IS-95B)
      - P_REV =6
          - [CDMA2000](../Page/CDMA2000.md "wikilink")

## 注

## 関連項目

  - [符号分割多元接続](../Page/符号分割多元接続.md "wikilink") (CDMA)
  - [標本化定理](../Page/標本化定理.md "wikilink")

[Category:携帯電話の通信規格](https://ja.wikipedia.org/wiki/Category:携帯電話の通信規格 "wikilink")