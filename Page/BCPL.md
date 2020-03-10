> この記事は[BCPL](https://ja.wikipedia.org/wiki/BCPL)から翻訳されています。


**BCPL** (Basic Combined Programming Language、*Basic-CPL*)は[1966年](../Page/1966年.md "wikilink")に[ケンブリッジ大学](../Page/ケンブリッジ大学.md "wikilink")の(*Martin Richards*)が設計した[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。

## 歴史

BCPLは元々ほかの言語を開発するために記述された[コンパイラ](../Page/コンパイラ.md "wikilink")\[1\]であり、90年代以降は利用されていない。しかしながらBCPLは[B言語](../Page/B言語.md "wikilink")の基礎となっており、B言語から派生した[C言語](../Page/C言語.md "wikilink")は文法的にBCPLの亜種であるといえるため、その影響は現在にも色濃く残されている。

BCPLは世界初の弓カッコ『{}』を文法規則に利用した言語であるとされる。最初のBCPLのマニュアルには弓カッコについての記述はなく$(と$)が用いられているが、後にTX-2に移植されたBCPLでは弓カッコが使われており、そのことを記述したマニュアルはB言語の開発時期よりも古いものである\[2\]\[3\]。さらに、このマニュアルは第2版であり、第1版時点で弓カッコが使われていれば、その起源はさらに古いことになる。 なお、弓カッコはB言語やC言語から逆に影響されてBCPLに導入されたものであるとC言語の作者であるリッチーは示唆しているが\[4\]、上記の時間的前後関係からそのようなことはありえず、これはリッチーが参照しているBCPLのマニュアルがTX-2版よりもさらに古い最初のものであったことに基づく誤解である。弓カッコの採用において、BCPLとB言語の間に関連性があったかどうかは完全には判明していないが、B言語の開発時点で、開発者であるトンプソンやリッチーはTX-2版BCPLを知らなかった可能性が高く、当時使用されていたテレタイプ端末の制約によって偶然に一致した可能性がある\[5\]\[6\]。

C言語では採用されなかったBCPLの//による単一行のコメントは[C++](../Page/C++.md "wikilink")や後の[C99](../Page/C99.md "wikilink")で再び採用された。

BCPLは1960年代初頭に開発された複雑な[CPLを簡単にしたものである](../Page/CPL_\(プログラミング言語\).md "wikilink")。リチャーズは「コンパイルを難しくする特徴を仕様から削る」ことによりBCPLを開発した。[CTSS](../Page/CTSS.md "wikilink")で動作する[IBM 7094用の最初のコンパイラの実装は](../Page/IBM_7090.md "wikilink")、1967年の春にリチャーズが[MITの](../Page/マサチューセッツ工科大学.md "wikilink")[Project MACを訪問している間に書かれた](https://ja.wikipedia.org/wiki/Project_MAC "wikilink")。1969 Spring Joint Computer Conferenceの論文で初公開された。

BCPLはクリーンでパワフルで移植性が高かった。そのため小さくて単純なコンパイラを記述することが可能であった。コンパイラが16KBの[メモリで動作すると言われた](../Page/主記憶装置.md "wikilink")。しかもリチャーズのコンパイラはそれ自身がBCPLで記述されており、非常に移植性が高かった。そのためBCPLは処理系の[ブート用として人気のある選択肢だった](../Page/ブートストラップ問題.md "wikilink")。

コンパイラの移植性についての主な理由はその構造にあった。コンパイラは2つのパーツに分けられていた。フロントエンドはソースをパースし、[仮想機械](../Page/仮想機械.md "wikilink")用のO-codeを生成した。バックエンドはO-codeを受け取り、ターゲットマシンのコードに変換した。新しいマシンをサポートするためにはコンパイラのコードの1/5だけを書き直せばよく、通常は2～5人月の作業であった。その後まもなくこの構造はごく一般的になった（[Pascal](../Page/Pascal.md "wikilink")及び[Java](https://ja.wikipedia.org/wiki/Java "wikilink")参照）が、この目的のためにバーチャルマシンを定義したのはリチャーズのBCPLコンパイラが世界初である。

1種類のデータ型（1[ワード](../Page/ワード.md "wikilink")は通常[アーキテクチャのマシンワードのアラインの固定ビット長であり](https://ja.wikipedia.org/wiki/コンピュータアーキテクチャ "wikilink")、またアドレスを示す適切なサイズのポインタ）だけしか持たないBCPLは特殊な言語といえる。当時は1ワードが8ビットではないコンピュータがほとんどであった。アドレス可能なメモリの最小単位がワードではなく[バイトであるマシンや](../Page/バイト_\(情報\).md "wikilink")、より大きなメモリ空間を使用できるアドレス長が32bitまたは64bitのマシンでBCPLを利用する際に、この選択は問題があったということが後に判明した。

全ての値の判断は値を処理するのに利用した[演算子](../Page/演算子.md "wikilink")によって決定された（例えば+は2つの値を両方とも整数として加算し、\!は値から間接的に参照して[ポインタとして扱う効果があった](../Page/ポインタ_\(プログラミング\).md "wikilink")。）。この働きにより実装はタイプチェックを提供しなかった。[ハンガリアン記法](../Page/ハンガリアン記法.md "wikilink") (Hungarian Notation)はプログラマーが予期せぬタイプエラーを回避するために開発された。

ワード指向のBCPLとバイト指向のハードウェアのミスマッチについては様々な方法で解決を試みられた。その1つはバイト列の中にワードを出し入れする標準ライブラリルーチンの提供だった。ビットフィールドセクション演算子と、（'%'文字で示す）[中置記法](../Page/中置記法.md "wikilink")のバイト間接参照演算子の2つの言語機能が後に付け加えられた。

BCPLは独自の方法で翻訳単位を超えるシンボルのバインディングを扱う。BCPLはユーザー定義型のグローバル変数を持たない。その代わりに[FORTRAN](../Page/FORTRAN.md "wikilink")の"blank common"に似たグローバルベクタがある。翻訳単位を超えて共有する全てのデータは、スカラーと、グローバルベクタに事前に配置したベクタへのポインタで構成される。ヘッダファイル（GET命令を使ってコンパイル時に読み込まれるファイル）は翻訳単位間でグローバルデータを同期させる重要な手段であり、GLOBAL命令を使用してシンボル名とワードアドレスの組み合わせたシンボル情報のリストをヘッダファイルに記述する。グローバルベクタは変数だけでなく外部関数へのバインディングにも使用する。これにより翻訳単位の動的なロードを容易に達成できる。基本ともいえるリンカに頼らないためBCPLではプログラマがリンクのプロセスを制御できる。

BCPLは最初の**[Hello world](../Page/Hello_world.md "wikilink")**プログラムが記述された言語であるといわれている。最初の[MUD](../Page/MUD.md "wikilink")もまたBCPLによって記述された[1](http://www.mudconnect.com/mud_intro.html)。

[TRIPOS](https://ja.wikipedia.org/wiki/TRIPOS "wikilink")や、起動 (Kickstart)処理、AmigaDOS初期バージョンを含む[AmigaOS](../Page/AmigaOS.md "wikilink")のコア部分など、いくつかのオペレーティングシステムではその一部または全体がBCPLで記述された。またBCPLは影響力の強い[パロアルト研究所](../Page/パロアルト研究所.md "wikilink")の[Alto](../Page/Alto.md "wikilink")-最初の近代的なパーソナルコンピューターのプロジェクト-で最初に使われた言語であり、その他の数多くの有力なプロジェクトの間では、初期のBravoドキュメント調合システム (document preparation system)がBCPLで記述された。

1970年までには、[ハネウェル635/645](../Page/GE-600シリーズ.md "wikilink")、[IBM 360](https://ja.wikipedia.org/wiki/System/360 "wikilink")、[TX-2](../Page/TX-0.md "wikilink")、CDC 6400、Univac 1108、[PDP-9](../Page/PDPシリーズ.md "wikilink")、KDF 9、Atlas 2に実装されていた。1979年には少なくとも25のアーキテクチャで実装された。2001年現在ではほとんど使われないようだ。

BCPLの哲学は書籍「*BCPL, the language and its compiler*」からの引用によって端的に示される。

  -
    *BCPLの哲学は、最良を知ると皆が考える暴君がいるのではなく、何が許されて何が許されないのかという決まりが定められているのでもない。どちらかといえばBCPLは、たとえ明らかに馬鹿げた事態に直面したときでさえ、不平を言わずに自らの能力を最大限に活かしてサービスを提供せんとする召使いとして振舞う。彼が何をしていて、細かい制限に制約されないということを、プログラマーは常に理解しているものと考える。*

BCPLの設計と哲学は後に[C言語](../Page/C言語.md "wikilink")に影響を与える[B言語](../Page/B言語.md "wikilink")に多大な影響を与えた。C言語は現在システムプログラミング用言語の1つである。

## プログラム例

n以下の[素数](../Page/素数.md "wikilink")を求めるプログラム。

    //
    // n以下の素数を求める
    //
    GET "LIBHDR"

    LET START() BE
    $(
        LET I, J, N

        WRITEF("N=")
        N := READN()

        FOR I=2 TO N DO
        $(
            FOR J=2 TO I-1 DO
            $(
                IF I REM J = 0 DO
                    BREAK
            $)
            IF I=J DO
                WRITEF("%N*N", I)
        $)
    $)

## 脚注

<references />

## 外部リンク

  - [Martin Richards](http://www.cl.cam.ac.uk/~mr10/)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.  「BPL - コンパイラ記述とシステムプログラミングのためのツール」　Martin Richards講演、Spring Jointコンピューターカンファレンス議事録 1969年 Vol 34 557～566頁
2.  <http://bitsavers.trailing-edge.com/pdf/mit/tx-2/TX-2_BCPL_Reference_Manual_May69.pdf>
3.  PDP-7版UNIXの開発は1969年の夏にトンプソンの妻が帰省している間に行われており(https://spectrum.ieee.org/tech-history/cyberspace/the-strange-birth-and-long-life-of-unix 参照)、B言語の開発は、PDP-7版UNIXが完成した以降のことであるため、TX-2版BCPLのマニュアルが書かれた時期より後であることが確認できる。
4.  <https://www.bell-labs.com/usr/dmr/www/bcpl.html>
5.  <https://www.wizforest.com/diary/1602.html#ID6>
6.  <https://www.wizforest.com/diary/160213.html>