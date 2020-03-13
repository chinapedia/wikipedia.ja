> この記事は[Broadcast Markup Language](https://ja.wikipedia.org/wiki/Broadcast_Markup_Language)から翻訳されています。


**Broadcast Markup Language** (**BML**) とは、[XMLベースの](../Page/Extensible_Markup_Language.md "wikilink")[データ放送](../Page/データ放送.md "wikilink")向けの[記述言語でARIB](../Page/データ記述言語.md "wikilink")（社団法人[電波産業会](../Page/電波産業会.md "wikilink")）によって策定されている。

[BSデジタル放送](../Page/衛星放送.md "wikilink")、[110度CSデジタル放送](../Page/衛星放送.md "wikilink")、[地上デジタル放送で使用されている](https://ja.wikipedia.org/wiki/地上デジタルテレビジョン放送 "wikilink")。 それぞれ対応の受信機には、BMLを表示、実行する「BMLブラウザ」が搭載されている。

[XHTMLをベースに](../Page/Extensible_HyperText_Markup_Language.md "wikilink")、[デジタル放送に向いた拡張が盛り込まれている](../Page/デジタル放送の一覧.md "wikilink")。 地上デジタル放送の場合、Aプロファイル、B プロファイル、C プロファイルと3種類の[プロファイルがあり](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")、A プロファイルは固定型[テレビ](../Page/テレビ.md "wikilink")用のデータ放送。C プロファイルは[ワンセグ](../Page/ワンセグ.md "wikilink")向け放送用のデータ放送規格として規格化されている。B プロファイルは移動受信向けのデータ放送規格だが、規格化は未定となっている。 これは車載向け3セグメント放送が（主にアンテナ技術の向上により）普通の家庭向け13セグメント放送で高感度受信できるメドが立ち、規格化の必要性がほぼなくなってしまったことによる。

## 実装

BMLは通常、BMLの仕様（ARIB STD-B24）によってサブセット化された[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")（これをBML文書と呼ぶ）と[JavaScript](../Page/JavaScript.md "wikilink")を標準化した[ECMAScript](../Page/ECMAScript.md "wikilink")、[PNG](../Page/Portable_Network_Graphics.md "wikilink")（静止画及び動画:MNGに対応。8bit index colorのみ）、[JPEG](../Page/JPEG.md "wikilink")（プロファイルはARIB STD-B24で規定される）、[MPEG](../Page/Moving_Picture_Experts_Group.md "wikilink")(MPEG1,MPEG2)、MPEG Audio、バイナリーテーブル（ECMAScript上でスキーマを定義してES上から抽出できるデータセットの一種）のセットによって構成される（これを[マルチメディア](../Page/マルチメディア.md "wikilink")[コンテンツ](../Page/コンテンツ.md "wikilink")と呼び、構成要素を[モノメディア](https://ja.wikipedia.org/wiki/モノメディア "wikilink")と呼ぶ）。ECMAScriptによりDHTML的な動的コンテンツ作成が可能である。さらにイベントと呼ばれるメカニズムによりES(Elementary Stream)上の変化を検出し、放送局側からコンテンツに動きを与える事が出来る。例えば、相撲の中継において勝敗表をテレビ局側から送出システムに入力すると直ちに受信機にイベントが発生し、ECMAScriptによってBML文書のDOMツリー上のデータを書き換える事でリアルタイムに情報を反映する事が出来る（これらのイベントドリブン的なデータ伝送にはもっぱらバイナリーテーブルが使われる）。この他、ECMAScriptには受信機側から電話回線（BASIC手順）・LAN([TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink"))によって放送局側へデータを伝達する機構（双方向機能/双方向通信機能）がある。こちらはプライバシーの問題や費用が視聴者・局側両方に発生する事から、それほど普及していない。[B-XML](https://ja.wikipedia.org/wiki/B-XML "wikilink")は、よりXMLとしての使い方を追求したARIB STD-B24で規定される異なる仕様だが、現在運用されていない。

## セキュリティ

BMLにはいくつかのセキュリティが施されている。これはECMAScriptによって受信機から個人情報等を読み取る事が可能である事、双方向通信によって読み出した個人情報等を第三者に送りつける事が可能である為である。まず第一のセキュリティは放送設備によって実現している。許可されない者が許可されていないコンテンツを送らない様に保護している。しかしながらこれは放送局のセキュリティポリシーによって実現している為完全ではない。第二のセキュリティは放送局識別情報によって行われる。ある放送波によって書き込まれた情報は、他の放送波によって送りつけられたECMAScriptから読み取る事が出来ない。これにより他局の情報を回収するといった行為が禁止される。第三のセキュリティはB-CASカードによって実現している。B-CASカードに書き込まれるデータは暗号化される。したがって復号鍵が無い状態でデータを読み込む事は出来ない。より強固なセキュリティの提案もあったが、むしろ重要な情報を受信機にむやみに書き込まないというポリシーの方が現実的であった為、現在受信機に保存されている個人情報等は必要最小限にとどめ、デジタル放送初期にみられた完全な個人情報の記録は、ポリシー制定合意に伴い削除された。なお、受信機に使われるメモリは[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")が使われており[ウェアレベリング](../Page/ウェアレベリング.md "wikilink")によってデータ書き込み先の分散が行われている。その為、ECMAScript上から削除されても、物理的には記録が残っている可能性がある。その為、受信機には、個人情報が保存されている可能性がある注意書きが添えられている。

## 文字コード

BMLでは[JIS X 0208の空き領域に独自の漢字や記号類を追加した文字集合を使用する](../Page/JIS_X_0208.md "wikilink")。エンコーディングはBML宣言で宣言される。ワンセグのデータ放送では[Shift_JIS](../Page/Shift_JIS.md "wikilink")エンコーディングが採用されている。

## 隠し機能

ARIB STD-B24の定めには、BMLブラウザのバージョンを判定する方法は定義されていない。しかしながら、受信機の世代によって対応するSTD-B24の版が異なり、実装に差異が存在する。またメーカーによってBMLブラウザやECMAScriptエンジンのミドルウエア製造元が異なり、たとえば[ソニー](../Page/ソニー.md "wikilink")と[松下ではかなり大きな実装の差が見受けられる](https://ja.wikipedia.org/wiki/パナソニック "wikilink")。そこで受信機メーカーはARIBに無断でBMLブラウザの製造元とバージョンを判別する方法を定義した。それは受信機メモリの残り容量を返す関数が実装上無意味\[1\]なのを利用して、残り容量を取得する関数を呼び出すと、受信機メーカー・受信機の製造日・BMLブラウザのバージョン・ECMAScriptエンジンのバージョンを示す[マジックナンバーが返されるようにした](https://ja.wikipedia.org/wiki/マジックナンバー_\(メッセージ\) "wikilink")。BMLコンテンツはこのマジックナンバーを判別することにより、受信機によって異なる振る舞いを回避し、すべての受信機で同じように振舞うコンテンツの製作を可能にしている。しかしながらこの実装はARIBの標準化委員会の意向を無視し、受信機メーカー側が勝手に結託してデファクトスタンダードを作った事から、標準化委員会の間ではこれを問題視する委員もいる。

## 脚注

## 関連項目

  - [MPEG](../Page/Moving_Picture_Experts_Group.md "wikilink")
  - [BCML](../Page/BCML.md "wikilink")

## 外部リンク

  - [1セグ放送用BMLブラウザーの機能と構成（株式会社インプレスR\&D）](http://i.impressrd.jp/files/images/bn/pdf/im200509-070-1seg.pdf)

<!-- end list -->

  - [ARIB 技術資料（放送分野）一覧表](http://www.arib.or.jp/tyosakenkyu/kikaku_hoso/hoso_gijutsu_number.html)
  - [ARIB STD-B24 の改定履歴](http://www.arib.or.jp/tyosakenkyu/kikaku_hoso/hoso_std-b024.html)
  - [ARIB STD-B24 5.5版(第一分冊)](http://www.arib.or.jp/english/html/overview/doc/2-STD-B24v5_5-1p3.pdf)
  - [ARIB STD-B24 5.5版(第二分冊)(1/2)](http://www.arib.or.jp/english/html/overview/doc/2-STD-B24v5_5-2p3-1.pdf)
  - [ARIB STD-B24 5.5版(第二分冊)(2/2)](http://www.arib.or.jp/english/html/overview/doc/2-STD-B24v5_5-2p3-2.pdf)
  - [ARIB STD-B24 5.5版(第三分冊)](http://www.arib.or.jp/english/html/overview/doc/2-STD-B24v5_5-3p3.pdf)

<!-- end list -->

  - [ARIB TR-B14の改定履歴](http://www.arib.or.jp/tyosakenkyu/kikaku_hoso/hoso_tr-b014.html)
  - [ARIB TR-B14 4.8版(第一分冊)(1/2)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B14v4_8-1p3-1.pdf)
  - [ARIB TR-B14 4.8版(第一分冊)(2/2)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B14v4_8-1p3-2.pdf)
  - [ARIB TR-B14 4.8版(第二分冊)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B14v4_8-2p3.pdf)
  - [ARIB TR-B14 4.8版(第三分冊)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B14v4_8-3p3.pdf)

<!-- end list -->

  - [ARIB TR-B15 の改定履歴](http://www.arib.or.jp/tyosakenkyu/kikaku_hoso/hoso_tr-b015.html)
  - [ARIB TR-B15 5.6版(第一分冊)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B15v5_6-1p4.pdf)
  - [ARIB TR-B15 5.6版(第二分冊)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B15v5_6-2p4.pdf)
  - [ARIB TR-B15 5.6版(第三分冊)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B15v5_6-3p4.pdf)
  - [ARIB TR-B15 5.6版(第四分冊)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B15v5_6-4p4.pdf)

<!-- end list -->

  - [ARIB TR-B27 の改定履歴](http://www.arib.or.jp/tyosakenkyu/kikaku_hoso/hoso_tr-b027.html)
  - [ARIB TR-B27 1.0版(第一分冊)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B27v1_0-1p3.pdf)
  - [ARIB TR-B27 1.0版(第二分冊)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B27v1_0-2p3.pdf)
  - [ARIB TR-B27 1.0版(第三分冊)](http://www.arib.or.jp/english/html/overview/doc/4-TR-B27v1_0-3p3.pdf)

[Category:データ放送](https://ja.wikipedia.org/wiki/Category:データ放送 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")

1.  再生可能なBMLコンテンツのサイズはARIB TR-B14/B15によって明確に規定されている為、参照する必要が無い。またBMLコンテンツがメモリ上でどのように処理されるかは何れの規格でも定義していないので、残メモリの量が判ったとしても、コンテンツ側では対処する方法が無いからである。