> この記事は[WinFixer](https://ja.wikipedia.org/wiki/WinFixer)から翻訳されています。


**WinFixer**（ウィンフィクサー）とは、インターネット上で蔓延している[マルウェア](../Page/マルウェア.md "wikilink")の一種で、あたかも[コンピュータ](../Page/コンピュータ.md "wikilink")内の問題点を修正するかのごとく、合法を装って偽の警告を行う不審なプログラムのこと。**WinAntiVirus**もしくは、**ErrorSafe**とも呼ばれる。

また、同種のマルウェアに**SystemDoctor**や**DriveCleaner**、**MySearch**などがあり、最近では**KyoiKanshi**（脅威監視）や**HadodoraiBugado**（ハードドライブガード）という新種まで出ている。

## 概要

このプログラムは、警告ダイアログ\[1\]を（主に[ポップアップ](https://ja.wikipedia.org/wiki/ポップアップ "wikilink")で）表示し、ユーザのコンピュータが[ウイルスや](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")[スパイウェア](../Page/スパイウェア.md "wikilink")といった有害なプログラム（マルウェア）に感染しているという偽の情報を流す。この表示でユーザを混乱させ、感染を信じさせた上で、このダイアログを通して強制的にユーザのコンピュータ内にインストールされる。また、ダイアログの他にも、ユーザに対して広告を表示するウィンドウを開き、コンピュータの調子が悪くなってしまったのだと納得させるような掲示を行ったり、誤った診断内容を表示したりする。

このような挙動から、WinFixerおよび類似のアプリケーションは、スパイウェアもしくはマルウェアであるとみなされている。ただし、こういった詐欺的ポップアップ表示とそれに伴う強制ダウンロードというのは、多くのスパイウェアに見られる常套手段である。また、このプログラムに感染すると、コンピュータの動作が重くなるといった被害を受けることがある。

  -  [トレンドマイクロ](../Page/トレンドマイクロ.md "wikilink")社による報告:[ウイルスニュース2006年10月11日付](http://jp.trendmicro.com/jp/threat/security_news/virusnews/article/20070216094135.html?ossl=2)
  -  [シマンテック](../Page/シマンテック.md "wikilink")社による報告:[1](http://securityresponse.symantec.com/avcenter/venc/data/winfixer.html)
  -  [マカフィー](../Page/マカフィー.md "wikilink")社による報告:[2](http://vil.nai.com/vil/Content/v_135733.htm)
  -  [カスペルスキー](../Page/カスペルスキー.md "wikilink")社もこのプログラムをマルウェアと認定している:[3](http://www.kaspersky.com/find?words=winfixer&search=1)
  -  [ソフォス](../Page/ソフォス.md "wikilink")社による報告:[4](http://www.sophos.com/virusinfo/analyses/winfixer.html)
  -  感染してしまったときのための除去プログラム（利用は[自己責任で](https://ja.wikipedia.org/wiki/責任#自己責任 "wikilink")）:[5](http://www.atribune.org/index.php?option=com_content&task=view&id=30&Itemid=2)

WinFixerによるダイアログメッセージの例：

  -
    *WinFixer 2005は、レジストリやドライブのエラーといったコンピュータ内のあらゆる問題をスキャンし、解決することができる便利なソフトウェア（ユーティリティ）です。このプログラムは、ハードディスクの断片化を解消したり、壊れてしまった[ワードや](../Page/Microsoft_Word.md "wikilink")[エクセル](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、または音楽や映像といったファイルを修復する機能で、コンピュータシステムのパファーマンスや安定性を保証します。*

WinFixerは、このような表示を行うが、実際には表示された行為を一切行わない。 （以下、翻訳中）

## 種類

WinFixerには、下記の種類が存在し、その他にも複数の種類が存在していると思われる。

  - WinAntiSpyware
  - ErrorSafe
  - SystemDoctor
  - [WinAntiVirusPro](../Page/WinAntiVirusPro.md "wikilink")
  - DriveCleaner
  - KyoiKanshi
  - SpyAxe

## 感染経路

コンピュータにWinFixerが感染する経路は複数存在するが、[Internet Explorer](../Page/Internet_Explorer.md "wikilink")（以下IE）を使用している場合に最も被害を受けやすい。[Mozilla Firefoxや](../Page/Mozilla_Firefox.md "wikilink")[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")などの他のブラウザである場合、IEよりは感染しにくいが、感染しないとは限らない。また、しばしば[光学ドライブ](../Page/光学ドライブ.md "wikilink")が停止することがある。

### 典型的な例（警告メッセージ）

IEを使用してWebサイトを閲覧中、WinFixerをダウンロードさせようとするページ（必ずしもwinfixer.comでは無く、広告として組み込まれている場合が多い）にアクセスした場合に、Winfixerをインストールするように誘導するダイアログが表示される。

ユーザが「OK」ボタンを押したときだけでなく、「キャンセル」ボタンを押したとき、あるいはウインドウ右上の「×」ボタンを押してダイアログを閉じようとしたときでも、WinFixerは自身をダウンロードしてコンピュータ内部に侵入しようとする。

この警告ダイアログはIEの[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")であり、Windowsタスクのマネージャリストの中に現れない。 この場合、「Altキー+f4キー」（アクティブなウインドウを閉じる）のコマンドを使用するか、またはダイアログを閉じる前にインターネットから切断することにより、この問題を避けることができる。

### 体験版をインストールしてしまう

無料体験版をインストールするように促すポップアップを見て、体験版をインストールしてしまう被害がしばしばある。

体験版をダウンロードして、インストールした場合、（実際にウイルスに感染していなくても）「（複数の）ウイルスが検出されました。隔離・駆除には製品版を購入してください」という趣旨のメッセージを出す。

しかし、実際にはこのプログラムはウイルススキャン自体をまったく行っていない。

WinFixerプログラムがインストールされた場合、[アンチウイルスソフトウェア](../Page/アンチウイルスソフトウェア.md "wikilink")を使用しないと除去ができない（なかには、アンチウイルスソフトウェアの駆除処理を妨害するタイプのものも存在するので注意が必要である）。駆除するまでの間、スクリーン上に、（何もしていなくても）購入を求めるウインドウが現れる。

## 脚注

<references/>

## 関連項目

  - [WinAntiVirusPro](../Page/WinAntiVirusPro.md "wikilink")
  - [マルウェア](../Page/マルウェア.md "wikilink")

## 外部リンク

  - [Symantec Security Response - SystemDoctor](http://www.symantec.com/region/jp/avcenter/venc/data/pf/jp-systemdoctor.html)
  - [Symantec Security Response - DriveCleaner](http://www.symantec.com/region/jp/avcenter/venc/data/jp-drivecleaner.html)
  - [Symantec Security Response - ErrorSafe](http://www.symantec.com/region/jp/avcenter/venc/data/jp-errorsafe.html)
  - [higaitaisaku.com（アダ被）:WinFixer 2005の対処法](http://www.higaitaisaku.com/removewinfixer.html)

[Category:スケアウェア](https://ja.wikipedia.org/wiki/Category:スケアウェア "wikilink") [Category:マルウェア](https://ja.wikipedia.org/wiki/Category:マルウェア "wikilink") [Category:詐欺](https://ja.wikipedia.org/wiki/Category:詐欺 "wikilink")

1.  Vundoというトロイの一種によるダイアログ表示で、一般的に[SysProtectと呼称される](https://ja.wikipedia.org/wiki/:en:SysProtect "wikilink")。このトロイは、Sun [Java](https://ja.wikipedia.org/wiki/Java "wikilink")1.4以前の脆弱性を利用するのが常套手段だが、必ずしもそうであるとは限らない（[ActiveX](../Page/ActiveX.md "wikilink")もしばしば利用される）。