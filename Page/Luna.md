> この記事は[Luna](https://ja.wikipedia.org/wiki/Luna)から翻訳されています。


**Luna**（ルナ）は、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") と [Windows Server 2003に搭載されている](../Page/Microsoft_Windows_Server_2003.md "wikilink")、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") (UI) の[スキンのひとつである](../Page/スキン_\(GUI\).md "wikilink")。

## 用語

[Windowsでは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、スキンのことを「テーマ」と称する。このうち、Windows XP以降で導入されたリッチな外観を「ビジュアル スタイル」と呼ぶ。アプリケーションでビジュアルスタイルを有効にするには、後述するようにコモンコントロールライブラリのバージョン6.0以降を使用するように指定しなければならない。

Lunaは開発[コードネーム](../Page/コードネーム.md "wikilink")および通称であり、正式名称ではない。Windows XP の開発コードネームから**Whistlerスタイル**と呼ばれることもある。実際のWindows XPでは「**Windows XP スタイル**」と表現されている。これに対し、ビジュアルスタイルを使わない従来のWindowsと同様のスタイルは「クラシック スタイル」と呼ばれる。

## 外観

デフォルトは[青色](https://ja.wikipedia.org/wiki/青色 "wikilink")をベースとした配色である。[タスクバー](../Page/タスクバー.md "wikilink")、[スタートメニュー](https://ja.wikipedia.org/wiki/スタートメニュー "wikilink")、ウィンドウの縁や、[タイトルバー](../Page/タイトルバー.md "wikilink")、[スクロールバー](../Page/スクロールバー.md "wikilink")、ログオン画面などの[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) 要素にLunaのデザインが適用される。全体的に丸みを帯びて光沢を持ったイメージが使用されている。標準の青色以外にも[シルバーとオリーブグリーンの配色があり](../Page/銀色.md "wikilink")、Windows XP[プリインストール](../Page/プリインストール.md "wikilink")のメーカー製PCの中には青色以外を初期設定にしている製品もあった。

「[草原](https://ja.wikipedia.org/wiki/草原_\(画像\) "wikilink")」([Bliss](https://ja.wikipedia.org/wiki/:en:Bliss_\(image\) "wikilink")) の[壁紙](../Page/壁紙.md "wikilink")もLuna既定の設定の特徴のひとつだが、これはクラシックスタイルでも使用することができる。

Lunaに使用される画像リソースはシステムファイル内に[Windows bitmap形式で埋め込まれており](../Page/Windows_bitmap.md "wikilink")、[マウスオーバー](https://ja.wikipedia.org/wiki/マウスオーバー "wikilink")およびクリックやドラッグの際に色が変わる単純なアニメーション効果も施される。このためクラシックスタイルと比較して[CPU](../Page/CPU.md "wikilink")の負荷やメモリの使用量が増える。ただし、アニメーションやフェード効果、影の有無などはシステムの詳細設定から有効・無効を切り替えることができる。

## Lunaから派生したビジュアルスタイル

### マイクロソフト純正

#### Royale

Lunaを元に、Media Center Edition と [Tablet PC Edition](../Page/タブレットPC.md "wikilink") 向けに開発されたデフォルメ版のビジュアルスタイルで、Media Center Edition やタブレットPCのマシンではエナジーブルーと呼ばれるテーマとしてプリセットされている。Royaleはグラデーションで光沢感を表現した、Media Center Style という配色を採用している。Windows XP デフォルトの草原をRoyaleの色調に合わせたエナジーブリスと呼ばれる壁紙も新規に添付されている。

Royaleは最初、Media Center Edition でしか利用できなかったが、[2005年](../Page/2005年.md "wikilink")[4月7日](../Page/4月7日.md "wikilink")にMicrosoft New Zealand がこれにリソースを追加した一般向けデスクトップテーマ「Royale Theme」を発表したことで、Media Center Edition 以外でも利用できるようになっている。

#### Zune Desktop Theme

[Zune](../Page/Zune.md "wikilink")発売を記念し、「Zune Desktop Theme」がZuneのサイトより期間限定で配布されていた。Royaleをベースに配色を変更し、Zuneを意識した黒基調のスタイルとなっている。また、Zuneのオリジナル壁紙が2種類添付されている。

#### Royale Noir

Royaleテーマの中で公式採用されなかったデザインが流出した物で、公式にはリリースされていない。タイトルバーは青みがかった黒、ボタンデザインは青を基調とし、RoyaleとZuneの中間のようなスタイルになっている。

### サードパーティー製のビジュアルスタイル

Windows XP の標準状態では、LunaとRoyale・Zune・Royale Noir以外のビジュアルスタイルを使えないが、システムファイル (uxtheme.dll) に改造を加えることで、Lunaに準じて制作された様々なスキンを使えるようになる。GUIを好みに合わせて変えたいが[WindowBlinds](../Page/WindowBlinds.md "wikilink")のようなアプリケーションは動作が重いため使いたくないユーザーには好まれている上級者向けの方法である。uxtheme.dllを改造する[パッチ](../Page/パッチ.md "wikilink")やユーザーが制作した様々なビジュアルスタイルがインターネット上で流通しているが、改造は自己責任で行う必要がある。

uxtheme.dllの改造だけではできないログオン画面の変更など、より多くのUI部位の変更に対応したStyleXPという[シェアウェア](../Page/シェアウェア.md "wikilink")も存在する。

### Windowsアプリケーション開発におけるビジュアルスタイル

Windows XP以降は、新しいビジュアルスタイルを使用したアプリケーションだけでなく、旧来のクラシックスタイルを使用したアプリケーションも同時に実行できるようになっている。これはWindows XP以降で搭載された[分離アプリケーションとSide-by-Sideアセンブリ](https://ja.wikipedia.org/wiki/分離アプリケーションとSide-by-Sideアセンブリ "wikilink")（通称WinSxS）と呼ばれる[ディスパッチ](https://ja.wikipedia.org/wiki/ディスパッチ "wikilink")技術に基づき、使用するコモンコントロールライブラリcomctl32.dllのバージョンをアプリケーションごとに指定できることによるものである。

Windows XP にはコモンコントロールの旧バージョン5および新バージョン6の両方がインストールされているが、このWinSxS技術により、コモンコントロールのバージョン6以降を使用するアプリケーションはビジュアルスタイルが適用され、コモンコントロールのバージョン5を使用するアプリケーションはクラシックスタイルが適用されるようになっている。

ビジュアルスタイルを適用したWindowsアプリケーションを開発するには、コモンコントロールのバージョン6以降を使用するように記述された、アプリケーションマニフェストファイルをリソースとして埋め込むか、実行プログラムの存在するフォルダにマニフェストファイルを配置する必要がある\[1\]。マイクロソフトの標準開発環境である [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") のバージョン2005以降は、[リンカのオプションでマニフェストファイルを指定できるほか](../Page/リンケージエディタ.md "wikilink")、pragmaディレクティブによるSide-by-Sideアセンブリのバージョン指定も可能となっている。

なお、[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 2.0以降を使用する[Windows Formsアプリケーションの場合は](../Page/Windows_Forms.md "wikilink")、Application.EnableVisualStylesメソッドを実行するだけでよい。[Windows Presentation Foundationの場合は](../Page/Windows_Presentation_Foundation.md "wikilink")、メッセージボックスなどの一部を除いて画面描画にはコモンコントロールライブラリではなく[XAML](https://ja.wikipedia.org/wiki/XAML "wikilink")描画エンジンが使用される。Windows XP上でWPFアプリケーションを実行する場合、既定でPresentationFramework.Luna.dllやPresentationFramework.Royale.dllといったテーマアセンブリが自動的に適用される。

## Vista以降

[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") ではLunaは削除され (ベータ版などでは搭載していたバージョンもあった/正規版でもにはLunaスタイルが採用されている)、[Windows Aero](../Page/Windows_Aero.md "wikilink") という新しい[インタフェースが実装された](../Page/インタフェース_\(情報技術\).md "wikilink")。半透明効果や3Dグラフィックスによる高度なエフェクトが多用されている。

Windows Aero が省かれた Windows Vista Home Basic や、他のエディションでもデスクトップ コンポジションを無効にする設定により、Windows XP に近いビジュアルスタイルが使用可能である。しかしLunaとの[互換性](../Page/互換性.md "wikilink")はない。

## 脚注

## 関連項目

  - [Aqua (コンピュータ)](../Page/Aqua_\(コンピュータ\).md "wikilink")

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/Category:グラフィカルユーザインタフェース "wikilink")

1.  [Windows XP ビジュアル スタイルの使用](https://msdn.microsoft.com/ja-jp/library/ms997646.aspx)