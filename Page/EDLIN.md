> この記事は[EDLIN](https://ja.wikipedia.org/wiki/EDLIN)から翻訳されています。


**EDLIN**（エドリン）は、[MS-DOS](../Page/MS-DOS.md "wikilink")および、その後の[マイクロソフト](../Page/マイクロソフト.md "wikilink")社の[OSに標準添付されている](../Page/オペレーティングシステム.md "wikilink")[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")である。コマンド制御のインターフェースにより、[テキスト](../Page/テキスト.md "wikilink")ファイルを編集する基本的な機能を持つ。数字により行番号を指定し、1文字の英字コマンドにより操作を指示する。（たとえば、**5d**はファイルの5行目を削除する操作を指示する。）

## 歴史

初期のMS-DOSではシステム唯一の[テキストエディタ](../Page/テキストエディタ.md "wikilink")だったが、後のバージョンではフルスクリーンの[MS-DOS Editorが付属するようになり](https://ja.wikipedia.org/wiki/MS-DOS_Editor "wikilink")、バージョン6でEDLINは削除された\[1\]。しかし、32ビット版[Windows NTには同梱されている](../Page/Microsoft_Windows_NT.md "wikilink")（[NTVDM](https://ja.wikipedia.org/wiki/NTVDM "wikilink")のDOSサポートがMS-DOSバージョン5.0に基づいているためである）。他のDOSコマンドとは異なり、ネイティブ[Win32](https://ja.wikipedia.org/wiki/Win32 "wikilink")プログラムに移植されていない。EDLINが存続していることは、[標準入力からコマンドの](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")[スクリプトを入力することにより](../Page/スクリプト言語.md "wikilink")、テキストファイルの小さな変更を自動的に行うために起動できるという事実から説明できるかもしれない。

実際には、MS-DOSには[GW-BASICという他のヴィジュアルエディタが用意されていた](https://ja.wikipedia.org/wiki/Microsoft_BASIC#インタプリタ系 "wikilink")。GW-BASICは[Microsoft BASICの](../Page/Microsoft_BASIC.md "wikilink")[インタプリタ](../Page/インタプリタ.md "wikilink")であり開発環境でもあった。また、MS-DOSバージョン5.0から6.22の[EDITエディタ（edit）は](https://ja.wikipedia.org/wiki/MS-DOS_Editor "wikilink")、実際には[QBasic](https://ja.wikipedia.org/wiki/QBasic "wikilink")を起動していた。QBasicはGW-BASICを置き換えたもので、さらに現代的なユーザインタフェースを持っていた。

EDLINは1980年に[ティム・パターソン](https://ja.wikipedia.org/wiki/ティム・パターソン "wikilink")が2週間で作ったものであり、6ヶ月の寿命しかないと思われていた。[1](http://www.patersontech.com/Dos/Byte/History.html) EDLINはもともと[シアトル・コンピュータ・プロダクツ](https://ja.wikipedia.org/wiki/シアトル・コンピュータ・プロダクツ "wikilink")社の[86-DOS](../Page/86-DOS.md "wikilink")（QDOS）のために書かれたものである。86-DOSはマイクロソフト社が買い取り、MS-DOSとして販売した。

## 現在の扱い

現在の環境でEDLINを使用する場合、[ロングファイルネーム](https://ja.wikipedia.org/wiki/ロングファイルネーム "wikilink")をサポートしていないという制限がある。たとえば、"longfilename.txt"という名前の既存ファイルを編集しようとすると、EDLINは"longfile.txt"という名前の新規ファイルを作成してしまう。これは、バージョン7.0までのMS-DOSの制限に関連していて、EDLIN自体の問題ではない。ロングファイルネームは、EDLINが書かれた後でMS-DOSや[Windowsの機能として追加されたものである](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

は[GPL版のEDLINクローンを作成した](../Page/GNU_General_Public_License.md "wikilink")。このクローンはロングファイルネームをサポートしていて、[FreeDOS](../Page/FreeDOS.md "wikilink")プロジェクトの一部としてダウンロード可能である。また、MS-DOSと同様に[Linux](../Page/Linux.md "wikilink")や[UNIX](../Page/UNIX.md "wikilink")でも動く。クローンの出力メッセージは様々なヨーロッパ言語や日本語にカスタマイズ可能であり、様々な[Cコンパイラでコンパイル可能である](../Page/C言語.md "wikilink")。

EDLINは、現在では一般的に役に立たないにもかかわらず、他のエディタがない環境では、EDLIN用スクリプトの[インタプリタ](../Page/インタプリタ.md "wikilink")として使用されることがある。スクリプトはEDLINコマンドの列のように見える。以下のように起動される：

    edlin < script

他の標準DOSツールとしては、[DEBUG.EXEがある](https://ja.wikipedia.org/wiki/debug_\(DOS\) "wikilink")。

## PC-98版MS-DOS 3.1でのEDLINのバグ

[日本電気](../Page/日本電気.md "wikilink") [PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用[MS-DOS](../Page/MS-DOS.md "wikilink") 3.1の初期バージョンにはEDLINに[2バイト文字](https://ja.wikipedia.org/wiki/2バイト文字 "wikilink")列の置換が正常に行われない[バグ](../Page/バグ.md "wikilink")が存在した。このバグ自体は緊急を要する重大な欠陥ではなかったが、報道機関に取り上げられたことで周知され、自主的[リコールに発展した](../Page/リコール_\(一般製品\).md "wikilink")。

[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")2月8日、一人のユーザーがMS-DOSの習得のために機能を試していたところ、このバグを発見。友人の協力を得てMS-DOSの前バージョン（Ver.2.0）を調べてみると、こちらでは正常に動作することが分かった。購入した販売店で店員に相談して操作してもらうも、やはり上手くいかなかったため、メーカーである日本電気に書面で問い合わせた。返答がなかったため17日に再度手紙を送ったところ、翌18日にサポート窓口からバグを認める電話連絡を受けた。10日後の28日にメーカーの担当者2名がバグ修正済みの交換品（[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")）を持参し、ユーザーの元を訪れた。これで問題は解決したが、ユーザーは他の購入者が気になったため、担当者にバグを公表するよう求めた。この時の担当者は対応をとる返答をしたが、数日経って販売店やメーカーのショールーム([Bit-INN](https://ja.wikipedia.org/wiki/Bit-INN "wikilink"))を度々訪れるも動きがない。そこに[NHKの記者が噂を嗅ぎ付けてユーザーの元を訪れ](https://ja.wikipedia.org/wiki/日本放送協会 "wikilink")、ユーザーは記者にバグの公表と製品の回収が妥当であることを説明した。この後、ユーザーはメーカーに再度連絡したものの、何の対応も取られないまま、3月14日19時台の[NHKニュース](../Page/NHKニュース.md "wikilink")で全国に放映された。\[2\]

報道後の日本電気の対応は迅速に行われた。ニュースが放映されたその日のうちに製品の無償回収を行うことを発表\[3\]\[4\]。3月17日に製品の登録ユーザー（4800人）に対して無償交換の通知を発送。また、1985年10月末より出荷している流通在庫（約6590本、登録ユーザー含む）を回収するため全国のパソコン販売店（3000店以上）に対しても通知を出した。4月初めには登録ユーザー分の回収をほぼ完了した。このリコールには1億円程度のコストが掛かるとした。

このバグの原因は米国[マイクロソフト](../Page/マイクロソフト.md "wikilink")のプログラムミスにあったが、発売元である日本電気は「責任は出荷前の検査で発見できなかった日本電気にある。賠償金などをマイクロソフトに要求することはしない。」としてマイクロソフトに責任を追及しなかった。この不祥事を受けて日本電気は保守・検査体制を強化するとコメントした。\[5\]

## 脚注

<references />

## 外部リンク

  - [MS-DOS Edlin command help](http://www.computerhope.com/edlin.htm)
  - [FreeDOS Edlin 2.10](http://sourceforge.net/projects/freedos-edlin)
  - [A Brief History Of DOS](http://nxdos.sourceforge.net/DOSHIST.HTM)
  - [W31:ラインエディタ EDLIN の使用方法について](http://support.microsoft.com/kb/406017/ja)
  - [FreeDOS Edlin](http://japanese.osstrans.net/software/freedos-edlin.html)（日本語）

[Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink") [Category:Windowsのコマンド](https://ja.wikipedia.org/wiki/Category:Windowsのコマンド "wikilink") [Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:1980年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1980年のソフトウェア "wikilink")

1.  MS-DOSリテール版の場合。他は[OEM](../Page/OEM.md "wikilink")先により異なる。
2.  中川貴雄「ユーザーの目：日本電気の「MS-DOS3.1」に潜んでいたバグ」『[日経パソコン](../Page/日経パソコン.md "wikilink")』[日経マグロウヒル](https://ja.wikipedia.org/wiki/日経マグロウヒル "wikilink")、1986年5月5日号、pp.207-212。
3.  「日電の主力パソコン、基本ソフトに欠陥。」『日本経済新聞』 1986年3月15日朝刊、31面。
4.  「パソコンに欠陥」『毎日新聞』 1986年3月15日朝刊、20面。
5.