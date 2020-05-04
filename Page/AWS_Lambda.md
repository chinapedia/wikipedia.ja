> この記事は[AWS Lambda](https://ja.wikipedia.org/wiki/AWS_Lambda)から翻訳されています。


**AWS Lambda**は[Amazon.com](../Page/Amazon.com.md "wikilink")が提供している[Amazon Web Services](https://ja.wikipedia.org/wiki/Amazon_Web_Services "wikilink") (AWS) の1つで、[イベントの発生に応じて](../Page/イベント_\(プログラミング\).md "wikilink")[プログラムを実行する環境を提供する](../Page/プログラム_\(コンピュータ\).md "wikilink")[クラウドコンピューティング](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink")サービスである。2014年11月に提供が開始された。

プログラムの実行に必要な[サーバ](../Page/サーバ.md "wikilink")などの環境が予め整えられているため、プログラムを作成して登録するだけで実行できるという特徴がある。同じAWSのサービスである[Amazon EC2は](https://ja.wikipedia.org/wiki/Amazon_Elastic_Compute_Cloud "wikilink")[仮想化](../Page/仮想化.md "wikilink")されたサーバを提供するのに対し、AWS Lambdaはプログラムの実行環境のみを提供するため、管理の手間が省かれるというのも特徴だ。プログラムの実行に必要なリソースは自動的に計算・割り当てされ、実行時間や回数などに応じて利用料金を支払う従量課金制となっている。また、実行するプログラムについては多数の[プログラミング言語](../Page/プログラミング言語.md "wikilink")に対応している。

## 特徴

AWS Lambdaはプログラムを登録するだけで実行できるようになる事が特徴で、同じクラウドコンピューティングサービスであるAmazon EC2と比較すると、AWS Lambdaは利用が容易である。Amazon EC2では仮想化されたサーバが提供されるため、そこに[オペレーションシステム](https://ja.wikipedia.org/wiki/オペレーションシステム "wikilink")や[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")をインストールするなどの環境構築の手間がかかり、それらの管理も行わなければならない。AWS Lambdaでは、用途をプログラム実行のみに絞ることで、利用者によるそれらの環境構築の手間を省いているのである\[1\]。

登録したプログラムは「Lambda 関数」と呼ばれ、何らかのイベントをトリガーとして実行される\[2\]。AWS Lambdaの登場前は、イベントをトリガーとするプログラムを実行するには、Amazon EC2を使い「イベントを待ち受けする」という常時実行のアプリケーションが必要だった。AWS Lambdaはイベントがトリガーとなりプログラムが実行されるため、イベントが発生していない状態ではプログラムの実行が不要になるのである。これは言い換えると「イベントの待ち受けをAWS Lambdaが代行している」とすることができる\[3\]。[Amazon API Gatewayを経由する](https://ja.wikipedia.org/wiki/Amazon_API_Gateway "wikilink")[HTTPリクエストや](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[Amazon S3や](https://ja.wikipedia.org/wiki/Amazon_Simple_Storage_Service "wikilink")[Amazon DynamoDBといったAWSの各種サービスにおける変更などの検知などがプログラムの実行トリガーとなる](https://ja.wikipedia.org/wiki/Amazon_DynamoDB "wikilink")\[4\]\[5\]。

プログラムの実行に必要な処理能力は、プログラムの実行時に自動的に割り当てられるため、イベントの頻度が増加しても処理の速度は維持することが可能である\[6\]。[テレビゲーム](https://ja.wikipedia.org/wiki/テレビゲーム "wikilink")では、年数回のイベントで一時的に大きな負荷がかかることがある場合にAWS Lambdaを使用することで、そのイベントのためだけにサーバを増強することを避けるために応用されているという\[7\]。

[Amazon CloudFront上でLambdaを実行する](https://ja.wikipedia.org/wiki/Amazon_CloudFront "wikilink")「Lambda@Edge」というサービスもある。これを使うと世界各地に置かれているCloudFrontの[コンテンツデリバリネットワーク](../Page/コンテンツデリバリネットワーク.md "wikilink") (CDN) 上でプログラムが実行されるため、より利用者に近い場所でプログラムが動くことによる負荷分散・レスポンス向上が期待できる\[8\]。

対応するプログラミング言語は[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Go](https://ja.wikipedia.org/wiki/Go "wikilink")、[PowerShell](../Page/PowerShell.md "wikilink")、[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")、[C\#](../Page/C_Sharp.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")と多岐に渡る。サードパーティの物も含め[フレームワーク](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")、[SDK](../Page/ソフトウェア開発キット.md "wikilink")、[ライブラリ](../Page/ライブラリ.md "wikilink")などを使用できる事を謳っており、これらを「Lambda Layer」というパッケージに一纏めにすることで複数のLambda 関数で共有することが可能である\[9\]。

## 料金

利用料金については前述の通り従量課金制であり、実際にプログラムを実行した回数と時間、Lambda関数に割り当てた[メモリの量によって変化する](../Page/主記憶装置.md "wikilink")。プログラムの実行時間は、プログラムの実行開始から処理の終了までの100 [ミリ秒](https://ja.wikipedia.org/wiki/ミリ秒 "wikilink")ごとの切り上げで計算される。無期限の無料利用枠が設けられており、1か月で100万回の実行回数、メモリの割り当て量に応じて最大320万秒の実行時間が無料で利用できる\[10\]。

## 脚注

## 外部リンク

  - [AWS Lambda](https://aws.amazon.com/jp/lambda/)

[Category:Amazon.com](https://ja.wikipedia.org/wiki/Category:Amazon.com "wikilink") [Category:Webサービス](https://ja.wikipedia.org/wiki/Category:Webサービス "wikilink")

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