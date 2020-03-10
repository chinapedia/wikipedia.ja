> この記事は[System4 \(\)](https://ja.wikipedia.org/wiki/System4_\(\))から翻訳されています。


**System4** は[アダルトゲーム](../Page/アダルトゲーム.md "wikilink")を手がける[アリスソフト](../Page/アリスソフト.md "wikilink")が製作した、[Windows上で動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ゲームエンジン](https://ja.wikipedia.org/wiki/ゲームエンジン "wikilink")であり、アリスソフトが販売するゲームに使用されている。随時バージョンアップが行われていることから System4.xという表現がとられる場合もある。開発環境であるSystem4[SDKと共にウェブ上で配布されており](https://ja.wikipedia.org/wiki/ソフトウェア開発キット "wikilink")（現在は公開を中止）、System4という単語が開発環境を指している場合もある。

## 概要

[System3がスクリプトに記述されたソースコードの行やラベルに着目してゲームの実行を行う一種の](https://ja.wikipedia.org/wiki/System3_\(アリスソフト\) "wikilink")[BASIC](../Page/BASIC.md "wikilink")的なエンジンであったのに対し、System4は構造化/オブジェクト指向化を推し進めた言語となっている。これにより、言語を習得することの難易度は若干上がったと思われるものの、以前より大規模なゲームを整然と記述することが可能になったと思われる（[構造化言語](https://ja.wikipedia.org/wiki/構造化言語 "wikilink")、[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")）。

System4は[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")された[中間コード](https://ja.wikipedia.org/wiki/中間コード "wikilink")を解釈しながらゲームを実行する。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のようにユーザーのPC上に[VMを設置することで](https://ja.wikipedia.org/wiki/バーチャルマシン "wikilink")、ゲーム開発者がユーザーのPC環境を意識せずともゲームが正常に動作することを狙っているとされる。このことを指して、仮想OSと表現されることがある。

## 成立の経緯

アリスソフトはSystem4を開発するより以前、やはり自社製である[System3を利用してゲームを製作](https://ja.wikipedia.org/wiki/System3_\(アリスソフト\) "wikilink")・販売していた。このSystem3は元々[C言語](../Page/C言語.md "wikilink") で記述されており、末期には度重なる機能追加によってコードが肥大化し保守が困難なものになっていたと言われている。この状況を打開すべく、大規模な開発に適した [C++言語](https://ja.wikipedia.org/wiki/C++言語 "wikilink")で一から書き起こされたのがSystem4である。 このメジャーバージョンアップに関しては、C++を習得したプログラマの入社がきっかけの一つであった様である。

## System4SDK

System4SDKには System4とその[コンパイラ](../Page/コンパイラ.md "wikilink")、[デバッガ](../Page/デバッガ.md "wikilink")、画像ファイルの[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")変換ツール、リファレンスマニュアルとサンプルソースファイル等が含まれる。

ゲーム開発環境の中には、シナリオを記述し、画像ファイルを指定するだけでノベルゲームやアドベンチャーゲームを製作できる簡便なものも存在するが、System4の場合はもっと低級（[低級言語](https://ja.wikipedia.org/wiki/低級言語 "wikilink")と言う場合の「低級」と同様の意味合い）な開発環境となる。サウンドや[スプライト等](../Page/スプライト_\(映像技術\).md "wikilink")、ゲーム製作に必須と思われる機能が提供される以外に、C（及びC標準ライブラリ）と似たような文字列操作を提供する関数や各種演算子、C++のデータ型やクラス機能に近いものも実装されている。System4本体は[DLL](https://ja.wikipedia.org/wiki/DLL "wikilink")を呼び出す機能しか持たず、主要な機能は外部DLLによって提供される。また、System4が持たない機能を補うために外部DLLを追加し、制御を渡すことも可能であり、System4を実質利用せずに外部DLLだけでゲームを完結させることも可能である。

System4SDKは商用・非商用を問わず無償で利用でき、製作したゲームを公開する際にはSystem4エンジンを同梱することが許されている。ただし、System4に関してアリスソフトによる保証・サポートは一切ない。

見方によっては高度なゲーム製作環境であるが、ユーザーによる利用はそれほど盛んではない。理由としては、趣味のゲーム製作においては扱いが簡単なツールが好まれることや、System4を使いこなせる者であれば最初からCやC++を選択するであろうことが考えられる。

なお、System4SDKは当初ユーザークラブ（アリスソフト主催の公式ファンクラブ）において会員に対して配布されていたが2008年春に公開が中止された。ただしSDKのアーカイブは再配布が認められていたため、現在もファンサイトから非公式ながら入手は可能である。

[Category:アリスソフト](https://ja.wikipedia.org/wiki/Category:アリスソフト "wikilink") [Category:ゲームエンジン](https://ja.wikipedia.org/wiki/Category:ゲームエンジン "wikilink")