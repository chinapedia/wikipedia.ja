> この記事は[Tenems](https://ja.wikipedia.org/wiki/Tenems)から翻訳されています。


**Tenems**(テネムズ)は、[.NET系](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")型の[プログラミング言語](../Page/プログラミング言語.md "wikilink")のひとつ。動作可能[OSは](../Page/オペレーティングシステム.md "wikilink")、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 98/Me/2000/XP/Server 2003。実行には.NET Frameworkが動作することが条件。

本体は[Visual Basic .NETで開発されており](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")、基本的に[コンパイラ](../Page/コンパイラ.md "wikilink")と標準[テンプレート](../Page/テンプレート_\(プログラミング\).md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")のみの配布となる。開発者は[カーズV3](https://ja.wikipedia.org/wiki/カーズV3 "wikilink")で、現在は[SourceForge.jp](http://sourceforge.jp/)にて[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトとして開発されている。ライセンスは修正済み[BSDライセンス](../Page/BSDライセンス.md "wikilink")。

## 特徴

.NET Frameworkを利用した[プログラミングを行うことができ](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、独自の「見やすい」[構文](https://ja.wikipedia.org/wiki/構文 "wikilink")を採用することによって、[ソースを読みやすくする工夫を行っている](../Page/ソースコード.md "wikilink")。基本的に[C\#を見やすくしただけのように見える言語である](../Page/C_Sharp.md "wikilink")。

また、「テンプレート機能」というものが使え、それを使うと標準テンプレートライブラリに用意されたソースコードや、他の[ファイルのソースコードの内容を容易に取り込める](../Page/ファイル_\(コンピュータ\).md "wikilink")。(構文は「\#import <テンプレート名>」と「\#include "ファイル名"」である。)

また、[コンソール](../Page/キャラクタユーザインタフェース.md "wikilink")[アプリケーションと](../Page/アプリケーションソフトウェア.md "wikilink")[Windows Formsを利用したアプリケーションや](../Page/Windows_Forms.md "wikilink")[DLLを開発可能であり](../Page/ダイナミックリンクライブラリ.md "wikilink")、[CGIも開発できる](../Page/Common_Gateway_Interface.md "wikilink")。

ちなみにCGI専用のテンプレートもある。

以下はサンプルソースコードである。なお、「--」以降は[コメントであるため](../Page/コメント_\(コンピュータ\).md "wikilink")、コンパイル時に取り除かれる。

    -- object型を拡張したクラス「test」
    <test> extends object {
        -- MessageBox.Showのエイリアスとして関数「msg」を定義。戻り値はobject。
        <msg> static routine object (string message, string title) {
            MessageBox.Show(message, title);
            out : 0;
        }
        -- プログラムのエントリポイントとなるMain関数。戻り値はint。
        <Main> public static routine int () {
            const string cns = "Hello, World!";
            string var = "'Hello World' program.";
            var = "The " + var;
            msg(cns, var);
            out : 0;
        }
    }

この例ではわざわざエイリアスとなる関数を新たに定義しているが、もちろん[Main関数から直接](https://ja.wikipedia.org/wiki/エントリーポイント "wikilink") .NET Frameworkのライブラリの[オブジェクトを呼び出すこともできる](../Page/オブジェクト_\(プログラミング\).md "wikilink")。

## コンパイラの実体

コンパイラとは言っているが、実際はTenems言語をC\#に変換し、C\#のコンパイラにファイルと[引数](../Page/引数.md "wikilink")を渡しているだけである。

## 外部リンク

  - [公式サイト](http://tenems.sourceforge.jp/)
  - [SourceForge.jpプロジェクトページ](http://sourceforge.jp/projects/tenems/)

[Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")