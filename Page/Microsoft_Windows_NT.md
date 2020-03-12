> この記事は[Microsoft Windows NT](https://ja.wikipedia.org/wiki/Microsoft_Windows_NT)から翻訳されています。


**Microsoft Windows NT**（マイクロソフト ウィンドウズ エヌティー）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。DECが手がけたVMSのアーキテクチャを基礎としており、開発もDECの元社員が全面的に行い、リリースに至っている。

[Windows 9x系といったWindowsファミリーのオペレーティングシステムより安定性に優れている](../Page/Windows_9x系.md "wikilink")。[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink") 以降はOSの名称からNTは外されたものの、OSとしてはWindows NTのバージョン5以降であり、現在の[Windows 10](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")(Windows NT ver10.0)に至るまでWindowsNTは継続した製品シリーズである。

## 概要

Windows NTは[MS-DOS](../Page/MS-DOS.md "wikilink")上の拡張シェルである[Windows 3.x系はもちろんWindows](https://ja.wikipedia.org/wiki/Windows_3.x "wikilink") 9x系とも違う完全32ビット・[プリエンプティブなマルチタスクOSであり](../Page/マルチタスク.md "wikilink")、Win9xとは別に新規に開発された新しいOSである。

設計の要素の多くは[デヴィッド・カトラー](../Page/デヴィッド・カトラー.md "wikilink")や一緒に入社した[DECの開発者の影響があり](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、[VMSの要素が反映されている](../Page/OpenVMS.md "wikilink")。OSのカーネル領域と[アプリケーション領域を分離して管理する構造で](../Page/アプリケーションソフトウェア.md "wikilink")、Windows 9x系に比べて高い安定性を確保していたが、その分だけ高いマシンスペックを要求した。このため、Windows 9x系が家庭用と位置付けられていたのに対し、Windows NT系は業務用として位置付けられていた。

安定した動作を要求される業務用途をメインに考えて設計された為か、Windows NT 4.0までは[Windows 9x系に比べて](../Page/Windows_9x系.md "wikilink")[マルチメディア](../Page/マルチメディア.md "wikilink")系の機能やゲーム[APIの](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")（Windows NT 4.0で一部対応）、[ACPIや](../Page/Advanced_Configuration_and_Power_Interface.md "wikilink")[PnP](../Page/プラグアンドプレイ.md "wikilink")、[USBや](../Page/ユニバーサル・シリアル・バス.md "wikilink")[IEEE 1394等の新しい規格への対応はなされていなかった](../Page/IEEE_1394.md "wikilink")。

## NTの意味

マイクロソフトはNTを「New Technology」の略としている\[1\]。しかし、後継の[Windows 2000においてブート時のロゴ画面上に](../Page/Microsoft_Windows_2000.md "wikilink")「Built on NT Technology」という文章が書かれており、この説だとすると「New Technology Technology」となり[Technologyが重なってしまう](../Page/RAS症候群.md "wikilink")。1998年の[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")へのインタビュー\[2\]によれば、「NT」の本来の意味は「New Technology」であった一方で、長い期間を経てその意味は薄れ、「NT」は単純にハイエンド向けのWindowsを指すようになったと説明している。他に、カトラーが先に開発した[VMSの一歩先を行くという意味で](../Page/OpenVMS.md "wikilink")、それぞれアルファベット順での次の文字にしたWNTとするためだろうという説\[3\]や、「NT」は、開発元のMicrosoftの略称「MS」のアルファベット上での次の文字になっているという説、初期の開発名称 i860エミュレータ'N10 (N-Ten)'の略との説などがある。\[4\]

## バージョンの変遷及びそれぞれの特徴

[IBM](../Page/IBM.md "wikilink")と共同で開発していた[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")のバージョン2の次期バージョンをWindows NTとし、IBMとは別に製品を開発していくこととなる。最初のバージョンは3.1であり、これ以前に発売されていた[Windows 3.1と互換性があるため](../Page/Microsoft_Windows_3.x.md "wikilink")、Windows NTの最初のバージョンも3.0ではなく3.1として発売した。これはWindows3.1と歩調を揃えるという、マーケティング上の理由による。

以下、英語版の発売年を併記する。

### Windows NT 3.1（1994年）

初期バージョン。[コードネーム](../Page/コードネーム.md "wikilink")はWNT。デスクトップ シェルとしてWindows 3.1と同じ[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")を採用していた。英語版は[1993年](../Page/1993年.md "wikilink")[7月27日](../Page/7月27日.md "wikilink")に発売された。[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")版、[MIPS版](../Page/MIPSアーキテクチャ.md "wikilink")、[Alpha版がある](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")（日本語版では、x86版、Alpha版のみ提供された）。Windows NT 3.1は、スタンドアロンおよびメンバーサーバーとして利用できる。同時期に発売されたWindows NT Advanced Server 3.1 は[ドメインコントローラ](../Page/ドメインコントローラ.md "wikilink")専用であり、Windows NT 3.5以降のエディションとは考え方が違う。

### Windows NT 3.5（1995年）

コードネームは[Daytona（デイトナ）](https://ja.wikipedia.org/wiki/デイトナ "wikilink")。英語版は[1994年](../Page/1994年.md "wikilink")[9月21日](../Page/9月21日.md "wikilink")に発売された。メモリ消費量の低減および処理速度の向上が図られており、NTを動作させるためのハードウェアのハードル引き下げに貢献した。また、[NTFSでしか利用出来なかった長いファイル名を](../Page/NT_File_System.md "wikilink")[FAT16で利用可能にした最初のOSである](https://ja.wikipedia.org/wiki/File_Allocation_Table#FAT16 "wikilink")。このコードネームを冠した[β版](../Page/ベータ版.md "wikilink")（正確には[リリース候補版](https://ja.wikipedia.org/wiki/リリース候補版 "wikilink")）が雑誌付録のCD-ROMで大量に配布され\[5\]注目を集めた。

### Windows NT 3.51（1996年）

英語版は[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")[5月30日](../Page/5月30日.md "wikilink")に発売された。Windows 95との[APIの共通化を図ると共に](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、NTFSではファイルの圧縮機能をサポートした。また[PowerPC](../Page/PowerPC.md "wikilink")版が追加された。

### Windows NT 4.0（1996年）

[Windows 95から継承した](../Page/Microsoft_Windows_95.md "wikilink")[GUIを採用した](../Page/Windows_Explorer.md "wikilink")。同時に[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")2のサポートなども行われている。その最大の特徴として、これまでの3.x系では[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")アーキテクチャにのっとり、低い[特権レベルで動作していたグラフィック関連のデバイスドライバを](../Page/リングプロテクション.md "wikilink")、OSのカーネルと同レベルである特権レベル0で動作させるようになった点が挙げられる。結果として、これまで大きな不評を浴びてきた、グラフィック処理の遅さについてのパフォーマンスは大幅に改善したが、その代償としてグラフィックデバイスのデバイスドライバのバグ、ハングアップによって最悪の事態ではOS全体の破壊が引き起こされ得るなど、システムの堅牢性やマイクロカーネルとしての実装理念としては3.xシリーズより大きく後退している。

NTはこの措置によってグラフィック描画速度の向上や[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")への対応が可能となり、商業的な成功への道筋をつけることができた。のちに、NT系列OSのグラフィック関連のデバイスドライバが特権レベル0で動作するという構造は、[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、[Windows Server 2008のリリース時に](../Page/Microsoft_Windows_Server_2008.md "wikilink")、本来のNT3.1方式の実装に改められている。

本来NT 4.0としてオールチンの手によって開発が進められていた[Cairoプロジェクトの失敗も加わり](https://ja.wikipedia.org/wiki/Cairo_\(オペレーティングシステム\) "wikilink")、メジャーバージョンアップであるVer 4.0を名乗るようになった。\[6\]

開発コードネームは当初、Cairoと名付けられていたが、結果的にCairoとして開発されていた完全オブジェクト指向OSの開発が頓挫したため4.0に名前を譲られた形となっている。その後CairoのコードネームはNT 4.0の後継にあたるNT 5.0（[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")）へ、Cairoプロジェクトの思想の一部は[WinFS](../Page/WinFS.md "wikilink")へそれぞれ受け継がれた。

## 出荷・販売本数の推移

### Windows NT 3.1

  - [1993年](../Page/1993年.md "wikilink")[7月27日](../Page/7月27日.md "wikilink") - 英語版発売\[7\]
  - [1993年](../Page/1993年.md "wikilink")[9月25日](../Page/9月25日.md "wikilink") - （発売60日）20万本出荷\[8\]
  - [1993年](../Page/1993年.md "wikilink")[11月4日](../Page/11月4日.md "wikilink") - （発売100日）25万本出荷\[9\]
  - [1994年](../Page/1994年.md "wikilink")[1月28日](../Page/1月28日.md "wikilink") - 日本語版発売\[10\]
  - [1994年](../Page/1994年.md "wikilink")[1月28日](../Page/1月28日.md "wikilink") - 30万本
  - [1994年](../Page/1994年.md "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink") - （発売1年）公称50万本販売\[11\]（日本では7000本）
  - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink") - 60万本

### Windows NT 3.5

  - [1994年](../Page/1994年.md "wikilink")[9月21日](../Page/9月21日.md "wikilink") - 英語版発売\[12\]
  - [1994年](../Page/1994年.md "wikilink")[12月8日](../Page/12月8日.md "wikilink") - 日本語版発売\[13\]

### Windows NT 3.51

  - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")[5月30日](../Page/5月30日.md "wikilink") - 英語版発売\[14\]
  - [1996年](../Page/1996年.md "wikilink")[1月19日](../Page/1月19日.md "wikilink") - 日本語版発売

### Windows NT 4.0

  - [1996年](../Page/1996年.md "wikilink")[9月3日](https://ja.wikipedia.org/wiki/9月3日 "wikilink") - 英語版発売\[15\]
  - [1996年](../Page/1996年.md "wikilink")[12月10日](../Page/12月10日.md "wikilink") - 日本語版発売\[16\]

## 脚注

## 関連項目

  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - [ReactOS](../Page/ReactOS.md "wikilink") - Windows NTとバイナリレベル・ドライバレベルでの互換性を確保することを目標とした、[オープンソース](../Page/オープンソース.md "wikilink")プロジェクト
  - [Wine](../Page/Wine.md "wikilink") - Windows APIを他のOSで動かそうというオープンソースのプログラム及びプロジェクト

## 外部リンク

  - [マイクロソフト - ホーム](http://www.microsoft.com/ja-jp)
  - [Windows NT Workstation ホーム](http://www.microsoft.com/japan/ntworkstation/)  [(Web Archives)](https://web.archive.org/web/20041009114618/http://www.microsoft.com/japan/ntworkstation/)
  - [Windows NT Server 4.0 ホーム](http://www.microsoft.com/japan/ntserver/)  [(Web Archives)](https://web.archive.org/web/20041029014535/http://www.microsoft.com/japan/ntserver/)
  - [マイクロコンピュータの歴史 著作: PSP 内倉憲一](http://www.technetjapan.com/jp/history/index7.htm)  [(Web Archives)](https://web.archive.org/web/20080223091326/http://www.technetjapan.com/jp/history/index7.htm)

[Category:Windows_NT系](https://ja.wikipedia.org/wiki/Category:Windows_NT系 "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")

1.  [Microsoft Windows : Windows of History](https://web.archive.org/web/20051201012934/http://www.microsoft.com/japan/windows/20th/history.mspx)ではNew Technologyの略であると書かれてあり、また[: Word文書 Windows NT Server 4.0 インストール ガイド](https://web.archive.org/web/20100213233004/http://www.microsoft.com/japan/technet/archive/prodtechnol/winntas/deploy/sp6a.mspx)の4ページにも、「NTFS（New Technology File System）その名前のとおり、Windows NT Server 4.0 用に設計されたファイル システムです。」という記述が見られる。
2.
3.  岩淵明男『マイクロソフト・ウインドウズ戦略のすべて』TBSブリタニカ、1993年10月7日初版、ISBN 4484932288、78頁。
4.  開発メンバーの一人 Mark Lucovsky氏の証言。 <http://itpro.nikkeibp.co.jp/free/NT/NEWS/20030127/2/> ( 2016年1月)
5.  [Windows 8の情報公開は、これまでより劣っている？](http://ascii.jp/elem/000/000/697/697355/)、ASCII.jp、2012年5月31日 6時0分更新。
6.  それまではNT 3.51の[シェル](../Page/シェル.md "wikilink")をアップデートしただけのShell Update Release (SUR) と呼ばれており、NT 3.52というバージョンを与えられていた。
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