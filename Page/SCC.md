> この記事は[SCC](https://ja.wikipedia.org/wiki/SCC)から翻訳されています。


**SCC**(**エスシーシー**)はコナミ(後の[コナミデジタルエンタテインメント](https://ja.wikipedia.org/wiki/コナミデジタルエンタテインメント "wikilink"))が開発した[波形メモリ音源](https://ja.wikipedia.org/wiki/波形メモリ音源 "wikilink")兼メモリーバンク制御チップ。  [thumb](https://ja.wikipedia.org/wiki/ファイル:Scc01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Scc02.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/画像:VRC_VI_03.jpg "wikilink")

## 概要

1986年2月頃、同社[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")サウンドプログラム担当の[青木豊](https://ja.wikipedia.org/wiki/青木豊 "wikilink")が[ファミリーコンピュータ ディスクシステムに音源が内蔵されていることをヒントにMSX用拡張音源の要望を出したことがきっかけで](https://ja.wikipedia.org/wiki/ファミリーコンピュータ_ディスクシステム "wikilink")、当時のMSX用ゲームのサウンド担当だった[上原和彦](https://ja.wikipedia.org/wiki/上原和彦 "wikilink")らがアーケードゲーム部門の音楽スタッフと音源の仕様を決めた\[1\]。さらにMSXのROMカートリッジゲーム用のメモリ制御機能を追加した拡張音源として製品化された。表面には2212P003、並びにKONAMI051649と書かれており、これはチップメーカーでの品番とKONAMIでの品番だといわれている。パッケージおよび印刷の外観から東芝製と考えられている。

1990年代以降はアーケードゲーム用基板に[FM音源](https://ja.wikipedia.org/wiki/FM音源 "wikilink")や、[PCM音源](../Page/PCM音源.md "wikilink")等と併せて搭載された。なお、[グラディウス等で使用された](../Page/グラディウス_\(ゲーム\).md "wikilink")[バブルシステム](https://ja.wikipedia.org/wiki/バブルシステム "wikilink")基板の音源は構造が似ているため似た音が出力されるが別の物である。

名称の詳細は諸説あり、MSXに使われた物は正式資料\[2\]によれば、**SOUND CREATIVE CHIP**が正しい。

家庭用ゲームソフトへの搭載は、1987年のMSX用ゲームソフト[グラディウス2](https://ja.wikipedia.org/wiki/グラディウス2 "wikilink")より採用された。

[ファミコン版](https://ja.wikipedia.org/wiki/ファミリーコンピュータ "wikilink")[悪魔城伝説](https://ja.wikipedia.org/wiki/悪魔城伝説 "wikilink")では、カートリッジ内のキャラクターROMにSCC-I(5P72-J802)と記載されており、さらに音源兼メモリバンク制御LSI　[VRC VI](https://ja.wikipedia.org/wiki/VRC_VI "wikilink")(1105-0039)の搭載もみられるが、VRC VIとSCC-Iの関連性について詳細は不明。なおVRC VIの音源部分は波形メモリではなくパルス+[のこぎり波](https://ja.wikipedia.org/wiki/のこぎり波 "wikilink")であり、SCCとは大きく異なる。

## 特徴

  - 同時発声数並びにチャンネル数は5音。
  - 周波数(12ビット)、振幅(ボリューム)(4ビット)のパラメータはMSX本体側の内蔵音源である[PSG](../Page/Programmable_Sound_Generator.md "wikilink")(AY-3-8910)と互換性がある。特に高音域における音程周波数の誤差は大きいものの、音程データを共用できるとして設定された\[3\]。
  - ROMゲームに実装されているSCC(2212P003)では、chDとchEは共通の波形という制限がある。
  - スナッチャーおよびSDスナッチャーに搭載されたSCC-I(2312P001、SCC+の名称が俗称として使われることがある。)は若干の仕様変更が行われており、互換モードの他に、チャンネル毎に任意の波形を生成できる独自のモードを持っている。
  - 波形メモリは32バイトと短めのため、「スペイシー(宇宙的)」と表現される独特な音色となる。
  - 音域が低域になるほど「ブーン」というハムノイズが一緒に発音される。これは矩形波を細かくした音構造になっていることによる。
  - [エンベロープ](https://ja.wikipedia.org/wiki/ADSR "wikilink")(音量の自動減衰)などは搭載されていない。
  - 音声はカートリッジスロットの音声入力を介して、本体側のミキサを通し出力される。リリースされたゲームではPSGも併用しており、最大8音使用していた。ただ、MSXは規格が各社共通だったものの、実際の製品仕様にはバラつきがあったため、SCCの音声が出力されない機種や拡張スロット、ならびに、SCCとPSGの音量バランスが大きく異なる機種も存在する。

## SCCを使用した主なゲーム(50音順)

  - [悪魔城ドラキュラ (アーケード版)](https://ja.wikipedia.org/wiki/悪魔城ドラキュラ_\(アーケードゲーム\) "wikilink") (欧米：[Haunted Castle](https://ja.wikipedia.org/wiki/:en:Haunted_Castle "wikilink"))
  - [F1スピリット](https://ja.wikipedia.org/wiki/F1スピリット "wikilink")(MSX)
  - [王家の谷 エルギーザの封印](https://ja.wikipedia.org/wiki/王家の谷_エルギーザの封印 "wikilink")(MSX1)
  - [王家の谷 エルギーザの封印](https://ja.wikipedia.org/wiki/王家の谷_エルギーザの封印 "wikilink")(MSX2)
  - [クォース](https://ja.wikipedia.org/wiki/クォース "wikilink")(MSX2)
  - [グラディウス2](https://ja.wikipedia.org/wiki/グラディウス2 "wikilink")(MSX)
  - [激突ペナントレース](https://ja.wikipedia.org/wiki/激突ペナントレース "wikilink")(MSX2)
  - [激突ペナントレース](https://ja.wikipedia.org/wiki/激突ペナントレース "wikilink")2(MSX2)
  - [ゴーファーの野望 エピソードII](https://ja.wikipedia.org/wiki/ゴーファーの野望_エピソードII "wikilink")(MSX)
  - [沙羅曼蛇(MSX)](https://ja.wikipedia.org/wiki/沙羅曼蛇_\(MSX\) "wikilink")
  - [シティボンバー](https://ja.wikipedia.org/wiki/シティボンバー "wikilink")(アーケード)
  - [スペースマンボウ](https://ja.wikipedia.org/wiki/スペースマンボウ "wikilink")(MSX2)
  - つりっ子ペン太（アーケード キッズメダル機）
  - [にゃんにゃんパニック](https://ja.wikipedia.org/wiki/にゃんにゃんパニック "wikilink")(アーケード)
  - [パロディウス](https://ja.wikipedia.org/wiki/パロディウス#パロディウス_〜タコは地球を救う〜 "wikilink")(MSX)
  - [魂斗羅](https://ja.wikipedia.org/wiki/魂斗羅 "wikilink")(MSX2)
  - [ヘクシオン](https://ja.wikipedia.org/wiki/ヘクシオン "wikilink")(アーケード)
  - [メタルギア2 ソリッドスネーク](https://ja.wikipedia.org/wiki/メタルギア2_ソリッドスネーク "wikilink")(MSX2)

以下の作品にはSCC-I搭載のSCC音源カートリッジが単独で付属しており、64KiBの[DRAM](https://ja.wikipedia.org/wiki/DRAM "wikilink")を搭載している。

  - [スナッチャー](https://ja.wikipedia.org/wiki/スナッチャー "wikilink")(MSX2、SCC-I使用)
  - [SDスナッチャー](https://ja.wikipedia.org/wiki/スナッチャー "wikilink")(MSX2、SCC-I使用)

### メモリバンク制御チップとしてのSCC

SCCのメモリバンク制御の機能としては、1バンクの大きさは8KiB固定で、バンクレジスターは6ビット長の物が4つ用意されているため、それらの制御によって512KiBの空間を管理することを可能にしている。ROMゲームカートリッジとしてはその空間にROMが接続され、前述の拡張音源とともに利用されている。単体での発売はされていないが、MSX版スナッチャーならびに、SDスナッチャーでは、該当ソフトウェアでのディスク[キャッシュを目的としてSCCに接続された](https://ja.wikipedia.org/wiki/キャッシュ_\(コンピュータシステム\) "wikilink")64KiBのRAMを搭載しており、128KiB分のメモリを搭載可能なほぼ同等の回路で構成されている。但し、チップに対して接続されているRAMが、スナッチャーのカートリッジではアドレスの前半、SDスナッチャーでは後半に実装されており、相互に交換して使うことは出来ない。スナッチャーや、SDスナッチャーはこれらのキャッシュを前提に設計されているため、ハードウェア[ドングル](https://ja.wikipedia.org/wiki/ドングル "wikilink")としての役割も担っている。また、後に発売された「コナミゲームコレクション」では一部のゲームにSCC音源用BGMが収録されており、これは「スナッチャー」付属カートリッジに対応して演奏されたが、SDスナッチャーのカートリッジは前述の実装アドレスの都合から認識しない。二つのSCCカートリッジは基板自体は同じであるため、SDスナッチャーの方でも空きパターンにメモリを実装することで、上記のゲームにおいて、認識させることが可能になる。多くのMSX用の拡張ハードウェアと異なり、このカートリッジには制御用のBIOSなどのソフトウェアは搭載されていない。SCC自体の持つメモリ管理機能によって、コナミ8Kバンク方式のROMイメージを、搭載されたRAM上に転送することで、ソフトウェアを実行することも可能である。なお、日本のユーザー間の一部ではこれらの仕組みを利用し、SCCを搭載したROMカートリッジを使用し、[SRAM](https://ja.wikipedia.org/wiki/SRAM "wikilink")と[キャパシタによるバックアップ可能なメモリカートリッジとして](https://ja.wikipedia.org/wiki/コンデンサ "wikilink")、似非SCC DISKと呼ばれる同人ハードウェアの作例が、頒布され、作成されたりしていた。

### コナミのSCCによる作曲傾向

コナミが当時SCCを用いて作曲した際の傾向として『金属的な[ブラス系の音をメロディーに用いる](../Page/金管楽器.md "wikilink")』ことが多かった。音抜けが良く印象に残りやすいことから多用されたことが見受けられる。

当時、PSG単体による楽曲ではデチューン(2つのチャンネルで僅かにずれた音程を発音しコーラス効果を得る)が主に用いられていた。SCCとPSGによる楽曲においてもグラディウス2などでデチューンが用いられているが、音程だけでなく音色をずらす(各チャンネルにおいて異なる波形で同旋律を発声させる)など多彩な表現が行われていた

アーケード版グラディウスの音源構成(PSG 6ch, K005289(波形メモリ音源) 2ch)に近いため、本体側のPSGとSCCを併用することでその音をMSX上で再現することも理論上は可能であるが、MSX版グラディウスの発売時にはまだSCCが存在しておらず内蔵音源であるPSGのみの対応となった。後に『コナミゲームコレクション Vol.3』にネメシスの名称でリメイクされスナッチャーのSCCカートリッジに対応したが、その際には独自の新規アレンジによるBGMデータが収録されている。

## DTM音源としてのSCC

ソフトウェアの添付品という側面から、市販されたハードウェアとしては珍しく、カートリッジに制御BIOSなどを持っておらず、マニュアルに資料が掲載されるなどしているわけでもなかったため、当初はユーザーからの利用は困難な状況にあった。

ユーザーに制御方法が知られるようになったのは、[マイコンBASICマガジン](https://ja.wikipedia.org/wiki/マイコンBASICマガジン "wikilink")が1989年7月号から、MSXでスナッチャー付属のSCC音源カートリッジを制御するという解析記事を連載したためである。連載では、完全ではないものの大部分の内容を解説と、それを補完するツールなどの掲載が行われている。

その後、1990年に[MSXマガジン](https://ja.wikipedia.org/wiki/MSXマガジン "wikilink")で発表された音楽ソフト[MuSICA](https://ja.wikipedia.org/wiki/MuSICA_\(ソフトウェア\) "wikilink")([ソフトベンダーTAKERU](https://ja.wikipedia.org/wiki/ソフトベンダーTAKERU "wikilink")販売の「MSXディスク通信'90年10月号」に収録)には、MSX版スナッチャー及びSDスナッチャーに付属するSCC音源カートリッジを制御、演奏させる機能があった。のちに同誌で、SCCを制御するためのコナミ提供の公式仕様が掲載され、草の根BBSなどで発表されたMGSDRVなど、フリーソフトでも対応する動きが広がった。

SCC音源カートリッジは単体としては流通しておらず、後にスナッチャー・SDスナッチャー共に中古市場でプレミア扱いされたことにより正規に販売されたものを入手するのは困難となり、実際の流通量は少なかった。しかし、コナミのSCC搭載のMSX用ゲームはユーザーに広く普及していたため、ゲームカートリッジをゲームが起動しないように改造して用いる方法や、MSX起動後に後からカートリッジを差す方法が考案された。そのため、かなり多くのユーザーがSCC音源を自由に利用可能になっていた。ただ、MSXが電源オン状態でもカートリッジの抜き差しは物理的には可能だが、本体やカートリッジはその動作を想定して作られていないため、後者の方法は抜き差し時の電流や信号によって精密回路を破損する恐れがあった。

後差し方法については、誤動作を抑えるために、Shiftキーを押しながらカートリッジを差し込む方法や、PAUSEボタンでシステムを強制停止させている間に差し、PAUSEを解除する方法が知られている。PAUSEボタンを用いる方法の方が安全性は高いといわれているが、PAUSEボタン搭載機種はFS-A1シリーズ以降の松下製MSX数機種と同時期以降のソニー製数機種のみであり、[turboRではPAUSEのハードウェア的な実装が変更されているので](https://ja.wikipedia.org/wiki/MSXturboR "wikilink")、回路のタイミングが停止しない。また、いずれにしても電源オン状態でスロットに無理やり挿入していることには変わりはなく、故障の原因となる可能性が高かった。

なお、現在はMSX[エミュレータ](https://ja.wikipedia.org/wiki/エミュレータ "wikilink")やSCC互換音源を搭載した[1チップMSX](https://ja.wikipedia.org/wiki/1チップMSX "wikilink")など、SCC相当の音源を利用できる環境は多く存在する。

SCC対応の演奏ソフトが普及した当時は、既に[FMPAC](https://ja.wikipedia.org/wiki/FMPAC "wikilink")や[MSX2+](https://ja.wikipedia.org/wiki/MSX2+ "wikilink")の登場によってFM音源([YM2413](https://ja.wikipedia.org/wiki/YM2413 "wikilink")(OPLL))もまた普及しており、標準的なMSXの環境ではPSG3音+FM音源9音+SCC5音で最大17音が出せ、音を重ね合わせることで深みのある音楽を奏でることが出来た。FM音源搭載MSXとコナミのSCC搭載ゲームの組み合わせで、同時期に流通していた[PC9801](https://ja.wikipedia.org/wiki/PC9801 "wikilink")や[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")等に比べ非常に安価かつ手軽にDTM環境を構築する事が可能であった。

### チップチューンにおけるSCC

近年の[チップチューン](https://ja.wikipedia.org/wiki/チップチューン "wikilink")ブームにより初期のビデオゲーム音源が見直されて来ているが、SCCも当時を代表する音源の1つとして人気がある。波形メモリ音源としてコナミのゲーム音のみならず、ナムコの業務用ゲーム音やPCエンジンの音を再現することも可能である。

しかしファミコンに比べ音源の認知度、発音環境、音源を制御し作曲できる人口の少なさにより、SCCを扱うミュージシャン・楽曲ともに数が少ない。

## 参考

  - [波形メモリ音源](https://ja.wikipedia.org/wiki/波形メモリ音源 "wikilink")
  - [バブルシステム](https://ja.wikipedia.org/wiki/バブルシステム "wikilink")
  - [チップチューン](https://ja.wikipedia.org/wiki/チップチューン "wikilink")
  - [ゲームミュージック](https://ja.wikipedia.org/wiki/ゲームミュージック "wikilink")
  - [上原和彦](https://ja.wikipedia.org/wiki/上原和彦 "wikilink") SCC開発者の一人。現コナミデジタルエンタテインメント執行役員シニアヴァイスプレジデント

## 脚注

<references/>

[Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink") [Category:コンピュータゲームの技術](https://ja.wikipedia.org/wiki/Category:コンピュータゲームの技術 "wikilink") [Category:コンピュータミュージック](https://ja.wikipedia.org/wiki/Category:コンピュータミュージック "wikilink") [Category:コナミデジタルエンタテインメント](https://ja.wikipedia.org/wiki/Category:コナミデジタルエンタテインメント "wikilink") [Category:MSX](https://ja.wikipedia.org/wiki/Category:MSX "wikilink") [Category:音源チップ](https://ja.wikipedia.org/wiki/Category:音源チップ "wikilink") [Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink")

1.  「音楽のこころ コナミのSCCにせまる\!\!」MSXマガジン 1990年9月号 P.66
2.  MSXマガジン 1990年9月号 P.67掲載写真 コナミ提供のSCCの技術資料。表紙に｢MSX｣の表記がある。
3.  「音楽のこころ コナミのSCCにせまる\!\!」MSXマガジン 1990年9月号 P.66 上原和彦、青木豊 談