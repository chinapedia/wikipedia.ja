> この記事は[NOP](https://ja.wikipedia.org/wiki/NOP)から翻訳されています。


**NOP**（ノップ）あるいは **NOOP**（ノープ）とは no operation （何もしない）を意味する。プログラミングやネットワーク通信と言ったコンピュータ関連の技術用語として使用される。

## 機械語

[機械語](../Page/機械語.md "wikilink")において NOP は多くの[命令セット](../Page/命令セット.md "wikilink")で用意されている[命令である](../Page/命令_\(コンピュータ\).md "wikilink")。[プロセッサ](../Page/プロセッサ.md "wikilink")はこの命令を読みとると文字通り「何もせず」に[プログラムカウンタ](https://ja.wikipedia.org/wiki/プログラムカウンタ "wikilink")の[インクリメント](../Page/インクリメント.md "wikilink")のみを行う。それ自身では何の意味も持たない命令ではあるが、

  - 外部機器や他のプログラムとの同期のタイミングを取るための時間稼ぎ
  - [ジャンプ命令のジャンプ先の指標](../Page/分岐命令.md "wikilink")
  - 後で命令を追加する予定の場所にダミーとして置く
      - たとえば[遅延スロット](https://ja.wikipedia.org/wiki/遅延スロット "wikilink")にとりあえず置く、あるいは置ける命令がない時に置く
  - NOPスレッドによる命令ポインタの制御
  - [ワンチップマイコンの](../Page/マイクロコントローラ.md "wikilink")[PROM](../Page/PROM.md "wikilink")では、0x00か0xffのどちらか「上書き可能なほう」で潰すと NOP になるようにしておくと、再利用に便利

などの用途で使用される。

規則的に命令を決めた結果、何の意味も持たない命令（同一レジスタでの移動、次の番地へのジャンプ）が出来たのでそれをNOPとすることもあれば（[TMS9900](../Page/TMS9900.md "wikilink")など。また、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")の場合 `XCHG AX, AX` である。ただし内部的な「AXレジスタを操作する」という意味は近年の高性能化プロセッサではそのまま解釈すると並列化の邪魔になるので、AXの参照を伴わないよう特別に解釈される）、専用の命令（[オペコード](../Page/オペコード.md "wikilink")）を用意することもある。

1950年代の[EDSAC](../Page/EDSAC.md "wikilink")において既に NOP に相当する命令はあった（コード 'X' であるが、何もしないという命令は命令でないと考えたためか命令一覧では省かれていることがあり、[文字コード](../Page/文字コード.md "wikilink")一覧に命令も添えてある表のほうで確認できる（EDSACでは[文字コード](../Page/文字コード.md "wikilink")と[オペコード](../Page/オペコード.md "wikilink")を一致させていた））。

## 高水準言語

NOPという表現はしばしば、何も起こさないような関数やコードを指して使われることがある (この場合**冗長コード**と呼ばれることもある)。[コンパイラ最適化](../Page/コンパイラ最適化.md "wikilink")では、このようなコードを検出し、削除する（オブジェクトサイズの削減といった直接的な効果があり、コードキャッシュが無駄に使われるのを回避するという副次的効果もある）。

プログラミング言語の構文によっては、何もないことが許されないため、NOPのようなものが必要な場合がある。次に例を示す。

### Python

[Python](../Page/Python.md "wikilink")における、何の効果も持たない pass 文 (pass statement) は、NOPに似ている。pass statementは、Pythonの特徴的な[インデントを使用する構文の都合上](../Page/オフサイドルール.md "wikilink")、記述したいことが何もなくても、何か記述が必要な場合に使われる。たとえば[クラスの定義には何か](../Page/クラス_\(コンピュータ\).md "wikilink")[ブロック本体が必要であるので](../Page/ブロック_\(プログラミング\).md "wikilink")、とにかくクラスを存在させたいだけ、といった場合にその本体として `pass` と書く。 たとえば、次のようになる。

``` python
class Foo(Bar): # クラスを継承する
  pass          # (再)定義すべき内容は何もない
```

## 通信プロトコル

いくつかの[通信プロトコル](../Page/通信プロトコル.md "wikilink")では、NOP や NOOP というコマンドを備えている。このコマンドを送信した場合、具体的に何かが起こるわけではないが[サーバ](../Page/サーバ.md "wikilink")からの応答は返ってくる。プロトコルによっては特別なメッセージや情報を返すものもある。このコマンドは主にサーバとの接続が切断されていないか、あるいは[トラフィック](https://ja.wikipedia.org/wiki/トラフィック "wikilink")の増大等の理由でサーバからの応答が遅れていないかを調べる目的で使用される。

NOP もしくは NOOP コマンドを備えている主な通信プロトコルとして以下のものがある。

  - [FTP](../Page/File_Transfer_Protocol.md "wikilink") - NOOP コマンド
  - [SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink") - NOOP コマンド
  - [POP3](../Page/Post_Office_Protocol.md "wikilink") - NOOP コマンド
  - [TCP](../Page/Transmission_Control_Protocol.md "wikilink") - TCP オプションでオプション番号 1 が No-Operation（何もしない）を意味する
  - [Telnet](../Page/Telnet.md "wikilink") - NOP コマンド

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:機械語](https://ja.wikipedia.org/wiki/Category:機械語 "wikilink") [Category:無](https://ja.wikipedia.org/wiki/Category:無 "wikilink")