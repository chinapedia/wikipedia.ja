> この記事は[Theora](https://ja.wikipedia.org/wiki/Theora)から翻訳されています。


**Theora** (セオラ、シオラ) は、[オープンな](../Page/オープンフォーマット.md "wikilink")[非可逆の](../Page/非可逆圧縮.md "wikilink")[動画](../Page/動画.md "wikilink")[圧縮](../Page/データ圧縮.md "wikilink")[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")、または、その[コーデック](../Page/コーデック.md "wikilink")である。[オープンな](../Page/オープンフォーマット.md "wikilink")[音声ファイルフォーマット](../Page/音声ファイルフォーマット.md "wikilink")である [Vorbis](../Page/Vorbis.md "wikilink") の開発元として知られる [Xiph.org](https://ja.wikipedia.org/wiki/Xiph.Org_Foundation "wikilink") が[VP3](https://ja.wikipedia.org/wiki/VP3 "wikilink")を基にして開発した。

## 概要

TheoraはOn2のVP3を基とした[後方互換のフォーマットである](../Page/互換性.md "wikilink")。ただし、ファイルフォーマットレベルでの互換性は無い。[Ogg](../Page/Ogg.md "wikilink")[コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")の標準ビデオコーデックとして利用され(同時に音声には通常[Vorbis](../Page/Vorbis.md "wikilink")が使われる)、**Ogg Theora**と呼称されることもある。 仕様とその標準的な実装であるlibtheoraは[オープンソース](../Page/オープンソース.md "wikilink")で提供される ([BSDライセンス](../Page/BSDライセンス.md "wikilink")、ロイヤリティフリー)。

## 動向

フォーマットは2004年8月、libtheora1.0 Alpha 3リリース時に凍結され、2008年11月に正式に1.0として安定版の参照ライブラリlibtheora 1.0がリリースされた。 長い間エンコーダ部分の改善は行われなかったが、1.0のリリースにおいて開発元のXiph.orgはエンコード品質を大きく改善するという新しいエンコーダ“Thusnelda” (Theora 1.1) が2009年9月24日にリリースされた。 [FFmpeg](../Page/FFmpeg.md "wikilink")のコアライブラリである[libavcodec](https://ja.wikipedia.org/wiki/libavcodec "wikilink")でも限定的ではあるがTheoraの開発が進んでいる。

## 特徴

  - ブロック単位の動き補償
  - 8x8 Type-II [離散コサイン変換](../Page/離散コサイン変換.md "wikilink")
  - 品質ベースエンコード (VBR)
  - 適応インループフィルター (deblocking)
  - 最小8x8のマクロブロック
  - 量子化行列のカスタマイズ (intra/inter, luma/chroma)
  - フレキシブルな[エントロピー符号](https://ja.wikipedia.org/wiki/エントロピー符号 "wikilink") (1フレームあたり80個のVLC tables)
  - YUV4:2:0に加えYUV4:2:2、YUV4:4:4のピクセルフォーマット
  - 8bitのカラーチャンネル
  - 複数のreference frames
  - 非正方ピクセル (ピクセル[アスペクト比](../Page/アスペクト比.md "wikilink")) のサポート
  - 16の倍数ではない解像度 (現在は8x8以上のフレーム) をサポート
  - 量子化値の非線形スケーリング
  - ブロック単位までの適応量子化
  - ストリームは[Iフレーム](https://ja.wikipedia.org/wiki/Iフレーム "wikilink")と[Pフレーム](https://ja.wikipedia.org/wiki/Pフレーム "wikilink")によって構成され[Bフレーム](https://ja.wikipedia.org/wiki/Bフレーム "wikilink")はサポートしない
  - 1/2画素精度の[動き補償](../Page/フレーム間予測.md "wikilink")
  - [Ogg](../Page/Ogg.md "wikilink")のほか、[AVI](../Page/Audio_Video_Interleave.md "wikilink")、[Matroska](../Page/Matroska.md "wikilink")、[Ogg Media等のコンテナ形式に対応](../Page/Ogg_Media.md "wikilink")

## 利用例

  - ウェブブラウザ上での動画再生。
  - コンピュータゲームでの動画。

## HTML5への策定をめぐる議論

特許上の懸念が少なくフリーで利用できるTheoraは、[HTML5](../Page/HTML5.md "wikilink")における標準動画コーデック候補として[Mozilla Foundationや](../Page/Mozilla_Foundation.md "wikilink")[オペラ・ソフトウェア](https://ja.wikipedia.org/wiki/オペラ・ソフトウェア "wikilink")などから支持されていたが、[アップルや](../Page/アップル_\(企業\).md "wikilink")[ノキア](../Page/ノキア.md "wikilink")などの反対により撤回された。また[Google](../Page/Google.md "wikilink")も、[H.264 AVCなどのより新しい圧縮コーデックと比べて圧縮率で劣るTheoraは](../Page/H.264.md "wikilink")/MPEG4[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")で使用できる水準に満たないと考えている\[1\]。一方で、たとえばXiph.orgのGreg Maxwellは独自に行った同一ファイルサイズでの比較検証において、Theoraは画質でも圧縮効率でもH.264より優れているものと主張している\[2\]。

2009年8月現在でTheoraはすでに[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")、[Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink") ([Chromium](https://ja.wikipedia.org/wiki/Chromium "wikilink")) などの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")でサポートされていて、

<video>

タグを用いることで[プラグイン](../Page/プラグイン.md "wikilink")なしに再生が可能である\[3\]。

## コンテナ形式と拡張子

通常はOgg[コンテナに格納され](../Page/コンテナフォーマット.md "wikilink")、ファイルの拡張子は.ogvとなる。音声コーデックはVorbisが使われる。 従来のビデオコーデック同様に[DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")を利用したコンテナ形式 (AVI、MKV等) に格納することも可能だがあまり使われることはない。

  - (Theora+Vorbis).ogv

注: (Theora+Vorbis).ogg

  -
    拡張子.oggは非推奨となったため、現在は拡張子.ogvが使われる。

## 脚注

<references />

## 関連項目

  - [Ogg](../Page/Ogg.md "wikilink")
  - [Vorbis](../Page/Vorbis.md "wikilink")
  - [WebM](https://ja.wikipedia.org/wiki/WebM "wikilink")
  - [ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")
  - [オープンソースのコーデックとコンテナフォーマット一覧](../Page/オープンソースのコーデックとコンテナフォーマット一覧.md "wikilink")
  - [動画編集ソフトウェア](https://ja.wikipedia.org/wiki/動画編集ソフトウェア "wikilink")
  - [Icecast](https://ja.wikipedia.org/wiki/Icecast "wikilink")

## 外部リンク

  - [Xiph.Org](http://www.xiph.org/)
  - [Theora.Org](http://www.theora.org/)
  - [ffmpeg2theora](http://www.v2v.cc/~j/ffmpeg2theora/)
  - [illiminable Ogg Directshow Filters for Speex, Vorbis, Theora and FLAC](http://www.illiminable.com/ogg/)
  - [Jheora Cortado](http://www.flumotion.net/cortado/) Java用

[Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Xiph.Org](https://ja.wikipedia.org/wiki/Category:Xiph.Org "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.  [HTML 5 drops open-source video codec](http://news.zdnet.co.uk/internet/0,1000000097,39670329,00.htm), ZDNet UK
2.  [YouTube / Ogg/Theora comparison](http://people.xiph.org/~greg/video/ytcompare/comparison.html), Xiph.Org
3.  [グーグルがOn2買収、videoタグの膠着状態に終止符か](http://www.atmarkit.co.jp/news/200908/06/on2.html), @IT