> この記事は[Samba](https://ja.wikipedia.org/wiki/Samba)から翻訳されています。


**Samba** （サンバ） は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Windowsネットワークを実装した](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")。 [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[BSD](../Page/BSD.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")などの[Unix系](../Page/Unix系.md "wikilink")[OS](../Page/オペレーティングシステム.md "wikilink") を用いて、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") の[ファイルサーバ](../Page/ファイルサーバ.md "wikilink")や[プリントサービス](../Page/プリントサーバ.md "wikilink")、ドメインコントローラ機能、ドメイン参加機能を提供する。

[1992年](../Page/1992年.md "wikilink")、[アンドリュー・トリジェル](https://ja.wikipedia.org/wiki/アンドリュー・トリジェル "wikilink")によって最初のバージョンが開発され、後に[GPL v2にて公開された](https://ja.wikipedia.org/wiki/GNU_General_Public_License#バージョン2 "wikilink")。 3.2系からは[GPL v3へ移行した](https://ja.wikipedia.org/wiki/GNU_General_Public_License#バージョン3 "wikilink")。

## 特長

**Samba**は12のサービスと12の[通信プロトコル](../Page/通信プロトコル.md "wikilink")の実装で、[CIFS](../Page/Server_Message_Block.md "wikilink")、[NetBIOS](https://ja.wikipedia.org/wiki/NetBIOS "wikilink") over TCP/IP (NetBT)、[SMB](../Page/Server_Message_Block.md "wikilink")/CIFS、[DCE/RPC](https://ja.wikipedia.org/wiki/DCE/RPC "wikilink")のほか、MSRPC、NetBIOSネームサーバ (NBNS) として知られる[WINS サーバ](https://ja.wikipedia.org/wiki/Windows_Internet_Naming_Service "wikilink")、NT ドメインログオンを含めた NT ドメインプロトコルスイート、セキュアアカウントマネージャ (SAM) データベース、ローカルセキュリティ認証 (LSA) サービス、NT プリントサービス (SPOOLSS)、そしてバージョン3では（[ケルベロス認証](https://ja.wikipedia.org/wiki/ケルベロス認証 "wikilink")と [LDAP](../Page/Lightweight_Directory_Access_Protocol.md "wikilink") に対応した） [Active Directoryへのドメイン参加機能が含まれている](https://ja.wikipedia.org/wiki/Active_Directory "wikilink")（AD参加機能によってUNIX/Linux上でのユーザ管理が不要になる）。

大雑把には、UNIX機をクライアントあるいは共有ファイルサーバとしてWindowsネットワークへ参加させる機能の他、[Windows NT 4.0サーバの機能と](../Page/Microsoft_Windows_NT.md "wikilink")、バージョン3では一部[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink") / [2003サーバの機能を持つ](../Page/Microsoft_Windows_Server_2003.md "wikilink")（例えば、VSS:ボリュームシャドウコピー機能など）。 本家の[Windows Serverと異なり](../Page/Windows_Server.md "wikilink")、本体価格やサーバに接続する[クライアント分のライセンス](../Page/クライアント_\(コンピュータ\).md "wikilink")\[1\]コストなどが一切不要であることや、アクセス権の指定など一部機能は本家を上回る部分もあるため、官公庁、大学、大企業を中心にSambaを導入する例も増えている。また、[Mac OS X v10.6.8まではSambaの機能によって](../Page/Mac_OS_X_v10.6.md "wikilink")、Windowsネットワーク環境でのファイル共有やドメイン参加を実現していた\[2\]が、[Mac OS X Lionからは取り去られて独自実装のsmbdに置き換えられている](https://ja.wikipedia.org/wiki/Mac_OS_X_Lion "wikilink")\[3\]。

## 名前の由来

**Samba**という名前は、[Windowsで使用されているネットワークファイルシステム](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")「[SMB](../Page/Server_Message_Block.md "wikilink") (Server Message Block)」に、2 つの母音を入れて作られている。**Samba**はもともと「smbserver」と呼ばれていたが、SMBserver の商標をもつSyntax\[4\]から登録[商標](../Page/商標.md "wikilink")であるとの通告があったため、名前が変更された。

## 主な機能

### ファイルサーバ

共有フォルダと呼ばれるサーバ側の空間に、ファイルを格納する機能。[NAS](../Page/ネットワークアタッチトストレージ.md "wikilink") としての機能を果たす。

[アクセス権を設定できるため](https://ja.wikipedia.org/wiki/アクセス制御 "wikilink")、特定のユーザに同じファイルを提供するといった用途が実現できる。 [ACLをサポートする環境なら](https://ja.wikipedia.org/wiki/アクセス制御リスト "wikilink")、ユーザやグループ毎に細かく[アクセス権を指定することも可能](https://ja.wikipedia.org/wiki/アクセス制御 "wikilink")。 Windowsサーバと比べて、「$」で終わる共有名でなくても隠し共有にできる利点がある。（隠し共有…共有名の検索やリストアップを行っても画面に現れないが、正しい名前を指定すればアクセスできる共有フォルダ）

### プリントサーバ

Windowsクライアント向けの[プリントサーバ](../Page/プリントサーバ.md "wikilink")機能。

共有[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")の提供やプリンタ[ドライバの配布を行う](../Page/デバイスドライバ.md "wikilink")。

### Windowsドメインコントローラ

Windows NT 4.0サーバで提供される機能で、[NT ドメインと呼ばれるネットワーク領域内で](https://ja.wikipedia.org/wiki/NT_ドメイン "wikilink")、ユーザやクライアントコンピュータの管理を行う機能。**Samba** 2.2から提供された。

ユーザアカウントやコンピュータアカウント、[アクセス権などの情報を中央集権的に管理し](https://ja.wikipedia.org/wiki/アクセス制御 "wikilink")、ユーザ認証や[シングルサインオン](../Page/シングルサインオン.md "wikilink")などの[サービス](../Page/サービス.md "wikilink")を提供する。

  - プライマリドメインコントローラ (PDC) : ユーザアカウントやコンピュータアカウントなどの、データの原本を持つコンピュータ。
    バックアップドメインコントローラ (BDC) : PDCのデータのコピーを持つコンピュータ。
    ドメインメンバ : PDC の認証を受けたコンピュータや、そのコンピュータを利用するユーザ。

ドメインメンバ（利用者側）からは、PDCとBDCは同じ機能を提供しているように見える。 BDCはバックアップの機能を提供しているため、ドメイン内に存在しなくても構わない。同じドメイン内にPDCとBDCが両方存在している場合、ドメインメンバは原則としてBDCにサービスの提供を依頼する。

**Samba** はPDC / BDCの機能を提供することができ、NT ドメイン内にメンバとして参加することもできる。ただし、WindowsサーバとSambaではアカウント情報の同期の取り方が異なるため、同じドメイン内でWindowsサーバのPDCとSambaのBDCを運用すること、或いはその逆はできない。（なおバージョン3からユーザやグループなどの属性を保持したまま、NT 4.0ドメインからSambaドメインへの移行がサポートされた。）

### Active Directory ドメインメンバ

Windows 2000サーバ以降から提供される[Active Directoryドメインへのドメインメンバとしての参加機能](https://ja.wikipedia.org/wiki/Active_Directory "wikilink")。**Samba** 3から提供された。

[Active Directoryは前述のNT](https://ja.wikipedia.org/wiki/Active_Directory "wikilink") ドメインに代わるもので、既存のネットワーク技術を応用して構成されている。ユーザアカウントなどの管理情報を[LDAPディレクトリサービスに格納し](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")、認証機構に[ケルベロス](https://ja.wikipedia.org/wiki/ケルベロス認証 "wikilink")、[名前解決](https://ja.wikipedia.org/wiki/名前解決 "wikilink")に[DNS](../Page/Domain_Name_System.md "wikilink")、管理情報の配布やコピーに[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")のみを使用する。

### Active Directory ドメインコントローラー

2012年12月にリリースされたSamba 4より[Active Directoryドメインのドメインコントローラー機能がサポートされている](https://ja.wikipedia.org/wiki/Active_Directory "wikilink")。

### smbclient

[UNIX](../Page/UNIX.md "wikilink")側から[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")**Samba**の共有フォルダに接続するための[クライアント](../Page/クライアント_\(コンピュータ\).md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")。

標準的なコマンドラインプログラム[FTPのような操作で](../Page/File_Transfer_Protocol.md "wikilink")、共有フォルダに接続し、ファイルを操作することができる。

### libnss_wins

[Name Service SwitchへWINSサーバーと](https://ja.wikipedia.org/wiki/Name_Service_Switch "wikilink")137/udpのブロードキャストを使ったホスト名解決を行うライブラリの提供。

## バージョン履歴

Samba 3.0までの歩みは「[Sambaの10年](http://wiki.samba.gr.jp/mediawiki/index.php/Samba%E3%81%AE10%E5%B9%B4)」を参照。

<table>
<thead>
<tr class="header">
<th><p>リリース日</p></th>
<th><p>バージョン</p></th>
<th><p>概要</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td></td>
<td><p>メジャーアップグレード。Samba 3.0系の最後のリリースはSamba 3.0.36。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>GPL2からGPL3にライセンス変更。ファイルサービスの従来の最大1,024バイトというパス名、および最大256バイトのファイル名という制約がなくなり、ホストOSで設定した値までの文字列が扱えるようになった[5]。</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>クラスタサポートや管理ツールが強化[6]。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>Samba 3とSamba 4ソースコードの両方を含む最初のリリース。デフォルトではSamba 4のビルドは無効[7]。</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Server_Message_Block#SMB2" title="wikilink">SMB2の実験的サポートを含む最初のリリース</a>[8]。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Server_Message_Block#SMB2" title="wikilink">SMB2を完全にサポートする最初のブランチ</a>[9]。</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>SambaをActive Directoryドメインコントローラにして、Windows Active Directoryドメインに完全に参加できる[10]。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Server_Message_Block#SMB_3.0" title="wikilink">SMB3のサポート</a>[11]。</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Btrfs" title="wikilink">Btrfs</a>ベースのファイル圧縮、スナップショット、 <a href="https://ja.wikipedia.org/wiki/winbind" title="wikilink">winbind</a>統合[12]。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>新しいロギング機能、SMB 3.1.1サポート[13]。</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>非同期フラッシュリクエスト[14]。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>NTLM v1はデフォルトで無効、バーチャルリストビュー(VLV)、さまざまなパフォーマンス改善[15]。</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>マルチプロセス<a href="https://ja.wikipedia.org/wiki/Netlogon" title="wikilink">Netlogon</a>のサポート[16]。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>Samba ADとMIT <a href="https://ja.wikipedia.org/wiki/Kerberos_(protocol)" title="wikilink">Kerberos</a>[17]</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>[18]</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>[19]</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>Python 3のフルサポート。preforkプロセスモデルの改良[20]。</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>セキュリティ更新[21]。</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 脚注

<references/>

## 関連項目

  - [Server Message Block](../Page/Server_Message_Block.md "wikilink") (SMB)
  - [Windows Internet Naming Service](https://ja.wikipedia.org/wiki/Windows_Internet_Naming_Service "wikilink") (WINS)
  - [Active Directory](https://ja.wikipedia.org/wiki/Active_Directory "wikilink")

## 外部リンク

  -
  - [日本Sambaユーザ会](http://wiki.samba.gr.jp/)

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [Client Access Licenseのことである](https://ja.wikipedia.org/wiki/Client_Access_License "wikilink")
2.  [OS X 10.5における設定](http://docs.info.apple.com/article.html?path=Mac/10.5/jp/8201.html)（アップル）
3.  [Sambaを取り去ったOS X Lion、その影響は……](http://builder.japan.zdnet.com/os-admin/os-x-lion11/35006283/)
4.  TotalNET Advanced Server という製品などを販売している。
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.