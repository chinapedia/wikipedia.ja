> この記事は[KMail](https://ja.wikipedia.org/wiki/KMail)から翻訳されています。


**KMail**は[KDE](../Page/KDE.md "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")における[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")である。

フォルダ、フィルタリング、[HTMLメールの表示](../Page/HyperText_Markup_Language.md "wikilink")、国際文字セットをサポートする。[IMAP](https://ja.wikipedia.org/wiki/IMAP "wikilink")、[dIMAP](https://ja.wikipedia.org/wiki/dIMAP "wikilink")[1](http://www-uxsup.csx.cam.ac.uk/pub/doc/suse/suse9.2/suselinux-userguide_en/ch12s03.html)、[POP3や](../Page/Post_Office_Protocol.md "wikilink")、送られてきたメールに対するローカルのメールボックスを扱える。[SMTPや](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")[sendmail](https://ja.wikipedia.org/wiki/sendmail "wikilink")を通じてメールを送れる。

## スパムとフィルタリング

KMailにはスパムフィルタープログラムを扱えるようにするための二つの特別なフィルターがある。

  - プログラムにメールを送る : どのようなプログラムでも指定できる。KMailフィルターが有効のとき、プログラムは実行され、プログラムに[標準入力として](../Page/入出力.md "wikilink") Eメールの内容を与えることができる。
  - メールをプログラムに通す : 特定のプログラムにメールを送るだけでなく、メールの内容をそのプログラムの出力で置き換えることができる。これにより[SpamAssassin](https://ja.wikipedia.org/wiki/SpamAssassin "wikilink")のようなメールに独自のヘッダを付加するシステムを利用できるようになる。

このようなモジュール化されたフィルターはテキストフィルター組み合わせられるので、（例えば）SpamAssassinによって印が付けられたメールをヘッダを検索することで検出することができる。

KMailでメールサーバ上でスパムのフィルタリングを手動で行える。これはダイアルアップユーザにとっては非常に興味深い機能である。最大サイズを超えたメールは自動的にローカルコンピュータにコピーされない。「ダウンロード」、「メールを後でダウンロード」、「サーバからメールを削除」というオプションがあり、KMailはメールの一覧を表示するがメッセージ全体をダウンロードしないようにできる。そのためスパムや大きなサイズのメッセージを削除するときに時間の節約となる。

## 暗号化のサポート

KMailは[OpenPGP](https://ja.wikipedia.org/wiki/OpenPGP "wikilink")標準をサポートし、インラインやOpenPGP/MIME法を用いた署名/暗号化を通じたメールメッセージや添付ファイルの自動的な暗号化、復号、署名の検証を行える。KMailではこの機能を実現するのに[GnuPGを利用している](../Page/GNU_Privacy_Guard.md "wikilink")。ユーザが視覚的に区別できるように、KMailでは検証したメールを信頼できる署名に対しては緑、信頼できない署名に対しては黄、無効な署名に対しては赤、暗号化されたメッセージに対しては青で色付けする。

KMailは[S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink")メッセージや[Chiasmus](https://ja.wikipedia.org/wiki/Chiasmus "wikilink")[2](http://www.bsi.de/produkte/chiasmus/indexeng.htm)（ドイツの[BSIによって作られたプロプライエタリな暗号化システム](../Page/BSI_\(ドイツ\).md "wikilink")）もサポートする。

## グループウェアサポート

[Kontact](../Page/Kontact.md "wikilink")[個人情報マネージャスイートの一部として使った場合](../Page/Personal_Information_Manager.md "wikilink")、KMailは[グループウェア](../Page/グループウェア.md "wikilink")クライアントとして動作し、ユーザ間でコンタクトリスト、メール、カレンダーやメモ書きを共有できる。

## 関連項目

  - [Maildir](https://ja.wikipedia.org/wiki/Maildir "wikilink")

## 外部リンク

  - [KMail 公式サイト](http://userbase.kde.org/Kmail) - KDE UserBase
  - [KMail ハンドブック](http://docs.kde.org/stable/en/kdepim/kmail/index.html) - KDE Documentation
  - [KDE - KMail - Mail Client](http://www.kde.org/applications/internet/kmail/)

[Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:電子メールソフト](https://ja.wikipedia.org/wiki/Category:電子メールソフト "wikilink")