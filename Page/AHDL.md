> この記事は[AHDL](https://ja.wikipedia.org/wiki/AHDL)から翻訳されています。


**AHDL**は、米[アルテラ](../Page/アルテラ.md "wikilink")社が[CPLD](../Page/CPLD.md "wikilink")や [FPGA](../Page/FPGA.md "wikilink")の[回路設計](https://ja.wikipedia.org/wiki/回路設計 "wikilink")用に策定した[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")の一種である。

LPM（ライブラリ・パラメータ・モジュール）と呼ばれる仕様により、回路構成の厳密な管理がやりやすいという特徴を持つ。

このHDLは、自社及び同業他社である[ザイリンクス](../Page/ザイリンクス.md "wikilink")などが導入している[VHDL](../Page/VHDL.md "wikilink")、[Verilog HDLと競合関係にある](https://ja.wikipedia.org/wiki/Verilog_HDL "wikilink")。しかし採用している製品が限定的であるほか、技術情報が少なく[IPなどの技術資産の蓄積も浅いことから](../Page/IPコア.md "wikilink")、ハードウェア記述言語としてのシェアは低い状況にある。 特に日本国内では、課題として日本語による技術資料がほとんど存在しないため、アルテラ社製FPGAのシェアに反してマイナーな言語とされている。

## 例

    % a simple AHDL up counter, released to public domain 13 November 2006 %
    % [block quotations achieved with percent sign] %
    % like c, ahdl functions must be prototyped %

    % PROTOTYPE:
     FUNCTION COUNTER (CLK)
        RETURNS (CNTOUT[7..0]); %

    % function declaration, where inputs, outputs, and
    bidirectional pins are declared %
    % also like c, square brakets indicate an array %

    SUBDESIGN COUNTER
    (
        CLK     :INPUT;
        CNTOUT[7..0]    :OUTPUT;
    )

    % variables can be anything from flip-flops (as in this case),
    tri-state buffers, state machines, to user defined functions %

    VARIABLE
        TIMER[7..0]: DFF;

    % as with all hardware description languages, think of this
     less as an algorithm and more as wiring nodes together %

    BEGIN
        DEFAULTS

            TIMER[].prn = VCC; %  this takes care of d-ff resets %
            TIMER[].clrn = VCC;
        END DEFAULTS;

        TIMER[].d = TIMER[].q + H"1";
    END;

## 関連項目

  - [ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")

[Category:EDAソフト](https://ja.wikipedia.org/wiki/Category:EDAソフト "wikilink") [Category:ハードウェア記述言語](https://ja.wikipedia.org/wiki/Category:ハードウェア記述言語 "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink") [Category:回路設計](https://ja.wikipedia.org/wiki/Category:回路設計 "wikilink")