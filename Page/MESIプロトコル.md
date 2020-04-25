> この記事は[MESIプロトコル](https://ja.wikipedia.org/wiki/MESIプロトコル)から翻訳されています。


[Diagrama_MESI.GIF](https://ja.wikipedia.org/wiki/File:Diagrama_MESI.GIF "fig:Diagrama_MESI.GIF")\]\] [MESI_protocol_activity_diagram.png](https://ja.wikipedia.org/wiki/File:MESI_protocol_activity_diagram.png "fig:MESI_protocol_activity_diagram.png")\]\] **MESIプロトコル**（別名、**イリノイ・プロトコル**）とは、[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")システムで[メモリや](../Page/主記憶装置.md "wikilink")[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")の[同期をとる](https://ja.wikipedia.org/wiki/同期_\(情報工学\) "wikilink")[キャッシュコヒーレンシ](https://ja.wikipedia.org/wiki/キャッシュコヒーレンシ "wikilink")と[メモリ一貫性](https://ja.wikipedia.org/wiki/メモリ一貫性 "wikilink")のプロトコルであり、ライトバック方式のキャッシュで広く使われている。イリノイ・プロトコルという別名は[イリノイ大学アーバナ・シャンペーン校](../Page/イリノイ大学アーバナ・シャンペーン校.md "wikilink")で開発されたことに由来する。

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")は、「[486プロセッサで以前から使われていたライトスルーキャッシュに加えて](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")、より効率的なライトバックキャッシュをサポートする」\[1\]として[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")プロセッサでMESIプロトコルを採用した。そのためパーソナルコンピュータでも広く使われている。

## 概要

各キャッシュラインは以下の4状態のいずれかにある。状態はキャッシュラインのタグに含まれる（2[bitで表される](../Page/ビット.md "wikilink")）。

  - **M** - Modified(変更): 当該キャッシュだけに存在し、主記憶上の値から変更されている(*dirty*)。他のCPUがこのキャッシュラインに相当する主記憶をリードするのを許可する前に、キャッシュ機構はこのキャッシュラインをいずれかの時点で主記憶に書き戻さなければならない。
  - **E** - Exclusive(排他): 当該キャッシュだけに存在するが、主記憶上の値と一致している(*clean*)。
  - **S** - Shared(共有): システム内の他のキャッシュにも同じキャッシュラインが存在している（主記憶とも内容が一致）。
  - **I** - Invalid(無効): このキャッシュラインは無効。

任意の2つのキャッシュがあるとき、それぞれの対応するキャッシュラインがとりうる状態の組合せは次のようになる。

<table>
<thead>
<tr class="header">
<th></th>
<th><p> M </p></th>
<th><p> E </p></th>
<th><p> S </p></th>
<th><p> I </p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p> M </p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td></td>
</tr>
<tr class="even">
<td><p> E </p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p> S </p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p> I </p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 動作

典型的システムでは、複数のキャッシュがメインメモリの接続された[バスを共有している](../Page/バス_\(コンピュータ\).md "wikilink")。それぞれのキャッシュには[CPU](../Page/CPU.md "wikilink")が接続されており、それがリード要求やライト要求を発行する。このようなシステムで全体として共有している主記憶へのアクセスを最小にすることが目的である。

Invalid状態以外のキャッシュラインはリード要求を満たすことができる。Invalid状態のラインにリード要求が来た場合、主記憶から内容を読み込む必要がある（Shared か Exclusive 状態に遷移する）。

ライト要求を実行できるのは、Modified状態かExclusive状態の場合のみである。Shared状態なら、書き込みを行う前にシステム内の他のキャッシュ（の該当するキャッシュライン）を Invalid 状態にしなければならない。これは、通常ブロードキャスト操作で実行され、その操作を *Read For Ownership (RFO)* と呼ぶ。

キャッシュ機構は Modified状態以外のキャッシュラインをいつでも捨てて Invalid状態にすることができる。Modified状態のラインは必ず主記憶に書き戻さなければならない。

Modified状態のキャッシュラインを持つキャッシュ機構は、バス上の流れを監視して（[バススヌープ](https://ja.wikipedia.org/wiki/バススヌーピング "wikilink")）、対応する主記憶上の位置へのリード要求をインターセプトして、それを再試行状態にする。そして自身の持つキャッシュラインの内容を主記憶に書き戻し、そのキャッシュラインの状態を Shared に遷移させる。

Shared 状態のキャッシュラインを持つキャッシュ機構もバススヌープによって他のCPUからの無効化要求を受け取り、対応するラインを捨てる（Invalid状態に遷移させる）。

Exclusive状態のキャッシュラインを持つキャッシュ機構もバススヌープで他のCPUのトランザクションを監視し、対応するアドレス範囲へのアクセスがあったら Shared 状態へ遷移させる。

Modified状態とExclusive状態は、システム内のそのキャッシュラインの所有権を有しているため、明確である。Shared 状態はあいまいなところがあり、他のCPUのキャッシュが該当キャッシュラインを捨てたときに実際には Exclusive状態になるべき場合があるが、そのような遷移は通常行われない（そのためにはブロードキャストが必要だが、実際問題としてあまり意味が無い）。

そういった意味では Exclusive状態というのは若干日和見的な最適化である。Shared状態のキャッシュラインに変更を加える場合、無効化要求をブロードキャストする必要があると規定することで、Exclusive状態のキャッシュラインの更新はトランザクションを必要としないのである。

### Read For Ownership

*Read For Ownership (RFO)* は[キャッシュコヒーレンシ](https://ja.wikipedia.org/wiki/キャッシュコヒーレンシ "wikilink")プロトコルの操作の1つで、リードと無効化ブロードキャストを組み合わせたものである。これはあるキャッシュラインに書き込む際、そのキャッシュの当該キャッシュラインがExclusive状態でもModified状態でもないときに行うもので、つまりそのキャッシュラインはMESIプロトコルではShared状態かInvalid状態である。この操作により他の全プロセッサの当該キャッシュラインはInvalid状態へと遷移させられる。RFOトランザクションはそのメモリアドレスに書き込むことを前提としたリード操作である。したがってこの操作は排他的である。それによりそのキャッシュにはデータがもたらされ、他の全プロセッサの当該キャッシュラインは無効化される。

## その他のキャッシュプロトコル

### MSIプロトコル

**MSIプロトコル**はExclusive状態を持たないキャッシュプロトコル。MESIプロトコルでExclusive状態となるような状況では、Shared状態となる。

Invalid状態のキャッシュラインにCPUからリードを行う場合、他のキャッシュの当該キャッシュラインがModified状態でないことを保証しなければならないが、その方式はアーキテクチャによって異なる。一般的な方式としてはリード要求のブロードキャストがないか[バススヌーピング](https://ja.wikipedia.org/wiki/バススヌーピング "wikilink")で監視する。また、キャッシュ内に各キャッシュラインを最近リードしたキャッシュがどれかを示す情報を格納しておく方式もある。Modified状態のキャッシュラインを別のキャッシュが持っていた場合、その内容を主記憶に書き戻し、キャッシュライン自体はShared状態かInvalid状態へと遷移しなければならない。Modified状態のキャッシュラインが書き戻されると、当該キャッシュラインへは主記憶か他のShared状態のキャッシュから内容を読み込み、Shared状態へと遷移する。

ライト要求は当該キャッシュラインがModified状態ならローカルにキャッシュに書き込むだけで済む。Shared状態なら、他のキャッシュのShared状態のキャッシュラインを無効化する必要がある。これもリードと同様にバススヌーピングなどで実現する。その上でModified状態に遷移してローカルにキャッシュにライトを行う。Invalid状態の場合、他のキャッシュのShared状態とModified状態のキャッシュラインを無効化しなければならない。別のキャッシュの当該キャッシュラインがModified状態なら、そのキャッシュラインの内容を主記憶に書き戻すか、ライト要求したキャッシュに対して内容を送る。なお、一般にCPUのライト要求はせいぜいワード単位までであり、キャッシュラインは複数ワードという構成が一般的であるため、Invalid状態でのライト要求の場合、書き込みの前に当該キャッシュライン全体を読み込んでおく必要がある。

任意の2つのキャッシュがあるとき、それぞれの対応するキャッシュラインがとりうる状態の組合せは次のようになる。

<table>
<thead>
<tr class="header">
<th></th>
<th><p> M </p></th>
<th><p> S </p></th>
<th><p> I </p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p> M </p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td></td>
</tr>
<tr class="even">
<td><p> S </p></td>
<td><p>{{×}}</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p> I </p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### MOSIプロトコル

**MOSIプロトコル**はExclusive状態の代わりに Owned(所有)状態のあるキャッシュプロトコル。Exclusive状態がないため、MSIプロトコルにOwned状態を加えたものと見たほうがよい（つまりExclusive状態はShared状態に包含されている）。

Owned状態のキャッシュラインは *dirty* であり、主記憶への書き戻しが必要である。Modified状態のキャッシュラインに相当するアドレスに他のCPUがリード要求を発行したときに、Owned状態に遷移する。Owned状態のキャッシュラインを持つキャッシュ機構は、当該アドレス範囲へのリード要求に対して主記憶の代わりに応答する。すなわち、そのキャッシュラインは他のCPUでは Shared 状態となっている。Owned状態でさらに変更を加える際には、他のキャッシュのShared状態の当該キャッシュラインを無効化して自身はModified状態へ遷移するか、他のキャッシュに更新内容を送ってShared状態を維持させる（アーキテクチャによって異なる）。

任意の2つのキャッシュがあるとき、それぞれの対応するキャッシュラインがとりうる状態の組合せは次のようになる。

<table>
<thead>
<tr class="header">
<th></th>
<th><p> M </p></th>
<th><p> O </p></th>
<th><p> S </p></th>
<th><p> I </p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p> M </p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td></td>
</tr>
<tr class="even">
<td><p> O </p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p> S </p></td>
<td><p>{{×}}</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p> I </p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### MOESIプロトコル

**MOESIプロトコル**はMESIプロトコルに Owned状態を加えたキャッシュプロトコル。[AMD64で採用されている](https://ja.wikipedia.org/wiki/x64 "wikilink")\[2\]。

任意の2つのキャッシュがあるとき、それぞれの対応するキャッシュラインがとりうる状態の組合せは次のようになる。

<table>
<thead>
<tr class="header">
<th></th>
<th><p> M </p></th>
<th><p> O </p></th>
<th><p> E </p></th>
<th><p> S </p></th>
<th><p> I </p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p> M </p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td></td>
</tr>
<tr class="even">
<td><p> O </p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p> E </p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td><p>{{×}}</p></td>
<td></td>
</tr>
<tr class="even">
<td><p> S </p></td>
<td><p>{{×}}</p></td>
<td></td>
<td><p>{{×}}</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p> I </p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

MESIプロトコルに比べると、*dirty*なキャッシュラインを持っている状態で他のキャッシュからリード要求があっても[主記憶に書き戻す必要がないという点が優れている](../Page/記憶装置.md "wikilink")。代わりにOwned状態のキャッシュラインは他のプロセッサに直接変更の加わったデータを送ることができる。これは、キャッシュ間のやりとりが主記憶とのやりとりよりも高速な場合に有利で、例えばマルチコアCPUでCPU毎にL2キャッシュがある場合などが相当する。

しかし、キャッシュラインが *clean* な場合、Invalid状態のキャッシュがリード要求したとき応答するのは主記憶であり、Shared状態やExclusive状態のキャッシュラインは応答しない。

## 関連項目

  - [キャッシュコヒーレンシ](https://ja.wikipedia.org/wiki/キャッシュコヒーレンシ "wikilink")

## 脚注・出典

## 外部リンク

  - [An interactive MESI simulation](https://www.cs.tcd.ie/Jeremy.Jones/vivio/caches/MESIHelp.htm)

[Category:キャッシュコヒーレンシ](https://ja.wikipedia.org/wiki/Category:キャッシュコヒーレンシ "wikilink")

1.  IA-32 Intel Architecture Software Developers Manual
2.  [AMD64 Architecture Programmer's Manual Vol 2 'System Programming'](http://support.amd.com/us/Processor_TechDocs/24593.pdf) p.167