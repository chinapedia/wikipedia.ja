> この記事は[PearPC](https://ja.wikipedia.org/wiki/PearPC)から翻訳されています。


**PearPC** は[アーキテクチャ独立な](../Page/コンピュータ・アーキテクチャ.md "wikilink")[PowerPC](../Page/PowerPC.md "wikilink")プラットフォーム[エミュレータ](../Page/エミュレータ.md "wikilink")であり、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Darwin](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")といった各種[PowerPC](../Page/PowerPC.md "wikilink")向け[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) を実行可能である。[GPLでライセンスされている](../Page/GNU_General_Public_License.md "wikilink")。[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")など、[POSIX](../Page/POSIX.md "wikilink")と[X11をベースとしたシステム上で動作可能](../Page/X_Window_System.md "wikilink")。最初の公式リリースは[2004年](../Page/2004年.md "wikilink")[5月10日](../Page/5月10日.md "wikilink")。

このエミュレータは、PowerPCコードを[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")コードに動的に変換する[ジャストインタイム](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink") (JIT) プロセッサエミュレーション・コアを中心とし、変換結果の[キャッシュを備えている](https://ja.wikipedia.org/wiki/キャッシュ_\(コンピュータシステム\) "wikilink")。x86アーキテクチャでしか動作できないが、アーキテクチャ独立な汎用プロセッサエミュレーション・コアよりも30倍以上の性能で動作する。しかし、ネイティブコードとして実行した場合の15倍の時間がかかる\[1\]。

ビルドを行っているPearPCサイトでは、[PowerPC G4プロセッサの](https://ja.wikipedia.org/wiki/PowerPC_G4 "wikilink")[AltiVec](../Page/AltiVec.md "wikilink")サポートを行っている。グラフィックスカードのアクセラレーションのサポートも進行中で、それによってmacOSの[Quartz Extremeの性能が向上することが期待されている](https://ja.wikipedia.org/wiki/Quartz_Extreme "wikilink")。

## 問題点

最新版は2011年7月13日にリリースされたPearPC 0.5.0である。ほとんどのアプリケーションをエミュレータ上で実行できるが、以下のような部分が未実装である。

  - サウンド機能エミュレーション
  - G5エミュレーション
  - .dmgサポート（現在は .dmgイメージを[ISO 9660イメージに変換する必要がある](../Page/ISO_9660.md "wikilink")）

なお、上記の問題点、及びその他の新たな機能など、SorceForge上に存在する最新のソースコードでは対応している。 ただ、前述のようにPearPC 0.5.0を最後に手軽に利用できるバイナリ（実行ファイル）でのリリースは行われていないため、各自でビルドする必要がある。

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[6月6日](../Page/6月6日.md "wikilink")、[アップル](../Page/アップル_\(企業\).md "wikilink")[CEO](https://ja.wikipedia.org/wiki/最高経営責任者 "wikilink")[スティーブ・ジョブズ](../Page/スティーブ・ジョブズ.md "wikilink")は、PowerPCからx86へのアーキテクチャの切り替えを発表した。この切り替えは2006年[8月](../Page/8月.md "wikilink")に完了した。この間、PearPCプロジェクトの今後が大いに話題になった。macOSがネイティブでx86プラットフォームで動作するなら、PearPCは[VMware](https://ja.wikipedia.org/wiki/VMware "wikilink")など他の仮想化製品に置き換え可能と思われるためである。

## フロントエンド

PearPC自体には[GUIがない](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。以前は 'Change CD' ボタンがあったが、正しく動作しないため除去された。しかし、[フロントエンド](../Page/フロントエンド.md "wikilink")もいくつか開発されている。PearGUIはmacOSアプリケーションに似た見た目だが、最新版のPearPCでは動作できない。PearPCCP (PearPC Control Panel) はPearPC 0.3以降で動作する。PearGUIは機能が不完全で、特に 'Create Disk Image' 機能が不完全なのが致命的だが、GUIとしては評判がよかった。PearPCCPは機能が豊富だが、GUIとしては見劣りし、バグも散見される。PearPC.netというサイトでは独自に[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ベースのAPEというフロントエンドをリリースしている。

## CherryOS 騒動

PearPCリリースから5カ月以内に、別のPowerPCエミュレータ[CherryOS](https://ja.wikipedia.org/wiki/CherryOS "wikilink")がPearPCより高機能で高性能であるとして登場した。しかし、その発表から数時間後、多くの専門家からCherryOSはPearPCを再パッケージしただけのものではないのかという疑問が提示された。CherryOSは2005年3月に商用製品として再リリースされた。多くの専門家は、このバージョンもPearPCプロジェクトのコード（一部または全部）を使っていると指摘した。また、[Mac OS Xをx](https://ja.wikipedia.org/wiki/macOS "wikilink")86アーキテクチャで動作させる製品を販売することの合法性も問題とされた。なぜなら、アップルの利用許諾契約書では、OSはアップル製コンピュータ上でのみ動作することを許諾されているためである。その後様々な批判や指摘を受け、CherryOSは販売中止となった。

## 関連項目

  - [SheepShaver](../Page/SheepShaver.md "wikilink")

## 参照

## 外部リンク

  - [PearPC 公式サイト](http://pearpc.sourceforge.net/)
  - [PearPC.Net](http://www.pearpc.net) コミュニティサイト
  - [PearPC Web Forum](http://www.emaculation.com/forum/)
  - [PearPC nightly builds](http://www.richardgoodwin.com/pearpc/)
  - [E-Maculation's PearPC page](http://emaculation.com/pearpc.php)

[Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")

1.  [PearPC - About](http://pearpc.sourceforge.net/about.html)