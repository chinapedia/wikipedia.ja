> この記事は[Text Editor and Corrector](https://ja.wikipedia.org/wiki/Text_Editor_and_Corrector)から翻訳されています。


**Text Editor and Corrector**（略称：**TECO**）は、1960年代に[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink") (MIT) で開発された[テキストエディタ](../Page/テキストエディタ.md "wikilink")。当初の名称は*\[paper\] **T**ape **E**ditor and **CO**rrector*であった。TECOとその派生エディタは、[vi](https://ja.wikipedia.org/wiki/vi "wikilink")（後に[UNIX](../Page/UNIX.md "wikilink")オペレーティングシステムに搭載）や[Emacs](../Page/Emacs.md "wikilink")エディタが普及する以前は広く使われていた。EmacsはTECOの直系の子孫である（TECO用マクロ集の名称だった）。

## 概要と影響

TECOの構文は複雑であり、テキスト操作の汎用[インタプリタ](../Page/インタプリタ.md "wikilink")型[プログラミング言語](../Page/プログラミング言語.md "wikilink")としても使えるようになっていた。マクロ機能は非常に強力で、今日では[正規表現](../Page/正規表現.md "wikilink")と呼ばれるものと対抗できるマッチング機能を備えていた。ほとんど全ての文字にコマンドが割り当てられており、適当な文字列も（必ずしも有益とは言えないが）TECOプログラムと解釈することができる。当時よく行われたゲームとして、TECOで何かのファイルを編集していて、自分の名前をコマンド列として与えたときに何が起きるかを見てみるというものがあった。

[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")は、当初TECO上で[Emacs](../Page/Emacs.md "wikilink")を実装した。その後、[Multics](../Page/Multics.md "wikilink") Emacsや[GNU Emacsは](../Page/GNU_Emacs.md "wikilink")[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")および[Emacs Lispで実装された](../Page/Emacs_Lisp.md "wikilink")。TECOを有名にしたのは、1964年にMITの[Project MACで実装された](https://ja.wikipedia.org/wiki/Project_MAC "wikilink")[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") [PDP-6](../Page/PDP-6.md "wikilink")上のものである。この実装では画面上に編集対象のテキストが継続的に表示され、対話型のオンラインエディタとして使われた。ただし、これは当初の実装とは異なるし、当初想定された使い方でもない。その後のTECOはDECの端末（[VT100](../Page/VT100.md "wikilink")など）でフルスクリーン表示が可能となった。

TECOはいくつかのオペレーティングシステムやコンピュータで利用可能であった。[PDP-1](../Page/PDP-1.md "wikilink")、[PDP-6](../Page/PDP-6.md "wikilink")および[PDP-10](../Page/PDP-10.md "wikilink")上の[Incompatible Timesharing System](../Page/Incompatible_Timesharing_System.md "wikilink") (ITS)、[PDP-10](../Page/PDP-10.md "wikilink")上の[TOPS-10](../Page/TOPS-10.md "wikilink")および[TOPS-20](../Page/TOPS-20.md "wikilink")などである。DECの各種オペレーティングシステムに対応したバージョンもあり、RT11用バージョンではGT40グラフィックス端末で利用可能だったり、[RSTS/E](https://ja.wikipedia.org/wiki/RSTS/E "wikilink")用バージョンでは一種のオペレーティング環境を提供していて、TECOの中であらゆる操作が可能となっていた。[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")は[コンパック](../Page/コンパック.md "wikilink")を経由してDECを取得しており、現在も[OpenVMS](../Page/OpenVMS.md "wikilink")にはTECOが付属している。

DECがPDP-10向けに配布した派生バージョンは現在もインターネット上で入手可能であり、[MS-DOS](../Page/MS-DOS.md "wikilink")/[Microsoft Windows環境にも](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（部分的に）実装した例がいくつかある。

## 歴史

TECOは[1963年](../Page/1963年.md "wikilink")ごろ、MITのDaniel L. Murphyが[PDP-1](../Page/PDP-1.md "wikilink")向けに開発した。当時彼が使えるPDP-1（2台）は別の部門のもので、これらにプログラムのソースコードを供給するには紙テープを使用する必要があった。一方、[IBM](../Page/IBM.md "wikilink")の[メインフレーム](../Page/メインフレーム.md "wikilink")では[パンチカード](../Page/パンチカード.md "wikilink")にソースコードを1行ずつパンチすることができ、カードの上端には人間が読める内容が印字されるようになっていた。このため、IBMのマシンでプログラムを書く際には、カードを並べ替えたり、削除したり、挿入したりといったことが手作業で可能だった。しかし、紙テープにはそのような機能が一切なく、そこからオンライン編集の必要性が生まれた。

PDP-1用の初期のエディタはExpensive Typewriter（「高価なタイプライタ」）と呼ばれていた。作者はStephen D. Pinerで、[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")としての基本的な機能しか備えておらず、検索・置換機能も持っていなかった。その名称は同じようにPDP-1向けに開発されたColossal Typewriter（「巨大なタイプライタ」）と似たような皮肉である。当時のオンラインエディタは、デバッグ時間を大幅に短縮する手段であった。

TECOはPDP-1をより効率的に活用することを目的としていた。マニュアルを見てみると、[コンソール](../Page/コンソール.md "wikilink")を使ってCPU時間を占有して編集を行うよりも、バッチ的にテキスト編集を行うコマンド列を紙テープで用意して適用することを指向していたことがわかる。つまり、編集対象の紙テープと編集コマンドの紙テープをPDP-1にセットして読み込ませ、TECOを実行して編集結果を再び紙テープに出力する。その後、アセンブラをロードして実行する。この間、オンライン編集による時間の浪費は発生しない。

TECOの当時としては洗練されていた検索機能は、オフラインのFlexowriter端末では行番号が印字されず、編集内容でしか場所を指定できないという事情が影響している。各種ループ機能や条件分岐は、編集コマンドの紙テープで十分な編集機能を発揮するために必要とされたのである（このため、TECOは言語として[チューリング完全](../Page/チューリング完全.md "wikilink")となった）。編集テープをなるべく短くするため、各編集コマンドはなるべく短くなるように設定された。

編集テープは一種のプログラムであり、他のプログラムと同様にデバッグを必要とする。従って、バッチ的な編集という当初の目的は、ちょっとした検索・置換でもさらなるデバッグを要するという問題に陥った。結局、TECOはExpensive Typewriterのようにオンライン編集に使われるようになった（とは言っても、TECOの方が機能が豊富で編集が容易であった）。最初のPDP-1バージョンは画面表示がなく、編集の途中の状態を見るには、編集テープ内に編集対象テキストをコンソールのタイプライタに印字するコマンドを挿入するしかなかった。

## TECO使用例

hello.c というファイルの内容が以下のようになっているとする:

`   int main(int argc, char **argv)`
`   {`
`       printf("Hello world!\n");`
`       return 0;`
`   }`

これについて、"Hello" の代わりに "Goodbye" と表示したいとする。以下はそれを行うときのTECOのセッション例である。"\*" はプロンプト、"$" は ESC のエコー表示である:

    *EBhello.c$$                     バックアップ付きでファイルをリード/ライト・オープン
    *P$$                             最初のページを読み込む
    *SHello$0TT$$                    "Hello" を検索してその行を表示する
        printf("Hello world!\n");    その行
    *-5DIGoodbye$0TT$$               5文字削除して、"Goodbye" を挿入し、その行を表示
        printf("Goodbye world!\n");  修正された行
    *EX$$                            編集結果をファイルにコピーして終了

## TECOコード例

<table>
<thead>
<tr class="header">
<th><p>コード例</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>ER</strong> <em>file</em> <strong>$</strong></p></td>
<td><p>ファイルをリード・オープンする</p>
</td></td>
</tr>
<tr class="even">
<td><p><strong>[</strong><em>q</em> ... <strong>]</strong><em>q</em></p></td>
<td><p>レジスタQ（数、テキスト、コードなどを保持できる）のプッシュとポップ</p></td>
</tr>
<tr class="odd">
<td><p><strong>&lt;</strong> <em>code</em> <strong>&gt;</strong></p></td>
<td><p>繰り返し; 他にも <em>next</em>、<em>break</em>、<em>continue</em> などに相当するコードがある</p></td>
</tr>
<tr class="even">
<td><p><em>n</em> <strong>"X</strong> <em>then-code</em> <strong>|</strong> <em>else-code</em> <strong>'</strong></p></td>
<td><p>if-then-else（Xは条件）</p></td>
</tr>
</tbody>
</table>

## TECOプログラミング言語

プログラミング言語としてのTECOの文法は奇妙だが、非常に強力で、そのクローンは[MS-DOS](../Page/MS-DOS.md "wikilink")や[UNIX](../Page/UNIX.md "wikilink")上でいまだに利用可能である。TECOのコマンドは文字（制御文字もある）であり、プロンプトはアスタリスク ("\*") である。ESCキーを2回押下することでコマンドが完了し、画面にはドル記号 ("$$") で表示される。

## TECOプログラム例

TECOプログラムでは、大文字/小文字は区別されず、空白は無視される。ただし、タブは挿入コマンドであり、無視されない。

### 例 1

バッファ内の各行を行の先頭の文字に従ってソートする。この例では[Goto文](../Page/Goto文.md "wikilink")を使用している。

` !START! j 0aua               ! 先頭にジャンプし、1文字めをレジスタAにロード !`
` !CONT! l 0aub                ! 次の行の1文字めをレジスタBにロード !`
` qa-qb"g xa k -l ga 1uz '     ! A>B なら行を入れ替えて、フラグをレジスタZにセットする !`
` qbua                         ! B を A にロード !`
` l z-."g -l @o/CONT/ '        ! バッファに他の行があれば（CONTに）ループする !`
` qz"g 0uz @o/START/ '         ! 行入れ替えが起きた場合、最初からもう1回行う !`

### 例 2

例1と同じことをするが、[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")を使用している。

` 0uz                             ! 繰り返しフラグをクリア !`
` <j 0aua l                       ! 1文字目をレジスタAにロード !`
` <0aub                           ! 次の行の1文字目をBにロード !`
` qa-qb"g xa k -l ga -1uz '       ! A>B なら、行を入れ替えてフラグをセット !`
` qbua                            ! B を A にロード !`
` l .-z;>                         ! バッファに他の行があればループ !`
` qz;>                            ! 入れ替えが起きたときは最初に戻る !`

### 例 3

TECOで書かれた[Brainfuck](../Page/Brainfuck.md "wikilink")インタプリタの例である。バッファの内容をBrainfuckプログラムとして実行する。

` @^UB#@S/{^EQQ,/#@^UC#@S/,^EQQ}/@-1S/{/#@^UR#.U1ZJQZ\^SC.,.+-^SXQ-^SDQ1J#@^U9/[]-+<>.,/<@:-FD/^N^EG9/;>J30000<0@I//>ZJZUL30000J0U10U20U30U60U7@^U4/[]/@^U5#<@:S/^EG4/U7Q7;`
` -AU3(Q3-91)"=%1|Q1"=.U6ZJ@i/{/Q2\@i/,/Q6\@i/}/Q6J0;'-1%1'>#<@:S/[/UT.U210^T13^TQT;QT"NM5Q2J'>0UP30000J.US.UI<(0A-43)"=QPJ0AUTDQT+1@I//QIJ@O/end/'(0A-45)"=QPJ0AUTDQT-1@I/`
` /QIJ@O/end/'(0A-60)"=QP-1UP@O/end/'(0A-62)"=QP+1UP@O/end/'(0A-46)"=-.+QPA^T(-.+QPA-10)"=13^T'@O/end/'(0A-44)"=^TUT8^TQPJDQT@I//QIJ@O/end/'(0A-91)"=-.+QPA"=QI+1UZQLJMRMB\`
` -1J.UI'@O/end/'(0A-93)"=-.+QPA"NQI+1UZQLJMRMC\-1J.UI'@O/end/'!end!QI+1UI(.-Z)"=.=@^a/END/^c^c'C>`

## 参考文献

  - *TECO pocket guide*. Digital Equipment Corporation, 1978. Order No. AV-D530A-TK. 17 pp. [1](http://zane.brouhaha.com/~healyzh/teco/TecoPocketGuide.html)
  - *TECO 6*. PDP-6 Memo No. 2, Memorandum MAC-M-191, October 29, 1964. [2](http://www.transbay.net/~enf/lore/teco/teco-64.html)

## 関連項目

  - [ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")
  - [テキストエディタの一覧](https://ja.wikipedia.org/wiki/テキストエディタの一覧 "wikilink")
  - [マイクロチップの魔術師](../Page/マイクロチップの魔術師.md "wikilink")

## 外部リンク

  - [Dan Murphy's personal site](http://www.opost.com/dlm/)
  - [Pete Siemsen's TECO collection](http://www.sourceforge.net/projects/teco/)
  - [Tom Almy's TECO page.](http://almy.us/teco.html)
  - [Introduction to the TECO syntax](http://scienceblogs.com/goodmath/2006/09/worlds_greatest_pathological_l_1.php)
  - [TECO Information](http://www.pdp8.net/editors/teco/teco.shtml)

[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:マサチューセッツ工科大学](https://ja.wikipedia.org/wiki/Category:マサチューセッツ工科大学 "wikilink")