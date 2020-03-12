> この記事は[Gdi++](https://ja.wikipedia.org/wiki/Gdi++)から翻訳されています。


**gdi++**（じーでぃーあいぷらすぷらす）は、[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")/[XPにおいて](../Page/Microsoft_Windows_XP.md "wikilink")、[フォント](../Page/フォント.md "wikilink")[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")を置き換え、フォントの入れ替えなどを伴うことなく[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")のかかった滑らかな表示を実現する[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。このソフトは現在[オープンソース](../Page/オープンソース.md "wikilink")で公開され、作者のWebサイトよりダウンロードすることができる。名前の「++」は、開発最初期において、適用するアプリケーションのバイナリの "gdi32.dll" の文字を直接 "gdi++.dll" のように書き換えていたために、サイズが同じで見分けが付きやすい文字列として選ばれたことによるもの。

## 開発履歴

初期のバージョンでは、[GDIによりあらかじめ大きめのサイズで](../Page/Graphics_Device_Interface.md "wikilink")[ラスタライズ](../Page/ラスタライズ.md "wikilink")されたフォントを[縮小](https://ja.wikipedia.org/wiki/縮小 "wikilink")するという手法が取られていたが、現在ではレンダリングエンジンに[FreeType](../Page/FreeType.md "wikilink")を利用した派生版が有志の手によって開発されている。 また、最初期に用いられていたアプリケーションのバイナリを直接書き換える方法は、[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[フックによりレンダリングエンジンを置き換える方法へと変更された](../Page/フック_\(プログラミング\).md "wikilink")。

## 評価など

[Windows Vistaではシステムの標準フォントが](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[メイリオ](../Page/メイリオ.md "wikilink")に置き換えられ、システムフォントに[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")がかかるように改良されたが、gdi++はそれと類似したレンダリングを[Windows 2000や](../Page/Microsoft_Windows_2000.md "wikilink")[Windows XPで実現できるという点が評価され](../Page/Microsoft_Windows_XP.md "wikilink")、「先取り」という表現は適切ではない\[1\]ものの、2006年窓の杜大賞で「Windows Vista先取り賞」を獲得した\[2\]。

ただし、Windows Vista/Windows XP標準のClearType(アンチエイリアス機能)とgdi++の提供するアンチエイリアス機能は同等なものではない。 使用するフォントや個人の好みにもよるが、gdi++を用いたレンダリングはVistaでのメイリオフォントによるものよりも良好なレンダリング結果が得られる\[3\]、と評されている。

## 脚注

## 外部リンク

  - [gdi++](http://drwatson.nobody.jp/gdi++/)
  - [gdi++ wiki](http://www39.atwiki.jp/gdiplusplus/)
      - [gdi++(FreeType)](http://www39.atwiki.jp/gdiplusplus/pages/12.html)
      - [gdiplus2](http://www18.atwiki.jp/gdiplus2/)
      - [GDI++専用 Uploader](http://free.flop.jp/gdi++/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/Category:グラフィカルユーザインタフェース "wikilink")

1.  日本語版WindowsにおいてXP以前で標準となっているMSフォント(MS ゴシック/MS 明朝など)では、内蔵の[ビットマップフォント](https://ja.wikipedia.org/wiki/ビットマップフォント "wikilink")が優先的に使用され、[ClearType](../Page/ClearType.md "wikilink")の恩恵を受ける機会自体が稀な為にその様な印象を受けるが、ビットマップを内蔵しないフォントのレンダリングに関してWindows Vista/Windows XPの違いは無い
2.
3.  ClearTypeは横方向のみのアンチエイリアス処理であるが、gdi++では縦方向にもアンチエイリアス処理がかかることも関係している