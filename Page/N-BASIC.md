> この記事は[N-BASIC](https://ja.wikipedia.org/wiki/N-BASIC)から翻訳されています。


**N-BASIC**（エヌベーシック）は、NEC（[日本電気](../Page/日本電気.md "wikilink")）のパソコン[PC-8000シリーズ](../Page/PC-8000シリーズ.md "wikilink")・[PC-8800シリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")に搭載された、[スタンドアロンBASIC](../Page/スタンドアロンBASIC.md "wikilink")[インタプリタ](../Page/インタプリタ.md "wikilink")の一種。[Microsoft BASICを基にしている](../Page/Microsoft_BASIC.md "wikilink")。

[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")を扱えるように拡張されたものは、NECのマニュアル等ではDISK-BASICと呼んでいるが、[ROM-BASIC](../Page/ROM-BASIC.md "wikilink")に対する普通名詞としての[DISK-BASIC](https://ja.wikipedia.org/wiki/DISK-BASIC "wikilink")とまぎらわしいため、一般にはN-DISK-BASICなどと呼ばれる。

## 概要

[1979年](../Page/1979年.md "wikilink")に発売されたPC-8001に24KBのROMで搭載された。

[倍精度実数演算やカラーグラフィックなど](../Page/浮動小数点数.md "wikilink")、当時の[スタンドアロンBASIC](../Page/スタンドアロンBASIC.md "wikilink")としては最先端の機能を備え、完成度が高く、後の同種の環境の模範となった。ただし、後の[N<small>88</small>-BASICなどと比較すると](../Page/N88-BASIC.md "wikilink")、[ラベルが使えない](https://ja.wikipedia.org/wiki/ラベル_\(プログラミング\) "wikilink")、[変数名が先頭](../Page/変数_\(プログラミング\).md "wikilink")2文字しか識別されない、構造化制御文がないなど見劣りする点もある。

命令や関数の前後は、必ずしも[空白文字](https://ja.wikipedia.org/wiki/空白文字 "wikilink")で区切らなくてもよい。よって、

``` basic
FORTRAN=ATOK5
```

と記述すると、「変数『[FORTRAN](../Page/FORTRAN.md "wikilink")』に、変数『[ATOK](../Page/ATOK.md "wikilink")5』の値を代入する命令（LET文）」ではなく、「『TRAN』という変数を、変数『A』の値を初期値、変数『K5』の値を終値としてループを回す命令（[FOR文](https://ja.wikipedia.org/wiki/for文 "wikilink")）」として解釈された。

N-BASICのROMを[逆アセンブル](https://ja.wikipedia.org/wiki/逆アセンブル "wikilink")して注釈をつけた『PC-8001 BASIC SOURCE PROGRAM LISTINGS』という書籍が秀和システムトレーディング（現・[秀和システム](../Page/秀和システム.md "wikilink")）から出版され、[マイクロソフト](../Page/マイクロソフト.md "wikilink")との間で訴訟問題に発展するという事件もあった。

N-BASICで開発されたソフトウェア資産が膨大であったため、N-BASICはその後のPC-8000シリーズ・PC-8800シリーズにも搭載された。また、[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")にもオプションROMの形で提供されていた。

PC-8001mkII/SRに搭載されたN<small>80</small>-BASICは、N-BASICの24KBのROMをそのまま利用し、それに8KBの拡張ROMを増設する形で実装されている。

## 開発

N-BASICはマイクロソフトのDISK BASIC version 4.51をベースに、PC-8001用にグラフィック機能や通信機能を強化して開発された\[1\]。[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")と[西和彦](../Page/西和彦.md "wikilink")が主設計を担当し、マーク・ウィルソンがプログラムのコーディングを担当した\[2\]。

PC-8001の開発は1978年夏頃に始まった。開発を指揮していた渡辺和也は、[アスキーの西和彦の仲介でマイクロソフトのBASICとビル](../Page/アスキー_\(企業\).md "wikilink")・ゲイツの紹介を受けた。渡辺はマイクロソフトやアメリカの市場調査に向かおうと考えたが、当時のマイクロソフトは社員10名余りのベンチャー企業で、パソコン市場も創生期にあって公に認知されておらず、出張の言い訳が難しかった。そこで、1978年11月にロサンゼルスで開催された見本市『[ウェスト・コースト・コンピュータ・フェア](https://ja.wikipedia.org/wiki/ウェスト・コースト・コンピュータ・フェア "wikilink")』を見学するという理由を付けてアメリカに渡り、見本市の見学は1日で済ませて、マイクロソフトへの訪問や市場調査に向かった\[3\]。この出張で渡辺はアメリカで[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")の地位にあるマイクロソフトのBASICを採用すると決めた。NEC社内には既に土岐泰三がPC-8001用に開発していたBASICがあった。土岐のBASICは処理速度が優れていた。社内には大企業たるNECが小さな会社（マイクロソフト）からソフトウェアを買うことに抵抗感を示す者も少なくなかった。しかし、マイクロソフトのBASICは他社で使用されている実績があるためにバグの心配が少ない上、既にアメリカでデファクトスタンダードの地位を確立していたことから、渡辺は先を見据えてマイクロソフトのBASICを採用することにした\[4\]\[5\]。西はマイクロソフトの日本代理店として最初の大型顧客を獲得するため、マイクロソフトのBASICを非常に安い価格でNECに提供した\[6\]。土岐が開発して採用が見送られたBASICはPC-8801のN88-BASICを開発する際に活用された\[7\]。PC-8001の成功を見た他のメーカーもマイクロソフトと交渉し始め、渡辺によればBASICの価格は1年後には1桁上がっていたという\[8\]。

## バージョン

  - Ver. 1.0
    PC-8001に搭載された初期のバージョン。80桁モードでプログラムを編集すると80桁目が欠けるなどのバグがあった。
  - Ver. 1.1
    PC-8001に搭載された後期のバージョン。バグが修正されている。Ver.1.0のユーザーは「ニューバージョンROM」としてBit-INNで有償で入手して交換することが出来た。1981年4月以降のPC-8001に搭載。
  - Ver. 1.2
    PC-8801に搭載されたバージョン。PC-8801はPC-8001と比べてキーボードなど一部ハードウェアが異なるため、それに対応するための変更が加えられている。
  - Ver. 1.3
    PC-8001mkIIに搭載されたバージョン。TABキーに対応。
  - Ver. 1.4
    PC-8801mkIIに搭載されたバージョン。

その後も後継機種に搭載され続け、最大Ver.1.8まで上がっていたが、機能には変更はない。

## 命令・関数

### 特徴的な命令や関数

N-BASICの特徴的な命令・関数を示す。

  - `CONSOLE`文
    スクロール範囲、[ファンクションキー](../Page/ファンクションキー.md "wikilink")の表示、カラーモードを設定する。

  - `COLOR`文
    文字色あるいは属性、グラフィックモードを設定する。

  - `KEY`文
    ファンクションキーに文字列を登録する。

  - `LINE`文

:\#キャラクタを用いて線や長方形を描画する。

:\#簡易グラフィック機能(キャラクタ属性として2x8ドット/キャラクタ、80文字x25行なので、160x100ドット/画面)を用いて線や長方形を描画する。

:\#カラーモードにおいて行ごとの表示属性（ブリンク、リバースなど）を設定する。

  - `PSET`/`PRESET`文
    簡易グラフィック機能により点を打ったり消したりする。
  - `CSAVE`/`CLOAD`/`CLOAD?`命令
    [テープに対してプログラムをセーブ](../Page/データレコーダ.md "wikilink")・ロード・ベリファイする。
  - `CLEAR`文
    変数を消去し、文字列領域と[機械語](../Page/機械語.md "wikilink")領域を確保する。
  - `USR`関数
    機械語で書かれたプログラムを呼び出す。
  - `MON`命令
    [機械語モニタ](https://ja.wikipedia.org/wiki/機械語モニタ "wikilink")に入る。
  - `MOUNT`/`REMOVE`命令（DISK-BASICのみ）
    フロッピーディスクを挿入したときに`MOUNT`によりFATを読み込み、抜く前に`REMOVE`によりFATを書き出す。FATの読み書きをメモリ上でのみ行うようにしてアクセスの高速化を図ったものだが、`REMOVE`を忘れてフロッピーの内容を破壊するという事故がおきやすい。また、REMOBEなどとタイプミスをするとREM文と解釈されてしまい、内部では何も処理されず（エラー表示もされない）、やはり記録内容の破壊につながった。これら注意を要する扱いづらさのため、大変評判が悪かった。PC-9801用のN-BASIC(86)ではこの命令を使用しなくても自動でMOUNT/REMOVEされる(互換性の為のダミー命令としてMOUNT/REMOVE文は残されている)。またN<small>80</small>/N<small>88</small>-DISK BASICでは不要となり、命令自体の削除となっている。 ベースとなった[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")用[Microsoft BASICにも同じ命令があった](../Page/Microsoft_BASIC.md "wikilink")。

### 組み込まれなかった命令

N-BASICでは、以下に示す命令は組み込まれなかった。

  - 描画関連
      - `CIRCLE` - 円弧描画
      - `PAINT` - 塗りつぶし
      - `CLS` - 画面消去
  - 機械語関連
      - `BSAVE`/`BLOAD` - バイナリデータの読み込み・保存
      - `CALL` - 機械語プログラムの呼び出し
  - その他
      - `ON KEY GOSUB`, `ON STOP GOSUB` - キー操作による割り込み
      - `RANDOMIZE` - 一様乱数の初期化

描画関連のうち`CLS`（画面消去）は、消去を行う文字コードを表示させることでその機能を代替している（例 - **`PRINT CHR$(12)`**）。また、バイナリデータの読み込み・保存は、機械語モニタにより行い、機械語プログラムの呼び出しは、前述の`USR`関数により行う。`CIRCLE`命令は、三角関数と`PSET`命令で円を描くサンプルプログラムがマニュアルに記載されていた。乱数の初期化は`RND`関数の添え字に負数を与えることで行えた。

### 使用されていなかった予約語

また、N-BASICには以下のような未使用[予約語](../Page/予約語.md "wikilink")が存在し、将来的な機能拡張が想定されていた。実際には、N<small>80</small>-BASICや[GP-IB](https://ja.wikipedia.org/wiki/GP-IB "wikilink")などの特殊な拡張ROMで使用された。

  - `CMD`
  - `STATUS`
  - `IEEE`
  - `IRESET`
  - `ISET`
  - `LISTEN`
  - `MAT`
  - `POLL`
  - `RBYTE`
  - `SRQ`
  - `TALK`
  - `WBYTE`

## 脚注

[Category:日本電気の製品](https://ja.wikipedia.org/wiki/Category:日本電気の製品 "wikilink") [Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink")

1.
2.
3.
4.  加藤明、「[PC-8001の開発](https://doi.org/10.1587/bplus.2010.15_58)」 『電子情報通信学会 通信ソサイエティマガジン』 2010年 2010巻 15号 p.15_58-15_65, 、電子情報通信学会
5.
6.
7.
8.