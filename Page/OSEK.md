> この記事は[OSEK](https://ja.wikipedia.org/wiki/OSEK)から翻訳されています。


**OSEK**（**オーゼック**、[独](../Page/ドイツ語.md "wikilink")：Offene Systeme und deren Schnittstellen für die Elektronik im Kraftfahrzeug、英語：Open system together with interfaces for automotive electronics（車載電子機器用の公開インタフェース及びシステム））は、自動車制御を行う[エンジンコントロールユニット](../Page/エンジンコントロールユニット.md "wikilink")（ECU）で用いるプログラムの業界標準作成を目標としてドイツの自動車産業が1993年に設立した[プロジェクト](../Page/プロジェクト.md "wikilink")である。 また、そのプロジェクトが規定した[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")仕様も指す。

## OSの標準化

フランス自動車産業におけるOSEKと同様のプロジェクトであったVDXと協調路線をとり、OSEK/VDXとして1995年10月に仕様を提示した。国際規格としては、ISO TC22(road vehicle)SC3で審議し、2005年現在、車載機器制御用OSの国際標準 ISO 17356シリーズとして[ISOが発行している](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")。ISOのOSEK OSの現行文書は、ISO 17356-1:2005 Road vehicles -- Open interface for embedded automotive applications -- Part 1: General structure and terms, definitions and abbreviated terms\[1\]である。Part6 OILなどシリーズ既発行。JISは未発行。

## 主な機能

### 割り込み処理機能

OSEKにおけるISR（interrupt service routine[割り込みサービスルーチン](https://ja.wikipedia.org/wiki/割り込みサービスルーチン "wikilink")）には、OSのサービスを使用しないISR1と、OSのサービスであるシステムコールを呼び出すことが出来るISR2がある。また、割り込みの禁止・許可を制御する機能も有している。OSEKでは、エンジン・モータのような角速度制御しているソフトウェアを割り込みで設計することを想定している。

### 処理（タスク）管理機能

OSEKにおける処理（[タスク](https://ja.wikipedia.org/wiki/タスク "wikilink")）は、他の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")における[スレッドと等価である](../Page/スレッド_\(コンピュータ\).md "wikilink")。[アプリケーション内における](../Page/アプリケーションソフトウェア.md "wikilink")[プログラムを並列実行する単位である](../Page/プログラム_\(コンピュータ\).md "wikilink")。OSEK/VDX仕様のOS上で動作するアプリケーションは、0個以上のタスクで構成する。タスクには、基本タスクと拡張タスクがある。拡張タスクは WaitEvent システムコールにより待ち状態に遷移できる。OSEKでは、タスクが割り込みを妨げない設計ができるようになっている。

### 応用状態（アプリケーションモード）

応用状態（アプリケーションモード）はOSが起動する際に操作状態（オペレーションモード）を選択する機能である。OS起動後は応用状態（アプリケーションモード）を変更することはできない。

### 事象（イベント）制御機能

事象（イベント）はタスク間の同期を取るための仕組みである。拡張タスクで用意している。

### 資源（リソース）

OSEKで規定する資源（リソース）は、タスク若しくはISRの優先度を上げるためのシステムオブジェクトである。 1つの資源（リソース）を複数のタスクで共有することで、共有メモリアクセスの排他制御が可能となる。

### 警告（アラーム）

警告（アラーム）は指定時間に、設定された動作を起こすための機能である。 警告（アラーム）満了時に起こせる動作は、タスク起動、イベント設定、ユーザ[コールバックである](../Page/コールバック_\(情報工学\).md "wikilink")。

### 伝言（メッセージ）

OSEK OS仕様では規定していない。OSEK COM仕様で伝言（メッセージ）の対応が可能。 OSEK COM仕様で、キューイング機能、可変長メッセージ、周期送信などの機能を有する。

### 鉤（フック）ルーチン

OSEKには鉤（フック）ルーチンという概念がある。 OS内部処理中に利用者領域で指定した操作（ハンドラ）を呼び出す機能を持つ。 タスクの切り替わり前後や、システムサービスのエラー発生時などに呼び出されるため、動作の追跡（トレース）や虫取り（デバッグ）に利用できるインタフェイスを有する。

## OIL(OSEK Implementation Language)

OILはアプリケーションの設定（コンフィギュレーション）記述を行うための専用言語である。OILで記述したアプリケーション設定ファイルを系生成器（システムジェネレータ）(SG)に通すと、例えば[C言語](../Page/C言語.md "wikilink")のソースファイルを出力する。OSEKはC言語で記述することを必須としていないため、他の言語のソースファイルを出力するSGがあってもよい。この方式は、[μITRON](https://ja.wikipedia.org/wiki/μITRON "wikilink")仕様における静的APIおよび生成器（コンフィギュレータ）によるものと同等である。ISOの現行文書は、 ISO 17356-6:2006 Road vehicles -- Open interface for embedded automotive applications -- Part 6: OSEK/VDX Implementation Language (OIL)。自動車技術会が自動車用ソフトウェアのJIS作成団体である。JISは未発行。

## 適合級（コンフォーマンスクラス）

OSEKでは、OS機能の理解を容易にするためや、OS機能の部分的な実装を可能とすること等を目的とした、適合級（コンフォーマンスクラス）と呼ぶ機能の部分集合（サブセット）を用意している。

コンフォーマンスクラスには以下の4種類がある。

  - BCC1：基本タスクのみ。各タスクは異なる優先度を持ち、タスクあたりの起動要求と優先度あたりのタスク数に制限あり。(逆に言えば、一つの優先度には一つのタスクしかないため、タスクの待ち状態がない設計ができる。)
  - BCC2：BCC1に加え、1優先度あたりの複数のタスクおよび多重起動要求が可能。
  - ECC1：BCC1に加え、拡張タスクが利用可能。
  - ECC2：ECC1に加え、1優先度あたりの複数のタスクおよび多重起動要求が可能。

## AUTOSAR

ヨーロッパを中心に、米日の自動車製造業者(OEM),自動車部品製造業者(supplyer)があつまり、自動車ソフトウェアの部品化を高める仕様として[AUTOSAR](https://ja.wikipedia.org/wiki/AUTOSAR "wikilink")を決めている。 AUTOSARでは、WTO/TBT協定に基づきOSとしてISO OSEKを参照し、拡張部分を規定している。

## オープンソース実装

OSEK OS仕様に準拠した実装として、[TOPPERS](https://ja.wikipedia.org/wiki/TOPPERS "wikilink")プロジェクトがTOPPERS/ATK1\[2\]をオープンソースとして提供している。 AUTOSAR 4.0仕様に準拠した実装として[TOPPERS](https://ja.wikipedia.org/wiki/TOPPERS "wikilink")プロジェクトがTOPPERS/ATK2\[3\]をオープンソースとして提供している。

## 参考文献

  - Programming in the OSEK/VDX Environment, ISBN 978-1578200818

## 脚注

## 関連項目

  - [車載LAN](https://ja.wikipedia.org/wiki/車載LAN "wikilink")
  - [Controller Area Network](https://ja.wikipedia.org/wiki/Controller_Area_Network "wikilink")
  - [FlexRay](https://ja.wikipedia.org/wiki/FlexRay "wikilink")

## 外部リンク

  - [OSEK/VDX Portal](http://portal.osek-vdx.org/)

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:自動車技術標準](https://ja.wikipedia.org/wiki/Category:自動車技術標準 "wikilink") [Category:自動車技術](https://ja.wikipedia.org/wiki/Category:自動車技術 "wikilink") [Category:ドイツの規格](https://ja.wikipedia.org/wiki/Category:ドイツの規格 "wikilink")

1.  ISO <https://www.iso.org/standard/33007.html>
2.  TOPPERS/ATK1 <https://www.toppers.jp/atk1.html>
3.  TOPPERS/ATK2 <https://www.toppers.jp/atk2.html>