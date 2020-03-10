> この記事は[SRAM](https://ja.wikipedia.org/wiki/SRAM)から翻訳されています。


**擬似SRAM**（ぎじエスラム、Pseudo Static Random Access Memory）とは、[SRAMインターフェースを備えた](../Page/Static_Random_Access_Memory.md "wikilink")[DRAMである](../Page/Dynamic_Random_Access_Memory.md "wikilink")。

## 擬似SRAMの利点

擬似SRAMは、純粋なSRAMやDRAMに比べて以下の利点がある。

  - スタティック動作が可能である。
    ダイナミック動作はタイミングが規定されており、規定時間内にデータの入出力を行わなければならない。スタティック動作ではアドレス指定、ストローブ信号の入力、データの入出力を任意のタイミングで行う事ができるので、[回路設計](https://ja.wikipedia.org/wiki/回路設計 "wikilink")が容易になる。
  - 廉価である
    SRAMは1記憶セルあたり最低6個の素子を必要とする。DRAMではキャパシタとスイッチングトランジスタだけで良いので集積密度が高く、小さなダイで良いので歩留まりに優れ、コスト的にはSRAMより優位にあり、単なるDRAMとSRAMの中間に存在する。
  - 大容量である
    セルあたりのフットプリントがSRAMより小さいので、同じダイ面積では数倍の記憶容量を実現できる。これはデバイスサイズに敏感な用途では重要な要素となる。
  - 複雑なメモリコントローラが不要である
    DRAMでは非常に複雑なメモリコントローラを必要とする。しかしSRAMインターフェースであれば、ラッチ回路があればよく、前述のスタティック動作でも良いことも相まって、回路規模をコンパクトにする事ができる。

## 擬似SRAMの欠点

  - 内部はダイナミック動作である
    本質的にはDRAMである為、ダイナミック動作が必要である。疑似SRAMはそれらのメモリコントローラ回路を内蔵しており、リフレッシュやプリチャージを制御している。この為、単なるDRAMに比べると若干高価である。
  - 消費電力が大きい
    前述のダイナミック動作による消費電力に加え、メモリコントローラ回路も内蔵しているので、消費電力の点ではSRAMにもDRAMにも劣る。
  - 低速である
    本来速度的に不利とされるDRAMを記憶セルに用いている上に周辺回路も統合しているので、アクセス速度はSRAMには到底及ばず、純粋なDRAMにも劣る。

## 用途

  - [SoCの記憶デバイスとして](https://ja.wikipedia.org/wiki/System-on-a-chip "wikilink")
    携帯電話などでは年々必要な記憶容量が増大する傾向にあり、高価なフラッシュメモリやSRAMの代替品として疑似SRAMが用いられている。デバイスが非常にコンパクトである事も採用される理由となっている。
  - 家電用機器の記憶デバイスとして
    家電用マイクロコントローラはメモリコントローラが無いかあっても簡易な物しかない場合が多く、簡易メモリコントローラだけでDRAMを実装できる擬似SRAMのニーズは多い。
  - 携帯ゲーム機用メモリ
    簡素な回路で利用できること、[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")インターフェースと回路を共通化することができるなど、メインメモリとして採用されている。

## 近年のトレンド

組み込み用途のものを中心に、近年の32bit[マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")はDRAMの制御回路（バスタイミングとリフレッシュの管理をする回路）を内蔵するようになってきている。このようなCPUを使う場合、疑似SRAMの利点のほとんどは生かされず欠点だけが残ることとなるため、擬似SRAMが採用されることは無く、4bit〜16bitの廉価なマイクロコントローラで主に使われている。

しかし、擬似SRAMのシェアは[eDRAM](https://ja.wikipedia.org/wiki/eDRAM "wikilink")によって奪われつつある。[SiP](https://ja.wikipedia.org/wiki/SiP "wikilink")によってパッケージ内にコアロジックとメモリを混載する技術が開発されてから、擬似SRAMのシェアは伸び悩んでいる。

## 関連

  - [1T-SRAM](https://ja.wikipedia.org/wiki/1T-SRAM "wikilink") : 擬似SRAMの一種だがアクセス機構や回路配置の工夫によって通常のSRAMよりも低消費電力かつ通常のDRAMよりも高速なアクセスを実現している。[ニンテンドーゲームキューブ](../Page/ニンテンドーゲームキューブ.md "wikilink")などのゲーム機で多く採用されている。

## 外部リンク

  - [ルネサステクノロジ](http://japan.renesas.com/fmwk.jsp?cnt=/press_release20040617.htm&fp=/company_info/news_and_events/press_releases&site=i)
  - [Nikkei NE 東芝製疑似SRAMの記事](http://www.nikki.ne.jp/news/115377.html)
  - [Design News Japan 業界初の128メガビット疑似SRAMの商品化について](http://www.designnewsjapan.com/news/200411/08comp_fujitsu041108.html)
  - [NECエレクトロニクス株式会社](http://www.necel.com/news/ja/archive/0411/0501.html)

[Category:半導体メモリ](https://ja.wikipedia.org/wiki/Category:半導体メモリ "wikilink")