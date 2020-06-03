> この記事は[Control-Alt-Delete](https://ja.wikipedia.org/wiki/Control-Alt-Delete)から翻訳されています。


[thumbキーボードにおける](https://ja.wikipedia.org/wiki/ファイル:Three-finger_salute.svg "wikilink") -- の位置\]\]

**Control-Alt-Delete** または **Ctrl-Alt-Del**（コントロール・オルト・デリート）とは、[コンピュータキーボードの](../Page/キーボード_\(コンピュータ\).md "wikilink")[コマンドの一つで](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")、[コンピュータ](../Page/コンピュータ.md "wikilink")を[再起動](../Page/再起動.md "wikilink")するときや、最近のほとんどのバージョンの[Microsoft WindowsでWindowsのセキュリティや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[タスクマネージャを呼び出すときに使用される](https://ja.wikipedia.org/wiki/Windows_タスク_マネージャー "wikilink")。[コントロールキー](../Page/コントロールキー.md "wikilink")（Ctrlキー）と[Altキー](https://ja.wikipedia.org/wiki/Altキー "wikilink")を押しながら、[削除キー](https://ja.wikipedia.org/wiki/削除キー "wikilink")（Delキー）を押すことで実行される。

日本では[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")の普及もあり、Alt を GRPH （[グラフキー](https://ja.wikipedia.org/wiki/グラフキー "wikilink")）に置き換えた、**CTRL-GRPH-DEL** という表現もされた。

## 起源

このキーストローク・コンビネーションは、オリジナルの[IBM PCを設計したデビッド](../Page/IBM_PC.md "wikilink")・ブラッドリーによって実装された。ブラッドリーは、コントロールキーとAltキーと[Escキー](https://ja.wikipedia.org/wiki/Escキー "wikilink")の組み合わせで[ソフトリブートが実行されるように設計していた](https://ja.wikipedia.org/wiki/ブート#ソフトリブート "wikilink")。 しかし、彼はキーボードの左側に手などをぶつけただけで簡単にこれらキーが同時に押されて、意図せずコンピュータが再起動してしまうことに気が付いた。そこで彼は、片手では同時に押せないよう、キーストローク・コンビネーションをコントロールキーとAltキーと削除キーに変更したのである（現在では[102キーボード](https://ja.wikipedia.org/wiki/102キーボード "wikilink")や[マルトロンキーボード](https://ja.wikipedia.org/wiki/マルトロンキーボード "wikilink")のような、片手でこれらキーを押すことができるものもある）。より進んだ[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")では、この状態を予約された組合せとして様々な目的に使用しているが、現在でも特定の環境や条件下ではソフトリブートが行われる。

ブラッドリーは、「私が Control-Alt-Delete を発明したかもしれない。しかし、[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")がそれを有名にした。」と語っている\[1\]。ゲイツ自身は、「あれは失敗だった」、「IBMのキーボード設計者がMicrosoftのためにそういう（再起動用の）ボタンを付けたがらなかった」と2013年に語っている\[2\]\[3\]。

## DOSやその他リアルモードで動作するシステム

[パソコン上で動作する](../Page/パーソナルコンピュータ.md "wikilink")[DOSやその他](../Page/DOS_\(OS\).md "wikilink")[リアルモード](../Page/リアルモード.md "wikilink")で動作するシステムは、キーストローク・コンビネーションは、[BIOS内のキーボード](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")・ハンドリング・コードによって認識され、[Intel 8086の](../Page/Intel_8086.md "wikilink")[NMI](../Page/割り込み_\(コンピュータ\).md "wikilink")(Non-Maskable Interrupt)シグナル（極一部の例外を除いてソフトリブートされる）として扱われる。

## Windows

### DOSベースのWindows

[Windows 3.0以前](../Page/Microsoft_Windows_3.x.md "wikilink")（スタンダードモードで起動されたWindows 3.1も含む）では、-- をするとMS-DOSと同様、再起動が行われる。386拡張モードで起動しているWindows 3.1、[Windows 95](../Page/Microsoft_Windows_95.md "wikilink")、[Windows 98](../Page/Microsoft_Windows_98.md "wikilink")、[Windows Meでは](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")、このキーボードストローク・コンビネーションは、Windowsキーボードデバイスドライバによって認識される。このとき、`system.ini` の `[386Enh]` の項の `LocalReboot` によって、Windowsは振る舞いを変える。

  - `LocalReboot=Off` - ソフトウェア処理による再起動（ソフトリブート）が実行される。
  - `LocalReboot=On`:
      - Windows 3.1は、[ブルースクリーン](../Page/ブルースクリーン.md "wikilink")を表示して、[エンターキー](https://ja.wikipedia.org/wiki/エンターキー "wikilink")を押して現在実行しているタスクを終了させるか、もう一度 -- を押してソフトリブートを実行するかを、ユーザーに選択させる。
      - Windows 95、Windows 98、Windows Meでは、現在実行中の[プロセス](../Page/プロセス.md "wikilink")の一覧を表示させ、これらプロセスを終了させ、応答がない場合は強制終了させることをユーザーに示す。もう一度 -- を押すと、ソフトリブートが実行される。

タスクやプロセスの強制終了は、例えばプログラムが[無限ループ](../Page/無限ループ.md "wikilink")に突入したときに役に立つ。理論的には、このキーストローク・コンビネーションを使用しても、ほかのプロセスは影響なく実行されなくてはならないが、Windows3.1ではリソースやメモリのリークが発生する。そのようなバージョンのWindowsでは、プロセスの強制終了後、直ちに他のアプリケーションのデータを保存し、再起動を行うことが強く推奨されている。そのようなダメージは、リソーストラッキングによって、新しいDOSベースWindowsではほとんど発生しない。

DOSベースWindowsで -- を二回押すと、たとえWindowsがプロセスリストを表示していなくてもソフトリブートが行われる。これは、-- の組合せに対する応答を定義できるユーザーレベルのプログラムがないため、全てのスタックしたプロセスを飛び越えることをユーザーに許可するためである。

### Windows NT

[Windows NTやその後継の](../Page/Microsoft_Windows_NT.md "wikilink")[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink")、[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、 [Windows 7](../Page/Microsoft_Windows_7.md "wikilink") 、[Windows Server 2008](../Page/Microsoft_Windows_Server_2008.md "wikilink")、[Windows 8](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")、[Windows Server 2012](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012 "wikilink")、[Windows 10では](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")、このキーストローク・コンビネーションは、[Winlogon](https://ja.wikipedia.org/wiki/Winlogon "wikilink")プロセスによって認識され、以下のうちいずれかの振る舞いをする。

  - 誰もログインしていない場合、ログイン画面を表示する。コンピュータのロックを解除する場合にも使う。
  - [NTドメイン](https://ja.wikipedia.org/wiki/NTドメイン "wikilink")または[Active Directoryのドメインに参加ないしは構成していたり](../Page/Active_Directory.md "wikilink")、Windows 2000が起動している場合、「Windowsのセキュリティ」のダイアログが表示され、ユーザーはコンピュータをロックしたり、パスワードを変更したり、ログアウトしたり、コンピュータをシャットダウンしたり、タスクマネージャを起動することができる。Windows VistaやWindows Server 2008では、それらのドメインを起動しているいないに関わらず、デフォルトの振る舞いである。提示されるオプションは、[グループポリシー](https://ja.wikipedia.org/wiki/グループポリシー "wikilink")を使用することによって制限できる。
  - Windows XPで、ドメインに接続していない場合、
      - ようこその画面で高速ユーザー切り替えが有効の場合、タスクマネージャを起動する。
      - ようこその画面で高速ユーザー切り替えが無効の場合、Windowsのセキュリティのダイアログが起動する。
  - Windows Vista以降の場合、
      - セキュリティオプションを起動する。

Windows NTのような構成では、何らかの方法でセキュリティを弱めない限り、Winlogonプロセスしかこのキーストローク・コンビネーションの通知を受け取ることができない。これは、カーネルがWinlogonプロセスの[プロセスID](https://ja.wikipedia.org/wiki/プロセスID "wikilink")を覚えていて、このプロセスにしか情報を通知しないからである。このようにこのキーストローク・コンビネーションはセキュア・アテンション・キーとなっている。Windows NTでは、これをセキュア・アテンション・シーケンスと呼ぶ。ユーザーは -- を押すことで、これが第三者のプログラムではなく、本当にオペレーティングシステムの表示しているものだと判断でき、安心してパスワードを入力することができる。Windowsでこの組合せがセキュア・アテンション・キーに選ばれたのは、PCプラットフォームでこの目的のためにキーストロークの組合せを変更する合理的理由がなかったためである\[4\]。

また、このキーストローク・コンビネーションはWindows Server 2003以降でタスクマネージャを呼び出す信頼のできる方法でもある。その他全てのキーストローク・コンビネーションはスタックしたプロセスに縛られる可能性があったが、ユーザープロセスが -- のシーケンスを妨害することはできない。しかし、これはWindowsグループポリシーで無効化できる。Windows NT 4.0以降の全てのNT系OSでは、-- の組合せがWindowsのセキュリティダイアログに割り当てられているときでも、-- のキーストローク・コンビネーションでタスクマネージャが起動できる。

副作用として、ユーザーが電源や電源スイッチ、リセットスイッチに触れる手段がない場合、以前は -- を使うことで再起動することができたが、現在は、グループポリシーの設定を行うことで一般ユーザーが勝手にコンピュータを再起動することができなくなった。

## OS/2

[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")では、このキーボードストローク・コンビネーションは、OS/2のキーボードデバイスドライバによって認識され、セッションマネージャプロセスに通知される。OS/2バージョン2以降の通常のセッションマネージャプロセスでは、親ワークプレイス・シェル・プロセスが *"The system is rebooting"* とウィンドウに表示して、ソフトリブートが行われる。このとき、もう一度 -- を押すと、セッションマネージャプロセスを待たずに直ちにソフトリブートが実行される。

いずれのケースでも、システムは[ページキャッシュ](https://ja.wikipedia.org/wiki/ページキャッシュ "wikilink")をフラッシュし、全てのディスクを綺麗にアンマウントする。しかし、全ての実行中のプロセスが綺麗に終了されるわけではない（ドキュメントは保存されない）。

## Linux

[Linux](../Page/Linux.md "wikilink")では、キーボードストローク・コンビネーションは[カーネル](../Page/カーネル.md "wikilink")のキーボードデバイスドライバによって認識される。特に指示されていない場合（たいていはシステム初期化中の間）、カーネルはソフトリブートを開始する。より一般的には、カーネルは *[init](https://ja.wikipedia.org/wiki/init "wikilink")* プロセスにシグナルを送り、スクリプトを実行したり、「現在のセッションを終了します」と表示したりする。

多くのLinuxディストリビューションでは、*init* はシグナルを受けて[ランレベル](../Page/ランレベル.md "wikilink")を切り替えて、ソフトリブート実行する。なお、Linuxのシステムではキーボードストローク・コンビネーションを無視することもできる。設定は、たいてい inittab(5)設定ファイルのcaというキーワード下にある。

## Mac OS

[Mac OS Xや](https://ja.wikipedia.org/wiki/macOS "wikilink")[Classic Mac OSで](../Page/Classic_Mac_OS.md "wikilink") -- に対応するキーの組合せは、-- （[コマンドキー](../Page/コマンドキー.md "wikilink")と[オプションキー](../Page/オプションキー.md "wikilink")を押しながらEscキー）である。これらを押すと強制終了ウィンドウが表示される。Macのノート型パソコンは、キーボード電源ボタンをサポートし、-- を押すと、システムを[ハードリブートする](https://ja.wikipedia.org/wiki/ブート#ハードリブート "wikilink")。macOSでは、-- になっている。macOSで-の組合せは、ログアウト、スリープ、再起動、終了の選択をする画面になる。1980年代のアップルの[マイコン](../Page/マイクロコンピュータ.md "wikilink")（[Apple IIや](../Page/Apple_II.md "wikilink")[Apple III](../Page/Apple_III.md "wikilink")）では、-- の組合せでソフトブートが始まる。

## Control-Alt-Deleteと大衆文化

[thumb](https://ja.wikipedia.org/wiki/ファイル:GroenLinks_demonstration_20041002_CtrlAltDel-crop.JPG "wikilink")

コンピュータが普及したことで、Control-Alt-Delete は[隠語](../Page/隠語.md "wikilink")としても使われるようになった。 は、英語で （…を投げ捨てる）とか （…を廃止する）という意味を持つ\[5\]。

## 参考文献

### 参照

<div class="references-small">

1.
2.  Linux manual pages for kill(2) and reboot(2).

3.  — a report of the effect of `LocalReboot` in Windows 95

4.  — a report of differences in `LocalReboot` between Windows 3.x and Windows 95

</div>

## 外部リンク

  - [David Bradley described how he invented CTRL-ALT-DEL and made famous stab on Bill Gates](http://www.worldspace.nu/The_origin_of_Control-Alt-Delete_-_David_Bradley_invented_CTRL-ALT-DEL_Bill_Gates_made_it_famous_avi:watch)

[Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:パーソナルコンピュータ](https://ja.wikipedia.org/wiki/Category:パーソナルコンピュータ "wikilink") [Category:コンピュータのキー](https://ja.wikipedia.org/wiki/Category:コンピュータのキー "wikilink")

1.
2.  [ビル・ゲイツ氏、「Ctrl＋Alt＋Del」は失敗だったと認める（2013年09月27日 11時29分 UPDATE）](http://www.itmedia.co.jp/news/articles/1309/27/news053.html) - ITmedia NEWS
3.  [ビル・ゲイツ氏、「Ctrl+Alt+Deleteは失敗だった」（2013.09.27 ）](http://www.cnn.co.jp/tech/35037737.html) - CNN.co.jp
4.
5.  [Wordspy](http://www.wordspy.com/words/Ctrl-Alt-Delete.asp) はこの用法の最初期の例として Chris Miksanek による Computerworld 誌の1995年12月18日付のコラム "Ctrl-Alt-Delete those holiday trinkets." を引用している