> この記事は[Libvirt](https://ja.wikipedia.org/wiki/Libvirt)から翻訳されています。


[thumbなどの](https://ja.wikipedia.org/wiki/ファイル:Libvirt_support.svg "wikilink")[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")をサポートし、[virt-manager](https://ja.wikipedia.org/wiki/virt-manager "wikilink")などの管理ソリューションをサポートする。\]\] **libvirt**とは、[仮想化](../Page/仮想化.md "wikilink")管理用の共通[APIを提供する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[レッドハット](../Page/レッドハット.md "wikilink")を中心とした[オープンソース](../Page/オープンソース.md "wikilink")[プロジェクト](../Page/プロジェクト.md "wikilink")である。

## 概要

libvirtは[仮想機械](../Page/仮想機械.md "wikilink")の制御を[抽象化した](../Page/抽象化_\(計算機科学\).md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")である。 本ライブラリの特徴は、サポート範囲が広いことである。 サポートしている仮想化は、現在[Xen](https://ja.wikipedia.org/wiki/Xen "wikilink")、[KVM](https://ja.wikipedia.org/wiki/Kernel-based_Virtual_Machine "wikilink")、[QEMU](../Page/QEMU.md "wikilink")、[LXC](https://ja.wikipedia.org/wiki/LXC "wikilink")、[OpenVZ](../Page/OpenVZ.md "wikilink")、[UML](../Page/User_Mode_Linux.md "wikilink")、[VirtualBox](../Page/VirtualBox.md "wikilink")、[VMware](../Page/VMware.md "wikilink") ESX・GSX・Workstation・Player、[Hyper-V](../Page/Hyper-V.md "wikilink")、そしてクラスタ管理ソフト[OpenNebula](https://ja.wikipedia.org/wiki/OpenNebula "wikilink")である。 更なる対象仮想機械の拡大を目指して例えば、対応や[Linux-VServer](../Page/Linux-VServer.md "wikilink")のサポートをどうするかなどが開発者メーリングリスト上で議論された。 また、様々な版数でのサポートも特徴である。たとえば、[Xenのリリースされたさまざまな版](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")（例えばXen3.1.0やXen3.0.3など）で動作する。また[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")だけでなく、[Windows上でも](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[MinGW](../Page/MinGW.md "wikilink")や[Cygwin](../Page/Cygwin.md "wikilink")を使えば動作する。

libvirt自体が多くの種類の仮想化をサポートしていても、必ずしもlibvirtを利用している[アプリケーションが全ての仮想化をサポートしているというわけではなく](../Page/アプリケーションソフトウェア.md "wikilink")、KVMやXenなどがlibvirtを利用しているアプリケーションのサポートの中心となっている。

また[ハードウェア](../Page/ハードウェア.md "wikilink")[プラットフォームに着目すると](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、[CPU](../Page/CPU.md "wikilink")の場合、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")、[x86-64](https://ja.wikipedia.org/wiki/x64 "wikilink")、[IA-64](../Page/IA-64.md "wikilink")、[POWERなどをサポートしており](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")、[ビット](../Page/ビット.md "wikilink") (32/64) および[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")を問わない。

このような幅広いサポートを行っているため、仮想機械を制御する[インタフェースとしては](../Page/インタフェース_\(情報技術\).md "wikilink")、[事実上の標準の地位を築きつつある](../Page/デファクトスタンダード.md "wikilink")。 例えば、[RHEL5上で仮想機械を管理するためのアプリケーションである](../Page/Red_Hat_Enterprise_Linux.md "wikilink")[Virtual Machine Managerの実装においても利用されている](https://ja.wikipedia.org/wiki/Virtual_Machine_Manager "wikilink")\[1\]。

本ソフトウェアのライセンスは[LGPLで提供されている](../Page/GNU_Lesser_General_Public_License.md "wikilink")。このため、[GPLで開発されているXenのライブラリ](../Page/GNU_General_Public_License.md "wikilink") ([libxc](https://ja.wikipedia.org/wiki/libxc "wikilink")) に比べてアプリケーション開発者の視点では使い勝手が良い。

標準提供APIは[Cと](../Page/C言語.md "wikilink")[Python](../Page/Python.md "wikilink")である。またその他の言語 ([Perl](../Page/Perl.md "wikilink"), [OCaml](../Page/OCaml.md "wikilink"), [Ruby](../Page/Ruby.md "wikilink"), [Java](https://ja.wikipedia.org/wiki/Java "wikilink")) のAPIもオプションパッケージで提供されている。また、運用管理の標準インタフェースである[CIMへの対応も](../Page/Common_Information_Model.md "wikilink")[IBM](../Page/IBM.md "wikilink")を中心にCMPI CIM Providerとしてlibvirt-CIMの開発が進んでいる。なお、CMPIは、Common Manageability Programming Interfaceの略である。

セキュリティ拡張として、MACアクセス制御との連携を考えた[sVirt](http://selinuxproject.org/page/SVirt)が検討されている。

本プロジェクトのメンテナーは、Daniel Veillard（通称Daniel）、Daniel Berrange（通称Dan）、Richard W.M.Jones（通称Rich）などレッドハットの開発者である。そのほか、レッドハット以外にもIBMや[ノベル](../Page/ノベル_\(企業\).md "wikilink")、[富士通](../Page/富士通.md "wikilink")の開発者に[ソースコード](../Page/ソースコード.md "wikilink")の変更権が与えられている。

## ソフトウェア構成

libvirtの実装はlibvirt.cを中心とした[ソフトウェア](../Page/ソフトウェア.md "wikilink")構成になっている。libvirtのAPIを利用しているアプリケーションとしては、管理コマンドvirshが提供されている。また、Python Bindingsもlibvirt.cの上位に位置する。

一方、各種仮想機械の制御[ドライバは](../Page/デバイスドライバ.md "wikilink")、libvirt.cの下に位置する。例えばXenの制御層の実装では、Xen統合管理層 (xen_unified.c) から、それぞれのXenの[モジュール](../Page/モジュール.md "wikilink")を呼び出す形になっている。[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")直接 (xen_internal.c)、管理ツールであるXend (xend_internal.c)、管理[データベース](../Page/データベース.md "wikilink")であるxenstore (xs_internal.c) を呼び出している。

また、[ネットワーク越しの制御に関するコードは](../Page/コンピュータネットワーク.md "wikilink")、以下の通りである。クライアント側では、remote_internal.cを介してリクエストを発行する。サーバ側では、libvirtd（コード的には、qemudディレクトリ以下）を介して、libvirtAPIを使って制御を行う。

## アクセス制御

libvirtAPIを使う前にクライアント認証を必要とする接続がある。

接続で用いるクライアント認証方法は、管理者が選択できる。

この選択は、libvirtAPIを用いるアプリケーションに依存せず、統一的に適用される。

  - サーバ設定
  - [UNIXドメインソケット](https://ja.wikipedia.org/wiki/UNIXドメインソケット "wikilink")による伝統的権限管理
  - Polkitを使ったUNIXドメインソケットの認証
  - ユーザ名とパスワードによる認証
  - [ケルベロス認証](../Page/ケルベロス認証.md "wikilink")

### サーバ設定

管理者は、libvirtdの認証方法を、ネットワークソケット毎に設定することができる。

この設定は、libvirtdの設定ファイル /etc/libvirt/libvirtd.confで行う。

そして、認証方法は、なし、POLKITそして[SASLの](https://ja.wikipedia.org/wiki/Simple_Authentication_and_Security_Layer "wikilink")3つから選択することができる。

さらに、SASL機構は、将来さまざまなオプションを設定できるようになる予定である。

### UNIXドメインソケットによる伝統的権限管理

libvirtがPolkitをサポートしていない場合、UNIXドメインソケットに対するアクセス制御は、伝統的なユーザグループアクセス制御により行われる。

2種類のソケットがあり、ひとつは読み書き可能、もう1つは読みのみ可能となっている。

読み書きソケットは、アクセス制御が厳しく(0700)、ルートユーザのみが使うことができる。

読みのみソケットは、アクセス制御がオープン (0777) であり、どのユーザも使うことができる。

非特権ユーザにより広いアクセスを許可する場合、libvirtd.confファイルを編集しunix_sock_rw_permsに許可権限を設定し、ユーザグループを、unix_sock_groupに設定する必要がある。例えば、前者の属性を0770にして、後者をwheelグループに設定すると、wheelグループの人全員libvirtdにアクセスできることになる。

### Polkitを使ったUNIXドメインソケットの認証

libvirtがPolkit認証をサポートする場合、アクセス制御は、より進んだ形態になる。

この場合、unix_sock_authパラメータは、polkitが標準になる。そして、ファイルアクセス権限は、読み書き権限を含め0777になる。クライアントアプリケーションは、Polkitと連携してアイデンティティを提供し、ソケットに接続する。

現デスクトップセッションのいずれのアプリケーションでも、パスワード認証を行うことが、読み書きソケットの標準ポリシーである。

この方法は[sudo](https://ja.wikipedia.org/wiki/sudo "wikilink")コマンドによる認証と似ている。しかし、クライアントアプリケーションは究極的に特権ユーザ（ルート）として動く必要がない。

そして標準ポリシーでは、読み専用ソケットにどのようなアプリケーションも接続できる。

ポリシーは/etc/PolicyKit/PolicyKit.confに置かれたマスター設定ファイルによって管理者が変更できる。

PolicyKit.conf(5)マニュアルページに設定方法詳細の記述がある。

属性として、2つのlibvirtd操作が設定されている。1つは、読み専用のorg.libvirt.unix.monitorである。もう1つは、読み書き可能なorg.libvirt.unix.manageである。

例として、fredに読み書き権限を与え、joeには管理者パスワードを認証を要求する例を示す。このアクセス制御をするためには、以下の設定を、PolicyKit.confに追記する必要がある。

` `<match action="org.libvirt.unix.manage">
`   `<match user="fred">
`     `<return result="yes"/>
`   `</match>
` `</match>
` `<match action="org.libvirt.unix.manage">
`   `<match user="joe">
`     `<return result="auth_admin"/>
`   `</match>
` `</match>

### ユーザ名とパスワードによる認証

TCPソケットを平文のまま用いたlibvirtdは、標準でSASLを認証機構として用いる。

SASL機構は、標準では、Digest-MD5を用いる。これは、基本的なユーザ名とパスワード形式の認証である。

データストリームを暗号化する方法も提供している。このため平文のTCPソケットのセキュリティもTLSソケットを使った場合と同等のセキュリティである。このため、UNIXドメインソケット及びTLSソケットをSASL認証するように設定しておくことは望ましい。この設定は、libvirt.conf設定ファイルのauth_unix_ro, auth_unix_rw, auth_tlsでSASL認証するようにしておく。

使い始めの段階では、ユーザアカウントは定義されていない。このためクライアントがTCP接続することが出来ない。

ユーザを追加し、設定を行うためには、saslpasswd2コマンドを使う。

このコマンドを実行するに当たって、アプリケーションがlibvirtであることを明示的に示す必要がある。

この例では、fredをアカウントに追加する例を示している。

` # saslpasswd2 -a libvirt fred`
` Password: xxxxxx`
` Again (for verification): xxxxxx`

全アカウントのリストを見るためには、sasldblistuser2コマンドを使う。このコマンドでは、libvirtのユーザデータベースを指定する必要がある。このデータベースは/etc/libvirt/passwd.dbにある。

` # sasldblistusers2 -f /etc/libvirt/passwd.db`
` fred@t60wlan.home.berrange.com: userPassword`

最後に、ユーザアクセスを停止する場合、saslpasswd2コマンドを再び使う。

` # saslpasswd2 -a libvirt -d fred`

### ケルベロス認証

TCPソケットを平文のまま用いたlibvirtdは、標準でSASLを認証機構として用いる。

SASL機構は、標準では、Digest-MD5を用いる。これは、基本的なユーザ名とパスワード形式の認証である。

ケルベロス (Kerberos) 認証のシングルサインオンを有効にするには、libvirt用SASL設定ファイルを変更する必要がある。そのファイルは、/etc/sasl2/libvirt.confである。そして、mech_listパラメータは、digest-md5の代わりにgssapiに変更する必要がある。

もし、UNIXドメインソケットやTLSソケットに対してSASLが有効になっている場合、Kerberosは、SASLを使うことができる。DIGEST-MD5のように、ケルベロス認証機構は、セッションのデータ暗号化機構を提供する。

ディストリビューションによっては、SASL-Kerberosプラグインをデフォルトでインストールしない。この場合、cyrus-sasl-gssapiなどのパッケージをインストールすることが必要になる。

ケルベロス認証プラグインがインストールされているかどうか調べるためには、pluginviewerを実行して、gssapiがリストされるか確認する必要がある。

` # pluginviewer`
` ...snip...`
` Plugin "gssapiv2" [loaded],     API version: 4`
`         SASL mechanism: GSSAPI, best SSF: 56`
`         security flags: NO_ANONYMOUS|NO_PLAINTEXT|NO_ACTIVE|PASS_CREDENTIALS|MUTUAL_AUTH`
`         features: WANT_CLIENT_FIRST|PROXY_AUTHENTICATION|NEED_SERVER_FQDN`

次に、ケルベロス認証のレルムの管理者は、プリンシプルをlibvirtサーバ用に発行する必要がある。

プリンシプルは、ホスト毎に、libvirtdに対応して一つ割り当てる必要がある。

そして、プリンシプルは、libvirt/full.hostname@KERBEROS.REALMと名づける必要がある。

この作業は、通常kadmin.localコマンドをケルベロス認証サーバで実行して行われる。しかしながらケルベロス認証サーバによっては、サービスプリンシプルを設定するために他の方法が必要な場合もある。

一度生成されると、プリンシプルは、キータブとしてエクスポートされる。そしてlibvirtd向けには、/etc/libvirt/krb5.tabに設定される。

` # kadmin.local`
` kadmin.local: add_principal libvirt/foo.example.com`
` Enter password for principal "libvirt/foo.example.com@EXAMPLE.COM":`
` Re-enter password for principal "libvirt/foo.example.com@EXAMPLE.COM":`
` Principal "libvirt/foo.example.com@EXAMPLE.COM" created.`
` `
` kadmin.local:  ktadd -k /root/libvirt-foo-example.tab libvirt/foo.example.com@EXAMPLE.COM`
` Entry for principal libvirt/foo.example.com@EXAMPLE.COM with kvno 4, encryption type Triple DES cbc mode with HMAC/sha1     added to keytab WRFILE:/root/libvirt-foo-example.tab.`
` Entry for principal libvirt/foo.example.com@EXAMPLE.COM with kvno 4, encryption type ArcFour with HMAC/md5 added to keytab WRFILE:/root/libvirt-foo-example.tab.`
` Entry for principal libvirt/foo.example.com@EXAMPLE.COM with kvno 4, encryption type DES with HMAC/sha1 added to keytab WRFILE:/root/libvirt-foo-example.tab.`
` Entry for principal libvirt/foo.example.com@EXAMPLE.COM with kvno 4, encryption type DES cbc mode with RSA-MD5 added to keytab WRFILE:/root/libvirt-foo-example.tab.`
` `
` kadmin.local: quit`
` `
` # scp /root/libvirt-foo-example.tab root@foo.example.com:/etc/libvirt/krb5.tab`
` # rm /root/libvirt-foo-example.tab`

ケルベロス認証するlibvirtに接続したいアプリケーションがユーザプリンシプルを取得するためにkinitを実行する必要はほとんどない。 PAMがケルベロス認証向けに設定されている場合、デスクトップセッションにログインした時点で自動的に取得しているためである。

## 各種libvirtドライバ

### Xenドライバ

libvirtのXenドライバは、3.0.1以降のXenを制御することができる。

libvirtのXenドライバは、複数の制御方法の組み合わせでXen仮想機械を制御する。

  - XenD: libvirt Xenドライバを使うためにはXenDにアクセスできることが必須である。このドライバを使うためには、XenDの設定ファイル/etc/xen/xend-config.sxpでUNIXドメインソケットインタフェースを利用可能にしておく必要がある。そのためにはこのファイルで、(xend-unix-server yes) と設定しておく必要がある。このソケットでのアクセスパスは、特権ユーザ（ルート）に通常限られる。その他の選択肢としてHTTPインタフェースを使うことができる。しかしセキュリティに注意する必要がある。

<!-- end list -->

  - XenStoreD: Xenstoredにアクセスして情報を取得することは、ドメイン情報取得の際のCPUのオーバーヘッドを減らすことができる。
  - Hypercalls: ハイパーコールを発行して情報を取得する。ドメイン情報を取得するには、一番効率的なアクセス方法である。
  - XM config: 3.0.4以前のXenでは、XenDにおいて不活性ドメインの制御は出来なかった。このため、これらのXenを制御する場合、libvirtでは/etc/xenのディレクトリにXM設定ファイルを保存して不活性ドメインの制御をしている。このディレクトリに、設定ファイル以外を決しておいてはいけない。

### QEMU/KVMドライバ

libvirtのQEMUドライバは0.8.1以降のQEMUを管理することができる。そして、このドライバはQEMUコマンド書式で制御できるいずれの仮想機械にも適用できる。QEMU形式のVMには、KVMとXennerが含まれる。

利用する前に必要な条件は以下の通りである。

  - QEMU: ドライバは/usr/bin以下のqemu, qemu-system-x86_64, qemu-system-mips, qemu-system-mipsel, qemu-system-sparc, qemu-system-ppcの存在をチェックする。チェック結果は、XMLファイルのcapabilityの項目で見ることができる。
  - KVM: ドライバは/usr/bin/qemu-kvmコマンドと/dev/kvmのデバイスノードの存在をチェックする。もし両方存在すれば、ハードウェア支援機構前提のゲストドメインを使うことができる。
  - Xenner: ドライバは/usr/bin/xennerコマンドと/dev/kvmのデバイスノードの存在をチェックする。もし両方存在すれば、Xen準仮想化ドメインをKVMを用いて使うことができる。

### リモートドライバ

ネットワーク越しのハイパーバイザを管理することができる。

## 関連項目

  - [Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink")
  - [Pythonを使っている製品あるいはソフトウェアの一覧](../Page/Pythonを使っている製品あるいはソフトウェアの一覧.md "wikilink")

## 脚注

## 外部リンク

### libvirt本体と各種言語バインディング

  - [the virtualization API](http://libvirt.org/)
      - [リリース履歴](http://libvirt.org/news.html)
      - [libvirt Code量の変遷](http://berrange.com/~dan/libvirt-loc.png)
      - [コンパイル状況確認](http://builder.virt-manager.org/module-libvirt--devel.html)
      - [ソースコード](http://libvirt.org/git/?p=libvirt.git)
      - [libvirtドライバ毎機能の一覧表](http://libvirt.org/hvsupport.html)
  - [Perl bindings](http://search.cpan.org/~danberr/Sys-Virt-0.1.1/)
  - [Ruby bindings](http://libvirt.org/ruby/)
  - [OCaml bindings](http://libvirt.org/ocaml/)
  - [Java bindings](ftp://libvirt.org/libvirt/java/)
  - [CIM provider](http://libvirt.org/CIM/) - [DMTFが策定している](../Page/Distributed_Management_Task_Force.md "wikilink")[CIMの仮想機械に関するインタフェースを実装したものである](../Page/Common_Information_Model.md "wikilink")。Libvirtがサポートしている仮想機械のうち、Xen, KVM, Linux Containersの3種類をサポートしている。なお、サポートしている仕様書は、src/profiles.hの記述を参照のこと。なお、Xenの外部プロジェクトとして進んでいたXen-CIMは、休眠プロジェクト\[[http://lists.xensource.com/archives/html/xen-cim/2008-03/msg00001.html\]になっている。そして、Xenを使う場合は、Citrixの提供するKenshoもしくは、本プロジェクトのコードを使う必要がある](http://lists.xensource.com/archives/html/xen-cim/2008-03/msg00001.html%5Dになっている。そして、Xenを使う場合は、Citrixの提供するKenshoもしくは、本プロジェクトのコードを使う必要がある)。
      - [CIMテスト状況](http://wiki.libvirt.org/page/Cimtest)

<!-- end list -->

  - [Windows Support](http://libvirt.org/windows.html) - [MinGW](../Page/MinGW.md "wikilink")のコンパイラを用いてバイナリを作成することができる。詳細は以下のページを参照のこと[1](http://libvirt.org/windows.html)。また、WindowsでのAPIの[glibc](https://ja.wikipedia.org/wiki/glibc "wikilink")との非互換はかなり大きいが、GNU Portability Library ([Gnulib](../Page/Gnulib.md "wikilink")) をlibvirtパッケージの中に取り込むことにより、互換性の手間を回避している。

### LibvirtAPIを使ったアプリケーション

  - [アプリケーションリスト](http://libvirt.org/apps.html)
  - [virt-manager（仮想機械運用管理ソフト）](http://virt-manager.et.redhat.com/) - 仮想機械インストーラvirt-installなどもこのページにある。
  - [virt-top（仮想機械版top）](http://et.redhat.com/~rjones/virt-top/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")

1.  [Virtual Machine Manager](http://virt-manager.et.redhat.com/)