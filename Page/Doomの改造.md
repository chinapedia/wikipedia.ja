> この記事は[Doomの改造](https://ja.wikipedia.org/wiki/Doomの改造)から翻訳されています。


**Doom WAD**（**ドゥーム ワッド**）は、[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")『[Doom](../Page/DOOM.md "wikilink")』とその続編『[Doom II：Hell on Earth](../Page/Doom_II.md "wikilink")』のパッケージファイルのデフォルト形式で、スプライト、ステージ、ゲームデータが含まれている。WADは、「*Where's All Data？（全てのデータはどこにある？）」の略である\[1\]。1993年の発売直後、『Doom』はステージ、グラフィック、他のゲームデータをパッケージ化したWADファイル用の独自の[MODを制作するプレイヤー達の大規模な支持を集め](../Page/Mod_\(コンピュータゲーム\).md "wikilink")、現在ではファーストパーソン・シューティングゲームでは一般的となっているMOD作成文化を生み出す上で重要な役割を果たした。*Doom''には、単一のカスタムステージから完全なオリジナルゲームまで、何千ものWADが作成されている。これらのほとんどは[インターネット](../Page/インターネット.md "wikilink")経由で自由にダウンロードが可能。いくつかのWADも[商業](../Page/商業.md "wikilink")的にリリースされており、一部の人々にとってWADを作る[趣味](https://ja.wikipedia.org/wiki/趣味 "wikilink")は、[レベルデザイナーとしての](https://ja.wikipedia.org/wiki/レベルデザイン "wikilink")[プロのキャリアへの入り口となった](../Page/専門職.md "wikilink")。

WADには、IWAD（内部WAD）とPWAD（パッチWAD）の2種類がある。IWADには、ゲームのロードに必要なデータが含まれているが、PWADには、カスタムステージの必要に応じて、新しいキャラクタースプライトなどの追加データが含まれている。

## 歴史

### Doomの拡張性

Doomを開発するにあたり、id Softwareは多くのプレイヤーが同社の過去作『Wolfenstein 3D』のカスタム[ステージやその他のModを作成しようとしたことを認識していた](../Page/ステージ_\(コンピュータゲーム\).md "wikilink")。ただし、そのゲーム用Modの作成とロードに関連する手順は面倒な作業だった。

id Softwareの主任プログラマーである[ジョン・カーマックは](https://ja.wikipedia.org/wiki/ジョン・D・カーマック "wikilink")、プレイヤーがゲームを拡張できるように、Doomの内部を一から設計した。そのため、ステージ、[グラフィック](../Page/グラフィック.md "wikilink")、[効果音](../Page/効果音.md "wikilink")、[音楽](../Page/音楽.md "wikilink")などのゲームデータは、[ゲームエンジン](../Page/ゲームエンジン.md "wikilink")とは別に「WADファイル」に保存される。これにより、プレーヤーはエンジンを変更せずに独自のデータを作成できた。Doomの初期設計文書によると、WADは「**W**here's **A**ll **D**ata？」の略である。

Doomを簡単に変更できるようにするアイデアは、[コピーレフト](../Page/コピーレフト.md "wikilink")の有名な支持者でお互いの作品を共有して構築する人々の[ハッカーの理想を支持していたカーマックと](../Page/ハッカー文化.md "wikilink")、若い頃にゲームをハッキングした経験があり、他のゲーマーにも同じことができるようにしたいと考えていたジョン・ロメロによって主に支持された。ただし、id Softwareのスタッフ全員がこの開発に満足していたわけではなく、ジェイ・ウィルバーやケヴィン・クラウドを含む一部の人々は、法的な懸念と、会社のビジネスに何の利益もないとの信念から反対した。

### ユーティリティとWADの登場

1993年12月10日にDoomの最初の[シェアウェア](../Page/シェアウェア.md "wikilink")がリリースされた直後に、愛好家はゲームを変更するためのさまざまなツールに取り組み始めた。1994年1月26日、ブレンドン・ワイバーはDoom Editing Utility（DEU）プログラムの最初の[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")バージョンをインターネットで公開した。これは、Doomファンによって作成されたプログラムで、まったく新しいステージを作成することを可能にした。DEUは同じ年の5月21日まで開発が続けられた。マット・フェルのUnofficial Doom仕様のリリースによって可能になった。その後まもなく、Doom愛好家はDEUのさらなる強化に関与するようになった。Raphaël Quinetがプログラム開発の取り組みとプロジェクト全体のリリースを主導し、Steve Baremanが文書化の取り組みとDEUチュートリアルの作成を主導した。30人以上の他の人々も努力を助け、彼らの名前はプログラム配布に含まれているREADME.1STファイルに表示されている。[Xを実行する](../Page/X_Window_System.md "wikilink")[Unixシステム用のDEU](../Page/UNIX.md "wikilink") 5.21のフォークであるYadexは、後に[GNU/GPLライセンスで公開された](../Page/GNU_General_Public_License.md "wikilink")\[2\]（カーマックはさらに、ゲームの制作に使用したユーティリティの[ソースコード](../Page/ソースコード.md "wikilink")を公開したが、これらは[NeXT](../Page/NeXT.md "wikilink")ワークステーション用の[Objective-C](../Page/Objective-C.md "wikilink")でプログラムされていたため、[PCユーザーであるほとんどの人には直接使用できなかった](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")）。

ジェフリー・バードは、1994年3月7日に『Origwad』というタイトルで公開されたDoomの最初のカスタムWADを作成したとされている。間もなく、無数の愛好家がカスタムWADを作成し、[AOL](../Page/AOL.md "wikilink")や[CompuServe](../Page/CompuServe.md "wikilink")フォーラム、その他のインターネットベースのチャネルで共有した。WADの多くは元のゲームのスタイルで作成され、その他は[TVシリーズ](../Page/テレビ番組.md "wikilink")、[映画](../Page/映画.md "wikilink")またはオリジナルのテーマをベースとしていた。id Softwareスタッフの一部はWADの一部に感銘を受けたことを明らかにしており、ジョン・カーマックは後に『[スター・ウォーズ](../Page/スター・ウォーズシリーズ.md "wikilink")』をテーマにしたModについて次のように述べた：

もう1つの特に注目すべき初期のModは、映画『[エイリアン2](../Page/エイリアン2.md "wikilink")』をベースとした『Aliens TC』（[\#トータルコンバージョン](https://ja.wikipedia.org/wiki/#トータルコンバージョン "wikilink")節を参照）である。

WADがグラフィックとオーディオを置き換えることによって『Doom』を変更したにもかかわらず、カスタマイズの量は多少制限されていた。武器や敵のタイミングや強さなど、ゲームの動作の多くは『Doom』の[実行ファイル](../Page/実行ファイル.md "wikilink")にハードコードされており、WADでは変更できない。グレッグ・ルイスによって制作されたDoom編集プログラム「[DeHackEd](../Page/DeHackEd.md "wikilink")」は、ユーザーがDoom実行ファイル内のパラメーターを変更できるようにすることで対応し、より高度なカスタマイズを可能にした。

### 商用WAD

1994年から1995年頃、WADは主に[電子掲示板](../Page/電子掲示板.md "wikilink")とパソコンショップやステージ制作の指示ガイドに同梱されたコレクション[CD経由で配布され](../Page/コンパクトディスク.md "wikilink")、後年には[インターネット](../Page/インターネット.md "wikilink")の[FTPサーバーでやりとりされるようになった](../Page/File_Transfer_Protocol.md "wikilink")。DoomソフトウェアのライセンスはカスタムWADから利益が得られないようにすることが必要であり、id SoftwareのメンバーはWADのコンピレーションCD-ROMの配給者に対して何らかの対策を講じていると主張しているが\[3\]、一部のWADセットと[ショベルウェア](https://ja.wikipedia.org/wiki/ショベルウェア "wikilink")バンドルはそれにも関わらず特定のアウトレットで有償で入手できた。

当時、id Softwareは新しい技術を使った新作『[Quake](../Page/Quake.md "wikilink")』に取り組んでいたが、Doomコミュニティから最も才能のあるWAD制作者を選び、公式拡張の制作と不正なコレクションCDに対抗するプロジェクトを開始した。チームは21の『[Master Levels](https://ja.wikipedia.org/wiki/:en:Master_Levels_for_Doom_II "wikilink")』を制作し、1995年12月26日にインターネットから任意にダウンロードされた1,830のWAD集である「Maximum Doom」とともにCDで発売された。1996年には、TeamTNTが制作した二つの32ステージのmegawad『[Final Doom](../Page/Final_Doom.md "wikilink")』が、id Softwareから正式な商品として発売された。

さらに、当時発売されたさまざまなファーストパーソン・シューティングゲームでは、id Softwareの商用ライセンスの下でDoomエンジンを使用していた。これは、本質的にDoomエンジンとパッケージ化されたカスタムWADである。1997年に発売された『Hacx：Twitch 'n Kill』がその例である。

商業的にリリースされたWADに貢献した多くの人々に加えて、さまざまな作者が他のゲームの開発に関与するようになった。

  - ケネス・スコット…『Hacx：Twitch 'n Kill』にアートワークを寄稿した後、id Softwareと[バンジー後に](../Page/バンジー_\(ゲーム会社\).md "wikilink")『[Halo](../Page/HALO_\(ビデオゲームシリーズ\).md "wikilink")』ゲームの開発を担う[343 Industriesでアートディレクターになった](https://ja.wikipedia.org/wiki/343_Industries "wikilink")。
  - 『Master Levels for Doom II』に 2つのステージを提供したティム・ウィリッツは、後にid Softwareの主任デザイナーになった。
  - 『Final Doom』を4分の1作成した[ダリオ・カザーリは](../Page/Final_Doom.md "wikilink")、[Valveに雇われて](../Page/Valve_Corporation.md "wikilink")『[Half-Life](../Page/ハーフライフ_\(ゲーム\).md "wikilink")』に取り組んだ。
  - Sverre Kvernmo…『Master Levels for Doom II』の5つのステージのデザイナーでTeamTNTのメンバー。Ion Stormに『[大刀](../Page/大刀_\(ゲーム\).md "wikilink")』のために雇われた。
  - Iikka Keränen…いくつかのDoom WADとそれ以降のQuake Modの作者。Ian Stormに雇われて『Anachronox』と『大刀』のステージを作成し、Looking Glass Studiosに『Thief II：The Metal Age』のステージを作成した。Keränenは後にバルブに雇われた。
  - ジョン・アンダーソン （レベルデザイナー）…「睡眠博士」としても知られる。『Master Levels for Doom II』の5つのステージと『The Ultimate Doom』のE4M7の作者であり、後に『Blood』『[Unreal](../Page/Unreal.md "wikilink")』および『大刀』に取り組んだ。
  - Matthias Worch （レベルデザイナー）は、Ritual Entertainmentに入社して『SiN』に取り組んだ。彼は後にUnrealシリーズに貢献した。

### ソースポート時代

1997年頃、id Softwareの『Quake』などより高度な技術とカスタマイズ性のあるデザインの新作ゲームに注目が集まるようになり、Doom WADへの関心は低下していった。

1997年12月23日、id SoftwareはDoomエンジンのソースコードを制限されたライセンスの元で公開し、1999年10月3日に[GNU General Public Licenseの条件下で再び公開した](../Page/GNU_General_Public_License.md "wikilink")。ソースコードが利用可能になると共にプログラマーがゲームのあらゆる面の修正、技術的制限及びバグの除去、全く新しい機能の追加を行えるようになった。

これらのエンジンのMod、つまりDoomソースポートは、それ以来WAD編集活動の多くの対象になっている（ただし、一部の純正主義者はオリジナルの無改造エンジンを好む）。2018年の時点で、いくつかのソースポートがまだ積極的に開発されており、Doomは未だにWADを作成する人々の根強い支持を維持している。

## WADの種類

### ステージとステージパック

WADの最も一般的なタイプは単一[ステージで構成され](../Page/ステージ_\(コンピュータゲーム\).md "wikilink")、通常はオリジナルのゲームのテーマを保持しているが、より特徴的な設定またはムードを定義するために新しい音楽といくつかの変更されたグラフィックスが含まれている場合がある。[シングルプレイヤーと](https://ja.wikipedia.org/wiki/シングルプレイヤーコンピュータゲーム "wikilink")[デスマッチ両方のマルチプレイヤーステージが一般的である](https://ja.wikipedia.org/wiki/デスマッチ_\(コンピュータゲーム\) "wikilink")。

また、いくつかのステージを含むWADも一般的であり、エピソードという扱いで9つのステージを置き換える場合もあれば、元のゲームの大半のステージを置き換えた「megawad」も存在する。

Megawadsは複数人で作られることが多く、開発期間も数か月から数年にわたる。

### トータルコンバージョン（Total conversion、TC）

単に新しいステージやグラフィックの変更を提供するのではなく、[ゲームの設定](../Page/キャンペーン_\(TRPG\).md "wikilink")、キャラクターセットおよびストーリーを全く異なるものにするためにゲームを[オーバーホール](https://ja.wikipedia.org/wiki/オーバーホール "wikilink")するWADは、「トータルコンバージョン（Total Conversion）」と呼ばれる。このフレーズは、『Ailens TC』（''Ailens Total Conversion）のタイトルの一部としてジャスティン・フィッシャーによって造語された\[4\]。オリジナルのゲームの特徴的な部分や特徴（キャラクターや武器など）を保持しながら同程度の広範な変更を提供するアドオンは、その延長線上で「部分改造（partial conversions）」と呼ばれることが多い。

## 有名なWAD

以下は、その選択において議論の余地がないと考えられる非常に人気のある、ユニークな、または歴史的に重要なWADの非包括的なリストである。代替リストとレビューサイトについては、以下の外部リンク項目を参照のこと。

### Megawad

  - 『10 Sectors』はDoomworldでの大会として始まり、参加者は10 sectorsのみを使用してBOOMソースポートにできる最高のステージを作るように挑戦され、勝者のMichal MeskoがVoodoo 5 5500 AGPグラフィックカードを受け取った。
  - 『Doom The Way id Did』…2012年に公開されたDoomの27ステージのmegawad。Jason "Hellbent" Rootによって最初に提案され、Doomworldコラボレーションプロジェクトとして実現した。megawadの目的は、オリジナルのゲームであったかのように見えて感じられるDoomステージの3つのエピソードを作成することであったが、それへのオマージュは一切なかった。32ステージの続編、『Doom II The Way id Did』が2013年に公開された\[5\]。さらに、2つのスピンオフが公開された。2016年に公開された『Doom The Way id Did: The Lost Episodes』には、『Doom the Way id Did』に提出されながらも最終版に入らなかったマップの6つのエピソードが収録されており、2016年に公開された『No End in Sight』は3人の『Doom the Way id Did』の寄稿者によって作成されたマップ（新規または『Doom the Way id Did』マップを変更したもの）の4つのエピソードを収録している。『Ultimate Doom The Way id Did』は、オリジナルのmegawadの9ステージのフォローアップエピソードであり、2019年に公開された。
  - 『Eternal Doom』…Team EternalとTeamTNTによって制作されたDoom II\[6\]の32ステージのmegawad。非商業的にいくつかのバージョンで公開され、最後のバージョンは1997年11月14日に公開された。Eternal Doomはプレーヤーとのテーマでさまざまなステージで、オリジナルのDoomモンスター配置し、[中世](../Page/中世.md "wikilink")の[城](../Page/城.md "wikilink")特色と未来的なハイテク拠点、[タイムトラベル](https://ja.wikipedia.org/wiki/タイムトラベル "wikilink")のサブプロットを特徴としている。Eternal Doomの特徴的な側面は、ステージのサイズであり、その平均はDoomおよびDoom IIのステージのサイズの約4倍である。Eternal Doomはステージの壮大な[建築](../Page/建築.md "wikilink")と複雑なレイアウトで高く評価されているが、一部の最大級の城の大きさとマップ内に配置されたスイッチ間をプレイヤーが行き来するよう強制するステージデザインも相まって見つけるのが困難な場合があり、批判の対象となっている。
  - 『Going Down』…2013年に公開されたDoom IIの32ステージのmegawad。イギリスのフリーランスアニメーターの[スィリアック・ハリス](https://ja.wikipedia.org/wiki/スィリアック・ハリス "wikilink")が制作した\[7\]。
  - 『Hell Revealed』…1997年5月2日に公開されたDoom IIの32ステージのmegawad。「Doom Done Quick speedrunning」プロジェクトのプレイヤーの1人、Yonatan DonnerとHaggay NIVによって制作された。Hell Revealedは、熟練プレーヤーにチャレンジを提供することを目的として設計され、その難易度の高さで有名になった：セット内の最も難しいステージは、プレーヤーが一度に数十の最も難しいモンスターと対戦するバトルグラウンドを備えている。一部のステージは合計で約500体のモンスターが登場する。Hell Revealedはオリジナルのゲーム『Doom』と『Doom II』に次いで、Doom WADの中で最もDoomのスピードランニング競争の対象とされてきた。同じコンセプトに基づいて構築され、さらに多くのモンスターを特徴とする32ステージの続編megawad『Hell Revealed II』が別のチームによって制作され、2003年12月31日に公開された。
  - 『Icarus: Alien Vanguard』：TeamTNTが制作した『DoomII』用の32ステージのmegawadで1996年3月22日に公開された。『TNT: Evilution』がid Softwareによって買収され、Final Doomパッケージの一部として発売される時、フリーウェアとして公開された。2003年に続編の『Daedalus: Alien Defense』が公開された。
  - 『Memento Mori』…The Innocent Crewの2人のメンバーであるDenisとThomas Möllerが、Tom Mustaineとダリオとミロのカザーリ兄弟を含む他の19人の作者と共に制作した『DoomII』の32ステージのmegawad。最初は1995年12月10日に公開され、1996年2月に更新版がリリースされた。続編となる32ステージのmegawad『Memento Mori II』が制作され、1996年7月27日に公開された。
  - 『Requiem』…以前に公開された『Memento Mori』シリーズに携わった同じ人々に加えて、このプロジェクトに特に取り組んだ2人の新しいマッパーによって制作された『DoomII』の32ステージのmegawad。1997年7月4日に公開され、idgamesアーカイブにアップロードされた。
  - 『Sigil』…ジョン・ロメロが制作したオリジナルの『Doom』の9ステージのエピソード。2018年12月10日に発表され、2019年5月に公開された\[8\]\[9\]。

### トータルコンバージョン

  - 『Action Doom 2：Urban Brawl』…[セルシェーディングされたグラフィックを特徴とするZDoomソースポートで開発された](../Page/トゥーンレンダリング.md "wikilink")2008年の[インディーゲーム](../Page/同人ゲーム.md "wikilink")。
  - 『Aliens TC』…ジャスティン・フィッシャーが制作し、1994年11月3日に公開した11ステージのTC。同TCは映画『[エイリアン2](../Page/エイリアン2.md "wikilink")』（1986）を題材としており、最初期のTCであると同時に最も有名なものの一つである\[10\]\[11\]。『[Doom II：Hell on Earth](../Page/Doom_II.md "wikilink")』の発売翌週に『Doom』の[ニュースグループ](../Page/ニュースグループ.md "wikilink")では同作よりもAilens TCに関連した話題が多かった。Aliens TCの人気はDoomコミュニティの外にも及んでおり、たとえば1998年のDreamWorksのPCゲーム『[Jurassic Park：Trespasser](https://ja.wikipedia.org/wiki/Trespasser_\(ゲーム\) "wikilink")』にインスピレーションを与えている。フィッシャーはさまざまなゲーム開発者（後にJurassic Park: Trespasserを制作するチームへのDreamWorksの勧誘も含む）に雇用をオファーされたが、大学の学位を取得するために辞退した。Ailiens TCはその不穏な雰囲気で有名であった。最初のステージ（E2M1）には敵がいない。これは、Doomのテンポの速いアクションを考慮した驚くべき機能である。しかし、その後プレーヤーは[エイリアンと対峙し](../Page/エイリアン_\(架空の生物\).md "wikilink")、『エイリアン2』のパワーローダーを武器として入手する。オリジナルWADは、初代Doom向けに作られたもので第二エピソード全体を1986年の映画をほぼ踏襲したステージに置き換え、シークレットステージのE2M9は『エイリアン』の宇宙船である。TCのボーナスレベルは、E3M1（オリジナルのデザインが大きすぎたため、E2M5マップからカットされた部分）とE3M2（E2M1のバリエーションであるが、敵が追加されたもの）である。マップE2M5とE3M1は、より直線的な他のステージとは対照的に、より多くのデスマッチ（近接センサーを使用）用に設計されている。ファンはDoom IIにこのWADを取り入れている。フィッシャーは1993年12月下旬にDoomをプレイしてから最初の5分以内にAliens TCを作成するというアイデアを得て、Doomと映画の雰囲気が似ていることに気付いた。ちなみに、id Softwareは当初DoomをAliensライセンスに基づいて計画する予定だったが、開発の初期段階ではそのアイデアを放棄したことが後で知られるようになった。
  - 『Ashes 2063』…Modder Vostyokが作成したTC。80年代の[ポストアポカリプス](https://ja.wikipedia.org/wiki/ポストアポカリプス "wikilink")映画に影響を受けた内容となっており、オリジナルのサウンドトラックを特徴としている\[12\]。
  - 『Batman Doom』…ACE Team Softwareによって制作され、1999年4月に公開された32ステージのトータルコンバージョン。[バットマンを題材としており](../Page/バットマン_\(架空の人物\).md "wikilink")、武器等も同作に準拠している。
  - 『Bloom』…『Doom』と『Blood』を組み合わせた内容のTCで、Bloom Teamが開発した。2019年のMOD DBのエディターズチョイスのクロスオーバー部門に選ばれた\[13\]。
  - 『[Chex Quest](https://ja.wikipedia.org/wiki/Chex_Quest "wikilink")』…1996年にDigital cafeが制作した全5ステージのTCで、ChexというシリアルのおまけのCDとして頒布された。同製品の販売終了後に[インターネット](../Page/インターネット.md "wikilink")上で[フリーウェア](../Page/フリーウェア.md "wikilink")として公開された。前述の経緯から子どもでも遊べるよう暴力表現や難易度を抑えた内容となっている\[14\]。続編に『Chex Quest 2：Flemoids Take Chextropolis』（1997年）と『Chex Quest 3』（2008年）があり、どちらも5つのステージを収録し、フリーウェアとして公開された。また、2020年5月にはリメイク版である『Chex Quest HD』が[Steam](../Page/Steam.md "wikilink")を通じて無料配信された\[15\]。
  - 『Doom 64 TC』…[NINTENDO64](../Page/NINTENDO64.md "wikilink")用に発売された『[Doom 64](https://ja.wikipedia.org/wiki/DOOM#DOOM "wikilink")』の複製であり、ゲームをベースとして異なるステージ、グラフィックス、およびオーディオを収録している。
  - 『Goldeneye Doom 2』…[NINTENDO64](../Page/NINTENDO64.md "wikilink")ゲーム『[ゴールデンアイ 007](../Page/ゴールデンアイ_007.md "wikilink")』の要素を追加するDoom IIのMod。
  - 『[Grezzo 2](../Page/Grezzo_2.md "wikilink")』は、イタリアのニコラ・ピロが2012年に開発したTCで、他のゲームやDoom Modの盗用や下品で[冒涜](../Page/冒涜.md "wikilink")的なコンテンツで有名である\[16\]\[17\]。
  - 『Hacx：Twitch 'n Kill』…1997年9月16日にBanjo SoftwareによってDoom IIの市販アドオンとして発売され、その後2000年にフリーウェアとして公開された。2010年10月9日、スタンドアロン版のバージョン1.2がリリースされた。Hacxには、21の新しいステージ、新しい武器、新しい音楽、新しい効果音、新しいグラフィックス、新しい敵など、まったく新しいコンテンツが収録されている。ゲームの動作は、独自のサイバネティックサイエンスフィクションの設定を考慮して大幅に変更されている\[18\]。
  - 『Paranoid』…『[Half-Life](../Page/ハーフライフ_\(ゲーム\).md "wikilink")』を忠実に再現することを目的とした8ステージのDoom IIのMod（GZDoomソースポートを使用）。新しい武器、敵、グラフィック、サウンド、モデル、空、3Dアーキテクチャ、ハブ構造、ストーリー主導のミッションおよび追加機能を搭載している。
  - 『Sonic Robo Blast 2』…Doom Legacyソースポートを使用して、ゲームを一人称シューティングゲームから『[ソニック・ザ・ヘッジホッグ](https://ja.wikipedia.org/wiki/ソニック・ザ・ヘッジホッグ "wikilink")』に基づく三人称プラットフォーマーに変更するDoomのMod。
  - 『Darkest Hour』…7ステージのDoom IIのModで、『[スター・ウォーズ](../Page/スター・ウォーズシリーズ.md "wikilink")』を題材としている。その後に、5ステージの「前日譚」の『*Dawn：A Prelude* 』が公開された。
  - 『Void』…2000年のゲーム『[アリス イン ナイトメア](../Page/アリス_イン_ナイトメア.md "wikilink")』に基づいたシングルステージのMod。

### その他

[右](https://ja.wikipedia.org/wiki/ファイル:Freedoom_0.11.3.png "wikilink")

  - 『[Brutal Doom](../Page/Brutal_Doom.md "wikilink")』…ブラジルのMod制作者のMarcos Abenante（通称：Sergeant_Mark_IV）が制作したMOD。オリジナル版よりもさらに過激な暴力表現で知られている\[19\]。
  - 『Doomsday of UAC』（ファイル名に倣ってUAC_DEAD.WADとも知られている）…1994年6月23日に公開されたレオ・マーティン・リムによるWADで、当時の最も現実的な環境の1つと考えられていたものを特徴としている\[20\]。Doomエンジンのレンダリングコードのそれまで未知のバグを利用して、「目に見えない階段」の形で特殊効果も導入した。後にこのトリックは広く使用されている。『Ultimate Doom』では、ボスが殺された後に部屋から脱出できるようにしたマップが依存していたタグ666の動作が変更されたため、このマップをプレイできなくなった。結果として生じた変更はバロン・オブ・ヘルのみが行動を引き起こすことができるように行われたので、この変更はステージを壊し、その結果、レッドキーを得るためにサイバーデーモンを殺さなければならない部分を進めることは不可能になった。最近のほとんどのソースポートでは、マップを適切にプレイできる。
  - 『D！Zone』（WizardWorks作）…DoomおよびDoom IIの何百ものステージを備えた拡張パック。同パックは、1995年に[ドラゴン誌の](https://ja.wikipedia.org/wiki/ドラゴン_\(雑誌\) "wikilink")217号のコラム「Eye of the Monitor」のコラムでJay＆Deeによってレビューされた。ジェイはパックに5つ星のうち1つを与え、ディーはパックに1.5星を与えた\[21\]。
  - 『Origwad』…ジェフリー・バードが制作し、1994年3月7日に公開され、Doom用にリリースされた最初のカスタムWADとして有名である。Origwadは2つの部屋が1つのドアで区切られた1つのステージで構成されている。最初の部屋にはショットガンとショットガンガイが含まれ、2番目の部屋には3体のインプ、2体のバロン・オブ・ヘル、および出口スイッチが存在する。

<!-- end list -->

  - 『Harris levels』 - [コロンバイン高校銃乱射事件](../Page/コロンバイン高校銃乱射事件.md "wikilink")の2人の犯人の1人エリック・ハリスが制作したDoomおよびDoom IIステージ群。
  - 『Sky May Be』…ジョークWAD。セクターが非常に広く、多くのテクスチャが単色に置き換えられ、多くのサウンドがイギリスのテレビ番組の音声に置き換えられている\[22\]。このWADはDoomworldのTop 10 Infamous WADsリストに記載されており、これまでに制作された最悪のWADの1つと見なされることもある。
  - 『UAC Military Nightmare』 –Doomシリーズのポートエンジンの一種であるskulltag用のWADで、テリーという人物が作成した。下品なスクリプトや奇妙なグラフィック、理不尽な難易度に加え、WADのファイルサイズを肥大化させたり、プレーヤーの設定を改ざんするなどといったトラブルで知られている。これらの問題を受け、WAD自体は2014年にDoomworldから削除された後、当該データが削除された状態で再アップロードされた。

#### Freedoom

Freedoomは、Doomで使用される[グラフィックス](../Page/コンピュータグラフィックス.md "wikilink")、[音楽](../Page/音楽.md "wikilink")、[サウンドエフェクトおよび](../Page/効果音.md "wikilink")[レベル](../Page/ステージ_\(コンピュータゲーム\).md "wikilink") （およびその他のその他のリソース）のセットの[無料代替](../Page/フリーソフトウェア.md "wikilink")（修正された[BSDライセンス](../Page/BSDライセンス.md "wikilink")）を作成することを目的としたプロジェクト\[23\]\[24\]。Doomエンジンは[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であるため、新しいリソースと一緒に配布でき、事実上、無料の完全なゲームを提供する。Freedoomを使用すると、ユーザーは通常元のゲームを必要とする他の何千ものWADをプレイできる。

Freedoomという名前の2つのシングルプレイヤーキャンペーン『Freedom: Phase 1』と『Freedom: Phase 2』とデスマッチステージ集を収録している\[25\]。

Freedoomは実行にソースポートを必要とせず、Doomの制限を排除した任意のソースポートで実行できる。ホームページ<https://freedoom.github.io/>からダウンロードできる。

同様のプロジェクト「Blasphemer」は、『Heretic』の完全無料版を制作することを目的としているが、Freedoomよりも完全には開発されていない\[26\]。

## レベルエディタ

Doomには多くの[レベルエディタが用意されている](../Page/ステージ_\(コンピュータゲーム\).md "wikilink")。オリジナルのDoom Editing Utility（DEU）は多くの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に移植されたが、時間の経過とともに重要性を失った。DETH、DeePsea、Linux Doom Editor、Yadexなど、多くの最新のDoomエディターは、DEUとその編集パラダイムにルーツを持っている。その他のレベルエディタには、WadAuthor、Doom Builder（2003年1月公開）、Doom Builder 2（2009年5月にDoom Builderの後継として公開）が含まれる。Doom BuilderやDoom Builder 2などの一部のDoomレベルエディタは、3D編集モードを備えている。現在、これら2つは廃止されているが、「GZDoom Builder」と呼ばれる新しいフォークがリリースされ、定期的に更新されている。

グラフィックやオーディオの塊を修正するために、他にも多くの特殊なDoomエディタが作成された。特に、XWE、SLADE、Wintex、SLumpEdなどです。モンスターやアイテムなどの物体および武器の動作も、実行可能なパッチユーティリティ[DeHackEd](../Page/DeHackEd.md "wikilink")を使用してある程度変更できる。ZDoomでは、ユーザーはDECORATEと呼ばれるスクリプト言語を通じて新しいモンスター、武器、アイテムを作成できる。これは、新しいオブジェクトを追加できない、オリジナルの武器とモンスターの動作から大きく逸脱できないなど、DeHackEdの多くの欠点を解決するために作成されたものである。

ユーティリティSligeを使用して、ランダムステージを自動的に生成できる。しかし、Sligeはマップを作成するときに面倒なアプローチをとっていたため、Obligeと呼ばれる新しいツールが作成された。このツールは完全に[Lua](../Page/Lua.md "wikilink")でコーディングされている。

## WAD2およびWAD3

Quakeでは、WADファイルは[PAKファイルに置き換えられた](https://ja.wikipedia.org/wiki/ファイルフォーマット一覧 "wikilink")。WADファイルはQuakeファイルに残るが、それらの使用はテクスチャに限定される。WAD2とWAD3は少し大きいディレクトリ構造を使用しているため、Doomと互換性がない。

## 注記

  - Joseph Bell、David Skrede： *Doom Construction Kit：Mastering and Modifying Doom*、Waite Group Press（1995年4月1日）、
  - リチャードH. "ハンク"ロイカートIII： *ドゥームハッカーガイド*、ミスプレス（1995年3月1日）、
  - Steve Benner、et al .: *Doom、Doom II、Heretic and Hexenの3Dゲーム錬金術*、SAMS Publishing（1996）、
  - Kushner、David： *Masters of Doom：How Two Guys Guys an Empire and Transformed Pop Culture*、Random House Publishing Group 2003、 ; 166〜169ページ
  - Larsen、Henrik： *The Unofficial Master Levels for Doom II FAQ*、version 1.02（2004年10月4日取得）

## 脚注

## 参考文献

  - ザック、ロバート（2018年12月）。["Doomを改造するための究極のガイド"](https://www.techradar.com/how-to/the-ultimate-guide-to-modding-doom) *TechRadar*
  - アンディハミルトン（2018年12月） [「Doomのカルト：idのクラシックの背後にある繁栄するmodシーン」](https://www.pcgamer.com/the-cult-of-doom-the-thriving-mod-scene-behind-ids-classic/) *[PCゲーマー](https://ja.wikipedia.org/wiki/PC_Gamer "wikilink")*

## 外部リンク

  - [Doomworld：史上最高の100 WAD](http://www.doomworld.com/10years/bestwads/) （2004年12月6日取得）
  - [Freedoomホームページ](https://freedoom.github.io/)

[Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink") [Category:Doom_(フランチャイズ)](https://ja.wikipedia.org/wiki/Category:Doom_\(フランチャイズ\) "wikilink")

1.
2.  [Yadex's Homepage](http://www.teaser.fr/~amajorel/yadex/)
3.
4.
5.  <http://www.doomworld.com/idgames/?file=levels/doom2/megawads/d2twid.zip>
6.
7.
8.
9.
10.
11. [Doomworld - The Top 100 WADs Of All Time: 1994](http://www.doomworld.com/10years/bestwads/1994.php)
12.
13.
14.
15.
16.
17.
18. [hacx](http://drnostromo.com/hacx/) on drnostromo.com
19.
20. [Doomworld - The Top 100 WADs Of All Time: 1994](http://www.doomworld.com/10years/bestwads/1994.php)
21.
22.
23.
24.
25.
26. [Blasphemer homepage](http://www.jeshimoth.com/jutegyte/blasphemer/)