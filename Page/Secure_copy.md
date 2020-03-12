> この記事は[Secure copy](https://ja.wikipedia.org/wiki/Secure_copy)から翻訳されています。


**Secure Copy**（）は、sftp同様、[Secure Shell](../Page/Secure_Shell.md "wikilink")（ssh）に含まれるsshの機能を使って[セキュリティの高い](../Page/コンピュータセキュリティ.md "wikilink")（セキュアな）[ファイル転送](https://ja.wikipedia.org/wiki/ファイル転送 "wikilink")を行う[コマンドの一つである](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。scpで使用される通信プロトコルは、**Secure Copy Protocol**（SCP）と呼ばれる。

SSHを介してファイル転送を行うプロトコルとしては[SSH File Transfer Protocol](../Page/SSH_File_Transfer_Protocol.md "wikilink")（以下SFTP）があり、両者はしばしば比較される。その際、SCPはより軽く、SFTPはより高機能と評されることがある\[1\]。2019年4月、[OpenSSH](../Page/OpenSSH.md "wikilink")の開発チームは「scpのプロトコルはもはや時代遅れで柔軟性がなく、修正が困難になっている」とし、SFTPや[rsync](https://ja.wikipedia.org/wiki/rsync "wikilink")など他のファイル転送プロトコルの使用を勧めている\[2\]\[3\]。

[認証情報](https://ja.wikipedia.org/wiki/認証#Authentication "wikilink")（たとえば[パスワード](../Page/パスワード.md "wikilink")認証なら、ユーザー名やパスワード）と、[セッション](../Page/セッション.md "wikilink")中でやり取りされる[データ](../Page/データ.md "wikilink")との両方ともが、暗号化されて[ネットワーク上を流れる](../Page/コンピュータネットワーク.md "wikilink")。[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")で古くから使われているリモートファイル転送コマンド[rcp](https://ja.wikipedia.org/wiki/rcp "wikilink")（）のセキュアなバージョンといえる。コマンドラインの指定方法はrcpとほぼ同じである。rcpは暗号化などに対応しておらず、安全ではない。ある種のシステムではrcpという名前で起動しようとするとscpコマンドを実行する。

ssh-agentコマンドなどと組み合わせて利用すれば、コピー時に認証情報の入力が不要で、cpやrcp同様に利用できる。

「SCPが対応する、1ファイルの転送可能な最大サイズは4GB」と解説されることがあるが\[4\]、これは正確ではない。プロトコル自体にはファイルサイズ制限はなく、最大サイズはクライアントおよびサーバのソフトウェアとOS、そしてファイルシステムに依存する。例えば、OpenSSHでは実質上ファイルサイズの制限なく取り扱えるようになっている\[5\]。

[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")には、[WinSCP](../Page/WinSCP.md "wikilink")というSCPを用いるGUI対応ソフトがある\[6\]。

## 脚注

## 関連項目

  - [SSH File Transfer Protocol](../Page/SSH_File_Transfer_Protocol.md "wikilink")
  - [rsync](https://ja.wikipedia.org/wiki/rsync "wikilink")
  - [File Transfer Protocol](../Page/File_Transfer_Protocol.md "wikilink")
  - [Secure Shell](../Page/Secure_Shell.md "wikilink")
  - [telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")
  - [WinSCP](../Page/WinSCP.md "wikilink")
  - [FISH](../Page/Files_transferred_over_shell_protocol.md "wikilink")

[Category:ファイル転送プロトコル](https://ja.wikipedia.org/wiki/Category:ファイル転送プロトコル "wikilink") [Category:Secure_Shell](https://ja.wikipedia.org/wiki/Category:Secure_Shell "wikilink")

1.
2.
3.
4.  例として、[WinSCP公式サイトのプロトコル比較。](https://web.archive.org/web/20160211192722/http://winscp.net:80/eng/docs/protocols)2016年2月11日時点のアーカイブ。
5.
6.  WinSCP <https://winscp.net/eng/download.php>