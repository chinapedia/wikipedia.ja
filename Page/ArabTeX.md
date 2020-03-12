> この記事は[ArabTeX](https://ja.wikipedia.org/wiki/ArabTeX)から翻訳されています。


**Arab** (ArabTeX) は[アラビア文字](../Page/アラビア文字.md "wikilink")および[ヘブライ文字](https://ja.wikipedia.org/wiki/ヘブライ文字 "wikilink")を利用するための [](../Page/TeX.md "wikilink") および [](../Page/LaTeX.md "wikilink") の[フリーのパッケージ](../Page/フリーソフトウェア.md "wikilink")。[シュトゥットガルト大学](https://ja.wikipedia.org/wiki/シュトゥットガルト大学 "wikilink")のクラウス・ラガリー教授が作成した。[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")記法のみで構成されるコードを入力してコンパイルするだけで、[リガチャ](https://ja.wikipedia.org/wiki/リガチャ "wikilink")（連字）や[母音記号](https://ja.wikipedia.org/wiki/母音記号 "wikilink")、ラテン文字転写を含めほぼ完全なアラビア文字、ヘブライ文字による[組版](../Page/組版.md "wikilink")が可能。アラビア文字を用いる言語では、[アラビア語](../Page/アラビア語.md "wikilink")（[マグリビーを含む](https://ja.wikipedia.org/wiki/マグリブ方言 "wikilink")）、[ペルシア語](https://ja.wikipedia.org/wiki/ペルシア語 "wikilink")、[ウルドゥー語](../Page/ウルドゥー語.md "wikilink")、[パシュトー語](../Page/パシュトー語.md "wikilink")、[スィンディー](https://ja.wikipedia.org/wiki/シンディー語 "wikilink")、[カシュミーリー](../Page/カシミール語.md "wikilink")、[ウイグル語](../Page/ウイグル語.md "wikilink")、[マレー語](../Page/マレー語.md "wikilink")（[ジャウィーによる](../Page/ジャウィ文字.md "wikilink")）が[ナスフ体で](../Page/イスラームの書法.md "wikilink")、ヘブル文字を用いるものでは[ヘブル語](https://ja.wikipedia.org/wiki/ヘブル語 "wikilink")、[イディッシュ語](../Page/イディッシュ語.md "wikilink")、[ヘブル＝アラビア語](https://ja.wikipedia.org/wiki/ヘブル＝アラビア語 "wikilink")がそれぞれサポートされる。

## ArabTeXの出力例

[ArabTeXでの出力例。「礼拝は眠りに勝る」](https://ja.wikipedia.org/wiki/ファイル:Arabtex_Salat.png "wikilink")

`\fullvocalize`
`\transtrue`
`\settrans{english}`
`\<'al-.s.salATu _hayruN mina al-nnawmi>`

## 特色

  - ごく一般的な  環境で動作可能であり、`\<`～`>`あるいは`\begin{arabtext}～\end{arabtext}`が Arab環境となる。[](https://ja.wikipedia.org/wiki/pTeX "wikilink") でもほとんどそのまま動作可能。
  - Arab はアラビア文字を構成する点や線をバラバラに分解したフォントを持っており、これを組み合わせることによって一つの文字を形成する。このため固定的なグリフを持つワードプロセッサによる印刷物より美しい出力を得ることができる。母音記号も適切な場所に配置され、有／最小限の配置／無の切り替えができる。
  - 文法的に煩雑な[ワスラ](https://ja.wikipedia.org/wiki/ワスラ "wikilink")や[マッダ](https://ja.wikipedia.org/wiki/マッダ "wikilink")、[ター・マルブータ](https://ja.wikipedia.org/wiki/ター・マルブータ "wikilink")、[ハムザ](https://ja.wikipedia.org/wiki/ハムザ "wikilink")などの処理も自動的に行われる。また古典的なハムザや短剣アリフなども処理できる。ペルシア語でも[エザーフェ](https://ja.wikipedia.org/wiki/エザーフェ "wikilink")の処理が自動的に行われる。
  - 転写機能を持つ。一つの Arab のソースコードでアラビア文字と同時にラテン文字への転写を生成することができる。アラビア文字のラテン転写は通常簡単に入力できないものもある（z の下に点など）が、これを効率的に入力することができる。また転写も言語コードの設定によって適切に反映され（[オスマン語](../Page/オスマン語.md "wikilink")転写も可能）、さらに`\settrans{hoge}` などの命令で転写方式も容易に変更することができる。
  - [ユニコード(Unicode)](../Page/Unicode.md "wikilink") などさまざまな既存のエンコードによるデータもそのまま入力してコンパイルすることができる。

## 外部リンク

  - [ArabTeX](http://baobab.informatik.uni-stuttgart.de/ifi/bs/research/arab_e.html) 公式サイト
  - [TeX & ArabTeX](http://www.osaka-gaidai.ac.jp/~mes/multi/multi_02.html)大阪外国語大学高階美行教授
  - [ArabTeX User's Guide日本語版](http://www.kotoito.net/arabtex.html) ArabTeXのマニュアル日本語訳

[Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink") [Category:アラビア文字](https://ja.wikipedia.org/wiki/Category:アラビア文字 "wikilink")