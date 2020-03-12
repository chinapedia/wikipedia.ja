> この記事は[Simple API for XML](https://ja.wikipedia.org/wiki/Simple_API_for_XML)から翻訳されています。


**Simple API for XML**（**SAX**、サックス）とは、[XML文書を](../Page/Extensible_Markup_Language.md "wikilink")[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")から利用するための[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

## 概要

[DOM](../Page/Document_Object_Model.md "wikilink") API が、[W3Cから勧告されたのに対して](../Page/World_Wide_Web_Consortium.md "wikilink")、SAX [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") は、[XML-DEVメーリングリスト](https://ja.wikipedia.org/wiki/XML-DEVメーリングリスト "wikilink")有志により策定された。そして、DOMに並ぶ[標準規格としての地位を固めている](../Page/デファクトスタンダード.md "wikilink")。

XML文書を[木構造として扱うDOMと異なり](../Page/木構造_\(データ構造\).md "wikilink")、一連のイベントとして表現する[イベント駆動型のAPIである](../Page/イベント駆動型プログラミング.md "wikilink")。したがって、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")が積極的にAPIにアクセスするDOMに対し、SAXではアプリケーションソフトウェアがイベントが来るのを待ち受ける受動的な動作が大部分を占める。

伝統的な[ストリームと同様に入力されたデータを次々とバトンタッチさせるような設計が可能となるため](../Page/ストリーム_\(プログラミング\).md "wikilink")、メモリを節約でき、[並列処理](https://ja.wikipedia.org/wiki/並列処理 "wikilink")にも適している。 XMLを読み込み、Javaのオブジェクトに変換するときはSAXの方がよく使われる。ただし、XML文書の先頭と最後を入れ替えるというような[ランダムアクセス](../Page/ランダムアクセス.md "wikilink")を必要とするアプリケーションソフトウェアにはDOMや[XMLデータベース](../Page/XMLデータベース.md "wikilink")の方が適している。

[Apache Cocoon](../Page/Apache_Cocoon.md "wikilink") のような[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")の高い優れたSAXアプリケーションソフトウェアが開発されている。

## 使用例

以下に、[プログラミング言語](../Page/プログラミング言語.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")での使用例を示す。[特別:Recentchanges](https://ja.wikipedia.org/wiki/特別:Recentchanges "wikilink")のRSSを読み込み、タイトルの一覧を表示している。

``` java
import java.io.IOException;
import javax.xml.parsers.*;
import org.xml.sax.*;
import org.xml.sax.helpers.DefaultHandler;

public class Test {
    public static void main(String[] args) throws ParserConfigurationException, SAXException, IOException {
        SAXParserFactory factory = SAXParserFactory.newInstance();
        SAXParser parser = factory.newSAXParser();

        parser.parse("http://ja.wikipedia.org/w/index.php?title=%E7%89%B9%E5%88%A5:Recentchanges&feed=rss", new DefaultHandler() {
            private String text = "";
            private boolean isItemStarted = false;

            public void startElement(String uri, String localName, String qName, Attributes attributes) {
                if(qName.equals("item")) {
                    isItemStarted = true;
                }
            }

            public void endElement(String uri, String localName, String qName) {
                if (isItemStarted && qName.equals("title")) {
                    System.out.println(text);
                }
            }

            public void characters(char[] ch, int start, int length) {
                text = new String(ch, start, length);
            }
        });
    }
}
```

## 外部リンク

  - [SAX](http://www.saxproject.org/)

[Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:構文解析_(プログラミング)](https://ja.wikipedia.org/wiki/Category:構文解析_\(プログラミング\) "wikilink")