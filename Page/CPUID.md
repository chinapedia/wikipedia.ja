> この記事は[CPUID](https://ja.wikipedia.org/wiki/CPUID)から翻訳されています。


**CPUID**は、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")の[機械語](../Page/機械語.md "wikilink")命令の一つ（及びそのアセンブリ・ニーモニック）である（[CPU](../Page/CPU.md "wikilink")の識別 (IDentification) の意）。[486の後期のステッピングで導入され](../Page/Intel486.md "wikilink")、[Pentiumで完全に公開された](../Page/Intel_Pentium_\(1993年\).md "wikilink")[1](http://www.intel.com/design/processor/manuals/253668.pdf)。

CPUIDを使用することで、ソフトウェアはプロセッサの形式と機能（例えば、[MMX](https://ja.wikipedia.org/wiki/MMX "wikilink")や[SSEなどの拡張のサポートの有無](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令 "wikilink")）を識別することができる。機械語オペコードは`0FA2h`であり、オペランドとしてEAXレジスタの値でどのような情報を取得するかを指定する。

CPUID命令が使用可能になるまでは、プロセッサの識別には、それぞれの振舞の微妙な違いを利用する難解なテクニックを駆使する必要があった[2](http://www.rcollins.org/ddj/Sep96/Sep96.html)[3](http://lxr.linux.no/source/arch/i386/kernel/head.S?v=1.2.13#L92)（たとえば「PUSH SP」の結果として、PUSHによる変化前と変化後の、どちらの値がプッシュされるか、等）。

## CPUID命令の呼び出し

CPUID命令は、EAXレジスタが暗黙のオペランドであり、それ以外の（明示的な）オペランドは無い。どのような情報を返すべきかを指定する値をEAXレジスタに設定し、CPUID命令を実行する。まず`EAX = 0`でCPUIDを呼び出し、CPUでサポートされている最大のパラメータを取得するべきである。CPUIDの拡張機能情報を取得する場合は、EAXのビット31をセットしてCPUIDを呼び出す。拡張機能情報でサポートされている最大の機能番号を得るためには、`EAX = 8000000h`でCPUIDを呼び出す。

\=== EAX=0: ベンダIDの取得 === これは、CPUベンダのID文字列を返す。12文字のASCII文字列がEBX, EDX, ECXの順序で格納される。基本機能の最大機能番号がEAXに格納される。

既知のCPUベンダのID文字列は以下のとおり：

  - `"AMDisbetter!"` - [AMD K5の初期のエンジニアリングサンプル](https://ja.wikipedia.org/wiki/AMD_K5 "wikilink")
  - `"AuthenticAMD"` - [AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")
  - `"CentaurHauls"` - [セントールテクノロジー](https://ja.wikipedia.org/wiki/セントールテクノロジー "wikilink")
  - `"CyrixInstead"` - [サイリックス](../Page/サイリックス.md "wikilink")
  - `"GenuineIntel"` - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")
  - `"GenuineTMx86"`, `"TransmetaCPU"` - [トランスメタ](https://ja.wikipedia.org/wiki/トランスメタ "wikilink")
  - `"Geode by NSC"` - [ナショナル セミコンダクター](https://ja.wikipedia.org/wiki/ナショナル_セミコンダクター "wikilink")
  - `"NexGenDriven"` - [NexGen](https://ja.wikipedia.org/wiki/NexGen "wikilink")
  - `"RiseRiseRise"` - [Rise Technology](https://ja.wikipedia.org/wiki/Rise_Technology "wikilink")
  - `"SiS SiS SiS "` - [SiS](https://ja.wikipedia.org/wiki/SiS "wikilink")
  - `"UMC UMC UMC "` - [UMC](../Page/UMC.md "wikilink")
  - `"VIA VIA VIA "` - [VIA Technologies](../Page/VIA_Technologies.md "wikilink")

例えば、ベンダIDが"GenuineIntel"の場合、EBXが0x756e6547、EDXが0x49656e69、ECXが0x6c65746eとなる。

``` asm
.section   .data
s0:     .string "Largest Standard Function Number Supported: %i\n"
s1:     .string "Vendor ID: %s\n"
.text
    .global main

    .type   main, @function
main:
    pushq   %rbp
    movq    %rsp, %rbp

    subl    %eax, %eax
    cpuid

    subq    $8, %rsp
    movl    %ebx, (%rsp)
    movl    %edx, 4(%rsp)
    movl    %ecx, 8(%rsp)
    movl    $s0, %edi
    movl    %eax, %esi
    subl    %eax, %eax
    call    printf

    movq    $s1, %rdi
    movq    %rsp, %rsi
    subl    %eax, %eax
    call    printf

    subl    %eax, %eax
    movq    %rbp, %rsp
    popq    %rbp
    ret
```

\=== EAX=1: プロセッサ情報とプロセッサの機能 === これはCPUの[ステッピング](https://ja.wikipedia.org/wiki/ステッピング "wikilink")、モデル、ファミリーをEAXに返す（これはCPUの*シグネチャ*とも呼ばれる）。また、機能フラグをEDXとECXに、追加の機能情報をEBXに返す。

EAXに格納される情報のフォーマットは以下のとおり:

  - 3:0 - ステッピング
  - 7:4 - モデル
  - 11:8 - ファミリー
  - 13:12 - プロセッサタイプ
  - 19:16 - 拡張モデル
  - 27:20 - 拡張ファミリー

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")と[AMDは](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、CPUのファミリーを上記の*ファミリー*と*拡張ファミリー*の合計で表示し、モデルを上記の*モデル*と4ビット左シフトした*拡張モデル*の合計で表示するように提案した。

プロセッサ情報と機能フラグはメーカ個別のものであるが、通常は互換性のためにインテルの値を他のメーカも使用している。

\=== EAX=2: キャッシュとTLBディスクリプタ情報 === これは、キャッシュと[TLBの機能を示すディスクリプタのリストをEAX](https://ja.wikipedia.org/wiki/トランスレーション・ルックアサイド・バッファ "wikilink"), EBX, ECX, EDXレジスタに格納する。

\=== EAX=3: プロセッサ・シリアル・ナンバ === これは、プロセッサのシリアル番号を返す。プロセッサ・シリアル・ナンバは、インテルが[Pentium IIIで導入したが](../Page/Pentium_III.md "wikilink")、プライバシーの懸念のためにこの後のモデルでは実装されていない（PSN機能ビットは常にクリアされている）。[トランスメタ](https://ja.wikipedia.org/wiki/トランスメタ "wikilink")のEfficeonとCrusoeプロセッサはこの機能を提供している。AMDは、この機能をどのCPUにも実装しなかった。

インテルPentium IIIでは、シリアル番号はEDX:ECXレジスタに格納される。トランスメタのEfficeonではEBX:EAXレジスタに、CrusoeではEBXレジスタだけに格納される。

プロセッサ・シリアル・ナンバ機能を使用するためには、[BIOSの設定を有効にする必要があることに注意すべきである](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")。

``` asm
.section   .data
s0:     .string "Processor serial number: %.4hX-%.4hX-%.4hX-%.4hX-%.4hX-%.4hX\n"
.text
    .global main

    .type   main, @function
main:
    pushq   %rbp
    movq    %rsp, %rbp

    movl    $1, %eax
    cpuid

    subq    $4, %rsp
    movl    %eax, (%rsp)
    movq    2(%rsp), %rbx
    movw    %bx, (%rsp)
    movw    %ax, 2(%rsp)

    movl    $3, %eax
    cpuid

    movl    %edx, 4(%rsp)
    movq    6(%rsp), %rax
    movw    %ax, 4(%rsp)
    movw    %dx, 6(%rsp)
    movl    %ecx, 8(%rsp)

    movl    $s0, %edi
    movw    (%rsp), %si
    movw    2(%rsp), %dx
    movw    4(%rsp), %cx
    movw    6(%rsp), %r8w
    movw    8(%rsp), %r8w
    movw    10(%rsp), %r9w
    movw    %r9w, (%rsp)
    subl    %eax, %eax
    call    printf

    subl %eax, %eax
    movq    %rbp, %rsp
    popq    %rbp
    ret
```

\=== EAX=80000000h: サポートする最大拡張機能番号の取得 === 最大の拡張機能番号をEAXに格納する。

\=== EAX=80000001h: 拡張プロセッサ情報とプロセッサの機能 === 拡張機能フラグをEDXとECXに格納する。

\=== EAX=80000002h,80000003h,80000004h: プロセッサブランド文字列 === プロセッサブランド文字列をEAX, EBX, ECX, EDXに格納する。全体で48バイトのNULL終端アスキー文字列のプロセッサブラント文字列を得るために、各パラメータを順番に設定しCPUIDを呼び出す必要がある。

``` asm
.section   .data
s0:     .string "Processor Brand String: %s\n"
.text
    .global main

    .type   main, @function
main:
    pushq   %rbp
    movq    %rsp, %rbp

    subq    $44, %rsp
    movl    $0x80000002, %eax
    cpuid

    movl    %eax, (%rsp)
    movl    %ebx, 4(%rsp)
    movl    %ecx, 8(%rsp)
    movl    %edx, 12(%rsp)
    addq    $16, %rsp

    movl    $0x80000003, %eax
    cpuid

    movl    %eax, (%rsp)
    movl    %ebx, 4(%rsp)
    movl    %ecx, 8(%rsp)
    movl    %edx, 12(%rsp)
    addq    $16, %rsp

    movl    $0x80000004, %eax
    cpuid

    movl    %eax, (%rsp)
    movl    %ebx, 4(%rsp)
    movl    %ecx, 8(%rsp)
    movl    %edx, 12(%rsp)
    subq    $32, %rsp

    movl    $s0, %edi
    movq    %rsp, %rsi
    subl    %eax, %eax
    call    printf

    subl    %eax, %eax
    movq    %rbp, %rsp
    popq    %rbp
    ret
```

\=== EAX=80000005h: 予約 === この機能は使用されていない。

\=== EAX=80000006h: 拡張L2キャッシュ情報 === ECXにL2キャッシュの詳細情報を格納する。2種類の方法で表したキャッシュサイズと、キャッシュとメモリの対応を示すコードを含む。

``` asm
.section   .data
s0:     .string "L2 Cache: %iMB\n"
.text
    .global main

    .type   main, @function
main:
    pushq   %rbp
    movq    %rsp, %rbp

    movl    $0x80000006, %eax
    cpuid

    subl    %edx, %edx
    movl    %ecx, (%rsp)
    movl    2(%rsp), %eax
    movl    $1024, %ecx
    divl    %ecx

    movl    $s0, %edi
    movl    %eax, %esi
    subl    %eax, %eax
    call    printf

    subl %eax, %eax
    movq    %rbp, %rsp
    popq    %rbp
    ret
```

\=== EAX=80000007h: 予約 === この機能は使用されていない。

\=== EAX=80000008h: 仮想アドレスと物理アドレスのサイズ === 最大の仮想アドレスサイズと物理アドレスサイズをEAXに格納する。

## 関連項目

  - [Pentium III: プライバシーに関する論争](https://ja.wikipedia.org/wiki/Pentium_III#第一世代“カトマイ”_\(Katmai\) "wikilink")
  - [CPU-Z](https://ja.wikipedia.org/wiki/CPU-Z "wikilink")、各種のシステム情報を取得するためにCPUIDを使用するウィンドウズユーティリティ

## 外部リンク

  - <http://www.sandpile.org/ia32/cpuid.htm>
  - <http://www.sandpile.org/> -- x86プロセッサの技術的な情報
  - CPUID ガイド:
      - [Intel](http://download.intel.com/design/processor/applnots/24161832.pdf) (PDF)
      - [AMD](http://support.amd.com/us/Processor_TechDocs/25481.pdf) (PDF)
  - Windows プログラム:
      - SIV <http://rh-software.com/>
      - CPUZ <http://www.cpuid.com/>
      - WCPUID <http://hp.vector.co.jp/authors/VA002374/src/download.html>
  - [DOS](../Page/DOS_\(OS\).md "wikilink") プログラム:
      - <http://www.coli.uni-saarland.de/~eric/stuff/soft/specials/cpulevel2007.zip>
      - <http://glstation.free.fr/mine/djgpp/download/cpu.zip>
      - <http://www.volny.cz/rayer/programm/programe.htm> (cpuid.zip)
  - [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") プログラム:
      - <http://www.etallen.com/cpuid.html>
      - <http://www.ka9q.net/code/cpuid/>
      - */proc/cpuinfo*インタフェースは、他の情報とあわせて、CPUIDからの出力を多く表示する
  - [Solaris](../Page/Solaris.md "wikilink")は*/dev/cpu/self/cpuid*インタフェースを提供している
      - <http://blogs.sun.com/JoeBonasera/entry/detecting_hardware_virtualization_support_for>

[Category:X86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:X86アーキテクチャ "wikilink") [Category:機械語](https://ja.wikipedia.org/wiki/Category:機械語 "wikilink")