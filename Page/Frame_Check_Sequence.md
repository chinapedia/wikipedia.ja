> この記事は[Frame Check Sequence](https://ja.wikipedia.org/wiki/Frame_Check_Sequence)から翻訳されています。


[Ethernet_frame.svg](https://ja.wikipedia.org/wiki/File:Ethernet_frame.svg "fig:Ethernet_frame.svg")の最後についている\[1\]。\]\] **frame check sequence**（フレームチェックシーケンス、**FCS**）とは、[通信プロトコル](../Page/通信プロトコル.md "wikilink")の[フレームに](https://ja.wikipedia.org/wiki/フレーム_\(ネットワーク\) "wikilink")[エラー検出のために付加されるコードである](../Page/誤り検出訂正.md "wikilink")。フレームは、送信元から送信先に[ペイロードを送信するために使用される](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")。

## 目的

フレームやその中に含まれる[ビット](../Page/ビット.md "wikilink")、[バイト](../Page/バイト_\(情報\).md "wikilink")、[フィールドは](../Page/フィールド_\(計算機科学\).md "wikilink")、様々な要因によるエラーの影響を受けやすい。FCSフィールドには、送信元においてフレーム内のデータに基づいて計算された数値が含まれている。この数値は、送信されるフレームの最後に追加される。宛先ノードでは、フレームを受信したとき、受信したフレーム内のデータに基づいて同じアルゴリズムでFCSの数値を再計算し、フレームに含まれるFCSの数値と比較する。2つの数値が異なる場合は、エラーとみなされ、フレームは破棄される。

FCSはエラー検出のみを提供する。エラー訂正は別の手段を使って実行する必要がある。例えば、[イーサネット](../Page/イーサネット.md "wikilink")の仕様では、破損したフレームは廃棄すべきであると規定されているが、フレームを再送させるための動作は規定されていない。[TCPなどの上位プロトコルにてデータの欠損が検出され](../Page/Transmission_Control_Protocol.md "wikilink")、再送とエラー訂正が行われる\[2\]。

## 実装

[Ethernet_Frame.png](https://ja.wikipedia.org/wiki/File:Ethernet_Frame.png "fig:Ethernet_Frame.png")の詳細な構造\]\] FCSは、受信側がフレームの最後のFCSを受信した時点で、フレーム全体の積算合計を計算できるような方法で送信されることが多い。イーサネットなどの[IEEE 802プロトコルでは](../Page/IEEE_802.md "wikilink")、データは最下位ビットが最初に送信され、FCSは最上位ビット（ビット31）が最初に送信されると標準で規定されている。代替的なアプローチは、反転したFCSもまた、最下位ビット（ビット0）を最初に送ることができるように、FCSのビット反転を生成することである。詳細は[イーサネットフレーム\#フレームチェックシーケンス](https://ja.wikipedia.org/wiki/イーサネットフレーム#フレームチェックシーケンス "wikilink")を参照。

## 種類

FCSのアルゴリズムで最もよく使用されるのは[巡回冗長検査](../Page/巡回冗長検査.md "wikilink")(CRC)である。32ビットのイーサネットやその他の[IEEE 802プロトコル](../Page/IEEE_802.md "wikilink")、16または32ビットの[X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")、16または32ビットの[HDLC](../Page/High-Level_Data_Link_Control.md "wikilink")、16ビットの[フレームリレー](../Page/フレームリレー.md "wikilink")\[3\]、16または32ビットの[Point-to-Point Protocol](../Page/Point-to-Point_Protocol.md "wikilink")(PPP)、およびその他の[データリンク層](../Page/データリンク層.md "wikilink")プロトコルで使用される。

[インターネットプロトコルスイート](https://ja.wikipedia.org/wiki/インターネットプロトコルスイート "wikilink")のプロトコルは、[チェックサム](../Page/チェックサム.md "wikilink")を使用する傾向がある\[4\]。

## 関連項目

  -
## 脚注

[Category:リンク層プロトコル](https://ja.wikipedia.org/wiki/Category:リンク層プロトコル "wikilink")

1.
2.  Cf: Wendell ODOM, Ccie \#1624, Cisco Official Cert Guide, Book 1, Chapter 3: Fundamentals of LANs, Page 74
3.
4.