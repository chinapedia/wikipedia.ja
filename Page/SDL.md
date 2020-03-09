> この記事は[SDL](https://ja.wikipedia.org/wiki/SDL)から翻訳されています。


[Linux_kernel_and_OpenGL_video_games.svg](https://ja.wikipedia.org/wiki/File:Linux_kernel_and_OpenGL_video_games.svg "fig:Linux_kernel_and_OpenGL_video_games.svg") [thumb](https://ja.wikipedia.org/wiki/ファイル:SDL_Layers.svg "wikilink")

**SDL** (**Simple DirectMedia Layer**) は、[C言語](../Page/C言語.md "wikilink")で書かれた[クロスプラットフォーム](https://ja.wikipedia.org/wiki/クロスプラットフォーム "wikilink")のマルチメディアライブラリである。[グラフィック](https://ja.wikipedia.org/wiki/グラフィック "wikilink")の描画や[サウンド](https://ja.wikipedia.org/wiki/サウンド "wikilink")の再生などの[APIを提供する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、[Android](https://ja.wikipedia.org/wiki/Android "wikilink")を公式にサポートしている。SDL自身はC言語で書かれているが、[インタフェース部は](https://ja.wikipedia.org/wiki/インタフェース_\(情報技術\) "wikilink")[Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などの[プログラミング言語](../Page/プログラミング言語.md "wikilink")にも移植されている。SDLそのものは[OS間の違いを吸収するための最低限の抽象化しか提供しないが](../Page/オペレーティングシステム.md "wikilink")、SDLで使える[フォント](../Page/フォント.md "wikilink")や[ネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")、[スプライトなどの多数の](../Page/スプライト_\(映像技術\).md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")が公開されている。

## SDLが使用するAPI

SDLは画面の描画にOSによって異なるAPIを使う。Windowsでは[DirectDraw](https://ja.wikipedia.org/wiki/DirectDraw "wikilink")ないし[GDIが](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink")、Linuxでは[Xlib](https://ja.wikipedia.org/wiki/Xlib "wikilink")が使用される。ただし、[環境変数](https://ja.wikipedia.org/wiki/環境変数 "wikilink")「SDL_VIDEODRIVER」を変更すれば、[プログラムを書き換えることなく別のAPIを使って表示することも可能になっている](../Page/プログラム_\(コンピュータ\).md "wikilink")。[1](https://www.libsdl.org/faq.php?action=listentries&category=9#9) 同様に音声出力に使うAPIも環境変数で変更が可能。

## ギャラリー

<center>

| *[Freeciv](https://ja.wikipedia.org/wiki/Freeciv "wikilink")* <File:Unknown> horizons 3176.PNG| *[Unknown Horizons](https://ja.wikipedia.org/wiki/Unknown_Horizons "wikilink")* <File:0adcarthaginians.jpg> | *[0 A.D.](https://ja.wikipedia.org/wiki/0_A.D. "wikilink")* <File:Hwscreen.png>| *[Hedgewars](https://ja.wikipedia.org/wiki/Hedgewars "wikilink")* <File:Fretsonfirex1.jpg>| *[Frets on Fire](https://ja.wikipedia.org/wiki/Frets_on_Fire "wikilink")* <File:OpenTTD-0.7.1-de.png>|*[OpenTTD](https://ja.wikipedia.org/wiki/OpenTTD "wikilink")* <File:Wesnoth-1.6-5.jpg>|*[The Battle for Wesnoth](https://ja.wikipedia.org/wiki/The_Battle_for_Wesnoth "wikilink")* <File:OOlite_Mac_OS_X_screenshot.jpg>| *[Oolite](https://ja.wikipedia.org/wiki/Elite "wikilink")* <File:SMC15PromoShot.png>| *[Secret Maryo Chronicles](https://ja.wikipedia.org/wiki/Secret_Maryo_Chronicles "wikilink")* <File:Trine> - Knight Block.jpg| *[Trine](https://ja.wikipedia.org/wiki/Trine_\(Computerspiel\) "wikilink")*

</center>

## 補助ライブラリ

  - [SDL_image](https://www.libsdl.org/projects/SDL_image/)-さまざまな画像形式をサポートする。
  - [SDL_mixer](https://www.libsdl.org/projects/SDL_mixer/)-さまざまな音声形式をサポートする。
  - [SDL_net](https://www.libsdl.org/projects/SDL_net/)-ネットワークをサポートする。
  - [SDL_ttf](https://www.libsdl.org/projects/SDL_ttf/)-TrueTypeフォントをサポートする。
  - [SDL_rtf](https://www.libsdl.org/projects/SDL_rtf/)-Rich Text Format形式の文書をサポートする。
  - [SDL_gfx](http://cms.ferzkopp.net/index.php/software/13-sdl-gfx)-図形を描くための補助ライブラリ。

## 出典

<references/>

## 関連項目

  - [allegro](https://ja.wikipedia.org/wiki/allegro "wikilink")-マルチプラットフォーム開発用のライブラリ。

## 外部リンク

  -
[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:マルチメディア](https://ja.wikipedia.org/wiki/Category:マルチメディア "wikilink")