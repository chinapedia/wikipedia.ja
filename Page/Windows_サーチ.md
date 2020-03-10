> この記事は[Windows ](https://ja.wikipedia.org/wiki/Windows_)から翻訳されています。


**Windows サーチ**（ウィンドウズ - , Windows Search）は[マイクロソフト](../Page/マイクロソフト.md "wikilink")から無償提供されている[Windows向けのデスクトップ検索ツール](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、および[Windows Vista以降](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、同ツールが標準で搭載された検索機能。公式リリース前から「[MSN](../Page/MSN.md "wikilink") デスクトップサーチ」として知られており「MSNサーチツールバー」の付属ツールという位置づけだった。その後、Windowsデスクトップサーチ (WDS) と名称を変えた。[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")リリースのバージョン2は[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")、[Windows XPおよび](../Page/Microsoft_Windows_XP.md "wikilink")[Windows Server 2003で利用可能だったが](../Page/Microsoft_Windows_Server_2003.md "wikilink")、[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")のバージョン3はXPとServer 2003のみで利用可能となった。

バージョン3.0以降、インデクサは[Windowsサービスとして稼働するようになったため](https://ja.wikipedia.org/wiki/Windows_NT系#Windowsサービス "wikilink")、1つの[インデックス](https://ja.wikipedia.org/wiki/インデックス "wikilink")を（Windowsサービスの[インスタンス](../Page/インスタンス.md "wikilink")と同様）複数のユーザーで共有可能となり、パフォーマンスが改善された。

[Windows VistaではWDS](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") 3.0と互換性を持つ[APIで動作する機能を](../Page/アプリケーションプログラミングインタフェース.md "wikilink")「Windows Search」という名称で実装した。同じように、Windows 2000からWindows 2003 Serverまでは、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")のファイルをインデックス化して検索に寄与する「インデックスサービス」という機能を備えていた。しかし、それには適切な[UIが備わっておらず](../Page/ユーザインタフェース.md "wikilink")、[エクスプローラの検索機能や](https://ja.wikipedia.org/wiki/Windows_Explorer "wikilink")、[MMCスナップイン](https://ja.wikipedia.org/wiki/MMCスナップイン "wikilink")によって間接的に利用されなければいけなかった。また[インクリメンタルサーチ](https://ja.wikipedia.org/wiki/インクリメンタルサーチ "wikilink")も出来なかった。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[6月](../Page/6月.md "wikilink")にはVistaでの名称にあわせ「Windows Search」としてバージョン4.0がリリースされた。対応OSはWindows XP/Server 2003/Vista/[Server 2008](https://ja.wikipedia.org/wiki/Windows_Server_2008 "wikilink")/XP x64/Server 2003 x64/Vista x64/Server 2008 x64。このバージョンではリモートPCで作成されたインデックスを使用して検索が出来るようになり、[EFS](https://ja.wikipedia.org/wiki/EFS "wikilink")暗号機能を使った暗号化ファイルの検索にも対応した。

## 概要

インストール後、Windows サーチはユーザーのハードディスクにあるファイルを走査し、インデックスを構築する。これには数時間かかる場合もあるが、最初の1回だけでよい。いったんインデックスが作成されれば、Windows サーチを使って検索するとき、このインデックスを利用してコンピュータ上のすべてのファイルを高速に検索することが可能となる。検索ではファイル名だけでなく、キーワード、コメント、[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")のほか（[ファイルタイプ](https://ja.wikipedia.org/wiki/ファイルタイプ "wikilink")に適した文書フィルタがインストールされていれば）ファイル内の文章に対しても行うことが可能となる。例えば、「ビートルズ」で検索すれば、それをファイル名に含むファイル、本文に「ビートルズ」の文字列を含むあらゆる文書、[電子メール](../Page/電子メール.md "wikilink")、そしてビートルズの楽曲ファイルをも一覧表示してくれる。

Windows サーチの特長の1つに[インクリメンタルサーチ](https://ja.wikipedia.org/wiki/インクリメンタルサーチ "wikilink")がある。これは文字が検索ボックスに入力されると、即座に検索を開始し、入力文字が増えるに従って検索結果を絞り込んでいくというものだ。これによりすべての文字列を入力し終わる前に、探しているファイルを見つけ出せる可能性がある。

Windows サーチはAdvanced Query Syntax (AQS)によって構築された先進的な[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")をサポートする。AQSはファイルタイプに応じたフィルタ群を提供すると同時に、検索ワードの[ブーリアン](https://ja.wikipedia.org/wiki/ブーリアン "wikilink")演算（AND, OR, NOT）のような検索クエリをリファインする。また、一般的なファイルやオフラインファイル・キャッシュ、電子メールなどから特定の情報から結果を絞り込むのにも使われる。Windows サーチではファイルタイプごとの検索や[ワイルドカード](https://ja.wikipedia.org/wiki/ワイルドカード "wikilink")による検索もサポートされている。デフォルトでは[ワード](../Page/Microsoft_Word.md "wikilink")、[エクセル](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、[パワーポイント](https://ja.wikipedia.org/wiki/パワーポイント "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[テキスト](../Page/テキスト.md "wikilink")などの文書ファイル、[MP3](../Page/MP3.md "wikilink")、[WMA](https://ja.wikipedia.org/wiki/Windows_Media_Audio "wikilink")、[WMV](https://ja.wikipedia.org/wiki/WMV "wikilink")、[ASF](https://ja.wikipedia.org/wiki/Advanced_Systems_Format "wikilink")、[AVI](https://ja.wikipedia.org/wiki/AVI "wikilink")といった[マルチメディア](../Page/マルチメディア.md "wikilink")、[JPEG](../Page/JPEG.md "wikilink")、[BMP](../Page/Windows_bitmap.md "wikilink")、[PNGといった画像ファイルに対応しており](../Page/Portable_Network_Graphics.md "wikilink")、各種ベンダによって提供される[IFilter](https://ja.wikipedia.org/wiki/IFilter "wikilink")もサポートしている。IFilterは特定のファイル形式と対応づけられ、インデックス作成時にファイルからテキスト情報を抽出するために利用される。ファイルからメタデータを処理するためには[プロパティ・ハンドラ](https://ja.wikipedia.org/wiki/プロパティ・ハンドラ "wikilink")が利用される。Windows サーチがメタデータをインデックス化する際に、プロパティ・ハンドラはプロパティの内容と[スキーマ](https://ja.wikipedia.org/wiki/スキーマ "wikilink")を必要とする。プロトコル・ハンドラは特定の格納データをインデックス化する際に用いられる。たとえば、一般的なファイルはファイルシステム・プロトコル・ハンドラを、[Outlook](https://ja.wikipedia.org/wiki/Outlook "wikilink")の格納データならOutlookプロトコル・ハンドラを、[IE履歴](../Page/Internet_Explorer.md "wikilink")、キャッシュの場合はIE履歴・キャッシュ・プロトコル・ハンドラを利用してアクセスされる。

Windows サーチは検索結果を[サムネイル](https://ja.wikipedia.org/wiki/サムネイル "wikilink")表示するための[ペイン](https://ja.wikipedia.org/wiki/ペイン "wikilink")（表示領域）を備えている。また、他のアプリケーションがインデクシング・サーチ機能を利用できるようにAPIを提供する。このAPIを利用すれば、アプリケーションは全インデックスあるいはその一部で特定の[パラメータ](https://ja.wikipedia.org/wiki/パラメータ "wikilink")に基づいた検索クエリを発行することが出来るようになる。その結果は該当アプリケーションのインターフェイス上に表示され、そこからすすんで、条件による絞り込みなどの処理も可能にする。Outlook 2007や[OneNote 2007といったアプリケーションはそれ自身によって作成されたユーザーデータにインデックスを付け](https://ja.wikipedia.org/wiki/OneNote "wikilink")、アプリケーション内で検索する機能を備えている。これらもWindows サーチAPIによって提供されている。これらの機能にはWDS 3.0もしくはWindows サーチ4.0がインストールされているか、Windows Vista以降備わった検索機能が必要とされる。XP/Server 2003の場合、Windows サーチインストール後、[タスクバー](https://ja.wikipedia.org/wiki/タスクバー "wikilink")にテキスト・フィールドが追加される。そこに入力された検索クエリに応じて、結果がフライアウト・ペイン上に表示される。Windows サーチの検索UI上でリストアップされたファイルをクリックすることで、ファイルを開くことなく、右側のプレビュー・ペインに内容が表示される。ウェブ検索も同じインターフェイスから行なうことができる。

## Windows Vistaの検索機能

Windows Vistaの検索機能はWindowsデスクトップサーチ3.0に基づいたものでAPIも同様に提供されるため、WDS APIを利用するアプリケーションはWindows Vistaでも同様に稼働する。インデックス型の検索機能はWindows Search Serviceによって提供される。インデクサは低いプライオリティ（優先順位）で動作するため、他の[プロセス](../Page/プロセス.md "wikilink")が帯域やCPU処理を要求するときは、システム全体の負荷を上げないように配慮される。

Windows Search Serviceでは次の3つのプロセスが実行される。

  - SearchIndexer.exe　インデクサ本体
  - SearchProtocolHost.exe　プロトコルハンドラをホストする
  - SearchFilterHost.exe　IFilterをホストする

Windows Vistaの検索機能にはWDS 3.0にない特徴が含まれている。

  - オフラインファイルのインデックス化
  - 新しい[ファイルシステム](../Page/ファイルシステム.md "wikilink")に対応したLow-Priority [I/O](../Page/入出力.md "wikilink")
  - ネットワーク共有されているコンテンツがサーバ上でインデックス付与された場合、別のWindows Vistaか[Windows Server 2008でリモート検索が可能となる](../Page/Microsoft_Windows_Server_2008.md "wikilink")。
  - インデックス型検索と[Grep](https://ja.wikipedia.org/wiki/Grep "wikilink")型検索の併用が可能
  - [自然言語](../Page/自然言語.md "wikilink")検索のサポート

Vistaではスタートメニューから検索する場合、「最近使用されたプログラム」を表示せず、検索結果を表示する。同様に[コントロールパネルではコントロールパネル](https://ja.wikipedia.org/wiki/コントロールパネル_\(Windows\) "wikilink")・オプションを検索することが出来る。

Vista以降のWindows OSには同等の検索機能が標準で備わっている。

## 関連項目

  - [全文検索](../Page/全文検索.md "wikilink")
  - [Microsoft Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")

## 外部リンク

  - [IFilter.Org](http://www.ifilter.org/Links.htm) （英語）

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:検索](https://ja.wikipedia.org/wiki/Category:検索 "wikilink") [Category:検索エンジン](https://ja.wikipedia.org/wiki/Category:検索エンジン "wikilink")