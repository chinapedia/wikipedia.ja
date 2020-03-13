> この記事は[Motion JPEG](https://ja.wikipedia.org/wiki/Motion_JPEG)から翻訳されています。


**Motion JPEG**（モーション ジェイペグ）とは、[動画](../Page/動画.md "wikilink")圧縮形式の一つである。

## 概要

それぞれの[フレームを](../Page/コマ_\(映画・漫画\).md "wikilink")[JPEG](../Page/JPEG.md "wikilink")形式で圧縮／伸長し、連続でこれを表示することで動画としている。

同じくJPEGの技術を応用した動画圧縮形式として知られる[MPEGは時間軸すなわちフレーム間も圧縮するのに対し](../Page/MPEG-1.md "wikilink")、Motion JPEGではフレーム間の圧縮を行わず、JPEGの2次元圧縮のみ行う方式である。音声ストリーム等を別とすれば、ファイルの実態は1コマ毎に静止画JPEGと同様の構造となる。そのため同じ[フレームレート](../Page/フレームレート.md "wikilink")であればMPEGよりは圧縮率が低くなるものの、激しい動きでもMPEGほど乱れない動画を作れた。一方でフレームレートが比較的ダイレクトにファイルサイズに反映されるため、フレームレートを犠牲にしてファイルサイズを減少させることもできた。また圧縮・展開が容易で、ソフトウェアやハードウェアのパワーをMPEGほど必要とはしない。さらに任意のフレームを切り出せるので、編集を容易に行える。

そのような扱いやすさを備える汎用の規格であることに加え、当時のマシンパワーでも圧縮率と画質をそれなりに両立できたことから、少なくとも1997年ごろまでは「もっとも実用的な動画圧縮方式」と言われていた\[1\]。

[コンテナ形式には](../Page/コンテナフォーマット.md "wikilink")[AVIと](../Page/Audio_Video_Interleave.md "wikilink")[MOVがあり統一されていない](../Page/QuickTime.md "wikilink")。[QuickTime Playerなどで再生可能なほか](../Page/QuickTime.md "wikilink")、Windowsでは[コーデック](../Page/コーデック.md "wikilink")をインストールすることで[メディアプレーヤーでも再生できた](../Page/Windows_Media_Player.md "wikilink")。

近年では、[Motion JPEG 2000や](../Page/JPEG_2000.md "wikilink")[Motion JPEG XRといった高性能な動画形式も開発されている](https://ja.wikipedia.org/wiki/JPEG_XR "wikilink")。

## 用途

当時は特にビデオキャプチャーカードの出力形式として利用されることが多かったが、マシンパワーやハードウェアの進歩により、次第に[MPEG-4 AVCにその地位を明け渡した](../Page/H.264.md "wikilink")。そのためにパソコン上で記録するために用いられることは少なくなったが、JPEG変換処理能力が高い[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")や[デジタルフォトフレーム](../Page/デジタルフォトフレーム.md "wikilink")での録画、再生用として利用が続いた。

当時の家庭用テレビゲーム機の一部にも採用されており、動画再生機能を売りとした[PC-FX](../Page/PC-FX.md "wikilink")にMotion JPEGデコーダが搭載されたほか、初代[プレイステーションの動画再生形式としてもサポートされた](../Page/PlayStation_\(ゲーム機\).md "wikilink")。また、後年には[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")の[写真チャンネル](../Page/写真チャンネル.md "wikilink")の動画形式としてもMotion JPEGが採用されている。

## 脚注

## 関連項目

  - [Motion JPEG 2000](../Page/JPEG_2000.md "wikilink")
  - [Motion JPEG XR](https://ja.wikipedia.org/wiki/JPEG_XR "wikilink")
  - [GIFアニメーション](../Page/GIFアニメーション.md "wikilink")
  - [DV (ビデオ規格)](../Page/DV_\(ビデオ規格\).md "wikilink")
  - [デジタルカメラ](../Page/デジタルカメラ.md "wikilink")
  - [QuickTime](../Page/QuickTime.md "wikilink")
  - [Audio Video Interleave](../Page/Audio_Video_Interleave.md "wikilink")
  - [ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")

## 外部リンク

  - [ダウンロード Motion JPEG 再生ドライバ](http://pro.grassvalley.jp/download/mjpgpbk.htm) - グラスバレー（旧カノープス）から提供されているWindows用32ビット版 Motion JPEGコーデック。かつては16ビット版 も提供されていた。
  - [MJPEG tools](http://mjpeg.sourceforge.net) - MJPEG toolsは、ビデオの録画と再生ができ、簡単な切り取り貼り付け編集、ビデオとオーディオのMPEG圧縮をおこなうツールである。
  - [ffdshow-tryouts](http://sourceforge.net/project/showfiles.php?group_id=173941) - ffdshow は、高度な DirectShow フィルターと、オーディオとビデオの多彩な形式をサポートしている VFW コーデックである。
  - [Apple Quicktime Format, including specification for MJPEG-A & MJPEG-B](http://developer.apple.com/standards/qtff-2001.pdf), pp95., アップルコンピュータ(2001).
  - [RFC 2435 RTP Payload Format for JPEG-compressed Video](http://tools.ietf.org/html/rfc2435)

[Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink")

1.  [グラスバレー](../Page/グラスバレー_\(企業\).md "wikilink")（旧カノープス）が提供しているMotion JPEGコーデック\[[http://pro.grassvalley.jp/download/mjpgpbk.htm\]のREADME.TXTより](http://pro.grassvalley.jp/download/mjpgpbk.htm%5DのREADME.TXTより)。