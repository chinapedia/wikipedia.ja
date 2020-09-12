> この記事は[Firebase](https://ja.wikipedia.org/wiki/Firebase)から翻訳されています。


**Firebase**(ファイアベース)は、2011年にFirebase, Inc.が開発したモバイル・Webアプリケーション開発プラットフォームで、その後2014年にGoogleに買収された\[1\]。 2020年3月現在、Firebaseプラットフォームには19の製品があり\[2\]\[3\]、9GAGを含む150万以上のアプリが利用されている\[4\]。

## 歴史

Firebaseは、2011年にJames TamplinとAndrew Leeによって設立されたスタートアップEnvolveから発展した。Envolve は、オンラインチャット機能をウェブサイトに統合するための API を開発者に提供していた。チャットサービスをリリースした後、Tamplin と Lee は、チャットメッセージ以外のアプリケーションデータを渡すために Envolve が使用されていることに気づいた。開発者は、ゲームの状態などのアプリケーションデータをユーザー間でリアルタイムに同期させるためにEnvolveを使用していた。TamplinとLeeは、チャットシステムとそれを支えるリアルタイムアーキテクチャを分離することにした\[5\]。 2011年9月に別会社としてFirebaseを設立し\[1\]、2012年4月に一般公開した\[6\]。

Firebaseの最初の製品は、iOS、Android、Webデバイス間でアプリケーションデータを同期し、Firebaseのクラウド上に保存するAPI「Firebase Real-time Database」でした。この製品は、ソフトウェア開発者がリアルタイムでコラボレーティブなアプリケーションを構築するのを支援する。

ベータローンチから1ヶ月後の2012年5月、FirebaseはベンチャーキャピタルのFlybridge Capital Partners、Greylock Partners、Founder Collective、New Enterprise Associatesから110万ドルのシード資金を調達した\[7\]。 2013年6月にはさらに、Union Square VenturesとFlybridge Capital Partnersから560万ドルのシリーズA資金を調達した\[8\]。

2014年、Firebaseは2つの製品を発表した。Firebase Hosting\[9\] とFirebase Authenticationである\[10\] これにより、モバイルバックエンドをサービスとして位置づけた。

2014年10月、FirebaseはGoogleに買収された\[11\]。 その1年後の2015年10月、GoogleはHTML5ウェブホスティングプラットフォームのDivshotを買収し、Firebaseチームと合併した\[12\] 。

2016年5月、同社が毎年開催している開発者向けカンファレンス「Google I/O」において、FirebaseはFirebase Analyticsを導入し、モバイル開発者向けの統合BaaS（Backend-as-a-Service）プラットフォームとしてサービスを拡充することを発表した。Firebaseは現在、Google Cloud Platform、AdMob、Google Adsなど、他のさまざまなGoogleサービスと統合し、より幅広い製品と開発者向けのスケールを提供している\[17\] Android端末にプッシュ通知を配信するGoogleサービス「Google Cloud Messaging」は、Firebaseの製品「Firebase Cloud Messaging」に取って代わられ、iOSとWeb端末の両方にプッシュ通知を配信する機能が追加されていた。2017年1月、GoogleはTwitterからFabricとCrashlyticsを買収し、それらのサービスをFirebaseに追加した\[13\]\[14\]\[15\] 。

2017年10月、Firebaseは初代Firebase Realtime Databaseの後継製品として、リアルタイムドキュメントデータベース「Cloud Firestore」の提供を開始した\[16\]\[17\]\[18\]\[19\]。

## サービス内容

### 分析

#### Google Analytics

[Google Analyticsは](https://ja.wikipedia.org/wiki/Google_Analytics "wikilink")、アプリの利用状況やユーザーのエンゲージメントに関する洞察を提供する無償のアプリ測定ソリューションである\[20\]。

### Develop

#### Firebase Cloud Messaging

以前はGoogle Cloud Messaging（GCM）として知られていたFirebase Cloud Messaging（FCM）は、Android、iOS、Webアプリケーション向けのメッセージと通知のためのクロスプラットフォームソリューションで、2016年現在では無償で利用できるようになっている\[21\]。

#### Firebase Authentication

Firebase Authenticationは、クライアント側のコードのみでユーザーを認証できるサービスである。ソーシャルログインプロバイダであるFacebook、GitHub、Twitter、Googleをはじめ、Google Play Games、Apple、Yahoo、Microsoftなどのサービスプロバイダをサポートしている。また、ユーザー管理システムを搭載しており、開発者はFirebaseに保存されている電子メールとパスワードによるユーザー認証を有効にすることができる\[22\]。

#### Firebase Realtime Database

Firebaseはリアルタイムデータベースとバックエンドをサービスとして提供している。このサービスはアプリケーション開発者にAPIを提供し、アプリケーションデータをクライアント間で同期させ、Firebaseのクラウド上に保存することを可能にしている\[23\]\[24\]。データベースには、[REST APIと](https://ja.wikipedia.org/wiki/REST_API "wikilink")[AngularJS](https://ja.wikipedia.org/wiki/AngularJS "wikilink")、[React](https://ja.wikipedia.org/wiki/React "wikilink")、[Ember.js](https://ja.wikipedia.org/wiki/Ember.js "wikilink")、[Backbone.js](https://ja.wikipedia.org/wiki/Backbone.js "wikilink")などのいくつかのJavaScriptフレームワーク用のバインディングを介してアクセスすることもできる\[25\]。リアルタイムデータベースを利用する開発者は、同社のサーバーサイドで強化されたセキュリティルールを利用することで、データの安全性を確保することができる\[26\]。

#### Cloud Firestore

2019年1月31日、Cloud Firestoreが正式にベータ版として公開され、Firebaseの正式製品となった\[27\]。 Firebase独自のデータベース化システムであるReal-time Databaseの後継システムであり、Real-time Databaseで提供されていたツリービューではなく、入れ子になったドキュメントやフィールドを利用できるようになっている。

#### Firebase Storage

Firebase Storageは、ネットワークの品質に関係なく、Firebaseアプリのための安全なファイルのアップロードとダウンロードを提供し、画像、オーディオ、ビデオ、またはその他のユーザーが作成したコンテンツを保存するために使用される。これはGoogle Cloud Storageによってバックアップされている\[28\]。

#### Firebase Hosting

Firebase Hostingは、2014年5月13日にサービスを開始した静的・動的Webホスティングサービスである。[CSS](../Page/CSS.md "wikilink")、[HTML](https://ja.wikipedia.org/wiki/HTML "wikilink")、JavaScriptなどの静的ファイルのホスティングや、Cloud Functionsによるサポートに対応している\[29\] 。 サービスは、HTTP Secure（[HTTPS](../Page/HTTPS.md "wikilink")）や[Secure Sockets Layer暗号化](../Page/Transport_Layer_Security.md "wikilink")（SSL）を利用して、[CDN](https://ja.wikipedia.org/wiki/CDN "wikilink")（Content Delivery Network）を介してファイルを配信する。FirebaseはCDNであるFastlyと提携し、Firebase Hostingを支えるCDNを提供している。同社によると、Firebase Hosting は顧客からの要望から生まれたもので、開発者はリアルタイムデータベースとして Firebase を利用しているが、コンテンツをホスティングする場所を必要としていた\[30\]\[31\]。

#### ML Kit

ML Kitは、2018年5月8日にGoogle I/O 2018でベータ版として発表された開発者向けのモバイル機械学習システムである\[32\]。 ML KitのAPIには、光学式文字認識、顔検出、バーコードのスキャン、画像のラベル付け、ランドマークの認識など、さまざまな機能が搭載されている。現在、iOSまたはAndroidの開発者向けに提供されています。与えられたAPIでは不十分な場合は、独自のTensorFlow Liteモデルをインポートすることもできる\[33\]。 APIはオンデバイスまたはオンクラウドで使用することができる。

### 安定性

#### 障害解析

クラッシュレポートでは、アプリ内のエラーの詳細なレポートを作成する。エラーは、類似したスタックトレースのクラスタにグループ化され、アプリユーザーへの影響の深刻度によってトリアージされる。自動レポートに加えて、開発者はカスタムイベントをログに記録して、クラッシュに至るまでの手順を把握するのに役立つ\[34\]。

#### 性能評価

Firebase Performanceは、アプリのパフォーマンスとアプリのユーザーが体験するレイテンシーについての洞察を提供する。

#### Firebase Test Lab

Firebase Test Labは、AndroidとiOSのアプリを一括してテストするためのクラウドベースのインフラを提供する。開発者は、様々なデバイスやデバイス構成でアプリをテストすることができる。テスト結果（ログ、動画、スクリーンショットなど）は、Firebaseコンソールで確認することができる。開発者がアプリのテストコードを書いていなくても、Test Lab は自動的にアプリを動作させ、クラッシュを探すことができる。Test Lab for iOSは現在ベータ版である\[35\]。

#### Admob

[Admob](https://ja.wikipedia.org/wiki/Admob "wikilink")はFirebaseのオーディエンスと統合されたGoogleの製品である。

### Grow

#### Firebase Dynamic Links

Dynamic Firebase linksは、デスクトップのウェブブラウザ、iOS、Android、モバイルアプリへの詳細なリンクなど、複数のプラットフォームで「最高の体験」を提供するために、動的に挙動を変化させるスマートなURLである。ダイナミックリンクはすべてのアプリのインストールで機能する。ユーザーがiOSまたはAndroidでダイナミックリンクを開き、アプリがインストールされていない場合、まずアプリをインストールするように促される。インストールされると、アプリケーションは実行を開始し、リンクにアクセスできるようになる\[36\]。

## 参照

## 外部リンク

  -
[Category:2014_mergers_and_acquisitions](https://ja.wikipedia.org/wiki/Category:2014_mergers_and_acquisitions "wikilink") [Category:Cloud_computing_providers](https://ja.wikipedia.org/wiki/Category:Cloud_computing_providers "wikilink") [Category:Cloud_platforms](https://ja.wikipedia.org/wiki/Category:Cloud_platforms "wikilink") [Category:Companies_established_in_2011](https://ja.wikipedia.org/wiki/Category:Companies_established_in_2011 "wikilink") [Category:Google_acquisitions](https://ja.wikipedia.org/wiki/Category:Google_acquisitions "wikilink") [Category:Google_Cloud](https://ja.wikipedia.org/wiki/Category:Google_Cloud "wikilink") [Category:Software_companies_established_in_2011](https://ja.wikipedia.org/wiki/Category:Software_companies_established_in_2011 "wikilink") [Category:Software_companies_of_the_United_States](https://ja.wikipedia.org/wiki/Category:Software_companies_of_the_United_States "wikilink")

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
12.
13.
14.
15.
16.
17.
18.
19.  Androidheadlines.com|date=2017-10-05|work=AndroidHeadlines.com {{\!}}|access-date=2017-10-19|language=en-US}}
20.
21.
22.
23.
24.
25.
26.
27.
28.
29. [dynamic Node.js support through Cloud Functions](https://firebase.google.com/docs/hosting/functions)
30.
31.
32.
33.  Machine learning for mobile developers {{\!}} Firebase|website=Firebase|language=en|access-date=2018-07-07}}
34.
35.
36.