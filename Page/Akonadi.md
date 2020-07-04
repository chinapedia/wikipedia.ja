> この記事は[Akonadi](https://ja.wikipedia.org/wiki/Akonadi)から翻訳されています。


**Akonadi**は、[PC-UNIX](https://ja.wikipedia.org/wiki/PC-UNIX "wikilink")用のデスクトップ環境である[KDE](../Page/KDE.md "wikilink") 4における[PIMフレームワークの実装である](../Page/Personal_Information_Manager.md "wikilink")。KDE 3においては、各PIMアプリケーションにおいてデータストレージとその取り扱い方が違っており、例えば検索、コンタクト情報の変更に対する通知など、同じ機能に対しても各ソフトウェアで異なった実装が求められていた。AkonadiはあらゆるPIMアプリケーションの拡張可能なデータ保管装置として一括的に機能し、また異なるアプリケーションが同じデータにアクセスしようとするときに発生したメモリーに関する問題（同じデータが複数回読み込まれること）も、Akonadiをサーバとして設置することにより解決された\[1\]。

Akonadiはデータの呼び出しと送信にサーバを用い、専用に作成された[API経由のアプリケーションは使用しない](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。データはAkonadiから特定のデータ（メール、カレンダー、コンタクトなど）を収集するために設計された[Model View Controllerに受け渡される](../Page/Model_View_Controller.md "wikilink")。これによりアプリケーションはビューアとエディタを用いてデータを表示し、作成することが可能になる。また、Akonadiは各アプリケーションにより作成されたデータもサポートする\[2\]。

AkonadiはPIMアプリケーションを作成する際に遭遇する困難な箇所を考慮して設計されたため、それらアプリケーション自体はより一層簡単に作成することが出来るようになった。Akonadiを使うことで、例えばMailody（KDEのメールクライアント）の開発者は、わずか10分で簡単なメールビューアを作り上げることができた\[3\]。

## 脚注

<references/>

## 外部リンク

  - [KDE PIM - Akonadi](http://pim.kde.org/akonadi/)

[Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink")

1.  [aKademy 2006 - Akonadi - The KDE 4.0 PIM Framework](http://conference2006.kde.org/conference/talks/9.php)
2.  [Akonadi Hacking Meeting](http://dot.kde.org/1177506111/)
3.  [Creating a mail reader in 10 minutes. | Tom Albers](http://www.omat.nl/drupal/creating-mail-reader-10-minutes)