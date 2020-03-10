> この記事は[Incompatible Timesharing System](https://ja.wikipedia.org/wiki/Incompatible_Timesharing_System)から翻訳されています。


**Incompatible Timesharing System**（**ITS**）は、[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")(MIT)で開発された初期の[タイムシェアリング](../Page/タイムシェアリングシステム.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)の1つ。[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書かれており、[CTSS](https://ja.wikipedia.org/wiki/CTSS "wikilink")（Compatible Time-Sharing System）との対比で名づけられている。主に[MIT人工知能研究所](../Page/MIT人工知能研究所.md "wikilink")で開発され、[Project MACからも何らかの助力があった](https://ja.wikipedia.org/wiki/Project_MAC "wikilink")。

## 歴史

ITSの開発は、Project MAC において[Multics](https://ja.wikipedia.org/wiki/Multics "wikilink")プロジェクトの方向性を良しとしない人々（人工知能研究所の大多数）により[1960年代](../Page/1960年代.md "wikilink")末ごろに開始された。特に問題とされたのは、Multics における強力なセキュリティ機能であった。名称は、Tom Knight が MIT の初期のタイムシェアリングOS [CTSS](https://ja.wikipedia.org/wiki/CTSS "wikilink") から発想して付けたとされている。

ITS は当初[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") [PDP-6](https://ja.wikipedia.org/wiki/PDP-6 "wikilink") 向けに開発され、後に [PDP-10](https://ja.wikipedia.org/wiki/PDP-10 "wikilink") に移植された（というよりも開発の大部分は PDP-10 向けに行われた）。1982年以降はあまり使われなかったものの、1990年までMITで稼動し、その後1995年までスウェーデンの Stacken Computer Club で稼動していた。

## 主な特徴

ITS には数多くの革新的機能が備わっていた。以下は、その中でも世界初の実装となった機能である:

  - 世界初のデバイス非依存のグラフィックス端末出力を備えていた。プログラムでは汎用的な表示制御コマンドを使い、システムがそれを自動的に端末機器毎の適切な制御文字列などに変換した。
  - ユーザープロセス内で動作する仮想デバイスをソフトウェアで実装するための汎用機構。
  - また、その機構を使った、透過的なマシン間共有型ファイルシステム（ほぼ世界初）。ITSマシンは全て[ARPANET](../Page/ARPANET.md "wikilink")に接続されていて、あるマシン上で他のマシンにあるファイルをローカルにあるファイルと同じように扱うことができた。
  - 洗練された[プロセス管理](../Page/プロセス管理.md "wikilink")。ユーザープロセスは[木構造の階層を形成しており](../Page/木構造_\(データ構造\).md "wikilink")、上位のプロセスが下位の複数のプロセスを制御する。下位プロセスは任意の時点で処理を中断させられ、その状態（レジスタの内容など）を調べることができる。その後、そのプロセスを問題なく再開させることが可能。
  - 高度なソフトウェア割り込み機構を持ち、ユーザープロセスの非同期操作が可能。
  - PCLSRing という機構により、擬似[不可分操作](https://ja.wikipedia.org/wiki/不可分操作 "wikilink")、割り込み可能な[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")などを提供。それまで、システムコールの途中で自分自身を含む任意のプロセスがその状態を観察することはできなかった。

これらの機能や他の先進的な機能は、その後のオペレーティングシステムに取り入れられた。

## ユーザー環境

ユーザー環境は、当時の他のOSとは全く異なっていた。

  - 当初、パスワードがなく、ユーザーはログオンすることなくITSを使うことができた。正式にはログオンは可能だが、単に他のユーザーがあるユーザーがシステムを使っていることを知ることができるという意味しかない。
  - システムの問題点をユーザーが発見した場合、その対処に斬新な手法が用いられた。システムをクラッシュさせるコマンドが用意されていて、これを誰でも実行することができるようになっていた。このコマンドは同時に誰がそのコマンドを実行したかをブロードキャストで通知するようになっていた。
  - 全てのファイルを誰でも編集可能。
  - 他のユーザーの使っている端末間で会話が可能であり、使用中の他のユーザーに助けを求めるコマンド（SHOUT）も用意されていた。
  - 他のユーザーの端末の表示を見ることが可能である（*OS* = "output spy" というコマンドを使用）。見られているユーザーには通知が行くので、見ている人とのセッションを見られている側から切断可能（*JEDGAR* コマンドを使用。その名称は[FBIの](../Page/連邦捜査局.md "wikilink")[ジョン・エドガー・フーヴァー](https://ja.wikipedia.org/wiki/ジョン・エドガー・フーヴァー "wikilink")から）。
  - ゲスト（TURIST）は研究所内の端末からでもARPANET上の外部のシステムからでも利用可能であった。このようなアクセスに関する[ポリシー](http://www.art.net/Studios/Hackers/Hopkins/Don/text/tourist-policy.html)が後に制定された。なお、"TURIST" というのはファイル名が6文字に制限されていたためで、PDP-10 が36ビットワードであったため、1文字6ビットで6文字が1ワードに収まったため、このような制限があった。

このような奇異な特徴が数ある中でも、ITSのトップレベルの[コマンドインタプリタはPDP](../Page/キャラクタユーザインタフェース.md "wikilink")-10の機械語デバッガ(DDT)で、未経験者にはそのコマンドは全く解読不能であった。

主なエディタとしては長年 [TECO](https://ja.wikipedia.org/wiki/Text_Editor_and_Corrector "wikilink") が使われていた。[Emacs](../Page/Emacs.md "wikilink")は当初、TECO 用マクロを集めたものであった。

ITS上では様々なソフトウェアが開発されたが、中でも[数式処理システム](../Page/数式処理システム.md "wikilink") [Macsyma](https://ja.wikipedia.org/wiki/Macsyma "wikilink")、[GNU](../Page/GNU.md "wikilink") INFO ヘルプシステム、[Maclisp](https://ja.wikipedia.org/wiki/Maclisp "wikilink")、[Emacs](../Page/Emacs.md "wikilink") などが有名である。

[ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")も ITS 上で始まったものである。

## 初期の開発者

  - [リチャード・グリーンブラット](https://ja.wikipedia.org/wiki/リチャード・グリーンブラット "wikilink")
  - Stewart Nelson
  - Tom Knight

## 参考文献

  - [ITS bibliography](http://www.stswiki.org/wiki/Incompatible_Timesharing_System_bibliography)
  - Bawden, Allen (n.d.) *[PCLSRing: Keeping Process State Modular](http://fare.tunes.org/tmp/emergent/pclsr.htm)*
  - Chiou, S; Music, C; Sprague, K; Wahba,R (2001). "[A Marriage of Convenience: The Founding of the MIT Artificial Intelligence Laboratory](http://mit.edu/6.933/www/Fall2001/AILab.pdf)." (pdf)
  - Eastlake, Donald E. (1972). *[ITS Status Report](ftp://publications.ai.mit.edu/ai-publications/pdf/AIM-238.pdf)* （文書をスキャンした画像をPDF化したもので、大きいので注意）
  - Lin, Yuwei (2004). “[Epistemologically Multiple Actor-Centered Systems: or, EMACS At Work\!](http://www.acm.org/ubiquity/views/pf/v5i1_lin.pdf) Ubiquity 5(1). (pdf file)
  - Williams, S. (2002). ''[Free as in Freedom: Richard Stallman's Crusade for Free Software.](http://www.faifzilla.org/toc.html)" Petaluma, CA: O'Reilly.

## 外部リンク

  - [Ken Harrenstien's PDP-10 simulator](http://klh10.trailing-edge.com/)
  - [file system images of various ITS machines, including source and documentation of the final system](http://www.its.os.org/)
  - [instructions allowing ITS to run on a PDP-10 emulator.](http://www.cosmic.com/u/mirian/its/)
  - [(Historical) Tourist access policy in ITS at MIT.](http://www.art.net/Studios/Hackers/Hopkins/Don/text/tourist-policy.html)
  - [An Introduction to ITS for the MACSYMA User](http://zane.brouhaha.com/~healyzh/_info_/its.primer)
  - [ITS System Documentation](http://zane.brouhaha.com/~healyzh/sysdoc/sysdoc.html)
  - [Jargon File Entry](http://catb.org/~esr/jargon/html/I/ITS.html)
  - [Donald Fisk's ITS info](http://web.onetel.com/~hibou/ITS.html)

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:マサチューセッツ工科大学](https://ja.wikipedia.org/wiki/Category:マサチューセッツ工科大学 "wikilink")