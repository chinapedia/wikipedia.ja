> この記事は[StrongSwan](https://ja.wikipedia.org/wiki/StrongSwan)から翻訳されています。


**strongSwan**は、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")向けの完全な[IPsec](../Page/IPsec.md "wikilink")実装である。

[FreeS/WAN](https://ja.wikipedia.org/wiki/FreeS/WAN "wikilink")プロジェクトから派生したプロジェクトであり、[GNU General Public Licenseでリリースされている](../Page/GNU_General_Public_License.md "wikilink")。スイスの\[1\]で通信セキュリティの教授を務めるAndreas Steffenが、主に保守を行っている。

[X.509](../Page/X.509.md "wikilink")[公開鍵証明書](../Page/公開鍵証明書.md "wikilink")を使った強力な[認証](../Page/認証.md "wikilink")機構が中心であり、標準化された[PKCS](../Page/PKCS.md "wikilink")\#11インタフェースを介した[ICカード](../Page/ICカード.md "wikilink")への[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")の安全な格納も行っている。また、[証明書失効リスト](../Page/証明書失効リスト.md "wikilink")と[Online Certificate Status Protocol](../Page/Online_Certificate_Status_Protocol.md "wikilink") (OCSP) もサポートしている。変わった機能として、[X.509](../Page/X.509.md "wikilink")を使ってグループメンバー属性に基づいた[アクセス制御](../Page/アクセス制御.md "wikilink")を実装している。

設定方法は直接的でわかりやすく、[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の各種[VPNクライアントなど](../Page/Virtual_Private_Network.md "wikilink")、他の[IPsec](../Page/IPsec.md "wikilink")実装とも素直に連携できる。

strongSwan 4.1では、RFC 4306で定義された[IKEv2](https://ja.wikipedia.org/wiki/IKEv2 "wikilink")プロトコルが実装されている。

## UML シミュレーション環境

[ユーザーモードLinux](https://ja.wikipedia.org/wiki/ユーザーモードLinux "wikilink") (UML) に基づいた使いやすいシミュレーション環境が付属している。8つの仮想ノードで構成されたネットワークで、[VPNに関するさまざまな状況を試せる](../Page/Virtual_Private_Network.md "wikilink")。

## 脚注

## 外部リンク

  - [strongSwan 公式サイト](http://www.strongswan.org/)
  - [strongSwan UML testing environment](http://www.strongswan.org/uml/)
  - [LinuxTag 2007 Paper: strongSwan - the new IKEv2 VPN Solution](http://www.strongswan.org/docs/LinuxTag2007-strongSwan.pdf)
  - [LinuxTag 2005 Paper: Advanced Features of Linux strongSwan](http://www.strongswan.org/docs/LinuxTag2005-strongSwan.pdf)
  - [DFN 2005 Paper: Advanced Network Simulation under User-Mode Linux](http://www.strongswan.org/uml/DFN_UML.pdf)

[Category:IPsec](https://ja.wikipedia.org/wiki/Category:IPsec "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink")

1.