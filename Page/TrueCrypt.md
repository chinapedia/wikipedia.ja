> この記事は[TrueCrypt](https://ja.wikipedia.org/wiki/TrueCrypt)から翻訳されています。


**TrueCrypt**（トゥルークリプト）とは、[暗号](../Page/暗号.md "wikilink")化された[仮想ディスク](https://ja.wikipedia.org/wiki/仮想ディスク "wikilink")を作成・利用するソフトウエア。仮想ディスクは[ファイルとして作成するだけでなく](../Page/ファイル_\(コンピュータ\).md "wikilink")、[パーティション](../Page/パーティション.md "wikilink")自体も対象にできる。ユーザは、作成された仮想ディスクを[USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")などと同じ感覚で[リムーバブルディスク](../Page/リムーバブルディスク.md "wikilink")ドライブとして[マウントすることで利用できる](https://ja.wikipedia.org/wiki/mount_\(UNIX\) "wikilink")。また、Windows版TrueCryptではシステムドライブ自体も暗号化することが出来る\[1\]。

このソフトウエアは、TrueCrypt License\[2\]の下で無償で利用できる。

現在は開発者から「安全ではない」とのメッセージが出されており、使用を中止し[BitLocker](https://ja.wikipedia.org/wiki/BitLocker "wikilink")など他のソリューションにのりかえることが推奨されている\[3\]。

代替としてはTrueCryptのソースコードに基づいた[VeraCrypt](https://ja.wikipedia.org/wiki/VeraCrypt "wikilink")や[CipherShed](https://ja.wikipedia.org/wiki/CipherShed "wikilink")などフリーウェアのプロジェクトがある。

## 開発終了

2014年5月28日に、TrueCryptの公式サイト `truecrypt.org` が、[HTTP 301 "Moved Permanently"（恒久的に移動した）によって訪問者を](https://ja.wikipedia.org/wiki/HTTPステータスコード#3xx_Redirection_リダイレクション "wikilink") `truecrypt.sourceforge.org` へ転送するようになった。転送先では、Windows XPのサポート終了に合わせて、TrueCryptの開発を2014年5月で終了した旨が警告されている。新しいバージョンのWindowsではOS標準の[BitLocker](https://ja.wikipedia.org/wiki/BitLocker "wikilink")が、LinuxやMac OS Xでも類似のシステムがあることから、TrueCryptはもはや不要であり、TrueCryptで暗号化されているデータをBitLockerに移行することが推奨されている。SourceForgeのプロジェクトページ `sourceforge.net/truecrypt` にも同じメッセージが表示されるようになり、プロジェクトの状況は "inactive"（活動していない）に変更された\[4\]。同時に、暗号化機能を除去し、既存の暗号化済みデータの復号機能のみを有するバージョン7.2がリリースされた。

開発終了の発表当初、この発表および新しくリリースされたバージョン7.2が本物なのか疑問が呈された\[5\]\[6\]\[7\]。ITコミュニティでは、この発表について様々な説が示された\[8\]\[9\]。[truecrypt.ch](http://truecrypt.ch/)\[10\]、[CipherShed.org](http://ciphershed.org/)およびクラウドファンドによってTrueCrypt 7.1aのセキュリティ監査を行っていたグループ\[11\]が、それぞれ独自にTrueCryptの[フォークを行うことを発表した](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。

Gibson Research Corporationによると、Steven Barnhartが、TrueCrypt Foundationのメンバーの一人にメールを送り、返事を受け取っている。それによると、開発終了の発表は「（プロジェクトを続けることに対する）興味を失った」ためであるとのことである\[12\]。

## 仕様・機能

  - TrueCryptは[暗号](../Page/暗号.md "wikilink")化された[仮想ディスク](https://ja.wikipedia.org/wiki/仮想ディスク "wikilink")を作成する機能を持つ。この仮想ディスクは「TrueCryptボリューム」と呼ばれる。
  - ボリュームのフォーマット形式はWindowsでは[FAT](../Page/File_Allocation_Table.md "wikilink") (FAT12, FAT16, FAT32) または[NTFS](../Page/NT_File_System.md "wikilink")、LinuxではFAT (VFAT), [ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink"), [ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink"), [ext4](https://ja.wikipedia.org/wiki/ext4 "wikilink")である。
  - 利用できる暗号化アルゴリズム（[ブロック暗号](../Page/ブロック暗号.md "wikilink")）は、[AES](../Page/Advanced_Encryption_Standard.md "wikilink"), [Serpent](https://ja.wikipedia.org/wiki/Serpent_\(暗号\) "wikilink"), [Twofish](../Page/Twofish.md "wikilink")（いずれも鍵長256ビット、ブロック長128ビット）の単独使用あるいは AES-Twofish, AES-Twofish-Serpent, Serpent-AES, Serpent-Twofish-AES, Twofish-Serpentのカスケード方式の計8種類である。
  - 利用できるハッシュアルゴリズム（[暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")）は、[RIPEMD](https://ja.wikipedia.org/wiki/RIPEMD "wikilink")-160（ハッシュ長160ビット）, [SHA-512](https://ja.wikipedia.org/wiki/SHA-2 "wikilink"), [Whirlpool](https://ja.wikipedia.org/wiki/Whirlpool_\(ハッシュ関数\) "wikilink")（いずれもハッシュ長512ビット）の3種類である。
  - ユーザは事前に作成されたTrueCryptボリュームを、TrueCryptのGUIを用いて[マウントすることにより利用する](https://ja.wikipedia.org/wiki/mount_\(UNIX\) "wikilink")。
  - TrueCryptボリュームをマウントするときに、パスワードによる認証またはキーファイルによる認証が行われる。
  - 一つのTrueCryptボリューム中に「外殻ボリューム」と「隠しボリューム」を作成することが出来る。マウント時にどちらのボリュームをマウントするかは、パスワードによって選択される。これは、脅迫等によってボリュームをマウントすることを強制された場合、「隠しボリューム」を開示しないために必要な機能である。
  - Windows、Mac OS X、Linux用のTrueCryptで作成されたTrueCryptボリュームはそれぞれ互換性があるため、相互に利用が可能である。

## インストール方法

  - [RHEL系](../Page/Red_Hat_Enterprise_Linux.md "wikilink")（[CentOS](../Page/CentOS.md "wikilink")等）のLinuxの場合

<!-- end list -->

  -
    [rpmforge](https://rpmrepo.org/RPMforge)リポジトリに接続して、`yum install truecrypt` によりインストール可能。
    なお、/usr/bin/truecryptコマンドはroot権限でしか機能しないため、ユーザ権限で利用する場合は[sudo](https://ja.wikipedia.org/wiki/sudo "wikilink")を利用する必要がある（visudoコマンドで実行権限を設定した後、`sudo truecrypt`を利用する）。

<!-- end list -->

  - [Debian](../Page/Debian.md "wikilink")系のLinuxの場合

<!-- end list -->

  -
    公式サイトで配布されているdebパッケージをインストールする。
    ユーザ権限での制限はRHEL系と同様。

<!-- end list -->

  - Windowsの場合

<!-- end list -->

  -
    公式サイトで配布されているセットアップファイルを実行する。
    Linux版とは違い、GUIはユーザ権限でも利用可能である。

## 情報の流出・盗難の予防

TrueCryptが作成した仮想ディスク（TrueCryptボリューム）は暗号化されているため、この仮想ディスクを納めた[コンピュータ](../Page/コンピュータ.md "wikilink")本体や、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、[USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")、[CD等のメディアが外部流出した場合でも](../Page/コンパクトディスク.md "wikilink")、内部に格納されているデータが復号（解読）されない限り情報流出することは無い。

例えば、機密データをUSBメモリに格納して持ち歩く場合、TrueCryptが作成した仮想ディスクとして格納すれば、たとえUSBメモリを紛失したり盗難されたりしたとしても、実質的な情報流出にはならない。

## 情報の流出・盗難を予防できない可能性

  - TrueCryptが作成した仮想ディスク（TrueCryptボリューム）が流出した場合で、その仮想ディスクに脆弱なパスワードが付与されていたり、同時にキーファイルも流出する等により、データを復号（解読）される可能性がある。

<!-- end list -->

  -
    *対抗手段：推測できない長いパスワードを付与。キーファイルはそれと推測されないファイル名にし、別に保存する等*

<!-- end list -->

  - TrueCryptが作成した仮想ディスク（TrueCryptボリューム）をマウントする時に、適切なアクセスコントロール（他のユーザがアクセス出来ない）を設定していない場合は、そのコンピュータにアクセスできる他者が仮想ディスクにアクセスすることが出来る場合がある。

<!-- end list -->

  -
    *対抗手段：Linuxの場合であれば、mount状態のuidとgidがユーザ自身であり、umaskが077であることを確認する*

<!-- end list -->

  - TrueCryptが作成した仮想ディスク上のファイルを、アプリケーションソフトで利用する場合、コンピュータの[メモリ上には復号](../Page/主記憶装置.md "wikilink")（解読）されたファイルのデータが展開されるとともに、場合によっては[テンポラリファイル](https://ja.wikipedia.org/wiki/テンポラリファイル "wikilink")や[スワップファイルに書き出されることもある](../Page/仮想記憶.md "wikilink")。これらは他者からアクセスできる場合がある。

<!-- end list -->

  -
    *対抗手段：OSの設定をスワップファイルを用いない設定とする。Linuxであれば、アプリケーション利用前にswapoffコマンドを実行すれば良い。Windowsであれば、コントロールパネルで仮想メモリを利用しない設定とすれば良い（再起動が必要）。また、利用するアプリケーション毎にテンポラリファイルがどこに作成されるか、常に注意を払う必要がある*

## 情報にアクセス不可能・情報喪失になる可能性

  - TrueCryptで作成した仮想ディスク（TrueCryptボリューム）のパスワードを忘れたり、キーファイルを紛失した場合は、誰でもいかなる方法でもアクセス・復号がその情報が意味を持つ時間内には不可能になり、実質的な意味として情報を喪失する。

## ライセンス

TrueCryptは、独自の "TrueCrypt License" によってリリースされている\[13\]\[14\]。このライセンスは、広く受け入れられている[オープンソース](../Page/オープンソース.md "wikilink")ライセンスではなく、配布や著作権に関する制限があることから[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")に認定されている[フリーソフトウェアライセンス](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス "wikilink")でもない\[15\]。TrueCrypt　7.1aのリリース時点で、TrueCrypt Licenseのバージョンは3.0であった。

2013年10月に、[Open Source Initiativeのメーリングリスト上での議論で](../Page/Open_Source_Initiative.md "wikilink")、オープンソースの定義に適合するようTrueCrypt Licenseの修正が進んでいることが示唆されたが、オープンソースソフトウェアであることがはっきりと示されない限り、それが受け入れられる見込みは少ないとされる\[16\]\[17\]。

OSI代表のSimon Phippsによると、

> ...（TrueCryptが）自らを「オープンソース」だと主張することは全く不適切である。単にOSIが認定していないライセンスだということではなく、問題を抱えていることがわかっているライセンスでリリースするものに「オープンソース」という用語を用いることは受け入れられない。\[18\]

著作権の制限やそのほかの法的問題の状況が不透明であることから\[19\]、TrueCrypt Licenseは主要な[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")からは[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")だとはみなされておらず、[Debian](../Page/Debian.md "wikilink")\[20\]、[Ubuntu](../Page/Ubuntu.md "wikilink")\[21\]、[Fedora](../Page/Fedora.md "wikilink")\[22\]、[openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")\[23\]、[Gentoo](https://ja.wikipedia.org/wiki/Gentoo "wikilink")\[24\]には同梱されていない。

このライセンスの利用者に対して、ソフトウェアを改変する権利あるいは他のプロジェクトでそのソフトウェアを使用する権利が認められているのかもはっきりとはしていない。暗号学者であるMatthew D. Greenは「（TrueCryptの開発者には）ライセンスの状況を修正することを含めて、TrueCryptのソースコードを他者が利用しやすくするよう、できることが多くあったはずだ」と述べ、他者が自分たちのソースコードをもとに独自にソフトウェアをビルドすることを認めたくなかったのだろうと推測している\[25\]。

2014年6月16日に、Matthew Greenによるライセンスに関する電子メールでの問い合わせに開発者を名乗る人物から返答があった。それによると、1）TrueCryptのライセンスをオープンソースに適合するものに変更するつもりはない、2）TrueCryptは[フォークされるべきではない](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")、3）新しいバージョンを作成したいのであればスクラッチから始めるべきであるとのことであった\[26\]\[27\]。

### 開発終了とライセンスバージョン3.1

2014年5月28日に、TrueCryptの開発終了が発表され、新たにバージョン7.2のソフトウェアがリリースされた。これに合わせてTrueCrypt Licenseにも、配布の際に公式サイトへのリンクや特定の文言を加えることを要求していた条項が除去され、バージョン3.1のライセンスとなった\[28\]。

## 脚注

## 関連項目

  - [ディスクの暗号化](https://ja.wikipedia.org/wiki/w:en:Disk_encryption "wikilink")（Wikipedia英語版の記事）
  - [暗号](../Page/暗号.md "wikilink")
  - [Advanced Encryption Standard](../Page/Advanced_Encryption_Standard.md "wikilink")
  - [LUKS](https://ja.wikipedia.org/wiki/LUKS "wikilink")（ディスク暗号化ソリューションの一つ）
  - [GnuPG](https://ja.wikipedia.org/wiki/GnuPG "wikilink")（公開鍵暗号化方式によるファイルの暗号化ソフトウエア）
  - [VeraCrypt](https://ja.wikipedia.org/wiki/VeraCrypt "wikilink")（TrueCryptのソースコードを[フォークしたTrueCrypt互換の暗号化ソフトウェアの一つ](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")）
  - [CipherShed](https://ja.wikipedia.org/wiki/CipherShed "wikilink")（TrueCryptのソースコードをフォークしたTrueCrypt互換の暗号化ソフトウェアの一つ）
  - [データの完全消去](https://ja.wikipedia.org/wiki/データの完全消去 "wikilink")

## 外部リンク

  - [TrueCrypt 公式サイト](http://www.truecrypt.org/)（Linux版、Mac OS X版、Windows版のダウンロードもここより行う）
  - [＠IT 暗号化仮想ドライブで手軽にファイルを暗号化](http://www.atmarkit.co.jp/fsecurity/column/ueno/44.html) （2007/1/27付の記事）
  - [窓の杜 システムドライブの暗号化で情報漏洩を防げる「TrueCrypt」v5.0](http://www.forest.impress.co.jp/article/2008/02/08/truecrypt5.html) （2008/02/08付の記事）

[Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:2004年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2004年のソフトウェア "wikilink")

1.
2.
3.  <http://internet.watch.impress.co.jp/docs/news/20140530_651011.html>
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.