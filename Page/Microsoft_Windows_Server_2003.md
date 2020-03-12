> この記事は[Microsoft Windows Server 2003](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2003)から翻訳されています。


**Windows Server 2003**（ウィンドウズ サーバー -）は [マイクロソフト](../Page/マイクロソフト.md "wikilink")が[Windows 2000 Serverの後継として開発した小規模](../Page/Microsoft_Windows_2000.md "wikilink")～大規模[サーバ](../Page/サーバ.md "wikilink")用の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。

## 概要

当初は[Windows XPと同じスケジュールで開発されていて](../Page/Microsoft_Windows_XP.md "wikilink")、Windows 2000同様にサーバ版とクライアント版を同時に完成させる予定であったが、多少開発に遅れが見られていたサーバ版は当時セキュリティ問題が大きく注目されたこともあり、セキュリティ強化も含め完成が見送られた。

それまでの新機能付加をOSのバージョンアップの目玉としてきたマイクロソフトは方針を変更し、より安全な環境を用意することに集中している （[IISのように](../Page/Internet_Information_Services.md "wikilink")、最初から書き直されたものもある）。

出荷までに何度か名称の変更があった。当初は[コード名](../Page/コードネーム.md "wikilink")「Windows Whistler Server」と呼ばれていたが、正式な製品名としては「Windows 2002 Server」という名称を経て「Windows .NET Server」となり、「Windows .NET Server 2003」でいったんは決まりロゴ グッズなども作成された。しかし発売直前にマーケティング上の理由でキャンセルされて表題どおりの正式名称となった。

2005年6月にx86プロセッサの64ビット拡張に対応したWindows Server 2003 x64 Editionsがリリースされ、Windows Server 2003を基にしたクライアント版のWindows XP Professional x64 Editionも合わせてリリースされた。同年12月にWindows Server 2003 R2がリリースされた。

## Windows Server 2003 Feature Packs

マイクロソフトはこのバージョンにおける新しいツールや特徴・機能を「Feature Packs」という形で無償ダウンロード提供をおこなっている。その内容は以下の通りである。

  - Active Directory Application Mode
  - Active Directory のユーザーおよびコンピュータ向けの Remote Control Add-on
  - Automated Deployment Services (ADS)
  - Directory Services Markup Language (DSML) Services for Windows
  - Identity Integration Feature Pack
  - Linux Guest Support for Virtual Server 2005 R2 （Virtual Machine Additions for Linux とも呼ばれる）
  - Scalable Networking Pack
  - [Virtual Server 2005 R2](../Page/Microsoft_Virtual_Server.md "wikilink")
  - [Windows Server Update Services](../Page/Windows_Server_Update_Services.md "wikilink")
  - [Windows Services for UNIX](https://ja.wikipedia.org/wiki/Services_for_UNIX "wikilink")
  - Windows Rights Management サービス（及びクライアント）
  - [Windows SharePoint Services](https://ja.wikipedia.org/wiki/Windows_SharePoint_Services "wikilink")
  - Windows システム リソース マネージャ
  - [グループ ポリシー管理コンソール](https://ja.wikipedia.org/wiki/グループポリシー "wikilink")
  - シャドウ コピー クライアント

## Windows Server 2003 R2

Windows Server 2003 Service Pack 1 をベースに開発されたもの。[2005年](../Page/2005年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")にリリースされた。内部での特に目立った変更は無いが、R2 では新機能がセットになった別インストール ディスクとして提供されている。R2 のいくつかの新機能は R2 以外でも利用できるよう提供されている。

R2では、今まであった機能の向上から、[UNIX](../Page/UNIX.md "wikilink") の機能の利用を可能にしたり、仮想化やそれに伴う OS ライセンス契約内容の改訂といったものまで、さまざまな変更が行われている。

なお、R2 は初期版の Windows Server 2003 とは別製品であり、正式にアップグレード権を持っていない場合、Windows Server 2003 から Windows Server 2003 R2 へのアップグレードは行えない。

## サービス パックに関して

### Service Pack 1

[2005年](../Page/2005年.md "wikilink")[4月19日](../Page/4月19日.md "wikilink")に公開した\[1\]。今までの形式のサービスパック同様、バグの修正に加えて以下の様な変更や強化があった。Service Pack 1 で導入された変更と強化はWindows XP Service Pack 2 から大方取り込んでいるものである。

  - [DEP](../Page/データ実行防止.md "wikilink") : [バッファ オーバーフローを利用したコンピュータへの攻撃を検知して攻撃を防ぐ効果が得られる](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")。ただし、DEP によって"わざと DEP にひっかかる仕組みを意図して利用している"プログラムなどがあるため、一部正常に動作しないプログラムもあるので注意されたい。
  - IIS のメタベース監査 : IISのメタベースの全ての変更を追跡できるようになった。
  - Windows Firewall : 今までにあった Internet Connection Firewall という名であったファイアウォール機能を強化させたもの。インバウンド接続をすべて禁止すると、サーバーとして動作できないため、自動的に有効になることはない。ただし、Service Pack 1と 統合された Windows Server 2003 をインストールした場合、インストール中は Windows Firewall が有効になる。これは Windows XP SP2 と同様の動作である。Windows XP と違うのは、管理者は初回ログオン時に表示される[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")で \[完了\] ボタンを押すことでファイアウォールを明示的に無効にする必要がある点である。
  - [Windows Media Player 10](../Page/Windows_Media_Player.md "wikilink") : Service Pack 1 には Windows Media Player 10 が同梱された。
  - セキュリティ構成ウィザード : サーバーの構成やポリシーの調査をすることで被攻撃対象を減らす手順を踏むことが出来るようになっている。
  - リモート アクセス検疫 : 企業ネットワークに接続する必要があるコンピュータ（クライアント コンピュータ）がネットワークの資源を利用できるようにする前に、あらかじめ企業ネットワークの求める構成になっているか確認することが出来るようになった。
  - 新しい ファイル システム フィルタ マネージャ\[2\]

### Service Pack 2

[2007年](../Page/2007年.md "wikilink")[3月27日](../Page/3月27日.md "wikilink")に公開した\[3\]。Service Pack 1 ほど大きな仕様の変更は無いが、Feature Packs から MMC 3.0 や Scalable Networking Pack が統合され、新しいコマンドライン ツール、Windows Vista の展開のサポートにネットワーク面も強化されている。

このService PackはWindows Server 2003 R2にも適用可能であるが、無印やSP1のWindows Server 2003に適用してもR2の新機能は搭載されない。

## エディションの種類

アップグレード対象製品は Windows NT Server 4.0、Windows 2000 Server、Windows 2000 Advanced Serverのみ。ただし、Windows 2000 Advanced ServerからWindows Server 2003 Standard Editionにする事はできない。

  - Web Edition
    Web サービスやホスティング サービスを目的としたフロントエンド用途である。IIS 6.0 が利用される環境を想定して設計されており、このエディションは CAL([:en:Client Access License](https://ja.wikipedia.org/wiki/:en:Client_Access_License "wikilink")) を必要としていない。OS 単体では販売されておらず、Web サーバー ファーム用のハードウェアとともに OEM 提供となっており、64 ビット版は提供されていない。
  - Standard Edition
    中小企業向けまたは大企業等で利用される[ファイル サーバーや](../Page/ファイルサーバ.md "wikilink")[プリント サーバーを目的とした小規模サーバー用途である](../Page/プリントサーバ.md "wikilink")。Active Directory などサーバー サービスは取り揃えている。
  - Enterprise Edition
    [SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") の使用や e コマースを目的としたバックエンド サーバー用途である。Standard Edition と比べてクラスタリングなどの高度な機能をサポートしている。
  - Datacenter Edition
    高度な信頼性や拡張性、可用性が必要な環境で使用される。
  - Compute Cluster Server
    [スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")などの[高性能数値演算](https://ja.wikipedia.org/wiki/高性能数値演算 "wikilink")[クラスタを必要とするアプリケーションの利用を想定して設計されたもの](../Page/コンピュータ・クラスター.md "wikilink")。x64 版のみのリリース。
  - Small Business Server
    [Exchange Server](../Page/Microsoft_Exchange_Server.md "wikilink") や [ISA Server](https://ja.wikipedia.org/wiki/Microsoft_Internet_Security_and_Acceleration_Server "wikilink") 等がセットになっている [SOHO](https://ja.wikipedia.org/wiki/Small_Office/Home_Office "wikilink") 等の小規模なビジネス環境用。製品としては安く機能が豊富だが、CAL 等に若干の決まりごとがある。Active Directory のインストールが必須要件であり、AD フォレスト内で単独のドメインしか構成できない制約がある。そのため、AD を削除したり、他ドメインと信頼関係を結ぶことは出来ない。また、後に発売された [Windows Home Server](../Page/Microsoft_Windows_Home_Server.md "wikilink") の基にもなっている。
  - Storage Server Edition
    Windows Powered Network Attached Storage (Windows Powerd NAS) の後継製品に当たり、Windows Server 2003 を基にしたストレージ機器 ([NAS](../Page/ネットワークアタッチトストレージ.md "wikilink")) 向けである。プロセッサ・メモリの上限は明記されておらず、ハードウェアとともに OEM 提供（[プリインストール](../Page/プリインストール.md "wikilink")）となっている。

## システム要件

<table>
<tbody>
<tr class="odd">
<td><table>
<caption>Windows Server 2003 システム要件[4]</caption>
<thead>
<tr class="header">
<th></th>
<th><p>最小システム要件</p></th>
<th><p>推奨システム要件</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Web</p></td>
<td><p>Standard</p></td>
<td><p>Enterprise</p></td>
</tr>
<tr class="even">
<td><p>プロセッサ</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>周波数</p></td>
<td><p>133 MHz</p></td>
<td><p>133 MHz (x86),<br />
1400 MHz (x64)</p></td>
</tr>
<tr class="even">
<td><p>認識数</p></td>
<td><p>2</p></td>
<td><p>4</p></td>
</tr>
<tr class="odd">
<td><p>メモリ</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>最低</p></td>
<td><p>128 MB</p></td>
<td><p>512 MB</p></td>
</tr>
<tr class="odd">
<td><p>最大 (32 ビット)</p></td>
<td><p>2 GB</p></td>
<td><p>4 GB</p></td>
</tr>
<tr class="even">
<td><p>最大 (64 ビット)</p></td>
<td></td>
<td><p>32 GB</p></td>
</tr>
<tr class="odd">
<td><p>ハード ディスク空き容量</p></td>
<td><p>1.5 GB</p></td>
<td><p>1.25 ～ 2.0 GB (x86),<br />
4.0 GB (x64)</p></td>
</tr>
<tr class="even">
<td><p>ディスク装置</p></td>
<td><p>CD-ROM または DVD-ROM ドライブ</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>ディスプレイ</p></td>
<td><p>VGA またはコンソール リダイレクションをサポートするハードウェア</p></td>
<td><p>SVGA</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

## 脚注

## 外部リンク

  -
[Category:Windows_Server](https://ja.wikipedia.org/wiki/Category:Windows_Server "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")

1.
2.  [The new Filter Manager feature is available in Windows 2000](http://support.microsoft.com/kb/894608/ja)
3.
4.  [Windows Server 2003 システム要件](http://www.microsoft.com/japan/windowsserver2003/evaluation/sysreqs/)