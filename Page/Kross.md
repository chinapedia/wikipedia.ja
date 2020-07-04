> この記事は[Kross](https://ja.wikipedia.org/wiki/Kross)から翻訳されています。


**Kross**（クロス）は、[Linux](../Page/Linux.md "wikilink")用デスクトップ環境である[KDE](../Page/KDE.md "wikilink") 4に搭載されている[スクリプトフレームワークである](../Page/スクリプト言語.md "wikilink")。本来は[KOffice](https://ja.wikipedia.org/wiki/KOffice "wikilink")用に設計されていたが結果的にはKDE 4の公式フレームワークとなった。ユーザーが自らが選択する[スクリプト言語](../Page/スクリプト言語.md "wikilink")で最大限のスクリプトの力を提供することを目的に開発された。Krossを使うことで開発者は、KDEプラットフォームを視野に入れながら、アプリケーションに複数のスクリプト言語を優先順位を付けることなくサポートさせることが容易になる。

Krossスクリプティングプラットフォーム自体はスクリプト言語ではなく、既にシステム上にあるスクリプト言語をKDEにサポートさせることを目的としている。現在サポートされている言語は[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")、Falconプログラミング言語の4つである。また他のスクリプト言語も容易に追加できる。

デスクトップアプリケーションもしくはデスクトップ環境のスクリプティングを可能にする他のアプローチと比較して、Krossには以下のような利点がある。

  - ユーザーは自分の好きなスクリプト言語を使うことが出来る。
  - アプリケーションの開発者は各スクリプト言語の仕様を知る必要が無い。
  - プラグインにより他のスクリプト言語を容易に追加できる。

## 他のスクリプトプラットフォームとの比較

### [SWIG Simplified Wrapper and Interface Generator](https://ja.wikipedia.org/wiki/SWIG "wikilink"):

  - サポートしているスクリプト言語はSWIGより少ない。
  - Krossは[Qt](../Page/Qt.md "wikilink")の上に開発されており、Qt関連のモジュールをラッピングすることなくそれらにアクセスできる\[1\]。
  - Krossをサポートするアプリケーションは、SWIGをサポートするアプリケーションよりも少ないコードで済む\[2\]。
  - SWIGではアプリケーションの[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")時において、サポートされるスクリプト言語が確定される。つまり、サポートされる言語のコードもしくは、アプリケーションの言語に合った共有ライブラリをアプリケーションにあらかじめ組み込んでおかなくてはならない。一方でKrossではアプリケーションを起動する際まで確定する必要は無い。

### [AppleScript](../Page/AppleScript.md "wikilink")

[AppleScript](../Page/AppleScript.md "wikilink")のオープン・スクリプティング・アーキテクチャ (OSA) と比較すると、

  - OSAは[IPC](../Page/プロセス間通信.md "wikilink")（[アップルイベント](../Page/Apple_event.md "wikilink")）により、各スクリプトがそれぞれのプロセスを有することが出来るが、Krossではスクリプトはメインアプリケーションと同じプロセスを共有することになる。それゆえ、Krossと異なり、OSAにおいてスクリプトは既に起動しているアプリケーション同士の橋渡しとなり得る。

<!-- end list -->

  -
    （ちなみに、あるスクリプトが複数のアプリケーションのコードに同時にアクセスする際、IPCが必ずしも必要となるわけではない。スクリプトは、アプリケーションをライブラリとしてリンクさせることが出来る。例：SWIGによるライブラリ）

<!-- end list -->

  - Krossはスクリプタに好きな言語でスクリプトを書かせられるのに対し、AppleScriptは他のスクリプト言語の枠内で呼び出すことが出来る一つの言語である。
  - 多くの[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")アプリケーションではGUIツールキット ([Cocoa](../Page/Cocoa.md "wikilink")) を選択するだけで、ボタンやメニューのクリック、または[スクリーンリーダー](../Page/スクリーンリーダー.md "wikilink")等の[アクセシビリティソフトウェアに与えられたデータにアクセスするといった基本的なスクリプトが実行できるのに対し](../Page/コンピュータアクセシビリティ.md "wikilink")（[Dogtail](https://ja.wikipedia.org/wiki/Dogtail "wikilink")等のGUIテストツールも同様）、Krossではアプリケーションに追加されるコードは明示化される必要がある。

Krossは現在、信用性が疑わしいスクリプトであっても動作を制限しない。Krossの開発者であるSauerは\[3\]、（例えば実験的な[Java](https://ja.wikipedia.org/wiki/Java "wikilink")プラグインを用いる際には）サンドボックスを適切に用いるか、署名されたスクリプトを用いて信頼性を高めるよう勧めている[1](http://www.kexi-project.org/wiki/wikiview/index.php?Scripting#Security_issues)。

## Krossを用いているアプリケーション

  - [KWord](../Page/KWord.md "wikilink")
  - [KSpread](https://ja.wikipedia.org/wiki/KSpread "wikilink")
  - [Krita](../Page/Krita.md "wikilink")
  - [Kexi](https://ja.wikipedia.org/wiki/Kexi "wikilink")
  - [SuperKaramba](../Page/SuperKaramba.md "wikilink")
  - [Plasma](https://ja.wikipedia.org/wiki/Plasma_\(KDE\) "wikilink")
  - [Kopete](../Page/Kopete.md "wikilink")

## 脚注

<references/>

## 外部リンク

  - [Krossホームページ（開発者向けドキュメント）](http://kross.dipe.org/)
  - [Kross開発者のインタビュー](http://dot.kde.org/1152490640/)
  - [Krossチュートリアル](http://techbase.kde.org/Development/Tutorials/Kross-Tutorial)
  - [akademy 2006 conferenceにおけるKrossの紹介](http://conference2006.kde.org/conference/talks/2.php)
  - [Kross名前空間リファレンス](http://www.englishbreakfastnetwork.org/apidocs/apidox-kde-4.0/kdelibs-apidocs/kross/html/namespaceKross.html)

[Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink") [Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  <http://www.kexi-project.org/wiki/wikiview/index.php?Scripting#Why_not_SIP_SWIG_> (accessed 2007-05-16)
2.
3.  [The Road to KDE 4: New KOffice Technologies](http://dot.kde.org/1168284615/)