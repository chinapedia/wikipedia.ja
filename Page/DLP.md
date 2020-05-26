> この記事は[DLP](https://ja.wikipedia.org/wiki/DLP)から翻訳されています。


**DLP**

1.  映像表示システムの一種。本項で紹介。
2.  [離散対数問題](https://ja.wikipedia.org/wiki/離散対数問題 "wikilink")。[ElGamal暗号](../Page/ElGamal暗号.md "wikilink")や[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink")の[数論](../Page/数論.md "wikilink")的安全性の根拠。
3.  [情報漏洩](../Page/情報漏洩.md "wikilink")対策。**D**ata **L**oss **P**revention あるいは **D**ata **L**eak **P**reventionの頭字語。

-----

**DLP**（ディーエルピー）とは、[デジタルミラーデバイス](../Page/デジタルミラーデバイス.md "wikilink") (DMD)を用いた映像表示システムのことで[機械式テレビジョン](../Page/機械式テレビジョン.md "wikilink")の一種である。*Digital Light Processing*の[頭字語](../Page/頭字語.md "wikilink")で、[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")の[登録商標](https://ja.wikipedia.org/wiki/登録商標 "wikilink")である（[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")登録）\[1\]\[2\]。

[2004年](../Page/2004年.md "wikilink")現在、[プロジェクタ](../Page/プロジェクタ.md "wikilink")市場の47%を占め\[3\]、[液晶](../Page/液晶.md "wikilink")式プロジェクタと[市場占有率](../Page/市場占有率.md "wikilink")を争っていたが、[2011年](../Page/2011年.md "wikilink")末ではDLPのシェアが1年でほぼ倍増した。世界のシアターのほぼ半数以上が[デジタルシネマ](../Page/デジタルシネマ.md "wikilink")に移行したとし、これが[2015年](../Page/2015年.md "wikilink")までには完了するだろうと発表した\[4\]。

## 構造

[thumb](https://ja.wikipedia.org/wiki/ファイル:DLP_Black_and_White.gif "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:DLP_Color_wheel.gif "wikilink") 白色に光る[ランプの光を](https://ja.wikipedia.org/wiki/ランプ_\(光源\) "wikilink")[レンズ](../Page/レンズ.md "wikilink")で集光し、DMDに当てる。DMDの個々のミラーがオン状態に傾いているときの光を他のレンズで拡大し、[スクリーン](../Page/スクリーン.md "wikilink")に投影する。DMDミラーがオフ状態に傾いているときの光は投影レンズに入らずに捨てられる。

ミラーをオンにしている時間とオフにしている時間の比率で投影する点の明るさが制御される。すなわち、100%オン状態だと最大輝度の点になるし、50%オン・50%オフだと半分の輝度の点になる。

カラー画像を投影するためには、大きく分けて2つの手法が用いられる。

一つは、DMDを3個用い、光源も赤・緑・青の3つを用意する方法である。これは3板方式と呼ばれる。光源は実際には3つ用意するのではなく、白色光源を[ダイクロイックフィルター](https://ja.wikipedia.org/wiki/ダイクロイックフィルター "wikilink")で3色に分離したものを用いる事が多い。

もう一つは、光源とDMDの間に高速で回転するカラーホイールを配置し、赤・緑・青の光を時分割でDMDに当てる方法である。これは単板方式と呼ばれる。赤色を投影したい場合には赤の光がDMDにあたっている瞬間だけミラーをオン状態にする\[5\]。

DMDを構成するミラーは[マイクロ秒](https://ja.wikipedia.org/wiki/マイクロ秒 "wikilink")単位でオン・オフを変化させる事ができるため、このような手法を用いる事ができる。例えば、秒60フレームの映像を投影する事を考えると、1フレームあたりの投影時間は1/60秒=16667マイクロ秒である。これを赤・緑・青のための3つの時間に分割すると16667÷3=5556マイクロ秒となり、この時間内で256段階の明るさを再生するためには5556÷256=21.7マイクロ秒ごとにミラーのオンオフを切り替えられるようになっていなければいけない。オンオフの切り換えにミリ秒単位の時間がかかる液晶の場合、明るさの階調を表示する仕組みの違いを考慮しても、単板でカラー画像再生を行なうのは現実的ではない。

## チップセット

[thumb](https://ja.wikipedia.org/wiki/ファイル:Digital_Micromirror_Device_-_Chip.jpg "wikilink") テキサス・インスツルメンツ社はDLPシステム専用の[CPU](../Page/CPU.md "wikilink")などの[ICを開発し販売している](../Page/集積回路.md "wikilink")。[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")のCPUに[DSP機能などを付加したDDPチップと](../Page/デジタル信号処理.md "wikilink")、DMDミラーをリセットする電圧を供給するためのDADチップ、安定化[電源とカラーホイールモーター制御などを司るPMDチップが用意されている](../Page/電源回路.md "wikilink")。現在市場で使われているDLPプロジェクタのほとんどはDDPチップとDADチップを用いて作られている。

また、これらのチップを用いた[ソフトウェア](../Page/ソフトウェア.md "wikilink")開発を容易にするために、DLP Composerと呼ばれる開発ワークベンチがテキサス・インスツルメンツ社より提供されている。さらに、[CodeWarrior](../Page/CodeWarrior.md "wikilink")用のDDP FPライブラリセットも用意されており、DLPプロジェクタの開発作業は原則としてこれらを用いて行なわれる事となる。

DLPの要となるDMDは画素数として、800x600、1024x768、1280x1024、1280x768、1280x720、1920x1080などの種類があり、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")画像、[テレビ](../Page/テレビ.md "wikilink")画像、[映画](../Page/映画.md "wikilink")など用途に応じて選択される。

## 利点と欠点

DLPを用いてプロジェクタを作る利点はいくつかあり、

  - 完全にデジタル処理で画像を作るため、色再現性などが良い
  - 投影画像がデバイスに焼き付く事がほとんどない
  - デバイスの経年劣化が圧倒的に少ない（液晶や反射型液晶と較べて）
  - 黒画像に余計な光が入り込みにくい（黒浮きが少ない。コントラスト比が高い）
  - 画素格子が目立たない（液晶と較べて。隙間が少なく[画素密度](https://ja.wikipedia.org/wiki/画素密度 "wikilink")が高い）
  - 動きが速い動画再生時に残像などの精細度を落とす現象が発生しにくい
  - 単板で作成する事ができるため、小型化が容易
  - 単板で作成する事ができるため、画素ズレや色ムラが生じない

などが挙げられる。

[thumb](https://ja.wikipedia.org/wiki/ファイル:DLP_rainbow_effect.JPG "wikilink") 一方、欠点もいくつか挙げられるが、そのほとんどはDMDの価格が高いということに起因する。DMDの価格は液晶プロジェクタで使用される液晶パネルの数倍程度もするため、一般市場では3板式のDLPプロジェクタは受け入れられず、単板式にならざるを得ない。

単板式の場合、人間の目にはきちんと混色されて見えていても一瞬一瞬には赤・緑・青の単色が明滅しているので、投影画像の前で素早く物を動かしたりすると画像には無いはずの色が見えることがある。初期の頃のDLPプロジェクタはDDPチップの処理能力が遅かったため、この現象が顕著に観察されたが、最近は処理能力が改善されて色時分割の時間単位が細かくなったため、ほとんど目立たなくなっている。

また、単板式はその原理上、常に光源の明るさの約3分の2を捨てている事になる（赤を投影している瞬間は光源の明るさのうち緑と青の成分を捨てている）。このため、液晶は偏光により明るさの2分の1を失っているにも関わらず、同一の光源ならば3板式の液晶プロジェクタの方が単板式のDLPプロジェクタよりも明るい。（なお、プロジェクタの投影画像の明るさはレンズや分光フィルタの性能などによる部分も大きいため、比較はそれほど単純にはできない。）

さらに、光時分割を行なうためのカラーホイールはモーターで回転させるので、機械的な耐久性や音が問題になることがある。もっとも、ランプの熱を放散するためのファンのモータよりは耐久性も静音性も高いので、致命的な問題とはいえない。また、後述する[LED](https://ja.wikipedia.org/wiki/LED "wikilink")光源を用いるとカラーホイールそのものが不要となる。

## 技術革新

前記の欠点の項で述べた通り、単板式のDLPプロジェクタは常に光の3分の2を捨てているという問題を持つ。これを改善するために、カラーホイールに赤・緑・青の領域に加えて白（透明）の領域を作ったものが使われる。すなわち、白を発色する際には、3分の1の明るさを持つ光を使う時間が4分の3と、100%の明るさを持つ光を使う時間が4分の1という事になり、合計では失う光は2分の1で済む。

ここまでの説明ではあえて触れなかったが、カラーホイールの色の境目が光束を横切っている間は、画像の部分部分によって色の異なる領域があり、また色フィルタの境目の乱反射などにより正しい色の光になっていない。このため、原則としてはこの間の光は全て捨ててしまわなければいけない。カラーホイール上のこの領域は「スポーク (*spoke*)」と呼ばれ、スポーク中の光は「スポーク光 (*spoke light*)」と呼ばれる。

実際、初期の頃のDLPプロジェクタはスポーク光を全て捨てていた（その期間はDMDのミラーをオフ状態にしていた）ため、かなり暗い製品になっていた。

色の正確性を多少犠牲にしても良いならば、赤と緑の境界のスポーク光は黄色を発色する際に使えるはずであり、全スポークの光を合わせればほぼ白の光になるはずである。このため、スポーク光を利用して色を作る技術が開発された。テキサス・インスツルメンツ社は、混色にスポーク光を使う[アルゴリズム](../Page/アルゴリズム.md "wikilink")を「サブカラーブースト (*Sub Color Boost* : SCB)」、白色にスポーク光を使うアルゴリズムを「スポークライトリキャプチャ (*Spoke Light Recapture* : SLR)」と呼んでいる。

なお、カラーホイールの白部分を使う手法とスポークライトリキャプチャを使う事を合わせて白の輝度を上げる手法の事を「ホワイトピーキング (*White Peaking*)」と呼ぶ。また、テキサス・インスツルメンツ社はこれらの技術を改良した物を「ブリリアントカラー (*BrilliantColor*)」と名付け、商標登録している。\[6\]

近年はLEDの照度が上がってきたこともあり、LEDを光源としたプロジェクタが登場している。LEDの場合高速に点滅させることができる3色の光源を容易に用いることができるため、単板式であってもカラーホイールが不要になる。スポーク光がほぼ無い（一瞬にして光源色が赤から緑などに変わる）ので、正確な色作りをしても無駄光が発生しない。ただし、光源となる3色のLED光源(一般的にはRGB)が物理的に離れているため光学系で補正しても点光源とならず、投影画像に色ズレが発生する。 また、まだLEDの照度は電球よりも1桁以上低いため、一般的な明るさの部屋で数十インチ以上のスクリーンに投影する用途には耐えられない。20-30インチ程度の大きさならば、現在では液晶モニタのほうが安価で性能が良いが、従来のプロジェクタに比べ各コンポーネントを小型化する事が可能な為、モバイルプロジェクタやトイプロジェクタは、LED光源タイプに置き換わっている。また、LEDの実効寿命が圧倒的に長くランニングコストが低い。LEDタイプのプロジェクタを内蔵したビデオカメラ、ノートPCやデスクトップPCも商品化されている。

## 携帯機器用プロジェクタ

米TI社は[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")から携帯機器に使用されるDLPプロジェクタ用の、新たな製品群の量産出荷を開始した\[7\]。

このDMD方式の「DLP Picoチップセット」と呼ばれる小型の表示用部品は、LED光源と共に使用され、[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")程度の大きさの小型プロジェクタの中核部品となる。既にOptima technology社とSypro Optics社が、2008年末と2009年第1四半期の製品出荷を目指して開発中である。これらの機器は携帯用の[メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")と接続することで、従来の数インチ単位の液晶画面の静止画や動画を、大画面に投影する利用法を想定している。登場する最初の世代では電池駆動で10[ルーメン](../Page/ルーメン.md "wikilink")、2時間程度の使用が想定され、480x320の画素数、2-4W程度の消費電力で、当初の価格は400米ドル以下、量産時では200米ドル以下とされている。米TI社のDLP Picoの他にもいくつかDMDやMEMSの小型の表示用部品の製造計画が発表されており、2008年末からはこれらの表示用部品を組み込んだ単品の携帯型プロジェクタが、2009年末頃からは携帯型情報機器に組み込まれた形で、携帯プロジェクタ機能の搭載品が市場に登場する可能性がある。

ただ、[ノートパソコン](../Page/ノートパソコン.md "wikilink")への搭載は既に開発済みの技術で目処が立っているが、[携帯電話](../Page/携帯電話.md "wikilink")への組み込みを考えれば、プロジェクタ機能の部品容積で0.7cm<sup>3</sup>以下、消費電力で1W以下としなければならず、部品価格も50-60米ドル以下が求められるなど、実現までのハードルは高い。携帯電話より比較的大きいデジタルカメラへの搭載は、早期実現の可能性はより高い。

集光部品が省けるレーザ素子の方がLEDより小型化には向くが、価格が高く、緑色のレーザ発光素子が無いために1,064nm程度の赤外発光レーザーをSHG素子によって532nm程度に波長変換するが、これでは効率が悪く、今後、直接発光が可能な緑色のレーザ素子の登場が待たれる\[8\]。

TI社はこのDLP Picoをさらに発展させた「DLP Pico HD」を発表、[CES](../Page/コンシューマー・エレクトロニクス・ショー.md "wikilink")2011 で、[Acer](https://ja.wikipedia.org/wiki/Acer "wikilink")、[Dell](https://ja.wikipedia.org/wiki/Dell "wikilink")、[LG](https://ja.wikipedia.org/wiki/LG "wikilink")、[Optoma](https://ja.wikipedia.org/wiki/Optoma "wikilink")、[ViewSonic](https://ja.wikipedia.org/wiki/ViewSonic "wikilink")、[HP](../Page/HP.md "wikilink")、[LG](https://ja.wikipedia.org/wiki/LG "wikilink")、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")、[Samsung](https://ja.wikipedia.org/wiki/Samsung "wikilink")など30社からこれらを搭載した製品のプロトタイプが展示された\[9\]。さらに翌年のCES2012 では、Picoチップセットの累積出荷台数が200万を超えたと発表した\[10\]。

## その他

プロジェクタ以外に空間光変調素子として[共焦点顕微鏡](https://ja.wikipedia.org/wiki/共焦点顕微鏡 "wikilink")\[11\]や[光造形式の](https://ja.wikipedia.org/wiki/光造形法 "wikilink")[3Dプリンター](../Page/3Dプリンター.md "wikilink")で使用される。

## 主なメーカー

DLPプロジェクタを製造している主なメーカーは次の通り。

  - [クリスティ・デジタル・システムズ](http://christiedigital.jp)
  - [NEC](https://ja.wikipedia.org/wiki/NEC "wikilink")
  - [オプトマ](https://ja.wikipedia.org/wiki/オプトマ "wikilink")
  - [加賀電子](../Page/加賀電子.md "wikilink")
  - [カシオ計算機](../Page/カシオ計算機.md "wikilink")
  - [シャープ](../Page/シャープ.md "wikilink")
  - [デル](../Page/デル.md "wikilink")
  - [東芝](../Page/東芝.md "wikilink")
  - [BenQ](../Page/BenQ.md "wikilink")
  - [松下電器産業](https://ja.wikipedia.org/wiki/パナソニック "wikilink")
  - [三菱電機](../Page/三菱電機.md "wikilink")
  - [レノボ](https://ja.wikipedia.org/wiki/聯想集団 "wikilink")
  - [projectiondesign](https://ja.wikipedia.org/wiki/projectiondesign "wikilink")
  - [BARCO](https://ja.wikipedia.org/wiki/BARCO "wikilink")
  - [ViewSonic](http://www.nihonbinary.co.jp/144ViewSonicPJD6531w.html)
  - [LightSpeed Design](http://www.nihonbinary.co.jp/082InFocusDepthQ.html)
  - [GDCテクノロジー](https://ja.wikipedia.org/wiki/GDCテクノロジー "wikilink")
  - [アストロデザイン](../Page/アストロデザイン.md "wikilink")
  - [シネ・フォーカス](https://ja.wikipedia.org/wiki/シネ・フォーカス "wikilink")

## 出典

## 関連項目

  - [プロジェクタ](../Page/プロジェクタ.md "wikilink")
  - [デジタルミラーデバイス](../Page/デジタルミラーデバイス.md "wikilink")
  - [リアプロジェクションテレビ](../Page/リアプロジェクションテレビ.md "wikilink")
  - [レーザーテレビ](https://ja.wikipedia.org/wiki/レーザーテレビ "wikilink")
  - [The Society for Information Display](https://ja.wikipedia.org/wiki/The_Society_for_Information_Display "wikilink")(SID:世界最大のディスプレイ学会)
  - [機械式テレビジョン](../Page/機械式テレビジョン.md "wikilink") - 表示に機械的な動作を有するテレビジョン。

## 外部リンク

  - [日本TI DLPテクノロジー](http://www.tij.co.jp/jrd/dlp/docs/technology/index.htm)

[Category:プロジェクター](https://ja.wikipedia.org/wiki/Category:プロジェクター "wikilink")

1.  [Texas Business](http://www.texasbusiness.com/plano-cinema-firm-to-open-theater-with-digital-projection-self-serve-snacks-cms-2820)
2.  日本では1998年に初めて商標登録されている（第4106085号ほか）。他社も別分野で登録している。
3.  [日本TI プレスリリース 2005年2月15日](http://www.tij.co.jp/news/sc/2005/scj_05_013.htm)
4.  [2011/12/7 TIニュースリリース](http://www.dlpcinema.com/technology/dlp-press-releases/press-release.aspx?id=1510)
5.  [アリの足先より小さな鏡”が生み出す映像美——DLPの魅力](http://www.itmedia.co.jp/lifestyle/articles/0409/03/news054.html)
6.  [TI PRESS RELEASE 6/8/2005](http://dlp.com/about_dlp/about_dlp_press_release.asp?id=1260)
7.  [TI、プロジェクター携帯電話を実現する「DLP Pico」チップセットの量産化を発表](http://japan.internet.com/allnet/20080213/2.html)
8.  根津貞著　『プロジェクターが携帯機器に載る』　日経エレクトロニクス　2008年8月11日号
9.  [2011/01/05 TIニュースリリース](http://www.dlp.com/jp/technology/dlp-press-releases/press-release.aspx?id=1422)
10. [2012/01/11 TIニュースリリース](http://www.dlp.com/jp/technology/dlp-press-releases/press-release.aspx?id=1520)
11.