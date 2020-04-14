> この記事は[C++マネージ拡張](https://ja.wikipedia.org/wiki/C++マネージ拡張)から翻訳されています。


**C++マネージ拡張** (****, ****) は、[C++](../Page/C++.md "wikilink")で[.NET Frameworkアプリケーションを記述するための](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")によるC++の拡張である。これによって、C++で[ネイティブコード](https://ja.wikipedia.org/wiki/ネイティブコード "wikilink")だけでなく[共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink") (CLR) に向けた[アプリケーションを記述できる](../Page/アプリケーションソフトウェア.md "wikilink")。この拡張は、[2002年](../Page/2002年.md "wikilink")にリリースされた[Visual Studio .NET](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") (2002) に含まれる[Visual C++ .NET](../Page/Microsoft_Visual_C++.md "wikilink") (2002) に初めて搭載された。

なお、[2005年](../Page/2005年.md "wikilink")後半にリリースされたVisual Studio 2005では、より洗練された[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")という独立した後継言語が登場し、C++マネージ拡張は非推奨となった。さらにVisual Studio 2015では廃止され、C++/CLIへの移行が促されている\[1\]\[2\]。

マネージドC++およびC++/CLIで記述されたアプリケーションは、C\#など他の.NET言語同様に[共通中間言語](../Page/共通中間言語.md "wikilink") (CIL) と呼ばれる[中間言語](../Page/中間言語.md "wikilink")にコンパイルされる。「マネージ (Managed)」とは、.NET[仮想マシンによって管理されながら動作するという意味である](../Page/仮想機械.md "wikilink")。このため、[ガベージコレクタ](https://ja.wikipedia.org/wiki/ガベージコレクタ "wikilink")などのCLRの機能を利用することができ、[C\#や](../Page/C_Sharp.md "wikilink")[VB.NETなどといった](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink").NET言語のコードを呼び出したり呼び出されたりといた相互運用ができる。

しかし、必要に応じて1つのアセンブリ（EXE/DLL）に[ネイティブコードも混在できる点が](../Page/機械語.md "wikilink").NET言語の中でも特殊である。このような言語はマネージドC++およびC++/CLIのほかにはない。一般の.NET言語は[P/Invoke](https://ja.wikipedia.org/wiki/P/Invoke "wikilink")や[COMを通してC](../Page/Component_Object_Model.md "wikilink")++コードとやりとりする必要がある。このため、マネージドC++およびC++/CLIは[マネージコード](../Page/マネージコード.md "wikilink")とネイティブコードの橋渡しとしてしばしば利用される。すなわち、C/C++あるいはその他の言語で書かれたライブラリを.NET用で利用するラッパーライブラリを作ったり、その逆を作ったりするために用いられるのである。

マネージドC++は以下のコンパイラで使用できる。

  - Visual C++ .NET 2002および.NET 2003
    コンパイラオプション`/clr`
  - Visual C++ 2005以降から2013まで
    コンパイラオプション`/clr:OldSyntax`

## 関連項目

  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")

## 脚注

{{.NET}}

[Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink")

1.
2.  \[<https://msdn.microsoft.com/ja-jp/library/k8d11d4s(v=vs.140>).aspx -clr (共通言語ランタイムのコンパイル)\]