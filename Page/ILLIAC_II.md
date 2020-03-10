> この記事は[ILLIAC II](https://ja.wikipedia.org/wiki/ILLIAC_II)から翻訳されています。


**ILLIAC II**（イリアック・ツー）は、[1962年](../Page/1962年.md "wikilink")に開発された[イリノイ大学の](https://ja.wikipedia.org/wiki/イリノイ大学アーバナ・シャンペーン校 "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")である。

## 概要

概念設計は1958年に提案されたもので、先進的な[エミッタ結合論理](../Page/エミッタ結合論理.md "wikilink") (ECL) 回路、[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")、[トランジスタ](../Page/トランジスタ.md "wikilink")によるメモリなどを採用し、[ILLIAC I](../Page/ILLIAC_I.md "wikilink") の100倍の性能を設計目標とした。

ILLIAC II は、8192ワードの[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")と65,536ワードの[磁気ドラムメモリ](https://ja.wikipedia.org/wiki/磁気ドラムメモリ "wikilink")を持つ。コアメモリのアクセス時間は1.8～2.0マイクロ秒であり、ドラムメモリのアクセス時間は7マイクロ秒であった。高速バッファも持っていて、一時的な結果を保持する短いループを形成していた（現在の[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")と同様のコンセプト）。高速バッファのアクセス時間は0.25マイクロ秒である。

ワードサイズは52ビットである。[浮動小数点数](../Page/浮動小数点数.md "wikilink")は、指数部 7ビット（4のべき乗）で、45ビットの仮数部という形式であった。[命令は](https://ja.wikipedia.org/wiki/命令セット "wikilink")26ビットのものと13ビットのものがあり、メモリ1ワードに4命令まで詰め込むことができた。

## 技術革新

  - ILLIAC II は世界初の[トランジスタ](../Page/トランジスタ.md "wikilink")製コンピュータのひとつである。[IBM 7030](https://ja.wikipedia.org/wiki/IBM_7030 "wikilink") コンピュータと同様、ILLIAC II はトランジスタが量産されることを見越して、まだ存在していないものを使う前提で設計された。
  - ILLIAC II プロジェクトは IBM 7030 に先行して競合する形で進行した。ILLIACの設計文書や関連文書はイリノイ大学として公開していたため、設計チームにはIBMが ILLIAC II のアイデアをいくつも借りたのではないかと見る向きもあった.\[1\]。
  - ILLIAC II は[SRT除算アルゴリズムの発明者の一人ジェームズ](https://ja.wikipedia.org/wiki/除算_\(デジタル\) "wikilink")・ロバートソンが設計した除算ユニットを備えていた。
  - ILLIAC II は [IBM 7030](https://ja.wikipedia.org/wiki/IBM_7030 "wikilink") と同様、最初のパイプライン方式を採用したコンピュータである。パイプラインの設計は[ドナルド・ギリース](https://ja.wikipedia.org/wiki/ドナルド・ギリース "wikilink")が行った。パイプラインの各ステージは、先行制御 (Advanced Control)、遅延制御 (Delayed Control)、相互作用 (Interplay) と名付けられた。
  - ILLIAC II には、Speed-Independent Circuitry という非同期回路を使った最初のコンピュータでもある。これは、デビッド・E・ミューラーの発明であり、Muller C-Element に基づいた非同期デジタル回路である。

## 発見

完成以前の評価中、[ドナルド・ギリース](https://ja.wikipedia.org/wiki/ドナルド・ギリース "wikilink")は ILLIAC II 向けに[メルセンヌ数](../Page/メルセンヌ数.md "wikilink")を探すプログラムを作った。実行してみると、新たな3つの素数が見つかった。この発見を記念して、イリノイ大学の郵便局の消印にはそのことが10年以上記され、ニューヨークタイムズ紙に取り上げられ、ギネスブックにも世界記録として掲載され、学術誌 Mathematics of Computation にも論文が掲載された。

## 退役後

完成の約10年後、ILLIAC II は分解された。そのころには数百のモジュールが単なる廃棄物になっていた。多くの学生が記念としてそれらを自宅に持ち帰っていった。ドナルド・ギリースも12個のモジュールを持ち帰っている。2006年、ギリースの遺族がそのうちの10個とフロントパネルをイリノイ大学に寄贈した。

また、ギリースの息子は ILLIAC II プロジェクトの膨大な関連文書（命令セット、設計報告、研究報告、進捗報告など全部で2000ページ）を保管していた。さらに詳細を知りたければ本人が連絡を受け付けている\[2\]。文書の大部分はイリノイ大学にもある。

## その他

[1960年](../Page/1960年.md "wikilink")9月に[相磯秀夫](../Page/相磯秀夫.md "wikilink")は演算制御装置の設計を担当した\[3\]。

## 脚注

## 関連項目

  - [ORDVAC](../Page/ORDVAC.md "wikilink")
  - [ILLIAC I](../Page/ILLIAC_I.md "wikilink")
  - [ILLIAC III](https://ja.wikipedia.org/wiki/ILLIAC_III "wikilink")
  - [ILLIAC IV](../Page/ILLIAC_IV.md "wikilink")

## 外部リンク

  - Gillies, Donald B. [Three New Mersenne Primes and a Statistical Theory](http://www.jstor.org/pss/2003409), Mathematics of Comput., Vol. 18:85 (Jan. 1964), pp. 93–97.
  - [ILLIAC II documentation](http://www.bitsavers.org/pdf/univOfIllinoisUrbana/illiac/ILLIAC_II) at bitsavers.org

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink") [Category:トランジスタ・コンピュータ](https://ja.wikipedia.org/wiki/Category:トランジスタ・コンピュータ "wikilink")

1.
2.  <http://www.ece.ubc.ca/~gillies>
3.  [日本のコンピュータパイオニア、相磯秀夫](http://museum.ipsj.or.jp/pioneer/aiso.html)、[情報処理学会](https://ja.wikipedia.org/wiki/情報処理学会 "wikilink")