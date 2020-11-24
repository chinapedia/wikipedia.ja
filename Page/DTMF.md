> この記事は[DTMF](https://ja.wikipedia.org/wiki/DTMF)から翻訳されています。


[200pxを送出する](https://ja.wikipedia.org/wiki/ファイル:Dialog_knappar_1969.jpg "wikilink")[押しボタン式電話機](../Page/押しボタン式電話機.md "wikilink")（日本国内での愛称は「プッシュホン」）\]\] **DTMF**（）は、0から9までの数字と、\*、\#、A、B、C、Dの記号の計16種類の符号を、低群・高群の2つの[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")[周波数](../Page/周波数.md "wikilink")帯域の合成信号音で送信する方法である。別名「**トーン信号**」 「**プッシュ信号**」「**PB信号**\[1\]」（PBは push button の略）とも呼ばれ、その信号音は人間の可聴域にあるため日本語では「**ピ、ポ、パ**」とも[擬音語](https://ja.wikipedia.org/wiki/擬音語 "wikilink")表記される。

プッシュ式[電話回線](../Page/電話回線.md "wikilink")での[電話番号](../Page/電話番号.md "wikilink")の送出、その他音声回線での数字入力（例・[コールセンター](../Page/コールセンター.md "wikilink")での着信後の項目選択）などで用いられる。

[ダイヤルパルス](../Page/ダイヤルパルス.md "wikilink")信号と比較して次の点が特徴である。

  - 情報伝達速度が速い。8数字/秒以上が可能である。
  - [ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")[通信線路](../Page/通信線路.md "wikilink")のみならず[多重化](../Page/多重化.md "wikilink")・[無線通信](../Page/無線通信.md "wikilink")回線でも使用可能である。

## 規格

規格としては、[ITU-T](../Page/ITU-T.md "wikilink")勧告Q.24\[2\]、日本では[総務省](../Page/総務省.md "wikilink")令 [端末設備等規則](https://ja.wikipedia.org/wiki/端末設備等規則 "wikilink")第12条第2号に基づく別表第2号に、押しボタンダイヤル信号の条件として規定されている。

<table>
<caption>DTMFマトリックス</caption>
<thead>
<tr class="header">
<th><p> </p></th>
<th><p>高群 (Hz)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1209</p></td>
<td><p>1336</p></td>
</tr>
<tr class="even">
<td><p><br />
(Hz)</p></td>
<td><p>697</p></td>
</tr>
<tr class="odd">
<td><p>770</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>852</p></td>
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p>941</p></td>
<td><p>*</p></td>
</tr>
</tbody>
</table>

左の表より、例えば"1"は697Hzと1209Hzの2つの音声信号の合成音によって表される。その他の符号も同様である。 {{-}}

通常、0から9までと\*・\#が使われる。このマトリックスに沿って、低群・高群それぞれから1周波数ずつの[正弦波](../Page/正弦波.md "wikilink")が用いられる。音声伝送回路にて伝送するため、全ての周波数は[可聴帯域](https://ja.wikipedia.org/wiki/可聴帯域 "wikilink")内に収まっている。耳に聞こえるDTMFは、2種類の正弦音波の合成音である。

### その他の規格

  - 信号周波数偏差
    信号周波数の±1.5%以内
  - 信号送出電力
    絶対レベルで表した値。Lは、[電気通信事業者](../Page/電気通信事業者.md "wikilink")交換設備から端末設備の接続点までの1,500Hzにおける[通信線路](../Page/通信線路.md "wikilink")伝送損失。
      - 低群周波数
        (-16.5+0.8L)dB以上・ (-6.5+0.8L)dB以下で、かつ-3.5dBを超えない信号
      - 高群周波数
        (-16.0+L)dB以上・ (-6.5+L)dB以下で、かつ-2.5dBを超えない信号
  - 信号送出時間
    50ms以上
  - ミニマムポーズ
    隣接する信号間の休止時間の最小値。30ms以上
  - 周期
    信号送出時間とミニマムポーズの和。120ms以上

## 関連機器

電話機側音声回路の送話器（[マイクロフォン](../Page/マイクロフォン.md "wikilink")）と[音響接続して](../Page/音響カプラ.md "wikilink")、DTMF信号を送出する**DTMFダイヤラー**と呼ばれる機器がある。信号音を発音する小型[スピーカー](../Page/スピーカー.md "wikilink")を持ち、送話器に密着させて使用する。家庭用[留守番電話](../Page/留守番電話.md "wikilink")機の普及黎明期に、外出先のダイヤル式[公衆電話](../Page/公衆電話.md "wikilink")などから録音機能（再生、消去など）の[遠隔操作](../Page/遠隔操作.md "wikilink")に用いられた。あるいは電子住所録から自動ダイヤルする目的で、[電子手帳](../Page/電子手帳.md "wikilink")や多機能デジタル[腕時計](../Page/腕時計.md "wikilink")に内蔵されたこともある。また、DTMF信号を復号し視覚化する解読器もある。

## 開発の経緯

DTMFは、[1950年代](../Page/1950年代.md "wikilink")後半に[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の[ベル研究所](../Page/ベル研究所.md "wikilink")で、回線の断続によって信号を伝送できない[無線通信](../Page/無線通信.md "wikilink")や[多重化](../Page/多重化.md "wikilink")回線で[電話番号](../Page/電話番号.md "wikilink")情報を伝送する技術として開発された。ダイヤルパルス信号（規則的な回線断続信号）を加入者[電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")でDTMFに変換し音声信号として個別線信号方式で伝送していた。

[1960年代](../Page/1960年代.md "wikilink")には、電子素子の発達により[プッシュホンなど](../Page/押しボタン式電話機.md "wikilink")[電話機](https://ja.wikipedia.org/wiki/電話機 "wikilink")の信号方式の一種となり、[ダイヤルパルス](../Page/ダイヤルパルス.md "wikilink")信号との併用が始まった。プッシュホン加入者が[電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")の拡張機能（[短縮ダイヤル](https://ja.wikipedia.org/wiki/短縮ダイヤル "wikilink")など）を使用する操作にも利用されはじめ、操作の際は[受話器](https://ja.wikipedia.org/wiki/受話器 "wikilink")（ハンドセット）を耳に当てたままであることからDTMF音が聞こえ、「ピ、ポ、パ」と擬音化されるまでに一般に浸透した。

## 備考

音声信号であるので電子機器でなくてもよく、[音叉](../Page/音叉.md "wikilink")や[笛](../Page/笛.md "wikilink")などで回線に乗せて発信させることもできる。

[日本テレビ系番組](../Page/日本テレビ放送網.md "wikilink")『[投稿\!特ホウ王国](../Page/投稿!特ホウ王国.md "wikilink")』では、このDTMFの周波数と同じ[声](../Page/声.md "wikilink")が出せる[姉妹](../Page/姉妹.md "wikilink")が出演し、[時報の電話サービス](https://ja.wikipedia.org/wiki/時報#電話 "wikilink")（117番）に電話をかけるという企画があった。[TBSテレビ](../Page/TBSテレビ.md "wikilink")の番組でも同じ趣旨の実験をしたが\[3\]、こちらは技術的な知識の欠如からDTMFを[平均律](../Page/平均律.md "wikilink")音階で解釈したため、実際の接続動作までに数時間を要した\[4\]。

2008年公開のアニメ映画『[名探偵コナン 戦慄の楽譜](../Page/名探偵コナン_戦慄の楽譜.md "wikilink")』では、登場人物が声によって警察通報用電話（[110番](../Page/110番.md "wikilink")）にかけるシーンがある。また、2009年放送のバラエティ番組『[探偵\!ナイトスクープ](../Page/探偵!ナイトスクープ.md "wikilink")』ではこのシーンが実際に可能なのかを実験し、[大阪音楽大学](../Page/大阪音楽大学.md "wikilink")の学生2人が声によって[時報電話サービス（117番）に電話をかけることに成功した](https://ja.wikipedia.org/wiki/時報#時報の媒体（戦後の運用） "wikilink")。詳細は[名探偵コナン 戦慄の楽譜\#プッシュホンの設定を参照](https://ja.wikipedia.org/wiki/名探偵コナン_戦慄の楽譜#プッシュホンの設定 "wikilink")。

## 音声

[File:Dtmf1.ogg|1](File:Dtmf1.ogg%7C1) [File:Dtmf2.ogg|2](File:Dtmf2.ogg%7C2) [File:Dtmf3.ogg|3](File:Dtmf3.ogg%7C3) [File:Dtmf4.ogg|4](File:Dtmf4.ogg%7C4) [File:Dtmf5.ogg|5](File:Dtmf5.ogg%7C5) [File:Dtmf6.ogg|6](File:Dtmf6.ogg%7C6) [File:Dtmf7.ogg|7](File:Dtmf7.ogg%7C7) [File:Dtmf8.ogg|8](File:Dtmf8.ogg%7C8) [File:Dtmf9.ogg|9](File:Dtmf9.ogg%7C9) [File:Dtmf0.ogg|0](File:Dtmf0.ogg%7C0) <File:DtmfStar.ogg>|\* <File:Dtmf-.ogg>|\# [File:DtmfA.ogg|A](File:DtmfA.ogg%7CA) [File:DtmfB.ogg|B](File:DtmfB.ogg%7CB) [File:DtmfC.ogg|C](File:DtmfC.ogg%7CC) [File:DtmfD.ogg|D](File:DtmfD.ogg%7CD)

## 脚注

## 関連項目

  - [押しボタン式電話機](../Page/押しボタン式電話機.md "wikilink")
  - [デジタル変調](../Page/デジタル変調.md "wikilink")

[Category:電話の信号](https://ja.wikipedia.org/wiki/Category:電話の信号 "wikilink") [Category:電子音源の合成方式](https://ja.wikipedia.org/wiki/Category:電子音源の合成方式 "wikilink")

1.  文部科学省検定教科書『電子技術』、高等学校工業用、平成25年3月1日 検定版、平成29年1月25日 発行、
2.  [Q.45 : Transmission characteristics of an analogue international exchange](http://www.itu.int/rec/T-REC-Q.45-198410-I/en) (ITU-T Recommendations)
3.  [『見物人の集まる実験室オモシロ科学マジック50連発スペシャル』](https://archive.is/BiGi)（2005年7月13日放送、[TBSテレビ](../Page/TBSテレビ.md "wikilink")）
4.  低群周波数の852Hzは平均律のイ (A：880Hz)、高群周波数の1209Hzは平均律のニ (D6：1174.659Hz) と、それぞれ1半音の約半分の差がある。