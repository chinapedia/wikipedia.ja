> この記事は[Cinepak](https://ja.wikipedia.org/wiki/Cinepak)から翻訳されています。


**Cinepak**（シネパック）は[SuperMac Technologiesの一事業部であるSuperMatchが開発した](https://ja.wikipedia.org/wiki/:en:SuperMac "wikilink")[ビデオコーデック](https://ja.wikipedia.org/wiki/コーデック#動画圧縮のコーデック "wikilink")。

## 概要

[1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink")に[アップルコンピュータの](../Page/アップル_\(企業\).md "wikilink")[QuickTime](../Page/QuickTime.md "wikilink")の一部としてリリースされた。

1倍速（150 kbyte/s）の[CD-ROM](../Page/CD-ROM.md "wikilink")の転送速度で320x240の解像度のビデオを[エンコード](../Page/エンコード.md "wikilink")できるように設計された。このコーデックは[1993年](../Page/1993年.md "wikilink")にWindowsへ移植された。また[Atari Jaguar CD](../Page/Atari_Jaguar.md "wikilink")、[メガCD](../Page/メガCD.md "wikilink")、[セガサターン](../Page/セガサターン.md "wikilink")、[3DO](../Page/3DO.md "wikilink")といった1990年代に発売されたCD-ROMを搭載する家庭用ゲーム機でも利用できた。

これは初期の[QuickTime](../Page/QuickTime.md "wikilink")（MOV）やマイクロソフトの[Video for Windows](https://ja.wikipedia.org/wiki/Video_for_Windows "wikilink")（[AVI](https://ja.wikipedia.org/wiki/Audio_Video_Interleave "wikilink")）で主力のビデオコーデックであったが、[Sorenson Videoや](https://ja.wikipedia.org/wiki/Sorenson_Video "wikilink")[Indeo Video](https://ja.wikipedia.org/wiki/Indeo "wikilink")、そして2000年代後半以降の[VC-1](https://ja.wikipedia.org/wiki/VC-1 "wikilink")や[H.264](https://ja.wikipedia.org/wiki/H.264 "wikilink")に取って代わられた。しかしながらCinepakで圧縮されたムービーはほとんどのムービー再生ソフトでまだ一般的に再生可能である。

Cinepakは現在ほとんどのコーデックが（特に[JPEG](../Page/JPEG.md "wikilink")や[MPEGファミリーが](../Page/Moving_Picture_Experts_Group.md "wikilink")）利用している[DCTアルゴリズムとは全く異なる](https://ja.wikipedia.org/wiki/離散コサイン変換 "wikilink")[ベクトル量子化](https://ja.wikipedia.org/wiki/ベクトル量子化 "wikilink")アルゴリズムを採用している。比較的低速な[CPU](../Page/CPU.md "wikilink")で実行できた（[68040の](https://ja.wikipedia.org/wiki/MC68040 "wikilink")25MHzクラスのCPUにおいて、320x240のビデオを秒間30フレームで再生できた）が、[ビットレートを落とすとブロックノイズが生じる傾向があり](../Page/ビット毎秒.md "wikilink")、フルモーションビデオゲームで批判を浴びた。

Cinepakはムービーをキーイメージとイントラコードイメージに分割する。各イメージはキーイメージ内に転送される独立した256色のカラーパレットを持つたくさんの水平な帯で分割される。それぞれの帯は4x4ピクセルのブロックで細分化される。圧縮プログラムは各ブロックにベストマッチする1〜2つの帯のパレットカラーを決定するために[ベクトル量子化](https://ja.wikipedia.org/wiki/ベクトル量子化 "wikilink")アルゴリズムを使用し、1カラーバイトまたは2カラーバイトのいずれかに加え、どのピクセルがどの色になるのかを決める16ビットのベクタでブロックの連続をエンコードする。イントラコードのフレームに対するキーのレートを調整し、各ブロックとブロックのランレングスで防げなかったエラーを調整して、狭い範囲内でデータレートが制御される。

このコーデックの名前は以前はCompactVideoであり、[FourCC](https://ja.wikipedia.org/wiki/FourCC "wikilink")識別子が"CVID"であるのはこのためである。

## コンテナ形式

  - Cinepakは主に[AVIと](https://ja.wikipedia.org/wiki/Audio_Video_Interleave "wikilink")[MOVで使われていた](../Page/QuickTime.md "wikilink")。

## 外部リンク

  - [Cinepakコーデックの技術資料（WebArchive）](http://web.archive.org/web/20020422040757/http://www.csse.monash.edu.au/~timf/videocodec/cinepak.txt)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink")