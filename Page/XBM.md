> この記事は[XBM](https://ja.wikipedia.org/wiki/XBM)から翻訳されています。


**XBM**（X BitMap）は、[X Window Systemの](../Page/X_Window_System.md "wikilink")[GUIにおいて](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[カーソル](../Page/カーソル.md "wikilink")や[アイコン](../Page/アイコン.md "wikilink")に使用する[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")を格納するための、[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")による[二値画像](https://ja.wikipedia.org/wiki/二値画像 "wikilink")[ファイルフォーマットである](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")\[1\]。1989年に登場した[X11](https://ja.wikipedia.org/wiki/X11 "wikilink")以降、XBMは[XPM](../Page/XPM.md "wikilink")に置き換えられた\[2\]。

## データ形式

他の画像ファイルに対するXBMファイルの明確な特徴として、[C言語](../Page/C言語.md "wikilink")のソースコードの文法を流用している点が挙げられる。これによって、前処理を経ずに直接アプリケーションに埋め込んでコンパイルすることが可能であるが、一方で元の[ピクセル](../Page/ピクセル.md "wikilink")データよりもファイルの大きさは著しく増大する。1バイトの画像情報を表現するのに複数のASCII文字が使われるために、画像データは'0x13'のようにC言語の16進記数法で記述されたバイト値を、コンマで区切ったリストとして符号化される\[3\]。

XBMのデータは、白黒のピクセルデータを持つ一連のstatic unsigned char型の[配列](../Page/配列.md "wikilink")で構成される。このフォーマットが広く使われていた時期には、ひとつの[ヘッダ](https://ja.wikipedia.org/wiki/ヘッダ_\(コンピュータ\) "wikilink")（.hファイル）ごとに単一の配列として画像を格納する形が一般的にみられた。以下はXBMをCソースコード内に記述した例である。

``` C
#define test_width 16
#define test_height 7
static unsigned char test_bits[] = {
0x13, 0x00, 0x15, 0x00, 0x93, 0xcd, 0x55, 0xa5, 0x93, 0xc5, 0x00, 0x80,
0x00, 0x60 };
```

通常の画像フォーマットのヘッダの代わりに、XBMでは2つないしは4つの\#define指示文が置かれる。先頭の2つの\#defineでは画像の縦と横のピクセル数が指定される。残りの2つでは（もしあるとすれば）ビットマップ内の「ホットスポット」（カーソルを指したときに反応する位置、一般的には0,0）の位置が指定される。

XBMの画像データは、静的配列に格納された1行のピクセル値で構成される。1[ビット](../Page/ビット.md "wikilink")がそれぞれのピクセル（0が白で1が黒）に対応するため、配列内では1バイトあたり8ピクセルの情報を持ち、画像内の左上端のピクセルは配列内の最初の1バイトの低位ビットで表される。画像の幅が8の倍数でない場合には、それぞれの行の最後の1バイト内の余分なビットは読み飛ばされる。

## サポート

[World Wide Webの黎明期において](../Page/World_Wide_Web.md "wikilink")、XBMがプロプライエタリではない最小の画像フォーマットだった名残りとして、いくつかの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")ではXBM画像の表示がサポートされている。ではバージョン0.3.34（1997年7月リリース）から完全にサポートされている\[4\]。[Internet Explorer 6や](https://ja.wikipedia.org/wiki/Internet_Explorer_6 "wikilink")[Mozilla Firefox 3.6](https://ja.wikipedia.org/wiki/Mozilla_Firefoxのバージョンの変遷#Firefox_3.6 "wikilink")\[5\]、それに[WebKit](../Page/WebKit.md "wikilink")ベースのウェブブラウザ\[6\]ではXBMサポートは削除されている。[Chromium](https://ja.wikipedia.org/wiki/Chromium "wikilink")では（[Google Chromeもまた同様に](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")）XBMがサポートされていない可能性が非常に高い\[7\]。[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")のバージョン2.12および6.0のドキュメントによれば、少なくともXBMが以前にはサポートされていたと示唆されている\[8\]\[9\]。

[XnView](https://ja.wikipedia.org/wiki/XnView "wikilink")や[FFmpeg](../Page/FFmpeg.md "wikilink")、[IrfanView](../Page/IrfanView.md "wikilink")など、いくつかの画像ビューアや変換ソフトウェアではXBMがサポートされている。48x48ピクセルのXBMは、[Netpbm](https://ja.wikipedia.org/wiki/Netpbm "wikilink")によって*Ikon*や[X-Face](https://ja.wikipedia.org/wiki/X-Face "wikilink")に変換できる\[10\]。

XPMに置き換えられたにもかかわらず、現代的であっても軽量な[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")では未だにXBMが活用されており、[Openbox](https://ja.wikipedia.org/wiki/Openbox "wikilink")ではウィンドウのタイトルバー上に表示される、アイコン化・最小化・復帰・最大化などの簡素なボタンの画像に使われている\[11\]。さらに、組み込みコンピュータ（マイクロコントローラ）のGUIでアイコンを表示するためにもXBMが使われている\[12\]。[ImageMagick](../Page/ImageMagick.md "wikilink")ではXBMの他フォーマットからの、または他フォーマットへの変換がサポートされている\[13\]。[GIMP](../Page/GIMP.md "wikilink")はXBMを作成・加工するために利用でき、他フォーマットからの、または他フォーマットへの変換もサポートされている。

## 脚注

## 関連項目

  - [Xlib](../Page/Xlib.md "wikilink")

[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.