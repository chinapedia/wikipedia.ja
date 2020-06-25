> この記事は[Cromemco Cyclops](https://ja.wikipedia.org/wiki/Cromemco_Cyclops)から翻訳されています。


**Cromemco Cyclops**（クロメンコ サイクロプス）は、[クロメンコ](../Page/クロメンコ.md "wikilink")が[1975年](../Page/1975年.md "wikilink")に発売した[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")であり、世界初の商用化された完全デジタル処理のカメラである。画像素子として[MOSイメージセンサを使用していた](../Page/MOSFET.md "wikilink")\[1\]。初の[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")へのインターフェイスを持つデジタルカメラである。イメージセンサは1[kbの](https://ja.wikipedia.org/wiki/キビバイト "wikilink")[DRAM](https://ja.wikipedia.org/wiki/DRAM "wikilink")メモリチップを改造したもので、解像度は32×32[画素](https://ja.wikipedia.org/wiki/画素 "wikilink")（0.001メガピクセル）だった\[2\]。

Cyclopsとは、ギリシャ神話に登場する単眼の巨人[キュクロープス](../Page/キュクロープス.md "wikilink")のことで、このカメラが単眼であることからその名がつけられたものである\[3\]。

## 背景

[Cyclops_Camera_-_Popular_Electronics_correspondence_1974.jpg](https://ja.wikipedia.org/wiki/File:Cyclops_Camera_-_Popular_Electronics_correspondence_1974.jpg "fig:Cyclops_Camera_-_Popular_Electronics_correspondence_1974.jpg")』誌編集長からのカメラプロジェクト「CYCLOPS」の取材記事掲載についての手紙。\]\] Cyclopsは、テリー・ウォーカー、[ハリー・ガーランド](../Page/ハリー・ガーランド.md "wikilink")、[ロジャー・メレン](../Page/ロジャー・メレン.md "wikilink")の3人によって開発され、『[ポピュラーエレクトロニクス](https://ja.wikipedia.org/wiki/ポピュラーエレクトロニクス "wikilink")』1975年2月号でホビイストの電子工作として紹介された\[4\]。

その1ヶ月前の同誌では、[MITS社のマイクロコンピュータ](../Page/Micro_Instrumentation_and_Telemetry_Systems.md "wikilink")[Altair 8800が紹介されていた](../Page/Altair_8800.md "wikilink")\[5\]。『ポピュラーエレクトロニクス』誌の技術編集者であるレス・ソロモンは、CyclopsとAltairのインターフェイスに価値を見出し、Cyclopsの開発者の1人のロジャー・メレンと、MITS社の社長である[エド・ロバーツ](../Page/エド・ロバーツ.md "wikilink")に連絡を取り、コラボレーションについて話し合うことにした\[6\]。

メレンは[ニューメキシコ州](../Page/ニューメキシコ州.md "wikilink")[アルバカーキ](../Page/アルバカーキ.md "wikilink")のMITS本社でロバーツと会った。ロバーツはメレンに、AltairとCyclopsのインターフェイスを製作することを勧め、彼らがこのプロジェクトをすぐに開始できるよう、メレンにAltairを速やかに送ることを約束した\[7\]。

カリフォルニアに帰ったメレンは、ガーランドと、Cyclops等のAltair用の製品を製造するための[パートナーシップ](../Page/パートナーシップ.md "wikilink")を結び、その名前を[クロメンコ](../Page/クロメンコ.md "wikilink")とした\[8\]。1976年1月、MITS社はAltairの最初の周辺機器としてCromemco Cyclopsを発表した\[9\]\[10\]\[11\]。

## 技術

[Cromemco_1024-element_image_sensor_used_in_Cyclops_Camera_(1975).jpg](https://ja.wikipedia.org/wiki/File:Cromemco_1024-element_image_sensor_used_in_Cyclops_Camera_\(1975\).jpg "fig:Cromemco_1024-element_image_sensor_used_in_Cyclops_Camera_(1975).jpg") [Cromemco_Cyclops_Camera_(1976)_2.jpg](https://ja.wikipedia.org/wiki/File:Cromemco_Cyclops_Camera_\(1976\)_2.jpg "fig:Cromemco_Cyclops_Camera_(1976)_2.jpg") Cyclopsは、MOSメモリチップを改造した革新的なイメージセンサを使用していた\[12\]。チップ上面のカバーを取り外し、そこにガラスの板を取り付けて、半導体に直接光が当たるようにした。動作理論については、『ポピュラーエレクトロニクス』のオリジナル記事に記載されている\[13\]。最初は、32×32の配列に配置された1024個のメモリセルが、全て"1"の状態になっている。光が当たったメモリセルは、その状態が"0"に変化する。光が強ければ強いほど、"1"から"0"に変化するスピードが速くなる。

25mm F2.8のDマウントレンズにより、イメージセンサに像を結ぶように調整されている。各メモリセルの状態のスキャンを計16回行う。1回目のスキャンでは、全てのメモリセルの状態が"1"になっている。当たる光が強いセルほど"1"から"0"に早く変化するので、各セルが"1"から"0"に変わったタイミング（すなわち、そのときのスキャン回数）によって、各セルに当たる光の強さが分かる。ほとんど光が当たっていないセルは、最後まで"1"のままである。このようにして、Cyclopsは16階調の[グレースケール](https://ja.wikipedia.org/wiki/グレースケール "wikilink")のイメージを取得する。

Cyclopsには2つのバイアスライトがついており、低照度環境での感度を向上させることができる。このライトは手動でも、コンピュータ制御でも調整可能で、センサに均一な低レベルの光を照射することができる。一度調整すれば、低照度環境下でも、イメージからのわずかな入射光に対しても感度が向上する。

## 脚注

## 外部リンク

  -
  -
  - \- [Twitter](../Page/Twitter.md "wikilink")

  -
  - [Cromemco Cyclops Camera Controller manual.](http://www.hartetechnologies.com/manuals/Cromemco/Cromemco%2088%20CCC%20Manual.pdf)

  - [Cromemco Cyclops Camera manual.](http://www.hartetechnologies.com/manuals/Cromemco/Cromemco%2088%20ACC%20Manual.pdf)

[Category:アメリカ合衆国の発明](https://ja.wikipedia.org/wiki/Category:アメリカ合衆国の発明 "wikilink") [Category:デジタルカメラ](https://ja.wikipedia.org/wiki/Category:デジタルカメラ "wikilink") [Category:イメージセンサ](https://ja.wikipedia.org/wiki/Category:イメージセンサ "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.