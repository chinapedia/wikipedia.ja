> この記事は[SCMS](https://ja.wikipedia.org/wiki/SCMS)から翻訳されています。


**SCMS**（Serial Copy Management System、シリアルコピーマネジメントシステム）は、民生用の[DAT](../Page/DAT.md "wikilink")や[Mini Disc](../Page/ミニディスク.md "wikilink")、[DCC](../Page/デジタルコンパクトカセット.md "wikilink")、[CDレコーダー](https://ja.wikipedia.org/wiki/CDレコーダー "wikilink")などの[デジタル](../Page/デジタル.md "wikilink")[録音機器に付加されている](../Page/録音再生機器.md "wikilink")[コピー防止技術](https://ja.wikipedia.org/wiki/コピーガード#音楽メディアなどに使用されているもの "wikilink")。

## 概要

SCMS対応機器間では、デジタル接続による[コピー](../Page/コピー.md "wikilink")は1世代のみ可能。2世代目からは、録音側機器が[デジタル信号](../Page/デジタル信号.md "wikilink")に含まれるコピー情報を検出して、録音を行わないようにする。ただしアナログ接続によるコピーは無制限で行える。なお、音楽[コンテンツ](../Page/コンテンツ.md "wikilink")の制作やその[メディアの](../Page/電子媒体.md "wikilink")[バックアップ](../Page/バックアップ.md "wikilink")を主な用途としている[業務用](../Page/業務用.md "wikilink")のデジタル録音再生機器では、SCMSの制限を解除できるものもある。 また、[コピーコントロールCD](../Page/コピーコントロールCD.md "wikilink")の一部（主に[EU](https://ja.wikipedia.org/wiki/EU "wikilink")製のもの）には、1世代目のコピーも許可しないものがある。

## SCMS-T（派生規格）

[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")（[KDDI](../Page/KDDI.md "wikilink")・[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")[連合](https://ja.wikipedia.org/wiki/連合 "wikilink")）向けの[W44T W44T II、LEXUS W44T III](../Page/W44T.md "wikilink")、TiMO、[W52T](../Page/W52T.md "wikilink")、[W54T](../Page/W54T.md "wikilink")、[W56T](../Page/W56T.md "wikilink")、[W54SA](../Page/W54SA.md "wikilink")、[W54S](../Page/W54S.md "wikilink")、[W63CA](https://ja.wikipedia.org/wiki/W63CA "wikilink")や、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")向けの[P902iS](../Page/P902iS.md "wikilink")などの[Bluetooth](../Page/Bluetooth.md "wikilink")対応[携帯電話](../Page/携帯電話.md "wikilink")で、付属のワイヤレスレシーバなどに音楽を転送する際に利用されている。 前述のau向け各機種や、[ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")向けの[910T](../Page/SoftBank_910T.md "wikilink")、[911T](https://ja.wikipedia.org/wiki/SoftBank_911T "wikilink")、[912SH](../Page/SoftBank_912SH.md "wikilink")、ドコモの[P903iTV](../Page/P903iTV.md "wikilink")、[P905i](../Page/P905i.md "wikilink")、[P905iTV](../Page/P905iTV.md "wikilink")（[ワンセグ](../Page/ワンセグ.md "wikilink")の音声を転送する際）の場合は、派生規格の**SCMS-T**という仕組みが使われている。

一部の[Android搭載](../Page/Android_\(オペレーティングシステム\).md "wikilink")[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")用を含むauのLISMO PlayerでBluetoothレシーバー、およびBluetoothヘッドフォンを使用するにはSCMS-T規格に対応したレシーバー、およびヘッドフォンを購入しなければならない。ただ、これらの情報は取扱説明書に小さく記述されているだけなので、知らない利用者も決して少なくない。

## 仕組

各トラックの最後に、[コピービット](https://ja.wikipedia.org/wiki/コピービット "wikilink")という2桁の管理情報が記録されているだけである。ID6コードとも呼ばれる。

ソニーのDATデッキのDTC-55ES、DTC-77ESなど、SCMS搭載以降の一部機種においては、隠しコマンドでID6コードを表示させて、現在走行しているテープがコピー可能な物なのかどうか調べられるようになっている。

コピービットについて

00=無制限コピー可能

01=未定義(基本的に「一回だけ録音可」で処理)

10=コピー不可能

11=一回だけコピー可能　SCMSを制定する以前は、ここも未定義とされていた。

このコピービットを書き換えてコピー永久可能にするような装置を売り買いすると、[1999年](../Page/1999年.md "wikilink")以降は[著作権法](../Page/著作権法.md "wikilink")・[不正競争防止法](../Page/不正競争防止法.md "wikilink")改正により、違法になる。ただし、自分たちで作詞、作曲、演奏などを手がけた音楽作品など、SCMSを解除する者がそのコンテンツの[著作権](../Page/著作権.md "wikilink")を有している場合は、この限りではない。業務用のデジタル録音再生機器にSCMSの制限を解除できる機能が搭載されているのは、このためである。

かつては、[秋月電子や](../Page/秋月電子通商.md "wikilink")[共立電子](https://ja.wikipedia.org/wiki/共立電子 "wikilink")などの[電子工作](../Page/電子工作.md "wikilink")専門店からSCMS解除装置作成キットが売られていた時期があり、音楽制作などで安価な民生用のデジタルオーディオ機器を活用する個人やアマチュアの音楽グループなどがコンテンツのバックアップを主な目的としてSCMS解除装置作成キットなどを購入する事があったが、1999年の[不正競争防止法](../Page/不正競争防止法.md "wikilink")の改正に伴い、SCMS解除装置作成キットの[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")国内での[販売](../Page/販売.md "wikilink")が禁止されたため、[趣味](https://ja.wikipedia.org/wiki/趣味 "wikilink")などで音楽制作を行なう個人やアマチュアの音楽グループなどは、コンテンツのバックアップには、民生用に比べ高額な業務用デジタル録音再生機器を導入せざるを得なくなった。なお、秋月電子や共立電子から回路図を入手したとしても、部品が入手困難である上に、プログラムが開示されていないため、再現は不可能に近い。

MDでコピービットが異なるトラックを結合した場合、自動的にコピービットがコピー制限の大きいのものに合わせられる。たとえば、「一回だけコピー可能（11）」のトラックと「コピー不可能（10）」のトラックを結合すると、結合後のトラックは「コピー不可能（10）」のトラックとして処理される。尚、コピービットが異なるトラックを結合できない機種も存在する。

また、SCMS搭載DATデッキでアナログ録音したDATテープも、ID6コードは「11」なので、1回限りしかデジタルコピーが出来ないが、このようなテープをSCMS導入前（ID6=「11］が未定義とされていた）の懇談会仕様のソニー製DATデッキで再生すると、ID6コードは「00」として扱われて、デジタル出力される。録音側のデッキでデジタル録音しても、コピーした側のテープもID6=「00」なので、それ以降のデジタルコピーが無制限に行えるようになった。しかし、再生側がSCMS導入後の製品で、録音側が懇談会仕様のDATデッキの組み合わせだと、懇談会仕様のDATデッキのデジタル入力については、ID6=「00」以外のデジタル録音は認められないため、デジタル録音は出来ない。たとえID6=「11」（1回のみ録音可能）であっても録音できない。必ず送り出しを懇談会仕様のDATデッキで行う必要があった。

## 関連項目

  - [コピーガード](../Page/コピーガード.md "wikilink")

[Category:著作権管理技術](https://ja.wikipedia.org/wiki/Category:著作権管理技術 "wikilink")