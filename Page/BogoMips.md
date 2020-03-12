> この記事は[BogoMips](https://ja.wikipedia.org/wiki/BogoMips)から翻訳されています。


**BogoMips**（"bogus"=「いんちきの」+ [MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")）とは、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")のブート時に[CPU](../Page/CPU.md "wikilink")速度を[ビジーループを使って非科学的に測定した結果である](../Page/ビジーウェイト.md "wikilink")\[1\]。その定義としてよく言われるのは「プロセッサが全く無駄な処理を1秒間に何百万回できるか」である\[2\]\[3\]。

BogoMipsは、あるプロセッサがクロック周波数や[キャッシュの有無から見て妥当な性能を示しているかを判断するのに使える](../Page/キャッシュメモリ.md "wikilink")。異なる種類のCPU間での性能比較には使えない\[4\]\[5\]。

## 歴史

1993年、ラルス・ビルゼニウスが comp.os.linux にLinuxカーネルにBogoMipsが導入された理由を次のように投稿している\[6\]。

> MIPSは Millions of Instructions Per Second（百万命令毎秒）の略だ。プロセッサの速度を求める手段である。そのような測定法の多くと同様、適切に利用されるより乱用されることが多い（異機種のコンピュータ間でMIPS値を正しく比較するのは非常に難しい）。
> BogoMipsは[リーナス自身の発案である](../Page/リーナス・トーバルズ.md "wikilink")。Linuxカーネル 0.99.11（1993年7月11日）はタイミングループを必要としていた（待ち時間が非常に短いのでループする以外のウェイト手段を採用できなかった）。タイミングループはプロセッサの処理速度の違いを較正しなければならない。そこでカーネルでブート時にビジーループを実際に回してみて、そのコンピュータがどの程度の速度かを測定することにした。"Bogo" は "bogus"（いんちきの）に由来し、それが一種のごまかしであることを意味している。BogoMipsの値はプロセッサ速度の一種の指標を与えるが、あまりにも非科学的なので BogoMips 以外に呼び様がない。
> ブート時にその値を表示する理由は2つある。第一にそのコンピュータのキャッシュや加速手段が正しく機能しているかをチェックするのに使える。第二にリーナスはこのニュースを聞いて混乱している人々を見かけたときにくすくす笑うのが大好きである。

## BogoMipsの正しい比較

非常に大まかではあるが、BogoMipsの相対値を計算する式を以下の表で示す。この相対値は**各[CPU](../Page/CPU.md "wikilink")が使用されていた当時の[Linux](../Page/Linux.md "wikilink")でのBogoMips値に基づく**ものである。clock は、そのCPUのクロック周波数。インデックスは、クロック周波数当たりの BogoMips の係数が Intel 386DX と同じCPUを1とした相対値である\[7\]。

| システム                                                                                                                                                             | 相対値           | インデックス         |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- | -------------- |
| [Intel 8088](../Page/Intel_8088.md "wikilink")                                                                                                                   | clock × 0.004 | 0.02           |
| [Intel/AMD 386SX](../Page/Intel_80386.md "wikilink")                                                                                                             | clock × 0.14  | 0.8            |
| [Intel/AMD 386DX](../Page/Intel_80386.md "wikilink")                                                                                                             | clock × 0.18  | 1 (これを 1 とした値) |
| [Motorola 68030](../Page/MC68030.md "wikilink")                                                                                                                  | clock × 0.25  | 1.4            |
| [Cyrix](../Page/サイリックス.md "wikilink")/[IBM](../Page/IBM.md "wikilink") 486                                                                                       | clock × 0.34  | 1.8            |
| Intel [Pentium](../Page/Intel_Pentium_\(1993年\).md "wikilink")                                                                                                   | clock × 0.40  | 2.2            |
| [Intel486](../Page/Intel486.md "wikilink")                                                                                                                       | clock × 0.50  | 2.8            |
| [AMD 5x86](../Page/Am5x86.md "wikilink")                                                                                                                         | clock × 0.50  | 2.8            |
| [MIPS](../Page/ミップス・テクノロジーズ.md "wikilink") [R4000](https://ja.wikipedia.org/wiki/R4000 "wikilink")/R4400                                                         | clock × 0.50  | 2.8            |
| [ARM9](https://ja.wikipedia.org/wiki/ARMアーキテクチャ#ARM9/9E "wikilink")                                                                                              | clock × 0.50  | 2.8            |
| Motorola 8081                                                                                                                                                    | clock × 0.65  | 3.6            |
| [Motorola 68040](../Page/MC68040.md "wikilink")                                                                                                                  | clock × 0.67  | 3.7            |
| [PowerPC](../Page/PowerPC.md "wikilink") 603                                                                                                                     | clock × 0.67  | 3.7            |
| Intel [StrongARM](../Page/StrongARM.md "wikilink")                                                                                                               | clock × 0.66  | 3.7            |
| [NexGen](https://ja.wikipedia.org/wiki/NexGen "wikilink") Nx586                                                                                                  | clock × 0.75  | 4.2            |
| [PowerPC](../Page/PowerPC.md "wikilink") 601                                                                                                                     | clock × 0.84  | 4.7            |
| [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink") [21064/21064A](https://ja.wikipedia.org/wiki/Alpha_21064 "wikilink")                                 | clock × 0.99  | 5.5            |
| [Alpha 21066](https://ja.wikipedia.org/wiki/Alpha_21064 "wikilink")/21066A                                                                                       | clock × 0.99  | 5.5            |
| [Alpha 21164](https://ja.wikipedia.org/wiki/Alpha_21164 "wikilink")/21164A                                                                                       | clock × 0.99  | 5.5            |
| Intel [Pentium Pro](../Page/Pentium_Pro.md "wikilink")                                                                                                           | clock × 0.99  | 5.5            |
| [Cyrix Cx5x86](../Page/Cyrix_Cx5x86.md "wikilink")/[6x86](https://ja.wikipedia.org/wiki/Cyrix_6x86 "wikilink")                                                   | clock × 1.00  | 5.6            |
| Intel [Pentium II](../Page/Pentium_II.md "wikilink")/[III](../Page/Pentium_III.md "wikilink")                                                                    | clock × 1.00  | 5.6            |
| [AMD K7/Athlon](../Page/Athlon.md "wikilink")                                                                                                                    | clock × 1.00  | 5.6            |
| Intel [Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")                                                                                                | clock × 1.00  | 5.6            |
| Intel [Itanium](../Page/Itanium.md "wikilink")                                                                                                                   | clock × 1.00  | 5.6            |
| MIPS [R4600](https://ja.wikipedia.org/wiki/R4600 "wikilink")                                                                                                     | clock × 1.00  | 5.6            |
| [Hitachi](../Page/日立製作所.md "wikilink") SH-4                                                                                                                      | clock × 1.00  | 5.6            |
| [Raspberry Pi (Model B)](https://ja.wikipedia.org/wiki/Raspberry_Pi "wikilink")                                                                                  | clock × 1.00  | 5.6            |
| Intel [Itanium 2](../Page/Itanium.md "wikilink")                                                                                                                 | clock × 1.49  | 8.3            |
| [Alpha 21264](https://ja.wikipedia.org/wiki/Alpha_21264 "wikilink")                                                                                              | clock × 1.99  | 11.1           |
| [VIA Centaur](../Page/VIA_Technologies.md "wikilink")                                                                                                            | clock × 1.99  | 11.1           |
| [AMD K5/K6/K6-2/K6-III](../Page/AMD_K6.md "wikilink")                                                                                                            | clock × 2.00  | 11.1           |
| AMD [Duron](../Page/Duron.md "wikilink")/[Athlon](../Page/Athlon.md "wikilink") XP                                                                               | clock × 2.00  | 11.1           |
| AMD [Sempron](../Page/Sempron.md "wikilink")                                                                                                                     | clock × 2.00  | 11.1           |
| [UltraSparc](../Page/SPARC.md "wikilink") II                                                                                                                     | clock × 2.00  | 11.1           |
| Intel [Pentium MMX](../Page/Intel_Pentium_\(1993年\).md "wikilink")                                                                                               | clock × 2.00  | 11.1           |
| Intel [Pentium 4](../Page/Pentium_4.md "wikilink")                                                                                                               | clock × 2.00  | 11.1           |
| Intel [Pentium M](../Page/Pentium_M.md "wikilink")                                                                                                               | clock × 2.00  | 11.1           |
| Intel [Core Duo](../Page/Intel_Core.md "wikilink")                                                                                                               | clock × 2.00  | 11.1           |
| Intel [Core 2 Duo](../Page/Intel_Core_2.md "wikilink")                                                                                                           | clock × 2.00  | 11.1           |
| Intel [Atom](https://ja.wikipedia.org/wiki/Intel_Atom "wikilink") N455                                                                                           | clock × 2.00  | 11.1           |
| Centaur C6-2                                                                                                                                                     | clock × 2.00  | 11.1           |
| [PowerPC](../Page/PowerPC.md "wikilink") 604/604e/750                                                                                                            | clock × 2.00  | 11.1           |
| Intel [Pentium III Coppermine](https://ja.wikipedia.org/wiki/Pentium_III#第二世代“カッパーマイン”_\(Coppermine\) "wikilink")                                                | clock × 2.00  | 11.1           |
| Intel [Pentium III Xeon](https://ja.wikipedia.org/wiki/Xeon#Pentium_III_Xeon "wikilink")                                                                         | clock × 2.00  | 11.1           |
| [Motorola 68060](../Page/MC68060.md "wikilink")                                                                                                                  | clock × 2.01  | 11.2           |
| Intel [Xeon MP (32-bit)](https://ja.wikipedia.org/wiki/Xeon#Xeon_MP_（NetBurstマイクロアーキテクチャ世代） "wikilink")（[ハイパースレッディング](../Page/ハイパースレッディング・テクノロジー.md "wikilink")） | clock × 3.97  | 22.1           |
| [IBM S390](../Page/System_z.md "wikilink")                                                                                                                       | データが不十分       |                |
| Intel [ARM](../Page/ARMアーキテクチャ.md "wikilink")                                                                                                                    | データが不十分       |                |

BogoMipsの詳細な情報と数百の測定値が [BogoMips Mimi-Howto](http://tldp.org/HOWTO/BogoMips/bogo-list.html) にある。

Linuxカーネル 2.2.14 以降、[キャッシュの設定がBogoMipsの計算前に行われるようになった](../Page/キャッシュメモリ.md "wikilink")。BogoMipsの計算方法は変わっていないので、当時の Pentium 系CPU以降ではBogoMips値が約2倍になっている。このBogoMips値の変化は実際のプロセッサ性能には何の効果もない。

## BogoMIPSの計算

Linuxカーネル (2.6.x) での BogoMips は `/usr/src/linux/init/calibrate.c` というソースファイルで実装されている。Linuxカーネルが使用するタイミングパラメータ `loops_per_jiffy` （Jiffy については[ジフィ](https://ja.wikipedia.org/wiki/ジフィ "wikilink")を参照）を計算で求めている。まず、ソースコードのコメントを示す。

    <nowiki>
     /*
       * A simple loop like
       *  while ( jiffies < start_jiffies+1)
       *    start = read_current_timer();
       * will not do. As we don't really know whether jiffy switch
       * happened first or timer_value was read first. And some asynchronous
       * event can happen between these two events introducing errors in lpj.
       *
       * So, we do
       * 1. pre_start <- When we are sure that jiffy switch hasn't happened
       * 2. check jiffy switch
       * 3. start <- timer value before or after jiffy switch
       * 4. post_start <- When we are sure that jiffy switch has happened
       *
       * Note, we don't know anything about order of 2 and 3.
       * Now, by looking at post_start and pre_start difference, we can
       * check whether any asynchronous event happened or not
       */
    </nowiki>

`loops_per_jiffy` は`udelay`関数（μ秒単位の遅延）と`ndelay`関数（ナノ秒単位の遅延）の実装で使われている。これらの関数は一部のドライバがハードウェアを待つのに必要としている。これらは[ビジーウェイト](../Page/ビジーウェイト.md "wikilink")を採用しているので、使用するとカーネルは実質的にブロックされる。i386アーキテクチャの場合 `/usr/src/linux/arch/i386/lib/delay.c` にて `delay_loop` が次のように実装されている。

``` c
/* simple loop based delay: */
static void delay_loop(unsigned long loops)
{
  int d0;

  __asm__ __volatile__(
    "\tjmp 1f\n"
    ".align 16\n"
    "1:\tjmp 2f\n"
    ".align 16\n"
    "2:\tdecl %0\n\tjns 2b"
    :"=&a" (d0)
    :"0" (loops));
}
```

これをCの擬似コードで書き直すと、次のようになる。

``` c
static void delay_loop(long loops)
{
  long d0 = loops;
  do {
    --d0;
  } while (d0 >= 0);
}
```

BogoMipsのさらなる詳細と（ほとんどが古いが）数百のBogoMips値が BogoMips mini-Howto\[8\] にある。

## 脚注

## 外部リンク

  - [BogoMips についてのよくある質問](http://linuxjf.sourceforge.jp/JFdocs/BogoMips/faq.html)
  - [BogoMips Mini-Howto, V38](http://www.clifton.nl/index.html?bogomips.html)（英語）
  - [The Jargon File: BogoMIPS](http://www.catb.org/~esr/jargon/html/B/BogoMIPS.html)（英語）
  - [BogoMips cpu rate](http://bogomips.ru)

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:ベンチマーク](https://ja.wikipedia.org/wiki/Category:ベンチマーク "wikilink")

1.
2.  [エリック・レイモンド](../Page/エリック・レイモンド.md "wikilink")とジェフ・マッケンジーが1990年代初めごろ[インターネット](../Page/インターネット.md "wikilink")で発言したが、起源は追跡不能。
3.
4.
5.
6.
7.
8.