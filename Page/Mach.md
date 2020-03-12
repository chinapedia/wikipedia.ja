> この記事は[Mach](https://ja.wikipedia.org/wiki/Mach)から翻訳されています。


**Mach**（**マーク**\[1\]）とは、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の[リチャード・ラシッド](https://ja.wikipedia.org/wiki/リチャード・ラシッド "wikilink")教授（実際の実装は[アビー・テバニアン](../Page/アビー・テバニアン.md "wikilink")が中心\[2\]）らの Mach プロジェクトにより開発された[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")タイプの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS)を言う。名前は「複数非同期通信ホスト」を意味する英語「」に由来している。

## 開発の経緯

1980年代中頃、[アメリカ国防総省](../Page/アメリカ国防総省.md "wikilink")[高等研究計画局によって開発されていた実験用マルチプロセッサコンピューター用のOSを](../Page/国防高等研究計画局.md "wikilink")[アメリカ国防総省](../Page/アメリカ国防総省.md "wikilink")に提案、採用されたことにより 1985年から Mach の開発は始まった。当初はスーパーコンピューター・ワークベンチ・プロジェクト（）と呼ばれていた。

当時、米国の研究機関で主に用いられていた 4.2BSD [UNIX](../Page/UNIX.md "wikilink") の設計は、古く効率の悪い仮想記憶機構、マルチプロセッサマシンに対して非効率な構造、移植性の悪い冗長なコードなど、当初の UNIX では想定していない様々な機能をカーネルに追加したため、非常に見通しの悪い構造となっていた。これを解決することがMachの目的であった。

  - マルチプロセッサ対応（100プロセッサ程度が想定された）
  - 高価で少ない実メモリを想定するのではなく、巨大なメモリ空間と十分な実メモリを有効利用する
  - 分散システムをサポートし、高速でネットワーク透過な [IPC](../Page/プロセス間通信.md "wikilink") をサポート
  - 移植性の高い構造
  - 4.3BSD と完全な互換性

これらを実現することを目標に開発が行われた。

## 歴史

当初から 4.3BSD UNIX と互換であることが決定されていたこともあり、4.3BSD のカーネルソースコードを元に修正を加えることで実装を行った。実際には3.0からがマイクロカーネルであり、Mach 2.5まではマイクロカーネルではない。

  - Mach 1.0
    1986年リリース。研究開発の進捗報告として発表された。新しい仮想記憶とプロセス間通信は実装されていたが、タスクとスレッドはまだ実装されていなかった。
  - Mach 2.0
    1988年リリース。タスクとスレッドの実装、いくつかの改善。初期の [NeXTSTEP](https://ja.wikipedia.org/wiki/NeXTSTEP "wikilink") のカーネルとして利用された。
  - Mach 2.5
    NFS の実装、 の [OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink") のカーネルとして利用された。
  - Mach 3.0
    1989年リリース。マイクロカーネル化。MkLinux のカーネルとしても使われた。Mach 3.0は、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")のカーネル*[XNU](../Page/XNU.md "wikilink")*にも用いられているが、実装はマイクロカーネルではない。

[リチャード・ラシッド](https://ja.wikipedia.org/wiki/リチャード・ラシッド "wikilink")教授が1991年に[マイクロソフト](../Page/マイクロソフト.md "wikilink")へ移籍した後も1994年まで[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")でMachプロジェクトは続いた。以後、Machの開発はユタ大学のMach 4 プロジェクト、 の Hurd プロジェクト、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の ARTプロジェクトなどに引き継がれていった。ユタ大学で Mach 4として分散環境を考慮したスレッドおよびメッセージの改良、Linux デバイスドライバインターフェースの実装を行った。FSF ではこの Mach 4をベースに改良を加え、[GNU Mach](https://ja.wikipedia.org/wiki/GNU_Mach "wikilink") として公開している。ARTプロジェクトでは分散リアルタイムOS実現のため、実時間駆動型スケジューラなどが Mach に組み込まれ、 として公開された。これらの研究開発は Mach のみならず BSD にもフィードバックされ、仮想記憶システムを含むいくつかの機能は 4.4BSD Lite にも利用されている。

## Mach の基本概念

  - タスク
    UNIX のプロセスは計算処理とそれに必要なリソースを一体化しているのに対し、Mach は計算処理とそのリソースを分離するとともに、独立に制御できるようにした。タスクは CPU 実行時間（スレッド）やメモリオブジェクト、アドレス空間、ポート等のリソースの集合体である。
  - スレッド
    UNIX のプロセスから、CPU 実行時間をリソースとして分離、抽象化したもの。スレッドは CPU の処理単位であり、並列に動作することができる。スレッドは必ず一つのタスクに属し、そのタスクの全てのリソースにアクセスできる。タスクは複数のスレッドを持つこともできる。リソースの保護はタスクを単位として行われるため、UNIX プロセスと異なりメモリ空間などのリソースと直接関連しない。結果としてスレッドの生成や切り換えは高速に行われるとともに、マルチプロセッサにも最適化される。
  - ポート
    初期の UNIX ではパイプ機能が主なプロセス間通信の手法であったが、ファイルを抽象化したパイプ機能では、様々な形態のデータの受け渡しを十分に抽象化できなくなっていた。UNIX では様々なデータの受け渡しを実現するため、様々な方法で拡張を行ったが\[3\]、Mach ではそれらを統合して新たにポートという概念を実装した。ポートはデータ受け渡しのために使われる通信チャネルである。構造化されたメッセージを受け渡す枠組みを実現し、ネットワーク越しの通信も含めて抽象化するとともに、高速、効率的なメッセージの送受信（out-of-lineデータ）が可能となった。
  - メッセージ
    カーネルが管理するプロセス間通信のデータオブジェクト。メッセージは複数の型づけされたデータの集まりである。メッセージはカーネルによって管理され、ポートを通じてプロセス間の通信に用いられる。
  - メモリオブジェクト
    Mach は UNIX と異なり、仮想記憶を管理する機能をカーネル内部に実装（内部ページャ）しているだけではなく、ユーザーレベルにも開放している（外部ページャ）。ページャが操作するメモリの基本的な抽象概念をメモリオブジェクトと呼ぶ。4.3BSD では実現できなかった [copy-on-write](../Page/コピーオンライト.md "wikilink") や map-on-reference といった[遅延評価](../Page/遅延評価.md "wikilink")のメカニズム\[4\]が実装され、効率よくメモリ資源を利用できるようになった。

これらの Mach 生まれの基本概念は、その後の UNIX のみならず、数多くの OS に多大な影響を及ぼした。

## 読み方

この新しい OS の名前をどうするのかという雑談の中で出た MUCK () というアイディアを、[リチャード・ラシッド](https://ja.wikipedia.org/wiki/リチャード・ラシッド "wikilink")教授の同僚のイタリア人 Darlo Giuse が Mach と聞き間違えたことに由来する。最終的にはコインの裏表で決定した\[5\]。従って原則英語読みの「マーク」という発音が正しい。

## Machを採用したOS

  - [OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink")
  - [NEXTSTEP](../Page/NEXTSTEP.md "wikilink") - Mach用[OPENSTEP](../Page/OPENSTEP.md "wikilink")
  - [GNU Hurd](../Page/GNU_Hurd.md "wikilink") ([GNU Mach](https://ja.wikipedia.org/wiki/GNU_Mach "wikilink"))
  - [MkLinux](https://ja.wikipedia.org/wiki/MkLinux "wikilink")
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink"), [iOS](https://ja.wikipedia.org/wiki/IOS_\(アップル\) "wikilink") ([Darwin](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")) （ただし、実行効率を得るために実行レベルでは単一バイナリになっている）

## 関連項目

  - [分散オペレーティングシステム](https://ja.wikipedia.org/wiki/分散オペレーティングシステム "wikilink")
  - [マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")
  - [BSD](../Page/BSD.md "wikilink")

## 脚注

<references/>

## 参考文献

  -
  -
[Category:OSのカーネル](https://ja.wikipedia.org/wiki/Category:OSのカーネル "wikilink") [Category:1986年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1986年のソフトウェア "wikilink")

1.  一般相対性理論におけるアインシュタイン方程式の宇宙定数Λの有無を決定する[マッハの原理](https://ja.wikipedia.org/wiki/マッハの原理 "wikilink")を提唱した[エルンスト・マッハ](../Page/エルンスト・マッハ.md "wikilink")の人名のマッハ（Mach）と同じアルファベットであることから**マッハ**と呼ばれることもあるが、正式にはマークと呼ぶのが正しいとされる。
2.  [Darwin Releases](http://www.opensource.apple.com/darwinsource/) Sourceのリスト内からダウンロード出来るxnuのソースコードを参照
3.  共有メモリ、4.2BSD 以降での Socket、SystemV での msgrop() など
4.  メモリを要求された時点で確保するのではなく、使用された時点で確保する方式。メモリがコピーされた場合も、実際の動作としてはコピーではなく仮想記憶機構を利用して多重参照するだけとし、実際にコピーを行うのは、書き換えられた領域のみとなる。結果として必要最小限のメモリ確保、メモリコピーしか行われないというメリットを持つ
5.  [Mach(1993)](https://ja.wikipedia.org/wiki/#Mach\(1993\) "wikilink") p.v