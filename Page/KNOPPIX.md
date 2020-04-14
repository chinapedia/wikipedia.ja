> この記事は[KNOPPIX](https://ja.wikipedia.org/wiki/KNOPPIX)から翻訳されています。


**KNOPPIX**（クノーピクス\[1\]、ノピックス）とは、[CD-ROM](../Page/CD-ROM.md "wikilink")または[DVD-ROM](https://ja.wikipedia.org/wiki/DVD-ROM "wikilink")から起動することが可能な[Debian](../Page/Debian.md "wikilink")ベースの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")。

## 概要

[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")のKlaus KnopperがDebianパッケージを元に開発しているものがオリジナルとなる。一枚のCD/DVD/USBメモリなどのリムーバブルメディアから起動できる[Live CDとして利用することを基本としていることが特徴](../Page/Live_CD.md "wikilink")。日本国内では[独立行政法人](../Page/独立行政法人.md "wikilink")[産業技術総合研究所](../Page/産業技術総合研究所.md "wikilink")によって、日本語化をはじめとする日本の国情にあわせたローカライゼーションや、様々な機能を追加したものが本家とは別途開発、配布されていた。

当初はCD版のみの提供だったが、収録希望のアプリケーションの数が増えるに伴いCD-ROMの容量では不足するため、正式な同時リリース決定の前に二度ほどDVDイメージの頒布も行われている。Version 4.0で本家のKlaus KnopperがDVD-ROM版とCD-ROM版をほぼ同時に提供することを決定した。CD-ROM版を"light"（軽量版）、DVD-ROM版を"maxi"（大容量版）と位置付け、DVD版では更に多くのアプリケーションが標準で利用可能となっている。4.0版（DVD版）は[2005年](../Page/2005年.md "wikilink")[6月22日](../Page/6月22日.md "wikilink")にLinuxTagで配布された。Version 7.2でCD-ROM版の提供を終了し、DVD-ROM版に一本化された。

Live CDとしての利用が前提であるため、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")にOSを[インストール](../Page/インストール.md "wikilink")する必要がなく、初期状態ではハードディスクに変更を加えずに[Linux](../Page/Linux.md "wikilink")を稼働させ、さまざまなコマンドやアプリケーションを使うことができる。 これらの特性から、ハードディスクに障害が発生している場合に仮のシステムとして起動させ、ハードディスクの診断や他のメディアなどへのデータをサルベージするなどの作業にも使用可能である。

また、パソコンに接続されたハードウエアを数多くサポートし自動的に認識する能力に優れていることも特徴の1つで、例えばユーザーはビデオ・カードの種類などを指定する必要がなく、直ちにGUIを利用可能となる。ネットワークについても[DHCP環境にあれば](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")、[LANにつながっているだけで自動的に接続設定がおこなう](../Page/Local_Area_Network.md "wikilink")。ネットワークに繋がれば、必要なファイルなどは[http](https://ja.wikipedia.org/wiki/http "wikilink"), [ftp](https://ja.wikipedia.org/wiki/ftp "wikilink")などで保存できるためハードディスクなどがなくても困らない。

基本的に1CD/1DVD[ブータブル](../Page/ブート.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")であるが、[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")などの[アプリケーションソフト](https://ja.wikipedia.org/wiki/アプリケーションソフト "wikilink")が付属している。CD/DVDから起動するため、デフォルトでは書き込み（[データ](../Page/データ.md "wikilink")の変更）を行うことができるユーザのホーム・[ディレクトリ](../Page/ディレクトリ.md "wikilink")などが[RAMディスク](../Page/RAMディスク.md "wikilink")上に置かれており、パソコンの[再起動](../Page/再起動.md "wikilink")や[シャットダウン](../Page/シャットダウン.md "wikilink")で保存したデータは消えてしまう。

しかし、それらを[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")、可搬式の[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")、[USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")などに保存することもできる。そのため国外の旅行先でも、CD-ROMから起動できるパソコンを借りることによって、自国語環境の元で簡単な仕事を行うこともできる。また、日本語版ではInstall2WinというWindowsパソコンにKNOPPIXをインストールして[マルチブート](../Page/マルチブート.md "wikilink")環境を構築することによってハードディスクからKNOPPIXが起動できるようにする機能が搭載されている。ただしこの機能は、下で述べるインストール機能よりインストールされるOSの操作は、LiveCDのOSに近い。だが、下で述べている機能ではKNOPPIXではなく、Debianがインストールされる。

データの書き換えができないCD/DVDに起動に必要な要素がすべて格納されているため、起動中にどのような状態になっても再起動すれば元に戻る、という特徴がある。この特徴を生かし、不特定多数がパソコンを共有する公共の場に置かれる[キオスク端末](https://ja.wikipedia.org/wiki/キオスク端末 "wikilink")や、学校教育などでの使用が考えられている。 そのため、日本語版では[教育ソフト](https://ja.wikipedia.org/wiki/教育ソフト "wikilink")を収録した、KNOPPIX Eduや[KNOPPIX/Mathが開発されている](https://ja.wikipedia.org/wiki/MathLibre "wikilink")。

また、最近OSで流行している[3Dデスクトップ](https://ja.wikipedia.org/wiki/3Dデスクトップ "wikilink")の搭載に対応するため、5.1から、3Dデスクトップ環境[Beryl](../Page/Beryl.md "wikilink")、5.3.1からはその後継の[Compiz Fusionが搭載された](https://ja.wikipedia.org/wiki/Compiz_Fusion "wikilink")。

## KNOPPIXの特徴

CDやDVDから起動できることが、最大の特徴であるKNOPPIXだが、バージョンごとに新たな技術的試みが取り込まれていることも、KNOPPIXの特徴となっている。

### UnionFS / aufs

KNOPPIX3.8.1からは、[UnionFS](https://ja.wikipedia.org/wiki/UnionFS "wikilink")というファイルシステムが採用されており、本来書き込むことができないはずのCD-ROMに対し、仮想的にファイルを書き込むことができるようになった。 これにより、一時的にではあるが、それまで不可能だったパッケージの追加などがおこなえるようになった。

KNOPPIX5.1からは安定性向上のため、unionfsに替わり、[aufs](https://ja.wikipedia.org/wiki/aufs "wikilink")(another unionfs)が採用されている。

### 各種エミュレータの搭載

KNOPPIXには各種エミュレーション用ソフトウエア（[エミュレータ](../Page/エミュレータ.md "wikilink")）が搭載されており、最もエミュレータが利用しやすいOSのひとつとなっている。[QEMU](../Page/QEMU.md "wikilink")はKNOPPIX上、もしくは[Windows上でKNOPPIXを起動でき](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Cooperative LinuxをWindowsにインストールすることで](../Page/Cooperative_Linux.md "wikilink")、Windows上の一ウインドウとしてKNOPPIXが動作する。[Xenと組み合わせた版であるXenoppixでは](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")、KNOPPIX上で[Plan 9や](../Page/Plan_9_from_Bell_Labs.md "wikilink")[NetBSD](../Page/NetBSD.md "wikilink")が利用できる。

### CD/DVD以外からの起動

KNOPPIXはCD/DVDから起動させるのが一般的であるが、多彩な起動方法が選択できることも特徴のひとつで、CD/DVDに格納されたイメージをハードディスクにインストールしてしまい、通常のLinuxディストリビューションの様にハードディスクから起動することも可能である。

KNOPPIX5.1以降には、KNOPPIXをUSBフラッシュメモリから起動させるためのスクリプトmkbootdevが追加されており、1GBのUSBフラッシュメモリを使用すればCD版のすべての機能を利用することができるようになっている。 また、公式対応以前にも、USBフラッシュメモリ起動の試みは、[USB-KNOPPIX](https://ja.wikipedia.org/wiki/USB-KNOPPIX "wikilink")など、各所でおこなわれていた。

そのほか[コンパクトフラッシュ](../Page/コンパクトフラッシュ.md "wikilink")からの起動や、サーバを用意して、ネットワークからのPXEブート、またHTTPポートを使用して必要なイメージをネットワークから取得して起動する方法も選択できるようになっている（HTTP-FUSE-KNOPPIX）。

### 産業技術総合研究所版の独自機能

バージョン6から[LCAT](https://ja.wikipedia.org/wiki/LCAT "wikilink")(Live CD Acceleration Tool kit)と呼ばれる機能が追加された。 これは、[Live CDから起動する際に読み込まれるデータの配置を最適化することによりCDのピックアップの移動を抑えて起動時間を短縮する機能であるが](../Page/Live_CD.md "wikilink")、機能単体のプロジェクトも存在する\[2\]。 産業技術総合研究所による日本語版の開発、並びに頒布は既に終了しており、7.0.2が最終版となっている。プロジェクトの閉鎖に伴い2015年4月に公式サイトは閉鎖された\[3\]。

尚、2015年現在オリジナルのKNOPPIXには日本語のロケールが追加されているため、初期状態はドイツ語版か英語版であることやIME等の積極的なサポートが無いなど、設定を要するものの日本語での利用も可能になっている。

## バージョン

| Knoppixバージョン | リリース日       |
| ------------ | ----------- |
| 3.1          | 2003年1月19日  |
| 3.2          | 2003年7月26日  |
| 3.3          | 2004年2月16日  |
| 3.4          | 2004年5月17日  |
| 3.6          | 2004年8月16日  |
| 3.7          | 2004年12月9日  |
| 3.8.2        | 2005年5月12日  |
| 3.9          | 2005年6月1日   |
| 4.0          | 2005年6月22日  |
| 4.0 updated  | 2005年8月16日  |
| 4.0.2        | 2005年9月23日  |
| 5.0          | 2006年2月25日  |
| 5.0.1        | 2006年6月2日   |
| 5.1.0        | 2006年12月30日 |
| 5.1.1        | 2007年1月4日   |
| 5.3.1        | 2008年3月26日  |
| 6.0          | 2009年1月27日  |
| 6.0.1        | 2009年2月8日   |
| 6.2          | 2009年11月18日 |
| 6.4.3        | 2010年12月20日 |
| 6.4.4        | 2011年2月1日   |
| 6.7.1        | 2011年9月21日  |
| 7.0.1        | 2012年6月15日  |
| 7.0.4        | 2012年10月27日 |
| 7.0.5        | 2012年12月21日 |
| 7.2.0        | 2013年6月26日  |
| 7.3.0        | 2014年3月14日  |
| 7.4.0        | 2014年8月6日   |
| 7.4.1        | 2014年9月14日  |
| 7.4.2        | 2014年9月30日  |
| 7.6.0        | 2015年11月21日 |
| 7.6.1        | 2016年1月16日  |
| 8.1.0        | 2017年9月5日   |
| 8.2.0        | 2018年5月10日  |
| 8.5.0        | 2019年2月10日  |
| 8.6.0        | 2019年8月17日  |
| 8.6.1        | 2019年11月23日 |
|              |             |

## 脚注

## 関連項目

  - [1CD Linux](https://ja.wikipedia.org/wiki/1CD_Linux "wikilink")
  - [Puppy Linux](../Page/Puppy_Linux.md "wikilink")
  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [Linuxライブディストリビューションの比較](../Page/Linuxライブディストリビューションの比較.md "wikilink")

## 外部リンク

  -
  -

[Category:Debian派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Debian派生ディストリビューション "wikilink") [Category:LiveCD](https://ja.wikipedia.org/wiki/Category:LiveCD "wikilink")

1.  日本語版を配布していた産業技術総合研究所による表記。
2.  [LCAT(Live CD Acceleration Tool kit)](https://osdn.jp/projects/lcat/)
3.  [KNOPPIX 日本語版](http://www.risec.aist.go.jp/project/knoppix/)