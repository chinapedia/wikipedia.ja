> この記事は[AtheOS](https://ja.wikipedia.org/wiki/AtheOS)から翻訳されています。


**AtheOS**は[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ベースのPCで動作する[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink") の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。当初、[AmigaOS](https://ja.wikipedia.org/wiki/AmigaOS "wikilink")の[クローン](https://ja.wikipedia.org/wiki/クローン "wikilink")を目指し作成されていたが、後に、方針を転換している。開発は中断されており、幾つかのプロジェクトへとフォークした。現在ではAtheOSのソースから派生している[Syllable](https://ja.wikipedia.org/wiki/Syllable "wikilink")がその直系の後継であるといえる。

公開時には既に実用となる完成度であり、公式サイトがAtheOSにより運用されていた。 [SMPへの対応や](../Page/対称型マルチプロセッシング.md "wikilink")、[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")を意識した[スレッドの多用など](../Page/スレッド_\(コンピュータ\).md "wikilink")、ソースこそ洗練されているといえない部分を含むものの、先進的な設計であった。

名前の"AtheOS"は[ギリシャ神話](https://ja.wikipedia.org/wiki/ギリシャ神話 "wikilink")の女神[アテナ](https://ja.wikipedia.org/wiki/アテナ "wikilink")から取られているが、奇しくもスペルは無神論者を意味する語と同じになっている。発音としてはアテオスと読む。 日本語はフォントを持っていれば表示は可能であるが、IMEの実装等は行われておらず、日本での情報や利用者は少ない。

[APIとしては](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[BeOS](../Page/BeOS.md "wikilink")の影響も見られる。

## 歴史

AtheOSは1994年から2000年初頭に掛けて[ノルウェー](../Page/ノルウェー.md "wikilink")のコンピュータ[プログラマ](../Page/プログラマ.md "wikilink")、[Kurt Skauenによって作成され](https://ja.wikipedia.org/wiki/Kurt_Skauen "wikilink")、2000年の3月、[usenet](https://ja.wikipedia.org/wiki/usenet "wikilink")で世界へ公開された。[ライセンス](../Page/ライセンス.md "wikilink")は[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であるが、SkauenはOSの完成度の向上のために、他の開発者の貢献を受け入れる事に躊躇いがちで、開発は停滞し、幾つかのプロジェクトへとフォークすることとなる。

2002年3月に[cosmoe](https://ja.wikipedia.org/wiki/cosmoe "wikilink")として、[カーネル](../Page/カーネル.md "wikilink")は[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、ウィンドウシステムは[XFree86](../Page/XFree86.md "wikilink")を使い、AtheOSのAPIを実装するプロジェクトが立ち上がった。

2002年7月には開発の停滞に業を煮やし、AtheOSのソースツリーを元に別プロジェクトとして開発を続行する[Syllable](https://ja.wikipedia.org/wiki/Syllable "wikilink")が発足している。

2007年時点で公式サイトは停止し、[Syllable](https://ja.wikipedia.org/wiki/Syllable "wikilink")のサイトにミラーが残っているのみであるが、[Syllable](https://ja.wikipedia.org/wiki/Syllable "wikilink")のサイトでは特に言及はない。 AtheOSとしての開発は中断されたままであるため、事実上停止したといえる。

Skauenは、AtheOSで動作するブラウザABrowseweb browserを作成するために[KHTML](../Page/KHTML.md "wikilink")の移植も行っている。

## 特徴

  - OS独自のネイティブな64ビット[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")、AtheOS File System(通常、AFSと呼ばれる)の実装。
  - SMPのサポート。
  - オリジナルのレガシーフリーなオブジェクト指向の[GUIアーキテクチャ](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。
  - POSIX規格の大部分のサポート。
  - マルチスレッド化された[プリエンプティブ・マルチタスク](https://ja.wikipedia.org/wiki/プリエンプション#プリエンプティブ・マルチタスク "wikilink")。
  - [オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の言語[C++](../Page/C++.md "wikilink")で書かれている[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

[Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:2000年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2000年のソフトウェア "wikilink")