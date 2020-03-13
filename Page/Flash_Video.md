> この記事は[Flash Video](https://ja.wikipedia.org/wiki/Flash_Video)から翻訳されています。


**Flash Video**（**フラッシュ ビデオ**）は、主に[Flash Player](https://ja.wikipedia.org/wiki/Flash_Player "wikilink") 6以降を利用してインターネット上で動画を配信するために利用される[コンテナ型のファイルフォーマットで](../Page/コンテナフォーマット.md "wikilink")、元は[マクロメディア](../Page/マクロメディア.md "wikilink")が開発していたものを、[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")が会社ごと買収した。Flash VideoはSWFファイルの内部に埋め込まれる場合もある。なお、アドビシステムズによって定義され、Flash Playerが対応している動画ファイルフォーマットには異なる「FLV」と「F4V」の2つが存在する。FLVファイル内の動画および音声のデータはSWFファイルと同じ方法で[エンコード](../Page/エンコード.md "wikilink")される。後者のF4VファイルフォーマットはISOベースのメディアファイルフォーマットを基にしており、これはFlash Player 9の「update 3」以降で対応を開始した。

Flash Videoフォーマットは[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")や[Googleビデオ](https://ja.wikipedia.org/wiki/Googleビデオ "wikilink")、Yahoo\! Video、[ロイター](../Page/ロイター.md "wikilink")を始めとした多くのニュース提供元などで次々に採用され、Web上における埋め込み動画の形式として、すぐにその地位を確立した。Adobe Flashの終了に伴い、現在は推奨されていない。

Flash Videoコンテナフォーマットそのものが開かれる際に利用される圧縮形式のほとんどは、特許によって保護されており、一般にはSorenson Sparkまたは[VP6コーデックによって映像データがエンコードされている](https://ja.wikipedia.org/wiki/On2_VP6 "wikilink")。最新のFlash Playerでは[H.264](../Page/H.264.md "wikilink")の映像と[HE-AAC](../Page/HE-AAC.md "wikilink")の音声にも対応している。

Flash Videoは広範囲で利用可能なFlash Playerと[Webブラウザの](../Page/ウェブブラウザ.md "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")や、[サードパーティー](../Page/サードパーティー.md "wikilink")によるプログラム等を通じて、ほとんどの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で観ることができる。作成には、[FFmpeg](../Page/FFmpeg.md "wikilink")などを使う。

## 特徴

[Adobe Flash](../Page/Adobe_Flash.md "wikilink")（旧Macromedia Flash）ではFlash Videoを他のメディアタイプと同様に扱うことができ、ファイル内の他のオブジェクトと同様に重ね合わせ、スクリプト処理、制御を行うことができる。現在[リッチコンテンツ](https://ja.wikipedia.org/wiki/リッチコンテンツ "wikilink")の主流であるFlash上で再生・表示できることが大きな特長である。

## 影響

[HTML上における動画表現はFlash](../Page/HyperText_Markup_Language.md "wikilink") Videoの普及以前、[Windows Media Videoや](../Page/Windows_Media_Video.md "wikilink")[QuickTime](../Page/QuickTime.md "wikilink")ムービーが存在していたが、ユーザーはファイルのコーデック毎にプラグインやプレーヤーのインストールが必要だった。

Flash MX（バージョン6）から**Flash Video**（Sorenson [H.263](../Page/H.263.md "wikilink")の調整版）がサポートされた。これにより従来の[テキスト](../Page/テキスト.md "wikilink")と[静止画](https://ja.wikipedia.org/wiki/静止画 "wikilink")ベースであったインターネットインフラが動画ベースへとシフトし、[Webの表現方法が革新される一因となった](../Page/World_Wide_Web.md "wikilink")。[2004年](../Page/2004年.md "wikilink")以降、[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")や[ニコニコ動画](../Page/ニコニコ動画.md "wikilink")などの大手動画投稿サイトでこの技術が採用されており、インターネット上での動画再生のインフラ構築にも大きく貢献をした。2018年現在、アドビはFlashからHTML5への移行を進めており、Flash Videoは推奨されていない。

## 仕様

FLVファイルフォーマットはFlash MX (Flash Player 6) から規定され、映像コーデック「Sorenson Spark（H.263派生）」、音声コーデック「PCM」「ADPCM」「MP3」「Nellymoser」に対応した。

その後、Flash Player 8から、より高画質な映像を扱える社の映像コーデック「VP6」を追加。同時にVP6を利用して映像の[アルファチャンネル](../Page/アルファチャンネル.md "wikilink")を保持できる「VP6 with alpha channel」にも対応した。また、映像コーデック「ScreenVideo」「ScreenVideo v2」にも対応した。

Flash Player 9 update 3 (9,0,115,0) からは更に映像コーデック「AVC (H.264)」、音声コーデック「AAC」に対応したが、アドビ社は「H.264/AVCとAACをフルに活用したい場合はFLVではなくF4Vファイルフォーマットの利用を推奨する」としている。また、同バージョンではHD映像用のVP6コーデックの新たなプロファイル「VP6-S」にも対応。従来のVP6との再生互換性を保ちつつ、低データレートかつ低負荷でのHD映像再生をサポートしている。なお、これにともない従来のVP6は「VP6-E」プロファイルと呼ばれている。

また、Flash Player 10からは音声コーデック「Speex」に対応している。

F4Vファイルフォーマットは、従来のFLVファイルフォーマットとは別にFlash Player 9 update 3から規定されたフォーマットであり、「ISO/IEC 14496-12: ISO base media file format」(MPEG-4 Part 12) をベースとして規定されている。F4Vがサポートする映像コーデックは「H.264/AVC」、音声コーデックは「MP3」「AAC」のみとなっているが、上記の通りH.264/AVCとAACをフルに活用できるように設計されており、H.264/AVCとAACを扱う場合は、FLVではなくF4Vの利用が推奨されている。

また、[2007年](../Page/2007年.md "wikilink")[8月20日](https://ja.wikipedia.org/wiki/8月20日 "wikilink")、開発元のアドビシステムズはFlash Player 9 betaからFlash Videoとして[MPEG-4](../Page/MPEG-4.md "wikilink") ([H.264](../Page/H.264.md "wikilink"), [AAC](../Page/AAC.md "wikilink"), [HE-AAC](../Page/HE-AAC.md "wikilink")) をサポートする予定であることを発表、[2007年](../Page/2007年.md "wikilink")[12月3日](../Page/12月3日.md "wikilink")にリリースされたFlash Player 9 update 3 (9,0,115,0) から正式に対応した。これは従来のFLVコンテナとは別に、H.264/AVC映像とAAC音声を含んだMPEG-4派生のコンテナフォーマットの再生をある程度サポートするということであり、[MP4](../Page/MP4.md "wikilink")、M4A、MOV、MP4V、3GP、3G2といったコンテナの再生がサポートされている。F4Vコンテナもその1つと言える。

エンコードには[Adobe Flashに含まれているエンコーダ以外にも](../Page/Adobe_Flash.md "wikilink")、VP6コーデックでFLVファイルへのエンコードをサポートしている[On2](https://ja.wikipedia.org/wiki/On2テクノロジー "wikilink") Flix, [Sorenson](https://ja.wikipedia.org/wiki/Sorenson "wikilink") Squeezeなど[サードパーティー](../Page/サードパーティー.md "wikilink")製の製品も使用される。書き出すためのMac OS X QuickTime用コーデックがAdobe Flashに付属するため、Mac OS Xならば、QuickTimeを利用するアプリケーション群全てで書き出し等が可能である。なお、FLVファイルは1ファイルあたり1つのビデオと1つのオーディオストリームに制限される。

また、FLVファイルは[FLV Extractや](https://ja.wikipedia.org/wiki/FLV_Extract "wikilink")[HugFlash](https://ja.wikipedia.org/wiki/HugFlash "wikilink")等の[フリーウェア](../Page/フリーウェア.md "wikilink")を用いて無劣化で[AVIや](../Page/Audio_Video_Interleave.md "wikilink")[MOV等に変換することが可能](../Page/QuickTime.md "wikilink")（器である[コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")を換えるだけであるため）。

[ストリーミング](../Page/ストリーミング.md "wikilink")には[Adobe Flash Media Server](https://ja.wikipedia.org/wiki/Adobe_Flash_Media_Server "wikilink")（旧Macromedia Flash Communication Server）を利用した[RTMP](https://ja.wikipedia.org/wiki/Real_Time_Messaging_Protocol "wikilink") (RTMPT/RTMPS) プロトコルが使用されるが、通常の[HTTPプロトコルを利用可能のためFlash](../Page/Hypertext_Transfer_Protocol.md "wikilink") Videoのストリーミングとして後者が多く用いられる（厳密にはストリーミングではなく[プログレッシブダウンロード](https://ja.wikipedia.org/wiki/プログレッシブダウンロード "wikilink")であり[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の[キャッシュに保存したファイルを元に再生する](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。キャッシュが残っている場合はページ移動時の再読み込みが速くなる）。

なお、RTMPプロトコルの仕様書は現在Adobeのサイト上より入手することが可能\[1\]。一方、RTMPの仕様書が公開される以前より[Red5](https://ja.wikipedia.org/wiki/Red5 "wikilink")というオープンソースプロジェクトにより解析が進められており、無料で使用できるFlash Videoストリーミングサーバが提供されている（[Red5によるドキュメント](http://osflash.org/documentation/)）。

FLVファイルを[DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")などで再生する場合は、[FourCC](https://ja.wikipedia.org/wiki/FourCC "wikilink")として「FLV1」(Sorenson Spark)、「FLV4/VP6F」(On2 VP6) がよく用いられる（[FFmpeg](../Page/FFmpeg.md "wikilink")、[ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")、FLV Splitter等）。

### F4Vのファイル形式

| 拡張子  | [MIMEタイプ](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink") | 説明                           |
| ---- | ----------------------------------------------------------- | ---------------------------- |
| .f4v | video/mp4                                                   | Video for Adobe Flash Player |
| .f4p | Protected Video for Adobe Flash Player                      |                              |
| .f4a | audio/mp4                                                   | Audio for Adobe Flash Player |
| .f4b | Audio Book for Adobe Flash Player                           |                              |

### Codec support

  - FLVコンテナで対応するメディアフォーマット

<!-- end list -->

  - Video: Sorenson H.263 (FLV1), [On2 VP6](https://ja.wikipedia.org/wiki/On2_VP6 "wikilink") (FLV4), Screen video, [H.264](../Page/H.264.md "wikilink")
  - Audio: [MP3](../Page/MP3.md "wikilink"), [ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink"), [Linear PCM](../Page/パルス符号変調.md "wikilink"), , [Speex](../Page/Speex.md "wikilink"), [AAC](../Page/AAC.md "wikilink"), [HE-AAC](../Page/HE-AAC.md "wikilink"), [G.711](../Page/G.711.md "wikilink")（システム内部用に予約）

<!-- end list -->

  - F4Vコンテナで対応するメディアフォーマット

<!-- end list -->

  - Video: H.264
  - Images (still frame of video data): GIF, PNG, JPEG
  - Audio: AAC, HE-AAC, MP3

上記および下記、AACと書かれた物は、AAC+, AAC-LC, AAC v1, AAC v2, [HE-AAC](../Page/HE-AAC.md "wikilink") v1, HE-AAC v2に対応している。

<table>
<caption>Flash PlayerとFlash Videoのビデオ・オーディオ形式[2][3]</caption>
<thead>
<tr class="header">
<th></th>
<th></th>
<th><p>ファイル形式</p></th>
<th><p>ビデオ形式</p></th>
<th><p>オーディオ形式</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>6</p></td>
<td><p>2002</p></td>
<td><p>SWF</p></td>
<td><p>Sorenson Spark, Screen video</p></td>
<td><p>MP3, ADPCM, Nellymoser</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>2003</p></td>
<td><p>SWF, FLV</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
<td><p>2005</p></td>
<td><p>On2 VP6, Sorenson Spark, Screen video, Screen video 2</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>9.0.115.0</p></td>
<td><p>2007</p></td>
<td><p>On2 VP6, Sorenson Spark, Screen video, Screen video 2, H.264</p></td>
<td><p>MP3, ADPCM, Nellymoser, AAC, HE-AAC</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>SWF, F4V, ISO base media file format</p></td>
<td><p>H.264</p></td>
<td><p>AAC, HE-AAC, MP3</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>10</p></td>
<td><p>2008</p></td>
<td><p>SWF, FLV</p></td>
<td><p>On2 VP6, Sorenson Spark, Screen video, Screen video 2, H.264</p></td>
<td><p>MP3, ADPCM, Nellymoser, Speex, AAC, HE-AAC</p></td>
</tr>
<tr class="odd">
<td><p>SWF, F4V, ISO base media file format</p></td>
<td><p>H.264</p></td>
<td><p>AAC, HE-AAC, MP3</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

H.264とAACを使う場合、FLV形式ではいくつかの制約事項があるため、プレイヤー開発者は新しいF4V形式を使うことを強く推奨する。

## 出典

<references/>

## 関連項目

  - [Adobe Flash](../Page/Adobe_Flash.md "wikilink")
  - [Adobe Media Player](https://ja.wikipedia.org/wiki/Adobe_Media_Player "wikilink")
  - [Red5](https://ja.wikipedia.org/wiki/Red5 "wikilink")
  - [On2 VP6](https://ja.wikipedia.org/wiki/On2_VP6 "wikilink")
  - [H.263](../Page/H.263.md "wikilink")
  - [H.264](../Page/H.264.md "wikilink")
  - [YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")

<!-- end list -->

  -
    Flash Videoを利用した動画共有サービス。

<!-- end list -->

  - [ニコニコ動画](../Page/ニコニコ動画.md "wikilink")

<!-- end list -->

  -
    ビデオ形式にFlash Videoを採用している。

<!-- end list -->

  - [Googleビデオ](https://ja.wikipedia.org/wiki/Googleのサービス#Googleビデオ "wikilink")
  - [Veoh](../Page/Veoh.md "wikilink")
  - [ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")
  - [RealPlayer](../Page/RealPlayer.md "wikilink")

<!-- end list -->

  -
    バージョン11からFlash Videoの再生及び保存に対応。

## 外部リンク

  - [Adobe Flash Media Live Encoder](http://www.adobe.com/jp/products/flashmediaserver/flashmediaencoder/)
  - [Adobe Flash Video File Format Specification](http://www.adobe.com/devnet/f4v.html)

[Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:Adobe_Flash](https://ja.wikipedia.org/wiki/Category:Adobe_Flash "wikilink")

1.  Adobe 2009 [Real-Time Messaging Protocol (RTMP) specification](http://www.adobe.com/devnet/rtmp.html)
2.  [Adobe ActionScript 3.0 \* ビデオ形式について](http://help.adobe.com/ja_JP/ActionScript/3.0_ProgrammingAS3/WS5b3ccc516d4fbf351e63e3d118a9b90204-7d46.html)
3.  Adobe (2007-12-03) [List of codecs supported by Adobe Flash Player](http://kb2.adobe.com/cps/402/kb402866.html), Retrieved on 2009-08-10