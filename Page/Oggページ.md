> この記事は[Ogg](https://ja.wikipedia.org/wiki/Ogg)から翻訳されています。


**Oggページ**は [Ogg](https://ja.wikipedia.org/wiki/Ogg "wikilink") [ビットストリーム](https://ja.wikipedia.org/wiki/ビットストリーム "wikilink")に含まれるデータのサイズ可変なユニットである。

## 概要

複数の[コーデック](../Page/コーデック.md "wikilink")を単一のファイルまたはストリームにまとめる(mux)のが[マルチメディア](../Page/マルチメディア.md "wikilink")[コンテナフォーマット](https://ja.wikipedia.org/wiki/コンテナフォーマット "wikilink")の目的の一つである。

Oggフォーマットを作った Christopher Montgomery が持つ視点は、「muxed codec dataはコーデックによって使用されるデータのユニットから分離された抽象的なレイヤーであるべきで、それはデコードの際に必要となるバッファの量を制限するためだ」というものである。彼の意見は[Xiph.org Foundationで働く他の開発者にも支持されており](https://ja.wikipedia.org/wiki/Xiph.org_Foundation "wikilink")、このことは [AVI](https://ja.wikipedia.org/wiki/AVI "wikilink"),[QuickTime](../Page/QuickTime.md "wikilink"),[MPEG](https://ja.wikipedia.org/wiki/MPEG "wikilink")のような他のフォーマットと比べて技術的な長所であるとのこと。

各 Oggページはデータのタイムオフセットを持っていて、 これにより[ストリーミング](../Page/ストリーミング.md "wikilink")時の効果的な[シーク](https://ja.wikipedia.org/wiki/シーク "wikilink")が可能になり時間的な正確性が得られる。その他のフォーマットでは対照的に、シーク情報を得るためにストリームのバイト位置をシークするか、もしくはTOCを信頼する方法を使う。

## 構造

すべての Oggページは4[バイトのmagic](../Page/バイト_\(情報\).md "wikilink")「OggS（4F 67 67 53）」で始まる。同期を見失った場合、デコーダはデコード再開のため、次に出現するOggSを探すことができる。この文字列の次にはOgg version 0を示すnull byteが続く。 2004年の時点ではOggの公式バージョンはこれのみであり、より新しいバージョンの計画はない。

次のバイトではtype flagsを指定する。

`1`
`   データは最後のページから続けられる `
`2`
`   ストリームの最初のページである `
`4`
`   ストリームの最後のページである `

これらの値は addition または OR によって結合される。

次の 8バイト（または 64ビット）は absolute granule position と呼ばれ、そのページからデコードされるデータの時間オフセットを指定している。この数が意味するものはビデオコーデックにより異なるが、しばしば動画データの[サンプル](https://ja.wikipedia.org/wiki/サンプル "wikilink")や[フレームを参照する](../Page/コマ_\(映画・漫画\).md "wikilink")。[Theora](https://ja.wikipedia.org/wiki/Theora "wikilink")のように、このフィールドをキーフレームと中間フレーム(interframes)に分離して使っているコーデックもある。

次の4バイトはこのページが属するstream serial numberであり、その次の4バイトはストリーム内のpage sequence numberである。

次の（23バイト目から始まる）4バイトはページの[CRC](../Page/巡回冗長検査.md "wikilink")[チェックサム](../Page/チェックサム.md "wikilink")である。このフィールドの値は変化するため、このフィールドをゼロとしてチェックの結果が算出される。

27バイト目は0～255の値を取り、含まれているセグメント数を指定する。これは次に続くセグメントテーブルのサイズでもあり、単位はバイトである。セグメントテーブルの各バイトはセグメントの長さを示す。各セグメントは長さにおいて 255バイトまでの長さを取り得、ページによって結束される。

`segment ＜ 255 の場合`
`   パケットの終りを示し、次のセグメントは新しいパケットを始める。`
`パケットが255の倍数で終わった場合`
`   0バイトの長さのセグメント内で終わるだろう `
`そのページの最後のセグメントが 255バイトの場合`
`   最後のパケットは次のページに続く`

## 外部リンク

  - [Ogg Page Structure](http://www.xiph.org/ogg/vorbis/doc/framing.html)

[Category:Xiph.Org](https://ja.wikipedia.org/wiki/Category:Xiph.Org "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink")