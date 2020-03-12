> この記事は[FFFTP](https://ja.wikipedia.org/wiki/FFFTP)から翻訳されています。


**FFFTP**（エフエフエフティーピー）は、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に曽田純（Sota, 以降は「作者」と記述）によって開発された[FTPクライアント](../Page/FTPクライアント.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")。漢字などの[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")を名前に含む[ファイルを扱えるのが特徴で](../Page/ファイル_\(コンピュータ\).md "wikilink")、日本語版と英語版が公開されている。

作者による開発は[2011年](../Page/2011年.md "wikilink")8月31日をもって終了したが、その後は有志による[オープンソース](../Page/オープンソース.md "wikilink")での開発が続けられている。

## 概要

[GUIにより](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[コマンドラインを使わずに](../Page/コマンドラインインタプリタ.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")にあるファイルを管理することができる。三面分割型のGUIを持ち、左側はローカル側ファイル一覧、右側はリモート側ファイル一覧、下側に作業履歴が表示される。

開発が有志によるFFFTPプロジェクトへ移されてから[UTF-8](../Page/UTF-8.md "wikilink")や[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")通信、セキュアな通信として[FTPS](../Page/FTPS.md "wikilink")への対応などの変更が加えられた。しかし、[SCPなどの](../Page/Secure_copy.md "wikilink")[SSHプロトコルを利用した転送方式には設定画面のGUIは既にできてはいるが](../Page/Secure_Shell.md "wikilink")、実装はされておらず、対応未定となっている。

2011年[10月](https://ja.wikipedia.org/wiki/10月 "wikilink")頃は安定性の観点からバージョン1.97bの利用をプロジェクト自ら推奨していた\[1\]が、脆弱性が次々と発見されてからは、特殊な事情を除き最新版へのバージョンアップが推奨されている\[2\]。

2017年10月には、開発メンバーの1人が、ホスト設定を[WinSCP](../Page/WinSCP.md "wikilink")へエクスポートする機能を実装したうえで開発を終える予定であると伝えた\[3\]。

2018年4月、開発を引き継ぐ人物が現れ、バージョン3.0が公開された\[4\]。

## 歴史

[Windows 95の時代](../Page/Microsoft_Windows_95.md "wikilink")、[ウェブページ](../Page/ウェブページ.md "wikilink")公開の流行に伴って多くのFTPクライアントが公開された。、。しかし、WS_FTPを含めフリーかつ日本語で使えるFTPクライアントは無かった。。

### 作者による開発

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")、FFFTPの開発が開始される。後に作者自身のブログで、開発を始めた経緯について『仕事で使うFTPソフトが欲しいと思ったのが、きっかけだった。[シェアウエアのFTPソフトで](../Page/シェアウェア.md "wikilink")、使いやすそうなのはいくつかあったけど、会社で買ってくれないと使えない。欲しいものは自分で作ろうと考えて、FFFTPの製作を開始した。』と述べている\[5\]。

[2002年](../Page/2002年.md "wikilink")、[オンラインソフトウェア大賞を受賞](../Page/フリーソフトウェア大賞.md "wikilink")。作者は『私が作成したソフトが、栄誉ある賞を受賞できるとは思ってもおりませんでした。』とコメントした\[6\]。

2008年[6月3日](../Page/6月3日.md "wikilink")、[デンマーク](https://ja.wikipedia.org/wiki/デンマーク "wikilink")のセキュリティベンダー[Secunia](https://ja.wikipedia.org/wiki/Secunia "wikilink")よりFFFTP 1.96bおよびそれ以前のバージョンに[ディレクトリトラバーサル](../Page/ディレクトリトラバーサル.md "wikilink")の脆弱性の存在が発表される\[7\]。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[1月30日](../Page/1月30日.md "wikilink")、[2009年](../Page/2009年.md "wikilink")から被害が拡大した[マルウェア](../Page/マルウェア.md "wikilink")[Gumblar](https://ja.wikipedia.org/wiki/Gumblar "wikilink")について、FFFTPの[レジストリ](../Page/レジストリ.md "wikilink")に記録された情報が狙われているとの報告が（作者により）発表された\[8\]。レジストリ上に記録されたIDやパスワード、接続先といった情報を盗まれて[ウェブサイト](../Page/ウェブサイト.md "wikilink")が改ざんされる被害も発生した\[9\]\[10\]。当初作者はFFFTPのバージョンアップによる機能強化については検討段階としており、「[SSLなどへの対応は難しい](../Page/Transport_Layer_Security.md "wikilink")」「完全に攻撃を逃れる方法は採れないかもしれません」との見解を発表した\[11\]。マルウェア対策としてレジストリからFFFTPのデータを削除するツールが提供され\[12\]、有志による対策が施された改造バイナリが提供された。

2010年[2月7日](../Page/2月7日.md "wikilink")に作者からリリースされた1.97にマルウェア対策済みのバイナリが取り込まれた。この変更によって起動時には「マスターパスワード」の入力を要求するようになり、併せて保存されるパスワードの暗号化アルゴリズムが[AESへと強化された](../Page/Advanced_Encryption_Standard.md "wikilink")。

2011年[8月31日](../Page/8月31日.md "wikilink")、作者はFFFTPの開発終了を宣言した。理由について自身のブログで『開発を継続していくモチベーションが保てなくなった』と説明している\[13\]。

### オープンソースによる開発

#### [OSDN](../Page/OSDN.md "wikilink")(旧SourceForge.JP)上での開発

  - 2011年[9月1日](../Page/9月1日.md "wikilink")より、有志により開発は[SourceForge.JP](https://ja.wikipedia.org/wiki/SourceForge.JP "wikilink")(現[OSDN](../Page/OSDN.md "wikilink"))上へ移行。
  - 2011年[10月12日](https://ja.wikipedia.org/wiki/10月12日 "wikilink")にSourceForge.JPへ移行してから初のバージョンアップとなる1.98が公開。アスキーモード転送時の漢字コード変換で新たに[UTF-8](../Page/UTF-8.md "wikilink")が追加され、[FTPS](../Page/FTPS.md "wikilink")（Explicitモード）に対応。
  - 2011年[10月28日](https://ja.wikipedia.org/wiki/10月28日 "wikilink")、[JVN](https://ja.wikipedia.org/wiki/JVN "wikilink")よりFFFTP 1.98aおよびそれ以前のバージョンから実行ファイル読み込みに関する脆弱性の存在が発表される\[14\]。
  - 2011年[11月5日](../Page/11月5日.md "wikilink")、バージョン1.98cよりUTF-8（BOMなし）への変換がサポートされ、FTPS（Implicitモード）などに対応。
  - 2011年[11月22日](https://ja.wikipedia.org/wiki/11月22日 "wikilink")、バージョン1.98dより[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")通信への対応、機能の改善や不具合の修正が行われた。
  - 2011年[12月9日](../Page/12月9日.md "wikilink")、JVNよりFFFTP 1.98cおよびそれ以前のバージョンから実行ファイル読み込みに関する脆弱性の存在が発表される\[15\]。
  - [2012年](../Page/2012年.md "wikilink")[2月23日](https://ja.wikipedia.org/wiki/2月23日 "wikilink")、バージョン1.98eを公開。速度や不具合の改善の他、ZIP版では標準でレジストリを使用しない設定となった。
  - 2012年[7月2日](../Page/7月2日.md "wikilink")、バージョン1.98fを公開。
  - [2013年](../Page/2013年.md "wikilink")[2月25日](../Page/2月25日.md "wikilink")、バージョン1.98gを公開。
  - [2014年](../Page/2014年.md "wikilink")[4月13日](../Page/4月13日.md "wikilink")、[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")ライブラリの[ハートブリード](https://ja.wikipedia.org/wiki/ハートブリード "wikilink")脆弱性に対応したバージョン1.98g1、1.98g2を相次ぎ緊急公開。次回更新時に正式リリースされる予定 \[16\]。
  - [2016年](../Page/2016年.md "wikilink")[5月14日](../Page/5月14日.md "wikilink")、バージョン1.99aを公開
  - [2017年](../Page/2017年.md "wikilink")[10月14日](../Page/10月14日.md "wikilink")、WinSCPへの設定エクスポート機能を搭載したバージョン2.00を最終版としてリリースし、開発終了することが表明された\[17\]。
  - [2018年](../Page/2018年.md "wikilink")[4月15日](../Page/4月15日.md "wikilink")、[OSDN](../Page/OSDN.md "wikilink")上での最終版となるバージョン2.00を公開

#### [GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")上での開発

  - [2018年](../Page/2018年.md "wikilink")[4月2日](../Page/4月2日.md "wikilink")、開発を引き継ぐ人物が現れ、[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")上に開発を移行しバージョン3.0を公開\[18\]。
  - [2018年](../Page/2018年.md "wikilink")[4月11日](../Page/4月11日.md "wikilink")、バージョン3.1を公開
  - [2018年](../Page/2018年.md "wikilink")[4月20日](https://ja.wikipedia.org/wiki/4月20日 "wikilink")、バージョン2.00の更新内容を取り込んだバージョン3.2を公開
  - [2018年](../Page/2018年.md "wikilink")[5月5日](../Page/5月5日.md "wikilink")、バージョン3.3を公開
  - [2019年](../Page/2019年.md "wikilink")[5月4日](https://ja.wikipedia.org/wiki/5月4日 "wikilink")、バージョン3.8を公開
  - [2019年](../Page/2019年.md "wikilink")[8月18日](../Page/8月18日.md "wikilink")、メジャーバージョンアップ、バージョン4.0を公開\[19\]

## 脚注

## 関連項目

  - [FTP](../Page/File_Transfer_Protocol.md "wikilink")
  - [FTPクライアント](../Page/FTPクライアント.md "wikilink")

## 外部リンク

  - : Ver.3以降

  - : Ver.2系

  - [Sota's Web Page](http://www2.biglobe.ne.jp/~sota/) : Ver.1系

[Category:FTPクライアント](https://ja.wikipedia.org/wiki/Category:FTPクライアント "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink") [Category:1997年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1997年のソフトウェア "wikilink")

1.  [FFFTP 1.98リリース](https://ja.osdn.net/projects/ffftp/wiki/Release_FFFTP-1.98)
2.  [FFFTP 1.98a以前に存在する脆弱性について（2011年10月28日）](https://ja.osdn.net/projects/ffftp/wiki/Security_200111028)
3.
4.
5.  [10年目 Sotaの雑記-ウェブリブログ](http://jun-sota.at.webry.info/200710/article_1.html)
6.  [OSP_Report OSP2002](http://www.iajapan.org/osp/osp2002.html)
7.  [窓の杜 - 【NEWS】定番FTPクライアントソフト「FFFTP」にディレクトリトラバーサルの脆弱性](http://www.forest.impress.co.jp/article/2008/06/03/ffftpweakness.html)
8.  [窓の杜 - 【NEWS】「FFFTP」のパスワードが“Gumblar”ウイルスにより抜き取られる問題が発生](http://www.forest.impress.co.jp/docs/news/20100130_346056.html)
9.  [Sota's Web Page (GumblarによるFFFTPへの攻撃について)](http://www2.biglobe.ne.jp/~sota/ffftp-vulnerability.html)
10. [FFFTPに注意\! 作者がGumblar対策を喚起 - すでにFFFTPに対する攻撃報告も | エンタープライズ | マイナビニュース](http://news.mynavi.jp/news/2010/02/01/045/)
11. [Sota's Web Page (FFFTP)](http://www2.biglobe.ne.jp/~sota/ffftp.html)　2010年1月30日更新時点
12.
13. [開発終了 Sotaの雑記-ウェブリブログ](http://jun-sota.at.webry.info/201108/article_6.html)
14. [JVN\#62336482: FFFTP における実行ファイル読み込みに関する脆弱性](http://jvn.jp/jp/JVN62336482/)
15. [JVN\#94002296: FFFTP における実行ファイル読み込みに関する脆弱性](http://jvn.jp/jp/JVN94002296/)
16.
17.
18.
19.