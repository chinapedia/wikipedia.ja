> この記事は[MX Linux](https://ja.wikipedia.org/wiki/MX_Linux)から翻訳されています。


**MX Linux**は、中量級の[Linux](../Page/Linux.md "wikilink")[OS](../Page/OS.md "wikilink")で、[Debian](../Page/Debian.md "wikilink")安定版がベースになっている。また、MXコミュニティによって作られ\[1\]\[2\]\[3\]\[4\]\[5\]\[6\]\[7\]\[8\]\[9\]\[10\]\[11\]、パッケージングされた追加の[ソフトウェア](../Page/ソフトウェア.md "wikilink")と共に、[antiX](https://ja.wikipedia.org/wiki/antiX "wikilink")のコンポーネントを用いている。MXは、antiXと以前の[MEPIS](../Page/MEPIS.md "wikilink")コミュニティの間の協力的事業として開発されており、それぞれの[ディストリビューション](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")からベストなツールと特色を用いることを狙っている。コミュニティは、プロジェクトのゴールについて”洗練されて効果的な[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")を簡単な設定と高い安定性\[12\]、強固なパフォーマンスに結びつける"\[13\]ことだと述べている。MX Linuxは、[Xfce](../Page/Xfce.md "wikilink")を用いており、[KDE Plasmaや他の環境も後から加えることができると共に](../Page/KDE.md "wikilink")、"スピンオフ"[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")としても入手できる。

## 歴史

MX Linuxは、[2013年](../Page/2013年.md "wikilink")の12月に、MEPISコミュニティのメンバーの間で行われた将来のオプションに関する議論の中で始まった\[14\]。これにantiXの開発者たちが加わり、ISOビルドシステムに加え、Live USB/DVDの技術を持ち込んだ。[DistroWatch](https://ja.wikipedia.org/wiki/DistroWatch "wikilink")に掲載されるために、MX Linuxは最初antiXのバージョンであると提示された。MXは、その[独自のDitroWatchのページ](https://distrowatch.com/table.php?distribution=mx)をMX-16の最初のパブリックベータのリリース（[2016年](../Page/2016年.md "wikilink")[11月2日](../Page/11月2日.md "wikilink")）に受け取った。

MX-14シリーズは、Debian安定板"Wheezy"に基づいており、最初はXfce 4.10、その後14.4のリリースに併せてXfce 4.12を用いた。MX-14のバージョンは、CDにフィットするように意図されて構築されており、限られた[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")のみがふくまれるという制限があった。このシリーズでは、しばしば複雑で不透明なものとなる一般的なタスクを行うユーザーを助けることを意図してデザインされた、手軽な[ユーティリティ](https://ja.wikipedia.org/wiki/ユーティリティ "wikilink")のコレクション、MX Toolsの漸進的な進化を見て取ることができる。

MX-15は、Debian安定版"Jessie"にベースを移し、systemd-shimを使うものとなった。これは、[systemd](https://ja.wikipedia.org/wiki/systemd "wikilink")をインストールするものの、デフォルトの[init](https://ja.wikipedia.org/wiki/init "wikilink")は[sysvinitであることを意味する](https://ja.wikipedia.org/wiki/init "wikilink")\[15\]。サイズの制限は上がり、ユーザーにフルターンキーの製品を示すことを開発者に可能にした。また、本質的なMX Toolsの拡張が行われた。

MX-16は依然として、Debian安定版"Jessie"に基くものの、アプリケーションは、他のソースからのものも含め、多くがバックポートされ、また加えられた。また、MX toolsへの追加や改善が行われた。これには、antiXの開発成果の受け入れや、拡張されたサポート、完全に新しいアイコン、テーマ、壁紙の組み合わせが含まれる。

MX-16.1は、MX16以降のバグ修正と改善が含まれる。また、同リリースには、新しいキングフィッシャーテーマの追加や、更新されたMX Tools、改善されたドキュメンテーションや、新しい翻訳の成果が含まれる。

MX-17は、そのベースをDebian 9（Stretch）に変更し、アップグレードされたアートワークや、新しいMX Tools、antiXを通じて進歩したLiveオペレーションなど、[MX Blog](https://mxlinux.org/blog/mx-17-released-december-15-2017)に詳細が書かれた変更が含まれる。

MX-18では、MX Toolsの開発が進められ、最新の[カーネル](../Page/カーネル.md "wikilink")の導入、ディスク全体の[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")、MX Boot optionsを通じて機能する[GRUB](https://ja.wikipedia.org/wiki/GRUB "wikilink")のテーマやスプラッシュ画面が追加された。また、新しいアートワークや改善された翻訳も含まれている。詳細は[MX Blog](https://mxlinux.org/blog/mx-18-continuum-now-available)に記載されている。

MX-19は、そのベースをDebian 10（Buster）にアップグレードし、デフォルトの[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")もXfce 4.14に更新された。このバージョンは、新しく改善されたツール、アートワーク、ドキュメンテーション、翻訳、技術的要素によって特徴づけられる。詳細は[MX Blog](https://mxlinux.org/blog/mx-19-patito-feo-released/)を参照。

## 機能

MX Linuxは、[UEFI](https://ja.wikipedia.org/wiki/UEFI "wikilink")コンピュータで使える[インストーラー](https://ja.wikipedia.org/wiki/インストーラー "wikilink")や、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")を変更する手段、AntiXのコアプログラム群などのような基本的なツールを備えている。しかしMXは、MX Toolsと呼ばれるユーザー志向のツール群を配布していることによって他のディストリビューションから区別される。これらのツールは、antiXの既に存在するアプリケーションや、antiXのアプリケーションからフォークしたものを含むが、MXのために開発されているものである。

例としては、**MX-snapshot**を挙げることができる。これは、Liveインストールを、単独の.ISOファイルにリマスターする[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")のツールである。これは、簡単かつ便利に、全ての設定を保ったまま、起動可能なディスクや[USBドライブから](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")"クローンされた"イメージを起動可能にするものである。この方法では、システム管理的な努力なしに、便利にシステムの移行や配布を行うことができる。snapshotはまた、インストールされたシステムの完全で便利な[バックアップ](../Page/バックアップ.md "wikilink")としても使うことができる。

## 関連項目

  - [antiX](https://ja.wikipedia.org/wiki/antiX "wikilink")
  - [MEPIS](../Page/MEPIS.md "wikilink")

## 出典

## 外部リンク

  -
  -
[Category:Debian派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Debian派生ディストリビューション "wikilink") [Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink")

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