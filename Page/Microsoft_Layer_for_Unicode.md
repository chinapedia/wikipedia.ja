> この記事は[Microsoft Layer for Unicode](https://ja.wikipedia.org/wiki/Microsoft_Layer_for_Unicode)から翻訳されています。


**Microsoft Layer for Unicode** (**MSLU**)は、[Windows 9x系](https://ja.wikipedia.org/wiki/Windows_9x系 "wikilink") (95/98/Me)で[Unicode](../Page/Unicode.md "wikilink")対応の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")を実行するための[マイクロソフト](../Page/マイクロソフト.md "wikilink")製の[ライブラリ](../Page/ライブラリ.md "wikilink")である。**UnicoWS** (Unicode for Windows 95/98/Me Systems)やUNICOWS.DLLなどといった名称でも知られている。

マイクロソフトは、MSLUのことを「Windows 95/98/ME上のWin32 APIのレイヤーであり、Unicodeを用いたプログラムだけを書いても全てのプラットフォーム上で動作させることができる」と記述している。[1](http://www.microsoft.com/globaldev/handson/dev/mslu_announce.mspx) MSLUが登場する前は9x系のWindowsに対応しつつ、Unicode対応にもするには、Unicodeを使ったものとそうでないもの（Windows 9x用）の2つをビルドする必要があった。

MSLUは[2001年](../Page/2001年.md "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")に発表され、同年[7月](https://ja.wikipedia.org/wiki/7月 "wikilink")の版の[Microsoft Platform SDKから収録され利用可能となったが](../Page/Microsoft_Windows_SDK.md "wikilink")、この頃は既にWindows 9x系の絶頂期を過ぎた後であった。

## 動作

[Windows APIでは](https://ja.wikipedia.org/wiki/Windows_API "wikilink")、普通**A** （[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink"): ANSIコードページに基づく[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")）版と**W** （[ワイド文字](../Page/ワイド文字.md "wikilink")）版の2つの関数が用意されている。[Windows 9x系では](https://ja.wikipedia.org/wiki/Windows_9x "wikilink")、A版のみが実装され、W版を呼び出そうとすると、極一部を除いて実装されていない旨のエラーになる。一方[Windows NT系では](../Page/Windows_NT系.md "wikilink")、A版とW版の両方が実装されている（ただし内部で直接実装されているのはW版であり、A版はW版の呼び出しへ変換する[サンク](https://ja.wikipedia.org/wiki/サンク "wikilink")となっている）。

リンクの際、KERNEL32.LIBやADVAPI32.LIBなどWindows APIのライブラリよりも先にUNICOWS.LIBを指定すると、[リンカはUNICOWS](../Page/リンケージエディタ.md "wikilink").LIBからシンボルを解決するようになる。

そして実行時、最初にワイド文字版の関数が呼ばれたとき、UNICOWS.LIB内へ実行が移る。このとき9x系のWindowsで実行していれば、UNICOWS.DLLを読み込みDLL内のサンク[スタブ](https://ja.wikipedia.org/wiki/スタブ "wikilink")へ実行を移す。このサンクスタブはワイド文字引数をANSI文字列へ変換してネイティブな**A**版APIを呼び出す役割を果たす。逆に**W**版APIを持つNT系のWindows上で実行していた場合、メモリ上に存在するインポートテーブルを書き換え、以後余分な負荷をかけずにW版の関数を呼び出せるようにする。

このようにするわけは、MSLUをリンクしたアプリケーションソフトウェアが、9x系のWindowsで実行したときのみUNICOWS.DLLを必要となるようにするためである。また、NT系で実行したときに、余分な手間がかかる機会を最初の1回の関数呼出のときだけに留める効果もある。

## 外部リンク

断りの無いものは全て英語である。

  - [Official announcement of availability.](http://www.microsoft.com/globaldev/handson/dev/mslu_announce.mspx)
  - [MSDN Magazine article describing MSLU](http://msdn.microsoft.com/msdnmag/issues/01/10/MSLU)
  - [MSDN programming reference pages](http://msdn.microsoft.com/library/en-us/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp)
  - [Michael Kaplan's blog entries about MSLU internals](http://blogs.msdn.com/michkap/archive/category/7995.aspx)
  - [Download of MSLU redistributable (UNICOWS.DLL)](http://go.microsoft.com/fwlink/?LinkId=14851)
  - [Usenet discussion group: microsoft.public.platformsdk.mslayerforunicode](http://groups.google.com/group/microsoft.public.platformsdk.mslayerforunicode?hl=en)
  - [Known bugs in each released MSLU version](http://www.trigeminal.com/usenet/usenet035.asp) — マイクロソフト内のMSLUの主要開発者が管理している。
  - [UNICODEプログラムの作り方](http://www.honet.ne.jp/~tri/program/unicows01.html) — （日本語）

### オープンソースの代替品

  - [libunicows](http://libunicows.sourceforge.net/) — UNICOWS.LIBの代替のみ。[MIT Licenseでライセンスされている](../Page/MIT_License.md "wikilink")。実行時にマイクロソフトのUNICOWS.DLLか次のOPENCOW.DLLが必要。
  - [Opencow: Open Layer for Unicode](http://opencow.sourceforge.net/) — DLLとLIBの実装。旧名MZLU。[MPL](../Page/Mozilla_Public_License.md "wikilink") 1.1/[GPL](../Page/GNU_General_Public_License.md "wikilink") 2.0/[LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink") 2.1でライセンスされている。元々は[Mozilla](../Page/Mozilla.md "wikilink")プロジェクトの一環としてであった。

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink")