> この記事は[Chroot](https://ja.wikipedia.org/wiki/Chroot)から翻訳されています。


**chroot**とは、[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")において、現在のプロセスとその子プロセス群に対して[ルートディレクトリ](https://ja.wikipedia.org/wiki/ルートディレクトリ "wikilink")を変更する操作である。ルートディレクトリを別のディレクトリに変更されたプロセスは、その範囲外のファイルにはアクセスできなくなるため、この操作を**chroot監獄**などとも呼ぶ。"chroot" は `chroot(2)` [システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")および `chroot(8)` コマンドを意味する。

chroot システムコールは、Unix Version 7 (1979) に新機能として加えられ、[1982年](../Page/1982年.md "wikilink")[3月18日](../Page/3月18日.md "wikilink")（[4.2BSDリリースの](../Page/BSD.md "wikilink")17ヶ月前）、[ビル・ジョイ](../Page/ビル・ジョイ.md "wikilink")がインストールおよびビルドシステムのテスト用にBSDに導入したのが起源である。

## 用途

chroot はOSの仮想化され分離されたコピーを作るのに使われる。これには、以下のような用途がある。

  - テストと開発
    実際に使用中のシステムで評価するには危険と思われる開発中ソフトウェアの[テスト環境構築に](https://ja.wikipedia.org/wiki/ソフトウェアテスト "wikilink") chroot を使う。
  - 依存関係制御
    ソフトウェアの開発において、[ビルドに最低限必要なものだけを用意した環境に](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink") chroot して実施することもできる。これにより、意図しない[ライブラリ](../Page/ライブラリ.md "wikilink")が[リンクされてしまうのを防ぐことができる](../Page/リンケージエディタ.md "wikilink")。
  - 互換性
    古いソフトウェアや異なる[ABIを使っているソフトウェアは](https://ja.wikipedia.org/wiki/Application_Binary_Interface "wikilink")、場合によっては chroot した環境で実行する必要がある。これは例えば、[動的リンク](../Page/動的リンク.md "wikilink")されるライブラリが同じ名前で異なる内容を必要とされる場合があるためである（[名前空間](../Page/名前空間.md "wikilink")の衝突の回避）。
  - 復旧
    [ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")できなくなったシステムの復旧において、別のブート媒体（[Live CD](https://ja.wikipedia.org/wiki/Live_CD "wikilink") など）で立ち上げておいて、ダメージのある環境に chroot することがある。UNIXのインストールでも、最初はインストール媒体で立ち上げておいて、最小限インストールした時点で chroot でディスクをルートディレクトリとすることもある。
  - 特権分離
    chroot されたプロセスのオープンしている[ファイル記述子](https://ja.wikipedia.org/wiki/ファイル記述子 "wikilink")（ファイル、[パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")、ネットワーク接続など）はそのまま保持されるので、chroot したディレクトリ内に作業用ファイルを残す必要がなく、chroot監獄の設計が簡略化される。これを応用して、特権プログラムの脆弱性のある部分だけを chroot して実行することで不正なファイルアクセスを防ぐことができる。しかし、chroot したとしてもシステムコールができなくなるわけでもなく、[ブロックデバイス](https://ja.wikipedia.org/wiki/ブロックデバイス "wikilink")へのアクセスを拒否するわけでもないため、特権を得た攻撃者にはあまり効果がない。
  - [ハニーポット](https://ja.wikipedia.org/wiki/ハニーポット "wikilink")
    chroot はネットワークサービスを実行する実システムのシミュレートにも使われる。しかし、chroot はシステムコールを仮想化しないし、ブロックデバイスや仮想ファイルシステム（Linux の `/proc` や `/sys`）へのアクセスをブロックしないので、ハニーポットに捉われた攻撃者がハニーポットであることに気づく可能性はある。

## 制限

  - プログラムは一般に起動されたときに、一時ファイル、設定ファイル、[スペシャルファイル](https://ja.wikipedia.org/wiki/スペシャルファイル "wikilink")、[共有ライブラリなどが特定の位置](../Page/ライブラリ.md "wikilink")（ディレクトリ）にあることを期待している。chroot されたプログラムがうまく起動するには、chroot したディレクトリにそれらのファイルが正しく配置されていなければならない。このため chroot を汎用の[サンドボックス機構として使うのは難しい](https://ja.wikipedia.org/wiki/サンドボックス_\(セキュリティ\) "wikilink")。
  - chroot を実行できるのは[スーパーユーザー](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")だけである。これは、精巧に作られたchroot監獄（例えば、ニセの `/etc/passwd` ファイルが置いてある）の中にユーザーが [setuid](https://ja.wikipedia.org/wiki/setuid "wikilink") プログラムを置けないようにするためである。またこのため、特権のないサンドボックス機構（例えば、一般ユーザーがインターネットからダウンロードした信頼できないアプリケーションをテストしてみるなど）としてchrootを使うこともできない。
  - chroot 機構は特権ユーザーによる意図的な改変に対する防御となることを意図していない。chroot された[スーパーユーザー](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")のプロセスは特権を制限されない。多くのシステムでは chroot のコンテキストは正しくスタックされず、特権を持ったまま2回目のchrootをするとchrootから抜け出せる\[1\]。そのため、chroot したプログラムは特権を放棄してから処理を続行すべきである。
  - chroot 機構自体は、[入出力](../Page/入出力.md "wikilink")、[帯域幅](../Page/帯域幅.md "wikilink")、ディスク容量、CPU時間などの[リソースを制限するわけではなく](../Page/計算資源.md "wikilink")、これらを行うにはOSレベルの仮想化が必要。多くのUNIXは完全な[ファイルシステム](../Page/ファイルシステム.md "wikilink")指向ではないため、ネットワーキングやプロセス制御などは chroot されたプログラムからもシステムコール経由で利用可能である。

一部のUNIXはこれらの制限の一部に対処した拡張を用意している（[OSレベルの仮想化](https://ja.wikipedia.org/wiki/OSレベルの仮想化 "wikilink")と呼ばれる）。

  - [Solaris](../Page/Solaris.md "wikilink") の [Solaris Containers](https://ja.wikipedia.org/wiki/Solaris_Containers "wikilink")
  - [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") は [cgroups](https://ja.wikipedia.org/wiki/cgroups "wikilink"), [LXC](https://ja.wikipedia.org/wiki/LXC "wikilink"), [OpenVZ](../Page/OpenVZ.md "wikilink"), [Parallels Virtuozzo Containers](../Page/Parallels_Virtuozzo_Containers.md "wikilink"), [Linux-VServer](https://ja.wikipedia.org/wiki/Linux-VServer "wikilink"), Linux [FreeVPS](https://ja.wikipedia.org/wiki/FreeVPS "wikilink") におけるセキュリティコンテキスト
  - [FreeBSD](../Page/FreeBSD.md "wikilink") の [FreeBSD jail](../Page/FreeBSD_jail.md "wikilink")
  - [NetBSD](../Page/NetBSD.md "wikilink") および [OpenBSD](../Page/OpenBSD.md "wikilink") の [sysjail](https://ja.wikipedia.org/wiki/sysjail "wikilink")

## 特筆すべき応用

  - [メール転送エージェント](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink") [Postfix](../Page/Postfix.md "wikilink") は、ヘルパープログラムを個々に chroot してパイプライン化して使用する。
  - [Debian](../Page/Debian.md "wikilink") と [Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink") はパッケージのビルドにおいて chroot を多用し、パッケージ間の意図しない依存関係を洗い出す。[SUSE](../Page/SUSE.md "wikilink") でも同様の手法を build プログラム内で行う。
  - [FTPサーバの多くは](../Page/File_Transfer_Protocol.md "wikilink")、信頼できないFTPクライアントのサンドボックス機構として chroot を使用する。コネクションに対応してプロセスを[fork](https://ja.wikipedia.org/wiki/fork "wikilink")し、子プロセスを chroot する（起動時のプログラムに chroot しているコードを含めないようにするため、子プロセスで chroot させる）。
  - [OpenSSH](https://ja.wikipedia.org/wiki/OpenSSH "wikilink")デーモンで特権分離をONに設定していると、各クライアントの認証前のトラフィックを処理する際に非特権ヘルパープロセスを空のディレクトリにchrootして実行させる。また、サンドボックスSFTPおよびシェルのセッションもchrootして実行する（version 4.9p1 以降）\[2\]。
  - [Google](../Page/Google.md "wikilink")はアプリケーションをchroot内で動作させている\[3\]。親プロセスのrootパーティションの変更がアプリケーションの動作に影響を与えない。

## fakechroot

chroot は root 権限が必要だが、LD_PRELOAD を使い、open() などにフックをかけて root 権限なしで chroot と同等のことを行う fakechroot がある\[4\]。

## 関連項目

  - [cgroups](https://ja.wikipedia.org/wiki/cgroups "wikilink")

## 脚注

## 参考文献

  - [chroot(2)](https://www.freebsd.org/cgi/man.cgi?chroot\(2\)) FreeBSD版システムコールのmanページ
  - [chroot(2)](https://linuxjm.osdn.jp/html/LDP_man-pages/man2/chroot.2.html) Linux版システムコールのmanページ (JM Project)
  - [chroot(8)](https://www.freebsd.org/cgi/man.cgi?query=chroot&sektion=8) FreeBSD版コマンドのmanページ（英語）
  - [chroot(1L)](https://linuxjm.osdn.jp/html/GNU_sh-utils/man1/chroot.1.html) GNU版コマンドのmanページ (JM Project)
  - [chroot(1M)](https://docs.oracle.com/cd/E56342_01/html/E54076/chroot-1m.html) コマンド Solaris 10 Reference Manual Collection（英語）
  - [chroot(1M)](https://docstore.mik.ua/manuals/hp-ux/en/B2355-60130/chroot.1M.html) コマンド man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:UNIXのシステムコール](https://ja.wikipedia.org/wiki/Category:UNIXのシステムコール "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink") [Category:コンピュータセキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータセキュリティ "wikilink") [Category:コンピュータセキュリティ手続](https://ja.wikipedia.org/wiki/Category:コンピュータセキュリティ手続 "wikilink")

1.  [How to break out of a chroot() jail](http://www.bpfh.net/simes/computing/chroot-break.html)
2.
3.
4.  [fakechroot/fakechroot - GitHub](https://github.com/fakechroot/fakechroot)