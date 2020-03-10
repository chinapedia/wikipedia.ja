> この記事は[TX-0](https://ja.wikipedia.org/wiki/TX-0)から翻訳されています。


**TX-0**(***T**ransistorized E**X**perimental computer **zero***)は、初期の完全[トランジスタ式コンピュータ](https://ja.wikipedia.org/wiki/トランジスタ式コンピュータ "wikilink")のひとつ。当時としては大規模な64K×18ビットワードの[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")を備えていた。[1956年](../Page/1956年.md "wikilink")に稼動を開始し、1960年代まで使われた。**tixo**とも呼ばれる。

[MIT](../Page/マサチューセッツ工科大学.md "wikilink")[リンカーン研究所](https://ja.wikipedia.org/wiki/リンカーン研究所 "wikilink")で主として、[トランジスタ](../Page/トランジスタ.md "wikilink")化設計と大規模磁気コアメモリシステムの実験のために設計されたもので、TX-0の基本設計はリンカーン研究所が以前に設計した有名な[Whirlwind](../Page/Whirlwind.md "wikilink")をトランジスタ化したものである。Whirlwindが大きな建物のフロア全体を占めるような大きさであったのに対して、TX-0はそれなりの部屋に収まり、しかも高速だった。Whirlwindと同様TX-0にもディスプレイシステムが装備されていた。12インチの[オシロスコープ](https://ja.wikipedia.org/wiki/オシロスコープ "wikilink")を装備していて、7インチ×7インチの範囲に512×512ピクセルの表示ができた。

TX-0は実用を目的としていたわけではない。メモリは64Kワードあったが、それを使いこなすには16ビットの[アドレス空間](../Page/アドレス空間.md "wikilink")が必要である。しかし、コスト削減のため、命令語長は18ビットに切り詰められていた。これでは、命令コードに2ビットしか使えず、[命令は](https://ja.wikipedia.org/wiki/命令セット "wikilink")4種類しかないことになる。TX-0には基本命令としてストアと加算と分岐しかなかった。しかし、4番目の命令 "operate" は命令語の続きを命令コードとして解釈するもので、これによって便利な命令をいくつも使うことができた。加算には10μ秒かかった。

TX-0の成功により、より大規模で複雑な **TX-1** が直ちに計画された。しかし、その複雑さゆえ計画はすぐに頓挫し、規模を縮小して再設計され、[1958年](../Page/1958年.md "wikilink")に**TX-2**が完成した。磁気コアメモリは当時非常に高価だったので、TX-0のメモリの一部はTX-2に転用された。研究対象としての TX-0 が不要になると、1958年7月にMIT電子工学研究所(RLE)にほぼ無期限で貸し出され、後に[MIT人工知能研究所](../Page/MIT人工知能研究所.md "wikilink")に受け継がれた。

リンカーン研究所から引き渡されたときにはわずか4Kワードのコアメモリしかなかったが、命令の形式は上述の通り64Kワードにアクセス可能であった。そこで約1年半後には命令コードを4ビットに増やし、インデックスレジスタも追加された。これによってプログラミングが格段に楽になり、後にはメモリを8Kまで拡張した。この新たに生まれ変わったTX-0は[音声認識](../Page/音声認識.md "wikilink")や[手書き文字認識](../Page/手書き文字認識.md "wikilink")などの様々な情報工学関連の研究開発に使われた。[テキストエディタ](../Page/テキストエディタ.md "wikilink")や[デバッガ](../Page/デバッガ.md "wikilink")などのツール類も開発された。

## TX-2

[TX-2_mod_top.jpg](https://ja.wikipedia.org/wiki/File:TX-2_mod_top.jpg "fig:TX-2_mod_top.jpg") **TX-2**はTX-0の後継として[1958年](../Page/1958年.md "wikilink")に完成し、[人工知能](../Page/人工知能.md "wikilink")や[ヒューマンマシンインターフェース](https://ja.wikipedia.org/wiki/ヒューマンマシンインターフェース "wikilink")の研究に使われた。[トランジスタ](../Page/トランジスタ.md "wikilink")ベースで64K×36ビットワードの[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")を搭載。[アイバン・サザランド](../Page/アイバン・サザランド.md "wikilink")の[スケッチパッドプログラムはTX](https://ja.wikipedia.org/wiki/Sketchpad "wikilink")-2上で動作した。

その後TX-2プロジェクトも障害に直面し、チームメンバーの何人かはプロジェクトを離れ会社を設立することになった。TX-2の設計の基本となっているモジュールを「研究モジュール」として一時期販売した後、[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")(DEC)はTX-0を簡素化した製品を開発し、1961年に[PDP-1](../Page/PDP-1.md "wikilink")として発売した。最初のPDP-1はTX-0の隣の部屋に設置され、一時期並んで動作していた。

## 外部リンク

  - [Tixo.Org](http://tixo.org)
  - [RLE Technical Report 627 TX-0 Computer History (Oct 1974) PDF](https://dspace.mit.edu/bitstream/1721.1/4132/1/RLE-TR-627-42827671.pdf)
  - [The TX-0: Its Past and Present](http://ed-thelen.org/comp-hist/TheCompMusRep/TCMR-V08.html)
  - [TX-0 documentation at bitsavers.org](http://www.bitsavers.org/pdf/mit/tx-0)
  - [TX-2 documentation at bitsavers.org](http://www.bitsavers.org/pdf/mit/tx-2)

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink") [Category:トランジスタ・コンピュータ](https://ja.wikipedia.org/wiki/Category:トランジスタ・コンピュータ "wikilink")