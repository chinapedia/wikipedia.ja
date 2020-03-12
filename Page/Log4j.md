> この記事は[Log4j](https://ja.wikipedia.org/wiki/Log4j)から翻訳されています。


**Apache log4j**は、[Javaの](../Page/Javaプラットフォーム.md "wikilink")[ロギングユーティリティ](../Page/データログ.md "wikilink")。元々はCeki Gülcüにより開発されていたが、現在は[Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")のプロジェクトの一つとなっている。。log4jは、の一つである。

Ceki Gülcüはその後、log4j互換の後継として、と[Logback](http://logback.qos.ch/)の開発プロジェクトを立ち上げている。

## 機能

### ログレベル

log4jは、6つのログレベルを標準提供する。この他に利用者が任意のログレベルを追加することも可能である。ログレベルが高い（情報量が少ない）ものから低い（情報量が多い）ものへと順に並べると下表の通り。

| FATAL | 致命的なエラー。プログラムの異常終了を伴うようなもの。コンソール等に即時出力することを想定                                                  |
| ----- | ---------------------------------------------------------------------------------------------- |
| ERROR | エラー。予期しないその他の実行時エラー。コンソール等に即時出力することを想定                                                         |
| WARN  | 警告。廃要素となったAPIの使用、APIの不適切な使用、エラーに近い事象など、実行時に生じた異常とは言い切れないが正常とも異なる何らかの予期しない問題。コンソール等に即時出力することを想定 |
| INFO  | 情報。実行時の何らかの注目すべき事象（開始や終了など）。コンソール等に即時出力することを想定。従ってメッセージ内容は簡潔に止めるべき                             |
| DEBUG | デバッグ用の情報。システムの動作状況に関する詳細な情報。コンソールではなくログ上にだけ出力することを想定                                           |
| TRACE | トレース情報。更に詳細な情報。コンソールではなくログ上にだけ出力することを想定                                                        |

### 設定ファイル

log4jは、二つの方法で設定が可能である。一つは[プロパティファイル](https://ja.wikipedia.org/wiki/プロパティ#Javaにおけるプロパティ "wikilink")、もう一つは[XMLファイルである](../Page/Extensible_Markup_Language.md "wikilink")。両者とも、3つの主要な[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")（ロガー、アペンダ、レイアウト）について定義することができる。ファイルにより設定を行うため、log4jを使用しているアプリケーションを変更することなく、ロギングをon/offできるという利点がある。たとえば、問題が発生するまではロギングをoffで動作させておき、設定ファイルを変更することで簡単にロギングを再開する、という使い方ができる。

**ロガー** (Loggers) は論理的なログファイル名であり、Javaアプリケーションはこれらの名前を意識する。個々のロガーにて取得するログのレベル（FATAL、ERROR等々）はロガー毎に独立に設定できる。古いバージョンのlog4jでは、これらは「カテゴリ」と「優先度」と呼ばれていたが、現バージョンではそれぞれ「ロガー」と「レベル」と呼んでいる。

**アペンダ** (Appenders) は具体的な出力処理を行う。アペンダには様々な種類があり、それぞれ内容を表す名前が付いている。例えばFileAppender、ConsoleAppender、SocketAppender、SyslogAppender、NTEventLogAppenderなどがあり、SMTPAppenderというものさえある。任意のロガーには複数のアペンダを付与できるので、同じログ情報を例えばローカルのファイルと他のコンピュータ上のリスナに同時に出力する、などという使い方が可能。

**レイアウト** (Layouts) は一件ずつのログを整形するためにアペンダによって参照される。例えば行単位に出力するログを整形する方法としてPatternLayoutというものがあり、これは[C言語](../Page/C言語.md "wikilink")の[printf](https://ja.wikipedia.org/wiki/printf "wikilink")関数によく似た書式指定子を使える。他にもHTMLLayoutやXMLLayoutなどがあり、これらはそれぞれHTMLやXMLの書式に整形したい場合に使える。

### 設定例

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE log4j:configuration PUBLIC
"http://logging.apache.org/log4j/docs/api/org/apache/log4j/xml/log4j.dtd">
<log4j:configuration>
    <!-- アペンダとは出力先のことであり、例えばコンソールやファイルを指す。
    アペンダの名前は好きに決めてよい。-->
    <appender name="stdout" class="org.apache.log4j.ConsoleAppender">
        <layout class="org.apache.log4j.PatternLayout">
            <param name="ConversionPattern"
                value="%d{ABSOLUTE} %5p %c{1}:%L - %m%n" />
        </layout>
    </appender>

    <!-- 'org.springframework'カテゴリのロガーは、infoレベル以上のメッセージのみロギングする。
    もしロガーをクラス名で検索し（例：Logger.getLogger(AClass.class)）AClassが
    springframework.orgパッケージに属するなら、そのロガーはこのカテゴリに属する。-->
    <logger name="org.springframework">
        <level value="info"/>
    </logger>

    <!-- springは原則としてinfo以上のログしか取らないが、PropertyEditorRegistrySupportクラスについては
    デバッグログも欲しい-->
    <logger name="org.springframework.beans.PropertyEditorRegistrySupport">
        <level value="debug"/>
    </logger>

    <logger name="org.acegisecurity">
        <level value="info"/>
    </logger>

    <root><!-- rootカテゴリ -->
        <!-- 別途定義が無い限り、デバッグレベル以上の全てのメッセージをロギングする。-->
        <!-- 別途定義が無い限り、全てのログは「stdout」アペンダにてロギングされる。 -->
        <level value="debug" />
        <appender-ref ref="stdout" />
    </root>
</log4j:configuration>
```

（訳注：この設定例中に出現する「カテゴリ」という用語と、「ロガー」の旧称としての「カテゴリ」との関係は不詳。）

## ログビューア

Apacheにはという別プロジェクトが存在しており、これはlog4jにて生成されたログファイルを利用する。ChainsawはJavaベースのGUIビューアであり、豊富な機能を持つ。Chainsawもlog4jに類似した設定ファイルを使用する。log4j向けのビューアは他にもあるが（例：[log2web](http://log2web.sf.net/)オープンソースかつウェブベース）、Chainsawに比較して機能が少ない。

## 脚注

<references/>

## 外部リンク

  - [Log4j公式サイト](https://logging.apache.org/log4j/)

  -
  - [杉浦ホームページ - Log4J徹底解説](http://www.nurs.or.jp/~sug/soft/log4j/)

### ポート

  - [Log4c](http://log4c.sourceforge.net/) - [C言語](../Page/C言語.md "wikilink")用port
  - [Log4perl](http://log4perl.sourceforge.net/) - [Perl](../Page/Perl.md "wikilink")用port
  - [Log4net](http://logging.apache.org/log4net/) - [.NET Framework用port](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [log4php](http://logging.apache.org/log4php/) - [PHP用port](../Page/PHP_\(プログラミング言語\).md "wikilink")
  - [Log4js](http://stritti.github.io/log4js/) - [JavaScript](../Page/JavaScript.md "wikilink")用port
  - [log4js-node](https://log4js-node.github.io/log4js-node/) - [Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")用port
  - [Log4plsql](http://log4plsql.sourceforge.net/) - Oracle [PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")用port

[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")