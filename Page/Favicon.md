> この記事は[Favicon](https://ja.wikipedia.org/wiki/Favicon)から翻訳されています。


[thumbの左側にある](https://ja.wikipedia.org/wiki/ファイル:Favicon.png "wikilink")、Wの画像がfaviconである。\]\] **favicon**（ファビコン）は、[ウェブサイト](../Page/ウェブサイト.md "wikilink")のシンボルマーク・イメージとして、ウェブサイト運営者がウェブサイトやウェブページに配置する[アイコン](../Page/アイコン.md "wikilink")の俗称である。favorite icon（フェイバリット・アイコン：お気に入りアイコン）という[英語](../Page/英語.md "wikilink")の語句を縮約した[かばん語](../Page/かばん語.md "wikilink")である。

## 概要

faviconのはじまりは、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")である[Microsoft Internet Explorer 5によってはじめて搭載された独自の](https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_5 "wikilink")（非HTML標準の）機能であった。ユーザーが任意のウェブサイトを[お気に入りに登録するときに](../Page/ブックマーク.md "wikilink")、ウェブブラウザは該当Webサイトのディレクトリから `favicon.ico` ファイルの存在を調べ、ある場合はこのファイルを該当Webサイトのアイコン画像として取り込む。それ以降にお気に入り一覧を表示する際、該当Webサイトについては一般的なWebアイコンではなく取り込んだアイコン画像が表示されるようになる。これにより、他のWebサイトのアイコンよりも目立たせ、ユーザーへイメージによる直観的な選択操作への便宜を図ることができる。

現在では多くのウェブブラウザが本機能を搭載している。アイコンファイルの配置場所を `link` タグにより任意に指定できるようになり、従来の[ICO形式以外に](https://ja.wikipedia.org/wiki/ICO_\(ファイルフォーマット\) "wikilink")[GIF形式や](../Page/Graphics_Interchange_Format.md "wikilink")[PNG形式もサポートされるウェブブラウザが増えたため広く利用されている](../Page/Portable_Network_Graphics.md "wikilink")。

当初はお気に入りに登録する際にはじめて参照されたファイルであることから、このファイルのアクセス回数を調べることでお気に入りへの登録状況を計測できた。現在の多くのウェブブラウザは、Webページアクセス時に（お気に入り登録操作の有無にかかわらず）faviconを参照するため、お気に入り登録状況の計測に、faviconファイルへのアクセスカウント利用はほぼ無意味となってしまっている。

## faviconの指定方法

### HTMLで指定する方法

HTML（旧来XHTMLと呼ばれていたXML構文のHTMLを含む）内でfaviconを指定するには、 `head` 要素の中で `link` 要素を次のように用いる。

``` html
<link rel="icon" href="https://example.com/favicon.ico" />
```

ファイル名の決まりは特にない。また、ファイル形式の決まりもなく、ウェブブラウザが認識する形式であればどのような形式を用いても良い。ただし、Internet Explorerは10以下ではICO形式しか認識しない。IE11ではPNG、GIF（アニメーション非対応）に対応した。

ウェブサーバ側ではアイコンの[MIMEタイプを正しく指定する必要がある](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")。なお、ICO形式では `image/vnd.microsoft.icon` である（`image/x-icon` が指定されている場合もあるが、[IANAに登録された標準的なMIMEタイプを用いることが望ましい](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")）。

### favicon.icoによる方法

ルートディレクトリに `favicon.ico` という名称のファイルを設置しておくと、HTML中で指定が無くともfaviconとして認識される\[1\]。

## 標準化問題

もともとfaviconはマイクロソフトによって提案され、Internet Explorerはあらゆるウェブサイトの指定URL (`favicon.ico`) にfaviconを要求する仕組みであった。その後、Microsoftは `link` 要素によりfaviconを呼び出す方法をサポートするようになったが、これは最初W3Cの勧告に従わない形式であり、次の点が問題とされた。

  - ICO形式にはIANAに登録されたMIMEタイプの割り当てがないため、多くのブラウザはfaviconとして指定されたファイルの種類を解析できない。
  - `rel` 属性の値を`shortcut icon`とする仕様であった。これは半角スペースを含むため、2つの属性値として解釈され、ウェブブラウザを混乱させる。
  - `favicon.ico`にアクセスする方式では、特定のURLパスをこの用途に占有することになり、World Wide Webのアーキテクチャにそぐわない。

しかし、2003年にICO形式が `image/vnd.microsoft.icon` としてIANAに登録されたことで最初の問題は解決した。さらに[Mozilla](../Page/Mozilla.md "wikilink")がブラウザでのサポートと同時に <link rel="icon" type="image/png" href="/path/image.png"> という形式を加え、`link` 要素によるfaviconの重複指定でウェブ製作者が画像形式を複数指定できるようになったため、書式の問題も実質上の解決となった。[Mozilla Suiteのfaviconサポートを契機に](../Page/Mozilla_Application_Suite.md "wikilink")、それ以後は多くのウェブブラウザがこの仕様を新たにサポートするようになっており、同様の書式で標準化されている。

## ブラウザでの対応状況

2007年現在、Internet Explorerをはじめとする主なブラウザがfaviconをサポートしているが、細部の挙動は各ブラウザによって異なる。アドレス欄やタブにアイコンが表示されてもブックマークリストに表示されないものもあれば、アドレス欄・ブックマークともに表示させるものも存在する。また、[IEコンポーネントブラウザ](../Page/IEコンポーネントブラウザ.md "wikilink")でfavicon処理機能は独自実装となるため、IEとは挙動が異なる。

favicon管理方法もブラウザによって異なるが、多くはfavicon専用のキャッシュを用いることで自動的に消えてしまうのを防いでいることが多い。

## 関連項目

  - [ICO (ファイルフォーマット)](https://ja.wikipedia.org/wiki/ICO_\(ファイルフォーマット\) "wikilink")
  - [X-Face](https://ja.wikipedia.org/wiki/X-Face "wikilink")

## 脚注

## 外部リンク

  - [Favicon Generator](https://99webtools.com/favicon-generator.php) - オンラインファビコンジェネレーター
  - [favicon.cc](https://www.favicon.cc/) - faviconのオンラインエディター

[Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink")

1.