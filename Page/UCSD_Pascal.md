> この記事は[UCSD Pascal](https://ja.wikipedia.org/wiki/UCSD_Pascal)から翻訳されています。


**UCSD Pascal**（UCSD パスカル）は、1978年に[カリフォルニア大学サンディエゴ](https://ja.wikipedia.org/wiki/カリフォルニア大学サンディエゴ "wikilink")校(UCSD)のケネス・ボウルズが教育用に開発した[Pascal](../Page/Pascal.md "wikilink")処理系である。

[CPU](../Page/CPU.md "wikilink")の異なる[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")上で動作するために、[P-Machine](https://ja.wikipedia.org/wiki/P-Machine "wikilink")と呼ばれる[仮想マシンを使用する](https://ja.wikipedia.org/wiki/バーチャルマシン "wikilink")。[コンパイラ](../Page/コンパイラ.md "wikilink")は[プログラムをそれぞれのCPU用の](../Page/プログラム_\(コンピュータ\).md "wikilink")[機械語](../Page/機械語.md "wikilink")に翻訳するのではなく、P-Machineの機械語であるP-Codeに翻訳する。そのため、P-Codeの仮想マシンを実装すればどのようなパーソナルコンピュータ上でも実行可能であった。またUCSD PascalはPascalコンパイラだけでなく、[スクリーンエディタや](../Page/テキストエディタ.md "wikilink")[デバッガ](../Page/デバッガ.md "wikilink")、ファイル管理を含む[統合開発環境](../Page/統合開発環境.md "wikilink")として実装され、後に[p-Systemという](../Page/UCSD_p-System.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に発展した。これらの開発環境の殆どすべてはPascalで書かれていたので、容易に異なる環境向けに移植できた。通常、仮想マシンは[インタプリタ](../Page/インタプリタ.md "wikilink")として実装された（P-Codeインタプリタ）。また、特に処理速度が必要な場合のために、P-Codeから実際のCPUの機械語に変換するネイティブコードコンパイラが提供される場合もあった。

P-Machineは典型的な[スタックマシン](../Page/スタックマシン.md "wikilink")で、様々な処理を主に[スタック](../Page/スタック.md "wikilink")上で行う[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")を持っていた。後にP-Codeをハードウエアで直接実行するPASCALマイクロエンジンと呼ばれるCPUと、それを利用した[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")が製造された。このCPUは[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[LSI-11](https://ja.wikipedia.org/wiki/LSI-11 "wikilink")用マルチチップCPUセットを流用し、P-Codeを解釈する[マイクロコード](https://ja.wikipedia.org/wiki/マイクロコード "wikilink")を実装したもので、今日[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")製造で著名なWestern Digital社が開発した。

初期の[コンピュータロールプレイングゲーム](https://ja.wikipedia.org/wiki/コンピューターRPG "wikilink")"[Wizardry](../Page/ウィザードリィ.md "wikilink")"は[Apple II上のApple](../Page/Apple_II.md "wikilink") Pascal(UCSD Pascal)で書かれていた。

## UCSD Pascalが実装されたコンピュータの例

  - [Apple IIシリーズ](../Page/Apple_II.md "wikilink")
  - [タンディ・ラジオシャック](https://ja.wikipedia.org/wiki/タンディ・ラジオシャック "wikilink") [TRS-80](../Page/TRS-80.md "wikilink")シリーズ
  - [IBM PC](../Page/IBM_PC.md "wikilink"), [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")
  - Terak 8510/a（LSI-11ベース）
  - [PC-8000シリーズ](../Page/PC-8000シリーズ.md "wikilink")、[PC-8800シリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")、[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")

## 関連項目

  - [UCSD p-System](../Page/UCSD_p-System.md "wikilink")

[Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:Pascal](https://ja.wikipedia.org/wiki/Category:Pascal "wikilink") [Category:仮想機械](https://ja.wikipedia.org/wiki/Category:仮想機械 "wikilink") [Category:1978年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1978年のソフトウェア "wikilink")