> この記事は[BD-J](https://ja.wikipedia.org/wiki/BD-J)から翻訳されています。


**BD-J**（**Blu-ray Disc Java**）とは、[Blu-ray Disc](../Page/Blu-ray_Disc.md "wikilink")（[BDビデオ](../Page/BDMV.md "wikilink")）における対話型のコンテンツのための基盤である。BD-J を使った Blu-ray Disc での特典コンテンツは[DVD-Video](../Page/DVD-Video.md "wikilink")におけるものよりずっと洗練されており、ネットワークアクセスをしたり（最新の[予告編](../Page/予告編.md "wikilink")をダウンロードしたり、撮影現場の映像を見せたり）、ピクチャインピクチャ機能やローカルな[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")にアクセスしたりできる。BD-J は Blu-ray Disc Association が開発した。ビデオコンテンツをサポートする Blu-ray Disc プレーヤーは BD-J をサポートすることが義務付けられている。ただし、初期のプレーヤーには[インターネット](../Page/インターネット.md "wikilink")アクセスやストレージアクセス、ピクチャインピクチャといった機能はサポートされていなかった。（インターネットアクセスを除いた）これらの機能を "Bonus View" と呼び、インターネットアクセスを含めたものを "BD Live" と呼ぶ。2007年10月31日以降、新規に発売されるプレーヤーには "Bonus View" の搭載が義務付けられているが、機種によっては[ファームウェア](../Page/ファームウェア.md "wikilink")の更新が必要なものもある\[1\]。"BD Live" は現在もオプション機能である。

## 技術

BD-J は、Globally Executable [MHP](../Page/Multimedia_Home_Platform.md "wikilink")（GEM）のパッケージ化メディア[プロファイルに基づいている](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")。GEM は[デジタルテレビ](https://ja.wikipedia.org/wiki/デジタルテレビ "wikilink")のアプリケーション標準であり、汎用的な放送用プロファイルとして [Multimedia Home Platform](../Page/Multimedia_Home_Platform.md "wikilink")（DVB-MHP）、北米のケーブルテレビ向けプロファイルとして OpenCable Application Platform（OCAP）、アメリカでの放送向けとして Advanced Common Application Platform（ACAP）がある。GEM は[ETSIの標準であり](../Page/欧州電気通信標準化機構.md "wikilink")、DVB-MHP は[DVBの標準である](../Page/デジタルビデオブロードキャスティング.md "wikilink")。GEM ベースの標準はすべて[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の [Java](https://ja.wikipedia.org/wiki/Java "wikilink") 技術に基づいている。BD-J、MHP、OCAP、ACAP はすべて Java ベースであるため、コンテンツの相互運用性が非常に高い。

## コンテンツ開発

コンテンツ制作には様々な形式が可能である。[NetBeans](../Page/NetBeans.md "wikilink")や[Eclipseのような](../Page/Eclipse_\(統合開発環境\).md "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink")を使った開発もあれば、プログラミングしないグラフィカルな環境（Macromedia Director のようなもの）を使ったり、HTML/XML/SVG といったデータ形式を解釈する[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")を使う方法も考えられる。プログラミング環境全体を Blu-ray Disc プレーヤーに搭載すれば、これまでにない先進的なコンテンツが生まれる可能性を秘めている。その場合、標準の BD-J のインタフェースだけでなく、Java の既存のライブラリやアプリケーションフレームワークを利用することもできる（BD-J は Java バージョン1.3 ベース）。

## サンプルコード

    import javax.tv.xlet.*;

    public class BasicXlet implements Xlet {
      public BasicXlet () {}
      public void initXlet (XletContext context) throws XletStateChangeException {}
      public void startXlet () throws XletStateChangeException {}
      public void pauseXlet () {}
      public void destroyXlet (boolean unconditional) throws XletStateChangeException {}
    }

## BD-J を使っているタイトル

以下は完全な一覧ではない。

  - [カーズ](../Page/カーズ_\(映画\).md "wikilink")
  - [レミーのおいしいレストラン](https://ja.wikipedia.org/wiki/レミーのおいしいレストラン "wikilink")
  - [スパイダーマンTMトリロジーBOX](../Page/スパイダーマン_\(映画\).md "wikilink")
  - [ビッグ・フィッシュ](../Page/ビッグ・フィッシュ.md "wikilink")
  - [ファンタスティック・フォー:銀河の危機](../Page/ファンタスティック・フォー:銀河の危機.md "wikilink")
  - [デイ・アフター・トゥモロー](../Page/デイ・アフター・トゥモロー.md "wikilink")
  - [エネミー・ライン](../Page/エネミー・ライン.md "wikilink")
  - [リーグ・オブ・レジェンド/時空を超えた戦い](https://ja.wikipedia.org/wiki/リーグ・オブ・レジェンド/時空を超えた戦い "wikilink")
  - [スピード](../Page/スピード_\(映画\).md "wikilink")
  - [守護神](../Page/守護神_\(映画\).md "wikilink")
  - [チキン・リトル](../Page/チキン・リトル.md "wikilink")
  - [パイレーツ・オブ・カリビアン/呪われた海賊たち](https://ja.wikipedia.org/wiki/パイレーツ・オブ・カリビアン/呪われた海賊たち "wikilink")
  - [パイレーツ・オブ・カリビアン/デッドマンズ・チェスト](https://ja.wikipedia.org/wiki/パイレーツ・オブ・カリビアン/デッドマンズ・チェスト "wikilink")
  - [GHOST IN THE SHELL / 攻殻機動隊](https://ja.wikipedia.org/wiki/GHOST_IN_THE_SHELL_/_攻殻機動隊 "wikilink")
  - [サマーウォーズ](https://ja.wikipedia.org/wiki/サマーウォーズ "wikilink")

## 脚注

## 関連項目

  - [CD-i](../Page/CD-i.md "wikilink")
  - [DVDプレイヤーズゲーム](https://ja.wikipedia.org/wiki/DVDプレイヤーズゲーム "wikilink")
  - [Blu-ray Disc](../Page/Blu-ray_Disc.md "wikilink")
  - [HDi](../Page/HDi.md "wikilink") - [HD DVD](../Page/HD_DVD.md "wikilink") における BD-J 対抗技術
  - [BDプレイヤーズゲーム（BD-PG）](https://ja.wikipedia.org/wiki/DVDプレイヤーズゲーム "wikilink")

## 外部リンク

  - [Blu-ray Disc Association](http://www.blu-raydisc.com/) - 公式サイト
  - [Official MHP website](http://www.mhp.org/) [DVB](../Page/デジタルビデオブロードキャスティング.md "wikilink") Project Office.
      - [GEM specification](http://www.mhp.org/mhp_technology/gem/)
  - [MHP tutorials](http://www.mhp-interactive.org/)
  - [MHP Knowledge Database](http://www.mhp-knowledgebase.org)
  - [OpenMHP](http://www.openmhp.org/) - MHP-オープンソースプロジェクト
  - [Sun Microsystems' Java Micro Edition](http://java.sun.com/javame/index.jsp)
  - [Java TV API](http://java.sun.com/products/javatv/)
  - [xleTView](http://xletview.sourceforge.net/) - MHP-オープンソースエミュレータ（Sourceforge）
  - [Interactive-TV-Web](http://www.interactivetvweb.org) - MHP/OCAP Website from Steven Morris.
  - [Official java.net BD-J Forums](http://forums.java.net/jive/forum.jspa?forumID=117&start=0) - 公式な BD-J 関連フォーラム
  - [bdjforum.com](http://www.bdjforum.com) - 非公式な開発者向けフォーラム
  - [1](https://web.archive.org/web/20160610054537/https://java.net/projects/hdcookbook/pages/Home) - 開発者ツール

[Category:Blu-ray_Disc](https://ja.wikipedia.org/wiki/Category:Blu-ray_Disc "wikilink") [Category:ビデオストレージ](https://ja.wikipedia.org/wiki/Category:ビデオストレージ "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:媒体](https://ja.wikipedia.org/wiki/Category:媒体 "wikilink")

1.