> この記事は[ \(Windows\)](https://ja.wikipedia.org/wiki/_\(Windows\))から翻訳されています。


**リソース** (resource) とは、[計算リソースのことであるが](../Page/計算資源.md "wikilink")、[Microsoft Windowsの用語としては](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、ある種のリソースのことを意味する。

Windowsでリソースと呼ばれるものには、「リソース」と「システムリソース」がある。

## リソース

リソースは、[実行ファイル](../Page/実行ファイル.md "wikilink")（EXE）や[ダイナミックリンクライブラリ](../Page/ダイナミックリンクライブラリ.md "wikilink")（DLL）に埋め込まれた読み込み専用の[データ](../Page/データ.md "wikilink")である。

[Windows APIには全てのアプリケーションのリソースに簡単にアクセスする方法を提供している](../Page/Windows_API.md "wikilink")。

### 種類

各リソースは型と名前を持ち、どちらも数値識別子か文字列である。

Windows には予め定義されたリソースの型として以下のものがある。

  - [カーソル](../Page/カーソル.md "wikilink")およびアニメーション動作するカーソル
  - [アイコン](../Page/アイコン.md "wikilink")
  - [ビットマップ](https://ja.wikipedia.org/wiki/ビットマップ "wikilink")
  - [ダイアログボックス](../Page/ダイアログボックス.md "wikilink")のテンプレート
  - [フォント](../Page/フォント.md "wikilink")
  - [HTML文書](../Page/HyperText_Markup_Language.md "wikilink")
  - [文字列](../Page/文字列.md "wikilink")とメッセージテンプレート
  - バージョン情報

プログラマはリソースの型を新たに定義することもできる。

### 使用法

Windows がプログラムファイルに対応して表示するアイコンは EXE ファイル内の最初のアイコンリソースである。EXEファイル内にアイコンリソースがない場合、標準のアイコンが表示される。

EXEファイルやDLLファイルに埋め込まれたリソースを編集できるエディタがいくつかある。一般にアプリケーション内の文字列を別の言語に変換するのに使ったり、アイコンやビットマップを変更するのに使ったりする。

### リソース・エディタ

  - [XN Resource Editor](http://www.wilsonc.demon.co.uk/d10resourceeditor.htm) ([オープンソース](../Page/オープンソース.md "wikilink"))
  - [Resource Hacker](http://www.angusj.com/resourcehacker/) ([フリーウェア](../Page/フリーウェア.md "wikilink"))
  - [Sato Icon Changer](https://ja.wikipedia.org/wiki/Sato_Icon_Changer "wikilink") ([フリーウェア](../Page/フリーウェア.md "wikilink")、アイコンリソースのみ変更可)
  - [Resource Tuner](http://www.heaventools.com/) ([シェアウェア](../Page/シェアウェア.md "wikilink"))

## システムリソース

システムリソースとは、[WindowsのコアコンポーネントであるKERNEL](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、USER、[GDIが使用するメモリ領域のことである](../Page/Graphics_Device_Interface.md "wikilink")。

[Windows NT系のOSではこの領域を](../Page/Windows_NT系.md "wikilink")[デスクトップヒープ](../Page/デスクトップヒープ.md "wikilink")もしくはデスクトップアプリケーションヒープと呼ぶ。

[Windows 9x系のOSに存在するシステムリソースは](../Page/Windows_9x系.md "wikilink")[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")やウインドウなどの情報を格納するUSERが128KB、フォントやビットマップ、アイコンなどの情報を格納するGDIが64KB割り当てられており、どちらか少ない方の全体の比率を指す。これが0%に近づくとフリーズを起こしやすくなったりウインドウを開くことが出来なくなることがあり、それがいわゆる「リソース不足」と呼ばれる現象である。

### ツール

  - [リソースメーター](https://ja.wikipedia.org/wiki/リソースメーター "wikilink")

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink")