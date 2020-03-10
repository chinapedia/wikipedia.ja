> この記事は[Java Remote Method Invocation](https://ja.wikipedia.org/wiki/Java_Remote_Method_Invocation)から翻訳されています。


'''Java Remote Method Invocation ''' [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (Java RMI) は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で書かれたプログラム間の[ORB](https://ja.wikipedia.org/wiki/Object_Request_Broker "wikilink")（オブジェクトリクエストブローカー）\[1\] であり、[RPCのオブジェクトに相当する機能を果たすためのJava](../Page/遠隔手続き呼出し.md "wikilink")[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

## 概要

  - 異なるJava仮想計算機にある[オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")の[メソッドを呼び出す仕組み](../Page/メソッド_\(計算機科学\).md "wikilink")（[分散オブジェクト](https://ja.wikipedia.org/wiki/分散オブジェクト "wikilink")技術）
  - RMIは[トランスポート層](../Page/トランスポート層.md "wikilink")などを見えなくする。⇒ [透過性](../Page/透過性_\(情報工学\).md "wikilink")
  - [ソケットによる通信](../Page/ソケット_\(BSD\).md "wikilink")

APIには二つの共通する実装がある。本来の実装は表現メカニズムを分類する[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")に依存している。したがって、それは一つのJVMからもう一つのJVMへと呼び出しを作ることだけをサポートする。このJavaのみによる実装の基礎をなすプロトコルは[JRMP](https://ja.wikipedia.org/wiki/JRMP "wikilink") (<em lang="en">Java Remote Method Protocol</em>) として知られている。非JVMコンテキストでのコード実行をサポートするために [CORBA](https://ja.wikipedia.org/wiki/CORBA "wikilink") (<em lang="en">Common Object Request Broker Architecture</em>) 対応が後から開発された。用語 **RMI** の使い方は単に、プログラミングインタフェースということを示すか、APIとJRMP両方を意味する一方、用語[RMI-IIOP](../Page/RMI-IIOP.md "wikilink")はRMIオーバーIIOPと読み、RMIインタフェースは[CORBA](https://ja.wikipedia.org/wiki/CORBA "wikilink")実装サポート機能性の多くを代表することを意味する。

本来のRMI APIは[HTTP転送のような異なる実装をいくぶん概括した](../Page/Hypertext_Transfer_Protocol.md "wikilink")。その上、CORBA対応で値渡しの機能を追加し、RMIインタフェースをサポートした。未だに、RMI-IIOPとJRMP実装はそれらのインタフェース内では完全に同一ではない。

このパッケージ名は **`java.rmi`** である。

## 関連項目

  - [直列化\#Java](https://ja.wikipedia.org/wiki/直列化#Java "wikilink")

## 脚注

## 外部リンク

  - [The Java RMI tutorial](http://java.sun.com/docs/books/tutorial/rmi/index.html) - Java チュートリアル

  - [Java Remote Method Invocation](http://java.sun.com/javase/ja/6/docs/ja/technotes/guides/rmi/index.html) - JDK ドキュメント 機能リファレンスガイド

  - [Java RMI 入門](https://docs.oracle.com/javase/jp/8/docs/technotes/guides/rmi/hello/hello-world.html)

  - \- Java Platform API 仕様

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:遠隔手続き呼出し](https://ja.wikipedia.org/wiki/Category:遠隔手続き呼出し "wikilink")

1.  [オブジェクト指向](../Page/オブジェクト指向.md "wikilink")と組み合わさった[RPC](../Page/遠隔手続き呼出し.md "wikilink") (Remote Procedure Call)