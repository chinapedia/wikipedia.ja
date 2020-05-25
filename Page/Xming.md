> この記事は[Xming](https://ja.wikipedia.org/wiki/Xming)から翻訳されています。


**Xming** は、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 上で動作する、[X Window System](../Page/X_Window_System.md "wikilink") の実装の一つ。Xming は [X.Org Server](../Page/X.Org_Server.md "wikilink") に基づいており、[Cygwin](../Page/Cygwin.md "wikilink") 版の [Cygwin/X](https://ja.wikipedia.org/wiki/Cygwin/X "wikilink")　(Xwin) にパッチを当てる形で\[1\]、[MinGW](../Page/MinGW.md "wikilink") と Pthreads-Win32 などを使って[クロスコンパイル](https://ja.wikipedia.org/wiki/クロスコンパイル "wikilink")されている。[Cygwin/X](https://ja.wikipedia.org/wiki/Cygwin/X "wikilink") は [Cygwin](../Page/Cygwin.md "wikilink") がないと動作できないが、Xming はそのような実行時依存性がない。Xming では他の環境の [X.Org Server](../Page/X.Org_Server.md "wikilink") 同様、[Mesa 3D](../Page/Mesa_3D.md "wikilink"), [OpenGL](../Page/OpenGL.md "wikilink"), [GLX](../Page/GLX.md "wikilink") などの3次元グラフィックスもサポートされている。

Xming に[SSH実装を組合せ](../Page/Secure_Shell.md "wikilink")、[UNIX](../Page/UNIX.md "wikilink")マシンから X11 セッションを安全にフォワードすることもできる。[PuTTY](../Page/PuTTY.md "wikilink") と *ssh.exe* をサポートしており、パッケージには PuTTY の plink.exe も含まれている。

## ライセンス

ソースコードは公開され続けているものの\[2\]、2007年5月以降はコンパイル済みのバイナリの入手には個人は£10以上の寄付、営利組織などは有償購入が必要となった\[3\]。寄付が始まる前の最後の6.9.0.31はSourceforgeでパブリックドメインとして配布し続けている。

## モード

Xming は、以下の5つのモードをサポートしている\[4\]。最初の3つは[Cygwin/X](https://ja.wikipedia.org/wiki/Cygwin/X "wikilink")と同じ。

  - シングルウィンドウ - X11 ルートウィンドウが Microsoft Windows の1つの境界付きのウィンドウとして表示される
  - マルチウィンドウ - X11 の各トップレベルウィンドウがそれぞれ Microsoft Windows の境界付きのウィンドウになる
  - ルートレス - Microsoft Windows の境界付きのウィンドウが使われずにオーバーレイする形で X11 のルートウィンドウが表示される。X11 側のウィンドウマネージャを利用可能。
  - タイトルバーなしシングルウィンドウ - シングルウィンドウで Microsoft Windows のタイトルバーがないもの
  - フルスクリーン - シングルウィンドウのフルスクリーン表示で、Microsoft Windows のタスクバーも非表示にしたもの

## 参照

## 外部リンク

  -
  - [Sourceforge development site](http://sourceforge.net/projects/xming)

[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [Xming Code](http://www.straightrunning.com/XmingCode/)
2.
3.  [Terms and Conditions](http://www.straightrunning.com/XmingNotes/terms.php)
4.  [Xming manual](http://www.straightrunning.com/XmingNotes/manual.php)