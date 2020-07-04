> この記事は[DLL地獄](https://ja.wikipedia.org/wiki/DLL地獄)から翻訳されています。


**DLL 地獄**（ディーエルエルじごく）とは、DLL や [COM](../Page/Component_Object_Model.md "wikilink") コンポーネントなどのバージョンアップなどに伴い、それ以前のバージョンの DLL/COM コンポーネントなどに依存して動作するアプリケーションが動作しなくなる現象のことである。コンピュータ業界においては "DLL HELL" と呼ばれる場合が多い。Windows 以外の [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) で発生するものについては "Dependency Hell" の名称がよく使われる。

## 概要

原理的には[動的リンク](../Page/動的リンク.md "wikilink")するライブラリを利用する OS 全てにおいて発生する可能性がある。

[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") では以前は、プログラマのミスやインストーラの不具合により発生することが多かった（特に[COMコンポーネントに関しては](../Page/Component_Object_Model.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が厳密なバージョン管理規約を規定している\[1\]にもかかわらず、このバージョン管理の仕組みを理解しないままエンドユーザーシステムにインストールさせてしまう開発者が少なくない）。ではシステム保護機能や[サイドバイサイド](https://ja.wikipedia.org/wiki/分離アプリケーションとSide-by-Sideアセンブリ "wikilink") (Side-by-Side, SxS) と呼ばれる仕組みにより減ってきているが、全面解決には至っていない。

また、[Linux](../Page/Linux.md "wikilink") において対象ディストリビューションが異なるパッケージを使用したり、サードパーティの[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")や[レポジトリ](https://ja.wikipedia.org/wiki/レポジトリ "wikilink")を使用することによりライブラリの依存関係が壊れ、同様の事象が発生することが多い。

## 起因

この現象が起きる理由としてさまざまなことが挙げることが出来るが、最大の問題は「共有ライブラリに対し互換性を失うような変更が行われた場合に、ライブラリを呼び出すプログラム側がそれを区別することができない」という点に起因する。

プログラムの保守・可読性の向上や、セキュリティ問題等に起因するやむをえない仕様変更等により、あるプログラムにおいて旧バージョンとの互換性が失われてしまうことは、本来は極力避けるべき行為であるが、実際にはよく起こる現象である。これが動的にリンクされる共有ライブラリの場合、その互換性が失われた部分の機能を利用するアプリケーションにとっては、アプリケーション自体の動作に支障をきたすことになる。特に OS 本体に同梱されるライブラリにおいてこのような変更が行われると、その影響範囲は極めて広い範囲に及ぶ。

また、ソフトウェアの[インストーラ](https://ja.wikipedia.org/wiki/インストーラ "wikilink")がシステムの共有ライブラリのバージョンチェックを行わず、古いバージョンに置換してしまうことでも発生する。

[サードパーティー](../Page/サードパーティー.md "wikilink")のアプリケーションにおいては、アプリケーションが利用するライブラリをアプリケーション本体と同じディレクトリに配置することでこの問題を回避するといった試みがなされることも多い。しかし実際には、ファイル名が同一のライブラリが複数ハードディスク内に存在する場合にどのライブラリを最初に呼び出すかという選択は OS 側の設定（主に[環境変数](../Page/環境変数.md "wikilink")PATHの設定）によって変化することが多く、自分が意図したライブラリとは別のライブラリが優先的に呼び出されてしまうケースも少なくなかった。この問題に対処するため、Windows 2000 サービスパック4で、PATHの設定が優先されないようライブラリの検索順序が変更された (Safe DLL search mode)\[2\]。

マイクロソフトは [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") において、同じライブラリの異なる複数のバージョンを同時にインストールできるようにした上で、アプリケーション側は必要に応じて自分の使用したいライブラリのバージョンを明示的に指定できるサイドバイサイドを提供するなど、この問題を OS レベルで解消することを狙っている。

## 対処

[Windows ME](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")/[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") 以降の Windows であれば、誤ってシステムフォルダのライブラリファイルを書き換えてしまった場合でも、「[システムの復元](../Page/システムの復元.md "wikilink")」機能を使用することでほとんどすべての場合において復旧が可能である。

また、上記以外の OS や「システムの復元」が無効になっている場合であっても、システムの[スナップショットやイメージバックアップが存在する場合はリストアを実施することにより復旧可能である](../Page/スナップショット_\(ファイルシステム\).md "wikilink")。

この両者のいずれの復旧方法共に使用できない場合、原因となったソフトウェアのアンインストールやライブラリの再インストールあるいは手動置換などで復旧できる場合もあるが、確実ではなくかえって事態を悪化させることも多い。また、この方法で復旧できた場合でも、システム内に不整合が起きている場合が多いので、すぐにユーザーデータを退避させ、OS インストーラでシステムの修復やリカバリを実施する方がよい。

## 脚注

## 関連項目

  - [ライブラリ](../Page/ライブラリ.md "wikilink")
  - [ダイナミックリンクライブラリ](../Page/ダイナミックリンクライブラリ.md "wikilink")
  - [Microsoft Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")
  - [Component Object Model](../Page/Component_Object_Model.md "wikilink")
  - [分離アプリケーションとSide-by-Sideアセンブリ](https://ja.wikipedia.org/wiki/分離アプリケーションとSide-by-Sideアセンブリ "wikilink")
  - [グローバル アセンブリ キャッシュ](https://ja.wikipedia.org/wiki/グローバル_アセンブリ_キャッシュ "wikilink")

## 外部リンク

  - [DLL Hell の終焉](http://www.microsoft.com/japan/msdn/net/vbtransitionguide/chapter2/chapter2_6.aspx) （MSDN） - 原因などについての解説あり

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:アンチパターン](https://ja.wikipedia.org/wiki/Category:アンチパターン "wikilink") [Category:コンピュータ・ジャーゴン](https://ja.wikipedia.org/wiki/Category:コンピュータ・ジャーゴン "wikilink")

1.  [The Versioning Theory for RPC and COM (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/aa378963.aspx)
2.