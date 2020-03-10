> この記事は[INtime](https://ja.wikipedia.org/wiki/INtime)から翻訳されています。


**INtime**（インタイム）とはTenAsys社が開発している[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")（以下RTOS）である。[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")以降の[CPU](../Page/CPU.md "wikilink")を搭載した[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")上で動作し、[Microsoft Windowsと共存して動作する事もできる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")からiRMXの権利を受け継いだRadiSys社によって、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")にiRMXの派生RTOSとして開発された。その後、[2000年](../Page/2000年.md "wikilink")にRadiSys社を退社したエンジニアがTenAsys社を設立。iRMXならびにINtimeに関する権利はTenAsys社に引き継がれ現在に至る。

日本国内を含むアジア地区における販売ならびに開発、技術サポートは株式会社[マイクロネット](https://ja.wikipedia.org/wiki/マイクロネット "wikilink")が行っている。

## 特徴

### Microsoft Windowsとの共存

Microsoft Windowsと共存し、同時に起動して利用することができる。INtime[カーネル](../Page/カーネル.md "wikilink")の起動時に、Windows OSはINtimeのひとつのINtime[プロセス](../Page/プロセス.md "wikilink")として取り込まれる。これによりRTOSとしての特性を損なうことなく、Windows用に提供される豊富な[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")や[アプリケーションを活用したシステム構成が可能になる](../Page/アプリケーションソフトウェア.md "wikilink")。

### ダイナミックローディング

INtime用に開発されたカーネル以外のすべての[モジュール](../Page/モジュール.md "wikilink")は、システムの稼動中、任意の時点で追加、削除、更新が自由に行える。

### メモリ保護

INtime用に開発されたアプリケーションは[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")保護機能により保護される。これにより各INtimeプロセス空間が分離され、メモリ破壊等のエラー時に、その影響を同一プロセス内に限定される。

WindowsもINtimeプロセスとして分離されているため、BSODによりWindowsカーネルが機能停止した場合でも、他のINtimeプロセスは影響を受けずに処理を継続する事が可能になる。

## 外部リンク

  - [TenAsys](http://www.tenasys.com/)
  - [株式会社マイクロネット](http://www.mnc.co.jp/)

[Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink")