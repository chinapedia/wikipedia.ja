> この記事は[VirtualDub](https://ja.wikipedia.org/wiki/VirtualDub)から翻訳されています。


**VirtualDub**（バーチャルダブ）は[動画](../Page/動画.md "wikilink")編集・[キャプチャーカードや](../Page/キャプチャ_\(録画ソフト\).md "wikilink")[WEB](../Page/World_Wide_Web.md "wikilink")[カメラなどから動画キャプチャーが行えるソフト](../Page/ビデオカメラ.md "wikilink")、[エンコーダー](../Page/エンコード.md "wikilink")。[GPLで配布されている](../Page/GNU_General_Public_License.md "wikilink")。

機能を拡張した**VirtualDub-MPEG2**や**VirtualDubMod**などの[亜種](https://ja.wikipedia.org/wiki/亜種 "wikilink")（改造版）も存在している。

## 概要

[AVI](https://ja.wikipedia.org/wiki/AVI "wikilink")[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")に対応した動画編集ソフト。[VBR](https://ja.wikipedia.org/wiki/VBR "wikilink")エンコードされた[MP3](../Page/MP3.md "wikilink")や[MPEG-1](../Page/MPEG-1.md "wikilink")の読み込みを標準でサポート。[プラグイン](../Page/プラグイン.md "wikilink")での拡張によりその他のフォーマットも読み込めるようになる。バージョン1.7からは[スマートレンダリング](https://ja.wikipedia.org/wiki/スマートレンダリング "wikilink")にも対応した。2004年9月のバージョン1.6から32bit版と64bit版が配布されている。[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")版も付属する。

## 特許問題

[ASFファイルフォーマットは](../Page/Advanced_Systems_Format.md "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")社が[米国で](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[特許](../Page/特許.md "wikilink")を取得している([US patent 6041345](http://v3.espacenet.com/textdoc?DB=EPODOC&IDX=US6041345))。VirtualDubはASFファイルの読み込みに正式対応していたが、マイクロソフト社側から[クレーム](../Page/クレーム.md "wikilink")を受けたため、それ以降はASFファイル非対応となり、ソースコードには 「microsoft no baka\!」と記述されている。

## フィルター

30種以上のフィルターが内蔵されているが、フィルターファイル(\*.vdf)をpluginsフォルダに入れることにより追加することができる。

## 入力プラグイン

プラグインファイル(\*.vkf/\*.vdplugin)を追加することで各フォーマットの読み込みに対応できる。32bit版はplugins32フォルダを作成、64bit版はplugins64フォルダを作成しプラグインファイルを入れる。

読み込みエラーが出る場合は[ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")のvfwの設定で該当[コーデック](../Page/コーデック.md "wikilink")を有効にしておくなどすると良い。必ず読み込めるとは限らず不安定な場合もあるので注意が必要。

**32bit版**

  - [WMV](https://ja.wikipedia.org/wiki/WMV "wikilink") (asf,wmv,wma)\[1\]
  - [AC-3](https://ja.wikipedia.org/wiki/AC-3 "wikilink")\[2\]
  - [FLIC](https://ja.wikipedia.org/wiki/FLIC "wikilink")\[3\]
  - [MPEG-2](../Page/MPEG-2.md "wikilink") (mpg,vob,m2v,mpeg,vdr)\[4\]
  - [Flash Video](../Page/Flash_Video.md "wikilink") (flv)\[5\]\[6\]
  - [Quick Time](https://ja.wikipedia.org/wiki/Quick_Time "wikilink") (mov,mp4)\[7\]\[8\]
  - [Matroska](../Page/Matroska.md "wikilink") (mkv,mka)\[9\]
  - [PVN](https://ja.wikipedia.org/wiki/PVN "wikilink")\[10\]
  - [Redcode RAW](../Page/レッド・デジタル・シネマカメラ・カンパニー.md "wikilink") files (R3D)\[11\]
  - [DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")\[12\]

**64bit版**

  - WMV\[13\]
  - AC-3\[14\]
  - FLIC\[15\]
  - MPEG-2\[16\]
  - Flash Video\[17\]
  - Quick Time\[18\]
  - Matroska\[19\]
  - DirectShow\[20\]

## 改造版

開発が終了したものも含む。

  - **VirtualDubMod** - [Matroska](../Page/Matroska.md "wikilink")や[Ogg Mediaの読み込み](../Page/Ogg_Media.md "wikilink")・作成に対応。
  - **VirtualDubMod Aud-X** - [Aud-X](https://ja.wikipedia.org/wiki/Aud-X "wikilink")等の[ACM](https://ja.wikipedia.org/wiki/Audio_Compression_Manager "wikilink")[サラウンド](../Page/サラウンド.md "wikilink")オーディオに対応させたもの
  - **VirtualDub-MPEG2** - [MPEG-2](../Page/MPEG-2.md "wikilink")の読み込みに対応。
  - **Nandub** - 2-pass[エンコード](../Page/エンコード.md "wikilink")を目的に作成されたもの。
  - **VirtualDub APNG Mod** - [Animated Portable Network Graphicsのサポート](../Page/Animated_Portable_Network_Graphics.md "wikilink")。

## 関連項目

  - [動画編集ソフトウェア](https://ja.wikipedia.org/wiki/動画編集ソフトウェア "wikilink")
  - [Avidemux](https://ja.wikipedia.org/wiki/Avidemux "wikilink")
  - [AviUtl](../Page/AviUtl.md "wikilink")
  - [AviSynth](https://ja.wikipedia.org/wiki/AviSynth "wikilink")
  - [OpenShot Video Editor](https://ja.wikipedia.org/wiki/OpenShot_Video_Editor "wikilink")
  - [TMPGEnc](../Page/TMPGEnc.md "wikilink")
  - [ノンリニア編集](../Page/ノンリニア編集.md "wikilink")

## 脚注

<references />

## 外部リンク

  - [Welcome to virtualdub.org\!](http://www.virtualdub.org/)
  - [VirtualDubMod](http://virtualdubmod.sourceforge.net/)
  - [VirtualDub APNG Mod](http://vdubapngmod.sourceforge.net/)
  - [VirtualDub日本語化パッチ](https://tnetsixenon.xrea.jp/)

[Category:映像編集・合成ソフト](https://ja.wikipedia.org/wiki/Category:映像編集・合成ソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [fccHandler's stuff](http://home.comcast.net/~fcchandler/)
2.
3.
4.
5.
6.  [Moitah.net](http://moitah.net/)
7.
8.  <http://www.tateu.net/software/>
9.
10. [VirtualDubフォーラム内](http://forums.virtualdub.org/index.php?act=ST&f=7&t=15580)
11. <http://arenafilm.hu/alsog/vdr3d/>
12. [VirtualDubフォーラム内](http://forums.virtualdub.org/index.php?act=ST&f=7&t=15093)
13.
14.
15.
16.
17.
18.
19.
20.