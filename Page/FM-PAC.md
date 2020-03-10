> この記事は[FM-PAC](https://ja.wikipedia.org/wiki/FM-PAC)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:FM-PAC_01.jpg "wikilink")

**FM-PAC**(えふえむぱっく)は、[松下電器産業（現：パナソニック）より](https://ja.wikipedia.org/wiki/パナソニック "wikilink")[1988年](../Page/1988年.md "wikilink")に発売された日本の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")、[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")シリーズ用の[拡張カートリッジであり](https://ja.wikipedia.org/wiki/拡張カード "wikilink")、正式名称は「FM Pana Amusement Cartridge」。[パナアミューズメントカートリッジ](https://ja.wikipedia.org/wiki/パナアミューズメントカートリッジ "wikilink")と同様の一部のゲームなどに対応した[バッテリーバックアップ](https://ja.wikipedia.org/wiki/バッテリーバックアップ "wikilink")メモリ、並びに[YM2413](https://ja.wikipedia.org/wiki/YM2413 "wikilink")を搭載し、MSXに9重和音、もしくは6重和音 + [ドラムセット](../Page/ドラムセット.md "wikilink")5音の演奏環境と、対応ゲームに対するデータのセーブを実現する。[希望小売価格](../Page/希望小売価格.md "wikilink")は7800円。

## 概要

FM-PACは「FM Pana Amusement Cartridge」を省略した呼び方である。そのほか、「FM PAC」または「FM P.A.C.」と略される\[1\]。使用に際してはMSX本体の[RAMが](../Page/Dynamic_Random_Access_Memory.md "wikilink")32KB以上必要である\[2\]。

カートリッジの形態を取り、MSXの[拡張スロット](https://ja.wikipedia.org/wiki/拡張スロット "wikilink")に挿入することで、標準では[PSGが](../Page/Programmable_Sound_Generator.md "wikilink")3[チャンネル](https://ja.wikipedia.org/wiki/チャンネル "wikilink")のみの出力しか持っていなかったMSXでそれに加えて、2オペレータ、モノフォニック、9和音または6和音＋リズム5和音の発音にする。

複数のスロットを備えたMSXで同時に挿入することで、ROMカートリッジで供給するゲームでも利用可能である。この[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")は「MSX-MUSIC」と呼ばれる。

また、ゲームソフトなどのセーブデータを保存するために8[KBの](https://ja.wikipedia.org/wiki/キロバイト "wikilink")[SRAMを搭載しており](../Page/Static_Random_Access_Memory.md "wikilink")、8つのセグメントに分けて利用が可能と\[3\]、[パナアミューズメントカートリッジ](https://ja.wikipedia.org/wiki/パナアミューズメントカートリッジ "wikilink")と同等の機能を持つ。この機能は対応ソフトウェア以外では使用できない。データをマネジメントするアプリケーションも内蔵されている(後述)。

縦210mm、幅108mm、厚さ17mmと\[4\]、一般的なMSX用カートリッジに比べて、やや背高のサイズとなっている。FM音源はMSX本体の内部を通り、本体の音声出力端子から、PSGとミックスされた音が出力される。カートリッジ上部にスライドスイッチがあり、FM音源のボリュームは3段階に切り替えて\[5\]\[6\]、本体内蔵のPSG音源との音量バランスを調整できる。

## サンプル曲

「パックコマンダー」にサンプル曲が全5曲収録されている。 サンプル曲1・2を[浅倉大介](../Page/浅倉大介.md "wikilink")が、3～5をK.OZAWAが作曲したとされている。浅倉大介担当の1・2はそれぞれ、[松下電器産業](https://ja.wikipedia.org/wiki/松下電器産業 "wikilink")発売・[T\&E SOFT開発による](https://ja.wikipedia.org/wiki/T&E_SOFT "wikilink")[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")用ゲームソフト「[アシュギーネ 虚空の牙城](https://ja.wikipedia.org/wiki/アシュギーネ_虚空の牙城 "wikilink")」のステージ1、オープニングデモの曲をFM音源アレンジしたものである。ただし、T\&E SOFTのコンポーザーで、MBIOSの設計者である[冨田茂](https://ja.wikipedia.org/wiki/冨田茂 "wikilink")によると、FM-PACサンプル曲のうち1曲は富田担当との事である\[7\]。

## MSX-MUSIC

MSXの標準拡張音源規格として本来は[MSX-AUDIO](https://ja.wikipedia.org/wiki/MSX-AUDIO "wikilink")が準備されていたが、MSXのオプション機器として製品化されたFS-CA1が34,800円と高価な上に、ほとんど普及しなかったため、低コスト版として開発された\[8\]。MSX-AUDIO規格と比べて、FM音源チップに廉価なものが使用され、MSX-AUDIOではPCMなどの取り扱いに必要だったRAMなどパーツや、出力も、拡張スロットの音声入力を使用するなどの簡略化によって、大幅なコストダウンが達成されている。なお、MSX-AUDIOの音色が、カートリッジ内のROM内に定義されたものであるのに対し、MSX-MUSICで採用された、YM2413はチップそのものに内蔵された音色が存在し、固定されているため、音名が同じであっても、プリセット音は、同じ出力を得られるわけではない。

ハードウェアとして、「YM2413」、ソフトウェアとして、「拡張BASIC」と、「FM BIOS」で構成され、他のMSXの拡張ハードウェアと異なり、拡張BIOSは提供されず、FM BIOSをマッピングした上で、直接エントリアドレスをコールする実装になっている。

本製品発売後リリースされたMSX2用のアプリケーションにおいても、多くのソフトウェアが対応した。MSX2+ではオプション扱いの規格であるが、MSX2+機で実際にMSX-MUSICを搭載しなかった機種は松下「FS-A1FX」などごく一部に限られており、事実上の標準搭載機能となっている。後に制定されたMSXturboRにて正式に標準機能となった。使用するにはMSX本体の[RAMが](../Page/Random_Access_Memory.md "wikilink")32KiB以上必要である\[9\]。

後述のMML節にあるとおり、通常利用される[平均律](../Page/平均律.md "wikilink")以外の音律を指定できることも、他の純正MMLや、音源ドライバには見られない特徴である。

尚、FMPACの発売時期が、MSX2と、MSX2+の間で、MSX2+の規格の記載されたドキュメントから記載が登場した事などから、メーカーオプションとして発売されたものが、規格として取り込まれたとされることが多いものの、規格として、内蔵デバイスと、外付けデバイスでは、仕様が異なって予め定義されている。MSX-AUDIOと違い、用意されたI/Oポートは、1つ分であるため、複数のYM2413を制御するようにはなっておらず、複数装備された環境では、初期化処理によって内蔵、外付けとハードウェアを探し、初期化処理で排他制御するようにドキュメントで明示されている。挙動としてはほぼ同一ではあるものの、外付けデバイスでは、メモリマップドI/Oのアドレスが、定義されているほか、I/Oポートの競合などを回避するため、初期化処理によって、I/Oポートを有効化してやらないと動作しない。それらの条件から、正常に動作させるためには、ソフトウェア側では、正規の手順で、スロットの検索、初期化処理を行う必要があり、特定の構成のみを想定した設計になっているソフトウェアの一部では、内蔵デバイスや差し込む場所などによって鳴らないという状況が発生している。

このように複数のYM2413を独立制御できないようになってはいるものの、MSX-AUDIOとは、別のリソースが割り振られているため、ハードウェア的に共存は可能になっており、海外のMEGA-DEMO等のソフトウェアの一部では、MSX-AUDIOと、MSX-MUSICを左右別チャンネルに接続することで、ステレオとして取り扱うソフトウェアも存在する。

ドライバにあたるFM BIOSは、当時T\&E SOFTに在籍していた、前述の富田茂による設計とコーディングである。\[10\]

1989年11月に発売された、『[マイコンBASICマガジン](../Page/マイコンBASICマガジン.md "wikilink")』の別冊である『MSX/MSX2/MSX2+ ゲーム・ミュージック・プログラム大全集』では、多くの使用曲が収録された。

最初の商用化された実装であるFM-PACは爆発的なヒットを記録し、他機種のゲームをも含めたヒットチャートでベスト3入りを記録した上、パーソナルコンピュータ全般を取り扱う『マイコンBASICマガジン』誌上の音楽プログラム投稿コーナーへの投稿の8割がMSX-MUSIC用のデータで占められたとされ\[11\]、また1989年5月から1990年4月までに実際に掲載された音楽プログラム61本のうち、15本がMSX-MUSICのものであった。\[12\]。

## パナアミューズメントカートリッジとして

8KBのSRAMにソフトウェアの状態保存などを行う。「パックコマンダー」というデータ管理用[ユーティリティソフト](https://ja.wikipedia.org/wiki/ユーティリティソフト "wikilink")がROMに内蔵されており、演奏機能などのおまけ機能もついていた。[BASIC](../Page/BASIC.md "wikilink")上から「CALL FMPAC」と命令する事で、起動が可能である\[13\]。

前身である、パナアミューズメントカートリッジ同様、通常、SRAMはシステムからは切り離されており、メモリマップドI/O経由で、スロットに対し、SRAMを割り当てる処理を行うことで、アクセスが可能になる。\[14\]。当時MSX用の[FDDは高価であり](https://ja.wikipedia.org/wiki/フロッピーディスクドライブ "wikilink")、また、ちょうどFDD内蔵MSX2への切り替わりの時期に相当したため、ロムカートリッジで供給されたゲームの中には、高価なFDDには対応せずにPACにのみ対応したタイトルが少なからず存在している。また、例外的にFDで供給されたにもかかわらず保存をFDに行えないゲームも存在した。数年後、FDDを内蔵したMSX2やMSX2+の普及した時期には逆に、FM-PACを持っていないとデータを保存できない問題も発生した。

## BASICからのMSX-MUSICの使用

FM音源制御命令はCALL命令のセットとして拡張されている。以下に主な命令とその使用法を述べる。

基本仕様はMSX-AUDIOの記述に準拠し、内蔵音色などは異なるものの、音名、パラメータなどは、互換性を意識したつくりとなっている。

  - CALL MUSIC(1,0,1,1,1,1,1,1)
    FM音源[BIOSを起動する](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")。左端の値(0/1)でFM9チャンネル、FM6チャンネル+リズム5チャンネルのモードを切り替える。上記の様に1とした場合はリズムモードとなり、PLAY \#2命令の各チャンネルに、FM音源1チャンネルを割り当てる。CALL MUSIC(1,0,2) などとして、複数チャンネルを割り当てることもできる。第2パラメータの0はMSX-AUDIOの「CALL AUDIO」命令との表記上の互換性のために残されているものであり、MSX-MUSIC上では常に0を設定する\[15\]\[16\]。
  - CALL VOICE(@0,@12)
    FM音源の各チャンネルに音色を設定する。チップ内蔵の15の音色以外は自作音色扱いとなり、1セットしかない自作音色用レジスタを占有してしまうため、同時に1種類しか使用できない。BASICの各命令の実行と、音源の演奏は標準設定では同期しておらず、このコマンドは主に演奏開始前に使用され、曲中での音色変更には通常、[MMLの](../Page/Music_Macro_Language.md "wikilink")@コマンドを用いる\[17\]。
  - CALL TEMPER(9)
    [音律](https://ja.wikipedia.org/wiki/音律 "wikilink")を設定できる\[18\]。
  - CALL VOICE COPY(@63, tone%)
    音色データエリアと任意の配列変数間でデータをコピーする。データサイズは32[バイト](../Page/バイト_\(情報\).md "wikilink")。[MSX-BASIC](../Page/MSX-BASIC.md "wikilink")では[整数型](https://ja.wikipedia.org/wiki/整数型 "wikilink")が2バイトなので、dim tone%(15) と定義されるのが一般的である。上記の例では音色番号63に配列変数tone%の内容をコピーしているが、逆の動作なども可能である。MSX-MUSICでは@0から@62まではプリセットの音色があり、慣例的に自作音色は63から使用されることが多かった。一般的には音色設定は以下のように行われる。

`DIM TONE%(15):FOR I=0 TO 15:READ A$:TONE%(I) = VAL("&H" + A$):NEXT`
`DATA 0000,0000,0000,0000`
`DATA 0000,0000,0000,0000`
`DATA 0000,0000,0000,0000`
`DATA 0000,0000,0000,0000`
`CALL VOICE COPY(TONE%, @63)`

  -
    曲中で複数の音色を使用する時は、PLAY文の合間に CALL VOICE COPY 文を挟むことで行う。
    音色設定にはFM音源のパラメータを直接（人間にとって自然に）表記して上記の32バイト配列にコンバートする手法や、FM音源チップのレジスタに直接値を書き込むコマンドの「Yコマンド」をMML中に用いる手法もあった。前者の変換プログラムは比較的に複雑なものになる\[19\]。後者では演奏中に臨機応変に音色を変化させることができる。
  - PLAY \#2, "C", "D", A$
    MMLに従い演奏を行う。従来の「PLAY」文が拡張されたものである。上記の右端の例の通り文字列変数も使用可能であり、むしろその方が一般的である。どの桁がFM/PSGのどのチャンネルを演奏するかは、CALL MUSICでの設定による。従来のPLAY文と違い、32分音符もある程度ズレなく演奏させることができる。標準設定では演奏はBASICの実行とは非同期に（自動的に）演奏される。なお、1度のPLAY分で流し込めるMMLの長さはMSX-BASICにより制限される。第1パラメータから順に、FM音源チャンネル(0～6個)、リズムチャンネル(0～1個）、PSGチャンネル(3個)となっている。
  - CALL PITCH(440) / CALL TRANSPOSE(n)
    MSX-MUSICでは、チューニングの変更も可能で、CALL PITCHではA4音の周波数を指定する。デフォルトでは440となっている\[20\]。また、CALL TRANSPOSE を用いて、1セント(半音の1/100)単位でプラスマイナス12799セントの移調も可能\[21\]。

## MML

[MMLは一般的なものと大差ない](../Page/Music_Macro_Language.md "wikilink")。MSX-MUSICでの[方言](../Page/方言.md "wikilink")や特徴として、以下のようなものがある。

  - オクターブ変更は \> で上昇、 \< で下降。当時としては一般的な記法である。
  - { } で音譜を括る事で[連符](https://ja.wikipedia.org/wiki/連符 "wikilink")となる。
  - @Vコマンドで[音量](https://ja.wikipedia.org/wiki/音量 "wikilink")を128段階に細かく設定できる。実際は内部では16段階に変換されるが、変数を持ち込む処理などで有益である。
  - Qコマンドを用いることで[スタッカート](https://ja.wikipedia.org/wiki/スタッカート "wikilink")や[レガート](https://ja.wikipedia.org/wiki/レガート "wikilink")を表現できる。8段階で調整可能。同様の表現を行うのに2000年代現在の[デスクトップミュージック](../Page/デスクトップミュージック.md "wikilink")(DTM)では[ゲートタイム](https://ja.wikipedia.org/wiki/ゲートタイム "wikilink")と呼ばれることが多い。
  - Tコマンドでテンポが設定される。MSXの[タイマ割り込みは](https://ja.wikipedia.org/wiki/割り込み_\(コンピュータ\)#CPUの割り込み "wikilink")1/60秒単位でしか発生しないため、音の長さが n(整数)/60秒 で表せない時には、テンポにずれが生じる。計算上、14400÷テンポ÷使用したい音譜(1-64)の解が整数であれば、問題はない。テンポが30の倍数の場合は、比較的好ましい結果になる場合が多い。[Music Macro Language\#システム上の制約と対策も参照されたし](https://ja.wikipedia.org/wiki/Music_Macro_Language#システム上の制約と対策 "wikilink")。

最も大きな点は、リズム音源演奏専用MMLの存在である。これは一般的なMMLとは全く異なり、例えば典型的な[8ビート](https://ja.wikipedia.org/wiki/8ビート "wikilink")であれば、

`B!H8H8SH8H8 B!H8BH8SH8H8`

となる。B:[バスドラム](https://ja.wikipedia.org/wiki/バスドラム "wikilink") S:[スネアドラム](../Page/スネアドラム.md "wikilink") H:[ハイハット](https://ja.wikipedia.org/wiki/ハイハット "wikilink") M:[タムタム](https://ja.wikipedia.org/wiki/タムタム "wikilink") C:[シンバル](../Page/シンバル.md "wikilink") となっており、可読性に難はあるものの、1まとまりのMMLで複数の打楽器を鳴らせる仕様となっている。なお、\!はアクセントとして、音量を通常のものとは異なる値に変化させる修飾コマンドである\[22\]。必ずしも音量が上がるわけではない。

## BASICでの演奏の限界

BASICでの演奏では[ポルタメント](https://ja.wikipedia.org/wiki/ポルタメント "wikilink")が行えない、[ビブラート](../Page/ビブラート.md "wikilink")が再現できない、という問題があった。直接レジスタを制御するYコマンドで実現は可能であるが、直接送り込むデータを列挙するため、非常に煩雑でMMLの可読性を著しく損なう。

MSX-MUSICのパーカッションの音色は、よく出来ているとは言い難く、多用されるスネアドラム等に対しては、音色を加工する方法としてPSGのノイズを重ねたり、PSGに割り振るなどし、音階が存在しなかった[タムタム](https://ja.wikipedia.org/wiki/タムタム "wikilink")に対しては、Yコマンドにより、直接チップに対して音程を指定する等の試行錯誤が見られた\[23\]。電波新聞社刊、『MSX2/2+ ゲーム・ミュージックプログラム大全集』(1989, 電波新聞社)および『MSX2/2+ ゲーム・ミュージックプログラム大全集II』(1990, 電波新聞社)では実際に、掲載されているFM-PAC対応演奏プログラムの多くで、ドラムスの演奏にこのような工夫が見られる。

更にBASIC上でFM音源BIOSの[ワークエリア](https://ja.wikipedia.org/wiki/ワークエリア "wikilink")に直接値を書き込み、周波数のわずかに異なる2音を重ね[デチューン効果を得る方法が確立されている](../Page/コーラス_\(音響機器\).md "wikilink")。\[24\]。

なお、PSGパートでは、タイマ割り込みとPSGのレジスタの直接変更（MSXの場合はBIOSで行える\[25\]）を用いたビブラート、コーラス、[ソフトウェアエンベロープ](../Page/ADSR.md "wikilink")、[シンセタムなどの技法はFM](https://ja.wikipedia.org/wiki/ドラムセット#バリエーション#エレクトリックドラム "wikilink")-PAC発売以前から行われている。これらについても『マイコンBASICマガジン』(1988年以降)、『ゲーム・ミュージック・プログラム大全集III』(1988, 電波新聞社)、『MSX2/2+ゲーム・ミュージックプログラム大全集』(1989, 電波新聞社)および『MSX2/2+ゲーム・ミュージックプログラム大全集』(1990, 電波新聞社)などで多くの実例が見られる。

## チップ内蔵音色

音色用レジスタを占有する音色も含めると、MSX-MUSICでは64種(無音含む)\[26\]の音色が用意されている。以下のものは制限無く使えるチップ内蔵音色である。何分この他には同時に1音色しか使用できないため、ほとんどのMSX-MUSIC用演奏データはそのほとんどの部分がこの15種の音色だけで演奏されている。なおチップ内では音色番号は0 - 15の値を取っており、下記の音色番号はMSX-MUSIC側が独自に割り振ったものである。また、取扱説明書p.44によれば、音色名については「参考のために付けたもので音色によっては、実際の楽器の音と異なることがあります。」ということになっている。

  - @0 [ピアノ](../Page/ピアノ.md "wikilink")1 （デフォルト）
  - @2 [ヴァイオリン](../Page/ヴァイオリン.md "wikilink")
  - @3 [フルート](../Page/フルート.md "wikilink")
  - @4 [クラリネット](../Page/クラリネット.md "wikilink")
  - @5 [オーボエ](../Page/オーボエ.md "wikilink")
  - @6 [トランペット](../Page/トランペット.md "wikilink")
  - @9 [オルガン](../Page/オルガン.md "wikilink")
  - @10 [ギター](../Page/ギター.md "wikilink")
  - @12 [エレキベース](https://ja.wikipedia.org/wiki/エレキベース "wikilink")（YM2413のアプリケーションマニュアルでは「Electric Guitar」とされている）
  - @14 [ハープシコード](https://ja.wikipedia.org/wiki/ハープシコード "wikilink")
  - @16 [ビブラフォン](https://ja.wikipedia.org/wiki/ビブラフォン "wikilink")
  - @23 [シンセ・ベース](../Page/シンセベース.md "wikilink")
  - @24 [シンセサイザ](https://ja.wikipedia.org/wiki/シンセサイザ "wikilink")
  - @33 [ウッドベース](https://ja.wikipedia.org/wiki/ウッドベース "wikilink")
  - @48 [ホルン](../Page/ホルン.md "wikilink")

## FM音源BIOS内蔵音律

メジャーはMと、マイナーはmと略記した。取扱説明書 p.45を参考とした。

  - 0 [ピタゴラス](../Page/ピタゴラス音律.md "wikilink")
  - 1 [ミーントーン](https://ja.wikipedia.org/wiki/中全音律 "wikilink")
  - 2 [ヴェルクマイスター](https://ja.wikipedia.org/wiki/ヴェルクマイスター音律 "wikilink")
  - 3 ヴェルクマイスター（修正）
  - 4 ヴェルクマイスター（別）
  - 5 [キルンベルガー](../Page/キルンベルガー第3法.md "wikilink")
  - 6 キルンベルガー（修正）
  - 7 ヴァロッティ・ヤング
  - 8 [ラモー](https://ja.wikipedia.org/wiki/ジャン＝フィリップ・ラモー "wikilink")
  - 9 [完全平均律](../Page/平均律.md "wikilink")(デフォルト)
  - 10 [純正律](../Page/純正律.md "wikilink") c M (a m)
  - 11 純正律 cis M (b m)
  - 12 純正律 d M (h m)
  - 13 純正律 es M (c m)
  - 14 純正律 e M (cis m)
  - 15 純正律 f M (d m)
  - 16 純正律 fis M (es m)
  - 17 純正律 g M (e m)
  - 18 純正律 gis M (f m)
  - 19 純正律 a M (fis m)
  - 20 純正律 b M (g m)
  - 21 純正律 h M (gis m)

## MSX用のその他の音源関係オプション

  - [MSX-AUDIO](https://ja.wikipedia.org/wiki/MSX-AUDIO "wikilink") - 先発の規格。国内で広く普及することは無かった。
  - FM Sound Synthesizer Unit II - SFG-05 [YAMAHA](https://ja.wikipedia.org/wiki/YAMAHA "wikilink")から発売された拡張音源ユニット。[YM2151](https://ja.wikipedia.org/wiki/YM2151 "wikilink")(OPM)を搭載し、[MIDI](../Page/MIDI.md "wikilink")端子も装備。希望小売価格29,800円。ただし通常のカートリッジスロットとは異なる独自の形式を持ち、YAMAHA社や[ビクター](https://ja.wikipedia.org/wiki/ビクター "wikilink")社製のMSX以外では別売のアダプターが必要だった。[ミュージックシーケンサー](https://ja.wikipedia.org/wiki/ミュージックシーケンサー "wikilink")や拡張BASICも供給された。[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")の項目も参照。
  - MIDIサウルス - 1990年に[BIT2](https://ja.wikipedia.org/wiki/BIT2 "wikilink")より発売された、MIDIインターフェイス。[ミュージックシーケンサー](https://ja.wikipedia.org/wiki/ミュージックシーケンサー "wikilink")がFDで付属。メロディー8トラック、リズム1トラック、最大16音ポリフォニック\[27\]。四分音符の分解能は96または48\[28\]。希望小売価格19800円。[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")の項目も参照。

## 脚注

## 参考文献

  - 『YM2413 FM Operator Type-LL (OPLL) Application Manual』 YAMAHA [1](http://www.smspower.org/maxim/Documents/YM2413ApplicationManual) OPLLについての詳細な仕様書。

  -
  - \- MSX-BASIC上でのMSX-MUSICプログラミングの実例が多数紹介されている。若干の入門講座もある。

  - \- MSX-BASIC上でのMSX-MUSICによるプログラミング手法、および拡張命令が詳細に解説されているほか、音楽の基礎知識についても解説がなされている。

  -
## 関連文献

  - \- MSX-MUSICとは直接の関係は無いが、その他の拡張音源に対しての記述がある。

## 関連項目

  - [MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")
  - [FM音源](../Page/FM音源.md "wikilink")
  - [内蔵音源](https://ja.wikipedia.org/wiki/内蔵音源 "wikilink")
  - [MSX-BASIC](../Page/MSX-BASIC.md "wikilink")
  - [SCC](../Page/SCC.md "wikilink") [コナミ](https://ja.wikipedia.org/wiki/コナミ "wikilink")の開発したMSX用音源チップ。
  - [MGSDRV](https://ja.wikipedia.org/wiki/MGSDRV "wikilink") フリーの演奏[ドライバ](https://ja.wikipedia.org/wiki/ドライバ "wikilink")。
  - [Music Macro Language](../Page/Music_Macro_Language.md "wikilink")
  - [パナアミューズメントカートリッジ](https://ja.wikipedia.org/wiki/パナアミューズメントカートリッジ "wikilink")
  - [内蔵音源](https://ja.wikipedia.org/wiki/内蔵音源 "wikilink")
  - [マイクロキャビン](https://ja.wikipedia.org/wiki/マイクロキャビン "wikilink") - MSX版の[ファイナルファンタジー](https://ja.wikipedia.org/wiki/ファイナルファンタジー "wikilink")、[サーク](../Page/サーク.md "wikilink")などでの、リッチな音使いが話題になった。
  - [シンセサウルス](https://ja.wikipedia.org/wiki/シンセサウルス "wikilink")

## 外部リンク

  - [MICRO COMPUTER CLUB 絵夢絶党](http://mzisland.com/club/mz-cmu/rst.html)
  - [BGMドライバ ・MGSDRV](http://gigamix.jp/mgsdrv/) - [Windowsでの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[エミュレーション](https://ja.wikipedia.org/wiki/エミュレーション "wikilink")演奏も可能。
  - [3MHz](http://cpu.dip.jp/3mhz/index.html) - MSX用音源ドライバSCMD
  - [MSX FMPAC SW-M004 取扱説明書 : 松下電器産業 : Free Download, Borrow, and Streaming : Internet Archive](https://archive.org/details/MSXFMPACUsersManual)

[Category:MSX](https://ja.wikipedia.org/wiki/Category:MSX "wikilink") [Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink") [Category:シンセサイザー](https://ja.wikipedia.org/wiki/Category:シンセサイザー "wikilink") [Category:コンピュータミュージック](https://ja.wikipedia.org/wiki/Category:コンピュータミュージック "wikilink") [Category:ヤマハの製品](https://ja.wikipedia.org/wiki/Category:ヤマハの製品 "wikilink")

1.  『FM音楽館』p.4
2.  取扱説明書 p.46
3.  取扱説明書 p.7
4.  取扱説明書 p.46
5.  『FM音楽館』 p5
6.  取扱説明書 p.9
7.  [富田のサイト、「TOMMYs'HomePage」](http://www.horae.dti.ne.jp/~stomita/music/albumn.html)
8.  「早すぎた迷オプション MSX-AUDIO」『MSX MAGAZINE 永久保存版 2』アスキー書籍編集部編著、アスキー、2003年、pp.148-151。
9.
10. [富田のサイト、「TOMMYs'HomePage」](http://www.horae.dti.ne.jp/~stomita/music/albumn.html)
11. 『MSX/MSX2/MSX2+ ゲーム・ミュージック・プログラム大全集』p.218 また『マイコンBASICマガジン』誌上では、89年1月号 p.208 に、投稿作品の6 - 7割がFM-PAC用だとの言及がある。
12. 『マイコンBASICマガジン』1990年5月号
13. 取扱説明書 pp.10-11
14. Marmsx『MSX article MAR MSX Gerência de Memória no MSX (II)』「4-SRAM」 および 徳間書店インターメディア 1988『ゲーム十字軍』 pp.136- など。なお同書ではMSXのBIOSの0014h「WRSLT」を用い、5ffehに4dhを、5fffhに69hを書き込んでいる。
15. 『FM音楽館』p141
16. 取扱説明書 p.36
17. 取扱説明書 p.40
18. 取扱説明書 pp.39, 45
19. 『MSX/MSX2/MSX2+ ゲーム・ミュージック・プログラム大全集』p.224
20. 取扱説明書 p.37
21. 取扱説明書 p.39
22. 取扱説明書 p.43
23. 『大全集II』 p.173
24. 1990年3月号p.191。または『MSX2/2+ ゲーム・ミュージックプログラム大全集』p.112
25. 『MSX2 テクニカルハンドブック』第5部「BIOS」 1986, アスキー
26. 『MSX/MSX2/MSX2+ ゲーム・ミュージック・プログラム大全集』
27.
28.