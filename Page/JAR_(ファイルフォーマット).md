> この記事は[JAR \(ファイルフォーマット\)](https://ja.wikipedia.org/wiki/JAR_\(ファイルフォーマット\))から翻訳されています。


**JAR**（ジャー）または**Java Archive**（ジャバ アーカイブ）とは、コンパイルされた複数の[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")及びそれが使用する画像などの[リソースを一つにまとめ](../Page/計算資源.md "wikilink")[ZIP形式で](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")[圧縮されたファイル](../Page/データ圧縮.md "wikilink")、及びそれを出力するツールのこと。圧縮されたファイルの拡張子には、「.jar」が使われる。\[1\]

これによりJava[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")、[Javaアプレット](../Page/Javaアプレット.md "wikilink")、[ライブラリ](../Page/ライブラリ.md "wikilink")の配布が容易になる。アプレットにおいては、複数のJava[クラスファイルを一つにまとめ圧縮することで](../Page/クラス_\(コンピュータ\).md "wikilink")、全体のファイルの大きさを小さくするだけでなく[HTTPコネクションの数を減らせるので](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[ウェブサーバの負荷が減り](../Page/Webサーバ.md "wikilink")、アプレットの起動速度が向上する。

Javaで書かれていない[ネイティブ](https://ja.wikipedia.org/wiki/ネイティブ "wikilink")なプログラムやライブラリも[アーカイブにまとめられて配布されることが多いが](../Page/アーカイブ_\(コンピュータ\).md "wikilink")、それらは展開してインストールする必要がある。これに対して、実行時環境などのJavaのツールはJARを直接扱えるため、ユーザが明示的にJARを解凍する必要はない。

類似する[アーカイバ](https://ja.wikipedia.org/wiki/アーカイバ "wikilink")として[JSP](../Page/JavaServer_Pages.md "wikilink")/[Servlet](https://ja.wikipedia.org/wiki/Servlet "wikilink")などの[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")を一つの[アーカイブ](../Page/アーカイブ.md "wikilink")にまとめる[WAR](https://ja.wikipedia.org/wiki/WAR_\(アーカイバ\) "wikilink") (Web Application Archive)、[EJB](../Page/Enterprise_JavaBeans.md "wikilink") (Enterprise JavaBeans) アプリケーションを一つのアーカイブにまとめる[EAR](https://ja.wikipedia.org/wiki/EAR "wikilink") (Enterprise Archive) などがある。

JARを含むこれらのアーカイブの実態はZIPそのものであり、ZIPを扱えるツールで同じように扱うことができる。ただし、JAR, WAR, EAR にはMETA-INF/[ディレクトリ](../Page/ディレクトリ.md "wikilink")内に[マニフェスト](../Page/マニフェスト.md "wikilink")と呼ばれる[メタ情報が格納されている](../Page/メタデータ.md "wikilink")。このメタ情報はJARを扱うJavaのツールが解釈する。

また、このJARには[電子署名](../Page/電子署名.md "wikilink")をすることも可能である。これにより、[Javaアプレット](../Page/Javaアプレット.md "wikilink")などの[Javaアプリケーション](https://ja.wikipedia.org/wiki/Javaアプリケーション "wikilink")を実行するとき、ユーザがその署名を信用した場合に限り、[サンドボックスモデルではできなかったユーザのローカル環境にあるターゲット資源にアクセスすることが可能になる](../Page/サンドボックス_\(セキュリティ\).md "wikilink")。

## 脚注

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink")

1.  [JDK 6 Java Archive (JAR)-related APIs & Developer Guides](http://download.oracle.com/javase/6/docs/technotes/guides/jar/index.html)