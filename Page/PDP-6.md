> この記事は[PDP-6](https://ja.wikipedia.org/wiki/PDP-6)から翻訳されています。


[Dec_pdp-6.lg.jpg](https://ja.wikipedia.org/wiki/File:Dec_pdp-6.lg.jpg "fig:Dec_pdp-6.lg.jpg")と[アラン・コトック](../Page/アラン・コトック.md "wikilink")(1964)\]\] **PDP-6**は、[1963年](../Page/1963年.md "wikilink")に[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")(DEC)が開発した[PDPシリーズ](../Page/PDPシリーズ.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")の1モデル。後の[PDP-10](../Page/PDP-10.md "wikilink")を生み出す原型となったもので、両者の[命令セット](../Page/命令セット.md "wikilink")はほぼ同じである。

PDP-6はDEC初の大型機である。[IBM](../Page/IBM.md "wikilink")、[ハネウェル](../Page/ハネウェル.md "wikilink")、[ゼネラル・エレクトリック](../Page/ゼネラル・エレクトリック.md "wikilink")などの当時の大型汎用機で一般的な36[ビット](../Page/ビット.md "wikilink")[ワード](../Page/ワード.md "wikilink")を採用していた。アドレス指定は初期のDECのマシンと同一の18ビットで、[主記憶容量は最大](../Page/主記憶装置.md "wikilink")256[Kワードである](../Page/キロ.md "wikilink")。[メモリには](../Page/主記憶装置.md "wikilink")[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")が使用され、32,768ワードのメモリを搭載するのが一般的であった(8ビット[バイト換算すると](../Page/バイト_\(情報\).md "wikilink")160Kバイト)。

[命令セット](../Page/命令セット.md "wikilink")アーキテクチャは「one-and-a-half address」に分類される。[命令のオペランドには](../Page/命令_\(コンピュータ\).md "wikilink")1つの完全な18ビットアドレスと4ビットのアドレスがあり、後者はメモリの0番地から15番地までを指してそこを「[アキュムレータ](../Page/アキュムレータ_\(コンピュータ\).md "wikilink")」(AC)として使用する。また、さらに別の4ビットのフィールドで同じメモリ上のAC群のひとつをインデックス[レジスタとして指定できる](../Page/レジスタ_\(コンピュータ\).md "wikilink")(ただしAC0は指定できない)。

ほとんどのPDP-6システムはオプションの Type 162 高速メモリを装備しており、これは[トランジスタ](../Page/トランジスタ.md "wikilink")による[フリップフロップ](../Page/フリップフロップ.md "wikilink")で構成された16ワード分のメモリである。高速メモリ(高速アキュムレータ、あるいは高速ACとも呼ぶ)は磁気コアメモリの先頭16ワードを置き換え、4倍の高速さで操作可能である。

PDP-6では、2つの機能によって[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")をサポートしていた。1つはステータスビットによる動作モードの選択機能("Executive"と"User"で、後者の方が制限されている)、もう1つはリロケーション/プロテクションレジスタによってユーザー[アドレス空間](../Page/アドレス空間.md "wikilink")を[主記憶装置](../Page/主記憶装置.md "wikilink")の一部領域に制限する機能である(PDP-10ではもう1本のリロケーション/プロテクションレジスタで共有セグメントを追加可能とした)。主に使用された[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)は、後に[TOPS-10](../Page/TOPS-10.md "wikilink")となるOSの初期のバージョンで、ソースコードが付属していたためサイトによってはカスタマイズして使用していた。MITの[ITSオペレーティングシステムもPDP](../Page/Incompatible_Timesharing_System.md "wikilink")-6上で開発が始まったものである。

PDP-6は23台しか販売されず、あらゆるDECマシンの中でも最も少ない。複雑で高価であり、顧客のサイトでインストールして使用できるようにするのも大変だった。加えて販売部門としてもPDP-6を売りにくい事情があった。PDP-6が市場に出て間もなく、DECは小型機市場に専念するために36ビット市場からは撤退するとしていたのである。その後DECが新たな36ビット機を計画しているとの噂が広まり、後にそれが[PDP-10](../Page/PDP-10.md "wikilink")としてリリースされることとなった。

PDP-6の6205基板は、大型(11×8インチ)で1ビット分の回路(AR、MB、MQ)を構成している(従って36枚の6205が必要)。88個の[トランジスタ](../Page/トランジスタ.md "wikilink")を搭載し、18ピンのコネクタと22ピンのコネクタがそれぞれ両端にある。このような形状であるため保守作業が非常に難しかった。また、電源を切っただけで6205基板が故障するということが度々あったのである。この苦い経験から[PDP-10](../Page/PDP-10.md "wikilink")では小さい基板だけで構成するよう設計された（KA10、KI10)。大型の基板を再度使うようになったのはKL10以降となる。

DEC経営陣はPDP-6の販売先が大学などの技術的リーダーであったことから、このシステムに価値があると考えた。科学技術分野への進出の足場にもなり、最先端のユーザーから技術動向を知ることもでき、DECのマシンに親しんだ新たな従業員候補が育つといった利点があったのである。

[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")のPDP-6は、稼動状態で1984年12月にボストンコンピュータ博物館([コンピュータ歴史博物館](https://ja.wikipedia.org/wiki/コンピュータ歴史博物館 "wikilink")の前身)に寄贈された。その所蔵品の大部分はカリフォルニア州マウンテンビューのコンピュータ博物館に移送されたが、PDP-6は現在では残っていない。コンピュータ歴史博物館には Type 162 高速メモリが残されている。完全な形のPDP-6は現存しない。

## 参考文献

  - Bell, C. Gordon, Mudge, J. Craig, McNamara John E. "The PDP-10 Family". (1979). Part V of *Computer Engineering: A DEC View of Hardware Systems Design*. Digital Equipment Corp.

## 関連項目

  - [PDPシリーズ](../Page/PDPシリーズ.md "wikilink") - [PDP-1](../Page/PDP-1.md "wikilink"), **PDP-6**, [PDP-7](../Page/PDP-7.md "wikilink"), [PDP-8](../Page/PDP-8.md "wikilink"), [PDP-10](../Page/PDP-10.md "wikilink"), [PDP-11](../Page/PDP-11.md "wikilink"), [PDP-12](https://ja.wikipedia.org/wiki/PDP-12 "wikilink")

## 外部リンク

  - [DEC PDP-6 Serial numbers](http://www.ultimate.com/phil/pdp10/pdp6-serials)
  - [DEC's PDP-6 was the worlds first commercial time-sharing system](http://americanhistory.si.edu/collections/comphist/bell.htm) Gordon Bell interview at the Smithsonian
  - <http://www.inwap.com/pdp10/usenet/pdp6>

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:トランジスタ・コンピュータ](https://ja.wikipedia.org/wiki/Category:トランジスタ・コンピュータ "wikilink")