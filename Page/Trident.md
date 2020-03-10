> この記事は[Trident](https://ja.wikipedia.org/wiki/Trident)から翻訳されています。


**Trident** （トライデント）は [Internet Explorer](../Page/Internet_Explorer.md "wikilink") に搭載されている [HTML レンダリング エンジンの名称で](https://ja.wikipedia.org/wiki/HTMLレンダリングエンジン "wikilink")、ライブラリ ファイルの名称から **MSHTML** とも呼ばれている。

Internet Explorer 4.0 より導入されたもので、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 向けではアップデートを重ねているが、[Macintosh](../Page/Macintosh.md "wikilink") 向けの [Internet Explorer for Mac](https://ja.wikipedia.org/wiki/Internet_Explorer_for_Mac "wikilink") は次のバージョンの 5.0 で [Tasman](https://ja.wikipedia.org/wiki/Tasman "wikilink") に置き換えられた。Internet Explorer 7 とそれ以降に含まれるバージョンでは[ウェブ標準](https://ja.wikipedia.org/wiki/ウェブ標準 "wikilink")に準拠するように開発されている。

Trident は[ソフトウェア開発者](https://ja.wikipedia.org/wiki/ソフトウェア開発者 "wikilink")が自分のソフトウェアにウェブ ブラウズ機能を容易に追加できるよう、[ソフトウェア コンポーネントとして設計されている](../Page/ソフトウェアコンポーネント.md "wikilink")。Trident ではウェブ アクセスと編集のための [COM](../Page/Component_Object_Model.md "wikilink") インターフェイスが提供されている。例えば、Trident のウェブ ブラウザ コントロールを使用してウェブ ページを表示したり、表示中の各要素の値を取得・変更したり、表示したウェブ ページ上で発生したイベントを取得したりといった機能を組み込むことができる。Trident の機能は mshtml.dll というライブラリとリンクすることによって利用可能であり、[C++](../Page/C++.md "wikilink") や [.NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") といった COM をサポートする処理系から扱うことができる。

[Windows 10](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink") では、[Internet Explorer](../Page/Internet_Explorer.md "wikilink") に代わり [Microsoft Edge](https://ja.wikipedia.org/wiki/Microsoft_Edge "wikilink") が標準ブラウザとなった。Microsoft Edge は Trident から[フォークされた新たなレンダリング](../Page/フォーク_\(ソフトウェア開発\).md "wikilink") エンジン、[EdgeHTML](https://ja.wikipedia.org/wiki/EdgeHTML "wikilink") が採用され、Trident の開発は終了した。ただし、互換性維持のため [Internet Explorer](../Page/Internet_Explorer.md "wikilink") も引き続き提供され、セキュリティ アップデートは今後も行われる\[1\]\[2\]。

## バージョンの変遷

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Trident</p></td>
<td><p>MSHTML.dll</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>4.0.x</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>5.0.x</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>5.5.x</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>6.0.x</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>7.0.x</p></td>
</tr>
<tr class="odd">
<td><p>3.1[3]</p></td>
<td><p>7.0.x</p></td>
</tr>
<tr class="even">
<td><p>4.0</p></td>
<td><p>8.0.x</p></td>
</tr>
<tr class="odd">
<td><p>5.0</p></td>
<td><p>9.0.x</p></td>
</tr>
<tr class="even">
<td><p>6.0</p></td>
<td><p>10.0.x</p></td>
</tr>
<tr class="odd">
<td><p>7.0</p></td>
<td><p>11.0.x</p></td>
</tr>
</tbody>
</table>

## Trident 使用製品

Trident は標準で Windows に含まれる [Windows Media Player](https://ja.wikipedia.org/wiki/Windows_Media_Player "wikilink") などのアプリケーションのインターネット対応に使用されている。[Internet Explorer 7](https://ja.wikipedia.org/wiki/Internet_Explorer_7 "wikilink") がリリースされるまでは Windows のシェルでも採用されていて、[Windows Explorer](../Page/Windows_Explorer.md "wikilink") でも使用されていた。 マイクロソフトは [Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") や [Office](../Page/Microsoft_Office.md "wikilink")、[Windows Live Essentials](https://ja.wikipedia.org/wiki/Windows_Live_Essentials "wikilink") といった Windows 以外の製品でも採用しているが、[Microsoft Outlook](../Page/Microsoft_Outlook.md "wikilink") はバージョン 2007 以降 [Microsoft Word](../Page/Microsoft_Word.md "wikilink") の HTML レンダリング エンジンに切り替えた。

Trident は多くの場合 [IE コンポーネント ブラウザ](../Page/IEコンポーネントブラウザ.md "wikilink") というようなシェルを独自に開発したウェブ ブラウザの HTML レンダリング エンジンとして利用されている。 また、Internet Explorer に限らず、[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") といったマイクロソフト製品ではない[ウェブ ブラウザの拡張機能を利用する形で](../Page/ウェブブラウザ.md "wikilink") Trident を利用する [IE Tab](../Page/IE_Tab.md "wikilink") といったものも存在する。

マイクロソフト製品ではない Trident を利用したアプリケーションは例として以下のようなものがある。

  - [IE Tab](../Page/IE_Tab.md "wikilink") - Firefox などの Internet Explorer 以外のウェブ ブラウザの拡張機能で Trident を利用可能にする
  - [Real Player](https://ja.wikipedia.org/wiki/Real_Player "wikilink") - ビルトインのウェブ ブラウザでの採用
  - [Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink") - ビルトインとウェブ ブラウザ Bento Browser での採用

## 脚注

## 関連項目

  - [EdgeHTML](https://ja.wikipedia.org/wiki/EdgeHTML "wikilink")

[Category:IEコンポーネントブラウザ](https://ja.wikipedia.org/wiki/Category:IEコンポーネントブラウザ "wikilink") [Category:ウェブブラウザ](https://ja.wikipedia.org/wiki/Category:ウェブブラウザ "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:Internet_Explorer](https://ja.wikipedia.org/wiki/Category:Internet_Explorer "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")

1.
2.
3.  [Windows Phone 7 browser is based on Internet Explorer 7](http://www.neowin.net/news/windows-phone-7-browser-is-based-on-internet-explorer-7)