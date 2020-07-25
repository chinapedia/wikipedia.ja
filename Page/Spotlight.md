> この記事は[Spotlight](https://ja.wikipedia.org/wiki/Spotlight)から翻訳されています。


**Spotlight**（**スポットライト**）とは、[Mac OS X v10.4 Tigerから搭載された](../Page/Mac_OS_X_v10.4.md "wikilink")[SQLite](../Page/SQLite.md "wikilink")をベースとしたデスクトップ検索機能、およびその基盤技術のことである。検索フィールドに欲しい情報のキーワードを入力するだけで関連する全ての対象を検索できる。[2004年](../Page/2004年.md "wikilink")の[WWDCで同OSと同時に発表され](../Page/Worldwide_Developers_Conference.md "wikilink")、その高速性が大いにアピールされた。

## 特徴

Mac OS X v10.4の[ファイルシステム](../Page/ファイルシステム.md "wikilink")は[HFS Plusをベースに](../Page/HFS_Plus.md "wikilink")、ファイルの内容から抽出した[メタデータ](../Page/メタデータ.md "wikilink")を同時に格納するよう拡張されている。この情報は事前にインデックス化されており、日付や著者名、メールアドレス、内容などの[属性](../Page/属性.md "wikilink")ごとに対応する値を保持するものである。そして対象属性とキーワードからなるクエリーを発行することで、指定した範囲から一致する情報をランク付けして引き出せる。この時情報は発見され次第リアルタイムで通知され、必要なら順次結果を更新することができる。

デスクトップ上部のメニューバーに常設されている全体検索では、種類指定や日付指定のような特殊な指定を事前に解析することで自然な検索を行うようになっている。ファイルを開いたり保存する際のダイアログにも検索フィールドがついており、フォルダを探し出すのに役に立つ。対応アプリケーションではウィンドウに検索フィールドが設けられており、アプリケーション内部のデータベースを検索することができる。たとえば、[iCal](https://ja.wikipedia.org/wiki/iCal "wikilink")でスケジュールをチェックしたり、[iPhoto](https://ja.wikipedia.org/wiki/iPhoto "wikilink")で写真を探したり、[Safari](../Page/Safari.md "wikilink")で[ブックマーク](../Page/ブックマーク.md "wikilink")や履歴を見つけたりできる。なおメタデータは検索対照だけでなくプレビューにも利用される。

他にも意図する機能を入力することによって環境設定の項目を探したり、アプリケーションの[ランチャー](../Page/ランチャー.md "wikilink")として利用できるなど、単純にファイルの検索にとどまらない応用が可能である。

[Mac OS X v10.5から](../Page/Mac_OS_X_v10.5.md "wikilink")、ネットワーク上の共有フォルダの検索にも対応（下記参照）、最近閲覧したWebページの検索もできるようになっている。初期の Spotlightでは日本語[形態素解析](../Page/形態素解析.md "wikilink")が不十分だったため、Googleで使われていた[MeCab](../Page/MeCab.md "wikilink")を採用した（/usr/lib/、/usr/include/mecab.h 等参照）。

## その他

事前に検索対象をインデックス化する構造のため、旧バージョンからアップデートした場合は初期インデックスの構築に数時間を要する場合がある。またメタデータの格納用に100MBから数GBほどのディスク容量を必要とする。

同ファイルシステムの実装には[BeOS](../Page/BeOS.md "wikilink")のファイルシステム[BFSを製作した](https://ja.wikipedia.org/wiki/Be_File_System "wikilink")[ドミニク・ジャンパオロ](https://ja.wikipedia.org/wiki/ドミニク・ジャンパオロ "wikilink")が関わっている。

Spotlightは高速さを売りにしており、Tigerが動作する下限クラスのMacであっても20-30秒もあれば全体の検索が終了する。[Power Mac G5以上の高速なマシンでは入力が終わる前に検索が終了していることもある](https://ja.wikipedia.org/wiki/Power_Mac#Power_Mac_G5 "wikilink")。

Mac OS X v10.5では、ネットワーク上の共有フォルダの検索にも対応したとされるが、10.5.6よりNAS（ネットワークハードディスク）の検索の際には、ターミナルを起動しての設定が必要（ファイルの更新には再検索が必要）。また、HFS+に依存しているため、SMBで接続されたボリュームの検索が不十分である。[Mac OS X v10.6からは](../Page/Mac_OS_X_v10.6.md "wikilink")、NTFSへの書き込みが可能となったが、SpotlightでNTFSボリューム上を検索すると、かなりの確率でシステムトラブルが発生する　[1](http://builder.japan.zdnet.com/sp/snow-leopard-09/story/0,3800100196,20404547,00.htm)（Snow Leopardの「NTFSへの書き込み」に関する後日談-Spotlightとの相性に問題） 。

## 関連項目

  - [Sherlock](../Page/Sherlock_\(ソフトウェア\).md "wikilink")

## 外部リンク

  - [アップル - Mac ハンドブック：Spotlight](http://support.apple.com/kb/HT2531?viewlocale=ja_JP)

[Category:検索エンジン](https://ja.wikipedia.org/wiki/Category:検索エンジン "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:iOS_(アップル)](https://ja.wikipedia.org/wiki/Category:iOS_\(アップル\) "wikilink") [Category:2005年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2005年のソフトウェア "wikilink")