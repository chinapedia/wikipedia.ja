> この記事は[HP Integrity NonStop](https://ja.wikipedia.org/wiki/HP_Integrity_NonStop)から翻訳されています。


**HPE Integrity NonStop**は、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")社が販売する[無停止コンピュータ](https://ja.wikipedia.org/wiki/無停止コンピュータ "wikilink")のシリーズ。もとは[タンデムコンピューターズ](../Page/タンデムコンピューターズ.md "wikilink")社の製品であったが、企業買収により[コンパック](../Page/コンパック.md "wikilink")を経てヒューレット・パッカードの製品となった。他にはない99.9999%の可用性を実現するアーキテクチャ「**NonStop**（無停止）」が採用された[オープンシステムである](../Page/オープンシステム_\(コンピュータ\).md "wikilink")。1993年以来[MIPSプロセッサを採用していたが](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")、2005年にインテルの[Itanium 2プロセッサに移行し](https://ja.wikipedia.org/wiki/Itanium "wikilink")、日本では製品名を**HP Integrity NonStop サーバ**としている。なお、Nonstop, Non-stop, Non-Stopなどと誤記されることが多いが「NonStop」が正しい。

## 歴史

2005年以前に関しては、[タンデムコンピューターズ](../Page/タンデムコンピューターズ.md "wikilink")を参照のこと。

### NonStop Server Sシリーズ

コンパックコンピュータ時代に発売開始され、MIPSプロセッサを使用する。 それまでのKシリーズと大きく異なるのは次の２点である。

1.  内部にServerNetと呼ばれる高速バスを使用し、これによってボトルネックを減少させている。
2.  PMFと呼ばれる、CPU・ServerNet・ディスクコントローラなどを一体化したハードウェアを採用した。

パフォーマンスが向上し、価格が下落することでユーザも大きく増加した。 2008年末で既に販売は終了している。

### NonStop Integrity Server NSシリーズ

日本HPとの合併により、それまで使用していたAlpha, PA-RISCなどのCPUを使用したサーバをIntel社チップに統合することで投資資源を最適化することにした。これはNonStopも例外ではなく、それまで使用してきたMIPSチップからItaniumプロセッサに移行している。 なお、HPはItaniumのシングルコアを採用したモデルをNSシリーズと呼んでいる。 NSシリーズの大きな特徴は下記の通りである。

1.  CPUにItaniumを使用することで、OSが全面的に書き換えられパフォーマンスも大きく向上した。
2.  CPUの冗長化構成に、これまでの「ロックステップ」による二重化からTMR, DMRという三重化・二重化構成が選べるようになった。これはCPUの演算結果をLSUで比較することで、物理CPUが停止しても他のCPUが動作する限り業務的には影響が発生しない特徴を持つ機能である。この考え方自体は以前のUNIX系Integrityで採用された考え方を継承している。
3.  ハードウェアが他のプラットフォームと共通部品が増え、19インチラックに収められるようになった。これは外見からNonStopと判断できなくなることを意味し、以前「Tandemの黒い壁」と呼ばれた特徴を失うことになる。しかし、現在のマシンルームの大半が19インチラックを採用している以上、やむを得ない決定と言えるであろう。

NSシリーズのTMR構成は通信・金融業などよりミッションクリティカルな顧客に多く採用された。しかし、ItaniumのシングルコアをIntelが今後開発する予定はなく、HPもマルチコアで演算結果比較を必要とするロジックを開発する予定はないため、NSシリーズの後継機種は発売されない予定である。

  - 2005年6月 [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")®[Itanium](https://ja.wikipedia.org/wiki/Itanium "wikilink")®2プロセッサ搭載　「[HP Integrity NonStop サーバ](https://ja.wikipedia.org/wiki/HP_Integrity_NonStop_サーバ "wikilink")　NS16000」発表
  - 2006年6月 [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")®[Itanium](https://ja.wikipedia.org/wiki/Itanium "wikilink")®2プロセッサ1.5GHz搭載　「[HP Integrity NonStop サーバ](https://ja.wikipedia.org/wiki/HP_Integrity_NonStop_サーバ "wikilink")　NS14000」発表

CPUの高速化・メモリの拡張により、アプリケーション的にも大きな変化が見られた。これまでのGuardianと呼ばれる独自OSからOSSと呼ばれるUNIX互換OSでの開発に軸足が移された。オープン系のミドルウェアに対応が進んだのもこの一環であり、Java, Tomcatなどの対応によりパッケージソフトウェアが動作するようになったのは大きな進歩と言えるであろう。

### NonStop Integrity Server NBシリーズ

NBシリーズ（NB50000c）はItaniumのマルチコア対応を行ったモデルである。 CPUはブレードタイプを使用することになったため、外見としては通常のブレードサーバと見分けがつかない。ブレードキャビネットの中にNonStop用の部品を一部使用しているのみである。 現在はデュアルコアのみが発売されているが、更に性能が向上することになった。また、集積度が高まったことも特徴といえるであろう。 NS2000と呼ばれる、CPU数限定のモデルも発売された。これはブレードを使用していないがデュアルコアを使用している。戦略的な価格を取っていることも特徴的である。 今後のNonStopはItaniumチップの発表に合わせ、マルチコア化が進むと考えられる。

現在、NonStopサーバの価格帯は以前と比べて非常に安価になってきている。しかし、汎用機・IAサーバと比較した時の差は依然として大きく、立ち位置を難しくしているとも言える。

## 外部リンク

  - [HPE Integrity NonStop サーバー](https://www.hpe.com/jp/ja/servers/nonstop.html)

[Category:サーバ_(ハードウェア)](https://ja.wikipedia.org/wiki/Category:サーバ_\(ハードウェア\) "wikilink") [Category:ヒューレット・パッカードの製品](https://ja.wikipedia.org/wiki/Category:ヒューレット・パッカードの製品 "wikilink")