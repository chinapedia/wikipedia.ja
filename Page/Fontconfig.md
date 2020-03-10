> この記事は[Fontconfig](https://ja.wikipedia.org/wiki/Fontconfig)から翻訳されています。


**Fontconfig**（または **fontconfig**）は、システム全体の[フォント](../Page/フォント.md "wikilink")の設定（代替フォントの設定、フォント置換の設定、レンダリングの設定、など）に関する情報をアプリケーションに提供するためのライブラリである。fontconfigは、元は[キース・パッカード](https://ja.wikipedia.org/wiki/キース・パッカード "wikilink")によって作られ、現在は Behdad Esfahbod によってメンテナンスされている。

fontconfigは、[permissive free software licence](https://ja.wikipedia.org/wiki/permissive_free_software_licence "wikilink") のもとで配布されている[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である\[1\]。

fontconfigは、典型的には、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")および他のUnixライクなシステムのデスクトップ環境で使われており、フォントの扱いにおいて重要な役割を果している。

## 利用

[エンドユーザー](https://ja.wikipedia.org/wiki/エンドユーザー "wikilink")は、fontconfigを使ってシステムのフォント設定をカスタマイズできる。

アプリケーションは、以下の2つの方法で fontconfig を利用できる：

1.  システム上で利用できるフォントを問い合わせる
2.  指定したパラメータ（*パターン*）にできるだけ近い（よく似た）フォントを問い合わせる

フォントのマッチングを行なうために、fontconfig はインストールされているすべてのフォントについての情報を保存する。例えば、[フォントファミリー](../Page/書体.md "wikilink")、スタイル、太さ、[dpi](https://ja.wikipedia.org/wiki/dpi "wikilink")、[Unicode](../Page/Unicode.md "wikilink")の対応範囲などの情報である。この情報は[フォント置換](https://ja.wikipedia.org/wiki/フォント置換 "wikilink")を行うためにも使われる。

## 設定

fontconfigでは、[XMLフォーマットを使って設定ファイルを記述する](../Page/Extensible_Markup_Language.md "wikilink")。fontconfigファイル用の[DTDは](../Page/Document_Type_Definition.md "wikilink")、通常`/etc/fonts/fonts.dtd`に置かれている。

マスター設定ファイルは通常 `/etc/fonts/fonts.conf` である。これに加えて、以下に示す他のいくつかの設定ファイルも（存在すれば）参照される。

  - `/etc/fonts/local.conf`
  - `/etc/fonts/conf.d/*.conf`
  - `$XDG_CONFIG_HOME/fontconfig/fonts.conf`
  - `$XDG_CONFIG_HOME/fontconfig/conf.d/*.conf`
  - `~/.fonts.conf （将来のバージョンで廃止される予定）`

設定ファイルの簡単な例：

``` xml
<?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "fonts.dtd">
<fontconfig>
    <!-- すべてのフォントに対してアンチエイリアスを有効にする -->
    <match target="font">
        <edit mode="assign" name="antialias"><bool>true</bool></edit>
    </match>
</fontconfig>
```

詳細については [fontconfig マニュアル](http://fontconfig.org/fontconfig-user.html)に記載されている。

## ユーティリティ

fontconfig には、フォント設定を管理する8つのコマンドラインユーティリティが付属している：

  - *fc-list*: fontconfigが把握しているすべてのフォントまたはパターンにマッチするすべてのフォントの一覧を表示する。
  - *fc-match*: fontconfigのマッチングルールに従ってフォントパターン（デフォルトで空のパターン）のマッチングを行い、利用可能なフォントのうち最も適切なものを見つける。
  - *fc-cache*: 指定されたディレクトリまたは設定ファイルで指定されたすべてのディレクトリから、[FreeType](../Page/FreeType.md "wikilink")が扱えるすべてのフォントの[キャッシュを作成する](https://ja.wikipedia.org/wiki/キャッシュ_\(コンピュータシステム\) "wikilink")。
  - *fc-cat*: キャッシュファイルまたはフォントディレクトリからフォント情報を読み込み、それを[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink") 形式で出力する。
  - *fc-query*: フォントファイルについて問い合わせ、結果を表示する。
  - *fc-scan*: フォントファイルまたはディレクトリをスキャンし、結果を表示する。
  - *fc-pattern*: 指定したパターンに最も近いフォントを表示する。
  - *fc-validate*: フォントファイルを検証し、結果を表示する。

Fontconfigは、[FreeType](../Page/FreeType.md "wikilink")（フォントレンダラ）および （XMLパーサライブラリ）という、二つの[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")に依存している。

[Fontmatrix](https://ja.wikipedia.org/wiki/Fontmatrix "wikilink") は、グラフィカルユーザインタフェイスで fontconfig を使ってシステム上でフォントを表示したり、選択したり、管理するのに役立つ。

## バージョン番号の付け方

最後の番号が90以上のときはプレリリースバージョンを示す、というバージョンの付け方をしている。

## 外部リンク

  - [fontconfig 公式サイト](http://fontconfig.org/)

  -
## 脚注

[Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

1.