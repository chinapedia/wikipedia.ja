> この記事は[Windows Defender](https://ja.wikipedia.org/wiki/Windows_Defender)から翻訳されています。


**Windows Defender**は元々はWindowsの[マルウェア対策ソフトであったが](https://ja.wikipedia.org/wiki/アンチウイルスソフトウェア "wikilink")、Windows 10のver.1709 (Fall Creators Update) 以降はMicrosoftがWindows向けに提供するセキュリティ機能のシリーズ名となり\[1\]、これに合わせてマルウェア対策ソフトの方は**Windows Defender ウイルス対策**と名称を変更した。

## シリーズ名としてのWindows Defender

下記のものを含んでいる\[2\]：

| 名称                                                                                     | 概要                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Windows Defender Security Center                                                       | セキュリティ関連のクライアントインターフェース\[3\]                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows Defender ウイルス対策                                                                | [マルウェア対策ソフト](https://ja.wikipedia.org/wiki/アンチウイルスソフトウェア "wikilink")                                                                                                                                                                                                                                                                                                                                                                                                       |
| Windows Defender Offline                                                               | ブータブル[CD](../Page/コンパクトディスク.md "wikilink")/[DVD](../Page/DVD.md "wikilink")、または[USBフラッシュドライブ](https://ja.wikipedia.org/wiki/USBフラッシュドライブ "wikilink")にマルウェア駆除用のシステムをインストールし、Windows起動中に検出や削除ができないマルウェアに対処するために提供されている。                                                                                                                                                                                                                                                      |
| Windows Defender Smart Screen                                                          | 既報告済の悪意のある可能性のあるサイトにアクセスしようとしたり悪意のある可能性のあるファイルをダウンロードしようとしたりすると警告する\[4\]。                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Windows Defender Firewall](https://ja.wikipedia.org/wiki/Windows_Firewall "wikilink") | [パーソナルファイアウォール](../Page/パーソナルファイアウォール.md "wikilink")                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Windows Defender Exploit Guard\[5\]                                                    | Exploit Protection                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ASR（Attack Surface Reduction、攻撃表面の縮小）                                                  | 「Office ベースやスクリプトベース、電子メールベースの脅威をブロックし、マシンにマルウェアが侵入することを」防ぐ\[6\]                                                                                                                                                                                                                                                                                                                                                                                                           |
| ネットワーク保護                                                                               | 「Windows Defender SmartScreenを使って、デバイスから信頼されていないホストやIPへのアウトバウンドプロセスをブロック」\[7\]                                                                                                                                                                                                                                                                                                                                                                                             |
| フォルダー アクセスの制御                                                                          | 「信頼されていないプロセスによる、保護されたフォルダーへのアクセスをブロック」\[8\]する事による[ランサムウェア](https://ja.wikipedia.org/wiki/ランサムウェア "wikilink")対策\[9\]。                                                                                                                                                                                                                                                                                                                                                      |
| Windows Defender Device Guard                                                          | アプリケーションやデバイスドライバのホワイトリスト機能\[10\]。アプリケーションやデバイスドライバに正当な署名が付いている事を確認した上でこれらを実行する\[11\]。「グループポリシーの「コードの整合性ポリシーを展開する」を使って、あらかじめ指定したアプリケーションだけしか動作しないように設定」する事も可能\[12\]。カーネルモードで動くバイナリをチェックする「カーネルモードのコードの整合性(Kernel Mode Code Integrity:KMCI)」とユーザーモードで動くバイナリをチェックする「ユーザーモードのコードの整合性(User Mode Code Integrity:UMCI)」からなっている\[13\]。　Windows Storeで配布されているアプリケーションは配布段階で署名が必須である\[14\]。また[PKIを用意して既存のアプリケーションに署名を行ってもよい](https://ja.wikipedia.org/wiki/公開鍵基盤 "wikilink")\[15\]。 |
| Windows Defender Application Control                                                   | 「ユーザーの実行が許可されるアプリケーションと、システム コア (カーネル) で実行されるコードを制限することによって」\[16\]、「ファイルベースのマルウェア (.exe、.dll など) 」\[17\]の脅威を軽減                                                                                                                                                                                                                                                                                                                                                             |
| Windows Defender Credential Guard                                                      | Active Directoryの資格情報を管理する[セキュリティ認証サブシステム](https://ja.wikipedia.org/wiki/:en:Local_Security_Authority_Subsystem_Service "wikilink")(Local Security Authority Subsystem Service : LSASS)をVSM側で実行し、さらに暗号化鍵をTPM(ない場合はUEFI)で保護する事で、Windowsの特権が攻撃者に取られても、Pass-the-Hash攻撃などで資格情報が窃取されないようにする\[18\]\[19\]。                                                                                                                                                                        |
| Windows Defender Application Guard                                                     | 「Microsoft Edge または Internet Explorer のいずれかから非信頼サイトを表示すると、Microsoft Edge では分離された Hyper-V 対応コンテナーに含まれるサイトが」開く\[20\]                                                                                                                                                                                                                                                                                                                                                         |
| Windows Defender Advanced Threat Protection                                            | EDR(Endpoint Detection and Response)\[21\]                                                                                                                                                                                                                                                                                                                                                                                                                                 |


\== Windows Defender ウイルス対策 ==

### 歴史

Windows Server 2003 | related_components = }}Windows Defenderはマイクロソフトが[2004年](../Page/2004年.md "wikilink")[12月17日](../Page/12月17日.md "wikilink")に買収を発表した [GIANT Company Softwareの](https://ja.wikipedia.org/wiki/:en:GIANT_Company_Software "wikilink")[GIANT AntiSpywareを基に開発したものである](https://ja.wikipedia.org/wiki/:en:GIANT_AntiSpyware "wikilink")。 もともとのGIANT AntiSpywareは[Windows 9xをサポートしたが](https://ja.wikipedia.org/wiki/Windows_9x系 "wikilink")、Windows Defenderではサポートしていない。しかし、GIANT Company Softwareとパートナーであった[Sunbelt Softwareは同じエンジンを搭載した](https://ja.wikipedia.org/wiki/Sunbelt_Software "wikilink")[Counterspy](https://ja.wikipedia.org/wiki/Counterspy "wikilink")と呼ばれる製品を販売しており、これはWindows 9xでの使用をサポートしている。

#### Beta

Beta 1は[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[1月7日](../Page/1月7日.md "wikilink")にMicrosoft AntiSpywareという名前でリリースされた。機能はGIANT AntiSpywareとあまり変わらず、基本的に[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")が変更されただけのものである。インストールするためには[Windows Genuine Advantage](../Page/Windows_Genuine_Advantage.md "wikilink") (WGA) の確認を必要とする。 Beta 2から名前が「Windows Defender」と改名され（日本では「Windows 防御ツール」とされたが、後に「Windows Defender」となった）、[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[2月14日](../Page/2月14日.md "wikilink")にリリースされた。 Beta 1とは比較にならないほどのさまざまな変更が行われた。 エンジンは[C++](../Page/C++.md "wikilink")で書き直された（GIANT AntiSpywareは[Visual Basic言語で書かれていた](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")）。 また、Beta 2では Windows サービスとして動作するように変更することにより、ユーザーがログインしていない時でもコンピュータを保護できるようになった。Beta 2ではGIANT AntiSpywareより多くのエントリーを保護できるようになった。さらに、Beta 2ではBeta 1に比べて直観的なインタフェースとなった。Beta 2でもWGAの確認を必要とする。マイクロソフトは後に[ドイツ語](../Page/ドイツ語.md "wikilink")版と[日本語](../Page/日本語.md "wikilink")版をリリースした。 なお、Beta版の時点では[Windows 2000はサポートされていた](../Page/Microsoft_Windows_2000.md "wikilink")。

#### 正式版

[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[10月25日](../Page/10月25日.md "wikilink")に英語版が正式公開され、[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[11月10日](../Page/11月10日.md "wikilink")に日本語版が正式公開された。多少の猶予期間を経た後、それまでの版はデジタル証明書の有効期限切れとして使えなくなり、アップデート適用が必須となった。マイクロソフトはWindows Defenderの正式版がWindows XP、Windows Server 2003をサポートすると発表した。

#### ブランド化

日本マイクロソフト株式会社はWindows 10 ver.1709 (Fall Creators Update) に合わせて行われた法人向け説明会の場でそれまでのアンチウイルスソフトとしての「Windows Defender」を「Windows Defender ウイルス対策」と改め、「Windows Defender」の名称をセキュリティ対策全般のブランド名として使用すると発表した\[22\]\[23\]。


\=== Windows Vista仕様の機能 ===

#### リアルタイム保護

Windows Defenderのリアルタイム保護機能はオプションで以下の機能がある。

  - 自動的に起動
    Windows起動時にモニタプログラムを動作させることが出来る。
  - システムの構成（設定）
    Windowsの構成（設定）をモニタする。
  - Internet Explorerのアドオン
    [Internet Explorer](../Page/Internet_Explorer.md "wikilink") (IE) 起動時にIEのアドオンをモニタする。
  - Internet Explorerの構成（設定）
    IEの構成（設定）をモニタする。
  - Internet Explorerのダウンロード
    IE でダウンロードするプログラムやファイルをモニタする。
  - サービスとドライバ
    各サービスやドライバをモニタする。
  - アプリケーションの実行
    アプリケーション起動時や実行時にアプリケーションをモニタする。
  - アプリケーションの登録
    WindowsやWindowsにアプリケーションを登録するプログラムやファイルをモニタする。
  - Windowsのアドオン
    Windowsのアドオンモニタープログラム（別名: ソフトウェアユーティリティ）。

#### ソフトウェア エクスプローラ

ソフトウェア エクスプローラはスタートアッププログラムや現在起動しているプログラム、ネットワークに接続しているプログラム、[Winsock](../Page/Winsock.md "wikilink")プログラムを表示出来るWindows Defenderの一部。

### Windows 8仕様の機能

Windows 8から[Microsoft Security Essentialsと同等の](https://ja.wikipedia.org/wiki/Microsoft_Security_Essentials "wikilink")[アンチウイルス](https://ja.wikipedia.org/wiki/アンチウイルス "wikilink")機能が含まれ\[24\]、それ以外の機能もWindows Vistaまでの仕様からMicrosoft Security Essentialsと同等のものになった\[25\]。

### Windows 10仕様の機能

Windows 10 ver.1607 (Aniversary Update) まで従来通りのユーザインタフェースとなっているが設定機能はWindowsの設定に移された。

Windows 10 ver.1607からWindows起動時に検索できるWindows Defender Offline機能の追加、スキャン結果がアクション センターに通知されるなどの機能が追加された\[26\]。

Windows 10 ver.1703 (Creators Update) ではWindows Defenderは大幅にリニューアルされてアプリが[UWPアプリとなり](https://ja.wikipedia.org/wiki/ユニバーサルWindowsプラットフォーム "wikilink")、名称が「Windows Defender セキュリティセンター」となった。

Windows 10 ver.1709 (Fall Creators Update) では、[Windows Defender Exploit Guard](https://docs.microsoft.com/ja-jp/windows/threat-protection/windows-defender-exploit-guard/exploit-protection-exploit-guard)（およびそのサブセットのWindows Defender Exploit protection）として、[Enhanced Mitigation Experience Toolkit](https://ja.wikipedia.org/wiki/Enhanced_Mitigation_Experience_Toolkit "wikilink") (EMET) として提供してきた機能が統合されている。

## Windows Defender Offline

Microsoft Standalone System Sweeperという製品の後継として、ブータブル[CD](../Page/コンパクトディスク.md "wikilink")/[DVD](../Page/DVD.md "wikilink")、または[USBフラッシュドライブ](https://ja.wikipedia.org/wiki/USBフラッシュドライブ "wikilink")にマルウェア駆除用のシステムをインストールし、Windows起動中に検出や削除ができないマルウェアに対処するために提供されている。Microsoft Security Essentialsと同じエンジンが組み込まれている。定義ファイルはネットワークに接続することができるならば更新することができるが、CD/DVDの場合は更新することができない。マイクロソフトは以前作成したCD/DVDのWindows Defender Offlineのディスクの再利用を推奨していない。

Windows10 Anniversary Updateでは設定アプリから直接実行できるようになった。



## 脚注

## 外部リンク

  - [Microsoft セキュリティ](https://www.microsoft.com/ja-jp/security/)
  - [Microsoft セーフティとセキュリティ センター](https://www.microsoft.com/ja-jp/safety/)
  - [Windows Defender](https://www.microsoft.com/ja-jp/safety/tools/defender.aspx)

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:2006年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2006年のソフトウェア "wikilink")

1.
2.
3.
4.
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
22.
23.
24.
25.
26.