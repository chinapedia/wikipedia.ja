> この記事は[Folding@home](https://ja.wikipedia.org/wiki/Folding@home)から翻訳されています。


**Folding@home**（FAH、フォールディング・アット・ホーム\[1\]）は、[分子動力学](../Page/分子動力学法.md "wikilink")[シミュレーション](../Page/シミュレーション.md "wikilink")によりタンパク質の[フォールディング](../Page/フォールディング.md "wikilink")を解析するための、[ボランティア](../Page/ボランティア.md "wikilink")・[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")プロジェクト。

## 概要

Folding@homeは、世界中の家庭にある[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")・[ゲーム機](../Page/ゲーム機.md "wikilink")・[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")などの身近なマシンを、分散コンピューティング技術によって科学研究に利用するプロジェクトである。参加者は無償のボランティアであり、おのおの所有するマシンに専用ソフトウェアをインストールし、アイドル時に余る計算リソースを提供する。研究者は、本プロジェクトの成果であるタンパク質の解析情報を手がかりにスクリーニング（ふるい分け）することで、[アルツハイマー病](https://ja.wikipedia.org/wiki/アルツハイマー病 "wikilink")・[ハンチントン病](../Page/ハンチントン病.md "wikilink")・[パーキンソン病](../Page/パーキンソン病.md "wikilink")・[癌](../Page/悪性腫瘍.md "wikilink")・各種[ウイルス](../Page/ウイルス.md "wikilink")対策などの研究効率を上げることができる。

本プロジェクトは、分散コンピューティングモデルとしても先駆的な取り組みをしている。クライアント（参加者のマシン）はそれぞれシミュレーションの一部（ワークユニット、WU）を受け取り、計算により完成させ、プロジェクトのサーバーに返す。先進的な統計シミュレーション手法により、有力な予測結果をクライアント間で共有して効率を高める。個人やチームの計算累積をウェブサイトに掲示することで参加者の達成感や競争心を刺激し、積極的かつ長期的な貢献を促す。

本プロジェクトは[ビジェイ・S・パンデ](https://ja.wikipedia.org/wiki/ビジェイ・S・パンデ "wikilink")教授の指揮のもと、2000年10月1日に[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")で発足した。2019年以降は、[ワシントン大学](https://ja.wikipedia.org/wiki/ワシントン大学 "wikilink")セントルイス校医学部に拠点を置き、パンデ教授の元教え子であるグレッグ・ボーマン博士が指揮している。発足以来、直接の成果として200以上の科学研究論文を発表してきた\[2\]。シミュレーションと実験の結果はよく一致している。

2020年2月末より[新型コロナウイルス（SARS-CoV-2）に対する取り組みを始めると](../Page/2019新型コロナウイルス.md "wikilink")、参加者が著しく増加し、同年3月25日に本プロジェクトの演算能力は1EFLOPSを突破\[3\]\[4\]、さらに翌4月中旬には2.4EFLOPSにも達した\[5\]。[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")の全[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")の合算を上回る能力を獲得し、これまでの数千倍長いタンパク質を対象とするシミュレーションが可能となっている。

## 生物医学研究への応用例

タンパク質の誤った折りたたみ（ミスフォールディング）は、[癌](../Page/悪性腫瘍.md "wikilink")、[クロイツフェルトヤコブ病](../Page/クロイツフェルト・ヤコブ病.md "wikilink")、[嚢胞性線維症](https://ja.wikipedia.org/wiki/嚢胞性線維症 "wikilink")、[ハンチントン病](../Page/ハンチントン病.md "wikilink")、[鎌状赤血球性貧血](../Page/鎌状赤血球症.md "wikilink")、[II型糖尿病を含む様々な疾患の結果となり得る](../Page/2型糖尿病.md "wikilink")。HIVやインフルエンザなどのウイルスによる細胞感染には、[細胞膜](https://ja.wikipedia.org/wiki/細胞膜 "wikilink")上でのタンパク質の折り畳み現象も関与している。タンパク質のミスフォールディングがよりよく理解されれば、タンパク質のフォールディングを調節する細胞の自然な能力を増強する治療法を開発することができる。このような[治療](../Page/治療.md "wikilink")法には、特定のタンパク質の産生を変化させたり、誤って折りたたまれたタンパク質を破壊したり、あるいは折り畳みプロセスを補助するために人工分子を使用することが含まれる。計算分子モデリングと実験解析の組み合わせは、[創薬](../Page/創薬.md "wikilink")の迅速化やコスト削減など、分子医学の未来と[治療法の合理的な設計を根本的に形作る可能性を秘めている](https://ja.wikipedia.org/wiki/医薬品設計 "wikilink")。Folding@homeの最初の5年間の目標は、フォールディングの理解を前進させることであったが、現在の目標は、ミスフォールディングと関連疾患、特に[アルツハイマー病](https://ja.wikipedia.org/wiki/アルツハイマー病 "wikilink")の理解である。

### ウイルス

2020年3月以降、Folding@homeは、治療法の発見や[コロナウイルスの世界的流行についての詳細な情報を得ようとしている世界中の研究者を支援するプログラムを開始した](../Page/新型コロナウイルス感染症の流行_\(2019年-\).md "wikilink")。プロジェクトの第一波は、SARS-CoV-2ウイルス、および関連するSARS-CoVウイルスからの薬物投与可能なタンパク質ターゲットをシミュレートするもので、これらについては、利用可能なデータが大幅に増えている\[6\]\[7\]\[8\]\[9\]。

## 経過

  - 2000年10月1日、プロジェクトを開始。
  - 2007年3月22日、[PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")（PS3）に対応\[10\]。3日後には700T（[テラ](../Page/テラ.md "wikilink")）[FLOPS](../Page/FLOPS.md "wikilink")以上の演算能力を獲得し、従来1年以上かかっていた複雑なシミュレーションが数週間で完了した\[11\]。
  - 2007年9月16日、分散コンピューティング史上初となる1P（[ペタ](https://ja.wikipedia.org/wiki/ペタ "wikilink")）FLOPSに到達（1秒間に1000兆回の演算能力）。
  - 2007年9月24日、PS3クライアントのみの合計で当時のスーパーコンピュータの能力に匹敵する1PFLOPSに到達\[12\]。
  - 2007年11月1日、世界一強力な分散コンピューティングネットワークとして[ギネスブックに認定](https://ja.wikipedia.org/wiki/ギネス・ワールド・レコーズ "wikilink")\[13\]\[14\]。
  - 2008年11月9日現在、計4.247PFLOPS、うち[GPUの処理能力は](../Page/Graphics_Processing_Unit.md "wikilink")2.226PFLOPS、PS3による処理能力は1.733PFLOPS。
  - 2012年3月23日現在、計5.427PFLOPS。
  - 2012年10月22日、PS3クライアントの終了を発表（2012年11月6日終了、延べ1500万人のユーザーが参加した）\[15\]。
  - 2015年1月13日、[Android](../Page/Android.md "wikilink")4.4以上搭載のスマートフォン／[タブレット](https://ja.wikipedia.org/wiki/タブレット "wikilink")向けクライアントアプリをリリース。当初は[Xperia](https://ja.wikipedia.org/wiki/Xperia "wikilink")シリーズのみ対応、のち条件を満たす他機種にも対応。
  - 2016年1月6日現在、計80.79PFLOPS、うちGPUの処理能力は78PFLOPS（96％）。GPUはNVIDIAのFermiが8割を占める。
  - 2020年2月27日、新型コロナウイルス感染症（COVID-19）に対する取り組みを発表\[16\]。
  - 2020年3月25日、分散コンピューティング史上初となる1E（[エクサ](https://ja.wikipedia.org/wiki/エクサ "wikilink")）FLOPSに到達（1秒間に100京回の演算能力）。

## 脚注

## 関連項目

  - [タンパク質構造予測](../Page/タンパク質構造予測.md "wikilink")
  - [フォールディング](../Page/フォールディング.md "wikilink")
  - [Foldit](https://ja.wikipedia.org/wiki/Foldit "wikilink")
  - [グリッド・コンピューティング](../Page/グリッド・コンピューティング.md "wikilink")
  - [分散コンピューティング](../Page/分散コンピューティング.md "wikilink")
  - [市民科学](https://ja.wikipedia.org/wiki/市民科学 "wikilink")
  - [SETI@home](../Page/SETI@home.md "wikilink")

## 外部リンク

  -
  -
[Category:分散コンピューティングプロジェクト](https://ja.wikipedia.org/wiki/Category:分散コンピューティングプロジェクト "wikilink") [Category:分子動力学ソフトウェア](https://ja.wikipedia.org/wiki/Category:分子動力学ソフトウェア "wikilink") [Category:分子モデリングソフトウェア](https://ja.wikipedia.org/wiki/Category:分子モデリングソフトウェア "wikilink") [Category:2019新型コロナウイルス感染症](https://ja.wikipedia.org/wiki/Category:2019新型コロナウイルス感染症 "wikilink") [Category:タンパク質構造](https://ja.wikipedia.org/wiki/Category:タンパク質構造 "wikilink") [Category:計算生物学](https://ja.wikipedia.org/wiki/Category:計算生物学 "wikilink") [Category:数理生物学](https://ja.wikipedia.org/wiki/Category:数理生物学 "wikilink") [Category:バイオインフォマティクス](https://ja.wikipedia.org/wiki/Category:バイオインフォマティクス "wikilink") [Category:スタンフォード大学](https://ja.wikipedia.org/wiki/Category:スタンフォード大学 "wikilink") [Category:ギネス世界記録](https://ja.wikipedia.org/wiki/Category:ギネス世界記録 "wikilink") [Category:GPGPU](https://ja.wikipedia.org/wiki/Category:GPGPU "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. [僕らの知らない間にPS3が医療に貢献――米国スタンフォード大学の「Folding@home」提供開始](http://www.itmedia.co.jp/games/articles/0703/15/news066.html)
11. [「1年以上かかるはずだった計算も数週間」--Folding@homeにPS3ユーザー25万人以上が登録](http://japan.cnet.com/news/media/20347945/)
12. [小堀龍之「ネットはいま 第2部 つながる――ゲーム機を持ち寄る(5)」『朝日新聞』2009年2月6日付夕刊、第3版、第3面。](http://www.asahi.com/special/net/TKY200902060198.html)
13.
14. [「プレイステーション ３」がスタンフォード大学の「Folding@home™」のギネス世界記録樹立に大きく貢献～「Folding@home™」が世界で最も強力な分散コンピューティングネットワークとして認定～](http://www.sie.com/corporate/release/2007/071101.html)
15. [「Life with PlayStation®」終了のお知らせ](http://www.jp.playstation.com/info/release/nr_20121022_life_with_playstation.html)
16.