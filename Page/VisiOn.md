> この記事は[VisiOn](https://ja.wikipedia.org/wiki/VisiOn)から翻訳されています。


**VisiOn** は、[ビジコープ](https://ja.wikipedia.org/wiki/ビジコープ "wikilink")が開発した[GUIベースの](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[オペレーティング環境](https://ja.wikipedia.org/wiki/オペレーティング環境 "wikilink")であり、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")の[MS-DOS](../Page/MS-DOS.md "wikilink")の初期のバージョンで動作した。VisiOn が人気となることはなかった（当時としては要求されるシステム構成が大きすぎた）が、[Windowsの開発に影響を与えた](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 歴史

### 背景

1981年春、Personal Software（後のビジコープ）は [VisiCalc](../Page/VisiCalc.md "wikilink") の成功によって潤っていた。そんな中、経営陣は今後の経営計画を練っていた。Ed Esber は VisiCalc と一緒に販売できるファミリ製品のコンセプトを提案したが、名前を似せる以外に機能的に連携できる製品がなかった。例えば、VisiPlot で VisiCalc のデータをグラフ化する場合、データを一旦 raw 形式でエクスポートして、再度インポートする必要があった。

Dan Fylstra 主導で、ユーザーのニーズを満たすにはどのように製品を連携させればよいかという技術的議論がなされた。彼らは3つの鍵となる概念を定めた。1つは汎用のデータ交換であり、各製品で共通の[データ構造](../Page/データ構造.md "wikilink")をサポートするというものである。もう1つはユーザインタフェースの共通化である。最後の1つは、あるプログラムを終了させて別のプログラムを起動するまでの時間の短縮であった。MS-DOS はシングルタスクであったため、例えば VisiDex で何かを参照するには VisiCalc での編集中のデータをセーブして終了させる必要があり、その後、再度 VisiCalc を再起動していた。この一連の操作をもっと単純化しようというのである。

### VisiOn の誕生

1981年6月、[ゼロックス](../Page/ゼロックス.md "wikilink")は [Xerox Star](https://ja.wikipedia.org/wiki/Xerox_Star "wikilink") [ワークステーション](../Page/ワークステーション.md "wikilink")を発表した。その時点で[アップルコンピュータがゼロックスのマシンの低価格版ともいうべきコンピュータを開発中であることは公然の秘密だった](../Page/アップル_\(企業\).md "wikilink")（後の [Lisa](../Page/Lisa_\(コンピュータ\).md "wikilink")）。Personal Software 社長 Terry Opdendyk は[テキサス州](../Page/テキサス州.md "wikilink")で単純なGUIを開発中の2人 Scott Warren と Dennis Abbe を知っており、彼らを Personal Software の本社（[カリフォルニア州](../Page/カリフォルニア州.md "wikilink")[サニーヴェイル](https://ja.wikipedia.org/wiki/サニーベール_\(カリフォルニア州\) "wikilink")）に招いた。彼らは非力な [TRS-80](https://ja.wikipedia.org/wiki/TRS-80 "wikilink") 上の [Smalltalk](../Page/Smalltalk.md "wikilink") のデモンストレーションを行い、同社の従業員に強烈な印象を与えた。

即座に契約が結ばれ、"Quasar" の開発がすぐさま開始された。名称は後に VisiOn に改められた。これは、"vision"（未来像）と同社の製品で採用されている "Visi" という接頭辞をかけたものである。[Apple III](../Page/Apple_III.md "wikilink") への移植は同年11月に完了し、その後各種[クロスコンパイラ](https://ja.wikipedia.org/wiki/クロスコンパイラ "wikilink")が揃っている [DEC VAX](https://ja.wikipedia.org/wiki/VAX "wikilink") 上で開発作業が行われた。1982年初め、Personal Software は社名を**ビジコープ**（VisiCorp）とし、同社の社運を VisiOn に賭けたのである。

VisiOn は最近のGUIが持つ多くの機能を備えており、しばらく一般化しなかったような機能も持っていた。完全[マウス駆動で](../Page/マウス_\(コンピュータ\).md "wikilink")、テキストもグラフィックスも[ビットマップ表示であり](https://ja.wikipedia.org/wiki/ビットマップ画像 "wikilink")、[オンラインヘルプ](https://ja.wikipedia.org/wiki/オンラインヘルプ "wikilink")を備え、一度に複数のプログラムを起動でき、それぞれを個別のウィンドウで表示した。しかし、VisiOn にはグラフィカルなファイルマネージャがなかった。また、高速なアプリケーション切り替えには[仮想記憶](../Page/仮想記憶.md "wikilink")システム実装のための[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")を必要とし、当時のハードディスクは非常に高価だった。

### COMDEXデモ

ビジコープの Tom Powers （新しいマーケティング担当副社長）は、1982年秋の [COMDEX](https://ja.wikipedia.org/wiki/COMDEX "wikilink") でこのシステムのデモンストレーションを行わせた。まだ出荷できる品質でないことから社内からは心配する声もあったし、即座に出荷できないと顧客や販売業者が待ちくたびれるという懸念もされた。また、同じショーで VisiWolrd もリリースされる予定となっていて、混同されることを恐れる声もあった。Powers は強引に作業を進め、IBM も事前に鳴り物入りで新製品を発表することで発売するころまでに新たな市場を作ってきたではないかと主張した。

COMDEX でのデモンストレーションは大成功を収めた。観客に対して、これがムービーなどではないことを説明しなければならなかった。[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")は、その PC が VAX などの他のマシンの単なる端末として動作しているのではないかと疑った。VisiOn は当時の業界の話題を独占した。しかし、この成功がいくつかの深刻な問題を引き起こすことになる。

まず、VisiOn の出荷日を知りたいという要望が多く寄せられ、ビジコープは 1983年夏のリリースであると発表した。しかし、その時点で開発者らはその時期の出荷が無理であると考えていた。1983年初め、最大限に努力しても第4四半期のリリースがぎりぎりであることが明らかとなり、その時点で業界はこれが[ベーパーウェア](https://ja.wikipedia.org/wiki/ベーパーウェア "wikilink")であると判断していた（ただし、ベーパーウェアという用語は当時は一般化していなかった）。

### 企業内戦

VisiOn の開発が続けられている間、ビジコープは崩壊の過程にあった。初期の[ベンチャーキャピタル](../Page/ベンチャーキャピタル.md "wikilink")の投資者らが選んだ社長 Terry Opdendyk は極めて独裁的な経営スタイルであり、多くの重要な経営陣がそれに反発して辞めていった。1981年末ごろから VisiOn のリリースまでに同社の製品管理関係者はほとんど辞めている。例えば、VisiCalc の開発責任者であった[ミッチ・ケイパー](https://ja.wikipedia.org/wiki/ミッチ・ケイパー "wikilink")、Ed Esber、Roy Folk などである。報道はこれを "corporate civil war"（企業内戦）と呼んだ。

中でもミッチ・ケイパーの離脱は大きな痛手だった。ケイパーは VisiPlot や VisiTrend の開発者であり、新たな進化した[表計算ソフト](../Page/表計算ソフト.md "wikilink")の開発を主張したが、Opdendyk は興味を示さなかった。当時、VisiCalc の売り上げは右肩上がりだったが、開発部門は袋小路に突き当たっていた。ケイパーが退職を決めたとき、他の経営陣は「統合型表計算ソフト」の他所での開発を禁じることを勧めたが、Opdendyk は「ケイパーはスパゲッティプログラマだ」と彼の才能を誹謗し、取り合わなかった。

ケイパーは [Lotus 1-2-3](../Page/Lotus_1-2-3.md "wikilink") をリリースし、1983年には VisiCalc の主な競合製品に成長させた。同年末、ビジコープの売り上げは半減した。主な経営陣の離脱と VisiCalc 開発者との争いにより、ビジコープは深刻な財政難に陥った。同社に残された唯一の希望は VisiOn だけだった。

### リリース

VisiOn は予定より数ヶ月遅れて、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")12月にリリースされた。**VisiOn Applications Manager**（基本[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")）は $495 で、マウスの購入には $295 が別途必要だった。その上で動作する3つのアプリケーションも同時にリリースされている。**VisiOn Calc**（[表計算ソフト](../Page/表計算ソフト.md "wikilink")）は $395、**VisiOn Graph** は $250、**VisiOn Word**（[ワードプロセッサ](../Page/ワードプロセッサ.md "wikilink")）は $375 であった。全部をパッケージにしたセットが $1765 であった。

しかし、VisiOn 導入時の主なコストはむしろマシンの方にあった。VisiOn は 2.2MB 以上のハードディスク容量を必要とし、当時市販されていた装置で言えば最低でも 5MB のハードディスク装置を必要とした。これを含めると、VisiOn 導入に必要となる費用は $7500 となる。

メディアは「オペレーティングシステムの最終形態」とまで言って、この製品を賛美し続けた。しかし、エンドユーザーにはそれほど受け入れられなかった。それは費用の問題だけでなく、性能に問題があったためでもある。当時のパーソナルコンピュータはせいぜい1つか2つのアプリケーションを搭載して利用されることが多く、VisiOn の存在意義は大きくはなかった。

一ヵ月後、[アップルコンピュータが](../Page/アップル_\(企業\).md "wikilink") [Macintosh](../Page/Macintosh.md "wikilink") をリリースし、大々的に宣伝された。もっとも、最初の Mac にはアプリケーションがほとんど無く、特に表計算ソフトが無かった。しかし、Mac は高性能で安価であり、グラフィカルなファイル管理プログラム（[Finder](https://ja.wikipedia.org/wiki/Finder "wikilink")）があり、見た目も好まれた。VisiOn と Macintosh は直接競合することはなかった（VisiOn はPC互換機向けだったため）が、VisiOn が提供できなかった高速性と利便性の両立を Macintosh は成し遂げていた。

さらなる問題として、ビル・ゲイツが1984年5月に [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") をリリースすることを発表した。発表時、同様な機能をハードディスク無しで実現し、費用はたったの $250 とされたため、業界の流れがいっきに変わった。皮肉なことに Windows のリリースは VisiOn よりも遅延して 1985年11月となり、VisiOn がハードディスクを必要とする原因となったマルチタスク機能を欠いていた。

VisiOn の売り上げは見る見る減少した。1985年2月、ビジコープは基本OSを $99 にしたが売り上げは改善せず、当然アプリケーションも売れなかった。全部をバンドルしたパッケージが $990 とされたことで状況は一時的に好転したが、売り上げは予測ほど伸びず、Lotus 1-2-3 にシェアを奪われ続けた。

VisiCalc の売り上げの減少と VisiOn の低迷により、1985年11月、同社は **Paladin Software** と合併し、名称は Paladin の方が存続することとなった。

## 技術的情報

VisiOn は [Intel 8086](../Page/Intel_8086.md "wikilink") [CPU](../Page/CPU.md "wikilink") を使った IBM PC（互換機）で動作した。512 [KBの](https://ja.wikipedia.org/wiki/キロバイト "wikilink") RAM と 5 MB の[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")が必要とされた。[CGA](../Page/Color_Graphics_Adapter.md "wikilink") 640×200 のモノクログラフィックスモードで動作する。同時に複数のアプリケーションを実行できる。オンラインの文書やヘルプファイルが組み込まれている。また、マウスを必要とした。

[C言語](../Page/C言語.md "wikilink")のサブセットで書かれており、VisiOn 向けのアプリケーションは[UNIX](../Page/UNIX.md "wikilink")への移植も可能とされていた（移植された例はない）。1984年、ビジコープの資産は[CDCに売却された](https://ja.wikipedia.org/wiki/コントロール・データ・コーポレーション "wikilink")。

## 関連項目

  - [DESQview](https://ja.wikipedia.org/wiki/DESQview "wikilink")
  - [GEM](https://ja.wikipedia.org/wiki/Graphical_Environment_Manager "wikilink")
  - [GEOS (オペレーティングシステム)](https://ja.wikipedia.org/wiki/GEOS_\(オペレーティングシステム\) "wikilink")
  - [TopView](https://ja.wikipedia.org/wiki/TopView "wikilink")
  - [Windows 1.0](https://ja.wikipedia.org/wiki/Microsoft_Windows_1.0 "wikilink")

## 外部リンク

  - [Nathan Lineback's GUI Gallery - VisiCorp Visi On](http://toastytech.com/guis/vision.html)

[Category:ウィンドウシステム](https://ja.wikipedia.org/wiki/Category:ウィンドウシステム "wikilink") [Category:DOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:DOSのソフトウェア "wikilink") [Category:1983年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1983年のソフトウェア "wikilink")