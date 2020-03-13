> この記事は[Web \(\)](https://ja.wikipedia.org/wiki/Web_\(\))から翻訳されています。


**Web**（ウェブ、旧名**Epiphany** (エピファニー)）は、[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")に[WebKit](../Page/WebKit.md "wikilink")を使った[GNOME](../Page/GNOME.md "wikilink")の標準[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")。シンプルで使いやすいことを念頭に設計されている。[ツールキットに](../Page/ウィジェット・ツールキット.md "wikilink")[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")3を使いGNOMEとよく統合されている。

トピック毎に整理する高機能なブックマークを搭載している。一つのページを複数のトピックに関連付けることが可能である。

Epiphany 2.26.3まで[Gecko](../Page/Gecko.md "wikilink")をサポートしていたが、これ以降のリリースは[WebKit](../Page/WebKit.md "wikilink")エンジンのみをサポートする\[1\]。

また、2.28以降pythonによる拡張はなくなり、[Seed](https://ja.wikipedia.org/wiki/Seed "wikilink")による拡張がサポートされた。

## 沿革

現在はGNOME最新版の正式公開に間に合うようにリリースされつづけている。 2.14以降は公開時のGNOMEとEpiphanyのバージョンは同一。

  - [2003年](../Page/2003年.md "wikilink")[9月8日](../Page/9月8日.md "wikilink") - Epiphany 1.0 リリース
  - [2004年](../Page/2004年.md "wikilink")[3月15日](../Page/3月15日.md "wikilink") - Epiphany 1.2 リリース
  - 2004年[9月14日](../Page/9月14日.md "wikilink") - Epiphany 1.4 リリース
  - [2005年](../Page/2005年.md "wikilink")[3月9日](../Page/3月9日.md "wikilink") - Epiphany 1.6 リリース
  - 2005年[9月15日](../Page/9月15日.md "wikilink") - Epiphany 1.8 リリース
  - [2006年](../Page/2006年.md "wikilink")[3月12日](../Page/3月12日.md "wikilink") - Epiphany 2.14 リリース。このバージョン系統からGNOME本家にメジャーバージョンナンバーが合わせられる。
  - 2006年[9月3日](https://ja.wikipedia.org/wiki/9月3日 "wikilink") - Epiphany 2.16 リリース
  - [2007年](../Page/2007年.md "wikilink")[3月14日](https://ja.wikipedia.org/wiki/3月14日 "wikilink") - Epiphany 2.18 リリース
  - 2007年[9月19日](../Page/9月19日.md "wikilink") - Epiphany 2.20 リリース。このバージョン系統から[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")が[WebKit](../Page/WebKit.md "wikilink")へ移行開始。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")3月12日 - Epiphany 2.22 リリース
  - 2008年[9月24日](../Page/9月24日.md "wikilink") - Epiphany 2.24 リリース
  - [2009年](../Page/2009年.md "wikilink")[3月31日](../Page/3月31日.md "wikilink") - Epiphany 2.26 リリース。このバージョン系統がGeckoサポートの最終版となった。
  - 2009年9月24日 - Epiphany 2.28 リリース
  - [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")3月31日 - Epiphany 2.30 リリース
  - 2010年[9月29日](../Page/9月29日.md "wikilink") - Epiphany 2.32 リリース
  - [2011年](../Page/2011年.md "wikilink")[4月6日](../Page/4月6日.md "wikilink") - Epiphany 3.0 リリース。このバージョン系統からGNOME本家共々GTK+3及びGNOME3系統へ移行。
  - 2011年[9月28日](../Page/9月28日.md "wikilink") - Epiphany 3.2 リリース
  - [2012年](../Page/2012年.md "wikilink")[3月28日](../Page/3月28日.md "wikilink") - Web 3.4 リリース。このバージョン系統からWebに名称変更。

### Galeonのフォーク

[2002年](../Page/2002年.md "wikilink")、[Galeon](../Page/Galeon.md "wikilink")の当初の開発者であるMarco Pesenti Grittiは、EpiphanyをGaleonのフォークとして開発した。このフォークは、Grittiと残りのGaleon開発者の間で新機能に関して意見の不一致があったため生じた。

同じ頃、[GNOMEプロジェクト](../Page/GNOMEプロジェクト.md "wikilink")は、ヒューマン・インターフェース・ガイドラインを適用したが、これはユーザインタフェースの単純化を促進するものであった。Galeonはパワーユーザ指向であったので、多くの開発者はこれを認めなかった。結果として、GrittiはGaleonベースの新たなブラウザを作り、重要でない多くの特徴は除去された。彼はEpiphanyをGNOME HIGに従うように意図した。Epiphanyはその開発開始時からGNOMEのテーマとその他の設定を用いている\[2\]\[3\]。

### Geckoベース

Epiphanyの最初のバージョンは、[2002年](../Page/2002年.md "wikilink")[12月24日](../Page/12月24日.md "wikilink")にリリースされた\[4\]。

Epiphanyは当初、Webページの表示に[Mozilla](../Page/Mozilla.md "wikilink")プロジェクトの[Gecko](../Page/Gecko.md "wikilink")レイアウトエンジンを使っていた。Mozillaのクロスプラットフォームなインターフェースの代わりに、GNOMEの[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")が提供された\[5\]。

### WebKitベース

開発課程で、Geckoバックエンドに関連した大きな問題に直面した\[6\]。これに対処するため、Epiphanyチームは[Webkit](https://ja.wikipedia.org/wiki/Webkit "wikilink")をもうひとつのレンダリングエンジンとしてサポートを加えた\[7\]。[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[4月1日](../Page/4月1日.md "wikilink")には、Geckoを使ってビルドする機能は除去され、WebKitのみを使うことを進める旨の宣言がチームによってなされた\[8\]。

[2009年](../Page/2009年.md "wikilink")9月、GNOME 2.28の一部として、WebKitへの移行は完了した\[9\]。

## 参照

## 外部リンク

  - [Epiphany](http://www.gnome.org/projects/epiphany/)
  - [Epiphany blog](http://blogs.gnome.org/epiphany/)

[Category:Geckoを用いたウェブブラウザ](https://ja.wikipedia.org/wiki/Category:Geckoを用いたウェブブラウザ "wikilink") [Category:WebKitを用いたウェブブラウザ](https://ja.wikipedia.org/wiki/Category:WebKitを用いたウェブブラウザ "wikilink") [Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink") [Category:GTK+を使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:GTK+を使用するソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:2002年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2002年のソフトウェア "wikilink")

1.  [Epiphany » Blog Archive » Gecko end-of-life](http://blogs.gnome.org/epiphany/2009/07/01/gecko-end-of-life/)
2.
3.
4.
5.
6.
7.
8.
9.