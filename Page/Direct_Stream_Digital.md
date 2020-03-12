> この記事は[Direct Stream Digital](https://ja.wikipedia.org/wiki/Direct_Stream_Digital)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:PCM-vs-DSD.svg "wikilink") **ダイレクトストリームデジタル**（）とは、[スーパーオーディオCD](../Page/Super_Audio_CD.md "wikilink")（SACD）で使用されている[アナログ](../Page/アナログ.md "wikilink")音声を[デジタル](../Page/デジタル.md "wikilink")信号化する際の方式についての[ソニー](../Page/ソニー.md "wikilink")と[フィリップス](../Page/フィリップス.md "wikilink")による商標である。[CD](https://ja.wikipedia.org/wiki/CD "wikilink")や[DVD](../Page/DVD.md "wikilink")で使用されている[パルス符号変調](../Page/パルス符号変調.md "wikilink") (PCM) ではなく[パルス密度変調](https://ja.wikipedia.org/wiki/パルス密度変調 "wikilink") (PDM) を用いているのが特徴である（[ΔΣ変調](../Page/ΔΣ変調.md "wikilink")）。

PCM方式とは異なり[ビット深度が](https://ja.wikipedia.org/wiki/ビット深度_\(音響機器\) "wikilink")1bitである代わりにサンプリング周波数を大きく取る。例えば、DSD64フォーマットのサンプリング周波数は2.8224MHzであるが、これはCD-DAの規格である44.1kHzの64倍にあたる。（一方、CD-DAのビット深度が16bitであり、DSDのビット深度は1bitであるため、非圧縮の場合の[ビットレート](../Page/ビットレート.md "wikilink")は4倍となる。）DSD128のサンプリング周波数は44.1kHzの128倍である5.6MHz（もしくは48kHzの128倍である6.144MHz）、DSD256のサンプリング周波数は44.1kHzの256倍である11.2896MHz（もしくは48kHzの256倍の12.288MHz）、DSD512のサンプリング周波数は22.5792MHz（または24.576MHz）である。

## 特徴

### 長所

100kHzまでカバーする周波数帯域（ただしフラットではなく上限に向かって下降する特性）と低ノイズ、瞬発力の高さ、そして音の情報量が多いにも関わらず周波数帯域が近い192kHzサンプリングと比較した場合データが軽く済むという特長がある。

また、DSDからのDA変換もアナログローパスフィルターを通すだけの非常にシンプルなハード設計が可能で、アナログ→DSD変換のLSIのコストが低く消費電力も抑えられるので、SACDや録音だけでなくデジタル[パワーアンプ](https://ja.wikipedia.org/wiki/パワーアンプ "wikilink")にも使われている。

### 短所

#### 高周波数帯での量子化ノイズ

短所としては、まず「高周波数になるほど量子化ノイズが増える」というものがある。この特性によりSACDの製品化初期の頃、スーパーツイーターの破損が頻発したため、現在では35kHz～45kHz程度の[ローパスフィルタ](../Page/ローパスフィルタ.md "wikilink")を搭載した再生機器が一般的であり、実際に100kHzは再生されない。なお、サンプリング周波数が非常に高いので、[人間が聴取可能な周波数帯域という意味ではこの問題は感知されない](https://ja.wikipedia.org/wiki/聴覚#可聴域 "wikilink")。変換誤差や高調波ひずみが発生しやすいという点は回路設計上大きな課題となっている。

#### 高速伝送の必要性

もう一つの短所としては、DSDの特性上ケーブルも1ビットを高速伝送するシリアル系のケーブルでなければ正確な伝送が出来ない点である。パラレル系でもシリアル系ケーブルでも正確な伝送が可能なPCMとの大きな違いでもある。実際にパイオニアやソニーなどのメーカー各社では、SACDとAVアンプとをデジタルにてシリアル伝送するためにiLINKを採用していた。

#### 後処理を行う上での制限

制作側から見た場合、1bit・ΔΣ変調の原理からミキシングはおろか[イコライジングさえ出来ず](../Page/イコライザー_\(音響機器\).md "wikilink")、2対ないし4対パラレルでマルチビット伝送するLANケーブルを用いるDante規格などのパラレル系機器が（制作音源の品質上）使い物にならない。現状では光ファイバーを用いるMADI規格か[thunderbolt](https://ja.wikipedia.org/wiki/thunderbolt "wikilink")対応機器を使用して伝送する、[Pyramix](http://dspj.co.jp/products/merging/pyramix.htm)やSonomaなどのマルチトラックダイレクトストリームデジタル録音システムを用いながらミキシング／イコライジングなどのプロセスはアナログ機器に頼るか、DSD-Wide、などのマルチビット信号にデジタル変換して行われている。

## DSDの記録方式

記録方式には以下の方法が存在している。DSD規格では以下のいずれかの方法が用いられている。そのため、SACDのソフトによっては、録音・記録方法が異なっている。

  - DSDレコーディング
    オリジナルレコーディングからすべてDSD方式で録音されているマスターを使用。 DSD方式で音楽情報を余すことなく録音することで、 DSDの持つ高いサウンドクオリティをスーパーオーディオCDで再現することが可能。
  - DSDミキシング
    アナログあるいはデジタルのマルチチャンネル・レコーダーから直接DSDにミックスダウンされたマスターを使用する方式。スーパーオーディオCDでは、ミキシングによって増大するダイナミックレンジやリミッタ処理によって発生する高調波などもそのまま収録することが可能となった。
  - DSDマスタリング
    アナログあるいはデジタルのオリジナルマスターから、直接DSD方式でマスタリングしたマスターを使用。例えばハイビット・ハイサンプリングのマスターのサウンドも品質を損なわずにスーパーオーディオCDに収録可能。

## DSDディスク

後述のDSFファイルをDVD±R、DVD±RWに記録するためのフォーマット。「Sound Reality」搭載の[VAIO](../Page/VAIO.md "wikilink")および[KORGのPC用アプリケーションソフト](https://ja.wikipedia.org/wiki/コルグ "wikilink")「AudioGate」で作成することができるほか、音楽配信サイトからDSD音源を購入し、市販のライティングソフトでDVD±R、DVD±RWに記録して作成することもできる。

[SACD](https://ja.wikipedia.org/wiki/SACD "wikilink")とは完全に別物であるため、通常のSACDプレーヤーで再生することはできないが、ソニーのSCD-XA5400ESやSCD-XE800など一部のSACDプレーヤー、[ティアック](../Page/ティアック.md "wikilink")のPD-501HRなど一部のCDプレーヤー、[SIEの](https://ja.wikipedia.org/wiki/ソニー・インタラクティブエンタテインメント "wikilink")[プレイステーション3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")（SACD再生非対応モデルを含む）は再生に対応している。なおDSDディスクをVAIOで製作した場合、PCMへ変換出力するDirectShowプラグインが書き込まれているため、DSD対応機能「Sound Reality」搭載のVAIO以外のPCでも（PCMとしてではあるが）再生できる。

## ファイルフォーマット

DSDには様々なファイルフォーマットが存在している。いずれにおいても互換性はない。

  - DSDIFF (Direct Stream Digital Interchange File Format)
    主に業務用に用いられており、DSDファイルフォーマットの中で最も使われている。PyramixやSonomaなどの業務用機器に対応製品が多い。民生用では、KORGのPC用アプリケーションソフト「AudioGate」か同社のレコーダー（MRシリーズ）、TASCAMのレコーダーなどで再生できる。
  - DSF (DSD Stream File)
    ソニーが2005年秋モデルのVAIO向けに開発した民生用途向けファイルフォーマット。「Sound Reality」搭載のVAIOに付属しているソフトウェア「DSD Direct」を用いることによりWAVから変換でき、DSDディスク作成に用いられる。再生には「Sound Reality」搭載のVAIO、あるいはKORGのPC用アプリケーションソフト「AudioGate」か同社のMRシリーズで再生可能。
  - WSD (Wideband Single-bit Data)
    「1ビットオーディオコンソーシアム（[早稲田大学](../Page/早稲田大学.md "wikilink")と[パイオニア](https://ja.wikipedia.org/wiki/パイオニア "wikilink")、[シャープ](../Page/シャープ.md "wikilink")共同の推進グループ）」が策定したファイル・フォーマット。チャンネル数やサンプリング周波数に制限がなく、あらゆる形式のデータに対応できることを特長としている。仕様が公開されているのも特徴である。KORGのPC用アプリケーションソフト「AudioGate」か同社のMRシリーズで再生可能。

## 関連項目

  - [音響機器](../Page/音響機器.md "wikilink")
  - [ΔΣ変調](../Page/ΔΣ変調.md "wikilink")
  - [ハイレゾリューションオーディオ](https://ja.wikipedia.org/wiki/ハイレゾリューションオーディオ "wikilink")
      - [Super Audio CD](../Page/Super_Audio_CD.md "wikilink")

      - [DVD-Audio](../Page/DVD-Audio.md "wikilink")

      -
[Category:通信工学](https://ja.wikipedia.org/wiki/Category:通信工学 "wikilink") [Category:ソニー](https://ja.wikipedia.org/wiki/Category:ソニー "wikilink") [Category:音声処理](https://ja.wikipedia.org/wiki/Category:音声処理 "wikilink") [Category:デジタルオーディオ](https://ja.wikipedia.org/wiki/Category:デジタルオーディオ "wikilink") [Category:登録商標](https://ja.wikipedia.org/wiki/Category:登録商標 "wikilink")