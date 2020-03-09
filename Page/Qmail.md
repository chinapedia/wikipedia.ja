> この記事は[Qmail](https://ja.wikipedia.org/wiki/Qmail)から翻訳されています。


**qmail**（キューメイル）は、[ダニエル・バーンスタイン](https://ja.wikipedia.org/wiki/ダニエル・バーンスタイン "wikilink")により開発された[メール転送エージェント](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink") (MTA)。[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) で動作する。現在の最新バージョンは[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[6月15日](https://ja.wikipedia.org/wiki/6月15日 "wikilink")にリリースされた**1.03**。

## 特徴

複雑化により[セキュリティホール](https://ja.wikipedia.org/wiki/セキュリティホール "wikilink")が頻発した[Sendmail](../Page/Sendmail.md "wikilink")とは異なり、高速で、非常にシンプルかつ堅牢な構造を目指して作成された。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")から公開されているが、運用上問題となる点は[DoS攻撃](https://ja.wikipedia.org/wiki/DoS攻撃 "wikilink")に対する脆弱性（[リソース制限で回避可能](https://ja.wikipedia.org/wiki/計算資源 "wikilink")）のみで、その他に発見されたセキュリティホールはない。ちなみに、セキュリティホールを発見すると500ドルの[賞金がもらえる](https://ja.wikipedia.org/wiki/懸賞金 "wikilink")。

設定に関しても、難解で煩雑なsendmailに対し、1[ファイル](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")1設定で簡素である。[インストール](https://ja.wikipedia.org/wiki/インストール "wikilink")した時点で[オープンリレーができないようになっている](https://ja.wikipedia.org/wiki/不正中継 "wikilink")。

メールボックスの形式は、堅牢さから独自に設計された[Maildir](https://ja.wikipedia.org/wiki/Maildir "wikilink")形式がデフォルトで、またそれが推奨されている。ただし、[mbox](https://ja.wikipedia.org/wiki/mbox "wikilink")で運用することも可能である。

[バーチャルホスト](https://ja.wikipedia.org/wiki/バーチャルホスト "wikilink")などを実現するための[ユーティリティとしての](https://ja.wikipedia.org/wiki/ユーティリティソフトウェア "wikilink")、[vpopmail](https://ja.wikipedia.org/wiki/vpopmail "wikilink")など、様々な周辺ツールがあるが、原作者による開発が事実上終了しており、最新のOSでの[コンパイルや](../Page/コンパイラ.md "wikilink")、[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS "wikilink")等、qmail開発当時にはなかった規格に対応しようとすると、非公式の[パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")を探して当てなければならず、構築を複雑なものとしている。

他の一般的なMTAは、宛先不明のメールは受け取りを拒否するのに対し、qmailは、一旦受け取った後、差出人（エンベロープFrom）に送り返す動作をする。このため、[スパムメール等の詐称に利用された第三者に大量のリターンメールを送信し](https://ja.wikipedia.org/wiki/スパム_\(メール\) "wikilink")、**backscatter**（後方拡散）または**collateral spam**（巻き添えスパム）と呼ばれる二次被害を起こすことがある。

また、改行コードの扱いについても[RFCに準拠しない動作をする問題がある](../Page/Request_for_Comments.md "wikilink")\[1\]。

### ライセンス

qmailは長らく[ソースコード](../Page/ソースコード.md "wikilink")の状態で配布が許され、コンパイル済みの状態で配布される場合には、 [ディレクトリ](https://ja.wikipedia.org/wiki/ディレクトリ "wikilink")構成を変更しないなど定められた条件に合致した場合のみ配布が許され、 各OSでの独自の[ソフトウェアパッケージ](https://ja.wikipedia.org/wiki/ソフトウェアパッケージ "wikilink")を作成することは困難であった。

その後、2007年11月30日にダニエル・バーンスタインはqmailを[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")に置くことを宣言した \[2\]\[3\]。 しかし作者は依然として、[プログラムを](https://ja.wikipedia.org/wiki/プログラム_\(コンピュータ\) "wikilink")/var/qmail以下に配置するなど、[インタフェースをオリジナルと一致させることを推奨している](https://ja.wikipedia.org/wiki/インタフェース_\(情報技術\) "wikilink")。

## 参考文献

## 関連項目

  - [daemontools](https://ja.wikipedia.org/wiki/daemontools "wikilink")

## 外部リンク

  - [qmail](http://cr.yp.to/qmail.html)
  - [netqmail](http://www.qmail.org/netqmail/)

[Category:メール転送エージェント](https://ja.wikipedia.org/wiki/Category:メール転送エージェント "wikilink") [Category:メール配送エージェント](https://ja.wikipedia.org/wiki/Category:メール配送エージェント "wikilink")

1.
2.
3.