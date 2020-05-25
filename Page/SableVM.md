> この記事は[SableVM](https://ja.wikipedia.org/wiki/SableVM)から翻訳されています。


**SableVM** は、[クリーンルーム設計](https://ja.wikipedia.org/wiki/クリーンルーム設計 "wikilink")の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")[バイトコード](../Page/バイトコード.md "wikilink")[インタプリタ](../Page/インタプリタ.md "wikilink")であり、[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")仕様第2版を実装している。

SableVM プロジェクトは、頑健で、移植性に優れ、効率的で、完全標準仕様準拠（JVM仕様、[JNI](../Page/Java_Native_Interface.md "wikilink")、呼び出しインタフェース、デバッグインタフェースなど）で、保守と拡張が容易なJava仮想マシンを一から作ることを目的として開始された。

中核部は性能を強化するため、[JITコンパイラを使った](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")[インタプリタ](../Page/インタプリタ.md "wikilink")となっており、移植性、保守性、単純性に優れている。このため、SableVM の[ソースコード](../Page/ソースコード.md "wikilink")は[可読性](../Page/可読性.md "wikilink")が高い。

SableVM は[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であり、[GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink") (LGPL) でライセンスされている。また、クラスライブラリとしては [GNU Classpath](../Page/GNU_Classpath.md "wikilink") を利用している。

SableVM は、Java仮想マシンの[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトの中でも、初めて JVMDI（Java Virtual Machine Debugging Interface）と JDWP（Java Debug Wire Protocol）をサポートした。これらのJavaデバッグインタフェース標準は [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") などでも、多機能で使いやすいJava開発環境を構築するのに使われている。

SableVM の開発は Sable Research Group （[マギル大学](../Page/マギル大学.md "wikilink")計算機科学科が母体）が開始し、現在はより広範囲のプログラマが参加している。[メーリングリスト](../Page/メーリングリスト.md "wikilink")以外にも、[IRC](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink") irc.sablevm.org（現在は、chat.freenode.net）のチャンネル \#sablevm で開発者同士が会話している。

## Java Intermediate Language

**Java Intermediate Language**（**JIL**）とは、Sable Research Group が2002年1月に提案した [Java](https://ja.wikipedia.org/wiki/Java "wikilink") プログラムの型構造を表現するための[中間言語](../Page/中間言語.md "wikilink")である。[XMLや](../Page/Extensible_Markup_Language.md "wikilink")[SGMLのサブセットになっており](../Page/Standard_Generalized_Markup_Language.md "wikilink")、Java プログラムを解析しやすくして、性能とスケーラビリティを向上させることを目的としている。

Sable Research Group 以外ではあまり採用されていない。

### 例

次のような Java コードがあるとする。

``` java
public MyClass implements MyInterface extends MySupperClass {
  int MyField;

  void MyMethod (double x, double y) {
    double z;
    z = x + y;
    this.MyField = z
  }
}
```

このコードを Java Intermediate Language で表すと、次のようになる。

``` xml
<jil>
<class name="MyClass" extends="MySupperClass">
  <modifiers><modifier name="public" /></modifiers>
  <interfaces><interface name="myinterface" /></interfaces>

  <fields>
    <field name="MyField" type="int" />
  </fields>

  <methods>
    <method name="MyMethod" returntype="void">
    <parameters>
      <parameter name="x" type="double" />
      <parameter name="y" type="double" />
    </parameters>
    <locals>
      <local name="z" type="double" />
    </locals>
    <statements>
      <!-- 各文はコード生成器向けの中間形式で表される。
           以下では、baf と呼ばれる言語が使われている。 -->
      <baf>
        <![CDATA[
          $r2 = $r0 + $r1;
          this.MyField = (double) $r2;
        ]]>
        <!-- ここでは、x が $r0、y が $r1、z が $r2 で表されている。 -->
      </baf>
    </statements>
    </method>
  </methods>
</class>
</jil>
```

## 外部リンク

  - [SableVM.org](http://www.sablevm.org/)
  - [Java Intermediate Language](http://www.sable.mcgill.ca/jil/class.xml)

[Category:Java仮想マシン](https://ja.wikipedia.org/wiki/Category:Java仮想マシン "wikilink")