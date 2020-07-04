> この記事は[Background Intelligent Transfer Service](https://ja.wikipedia.org/wiki/Background_Intelligent_Transfer_Service)から翻訳されています。


**Background Intelligent Transfer Service**（BITS、バックグラウンド インテリジェント転送サービス）は、アイドル中のネットワーク回線の帯域幅を使用し、非同期にマシン間のファイル転送を行う[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の構成の一部である。

[Microsoft Update](../Page/Microsoft_Update.md "wikilink")、[Windows Server Update Services](../Page/Windows_Server_Update_Services.md "wikilink")、[System Management Serverやその他のアプリケーションやWindows](https://ja.wikipedia.org/wiki/System_Management_Server "wikilink") サービスで利用されている。

BITSは[COMコンポーネントとして登録されており](../Page/Component_Object_Model.md "wikilink")、実質どの様なプログラミング言語でも利用できる。

## テクノロジ

BITSは未使用の帯域を利用してファイル転送を行う仕組みである。通常、BITSはバックグラウンドでファイルを転送し、他のアプリケーションでネットワーク帯域を利用する場合、使用しているネットワーク帯域を調整して作業を続ける。たとえば、何らかのアプリケーションが80%のネットワーク帯域を利用する場合、BITSは残りの20%のネットワーク帯域を利用する。 BITSはリジューム機能を備えており、不意な転送の中断が起きても途中から作業の再開を行うことが出来る。

### 転送

BITSは非同期にファイルを転送する。[HTTPまたは](../Page/Hypertext_Transfer_Protocol.md "wikilink")[HTTPS](../Page/HTTPS.md "wikilink")上のデータ転送をサポートしている。

### ジョブ

BITSはファイル転送の管理のためにキューを用いている。BITSはアプリケーションがジョブを作成した時点で開始される。ジョブとはコンテナであり、コンテナには一つ以上のファイルがある。それに発信元および転送先のURIを指定して加える必要がある。 BITSでのダウンロードは複数のファイルの同時転送をサポートするが、アップロードは一度に一つのみのサポートとなっている。 属性はファイル単位で設定することができる。またジョブのセキュリティは作成したアプリケーションのセキュリティコンテキストを継承する。 ジョブを管理には管理するAPIを利用する。プログラム的に開始・停止・休止・再開という状態の遷移をサポートしている。 バックグラウンド転送はBITSによって最適化され、BITS自身がネットワーク帯域の消費が増えるにつれ、転送率を低下させる。

### スケジューリング

BITSのスケジューリングはタイムスライスで管理されており、転送の優先度に応じて時間配分が調整される。また、BITSはエラー回復メカニズムを備えており、致命的または一時的なエラーによってジョブの状態を変更する。一時的なエラーの場合、BITSは元に戻るまで待ち、再試行を試みる。致命的なエラーの場合、ジョブを作成したアプリケーションにジョブのコントロールが移る。

### ツール

コマンドライン用のBITS管理ユーティリティ (bitsadmin.exe) はWindows Server 2003 Service Pack 1 Support Toolsに同梱され、Windows Vistaで同梱された。

## バージョン

<table>
<caption>BITS のバージョン[1]</caption>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>提供日</p></th>
<th><p>含まれた OS</p></th>
<th><p>使用可能 OS</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>2001年10月</p></td>
<td><ul>
<li>Windows XP</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.2</p></td>
<td><p>2002年7月</p></td>
<td><ul>
<li>Windows XP SP1</li>
<li>Windows 2000 SP3</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.5</p></td>
<td><p>2003年4月</p></td>
<td><ul>
<li>Windows Server 2003</li>
</ul></td>
<td><ul>
<li>Windows 2000 SP3</li>
<li>Windows XP</li>
</ul></td>
</tr>
<tr class="even">
<td><p>2.0</p></td>
<td><p>2004年8月</p></td>
<td><ul>
<li>Windows XP SP2</li>
<li>Windows Server 2003 SP1</li>
</ul></td>
<td><ul>
<li>Windows 2000 SP3, SP4</li>
<li>Windows XP, SP1</li>
<li>Windows Server 2003</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2.5</p></td>
<td><p>2006年11月</p></td>
<td><ul>
<li>Windows XP SP3</li>
<li>Windows Vista</li>
<li>Windows Server 2008</li>
</ul></td>
<td><ul>
<li>Windows XP SP2</li>
<li>Windows Server 2003 SP1, SP2</li>
</ul></td>
</tr>
<tr class="even">
<td><p>3.0</p></td>
<td><p>2006年11月</p></td>
<td><ul>
<li>Windows Vista</li>
<li>Windows Server 2008</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.0</p></td>
<td><p>2009年7月</p></td>
<td><ul>
<li>Windows 7</li>
<li>Windows Server 2008 R2</li>
</ul></td>
<td><ul>
<li>Windows Vista SP1, SP2</li>
<li>Windows Server 2008, SP2</li>
</ul></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## マイクロソフト製品以外での主な利用例

  - [BITSync](http://klinkby.wordpress.com/2008/01/19/bitsync/)
  - [Zenworks 7](http://www.novell.com/documentation/zenworks7/dm7install/index.html?page=/documentation/zenworks7/dm7install/data/b3qayj3.html)
  - [KBOX Systems Management Appliance](https://ja.wikipedia.org/wiki/KACE "wikilink")
  - [RSS Bandit](https://ja.wikipedia.org/wiki/RSS_Bandit "wikilink")
  - [EVE-Online](https://ja.wikipedia.org/wiki/EVE-Online "wikilink")
  - [WinBITS](http://www.darvin.de/english/index.html)
  - [Google Gears](https://ja.wikipedia.org/wiki/Google_Gears "wikilink")
  - [Google Pack](https://ja.wikipedia.org/wiki/Google_Pack "wikilink")
  - [Oxygen media platform](https://ja.wikipedia.org/wiki/Oxygen_media_platform "wikilink")

## 脚注

## 外部リンク

  - [MSDN.BITS.What's New](http://msdn2.microsoft.com/en-us/library/aa363167.aspx)

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  \[<http://msdn.microsoft.com/en-us/library/aa363167(VS.85>).aspx What's New (Windows)\]