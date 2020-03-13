> この記事は[JavaXPCOM](https://ja.wikipedia.org/wiki/JavaXPCOM)から翻訳されています。


**JavaXPCOM**は、[XPCOM](../Page/XPCOM.md "wikilink")の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")[バインディングである](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")。[XULRunner](../Page/XULRunner.md "wikilink")に同梱されており、これを使用することでJavaからXPCOMコンポーネントの利用が可能となる。

## 利用方法

XULRunnerがインストールされていることが前提となる。ここでは、/opt/xulrunner/1.8.0.4にインストールされた[Linux](../Page/Linux.md "wikilink")版を元に、例示する。

### CLASSPATHの設定

[CLASSPATHにMozillaInterfaces](https://ja.wikipedia.org/wiki/クラスパス "wikilink").jarを追加する。

`export CLASSPATH=$CLASSPATH:/opt/xulrunner/1.8.0.4/xulrunner/sdk/lib/MozillaInterfaces.jar`

### コンポーネントの利用

#### インポート

インポートするパッケージは、'org.mozilla.xpcom.\*'となる。XULRunnerには、1,000を越えるコンポーネントが含まれるが、すべてこのパッケージに属している。

``` java
import org.mozilla.xpcom.*;
```

#### GREパスの取得

GREパス、つまりXULRunnerのインストール場所を取得する。取得したパスは、XPCOMの初期化時に使用する。

``` java
GREVersionRange[] range = new GREVersionRange[1];
range[0] = new GREVersionRange("1.8", true, "1.9+", true);
Properties props = null;

File grePath = null;
try {
    grePath = Mozilla.getGREPathWithProperties(range, props);
} catch (FileNotFoundException e) { }

if (grePath == null) {
    System.out.println("found no GRE PATH");
    return;
}
```

#### Mozillaオブジェクトの取得

Mozillaオブジェクトを取得する。

``` java
Mozilla mozilla = Mozilla.getInstance();
```

#### XPCOMの初期化

``` java
try {
    mozilla.initialize(grePath);
    mozilla.initXPCOM(grePath, null);
} catch (IllegalArgumentException ex) {
    System.out.println("no javaxpcom.jar found in given path");
    return;
} catch (Exception ex) {
    System.out.println("initXPCOM failed");
    ex.printStackTrace();
    return;
}
```

#### コンポーネントマネージャの取得

``` java
nsIComponentManager componentManager = mozilla.getComponentManager();
```

#### XPCOMコンポーネントの取得

Contract IDを使って、コンポーネントをインスタンス化する。

``` java
nsIMutableArray array = (nsIMutableArray)componentManager.createInstanceByContractID(
        "@mozilla.org/array;1",
        null,
        nsIMutableArray.NS_IMUTABLEARRAY_IID);
```

#### XPCOMのシャットダウン

``` java
mozilla.shutdownXPCOM(null);
```

## 関連項目

  - [XULRunner](../Page/XULRunner.md "wikilink")
  - [XUL](../Page/XUL.md "wikilink")
  - [XPCOM](../Page/XPCOM.md "wikilink")

## 外部リンク

  - [JavaXPCOMトップページ](http://developer.mozilla.org/ja/docs/JavaXPCOM)

[Category:Mozilla](https://ja.wikipedia.org/wiki/Category:Mozilla "wikilink")