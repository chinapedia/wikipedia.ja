> この記事は[VHDL](https://ja.wikipedia.org/wiki/VHDL)から翻訳されています。


**VHDL**は、[デジタル回路](../Page/デジタル回路.md "wikilink")設計用の、[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")(HDL: Hardware Description Language)の一種である。標準化は（現在は）IEEE/IECによる。主として[論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")の設計に、特に[FPGA](../Page/FPGA.md "wikilink")や[ASIC](../Page/ASIC.md "wikilink")などの設計で使う。IEEEとIECで同一規格[IEEE](../Page/IEEE.md "wikilink") 1076-2008 VHDL Language Reference Manual/IEC 61691-1-1:2011 Behavioural languages - Part 1-1: VHDL Language Reference Manual を発行している。名前の由来は英語のVHSIC HDLの略で、VHSICは、very high speed integrated circuits(超高速集積回路)である。

## 歴史

米国[国防総省](https://ja.wikipedia.org/wiki/国防総省 "wikilink")は、業者の納品する機器で含む[ASIC](../Page/ASIC.md "wikilink")の動作の文書記述のためにVHDLを開発した。すなわち、分厚く複雑になりがちな紙のマニュアルの代替を目指したのが始まりである。

全般に、同じく米国防総省のプログラミング言語である[Ada](../Page/Ada.md "wikilink")の影響が大きく、その構文は（Adaと同じく）いわゆる「[ALGOL](../Page/ALGOL.md "wikilink")系」である。規格では、ケース・インセンシティブ（大文字、小文字の区別をしない）としている。

この文書作成用言語で書いた仕様がそのまま実行できたら便利であろうとのアイデアにより、論理([シミュレータ](https://ja.wikipedia.org/wiki/シミュレータ "wikilink"))が実装され、さらにゲートレベルの回路を生成する[論理合成](../Page/論理合成.md "wikilink")ツール（ソフトウェア）が実装された。合成ツールを用いれば、他のHDLと同様、同じVHDL記述から設計者の指定する条件で別の回路を合成することもできる。費用を優先するか、性能を優先するか、その他各種の複合条件を指定して生成することができる。

VHDLの最初のバージョンは[IEEE](../Page/IEEE.md "wikilink") 1076-1987として規格化した。[整数](../Page/整数.md "wikilink")、[実数](../Page/実数.md "wikilink")、論理値、文字、時間およびそれらの配列として`bit_vector`や`string`([文字列](../Page/文字列.md "wikilink"))など広範囲なデータ型がある。

しかしこのバージョンでは[多値論理](../Page/多値論理.md "wikilink")を定義していない。信号のドライブ能力や不定値を考慮した9値の`std_logic`を定め、IEEE 1164として規格化した。

その後、IEEE 1076-1993\[1\]、IEEE 1076-2000\[2\]、IEEE 1076-2002\[3\]、IEEE 1076-2008\[4\] と改定し、IECが同一規格を発行するようになった。[WTO/TBT協定で](https://ja.wikipedia.org/wiki/貿易の技術的障害に関する協定 "wikilink")、国際取引の技術基準は国際規格を尊重することになっているため、IECの規格文書として発行することに合意したものである。

## コード例

ここではVHDL-93に準拠したコードを示す。

### [Hello World](../Page/Hello_world.md "wikilink")

Hello Worldプログラム例:

``` vhdl
-- VHDL example programme: hello.vhd

use std.textio.all;

entity hello is
end entity hello;

architecture Wiki of hello is

    constant message : string := "hello world";

begin

    process is
        variable L: line;
    begin
        write(L, message);
        writeline(output, L);
        wait;
    end process;

end architecture Wiki;
```

メッセージはシミュレータのデフォルト出力ウインドウに出力される。

### [フィボナッチ数列](https://ja.wikipedia.org/wiki/フィボナッチ数列 "wikilink")

次の例はもう少し実用的なものである:

``` vhdl
-- Fib.vhd
--
-- Fibonacci number sequence generator

library IEEE;
use IEEE.std_logic_1164.all;
use IEEE.numeric_std.all;

entity Fibonacci is
port
(
    Reset       : in    std_logic;
    Clock       : in    std_logic;
    Number      : out   unsigned(31 downto 0)
);
end entity Fibonacci;

architecture Rcingham of Fibonacci is

    signal  Previous    : natural;
    signal  Current     : natural;
    signal  Next_Fib    : natural;

begin

    Adder:
    Next_Fib <= Current + Previous;

    Registers:
    process (Clock, Reset) is
    begin
        if Reset = '1' then
            Previous <= 1;
            Current  <= 1;
        elsif Clock'event and Clock = '1' then
            Previous <= Current;
            Current  <= Next_Fib;
        end if;
    end process Registers;

    Number <= to_unsigned(Previous, 32);

end architecture Rcingham;
```

シミュレーションを行うと`Next_Fib`がオーバーフローするまで、フィボナッチ数列を生成する。

## 参照

<references />

## 外部リンク

  - [IEEE VASG (VHDL Analysis and Standardization Group)](http://www.eda.org/twiki/bin/view.cgi/P1076/WebHome)

[Category:EDAソフト](https://ja.wikipedia.org/wiki/Category:EDAソフト "wikilink") [Category:ハードウェア記述言語](https://ja.wikipedia.org/wiki/Category:ハードウェア記述言語 "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink") [Category:IEEE標準](https://ja.wikipedia.org/wiki/Category:IEEE標準 "wikilink") [Category:回路設計](https://ja.wikipedia.org/wiki/Category:回路設計 "wikilink")

1.  [1076-1993 IEEE Standard VHDL Language Reference Manual](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=392561)
2.  [1076-2000 IEEE Standard VHDL Language Reference Manual](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=893288)
3.  [1076-2002 IEEE Standard VHDL Language Reference Manual](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=1003477)
4.  [1076-2008 IEEE Standard VHDL Language Reference Manual](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=4772740)