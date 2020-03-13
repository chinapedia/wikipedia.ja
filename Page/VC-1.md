> この記事は[VC-1](https://ja.wikipedia.org/wiki/VC-1)から翻訳されています。


**VC-1**（ブイシーワン）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した[動画像](https://ja.wikipedia.org/wiki/動画像 "wikilink")[圧縮方式である](../Page/データ圧縮.md "wikilink")[Windows Media Video](../Page/Windows_Media_Video.md "wikilink") 9を規格化したものである。

規格化にあたり、[MPEGなどと同様に](../Page/MPEG-1.md "wikilink")、復号処理、すなわちデコーダの設計に関する規格として標準化されており、符号化処理、すなわちエンコーダの設計に関しては言及しない。なお、Windows Media Videoの場合は[Windows Media PlayerやWindows](../Page/Windows_Media_Player.md "wikilink") Mediaエンコーダ等で利用するコーデック全般を指す。

## 概要

[2003年](../Page/2003年.md "wikilink")[9月](../Page/9月.md "wikilink")、マイクロソフトは米国映画テレビジョン技術者協会([SMPTE](../Page/SMPTE.md "wikilink"))に、Windows Media Video 9の符号化技術に[インタレース対応のための拡張を追加したものを規格化し](../Page/走査.md "wikilink")、VC-9という名称で提出した。Windows Media Video 9相当の部分はベースライン[プロファイルおよびメインプロファイル](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")、インタレース対応の部分はアドバンスドプロファイルとして定められている。

その後、最初に提出した規格の名称の番号が9ではおかしいという指摘があり、VC-1に改称された。

[2004年](../Page/2004年.md "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")、[DVDフォーラム](../Page/DVDフォーラム.md "wikilink")がVC-9(当時)および[MPEG-4 AVCを](../Page/H.264.md "wikilink")[HD DVDプレーヤの必須](../Page/HD_DVD.md "wikilink")[コーデック](../Page/コーデック.md "wikilink")とすることを承認し、同12月にVC-1についてはアドバンスドプロファイルを採用することを決定した。また、[Blu-ray Discでも同](../Page/Blu-ray_Disc.md "wikilink")9月にVC-1アドバンスドプロファイルとMPEG-4 AVCハイプロファイルの採用を決定している。

[2005年](../Page/2005年.md "wikilink")[10月](https://ja.wikipedia.org/wiki/10月 "wikilink")、SMPTEでのVC-1規格化作業が完了し、SMPTE 421Mとして発表された。

[2007年](../Page/2007年.md "wikilink")[1月30日](../Page/1月30日.md "wikilink")、[Windows Media Player 11](../Page/Windows_Media_Player.md "wikilink") for [Windows XPが](../Page/Microsoft_Windows_XP.md "wikilink")、[Windows Vistaの発売にあわせ正式公開された](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。それまではβ版コーデックを入れないといけなかったが、WMP 11にはVC-1コーデック(WVC1)が同梱され、扱いやすくなった。なお、Windows Vistaには最初からWMP 11が含まれているため、VC-1コーデックに標準で対応している。

2014年現在、ffmpegはエンコードをサポートせずVC-1をエンコードできるエンコーダーは商用、非商用とも僅かである。またマルチプラットホームでの再生にも難があり、普及率ではH.264に大きく後れをとっている。

## 符号化技術

符号化技術そのものは[MPEG-4パート2をベースとしており](https://ja.wikipedia.org/wiki/MPEG-4#MPEG-4_\(Part_2\) "wikilink")、さらに[圧縮効率](https://ja.wikipedia.org/wiki/圧縮効率 "wikilink")を高めるためのさまざまな工夫が施されている。この点に加えて、全ての符号化処理が16ビット整数で実現可能であることが、[H.264](../Page/H.264.md "wikilink")との共通点といえるため、VC-1とH.264は技術面でも性能面でもしばしば比較の対象として取り上げられている。

### 整数変換

H.264と同様に、VC-1では浮動小数点精度の[離散コサイン変換](../Page/離散コサイン変換.md "wikilink")(DCT)の代わりに整数変換を採用している。画像特徴に応じて8×8,8×4,4×8,4×4の4種類から変換行列を選択可能であることがVC-1の特徴である。

H.264では整数変換のスケーリング演算と量子化が統合されているのに対して、VC-1の整数変換は単純にDCTの整数近似として定められている。このため、変換行列の近似には、デコーダに影響のない範囲での誤差が許容される。

### フレーム間予測

VC-1の[フレーム間予測](../Page/フレーム間予測.md "wikilink")方式はMPEG-4パート2とほぼ同等であり、16×16および8×8のいずれかの画素ブロックを単位とした動き補償を行う。

#### 分数精度画素動き補償

VC-1ではピクチャ単位で動きベクトルの画素精度を1/2と1/4のうちいずれかから選択可能である。なお、MPEG-4パート2ではストリーム単位でしか画素精度を選択できない。

また、デコーダ側の処理負荷を軽減することを目的として、1/2画素精度の場合は画素補間フィルタをバイキュービックフィルタかバイリニアフィルタのうちいずれかから選択できる。

#### ハイブリッド動きベクトル予測

MPEG-4では、動きベクトルをより小さい表現でできるようにするために、上、右上、左に隣接するブロックの動きベクトルの中間値を予測動きベクトルとして、実際の動きベクトルと予測動きベクトルの誤差を符号化するようにしている。これにより、画面全体で動きベクトルの変化が緩やかなときに動きベクトルの符号量を大幅に削減することができる。これをメジアン予測と呼ぶ。

一方、メジアン予測の場合、局所的に大きさや向きが大幅に異なる動きベクトルが出現した場合、予測によってかえって符号量が増大することがある。そこでVC-1では、メジアン予測を使わずに上ないし左のブロックの動きベクトルをそのまま予測値として利用するブロックを指定できる。これをハイブリッド動きベクトル予測と呼んでいる。

### AC/DC予測

VC-1では、フレーム間予測を用いないピクチャやブロックにおいて、MPEG-4パート2と同様のAC/DC予測を採用している。

MPEG-4との違いは、エントロピー符号化におけるハフマンテーブルが条件によって異なるものと利用するという点である。

### オーバーラップスムージング

VC-1では、ブロック境界での歪みを軽減するために、ブロック境界をスムージングするフィルタを、動き補償の参照フレームに対して適用する。

H.264で採用されているデブロッキングフィルタと同等の役割を果たすが、H.264に比べて単純な処理構造を持つことが特徴である。

### ビットプレーン符号化

一般に、MPEG系の符号化方式では、16×16画素のマクロブロックを単位として、そのマクロブロックの符号化モードやDCT係数、動きベクトルなどを符号化する。

これに対して、VC-1では各マクロブロックに固定的に1ビットずつ割り当てられる符号化モードのデータについては、ピクチャ単位でまとめて符号化する。これをビットプレーン符号化と呼んでいる。スキップモード(DCT係数も動きベクトルも符号化せず、予測可能な情報のみを用いて復号するモード)やハイブリッド動きベクトル予測などのデータが対象となる。

### プロファイル

VC-1では、分数精度動き補償でのバイキュービックフィルタなどのような処理負荷の高いツールを省いた**ベースラインプロファイル**(Baseline Profile)と、インタレース対応以外の全てのツールを採用した**メインプロファイル**(Main Profile)、インタレース対応のための拡張プロファイルである**アドバンスドプロファイル**(Advanced Profile)の3種類が規定されている。

なお、もともとPC向けのストリーミング用コーデックであるWindows Media Video 9をベースとして、後付けの形でインタレースに対応したため、アドバンスドプロファイルとメインプロファイルに全く互換性がないのが特徴である。このため、[Microsoft Windows向けには](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、Windows Media Player 10の付属コーデックとしてWindows Media Video 9 Advanced Profileが追加されている。

## 多重化フォーマット

映像と音声を多重化するシステムフォーマットとして、Windows Mediaでは[ASFがよく用いられる](../Page/Advanced_Systems_Format.md "wikilink")。これに対し、SMPTEでは放送向けにVC-1を用いる際、[MPEG-2 TSを用いるための勧告](https://ja.wikipedia.org/wiki/MPEG-2システム#トランスポートストリーム "wikilink")(SMPTE RP227)を公開している。また、HD DVDとBlu-ray Discでも、MPEG-2 TSを多重化フォーマットとして採用している。

## 特許問題

これまで、マイクロソフトがWindows Media Videoとしてプロプライエタリな製品技術として利用していた頃には表面化しなかったが、VC-1としてSMPTEに提出されるにあたり、これがMPEG-4をベースとした技術であることが判明した。そのため、その技術がマイクロソフト以外の特許を含む可能性が高いものと考えられるようになり、ライセンスの扱い方が問題となった。

この問題を解決するため、2004年[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")、米国のライセンス管理会社[MPEG LAが](https://ja.wikipedia.org/wiki/MPEG_LA "wikilink")、[MPEG-2](../Page/MPEG-2.md "wikilink")やMPEG-4、H.264と同様にVC-9(当時)のライセンス管理を行うことを表明し、関連特許の募集を開始している。

## 利用例

  - [Blu-ray Disc](../Page/Blu-ray_Disc.md "wikilink")
  - [HD DVD](../Page/HD_DVD.md "wikilink")

## 外部リンク

  - [VC-1公認: WMVの一部はVC-1非互換に - 妖精現実フェアリアル](http://www.faireal.net/dat/d6/d60409.xml)
  - [Windows Media Video 9 Advanced Profile Update Beta](http://www.microsoft.com/windows/windowsmedia/forpros/encoder/default.mspx)

<!-- end list -->

  - [Microsoft Windows Media:Windows Media Player 11](http://www.microsoft.com/japan/windows/windowsmedia/player/11/)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:アメリカ合衆国のメディア](https://ja.wikipedia.org/wiki/Category:アメリカ合衆国のメディア "wikilink")