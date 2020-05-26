> この記事は[Parallel Virtual Machine](https://ja.wikipedia.org/wiki/Parallel_Virtual_Machine)から翻訳されています。


**Parallel Virtual Machine**（パラレル・バーチャル・マシン、仮想並列計算機、略称：**PVM**）は[並列計算を行うための](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。

## 特徴

PVMは、[アメリカの](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[オークリッジ国立研究所](../Page/オークリッジ国立研究所.md "wikilink")のメンバーを中心に開発された。動作するマシンの種類が多いこと（[Linux](../Page/Linux.md "wikilink")、[BSD](../Page/BSD.md "wikilink")、[Windowsで動作可能](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")）や、入手方法が容易であるため、研究機関などで広く利用されている。

PVMをインストールすると、ネットワークに接続された複数台のコンピュータを、単一の計算機として利用できるようになる。このことにより、複数台のマシンが持つ計算パワーを、1つの大規模計算問題に結集して処理を行うことができる。

PVMソフトウェアシステムの構成は、大きく2つに分けられる。1つはデーモン、もう1つはルーチンライブラリである。

  - pvmd3（pvmd）
    この[デーモンは](../Page/デーモン_\(ソフトウェア\).md "wikilink")、一度起動するとバーチャルマシンを構成する全コンピュータ上に常駐する。使用者は、ログインさえできればどんなコンピュータにもこのデーモンのインストールが可能である。PVMを利用したアプリケーションを実行する場合に、まずバーチャルマシンを構成しているコンピュータのうちのどれか1台のマシンからpvmd3を起動する。 pvmd3は独自のシェルスクリプトのようなものを持ち、ここからマシンを構成するコンピュータのpvmd3を起動する。全てのpvmd3を起動した後、どれか一つのコンピュータに表示されたUNIXプロンプトに対して特定のコマンドを入力することにより、 PVMアプリケーションを実行できる。複数のユーザは、 互いにコンピュータをオーバーラップさせてバーチャルマシンを構成でき、 また、 各ユーザは一人で複数のPVMアプリケーションを同時に実行することも可能である。
  - libpvm3.a
    PVMインターフェースを利用するためのルーチンのライブラリである。このライブラリは、メッセージパッシング、プロセスの生成、タスクの協調などの必要な関数を提供する。PVMを利用したアプリケーションを実行する場合には、アプリケーションプログラムとこのライブラリをリンクする必要がある。

## 関連項目

  - [並列化](../Page/並列化.md "wikilink")
  - [並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")
  - [コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")

[Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:並行計算](https://ja.wikipedia.org/wiki/Category:並行計算 "wikilink")