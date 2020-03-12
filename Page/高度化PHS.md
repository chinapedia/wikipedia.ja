> この記事は[PHS](https://ja.wikipedia.org/wiki/PHS)から翻訳されています。


**高度化PHS**（こうどかピーエイチエス）とは、現行の[PHS](../Page/PHS.md "wikilink")規格の改良型である。高速[無線アクセス](../Page/無線アクセス.md "wikilink")システム的性能を持つ。

## 経緯

高度化PHSは、2000年前後当初より、旧[郵政省](../Page/郵政省.md "wikilink")・[総務省](../Page/総務省.md "wikilink")の情報通信審議会により提案され推進された、PHSの改良型の規格である。高度化PHSのための帯域も新たに割り当てられたが、実際に事業者レベルでの実装の実現を見るには、2006年2月23日の[ウィルコム](../Page/ウィルコム.md "wikilink")（現：[ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")の[Y\!mobile](https://ja.wikipedia.org/wiki/Y!mobile "wikilink")部門）による[W-OAM](../Page/W-OAM.md "wikilink")のサービス開始まで待つ必要があった。

推進・事業化のいずれも、現状は[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")国内に限られている。

### 略歴

[thumb](https://ja.wikipedia.org/wiki/画像:ウィルコムPHS高度化対応アンテナ基地局_2007年.jpg "wikilink")

  - [2001年](../Page/2001年.md "wikilink")[6月25日](../Page/6月25日.md "wikilink")
    [総務省](../Page/総務省.md "wikilink")・技術的条件の告示（PHSの高度利用及び周波数有効利用の促進に向けて\[1\]）。

  - [2002年](../Page/2002年.md "wikilink")[7月25日](../Page/7月25日.md "wikilink")発表資料
    メーカー[三洋電機](../Page/三洋電機.md "wikilink")の実験機によるフィールドテスト。

  - [2005年](../Page/2005年.md "wikilink")

:; [2月](https://ja.wikipedia.org/wiki/2月 "wikilink")

:: [ウィルコム](../Page/ウィルコム.md "wikilink")による、8PSKを採用した高度化PHSのアナウンス。

:; 7月

  -

      -
        京セラ製高度化対応基地局の出荷、設置工事を開始\[2\]。

  - 2006年2月23日
    ウィルコムによる[W-OAM](../Page/W-OAM.md "wikilink")サービス開始。

  - 2007年12月
    京セラ製光回線IP化高度化PHS基地局を、量産開始\[3\]。

## 技術

*PHSの基本的な技術的仕様については、[PHS](../Page/PHS.md "wikilink")の項も参照。*

現状のPHS規格では、[TDMA](https://ja.wikipedia.org/wiki/時分割多元接続 "wikilink")/[TDDの](https://ja.wikipedia.org/wiki/時分割複信 "wikilink")1スロット32k[bps](../Page/ビット毎秒.md "wikilink")（1通話スロットあたりのトラフィックチャネル（通話チャネル）のデータレート）となっている。

2001年6月25日の総務省情報通信審議会の答申に基づく、ユーザーレートで最大1Mbps程度の高速データ伝送速度を可能にする技術的条件の告示（PHSの高度利用及び周波数有効利用の促進に向けて\[4\]）における技術的条件では、[変調方式を最大](../Page/デジタル変調.md "wikilink")32[QAM](https://ja.wikipedia.org/wiki/直交振幅変調 "wikilink")、トラフィックチャネルの周波数帯域幅を最大884kHz（現行の3倍幅）、更にロールオフ率やスロット構成の変更などが示された。

高度化PHS用の新たな[周波数](../Page/周波数.md "wikilink")帯域（1884.65 - 1893.35MHz、現行PHS帯域の低い側に隣接）の免許が割り当てられ、実際にメーカー[三洋電機](../Page/三洋電機.md "wikilink")の実験機によるフィールドテストも行われた（[2002年](../Page/2002年.md "wikilink")[7月25日](../Page/7月25日.md "wikilink")発表資料）。この実験では適応変調方式（最大16QAMから最低π/4 DQPSK）が使われ、現行PHSから[変調方式のみを高度化した](../Page/デジタル変調.md "wikilink")「タイプ1」の高度化、更に加えてトラフィックチャネル3倍幅・ロールオフ率やスロット構成の変更をする「タイプ2」の高度化の、実証実験がなされた。

しかしそれ以降、PHSが一時期、いわゆる「冬の時代」を迎え、高度化PHSのサービス実用化展開は停滞するに至った。[2005年](../Page/2005年.md "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")、[ウィルコム](../Page/ウィルコム.md "wikilink")が最大256kbpsの「8xパケット方式」（現行PHS方式で最大8リンクを束ねる《8x/2RF》）をサービス開始したのに伴って、ようやく、変調方式としてD8PSKを採用し最大384kbps程度のスループットを実現する高度化PHS（前記「タイプ1」）の採用計画が、ウィルコムよりアナウンスされた。

PHSの技術基準の改正について、2005年10月21日意見の聴取\[5\]を行い、2005年11月9日、意見を決定\[6\]され、2005年12月1日から施行された。公衆PHSサービスに64QAM・256QAMの高能率変調方式を追加され、1チャンネル当たりの通信容量が、それぞれ96kbps・128kbpsとなり、4タイムスロット2周波で多重する場合には1Mbps以上の伝送速度を実現することが可能となった。制御チャンネルについて、簡易な変調方式π/2 DBPSKを追加するとともに空中線利得を現在の10dBiから15dBiに引上げ、到達範囲が拡大された。

そして、2006年2月23日に至りようやく、高度化PHS（[W-OAM](../Page/W-OAM.md "wikilink")）としてのサービス開始を見た。なお、最大スループット（理論値）はD8PSK/8x通信時において408kbpsとなり、[第三世代携帯電話](https://ja.wikipedia.org/wiki/第三世代携帯電話 "wikilink")・[W-CDMA](../Page/W-CDMA.md "wikilink")方式の標準的な最大スループット384kbpsを理論値において上回った。

ウィルコムは将来的には、16 - 64QAMで最大16スロットを束ね《16x/4RF》、最大1.5Mbpsの計画があるとしている。

なお、（2002年三洋電機フィールド実験における）「タイプ2」の高度化について事業化のアナウンスをしているPHS事業者はない。

高度化PHSにおいては、ビットレートを向上させる上記QAMやD8PSKの他にカバーエリアや屋内浸透度を向上させるπ/2 DBPSK（通常のπ/4 DQPSKの約1/2のレート）もあり、通信の状態に応じて変調方式を変化させる[適応変調](https://ja.wikipedia.org/wiki/適応変調 "wikilink")方式を採る。

一部[マスメディア](../Page/マスメディア.md "wikilink")で[京セラ](../Page/京セラ.md "wikilink")が主導する[iBurst](https://ja.wikipedia.org/wiki/iBurst "wikilink")が高度化PHSとして報道されているが、iBurst自体は[TDD](https://ja.wikipedia.org/wiki/時分割複信 "wikilink")-[TDMA方式を採用している事以外には](https://ja.wikipedia.org/wiki/時分割多元接続 "wikilink")、PHS・高度化PHSとの共通点は少なく、またその規格にも適合していない。

## PHS制御チャネル移行およびIMT-2000側のガードバンド

前述の2001年6月25日の総務省情報通信審議会の答申においては同時に、PHS帯と[IMT-2000](https://ja.wikipedia.org/wiki/IMT-2000 "wikilink")帯域（日本における[第3世代移動通信システム](../Page/第3世代移動通信システム.md "wikilink")用の帯域、2.0GHz帯）との干渉問題の解決のためPHSの公衆用共通制御キャリア（BCCH、単に制御チャネルとも呼ばれる）を低い周波数の方にずらす対策を取る事も示された。*詳細は[PHS\#制御チャネル移行およびIMT-2000側のガードバンド](https://ja.wikipedia.org/wiki/PHS#制御チャネル移行およびIMT-2000側のガードバンド "wikilink")を参照。*

これに伴い、[2012年](../Page/2012年.md "wikilink")[2月29日](../Page/2月29日.md "wikilink")に、DDIポケット時代に発売された該当する端末のほとんど（ウィルコムブランドの端末は、すべて制御チャネル移行後の周波数帯に対応している\[7\]）が使用停止とされ、同年[3月1日](../Page/3月1日.md "wikilink")以降、制御チャネル移行後の周波数帯による運用に完全移行される。

## 脚注

<references/>

## 出典・参考資料

  - [PHS高度化対応アンテナ拡大画像](http://k-tai.impress.co.jp/cda/parts/image_for_link/116212-28288-16-1.html) 第5回 ケータイ国際フォーラムに出品されたPHS高度化対応アンテナ画像

## 関連項目

  - [ウィルコム](../Page/ウィルコム.md "wikilink")
  - [W-OAM](../Page/W-OAM.md "wikilink")
  - [適応変調](https://ja.wikipedia.org/wiki/適応変調 "wikilink")
  - [PHS](../Page/PHS.md "wikilink")
  - [移動体通信](../Page/移動体通信.md "wikilink")：規格の比較

[Category:携帯電話_(PHS)](https://ja.wikipedia.org/wiki/Category:携帯電話_\(PHS\) "wikilink") [Category:携帯電話の通信規格](https://ja.wikipedia.org/wiki/Category:携帯電話の通信規格 "wikilink")

1.  [PHSの高度利用及び周波数有効利用の促進に向けて](http://www.soumu.go.jp/joho_tsusin/pressrelease/japanese/sogo_tsusin/010625_4.html)
2.  [2006年3月期 第1四半期 事業説明会（2005年8月4日実施）＜スライド43：国内PHS市場への取り組み＞](http://www.kyocera.co.jp/ir/presentations/pdf/speech0508.pdf)（pdf）
3.  [高度化PHS基地局（IP対応）の量産開始および次世代PHS基地局開発について 発表日：2007年11月09日](http://www.kyocera.co.jp/news/2007/1102.html)
4.
5.  [意見の聴取](http://www.soumu.go.jp/s-news/2005/051109_2.html)
6.  [意見を決定](http://www.soumu.go.jp/joho_tsusin/policyreports/denpa_kanri/051109_3.html)
7.  ただし、ウィルコムブランド初期の端末の中には、アップデートが必要な場合もある。