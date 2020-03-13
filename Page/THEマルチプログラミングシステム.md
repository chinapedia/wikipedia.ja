> この記事は[THE](https://ja.wikipedia.org/wiki/THE)から翻訳されています。


**THEマルチプログラミングシステム**（*THE multiprogramming system*）は、[エドガー・ダイクストラ](../Page/エドガー・ダイクストラ.md "wikilink")らが開発した初期の[マルチタスク](../Page/マルチタスク.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS)。1965年から66年に論文に記され\[1\]、1968年に発表された\[2\]。ダイクストラはこのシステムを命名したことはない。"THE" とは "Technische Hogeschool Eindhoven" の略で、[オランダ語](../Page/オランダ語.md "wikilink")で[アイントホーフェン工科大学](https://ja.wikipedia.org/wiki/アイントホーフェン工科大学 "wikilink")を意味する。THEシステムは基本的に[マルチタスク](../Page/マルチタスク.md "wikilink")をサポートした[バッチ処理](../Page/バッチ処理.md "wikilink")システムである\[3\]。[マルチユーザー](https://ja.wikipedia.org/wiki/マルチユーザー "wikilink")OSとしては設計されていない。同時期の [Project GENIE](../Page/Project_GENIE.md "wikilink") で開発された [SDS 940](https://ja.wikipedia.org/wiki/SDS_940 "wikilink") に似ているが、THEシステムでのプロセス群は静的だった\[4\]。

THEシステムは初のソフトウェアベースの[メモリセグメンテーションを導入し](../Page/セグメント方式.md "wikilink")（[Electrologica X8](https://ja.wikipedia.org/wiki/:en:Electrologica_X8 "wikilink") はハードウェアでの[メモリ管理](../Page/メモリ管理.md "wikilink")をサポートしていなかった）\[5\]、プログラマは[磁気ドラムメモリ](../Page/磁気ドラムメモリ.md "wikilink")上の物理的位置を気にする必要がなくなった。そのために修正を加えた[ALGOL](../Page/ALGOL.md "wikilink")コンパイラ（ダイクストラのシステムでサポートされた唯一の[プログラミング言語](../Page/プログラミング言語.md "wikilink")）を使い、[システムルーチン呼び出しを自動生成し](../Page/サブルーチン.md "wikilink")、必要な情報が必要なときにスワップインされることを保証している\[6\]。

## 設計

THEマルチプログラミングシステムの設計は階層構造となっている点が重要で、上位層は下位層にのみ依存している。

  - Layer 0
    マルチプログラミングを実現する階層。CPUを割り当てるプロセスを決定し、[セマフォ](../Page/セマフォ.md "wikilink")上でブロックしているプロセス群の責任を持つ。割り込みを処理し、必要に応じて[コンテキストスイッチ](../Page/コンテキストスイッチ.md "wikilink")を行う。最も低いレベル。現代的に言えば[スケジューラである](../Page/スケジューリング.md "wikilink")。
  - Layer 1
    プロセスへのメモリ割り当て機構。現代的に言えばページャである。
  - Layer 2
    プロセス間通信機能。オペレーティングシステムとコンソールとの通信機能。
  - Layer 3
    全周辺機器の入出力管理。各種機器からの情報をバッファリングする機能も含まれる。
  - Layer 4
    ユーザープログラムを処理する階層。そこに5つのプロセスが存在し、ユーザープログラムの[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")・実行・プリントアウトを行う。完了すると制御はスケジュールキューに戻され、開始されたばかりのプロセスや[入出力](../Page/入出力.md "wikilink")でブロックされているプロセスを優先する。
  - Layer 5
    ユーザー層（ダイクストラは「我々は実装していない」と述べている）

上位層が下位層にのみ依存するという制約を課したのは、（準[形式手法](../Page/形式手法.md "wikilink")的に）システムの挙動を推測しやすくし、システムを段階的に構築できるようにするためである。システムは Layer 0 から順に実装され、それぞれの層が提供する抽象化を順に試験していった。この形式手法的設計プロセスは大いに成功し、ダイクストラは次のように述べている。

> 我々は、論理的[健全性](https://ja.wikipedia.org/wiki/健全性 "wikilink")が演繹的に証明できる方法で洗練されたマルチプログラミングシステムを設計可能であり、その実装が徹底的な評価に耐えることを見出した。評価中に見られた誤りは瑣末なコーディング上の誤りだけであり（500命令に1回の割合で発生した）、10分程度のマシンでの調査で個々の問題を検出でき、その対処も容易であった。\[7\]

このように[カーネル](../Page/カーネル.md "wikilink")を階層化するという方式は[Multics](../Page/Multics.md "wikilink")の[リングプロテクション](../Page/リングプロテクション.md "wikilink")モデルに似ている。その後のOSは何らかの階層化を導入していることが多く、例えば [Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") や [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") がそうだが、階層の数はTHEシステムより少ない。

動作プラットフォームはオランダの [Electrologica X8](https://ja.wikipedia.org/wiki/:en:Electrologica_X8 "wikilink") コンピュータで、システム自体は[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書かれている。このコンピュータは32キロワードの[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")（1[ワード](../Page/ワード.md "wikilink")は27ビット\[8\]）、[LRU方式の](https://ja.wikipedia.org/wiki/キャッシュアルゴリズム "wikilink")[バッキングストアを備えた](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")512Kワードの磁気ドラムメモリ、紙テープリーダー・パンチャー、プリンターを備えていた。

## 脚注

## 参考文献

  - E. W. Dijkstra . *EWD 126: 'The Multiprogramming System for the EL X8 THE* (manuscript). 1965年6月14日 テキスト [1](http://www.cs.utexas.edu/users/EWD/transcriptions/EWD01xx/EWD126.html) PDF [2](http://www.cs.utexas.edu/users/EWD/ewd01xx/EWD126.PDF)

## 関連項目

  - [リングプロテクション](../Page/リングプロテクション.md "wikilink")

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:エドガー・ダイクストラ](https://ja.wikipedia.org/wiki/Category:エドガー・ダイクストラ "wikilink") [Category:1968年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1968年のソフトウェア "wikilink")

1.   ([original](http://www.cs.utexas.edu/users/EWD/ewd01xx/EWD196.PDF); [transcription](http://www.cs.utexas.edu/users/EWD/transcriptions/EWD01xx/EWD196.html))
2.
3.
4.
5.
6.
7.
8.