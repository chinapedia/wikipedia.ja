> この記事は[Sendmail](https://ja.wikipedia.org/wiki/Sendmail)から翻訳されています。


**Sendmail** は [UNIX](../Page/UNIX.md "wikilink") で古くから使われてきた[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")[ソフトウェアである](../Page/アプリケーションソフトウェア.md "wikilink")。

Sendmail プログラム本体は、[パターンマッチルールによって動作する](../Page/パターンマッチング.md "wikilink")[オートマトン](https://ja.wikipedia.org/wiki/オートマトン "wikilink")と、[MTA動作を支援する](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")[ユーティリティである](https://ja.wikipedia.org/wiki/ユーティリティソフトウェア "wikilink")。 MTA としての動作そのものは、sendmail.cf に記述された複雑で莫大な量のパターンマッチルールによって実現している。

## 歴史

[1980年代](../Page/1980年代.md "wikilink")から[1990年代](../Page/1990年代.md "wikilink")にかけて、数多くの[企業](https://ja.wikipedia.org/wiki/企業 "wikilink")や[研究機関](https://ja.wikipedia.org/wiki/研究機関 "wikilink")により、様々な電子メールプロトコルと、それらを[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")した独自仕様の電子メールシステムが乱立していた。Sendmail は、それらの乱立する各種プロトコルを相互変換し、橋渡しする目的で登場した。

電子メールプロトコルよりも底層に位置する通信プロトコルには、近年[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")の普及により一般的になった[TCP/IPだけでなく](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")、[パソコン通信](../Page/パソコン通信.md "wikilink")が主流であった時代の[UUCPなど](https://ja.wikipedia.org/wiki/Unix_to_Unix_Copy_Protocol "wikilink")、様々なものに対応している。しかし、その柔軟性の代償として[セキュリティホール](https://ja.wikipedia.org/wiki/セキュリティホール "wikilink")が多く見つかっている。

2013年10月、米によるの買収により、その開発やサポートもプルーフポイントに移管された\[1\]。

## 特徴

  - 設定ファイルの複雑性

:\* 設定ファイルが非常に複雑であるため、通常はまず mc ファイルという [M4](https://ja.wikipedia.org/wiki/M4_\(プログラミング言語\) "wikilink") [マクロ言語](https://ja.wikipedia.org/wiki/マクロ言語 "wikilink")で記述してから、実際のファイル（cf）を生成する。

:\* 設定ファイルの複雑さとセキュリティホールのできやすさを改善するために、いくつか代替のメールサーバも開発されている。

  - 商用版 Sendmail

:\* Sendmail には[オープンソース](../Page/オープンソース.md "wikilink")版と[商用版があり](https://ja.wikipedia.org/wiki/商用ソフトウェア "wikilink")、商用版ではIMAP/POPサーバを構築することのできる Sendmail Advanced Server という製品がある。

:\* 商用版では設定方法に[GUIを利用でき](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、GUI上から設定内容を反映することができる。

:\* 柔軟性と引き換えに設定方法の複雑さが増しているため、商用サポートや商用版により複雑さを取り除くオプションが用意されているとも言える。

:\* 商用版では、メールの送信速度も改善されている。

  - 次世代 Sendmail

:\* まったく新たに構造を作り直した次世代の Sendmail として Sendmail X が開発される。その後 MeTA1 と改名された\[2\]。

  - Milter API のサポート

:\* Sendmail では [Milter](https://ja.wikipedia.org/wiki/電子メールフィルタリング "wikilink") API をサポートしているため、Milter API で作成された[プラグイン](https://ja.wikipedia.org/wiki/プラグイン "wikilink")を容易に利用することができる。

:\* 有名なOpenSource Milterとしては[SpamAssassin](https://ja.wikipedia.org/wiki/SpamAssassin "wikilink")があり、商用Red Hat系の製品では標準的に用意されている。

:\* スパム対策、[ウイルス対策](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")、[コンプライアンス対策](https://ja.wikipedia.org/wiki/企業コンプライアンス "wikilink")、メール[アーカイブなど](https://ja.wikipedia.org/wiki/アーカイブ_\(コンピュータ\) "wikilink")、Milter によって実現可能な領域が広がっている。

:\* 商用の製品としては Mailstream Manager という製品を導入することで商用の Milter プラグインを利用できる。

## 脚注

<references/>

## 関連項目

  - [Courier-MTA](https://ja.wikipedia.org/wiki/Courier-MTA "wikilink")
  - [Postfix](https://ja.wikipedia.org/wiki/Postfix "wikilink")
  - [qmail](https://ja.wikipedia.org/wiki/qmail "wikilink")
  - [XMail](https://ja.wikipedia.org/wiki/XMail "wikilink")
  - [エリック・オールマン](https://ja.wikipedia.org/wiki/エリック・オールマン "wikilink")

## 外部リンク

  - [Sendmail.org](http://www.sendmail.org/)

[Category:メール転送エージェント](https://ja.wikipedia.org/wiki/Category:メール転送エージェント "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.  <http://www.sendmail.org/sm-X/>