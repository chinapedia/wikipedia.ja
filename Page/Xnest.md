> この記事は[Xnest](https://ja.wikipedia.org/wiki/Xnest)から翻訳されています。


[thumbセッション上で](https://ja.wikipedia.org/wiki/画像:KDM-Xnest.jpg "wikilink")、新たな[KDMを表示した](https://ja.wikipedia.org/wiki/KDEディスプレイマネージャ "wikilink") Xnest ウィンドウが表示されている様子\]\] **Xnest** は [X Window System](../Page/X_Window_System.md "wikilink") サーバの一種であり、1つの[ウィンドウ](../Page/ウィンドウ.md "wikilink")内にその出力を表示する。つまり、Xnest は X Window System の画面が1つのウィンドウとして通常の画面上に開けるようになっている。

プロトコルレベルでは、Xnest はホストとなるウィンドウのクライアントのように振る舞い、Xnest のウィンドウ（セッション）内でウィンドウを開くアプリケーションから見ればサーバとして振舞う。

Xnest は他のコンピュータの仮想デスクトップをウィンドウ内で動作させることができる。Xnest はサーバの[デバッグ](../Page/デバッグ.md "wikilink")に使われたり、アプリケーションが各種画面サイズでうまく動作するかのテストに使われる。実際、ユーザーはXnestのウィンドウのサイズを選択でき、それが仮想画面のサイズになる。そのため、[PDAの画面サイズでXnestのウィンドウを起動し](../Page/携帯情報端末.md "wikilink")、アプリケーションがその機器の画面の大きさでうまく機能するかどうかをテストするなどの利用法がある。

## リモートデスクトップへのアクセス

Xnest は他のコンピュータのデスクトップをローカルに表示するのにも使われる。

  - [XDMCPを使うと](../Page/Xディスプレイマネージャ.md "wikilink")、Xnestで他のコンピュータのデスクトップをウィンドウ内で動作させることができる。これは例えば `Xnest :10 -query other_computer_name` などとすればよい。リモートマシンは表示を行いたいマシンからの XDMCP コネクションを受理するよう設定しておく必要がある。
  - また、Xnext をリモートマシン上で動作させ、そのウィンドウをローカルのディスプレイに表示することもできる。つまり、XnestをリモートのXアプリケーションとし、ローカルなXサーバと接続させる（[環境変数](https://ja.wikipedia.org/wiki/環境変数 "wikilink") DISPLAY を設定し、[xauth](https://ja.wikipedia.org/wiki/xauth "wikilink")などを使ってリモートのアプリケーションからの接続を許可する）。そして、そのXnestをリモートマシンのXサーバとして機能させる（`startx -- Xnest -geometry 800x600` などとする）。これには例えば[SSHを使い](../Page/Secure_Shell.md "wikilink")、`ssh -X other_computer_name` などとして接続することで設定する。

さらに、Xnest は普通のXサーバとしても機能するので、リモートでアプリケーションを起動し、それらをローカルのXnestに接続することができる。

## ドライバ版

2011年5月に、xorg.conf で指定して利用する、ドライバ版の xf86-video-nested が公開になり\[1\]、2013年リリース予定の X11R7.8 では単体アプリとしての Xnest は廃止が検討されている\[2\]。

## 関連項目

  - [Virtual Network Computing](https://ja.wikipedia.org/wiki/Virtual_Network_Computing "wikilink") (VNC)

## 参照

## 外部リンク

  - [Xnest manual page](http://www.xfree86.org/4.2.0/Xnest.1.html)

[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")

1.  [PUSH xf86-video-nested - Driver for nesting X-servers](http://lists.x.org/archives/xorg-devel/2011-May/022007.html)
2.  [Releases/7.8](http://www.x.org/wiki/Releases/7.8)