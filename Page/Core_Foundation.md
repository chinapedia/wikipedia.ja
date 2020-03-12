> この記事は[Core Foundation](https://ja.wikipedia.org/wiki/Core_Foundation)から翻訳されています。


**Core Foundation**は[Cocoa](../Page/Cocoa.md "wikilink")のFoundationに相当するものを[C言語](../Page/C言語.md "wikilink")で記述したもの。実装をCへ移した理由は、[Carbon](../Page/Carbon.md "wikilink")との共有コードベースを備える為だと考えられる。

Core Foundationは[オープンソース](../Page/オープンソース.md "wikilink")の[Darwinの一部なので必要なら](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")を見ることができる。C言語で書かれているものの、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の雰囲気は残しており、[参照カウンタ](https://ja.wikipedia.org/wiki/参照カウンタ "wikilink")を用いたメモリ管理など[Objective-C](../Page/Objective-C.md "wikilink")に近いものになっている。Core FoundationのオブジェクトはCFTypeと呼ばれるopaqueな構造体であり、ヘッダ部をObjective-C互換にする事でメッセージ送信との混在利用が可能としている (toll-free bridge)。

Core Foundationに含まれるものはCFで始まる名前がつけられている。たとえばCFString（NSStringに相当）やCFArray（NSArrayに相当）、[Mac OS X v10.3以降ではCFStream](../Page/Mac_OS_X_v10.3.md "wikilink")（NSStreamに相当）など。他に[Quartz](../Page/Quartz.md "wikilink")のCGXXX、SearchKitのSKXXXなどもCFType互換となっており、相関性の高いインターフェースを備えている。

Core Foundationの本家であるCocoaもまずはC言語で実装し、それをObjective-Cでラップするという流れになっているようである。

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")での実装が基本であるが、主たる機能がCoreFoundation.dll、CoreGraphics.dll等の形で[Windows上に移植されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。 これらのライブラリは、同社の[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")[Safari](../Page/Safari.md "wikilink")の移植に活用されている。[APIそのものは公開されていないが](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、一部のユーザーによって、同DLLでCoreFoundationの機能をWindows上で実現させる方法が発見されている。。

## 外部リンク

  - [Core Foundation - ADC](http://developer.apple.com/corefoundation/)

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")