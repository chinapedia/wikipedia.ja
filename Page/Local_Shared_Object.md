> この記事は[Local Shared Object](https://ja.wikipedia.org/wiki/Local_Shared_Object)から翻訳されています。


**Local Shared Object**（ローカル・シェアード・オブジェクト、**LSO**）とは[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")の[Flash Player](../Page/Adobe_Flash.md "wikilink") がユーザーPCの内部に保存するデータ形式である\[1\]。 データは、[HTTP cookieのような使用法であることから](https://ja.wikipedia.org/wiki/HTTP_cookie "wikilink")「Flashクッキー」とも呼ばれ\[2\]、ブラウザの[クッキーのようにサイト毎の情報を保持する](https://ja.wikipedia.org/wiki/HTTP_cookie "wikilink")。 Macromedia Flash MX (Flash Player 6) 以降で実装されている。

## セキュリティの問題

LSOは[サンドボックスのセキュリティモデルに基づいて作成されている](https://ja.wikipedia.org/wiki/サンドボックス_\(セキュリティ\) "wikilink")。Adobe Flash Playerは[ウェブサイト](../Page/ウェブサイト.md "wikilink")や[ドメインごとにLSOを自動的に保存する](../Page/ドメイン名.md "wikilink")。 LSOはプライバシー問題を含むデータを持つこともありえるが、Cookieのようにテキスト形式で保存されるため可読性が高い。 また、LSOはテンポラリファイルではなく通時的に保存される。

このようなことからセキュリティ上問題があると考えられており、アドビも対策を2つ提供している。1つめはFlashPlayer再生中に右クリック後設定を選択し、現在見ているサイトのローカル記憶領域を0にする方法。2つめは、アドビのグローバル設定サイトから全体の設定([1](http://www.macromedia.com/support/documentation/jp/flashplayer/help/settings_manager03.html))をする方法である。

## プライバシー問題

LSOはcookieと同じように使用できることから、マーケティングに利用されるケースもある\[3\]が、cookieほど有名ではないため、気づかないで利用している人も多い。LSOはcookieと違い有効期限がないため、情報が消えることが無いことも問題である。

## 製品ごとのLSOファイルの置き場所

LSOファイルは製品ごとに異なる場所に保存される（通常設定時）。

| 製品                                                                    | ディレクトリ                                                                  | 拡張子 |
| --------------------------------------------------------------------- | ----------------------------------------------------------------------- | --- |
| [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") | `%USERPROFILE%\Application Data\Macromedia\Flash Player\#SharedObjects` | SOL |
| [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")               | `~/Library/Preferences/Macromedia/Flash Player`                         |     |
| [MacBook Air](https://ja.wikipedia.org/wiki/MacBook_Air "wikilink")   | `/Library/Preferences/[アプリケーションのパッケージ名(ID)]`                            |     |
| [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")               | `~/.macromedia`                                                         |     |

## 確認されている不具合

Flash Player 10において、64KB以上のデータが読み込めない不具合が存在する\[4\]。 そのため、Flash Player 10でLSOを使用する際には容量を64KB未満に抑えなければならないため注意が必要である。 2009年7月30日以降のFlash Playerでは、この不具合は修正されている。

## ソフトウェア

LSO関連ソフトは性質上2つの観点で作成されている。1つはセキュリティ観点からLSOを削除、書き出し制限をつけるもの。もう1つはLSOを閲覧、編集するものである。

### セキュリティ関連ソフト

  - [Objection](http://objection.mozdev.org/)\[5\]\[6\] :[Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")の[拡張機能](https://ja.wikipedia.org/wiki/拡張機能_\(Mozilla\) "wikilink")。LSOの削除が行える
  - [CCleaner](../Page/CCleaner.md "wikilink"): レジストリ最適化ソフト。LSOの削除が行える
  - Sandboxie: サンドボックス用のセキュリティソフト

### 閲覧編集ソフト

  - SolVE
  - .sol Editor
  - Dojo Toolkit
  - MAXA Cookie Manager
  - PyAMF
  - SOLReader
  - s2x

## 脚注

## 関連項目

  - [Adobe Flash](../Page/Adobe_Flash.md "wikilink")
  - [サンドボックス (セキュリティ)](https://ja.wikipedia.org/wiki/サンドボックス_\(セキュリティ\) "wikilink")
  - [HTTP cookie](https://ja.wikipedia.org/wiki/HTTP_cookie "wikilink")
  - [マジッククッキー](https://ja.wikipedia.org/wiki/マジッククッキー "wikilink")

[Category:Adobe_Flash](https://ja.wikipedia.org/wiki/Category:Adobe_Flash "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:セキュリティ技術](https://ja.wikipedia.org/wiki/Category:セキュリティ技術 "wikilink")

1.
2.
3.
4.
5.
6.