> この記事は[Objective-C](https://ja.wikipedia.org/wiki/Objective-C)から翻訳されています。


**Objective-C**（オブジェクティブ シー）は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")の一種。[C言語](../Page/C言語.md "wikilink")をベースに[Smalltalk](../Page/Smalltalk.md "wikilink")型の[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")機能を持たせた上位互換言語である。

Objective-Cは[NeXT](../Page/NeXT.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の[OSに標準付属する公式開発言語である](../Page/オペレーティングシステム.md "wikilink")。macOSのパッケージ版に開発環境がDVDで付属するほか、ユーザ登録をすれば無償でダウンロードできる（[Xcode](../Page/Xcode.md "wikilink")の項目参照）。現在では主に[アップルのmacOSや](../Page/アップル_\(企業\).md "wikilink")[iOS上で動作するアプリケーションの開発で利用される](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。

## 概要

Objective-CはCを拡張してオブジェクト指向を可能にしたというよりは、Cで書かれたオブジェクト指向システムを制御しやすいように[マクロ的な拡張を施した言語である](../Page/マクロ_\(コンピュータ用語\).md "wikilink")。したがって、「better C」に進んだ[C++](../Page/C++.md "wikilink")とは異なり、「C & Object System」という考え方であり、ある意味2つの言語が混在した状態にある。

関数（メソッド）の定義と呼び出し方が独特であるため、Objective-Cのコードは一見C++以上にCとはかけ離れた独特の記述となる。しかし、言語仕様はCの完全上位互換であり、[if](https://ja.wikipedia.org/wiki/if文 "wikilink")/[for](https://ja.wikipedia.org/wiki/for文 "wikilink")/[whileなどの制御文や](https://ja.wikipedia.org/wiki/while文 "wikilink")、intなどのスカラー型、[関数記法](https://ja.wikipedia.org/wiki/サブルーチン#関数 "wikilink")、宣言・[代入といった基本的な文法はCに準拠する](../Page/変数_\(プログラミング\).md "wikilink")。一方オブジェクトシステムはSmalltalkの概念をほぼそのまま借用したもので、動的型のクラス型オブジェクト指向ランタイムを持ち、メッセージパッシングにより動作する。このことからしばしば「インラインでCの書けるSmalltalk」または「インラインでSmalltalkの書けるC」などと呼ばれる。Cとは異なるObjective-Cに特有の部分は、@で始まる**コンパイラディレクティブ**で明示され、オブジェクトのメソッド呼び出しは\[\]で囲まれた**メッセージ式**で行われる。

最大の特徴はオブジェクトシステムが完全に動的という点で、実行時のクラス拡張、オブジェクト汎用型idの導入により型によらない動的配列・辞書など、インタプリタに近い記述力をもつことである。実際にコードそのものはネイティブコンパイルされるものの、動作原理はほぼインタプリタに近く、コンパイラ型言語としてはまれな柔軟性を発揮する。

したがって、C側から見れば一種のスクリプトインタプリタが乗っているような状態であり、逆にオブジェクトシステムからはOS機能や膨大なC言語資源を直接利用可能なインターフェースが備わっているといえる。また仮想マシンを持たずに済むため、取り回しも良い。パフォーマンスはJavaのような中間コード型言語よりも良好で、CやC++のようなネイティブコンパイル言語には劣るとされる。Objective-C特有のこの形態は双方のメリット・デメリットが明確で、実際的な使い勝手が非常に優れている。この特性に着目したのが[NEXTSTEP](../Page/NEXTSTEP.md "wikilink")で、[UNIX](../Page/UNIX.md "wikilink")との互換性と先進的なオブジェクト指向環境の両立に成功し、その後のOS設計に大きな影響を与えることとなった。

後続言語への影響としては、特に[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の基礎設計にその姿を見ることができる（[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が[OPENSTEP](../Page/OPENSTEP.md "wikilink")に関わっていたことと関係がある）。

| クラス        | 単一継承＋インタフェース多重継承（プロトコル）　通常はルートクラスから継承                                                                                                          |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| オブジェクトシステム | [動的束縛](https://ja.wikipedia.org/wiki/名前束縛 "wikilink")、[メタクラス](../Page/メタクラス.md "wikilink")を持つ                                                  |
| 型          | [動的型](../Page/動的型付け.md "wikilink")＋見た目の[静的型のハイブリッド](https://ja.wikipedia.org/wiki/静的型付け "wikilink")                                            |
| 実行速度       | コードはCと同等のネイティブコンパイル、メソッド呼び出しは動的ディスパッチを行なうのでやや遅延する。平均してC/C++より多少遅く、中間コード型言語（Javaなど）より数倍程度高速といわれる。ただし、クリティカルな部分はいつでもCで書き直せるため、実行速度が問題になることはまずない。 |
| その他        | オブジェクトはポインタ互換、Cのスカラー型はオブジェクトではない                                                                                                               |

オブジェクトシステムの概要

## 歴史

Objective-Cは、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に[Brad CoxとTom](https://ja.wikipedia.org/wiki/:en:Brad_Cox "wikilink") Loveによって開発され\[1\]、そのコンパイラやライブラリを支援するためにStepstone社を創立した。Stepstone社は、Objective-Cに力を注いだが、それはマイナーな存在であった。Objective-Cが認知され始めるきっかけは、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")、[アップルコンピュータを去った](../Page/アップル_\(企業\).md "wikilink")[スティーブ・ジョブズ](../Page/スティーブ・ジョブズ.md "wikilink")が、m68k機であるNeXTコンピュータと[NeXTSTEP](https://ja.wikipedia.org/wiki/NeXTSTEP "wikilink")オペレーティングシステムの開発を行うNeXT Computer社を創立したことに始まる。

そのマシンのユーザインタフェースは、[Display PostScriptとObjective](../Page/Display_PostScript.md "wikilink")-Cで書かれたApplication Kitにより提供され、Objective-CはNeXTコンピュータの主力言語となった。その後の歴史は、主にNeXT社とともにあり、[GCCをベースにしたObjective](../Page/GNUコンパイラコレクション.md "wikilink")-Cサポートが行われ、プロトコルの導入など文法の拡張なども行われている。NeXT社による多くの成果は、GCCに還元されている。

1995年には、NeXT社がStepstone社からObjective-C言語と、その商標に関する全ての権利を買い取っている。1997年初頭、アップルがNeXT社を買収し、2001年に登場したMac OS Xの[Cocoa](../Page/Cocoa.md "wikilink")[フレームワークのコア言語として採用されている](../Page/アプリケーションフレームワーク.md "wikilink")。[Mac OS X v10.5からは一部言語仕様の変更が行われ](../Page/Mac_OS_X_v10.5.md "wikilink")**Objective-C 2.0**と呼ばれる（詳細は[\#Objective-C 2.0を参照](https://ja.wikipedia.org/wiki/#Objective-C_2.0 "wikilink")）。

コンパイラおよび言語仕様は完全に公開されているものの、長らくNeXTおよびその後継であるmacOSと[iOSの専用言語に近い状態にある](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。2008年にiPhone OS（現iOS）のAPIが公開されて以降、習得者の人口が増える傾向にあるが、アップルの開発環境は、徐々に[LLVMベースにシフトし](https://ja.wikipedia.org/wiki/Low_Level_Virtual_Machine "wikilink")、GCC版は事実上の[GNUstep](../Page/GNUstep.md "wikilink")専用と化している。

## 基本的な構文

### メッセージ送信

C++とは異なり、オブジェクトのメソッド呼びだしには[Smalltalkのメッセージ式を模した新たな構文が導入されている](https://ja.wikipedia.org/wiki/Smalltalk#メッセージ式 "wikilink")。Objecitve-Cではこれをメッセージ式と呼び、メソッド呼びだしはメッセージ送信と呼ぶ。メッセージ送信は実行時のメッセージパッシングであり、その時渡されるメッセージ値をセレクタという。特徴的なのはSmalltalk同様キーワード引数形式をとることで、セレクタ名と引数値が交互に並んだ形態になる。なおSmalltalkにはある[カスケード式](https://ja.wikipedia.org/wiki/Smalltalk#メッセージ式 "wikilink")（一つのオブジェクトに続けてメッセージを送る）はない。

``` objc
// メッセージの送信
// 単項メッセージ
[receiver msg];
// 引数付きメッセージ。この場合「msg:with:」でセレクタ一つ
val = [receiver msg: arg1 with: arg2];
// メッセージの入れ子
val = [obj1 msg: [obj2 msg]];
```

### クラス定義

Objective-Cのクラスは定義部と実装部に分かれており、通常定義部を.hファイル、実装部を.mファイルに記述する。後述のカテゴリによりクラス定義を複数のパートに分割できる。

``` objc
// クラスの定義 (MyObject.h)
@interface MyObject : NSObject
{
    int val;
    id obj;
}

+ (void)classMethod:(id)arg;  // クラスメソッド
- (id)method:(NSObject*)arg1 with:(int)arg2;  // インスタンスメソッド。arg1は型付き
@end
```

``` objc
// 実装 (MyObject.m)
@implementation MyObject
+ (void)classMethod:(id)arg
{
    // some operation
}

- (id)method:(NSObject*)arg1 with:(int)args2
{
    return obj;
}

// 典型的なinit
- (id)init
{
    self = [super init]; // スーパークラスの呼びだし
    if(self != nil)
    {
        val = 1;
        obj = [[SomeClass alloc] init];
    }
    return self;
}

// deallocは自身のリソースを解放してからスーパークラスに回す
- (void)dealloc
{
    [obj release];
    [super dealloc];
}
@end
```

メソッドにはクラスメソッドとインスタンスメソッドがあり、それぞれ接頭辞+及び-により区別される。クラスメソッドはクラスオブジェクトの操作に、インスタンスメソッドはインスタンスオブジェクトの操作に使用される。クラスメソッドは特にインスタンスオブジェクトの生成にも使用される事が多い。インスタンスメソッドは、インスタンスオブジェクトにメッセージを送信した際に起動され、クラスメソッドはクラスオブジェクトにメッセージを送信した際に起動する。なお、インスタンスメソッドとクラスメソッドは全く同じ名前のセレクタを指定して定義できる。

いわゆるコンストラクタは存在しない。慣習として新規オブジェクトの生成は+allocで、初期化は-initで行われるが、プログラマが自由に別の特殊化したメソッドを定義することが可能であり、初期化中に別の初期化メソッドを呼びだす場合もある。一方デストラクタ（ファイナライザ）に相当するものは-dealloc、またはガベージコレクション使用時の-finalizeで、これらのメソッドはオブジェクトの破壊時に必ず呼び出される。

[selfは特殊な変数で](https://ja.wikipedia.org/wiki/this_\(プログラミング\) "wikilink")、メソッドの実行時に自動的にレシーバが代入される。再代入も可能であり、-init等でスーパークラスの実装で自分自身を初期化し、正しい値が返った時のみ継続して初期化を行なうなどに利用される。

オブジェクトの型はオブジェクトを特定のクラスに制限したい時に用いられる。ただしこれはソースコードでのみ意味を持ち、実行レベルでは全てidとして扱われる。また型付きのオブジェクトはインスタンス変数を構造体互換でアクセスできる。保護レベルはpublic（フリー）、protected（継承クラスのみ）、private（同一クラスのみ）があり、デフォルトはprotectedである。ただメモリ管理の一貫性などの理由から、ほとんどの場合[アクセサ](https://ja.wikipedia.org/wiki/アクセサ "wikilink")を用いる。

### 互換性

32bit時代のLinux版GCCではNSObjectクラスではなく、Objectクラスが使用されていた。64bit時代になってからは、かろうじてObjectクラスの定義が残っているものの殆どのメソッドは削除され、かつてのようにNSObjectクラスの代わりに使用することは出来ない。ソースコードレベルでは完全に互換性が失われている。代わりにGNUStepを導入し、ヘッダーとして\#import\<Foundation/NSObject.h\>を記述し、ObjectクラスをNSObjectクラスに変更する必要がある。また、ライブラリの指定も従来の-lobjcだけでは足りず、-lgnustep-baseの指定が必要となる。

## 特徴

### リフレクション

Objective-Cのオブジェクトは全て自分自身に関する定義情報を保持しており、実行時に利用することができる。

#### リフレクションの一部

``` objc
- (BOOL)respondsToSelector:(SEL)aSel;
- (BOOL)isKindOfClass:(Class)cls;
```

### 転送

実装系によるが、存在しないメソッドを呼びだした際、例外を発生する前にそれを他のオブジェクトに転送するチャンスが与えられる。[Message Forwardingと呼ばれる](https://ja.wikipedia.org/wiki/メッセージ転送 "wikilink")。

#### 転送の例

Appleの[ランタイムでは](../Page/ランタイムライブラリ.md "wikilink")、セレクタに対応する引数情報と転送処理の二つの過程を経て行われる。

``` objc
// NSMethodSignatureはメソッドの引数の数や型情報を表すオブジェクト
// Objective-Cのメソッドはスカラー型をとるC関数互換なので正確なスタック情報が必要となる
- (NSMethodSignature*)methodSignatureForSelector:(SEL)sel
{
    id signature = [otherObj methodSignatureForSelector: sel];
    return signature;
}

// NSInvocationはターゲットと引数を持ち、返値を受け取るオブジェクト
// 元のターゲットの代わりに別のターゲットで実行を行なうとあたかもそのオブジェクトにメッセージが送られたかのように動作する

- (void)forwardInvocation:(NSInvocation*)invocation
{
    SEL aSel =  [invocation selector];
    if([otherObj respondsToSelector: aSel])
    {
        [invocation invokeWithTarget: otherObj];
    }
    else
    {
        [self doesNotRecognizeSelector: aSel];
    }
}
```

### プロトコル

プロトコルはクラスのメソッドインターフェースを規定する機構である。元々はNeXTワークステーション上で分散オブジェクトシステムを構成する際、リモートオブジェクトの通信効率を上げるために導入された。

プロトコルに準拠するクラスは定義されたメソッドを全て実装しなければならない。また、プロトコルは多重継承を許す。

#### プロトコルの例

``` objc
// プロトコルを定義する
@protocol MyProtocol <NSObject, NSCopying>
- (void)methodForRespond;
@end

// プロトコルを導入する
@interface MyObject <MyProtocol>
...
@end
```

類似した機構に実装をオプションにできるinformalプロトコルがある。これは後述のカテゴリのうち、インターフェース定義のみを利用する方法で、利用側は実装状態をリフレクションで調査して正当な場合のみ呼びだす。

``` objc
// ここでは「NSObjectにはtransferAcceptable:が定義されている」と宣言している
// 実際には対応する実装を用意する義務がないため、NSObjectを継承したオブジェクトがそれを行なった場合のみ利用できる
@interface NSObject (OptionalMethods)
- (BOOL)transferAcceptable:(id)obj;
@end

- (void)method
{
    id val,obj;
    ...
    if([obj respondsToSelector: @selector(transferAcceptable:)])
    {
        [obj transferAcceptable: val];
        ...
    }
}
```

### カテゴリ

カテゴリは、クラス定義をグループに分割したり、既存のクラスにメソッドを追加したりするための言語機能。Smalltalkが統合開発環境上でクラスとメソッドの表示を整理するために使っている[クラスカテゴリーとメソッドカテゴリー](https://ja.wikipedia.org/wiki/Smalltalk#ファイル用構文 "wikilink")(プロトコルとも言う)をそのまま取り込んだ。

クラスの実装を関連するメソッド群毎に別々の場所に分割して記述することを可能とする目的で作られた。

このほか、カテゴリに宣言したメソッドが実行時にカテゴリがロードされたタイミングでクラスへ追加される、という性質を応用して、ソースコードを直接修正できないクラスに対してサブクラスを定義せずにメソッドを追加する、といった用途や、Informalプロトコルの定義等にも用いられる。

カテゴリメソッドで既存のメソッドをオーバーライドすることも可能であるが、推奨されていない。

#### カテゴリの例

``` objc
@interface NSObject (BetterHash)
- (unsigned)hash;
@end

@implementation NSObject (BetterHash)
// 子孫クラスのうち、独自のオーバーライドのない-hashは全てこの実装に置き換わる
- (unsigned)hash
{
    return better_hash_function(self);
}
@end
```

### その他

#### メタ言語的メカニズム

オブジェクトシステム自体がCで書かれていることに加え、C哲学である「**プログラマにできることを制限しない**」を良くも悪くも受け継いでいるため、Objective-Cにはさまざまな超言語的技法が存在している。これらの機能は非常に強力であるため乱用を避けるべきだが、この柔軟性こそがObjective-Cの魅力と評する向きもある。

  - posing
    クラステーブルを書き換えることでクラスの実体を置き換える技法。
  - method swizzling
    クラスのメソッドテーブルを書き換えることでセレクタ名のリネーミングを行なう技法。
  - IMP呼びだし
    毎回メッセージパッシングを行なう代わりに、一度だけメソッドを解決して関数ポインタを取り出し、メソッドの呼び出しを高速化する技法。呼びだしコストが通常のC関数と等しくなる。俗にインライン化とも呼ばれる。

#### Objective-C++

Objective-CとC++が混在したもの。両者はCからの拡張部分がほぼ干渉しないため、お互いをただのポインタ値と見なすことで表記が混在できる。したがってクラスシステムの互換性はなく、単純なObjective-C & C++になる。拡張子は.mm。

[関数やObjective](../Page/サブルーチン.md "wikilink")-C[メソッドの内部では](../Page/メソッド_\(計算機科学\).md "wikilink")、Objective-CとC++両方の機能を任意に組み合わせて利用することができる。例えば、Objective-Cオブジェクトの寿命を管理する[スマートポインタ](https://ja.wikipedia.org/wiki/スマートポインタ "wikilink")を、C++の機能を用いて作成するようなことが可能である。他方、[クラスの階層はObjective](../Page/クラス_\(コンピュータ\).md "wikilink")-CとC++で完全に分かれており、一方が他方を[継承することは全く不可能である](../Page/継承_\(プログラミング\).md "wikilink")。また、伝統的なObjective-Cの[例外処理](../Page/例外処理.md "wikilink")とC++のそれは互換性がなく、プログラマが両者を逐一捕捉・変換しなければ、[メモリリーク](../Page/メモリリーク.md "wikilink")や[クラッシュにつながる](https://ja.wikipedia.org/wiki/クラッシュ_\(コンピュータ\) "wikilink")。

主な用途はC++のライブラリをObjective-Cからアクセスするためのラッパー記述で、実例としてAppleの[WebKit](../Page/WebKit.md "wikilink")（[KHTML](../Page/KHTML.md "wikilink")ベース）などがある。コンパイル速度が非常に遅くなることもあって積極的に用いられることは少ない。

#### 言語ブリッジ

上述のように、Objective-Cランタイムシステムの実体はC言語関数群そのものである。このライブラリの内部でリフレクションやメッセージ送信の機構が全て閉じているため、これらに対するラッパーを用意することで、外部言語からシステムの完全制御が可能になる。

現在言語ブリッジが確立している言語には、、[Python](../Page/Python.md "wikilink")（[PyObjC](https://ja.wikipedia.org/wiki/PyObjC "wikilink")）、[Ruby](../Page/Ruby.md "wikilink")（）などがある。

#### 処理系の特性

  - Apple/NeXT版
  - GNU版
  - Portable Objective-C版

#### メモリ管理

初期のObjective-CプログラムはC同様単純な割当と解放を行なっていたが、現在は標準APIライブラリに実装された[参照カウント](../Page/参照カウント.md "wikilink")方式のAutorelease poolを利用するのが標準的である。参照カウント方式ではあるが[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")とは異なり、半自動で行なわれる。方法としてはNSAutoreleasePoolクラスをインスタンス化し、ここに解放されるべきオブジェクトを、autoreleaseメッセージを用いて登録する。登録した全てのオブジェクトが不要になったらreleaseメッセージでNSAutoreleasePoolのインスタンスを解放する。すると登録されていたオブジェクトもすべて一斉に解放されるというものである <ref>macやiOSの標準APIでは基底クラスNSObjectに参照カウントを実装してあり、他のクラスがNSObjectを継承している。

  - [Apple IOs API Reference \#NSObject](http://developer.apple.com/library/IOs/documentation/Cocoa/Reference/Foundation/Protocols/NSObject_Protocol/Reference/NSObject.html)（2012年1月20日閲覧）
  - [Apple mac API Reference \#NSObject](http://developer.apple.com/library/mac/documentation/Cocoa/Reference/Foundation/Protocols/NSObject_Protocol/Reference/NSObject.html)（2012年1月20日閲覧）
  - [高度なメモリ管理プログラミングガイド](http://developer.apple.com/jp/devcenter/ios/library/documentation/MemoryMgmt.pdf)
  - 荻原 剛志『Mac OS X プログラミング入門 Objective-C』広文社,2001年,ISBN 4-87778-068-8</ref>。

ほかにもオブジェクト(仮にobjAとする)のイニシャライザ(初期化メソッド)を呼び出すと、その時点で自分をautoreleaseするオブジェクトを定義できる。そのようなオブジェクトをインスタンス化したユーザは、objAに対して明示的にautoreleaseせずとも、NSAutoreleasePoolのインスタンスをreleaseするだけでobjAを解放できることになる。例としてNSStringクラスがある。stringWithCString:で初期化するとautoreleaseされた状態になる。

##### 手動管理の場合

``` objc
int count = 0;
// オブジェクトのインスタンス化
// これら2つは自動的に参照カウントが1になる
id objFoo = [[Foo alloc] init];
id objBar = [[Bar alloc] init];
id baz = objFoo; // Fooを間接参照
id qux = objBar; // Barを間接参照
[baz retain]; // Fooの参照カウントは2になる
// オブジェクトの解放
[objFoo release]; // objFooは解放されるがFooの参照カウントは1で維持される
[objBar release]; // 変数quxはretainしていないのでBarは破棄される
[baz release]; // Fooが解放される
count = [qux retainCount]; // Barの参照カウントを参照する。Barは解放されているのでエラー
```

##### NSAutoreleasePoolの例

``` objc
int count = 0;
// NSAutoreleasePoolのインスタンス化
NSAutoreleasePool *pool = [[NSAutoreleasePool alloc] init];
id objFoo = [[Foo alloc] init];
id objBar = [[Bar alloc] init];
id objBaz = [[Baz alloc] init];
// Autorelease poolに登録
[objFoo autorelease];
[objBar autorelease];
[objBaz autorelease];
// オブジェクトを参照する変数
id qux = objFoo;
id fooBar = objBar;
[qux retain]; // FooのretainCountは2
// Autorelease poolの解放
[pool release];
count = [qux retainCount]; // Fooをretain後オーナーだったobjFooが解放されたので1
count = [fooBar retainCount]; // Barをretainしていないのでエラー
count = [objBaz retainCount]; // ほかの参照がなかったので解放済み。エラー
count = [objBar retainCount]; // fooBarがretainしていなかったのでエラー
```

オーナー(所有者)とは、あるオブジェクトのインスタンスをretainまたはautoreleaseしたオブジェクトないしは変数のことで、上の例で、poolをreleaseする直前ではobjで始まる変数とquxが該当する。

OPENSTEPライブラリは、イベントサイクル単位でAutorelease poolと呼ばれる暗黙の参照元を持っており、オブジェクトをここに登録することでイベント終了時には自動で解放されるオブジェクトを実現している。Macに移植後もNSApplicationクラスに実装されているが、オブジェクトの登録も不要となっている。前述のNSAutoreleasePoolは、NSApplicationクラスが不要なときでも自動解放ができるように用意されたものといえる。

GNU版ランタイム及び、Mac向けのApple版ランタイム(Objective-C 2.0以降)ではガベージコレクションも利用可能だが、iOSに於てはリソースの効率上使用できない。Appleはさらに第三の方式としてARC (Automatic Reference Counting) 方式を開発したため、Apple系では今後この方式が主流になる見込みである。

##### 自動参照カウント (ARC)

自動参照カウントは内部的にはretain/release/autoreleaseと同様のメカニズムで動作するが、コンパイル時にメソッドの命名ルール等を見て自動的にretain/release相当のコードを挿入する方式である。これにより、自動参照カウントでは明示的なretain/releaseがそもそも不可能になる。管理周りのコードの削減に加え、autorelease管理の実行効率が向上するため、旧方式のプログラムを自動参照カウントに切り替えるだけでもパフォーマンスがいくぶん向上する。

## Objective-C 2.0

アップルは[Mac OS X v10.5において](../Page/Mac_OS_X_v10.5.md "wikilink")**Objective-C 2.0**という名称で言語仕様の変更を行った。

  - ガベージコレクションの導入
    世代別の保守的GCを導入し、GC管理下にあるオブジェクトは全てメモリ管理を自動化できる。なお、これに伴い[Core FoundationのオブジェクトもGC管理下に置けるようになった](../Page/Core_Foundation.md "wikilink")。GCモードでは[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")周りの性能が向上するとみられる。
  - プロパティの導入
    [C\#などに採用されているプロパティが追加された](../Page/C_Sharp.md "wikilink")。setter/getterの扱いが大幅に簡略化される。またKey-Value-Codingに関してドット記法が導入され、**obj.propName**のようなアクセスができるようになった。メッセージ送信メタファからは逸脱した感もあるが、元々構造体が同じ記法を用いている上、メッセージ式を正確に書くよりもはるかに記述量が減るため、実利主義のObjective-Cらしい拡張と言える。
  - Fast Enumeration
    いわゆる[foreach文](https://ja.wikipedia.org/wiki/foreach文 "wikilink")の導入。
  - プロトコルの強化
    実装オプションのプロトコル定義が増えた。
  - Class Extensions
    実装をオプションにできない無名カテゴリ。実装必須のプライベートメソッドを（インターフェース的に）公開したくない時に用いる。Objective-Cでは動的ディスパッチを行うので、非公開メソッドでも呼び出しに制限がない点に注意。
  - ランタイム構造の変更
    クラスのposingは廃止された。その代わりにメソッドの交換（セレクタのマッピングを入れ替える）が公式に用意され、カテゴリと組み合わせることでほぼ同じ機能を実現できる。その他にも、ランタイム周りはほとんど原形を留めないほどに手が入っている。

## 脚注

## 参考文献

Objective-Cに関する最初の本であり、Objective-Cを利用したオブジェクト指向システム開発に関する本。

  - *Object Oriented Programming: An Evolutionary Approach; Brad J. Cox, Andrew J. Novobilski; Addison-Wesley Publishing Company, Reading, Massachusetts, 1991; ISBN 0-201-54834-8*
    （邦題:「オブジェクト指向のプログラミング」 ISBN 4-8101-8046-8）

この本はObjective-CのNeXTSTEPでの実装について記述している。NeXTSTEPが明確なターゲットだが、Objective-Cを学習するためのよい入門書となる。

  - *NeXTSTEP Object Oriented Programming and the Objective C Language; Addison-Wesley Publishing Company, Reading, Massachusetts, 1993; ISBN 0-201-63251-9*
    （邦題:「OBJECT-ORIENTED PROGRAMMING AND THE OBJECTIVE-C LANGUAGE（日本語版）」 ISBN 4-7952-9636-7）

多くの実例とともに、Stepstone版とNeXT版のObjective-Cについて、両者の違いを含めて論じている。

  - *Objective-C: Object Oriented Programming Techniques; Lewis J. Pinson, Richard S. Wiener; Addison-Wesley Publishing Company, Reading, Massachusetts, 1991; ISBN 0-201-50828-1*
    （邦題:「OBJECTIVE-C オブジェクト指向のプログラミング」 ISBN 4-8101-8054-9）

Objective-C、C++、Smalltalk、[Object Pascal](../Page/Object_Pascal.md "wikilink")、Javaを比較しながら、オブジェクト指向プログラミングの話題を紹介している。

  - *An Introduction to Object-Oriented Programming; Timothy Budd; Addison-Wesley Publishing Company, Reading, Massachusetts; ISBN 0-201-54709-0*
    （邦題:「オブジェクト指向プログラミング入門」 ISBN 4-8101-8048-4）

## 外部リンク

  - [The Objective-C Programming Language](http://developer.apple.com/documentation/cocoa/Conceptual/ObjectiveC/)（[日本語訳](http://developer.apple.com/jp/documentation/cocoa/Conceptual/ObjectiveC/)）Apple Inc. - Objective-C言語とはどういうものかを知ることができる文書。
  - [ダイナミックObjective-C](http://news.mynavi.jp/column/objc/) - [マイナビニュース](https://ja.wikipedia.org/wiki/マイナビニュース "wikilink")のコラム。

[Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:iOS_(アップル)](https://ja.wikipedia.org/wiki/Category:iOS_\(アップル\) "wikilink")

1.