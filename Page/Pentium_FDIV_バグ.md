> この記事は[Pentium FDIV バグ](https://ja.wikipedia.org/wiki/Pentium_FDIV_バグ)から翻訳されています。


**Pentium FDIV バグ**は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[Pentiumプロセッサに含まれていた](../Page/Intel_Pentium_\(1993年\).md "wikilink")、特定の値の除算の結果が誤ったものになる、という[バグ](../Page/バグ.md "wikilink")である。

## 発端

[1994年](../Page/1994年.md "wikilink")[10月30日](../Page/10月30日.md "wikilink")、[リンチバーグ大学](https://ja.wikipedia.org/wiki/リンチバーグ大学 "wikilink")のThomas Nicely教授はPentiumプロセッサの浮動小数点演算ユニットにバグがあることを報告した。その内容は、とある[割り算を行うと非常に小さな量だけ間違った値を返すというものだった](../Page/除法.md "wikilink")。この結果は[インターネット](../Page/インターネット.md "wikilink")を通じて他の人々の手で素早く検証された。そして問題を起こすのがPentiumプロセッサの[x87浮動小数点除算命令であることと](../Page/Intel_8087.md "wikilink")、そのニモニックFDIVから**Pentium FDIV バグ**として知られるようになった。また、別の人々はPentiumが返す結果が引き起こす割り算問題は、100万回に高々61回までしか起こらないことを見つけた（これは、オペランドの色々な値に対して、という意味である。このバグは特定の値に対して必ず起きる）。

この問題はPentiumプロセッサの特定のモデルのみで発生する。120MHz以上のクロックのPentium系プロセッサのモデルには、このバグはない。

## 原因

Pentiumで新たに実装された割り算の回路の設計を誤ったのが原因で計算を誤ることが後に明らかにされた。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[CPU](../Page/CPU.md "wikilink")の除算命令の実行はi486まで、non-restoringなどに見られるような1ステップで1ビットずつ商を求める方式によっていたが、Pentiumでは[SRT法を導入し](https://ja.wikipedia.org/wiki/除算_\(デジタル\)#SRT除算 "wikilink")、1ステップで2ビットずつ商を求めるようにし、除算に要するステップ数を約半分にした。このアルゴリズムでは商を求める際に表を参照するが、その表のエントリの一部が誤っていた。すなわち、表のなかで参照されるエントリは一部であり、それ以外の参照されないエントリについてはゼロを設定したが、実際には参照されるエントリのごく一部についても参照されることがないと誤解し、本来有意な値を設定するべきエントリのうち5個に誤ってゼロが設定された。そのために除算の途中で当該エントリを参照すると以後の演算を誤る。ここから、誤ったエントリを参照する特定の値をFDIV命令のオペランドに与えると必ず演算を誤ることになり、確率的・偶発的に誤りが発生するのではない。

## 当初の対応

この報告によって大論争が巻き起こった。インテルは最初この問題の存在を否定していた。やがて、インテルは問題を認めたが、誤りは重大ではなく、たいていのユーザーには影響がないと主張する一方で、影響があると確認できたユーザーにはプロセッサの交換を行うと表明した。平行して、FDIVと同等の除算を行うルーチンを公開し、エラッタ回避の為にこのルーチンを用いるように求めたが、これはFDIV命令より実行に時間がかかりパフォーマンスに悪影響を及ぼした。

多くの独自の検証によって、このバグはほとんど重要ではなく、たいていのユーザーに対する影響は無視してもよいと分かったが、このインテルの対応は非常に大きな抗議を引き起こした。当時インテルのPentiumに競合する「586」クラスの互換[プロセッサや](../Page/CPU.md "wikilink")[PowerPC](../Page/PowerPC.md "wikilink")の売り込みを図った[IBM](../Page/IBM.md "wikilink")のような企業は、一緒になって非難した。例えば[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が計算を誤る確率はとても小さく隕石に当たるリスクが実質的に無視出来るのと同様であると表現したのに対して、競合他社は隕石の軌道を計算して落ちてくる所に立てば必ず当たると皮肉を込めて非難した。

## 交換

ついにインテルは、要求があればバグのあるPentiumプロセッサをすべて修正品と交換するという、潜在的には非常に大きな損失をこうむる可能性のある対応を申し出た。しかし、このチップ交換を行った顧客は、実際にはほんの少数であったことが判明した。一大企業の広報としてはしばしば陥る悪夢ではあったが、実際にはすでに織り込み済みだと認識され、交換を発表したその日のインテルの株価は上がった。

## 結果

結局インテルは根拠のないリコールをさせられたと言う人もいる。ただ、科学技術計算などでは演算結果がすべてなので、計算を誤る可能性がごく僅かであるとしても万全の信頼をおけないのであれば研究や仕事において致命的である人たちもいたこともまた事実である。前述のようにこのバグをソフトウェア的に回避できるが、引き換えに演算速度が遅くなり、結局以前のプロセッサで実行する方が早くなってPentiumプロセッサを使う意味が全くなくなってしまう。演算精度を重視する顧客は敢えてi486の高ランク品を選んだり、[AMDなど競合他社の製品を選んだりした](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")。この問題はそのような科学技術系などの計算目的でプロセッサを購入した人をインテルが切り捨てるのか、切り捨てないのかという問題でもあった。

[Pentium Pro以後のCPUでは](../Page/Pentium_Pro.md "wikilink")[マイクロコード](https://ja.wikipedia.org/wiki/マイクロコード "wikilink")を修正する手段が盛り込まれている。書き換え可能な[コントロールストア](../Page/コントロールストア.md "wikilink")を持ち、[エラッタが生じた場合には](../Page/正誤表.md "wikilink")[BIOSや](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")[OSのアップデータを介してこれを回避するマイクロコードを提供する](../Page/オペレーティングシステム.md "wikilink")。これにより、CPUの交換によらずにエラッタを回避する。

## 関連項目

  - [Pentium F00F バグ](../Page/Pentium_F00F_バグ.md "wikilink")
  - [ブルン定数](../Page/ブルン定数.md "wikilink") - この計算をPentiumで行わせた過程で、本稿で取り上げたFDIVのバグが発覚した。
  - [ファームウェア](../Page/ファームウェア.md "wikilink")

## 参考文献

  -
## 外部リンク

  - [Thomas R. Nicely's Home Page](http://www.trnicely.net/#PENT) - バグを発見したNicely教授の個人ウェブサイト
  - [Bugs in the Intel Microprocessors](http://www.cs.earlham.edu/~dusko/cs63/fdiv.html) - 原因とともに正確な情報が記されたページ
  - [Ivars Peterson's MathTrek: Pentium Bug Revisited](http://www.maa.org/mathland/mathland_5_12.html)
  - [A Tale of Two Numbers](http://www.mathworks.com/company/newsletters/news_notes/pdf/win95cleve.pdf), by [Cleve Moler](https://ja.wikipedia.org/wiki/Cleve_Moler "wikilink") of [The MathWorks](https://ja.wikipedia.org/wiki/The_MathWorks "wikilink")
      - [さらなる詳細が込められたZIPファイル](http://www.mathworks.com/matlabcentral/fileexchange/loadFile.do?objectId=1666&objectType=file)
  - [FDIV Replacement Program - FDIV Replacement Program Home](http://support.intel.com/support/processors/pentium/fdiv/) - インテル公式サイト
  - [IntelによるSRT法の解説](http://www.intel.com/support/processors/pentium/fdiv/wp/4.htm) - インテル公式サイト
  - [CPU黒歴史 大損失と貴重な教訓を生んだPentiumのバグ](http://ascii.jp/elem/000/000/757/757002/) - CPU黒歴史の中でバグについて取り上げている。

[Category:X86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:X86アーキテクチャ "wikilink") [Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink") [Category:ハードウェアバグ](https://ja.wikipedia.org/wiki/Category:ハードウェアバグ "wikilink")