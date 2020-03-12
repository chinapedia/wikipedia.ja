> この記事は[Cdparanoia](https://ja.wikipedia.org/wiki/Cdparanoia)から翻訳されています。


**cdparanoia**（シーディーパラノイア）は[Linux](../Page/Linux.md "wikilink")上で\[1\]動作する[オープンソース](../Page/オープンソース.md "wikilink")かつ[フリーなCDリッパーである](../Page/フリーソフトウェア.md "wikilink")。有志により[BeOS](../Page/BeOS.md "wikilink")・[BSD系OS](../Page/BSDの子孫.md "wikilink")・[Mac OS Xなど他の](https://ja.wikipedia.org/wiki/macOS "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) 向けにも移植されている.[ミニマリズム](https://ja.wikipedia.org/wiki/ミニマル "wikilink")（最小限主義）的な思想で設計されている。貧弱な[ハードウェア](../Page/ハードウェア.md "wikilink")の下であっても、強力なエラー補正機能によって高品質な[リッピング](../Page/リッピング.md "wikilink")を実現する事が出来る。

## 設計

全体の核となるパラノイアライブラリが実際の作業の大半を担当しているため、[アプリケーションとしてのcdparanoiaは](../Page/アプリケーションソフトウェア.md "wikilink")、単なるparanoiaライブラリの[フロントエンド](../Page/フロントエンド.md "wikilink")である。paranoiaライブラリの最終安定バージョンはParanoia IIIである。

cdparanoiaの設計は基本的に「多すぎる機能は本質を損なう\[2\]」という考えに基づいている。cdparanoiaは、[GUIや](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[CDDB](../Page/CDDB.md "wikilink")アクセスなどの関係のない機能の代わりに、正確なリッピング機能を提供し、[CD-ROMドライブというハードウェアについてよく知る事が出来るように設計されている](../Page/光学ドライブ.md "wikilink")。

## 開発の歴史

cdparanoiaは[Xiph.org](https://ja.wikipedia.org/wiki/Xiph.org "wikilink")の、後の[Vorbisや](https://ja.wikipedia.org/wiki/Ogg_Vorbis "wikilink")[Theora](../Page/Theora.md "wikilink")と同じチームによって開発された。ソースコードリポジトリは[Subversionを用いて公開されている](../Page/Apache_Subversion.md "wikilink")。プロジェクトはcdda2wavへの[パッチ](../Page/パッチ.md "wikilink")を制作するためのものとして開始された。それらはParanoia IおよびIIと呼ばれ、限定的なエラー補正と少数のデバイスがサポートされていた。1998年1月のParanoia IIIから[スタンドアローン](../Page/スタンドアローン.md "wikilink")の[ライブラリ](../Page/ライブラリ.md "wikilink")となった。

最新の開発バージョンであるParanoia IVは、より柔軟性、移植性、有能性に優れたものとなるように設計されている。[パラレルポート](../Page/パラレルポート.md "wikilink")用デバイスのサポートやプリギャップの検出と除去、[Solaris](../Page/Solaris.md "wikilink")への[移植が計画されている](../Page/移植_\(ソフトウェア\).md "wikilink")。[ウェブサイト](../Page/ウェブサイト.md "wikilink")や[ソースコード](../Page/ソースコード.md "wikilink")の公式なアップデートが途絶えた事もあり、[2002年](../Page/2002年.md "wikilink")以降、プロジェクトが終了したかのように見えたが、2006年8月にバージョン10.0のプレリリースとともに継続が発表された\[3\]。

## ステータスインジケータ

cdparanoiaは進行状況を表すために[スマイリーフェイス](../Page/スマイリーフェイス.md "wikilink")に似た[顔文字](../Page/顔文字.md "wikilink")を表示するのが特徴である。

`:-)        通常動作、低／無ジッタ`
`:-|        通常動作、有意なジッタ`
`:-/        読み取りドリフト`
`:-P        最小単位の読み取り動作における無報告のストリーミング消失`
`8-|        再読み取り中に問題を検出、訂正困難`
`:-0        SCSI/ATAPI転送エラー`
`:-(        スクラッチ（擦り傷）を検出`
`;-(        訂正を放棄`
`8-X        訂正不可能な既知のエラーにより終了`
`:^D        展開完了`

## 関連項目

  - [CD-DA](../Page/CD-DA.md "wikilink")
  - [Sound Juicer](https://ja.wikipedia.org/wiki/Sound_Juicer "wikilink")

## 脚注

<references />

## 外部リンク

  - [CDDA Paranoia Homepage](http://www.xiph.org/paranoia/index.html) -- 公式サイト
  - [cdparanoia user manual (Japanese)](http://xiph.org/paranoia/manualj.html) -- 日本語版マニュアル
  - [2](http://strangehours.livejournal.com/9698.html) -- Mac OS X 用ソース
      - [Bronson Beta](http://www.bronsonbeta.com/) -- Mac OS X 用インストーラ
  - [cdparanoia for BeOS](http://www.learningcurve.freeserve.co.uk/cdparanoia.html)
  - [The FreeBSD Ports Archive: cdparanoia](http://www.freebsdsoftware.org/audio/cdparanoia.html)
  - [The NetBSD Packages Collection: audio/cdparanoia](http://www.jp.netbsd.org/ja/JP/Documentation/Packages/list/audio/cdparanoia/README.html)

[Category:Xiph.Org](https://ja.wikipedia.org/wiki/Category:Xiph.Org "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [1](http://xiph.org/paranoia/faq.html#req)
2.  [Why don't you implement CDDB? A GUI? Four million other features I want?](http://xiph.org/paranoia/faq.html#gimme)
3.  [Prerelease of Cdparanoia 10.0](http://lists.xiph.org/pipermail/paranoia-announce/2006-August/000006.html)