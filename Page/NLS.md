> この記事は[NLS](https://ja.wikipedia.org/wiki/NLS)から翻訳されています。


**NLS**（oN-Line System）は、[ダグラス・エンゲルバート](../Page/ダグラス・エンゲルバート.md "wikilink")率いる研究者チームが[1960年代](../Page/1960年代.md "wikilink")に[スタンフォード研究所](https://ja.wikipedia.org/wiki/スタンフォード研究所 "wikilink")(SRI)内の [Augmentation Research Center](https://ja.wikipedia.org/wiki/:en:Augmentation_Research_Center "wikilink") (ARC) で設計・開発した革新的な[マルチユーザー](https://ja.wikipedia.org/wiki/マルチユーザー "wikilink")連携[システム](../Page/システム.md "wikilink")。NLSは世界で初めて、[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")リンク、[マウス](../Page/マウス_\(コンピュータ\).md "wikilink")、[ラスタースキャン](../Page/ラスタースキャン.md "wikilink")型[ディスプレイ](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")、関連性によって組織された情報、[グラフィカルユーザインターフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")、[プレゼンテーションソフトウェア](../Page/プレゼンテーションソフトウェア.md "wikilink")など様々なコンセプトを実用化した。[ARPA](../Page/国防高等研究計画局.md "wikilink")、[NASA](../Page/アメリカ航空宇宙局.md "wikilink")、[アメリカ空軍](https://ja.wikipedia.org/wiki/アメリカ空軍 "wikilink")が資金提供した。

## 開発

[ダグラス・エンゲルバート](../Page/ダグラス・エンゲルバート.md "wikilink")は空軍の支援で研究していた1959年から1960年にかけてそのコンセプトを発展させ、1962年にフレームワークを発表した。NLSという奇妙な頭字語（本来なら OLS）は、システム発展の経緯の産物である。最初に使用したコンピュータは1人のユーザーしかサポートできなかった。1963年に使用した  の能力は非常に貧弱だった\[1\]。

場当たり的暫定措置として、チームはオフラインユーザーのためのシステムを開発した。これは、オンラインのワークステーションを使えないとき、コマンド列を[紙テープ](../Page/紙テープ.md "wikilink")にパンチすることで文書の編集ができるようにしたものである。ここでいうオンライン・オフラインという語は通信回線がつながっているという今日的な意味とは異なり、計算機にリアルタイムに直接的にデータ入力することをオンライン、別の装置でパンチカードなどのメディアに書き込んでおいてから後で計算機に入力させようとする事をオフラインと呼んでいる。オフライン作業では視覚的[フィードバック](../Page/フィードバック.md "wikilink")なしで作業しなければならないため、非常に使いにくいことは明白であった。不運なユーザーは頭の中でコマンドの効果を確認しなければならなかった。ある意味でUNIXのテキストエディタ [ed](https://ja.wikipedia.org/wiki/ed "wikilink") に似ているとも言える。一方で、1960年代のオフィスの慣習にはマッチしていたとも言え、管理職は原稿に赤を入れて秘書に渡していた\[2\]。

テープが完成すると、ユーザーは編集対象の文書の収められた紙テープと新たなコマンド列の収められた紙テープをコンピュータにセットし、そのコマンド列が適用された新たな文書の最新版の紙テープを得る。このような「オフライン」のワークフローと対話型の「オンライン」の編集機能が同時にサポートされていた。"off-line" も "on-line" も同じ O で始まるため、オフラインのシステムを FLTS (Off-Line Text System)、オンラインのシステムを NLTS (On-Line Text System) と呼んだ。テキスト編集以外の機能も備えるようになると "T" が省かれ、対話型バージョンは NLS と呼ばれるようになった\[3\]。

心理学の素養もあった[ロバート・テイラーは](../Page/ロバート・テイラー_\(情報工学者\).md "wikilink")[NASAから資金を提供](../Page/アメリカ航空宇宙局.md "wikilink")。その後テイラーが[ARPAのIPTO](../Page/国防高等研究計画局.md "wikilink")に移ると、さらに積極的にこのプロジェクトに資金提供しはじめた。1965年、NLSの開発は  上に移行\[4\]。1966年、[Jeff Rulifson](https://ja.wikipedia.org/wiki/:en:Jeff_Rulifson "wikilink") がSRIに参加し、1973年までNLSの主任プログラマを務めた\[5\]。

1968年、NLSの開発は Scientific Data Systems 社の[タイムシェアリング型](../Page/タイムシェアリングシステム.md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink") [SDS 940](https://ja.wikipedia.org/wiki/SDS_940 "wikilink") へと移行した\[6\]。約96MBのディスク装置を備えていた。最大16台の[ワークステーション](../Page/ワークステーション.md "wikilink")を接続可能であり、各ワークステーションには[ラスタースキャン](../Page/ラスタースキャン.md "wikilink")型[ディスプレイ](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")、3ボタン式[マウス](../Page/マウス_\(コンピュータ\).md "wikilink")、[Chord Keyset](https://ja.wikipedia.org/wiki/:en:chord_keyset "wikilink") と呼ばれる[入力機器](https://ja.wikipedia.org/wiki/入力機器 "wikilink")が備わっている。キーボードから入力されたテキストはあるサブシステムを経由して2つあるディスプレイ・コントローラとディスプレイ・ジェネレータの一方にバスを経由して送られる。入力テキストはその後 5 インチ（127 mm）の[ブラウン管](../Page/ブラウン管.md "wikilink")(CRT)に送られる。CRTには特殊なカバーがかかっていて、表示されたビデオ画像は高解像度のモノクロTVカメラで撮影される。TVカメラの情報は有線カメラ制御と[パッチパネル](https://ja.wikipedia.org/wiki/パッチパネル "wikilink")に送られ、最終的に各ワークステーションのモニターに表示される。

NLSの開発は[1968年](https://ja.wikipedia.org/wiki/1968年 "wikilink")後半になんとか完了し、1968年12月9日、[サンフランシスコ](../Page/サンフランシスコ.md "wikilink")で技術者らの前で実演が行われた。そのデモは最先端のビデオ技術を使い、従来になかった手法でNLSの新規性を実演してみせたことから、「全てのデモの母」と呼ばれている。ステージ上のエンゲルバートの端末は[エイムズ研究センター](https://ja.wikipedia.org/wiki/エイムズ研究センター "wikilink")から借りた巨大[プロジェクタ](../Page/プロジェクタ.md "wikilink")と接続され、NLS は[電話](../Page/電話.md "wikilink")回線で[メンローパークのARCにある](https://ja.wikipedia.org/wiki/メンローパーク_\(カリフォルニア州\) "wikilink") SDS 940 と接続されていた。[ダグラス・エンゲルバート](../Page/ダグラス・エンゲルバート.md "wikilink")はヘッドセットをつけて聴衆に説明し、プレゼンテーション用の22フィートのプロジェクション・スクリーンにはエンゲルバートの手元の動きが大写しされたので、観衆はマウスの使い方などがよくわかり、メンローパークにいたチームメンバーもプレゼンテーションに参加した\[7\]。

NLS の最も革新的な機能の1つである Journal は、1970年に David Evans が彼の博士論文の一環で開発したものである\[8\]。Journal は原始的なハイパーテキストベースの[グループウェア](../Page/グループウェア.md "wikilink")であり、その後の共同型文書作成サポートソフトウェア（たとえば、[ウィキ](../Page/ウィキ.md "wikilink")）の先駆けと思われる。ARC ではこれを議論やコンセプトを洗練させることに使用したが、これも今日のウィキなどと全く同じである。Journal は初期の[ネットワークインフォメーションセンターでの文書保管や初期の](https://ja.wikipedia.org/wiki/InterNIC "wikilink")[電子メール](../Page/電子メール.md "wikilink")アーカイブに使われていた\[9\]。Journal に関する文書のほとんどは紙の形で保存されており、[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")にある。それらは1970年から1976年の商用化開始までの ARC に関する貴重な記録でもある。他に[コンピュータ歴史博物館](https://ja.wikipedia.org/wiki/コンピュータ歴史博物館 "wikilink")にも記録が保管されている。

NLSは[TREE-METAという](https://ja.wikipedia.org/wiki/:en:TREE-META "wikilink")[パーサジェネレータ](https://ja.wikipedia.org/wiki/パーサジェネレータ "wikilink")を使ったいくつかの[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")を使って実装された\[10\]。最終的に使われた実装言語はL10と呼ばれている\[11\]。

1970年、NLSは[PDP-10](../Page/PDP-10.md "wikilink")（[BBNが](../Page/BBNテクノロジーズ.md "wikilink")[TENEXが動作するよう改造したバージョン](https://ja.wikipedia.org/wiki/TOPS-20#TENEX "wikilink")）に移植された\[12\]。1971年中ごろ、TENEX版NLSがネットワークインフォメーションセンター (NIC) で実際に使われるようになったが、同時に利用できるユーザー数は少なかった\[13\]。専用ワークステーション以外に、当時一般的だった安価なタイプライター型の端末からもアクセス可能だった。1974年までにNICは別プロジェクトとして独立し、自前のコンピュータを使用するようになった。

## 世界初

NLSのあらゆる機能は、エンゲルバートの「集団による知的作業の強化」という目標に沿ったもので、単にシステムを使いやすくするのではなく、ユーザーの知的作業を強化することに集中していた\[14\]。従って以下に示す機能群は、エンゲルバートが後に WYSIAYG (What You See Is All You Get)\[15\] パラダイムと称したものというよりも、熟練したユーザーが駆使できる可能性を持った完全対話型パラダイムをサポートするものだった\[16\]。

  - コンピュータマウス
  - 2次元ディスプレイ編集
  - ファイル内オブジェクトアドレッシング、リンク
  - ハイパーメディア
  - アウトライン処理
  - 柔軟なビュー制御
  - マルチウィンドウ
  - ファイルをまたいだ編集
  - ハイパーメディアを使った電子メール
  - ハイパーメディア出版
  - 文書の版管理
  - 画面共有型会議システム

<!-- end list -->

  - コンピュータ支援会議
  - フォーマット・ディレクティブ
  - 文脈依存ヘルプ
  - 分散クライアント・サーバ・アーキテクチャ
  - 一様なコマンド文法
  - 汎用ユーザインタフェースのためのフロントエンド・モジュール
  - 複数ツールの統合
  - 文法駆動型コマンド言語インタプリタ
  - 仮想端末用プロトコル
  - RPCプロトコル
  - 互換「コマンドメタ言語」

## 転落と後継

NLS、そして ARC の転落の原因として、そのプログラムの習熟が困難であったことが挙げられる。NLS は学習しやすさを設計のポイントとしておらず、プログラムモードを多用し、厳密な階層構造に依存し、ポイント・アンド・クリックといった簡単なインターフェイスを持たず、役に立つことをするには暗号のようなコードを覚える必要があった。キーボードの代替として Chord Typeset を使う場合、5ビットの二進数コードを覚える必要があった。さらに[1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")、SRI に[ARPANET](../Page/ARPANET.md "wikilink")が接続され、分散[コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")の時代となり、少人数向けの[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")は時代遅れとなりつつあった。実際、タイムシェアリングは急速に個人用のミニコンピュータ（さらにはパーソナルコンピュータ）やワークステーションに代替されていった。NLS を他のハードウェアに移植する作業も行われ、[PDP-10](../Page/PDP-10.md "wikilink") などへの移植に成功したものの、NLS を SRI 以外に広めようという動きは起きなかった。

エンゲルバートの「ブートストラッピング」活動の方向性に不満を感じた SRI の研究者らの多くは[パロアルト研究所](https://ja.wikipedia.org/wiki/パロアルト研究所 "wikilink")に移り、マウスの考え方をもたらした。1977年、SRI は NLS を Tymshare 社に売却し、NLS は Augment と名称が変更された。Tymshare 社はその後それを[マクドネル・ダグラス](../Page/マクドネル・ダグラス.md "wikilink")社に[1980年代](../Page/1980年代.md "wikilink")初めに売却した\[17\]。NDMA Inc. が販売した HyPerform というソフトウェアは NLS/Augment の後継品である。

「完全対話型」というパラダイムの一部は、他のシステムに継承された。例えば、[Mozilla](../Page/Mozilla.md "wikilink") [Firefox](../Page/Mozilla_Firefox.md "wikilink") のアドオンである [Hyperwords](https://ja.wikipedia.org/wiki/:en:Hyperwords "wikilink") がある。Hyperwords はエンゲルバートのウェブドキュメンタリー Invisible Revolution に触発されて考案された\[18\]。そのプロジェクトは、ウェブ上のリンクのない単語とも相互作用できることを目的としている。Hyperwords は単純な階層型メニューを通して機能する。エンゲルバートはこのプロジェクトの諮問委員を務めていた。

2005年から2008年にかけて、[コンピュータ歴史博物館](https://ja.wikipedia.org/wiki/コンピュータ歴史博物館 "wikilink")のボランティアチームがNLSの復元を試みた\[19\]\[20\]。

## 脚注

## 関連文献

  -
## 関連項目

  - [ENQUIRE](../Page/ENQUIRE.md "wikilink")

## 外部リンク

  - [Doug Engelbart Institute website](http://www.dougengelbart.org)
      - [1968 Demo resources page](http://www.dougengelbart.org/firsts/dougs-1968-demo.html)
      - [About NLS/Augment](http://www.dougengelbart.org/about/augment.html)
      - [Bibliography](http://www.dougengelbart.org/about/bibliography.html)
      - [Videography](http://www.dougengelbart.org/library/videography.html)
      - [Engelbart Archives Special Collections](http://www.dougengelbart.org/library/engelbart-archives.html)
  - [1968年のオリジナルデモの RealVideo クリップ](http://sloan.stanford.edu/mousesite/1968Demo.html)
  - [1968年のデモの高解像度版ビデオ](http://www.1968demo.org/)
  - [HyperScope, ブラウザベースでの NLS 再生・拡張プロジェクト](http://hyperscope.org) ダグラス・エンゲルバート自身が参加している
  - [OpenAugment, もう1つの NLS/Augment の実装](http://www.openaugment.org/)
  - [NLS documents at bitsavers.org](http://bitsavers.org/pdf/sri/arc)

[Category:ハイパーテキスト](https://ja.wikipedia.org/wiki/Category:ハイパーテキスト "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  David Evans という名の著名な学者は何人かいるので、混同に注意。 [David A. Evans](http://unrev.stanford.edu/presenters/david_evans/david_evans.html)
9.
10. Engelbart, D., Study for the development of Human Augmentation Techniques. Final Report, July 1968. Sections 4 and 5.
11.
12.
13.
14.
15. ["What you see is ALL you get"](http://www.guidebookgallery.org/articles/inventingthelisauserinterface/whatyouseeisallyouget) Harvey Lehtmann, Interactions, issue 2/1997, pp. 51.
16.
17.
18.
19.
20.