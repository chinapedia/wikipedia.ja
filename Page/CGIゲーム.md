> この記事は[CGIゲーム](https://ja.wikipedia.org/wiki/CGIゲーム)から翻訳されています。


**CGIゲーム**（シージーアイゲーム）とは、[CGI](../Page/Common_Gateway_Interface.md "wikilink")[プログラムとして作られた](../Page/プログラム_\(コンピュータ\).md "wikilink")[ブラウザゲーム](../Page/ブラウザゲーム.md "wikilink")である。多くのCGIゲームは[ウェブサービスとして公開され](../Page/Webサービス.md "wikilink")、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")などを通じてプレイすることができる。

## 概要

CGIゲームは、古く[パソコン通信](../Page/パソコン通信.md "wikilink")の時代にその原型を見ることのできる「サーバ上で動作させるゲーム」である。パソコン通信時代と違うのは、サーバプログラムが[テキスト形式のデータで結果を出力してくるのではなく](../Page/プレーンテキスト.md "wikilink")、ウェブブラウザで開かせるための[HTMLなどで送信され](../Page/HyperText_Markup_Language.md "wikilink")、ユーザはこのブラウザ上に表示されたものを介して操作する点であり、CGIを利用することから、このように呼ばれている。

表示はすべてウェブ閲覧用の標準的なウェブブラウザを介することもありホストコンピュータ（プレイヤーの使っているパソコン等）の[OSには依存しない](../Page/オペレーティングシステム.md "wikilink")。表示文字量の制限などが無ければ、[携帯電話](../Page/携帯電話.md "wikilink")のブラウザ上からも操作可能なCGIゲームも存在する。しかしブラウザの表示機能に依存するため、一部ブラウザからの使用に制限や問題の出るものも見られる。

サーバ上で動作するプログラム本体は主に[C言語](../Page/C言語.md "wikilink")や[Perl](../Page/Perl.md "wikilink")、[PHPなどで](../Page/PHP_\(プログラミング言語\).md "wikilink")[実装](../Page/実装.md "wikilink")されている（当然サーバ上で動作してブラウザへと返信が返せるようになっていれば、使用される[プログラミング言語](../Page/プログラミング言語.md "wikilink")は限定されない）が、ブラウザの表現能力が向上し、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や[ダイナミックHTML](../Page/ダイナミックHTML.md "wikilink")などで記述されたプログラムや[Adobe Flash等の能動的なプラグインを処理できることから](../Page/Adobe_Flash.md "wikilink")、ブラウザ上の表示機能は各々のホストコンピュータに任せ、他プレイヤーとの連携やデータの管理のみがサーバで行われる様式のものも登場している。

これらは他のJavaで書かれたゲームプログラムやFlashゲームと区別がつき難いこともあり、CGIゲームの範疇に含まれないケースも見られる。他方、サーバを介す必要の無い[P2Pという方式の通信を行うものもある](https://ja.wikipedia.org/wiki/ピア・ツー・ピア "wikilink")。しかしこれらは、CGIゲームの定義内には非ず、[オンラインゲーム](../Page/オンラインゲーム.md "wikilink")としてのみ定義される。

また上記にて便宜的に「サーバ」とは表現したが、家庭向けのパーソナルコンピュータでも設定如何でウェブサーバとして、またはPerlなどの代表的なCGIプログラム実装言語を利用できるため、単にCommon gateway interface（CGI）の仕組みを利用していれば、これらCGIゲームの範疇に含むといえる。

## 歴史

CGIゲームは、CGI[チャット](../Page/チャット.md "wikilink")と共に1990年代後半に爆発的にヒットした。代表作として、数万人の登録者を有し、プレイステーションに移植されるに至った『[ロードオブモンスターズ](../Page/ロードオブモンスターズ.md "wikilink")』シリーズが挙げられる。この人気作、『ロードオブモンスターズ』は4作目まで約10年間ほど続き、20世紀で幕を閉じることになる。

その後、21世紀に入りロードオブモンスターズなどの無配布型CGIゲームに代わって新たに台頭したのが、有料化した課金型CGIゲームと、[ソースコード](../Page/ソースコード.md "wikilink")を公開して[シェアを稼ぐ形の配布型CGIゲームである](../Page/市場占有率.md "wikilink")。課金型CGIや配布型CGIゲームの多くは、その後登場した[MMORPG](../Page/MMORPG.md "wikilink")や[ソーシャルゲーム](https://ja.wikipedia.org/wiki/ソーシャルゲーム "wikilink")にシェアを奪われた。

## 配布型CGIゲームとは

配布元から[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")したCGIスクリプトを説明に従ってWebサーバへ[アップロード](../Page/アップロード.md "wikilink")することによって個人でも比較的容易に設置することができる。また、その多くは改造が許可されているので運用者によって多数のバリエーションが生まれ、かつほとんどが無料で楽しめることから、Webサイト運営者に人気の[コンテンツ](../Page/コンテンツ.md "wikilink")である。

一方、これらのプログラムを設置することにより、単なるページ閲覧を大幅に超えるレベルにまでサーバ負荷が増大することから、たとえ[掲示板などのCGIスクリプト設置を認めて](../Page/電子掲示板.md "wikilink")[Webサーバ](../Page/Webサーバ.md "wikilink")をレンタルしている[プロバイダであっても](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、ゲームCGIの設置は認めていないことが多く、有料レンタルサーバにおいては設置を認めている場合もある。

企業が製作するゲームとは違って個人製作のものが主流となっており、21世紀に入ってからは数多くの[フリーウェア](../Page/フリーウェア.md "wikilink")がソースコードとともに公開されていた。ゲームの形態は個人で遊ぶ形態と、多人数が同時参加する[オンラインゲーム](../Page/オンラインゲーム.md "wikilink")形態のモノも提供されている。

製作されるジャンルは[RPGや](https://ja.wikipedia.org/wiki/コンピューターRPG "wikilink")[シミュレーションゲーム](../Page/シミュレーションゲーム.md "wikilink")など多岐にわたるが、中には果たしてゲームと呼ぶべきかどうかも疑わしい「不特定多数参加型環境ソフト（眺めたり、勝手気侭に弄り回すだけ）」というものすらある。参加人数は一人で遊ぶものから、一定数の制限枠内で競い合うもの、さらには不特定多数が好き勝手に出入り自由なものも見られるため、明確な定義は難しい。

CGIがウェブ上の[コミュニケーション](../Page/コミュニケーション.md "wikilink")を[電子掲示板](../Page/電子掲示板.md "wikilink")や[チャット](../Page/チャット.md "wikilink")などの形で仲介しているように、これらCGIゲームも、「コンピュータゲームという[インタフェースを介して](../Page/インタフェース_\(情報技術\).md "wikilink")、コミュニケーションを行う仕組み」ともいえる。

## 課金型CGIゲームの代表作

  - [アクア＝エリアス](../Page/アクア＝エリアス.md "wikilink")
  - The Treasure of GENUM

## 配布型CGIゲームの代表作

  - GundamField
  - Script Of Saga II
  - ネット航海時代
  - [箱庭諸島](../Page/箱庭諸島.md "wikilink")
  - Free Fight Adventure（旧称Final Fantasy Adventure）
  - 罪と罰++二律背反
  - SOLD OUT
  - 劇空間ぱわふるリーグ2
  - ＠パーティー2
  - Blind Justice
  - VIP列島

## 関連項目

  - [CGI](../Page/Common_Gateway_Interface.md "wikilink")
  - [ブラウザゲーム](../Page/ブラウザゲーム.md "wikilink")
  - [オンラインゲーム](../Page/オンラインゲーム.md "wikilink")
  - [ソーシャルゲーム](https://ja.wikipedia.org/wiki/ソーシャルゲーム "wikilink")

[Category:CGIゲーム](https://ja.wikipedia.org/wiki/Category:CGIゲーム "wikilink")