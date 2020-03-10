> この記事は[WinShare](https://ja.wikipedia.org/wiki/WinShare)から翻訳されています。


**WinShare**は、[日本電気](../Page/日本電気.md "wikilink")（NEC）が1997年から販売しているリモート操作ソフトウェア。ネットワークに接続された[PC](../Page/PC.md "wikilink")や[サーバ](../Page/サーバ.md "wikilink")といった機器のリモート操作を実現する。

## 概要

操作する側の機器（オペレーションPC）にWinShare オペレーション、操作される側の機器（リモートPC）にWinShare リモートをそれぞれインストールすることで、オペレーションPCからリモートPCを簡単にリモート操作できるようになる。

対応している[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は[Microsoft Windowsであり](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、リモートPCは[Windows Embeddedにも対応している](https://ja.wikipedia.org/wiki/Windows_Embedded "wikilink")。基本的な機能は[VNC](https://ja.wikipedia.org/wiki/VNC "wikilink")や[Symantec](https://ja.wikipedia.org/wiki/Symantec "wikilink") pcAnywhereと同等であるが、以下に挙げる様な特徴を持つ。

### リモート操作

オペレーションPCのマウスやキーボードを用いて、リモートPCを自在にリモート操作できる。[Ctrl-Alt-Del](https://ja.wikipedia.org/wiki/Ctrl-Alt-Del "wikilink")コマンドの送信や[IME](https://ja.wikipedia.org/wiki/IME "wikilink")の切り替え等も行える。なお、リモート操作中の画面はオペレーションPCとリモートPCの双方に表示される。

### ファイル転送

[Windows Explorerライクの](https://ja.wikipedia.org/wiki/Windows_Explorer "wikilink")[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")で、オペレーションPCからリモートPCに対するファイルの送受信を行うことができる。どのようなファイルを送受信したかといった履歴はログとして保存することも可能。

### 電源制御

[Intel](https://ja.wikipedia.org/wiki/Intel "wikilink") Active Management Technology（Intel AMT）、もしくは[Wake-on-LAN](../Page/Wake-on-LAN.md "wikilink")によるリモートPCの電源制御（電源ONやリセット等）が可能。

### NAVIPAD（透明ボード機能）

リモート操作中の画面上にフリーハンドで絵や文字を描くことが可能。描かれた絵や文字はオペレーションPCとリモートPCの双方に表示される。

### セキュリティ対策

リモート操作開始時のユーザ認証／アクセスホスト制御や、リモート操作内容のログ出力等が可能。また、リモートPCが出力するログは暗号化して保存したり、事前に指定した任意のファイルサーバに集約保存したりすることもできる。オペレーションPCとリモートPCがともにVer6.1以降の場合、全ての通信内容は鍵長256ビットの[AES](https://ja.wikipedia.org/wiki/AES "wikilink")によって暗号化される。

### 中継サーバ経由の接続

中継サーバを設置することで、オペレーションPCからリモートPCに直接接続できないネットワーク構成の場合でもリモート操作が可能。ただし、中継サーバは自前で準備が必要。

### 招待機能

リモートPCの端末利用者がヘルプデスク(オペレーションPC)からのサポートを欲したときに、招待ファイルを発行しオペレーションPCの利用者に送付することで、簡単に一時接続によるサポートを受けることが可能。

### 英語OS対応

英語版の[Microsoft Windowsでの利用が可能](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 経歴

<table>
<caption>WinShareのリリース経歴</caption>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>主な強化内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Ver2.0</p></td>
<td><p>1997/06/09</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Ver2.1</p></td>
<td><p>1998/09/09</p></td>
<td><p>操作レスポンス向上、バージョンアップインストール対応</p></td>
</tr>
<tr class="odd">
<td><p>Ver3.0</p></td>
<td><p>2000/07/03</p></td>
<td><p>Windows XP対応、ファイル転送</p></td>
</tr>
<tr class="even">
<td><p>Ver4.0</p></td>
<td><p>2003/01/06</p></td>
<td><p>ユーザ毎のセキュリティ設定</p></td>
</tr>
<tr class="odd">
<td><p>Ver5.0</p></td>
<td><p>2006/04/06</p></td>
<td><p>リモート デスクトップ接続との併用対応、Windows XPの簡易ユーザ切り替え機能</p></td>
</tr>
<tr class="even">
<td><p>Ver5.1</p></td>
<td><p>2008/01/08</p></td>
<td><p>Windows Vista対応、Windows Server 2003 x64版での制限事項解除<br />
Windows Server 2008対応、インストール方式変更</p></td>
</tr>
<tr class="odd">
<td><p>Ver5.2</p></td>
<td><p>2010/04/26</p></td>
<td><p>Windows 7、Windows Server 2008 R2対応</p></td>
</tr>
<tr class="even">
<td><p>Ver5.3</p></td>
<td><p>2012/07/02</p></td>
<td><p>サイレントインストール対応<br />
通信暗号化対応<br />
英語OS対応<br />
Windows 8、Windows Server 2012対応</p></td>
</tr>
<tr class="odd">
<td><p>Ver6.0</p></td>
<td><p>2014/06/02</p></td>
<td><p>リモート電源制御<br />
4Kディスプレイ対応</p></td>
</tr>
<tr class="even">
<td><p>Ver6.1</p></td>
<td><p>2016/02/01</p></td>
<td><p>利用ポート数削減（ポート一本化）<br />
ログ暗号化／集約保存対応<br />
NAVIPADテキスト入力対応<br />
Windows 10対応</p></td>
</tr>
<tr class="odd">
<td><p>Ver6.2</p></td>
<td><p>2017/04/03</p></td>
<td><p>マルチディスプレイ対応<br />
リモート操作録画対応<br />
ログファイル形式変更<br />
割り込み接続許可／拒否設定対応<br />
Windows Server 2016対応</p></td>
</tr>
<tr class="even">
<td><p>Ver7.0</p></td>
<td><p>2018/04/09</p></td>
<td><p>中継サーバ経由のリモート接続に対応 コンソール接続に対応</p>
<p>リモート接続可能な時間帯の設定に対応</p>
<p>構築自動化(Ansible)に対応</p>
<p>プロキシサーバ経由の接続に対応</p>
<p>召喚機能に対応</p>
<p>アイコンによる接続状態通知に対応</p></td>
</tr>
<tr class="odd">
<td><p>Ver7.1</p></td>
<td><p>2019/04/10</p></td>
<td><p>Windowsユーザ認証に対応 中継サーバ経由接続の諸元拡大</p>
<p>クリップボードデータの自動共有化</p>
<p>Windows Server 2019対応</p></td>
</tr>
</tbody>
</table>

## 関連項目

  - [NEC](../Page/日本電気.md "wikilink")
  - [Express5800](https://ja.wikipedia.org/wiki/Express5800 "wikilink")

## 外部リンク

  - [WinShare](http://jpn.nec.com/websam/winshare/)

[Category:日本電気の製品](https://ja.wikipedia.org/wiki/Category:日本電気の製品 "wikilink") [Category:リモートデスクトップ](https://ja.wikipedia.org/wiki/Category:リモートデスクトップ "wikilink")