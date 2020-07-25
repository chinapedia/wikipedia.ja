> この記事は[BREW](https://ja.wikipedia.org/wiki/BREW)から翻訳されています。


**BREW**（ブリューまたはブリュウ、ブルー、*Binary Runtime Environment for Wireless*）はQualcomm [REX OS上で動く](https://ja.wikipedia.org/wiki/REX_OS "wikilink")[CDMA](https://ja.wikipedia.org/wiki/Code_Division_Multiple_Access "wikilink")[携帯電話](../Page/携帯電話.md "wikilink")向け[アプリケーションの](../Page/アプリケーションソフトウェア.md "wikilink")[プラットフォームである](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。[cdmaOne](https://ja.wikipedia.org/wiki/cdmaOne "wikilink")、[CDMA2000](../Page/CDMA2000.md "wikilink")の開発元である[クアルコム](../Page/クアルコム.md "wikilink")が開発したもので、同社の[登録商標となっている](../Page/商標.md "wikilink")。ネーミングに関しては[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の「[コーヒー](https://ja.wikipedia.org/wiki/コーヒー "wikilink")」に対して「[ビール](../Page/ビール.md "wikilink")」の意味も込められている。

## BREWの特徴

BREWとはクアルコムが製造販売している携帯電話用プラットフォームMSMチップセット用に構築・拡張されたアプリケーション実行環境である。コンパイルはクアルコム提供のSDK、[Microsoft Visual C++にアドインしたRVCT](../Page/Microsoft_Visual_C++.md "wikilink")（ARMコンパイラ）、もしくは[gccによって行える](../Page/GNUコンパイラコレクション.md "wikilink")。なお、gcc は公式にはサポート外である。

日本では、[2016年](../Page/2016年.md "wikilink")[8月](../Page/8月.md "wikilink")現在、[KDDI](../Page/KDDI.md "wikilink")・[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")のスマートフォンと[シャープ](../Page/シャープ.md "wikilink")製の[AQUOS Kシリーズ](https://ja.wikipedia.org/wiki/AQUOS "wikilink")（[SHF31](https://ja.wikipedia.org/wiki/SHF31 "wikilink")、[SHF32](https://ja.wikipedia.org/wiki/SHF32 "wikilink")等）、[京セラ](../Page/京セラ.md "wikilink")製のGRATINA 4Gシリーズ（[KYF31](https://ja.wikipedia.org/wiki/KYF31 "wikilink")等）、同じく京セラ製のかんたんケータイシリーズ（[KYF32](https://ja.wikipedia.org/wiki/KYF32 "wikilink")等。旧称・[簡単ケータイ](../Page/簡単ケータイ.md "wikilink")シリーズ）を含む一部のフィーチャーフォンを除く各[au携帯電話のほとんどの機種がEZアプリ](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")（BREW）を使用している。2016年9月現在、スマートフォン、およびAQUOS Kシリーズ、GRATINA 4Gシリーズ、かんたんケータイシリーズ、[mamorino Watch](https://ja.wikipedia.org/wiki/mamorino_Watch "wikilink")（ZTF31）以外で使用できない機種には、[W11H](../Page/W11H.md "wikilink")、[W11K](../Page/W11K.md "wikilink")、[W21H](../Page/W21H.md "wikilink")、[A101K](../Page/簡単ケータイS.md "wikilink")（簡単ケータイS）、[A1405PT](../Page/A1405PT.md "wikilink")、[A1406PT](https://ja.wikipedia.org/wiki/A1406PT "wikilink")、[A1407PT](https://ja.wikipedia.org/wiki/A1407PT "wikilink")、[mamorinoシリーズ](https://ja.wikipedia.org/wiki/mamorinoシリーズ "wikilink")（[KYY01](https://ja.wikipedia.org/wiki/KYY01 "wikilink")、[KYY02](https://ja.wikipedia.org/wiki/KYY02 "wikilink")、[KYY05](https://ja.wikipedia.org/wiki/KYY05 "wikilink")）全機種、[PT001](https://ja.wikipedia.org/wiki/PT001 "wikilink")（簡単ケータイS）、[Mi-Look](https://ja.wikipedia.org/wiki/Mi-Look "wikilink")（[KYY03](https://ja.wikipedia.org/wiki/KYY03 "wikilink")）等がある。

以下の特徴を持つ。

1.  [C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")でコンパイルされたバイナリ（アプリケーション）を実行する。
2.  アプリケーションをダウンロードし、実行できる。
3.  APIの実装形式にCOMを利用しており、拡張が容易である。
4.  Extensionという機構を利用し、外部ライブラリを利用できる。
5.  メモリ保護機能が無い 。

携帯電話による実機での動作テストはBREW ApploaderとよばれるツールでBREWアプリと認証（sigファイル）を転送ケーブルにより携帯電話に転送する。また転送先の携帯電話を転送モードに設定する必要がある。クアルコムにデベロッパー登録を行う事によってこれらのツールを入手出来る。

BREWのExtensionとはダウンローダブルなライブラリのことである。実態としてBREWでは全てのAPIがExtension形式で実装されている。Extensionの実装者はその利用を可能とするため、「特権」を要求する事が出来る。たとえばINetMgrというAPIを利用する為には、利用する側のアプリケーションが「PL_NETWORK」という特権を保持している必要がある。この仕組みによってBREWのアプリケーションは利用可能なExtension（=API）を外部へ示す必要があるため、アプリケーションのサーバへの登録に対して審査を行う事が可能となっている。

## KDDI（EZアプリ）での運用

BREWは携帯電話会社や携帯電話製造会社にて様々なカスタマイズを施され運用がなされている。KDDIでもカスタマイズされており、運用上の特徴は以下の通りである。

BREW Apploaderの利用、sigファイルの生成、転送モード設定は現在KDDI公式コンテンツプロバイダのみ行うことができる。いわゆる「野良アプリ」「勝手アプリ」と呼ばれる一般ユーザーが作ったアプリの配布および実行は、PC上のエミュレータ上で動かせるまでであり、携帯電話への配布や実行はできない。また、公式コンテンツプロバイダであっても検証合格前のBREWアプリをネットワーク経由で携帯端末にダウンロードすることはできない。そのため、[オープンアプリプレイヤー](../Page/オープンアプリプレイヤー.md "wikilink")がリリースされるまでは、一般ユーザーは[Flash Liteによるコンテンツ作成をする必要があった](https://ja.wikipedia.org/wiki/Flash_Lite "wikilink")。

なお、[WIN対応機以降は](../Page/CDMA_1X_WIN.md "wikilink")、EZアプリ（BREW・[Javaとも](../Page/EZアプリ_\(Java\).md "wikilink")）は1アプリケーション当たりで通信できるデータ量が1つのアプリにつき3MBまでという自主規制が、公式コンテンツプロバイダに課されている。また、EZアプリ全体では、携帯電話側で1日6MBの通信制限がある。しかし、初期の頃はこれを知らずに順守しなかったコンテンツプロバイダが存在し、定額制課金に加入していないユーザーが知らぬ間に大量のパケットを消費し、**[多額のパケット料金を請求される](../Page/パケ死.md "wikilink")**などの問題も存在した。

もともとのBREWの仕様としてはそのような制限はなく、KDDIの仕様に基づいたEZアプリ（BREW）が通常利用するネットワーク（BREW.NET）の仕様制限である。従って別の通信を利用するBREWアプリケーション、たとえば[KCP](../Page/KCP.md "wikilink")や[KCP+](../Page/KCP+.md "wikilink")でBREWアプリケーション化されたEZブラウザやEメールソフトウェアはこのような制限を受けない。

2010年の一部機種では通信制限を撤廃されている機種もある。

2011年春モデルより[EZアプリ（J）の登場により](../Page/EZアプリ_\(Java\).md "wikilink")**EZアプリ（B）**に名称変更となった。

KDDIは[2016年](../Page/2016年.md "wikilink")[4月28日](../Page/4月28日.md "wikilink")、対応する[3G対応au携帯電話の利用者が減少している](../Page/CDMA_1X_WIN.md "wikilink")（2013年比で約40％減少）ことから、EZアプリ（B）を提供するために必要なクアルコムとのライセンス契約が終了する[2018年](../Page/2018年.md "wikilink")[3月31日](../Page/3月31日.md "wikilink")を以って、EZアプリ（B）の配信サービスとKDDIが提供する一部アプリのサービスを終了することを発表した\[1\]\[2\]。配信サービス終了後も、端末上にあるアプリ（プリインストールならびにダウンロード済）は引き続き実行可能だが、アプリを削除したり端末のリセット（初期化）を行うとプリインストールアプリ以外のアプリは再入手できなくなる。また配信サービス終了によりバージョンアップもできなくなるため、2018年4月以降に仕様変更などが発生した場合、そのアプリは（プリインストールアプリも含め）事実上使用できなくなる。

## KDDI以外の日本の携帯電話会社での利用

[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")も2005年8月5日発売の[SA700iS](../Page/SA700iS.md "wikilink")で導入された。ただしこれは、ユーザがBREWアプリをダウンロードできるものでも、ドコモとしてBREWを導入するものでもなく、ブラウザやJava VM（[iアプリ](https://ja.wikipedia.org/wiki/iアプリ "wikilink")）、GPSナビゲーションアプリを動作させる基本[プラットフォーム的な環境として導入したものである](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。au向けが主体だった[三洋電機](../Page/三洋電機.md "wikilink")（大阪、のちの[京セラ](../Page/京セラ.md "wikilink")SANYOブランド）がドコモに参入 するにあたって、au端末向けの開発ノウハウを流用する目的もあったと推測される。

## バージョンについて

下記の機能は、一般的なBREWの仕様に関する記述であり、必ずしも各キャリアやメーカが全ての機能を実装している訳ではない。

  - BREW 1.0
    KDDIおよび[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")のau携帯電話に採用。初採用された機種は[パナソニック モバイルコミュニケーションズ製の端末C](../Page/パナソニック_モバイルコミュニケーションズ.md "wikilink")3003P。ただしダウンロードして実行する機能は搭載されておらず、純粋に携帯電話内部用のアプリケーション作成に利用された。

  - BREW 2.0/2.1
    BREW Extensionのダウンロードという機能が追加された。ネットワークを通して必要なプログラムが自動的にダウンロードされる機能である。[マスコットカプセルエンジン等が該当する](../Page/MascotCapsule.md "wikilink")。このExtensionにより3D描画が可能となる。

    その他主にマルチメディア系APIの充実が図られた。

  - BREW 3.0
    外部メモリからサウンドや写真などのファイルにアクセス可能になり、[シリアルポート](../Page/シリアルポート.md "wikilink")または[USBを使って](../Page/ユニバーサル・シリアル・バス.md "wikilink")[パソコンにアクセスする機能が付加された](../Page/パーソナルコンピュータ.md "wikilink")。BREW3.0は世界中で利用されず、Qualcommのヒストリからは削除された。現在はSDKのダウンロードも出来なくなった。

  - BREW 3.1
    BREW 3.0を基本に[マルチメディア](../Page/マルチメディア.md "wikilink")コンテンツのアクセス機能や[バリュー課金](https://ja.wikipedia.org/wiki/バリュー課金 "wikilink")と呼ばれるコンテンツ購入機能などが追加された。IAPPHISTORY、IAPPLETCTL等のプラットフォーム向けのAPIが追加された。

  - BREW 4.0
    KDDIおよび沖縄セルラー電話のau携帯電話に世界で初めて採用された。採用機種はau携帯電話向け最新プラットフォーム「KCP+」(KCP2.x)対応端末全機種。[マルチウィンドウ](https://ja.wikipedia.org/wiki/マルチウィンドウ "wikilink")対応。au携帯電話には「マルチプレイウィンドウ」として実装され、この機能はのちに「**クイックアクセスメニュー**」に発展する。

  - BREW 5.0

<!-- end list -->

  -
    [KCP3.x](https://ja.wikipedia.org/wiki/KCP3.x "wikilink")、およびその元となった[Brew MPに採用されている](https://ja.wikipedia.org/wiki/Brew_MP "wikilink")。2016年9月現在、国内市場向け端末ではau携帯電話の[PT003](https://ja.wikipedia.org/wiki/PT003 "wikilink")のみに搭載。

## KDDIが提供していたアプリ（EZアプリ）

  - [EZテレビ](../Page/EZテレビ.md "wikilink")
  - GPSMAP
  - [EZ-FM](https://ja.wikipedia.org/wiki/EZ-FM "wikilink")
  - [EZナビウォーク](../Page/EZナビウォーク.md "wikilink") - 「3Dナビ」対応版を含む。
  - [EZ助手席ナビ](../Page/EZ助手席ナビ.md "wikilink")
  - 安心ナビ
  - 聴かせて検索
  - [EZ Game Street\!](../Page/EZ_Game_Street!.md "wikilink") - 2010年現在提供終了。
  - Full Game\! - 既存のEZアプリ (BREW) の大容量版にあたるアプリで**BREW4.0**がベースとなっている。「[KCP+](../Page/KCP+.md "wikilink")」（KCP2.x）以降のプラットフォームに対応した機種がこのアプリに対応する。
  - live earth
  - EZ Quick

## 関連するソフトウェア

  - [SophiaFramework：BREW向けC++クラスライブラリ](http://www.s-cradle.com/products/sophiaframework/index.html) - BREWアプリケーションをC++プログラミング言語で開発するためのC++クラスライブラリ
  - [SophiaCompress(BREW)：BREWアプリ圧縮ツール](http://www.s-cradle.com/products/sophiacompress_brew/index.html) - BREWアプリケーションのサイズを実行形式のまま圧縮するBREWアプリ圧縮ツール
  - [BREW対応RealViewコード生成ツール（RVCT for BREW)](http://www.sophia-systems.co.jp/arm/rvds/rvct_brew.html) - BREW対応のARM搭載プラットフォーム上で動作するアプリケーションの開発ツール

## 脚注・出典

## 関連項目

  - [KCP](../Page/KCP.md "wikilink")
  - [KCP+](../Page/KCP+.md "wikilink")
  - [Brew Mobile Platform（Brew MP）](https://ja.wikipedia.org/wiki/Brew_Mobile_Platform "wikilink")
  - [EZアプリ (Java)](../Page/EZアプリ_\(Java\).md "wikilink")
  - [オープンアプリプレイヤー](../Page/オープンアプリプレイヤー.md "wikilink")

## 外部リンク

  - [BREW JAPAN(Qualcomm公式総合情報サイト)](http://www.brewjapan.com/)
  - [Qualcomm BREWホーム(Qualcomm公式開発者向け情報サイト)](http://www.qualcomm.com/brew/jp/)
  - [EZ factory内 BREW技術情報(KDDI)](http://www.au.kddi.com/ezfactory/tec/spec/brew.html)
  - [BREWとは(SophiaCradle)](http://www.s-cradle.com/developer/brew/20050328_01.html)
  - [BREW FAQ情報(SophiaCradle)](http://www.s-cradle.com/developer/brew/tqbr/index.html)
  - [BREWプログラミング入門(SophiaCradle)](http://www.s-cradle.com/developer/itmedia/ITmedia_Mobile_BREW_Programming.html)
  - [RVCT for BREW(正規販売代理店ソフィアシステムズ）](http://www.sophia-systems.co.jp/arm/rvds/rvct_brew.html)

[Category:携帯電話アプリ](https://ja.wikipedia.org/wiki/Category:携帯電話アプリ "wikilink") [Category:組み込みOSの製品](https://ja.wikipedia.org/wiki/Category:組み込みOSの製品 "wikilink")

1.  [KDDI、「EZアプリ」と3G端末の国際ローミングを2018年3月に終了](http://www.itmedia.co.jp/mobile/articles/1604/28/news109.html) - [ITmedia](../Page/ITmedia.md "wikilink") 2016年4月28日。
2.  [3G ケータイ向けアプリサービス「EZアプリ」の配信、および一部サービスの終了について](http://news.kddi.com/kddi/corporate/newsrelease/2016/04/28/1772.html) - KDDI 2016年4月28日。