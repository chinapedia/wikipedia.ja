> この記事は[Max \(\)](https://ja.wikipedia.org/wiki/Max_\(\))から翻訳されています。


**Max**（マックス）は、[サンフランシスコ](../Page/サンフランシスコ.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")企業[Cycling '74が開発](https://ja.wikipedia.org/wiki/Cycling_'74 "wikilink")・保守している[音楽](../Page/音楽.md "wikilink")と[マルチメディア](../Page/マルチメディア.md "wikilink")向けのグラフィカルな[統合開発環境](../Page/統合開発環境.md "wikilink")（[ビジュアルプログラミング言語](../Page/ビジュアルプログラミング言語.md "wikilink")）である。[作曲家](../Page/作曲家.md "wikilink")や[メディアアーティストらに](../Page/メディアアート.md "wikilink")20年以上使われ続けている。

## Max/MSP

バージョン4までは[DSPの追加機能を備えた](https://ja.wikipedia.org/wiki/デジタルサウンドプロセッサ "wikilink")**Max/MSP**（マックス・エムエスピー）という名で発売されており、それに追加モジュールとして[映像](https://ja.wikipedia.org/wiki/映像 "wikilink")を取り扱う**Jitter**（ジッター）が別売りで販売されていた。

バージョン5からは全てのMaxにJitterが含まれ、MaxとMSPとJitterは一つのパッケージとして販売されるようになった。これにより名称は再び**Max**に戻った。

## モジュール化

Maxは非常に[モジュール](../Page/モジュール.md "wikilink")性が高く、ほとんどの[ルーチンは](../Page/サブルーチン.md "wikilink")[共有ライブラリの形で存在している](../Page/ライブラリ.md "wikilink")。[APIによって](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[サードパーティー](../Page/サードパーティー.md "wikilink")が（external objectsと呼ばれる）新たなルーチンを開発可能である。結果として、多くのMaxユーザーが商用か否かに関わらず、拡張を行っている。[拡張性](../Page/拡張性.md "wikilink")とグラフィカルな[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")により、Maxはインタラクティブな音楽パフォーマンスソフトウェア開発における共通言語ともいうべき存在になっている。

## 歴史

Maxのオリジナル作成者は[ミラー・パケット](https://ja.wikipedia.org/wiki/ミラー・パケット "wikilink") (Miller S. Puckette) であり、[1988年](../Page/1988年.md "wikilink")に[IRCAM](../Page/IRCAM.md "wikilink")で作曲家がインタラクティブな[デスクトップミュージック](../Page/デスクトップミュージック.md "wikilink")制作システムにアクセスできるように、[ピアノ](../Page/ピアノ.md "wikilink")と[コンピュータ](../Page/コンピュータ.md "wikilink")を組み合わせた*Sogitec 4X*というシステムのためのエディタ*Patcher*として作られた\[1\]。

[1989年](../Page/1989年.md "wikilink")、IRCAMはMaxの並行処理版を開発し、[NeXT](../Page/NeXT.md "wikilink")に[IRCAM Signal Processing Workstationを接続したもので動作するよう移植した](https://ja.wikipedia.org/wiki/:en:ISPW "wikilink")（後に[SGIのマシンや](../Page/シリコングラフィックス.md "wikilink")[Linux](../Page/Linux.md "wikilink")にも移植された）。これを Max/FTS (Faster Than Sound) と呼んだ\[2\]\[3\]。

1989年、Maxは[Opcode Systemsに](../Page/Opcode.md "wikilink")[ライセンス](../Page/ライセンス.md "wikilink")供与され、同社は[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")にMax/Opcodeという商用版を販売したが、売れ行きは芳しくなく、数年後に他社に売却されている。現在の商用版Maxは[1999年](../Page/1999年.md "wikilink")から、Max/Opcodeでの拡張を行ったDavid Zicarelliが[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に設立\[4\]したCycling '74によって販売されている。

Maxにはいくつかの拡張があり、特に[Pure Dataから](../Page/Pure_Data.md "wikilink")1997年に移植された音響拡張セットが有名である。これを**MSP**（Max Signal ProcessingまたはMiller S. Pucketteの略）と呼び、このアドインパッケージをMaxに追加することでデジタル音声信号をリアルタイムで操作可能となり、ユーザーが独自のシンセサイザーやエフェクトプロセッサを作ることが可能となる。それ以前のMaxはハードウェアシンセサイザーやサンプラーなどへのインタフェースとして設計されていて、[MIDI](../Page/MIDI.md "wikilink")その他のプロトコルを制御する言語だった。現在は全てのMaxにMSP機能がバンドルされている。

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")、Max/FTS の後継が[Java](https://ja.wikipedia.org/wiki/Java "wikilink")を使って開発され ([jMax](https://ja.wikipedia.org/wiki/jMax "wikilink"))、[オープンソース](../Page/オープンソース.md "wikilink")としてリリースされた。

1999年、Maxでビデオのリアルタイム制御を可能とする拡張である**nato.0+55**がリリースされた。これは、謎の多いネット上の存在である[Netochka Nezvanovaが開発して配布したものだが](https://ja.wikipedia.org/wiki/Netochka_Nezvanova "wikilink")、マルチメディアアーティストの間で人気となった。

同じころ、Cycling '74も正式なビデオ制御実装を開発した。[2003年](../Page/2003年.md "wikilink")にリリースされた**Jitter**というパッケージは、リアルタイムのビデオ/3次元/[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")処理機能を提供するものである。これもバージョン5から全てのMaxにバンドルされている。

## 競合ソフトウェア

  - [Native Instrumentsの](../Page/Native_Instruments.md "wikilink")[Reaktor](../Page/Reaktor.md "wikilink")は、シンセサイザーの構築に特化しているため、その目的であればMaxよりも理解しやすい。ただし拡張性は劣る。
  - [アップルの](../Page/アップル_\(企業\).md "wikilink")[Quartz Composerもパッチ型プログラミングという共通点がある](https://ja.wikipedia.org/wiki/Quartz_Composer "wikilink")。
  - [Pure Data](../Page/Pure_Data.md "wikilink") - オリジナルの開発者ミラー・パケットによる[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")プログラムで、[1996年](../Page/1996年.md "wikilink")にリリースされた。完全に設計し直したものであり、DSPによる信号処理への支援が無いなど、基本的な点でMaxのオリジナルと異なる部分があるが、多くの部分で似ており、Maxを擬似的に代替可能なものとなっている。
  - [OpenMusic](https://ja.wikipedia.org/wiki/OpenMusic "wikilink") - MAXと同様IRCAMにおいて開発されたオブジェクト指向プログラミング音楽用言語。Maxが主に演奏行為におけるリアルタイム処理を目的とした使い方に適しているのに対し、OpenMusicはあらかじめ準備しておいた楽譜（[MIDI](../Page/MIDI.md "wikilink")データまたは[Finale](../Page/Finale.md "wikilink")用フォーマット）やサウンドファイルの出力に適している。[SDIF](https://ja.wikipedia.org/wiki/SDIF "wikilink")フォーマットに対応しており、Maxをはじめとする様々なソフトウェアとのデータのやり取りも充実している。
  - [Ableton Live](../Page/Ableton_Live.md "wikilink") - ライブパフォーマンス、タイムラインベースの制作に強い。Cycling '74とAbletonの共同開発により、2009年、[MAX for Liveがリリースされた](https://ja.wikipedia.org/wiki/MAX_for_Live "wikilink")。

## その他

Maxの名称は、MAXの先祖に当たる世界初の音楽プログラミング言語[MUSICを開発した](https://ja.wikipedia.org/wiki/MUSIC-N "wikilink")[マックス・マシューズ](https://ja.wikipedia.org/wiki/マックス・マシューズ "wikilink")に由来する。Maxで開発したプログラムは実行環境と共にスタンドアロンのアプリケーションとすることができ、商用でもフリーでも自由に配布可能である。また、Maxは他のシステムで[VST](https://ja.wikipedia.org/wiki/VST "wikilink")などの[プラグイン](../Page/プラグイン.md "wikilink")として使うこともできる。

ライブの音楽パフォーマンスで[ノートパソコン](../Page/ノートパソコン.md "wikilink")が使われることが多くなり、Maxが開発環境として使われることも多くなっている。

## Maxを利用する主なアーティスト

  - [秋田昌美](../Page/秋田昌美.md "wikilink")
  - [リチャード・D・ジェームス](https://ja.wikipedia.org/wiki/エイフェックス・ツイン "wikilink")
  - [オウテカ](../Page/オウテカ.md "wikilink")
  - [高橋悠治](../Page/高橋悠治.md "wikilink")
  - [坂本龍一](../Page/坂本龍一.md "wikilink")
  - [佐近田展康](https://ja.wikipedia.org/wiki/佐近田展康 "wikilink")
  - [ジョニー・グリーンウッド](../Page/ジョニー・グリーンウッド.md "wikilink")（[レディオヘッド](https://ja.wikipedia.org/wiki/レディオヘッド "wikilink")）
  - [竹村延和](../Page/竹村延和.md "wikilink")
  - [ポーリン・オリヴェロス](https://ja.wikipedia.org/wiki/ポーリン・オリヴェロス "wikilink")
  - [青木孝允](../Page/青木孝允.md "wikilink")
  - [ヤン富田](https://ja.wikipedia.org/wiki/ヤン富田 "wikilink")

IRCAMに関係する作曲家は、アシスタント技術士の支援を得てMaxによる電子音響を自作に応用することが多い。古くは[ピエール・ブーレーズ](../Page/ピエール・ブーレーズ.md "wikilink")が[4X](https://ja.wikipedia.org/wiki/4X "wikilink")コンピュータを用いて近年の代表作「レポン」などを作曲したが、この4Xコンピュータの制御に用いるために開発されたのが最初期のMaxである。「レポン」の制御プログラムは現在のMaxシステムにも移植され、最近の演奏会にて用いられている。他にも[カイヤ・サーリアホ](../Page/カイヤ・サーリアホ.md "wikilink")、[ジョナサン・ハーヴェイなどといった作曲家による電子音響を用いた作品にも用いられており](https://ja.wikipedia.org/wiki/ジョナサン・ハーヴィ_\(作曲家\) "wikilink")、そのための開発準備はIRCAMの各スタジオにて行われている。またIRCAMでは1ヶ月および1年間（[2007年](../Page/2007年.md "wikilink")度以降は2年間）の研究員制度を設けており、公募によって選ばれた数名の若手作曲家は初歩からMaxおよびその他のソフトウェアを学び、1年後にはそれらを自らプログラミングして自作発表の演奏会に用いている。

## 関連項目

  - [Pure Data](../Page/Pure_Data.md "wikilink")
  - [Jeskola Buzz](https://ja.wikipedia.org/wiki/Jeskola_Buzz "wikilink")
  - [Ableton Live](../Page/Ableton_Live.md "wikilink")

## 脚注

## 外部リンク

  - [Home Page of Cycling '74](http://www.cycling74.com)
  - [RTC-lib](http://www.essl.at/works/rtc.html) Max/MSP/Jitter でのアルゴリズム的合成のためのソフトウェアライブラリ
  - [Pd Home Page](http://puredata.info/)
  - [jMax project page](http://sourceforge.net/projects/jmax/) on [SourceForge.net](../Page/SourceForge.net.md "wikilink")
  - [AE Max/MSP patches and Powmod patch library](http://web.archive.org/web/20070927210930/http://www.recordlabelrecords.org/maxmsp.html)
  - [Max Objects Database](http://www.maxobjects.com/)
  - [Studiotoolz\!](http://www.studiotoolz.net/)
  - [日本輸入代理店エムアイセブンジャパン｜Cycling '74日本語ポータルサイト](http://www.mi7.co.jp/products/cycling74/)
  - [David Zicarelli｜Max開発者インタビュー](http://www.mi7.co.jp/story/david.zicarelli.php)

[Category:音声処理ソフト](https://ja.wikipedia.org/wiki/Category:音声処理ソフト "wikilink") [Category:コンピュータミュージック](https://ja.wikipedia.org/wiki/Category:コンピュータミュージック "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:ソフトウェア・シンセサイザー](https://ja.wikipedia.org/wiki/Category:ソフトウェア・シンセサイザー "wikilink") [Category:音楽ソフトウェア](https://ja.wikipedia.org/wiki/Category:音楽ソフトウェア "wikilink") [Category:VJ](https://ja.wikipedia.org/wiki/Category:VJ "wikilink") [Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink") [Category:1988年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1988年のソフトウェア "wikilink")

1.  [Explanatory notes: Pluton](http://www-crca.ucsd.edu/~msp/pdrp/latest/files/manoury-pluton/doc/history.htm)
2.  [A brief history of MAX](http://freesoftware.ircam.fr/article.php3?id_article=5) (with a block diagram of variant history)
3.  [Max/MSP History and Background — Where did MaxMSP come from?](http://www.cycling74.com/twiki/bin/view/FAQs/MaxMSPHistory#Where_did_MaxMSP_come_from)
4.  [Cycling '74 About Us](http://www.cycling74.com/special/aboutus)