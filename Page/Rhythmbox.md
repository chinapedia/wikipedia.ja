> この記事は[Rhythmbox](https://ja.wikipedia.org/wiki/Rhythmbox)から翻訳されています。


**Rhythmbox**（リズムボックス）は、デジタル音楽を再生・整理するオーディオプレーヤーである。

[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")の影響を受けている[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。[GNOME](../Page/GNOME.md "wikilink")デスクトップで[GStreamer](../Page/GStreamer.md "wikilink")メディアフレームワークを使って動くように設計されている。2007年11月現在活発に開発が行われている。

## 特徴

### 音楽再生

様々なデジタル音源の再生をサポートしている。最も一般的なものはローカルのコンピュータに保存されている音楽であり、ライブラリと呼ばれる。インターネットラジオとPodcastのストリーミング再生もサポートしている。また、[Replay Gain](https://ja.wikipedia.org/wiki/Replay_Gain "wikilink") 標準をサポートしている。

ライブラリ内の音楽の検索や並べ替え、プレイリストのグループ化や整理も可能である。カスタマイズした規則に従って自動的に更新される「スマートプレイリスト」を作ることも出来る。シャッフル（ランダム）モードやリピートモードでの再生も可能である。

曲目のレーティング（順位付け）もサポートしており、高いレーティングがついた曲目をシャッフルモードで高頻度で再生することも出来る。自動レーティングも選択出来る。

### 音楽インポート

  - 音楽CDの[リッピング](../Page/リッピング.md "wikilink")（オプションの[Sound Juicerパッケージが必要](https://ja.wikipedia.org/wiki/Sound_Juicer "wikilink"))）
  - さまざまなオーディオフォーマット（[GStreamerによる](https://ja.wikipedia.org/wiki/Gstreamer "wikilink")）
  - [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")サポート（実験的）
  - バージョン3.0より作業の進行状況を知らせる表示機能がトラックリストの下に加わった。\[1\]

### 音楽CD作成

バージョン0.9以降でプレイリストから[音楽CDを作成できるようになった](../Page/CD-DA.md "wikilink")。

### アルバムカバーディスプレイ

バージョン0.9.5以降で再生中の曲のアートワーク（[CDジャケット](https://ja.wikipedia.org/wiki/CDジャケット "wikilink")の写真など）を表示できるようになった。ID3タグに埋め込まれたものを読み込むだけでなく、インターネットからアートワークを探すこともできる。

### 楽曲歌詞ディスプレイ

バージョン0.9.5以降で、再生中の歌の歌詞を表示できるようになった（ただし[leoslyrics](https://ja.wikipedia.org/wiki/leoslyrics "wikilink")などの歌詞データベースに登録されたものに限る)。

### Last.fm サポート

バージョン0.9.6以降で、再生した音楽の情報を[Last.fm](../Page/Last.fm.md "wikilink")のアカウントに送信できるようになった。さらにバージョン0.9.7以降でLast.fm音楽ストリームを利用できるようになった。

### Jamendo サポート

バージョン0.9.6以降で、自由な音楽ライブラリである[Jamendo](https://ja.wikipedia.org/wiki/Jamendo "wikilink")の閲覧と再生ができるようになった。

### DAAP 共有

バージョン0.10.0は[DAAPによる共有をサポートしている](https://ja.wikipedia.org/wiki/Digital_Audio_Access_Protocol "wikilink")。

### 統合

[thumb](https://ja.wikipedia.org/wiki/ファイル:GNOME-Music-Applet-screenshot.png "wikilink")

Rhythmboxは以下のように多くの外部プログラムやデバイスと統合・拡張できる。

  - [ファイルのコンテキストメニュー拡張](../Page/ファイル_\(GNOME\).md "wikilink")（バージョン0.8.8ではデフォルトでは無効になっている）
  - [XChat](https://ja.wikipedia.org/wiki/XChat "wikilink")（XChatプラグインを利用）[Rhythmbox XChat Announcer (Perl)](http://tim.codestorm.net/projects/xchat-rhythmbox/)
  - [Pidgin-Rhythmbox](http://jon.oberheide.org/projects/pidgin-rhythmbox/)は自動的に[Pidgin](../Page/Pidgin.md "wikilink")ユーザ情報に現在再生中の曲情報をアップデートする。
  - [Music Applet](http://www.kuliniewicz.org/music-applet/)（旧バージョンはRhythmbox Appletとして知られていた）は[GNOME](../Page/GNOME.md "wikilink")パネルからのRhythmboxプレイバックの操作を可能にするアプレットである。
  - Rhythmletも[gDesklets](https://ja.wikipedia.org/wiki/gDesklets "wikilink")の一種であり、アルバムのジャケット画像をローカルファイルや[Amazon.com](../Page/Amazon.com.md "wikilink")から取得し、表示する文字列やプレイバック操作を設定でき、編集可能な検索バーやレーティングを提供する。
  - SideCandyRhythmboxはgDeskletを元にしたRhythmboxコントロールとSideCandyを表示する。
  - Rhythmbox XSLT は音楽ライブラリを[ウェブページ](../Page/ウェブページ.md "wikilink")として表示可能にする。
  - Drivelは再生中の曲名を[LiveJournal](https://ja.wikipedia.org/wiki/LiveJournal "wikilink")のブログ・エントリーに表示する。
  - Rhythmbox Tune Publisher は再生中の曲名を、（Jabber World Mapで使われる）User Tune プロトコルを用いて[XMPPに表示する](../Page/Extensible_Messaging_and_Presence_Protocol.md "wikilink")。
  - Blue Remote は[Bluetooth](../Page/Bluetooth.md "wikilink")を内蔵した電話機からRhythmboxを操作可能にする。
  - [FoxyTunes](https://ja.wikipedia.org/wiki/FoxyTunes "wikilink")は[Mozilla Firefoxの拡張](../Page/Mozilla_Firefox.md "wikilink")（extension）であり、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")からのプレイバック操作を可能にする。
  - [Jamendo](https://ja.wikipedia.org/wiki/Jamendo "wikilink")や[Magnatune](https://ja.wikipedia.org/wiki/Magnatune "wikilink")上で[クリエイティブ・コモンズ・ライセンス](https://ja.wikipedia.org/wiki/クリエイティブ・コモンズ・ライセンス "wikilink")に従うアルバムを再生するためのプラグインがある。

### デバイス

Rhythmboxは再生デバイスの認識にLinux Hardware Abstraction Layer (HAL) を用いる。

## 脚注

<references/>

## 外部リンク

  -
  - [Alarm plugin for Rhythmbox](http://fabien.carrion.free.fr/Rhythmbox.html)

[Category:音楽ソフトウェア](https://ja.wikipedia.org/wiki/Category:音楽ソフトウェア "wikilink") [Category:メディアプレーヤーソフト](https://ja.wikipedia.org/wiki/Category:メディアプレーヤーソフト "wikilink") [Category:GTK+を使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:GTK+を使用するソフトウェア "wikilink") [Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink") [Category:2001年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2001年のソフトウェア "wikilink")

1.