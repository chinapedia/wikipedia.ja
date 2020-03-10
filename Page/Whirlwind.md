> この記事は[Whirlwind](https://ja.wikipedia.org/wiki/Whirlwind)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Whirlwind_1_\(2103090140\).jpg "wikilink") **Whirlwind**（ホワールウィンド、原義は「[つむじ風](https://ja.wikipedia.org/wiki/つむじ風 "wikilink")」）とは、[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")（MIT）で開発された[コンピュータ](../Page/コンピュータ.md "wikilink")である。[リアルタイム処理](https://ja.wikipedia.org/wiki/リアルタイム処理 "wikilink")を念頭に置いた世界初のコンピュータであり、出力機器として世界初の[モニター端末を使い](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")、従来の機械システムの電子的置換ではない初めてのシステムと言われている。その開発は、直接的には[アメリカ空軍](https://ja.wikipedia.org/wiki/アメリカ空軍 "wikilink")の[SAGEシステムに受け継がれ](https://ja.wikipedia.org/wiki/半自動式防空管制組織 "wikilink")、間接的には[1960年代](../Page/1960年代.md "wikilink")の商用コンピュータに影響を及ぼした。

## 背景

[第二次世界大戦](https://ja.wikipedia.org/wiki/第二次世界大戦 "wikilink")中、[アメリカ海軍](../Page/アメリカ海軍.md "wikilink")はMITに[爆撃機](../Page/爆撃機.md "wikilink")の乗組員を訓練するための[フライトシミュレータ](https://ja.wikipedia.org/wiki/フライトシミュレータ "wikilink")を制御するコンピュータの開発が可能か打診した。彼らが想定していたのは、パイロットの操作に基づいて計器盤の表示を継続的にシミュレートするという単純なコンピュータであった。従来の[リンクトレーナ](https://ja.wikipedia.org/wiki/リンクトレーナ "wikilink")とは異なり、彼らの想定したシステムは[空気力学](https://ja.wikipedia.org/wiki/空気力学 "wikilink")的モデルに基づいた実物に限りなく近いものであり、様々な航空機の訓練に使えるものだったのである。

MITサーボ機構研究室はそのようなシステムは開発可能であるとの結論に至った。それを受けて海軍は「Project Whirlwind」の名前で資金提供を決定し、プロジェクトの責任者として[ジェイ・フォレスター](https://ja.wikipedia.org/wiki/ジェイ・フォレスター "wikilink")が選任された。彼らは即座に大型の[アナログコンピュータ](https://ja.wikipedia.org/wiki/アナログコンピュータ "wikilink")を開発したが、それは正確さに欠け、柔軟性に乏しかった。その問題を解決するにはさらに大型のシステムが必要だったが、それは到底製造可能とは考えられなかった。

[1945年](../Page/1945年.md "wikilink")、MITのチームの一員であったジェリー・クローフォードは[ENIAC](../Page/ENIAC.md "wikilink")のデモンストレーションを見てデジタル式コンピュータが解決策となるかもしれないと示唆した。デジタル式であれば、部品を追加する代わりにプログラムを追加すれば[シミュレーション](../Page/シミュレーション.md "wikilink")の正確性を向上させることができる為であった。当時の認識ではコンピュータは十分に高速であり、どんな複雑なシミュレーションでも理論的には可能と思われた。

当時のコンピュータは一度にひとつのタスクを実行する[バッチ処理](https://ja.wikipedia.org/wiki/バッチ処理 "wikilink")用に開発されていた。入力データが事前に用意され、コンピュータがそれを使って計算を行い、結果を出力する。しかしこれではWhirlwindシステムには不十分である。Whirlwindでは、時々刻々と変化する入力に対して連続的に計算を行う必要があった。速度が最も大きな問題となった。一般のシステムでは計算結果がプリントアウトされるのをじっと待っているのが普通だったが、Whirlwindでは速度が遅いとシミュレーションできる複雑さが極端に制限されてしまう。

## 詳細

### 設計と製造

[1947年](../Page/1947年.md "wikilink")、フォレスターとエヴァレットは高速な[プログラム内蔵式コンピュータの設計を完了した](../Page/プログラム内蔵方式.md "wikilink")。当時の多くのコンピュータは「ビット直列」式で動作していた。これは1ビットの演算を繰り返し実行することでワード長ぶんの処理を行う方式で、ワード長は48ビットとか60ビットと長かった。しかしこの方式は彼らの用途には性能が悪すぎたので、Whirlwindは16ビットを並列に処理する演算回路を備え、ワード長も 16ビットとして、サイクル毎に「ビット並列」式で演算が行えた。メモリの速度を無視すれば Whirlwind は当時の他のコンピュータの 16倍の高速性を誇っていた。現在ではほとんどのコンピュータはこの方式を採用していて、さらに 32ビットや 64ビットのワードを一度に処理するようになっている。

ワード長はちょっとした考慮のうえで決定された。マシンは命令毎にひとつのメモリアドレスを指定されて動作する。二つのオペランドに対する演算をする場合（例えば加算をする場合）、もう一方のオペランドは直前の命令のオペランドを使用するものとされた。したがって、Whirlwindのプログラムは[逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink")の[電卓](../Page/電卓.md "wikilink")に似ている。ただし、オペランドのスタックがあるわけではないが。設計者は最低でも2000ワード分のメモリが必要であると考え、アドレスのビット幅を11ビットとし、さらに16～32種類の命令を識別するための命令コード用の 5ビットを加えて、ワード長を 16ビットとしたのである。[ジョン・フォン・ノイマン](../Page/ジョン・フォン・ノイマン.md "wikilink")はこのワード長の小ささを聞いて、Whirlwindに興味を持たなかったという（彼の興味は科学技術計算にあり、精度を上げるためにワード長が長くなければならなかった）。

マシンの建造は翌年から開始された。これには175人（うち70人が技術者）が関わっている。Whirlwindは完成までに 3年を費やし、[1951年](https://ja.wikipedia.org/wiki/1951年 "wikilink")4月20日に動作した。当初海軍のフライトシミュレータ向けだったものが、完成時には空軍の[SAGE向けになっていた](https://ja.wikipedia.org/wiki/半自動式防空管制組織 "wikilink")。プロジェクトは毎年百万ドルを消費し、海軍は既に興味を失っていたのである。一方空軍では、[冷戦](../Page/冷戦.md "wikilink")の勃発、航空機のジェット化による高速化、また特に[ソ連の](https://ja.wikipedia.org/wiki/ソビエト連邦 "wikilink")[原子爆弾](../Page/原子爆弾.md "wikilink")完成により、可能な限り迅速に未確認機の発見と要撃管制、敵の侵攻であれば即座に撃墜できる態勢を整えることが喫緊の急務であり、自動化された機械の助け無くしてジェット機による核攻撃を防ぐことは不可能であった。このためWhirlwindを彼らのプロジェクトに組み込んだ結果であった。

### マシンの「コア」

[thumb](https://ja.wikipedia.org/wiki/ファイル:Project_Whirlwind_-_core_memory,_circa_1951_-_detail_2-1.JPG "wikilink") 当初の速度は非常に遅く（20KIPS）、実用には程遠かった。トラブルの原因のほとんどは[主記憶装置](../Page/主記憶装置.md "wikilink")として[ウィリアムス管](https://ja.wikipedia.org/wiki/ウィリアムス管 "wikilink")を使っていたためである。フォレスターはこれを改善する技術を探し、らせん状の磁気テープなどを試したが、最終的に[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")にたどり着いた。これによって性能は約二倍（40KIPS）となった（[1953年](https://ja.wikipedia.org/wiki/1953年 "wikilink")）。加算は 49マイクロ秒、乗算は 61マイクロ秒かかっていた（磁気コアメモリを使う前の値）。

磁気コアメモリを実装することで、Whirlwindは当時の世界最高速コンピュータとなった。加算時間は8マイクロ秒、乗算時間は25.5マイクロ秒、除算は57マイクロ秒（ただし、メモリアクセス時間を除く）となった。[磁気ドラムメモリ](https://ja.wikipedia.org/wiki/磁気ドラムメモリ "wikilink")では8,500マイクロ秒だったアクセス時間が、磁気コアメモリでは8マイクロ秒に改善されている。

この高速化によって[SAGEで十分使える性能となり](https://ja.wikipedia.org/wiki/半自動式防空管制組織 "wikilink")、[AN/FSQ-7](https://ja.wikipedia.org/wiki/AN/FSQ-7 "wikilink") という量産機を製造して使用する段階となった。当時、[RCA](https://ja.wikipedia.org/wiki/RCA "wikilink")が有力だったが、[IBM](../Page/IBM.md "wikilink")がその製造業者に選ばれた。IBMは後にこのシステムで培われたリアルタイム技術を[SABRE](https://ja.wikipedia.org/wiki/SABRE "wikilink")システム（航空機のチケット予約システム）で商用化している。AN/FSQ-7 の製造は[1957年](../Page/1957年.md "wikilink")に開始され、同時に建物や送電施設や通信ネットワークがSAGEシステムのために建設された。

## Whirlwind のその後

Whirlwind IIは、1959年6月30日までSAGEにおいてサポート役を果たした。その後1970年代後半までプロジェクトメンバーのBill Wolfが年1ドルでマシンを借りていた。その後[ケン・オルセン](https://ja.wikipedia.org/wiki/ケン・オルセン "wikilink")がこれを買い取って一時的に所有していたが、[スミソニアン博物館](../Page/スミソニアン博物館.md "wikilink")に寄贈した。

Whirlwindは約5000本の[真空管](https://ja.wikipedia.org/wiki/真空管 "wikilink")で構成されていた。そのデザインをそのままトランジスタ化する作業が[ケン・オルセン](https://ja.wikipedia.org/wiki/ケン・オルセン "wikilink")によって行われており、[TX-0](https://ja.wikipedia.org/wiki/TX-0 "wikilink")として知られている。これが成功を収めたので、さらに大規模化したTX-1が計画された。しかしこのプロジェクトは野心的すぎたため、規模を縮小して[TX-2](https://ja.wikipedia.org/wiki/TX-2 "wikilink")が完成した。これもトラブルが多いマシンであったが、オルセンは途中でプロジェクトを抜けて[デジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/デジタル・イクイップメント・コーポレーション "wikilink")社（DEC）を設立。DECの[PDP-1](https://ja.wikipedia.org/wiki/PDP-1 "wikilink")はTX-0とTX-2のコンセプトを集めて、より小さなマシンに仕立てたものである。

## 参考文献

  - John F. Jacobs, *The SAGE Air Defense System: A Personal History* (MITRE Corporation, 1986) Whirlwindに関する様々な資料を含む
  - 『コンピューター200年史 －情報マシーン開発物語－』M.キャンベル＝ケリー他(著)、山本菊男(訳)、海文堂（1999年）、ISBN 4-303-71430-5

## 外部リンク

いずれも英文。

  - [Computer Structures: Readings & Examples — The Whirlwind I computer](http://www.research.microsoft.com/~gbell/Computer_Structures__Readings_and_Examples/00000157.htm)
  - [Whirlwind documentation](http://www.bitsavers.org/pdf/mit/whirlwind)

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:1940年代のコンピュータ](https://ja.wikipedia.org/wiki/Category:1940年代のコンピュータ "wikilink") [Category:1950年代のコンピュータ](https://ja.wikipedia.org/wiki/Category:1950年代のコンピュータ "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink") [Category:真空管式コンピュータ](https://ja.wikipedia.org/wiki/Category:真空管式コンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink")