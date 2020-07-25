> この記事は[DragonFly BSD](https://ja.wikipedia.org/wiki/DragonFly_BSD)から翻訳されています。


**DragonFly BSD**(ドラゴンフライ ビーエスディー)は、[NetBSD](../Page/NetBSD.md "wikilink")や[FreeBSD](../Page/FreeBSD.md "wikilink")と同じく[BSDの子孫](../Page/BSDの子孫.md "wikilink")の1つの、[UNIXライクな](../Page/Unix系.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。

が[プロジェクト](../Page/プロジェクト.md "wikilink")[リーダー](https://ja.wikipedia.org/wiki/リーダー "wikilink")となり、[2003年](../Page/2003年.md "wikilink")にFreeBSD 4.8-STABLEから[分岐する形で](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")[開発](../Page/開発.md "wikilink")が始まり、[2004年](../Page/2004年.md "wikilink")[7月12日](../Page/7月12日.md "wikilink")に初のメジャー[バージョン](https://ja.wikipedia.org/wiki/バージョン "wikilink")である**DragonFly BSD** 1.0が公開された\[1\]。

**DragonFly BSD**は、FreeBSD 4.xの[後継](https://ja.wikipedia.org/wiki/後継 "wikilink")というだけでなく、FreeBSD 5.xとも全く異なる[方針で開発されている](https://ja.wikipedia.org/wiki/針路 "wikilink")。この例として、[LWKTや軽量](https://ja.wikipedia.org/wiki/軽量カーネルスレッド "wikilink")[メッセージ](../Page/メッセージ_\(コンピュータ\).md "wikilink")[システム](../Page/システム.md "wikilink")が有る。このような多くの、**DragonFly BSD**に[実装](../Page/実装.md "wikilink")される[概念](../Page/概念.md "wikilink")は、[AmigaOS](../Page/AmigaOS.md "wikilink")に触発されている。

バージョン4.8からは、インストーラーで[UEFIがサポートされている](../Page/Unified_Extensible_Firmware_Interface.md "wikilink")\[2\]。

## カーネルの設計

**DragonFly BSD**には、最近の殆どの[カーネル](../Page/カーネル.md "wikilink")のように、[ハイブリッドカーネルが採用されている](https://ja.wikipedia.org/wiki/カーネル#ハイブリッドカーネル "wikilink")。つまり、これは、[モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink")と[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")の両方の性質を併せ持ち、必要に応じて両方の[メリット](../Page/メリット.md "wikilink")を使うということである。例えば、マイクロカーネルの[メッセージ](../Page/メッセージ_\(コンピュータ\).md "wikilink")[システム](../Page/システム.md "wikilink")にあるような[メモリ保護](../Page/メモリ保護.md "wikilink")の[恩恵を受けるのと同時に](https://ja.wikipedia.org/wiki/恩寵 "wikilink")、モノリシックカーネルにあるような[処理速度は残っている](../Page/スループット.md "wikilink")。メッセージサブシステムは、[Mach](../Page/Mach.md "wikilink")のようなマイクロカーネルの[デザインと似て](../Page/設計.md "wikilink")、余り複雑ではないものになっている。さらに、これは[同期](../Page/同期_\(計算機科学\).md "wikilink")[通信](../Page/通信.md "wikilink")と非同期通信の両方に対応しており、[状況](https://ja.wikipedia.org/wiki/状況 "wikilink")に応じて最良の[性能](https://ja.wikipedia.org/wiki/性能 "wikilink")を出せるようになっている。

[デバイス](https://ja.wikipedia.org/wiki/デバイス "wikilink")[I/Oや](../Page/入出力.md "wikilink")[仮想ファイルシステム](../Page/仮想ファイルシステム.md "wikilink") (VFS) はメッセージサブシステムを使うように変更されている。これらの新しい[機構](https://ja.wikipedia.org/wiki/機構 "wikilink")に拠り、[カーネル](../Page/カーネル.md "wikilink")の様々な部分を[ユーザーランドで実行可能になる](../Page/アドレス空間.md "wikilink")。[ユーザーランドでカーネルの一部を実行すると](../Page/オペレーティングシステム.md "wikilink")、その部分はカーネルという大きなプログラムの一部ではなく、小さく[独立](../Page/独立.md "wikilink")した1つのプログラムとなる。こうすることで、ユーザーランドで動いている[ドライバーが](../Page/デバイスドライバ.md "wikilink")[クラッシュしても](https://ja.wikipedia.org/wiki/クラッシュ_\(コンピュータ\) "wikilink")、カーネル全体はクラッシュしなくなるという[利点も有る](../Page/メリット.md "wikilink")。

[システムコール](../Page/システムコール.md "wikilink")はユーザーランド版とカーネルランド版に分けられ、メッセージとして[カプセル化](../Page/カプセル化.md "wikilink")されるようになった。これに拠って、[標準](../Page/標準化.md "wikilink")[システムコール](../Page/システムコール.md "wikilink")の実体をユーザーランドにある[互換レイヤー](../Page/互換レイヤー.md "wikilink")に移すときの[プログラム量と複雑さを軽減可能になると同時に](../Page/プログラム_\(コンピュータ\).md "wikilink")、新旧の**DragonFly BSD**の[互換性](../Page/互換性.md "wikilink")を保ち易くなった。さらに、[Linux](../Page/Linux.md "wikilink")やその他の[UNIX](../Page/UNIX.md "wikilink")系[OSの](../Page/オペレーティングシステム.md "wikilink")[アプリケーションを動かすための](../Page/アプリケーションソフトウェア.md "wikilink")[機構](https://ja.wikipedia.org/wiki/機構 "wikilink")もユーザーランドに移せる。このような[FreeBSD jail上に作られたネイティブな](../Page/FreeBSD_jail.md "wikilink")[ユーザーランド](../Page/オペレーティングシステム.md "wikilink")[互換](../Page/互換性.md "wikilink")[レイヤーを使うことで](../Page/階層構造.md "wikilink")、[UMLと同等のことができる](https://ja.wikipedia.org/wiki/User-Mode_Linux "wikilink")。しかし、UMLと異なり、[仮想化](../Page/仮想化.md "wikilink")には実際の[ハードウェア](../Page/ハードウェア.md "wikilink")と通信するための特別な[ドライバーを必要としない](../Page/デバイスドライバ.md "wikilink")。なお、UMLはLinuxを[ポーティングしたもので](../Page/移植_\(ソフトウェア\).md "wikilink")、ホスト[OSのカーネルを別の](../Page/オペレーティングシステム.md "wikilink")[ハードウェア](../Page/ハードウェア.md "wikilink")[プラットフォームと見なす](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[実装](../Page/実装.md "wikilink")になっている。

### CPU局所化

[スレッドは](../Page/スレッド_\(コンピュータ\).md "wikilink")[CPU](../Page/CPU.md "wikilink")に強く結び付けられるという[デザインになっていて](../Page/設計.md "wikilink")、各々のCPUはそれぞれ[LWKT](https://ja.wikipedia.org/wiki/軽量カーネルスレッド "wikilink")[スケジューラーを持っている](../Page/スケジューリング.md "wikilink")。なお、スレッドが勝手に動作する[プロセッサ](../Page/プロセッサ.md "wikilink")ーを変えることはできず、[IPI](https://ja.wikipedia.org/wiki/プロセッサ間割り込み "wikilink")[メッセージを使った場合のみ別のCPUへとスレッドが移される](../Page/メッセージ_\(コンピュータ\).md "wikilink")。そして、CPUを跨ぐスレッド[スケジューリング](../Page/スケジューリング.md "wikilink")も非[同期のIPIメッセージを送ることで行われる](../Page/同期_\(計算機科学\).md "wikilink")。この[方法を使うと](../Page/方法論.md "wikilink")、スレッドサブ[システム](../Page/システム.md "wikilink")を綺麗に区切れるが、その[利点は](../Page/メリット.md "wikilink")、[SMPシステムにて複数のCPUの](../Page/対称型マルチプロセッシング.md "wikilink")[キャッシュに同一](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")[データが乗らない](https://ja.wikipedia.org/wiki/データ#電子データ "wikilink")、ということである。これに拠り、システムの各プロセッサーがスレッドの実行のために異なったデータをキャッシュできるようになり、高い[性能](https://ja.wikipedia.org/wiki/性能 "wikilink")を出せる。

LWKTサブシステムでは複数のカーネルスレッドに[処理を分けるように](../Page/コンピューティング.md "wikilink")[実装](../Page/実装.md "wikilink")された\[3\]。これに拠り、複数の[カーネル](../Page/カーネル.md "wikilink")内[タスク](https://ja.wikipedia.org/wiki/タスク "wikilink")で[リソースを](../Page/計算資源.md "wikilink")[共有](../Page/共有.md "wikilink")することで生じる[競合状態を無くせる](https://ja.wikipedia.org/wiki/リソース競合 "wikilink")。このようにCPU毎の[局所性](https://ja.wikipedia.org/wiki/局所性 "wikilink")を保つようにする[アルゴリズム](../Page/アルゴリズム.md "wikilink")でスレッドを分ける[実装](../Page/実装.md "wikilink")は略間違い無く**DragonFly BSD**に特有の[デザインである](../Page/設計.md "wikilink")。

### 共有資源の保護

[共有](../Page/共有.md "wikilink")[資源](../Page/計算資源.md "wikilink")([ファイルや](../Page/ファイル_\(コンピュータ\).md "wikilink")[データ](https://ja.wikipedia.org/wiki/データ#電子データ "wikilink")[構造体](../Page/構造体.md "wikilink")など)への[アクセス](../Page/アクセス.md "wikilink")は、[マルチプロセッサー](../Page/マルチプロセッシング.md "wikilink")[マシーン](https://ja.wikipedia.org/wiki/マシーン "wikilink")で[安全](../Page/安全.md "wikilink")に動作させるためには、[直列化されなくてはならない](../Page/シリアライズ.md "wikilink")。こうすることで、[スレッドや](../Page/スレッド_\(コンピュータ\).md "wikilink")[プロセス](../Page/プロセス.md "wikilink")は同時に同じ[資源を変更できなくなる](../Page/計算資源.md "wikilink")。[アトミック操作](../Page/不可分操作.md "wikilink")・[スピンロック](../Page/スピンロック.md "wikilink")・[クリティカルセクション](../Page/クリティカルセクション.md "wikilink")・[ミューテックス](../Page/ミューテックス.md "wikilink")・[直列化](../Page/シリアライズ.md "wikilink")[トークン](https://ja.wikipedia.org/wiki/字句解析#トークン "wikilink")・[メッセージ](../Page/メッセージ_\(コンピュータ\).md "wikilink")[キューは全て同じ](../Page/キュー_\(コンピュータ\).md "wikilink")[資源への同時アクセスを防ぐのに使える](../Page/計算資源.md "wikilink")[方法である](../Page/方法論.md "wikilink")。[Linux](../Page/Linux.md "wikilink")も[FreeBSD](../Page/FreeBSD.md "wikilink") 5.xも粒度の細かい[ミューテックス](../Page/ミューテックス.md "wikilink")を使った[モデルを用いることでより高](../Page/プロセスモデル.md "wikilink")[性能](https://ja.wikipedia.org/wiki/性能 "wikilink")なマルチプロセッサー[システム](../Page/システム.md "wikilink")を構成しているが、**DragonFly BSD**はそうではなく、複数のスレッドが[共有](../Page/共有.md "wikilink")[リソースに同時にアクセスしたり変更したりするのを防ぐために](../Page/計算資源.md "wikilink")、[クリティカルセクション](../Page/クリティカルセクション.md "wikilink")と[直列化](../Page/シリアライズ.md "wikilink")[トークンを用いている](https://ja.wikipedia.org/wiki/字句解析#トークン "wikilink")。最近まで、**DragonFly BSD**も[SPLを使っていたが](https://ja.wikipedia.org/wiki/SPL_\(オペレーティングシステム\) "wikilink")、その部分は[クリティカルセクション](../Page/クリティカルセクション.md "wikilink")で置き換えられた。

[LWKTサブ](https://ja.wikipedia.org/wiki/軽量カーネルスレッド "wikilink")[システム](../Page/システム.md "wikilink")・[IPIメッセージサブシステム](https://ja.wikipedia.org/wiki/プロセッサ間割り込み "wikilink")・新しい[メモリアロケーター](https://ja.wikipedia.org/wiki/メモリアロケーター "wikilink")などを含むシステムの中心的な部分の多くは[ロックしない](../Page/ロック_\(情報工学\).md "wikilink")。つまり、[ミューテックス](../Page/ミューテックス.md "wikilink")無しで動き、[CPU](../Page/CPU.md "wikilink")毎に[処理を行う](../Page/コンピューティング.md "wikilink")。[クリティカルセクション](../Page/クリティカルセクション.md "wikilink")は[局所的な](https://ja.wikipedia.org/wiki/局所性 "wikilink")[割り込みから守るために使われ](../Page/割り込み_\(コンピュータ\).md "wikilink")、CPU毎に処理を行う。これに拠り、動かされているスレッドはCPUを横取りされないことが[保証](../Page/保証.md "wikilink")されている。

直列化トークンは他のCPUからの[並列アクセスを防ぐために使われ](../Page/並列化.md "wikilink")、複数のスレッドで同時に保持される。この[結果](https://ja.wikipedia.org/wiki/結果 "wikilink")、それらのスレッドの一つが与えられた[時間](../Page/時間.md "wikilink")に処理を行うことが[保証](../Page/保証.md "wikilink")される。それゆえ、ミューテックスを持っているスレッドと違い、ブロックされていたり[スリープしているスレッドは他のスレッドが共有リソースにアクセスすることを](https://ja.wikipedia.org/wiki/スリープ_\(コンピュータ\) "wikilink")[禁止](https://ja.wikipedia.org/wiki/禁止 "wikilink")しない。直列化トークンを使うことで、ミューテックスを使った場合のような[デッドロック](../Page/デッドロック.md "wikilink")や[優先度の逆転](https://ja.wikipedia.org/wiki/優先度の逆転 "wikilink")を引き起こす[状況](https://ja.wikipedia.org/wiki/状況 "wikilink")を防げる。これに加え、複数のスレッドで共有するような[リソースを要求する長い](../Page/計算資源.md "wikilink")[プロシージャ](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")ーの[設計](../Page/設計.md "wikilink")や[実装](../Page/実装.md "wikilink")をずっと単純にできる。直列化トークンの実装は最近のLinuxにある[RCUによく似たものに発展しているが](../Page/リード・コピー・アップデート.md "wikilink")、[計算機](../Page/計算機.md "wikilink")内の全ての[プロセッサ](../Page/プロセッサ.md "wikilink")ーではなく同じトークンで[競合しているプロセッサー同士が影響を受ける](../Page/競合状態.md "wikilink")、という実装になっている。

### その他

[開発](../Page/開発.md "wikilink")の初期段階では、[スラブアロケータ](https://ja.wikipedia.org/wiki/スラブアロケータ "wikilink")ーが採用され、[FreeBSD](../Page/FreeBSD.md "wikilink") 4.xの[カーネル](../Page/カーネル.md "wikilink")[メモリアロケーター](https://ja.wikipedia.org/wiki/メモリアロケーター "wikilink")から置き換えられた。これは[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")を割り当てるときに[排他制御](../Page/排他制御.md "wikilink")やブロック操作を必要とせず、[MPSAFEである](https://ja.wikipedia.org/wiki/マルチプロセッサーセイフ "wikilink")。

[SFBUF](https://ja.wikipedia.org/wiki/SFBUF "wikilink") \[4\]と[MSFBUF](https://ja.wikipedia.org/wiki/MSFBUF "wikilink") が使われている。SFBUFは短い[時間](../Page/時間.md "wikilink")しか使わない単一ページの[マッピング](https://ja.wikipedia.org/wiki/マッピング "wikilink")を操作するのに用い、必要ならそれらのマッピングを[キャッシュする](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。これらの[機構](https://ja.wikipedia.org/wiki/機構 "wikilink")は単一の[VM](../Page/仮想機械.md "wikilink")[ページで保持されている](../Page/ページング方式.md "wikilink")[データへの](https://ja.wikipedia.org/wiki/データ#電子データ "wikilink")[参照を補うために使われる](../Page/参照_\(情報工学\).md "wikilink")。この単純で強力な[抽象化に拠って様々なことが可能になる](../Page/抽象化_\(計算機科学\).md "wikilink")。例えば、sendfile(2)\[5\]での[ゼロ](../Page/0.md "wikilink")[コピーが実現されている](https://ja.wikipedia.org/wiki/Digital_copy "wikilink")。

SFBUFは[カーネル](../Page/カーネル.md "wikilink")の様々な箇所で用いられる。例えば、[vnode](https://ja.wikipedia.org/wiki/vnode "wikilink")[オブジェクトの](../Page/オブジェクト_\(プログラミング\).md "wikilink")[ページャ](https://ja.wikipedia.org/wiki/ページャ "wikilink")ーや[パイプサブ](../Page/パイプ_\(コンピュータ\).md "wikilink")[システム](../Page/システム.md "wikilink")([XIO](https://ja.wikipedia.org/wiki/XIO "wikilink")\[6\]を用いた間接[転送の場合](https://ja.wikipedia.org/wiki/データ転送 "wikilink"))で広[帯域な転送を行うために用いられる](../Page/デバイス帯域幅の一覧.md "wikilink")。SFBUFは単一のVMページでしか使えないために、[MSFBUFS](https://ja.wikipedia.org/wiki/MSFBUFS "wikilink")が短い時間しか使わない複数のページのマッピングを操作するのに用いられる。

SFBUFの[概念](../Page/概念.md "wikilink")はのがsendfile(2)\[7\]を書いたときに考案された。そして、この[概念](../Page/概念.md "wikilink")はとによって書き直された。また、[MSFBUF](https://ja.wikipedia.org/wiki/MSFBUF "wikilink")はとにより考案された。

## 開発の方向性

### 対応プロセッサー

**DragonFly BSD**は、現在では、[x86-64](https://ja.wikipedia.org/wiki/x64 "wikilink")[アーキテクチャーベースの](../Page/コンピュータ・アーキテクチャ.md "wikilink")[計算機](../Page/計算機.md "wikilink")（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")と[AMD](https://ja.wikipedia.org/wiki/AMD "wikilink")）で動作する（32ビットへの対応は、3.8 を最後に打ち切られた\[8\]）。これは単一[プロセッサ](../Page/プロセッサ.md "wikilink")ーも[SMPも両方対応している](../Page/対称型マルチプロセッシング.md "wikilink")。

### パッケージ管理

初期の**DragonFly BSD**では、[FreeBSD](../Page/FreeBSD.md "wikilink")の[ports](https://ja.wikipedia.org/wiki/ports "wikilink")を[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")として使っており、[NetBSD](../Page/NetBSD.md "wikilink")の[pkgsrc](https://ja.wikipedia.org/wiki/pkgsrc "wikilink")は[オプション](https://ja.wikipedia.org/wiki/オプション "wikilink")として使えるに過ぎなかった。しかし、**DragonFly BSD** 1.4から[pkgsrc](https://ja.wikipedia.org/wiki/pkgsrc "wikilink")が[システム](../Page/システム.md "wikilink")の公式な[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")となった\[9\]。これで、[開発](../Page/開発.md "wikilink")者は追加で[インストール](../Page/インストール.md "wikilink")される[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[アップデート](https://ja.wikipedia.org/wiki/アップデート "wikilink")作業から解放されることになった。また、この変更はpkgsrcの開発者が[pkgsrc](https://ja.wikipedia.org/wiki/pkgsrc "wikilink")の[移植性](../Page/移植性.md "wikilink")を高めるのにも役立った。

**DragonFly BSD** 3.4より、新たな[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")として[DPorts](https://ja.wikipedia.org/wiki/DPorts "wikilink")が導入された\[10\]。DPortsはFreeBSDのportsを**DragonFly BSD**で使用できるようにする仕組みであるが、pkgsrcとDPortsを同時には使えない。

### スレッドとメッセージング

[システムコール](../Page/システムコール.md "wikilink")と[デバイス](https://ja.wikipedia.org/wiki/デバイス "wikilink")[I/Oの](../Page/入出力.md "wikilink")[実装](../Page/実装.md "wikilink")は**DragonFly BSD**の[スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")[メッセージング](../Page/メッセージ_\(コンピュータ\).md "wikilink")[システム](../Page/システム.md "wikilink")を使うように変更されたが、これらは未だに[同期して動作している](../Page/同期_\(計算機科学\).md "wikilink")。最終的には、全てのメッセージサブシステムを同期又は非同期のどちらでも動作するようにする予定である。

[ユーザーランドスレッドの](../Page/オペレーティングシステム.md "wikilink")[サポートも今後のリリースの重要な課題である](../Page/サービス.md "wikilink")。**DragonFly BSD**では、今のところ、N:1スレッドしか持っていない。これについては、[開発](../Page/開発.md "wikilink")当初から取り組んでおり、 [近代](../Page/近代.md "wikilink")的な[スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")[実装](../Page/実装.md "wikilink")になる予定である\[11\]。

### ファイルシステム

**DragonFly BSD** 2.0より、[ファイルシステム](../Page/ファイルシステム.md "wikilink")として、[HAMMER](https://ja.wikipedia.org/wiki/HAMMER "wikilink")\[12\]を採用している。

HAMMERの[後継](https://ja.wikipedia.org/wiki/後継 "wikilink")として、HAMMER2の[開発](../Page/開発.md "wikilink")がによって主導され、**DragonFly BSD** 5.0より実験的にサポートされ、**DragonFly BSD** 5.2より公式にサポートされる。

### その他

  - [devfs](https://ja.wikipedia.org/wiki/devfs "wikilink")が[Google Summer of Code](https://ja.wikipedia.org/wiki/Google_Summer_of_Code "wikilink") 2009の[プロジェクト](../Page/プロジェクト.md "wikilink")として[実装](../Page/実装.md "wikilink")された。
  - [PUFFSが](https://ja.wikipedia.org/wiki/Pass-to-Userspace_Framework_File_System "wikilink")[NetBSD](../Page/NetBSD.md "wikilink")から[移植された](../Page/移植_\(ソフトウェア\).md "wikilink")。
  - [USB4BSD](https://ja.wikipedia.org/wiki/USB4BSD "wikilink")が[FreeBSD](../Page/FreeBSD.md "wikilink")から移植された。
  - バージョン4.0.1より、i386アーキテクチャ（32ビット版x86）のサポートが廃止されてx86_64版のみがサポートされることとなった\[13\]。

## 開発と配布

[FreeBSD](../Page/FreeBSD.md "wikilink")と[OpenBSD](../Page/OpenBSD.md "wikilink")と同様に、DragonFly BSDの開発者は[関数プロトタイプ](../Page/関数プロトタイプ.md "wikilink")スタイルの[Cのコードを](../Page/C言語.md "wikilink")、より現代的で[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")準拠のものに少しずつ置き換えている。他のOSと同様に、DragonFlyのバージョンの[GCC](https://ja.wikipedia.org/wiki/GCC "wikilink")は、Stack-Smashing Protecterがデフォルトで有効になっており、バッファ・オーバーフローに基づいた攻撃に対する追加的な保護を提供している。ただし、[2005年](../Page/2005年.md "wikilink")[7月23日](../Page/7月23日.md "wikilink")からは、この保護付きのカーネルのビルドはデフォルトではない\[14\]。

FreeBSDの派生物として、DragonFlyは、簡単に使うことができる統合されたビルドシステムを持ち、このシステムは、ベースシステムの全体をソースコードから少ないコマンドでリビルドすることができる。DragonFlyの開発者たちは、[Git](../Page/Git.md "wikilink")をDragonFlyのソースコードを管理するために使っている。また、FreeBSDとは違って、Dragonflyは、安定版と非安定版のリリースの両方をひとつのソースツリーに持っており、これはより小さな開発ベースによるものである\[15\]。

### 配布メディア

OSは、[Live CDとLive](../Page/Live_CD.md "wikilink") USB（完全な[X11](https://ja.wikipedia.org/wiki/X11 "wikilink")フレーバーが利用可能）として配布され、これは完全なDragonFlyのシステムにブート可能である\[16\]。また、このメディアは、マニュアルページの完全なセットとソースコード、将来のバージョンで有用なパッケージとベースシステムを含んでいる。このことの優位点は、単一のCDで、ソフトウェアをコンピュータにインストールすることができ、フルセットのツールをダメージを受けたシステムの修復に利用することができ、システムの能力をインストールなしでデモンストレートすることができることである。デイリースナップショットは、マスターサイトから利用することができ、これは最も最近のバージョンのDragonFlyをソースからのビルドなしで利用したいと考えているユーザーに向いている。

DragonFlyは、他のオープンソースのBSDと同様に、現代のバージョンの[BSDライセンス](../Page/BSDライセンス.md "wikilink")の下で配布されている。

## 注釈・出典

## 関連項目

  - [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")
  - [カーネル](../Page/カーネル.md "wikilink")
      - [モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink")
      - [マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")
  - [スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")
      - [軽量カーネルスレッド](https://ja.wikipedia.org/wiki/軽量カーネルスレッド "wikilink")
  - [UNIX](../Page/UNIX.md "wikilink")
      - [UNIXライク](../Page/Unix系.md "wikilink")
  - [Linux](../Page/Linux.md "wikilink")
  - [BSD](../Page/BSD.md "wikilink")
      - [BSDの子孫](../Page/BSDの子孫.md "wikilink")
          - [FreeBSD](../Page/FreeBSD.md "wikilink")
  - [オープンソース](../Page/オープンソース.md "wikilink")

## 外部リンク

  -
  - [Leaf - DragonFly BSD Developer Resources](http://leaf.dragonflybsd.org/index.html)

  - [DragonFly BSD Mailing List Archives](http://lists.dragonflybsd.org/index.html)

  - [DragonFlyBSD bugtracker](http://bugs.dragonflybsd.org/projects/)

  - [gitweb.dragonflybsd.org Git](http://gitweb.dragonflybsd.org/projects.git)

  - [avalon.dragonflybsd.org](http://avalon.dragonflybsd.org/index.html)

<!-- end list -->

  - [GitHub · Build software better, together.](https://github.com/home)

<!-- end list -->

  -   - [DragonFly BSD](https://github.com/DragonFlyBSD)

  - [FreeBSD and Linux Kernel Cross-Reference](http://fxr.watson.org/index.html)

      - [DFBSD](http://fxr.watson.org/fxr/source?v=DFBSD)

[Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:LiveCD](https://ja.wikipedia.org/wiki/Category:LiveCD "wikilink") [Category:2004年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2004年のソフトウェア "wikilink")

1.
2.
3.  例えば、[ネットワークコード](https://ja.wikipedia.org/wiki/ネットワークコード "wikilink")では、[プロトコル](../Page/プロトコル.md "wikilink")毎に1スレッドとなる。
4.
5.
6.
7.
8.  <https://www.dragonflybsd.org/docs/faq/FAQ-English/>
9.
10.
11. によれば、理想的にはM:Nスレッドの実装をしたい 、とのことである。
12.
13.
14.
15.
16.