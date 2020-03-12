> この記事は[WebDAV](https://ja.wikipedia.org/wiki/WebDAV)から翻訳されています。


**WebDAV**（**Web-based Distributed Authoring and Versioning**、ウェブダブ）は[Hypertext Transfer Protocolを拡張したもので](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[Webサーバ](../Page/Webサーバ.md "wikilink")上のファイル管理を目的とした[分散ファイルシステム](../Page/分散ファイルシステム.md "wikilink")を実現するプロトコルである。

## 概要

WebDAVは、[Webサーバ](../Page/Webサーバ.md "wikilink")に対して直接ファイルのコピーや削除を行ったり、ファイル所有者や更新日時などのファイル情報を取得・設定するといった機能を持つ分散ファイルシステムで、HTTP 1.1を拡張したプロトコルで実現される。元々はファイルの[バージョン管理機能も内包していたが](../Page/バージョン管理システム.md "wikilink")、後に RFC 3253 で定義されたDelta-Vに分離された。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")によって最初に開発され、1999年2月に RFC 2518 が発表された。2007年6月に発表された RFC 4918 が2008年1月現在最新の定義である。

### 特徴

[Webサーバ](../Page/Webサーバ.md "wikilink")等でコンテンツのアップロードや更新を行う際に、[FTPや](../Page/File_Transfer_Protocol.md "wikilink")[scpのような別のサービス](../Page/Secure_copy.md "wikilink")・プロトコルを使うことなく、HTTPだけで全てのコンテンツ管理を完結できる。また、HTTPの拡張のみによって実装されているため、[ファイアウォール](../Page/ファイアウォール.md "wikilink")によって既存のファイル転送サービスが利用できない環境や、[HTTPプロキシを経由した環境でも利用できる](../Page/プロキシ.md "wikilink")。

## 設計

WebDAVには、元となるHTTP 1.1に加え次のメソッドが存在する。HTTPのヘッダ部でメソッドおよびURIを指定する。ボディ部では、クライアント・サーバ双方ともXMLを用いる。

  - PROPFIND:指定したURIが示す資源の属性を取得する。具体的には、要求する属性をクライアントがWebサーバに送信すると、サーバはそれに対応した属性値を返す。また、その資源の属性全てを取得することも出来る。
    PROPPATCH:指定したURIが示す資源の属性の設定や削除を行う。
    MKCOL:指定したURIの場所に新たな資源を作成する。
    COPY:指定したURIが示す資源およびその属性値を別のURIにコピーする。
    MOVE:指定したURIが示す資源およびその属性値を別のURIに移動する。
    LOCK:指定したURIが示す資源の[ファイルロック](../Page/ファイルロック.md "wikilink")を設定する。[共有ロックと](https://ja.wikipedia.org/wiki/ファイルロック#共有ロック "wikilink")[排他ロックの二種類が利用できる](https://ja.wikipedia.org/wiki/ファイルロック#排他ロック "wikilink")。
    UNLOCK:指定したURIが示す資源のロックを解除する。

## 実装

### Webサーバ

  - [Internet Information Services](../Page/Internet_Information_Services.md "wikilink")
    [Windows ServerにおけるWebサーバInternet](../Page/Windows_Server.md "wikilink") Information Servicesは、バージョン5.0からWebDAVをサポートしている\[1\]。
  - [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink")
    バージョン1.3から既存のApache HTTP Serverに追加する形でのWebDAVモジュールが存在していた\[2\]。バージョン2.0からは標準搭載され\[3\]、設定のみで利用できる。
  - [Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink")
    WebDAVサーバ機能を実現する追加モジュール\[4\]が存在する。
  - [04WebServer](http://www.soft3304.net/04WebServer/)
    2003年10月1日公開のバージョン0.40から実装されている。

### クライアント

#### Windows

[Windows 98以降は](../Page/Microsoft_Windows_98.md "wikilink")「Webフォルダ」という名称のWebDAVクライアント機能を内蔵し、ネットワーク上に置かれたファイルとしてアクセスできる。

[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") SP2以降で[Basic認証](../Page/Basic認証.md "wikilink")を行うには、レジストリの設定を変更する必要がある\[5\]。HTTPSの場合、Windowsエクスプローラではネットワークドライブとして割り当てることはできない。また、Windows Vistaの64bit版ではWebDAV機能は動作しない。

その他、Windows用のクライアントとして、CarotDAV\[6\]やNetDrive\[7\]、TeamFileクライアント\[8\]などがある。

#### OS X

[Finder](../Page/Finder.md "wikilink")は、WebDAVクライアント機能を内蔵している。[アップルが運営するストレージサービス](../Page/アップル_\(企業\).md "wikilink")[iDisk](https://ja.wikipedia.org/wiki/iDisk "wikilink")へのアクセスには、WebDAVを利用している\[9\]。

#### UNIX

[GNOME](../Page/GNOME.md "wikilink")においてファイルアクセス抽象化機能を提供する[GnomeVFS](https://ja.wikipedia.org/wiki/GnomeVFS "wikilink")は、WebDAVクライアント機能を備えている。[GNOME](../Page/GNOME.md "wikilink")の[ファイルなどファイルアクセスにGnomeVFSを用いているアプリケーションは](../Page/ファイル_\(GNOME\).md "wikilink")、シームレスにWebDAVサーバ上のファイルにアクセスできる。

cadaver\[10\]は、[キャラクタユーザインタフェース](../Page/キャラクタユーザインタフェース.md "wikilink")を持つWebDAVクライアントである。

#### その他

[Perl](../Page/Perl.md "wikilink")におけるHTTP::DAV\[11\]、[Python](../Page/Python.md "wikilink")のPyDAV\[12\]などのように、各種[スクリプト言語](../Page/スクリプト言語.md "wikilink")向けのクライアントライブラリが複数存在する。

[Subversionや](../Page/Apache_Subversion.md "wikilink")[arch](https://ja.wikipedia.org/wiki/arch "wikilink")では、リモートリポジトリへのアクセスプロトコルにWebDAVが利用できる。

## WebDAVを使用した規格

  - [CalDAV](https://ja.wikipedia.org/wiki/CalDAV "wikilink"):カレンダーの情報を交換するための規格。
    [CardDAV](https://ja.wikipedia.org/wiki/CardDAV "wikilink"):アドレス帳の情報を交換するための規格。

## その他

[ハロウィーン文書](../Page/ハロウィーン文書.md "wikilink")内でのHTTP-DAV\[13\]\[14\]とは、WebDAVのことを指している。

## 脚注

<references/>

## 外部リンク

  - [WebDAV日本語情報ページ](http://webdav.todo.gr.jp/)
  - [WebDAV-jpメーリングリスト](http://www.todo.ne.jp/webdav/)
  - [WebDAV Testing Server](http://test.webdav.org/) 接続テスト用に公開されているWebDAVサーバ。

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink")

1.  [Windows 2000 ホーム ‐ Internet Information Services 5.0 技術概要](http://www.microsoft.com/japan/technet/prodtechnol/windows2000serv/techinfo/howitworks/iis/iis5techoverview.mspx)
2.  [mod_dav: a DAV module for Apache](http://www.webdav.org/mod_dav/)
3.  [Apache 2.0 の新機能の概要](http://httpd.apache.org/docs/2.0/ja/new_features_2_0.html)
4.  [WebDAV in Ruby on Rails](http://wiki.rubyonrails.org/rails/pages/WebDAV)
5.  [Windows シェル コマンドを使って、または エクスプローラ表示 を使って、 Windows SharePoint Services 3.0 または Windows SharePoint Services 2.0 にドキュメントライブラリに接続できません。](http://support.microsoft.com/?kbid=841215)
6.  [麗の小屋 - WebDAV Client CarotDAV -](http://www.rei.to/carotdav.html)
7.  [Solution Box Inc.](http://www.netdrive.net/)
8.  [チームファイル](http://www.teamfile.com)
9.  [.Mac Services: iDisk についてよくお問い合わせいただく質問と解答 (FAQ) - 4/5](http://docs.info.apple.com/article.html?artnum=31327-ja#faq7)
10. [cadaver - command-line WebDAV client](http://www.webdav.org/cadaver/)
11. [<HTTP::DAV>](http://search.cpan.org/~pcollins/HTTP-DAV-0.31/DAV.pm)
12. [PyDAV](http://pypi.python.org/pypi/PyDAV)
13. [Halloween Document 10](http://www.catb.org/~esr/halloween/halloween1.html#comment28)
14. [Halloween I:Japanese ([山形浩生](../Page/山形浩生.md "wikilink")による日本語訳)](http://cruel.org/freeware/halloween1j.html#comment28)