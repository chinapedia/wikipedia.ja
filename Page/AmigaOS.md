> この記事は[AmigaOS](https://ja.wikipedia.org/wiki/AmigaOS)から翻訳されています。


**AmigaOS（アミガOS）**は、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") [Amiga](../Page/Amiga.md "wikilink")専用の[OSである](../Page/オペレーティングシステム.md "wikilink")。[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の[コモドール](../Page/コモドール.md "wikilink")が[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に開発し、Amiga 1000と共にリリースした。初期のバージョン (1.0-3.9) は[モトローラ](../Page/モトローラ.md "wikilink")の[68kシリーズの](../Page/MC68000.md "wikilink")[16ビット](../Page/16ビット.md "wikilink")および[32ビット](../Page/32ビット.md "wikilink")の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")で動作し、新しいAmigaOS 4は[PowerPC](../Page/PowerPC.md "wikilink")マイクロプロセッサでのみ動作する。

日本では一般的な知名度は低いが、子供向けテレビ番組の[ウゴウゴルーガ](../Page/ウゴウゴルーガ.md "wikilink")の[CGアニメでAmigaが使用された場面が出たことで一部では有名](../Page/コンピュータグラフィックス.md "wikilink")。日本語を含む[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")への対応に消極的であったため日本での販売は伸びなかったが、[北アメリカ](../Page/北アメリカ.md "wikilink")や[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")では、そのユニークなデザインで人気が高い。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:Amiga500_system1.jpg "wikilink")

AmigaOSは、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に販売が開始されたときから、[マルチタスク](../Page/マルチタスク.md "wikilink")と[カラー](../Page/カラー.md "wikilink")グラフィックスに対応するなど、当時としては先進的な機能が備えられていた。Execと呼ばれる[プリエンプティブ・マルチタスク型](https://ja.wikipedia.org/wiki/プリエンプション "wikilink")[カーネル](../Page/カーネル.md "wikilink")の上に、Amigaの独特なハードウェアの抽象化層があり、ディスクオペレーティングシステムの*AmigaDOS*、ウィンドウシステム[APIの](../Page/アプリケーションプログラミングインタフェース.md "wikilink")*Intuition*、[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) の*Workbench*が載っている。また、[コマンド行インタフェース](../Page/キャラクタユーザインタフェース.md "wikilink") (CLI) の*AmigaShell*もシステムに含まれている。GUIとCLIは相補的であり、同等の機能を有する。

しかし、ライバルの[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")との競争に敗れ、[1994年](../Page/1994年.md "wikilink")にコモドールが破産してしまい、一時は販売が停止してしまった。その後、コモドールの資産は数多くの企業に渡り、コモドール破産から5年後の[1999年](../Page/1999年.md "wikilink")に、新たに誕生したAmiga.intによって数年ぶりにAmigaOS 3.5が販売されたものの、先進的な機能が備えられておらず、特にこれといった特徴もなかったため、売り上げは低迷していた。

そんな中、[2004年](../Page/2004年.md "wikilink")に、一気にバージョンアップされたAmigaOS 4.0が発表。失敗に近かったAmigaOS 3.5よりも、新機能が多数増加され、一新された。

現在のAmigaの知的資産を所有するのは[Amiga Incである](https://ja.wikipedia.org/wiki/:en:Amiga_Inc "wikilink")。同社はAmigaOS 4の開発を監督する立場にあるが、実際の開発は[Hyperion Entertainmentに委託している](https://ja.wikipedia.org/wiki/:en:Hyperion_Entertainment "wikilink")。2006年12月20日、Amiga IncはHypelionのAmigaOS 4の開発ライセンスを終了させた。しかし、2009年9月30日、HyperionはAmigaOS 3.1の全世界での独占的かつ永久的な使用・開発・改変・販売・配布の権利とAmigaOS 4.xとその後の（AmigaOS 5 を含む）バージョンを販売する権利を獲得した\[1\]。

[2006年](../Page/2006年.md "wikilink")[12月24日](../Page/12月24日.md "wikilink")にAmigaOne向けのAmigaOS 4.0がリリースされた。

現在は、過去ほどの人気は失ったものの、再び人気を取り戻そうとしている。

## コンポーネント

AmigaOSは、[ROM上の](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")*Kickstart*とディスク上の*Workbench*に分かれている。KickstartとWorkbenchは同時にリリースされ、それぞれ対応したバージョン同士で使うようになっていた。しかし、[コモドール](../Page/コモドール.md "wikilink")がKickstartの開発をやめたため、Workbench 3.5以降はKickstart 3.1のROMにブート時に[パッチ](../Page/パッチ.md "wikilink")をあてる形で対応していた。

### Kickstart

**Kickstart**は[ブート](../Page/ブート.md "wikilink")ストラップROMである。Kickstartには標準的なAmigaハードウェアをブートするのに必要なコードと、AmigaOSの中核コンポーネントの多くを含んでいる。Kickstartの機能は[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")で言えば、[BIOSと](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")[OSの](../Page/オペレーティングシステム.md "wikilink")[カーネル](../Page/カーネル.md "wikilink")の主要部分に相当する。しかし、Kickstartはブート時に典型的なPCよりも多くの機能を提供でき、例えば完全なウィンドウ環境が立ち上げ途中でも利用可能である。

KickstartにはAmigaOSの *Exec*、*Intuition*、*AmigaDOS* 中核部、*Autoconfig* によって拡張ハードウェアを使う機能などが含まれる。つまり、Amigaは電源を入れただけでOSの基本的部分の多くを既に使える状態になっている。後のバージョンでは[IDEおよび](../Page/Advanced_Technology_Attachment.md "wikilink")[SCSIコントローラのドライバや](../Page/Small_Computer_System_Interface.md "wikilink")[PCカード](../Page/PCカード.md "wikilink")ポートのドライバなど、Amiga本体に追加されたハードウェアのドライバが追加されている。

立ち上げ時やリセット時、Kickstartは診断やシステムチェックを行い、Amigaの[チップセット](../Page/チップセット.md "wikilink")を初期化し、OS中核コンポーネントを初期化する。次に接続されているブートデバイスを調べ、優先度の高い方からブートを試みる。ブートデバイスが全くない場合、ユーザーに対してブートデバイス（通常フロッピーディスク）を挿入するよううながすメッセージをディスプレイに表示する。

### Workbench

**Workbench**は[Amiga](../Page/Amiga.md "wikilink")用の標準のグラフィカル・デスクトップ環境である。WorkbenchはOSそのものではなく、その上で動作する[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")である。ソフトウェアを動作させるのにWorkbench環境は必須ではない。実際多くのゲームは自前でハードウェアとメモリを制御するため、Kickstartから直接ブートできるようになっていた（[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")上にブートブロックがある）。

名前が示す通り、作業台（ワークベンチ）の[メタファー](../Page/メタファー.md "wikilink")を使っており、厳密にはデスクトップではない。ディレクトリは「引き出し」、実行ファイルは「工具（ツール）」、データファイルは「プロジェクト」、GUIウィジェットは「小道具（ガジェット）」とされている。多くの面でインタフェースは[Mac OSに似ている](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")。メインデスクトップには挿入されているディスクのアイコンとハードディスクドライブのパーティションのアイコンが表示され、それぞれのスクリーンの上部に1つのメニューバーがある。Macintoshとは異なり、マウスは2ボタン式だったが、右ボタンだけでMacintoshのようにプルダウンメニューを操作できる（ボタンを離したときに選択される）。

AmigaOS独特の機能として「マルチスクリーン」がある。AmigaOSのスクリーンはWorkbenchのデスクトップ環境を必要としない。それらのスクリーンは概念的には [X Window Systemの仮想デスクトップやワークスペースに似ているが](../Page/X_Window_System.md "wikilink")、必要に応じてアプリケーションプログラムが動的に生成する。それぞれのスクリーンは解像度や[色深度](../Page/色深度.md "wikilink")をそれぞれ別々に設定できる。スクリーンの右上端のガジェットでスクリーンを切り替える。OSが全スクリーンの内容をメモリ上に保持しており、描画をその時点で素早く行う。スクリーン上端のタイトルバーでスクリーンを上下にドラッグすることもできる。かつてのAmigaは専用チップセットの機能を使ってこれを実現していたが、AmigaOS 4では新たな技法を採用しており任意の方向にスクリーンをドラッグできる。異なるスクリーン間でのドラッグ・アンド・ドロップもできる。

Workbenchの基盤となっているのが*Intuition*というウィンドウシステムである。スクリーン / ウィンドウ / ガジェットの制御と描画、キーボードとマウスの入力の処理、プログラムへのメッセージパッシングなどを行う。

#### AmigaOS 2.x でのユーザインタフェースの改善

AmigaOS 2.0 までは統一的な[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")のデザイン標準は存在しなかった。アプリケーション開発においてはそれぞれが自前のウィジェット（ボタンやメニュー）を用意する必要があり、Intuitionが提供するサポートは最小限の範囲だった。AmigaOS 2.0には標準ウィジェットセットを提供する*gadtools.library*が追加され、ルック・アンド・フィールのガイドラインとなる*Amiga User Interface Style Guide*ができた。

また、それまでWorkbenchのスクリーンが唯一の共有可能スクリーンだったが、2.0以降ではアプリケーションが他のアプリケーションと共有可能なスクリーンを作成できるようになった。

また、AmigaOS 2.0では単純な[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")のマークアップ体系とブラウザである*[AmigaGuide](https://ja.wikipedia.org/wiki/:en:AmigaGuide "wikilink")*が導入され、アプリケーションのオンラインヘルプに使われた。また、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")風のスクリプト言語で動作する標準のソフトウェアインストールプログラム*Installer*も導入された。

AmigaOS 2.0までアプリケーションはキーボードやマウスの入力イベントを捉えるために[フックをしかけ](../Page/フック_\(プログラミング\).md "wikilink")、システム全体の入力ストリームを捉えるしかなかった。AmigaOS 2.0では入力イベントを修正したり詳細に調べたりするための標準インタフェース*Commodities*が提供されるようになった。これにより、グローバルな「ホットキー」のキー押下シーケンスの設定ができ、*Commodities Exchange*というレジストリでユーザーがどんな入力イベントがあるかを見ることができるようになった。

AmigaOS 2.1では*locale.library*が導入され、AmigaOSの英語以外への翻訳が行えるようになった\[2\]。

### AmigaDOS

**AmigaDOS** はAmigaOSのディスクオペレーティングシステム ([DOS](../Page/DOS_\(OS\).md "wikilink")) 部分である。[ファイルシステム](../Page/ファイルシステム.md "wikilink")、ファイルとディレクトリの操作、[コマンド行インタフェース](../Page/キャラクタユーザインタフェース.md "wikilink")、ファイルのリダイレクト、コンソール・ウィンドウなどの機能を有する。[コマンド・リダイレクション](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")、[パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")、[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")型の[スクリプト言語](../Page/スクリプト言語.md "wikilink")、システムのグローバル[変数やローカル変数といった仕組みを提供している](../Page/変数_\(プログラミング\).md "wikilink")。

AmigaOS 1.xでは[BCPL](../Page/BCPL.md "wikilink")で書かれた[TRIPOS](https://ja.wikipedia.org/wiki/TRIPOS "wikilink")をベースにしていた。しかし、他の言語とのインタフェースが難しく間違いやすいことがわかり、TRIPOSからの移植はあまり効率的ではなかった。

AmigaOS 2.x以降では1.xとの互換性を保ちつつ[C言語](../Page/C言語.md "wikilink")と[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")に書き直された。また、[サードパーティー](../Page/サードパーティー.md "wikilink")で行われていた*AmigaDOS Resource Project* (ARP)\[3\]の成果も取り入れている。ARPでも独自にBCPLで書かれたユーティリティやインタフェースを書き換えていた。

ARPはまた、Amiga向けの標準化されたファイル・リクエスター（ファイル選択ダイアログのようなもの）を提供し、UNIX風のワイルドカードをコマンドのパラメータに使えるようにした。他にもコマンドが受け付ける日付フォーマットの範囲を改善し、コマンドをメモリに常駐させてロード回数を減らす機能も追加された。

AmigaOS 4.0ではBCPLからの遺産は完全に払拭され、AmigaOS 4.1で64ビットサポートのための改造が行われている。

ファイル[拡張子](../Page/拡張子.md "wikilink")はAmigaOSでもよく使われるが必須ではなく、AmigaDOSも拡張子を特別に扱うことはない。単にユーザーがファイルの種類を名前から推測しやすくしているだけである。実行ファイルは[マジックナンバー (プログラム)を使って認識する](../Page/マジックナンバー_\(プログラム\).md "wikilink")。

### グラフィックス

AmigaOSはバージョン3までAmigaの本来のグラフィックス・チップセットのみを*graphics.library*経由でサポートしていた。このためアプリケーションではOSの機能を使わずに直接ハードウェアを操作するものが多かった。サードパーティー製グラフィックスカードは公式にはサポートされなかった。

AmigaOSが任意のグラフィックスシステムを直接サポートできる体系が*retargetable graphics* (RTG) である\[4\]。AmigaOS 3.5ではいくつかのRTGシステムがOSに同梱されており、Amiga本来のチップセット以外のグラフィックスカードも一部サポートされた。主なRTGシステムとして、[CyberGraphX](https://ja.wikipedia.org/wiki/:en:CyberGraphX "wikilink")、Picasso 96、EGSがある。

Amigaには[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")機能がないため、3Dグラフィックス・インタフェースも標準化されていない。そのためグラフィックスカードのベンダーがそれぞれ独自の標準（[MiniGL](https://ja.wikipedia.org/wiki/:en:MiniGL "wikilink")、[Warp3D](https://ja.wikipedia.org/wiki/:en:Warp3D "wikilink")、Storm[Mesa](../Page/Mesa_3D.md "wikilink") (*agl.library*)、CyberGLなど）を提供した。

Amigaが誕生したころ、デスクトップGUIや表示などに3Dグラフィックス・ライブラリを使うという考え方はほとんど存在しなかったが、Amigaはグラフィックス機能が強力だったため3DCGの開発プラットフォームとして広く使われた。初期の3DCG制作ソフトウェアとしてVideoScape 3Dや[TrueSpace](https://ja.wikipedia.org/wiki/:en:TrueSpace "wikilink") 3Dがある。その後も[Imagineや](https://ja.wikipedia.org/wiki/:en:Imagine_\(3D_modeling_software\) "wikilink")[LightWave](../Page/LightWave.md "wikilink")がAmiga向けにリリースされている。LightWaveは『[バビロン5](../Page/バビロン5.md "wikilink")』などのテレビ番組のCG制作にも使われた。

また、Amigaはビデオ信号の[ゲンロック](https://ja.wikipedia.org/wiki/ゲンロック "wikilink")（同期）が容易だということでも知られているが、ビデオキャプチャ用インタフェースは内蔵していない。最盛期にはAmiga向けのサードパーティー製ビデオキャプチャ用インタフェースが数多く製造販売されていた。

AmigaOS本来のグラフィック・エンジン兼[ウィジェット・ライブラリとして](../Page/ウィジェット・ツールキット.md "wikilink")*intuition.library*がある。AmigaOS 2.0ではそれがGadToolsに拡張された。Stefan Stuntzが開発した[Magic User Interface](https://ja.wikipedia.org/wiki/:en:Magic_User_Interface "wikilink") (MUI) が2.0以降のAmigaシステムで使われ、[AROSではMUIクローンの](https://ja.wikipedia.org/wiki/AROS_Research_Operating_System "wikilink")[Zuneを実装](https://ja.wikipedia.org/wiki/:en:Zune_\(GUI_toolkit\) "wikilink")、[MorphOS](https://ja.wikipedia.org/wiki/MorphOS "wikilink")ではMUIが標準のウィジェット・ツールキットとなっている。また、ClassACTというウィジェット・ツールキットは[ReAction GUIへと発展し](https://ja.wikipedia.org/wiki/:en:ReAction_GUI "wikilink")、AmigaOS 3.0および4.0で使われている。AmigaOS 4.0ではReAction GUIが標準の1つとされている。[CygnixはAmiga上で](../Page/Cygwin.md "wikilink")[X11互換グラフィック環境を提供するものである](../Page/X_Window_System.md "wikilink")。他にも[cairo](https://ja.wikipedia.org/wiki/cairo "wikilink")や[Anti-Grain Geometryといったグラフィックライブラリが一部ベンダーから登場している](https://ja.wikipedia.org/wiki/:en:Anti-Grain_Geometry "wikilink")。

現在のAmigaではクロスプラットフォームの[SDL](../Page/SDL.md "wikilink") (Simple DirectMedia Layer) エンジンをゲームや他のマルチメディアプログラムによく使っている。

AmigaOS 4.1では3Dのハードウェアアクセラレーションに対応したPorter-Duff画像合成エンジンを採用している。

### オーディオ

AmigaOSはバージョン3.1まで、Amigaの元々のチップセットのサウンド機能のみを*audio.device*経由でサポートしていた。サードパーティーのオーディオカードのサポートはベンダー任せだったが、デファクトスタンダードとして[AHI](https://ja.wikipedia.org/wiki/:en:AHI_\(Amiga\) "wikilink")\[5\]が採用されるようになった。AHIは68k系のAmigaOS 2.0以降でOSとは別にインストール可能である\[6\]。AmigaOS自体が[MIDI](../Page/MIDI.md "wikilink")をサポートしたのは3.1になってからで、Roger Dannenbergの*camd.library*が標準MIDI APIとして採用された。コモドール版の*camd.library*にはシリアルポート用ドライバも組み込まれている。後にKjetil Matheussenが公開したオープンソース版*camd.library*にはシリアルポート用ドライバがないが、代わりに外部ドライバを提供している。

#### 音声合成

Amigaには当初からSoftvoice, Inc.\[7\]の開発した[音声合成](../Page/音声合成.md "wikilink")ソフトウェアがあった。これは大まかに3つの部分に分けられる。[アメリカ英語](../Page/アメリカ英語.md "wikilink")で使用するすべての[音素](../Page/音素.md "wikilink")を音響信号に変換する*narrator.device*、英文テキストをアメリカ英語の音素列に変換する*translator.library*、コマンドラインのユーザーが出力を音声にリダイレクトできる*SPEAK:*ハンドラである。

AmigaOS 1.xにはユーティリティとして*Say*プログラムがあり、[AmigaBASIC](https://ja.wikipedia.org/wiki/AmigaBASIC "wikilink")で音声を出力するデモプログラムが付属していた。

音声合成機能はサードパーティーのプログラムでも使われ、特に教育ソフトでの利用が多かった。ワープロソフトのProwriteと Excellence\!には文書を読み上げる機能があった。

*narrator.device*の扱える音素には限界があったが、Francesco Devittは任意の言語を音素列に変換する*translator.library*を開発した。ただし対象言語には規則群を設定する必要があり、限定的な多言語音声合成を可能とした\[8\]。

Workbench 2.0まで音声合成がサポートされていたが、2.1以降は音声合成ソフトウェアが省かれている\[9\]。

### ARexx

AmigaOSは、ARexx (Amiga Rexx) と呼ばれる[REXX](../Page/REXX.md "wikilink")言語をサポートしている。REXXはスクリプト言語で、[AppleScript](../Page/AppleScript.md "wikilink")のようにOSのスクリプティングにも使え、[Microsoft Officeでの](../Page/Microsoft_Office.md "wikilink")[VBAのようにアプリケーション内のスクリプティングにも使え](../Page/Visual_Basic_for_Applications.md "wikilink")、プログラム間の通信にも使える。ユーザーにとっては1つのスクリプト言語であらゆることができるため、便利である。

プログラムは「ARexxポート」の文字列メッセージを待ち受けることができる。このメッセージをユーザーがマウスでボタンを押下したのと似たような形でプログラムが解釈できる。例えば、電子メールプログラム内で表示中の電子メールを読み取るARexxスクリプトを動作させ、外部のプログラムを起動して電子メールの内容を渡して処理するといったことができる。これを使えばアプリケーション間で一時ファイルを経由することなくメモリ上でデータをやりとりできる。

### RAMディスク

AmigaOSには動的に大きさの変わる[RAMディスク](../Page/RAMディスク.md "wikilink")があり、内容によって自動的にサイズが変化する。AmigaOS 2.x以降、ブート時にシステム設定ファイルがRAMディスクにロードされ、OSの高速化を図っている。他のファイルもRAMディスクにコピーでき、アクセスを高速化できる。また、AmigaOS 2.x以降からRAMディスク上のファイルの更新を検知して通知する機能をサポートした。

固定サイズのRAMディスクもサポートしており、中身を退避させて立ち上げ時に再ロードできる。これは通常「RADディスク」と呼ばれており、（ブートセクタがあれば）ブートデバイスとしても使える。

### ブーﾄブロック

Kickstartは立ち上げ時にブート可能デバイス（一般にフロッピーディスクまたはハードディスク）からの[ブート](../Page/ブート.md "wikilink")を試みる。フロッピーディスクの場合、ディスクの先頭の2セクタ（ブートブロック）をまず読み込み、そこに格納されているブート命令列を実行する。通常このコードはOS（AmigaDOSとGUI）をロードしてそれに制御を渡し、そのディスクをブートボリュームとして使用する。このようなディスクは他にどういう中身が格納されていても「ブートディスク」または「ブータブルディスク」と呼ばれる。"install" コマンドを使えば、ブランクディスクにブートブロックを書き込むことができる。ゲームなどのソフトウェアの媒体には独自のブートブロックが書かれている。そのためゲームやデモといったアプリケーションでは、AmigaOSを使わずにメモリやハードウェアを直接制御することになる。

ブートブロックは[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")作者の格好の攻撃対象となった。ブートブロックがウイルスに感染するとブートコードが書き換えられるため、ブートディスクはうまく起動できなくなる。そのような初期のウイルスとして[SCA virusがある](https://ja.wikipedia.org/wiki/:en:SCA_virus "wikilink")。

## 技術概要

[John C. Dvorakは](https://ja.wikipedia.org/wiki/:en:John_C._Dvorak "wikilink")1996年、次のように記している。

### ライブラリとデバイス

AmigaOSの[モジュール](../Page/モジュール.md "wikilink")化技法は[動的読み込みの共有ライブラリが中心であり](../Page/ライブラリ.md "wikilink")、ディスク上の "`.library`" という拡張子のついたファイルとして格納されているものと、Kickstart ROM内に格納されているものがある。ライブラリ関数へのアクセスは全て間接[ジャンプテーブルを経由して行い](../Page/テーブルジャンプ.md "wikilink")、ジャンプテーブルにはライブラリのベースポインタからのオフセットが格納されている。そのため、全てのライブラリ関数に実行時に[パッチ](../Page/パッチ.md "wikilink")をあてたり[フックをしかけることができ](../Page/フック_\(プログラミング\).md "wikilink")、これはROMに格納されたライブラリでも同様である。

AmigaOSで最も重要なライブラリは*exec.library*であり、ライブラリであると同時に[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")*Exec*と見なすことができる。システム上で動作するタスク群の[スケジューリング](../Page/スケジューリング.md "wikilink")を行い、優先度付きの[ラウンドロビン・スケジューリング](../Page/ラウンドロビン・スケジューリング.md "wikilink")で[プリエンプティブ・マルチタスクを実現する](https://ja.wikipedia.org/wiki/プリエンプション "wikilink")。Exec は他のライブラリへのアクセスを提供し、[メッセージ・パッシングによる高度な](../Page/メッセージ_\(コンピュータ\).md "wikilink")[プロセス間通信](../Page/プロセス間通信.md "wikilink")を提供する。一般にマイクロカーネル実装はメッセージをアドレス空間の間でコピーする必要があるため、性能に問題が生じる。しかし、AmigaOSは1つのアドレス空間しか持たないため、Exec によるメッセージパッシングは非常に効率的である。AmigaOS内で唯一の固定アドレス（アドレス4番地）には*exec.library*へのポインタが格納されており、これを使って他のライブラリにアクセスすることができる。Exec は[カール・サセンラス](https://ja.wikipedia.org/wiki/カール・サセンラス "wikilink")が設計・実装した。

それまでのOSとは異なり、Execカーネルは特権モードになっていない。当時の68kファミリ向けのOS（[Atari TOS](https://ja.wikipedia.org/wiki/:en:Atari_TOS "wikilink")、[SunOS](../Page/SunOS.md "wikilink")など）は[トラップ命令でカーネルの機能を呼び出していた](../Page/例外処理.md "wikilink")。それにより、カーネル機能は68kの「スーパーバイザモード」で動作し、ユーザーソフトウェアは特権のない「ユーザーモード」で動作する。68k上の [Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink") でさえスーパーバイザモードを使っていた。それに対して Exec ではユーザーモードでジャンプテーブル経由で機能を呼び出す。スーパーバイザモードが必要なときは（スーパーバイザモードでないと実行できない命令がある）、カーネルであってもユーザープログラムであってもライブラリ関数のSupervisor()またはSuperState()を使う。

[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")もライブラリになっているが、標準化されたインタフェースを実装している。アプリケーションは通常、デバイスドライバをライブラリとして直接呼び出すことはなく、*exec.library*のI/O機能を経由して間接的にアクセスする。デバイスドライバも、ディスク上のファイルの形で格納されているもの（拡張子は "`.device`"）とKickstart ROMに格納されているものがある。

### Datatypes

DatatypesはAmiga上のデータファイルを扱う独特の手法である。一連の "datatype" を扱う集中型システムであり、対応するdatatypeが存在する任意のデータファイルを読み書き、ロード/セーブできる一連の小さなプログラムの集合体と見ることができる。

ペイントプログラムなどのAmigaの生産性ソフトウェアは、存在する様々な画像ファイルを扱うためにそれぞれの記述子を埋め込む必要がない。Amiga向けソフトウェアの開発においては、Datatypesを扱うコードを埋め込めばよく、そうすることでDatatypesシステムが扱えるあらゆる画像ファイルをオープンしたりセーブしたりできるようになる。

例えば、`jpeg.datatype`と`tiff.datatype`はそれぞれ対応するファイルフォーマット（[JPEG](../Page/JPEG.md "wikilink")と[TIFF画像ファイル](../Page/Tagged_Image_File_Format.md "wikilink")）があり、Datatypesに対応したプログラムであれば、これらのdatatypeに対応した機能を自動的にロードして使うことができる。

datatypeのコードを書いて追加することもでき、新たに登場したファイルフォーマットにも対応可能である。

### ハンドラとファイルシステム

デバイスおよびリソース管理の上位層はライブラリとは異なるタスク型のハンドラ (handler) で制御され、メッセージ・パッシングでやり取りする。

重要な種類のハンドラとして[ファイルシステム](../Page/ファイルシステム.md "wikilink")・ハンドラがある。AmigaOSではハンドラを書きさえすれば任意のファイルシステムを使用できる。これを利用したプログラムとしてAmiga以外のフロッピーディスクを扱えるようにした [CrossDOS](https://ja.wikipedia.org/wiki/:en:CrossDOS "wikilink") があり、[OFSと](https://ja.wikipedia.org/wiki/:en:Amiga_Old_File_System "wikilink")[FFSというAmigaOSの標準ファイルシステム以外のファイルシステムも少数ながら存在する](https://ja.wikipedia.org/wiki/:en:Amiga_Fast_File_System "wikilink")。これを使えば、[ジャーナリングや](../Page/ジャーナリングファイルシステム.md "wikilink")[ファイルパーミッション](../Page/ファイルパーミッション.md "wikilink")など標準では存在しない機能を追加することもできる。

ハンドラはDOSに対して「デバイス名」で提示されることが多く、それを使ってそのハンドラに対応する周辺機器にアクセスできる。

例えば、*SPEAK:*ハンドラにはテキストを送ることができる。そのハンドラは*translator.library*を使ってテキストを[音素](../Page/音素.md "wikilink")列に変換し、それらを*narrator.device*に送ると音素列が音声信号に変換され、そこから*audio.device*に音声信号を送ってAmigaのオーディオ・ハードウェアで音声を再生する。

デバイス名は大文字と小文字を区別しない文字列で表され（通常、大文字で表現）、その後ろに[コロンが付く](../Page/コロン_\(記号\).md "wikilink")。コロンの後に規則子 (specifier) を付けることができ、それによって「何」に「どのように」アクセスするのかという情報を補足できる。ファイルシステムの場合、規則子としてそのファイルシステム内のファイルのパス名を指定することが多い。他のハンドラの場合、使いたい入出力チャンネルの指定などを規則子で行う。例えばシリアルポート *SER:* の場合、規則子に[ビットレート](../Page/ビット毎秒.md "wikilink")、スタートビット、ストップビットなどといった情報を指定する。

ファイルシステムではデバイス名として「ドライブ名」を提示する。例えば*DF0:*はデフォルトでは1台目のフロッピーディスクドライブを指す。多くのシステムでは*DH0:*が1台目のハードディスクドライブを指す。

ファイルシステムはデバイス名と同様の形式で「ボリューム名」でも指定できる。この場合、対象周辺機器に挿入されている特定の媒体を識別できる。例えば*DF0:*に挿入されているフロッピーディスクの名前が "Workbench" なら、*Workbench:*とボリューム名を指定することで*DF0:*にある特定のフロッピーディスクを指定できる。

*DF0:*ドライブに "Work" というディスクがあり、そのファイルシステムの "Win" というディレクトリにある "Amp" というファイルにアクセスしたい場合、

`DF0:Win/Amp`

または

`Work:Win/Amp`

とする。ただし、これらは完全に同じではない。後者の場合、ボリューム名が指定されているので、*DF0:*に "Work" というボリュームがない場合は*DF0:*にアクセスしない。その場合、"Wrok" というボリュームを入れるよう促すようなメッセージが表示される。

[プログラムは](../Page/プログラム_\(コンピュータ\).md "wikilink")、絶対位置（ドライブ、ボリュームなど）が不明なファイルにアクセスしなければならないことがある。その場合わかっているのは「論理パス」だけであり、そのファイルがライブラリなのか文書ファイルなのか、あるいはプログラムのメッセージの翻訳なのかなどということしかわからない。

このような場合、AmigaOSでは「アサイン (assign)」を使う。アサインもデバイス名と同じ形式だが、特定のファイルシステムのディレクトリを指している。1つのアサインが指す場所はユーザーが好きなようにいつでも変更できる。これは[MS-DOS](../Page/MS-DOS.md "wikilink")の*subst*コマンドと似ているが、同一ではない。アサインはまた、1つで複数の物理的位置を同時に示すこともでき、物理的に別々の実体のあるものを論理的にまとめることもできる。AmigaOSシステムで標準的に使われているアサインとして以下のものがある。

  - *SYS:*
    ブートドライブのルートディレクトリを指す。
  - *C:*
    シェルのコマンド群があるディレクトリを指す。ブート時、もしあればSYS:Cであり、さもなくばSYS:と同じである。従ってコマンドパスのデフォルトはC:とカレントディレクトリである。C:に実行ファイルを置いておけば、単にファイル名をタイプするだけで実行できる。
  - *DEVS:*
    システムのデバイス群のあるディレクトリを指す。ブート時、もしあればSYS:Devsであり、さもなくばSYS:と同じである。
  - *L:*
    AmigaDOSのハンドラとファイルシステムのあるディレクトリを指す。ブート時、もしあればSYS:Lであり、そのディレクトリがない場合L:は自動生成されない。
  - *LIBS:*
    システムのライブラリのあるディレクトリを指す。ブート時、もしあればSYS:Libsであり、さもなくばSYS:と同じである。
  - *S:*
    スクリプトのあるディレクトリを指し、特にブート時に（もしあれば）自動実行されるスクリプトである`startup-sequence`のあるディレクトリを指す。ブート時、もしあればSYS:Sであり、そのディレクトリがない場合S:は自動生成されない。
  - *PROGDIR:*
    現在実行中の実行ファイルが存在するディレクトリを常に指している特殊なアサイン。したがって "SYS:Tools/Multiview" と "SYS:System/Format" を実行中なら、MultiviewにとってはPROGDIR:はSYS:Toolsを指し、同時にFormatコマンドにとってはSYS:Systemを指している。この機能はWorkbench 2.0で導入された。

### ページングメモリとスワップパーティション

AmigaOS 4.0の最新アップデート版では、物理メモリを割り当て、システムが不活発なときに[デフラグメンテーション](../Page/デフラグメンテーション.md "wikilink")を行う新たな知的システムを導入した。[スラブアロケーション](https://ja.wikipedia.org/wiki/スラブアロケーション "wikilink")方式に基づくもので、ページングメモリを扱う機能もあり、AmigaOSでも物理メモリの内容を二次記憶装置に退避させスワップする一種の[仮想記憶](../Page/仮想記憶.md "wikilink")が可能となった\[10\]\[11\]。その後、[ページング方式](../Page/ページング方式.md "wikilink")が評価され AmigaOS 4.1で最終的に実装された。AmigaOS 4.0では物理メモリの操作に[バディ・システム](https://ja.wikipedia.org/wiki/動的メモリ確保#バディブロック "wikilink")・アルゴリズムを使っている。

AmigaOS 4.1では、オプションで任意の大きさのスワップパーティションを作成でき、OSインストール時に独立したパーティションとしてフォーマットする。スワップメモリは、デフラグメンテーションを行ってもメモリ要求を満たせないときに自動的に使われる。スワップメモリを使うかどうかは AmigaOS システムの **Preferences** にあるオプションボタンで指定でき、任意の時点で物理メモリのみで動作するよう設定できる。

## 他のOSへの影響

### クローン

[thumb](https://ja.wikipedia.org/wiki/ファイル:AmigaOS_3_and_clones.svg "wikilink") AmigaOSからは少なくとも2つの「クローン」オペレーティングシステムが生まれている。

  - [AROS Research Operating System](https://ja.wikipedia.org/wiki/AROS_Research_Operating_System "wikilink") (AROS)
    AmigaOSのAPIを移植性のあるオープンソースのオペレーティングシステムとしたクローン。AmigaOSとは（68k上で動作させない限り）バイナリ互換ではないが、ユーザーによればソース互換性は高いという。
  - [MorphOS](https://ja.wikipedia.org/wiki/MorphOS "wikilink")
    PowerPC向けのオペレーティングシステムだが、一部のAmigaハードウェアでも動作する。行儀のよいAmigaOS用アプリケーション（つまり、Amigaのハードウェアに直接アクセスしようとしないもの）についてはバイナリ互換を保っている。

### その他の影響

  - [DragonFly BSD](../Page/DragonFly_BSD.md "wikilink")
    厳密にはAmigaとは関係ないが、[FreeBSD](../Page/FreeBSD.md "wikilink") 4.8からフォークしたDragonFly BSDはFreeBSDの開発者でAmigaのプログラマだった[Matt Dillonが開発した](https://ja.wikipedia.org/wiki/:en:Matt_Dillon_\(computer_scientist\) "wikilink")。DragonFly BSDはFreeBSDの[カーネル](../Page/カーネル.md "wikilink")をよりAmigaOSにアーキテクチャ的に近くしたもので、カーネル内のメッセージパッシング機能があり、非常に効率的なほぼ[排他制御](../Page/排他制御.md "wikilink")を使わない[SMPサポートが可能である](../Page/対称型マルチプロセッシング.md "wikilink")。
  - [BeOS](../Page/BeOS.md "wikilink")
    AmigaOSのDatatypesを基本として受け継いでおり、OS全体があらゆる種類のファイル（テキスト、音声、動画、文書など）を標準のファイル記述子から認識できる。Datatypeシステムは、全システムと生産性ツールが様々なファイルをロードする機能を持つ必要をなくし、標準のファイルローダーやセーバーを提供する。
  - [AtheOS](../Page/AtheOS.md "wikilink")
    AmigaOSに着想を得たOSで、当初はAmigaOSのクローンを意図していた\[12\]。AtheOSからフォークした[Syllable](https://ja.wikipedia.org/wiki/Syllable "wikilink")もAmigaOSと[BeOS](../Page/BeOS.md "wikilink")の機能を一部受け継いでいる。
  - [3DO](../Page/3DO.md "wikilink") Interactive Multiplayer
    AmigaOSとよく似ており、AmigaOSの Intuition のUIを開発した [RJ Mical](https://ja.wikipedia.org/wiki/:en:RJ_Mical "wikilink")\[13\] が開発した\[14\]。

## イースターエッグ

AmigaOSの一部バージョンには[著作権](../Page/著作権.md "wikilink")メッセージが[イースター・エッグになっていて](../Page/イースター・エッグ_\(コンピュータ\).md "wikilink")、ちょっとしたトリッキーなアクセスで表示できる。

  - バージョン1.xでは、両側のシフトキーと両側の[Altキー](https://ja.wikipedia.org/wiki/Altキー "wikilink")とファンクションキーのF1からF10までを押下すると、タイトルバーに著作権メッセージが表示される。例えば F10 を押下すると "Moral support: Joe Pillow and the Dancing Fools" と表示される。Joe Pillowとは、Amigaのプロトタイプをコンピュータショーに出展するために旅客機の座席に載せて運んだときのチケット予約の名前である\[15\]。
  - バージョン2.xと3.0では、Workbenchのメニューから "About..." を繰り返し選択し、[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")をいくつも開く。そのダイアログボックスを20個ほど同時に表示させると、通常とは異なるダイアログボックスが出てきて、そこに秘密のメッセージが表示される。バージョン3.1では、単に "About..." のダイアログボックスを開けば、そこにそのメッセージも同時に表示されるようになった。
  - Amiga 1000のAmigaDOS 1.0向けのKickstartマスターフロッピーディスクは複製しても消去されず、そこにソースコードなどのファイルの残骸が残っていた。

## 脚注・出典

## 関連項目

  - [Amiga](../Page/Amiga.md "wikilink")
  - [AmigaOne](https://ja.wikipedia.org/wiki/AmigaOne "wikilink")
  - [平沢進](https://ja.wikipedia.org/wiki/平沢進 "wikilink")
  - [岩井俊雄](../Page/岩井俊雄.md "wikilink")
  - [Guru Meditation](../Page/Guru_Meditation.md "wikilink")

## 外部リンク

  - [AMIGA](http://www.amiga.com/) (英語)
  - [www.chiptune.com](http://www.chiptune.com) (JavaScriptによるAmigaDOS1.3のエミュレート)
  - [AmigaOS Support homepage](http://os.amigaworld.de/index.php?lang=en)
  - [The Workbench Nostalgia Page](http://www.gregdonner.org/workbench) – AmigaOSの各バージョンの非常に詳細な情報
  - [Reference Library](http://gega.homelinux.net/AmigaDevDocs/)
  - [Amiga Developer Help Site](http://amiga.sourceforge.net/amigadevhelp/)
  - [Famous Amiga Uses](http://wigilius.se/amiga/)

[Category:AmigaOS](https://ja.wikipedia.org/wiki/Category:AmigaOS "wikilink") [Category:OSファミリ](https://ja.wikipedia.org/wiki/Category:OSファミリ "wikilink") [Category:1985年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1985年のソフトウェア "wikilink")

1.
2.
3.  <http://uk.aminet.net/misc/antiq/ARP_13.readme>
4.   090427 amigau.com
5.  [AHI — Retargetable Audio for AmigaOS et al.](http://www.lysator.liu.se/ahi/)
6.  <http://arp2.berlios.de/ahi/#binaries> 2010-11-19
7.  <http://www.text2speech.com/#aboutsv>
8.  <http://uk.aminet.net/util/libs/translator42.readme>
9.
10.
11.
12.
13. [Mical Page](http://www.mical.org/workhistory/)
14. [A history of the Amiga, part 3: The first prototype: Page 3](http://arstechnica.com/articles/culture/a-history-of-the-amiga-part-3.ars/3)
15. Article about Joe Pillow on AmigaU <http://www.amigau.com/aig/pillow.html>