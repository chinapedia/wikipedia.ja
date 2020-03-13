> この記事は[Uniform Type Identifier](https://ja.wikipedia.org/wiki/Uniform_Type_Identifier)から翻訳されています。


（**UTI**）は[データ](../Page/データ.md "wikilink")（エンティティ）のタイプ（種類、型）を一意に識別する文字列である。[アップルの](../Page/アップル_\(企業\).md "wikilink")  から追加され\[1\]、 などで[ファイルや](../Page/ファイル_\(コンピュータ\).md "wikilink")[フォルダ](../Page/ディレクトリ.md "wikilink")、[クリップボード](../Page/クリップボード.md "wikilink")のデータ、[バンドル](../Page/アプリケーションパッケージ.md "wikilink")、[エイリアス](../Page/ソフトリンク.md "wikilink")、[シンボリックリンク](../Page/ソフトリンク.md "wikilink")、[ストリーミング](../Page/ストリーミング.md "wikilink")データなどを識別するのに利用されている。UTIは[ドメイン名](../Page/ドメイン名.md "wikilink")を逆さにした構造をしている。また、UTIは[マルチメディア](../Page/マルチメディア.md "wikilink")ファイルが（ のように）単一のタイプに識別されないように [多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")を採用している。つまり1つの識別子は例えば `public.audio`、`public.video`、`public.text`、`public.image` など複数の識別子を継承できる。

継承の階層がUTIの最も重要な部分である。UTIの階層には次の2つがある。

  - 物理階層\[2\]
  - 機能階層\[3\]

物理階層での継承は必須だが、機能階層での継承は任意である。

`public`ドメインはアップルのみが宣言可能なドメインで、UTIにおける基底タイプを含んでいる。

<table>
<thead>
<tr class="header">
<th><p>識別子</p></th>
<th><p>継承元</p></th>
<th><p>意味</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>public.item</code></p></td>
<td></td>
<td><p>物理ヒエラルキーの基底タイプ</p></td>
</tr>
<tr class="even">
<td><p><code>public.content</code></p></td>
<td></td>
<td><p>すべてのドキュメント・データ（機能ヒエラルキー）の基底タイプ</p></td>
</tr>
<tr class="odd">
<td><p><code>public.data</code></p></td>
<td><p><code>public.item</code></p></td>
<td><p>ファイル、<a href="../Page/バイト_(情報).md" title="wikilink">バイトストリーム</a>、クリップボードデータの基底タイプ</p></td>
</tr>
<tr class="even">
<td><p><code>public.image</code></p></td>
<td><p><code>public.data</code><br />
<code>public.content</code></p></td>
<td><p><a href="../Page/画像.md" title="wikilink">画像</a>の基底タイプ</p></td>
</tr>
</tbody>
</table>

UTIは他のファイルタイプ識別子を識別する用途でも使われる。

| 識別子                         | 継承元                            | 意味                                                                                                      |
| --------------------------- | ------------------------------ | ------------------------------------------------------------------------------------------------------- |
| `public.filename-extension` | `public.case-insensitive-text` | [拡張子](../Page/拡張子.md "wikilink")                                                                        |
| `public.mime-type`          | `public.case-insensitive-text` | <tt>MIMEタイプ                                                                                             |
| `com.apple.ostype`          | `public.text`                  | [OSType](https://ja.wikipedia.org/wiki/OSType "wikilink")。[リソースフォーク](../Page/リソースフォーク.md "wikilink")参照。 |
| `com.apple.nspboard-type`   | `public.text`                  | [NSPasteboard](https://ja.wikipedia.org/wiki/NSPasteboard "wikilink")タイプ                                |

## 脚注

<references/>

## 外部リンク

  - [](http://developer.apple.com/library/mac/#documentation/Miscellaneous/Reference/UTIRef/Articles/System-DeclaredUniformTypeIdentifiers.html)
  - [](http://developer.apple.com/documentation/Carbon/Conceptual/understanding_utis/)
      - (和訳)[ の概要](http://potting.syuriken.jp/potting_conv/understanding_utis_J/chapter1.html)
  - [Mac OS X 10.4 Tiger](http://arstechnica.com/reviews/os/macosx-10.4.ars/11)（ のUTIに関する記事

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:メタデータ](https://ja.wikipedia.org/wiki/Category:メタデータ "wikilink") [Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink")

1.  クリップボードでは  から利用されていた
2.
3.