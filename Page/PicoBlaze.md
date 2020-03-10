> この記事は[PicoBlaze](https://ja.wikipedia.org/wiki/PicoBlaze)から翻訳されています。


**PicoBlaze**は、[ザイリンクス](https://ja.wikipedia.org/wiki/ザイリンクス "wikilink")が自らの[FPGAや](https://ja.wikipedia.org/wiki/プログラマブルロジックデバイス#FPGA "wikilink")[CPLD](https://ja.wikipedia.org/wiki/CPLD "wikilink")製品向けに提供している[ソフトプロセッサ](../Page/ソフトプロセッサ.md "wikilink")コアの名称である。PicoBlazeは[8ビット](../Page/8ビット.md "wikilink")の[RISC](../Page/RISC.md "wikilink")アーキテクチャに基づき、FPGAの[Virtex 4シリーズの上で](https://ja.wikipedia.org/wiki/Virtex_4 "wikilink")、100[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")を達成することが出来る。[プロセッサ](../Page/プロセッサ.md "wikilink")は広範囲の周辺機器へのアクセスのため、8ビットのアドレスとデータポートを持っている。このコアのライセンスは、ザイリンクスのデバイスの上であれば、無料で動作させることを認めていて、開発環境も提供されている。[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")のツールがMediatronix等から入手可能である。ビヘイビア合成による、このコアから独立した、デバイス非依存の実装の[PacoBlaze](https://ja.wikipedia.org/wiki/PacoBlaze "wikilink")が、[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")の下でリリースされている。

PicoBlazeの設計は、当初"Constant(K) Coded Programmable State Machine"（その前は「ケンチャップマンのPSM」／"Ken Chapman's PSM"）を表すKCPSMと名づけられていた。ケン・チャップマンはPicoBlazeを考案し実装したザイリンクスのシステムデザイナーであった。\[1\]

[VHDL](https://ja.wikipedia.org/wiki/VHDL "wikilink")でPicoBlazeマイクロコントローラを実装するときは、それぞれのKCPSM部品の名前を使用しなければならない。\[2\] 例えば、PacoBlaze3プロセッサでは以下のようになる：

` component kcpsm3 is`
`   port (`
`     address : out std_logic_vector(9 downto 0);`
`     instruction : in std_logic_vector(17 downto 0);`
`     port_id : out std_logic_vector(7 downto 0);`
`     write_strobe : out std_logic;`
`     out_port : out std_logic_vector(7 downto 0);`
`     read_strobe : out std_logic;`
`     in_port : in std_logic_vector(7 downto 0);`
`     interrupt : in std_logic;`
`     interrupt_ack : out std_logic;`
`     reset : in std_logic;`
`     clk : in std_logic`
`     );`
` end component;`

## 関連項目

  - [PacoBlaze](https://ja.wikipedia.org/wiki/PacoBlaze "wikilink")
  - [LatticeMico8](https://ja.wikipedia.org/wiki/LatticeMico8_-_8-bit_Microcontroller "wikilink")
  - [LatticeMico32](https://ja.wikipedia.org/wiki/LatticeMico32 "wikilink")
  - [MicroBlaze](https://ja.wikipedia.org/wiki/MicroBlaze "wikilink")
  - [Nios](https://ja.wikipedia.org/wiki/Nios_embedded_processor "wikilink")
  - [Nios II](https://ja.wikipedia.org/wiki/Nios_II "wikilink")

## 外部リンク

  - [PicoBlaze on the Xilinx website](http://www.xilinx.com/picoblaze)
  - [PicoBlaze product brief](http://www.xilinx.com/bvdocs/ipcenter/data_sheet/picoblaze_productbrief.pdf)
  - [PicoBlaze user manual](http://www.xilinx.com/bvdocs/userguides/ug129.pdf)
  - [TechXclusives: Creating Embedded Microcontrollers (Programmable State Machines)](http://www.xilinx.com/xlnx/xweb/xil_tx_display.jsp?sTechX_ID=kc_emb_micro) [PDF](http://bleyer.org/pacoblaze/picoblaze.pdf)
  - [PicoBlaze user resources](http://www.xilinx.com/ipcenter/processor_central/picoblaze/picoblaze_user_resources.htm)
  - [Professional IDE for Linux and Windows](http://www.moravia-microsystems.com/multitarget-development-system/)
  - [Mediatronix free FPGA tools](http://www.mediatronix.com/pBlazASM)
  - [Free Linux IDE](http://www.xs4all.nl/~marksix)
  - [PacoBlaze: a synthesizable and behavioral Verilog clone of PicoBlaze](http://bleyer.org/pacoblaze)

## 参照

<references />

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.
2.