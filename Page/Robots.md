> この記事は[Robots](https://ja.wikipedia.org/wiki/Robots)から翻訳されています。


***robots***（ロボッツ）は、[ターン制](https://ja.wikipedia.org/wiki/ターン制 "wikilink")の[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")である。プレイヤーキャラクターを追いかけて殺すようにプログラムされたロボットから逃げ、ロボット同士や障害物と衝突させて破壊するのが目的である。

1970年代の[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")のプラットフォームで制作された***Chase***（チェイス）というゲームを源流とする。多くのバリエーションが存在するが、その中でも著名なのが、[ホビーパソコン](../Page/ホビーパソコン.md "wikilink")上の***Escape\!***（エスケープ\!）や***Zombies***（ゾンビーズ）、[MacOS](../Page/MacOS.md "wikilink")の***Daleks***（ダレクス）、そして[UNIX](../Page/UNIX.md "wikilink")の***robots***である。

オリジナルのゲームの著者は不明であるが、[1970年代](../Page/1970年代.md "wikilink")初期に[ダートマス大学](../Page/ダートマス大学.md "wikilink")の[DTSS](../Page/DTSS.md "wikilink")で制作された可能性が高い。[1976年](../Page/1976年.md "wikilink")初頭に『』誌に最初の公開バージョンが登場し、その後の数年間で様々な修正バージョンが登場した。Daleksとrobotsはどちらも[1984年](../Page/1984年.md "wikilink")に登場し、ここからも派生バージョンが生まれた。

## 内容

[Robots_text_screenshot.png](https://ja.wikipedia.org/wiki/File:Robots_text_screenshot.png "fig:Robots_text_screenshot.png") プレイ画面は長方形の2次元のグリッドである。プレイヤーキャラクターを殺すようにプログラムされた複数のロボットから逃げ切るのがゲームの目的である。

ゲームはターン制である。オリジナルのバージョンでは、プレイヤーのプレイ開始位置はランダムに決定される。 GNOMEバージョンなど一部の派生バージョンでは、プレイヤーはグリッドの中心からプレイを開始する。ロボットは、グリッド上のランダムに選択された場所に配置される。プレイヤーキャラクターは任意の方向（上下左右または斜め）に1マス移動するたびに、各ロボットはプレイヤーキャラクターにできるだけ近づくように1マス移動する。プレイヤーキャラクターがロボットと衝突すると、プレイヤーキャラクターは死亡し、ゲームが終了する。

ロボットは、グリッド上の他のオブジェクト（ロボットまたは障害物）と衝突すると破壊される。*Chase*から派生した初期のバージョンでは、グリッド上に障害物が複数設置されている。*robots*から派生した後のバージョンでは、最初は障害物はなく、2つのロボットが衝突したときに、その場所に障害物ができる。どちらの場合も、障害物に衝突するとプレイヤーキャラクターもロボットも死亡する。プレイヤーは、ロボットが自身を追いかける性質を利用して、ロボット同士が衝突したり、静止している障害物に衝突したりするようにプレイヤーキャラクターを移動させる。

ロボットから逃げることが困難な場合には、[テレポートすることもできる](../Page/瞬間移動.md "wikilink")。テレポートは1ターンとみなされ、ロボットは移動先に向かって移動する。移動先はランダムに選択されるため、移動先でロボットや障害物に接触する可能性もある。一部のバージョンには、オブジェクトがない場所へ確実に移動する「安全なテレポート」機能や、近くにあるロボットを破壊できる「近接武器」機能を持ったものもあるが、いずれも使用回数は限られている（各レベルごとに1回など）。いくつかのバージョンではさらに戦車が追加されている。これはロボットと同様に動作するが、他のオブジェクトと衝突しても破壊されない。

全てのロボットが破壊されると、ゲームクリアとなる。最近のバージョンでは、ゲームをクリアすると、よりロボットの数の多い次のレベルに進む。

## 歴史

[Robots_graphic_screenshot.png](https://ja.wikipedia.org/wiki/File:Robots_graphic_screenshot.png "fig:Robots_graphic_screenshot.png") オリジナルの*Chase*は、[ダートマス大学](../Page/ダートマス大学.md "wikilink")の[DTSS](../Page/DTSS.md "wikilink")にて[ダートマスBASIC](https://ja.wikipedia.org/wiki/ダートマスBASIC "wikilink")で書かれた。オリジナルの著者は不明であり、オリジナルのソースコードは所在不明となっている。

『』誌の1976年1-2月号に、ビル・コッター(Bill Cotter)がオリジナルソースをに移植したソースコードが掲載された\[1\]。そのソースコードは1979年の*More BASIC Computer Games*に再掲載され、メインフレーム時代のダートマスBASICゲームの作者であるマック・オーグルズビー(Mac Oglesby)が元の作者であったと示唆するメモが追加された\[2\]が、オーグルズビーはオリジナルのゲームの作者であることを否定している。

このゲームをそのまま移植したものが、同時代のコンピュータ雑誌に登場した。その中には、SWCP 4k BASIC\[3\]や、にカードを使用したグラフィカルバージョンなどがある\[4\]。また、 IV上で[PLATO](https://ja.wikipedia.org/wiki/PLATO "wikilink")システムの言語により*HiVolts*として移植された\[5\]。

*Escape\!*として知られるバージョンからは多くの派生バージョンが生まれたが、この名前が最初に使われたのがいつであるかは不明である。その中の1つは*Announcing: Computer Games*誌に掲載された[TRS-80](../Page/TRS-80.md "wikilink")向けのもので、別の敵である戦車が追加され、テレポートの回数が2回に制限された\[6\]。*Escape\!*の商用グラフィック版は、1982年に社によって発売された。このバージョンでは、プレイヤーが自身のキャラクターを動かさなくてもロボットが動くリアルタイムモードが追加された。*Creative Computing*誌のこのゲームのレビューには、オリジナルの作者がマック・オーグルズビーであると書かれている\[7\]。

*Robot Minefield*として知られる*Escape\!*の修正バージョンは、1983年に(Tim Hartnell)とネイサン・ブッチャー(Nathan Butcher)によってリリースされた。このバージョンでは、敵の数が4体に減らされ、戦車は廃止された。さらに、プレイヤーキャラクターは4方向（上下左右）にしか移動できないが、ロボットは斜めにも移動することができた。ゲームはリアルタイムモードのみであり、プレイヤーが熟考していると、ロボットが集まってきてゲームオーバーになってしまう。このバージョンは、1983年の*Giant Book of Computer Games*で発表された\[8\]\[9\]。

UNIX版の*robots*は、1984年11月にアラン・R・ブラック(Allan R. Black)によって開発された。1985年5月に[ネットニューズ](https://ja.wikipedia.org/wiki/ネットニューズ "wikilink")のニュースグループ *net.sources.games* に投稿された\[10\]\[11\]。その後、によって[BSD](../Page/BSD.md "wikilink")に移植された。BSD版の*robots*は、1986年6月に4.3BSDで初めて登場した\[12\]\[13\]。

## 関連項目

  - [ロボトロン2084](../Page/ロボトロン2084.md "wikilink") - このゲームのリアルタイムモードを元にして開発されたアーケードゲーム

## 脚注

### 注釈

### 出典

[Category:Linux用ゲームソフト](https://ja.wikipedia.org/wiki/Category:Linux用ゲームソフト "wikilink") [Category:メインフレーム用ゲームソフト](https://ja.wikipedia.org/wiki/Category:メインフレーム用ゲームソフト "wikilink") [Category:ロボットを題材としたコンピュータゲーム](https://ja.wikipedia.org/wiki/Category:ロボットを題材としたコンピュータゲーム "wikilink") [Category:アメリカで開発されたコンピュータゲーム](https://ja.wikipedia.org/wiki/Category:アメリカで開発されたコンピュータゲーム "wikilink")

1.
2.  [Chase (additional detail from 1979)](http://www.atariarchives.org/morebasicgames/showpage.php?page=26)
3.
4.
5.
6.
7.
8.  [GameBase64: Robot Minefield](http://www.gamebase64.com/game.php?id=23433&d=18)
9.  [Tim Hartnell's Giant Book of Computer Games, p.273: Robot Minefield](http://wos.meulie.net/pub/sinclair/books/GiantBookOfComputerGames\(BallantineBooks\).pdf)
10.
11. [robots, by Allan R. Black](https://github.com/fjarlq/robots)
12. [4.3BSD robots(6) man page](http://www.retro11.de/ouxr/43bsd/usr/man/cat6/robots.0.html)
13. [4.3BSD robots source code](http://minnie.tuhs.org/cgi-bin/utree.pl?file=4.3BSD/usr/src/games/robots)