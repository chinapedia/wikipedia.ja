> この記事は[System i](https://ja.wikipedia.org/wiki/System_i)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:IBM_AS400.JPG "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:I5-570.jpg "wikilink")  **AS/400**（えーえすよんひゃく）、**iSeries**（あいしりーず）、**System i**（しすてむあい）は[IBM](../Page/IBM.md "wikilink")のビジネス・アプリケーション用サーバー。世界的には[ミッドレンジコンピュータ](../Page/ミッドレンジコンピュータ.md "wikilink")、日本では[オフィスコンピュータ](../Page/オフィスコンピュータ.md "wikilink")と分類される場合が多い。

  - 1988年 IBM AS/400 - 当記事で記載
  - 2000年 IBM eServer iSeries に改称 - 当記事で記載
  - 2006年 IBM System i に改称 - 当記事で記載
  - 2008年 IBM Power Systems に統合 - ハードウェアは[Power Systems](https://ja.wikipedia.org/wiki/Power_Systems "wikilink")、オペレーティングシステムは[IBM iを参照](../Page/IBM_i.md "wikilink")

## 名称

  - IBM AS/400 - 「AS」はApplication System の略、オペレーティングシステムは[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")（同時期の別製品名称は [PS/2](https://ja.wikipedia.org/wiki/PS/2 "wikilink")、[RS/6000](https://ja.wikipedia.org/wiki/RS/6000 "wikilink")、[ES/9000](https://ja.wikipedia.org/wiki/ES/9000 "wikilink")）
  - IBM eServer iSeries - 「i」は「Integration（統合）」を意味する（同時期の別製品名称は [xSeries](https://ja.wikipedia.org/wiki/xSeries "wikilink")、[pSeries](https://ja.wikipedia.org/wiki/pSeries "wikilink")、[zSeries](https://ja.wikipedia.org/wiki/zSeries "wikilink")）
  - IBM System i - 「i」は「Integration（統合）」を意味する（同時期の別製品名称は [System x](../Page/System_x.md "wikilink")、[System p](../Page/System_p.md "wikilink")、[System z](../Page/System_z.md "wikilink")）
  - IBM Power Systems (IBM i) - ハードウェアは[POWER](https://ja.wikipedia.org/wiki/POWER "wikilink")プロセッサ搭載、オペレーティングシステムの「i」は「Integration（統合）」を意味する（同時期の別製品名称は [IBM z](https://ja.wikipedia.org/wiki/IBM_Z "wikilink")）

## 歴史

  - [1988年](../Page/1988年.md "wikilink")、[System/38](https://ja.wikipedia.org/wiki/System/38 "wikilink")データベースマシンと[System/36](https://ja.wikipedia.org/wiki/System/36 "wikilink")を結合させ、最初のAS/400がリリースされる。オブジェクトベースシステムであり、[エドガー・F・コッド](../Page/エドガー・F・コッド.md "wikilink")の関係[データベースモデルに基づいて実装された](https://ja.wikipedia.org/wiki/関係データベース "wikilink")**[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")**関係データベースがシステムの中核部分に組み込まれている。登場したとき、2,500本以上のビジネスアプリケーションソフトウェアが用意されていた。このときの[CPU](../Page/CPU.md "wikilink")は独自の[CISC](../Page/CISC.md "wikilink")プロセッサであり、[System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink")に似た[命令セット](../Page/命令セット.md "wikilink")であった。後に[POWERプロセッサに移行した](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")。
  - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")、64ビットプロセッサ[RS64](../Page/RS64.md "wikilink")をサポートし、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") ([OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")) も64ビット化された。
  - [2000年](../Page/2000年.md "wikilink")、eSever iSeries と改称。
  - [2004年](../Page/2004年.md "wikilink")、[POWER5](https://ja.wikipedia.org/wiki/POWER5 "wikilink") プロセッサを使用した **System i5** サーバが登場。
  - [2006年](../Page/2006年.md "wikilink")、System i と改称。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")、後継のハードウェア [Power Systems](https://ja.wikipedia.org/wiki/Power_Systems "wikilink") が発表。ほぼ同時期にOSも [IBM i](../Page/IBM_i.md "wikilink") 名で新バージョンがリリース。
  - 2009年以降のOS新バージョンのリリースについては、[IBM i](../Page/IBM_i.md "wikilink") のページを、ハードウェアの発表については、 [Power Systems](https://ja.wikipedia.org/wiki/Power_Systems "wikilink") のページをそれぞれ参照のこと。

## 特長

  - [TIMI](https://ja.wikipedia.org/wiki/System/38#TIMI "wikilink")（Technology Independent Machine Interface） - System/38より継承した、テクノロジーに依存しないマシンインターフェイスと呼ばれる技術。主に[水平マイクロコードにより実装され](https://ja.wikipedia.org/wiki/マイクロコード "wikilink")、[プロセッサ](../Page/プロセッサ.md "wikilink")の[命令セット](../Page/命令セット.md "wikilink")などハードウェアの[実装](../Page/実装.md "wikilink")を変更しても[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) を含めた[ソフトウェア](../Page/ソフトウェア.md "wikilink")をそのまま動作させることができる。この仕組みは[仮想機械](../Page/仮想機械.md "wikilink")に似ているが、仮想機械を使用するシステムが基本的には[インタプリタ](../Page/インタプリタ.md "wikilink")形式であって、実行時に逐次プロセッサが理解できる[機械語](../Page/機械語.md "wikilink")に変換されるのに対して、TIMIでは[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")によって生成された実行ファイルの中にTIMIの中間言語で書かれた実行コードとコンパイル時点での実プロセッサに対応した機械語とを持っているという点で大きく異なっている。このため、実プロセッサが変わっても実行ファイルさえあれば変換（中間コードから機械語を再生成）することが可能で、[ソースファイル](https://ja.wikipedia.org/wiki/ソースファイル "wikilink")が無くてもハードウェアを自由に交換できるという優れた[可搬性](https://ja.wikipedia.org/wiki/可搬性 "wikilink")を、実行速度を犠牲にすることなく実現している。このためCPUをPOWERに変更した際の移行も順調に行われた。なおTIMIの[命令セット](../Page/命令セット.md "wikilink")のポインタは128ビットで、ハードウェアの進化に対応でき、既存のソフトウェアの修正は必要ない。
  - [単一レベル記憶](../Page/単一レベル記憶.md "wikilink") (SLS, single-level store) - メインメモリ等の[主記憶装置](../Page/主記憶装置.md "wikilink")と、ディスク装置等の[補助記憶装置](../Page/補助記憶装置.md "wikilink")を、単一の巨大な[アドレス空間](../Page/アドレス空間.md "wikilink")として管理する。このため「ソフトウェアを実行するためには、ディスク装置上のモジュールを、メインメモリにロードする」との処理が不要で、ボトルネック発生の少ない高速な[入出力](../Page/入出力.md "wikilink")が得られる。
  - 汎用の[コンピュータシステム](../Page/コンピュータシステム.md "wikilink")として初めて[アメリカ国家安全保障局](../Page/アメリカ国家安全保障局.md "wikilink")（NSA）から C2 レベルのセキュリティ認証を受けた。
  - 論理区画（[LPAR](../Page/LPAR.md "wikilink")）- [IBM](../Page/IBM.md "wikilink")の[メインフレーム](../Page/メインフレーム.md "wikilink")から導入され、ひとつのマシンを論理的に複数に分割して使用することができるようになった。各パーティションにはシステムリソース（[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")容量、CPU時間）を割り当てられ、それぞれにOSが動作する。動作可能な[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) は、[i5/OS](https://ja.wikipedia.org/wiki/i5/OS "wikilink") (IBM i) 、[Linux](../Page/Linux.md "wikilink")、[AIX](../Page/AIX.md "wikilink")など。

## 関連項目

  - IBM Systems
      - [System z](../Page/System_z.md "wikilink")
      - [System p](../Page/System_p.md "wikilink")
      - [System x](../Page/System_x.md "wikilink")

## 文献

  - [フランク・ソルティス](https://ja.wikipedia.org/wiki/フランク・ソルティス "wikilink") (著) 、[日本アイ・ビー・エム](../Page/日本アイ・ビー・エム.md "wikilink")(株) AS/400製品事業部 (翻訳/監修) 、『Inside the AS/400 : featuring the AS/400e series : 日本語版 第2版』、インフォ・クリエイツ、1998年、ISBN 4-900741-88-4

## 外部リンク

  - [IBM i - Japan](https://www.ibm.com/jp-ja/it-infrastructure/power/os/ibm-i)
  - [IBM Power Systems - Japan](https://www.ibm.com/jp-ja/it-infrastructure/power)
  - [IBM マーケットプレイス](https://www.ibm.com/jp-ja/products)
  - [IBM ソフトウェア](https://www.ibm.com/software/jp/)
  - [RPGPGM.COM](https://www.rpgpgm.com) 英語での多くのプログラミング例

[Category:IBMのミニコンピュータ](https://ja.wikipedia.org/wiki/Category:IBMのミニコンピュータ "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:サーバ_(ハードウェア)](https://ja.wikipedia.org/wiki/Category:サーバ_\(ハードウェア\) "wikilink")