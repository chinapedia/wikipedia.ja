> この記事は[Readahead](https://ja.wikipedia.org/wiki/Readahead)から翻訳されています。


**Readahead**は、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")のシステムコールで、ファイルの内容をページキャッシュに読み込む。これは、順次アクセスされたファイルをプリフェッチし、そのコンテンツを、[HDD](https://ja.wikipedia.org/wiki/HDD "wikilink")よりも[RAM](https://ja.wikipedia.org/wiki/RAM "wikilink")から読み込まれるようする。これはファイルアクセスのレイテンシを低くする\[1\]\[2\]。

多くの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")は、一般よく使われるファイルのリストについてのreadaheadを起動高速化のために用いている。そのような構成では、[カーネル](../Page/カーネル.md "wikilink")がprofileブートパラメータとともにブートしたら、ブート中の全てのファイルアクセスが記録され、後のブートシークエンスで読み込まれるファイルの新しいリストが作られる。これは、追加のインストールされたサービスを高速に開始する。なぜなら、これらのサービスは、デフォルトのreadaheadのリストに含まれていないからである\[3\]。

[systemd](https://ja.wikipedia.org/wiki/systemd "wikilink")を用いるLinuxディストリビューションでは、readaheadのバイナリは（ブートシークエンスの一部としては）systemd-readaheadに置き換えられている\[4\]。しかしながら、systemdのバージョン 217で、readaheadのサポートは除去された。これは、メンテナンスされておらず、期待されるパフォーマンスの利益を提供できていないことによるとされる\[5\]。

現在、実験的なページレベルのシステムのプリフェッチが、さらにパフォーマンスを向上させるために開発されている\[6\]。

## 脚注

### 出典

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")

1.
2.
3.
4.
5.
6.