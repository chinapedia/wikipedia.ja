> この記事は[BESYS](https://ja.wikipedia.org/wiki/BESYS)から翻訳されています。


**BESYS (Bell Operating System)**はコンピュータ黎明期の1957年に[IBM 704用の](../Page/IBM_704.md "wikilink")[バッチ処理](../Page/バッチ処理.md "wikilink")環境として[ベル研究所](../Page/ベル研究所.md "wikilink")が開発したオペレーティングシステム(OS)。

## 概要

704はCPUが高速であったのに対し、接続中の[作表機](../Page/作表機.md "wikilink")(パンチカードを読んだり集計したりする装置の総称)が遅くてボトルネックとなり、また人手による操作は原理的に早くならないのにマシンを占有されてしまうことから、この大幅なギャップを埋めるべくベル研究所が開発したシステム\[1\]。

システムの設計目標は次のようなものだった。

  - ハードウェアの有効活用、ノンストップオペレーション。
  - [作表機データのオフラインスプーリングによる効率的なバッチ処理とテープ間操作](https://ja.wikipedia.org/wiki/タビュレーティングマシン "wikilink")。
  - 制御カードの導入によりオペレーターの介入を必要最小限に抑える。
  - [入出力](../Page/入出力.md "wikilink")機能、システム制御機能、その他の[ライブラリ](../Page/ライブラリ.md "wikilink")をユーザープログラムに提供。
  - [デバッグ](../Page/デバッグ.md "wikilink")用の[コアダンプ](../Page/コアダンプ.md "wikilink")機能。
  - [IBM 650との互換性](../Page/IBM_650.md "wikilink")\[2\]。

BESYS-1の初期バージョンは1957年10月16日まで使用された\[3\]。[ビクター・ヴィソツキによる監修の下](https://ja.wikipedia.org/wiki/:en:Victor_A._Vyssotsky "wikilink")、[ジョージ・ミーリとグウェン](https://ja.wikipedia.org/wiki/:en:George_H._Mealy "wikilink")・ハンセンがワンダ・リー・マンメルと共に、IBMの[FORTRAN](../Page/FORTRAN.md "wikilink")や[ユナイテッド・エアクラフトの](https://ja.wikipedia.org/wiki/:en:ユナイテッド・エアクラフト "wikilink")[SAPを使って開発した](https://ja.wikipedia.org/wiki/:en:Symbolic_Assembly_Program "wikilink")。[パンチカード](../Page/パンチカード.md "wikilink")で入力された大量のジョブを効率よく処理し、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")やパンチカードでの出力に適した形で結果を生成するよう設計された。またこのシステムは[磁気テープ](../Page/磁気テープ.md "wikilink")や[磁気ディスクといった外部記憶装置にも対応していた](https://ja.wikipedia.org/wiki/磁気記録 "wikilink")。パンチカードやプリンタで出力したデータは、コンピュータには直接接続していない[電子作表機や](../Page/作表機.md "wikilink")[IBM 1401コンピュータでオフライン処理するのが一般的で](../Page/IBM_1401.md "wikilink")、後に周辺コンピュータを直結して処理するようになった。

ベル研究所で最初に実際に運用されたシステムはBESYS-2だった。システムは[磁気テープ](../Page/磁気テープ.md "wikilink")に保存され、メモリの下位64ワード(1ワード36ビット)と上位4Kワードに常駐した。上位4Kワードはモニタープログラムの常駐部本体が保持され、部分的に[磁気ドラムへスワップでき](../Page/磁気ドラムメモリ.md "wikilink")、ユーザープログラムが必要に応じて追加のメモリコアを利用できるようスペースを開けられるようになっていた\[4\]。

「BESYSは便利な入出力機能と統合的なディスク記憶装置のファイル管理ができる高度なソフトウェアパッケージだった\[5\]。」

## 社内用システム

BESYSは10年以上に渡りベル研究所の様々な部門で広く使用された。ユーザーグループの[SHAREを通じてベル研究所以外の外部組織へも無料](https://ja.wikipedia.org/wiki/:en:SHARE_\(computing\) "wikilink")・無サポートで提供された。

## BESYSのバージョン

BESYSは[IBM 709Xシリーズのアップグレードに応じてBESYS](https://ja.wikipedia.org/wiki/IBM_700/7000_series "wikilink")-3 (1960)、BESYS-4 (1962)、BESYS-5 (1963)、BESYS-7 (1964)、BE90 (1968)などのバージョンがあった\[6\]。ベル研究所の各ラボが[IBM System/360を導入したことでBESYSの開発は終了した](https://ja.wikipedia.org/wiki/System/360 "wikilink")。BESYS開発プロジェクトは全期間を通じてジョージ・ボールドウィンが責任者だった。

## 関連項目

  - [IBM](../Page/IBM.md "wikilink")
  - [IBMメインフレーム](../Page/IBMメインフレーム.md "wikilink")
  - [IBMメインフレーム用オペレーティングシステムの歴史](../Page/IBMメインフレーム用オペレーティングシステムの歴史.md "wikilink")
  - [メインフレーム](../Page/メインフレーム.md "wikilink")

## 脚注



[Category:ベル研究所](https://ja.wikipedia.org/wiki/Category:ベル研究所 "wikilink") [Category:1957年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1957年のソフトウェア "wikilink") [Category:IBMのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:IBMのオペレーティングシステム "wikilink") [Category:メインフレームのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:メインフレームのオペレーティングシステム "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink")

1.
2.
3.
4.
5.
6.