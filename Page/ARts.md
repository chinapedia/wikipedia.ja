> この記事は[ARts](https://ja.wikipedia.org/wiki/ARts)から翻訳されています。


**aRts** は **a**nalog **R**eal **t**ime **s**ynthesizer の略であり、[KDE](../Page/KDE.md "wikilink") のもとでアナログシンセサイザーをシミュレートする[アプリケーションである](../Page/アプリケーションソフトウェア.md "wikilink")。

## 概要

aRts の重要な構成要素は[サウンドサーバ](https://ja.wikipedia.org/wiki/サウンドサーバ "wikilink")であり、[リアルタイム](../Page/リアルタイム.md "wikilink")で複数の[サウンドストリームを混ぜるものである](../Page/ストリーミング.md "wikilink")。artsd（d は[デーモン](../Page/デーモン.md "wikilink")を表す）と呼ばれる[サウンドサーバ](https://ja.wikipedia.org/wiki/サウンドサーバ "wikilink")は KDE の標準的なサウンドサーバとしても利用されている。このサウンドサーバは KDE に依存せず、他のプロジェクトで使うことができる。aRts は別のリアルタイムサウンドサーバである [JACK Audio Connection Kit](https://ja.wikipedia.org/wiki/JACK_Audio_Connection_Kit "wikilink") に直接競合し、[Enlightened Sound Daemon](https://ja.wikipedia.org/wiki/Enlightened_Sound_Daemon "wikilink") (ESD) に間接的に競合する。今は artsd の代わりに [ALSA](https://ja.wikipedia.org/wiki/Advanced_Linux_Sound_Architecture "wikilink") のソフトウェアミキサーを使うことが一般的である。

**aRts** [プラットフォーム](../Page/プラットフォーム.md "wikilink") には [aRtsビルダー](https://ja.wikipedia.org/wiki/aRtsビルダー "wikilink")も含まれ、これは使いやすい[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")を通してミキサー、シーケンサー、シンセサイザーなどのオーディオ[スキーマ](https://ja.wikipedia.org/wiki/スキーマ "wikilink")に対するカスタムのレイアウトや設定を構築するためのアプリケーションである。aRts は[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であり、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") のもとで配布されている。

## aRts の将来

[2004年](../Page/2004年.md "wikilink")[12月2日](../Page/12月2日.md "wikilink")に、aRts の製作者や主な開発者 Stefan Westerfeld は aRts に関する多くの基本的な開発上の問題や技術問題のためにプロジェクトを離れると[公表した](http://www.arts-project.org/doc/arts-maintenance.html)。

KDE 4 で開発者は aRts を [Phonon](https://ja.wikipedia.org/wiki/Phonon "wikilink") として知られている新しいマルチメディア API で置き換えることを計画している[1](http://dot.kde.org/1146140474/)。Phonon では単一のマルチメディアフレームワークに依存することを避けるため、[Xine](../Page/Xine.md "wikilink") のような、他のシステムの上に共通したインターフェイスを提供することになる。

## 関連項目

  - [Enlightened Sound Daemon](https://ja.wikipedia.org/wiki/Enlightened_Sound_Daemon "wikilink") (ESD) – [GNOME](../Page/GNOME.md "wikilink") で使われる
  - [PulseAudio](https://ja.wikipedia.org/wiki/PulseAudio "wikilink") - ESD を置き換えることを目標とした Advanced Sound Server

## 外部リンク

  - [aRts プロジェクトの公式サイト](http://www.arts-project.org/)

[Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink") [Category:ソフトウェア・シンセサイザー](https://ja.wikipedia.org/wiki/Category:ソフトウェア・シンセサイザー "wikilink")