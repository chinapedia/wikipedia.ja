> この記事は[Simulation RPG Construction](https://ja.wikipedia.org/wiki/Simulation_RPG_Construction)から翻訳されています。


**Simulation RPG Construction**（シミュレーション アールピージー コンストラクション）は、[シミュレーションRPG](https://ja.wikipedia.org/wiki/シミュレーションRPG "wikilink")を制作できる[Windows用の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[フリーウェア](../Page/フリーウェア.md "wikilink")。通称**SRC**。作者はKei。

## 概要

本作は、[フリーウェア](../Page/フリーウェア.md "wikilink")の[シミュレーションRPG](https://ja.wikipedia.org/wiki/シミュレーションRPG "wikilink")製作ツールである。なお、本作はあくまで[ゲームエンジン](../Page/ゲームエンジン.md "wikilink")であるため単体では動作しない。動作には別途[ランタイム](../Page/ランタイムライブラリ.md "wikilink")、画像ファイル、シナリオデータなどが必要となる。 現在のところ有力な製作支援ツールは無く、10年経った現在もゲームの製作には[メモ帳](https://ja.wikipedia.org/wiki/メモ帳 "wikilink")などのテキストエディタで行うのが一般的である。 そのため、ゲームの製作には[BASIC](../Page/BASIC.md "wikilink")程度のプログラミング知識が必要となり、ゲームの製作は決して簡単ではない。

歴史は古く、既に削除されているが1997年の初版リリース当初の謳い文句としては「**[バンプレスト](https://ja.wikipedia.org/wiki/バンプレスト "wikilink")の[スーパーロボット大戦シリーズ](../Page/スーパーロボット大戦シリーズ.md "wikilink")のようなゲームが制作できる**」というコンセプトであったが、SRCの主なユーザーである[二次創作](https://ja.wikipedia.org/wiki/二次創作 "wikilink")シナリオがグレーゾーンにある事もあり、上記の説明の通りに修正されていった。

## 本体

本体は**安定版**と**開発版**に分けられている。本体の開発には[Visual Basicが用いられている](../Page/Visual_Basic.md "wikilink")。

公式サイトにてダウンロードできるSRCのバージョンは以下の通りとなっている。

### 安定版

開発版で十分にテストされ、バグフィックスされたもの。バージョン番号の2桁目が偶数になっているものが安定版となる。

  - Ver2.2系列最新バージョン
    現在主流となっている安定版SRCの最新バージョン。
  - Ver2.0.34（2005年9月11日リリース）
    Ver2.0系列（前期安定版）の最終バージョン。
  - Ver2.0.32（2005年6月11日リリース）
    [ネイティブコードコンパイルを用いたバージョン](../Page/コンパイラ.md "wikilink")。
  - Ver1.6.61（2003年5月18日リリース）
    Ver1.6系列の最終バージョン。Ver2.2系列及びVer2.0系列はVer1.6系列とは互換性がなく、また現在もVer1.6系列のシナリオやデータが配布されていることから、需要はそれなりにある。
  - Ver1.6.45（2001年12月9日リリース）
    [DirectMusicが使用されていないSRCの最終バージョン](https://ja.wikipedia.org/wiki/DirectX "wikilink")。DirectMusicの関係でエラーが発生してしまう場合は、このバージョンを用いる必要がある。

### 開発版

次期安定版に向けて開発される本体。主に開発中の機能や変更機能の動作のテストが行なわれる。バージョン番号の2桁目が奇数になっているものは開発版となる。 配布されるデータやシナリオの中には、開発版で動作させることを前提とするものも存在する。

  - Ver2.4.0a（2012年11月25日リリース）
    現在の開発版の最終バージョン。
  - Ver2.1.16（2005年12月10日リリース）
    前期開発版の最終バージョン。

## シナリオ

SRCで動作するスクリプトは**シナリオ**と呼称される事が多い。これは、SRCで動作するゲームが本体に添付され、同時にダウンロードできた時代の名残である。 シナリオは通常[インターネット](../Page/インターネット.md "wikilink")上で無償配布されており、[公式サイト](http://www.src.jpn.org)などでリンク集を通じて入手できるものが多い。また、雑誌への掲載や[同人誌即売会](../Page/同人誌即売会.md "wikilink")での頒布などオフラインで配布されるものもある。

### ファイル構成

シナリオは主に以下の各種ファイルで構成される。

#### イベント

シナリオの根底となるデータファイル。[拡張子](../Page/拡張子.md "wikilink")は「.eve」。このファイルの中でイベントの設置、敵の配置などの設定を行なう。拡張子は違うが、実態は[テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")であるので、Windows標準のメモ帳でも編集が可能である。ただし、ファイルの大きさが膨大になりがちであり、Windows標準のメモ帳ではサイズ制限上編集できないこともあるので、他の[テキストエディタ](../Page/テキストエディタ.md "wikilink")を使用するのが望ましい。イベントファイルは後述するマップファイルと同一のフォルダに入れるのが原則とされているが、現在ではそれぞれ別々のフォルダに格納する方式が主流になっている。

#### サブルーチン

シナリオに組み込んで使用するファイル。拡張子は「.eve」であり、シナリオ同様テキストファイルであるためテキストエディタでの編集が可能。シナリオのシステムを拡充するために利用されている場合が多く、第三者が流用可能なようにして配布されているものも多い。 旧バージョンでは｢インクルード｣と呼ばれており、現在でもこちらの呼称を使用するユーザーは多い。

#### 画像

利用できる画像形式は[Bitmap形式](https://ja.wikipedia.org/wiki/Windowsビットマップ "wikilink")（.bmp）が基本となる。 演出などに使用する画像には[JPEG](../Page/JPEG.md "wikilink")、[PNG](../Page/Portable_Network_Graphics.md "wikilink")、[GIFの各形式が利用できる](../Page/Graphics_Interchange_Format.md "wikilink")。 また、[Flashを利用する事で限定的だが動画再生にも対応している](../Page/Adobe_Flash.md "wikilink")。 画像の種類には、マップ上でユニットをあらわす「ユニットアイコン」と「パイロットアイコン」、マップを表現するための「マップチップ」、アニメーションなどで一時的に表示される「カットイン」等がある。

#### データ

操作するキャラクターのステータスや攻撃／防御時の画面演出などを設定するファイル。 前述の通り、SRCの製作支援ソフトの類は現在ほとんど存在しない（公式ページにからリンクされているソフトもほとんどが最新版に対応していないため動作しない）ため、データは全てWindows標準のメモ帳などのテキストエディタで編集する以外にない。

#### マップ

シナリオに関連するマップのデータファイル。SRC本体付属のマップエディタから作成できる。拡張子は「.map」。

#### BGM/サウンド

シナリオで使用されるBGM。[MIDI](../Page/MIDI.md "wikilink")形式（.midi）、[WAVE](https://ja.wikipedia.org/wiki/WAVE "wikilink")形式（.wav）、[MP3](../Page/MP3.md "wikilink")形式（.mp3）（要プラグイン）が利用できる。

## 脚注・出典

<references/>

## 外部リンク

  - 公式サイト

:\*[SRC -Simulation RPG Construction-](http://www.src-srpg.jpn.org/)

  - リンク集

:\*[SRCオリ制作サポートwiki](http://www38.atwiki.jp/src_freematerial/pages/1.html)

:\*[SRC版権シナリオサポートwiki](http://www38.atwiki.jp/src_c_material/)

  - 開発サイト

:\*[SRC総合支援センター](http://www.gsc.ne.jp/)

:\*[ラノベSRC@Wiki](http://www4.atwiki.jp/99772200/)

:\*[未完成データを丸投げするデータサイト](http://www19.atpages.jp/phantom365/mikansei/)

:\*[アルファナイズドデータセンター](http://www7.atpages.jp/srcalfa/)

[Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:シミュレーションRPG](https://ja.wikipedia.org/wiki/Category:シミュレーションRPG "wikilink") [Category:ゲームエンジン](https://ja.wikipedia.org/wiki/Category:ゲームエンジン "wikilink") [Category:コンピュータゲーム制作ソフト](https://ja.wikipedia.org/wiki/Category:コンピュータゲーム制作ソフト "wikilink")