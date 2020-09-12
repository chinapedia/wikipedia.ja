> この記事は[Chef \(ソフトウェア\)](https://ja.wikipedia.org/wiki/Chef_\(ソフトウェア\))から翻訳されています。


は企業であり、[Ruby](../Page/Ruby.md "wikilink")と[Erlang](../Page/Erlang.md "wikilink")で記述された[構成管理](../Page/構成管理.md "wikilink")ツールの名前である。システム構成の「レシピ」の記述には、ピュアRubyの[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink") （DSL）を使用する。 Chefは、会社のサーバーの構成と保守のタスクを合理化するために使用され、Internap、[Amazon EC2](https://ja.wikipedia.org/wiki/Amazon_Elastic_Compute_Cloud "wikilink")、[Google Cloud Platform](https://ja.wikipedia.org/wiki/Google_Cloud_Platform "wikilink")、[Oracle Cloud](https://ja.wikipedia.org/wiki/Oracle_Cloud "wikilink")、[OpenStack](https://ja.wikipedia.org/wiki/OpenStack "wikilink")、[SoftLayer](https://ja.wikipedia.org/wiki/SoftLayer "wikilink")、[Microsoft Azure](https://ja.wikipedia.org/wiki/Microsoft_Azure "wikilink")、Rackspaceなどのクラウドベースのプラットフォームと統合して、自動的にプロビジョニングし、新しいマシンを構成する。 Chefには、小規模システムと大規模システムの両方に対応するソリューションが含まれており、それぞれの範囲に応じた機能と価格が設定されている。

## 機能

ユーザーは、Chef がどのようにサーバアプリケーションやユーティリティ (例えば [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink")、[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink") や [Hadoop](https://ja.wikipedia.org/wiki/Hadoop "wikilink")) を管理・設定するかを「レシピ」に書き込む。 レシピは管理の簡単のために「クックブック」としてまとめることができる。 レシピには一連のリソースがどのような状態であるべきか、例えば[パッケージがインストールされているとか](../Page/パッケージ管理システム.md "wikilink")、[サービスが起動している](../Page/デーモン_\(ソフトウェア\).md "wikilink")、あるいは[ファイルが書き込まれている状態であるべきことを記述する](../Page/ファイル_\(コンピュータ\).md "wikilink")。 これらのリソースは、実行するソフトウェアを特定のバージョンに設定することができ、ソフトウェアが依存性に基づいて正しい順番でインストールされることを保証することが可能である。 Chefは、それぞれのリソースが正しく設定されるようにし、望ましい (*desired*) 状態でないリソースを修正する。 \[1\]

Chef は[クライアント/サーバモードで](../Page/クライアントサーバモデル.md "wikilink")、あるいは「chef-solo」と呼ばれる[スタンドアローン](../Page/スタンドアローン.md "wikilink")設定で実行できる。 クライアント/サーバモードでは、Chef クライアントは[ノードの様々な属性を](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\)#分散システムのノード "wikilink") Chef サーバへ送信する。 サーバーは [Elasticsearch](https://ja.wikipedia.org/wiki/Elasticsearch "wikilink") を使ってこれらの属性をインデックスし、この情報を問い合わせる API をクライアントに提供する。 Chef レシピはこれらの属性を問い合わせ、結果のデータを使ってノードを設定するのに役立てることができる。

もともと Chef は [Linux](../Page/Linux.md "wikilink") を管理するのに使われていたが、後のバージョンでは [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") にも同様に使用できるようになった\[2\]。

Linux では 、[Ansible](https://ja.wikipedia.org/wiki/Ansible "wikilink")、[Puppet](https://ja.wikipedia.org/wiki/Puppet_\(ソフトウェア\) "wikilink") に並んでメジャーな構成管理システムの1つである\[3\]\[4\]。 構成管理ツールである一方、Chef は Puppet や Ansible と並び [Infrastructure as Code](https://ja.wikipedia.org/wiki/Infrastructure_as_Code "wikilink") (IAC) ツールの1つでもある\[5\]。

## プラットフォームサポート

Chefは、クライアントおよびサーバー製品のサポートされるプラットフォームマトリックスに従って、複数のプラットフォームでサポートされる \[6\]。クライアントの主要なプラットフォームサポートには、[AIX](../Page/AIX.md "wikilink")、[RHEL](../Page/Red_Hat_Enterprise_Linux.md "wikilink") / [CentOS](../Page/CentOS.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[OS X](../Page/MacOS.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Microsoft Windowsおよび](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Ubuntu](../Page/Ubuntu.md "wikilink")が含まれる。 追加のクライアントプラットフォームには、[Arch Linux](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")、[Debian](../Page/Debian.md "wikilink")、 [Fedora](../Page/Fedora.md "wikilink")が含まれる。Chef Serverは、[RHEL](../Page/Red_Hat_Enterprise_Linux.md "wikilink") / [CentOS](../Page/CentOS.md "wikilink")、[Oracle Linux](../Page/Oracle_Linux.md "wikilink")、[Oracle Cloud](https://ja.wikipedia.org/wiki/Oracle_Cloud "wikilink")、[Ubuntu](../Page/Ubuntu.md "wikilink")でサポートされている。

## 利用企業

Chefは[Facebook](../Page/Facebook.md "wikilink") \[7\]、[AWS OpsWorks](https://ja.wikipedia.org/wiki/Amazon_Web_Services "wikilink")、HPパブリッククラウド \[8\]、[Prezi](https://ja.wikipedia.org/wiki/Prezi "wikilink") \[9\]、BlackLine、および[アメリカ合衆国移民・関税執行局](https://ja.wikipedia.org/wiki/アメリカ合衆国移民・関税執行局 "wikilink")によって使用されている \[10\]。

## 関連項目

  - [Ansible (ソフトウェア)](https://ja.wikipedia.org/wiki/Ansible_\(ソフトウェア\) "wikilink")

  -
  - [DevOps](https://ja.wikipedia.org/wiki/DevOps "wikilink")

  -
  -
  - [Puppet](https://ja.wikipedia.org/wiki/Puppet_\(ソフトウェア\) "wikilink")

  -
  -
## 参考文献

## 外部リンク

  -
  - [Chef on GitHub](https://github.com/chef/chef)

[Category:構成管理](https://ja.wikipedia.org/wiki/Category:構成管理 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:Ruby](https://ja.wikipedia.org/wiki/Category:Ruby "wikilink")

1.
2.
3.  .
4.
5.
6.
7.
8.
9.
10.