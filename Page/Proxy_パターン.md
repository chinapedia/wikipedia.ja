> この記事は[Proxy ](https://ja.wikipedia.org/wiki/Proxy_)から翻訳されています。


[thumbで表した](https://ja.wikipedia.org/wiki/ファイル:proxy_pattern_diagram.svg "wikilink") Proxy パターン\]\] **Proxy パターン**は、[プログラミングにおける](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")[デザインパターンの一種](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")。Proxy（プロキシ、代理人）とは、大まかに言えば、別の物のインタフェースとして機能するクラスである。その「別の物」とは何でもよく、ネットワーク接続だったり、メモリ上の大きなオブジェクトだったり、複製がコスト高あるいは不可能な何らかのリソースなどである。

Proxy パターンのよく知られている例として、[参照カウント](../Page/参照カウント.md "wikilink")付き[ポインタオブジェクトがある](../Page/ポインタ_\(プログラミング\).md "wikilink")。

複雑なオブジェクトの複数のコピーが必須となる状況では、Proxy パターンに [Flyweight パターンを加えることでメモリ使用量を抑えることができる](../Page/Flyweight_パターン.md "wikilink")。通常、複雑なオブジェクトのインスタンスは1つだけ生成し、プロキシオブジェクトを複数生成する。それらプロキシオブジェクトは唯一の複雑なオブジェクトへの参照を含む。プロキシへの操作は、オリジナルのオブジェクトにフォワードされる。プロキシオブジェクトが全て破棄されると、参照されていた複雑なオブジェクトの使用していたメモリも解放される。

## 例

### Virtual Proxy (Java)

以下の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の例は、"virtual proxy" パターンを示したものである。このプログラムは以下のように出力する。

`Loading    HiRes_10MB_Photo1`
`Displaying HiRes_10MB_Photo1`
`Loading    HiRes_10MB_Photo2`
`Displaying HiRes_10MB_Photo2`
`Displaying HiRes_10MB_Photo2`

`ProxyImage` クラスは、実際に必要になるまで時間のかかる画像ファイルのロードを遅延させる。ファイルが結局必要とされなかった場合、時間のかかるロードは全く行われずに済む。

``` java
import java.util.*;

interface Image {
    public void displayImage();
}

class RealImage implements Image {
    private String filename;
    public RealImage(String filename) {
        this.filename = filename;
        loadImageFromDisk();
    }

    private void loadImageFromDisk() {
        // 時間のかかる一連の操作
        // ...
        System.out.println("Loading   "+filename);
    }

    public void displayImage() { System.out.println("Displaying "+filename); }
}

class ProxyImage implements Image {
    private String filename;
    private Image image;

    public ProxyImage(String filename) { this.filename = filename; }
    public void displayImage() {
        if (image == null) {
            image = new RealImage(filename); // ロードはオンデマンドでのみ行われる
        }
        image.displayImage();
    }
}

class ProxyExample {
    public static void main(String[] args) {
        Image image1 = new ProxyImage("HiRes_10MB_Photo1");
        Image image2 = new ProxyImage("HiRes_10MB_Photo2");
        Image image3 = new ProxyImage("HiRes_10MB_Photo3");

        image1.displayImage(); // ロードが必要
        image2.displayImage(); // ロードが必要
        image2.displayImage(); // すでにロード済みなのでロード不要
        // image3の画像は一度もロードされない
    }
}
```

### Protection Proxy (C\#)

以下の[C\#の例では](../Page/C_Sharp.md "wikilink")、`RealClient` はアカウント番号を格納する。正しいパスワードを知っているユーザーだけが、このアカウント番号にアクセスできる。`RealClient` はパスワードを知っている `ProtectionProxy` で守られている。ユーザーがアカウント番号を得たい場合、まずプロキシがユーザーに対して認証を求め、ユーザーが正しいパスワードを入力したときだけプロキシが `RealClient` を呼び出してアカウント番号をユーザーに通知する。

この例では、正しいパスワードは **thePassword** である。

``` csharp
using System;

namespace ConsoleApplicationTest.FundamentalPatterns.ProtectionProxyPattern
{
    public interface IClient {
        string GetAccountNo();
    }

    public class RealClient : IClient {
        private string accountNo = "12345";
        public RealClient() {
            Console.WriteLine("RealClient: Initialized");
        }
        public string GetAccountNo() {
            Console.WriteLine("RealClient's AccountNo: " + accountNo);
            return accountNo;
        }
    }


    public class ProtectionProxy : IClient
    {
        private string password;  //秘密のパスワード
        RealClient client;

        public ProtectionProxy(string pwd) {
            Console.WriteLine("ProtectionProxy: Initialized");
            password = pwd;
            client = new RealClient();
        }

        // ユーザーを認証し、アカウント番号を返す
        public String GetAccountNo() {
            Console.Write("Password: ");
            string tmpPwd = Console.ReadLine();

            if (tmpPwd == password) {
                return client.GetAccountNo();
            } else {
                Console.WriteLine("ProtectionProxy: Illegal password!");
                return "";
            }
        }
    }

    class ProtectionProxyExample
    {
        [STAThread]
        public static void Main(string[] args) {
            IClient client = new ProtectionProxy("thePassword");
            Console.WriteLine();
            Console.WriteLine("main received: " + client.GetAccountNo());
            Console.WriteLine("\nPress any key to continue . . .");
            Console.Read();
        }
    }
}
```

## 関連項目

  - [Composite パターン](https://ja.wikipedia.org/wiki/Composite_パターン "wikilink")
  - [Decorator パターン](../Page/Decorator_パターン.md "wikilink")

## 外部リンク

  - [Proxy pattern in Java](http://wiki.java.net/bin/view/Javapedia/ProxyPattern)
  - [Proxy pattern in UML and in LePUS3 (a formal modelling language)](http://www.lepus.org.uk/ref/companion/Proxy.xml)
  - [Jt](http://www.fsw.com/Jt/Jt.htm) J2EE Pattern Oriented Framework
  - [Compositeパターン/Proxyパターン](http://itpro.nikkeibp.co.jp/article/COLUMN/20060113/227229/) ITpro、矢沢久雄

[Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink") [Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")