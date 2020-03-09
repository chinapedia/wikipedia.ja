> この記事は[Microsoft Windows 2000](https://ja.wikipedia.org/wiki/Microsoft_Windows_2000)から翻訳されています。


**Windows 2000**（ウィンドウズ にせん\[1\]）はマイクロソフトが[Windows NT 4.0の後継バージョンとして発表した](https://ja.wikipedia.org/wiki/Microsoft_Windows_NT_4.0 "wikilink")[Windows NT系の](https://ja.wikipedia.org/wiki/Windows_NT系 "wikilink")[オペレーティング システムである](../Page/オペレーティングシステム.md "wikilink")。略称はWin2000、Win2k、W2K。[開発コードネームはCairo](https://ja.wikipedia.org/wiki/コードネーム "wikilink")、NT 5.0\[2\]。

## 概要

Windows 2000は[Windows 9x系に比べて安定性](https://ja.wikipedia.org/wiki/Windows_9x系 "wikilink")・堅牢性に優れた NT[カーネル](../Page/カーネル.md "wikilink")を基に開発された。当初の正式名称は「**Windows NT 5.0**\[3\]」として発表されていたが、後に現在のものに変更された\[4\]。主に業務用として位置付けられている。しかし、開発当初からWindows NT系とWindows 9x系の統合が計画されていたため、一般ユーザーへも十分に対応できるようWindows 9x系のユーザーインターフェイスも取り込まれている\[5\]。

当初の製品版では65000件以上の問題を抱えていた\[6\]と揶揄されたが、数度の[サービスパック](https://ja.wikipedia.org/wiki/サービスパック "wikilink")の適用により、安定性や使い勝手なども登場当初と比べると格段に向上した。当初は各種ドライバ類が少なく、特にマルチメディア関連機器の多くに非対応という弱点を抱えていた。しかし次第に専用もしくは[Windows XP互換のドライバが開発された](../Page/Microsoft_Windows_XP.md "wikilink")。

Windows NT系は移植性を高める設計が行われており、前バージョンのWindows NT 4.0では[PowerPC](../Page/PowerPC.md "wikilink")や[DEC Alphaなどの複数の](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")[プラットフォームに向けて販売されていた](https://ja.wikipedia.org/wiki/プラットフォーム_\(コンピューティング\) "wikilink")。しかしIA-32以外のプラットフォームが事実上消滅してしまったため、Windows 2000ではβ3までは複数存在していたものの、結局IA-32以外の発売は取り止めとなった。ただし後述の「Windows Advanced Server, Limited Edition」についてはIA-64（[Itanium](https://ja.wikipedia.org/wiki/Itanium "wikilink")シリーズ）用が後にリリースされた。また、[PC-9800シリーズ](https://ja.wikipedia.org/wiki/PC-9800シリーズ "wikilink")の対応もWindows 2000を最後に終了した。

Windows 2000はサーバー用とクライアント用が同一の製品名として発売された最後のWindowsではあるが、後期のサーバエディションである「Windows Datacenter Server Limited Edition」や「Windows Advanced Server, Limited Edition」からは「Windows 2000」の名称が外れている。これ以降のWindowsのリリースでも同様に、サーバー用とクライアント用が別のバージョンや別の製品名で別けて発売されている。

2019年1月現在、Windows 2000は企業・法人向けのボリュームライセンス契約者に限定したダウングレード権としてライセンスのみ\[7\]提供が継続されている\[8\]。その他のサポートとしては、それまでに提供された修正モジュールがダウンロードできる「オンラインセルフヘルプサポート」\[9\]があるほか、企業等の契約者に対する有料の「カスタマーサポート」にて新たなOS環境へ移行するための手助けを受けられる。しかし延長サポートがすでに終了しているため、新たな修正モジュールは必ずしも開発されているわけではない。その後もいくつかの更新プログラムが提供されている\[10\]が、無論すべてのhotfixが対応しているわけではなく、Windows 2000では延長サポート中でさえ開発困難なパッチは対応が見送られるケースもあった\[11\]。また充分な動作検証が行われていない場合もある\[12\]。

Windows 2000は主に企業で多く用いられていたため、資金難等の理由からシステム更新の遅れた企業で需要が残るケースが少なくなかった\[13\]。実際、後続OSであるWindows XPのサポートも終了した2014年4月時点ですら、XPを利用して構築されたサーバは世界で6000件程度なのに対し、（サーバエディションの存在する）Windows 2000については50万台ものサーバがなおも稼動しているという\[14\]。さらに、組み込み向けの"Windows 2000 Professional for Embedded Systems"は延長サポートの終了が2010年7月13日までで、ライセンス搭載製品出荷提供可能期間終了の[2015年](https://ja.wikipedia.org/wiki/2015年 "wikilink")[3月31日](https://ja.wikipedia.org/wiki/3月31日 "wikilink")までサポートされるという事情もあった\[15\]。こうした問題に目を付けた一部のセキュリティソフトベンダでは独自サポートを継続する動きも見られ\[16\]、企業向けのセキュリティソフトでは**2016年3月31日までサポートされていた**例\[17\]もある。ただし、そうしたセキュリティベンダでも基本的には新しい環境への移行を推奨している。[独立行政法人](https://ja.wikipedia.org/wiki/独立行政法人 "wikilink")[情報処理推進機構](https://ja.wikipedia.org/wiki/情報処理推進機構 "wikilink")（IPA）も、根本的な解決ではないとしながらもシステム更新までに時間が掛かる場合のつなぎとしてセキュリティツールの使用を指導している。またIPAはこうしたサポートの終了した旧OSのセキュリティ上の危険性を指摘しており、**なるべく、ネットワークに接続しない単独の専用システム（[スタンドアローン](https://ja.wikipedia.org/wiki/スタンドアローン "wikilink")）にしたうえで[USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")や[FD](https://ja.wikipedia.org/wiki/フロッピーディスク "wikilink")、[MO](../Page/光磁気ディスク.md "wikilink")、外付け[HDD等の外部](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")[補助記憶装置](../Page/補助記憶装置.md "wikilink")でデータ交換しない**ことを呼びかけている\[18\]。

| 本数         | 日付                 |
| ---------- | ------------------ |
| 50万本（米国）   | 2000年3月7日発表\[19\]  |
| 100万本（全世界） | 2000年3月14日発表\[20\] |
| 150万本      | 2000年4月20日\[21\]   |

**出荷本数の推移**

## 特徴

### Windows 9x系統からの機能

  - [USBや](../Page/ユニバーサル・シリアル・バス.md "wikilink")[プラグアンドプレイ](https://ja.wikipedia.org/wiki/プラグアンドプレイ "wikilink")による容易な周辺機器の増設
  - [ACPIによる電源管理機能](https://ja.wikipedia.org/wiki/Advanced_Configuration_and_Power_Interface "wikilink")
  - [Windows 98](../Page/Microsoft_Windows_98.md "wikilink")/98 Second Editionと似た[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")（操作性は改良されており、利便性はかなり向上している）
  - [DirectXや](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")[OpenGL](https://ja.wikipedia.org/wiki/OpenGL "wikilink")といったマルチメディア及びゲーム環境への対応または強化
  - [DVD-ROM等の大容量ディスクへの対応](https://ja.wikipedia.org/wiki/DVD#DVD-ROM "wikilink") など

### Windows 2000での新機能

  - [Active Directory](https://ja.wikipedia.org/wiki/Active_Directory "wikilink")
    Active Directoryは、Windows NT 4.0サーバー以前に導入や利用されていた「NT[ドメイン](https://ja.wikipedia.org/wiki/ドメイン_\(ディレクトリサービス\) "wikilink")」に代わる新たな概念として導入された。
  - [NTFS 3.0](https://ja.wikipedia.org/wiki/NT_File_System "wikilink")（NTFS5, NTFS2000）
    Windows NTで採用されている[NTFSにさらなる改良を加えた](https://ja.wikipedia.org/wiki/NT_File_System "wikilink")[ファイル システム](https://ja.wikipedia.org/wiki/ファイルシステム "wikilink")。各ユーザー[アカウント](https://ja.wikipedia.org/wiki/アカウント "wikilink")ごとに使用できるディスク容量を制限できる「ディスク クォータ」が装備された。また、ファイル システムそのものを[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")する機能も搭載され、セキュリティ保護に関連する機能が強化された。
  - Windows/Win32 Driver Model（[WDM](https://ja.wikipedia.org/wiki/Windows_Driver_Model "wikilink")）
    それまで、[デバイスドライバ](https://ja.wikipedia.org/wiki/デバイスドライバ "wikilink")は通常[Windows 95とWindows](../Page/Microsoft_Windows_95.md "wikilink") NTでは異なるものが必要であった。しかし、この問題を解決するためWin32 Driver Modelが導入され、これに従って開発されたドライバはWindows 98/98SE/MeでもWindows 2000でも同じものが使えると謳われた（Windows 95とWindows NT 4.0もしくはそれ以前は未対応）。
    そのほかにも、AT互換機とPC-9800シリーズの間でドライバの互換性が高まるという一面もあった\[22\]。
    しかし、結果的に目論見は失敗し、[Windows Driver Modelへとスケールダウンすることになる](https://ja.wikipedia.org/wiki/Windows_Driver_Model "wikilink")。Windows Driver ModelとWin32 Driver Modelの違いは、ドライバの[バイナリ](https://ja.wikipedia.org/wiki/バイナリ "wikilink")互換（Win32 Driver Model）であるか、[ソース互換](../Page/ソースコード.md "wikilink")（Windows Driver Model）であるかの違いである。
  - 自動インストーラへの対応
    アプリケーションを自動修復できるプログラムがある場合、備え付けのWindowsインストーラ サービスによって自動的に修復される。また、Windows 98 / 98 Second Editionにもあったシステムまたは[レジストリ](https://ja.wikipedia.org/wiki/レジストリ "wikilink")の自動修復機能も強化され、再セットアップ操作を極力排除している。

そのほかにも

  - 日本語版においてシステムフォントとしての全角のひらがなとカタカナの文字幅が小さくなった「MS UI ゴシック」が新たに導入され、ウインドウのメニューバーなどに使用されていた[半角カナ](https://ja.wikipedia.org/wiki/半角カナ "wikilink")が全角カナに統一
  - [コンピュータアクセシビリティ](https://ja.wikipedia.org/wiki/コンピュータアクセシビリティ "wikilink")のサポート
  - [多言語](https://ja.wikipedia.org/wiki/多言語 "wikilink")への対応
  - [グループポリシー](https://ja.wikipedia.org/wiki/グループポリシー "wikilink")によるユーザー管理の一元化
  - [Microsoft 管理コンソールによる一部アプリケーションの統一された操作環境](https://ja.wikipedia.org/wiki/Microsoft_管理コンソール "wikilink")
  - [Microsoft Windows Installer](https://ja.wikipedia.org/wiki/Microsoft_Windows_Installer "wikilink") 1.1の搭載

などの機能追加及び強化が図られた。

## エディション

  - Windows 2000 Professional
    クライアント向けのエディションで、パワー ユーザーやビジネスで使用するデスクトップやラップトップのパソコンを対象にしている。また、組み込み向けの OS として同エディションを基にしたWindows 2000 Professional for Embedded Systemsが出荷された。
  - Windows 2000 Server
    ワークグループや小規模なコンピューティング環境向けのエディションで、IISやActive Directoryといったサーバー サービスが揃っている。
  - Windows 2000 Advanced Server
    基幹システム向けのエディションで、Serverエディションに比べよりクラスタリングのサポートなど高機能な機能を含んでいる。2002年7月にはItanium 2 プロセッサで動作する64ビット版のWindows Advanced Server Limited Edition が発表され、プリインストールされて出荷された\[23\]。
  - Windows 2000 Datacenter Server
    Advanced Serverエディションが対象となるよりも規模が大きなシステム向けのエディションで、プロセッサ数やメモリ容量などが大きなハードウェアをサポートする。Datacenter Edition はパッケージとして販売はされていない。日本語版は提供されていないが、2002年3月にパフォーマンスやスケーラビリティが高いWindows Datacenter Server Limited Edition が出荷された\[24\]。

## サービスパック

サービスパックではないがそれに準ずるものとしてロールアップも複数回登場しているため、時系列上これも併記する。サービスパックはOSバージョンに準ずる扱いであり、それぞれにサポート期間が設定されている。またWindowsコンポーネント追加の際にもサービスパック適用済みのファイルからインストールされる。これに対しロールアップは単に修正プログラム集であり、後からWindowsコンポーネントを追加した際にはそのファイルに対してロールアップは適用されていない\[25\]。またサポート期限も対象サービスパックの期限に依存する。

  - Service Pack 1
    2000年9月8日に公開された\[26\]。[Outlook Expressをバージョン](https://ja.wikipedia.org/wiki/Outlook_Express "wikilink")5.0から5.5に置き換えた。2002年8月1日にサポートが終了した。
  - Service Pack 2
    2001年6月1日に公開された\[27\]。自動的に128ビット暗号機能がインストールされる。また、隠れた機能ではあるが[互換性のないアプリケーションを仮想的に実行する互換性機能が導入される](https://ja.wikipedia.org/wiki/Microsoft_Windows_XP#Windows_9x系との互換性 "wikilink")（別途使用可能にするための操作が必要になる）。2004年6月30日にサポートが終了した。
      - Service Pack 2用の更新プログラム セキュリティロールアップパッケージ 1（SRP1）
        2002年1月30日に公開された\[28\]。SP2以降から当時までのセキュリティ関連のアップデートをまとめたもの。SP3以降には含まれている。
  - Service Pack 3
    2002年8月9日に公開された\[29\]。[反トラスト訴訟に基づく実装として](https://ja.wikipedia.org/wiki/反トラスト法 "wikilink")、Windows XP Service Pack 1 で実装したプログラムの追加と削除内に[ウェブ ブラウザや](../Page/ウェブブラウザ.md "wikilink")[電子メール クライアント等の](https://ja.wikipedia.org/wiki/電子メールクライアント "wikilink")、特定のアプリケーションを[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")製アプリケーションに差し替える「プログラムのアクセスと既定の設定」を実装した。また、[Microsoft Java VMの削除や](https://ja.wikipedia.org/wiki/Java仮想マシン "wikilink")、別途レジストリの操作が必要だが（つまりインストール時点では未対応）[137GB以上のハードディスク（48bit LBA）に対応した](https://ja.wikipedia.org/wiki/Advanced_Technology_Attachment#48bit_LBA\(BigDrive\) "wikilink")。2005年6月30日にサポートが終了した。
  - Service Pack 4
    2003年7月3日に公開された\[30\]。新たに[DVD-Audioのほか](https://ja.wikipedia.org/wiki/DVD#DVDオーディオ "wikilink")[USB 2.0や](https://ja.wikipedia.org/wiki/ユニバーサル・シリアル・バス#USB_2.0 "wikilink")[IEEE 802.11の規格に標準ドライバで対応した](https://ja.wikipedia.org/wiki/IEEE_802.11 "wikilink")。2010年7月13日にサポートが終了した。
      - Service Pack 4 用の更新プログラム ロールアップ 1（SP4 Rollup 1）
        2005年6月28日に公開された\[31\]。Service Pack 4公開からの約2年分に公開した修正プログラムをまとめたもので、追加で新しいファイル システム フィルタ マネージャが導入された\[32\]。しかしリリース後にいくつかの不具合が報告されたため、報告された不具合に対処したパッケージSP4 Rollup 1 v2が2005年9月14日に再度公開されて置き換えられた\[33\]。
  - Service Pack 5（中止）
    2004年11月に開発が中止され、Service Pack 4のロールアップ（SP4 Rollup 1 v2）をもって替えることが決定された\[34\]。

## システム要件

| エディション                                | Professional                         | Server                    | Advanced Server          | Datacenter Server |
| ------------------------------------- | ------------------------------------ | ------------------------- | ------------------------ | ----------------- |
| [プロセッサー](../Page/CPU.md "wikilink")   | 速度                                   | 133 MHz以上のPentium互換プロセッサー | Pentium III Xeon またはそれ以上 |                   |
| 最大搭載数                                 | 2                                    | 4                         | 8                        | 8                 |
| [物理メモリー](../Page/主記憶装置.md "wikilink") | 最低                                   | 32 MB（64 MB以上を推奨）         | 128 MB（256 MB以上を推奨）      |                   |
| 最高                                    | 4 GB                                 | 4 GB                      | 8 GB                     | 32 GB             |
| ストレージ                                 | 850 MB以上の空き容量のある2 GBのもの              | 1 GB以上の空き容量のある2 GBのもの     |                          |                   |
| 画面解像度                                 | 640 x 480                            |                           |                          |                   |
| 光学ドライブ                                | CD-ROMまたはDVD-ROMドライブ                 |                           |                          |                   |
| その他                                   | Microsoft Mouseまたは互換性のあるポインティング デバイス |                           |                          |                   |

Windows 2000（IA-32版）ハードウェア仕様要求

## 旧バージョンからのアップグレード / アンインストール

Windows 2000 Professionalは本来、[Windows NT 3.51](../Page/Microsoft_Windows_NT.md "wikilink") Workstationと[Windows NT 4.0](https://ja.wikipedia.org/wiki/Microsoft_Windows_NT_4.0 "wikilink") Workstationからのアップグレードを想定しているが、[Windows NT系列のOSと](https://ja.wikipedia.org/wiki/Windows_NT系 "wikilink")、[Windows 9x系列のOSは](https://ja.wikipedia.org/wiki/Windows_9x系 "wikilink")[Win32](https://ja.wikipedia.org/wiki/Win32 "wikilink")という共通の[APIを備えている為](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[Windows 95](../Page/Microsoft_Windows_95.md "wikilink")、[Windows 98](../Page/Microsoft_Windows_98.md "wikilink")（Second Edition含む）、[Windows Meからでもアップグレードは可能](https://ja.wikipedia.org/wiki/Microsoft_Windows_Me "wikilink")。ただし、どのバージョンからアップグレードしても、旧バージョンに戻す事（[アンインストール](https://ja.wikipedia.org/wiki/アンインストール "wikilink")）はできない（Windows 2000には元々アンインストール機能が備わっていないため）。なお、**Windows 2000 Professional 期間限定アップグレード**パッケージ（Windows 95/98/98SEからのアップグレード）もあった。また、Windows MeはWindows 2000よりも後にリリースされているので本来ならアップグレード対象になっていないはずだったが、Microsoftから2001年2月に正式にWindows MeもWindows 2000のアップグレード対象OSとして認められた。ただし、アップグレードインストールはサポートされておらず、フォーマットしての新規インストールのみがサポートされている。一応、Windows MeからWindows 2000にアップグレードインストールする事自体はできるが、Windows Meからアップグレードすると、Windows Meに備わっていた一部の機能（システムの復元など）が利用できなくなる。また、通常パッケージ版ではWindows 3.1及びそれ以前のOSからはアップグレードできない。

Windows 2000 ServerとWindows 2000 Advanced Serverへは、Windows NT Server 3.51と4.0からのみアップグレード可能。また、Windows 2000の異なるバージョン間でのアップグレードはサポートされていない（Windows 2000 ProfessionalからWindows 2000 Serverにアップグレードする事はできず、その逆もできない。ただし、新規インストールは可能）。

[アカデミックパックでは](https://ja.wikipedia.org/wiki/アカデミックパッケージ "wikilink")「優待アップグレード版」という形態が取られており、上記に加えWindows 3.1も正式なアップグレード対象に含まれた。さらに他社OSもアップグレード対象であり、パッケージのシールでは具体例として[UNIX](../Page/UNIX.md "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")および[Macintosh](../Page/Macintosh.md "wikilink")が挙げられている。すなわちコンピュータシステムごと乗り替える「アップグレード」も想定されている。無論これらはライセンスの話であり、インストールについては通常版と同様に（Windows 95/98/98SE/NT以外からの）アップグレードインストールはサポートされておらず新規インストールしかできない。ちなみにこの「優待アップグレード版」CDから新規インストールを開始すると、アップグレード版であるにも関わらず、旧バージョンのインストールメディアの挿入を要求されない（通常のアップグレード版から新規インストールを開始すると、途中でアップグレード対象製品のCDの挿入を要求されるはずである）。

ボリュームライセンス版ではクライアントOS（Windows 2000の場合はProfessional）について、最新OSへのアップグレードライセンス（に付随するWindows 2000へのダウングレード権）として提供されている。そのアップグレード対象は契約内容によって異なり、場合によっては一部の他社OSがアップグレード対象になることもある。やはりWindows 95/98/98SE/NT以外からのアップグレードインストールはサポートされていない。

## 新しいバージョンへのアップグレード / アンインストール

Windows 2000がアップグレード元OSの場合、そのバージョンによってアップグレード先が異なるのが特徴である。Windows 2000 Professionalからアップグレードする場合と、Windows 2000 Server及びWindows 2000 Advanced Serverからアップグレードする場合とでアップグレード先が変わる（Windows 2000 ServerとWindows 2000 Advanced Serverは基本的にアップグレード先が共通だが、Windows 2000 Advanced Serverからアップグレードする場合、[Windows Server 2003の下位エディション](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2003 "wikilink")（Standard）にはアップグレードできないので注意）。

Windows 2000 Professionalからは[Windows XP Professionalか](../Page/Microsoft_Windows_XP.md "wikilink")[Windows Vistaにのみアップグレードする事ができる](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。ただし、Windows Vistaへは直接アップグレードする事ができず、新規インストールを行う必要がある。Windows 2000からアップグレードによって（環境を引き継いで）Windows Vistaにしたい場合、間にWindows XP Professionalを挟む必要がある。Windows XP Home Editionにはアップグレードできない（セットアップ開始時に強制終了してしまうので、CD-ROMから起動しないと新規インストールも行えない）。故にWindows 2000 Professionalから直接アップグレードできるのは、Windows XP Professionalのみとなる。なお、日本語版のみ、Windows 2000 Professionalのみからアップグレード可能の、**Windows XP Professional 期間限定特別アップグレード版**もあった。

一方、Windows 2000 Server及びWindows 2000 Advanced ServerからはWindows Server 2003か[Windows Server 2008にのみアップグレード可能](https://ja.wikipedia.org/wiki/Windows_Server_2008 "wikilink")。ただし、Windows 2000 ProfessionalからWindows Vistaにするのと同様、Windows 2000 Server及びWindows 2000 Advanced ServerからいきなりWindows Server 2008にする事はできない。間にWindows Server 2003を挟むか、新規インストールをする必要がある。

また、両バージョン間に互換性は無い為、Windows 2000 ProfessionalからWindows Server 2003にアップグレードしたり、Windows 2000 ServerやWindows 2000 Advanded ServerからWindows XP Professionalにアップグレードする事はできない（いずれもの場合もそのバージョンからセットアップを起動しての新規インストール及び、CD-ROMから起動しての新規インストールは可能）。

Windows 2000がアップグレード元OSの場合、基本的にどのバージョンからどのバージョンにアップグレードしても、新しいバージョンを[アンインストール](https://ja.wikipedia.org/wiki/アンインストール "wikilink")してWindows 2000に戻す事はできない。

## 脚注

### 注釈

### 出典

## 外部リンク

  -
[Category:Windows_NT系](https://ja.wikipedia.org/wiki/Category:Windows_NT系 "wikilink") [Category:2000年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2000年のソフトウェア "wikilink")

1.  「Windows 2000」の読みは[Windows XP Professionalに収録されている](../Page/Microsoft_Windows_XP.md "wikilink")「Windows XP ツアー」の動画を参照。
2.
3.  なお後述のように後期の[IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink")(Itanium)版サーバについては2000ベースでありながら内部バージョンが5.1であり、この影響で[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")版[XPや](../Page/Microsoft_Windows_XP.md "wikilink")[Server 2003は](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2003 "wikilink")5.2を名乗っている。
4.
5.  開発段階において、すでに[Neptune等の一般ユーザー向けOSが並行開発されていた](https://ja.wikipedia.org/wiki/Microsoft_Windows_Neptune "wikilink")。後にNeptuneで予定されていた一部の機能は9x系の[Windows Meで実現し](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")、最終的に[Whistlerで統合されることとなった](../Page/Microsoft_Windows_XP.md "wikilink")。
6.
7.  インストールCDの提供は既に終了している。
8.
9.  マイクロソフトのサポート ライフサイクルにあるビジネス向け製品のオンラインセルフヘルプサポート期間は「製品が出荷されてから最短10年間」であり、「最短年数」を経過した製品では完全にはサポートされない場合がある。
10. 例えば[2011年9月](http://www.microsoft.com/ja-jp/download/details.aspx?id=27315)・[2012年8月](http://www.microsoft.com/ja-jp/download/details.aspx?id=30629)・[2013年2月](http://www.microsoft.com/ja-jp/download/details.aspx?id=36707)といったセキュリティリリースにはいくつか含まれていることが確認できる。
11.
12. 例えば[KB2803751](http://support.microsoft.com/hotfix/KBHotfix.aspx?kbnum=2803751&kbln=ja)などは特定の不具合が無ければ導入しないことが推奨されている。
13.
14.
15. 例えば[東京エレクトロンデバイス](https://esg.teldevice.co.jp/product/microsoft/schedule.html)、[岡谷エレクトロニクス](https://www.oec.okaya.co.jp/product/embedded/microsoft-embedded/support)、[菱洋エレクトロ](https://www.ryoyo.co.jp/microsoft/microsoft-5/)、[アヴネット](https://www.avnet.co.jp/maker/Microsoft.aspx)。
16. 例えば2012年になって日本市場に本格参入した[ALYac](https://ja.wikipedia.org/wiki/ALYac "wikilink")に至っては、当時すでにWindows 2000が延長サポート終了後2年も過ぎていたにもかかわらず動作対象に含めており、2018年9月現在も現行製品となっている。
17.  - ただし新規販売は2013年3月末で終了。
18.
19.
20.
21.
22. 例えば[玄人志向](https://ja.wikipedia.org/wiki/玄人志向 "wikilink")の複合機能PCIカード「CHANPON3」は日本国外のAT互換機用パーツのOEM販売品であるが、PC-9800シリーズでサウンド機能を使う場合はWDMドライバを使うように指示されていた([インターフェースボード CHANPON3(2015年10月29日時点のアーカイブ)](https://web.archive.org/web/20151029192950/http://archive.kuroutoshikou.com/products/chanpon3/chanpon3.html))。
23.
24.
25.
26.
27.
28.
29.
30.
31.
32. [新フィルタマネージャ機能は、Windows 2000で使用できます。](http://support.microsoft.com/kb/894608/ja)
33.
34.