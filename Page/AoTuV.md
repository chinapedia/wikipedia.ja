> この記事は[AoTuV](https://ja.wikipedia.org/wiki/AoTuV)から翻訳されています。


**aoTuV** (AOyumi TUned Vorbis)は、[オープンソース](../Page/オープンソース.md "wikilink")の[Vorbis互換](https://ja.wikipedia.org/wiki/Ogg_Vorbis "wikilink")[エンコーダ](../Page/エンコード.md "wikilink")。一部からは蒼粒、青粒などと呼ばれている。

## 概要

チューニング・開発・配布は[日本人](https://ja.wikipedia.org/wiki/日本人 "wikilink")の[蒼弓](https://aynote.wordpress.com/)が行っている。[2019年](../Page/2019年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")現在、バージョンはBeta6.03 (2018)。

Vorbisは規格自体がオープンソースかつ[パテントフリーであるため](https://ja.wikipedia.org/wiki/ソフトウェア特許 "wikilink")、数多くのエンコーダが開発されているが、その中でもaoTuVはもっとも高い音質のVorbisを作成できるとされている。
また、Vorbisをq-2(32kbps)でエンコードできるのも、aoTuVの特徴である。
Hydrogenaudio主催による数々の公開リスニングテストで、aoTuVは高い評価を受けている。

### aoTuVの発展

Vorbis の公式エンコーダのバージョンが 1.0.1 の頃、[MP3](../Page/MP3.md "wikilink")を越えることを目指して開発された Vorbis ではあったが、音質評価は必ずしも賞賛ばかりではなかった。 当時の公式エンコーダにはプリエコー（pre echo）と高域ブースト（HF boost）が発生する問題があり、それが音質低下の主たる要因であった。この問題を解決しようと、有志によってチューニングされたエンコーダが幾つか登場した。 aoTuV以前の主なチューニング版には GT3・QKTune・Modest Tuning 等がある。 このうちGT3 はプリエコーを軽減したのが特徴で、主に高いビットレートで効果を発揮した。しかし、公式エンコーダや他のチューニング版に比べビットレートが膨らむ傾向にあるのが難点であった。 QKTune は高域ブーストの軽減を図っており、主に平均的なビットレートで効果を発揮した。

#### aoTuV alpha 1

Vorbisの高音質化を目指したチューニング版の一つとして、蒼弓による aoTuV が登場したのは2003年12月23日であった。 aoTuV は細かい部分の調整が主で、比較的低いビットレートに重点を置いて調整しているのが特徴である。 また、q-2 に対応しているのも特徴であり、平均約 40kbps でエンコードすることができた。 一方で、プリエコー・高域ブースト対策で他より遅れを取っていたため、中～高ビットレートでは他より優位とはいかなかった。 そのため Vorbis ユーザーの間では、低ビットレートは aoTuV、q5までは公式エンコーダ、q6以上はGT3、と使い分けることが推奨された。 各チューニング版を合成して、それぞれの良さを合わせる試みも幾つかあったが、各チューニング版のトレードオフも改善されないまま合わさってしまうこともあって大きな成果にはならなかった。

#### aoTuV experiment \[20040329\]

2004年3月29日、蒼弓は aoTuV に大きな改良を加え、その開発版を公開した。 このバージョンはどのビットレートにおいてもプリエコーと高域ブーストを非常に良く軽減していて評判となった（高ビットレートではまだ GT3 が有利な面もあるにはあったが）。

低ビットレートにおいては、このバージョン以降は他のチューニング版の追随を許さなくなった。 高ビットレートは、まだ少し不得意であったがこれ以降のバージョンで改良されていくこととなる。

#### aoTuV beta 2

開発版での改良を反映した正式版は2004年4月21日に公開され、以降、Hydrogenaudio主催の公開リスニングテストで高評価を得ることになる。 この高評価を受け、海外などで aoTuV を内部に取り込んだツール類が公開されるようになる。 また、aoTuV beta 2 による改良点はほとんどが公式エンコーダにも取り込まれ、libvorbisバージョン 1.1 として公開された。

#### aoTuV beta 3

2004年11月21日に公開。公式エンコーダのバージョンアップに伴い、aoTuV もチューニングのベースとする公式エンコーダを libvorbis 1.1 に変更した。 このバージョンではq-2 の仕様が変更され、より低い平均 32kbps でエンコードできるようになった。 これは当初は q-3 と呼ばれていたものである。

#### aoTuV beta 4

2005年6月18日公開。チャンネル間処理に大きな改良を施した。 Vorbis のチャンネル間処理は効率を増す一方で高域ブーストの原因の一つとなっていた所でもある。 beta 4 が公開されてから少し経った6月27日、公式エンコーダも libvorbis 1.1.1 にバージョンアップした。 libvorbis 1.1 から libvorbis 1.1.1 にかけての変更点はいくつかのバグの修正である。 7月7日、既に公開されていた aoTuV beta 4 はこれらのバグ修正を取り込んだものに差し替えられた。 そのため、同じ beta 4 でも内容が異なるエンコーダが存在する。

#### aoTuV beta 4.5

2005年11月5日公開。beta3の弱音処理コードが書き換えられた。 beta 4 から beta 4.5 にかけての改良は q3 未満を対象としたもので、q3 以上の場合は beta 4 とほぼ同等の結果をもたらす。

#### aoTuV beta 4.51

2005年11月19日公開。GCC4でコンパイルした際に正常に動作しないコードを出力する問題が修正された。 当時、公式エンコーダも同じ問題を持っており libvorbis 1.1.2 で修正された。

#### aoTuV Release 1

2006年8月23日公開。beta 4.51 を改名して安定版としたものである。 β版を避けるユーザーのために用意された。

#### aoTuV beta 5

2006年10月24日公開。いくつかの改良により、低いビットレートでの音荒れ、音揺れ問題、Channel Couplingに起因する問題の幾つか、プリエコーを改善した。 また、変更点や追加部分に合わせて、各部のチューニングをやり直したバージョンである。 公式エンコーダの libvorbis 1.1.2 までの改良も取り込まれている。 Release 1 が公開される以前から開発されていたものである。 11月5日、[svn.xiph.org](https://ja.wikipedia.org/wiki/Xiph.Org_Foundation "wikilink") に aoTuV 用のブランチが作成された。 これは、aoTuV の開発が公式のプロジェクトとして認められたことを意味する。 aoTuV が公式エンコーダに取り込まれたわけではないが事実上の公式エンコーダになる可能性は高くなった。

#### aoTuV beta 5.5

ユーザーの要望に応える形で、2008年3月31日、約1年半の沈黙を破ってのリリース。 プリエコーをさらに改善し、細部の挙動を beta 5 よりも改良した。

#### aoTuV beta 5.6

#### aoTuV beta 5.61

#### aoTuV beta 5.7

#### aoTuV beta 6

#### aoTuV beta 6.01

#### aoTuV beta 6.02

libvorbis1.2.2～1.3.2の修正を取り込み、特定パターンのプリ/ポストエコーを改善、ステレオモード切替のしきい値を変更、 Noise normalization処理の改善など小粒ながらも比較的広きに渡る修正が行われているが、公開初日に「特定の波形が破綻する」という不具合が発覚している。

#### aoTuV beta 6.03

5.1chソースのエンコードに関する問題を修正。
libvorbis 1.3.4を統合(2014)。

libvorbis 1.3.5を統合(2015)。

libvorbis 1.3.6を統合(2018)。

## aoTuVの履歴

  - 2003年12月23日 aoTuV alpha 1 (q-2 に対応、40kbps)
  - 2004年1月1日 aoTuV alpha 2
  - 2004年1月31日 aoTuV alpha 3
  - 2004年2月15日 aoTuV beta 1
  - 2004年2月27日 aoTuV beta 1_a
  - 2004年3月29日 ※aoTuV experiment \[20040329\] (プリエコー・高域ブーストをほぼ解消)

<!-- end list -->

  - 2004年4月21日 aoTuV beta 2

<!-- end list -->

  - 2004年11月21日 aoTuV beta 3 (q-2 の変更、32kbps)

<!-- end list -->

  - 2005年6月18日 aoTuV beta 4
  - 2005年7月7日 aoTuV beta 4
  - 2005年11月5日 aoTuV beta 4.5
  - 2005年11月19日 aoTuV beta 4.51

<!-- end list -->

  - 2006年8月23日 aoTuV Release 1 (初の安定版、beta 4.51 を改名したもの)
  - 2006年10月24日 aoTuV beta 5
  - 2008年3月31日 aoTuV beta 5.5
  - 2008年12月10日 aoTuV beta 5.6
  - 2008年12月16日 aoTuV beta 5.61
  - 2009年3月3日 aoTuV beta 5.7
  - 2011年2月22日 aoTuV beta 6
  - 2011年2月23日 aoTuV beta 6.01
  - 2011年2月27日 aoTuV beta 6.02
  - 2011年4月25日 aoTuV beta 6.03
  - 2014年5月11日 aoTuV beta 6.03 (2014)
  - 2015年8月10日 aoTuV beta 6.03 (2015)
  - 2018年5月2日 aoTuV beta 6.03 (2018)

※aoTuV experiment \[20040329\] は開発版であるが、aoTuV の現在の高い評価につながる重要な改良が行われたバージョンであるため掲載した。

## 関連項目

  - [MP3](../Page/MP3.md "wikilink")
  - [LAME](https://ja.wikipedia.org/wiki/LAME "wikilink")

## 外部リンク

### 参考ページ

  - [2005年7月開催の80kbpsにおけるリスニングテスト](http://www.hydrogenaudio.org/forums/index.php?showtopic=35438)　aoTuV1位
  - [2005年8月開催の180kbpsにおけるリスニングテスト](http://www.hydrogenaudio.org/forums/index.php?showtopic=36465)　aoTuV1位

### 関連サイト

  - [aoTuV公式ページ](https://ao-yumi.github.io/aotuv_web/index.html)

[en:AoTuV](https://ja.wikipedia.org/wiki/en:AoTuV "wikilink")

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink")