> この記事は[Help:URL](https://ja.wikipedia.org/wiki/Help:URL)から翻訳されています。


ウィキペディアにおける、一般にアドレスと呼ばれる**[URI](https://ja.wikipedia.org/wiki/URI "wikilink")** ([URL](https://ja.wikipedia.org/wiki/URL "wikilink"))について説明します。ウィキペディアのURIは、主に、通常の記事を表示する際の単純な形式と、引数をとる形式の2種類があります。このうち、引数について主に説明しています

引数を理解することで、見たい範囲を指定するといったことができるようになるでしょう。 引用してきたら、参考にして書き込むのもいいでしょう

## ページ

ウィキペディア日本語版の [URIは](../Page/Uniform_Resource_Identifier.md "wikilink") <https://ja.wikipedia.org/> です。

各記事のURIは、このアドレスの後に、`wiki/ページ名` を続けます。半角空白は、[アンダースコア](../Page/アンダースコア.md "wikilink") `_` に置換されたものとなります。

| 記事名                                                               | 通常のURI                                     | 引数形式のURI                                                |
| ----------------------------------------------------------------- | ------------------------------------------ | ------------------------------------------------------- |
| [ワイン](../Page/ワイン.md "wikilink")                                  | <https://ja.wikipedia.org/wiki/ワイン>        | <https://ja.wikipedia.org/w/index.php?title=ワイン>        |
| [Japan Expo](https://ja.wikipedia.org/wiki/Japan_Expo "wikilink") | <https://ja.wikipedia.org/wiki/Japan_Expo> | <https://ja.wikipedia.org/w/index.php?title=Japan_Expo> |

以降は主に、引数を用いた形式にて説明していきます。複数の引数は`&`によってつなげることで同時に使えます。また index.php は省略できます。

### パーセントエンコーディング

なお、[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")の[アドレスバー](https://ja.wikipedia.org/wiki/アドレスバー "wikilink")では日本語を直接指定するとうまく動作しない場合があります。その場合は、[UTF-8](../Page/UTF-8.md "wikilink")の[パーセントエンコーディング](../Page/パーセントエンコーディング.md "wikilink")に変換します。

  - ワインでは、`%E3%83%AF%E3%82%A4%E3%83%B3` となります。URIは以下です。
  - <https://ja.wikipedia.org/wiki/%E3%83%AF%E3%82%A4%E3%83%B3>

このパーセントエンコーディング形式へは簡単に変換できます。[マジックワード](https://ja.wikipedia.org/wiki/Help:マジックワード "wikilink") の {{fullurl:ページ名}}を用います。

  - {{fullurl:ワイン}}

  -
### リダイレクトしない

[リダイレクトページのリダイレクトを無効にする](https://ja.wikipedia.org/wiki/Help:リダイレクト "wikilink")。`redirect=no`を使います。

<https://ja.wikipedia.org/w/index.php?title=葡萄酒&redirect=no>

特に[特別ページへのリダイレクトでは](https://ja.wikipedia.org/wiki/Help:特別ページ "wikilink")、リンク元へのリンクがないので、この引数を使います。

## 最近更新したページ

ある時間以降の更新履歴を見るには、`from=yyyymmddhhmmss`を使います。数字で年月日・時分秒です。例えば、 年日 (UTC) 以降の更新履歴を見るには。

<https://ja.wikipedia.org/w/index.php?title=特別:最近の更新&from=>

表示するページ数の上限を変えるには、`para=limit`を使います。

<https://ja.wikipedia.org/w/index.php?title=特別:最近の更新&from=>\&limit=25

指定した日時以降の全ての更新を表示するには、limit に大きな数を指定して下さい。指定できる最大値は 5000 です。それ以上の数でも5000までしか表示されません。また[ログイン](https://ja.wikipedia.org/wiki/Help:ログイン "wikilink")**している**場合、5000よりも少ない数しか指定できません（ログイン時に指定できる数値は不明です）。

[bot](https://ja.wikipedia.org/wiki/Wikipedia:Bot "wikilink") による編集を表示するには、`hidebots=0`と指定します。

## 編集履歴

ある記事の編集履歴を見るには、`action=history`を使います。

<https://ja.wikipedia.org/w/index.php?title=ワイン&action=history>

（先頭から）31番目～35番目の編集を表示するには、`offset=30`で30番目まで省略し、`limit=5`で5つだけ表示します。

<https://ja.wikipedia.org/w/index.php?title=ワイン&limit=5&offset=30&action=history>

記事の履歴から過去の版を開くと`oldid`という引数があります。これがその版を特定するためのID番号です。

<https://ja.wikipedia.org/w/index.php?title=ワイン&oldid=132281>

この際の`title=ワイン`は、実際に表示する版の決定にはまったく関係していません。oldidを指定した時には、titleは省略することも可能です。

### 二つの版の差分を見るには

ワインの記事のさきほどの版と最新版の[差分を見るには](https://ja.wikipedia.org/wiki/Help:差分 "wikilink")、

<https://ja.wikipedia.org/w/index.php?title=ワイン&diff=0&oldid=132281>

一番最近の更新と最新版の差分を見るには、

<https://ja.wikipedia.org/w/index.php?title=ワイン&diff=0&oldid=0>

とします。

特定の二つの版の差分を見るには、

<https://ja.wikipedia.org/w/index.php?title=ワイン&diff=180213&oldid=132281>

としてください。こういった差分表示は、通常は、ページの「履歴」から表示させることができます。

また、ここでもページの ID 番号を使用していますので、IDを入れ替えたり、互いに異なるページの ID を入力すると奇妙なことになります。

例：https://ja.wikipedia.org/w/index.php?title=ワイン\&diff=132281\&oldid=180213

例2：https://ja.wikipedia.org/w/index.php?title=ワイン\&diff=555555\&oldid=132281

## 利用者の投稿記録

たとえば、利用者 Brion VIBBER の11番目～15番目の編集を見るには、以下のように書いてください。

<https://ja.wikipedia.org/w/index.php?title=特別:Contributions&limit=5&offset=10&target=Brion_VIBBER>

## ウォッチリスト

14.4分前（24時間の百分の一）からの更新を見るには、以下のように書いて下さい。

<https://ja.wikipedia.org/w/index.php?title=特別:Watchlist&days=0.01>

## 関連ページの更新状況

[ワイン](../Page/ワイン.md "wikilink")からリンクされているページの最近の更新を見るには、以下のように書いて下さい。

<https://ja.wikipedia.org/w/index.php?title=特別:Recentchangeslinked&target=ワイン&days=1000&limit=1000>

## リンク元

以下はどちらも同じです。

<https://ja.wikipedia.org/w/index.php?title=特別:Whatlinkshere/ワイン>

<https://ja.wikipedia.org/w/index.php?title=特別:Whatlinkshere&target=ワイン>

## 新規ページ

新しく作成されたページのうち、新しいもの501番目～505番目を表示するには、以下のように書いて下さい。

<https://ja.wikipedia.org/w/index.php?title=特別:Newpages&limit=5&offset=500>

## 利用者

登録利用者の501番目～600番目（アルファベット順。user-ID とはちがいます）を表示するには、以下のように書いて下さい。

<https://ja.wikipedia.org/w/index.php?title=特別:Listusers&limit=100&offset=500>

この機能を使えば、知りたい利用者名に近い名前のうち、どの利用者名が使用済みかを確かめるのに、最初から順に見ていく必要が無くなります。offset は、試行錯誤してください。

## デフォルトの制限値

何件表示するかの制限値を指定しなかった場合、

  - 最近更新されたページ、関連ページの更新状況、新規ページについては、オプションで指定した数になります（ログインしていない場合は、50）。
  - 編集履歴と利用者の投稿記録については、50です。

## 保護されたページのソースを見るには

保護されたページも含め、ページのソースを見るには、編集用の URL を使用してください。たとえば、[MediaWiki:Recentchanges](https://ja.wikipedia.org/wiki/MediaWiki:Recentchanges "wikilink") なら、以下のように書いて下さい。

<https://ja.wikipedia.org/w/index.php?title=Mediawiki:Recentchanges&action=edit>

## 関連項目

  - [Help:リンク](https://ja.wikipedia.org/wiki/Help:リンク "wikilink"): リンクを作るマークアップのヘルプ
  - [Help:固定リンク](https://ja.wikipedia.org/wiki/Help:固定リンク "wikilink")
  - [Help:キャッシュ破棄](https://ja.wikipedia.org/wiki/Help:キャッシュ破棄 "wikilink")