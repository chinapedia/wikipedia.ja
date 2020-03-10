> この記事は[OpenNTPD](https://ja.wikipedia.org/wiki/OpenNTPD)から翻訳されています。


**OpenNTPD**は、NTP（[Network Time Protocol](../Page/Network_Time_Protocol.md "wikilink")）を利用して計算機の時間を合わせる[ソフトウェア](../Page/ソフトウェア.md "wikilink")で、安全性を考慮して開発され、[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")で公開されている。 OpenNTPDはNTP[サーバ](../Page/サーバ.md "wikilink")と同期して時間を合わせる機能だけでなく、NTPサーバとしても振る舞うことが出来る。 OpenNTPDは初期の頃は[OpenBSD](../Page/OpenBSD.md "wikilink")プロジェクトの一部としてHenning Brauerが開発していた。 Darren Tuckerにより他の様々な[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で利用できるようにする開発がされてからは、[OpenSSH](https://ja.wikipedia.org/wiki/OpenSSH "wikilink")のようにOpenBSDのサブプロジェクトになっている。この移植版リリースには、OpenSSH と同じくバージョン番号に Portable release を表す **p** がつけられている。

## 歴史

OpenNTPDは既存のNTP[デーモンの問題を解決するために開発された](../Page/デーモン_\(ソフトウェア\).md "wikilink")。既存のNTPデーモンには設定が難しいという問題、プログラムが正常に動くかを調べるのが難しいという問題、ライセンス上の問題があった。\[1\] OpenNTPDはこれらの問題を解決するために開発され、最初は 2004年11月2日にリリースされた[OpenBSD](../Page/OpenBSD.md "wikilink") 3.6 と一緒に配布された。

## 目的

OpenNTPDは適度な正確さを保ちつつ、安全で、プログラムの安全性を調査しやすく、設定しやすく、少ないメモリしか消費しない[NTP](../Page/Network_Time_Protocol.md "wikilink")[デーモンとして開発されている](../Page/デーモン_\(ソフトウェア\).md "wikilink")。 安全性はネットワークからの入力に対してしっかりと正当性を調査することや[strlcpy](https://ja.wikipedia.org/wiki/strlcpy "wikilink")を用いたバッファー操作、潜在的なセキュリティーホールの影響を小さくする特権分離により達成されている。 設定しやすさは、他のNTPで提供しているものよりも少ない典型的な機能しか実装しないことで実現している。 実際、OpenNTPDの設定として必要なものはOpenNTPDが待ち受けるIPアドレスとホスト名、利用する時間計測デバイス、同期をとるサーバぐらいである。

## 評判

OpenNTPDにはthe Network Time Protocol project\[2\]で開発されたNTPデーモンに比べて精度が低いという評価がある。\[3\] OpenNTPDプロジェクトはプログラムの単純さと安全さのためにマイクロ秒単位の正確さを犠牲にしていると、この評価を認めている。

## 参考文献

## 外部リンク

  -
[Category:OpenBSD](https://ja.wikipedia.org/wiki/Category:OpenBSD "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:時間に関するネットワークソフト](https://ja.wikipedia.org/wiki/Category:時間に関するネットワークソフト "wikilink")

1.  [OpenNTPD 目標](http://www.openntpd.org/ja/goals.html)
2.  [the Network Time Protocol project](http://www.ntp.org/)
3.  The OpenBSD Networking FAQ: [6.12.1 - "But OpenNTPD isn't as accurate as the ntp.org daemon\!"](http://www.openbsd.org/faq/faq6.html#OpenNTPDaccurate)