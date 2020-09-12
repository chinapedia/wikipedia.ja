> この記事は[PEEKとPOKE](https://ja.wikipedia.org/wiki/PEEKとPOKE)から翻訳されています。


[コンピューティング](../Page/コンピューティング.md "wikilink")において、**PEEK**（ピーク）と**POKE**（ポーク）は、いくつかの[高水準プログラミング言語で使用されるコマンドで](../Page/高水準言語.md "wikilink")、[メモリアドレス](../Page/メモリアドレス.md "wikilink")で参照される特定のメモリセルの内容にアクセスするために使用する\[1\]\[2\]。[BASIC](../Page/BASIC.md "wikilink")のものがよく知られているが、[Pascal](../Page/Pascal.md "wikilink")やなど他の[プログラミング言語](../Page/プログラミング言語.md "wikilink")にも同様のコマンドがある。このコマンドは、[C言語](../Page/C言語.md "wikilink")などにおける[ポインタに匹敵する役割を持っている](../Page/ポインタ_\(プログラミング\).md "wikilink")。

PEEKとPOKEは、初期の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")において様々な目的を果たすために考案され、特に、[メモリ空間にマッピングされた](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")[ハードウェアレジスタを変更するために使用された](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\)#ペリフェラルデバイスのレジスタ "wikilink")。また、プログラマはこのコマンドを使用して、ソフトウェアをコピーしたり、特定のソフトウェアのプログラミングの意図を回避したりすることもある（例えば、ゲームプログラムを操作してユーザが[チート](../Page/チート.md "wikilink")できるようにするなど）。今日では、BASICのような高水準言語を使用して、低水準でメモリを制御することはあまりなく、PEEK、POKEというコマンドの概念は一般的に時代遅れとみなされている。

英語においては、*peek*や*poke*という言葉が、プログラミングにおけるメモリアクセスを指す動詞（poked, peekedなど）として口語的に使われることがある。

## 文法

PEEK関数とPOKEコマンドは、通常、以下のように（BASIC[プロンプトで入力して即実行](../Page/コマンドプロンプト.md "wikilink")）か、間接モード（下記のソースのように[プログラムの中から実行](../Page/プログラム_\(コンピュータ\).md "wikilink")）で呼び出される。

``` qbasic
integer_variable = PEEK(address)

POKE address, value
```

引数の*address*と*value*は、評価される式がそれぞれ有効なメモリアドレスまたは値に対応する限り、複雑な[式を含んでいても良い](../Page/式_\(プログラミング\).md "wikilink")。ここで言う「有効なアドレス」とは、コンピュータの[アドレス空間](../Page/アドレス空間.md "wikilink")内のアドレスであり、「有効な値」とは、（一般的には）ゼロから最小アドレス可能なユニット（メモリセル）が保持することができる最大符号なし数までの符号なし値である。

## メモリセルとハードウェアレジスタ

POKEまたはPEEKされるアドレス位置は、通常のメモリセルや、対応するチップ（I/Oユニット、サウンドチップ、ビデオグラフィックスチップなど）の[メモリマップされた](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")[ハードウェアレジスタ](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\)#ペリフェラルデバイスのレジスタ "wikilink")、CPU自体のメモリマップされた[レジスタを参照することができる](../Page/レジスタ_\(コンピュータ\).md "wikilink")（これにより、強力な[機械語モニタ](https://ja.wikipedia.org/wiki/機械語モニタ "wikilink")や[デバッグ](../Page/デバッグ.md "wikilink")ツール、シミュレーションツールをソフトウェアで実装することが可能になる）。以下は、POKEによる対応チップ制御の一例として、[コモドール64](../Page/コモドール64.md "wikilink")の内蔵グラフィックスチップの特定のレジスタを操作して、画面の境界線を黒くするコマンドの例である。

``` qbasic
POKE 53280, 0
```

以下は、[Atari 8ビット・コンピュータで](../Page/Atari_8ビット・コンピュータ.md "wikilink")ディスプレイドライバに、全てのテキストを上下逆さまにするように指示するコマンドである。

``` qbasic
POKE 755, 4
```

ハードに紐付けられたメモリ位置は機種によって異なるため、様々な機種の「メモリマップ」は重要な文書である。定型的な例として、アタリのコンピュータの64キロバイトのメモリ全体をロケーションごとにマッピングした本『』が出版されている。

一般的に、ユーザプログラム、ユーザデータ、オペレーティングシステムのコードとデータ、メモリマップされたハードウェアユニットのために指定されたメモリアドレス領域は、機種によって異なる。このため、PEEK関数やPOKEコマンドは本質的に非[移植性であり](../Page/移植_\(ソフトウェア\).md "wikilink")、これらを使用したプログラムは、そのプログラムが書かれたシステム以外ではほぼ確実に動作しない。

## チートとしてのPOKE

多くの8ビットコンピュータ用ゲームにおいては、ゲームをメモリにロードし、起動する前に特定のメモリアドレスを変更して、無制限のライフ、無敵化、敵からの不可視化などの[チート](../Page/チート.md "wikilink")を行うことができた。このような変更は、POKEコマンドを使って行われた。[コモドール64](../Page/コモドール64.md "wikilink")、[ZX Spectrum](../Page/ZX_Spectrum.md "wikilink")、[Amstrad CPCでは](https://ja.wikipedia.org/wiki/Amstrad_CPC "wikilink")、関連するカートリッジやを持っているプレイヤーは、実行中のプログラムをフリーズさせてPOKEを入力し、チート状態で再開することもできた。

例えば、ZX Spectrum向けの『[ナイト・ロアー](https://ja.wikipedia.org/wiki/ナイト・ロアー "wikilink")』では、以下のコマンドで無敵化することができた。

``` qbasic
POKE 47196, 201
```

この場合、値201は[RET命令に相当するので](../Page/Return文.md "wikilink")、[衝突判定](https://ja.wikipedia.org/wiki/衝突判定 "wikilink")をトリガーする前に、ゲームがサブルーチンから早期に復帰する。

『』などの雑誌には、ゲームにおけるそのようなPOKEコマンドが掲載されていた。このようなコードは、一般的に、機械語コードを[リバースエンジニアリング](../Page/リバースエンジニアリング.md "wikilink")して、ライフ数、衝突の検出などに関連するメモリアドレスを識別することで発見されていた。

POKEによるチートの使用は、最近のゲームでは難しくなっている。最近のオペレーティングシステムは、外部プログラムからの非共有メモリへのアクセスができないようするために、[仮想記憶](../Page/仮想記憶.md "wikilink")化による[メモリ保護](../Page/メモリ保護.md "wikilink")を行っている（例えば、アプリケーションごとに[ページテーブル](../Page/ページテーブル.md "wikilink")を分けるなど）。

## 16ビットマシンのPEEKとPOKE

初期のBASICが動作するほとんどのコンピュータは8ビットプロセッサを使用していたため、1つのPEEKまたはPOKEの値は0から255の間のものだった。16ビットマシンにおいて16ビットの整数値を読み書きするには、`PEEK`や`POKE`を2回実施する必要がある。アドレスAの16ビット整数値を読み出すためには、とする必要があり、アドレスAに16ビット整数Vを書き込むためには、に続けてを実行する必要がある。

[IBM PCや](../Page/IBM_PC.md "wikilink")[Amiga](../Page/Amiga.md "wikilink")などの16・32ビットマシンでは、16ビット値を一度に読み書きできる`DPEEK`や`DPOKE`のようなコマンドが公式で用意されていた\[3\]。[Sinclair QLでは](https://ja.wikipedia.org/wiki/Sinclair_QL "wikilink")、16・32ビット値の読み書きができる`PEEK_W/PEEK_L`、`POKE_W/POKE_L`コマンドがあった。[Atari STシリーズでは](../Page/Atari_ST.md "wikilink")、コマンド名称は8ビットのコマンドと同様だが、読み書きするビット幅を指定することができた。また、いくつかの8ビットマシンには、16ビット幅のPEEKとPOKEを行うBASIC方言があった。例えば、東ドイツの"Kleincomputer" KC85/1（別名 Z9001）やKC87には、`DEEK`、`DOKE`コマンドがあった\[4\]。

## その他のBASICのPEEKとPOKE

1980年代初期のベンダーである[ノーススター・コンピューターズ](https://ja.wikipedia.org/wiki/ノーススター・コンピューターズ "wikilink")は、独自のBASIC方言・を持つオペレーティングシステム・NSDOSを使用していたが、法的問題の懸念から、コマンド名を`EXAM`と`FILL`に変更していた。他に、MEMWとMEMRを代わりに使用するBASIC方言もあった。

[BBC Microやその他の](../Page/BBC_Micro.md "wikilink")[エイコーン・コンピュータ](../Page/エイコーン・コンピュータ.md "wikilink")のマシンで使用されたでは、PEEKやPOKEというキーワードはなく、*query*と呼ばれる[疑問符](../Page/疑問符.md "wikilink")(?)を関数とコマンドの両方の操作に使用していた。以下にその例を示す（以下の例では、分かりやすさのためにREMの後のコメント内の説明を日本語で表記しているが、実際のBBC BASICでは日本語は使えない）。

``` bbcbasic
> DIM W% 4  : REM 4バイトのメモリを確保し、整数型変数 W% で指定する。
> ?W% = 42  : REM 定数 42 を格納する。これは'POKE W%, 42'と等価である。
> PRINT ?W% : REM W% が指すバイトを表示する。これは'PRINT PEEK(W%)'と等価である。
        42
```

32ビット値は、*pling*と呼ばれる[感嘆符](../Page/感嘆符.md "wikilink")(\!)を使用して、最下位バイトを最初にして（[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")）、PEEKやPOKEを実施することができる。さらに、アドレスの後にqueryかplingのいずれかを指定して、オフセット値を指定してアドレスをオフセットすることもできる。

``` bbcbasic
> !W% = &12345678   : REM アンパサント(&)は16進数であることを意味する。
> PRINT ~?W%, ~W%?3 : REM チルダ(~)は16進数として表示する。
        78        12
```

文字列は、ドル記号($)を使用して同様の方法でPEEKやPOKEを行うことができる。文字列の終端は、キャリッジリターン文字（ASCIIでは&0D）で示される。オフセットは、ドル記号では使用できない。

``` bbcbasic
> DIM S% 20          : REM 20バイトのメモリを確保し、 S% で指定する。
> $S% = "MINCE PIES" : REM 文字列'MINCE PIES'を格納する。文字列は &0D で終端されている。
> PRINT $(S% + 6)    : REM S% + 6バイトから始まる &0D で区切られた文字列を表示する。
PIES
```

## "POKE"という言葉の使用法

"POKE"という言葉は、特に1970年代後半から1980年代初頭にかけて8ビットコンピュータでプログラムを学んだ人々の間で、BASICを介したもの以外も含めて、「メモリの内容を直接操作すること」の意味で使用されることがある。

[Visual Basic](../Page/Visual_Basic.md "wikilink") for Windowsでは、[DDEを実現するのにLinkPokeキーワードを使用する](../Page/動的データ交換.md "wikilink")。

8ビットビデオゲームの[チート](../Page/チート.md "wikilink")はPOKEと呼ばれることもあった（上記の[チートとしてのPOKEを参照](https://ja.wikipedia.org/wiki/#チートとしてのPOKE "wikilink")）。

## 脚注

### 注釈

### 出典

## 関連項目

  -
  - [自己書き換えコード](../Page/自己書き換えコード.md "wikilink")

  - [ポインタ (プログラミング)](../Page/ポインタ_\(プログラミング\).md "wikilink")

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:記憶装置](https://ja.wikipedia.org/wiki/Category:記憶装置 "wikilink")

1.
2.
3.  Dave and Laura Yearke, ["Turbo BASIC Command Set"](http://www.umich.edu/~archive/atari/8bit/Unverified/Cislib_b/tbhlp.txt), Western New York Atari Users Group
4.