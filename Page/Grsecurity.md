> この記事は[Grsecurity](https://ja.wikipedia.org/wiki/Grsecurity)から翻訳されています。


**grsecurity** は、[コンピュータセキュリティ](../Page/コンピュータセキュリティ.md "wikilink")強化のための[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")用[パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")セットである。ユーザーをログイン可能にしている[Webサーバ](../Page/Webサーバ.md "wikilink")など、信頼できるかどうか不明なリモートからのコネクション要求を受け付けるシステムで主に利用される。

grsecurity は [GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") でリリースされている[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## PaX

grsecurity に含まれる主要コンポーネントは [PaX](../Page/PaX.md "wikilink") である。これは、[スタック](../Page/スタック.md "wikilink")などに使われているメモリを実行不可能とし、プログラムコードが書かれているメモリを書き込み不能と設定する。これによって[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")などの脆弱性を利用した攻撃に対する防御とする。また、[ASLR](https://ja.wikipedia.org/wiki/ASLR "wikilink") (Address Space Layout Randomization) によって仮想空間内の配置を無作為に変化させ、特定の内容が特定のアドレスにあることに依存した攻撃を防ぐ。PaX 自体は grsecurity の開発者らが開発しているわけではなく、grsecurity とは別に入手可能である。

## ロールベースアクセス制御

grsecurity には、完全な[ロールベースアクセス制御](../Page/ロールベースアクセス制御.md "wikilink") (RBAC) システムを提供するコンポーネントも含まれる。RBAC は従来の[UNIX](../Page/UNIX.md "wikilink")の[アクセス制御リスト](https://ja.wikipedia.org/wiki/アクセス制御リスト "wikilink")よりも厳密なアクセス制限が可能で、完全な最小権限システム（ユーザーやプロセスが動作に必要な最小限の権限のみを持ち、余分な権限を持たせないシステム）を構築する基礎となる。これにより、攻撃者がシステムの機密情報を入手または破壊する可能性は劇的に削減できる。RBAC は「役割(role)」の集合を通して動作する。各役割には何ができて何ができないかという制限を個々に設定でき、これによってポリシーが形成される（ポリシーは修正可能）。

## その他の機能

grsecurity では、Linuxカーネルの[監査](../Page/監査.md "wikilink")機能も拡張している。特定のユーザーのグループを監査するよう設定したり、デバイスのmount/unmountを監査したり、システムの日時の変更を監査したりといった設定が可能である。

trusted path execution は、誰でも書き込める状態の[実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")の実行を防ぐオプション機能である。ユーザーが誤って（あるいは故意に）持ち込んだ[マルウェア](https://ja.wikipedia.org/wiki/マルウェア "wikilink")の実行を防ぐことができる。

grsecurity はまた、[chroot](https://ja.wikipedia.org/wiki/chroot "wikilink")「監獄」のセキュリティを強化する。chroot監獄は特定のプロセスをシステムの他の部分から隔離するのに使われ、何らかのダメージが他に及ばないようにする。しかし、chroot監獄を破る方法も存在する。grsecurity はそれらの方法を使えないようにする。

他にも、[dmesg](https://ja.wikipedia.org/wiki/dmesg "wikilink") や [netstat](https://ja.wikipedia.org/wiki/netstat "wikilink") コマンドを[スーパーユーザー](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")以外は実行できないようにし、一般ユーザーがシステムについて余分な知識を獲得できないようにする機能もある。

## 関連項目

  - [PaX](../Page/PaX.md "wikilink")
  - [Linux Security Modules](https://ja.wikipedia.org/wiki/Linux_Security_Modules "wikilink") (LSM) grsecurityの作者はLSMを使用しないことに言及している。[1](http://www.grsecurity.net/lsm.php)
  - [Exec Shield](https://ja.wikipedia.org/wiki/Exec_Shield "wikilink")
  - [Security-Enhanced Linux](https://ja.wikipedia.org/wiki/Security-Enhanced_Linux "wikilink")

## 外部リンク

  - [公式サイト](http://www.grsecurity.net/)
  - [grsecurity on freshmeat](http://freshmeat.net/projects/grsecurity/)

[Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")