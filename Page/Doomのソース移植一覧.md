> この記事は[Doomのソース移植一覧](https://ja.wikipedia.org/wiki/Doomのソース移植一覧)から翻訳されています。


この記事は、元々[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")『[Doom](../Page/DOOM.md "wikilink")』で使用されていた**Doomエンジンの非公式ソース（コード）移植**の一覧である。ほとんどの場合、ここに示されているソース移植は、[id Softwareまたは関連会社によって作成された](https://ja.wikipedia.org/wiki/id_Software "wikilink")[Doomの公式版](../Page/Doomの公式版.md "wikilink")とは対照的に、[Doomコミュニティによって行われた改造であり](../Page/DOOM.md "wikilink")、日本語のメディアでは互換エンジンと呼ばれることもある\[1\]。

Doomエンジンの[ソースコード](../Page/ソースコード.md "wikilink")は1997年12月23日に公開された。Doomは元々[MS-DOS](../Page/MS-DOS.md "wikilink")用に制作されたが、DOS版ではプロプライエタリなサウンドライブラリを使用していたため、公開されたオリジナルのソースコードはDOS版の後に発売された[Linux](../Page/Linux.md "wikilink")版のものであった\[2\]。ソース移植の本来の目的はクロスプラットフォームの互換性であったが、*Doom*ソースコードの公開後まもなく、プログラマー達は独自のソース移植にある古い未対処の『Doom』のバグと欠陥を修正し、その後ゲーム機能の強化やゲームプレイを変更する独自の改造（Mod）を導入した。

このソースコードはもともと商用利用を禁じ、プログラマが[実行可能形式で公開したModのソースコードを提供することを要求しないプロプライエタリなライセンスの下で公開されていたが](../Page/実行ファイル.md "wikilink")、コミュニティからの要望を受けて1999年10月3日に[GNU General Publicの下で再公開された](../Page/GNU_General_Public_License.md "wikilink")。

## パソコン

### GNU/LinuxおよびWindows（IBM PC互換）

#### GLDoom

最初のソース移植の1つであり、よく知られているものの1つであるGLDoomは、DoomエンジンにOpenGLアクセラレーションされたグラフィックサポートを導入する最初の試みであった。プロジェクトは、1999年に開発者の自宅での事故でソースコードが失われたため滅びた\[3\]。しかし、2010年4月に作者は友人のハードドライブの1つでGLDoomのソースを再発見し、いくつかの修正を行った。それにもかかわらず、2010年4月11日現在、開発は休止状態が続いている\[4\]。

#### Boomと派生

Boomは、[TeamTNT](../Page/TeamTNT.md "wikilink")によるDoomソースコードのDOS向け移植である。多くのソフトウェアの不具合を修正し、エンジンに他の多くのソフトウェア拡張機能を追加しており、その追加機能は大半の最新バージョンのDoomソース移植（PrBoom+、ZDoom、Doom Legacyなど）に組み込まれている。Boomの最後のアップデート、バージョン2.02は1998年10月22日に公開された。1999年10月、Boomのソースコードが公開された\[5\]。ソース移植としてのBoomのさらなる開発は、DOS向けはMBF、Windows向けはPrBoom、Linux向けはLxDoomとして継続された。後者の2つは後にPrBoomとして統合され、MBFの機能の多くを引き継いだため、PrBoomの後継であるPrBoom+は事実上、Boomの現代的な等価物である。

##### LxDoom

LxDoomは、1999年にColin PhippsがBoomをベースとして制作したLinux向けのソース移植である。特にオリジナルのDoomから継承された制限とバグの削除、および計算効率の向上に重点を置いていた。2000年にはWindowsのソース移植であるPrBoomと統合し、その基礎となっている。それ以来、PrBoomはWindowsとLinuxの両方のバージョンで利用が可能であった。

##### RORDoom

RORDoomは、Julian Aubourgが作成し2000年に公開したDOSベースのソース移植である。これは、セクターが他のセクターと重なることを可能にする機能（room-over-room）を組み込んだ最初のDoomソース移植である。これにより、Doomエンジンで部屋を別の部屋の上に重ねることができないという問題が解消された。

##### Eternity Engine

Eternity Engineは、 [GNU General Public Licenseの下でライセンスされたWindowsのソース移植である](../Page/GNU_General_Public_License.md "wikilink")。2001年1月8日にバージョン3.29ベータ1として最初に公開された。元々はDoomの全改造（TC）を動作させるためのものであったが、そのプロジェクトが中断した後（最終的に2006年にキャンセルされた）、エンジンが主役となった。エンジンはSmack My Marine Up（SMMU）をベースにしている。スクリプト、ポータル、ポリオブジェクト、『Heretic』のサポートなどの機能が含まれている。

##### Marine's Best Friend

Marine's Best Friend（MBF）は、DOSベースのソース移植である。Boomをベースとしており、高解像度グラフィックス、強化されたモンスター[AI](../Page/人工知能.md "wikilink")、Doomのプレリリースベータ版の[エミュレーションおよびプレイヤーをフォローして支援する](../Page/エミュレータ.md "wikilink")「ヘルパー」（具体的にはエンジン名が示す犬を指す）を含むいくつかの新機能を追加する。MBFはLee Killoughによって開発され、現在はアップデートされていない。そのコードは後にソース移植の「Smack My Marine Up」のベースとして使用され、次にEternity Engineを構築するために使用された。コードの一部はPrBoomでも採用された。2004年8月、James HaleyとSteven McGranahanは、Marine's Best FriendをWindowsにWinMBFとして移植した。WinMBFは2005年1月に最後のアップデートが行われた。

##### PrBoom

PrBoomは、BoomおよびMBFの[Linux](../Page/Linux.md "wikilink")および[Windows移植から派生したDoomのソース移植であり](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、オプションの[OpenGL](../Page/OpenGL.md "wikilink")レンダラーと、以前の実行ファイル（Doomバージョン1.9、Boom、MBFなど）の動作を本質的な方法で復元できるオプションが含まれている。当初は[Windowsと](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](../Page/Linux.md "wikilink")用に設計され、AmigaOS 4、[AROS](https://ja.wikipedia.org/wiki/AROS_Research_Operating_System "wikilink")、[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")、[GP2X](../Page/GP2X.md "wikilink")、[MorphOS](https://ja.wikipedia.org/wiki/MorphOS "wikilink")、[Nintendo DS](../Page/ニンテンドーDS.md "wikilink")、[Nintendo 3DS](https://ja.wikipedia.org/wiki/ニンテンドー3DS "wikilink")、[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")、[Rockbox](../Page/Rockbox.md "wikilink")にも移植されている。 PrBoom+という名前のバリエーションでは、デモの録音および表示機能が強化されている。id Software公式のDoom iPhone移植版はPrBoomをベースとしている\[6\]。ソース移植は、[Freedoomとともに](../Page/Doomの改造.md "wikilink")[Ubuntuソフトウェアセンター](https://ja.wikipedia.org/wiki/Ubuntuソフトウェアセンター "wikilink")と[Fedora](../Page/Fedora.md "wikilink")の[RPMソフトウェアリポジトリにパッケージ化されている](../Page/RPM_Package_Manager.md "wikilink")。PrBoomは、2008年11月9日にバージョン2.5.0として最終更新が行われ、PrBoom+は、2016年1月10日にバージョン2.5.1.4として最終更新が行われた。

PrBoomとPrBoom+は他のいくつかのDoomソース移植よりもシンプルであるが、オリジナルのゲームの動作に比較的近いままであり、優れた[デモサポートを備えているため](../Page/やり込み.md "wikilink")、好まれることが多い。ただし、他の移植の一部のバグ修正と動作の変更は、オリジナルのゲームプレイ用に制作されたステージのプレイ方法がアンバランスになり、プレーヤーに特定の利点または欠点を与える可能性がある。

#### Doomsday Engineと派生

Doomsday Engineは、GPLv2ライセンスのソース移植（以前のjDoom、jHexen、jHereticを組み込んだもの）であり、 [Linux](../Page/Linux.md "wikilink")、[Mac OS Xおよび](../Page/MacOS.md "wikilink")[Windows上で動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[7\]。このソース移植は、『Heretic』および『Hexen：Beyond Heretic』にも対応している。ハードウェアアクセラレーションエンジンは、3Dモデル、オブジェクトと動きのスムージング、シャドウ、ダイナミックライティングなどの機能をサポートしている。また、拡張機能を編集するためのXGラインおよびセクタータイプ、および組み込みのマスターサーバーゲームブラウザー（ランチャー）も内蔵している。

##### Risen3D

Risen3Dは、Doomsday Engineのバージョン1.7.8をベースにした[Windows専用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[フォークで](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")2003年3月15日に公開された。当初は*Boom*マップ編集機能のサポートが追加されただけであったためBoomsdayと呼ばれていた。 最新バージョンであるバージョン2.2.26は2014年7月に公開された。

#### DOSDoomと派生物

1997年12月23日に公開されたDOSDoomは、公開されたDoomのソース移植としては初のものであった。DOSDoomは公開されたLinux版のDoomのソースコードを取得してDOSに移植したChi Hoangによって作成された。その後の更新で半透明性、高解像度、16ビットカラーレンダリングなど、オリジナルのDoomソースコードの公開直後には見られなかったいくつかの新機能が搭載されていった。DOSDoomの最終更新は1999年4月10日で、バージョン0.653が公開された。

##### Doom Legacy

Doom Legacyは、元々はDOSDoomのフォークとして書かれたソース移植で、マウスルック、ジャンプ、コンソール、32プレイヤーのデスマッチ、スキン、そして後にWindows、Linux、 [Mac OS Xのネイティブ移植を導入している](../Page/MacOS.md "wikilink")。また、多くのBoom機能と3Dアクセラレーションをサポートする。2000年12月に公開されたバージョン1.31ではステージのフロアの上に直接フロアを含められるようになるなどの追加機能が含まれており、オリジナルのDoomエンジンのゲームのようにステージを厳密に2Dにする必要はない。Doom LegacyにはFragglescriptと呼ばれる独自のスクリプト言語を有している。バージョン2はかなり長い間開発中である。

##### EDGE

Enhanced Doom Gaming Engine（EDGE）は、DOSDoomから派生した移植で2000年6月20日に最初に公開された。EDGEの最も魅力的な機能は、実行ファイルの外部にあるテキストファイル内のすべてのゲームの動作を記述するDDFシステムである。 その結果、他のソース移植に存在する制限をはるかに少なくして多くの新しい武器や機能を追加するために拡張性を使用するモッダーの間で人気を博している。EDGEはMS-DOS、Windows、Linux、BeOS、Mac OS Xなど多くのオペレーティングシステムに移植されている。EDGEの最終アップデートのバージョン1.35は、2011年4月9日に公開された。

EDGEの後継である3DGEは2011年4月11日に初公開された。新機能の中には、スクリプト機能の改善、バグ修正、OpenGLの機能強化、『Heretic』のサポート、画面分割マルチプレイなどがある。最終更新日は2016年8月22日であるが、チームは開発版の公開を頻繁に行っている。このエンジンは、Windows、Linux、Mac OSX、OpenBSD、[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")などの複数のプラットフォームに移植されている。

#### Vavoom

VavoomはDoom、『Heretic』および『Hexen：Beyond Heretic』のソースツリーをマージして作られたソース移植。VavoomではQuakeのソースコードの一部（主にネットワーキングとレンダリングに使用される）も使用しており、『Strife：Quest for the Sigil』をサポートする最初のソース移植であった。1999年9月から開発が開始され、2000年6月14日に初公開された。その機能には、カラーライティングとソフトウェア、Direct 3DおよびOpenGLレンダラー、フリールックのサポート、3DフロアおよびBoomの拡張属性のサポートを備えた真の3Dポリゴンエンジンがある。このソース移植は、デフォルトでエンジンが使用するすべてのゲームの[シェアウェア](../Page/シェアウェア.md "wikilink")ステージを取得する[無料のインストーラーとともに](../Page/フリーソフトウェア.md "wikilink")、[Fedora](../Page/Fedora.md "wikilink") [RPMソフトウェアリポジトリにパッケージ化されている](../Page/RPM_Package_Manager.md "wikilink")。Vavoomの最新バージョンであるバージョン1.33は2010年12月31日に公開された。

#### ZDoomと派生

ZDoomは、Microsoft Windows、Linux、Mac OS Xをターゲットにしたソース移植である。最初のバージョンであるバージョン1.11は、1998年3月6日に公開された。ZDoom は、編集の観点から最も先進的で機能満載の Doom ソース移植の一つであり、Boom の編集拡張機能に加えて、『Hexen: Beyond Heretic』で使用されている Doomエンジンのバージョンで作られたすべての拡張機能をサポートし、いくつかの新機能も追加されている。Doomの他にも、『Chex Quest』『Heretic』『Hexen: Beyond Heretic』『Strife: Quest for the Sigil』にも対応している。他の多くのソース移植とは異なり、ZDoomはIWADに収録されているイントロのデモを含め、バニラのDoomで記録されたデモをプレイすることはできない。2016年2月22日にZDoomの最終バージョンであるバージョン2.8.1が公開された。

2017年1月7日、ZDoomのウェブサイトの管理人「randi」はZDoomの開発終了を発表し\[8\]、代替としてQZDoomかGZDoomを推奨した\[9\]。

##### csDoom

csDoomまたはClient/Server Doomは、インターネット上でDoomのマルチプレイヤーゲームをプレイするために特別に構築されたZDoomをベースにしたソース移植。これは（QuakeWorldの）[クライアント/サーバーネットワークコードを使用する最初の移植であり](../Page/クライアントサーバモデル.md "wikilink")、プレイヤーはその場でDoomサーバーに参加できる\[10\]。プロジェクトは閉鎖され、そのソースは2001年初頭に作者によってGPLの下で公開された。それまでソースコードは非公開だった（QuakeWorldのGPLライセンスに違反していたため、作者はジョン・カーマックから公開を強いられた）。

##### GZDoom

GZDoomは、ZDoomをベースとしたソース移植であり、[OpenGL](../Page/OpenGL.md "wikilink") 3レンダラーを含むように機能セットを拡張している。2005年8月30日に公開された。GZDoomは、Doom LegacyおよびVavoomと互換性のある3Dフロアサポート、3Dモデルサポート、360度スカイボックスなどの機能を誇っている。バージョン2.4.0は、2017年3月19日のQZDoom 1.3.0のリリースと共にZDoom.orgで正式に公開された最初のバージョンであった\[11\]。

また、2019年に公開されたバージョン4.2.0は、日本語に対応している。 GZDoomの最新バージョンであるバージョン4.3.3は、2020年1月20日に公開された\[12\]。

##### GZ3Doom

GZ3Doomは、GZDoomをベースとしたソース移植であり、エンジンに[Oculus Riftサポートを追加しつつ](https://ja.wikipedia.org/wiki/Oculus_Rift "wikilink")、Doom、Doom II、HereticおよびHexenを引き続きサポートする\[13\]。

##### Odamex

Odamexは、Doomエンジンの無料クロスプラットフォームModであり、プレイヤーは簡単にDoomのオンラインプレイ専用サーバーに参加することができる\[14\]。Odamexの目標は、どんなプラットフォームでも誰でもプレイできる、競争力のあるオープンソースのDoom移植になることである。移植の強化点としては、オリジナルのDoomエンジンの物理切り替えや強化された物理でプレイ、32ビットカラーレンダラー、オンザフライでパッチWADをダウンロードしてインストールする機能、キャプチャー・ザ・フラッグとチームデスマッチモードの実装などがある。

##### SkulltagとZandronum

Skulltagは(G)ZDoomをベースにしたマルチプレイヤー中心のDoom移植の一つである\[15\]。32人のマルチプレイヤーとデスマッチやキャプチャー・ザ・フラッグなどの標準的モードのほか、協力プレイや侵略マップなどの様々なゲームモードが追加されている\[16\]。Skulltagは3Dモデルや高解像度テクスチャに対応する。Skulltagの最終バージョンが2010年11月7日にバージョン0.98dとして公開された。Skulltagは2012年6月7日に閉鎖された。

Skultag 98eは、原作者が別のプロジェクトに移った後、同じ開発者によって作られたZandronumに引き継がれた。Zandronumは2012年8月24日にバージョン1.0として初公開された。Zandronumはサーバーごとに最大64人のオンラインプレイヤーをサポートし、Skulltagでは以前はOpenGLのみの機能だった3Dフロア用のソフトウェアレンダリングを導入した。Zandronumの最新バージョンの3.0は2017年9月7日に公開された。

##### ZDaemon

ZDaemonはDoomのオンラインマルチプレイヤーソース移植である。プレイヤーはアカウントを作成し、付属のサーバーブラウザー（ZDaemon Launcher）を使用してマルチプレーヤーサーバーに簡単に接続できる。ZDaemonランチャーは、「ZRC」（ZDaemonリレーチャット）と呼ばれる独自のクライアントを介してZDaemonの[IRCチャネルにアクセスする機能も搭載している](../Page/Internet_Relay_Chat.md "wikilink")。2018年3月15日に最新バージョン1.10.01が公開された。なりすましを減らすために、バージョン1.09ではゲーム内のニックネーム認証が導入された。これにより、プレイヤーは別名（クランタグなど）を使用することができるが、実際にニックネームを所有している場合に限られる。ZDaemonは、有効になっているサーバーから経験値と同様に統計を収集する。これによりプレイヤーはプレイ中にレベルを上げることができるが、レベルを上げてもゲーム内のメリットはない。

#### Chocolate Doom

Chocolate Doomは、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、AmigaOS 4\[17\]、[MorphOS](https://ja.wikipedia.org/wiki/MorphOS "wikilink")およびその他の最近のオペレーティングシステム用のソース移植であり、オリジナルのDOS実行ファイル（「 [バニラ](https://ja.wikipedia.org/wiki/バニラ_\(ソフトウェア\) "wikilink") Doom」）に可能な限り近い動作をするように設計され、DOS実行ファイルで見つかったバグの複製やゲームを[クラッシュさせるバグさえもその対象となる](https://ja.wikipedia.org/wiki/クラッシュ_\(コンピュータ\) "wikilink")。これは、単にソースコードにバグを残すだけではない。DOS版に存在するいくつかのバグ（たとえば、[Doom IIの空のバグ](../Page/Doom_II.md "wikilink")）が公開されたDoomソースコードでは修正されたため、これらのバグはChocolate Doom用に再作成された。Chocolate Doomの最初のバージョンは2005年9月7日に公開された。 DOS実行ファイルにかぎりなく近い形で設計されているため、新しい機能はなく高解像度のサポートにも欠けている。ホストオペレーティングシステムの標準[MIDI](../Page/MIDI.md "wikilink")出力と同様にOPL3音楽エミュレーションをサポートしている。Chocolate Domは[ステージデザイナーや](../Page/Doomの改造.md "wikilink")、未改造のDoomを好むプレイヤーの間で人気を博しているテストエンジンである。デフォルトでは、[Windows 98で実行されているdoom](../Page/Microsoft_Windows_98.md "wikilink").exeバージョン1.9の動作をシミュレートするが、それぞれのIWADを検出した場合、The Ultimate Doomや[Final Doomの実行ファイルをシミュレートする](../Page/Final_Doom.md "wikilink")。Chocolate Doomの最新バージョンであるversion 3.0.0は、2017年12月30日に公開された。

#### Crispy Doom

Crispy DoomはChocolate Doomのフレンドリーフォークであり、より高いディスプレイ解像度を提供し、Doomエンジンの静的な制限を取り除き、オリジナルと完全に互換性のある構成ファイル、セーブゲーム、ネットプレイおよびデモを維持しながら、さらに視覚的、戦術的および物理的な拡張をオプションで提供している。

### BeOS

これはBeOSオペレーティングシステムと互換性のあるDoomの移植である。Doomが利用できるBeOSの詳細については脚注を参照のこと：[1](https://web.archive.org/web/20120402162838/http://www.doomworld.com/classicdoom/ports/index.php?platform=7)。

### Acorn RISC OS

Jeff DoggettがDoomのオープンソースRISC OS移植を開発した。この移植はDoom、Doom II、The Ultimate DoomおよびFreedoomのゲームファイルをサポートする。

### Amiga

[Amiga](../Page/Amiga.md "wikilink")コンピュータには、さまざまなバージョンのDoomがある。

  - ADoomは、IDのLinuxソースコードをベースとしたAmigaのネイティブ移植である\[18\]（68kおよびPPCバージョンが存在する\[19\]）。
  - DoomAttackは、別のAmigaのネイティブ移植（68k AGA/RTG）\[20\]。
  - v2.02（68k AGA）に基づくBOOM\[21\]
  - v1.22（68k AGA / RTG）に基づくZDOOM\[22\]
  - v0.64（68k AGA / RTG）に基づくODAMEX\[23\]

DoomのすべてのAmiga移植にはオリジナルのIWADが必要になる。

### OS X

ZandronumはMac OS X専用に設計されている。Doomsday、Odamex、PrBoomなどのソース移植はOS Xと互換性があるが、本来は可能な限り移植可能にすることを目的としたクロスプラットフォームプロジェクトである。

## ポータブル機器

### Nintendo DS

PrBoomの移植はニンテンドーDS用に書かれた。PWADとDEHパッチはサポートされているが、起動時にそれらをロードするための引数を持つ個別のファイルを作成することによってのみサポートされる。PCにセットアップしたPrBoomサーバーを使用する場合、Wi-Fiネットワークプレイに対応する\[24\]。

### Digita OS

DOOMDは、FlashPoint Technologyのデジタルカメラ用DigitaOS用に公開された移植版。この移植は、1997年に公開されたソースコードに直接基づいている。DoomとDoom IIの両方のIWADをサポートしており、カスタムWADもサポートしているが、選択インターフェースは実装されていない\[25\]\[26\]。

### iPod

ハックにより、第5世代のiPodでDoomの移植版を実行できた\[27\]。Rockboxの[Rockdoom](http://www.rockbox.org/wiki/PluginDoom)プラグイン（PrBoomベース）を実行しているiPodでDoomを実行することもできる。これには、対応デバイスにRockboxをインストールしてからRockdoomをインストールし、最後にゲームのWADファイルをコピーして実行する必要がある。これにより、RockboxがサポートするほぼすべてのデバイスでDoomを利用できるようになるが、実際の実装、制限された操作、デバイスのパワーおよび画面によってはDoomをプレイできなくなる可能性がある。

### Android

Android向けのDoomの移植がいくつか存在する。最も基本的なものの中で、AnDoomとDoom Touchが''オリジナルを忠実にエミュレートし\[28\]\[29\]、Doom GLESはOpenGL ESのアクセラレーションされたグラフィックスを提供する\[30\]。また、ネットワークマルチプレイを提供するPRBoomの移植版も利用できる\[31\]。ただし、この移植はPlayストアから削除されている。

### Sony Ericsson

Sedoomは、siedoom移植をベースとした[Sony Ericssonの携帯電話用のDoomエンジンのオープンソース移植である](../Page/ソニーモバイルコミュニケーションズ.md "wikilink")。すべての通常のIWADに対応し、カスタムWADの読み込みにも対応している\[32\]。

### Symbian

C2Doomという名前の移植がS60およびS80の電話機で動作するように作成された。Bluetoothを介して、最大4人プレイヤー用の協力プレイとデスマッチのマルチプレイに対応する\[33\]。

### ZuneとZune HD

OpenZDKを使用して[Zune](../Page/Zune.md "wikilink")デバイスで動作する2つの移植が公開された。1つはZune HD用で、もう1つは第3世代Zune以下用である\[34\]\[35\]。

### TI-Nspireシリーズ

[TI-Nspireグラフ計算機](https://ja.wikipedia.org/wiki/TI-Nspireシリーズ "wikilink")（具体的には[NDless脱獄ソフトウェア](https://ja.wikipedia.org/wiki/TI-Nspireシリーズ "wikilink")）用のソース移植「nDoom」が制作された。これはオリジナルのDoomエンジンの直接移植したものであり、結果としてオリジナルの実行ファイル用に設計されたすべてのIWADおよびPWADをサポートする。『Heretic：Shadow of the Serpent Riders』と『Hexen』のサポートが追加された\[36\]。

## その他の移植

これらのDoomソース移植は、Doomエンジンのソースコードをベースにしながらも[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")や[Adobe Flashなどの](../Page/Adobe_Flash.md "wikilink")[仮想マシン上で動作するという特徴がある](../Page/仮想機械.md "wikilink")。後者の性質上、これらの移植の中にはCコードの自動解析（Adobe Alchemyなど）の使用を選択したものもあるが、大幅な書き換えを採用したものもある。

### HTML5

Freedoomは、[Emscripten](https://ja.wikipedia.org/wiki/Emscripten "wikilink")およびasm.jsを介して「boon」という名前で[World Wide Webに移植されている](../Page/World_Wide_Web.md "wikilink")\[37\]\[38\]。

### Adobe Flash

ネイティブコードで直接実行されないDoomの最も有名なバージョンは、Adobe Alchemyと[ActionScript](../Page/ActionScript.md "wikilink")で書かれたDoom Triple Pack\[39\]である。これは基本的にオリジナルのCソースをコンパイル済みのAdobe Alchemy[バイトコード](../Page/バイトコード.md "wikilink")に直接変換したもので、最近のAdobe Flash Playerのバージョンで動作するようになっている。

### Java

過去に、JavaでDoomCott\[40\]やStark Engine\[41\]などのJavaでDoomソースポートを作成する試みがなされたが、放棄されたか適切にソース移植と呼べるほどの機能が得られず失敗に終わった。2010年時点で唯一アクティブなJava DoomプロジェクトはMocha Doom\[42\]であり、最新のDoomソース移植と同様の機能を持ち、オリジナルのゲームデータと直接互換性がある純粋なJava実装である。

### Python

2010年、 Doomは[SDL](../Page/SDL.md "wikilink")ライブラリを使用して[Python](../Page/Python.md "wikilink")スクリプト言語に「PyDoom」という名前で移植された\[43\]\[44\]。

### Doom 3 mod

プレイヤーがゲーム内端末を使用してオリジナルのDoomを実行できるようにする[Doom 3用modが制作された](https://ja.wikipedia.org/wiki/Doom_3 "wikilink")。「Terminal Doom」と呼ばれるこのMODは、1997年に公開されたソースコードをベースとして、Doom 3のインタラクティブ表面上の実験を構成している。発売されたDoomのすべての小売およびシェアウェアは、この移植版でサポートされている\[45\]\[46\]。

### Hewlett-Packard 16700シリーズロジックアナライザー

Doomは、 [PA-RISC](../Page/PA-RISC.md "wikilink")プラットフォーム上の[HP-UX](../Page/HP-UX.md "wikilink") 10.20に移植され、HP（後の[アジレント](../Page/アジレント・テクノロジー.md "wikilink")、現在の[キーサイト](https://ja.wikipedia.org/wiki/キーサイト・テクノロジー "wikilink")）の16700ファミリーのPA-RISCベースの[ロジックアナライザ](../Page/ロジックアナライザ.md "wikilink")にイースターエッグとして収録された\[47\]。

### VEX V5 Robot Brain

2018年、Doomはプログラミング言語「PROS」を使用してVEX Robotics V5 Brainに移植された\[48\]。

## 簡略化系図

次の図は、Doomソース移植の簡略化系図を示している。 [代替文=A simplified family tree of Doom source ports](https://ja.wikipedia.org/wiki/ファイル:Doom-ports.svg "wikilink")

## 脚注

## 外部リンク

  - [Doomworld -- ソース移植](https://www.doomworld.com/forum/6-source-ports/)（英語）
  - [Doomソース移植の系譜](http://www.doomworld.com/10years/ports/) （英語）
  - [Wayback Machineによる](../Page/インターネットアーカイブ.md "wikilink")[Nokiaの携帯電話移植](https://web.archive.org/web/20030210160355/http://www.wildpalm.co.uk/doom7650.html)（このページはもはや[WildpalmのWebサイト](http://www.wildpalm.co.uk)には存在しない）
  - [ZDoom、GZDoom、QZDoom](http://zdoom.org/)
  - [Zandronum](https://zandronum.com/)
  - [Doomsday](http://dengine.net/)
  - [Chocolate Doom](https://www.chocolate-doom.org/wiki/index.php/Chocolate_Doom)

<!-- end list -->

1.
2.
3.
4.  <http://gldoom.sourceforge.net/>
5.  <https://www.doomworld.com/idgames/themes/TeamTNT/boom/boom202s>
6.  [iPhone Doom Classic Progress Report](http://www.idsoftware.com/iphone-doom-classic-progress/)
7.  [dengine.net](http://dengine.net/) Doomsday Engine website: about, news, builds, wiki, forums.
8.
9.
10.
11. <https://forum.zdoom.org/viewtopic.php?t=55739>
12. <https://zdoom.org/news>
13.
14.
15.
16.
17.
18.
19.
20.
21. <http://aminet.net/package/game/shoot/BOOM>
22. <http://aminet.net/search?query=ZDOOM>
23. <http://aminet.net/search?query=odamex>
24.
25. [Dedicated Doom handheld hacked from an old digital camera](http://www.crunchgear.com/2010/03/01/dedicated-doom-handheld-hacked-from-an-old-digital-camera/)
26. <http://www.visi.com/~xevious/mamed/readmed.htm>
27. [Doom ported to the iPod - Engadget](https://www.engadget.com/2005/08/07/doom-ported-to-the-ipod/)
28. [Doom Touch at Play Store](https://play.google.com/store/apps/details?id=com.beloko.doom)
29. [AnDoom at Play Store](https://play.google.com/store/apps/details?id=com.bakateam.andoom&hl=en)
30. [Doom GLES Doom GLES at Play Store](https://play.google.com/store/apps/details?id=com.kokak.DoomGLES)
31. [PRBoom at Play Store](https://play.google.com/store/apps/details?id=com.bestapp.prboomdoom)
32. <http://forums.se-nse.net/topic/48785-sedoom/page__p__660601&#entry660601?s=d2d0541b799696fa7c878ed67c7c56a0>
33. [Doom for S60 and S80 Phones.](http://koti.mbnet.fi/mertama/downloads.html)
34. <http://www.zuneboards.com/forums/showthread.php?t=50582>
35. <http://www.zuneboards.com/forums/showthread.php?t=51403>
36. <http://tiplanet.org/forum/archives_voir.php?id=3889>
37. [Play Freedoom](https://kripken.github.io/boon/boon.html)
38. [Emscripten Demos](https://github.com/kripken/emscripten/wiki/Porting-Examples-and-Demos)
39. [Doom Triple Pack](http://www.newgrounds.com/portal/view/470460)
40. [Doomcott, with broken Java Applet.](http://java-emu.emuunlim.com/doomcott/doom.html)
41. [Stark engine, archived page.](https://web.archive.org/web/20021119165755/http://www.theintraclinic.com/stark/)
42. [Mocha Doom official Sourceforge project page](http://sourceforge.net/projects/mochadoom/)
43. [PyDoom on DoomWiki](https://doomwiki.org/wiki/PyDoom)
44. [PyDoom on Github](https://github.com/Pink-Silver/PyDoom)
45. <http://doom3.filefront.com/file/Terminal_DOOM_Demo;42285>
46. <http://battleteam.net/tech/fis/>
47. <http://www.perdrix.co.uk/hp16700/#mozTocId978366>
48. <https://github.com/sealj553/VexV5Doom>