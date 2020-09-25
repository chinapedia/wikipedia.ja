> この記事は[PuTTY](https://ja.wikipedia.org/wiki/PuTTY)から翻訳されています。


{{ Infobox Software | 名称 = PuTTY | ロゴ = PuTTY icon 128px.png | スクリーンショット = [256px](https://ja.wikipedia.org/wiki/ファイル:PuTTY.PNG "wikilink") | 説明文 = PuTTYの設定ウィンドウ | 開発元 = Simon Tatham | 初版 =  | 最新版 = 0.74 | 最新版発表日 =  | プログラミング言語 = [C言語](../Page/C言語.md "wikilink") | 対応OS = [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
[UNIX](../Page/UNIX.md "wikilink")
[Android](../Page/Android_\(オペレーティングシステム\).md "wikilink")
[Windows Mobile](../Page/Windows_Mobile.md "wikilink")
[Symbian OS](../Page/Symbian_OS.md "wikilink")
[Windows Embedded Compact](../Page/Microsoft_Windows_Embedded_CE.md "wikilink") | 種別 = リモートログオン[クライアント](../Page/クライアント_\(コンピュータ\).md "wikilink") | ライセンス = [MIT License](../Page/MIT_License.md "wikilink")\[1\] | 公式サイト = [PuTTY: A Free Telnet/SSH Client](https://www.chiark.greenend.org.uk/~sgtatham/putty/index.html) }}

**PuTTY**(パティ)はSimon Tathamが[MIT Licence](https://ja.wikipedia.org/wiki/MIT_Licence "wikilink")\[2\]([オープンソース](../Page/オープンソース.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")[ライセンス](../Page/ライセンス.md "wikilink")の一種)で開発·公開しているリモートログオン[クライアントである](../Page/クライアント_\(コンピュータ\).md "wikilink")。

## 特徴

本[ソフトウェア](../Page/ソフトウェア.md "wikilink")は、下記の機能を有し、[SSH](../Page/Secure_Shell.md "wikilink")·SSH2·[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")·[rlogin](https://ja.wikipedia.org/wiki/rlogin "wikilink")·[TCP](../Page/Transmission_Control_Protocol.md "wikilink")·[シリアルポート](../Page/シリアルポート.md "wikilink")([RS-232](../Page/RS-232.md "wikilink")·[RS-422](https://ja.wikipedia.org/wiki/RS-422 "wikilink")·[RS-485](https://ja.wikipedia.org/wiki/RS-485 "wikilink"))の各[通信プロトコル](../Page/通信プロトコル.md "wikilink")に対応している。 また、[サードパーティー](../Page/サードパーティー.md "wikilink")の成果も有って、[Windowsのみならず](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[UNIX](../Page/UNIX.md "wikilink")系から[Androidや](../Page/Android_\(オペレーティングシステム\).md "wikilink")[Windows Mobileまで](../Page/Windows_Mobile.md "wikilink")、更には[Symbian OSや](../Page/Symbian_OS.md "wikilink")[Windows Embedded Compactも含めて](../Page/Microsoft_Windows_Embedded_CE.md "wikilink")、様々な[OSに移植されている](../Page/オペレーティングシステム.md "wikilink")。

  - [ポートフォワーディング機能](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")([X11](https://ja.wikipedia.org/wiki/X11 "wikilink")フォワードを含む)
  - [VT102の粗完全な](../Page/VT100.md "wikilink")[エミュレーション及び](../Page/エミュレータ.md "wikilink")[xterm](https://ja.wikipedia.org/wiki/xterm "wikilink")やECMA-48端末の制御シーケンスの多くのサポート
  - 詳細なオプション([暗号](../Page/暗号.md "wikilink")化や[認証](../Page/認証.md "wikilink")に関する設定や[トンネリング](../Page/トンネリング.md "wikilink")など)
  - 接続先毎に異なる設定を保存できる
  - [SCPや](../Page/Secure_copy.md "wikilink")[SFTP](https://ja.wikipedia.org/wiki/SFTP "wikilink")の[コマンドラインクライアント](../Page/コマンドラインインタプリタ.md "wikilink")[ユーティリティの付属](../Page/ユーティリティソフトウェア.md "wikilink")
      - **Plink**: 各[プロトコル](../Page/プロトコル.md "wikilink")(ssh·telnet·rlogin)での接続を司るコマンドラインツール
      - **PuTTY**: [バックエンドにPlinkを用いて](https://ja.wikipedia.org/wiki/バックグラウンド_\(ソフトウェア\) "wikilink")[サーバーへの接続を行う](../Page/リモートホスト.md "wikilink")[CUIツール](../Page/キャラクタユーザインタフェース.md "wikilink") (PuTTY本体)
          - **PuTTYtel**: telnetとrloginのみ可能なCUIツール
      - **PSCP**: SSHまたはSSH2のサーバーとSCPで[ファイルを遣り取りする](../Page/ファイル_\(コンピュータ\).md "wikilink")[コマンドライン](https://ja.wikipedia.org/wiki/テキストユーザインタフェース "wikilink")[ツール](../Page/ツール.md "wikilink")
      - **PSFTP**: SSH2サーバーとファイルをSFTPで対話的に遣り取りするコマンドラインツール
      - **PuTTYgen**: SSHでの[暗号](../Page/暗号.md "wikilink")[通信に必要な](../Page/データ通信.md "wikilink")[RSA暗号](../Page/RSA暗号.md "wikilink")や[DSAによる](https://ja.wikipedia.org/wiki/Digital_Signature_Algorithm "wikilink")[公開鍵を作成する](../Page/公開鍵暗号.md "wikilink")
      - **Pageant**: SSH認証を行う[デーモン](../Page/デーモン_\(ソフトウェア\).md "wikilink")(PuTTY·PSCP·PSFTP·Plinkを内部的に使用する)

更に、**PuTTY PRIVATE PATCHES**や**PuTTYrv**のように、オリジナルのPuTTYを基に[機能追加された版が幾つか存在する](https://ja.wikipedia.org/wiki/patch "wikilink")。

### 複数接続

PuTTYを内部で多重起動して同時に複数の端末に接続できるユーティリティとして、**SuperPutty**や**PuTTYTabManager**が利用されている。 これらは、[タブ化され各ウィンドウペインをドッキング自在な](../Page/タブ_\(GUI\).md "wikilink")[ユーザーインターフェイスを持ち](../Page/ユーザインタフェース.md "wikilink")、一つの[ウィンドウ](../Page/ウィンドウ.md "wikilink")内で複数接続から[セッション管理まで実行できるので](https://ja.wikipedia.org/wiki/セッション_\(コンピュータ\) "wikilink")[ユーザビリティ](../Page/ユーザビリティ.md "wikilink")に優れる。 ただし、これらはPuTTYのラッパー として機能するので、単独での利用はできずPuTTYを組み合わせて用いられる。 SuperPuttyは、バックグラウンドでPuTTYと供にPSCPや[WinSCP](../Page/WinSCP.md "wikilink")および[FileZilla](https://ja.wikipedia.org/wiki/FileZilla "wikilink")を連携させて、SuperPuttyの[GUIユーザーインターフェイスからSCPやSFTPによるファイルを遣り取りでき](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、また、[リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")クライアントである[TightVNC](https://ja.wikipedia.org/wiki/TightVNC "wikilink")を組み合わせれば、SSHポートフォワーディングを介した[VNC接続を行える](../Page/Virtual_Network_Computing.md "wikilink")。

### 派生版

PuTTYから[派生した](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")[アプリケーションとしては](../Page/アプリケーションソフトウェア.md "wikilink")、**KiTTY**や**PieTTY**などがある。 これらには、PuTTYの特徴を備えたうえで、更に独自の機能拡張が施されている。

### PuTTYを内包しているもの

SSHクライアントの一種である[mRemoteNG](https://ja.wikipedia.org/wiki/mRemoteNG "wikilink")や[Solar-PuTTY](https://ja.wikipedia.org/wiki/Solar-PuTTY "wikilink")では、パッケージにPuTTYの機能拡張版が含まれている。 また、VT220の[エミュレーターの一種である](../Page/端末エミュレータ.md "wikilink")[IVTは](https://ja.wikipedia.org/wiki/IVT_\(端末エミュレータ\) "wikilink")、PuTTYのコードを含んでいおり\[3\]、リモートログオンクライアントとしても利用できる。

[Cygwin](../Page/Cygwin.md "wikilink")や[MSYS](../Page/MSYS.md "wikilink")では、PuTTYを基に\[4\]、**[mintty](https://ja.wikipedia.org/wiki/mintty "wikilink")**が独立して開発されている。 [Xming](../Page/Xming.md "wikilink")はPuTTYをサポートしており、[パッケージにはPuTTYのplink](../Page/パッケージソフトウェア.md "wikilink").exeも含まれている。

Androidで動作する[Mobile SSHでは](https://ja.wikipedia.org/wiki/Mobile_SSH "wikilink")、[バックエンド](../Page/フロントエンド.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")にPuTTYが使用されている。

## 日本における動向

[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")では、1990年代後半までは[Tera TermがWindows用端末エミュレータの代表格だった](../Page/Tera_Term.md "wikilink")。その後にSSH2の需要が高まったが、Tera Termは長らくSSH2をサポートしていなかった。 その一方で、PuTTYは登場した1998年当初からSSH1及びSSH2に対応していたため、Tera Termからの移行が進んでいった。

現在では、有志の[日本語化による](../Page/国際化と地域化.md "wikilink")**PuTTYjp**や様々なpatchを適用した**PuTTY ごった煮版**を基として更に機能が追加されたPuTTY PRIVATE PATCHESやPuTTYrvが広く使用され、Windows環境では代表的なリモートログオンクライアントとなっている。

## 脚注

### 注釈

### 出典

## 関連項目

[プロトコル](../Page/プロトコル.md "wikilink")

  - [SSH](../Page/Secure_Shell.md "wikilink")
      - [SCP](../Page/Secure_copy.md "wikilink")
      - [SFTP](https://ja.wikipedia.org/wiki/SFTP "wikilink")

[実装](../Page/実装.md "wikilink")

  - [OpenSSH](../Page/OpenSSH.md "wikilink")
  - [Bitvise SSH Server](https://ja.wikipedia.org/wiki/Bitvise_SSH_Server "wikilink") [Bitvise SSH Client](https://ja.wikipedia.org/wiki/Bitvise_SSH_Client "wikilink")
  - [FileZilla](https://ja.wikipedia.org/wiki/FileZilla "wikilink")

クライアントアプリケーション

  - [WinSSHTerm](https://ja.wikipedia.org/wiki/WinSSHTerm "wikilink")
  - [mRemoteNG](https://ja.wikipedia.org/wiki/mRemoteNG "wikilink")
      - [mRemote](https://ja.wikipedia.org/wiki/mRemote "wikilink")
  - [RLogin](https://ja.wikipedia.org/wiki/RLogin "wikilink")
  - [Poderosa](../Page/Poderosa.md "wikilink") (【元】Terminal Emulator VaraTerm)
  - [Tera Term](../Page/Tera_Term.md "wikilink")
  - [Bitvise SSH Client](https://ja.wikipedia.org/wiki/Bitvise_SSH_Client "wikilink")
  - [MobaXterm](https://ja.wikipedia.org/wiki/MobaXterm "wikilink")
  - [Xshell](https://ja.wikipedia.org/wiki/Xshell "wikilink")
  - [SmarTTY](https://ja.wikipedia.org/wiki/SmarTTY "wikilink")
  - [JuiceSSH](https://ja.wikipedia.org/wiki/JuiceSSH "wikilink")
  - [WinSCP](../Page/WinSCP.md "wikilink")
  - [Tunnelier](https://ja.wikipedia.org/wiki/Tunnelier "wikilink")

PuTTY内包

  - [IVT](https://ja.wikipedia.org/wiki/IVT_\(端末エミュレータ\) "wikilink")
  - [Solar-PuTTY](https://ja.wikipedia.org/wiki/Solar-PuTTY "wikilink") (【元】Dameware SSH client)
  - [Xming](../Page/Xming.md "wikilink")
  - [Secure Shell App](https://ja.wikipedia.org/wiki/Secure_Shell_App "wikilink")
  - [Mobile SSH](https://ja.wikipedia.org/wiki/Mobile_SSH "wikilink")

端末エミュレーター

  - [Hyper](https://ja.wikipedia.org/wiki/Hyper "wikilink")
  - [Termius](https://ja.wikipedia.org/wiki/Termius "wikilink") (【元】ServerAuditor)
  - [Terminals](https://ja.wikipedia.org/wiki/Terminals "wikilink")

参考

  -
## 外部リンク

本体

  - [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/index.html) [(リポジトリ)](https://git.tartarus.org/?p=simon/putty.git;a=summary) [(PortableApps)](https://portableapps.com/apps/internet/putty_portable)

<!-- end list -->

  -   - [PuTTY PRIVATE PATCHES](http://ice.hotmint.com/putty/index.html) (開発版PuTTY & ごった煮版 & 各種patch)
          - [D2D/DW PuTTY](https://ice.hotmint.com/putty/d2ddw.html) (開発版PuTTY & ごった煮版 & 各種patch & [Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")および[DirectWrite](https://ja.wikipedia.org/wiki/DirectWrite "wikilink")での[レンダリング](../Page/レンダリング_\(コンピュータ\).md "wikilink"))

<!-- end list -->

  -   - [PuTTYrv](http://www.ranvis.com/putty) [(GitHub リポジトリ)](https://github.com/ranvis/putty) (【元】**PuTTY-ranvis**) (安定版PuTTY & ごった煮版 & 各種patch)
      - [PuTTYjp](http://hp.vector.co.jp/authors/VA024651/PuTTYkj.html) ([日本語](../Page/日本語.md "wikilink")対応 & [フォント](../Page/フォント.md "wikilink")変更)
      - [PuTTY-url](http://ryara.net/putty-url/index.html) ([URL](../Page/Uniform_Resource_Locator.md "wikilink")[文字列](../Page/文字列.md "wikilink")の[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")化)
      - puttywincrypt [(SourceForge リポジトリ)](https://sourceforge.net/projects/puttywincrypt/) [(Google リポジトリ)](https://code.google.com/p/puttywincrypt/) ([スマートカードおよび](../Page/ICカード.md "wikilink")[Wincrypt](https://ja.wikipedia.org/wiki/Wincrypt "wikilink")への対応)
      - [PuTTY](http://jakub.kotrla.net/putty/index.html) ([ウクライナ語](../Page/ウクライナ語.md "wikilink")·[イタリア語](../Page/イタリア語.md "wikilink")·[ポーランド語](../Page/ポーランド語.md "wikilink")·[タイ語](../Page/タイ語.md "wikilink")·[ウズベク語](../Page/ウズベク語.md "wikilink")·[ポルトガル語](https://ja.wikipedia.org/wiki/ポルトガル語 "wikilink")·[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink")·[フィンランド語](../Page/フィンランド語.md "wikilink")対応およびファイルへの設定情報保存)
      - [PuTTY](https://www.putty.sk/)
      - [PuTTY JP XTrans](https://web.archive.org/web/20060116095616/http://www.withe.ne.jp/~kabocha/softs/putty/) (安定版PuTTY & ごった煮版 & 背景透過) (開発中止)
      - [PuTTYどこでもハック版](http://ncl.sakura.ne.jp/doc/ja/software/dkdmputty-readme.html) (PuTTY & ごった煮版 & 非固定幅フォントや組込み日本語フォントへの対応など) (開発中止)
      - [PuTTY ごった煮版](https://web.archive.org/web/20170411054717/http://yebisuya.dip.jp/Software/PuTTY/index.html) (各種patch適用) (開発中止)

<!-- end list -->

  -   - [PuTTY](https://w.atwiki.jp/pokatan/) (PuTTY & ごった煮版 & テキスト周囲の縁取り & マウス選択挙動変更 & 背景半透明化) (開発中止)
      - [PuTTY](https://web.archive.org/web/20150224145927/http://nanabit.net/softwares/putty-bgi-patch.html) (背景画像表示) (開発中止)
      - [Le Putty](http://leputty.sourceforge.net/index.html) [(SourceForge リポジトリ)](https://sourceforge.net/projects/leputty/) ([ZMODEM](https://ja.wikipedia.org/wiki/ZMODEM "wikilink")対応) (開発中止)
      - [PuTTY](https://web.archive.org/web/20171220205836/https://www.warp13.co.uk/putty.py) (自動再接続対応) (開発中止)
      - [portaPuTTY](https://web.archive.org/web/20080704170005/http://socialistsushi.com/portaputty/) [(Google リポジトリ)](https://web.archive.org/web/20120618145100/http://code.google.com/p/portaputty/) (設定情報をのファイル保存) (開発中止)
      - [Transparent PuTTY](https://web.archive.org/web/20161023084451/http://www.qbaum.net/wp/?page_id=112) (ウィンドウの透明化) (開発中止)
      - [transputty](https://web.archive.org/web/20160515203214/http://cprogramming.hu/transputty/) (ウィンドウの透明化) (開発中止)
      - futty [(Google リポジトリ)](https://code.google.com/p/futty/) [(SourceForge リポジトリ)](https://sourceforge.net/projects/futty/) (PuTTYTray & PuTTY) (開発中止)
          - [PuTTYTray: Redux](http://www.simmonsconsulting.com/puttytray/index.php) (開発中止)
              - [PuTTY Tray](https://puttytray.goeswhere.com/index.html) [(GitHub リポジトリ)](https://github.com/FauxFaux/PuTTYTray) (自動再接続·ウィンドウの透過·[タスクトレイ](../Page/タスクトレイ.md "wikilink")への最小化·URL文字列のハイパーリンク化·設定情報のファイル保存) (開発中止)

<!-- end list -->

  -   - adbputty [(GitHub リポジトリ)](https://github.com/sztupy/adbputty/) [(GitHub リポジトリ)](https://github.com/kiddlu/adbputty/) (adb: [Android Debug Bridge](https://ja.wikipedia.org/wiki/Android_Debug_Bridge "wikilink") 対応) (開発中止)
      - [putty](http://putty.grzybicki.pl/) (ポーランド語対応) (開発中止)
      - [PuTTY DBCS patched](https://web.archive.org/web/20110727081905/http://www.mhsin.org/putty/) ([中国語](../Page/中国語.md "wikilink")対応) (開発中止)

<!-- end list -->

  -   - [HPuTTY](http://hputty.org/index.html) [(GitHub リポジトリ)](https://github.com/teamnop/HPuTTY/) (PuTTYTray & iPuTTY & @) (開発中止)
          - [iPuTTY](https://kldp.net/iputty/) [(GitHub リポジトリ)](https://github.com/iPuTTY/iPuTTY) [(Bitbucket リポジトリ)](https://bitbucket.org/daybreaker/iputty/src/default/) ([朝鮮語](../Page/朝鮮語.md "wikilink")対応) (開発中止)
              - [dputty](https://web.archive.org/web/20140606082857/https://dev.daybreaker.info/dputty) [(リポジトリ)](http://svn.daybreaker.info/dputty/) (朝鮮語対応) (開発中止)

[マニュアル](../Page/マニュアル.md "wikilink")

  - [PuTTY User Manual](https://tartarus.org/~simon/putty-snapshots/htmldoc/index.html)

<!-- end list -->

  -   - [PuTTY ユーザマニュアル](https://www.ranvis.com/doc/putty/man/index.html) (日本語[翻訳](../Page/翻訳.md "wikilink"))

複数接続&セッション管理

  - SuperPutty [(facebook)](https://www.facebook.com/superputty) [(GitHub リポジトリ)](https://github.com/jimradford/superputty) (KiTTYおよびMinTTYもしくはputtycygにも対応している) (開発引き継ぎ)
      - SuperPutty [(GitHub リポジトリ)](https://github.com/phendryx/superputty) [(Google リポジトリ)](http://code.google.com/p/superputty/) (開発中止)
  - [PuTTYTabManager](https://sites.google.com/site/macdsite/utilidades/puttytabmanager) (KiTTYにも対応している)
  - [PuTTY Connection Manager](https://web.archive.org/web/20111101154926/http://puttycm.free.fr/cms/index.php?option=com_content&view=frontpage&Itemid=62) (開発中止)
  - Multi PuTTY Manager [(SourceForge リポジトリ)](https://sourceforge.net/projects/multiputtymanager/) (開発中止)
  - [PuTTY Manager](http://puttymanager.sourceforge.net/index.php?option=com_content&view=article&id=1&Itemid=8) [(SourceForge リポジトリ)](https://sourceforge.net/projects/puttymanager/) (開発中止)

フォーク

  - [KiTTY](http://www.9bis.net/kitty/index.php?theme=default&zone=en&page=Welcome&action=&id=&pageid=) [(GitHub リポジトリ)](https://github.com/cyd01/KiTTY/) [(Google ドライブ)](https://drive.google.com/drive/u/0/folders/0BzxnxE_EM8nlamd1cEV5b003QVk)
  - [PieTTY](https://sites.google.com/view/pietty-project) (【元】**pputty**)
  - RuTTY [(SourceForge リポジトリ)](https://sourceforge.net/projects/rutty/) (scripting機能)
  - [Metro PuTTY](http://mattwesemann.azurewebsites.net/index.html)
  - [Nutty](https://web.archive.org/web/20161111205156/http://groehn.net/nutty/) (URL文字列のハイパーリンク化) (開発中止)
  - [TuTTY](http://putty.dwalin.ru/?tutty) [(GitHub リポジトリ)](https://github.com/nohuhu/TuTTY) (開発中止)
  - [ExtraPuTTY](http://www.extraputty.com/index.php) [(SourceForge リポジトリ)](https://sourceforge.net/projects/extraputty/) (開発中止)
  - [Quest PuTTY](http://rc.quest.com/topics/putty/) (開発中止)

ユーティリティ

  - セッション管理
      - [PuTTY Session Manager](https://puttysm.sourceforge.io/index.html) [(SourceForge リポジトリ)](https://sourceforge.net/projects/puttysm/) (KiTTYにも対応している) (開発中止)
          - [KiTTY Session Manager](https://www.noobunbox.net/projects/kitty-session-manager) [(GitHub リポジトリ)](https://github.com/novakin/Kitty-Session-Manager/) (KiTTY専用) (開発中止)
      - [PuTTYMenu](https://web.archive.org/web/20160718153527/http://www.ntsend.freeserve.co.uk/puttymenu.html) (開発中止)
      - [QuickPutty](https://web.archive.org/web/20110904062812/http://www.deckmyn.org/olivier/software) (開発中止)
      - putty-launchy-plugin [(Google リポジトリ)](https://code.google.com/p/putty-launchy-plugin/) (開発中止)
      - [plaunch](http://putty.dwalin.ru/?plaunch) (開発中止)
  - [VPN接続補助](../Page/Virtual_Private_Network.md "wikilink")
      - putty-tunnel-manager [(Google リポジトリ)](https://code.google.com/p/putty-tunnel-manager/) (開発中止)
      - [MyEnTunnel](https://web.archive.org/web/20150731031944/http://nemesis2.qx.net/pages/MyEnTunnel) (開発中止)
      - [CallingHome](http://callinghome.sourceforge.net/overview.html) [(SourceForge リポジトリ)](https://sourceforge.net/projects/callinghome/) (開発中止)
  - その他
      - [PuttyTabs](http://www.raisin.de/putty-tabs/putty-tabs.html) (ウィンドウ管理) (開発中止)
      - [PuttyConfer](https://web.archive.org/web/20190228173452/http://www.thiago.joi.com.br/andre/puttyconfer.html) (レジストリ中のPuTTY設定情報管理) (開発中止)
      - putty-launchy-plugin [(Google リポジトリ)](https://code.google.com/p/putty-launchy-plugin/) (開発中止)
      - [PuTTYCS](http://www.millardsoftware.com/puttycs) (起動している全てのPuTTYへのコマンド一斉送信) (開発中止)
      - [PuTTY Magic](https://web.archive.org/web/20171119153629/http://www.kenworld.se/robert/index.asp?dir=Putty%20Magic) (ウィンドウの透明化) (開発中止)
      - JAWS-PuTTY-Scripts [(GitHub リポジトリ)](https://github.com/munawarb/JAWS-PuTTY-Scripts) (開発中止)
      - boxtty [(GitHub リポジトリ)](https://github.com/plasticbox/boxtty) (開発中止)

複数接続対応

  - [MTPuTTY](http://www.ttyplus.com/index.html) (開発中止)

[MUD](../Page/MUD.md "wikilink")対応

  - [PowTTY](http://www.elvenrunes.com/powtty/) (開発中止)
  - [DF Client](https://web.archive.org/web/20140104124115/http://www.dforces.net/client/) (開発中止)

[DLL形式](../Page/ダイナミックリンクライブラリ.md "wikilink")

  - [W-PuTTY-CD](https://web.archive.org/web/20120213175953/http://www.winputty.com/Default.html) (開発中止)

他のOSや[プラットフォームへの移植](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")

  - [mintty](https://ja.wikipedia.org/wiki/mintty "wikilink") (Cygwin、MSYS、MSYS2用)
  - puttycyg [(Google リポジトリ)](https://code.google.com/p/puttycyg/) (Cygwin 用) (開発中止)
  - [PocketPuTTY](https://web.archive.org/web/20150221064425/http://pocketputty.net/index.html) (Windows Embedded Compact 用) (開発中止)
      - (日本語対応) (Windows Mobile & Windows Embedded Compact & Pocket PC 用) (開発中止)
  - [s2putty](http://s2putty.sourceforge.net/index.html) [(SourceForge リポジトリ)](https://sourceforge.net/projects/s2putty/) (Symbian OS 用) (開発中止)
  - [Putty](https://web.archive.org/web/20090416174705/http://matrix.tmit.bme.hu/putty/) ([Symbian UIQ](https://ja.wikipedia.org/wiki/Symbian_UIQ "wikilink") 用) (開発中止)
  - [PuTTy](https://web.archive.org/web/20070703043843/http://www.mobileyes.com/index.php?option=com_content&task=view&id=23&Itemid=51) (Symbian UIQ 用) (開発中止)
  - [Putty](https://web.archive.org/web/20130106173923/https://kelley.ca/amd64/) (AMD64 用) (開発中止)

複数接続&セッション管理

  - AutoPutty [(GitLab リポジトリ)](https://gitlab.com/jwhitmore/autoputty) [(GitHub リポジトリ)](https://github.com/jwhitmore/AutoPutty) ([Qt](../Page/Qt.md "wikilink")環境で動作する) (開発引き継ぎ)
      - [AutoPuTTY](https://r4di.us/autoputty/index.htm) [(GitHub リポジトリ)](https://github.com/r4dius/AutoPuTTY) (開発中止)

[Category:端末エミュレータ](https://ja.wikipedia.org/wiki/Category:端末エミュレータ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Secure_Shell](https://ja.wikipedia.org/wiki/Category:Secure_Shell "wikilink") [Category:Telnet](https://ja.wikipedia.org/wiki/Category:Telnet "wikilink")

1.
2.
3.
4.