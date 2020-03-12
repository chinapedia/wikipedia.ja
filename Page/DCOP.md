> この記事は[DCOP](https://ja.wikipedia.org/wiki/DCOP)から翻訳されています。


**DCOP** (**D**esktop **CO**mmunication **P**rotocol'') とは、プロセス間または[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")間の軽量な[プロセス間通信](../Page/プロセス間通信.md "wikilink")システムである。このシステムの主眼は、[アプリケーション群が相互にやり取りして](../Page/アプリケーションソフトウェア.md "wikilink")、全体として複雑なタスクを実施できるようにすることである。基本的にDCOPは「遠隔制御」システムであり、あるアプリケーションやスクリプトから他のアプリケーションの助けを得ることを可能にする。[X Window Systemのクライアント間通信プロトコルをベースとして構築されている](../Page/X_Window_System.md "wikilink")。

DCOPを使うことで、新たなアプリケーションを一から書かなくとも新機能を実現できるようになる。[KDE](../Page/KDE.md "wikilink")のアプリケーションと[ライブラリ](../Page/ライブラリ.md "wikilink")はDCOPを多用しており、多くのKDEアプリケーションはDCOPの機構を通して[スクリプトから制御できる](../Page/スクリプト言語.md "wikilink")。

最近のKDEシステムでは、全てのKDEアプリケーションが基本的なDCOPインタフェースを備えており、これはそのアプリケーションの作者が明示的にDCOPを使用していない場合でもそのようになっている。例えば、全てのアプリケーションが "quit" コマンドによるアプリケーションのクローズを自動的にサポートしている。

DCOPを組み込んだアプリケーションと[シェル](../Page/シェル.md "wikilink")から通信するコマンド行ツールとして 'dcop'（小文字である点に注意）がある。また、同じ[インタフェースを提供する](../Page/インタフェース_\(情報技術\).md "wikilink")[GUIツールとして](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") 'kdcop' がある。

例えば、KDEデスクトップには一定時間間隔で背景の壁紙を切り換える機能がある。しかし、今の壁紙が気に入らないとき、それを即座に簡単に切り換えることはできない。また、ある壁紙を実際に見てみて、今後表示されないようにしたいと思った場合も、簡単に削除する方法はない。

しかし、dcopを使えば、そのような操作が簡単に追加できる。次のコマンド

` dcop kdesktop KBackgroundIface changeWallpaper`

は、シェルから壁紙を次に切り換えさせるものである。そして、次のコマンド

` dcop kdesktop KBackgroundIface currentWallpaper 1`

は、デスクトップ 1 の現在の壁紙のファイル名を得ることができる（KDEを含むXのデスクトップ環境では、[仮想デスクトップ](../Page/仮想デスクトップ.md "wikilink")を複数サポートしているのが一般的である）。これらを組み合わせてシェルスクリプトを組めば、壁紙を切り換えて、前に表示していた壁紙を削除することができる。例えば、次のようになる。

``  OLDWALLPAPER=`dcop kdesktop KBackgroundIface currentWallpaper 1` ``
` dcop kdesktop KBackgroundIface changeWallpaper`
` rm "$OLDWALLPAPER"`

このようにDCOPによって、アプリケーションが本来持っていなかった機能を簡単に追加することが可能となる。

## DCOPモデル

モデルは単純である。DCOPを使っているアプリケーションは全てクライアントである。クライアントはDCOPサーバを通して相互に通信する。DCOPサーバは一種の交通管制を行い、メッセージや呼び出しが適切な送信先に届くようにする。全てのクライアントは同列に扱われる。

DCOPでは2種類のアクションが可能である。"send and forget" メッセージは送信するだけで、ブロックされない。"calls" はデータが返されるのを待つ。

送信データは、[Qt](../Page/Qt.md "wikilink")の全てのクラスに備わっているQDataStreamオペレータを使って[シリアライズ](../Page/シリアライズ.md "wikilink")される。これは高速で単純であり、マーシャリングのためのコードを書くのも簡単である。さらに[IDL風のコンパイラがあり](../Page/インタフェース記述言語.md "wikilink")（dcopidlと dcopidl2cpp）、スタブとスケルトンを生成できる。dcopidlコンパイラを使うと、データ型を間違えないという利点もある。

[D-Bus](../Page/D-Bus.md "wikilink")は [freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink") が標準化したメッセージバスシステムであり、DCOPから強い影響を受けている。KDEの次のバージョンである KDE4では、DCOPが[D-Bus](../Page/D-Bus.md "wikilink")に置き換えられる予定である。

## 外部リンク

  - [DCOP Documentation](http://api.kde.org/3.5-api/kdelibs-apidocs/dcop/html/index.html)
  - [Tutorial for creating a DCOP Interface](http://developer.kde.org/documentation/tutorials/dot/dcopiface/dcop-interface.html)

[Category:OSのプロセス管理](https://ja.wikipedia.org/wiki/Category:OSのプロセス管理 "wikilink") [Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink")