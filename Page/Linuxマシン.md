> この記事は[Linux](https://ja.wikipedia.org/wiki/Linux)から翻訳されています。


**Linuxマシン**（リナックスマシン）とは、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")や、Linuxカーネルを含めた[GNU/Linuxオペレーティングシステム](https://ja.wikipedia.org/wiki/GNU/Linuxオペレーティングシステム "wikilink")を実行するコンピュータを指す。ソフトウェアだけではなく、ハードウェアも含めている。**Linuxボックス**と呼ぶこともある（英語ではLinux boxが普通の呼び名）。

Linuxは多くの種類の[コンピュータ](../Page/コンピュータ.md "wikilink")（[CPU](../Page/CPU.md "wikilink")アーキテクチャ、[コンピュータ・アーキテクチャ](../Page/コンピュータ・アーキテクチャ.md "wikilink")）で利用可能な[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) で、Linuxマシンと呼んでも、通常の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")を始め、マッチ箱程度のサイズから、大きなものは[メインフレーム](../Page/メインフレーム.md "wikilink")と呼ばれる大型のコンピュータまで、世界に存在するコンピュータと呼べる多くの物の上で動作している。そのため、Linuxマシンに、典型的な外観を定義することは出来ない。しかし、Linuxマシンと言ったとき、多くの場合はパーソナルコンピュータ、[サーバ](../Page/サーバ.md "wikilink")コンピュータでLinuxが動作しているものを指す。

Linuxマシンを作ることが出来るコンピュータのタイプ（CPUアーキテクチャ）は[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")を参照のこと。

Linuxマシンと言った場合、ネットワーク上で独立した単位のコンピュータを指す場合が多く、複数のLinuxマシンが何らかのネットワークで接続され、処理を複数のコンピュータで処理し、利用者から一つのコンピュータの塊に見えるような場合は、[Linuxクラスタ](https://ja.wikipedia.org/wiki/Linuxクラスタ "wikilink")（または[コンピュータ・クラスタ](https://ja.wikipedia.org/wiki/コンピュータ・クラスタ "wikilink")）と呼ぶ。

また、Linuxクラスタの一種であるが、クラスタが[インターネット](../Page/インターネット.md "wikilink")上に作られているような場合は、[Linuxグリッド](https://ja.wikipedia.org/wiki/Linuxグリッド "wikilink")と呼ぶ。グリッドの場合、特に複数のOSが参加できるようにしている場合が多い。

## Linuxマシンの使われ方

## Linuxマシンの分類

  - [ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")
    概ね、マッチ箱からVHSテープの大きさのコンピュータで、ルータとして使われる。一般にハードウェアの性能が非常に低いため、メモリフットプリントの小さい軽量版[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")が用いられる。

<!-- end list -->

  - タワー型サーバ
    机や床などに据え置きするタイプのサーバで、タワー型PCと同様な形をしている。大きさは[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")のミニタワーサイズから冷蔵庫大サイズまで様々ある。

<!-- end list -->

  - [ブレードサーバ](../Page/ブレードサーバ.md "wikilink")
    [Webサーバ](../Page/Webサーバ.md "wikilink")、[データベースサーバを稼働させている業務用の薄型サーバである](../Page/データベース管理システム.md "wikilink")。サーバラックに集約して運用することが多く、単体で用いることは少ない。ネットワークを介して遠隔操作するため、レスポンス向上のために、CUIによる操作が一般的である。

<!-- end list -->

  - ラックマウント型サーバ
    インターネットデータセンター等に設置されているサーバ用のラック（[19インチラック](../Page/19インチラック.md "wikilink")）にマウントするのに適した形状のサーバである。ラックサーバとも呼ばれる。詳細は[ラックマウント型サーバ](../Page/ラックマウント型サーバ.md "wikilink")を参照。

<!-- end list -->

  - パーソナルコンピュータ/ワークステーション
    ユーザーが物理的に直接操作するコンピュータである。CPU,メモリ以外にも、GPUやオーディオ等多様な機能が搭載される傾向にある。殆どの場合[X Window Systemを搭載しているため](../Page/X_Window_System.md "wikilink")、GUIで操作可能な場合が多い。利用するハードウェアが対応している限り、OSの選択に制約はなく、様々な[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")が利用可能である。

<!-- end list -->

  - クラスタ
    サーバを集めたもの。[データセンター](https://ja.wikipedia.org/wiki/データセンター "wikilink")内で稼働している。スペースの制約から、ブレードサーバをサーバラックに集約するタイプが多い。ネットワークを介して遠隔操作するため、レスポンス向上のために、CUIによる操作が一般的である。

<!-- end list -->

  - メインフレーム
    企業の基幹業務処理向けに特別に設計される、高性能,高信頼な大型汎用コンピュータである。企業システムの中枢部として稼働する。2000年以前は信頼性確保の面からAT\&T社に起源を持つUNIXが用いられて来た。しかし、それ以降は徐々にLinuxが普及して行った。ネットワークを介して遠隔操作するため、レスポンス向上のために、CUIによる操作が一般的である。

## Linuxボックスの作り方

## 関連記事

  - [Linux](../Page/Linux.md "wikilink")
  - [Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")