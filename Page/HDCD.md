> この記事は[HDCD](https://ja.wikipedia.org/wiki/HDCD)から翻訳されています。


**HDCD** (High Definition Compatible Digital)は、ディザ技術・非直線量子化技術および隠しコード化技術を用いて、20bit〜24bit音源を自然な音質で、なおかつ聴感上のノイズを低下させつつ音量感を伴う音で16bit化し聴取するしくみである。

## 特徴

A/D変換器や語長の丸めには量子化雑音の分布が平坦となる回路を採用していることが特徴である。 HDCD盤はコンパクトディスク（CD）と完全な互換性を有するが、HDCDデコーダーを有した機器で再生するとHDCD盤であることが表示される。また、この**HDCD盤からリッピングした音源を再生する場合でもHDCDエンコード音源である**ことが表示される。これは、16bit信号の中にHDCDエンコード音源であることを示す隠しコードが埋め込まれ、再生時にはデコーダーで復調されることで判別される。

HDCDには、PeakExtensionやLowLevelExtendと呼ばれる付加機能もある。 ピークエクステンションとは、波形尖塔部を鈍らせて記録することによって録音レベルを上昇させ、充分な音量感を得るしくみである。 ローレベルエクステンドとは、微少レベルの音楽信号を嵩上げ記録し、再生時には元の記録レベルに戻すことによりノイズリダクション効果を得るしくみである。

HDCDの基本回路は1986年〜1991年の間にマイケル・プラウマー及びキース・ジョンソン等が考案し、HDCDエンコーダー（Model1）、HDCDデコーダー（PMD100）、HDCDデモCD（RR-S3CD）は既に1994年に発売されていたが、1996年に設立された米国パシフィック・マイクロソニックス社が開発した技術と紹介される場合が多い。

## 基本機能

音源を自然な音質で収録・再生するために量子化雑音の分布が平坦となる回路を採用していることが特徴で、内蔵A/D変換回路には4倍オーバーサンプリング20bit逐次比較型が用いられ、16bitに丸める際には高域集中ディザが用いられる。A/D変換器はマルチビット逐次比較型を採用することでノイズフロアの平坦性を確保し、自然な音色で記録できる。HDCDエンコーダーには外部A/D変換ユニットのデジタル信号も入力可能なためノイズシェーピングを用いたデータもHDCDエンコードすることはできるので、HDCD盤であれば必ずノイズフロアが平坦であるとは限らない。⊿Σ型A/D変換器を用いて収録した音源でもノイズフロアが平坦な場合もあるので、HDCDエンコーダー内蔵逐次比較型A/D変換回路を使わねばならない訳ではない。

ダイナミック フィルタ プロセスと呼ばれる可変LPF技術は、リアルタイムに音楽成分のスペクトラムを観測し、高域エネルギー成分の有無によって、A/D変換回路の折り返しノイズ防止用プリフィルターを可変することで常時高次LPFが挿入されることによる特性劣化を防ぐためのしくみである。現在では一般的な、高速標本化で得た低bit信号の量子化雑音の分布を⊿Σ変調器を用いて整形するA/D変換回路とは異なり、4倍オーバーサンプリング20bit逐次比較型A/D変換回路を用いているが、この機能によって低速標本化A/D変換回路における高次LPF挿入の弱点を克服している。高速標本化⊿Σ型A/D変換回路を使用する場合には、ダイナミック フィルタ プロセスは働かない。

24bit\~20bit音楽信号をCDフォーマットの16bitに丸める際に高域集中ディザを採用することによってグラニュラーディストーションを回避しつつ聴感S/Nを確保する。 HDCDエンコード音源の量子化雑音分布をみると、16kHzまでは平坦なノイズフロアとなっていることが判る。16kHz以上の帯域は人間の耳には感度が低いので気付かないが、高域集中ディザが記録されているのでノイズフロアが上昇している。 ディザを用いて16bitに語長が丸められたデータはデコーダーが無くとも一般のCDプレーヤーで再生可能なので、汎用性・互換性の高いシステムと紹介されることが多い。「減算型ディザ A/D 変換」と紹介している場合があるが、16kHz以上の帯域に発生させた高域ノイズはCD盤上に記録され、D/A変換回路で再生されるので、ここでいう高域集中ディザはA/D変換回路内で用いられるディザではなく、あくまでも20bit〜24bit音源を16bitに丸める際の高域集中ディザのことである。しばしば16bitへの語長丸めについて、「CD でのエンコードに 4 ビット分をプラスする」という説明を行っている場合が散見されるが、これは誤りである。HDCDプロセスで用いられるのはあくまでもディザであり、20bit語長を16bitに丸める仕組みなので4bit分をプラスする訳ではない。

HDCD判別信号の隠しコードをデータ内に埋め込む技術によってHDCD盤と通常CDを判別する機能を有している。 「HDCDは16bitの中の1bitに20bitや24bitのデータを記録再生する」、という記述も散見されるが、これは誤りである。「20bitの情報を圧縮して16bitに置き換え、再生時に再び20bitに近い形に戻す」、という説明も見られるが、これも誤りである。16bit以上の符号を非直線量子化などにより16bit中の1bitに記録している訳ではない。16bit以上のダイナミックレンジを記録再生できるというのは、高域集中ディザを用いて20bitや24bitのハイビットPCMデータを16bitに語長丸めを行なうという仕組みを指す。16bitデータに記録されているのはHDCD判別符号であるが、この隠しコード記録方法を16bit以上のハイビット分解能データを記録していると誤解されることが多い。また、この判別符号は常時記録再生されているわけではなく間欠的に記録されている。この「ハイビット音源を16bitに丸める」、という部分はソニーが行っているSBM（スーパービットマッピング）やロンドン・デッカが行っているPONS（サイコアコースティカリー・オプチマム・ノイズシェーピング）と同様なプロセスであるが、SBMやPONSはノイズシェーピングを用いて、人間の聴覚が敏感な帯域の量子化ノイズフロア形状を窪ませているのに対して、HDCDの高域集中ディザは16kHzまでは平坦であるというところが異なる。

## オプション機能

（楽曲の傾向によって向き不向きがあるので、下記機能を用いて制作されたHDCD盤は極めて少ない。）

  - ピークエクステンション回路

音楽信号編集時に非直線量子化を応用したコンプ回路を用いて、0dBを超える+9dB相当の波形のピーク部分を、アナログテープレコーダーと近似な飽和特性によって丸めることで平均音圧レベルを高める機能。通常のCDプレーヤーでHDCD盤を再生すると、波形尖塔部はマスタリング時に鈍らせた波形で再生されるが、HDCDデコーダー搭載CDプレーヤーではマスタリング時に鈍らせた以前の波形が非直線量子化によって波形が復元され再生される。 （しばしばHDCD盤は楽曲のピークを鈍らせているので圧縮された音になる、との誤解も多いが、CDマスタリング時に波形尖塔部を鈍らせるという作業は、一般のCDソフト制作時にも多用されている。しかしHDCD盤としてマスタリングされたCD盤は、鈍らせた前の波形尖塔部が再生されるというメリットを有する。）

  - ローレベルエクステンド回路

楽音レベルがある一定以下の音量が連続した場合、ローレベル信号をブーストして記録し、HDCD再生時には元の信号レベルで再生されることによってノイズを抑えダイナミックレンジを拡大する機能。

## エンコーダーの基本構成

HDCDエンコーダーは、「A/D変換回路」－「HDCDエンコーダー回路」－「D/A変換回路」という3つの構成から成り立っている。

A/D変換回路のデシメーションフィルターの出力bit数は20bitであるが、HDCDエンコーダーの入出力インターフェースは24bitである。内蔵A/D変換回路を使わず外部のユニットを接続しデジタル入力することも可能である。HDCDエンコーダーは標本化周波数44.1kHzに対応したModel1と、ハイサンプリング88.2kHz及び96kHzに対応したModel2の2機種が販売されていたが、現在は製造中止となっている。

## 過去行われてきた急峻なLPFが必要とされる低速標本化A/D変換回路の改善方法

キース・ジョンソンはリファレンス・レコーディングス社を経営し、SONY製PCMエンコーダーユニットを用いて数々のクラシック音楽のレコーディングを手掛けていた。このPCMエンコーダーは二重積分型A/D変換回路を採用していたので、折り返しノイズ防止用アンチエイリアス・アナログフィルターは急峻な減衰特性だった。このため次数が大きいLPFが常時挿入されるので位相が回転してしまうという欠点があった。

しかしジョンソンは、「音楽ホールで演奏されるクラシック音楽の場合には高い周波数成分はそれ程無い」と考えたので、Apogee社製244GというLPFに換装して改造して使用していた。244Sという、本来A/D変換器に用いる急峻な特性のLPFもあったが、位相回転を嫌い、あえて244Gを用いていた。（Gはジェントル、Sはシャープの略）

## HDCDプロセス

### A/D変換

まず、アナログ信号は、4倍オーバーサンプリング・マルチビット逐次比較型A/D変換回路で20bit176.4kHzでデジタル符号化される。 その後標本化周波数は1/2の88.2kHzに間引かれた後で1/4の44.1kHzにデシメーションされる。デシメーション回路ICは20bitだが、インターフェースは24bitに対応している。

現在主流の⊿∑変調器を用いた高速標本化低bitA/D変換回路に比較するとノイズフロアが平坦なので、どのようなパワースペクトル密度を有する楽曲でも“キャラクター”が付くことなく自然な音質で収録できるという利点がある。しかし、4倍という低速な標本化周波数であるためにLPFは急峻な減衰特性を要求されるという弱点があるが、この課題に関してHDCDはLPF次数を可変させる回路で対処した。常時入力信号の高域特性を監視し、高域信号が弱い場合にはLPF次数を短くし、減衰特性は比較的緩やかな特性とする。パルシブな信号が入力された時は急峻なLPFが挿入される。コンサートホールで収録するクラシック音楽などでは、元々のアナログ信号の高域エネルギーは小さいので、常時急峻なフィルターを挿入する必要は無いと考えた訳である。

### HDCDエンコード

CDソフトを制作する場合にはHDCDエンコードユニット内のA/D変換回路で変換された20bitデータを16bitに切り詰める必要があるが、HDCDでは人間の聴覚感度の低い16kHz以上の帯域にランダムノイズを集中させる“高域集中ディザ”を用いることによって、量子化語長を丸める際のグラニュラーディストーションを抑えた。A/D変換器が逐次比較マルチビット回路であり、量子化語長を丸める際には再量子化ノイズのパワースペクトラムを人間の聴覚感度に合わせて窪ませるノイズシェーピングは用いていないので、人間の耳では敏感な16kHzまでのノイズフロアは平坦とすることができた。

オプションの機能である“ピークエクステンション”を用いると、+9dBまでの波形尖塔部をアナログテープレコーダーが有するソフトクリップ特性でコンプすることができる。HDCDエンコード信号を通常のD/A変換ユニットで再生すると、波形尖塔部はソフトクリップ特性のまま再生されるが、HDCD対応D/A変換回路で波形尖塔部を再生すると、非直線量子化で再生することによって元の+9dB波形が復活再生される。また、小さな信号レベルが連続する場合には“ローレベルエクステンド機能”を用いると音量嵩上げ回路が働き、一種のノイズリダクション効果によってシステムノイズを低く高S/Nで音楽を収録再生することができる。一部の説明では、「ピーク エクステンション モードの復元可能で柔軟な制限により、最大 6 db まで信号レベルを上げることで、解像度を高めている」という説明を行なっているが、解像度が高められているのではなく、非直線量子化によって鈍らせた波形尖塔部が元の尖塔波形に復元される。また、ピークエクステンションは、楽曲全体を通じての記録レベルが低めで、ごく短時間のレベルが高まる場合に用いられる。ローレベルエクステンドについても、音楽の傾向によっては向き不向きがあるので、この機能を用いたHDCD盤は極めて少ない。このため、この6dB増幅記録/減衰再生を1bit分の解像度向上として説明することは誤りである。「高度なシステムを使用して、CD でのエンコードに 4 ビット分をプラスする」という説明を行なっている場合があるが、これはHDCDは高域集中ディザを用いてCDの16bitとするという基本的な仕組みを理解していないために、上記のような誤解を生じ易い解説をしていると思われる。

これらのHDCD回路動作判別は、隠しコマンド化されてディザ信号の中に記録されている。この隠しコードをHDCDデコード回路で検出することで16bit直線量子化の範囲を超えたダイナミックレンジを確保することができるわけである。

HDCDエンコードされたCDの44.1kHz16bit符号をリッピングし、そのデジタル音楽信号をそのままコピーしても判別信号は消失しないが、音量や音質を調整したり標本化周波数を変換すると隠しコードは消失する。

### HDCD音源の編集およびマスタリング・HDCD盤のプレス製造

HDCD音源を編集する場合、調整卓のフェーダーやエフェクト機能を用いるとHDCD音源に埋め込まれたHDCD判別用隠しコードが離散してしまう。このような編集を行った音源をCD盤としてプレスし再生した場合、HDCD判別用インジケーターが点滅したり点灯しなくなったりする。HDCD音源を編集した場合には、再度、そのデータをHDCDエンコーダーに入力し、隠しコマンドを打ち込まなければならない。

### HDCDデコーダー内蔵デジタルフィルター

HDCDデコーダーはD/A変換ユニット内部のオーバーサンプリングデジタルフィルター回路に内蔵されている。 初期のHDCDデコーダー内蔵デジタルフィルターは、パシフィックマイクロソニックス社製PMD-100が供給され、米国マークレビンソン社を始めとする高級CDプレーヤーD/A変換ユニットに搭載されていた。（PMD100の日本での代理店は高千穂交易） また、1999年にバーブラウン社からD/A変換回路も内蔵し、96kHz24bitハイビットハイサンプリングに対応したDAC-ICも発売されたが、このPCM1732は⊿Σ変調回路を用いたD/A変換部を搭載しており、基本クロックの設定によっては通過帯域内のノイズフロアが平坦ではなくなるという使いこなし上の課題を有した。 数年後、モトローラ社製DSP56300をベースにハイビットハイサンプリングに対応したHDCD単体デジタルフィルターPMD200が発売されたが、この時期にモトローラ社の半導体DSP事業はオン・セミコンダクター社へ事業譲渡され、パシフィックマイクロソニックス社のHDCD関連事業もマイクロソフト社へ身売りしてしまったのでPMD200はごく一部のメーカーが採用したに留まった。その後、アナログデバイセス社製SharcDSPにHDCDデコード回路が搭載され、今日に至る。

### HDCD盤（コンパクトディスク）およびHDCD音源（wavefile）の再生とデコード

本来、HDCD対応機器はパシフィックマイクロソニックス社のライセンスを受けて製造されるが、一部メーカーは独自ルートでPMD100を入手し製品に搭載していた。この欧州メーカーの製品ではライセンス上義務づけられていたHDCDロゴ記載やHDCDインジケーターは無く、デジタルインターフェースレシーバーICであるクリスタルセミコンダクターズ社製CS8412の後ろにアナログデバイセズ社製ASRC非同期サンプリングコンバーターであるAD1890を設け、クロックを打ち直していた。AD1890の出力をPMD100に入力していたために、HDCD隠しコマンドを検出することが出来ずにピークエクステンションやローレベルエクステンションなどのHDCD特有の機能が動作しておらず、単なる8倍オーバーサンプリングデジタルフィルターとして機能していた。HDCD判別信号は元の16bit音源の中に隠しコマンドとして記録されているために、fs変換回路を通過した際に隠しコマンドが消失してしまったわけである。 また、当時発売されていたCD-Rレコーダー/プレーヤーの中には、常時fs変換回路が動作していたモデルもあったために、このメーカーのCD-RでHDCD盤をコピーするとHDCD判別信号が消滅してしまうということもあった。 この点では最近普及しているパソコンへのリッピング再生に於いても同様な問題がある。HDCDエンコードされたCDの44.1kHz16bit符号をリッピングし、そのデジタル音楽信号をパソコンのサウンドカード上のデジタル端子から出力し、外部D/A変換ユニットで再生する場合、パソコンがバイナリー一致でなければHDCD判別信号は消失する。

## その他

HDCDデコーダー搭載機器でHDCD盤と通常CD盤を再生したときの音量に関して。

HDCDライセンスアグリーメントでは、HDCD盤と通常CD盤再生時の音量は等しくなければならないと規定されている。 実はHDCDエンコード盤は、0dBを超える波形尖塔部を鈍らせて記録し、再生時に非直線量子化によって鈍らせた波形尖塔部を復活させるピークエクステンションというしくみのために、通常のCD盤と比較すると音量が小さく聴こえてしまうのでHDCD盤と通常CD盤再生時に音量差があると、いちいちリスナーが再生時のボリュームを調整する煩わしさが生じるので、音量差が生じないようにしくみになっている。 また、再生音量が小さいと、音質が劣って聴こえる可能性もあるので、**HDCD対応機器は通常CD盤を再生した際に-6dB音量を絞る**ようになっている。

音量を絞る方法には、HDCDデコーダー内部のデジタルボリュームを用いる場合と、D/A変換後のアナログ信号を絞る2つの方法が用意されている。 デジタルボリュームを用いる回路は非常に簡素で簡便なために多くの機器で採用されているが、この方法であると、通常CD盤を再生する際に、常時-6dB絞られるので、HDCDデコーダー以降のD/A変換回路もフルスケールが用いられずに-6dB絞られたデータが再生される。 HDCDデコーダーIC（PMD100およびPMD200などを始めDSPでHDCDデコーダーを組んだ場合も含む）にはアナログアッテネーター駆動用出力端子も有しているので、マークレビンソンNo.30.5Lなどの一部機器ではアナログ回路によって音量差が生じないようにする回路を採用した機器もある。 しかしHDCDデコーダー搭載ICを良く見てみると、アナログアッテネーターを用いてHDCD/CD音量差を生じさせない回路を採用したとしても、HDCDデコーダーIC内のデジタルアッテネーターは入力信号を常時-1dB減衰させていることに気付く。 これはテストCDに記録された矩形波を再生する際に、デジタルフィルターを通過する際にリンギングが生じるが、このリンギングがクリップしないように考慮するために減衰させているためである。 矩形波をテストCDに記録する際に、フルスケールで記録すると、上記のような場合、リンギングがクリップしてしまうが、通常の音楽信号の場合は、リンギングが生じた波形が記録されているために再生時に波形がクリップするということは無い。例えば、JAS（日本オーディオ協会）発刊のオーデイオテストCD「JAS CD-1」に収録されている矩形波テスト信号をNPC社製SM5842などのデジタルフィルター搭載D/A変換ユニットで再生すると、矩形波はフルスケールで記録されているためにリンギングが生じる部分はクリップするが、PMI社製PMD100などのデジフィルでは、あらかじめ入力信号を減衰させているので矩形波のリンギング部はクリップせずに再生する。 HDCD対応デジフィルの殆ど全てのICでは必ず-1dB絞っているので、通常の音楽CD盤を再生したとき、そのD/A変換回路のフルスケールは用いられていないことになる。

MODEL1やMODEL2などのHDCDエンコーダーを用いれば信号にHDCD隠しコードが重畳されるので、デコード時にHDCDインジケーターが点灯する。 しかし音源収録時に、⊿∑型A/D変換ユニットを用いた場合はノイズフロアが平坦ではない。HDCD の目的効果を発揮させるためには、本来HDCD技術が意図した内容を制作者側でHDCDの目的・効果を理解し、正しいプロセスで信号を制作する必要がある。

特に波形尖塔部を丸めて平均音圧レベルを上昇させて音量感を得ることは一般的にマスタリングの段階で行なわれているが、HDCDのピークエクステンション機能を用いるとピーク波形を上手に丸めることができる。そしてHDCD対応再生機器を所有する一般ユーザーならば、マスタリング段階で丸めた波形が復活する。

## Windows PCでのHDCDデコード

HDCD としてエンコードされた CD 、またそのデコードに対応する再生機器の数は少ないが、[Microsoft Windows XP上にインストールされたバージョン](../Page/Microsoft_Windows_XP.md "wikilink")9以上の [Windows Media Player](../Page/Windows_Media_Player.md "wikilink") ならばパソコンでデコードする事ができると言われている。外部DACユニットへの送出ではなくパソコン内のサウンドカードでHDCD音源をD/A変換する場合は、デジタルフィルターがHDCD対応である必要があるが、2010年現在、HDCD対応デジタルフィルターを搭載したサウンドカードは無い。

また、[Windows Media Playerには](../Page/Windows_Media_Player.md "wikilink")、HDCD隠しコードがエンコードされた16bitWAVEファイルをデコードして24bit化する機能は無いので、サウンドカードが24bitインターフェースを有していてもピークエクステンションやローレベルエクステンションはデコードされない。単に高域集中ディザによって24bitを16bitにしたデータがD/A変換されていることを説明したものと思われる。

  - なお、[Windows Media Playerで再生したデジタル出力信号をにデジタル伝送する際には](../Page/Windows_Media_Player.md "wikilink")、サウンドカードやパソコンがバイナリー一致でなければHDCD隠しコードが消失する。

2010年現在で、もっとも手軽にWindows PCでHDCDをデコードするには、プレイヤーアプリケーションである[foobar2000](https://ja.wikipedia.org/wiki/foobar2000 "wikilink")を利用することである。[ソフトウェアHDCDデコーダコンポーネント（ポストプロセッサー）](http://www.foobar2000.org/components/view/foo_hdcd)がサードパーティから頒布されており、[Wave](https://ja.wikipedia.org/wiki/Wave "wikilink")などの非圧縮ファイルフォーマットに加え、[FLAC](../Page/FLAC.md "wikilink")や[WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")といった[可逆圧縮](../Page/可逆圧縮.md "wikilink")フォーマットファイルのHDCDコードを自動的に検知して、ユーザが意識することなくHDCDデコードを行ったり、複数ファイルにHDCDコードが存在しているのか判定を行うことができる。

  - もともとWindowsでは、[hdcd.exe](http://www.srcf.ucam.org/~cjk32/hdcd/)というソフトウェアHDCDデコーダ（CUIアプリケーション）が存在し、リッピングされた[Wave](https://ja.wikipedia.org/wiki/Wave "wikilink")ファイルにHDCDコードが埋め込まれているかの判定や、HDCDデコードを施した24bit Waveファイルの出力を行うことができる。前述のfoobar2000のコンポーネントもhdcd.exeの実装を流用している。

## 他の24bit→16bit丸め技術の近況

HDCD は24bitを16bitに丸める際に高域集中ディザを用いていたが、Apogee社のUV22もほぼ同様の高域集中ディザによって量子化語長を丸めている。

## 関連項目

  - [音響機器](../Page/音響機器.md "wikilink")

## 外部リンク

  - [HDCDについて](https://www.microsoft.com/japan/windows/windowsmedia/forpros/hdcd/hdcdabout.aspx)(Microsoft)
  - [hdcd.exe（ソフトウェアHDCDデコーダ）の配布サイト](http://www.srcf.ucam.org/~cjk32/hdcd/)
  - [foobar2000用HDCDデコードコンポーネントの配布ページ](http://www.foobar2000.org/components/view/foo_hdcd)

[Category:マイクロソフト](https://ja.wikipedia.org/wiki/Category:マイクロソフト "wikilink") [Category:コンパクトディスク](https://ja.wikipedia.org/wiki/Category:コンパクトディスク "wikilink") [Category:高品質CD](https://ja.wikipedia.org/wiki/Category:高品質CD "wikilink")