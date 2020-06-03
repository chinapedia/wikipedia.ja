> この記事は[IronRuby](https://ja.wikipedia.org/wiki/IronRuby)から翻訳されています。


**IronRuby**は、[.NET Framework上で動作する](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")による[Ruby](../Page/Ruby.md "wikilink")の実装である。 [CLR](../Page/共通言語ランタイム.md "wikilink") 2.0/4.0上で[動的型付け](../Page/動的型付け.md "wikilink")や動的メソッドディスパッチの機能を提供する[動的言語ランタイム](../Page/動的言語ランタイム.md "wikilink")の上に実装されている。 現在では[Apache License](../Page/Apache_License.md "wikilink") ver. 2.0のもと公開され、ユーザーコミュニティにて開発と管理がなされている。

## 歴史

IronRubyはWilco BauwerのIronRubyプロジェクトの名称を許可をとって使用している\[1\]。[2007年](../Page/2007年.md "wikilink")[4月30日](../Page/4月30日.md "wikilink")、[MIX](https://ja.wikipedia.org/wiki/MIX_\(マイクロソフト\) "wikilink") 2007において発表され、 2007で公開されることが予定されていた\[2\]。[2007年](../Page/2007年.md "wikilink")[7月23日](../Page/7月23日.md "wikilink")、約束どおりJohn Lamと[DLRの設計チームはIronRubyコンパイラのプレ](../Page/動的言語ランタイム.md "wikilink")[アルファ版](https://ja.wikipedia.org/wiki/アルファ版 "wikilink")をOSCONにて公開した。彼はまた、IronRubyを迅速に[オープンソース](../Page/オープンソース.md "wikilink")コミュニティに提供すると発表した\[3\]。

  - 2009年5月21日 RailsConf 2009にてバージョン0.5を発表、Ruby On Railsのデモが行われた。\[4\]
  - 2009年7月2日 バージョン0.6公開。\[5\]
  - 2009年7月23日 OSCON 2009でバージョン0.9の発表と、1.0への道筋が示された。\[6\]
  - 2009年8月1日 バージョン0.9公開。主要な機能の実装は0.9で一度終了し、バージョン1.0.0リリースまで品質の向上が主な作業となった。\[7\]
  - 2009年11月2日 バージョン0.9.2公開。バグ修正とDLRの更新に伴う更新が主な修正点。\[8\]
  - 2010年4月12日 バージョン1.0.0公開。正式なリリースで、初の安定版となる。\[9\]
  - 2010年7月17日 ライセンスがそれまでの[Microsoft Public Licenseから](../Page/シェアードソース.md "wikilink")[Apache License](../Page/Apache_License.md "wikilink") ver. 2.0に変更される。\[10\]
  - 2010年10月21日 IronRuby, IronPythonがマイクロソフトの管理下でなくなる事が示される。\[11\]
  - 2010年10月21日 バージョン1.1.1リリース。マイクロソフトとしての最後のリリース。このリリースよりVisual Studioへのアドオン機能が追加される。また、このリリースで互換性を持つRubyのバージョンが1.9.1とされた。\[12\]
  - 2011年2月7日 バージョン1.1.2リリース。コミュニティへの移管後の初めてのリリース。\[13\]
  - 2011年3月13日 バージョン1.1.3リリース。\[14\]

IronRubyは[RubySpec](https://ja.wikipedia.org/wiki/RubySpec "wikilink")を元に実装されており、 [Github](https://ja.wikipedia.org/wiki/Github "wikilink")にあるIronRubyのリポジトリにはMSpecテストフレームワークを使用したRubySpecのテストが含まれている。\[15\]

## Monoへの対応

IronRubyはマイクロソフトの[Common Language Runtime](https://ja.wikipedia.org/wiki/Common_Language_Runtime "wikilink") (CLR) ではないオープンソースソフトウェア実装である[Monoでも動作する](../Page/Mono_\(ソフトウェア\).md "wikilink")\[16\]。しかし、マイクロソフト管理下の時点でのIronRubyチームは[WindowsのCLR上でしか動作確認を行っておらず](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[17\]、Mono上でのビルド確認は行われなかった\[18\]\[19\]\[20\]。

Monoでのビルドに関してはGithubのWikiに記述がある。\[21\]

## 動作保証となっているランタイムのバージョン

### Version 1.0.0

  - .NET Framework 2.0 SP1
  - .NET Framework 4.0

### Version 1.1 以降

  - .NET Framework 4.0
  - Silverlight 4

## .NETとの相互互換性

Rubyからの視点だと、.NETのクラスはRubyのクラスではないので、そこでの相互運用性については限定的である。ただし、.NETのアセンブリの呼び出しや、.NETからのRubyスクリプトの呼び出しは他の環境に比べれば遙かに容易である。

## ライセンス

IronRubyは、[BSDスタイルのライセンスに近い](../Page/BSDライセンス.md "wikilink")[Microsoft Public Licenseの下でリリースされていたが](../Page/シェアードソース.md "wikilink")、2010年7月16日にIronRuby、IronPython、Dynami Language Runtime (DLR) はマイクロソフトによって[Apache License](../Page/Apache_License.md "wikilink"), v2.0に変更された。\[22\]

## 関連書籍

  - Shay Friedman, "IronRuby Unleashed", Sam's, 2010, ISBN 0672330784
  - Ivan Porto Carrero and Adam Burmister, "IronRuby in Action", Manning, 2010, ISBN 1933988614

## 関連項目

  - [JRuby](https://ja.wikipedia.org/wiki/JRuby "wikilink")
  - [Ruby](../Page/Ruby.md "wikilink")
  - [IronPython](../Page/IronPython.md "wikilink")

## 外部リンク

  - [Codeplex IronRuby](http://ironruby.codeplex.com/)
  - [IronRuby](http://ironruby.net/)
  - [IronRuby source code](https://github.com/IronLanguages/main/)
  - [S. Somasegar's blog entry announcing IronRuby](http://blogs.msdn.com/somasegar/archive/2007/04/30/mix-07-silverlight-shines-brighter.aspx)
  - [John Lam's IronRuby blog entry](http://www.iunknown.com/2007/04/introducing_iro.html)
  - [John Lam's IronRuby release blog](http://www.iunknown.com/2007/07/a-first-look-at.html)
  - [State of IronRuby](http://rubyconf2007.confreaks.com/d2t1p1_state_of_ironruby.html) by John Lam at RubyConf 2007
  - [IronRuby: The Right Language for the Right Job](http://channel9.msdn.com/pdc2008/TL44/) by John Lam at PDC2008

## 脚注

<references />

{{.NET}}

[Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:Ruby](https://ja.wikipedia.org/wiki/Category:Ruby "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

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
15.
16.
17.
18.
19.
20.
21.
22.