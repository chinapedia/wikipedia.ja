> この記事は[PCM音源](https://ja.wikipedia.org/wiki/PCM音源)から翻訳されています。


**PCM音源**（ピーシーエムおんげん）は、[コンパクトディスク](../Page/コンパクトディスク.md "wikilink")などで扱われる[パルス符号変調](../Page/パルス符号変調.md "wikilink") (pulse code modulation、**PCM**) 技術を用いた[デジタルシンセサイザー](https://ja.wikipedia.org/wiki/デジタルシンセサイザー "wikilink")の[音源](../Page/音源.md "wikilink")方式のひとつ。

## 概要

あらかじめ[メモリに記録しておいたPCM波形](../Page/記憶装置.md "wikilink")（サンプル）を再生することで音を生成する装置を示す。電子楽器においてのPCM音源とは、例えば楽器の音などを録音・メモリへ蓄積しておき、鍵盤の押鍵や[MIDI](../Page/MIDI.md "wikilink")のノートオン信号などに応じて所望の音程のPCM波形をメモリから再生する音源方式を示す。[1988年](../Page/1988年.md "wikilink")に[コルグ](https://ja.wikipedia.org/wiki/コルグ "wikilink")から発売されたシンセサイザーである[M1に採用され](../Page/コルグ・Mシリーズ.md "wikilink")、後に[電子ピアノ](../Page/電子ピアノ.md "wikilink")やシンセサイザーなどの[電子楽器](../Page/電子楽器.md "wikilink")の音源方式のひとつとして広く普及している。

PCM音源はメモリの量が十分あれば任意の波形を発音できることが長所である。対して[FM音源](../Page/FM音源.md "wikilink")や[アナログモデリング音源等の他の](../Page/バーチャルアナログ音源.md "wikilink")[音源](../Page/音源.md "wikilink")方式と比べ、[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")に収録した波形を変化させることは、単純にボリュームや音階を変化させることを除けば困難であり、[シンセサイザー](../Page/シンセサイザー.md "wikilink")としての音作りの自由度などでそれら他の音源方式に分を譲る点がある。

PCM音源は楽器メーカーによって独自の名称が用いられることがある。[ヤマハ](../Page/ヤマハ.md "wikilink")のAWM2音源、[ローランド](../Page/ローランド.md "wikilink")のRS-PCM音源、LA音源、[コルグ](https://ja.wikipedia.org/wiki/コルグ "wikilink")のaiスクエアシンセシスやAccess、HIなどと呼ぶ音源方式はいずれもPCM音源である。これらは各社が開発したチップセットや、サンプルの圧縮方法、ひいてはサンプルされた元の音の違い、フィルターの有無等を明示する為の商業用の商標であると考えてよい。

## 歴史

歴史的経緯として、PCM音源方式の[シンセサイザー](../Page/シンセサイザー.md "wikilink")の誕生は、1960年代のコンピュータ制御式電子音楽スタジオ、1970年代の[ディジタルオルガン開発や](../Page/電子オルガン.md "wikilink")、初期のディジタル音楽ワークステーション開発にさかのぼる事ができる。

### 世界の動向

[1960年代](../Page/1960年代.md "wikilink")初期、イギリス在住のロシア系作曲家 Peter Zinovievは、プライベート電子音楽スタジオ Putney のコンピュータ制御を計画し、技術者のDavid Cockwell（AKAI Sシリーズ設計者）、作曲家の Tristram Caryと共に開発を進め、1967年二台のミニコンDEC PDP-8を導入し、遅くとも1969年には、同年創業のUK法人[エレクトロニック・ミュージック・スタジオ](https://ja.wikipedia.org/wiki/エレクトロニック・ミュージック・スタジオ "wikilink")（ロンドン）のPutneyスタジオで、「Musys IIIシステム」が稼動した\[1\]\[2\]。このシステム上（もしくは後に追加された DOB (Digital Oscillator Bank) も併用）で、世界最初のサンプリングが実現されたと考えられている\[3\]。EMSと同様なコンピュータ・サンプラーは、後にアメリカでも開発された。1972年創業のComputer Music Inc.の1976年発売の製品「Computer Music Melodian」は、ミニコンDEC PDP-8を中心に、12bit 22kHzのA/DおよびD/Aコンバータ、アンチエイリアス・フィルターを追加した一種のソフトウェア・サンプラーで、1979年[スティービー・ワンダー](https://ja.wikipedia.org/wiki/スティービー・ワンダー "wikilink")のサウンドトラック「[The Secret Life of Plants](https://ja.wikipedia.org/wiki/:en:The_Secret_Life_of_Plants "wikilink")」で使用された。

このように黎明期のPCM音源は、高価なミニコンを駆使した実験装置的な構成だったので、次の段階として、当時民生利用の始まったLSI技術を使った安価なディジタル楽器の実現が開始された。しかし当時米国のLSIビジネスは、金に糸目をつけない宇宙開発・軍事開発を主な顧客としており、民生分野では電卓のような数百万台規模の市場でしか実績がなかったので、市場規模が何桁も小さな楽器分野では、たちまち行き詰るのが目に見えていた。

[1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")、[ロックウェルのラルフ](../Page/ロックウェル・インターナショナル.md "wikilink")・ドイチュは、 電卓と同様に電子楽器でディジタル革命を起こす計画を立て、[アーレン・オルガン](https://ja.wikipedia.org/wiki/アーレン・オルガン "wikilink")と提携してディジタル・オルガンの開発を進めた。そして[1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")アーレン コンピュータ・オルガンを発売、[1974年](../Page/1974年.md "wikilink")子会社[RMIからHarmonic](https://ja.wikipedia.org/wiki/w:en:Rocky_Mout_Instruments "wikilink") Synthesizer\[4\]を発売した。後者はディジタル倍音加算にアナログ・フィルターを組み合わせた製品で、リアルタイム演算の代わりに計算結果をウェーブテーブル（単周期のPCM音源）に格納して再生する方式が採用された。これら製品の実装技術全てを世界初とするのはかなり無理のある主張だったが、当時は *アポロ計画の技術を使った世界初のコンピュータオルガン* という荒唐無稽な宣伝がなされ、ロックウェルはディジタル楽器の基礎技術全般を囲い込む独占特許の取得に成功した<ref>
この特許は、ディジタル楽器の基本要素（波形テーブル/ビブラート付加/エンベロープ制御/キーボード・スキャン等）を全て網羅したもので、[先発明主義](../Page/先発明主義.md "wikilink")の観点からはその有効性は疑わしかった。

国内最大手[ヤマハ](../Page/ヤマハ.md "wikilink")は当時は訴訟対象ではなかったものの、開発中のディジタル楽器製品が訴訟対象と成り得たので、積極的対応を取る決断をした。そして先行発明の調査に基づいて、アーレン特許を無効とする訴訟を起こした。訴訟は和解で終結したが、いくつかの項目でアーレン特許を否定しきれず、結局多額の特許使用料を支払う結末となった。

一方[ローランド](../Page/ローランド.md "wikilink")は、1970年代当時規模が小さく、ディジタル楽器開発も1980年代半ばまで本格化しなかったので、この特許問題への対応は公表されていない。しかし1980年代後半[ロジャース・オルガン](https://ja.wikipedia.org/wiki/ロジャース・オルガン "wikilink")の買収後に、問題当事者の一人ラルフ・ドイッチェを自社ユーザとして宣伝している。1970年代に業界全体を揺るがした特許問題をあたかも揶揄するかのような挑戦的宣伝を行った真の理由は謎である。</ref>。 提携先のアーレンは訴訟を起こし独占特許を奪取したが、特許買収には巨額な費用を要し、結局、同業他社に次々と巨額な特許使用料請求を行った\[5\]。この結果、訴訟リスクの高い大手楽器メーカはディジタル楽器開発に消極的になり、代わりに訴訟リスクの小さな研究機関やベンチャー企業が活躍する場を得た。

[1975年](../Page/1975年.md "wikilink")頃世界各地で、音楽製作をコンピュータ上でシームレスに処理する「ディジタル音楽ワークステーション」の開発が開始された。[1979年](../Page/1979年.md "wikilink")登場の[フェアライト](https://ja.wikipedia.org/wiki/フェアライト "wikilink")CMIや[シンクラビア](https://ja.wikipedia.org/wiki/シンクラビア "wikilink")IIは、[サンプラー](../Page/サンプラー.md "wikilink")機能や再合成機能を提供し、1980年の[LINN LM-1ディジタル](https://ja.wikipedia.org/wiki/w:en:Linn_LM-1 "wikilink")・ドラムマシンや、1982年の[イミュレータと共に](https://ja.wikipedia.org/wiki/w:en:E-mu_Emulator "wikilink")、初期の[サンプリング](../Page/サンプリング.md "wikilink")音楽の流行を形成した。なお登場当時のサンプラーは、音質やサンプリング時間、表現能力に大きな制限があったため、リアルな生楽器の再現は難しく、むしろ音質劣化を音楽的表現として生かす使い方が多かった。こういった初期の制限は、1980年代半ば頃までには大きく改善され、更に演奏トラック全体を取り込んで編集処理する初期の[DAW機能がハイエンド環境で提供されはじめた](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink")\[6\]。その後1980年代後半にディジタル楽器全般の低価格化が進み、かつてサンプリングドラム用ROMメーカとして出発した[デジデザインや](https://ja.wikipedia.org/wiki/Digidesign "wikilink")[エンソニックがDAW製品の開発を開始すると](https://ja.wikipedia.org/wiki/:en:Ensoniq "wikilink")、フェアライトは価格より実績や安定性が重視される業務用DAW機器分野に転進した\[7\]。

1979年頃 [PPGの](https://ja.wikipedia.org/wiki/w:en:Palm_Products_GmbH "wikilink") Wavecomputer 340/380は、ウェーブテーブル・シンセシス ([Wavetable synthesis](https://ja.wikipedia.org/wiki/:en:Wavetable_synthesis "wikilink")) と呼ばれる64種の波形を切り替えて音色を変化させる音響合成方式を採用した\[8\]。また1981年発売のPPG Wave 2.0では、[アナログシンセサイザー](../Page/アナログシンセサイザー.md "wikilink")と同様なフィルタやエンベロープを追加して、ディジタル/アナログ併用の[ハイブリッド・シンセサイザー](https://ja.wikipedia.org/wiki/ハイブリッド・シンセサイザー "wikilink")を完成した\[9\]。その後1982年PPG Wavetermではディジタル音楽ワークステーション機能を追加、1986年PPG HDU (Hard Disk Unit) でDAW機能を追加し\[10\]、同年参考展示のPPG Realizerでは 上記DAW機能に加え、他のシンセ（[minimoogや](https://ja.wikipedia.org/wiki/モーグ・シンセサイザー#ミニモーグ "wikilink")[DX7](../Page/ヤマハ・DXシリーズ.md "wikilink")）のソフトウェア・モデリング機能も統合した\[11\]。しかし1987年PPGは倒産し realizerは商品化されなかった。ハードウェア楽器をソフトウェア的にシミュートするこのアイデアは、後継会社Waldorfと提携先DAWソフト会社 [スタインバーグ](https://ja.wikipedia.org/wiki/スタインバーグ "wikilink")により、1996年 [VST](https://ja.wikipedia.org/wiki/Virtual_Studio_Technology "wikilink") (Virtual Studio Technology)、1998年VSTi (VST instruments) として実現され、現在では広く普及している。

普及価格帯の製品では、1985年[Ensoniq](https://ja.wikipedia.org/wiki/w:en:Ensoniq "wikilink") [Mirage](https://ja.wikipedia.org/wiki/w:en:Ensoniq_Mirage "wikilink")、[AKAI](../Page/AKAI_professional.md "wikilink") S612といった一連の低価格[サンプラー](../Page/サンプラー.md "wikilink")が登場し、サードパーティによるサンプリング・ライブラリ提供と合わせ、音色入替え可能なPCM音源として普及した。Ensoniq Mirageはサンプラーながら最初からVCFやVCAを搭載しており、次の製品ESQ-1 は波形テーブル内蔵のハイブリッドシンセだった。Ensoniqはこれ以降もサンプリングに特化する事はなく、サンプルデータや波形テーブルを加工するPCM音源のシンセサイザーを次々と発売した。一方、初期のAKAIサンプラーは録音/編集/再生に特化した「サンプリング機材」だったが、その後シンセサイザー機能やエフェクター機能を取り込んで、複雑な音色作りや繊細な表現が可能な「楽器」へと進化した。1998年Nemsys Gigasamplerは大容量ソフトウェア・サンプラーを実用化し、その後ソフトウェア・サンプラーは数GBのサンプルを駆使して高価な生楽器の音を手軽に再現する「ツール」として現在普及している。

### 日本メーカの動向

前述のように世界市場では70年代からディジタル楽器が製品化されていたが、国内は一部メーカを除き、ディジタル楽器の研究が決定的に立ち遅れていた。その原因としては、当時国内の電子楽器専業メーカは成長途上だったため、基礎研究投資を行う余力に欠けていた事、逆に体力に余裕のある大手総合メーカ（電器メーカ含む）は、70年代ディジタルオルガン特許訴訟の影響を受け、ディジタル楽器開発に消極的だった事、等が挙げられる。

そのような中、ヤマハは訴訟問題とディジタル音源開発に真正面から取り組み、1980年以降は次々とディジタル音源製品を発売した（ただしPCM音源は問題の特許と抵触する可能性が高かったからか、当初は発売していない）。他方、多くの国内メーカは、80年代半ばに海外メーカが安価な製品を発売するまで (Alesis, Ensoniq, Emu)、本格的なディジタル楽器を一切発売しなかった。

日本におけるPCM音源製品の草分けは、1982年日本ハモンド/Jugg BoxのPCMドラムマシン「DPM-48」と推定される。サンプルは別売りROMで入れ替え可能だったが、発売時期の関係上MIDIには対応していなかった。その後、ローランド/ヤマハ/コルグ/カシオ/テクニクスといった他の国内メーカもPCMドラムマシンを製品化している。

1985年には[AKAI professionalが国産初のサンプラー](../Page/AKAI_professional.md "wikilink")「S-612」を発売している。このS612は 最大サンプリング周波数32kHzの12bitサンプラーで、サンプリング時間は最長1秒（32kHz時）だったが、音作りに重要なVCFやVCAは内蔵しておらず、同年先行して登場していた [Ensoniq Mirageと比較するととてもシンプルな製品だった](https://ja.wikipedia.org/wiki/w:en:Ensoniq_Mirage "wikilink")。その後AKAI Sシリーズは、S900, S1000でスペックと機能を充実させ、80年代後半 - 90年代にはE-muと並ぶ代表的サンプラーに成長した。同シリーズの設計はDavid Cockerell（前期EMSの各製品やElectro-Harmonixディジタルディレイの設計者）、AKAI S1000のOS開発はChris Hugget（EDP WASP/OSC OSCar/Novation SuperNovaの設計者）が担当しており、イギリスを代表する2人のシンセ・デザイナーによる製品と言えるかもしれない。

1987年[ローランド](../Page/ローランド.md "wikilink")はD-50というサンプル・ウェーブをレイヤーできる[LA音源](../Page/LA音源.md "wikilink")方式シンセを発売した。翌年発売されたコルグ社のM1は、サンプルを幾重にも重ねて発音するレイヤー（コンビネーション）機能やVDF（Variable Digital Filter、フィルター）やVDA（Variable Digital Amplifier、[エンベロープ](https://ja.wikipedia.org/wiki/エンベロープ "wikilink")）を備えリアルな音と幅広い音作りを特徴とした。このVDFやVDAによって、ただ鍵盤に楽器音を並べて再生するだけにとどまらず、VDFによって音の明るさを調整したり、VDAによって音の立ち上がりやその消え方といったパラメータを変化させたりすることができる。また、ローランドのJV-1080やJV-2080のように拡張カードを差し替えて膨大な[音色](../Page/音色.md "wikilink")を扱えるようにした機種もある。

VDFでは、録音された楽器音を削って暗くすることしかできず、VDAで調整可能な時間的変化も限られた範囲での調整となるため、前述の通り音作りの幅が狭い。この点を克服するため、80年代末から90年代の初頭にかけて、シンセサイザーのメーカー各社は工夫を重ねた。ヤマハでは[FM音源](../Page/FM音源.md "wikilink")とハイブリッド型の[RCM音源](../Page/RCM音源.md "wikilink")を開発し、PCM波形をFM変調できる[SY77を発売する](../Page/ヤマハ・SYシリーズ.md "wikilink")。またコルグの[01/Wシリーズではウェーブシェーピングという波形を変調できる方法を採用した](https://ja.wikipedia.org/wiki/コルグ・01/Wシリーズ "wikilink")。また同社の[WAVESTATIONシリーズでは](../Page/コルグ・WAVESTATIONシリーズ.md "wikilink")、波形を繋ぎ合わせることで時間的に変化できるようにした。そして[ローランド](../Page/ローランド.md "wikilink")社ではアナログシンセイザーと同じように波形を変調できるリングモジュレータを搭載した。また、[JD-800のようにアナログシンセサイザーのノウハウを生かした音作りが可能な機種もリリースされた](../Page/ローランド・JDシリーズ.md "wikilink")。しかし、90年代後半以後、波形ROMの容量の増加による、PCM音源の音質の向上、そして、様々な奏法の演奏自体を波形として収録可能になったこと、ハイブリッド音源の音作りの難解さなどの理由からヤマハの[EX5など一部の機種を除き](../Page/ヤマハ・EXシリーズ.md "wikilink")、このような工夫を施したPCM音源のシンセサイザーは姿を消していった。

### エンターテインメント

[家庭用ゲーム機](https://ja.wikipedia.org/wiki/家庭用ゲーム機 "wikilink")におけるPCM音源は、[スーパーファミコン](../Page/スーパーファミコン.md "wikilink")の64kバイトや[メガCD](../Page/メガCD.md "wikilink")及び[プレイステーションの](../Page/PlayStation_\(ゲーム機\).md "wikilink")512kバイトなど、サウンド用のメモリ容量の少なさという厳しい制約がついてまわるため、波形の時間的な変化などは苦手としており、原始的なシンセサイザーと同様に、音量や音高の変化を（時に擬似的な）モジュレーションやエンベロープなどに依存する事で、楽音の表現力を補完している事が多かった。例外として、[アーケードゲーム](../Page/アーケードゲーム.md "wikilink")の一部は膨大な容量をPCM波形に割いている場合もあるが、90年代のPCM音源黎明期においてはメモリ容量も小さく高価であった為、コストのかかる手法であった。なお、楽器としての使用ではなく、単純な音声の再生（セリフの発音など）に関しては、PCM音源のバッファを一時バッファとして使い、DMA転送で連続してデータを送り込みながら再生することで、バッファ容量以上の時間の音声の再生を実現することが多かった。一方で[DVD](../Page/DVD.md "wikilink")メディアなどから[ストリーミング](../Page/ストリーミング.md "wikilink")再生をするときには容量の制約はほぼなくなるが、ローディング時間増などのデメリットがある。家庭用ゲーム機の多くは、この2種類を用途により使い分けている。

### 携帯電話

携帯電話の[着メロ](https://ja.wikipedia.org/wiki/着メロ "wikilink")や[着うた](../Page/着うた.md "wikilink")についても、PCM音源、またはADPCM音源が採用されているものの、[着メロ](https://ja.wikipedia.org/wiki/着メロ "wikilink")の場合、パケット課金が存在する為に、端末に搭載できるメモリが大きくなった現在でも、[着メロ](https://ja.wikipedia.org/wiki/着メロ "wikilink")として[FM音源](../Page/FM音源.md "wikilink")とあわせて原始的なシンセサイザーとして配信される場合がある。

## 波形のループ

減衰の早い音では「ワンショット」と呼ばれる通常のサンプリング、及び再生が行われるが、減衰の遅い、もしくは減衰の無い音を用いる場合、メモリーの使用量が膨大となる\[12\]。この場合、アタック部分\[13\]が過ぎた後、安定した波形をループさせることで、メモリー使用量を大幅に削減することが可能である。またこの場合、[エンヴェロープ](https://ja.wikipedia.org/wiki/エンヴェロープ "wikilink")などを併用し、より自然な音を構成することが求められる。ある程度長い時間単位でループさせる場合もあれば、波形1周期を基準にループさせる場合もある。前者の場合はより自然に音を繋ぐため、波形を厳選した上で、クロス･フェード\[14\]を行う場合もある。後者の場合はメモリーは大きく節約できるものの、一般に表情が乏しくなるため、各種パラメータを変更することで、音に表情を付けることが必要とされる\[15\]。

## 脚注

## 関連項目

  - [波形メモリ音源](../Page/波形メモリ音源.md "wikilink")
  - [物理モデル音源](../Page/物理モデル音源.md "wikilink")
  - [パルス符号変調](../Page/パルス符号変調.md "wikilink") (PCM)
  - [サンプラー](../Page/サンプラー.md "wikilink")
  - [シンセサイザー](../Page/シンセサイザー.md "wikilink")
  - [ミュージックワークステーション](../Page/ミュージックワークステーション.md "wikilink")
  - [音源モジュール](../Page/音源モジュール.md "wikilink")
  - [DTM（デスクトップミュージック）](../Page/デスクトップミュージック.md "wikilink")
  - [サウンドフォント](https://ja.wikipedia.org/wiki/サウンドフォント "wikilink")

[Category:電子音源の合成方式](https://ja.wikipedia.org/wiki/Category:電子音源の合成方式 "wikilink")

1.
2.
3.
    DOBは、ディジタル技術による64個のオシレータ/振幅制御器の組で、各オシレータは1024サンプルのウェーブテーブルを持ち、16bit 46kHzのサンプル出力が可能だった（開発者 : David Cockwell（1965年 - 1975年在職）, Peter Eastty（1972年 - 1977年在職））。この他、DOBと組み合わせる128系統[デジタルフィルタ](https://ja.wikipedia.org/wiki/デジタルフィルタ "wikilink") Analysing Filter Bank（開発 : Peter Eastty）も開発された。
4.  synthmuseum.com: [RMI Harmonic Synthesizer](http://www.synthmuseum.com/rmi/rmihar01.html)
5.  fundinguniverse.com: [Allen Organ Company History](https://www.fundinguniverse.com/company-histories/Allen-Organ-Company-Company-History.html)
6.  1985年[Synclavier](https://ja.wikipedia.org/wiki/シンクラビア "wikilink") "Direct to Disk" option
7.  フェアライトジャパン: [Fairlight Japanについて](http://www.fairlight.co.jp/intro1.html)
8.  ppg.synth.net: [PPG WaveComputer 340/380](http://ppg.synth.net/340/)
9.  ppg.synth.net: [Wave2.0](http://ppg.synth.net/wave20/)
10. synthmuseum.com: [PPG Hard Disk Unit](http://synthmuseum.com/ppg/ppghdu01.html)
11. synthmuseum.com: [PPG Realizer](http://synthmuseum.com/ppg/ppgreal01.html), proun.net: [PPG Realizer](http://www.proun.net/gallery/ppg_realizer.html)
12. 代表的なものとして、[ブラスや](../Page/金管楽器.md "wikilink")[ストリングス](https://ja.wikipedia.org/wiki/ストリングス "wikilink")など。
13. 発音直後、倍音の変化が著しい部分。
14. この場合、ループの繋ぎの部分で現在の波形を[フェードアウト](https://ja.wikipedia.org/wiki/フェードアウト "wikilink")させつつ、次の波形を[フェードイン](https://ja.wikipedia.org/wiki/フェードイン "wikilink")させる。
15. 『シンセサイザーの全知識』 安斎直宗 リットー・ミュージック [1996年](../Page/1996年.md "wikilink") ISBN 4-8456-0106-0 p110 - p124