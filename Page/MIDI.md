> この記事は[MIDI](https://ja.wikipedia.org/wiki/MIDI)から翻訳されています。


**MIDI**（ミディ、**M**usical **I**nstrument **D**igital **I**nterface）は、[電子楽器](../Page/電子楽器.md "wikilink")の演奏データを機器間で転送・共有するための共通規格である\[1\]。日本のMIDI規格協議会（JMSC、現在の社団法人[音楽電子事業協会](https://ja.wikipedia.org/wiki/音楽電子事業協会 "wikilink")）と国際団体の[MIDI Manufacturers Association](https://ja.wikipedia.org/wiki/MIDI_Manufacturers_Association "wikilink") (MMA) により策定され1981年に公開された。

## 概要

MIDIは音楽制作の現場で幅広く利用されている。MIDI規格に則って作成されたデータは、[DAWをはじめとした](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink")[シーケンサーなどで再生](../Page/ミュージックシーケンサー.md "wikilink")・編集することができる。

物理的な送受信回路・[インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink")、通信[プロトコル](../Page/プロトコル.md "wikilink")、[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")など複数の規定からなる。MIDI 1.0の策定完了から38年後の[2019年](../Page/2019年.md "wikilink")に、Ver.2.0となるMIDI 2.0の策定開始が発表された\[2\]。

MIDIデータは、音声データ（マイクなどで録音した音の波形を[サンプリングしたもの](https://ja.wikipedia.org/wiki/標本化 "wikilink")）ではなく演奏情報（発音せよ、音の高さは - 、音の大きさは - 、といった楽器や音源への[メッセージ](../Page/メッセージ_\(コンピュータ\).md "wikilink")）であり、データサイズが小さく、また音楽の細部を容易に変更することができる。

電子楽器以外では[劇場](../Page/劇場.md "wikilink")の[舞台照明](../Page/舞台照明.md "wikilink")のコントロールなどにも応用されている。また、MIDI規格と[パソコンの普及は](../Page/パーソナルコンピュータ.md "wikilink")、ホビーとしての音楽制作（[DTM](../Page/デスクトップミュージック.md "wikilink")）を一般化した。

当初、MIDI規格は、ハードウェアとソフトウェアの両分野にまたがり策定された。ハードウェアの規格は、[インタフェースや送受信回路](../Page/インタフェース_\(情報技術\).md "wikilink")・端子に関することであり、ソフトウェアの規格は、データフォーマット（機器同士が[リアルタイム](../Page/リアルタイム.md "wikilink")通信する際の規格であって、MIDIデータを保存流通させる[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")とは異なる）に関することである。

その後、MIDIの普及に伴いRP（Recommended Practice、推奨実施例）という拡張規格が策定された。音色配列などを厳密に定めた[GMシステムレベル1や](../Page/General_MIDI.md "wikilink")、MIDIデータを保存流通させるファイルフォーマット、劇場の舞台照明をコントロールする規格（[MIDIショーコントロール](https://ja.wikipedia.org/wiki/MIDIショーコントロール "wikilink")）が、このRPに含まれる。

MIDIはJIS（[日本産業規格](../Page/日本産業規格.md "wikilink")）によって以下のように[規格化](../Page/規格化.md "wikilink")されている。

1.  X 6054-1 電子楽器デジタルインタフェース（MIDI）- 第1部：総則
2.  X 6054-2 電子楽器デジタルインタフェース（MIDI）- 第2部：プロトコル仕様

## ハードウェア規格

[thumb](https://ja.wikipedia.org/wiki/ファイル:DIN-5_Diagram.svg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Midiaansl.jpg "wikilink")

### 送信

31.25Kbps (±1%) の非同期方式[シリアル転送を用いる](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")。

### 接続

MIDI機器（ハードウェア）は5ピンの[DINコネクタ](../Page/DINコネクタ.md "wikilink")で接続するのが一般的である。両端に位置する1番ピンと3番ピンは現在の仕様上では使用されず、中央2番ピンはケーブルの[シールド](../Page/シールド.md "wikilink")用に、4番、5番ピンがデジタル信号の伝送に使用される。MIDIケーブルの両端はどちらもオス端子で、シールドされた[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")として設計される。

コネクタには、MIDI信号を受け取るMIDI IN、MIDI信号を送信するMIDI OUT、受信したMIDI信号をそのまま送信するMIDI THRUの3種類がある。機器パネル側は常にメス端子となる。や障害の連鎖防止のため、MIDI機器同士には電気的[絶縁が規定されており](https://ja.wikipedia.org/wiki/絶縁_\(電気\) "wikilink")、受信側内部では[接地](../Page/接地.md "wikilink")線の2番ピンは接続されず、信号は[フォトカプラ](../Page/フォトカプラ.md "wikilink")で受信される基本仕様となっている。フォトカプラを経由するたびに信号波形の再現性が下がるため、MIDI THRUを多段直列すると通信エラーが発生することもある。並列に複数のMIDI機器を接続する場合や、信号系統を簡単に切り替えたい時はMIDI[パッチベイ](https://ja.wikipedia.org/wiki/パッチベイ "wikilink")を用いるが、これを使うことにより多段時の通信エラーも回避できる。

MIDIは[バスではない](../Page/バス_\(コンピュータ\).md "wikilink")。MIDI IN端子とMIDI OUT端子が別々で用意されていることから判るように、MIDIケーブル間のデータは一方向に送信される。

後述するアクティブセンシング機能で、接続状態が良好か、断線していないかを常に判定しており、アクティブセンシングが途絶えたとき、お互いのMIDI機器はケーブルが抜けたと判定するように作られている。

現代には、MIDI IN、MIDI OUTを使わず[RS-232](../Page/RS-232.md "wikilink")C、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[IEEE 1394などの規格を使った接続を行う機器も存在している](../Page/IEEE_1394.md "wikilink")。この場合、MIDIケーブルではなくこれらの規格のケーブル内をMIDI信号が通るため、転送に関して上記の通りではない。

### チャンネル

2本のMIDIケーブルを用い、お互いの機器のMIDI IN、MIDI OUTをそれぞれつないだ状態を1つの「システム」と捉える。このシステム毎に16の[チャンネル](https://ja.wikipedia.org/wiki/チャンネル "wikilink")が用意される。基本的にひとつのチャンネルにひとつの楽器（1パート）が割り当てられる。

これにより、1本のMIDIケーブルで16チャンネル分のデータを送信もしくは受信させることができる。例えば「1チャンネルのピアノと3チャンネルのギターを鳴らす」といったことである。16チャンネル分のデータは、後述する「チャンネルメッセージ」にて正確に分類され、相手機器の各チャンネルに届く。

それ以上のチャンネルを制御するためにはMIDIケーブルが複数本必要となり、MIDIデータのパート数（=チャンネル数）によっては、複数のMIDI音源を用意する必要もでてくる。

## データフォーマット

### MIDIメッセージ

MIDI規格上のデータの送受信は、すべて**MIDIメッセージ**で行われる。MIDIメッセージは、複数の[バイト](../Page/バイト_\(情報\).md "wikilink")（[8ビット](../Page/8ビット.md "wikilink")）で構成されている。「電子楽器の鍵盤を弾いたことで音が出る」という一連の流れもMIDIメッセージで制御されている。バイト単位で処理していくため、文言上では[16進数を用い](../Page/十六進法.md "wikilink")、数の後にHを付ける。

MIDIメッセージを効率よく送信するために、MIDIメッセージに使用されるバイトは「ステータスバイト」か「データバイト」の大きく2種類に分けられる。ステータスバイトとは[MSB](https://ja.wikipedia.org/wiki/最上位ビット "wikilink") (Most Significant Bit)が「1」、すなわち80H - FFHまでの128個のバイトを指し、データバイトとはMSBが「0」、すなわち00H - 7FHまでの128個のバイトを指す。

MIDIメッセージは複数のバイトで構成されていると前述したが、これらの先頭は常にステータスバイトで始まり、ステータスバイトの後に任意の個数のデータバイトが続く。ステータスバイトでは、ノートオンやコントロールチェンジ、システムエクスクルーシブなどを定義する。データバイトは、ステータスバイトで定義したものについて、その内容や数値を指定するのに使用する。

ステータスバイトが80H - FFHのうち何であるかによって、「チャンネルメッセージ」、「システムメッセージ」に分かれる。

#### チャンネルメッセージ

チャンネルメッセージとは、特にチャンネルを指定して送信するMIDIメッセージのことである。チャンネルメッセージのステータスバイトは80H - EFHである。ここからさらに「チャンネルボイスメッセージ」、「チャンネルモードメッセージ」と分類される。

##### チャンネルボイスメッセージ

[thumb](https://ja.wikipedia.org/wiki/ファイル:NoteNamesFrequenciesAndMidiNumbers_V3.svg "wikilink") チャンネルボイスメッセージとは、音を鳴らす、止める、[音色](../Page/音色.md "wikilink")を変える、[ピッチ](https://ja.wikipedia.org/wiki/ピッチ "wikilink")を変えるといった、音源の演奏に必要な情報に関する定義のことである。最大2つのデータバイトが続くことで、その内容・数値を決定する。

ステータスバイトの下位4ビットがMIDIチャンネル番号-1（0(0H)Hはチャンネル1、15（FH)はチャンネル16）を表している。

データバイトにて指定する**[ノートナンバー](https://ja.wikipedia.org/wiki/ノートナンバー "wikilink")**とは、最も低い音を0、最も高い音を127と割り当てた音の高さのことであり、半音刻みとなっている。[中央ハ](https://ja.wikipedia.org/wiki/中央ハ "wikilink")にはノートナンバー60が割り当てられ、88鍵盤の[ピアノ](../Page/ピアノ.md "wikilink")で出せる音域（A0 - C8の7オクターブと短3度）はノートナンバー21 - 108と割り当てられるので、MIDIでは[それよりさらに広い音域](https://ja.wikipedia.org/wiki/88鍵のピアノの音域外の音 "wikilink")（C-1 - G9の10オクターブと完全5度）をカバーできる。また、**ベロシティ**とは音の強さ(楽器で例えれば各弦や各鍵を弾く速さによって変化する音の強弱([強弱法](../Page/強弱法.md "wikilink")))のことである。1 - 127まであり[mp（メゾピアノ）が](../Page/強弱法.md "wikilink")64となり、127が最も強く、1が最も弱く、数値が0の場合は発音の終了（楽器で例えれば離鍵など）を表す。

なお、以下の説明では、これら0 - 127までの数字を、[16進数で表記する](../Page/十六進法.md "wikilink")。また、nはチャンネル番号を表わす。

  - 8nH ノートオフ
    音を止める命令。鍵盤楽器ではキーを離した時に送信される。ノートオフによって鳴っている音を止める。
    第1データバイト - ノートナンバーを指定
    第2データバイト - オフベロシティ値
  - 9nH ノートオン
    音を鳴らす命令。鍵盤楽器ではキーを押した時に送信される。この後ノートオフが送信されないままだと、音が鳴りっぱなしとなる。
    第1データバイト - ノートナンバーを指定
    第2データバイト - ベロシティ値
    なお「ノートオン・ベロシティ0」もノートオフと同じメッセージとみなされる。
  - AnH ポリフォニック キープレッシャー
    鍵盤楽器で、キーを押した状態でさらに押し込んだ際に、その圧力に応じて送信される。
    第1データバイト - ノートナンバーを指定
    第2データバイト - プレッシャー値
  - BnH [コントロールチェンジ](../Page/コントロールチェンジ.md "wikilink")
    音量、音質など様々な要素を制御するための命令。
    第1データバイト - コントロールナンバー（00H - 77H）を指定 - どのパラメータをコントロールするのか指定
    第2データバイト - コントロール値 - コントロール番号にて指定した要素の大小や強弱を設定
    ただし第1データバイトが78H - 7FH（120 - 127）の場合はコントロールチェンジではなく、チャンネルモードメッセージとなる。
  - CnH [プログラムチェンジ](https://ja.wikipedia.org/wiki/プログラムチェンジ "wikilink")
    音色を変える命令。00H - 7FHで、最大128種類から音色を選択できる。
    第1データバイト - プログラムナンバーを指定
    第2データバイトは使用しない。
  - DnH チャンネルプレッシャー
    鍵盤楽器で、キーを押した状態でさらに押し込んだ際に、その圧力に応じて送信される。ポリフォニック キープレッシャーと違い、そのチャンネルの全ノートナンバーに対して有効となる。
    第1データバイト - プレッシャー値
    第2データバイトは使用しない。
  - EnH [ピッチベンド](../Page/ピッチベンド.md "wikilink")
    鳴っている音の[ピッチ](https://ja.wikipedia.org/wiki/ピッチ "wikilink")を変える命令。MSB (Most Significant Byte) 128段階の1段階ずつをさらに[LSB](../Page/最下位ビット.md "wikilink") (Least Significant Byte) で128分割しているので、計16384段階の細かい指定ができる。[シーケンサー上では](../Page/ミュージックシーケンサー.md "wikilink")、-8192 - 0 - 8191といった数値で表示することが多い。
    第1データバイト - ピッチベンド値MSB
    第2データバイト - ピッチベンド値LSB

ステータスバイト部のnには0H - FHが代入され、これは1チャンネル - 16チャンネルを表す。「90H 3CH 40H」というMIDIメッセージがあったとすると、これは「ノートオン、1チャンネル。3CH=60なので[中央ハ](https://ja.wikipedia.org/wiki/中央ハ "wikilink")を鳴らす。40H=64なので[mpで鳴らす](../Page/強弱法.md "wikilink")」という命令である。

##### チャンネルモードメッセージ

チャンネルモードメッセージとは、ある楽器は和音が出せるのか、16チャンネルは区別するのかしないのか、といったことを設定するための定義のことである。BnHで始まるがコントロールチェンジには含まれず、BnHのあとに78H - 7FHが続くと、チャンネルモードメッセージのいずれかと判断される。多くの場合、第2データバイトには00Hが[ダミー](https://ja.wikipedia.org/wiki/ダミー "wikilink")として送信され、受信側も無視する。ステータスバイト部のnには0H - FHが代入され、これは1チャンネル - 16チャンネルを表す。

  - BnH 78H オールサウンドオフ
    該当するチャンネルの発音中の音を直ちに消音する。後述のオールノートオフより強制力が強い。
  - BnH 79H リセットオールコントローラ
    該当するチャンネルの全種類のコントロール値を初期化する。初期化されるコントロールや初期値は、受信するMIDI機器側に依存する。
  - BnH 7AH ローカルコントロール
    鍵盤と音源を兼ねそろえたシンセサイザーの、鍵盤部と音源部の内部的な接続に関する設定。第2データバイトを指定することでオンオフを行う。
    00H - ローカルオフ - 鍵盤と音源が接続されていない状態。鍵盤を弾くと、MIDI OUTからMIDIメッセージは送信されるが、音源は動かない。
    7FH - ローカルオン - 鍵盤と音源が接続されている状態。鍵盤を弾くと、音源から音が出る。
  - BnH 7BH オールノートオフ
    該当するチャンネルの発音中の音すべてに対してノートオフ命令を出す。ただし、音の余韻の長いものや、[サスティンペダルがオンの状態では音は止まらないので](https://ja.wikipedia.org/wiki/ピアノ#ペダル "wikilink")、オールサウンドオフを使用する。
  - BnH 7CH - 7FH MIDIモード設定
    7CH、7DH、7EH、7FHの4つのチャンネルモードメッセージを使いオムニモード、発音数のオンオフを組み合わせることで、4種のMIDIモードを設定できる。
    オムニモード - 7CH オムニオン、7DH オムニオフで設定。MIDIチャンネルを区別するかしないか。オフの場合、チャンネルに関係なく全ての情報を受信し処理、発音する。
    発音数 - 7EH モノモードオン、7FH ポリモードオンで設定。どちらかを設定すると片方のモードは自動的にオフになる。単音しか出せないのか、和音が出せるのかを設定する。
      - モード1 = 7DH オムニオン + 7FH ポリモード
        MIDIチャンネルを意識せず和音演奏ができるモード。
      - モード2 = 7DH オムニオン + 7EH モノモード
        MIDIチャンネルに関わらず、常に1音のみ鳴らすモード。
      - モード3 = 7CH オムニオフ + 7FH ポリモード
        一般的な送受信モード。MIDIチャンネルを区別し、各チャンネル毎に和音を用いた演奏が可能なモード。
      - モード4 = 7CH オムニオフ + 7EH モノモード
        チャンネルは区別するが、各チャンネル毎に1音しか出せないモード。たとえば6弦ある[ギターシンセサイザー](../Page/ギターシンセサイザー.md "wikilink")の各弦を各チャンネルに割り当てる場合に使用する。この場合、単音で発声するチャンネルは6つとなるので、第2データバイトでは06Hを送信する。

#### システムメッセージ

システムメッセージとは、チャンネルに関係なくMIDIシステム全体に対する命令を行うMIDIメッセージである。システムメッセージのステータスバイトはF0H - FFHである。機能ごとに「システムエクスクルーシブメッセージ」、「システムコモンメッセージ」、「システムリアルタイムメッセージ」の分類される。

##### システムエクスクルーシブメッセージ

[システムエクスクルーシブメッセージ](https://ja.wikipedia.org/wiki/システムエクスクルーシブメッセージ "wikilink")（Sys-Ex、またはSysExと略記し、シスイーエックスと読む場合もある）は、MIDI機器のより細かい設定を行ったり、音色データや[サンプリング](../Page/サンプリング.md "wikilink")データを送受信するなど、各メーカーのMIDI機器の固有のデータのやりとりに使用できるシステムメッセージである。ステータスバイトF0Hで始まる。

MIDIメッセージは大抵2バイト程度のデータバイトで成り立つが、SysExはMIDIメッセージ中、唯一データバイト長が指定されていない。可変長のため、最後にシステムコモンメッセージとして定義されているF7H エンドオブエクスクルーシブ (EOX) を送信することでSysExの終了を表現する。

##### システムコモンメッセージ

システムコモンメッセージは、主にシステムリアルタイムメッセージと併用され、MIDIシーケンサーなどの[同期](../Page/同期.md "wikilink")に使用される。ステータスバイト以下にデータバイトが続くものが多い。

  - F1H [MTCクォーターフレームメッセージ](https://ja.wikipedia.org/wiki/MIDIタイムコード "wikilink")
    [MIDIタイムコード](https://ja.wikipedia.org/wiki/MIDIタイムコード "wikilink") (MTC) の絶対時間情報を扱う。全2バイトで構成され、2バイト目で時刻、分、秒、フレームのカウントを処理する。
  - F2H ソングポジションポインタ
    同期時にマスター側で操作したロケータ位置をスレーブ側に送信する際に使用。[16分音符単位で指定できる](../Page/音符.md "wikilink")。第1データバイトでソングポジションポインタLSB、第2データバイトでソングポジションポインタMSBを扱う。
  - F3H ソングセレクト
    受信側のMIDI機器が複数のソング・シーケンスを扱える場合、第1データバイトでソングナンバーを選択する。
  - F4H 未定義
    F5H 未定義
    定義されず、使われていない。
  - F6H チューンリクエスト
    [アナログシンセサイザー](../Page/アナログシンセサイザー.md "wikilink")（デジタルのそれに比べ自身の発熱や周囲の温度変化、舞台上で浴びる照明などで経時により[調律](../Page/調律.md "wikilink")が狂いやすい）などで、[オシレータを再調律させるための命令](https://ja.wikipedia.org/wiki/電圧制御発振器 "wikilink")。現在はアナログシンセサイザーとともにほとんど使われない。
  - F7H エンドオブエクスクルーシブ (EOX)
    F0Hから始まるSysExの終了を示すステータスバイト。単独で機能し、データバイトを持たない。

##### システムリアルタイムメッセージ

システムリアルタイムメッセージは、MIDIシーケンサーなどの[同期](../Page/同期.md "wikilink")、**[MIDIタイミングクロック](https://ja.wikipedia.org/wiki/MIDIタイミングクロック "wikilink")**に使用される。ステータスバイト以下にデータバイトが続かず、単独の1バイトのみで機能する。[リアルタイム](../Page/リアルタイム.md "wikilink")に送信される必要があるため、最優先で送信される。

  - F8H タイミングクロック
    絶対時間を持たない[クロック](../Page/クロック.md "wikilink")情報。[4分音符ごとに](../Page/音符.md "wikilink")24カウントされる。
  - F9H 未定義
    定義されず、使われていない。
  - FAH スタート
    FBH コンティニュー
    FCH ストップ
    マスター側機器のコントロールパネルを操作したときに送信。それぞれスレーブ側機器の先頭から再生、停止中からの再生、停止を行う。
  - FDH 未定義
    定義されず、使われていない。
  - FEH アクティブセンシング
    突然のMIDIケーブルの断線や接触不良や出力側機器の故障などで、音が鳴りっぱなしになったりしないようにするための[フェイルセーフ](../Page/フェイルセーフ.md "wikilink")の仕組みである。MIDI機器間ではこのアクティブセンシングが常に送信されている。[ウォッチドッグタイマー](../Page/ウォッチドッグタイマー.md "wikilink")の一種である。受信側は、一度もアクティブセンシングを受けていない状態では通常通り動作するが、一度送信側からこれを受信すると、300ms（[ミリ秒](https://ja.wikipedia.org/wiki/ミリ秒 "wikilink")）以内に次のMIDIメッセージが送られてくることを期待するようになる。この状態で、アクティブセンシングや、その他MIDIメッセージを受信しなかった場合、断線したと判定する。
    ただし、実際は誤差やMIDI THRU処理の遅れを考慮し270ms - 330msの間で処理するよう余裕を持たせてある。このことから、送信側は270ms間隔でアクティブセンシングを送信し続ける。
  - FFH システムリセット
    これを受信した全てのMIDI機器はリセット（電源投入時の状態に戻）される。通常は使用しない。

### サンプルダンプ

[サンプルダンプとは](https://ja.wikipedia.org/wiki/システムエクスクルーシブ "wikilink")、システムエクスクルーシブメッセージを使用して[サンプラー](../Page/サンプラー.md "wikilink")とMIDI機器間で[サンプリング](../Page/サンプリング.md "wikilink")データを通信する規格である。サンプルダンプに関するフォーマットをサンプルダンプスタンダード (SDS) という。[MMAが](https://ja.wikipedia.org/wiki/MIDI_Manufacturers_Association "wikilink")1987年に提案した規格で、MMA-0003として定義されている。

ただし、前述の通りMIDIの通信速度は31.25Kbpsと、データ転送用途としては非常に遅い上、現代には[USBや](../Page/ユニバーサル・シリアル・バス.md "wikilink")[IEEE 1394などの高速](../Page/IEEE_1394.md "wikilink")[シリアルバスも普及しているため](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")、一部の学習・研究用途を除き使われることは無くなった。

## RP

RP (Recommended Practice) とは、MIDI規格策定後、利便性を高めるための**推奨実施例**として拡張された規格である。現在すでに複数の拡張規格が[AMEIと](https://ja.wikipedia.org/wiki/音楽電子事業協会 "wikilink")[MMAにより承認されており](https://ja.wikipedia.org/wiki/MIDI_Manufacturers_Association "wikilink")、いずれも共通規格としてMIDI規格に組み込まれている。

### スタンダードMIDIファイル

スタンダードMIDIファイル(SMF)とは、MIDI機器やMIDIメッセージを用いる演奏に関するデータの**保存形式**であり、メーカー毎のソフトやハードに関係なく使用できる共通の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。拡張子は.mid。いわゆる「MIDIデータ」は**演奏形式**である[前述した](https://ja.wikipedia.org/wiki/#MIDIデータフォーマット "wikilink")「MIDIデータフォーマット」の略称であるが、このスタンダードMIDIファイルを指すべく拡大使用される場合がある。

[Opcode](../Page/Opcode.md "wikilink")社により独自規格として提案されたが、[1991年](../Page/1991年.md "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink")に[AMEIと](https://ja.wikipedia.org/wiki/音楽電子事業協会 "wikilink")[MMAによりRPの第](https://ja.wikipedia.org/wiki/MIDI_Manufacturers_Association "wikilink")1号(RP-001)に追認された。

### GM

GMシステムレベル1、通称[GM](../Page/General_MIDI.md "wikilink") (General MIDI) とは、それまで各メーカー毎に異なっていた音色配列を統一することを目的として策定されたRPである。[1991年](../Page/1991年.md "wikilink")に、RP-003にて定義されている。音色配列の他、最低同時発音数や音色数、コントロールチェンジの効き具合といったことも指定されている。

さらに、従来のGMでは時代の進化に伴い補いきれなくなってきた部分を補完するため、GMシステムレベル2 (GM2) が上位規格として拡張された。GMとは完全な[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")性をもつ。

のちに、主に[携帯電話](../Page/携帯電話.md "wikilink")の[着信メロディ](../Page/着信メロディ.md "wikilink")の制作用途として、General MIDI Lite (GML) も上位規格として拡張された。

  - [1991年](../Page/1991年.md "wikilink") - GMシステムレベル1 - RP-003
  - [1999年](../Page/1999年.md "wikilink") - GMシステムレベル2 - RP-024
  - [2001年](../Page/2001年.md "wikilink") - General MIDI Lite - RP-033

### DLS

[DLS](https://ja.wikipedia.org/wiki/Downloadable_Sounds "wikilink") (Downloadable Sounds) は、SMFデータを[サウンドカード](../Page/サウンドカード.md "wikilink")などの音源機器に転送して再生するために策定されたRPである。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に、RP-016にて定義されている。再生する音源が異なると、作者の意図しない音色で再生されてしまうSMFとは異なり、DLS対応機器ならほとんど同じ音での再生を行なうことが可能となる。拡張子は.dls。

のちに、上位規格であるDLSレベル2.1や、携帯電話向けのMobile DLSが拡張された。

  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink") - DLSレベル1.0 - RP-016
  - [1999年](../Page/1999年.md "wikilink") - DLSレベル1.1 - RP-016
  - [2000年](../Page/2000年.md "wikilink") - DLSレベル2.0 - RP-025
  - 2000年 - DLSレベル2.1 - RP-025
  - [2003年](../Page/2003年.md "wikilink") - Mobile DLS - RP-041

### XMF

[XMF](https://ja.wikipedia.org/wiki/Extensible_Music_Format "wikilink") (eXtensible Music Format) は、[MMAによって提案された新しい音楽](https://ja.wikipedia.org/wiki/MIDI_Manufacturers_Association "wikilink")[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。SMFや、[音声ファイルであるWAVなどが一つのファイルとして格納できるようになっている](../Page/音声ファイルフォーマット.md "wikilink")。

複数回改稿されており、それぞれのバージョン毎にRPとして承認されている。

  - [2001年](../Page/2001年.md "wikilink") - XMFメタファイルフォーマット1.00 - RP-030
  - [2003年](../Page/2003年.md "wikilink") - XMFメタファイルフォーマット1.01 - RP-039
  - [2004年](../Page/2004年.md "wikilink") - XMFメタファイルフォーマット2.00 - RP-043

また、複数の用途に向けて、複数のタイプが定義、検討されている。

  - [2001年](../Page/2001年.md "wikilink") - XMFタイプ0 アンド XMFタイプ1ファイル - RP-031
  - [2004年](../Page/2004年.md "wikilink") - XMFタイプ2/Mobile XMFファイル - RP-042
  - [2007年](../Page/2007年.md "wikilink") - XMFタイプ3/Mobile オーディオクリップ for Mobile XMFファイル - RP-045
  - 20XX年 - XMFタイプ4/Interactive XMF (iXMF)

XMFに関する拡張規格も用意されている。

  - [2003年](../Page/2003年.md "wikilink") - UnPackerID for ZLIB - RP-040
  - [2006年](../Page/2006年.md "wikilink") - ID3 Meta-data Tags for XMF - RP-047

### MIDIショーコントロール

[MIDIショーコントロール](https://ja.wikipedia.org/wiki/MIDIショーコントロール "wikilink") (MIDI Show Control, MSC) とは、照明や映像機器など、[ショー](../Page/ショー.md "wikilink")の演出をコントロールする目的で策定されたRPである。[1991年](../Page/1991年.md "wikilink")にRP-002、のちにRP-014にて定義されている。

### MIDIタイムコード

[MIDIタイムコード](https://ja.wikipedia.org/wiki/MIDIタイムコード "wikilink") (MIDI Time Code, MTC) は、[同期](../Page/同期.md "wikilink")システムを組むことを目的として策定されたRPである。[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に、RP-004にて定義されている。

MIDI規格策定時に、同時に策定された[MIDIタイミングクロック](https://ja.wikipedia.org/wiki/MIDIタイミングクロック "wikilink")は絶対時間を持たなかったが、[SMPTE](../Page/SMPTE.md "wikilink")の普及につれMIDI上でも絶対時間を持った[クロック](../Page/クロック.md "wikilink")が必要となってきたことが、MTC策定の背景である。

MIDI策定団体である[MMAが中心に提案したため](https://ja.wikipedia.org/wiki/MIDI_Manufacturers_Association "wikilink")、RPのほかにMMA-0001としても定義されている。

### 記譜情報

記譜情報はMIDIデータ（MIDIメッセージの集合）を[楽譜](../Page/楽譜.md "wikilink")上に[音符](../Page/音符.md "wikilink")として表示するために策定されたRPである。RP-005、RP-006にて定義されている。

### ファイルダンプ

ファイルダンプとは、MIDIケーブルを使ってSMFデータを転送するために策定されたRPである。RP-009にて定義されている。

### MIDIマシンコントロール

[MIDIマシンコントロールとは](https://ja.wikipedia.org/wiki/システムエクスクルーシブメッセージ "wikilink")、システムエクスクルーシブメッセージを用いて[MTRや](https://ja.wikipedia.org/wiki/マルチトラックレコーダー "wikilink")[VTRを制御するために策定されたRPである](../Page/ビデオテープレコーダ.md "wikilink")。[1992年](../Page/1992年.md "wikilink")に、RP-013にて定義されている。

### SMF with Lyrics

SMF with Lyrics (SMF Language and Display extensions) とは、SMFのメタイベントとして用意されている歌詞格納機能を拡張したRPである。[1999年](../Page/1999年.md "wikilink")に、RP-026にて定義されている。

メタイベントと違い、表示を目的としており、曲タイトル、作曲者名、作詞者名、歌詞やふりがなを格納できる。カラオケの歌詞表示や楽譜上の歌詞表記などの用途を想定されている。また、日本語 ([Shift JIS](../Page/Shift_JIS.md "wikilink")) も使用できる。

### MIDI Media Adaptation Layer for IEEE-1394

MIDI Media Adaptation Layer for IEEE-1394は、MIDI[インタフェースなどのMIDI機器を](../Page/インタフェース_\(情報技術\).md "wikilink")[IEEE 1394を用いて接続することに関するRPである](../Page/IEEE_1394.md "wikilink")。[2000年](../Page/2000年.md "wikilink")に、RP-027にて定義されている。

### SP-MIDI

SP-MIDI (Scalable Polyphony MIDI) は、あらゆる音源で最適なデータを再生するために策定されたRPである。[2002年](../Page/2002年.md "wikilink")に、RP-034、RP-035にて定義されている。

例えば、通常だと24ボイス（パート数）を持つ音源用に作られたデータを16ボイスの音源で再生すると、8ボイス分は無視されてしまう。このままではデータ制作者の意図した再生ができないため、従来なら24ボイス用、16ボイス用と複数のデータを用意する必要が有った。このSP-MIDIの規格に従うと、ひとつのデータに前もって複数環境分の情報を収録できるので、少ない工数で、あらゆる音源で問題なく再生が出来るようになる。この技術は主に[携帯電話](../Page/携帯電話.md "wikilink")向けに使用される。

### MIDI XML

MIDI XML ("MIDI Names, Device Types, & Events in XML") は、SMFを[XMLで記述することを目的として策定されたRPである](../Page/Extensible_Markup_Language.md "wikilink")。[2003年](../Page/2003年.md "wikilink")に、RP-038にて定義されている。

## その他の規格

RPとして承認されていないが、各メーカーが独自に打ち出した規格も存在する。中には、比較的一般的となった規格も存在する。ただしメーカーに左右されるため、メーカーを越えた互換性は無い場合が多い。

なお、現在はこれ以上の音色配列などに関する規格の複雑化を防ぐため、[AMEI](https://ja.wikipedia.org/wiki/音楽電子事業協会 "wikilink")、[MMA共にGM](https://ja.wikipedia.org/wiki/MIDI_Manufacturers_Association "wikilink")2に一本化することを求めており、また、GS・XGはお互い規格をオープンにして相互にサポートすべきとしている\[3\]。しかし、実際にはローランド製、ヤマハ製の製品であってもGS・XG自体をサポートしない製品が増えてきたことも事実である。

同じ楽譜で演奏をしても、演奏者や楽器が異なると音が違って聴こえるように、使用する音源を変えれば出音は違ってくる。そのため、例えば[インターネット](../Page/インターネット.md "wikilink")上で配布されているMIDIデータをデータ制作者の意図した通りに演奏するためには、制作者が使ったものと同じ、音色設定を完全に一致させた音源が必要になる。たとえGS対応と謳っていてもGS対応音源なら何でもいいというわけではなく、どの音源モジュールを使うかによって音は異なる。

### GSフォーマット

[GSフォーマット](../Page/GSフォーマット.md "wikilink")は、[1991年](../Page/1991年.md "wikilink")に[ローランド](../Page/ローランド.md "wikilink")が提唱、策定した音色配列などに関する独自規格。RP-003であるGMを拡張して作られたと思われがちだが、こちらが先行している。GMは、GSから他社と共有できる部分を抜粋し標準化したものである。

GSに対応した音源には、SC-55やSC-88Proなどの[ローランド・SCシリーズ](../Page/ローランド・SCシリーズ.md "wikilink")が有名。

### XGフォーマット

[XGフォーマット](../Page/XGフォーマット.md "wikilink")は、[1994年](../Page/1994年.md "wikilink")に[ヤマハ](../Page/ヤマハ.md "wikilink")が提唱、策定した音色配列などに関する独自規格。ヤマハ製の[音源モジュール](../Page/音源モジュール.md "wikilink")や[シンセサイザー](../Page/シンセサイザー.md "wikilink")の互換性を持たせるためにGMを拡張する形で作られた。

XGに対応した音源には、MU80やMU500などの[ヤマハ・MUシリーズ](../Page/ヤマハ・MUシリーズ.md "wikilink")が有名。

## 用途と機器

本項ではMIDI規格が使われる用途と、MIDI規格を使用するハードウェア（機器）、ソフトウェアについて解説する。なお、箇条書きにしているハードウェアやソフトウェアは一例である。

### 音楽制作

総合的な音楽制作用途は、MIDIの代表的な使用例である。[パソコンと](../Page/パーソナルコンピュータ.md "wikilink")[ソフトウェア音源さえあれば](../Page/ソフトウェア・シンセサイザー.md "wikilink")、大がかりな設備投資をする必要無く[DTMを楽しめるといったことで](../Page/デスクトップミュージック.md "wikilink")、90年代から一般の趣味としても普及し出した。

現代は、オーディオ編集とMIDIデータ編集を同時に行える統合環境[DAWが業務向けを中心に普及している](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink")。

  - ハードウェア

:; 送信側

:\* [ミュージックシーケンサー](../Page/ミュージックシーケンサー.md "wikilink")（ハードシーケンサー）

:\* [MIDIコントローラー](https://ja.wikipedia.org/wiki/MIDIコントローラー "wikilink")

:\* [シンセサイザー](../Page/シンセサイザー.md "wikilink")（MIDI OUT端子が有るのならば、他のMIDI機器を制御可能）

:\* [ミュージックワークステーション](../Page/ミュージックワークステーション.md "wikilink")（同上）

:; 受信側

:\* [シンセサイザー](../Page/シンセサイザー.md "wikilink")

:\* [ミュージックワークステーション](../Page/ミュージックワークステーション.md "wikilink")

:\* [音源モジュール](../Page/音源モジュール.md "wikilink")

  - ソフトウェア

:; 送信側

:\* [ミュージックシーケンサー](../Page/ミュージックシーケンサー.md "wikilink")（ソフトシーケンサー）

:\* [デジタルオーディオワークステーション](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink") (DAW)

:; 受信側

:\* [ソフトウェア・シンセサイザー](../Page/ソフトウェア・シンセサイザー.md "wikilink")（ソフトウェア音源）

:\*\* [Microsoft GS Wavetable SW Synth](../Page/Microsoft_GS_Wavetable_SW_Synth.md "wikilink") - [Microsoft Windows 2000以降の](../Page/Microsoft_Windows_2000.md "wikilink")[Windowsに搭載されており最も普及しているソフトウェア音源](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")

:\*\* [QuickTime](../Page/QuickTime.md "wikilink")ミュージックシンセ - [Mac OSに標準で付属するソフトウェア音源](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")

かつては、ハードウェア音源の代わりに、[PCM音源](../Page/PCM音源.md "wikilink")等の音源データをソフトウェア向けに加工し、パソコン上の[サウンドボード](https://ja.wikipedia.org/wiki/サウンドボード "wikilink")でMIDIファイルの再生を可能にしたソフトウェアMIDI音源も開発された。しかしながら、同時発音数や音質がCPUの性能に依存するなど、ソフトウェアMIDI音源発売当初はリアルタイム演奏には不向きであった。

現在は、一般のパソコンが[ソフトウェア音源を処理するのに十分な性能を持ったことや](../Page/ソフトウェア・シンセサイザー.md "wikilink")、再生時に音源が不要な[MP3](../Page/MP3.md "wikilink")等の[圧縮](../Page/音声圧縮.md "wikilink")[音声ファイルフォーマット](../Page/音声ファイルフォーマット.md "wikilink")の普及により、一般ユーザーではDTM愛好家以外のハードウェアベースのMIDI音源の使用は著しく減少している。

### 録音・MA

[録音](../Page/録音.md "wikilink")や[MA](../Page/映像編集.md "wikilink") (Multi Audio) でもMIDIは使用される。演奏情報の送受信ではなく、システムメッセージを中心とした同期処理が行われている。

  - ハードウェア

:; 送信側

:\* [ミュージックシーケンサー](../Page/ミュージックシーケンサー.md "wikilink")（ハードシーケンサー）

:\* [ドラムマシン](../Page/ドラムマシン.md "wikilink")、リズムマシン

:\* [コントロールサーフェス](https://ja.wikipedia.org/wiki/コントロールサーフェス "wikilink")

:; 受信側

:\* [マルチトラックレコーダー](https://ja.wikipedia.org/wiki/マルチトラックレコーダー "wikilink") (MTR)

:\* [ビデオテープレコーダ](../Page/ビデオテープレコーダ.md "wikilink")ー (VTR)

  - ソフトウェア

:; 送信側

:\* [ミュージックシーケンサー](../Page/ミュージックシーケンサー.md "wikilink")（ソフトシーケンサー）

:\* [デジタルオーディオワークステーション](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink") (DAW)

:; 受信側

:\* [ミュージックシーケンサー](../Page/ミュージックシーケンサー.md "wikilink")（ソフトシーケンサー）

:\* [デジタルオーディオワークステーション](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink") (DAW)

  -

      -
        （別々のコンピュータ上のソフトウェアに関する同期）

### カラオケ

カラオケ機器は、MIDIデータを再生する機能が備わっている。各カラオケ店舗では、[インターネット](../Page/インターネット.md "wikilink")回線を通じて最新曲のMIDIデータを受信する仕組みになっており、[通信カラオケ](../Page/通信カラオケ.md "wikilink")と呼ばれるのはこのためである。[ブロードバンドインターネット接続](https://ja.wikipedia.org/wiki/ブロードバンドインターネット接続 "wikilink")が普及する以前は、現在のように大量の音声データをインターネットで送受信するのは困難であったが、MIDIデータであれば、当時の低速な回線でも十分に送受信可能であった。

なお、カラオケ用MIDIデータはカラオケデータ制作専門の[プログラマ](../Page/プログラマ.md "wikilink")などが、[ソフトシーケンサーなどを用いて制作し](../Page/ミュージックシーケンサー.md "wikilink")、通信カラオケ配信会社に卸す仕組みとなっている。

### モバイル機器・着信メロディ

スマートフォンの登場以前、携帯電話の[着信メロディ](../Page/着信メロディ.md "wikilink")においてMIDI規格が利用されていた。携帯電話内のデータを、携帯電話内に搭載された音源が処理し音を鳴らしている。携帯電話向けのRPも複数拡張された。

### 舞台照明・演出

[1991年](../Page/1991年.md "wikilink")にRP-002として[MIDIショーコントロール](https://ja.wikipedia.org/wiki/MIDIショーコントロール "wikilink")が定義された。これにより、MIDIで舞台装置、照明、演出効果などが制御できるようになった。

  - ハードウェア

:; 送信側

:\* [ホスト](https://ja.wikipedia.org/wiki/ホスト "wikilink")コントローラー

:; 受信側

:\* 各舞台用機材（照明など）

### その他

[鉄道](../Page/鉄道.md "wikilink")の[プラットホーム](../Page/プラットホーム.md "wikilink")で流れる[発車メロディ](../Page/発車メロディ.md "wikilink")や、[学校](https://ja.wikipedia.org/wiki/学校 "wikilink")・[会社](../Page/会社.md "wikilink")で流れる[チャイム](../Page/チャイム.md "wikilink")を再生する[タイマー](../Page/タイマー.md "wikilink")などでもMIDI規格が応用されることがある。

## MIDI検定

MIDIの基礎知識や、業務レベルの細かい知識などを問う[MIDI検定](../Page/MIDI検定.md "wikilink")が[1999年](../Page/1999年.md "wikilink")より実施された。現在4,3,2,1級の4階級が用意されており、2級には2級筆記試験と2級実技試験の2段階が用意されている。

3,2級検定試験は年1回の実施、MIDI4級検定試験は各公認講師・指定校による随時開催となっている。

MIDI検定開始から11年間、1級試験は実施されず2級実技試験が最高級とされていたが、2010年1月15日より、1級試験が新設された。

## 年表

  - [1981年](../Page/1981年.md "wikilink") - [日本楽器製造（現・ヤマハ）](../Page/ヤマハ.md "wikilink")、[ローランド](../Page/ローランド.md "wikilink")、[コルグ](https://ja.wikipedia.org/wiki/コルグ "wikilink")、[河合楽器（カワイ）](../Page/河合楽器製作所.md "wikilink")、[シーケンシャル・サーキット](../Page/シーケンシャル・サーキット.md "wikilink")、[オーバーハイム](../Page/オーバーハイム.md "wikilink")の国内外楽器メーカー6社が『MIDI 1.0 Specification』をまとめる。
  - [1982年](../Page/1982年.md "wikilink")10月 - ローランドを中心に規格化が進められ、米国音楽雑誌「KEYBOARD」誌上で Ver.1.0 が公開される。
  - [1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")1月 - [NAMMショーにて](https://ja.wikipedia.org/wiki/楽器ショー#NAMM_ショー "wikilink")[シーケンシャル・サーキット](../Page/シーケンシャル・サーキット.md "wikilink")製Prophet600と[ローランド](../Page/ローランド.md "wikilink")製JX-3Pとの接続デモが行われる。
  - 1983年8月 - 日本語版 MIDI 1.0 規格を発表。
  - [1984年](../Page/1984年.md "wikilink") - MIDI Manufacturers Association (MMA) が発足。
  - [1989年](../Page/1989年.md "wikilink")1月 - MIDI 1.0（Ver.4.1日本語版）発表。
  - [1991年](../Page/1991年.md "wikilink") - [スタンダードMIDIファイル](../Page/スタンダードMIDIファイル.md "wikilink")(RP-001) がMIDI規格の「推奨実施例」(Recommended Practice) として承認。
  - [1991年](../Page/1991年.md "wikilink")9月 - [GMシステムレベル1](../Page/General_MIDI.md "wikilink")(RP-003) がMMA,JMSCによって策定。
  - [1991年](../Page/1991年.md "wikilink") - [ローランド](../Page/ローランド.md "wikilink")初の[GSフォーマット](../Page/GSフォーマット.md "wikilink")対応音源、[SC-55が発売](../Page/ローランド・SCシリーズ.md "wikilink")。
  - [1994年](../Page/1994年.md "wikilink") - [ヤマハ](../Page/ヤマハ.md "wikilink")初の[XGフォーマット](../Page/XGフォーマット.md "wikilink")対応音源、[MU80が発売](../Page/ヤマハ・MUシリーズ.md "wikilink")。
  - [1996年](../Page/1996年.md "wikilink")5月 - 社団法人[音楽電子事業協会](https://ja.wikipedia.org/wiki/音楽電子事業協会 "wikilink") (AMEI) が発足。
  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink") - [Downloadable Sounds](https://ja.wikipedia.org/wiki/Downloadable_Sounds "wikilink") (RP-016) を策定。
  - [1999年](../Page/1999年.md "wikilink")[1月17日](https://ja.wikipedia.org/wiki/1月17日 "wikilink") - 第1回3級MIDI検定試験を実施。
  - 1999年[1月20日](../Page/1月20日.md "wikilink") - MIDIがJIS規格として策定される。
  - 1999年7月 - GMシステムレベル2 (RP-024) を策定。
  - [2001年](../Page/2001年.md "wikilink") - [Extensible Music Format](https://ja.wikipedia.org/wiki/Extensible_Music_Format "wikilink") (RP-030) を策定。
  - [2001年](../Page/2001年.md "wikilink")5月 - 携帯電話着信メロディ用の規格[General MIDI Lite](../Page/General_MIDI.md "wikilink") (RP-033) を策定。
  - [2003年](../Page/2003年.md "wikilink")[7月3日](../Page/7月3日.md "wikilink") - 社団法人音楽電子事業協会がMIDI規格誕生20周年記念事業を開催。
  - [2013年](../Page/2013年.md "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink") - ローランド社（浜松市）の創業者である[梯郁太郎](../Page/梯郁太郎.md "wikilink")がMIDI規格の制定に対する貢献によりテクニカル・グラミー・アワードを受賞\[4\]。
  - 2016年7月 - MIDI 1.0規格書、RP、CAが無償公開される\[5\]。
  - [2019年](../Page/2019年.md "wikilink")1月18日 - MIDI 1.0の策定完了から38年目となる[2019年](../Page/2019年.md "wikilink")に、次世代となるMIDI 2.0の策定開始を発表した\[6\]。

## 脚注

## 参考文献

  -
## 関連項目

  - [音楽電子事業協会](https://ja.wikipedia.org/wiki/音楽電子事業協会 "wikilink")
  - [MIDI Manufacturers Association](https://ja.wikipedia.org/wiki/MIDI_Manufacturers_Association "wikilink")
  - [MIDI検定](../Page/MIDI検定.md "wikilink")
  - [OpenSound Control](../Page/OpenSound_Control.md "wikilink")
  - [Virtual Studio Technology](https://ja.wikipedia.org/wiki/Virtual_Studio_Technology "wikilink")
  - [梯郁太郎](../Page/梯郁太郎.md "wikilink") - 規格策定の貢献者

## 外部リンク

  - [社団法人音楽電子事業協会](http://www.amei.or.jp/)
      - [MIDI1.0規格書](http://amei.or.jp/midistandardcommittee/MIDIspcj.html)
      - [RP/CA](http://amei.or.jp/midistandardcommittee/RP&CAj.html)
  - [MIDI Manufacturers Association](https://www.midi.org/)

[Category:MIDI](https://ja.wikipedia.org/wiki/Category:MIDI "wikilink") [Category:JIS](https://ja.wikipedia.org/wiki/Category:JIS "wikilink") [Category:日本の発明](https://ja.wikipedia.org/wiki/Category:日本の発明 "wikilink")

1.
2.
3.  [ローランドとヤマハがMIDI規格の互換性向上で協力](http://www.watch.impress.co.jp/pc/docs/article/20010116/midi.htm)
4.
5.
6.