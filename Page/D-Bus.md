> この記事は[D-Bus](https://ja.wikipedia.org/wiki/D-Bus)から翻訳されています。


**D-Bus**（Desktop Bus、ディーバス）は、メッセージバスと呼ばれる、アプリケーション間でやりとりを行うための、[プロセス間通信](../Page/プロセス間通信.md "wikilink")（IPC）実装の1つである。プロセスの生成期間を調節し、それらのサービスが必要なときに簡単に呼び出すことができるようにすることができる。軽量さ、低依存度を保って開発されている。

D-Busは[KDE](../Page/KDE.md "wikilink")（バージョン2 - 3）独自のIPC実装である[DCOP](../Page/DCOP.md "wikilink")の影響を受けて生まれ、KDE4 ([Qt](../Page/Qt.md "wikilink")4) で採用された。[GNOME](../Page/GNOME.md "wikilink")も独自のIPC実装である[Bonobo](../Page/Bonobo.md "wikilink")からD-Busへ移行している。Linuxでも[udev](https://ja.wikipedia.org/wiki/udev "wikilink")によるマウントメッセージの通知を行う際にD-Busを使っている。[X.Org Server](../Page/X.Org_Server.md "wikilink")7.3からはD-Busによる実行時の設定が可能になっている。

D-Busは多くの言語とライブラリとの[バインディングを持ち](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")、[C言語](../Page/C言語.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C++](../Page/C++.md "wikilink")、[C\#](../Page/C_Sharp.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")、[Qt](../Page/Qt.md "wikilink")、[Maemo](https://ja.wikipedia.org/wiki/Maemo "wikilink")（携帯端末用のデスクトップ環境）などから利用できる。さらに、[Unix系](../Page/Unix系.md "wikilink")OSだけでなく、winDBusという名前の別プロジェクトとして[Windows版も開発されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 機構

D-Busデーモン（dbus-daemon）によってメッセージを管理する。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の起動中に常時実行される**システム管理用のデーモン**と、該当ログインセッションが有効である期間中実行される**ログインセッション管理デーモン**の2つがある。システム管理用のデーモンは、プリンタキューの追加やデバイスの追加・削除などを通知する。セッションごとのデーモンは、[デスクトップアプリケーション](https://ja.wikipedia.org/wiki/デスクトップアプリケーション "wikilink")間の通信に使われる。

デーモンとアプリケーションの間の通信としては、ソケットを用いる。

## アーキテクチャ

D-Busは、3つのレイヤーから構成されるアーキテクチャである\[1\]。

1.  **`libdbus`** - 2つのアプリケーションをつなぎ、メッセージを交換することを可能にするライブラリ
2.  **`dbus-daemon`** - `libdbus` 上に作られた[実行ファイル](../Page/実行ファイル.md "wikilink")形式のメッセージバスデーモン。複数のアプリケーションが接続する。デーモンは1つのアプリケーションから0個以上の複数のアプリケーションにメッセージを配信する。[出版-購読型モデル](../Page/出版-購読型モデル.md "wikilink")を実装できる。
3.  特定のアプリケーションフレームワークに基づくラッパーライブラリ

D-Busの設計は、以下の2つのケースに基づいて行われた。

1.  同じデスクトップセッション内のデスクトップ環境上のアプリケーション間の通信。全体として、デスクトップセッションを1つに統合する。
2.  デスクトップセッションとオペレーティングシステム間の通信。オペレーティングシステムには典型的にはカーネルやシステムデーモンなどが含まれる。

## D-Busを利用するソフトウェア

  - [HAL (ソフトウェア)](../Page/HAL_\(ソフトウェア\).md "wikilink") （ハードウェアの変更をアプリケーションへ通知する）
  - [notification-daemon](https://ja.wikipedia.org/wiki/notification-daemon "wikilink")（Xのイベントをアプリケーションに通知する）

## 参照

<references />

## 関連項目

  - [freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink")

## 外部リンク

  -
  - [ソースコード](http://gitweb.freedesktop.org/?p=dbus/dbus.git;a=summary)

  - [D-Bus 仕様](http://www1.ocn.ne.jp/~s_step/html/ja/dbus/dbus-specification.html)

  - [D-Bus Tutorial](https://dbus.freedesktop.org/doc/dbus-tutorial.html)

  - [IBM D-BUSを使用してデスクトップ・アプリケーションを接続](https://www.ibm.com/developerworks/jp/linux/library/l-dbus/)

  - [D-BUSのWindowsポーティング](https://sourceforge.net/projects/windbus/)

  - [NokiaのLinux開発環境(Maemo)のチュートリアル](http://maemo.org/maemo_training_material/maemo4.x/html/maemo_Platform_Development/index.html)

  - [MeeGo wiki D-Busオーバービュー](http://wiki.meego.com/D-Bus/Overview)

[Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink") [Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink") [Category:OSのプロセス管理](https://ja.wikipedia.org/wiki/Category:OSのプロセス管理 "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:遠隔手続き呼出し](https://ja.wikipedia.org/wiki/Category:遠隔手続き呼出し "wikilink")

1.