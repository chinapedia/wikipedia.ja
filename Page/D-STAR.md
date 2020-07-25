> この記事は[D-STAR](https://ja.wikipedia.org/wiki/D-STAR)から翻訳されています。


**D-STAR**（）とは、[日本アマチュア無線連盟](../Page/日本アマチュア無線連盟.md "wikilink")が開発した音声モードとデータモードとをもつ[デジタル](../Page/デジタル.md "wikilink")化された[アマチュア無線](../Page/アマチュア無線.md "wikilink")通信網である。従来と同様の無線機同士直接の通信又は[レピータ](https://ja.wikipedia.org/wiki/レピータ "wikilink")を介した通信の他に、レピータ間の中継ができるよう設計されているなどの特徴がある。

D-STAR方式のレピータを、ここではデジタルレピータと書く。

## モード

通信モードには、DV（Digital Voice：デジタル音声）モードとDD（Digital Data：デジタルデータ）モードとの2種類がある。 [電波型式](https://ja.wikipedia.org/wiki/電波型式 "wikilink")は、F7Wである。

### DVモード

VHF・UHF帯を使用し、音声を[AMBE](https://ja.wikipedia.org/wiki/AMBE "wikilink")（米[デジタルボイスシステムズ](https://ja.wikipedia.org/wiki/デジタルボイスシステムズ "wikilink")社（Digital Voice Systems, Inc.、略称DVSI）が開発した高度マルチバンド励振方式：「Advanced Multi-Band Excitation」の略）で2.4kbpsに[符号化し](https://ja.wikipedia.org/wiki/音声符号化 "wikilink")、[GMSK](https://ja.wikipedia.org/wiki/GMSK "wikilink")（Gaussian filtered Minimum Shift Keying、[ガウス最小偏移変調](https://ja.wikipedia.org/wiki/最小偏移変調 "wikilink")）で[変調して占有周波数帯幅](../Page/デジタル変調.md "wikilink")6kHzで送信するモードである。DVモードでは、音声の伝送と同時に4.8kbpsの低速デジタルデータ送信が可能である（後述のDDモードの上に[イーサネット](../Page/イーサネット.md "wikilink")電話又は[IP電話](../Page/IP電話.md "wikilink")を乗せているものではない）。

### DDモード

1200MHz帯を使用する、占有周波数帯幅150kHzで速度128kbpsのデジタルデータ通信モードである。[イーサネット](../Page/イーサネット.md "wikilink")フレームを透過的に流すことができる。DDモード対応トランシーバ（市販モデルとして[アイコム](../Page/アイコム.md "wikilink")のID-1）はイーサネット接続が必要である。

[前方誤り訂正](../Page/前方誤り訂正.md "wikilink")が含まれていないため、データエラーには上位層が再送を行うことによって対応する。そのため、[マルチパス](../Page/マルチパス.md "wikilink")等によって[エラーレートが上がると](../Page/符号誤り率.md "wikilink")[輻輳](../Page/輻輳.md "wikilink")が生じて伝送速度が著しく低下するという問題がある。

市販モデルとしては[アイコム](../Page/アイコム.md "wikilink")のIC-9700がDDモードに対応している。（ID-1は、2014年に生産終了）

## 中継

デジタルレピータ局間は、5GHzまたは10GHz帯レピータアシスト局による10M[bpsの](../Page/ビット毎秒.md "wikilink")[非同期転送モード](https://ja.wikipedia.org/wiki/データ転送 "wikilink")（[ATM](../Page/Asynchronous_Transfer_Mode.md "wikilink")）回線（アシスト回線という）、もしくはレピータに接続された[ゲートウェイ](../Page/ゲートウェイ.md "wikilink")と呼ばれる[ホストPC間の](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")[インターネット](../Page/インターネット.md "wikilink")接続により中継ができる。DDモード上の[TCP/IPについては](../Page/インターネット・プロトコル・スイート.md "wikilink")、ゲートウェイから外部の[インターネット](../Page/インターネット.md "wikilink")へも接続できる。

## 従来のアマチュア無線におけるパケット通信との互換性

ターミナルノードコントローラを利用する従来の[パケット通信 (アマチュア無線)](../Page/パケット通信_\(アマチュア無線\).md "wikilink") とはインタフェースが異なるため、相互利用はできない。従来のパケット通信でもTCP/IP通信がおこなわれていたが、そちらはAX.25（[:en:AX.25](https://ja.wikipedia.org/wiki/:en:AX.25 "wikilink")）にIPを乗せたものであり、D-STARのDDモードはイーサネットであるため直接の相互運用はできず、レイヤ3（IPの層、[ネットワーク層](../Page/ネットワーク層.md "wikilink")）を通す必要がある。

## 利用

ローカル局同士直接のデジタル音声・デジタルデータ通信も可能であるが、ローカル局の無線機からデジタルレピータを経由して相手先の無線局又は更にアシスト回線、ゲートウエイ局経由のインターネット回線などのデジタル幹線網を経由して別のデジタルレピータを経由して相手先の無線局と通信する、という利用法が広く行われている。

応用として、DVモードのデジタル音声通信と同時に[GPSとDVモードの](../Page/グローバル・ポジショニング・システム.md "wikilink")4.8kbpsデジタルデータ通信機能を利用して、位置情報をリアルタイムに交換しあう通信方法が利用されている。

2006年9月以降に周波数などが再編成され、430MHzでのDVのレピータ局も増設された。D-STARのレピータは、当初、日本国内(G1＝第一世代）だけだったが、珍しく日本発の規格が欧米に広がり世界規模のアマチュア無線デジタル網に育った。2015年現在、世界のレピータ数：1000程度、日本国内：160以上と、後発の欧米のレピータは世界のレピータ群串刺しの反射板（レフレクタ、Reflector）と接続できるなど仕様が新しい（G2=第二世代）。

## 歴史

  - 1998年　[郵政省](../Page/郵政省.md "wikilink")からの依託により、[日本アマチュア無線連盟](../Page/日本アマチュア無線連盟.md "wikilink")が「アマチュア無線へのデジタル技術導入に関する調査検討」プロジェクト開始。
  - 2001年　日本アマチュア無線連盟の次世代通信委員会が中心となりD-STARシステムの実験局免許を取得、実用化実験を開始。
  - 2002年　[アマチュア無線フェスティバル](../Page/アマチュア無線フェスティバル.md "wikilink")での展示・デモ通信を実施。
  - 2004年　総務省省令等の改正により、[日本アマチュア無線連盟](../Page/日本アマチュア無線連盟.md "wikilink")によるD-STARシステムの運用開始。当初は関東、東海、関西の3地域のレピータで開始。
  - 2005年　レピータ開設募集開始。

## 関連項目

  - [WIRES-X](https://ja.wikipedia.org/wiki/WIRES-X "wikilink")
  - [WiRES-II](https://ja.wikipedia.org/wiki/WiRES-II "wikilink")
  - [Echolink](https://ja.wikipedia.org/wiki/Echolink "wikilink")

## 外部リンク

  - [JARL D-STAR プロジェクト](http://www.jarl.com/d-star/) - D-STAR の基礎知識から技術資料まで紹介されている。
  - [東海地方（2エリア）D-STAR 協議会（D-STAR2）](http://isotope.sist.chukyo-u.ac.jp/dstar2/) - D-STAR について積極的なアマチュア無線家の団体。D-STAR の紹介、全国の D-STAR レピータの一覧、D-STAR [ロール・コール](https://ja.wikipedia.org/wiki/ロール・コール "wikilink")の情報等が掲載されているほか、中京大学情報理工学部によるD-STAR [メーリング・リストの運営も行っている](../Page/メーリングリスト.md "wikilink")。
  - [アイコム デジタルトランシーバ ID-1 使用レポート](http://isotope.sist.chukyo-u.ac.jp/dstar2/ID-1/) - アマチュア無線家 7L1FFN によるレポート。DD モード、DV モードを含む、設定方法や交信方法が書かれている。

[Category:アマチュア無線](https://ja.wikipedia.org/wiki/Category:アマチュア無線 "wikilink") [Category:モバイルネットワーク](https://ja.wikipedia.org/wiki/Category:モバイルネットワーク "wikilink")