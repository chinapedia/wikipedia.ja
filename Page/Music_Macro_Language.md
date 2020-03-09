> この記事は[Music Macro Language](https://ja.wikipedia.org/wiki/Music_Macro_Language)から翻訳されています。


**Music Macro Language**（ミュージック・マクロ・ランゲージ）とは音楽演奏を表現する[データ記述言語](https://ja.wikipedia.org/wiki/データ記述言語 "wikilink")ないし[ドメイン固有言語](https://ja.wikipedia.org/wiki/ドメイン固有言語 "wikilink")である。**MML**と略されることが多いが、[XMLの一種である](../Page/Extensible_Markup_Language.md "wikilink")[Music Markup Languageも音楽を表現するものでそちらもMMLと略されるため](https://ja.wikipedia.org/wiki/Music_Markup_Language "wikilink")、混同されることがある。

楽曲として聞くに堪える音声信号を直接表現するとデータ量が膨大になるため、また人間可読な文字列として簡単にシーケンスデータを入力するため、初期の[パソコン](https://ja.wikipedia.org/wiki/パソコン "wikilink")での音楽演奏によく使われた。独立した演奏プログラムとしての実装と、[BASIC](../Page/BASIC.md "wikilink")に埋込みの、`PLAY`文で演奏するものと、どちらが先かは定かではない。

現代でも簡単にシーケンスデータを表現するものとしてよく使われている。[SMFや各種演奏ソフト用のデータ形式に変換するものをMMLコンパイラと呼んでいる](https://ja.wikipedia.org/wiki/Standard_MIDI_File "wikilink")。

## 主なコマンド

方言は音源や実装により多種多様である。ここでは代表的（比較的どれでも共通）なものを挙げるが、違っているものもある。大文字小文字を区別しないものが多いが、区別して別のコマンドとしているものもある。

  - `C D E F G A B`
    それぞれ、ドレミファソラシの[音符](https://ja.wikipedia.org/wiki/音符 "wikilink")。
  - [`#`](https://ja.wikipedia.org/wiki/変化記号 "wikilink")`  + - `
    音符の後につけて半音上げ下げを表す。\#と+は同じ意味。
  - `R`
    休符。
  - 数字 `.`
    音符や休符の後につけ、音の長さを表す。`2`=2分音符。`.`は付点で長さを1.5倍する。`4.`=付点4分音符。
  - `&`
    二つの音符を連結する。[タイを表す](https://ja.wikipedia.org/wiki/タイ_\(音楽記号\) "wikilink")。前後の音階が異なる場合、無視される、[スラー](https://ja.wikipedia.org/wiki/スラー "wikilink")として処理される、[ポルタメント](https://ja.wikipedia.org/wiki/ポルタメント "wikilink")として処理される、など、扱いは実装によって異なり、一定ではない。
  - `O`
    [オクターブ](https://ja.wikipedia.org/wiki/オクターブ "wikilink")指定
  - `> <`
    オクターブの上下。どちらがアップダウンを意味するかは実装によって異なる
  - `L`
    `A`～`G`や`R`の後に数字をつけないときの音の長さを指定。初期値は4であることが多い。
  - `V`
    音量（ボリューム）を指定
  - `@`
    [FM音源](https://ja.wikipedia.org/wiki/FM音源 "wikilink")などでの音色の指定
  - `T`
    [テンポ](https://ja.wikipedia.org/wiki/テンポ "wikilink")を指定。たとえば「`T120`」なら120BPMで演奏する。プラットフォームによってはテンポのずれが発生する。

やや一般的でないものに、次のものが挙げられる。

  - `N`
    通常のオクターブ+CDEFGABではなく、音の高さを数値で直接指定する。
  - `Q`
    発音の長さを指定する。[レガート](https://ja.wikipedia.org/wiki/レガート "wikilink")や[スタッカート](https://ja.wikipedia.org/wiki/スタッカート "wikilink")を表現する。
  - `P`
    左右の定位を設定する。噛み砕いて言えば[ステレオ](../Page/ステレオ.md "wikilink")設定である。
  - `S`
    [PSGの](../Page/Programmable_Sound_Generator.md "wikilink")[エンベロープの種類を選択する](https://ja.wikipedia.org/wiki/ADSR "wikilink")。
  - `M`
    PSGのエンベロープの周期を設定する。
  - `Y`
    ハードウェア固有のパラメータ設定。

## 「テンポずれ」対策

古い[パソコンの一部の演奏系では](../Page/パーソナルコンピュータ.md "wikilink")、実際の分解能が低いために、テンポや音長の指定のしかたによっては強烈な「テンポずれ」と呼ばれる、分数で表現される厳密値との時間ズレが発生した。これを回避するために、様々な運用上の工夫がされた。

### 対策1・最短音符合わせ

多用された技法の1つに「最短音符合わせ」というものがある。「みんな一斉にまとめてずれれば、ずれがわからない」という理屈であり、全ての音長を、短い音符の連続で記すが、可読性は非常に悪くなる。以下に一例を記す。

  - 通常の表現
    `C4D4E4F4` もしくは `L4CDEF`
  - 最短音符合わせ
    `L16C&C&C&CD&D&D&DE&E&E&EF&F&F&F`

その後、さまざまな個人や企業が音源ドライバを開発したが、それらはテンポずれが発生しないように設計されていた。また、テンポずれが発生する環境でも、最短音符合わせを使わずにテンポずれを防ぐ技法が編み出された\[1\]。そのため、可読性が悪い最短音符合わせは、次第に使われなくなっていった。

### 対策2・使用するテンポの限定

後発の音源ドライバにおいても発生した事象として「特定のテンポにおいて、目的とする音長が再現されない結果リズム感を損ねた再生が行われる」ことがある。これは「1秒間のtick数×60÷テンポ数」が整数、かつその値を「音符の分数÷4」で割った値が整数、という条件を満たさないことが原因で発生する。逆にこの条件を満たすテンポと分数で作られた曲は音長のズレや曲の破綻が発生しない。

  - 例: 1秒間のtick数が60（1分間の1秒間のtick数が3600）のシステムにおける使用可能なテンポの例
    **60**, **75**, **80**, **90**, **100**, **120**, **150**, **180**, **200**, **225**, **240** など

#### 応用・テンポ数225と64分音符による音長表現法

分解能の低さは、[テクノポップ](https://ja.wikipedia.org/wiki/テクノポップ "wikilink")などのグルーブ感（音長やリズムの微妙な変化とその一定性）を重視する音楽の多くをPCとMMLでは再現困難または不能とする。また、通常の4分音符や8分音符という長さのみでの表現はそもそも不可能な曲もある。しかし「tickが1/60秒のシステムの場合は、テンポ225に設定することで64分音符をtick1回分の長さとして扱うことが可能」というテクニックで、テンポと音長の組み合わせでは再現できなかった音長の楽曲が演奏可能となる。

  - 例：7/60音長(`x16..`)に設定すると、テンポ128.571(以下略)の16分音符となる

これにより一部のテクノやハウスなどの楽曲も演奏可能になる。またこのように4の倍数以外の音長で構成される曲のテンポは非整数値となる。この手法も後に絶対音長を指定できる音源ドライバが登場して以降、使用頻度は減少する。

## 脚注

<references />

## 関連項目

  - [チップチューン](https://ja.wikipedia.org/wiki/チップチューン "wikilink")
  - [N88-BASIC](https://ja.wikipedia.org/wiki/N88-BASIC "wikilink")
  - [ABC記譜法](https://ja.wikipedia.org/wiki/ABC記譜法 "wikilink")
  - [Ray (ソフトウェア)](https://ja.wikipedia.org/wiki/Ray_\(ソフトウェア\) "wikilink")

## 外部リンク

  - [SPICE](http://gorry.haun.org/spice/index.html)
  - [テキスト音楽「サクラ」](http://oto.chu.jp/)
  - [714MIDI・みゅあっぷ98](http://homepage3.nifty.com/y_ohta/packen/index.htm)
  - [Z-MUSIC](http://www.z-z-z.jp/index.htm)
  - [MuSICA 講座・テンポずれ対策](http://www002.upp.so-net.ne.jp/ahiroe/msx/mlecture.html#tempo)

[Category:コンピュータ言語](https://ja.wikipedia.org/wiki/Category:コンピュータ言語 "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:記譜法](https://ja.wikipedia.org/wiki/Category:記譜法 "wikilink")

1.  たとえば[N88-BASIC](https://ja.wikipedia.org/wiki/N88-BASIC "wikilink")の場合、`T`コマンドの値を88/176/177等に固定し、`Y`コマンドでOPNのTIMER-Bを操作してテンポを指定することにより、テンポずれを防ぐことができる。