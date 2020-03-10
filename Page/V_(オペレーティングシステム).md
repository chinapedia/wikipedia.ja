> この記事は[V \(\)](https://ja.wikipedia.org/wiki/V_\(\))から翻訳されています。


**V オペレーティングシステム**（**V-System**とも記されるが [System V](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") との混同に注意）は、1980年代に[デビッド・チェリトン](https://ja.wikipedia.org/wiki/デビッド・チェリトン "wikilink")を中心とした[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")の Distributed Systems Group が開発した[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")型の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。V はチェリトンが以前に開発した Thoth と Verax の後継であった。

  -
    V では今日「[スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")」と呼ばれているものを「プロセス」と呼び、複数のスレッドが1つのアドレス空間を共有する「[プロセス](../Page/プロセス.md "wikilink")」と呼ばれているものを「チーム」と呼んでいた。しかし、本項目では現代的な用語を使う。

V における重要な概念として「[マルチスレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")」と「同期[メッセージパッシング](https://ja.wikipedia.org/wiki/メッセージ_\(コンピュータ\) "wikilink")」がある。V におけるスレッド間通信には同期メッセージパッシングが使われ、簡単に言えば応答する前に送信元のアドレス空間の一部の読み書きができるアクセス権を含めた固定長のメッセージである。このメッセージパッシング・インタフェースは、同じプロセス内のスレッド間でも、同じマシン上の異なるプロセスにあるスレッド間でも、[イーサネット](../Page/イーサネット.md "wikilink")で接続された異なるマシン上のスレッド間でも使われる。メッセージを受信したスレッドは、他のメッセージを受信する前に必ず応答しなければならないわけではない。この点は[Ada](../Page/Ada.md "wikilink")のランデブー機能とは異なる。

メッセージ機能を使う典型パターンは、クライアントがサーバに対して何らかのサービスを要求するパターンである。クライアント側から見れば、これは[遠隔手続き呼出し](https://ja.wikipedia.org/wiki/遠隔手続き呼出し "wikilink") (RPC) のようなものである。自動スタブジェネレータのような便利さはないが、一方でクライアントはパラメータを参照渡しでき、これはRPCには不可能である。サーバ側から見てRPCとは大きくことなる点として、全てのクライアントからの要求はデフォルトでは1つのサーバスレッドに多重化される点が挙げられる。ただし、サーバはスレッドを明示的にフォークさせて、クライアントの要求を並行して処理することもできる。この場合、サーバ側のモデルはRPCにより近くなる。

V はそれ自体がチェリトンのグループの目的というわけではなかった。V は様々な分散オペレーティングシステムやネットワーキングの研究プロジェクトに利用された。当時の同様のオペレーティングシステム研究プロジェクト（Spriteなど）と同様、ほぼ[セルフホスティング](../Page/セルフホスティング.md "wikilink")式の完全なシステムであった。多くの学生が[サンや](../Page/サン・マイクロシステムズ.md "wikilink")[DECのディスクレス型ワークステーションに](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") V を唯一のオペレーティングシステムとして搭載し、使っていた。[コンパイルは](../Page/コンパイラ.md "wikilink") V 自身でも可能だったし、[VAX](https://ja.wikipedia.org/wiki/VAX "wikilink")上の[UNIX](../Page/UNIX.md "wikilink")でも可能だった（こちらの方が安定しているため、V の動作するマシンのファイルサーバとなっていた）。

最近では、PCクラスのマシンで [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") や [BSD](../Page/BSD.md "wikilink") が広く利用できるようになったため、この種のセルフホスティング式でのオペレーティングシステム研究は稀となり、基盤を提供するためだけにそれほどのことをする動機が失われつつある。V は今ではほとんど忘れ去れているが、時代に足跡を残したと言える。V 用に開発された [W Window System](../Page/W_Window_System.md "wikilink") は、[X Window System](../Page/X_Window_System.md "wikilink") の元になった。V はまた、より純粋な[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")の研究プロジェクトである[アップルの](../Page/アップル_\(企業\).md "wikilink") Vanguard も生み出した。Vanguard は基本システムに様々な改良を加えたが、組織改編に伴って消えていった。[テクトロニクス](https://ja.wikipedia.org/wiki/テクトロニクス "wikilink")のテレビ用測定器 VM700 は1980年代末に V を使っているネットワーク環境で開発され、若干修正を加えた V がオペレーティングシステムとして搭載されている。この機器は現在もまだ製造販売されている。

## 参考文献

  - [The V Distributed System](http://eia.udg.es/~teo/sd/documents/articles/p314-cheriton.pdf)

## 外部リンク

  - [Stanford DSG history](http://www.dsg.stanford.edu/History.html)

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink")