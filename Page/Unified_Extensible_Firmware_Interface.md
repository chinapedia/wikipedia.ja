> この記事は[Unified Extensible Firmware Interface](https://ja.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface)から翻訳されています。


[frame](https://ja.wikipedia.org/wiki/ファイル:Efi-simple_ja.svg "wikilink")

**Unified Extensible Firmware Interface**（ユニファイド・エクステンシブル・ファームウェア・インタフェース、**UEFI**）は[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")（OS）とプラットフォーム[ファームウェア](../Page/ファームウェア.md "wikilink")との間のソフトウェア[インタフェースを定義する](../Page/インタフェース_\(情報技術\).md "wikilink")[仕様](../Page/仕様.md "wikilink")である。

UEFIを採用した[System BIOSは](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")「UEFI BIOS」と呼ばれ、単に「UEFI」と略されることが多いが、ユーザーがアクセスし設定などを行うGUIはUEFIであっても「BIOS」と呼ばれる事が多い。UEFI BIOSは[IBM PC互換機に採用された古いSystem](../Page/IBM_PC.md "wikilink") BIOSのよりセキュアな置き換えを意図している\[1\]。遠隔診断やOSがロードされていない状態での修復なども可能とする\[2\]。「BIOS」とは異なり、「UEFI」の読みは特に定められていない。

UEFIの元となる **EFI** (**Extensible Firmware Interface**) 仕様は元々[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")と[ヒューレットパッカード](https://ja.wikipedia.org/wiki/ヒューレットパッカード "wikilink")によって開発された。2005年、EFI 1.10に基づいてUEFIへと発展した。UEFI仕様は業界団体[Unified EFI Forumの下で開発されている](https://ja.wikipedia.org/wiki/Unified_EFI_Forum "wikilink")。

UEFI自体は単なる「インタフェースの仕様」であるため、特定のプロセッサに依存しない。これまでのBIOSとは異なり、近代的なソフトウェア開発手法を用いることが推奨されており、[C言語](../Page/C言語.md "wikilink")で実装したものなどが代表的である\[3\]。

## 歴史

そもそもEFIが開発された動機は、[1990年代](../Page/1990年代.md "wikilink")中盤のインテルとヒューレットパッカードによる初代[Itanium](../Page/Itanium.md "wikilink")機の開発初期にまでさかのぼる。[IBM PC由来のSystem](../Page/IBM_PC.md "wikilink") BIOSなどの制限（16ビットプロセッサモード、1MBの[アドレス空間](../Page/アドレス空間.md "wikilink")、[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")ハードウェアへの依存など）によって、従来の各種\[4\]スキームはItaniumの（当初の\[5\]）ターゲットである巨大なサーバプラットフォームには採用できなかった\[6\]。その課題に対する最初の成果が、1998年に**Intel Boot Initiative**と呼ばれ\[7\]、後にEFIと名前を変えた\[8\]\[9\]。

EFI仕様1.02は[2000年](../Page/2000年.md "wikilink")[12月12日](../Page/12月12日.md "wikilink")にインテルによってリリースされた（最初に発行されたものはバージョン1.01であったが、法的な不備や商標などのミスによりすぐに取り下げられている）。

EFI仕様1.10は[2002年](../Page/2002年.md "wikilink")[12月1日](../Page/12月1日.md "wikilink")にインテルによってリリースされた。これには、バージョン1.02からのいくつかの細かい機能強化と、EFIドライバのモデルが記載されていた。

[2005年](../Page/2005年.md "wikilink")、インテルは、同仕様の普及を行うために設立された[Unified EFI ForumへEFIの権利を移管した](https://ja.wikipedia.org/wiki/Unified_EFI_Forum "wikilink")。以後は同フォーラムがEFI仕様の開発と普及につとめている。これを反映して、EFIはUnified EFI（UEFI）と名前を変え、多くのドキュメントが両方の用語を同じ意味で使用するようになった。元々のEFI仕様は依然としてインテルに所有権があり、EFIベースの製品へのライセンスもインテルが提供しているが、UEFI仕様は同フォーラムが所有している\[10\]\[11\]。

[2007年](../Page/2007年.md "wikilink")[1月7日](../Page/1月7日.md "wikilink")、UEFI仕様バージョン2.1がリリースされた。[暗号](../Page/暗号.md "wikilink")化の改善、ネットワーク認証、ユーザインタフェースのアーキテクチャ（UEFI中にある対人インタフェース）が追加されている。最新のUEFI規格は2.6（Errata A）である。

インテルによる開発から10年以上たった[2011年](../Page/2011年.md "wikilink")、2TB以上の容量を持つ[ハードディスクに対応するために](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、[P67、H67、H61、Z68](https://ja.wikipedia.org/wiki/インテル_チップセット#Intel_6_Series "wikilink")[チップセット](../Page/チップセット.md "wikilink")を使用したマザーボードでUEFIの採用が本格化した\[12\]。

## 詳細

[thumb](https://ja.wikipedia.org/wiki/ファイル:Efi_flowchart_extended.svg "wikilink")

EFI仕様によって定義されたインタフェースは、プラットフォーム情報などのデータテーブルを持っている。この情報やEFIの機能はブートローダーやOSが利用できる。UEFIファームウェアには以下のような技術的利点がある\[13\]。

  - 2[TiBを超える大きなディスクからブートできる](https://ja.wikipedia.org/wiki/テビバイト "wikilink")\[14\]
  - より高速なブートが可能である
  - CPUに依存しないアーキテクチャ
  - CPUに依存しないドライバ
  - ネットワークも使用可能な柔軟なプレOS環境が利用できる
  - モジュール化設計が採用されている

従来のSystem BIOSに対する強化点としては、[ACPIや](../Page/Advanced_Configuration_and_Power_Interface.md "wikilink")[SMBIOS](../Page/SMBIOS.md "wikilink")がすでにEFIの中にあるため、16ビットで動作するインタフェースに依存せずに使用できることが挙げられる。

### ディスクのサポート

[マスターブートレコード](../Page/マスターブートレコード.md "wikilink")（MBR）などの標準的なPCのディスクパーティションの処理に加えて、EFIでは[GUIDパーティションテーブル](../Page/GUIDパーティションテーブル.md "wikilink")（GPT）をサポートしている。これによりPCでの[ディスクパーティションの容量の限界と領域の数の制限は拡張され](../Page/パーティション.md "wikilink")、同じ時期に開発された2[TB以上の](../Page/テラバイト.md "wikilink")[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")接続の内蔵ハードディスクからの起動がサポートされた\[15\]。GPTでのディスクとパーティションの最大サイズは9.4[ZB](https://ja.wikipedia.org/wiki/ゼタバイト "wikilink")（2<sup>73</sup>バイト）である\[16\]\[17\]。EFI規格ではファイルシステムには言及していないが、UEFI規格では[FAT12、FAT16、FAT32のサポートを必須としている](../Page/File_Allocation_Table.md "wikilink")。

### プロセッサのサポート

バージョン2.3では、Itanium、x86、x86_64、[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")をサポートしている（バインディングが存在する）。

System BIOSは16ビットの[Intel 8088を採用した](../Page/Intel_8088.md "wikilink")[IBM 5150の設計に基づいているため](../Page/IBM_PC.md "wikilink")、16ビット・プロセッサモードと1MBのアドレス空間という制限があった\[18\]\[19\]。一方、UEFIのプロセッサモードは32ビット（[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")-32、ARM）または64ビット（[x86-64](https://ja.wikipedia.org/wiki/x64 "wikilink")、Itanium）である\[20\]\[21\]。64ビットのUEFIではロングモードも可能であり、ブート前の環境で64ビットアドレッシングの全メモリに直接アクセス可能である\[22\]。

UEFIでは、ファームウェアとOSのアドレス空間が一致していなければならない。たとえば、64ビットのUEFIからは64ビットのオペレーティングシステムしかブートできない。

### ブートサービス

EFIはブートサービスを定義していて、これにはさまざまなデバイス上でテキストおよびグラフィカルなコンソールが利用できる機能や、バスや[ブロックデバイス](https://ja.wikipedia.org/wiki/ブロックデバイス "wikilink")、[ファイルシステム](../Page/ファイルシステム.md "wikilink")の機能が含まれる。ブートサービスは「ExitBootServices」を呼び出すまでのファームウェアがプラットフォームを制御している状態でのみ利用可能である。また、OS動作中も利用できるランタイムサービスとしては、日付や時間、[NVRAM](https://ja.wikipedia.org/wiki/NVRAM "wikilink")の管理サービスなどがある。

### プロトコル

EFIでは2つのバイナリモジュール間の通信に使うソフトウェアインタフェース群をプロトコルとして定義している。全てのEFIドライバは、このプロトコルに則って他のモジュールにサービスを提供しなければならない。

### デバイスドライバ

EFIの仕様では、標準的なアーキテクチャ依存の[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")に加えて、プロセッサに依存しないデバイスドライバ実行環境を提供しており、**EFI Byte Code**または**EBC**と呼ばれている。システムのファームウェアは、その環境にロードされたもしくはその環境内にあるEBCイメージ用の[インタプリタ](../Page/インタプリタ.md "wikilink")を実行できることを、UEFI仕様によって要求されている。その点、EBCは[Open Firmwareに似ている](../Page/Open_Firmware.md "wikilink")。これはハードウェアに依存しないファームウェアで、[PowerPC](../Page/PowerPC.md "wikilink")ベースの[アップルの](../Page/アップル_\(企業\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")や[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[SPARC](../Page/SPARC.md "wikilink")コンピュータなどの間で採用された。

いくつかのアーキテクチャに特化した（非EBCな）EFIデバイスドライバはOSから利用可能なインタフェースを持つことができる。これにより、OSに特化したドライバをロードしなくても、基本的なグラフィックスやネットワーク機能についてはOSがEFIに頼ることができる。

### ブートマネージャー

**EFIブートマネージャー**はまたOSを選択してロードするのにも使うことができる。これにより専用のブートローダ機構は必要がなくなる（OSのブートローダはEFIアプリケーションになる）。この場合、[ブートセクタ](../Page/ブートセクタ.md "wikilink")を使用せずに済むが、最初にロードすべき標準で定められた名前のファイルを、特殊なパーティションテーブルから参照できるようにしておく必要がある（ファイル名の例：`\EFI\BOOT\boot[architecture name].efi`）。

OSのブートローダーはUEFIアプリケーションの一種となるので、ファームウェアからアクセス可能な[ファイルシステム](../Page/ファイルシステム.md "wikilink")上にファイルとして格納しておく。NVRAMに格納されたブート変数で、そのローダーのパスを示す。ブートローダーはファームウェアから自動検出することも可能で、たとえばリムーバブル・デバイスからのブートも可能となっている。

また、特定のハードウェアやオペレーティングシステムに依存しないように、UEFIアプリケーションのバイナリコードの記述には、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した、ハードウェアやOSに依存しないバイナリフォーマットである[Portable Executable（PE）フォーマットを用いることが定められている](../Page/Portable_Executable.md "wikilink")。

### セキュアブート

UEFIセキュアブートは、起動対象のオペレーティングシステムの電子署名を検証して正当なソフトウェアであることが確認できた場合にのみブート処理を継続する\[23\] 。

WindowsマークのあるマシンではセキュアブートにMicrosoftの電子署名が使われており、Windows 8以降はセキュアブート電子署名が付与されている。一方で、Windows 7以前のオペレーティングシステムやLinuxディストリビューションは電子署名が付与されていないため、セキュアブートが有効なUEFIブートローダーでは起動できない。

マイクロソフトがリリースしたWindows 8 OEM製品のハードウェア認定に関する文書\[24\]によれば、x86およびx86-64を採用した全デバイスはセキュアなUEFIを有効にしなければならないが、カスタム・セキュアブート・モードでユーザーがシグネチャを追加できる手段を提供すると記述されている。一方、Windowsの動作するARMデバイスでは、セキュアブートを無効にできる実装を禁止している\[25\]ため、カスタム・セキュアブート・モードへの移行もセキュアブートの無効化も不可能である。Windows 10のハードウェア認定要件ではセキュアブートの無効化手段の提供はオプションとなった\[26\]。

マイクロソフトは、実費でマイクロソフトの鍵によって署名を行うサービスを提供している。[Fedora](../Page/Fedora.md "wikilink")、[openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")、[Ubuntu](../Page/Ubuntu.md "wikilink")、[RHEL](https://ja.wikipedia.org/wiki/RHEL "wikilink")（RHEL 7から）、[CentOS](../Page/CentOS.md "wikilink")（CentOS 7から）などの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")は、この署名サービスによって署名された軽量ブートローダを用いることでセキュアブート（の鍵配布と鍵インストールに纏わる問題）に対応している\[27\]\[28\]。セキュアブートへの対応を計画している[FreeBSD](../Page/FreeBSD.md "wikilink")もマイクロソフトの署名サービスを利用する計画である\[29\]。

### EFIシェル

EFIコミュニティは[オープンソース](../Page/オープンソース.md "wikilink")な[シェル](../Page/シェル.md "wikilink")環境を作った\[30\]。これはちゃんとしたOSを直接起動するのではなく、なんらかの実装上でユーザがEFIシェルと呼ぶものを起動することができる。このシェルはEFIアプリケーションであり、プラットフォームのROM内に直接焼きこまれているか、ROM内のデバイスドライバが制御できるデバイス内に存在する必要がある。

EFIシェルは、他のEFIアプリケーション、たとえばシステムの起動やOSのインストール、システムの診断や設定、システムのフラッシュROMのアップデートなどに使われる。このことにより、完全なOSを起動することなしに[CDや](../Page/コンパクトディスク.md "wikilink")[DVD](../Page/DVD.md "wikilink")を再生したり、必要な機能を持つEFIアプリケーションを実行することができる。また、シェルのコマンドを使って、ファームウェアがサポートしているファイルシステム間同士で直接ファイルのコピーや移動を行うこともできる。デバイスドライバは動的にロードとアンロードができ、完全な[TCP/IP](../Page/インターネット・プロトコル・スイート.md "wikilink")[スタックもまたシェル内から利用することができる](../Page/プロトコルスタック.md "wikilink")。

EFIシェルにはスクリプトファイルの機能があり、拡張子には .nsh を使う。[バッチファイル](../Page/バッチファイル.md "wikilink")に似ており、コマンドにはUnixまたはMS-DOSのコマンドに類似したものがある。

### 拡張機能

EFIの拡張機能は、コンピュータに搭載されている[不揮発性のストレージデバイスからロードされる](../Page/不揮発性メモリ.md "wikilink")。たとえば、マザーボード上の[ROMに格納されている標準EFIファームウェアに機能を追加するために](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、[OEM](../Page/OEM.md "wikilink")がハードディスクにEFIパーティションを作って、そのシステムを販売することができる。

## 実装と採用実績

### Intel Platform Innovation Framework for EFI

Intel Platform Innovation Framework for EFI（元々*Tiano*というコードネームで呼ばれていた）はEFIサポートを含み、完全でレガシーフリーなファームウェア実装である。これは、**Compatibility Support Module**（CSM）と呼ばれるものを通してレガシーなSystem BIOSのサポートが可能である。

特に、このフレームワークには、電源投入後のプラットフォームの初期化に必要なすべての処理が含まれている。これらのファームウェアの内部動作はEFIの仕様には定義されていないが、[Platform Initialization Specification](https://ja.wikipedia.org/wiki/Platform_Initialization_Specification "wikilink")（PI Specification）に記載されている。

インテルはこのフレームワークを完全な形でエンドユーザーに提供しているわけではない。[アメリカンメガトレンド](https://ja.wikipedia.org/wiki/American_Megatrends "wikilink")（AMI）\[31\]や[Insyde Software](https://ja.wikipedia.org/wiki/:en:Insyde_Software "wikilink")\[32\]、[Phoenix Technologies](https://ja.wikipedia.org/wiki/:en:Phoenix_Technologies "wikilink")\[33\]など、独立したBIOSベンダーに対してファームウェアの提供が行われているので、それらを通じて利用が可能である。

フレームワークの一部は、**EFI Developer Kit**（EDK）という名前で[TianoCore project](http://www.tianocore.org/)で[オープンソース](../Page/オープンソース.md "wikilink")としてリリースされている。この実装は、EFIといくつかのハードウェア初期化コードを含んでいるが、それ自身で完全な機能を持つファームウェアを構成できるわけではない。このコードには[BSDライセンス](../Page/BSDライセンス.md "wikilink")と[Eclipse Public Licenseを含むいくつかのライセンスが適用されている](https://ja.wikipedia.org/wiki/Eclipse_Public_License "wikilink")。TianoCoreは[coreboot](https://ja.wikipedia.org/wiki/coreboot "wikilink")のペイロードとしても利用できる。

### EFIおよびこのフレームワークを用いたプラットフォーム

インテルの最初のItaniumワークステーションとサーバは2000年にリリースされ、EFI 1.02を実装している。

ヒューレット・パッカードの最初の[Itanium 2システムは](https://ja.wikipedia.org/wiki/Itanium_2 "wikilink")2002年にリリースされ、EFI 1.10を実装している。これらは[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")が起動できた。2003年6月には[OpenVMS](../Page/OpenVMS.md "wikilink")もサポートされている。

[DIG64](https://ja.wikipedia.org/wiki/DIG64 "wikilink")仕様に従ったEFI互換ファームウェアを搭載したすべてのItaniumとItanium2システム。

[2003年](../Page/2003年.md "wikilink")[11月](../Page/11月.md "wikilink")、[ゲートウェイは](../Page/ゲートウェイ_\(PCメーカー\).md "wikilink")、Gateway 610 Media Centerに、x86のWindowsベースのコンピュータシステムとしては初めてこのフレームワークをベースとしたファームウェアである、Insyde SoftwareのInsydeH2Oというファームウェアを導入した。このファームウェアではまだWindowsを起動するために、compatibility support moduleを使ってレガシーSystem BIOSを実装していた。

[2006年](../Page/2006年.md "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")、アップルはインテルアーキテクチャ ([IA-32](../Page/IA-32.md "wikilink")) をベースとした最初のMacintosh ([Intel Mac](../Page/Intel_Mac.md "wikilink")) を出荷した。このシステムは以前のPowerPCベースのシステムに採用していたOpen Firmwareに代わって、EFIを採用していた。2006年[4月5日](../Page/4月5日.md "wikilink")、アップルは [Boot Camp](../Page/Boot_Camp.md "wikilink") と呼ばれるソフトウェアをリリースした。これには [Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") または Vista をユーザが既存のパーティションを壊さずに簡単にインストールできるツールと、Windows XP用のドライバディスクを提供している。ここでもまたファームウェアアップデートを通じて、EFI実装に加えてレガシーSystem BIOSのサポートが追加された。続くMacintoshの機種ではより新しいファームウェアが入った状態で出荷されている。2014年現在のMacintoshは、Winodows 7以降のみに対応し、Windows XPのようなレガシーSystem BIOSを使ってロードされるOSを起動できない。

非常にメジャーなインテルの[マザーボード](../Page/マザーボード.md "wikilink")は、このフレームワークをベースとしたファームウェアを搭載して出荷されている。2005年では、100万台以上インテルのボードがこのフレームワークを搭載して出荷されている\[34\]。新型のモバイルやデスクトップ、サーバ製品ではこのフレームワークを用いて2006年に出荷が開始されている。すぐにすべてのIntel 945チップセットを採用しているボードはこのフレームワークを搭載することになるだろう。しかし、製品用のファームウェアはEFIをサポートせず、レガシーSystem BIOSに限定している。

2005年以来、EFIは[XScale](../Page/XScale.md "wikilink")をベースとする[組み込みシステム](../Page/組み込みシステム.md "wikilink")のようなPC以外のアーキテクチャにも実装されている\[35\]。

NT32を含むEDKによってWindowsアプリケーション内でEFIファームウェアおよびEFIアプリケーションを動作させることができるようになった。ただし、EDK NT32 では直接的なハードウェアアクセスは許されていない。つまり、EDK NT32 のターゲットとしてどんなEFIアプリケーションも実行できるわけではない。2007年、ヒューレット・パッカードはEFI互換ファームウェアを用いた高機能プリンタ8000シリーズをリリースした。

2008年、x86-64 システムでのUEFI採用が増えた。その多くは Compatibility Support Module (CSM) を使ったBIOSベースのOSのブートしか許していないが（従ってユーザーにはUEFIベースであることが明示されていない）、UEFIベースのOSのブートを許すシステムも出てきている。例えば、IBM x3450 サーバ、ClickBIOSを搭載した[MSI製マザーボード](../Page/Micro-Star_International.md "wikilink")、HP EliteBookやタブレットPC、HP CompaqノートPCなどがある。

2009年、IBMはUEFIを搭載した [System x](../Page/System_x.md "wikilink") マシンや [BladeCenter](https://ja.wikipedia.org/wiki/BladeCenter "wikilink") マシンを出荷した。デルもUEFIを搭載したサーバを出荷している。他にも UEFI のホワイトペーパーに採用例が挙げられている\[36\]。[Sandy Bridge](https://ja.wikipedia.org/wiki/Sandy_Bridgeマイクロアーキテクチャ "wikilink") [PC](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink") プラットフォームの多くはUEFIを採用している。

### オペレーティングシステム（OS）

(U)EFI仕様において、(U)EFIからブートできるOSを「(U)EFI-aware OS」と呼ぶ。ここで「(U)EFIからブートできる」とは、任意のストレージデバイスに格納された(U)EFIのOSローダーを使って直接[ブート](../Page/ブート.md "wikilink")できることを意味する。OSローダーのデフォルトの位置は `\EFI\BOOT\boot[architecture name].efi`であり、「architecture name」には、たとえばIA32、X64、IA64などが入る。一部OSベンダーは独自のOSローダーを持っており、ブート位置を変更している場合もある。

  - [Linuxは](../Page/Linuxカーネル.md "wikilink")2000年初期から[elilo](https://ja.wikipedia.org/wiki/elilo "wikilink")というEFIブートローダを使って、EFIを使って起動することができる。以前では、eliloや[GRUB](../Page/GNU_GRUB.md "wikilink")\[37\]は[IA-64](../Page/IA-64.md "wikilink")プラットフォーム上でLinuxを単に起動できるだけであり、[x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink")とIA32プラットフォームでも同じことが可能である\[38\]。現在では[GRUB2](https://ja.wikipedia.org/wiki/GRUB2 "wikilink")のEFI版もある。
  - [HP-UX](../Page/HP-UX.md "wikilink")は2002年から[IA-64システム上で](../Page/Itanium.md "wikilink")(U)EFIを使ったブート機構を使用していた。
  - HP [OpenVMS](../Page/OpenVMS.md "wikilink") の IA-64 版は2003年12月の最初の評価版リリースから(U)EFIを使っている。製品版は2005年1月からリリースされている\[39\]。
  - [マイクロソフト](../Page/マイクロソフト.md "wikilink")のIA-64用の[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink")、Windows XP 64bit Edition、[Windows Advanced Server, Limited EditionはすべてEFIをサポートしており](../Page/Microsoft_Windows_2000.md "wikilink")、DIG64仕様を通じてプラットフォームの要件となっている。
  - アップルは、[Macにインテルアーキテクチャを初めて採用した](../Page/Intel_Mac.md "wikilink")2006年1月以降、一貫してEFIを採用している。
  - マイクロソフトは[Windows Server 2008のx](../Page/Microsoft_Windows_Server_2008.md "wikilink")64版でUEFIに対応した。[Windows Vistaのx](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")64版では、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[3月19日](../Page/3月19日.md "wikilink")に[Windows Update及びダウンロードセンターで配布が開始されたSP](../Page/Microsoft_Update.md "wikilink")1でEFIに対応した。当初マイクロソフトは市場の関心が64ビットへ向いていることなどを理由に32ビットWindowsへのUEFI実装を行わなかったが\[40\]、Windows 8の32ビット版ではSecure Bootと共にUEFIへと対応している\[41\]\[42\]。マイクロソフトは、Andrew RitzとJamie SchwarzがWindows VistaとWindows Server 2008上でUEFIを用いてOS起動前の処理を説明するビデオをリリースした\[43\]。
  - マイクロソフトは、[自作パソコン](../Page/自作パソコン.md "wikilink")向けに単体販売される[マザーボード](../Page/マザーボード.md "wikilink")を含むコンピュータ本体に "Designed for Windows 8" のロゴを付ける条件として、UEFIでをデフォルトで有効にすることを要求している\[44\]\[45\]。[レッドハット](../Page/レッドハット.md "wikilink")の開発者マシュー・ギャレットはセキュアブートをデフォルトで有効にするという要求に懸念を表明したが、マイクロソフトはそれに対して自身がそれを命令したことはないし、ファームウェア内で後から無効にすることを妨げるつもりもないと応じた\[46\]\[47\]。

### 仮想化

  - では、HP IntegrityサーバでのUEFIブートを提供する。UEFI-awareのゲストOSのための仮想UEFI環境も提供する。

  - インテルでは、Sourceforge上でOpen Virtual Machine Firmwareプロジェクトを主催している\[48\]。

  - Mac OS X向けのは、EFIを使って、Mac OS X Serverの仮想マシンをブートできる。

  - [VirtualBox](../Page/VirtualBox.md "wikilink") は3.1からUEFIを実装しているが\[49\]、レガシーBIOSからUEFIへの移行期に開発されたOSの起動に必要となるCSMが実装されていないため、対応OSはUnix/Linux系または[Windows 8以降の](https://ja.wikipedia.org/wiki/Windows_8 "wikilink")[x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink")版に限られている（Vistaや7のx64版はUEFI対応不可）\[50\]\[51\]。

  - [QEMU](../Page/QEMU.md "wikilink")/[KVMはEFIと共に利用可能である](https://ja.wikipedia.org/wiki/Kernel-based_Virtual_Machine "wikilink")。

  - [VMware](../Page/VMware.md "wikilink") vSphereの一部であるVMware ESXi version 5 hypervisorは仮想マシン内のBIOSの代替として仮想化EFIをサポートしている。

  - VMware Workstation 11以降ではEFIを使用した仮想マシンの起動をサポートしている。

  - VMware Workstation 14以降ではSecureBootを使用した仮想マシンの起動をサポートしている。

  - [Hyper-V](../Page/Hyper-V.md "wikilink")の第二世代仮想マシンはUEFIをサポートする。

### コンシューマ市場

2011年、[ASRock](../Page/ASRock.md "wikilink")、[ASUS](../Page/ASUS.md "wikilink")TeK、[GIGABYTE](../Page/GIGABYTE.md "wikilink")、[MSI](../Page/Micro-Star_International.md "wikilink") 、[BIOSTAR](https://ja.wikipedia.org/wiki/BIOSTAR "wikilink")などは、インテルの[6-series](https://ja.wikipedia.org/wiki/インテル_チップセット#Intel_6_Series "wikilink") [LGA 1155チップセットおよびAMDの](https://ja.wikipedia.org/wiki/LGA1155 "wikilink") 9 seriesチップセットを使ったコンシューマ向けマザーボードで、EFIを採用している\[52\]。

## グラフィックス機能

AMI AptioのUEFI実装では、メニューなどにグラフィックス要素が使われている\[53\]。

EFI仕様では、2つのグラフィックス表示プロトコルが定義されている。1つはUGA (Universal Graphics Adapters) で、もう1つはGOP (Graphics Output Protocol) である。2つはよく似ている。UGAはEFI 1.1かそれ以前でのみ動作する。EFIはユーザインタフェースを定義していない。したがって、見た目や操作方法はSystem BIOSベンダーに一任されている。今 のところ多くのEFI実装では、System BIOSのようなテキストモードのユーザインタフェースを採用している。

## 批判

[coreboot](https://ja.wikipedia.org/wiki/coreboot "wikilink")開発者の1人Ronald G. Minnichと[SF作家](../Page/SF作家.md "wikilink")でデジタル権利活動家の[コリイ・ドクトロウ](https://ja.wikipedia.org/wiki/コリイ・ドクトロウ "wikilink")はEFIについて、ユーザーが自身のコンピュータを真に制御する能力を阻害することで知的所有権を守ろうとする試みだとして批判している\[54\]\[55\]。EFIは、BIOS最大の懸案事項である、ファームウェア用とOS用に別々のドライバが必要だという点を全く解決していない\[56\]。

TianoCoreはUEFIに基づく完全にフリーなファームウェアを作るツールを提供するオープンソースプロジェクトだが\[57\]、チップセット初期化のための特殊なドライバが含まれておらず、チップセットベンダーからの追加の機能提供を必要としている。TianoCoreはcorebootのペイロード・オプションであり、チップセット初期化コードも含んでいる。

UEFIは従来のSystem BIOSよりもネットワークブートの柔軟性が高いため、その点でセキュリティ的に懸念する見方もある\[58\]。

[レッドハット](../Page/レッドハット.md "wikilink")の開発者マシュー・ギャレットは記事「UEFI secure booting」で、UEFIのセキュアブートがLinuxに影響を与えるかもしれないという懸念を表明した（Windows 8 のロゴをつけたマシンでは、セキュアブートが有効化された状態で出荷され、キーコードのないLinuxではブートできない）\[59\]。これに対してマイクロソフトは、顧客がセキュアブートを後から無効にすることは可能だと応じた\[60\]\[61\]。しかし、指定以外のOSをインストールできなくすることでユーザーサポートにかかるコストを削減したいと考えている一部のハードウェアベンダーがセキュアブートを無効にできない実装のファームウェアを搭載した機器を販売し始めるのではないかという懸念が残っている\[62\]。

[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")のジョシュア・ゲイはUEFIでのセキュアブート実装について懸念を表明し、FSFは次のような声明を発表した。

> （下に署名する）我々は、フリーソフトウェアのOSをインストール可能にする形でいわゆる「セキュアブート」をUEFIに実装するよう全コンピュータメーカーに求める。ユーザーの自由を尊重し真のユーザーセキュリティを守るため、メーカーはコンピュータ所有者がブート制限を無効にできるようにするか、フリーソフトウェアのOSを自由にかつ絶対確実にインストールして利用できる手段を提供しなければならない。我々はそのような重大な自由を妨げるコンピュータを購入しないし勧めない。また、我々のコミュニティの人々にそのようなシステムを購入しないよう呼びかけていく。\[63\]\[64\]

## 脚注

## 関連項目

  - [オープンシステム](../Page/オープンシステム_\(コンピュータ\).md "wikilink")
  - [Advanced Configuration and Power Interface](../Page/Advanced_Configuration_and_Power_Interface.md "wikilink") (ACPI)
  - [Basic Input/Output System](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink") (BIOS)
  - [ブート](../Page/ブート.md "wikilink")
  - [Coreboot](https://ja.wikipedia.org/wiki/Coreboot "wikilink")
  - [プログラム仕様](../Page/プログラム仕様.md "wikilink")
  - [Open Firmware](../Page/Open_Firmware.md "wikilink")
  - [SMBIOS](../Page/SMBIOS.md "wikilink")
  - [システムマネジメントモード](../Page/システムマネジメントモード.md "wikilink") (SMM)
  - [Unified EFI Forum](https://ja.wikipedia.org/wiki/Unified_EFI_Forum "wikilink")
  - [Trusted Platform Module](../Page/Trusted_Platform_Module.md "wikilink") (TPM)

## 外部リンク

  - [UEFI FORUM](https://uefi.org/)

  - [Intel's EFI page](https://www.intel.com/content/www/us/en/architecture-and-technology/unified-extensible-firmware-interface/efi-homepage-general-technology.html)

  - [ブートおよび UEFI](https://docs.microsoft.com/ja-jp/windows-hardware/drivers/bringup/boot-and-uefi)

  - [EFI Architecture](http://www.ddj.com/dept/embedded/199500688?cid=RSSfeed_DDJ_All) Dr. Dobbs Portal Article

  -
  -
  - [Will your computer's "Secure Boot" turn out to be "Restricted Boot"?](https://www.fsf.org/campaigns/secure-boot-vs-restricted-boot)

  -
  - [2020年、ついにIntelのx86でDOSが動作しなくなる～UEFIからレガシーBIOS互換を削除(2017年11月17日)](https://pc.watch.impress.co.jp/docs/news/1092273.html)

[Category:ファームウェア](https://ja.wikipedia.org/wiki/Category:ファームウェア "wikilink") [Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.
3.
4.  ROM内のコードによるマシン初期化手順、ディスクパーティション、OSのブートに繋げる手順、等
5.  新規アーキテクチャであり、またその高機能に由来する高コストに加え、開発コストの回収の必要から当初は高価格の商品となるため、エンタープライズが当初の（結果としてはその後も）Itaniumのターゲットであった。
6.
7.
8.
9.
10.
11.
12.
13.
14. [GUIDパーティションテーブル](../Page/GUIDパーティションテーブル.md "wikilink")を使う場合のみ
15.
16.
17.
18.
19.
20.
21.
22.
23.
24. <http://download.microsoft.com/download/A/D/F/ADF5BEDE-C0FB-4CC0-A3E1-B38093F50BA1/windows8-hardware-cert-requirements-system.pdf>
25.
26.
27.
28.
29.
30. [Efi-shell.tianocore.org](https://efi-shell.tianocore.org/) for EFI shell information
31.
32.
33.
34.
35.
36.
37. <http://fedoraproject.org/wiki/Features/EFI>
38. [1](http://sourceforge.net/projects/elilo/) ELILO: EFI Linux Boot Loader
39.
40.
41.
42.
43.
44.
45.
46.
47.
48.
49.
50.
51.
52. [Asus P67 Motherboard Preview](http://www.bit-tech.net/hardware/motherboards/2010/11/16/asus-lga1155-motherboard-preview/1), .
53. [Intel shows PC booting Windows with UEFI firmware](http://apcmag.com/5862/intel_shows_pc_booting_windows_with_uefi_firmware)
54.
55.
56.
57.
58.
59.
60.
61.
62. [Windows 10搭載PCにはLinuxなどをインストールできなくなる可能性あり - GIGAZINE](http://gigazine.net/news/20150323-win10-secure-boot/)
63.
64.