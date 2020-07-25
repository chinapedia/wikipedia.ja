> この記事は[3DMark](https://ja.wikipedia.org/wiki/3DMark)から翻訳されています。


**3DMark**（スリーディーマーク）は、[フィンランド](../Page/フィンランド.md "wikilink")の[Futuremark](https://ja.wikipedia.org/wiki/Futuremark "wikilink")、その後のUL Benchmarksが開発する、[Microsoft Windows上で動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ベンチマーク](../Page/ベンチマーク.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")を用いた[3Dの性能を測るベンチマークソフトでは](../Page/3次元コンピュータグラフィックス.md "wikilink")[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")に位置づけられており\[1\]、[ゲーマー](../Page/ゲーマー.md "wikilink")を中心とした利用者から支持を得ている。

## 概要

本[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")は設定変更機能が制限されている「フリー版」と、規定の料金を支払い様々な機能を利用して性能を測る「プロフェッショナル版」などのラインアップがある。

計測には常に最新技術の機能が用いられているため、各バージョンがリリースされた時期の主要な[ビデオカード](../Page/ビデオカード.md "wikilink")を用いて計測すると負荷は非常に高い。言い換えると、最新バージョンでも快適に動く環境の場合では、同時期に主要となっているグラフィック機能を快適に利用することができるため、その指針ともなる。

2013年11月8日には3DMarkの15周年を記念する形で、過去のバージョンが無料公開された\[2\]。2019年1月現在、サポートの切れた『3DMark Vantage』や『3DMark 06』以前のバージョン（の、それぞれの最終版）が、フルバージョンのレジストキー付きで無料公開されている\[3\]。これらの旧バージョンは新しいPCでは意味あるベンチマーク結果を返さないため、あくまでレガシーPC向けとされている。

## 起源

もともとは、フィンランドの[メガデモ](../Page/デモシーン.md "wikilink")（ストーリー性のあるグラフィックを使ったデモプログラム）を手がけた**[Future Crew](https://ja.wikipedia.org/wiki/Future_Crew "wikilink")**のメンバーによって設立されたソフト会社、**[Remedy Entertainment](https://ja.wikipedia.org/wiki/Remedy_Entertainment "wikilink")**によるベンチマークソフト、『**[Final Reality](https://ja.wikipedia.org/wiki/Final_Reality "wikilink")**』が3DMarkの起源になっている\[4\]\[5\]。

これは同社で開発していた3Dゲームソフト**[MAX PAYNE](https://ja.wikipedia.org/wiki/MAX_PAYNE "wikilink")**用に作られた3Dエンジンである**[MAX-FX](https://ja.wikipedia.org/wiki/MAX-FX "wikilink")**を使ったもので、[DirectX5を利用していた](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")。当時はまだ「専用の3Dグラフィックカードを用いた方が3Dゲームに適している」と言われていたが、この時期に登場した、[NVIDIA](../Page/NVIDIA.md "wikilink")の[RIVA 128などのDirectXをサポートする汎用グラフィックチップによって](https://ja.wikipedia.org/wiki/RIVA "wikilink")、DirectXが3Dゲームにも適していることを証明する一助ともなった。

## SystemInfo

3DMarkではPCの環境を判断する『SystemInfo』というツールが使われている。一部ビデオカード（ドライバ）やCPUなどの想定外の環境では起動しない可能性もあるが、この場合は「-nosysteminfo」というパラメータを起動時に付けることでSystemInfoの段階をスキップでき、起動阻害を回避できる場合がある。SystemInfoは独自にアップデートすることもできるため最新版を使うことが推奨されるが、Windows XP SP2以前のレガシー環境では4.28以前のバージョンまでしか対応していないので、それを使うことになっている\[6\]。

## 各バージョン

### 3DMark99

Final Realityの成功により、RemedyではMAX-FXおよびMAX PAYNEの宣伝のためベンチマーク制作グループをFuturemark社として独立させた。そして[1999年](../Page/1999年.md "wikilink")に同社が最初に発表したのが3DMark99である。これはMAX-FXをDirectX6に対応させ、デモだけでなくベンチマーク用として計測できる機能を追加したものになっている。

その後、DirectX 6.1に対応した**3DMark99 MAX**をリリースしている。これは、新たに搭載された[SSEならびに](../Page/ストリーミングSIMD拡張命令.md "wikilink")[3DNow\!](../Page/3DNow!.md "wikilink")対応部分を加えることで、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") [Pentium IIIプロセッサや](../Page/Pentium_III.md "wikilink")[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") [K6-2](https://ja.wikipedia.org/wiki/K6-2 "wikilink")プロセッサの優位性を示すことが可能となっている。

ゲームを模したテストは次の通り。

  - Race
    近未来的なレース場を舞台にした、車輪の無い浮遊するマシンによる[レースゲーム](../Page/レースゲーム.md "wikilink")を模したテスト。
  - First Person
    建物内部に浮遊するメカを撃墜する、[ファーストパーソン・シューティングゲーム](../Page/ファーストパーソン・シューティングゲーム.md "wikilink")を模したテスト。

### 3DMark2000

社名を**MadOnion.com**と改めて発表した最初のソフトである。DirectX7に対応し、[ハードウェアT\&L](https://ja.wikipedia.org/wiki/ハードウェアT&L "wikilink")による描画が可能になったMAX-FXエンジンを使っている。ベンチマーク項目でもハードウェアT\&LとソフトウェアT\&Lを選択できるようになっている。また[MMX](../Page/MMX.md "wikilink")が必須条件となり、MMX非搭載CPUでは動作しなくなってしまった。バージョン1.1のアップデートではWindows 2000にも正式対応するようになった。アップデートによるベンチマーク結果の変動は3パーセント程度だったという\[7\]。

デモのストーリーも長くなり、ある程度一貫性の取れたものへと変わっている。特に映画『[マトリックス](../Page/マトリックス_\(映画\).md "wikilink")』に影響されたシーンが含まれているのが特徴的である。

この当時、NVIDIA社から[GeForce 256が登場し](https://ja.wikipedia.org/wiki/GeForce "wikilink")、搭載されるハードウェアT\&L機能のためのデモとして利用された。

ゲームを模したテストは次の通り。

  - Helicopter
    山岳地帯が描かれ、[攻撃ヘリコプター](../Page/攻撃ヘリコプター.md "wikilink")による戦闘が描かれる。
  - Adventure
    港のある中世の町並が描かれる。ディテールが高くなるにつれて通行人や帆船の数が増える。

### 3DMark2001

DirectX8に対応したベンチマークソフトである。新たに[バーテックスシェーダ](https://ja.wikipedia.org/wiki/バーテックスシェーダ "wikilink")、[ピクセルシェーダ](https://ja.wikipedia.org/wiki/ピクセルシェーダ "wikilink")用のベンチマークが加わっている。

前作同様、『マトリックス』のパロディ\[8\]のアクションシーンがデモに加わっており、主人公の顔が元[F1チャンピオンの](../Page/フォーミュラ1.md "wikilink")[ミカ・ハッキネン](../Page/ミカ・ハッキネン.md "wikilink")そっくりであった。

この製品をもってMAX-FXエンジンは完成の域に達し、これを元に[MAX PAYNEがRemedyよりリリースされた](https://ja.wikipedia.org/wiki/MAX_PAYNE "wikilink")。それと同時にMadOnion.comの役目は終わったが、社名をFuturemarkに戻した後、独自の3Dエンジンを用いたベンチマークソフトの開発を行うこととなった。

ゲームを模したテストは次の通り。

  - Car Chase
    近未来風の世界で、車輪の大きなオフロードカーのアクションが描かれる。
  - Dragothic
    女性を載せた巨大なドラゴンが、中世の町並を飛びまわる。
  - Lobby
    サングラスをかけた黒いロングコートの男が、ギャング風の黒服相手に、建物のロビーで銃撃戦を行う。
  - Nature
    蝶が飛び回り、木々や水面が風にゆらめくなど、大自然の様子が描かれる。

### 3DMark03

DirectX9.0に対応した独自エンジンによるベンチマークソフトである。

リリースされた当時はハイエンドのビデオカードでも比較的重く、ゲーム用ではない3Dエンジンを使ったため、各界から「ゲーム用としての性能を試す正当なベンチマークではない」との批判を受けた。シリーズの成功により影響力が大きくなり「特定のメーカーのグラフィックチップに特化したものではないか」といった種々の問題が生まれた。しかしながら、それを超えるベンチマークが存在しなかったため、引き続きスタンダードとして用いられることが多かった。

デモ内容は[シェーダモデル](https://ja.wikipedia.org/wiki/シェーダモデル "wikilink")1.4および2.0に対応したもので、4つのショートストーリーごとに異なるテストを行っている。それぞれのストーリーもさらに長く見ごたえのあるものになり、店頭デモとしても活躍するようになった。さらに、音楽もプロのミュージシャンを採用することで臨場感を広げている。

ゲームを模したテストは次の通り\[9\]。

  - Wings of Fury
    プロペラ戦闘機の空中戦を描いた[フライトシミュレータ相当のテスト](../Page/フライトシミュレーション.md "wikilink")。最後はウシのいる牧場も描かれる。DirectX7相当の機能とバーテックスシェーダ1.1を使用。
  - Battle of Proxycon
    宇宙船の内部での銃撃戦を描くファーストパーソン・シューティングゲーム相当のテスト。DirectX8のバーテックスシェーダ1.1とピクセルシェーダ1.1または1.4を使用。
  - Troll's Lair
    剣を持った女性が、隠し部屋の[トロールの住処に乗り込んで戦う](https://ja.wikipedia.org/wiki/トロール_\(トールキン\) "wikilink")、[ロールプレイングゲーム](../Page/ロールプレイングゲーム.md "wikilink")相当のテスト。DirectX8のバーテックスシェーダ1.1とピクセルシェーダ1.1または1.4を使用。
  - Mother Nature
    3DMark2001のNatureをさらに発展させた、大自然の風景を描くテスト。DirectX9の機能であるピクセルシェーダ2.0とバーテックスシェーダ2.0を使用。

### 3DMark05

リリースは[2005年](../Page/2005年.md "wikilink")。シェーダモデル2.0準拠のベンチプログラムである。フリーダウンロード版の構成は次の通り。

  - Return to Proxycon
    ファーストパーソン・シューティングゲームを模したベンチマーク。兵士の銃撃戦を描画。前作Battle of Proxyconの続編で、今度は宇宙海賊らしき相手と戦う\[10\]。
  - Firefly Forest
    [アドベンチャーゲーム](../Page/アドベンチャーゲーム.md "wikilink")及び[アクションゲーム](../Page/アクションゲーム.md "wikilink")を模したベンチマーク。森林を行く蛍1匹の光と、それに反映される影などを描画。
  - Canyon Flight
    レースゲームを模したベンチマーク。飛行船と竜のような巨大生物を描画。

デモ内容はさらに濃厚なストーリ性を持ち非常に見ごたえのあるものになっている。さらにエンドロールでは、フィンランドのバンド**Poets of the fall**([en](https://ja.wikipedia.org/wiki/:en:Poets_of_the_Fall "wikilink"))の『**lift**([en](https://ja.wikipedia.org/wiki/:en:Lift_%28Poets_of_the_Fall_song%29 "wikilink"))』を採用していることも注目された。

### 3DMark06

リリースは[2006年](../Page/2006年.md "wikilink")。シェーダーモデル3.0準拠、[マルチコア](../Page/マルチコア.md "wikilink")CPU対応などで構成されている。

3DMark05に含まれる3つのテストがシェーダモデル3.0による描画に変更された上で収録されており、より複雑なモデルを描画使用することで処理が重くなっている（**Firefly Forest**の蛍が2匹になっている、など）。

デモは3DMark05のテストをブラッシュアップしたものと、新たに追加された下記のテストである。

  - Deep Freeze
    南極基地の風景を模したベンチマーク。他のテストとは異なり、画面上を動き回るもの（生物や乗り物など）が存在しない。吹雪の中にたたずむ建物と時間経過によって変わる日の光を写実的に描画している。
  - Red Valley
    2つの陣営に分かれて戦う戦車を模したベンチマーク。各陣営の戦車のAIを別のスレッドで動かすためマルチコアCPUではスコアが上昇する。CPU用のテストであり、グラフィックカードの影響を抑えるため、[フレームレート](../Page/フレームレート.md "wikilink")の上限は2fpsに抑えられている。

### 3DMark Vantage

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")リリース。DirectX10及びシェーダーモデル4.0に対応しており、これを搭載する[Windows Vista以降の](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")[OS対応となっている](../Page/オペレーティングシステム.md "wikilink")。[64ビット](../Page/64ビット.md "wikilink")版にも対応している。それ以前のバージョンには対応しておらず、[Windows XPでは動作しない](../Page/Microsoft_Windows_XP.md "wikilink")。

なお、最初のリリースであるBuild 1.0.0が日本時間2008年4月に公開されたが、いくつかの問題があったため、それらを修正したBuild 1.0.1が同年5月22日と6月2日に公開された。その後[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[2月11日](../Page/2月11日.md "wikilink")に1.02が公開され、2011年[3月15日](../Page/3月15日.md "wikilink")には「Build」から「Version」へと表記変更が成された上でVersion 1.1.0が公開されている。

当初「Trial Edition」（体験版）として配布された無料版は1度しか実行出来ないという制約が設けられていたが、後発の3DMark11の公開後に発表されたVersion1.1.0からは、実行回数無制限の「Basic Edition」へと切り替えられている。

リリース時期に前後にして登場しているマルチコアCPUやマルチGPU、さらに物理演算エンジンである[PhysX](../Page/PhysX.md "wikilink")プロセッサの登場によって性能の差が大きく広がったため、パソコンの性能に合わせた4種類の[プリセット](https://ja.wikipedia.org/wiki/プリセット "wikilink")パターンを用意している。この内1.0.2以前のbuildにおいて、体験版で起動できたのはPerformanceが1度のみである。

  - Entry
    ローエンドクラスのグラフィックカードを対象。128MB以上のグラフィックメモリ、1024×768ドットのディスプレイ解像度が求められる。
  - Performance
    ミドルクラスのグラフィックカードを対象。256MB以上のグラフィックメモリ、1280×1024ドットのディスプレイ解像度が求められる。
  - High
    ハイエンドクラスのグラフィックカードを対象。512MB以上のグラフィックメモリ、1680×1050ドットのディスプレイ解像度が求められる。
  - Extreme
    最上級のグラフィックカードを対象。512MB以上のグラフィックメモリ、1920×1200ドットのディスプレイ解像度が求められる。

デモとしては、下記の4種類が行われる。

  - Jane Nash
    ゲーム『[トゥームレイダー](../Page/トゥームレイダー.md "wikilink")』を彷彿させる、一人称のアクションゲームのように描画される。
  - New Calico
    [小惑星](../Page/小惑星.md "wikilink")群で繰り広げられる艦隊戦が繰り広げられる。
  - AI (Merry Go Round AI Show)
    プロペラ機によるエアレースを描画。人工知能による制御に関する処理を計測する。
  - Physics（Crash’n’Burn Physics）
    AIと同じくエアレースの描画だが、[PhysX](../Page/PhysX.md "wikilink")ソフトウェアライブラリを適用した物理演算処理の能力を計測する。

### 3DMark11

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")リリース。DirectX11専用で、対応OSはWindows Vista及び[Windows 7のみだが](../Page/Microsoft_Windows_7.md "wikilink")、無料版の実行回数制限はなくなった\[11\]。

### 3DMark

[2013年](../Page/2013年.md "wikilink")リリース。Windows版はVista以降に対応（7,8.x,10推奨）\[12\]。

## 脚注

## 外部リンク

  - [UL Benchmarks公式（英語）](https://benchmarks.ul.com/)

[Category:ベンチマーク](https://ja.wikipedia.org/wiki/Category:ベンチマーク "wikilink") [Category:1998年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1998年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.  [Login](../Page/ログイン_\(雑誌\).md "wikilink")（[エンターブレイン](https://ja.wikipedia.org/wiki/エンターブレイン "wikilink")） 2000年11月号、p.129。
8.
9.
10.
11.
12.