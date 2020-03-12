> この記事は[Hu-BASIC](https://ja.wikipedia.org/wiki/Hu-BASIC)から翻訳されています。


**Hu-BASIC**（ヒューベーシック）は、[シャープ](../Page/シャープ.md "wikilink")の[パソコン](https://ja.wikipedia.org/wiki/パソコン "wikilink")である[MZ-80K](https://ja.wikipedia.org/wiki/MZ-80K "wikilink")向けに開発された[BASIC](../Page/BASIC.md "wikilink")言語。開発元は[ハドソン](../Page/ハドソン.md "wikilink")。名称はハドソンの社名(**Hu**dson)に由来する。

MZシリーズが標準で採用したシャープ製の[S-BASIC](../Page/S-BASIC.md "wikilink")は、[PETに由来する命令セットであるため大勢を占めたマイクロソフト系のBASICからの移植性は低かった](../Page/PET_2001.md "wikilink")。対してHu-BASICはMS-BASICと同じ命令体系を持ち、それらからのソフトウェアの[移植が容易であった](../Page/移植_\(ソフトウェア\).md "wikilink")。[MZ-700](../Page/MZ-700.md "wikilink")ではS-BASICと共にHu-BASICも標準添付された（後継機種の[MZ-1500](../Page/MZ-1500.md "wikilink")では別売）。MZ-80K系の機種に対してのみ、バグを多く含んだものの、BASICコンパイラが開発・発売されている。

後にシャープAV事業部から発売された[X1シリーズにも移植されており](../Page/X1_\(コンピュータ\).md "wikilink")、X1ではS-BASICは無くHu-BASICが単独で標準添付された。

[ファミリーコンピュータ](https://ja.wikipedia.org/wiki/ファミリーコンピュータ "wikilink")用の[ファミリーベーシック](../Page/ファミリーベーシック.md "wikilink")に採用された「NS-Hu BASIC」も同一のブランドであり、一部同様の特徴を持ち合わせてはいるが、機能的にはかなり異なる。その他、[サムスン](https://ja.wikipedia.org/wiki/サムスン "wikilink")が[韓国で](../Page/大韓民国.md "wikilink")1982年に発売した[SPCシリーズ](https://ja.wikipedia.org/wiki/SPCシリーズ "wikilink")でも採用されている。

## 特徴

[thumb](https://ja.wikipedia.org/wiki/ファイル:Hu-BASIC_X1.png "wikilink")

  - シャープの[ポケットコンピュータ](../Page/ポケットコンピュータ.md "wikilink")や[富士通](../Page/富士通.md "wikilink")の[F-BASIC](../Page/F-BASIC.md "wikilink")などと同じく、命令文に省略形式が存在し、“LOCATE”は“LOC.”、“FOR”、“NEXT”はそれぞれ“F.”、“N.”と入力することでタイピングの手間を減らすことができた。
  - 同時期のMS-BASICに比べ内部構造が洗練されており、実行速度も高速であった。
  - [MZ-2000](https://ja.wikipedia.org/wiki/MZ-2000 "wikilink")/[2200用のVersion](https://ja.wikipedia.org/wiki/MZ-2000#MZ-2200 "wikilink") 2.0以降やX1用は[RAMディスク](../Page/RAMディスク.md "wikilink")に対応しており、RAMディスクを利用可能な環境であれば、テープ版であってもランダムアクセス処理を可能にしていた。
      - 他機種のフロッピーディスクに対応しないBASIC([ROM-BASIC](../Page/ROM-BASIC.md "wikilink"))では、カセットテープの[シーケンシャルアクセス](../Page/シーケンシャルアクセス.md "wikilink")しかサポートしないため、ほとんどはランダムアクセス用の命令自体が実装されていなかった。
  - ディスクのフォーマットは共通になっており、機種に依存せずファイルの読み書きが可能。そのためMZ用では、S-BASICとデータディスクの裏表の扱いが反転している。
      - 後にX1のHu-BASICを軸に開発された[S-OS"SWORD"でも](https://ja.wikipedia.org/wiki/Oh!X#THE_SENTINEL "wikilink")、このディスクフォーマットが用いられた。

元々単体製品だったゆえに多くの機能を盛り込んだことで、BASIC本体が大きくなったため、ユーザーが利用可能なフリーエリアは他の環境よりも狭くなっている。64[KiBの主記憶が実装されたX](https://ja.wikipedia.org/wiki/キビバイト "wikilink")1用であっても、フリーエリアは20KiB程度である。その後X1turboになる際、ファイル管理ルーチン、グラフィック描画ルーチン、[機械語モニタ](https://ja.wikipedia.org/wiki/機械語モニタ "wikilink")プログラム、日本語変換機能をシャドーROMに追い出しフリーエリアを増やしている（turbo BASIC）。X1F以降に標準添付されたV2.0では、NEW ON命令を使用することで、機能重複・低使用頻度の命令文やエラーメッセージなどを段階的に削除し、フリーエリアを増やせるようになっている（NEW BASIC）。

## バージョン

### MZ-700用

  - HU-BASIC VERSION 2.0A
    MZ-700シリーズ用として標準添付されたもの。

### MZ-1500用

  - HuBASIC Ver2.0
    標準添付されたMZ-700シリーズ用とは異なり別途販売されたもの。

### シャープX1用

  - CZ-8CB01 V1.0
    初代X1などデータレコーダ搭載モデルに標準添付。カセットテープ専用。
  - CZ-8RB01 V1.0
    CZ-8CB01 V1.0をROMに納め、X1用の拡張ボードとしたもの。ROMのままメモリ空間に配置されるのではなく、あくまでもRAMに転送してから起動するが、カセットテープからBASICをロードする時間を省くことができる。
  - CZ-8FB01 V1.0
    ディスクドライブ搭載機種に標準添付。CZ-8CB01 V1.0にフロッピーディスク関連の命令を追加したもの。フリーエリアが若干減少している。
  - CZ-8FB01 V2.0
    X1F/Gのディスクドライブ搭載モデル及びtwinに標準添付。NEW BASICとも呼ばれる。X1turbo開発時に得たノウハウをフィードバックし、グラフィック描画速度を大幅に向上させ、漢字も扱いやすくなった。反面、削除された命令もあり、広く利用されたV1.0に対する互換性が低下したため、利用があまり進まなかった。
  - CZ-8CB01 V2.0
    X1F/Gのデータレコーダ搭載モデルに標準添付。CZ-8FB01 V2.0と同等だがNEW ON命令で削除される命令セットがデータレコーダに合わせたものになっている点が異なる。
  - CZ-8FB02
    X1turboシリーズ（model10を除く）に標準添付。turbo BASICとも呼ばれる。400ライン表示などのX1turboのハードをサポートし、グラフィック描画速度も改善、全角文字を半角英数字と同等に扱えるようになった。CZ-8CB01/8RB01/8FB01 V1.0に対する上位互換性は良好だが、BIOS ROMをコールする[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")のため、全体的な速度はCZ-8CB01/8RB01/8FB01より遅い。
  - CZ-8CB02
    CZ-8FB02のテープ版。X1turbo model10に標準添付されたが、単体での販売はされていない。テープ版でありながら機能はフロッピーディスク版と同等であり、ハードウェアを増設すればそのままフロッピーディスクドライブ、拡張GRAM、シリアルマウスI/Fの操作も可能。
  - CZ-8FB03
    X1turboZII・ZIIIに標準添付。New Z-BASICとも呼ばれる。バンクメモリを使用してFM音源とX1turboZで追加されたアナロググラフィック機能をサポートしたもの。変数領域をバンクメモリに配置することでフリーエリアを広げることが出来るが、バンクメモリを切り替える[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")のため、CZ-8FB02/8CB02よりさらに遅くなった。X1turbo/Zまでのバンクメモリ非搭載機種では、単体販売されたNew Z-BASICに同梱されているバンクメモリボードを増設することにより対応する。

### ファミリーベーシック用（NS-Hu BASIC）

### サムスンSPC用

  - V1.0
    SPC-1000に付属。

### その他

  - mini Hu-BASIC/コンパイラー　
    コンパイラに特化した整数BASICのインタプリターとコンパイラのセット。Hu-BASICとは文法が大きく異なり、[Tiny BASICに近い](../Page/Tiny_BASIC.md "wikilink")。
    MZ-700用、X1用、PC-8001mkII用が存在する。カセットテープ専用。

## 関連項目

  - [Human68k](../Page/Human68k.md "wikilink") - X1の後継機[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")。シャープとハドソンが共同開発している。
  - [S-BASIC](../Page/S-BASIC.md "wikilink") - シャープが自社開発したMZシリーズ用のBASIC。
  - [dB-BASIC](https://ja.wikipedia.org/wiki/dB-BASIC "wikilink") - [デービーソフト](../Page/デービーソフト.md "wikilink")が開発したMZシリーズおよびX1シリーズ用のBASIC。

[Category:シャープ](https://ja.wikipedia.org/wiki/Category:シャープ "wikilink") [Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:ハドソン](https://ja.wikipedia.org/wiki/Category:ハドソン "wikilink")