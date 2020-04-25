> この記事は[WinG](https://ja.wikipedia.org/wiki/WinG)から翻訳されています。


**WinG** (ウィン・ジー) とは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[Windows 3.1向けに開発したグラフィック](../Page/Microsoft_Windows_3.x.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")の一つである。

## 開発の経緯

[Windowsに標準搭載されていたグラフィックライブラリ](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[GDIでは](../Page/Graphics_Device_Interface.md "wikilink")、グラフィックの描画のたびに[インタフェースを介してグラフィックカードに描画命令を送る仕組みであったために描画速度が遅く](../Page/インタフェース_\(情報技術\).md "wikilink")、高速な2D描画を必要としたゲームには利用できなかった。そのため、オフィスアプリケーションやマルチメディアの利用はWindowsだが、ゲームのときはWindowsを終了させ、[MS-DOS](../Page/MS-DOS.md "wikilink")上でゲームを起動して楽しむのが一般的だった。MS-DOSはマシンのハードウェアを直接制御することができた\[1\]が、Windows 3.1の上でゲームを動かすとOSが割り込むためにゲームを高速に動作させるのは不可能に近い話だった。また、MS-DOSでは[OpenGL](../Page/OpenGL.md "wikilink")のようにハードウェアの違いを吸収できなかったので、ソフトメーカーが自力でおびただしい数のハードウェアそれぞれを意識したコードを書くか、他社が提供するドライバとライブラリを利用するしか無かった。そこで、 GDIのパフォーマンスの違い（特に[Bit Block Transfer](../Page/Bit_Block_Transfer.md "wikilink") (BitBlt) 処理）を吸収することで高速描画を可能とするライブラリとして、**WinG**が開発された。

## 制限

画面モードが256色であることが前提である。またWinGを最初に使用する際（または画面モードを変更した際）にはプログラムの最初でVRAM構造などによるパフォーマンスの違いを吸収するためにベンチマーク処理を行わなくてはならない。。

## [インストール](../Page/インストール.md "wikilink")方法

[Win32s](../Page/Win32s.md "wikilink")や[Video for Windows同様に](https://ja.wikipedia.org/wiki/Video_for_Windows "wikilink")、インストーラを利用してインストールすることができた。

## [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")への移行

このWinGの成果は、[Windows 95以後にも活かされた](../Page/Microsoft_Windows_95.md "wikilink")。Windows 95でも、ハードウェアに直接アクセスできない制約が残っているため、WinGを元に32ビットプログラムへの拡張が行われることになる。当初は、Windows Games SDKとして、拡張されたWinGのほか、サウンドチップやジョイパッドなどの[入力機器](https://ja.wikipedia.org/wiki/入力機器 "wikilink")と直接やりとりできるインタフェースとしてリリースされ、その後、マルチメディアテクノロジーの総称として[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")と言う名称が与えられた。WinGの後継となった[DirectDraw](../Page/DirectDraw.md "wikilink")はDirectX 7まで使用され、その後DirectX 8以降は[Direct3D](../Page/Direct3D.md "wikilink")と統合されてDirectX Graphicsとなっている。

## WinG使用のゲーム

  - [Doom](https://ja.wikipedia.org/wiki/Doom "wikilink") (1995)\[2\]
  - [シムシティ2000](../Page/シムシティ2000.md "wikilink") for Windows:[マクシス](../Page/マクシス.md "wikilink")
  - [シムタウン](../Page/シムタウン.md "wikilink"):[マクシス](../Page/マクシス.md "wikilink")
  - [3×3 EYES](../Page/3×3_EYES.md "wikilink")～吸精公主～:[ニホンクリエイト](../Page/ニホンクリエイト.md "wikilink") (Windows 95版も発売)
  - [信長の野望・天翔記](../Page/信長の野望・天翔記.md "wikilink"):[コーエー](../Page/コーエー.md "wikilink") (Windows 95版も発売)
  - [太閤立志伝II](../Page/太閤立志伝II.md "wikilink") for Windows:[コーエー](../Page/コーエー.md "wikilink")
  - [ぷよぷよ](../Page/ぷよぷよ.md "wikilink") for Windows:[ボーステック](../Page/ボーステック.md "wikilink") (Windows 95&98版も発売)
  - [ザ・タワー (ゲーム)](../Page/ザ・タワー_\(ゲーム\).md "wikilink") (1995)

## 脚注

## 関連項目

  - [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink")

1.  [［GDC 2016］PS4のゲームをMS-DOSに移植？ 8bit風アクション「Retro City Rampage」開発者が21世紀におけるDOSゲーム開発を語った - 4Gamer.net](http://www.4gamer.net/games/999/G999901/20160319013/)
2.  [WinDoom, WinG, Win32s on Windows 3.1 (on Qemu) | Fun with virtualization](http://virtuallyfun.superglobalmegacorp.com/2011/03/29/windoom-wing-win32s-on-windows-3-1-on-qemu/)