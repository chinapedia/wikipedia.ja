> この記事は[Decibel](https://ja.wikipedia.org/wiki/Decibel)から翻訳されています。


**Decibel**（デシベル）は、[Linux](../Page/Linux.md "wikilink")デスクトップ環境の一つである[KDE](../Page/KDE.md "wikilink")のバージョン4に搭載される予定のコミュニケーションに関する新しいフレームワークである。Decibelは全ての[通信プロトコル](../Page/通信プロトコル.md "wikilink")をデスクトップに統一することを目標としている。現在のところ、[AOL Instant Messengerや](../Page/AOL_Instant_Messenger.md "wikilink")[Windows Live メッセンジャー](../Page/Windows_Live_メッセンジャー.md "wikilink")、[メール](../Page/電子メール.md "wikilink")、[Skype](../Page/Skype.md "wikilink")などでプロトコルは別々の方法で取り扱われているが、Decibelはこれらを一つにまとめることで、ユーザーは自身のコンタクト情報をより簡単に管理することが出来るようになると見られる。

例えば、ユーザーA がユーザーB とメッセージを送信する状況を考えてみる。ユーザーAがコンピュータにユーザーBと接続するよう要求すると、サービスマネージャは要求を受け入れて、ユーザーBにそのメッセージを送信するために最も望ましい方法を（電話番号やEメールアドレスなどに応じて）自動的に選択する。それゆえ、ユーザーBがどのプロトコルを用いていようとも、ユーザーAはBと通信できる。

## 機能

Decibelはコミュニケーションプロトコルに[テレパシープロトコルを用いるデスクトップ](https://ja.wikipedia.org/wiki/テレパシー_\(ソフトウェア\) "wikilink")[デーモンとして作動するが](../Page/デーモン_\(ソフトウェア\).md "wikilink")、そのデーモンを直接操作することは出来ない。しかしDecibelはリアルタイムコミュニケーションをアプリケーションに統合する労力を減らすために、テレパシーの上にいくつかの機能を加えている。テレパシーと同様に[D-Bus](../Page/D-Bus.md "wikilink")を用いており、それゆえ、D-Busを用いているアプリケーションはDecibelのサービスを利用することが出来る。また、プロトコルの設定やアカウントの管理、またはデスクトップにおける特定の作業を行うことが出来る。例えば[Qt](../Page/Qt.md "wikilink")または[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")などの[ツールキットを用いてGUIを起動したり](../Page/ウィジェット・ツールキット.md "wikilink")、[PIMにパスワードを保存させたり別のアカウントの情報を管理することなどが挙げられる](../Page/Personal_Information_Manager.md "wikilink")。

## KDE 4における対応

DecibelはKDE 4.1の[Kopete](../Page/Kopete.md "wikilink")に完全に対応する予定であり、4.0では部分的に対応している。Kopeteと[Pidgin](../Page/Pidgin.md "wikilink")は現在のプロトコルを、テレパシーの仕様で利用できるようにする予定である

## 関連項目

  - [KDE](../Page/KDE.md "wikilink")
  - [Telepathy](https://ja.wikipedia.org/wiki/Telepathy "wikilink")：Decibelが用いているアプリケーションフレームワーク

## 外部リンク

  - [Decibel ホームページ](http://decibel.kde.org/)

[Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink")