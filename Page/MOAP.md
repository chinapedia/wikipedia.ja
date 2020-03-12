> この記事は[MOAP](https://ja.wikipedia.org/wiki/MOAP)から翻訳されています。


**MOAP**（*Mobile Oriented Applications Platform*）は、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")が中心となり開発を行っている携帯電話用プラットフォーム（[アプリケーションプラットフォーム](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")・[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")）である。[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の[第三世代携帯電話](https://ja.wikipedia.org/wiki/第三世代携帯電話 "wikilink")「[FOMA](../Page/FOMA.md "wikilink")」に搭載されている。クローズドユーザインタフェースなので、[UIQ](../Page/UIQ.md "wikilink")や[S60](https://ja.wikipedia.org/wiki/S60 "wikilink")などと違いサードパーティがネイティブアプリケーションのソフト開発を行うことができない。[Symbian OS用と](../Page/Symbian_OS.md "wikilink")[Linux](../Page/Linux.md "wikilink")用と2種類用意されている。

## 概要

携帯電話メーカ各社がそれまで携帯電話用のインターフェース、ミドルウェア等を開発してきたが、それらの開発コストの抑制、インターフェースの均一化を図る目的で開発を進めている。Symbian OS用、Linux OS用と2タイプ用意されている。開発用の[エミュレーター](https://ja.wikipedia.org/wiki/エミュレーター "wikilink")も用意されている上、メーカーはMOAP上に設けられた独自アプリケーションエリア、[ミドルウェア](../Page/ミドルウェア.md "wikilink")上の独自エリアのみを開発すればよく、携帯電話の開発速度の向上、開発コストの抑制を行うことができるうえ、NTTドコモ独自のサービスも全メーカーに簡単に展開することができる。

以下の図がプラットフォームの構成図であり、メーカーは**グレーの部分**のみの開発で済む。

|                                                                |
| -------------------------------------------------------------- |
| [iアプリ](https://ja.wikipedia.org/wiki/iアプリ "wikilink")（フリー開発部分） |
| ネイティブアプリ（メーカ独自開発）                                              |
|                                                                |
| ミドルウェア（MOAP共通）                                                 |
| OS部分（MOAP共通）                                                   |

なお、NTTドコモではFOMA端末の開発効率を向上させるため、Symbian OS・Linux OSいずれに向けてもアプリケーションソフトウェアセット「[オペレータパック](https://ja.wikipedia.org/wiki/オペレータパック "wikilink")」を開発し、2011年現在はMOAP後継としてFOMA端末への搭載を進めている。Symbianベースのものとしては[SH-07B](https://ja.wikipedia.org/wiki/SH-07B "wikilink")より、Linuxベースのものとしては[N-01B](https://ja.wikipedia.org/wiki/N-01B "wikilink")より搭載が開始された。

### MOAPの機能例

<table>
<tbody>
<tr class="odd">
<td><ul>
<li>通信シーケンス制御</li>
<li><a href="../Page/WORLD_WING.md" title="wikilink">WORLD WINGの言語交換</a></li>
<li>回線交換、パケット交換の分離規制機能</li>
<li><a href="https://ja.wikipedia.org/wiki/iモード" title="wikilink">iモード</a>ブラウザ/<a href="../Page/フルブラウザ.md" title="wikilink">フルブラウザ</a></li>
<li><a href="https://ja.wikipedia.org/wiki/iモードメール" title="wikilink">iモードメール</a></li>
<li><a href="https://ja.wikipedia.org/wiki/iアプリ" title="wikilink">iアプリ</a>プラットホーム</li>
<li><a href="https://ja.wikipedia.org/wiki/デコメアニメ" title="wikilink">デコメアニメ</a></li>
<li><a href="https://ja.wikipedia.org/wiki/iコンシェル" title="wikilink">iコンシェル</a></li>
<li><a href="https://ja.wikipedia.org/wiki/iウィジェット" title="wikilink">iウィジェット</a></li>
<li><a href="https://ja.wikipedia.org/wiki/iチャネル" title="wikilink">iチャネル</a></li>
<li><a href="https://ja.wikipedia.org/wiki/iエリア" title="wikilink">iエリア</a></li>
</ul></td>
<td><ul>
<li><a href="../Page/2in1_(NTTドコモ).md" title="wikilink">2in1</a></li>
<li><a href="../Page/プッシュトーク.md" title="wikilink">プッシュトーク</a></li>
<li><a href="https://ja.wikipedia.org/wiki/iチャネル" title="wikilink">iチャネル</a></li>
<li><a href="https://ja.wikipedia.org/wiki/iコンシェル" title="wikilink">iコンシェル</a></li>
<li><a href="../Page/ワンセグ.md" title="wikilink">ワンセグ</a></li>
<li><a href="https://ja.wikipedia.org/wiki/ケータイお探しサービス" title="wikilink">ケータイお探しサービス</a></li>
<li><a href="https://ja.wikipedia.org/wiki/イマドコサーチ" title="wikilink">イマドコサーチ</a></li>
<li><a href="https://ja.wikipedia.org/wiki/おまかせロック" title="wikilink">おまかせロック</a></li>
<li><a href="https://ja.wikipedia.org/wiki/電話帳お預かりサービス" title="wikilink">電話帳お預かりサービス</a></li>
<li><a href="https://ja.wikipedia.org/wiki/エリアメール" title="wikilink">エリアメール</a></li>
<li><a href="https://ja.wikipedia.org/wiki/きせかえツール" title="wikilink">きせかえツール</a>　他</li>
</ul></td>
</tr>
</tbody>
</table>

## MOAP(S)

Symbian OSを搭載した携帯電話用。以下のメーカーの端末に搭載されている。

  - [ソニー・エリクソン](https://ja.wikipedia.org/wiki/ソニー・エリクソン・モバイルコミュニケーションズ "wikilink")（[SO705i](../Page/SO705i.md "wikilink")、[SO706i](../Page/SO706i.md "wikilink")を除く）
  - [シャープ](../Page/シャープ.md "wikilink")
  - [三菱電機](../Page/三菱電機.md "wikilink")
  - [富士通](../Page/富士通.md "wikilink")

[Symbian FoundationからSymbian](https://ja.wikipedia.org/wiki/Symbian_Foundation "wikilink") Foundation Platform Releaseの一部としてオープンソース化されている。

## MOAP(L)

Linuxを搭載した携帯電話用。以下の端末に搭載されている。

  - [パナソニック モバイルコミュニケーションズ製の端末](../Page/パナソニック_モバイルコミュニケーションズ.md "wikilink")
  - [日本電気](../Page/日本電気.md "wikilink")（現[NECカシオ](https://ja.wikipedia.org/wiki/NECカシオ_モバイルコミュニケーションズ "wikilink")）製の端末
  - [SO705i](../Page/SO705i.md "wikilink")・[SO706i](../Page/SO706i.md "wikilink")

## 関連項目

  - [Symbian OS](../Page/Symbian_OS.md "wikilink")
  - [Linux](../Page/Linux.md "wikilink")
  - [LiMo Platform](https://ja.wikipedia.org/wiki/LiMo_Foundation "wikilink")
  - [NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")
  - [UIQ](../Page/UIQ.md "wikilink")
  - [S60](https://ja.wikipedia.org/wiki/S60 "wikilink")

## 脚注

<references/>

## 外部リンク

  - NTT DoCoMoテクニカル・ジャーナル

<!-- end list -->

  - [FOMA端末ソフトウェアプラットフォーム"MOAP"の開発](http://www.nttdocomo.co.jp/binary/pdf/corporate/technology/rd/technical_journal/bn/vol13_1/vol13_1_055jp.pdf) (PDF)
  - [移動端末用ソフトウェアプラットフォーム"MOAP"の拡充](http://www.nttdocomo.co.jp/binary/pdf/corporate/technology/rd/tech/main/platform/vol14_1_15jp.pdf) (PDF)

<!-- end list -->

  - [ITmedia](../Page/ITmedia.md "wikilink")

<!-- end list -->

  - [グローバル端末の開発も容易に――ドコモのプラットフォーム「MOAP」の未来](http://plusd.itmedia.co.jp/mobile/articles/0710/19/news031.html)

[Category:携帯電話_(NTTドコモ)](https://ja.wikipedia.org/wiki/Category:携帯電話_\(NTTドコモ\) "wikilink")