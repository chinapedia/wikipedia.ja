> この記事は[IRMX](https://ja.wikipedia.org/wiki/IRMX)から翻訳されています。


RadiSys{{・}}TenAsys | family = | source_model = | released = | latest_release_version = | latest_release_date= | latest_test_version= | latest_test_date = | frequently_updated = | marketing_target = | language = | kernel_type= | userland = | ui = | license= [プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink") | working_state= | supported_platforms= | updatemodel= | package_manager= }} ''' iRMX '''とはTenAsys社が開発している[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")（以下RTOS）である。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[8080](../Page/Intel_8080.md "wikilink")、[8086系マイクロプロセッサ上で動作する](../Page/Intel_8086.md "wikilink")。iRMXはIntel Real-time Multitasking eXecutiveを意味する頭字語である。[米国インテルが](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[1970年代](../Page/1970年代.md "wikilink")後半から自社製の8080、8086系プロセッサおよび[MULTIBUS](https://ja.wikipedia.org/wiki/MULTIBUS "wikilink")システム用に開発し、[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")にリリースした。著作権および開発ライセンスは[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に米国RadiSys社に引き継がれ、さらに[2000年](../Page/2000年.md "wikilink")にはRadiSys社からTenAsys社に引き継がれた。

iRMXの技術は1997年以降、[Microsoft Windowsと共存動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[INtime](https://ja.wikipedia.org/wiki/INtime "wikilink")に移行されているが、旧バージョンのiRMXシステムの後継用RTOSとして現在もiRMX IIIおよびiRMX for Windows (iRFW) が販売・サポートされている。

iRMX for Windowsは[INtime](https://ja.wikipedia.org/wiki/INtime "wikilink")と比較して、C-386、PLM-386、FORTRAN-386、ASM-386など従来世代の開発言語に対応すること、独自のファイルドライバ（ディスクI/O）を持っていること、メモリアクセス方法が、近年の32ビットのフラットアドレッシングのほか旧世代[CPU](../Page/CPU.md "wikilink")で多用された16ビットのセグメントアドレッシング機能も有すること、などである。これによって、古いiRMXを利用したアプリケーションを新しい[PCハードウェアに移行することができる](../Page/パーソナルコンピュータ.md "wikilink")。 日本国内における販売は株式会社[株式会社マイクロネット](http://www.mnc.co.jp/)が行っている。

## 製品史

### iRMX

[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")以降、8080、8086、[80286を対象にiRMX](../Page/Intel_80286.md "wikilink") -80、-86、-286がそれぞれリリースされてきたが、[80386以降のプロセッサ用にはiRMX](../Page/Intel_80386.md "wikilink") I、II、IIIの名称で順次リリースされた。iRMX -80以降これらのiRMXは[スタンドアロンシステム用のROTSとして用いられた](https://ja.wikipedia.org/wiki/スタンドアローン "wikilink")。現在サポートされているのはiRMX IIIである。

### dosRMX、dosRMX-98、win RMX-98、net RMX

これらのRMXは、一つのプロセッサにiRMXと[MS-DOS](../Page/MS-DOS.md "wikilink") (DOS) またはMicrosoft Windows (Windows) とを搭載し、リアルタイムサービスとDOS（またはWindows）のサービスとを同時に実行させるためのRTOSである。 DOSまたはWindowsはRMXの支配下に入りRMXのプロセスの一つとして実行されるためリアルタイム処理が遅れることはない。 dosRMXは[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")用、dosRMX-98は[日本電気](../Page/日本電気.md "wikilink")が発売したPCアーキテクチャである[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用で、いずれもMS-DOSバージョン6以前に対応する。 win RMX-98 、net RMXは[Windows 3.0に対応するRTOSであり](../Page/Microsoft_Windows_3.x.md "wikilink")、win RMX-98はPC-9800シリーズ用、net RMXはPC/AT互換機用である。

### iRMX for Windows（iRFWともいう）

[Windows NT系の](https://ja.wikipedia.org/wiki/Windows_NT系 "wikilink")32ビットアーキテクチャWindowsに対応するRTOSである。現在販売・サポートされているiRMX for WindowsはiRMX IIIをベースにしている。 [Windows 9x系には対応していない](https://ja.wikipedia.org/wiki/Windows_9x系 "wikilink")。

## 外部リンク

  - [TenAsys](http://www.tenasys.com/)
  - [株式会社マイクロネット](http://www.mnc.co.jp/)
  - 株式会社マイクロネット－[INtime/iRFWの歴史](http://www.mnc.co.jp/INtime/INtime_rekishi.html/)

[Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink")