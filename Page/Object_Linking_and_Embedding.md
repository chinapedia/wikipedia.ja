> この記事は[Object Linking and Embedding](https://ja.wikipedia.org/wiki/Object_Linking_and_Embedding)から翻訳されています。


**Object Linking and Embedding** （**OLE**、**オブジェクトのリンクと埋め込み**）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した、オブジェクトをやり取りするための仕組み・規約である。 開発者に対しては、OLEコントロール拡張（OLE Control Extension, OCX）のような、カスタム[ユーザーインターフェイス](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")要素の開発と利用をもたらす。 技術詳細的には、OLEオブジェクトは、**`IOleObject`**インターフェイス\[1\]を実装した何らかのオブジェクトである（オブジェクトの要求仕様によっては、他のインターフェイスをともに実装していることもある）。

## 概要

OLEは文書の一部分を他のソフトで編集させ、それを元の文書に取り込むことも可能にしている。たとえば、[DTP](../Page/DTP.md "wikilink")では、テキストを[ワープロソフト](../Page/ワープロソフト.md "wikilink")、図を[ペイントツール](https://ja.wikipedia.org/wiki/ペイントツール "wikilink")や[ドローツール](https://ja.wikipedia.org/wiki/ドローツール "wikilink")で編集するといった具合である。また、他のデータへの参照を文書に含めることもでき、その場合参照先のデータが変更されると、参照が含まれる文書にも即座にその変更が反映される。

OLEの初期の用途は**[複合文書](https://ja.wikipedia.org/wiki/複合文書 "wikilink")**の管理のためであるが、ドラッグアンドドロップや[クリップボード](https://ja.wikipedia.org/wiki/クリップボード "wikilink")による[アプリケーション間でのデータの転送のためにも使われている](../Page/アプリケーションソフトウェア.md "wikilink")。また、OLEによるオートメーションは、[JScript](https://ja.wikipedia.org/wiki/JScript "wikilink")や[VBScript](../Page/VBScript.md "wikilink")を経由して、アプリケーションの動作を自動化するスクリプティングにも使われている。

OLEを活用しているソフトウェア実例としては、[Microsoft Office製品のほか](../Page/Microsoft_Office.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")版[Adobe](https://ja.wikipedia.org/wiki/Adobe "wikilink")クリエイティブ製品の\[2\]が挙げられる。

## 歴史

### OLE 1.0

OLE 1.0は1990年、[動的データ交換](https://ja.wikipedia.org/wiki/動的データ交換 "wikilink") (Dynamic Data Exchange, DDE) の後継として公開された。DDEが2つのアプリケーションの間で限定的なデータ転送を行う仕組みだったのに対し、OLEは2つのドキュメント間の連携（リンク）や、あるドキュメントに別のドキュメントを埋め込みを管理する機能を持った仕組みであった。

OLEサーバとクライアント間の通信には、システムライブラリを介するが、これには[仮想関数テーブル](https://ja.wikipedia.org/wiki/仮想関数テーブル "wikilink") (vtable, VTBL) が用いられた。VTBLには、OLEシステムがサーバやクライアントとの通信に用いる関数へのポインタが所定の構造に従って収められている。サーバとクライアントに対応するシステムライブラリは、OLESVR.DLLとOLECLI.DLLで、当初はこの2つの間の通信に`WM_DDE_EXECUTE`メッセージが利用されていた。

OLE 1.0は後に[COMや](../Page/Component_Object_Model.md "wikilink")[DCOMとして](../Page/Distributed_Component_Object_Model.md "wikilink")[ソフトウェアの部品化を実現するアーキテクチャとなっていった](../Page/ソフトウェアコンポーネント.md "wikilink")。

OLEオブジェクトがクリップボードやドキュメントに埋め込まれる形で存在するとき、2つのWindowsネイティブな表現形式（[ビットマップと](https://ja.wikipedia.org/wiki/Windowsビットマップ "wikilink")[メタファイル](https://ja.wikipedia.org/wiki/メタファイル "wikilink")）も保存されている。これにより、オブジェクトをメモリ上に作成するアプリケーションをロードすることなく画面表示が可能になる。さらに、そのOLEオブジェクトに対応する適切なアプリケーションがインストールされていれば、オブジェクトを編集できる。

### OLE 2.0

OLE 1.0の改良版として現れたOLE 2.0は、その目指すところはOLE 1.0と大きな違いはないが、実装面では、生のVTBLではなくCOMを使って実装し直されたという大きな違いがある。また、、[ドラッグ・アンド・ドロップ](../Page/ドラッグ・アンド・ドロップ.md "wikilink")、[インプレースアクティベーション](https://ja.wikipedia.org/wiki/インプレースアクティベーション "wikilink")などの新機能が加わった。

## 関連項目

  - [Component Object Model](../Page/Component_Object_Model.md "wikilink")
  - [ActiveX](../Page/ActiveX.md "wikilink")
  - [Windows Script Host](https://ja.wikipedia.org/wiki/Windows_Script_Host "wikilink")
  - [Active Scripting](https://ja.wikipedia.org/wiki/Active_Scripting "wikilink")
  - [Microsoft Office](../Page/Microsoft_Office.md "wikilink")
  - [Bonobo](../Page/Bonobo.md "wikilink")、[KPart](https://ja.wikipedia.org/wiki/KPart "wikilink")
  - [OLE for Process Control](https://ja.wikipedia.org/wiki/OLE_for_Process_Control "wikilink")
  - [スクラップ (Windows)](https://ja.wikipedia.org/wiki/スクラップ_\(Windows\) "wikilink")

## 脚注

## 外部リンク

  -
[Category:コンピュータのユーザインタフェース](https://ja.wikipedia.org/wiki/Category:コンピュータのユーザインタフェース "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")

1.  [IOleObject interface (COM)](https://msdn.microsoft.com/en-us/library/windows/desktop/dd542709.aspx)
2.  [Adobe Scripting Center | Adobe Developer Connection \[ADC](http://www.adobe.com/jp/devnet/scripting.html)\]