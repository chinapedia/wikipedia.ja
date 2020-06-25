> この記事は[Deno](https://ja.wikipedia.org/wiki/Deno)から翻訳されています。


**Deno**は、[V8](https://ja.wikipedia.org/wiki/V8_\(JavaScriptエンジン\) "wikilink") [JavaScriptエンジン](https://ja.wikipedia.org/wiki/JavaScriptエンジン "wikilink")及び[Rust](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")に基づいた、[JavaScript](../Page/JavaScript.md "wikilink")及び[TypeScript](https://ja.wikipedia.org/wiki/TypeScript "wikilink")の[ランタイム環境である](https://ja.wikipedia.org/wiki/ランタイムシステム "wikilink")。[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")の作者である[ライアン・ダール](https://ja.wikipedia.org/wiki/ライアン・ダール "wikilink")によって作成され、セキュリティと生産性に焦点を当てている\[1\]。ライアン・ダールが2018年に行った講演「Node.jsに関する10の反省点」で発表された\[2\]。Denoは単一の[実行ファイル](../Page/実行ファイル.md "wikilink")内でランタイム環境と[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")の両方の役割を明示的に引き受けるので、別途パッケージ管理システムを必要としない\[3\]\[4\]。

## 歴史

DenoはJSConf EU 2018でのライアン・ダールによる講演「Node.jsに関する10の反省点」で発表された\[5\]。ライアン・ダールはこの講演において、後悔しているNode.jsの初期設計での決定について言及し、[APIの設計で](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[promiseを使用しないという選択をしたこと](../Page/Future_パターン.md "wikilink")、古い[GYPビルドシステムを使用するようにしたこと](https://ja.wikipedia.org/wiki/GYP_\(ソフトウェア\) "wikilink")、`node_modules`と`package.json`の採用、[拡張子](../Page/拡張子.md "wikilink")を除外したこと、`index.js`による魔法のようなモジュールの依存関係の解決、V8の[サンドボックス環境の破壊を挙げている](../Page/サンドボックス_\(セキュリティ\).md "wikilink")\[6\]。最終的に、彼はDenoのプロトタイプ版を発表し、[Protocol Buffersのような](https://ja.wikipedia.org/wiki/Protocol_Buffers "wikilink")[シリアライズ](../Page/シリアライズ.md "wikilink")ツールを使用したメッセージの受け渡しを通じて[システムコール](../Page/システムコール.md "wikilink")[バインディングを実現し](../Page/束縛_\(情報工学\).md "wikilink")、[アクセス制御](../Page/アクセス制御.md "wikilink")用のコマンドラインフラグを提供することを目指した。

Denoは当初は[Goで実装され](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")、特権側 (Goとシステムコールアクセス) と非特権側 (V8) の間のシリアライズにProtocol Buffersを使用していた\[7\]。しかしながら、実行時間が2倍になることと[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")の圧力から、コードは直ぐにRustで再実装された\[8\]。非同期イベント駆動型プラットフォームとしてに代わってが導入され、より高速な「ゼロ・コピー」シリアライゼーション及びデシリアライゼーションのためにが導入された\[9\]が、2019年4月にシリアライゼーションの大幅なオーバーヘッドを測定したベンチマークが公開されたことによって\[10\]、FlatBuffersは同年8月の後半に削除された\[11\]。

Goの標準ライブラリをモデルとしたDenoの標準ライブラリは、広範なツール及びユーティリティを提供するために2018年11月に作成され、Node.jsの依存関係での爆発問題を部分的に解決した\[12\]。

## 概要

Denoは現代の[プログラマ](../Page/プログラマ.md "wikilink")のための生産的で安全な[スクリプト環境を目指している](../Page/スクリプト言語.md "wikilink")\[13\]。Node.jsと同様に、Denoはに重点を置いており、[非ブロッキングコアIOユーティリティのセットとそのブロッキング版を提供している](https://ja.wikipedia.org/wiki/非同期IO "wikilink")。Denoは[Webサーバ](../Page/Webサーバ.md "wikilink")の作成や科学計算に利用することができる。

### Node.jsとの比較

DenoとNode.jsは[Google Chromeなどの](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")[Chromium](https://ja.wikipedia.org/wiki/Chromium "wikilink")ベースの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")で採用されているV8 JavaScriptエンジン上に構築されたランタイム環境である。どちらも内部[イベントループ](../Page/イベントループ.md "wikilink")があり、スクリプトと広範なコマンドラインユーティリティを実行するための[コマンドラインインタフェース](https://ja.wikipedia.org/wiki/コマンドラインインタフェース "wikilink")を提供している。

DenoがNode.jsと異なる主な点は以下の通りである\[14\]:

1.  [CommonJS](https://ja.wikipedia.org/wiki/CommonJS "wikilink")の代わりに、ES Moduleをデフォルトのモジュールとシステムとして使用する。
2.  ウェブブラウザと同様に、依存関係 (ローカル及びリモート) を読み込むために[URL](https://ja.wikipedia.org/wiki/URL "wikilink")を使用する。
3.  リソースを取得するためのパッケージ管理システムが組み込まれているので、[npmは不要である](https://ja.wikipedia.org/wiki/npm_\(パッケージ管理ツール\) "wikilink")。
4.  キャッシングメカニズムを備えたスナップショットTypeScript[コンパイラ](../Page/コンパイラ.md "wikilink")を使用することによるTypeScriptのサポート。
5.  幅広いWeb APIを実装することによるウェブブラウザとの互換性の向上。
6.  サンドボックスコードを実行するために、[ファイルシステム](../Page/ファイルシステム.md "wikilink")とネットワークアクセスを制御することができる。
7.  promise、[ES6及びTypeScriptの機能を利用するためにAPIを再設計したこと](../Page/ECMAScript.md "wikilink")。
8.  コアAPIのサイズを最小限にしながら、外部に依存関係の無い大きな標準ライブラリを提供すること。
9.  特権システムAPIを呼び出しとバインディングの使用のために、メッセージ受け渡しチャネルを使用すること。

## 例

以下は、読み取り / 書き込み / ネットワーク権限無しの基本的なDenoスクリプトの実行例である (サンドボックスモード):

``` bash
deno run main.ts
```

権限を許可する場合は、明示的に対応するフラグを指定する必要が有る:

``` bash
deno run --allow-read --allow-net main.ts
```

スクリプトの依存関係を検査する場合は、`info`サブコマンドを使用する:

``` bash
deno info main.ts
```

Denoでの基本的な[Hello worldは以下の通りである](../Page/Hello_world.md "wikilink") (Node.jsと同様):

``` ts
console.log("Hello world");
```

Denoはウェブブラウザでは使用できない殆どのDeno固有のAPIにグローバル名前空間を提供する。[UNIX](../Page/UNIX.md "wikilink")の[`cat`](https://ja.wikipedia.org/wiki/cat_\(UNIX\) "wikilink")コマンドは、以下のように実装することができる:

``` ts
/* cat.ts */

/* Deno APIs are exposed through the `Deno` namespace. */
const { stdout, open, copy, args } = Deno;

// Top-level await is supported
for (let i = 1; i < args.length; i++) {
    const filename = args[i]; // Obtains command-line arguments.
    const file = await open(filename); // Opens the corresponding file for reading.
    await copy(stdout, file); // Performs a zero-copy asynchronous copy from `file` to `stdout`.
}
```

上記の`Deno.copy`関数は、Goの`io.Copy`関数のように機能する。`stdout` ([標準出力](https://ja.wikipedia.org/wiki/標準出力 "wikilink")) は`Writer`に出力され、`file`の入力は`Reader`である。このプログラムを実行するには、ファイルシステムの読み取り許可が必要である:

``` bash
deno run --allow-read cat.ts myfile
```

以下はDenoによる基本的なHTTPサーバの実装である:

``` ts
// Imports `serve` from the remote Deno standard library, using URL.
import { serve } from "https://deno.land/std@v0.21.0/http/server.ts";

const body = new TextEncoder().encode("Hello World\n");
// `serve` function returns an asynchronous iterator, yielding a stream of requests
for await (const req of serve(":8000")) {
    req.respond({ body });
}
```

上記のスクリプトを実行すると、Denoはリモートの標準ライブラリファイルを自動的にダウンロードしてキャッシュし、コードをコンパイルする。同様に、URLを入力ファイル名として指定することで、明示的にダウンロードせずに標準ライブラリスクリプト ([ファイルサーバ](../Page/ファイルサーバ.md "wikilink")など) を直接実行することができる (`-A`は全ての権限を有効にするフラグである):

``` console
$ deno run -A https://deno.land/std/http/file_server.ts
Download https://deno.land/std/http/file_server.ts
Compile https://deno.land/std/http/file_server.ts
...
HTTP server listening on http://0.0.0.0:4500/
```

## 脚注

## 関連項目

  - [Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")

## 外部リンク

  -
  -
[Category:JavaScript](https://ja.wikipedia.org/wiki/Category:JavaScript "wikilink") [Category:ランタイムシステム](https://ja.wikipedia.org/wiki/Category:ランタイムシステム "wikilink") [Category:パッケージ管理システム](https://ja.wikipedia.org/wiki/Category:パッケージ管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

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