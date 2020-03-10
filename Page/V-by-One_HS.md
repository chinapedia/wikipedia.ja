> この記事は[V-by-One HS](https://ja.wikipedia.org/wiki/V-by-One_HS)から翻訳されています。


**V-by-One HS**は、電気信号を伝送する[インターフェースの一つで](../Page/インタフェース_\(情報技術\).md "wikilink")、特に[薄型テレビ](https://ja.wikipedia.org/wiki/薄型テレビ "wikilink")向けに[ザインエレクトロニクス社](https://ja.wikipedia.org/wiki/ザインエレクトロニクス社 "wikilink")により開発された。現在では、マルチ・ファンクション・プリンタなどの事務機器、[車載インフォテイメント](https://ja.wikipedia.org/wiki/車載インフォテイメント "wikilink")、ロボット、セキュリティなどの広範な分野に適用されている。

従来、薄型テレビの内部配線において、その画像信号の伝送に[LVDSが標準的に用いられてきたが](https://ja.wikipedia.org/wiki/Low_voltage_differential_signaling "wikilink")、高[解像度](https://ja.wikipedia.org/wiki/解像度 "wikilink")化と[色深度](../Page/色深度.md "wikilink")拡張により、必要な伝送速度が高速化し、ケーブル間のタイミングのずれ(スキュー)の問題が顕在化してきた。**V-by-One HS**は、[SerDes](https://ja.wikipedia.org/wiki/SerDes "wikilink")に加え、[クロック・データ・リカバリ](../Page/クロック・データ・リカバリ.md "wikilink")等の技術を取り入れ、1ペアあたり3.75Gbpsの高速伝送を実現しながら、スキューの問題を解決すると共に、[EMI](https://ja.wikipedia.org/wiki/電波障害 "wikilink")、消費電力を低減している。また、伝送ペア数の削減でケーブル・コネクタなどのトータルコスト低減が可能とされる。

## 概要

  - 大型[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")の画像入力信号の[VESA](../Page/VESA.md "wikilink")標準仕様であるLVDSを置き換えることを目的として開発された。
  - イコライザ機能の導入により、従来のLVDSに比べて伝送品質を向上している。
  - クロック・データ・リカバリの採用で、従来のLVDSで顕在化したケーブルスキューの問題を解決している。
  - 従来のLVDSで必要とされたクロック伝送ケーブル（固定周波数の伝送）が無く、EMIノイズが低くなる。
  - 最大3.75Gbps伝送を可能とし、ケーブル本数、コネクタ数が減り、トータルコスト低減、省スペース化が実現される。
  - 伝送速度が可変なため、固定周波数の伝送仕様に比べ、低消費電力にできる。 シリアル伝送速度　：　600Mbps　～ 3.75Gbps
  - 従来のLVDSによる設計から大きく変更することがなくシームレスな移行を可能としている。
  - 開発元のザインエレクトロニクス社から仕様が公開され、オープンスタンダードとなっている。

## 開発までの経緯

液晶ディスプレイは[ブラウン管](../Page/ブラウン管.md "wikilink")ディスプレイと異なり、個々[ピクセル](../Page/ピクセル.md "wikilink")を表示する信号はデジタル信号でなければならない。液晶ディスプレイがノートパソコンに応用が始まった当初、画像信号はパラレル信号として伝送されていたが、18ビットカラーの色深度でもRGB6本ずつと制御信号3本にクロックと22本もの信号線が必要となり配線スペースやスキュー調整の難しさなどの問題があった。

これらの問題を解決するために、液晶ディスプレイ向けの[インターフェースとしてLVDSの応用が考案された](../Page/インタフェース_\(情報技術\).md "wikilink")。LVDSは、TIA/EIA-644で規格される差動伝送方式で、高速化が可能なため液晶ディスプレイ向けでは画像信号をシリアル化して伝送する。導入当初は18ビットカラーが主流であったため、RGBそれぞれ6ビットと制御信号3ビットの合計21ビットを、3chの差動信号ペアに7ビットずつ振り分け、クロックの1chと合わせて4ペアの配線でシリアル伝送する仕様が提案された。つまり[パラレル通信](https://ja.wikipedia.org/wiki/パラレル通信 "wikilink")では22本必要だった配線が8本で[シリアル通信](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")できるようになった。この方式がビデオ周辺機器に関する業界標準化団体VESAに標準仕様として採用され、液晶ディスプレイ向けインターフェースとして、広くLVDSが普及することになった。

その後、液晶ディスプレイの高解像度化と色深度拡張が進み、また液晶ディスプレイの欠点とされる応答速度の向上のために[倍速駆動](https://ja.wikipedia.org/wiki/倍速駆動 "wikilink")といった技術の導入もあって、液晶ディスプレイに入力するべき画像信号のデータ量は増大の一途となった。

その結果、例えばフルハイビジョン（1920×1080）で10ビット色深度の倍速パネルとではLVDSでも24ペア48本もの配線が必要になってしまった。そして伝送クロックも高速となり、数百psオーダーのスキュー調整が必要になっている。さらに従来のLVDSの仕様では固定周波数のクロック伝送が必要で、スペクトルが集中するため、無線LANなどに影響を与えないようにEMIを抑制することが難しくなっている。

加えてLVDSは規格上、GNDから1.2Vの電圧を中心に変化する電気信号を伝送しなければならない。[LSI](https://ja.wikipedia.org/wiki/LSI "wikilink")の微細化が進み、この電圧の規格がLSI設計上、大きな制限をもたらすようになっていた。 このような中、[DVIや](https://ja.wikipedia.org/wiki/Digital_Visual_Interface "wikilink")[HDMI](https://ja.wikipedia.org/wiki/High-Definition_Multimedia_Interface "wikilink")、[DisplayPort](../Page/DisplayPort.md "wikilink")といった様々なインターフェースの仕様が提案され、実用化されてきた。

DVIとHDMIはスキュー調整の機能がついており、HDMIにはコンテンツ保護機能として[HDCPを実装しているため](https://ja.wikipedia.org/wiki/コピーガード "wikilink")、機器間の画像信号伝送としては最適で広く普及が始まっている。しかしながら実装にはライセンス費用が必要な上、機器内の画像信号伝送としては、機能が冗長で消費電力も大きくなるため、応用されることはなかった。

DisplayPortはVESAにおいてLVDSを置き換える仕様として規格されたもので、今後の普及が期待されている。伝送方式の仕様は[PCI Expressに似たバイアスとなっており](https://ja.wikipedia.org/wiki/PCI_Express "wikilink")、LSI設計上の障壁が低いとされる。しかしHDMIと同様、機器間伝送を想定してHDCPが実装されているため、機器内の画像信号伝送としては、機能が冗長で消費電力も大きくなることが懸念されている。さらにDisplayPortは伝送速度が固定で、様々なクロック周波数が存在する画像信号に対し遅い周波数では大きな無駄が発生する上に、受信側でクロックを再生する必要がある。これらの理由から、LVDSからの移行には解決しなければならない課題が多い。

以上に述べた背景に基づき**V-by-One HS**の開発が進められた。すなわちイコライザ機能の導入により、従来のLVDSに比べて伝送品質を向上し、さらなる高速化（最大1ペアあたり3.75Gbps）を実現している。また [クロック・データ・リカバリ](../Page/クロック・データ・リカバリ.md "wikilink")の採用で、従来のLVDSで顕在化したケーブルスキューの問題を解決した。そしてLVDSで必要とされたクロック伝送ケーブル（固定周波数の伝送）が無いため、EMIノイズが低くなるという。

伝送速度の高速化でケーブル本数、コネクタ数が減り、トータルコスト低減、省スペース化が実現できると期待される。例えばUDパネル（3840×2160）では、LVDSを用いると96ペアのケーブルが必要なのに対して、V-by-One HSでは16ペアで伝送可能である。また伝送速度が可変なため、従来のLVDSによる設計から大きく変更することがなくシームレスな移行が可能になる。さらに、開発元のザインエレクトロニクス社から仕様が公開され、オープンスタンダードとなっている。

## 関連項目

  - [Low voltage differential signaling](https://ja.wikipedia.org/wiki/Low_voltage_differential_signaling "wikilink")
  - [High-Definition Multimedia Interface](https://ja.wikipedia.org/wiki/High-Definition_Multimedia_Interface "wikilink")
  - [DisplayPort](../Page/DisplayPort.md "wikilink")

## 外部リンク

  - [V-by-One® (SerDes)｜製品紹介｜ザインエレクトロニクス-Mixed Signal LSI-THine](http://www.thine.co.jp/products/pr_details/V-by-One.html)

[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink")