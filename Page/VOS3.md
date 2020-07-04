> この記事は[VOS3](https://ja.wikipedia.org/wiki/VOS3)から翻訳されています。


**VOS3**（ボス・スリー、ボス・サン、Virtual-storage Operating System 3）は、[日立製作所](../Page/日立製作所.md "wikilink")が製造・販売している[メインフレーム](../Page/メインフレーム.md "wikilink")用[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のこと。

## 歴史

### 通産省共同研究

[1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")4月に決定された[OECDの](../Page/経済協力開発機構.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")の貿易自由化方針への対応策として、当時の[通商産業省は](../Page/経済産業省.md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink")メーカー6社のグループ化を行い、[1972年](../Page/1972年.md "wikilink")から[1976年](../Page/1976年.md "wikilink")の3グループによるそれぞれの技術研究組合による共同研究に計600億円近くの補助金を拠出した。[日立製作所](../Page/日立製作所.md "wikilink")及び[富士通](../Page/富士通.md "wikilink")は[IBM互換機](https://ja.wikipedia.org/wiki/IBM互換機 "wikilink")である[Mシリーズ](https://ja.wikipedia.org/wiki/Mシリーズ "wikilink")を共同開発した。（⇒[三大コンピューターグループ](../Page/三大コンピューターグループ.md "wikilink")）

VOS3は大型[メインフレーム](../Page/メインフレーム.md "wikilink")[Mシリーズ向けに開発された](https://ja.wikipedia.org/wiki/HITAC#HITAC_Mシリーズ "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。

### VOS3の機能

[基本プログラムとしてのVOS](../Page/システムソフトウェア.md "wikilink")3の機能は

  - 多重[仮想記憶](../Page/仮想記憶.md "wikilink")
  - [マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")サポート
  - 資源集中管理機能
  - [リモート](../Page/リモート.md "wikilink")[バッチ機能](../Page/バッチ処理.md "wikilink")
  - [オンライン](../Page/オンライン.md "wikilink")リアルタイム制御機能
  - [RASIS](../Page/RASIS.md "wikilink")機能
  - [TSS機能](../Page/タイムシェアリングシステム.md "wikilink")

である。当初、先行のOS、VOS2からの移行をスムーズにできるように、VOS2、VOS3で[システムソフトウェア](../Page/システムソフトウェア.md "wikilink")類等も共通化されていた。

最初のVOS3は[1977年](../Page/1977年.md "wikilink")4月（[昭和](../Page/昭和.md "wikilink")52年4月） [日立製作所](../Page/日立製作所.md "wikilink")中央研究所にM-180システムとともに納入された。

## VOS3の機能拡張プロダクト

VOS3の機能拡張プロダクト群と主な特徴を以下に挙げる。

### VOS3/SP21

VOS3/SP21(VOS3/System Product 21)はVOS3/SP(VOS3/System Product)系の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を[IBM産業スパイ事件](../Page/IBM産業スパイ事件.md "wikilink")後に新たに[コーディング](https://ja.wikipedia.org/wiki/コーディング "wikilink")し直したものである。

新たにM-240H、M-260H、M-280Hをサポートする。拡張機能は以下の通り。

  - 大容量[ディスクサポート](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")(H-8598)・資源集中管理機能エンハンス
  - [チャネル](https://ja.wikipedia.org/wiki/チャネル "wikilink")拡張・[コンソール](../Page/コンソール.md "wikilink")機能エンハンス
  - 実記憶拡張(32MB)・スケジューラ拡張・JSS3、JSS4エンハンス

### VOS3/ES1

VOS3/ES1(VOS3/Extend System product 1)は[IBM](../Page/IBM.md "wikilink") [MVS](../Page/Multiple_Virtual_Storage.md "wikilink")/XAに対抗しM/EXモードで動作し、31ビットアドレッシングおよび拡張チャネルシステム(ECS)をサポートしたもの。[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")（[昭和](../Page/昭和.md "wikilink")60年）3月出荷。

新たにM-68X、M-660H、M-640シリーズをサポートする。拡張機能は以下の通り。

  - 31ビットアドレッシングサポート

ECSは[1986年](../Page/1986年.md "wikilink")（[昭和](../Page/昭和.md "wikilink")60年）1月出荷のバージョンからサポートされた。

  - VOS3/ES1 ECSサポート

### VOS3/AS

VOS3/AS(VOS3/Advanced System product)はIBM MVS/ESAに対抗しM/ASAモードで動作し、仮想拡張記憶機構を使用し47ビットアドレッシング（16テラバイト）をサポートした。

新たにM-880、M-860シリーズをサポートする。拡張記憶は以下の通り

  - ACONARCチャネルサポート
  - PRMA(Processor Resource Management Assist) プロセッサ資源分割管理機構支援

### VOS3/FS

VOS3/FS(VOS3/Forefront System Product)は、MP5800、MP5600、[MP6000](https://ja.wikipedia.org/wiki/MP6000 "wikilink")シリーズをサポートしたもの。

### VOS3/LS

VOS3/LS(VOS3/Leading System Product)は[IBM](../Page/IBM.md "wikilink") [z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")連携システム。64ビットアドレッシングをサポートする。 新たに[AP8000](https://ja.wikipedia.org/wiki/AP8000 "wikilink")シリーズをサポートする。2002年4月出荷開始。

  - 64ビットアドレッシングサポート

### VOS3/US

VOS3/US(Virtual-storage Operating System 3/Unific System Product)システムはVOS3/LSの後継となるOSである。2008年2月に発表され、2008年7月に出荷開始。 新しいハードウェアとしてAP8800シリーズに対応した。 [BladeSymphony](https://ja.wikipedia.org/wiki/BladeSymphony "wikilink")との連携に必要な製品が今までは別売製品として出されていたのが「VOS3/US標準パッケージ」として提供されている。

## 外部リンク

  - [VOS3ホームページ](http://www.hitachi.co.jp/Prod/comp/soft1/VOS3/index.html)

[Category:メインフレームのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:メインフレームのオペレーティングシステム "wikilink")