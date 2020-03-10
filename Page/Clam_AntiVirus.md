> この記事は[Clam AntiVirus](https://ja.wikipedia.org/wiki/Clam_AntiVirus)から翻訳されています。


**Clam AntiVirus** （クラム・アンチウイルス。略称 **ClamAV**）とは、[オープンソース](../Page/オープンソース.md "wikilink") ([GPL](../Page/GNU_General_Public_License.md "wikilink")) で提供されている[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の[アンチウイルスソフトウェア](https://ja.wikipedia.org/wiki/アンチウイルスソフトウェア "wikilink")である。

Clam AntiVirusの開発プロジェクトでは、[メールゲートウェイ](https://ja.wikipedia.org/wiki/メールゲートウェイ "wikilink")で[電子メール](../Page/電子メール.md "wikilink")のウィルススキャンを行うことを開発目標の主眼としている\[1\]。当初[UNIX](../Page/UNIX.md "wikilink")用として開発され、その後[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")、[BSD](../Page/BSD.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[OpenVMS](https://ja.wikipedia.org/wiki/OpenVMS "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[OSFと](https://ja.wikipedia.org/wiki/Open_Software_Foundation "wikilink")[Solaris](../Page/Solaris.md "wikilink")に移植されている。[Windowsにも](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、現在では「ClamAV for Windows」「ClamWin」「MoonSecureAV」など、多くの派生版が移植されている。

主に[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")におけるサーバサイドにおけるE-mailウイルススキャンの分野で広く利用されている。 従来より常駐監視機能(オンアクセススキャン)が標準実装されていなかったため、常駐監視としては[Dazuko](https://ja.wikipedia.org/wiki/Dazuko "wikilink")+Clamukoを利用したり[crond](https://ja.wikipedia.org/wiki/crond "wikilink")のジョブとしてフルスキャンを実施する方法が一般的だった。

しかし、[2013年](../Page/2013年.md "wikilink")[9月19日](../Page/9月19日.md "wikilink")にリリースされた0.98からは[fanotify](https://ja.wikipedia.org/wiki/fanotify "wikilink")を用いた監視機能が実装されたため、2.6.36以降のLinux等ではDazukoモジュールを用いなくても任意のフォルダの常駐監視が可能となった。

その他、macOS 版の ClamXav では ClamXav Sentry を常駐させる事ができ、任意のフォルダなどを監視させる事が可能である。また、[Mac OS X Server](https://ja.wikipedia.org/wiki/macOS_Server "wikilink") 10.4 Tiger 以降には ClamAV が標準で含まれている。 その他、常駐保護機能を持つものとして「ClamAV for Windows」や「MoonSecureAV」などの派生版がある。

__TOC__

## 機能

ClamAVには次に示すような何種類かのユーティリティが含まれる。コマンドライン版スキャンツール（clamscan）、データベース アップデートツール（freshclam）、マルチスレッドで実行可能なデーモン（clamd）である。また、sendmailのメールフィルタリング拡張コンポーネント機能を持っており、オンデマンドのスキャンを行える。さらに、[ZIPや](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")[tar](https://ja.wikipedia.org/wiki/tar "wikilink")、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")といった圧縮ファイルや、[Microsoft Officeで作成されたファイルや](../Page/Microsoft_Office.md "wikilink")[PDFファイルもスキャンすることが出来る](../Page/Portable_Document_Format.md "wikilink")。

ウイルスデータベースは、最大1日数回アップデートされ、[2011年](../Page/2011年.md "wikilink")[7月20日](../Page/7月20日.md "wikilink")現在では1,000,066 件のウイルスパターンを保有している。\[2\]

## グラフィカルインターフェース（GUI）

### Linux

  - ClamTk[1](http://clamtk.sourceforge.net/) − gtk2-perlアプリケーション。[RHELや](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink")[CentOS](https://ja.wikipedia.org/wiki/CentOS "wikilink")では ClamTk 公式サイトにて最新版のRPMパッケージが公開されている。
  - KlamAV[2](http://klamav.sourceforge.net/klamavwiki/index.php/Main_Page) - RHELやCentOSではソースコードでインストールする必要がある。[Fedora](../Page/Fedora.md "wikilink")ではLivnaリポジトリにrpmパッケージが公開されている場合がある。

### Windows

  - ClamWin[3](http://www.clamwin.com/)

<!-- end list -->

  - 補助ツールである Clam Sentinel をインストールすることで、常駐化が可能。

### macOS

  - ClamXav[4](http://www.clamxav.com/)

## 関連項目

  - [マルウェア](https://ja.wikipedia.org/wiki/マルウェア "wikilink")
  - [コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")
  - [スパイウェア](https://ja.wikipedia.org/wiki/スパイウェア "wikilink")
  - [ルートキット](https://ja.wikipedia.org/wiki/ルートキット "wikilink")
  - [バックドア](https://ja.wikipedia.org/wiki/バックドア "wikilink")
  - [キーロガー](https://ja.wikipedia.org/wiki/キーロガー "wikilink")
  - [トロイの木馬](https://ja.wikipedia.org/wiki/トロイの木馬_\(ソフトウェア\) "wikilink")

## 参考文献

<references/>

[Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.  開発元ホームページ <http://www.clamav.net/> にて確認