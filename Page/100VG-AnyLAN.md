> この記事は[100VG-AnyLAN](https://ja.wikipedia.org/wiki/100VG-AnyLAN)から翻訳されています。


**100VG-AnyLAN**（ひゃくブイジーエニィラン）は、過去に存在したコンピュータを接続する[ネットワークの規格のひとつである](../Page/コンピュータネットワーク.md "wikilink")。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に[IEEE 802.12で標準規格化された](https://ja.wikipedia.org/wiki/IEEE_802.12 "wikilink")100M[bpsの転送速度の](../Page/ビット毎秒.md "wikilink")[LANである](../Page/Local_Area_Network.md "wikilink")100VG-AnyLANは、10BASE-Tと同じカテゴリー3のアンシールデッド・[ツイステッド・ペア・ケーブル](../Page/ツイストペアケーブル.md "wikilink")（UTPケーブル）を使用して、[セグメント長は最大](https://ja.wikipedia.org/wiki/イーサネット#物理的構成 "wikilink")100mであった。

## 前身 100BASE-VG

1990年に[IEEE 802.3小委員会で](../Page/イーサネット.md "wikilink")10MbpsのLAN規格「10BASE-T」を正式承認した。2年間の準備期間の後、1992年から同じ802.3で100Mbpsの次期LAN規格の標準化作業が開始された。このIEEE 802.3小委員会に対して、米[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")社（HP社）が100VG-AnyLANの元となった100BASE-VGを提案した。

IEEE 802.3の規定したフレームは[100BASE-TX](https://ja.wikipedia.org/wiki/100BASE-TX "wikilink")と同じであるが、アクセス制御方式は100BASE-TXの[CSMA/CD](https://ja.wikipedia.org/wiki/CSMA/CD "wikilink")ではなく、全く新しい方式を採用した。当時のHP社によると、[CSMA/CD](https://ja.wikipedia.org/wiki/CSMA/CD "wikilink")方式では伝送路が混雑した場合に運の悪い[PCはいつまでたっても送信できないという弱点があるので](../Page/パーソナルコンピュータ.md "wikilink")、100BASE-VGでは平等にチャンスが与えられるように、[ハブが各ポートのPCに順番に送信要求がないか訊ねていくことで解決したとされている](../Page/ハブ_\(ネットワーク機器\).md "wikilink")。

また、100BASE-VGのケーブルは10BASE-Tと同じカテゴリー3の[UTPケーブルで済むため](../Page/ツイストペアケーブル.md "wikilink")、コスト的にも有利であると、HP社は主張していた。カテゴリー3のケーブルは、元々電話用の配線ケーブルであったため、100BASE-VGと100VG-AnyLANの「VG」はVoice Grade（音声品質）から付けられた。

## 改名 100VG-AnyLAN

1993年夏から100BASE-VGは、802.3小委員会から802.12小委員会へと協議の場が移され、当時、[トークン・リングを推進していた米](../Page/トークンリング.md "wikilink")[IBM](../Page/IBM.md "wikilink")社が100BASE-VGの規格案にトークン・リング・フレームの利用も追加する提案を行い承認された。これに合わせて、規格名称が100BASE-VGから100VG-AnyLANに変更された。新しい名称の「Any」にはさまざまなフレームが扱えるという意味が込められていた。

1995年にIEEE 802.12で100VG-AnyLANが標準規格として正式承認された。

## 勝敗

結局、100Mbpsの転送速度のLANでは、IEEEによる規格の一本化は出来ず、100BASE-TXと100VG-AnyLANの2つの規格が10BASE-Tの次期LAN製品の形で市場に問われることになった。

1990年代後半、100Mbpsの[LANスイッチ](../Page/スイッチングハブ.md "wikilink")（スイッチング・ハブ、L2スイッチ）の価格は、旺盛な一般のPCユーザーの需要に支えられて急速に低下してゆき、「10BASE-Tと100BASE-TXは混在環境でそのまま使えます。」という導入時のハードルが低かった事や、ネットワーク機器メーカーやPCメーカー、ソフトウェア・メーカーも、10BASE-Tからの変更に手間が掛からなかった事なども手伝ってすぐに店頭から100VG-AnyLANの製品は消えていった。つまり一言でいえば、10BASE-Tからの「上位互換性」が雌雄を決した。

100VG-AnyLAN陣営が問題としていた100BASE-TXの[CSMA/CD](https://ja.wikipedia.org/wiki/CSMA/CD "wikilink")による「弱点」は、実際には特定ポートの遅延は使用者から意識できるほどは発生せず、むしろネットーワーク全体の転送速度が問題として意識されていた。転送速度が問題となった初期には、常に価格が低下していたLANスイッチを買い足して、セグメントを分けることで速度の改善が図れたため、さらに安価な100BASE-TXが優位になり、体感できない程の公平な転送チャンスの割り振り機能の為に、数倍～十倍程度の高価格の100VG-AnyLAN製品を購入するユーザーは皆無となった。

## 動作

100VG-AnyLANに特徴的な動作を以下に説明する。

100VG-AnyLANは[CSMA/CD](https://ja.wikipedia.org/wiki/CSMA/CD "wikilink")方式のパケットの衝突（コリジョン）を避ける為に、LANスイッチ側から配下の各ポートに順番に送信要求がないかを訊ねてゆく。このため、ポートに接続されたPCは最悪でも一定時間だけ待てば確実に自分の送信の順番が回ってくるので、偶然に頼る[CSMA/CD](https://ja.wikipedia.org/wiki/CSMA/CD "wikilink")方式よりもネットワークとしての確実性は高まる。また、[伝送路](../Page/伝送路.md "wikilink")の混雑時には[CSMA/CD](https://ja.wikipedia.org/wiki/CSMA/CD "wikilink")方式のように衝突時に伝送路が使用されない時間の生じる割合が高まることはなくなるため、混雑時の伝送効率の向上が期待できる。

## 出典

  - 前田潤著 「温故知新 100VG-AnyLAN」 日経エレクトロニクス 2008年1月号 p.69

## 関連項目

  - [イーサネット](../Page/イーサネット.md "wikilink")
  - [100メガビット・イーサネット](../Page/100メガビット・イーサネット.md "wikilink")
  - [IEEE 802.3](../Page/イーサネット.md "wikilink")
  - [IEEE 802.5](https://ja.wikipedia.org/wiki/IEEE_802.5 "wikilink")

[Category:IEEE_802](https://ja.wikipedia.org/wiki/Category:IEEE_802 "wikilink") [Category:有線通信](https://ja.wikipedia.org/wiki/Category:有線通信 "wikilink")