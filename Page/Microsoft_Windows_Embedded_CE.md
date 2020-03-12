> この記事は[Microsoft Windows Embedded CE](https://ja.wikipedia.org/wiki/Microsoft_Windows_Embedded_CE)から翻訳されています。


**Windows Embedded Compact** （ウィンドウズ エンベデッド コンパクト）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した[組み込み機器向けの](../Page/組み込みシステム.md "wikilink")32[ビット](../Page/ビット.md "wikilink")の[マルチタスク](../Page/マルチタスク.md "wikilink")/[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink") (RTOS)。一般にはHandheld PCや[Pocket PC](../Page/Pocket_PC.md "wikilink")　SHARPBrainなどの[PDAで使われている](../Page/携帯情報端末.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) として知られている。[1996年](../Page/1996年.md "wikilink")[11月](../Page/11月.md "wikilink")に発表されている。近年は[PND](../Page/PND.md "wikilink")にも採用されている\[1\]。バージョン 6.0 では **Windows Embedded CE** 、バージョン 5.0 までは、**Windows CE** と呼ばれていた。

## 概要

[Windows 9x系や](../Page/Windows_9x系.md "wikilink")[Windows NT系等と共に](../Page/Windows_NT系.md "wikilink")、Windowsファミリーに属する。[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") (PC) 用[Windowsと異なりOSのみで一般に販売されることはなく](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、対象となる装置に組み込んで使用することを前提としている。また、組み込み用OSとしてWindows Embeddedファミリーにも位置する。かつてのPC用の[Windows NTのように](../Page/Microsoft_Windows_NT.md "wikilink")、複数の[CPU](../Page/CPU.md "wikilink")[アーキテクチャに対応する](../Page/コンピュータ・アーキテクチャ.md "wikilink")。

OSとしては[windowsNT2.X](https://ja.wikipedia.org/wiki/windowsNT2.X "wikilink")から仮想記憶やメモリー量を制限し、APIや機能を絞り込むなど徹底的に軽量化されたものに必要な機能のみを付加するシステムになっており、86系に特化した[ノンプリエンプティブ](https://ja.wikipedia.org/wiki/ノンプリエンプティブ "wikilink")なWindows9Xと異なりWindowsNTと同様に完全な[プリエンプティブ](https://ja.wikipedia.org/wiki/プリエンプティブ "wikilink")、[マルチタスク](../Page/マルチタスク.md "wikilink")、[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")の[リアルタイムOS](https://ja.wikipedia.org/wiki/リアルタイムOS "wikilink")である。このため一部のダイアローグがWindowsNT2.Xのものと類似している。

初期のWindowsNTの特色である高い移植性が保たれており、[ARM](https://ja.wikipedia.org/wiki/ARM "wikilink")、[SuperH](../Page/SuperH.md "wikilink")をはじめとした様々なCPUアーキテクチャーに対応している。WindowsCE6.Xからはカーネルが近代化され、メモリーは2GB、プロセス数は32000までに拡張され、プロセスのカーネル階層への移動など負荷の重いタスクへの対応や高速化が図られている。

組み込み用という性格上、機器を開発するメーカがその機器に不要な機能は削除し必要な機能のみを選んで搭載することも可能である。このため、利用者からは、Windows CEが搭載されていることを意識することなく使える機器を作ることもできる。業務用専用端末や、[セットトップボックス](../Page/セットトップボックス.md "wikilink")等で用いる場合は、このようにして必要な機能を搭載する。また、実装した機能によって対価の[ロイヤリティ](https://ja.wikipedia.org/wiki/ロイヤリティ "wikilink")が変動する。

必要な機能のみを選択して搭載することができるという特徴を生かして、Windows CEを搭載する[POSレジや](../Page/販売時点情報管理.md "wikilink")、[ビデオプロジェクタ](../Page/プロジェクタ.md "wikilink")、[カーナビ](../Page/カーナビゲーション.md "wikilink") (Windows CE for Automotive)、[ゲーム機](../Page/ゲーム機.md "wikilink")（[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")）、ポータブルAVプレーヤー (Portable Media Center)、シンクライアント端末 (Windows-based Terminal、Smart Display) なども存在する。これらにはPDAに見られるようなOSとしての[GUIを実装していないものも多いが](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、レジでは最近タッチパネルを搭載してボタンと[組み込みOSの操作で作業の効率化を図る傾向がある](../Page/組み込みオペレーティングシステム.md "wikilink")。

なお、これらの端末にも[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") (PC) 用[Windowsと同様に](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Windowsのライセンスシールが貼り付けられる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 名称

「CE」の名称は[家電を意味するConsumer](../Page/家庭用電気機械器具.md "wikilink") Electronicsの略と言われているが、マイクロソフトによると、「CEは何かしらの略語ではないが、"Compact," Connectable," Compatible," "Companion," and "Efficient."（小さく、つなぎやすく、互換性のある、つきあえる、効率的なもの）の意味合いがある」と説明している\[2\]。

## バージョン

[300px](https://ja.wikipedia.org/wiki/ファイル:Windows_CE_Timeline.png "wikilink") 改良により、機能追加のほか、リアルタイムイベントでの応答速度の向上などが行われている。

  - Windows CE 1.0 (Pegasus)
  - Windows CE 2.0, 2.11, 2.12 (Mercury)
  - Windows CE 3.0 (Cedar)
  - Windows CE .NET 4.0 (Talisker)
      - Windows CE .NET 4.1 (Jameson)
      - Windows CE .NET 4.2 (McKendric)
  - [Windows CE 5.0](https://ja.wikipedia.org/wiki/Windows_CE_5.0 "wikilink") (Macallan)
  - Windows Embedded CE 6.0 (Yamazaki)
  - Windows Embedded Compact 7 (Chelan)
  - Windows Embedded Compact 2013

CE 4.0 から CE 6.0 までのコードネームは有名な[ウィスキー](https://ja.wikipedia.org/wiki/ウィスキー "wikilink")の名前より取られている。

### Windows Embedded CE 6.0

次世代バージョンとして、Version 6.0が開発された。5.0までは、 プロセス数は最大32個に制限され、そして各プロセスの仮想アドレス空間は32MBに制限されていた。6.0ではプロセス数制限は最大32000個までに拡張され、各プロセスの仮想アドレス空間は2GBまでに広げられる。これにより大量のメモリを消費する[アプリケーションが実現可能になる](../Page/アプリケーションソフトウェア.md "wikilink")。またカーネルは上位2GBのアドレス空間に置かれ、従来ユーザープロセスだった[GWES](https://ja.wikipedia.org/wiki/GWES "wikilink")、[ファイルシステム](../Page/ファイルシステム.md "wikilink")、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")はカーネル空間に統合される。これにより従来プロセス切り替え[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")がAPI呼び出しに伴っていたが、これも[システムコール](../Page/システムコール.md "wikilink")という形になり高速化される。特にネットワークへのアクセス速度は大幅に高速化されるとしている。

### Windows Embedded Compact 7

CE 6.0 の発展バージョンとして開発されたWindows Embedded Compact 7 は 8物理コアまでの[%E5%AF%BE%E7%A7%B0%E5%9E%8B%E3%83%9E%E3%83%AB%E3%83%81%E3%83%97%E3%83%AD%E3%82%BB%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0](https://ja.wikipedia.org/wiki/%E5%AF%BE%E7%A7%B0%E5%9E%8B%E3%83%9E%E3%83%AB%E3%83%81%E3%83%97%E3%83%AD%E3%82%BB%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0 "wikilink")、3GBまでの物理メモリ空間サポート、NDIS 6.1ベースのネットワークスタック、[.NET Compact Framework](../Page/.NET_Compact_Framework.md "wikilink") v3.5 が特徴である。また Silverlight for Windows Embedded によるUI開発が可能になった\[3\]\[4\]。

### Windows Embedded Compact 2013

Compact 7の後継として、2013年6月に一般利用可能となった。 サポートするCPUの種類としてはx86およびARMv7T2が必要とされ、MIPS系、およびARMv5、ARMv6までのアーキテクチャサポートは削除された。

開発環境として[Visual Studio 2012 update2](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio#Visual_Studio_2012 "wikilink") 以降および [Visual Studio 2013](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio#Visual_Studio_2013 "wikilink")、[Visual Studio 2015が利用可能である](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio#Visual_Studio_2015 "wikilink")。ARMコンパイラは[Windows RT用に用意されたものと同じARMコンパイラが利用される](https://ja.wikipedia.org/wiki/Microsoft_Windows_RT "wikilink")。そのため(ARMでもx86でも) C++0x 拡張が利用可能である。

UI開発手法として上記Visual Studio 同梱のRAD開発ツール、**Blend for Visual Studio**の利用が推進された一方で、これまでのHPC Shell機能やコントロールパネルUIはサポートが削除された。.NET Compact Frameworkとしては v3.9がサポートされている。

## アプリケーション開発環境

Windows Embedded CEのアプリケーション開発は、現在ではネイティブコード開発とマネージドコード開発の2とおり開発手法が用意されている。

### ネイティブコード開発

CPUのネイティブコードでプログラムの実行ファイル（DLLまたはEXE）を作成する方法がネイティブコード開発である。ネイティブコード開発ではデスクトップPC用の[Win32 APIのサブセットが利用可能である](https://ja.wikipedia.org/wiki/Win32_API "wikilink")。またデータベースやリモートツール関連でCE独自のAPIも用意されている。文字列を使用するAPIはほとんどの場合[UNICODE](https://ja.wikipedia.org/wiki/UNICODE "wikilink")バージョンのみが用意され、ANSIバージョンも用意されているAPIはCランタイム系や[Winsock](../Page/Winsock.md "wikilink")関連など一部にとどまる。

Windows CEではこれまでに以下のCPUアーキテクチャがサポートされていたことがある。

  - [MIPS系CPU](../Page/MIPSアーキテクチャ.md "wikilink") - MIPS32、MIPSII、MIPSIIFPなど
  - [ARM系CPU](../Page/ARMアーキテクチャ.md "wikilink") - ARMv4、ARMv4I、ARMv5、ARMv6、ARMv7
  - [SuperH](../Page/SuperH.md "wikilink")シリーズCPU - SH3、SH3DSP、SH4
  - [PowerPC](../Page/PowerPC.md "wikilink")
  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink") - x86、x86EM

これ以外に、CEFと呼ばれる仮想マシンコードを利用した開発が一時サポートされていたが\[5\]、このコンセプトはCE 4.0以降のマネージドコード開発へと引き継がれていった。

ネイティブコード開発ツールとしては当初 Visual Studio 6.0にアドオンして使用する Windows CE Toolkit for Visual C++/Visual Basic 5.0や2003 が使用されたが、Windows CE 3.0以降では無償で入手できる eMbedded Visual Tools 3.0 / eMbedded Visual C++ 4.0 が利用されるようになった。CE5 / 6.0 / Compact7 では Visual Studio 2005 / Visual Studio 2008 Pro以上でネイティブコード開発が行われるようになったが、これらの開発製品は有償で入手する必要があった。

Compact 2013 の場合、Visual Studio 2012/2013/2015 のPro以上、または無償で入手できる[Community Editionに](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio#Community "wikilink")、[Application Builder](https://www.microsoft.com/en-us/download/details.aspx?id=38819)をAdd On して利用する。

### マネージドコード開発

マイクロソフトの[.NET Framework構想に準じたアプリケーション開発の手法をマネージドコード開発という](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。Windows CEのマネージドコード実行環境は[.NET Compact Frameworkと呼ばれる](../Page/.NET_Compact_Framework.md "wikilink")。これはデスクトップPC向け[.NET Frameworkのサブセットであり](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、一部共通のクラスライブラリが用意される\[6\]。開発言語としては[C\#および](../Page/C_Sharp.md "wikilink")[Visual Basic(.NET)がサポートされている](../Page/Visual_Basic.md "wikilink")。

  - .NET Compact Framework v1.0

<!-- end list -->

  - .NET Compact Framework v2.0

<!-- end list -->

  - .NET Compact Framework v3.5

当初はマネージドコード開発のみのためにVisual Studio ( Visual C\# / Visual Basic ) 2003 が利用された(ネイティブコード開発はできなかった)が、その後の Visual Studio 2005 および Visual Studio 2008 では一つの環境でネイティブコード開発とマネージドコード開発の両方が可能になった。

### RAD開発

Windows Embedded CE 6.0 R3 や Compact 7 / 2013 ではアプリケーション開発手法として Silverlight for Windows Embedded が利用可能である。これは[Expression Blend](https://ja.wikipedia.org/wiki/Microsoft_Expression_Blend "wikilink") または \[<https://msdn.microsoft.com/ja-jp/library/jj171012(v=vs.110>).aspx Blend for Visual Studio\] を利用して作成したデザインにC++で開発した処理コードを組み合わせるという、ハイブリッドな開発手法である。

### デバッグ手法

作成したアプリケーションの動作確認は、PC上で実行するCE[エミュレータ](../Page/エミュレータ.md "wikilink")、または[シリアルケーブルや](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")[LAN経由で](../Page/Local_Area_Network.md "wikilink")[ActiveSyncや](../Page/Microsoft_ActiveSync.md "wikilink")[Windows Mobile Device Centerにより接続したターゲット機にリモートで](../Page/Microsoft_ActiveSync.md "wikilink")、それぞれダウンロードして行う。

Windows CE 2.x/3.0の時代には、Windows PC上のWin32 APIに変換する形で動作するWindows CEエミュレータが用意されていた。このAPIエミュレータを利用するには、デバッグ時に一時的にx86コードを生成する必要があった。

Windows CE 5.0/6.0 や Windows Mobile 5.0/6.xの世代では ARMコードで動作するエミュレータが用意され、ARM実機用と同じバイナリをエミュレータでそのまま動かすことができた。

Compact7 や Compact 2013では[Windows Virtual PCを利用して動作するデバッグ用OSイメージ作成用のBSP](https://ja.wikipedia.org/wiki/Microsoft_Virtual_PC#Windows_Virtual_PC_.E6.97.A5.E6.9C.AC.E8.AA.9E.E7.89.88 "wikilink")(VCEPC)が提供され、実機と接続するのと同じイーサネット接続を利用してデバッグすることができる。ただしWindows Virtual PCで動作するデバッグ用OSをビルドするためにもそれなりのスキルが要求されるため、あまり一般的とは言えない。

### その他の開発製品

  - [Visual CE](https://ja.wikipedia.org/wiki/Visual_CE "wikilink")：データベース・アプリケーション開発ツール。ソフトウエアマネジメントから1998年5月12日に発売\[7\]。開発元は、アメリカの SYWARE の製品。

## プラットフォーム開発環境

Windows CE はその初期よりマイクロソフトの組み込み向けOS製品としての利用を計画されていた。やがて出荷された以下のツールキットを使用すると、ユーザーは独自のWindows CE OSを開発しカスタム機器向けの組み込みOSとして利用することができるようになった\[8\]。

  - Windows CE 2.11 ETK (Embedded Tool Kit)

最初の組み込み向けCE開発環境、ベータ版として提供

  - Windows CE 2.12 Platform Builder

最初の製品版組み込み向け CE開発環境、独自[IDEでOSビルドが可能](../Page/統合開発環境.md "wikilink") (例)Pocket Post Pet

  - Windows CE 3.0 Platform Builder

IDEで使用するコンポーネントを選択できるようになった(例)Windows Based Terminal、WebPad

  - Windows CE.NET 4.0 Platform Builder

大幅に機能向上。NDIS5.1ネットワーク、MUI機能、VoIP機能など(例)Set Top Box

  - Windows CE.NET 4.1 Platform Builder
  - Windows CE.NET 4.2 Platform Builder

（例）Portable Media Center

  - Windows CE 5.0 Platform Builder

（例）Network Media Device\[9\]、[Nav Readyなどの派生製品がある](https://ja.wikipedia.org/wiki/Windows_Embedded "wikilink")

  - Windows Embedded CE 6.0

これまでの独自IDEからVisual Studio 2005のアドオンへと変更された

  - Windows Embedded CE 6.0 R2
  - Windows Embedded CE 6.0 R3

（例）ネットワークプロジェクタ、PND、カラオケ端末

  - Windows Embedded Compact 7

Visual Studio 2008のアドオンとして提供 (例)タブレット

  - Windows Embedded Compact 2013

Visual Studio 2012/2013/2015のアドオンとして提供

近年ではこれらのプラットフォーム開発ツールは[Visual Studio Professional with MSDNのダウンロード特典を利用して入手する方法が一般的である](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio#Professional "wikilink")。 2015年12月現在、[MSDN Subscriber Download](https://msdn.microsoft.com/ja-jp/subscriptions/downloads/hh442898.aspx)サイトを利用して CE.NET 4.1 から Compact 2013までのすべてのリリースを入手可能である。

### Export SDK機能

上記ツールキットを使用すると、OEMのニーズに応じたOS機能のみを搭載したカスタムWindows CE OSを作成することができるが、これらカスタム機器（通常よりも使用可能API少ない）で正常に動作するネイティブコードアプリケーション開発をサポートするために、ツールキットにはカスタム機器で使用可能なヘッダーファイルとライブラリのみをまとめて出力する、カスタムSDK作成機能が備わっている。この機能を用いて作成されたカスタムSDK は eMbedded Visual C++ やVisual Studio 2005/2008、Visual Studio 2012/2013/2015 + Application Builder環境で使用することができる。

### Shared Source

最近のPlatform Builder には再ビルド可能なCEカーネルほかいくつかの中心モジュールのソースコードが付属しており、ツールキットインストール時に簡単なEULAに同意することでOSのビルドツリー内にインストールされる。これを利用してカーネルの処理内容を理解したりデバッグ時にカーネルデバッガから参照したりすることができる。

### ライセンス料

Windows CE Platform Builderを利用してカスタムWindows CE OSを開発しこれを機器に搭載して製品出荷する場合、組み込みOSとしての使用料をマイクロソフトに支払う必要がある。その際には代理店経由で契約を締結し、COAと呼ばれるシールを製品に貼付して出荷する。Windows CEの組み込みOSとしてのライセンス料は使用OSコンポーネントによりいくつかのカテゴリに分けられるが、およそ1台あたりUS $3 から US$16の範囲とされている\[10\]。

## PDAでの利用

[PDAと呼ばれる製品群にはWindows](../Page/携帯情報端末.md "wikilink") CEをOSとするものがあり、これらPDA用に必要な[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")や[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")などの機能をマイクロソフトがまとめた製品が「Handheld PC」や「Pocket PC」である。「Handheld PC」や「Pocket PC」はOSを示すものではない。例えば、[NECの](../Page/日本電気.md "wikilink")「[モバイルギア](../Page/モバイルギア.md "wikilink")」の「MC-R530」という製品の場合は、Windows CE Ver.2.11を搭載した、Windows CE Handheld PC Edition Ver.3.01仕様の製品というようになる。

初期の頃、Windows CEの利用形態の一つとして、携帯用端末での使用が検討され、その結果x86ベースの[ノートパソコン](../Page/ノートパソコン.md "wikilink")よりも小型化された[キーボード付きの形状のものと](../Page/キーボード_\(コンピュータ\).md "wikilink")、[タッチパネル](../Page/タッチパネル.md "wikilink")へのペン（[スタイラス](../Page/スタイラス.md "wikilink")）による入力操作を基本とするキーボードを持たない小型のものが登場した。前者を「[Handheld PC](https://ja.wikipedia.org/wiki/Handheld_PC "wikilink")」（ハンドヘルド・ピーシー＝H/PC）、後者を「Pocket PC」（ポケット・ピーシー）と呼ぶ 。

どちらの場合も、[Windows 95以降でウィンドウを](../Page/Microsoft_Windows_95.md "wikilink")「最大化表示」で使用した状態に似た[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")となっており、Windowsユーザであれば、あまり違和感なく操作することができるよう配慮されている。また、携帯用という点を重視し、小型軽量で[電池](../Page/電池.md "wikilink")（バッテリ）による長時間駆動が可能である。キーボード付きのものでもペン操作が出来るものが多い。多くは[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")を持たず、[メモリカード](https://ja.wikipedia.org/wiki/メモリカード "wikilink")スロットを実装する。

キーボード型やペン型PDAであっても、マイクロソフトが提供する上記のプラットフォームを使わず、Windows CEカーネル上に独自のユーザモード層を構築した製品もある。[カシオのl](../Page/カシオ計算機.md "wikilink")'agenda（ラジェンダ）、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")のポケットポストペットやシグマリオンIII、[日立のNPD](../Page/日立製作所.md "wikilink")-10JWL/20JWL、[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")（[KDDI](../Page/KDDI.md "wikilink")・[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")）のトリコメール、サイバーバンクジャパンのPC-EPhoneIIなどがこれに当たる。その理由として、GUIを独自実装することで[ロイヤリティ](https://ja.wikipedia.org/wiki/ロイヤリティ "wikilink")を下げられることが挙げられる。また、キーボード型の製品ではH/PCの開発が既に終息していること、ペン型の製品ではARM以外のCPUのサポートを中止したことも挙げられる。これらの機種の一部では、足りないモジュールを独自に補完してPocket PC用などのアプリケーションを動作させる試みが、ユーザーの間で行われている。

### キーボード型製品名称の推移

  - Handheld PC 1.0
    [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[6月25日](../Page/6月25日.md "wikilink")発表。Windows CE 1.0ベース。
  - Handheld PC 2.0
    [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[3月11日](../Page/3月11日.md "wikilink")発表。Windows CE 2.0ベース。
  - Handheld PC 3.0 (Handheld PC Professional Edition)
    [1999年](../Page/1999年.md "wikilink")[2月22日](../Page/2月22日.md "wikilink")発表。Windows CE 2.11ベース。
  - Handheld PC 2000
    [2000年](../Page/2000年.md "wikilink")[10月10日](../Page/10月10日.md "wikilink")発表。Windows CE 3.0ベース。

### ペンオペレーション製品名称の遷移

  - Palm PC
    [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に発表した際の名称。
  - Palm-size PC 1.1
    [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[12月3日](../Page/12月3日.md "wikilink")発表。[Palm OSと酷似するということで改称](https://ja.wikipedia.org/wiki/Palm_OS "wikilink")。白黒インタフェース。（読み：パームサイズPC）（略称：PsPC）
  - Palm-size PC 1.2
    [1999年](../Page/1999年.md "wikilink")[2月22日](../Page/2月22日.md "wikilink")発表。カラー表示対応。

[thumb](https://ja.wikipedia.org/wiki/ファイル:NTT_G-FORT.jpg "wikilink")

  - Pocket PC (2000)
    [2000年](../Page/2000年.md "wikilink")[7月13日](../Page/7月13日.md "wikilink")発表。Windows CE 3.0ベースになったことを機に改称。ウェブブラウザ (Pocket Internet Explorer)、ファイルエクスプローラ搭載。左下にあった「スタート」ボタンが廃止され、左上のプルダウンボタンからタスクを開く形態となった。プラットフォーム準拠のアプリには終了ボタンが付かなくなった。略称：PPC。
  - Pocket PC 2002
    [2001年](../Page/2001年.md "wikilink")[10月5日](../Page/10月5日.md "wikilink")発表。Windows XPに準じた インタフェースを採用し、若干高速化した。これ以降は[ARM系CPUのみをサポートするようになった](../Page/ARMアーキテクチャ.md "wikilink")。アプリに終了ボタンが付くようになったが、実際には終了せず、Windowsの最小化ボタンに近い。
  - Pocket PC 2003
    [2003年](../Page/2003年.md "wikilink")[6月30日](../Page/6月30日.md "wikilink")発表。Windows Mobile 2003 software for Pocket PCが正式名称。Windows CE.NET 4.2ベース。
  - Pocket PC 2003 Second Edition
    [2004年](../Page/2004年.md "wikilink")[7月6日](../Page/7月6日.md "wikilink")発表。Windows Mobile 2003 Second Edition software for Pocket PCが正式名称。[VGA画面をサポート](../Page/Video_Graphics_Array.md "wikilink")。
  - Windows Mobile 5.0
    [2005年](../Page/2005年.md "wikilink")[8月23日](../Page/8月23日.md "wikilink")発表。インタフェースを若干変更。Officeアプリケーションの機能向上。Windows Media Player 10 Mobile搭載など。[.NET Frameworkのサブセットである](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink").NET Compact Frameworkの実行環境が搭載されている。
  - Windows Mobile 6
    [2007年](../Page/2007年.md "wikilink")[2月12日](../Page/2月12日.md "wikilink")発表。インタフェースを刷新し、Vista風デザインとなる。Officeスイートを改良。HTMLメールをサポートしWindows Live Mailに対応。このバージョンからWindows Mobile StandardとWindows Mobile Professional、そして機能面ではWindows Mobile Professionalと同じだが、通信機能がオプション扱いの主にPDA向けのWindows Mobile Classicの三つのエディションに分けられる。バージョン番号はCE 5.2で、CE 6.0カーネルの搭載は見送られた。

Pocket PC2002以降はARM系CPUのみサポートされている。

## PDAの発展と終息

[thumb](https://ja.wikipedia.org/wiki/ファイル:Pocket_LOOX_600.jpg "wikilink") H/PCについては、かつては[NECの](../Page/日本電気.md "wikilink")「[モバイルギア](../Page/モバイルギア.md "wikilink")」、[シャープ](../Page/シャープ.md "wikilink")の「テリオス」、[日本ビクター](../Page/日本ビクター.md "wikilink")の「インターリンク」、[日立製作所](../Page/日立製作所.md "wikilink")の「ペルソナ」、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")の「Jornada」、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")が販売する「[シグマリオン](https://ja.wikipedia.org/wiki/シグマリオン "wikilink")」などの機種があったが、いずれも生産を終了している。マイクロソフトもH/PC向けの製品をリリースしておらず、H/PC市場は事実上終息している。

Pocket PCについては、国内メーカでは[カシオ計算機](../Page/カシオ計算機.md "wikilink")の「[カシオペア](../Page/カシオペア_\(コンピュータ\).md "wikilink")」や[東芝](../Page/東芝.md "wikilink")の「[GENIO e](../Page/GENIO_e.md "wikilink")」、NECの「ポケットギア」、[富士通](../Page/富士通.md "wikilink")の「Pocket LOOX」、NTTドコモが販売する「muséa」等がある。この他に、ヒューレット・パッカード（旧[コンパック](../Page/コンパック.md "wikilink")）の「[iPAQ](https://ja.wikipedia.org/wiki/iPAQ "wikilink")」や[デル](../Page/デル.md "wikilink")の「Axim」など海外メーカー製品もあり、かつては選択の幅も広かったが、各メーカとも[法人](../Page/法人.md "wikilink")用途向けに注力するようになったことや、[通信販売](../Page/通信販売.md "wikilink")でのみ販売する手法に切り替えたこともあり、店頭でこのタイプの端末を見ることも少なくなっている。

[携帯電話](../Page/携帯電話.md "wikilink")の高機能化がPDA全体の販売数が減少した一因、という意見もある。Windows CEは[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")向けのWindows Mobile for Smartphone（日本未発売）やWindows Mobile for Pocket PC Phone Editionというバージョンを出し、携帯電話へのシフトを強めている。

[150px](https://ja.wikipedia.org/wiki/ファイル:HT-01A.jpg "wikilink")(WindowsMobile6.1)\]\]

## PDAの現状

### 日本国内でのスマートフォンへの採用

  - [WILLCOM](../Page/ウィルコム.md "wikilink") [W-ZERO3](../Page/W-ZERO3.md "wikilink")シリーズ - 2005年12月に初代機WS003SH（[W-ZERO3](../Page/W-ZERO3.md "wikilink")、[シャープ](../Page/シャープ.md "wikilink")製）が発売。OSにはWindows Mobile 5.0 for Pocket PCが使われている。\<\!--項目表題とは関係ないので

VGA液晶・キーボード・[無線LAN](../Page/無線LAN.md "wikilink")などが搭載された[PHS](../Page/PHS.md "wikilink")端末で、発売前の店頭予約受付に200人以上が並び、オフィシャルストアでは抽選販売も行われた。モバイルソリューションとして、NTT Docomo hTcZ、Softbank X01HT、WILLCOM W-ZERO3シリーズを推奨している。--\>

  - NTTドコモ [hTc Z](https://ja.wikipedia.org/wiki/hTc_Z "wikilink") [HT1100](https://ja.wikipedia.org/wiki/HT1100 "wikilink")　 [F1100](https://ja.wikipedia.org/wiki/F1100 "wikilink")
  - [SoftBank X01HT](../Page/SoftBank_X01HT.md "wikilink") - スマートフォン、HSDPAの3G高速通信を初採用。
  - [イー・モバイル](../Page/イー・モバイル.md "wikilink") [EMONSTER](https://ja.wikipedia.org/wiki/EMONSTER "wikilink") (S11HT)
  - [シャープ](../Page/シャープ.md "wikilink") [Brain](https://ja.wikipedia.org/wiki/Brain_\(電子辞書\) "wikilink") - [電子辞書](../Page/電子辞書.md "wikilink")

## 関連項目

  - [Windows Mobile](../Page/Windows_Mobile.md "wikilink")
  - [Pocket PC](../Page/Pocket_PC.md "wikilink") - 主流は[Windows Mobile搭載の](../Page/Windows_Mobile.md "wikilink")[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")にタッチパネルを組み合わせたもの。
  - [Windows Automotive](https://ja.wikipedia.org/wiki/Windows_Automotive "wikilink") - カーナビゲーションシステムにおける採用例（[Pioneer](https://ja.wikipedia.org/wiki/パイオニア "wikilink")「[サイバーナビ](https://ja.wikipedia.org/wiki/サイバーナビ "wikilink")」「[楽ナビ](https://ja.wikipedia.org/wiki/楽ナビ "wikilink")」、[Panasonic](https://ja.wikipedia.org/wiki/パナソニック "wikilink")「[\*Strada](../Page/Strada.md "wikilink")」、[Clarion](../Page/クラリオン.md "wikilink")「Smoonavi」など）がある。
  - [Microsoft Zune](../Page/Zune.md "wikilink") - OSとしてWindows CEベースのPortable Media Centerを採用している。
  - [ドリームキャスト](../Page/ドリームキャスト.md "wikilink") - Windows CE搭載ゲームコンソール。
  - [タブレットPC](../Page/タブレットPC.md "wikilink")
  - [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")、[iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink") - Pocket PC及びZuneの競合商品。[Mac OS Xから派生したOSを搭載](https://ja.wikipedia.org/wiki/macOS "wikilink")。
  - [BlackBerry](../Page/BlackBerry.md "wikilink") - カナダ Research in Motion社のスマートフォン。マイクロソフトによる買収の噂もあった\[11\]。
  - [Android](../Page/Android.md "wikilink")
  - [Palm](../Page/Palm.md "wikilink") - 上記Pocket PCの競合商品。Treoの一部機種ではWindows Mobileを搭載していた。現在では終息しつつあり、後継の[WebOSを待つ段階である](https://ja.wikipedia.org/wiki/Palm_WebOS "wikilink")。
  - [Zaurus](https://ja.wikipedia.org/wiki/Zaurus "wikilink") - Pocket PCのかつての競合製品。現在は終息。
  - [ITRON](../Page/ITRON.md "wikilink")
  - [REX OS](https://ja.wikipedia.org/wiki/REX_OS "wikilink")
  - [Brew MP](https://ja.wikipedia.org/wiki/Brew_MP "wikilink")

## 脚注

<references />

## 外部リンク

  -
  - [WindowsCE FAN](http://www.wince.ne.jp/)

[Category:Windows_CE](https://ja.wikipedia.org/wiki/Category:Windows_CE "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink") [Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")

1.  採用例として[ユピテルが製造](../Page/ユピテル_\(企業\).md "wikilink")・販売する「YERA」「MOGGY」「drive navi」「LeiNavi/LeiNavi+」などがある。なお「オリジナル・コンテンツ・ナビゲーション」とはユピテルにおけるPND製品群の通称である
2.  [The Meaning of "CE" in Windows CE](http://support.microsoft.com/kb/166915/en), マイクロソフト, 2002年9月3日
3.  [マイクロソフト、Windows Embedded Compact 7のCTPを公開](http://pc.watch.impress.co.jp/docs/news/20100604_372263.html), PC Watch, 2010年6月4日
4.  [Microsoft、Windows CE後継OS「Windows Compact 7」の提供開始](http://pc.watch.impress.co.jp/docs/news/20110304_430874.html), PC Watch, 2011年3月4日
5.  [Windows CE FAN, MIPS用? SH用? ひとつの実行ファイルで大丈夫 期待の新技術 CEF とは?](http://www.wince.ne.jp/Review/Katsuo/Dev99/cedev25.htm), Windows CE FAN, 1999年6月10日
6.  .NET Compact Frameworkで作成されたWinFormベースのアプリケーションは、再コンパイルせずにそのままデスクトップ上の.NET Frameworkで動く場合が多い
7.
8.  [History of Windows Embedded Compact 7](http://www.microsoft.com/windowsembedded/en-us/evaluate/history-of-windows-embedded-compact-7.aspx), Microsoft
9.
10. [Windows Embedded Compact 7 Product Information and Pricing](http://www.microsoft.com/windowsembedded/en-us/develop/windows-embedded-compact-7-os-components.aspx), Microsoft
11.