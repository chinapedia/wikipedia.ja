> この記事は[IOCCC](https://ja.wikipedia.org/wiki/IOCCC)から翻訳されています。


**The International Obfuscated C Code Contest**（**IOCCC**, 国際難読化\[1\]Cコードコンテスト）は、故意に難解な[C言語](../Page/C言語.md "wikilink")のプログラムを書き、その読みにくさと[複雑さ](https://ja.wikipedia.org/wiki/複雑さ "wikilink")を競うという[ハッカー](../Page/ハッカー.md "wikilink")の[奇祭](https://ja.wikipedia.org/wiki/奇祭 "wikilink")（[プログラミングコンテスト](https://ja.wikipedia.org/wiki/プログラミングコンテスト "wikilink")）である。

## 概要

一般的に読みにくいコードであれば評価が高いが、目にした瞬間のインパクトや、コードの汚さに反して実行結果の美しさなど、さまざまな要因でアーティスティックなものが選ばれる。多くの作品は一見するとC言語のコードに見えず、コード全体が[アスキーアート](../Page/アスキーアート.md "wikilink")になっているものなどが典型的である。

公式サイトでは、大会の理念は次のように説明されている。

  - 大会ルールの元で最高に意味不明/難解なCプログラムを書くこと
  - 皮肉なやり方で[プログラミング作法](../Page/プログラミング作法.md "wikilink")の重要性を訴えること
  - 普通書かないコードを用いてCコンパイラに負荷をかけること
  - C言語の持つ、ある種の神秘性を解き明かすこと
  - 粗雑なCコードに関して邪魔の入らない公開討論の場を提供すること

第一回大会は1984年に行われ、以降2006年まで年1回のペースで入賞者が発表された。2007年から2010年の間は開催されなかったが、2011年から再開され、進行に前後は見られるもののだいたい年1回のペースで2014年まで開催されている。[Perl](../Page/Perl.md "wikilink")作者の[ラリー・ウォール](../Page/ラリー・ウォール.md "wikilink")や[KornShell](../Page/KornShell.md "wikilink")作者のなどの著名な業界関係者も参加している。

このようなコンテストを開催しようと思ったきっかけは、初期の開催者[Landon Curt NollとLarry](https://ja.wikipedia.org/wiki/w:Landon_Curt_Noll "wikilink") Basselが、[Bourne Shellのソースコード](../Page/Bourne_Shell.md "wikilink")\[2\]と、初期の[BSD](../Page/BSD.md "wikilink")のfinger（[w:Finger protocol](https://ja.wikipedia.org/wiki/w:Finger_protocol "wikilink")）のソースコードを見たことだという\[3\]。

## コードの例

  - 1987年「Best One Liner」受賞、デビッド・コーン作。

<!-- end list -->

``` c
main() { printf(&unix["\021%six\012\0"],(unix)["have"]+"fun"-0x60);}
```

  -
    説明：一見コンパイルが通らないように見えるが、上記コードは正常にコンパイルされ、実行すると「unix」と表示される。UNIX上でコンパイルした場合トークンunixが1としてマクロ定義(\#define unix 1)されており、配列要素のアクセス方法で配列と添字が交換可能である\[4\]ことなどのテクニックを利用している。

下記の例は1988年の大会にエントリーされた、[円周率](https://ja.wikipedia.org/wiki/円周率 "wikilink")を計算するプログラムである: \[5\]\[6\]

``` c
#define _ -F<00||--F-OO--;
int F=00,OO=00;main(){F_OO();printf("%1.3f\n",4.*-F/OO/OO);}F_OO()
{
            _-_-_-_
       _-_-_-_-_-_-_-_-_
    _-_-_-_-_-_-_-_-_-_-_-_
  _-_-_-_-_-_-_-_-_-_-_-_-_-_
 _-_-_-_-_-_-_-_-_-_-_-_-_-_-_
 _-_-_-_-_-_-_-_-_-_-_-_-_-_-_
_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_
_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_
_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_
_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_
 _-_-_-_-_-_-_-_-_-_-_-_-_-_-_
 _-_-_-_-_-_-_-_-_-_-_-_-_-_-_
  _-_-_-_-_-_-_-_-_-_-_-_-_-_
    _-_-_-_-_-_-_-_-_-_-_-_
        _-_-_-_-_-_-_-_
            _-_-_-_
}
```

(なお、上のプログラムはK\&RのCでは動作するが、ANSI Cでは修正しないと動作しない\[7\].)

次のものは1998年の大会で優勝した、フライトシミュレータのプログラムである\[8\] :

``` c
#include                                     <math.h>
#include                                   <sys/time.h>
#include                                   <X11/Xlib.h>
#include                                  <X11/keysym.h>
                                          double L ,o ,P
                                         ,_=dt,T,Z,D=1,d,
                                         s[999],E,h= 8,I,
                                         J,K,w[999],M,m,O
                                        ,n[999],j=33e-3,i=
                                        1E3,r,t, u,v ,W,S=
                                        74.5,l=221,X=7.26,
                                        a,B,A=32.2,c, F,H;
                                        int N,q, C, y,p,U;
                                       Window z; char f[52]
                                    ; GC k; main(){ Display*e=
 XOpenDisplay( 0); z=RootWindow(e,0); for (XSetForeground(e,k=XCreateGC (e,z,0,0),BlackPixel(e,0))
; scanf("%lf%lf%lf",y +n,w+y, y+s)+1; y ++); XSelectInput(e,z= XCreateSimpleWindow(e,z,0,0,400,400,
0,0,WhitePixel(e,0) ),KeyPressMask); for(XMapWindow(e,z); ; T=sin(O)){ struct timeval G={ 0,dt*1e6}
; K= cos(j); N=1e4; M+= H*_; Z=D*K; F+=_*P; r=E*K; W=cos( O); m=K*W; H=K*T; O+=D*_*F/ K+d/K*E*_; B=
sin(j); a=B*T*D-E*W; XClearWindow(e,z); t=T*E+ D*B*W; j+=d*_*D-_*F*E; P=W*E*B-T*D; for (o+=(I=D*W+E
*T*B,E*d/K *B+v+B/K*F*D)*_; p<y; ){ T=p[s]+i; E=c-p[w]; D=n[p]-L; K=D*m-B*T-H*E; if(p [n]+w[ p]+p[s
]== 0|K <fabs(W=T*r-I*E +D*P) |fabs(D=t *D+Z *T-a *E)> K)N=1e4; else{ q=W/K *4E2+2e2; C= 2E2+4e2/ K
 *D; N-1E4&& XDrawLine(e ,z,k,N ,U,q,C); N=q; U=C; } ++p; } L+=_* (X*t +P*M+m*l); T=X*X+ l*l+M *M;
  XDrawString(e,z,k ,20,380,f,17); D=v/l*15; i+=(B *l-M*r -X*Z)*_; for(; XPending(e); u *=CS!=N){
                                   XEvent z; XNextEvent(e ,&z);
                                       ++*((N=XLookupKeysym
                                         (&z.xkey,0))-IT?
                                         N-LT? UP-N?& E:&
                                         J:& u: &h); --*(
                                         DN -N? N-DT ?N==
                                         RT?&u: & W:&h:&J
                                          ); } m=15*F/l;
                                          c+=(I=M/ l,l*H
                                          +I*M+a*X)*_; H
                                          =A*r+v*X-F*l+(
                                          E=.1+X*4.9/l,t
                                          =T*m/32-I*T/24
                                           )/S; K=F*M+(
                                           h* 1e4/l-(T+
                                           E*5*T*E)/3e2
                                           )/S-X*d-B*A;
                                           a=2.63 /l*d;
                                           X+=( d*l-T/S
                                            *(.19*E +a
                                            *.64+J/1e3
                                            )-M* v +A*
                                            Z)*_; l +=
                                            K *_; W=d;
                                            sprintf(f,
                                            "%5d  %3d"
                                            "%7d",p =l
                                           /1.7,(C=9E3+
                              O*57.3)%0550,(int)i); d+=T*(.45-14/l*
                             X-a*130-J* .14)*_/125e2+F*_*v; P=(T*(47
                             *I-m* 52+E*94 *D-t*.38+u*.21*E) /1e2+W*
                             179*v)/2312; select(p=0,0,0,0,&G); v-=(
                              W*F-T*(.63*m-I*.086+m*E*19-D*25-.11*u
                               )/107e2)*_; D=cos(o); E=sin(o); } }
```

このプログラムは下にあげたLinuxのコマンドラインの命令でコンパイルできる。

    cc banks.c -o banks -DIT=XK_Page_Up -DDT=XK_Page_Down \
        -DUP=XK_Up -DDN=XK_Down -DLT=XK_Left -DRT=XK_Right \
        -DCS=XK_Return -Ddt=0.02 -lm -lX11 -L/usr/X11R6/lib

## 脚注

## 参考文献

  - \- 原著（[The new Hacker's dictionary](../Page/ジャーゴンファイル.md "wikilink")）第2版の翻訳。

      - \- 原著（[The new Hacker's dictionary](../Page/ジャーゴンファイル.md "wikilink")）第3版の翻訳。

  -
## 関連項目

  - [プログラミング作法](../Page/プログラミング作法.md "wikilink")
  - [可読性](https://ja.wikipedia.org/wiki/可読性 "wikilink")
  - [難読化コード](https://ja.wikipedia.org/wiki/難読化コード "wikilink")
  - [難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")
  - [Obfuscated Perl Contest](https://ja.wikipedia.org/wiki/:en:Obfuscated_Perl_Contest "wikilink")
  - [国際難読javascriptコードコンテスト](https://ja.wikipedia.org/wiki/国際難読javascriptコードコンテスト "wikilink")

## 外部リンク

  - [大会公式サイト](https://www.ioccc.org)

[Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:プログラミングコンテスト](https://ja.wikipedia.org/wiki/Category:プログラミングコンテスト "wikilink") [Category:ユーモアの賞](https://ja.wikipedia.org/wiki/Category:ユーモアの賞 "wikilink")

1.  [難読化コード](https://ja.wikipedia.org/wiki/難読化コード "wikilink")に変換するツールを指すobfuscatorなどと同義の「obfuscate」で、「邪悪な」などと意訳されることもある（『Life with UNIX』の日本語版など）。[Perl](../Page/Perl.md "wikilink")による同様のコンテストである[:en:Obfuscated Perl Contestは](https://ja.wikipedia.org/wiki/:en:Obfuscated_Perl_Contest "wikilink")、時事ネタ（[竹下登\#内閣総理大臣](https://ja.wikipedia.org/wiki/竹下登#内閣総理大臣 "wikilink")の「言語明瞭・意味不明瞭」）から「言語不明瞭Perlコンテスト」と訳された[1](http://twitter.com/yoshiyuki_kondo/status/171591102510538752)。なお「Perlは普通に書いても難読になるからコンテストが必要ない」というハッカージョークがある。
2.  Bourne Shellのソースコード（ <http://minnie.tuhs.org/cgi-bin/utree.pl?file=V7/usr/src/cmd/sh> ）はマクロ（ <http://minnie.tuhs.org/cgi-bin/utree.pl?file=V7/usr/src/cmd/sh/mac.h> ）を使用した「[ALGOL](../Page/ALGOL.md "wikilink")のような見た目のC」で書かれていることで悪名高い
3.  [IOCCCのFAQ](http://www.ioccc.org/faq.html)の「Q: How did the IOCCC get started?」に対する回答より
4.  Cコンパイラでは、配列aと添字iに対してa\[i\]は\*(a+i)として解釈される。そのためi\[a\]と書いても同じ結果が得られる。コード例では1\["have"\]は"have"\[1\]と等価であり、結果は'a'である。
5.  [5th International Obfuscated C Code Contest, 1988 - westley.c](http://www0.us.ioccc.org/years.html#1988)
6.  [レイモンド(1995)](https://ja.wikipedia.org/wiki/#レイモンド1995 "wikilink") p.353
7.  using gcc, compile with the following command line: `gcc -traditional-cpp -o r r.c` or `gcc -E r.c | sed 's/- -/--/g' > r2.c ; gcc -o r2 r2.c` (The source file is `r.c`)
8.  [IOCCC Flight Simulator](http://www.aerojockey.com/software/ioccc/index.html)