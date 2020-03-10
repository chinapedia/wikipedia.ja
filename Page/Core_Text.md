> この記事は[Core Text](https://ja.wikipedia.org/wiki/Core_Text)から翻訳されています。


**Core Text**は、[Mac OS X v10.4で初めて導入され](../Page/Mac_OS_X_v10.4.md "wikilink")、[Mac OS X v10.5で公開された](../Page/Mac_OS_X_v10.5.md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の[Core Foundation風の](../Page/Core_Foundation.md "wikilink")[APIで](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、古くからmacOSにあり非推奨となった[QuickDraw](https://ja.wikipedia.org/wiki/QuickDraw "wikilink")や[ATSUIに代わってテキストレンダリングの機能を担うものである](https://ja.wikipedia.org/wiki/Apple_Type_Services_for_Unicode_Imaging "wikilink")。[アップルによると](../Page/アップル_\(企業\).md "wikilink")、Core Textは高いパフォーマンスと利用の容易さを意識して設計され、このレイアウトAPIはシンプルで安定しており、Core Foundationや[Core Graphics](../Page/Quartz.md "wikilink")、[Cocoa](../Page/Cocoa.md "wikilink")と密接に関連している。\[1\]

## 特徴

Core Textは次のような不透過型を提供している。

  - **CTFramesetter** - CTTypesetterを使って、与えられた属性付き文字列とCGPathからCTFrameオブジェクトを生成する。
  - **CTTypesetter** - 改行などの行のレイアウトを行う。
  - **CTFrame** - 行（CTLineオブジェクト）の配列を表す。
  - **CTLine** - 同じ属性を持つグリフの並びの配列を表す。
  - **CTFont** - フォントを表す。

## 使用例

次のコードは与えられたグラフィックコンテクストに「Hello, World\!」と表示する。

``` cpp
// フォントの準備
CTFontRef font = CTFontCreateWithName(CFSTR("Times"), 48, NULL);

// 属性付き文字列の生成
CFStringRef keys[] = { kCTFontAttributeName };
CFTypeRef values[] = { font };
CFDictionaryRef attr = CFDictionaryCreate(NULL, (const void **)&keys, (const void **)&values,
                      sizeof(keys) / sizeof(keys[0]), &kCFTypeDictionaryKeyCallBacks, &kCFTypeDictionaryValueCallBacks);
CFAttributedStringRef attrString = CFAttributedStringCreate(NULL, CFSTR("Hello, World!"), attr);
CFRelease(attr);

// 文字列の描画
CTLineRef line = CTLineCreateWithAttributedString(attrString);
CGContextSetTextMatrix(context, CGAffineTransformIdentity);
CGContextSetTextPosition(context, 10, 20);
CTLineDraw(line, context);

// 後片付け
CFRelease(line);
CFRelease(attrString);
CFRelease(font);
```

## 参照

## 外部リンク

  - [Overview at Apple's Developer Connection](http://developer.apple.com/documentation/Carbon/Conceptual/CoreText_Programming/Overview/chapter_2_section_1.html)

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink")

1.  [Core Text Programming Guide: Core Text Overview](http://developer.apple.com/documentation/Carbon/Conceptual/CoreText_Programming/Overview/chapter_2_section_1.html)