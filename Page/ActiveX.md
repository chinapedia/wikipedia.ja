> この記事は[ActiveX](https://ja.wikipedia.org/wiki/ActiveX)から翻訳されています。


**ActiveX**（アクティブエックス）とは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発する[インターネット](../Page/インターネット.md "wikilink")に関する[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")やその技術を示す用語である。一般的には同社製の[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")である[Internet Explorerやそのコンポーネントを利用した](../Page/Internet_Explorer.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")上で動的なコンテンツを再生するための技術（ActiveXコントロール）を指す。[JavaScript](../Page/JavaScript.md "wikilink")や[HTML5](../Page/HTML5.md "wikilink")/[CSS3](https://ja.wikipedia.org/wiki/CSS3 "wikilink")といった標準規格の普及によって2015年現在では当たり前となった、RIA ([リッチインターネットアプリケーション](../Page/リッチインターネットアプリケーション.md "wikilink")) を実現するための技術の先駆けとも言える。

元々はマイクロソフトがオブジェクトのやりとりを行う仕組みである[Object Linking and Embedding](../Page/Object_Linking_and_Embedding.md "wikilink") (OLE) からインターネットに関する技術を分離させたものがActiveXにあたる。

## ActiveXコントロール

開発者を除いたエンドユーザーの間では、ActiveXといえば大抵の場合、ActiveXコントロールを指していることが多い。ActiveXコントロールの例としては、[Microsoft Update](../Page/Microsoft_Update.md "wikilink")、Internet Explorer版[Adobe Flashや](../Page/Adobe_Flash.md "wikilink")[Adobe Shockwave](../Page/Adobe_Shockwave.md "wikilink")、[QuickTime](../Page/QuickTime.md "wikilink")、[楽天Edy](../Page/楽天Edy.md "wikilink")、[公的個人認証サービス](../Page/公的個人認証サービス.md "wikilink")システムなどが挙げられ、Internet Explorerでそれらのサービスやコンテンツを利用するための[プラグイン](../Page/プラグイン.md "wikilink")として利用されることが多い。

Windowsのプログラミングインターフェイスを直接利用できる設計となっているため、クロスプラットフォーム設計のブラウザに搭載されている同様の技術よりもプラグイン開発の自由度が非常に高く、ファイルシステムやハードウェアも含めたWindows搭載コンピュータのほぼ全ての機能に直接的なアクセスを提供するコードを作成することが可能である。そのため、クラウドベースのメンテナンスサービスや[スマートカード](https://ja.wikipedia.org/wiki/スマートカード "wikilink")を用いたユーザー認証システムなどに多用されており、ウイルス駆除サービスや税務システムなどの高度なセキュリティを要求される分野での利用も多く見られる。

[Internet Explorer以外の](../Page/Internet_Explorer.md "wikilink")[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")に関しては、ActiveXは標準サポートされていない。[Windows版の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Mozillaでは](../Page/Mozilla_Application_Suite.md "wikilink")「Mozilla ActiveX Controls」というプラグインを利用すればActiveXコントロールを使って[Gecko](../Page/Gecko.md "wikilink")をソフトウェアへと組み込むことができた。[Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")には「ActiveX Hosting plugin for Firefox」というプラグインが存在する。[Google Chromeには](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")「ActiveX for Chrome」というプラグインが存在する。その他、[IE Tabを使用し](../Page/IE_Tab.md "wikilink")、IEコンポーネントを他のブラウザでホスティングすることでActiveXを利用する方法もある。また、Windowsのみならず[Mac OSで動作する](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[Internet Explorer for Macでも利用できた](../Page/Internet_Explorer_for_Mac.md "wikilink")。

## 問題

### ブラウザ依存

ActiveXコントロールを採用するサイトは、Internet Explorerもしくは前述のプラグインを導入したブラウザ以外では利用できない。

ActiveXを多用する企業や官公庁は特に[日本](https://ja.wikipedia.org/wiki/日本国 "wikilink")\[1\]や[韓国に多く](../Page/大韓民国.md "wikilink")、日本や韓国の官公庁や企業では128ビット暗号化に[SSLを採用せず](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")、独自のActiveXアプリ（[Xecureweb](https://ja.wikipedia.org/wiki/Xecureweb "wikilink")等）を採用しており、官公庁や金融機関やインターネットショッピングなどに積極的に採用されている。そのため、WindowsとInternet Explorerとの組み合わせに依存した形となっている。また、ActiveXを使った暗号化により、後述のセキュリティ問題があるという事も否めない。詳しくは[韓国のインターネット\#問題点](https://ja.wikipedia.org/wiki/韓国のインターネット#問題点 "wikilink")を参照。

### セキュリティ

[ウェブページ](../Page/ウェブページ.md "wikilink")の表示に変化を与えたり、インタラクティブ性を提供したり、コンピュータ本体や周辺機器のハードウェア機能にWebブラウザから直接アクセスする手段を提供したりすることで、[ウェブサイト](../Page/ウェブサイト.md "wikilink")を閲覧する楽しさや利便性を飛躍的に向上させる。しかし、[Windows Vistaよりも前のバージョンのOSでは](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、ActiveXコントロールの動作に制限が掛けられていないために[セキュリティ上](../Page/コンピュータセキュリティ.md "wikilink")、しばしば問題になっている\[2\]\[3\]（同様の技術である[Javaアプレット](../Page/Javaアプレット.md "wikilink")では[サンドボックス機構によりその動作範囲は厳しく制限される](../Page/サンドボックス_\(セキュリティ\).md "wikilink")）。

例えば、[シマンテック](../Page/シマンテック.md "wikilink")や[トレンドマイクロ](../Page/トレンドマイクロ.md "wikilink")のオンライン[ウイルススキャンサービスからわかるように](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")、ActiveXコントロールを用いれば、現在[ログオン](https://ja.wikipedia.org/wiki/ログオン "wikilink")しているユーザーがアクセスできるコンピュータ内のファイル全てに自由にアクセスできる。したがって、[マルウェア](../Page/マルウェア.md "wikilink")として動作するような、悪意のあるActiveXコントロールがユーザーのファイルに[不正アクセス](https://ja.wikipedia.org/wiki/不正アクセス "wikilink")し、情報を盗み取ることも可能である。ActiveXコントロールのインストールは、[セキュリティーホール](https://ja.wikipedia.org/wiki/セキュリティーホール "wikilink")にもなるので、充分気をつけなくてはならない。

#### 対策

ActiveXコントロールに、ベンダーが[デジタル署名](../Page/デジタル署名.md "wikilink")を付与\[4\]することで、それが第三者によって改変されていないかをユーザーが確認できる。署名の検証ができないActiveXコントロールを避けることで、正当なActiveXコントロールに似せた、偽のコントロールを導入してしまうリスクを低減することができる。

なお、デジタル署名はあくまでもオリジナルとの同一性を証明するものであり、ベンダーが偶然ないしは故意に危険なコードを実装することで、危害を与えることは可能である。ActiveXコントロールのセキュリティホールを攻撃する不正なデータを受信することで被害を受ける可能性が多数指摘されている\[5\]\[6\]。

また、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") Service Pack 2以降は初期設定で ActiveXコントロールのインストールやダウンロードを自動的にブロックして情報バーでその旨を通知するようになっている。Internet Explorer 7ではActiveXコントロールの機能を実装した上で、標準設定では無効とされている。Windows Vistaでは、ActiveXコントロールはより低い権限で実行し、アクセス可能な範囲を極力狭める機構が導入された\[7\]。また、2015年にリリースされた[Windows 10に含まれる新ブラウザ](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")[Microsoft EdgeではActiveXや](https://ja.wikipedia.org/wiki/Microsoft_Edge "wikilink")[VBScript](../Page/VBScript.md "wikilink")などの「古いIE技術」が削除され、サポート外となった\[8\]。

## その他のActiveX技術

Microsoft は ActiveX を利用した様々な製品を開発し、その多くは2015年現在においても利用されている。

  - [ActiveX Data Objects](https://ja.wikipedia.org/wiki/ActiveX_Data_Objects "wikilink")
  - [Active Server Pages](../Page/Active_Server_Pages.md "wikilink")
  - [DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")
  - [Collaboration Data Objects](https://ja.wikipedia.org/wiki/Collaboration_Data_Objects "wikilink")
  - [Active Scripting](https://ja.wikipedia.org/wiki/Active_Scripting "wikilink")
  - [Advanced Systems Format](../Page/Advanced_Systems_Format.md "wikilink")

## 脚注

<references />

## 関連項目

  - [Component Object Model](../Page/Component_Object_Model.md "wikilink")
  - [Internet Explorer](../Page/Internet_Explorer.md "wikilink")
  - [Microsoft Update](../Page/Microsoft_Update.md "wikilink")
  - [Windows Presentation Foundation](../Page/Windows_Presentation_Foundation.md "wikilink")
  - [Silverlight](https://ja.wikipedia.org/wiki/Silverlight "wikilink")

[Category:マイクロソフト](https://ja.wikipedia.org/wiki/Category:マイクロソフト "wikilink") [Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink")

1.  [e-Gov電子申請システム動作確認環境](http://www.e-gov.go.jp/help/shinsei/flow/setup01/recommended.html)
2.  [ActiveX／プラグインについて｜イチからはじめるセキュリティー｜eoセキュリティーインフォメーション](http://eonet.jp/security/knowledge/pc/activex.html)
3.  [Blogs - Japan IE Support Team Blog - Site Home - TechNet Blogs](http://blogs.technet.com/b/jpieblog/archive/2013/11/30/3614857.aspx)
4.  [MSDN](https://ja.wikipedia.org/wiki/MSDN "wikilink") Web Development Developer Center: [Authenticode](http://msdn2.microsoft.com/en-us/library/ms537359.aspx)
5.  [Windows Media Player プラグインの脆弱性により、リモートでコードが実行される (911564) (MS06-006)](http://www.microsoft.com/japan/technet/security/bulletin/MS06-006.mspx)
6.  [Macromedia - APSB06-03: Flash Player Update to Address Security Vulnerabilities](http://www.adobe.com/devnet/security/security_zone/apsb06-03.html)
7.  [セキュリティ対策の要点解説 第 20 回 Windows Vista のセキュリティ機能 ～ Internet Explorerの保護モード ～](https://www.microsoft.com/japan/technet/security/secnews/secpoint/secpoint0020.mspx)
8.