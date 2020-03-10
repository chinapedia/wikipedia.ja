> この記事は[FreeType](https://ja.wikipedia.org/wiki/FreeType)から翻訳されています。


**FreeType**（フリータイプ）は、フォントエンジンを実装した[ライブラリ](../Page/ライブラリ.md "wikilink")である。を中心に、フォント関連の様々な操作をサポートしている。

FreeType はあくまでも[フォント](../Page/フォント.md "wikilink")関連のライブラリであって、テキストのレイアウトやグラフィックスの処理（色付きテキストの[レンダリングなど](https://ja.wikipedia.org/wiki/レンダリング_\(コンピュータ\) "wikilink")）といった上位の [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") は提供しない。また、フォントの編集や追加もできない。しかし、フォントファイルの内容へのアクセスについて、抽象化された一様で扱いやすい[インタフェースを提供することで](../Page/インタフェース_\(情報技術\).md "wikilink")、[アプリケーションフレームワーク](https://ja.wikipedia.org/wiki/アプリケーションフレームワーク "wikilink")における下位レベルのテキスト描画処理などの実装が容易になる。

[TrueType](../Page/TrueType.md "wikilink")、[Type1フォント](https://ja.wikipedia.org/wiki/PostScriptフォント#Type_1 "wikilink")、[OpenType](../Page/OpenType.md "wikilink")などのフォント形式をサポートしている\[1\]。

FreeType のライセンス形態は、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") または [BSD License](https://ja.wikipedia.org/wiki/BSD_License "wikilink") に似た独自のライセンスである。従って、このライブラリは商用か否かにかかわらず、任意のプロジェクトで使用可能である。ライセンスファイルに記された作者は David Turner、Robert Wilhelm、Werner Lemberg である。

などの他のライブラリでも使用されている\[2\]。[FreeBSD](../Page/FreeBSD.md "wikilink")や[Android](https://ja.wikipedia.org/wiki/Android "wikilink")、[iOSなどの](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")におけるフォント描画にも採用されている。

## 参考文献

## 外部リンク

  - [FreeType Project](https://freetype.org/)
  - [FreeType Project at SourceForge](http://freetype.sourceforge.net/index2.html)

[Category:DTPソフト](https://ja.wikipedia.org/wiki/Category:DTPソフト "wikilink") [Category:タイポグラフィ](https://ja.wikipedia.org/wiki/Category:タイポグラフィ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [FreeType 2 FAQ](https://www.freetype.org/freetype2/docs/ft2faq.html)
2.  [Frequently Asked Questions (FAQ)](http://www.sfml-dev.org/faq.php#build-link-static)に依存関係の記載あり