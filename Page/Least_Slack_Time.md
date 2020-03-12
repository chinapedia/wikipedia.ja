> この記事は[Least Slack Time](https://ja.wikipedia.org/wiki/Least_Slack_Time)から翻訳されています。


**Least Slack Time**(LST)は、[スケジューリング](../Page/スケジューリング.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")の一種。プロセスの *slack time* (余裕時間)に基づいて優先度を設定する。**Least Laxity First**(LLF)とも呼ばれる。一般に[組み込みシステム](../Page/組み込みシステム.md "wikilink")、特に[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")システムで使用されている。LSTを使用する場合、各プロセッサ上の各プロセスは同じ実行時間を備え、プロセスが特定のプロセッサにアフィニティ(Affinity)を持つことがないという制約がある。この制約によって組み込みシステムへの適合性が高くなっている。

## Slack time

このスケジューリングアルゴリズムは、*slack time*が最小なプロセスを選択して実行する。*slack time*とは、デッドラインまでの時間、実行可能となるまでの時間、実行時間の一時的な差と定義される。

より形式的に *slack time* を定義すれば、以下の式で表される:

\((d - t) - c'\)

ここで \(d\) はプロセスのデッドライン、すなわち現時点から \(d\) までの間にそのプロセスの処理をしなければならないことを意味する。\(t\) は現時点から実行サイクルが開始されるまでの時間であり、プロセスはそれより先に実行することができない。\(c'\) は実行にかかる時間である。従って、*slack time* とは、そのプロセスを可能な限り早く実行するとしたときのデッドラインまでの余裕時間である。すなわち、このアルゴリズムは可能な限りプロセスの実行を後回しにしようとする。

## 適用分野

LSTスケジューリングは、イベント発生頻度に事前の仮定を置かないので、非周期的タスクから構成されるシステムで使い易い。LSTの主な弱点は、現在のシステム状態のみを見ていてその先どうなるかを全く考慮していない点である。従って、一時的なシステムリソースの過負荷が発生するとLSTは最適な方式とは言えなくなる。また、割り込み不可能なプロセスがある環境でも最適な動作を保証できない。しかし、[Earliest Deadline Firstと同様](../Page/Earliest_Deadline_First.md "wikilink")(そして[レートモノトニックスケジューリング](../Page/レートモノトニックスケジューリング.md "wikilink")とは違って)、このアルゴリズムはプロセッサ使用率100%まで機能する。

## 関連項目

  - [スケジューリング](../Page/スケジューリング.md "wikilink")
  - [Earliest Deadline First](../Page/Earliest_Deadline_First.md "wikilink")

[Category:OSのプロセス管理](https://ja.wikipedia.org/wiki/Category:OSのプロセス管理 "wikilink") [Category:並行計算](https://ja.wikipedia.org/wiki/Category:並行計算 "wikilink")