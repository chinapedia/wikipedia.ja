> この記事は[Peripheral Interchange Program](https://ja.wikipedia.org/wiki/Peripheral_Interchange_Program)から翻訳されています。


**Peripheral Interchange Program**（**PIP**）は、[DEC製コンピュータにおけるデータファイル転送ユーティリティ](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")。1960年代に [PDP-6](https://ja.wikipedia.org/wiki/PDP-6 "wikilink") 上で最初に実装された。その後、[PDP-10](https://ja.wikipedia.org/wiki/PDP-10 "wikilink") や [PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink") にも実装されている。

## 歴史

PIP は当初 ATLATL（"Anything Lord to Anything Lord" の略）と呼ばれていた。この名称はデバイスに依存しない[ファイルコピー](https://ja.wikipedia.org/wiki/ファイルコピー "wikilink")ツールであることを示している。

紆余曲折を経て、以下のような構文に落ち着いた。

    PIP destination=source

この語順は一般的な[英語](../Page/英語.md "wikilink")の語順とは逆である。そのため、[PDPマシン上の数あるユーティリティの](https://ja.wikipedia.org/wiki/PDPシリーズ "wikilink")1つとして、次のようなコマンド構文も生まれた。

    COPY source destination

しかし取って代わられたわけではなく、1980年代中ごろにも PIP は普通に使われていた。

## CP/M での PIP

[ゲイリー・キルドール](../Page/ゲイリー・キルドール.md "wikilink")は [CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink") で PIP とファイルのコンセプトを[RSTS/E](https://ja.wikipedia.org/wiki/RSTS/E "wikilink")などから流用した。[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")上のファイルにアクセスするだけでなく、CP/M の PIP は以下のような「スペシャルファイル」間でデータ転送が可能だった。

  - `CON:` — [コンソール](https://ja.wikipedia.org/wiki/コンソール "wikilink") （入出力）
  - `AUX:` — 補助デバイス。CP/M 1 および 2 では、AUX: ではなく PUN: （紙テープパンチ）と RDR: （紙テープリーダー）を用いていた。
  - `LST:` — リスト出力デバイス。通常は[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")
  - `PRN:` — LST: と同じ。ただし、行番号が付与され、タブ文字が拡張され、60行毎にフォームフィードが付与される。
  - `NUL:` — ヌルデバイス。入力としては [Peripheral_Interchange_Program//dev/zero](https://ja.wikipedia.org/wiki/Peripheral_Interchange_Program/dev/zero "wikilink")、出力としては [Peripheral_Interchange_Program//dev/null](https://ja.wikipedia.org/wiki/Peripheral_Interchange_Program/dev/null "wikilink") として機能する。
  - `EOF:` — [End Of File](https://ja.wikipedia.org/wiki/End_Of_File "wikilink") 文字（[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink") `0x1A`）を生成する入力デバイス
  - `INP:` — カスタム入力デバイス。デフォルトでは EOF: と同じ。
  - `OUT:` — カスタム出力デバイス。デフォルトでは NUL: と同じ。

これらはPIPでしか使えないため、真の[スペシャルファイル](https://ja.wikipedia.org/wiki/スペシャルファイル "wikilink")ではない。2つのカスタムデバイスは、PIPプログラムの先頭から固定の位置に呼び出しコードが実装されていた。これは、ユーザーや[OEM](../Page/OEM.md "wikilink")がその位置に[パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")を当てることで独自の入出力機器をサポート可能とすることを意図していた。プログラム内にはそのための246バイトの空き領域が用意されていた。

CP/M では `PIP destination=source` という構文だけでなく、`PIP destination_source` という構文もあった。これは、[端末](../Page/端末.md "wikilink")によっては '[_](https://ja.wikipedia.org/wiki/アンダースコア "wikilink")' を左向きの矢印で表示するものがあったためである。つまり、`PIP destination←source` のように表示された。これは文書には明記されておらず、CP/M ではファイル名に使える文字の種類が明確に定義されていなかった。このため、アンダースコアを使ったファイル名もエラーにはならず、そのようなファイルはPIPでうまく扱えない。

## 関連項目

  - [copy (コマンド)](https://ja.wikipedia.org/wiki/copy_\(コマンド\) "wikilink") - DECのマシンや DOS、OS/2、Windows でのファイルコピーコマンド
  - [cp (UNIX)](https://ja.wikipedia.org/wiki/cp_\(UNIX\) "wikilink")
  - [カーミット (プロトコル)](../Page/カーミット_\(プロトコル\).md "wikilink")

[Category:CP/M](https://ja.wikipedia.org/wiki/Category:CP/M "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink")