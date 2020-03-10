> この記事は[WDDX](https://ja.wikipedia.org/wiki/WDDX)から翻訳されています。


**WDDX** (Web Distributed Data eXchange) とは、プログラミング言語やプラットフォームやトランスポート層に依存しないデータ交換機構であり、異なる環境や異なるコンピュータ間でのデータ交換を実現する。数値、文字列、ブーリアンといった単純なデータ型をサポートし、それらを組み合わせた構造体や配列やレコードなどもサポートする。WDDX は各種言語でサポートされている。[Ruby](../Page/Ruby.md "wikilink")、[Python](../Page/Python.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C++](../Page/C++.md "wikilink")、[.NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、[Flash](../Page/Adobe_Flash.md "wikilink")、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、[Haskell](../Page/Haskell.md "wikilink")などがある。

データは[XML](../Page/Extensible_Markup_Language.md "wikilink") 1.0 [DTD](../Page/Document_Type_Definition.md "wikilink") でエンコード（符号化）され、プラットフォームに依存しない、まとまった形式となる。そのような形式のデータを[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[FTPなど適当な転送機構で送る](../Page/File_Transfer_Protocol.md "wikilink")。受信側のマシンにはWDDXを解釈できるソフトウェアが搭載されており、そのマシンが扱える形式に変換を行う。WDDX はファイルシステムやストレージへ格納する際のデータ[シリアライズ](../Page/シリアライズ.md "wikilink")機構としても使うことができる。典型的な使用法としては、WebブラウザでWDDXを解釈する[JavaScript](../Page/JavaScript.md "wikilink")を動作させ、サーバからブラウザに対して複雑なデータをWDDX形式で送る。これは一種の[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")である。

WDDX は1998年、Allaire の Simeon Simeonov が [ColdFusion](https://ja.wikipedia.org/wiki/ColdFusion "wikilink")サーバ環境向けに開発したのが最初である\[1\]。

共に1998年に生まれた WDDX と [XML-RPC](../Page/XML-RPC.md "wikilink") は [SOAP](../Page/SOAP_\(プロトコル\).md "wikilink") と[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")の先駆けとなった。

例: \[2\]

    <nowiki>
     <wddxPacket version='1.0'>
       <header comment='PHP'/>
       <data>
         <struct>
           <var name='pi'>
             <number>3.1415926</number>
           </var>
           <var name='cities'>
             <array length='3'>
               <string>Austin</string>
               <string>Novato</string>
               <string>Seattle</string>
             </array>
           </var>
         </struct>
       </data>
     </wddxPacket>
    </nowiki>

## 脚注

<references/>

## 外部リンク

  - [OpenWDDX website](http://www.openwddx.org/)
  - [GCA98 WDDX Presentation](http://www.infoloom.com/gcaconfs/WEB/chicago98/simeonov.HTM)
  - [Cover Pages on WDDX](http://xml.coverpages.org/wddx.html)
  - [Exchanging Data with WDDX](http://www.webmonkey.com/webmonkey/99/15/index3a.html)
  - [Using WDDX with Flash](http://www.xml.com/pub/r/1266)

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink")

1.
2.  [php.net/wddx](http://www.php.net/wddx)