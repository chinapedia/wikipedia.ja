> この記事は[IE Tab](https://ja.wikipedia.org/wiki/IE_Tab)から翻訳されています。


**IE Tab**は、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")、[Flock](../Page/Flock.md "wikilink")、[SeaMonkey](../Page/SeaMonkey.md "wikilink")、[Google Chromeで動作するソフトウェア](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")（拡張機能）である。

## 概要

IE Tabを利用するとFirefoxなど他のブラウザの中で[Internet Explorerの](../Page/Internet_Explorer.md "wikilink")[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")を利用することが出来るようになる。この機能を利用すると、直接そのブラウザからWindows UpdateなどIEでしか動作しないページを閲覧できるようになり、Internet Explorerを利用中のブラウザとは別に起動する必要がなくなる。

IE Tabはシステム内からIEコンポーネントを呼び出し、[拡張機能内部でウェブページの表示領域いっぱいに](../Page/拡張機能_\(Mozilla\).md "wikilink")`application/ietab`オブジェクトを埋め込み[IEのブラウザエンジンを利用した表示を可能とする](../Page/Trident.md "wikilink")。このため、IEのブラウザエンジンを通じて表示されたページの履歴やキャッシュはIEに保存される仕様になっていたり、オブジェクト埋め込みと言う形式を取っているためIEで表示した領域は一般的な拡張機能による追加効果を得られない欠点があったりと、その機能はIEのブラウザエンジンによる使用をメインとしたものでなく補助として用いるのに適した仕様となっている。また、これは[IEコンポーネントブラウザ](../Page/IEコンポーネントブラウザ.md "wikilink")のような動作をする拡張機能であり、[Windowsのシステムに依存するため動作環境は当然Windowsに限定される](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[Linux](../Page/Linux.md "wikilink")などでもインストールはできるが、IEでページを開こうとしても未定義URLとして白紙の画面を返すのみである。

後にBlackfish Softwareによってオリジナルのソースコードを元にIE Tab2が作成され、Google Chromeへの移植版が開発されている。Firefoxとインターフェースの仕様が異なるGoogle Chrome版では、ページ内にIE Tabの表示領域と専用のアドレスバーを表示し、専用のアドレスバーにURIを入力して表示する。

## IE View

IE ViewはIE Tabの原型となるFirefox拡張機能である。[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")で動作。閲覧中ページのURLを[コンテキストメニュー](../Page/コンテキストメニュー.md "wikilink")からInternet Explorerに送り、ページをIEで閲覧させるようにするのを目的とする。URLを送って起動と同時に指定ページをダイレクトで開かせる仕組みなので、アドレスをコピーするなどと言った煩わしい操作を省略することができる。アドレスをあらかじめ登録しておけば、URLを開くと同時にIEへとアドレスを送ると言うことも可能。この機能はIE Tabにも引き継がれており、IE TabではURLを開くと同時にURLを送るだけでなくブラウザエンジンをIEへ切り替えることも出来るようになっている。

ちなみにURLを送るブラウザはデフォルトでIEとなっているが、設定を変更することでIEコンポーネントブラウザなど任意のブラウザにすることも可能である。また、このIE Viewを元にOperaViewやSafari Viewという拡張機能も作成されている。これは、IE Viewと同じようにして[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")や[Safari](../Page/Safari.md "wikilink")へURLを送るためのものだが、別拡張として扱われるようにしているためIE Viewとの併用も可能である。

## 関連項目

  - [Flock](../Page/Flock.md "wikilink")
  - [Internet Explorer](../Page/Internet_Explorer.md "wikilink")
  - [IEコンポーネントブラウザ](../Page/IEコンポーネントブラウザ.md "wikilink")
  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")
  - [SeaMonkey](../Page/SeaMonkey.md "wikilink")
  - [Trident](../Page/Trident.md "wikilink")

## 外部リンク

  - [IE Tab.net（IE Tab2公式ページ）](http://www.ietab.net/)
      - [IE Tab2](https://addons.mozilla.org/firefox/92382) - for FireFox 3.6+
      - [Chrome版IE Tab](https://chrome.google.com/extensions/detail/hehijbfgiekmjfkfjpbkbammjbdenadd)
  - [mozdev.org - ietab: index（IE Tabオリジナル版開発元）](http://ietab.mozdev.org/)
      - [Mozilla-Add-Onsの配布元ページ](https://addons.mozilla.org/firefox/1419/)
  - [IE View - Launch pages in IE from Firefox（IE View開発元）](http://ieview.mozdev.org/)
  - [mozdev.org - operaview: index（OperaView開発元）](http://operaview.mozdev.org/)

[Category:拡張機能_(Mozilla)](https://ja.wikipedia.org/wiki/Category:拡張機能_\(Mozilla\) "wikilink") [Category:IEコンポーネントブラウザ](https://ja.wikipedia.org/wiki/Category:IEコンポーネントブラウザ "wikilink")