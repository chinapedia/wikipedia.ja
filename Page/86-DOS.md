> この記事は[86-DOS](https://ja.wikipedia.org/wiki/86-DOS)から翻訳されています。


**86-DOS**は16bitのディスク[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。元々は[シアトル・コンピュータ・プロダクツ](https://ja.wikipedia.org/wiki/シアトル・コンピュータ・プロダクツ "wikilink")（Seattle Computer Products : SCP)から販売された[Intel 8086ベースのコンピュータ](../Page/Intel_8086.md "wikilink")・キット用として[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")に[ティム・パターソン](https://ja.wikipedia.org/wiki/ティム・パターソン "wikilink")が4ヶ月で開発した。最初の**[PC DOS](https://ja.wikipedia.org/wiki/IBM_PC_DOS "wikilink")**（**[MS-DOS](../Page/MS-DOS.md "wikilink")**）は、86-DOSをベースに作られた。86-DOSやMS-DOSのコマンド構造と[APIは](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[デジタルリサーチ](../Page/デジタルリサーチ.md "wikilink")社の[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")に似ており、簡単にプログラムを[移植することができた](../Page/移植_\(ソフトウェア\).md "wikilink")。

86-DOSは発売前はQDOS(Quick and Dirty Operating System、即席オペレーティングシステム)と呼ばれた。[シンクレア・リサーチ](https://ja.wikipedia.org/wiki/シンクレア・リサーチ "wikilink")社の[Sinclair QLコンピュータ用OSであるQDOSとは無関係](https://ja.wikipedia.org/wiki/Sinclair_QL "wikilink")。

## 起源

SCPは[1976年](../Page/1976年.md "wikilink")6月に8086コンピュータ・キットのデモを行い、11月から出荷したが、オペレーティングシステムがなく販売に苦戦しており、86-DOSの前身となるQDOSを開発した。ボードと一緒にSCPが提供したソフトウェアは、スタンド・アロンの[Microsoft BASIC](../Page/Microsoft_BASIC.md "wikilink")-86だけだった。マイクロソフトは新しいプロセッサ上でソフトを動かすことに非常に熱心で、開発用としてSCPから8086ボードのプレ・リリース版を借りており、6月のデモに参加した。

当時のマイクロコンピュータ用の主要なオペレーティングシステムはデジタルリサーチのCP/Mだったが、1980年の時点では16bit版は存在していなかった。SCPは開発用ボードをデジタルリサーチに提供しておらず、デジタルリサーチが興味を持たなかったのか、CP/Mの16bit版をデジタルリサーチが開発することは無いだろうとSCPが考えたのかは明らかではない。当時動作するプロトタイプはSCPの社内にも2台しかなかった。利用可能なオペレーティングシステムが無いまま、パターソンは1980年4月にQDOSの開発を始めた。

パターソンの設計したQDOSは、内部のAPIがCP/Mと同じで、ユーザコマンドも大部分が同じであった。MS-DOSと同様に、QDOSはCP/Mの「遺物的なコマンド」をいくつか切り捨てていた。DECミニコンピュータで使われていたコマンドに似ている[PIPファイル](../Page/Peripheral_Interchange_Program.md "wikilink")・コピー・サブシステムは、COPYコマンドに置き換えられた。PIPに続けて「コピー先=コピー元」とタイプして実行するのではなく、「COPY コピー元 コピー先」の形に単純化され、PDP-11オペレーティングシステムの流れを汲むVAX/VMSのCOPYコマンドと同様になった。またCP/Mはフロッピーディスクを入れ替える時にコントロールキーを打たなければならず評判が悪かった。その後のDOSやWindowsは、UnixとGUIオペレーティング・システム・シェルに似た機能とユーザ・インターフェースを採用していった。

QDOSが**86-DOS**の名前で販売されたとき、CP/Mの特徴の多くが取り入れられなかった。パターソンはCP/Mのファイルシステムをそのままコピーせず、[Microsoft BASICのいくつかのバージョンで採用された](../Page/Microsoft_BASIC.md "wikilink")[FAT ファイルシステムを使った](../Page/File_Allocation_Table.md "wikilink")。

## IBM の関心

1980年後半、[IBM](../Page/IBM.md "wikilink")は[IBM PCのプロトタイプを開発していた](../Page/IBM_PC.md "wikilink")。その当時最も普及していたオペレーティングシステムはCP/Mであり、IBMは競争のためにはCP/Mが必要だと考えていた。最終的にIBMはCP/Mではなく86-DOSを採用した。その理由には諸説ある。

CP/Mの開発者であり、後に[DR-DOS](../Page/DR-DOS.md "wikilink")も開発するデジタルリサーチ社の[ゲイリー・キルドール](../Page/ゲイリー・キルドール.md "wikilink")は、IBMの職員と会うことを避けていたと言われている。またキルドールがデジタルリサーチ社を訪問したIBMの重役たちを何時間も待たせて自家用飛行機を飛ばしていたという[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")の話が有名である。IBMは[マイクロソフト](../Page/マイクロソフト.md "wikilink")からオペレーティングシステムの提供を受けることになり、キルドールは世紀のチャンスを逃した。ただしいずれの話も真実かどうかははっきりしていない。

パターソンらによるとキルドールは商談には関与せず、弁護士でもある妻のDorothy McEwenに任せていた。パターソンは「彼女がIBMとの[秘密保持契約](https://ja.wikipedia.org/wiki/秘密保持契約 "wikilink")（NDA）へのサインを嫌がった」と語っている。また後にキルドールが[NHKスペシャル](../Page/NHKスペシャル.md "wikilink")『[新・電子立国](../Page/新・電子立国.md "wikilink")』のインタビューで語ったところによれば、IBMの重役が最初にデジタルリサーチを訪れた時、キルドールは既にサンノゼで別の商談の予定が入っていたため、妻に代わりに対応してもらった際にNDA締結を巡るトラブルがあったという\[1\]。ただしキルドールの同僚である[ゴードン・ユーバンクス](https://ja.wikipedia.org/wiki/ゴードン・ユーバンクス "wikilink")は「彼女はサインした」と言っている。ユーバンクスは「キルドールは[PL/1](https://ja.wikipedia.org/wiki/PL/1 "wikilink")コンパイラに取り組んでいたので、当時はCP/Mの16bitプロセッサへの移植には興味が無かった」とも言っている。

他の説では、IBMとデジタル社が価格面で折り合わなかったのだ、とされている。IBMは250,000ドルでCP/Mを丸ごとすべて買い取ることを提案したが、キルドールの希望は1コピーあたり10ドルのライセンスであった。\[2\]

少なくとも、IBMとデジタルリサーチの間で具体的にCP/Mの供給を巡り複数回の交渉が行われたことや、IBMから25万ドルでCP/Mを買い取りたいという提案があったことはキルドール自身が認めており\[3\]、NDAを巡るトラブルが当初あったにせよ、その後両社の間でNDAが結ばれ具体的な価格交渉が行われたことは間違いないと思われる。ただしこの交渉に関してIBM側の関係者とキルドールの証言が大きく食い違っているのも事実で（NHKのインタビューに対し、IBM側の交渉担当者だった[ジャック・サムズ](https://ja.wikipedia.org/wiki/ジャック・サムズ "wikilink")は「キルドールとは一度も会っていない」と語っているのに対し、キルドールは「サムズとは複数回会って交渉した」と語っている\[4\]）、真相は依然謎に包まれている。

結果的にIBMはマイクロソフトにオペレーティングシステムの提供を依頼し、マイクロソフトもまたそれを受諾した（マイクロソフトは既にPC用の[ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")[BASIC](../Page/BASIC.md "wikilink")インタプリタも提供していた）。

## PC DOS の誕生

1980年12月にマイクロソフトは、シアトル・コンピュータ・プロダクツ社(SCP)から86-DOSの非独占的なライセンスを25,000ドルで買い取った。1981年5月にはティム・パターソンを引き抜いて、86-DOSの[IBM PC](../Page/IBM_PC.md "wikilink")（安いが遅い [8088と](../Page/Intel_8088.md "wikilink")、それ用の周辺チップを使用）への移植を行なわせた。IBMは連日開発に付き合い、受領の前に300以上の[バグ](../Page/バグ.md "wikilink")を報告し、ユーザ・マニュアルも作成した。

PCをリリースする1ヶ月前の[1981年](../Page/1981年.md "wikilink")7月に、マイクロソフトはSCPから86-DOSの全ての権利を50,000ドルで買い取った。それはIBMの主な要求を満たしていた。見た目がCP/Mに似ており、86-DOSのTRANSコマンドを使って8080のソースファイルを8086の機械語に変換できるおかげで既存の8bit CP/Mプログラムを簡単に移植できた。マイクロソフトは86-DOSをIBMにライセンスし、[PC DOS](https://ja.wikipedia.org/wiki/IBM_PC_DOS "wikilink") 1.0となった。このライセンスでは、マイクロソフトが他の会社にDOSを売ることも認められており、実際に販売が行なわれた。取引は大成功を収めたのだが、後にSCPはマイクロソフトを訴える。マイクロソフトはIBMと秘密保持契約(NDA)を結んでおり、IBMとの関係を公にすることは契約に反していたが、SCPはマイクロソフトがオペレーティングシステムを安く買い取るためにIBMとの関係を秘密にしたと主張した。最終的には100万ドルで和解した。

## 知的財産論争

IBMはDOSを60ドルで販売し、その価格設定は240ドルのCP/M-86よりも遥かに魅力的だった。デジタルリサーチ社は、CP/Mの[システムコール](../Page/システムコール.md "wikilink")、プログラム構造、[ユーザーインターフェイス](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")のほぼすべてをDOSに模倣されていたためマイクロソフトを訴えることを考えたが、結局は取りやめた。マイクロソフトを訴えればIBMも訴えなければならなくなり、IBMのような巨大な企業を相手に裁判で戦えるほどの資金は無く、勝てる見込みが無いと考えられた。

[1982年](../Page/1982年.md "wikilink")までにIBMが[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")に準拠したDOSのバージョンをリリースするようマイクロソフトに依頼した時には、PC DOS 2.0はDOSをほとんど書き直していた。[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")3月までには、86-DOS由来のソースコードはほんの一部が残っているだけになっていた。86-DOS由来のソフトウェアで最も長く生き残った部分は、原始的なライン・エディタの[EDLIN](https://ja.wikipedia.org/wiki/EDLIN "wikilink")である。[QBasic](https://ja.wikipedia.org/wiki/QBasic "wikilink")を元とするグラフィカルなエディタ（EDITとして知られている）を同梱した[MS-DOS](../Page/MS-DOS.md "wikilink") 5.0が[1991年](../Page/1991年.md "wikilink")6月にリリースされるまで、EDLINはマイクロソフト版のDOSで提供されていた唯一のエディタであった。

## 86-DOS のバージョン

  - QDOS v0.1 1980年8月
  - 86-DOS v0.3 1980年12月
  - 86-DOS v1.0 1981年4月
  - PC DOS v1.0 1981年8月
  - PC DOS v1.10 1982年6月
  - MS-DOS v1.24 1982年6月
  - MS-DOS v1.25 1982年7月

## 出典

<references/>

## 関連項目

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")
  - [CP/M-86](https://ja.wikipedia.org/wiki/CP/M-86 "wikilink")

## 外部リンク

  - [Tim Paterson's brief history](http://www.patersontech.com/dos/byte%E2%80%93history.aspx) of QDOS/86-DOS

[Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink") [Category:1980年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1980年のソフトウェア "wikilink") [Category:プロプライエタリOS](https://ja.wikipedia.org/wiki/Category:プロプライエタリOS "wikilink")

1.  [NHKスペシャル](../Page/NHKスペシャル.md "wikilink")『[新・電子立国](../Page/新・電子立国.md "wikilink")』第1巻「ソフトウェア帝国の誕生」（[相田洋](../Page/相田洋.md "wikilink")著、[日本放送出版協会](https://ja.wikipedia.org/wiki/日本放送出版協会 "wikilink")、[1996年](../Page/1996年.md "wikilink")）pp.276 - 281
2.
3.
4.