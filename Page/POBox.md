> この記事は[POBox](https://ja.wikipedia.org/wiki/POBox)から翻訳されています。


**POBox**(「ピーオーボックス」あるいは「ポボックス」、*Predictive Operation Based On eXample*)は、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")の[研究者](https://ja.wikipedia.org/wiki/研究者 "wikilink")で、元[ソニー](../Page/ソニー.md "wikilink")コンピュータサイエンス研究所研究員の[増井俊之](../Page/増井俊之.md "wikilink")が考案・開発した、文章入力補助機能の[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。

[携帯電話](../Page/携帯電話.md "wikilink")や[PDAその他モバイル端末向けの](../Page/携帯情報端末.md "wikilink")[予測変換機能としては先駆け的存在だった](https://ja.wikipedia.org/wiki/入力予測 "wikilink")\[1\]。

## 特徴

POBoxは「予測/例示インタフェース」を採用し、ユーザからの入力に対して次のように処理を行う。

  - 変換辞書に登録されている単語について、入力文字の組み合わせから予測して候補を表示する。
  - 過去の入力内容、単語の使用頻度に基づいて、入力単語を予測して候補を表示する。

使い込むほどにユーザの癖を[学習](../Page/学習.md "wikilink")し、極端な場合、1文字入力とカーソル操作で希望する文章の入力が完了する。PDAや携帯電話といった、入力デバイス（[キーボード](../Page/キーボード_\(コンピュータ\).md "wikilink")）空間が制約される環境で真価を発揮する。

## 対応プラットフォーム

### パーソナルコンピュータ・携帯情報端末

  - [Palm OS](https://ja.wikipedia.org/wiki/Palm_OS "wikilink")
  - [Newton OS](https://ja.wikipedia.org/wiki/Newton_OS "wikilink")
  - [Windows 98](../Page/Microsoft_Windows_98.md "wikilink") / [Me](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink") / [2000](../Page/Microsoft_Windows_2000.md "wikilink") / [XP](../Page/Microsoft_Windows_XP.md "wikilink") / [CE](../Page/Microsoft_Windows_Embedded_CE.md "wikilink")
  - [Emacs](../Page/Emacs.md "wikilink")
  - ソニー InfoCarry

### 携帯電話

POBox自体は既述の通り予測変換エンジンだが、[Wnn](../Page/Wnn.md "wikilink")シリーズ([オムロン](../Page/オムロン.md "wikilink"))との組み合わせで[ソニー](../Page/ソニー.md "wikilink")、[ソニーモバイルコミュニケーションズ](../Page/ソニーモバイルコミュニケーションズ.md "wikilink")(旧ソニー・エリクソン・モバイルコミュニケーションズ)製の日本国内向け携帯電話端末に標準で採用され、実質的に[日本語入力システム](../Page/日本語入力システム.md "wikilink")の一種として扱われることもある。ただし初期はWnnの辞書のみを採用し、その後に基幹部分も含め採用された。バージョンもミニWnn、モバイルWnn、AdvancedWnnなどを経てW64Sを含む2009年以降の機種にはiWnnとの組み合わせで搭載されている。カタログなどにもPOBoxの搭載が強調されて掲載される場合もある。

#### POBox・POBox Pro

[フィーチャーフォンでは](https://ja.wikipedia.org/wiki/フィーチャー・フォン "wikilink")[au向けに](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")[C406S](https://ja.wikipedia.org/wiki/C406S "wikilink")で初搭載され、以後[ドコモ向けのソニー](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")、ソニー・エリクソン、ソニーモバイル製日本国内向け端末に搭載、後に上位版の"POBox Pro"となった。一部機種を除きソニーモバイルの公式PCサイトより自作のダウンロード辞書作成も可能だった。

一時期は[ジョグダイヤル](../Page/ジョグダイヤル.md "wikilink")との組み合わせで「スピードメーラー」などの呼称で搭載されていたが、携帯電話のプラットフォームやユーザインタフェイス共通化のため([KCP](../Page/KCP.md "wikilink")および[KCP+](../Page/KCP+.md "wikilink")を参照のこと)ジョグダイヤルは搭載されることはなくなった。

POBoxでは予測精度の向上を目的としてデフォルトの辞書の登録語数は[ATOK](../Page/ATOK.md "wikilink")(予測変換システムのAPOTを含む)などと比較すると絞り込まれており、ユーザーが目的に応じてダウンロード辞書を活用することを前提としている\[2\]。またATOKでは最初の文字に濁点や半濁点が含まれる候補はこれらを入力するまで表示されないのに対し、POBoxでは表示される\[3\]。

  - POBox
    以下のようなマイナーバージョンアップが行われたが、名称自体にバージョン名などは付加されなかった。
      -
        [SO504i](https://ja.wikipedia.org/wiki/SO504i "wikilink")以降 - 逆トグル（文字の出現順を逆送りする機能）への対応\[4\]。
        [SO212i](https://ja.wikipedia.org/wiki/SO212i "wikilink")以降 - 大文字・小文字の切り替え機能の追加、ダウンロード辞書への対応\[5\]。
        [SO506iS](https://ja.wikipedia.org/wiki/SO506iS "wikilink")・[W21S](../Page/W21S.md "wikilink")以降 - モードレス（ひらがな入力時に英数字やカタカナをそのまま変換できる）への対応、単漢字候補が埋もれやすい欠点への対策など入力環境の改善\[6\]。
  - POBox Pro
    搭載機種：[SO705i](../Page/SO705i.md "wikilink") / [W43S](../Page/W43S.md "wikilink") / [W44S](../Page/W44S.md "wikilink") / [W51S](../Page/W51S.md "wikilink") / [ウォークマンケータイ W52S](../Page/W52S.md "wikilink") / [W53S](../Page/W53S.md "wikilink")
    予測変換ウィンドウにおけるタブの採用など使い勝手が向上した。さらに入力詳細設定で文字入力時の細かい設定ができるようになった。
  - POBox Pro 2.0
    搭載機種：[SO905i](../Page/SO905i.md "wikilink") / [Cyber-shotケータイ SO905iCS](../Page/SO905iCS.md "wikilink") / [W54S](../Page/W54S.md "wikilink") / [Cyber-shotケータイ W61S](../Page/W61S.md "wikilink")
    POBox Proより学習機能・予測機能を強化。新たに文字入力後に接続語を予測する「つながり候補」機能が追加された。[2タッチ入力](../Page/2タッチ入力.md "wikilink")（ポケベル打ち）にも対応した。
  - POBox Pro E
    搭載機種：[W62S](../Page/W62S.md "wikilink")
    POBox Pro 2.0をベースに、英語の予測変換に対応している。
  - POBox Pro 3.0
    搭載機種：[SO906i](https://ja.wikipedia.org/wiki/SO906i "wikilink") / [フルチェンケータイ re](../Page/フルチェンケータイ_re.md "wikilink")(W63S) / [Walkman Phone, Xmini](https://ja.wikipedia.org/wiki/Xmini "wikilink")(W65S)
    POBox Pro 2.0からさらに学習機能・予測機能が進化している。新機能として\[7\]複合語入力に対応した「つなげて学習」、話し言葉を学習、候補に表示する「しゃべり語学習」が追加されている。キーを押し続けることで同じ文字を連続入力できる「つづけて入力」（通称「[ジョジョ打ち](../Page/ジョジョの奇妙な冒険.md "wikilink")」\[8\]\[9\]）、デコレーションメールの色付き文字を学習する「カラフルPOBox」を搭載している。
  - POBox Pro 3.0E
    搭載機種：[W64S](https://ja.wikipedia.org/wiki/W64S "wikilink") / [Cyber-shotケータイ S001](https://ja.wikipedia.org/wiki/S001 "wikilink") / [Walkman Phone, Premier3](https://ja.wikipedia.org/wiki/Premier3 "wikilink") / [G9](https://ja.wikipedia.org/wiki/G9 "wikilink") / [S002](https://ja.wikipedia.org/wiki/S002 "wikilink") / [BRAVIA Phone U1](https://ja.wikipedia.org/wiki/U1_\(携帯電話\) "wikilink") / [URBANO BARONE](https://ja.wikipedia.org/wiki/URBANO_BARONE "wikilink")
    POBox Pro 3.0をベースに、英語の予測変換に対応している。
  - POBox Pro 4.0E
    搭載機種：[Cyber-shotケータイ S003](https://ja.wikipedia.org/wiki/S003 "wikilink") / [BRAVIA Phone S004](https://ja.wikipedia.org/wiki/S004 "wikilink") / [BRAVIA Phone S005](https://ja.wikipedia.org/wiki/S005 "wikilink") / [URBANO MOND](https://ja.wikipedia.org/wiki/URBANO_MOND "wikilink")
    変換候補でデコレーション絵文字（絵文字風のイラスト画像）を表示するほか、「ありがとう」「うれしい」「かなしい」など感情を示す言葉を変換する際には、その感情に合わせた文字色の変換候補を表示するようになった\[10\]。
  - POBox Pro 5.0E
    搭載機種：[Cyber-shotケータイ S006](https://ja.wikipedia.org/wiki/S006 "wikilink") / [G11](https://ja.wikipedia.org/wiki/G11 "wikilink")
    単語の読みの長さにより変換候補を絞り込む「ワイルドカード予測」(iWnn由来)が追加され、カラフルPOBoxにおいても英語予測に対応した\[11\]。
  - POBox Pro 6.0E
    搭載機種：[S007](https://ja.wikipedia.org/wiki/S007 "wikilink") / [URBANO AFFARE](https://ja.wikipedia.org/wiki/URBANO_AFFARE "wikilink")
    過去の入力履歴を参照して文字入力をする前に予測候補を出す「いきなり予測」(iWnn由来)が追加された\[12\]。

### POBox Touch

[Android](../Page/Android.md "wikilink")搭載[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")・[タブレット向けバージョンで](../Page/タブレット_\(コンピュータ\).md "wikilink")、ソフトウェアキーを用いたタッチパネルでの日本語や記号入力に最適化した、ダイナミック表示を行うQWERTYキーなどのUIが特徴となっている。自作ダウンロード辞書には対応していない。主に[ソニーモバイル](../Page/ソニーモバイルコミュニケーションズ.md "wikilink")(旧ソニー・エリクソン)製スマートフォン・タブレット端末、ソニー製タブレット端末に搭載される。

2.x以降の主な変更点は次の通りとなっている。

  - 2.0 - フリック入力やQWERTYキーなどのカスタマイズ機能の追加。
  - 3.x - [Simeji](https://ja.wikipedia.org/wiki/Simeji "wikilink")互換の[プラグイン](../Page/プラグイン.md "wikilink")による外部アプリとの連携機能や英語予測変換に対応。公式サイトにおいてプラグインとして紹介されているものにはユニークなものも存在する。
  - 4.x - キーボードスキンへの対応や音声入力への対応。
  - 5.x - 手書き入力やキーボードカスタマイズ、キーボードサイズの調整(スマートフォンのみ)、[Social IMEに対応](https://ja.wikipedia.org/wiki/Social_IME "wikilink")。ただし手書き入力可能なのは平仮名と英数字のみで、入力後さらに予測変換を行う必要がある。
  - 6.x - タブレット端末に最適化。手書き入力の漢字入力に対応。スマートフォンにおいてQWERTYキーボードに数字キーが表示されるようになる。

<!-- end list -->

  - デフォルトでの搭載機種(これ以外のAndroid端末でも使用可能な場合がある)
    [Xperia](https://ja.wikipedia.org/wiki/SO-01B "wikilink") (SO-01B)
    [Xperia arc](https://ja.wikipedia.org/wiki/SO-01C "wikilink") (SO-01C)
    [Xperia acro](https://ja.wikipedia.org/wiki/Xperia_acro "wikilink") ([SO-02C](https://ja.wikipedia.org/wiki/SO-02C "wikilink") / [IS11S](https://ja.wikipedia.org/wiki/IS11S "wikilink"))
    [Xperia ray](https://ja.wikipedia.org/wiki/SO-03C "wikilink") (SO-03C)
    [Xperia PLAY](https://ja.wikipedia.org/wiki/SO-01D "wikilink") (SO-01D)
    [Sony Ericsson mini](https://ja.wikipedia.org/wiki/S51SE "wikilink") (S51SE)
    [Xperia NX](https://ja.wikipedia.org/wiki/SO-02D "wikilink") (SO-02D)
    [Xperia acro HD](https://ja.wikipedia.org/wiki/Xperia_acro_HD "wikilink") ([SO-03D](https://ja.wikipedia.org/wiki/SO-03D "wikilink") / [IS12S](https://ja.wikipedia.org/wiki/IS12S "wikilink"))
    [Xperia GX](https://ja.wikipedia.org/wiki/SO-04D "wikilink") (SO-04D)
    [Xperia SX](https://ja.wikipedia.org/wiki/SO-05D "wikilink") (SO-05D)
    [Xperia VL](https://ja.wikipedia.org/wiki/SOL21 "wikilink") (SOL21)
    [Xperia AX](https://ja.wikipedia.org/wiki/SO-01E "wikilink") (SO-01E)
    [Xperia Z](https://ja.wikipedia.org/wiki/SO-02E "wikilink") (SO-02E)
    [Xperia Tablet Z](https://ja.wikipedia.org/wiki/SO-03E "wikilink") (SO-03E) / [Xperia Tablet Z](https://ja.wikipedia.org/wiki/Xperia_Tablet_Z "wikilink") (Wi-Fiモデル)
    [Xperia A](https://ja.wikipedia.org/wiki/SO-04E "wikilink") / Xperia feat. HATSUNE MIKU (SO-04E)
    [Xperia UL](https://ja.wikipedia.org/wiki/SOL22 "wikilink") (SOL22)
    [Xperia Z1](https://ja.wikipedia.org/wiki/Xperia_Z1 "wikilink") ([SO-01F](https://ja.wikipedia.org/wiki/SO-01F "wikilink") / [SOL23](https://ja.wikipedia.org/wiki/SOL23 "wikilink"))
    [Xperia Z1 f](https://ja.wikipedia.org/wiki/SO-02F "wikilink") (SO-02F)

### 家電製品

  - ソニー [Airboard](https://ja.wikipedia.org/wiki/Airboard "wikilink")
  - ソニー DCR-IP55([カムコーダ](../Page/カムコーダ.md "wikilink"))
  - ソニー DPP-EX50([プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink"))

## 関連項目

  - [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink") - POBoxの開発経験を買われ[2006年](../Page/2006年.md "wikilink")に米[アップルに入社した増井らの手によって](../Page/アップル_\(企業\).md "wikilink")、[日本語入力システム](../Page/日本語入力システム.md "wikilink")の開発が行われた。

## 脚注

## 外部リンク

  - [チュートリアル予測/ 例示インタフェースの研究動向](http://pitecan.com/papers/PBESurvey/PBESurvey.pdf)
  - [seesaa download POBox for Windows](http://download.seesaa.jp/contents/win/system/ime/06534/)

[Category:文字入力補助](https://ja.wikipedia.org/wiki/Category:文字入力補助 "wikilink") [Category:日本語入力ソフト](https://ja.wikipedia.org/wiki/Category:日本語入力ソフト "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:Androidのソフトウェア](https://ja.wikipedia.org/wiki/Category:Androidのソフトウェア "wikilink") [Category:ソニー](https://ja.wikipedia.org/wiki/Category:ソニー "wikilink")

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