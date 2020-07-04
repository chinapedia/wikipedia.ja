> この記事は[Tagged Image File Format](https://ja.wikipedia.org/wiki/Tagged_Image_File_Format)から翻訳されています。


**TIFF** （ティフ、**<span dir="ltr" lang="en">Tagged Image File Format</span>**）は、[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")の符号化形式の一種である。タグと呼ばれる識別子を使うことによって、様々な形式の[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")を柔軟に表現できる。

## 概要

TIFFフォーマットは、[1986年](../Page/1986年.md "wikilink")に[マイクロソフト](../Page/マイクロソフト.md "wikilink")および[<span dir="ltr" lang="en">Aldus</span>](https://ja.wikipedia.org/wiki/Aldus "wikilink")（1994年、アドビシステムズに合併）によって開発された画像データフォーマット。画像データを、解像度や色数、符号化方式が異なるものでも様々な形式で一つのファイルにまとめて格納できるため、アプリケーションソフトに依存することがあまり無いフォーマットであると言える。 何度かの改訂によって拡張が行われているが、その多くはタグの追加という形を取っており、過去に作られたデータとの互換性に配慮されている。主流となっているのはTIFF Revision 6.0（以下TIFF6.0）だが、後に発行された<span dir="ltr" lang="en">Adobe PageMaker 6.0 Technical Notes</span>および<span dir="ltr" lang="en">Adobe Photoshop Technical Notes</span>などにより若干の追加および変更がなされている。

かつて[<span dir="ltr" lang="en">FM TOWNS</span>](../Page/FM_TOWNS.md "wikilink")、[<span dir="ltr" lang="en">Macintosh</span>](../Page/Macintosh.md "wikilink")、[<span dir="ltr" lang="en">NeXT</span>でよく利用され](../Page/NeXT.md "wikilink")、[<span dir="ltr" lang="en">Windows</span>](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 3.0でDIB ([BMP](https://ja.wikipedia.org/wiki/Windowsビットマップ "wikilink")) が標準になるまでは<span dir="ltr" lang="en">Windows</span>でも標準の画像フォーマットの形式とされていた。白黒2値、[グレースケール](https://ja.wikipedia.org/wiki/グレースケール "wikilink")、および様々なカラー形式（RGB/CMYK）に対応している。しかしあまりにも自由度の高い表現が可能なので、完全な互換性を保つことが難しくなっている。 TIFFの規約もすべてのタグをサポートする必要はないと明記し、互換性の問題を低減するためのサブセットが提案されるが、必ずしもその基準は守られない。

TIFFでは、非圧縮、[LZW圧縮](../Page/Lempel–Ziv–Welch.md "wikilink")、[ZIP圧縮](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")、[連長圧縮](../Page/連長圧縮.md "wikilink")の一種である[<span dir="ltr" lang="en">PackBits</span>など様々な圧縮方法が使用可能である](https://ja.wikipedia.org/wiki/連長圧縮#PackBits "wikilink")。そのほとんどは[可逆圧縮](../Page/可逆圧縮.md "wikilink")法だが、TIFF6.0以降、[JPEG](../Page/JPEG.md "wikilink")圧縮もサポートされた。ファイルサイズを重視する用途では、白黒2値にはG4 (MMR) 圧縮、それ以外には[JPEG](../Page/JPEG.md "wikilink")圧縮やLZW圧縮が使われることが多い。また[DTP](../Page/DTP.md "wikilink")や印刷用途などでは非圧縮が使われることもある。LZW圧縮は、[GIFと同じく](../Page/Graphics_Interchange_Format.md "wikilink")[特許上の問題により自由に使えない時期があった](https://ja.wikipedia.org/wiki/GIF#特許問題とその顛末 "wikilink")（日本では2004年6月20日まで）。

ウェブブラウザでは[<span dir="ltr" lang="en">Internet Explorer</span>のバージョン](../Page/Internet_Explorer.md "wikilink")9からTIFFの表示に対応している。

TIFFは画像を編集する中間段階で用いることが下記のような理由で効果的である。

  - たいていの編集用ソフトはTIFFフォーマットに対応している
  - [JPEG](../Page/JPEG.md "wikilink")圧縮を使わない限り、保存を繰り返しても基本的に画質が劣化しない
  - 色に関する制約が非常に少ない（チャンネルあたりの色数として、1/2/4/8/10/12/14/16/32ビット[整数](../Page/整数.md "wikilink")や16/32/64ビット[浮動小数点数](../Page/浮動小数点数.md "wikilink")などもサポートしている）

## JPEG圧縮

TIFF6.0で導入された[JPEG](../Page/JPEG.md "wikilink")圧縮については、仕様上の不備が指摘されており、後に発行された<span dir="ltr" lang="en">Adobe Photoshop Technical Notes</span>によって大幅な変更が加えられた。この変更では、従来のTIFF6.0で[JPEG](../Page/JPEG.md "wikilink")圧縮のために定義されていた`Compression=6`および関連タグを廃止し、代わりに新しく`Compression=7`およびそれに関連するタグが導入されている。これによって様々な問題点がクリアされ実装も容易になったことから徐々にこの形式への移行が進んでいるが、互換性などの問題から従来の`Compression=6`も引き続き使われている。なお`Compression=6`ではタグの記述方法が難解なことなどから、TIFF6.0の仕様にさえも準拠せず独自の解釈で[エンコード](../Page/エンコード.md "wikilink")/[デコード](https://ja.wikipedia.org/wiki/デコード "wikilink")を行う[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")も少なくない。そのため、JPEG圧縮のTIFFファイルの中には著しく互換性の低いものがある。

## マルチページ

ひとつのファイルの中に複数の画像を格納した**マルチページファイル**を構成できるのもTIFFの特徴のひとつである。タグ情報はページごとに独立して管理されるため、ページごとに画像のサイズ、圧縮方法、カラー形式などを独立して決めることができる。ページ数自体に制限はないが、あまりにもページ数が多いとTIFFの理論的な上限サイズである4GBに達することがあるため注意が必要である。また[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")によっては2GBまでしかサポートしないものもあるため、2GBを実質的な上限サイズと考えた方がより安全である。

マルチページファイルは、各ページが持っている「次のページ」の先頭への[ポインタによって連結された](../Page/ポインタ_\(プログラミング\).md "wikilink")[線形リスト](https://ja.wikipedia.org/wiki/線形リスト "wikilink")として実現されている。ここでいうポインタとは、[ファイル先頭から数えた](../Page/ファイル_\(コンピュータ\).md "wikilink")[バイト数のことである](../Page/バイト_\(情報\).md "wikilink")。同様のポインタは、ファイル上の様々なデータの位置を表すためにも使われている。したがって、複数のTIFFファイルを単純に連結しただけではマルチページファイルにはならないし、逆にマルチページファイルの一部を単純に切り出しても正常なTIFFファイルにはならない。

## ファクシミリでの利用

TIFFフォーマットには、[ファクシミリ](https://ja.wikipedia.org/wiki/ファクシミリ "wikilink") (FAX) のデータを表現するために、TIFF-Fと呼ばれるプロファイルが RFC 2306 (<span dir="ltr" lang="en">Tag Image File Format (TIFF) - F Profile for Facsimile</span>) で定義されている。FAX送受信の際に用いる圧縮形式であるMH、MR、MMRなどの符号化方式に対応しているため、送受信データとの間では最小限の変換処理を行うだけでファイル化できる。また、前述したマルチページファイルの機能を利用して、複数ページを1ファイルで表現できるほか、他の多くのイメージファイル形式では表現が困難な、ピクセル縦横比の異なる画像を表現できることなどが利点として挙げられる。

[<span dir="ltr" lang="en">InternetFAX</span>規格のひとつである](../Page/InternetFAX.md "wikilink") [T.37](https://ja.wikipedia.org/wiki/T.37 "wikilink")では、送受信ファイル形式として TIFF-Fを使用することが明示されており、Windows FAX サービスや、その他の T.37ゲートウェイ装置は、TIFFファイルの添付された電子メールメッセージとして受信FAXを転送する。

いっぽう、クラウド利用型のファクシミリ・サービスでは対応が分かれている。日本のNTT東西地域会社が提供する「FAXお知らせメール」サービス\[1\]ではお知らせメールへのファクシミリ・データ添付は行われず、内容を確認するにはブラウザでログインしてTIFFファイルをダウンロードし、TIFFファイルの表示に対応したビューワアプリを利用して閲覧する方式となっている。[eFax](https://ja.wikipedia.org/wiki/eFax "wikilink")ではTIFFではなく、PDFファイルを添付したメールとしてFAXを転送する\[2\]。NTT東日本の提供する「ひかりFAX」アプリ（公開終了\[3\]）では、受信内容をページ毎に分かれた複数の[JPEG](../Page/JPEG.md "wikilink")ファイルに変換して端末内に保存する。

## 脚注

**注釈**  **出典**

**参考文献**

## 関連項目

  - [DNG](../Page/Digital_Negative.md "wikilink")
  - [JPEG XR](https://ja.wikipedia.org/wiki/JPEG_XR "wikilink")([HD Photo](../Page/HD_Photo.md "wikilink"))
  - [文書管理システム](../Page/文書管理システム.md "wikilink")

## 外部リンク

  - [TIFF仕様書など](http://partners.adobe.com/public/developer/tiff/index.html)
  - [Broadband Watch--BBっとWORDS 「TIFFの特徴」](http://bb.watch.impress.co.jp/cda/bbword/15780.html)

[Category:ラスターグラフィックス・ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ラスターグラフィックス・ファイルフォーマット "wikilink") [Category:メタデータ](https://ja.wikipedia.org/wiki/Category:メタデータ "wikilink")

1.  [ひかり電話 FAXお知らせメール](https://flets.com/hikaridenwa/service/fax.html)
2.  [eFax](https://www.efax.co.jp)
3.