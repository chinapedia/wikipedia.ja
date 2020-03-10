> この記事は[Security-Enhanced Linux](https://ja.wikipedia.org/wiki/Security-Enhanced_Linux)から翻訳されています。


**Security-Enhanced Linux** (**SELinux**) は、[アメリカ国家安全保障局](../Page/アメリカ国家安全保障局.md "wikilink") (NSA) が[GPL下で提供している](../Page/GNU_General_Public_License.md "wikilink")、[Linux](../Page/Linux.md "wikilink")の[カーネル](../Page/カーネル.md "wikilink")に[強制アクセス制御](https://ja.wikipedia.org/wiki/強制アクセス制御 "wikilink") (MAC) 機能を付加する[モジュール](../Page/モジュール.md "wikilink")の名称。名前から勘違いされることが多いが、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")の一つではない。

## 概要

SELinuxは[1992年](../Page/1992年.md "wikilink")、NSAが主体となってFlukeという[OS上におけるMAC機能の研究のために開発された](../Page/オペレーティングシステム.md "wikilink")。MAC機能はセキュリティの高いOSの提供を可能にするが、主に[Multi Level Securityと呼ばれる機能で提供されている](https://ja.wikipedia.org/wiki/Multi_Level_Security "wikilink")。この機能では、アクセスする対象（サブジェクト）すべてに階層化された権限が与えられる一方、アクセスされる対象（オブジェクト）にもすべて階層化された情報の重要度に応じたラベルを付加する。このことによってアクセス制御を行うものだが、柔軟に実装するには複雑化してしまうという欠点があった。

SELinuxではこの問題点を解決するために、Flaskというベースアーキテクチャを開発し、Flask上でのセキュリティポリシー言語を記述することにより、あらゆるセキュリティモデルに対して柔軟に対応できるように設計された。また、セキュリティポリシー言語とセキュリティチェックの仕組みはそれぞれ独立しており、ポリシーがアーキテクチャに制約されないという特長がある。

[2000年](../Page/2000年.md "wikilink")[12月22日](../Page/12月22日.md "wikilink")に一般公開され、[2003年](../Page/2003年.md "wikilink")[8月13日](../Page/8月13日.md "wikilink")には[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")2.6において、新機能である[Linux Security Modules](https://ja.wikipedia.org/wiki/Linux_Security_Modules "wikilink") (LSM) の拡張モジュールとしてメインライン化された。

## 内容

従来の [Linux](../Page/Linux.md "wikilink")（もっと広くいえば[UNIX](../Page/UNIX.md "wikilink")全体）では、ディレクトリやファイルといったリソースに対するアクセス制限は、 それぞれの許可情報（パーミッション）に基づいている。

このパーミッションは「オーナー」・「グループ」・「その他のユーザ」に対して、それぞれ「読み込み」・「書き込み」・「実行」の許可を設定するものであり、これらのパーミッションを「無視して」アクセス可能なユーザとして root（[スーパーユーザー](../Page/スーパーユーザー.md "wikilink")） が君臨している。 すなわち、すべての権限が root に集中しているため、いちど root のパスワードが漏洩すると、システム全体に致命的な被害を及ぼすという欠点がある。

SELinux はこの事実に注目し、セキュリティの対象に応じて[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[FTPといった](../Page/File_Transfer_Protocol.md "wikilink")[プロセス](../Page/プロセス.md "wikilink")ごとにアクセス制限をかける Type Enforcement (TE)と、rootも含む全てのユーザに関して制限をかける[ロールベースアクセス](../Page/ロールベースアクセス制御.md "wikilink")(RBAC)などで制御し、rootに権限が集中することを防いでいる。

### TE

TE では全てのプロセスに対して「ドメイン」と呼ばれるラベルを付加する。またリソースに対しても同じく「タイプ」と呼ばれるラベルを付与する。さらに各リソースには「アクセス・ベクタ」が割り当てられる。アクセス・ベクタとは「読み込み」、「書き込み」といったリソースに対して行える操作の種類のことである。 これにより各ドメインとタイプに対して許可されるアクセス・ベクタを、セキュリティーポリシーとして設定可能にしている。

### RBAC

RBAC は「ロール」と呼ばれるいくつかのドメインを束ねたものを設定し、それをユーザに付与する仕組みである。ユーザは付与されたロール内のドメインの権限でのみファイルにアクセス可能である。この機能により各ユーザ毎に細かく権限を付与、制限することが可能である。このため例えば Web管理者には Web管理に必要なファイルのみにアクセス可能にする、という風にユーザに応じて権限の役割分担が行える。このことにより仮にあるユーザのパスワードが漏洩しても、被害を受けるのはそのユーザが持つ権限に対してのみであり、被害を最小限に押さえることができる。

## 脚注

## 関連項目

  - [grsecurity](https://ja.wikipedia.org/wiki/grsecurity "wikilink")
  - [TOMOYO Linux](https://ja.wikipedia.org/wiki/TOMOYO_Linux "wikilink")
  - [AppArmor](https://ja.wikipedia.org/wiki/AppArmor "wikilink")

## 外部リンク

  - [Security-Enhanced Linux](https://www.nsa.gov/what-we-do/research/selinux/)
  - [SELinux Project Wiki](http://selinuxproject.org/)
  - [日本セキュアOSユーザ会](http://www.secureos.jp/)

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:アメリカ国家安全保障局](https://ja.wikipedia.org/wiki/Category:アメリカ国家安全保障局 "wikilink")