> この記事は[Chain of Responsibility パターン](https://ja.wikipedia.org/wiki/Chain_of_Responsibility_パターン)から翻訳されています。


**Chain-of-responsibility パターン**, **CoR** パターンは、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")設計における[デザインパターンの一つであり](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")、一つの[コマンドオブジェクトと一連の](../Page/Command_パターン.md "wikilink")**処理オブジェクト** (processing objects) から構成される。各処理オブジェクトは、処理できるコマンドオブジェクトの種類と、自身が処理できないコマンドオブジェクトをチェーン内の次の処理オブジェクトに渡す方法を記述する情報を保持する。また、新たな処理オブジェクトをチェーンの最後に追加する機構を備える。

標準的な chain-of-responsibility のモデルの派生ハンドラーが[ディスパッチャとして動作し](https://ja.wikipedia.org/wiki/:en:dynamic_dispatch "wikilink")、コマンドを様々な方向に送出できるようにすることで、いわば *tree of responsibility* を形成しているものもある。

また、これを再帰的に行うケースもあり、処理オブジェクトが上位の処理オブジェクトを、問題の一部を解決するコマンドとともに呼び出すこともある。こうした場合再帰はコマンドが処理されるか、全てのツリーを巡回するまで継続される。[XML](https://ja.wikipedia.org/wiki/XML "wikilink")のインタプリタ（パースはするが実行はしない）などがこの例に当てはまるだろう。

このパターンはプログラミングにおいてよく用いられる、疎結合性を促進させる方法である。

## 例

### Java

以下の [Java](https://ja.wikipedia.org/wiki/Java "wikilink") コードは、ロギングクラスの例を用いてこのパターンを示したものである。各ロギングハンドラーはログレベルで何らかのアクションを起こすべきかどうかを判断し、次のロギングハンドラーにメッセージを渡す。

出力：

`  Writing to debug output: Entering function y.`
`  Writing to debug output: Step1 completed.`
`  Sending via e-mail:      Step1 completed.`
`  Writing to debug output: An error has occurred.`
`  Sending via e-mail:      An error has occurred.`
`  Writing to stderr:       An error has occurred.`

この例はロギングクラスをこの方法で書くことを推奨するものではなく、また、CoR の「純粋な」実装では、ロガーがメッセージを処理した後に、その責任を後段に渡すことはない。この例では処理されるかどうかに関係なく、メッセージがチェーンの先に渡される。

``` java
import java.util.*;

abstract class Logger {
    public static final int ERROR = 3;
    public static final int NOTICE = 5;
    public static final int DEBUG = 7;
    private final int mask;
    protected Logger(int mask) { this.mask = mask; }

    // The next element in the chain of responsibility
    protected Logger next;
    public Logger setNext(Logger l) {
        next = l;
        return this;
    }

    public void message(String msg, int priority) {
        if (priority <= mask) {
            writeMessage(msg);
            if (next != null) {
                next.message(msg, priority);
            }
        }
    }

    abstract protected void writeMessage(String msg);

}

class StdoutLogger extends Logger {
    public StdoutLogger(int mask) { super(mask); }

    @Override
    protected void writeMessage(String msg) {
        System.out.println("Writting to stdout: " + msg);
    }
}

class EmailLogger extends Logger {
    public EmailLogger(int mask) { super(mask); }

    @Override
    protected void writeMessage(String msg) {
        System.out.println("Sending via email: " + msg);
    }
}

class StderrLogger extends Logger {
    public StderrLogger(int mask) { super(mask); }

    @Override
    protected void writeMessage(String msg) {
        System.out.println("Sending to stderr: " + msg);
    }
}

public class ChainOfResponsibilityExample {
    public static void main(String[] args) {
        // Build the chain of responsibility
        final Logger l =
            new StdoutLogger(Logger.DEBUG).setNext(
            new EmailLogger(Logger.NOTICE).setNext(
            new StderrLogger(Logger.ERROR)));

        // Handled by StdoutLogger
        l.message("Entering function y.", Logger.DEBUG);

        // Handled by StdoutLogger and EmailLogger
        l.message("Step1 completed.", Logger.NOTICE);

        // Handled by all three loggers
        l.message("An error has occurred.", Logger.ERROR);
    }
}
```

### [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")

``` PHP
<?php
abstract class Logger {
    const ERR = 3;
    const NOTICE = 5;
    const DEBUG = 7;

    protected $mask;
    protected $next; // The next element in the chain of responsibility

    public function setNext(Logger $l) {
        $this->next = $l;
        return $this;
    }

    abstract public function message($msg, $priority);
}

class DebugLogger extends Logger {
    public function __construct($mask) {
        $this->mask = $mask;
    }

    public function message($msg, $priority) {
        if ($priority <= $this->mask) {
            echo "Writing to debug output: {$msg}\n";
        }

        if (false == is_null($this->next)) {
            $this->next->message($msg, $priority);
        }
    }
}

class EmailLogger extends Logger {
    public function __construct($mask) {
        $this->mask = $mask;
    }

    public function message($msg, $priority) {
        if ($priority <= $this->mask) {
            echo "Sending via email: {$msg}\n";
        }

        if (false == is_null($this->next)) {
            $this->next->message($msg, $priority);
        }
    }
}

class StderrLogger extends Logger {
    public function __construct($mask) {
        $this->mask = $mask;
    }

    public function message($msg, $priority) {
        if ($priority <= $this->mask) {
            echo "Writing to stderr: {$msg}\n";
        }

        if (false == is_null($this->next)) {
            $this->next->message($msg, $priority);
        }
    }
}

class ChainOfResponsibilityExample {
    public function __construct() {
        // build the chain of responsibility
        $l = new DebugLogger(Logger::DEBUG);
        $e = new EmailLogger(Logger::NOTICE);
        $s = new StderrLogger(Logger::ERR);

        $e->setNext($s);
        $l->setNext($e);

        $l->message("Entering function y.",     Logger::DEBUG);     // handled by DebugLogger
        $l->message("Step1 completed.",         Logger::NOTICE);    // handled by DebugLogger and EmailLogger
        $l->message("An error has occurred.",   Logger::ERR);       // handled by all three Loggers
    }
}

new ChainOfResponsibilityExample();
?>
```

## 関連項目

  - [Interception パターン](https://ja.wikipedia.org/wiki/Interception_パターン "wikilink")
  - [Interceptor パターン](https://ja.wikipedia.org/wiki/Interceptor_パターン "wikilink")
  - [Single responsibility 原則](https://ja.wikipedia.org/wiki/:en:Single_responsibility_principle "wikilink")(英語)

## 外部リンク

  - Article "[The Chain of Responsibility pattern's pitfalls and improvements](http://www.javaworld.com/javaworld/jw-08-2004/jw-0816-chain.html)" by [Michael Xinsheng Huang](https://ja.wikipedia.org/wiki/Michael_Xinsheng_Huang "wikilink")(英語)
  - Article "[Follow the Chain of Responsibility](http://www.javaworld.com/javaworld/jw-08-2003/jw-0829-designpatterns.html)" by [David Geary](https://ja.wikipedia.org/wiki/:en:David_Geary "wikilink")(英語)
  - Article "[Pattern Summaries: Chain of Responsibility](http://developer.com/java/other/article.php/631261)" by [Mark Grand](https://ja.wikipedia.org/wiki/:en:Mark_Grand "wikilink")
  - [CoR overview](http://dofactory.com/Patterns/PatternChain.aspx)(英語)
  - [Behavioral Patterns - Chain of Responsibility Pattern](http://allapplabs.com/java_design_patterns/chain_of_responsibility_pattern.htm)(英語)
  - [Descriptions from Portland Pattern Repository](http://c2.com/cgi/wiki?ChainOfResponsibilityPattern)(英語)
  - [Apache Jakarta Commons Chain](http://jakarta.apache.org/commons/chain/)(英語)

[Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink") [Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")