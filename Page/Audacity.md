> この記事は[Audacity](https://ja.wikipedia.org/wiki/Audacity)から翻訳されています。


**Audacity**（オーダシティ）は[フリーな](../Page/フリーソフトウェア.md "wikilink")[デジタル・オーディオ・エディタ](https://ja.wikipedia.org/wiki/波形編集ソフトウェア "wikilink")。[Linux](../Page/Linux.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")などの[PC-UNIX](https://ja.wikipedia.org/wiki/PC-UNIX "wikilink")、[Mac OS 9](https://ja.wikipedia.org/wiki/Classic_Mac_OS#Mac_OS_9 "wikilink")、[Windowsといった](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) で動作する。Audacityの[ソースコード](../Page/ソースコード.md "wikilink")は[GNU General Public License バージョン2](https://ja.wikipedia.org/wiki/GNU_General_Public_License#バージョン2 "wikilink") (GPLv2) でリリースされている。[グラフィカルユーザインターフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink") (GUI) は[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")を用いて作成されている。[SourceForge.net](../Page/SourceForge.net.md "wikilink")の2007年度マルチメディア部門最優秀プロジェクト賞を、コミュニティの投票によって受賞した。

## 特徴

Audacityには次のような特徴がある:

  - [WAV](../Page/WAV.md "wikilink")・[FLAC](../Page/FLAC.md "wikilink")・[Ogg Vorbis](https://ja.wikipedia.org/wiki/Ogg_Vorbis "wikilink")・[MP3](../Page/MP3.md "wikilink")（外部MP3[エンコーダ](https://ja.wikipedia.org/wiki/エンコーダ "wikilink")の[LAME](../Page/LAME.md "wikilink")を利用）といった[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")のインポート・エクスポート
  - 音声の録音・再生 - コンピュータに[マイクを繋いでのアナログ録音も可能](../Page/マイクロフォン.md "wikilink")
  - カット・コピー・ペーストによる直感的な編集 - アンドゥ（操作の取り消し）の回数は無制限
  - [マルチトラックの](https://ja.wikipedia.org/wiki/マルチトラックレコーダー "wikilink")[ミキシング](../Page/ミキシング.md "wikilink")
  - デジタルエフェクト - プリセットエフェクトのほかに汎用性の高い[VST](https://ja.wikipedia.org/wiki/VST "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")が利用可能
  - 振幅[エンベロープ](https://ja.wikipedia.org/wiki/エンベロープ "wikilink")の編集
  - [ノイズ](../Page/ノイズ.md "wikilink")除去フィルタリング機能
  - [高速フーリエ変換](../Page/高速フーリエ変換.md "wikilink")を利用したスペクトラム分析
  - 最大チャネル数 16、最大[サンプリングレート](../Page/サンプリング周波数.md "wikilink") 192 kHz、最大サンプルフォーマット 32 bit浮動小数点
  - 多言語対応 - 日本語も Nihongo として選べる（ただし、ヘルプは英語）

など

### エクスポート

一度取り込んだ音声データは専用フォーマットの「Audacityプロジェクト (.aup)」フォーマットで保存できる。このフォーマットで保存すると編集履歴が保たれる。ここからWAVや[AIFF](../Page/AIFF.md "wikilink")など・MP3・Ogg Vorbisへのエクスポートが可能。

  - Ogg Vorbis - エンコーディングはVBR（Variable Bit Rate, 可変[ビットレート](../Page/ビット毎秒.md "wikilink")）で、Q0からQ10までを選択可能
  - LAMEによるMP3へのエンコーディングでは、VBRは選べない

（いずれもversion 1.3b時点）

（version 1.33bでエクスポートに変更があった模様。出力はエクスポートで統一され、更に保存形式とオプションが追加され、ビットレートの変更などが可能になった）

### エラーについて

日本語名のファイルや、文字化けしたファイルをインポートし（アーティスト名などのタグも含む）、aup形式で保存した場合、 not-well-formed（3行目）エラーがでる。 これは、XMLに由来するものであり、回避方法は、aupファイルをメモ帳等で開き、3行目の文字化け部分をカットすることで直る。

## 関連項目

  - [マルチトラック・レコーダー](../Page/マルチトラック・レコーダー.md "wikilink")
  - [波形編集ソフトウェア](https://ja.wikipedia.org/wiki/波形編集ソフトウェア "wikilink")

## 外部リンク

  - [公式サイト](https://www.audacityteam.org/)
  - [Audacity Wiki](https://wiki.audacityteam.org/wiki/Audacity_Wiki_Home_Page) - [MediaWiki](../Page/MediaWiki.md "wikilink")を利用したWiki。現在はほぼ英語。ライセンスは[cc-by-2.5](../Page/クリエイティブ・コモンズ.md "wikilink")
  - [Editing audio in Linux:Audacity](https://arstechnica.com/features/2005/10/linux-audio/3/)（英語）

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:音声処理ソフト](https://ja.wikipedia.org/wiki/Category:音声処理ソフト "wikilink") [Category:2000年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2000年のソフトウェア "wikilink")