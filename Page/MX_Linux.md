> この記事は[MX Linux](https://ja.wikipedia.org/wiki/MX_Linux)から翻訳されています。


**MX Linux**は、中量級の[Linux](../Page/Linux.md "wikilink")[OS](../Page/OS.md "wikilink")で、[Debian](../Page/Debian.md "wikilink")安定版がベースになっている。また、MXコミュニティによって作られ\[1\]\[2\]\[3\]\[4\]\[5\]\[6\]\[7\]\[8\]\[9\]\[10\]\[11\]、パッケージングされた追加の[ソフトウェア](../Page/ソフトウェア.md "wikilink")と共に、[antiX](https://ja.wikipedia.org/wiki/antiX "wikilink")のコンポーネントを用いている。MXは、antiXと以前の[MEPIS](../Page/MEPIS.md "wikilink")コミュニティの間の協力的事業として開発されており、それぞれの[ディストリビューション](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")からベストなツールと特色を用いることを狙っている。コミュニティは、プロジェクトのゴールについて”洗練されて効果的な[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")を簡単な設定と高い安定性\[12\]、強固なパフォーマンスに結びつける"\[13\]ことだと述べている。MX Linuxは、[Xfce](../Page/Xfce.md "wikilink")を用いており、[KDE Plasmaや他の環境も後から加えることができると共に](../Page/KDE.md "wikilink")、"スピンオフ"[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")としても入手できる。

## 歴史

MX Linuxは、[2013年](../Page/2013年.md "wikilink")の12月に、MEPISコミュニティのメンバーの間で行われた将来のオプションに関する議論の中で始まった\[14\]。これにantiXの開発者たちが加わり、ISOビルドシステムに加え、[Live USB/DVDの技術を持ち込んだ](https://ja.wikipedia.org/wiki/LiveCD "wikilink")。[DistroWatch](https://ja.wikipedia.org/wiki/DistroWatch "wikilink")に掲載されるために、MX Linuxは最初antiXのバージョンであると提示された。MXは、その[独自のDitroWatchのページ](https://distrowatch.com/table.php?distribution=mx)をMX-16の最初のパブリックベータのリリース（[2016年](../Page/2016年.md "wikilink")[11月2日](../Page/11月2日.md "wikilink")）に受け取った。

MX-14シリーズは、Debian安定板（コード名 wheezy）に基づいており、最初はXfce 4.10、その後14.4のリリースに併せてXfce 4.12を用いた。MX-14のバージョンは、CDにフィットするように意図されて構築されており、限られた[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")のみがふくまれるという制限があった。このシリーズでは、しばしば複雑で不透明なものとなる一般的なタスクを行うユーザーを助けることを意図してデザインされた、手軽な[ユーティリティ](https://ja.wikipedia.org/wiki/ユーティリティ "wikilink")のコレクション、MXツールの漸進的な進化を見て取ることができる。

MX-15は、Debian安定版（jessie）にベースを移し、systemd-shimを使うものとなった。これは、[systemd](https://ja.wikipedia.org/wiki/systemd "wikilink")をインストールするものの、デフォルト（既定）の[init](https://ja.wikipedia.org/wiki/init "wikilink")は[sysvinitであることを意味する](https://ja.wikipedia.org/wiki/init "wikilink")\[15\]。サイズの制限は上がり、ユーザーにフルターンキーの製品を示すことを開発者に可能にした。また、本質的なMXツールの拡張が行われた。

MX-16は依然として、Debian安定版(jessie)に基くものの、アプリケーションは、他のソースからのものも含め、多くがバックポートされ、また加えられた。また、MXツールへの追加や改善が行われた。これには、antiXの開発成果の受け入れや、拡張されたサポート、完全に新しいアイコン、テーマ、壁紙の組み合わせが含まれる。

MX-16.1には、MX16以降のバグ修正と改善が含まれる。また、同リリースには、新しいキングフィッシャーテーマの追加や、更新されたMXツール、改善されたドキュメンテーションや、新しい翻訳の成果が含まれる。

MX-17は、そのベースをDebian 9（stretch）に変更し、アップグレードされたアートワークや、新しいMXツール、antiXを通じて進歩したライブ・オペレーションなど、[MX Blog](https://mxlinux.org/blog/mx-17-released-december-15-2017)に詳細が書かれた変更が含まれる。

MX-18では、MXツールの開発が進められ、最新の[カーネル](../Page/カーネル.md "wikilink")の導入、ディスク全体の[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")、MX Boot オプションを通じて機能する[GRUB](https://ja.wikipedia.org/wiki/GRUB "wikilink")のテーマやスプラッシュ画面が追加された。また、新しいアートワークや改善された翻訳も含まれている。詳細は[MX Blog](https://mxlinux.org/blog/mx-18-continuum-now-available)に記載されている。

MX-19は、そのベースをDebian 10（buster）にアップグレードし、デフォルトの[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")もXfce 4.14に更新された。このバージョンは、新しく改善されたツール、アートワーク、ドキュメンテーション、翻訳、技術的要素によって特徴づけられる。詳細は[MX Blog](https://mxlinux.org/blog/mx-19-patito-feo-released/)を参照。

## 特徴

MX Linuxは、[UEFI](https://ja.wikipedia.org/wiki/UEFI "wikilink")コンピュータで使える[インストーラー](https://ja.wikipedia.org/wiki/インストーラー "wikilink")や、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")を変更する手段、AntiXのコアプログラム群などのような基本的なツールを備えている。しかしMXは、MXツールと呼ばれるユーザー志向のツール群を配布していることによって他のディストリビューションから区別される。これらのツールは、antiXの既に存在するアプリケーションや、antiXのアプリケーションからフォークしたものを含むが、特にMXのために開発されているものである。

一例としては、**MXスナップショット**を挙げることができる。これは、ライブインストールを、単独の.ISOファイルにリマスターする[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")のツールである。この"クローンされた"イメージは、簡単かつ便利に、全ての設定を保ったまま、起動可能なディスクや[USBドライブからの起動を可能にするものである](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")。この方法では、システム管理的な努力なしに、便利にシステムの移行や配布を行うことができる。MXスナップショットはまた、インストールされたシステムの完全で便利な[バックアップ](../Page/バックアップ.md "wikilink")としても使うことができる。

## 評価

### ランキングの推移について

DistroWatch は、オープンソースの OS を紹介しているサイトである。各々の OS のページの閲覧数を掲載しており、近年はランキング上位の位置を占めるようになった。2020年4月6日現在、すでに第1位にある。

### ユーザーの評価

DistroWatch には、Linuxディストリビューション毎にユーザーのレビューが掲載されている。MX Linuxについても[こちらのページ](https://distrowatch.com/dwres.php?resource=ratings&distro=mx)に読者のレビューがある。

## プロジェクトの組織構成

MX 開発チームは、様々な経歴、才能、興味を持ったボランティアのグループで構成されている。以下の各々の担当は、開発チーム内での年次投票で決められている。（以下は2020年4月1日現在）[出典](https://mxlinux.org/about-us/)

### 開発チームについて

リーダーシップ

  - Adrian
  - Dolphi_Oracle
  - Jerry3904

主要チームリーダー

  - チーム代表： anticapitalista
  - アート関係担当： asqwerth
  - ウェブサイト担当： peregrine
  - フォーラム担当： richb
  - パッケージ担当： Stevo

## リリースの種類

MX コミュニティが独自にリリースするリポジトリには、MXメイン版や MXテスト版、MX-ahs版がある。また、MX のシステムには、Debian やサードパーティーがリリースする複数のリポジトリを組み込み、共用することが可能なようにしている。ただし基本的には、ライブラリの依存関係などの問題でシステムの不具合発生を招かないようにするため、Debian安定版だけを利用することが推奨されている。

MX パッケージチームは、ユーザーが新しいグラフィックスタックやファームウェアのようなものをインストールできるように、メインリポジトリの特別なセクションに取り組んできた。これには、更新された mesa パッケージや xorg ドライバなどが含まれている。また、様々なグラフィックアクセラレーション・パッケージや、それらを利用できるアプリケーションのアップデートもある。このリポジトリを MXでは "Advanced Hardware Support" または "ahs" と呼んでいる。\[16\]

  - MXメイン版
  - MXテスト版
  - MX-ahs
  - Debian安定版
  - Debianバックポート
  - マルチメディアリポジトリ
  - Flatpakリポジトリ

## 対応アーキテクチャ

MX では、以下のようなアーキテクチャに対応したバイナリ版を作成している。

  - AMD64 (amd64/x86-64)
  - x86 (i386/IA-32)

## リリース/バージョン履歴

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>正式な公開日</p></th>
<th><p>対応する Debian LTS サポート期限</p></th>
<th><p>ベースとなった Debian GNU/Linux</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>MX-19.2</p></td>
<td><p>2020年06月01日</p></td>
<td><p>2024年（予定）</p></td>
<td><p>Debian 10 (buster)</p></td>
</tr>
<tr class="even">
<td><p>MX-19.1</p></td>
<td><p>2020年02月14日</p></td>
<td><p>2024年（予定）</p></td>
<td><p>Debian 10 (buster)</p></td>
</tr>
<tr class="odd">
<td><p>MX-19</p></td>
<td><p>2019年10月21日</p></td>
<td><p>2024年（予定）</p></td>
<td><p>Debian 10 (buster)</p></td>
</tr>
<tr class="even">
<td><p>MX-18.3</p></td>
<td><p>2019年05月26日</p></td>
<td><p>2022年</p></td>
<td><p>Debian 9 (stretch)</p></td>
</tr>
<tr class="odd">
<td><p>MX-18.2</p></td>
<td><p>2019年04月07日</p></td>
<td><p>2022年</p></td>
<td><p>Debian 9 (stretch)</p></td>
</tr>
<tr class="even">
<td><p>MX-18.1</p></td>
<td><p>2019年2月9日</p></td>
<td><p>2022年</p></td>
<td><p>Debian 9 (stretch)</p></td>
</tr>
<tr class="odd">
<td><p>MX-18</p></td>
<td><p>2018年12月20日</p></td>
<td><p>2022年</p></td>
<td><p>Debian 9 (stretch)</p></td>
</tr>
<tr class="even">
<td><p>MX-17.1</p></td>
<td><p>2018年4月14日</p></td>
<td><p>2022年</p></td>
<td><p>Debian 9 (stretch)</p></td>
</tr>
<tr class="odd">
<td><p>MX-17</p></td>
<td><p>2017年12月15日</p></td>
<td><p>2022年</p></td>
<td><p>Debian 9 (stretch)</p></td>
</tr>
<tr class="even">
<td><p>MX-16.1</p></td>
<td><p>2017年6月8日</p></td>
<td><p>2020年</p></td>
<td><p>Debian 8 (jessie)</p></td>
</tr>
<tr class="odd">
<td><p>MX-16</p></td>
<td><p>2016年12月14日</p></td>
<td><p>2020年</p></td>
<td><p>Debian 8 (jessie)</p></td>
</tr>
<tr class="even">
<td><p>MX-15</p></td>
<td><p>2015年12月24日</p></td>
<td><p>2020年</p></td>
<td><p>Debian 8 (jessie)</p></td>
</tr>
<tr class="odd">
<td><p>MX-14.4</p></td>
<td><p>2015年3月22日</p></td>
<td><p>サポート終了</p></td>
<td><p>Debian 7 (wheezy)</p></td>
</tr>
<tr class="even">
<td><p>MX-14.3</p></td>
<td><p>2014年12月3日</p></td>
<td><p>サポート終了</p></td>
<td><p>Debian 7 (wheezy)</p></td>
</tr>
<tr class="odd">
<td><p>MX-14.2</p></td>
<td><p>2014年6月30日</p></td>
<td><p>サポート終了</p></td>
<td><p>Debian 7 (wheezy)</p></td>
</tr>
<tr class="even">
<td><p>MX-14.1.1</p></td>
<td><p>2014年6月18日</p></td>
<td><p>サポート終了</p></td>
<td><p>Debian 7 (wheezy)</p></td>
</tr>
<tr class="odd">
<td><p>MX-14</p></td>
<td><p>2014年3月24日（PAE）</p>
<p>2014年3月27日（non-PAE）</p></td>
<td><p>サポート終了</p></td>
<td><p>Debian 7 (wheezy)</p></td>
</tr>
</tbody>
</table>

出典：MX Linux.org\[17\]

## 関連項目

  - [antiX](https://ja.wikipedia.org/wiki/antiX "wikilink")
  - [MEPIS](../Page/MEPIS.md "wikilink")
  - [Debian GNU/Linux](https://ja.wikipedia.org/wiki/Debian_GNU/Linux "wikilink")
  - [Xfce](../Page/Xfce.md "wikilink")
  - [ライブCD](https://ja.wikipedia.org/wiki/ライブCD "wikilink")

## 出典

## 外部リンク

  -
  - [MX Linux フォーラム](https://forum.mxlinux.org/)

  - [MX Linux プロジェクト日本語ページ (OSDN)](https://ja.osdn.net/projects/mx-linux/)

  -
[Category:Debian派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Debian派生ディストリビューション "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12. <https://www.techbrackets.com/mx-linux-review/>
13. <https://mxlinux.org>
14. <https://mxlinux.org/about-us/>
15. <https://mxlinux.org/about-us>
16.
17.