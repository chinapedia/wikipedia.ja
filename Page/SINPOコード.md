> この記事は[SINPOコード](https://ja.wikipedia.org/wiki/SINPOコード)から翻訳されています。


**SINPOコード**（シンポ-）とは、[BCL](../Page/BCL.md "wikilink")の受信報告において用いられる、[電波](../Page/電波.md "wikilink")の受信状態を表現する[コード](https://ja.wikipedia.org/wiki/コード_\(暗号\) "wikilink")。

## 概説

SINPOコードは、ITUにより受信状態を記述する分類としてITU-R SM.1135 で使用を勧告されているコードである。 具体的な表現は下記の通り。

| 格付け             | 信号の強さ        | [混信](../Page/混信.md "wikilink") | 雑音                      | 伝播障害           | 総合評価   |
| --------------- | ------------ | ------------------------------ | ----------------------- | -------------- | ------ |
| Signal Strength | Interference | Noise                          | Propagation Disturbance | Overall Rating |        |
| 5               | 極めて強い        | なし                             | なし                      | なし             | 極めて良い  |
| 4               | 強い           | 少しある                           | 少しある                    | 少しある           | よい     |
| 3               | 中位           | 中位                             | 中位                      | 中位             | 中位     |
| 2               | 弱い           | 強い                             | 強い                      | 強い             | 悪い     |
| 1               | 辛うじて聞こえる     | 極めて強い                          | 極めて強い                   | 極めて強い          | 使用出来ない |

※[ヒト](../Page/ヒト.md "wikilink")の耳を用いた体感表現である為、絶対的なものではなく個人差はある。

使用に当たっては表現にいくつかの条件がある。[日本BCL連盟](https://ja.wikipedia.org/wiki/日本BCL連盟 "wikilink")が唱えたものによれば

  - Oが5であれば前4項の評価も当然5である
  - Oが4以下の場合は、前4項のうち最低評価になった原因に準じる

などがあるという事である。

また、SINPOコードの簡略表現として「SIOコード」というものがある。しかし、資料によって格付けが3段階、5段階、6段階評価だったりとバラバラで、表現の共通認識が醸成されているとは言い難く、公的に使用する場合は留意が必要である。止むを得ず受信報告書等に使用する場合は、（例えば、[放送局](../Page/放送局.md "wikilink")が専用受信報告書用紙を発行することが有り、それにSIOコードの使用が指定されている場合などがある）「3段階評価（2 - 4）」「5段階評価（1 - 5）」「6段階評価（0 - 5）」などと注釈を付けると無難であろう。

逆に、SINPOコードより細かい表現として、一般的ではないが「SINPFEMOコード」というものがある（国際電気通信条約附属[無線通信規則](https://ja.wikipedia.org/wiki/無線通信規則 "wikilink")付録第15号、国際無線通信諮問委員会勧告第251号）。こちらは以下の通り。

<table>
<thead>
<tr class="header">
<th><p>格付け</p></th>
<th><p>信号の強さ</p></th>
<th><p>混信</p></th>
<th><p>雑音</p></th>
<th><p>伝播障害</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/フェージング" title="wikilink">フェーディング周期</a></p></th>
<th><p>変調の質</p></th>
<th><p>変調の深度</p></th>
<th><p>総合評価</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Signal Strength</p></td>
<td><p>Interference</p></td>
<td><p>Noise</p></td>
<td><p>Propagation Disturbance</p></td>
<td><p>Fading Cycle</p></td>
<td><p>Emission</p></td>
<td><p>Moduration level</p></td>
<td><p>Overall Rating</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>極めて強い</p></td>
<td><p>なし</p></td>
<td><p>なし</p></td>
<td><p>なし</p></td>
<td><p>なし</p></td>
<td><p>極めて良い</p></td>
<td><p>最大</p></td>
<td><p>極めて良い</p></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p>強い</p></td>
<td><p>少しある</p></td>
<td><p>少しある</p></td>
<td><p>少しある</p></td>
<td><p>遅い</p></td>
<td><p>よい</p></td>
<td><p>深い</p></td>
<td><p>よい</p></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td><p>中位</p></td>
<td><p>中位</p></td>
<td><p>中位</p></td>
<td><p>中位</p></td>
<td><p>中位</p></td>
<td><p>中位</p></td>
<td><p>中位</p></td>
<td><p>中位</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>弱い</p></td>
<td><p>強い</p></td>
<td><p>強い</p></td>
<td><p>強い</p></td>
<td><p>速い</p></td>
<td><p>悪い</p></td>
<td><p>浅い<br />
掛かっていない</p></td>
<td><p>悪い</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>辛うじて聞こえる</p></td>
<td><p>極めて強い</p></td>
<td><p>極めて強い</p></td>
<td><p>極めて強い</p></td>
<td><p>非常に速い</p></td>
<td><p>非常に悪い</p></td>
<td><p>絶えず過変調</p></td>
<td><p>使用出来ない</p></td>
</tr>
</tbody>
</table>

## 関連項目

  - [国際放送](../Page/国際放送.md "wikilink")
  - [短波放送](../Page/短波放送.md "wikilink")
  - [日本語放送](../Page/日本語放送.md "wikilink")
  - [BCL](../Page/BCL.md "wikilink")
  - [RSTコード](https://ja.wikipedia.org/wiki/RSTコード "wikilink")

[Category:ラジオ](https://ja.wikipedia.org/wiki/Category:ラジオ "wikilink")