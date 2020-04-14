> この記事は[Gravatar](https://ja.wikipedia.org/wiki/Gravatar)から翻訳されています。


**Gravatar**（グラバター）は、サイトを越えて利用できる[アバター](../Page/アバター.md "wikilink")を作成できるサービス。トム・プレストン・ワーナーが開発した。2007年に[Automattic](https://ja.wikipedia.org/wiki/Automattic "wikilink")が買収し、ブログのプラットフォームであるWordPress.comに統合されている。

## 設計図

ユーザーはメールアドレスでGravatarにユーザー登録し、メールアドレスに連携したデジタルアバターをアップロードできるほか、主な[ブログ](../Page/ブログ.md "wikilink")アプリでGravatarの[プラグイン](../Page/プラグイン.md "wikilink")を利用できる。[ブログ](../Page/ブログ.md "wikilink")にコメントを投稿すると登録された[メールアドレス](../Page/メールアドレス.md "wikilink")に関連付けられたアバターをGravatarで検索し、もし存在すればコメントと共にそのアバターが表示される。

[WordPress](../Page/WordPress.md "wikilink")はバージョン2.5\[1\]から、ウェブベースの[プロジェクト管理アプリ](../Page/プロジェクトマネジメント.md "wikilink")[Redmine](https://ja.wikipedia.org/wiki/Redmine "wikilink")はバージョン0.8から、ネイティブでGravatarに対応している\[2\]。また、[Drupal](../Page/Drupal.md "wikilink")や[MODX](../Page/MODX.md "wikilink")といったウェブベースの[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink")で利用できるサードパーティ製のGravatarモジュールも存在する\[3\]\[4\]。

アバターの画像は最大で横2048[ピクセル](../Page/ピクセル.md "wikilink")で、正方形のみに対応し、表示サイズのデフォルトは80x80ピクセルとなっている\[5\]。もしアップロードしたアバターのサイズが異なる場合は適度に拡大縮小される。Gravatarは映画業界の[MPAAに準じた年齢制限のレイティングシステムを採用しており](../Page/アメリカ映画協会_\(業界団体\).md "wikilink")、[ウェブマスター](https://ja.wikipedia.org/wiki/ウェブマスター "wikilink")は[ウェブサイト](../Page/ウェブサイト.md "wikilink")に表示するアバターを任意のレベルで制限できる。

ウェブマスターは、ユーザーがGravatarに登録していない場合、Identiconと呼ばれるIDから自動生成したユニークなアバターを自動的に表示するように設定できる。

Gravatarの[Webサーバ](../Page/Webサーバ.md "wikilink")ーは、メールアドレスから生成した[MD5](../Page/MD5.md "wikilink")の[ハッシュ値を含む特定の](../Page/ハッシュ関数.md "wikilink")[URLにアクセスすると対応したアバターを返す](../Page/Uniform_Resource_Locator.md "wikilink")。しかし、この手法は[辞書攻撃](../Page/辞書攻撃.md "wikilink")や[レインボーテーブル](../Page/レインボーテーブル.md "wikilink")といった攻撃に対して脆弱であることが分かっている\[6\]。実際にあった例として、あるフォーラムではユーザーの10%以上がフォーラムで表示されるユーザー名とGravatarに送られるURLからメールアドレスを特定することが可能だった\[7\]。

## メタデータ

ユーザーのプロファイルは[hCard](https://ja.wikipedia.org/wiki/hCard "wikilink")、[JSON](../Page/JavaScript_Object_Notation.md "wikilink")、[XML](../Page/Extensible_Markup_Language.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[vCard](https://ja.wikipedia.org/wiki/vCard "wikilink")などのさまざまな規格に対応しており、[QRコード](../Page/QRコード.md "wikilink")で入出力できる。生データ形式 (JSON, XML, PHP) はPortable Contacts仕様に準じている\[8\]。

## 歴史

当初、Gravatarのサービスは長い間放置されていた。急にGravatarの人気が高まり、多くの帯域幅が必要になったため、急遽新バージョンの開発に取りかかった。2007年2月16日にGravatar 2.0がリリースされた\[9\]。サーバースクリプトが改善され、[インターネット](../Page/インターネット.md "wikilink")の別の場所にすでに保存されている画像をトリミングして使用できるような機能も密かに追加されたほか、アカウントごとに2つのアバターが持ててユーザーによるアバターの変更が容易になった。新たにスタートしたGravatar Premiumサービスでは、メールアドレスを無制限に登録できた。

2007年6月11日には、Gravatar 2.0がリリースされてからユーザーが32,000人増えたことを、トム・プレストン・ワーナーが発表した\[10\]。

2007年10月18日には[Automattic](https://ja.wikipedia.org/wiki/Automattic "wikilink")がGravatarを買収し\[11\]、これまでの有料サービスがすべて無料化されてレスポンス速度が向上し、無料化の直前に料金を支払ったユーザーに返金した\[12\]。

2010年12月2日には、[マット・マレンウェッグ](https://ja.wikipedia.org/wiki/マット・マレンウェッグ "wikilink")が*The Big Web Show*でGravatarが1日に約200億枚のアバターを表示していることを明らかにした\[13\]。

## 出典

## 外部リンク

  -

[Category:仮想世界](https://ja.wikipedia.org/wiki/Category:仮想世界 "wikilink") [Category:インターネットの文化](https://ja.wikipedia.org/wiki/Category:インターネットの文化 "wikilink") [Category:ブログソフト](https://ja.wikipedia.org/wiki/Category:ブログソフト "wikilink")

1.
2.
3.
4.
5.
6.  [Gravatars: why publishing your email's hash is not a good idea](http://www.developer.it/post/gravatars-why-publishing-your-email-s-hash-is-not-a-good-idea) Developer IT, December 8, 2009
7.
8.
9.
10.
11.
12.
13.