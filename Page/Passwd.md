> この記事は[Passwd](https://ja.wikipedia.org/wiki/Passwd)から翻訳されています。


**passwd**（パスワード）は [Unix系](../Page/Unix系.md "wikilink")OSで使うコマンドである。ユーザの[パスワード](../Page/パスワード.md "wikilink")を変えるのに用いる。

## 機能

[ハッシュ化された新しいパスワードを生成するのに](../Page/ハッシュ関数.md "wikilink")[鍵導出関数](https://ja.wikipedia.org/wiki/鍵導出関数 "wikilink")を使う。ハッシュ化されたものだけを保存する。ハッシュ化したパスワードをローカルファイルに保存する。その場所は`/etc/passwd`や、shadowパスワードが使われているときは`/etc/shadow`である。ローカルに保存するということは、コマンドを実行したコンピュータのみに変更されたパスワードを適用するということである。

PAM (Pluggable authentication module) が使われていれば、どの分散認証機構でもpasswdコマンドがパスワードを変更するのに使える。PAMに対応したOSとして[Linux](../Page/Linux.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[FreeBSD](../Page/FreeBSD.md "wikilink")がある。また、PAMモジュールのあるスキームには[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の [NIS](../Page/ネットワーク・インフォメーション・サービス.md "wikilink")、[ケルベロス認証](../Page/ケルベロス認証.md "wikilink")、[LDAPなどがある](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")。passwdは、Linux Standard Baseでも指定コマンドになっている\[1\]。

## 関連

PAMが登場する前は、パスワードを変えるために認証スキーム毎に異なるコマンドを使う必要があった。例えば、NISパスワードを変更するコマンドは**yppasswd**だった。このためユーザは異なるシステムではパスワードを変える方法が違うということに気をつけなければならなかった。また、同じ機能を持つにもかかわらず、バックエンド毎に別のプログラムを書かなければならないという無駄が生じていた。

## 注釈

<references />

## 外部リンク

  - [Manpage of PASSWD](https://linuxjm.osdn.jp/html/shadow/man1/passwd.1.html) JM Project
  - [passwd(1)](https://docs.oracle.com/cd/E19253-01/819-1210/6n3j74jri/index.html) man page（SunOS リファレンスマニュアル）
  - [passwd(1)](https://nixdoc.net/man-pages/HP-UX/man1/passwd.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

1.  Linux Standard Base <https://refspecs.linuxfoundation.org/lsb.shtml>