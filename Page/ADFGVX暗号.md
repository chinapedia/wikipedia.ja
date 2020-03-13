> この記事は[ADFGVX](https://ja.wikipedia.org/wiki/ADFGVX)から翻訳されています。


**ADFGVX暗号**（ADFGVXあんごう、**ADFGVX cipher**）は、[ポリュビオスの暗号表](../Page/ポリュビオスの暗号表.md "wikilink")と鍵を使った[転置式暗号](../Page/転置式暗号.md "wikilink")を組み合わせた[暗号](../Page/暗号.md "wikilink")の一つ。[第一次世界大戦](../Page/第一次世界大戦.md "wikilink")中にドイツ軍が使用した。

## 概要

この暗号は、フリッツ・ナベル(Fritz nebel)[大佐](../Page/大佐.md "wikilink")によって発明されたADFGX暗号を拡張したものであり、ADFGX暗号は[1918年](../Page/1918年.md "wikilink")[3月5日](../Page/3月5日.md "wikilink")から[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")軍が使い始め、数ヶ月後にはADFGVX暗号が使い始められた。

この暗号の名前は、暗号文がADFGVXの6文字で表されたことによる。なぜ、この6文字かというと、そのころ使われていた[モールス信号](https://ja.wikipedia.org/wiki/モールス信号 "wikilink")で、それぞれの文字が識別しやすかった(混同されにくかった)からである。A(・－)D(－・・)F(・・－・)G(－－・)V(・・・－)X(－・・－)

ADFGX暗号もADFGVX暗号とも、[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")の暗号解読者、ジョルジュ・パンヴァン (Georges Painvin)によって解読された。

## 歴史の中でのADFGVX暗号

[19世紀](../Page/19世紀.md "wikilink")の中頃、[バベッジ](https://ja.wikipedia.org/wiki/バベッジ "wikilink")（1854年頃、ただし公表されなかった）とカシスキー（1863年に出版）によって[ヴィジュネル暗号](../Page/ヴィジュネル暗号.md "wikilink")の解読法が明らかにされてから、絶対安全な暗号というものはなくなってしまった。19世紀末に発明された[無線通信](../Page/無線通信.md "wikilink")は安全な暗号の要求を高めたが、20世紀になっても19世紀的な暗号手法を組み合わせた方式が使われ続け、しかもその多くは時間の問題で、解読されていった。この状況は1915年〜1918年頃に各国で[機械式暗号](../Page/機械式暗号.md "wikilink")が発明されるまで続く。暗号の歴史については[暗号史](../Page/暗号史.md "wikilink")を参照。

第一次世界大戦中に使用されたADFGX／ADFGVX暗号もそのような解読された暗号の一つとして有名である。

ADFGX暗号がドイツ軍に採用されたのは、1918年にはじまるドイツ軍の大規模攻撃（3月21日）の直前のことである。ドイツ軍は[換字式](../Page/換字式暗号.md "wikilink")、[転置式を組み合わせたこの暗号を安全なものと信じて採用した](../Page/転置式暗号.md "wikilink")。

しかし、フランスの暗号解読者ジョルジュ・パンヴァンは、数ヶ月の努力によってADFGX暗号の解読に成功した。するとドイツ軍はADFGX暗号を改良したADFGVX暗号を導入し、再び解読できなくなった。1918年[6月](../Page/6月.md "wikilink")、ドイツ軍は[パリ](https://ja.wikipedia.org/wiki/パリ "wikilink")から100[キロまで迫っていた](../Page/キロメートル.md "wikilink")。兵力も十分。連合国側の最後の望みはADFGVX暗号を解読し、ドイツ軍の攻撃目標を見つけることであった。[6月1日](../Page/6月1日.md "wikilink")、パンヴァンの元に暗号文が届けられると、翌日の夜には解読成功。ドイツ軍の猛攻をしのぎ、撃退することができた。

## 暗号方式

### 鍵生成

[thumb](https://ja.wikipedia.org/wiki/ファイル:ADFGVX暗号.fig2.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:ADFGVX暗号.fig1.png "wikilink") ADFGVX暗号の[鍵は](../Page/鍵_\(暗号\).md "wikilink")、換字表（図1,2）と鍵文字（置換鍵を決める合言葉）との2つである。

1.  図1にa〜z、0〜9の36文字をランダムに入れて、換字表を作成する（図2）。
2.  次に鍵文字を決める。今回はweasel([イタチ](../Page/イタチ.md "wikilink"))を使う。

補足：鍵文字から次のようにして転置鍵を求める。まず、鍵文字から重複している文字を消す。weaselの場合、eはwの次とsの次にあるが、sの次にあるほうが後なので、このeを消す。するとweaslの5文字となる。各文字をアルファベット順に1,2,3...の数字に置き換える。weaslは**52143**となる。これが転置鍵となる。

実際には、鍵文字は2ダース程度の文字数で、換字表・鍵文字共に毎日に更新されていた。

### 暗号化

[thumb](https://ja.wikipedia.org/wiki/ファイル:ADFGVX暗号.fig4.png "wikilink")

換字表と鍵文字（転置鍵）を使って、平文を次のように変換する。

1.  平文を1文字ずつ、換字表(図2)を使って変換する。例えば**i→FA**となる。平文を**I am going**とすると、一次暗号文 **FADVAGXXDXFAGDXX**ができる。ここまでは単なる[ポリュビオスの暗号表](../Page/ポリュビオスの暗号表.md "wikilink")であって、[頻度分析によって解読されてしまう](../Page/頻度分析_\(暗号\).md "wikilink")。
2.  図3に示すように一次暗号文を、転置鍵のサイズ（5文字）で改行して書き出し、**12345**の順に縦に読み出すと二次暗号文**DXGAXAAXXVDDFGFX**が得られる。

### 復号

復号は暗号化の手順を逆に行う。

## 解読方法

  - 転置鍵(鍵幅は通常15〜22)と6x6の換字表は毎日更新され、連合国の解読者は同じ鍵の暗号文を集めて解読した。
  - 解読はまず転置矩形のサイズ(鍵幅)を推定し、ついで元の配列に戻し、最後に頻度分析から換字表を復元した。

### 特別解読法

  - 大戦中に連合国が編み出した解読方法は、3つの特別解読法(Special solution)であった。

<!-- end list -->

1.  平文での末尾部が同じである2通の暗号文を入手した場合。
2.  平文での冒頭部が同じである2通の暗号文を入手した場合。
3.  文字数の因数分解から、ある特定サイズの矩形が転置に用いられたと確信した場合(例えば703文字であれば、19x37または37x19の矩形サイズである)

### 一般解読法

  - 一般解読法(General solution)が編み出されたのはドイツ降伏後であった。

## 参考文献

文献1は特別解読および一般解読について解説。文献2は一般解読のみだが当時の暗号文が付録されている。

1.  William F. Friedman, "Military Cryptanalysis: Transposition and Fractionating Systems", Cryptographic Series, No 61, Part 4, Aegean Park Press, 1993/12 (ISBN 0-89412-198-7)
2.  J. Rives Childs, "General Solution of the ADFGVX cipher system", Cryptograhic Series, C-88, Aegean Park Press, 2000/3/1 (ISBN 0-89412-284-3)

[Category:暗号](https://ja.wikipedia.org/wiki/Category:暗号 "wikilink")