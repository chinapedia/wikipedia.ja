> この記事は[Xmonad](https://ja.wikipedia.org/wiki/Xmonad)から翻訳されています。


**xmonad** は [X Window System](../Page/X_Window_System.md "wikilink") 上で動く [タイル型ウィンドウマネージャ](https://ja.wikipedia.org/wiki/タイル型ウィンドウマネージャ "wikilink") である。このウィンドウマネージャは、[関数型プログラミング言語](https://ja.wikipedia.org/wiki/関数型プログラミング言語 "wikilink")[Haskell](../Page/Haskell.md "wikilink")で書かれている。

2007年3月に開発が始まったxmonadは、[dwm](https://ja.wikipedia.org/wiki/dwm_\(ウィンドウマネージャ\) "wikilink")、[larswm](https://ja.wikipedia.org/wiki/larswm "wikilink")、[StumpWM](https://ja.wikipedia.org/wiki/StumpWM "wikilink")等、他のタイル型ウィンドウマネージャと同様に、マウスを使わずに生産的にウィンドウを制御することを可能にすることを目指している。 xmonad は、[Arch Linux](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")、[Debian](../Page/Debian.md "wikilink")、[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")、[Gentoo](https://ja.wikipedia.org/wiki/Gentoo "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")等、多くの[Unix系](../Page/Unix系.md "wikilink")OSで利用可能である。

xmonadは、元々dwmの[クローン](https://ja.wikipedia.org/wiki/クローン "wikilink")であったが、今では、ワークスペース毎のレイアウト、タイリングリフレクション、状態の保存、レイアウトのミラーリング、[GNOME](../Page/GNOME.md "wikilink")上でのサポート、[ステータスバー](https://ja.wikipedia.org/wiki/ステータスバー "wikilink")等、dwmでは利用できない機能をサポートしている。

実行中に、設定ファイルを変更しリロードすることで、カスタマイズ可能である。

xmonadの特徴は、他のタイル型ウィンドウマネージャへ影響を与えている。例えば、dwm は urgency hooks という機能を xmonad から取り入れたり、バージョン4.8 で [Xinerama](https://ja.wikipedia.org/wiki/Xinerama "wikilink") をサポートし、 xmonadの機能である Fibonacci レイアウトを可能している。

他のウィンドウマネージャのエミュレーションやFibonacci レイアウトのような普通ではないレイアウトアルゴリズム等、xmonadのコアシステムの拡張は活発なコミュニティで実装されており、ライブラリとして利用可能である。

マウスを使う必要をなくすことに加えて、xmonadのバージョン0.7では、開発においてsemi-formal methodと[プログラム導出](https://ja.wikipedia.org/wiki/プログラム導出 "wikilink")を多く使うことで、信頼性の向上と、コード量を1200行以下にすることを可能にした。例えば、ウィンドウマネージャの特性(ウィンドウ[フォーカスの振舞いなど](https://ja.wikipedia.org/wiki/フォーカス_\(GUI\) "wikilink"))はQuickCheckを用いて検査される。

xmonadは、Haskellで書かれた初めてのウィンドウマネージャであることに加えて、 次の点においても、一般的ではない。 それは、zipper データ構造を、フォーカスを自動で扱うのに使ったことである。 これは、[パターンマッチを用いていることを考慮すると安全であることが証明されており](../Page/パターンマッチング.md "wikilink")、さらなる信頼性の向上に寄与している。

開発者は次のように述べている。

> "xmonad は X Window System 用のタイル型ウィンドウマネージャであり、Haskellによって実装し、設定を行い、動的に拡張可能である。xmonadの実装は、[副作用](../Page/副作用.md "wikilink")に支配されるソフトウェアを、純粋関数型データ構造や、表現力の高い[型システム](https://ja.wikipedia.org/wiki/型システム "wikilink")、高度な静的検査、特性に基いたテストを利用した Haskell から予想されるように、正確で効率的に開発可能であることを示している。加えて、我々はHaskellをアプリケーションの設定や拡張を行う言語でもあると考える。"

xmonadの実装は、Haskell の特徴や、Xlib や xft の Haskell [バインディング](https://ja.wikipedia.org/wiki/バインディング "wikilink") に加えて、QuickCheck、パターンガードのような[GHC](https://ja.wikipedia.org/wiki/GHC "wikilink")拡張、[モナド](../Page/モナド_\(プログラミング\).md "wikilink")、モナド変換、zipper、Cabalライブラリ、等のさまざまなツールを利用している。

## 脚注

<references/>

[Category:Xウィンドウマネージャ](https://ja.wikipedia.org/wiki/Category:Xウィンドウマネージャ "wikilink")