> この記事は[Observer パターン](https://ja.wikipedia.org/wiki/Observer_パターン)から翻訳されています。


** パターン**（オブザーバ・パターン）とは、[プログラム内の](../Page/プログラム_\(コンピュータ\).md "wikilink")[オブジェクトのイベント](../Page/オブジェクト_\(プログラミング\).md "wikilink")( 事象 )を他のオブジェクトへ通知する処理で使われる[デザインパターンの一種](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")。

通知するオブジェクト側が、通知されるオブジェクト側に観察（）される形になる事から、こう呼ばれる。

[出版-購読型モデル](../Page/出版-購読型モデル.md "wikilink")とも呼ばれる。[暗黙的呼び出し](https://ja.wikipedia.org/wiki/暗黙的呼び出し "wikilink")の原則と関係が深い。

分散イベント処理システムの実装にも使われる。言語によっては、このパターンで扱われる問題は言語が持つイベント処理構文で処理される。

## クラス図

このパターンの基本は、イベントを通知される側の1つ以上のオブジェクト（**オブザーバ 又**は **リスナー**と呼ぶ）を、通知する側（**サブジェクト**と呼ぶ）のオブジェクトに登録する事である。そして通知関数が、抽象メソッドになっている事が重要である。

以下に、その構造を[UMLクラス図で視覚化したものを示す](../Page/統一モデリング言語.md "wikilink")。

[ファイル:Observer-pattern-class-diagram.png](https://ja.wikipedia.org/wiki/ファイル:Observer-pattern-class-diagram.png "wikilink")

## 各クラスの解説

このパターンに登場する各インターフェース・メソッド・インターフェースの実装クラスを、以下で解説する。

### Subject

イベントを通知するオブジェクト側のインターフェース。1つ以上のObserver( イベントを通知されるオブジェクト側のインターフェース )の登録・削除・通知の関数書式の体裁を提供する。

以下の抽象メソッドを持つ:

  - *addObserver* - Subjectが持つ「 通知を受け取るObserver群 」に、新たなObserverを加える。
  - *deleteObserver* - 上述で加えられた物を削除する。
  - *notifyObservers* - Subjectが持つ「 通知を受け取るObserver群 」に、Observer::notify() を呼んでイベントを通知する。

上のUMLクラス図では、Subjectがインターフェースと実装クラスに分かれているが、パターン要件でない。インターフェースを使わずクラスを直接実装する事もある。

### ConcreteSubject

Subjectの実装クラス。通知対象であるObserver群を持つ。各Observerが受け取る通知に関する処理を司る。notifyObservers() を呼ぶと、Observer群の1つ以上にイベントを通知する。

### Observer

イベントを通知される側のインターフェース。以下の抽象メソッドを持つ:

  - *notify* - Observerにとっては通知を受け取る処理、このメソッドを呼ぶSubjectにとっては通知を送る処理、と言える。このメソッドの個数や各書式は、通知内容により様々である。

### ConcreteObserver

Observerの実装クラス。

## 典型的用法

  - ユーザーが何らかの操作をするなどの外部イベントを待つ。[イベント駆動型プログラミング](../Page/イベント駆動型プログラミング.md "wikilink")参照。
  - あるオブジェクトの属性値の変化を待つ。なお、複数の属性値の変化でコールバック関数を呼び出すようにしているとイベントの連鎖的発生を引き起こす。
  - メーリングリストで、何らかのイベント（新製品情報など）があったとき、購読者リストに登録している人にメッセージを送る。

Observer パターンは [Model View Controller](../Page/Model_View_Controller.md "wikilink") (MVC) パラダイムの実装に使われることも多い。MVC では、モデルとビューの連携に Observer パターンが使われる。通常、コントローラーがモデルの変化を検出し、ビュー（オブザーバ）に通知する。

## 擬似コード

### Python

以下の[擬似コード](../Page/擬似コード.md "wikilink")は [Python](../Page/Python.md "wikilink") 風文法で Observer パターンを記述したものである。

``` python
 class Listener:
     def __init__(self, name, subject):
         self.name = name
         subject.register(self)

     def update(self, event):
         print self.name, "received event", event

 class Subject:
     def __init__(self):
         self.listeners = []

     def register(self, listener):
         self.listeners.append(listener)

     def unregister(self, listener):
         self.listeners.remove(listener)

     def notify_listeners(self, event):
         for listener in self.listeners:
             listener.update(event)

 subject = Subject()
 listenerA = Listener("<listener A>", subject)
 listenerB = Listener("<listener B>", subject)
 # subject には2つのリスナーが登録されている。
 subject.notify_listeners ("<event 1>")
 # 出力:
 #     <listener A> received event <event 1>
 #     <listener B> received event <event 1>
```

### Java

ロックを避けるため、CopyOnWriteArraySetを使用する。

``` java
 public interface Listener {
     public void onEvent();
 }

 import java.util.concurrent.CopyOnWriteArraySet;

 public class Subject {
     private Set<Listener> listenerSet = new CopyOnWriteArraySet<Listener>();

     public void addListener(Listener listener) {
         listenerSet.add(listener);
     }

     private void notifyListeners() {
         for (Listener listener : listenerSet) {
             listener.onEvent();
         }
     }
 }
```

## 実装

Observer パターンは各種[ライブラリ](../Page/ライブラリ.md "wikilink")やシステムに実装されている。特に[GUIツールキットには必ず含まれる](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。

  - Java [Swing](../Page/Swing.md "wikilink") ライブラリは Observer パターンを多用している。
  - [Boost.Signals](http://www.boost.org/doc/html/signals.html) - C++ STL の拡張。signal/slot モデルを提供する。
  - [Qt](http://doc.trolltech.com/4.1/index.html) - C++ フレームワークの signal/slot モデル。
  - [libsigc++](http://libsigc.sourceforge.net) - C++ [シグナルプログラミング](https://ja.wikipedia.org/wiki/シグナルプログラミング "wikilink")・テンプレートライブラリ
  - [sigslot](http://sigslot.sourceforge.net/) - C++ Signal/Slot ライブラリ
  - [XLObject](http://xlobject.sourceforge.net/) - テンプレートベースの C++ signal/slot モデル
  - [GLib](../Page/GLib.md "wikilink") - [C言語](../Page/C言語.md "wikilink")でのオブジェクトと [signals](https://ja.wikipedia.org/wiki/シグナルプログラミング "wikilink")/[callbacks](../Page/コールバック_\(情報工学\).md "wikilink") の実装（他のプログラミング言語用の実装もある）
  - [Exploring the Observer Design Pattern](http://msdn2.microsoft.com/en-us/library/ms954621.aspx) - [C\#](../Page/C_Sharp.md "wikilink") と [Visual Basic .NET](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink") による実装。[delegates](https://ja.wikipedia.org/wiki/Delegate_\(.NET\) "wikilink") を利用。
  - [Using the Observer Pattern](http://ramblings.aaronballman.com/?p=288) - [REALbasic](https://ja.wikipedia.org/wiki/REALbasic "wikilink") による実装
  - [flash.events](http://livedocs.macromedia.com/flex/2/langref/flash/events/package-detail.html) - [ActionScript](../Page/ActionScript.md "wikilink") 3.0 でのパッケージ（ActionScript 2.0 の mx.events パッケージの後継）
  - [YUI Event utility](http://developer.yahoo.com/yui/event/) - カスタムイベントを Observer パターンで実装
  - [Py-notify](http://home.gna.org/py-notify/) - [Python](../Page/Python.md "wikilink") 実装

## 関連項目

  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")

## 外部リンク

  - [A sample implementation in .NET](http://www.codeproject.com/gen/design/applyingpatterns.asp)
  - [Observer Pattern in Java](http://www.javaworld.com/javaworld/javaqa/2001-05/04-qa-0525-observer.html)
  - [Observer Pattern implementation in JDK 1.4](http://java.sun.com/j2se/1.4.2/docs/api/java/util/Observable.html)
  - [Using the Observer Pattern in .NET](http://www.ondotnet.com/pub/a/dotnet/2005/01/03/binaryclock.html)
  - [Definition & UML diagram](http://www.dofactory.com/Patterns/PatternObserver.aspx)
  - [A discussion of fine-grained observers](http://kelly.anderson.name/patterns/observer/earlyobserverpattern.htm)

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink") [Category:認識](https://ja.wikipedia.org/wiki/Category:認識 "wikilink")