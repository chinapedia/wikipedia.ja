> この記事は[Misskey](https://ja.wikipedia.org/wiki/Misskey)から翻訳されています。


**Misskey**（ミスキー）は、日本発の[分散型ミニブログ用のオープンソースソフトウェアである](https://ja.wikipedia.org/wiki/分散型ソーシャル・ネットワーク "wikilink")。syuiloが開発している。

## 概要

Misskeyは短文投稿のための分散型SNSである。利用者の投稿は「ノート」と呼ばれる。 Misskeyは他の分散型SNSと同様、管理者や設置場所の異なったサーバーが存在し、利用者はサーバーを選ぶ、あるいは自身でサーバーを開設することによって[fediverse](https://ja.wikipedia.org/wiki/fediverse "wikilink")に参加する。 Misskeyインスタンスへの登録にメールアドレスは不要である\[1\]。 Misskeyという名前は作者のsyuiloが名前を考えていたときに偶然聴いていた[May'n](../Page/May'n.md "wikilink")の楽曲「Brain Diver」の歌詞から採られている\[2\]。

## 発展

### 開発

Misskeyは[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")上でソースコードを公開しており、改善の提案を行うことができる。 自分で改造することも自由である。 ただし改造したMisskeyでサーバーを運営する場合は、[AGPL](https://ja.wikipedia.org/wiki/AGPL "wikilink")v3に基づいて改造後のソースコードを公開する義務がある。 また[API](https://ja.wikipedia.org/wiki/API "wikilink")が公開されているので、これを利用してアプリを作成することもできる。 翻訳は[Crowdin](https://ja.wikipedia.org/wiki/Crowdin "wikilink")上で行われている。

### 使用技術

[TypeScript](https://ja.wikipedia.org/wiki/TypeScript "wikilink")と[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")を使って書かれている。 データベースとして [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")を使用、 2018年2月以降はWebクライアントに[Vue.js](https://ja.wikipedia.org/wiki/Vue.js "wikilink")を使用している。 サーバー間の通信プロトコルには [ActivityPub](https://ja.wikipedia.org/wiki/ActivityPub "wikilink")が使用されているため、Misskeyのサーバー間だけでなく、 [Mastodon](https://ja.wikipedia.org/wiki/Mastodon "wikilink")や[Pleroma](https://ja.wikipedia.org/wiki/Pleroma "wikilink")など同標準に準拠した他のミニブログのサーバーと通信可能となっている。

### 沿革

  - 2014年 - 開発が開始され、運用が始まる
  - 2018年4月8日 - サーバー間の通信プロトコルをActivityPub対応して分散型SNSになる\[3\]。コードネームをnighthikeと改称。
  - 2018年7月10日 - joinmisskeyが開設される。
  - 2019年4月14日 - v11をリリース。データベースソフトウェアにPostgreSQLを採用した。コードネームをdaybreakと改称。
  - 2020年2月6日 - v12をリリース。コードネームはindigo。

## 機能

### タイムライン

Misskeyは4種類のタイムラインを持つ。 ホームタイムラインには自分がフォローしたユーザーの投稿が新しい順に表示される。 同様にローカルタイムラインにはそのサーバー内のすべてのユーザーの、 ソーシャルタイムラインにはホームタイムラインとローカルタイムラインを合わせた、 グローバルタイムラインにはリモートも含めてそのサーバーが認識しているすべてのユーザーの投稿が表示される。

### 他の特徴的な機能

  - 藍
    Misskeyの看板娘とされる少女。同名のBotが存在し、挨拶を返す、迷路を生成する、数当てやリバーシの対戦相手になる等の機能がある。その他ある特定のフレーズに反応を返すこともできる。
  - ドライブ
    ユーザーの投稿したファイルを管理する機能。 投稿に添付したりアカウントのアイコンに設定したりしたファイルはドライブに追加される。ファイルを直接ドライブにアップロードすることも可能。
  - アンケート
    投稿にアンケートを添付できる。選択肢を2 - 10個設定し、ユーザーが1つ以上の項目に投票する。 アンケートの期限も自由に設定できる。
  - リバーシ
    Misskeyユーザー同士で[リバーシ](https://ja.wikipedia.org/wiki/リバーシ "wikilink")で遊ぶことができる。変則ルールにも対応している。
  - Cat
    有効にすると、自分の全投稿で「な」と「ナ」が「にゃ」と「ニャ」に変換される。 またユーザー名の横に「cat」バッジが付く。 無効化すると元に戻る。
  - MFM
    Misskey Flavored Markdownという[Markdown](https://ja.wikipedia.org/wiki/Markdown "wikilink")風の構文を投稿やプロフィールに使うことができる。

## 派生

Dolphinは、Misskeyの派生として2019年10月から開発が始まったオープンソースの分散マイクロブログソフトウェアである。 1人もしくは少人数サーバー用途向けとされている。 サーバーの構築方法はMisskeyとほぼ同じであるが、ビルドに要するスペックはMisskeyよりも低い。

## マストドンとの違い

MisskeyもマストドンもActivityPub規格に準拠した分散型SNSであるが、 依存するプログラミング言語とライブラリが異なり、APIの互換性もない。 思想的にMastodonがTwitterやFacebookなどの中央集権型SNSを批判する立場をとる一方で、 当初は分散型SNSとして設計されていなかったMisskeyはユーザーが快適な環境を求める選択肢の一つとして提示されている\[4\]。

## 出典

<references />

## 関連項目

  - [ActivityPub](https://ja.wikipedia.org/wiki/ActivityPub "wikilink")
  - [Mastodon](https://ja.wikipedia.org/wiki/Mastodon "wikilink")

[Category:ソーシャル・ネットワーキング・サービス](https://ja.wikipedia.org/wiki/Category:ソーシャル・ネットワーキング・サービス "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ミニブログ](https://ja.wikipedia.org/wiki/Category:ミニブログ "wikilink") [Category:ブログソフト](https://ja.wikipedia.org/wiki/Category:ブログソフト "wikilink")

1.
2.
3.
4.