> この記事は[Pentium F00F バグ](https://ja.wikipedia.org/wiki/Pentium_F00F_バグ)から翻訳されています。


**f00f**("foof"と発音する)は、[Intelの](https://ja.wikipedia.org/wiki/インテル "wikilink")[Pentium](../Page/Intel_Pentium_\(1993年\).md "wikilink")、Pentium [MMX](../Page/MMX.md "wikilink")、Pentium[オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")の、ある世代以前のモデルにある、公開されている設計上の不具合の通称である。問題\[1\]を起こす[機械語](../Page/機械語.md "wikilink")バイト列「f0 0f c7 c8」の先頭2バイトの[16進表現に由来する](../Page/十六進法.md "wikilink")。

Intelはこの問題を「ロック付CMPXCHG8B命令の無効オペランドエラッタ」と呼んでいる\[2\]。

## 内容

問題を起こす機械語コード(f0 0f c7 c8)に対応する[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")表現は以下のようになる。本来はメモリオペランドを指定して使用する前提の命令であり\[3\]、アセンブラによってはエラーとされアセンブルを拒否されるかもしれない。

``` asm
lock cmpxchg8b eax
```

<small>*不具合を引き起こすにはオペランドはレジスタである必要がある。ここでは例示としてeaxをオペランドにしているが、その他のレジスタでもよい。*</small>

*cmpxchg8b*命令は、オペランドとして指定されたアドレスのメモリ上の8byteの領域を取る。この命令を実行すると、*edx:eax*の値とメモリ上の8byte値を比較し、一致したらZフラグをセットするとともに*ecx:ebx*の値をこの8byte領域にストアし、一致しなければZフラグをクリアするとともに8byteのデータを*edx:eax*にロードする（[コンペア・アンド・スワップ](../Page/コンペア・アンド・スワップ.md "wikilink")、詳細はリファレンスマニュアル等を参照）。ただし、この命令の機械語では、命令フォーマット上はオペランドにレジスタも指定することが許容される。そして、レジスタオペランドを指定したcmpxchg8b命令を、lockプレフィクス付で実行すると、この不具合が引き起こされる。

lockプレフィックス\[4\]なしでは、この命令は不正命令例外を引き起こすだけである。即ち、レジスタペア*edx:eax*に格納された8byte=64bitのデータと、指定されたレジスタ、上記の例では*eax*に格納された4byte=32bitのデータの比較は妥当ではないからである。

しかし、lockプリフィックスを付けた場合、以後のメモリアクセスが抑制されるために、プロセッサは不正命令例外ハンドラに移行することができず、この段階でハングアップし以後は一切の命令をせず、割り込みも受け付けなくなってしまう。復旧するにはシステムを再起動しなければならない。

## 対策

この命令は特別な権限を要求せず、特にユーザープロセスの実行中にOSが全く関与できずに発生すると思われたため、当初は重大な問題と考えられた\[5\]。以後、OSでの対策が行われるとともに、プロセッサ側でも対策が行われた。

### オペレーティングシステムでの対応

広く普及していたプロセッサに[エラッタ](https://ja.wikipedia.org/wiki/エラッタ "wikilink")が発見されたことから、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")ベンダは発生条件を検知してクラッシュを防ぐ対策を実装する作業に追われた\[6\]\[7\]。

回避には[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")での対策を要する。例外発生時に、例外ハンドラへのアクセスが、まず[ページフォールト](../Page/ページフォールト.md "wikilink")を発生するようにして、不具合を回避する。

### プロセッサのバグフィクス

[Pentium Pro以降のIntelプロセッサにはこのバグの影響はない](../Page/Pentium_Pro.md "wikilink")。また、最新のIntel Pentium Processor Speficificationもアップデートされ、B2ステッピングではこの問題は修正されている。

## 影響

f00f命令を問題のあるシステム上で実行しても、ハードウェア的なダメージを起こさない。もちろん[ファイルシステム](../Page/ファイルシステム.md "wikilink")や[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")、その他の状況にもよるが、ディスクバッファがフラッシュされていなかったり書込み操作中にドライブに割り込まれたり、とあるアトミックでない操作中に割り込まれたりした状態でこのコードを踏み、フリーズしたならば、データを失うことはあり得る。

f00fバグは一般的に知られたので、この言葉は時々よく似たハードウェア設計ミス、例えばのようなものを指すのにも使われる。

## 脚注 

## 関連項目

  - [Pentium FDIV バグ](../Page/Pentium_FDIV_バグ.md "wikilink")
  - [Cyrix coma bug](https://ja.wikipedia.org/wiki/Cyrix_coma_bug "wikilink")

## 外部リンク

  - [Intel® Pentium® Processor Invalid Instruction Erratum Overview](https://www.intel.com/content/www/us/en/support/articles/000008595/processors.html)

  -
[Category:X86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:X86アーキテクチャ "wikilink") [Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink") [Category:ハードウェアバグ](https://ja.wikipedia.org/wiki/Category:ハードウェアバグ "wikilink") [Category:コンピュータ・フォークロア](https://ja.wikipedia.org/wiki/Category:コンピュータ・フォークロア "wikilink")

1.  OS側で特別の対策をしていないと[プロセッサ](../Page/プロセッサ.md "wikilink")が止まる。
2.
3.
4.  排他制御を指示するもので、同じメモリアドレスに対して2つのプロセッサが競合しないように使われる。
5.
6.
7.