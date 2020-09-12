> この記事は[Pilot \(オペレーティングシステム\)](https://ja.wikipedia.org/wiki/Pilot_\(オペレーティングシステム\))から翻訳されています。


**Pilot** は、1977年初頭に [Xerox PARC](https://ja.wikipedia.org/wiki/Xerox_PARC "wikilink") によって設計されたシングルユーザの[マルチタスク](../Page/マルチタスク.md "wikilink") OS である。Pilot は [Mesa プログラミング言語で書かれており](../Page/Mesa.md "wikilink")、合計で約 24,000 [行のコードが含まれている](https://ja.wikipedia.org/wiki/LOC "wikilink")\[1\]。

Pilot は、高度にネットワーク化された他の Pilot システムが共存する環境において、シングルユーザシステムとして設計されており、Pilot ストリームインターフェースを介してネットワーク上で[プロセス間通信](../Page/プロセス間通信.md "wikilink") (IPC) を行うように設計されたインターフェースを備えている。Pilot は、[仮想メモリとファイルストレージを](../Page/仮想記憶.md "wikilink") 1つのサブシステムに統合し、システムとそのリソースを管理するためにマネージャ/カーネルアーキテクチャを採用した。設計者は、[非プリエンプティブなマルチタスクモデルを検討したが](https://ja.wikipedia.org/wiki/ノンプリエンプティブ "wikilink")、後に[モニタに基づいて](../Page/モニタ_\(同期\).md "wikilink")[プリエンプティブ](https://ja.wikipedia.org/wiki/プリエンプティブ "wikilink") (ブロックされるまで実行する) システムを選択した\[2\]。Pilotには、ディスクに書き込まれたオペレーティングシステムのフリーズしたスナップショットをデバッグできるデバッガ、Co-Pilotが含まれていた。   

典型的な Pilot ワークステーションでは、3つの異なるディスクボリューム上で 3つのオペレーティングシステムを同時に実行していた。Co-Co-Pilot (メインのオペレーティングシステムがクラッシュした場合のバックアップデバッガ)、Co-Pilot (メインのオペレーティングシステムで、Co-Co-Pilot の下で実行され、プログラムのコンパイルとバインドに使用される)、そして 3番目のディスクボリューム上で実行されている Pilotの下位のコピーで、起動してテストプログラムを実行できる (メインの開発環境がクラッシュする可能性がある）。デバッガは、別のディスクボリュームに格納されたプログラムの変数を読み書きするために作成されたた。

このアーキテクチャは、開発者が下位ディスクボリュームに格納されたセマフォロック付きのオペレーティングシステムコードをシングルステップで実行できるというユニークなものである。しかし、Dシリーズの Xerox プロセッサのメモリとソースコードが大きくなるにつれて、オペレーティングシステムのチェックポイントと復元 (「ワールドスワップ」と呼ばれる) にかかる時間が非常に長くなった。下位のオペレーティングシステム環境でたった 1行のコードを実行するのに 60～120 秒かかることもあった。最終的には、Co-Pilot に代わる共存デバッガが開発された\[3\]。

Pilot は [Xerox Star](../Page/Xerox_Star.md "wikilink") ワークステーションのオペレーティングシステムとして使用された。

## 参照項目

  - オペレーティングシステムのタイムライン

## 参考文献

## 詳細な文献

  - Horsley, T.R., and Lynch, W.C. Pilot: A software engineering case history. In Proc. 4th Int. Conf. Software Engineering, Munich, Germany, Sept. 1979, pp. 94-99.

## 外部リンク

  - [Pilot: An Operating System for a Personal Computer](http://www.mcjones.org/paul/pilot/pilot.html)

[Category:1981年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1981年のソフトウェア "wikilink") [Category:ゼロックス](https://ja.wikipedia.org/wiki/Category:ゼロックス "wikilink") [Category:プロプライエタリOS](https://ja.wikipedia.org/wiki/Category:プロプライエタリOS "wikilink") [Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink")

1.
2.
3.