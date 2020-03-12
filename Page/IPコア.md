> この記事は[IP](https://ja.wikipedia.org/wiki/IP)から翻訳されています。


**IPコア**（あいぴーコア、）とは、[LSIを構成するための部分的な回路情報で](../Page/集積回路.md "wikilink")、特に機能単位でまとめられているものを指す。単にIPと呼ぶ場合もある。

[ASIC](../Page/ASIC.md "wikilink")開発や[プログラマブルロジックデバイス](../Page/プログラマブルロジックデバイス.md "wikilink")を用いた開発の際に利用する。

1990年代以降、LSIの開発手法として[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")による開発が盛んになり、開発効率の向上が求められた。 そこで、既存開発製品の回路を、機能ブロック単位で再利用可能な形にまとめ、他の製品でも利用可な部分はそれを流用する方法が用いられた。 更に、この再利用可能な機能ブロックは、その開発者だけでなく、他の開発者や他の会社との間でもやり取りが行われるようになり、 新しいビジネスモデルが発達した。 IPコアベンダは、LSIを開発するためのIPコアを提供し、LSI開発側はIPコアベンダに[使用料を支払う契約を結ぶのが一般的である](../Page/ロイヤルティー.md "wikilink")。

IPとは元々は知的財産という意味だが、半導体業界において回路情報は重要な技術製品であり、形のない商品としてIPと呼ばれるようになった。

## IPコアの形態での分類

LSIの集積規模が飛躍的に向上したことを背景に、大規模なIPコアも開発されるようになった。 またプログラマブルロジックも、規模、速度ともに実用レベルに達すると、[FPGA](../Page/FPGA.md "wikilink")をメインのターゲットにしたIPコアも登場した。

  - ハードマクロ
      -
        マスクに相当する画像データとして提供される。シミュレーション用に等価なゲートモデルや、ビヘイビアモデルも同時に提供されることが多い。
        半導体プロセス技術に依存する。
        ソフトマクロに比べ、性能、面積の面で優れる。
        スタンダードセルでは実現できない回路（アナログ回路など）も含むことができる。
        プログラマブルロジックデバイスでは、利用できない。ただし、FPGA等にあらかじめ埋め込まれているハードマクロが存在する場合もある。
        ストラクチャードASICでは、あらかじめ埋め込まれているハードマクロが存在する場合もある。
        実チップになった実績があるものが多く、十分検証されている可能性が高い。

<!-- end list -->

  - ソフトマクロ
      - [RTLの形で提供されるもの](../Page/レジスタ転送レベル.md "wikilink")。
          -
            利用者の手元でターゲットのプロセス用に論理合成すればよく、半導体プロセス技術に依存しない。
            回路の構成がわかるため、トラブル発生時に解析が容易になる。
            RTLレベルでカスタマイズすることが可能（商用IPコアの場合、サポートが受けられなくなる可能性もある）。
      - ゲートレベルに論理合成されたネットリストの形のもの。
          -
            提供側がオリジナルのRTLを公開したくない場合に、ブラックボックスとして提供される。
            IPコア内部の変更は基本的にできない。
      - RTLより上位のビヘイビア記述の形で提供されるものもある。

また、IPコアベンダとして、商用のもの以外に、フリーで配布されているものもある\[1\]。

## IPコアを利用する長所・短所

長所

  - IPコアを利用することで、全てを始めから開発するより開発期間を短縮できる。
  - 半導体プロセス技術に依存しない。（RTLで提供されるソフトマクロの場合）

短所

  - 品質/信頼性 IPコアによっては詳細な設計仕様/検証結果がついていない場合もある。詳細な仕様や、どこまで正確に検証されているかを、よく確認する必要がある。
  - 接続性 既存の回路にIPコアを組み合わせる場合、仕様の確認ミスから接続部分で問題が起こりやすい。
  - ハードマクロのIPコアの場合、ターゲットの半導体プロセス技術以外では利用できない。
  - 高額なライセンスフィ IPコアを購入してライセンス契約をする際は、導入時に契約金を払う場合と、量産製品ひとつ毎に契約金を払う場合とがある。契約形態によってはそれら両方の場合もある。トラブル時のサポート体制なども含め、かえってコストがかかる場合もありうるため、商用IPコアを利用する場合はよく検討する必要がある。

## IPコアとして提供されている機能の例

[デジタル回路](../Page/デジタル回路.md "wikilink")のIPコアが一般的であるが、[アナログ回路](../Page/アナログ回路.md "wikilink")のIPコアも存在する。

  - デジタル回路
      - [CPU](../Page/CPU.md "wikilink")（[ソフトプロセッサ](../Page/ソフトプロセッサ.md "wikilink")）、[DSP](../Page/デジタルシグナルプロセッサ.md "wikilink")
      - CPU周辺回路 （[タイマー](../Page/タイマー.md "wikilink")、[DMA](../Page/Direct_Memory_Access.md "wikilink")、[割り込み制御](../Page/割り込み_\(コンピュータ\).md "wikilink")、他）
      - [メモリ](../Page/記憶装置.md "wikilink") （[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")、[SRAM](../Page/Static_Random_Access_Memory.md "wikilink")、[DRAM](../Page/Dynamic_Random_Access_Memory.md "wikilink")、他）
          -
            基本的に半導体プロセス技術依存
            フルスクラッチのフルカスタム[ASIC](../Page/ASIC.md "wikilink")でのみ利用可能
      - 通信I/F （[UART](../Page/UART.md "wikilink")、[SPI](../Page/シリアル・ペリフェラル・インタフェース.md "wikilink")、[I²C](https://ja.wikipedia.org/wiki/I²C "wikilink")、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[イーサネット](../Page/イーサネット.md "wikilink")、[ATM](../Page/Asynchronous_Transfer_Mode.md "wikilink")、[JTAG](../Page/JTAG.md "wikilink")、他）
      - バスI/F （[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")、[PCI Express](../Page/PCI_Express.md "wikilink")、AHB、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink") I/F、各種メモリカードI/F、他）
      - 基本算術演算 （[浮動小数点演算](../Page/浮動小数点数.md "wikilink")、FFT、他）
      - [暗号](../Page/暗号.md "wikilink")化/復号 （[AES](../Page/Advanced_Encryption_Standard.md "wikilink")、[DES](../Page/Data_Encryption_Standard.md "wikilink")、[RSA](../Page/RSA暗号.md "wikilink")、[RC5](../Page/RC5.md "wikilink")、[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")、[MD5](../Page/MD5.md "wikilink")、[TLS/SSL](../Page/Transport_Layer_Security.md "wikilink")、他）
      - 画像処理 （静止画[CODEC](../Page/コーデック.md "wikilink")（[JPEG](../Page/JPEG.md "wikilink")、他）、動画CODEC （[MPEG](../Page/Moving_Picture_Experts_Group.md "wikilink")）、画像認識、他）
      - 音声処理 （音声CODEC（[MP3](../Page/MP3.md "wikilink")、[AAC](../Page/AAC.md "wikilink")、[μ-law](../Page/G.711.md "wikilink")、A-law）、音声合成、他）

<!-- end list -->

  - アナログ回路
      -
        基本的に半導体プロセス技術依存
    <!-- end list -->
      - [AD](../Page/アナログ-デジタル変換回路.md "wikilink")、[DA変換](../Page/デジタル-アナログ変換回路.md "wikilink")
      - [オペアンプ](../Page/オペアンプ.md "wikilink")
      - [PLL](../Page/位相同期回路.md "wikilink")、[クロック](../Page/クロック.md "wikilink")、タイミング
      - 電源
      - 大電力ドライバ （モータドライバ）
      - センサ （加速度、圧力、光/画像、温度、磁気、電流/電圧、他）

## 主な用途

  - [ASIC](../Page/ASIC.md "wikilink")
  - [FPGA](../Page/FPGA.md "wikilink")や[CPLD](../Page/CPLD.md "wikilink")などのプログラマブルロジックデバイス

## 関連項目

## 脚注

<references/>

[Category:集積回路](https://ja.wikipedia.org/wiki/Category:集積回路 "wikilink") [Category:デジタル回路](https://ja.wikipedia.org/wiki/Category:デジタル回路 "wikilink") [Category:アナログ回路](https://ja.wikipedia.org/wiki/Category:アナログ回路 "wikilink")

1.