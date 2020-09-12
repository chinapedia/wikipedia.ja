> この記事は[TV program Making language](https://ja.wikipedia.org/wiki/TV_program_Making_language)から翻訳されています。


**TVML**（）は、[テレビ番組](../Page/テレビ番組.md "wikilink")を記述する特別な言語である。この言語で記述されたテレビ番組[台本](../Page/台本.md "wikilink")をTVMLプレイヤーと呼ばれる[ソフトウェア](../Page/ソフトウェア.md "wikilink")で再生すると、リアルタイム[CG](https://ja.wikipedia.org/wiki/CG "wikilink")や[音声合成](../Page/音声合成.md "wikilink")などにより作られた映像音声を即座に見ることができる。

TVMLは[NHK放送技術研究所](../Page/NHK放送技術研究所.md "wikilink")が1996年に提案し、以降、当所を中心に言語仕様の[アップデート](https://ja.wikipedia.org/wiki/アップデート "wikilink")およびTVMLプレイヤーの開発が進められている。TVMLプレイヤーは[フリーウェア](../Page/フリーウェア.md "wikilink")で配布されており、大学、教育機関などでの利用が多い。また、NHK番組制作での利用のほか、いくらかの商用利用もされている。

## 言語記述

TVMLの書式は、やらせたいことを書き並べるだけの単純なものである。

`camera: closeup ( what = Bob )`
`character: bow ( name = Bob )`
`character: talk ( name = Bob, text = "これ見てよ" ) `
`title: display ( type=imagefile, filename = "neta.jpg" )`

このように書いてTVMLプレイヤーで再生すると

`カメラがBobにクローズアップして`
`Bobがおじぎしてから`
`「これ見てよ」と 合成音声でしゃべった後`
`neta.jpgという画像が表示される`

という映像が得られる。このように、TVMLは上から一行一行実行して行くだけのシンプルな動作をするので、かなり簡単に映像を作ることができる。

TVMLは次に上げるようなテレビ番組を制作するのに十分な機能をサポートしている。

`CGキャラクタのしゃべりと動作 (character) `
[`カメラワーク`](https://ja.wikipedia.org/wiki/カメラワーク "wikilink")`  (camera)`
`小道具の配置  (prop)`
`スタジオセット (set)`
`照明  (light)`
`2Dタイトル表示  (drawing)`
[`スーパーインポーズ`](https://ja.wikipedia.org/wiki/スーパーインポーズ "wikilink")` (super)`
`ムービーファイル再生  (movie)`
`オーディオファイル再生  (sound)`
[`ナレーション`](https://ja.wikipedia.org/wiki/ナレーション "wikilink")入れ`  (narration)`

## TVMLプレイヤー

TVMLプレイヤーはTVMLスクリプトを再生するソフトウェアで、現在、[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")の[PCで動くものがNHK技研および](../Page/パーソナルコンピュータ.md "wikilink")（株）[インターネット総合研究所](../Page/インターネット総合研究所.md "wikilink")で開発され、フリーウェアとして配布されている。

## その他の話題

  - 言語仕様は2010年時点でVersion2.0とVersion3.0が混在した状態である。ただし、両者に大きな相違はない。
  - TVMLプレイヤーのほか、平書き台本だけで番組が作れる「TVMLプレイヤーミニ」や「TV4U TVCreator」もフリーウェア配布している。
  - tvifと呼ばれる[SDKを配布しており](../Page/ソフトウェア開発キット.md "wikilink")、TVMLプレイヤーエンジンを外部ユーザーアプリケーションから使用することができる。
  - TVMLを考案した林正樹\[1\]（当時NHK技研在籍）は（株）インターネット総合研究所で引き続きTVMLの開発を進めた。同社ではTVMLと平書き台本が再生できる「T2Vプレイヤー」をフリーウェアで配布した。
  - [米Microsoft Corp.と米](../Page/マイクロソフト.md "wikilink")[WebTV](../Page/WebTV.md "wikilink") Networks, Inc.が開発した言語に同じ名前のTVMLというものがあるが、これとは異なる言語である。
  - TVMLの言語仕様は[プロトタイプベース](../Page/プロトタイプベース.md "wikilink")[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")に近い。character, cameraなどの「イベント」が[オブジェクトに相当し](../Page/オブジェクト_\(プログラミング\).md "wikilink") walk(), talk()などの「コマンド」が[メソッドや](../Page/メソッド_\(計算機科学\).md "wikilink")[メンバ関数](https://ja.wikipedia.org/wiki/メンバ関数 "wikilink")に相当する。ただし、characterやcameraなどのイベントタイプは自作することができず、あらかじめ用意されたものを使う。TVMLの上位[レイヤーとしてこれらオブジェクト指向型の言語を策定しようとする動きもある](../Page/階層構造.md "wikilink")。
  - 「台本」のようなコードを記述するコンピューター言語には他にも、「[Shakespeare言語](../Page/Shakespeare_\(プログラミング言語\).md "wikilink")」や「[Mana言語](https://ja.wikipedia.org/wiki/Mana_\(プログラミング言語\) "wikilink")」がある（TVMLは[データ記述言語](../Page/データ記述言語.md "wikilink")の一種であるが、これらの言語は[プログラミング言語](../Page/プログラミング言語.md "wikilink")である）。

## 脚注

## 関連項目

  - [Mana (プログラミング言語)](https://ja.wikipedia.org/wiki/Mana_\(プログラミング言語\) "wikilink")
  - [Shakespeare (プログラミング言語)](../Page/Shakespeare_\(プログラミング言語\).md "wikilink")
  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")
      - [データ記述言語](../Page/データ記述言語.md "wikilink")

## 外部リンク

  - [TVMLオフィシャルホームページ](http://www.nhk.or.jp/strl/tvml/)

  - \- インターネット総合研究所

  - [TVML Player mini](http://www.nhk.or.jp/strl/tvml/japanese/mini/index.html)

  - [TV4Uウェブサイト](http://www.nhk.or.jp/strl/tvml/tv4u/index.html)

[Category:コンピュータ言語](https://ja.wikipedia.org/wiki/Category:コンピュータ言語 "wikilink") [Category:テレビ番組](https://ja.wikipedia.org/wiki/Category:テレビ番組 "wikilink") [Category:放送文化基金賞・放送技術](https://ja.wikipedia.org/wiki/Category:放送文化基金賞・放送技術 "wikilink")

1.  [林正樹ホームページ](http://hayashimasaki.net/)