> この記事は[XPCOM](https://ja.wikipedia.org/wiki/XPCOM)から翻訳されています。


**XPCOM** (Cross Platform Component Object Model) は、[Mozilla](../Page/Mozilla.md "wikilink")プロジェクトにおいて開発されている[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")な[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")技術である。マイクロソフトの[Component Object Model](../Page/Component_Object_Model.md "wikilink") (MS COM) の[オープンソース](../Page/オープンソース.md "wikilink")実装に相当する。XPCOMは[C++](../Page/C++.md "wikilink")で実装されており、[Linux](../Page/Linux.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")という主要なプラットフォーム上で動作する。複数の[言語バインディング](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")が提供されており、C++の他に、[JavaScript](../Page/JavaScript.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Python](../Page/Python.md "wikilink")等の実装が存在する。XPCOMのインタフェースには、XPIDLと呼ばれる[インタフェース記述言語](../Page/インタフェース記述言語.md "wikilink") (IDL) が用いられている。

XPCOMにはコアとなるコンポーネントとクラス群が一緒に提供されている。例えば、ファイルやメモリの管理、[文字列](../Page/文字列.md "wikilink")や[配列](../Page/配列.md "wikilink")などの基本データ構造などがこれに含まれる。しかし、ほとんどのXPCOMコンポーネントは、コア以外の部分で提供されている。たとえば、[Gecko](../Page/Gecko.md "wikilink")レンダリングエンジンなどがこれにあたる。

## MonoのCOM相互運用

[MonoにおけるCOM相互運用はMS](../Page/Mono_\(ソフトウェア\).md "wikilink") COMおよびXPCOMを基盤としている\[1\]\[2\]。

## XUL/XPCOMベースのアドオン

Mozillaは[Firefoxや](../Page/Mozilla_Firefox.md "wikilink")[Thunderbirdにおいて](../Page/Mozilla_Thunderbird.md "wikilink")、[XUL](../Page/XUL.md "wikilink")/XPCOMを利用した[アドオン](https://ja.wikipedia.org/wiki/アドオン "wikilink")（[拡張機能](../Page/拡張機能_\(Mozilla\).md "wikilink")）の[SDKを提供してきたが](../Page/ソフトウェア開発キット.md "wikilink")、XUL/XPCOMベースのアドオンの段階的な廃止を表明している。Firefox Quantum 57 では全面的に廃止され\[3\]\[4\]\[5\]、。

Firefox Quantum の拡張機能では、XUL/XPCOMの代わりに [Microsoft Edge](https://ja.wikipedia.org/wiki/Microsoft_Edge "wikilink")、[Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")などでサポートされている WebExtensions\[6\] を使用する。

## 脚注

<references/>

## 関連項目

  - [Mozilla](../Page/Mozilla.md "wikilink")
  - [Gecko](../Page/Gecko.md "wikilink")
  - [XUL](../Page/XUL.md "wikilink")
  - [XULRunner](../Page/XULRunner.md "wikilink")
  - [XPConnect](https://ja.wikipedia.org/wiki/XPConnect "wikilink")（JavaScript用XPCOMバインディング）
  - [JavaXPCOM](../Page/JavaXPCOM.md "wikilink")（Java用XPCOMバインディング）
  - [PyXPCOM](https://ja.wikipedia.org/wiki/PyXPCOM "wikilink")（Python用XPCOMバインディング）
  - [RbXPCOM](https://ja.wikipedia.org/wiki/RbXPCOM "wikilink")（[Ruby](../Page/Ruby.md "wikilink")用XPCOMバインディング）
  - [PlXPCOM](https://ja.wikipedia.org/wiki/PlXPCOM "wikilink")（[Perl](../Page/Perl.md "wikilink")用XPCOMバインディング）

## 外部リンク

  - [XPCOM - Mozilla | MDN](https://developer.mozilla.org/ja/docs/Mozilla/Tech/XPCOM)
  - [XPCOM reference - Mozilla | MDN](https://developer.mozilla.org/ja/docs/Mozilla/Tech/XPCOM/Reference)
  - [mozdev books:8.XPCOM](http://books.mozdev.org/chapters/ch08.html)
  - [XPCOM](http://www.mozilla-japan.org/projects/xpcom/)
  - [XPCOM資料](http://www.mozilla-japan.org/catalog/architecture/xpcom/)
  - [Gecko Embedding API Reference](https://developer.mozilla.org/en-US/docs/Mozilla/Gecko/Embedding_Mozilla)

<!-- end list -->

  - [Gecko組み込みの基礎](http://kawaguchiyohkan.at.infoseek.co.jp/GeckoEmbeddingBasics/EmbeddingBasicsTOC.html)
  - [XPCOMリファレンス](http://wiki.fdiary.net/xul/?XPCOM%A5%EA%A5%D5%A5%A1%A5%EC%A5%F3%A5%B9)
  - [まじらもじら:埋め込み用API](http://www.symphonyinc.co.jp/mozilla/webbrowser-j.html)

<!-- end list -->

  - [dW:XPCOM 第1回 XPCOM入門](https://www.ibm.com/developerworks/jp/webservices/library/co-xpcom.html)
  - [dW:XPCOM 第2回 XPCOMコンポーネントの基本](https://www.ibm.com/developerworks/jp/webservices/library/co-xpcom2.html)
  - [dW:XPCOM 第3回 XPCOMのセットアップ](https://www.ibm.com/developerworks/jp/webservices/library/co-xpcom3.html)
  - [dW:XPCOM 第4回](https://www.ibm.com/developerworks/jp/webservices/library/co-xpcom4/)
  - [dW:XPCOM Part 5: Implementation](https://www.ibm.com/developerworks/webservices/library/co-xpcom5.html)

[Category:Mozilla](https://ja.wikipedia.org/wiki/Category:Mozilla "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.  [The Mono Runtime | Mono](https://www.mono-project.com/docs/advanced/runtime/)
2.  [COM Interop | Mono](https://www.mono-project.com/docs/advanced/com-interop/)
3.  [Firefox 57 (Quantum) for developers - Mozilla | MDN](https://developer.mozilla.org/ja/Firefox/Releases/57)
4.  [Firefox アドオン技術の現代化 | Firefox ヘルプ](https://support.mozilla.org/ja/kb/firefox-add-technology-modernizing/)
5.  [Porting a legacy Firefox extension | Extension Workshop](https://extensionworkshop.com/documentation/develop/porting-a-legacy-firefox-extension/)
6.  <https://developer.mozilla.org/ja/Add-ons/WebExtensions>