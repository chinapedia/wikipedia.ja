> この記事は[拡張機能 \(Mozilla\)](https://ja.wikipedia.org/wiki/拡張機能_\(Mozilla\))から翻訳されています。


[Mozillaのソフトウェアにおける](../Page/Mozilla_Foundation.md "wikilink")[拡張機能](https://ja.wikipedia.org/wiki/拡張機能 "wikilink")とは、[Mozilla Firefoxや](../Page/Mozilla_Firefox.md "wikilink")[Mozilla Thunderbirdなどで利用できる](../Page/Mozilla_Thunderbird.md "wikilink")[アドオン](https://ja.wikipedia.org/wiki/アドオン "wikilink")のうち、ソフトウェアに機能を追加したり、既存の機能を変更したりするものである\[1\]。

## 概要

拡張機能は[Mozilla Foundation製の](../Page/Mozilla_Foundation.md "wikilink")[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")（[Firefox for Mobile含む](https://ja.wikipedia.org/wiki/Firefox_for_Mobile "wikilink")）や[Mozilla Thunderbirdのほか](../Page/Mozilla_Thunderbird.md "wikilink")、これらと協調して有志により開発されている[SeaMonkey](../Page/SeaMonkey.md "wikilink")などに対して主に設定や操作の機能強化を行うものである。また同じ仕組みを利用してテーマ（[スキン](../Page/スキン_\(GUI\).md "wikilink")）も提供することができる。また、拡張機能には[セキュリティ](https://ja.wikipedia.org/wiki/セキュリティ "wikilink")[修正パッチとして作成されるものや英語版しか出ていないソフトウェアに対する日本語化パックとして配布されるものもある](../Page/パッチ.md "wikilink")。

## 歴史

2015年以前のFirefoxでは、「寛容なアドオンモデル」が採用されていた。これは、[XUL](../Page/XUL.md "wikilink")や[XPCOM](../Page/XPCOM.md "wikilink")といった技術によってFirefoxの内部にアクセスし、[ユーザーインターフェイス](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")を大きく変えてしまうような大きな柔軟性をもたらすものだった。しかしそれは、Firefoxの内部構造に依存しすぎており、Firefoxのバージョンアップによって使用できなくなったり、クラッシュやパフォーマンスの低下を起こしたりする可能性があった。さらに、Firefoxのマルチプロセス化（e10s）のような新技術の導入を阻害することも問題となっていた\[2\]。

そこで[Mozillaは](../Page/Mozilla_Foundation.md "wikilink")、2015年8月21日にFirefoxのアドオンをWebExtensions\[3\]に置き換えていく方針を明らかにした。WebExtensionsは[Blinkのアドオンと互換性が高く](https://ja.wikipedia.org/wiki/Blink_\(レンダリングエンジン\) "wikilink")、Blinkのものを簡単に移植できる\[4\]。この移行には否定的な声も少なくなかったが\[5\]、Mozillaは2017年11月14日リリースの「Firefox Quantum（Firefox 57）」ですべてのレガシーアドオンを廃止した\[6\]。延長サポート版であるFirefox ESRはバージョン52まで対応していたが、2018年9月5日まででサポート終了となりESR 60以降はレガシーアドオンが廃止された\[7\]。なお、Firefoxから派生した[Waterfox](https://ja.wikipedia.org/wiki/Waterfox "wikilink")と[Pale Moonは](https://ja.wikipedia.org/wiki/Pale_Moon "wikilink")、レガシーアドオンのサポートを続けている\[8\]\[9\]。

一方、Thunderbirdでは2018年3月リリースのThunderbird 59でもレガシーアドオンのサポートが継続されるが、コアエンジンの更新や仕様変更によって使用できなくなるものもありうる\[10\]。Thunderbird 68 以降向けには MailExtensions（WebExtensionsに Thunderbird 向けの機能を追加したもの\[11\]）を利用してアドオンを構築することが推奨 (should) とされている。[2020年](../Page/2020年.md "wikilink")[6月](../Page/6月.md "wikilink")付近リリース予定の Thunderbird 78では MailExtensions でのレガシー機能サポートが廃止される予定\[12\]。

## 技術

2015年にMozillaがアドオンをWebExtensionsに移行させることを発表する前には\[13\]、[XUL](../Page/XUL.md "wikilink")/[XPCOM](../Page/XPCOM.md "wikilink")オーバーレイ、ブートストラップ型拡張機能、Add-on SDKを利用した開発方法が存在した。しかし、WebExtensionsが採用されるようになってからは、それらの技術を利用したアドオンは廃止されることになった。WebExtensionsはクロスブラウザで動作可能なアドオンを開発するための技術で、[Google Chromeや](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")のextension APIと互換性があり、わずかな変更だけでFirefoxでも動作させることができる。WebExtensionsは[JavaScript](../Page/JavaScript.md "wikilink")、[HTML](https://ja.wikipedia.org/wiki/HTML "wikilink")、[CSSなどの開発者が使い慣れたWebベースの技術を使用して作成されている](../Page/Cascading_Style_Sheets.md "wikilink")。Webページ上のJavaScriptと同じWeb APIを活用できるが、拡張機能は独自のJavaScript APIセットにもアクセスできる\[14\]\[15\] 。

## インストールと管理

拡張機能を利用するにはユーザーが各自[Mozilla Add-onsのような任意のサイトから配布されている拡張機能をダウンロードし](../Page/Mozilla_Add-ons.md "wikilink")、インストールすることが必要となる。インストールには[XPInstall](../Page/XPInstall.md "wikilink")モジュールを用いることでユーザーはインストールを許可するだけで自動的にインストールが完了するようになっている。

拡張機能はアドオンマネージャを用いて管理する。拡張機能にアップデートの提供元が記述されているとき、自動的にアップデートが無いかをチェックする。特にブラウザのバージョンアップをしたときは互換性チェックを再度行い、不合格である拡張機能は無効化される。アドオンマネージャから直接 Mozilla Add-ons に登録された拡張機能を検索し、インストールすることもできるようになっている。

拡張機能のインストールにはその拡張機能がインストールしたいブラウザに対応していることが条件であり、標準ではインストール直前にブラウザのバージョンチェックが行われる。ブラウザとの互換性チェックはその拡張機能で設定されたバージョンの範囲にインストールするブラウザのバージョンが含まれているかどうかで調べるため、公式には対応が謳われていない拡張機能でもその情報さえ弄れば動作してしまう場合もある。Firefox 5以降で採用されたラピッドリリースへの対応のため、Firefox 10以降相当のブラウザではアドオンの最高対応バージョンがFirefox 4以降であればそのブラウザに対応しているものとみなしてインストールされるようになった\[16\]。

## 拡張機能が登場した背景

Firefoxの登場以前に開発されていた[Mozilla Suiteではソフトウエア本体に様々な機能追加を行ったため](https://ja.wikipedia.org/wiki/Mozilla_Suite "wikilink")、開発が進むに従い[ソフトウェアの肥大化](https://ja.wikipedia.org/wiki/ソフトウェアの肥大化 "wikilink")や[バグ](../Page/バグ.md "wikilink")の増加をもたらした。次世代ブラウザであるFirefoxやThunderbirdではこのような事態を避けるため、高い拡張性を残しながらもソフトウェアのサイズを小さいものにとどめる方法として、機能追加は拡張機能で行うよう方針が改められた。

## プラグインとの違い

拡張機能はブラウザそのものの機能を拡張するのに対し、プラグインは[Flashのような](../Page/Adobe_Flash.md "wikilink")[グラフィック](../Page/グラフィック.md "wikilink")[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")への対応を強化するもので、ブラウザそのものの機能には影響を与えない。

### 窓の杜「プラグイン」問題

事の発端は[2005年](../Page/2005年.md "wikilink")[2月17日](../Page/2月17日.md "wikilink")に掲載された[窓の杜](../Page/窓の杜.md "wikilink")の『「Firefox」プラグイン特集』という記事\[17\]である。編集部が“拡張機能”という言葉が一般に認識されにくい、IEなど他製品で言う“プラグイン”と同じものであるとして意識して欲しいなどの理由から、記事の中で“プラグイン”という表記を取った。（しかしIEの機能拡張プログラムは「アドオン」と呼ばれており、窓の杜もそれを肯定しているため既に主張が破綻しているとの指摘がある\[18\]）。

しかしこの表記がユーザーの混乱を招くとして懸念され、[Bugzilla](../Page/Bugzilla.md "wikilink")-jpにはバグとして登録される\[19\]まで問題が発展した。

このことについて国内の拡張機能開発者Piroらは以下のような点が問題だと述べている。

  - ユーザーが拡張機能を「プラグイン」として認識してしまうと検索などで拡張機能を探し出すことが困難となる。
  - 用語の浸透度が逆転すると本来の「プラグイン」の情報が「プラグインとして認識された拡張機能」の情報に埋もれてしまい、本来の「プラグイン」を検索したいユーザーや開発者を翻弄させる。

この問題は1年近く議論されていたが、窓の杜の2006年3月23日の記事\[20\]で編集部は「今後“プラグイン”と“拡張機能”を区別して表記する」と書いたため問題は終結した。

その後MozillaはFirefox 2.0のリリース以降ソフトウェアの画面や公式ページで拡張機能やテーマをまとめて「アドオン」としており、拡張機能は「アドオン」とも呼ばれるようになっている。

## 主な拡張機能の種類

  - 機能を追加し、向上させるもの
      - [Mozilla Suiteの機能と同等の働きをするもの](https://ja.wikipedia.org/wiki/Mozilla_Suite "wikilink") - [ChatZilla](../Page/ChatZilla.md "wikilink")、[Eメール](https://ja.wikipedia.org/wiki/Eメール "wikilink")、[ニュースリーダーなど](../Page/ネットニュース.md "wikilink")。
      - [ブラウジング](https://ja.wikipedia.org/wiki/ブラウジング "wikilink")性能の向上 - [Tab Mix Plusなど](https://ja.wikipedia.org/wiki/Tab_Mix_Plus "wikilink")。
      - ブックマークなどの[データの同期](../Page/ファイル同期.md "wikilink") - 標準機能である[Firefox Syncに近い](https://ja.wikipedia.org/wiki/Firefox_Sync "wikilink")。
      - [検索プラグイン](https://ja.wikipedia.org/wiki/検索プラグイン "wikilink") - Mozillaでは検索ツールなどと呼ぶ
      - [ツールバー](https://ja.wikipedia.org/wiki/ツールバー "wikilink") - 検索プラグインとは異なる。
    <!-- end list -->
      -
        など

<!-- end list -->

  - 開発・[デバッグツール](../Page/バグ.md "wikilink")
      - [DOM Inspector](../Page/DOM_Inspector.md "wikilink") - ウェブページや
      - [Firebug](../Page/Firebug.md "wikilink")
  - ウェブページの見た目を変更するもの
      - [Adblock Plus](https://ja.wikipedia.org/wiki/Adblock_Plus "wikilink")
      - [AutoPagerize](https://ja.wikipedia.org/wiki/AutoPagerize "wikilink")
      - [NoScript](../Page/NoScript.md "wikilink")
      - [Stylish](https://ja.wikipedia.org/wiki/Stylish "wikilink")
      - [uBlock Origin](https://ja.wikipedia.org/wiki/uBlock_Origin "wikilink")
    <!-- end list -->
      -
        など

<!-- end list -->

  - 全く無意味であるもの（[ジョークソフト](../Page/ジョークプログラム.md "wikilink")）
      - 中止ボタンがしいたけに見えて困る
    <!-- end list -->
      -
        など。

## 他のブラウザにおける類似の機能

[Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")のextension APIは、WebExtensionsと互換性がある。また、WebExtensionsは[Microsoft Edgeでも動作する](https://ja.wikipedia.org/wiki/Microsoft_Edge "wikilink")\[21\]。

## 脚注

## 関連項目

  - [Greasemonkey](../Page/Greasemonkey.md "wikilink") - 機能を向上させるための[スクリプトの実行環境を追加する](../Page/スクリプト言語.md "wikilink")。

## 外部リンク

  - [addons.mozilla.org - Firefox 向けアドオン](https://addons.mozilla.org/ja/firefox/)
  - [mozilla developer center:Extensions](http://developer.mozilla.org/ja/docs/Extensions)

[en:Add-on (Mozilla)](https://ja.wikipedia.org/wiki/en:Add-on_\(Mozilla\) "wikilink")

[Category:拡張機能_(Mozilla)](https://ja.wikipedia.org/wiki/Category:拡張機能_\(Mozilla\) "wikilink") [Category:Mozilla](https://ja.wikipedia.org/wiki/Category:Mozilla "wikilink") [Category:ソフトウェア](https://ja.wikipedia.org/wiki/Category:ソフトウェア "wikilink")

1.
2.
3.  <https://wiki.mozilla.org/WebExtensions>
4.
5.
6.
7.
8.
9.
10.
11. <https://developer.thunderbird.net/add-ons/about-add-ons>
12. <https://developer.thunderbird.net/add-ons/tb78>
13.
14. [What are extensions? - Mozilla | MDN](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/What_are_WebExtensions)
15.
16.
17.
18. <http://www.d-toybox.com/studio/weblog/show.php?mode=single&id=2006031300>
19. <http://bugzilla.mozilla.gr.jp/show_bug.cgi?id=5052>
20.
21.