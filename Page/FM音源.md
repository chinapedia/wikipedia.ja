> この記事は[FM](https://ja.wikipedia.org/wiki/FM)から翻訳されています。


<File:Synclavier1> JB.jpg|[シンクラヴィア](https://ja.wikipedia.org/wiki/シンクラヴィア "wikilink")I (1975年) <File:YAMAHA> GS1 (inside, CCRMA).jpg|ヤマハ・GS1 (1980年) <File:YAMAHA_DX7.jpg>|[ヤマハ・DX7](https://ja.wikipedia.org/wiki/ヤマハ・DXシリーズ "wikilink") (1983年)

**FM音源**（エフエムおんげん）は、Frequency Modulation（[周波数変調](../Page/周波数変調.md "wikilink")）を応用する音色合成方式を用いた[音源](../Page/音源.md "wikilink")。を中心として[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")のCCRMA（Center for Computer Research in Music and Acoustics）で開発されたものを、[日本楽器製造（現・ヤマハ）がライセンスを受け実用化した](https://ja.wikipedia.org/wiki/ヤマハ "wikilink")\[1\]。ヤマハによれば、実際にはPhase Modulation（[位相変調](https://ja.wikipedia.org/wiki/位相変調 "wikilink")）によって実装されている\[2\]。

基本波形の発振・変調をおこなう合成器（オペレータと呼ばれる）を複数組み合わせて音色を合成する。数学的には発振機構が[二重振り子](https://ja.wikipedia.org/wiki/二重振り子 "wikilink")のような非線形演算に基づいているため、演奏に合わせて波形生成のパラメーターを変化させることにより倍音成分が大きく変化し、音色を劇的に変化させることが可能である。しかし、その挙動は[カオスであるため](https://ja.wikipedia.org/wiki/カオス理論 "wikilink")、パラメータの変動による倍音変化は予測し難い。

それまでの[減算方式](https://ja.wikipedia.org/wiki/減算方式 "wikilink")の[アナログシンセサイザー](https://ja.wikipedia.org/wiki/アナログシンセサイザー "wikilink")にはなかった複雑な[倍音](https://ja.wikipedia.org/wiki/倍音 "wikilink")成分を持つ音色、特に[エレクトリックピアノ](../Page/エレクトリックピアノ.md "wikilink")や[ブラスのほか](../Page/金管楽器.md "wikilink")、非整数次倍音を含む[ベル](https://ja.wikipedia.org/wiki/ベル "wikilink")系の金属的な音色の再現が特長とされる\[3\]\[4\]。FM音源が奏でるきらびやかで金属的な響きは1980年代のポピュラー音楽に多く取り入れられ、当時を象徴するサウンドとも評されている\[5\]。

FM音源の音色の定義に要するパラメーターはせいぜい数十[バイト程度であり](https://ja.wikipedia.org/wiki/バイト_\(情報\) "wikilink")、[メモリーの使用量を筆頭として要求される](../Page/記憶装置.md "wikilink")[計算資源](https://ja.wikipedia.org/wiki/計算資源 "wikilink")が比較的少なく、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")、[家庭用ゲーム機](https://ja.wikipedia.org/wiki/家庭用ゲーム機 "wikilink")、[携帯電話](../Page/携帯電話.md "wikilink")などに広く利用されている（詳しくは後述）。

## 概要

### 原理

[thumb](https://ja.wikipedia.org/wiki/ファイル:2op_FM.svg "wikilink") [Phase-modulation.gif](https://ja.wikipedia.org/wiki/File:Phase-modulation.gif "fig:Phase-modulation.gif")

自然音のような動的に変化する複雑なスペクトルが、2つの発振器からの合成で現れる、**変調合成**の一手法である。FM合成器（**オペレータ**）のキャリア、モジュレータの波形を正弦波とすると、合成される信号波 \(FM(t)\) は以下の式で表される。

\[FM(t) = A\sin(2\pi f_c t+\beta\sin(2\pi f_m t))\]

  -
    ここで \(A\): キャリア振幅, \(f_c\): キャリア周波数, \(\beta\): 変調指数, \(f_m\): モジュレータ周波数

FM合成で得られた出力のスペクトルは、\(f_c \pm nf_m(n = 1, 2, 3,  \cdots)\)という、キャリアの周りに、モジュレータ周波数の整数倍で側波帯が現れたものとなる。側波帯成分の振幅は[ベッセル関数](https://ja.wikipedia.org/wiki/ベッセル関数 "wikilink")で表すことができる。

[シンセサイザー](../Page/シンセサイザー.md "wikilink")や音源[チップ](https://ja.wikipedia.org/wiki/チップ "wikilink")では、複数個の合成器を直列あるいは並列につなぎ、様々な合成結果を得る。このつなぎかたを**アルゴリズム**と呼んでいる。また、[ヤマハ](https://ja.wikipedia.org/wiki/ヤマハ "wikilink")による研究開発の過程で、出力をモジュレータに[フィードバック](https://ja.wikipedia.org/wiki/フィードバック "wikilink")するフィードバックFMが考案された。

### 応用と発展

[ヤマハ](https://ja.wikipedia.org/wiki/ヤマハ "wikilink")（当時・日本楽器製造）は、FM方式の特許のライセンスを取得し研究開発を進め、[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")にGS1とGS2を発表する。1982年には廉価版のCE20及びCE25を発表する。GS, CEシリーズは音色作りがユーザーに開放されていないプリセットキーボードであった（GS1はヤマハ渋谷店に設置されていたプログラマーでユーザーが音色を作ることは一応可能であった）。またGSシリーズは100～260万円と高額であり、非常に大きく、かつ重かった。その後、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に発売されたシンセサイザー[DX7が低価格かつ音色作成機能が開放されたことによって](https://ja.wikipedia.org/wiki/ヤマハ・DXシリーズ "wikilink")、一般に耳にする音楽で広く使われるようになり、FM音源のサウンドは広く知られるようになった。

また、音源[チップ](https://ja.wikipedia.org/wiki/チップ "wikilink")は、[1980年代](../Page/1980年代.md "wikilink")の[パソコンや](../Page/パーソナルコンピュータ.md "wikilink")[アーケードゲーム](../Page/アーケードゲーム.md "wikilink")機や、家庭用[ゲーム機](../Page/ゲーム機.md "wikilink")の[セガ・マークIII](../Page/セガ・マークIII.md "wikilink")のFMサウンドユニット、日本国内版のセガ[マスターシステム](https://ja.wikipedia.org/wiki/マスターシステム "wikilink")、[メガドライブ](../Page/メガドライブ.md "wikilink")、[MSX2+](https://ja.wikipedia.org/wiki/MSX2+ "wikilink")のパナソニックFS-A1WX等の内蔵音源として幅広く使われ、80年代中期から90年代初頭辺りまでこれらから発せられる音として定番となっていた。

特に[エレクトリックピアノ](../Page/エレクトリックピアノ.md "wikilink")の音色は秀逸で、[PCM音源](../Page/PCM音源.md "wikilink")に[サンプリング](https://ja.wikipedia.org/wiki/サンプリング "wikilink")され今でもよく使用されている。マリンバやオルガンの音などはPCM音源に負けないほどリアルな音が出せる。アコースティックピアノの音のシミュレートは苦手であり、 PCM音源に押されて、一時はシンセサイザー市場から消えかけた。しかし、FM音源独自の[ベロシティ](https://ja.wikipedia.org/wiki/ベロシティ "wikilink")による音色のダイナミックな変化が見直され、ソフトウェアシンセサイザーのFM7やヤマハのDX200、[PLG150-DXなど近年もFM音源の機種が発表されている](https://ja.wikipedia.org/wiki/Modular_Synthesis_Plug-in_System "wikilink")。

発声用の「キャリア」だけでなく、変調用の「モジュレータ」にも[エンベロープの設定が可能であるため](https://ja.wikipedia.org/wiki/ADSR "wikilink")、倍音構成の時間変化を伴う音色を作成できる。FM変調による倍音変化は減算式フィルタによる倍音変化に比べて自由度が高いことから、極端な倍音変化を設定することで「にょわーーーーん」などという擬音語で表現されるような、金属的かつ非自然的な「FM音源らしい音」を生み出すことができる。[レゾナンス](https://ja.wikipedia.org/wiki/レゾナンス "wikilink")、[ワウペダル](https://ja.wikipedia.org/wiki/ワウペダル "wikilink")などの項目も参考になると思われる。他の方式のシンセサイザーでも[レゾナンス](https://ja.wikipedia.org/wiki/レゾナンス "wikilink")などのパラメータをリアルタイムで変更することによって、ある程度の再現は可能。だが、生産性に問題があり、演奏データの肥大化にも繋がる。

逆に、自然な生楽器の再現などにこの自由度を生かすこともでき、減算方式のシンセサイザーに比べてよりリアルな表現が可能である。無論PCMなど録音済み波形を用いる音源に比べれば再現度は劣るが、必要な計算リソースも少ないため、現在でも低コストで多彩な音色が得られる音源装置として有用な選択肢となっている。

[TX81Zなどの後期のFM音源の機種や](https://ja.wikipedia.org/wiki/ヤマハ・TXシリーズ "wikilink")[SY99など](https://ja.wikipedia.org/wiki/ヤマハ・SYシリーズ "wikilink")[AFM音源の機種では](https://ja.wikipedia.org/wiki/RCM音源 "wikilink")[正弦波](https://ja.wikipedia.org/wiki/正弦波 "wikilink")以外の波形で変調可能になった。

[1989年](../Page/1989年.md "wikilink")に発売されたヤマハのシンセサイザー[SY77ではAFM音源へとアップグレードされ](https://ja.wikipedia.org/wiki/ヤマハ・SYシリーズ "wikilink")、[PCM音源](../Page/PCM音源.md "wikilink")によりキャリアを変調させることも可能となる。その完成形が[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")に発売された[SY99と言える](https://ja.wikipedia.org/wiki/ヤマハ・SYシリーズ "wikilink")。

その後、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に登場した[FS1Rではフォルマントシンギング音源と呼ばれる人の](https://ja.wikipedia.org/wiki/ヤマハ・FS1R "wikilink")[声](https://ja.wikipedia.org/wiki/声 "wikilink")をも[シミュレートできる音源とハイブリッドとなり](https://ja.wikipedia.org/wiki/シミュレーション "wikilink")、オペレータもDX7の6機から8機と増え、変調させられる幅が広がった。FS1Rが発売された頃にはFM音源の音色が飽きられており、簡単にリアルな生楽器音を実現できるPCM音源が主流になっていたため、FS1Rは商業的には成功しなかった。FS1Rを最後にヤマハのFM音源シンセサイザーは一旦市場から消えることになった。

最近では[携帯電話](../Page/携帯電話.md "wikilink")の[着信メロディ](https://ja.wikipedia.org/wiki/着信メロディ "wikilink")再生用に使用されている。

一部のチップには、「音声合成モード/複合正弦波合成モード」が用意されている。特定のチャンネルのオペレータに、独立してF-Numberが設定可能になっており、内蔵タイマーのオーバーフロー毎に該当チャンネルのオペレータをキーオンにするというものであり、音源ソース、並びにそこからの変換については、あらかじめ別途行う必要がある。その仕様上、該当するチップにはタイマーが内蔵されており、割り込みの発生源などとしても利用されていた。チャンネルもしくは、オペレータなどの設定により、正弦波を発声するように設定し、制御を行えば、同様の効果を得ることが出来る。PCMなどと比較すれば、必要とするリソースや、チップの機能を使えることによる処理の軽さがメリットとはなるが、FM音源1チャンネルのオペレータの駆動のみという状況と、パラメータとして設定できる値の分解能などの要因で、音質は然程高くは無く、時期によってはその正弦波に波形を分解する処理そのものに労力がかかったこともあって、[ゲームアーツ](../Page/ゲームアーツ.md "wikilink")のメーカーロゴや、ゲーム中の一部の音声などに用いられた以外での利用は少ない。[MA-7](https://ja.wikipedia.org/wiki/MA-7 "wikilink")では、Humanoid Voiceとして、正弦波合成の出力を用いている。

また、日本で携帯電話が普及した2000年前後頃からは携帯機器用音源チップ\[6\](MAシリーズ)にも組み込まれ、主に[KDDI](../Page/KDDI.md "wikilink")（[auブランド](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")）や[ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")（[SoftBankブランド](../Page/SoftBank_\(携帯電話\).md "wikilink")）、[イー・モバイル](https://ja.wikipedia.org/wiki/イー・モバイル "wikilink")（現・ソフトバンク[Y\!Mobile](https://ja.wikipedia.org/wiki/Y!Mobile "wikilink")ブランド）等の携帯電話に内蔵されている。

なお、2014年のパーソナルコンピュータには原則的に搭載されていないが、[拡張ボード](https://ja.wikipedia.org/wiki/拡張ボード "wikilink")として別途購入、搭載は可能。更に、各種コンピュータの[エミュレータ](https://ja.wikipedia.org/wiki/エミュレータ "wikilink")ソフトの流行と共に、PCM音源を使いソフトウェアで波形合成して再生するドライバが有志により開発されている。

2015年9月、ヤマハより[refaceシリーズの一つとしてFM音源を](https://ja.wikipedia.org/wiki/ヤマハ・refaceシリーズ "wikilink")17年ぶりに搭載したキーボードシンセサイザreface DXが発売された。さらに、MOTIFシリーズに代わるフラッグシップシンセとして、FM-XとAWM2のハイブリッドシンセである[MONTAGEが](https://ja.wikipedia.org/wiki/ヤマハ・MONTAGE "wikilink")2016年に発売された。2018年にはMONTAGEの廉価版であるMODXが発売された。

FM音源は長らく特許であったため、他社から採用機種が発売されることはまれであった。1987年にはKORGからDS-8と707というFM音源デジタルシンセサイザーが発売された。これは当時経営が悪化していたKORGを救済するため、ヤマハからFM音源チップが供給されたものである。現在は特許が切れており、各社からFM音源を搭載したハードウェアシンセサイザーやソフトウェアシンセサイザープラグインが発売されている。

## 音源チップ一覧

### OPL系

[thumb](https://ja.wikipedia.org/wiki/ファイル:YM3526_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Y8950_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:YM2413_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:YM3812_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:YMF262-M.jpg "wikilink") 2オペレータ。内蔵リズム音はハイハット、トップシンバル、タム、バスドラム、スネアドラムの5音。バスドラムを除き1オペレータで生成されるため、FM3ch分のレジスタで5chのリズム音を同時に発音可能。 もともとは、[キャプテンシステム](https://ja.wikipedia.org/wiki/キャプテンシステム "wikilink")および[文字多重放送](https://ja.wikipedia.org/wiki/文字多重放送 "wikilink")受信端末用に設計されており、メロディ6音以上＋リズム5音以上という性能はキャプテンシステム標準端末仕様ランク2に相当する。

  - [YM3526](https://ja.wikipedia.org/wiki/YM3526 "wikilink")(OPL) 2オペレータ9chまたは6ch + リズム5ch。2オペレータなのでアルゴリズムは直列、並列の2種類のみ。[タイトー](https://ja.wikipedia.org/wiki/タイトー "wikilink")の[バブルボブル](../Page/バブルボブル.md "wikilink")や、[テラクレスタ](https://ja.wikipedia.org/wiki/テラクレスタ "wikilink")（海外版）をはじめとした[日本物産](https://ja.wikipedia.org/wiki/日本物産 "wikilink")のアーケードゲームなどで使用されていた。
  - Y8950([MSX-AUDIO](https://ja.wikipedia.org/wiki/MSX-AUDIO "wikilink")) 2オペレータ9chまたは6ch + リズム5ch、[ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink") 1ch(16kHz/4bit/[モノフォニック](https://ja.wikipedia.org/wiki/モノフォニック "wikilink"))、32kB～256kBの波形メモリを外部に持てる。MSXの音源規格にあわせ、OPL相当の機能に加えADPCMの回路機能を包含しており、チップ表面には、MSXのロゴと、MSX-AUDIOの表記があり、マニュアルには他のチップでは存在する"Operator Type"等の表記が無い。[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")の拡張カートリッジや[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用サウンドボード、アーケード基板、MZ-2861用ADPCMボード(MZ-1E36)などで使用。
  - [YM3812](https://ja.wikipedia.org/wiki/YM3812 "wikilink")/FM1312(OPL II) 2オペレータ9chまたは6ch + リズム5ch、[AdLib](https://ja.wikipedia.org/wiki/AdLib "wikilink")や[Sound Blasterで使用](https://ja.wikipedia.org/wiki/Sound_Blaster "wikilink")。YM3812はYM3526とハードウェアレベルで互換性があり、そのまま差し替えて使用することが可能。[サイン波](https://ja.wikipedia.org/wiki/サイン波 "wikilink")以外の発振も可能になり、音作りの幅が広がった。また、初期のSound Blaster ProではOPL IIを2台搭載した。
  - [YM2413](https://ja.wikipedia.org/wiki/YM2413 "wikilink")(OPLL) 2オペレータ9chまたは6ch + リズム5ch。OPL2のサブセットで、特定の音色セットを内蔵することで制御を単純化した廉価版にあたり、他のOPL系のチップと比較し、音色を保持するレジスタが1セットしか実装されておらず、パラメータの分解能も削られている他、同時に使用できる音色は内蔵の15音色に限られる。内蔵されている15音色は、キャプテンシステム・文字放送受信端末標準仕様に定められているものであり、ほとんどのキャプテンシステム端末・文字多重放送受信端末装置に搭載されていた。 [MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")の拡張カートリッジ([FM-PAC](https://ja.wikipedia.org/wiki/FM-PAC "wikilink"))および[MSX-MUSIC](https://ja.wikipedia.org/wiki/MSX-MUSIC "wikilink")としても利用された他、[UFOキャッチャー](https://ja.wikipedia.org/wiki/UFOキャッチャー "wikilink")、[セガマーク3](https://ja.wikipedia.org/wiki/セガマーク3 "wikilink")用周辺機器のFMサウンドユニットおよび、同機種内蔵の日本国内版のセガ[マスターシステム](https://ja.wikipedia.org/wiki/マスターシステム "wikilink")、麻雀学園、クイズカプコンワールド、ポンピングワールドなどのカプコンのアーケード基板、[ニューパルサー](https://ja.wikipedia.org/wiki/ニューパルサー "wikilink")・[大花火](https://ja.wikipedia.org/wiki/大花火 "wikilink")・[ジャグラー](https://ja.wikipedia.org/wiki/ジャグラー "wikilink")・[スフィンクス7](https://ja.wikipedia.org/wiki/スフィンクス7 "wikilink")・他の一部の[パチスロ](https://ja.wikipedia.org/wiki/パチスロ "wikilink")機\[7\]などで使われている。 また、以下の様な派生品も存在する。
      - YM2420(OPLL2)。ヤマハのポータブルキーボード、[ショルキー](https://ja.wikipedia.org/wiki/ショルキー "wikilink")シリーズに搭載された。内蔵音色セットなど性能・機能はOPLLと同等だが、自社の楽器用に制御手順が変更されている。
      - YMF281(OPLL-P)。OPLLの内蔵音色を差し替えたもの。パチンコ向けとされる。
      - MS1823(YM2423)。OPLLの内蔵音色を差し替えたもの。[シャープ](../Page/シャープ.md "wikilink")にOEM供給された。[Philips](https://ja.wikipedia.org/wiki/Philips "wikilink")のポータブルシーケンサーPMC100や[Atari ST用のFM音源カートリッジに搭載された](https://ja.wikipedia.org/wiki/Atari_ST "wikilink")。
      - 内蔵音色を差し替え、同時発音数がメロディー6音になったサブセット版がコナミのVRC VIIの音源部に採用されている。
  - [YMF262](https://ja.wikipedia.org/wiki/YMF262 "wikilink")-M(OPL3)([en](https://ja.wikipedia.org/wiki/:en:Yamaha_YMF262 "wikilink"))： 2オペレーター/4オペレータ可変。リズム部はOPL同等。2オペレータ18ch、4オペレータ6ch＋2オペレータ6ch、4オペレータ6ch＋2オペレータ3ch＋リズム5chなど動作モードが多い。ベース波形を8種類から選択可能。 主に[Sound Blasterシリーズに搭載されていたチップである](https://ja.wikipedia.org/wiki/Sound_Blaster "wikilink")。Sound Blaster Proの後期モデルから採用され、以後のモデルにも本製品や互換品が利用されている。SB互換音源としてEPSON PCシリーズのWindows3.1対応機や、サードパーティ製音源等にも採用例がある。ゲームセンター向けのメダルゲームを多く開発製造してきたシグマ社のビデオスロット、ビデオポーカー、メカニカルスロット用のゲーム基板、SG97V/SG97Mにも搭載されている\[8\]。 Sound Blasterシリーズが[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")では事実上の標準といえるほど普及していたことや、マイクロソフトが[Windows 3.1向けに制定したサウンドカード仕様であるWindows](https://ja.wikipedia.org/wiki/Windows_3.1 "wikilink") Sound System([en](https://ja.wikipedia.org/wiki/:en:Windows_Sound_System "wikilink"))がOPL3の利用を前提としていたこともあり、「SBPro互換」と称するOPL3コアを流用した互換品やエミュレーションチップも数多く存在する。
      - YMF262-S：[QFP](https://ja.wikipedia.org/wiki/QFP "wikilink")版
      - YMF289（OPL3-L)：OPL3の省電力版。PCMCIA版Sound Blaster等で採用。
      - YMF297-F：PC-9801-118サウンドボード用。OPL3の機能に加え、OPNA互換モードも備えている。このため118ボードは86ボードとの互換性を保ちながらWindows Sound Systemにも対応している（ただし118ボードはDOSからの利用は正式サポートされていなかった）。
      - CT1747：クリエイティブテクノロジーによる互換チップ。OPL3同等のコアが内包されている。
      - YMF701(OPL3-SA)：16bitのサウンドCODEC、MIDI I/Fを備え、ワンチップでSBPro互換を実現している。
  - YMF278B-F/YMF278B-S (OPL4) ：OPL3に24chのPCM音源を付加した製品。YAMAHA SOUND EDGE SW-20、[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")の拡張カートリッジMoonsound(ムーンサウンド)、コンピュータ・テクニカ製のPC-98x1用拡張サウンドボードであるオールサウンドプレーヤー98(SPB-98)で使用されていた。
      - FM音源部はOPL3同等
      - PCM24音同時発音,最大512音色
      - 入力クロック　33.8388MHz
      - 音声出力データのサンプリング周波数　44.1kHz
      - 波形データは8ビット、12ビット、16ビット構成を選択可能
      - 各音声出力チャンネルは個別に16段階の[パン設定が可能](https://ja.wikipedia.org/wiki/パンニング_\(音響\) "wikilink")
      - 外部メモリはROMまたはSRAMを接続可能、容量32Mビット
      - 1Mビット、4Mビット、8Mビット、16Mビット用チップセレクト信号出力可能
      - 音声出力6ch、YAC513(DAC)を接続可能
      - エフェクターYSS225(EP)接続可能
      - 80ピンQFP(YMF278B-F)または100ピンQFP(YMF278B-S){{-}}{{-}}

### OPN系

[thumb](https://ja.wikipedia.org/wiki/ファイル:YM2608_FMSynthesizerChip.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Yamaha_YM2612_chip.jpg "wikilink") 4オペレータ。

  - [YM2203](https://ja.wikipedia.org/wiki/YM2203 "wikilink")(OPN) 4オペレータ、3ch + [PSG](../Page/Programmable_Sound_Generator.md "wikilink")(SSG)3ch / FMの1chは効果音または音声合成(CSM)モードとして使用可 + ノイズ1ch、[PC-6001mkIISR](https://ja.wikipedia.org/wiki/PC-6000シリーズ#PC-6001mkIISR "wikilink")・[PC-6601SR](https://ja.wikipedia.org/wiki/PC-6600シリーズ#PC-6601SR "wikilink")・[PC-8800シリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")・[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")・[MZ-2500](https://ja.wikipedia.org/wiki/MZ-2500 "wikilink")・[FM77AV](https://ja.wikipedia.org/wiki/FM77AV "wikilink")などで使用。AY-3-8910と同様の機能を搭載しており、音声出力機能だけでなく、8bit×2系統のI/Oポートも実装。レジスタの構造も互換を持たせている。
      - YMF264(OPNC)CMOS版。中期以降の[EPSON PCシリーズの](https://ja.wikipedia.org/wiki/EPSON_PCシリーズ "wikilink")26音源互換部に採用されている他、98NOTE向けのサウンドユニット(LSU-N98、NMB-G)にて使用。
  - [YM2608](https://ja.wikipedia.org/wiki/YM2608 "wikilink")(OPNA) 4オペレータ、6chステレオ + リズム6chステレオ + SSG3ch + ADPCM1chステレオ + ノイズ1ch、YM2203の[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")で、キャプテンシステムおよび文字多重放送端末仕様に適合する。[PC-8800シリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")・[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")などで使用\[9\]。
  - [YM2610](https://ja.wikipedia.org/wiki/YM2610 "wikilink")(OPNB) 4オペレータ、4chステレオ + SSG3ch + ADPCM7ch(周波数固定6+周波数可変1ch)ステレオ + ノイズ1chステレオ、YM2608[下位互換](https://ja.wikipedia.org/wiki/下位互換 "wikilink")、[F2システム](https://ja.wikipedia.org/wiki/F2システム "wikilink")・[ネオジオ](https://ja.wikipedia.org/wiki/ネオジオ "wikilink")などで使用
      - YM2610B YM2610のFM音源を6chに拡張したもの。
  - [YM2612](https://ja.wikipedia.org/wiki/YM2612 "wikilink")(OPN2)/YM3438(OPN2C) 4オペレータ、6chステレオ。YM2608[下位互換](https://ja.wikipedia.org/wiki/下位互換 "wikilink")。[メガドライブ](../Page/メガドライブ.md "wikilink")・[FM TOWNS](../Page/FM_TOWNS.md "wikilink")・セガ[systemC2](https://ja.wikipedia.org/wiki/セガ・システムC "wikilink")（アーケード版『[ぷよぷよ](../Page/ぷよぷよ.md "wikilink")』他）・ニューUFOキャッチャーなどで使用。内蔵DACの解像度はYM2612、YM3438共に9ビットであるが、YM3438のみCMOS化された事によりノイズは減っている。また一部の[FM TOWNSで使われた互換チップYMF](../Page/FM_TOWNS.md "wikilink")276\[10\]は、汎用のシリアル接続[DACを接続可能である](https://ja.wikipedia.org/wiki/デジタル-アナログ変換回路 "wikilink")。解像度は16bit。
  - [YMF288](https://ja.wikipedia.org/wiki/YM2608#YMF288（OPN3\) "wikilink")(OPN3) 4オペレータ、6chステレオ + リズム6chステレオ + PSG3ch + ノイズ1chステレオ、YM2608[下位互換](https://ja.wikipedia.org/wiki/下位互換 "wikilink")であるため、OPNAの代用として使われることもある。消費電力は低減し、チップサイズも小さくなったものの、I/O機能、CSM音声合成、ADPCM等が回路として削除されている。[満開製作所](https://ja.wikipedia.org/wiki/満開製作所 "wikilink")のまーきゅりーゆにっと、[PC-9821](https://ja.wikipedia.org/wiki/PC-9821 "wikilink")等で利用されている。
  - YMF297(OPN4 もしくは OPN3/OPL3) OPN3にOPL3互換動作モードを追加したもの｡PC-9801-118音源ボードに使用された｡

### OPM系

[thumb](https://ja.wikipedia.org/wiki/ファイル:Yamaha_YM2151.PNG "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:YAMAHA-YM2164.jpg "wikilink") 4オペレータ。 特筆すべきは、基準音の整数倍の周波数から大幅に周波数をずらした正弦波で変調をかけられるようになっている事で、これを実現するパラメータを一般的に「デチューン2」もしくはDT2と呼ぶ\[11\]。このため[シンバル](https://ja.wikipedia.org/wiki/シンバル "wikilink")等の金属製打楽器にみられるような非整数倍音成分を含むものなどの音作りが容易になっている\[12\]。 なお、他に「デチューン2」に相当するパラメータを持つFM音源チップに、OPQ、OPU（いずれもポータトーン、ポータサウンドの一部モデルに搭載）がある。

  - [YM2151](https://ja.wikipedia.org/wiki/YM2151 "wikilink")(OPM) 4オペレータ、8chステレオ。1980年中盤～1990年中盤のアーケードゲーム基板、[X1](../Page/X1_\(コンピュータ\).md "wikilink")・[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")、一部の[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")などで使用。特にアーケードゲームでは数多くのメーカーに広く用いられ、PCM音源との併用で使用されることが多かった。
  - YM2164(OPP) 4オペレータ、8chステレオ DX21、DX27、DX27S、DX100、FB-01、SFG-05、コルグDS-8、707等で使用。

{{-}}

### OPZ系

[thumb](https://ja.wikipedia.org/wiki/ファイル:YM2414_02.jpg "wikilink") 4オペレータ。OPM/OPPの派生型で、ほぼ上位互換。ヤマハの[ポータトーン](https://ja.wikipedia.org/wiki/ポータトーン "wikilink")・[キーボーディシモ](https://ja.wikipedia.org/wiki/キーボーディシモ "wikilink")シリーズ等では、下位モデルにOPP、上位モデルにOPZが搭載されるといったような棲み分けがされている。

  - [YM2414](https://ja.wikipedia.org/wiki/YM2414 "wikilink")(OPZ) 4オペレータ、8chステレオ。YAMAHA TX81ZおよびV2(DX11)ほか多数で使用。波形選択パラメータにより正弦波を含む8種類の波形を使用できる。OPMと比較して、オペレータごとの周波数倍率を細かく指定できるため、柔らかいストリングスの音を作れる(キャリアを4.01倍、モジュレータを3.99倍にして直列に組み合わせるなど)利点がある。パッケージ、ピンアサイン及び使用するDACがOPM/OPPと共通しているが実際に置換して互換性確認したユーザーはまだいないようである。
  - YM2424(OPZII) 4オペレータ、8chステレオ YAMAHA V50にて2個使用。YM2414から、FIXモードでのオペレータ発振可能周波数が拡大された。

{{-}}

### OPX系

[thumb](https://ja.wikipedia.org/wiki/ファイル:Yamaha_YMF271-F_01.jpg "wikilink")

  - YMF271-F(OPX)
      - 2オペレータ(4アルゴリズム),3オペレータ(8アルゴリズム),4オペレータ(16アルゴリズム)のいずれかに設定可能。
      - FM演算用に7種類の内蔵プリセットデータまたは外部メモリのPCM波形データを使用可能。
      - エフェクターLSI(YSS225)との8chインターフェイス内蔵。
      - PCM同時12音。
      - 波形データ用にROMまたはRAMを8MBリニアアクセスで接続可能。
      - 波形データフォーマットは8ビットまたは12ビットリニア。
      - PCMはループ機能とオルタネートループ機能によりデータを節約可能。
      - スロット数は48。
      - LFO内蔵で各スロット毎に波形、周波数、周波数変調、振幅変調の設定が可能。
      - 音声出力サンプリングレートは44.1kHz(マスタークロック16.9344MHz時)。
      - 音声出力は4ch出力可能で、各チャンネルごとにパンの設定可能。
      - パッケージは128ピンQFP。

{{-}}

### OPS系

[thumb](https://ja.wikipedia.org/wiki/ファイル:DX7IIDmainboard.jpg "wikilink") 6オペレータ/16chステレオ/32アルゴリズム。オペレータ部(OP)とエンベロープジェネレータ部(EG)に分離している。入力クロックは9.4265MHz。動作クロックは4.71MHzである。OP部はEGから送られる14bitの周波数データを元にSINテーブルの値を読み、同じくEGから送られる12bitのエンベロープ値を使って出力を決定する。内部データは12bit値とシフト値で構成されているが実際の音声信号を得る手順はOPSとOPSIIで若干異なっており、OPSの場合12bitのデータを12bitD/Aコンバータ(BA9221)に対して出力し、得られた信号をアナログスイッチを通してシフトすることで音声信号を得るのに対し、OPSIIでは12bitのデータを内部でシフト操作して15bitデータに変換した上で16bitD/Aコンバータ(PCM54HP)に出力することで音声信号を得ている。DXシリーズやTXシリーズで使用された為かなりの数量が出回ったが、YM2151のようにICとして外販されたわけではないため、情報が公開されておらず内部レジスタ構成などは一切不明である。

  - YM2128(OPS)+YM2129(EGS)
      - DX7/DX1/DX5/TX216/TX816等で使用。
  - YM2604(OPSII)+YM3609(EGM)
      - DX7IID/DX7IIFD/TX802等で使用。

{{-}}

### その他

[thumb](https://ja.wikipedia.org/wiki/ファイル:315-5687_01.jpg "wikilink")

  - YMF292-F (SEGA 315-5687) SCSP(Saturn Custom Sound Processor) [MODEL3](https://ja.wikipedia.org/wiki/MODEL3 "wikilink")、[セガサターン](../Page/セガサターン.md "wikilink")およびその互換機、[ST-V](https://ja.wikipedia.org/wiki/ST-V "wikilink")などで使用。
  - SCSPはセガサターンのバージョンにより、複数の型番（タイプ）がある。
      - PCM再生データサンプリングレート：DC～44kHz
      - PCMデータ：8ビットまたは16ビットリニア
      - 32ch FMまたはPCM
      - すべてFM 4オペレータで使用した場合、8ch FMサウンド出力
      - すべてPCMとして使用する場合は32ch PCMサウンド出力
      - 1スロットにつき1LFO割り当て可能、32chのLFO使用可能。
      - 32ch エンベロープジェネレータ内蔵
      - プリスケーラ内蔵8ビットデジタルタイマー内蔵
      - デジタルミキサー内蔵
      - ヤマハ製FH-1 DSP内蔵。各種サウンドエフェクト制御
      - リバーブ(ホール、ルーム、ボーカル、プレートなど)
          - 反響
          - エコー/ディレイ(ステレオ、モノラル）
          - ピッチシフタ（シングル、ダブル、トリプル）
          - コーラス、フランジャー
          - 交響曲サラウンド
          - ボイスキャンセル、オートパン
          - 位相、ひずみ
          - フィルター
          - パラメトリックイコライザ
      - 4MビットDRAM接続可能(サウンドCPU 68EC000用プログラム、PCMサウンドデータ、DSP)
      - DMA内蔵。SCSPとDRAM間のデータ転送に使用する。
      - メインCPUインターフェイス：セガサターンの場合はSCUとSCSP間のインターフェイス(B-BUS)となる。
      - サウンドCPUインターフェイス：68EC000とのインターフェイス。
      - 割り込み出力(2ch)：メインシステム用およびサウンドCPU用
      - 外部割込み信号入力：3ch（サターンでは未使用）
      - リセット入力：セガサターンの場合はSMPCから出力されるリセット信号を入力する。
      - デジタルサウンド出力
      - 外部デジタル入力(1ch)
      - MIDIインターフェイス内蔵(入力1ch、出力1ch)
  - YMU757(MA-1)
      - 2オペレータ?FM4ch
      - 4音同時発音
  - YMU759(MA-2)
      - 4オペレータFM8音(または2オペレータ16音)+4bitADPCM(4k/8kHz)1音、ステレオ出力
      - 同時発音数(チップ最大性能)16
  - YMU762(MA-3)
      - 4オペレータFM16音(または2オペレータ32音)+WaveTable音源8音+PCM/ADPCM(4～48kHz)2ストリーム、ステレオ出力
      - 同時発音数(チップ最大性能)40
  - YMU765(MA-5)
      - FM音源部はMA-3と同じ。Wavetable発音数増、フォルマント発声音源(HV)および簡易アナログ音源(AL)を追加。
      - 同時発音数(チップ最大性能)64
  - YMF825(SD-1)
      - 4オペレーター16和音、基本波形29種類から選択、3バンドイコライザーを内蔵。
      - DACと900mwのアンプを内蔵しているため、直接スピーカーを駆動することが可能。
      - 中国市場向け家電用として開発されたが、好事家向け工作キットとしても流通している。\[13\]
  - YMU786/790/791(MA-7/7D/7i)
      - MA-5をベースに、3Dエフェクトプロセッサ・リバーブプロセッサ等を追加。マルチファイル同時再生(4ファイル)およびアプリケーションからのリアルタイムMIDIINコントロールに対応。
      - ピアノ、ストリングスなどWavetable音源の音色追加。
      - ユーザーRAMの容量増加。MA-5の8KBから16KBへ増加。
      - 汎用エフェクタの追加。(ディストーション、オーバードライブなど)
      - 同時発音数(チップ最大性能)128
      - ベースチップYMU786にはアナログ出力ブロック(ミキサー、ヘッドフォンアンプ等)がインテグレートされている。
      - YMU790はYMF786よりアナログ出力ブロックを取り除いたもの。
      - YMU791はYMF786に[ADコンバータ](https://ja.wikipedia.org/wiki/アナログ-デジタル変換回路 "wikilink")、[マイク入力](https://ja.wikipedia.org/wiki/マイクロフォン "wikilink")、[ライン入力](https://ja.wikipedia.org/wiki/ライン_\(音響機器\) "wikilink")、レシーバアンプ等を追加し入出力を集約化したもの。
  - YM2403(OPLP)/YM2404(OPLM)
      - エレクトーンHX-1に搭載。入力クロック3.2MHz。EGに相当するのはYM3807(MOD/Modulation Signal Generator)、D/AコンバータはYM3017である。名称にOPLの文字を含むがOPL系に含まれるのかは不明。
      - HX-1は8オペレータ8chステレオの「FMポリ音色」と16オペレータ1chモノラルの「FMモノ音色」を使用できる。
      - HX-1ではまた4オペレータのFM音源とAWM音源も使用できるがどのチップがFM音源の機能を持つのかは不明。HX-1に搭載された他のヤマハ製音源チップはYM3602(OPRW)YM3604(OPBW)YM2415(OPAW)の何れも名称に'W'の文字を含む3種類である。

## 関連書籍

[ジョン・チョウニング](https://ja.wikipedia.org/wiki/ジョン・チョウニング "wikilink")著、[デビッド・ブリストウ](https://ja.wikipedia.org/wiki/デビッド・ブリストウ "wikilink")著、広野幸治訳『DXシンセサイザーで学ぶFM理論と応用』ヤマハ音楽振興会、1986年、ISBN 4636208358

## 脚注

<references />

## 関連項目

  - [ヤマハ・DXシリーズ](https://ja.wikipedia.org/wiki/ヤマハ・DXシリーズ "wikilink")
  - [ヤマハ・TXシリーズ](https://ja.wikipedia.org/wiki/ヤマハ・TXシリーズ "wikilink")
  - [ヤマハ・SYシリーズ](https://ja.wikipedia.org/wiki/ヤマハ・SYシリーズ "wikilink")
  - [ヤマハ・TGシリーズ](https://ja.wikipedia.org/wiki/ヤマハ・TGシリーズ "wikilink")
  - [シンクラヴィア](https://ja.wikipedia.org/wiki/シンクラヴィア "wikilink")
  - [AudioEngine](https://ja.wikipedia.org/wiki/AudioEngine "wikilink")
  - [LA音源](https://ja.wikipedia.org/wiki/LA音源 "wikilink")

[Category:シンセサイザー](https://ja.wikipedia.org/wiki/Category:シンセサイザー "wikilink") [Category:電子音源の合成方式](https://ja.wikipedia.org/wiki/Category:電子音源の合成方式 "wikilink") [Category:音源チップ](https://ja.wikipedia.org/wiki/Category:音源チップ "wikilink") [Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink")

1.
2.
3.
4.
5.  Daniel J. Levitin, "*This is your brain on music*", Penguin Books, 2006
6.  [1](http://smaf-yamaha.com/jp/what/soundchip_ma7.html)[2](http://smaf-yamaha.com/jp/what/soundchip_ma7.html)
7.  [山佐ホームページ おもいでのニューパルサー 軍艦マーチの終止符を打った男](http://www1.yamasa.co.jp/40th_remnp/interview/int01.html)（2010年6月閲覧）
8.  [シグマSG97VM-1の修理01](http://blog.livedoor.jp/medage/archives/21395641.html)
9.  YM2608 OPNA Application Manual
10. [『頭脳圧搾工場 in 仙台』のページ TOWNS搭載のチップ](http://www.purose.net/befis/towns/chip/)
11. 『マイコンBASIC Magazine DELUXE ゲーム・ミュージック・プログラム大全集III』1989 電波新聞社 pp.23, 28
12.
13. [YMF825Boardの紹介](https://yamaha-webmusic.github.io/ymf825board/intro/)