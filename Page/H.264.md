> この記事は[H.264](https://ja.wikipedia.org/wiki/H.264)から翻訳されています。


**H.264**（エイチにいろくよん）、**MPEG-4 AVC**（エムペグフォーエーブイシー）は、[動画圧縮規格の一つ](https://ja.wikipedia.org/wiki/動画#動画圧縮 "wikilink")。

[ITU-T](../Page/ITU-T.md "wikilink")では「H.264」として、[2003年](../Page/2003年.md "wikilink")初めに勧告された。[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IECでは](../Page/国際電気標準会議.md "wikilink")、ISO/IEC 14496-10「[MPEG-4](../Page/MPEG-4.md "wikilink") Part 10 Advanced Video Coding（通称：MPEG-4 AVC）」として規定されている。どちらも技術的には同一のものであり、ITU-TとISO/IECが共同で策定したため、両者の呼称を「**H.264/MPEG-4 AVC**」「**MPEG-4 AVC/H.264**」と併記することが多い。規格文書では「**ITU-T Rec. H.264 | ISO/IEC 14496-10 Advanced Video Coding**」と縦線で区切られているため、「**H.264|MPEG-4 AVC**」などとすることもある。主にソフトウェア内部の識別子として「AVC1」も使われている。

従来方式である[MPEG-2](../Page/MPEG-2.md "wikilink")などの2倍以上の[圧縮効率を実現する](../Page/データ圧縮比.md "wikilink")。[携帯電話](../Page/携帯電話.md "wikilink")などの低[ビットレート用途から](../Page/ビット毎秒.md "wikilink")、[HDTVクラスの高ビットレート用途に至るまで幅広く利用されることを想定している](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")。

## 技術概要

圧縮アルゴリズムの原理は、従来方式の[MPEG-1](../Page/MPEG-1.md "wikilink")、[MPEG-2](../Page/MPEG-2.md "wikilink")、[H.261](../Page/H.261.md "wikilink")、[H.263](../Page/H.263.md "wikilink")、[MPEG-4](../Page/MPEG-4.md "wikilink")などと基本的には同様で、[空間変換](https://ja.wikipedia.org/wiki/空間変換 "wikilink")や[フレーム間予測](../Page/フレーム間予測.md "wikilink")、[量子化](https://ja.wikipedia.org/wiki/量子化 "wikilink")、[エントロピー符号](https://ja.wikipedia.org/wiki/エントロピー符号 "wikilink")化を採用している。H.264ではこれらのツールに対して非常に多数の改良が施されており、[算術符号](../Page/算術符号.md "wikilink")化やフィルタなどのツールも追加されている。さらに、画像特徴に応じて多彩なモードを適応的に使い分けることで、従来方式をはるかにしのぐ圧縮効率を達成している。

### 整数変換

従来規格のMPEG-1、MPEG-2やH.261では16×16画素、H.263、MPEG-4では8×8画素のブロック（マクロブロック）を単位として、原画像ないしフレーム間予測の予測誤差画像の[離散コサイン変換](../Page/離散コサイン変換.md "wikilink") (DCT) 係数を求め、その係数を量子化している。このとき、[コサイン関数を用いるため](../Page/三角関数.md "wikilink")、実数精度の演算が必要となる。これに対しH.264では、16ビット整数精度で演算が可能な整数変換を採用している。この整数変換は、加減算とビットシフトのみによって演算可能となるように設計されているため、[ソフトウェア](../Page/ソフトウェア.md "wikilink")、[ハードウェア](../Page/ハードウェア.md "wikilink")いずれの場合でも実装が非常に容易となる。

演算がすべて整数精度で行われることで、実数演算の実装差による「デコーダごとの演算結果の差分」を生じさせることなく[エンコード](../Page/エンコード.md "wikilink")することが可能となった。これは、エンコード時の局部復号器の結果とすべてのデコーダでの出力結果が全く同一になることを意味している。エンコード時の局部復号器の結果とデコーダの出力結果が異なる場合、エンコーダが作成する再構成画像とデコーダが作成する再構成画像が異なることとなるため、フレームが経過するごとに画像にノイズが蓄積してしまう。これを回避するため従来技術ではそのDCT演算誤差の帳消しのために定期的にイントラマクロブロックを挿入する必要があった。H.264では整数変換を用いており誤差の問題が生じないため、定期的にイントラマクロブロックを挿入する必要がない。

デコーダの実装差による出力結果の違いが生じないことは、デコーダの規格適合性を検証する上でも有利となる。H.264の関連規格であるH.264.1はH.264規格適合性の検証手法を定めるもので、H.264で符号化済の試験用ビットストリームとそのデコード結果の組が多数付属している。開発中のデコーダに試験用ビットストリームを入力し、その出力結果とH.264.1付属のデコード結果が厳密に一致しているかどうかを確かめることで、規格適合性の判断を行うことができる。

当初、H.264で使用可能な整数変換のブロックサイズは4×4画素のみだった。このサイズでは、低解像度の動画の圧縮では比較的好適な画質を示すが、[HDTVなどのような高解像度の動画で画質の再現性に弱いという問題点があった](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")。そのため、後に導入された[プロファイル群では](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")、これを克服するために8×8サイズの整数変換が導入されている。これらのプロファイルでは、フレーム内で4×4変換と8×8変換を適応的に切り替えて使用することができる。

### フレーム間予測

#### 複数参照フレーム

従来技術では、[フレーム間予測](../Page/フレーム間予測.md "wikilink")で参照フレームとして指定できるフレームは、Pフレームについては直前のI, Pフレーム、Bフレームについては直前および直後のI, Pフレームに固定されている。

H.264では、複数の参照フレームを持つことによって、例えばシーンチェンジや移動物体を考慮してより前のフレームを参照フレームとして指定することが可能となっている。また、Bフレームについては未来方向のフレームを使わずに過去の2フレームを参照フレームとして指定したり、別のBフレームを参照フレームとして指定することが可能となっている。

複数参照フレームの導入に伴いIフレームより前のフレームも参照可能となっている。この場合、Iフレームから再生を開始しようとしても、後続のフレームが、再生を開始しようとするIフレームより前のフレームの情報を必要とすることがある。このため、H.264ではIフレームから再生を開始することができるとは限らない。この問題を解決するため、参照フレームが格納されているバッファのクリアを行うことでそのフレームから再生が可能であることを保証する、IDR (Instantaneous Decoder Refresh) フレームが導入されている。すなわち、P, BフレームはIDRフレームをまたいで参照フレームを指定することができないように定められている。

#### 可変ブロックサイズ

従来技術では、動き補償の単位は16×16画素のマクロブロックが基本であり、[H.263](../Page/H.263.md "wikilink")および[MPEG-4](../Page/MPEG-4.md "wikilink")においては8×8画素ブロック単位の動き補償も利用できた。

H.264ではさらに単位ブロックサイズを追加し、16×16, 16×8, 8×16, 8×8の4種類から選択可能となっている。さらに、8×8画素ブロックについては、8×8, 8×4, 4×8, 4×4の4種類のサブブロック分割も指定できる。

このように多数のブロックサイズを利用することで、形状や動きに適したブロックから予測が可能である。これは、原理的には符号化効率が上がることとなる。ただし、サブブロックを指定することは余分なヘッダが付加されることになり、これがオーバーヘッドとなって符号化効率に影響を与える可能性もある。シーンに適した動き補償ブロックサイズを選択することが、エンコーダには求められる。

#### 重み付け予測

H.264では、従来方式では画質向上が困難だった[フェード](../Page/フェード.md "wikilink")や[ディゾルブ](https://ja.wikipedia.org/wiki/ディゾルブ "wikilink")などの特殊効果が用いられている動画の画質向上のため、参照フレームの予測誤差に重み付け係数を掛けてデコードする、重み付け予測 (Weighted Prediction) が採用されている。フェードやディゾルブは、前フレームと現フレームで一定のオフセットがかかったような画像であるため、そのことで予測差分に大きな値が生じることとなり、MPEG-4などでは画質劣化の原因として問題となっていた。

#### 1/4画素精度動き補償

動き補償の精度としては、MPEG-4 ASPで導入された1/4画素精度（クォーターペル精度）動き補償を使用している。ゆっくり動くパンなどで特に効果的である。1/2画素精度動き補償では6tapフィルターを用いて高周波まで再現を行っており、MPEG-4で使用された線形補間よりも再現性が良くなっている。1/4画素の生成は、再現性の高い1/2画素を用いてその線形補間で作成を行う。

### イントラ予測

H.264では、フレーム間予測を用いないマクロブロックに対して、上や左などに隣接するマクロブロックの隣接画素から補間によって予測画像を生成し、その予測画像との差分を符号化する、イントラ予測 (Intra prediction) が採用されている。予測画像の生成単位となるブロックサイズは、輝度 (Y) 成分については4×4および16×16画素の2種類であり、色差 (Cb, Cr) 成分の8×8画素については8×8画素単位の1種類である。また、予測画像生成における補間パターンは、輝度成分の4×4単位の場合は9種類、輝度成分の16×16単位および色差成分の場合は4種類が利用できる。

さらに、ハイプロファイル以上のプロファイル（後述）では、8×8画素単位のイントラ予測も利用可能である。補間パターンは4×4の場合と同様の9種類が利用できる。なお、8×8、4×4の場合は、整数変換も同じ行列サイズに固定される。

MPEG-4で導入されているAC/DC予測では、予測する係数がDCT係数の行列のうちの最上列ないし最左行の係数に限られているため、縦方向ないし横方向の画素変化に対してしか予測効率を高めることができない。これに対して、H.264のイントラ予測ではDCT係数ではなく画素レベルでの予測を行い、かつ縦・横方向以外にも斜め方向の画素予測パターンも利用できるため、予測効率が大幅に向上している。

### エントロピー符号化

H.264では、[ハフマン符号](../Page/ハフマン符号.md "wikilink")をベースとした可変長符号化 (VLC; Variable Length Coding) と、[算術符号](../Page/算術符号.md "wikilink")化のいずれかを選択できる。

前者はBaseline Profileで採用され、従来の3次元VLCに近いCAVLC (Context-based Adaptive VLC) と、指数ゴロム (Exponential-Golomb) 符号を用いることによって変換テーブルを用いずに符号化するUVLC (Universal VLC) が用いられる。CAVLCでは隣接MBのDCT係数の状態に依存して現在のMBの符号化に使用する符号化テーブルを切り替える。このように切り替えを行うことで、現在の画像のテクスチャに応じた符号化テーブルが使用でき、より短い符号への圧縮が期待できる。

後者はCABAC (Context-based Adaptive Binary Arithmetic Coding) と呼ばれ、Main Profileで採用されている。

H.264ではこのように複数の符号化方式が用いられている。これは、処理量は少ないが効果もそこそこのCAVLCと、処理量は大きいが効果も高いCABACではその用途が異なるため、そのことによって「符号化」という同じ目的を持ったツールが複数存在することとなった。

### デブロッキングフィルタ

H.264では、かつて[H.261](../Page/H.261.md "wikilink")で採用されたループ内フィルタ (In-loop Filter) と似たように、ループ内にデブロッキングフィルタ (Deblocking Filter) が設置されている。このフィルタはH.261のようなブロック全体の平滑化フィルタではなく、整数変換のブロック境界のみを平滑化して[ブロックノイズ](../Page/ブロックノイズ.md "wikilink")の発生を抑制するものである。H.261のループ内フィルタは、MPEG-2以降で採用された半画素精度動き補償が数学上同等の役割を果たすため、その意味を失った。

デブロッキングフィルタは圧縮率向上のためには効果的であるが処理量が大きいために、そのON/OFFがヘッダによって指定可能とされている。したがって、処理量に懸念がある場合にはデブロッキングフィルタを使用しないといった選択肢も可能である。

### SI, SPフレーム

例えば番組のチャンネルを切り替えたり、再生の途中でプレビューを見ながら早送りしたりする場合のように、ある動画ストリームから途中で別のストリームに切り替えて再生する場合、次のストリームの再生はフレーム間予測を用いないIフレームを受信するまでできなくなる。そこでH.264では、切替用の中間フレームとして、SI, SP（SはSwitchingの意）フレームが採用されている。特にSPフレームの場合は、切替前の動画のフレームを参照画像として切替後の動画がデコードできるように符号化される。

## NAL構造

H.264のビット列の規則（シンタックス）は、圧縮符号化された画像データをビット列に変換するための規則を定めた**VCL (Video Coding Layer)** と、VCLやヘッダ情報などのデータを分割および識別するための**NAL (Network Abstraction Layer)** の2層構造を持つ。

従来技術では、シンタックスに従って1つの動画を圧縮符号化した場合、1つのビット列（エレメンタリストリーム）となる。これに対し、H.264では複数の種類のNALユニットに分割して符号化される。なお、従来のエレメンタリストリームと同様に1つのビット列として圧縮データを扱うことができるように、バイトストリームフォーマットがAnnex Bで規定されている。

NAL構造によって、[MP4](../Page/MP4.md "wikilink")などのファイルフォーマットに格納したり、[RTP](https://ja.wikipedia.org/wiki/:en:Real-time_Transport_Protocol "wikilink")[パケット](../Page/パケット.md "wikilink")に分割して伝送したりするなど、圧縮データをさまざまな用途に柔軟に適用できるようになっている。

## マルチビュー符号化

複数の視点（マルチビュー）で撮影された映像を、それぞれのビューを独立して扱うよりも効率的に圧縮することができるマルチビュー符号化 (MVC: Multiview Video Coding) が、H.264のバージョン10で追加で規格化されている。MVCではマルチビュー映像を、1個の**ベースビュー** (base view) と、1個以上の**非ベースビュー** (non-base view) として符号化する。ベースビューは既存のプロファイル（現在ではハイプロファイルのベースビューのみ定義）のストリームとして符号化され、非ベースビューはMVCで新たに拡張されたプロファイルとシンタックスを用いて、他のビューや自分自身のビューに含まれるフレームを参照（**ビュー間予測**: inter-view prediction）して符号化される。

ビュー間予測を用いることで、ビュー間の相関が利用可能になるほか、非ベースビューでは符号量の大きいIフレームを使用しない符号化が可能となるため、より効率的に圧縮できる。通常のH.264ストリームでは、多くのアプリケーションで必要となるランダムアクセス機能（放送チャンネル切替えやチャプタージャンプのようにストリームの途中から再生する機能）のために、適切な時間間隔でIフレームを挿入しておく必要があった。放送の場合は通常0.5秒程度である。

MVCでもベースビューではそれが当てはまるが、非ベースビューのフレームについては、ベースビューのみを参照するP/Bフレームだけで構成すれば、ベースビューがランダムアクセス可能である限り、その非ベースビューもランダムアクセス可能である。なお、そのように符号化された非ベースビューのみを参照する形で、別の非ベースビューを符号化してもやはりランダムアクセスは可能である。

MVCに対応しない従来のデコーダでもベースビューのプロファイルとレベルを満足すれば、ベースビューのみの再生は可能であり、[後方互換](https://ja.wikipedia.org/wiki/後方互換 "wikilink")性が維持される。非ベースビューについても、使用されている圧縮のツール（アルゴリズム）についてはビュー間予測が可能という点を除き従来のI/P/Bピクチャと同じものを使用するため、デコーダをMVC対応とするのに必要な機能拡張は少ない。ただし、複数のビューをデコードするために、必要な処理速度は単一ビューに比べ増大する。

MVCを使用した場合の圧縮の効率は、2視点のステレオ映像の場合、1視点に比べ50%程度のデータ量の増加で圧縮可能とされている。なお、50%程度という数字はBlu-ray Disc Associationが2009年12月17日に発表したものである。

## プロファイルとレベル

MPEG-2などと同様、目的用途別に定義された機能の集合を表す**プロファイル**と、処理の負荷や使用メモリ量を表す**レベル**が定義がされる。これらは画面解像度やフレームレートに影響する。

H.264に準拠する機器またはビットストリームそのものは、このプロファイルとレベルによって、機器の性能やビットストリームをデコードするのに必要な性能を表示することが多い。

### プロファイル

H.264規格では当初ベースラインプロファイル、メインプロファイル、拡張プロファイルのみだった。その後、規格の拡張に伴い種類が増加している。以下では主なものを挙げる。

  - **制約付きベースラインプロファイル**(Constrained Baseline Profile)

<!-- end list -->

  -
    ローコストアプリケーションのためのプロファイル。ビデオ会議やモバイルアプリ等で使用される。

<!-- end list -->

  - **ベースラインプロファイル**(Baseline Profile)

<!-- end list -->

  -
    I, Pフレームのみ、エントロピー符号化はCAVLC+UVLCのみ。

<!-- end list -->

  - **メインプロファイル**(Main Profile)

<!-- end list -->

  -
    ベースラインプロファイルにBフレーム、CABAC、重み付け予測などを追加。

<!-- end list -->

  - **拡張プロファイル**(Extended Profile)

<!-- end list -->

  -
    ベースラインプロファイルにSI, SPフレームなどを追加。

<!-- end list -->

  - **ハイプロファイル**(High Profile)

<!-- end list -->

  -
    メインプロファイルに8×8画素整数変換、量子化マトリックス等を加えたもの。また、YCbCr 4:0:0色空間（[グレースケール](https://ja.wikipedia.org/wiki/グレースケール "wikilink")）にも対応している。

<!-- end list -->

  - **ハイ 10 プロファイル**(High 10 Profile)

<!-- end list -->

  -
    ハイプロファイルに10ビット画像フォーマットへの対応を追加したもの。

<!-- end list -->

  - **ハイ 4:2:2 プロファイル**(High 4:2:2 Profile)

<!-- end list -->

  -
    ハイ10プロファイルにYCbCr 4:2:2色空間への対応を追加したもの。

<!-- end list -->

  - **ハイ 4:4:4 プロファイル**(High 4:4:4 Predictive Profile)

<!-- end list -->

  -
    ハイ4:2:2プロファイルにYCbCr 4:4:4色空間や12ビット画像フォーマット、YCbCr以外への色空間への変換、[可逆圧縮](../Page/可逆圧縮.md "wikilink")など多数の機能を追加したもの。

<!-- end list -->

  - **マルチビューハイプロファイル**(Multiview High Profile)

<!-- end list -->

  -
    MVC拡張規格の策定に伴い定義されたプロファイル。ベースビューはハイプロファイルと互換のある符号化を行い、非ベースビューはマルチビュー拡張で定義されたシンタックスで符号化する。最大1024個のビューを符号化できるが、インターレース符号化をサポートしない。

<!-- end list -->

  - **ステレオハイプロファイル**(Stereo High Profile)

<!-- end list -->

  -
    ステレオ（2視点）映像を想定しており、MVCにおいて、ビューの数を2個以下に制限し、インターレース符号化をサポートするMVC拡張用プロファイル。[Blu-ray Discの](../Page/Blu-ray_Disc.md "wikilink")3D拡張版に採用されている。

<table>
<caption>プロファイルごとの機能一覧表</caption>
<thead>
<tr class="header">
<th><p>Feature</p></th>
<th><p>CBP</p></th>
<th><p>BP</p></th>
<th><p>XP</p></th>
<th><p>MP</p></th>
<th><p>HiP</p></th>
<th><p>Hi10P</p></th>
<th><p>Hi422P</p></th>
<th><p>Hi444PP</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>I and P スライス</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>YCbCr色空間</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>色深度 (bits)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Flexible macroblock ordering (FMO)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>任意順序スライス (ASO)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>冗長スライス (RS)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>データ分割</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>SI and SP slices</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>B スライス</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>インターレースコード (PicAFF, MBAFF)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>複数フレーム参照</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>In-loop deblocking filter</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>CAVLC 符号化</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>CABAC 符号化</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>8×8 vs. 4×4 適応変換</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Quantization scaling matrices</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Separate C<sub>b</sub> and C<sub>r</sub> QP control</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>グレースケール (4:0:0)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Separate color plane coding</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>予測的可逆エンコード</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### レベル

**レベル1**から**レベル5.1**まで、16段階が定義されている。それぞれのレベルにおいて、処理の負荷や使用メモリ量等を表すパラメータの上限が定められ、画面解像度やフレームレートの上限を決定している。各パラメータの詳細は[英語版を参照のこと](https://ja.wikipedia.org/wiki/:en:H.264/MPEG-4_AVC#Levels "wikilink")。

<table>
<caption>Levels with maximum property values</caption>
<thead>
<tr class="header">
<th><p>Level</p></th>
<th><p>最大マクロブロック</p></th>
<th><p>最大動画ビットレート (VCL)</p></th>
<th><p>解像度例@<br />
フレームレート<br />
（ストアされる最大フレーム数）</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>秒あたり</p></td>
<td><p>フレームあたり</p></td>
<td><p>BP, XP, MP<br />
(kbit/s)</p></td>
<td><p>HiP<br />
(kbit/s)</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>1,485</p></td>
<td><p>99</p></td>
<td><p>64</p></td>
</tr>
<tr class="odd">
<td><p>1b</p></td>
<td><p>1,485</p></td>
<td><p>99</p></td>
<td><p>128</p></td>
</tr>
<tr class="even">
<td><p>1.1</p></td>
<td><p>3,000</p></td>
<td><p>396</p></td>
<td><p>192</p></td>
</tr>
<tr class="odd">
<td><p>1.2</p></td>
<td><p>6,000</p></td>
<td><p>396</p></td>
<td><p>384</p></td>
</tr>
<tr class="even">
<td><p>1.3</p></td>
<td><p>11,880</p></td>
<td><p>396</p></td>
<td><p>768</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>11,880</p></td>
<td><p>396</p></td>
<td><p>2,000</p></td>
</tr>
<tr class="even">
<td><p>2.1</p></td>
<td><p>19,800</p></td>
<td><p>792</p></td>
<td><p>4,000</p></td>
</tr>
<tr class="odd">
<td><p>2.2</p></td>
<td><p>20,250</p></td>
<td><p>1,620</p></td>
<td><p>4,000</p></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td><p>40,500</p></td>
<td><p>1,620</p></td>
<td><p>10,000</p></td>
</tr>
<tr class="odd">
<td><p>3.1</p></td>
<td><p>108,000</p></td>
<td><p>3,600</p></td>
<td><p>14,000</p></td>
</tr>
<tr class="even">
<td><p>3.2</p></td>
<td><p>216,000</p></td>
<td><p>5,120</p></td>
<td><p>20,000</p></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p>245,760</p></td>
<td><p>8,192</p></td>
<td><p>20,000</p></td>
</tr>
<tr class="even">
<td><p>4.1</p></td>
<td><p>245,760</p></td>
<td><p>8,192</p></td>
<td><p>50,000</p></td>
</tr>
<tr class="odd">
<td><p>4.2</p></td>
<td><p>522,240</p></td>
<td><p>8,704</p></td>
<td><p>50,000</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>589,824</p></td>
<td><p>22,080</p></td>
<td><p>135,000</p></td>
</tr>
<tr class="odd">
<td><p>5.1</p></td>
<td><p>983,040</p></td>
<td><p>36,864</p></td>
<td><p>240,000</p></td>
</tr>
</tbody>
</table>

## 利用例

H.264は下記の放送・規格で採用されている。なお、[日本の地上デジタルテレビ放送](https://ja.wikipedia.org/wiki/日本の地上デジタルテレビ放送 "wikilink") (ISDB-T) では、[MPEG-2](../Page/MPEG-2.md "wikilink")が採用されているが、H.264は[ISDB-T方式を改良した](https://ja.wikipedia.org/wiki/ISDB#ISDB-T（地上波） "wikilink")、[ブラジル](https://ja.wikipedia.org/wiki/ブラジル "wikilink")の[SBTVD方式の他](https://ja.wikipedia.org/wiki/ISDB#SBTVD "wikilink")、[DVB-T](https://ja.wikipedia.org/wiki/DVB-T "wikilink")方式の一部で採用されている。

### [デジタル放送](../Page/デジタル放送.md "wikilink")方式

  - [DVB-T](https://ja.wikipedia.org/wiki/DVB-T "wikilink")
  - [DVB-S2](https://ja.wikipedia.org/wiki/DVB-S2 "wikilink")
      - [スカパー\!プレミアムサービス](../Page/スカパー!プレミアムサービス.md "wikilink")
  - [ISDB](../Page/ISDB.md "wikilink")
      - [SBTVD (ISDB-TB)](https://ja.wikipedia.org/wiki/ISDB#ISDB-T_International "wikilink")
      - [ワンセグ](../Page/ワンセグ.md "wikilink")
      - [NOTTV](https://ja.wikipedia.org/wiki/NOTTV "wikilink")（[2016年](../Page/2016年.md "wikilink")6月終了）
  - [DMB](../Page/DMB.md "wikilink")
      - [モバHO\!](../Page/モバHO!.md "wikilink")（[2009年](../Page/2009年.md "wikilink")3月終了）

### マルチメディア規格

  - [QuickTime](../Page/QuickTime.md "wikilink") 7 - QuickTime 7 PlayerではH.264の再生、QuickTime 7 ProではH.264への変換が出来る
  - [Adobe Flash Player](../Page/Adobe_Flash.md "wikilink") 9 - 2007年8月21日、H.264対応版発表
  - [Microsoft Silverlight](../Page/Microsoft_Silverlight.md "wikilink") - 2009年7月にリリースされたSilverlight 3でH.264に対応
  - [DivX](https://ja.wikipedia.org/wiki/DivX "wikilink") - バージョン7のDivX Plus HDでH.264を採用
  - [Nero Digital](https://ja.wikipedia.org/wiki/Nero_Digital "wikilink")
  - [メモリースティックビデオ](../Page/メモリースティックビデオ.md "wikilink")ファイルフォーマット
  - [ユニバーサル・メディア・ディスク](../Page/ユニバーサル・メディア・ディスク.md "wikilink") (UMD)
  - [AVCHD](../Page/AVCHD.md "wikilink")
  - [AVCREC](../Page/AVCREC.md "wikilink")
  - [HD Rec](../Page/HD_Rec.md "wikilink")

また、下記の規格にも映像[コーデック](../Page/コーデック.md "wikilink")のひとつとして採用された。

  - [Blu-ray Disc](../Page/Blu-ray_Disc.md "wikilink")
  - [HD DVD](../Page/HD_DVD.md "wikilink")

### 動画コンテンツ

  - [Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")（[みんなのニンテンドーチャンネル](../Page/みんなのニンテンドーチャンネル.md "wikilink")）
  - [アクトビラ](../Page/アクトビラ.md "wikilink")

### 動画共有サービス

現在、ほとんどの[動画共有サービス](../Page/動画共有サービス.md "wikilink")は、[Flash Video](../Page/Flash_Video.md "wikilink") (flv) とH.264 (mp4) を使用している。

  - [ニコニコ動画](../Page/ニコニコ動画.md "wikilink") - 2008年7月5日より600kbpsまでのH.264動画を一般会員も投稿可能、有料会員はビットレート無制限で投稿可という仕様だったが、2016年12月08日から一般会員もビットレート無制限になった。
  - [Dailymotion](../Page/Dailymotion.md "wikilink") - フランスの動画共有サイト。ヨーロッパの動画共有サービスでは最初に対応したという。
  - [eyeVio](https://ja.wikipedia.org/wiki/eyeVio "wikilink") - H.264によるハイビジョン動画配信・eyeVio HD PROを2008年7月より開始した。
  - [PANDORA.TV](../Page/パンドラTV.md "wikilink") - 韓国の動画共有サイト。
  - [Veoh](../Page/Veoh.md "wikilink") - アメリカの動画共有サイト。H.264動画を無制限容量で投稿可能。
  - [Youku](../Page/Youku.md "wikilink") - 中国の動画共有サイト。
  - [YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink") - 以前はビデオコーデックが[H.263](../Page/H.263.md "wikilink")（音声[MP3](../Page/MP3.md "wikilink")）だったが、2011年ごろからはH.264（音声[AAC](../Page/AAC.md "wikilink")）のデータ形式が標準となっていた。2018年現在、[VP9](https://ja.wikipedia.org/wiki/VP9 "wikilink")（音声[Opus](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink")）への再エンコードが進んでおり、[4Kは](https://ja.wikipedia.org/wiki/4K解像度 "wikilink")[VP9](https://ja.wikipedia.org/wiki/VP9 "wikilink")でしか視聴できない。
  - [zoome](https://ja.wikipedia.org/wiki/zoome "wikilink") - 3,000 kbpsまで（音声込みの上限値）のH.264動画を完全無料（[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[8月1日](../Page/8月1日.md "wikilink")に有料化）で投稿可能。[2007年](../Page/2007年.md "wikilink")[12月20日](../Page/12月20日.md "wikilink")より。日本の動画投稿サイトで最初に対応した。[2011年](../Page/2011年.md "wikilink")[8月31日](../Page/8月31日.md "wikilink")をもって終了。

### 通信

  - [JNN次世代HD](https://ja.wikipedia.org/wiki/Japan_News_Network "wikilink") [SNG](../Page/SNG_\(放送\).md "wikilink")[中継車](../Page/中継車.md "wikilink") - HD対応のテレビ中継車。[DVB-S2方式を使用](https://ja.wikipedia.org/wiki/デジタルビデオブロードキャスティング#衛星用 "wikilink")\[1\]。2008年12月よりJNN系列局で順次導入。
  - NHK[お天気カメラ](../Page/お天気カメラ.md "wikilink")・[情報カメラ](https://ja.wikipedia.org/wiki/情報カメラ "wikilink") - IP回線を使い[NHK放送センター](../Page/NHK放送センター.md "wikilink")と[NHK大阪放送局](../Page/NHK大阪放送局.md "wikilink")に伝送\[2\]。

その他、海外スポーツイベントの生中継等でも使用。

## ライセンス

H.264には多数の[特許](../Page/特許.md "wikilink")権が含まれており、本規格を採用したハードウェア製品やソフトウェア製品を製造する企業は、特許使用料であるパテント料の支払いが求められる。これらの[ライセンス](../Page/ライセンス.md "wikilink")に関する管理は、[パテントプール](https://ja.wikipedia.org/wiki/パテントプール "wikilink")である[MPEG-LAコンソーシアム](https://ja.wikipedia.org/wiki/MPEG-LAコンソーシアム "wikilink")が特許権者からの委託を受けて業務を代行している。

"H.264"を採用した製品を購入した消費者は個別に使用料を請求されることはないが、製品価格にそれらのコストが含まれることになる。

2013年10月30日、米Cisco Systemsより、同社によるH.264の実装をオープンソース化、無償でダウンロードできるようにするとの発表。 このオープンソースを利用するにあたりMPEG-LAコンソーシアムへのライセンス料はCiscoが負担する。 BSDライセンスにより公開中。  

## 競合方式

MPEG-2の2倍以上の圧縮効率を持つとされる動画圧縮規格には、H.264の他にも米[マイクロソフト](../Page/マイクロソフト.md "wikilink")社が開発した[VC-1](../Page/VC-1.md "wikilink") ([Windows Media Video](../Page/Windows_Media_Video.md "wikilink") 9) がある。H.264とVC-1は同一ビットレートで同等の画質性能であるという意見がある。

  - VC-1
    2003年、マイクロソフト社は"WMV9"の基本アルゴリズムにインタレース映像への対応を加えた仕様を"VC-9"と命名して、米国映画テレビ技術者協会 ([SMPTE](../Page/SMPTE.md "wikilink")) に提出した、これは後に名称が"VC-1"に改められた。VC-1はH.264と共に[HD DVDと](../Page/HD_DVD.md "wikilink")[Blu-ray Discでの動画圧縮規格として採用された](../Page/Blu-ray_Disc.md "wikilink")。"H.264"は非常に多数の複雑な符号化ツールで構成されており、VC-1に比べてエンコーダもデコーダも処理負荷が増す傾向があるが、H.264はITU-TおよびISO/IECといった国際標準化団体の規格であるため、世界中の多くの企業が支持を表明し、製品に採用されている。また、デジタルTVやパソコン等に用いられる画像処理半導体の処理能力向上に伴って、負荷の重さは以前ほど問題にならなくなってきている。

## ウェブブラウザ

PCの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")では[Adobe Flashを通じて広く利用されている](../Page/Adobe_Flash.md "wikilink")。[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")などでは動画フォーマットの選択制限が厳しいこともあり、[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となっている。

ウェブ表示の次世代規格である[HTML5](../Page/HTML5.md "wikilink")にはvideo要素で動画再生を行う機能が盛り込まれており、これに使用する動画フォーマットについて、ウェブブラウザ[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")の[アップルと](../Page/アップル_\(企業\).md "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")はH.264を推進しているが、[Mozilla Foundationと](../Page/Mozilla_Foundation.md "wikilink")[オペラ・ソフトウェア](https://ja.wikipedia.org/wiki/オペラ・ソフトウェア "wikilink")、[Google](../Page/Google.md "wikilink")は[ロイヤリティ](https://ja.wikipedia.org/wiki/ロイヤリティ "wikilink")が発生する点などを問題視し、積極的な利用に難色を示していた。2016年4月現在では、[Safari](../Page/Safari.md "wikilink")、[Internet Explorer](../Page/Internet_Explorer.md "wikilink")、[Mozilla FirefoxはH](../Page/Mozilla_Firefox.md "wikilink").264をサポートしているが、[Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")ではサポートしていない。

Mozilla FoundationはかつてH.264をサポートしていなかったため、反発した一部の有志が、Mozilla FirefoxにH.264サポートを追加したウェブブラウザを提供することを目的としたプロジェクトを立ち上げた\[3\]。これはH.264に関する特許が成立していない国のユーザに向けたもので、特許が成立している国のユーザは事実上使うことはできない。2012年、Mozilla FoundationはH.264のサポートを表明した\[4\]。

マイクロソフトはMozilla FirefoxでH.264を再生できるようにするアドオンを公開している\[5\]。これは動的にvideo要素をobject要素に書き替えるという力業で実現しており、video要素固有のAPIが利用できなくなるという仕組み上の欠点を抱えている。

## 脚注

## 参考図書

  -
  -
  -
## 関連項目

### ハードウェア

  - [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")
  - [Apple TV](../Page/Apple_TV.md "wikilink")
  - [PSP](../Page/PlayStation_Portable.md "wikilink")

### ソフトウェア

  - [Silverlight](https://ja.wikipedia.org/wiki/Silverlight "wikilink")

<!-- end list -->

  - [x264](https://ja.wikipedia.org/wiki/x264 "wikilink")
  - [ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")

<!-- end list -->

  - [Flash Player](../Page/Adobe_Flash.md "wikilink")
  - [AVC-Intra](https://ja.wikipedia.org/wiki/AVC-Intra "wikilink")

### 関連団体

  - [ISO/IEC JTC 1](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")

### その他

  - [動画](../Page/動画.md "wikilink")
  - [データ圧縮](../Page/データ圧縮.md "wikilink")

## 外部リンク

  - [リファレンスソフトウェア](http://iphome.hhi.de/suehring/tml/)
  - [規格書](http://www.itu.int/rec/T-REC-H.264/e)
  - [米Cisco Systems OpenH264](http://www.openh264.org/)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:MPEG](https://ja.wikipedia.org/wiki/Category:MPEG "wikilink")

1.  関昭一・井下雅美「「JNN次世代HD-SNG中継車」標準仕様車について」、『放送技術』第67巻（2014年5月号）、兼六館出版、2014年5月、 ISSN 0287-8658
2.  平樹・田嶋亨「ロボットカメラモニタリングシステムの更新」、『放送技術』第62巻（2009年3月号）、兼六館出版、2009年3月、 ISSN 0287-8658
3.  [Wild Fox Project](http://wildfox.sourceforge.net/)
4.  [Mozilla が H.264 をサポートへ、webM 一本化を断念](http://japanese.engadget.com/2012/03/20/mozilla-h-264-webm/) [Engadget](https://ja.wikipedia.org/wiki/Engadget "wikilink") 2012年03月20日
5.  [HTML5 Extension for Windows Media Player Firefox Plug-in](http://www.interoperabilitybridges.com/html5-extension-for-wmp-plugin) Interoperability Bridges and Labs Center