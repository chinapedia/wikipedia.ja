> この記事は[Asynchronous Transfer Mode](https://ja.wikipedia.org/wiki/Asynchronous_Transfer_Mode)から翻訳されています。


**Asynchronous Transfer Mode**（アシンクロナス トランスファー モード、非同期転送モード、**ATM**）は、53バイトの固定長のデータであるセルを基本的な通信の単位とする、[Virtual Circuit](https://ja.wikipedia.org/wiki/Virtual_Call "wikilink") cell relay（[仮想回線](https://ja.wikipedia.org/wiki/仮想回線 "wikilink")セルリレー）による[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

## 解説

[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")よりも[電気通信](../Page/電気通信.md "wikilink")の業界の既存技術・発想をもとに標準化され、グローバルな通信網からプライベートな[LANまでを統合しATMに置き換えようと広範囲に渡って準備がなされた](../Page/Local_Area_Network.md "wikilink")。

設計当初のATMは、次世代の高速網に適したものとなっており、1M[bps以下の回線速度では](../Page/ビット毎秒.md "wikilink")、充分なメリットが出ないばかりか、512kbpsの回線速度になると通信サービス品質そのものに影響するほどであった。ATM黎明期における国内でのATM応用用途は、512k回線に32チャネル分の音声帯域を確保することなどであり、本格的なデータ通信用途の需要には程遠い状態であった。90年代半ばには次世代高速ISDN (B-ISDN) として期待されたが、当時の日本国内の大手キャリアは512kbpsで充分な特性の出ない製品を仕様外として排除したため、日本市場をアテにしていた海外ベンダは、一気に体力が失せることとなった。加えて、ATMスイッチが高価で一般家庭には普及できず、ATMフォーラムでの仕様策定が遅れに遅れたり、開発のコアとなる技術者がL3スイッチベンダに行ってしまったり、そのうちに100BASE-TXの普及や1000BASEのめどがついてくると、ATMフォーラムは一時壊滅状態となった。

当初の意図に反し、非常に複雑な技術になってしまったため、ATMは次世代の主流にならず限定的に使用された。

ATMの設計思想は、[MPLSへと引き継がれ](../Page/Multi-Protocol_Label_Switching.md "wikilink")、汎用のレイヤ2のパケットスイッチングのプロトコルとして、[ルーター](../Page/ルーター.md "wikilink")を介した[IPの通信網で利用されている](../Page/Internet_Protocol.md "wikilink")。

## ATM方式の利用

速度保証を謳ったキャリアサービスのほとんどは、ATMバックボーンがベースとなっている。[ADSL](../Page/ADSL.md "wikilink")などの[DSLでも多重化のために広く用いられており](../Page/デジタル加入者線.md "wikilink")、この分野については実用上のニーズに良く適合したと言える。また、速度の異なる回線を一本の物理回線に多重化できる利点を生かして[W-CDMA](../Page/W-CDMA.md "wikilink")などの方式携帯電話のバックボーンにも用いられている。

## セルを使う理由

小さなデータのセルを使うことの目的は、データストリームの多重化において発生するジッタ（遅延の揺らぎ）を軽減することにある。

ATMはもともと音声信号のサポートに重点が置かれている。音声信号は遅延に敏感なため（人間の耳で許容できるのは20～30ms程度といわれる）、セルの組み立て（および復元）によるタイムロスを減らすにはペイロードが小さいほどよい。一方大容量データ（テレビ電話など）を扱うにはペイロードが大きいほどよい。この点でヨーロッパ案の32オクテットとアメリカ案の64オクテットの折衷でペイロードが48オクテットに決定された。

ATMが設計された時点では、155Mbps SDH（実データ135Mbps）は高速な光ファイバー通信とみなされ、 数多くのPDH接続は米国では1.544Mbps から 45Mbps程度の非常に遅いネットワークであった（ヨーロッパでは2Mbpsから 34Mbps）。

この速度では、最も長いパケットとなる1,500バイト（12,000ビット）のデータの送信には89マイクロ秒を要する。 1.544Mbpsの一次群速度回線などの遅い方の接続の場合は同じデータを送信するのに7.8ミリ秒を要する。

## ATM網

ATMは、既存の一般[電話網](../Page/電話網.md "wikilink") (PSTN)・デジタルハイアラーキ（[PDH](../Page/Plesiochronous_Digital_Hierarchy.md "wikilink")・SONET/[SDH](../Page/Synchronous_Digital_Hierarchy.md "wikilink")）・[パケット通信](../Page/パケット通信.md "wikilink")（データ長が可変の[IP](../Page/Internet_Protocol.md "wikilink")、[フレームリレー](../Page/フレームリレー.md "wikilink")）を統合する、複数レベルの[QoSをサポートする高速サービス総合デジタル網](../Page/Quality_of_Service.md "wikilink") (B-[ISDN](../Page/ISDN.md "wikilink")) の実現を目的としていた。[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")でいうところの物理層（第1層）から、データリンク層（第2層）、ネットワーク層（第3層）までの標準規格を提供している。当初155Mbps（実データ部135Mbps）として設計され、600Mbps近くまで提供されている。

## ATMの仕組み

ATMは回線交換方式とパケット方式両方の長所を取り入れている。データをセルに組み立てる点では[パケット](../Page/パケット.md "wikilink")方式に似ているが、ATMセルは[イーサネット](../Page/イーサネット.md "wikilink")パケットとは違い固定長であるためセルの先頭を識別することが容易であり、宛先をハードウェアで処理することで交換機内でのタイムロスを減らしている。

なお、回線交換方式のように回線を占有することは無い。

回線交換とパケット交換の方式間の特性差を解消するため、データは仮想回線識別子の付いた53オクテット固定長の**セル**（5オクテットはヘッダー、48オクテットはペイロード）に割り付けられて送出される。高ビットレートの情報はセルを多く送り、低ビットレートの情報はセルを少なくして送るので回線を有効に利用できる。

ATMは上位層との整合のためにデータリンク層に副層が設けられており、[ATM 適合層](https://ja.wikipedia.org/wiki/ATM_適合層 "wikilink") (ATM Adaptation Layer : AAL) といわれる。上位層（主にTCP/IP）をペイロードに組み立てる方法に応じ[AAL1から](https://ja.wikipedia.org/wiki/ATM_適合層 "wikilink")[AAL5までの](https://ja.wikipedia.org/wiki/ATM_適合層 "wikilink")4種類が存在するが（AAL3と4は統合された）、現在使われているのは主にAAL5である。AAL5はATMの長所を生かすために紛失セルの再送要求は行なわず、上位層が紛失セル（もしくはパケット）を処理する。

[AAL5は同期を必要としないが](https://ja.wikipedia.org/wiki/ATM_適合層 "wikilink")、実際の運用ではATM網全体で同期を取っている。つまりここでの非同期というのはセルの送出についてであって、キャリアとなっている低レベルのビットストリームのことではない。

### ATM セルの構造

ATMセルは5オクテットのヘッダーと48オクテットのペイロードから構成される。ペイロードのサイズは("[セルを使う理由](https://ja.wikipedia.org/wiki/#セルを使う理由 "wikilink")")に記述されている理由で48オクテットが選ばれた。

ATMでは2種類の異なるセルの規格が制定されている: [NNI](https://ja.wikipedia.org/wiki/網・網インタフェース "wikilink") (Network-Network Interface)と[UNI](https://ja.wikipedia.org/wiki/ユーザ・網インタフェース "wikilink") (User-Network Interface)である。大半のATMリンクはUNIセルフォーマットを使用する。

<table>
<tbody>
<tr class="odd">
<td><p><strong>UNI ATM セルの図</strong></p>
<table>
<tbody>
<tr class="odd">
<td><p>7</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
<td><p>4<br />
</p></td>
<td><p>3<br />
</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
<td><p>0<br />
</p></td>
</tr>
<tr class="even">
<td><p>GFC</p></td>
<td><p>VPI<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>VPI<br />
</p></td>
<td><p>VCI<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>VCI<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>VCI</p></td>
<td><p>PT</p></td>
<td><p>CLP<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>HEC</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><br />
<br />
<br />
<br />
ペイロードと必要なパッディング(48オクテット)<br />
<br />
<br />
<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table></td>
<td><p><strong>NNI ATM セルの図</strong></p>
<table>
<tbody>
<tr class="odd">
<td><p>7</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
<td><p>4<br />
</p></td>
<td><p>3<br />
</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
<td><p>0<br />
</p></td>
</tr>
<tr class="even">
<td><p>VPI<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>VPI<br />
</p></td>
<td><p>VCI<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>VCI<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>VCI</p></td>
<td><p>PT</p></td>
<td><p>CLP<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>HEC</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><br />
<br />
<br />
<br />
ペイロードと必要なパッディング(48オクテット)<br />
<br />
<br />
<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

  - GFC:汎用フロー制御
  - VPI:仮想パス識別子
  - VCI:仮想チャネル識別子
  - PT:ペイロードタイプ
  - CLP:輻輳損失プライオリティ
  - HEC:エラー制御

## 脚注

## 関連項目

  - [トラフィックシェーピング](../Page/トラフィックシェーピング.md "wikilink")

## 外部リンク

  - [ATMフォーラム（英語）](http://www.mfaforum.org/)

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")