> この記事は[XCB](https://ja.wikipedia.org/wiki/XCB)から翻訳されています。


**XCB**（**X C Binding**）は、[X Window System](../Page/X_Window_System.md "wikilink") の[C言語](../Page/C言語.md "wikilink")[バインディングである](https://ja.wikipedia.org/wiki/バインディング_\(情報工学\) "wikilink")。[Xlib](../Page/Xlib.md "wikilink")を置換することを目的としている。このプロジェクトは Bart Massey が[2001年](../Page/2001年.md "wikilink")に開始した。

**Xlib/XCB** は Xlib と XCB の[アプリケーション・バイナリ・インタフェース互換性を提供することで](../Page/Application_Binary_Interface.md "wikilink")、段階的な移植経路を提供するものである。Xlib/XCB は Xlib のプロトコル層を使うが、Xlib トランスポート層は XCB で置換しており、XCB を直接使うために XCB コネクションにアクセスできるようになっている。

## XCB の目的

XCB の主な目的は以下の2つである。

  - ライブラリサイズを小さくし、単純化する。
  - [Xプロトコルに直接アクセスする](../Page/X_Window_System_コアプロトコル.md "wikilink")。

後者の目的には、[C言語](../Page/C言語.md "wikilink")インタフェースを非同期にするという意味も含まれ、[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")化しやすくし、（[XMLプロトコル記述により](../Page/Extensible_Markup_Language.md "wikilink")）拡張実装を容易にする。

コアプロトコルと拡張プロトコルは[XML](../Page/Extensible_Markup_Language.md "wikilink") (xcb-proto) で記述され、Cバインディングは[Python](../Page/Python.md "wikilink")スクリプトによって生成される（以前のバージョンでは[XSLTあるいは](../Page/XSL_Transformations.md "wikilink")[m4を使っていた](https://ja.wikipedia.org/wiki/m4_\(プログラミング言語\) "wikilink")）。第三の目的は、このプロトコル記述をプロトコルに関する文書生成に再利用したり、C言語以外のバインディングやサーバサイドのスタブ生成に活用することである。

Massey らは XCB の主要部分の[形式的検証](../Page/形式的検証.md "wikilink")を[Z言語](../Page/Z言語.md "wikilink")を使って行ってきた（Xlib にはマルチスレッドの同期処理にAPI仕様レベルで誤りがあることが以前から知られていた）。

## 例

``` c
 /* ウィンドウ内に四角形を描画する単純な XCB アプリケーション */

 #include <xcb/xcb.h>
 #include <stdio.h>
 #include <stdlib.h>

 int main()
 {
   xcb_connection_t    *c;
   xcb_screen_t        *s;
   xcb_window_t         w;
   xcb_gcontext_t       g;
   xcb_generic_event_t *e;
   uint32_t             mask;
   uint32_t             values[2];
   int                  done = 0;
   xcb_rectangle_t      r = { 20, 20, 60, 60 };

                        /* サーバとのコネクションをオープン */
   c = xcb_connect(NULL,NULL);
   if (xcb_connection_has_error(c)) {
     printf("Cannot open display\n");
     exit(1);
   }
                        /* 第一スクリーン取得 */
   s = xcb_setup_roots_iterator( xcb_get_setup(c) ).data;

                        /* グラフィックスコンテキスト生成 */
   g = xcb_generate_id(c);
   w = s->root;
   mask = XCB_GC_FOREGROUND | XCB_GC_GRAPHICS_EXPOSURES;
   values[0] = s->black_pixel;
   values[1] = 0;
   xcb_create_gc(c, g, w, mask, values);

                        /* ウィンドウ生成 */
   w = xcb_generate_id(c);
   mask = XCB_CW_BACK_PIXEL | XCB_CW_EVENT_MASK;
   values[0] = s->white_pixel;
   values[1] = XCB_EVENT_MASK_EXPOSURE | XCB_EVENT_MASK_KEY_PRESS;
   xcb_create_window(c, s->root_depth, w, s->root,
                   10, 10, 100, 100, 1,
                   XCB_WINDOW_CLASS_INPUT_OUTPUT, s->root_visual,
                   mask, values);

                        /* ウィンドウをマップ（表示）する */
   xcb_map_window(c, w);

   xcb_flush(c);

                        /* イベントループ */
   while (!done && (e = xcb_wait_for_event(c))) {
     switch (e->response_type & ~0x80) {
     case XCB_EXPOSE:    /* ウィンドウ描画/再描画 */
       xcb_poly_fill_rectangle(c, w, g,  1, &r);
       xcb_flush(c);
       break;
     case XCB_KEY_PRESS:  /* キー押下で exit */
       done = 1;
       break;
     }
     free(e);
   }
                        /* サーバとのコネクションをクローズ */
   xcb_disconnect(c);

   return 0;
 }
```

XCB はこの例からも分かるとおり、[Xlib](../Page/Xlib.md "wikilink")にほぼ相当するものの、API の抽象化レベルは若干低い。

## プロトコルの記述

XCB の作者はX11プロトコルを記述するプログラミング言語に中立であり、他のプログラミング言語とのバインディングを可能にする、専用のインターフェイス記述言語を XML で作った。libxcb 自身はコードジェネレーターと小さなC言語のユーティリティー関数からなる。

例：

``` xml
<xcb header="bigreq" extension-xname="BIG-REQUESTS"
    extension-name="BigRequests" extension-multiword="true"
    major-version="0" minor-version="0">

  <request name="Enable" opcode="0">
    <reply>
      <pad bytes="1" />
      <field type="CARD32" name="maximum_request_length" />
    </reply>
  </request>
</xcb>
```

## 参考文献

  - [XCB: An X Protocol C Binding](http://www.linuxshowcase.org/2001/full_papers/massey/massey.pdf) ([PDF](../Page/Portable_Document_Format.md "wikilink")) （Bart Massey and Jamey Sharp、[2001年](../Page/2001年.md "wikilink")[9月19日](../Page/9月19日.md "wikilink")、[XFree86](../Page/XFree86.md "wikilink") [2001年](../Page/2001年.md "wikilink")技術会議）
  - [XCL: An Xlib Compatibility Layer For XCB](http://www.usenix.org/events/usenix02/tech/freenix/full_papers/sharp/sharp_html/index.html) （Jamey Sharp and Bart Massey、[2002年](../Page/2002年.md "wikilink")[4月15日](../Page/4月15日.md "wikilink")、[USENIX](../Page/USENIX.md "wikilink") [2002年](../Page/2002年.md "wikilink")技術会議）
  - [X Meets Z: Verifying Correctness In The Presence Of POSIX Threads](http://www.usenix.org/events/usenix02/tech/freenix/full_papers/massey/massey_html/index.html) （Bart Massey and Robert Bauer、[2002年](../Page/2002年.md "wikilink")[4月15日](../Page/4月15日.md "wikilink")、[USENIX](../Page/USENIX.md "wikilink") [2002年](../Page/2002年.md "wikilink")技術会議）

## 脚注

## 外部リンク

  -
  - [XCB API リファレンス](http://xcb.freedesktop.org/XcbApi/) - [チュートリアル](http://xcb.freedesktop.org/tutorial/)

  - [libxcb チュートリアル](http://www.x.org/releases/current/doc/libxcb/tutorial/index.html)

  - [論文等](http://xcb.freedesktop.org/Publications)

[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink")