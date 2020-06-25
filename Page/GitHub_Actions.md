> この記事は[GitHub Actions](https://ja.wikipedia.org/wiki/GitHub_Actions)から翻訳されています。


**GitHub Actions**は、[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")が提供する[CI](https://ja.wikipedia.org/wiki/継続的インテグレーション "wikilink")/[CDサービスである](../Page/継続的デリバリー.md "wikilink")。

[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")と高度に統合されており、GitHubに公開されたコードを自動でビルド・テスト・デプロイを行うのが主目的である。

## 設定

リポジトリの `.github/workws`以下に[YAML](../Page/YAML.md "wikilink")形式の設定ファイルを記述することで設定を行う。

設定はワークフローとアクションという単位で行われる。

### ワークフロー

設定ファイルの基本単位。イベントが起きたときに実行する処理を記述しておく。

### アクション

再利用可能な設定ファイルの単位。アクションだけを定義したリポジトリを読み込むことで複数のリポジトリから利用したり、ワークフローの存在するリポジトリに置くことでそのリポジトリにある複数のワークフローから利用することができる。

GitHubから公式で[Ruby](../Page/Ruby.md "wikilink")や[Go言語などの環境構築をするためのアクションが用意されている](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")\[1\]。

## 脚注

<references />

## 外部リンク

  - [Actions | GitHub](https://github.co.jp/features/actions)
  - [Features・GitHub Actions・GitHub](https://github.com/features/actions)

[Category:コンピュータ](https://ja.wikipedia.org/wiki/Category:コンピュータ "wikilink") [Category:継続的インテグレーション](https://ja.wikipedia.org/wiki/Category:継続的インテグレーション "wikilink")

1.