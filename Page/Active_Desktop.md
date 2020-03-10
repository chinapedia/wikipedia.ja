> この記事は[Active Desktop](https://ja.wikipedia.org/wiki/Active_Desktop)から翻訳されています。


**アクティブデスクトップ** (**Active Desktop**)は、[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 4.0のオプションだった[Windowsデスクトップのアップデート](https://ja.wikipedia.org/wiki/Windowsデスクトップのアップデート "wikilink")に含まれる、デスクトップに[HTMLコンテンツを追加できるようにするなどといった機能である](../Page/HyperText_Markup_Language.md "wikilink")。この機能は、[Windows 95の機能を拡張するものであり](../Page/Microsoft_Windows_95.md "wikilink")、[Windows 98から標準搭載されていたが](../Page/Microsoft_Windows_98.md "wikilink")、[Windows Vistaで廃止されている](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。Internet Explorer 4.0から6.0には搭載、7.0で廃止された。

これを用いると、HTMLコンテンツを通常の壁紙として、あるいはそれとは独立した**デスクトップアイテム**として設置できる。どちらの場合でも、通常、オンラインで更新・同期されるため、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")を起動することなくウェブサイトの内容の表示を可能としている。

アクティブデスクトップは、デスクトップにカスタマイズにアイテムを設置できるという点で各種[デスクトップガジェット技術と同様である](https://ja.wikipedia.org/wiki/ウィジェットエンジン#デスクトップウィジェット "wikilink")。

アクティブデスクトップの使用を停止すると、特に性能の低いPCにおいて性能の向上と僅かながらメモリ使用量の減少が見られる。ディスプレイのプロパティにこの機能を利用するためのチェックボックスが存在する。さらに、[TweakUI](https://ja.wikipedia.org/wiki/TweakUI "wikilink")にはActiveDesktopを完全に使用禁止にする設定と設定の変更を禁止する設定という2つの設定項目が存在する。

## 歴史

アクティブデスクトップの始まりは、[PointCast](https://ja.wikipedia.org/wiki/PointCast "wikilink")などの[Push技術](https://ja.wikipedia.org/wiki/Push技術 "wikilink")への投資をマイクロソフトが試みるようになったことからである。アクティブデスクトップでは、ニュースや株価など頻繁に更新される情報を「チャンネル」としてコンピュータのデスクトップに設置することで、ウェブブラウザを起動することなく情報を表示できるようにしていた。

1997年、Windows 95とNT 4.0用のInternet Explorer 4.0のオプション機能、[Windowsデスクトップのアップデート](https://ja.wikipedia.org/wiki/Windowsデスクトップのアップデート "wikilink")に含まれる機能の1つとして、アクティブデスクトップの公開が始まった。Windowsデスクトップのアップデート全体が（誤って）アクティブデスクトップと呼ばれることもあるが、WindowsデスクトップのアップデートにはWindowsのシェル全体を4.0から4.71あるいは4.72へのアップグレードをしなければならない。これには、「すべて大文字のファイル名を使用する」、シングルクリックでのファイルを開く操作、フォルダ毎のHTML表示、QuickLaunch、スタートメニューの項目のドラッグアンドドロップや右クリックによるコンテキストメニューや名前の変更など、当時まだ発売されていないWindows 98と見まごうほどにインタフェースに様々な変更が加わったものも含まれる。また、このアップデートにより、WindowsエクスプローラのアドレスバーにインターネットのURLを入力してそのままそのウィンドウでインターネットを閲覧できる機能も加わっている。

アクティブデスクトップは、システムリソースを多量に消費することから、安定性の低下を招くことが主な原因として多くの人にとっては失敗したと考えられている\[1\]。また、マイクロソフトと米司法省の反トラスト訴訟において、Internet Explorerは独立した製品ではなくWindowsと一体の機能であるとして、アクティブデスクトップが持ち出された。

## その後の経過

Windows Vistaでは、アクティブデスクトップに代わって、[Windowsサイドバー](https://ja.wikipedia.org/wiki/Windowsサイドバー "wikilink")が搭載されている。これも同様にデスクトップにアイテムを設置する機能である。そのため、Windows XPがマイクロソフトのOSの中でアクティブデスクトップに対応した最後の製品となった。ただし、64ビット版のWindows XPはアクティブデスクトップに対応していない。なお、現在でもウェブページの表示と[Channel Definition Formatに基づくチャンネルの表示する機能は用意されている](https://ja.wikipedia.org/wiki/Channel_Definition_Format "wikilink")。

HTML表示の機能は現在主に元の壁紙に検索ボックスを追加するために用いられている。例えば、下記のコードはウィキペディアの検索ボックスをデスクトップに追加するものである。

``` html4strict
<form
    name="searchform"
    action="http://ja.wikipedia.org/wiki/%E7%89%B9%E5%88%A5:%E6%A4%9C%E7%B4%A2"
    id="searchform">
  <input
      id="searchInput"
      name="search"
      type="text"
      accesskey="f"
      value="" />
  <input
      type='submit'
      name="go"
      id="searchGoButton"
      value="Go" />
</form>
```

また、Internet Explorer 8で導入された[ウェブスライス](https://ja.wikipedia.org/wiki/ウェブスライス "wikilink")と比較されることもある。

## 脚注

## 外部リンク

  - [Internet Explorer 4.0 Desktop Gallery](http://www.microsoft.com/windows/ie/previous/gallery/default.mspx) (現在は削除されている)
      - [2004年時点でのアーカイブ](http://web.archive.org/web/20040610054229/http://www.microsoft.com/windows/ie/previous/gallery/default.mspx)
  - <http://wallabyweb.com/training/IE4/> Detailed technical documentation of Internet Explorer 4.0 features/changes

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink")

1.