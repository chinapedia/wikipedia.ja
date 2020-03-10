> この記事は[VP6](https://ja.wikipedia.org/wiki/VP6)から翻訳されています。


**On2 TrueMotion VP6**（トゥルーモーション ブイピーシックス）は[米国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")が開発したビデオ[コーデック](../Page/コーデック.md "wikilink")。

[Macromedia Flash 8で](../Page/Adobe_Flash.md "wikilink")[Flash Videoのコーデックの一つとして新たに採用されている](../Page/Flash_Video.md "wikilink")。なお、実際にFlash内に組み込むには[Flash Professional 8または](../Page/Adobe_Flash.md "wikilink")[Flex 2以降が必要になる](https://ja.wikipedia.org/wiki/Flex "wikilink")。また、[中国独自の](../Page/中華人民共和国.md "wikilink")[DVD](../Page/DVD.md "wikilink")代替規格である[EVD](../Page/EVD.md "wikilink") (Enhanced Versatile Disk) の動画[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")としても採用されている。

[MPEG-4](../Page/MPEG-4.md "wikilink")の技術を基礎にして作られた[VP3](https://ja.wikipedia.org/wiki/VP3 "wikilink")、[VP4](https://ja.wikipedia.org/wiki/VP4 "wikilink")、[VP5](https://ja.wikipedia.org/wiki/VP5 "wikilink")の後継とされており、すべての性能がVP5よりも向上しているとしている。

圧縮率はMPEG-4のサブセットとして出て間もなかった[H.264 AVCを凌駕し](../Page/H.264.md "wikilink")/MPEG-4、同様に高画質でありながら低スペックで再生可能とする[Windows Media Video 9/VC-1よりも絶対的に高いとしている](../Page/VC-1.md "wikilink")。

また、フル[HDTVクラス](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")（1920×1080ピクセル）の動画を2.5[GHz程度の](../Page/ギガヘルツ.md "wikilink")[CPU](../Page/CPU.md "wikilink")で[デコードできるという](../Page/エンコード.md "wikilink")、デコードの速さも売りである。

## 特徴

  - 高圧縮、高画質（[フルハイビジョンは](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")6〜8Mbps程度で可能）
  - デコードが速い
  - [エンコード](../Page/エンコード.md "wikilink")が非常に遅い
  - 低レートにおいても破綻しない（640×480ピクセルの動画を200kbpsでエンコードしても見られる範囲）
  - 高レートでも安定している
  - [MPEG-2](../Page/MPEG-2.md "wikilink")等と比べて廉価な[ライセンス料](../Page/ロイヤルティー.md "wikilink")

## 画質

VP6は[VC-1](../Page/VC-1.md "wikilink")や[H.264](../Page/H.264.md "wikilink")と同等に[デブロッキング](https://ja.wikipedia.org/wiki/デブロッキング "wikilink")フィルターを使用しており[ブロックノイズ](../Page/ブロックノイズ.md "wikilink")は目立たない。しかしながら、玉になるようなノイズがみられ、長い間変化が少なく揺らぐような画像においては多少なりノイズが目立つようになる。

VP6は暗部のノイズに強く、MPEGやVC-1よりも暗部の再現能力は優れている。したがって、暗い画像でもノイズの少ない画像として記録することができる。

カラースペースは[MPEG-1](../Page/MPEG-1.md "wikilink")と同様に[YUV420](https://ja.wikipedia.org/wiki/色空間#YCbCr_/_YPbPr "wikilink") (YV12) が採用されている。

また、圧縮率を上げるとのっぺりとした画像になるが、MPEG系の低レート時よりは見やすいといえる。

## メソッド

### VP60R Simple Profile

VP6の最初のバージョンで実装されていた[プロファイル](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")。

3つのプロファイルの中では最も速く圧縮することができるが、画質は最も悪い。

オプションには[ノイズリダクション](../Page/ノイズリダクション.md "wikilink")しか存在していない。しかし、このノイズリダクションは強いものでは無く、実際掛けたところでどれほどの効果が上がっているのかは未知数である。

### VP61R Advanced Profile

VP6.1として登場したプロファイル。

圧縮率や画質は向上しているが、その分再生速度、圧縮速度ともに落ちた。

### VP62R Heightened Sharpness Profile

VP6としては最高のプロファイル。VP6.2で登場した。

Advanced Profileよりもさらに圧縮率が向上し、画質が向上している。

新たに[シャープフィルタ](https://ja.wikipedia.org/wiki/シャープフィルタ "wikilink")が追加されている。

## 利用例

  - [EVD](../Page/EVD.md "wikilink") (Enhanced Versatile Disk)
  - [Macromedia Flash 8](../Page/Adobe_Flash.md "wikilink")
  - [WinAMP](https://ja.wikipedia.org/wiki/Winamp "wikilink")
  - TrueCast Player

## コンテナ形式

[Flash Video](../Page/Flash_Video.md "wikilink") (FLV) の他、[AVIや](../Page/Audio_Video_Interleave.md "wikilink")[MKVでも利用が可能である](../Page/Matroska.md "wikilink")。AVIとFLVは無劣化での相互変換が可能。 さらにOn2社製の[TrueCast](https://ja.wikipedia.org/wiki/TrueCast "wikilink")7 (.tc7)という形式でも使うことができる。この場合、音声コーデックは[TrueAudioになる](../Page/TTA.md "wikilink")。

## [FOURCC](https://ja.wikipedia.org/wiki/FOURCC "wikilink")

  - VP60
  - VP61
  - VP62
  - FLV4
  - VP6F

## 関連項目

  - [VP3](https://ja.wikipedia.org/wiki/VP3 "wikilink")
  - [VP7](https://ja.wikipedia.org/wiki/VP7 "wikilink")
  - [VP8](https://ja.wikipedia.org/wiki/VP8 "wikilink")
  - [VP9](https://ja.wikipedia.org/wiki/VP9 "wikilink")
  - [Theora](../Page/Theora.md "wikilink")

## 外部リンク

  - [On2 TrueMotion VP6](http://www.on2.com/index.php?358)
  - [Adobe Flash Media Encoder](http://www.adobe.com/jp/products/flashmediaserver/flashmediaencoder/)
  - [kaourantin.net: The quest for a new video codec in Flash 8](http://www.kaourantin.net/2005/08/quest-for-new-video-codec-in-flash-8.html)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink")