> この記事は[Ubuntu-restricted-extras](https://ja.wikipedia.org/wiki/Ubuntu-restricted-extras)から翻訳されています。


**Ubuntu Restricted Extras**は、コンピューターの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") [Ubuntu](../Page/Ubuntu.md "wikilink")用の[ソフトウェアパッケージ](../Page/パッケージ管理システム.md "wikilink")。ユーザーは、法的または著作権上の理由で含まれていない重要なソフトウェアをインストールされている。

以下、インストールするメタパッケージ。

  - [MP3](../Page/MP3.md "wikilink")および暗号化されていない[DVD再生のサポート](../Page/DVD-Video.md "wikilink")
  - [Microsoft TrueTypeコアフォント](../Page/コアフォント.md "wikilink")
  - Adobe Flashプラグイン
  - 一般的なオーディオおよびビデオファイルの[コーデック](../Page/コーデック.md "wikilink")

## 背景

Ubuntuのメンテナーは、すぐに[使えるインストールに完全に](../Page/フリーソフトウェア.md "wikilink")[無料のソフトウェアのみを含めたいため](../Page/フリーソフトウェア.md "wikilink")、このパッケージのソフトウェアはデフォルトではUbuntuに含まれていない。このパッケージに含まれる[ソフトウェアは](../Page/ソフトウェア特許.md "wikilink") 、 [ソースが](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[クローズドであるか](../Page/プロプライエタリ・ソフトウェア.md "wikilink")、[ソフトウェアの特許により妨げられているか](../Page/ソフトウェア特許.md "wikilink")、または制限されている可能性がある。たとえば、Adobe Flashプラグインはクローズドソースのソフトウェア。さらに、 [MP3](../Page/MP3.md "wikilink")や[H.264](../Page/H.264.md "wikilink")などの多くのマルチメディア形式が特許を取得。これらの特許が適用される国では、これらの形式を使用するソフトウェアを合法的に配布するには、特許所有者にライセンス料を支払う必要がある\[1\]。  



## 内容

Ubuntu Restricted Extrasはメタパッケージであり、次の依存関係がある： \[2\]

  - flashplugin-installer
  - gstreamer0.10-ffmpeg
  - gstreamer0.10-fluendo-mp3
  - gstreamer0.10-pitfdll
  - gstreamer0.10-plugins-bad
  - gstreamer0.10-plugins-ugly
  - gstreamer0.10-plugins-bad-multiverse
  - gstreamer0.10-plugins-ugly-multiverse
  - icedtea6-plugin
  - libavcodec-extra-52
  - libmp4v2-0
  - ttf-mscorefonts-installer
  - アンロール

Ubuntu 10.10以降、これらの依存関係のいくつかは、デフォルトで含まれている別のメタパッケージ*ubuntu-restricted-addons*を介して間接的に含まれている。

## 包含物

Ubuntu Restricted Extrasに含まれるソフトウェアの法的ステータスにより、パッケージはデフォルトではUbuntu CDに含まれてない\[3\]。 しかし、このような超OS、などいくつかのディストリビューション、 Pinguy OSとRevamplinuxは 、インストールCDまたはDVDのパッケージをバンドル。  <sup>\[ *[<span title="This claim needs references to reliable sources. (January 2017)">引用が必要</span>](https://ja.wikipedia.org/wiki/Wikipedia:「要出典」をクリックされた方へ "wikilink")* \]</sup>

## 関連項目

  - [deb形式](https://ja.wikipedia.org/wiki/Deb_\(ファイルフォーマット\) "wikilink")

## 脚注

[Category:Ubuntu](https://ja.wikipedia.org/wiki/Category:Ubuntu "wikilink")

1.
2.  [Package: ubuntu-restricted-extras in Maverick Meerkat](http://packages.ubuntu.com/maverick/ubuntu-restricted-extras)
3.  [Ubuntu repositories and ISO inclusion](https://help.ubuntu.com/community/Repositories/Ubuntu)