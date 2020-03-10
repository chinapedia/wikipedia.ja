> この記事は[InternetFAX](https://ja.wikipedia.org/wiki/InternetFAX)から翻訳されています。


**InternetFAX**（いんたーねっとふぁっくす）とは、FoIPとも呼ばれる、[ファクシミリ](https://ja.wikipedia.org/wiki/ファクシミリ "wikilink")を[パケット](../Page/パケット.md "wikilink")に変換した上で[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")で伝送する技術である。

この項では「InternetFAX」の技術と[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")との違いを記述する。その他については[関連項目も参照のこと](https://ja.wikipedia.org/wiki/#関連項目 "wikilink")。

## 概要および経緯

InternetFAXには、[リアルタイム](../Page/リアルタイム.md "wikilink")伝送方式と[電子メール](../Page/電子メール.md "wikilink")のような[蓄積交換方式とがある](../Page/ストアアンドフォワード.md "wikilink")。

[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")ごろには、狭い帯域のパケット通信での自然な音声のリアルタイム伝送の研究が盛んに行われ、VoIP技術に目処が立った。次に、狭帯域の遅延のある通信網で静止画像を伝送する、[T.37](https://ja.wikipedia.org/wiki/T.37 "wikilink")と[T.38](https://ja.wikipedia.org/wiki/T.38 "wikilink")のFAX規格が[ITU-T](../Page/ITU-T.md "wikilink")に提案された。

[2000年](../Page/2000年.md "wikilink")以降、[ブロードバンドインターネット接続](https://ja.wikipedia.org/wiki/ブロードバンドインターネット接続 "wikilink")とともに、[ISDN](../Page/ISDN.md "wikilink")と同じ[G.711](../Page/G.711.md "wikilink")符号化の[IP電話](../Page/IP電話.md "wikilink")サービスが利用されるようになった。そのようなVoIPで、[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")をみなし音声として伝送するものをinbandFAXと呼ぶ。

### 方式間の比較

<table style="width:10%;">
<caption>インターネットファクシミリ方式間の比較</caption>
<colgroup>
<col style="width: 0%" />
<col style="width: 0%" />
<col style="width: 0%" />
<col style="width: 0%" />
<col style="width: 1%" />
<col style="width: 6%" />
<col style="width: 4%" />
<col style="width: 0%" />
<col style="width: 0%" />
<col style="width: 0%" />
</colgroup>
<thead>
<tr class="header">
<th><p><a href="../Page/ITU-T.md" title="wikilink">ITU-T</a></p></th>
<th><p>別名</p></th>
<th><p>必<br />
要<br />
帯<br />
域</p></th>
<th><p>通信速度</p></th>
<th><p>安定性</p></th>
<th><p><a href="../Page/リアルタイム.md" title="wikilink">リアルタイム</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/電話網" title="wikilink">電話網</a><a href="https://ja.wikipedia.org/wiki/ゲートウェイ" title="wikilink">ゲートウェイ</a></p></th>
<th><p>用途</p></th>
<th><p>通信先指定</p></th>
<th><p>特徴</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/G.711.md" title="wikilink">G.711</a><br />
インバンド</p></td>
<td><p>みなし<br />
音声<br />
方式</p></td>
<td><p>大</p></td>
<td><p>9.6<br />
k<a href="../Page/ビット毎秒.md" title="wikilink">b/s</a><br />
以下</p></td>
<td><p>保証されてはいない</p></td>
<td><p>○</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/VoIP" title="wikilink">VoIP</a></p></td>
<td><p><a href="../Page/IP電話.md" title="wikilink">IP電話</a></p></td>
<td><p><a href="../Page/電話番号.md" title="wikilink">電話番号</a></p></td>
<td><p>FAX端末を選ばない</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/T.37" title="wikilink">T.37</a><br />
Simple Mode</p></td>
<td><p>メール<br />
方式</p></td>
<td><p>小</p></td>
<td><p>高速</p></td>
<td><p>保証されている</p></td>
<td><p>遅延が大きい場合がある</p></td>
<td><p>FAX<br />
専用</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/アプリケーションサービスプロバイダ" title="wikilink">ASP</a></p></td>
<td><p><a href="../Page/電話番号.md" title="wikilink">電話番号</a><br />
<a href="https://ja.wikipedia.org/wiki/メールアドレス" title="wikilink">メールアドレス</a></p></td>
<td><p>基本的な伝送機能のみ</p></td>
</tr>
<tr class="odd">
<td><p>T.37<br />
Full Mode</p></td>
<td><p>送達確認・能力交換などの双方向機能<br />
高精細度・カラー伝送などの付加機能</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>T.37<br />
<a href="https://ja.wikipedia.org/wiki/ダイレクトSMTP" title="wikilink">ダイレクトSMTP</a></p></td>
<td><p>IPアドレス<br />
方式</p></td>
<td><p>○</p></td>
<td><p>通信不可</p></td>
<td><p><a href="../Page/イントラネット.md" title="wikilink">イントラネット</a></p></td>
<td><p><a href="../Page/IPアドレス.md" title="wikilink">IPアドレス</a><br />
<a href="../Page/ドメイン名.md" title="wikilink">ドメイン名</a></p></td>
<td><p>同一ローカルネットワーク内で<br />
<a href="https://ja.wikipedia.org/wiki/メールサーバ" title="wikilink">メールサーバ</a>不要の直接通信</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/T.38" title="wikilink">T.38</a></p></td>
<td><p>FoIP</p></td>
<td><p>電話網FAXによっては通信不能</p></td>
<td><p>○</p></td>
<td><p>FAX<br />
専用</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/内線電話" title="wikilink">内線電話</a><br />
<a href="https://ja.wikipedia.org/wiki/Next_Generation_Network" title="wikilink">NGN</a></p></td>
<td><p><a href="../Page/電話番号.md" title="wikilink">電話番号</a></p></td>
<td><p>internet facsimile protocol<a href="../Page/パケット.md" title="wikilink">パケット</a>で伝送</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 網構成

電話網からのFAX発信を、VoIP[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")で音声パケットに変換し、IPで中継するものが、[IP電話](../Page/IP電話.md "wikilink")サービスで利用可能である。

  -
    FAX装置 - VoIPゲートウェイ - インターネットプロトコル - VoIPゲートウェイ - FAX装置

電話網からのFAX発信を、InternetFAX[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")でパケットに変換し、IPで中継するものが、[内線電話](https://ja.wikipedia.org/wiki/内線電話 "wikilink")とデータ通信網の統合のために利用されている。

  -
    FAX装置 - InternetFAXゲートウェイ - インターネットプロトコル - InternetFAXゲートウェイ - FAX装置

電話網からのFAX発信を、InternetFAXゲートウェイで変換して電子メールで受信する、[ASPがある](https://ja.wikipedia.org/wiki/アプリケーションサービスプロバイダ "wikilink")。

  -
    FAX装置 - InternetFAXゲートウェイ - インターネット - メールサーバ - 電子メールとして受信

電子メールとして発信し、InternetFAXゲートウェイでファクシミリ信号に変換してFAX装置で受信するものが、同報通信・不達時再送信・時間指定送信などを付加してASPとして提供されている。

  -
    電子メールとして発信 - メールサーバ - インターネット - InternetFAXゲートウェイ - FAX装置

[ダイレクトSMTP](https://ja.wikipedia.org/wiki/ダイレクトSMTP "wikilink") T.37 Full Mode 対応装置間で、同一ローカルネットワークの固定[IPアドレス](../Page/IPアドレス.md "wikilink")・[ホスト名](../Page/ホスト名.md "wikilink")指定で[ダイナミックドメインネームシステム](../Page/ダイナミックドメインネームシステム.md "wikilink")(動的グローバルIPアドレス)対応[ルーター](../Page/ルーター.md "wikilink")接続での直接通信が可能である。T.38 対応装置間で、グローバル固定IPアドレスもしくは固定ローカルIPアドレス、[SIPによる内線電話番号](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink")、[NGN網の](https://ja.wikipedia.org/wiki/Next_Generation_Network "wikilink")[電話番号](../Page/電話番号.md "wikilink")での直接通信が可能である。

  -
    InternetFAX装置 - インターネットプロトコル - InternetFAX装置

## リアルタイム転送方式

FAX端末間を[リアルタイム](../Page/リアルタイム.md "wikilink")に接続し、伝送を行うものである。リアルタイム伝送であるので、送信結果の確認が容易である。

### G.711インバンド方式

G.711インバンド方式は、G3ファクシミリの[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")信号をみなし[音](../Page/音.md "wikilink")声として伝送するものである。多くの[IP電話](../Page/IP電話.md "wikilink")サービスで利用可能であるが、伝送が保証されているものはない

  - 利点
      - 網側にFAX専用のゲートウェイが不要。
      - 音声のままなのでFAX端末を選ばない。
  - 欠点
      - 9600[b/s以下の通信速度となる](../Page/ビット毎秒.md "wikilink")。
      - パケットの揺らぎやロス・伝送信号レベルの設定の不具合・無音圧縮による信号の頭切れ・[エコーキャンセラによる波形の乱れなどにより](../Page/エコー除去.md "wikilink")、伝送時間の増大・通信の切断がおこる場合がある。

[情報通信ネットワーク産業協会](https://ja.wikipedia.org/wiki/情報通信ネットワーク産業協会 "wikilink")によって『IP-PBXにVoIP-TAを経由してファクシミリ端末を収容する際のVoIP-TA/ファクシミリ端末ガイドライン』（2007年10月19日制定）が提案された。

### ITU-T T.38

T.38は、画像情報をIP[パケット](../Page/パケット.md "wikilink")変換して[リアルタイム](../Page/リアルタイム.md "wikilink")伝送するものであり、[ITU-T](../Page/ITU-T.md "wikilink")で[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[6月](../Page/6月.md "wikilink")勧告された。

G3ファクシミリの[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")信号を[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")で変換するものが、[内線電話](https://ja.wikipedia.org/wiki/内線電話 "wikilink")の[IP網](https://ja.wikipedia.org/wiki/IP網 "wikilink")に使用されている。[PCのFAX送信](../Page/パーソナルコンピュータ.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")や業務用[複合機](https://ja.wikipedia.org/wiki/複合機 "wikilink")で、[SIPによる内線電話番号](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink")・[IPアドレス](../Page/IPアドレス.md "wikilink")で送信可能である。2010年2月1日に、[NGN網の](https://ja.wikipedia.org/wiki/Next_Generation_Network "wikilink")[電話番号](../Page/電話番号.md "wikilink")でのFAXサービスのインプリメント仕様を、[ソフトフロント](https://ja.wikipedia.org/wiki/ソフトフロント "wikilink")が発表した。\[1\]

  - 利点
      - 9600b/s超える速度での伝送が可能。
      - データだけを転送するので狭い帯域でも送受信が可能。
  - 欠点
      - 電話網と接続する場合、FAX専用のゲートウェイがインターネット網側に必要。
      - 電話網FAX端末の信号方式によっては通信不能となる場合がある。
      - 信号の伝送遅延等により送受信が正常終了しないことがある。

## 蓄積交換方式

[蓄積交換方式は](../Page/ストアアンドフォワード.md "wikilink")、FAXの[画像](../Page/画像.md "wikilink")[データ](../Page/データ.md "wikilink")を[電子メール](../Page/電子メール.md "wikilink")の添付ファイルに変換し[メールアドレス](https://ja.wikipedia.org/wiki/メールアドレス "wikilink")を指定して[SMTPで伝送するものである](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")。

T.37ゲートウェイ・[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")・[オンラインストレージ](https://ja.wikipedia.org/wiki/オンラインストレージ "wikilink")を組み合わせた[ASPが提供されている](https://ja.wikipedia.org/wiki/アプリケーションサービスプロバイダ "wikilink")。[ダイナミックドメインネームシステム](../Page/ダイナミックドメインネームシステム.md "wikilink")・[ダイレクトSMTP](https://ja.wikipedia.org/wiki/ダイレクトSMTP "wikilink")により[ドメインネーム](https://ja.wikipedia.org/wiki/ドメインネーム "wikilink")で動的グローバルIPアドレスを直接指定し、リアルタイムのT.37 Full Mode 通信画可能な機器がある。

  - 利点
      - [パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")・[携帯電話](../Page/携帯電話.md "wikilink")など他の[情報機器](https://ja.wikipedia.org/wiki/情報機器 "wikilink")でデータの再利用が容易である。
      - 同報通信・不達時再送信・時間指定送信などの付加機能の実現が網側で可能である。
      - 狭い帯域でも送受信が可能である。
  - 欠点
      - 相手先に到達するまでの遅延時間が大きくなる場合がある。

### ファクシミリ関連電気通信サービス

<table>
<caption><a href="https://ja.wikipedia.org/wiki/電話網" title="wikilink">電話網</a>からインターネット網への着信のみファクシミリ関連<a href="https://ja.wikipedia.org/wiki/電気通信役務" title="wikilink">電気通信サービス</a></caption>
<colgroup>
<col style="width: 15%" />
<col style="width: 10%" />
<col style="width: 30%" />
<col style="width: 15%" />
<col style="width: 30%" />
</colgroup>
<thead>
<tr class="header">
<th><p><a href="../Page/商標.md" title="wikilink">商標</a><br />
（<a href="../Page/企業.md" title="wikilink">企業</a>）</p></th>
<th><p>付与される<a href="../Page/電話番号.md" title="wikilink">電話番号</a></p></th>
<th><p>ファイル形式</p></th>
<th><p>保存容量</p></th>
<th><p>特徴</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Tagged_Image_File_Format.md" title="wikilink">TIFF</a></p></td>
<td><p><a href="../Page/Portable_Document_Format.md" title="wikilink">PDF</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/D-FAX" title="wikilink">D-FAX</a><a href="http://www.d-fax.ne.jp/">1</a><br />
（<a href="../Page/東京テレメッセージサービス.md" title="wikilink">東京テレメッセージサービス</a>）</p></td>
<td><p>020-</p></td>
<td><p>○</p></td>
<td><p>1,050円/年間</p></td>
<td><p>7日前までの送信ファイルの閲覧 1,050円/年間</p></td>
</tr>
<tr class="odd">
<td><p>F@xEm@il<a href="http://www.giken.co.jp/ics/faxemail/">2</a><br />
（技研商事インターナショナル）</p></td>
<td><p>03-<br />
<a href="https://ja.wikipedia.org/wiki/アメリカ合衆国" title="wikilink">米</a>120都市</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/フレッツ#ひかり電話" title="wikilink">ひかり電話FAXお知らせメール</a><a href="http://flets.com/hikaridenwa/service/fax.html">3</a><br />
（<a href="../Page/東日本電信電話.md" title="wikilink">NTT東日本</a>・<a href="../Page/西日本電信電話.md" title="wikilink">NTT西日本</a>）</p></td>
<td><p>ひかり電話の追加番号</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>10MB</p></td>
</tr>
</tbody>
</table>

<table>
<caption>電話網からインターネット網への着信とインターネット網から日本国内の電話網への発信とのファクシミリ関連電気通信サービス</caption>
<thead>
<tr class="header">
<th><p>商標<br />
（企業）</p></th>
<th><p>付与される電話番号</p></th>
<th><p>受信ファイル形式</p></th>
<th><p>送信ファイル形式</p></th>
<th><p>保存容量</p></th>
<th><p>特徴</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TIFF</p></td>
<td><p><a href="../Page/JPEG.md" title="wikilink">JPEG</a></p></td>
<td><p>PDF</p></td>
<td><p>TIFF</p></td>
<td><p>JPEG</p></td>
<td><p>PDF</p></td>
</tr>
<tr class="even">
<td><p>KDDIペーパレスFAX<a href="http://www.kddi.com/pub/fax/">4</a><br />
（<a href="../Page/KDDI.md" title="wikilink">KDDI</a>）</p></td>
<td><p>050-</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>BizFAXストレージ＆リモート<a href="http://www.ntt.com/050fax/">5</a><br />
（<a href="../Page/NTTコミュニケーションズ.md" title="wikilink">NTTコミュニケーションズ</a>）</p></td>
<td><p>050-</p></td>
<td><p>PC</p></td>
<td><p><a href="../Page/携帯電話.md" title="wikilink">:携帯</a></p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>ToonesインターネットFAX<a href="http://www.toones.jp/">6</a><br />
（Karigo）</p></td>
<td></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>どこでもMyFAX<a href="http://www.nekonet.co.jp/service/network/dokodemo-myfax.html">7</a><br />
（<a href="https://ja.wikipedia.org/wiki/ヤマトシステム開発" title="wikilink">ヤマトシステム開発</a>）</p></td>
<td><p>03- 050- 0120-</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>BIZBOX FAX<a href="http://t-con.net/service/documents/bizbox01.htm">8</a><br />
（<a href="https://ja.wikipedia.org/wiki/東芝ファイナンス" title="wikilink">東芝ファイナンス</a>）</p></td>
<td></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>Fax2Mail<a href="http://easylink-marketing.jp/f2m/">9</a><br />
（エクスパダイト）</p></td>
<td><p>03-</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>FleaFAX<a href="http://www.covia.jp/net/fleaFax-01.html">10</a><br />
（コヴィア・ネットワークス）</p></td>
<td><p>03- 050-</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>Message+（メッセージプラス）<a href="http://www.messageplus.jp/">11</a><br />
（アクセルコミュニケーションズ）</p></td>
<td><p>050-</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
</tbody>
</table>

<table>
<caption>電話網からのインターネット網への着信とインターネット網から日本国内外の電話網への発信とのファクシミリ関連電気通信サービス</caption>
<thead>
<tr class="header">
<th><p>商標<br />
（企業）</p></th>
<th><p>付与される電話番号</p></th>
<th><p>受信ファイル形式</p></th>
<th><p>送信ファイル形式</p></th>
<th><p>保存容量</p></th>
<th><p>特徴</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TIFF</p></td>
<td><p>JPEG</p></td>
<td><p>PDF</p></td>
<td><p>TIFF</p></td>
<td><p>JPEG</p></td>
<td><p>PDF</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/ファクシミリ通信網" title="wikilink">BizFAX スマートキャスト</a><a href="http://www.ntt.com/bizfax/smart/">12</a><br />
（<a href="../Page/NTTコミュニケーションズ.md" title="wikilink">NTTコミュニケーションズ</a>）</p></td>
<td><p>26桁の特殊な専用番号</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>eFax<a href="http://www.efax.co.jp/">13</a><br />
（j2 Global Japan）</p></td>
<td><p>世界46カ国、3,500都市の番号</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>InterFAX<a href="http://www.interfax.jp/">14</a><br />
（ドゥイット）</p></td>
<td><p>03- 0120- 0800-</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>TransAct<a href="http://www.transact.ne.jp/">15</a><br />
（トランザクト）</p></td>
<td><p>03-</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>faximo<a href="http://faximo.jp/">16</a><br />
（エディックワークス）</p></td>
<td><p>03-</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>FAXCAST<a href="http://www.faxcast.ne.jp/">17</a><br />
（創心企画）</p></td>
<td><p>03-</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>PamFax<a href="http://www.pamfax.biz/ja/">18</a><br />
（PamConsult）</p></td>
<td><p>世界31カ国の番号</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>HelloFax<a href="https://www.hellofax.com/">19</a><br />
（JN PROJECTS）</p></td>
<td><p>米国</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>PHYTTER FAX<a href="http://www.phytter.com/ja/top-fax.php">20</a><br />
（Interush）</p></td>
<td><p>03- 米国</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>myfax<a href="http://www.myfax.com/">21</a><br />
（j2 Global Communications）</p></td>
<td><p>米国</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

| 商標                                                                   | 企業                                                                                        | 送信ファイル形式 | 特徴   |
| -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | -------- | ---- |
| TIFF                                                                 | JPEG                                                                                      | PDF      | Word |
| AIFnetwork[22](http://www.aif.net/)                                  | アイナス                                                                                      |          |      |
| @Tovas[23](http://www.attovas.com/)                                  | [コクヨ](https://ja.wikipedia.org/wiki/コクヨ "wikilink")                                       |          |      |
| BizFit Office[24](http://panasonic-denkois.co.jp/bizfit/office/fax/) | [パナソニック電工インフォメーションシステムズ](https://ja.wikipedia.org/wiki/パナソニック電工インフォメーションシステムズ "wikilink") | ○        | ×    |
| 0FAX.net[25](https://0fax.net/)                                      | 杉松                                                                                        | ×        | ×    |

インターネット網から日本国内の電話網への発信のファクシミリ関連電気通信サービス

| 商標                                                       | 企業                                | 送信ファイル形式 | 特徴   |
| -------------------------------------------------------- | --------------------------------- | -------- | ---- |
| TIFF                                                     | JPEG                              | PDF      | Word |
| FNX[26](http://www.nexway.co.jp/service_top.html)        | ネクスウェイ                            |          |      |
| faximoSilver[27](http://silver.faximo.jp/)               | エディックワークス                         | ○        | ○    |
| BIGLOBEメールFAX配信サービス[28](http://email.biglobe.ne.jp/fax/) | [NEC](../Page/日本電気.md "wikilink") | ×        | ×    |

インターネット網から日本国内外の電話網への発信のファクシミリ関連電気通信サービス

## InternetFAX専用機器

### InternetFAX装置

InternetFAX装置は、[IPの回線に接続し](../Page/Internet_Protocol.md "wikilink")[電子メール](../Page/電子メール.md "wikilink")を直接発着信できるFAXである。業務用の[複合機](https://ja.wikipedia.org/wiki/複合機 "wikilink")の付加機能として提供されているものが多い。

  - 主な機能
      - [IPアドレス](../Page/IPアドレス.md "wikilink")・[ドメインネーム](https://ja.wikipedia.org/wiki/ドメインネーム "wikilink")・[ダイナミックドメインネームシステム](../Page/ダイナミックドメインネームシステム.md "wikilink")(動的グローバルIPアドレス)・[ダイレクトSMTP](https://ja.wikipedia.org/wiki/ダイレクトSMTP "wikilink")での発着信
      - 転送機能
      - InternetFAXゲートウェイ機能
      - T.37 Full Mode の、送達確認・能力交換などの双方向機能、高精細度・カラー伝送などの付加機能
      - [PDFファイル形式での伝送機能を持つものもある](../Page/Portable_Document_Format.md "wikilink")。

### InternetFAXゲートウェイ

**InternetFAXゲートウェイ**は、[電話網](https://ja.wikipedia.org/wiki/電話網 "wikilink")に接続した[ファクシミリ](https://ja.wikipedia.org/wiki/ファクシミリ "wikilink")端末の信号を[IPに変換](../Page/Internet_Protocol.md "wikilink")（オンランプ）、IPの信号をファクシミリ端末信号に変換（オフランプ）する機能を持った機器である。G3, Super G3 のみに対応しているものがほとんどである。

FAX[モデム](https://ja.wikipedia.org/wiki/モデム#可聴帯域用のモデム "wikilink")・[イーサネット](../Page/イーサネット.md "wikilink")を[インターフェースとして実装している](../Page/インタフェース_\(情報技術\).md "wikilink")。拡張機能を[ソフトウェア](../Page/ソフトウェア.md "wikilink")として実装している。

  - T.37ゲートウェイ : [電子メール](../Page/電子メール.md "wikilink")とFAX信号とを相互変換。[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")機能と一体のものもある。
  - T.38ゲートウェイ : FAX信号を[パケット](../Page/パケット.md "wikilink")に変換して[リアルタイム](../Page/リアルタイム.md "wikilink")伝送

## 関連項目

  - [VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink") : 網構成・専用機器など
  - [Session Initiation Protocol](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink")
  - [H.323](https://ja.wikipedia.org/wiki/H.323 "wikilink")
  - [IP電話](../Page/IP電話.md "wikilink") : 専用の[IP加入者網を利用したもの](../Page/Internet_Protocol.md "wikilink")。IP電話サービスの概要・法的位置付け・[電気通信事業者](https://ja.wikipedia.org/wiki/電気通信事業者 "wikilink")など。
  - [インターネット電話](https://ja.wikipedia.org/wiki/インターネット電話 "wikilink") : [インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")を利用したもの。
  - [IPセントレックス](https://ja.wikipedia.org/wiki/IPセントレックス "wikilink") : [内線電話](https://ja.wikipedia.org/wiki/内線電話 "wikilink")のVoIP化、モバイルセントレックス・企業内IPセントレックス。
  - [電話網](https://ja.wikipedia.org/wiki/電話網 "wikilink")

## 脚注

## 外部リンク

  - [大野研究室 WIDE/IFAX](http://www.ohnolab.org/researches/ifax/japanese/) : Simple ModeインターネットFAXのフリーソフトウェア
  - [インターネットFAX概要](http://kobe-navi.info/) : インターネットFAX情報と比較など
  - [インターネットFAXシステム構成](http://internet-fax.info/pcfax-soft.html) : パソコンFAXソフトとインターネットFAXの違いなど

[Category:IP電話](https://ja.wikipedia.org/wiki/Category:IP電話 "wikilink")

1.  [NGN を利用する T.38 ベースの IP 化 FAX 接続](http://www.softfront.co.jp/library/2013/10/100201_specification-IPFAX.pdf)