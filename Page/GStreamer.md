> この記事は[GStreamer](https://ja.wikipedia.org/wiki/GStreamer)から翻訳されています。


**GStreamer**（ジーストリーマー）は、[フリー](../Page/フリーソフトウェア.md "wikilink")（ライセンスは[LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink")）の[マルチメディア](../Page/マルチメディア.md "wikilink")フレームワーク。

[C言語](../Page/C言語.md "wikilink")で記述され、主に[UNIX](../Page/UNIX.md "wikilink")で開発されている。ビデオ編集ソフトやストリーミング、そして[メディアプレーヤ](https://ja.wikipedia.org/wiki/メディアプレーヤ "wikilink")などのようなマルチメディア[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")のベースとなる機能を提供する。[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")となるよう設計されており、[Linux](../Page/Linux.md "wikilink") ([x86](https://ja.wikipedia.org/wiki/x86 "wikilink"), [PowerPC](../Page/PowerPC.md "wikilink"), [ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink"))、[Solaris](../Page/Solaris.md "wikilink") (x86, [SPARC](../Page/SPARC.md "wikilink"))、[OpenSolaris](../Page/OpenSolaris.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")上で動く。

核となる部分以外では、プラグインのライブラリ群で構成されている。 動的にロードされ、種々の[コーデック](../Page/コーデック.md "wikilink")、[コンテナフォーマット](https://ja.wikipedia.org/wiki/コンテナフォーマット "wikilink")、出力ドライバをサポートしている。 他の[プログラミング言語](../Page/プログラミング言語.md "wikilink")では、[Python](../Page/Python.md "wikilink")、[Vala](https://ja.wikipedia.org/wiki/Vala "wikilink")、[C++](../Page/C++.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[GNU Guile](https://ja.wikipedia.org/wiki/GNU_Guile "wikilink")、[Ruby](../Page/Ruby.md "wikilink")などに[バインディングされている](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")。

[GNOME](../Page/GNOME.md "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")はGStreamer技術の最初のかつ主要なユーザであり、GNOMEのアプリケーションがマルチメディア機能を実装するのにこのフレームワークを利用するよう支援した。[KDE](../Page/KDE.md "wikilink")のメディアプレーヤである[Amarok](https://ja.wikipedia.org/wiki/Amarok "wikilink")など、他のアプリケーションもこれを利用している。KDEのバージョン4では、これが標準のマルチメディアフレームワークとなる予定であったが、頻繁に[ABIが変更されるため](https://ja.wikipedia.org/wiki/Application_Binary_Interface "wikilink")、KDE では新たに [Phonon](https://ja.wikipedia.org/wiki/Phonon "wikilink") が開発されることとなった。PhononではバックエンドとしてGStreamerを使うことができる。

GStreamerは[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")や[タブレット](https://ja.wikipedia.org/wiki/タブレット "wikilink")などの組み込み機器でも利用されていて、[Palm Pre](https://ja.wikipedia.org/wiki/Palm_Pre "wikilink")、[Maemo](https://ja.wikipedia.org/wiki/Maemo "wikilink")、[Tizen](https://ja.wikipedia.org/wiki/Tizen "wikilink") などで使われている。

GStreamer は CPU によるソフトウェアコーデックも利用できるし、OpenMAX IL (Linux), DirectShow (Windows), QuickTime (macOS) などを経由して OS のコーデックを再利用したり、ハードウェアコーデックを呼び出したりすることも出来るし、[FFmpeg](../Page/FFmpeg.md "wikilink") (libav) 経由でそれらのコーデックを利用することも出来るし、VPU ベンダーのハードウェアコーデックのプラグインを利用したりすることも出来る。

このプロジェクトは、[freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink")でホストされており、フリーなデスクトップ環境間での相互運用性を改善することや技術を共有することを目的としている。

## 歴史

このプロジェクトは、[1999年](../Page/1999年.md "wikilink")にErik Walthinsenによって設立され、[オレゴン大学院大学](https://ja.wikipedia.org/wiki/オレゴン大学院大学 "wikilink")の研究プロジェクトから多くの核となるアイデアがもたらされた。Wim Taymansはすぐにプロジェクトに参加して、以来システムを多くの面で拡張した。世界中の多くの人が様々な面で貢献した。RidgeRunという[組み込みLinux](../Page/組み込みLinux.md "wikilink")の企業で働くBrock A. Frazierによってロゴがデザインされた。この企業は、Erik Walthinsenを小型機器にGStreamerを組み込む方法を開発するために雇用する、という形でGStreamerの最初のスポンサーとなった。

## 脚注

## 関連項目

  - [オープンソースのコーデックとコンテナフォーマット一覧](../Page/オープンソースのコーデックとコンテナフォーマット一覧.md "wikilink")
  - [オープンソースのメディアプレーヤー一覧](../Page/オープンソースのメディアプレーヤー一覧.md "wikilink")

## 外部リンク

  -
  - [GStreamerアプリケーション開発マニュアル](http://gstreamer.freedesktop.org/data/doc/gstreamer/head/manual/html/index.html)

      - [日本語訳(あしたのオープンソース研究所)](http://oss.infoscience.co.jp/gstreamer/)

  - [GStreamerを利用したアプリケーションソフトの一覧](http://gstreamer.freedesktop.org/apps/)

  - [GStreamer概要 - SourceForge.JP Magazine](http://sourceforge.jp/magazine/03/06/16/1621207)

[Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")