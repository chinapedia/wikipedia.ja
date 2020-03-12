> この記事は[StepMania](https://ja.wikipedia.org/wiki/StepMania)から翻訳されています。


**StepMania**（ステップマニア）はPC用の[オープンソース](../Page/オープンソース.md "wikilink")[音楽ゲーム](../Page/音楽ゲーム.md "wikilink")である。

## 概要

一般的には[コナミ](https://ja.wikipedia.org/wiki/コナミ "wikilink")の『[Dance Dance Revolution](https://ja.wikipedia.org/wiki/Dance_Dance_Revolution "wikilink")』（以下DDRと表記）の[シミュレータ](https://ja.wikipedia.org/wiki/シミュレータ "wikilink")とされているが、実際には[デフォルトで](../Page/デフォルト_\(コンピュータ\).md "wikilink")[Pump It Up](../Page/Pump_It_Up.md "wikilink")、追加のプログラムを組み込めば[ParaParaParadise](../Page/ParaParaParadise.md "wikilink")や[EZ2Dancer](../Page/EZ2Dancer.md "wikilink"),[Pop'n musicなどのシミュレータとしても使うことができる](../Page/Pop'n_music.md "wikilink")（ただしノートの形式などプレイに直接関与する部分のみ対応させる物であり、得点計算などについては対応していない）。

元々は[Windows用であるが](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[Linux](../Page/Linux.md "wikilink")への移植も行われている。また、（正当なものではないが）[Xboxへの移植も行われている他](../Page/Xbox_\(ゲーム機\).md "wikilink")、海外ではこのゲームのエンジンを使用したダンスゲーム『In the Groove』も発売されている。

日本国内においては2004年のfoonmixの公開から使用する人が多くなり、別のStepmaniaパッケージを配信するユーザーや、プレイ動画をYoutubeやニコニコ動画等に投稿するユーザーも現れ、盛んとなった。しかし最近は、パッケージに楽曲提供を行った有名同人アーティストの商業用音楽ゲームへの進出や、パッケージ配信を行っていたユーザーの諸事情などにより、過去に比べ公開されているパッケージやそれを制作するユーザーが少なくなっている。

## 機能

  - 譜面は専用の[テキストファイル](../Page/テキストファイル.md "wikilink")である.smや.sscの他、[Dance With Intensity用のDWI](https://ja.wikipedia.org/wiki/Dance_With_Intensity "wikilink")、同じ曲に対する複数の[BMSの集合等の形で持つことができる](https://ja.wikipedia.org/wiki/BMS_\(音楽ゲーム\) "wikilink")。なお、後述するEDITで保存する際に、3.9ではsmとDWI、5.0ではsmとssc2つの譜面ファイルを生成する。
  - 家庭用DDRに似た形のEDIT MODEで譜面の作成ができる。なお、譜面にはDDR同様の矢印の他に、踏んではいけない（通過したときにその方向が押されていると爆発してゲージが減る）地雷を設置することができる他、DDRよりも細かい（24分/32分/48分/64分、StepMania4.0以降では左記に加え192分）タイミングの配置も可能で、DDRのEDITにある「1ラインにつき2方向まで」の制限もなくなっている。
  - [テーマファイルにより外観などを非常に自由に作成できる](https://ja.wikipedia.org/wiki/スキン "wikilink")（ゲームモードの数を増減する事もできる）他、随時かかるアナウンスやプレイ中に流れる矢印マークなど様々な箇所をカスタマイズ出来る。
  - ゲーム中で選択できるオプションの中には、DDRに存在しない物も多数ある。例えば譜面の速度を1曲通して一定値にする"C???"（"???"にスクロール速度が入る。スクロール停止箇所もC???適用時は対応する幅の空白として表示される）や、譜面が一度逆方向に流れた後順方向に戻ってくる"[BOOMERANG](../Page/ブーメラン.md "wikilink")"など。
  - 作成した譜面やテーマなどは付属のツールで[ZIPアーカイブのパッケージにして配布することもできる](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")。このときに複数の種類のデータをまとめて梱包することも可能。ツールで作成した配布ファイルは拡張子がsmzipであり、ツールを用いてインストールすることもできる。

## ライセンスに関して

当初StepManiaは[GPLの下で公開されていたが](../Page/GNU_General_Public_License.md "wikilink")、『In the Groove』として商業展開するに当たってはGPLによる[ソース公開義務が](../Page/ソースコード.md "wikilink")[著作権](../Page/著作権.md "wikilink")との絡みで問題となった。そのため場合によってはソースを公開しなくてもよい形式のライセンスに変更することになったが、そのためにはそれまでの開発に貢献した人たちの了承を得る必要があった。これについては『In the Groove』のスタッフ表記に全開発者の名前を出すという形で合意され、以降StepManiaは[MITライセンスでの公開となった](https://ja.wikipedia.org/wiki/オープンソース#X11_のライセンス "wikilink")。

場合によってはソースを公開する必要がなくなったとはいえ、今日でもStepMania自体はオープンソースである。しかし実際の所、2006年現在主流の3.x系列はDDRシリーズと似通っている箇所が多い。初期状態で[インストール](../Page/インストール.md "wikilink")されているテーマファイルでのタイトル画面は「SMMAX」となっており、その他においてもDDRシリーズ作品のひとつのDDRMAXと類似する箇所が見受けられる。以上の問題点がライセンス等で懸念されるため、どの[Linux](../Page/Linux.md "wikilink")ディストリビューションも公式パッケージのラインナップにStepManiaを含めるには至っていない。AlphaバージョンのStepMania 4では、独自のテーマファイルで製作が進行しており、この問題が解決される可能性があったものの開発が進まず、4シリーズは5シリーズの評価版として開発されることになり、新たに3.9・3.95シリーズを拡張した4.0が開発されることとなった\[1\]。この4.0シリーズでは、一部のグラフィック、音楽が改変されているものの、その他は3.9シリーズベースのままであり、大きな改善とはなっていない。

### オンライン対戦について

StepMania3.95・4.0に付属したStepManiaOnlineを用いると、オンライン対戦ができるようになる。 チャットなどを利用することができるが、日本語には対応しておらず、Alt+半角/全角で日本語入力を有効にすると、勝手に文字が打ち込まれる状態になる。 オンライン対戦するには、利用するサーバーによってアカウントを取得しなければいけない。 オンライン対戦用のサイトから登録可能。 （オンライン対戦専用のパックもある）

## 脚注

<references />

## 関連項目

  - [BMS (音楽ゲーム)](https://ja.wikipedia.org/wiki/BMS_\(音楽ゲーム\) "wikilink")
  - [MSD (音楽ゲーム)](https://ja.wikipedia.org/wiki/MSD_\(音楽ゲーム\) "wikilink")

## 外部リンク

  - [StepMania公式サイト](http://www.stepmania.com/) （英語、[Altavistaの翻訳サービス経由](http://babelfish.altavista.com/babelfish/tr?doit=done&url=www.stepmania.com/stepmania/&lp=en_ja)）
  - [StepMania Online](http://www.stepmaniaonline.com/)（英語、オンライン対戦版）
  - [SMTheming Wiki](http://kki.ajworld.net/wiki/Main_Page)

### 日本国内における主なパッケージサイト

  - [Vocalosteps](http://vocalosteps.a-zeroproduce.net/)
  - [CyberiaStyle](http://cyberiastyle.skr.jp/)
  - [foonmix](http://foonmix.nothing.sh/)
  - [D3MIX](http://d3nex.a-zeroproduce.net/)
  - [XXmiX](http://www.bit-symphony.net/)
  - [pop☆candy](http://dee.manbow.org/popcandy/)
  - [Panzer Force](http://panzerforce.ath.cx/)
  - [Y.W MIX](http://www.yw-works.com/ywmix/)

[Category:音楽ゲーム](https://ja.wikipedia.org/wiki/Category:音楽ゲーム "wikilink") [Category:Linux用ゲームソフト](https://ja.wikipedia.org/wiki/Category:Linux用ゲームソフト "wikilink") [Category:Macintosh用ゲームソフト](https://ja.wikipedia.org/wiki/Category:Macintosh用ゲームソフト "wikilink") [Category:Windows用ゲームソフト](https://ja.wikipedia.org/wiki/Category:Windows用ゲームソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:ゲームエンジン](https://ja.wikipedia.org/wiki/Category:ゲームエンジン "wikilink") [Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:アセンブリ言語](https://ja.wikipedia.org/wiki/Category:アセンブリ言語 "wikilink")

1.  \[[http://www.stepmania.com/wiki/StepMania_4.0\]4.0ダウンロードページのNote参照](http://www.stepmania.com/wiki/StepMania_4.0%5D4.0ダウンロードページのNote参照)。