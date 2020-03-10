> この記事は[J Sharp](https://ja.wikipedia.org/wiki/J_Sharp)から翻訳されています。


**J\#**は、[サンマイクロシステムズ](https://ja.wikipedia.org/wiki/サンマイクロシステムズ "wikilink")の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[J++といった言語向けに開発された既存のアプリケーションやノウハウを](https://ja.wikipedia.org/wiki/Microsoft_Visual_J++ "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[.NET Framework上に移植するための](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。J\#ではJavaの[バイトコード](../Page/バイトコード.md "wikilink")を処理の対象にすることができる。つまり、サードパーティ製ライブラリのソースコードが入手できなかったとしてもそれらを利用可能である。J\#は、[インド](../Page/インド.md "wikilink")の[HITEC市](https://ja.wikipedia.org/wiki/HITEC市 "wikilink")にあるマイクロソフトインド開発局で開発された\[1\]。

## J\#エディタ

Javaと違い、Visual Studioやスタンドアロン型のVisual J\# Express Editionは、[Windows環境でのみ動作するバイナリコードの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[アプレット](https://ja.wikipedia.org/wiki/アプレット "wikilink")やアプリケーションのみを作成できる。つまり、拡張子が.exeの実行ファイルやコンソールアプリケーション、そして拡張子が.dllのクラスファイルである。Visual J\#の未コンパイルJavaファイルは、.jsl形式である。

## J\#とJavaの基本的な違い

JavaとJ\#とで全般的な文法はほぼ同じであるが、.NET環境をサポートするためにJavaの規格には適合していない。たとえば、.NETプロパティを普段のJavaBeanのクラスで使うためには、getXxxメソッドやsetXxxメソッドのようなget/setのプレフィックスを備える必要があり，メソッドに対してJavadocのような注釈を添える。

``` java
    /** @beanproperty    */
```

もしget/setで始まるプライベート変数を有するなら，get/setで始まらない別の名称に変更しなければならない。 J\#はJavaのソースコードから.classファイルのような[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")にコンパイルしないし、Javaアプレット開発環境やWebブラウザ上でアプレットを実行する機能もない。しかしながら、ActiveXオブジェクトとしてホストするためのラッパー(Microsoft J\# Browser Controls)は提供されている。 最後に、[Java Native Interface](https://ja.wikipedia.org/wiki/Java_Native_Interface "wikilink") (JNI) と[Raw Native Interface](https://ja.wikipedia.org/wiki/Raw_Native_Interface "wikilink") (RNI) については、[P/Invoke](https://ja.wikipedia.org/wiki/P/Invoke "wikilink")（プラットフォーム呼び出し）で代用する。J\#は[Java RMIをサポートしない](https://ja.wikipedia.org/wiki/Java_Remote_Method_Invocation "wikilink")。

言い換えると、Javaが[中間コード](https://ja.wikipedia.org/wiki/中間コード "wikilink")をJava仮想マシン上で動作させるのと同じように、J\#は[共通中間言語](../Page/共通中間言語.md "wikilink")にいったんコンパイルされた中間コードを.NET Framework上で実行する。

## J\#の将来

J\#は、[C\#や](../Page/C_Sharp.md "wikilink")[VB.NETに負けないプログラミング言語であるとは一般的に考えられていない](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")。そしてほか言語になされるのと同じくらいのサポート、サンプルの提供、またはアップデートもなされていない。この事実にも関わらず、J\#は.NETで利用可能な言語であり、[共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink")が備える機能をほとんど利用できる。

2007年にマイクロソフトのJ\#開発チームは、J\#の将来について2つの重要なアナウンスをおこなった\[2\]。

  - マイクロソフトは64ビットランタイムをサポートして欲しいという顧客の要求に応えるため、Visual J\#のアップデートバージョンを提供する。それはJ\#2.0 Second Editionと呼ばれる64ビット環境の再頒布できるバージョンを含むはずである\[3\]\[4\]。
  - J\#とJava Language Conversion Assistantを、Visual Studioの将来のバージョンに含めないこと。それは現在のJ\#の特徴が顧客の要求へあわなくなり、J\#の利用が衰えたためである。Visual Studio 2005として出荷されている現在のバージョンは、[製品ライフサイクル戦略によって](https://ja.wikipedia.org/wiki/商品ライフサイクルマネジメント "wikilink")2015年までサポートされる\[5\]。

## 脚注

## 関連項目

  - [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")
  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [Microsoft Visual J++](https://ja.wikipedia.org/wiki/Microsoft_Visual_J++ "wikilink")
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [IKVM.NET](https://ja.wikipedia.org/wiki/IKVM.NET "wikilink")

{{.NET}}

[Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:Microsoft_Visual_Studio](https://ja.wikipedia.org/wiki/Category:Microsoft_Visual_Studio "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink")

1.
2.  [Announcements on J\# Future](https://msdn.microsoft.com/en-us/vstudio/bb188593.aspx)
3.  [Download Microsoft Visual J\#® 2.0 再頒布可能パッケージ Second Edition (x86) from Official Microsoft Download Center](https://www.microsoft.com/ja-jp/download/details.aspx?id=18084)
4.  [Download Microsoft Visual J\#® 2.0 再頒布可能パッケージ Second Edition (x64) from Official Microsoft Download Center](https://www.microsoft.com/ja-jp/download/details.aspx?id=15468)
5.