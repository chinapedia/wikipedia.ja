> この記事は[NOR型フラッシュメモリ](https://ja.wikipedia.org/wiki/NOR型フラッシュメモリ)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:IPhone_3G_teardown_-_Intel_3050M0Y0CE_-3303.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:NOR_flash_layout.svg "wikilink") **NOR型フラッシュメモリ**（ノアがたフラッシュメモリ）は、[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")の一種である。

[NAND型フラッシュメモリ](../Page/NAND型フラッシュメモリ.md "wikilink")とは異なり、データの読み出しにおいて、[RAMと同様にアドレス指定によるアクセスができ](../Page/Random_Access_Memory.md "wikilink")、コードをRAMにコピーすることなく直接実行すること(execute in place)が可能。

データの書き込みについては、一度ブロック単位で消去した後、書き込むという手順を踏む。この手順についてはIntel系コマンドやAMD系コマンドなどがあるが、チップの特性情報を読み出すコマンドは共通フラッシュメモリインターフェース(Common Flash memory Interface) として標準化されている。用途として、[マイコン](../Page/マイコン.md "wikilink")をはじめ、高い信頼性が求められる[ルーター](../Page/ルーター.md "wikilink")、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")、[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")、[GPS](../Page/グローバル・ポジショニング・システム.md "wikilink")、車載機器、[携帯電話](../Page/携帯電話.md "wikilink")や[PDAなど](../Page/携帯情報端末.md "wikilink")、どれもハードディスクが使用できない環境で[ファームウェア](../Page/ファームウェア.md "wikilink")の格納等に使われる。

従来はデータの信頼性にも優れ、NAND型フラッシュメモリで必要な[エラー訂正](../Page/誤り検出訂正.md "wikilink")(ECC)が不要であるとされていたが、半導体プロセスの微細化によって\[1\]等が無視できないレベルに達したため、現在ではNORフラッシュでもECCの利用が必要である。

読み出し速度、[ランダムアクセス](../Page/ランダムアクセス.md "wikilink")が高速な一方、NAND型に比べ、集積度が劣る、書き込みが遅いなどの欠点が挙げられる。

NAND型に比べ、高い信頼性を特長とするNOR型は、従来の[ROMの代わりにファームウェアを格納するメモリとして基板に直接実装される形で利用されていることが多い](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")。また、近年マルチビット化により大容量化が進み、1チップで1Gビットの製品も発表され\[2\]、NAND型に対抗できる製品も出てくるようになった。これらの製品では、書き込み時の高速化および消費電力が改善、集積度の向上などが図られている。

## 脚注

<references />

## 関連項目

  - [フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")
  - [東芝](../Page/東芝.md "wikilink")
  - [舛岡富士雄](../Page/舛岡富士雄.md "wikilink") - 発明者。[1984年](../Page/1984年.md "wikilink")に発明し、[1988年](../Page/1988年.md "wikilink")にインテルが商用として発売した。

[en:Flash memory\#NOR memories](https://ja.wikipedia.org/wiki/en:Flash_memory#NOR_memories "wikilink")

[Category:半導体メモリ](https://ja.wikipedia.org/wiki/Category:半導体メモリ "wikilink")

1.  <http://www.hitachi.co.jp/rd/portal/contents/story/softerr/index.html>
2.  <http://www.micron.com/products/datasheets/18b2cc63-9a5b-4cab-bcca-c1296342aeae>