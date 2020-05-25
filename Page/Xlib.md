> この記事は[Xlib](https://ja.wikipedia.org/wiki/Xlib)から翻訳されています。


**Xlib** は、[X Window System](../Page/X_Window_System.md "wikilink") のクライアント用[ライブラリ](../Page/ライブラリ.md "wikilink")であり、[C言語](../Page/C言語.md "wikilink")で書かれている。[Xサーバ](https://ja.wikipedia.org/wiki/Xサーバ "wikilink")とのやり取りを行う[サブルーチン](../Page/サブルーチン.md "wikilink")群を含む。それらのサブルーチンを使うことで、[Xプロトコル](https://ja.wikipedia.org/wiki/Xプロトコル "wikilink")の詳細を知らなくともプログラムを書くことが可能になっている。Xlib を直接使っているアプリケーションは少なく、通常は Xlib の上位に[ウィジェット・ツールキット](../Page/ウィジェット・ツールキット.md "wikilink")を提供する次のようなライブラリを配置して使う。

[frame](https://ja.wikipedia.org/wiki/画像:X-client-libraries.svg "wikilink")

  - [Intrinsics](https://ja.wikipedia.org/wiki/Intrinsics "wikilink") (Xt)
  - [Athena widget set](https://ja.wikipedia.org/wiki/Xaw "wikilink") (Xaw)
  - [Motif](../Page/Motif_\(GUI\).md "wikilink")
  - [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")
  - [Qt](../Page/Qt.md "wikilink")（X11 版）
  - [Tk](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")

Xlib が登場したのは[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")ごろであり、[UNIX](../Page/UNIX.md "wikilink")系[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の[GUIに使われている](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。[XCB](../Page/XCB.md "wikilink") は Xlib の後継となるべく開発されている。

## データ型

Xlib での主要なデータ型は `Display` 構造体\[1\]と各種識別子型である。

ディスプレイとは、いわばグラフィカルな操作が行われる物理的あるいは仮想的な機器である。Xlib における `Display` 構造体には、ディスプレイに関する情報が格納されているが、より重要な情報としてクライアントとサーバ間のチャンネルに関する情報も格納している。例えば、[UNIX](../Page/UNIX.md "wikilink")系OSでは `Display` 構造体には、そのチャンネルの[ソケットの](../Page/ソケット_\(BSD\).md "wikilink")[ファイルハンドル](https://ja.wikipedia.org/wiki/ファイルハンドル "wikilink")が含まれる（`ConnectionNumber` マクロで取り出し可能）。Xlib の関数の多くは `Display` 構造体を引数としている。これは、Xlib の関数の多くがチャンネルに対して操作したり、特定のチャンネルに関する操作をするためである。特にサーバとやり取りする Xlib の関数は、チャンネルにアクセスするのにこの構造体を必要とする。ローカルな処理しかしない関数でも、特定のチャンネルに関連したデータを操作するためにこの構造体を必要とする。例えば、イベントキューの操作はチャンネルごとのイベントキューを操作する。

ウィンドウ、カラーマップなどはサーバが管理する。つまり、実際の見た目に関するデータはサーバ側にある。クライアントは識別子を使ってそれらのオブジェクトを操作する。クライアントはオブジェクトを直接操作できず、サーバにオブジェクトの識別子を指定して操作を要求する。

`Windows`、`Pixmap`、`Font`、`Colormap` などの型はすべて識別子であり、実際には32ビットの整数である。クライアントはサーバに対してウィンドウの生成を要求することでウィンドウを生成する。これは、ウィンドウの識別子（つまり番号）を返す Xlib 関数を呼び出すことで行われる。その後、その識別子を使ってクライアントがサーバに対してそのウィンドウへの各種操作を要求する。

識別子はサーバ内で一意である。その多くは別々のアプリケーションであっても同じオブジェクトを指すのに使われる。例えば、1つのサーバと接続した2つのアプリケーションがあるとき、1つの識別子でどちらも同じウィンドウを参照することができる。それぞれのアプリケーションは使用しているチャンネルが異なるため、それぞれ別々の `Display` 構造体を持っている。しかし、同じ識別子についての操作を要求すれば、同じオブジェクトに対して操作が行われる。

## プロトコルとイベント

サーバに要求を送る Xlib 関数は即座に要求を送るのではなく、*output buffer* という[バッファ](../Page/バッファ.md "wikilink")に一旦格納する。この場合の *output* はクライアントからサーバに向けての出力である。output buffer はサーバへのあらゆる種類の要求を格納でき、それは必ずしも画面に見える効果だけではない。output buffer は、関数 `XSync` や `XFlush` を呼び出したとき、あるいはサーバからの戻り値がある関数を呼び出したとき（応答があるまでそれら関数はブロックする）、あるいはその他の条件でフラッシュ（バッファ上のすべての要求がサーバに送られ、バッファを空にする）される。

Xlib は受け取ったイベントを[キューに格納する](../Page/キュー_\(コンピュータ\).md "wikilink")。クライアント・アプリケーションは、そのキューを調べて、イベントを取り出す。Xサーバがイベントを非同期に送るのに対して、Xlib を使うアプリケーションはキュー上のイベントにアクセスするのに Xlib 関数を明示的に呼び出さなければならない。そのような関数の中にはブロックするものもあり、その時点でも output buffer がフラッシュされる。

エラーは非同期に受け取られ、扱われる。アプリケーションは、エラー発生時にエラーメッセージをサーバから受け取るエラーハンドラを登録しておく。

ウィンドウの一部が見えない状態のとき、ウィンドウの内容が保持されているとは限らない。その場合、隠れていたウィンドウが見える状態になると `Expose` イベントがアプリケーションに送られる。アプリケーションは、そのイベントを受けてウィンドウの内容を再描画しなければならない。

## 関数

Xlib ライブラリの関数は次のように分類される。

1.  コネクションに関する操作（`XOpenDisplay`, `XCloseDisplay`, ...）
2.  サーバへの要求。操作要求（`XCreateWindow`, `XCreateGC`,...）と情報要求（`XGetWindowProperty`, ...）がある。
3.  クライアント側での操作。イベントキュー操作（`XNextEvent`, `XPeekEvent`, ...）とその他のローカルなデータの操作（`XLookupKeysym`, `XParseGeometry`, `XSetRegion`, `XCreateImage`, `XSaveContext`, ...）がある。

## 例

以下のプログラムは、ウィンドウを表示し、その中に小さな黒い四角形を描画するものである。

``` C
 /*
   ウィンドウに四角形を描画する簡単な Xlib アプリケーション
 */

 #include <X11/Xlib.h>
 #include <stdio.h>
 #include <stdlib.h>
 #include <string.h>

 int main() {
   Display *d;
   int s;
   Window w;
   XEvent e;

                        /* サーバとのコネクションを開く */
   d=XOpenDisplay(NULL);
   if(d==NULL) {
     printf("Cannot open display\n");
     exit(1);
   }
   s=DefaultScreen(d);

                        /* ウィンドウ生成 */
   w=XCreateSimpleWindow(d, RootWindow(d, s), 10, 10, 100, 100, 1,
                         BlackPixel(d, s), WhitePixel(d, s));

                        /* 受け付けるイベントの種類を選択 */
   XSelectInput(d, w, ExposureMask | KeyPressMask);

                        /* ウィンドウを可視化 */
   XMapWindow(d, w);

                        /* イベントループ */
   while(1) {
     XNextEvent(d, &e);
                        /* ウィンドウの描画と再描画 */
     if(e.type==Expose) {
       XFillRectangle(d, w, DefaultGC(d, s), 20, 20, 10, 10);
       XDrawString(d, w, DefaultGC(d, s), 50, 50, "Hello, World!",strlen("Hello, World!"));
     }
                        /* キー押下で終了 */
     if(e.type==KeyPress)
       break;
   }

                        /* サーバとのコネクションを閉じる */
   XCloseDisplay(d);

   return 0;
 }
```

クライアントは `XOpenDisplay` を呼び出すことでサーバとのコネクションを生成する。そして `XCreateSimpleWindow` でウィンドウ生成を要求する。`XMapWindow` を別途呼び出すことで、ウィンドウが画面上に見えるようになる。

四角形は `XFillRectangle` 呼び出しで描画される。この操作はウィンドウが生成された後でないと実行できない。しかも、一回呼び出すだけでは十分ではない。前述したようにウィンドウの内容は常に保持されるとは限らない。例えば、ウィンドウが別のウィンドウの下に隠され、再び上に出てきたとき、再描画が必要な場合がある。このため、上記プログラムでは、`Expose` イベントを受け取るたびに再描画を行っている。

したがって、ウィンドウの中身の描画は[イベントループ](../Page/イベントループ.md "wikilink")内で行われる。ループに入る前に、アプリケーションは受け取りたいイベントを選択しており、上記の例では `XSelectInput` でそれを行っている。イベントループは入って来るイベントを待ちうける。イベントがキー押下だった場合、このアプリケーションは終了する。expose イベントなら、ウィンドウの中身を再描画している。`XNextEvent` を呼び出すと、キュー上にイベントがなければ output buffer がフラッシュされる。

## 関連するライブラリ

Xlib はボタンもメニューもスクロールバーも提供しない。そのような[ウィジェットは](../Page/ウィジェット_\(GUI\).md "wikilink")、Xlib を使う別のライブラリが提供する。そのようなライブラリは次の2種類に分類される。

  - [Intrinsics](https://ja.wikipedia.org/wiki/Intrinsics "wikilink")（Xt）ライブラリ上に構築されたライブラリ群。Xt はウィジェットをサポートするためのライブラリだが、具体的なウィジェットは提供しない。特定のウィジェットは Xt 上の[ウィジェット・ツールキット](../Page/ウィジェット・ツールキット.md "wikilink")のライブラリが提供する。例えば、[Xaw](https://ja.wikipedia.org/wiki/Xaw "wikilink") や [Motif](../Page/Motif_\(GUI\).md "wikilink") がある。
  - Xlib を直接使い、具体的なウィジェットを提供するライブラリ群。この場合、Xt ライブラリは使われない。[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")、[Qt](../Page/Qt.md "wikilink")（X11版）、[FLTK](../Page/FLTK.md "wikilink")（X11版）などがある。

このようなウィジェット・ライブラリを使ったアプリケーションでは、イベントループに入る前にウィンドウの中身を指定し、`Expose` イベントによる再描画も自動的に行われる。

Xlib の代替として [XCB](../Page/XCB.md "wikilink") がある。その目的は、ライブラリの縮小とX11プロトコルへの直接的なアクセスである。XCB を下層に使って Xlib のインタフェースを提供する実装もある。

## 脚注

## 関連項目

  - [X Window System](../Page/X_Window_System.md "wikilink")
  - [Xプロトコル](https://ja.wikipedia.org/wiki/Xプロトコル "wikilink")

## 外部リンク

  - [Xlib Programming Manual](http://www.sbin.org/doc/Xlib)

  - [Manual pages for all Xlib functions](http://tronche.com/gui/x/xlib/function-index.html)

  - [Kenton Lee's pages on X Window and Motif](http://www.rahul.net/kenton/bib.html)

  - [A short tutorial on Xlib](http://tronche.com/gui/x/xlib-tutorial/)

  - [A longer tutorial on Xlib](http://users.actcom.co.il/~choo/lupg/tutorials/xlib-programming/xlib-programming.html)

  - [Using Xlib for creating a screensaver module](http://www.dis.uniroma1.it/%7eliberato/screensaver)

  -
[Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")

1.