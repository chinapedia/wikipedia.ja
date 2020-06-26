> この記事は[Transport Layer Security](https://ja.wikipedia.org/wiki/Transport_Layer_Security)から翻訳されています。


**Transport Layer Security**（トランスポート・レイヤー・セキュリティ、**TLS**）は、[インターネット](../Page/インターネット.md "wikilink")などの[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")において[セキュリティを要求される通信を行うための](../Page/セキュア通信.md "wikilink")[プロトコルである](../Page/通信プロトコル.md "wikilink")。主な機能として、通信相手の[認証](../Page/認証.md "wikilink")、通信内容の[暗号](../Page/暗号.md "wikilink")化、[改竄](../Page/改竄.md "wikilink")の検出を提供する。TLSは[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")によって策定された。

当プロトコルは（特に区別する場合を除いて）**SSL** (**Secure Sockets Layer**) と呼ばれることも多い。これは、TLSの元になったプロトコルがSSLであり\[1\]、そのSSLという名称が広く普及していることによる\[2\]。

2018年現在の最新版はTLS 1.3である。

## 概要

TLSは多くの場合、コネクション型の[トランスポート層](../Page/トランスポート層.md "wikilink")プロトコル（通常は[TCP](../Page/Transmission_Control_Protocol.md "wikilink")）と[アプリケーション層](../Page/アプリケーション層.md "wikilink")のあいだにおいて使われる。特に[HTTPでの利用を意識して設計されているが](../Page/Hypertext_Transfer_Protocol.md "wikilink")、アプリケーション層の特定のプロトコルには依存せず、様々なアプリケーションにおいて使われている。TLS 1.1以降を元にしたプロトコルが、[UDPや](../Page/User_Datagram_Protocol.md "wikilink")[DCCPといった](../Page/Datagram_Congestion_Control_Protocol.md "wikilink")[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")型プロトコル上でも実装されており、こちらは[Datagram Transport Layer Security](https://ja.wikipedia.org/wiki/Datagram_Transport_Layer_Security "wikilink") (DTLS) として独立して標準化されている。

TLSはHTTPなどのアプリケーション層のプロトコルと組み合わせることで、[HTTPS](../Page/HTTPS.md "wikilink")などセキュアな通信プロトコルを実現している。そのようなプロトコルとして以下のものがある：

| SSLと組み合わせたプロトコル                                         | ポート番号 | 元のプロトコル                                                             | ポート番号 |
| ------------------------------------------------------- | ----- | ------------------------------------------------------------------- | ----- |
| [HTTPS](../Page/HTTPS.md "wikilink")                    | 443   | [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")           | 80    |
| [SMTPS](https://ja.wikipedia.org/wiki/SMTPS "wikilink") | 465   | [SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")         | 25    |
| [LDAPS](https://ja.wikipedia.org/wiki/LDAPS "wikilink") | 636   | [LDAP](../Page/Lightweight_Directory_Access_Protocol.md "wikilink") | 389   |
| [FTPS](../Page/FTPS.md "wikilink") (data)               | 989   | [FTP](../Page/File_Transfer_Protocol.md "wikilink") (data)          | 20    |
| FTPS (control)                                          | 990   | FTP (control)                                                       | 21    |
| [IMAPS](https://ja.wikipedia.org/wiki/IMAPS "wikilink") | 993   | [IMAP](../Page/Internet_Message_Access_Protocol.md "wikilink")      | 143   |
| [POP3S](https://ja.wikipedia.org/wiki/POP3S "wikilink") | 995   | [POP3](../Page/Post_Office_Protocol.md "wikilink")                  | 110   |

### アプリケーション層プロトコルへの適用

TLSは特定のアプリケーション層プロトコルに依存しないため、HTTP以外にも多くのプロトコルにおいて採用され、[クレジットカード](../Page/クレジットカード.md "wikilink")情報や[個人情報](../Page/個人情報.md "wikilink")、その他の機密情報を通信する際の手段として活用されている。

既存のアプリケーション層プロトコルでTLSを利用する場合、大きく2つの適用方式が考えられる。まずひとつは、下位層（通常はTCP）の接続を確立したらすぐにTLSのネゴシエーションを開始し、TLS接続が確立してからアプリケーション層プロトコルの通信を開始する方式である。もうひとつは、まず既存のアプリケーション層プロトコルで通信を開始し、その中でTLSへの切り替えを指示する方式である。切り替えコマンドとして`STARTTLS`が広まっているため、この方式自体を[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS "wikilink")と呼ぶこともある。

前者はアプリケーション層のプロトコルをまったく変更しなくてすむことが利点である。その反面、平文で接続を開始する実装と共存できなくなるため、既存の[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")とは別にTLS対応用のポート番号が必要となる。実態としては、SSL/TLSの最初の適用例である[HTTPS](../Page/HTTPS.md "wikilink")をはじめとして、前者の方式を使うことが多い。ただし、この方式はバーチャルホストを構成する際に問題となる可能性がある。詳細は[\#バーチャルホスト](https://ja.wikipedia.org/wiki/#バーチャルホスト "wikilink")の節を参照。

なお、ポート番号を分ける方式をSSL、同一ポート番号で切替える方式（STARTTLS方式）をTLSと呼んでいる実装もある\[3\]。TLS/SSLという用語の区別がプロトコルのバージョンを指しているか、アプリケーション層プロトコルへの適用方式を指しているかは、文脈で判断する必要がある。

### セキュリティ上の考察

#### TLS適用の有無と使用アルゴリズムの強度

TLSを導入さえすればセキュリティが確保できるという認識は誤っている。TLS通信は、[平文](../Page/平文.md "wikilink")での通信に比べて（主に[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")・[復号](https://ja.wikipedia.org/wiki/復号 "wikilink")時）余分な[計算機能力を使用するため](https://ja.wikipedia.org/wiki/計算時間 "wikilink")、本当に必要なとき以外は使用しないことが多い。システムはデータの重要性を判断することができないので、TLSが必要なときに正しく使われているかどうかは、利用者自身が判断しなければならない。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Firefox-SSL-padlock.png "wikilink") 特に[World Wide Webでは](../Page/World_Wide_Web.md "wikilink")、ハイパーリンクによるページ遷移を繰り返して処理を行うため、どの通信でSSL/TLSが使用されているか把握することが重要になる。多くのウェブブラウザは、画面のどこかに[南京錠](../Page/南京錠.md "wikilink")の[アイコン](../Page/アイコン.md "wikilink")を表示したり、[アドレスバー](https://ja.wikipedia.org/wiki/アドレスバー "wikilink")の色を変化させたりして、利用者に情報を提供している。

また実際に使用するアルゴリズムは双方のネゴシエーションによって決まるため、TLSを使用していても、システムとして許容はするが推奨できないアルゴリズムが採用される可能性がある。このような場合もダイアログメッセージなどを使って利用者に警告すべきである。

#### 証明書の正当性

TLSは公開鍵証明書を用いて認証を行い、[なりすまし](https://ja.wikipedia.org/wiki/なりすまし "wikilink")を極力排除しようとする。しかしシステムの自動的な対応には限界があり、すべてのなりすましを検出できるわけではない。

[公開鍵証明書](../Page/公開鍵証明書.md "wikilink")には認証局による電子署名が与えられる。その署名の正当性を評価するためには認証局の証明書が必要であり、最終的には[ルート証明書](../Page/ルート証明書.md "wikilink")と呼ばれる一群の証明書に行きつく。各システムは、認証局の証明書として信用できるルート証明書を、あらかじめ保持している。認証局は自身の秘密鍵を厳重に秘匿し、また証明書の発行にあたっては正当なサーバ管理者かどうか確認することが求められる。これらが保証されない認証局のルート証明書を組み込むことは、TLSにおける認証機能を破綻させることになる。仮に認証局自体は安全でも、入手したルート証明書が本当に意図する認証局のものかどうか判断することは難しいという点も注意すべきである。

TLSで認証を行うためには、認証局の署名に加えて、証明書の発行先を確認する必要がある。確認しない場合、サーバAの管理権限を持たない者がサーバBとして正当な証明書を取得し、その証明書を使ってサーバAを名乗ることができてしまう。TLS用のサーバ証明書には発行先サーバのホスト名が書き込まれており、クライアントは自分が接続しようとしているサーバのホスト名と一致するかどうか確認することができる。

現実には「正当な」サーバであっても、これらの検証において「問題がある」と判断される証明書を使って運用されているサーバが少なからず存在する。セキュリティ研究者の[高木浩光](../Page/高木浩光.md "wikilink")は、このような証明書のことを、[オレオレ詐欺をもじって](https://ja.wikipedia.org/wiki/振り込め詐欺 "wikilink")「[オレオレ証明書](https://ja.wikipedia.org/wiki/オレオレ証明書 "wikilink")」と呼んで批判している\[4\]。

この検証は、システムに指示された接続先のホスト名と実際に接続した先のホスト名が一致することを検証しているのであり、利用者が意図する接続先とは必ずしも一致しないことに注意する必要がある。

例として、利用者が意図する接続先であるサーバAがホスト名www.example.**com**でサービスを提供しており、攻撃者はサーバBおよびホスト名www.example.**org**を取得している場合を考える。仮に攻撃者が[DNS偽装](https://ja.wikipedia.org/wiki/DNS偽装 "wikilink")に成功して、www.example.comへの接続をサーバBに導くことができたとしても、www.example.comのサーバ証明書を入手できないので、TLS接続を提供することはできない。しかし攻撃者も、www.example.orgのサーバ証明書を入手することはできる。したがって、サーバAに接続しようとしている利用者を、www.example.comではなくwww.example.orgへ接続させることができれば、クライアントからは正当な証明書を持ったサーバとしか見えない。

上記のような例も考慮した上で、利用者が意図している接続先かどうかを判断するためには、以下の2つの条件を満たす必要がある。

1.  利用者は意図する接続先の正しいホスト名を知っている。
2.  利用者は、現在システムに指示されている接続先が、自分の知っている正しいホスト名と一致していることを確認できる。

2は、[情報処理推進機構](../Page/情報処理推進機構.md "wikilink") (IPA) が公開している「安全なウェブサイトの作り方」\[5\]という文書の「[フィッシング詐欺を助長しないための対策](../Page/フィッシング_\(詐欺\).md "wikilink")」に対応する。

#### 乱数の品質

他の多くの近代暗号と同様に、TLSもまた、暗号としての強度は乱数の品質に依存している。桁数（[ビット](../Page/ビット.md "wikilink")長）の大きな暗号は推測が難しいという前提が暗号強度の根拠となっている。（これは、[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")システムにも言える）もし何らかの理由で乱数の出現確率が大きく偏るようなことがあれば、[総当たり攻撃](../Page/総当たり攻撃.md "wikilink")で解読される可能性が上昇する。通常は、これは実装の問題に起因している。

古い例では、Netscapeの初期の実装における乱数生成の脆弱性がある。[プロセスIDや時刻から乱数を生成していることが判明し](../Page/プロセス識別子.md "wikilink")、これらの情報を取得できる場合には総当たり攻撃の所要時間が大幅に短くなるという問題があった\[6\]。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[5月15日](../Page/5月15日.md "wikilink")には[Debian](../Page/Debian.md "wikilink")が脆弱性に関する報告\[7\]を発表した。[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")ライブラリのパッケージメンテナンスの際に誤ったパッチを導入した結果、鍵生成に適切な乱数が使われず僅か65536 (= 2<sup>16</sup>) 通りの予測可能な物が生成されてしまった事を明らかにした\[8\]（なお、この問題はOpenSSLそのものの脆弱性ではない）。この影響を受けるのはDebian sargeより後のバージョンのDebianと、それから派生した[Damn Small Linux](../Page/Damn_Small_Linux.md "wikilink")、[KNOPPIX](../Page/KNOPPIX.md "wikilink")、[Linspire](../Page/Linspire.md "wikilink")、[Progeny Debian](../Page/Progeny_Debian.md "wikilink")、[sidux](https://ja.wikipedia.org/wiki/sidux "wikilink")、[Ubuntu](../Page/Ubuntu.md "wikilink")、[UserLinux](../Page/UserLinux.md "wikilink")、[Xandros](../Page/Xandros.md "wikilink")である。脆弱性のあるバージョンのOpenSSLは[2006年](../Page/2006年.md "wikilink")[9月17日](../Page/9月17日.md "wikilink")に公開された。安定バージョンがリリースされた[2007年](../Page/2007年.md "wikilink")[4月8日](../Page/4月8日.md "wikilink")以降は確実に影響を受ける。脆弱性のあるバージョンのOpenSSLで作られた鍵全て、[SSH鍵](../Page/Secure_Shell.md "wikilink")、[OpenVPN](../Page/OpenVPN.md "wikilink")鍵、[DNSSEC鍵](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink")、[X.509](../Page/X.509.md "wikilink")証明書を生成するのに使われる鍵データ、およびSSL/TLSコネクションに使うセッション鍵等が影響を受ける。これらの鍵は65536通り全てを総当たり攻撃で試すだけでいずれの鍵が使われているか解読可能であり（SSHでは20分間で解読できたと報告されている）、また脆弱な鍵がインストールされたDebianを含む全ての[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")において緊急の対応が必要であると専門家が注意を呼びかけている。生成された鍵に問題があるため、Debian GNU/Linuxで生成した鍵を[Microsoft Windowsのような非UNIXシステムに導入しているような場合も](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、この脆弱性の影響を受ける。具体的対応については、Debianの報告の他、[JPCERT/CC](https://ja.wikipedia.org/wiki/JPCERT/CC "wikilink")の勧告\[9\]等に従うべきである。

## プロトコル概要

本説ではTLS 1.2の概要を説明する。

TLSには主なプロトコルとして暗号通信に必要な鍵 (**master secret**) を[鍵共有](https://ja.wikipedia.org/wiki/鍵共有 "wikilink")して[セッション](../Page/セッション.md "wikilink")を確立する**TLSハンドシェイクプロトコル**と、master secretを用いて暗号通信することで確立されたセッションにおける[コネクション](https://ja.wikipedia.org/wiki/コネクション "wikilink")をセキュアにする**TLSレコードプロトコル**がある。

その他に用いている暗号方式やハッシュ関数等のアルゴリズムを変更する **Change Cipher Spec プロトコル**と通信相手からの通信終了要求や何らかのエラーを通知する **アラートプロトコル**がある。

### TLSハンドシェイクプロトコル

TLSハンドシェイクプロトコルは4つのフェーズに大別できる。

<table>
<tbody>
<tr class="odd">
<td style="text-align: center;"><table>
<tbody>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>クライアント</p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
</tbody>
</table></td>
<td><p>（第一フェーズ）</p></td>
<td style="text-align: center;"><table>
<tbody>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>   サーバ   </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p> </p></td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>─ClientHello───→</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>←ServerHello────</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p> </p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>（第二フェーズ）</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>←Certificate────</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>←ServerKeyExchange─</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>←CertificateRequest──</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>←ServerHelloDone──</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p> </p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>（第三フェーズ）</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>─Certificate───→</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>─ClientKeyExchange→</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>─CertificateRequest─→</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>─CertificateVerify─→</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p> </p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>（第四フェーズ）</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>─Change Cipher Spec→</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>─Finished─────→</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>←Change Cipher Spec─</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>←Finished──────</p></td>
<td></td>
<td style="text-align: center;"></td>
</tr>
</tbody>
</table>

#### 第一フェーズ

第一のフェーズではサーバ・クライアント間で通信に必要情報の合意を図る。このフェーズでは、まずクライアントからサーバに**ClientHello**が送信され、次にサーバからクライアントに**ServerHello**が送信される\[10\]。

ClientHelloはTLSのバージョン、乱数、セッションID、通信に用いる暗号方式やハッシュアルゴリズムのリスト (**cipher_suites**)、通信内容の圧縮方法、および拡張領域の6つからなる\[11\]。乱数は鍵共有におけるリプレイ攻撃を防ぐためのものである。

ServerHelloもClientHelloと同様の6つからなっている（名称は一部異なる）\[12\]。ServerHelloの主な目的は、ClientHelloで提示された選択肢の中でサーバにとって好ましいものを選択する事で、例えばClientHelloで提示されたcipher_suitesの中から、サーバが通信に使いたいcipher_suiteを一組選ぶ\[13\]。乱数はClientHelloとは独立して選ぶ\[14\]。これもリプレイ攻撃を回避するためである。セッションIDは特に問題がなければClientHelloと同一のものを返す。

#### 第二フェーズ

第二フェーズではサーバからクライアントに対して鍵共有に必要な情報を送る。具体的にはサーバは**Certificate**、**ServerKeyExchange**、**CertificateRequest**、**ServerHelloDone**を（第一フェーズServerHelloに引き続き）クライアントに送信する\[15\]。

Certificateは鍵共有で用いる公開鍵とその証明書で別途取り決めがない限り[X.509](../Page/X.509.md "wikilink")v3のフォーマットに従う\[16\]。なお鍵共有方式としてDH_anonを用いている場合にはcertificateは必要ない\[17\]。

ServerKeyExchangeは鍵共有プロトコルに依存して送るデータが異なるが、DH_anonであれば、という形のデータを送る。ここではサーバの秘密の乱数である。鍵共有プロトコルがDHE_DSS、DHE_RSA、DH_anonでは何らかのserver_key_exchangeを送るが、RSA、DH_DSS、DH_RSAでは何も送らない\[18\]。

CertificateRequestはクライアントの公開鍵とその証明書を送ることを要求するためのもので、サーバが許容できる証明書の種別、ハッシュと署名方式、および[認証局](../Page/認証局.md "wikilink")のリストからなっている\[19\]。

そして最後にサーバ側からのメッセージ送信が終わった事を示すServerHelloDoneをクライアントに送る。

#### 第三フェーズ

第三フェーズではクライアントからサーバに対して鍵共有に必要な情報を送る。具体的にはクライアントは**Certificate**、**ClientKeyExchange**、**CertificateVerify**をサーバに送る\[20\]。

Certificateは鍵共有で用いるクライアントの公開鍵とその証明書である。証明書はサーバから送られてきたCertificateRequestの条件を満たさねばならない。

ClientKeyExchangeは鍵共有プロトコルに依存して送るデータが異なるが、DH_anonであれば、という形のデータを送る。ここではクライアントの秘密の乱数である。

ここまでのプロトコルにより、サーバとクライアントの間で**premaster secret**が共有された事になる。DH_anonであればpremaster secretはである。premaster secretを鍵にした[擬似ランダム関数](https://ja.wikipedia.org/wiki/擬似ランダム関数 "wikilink")にServerHelloとClientHelloの乱数などを並べたものを入力した結果得られたものが**master secret**である\[21\]。

CertificateVerifyはクライアントが署名能力を持っている事を証明するためにこれまでTLSハンドシェイクプロトコルで送受信された全メッセージに対し、共有されたmaster secret で署名したものである \[22\]。

#### 第四フェーズ

クライアントは必要ならChange Cipher Spec プロトコルのメッセージをサーバに送り、終了を意味するFinishedをサーバに送る。同様にサーバも必要ならChange Cipher Spec プロトコルのメッセージをクライアントに送り、終了を意味するFinishedをクライアントに送る\[23\]。

### TLSレコードプロトコル

TLSレコードプロトコルはアプリケーション層から受け取った通信内容を2<sup>14</sup>バイト以下のブロックに**分解** (fragmentation) し、各ブロックを**圧縮** (compress) し、圧縮されたブロックを[認証暗号で暗号化する](https://ja.wikipedia.org/wiki/認証付き暗号 "wikilink")**レコード Payload 防護**を施した上で、通信内容を通信相手に送信する\[24\]。

認証暗号は、TLS 1.1まではMACをつけた後で共通鍵暗号化するMAC-then-Encrypt (MtE) のみが利用可能であった。TLS 1.2からは、[AES](../Page/Advanced_Encryption_Standard.md "wikilink")-[GCMのようなAEADに分類される認証暗号専用の](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink")[暗号利用モード](../Page/暗号利用モード.md "wikilink")も利用可能になり\[25\]、TLS 1.3ではAEADのみが利用可能となっている。

認証暗号にブロック暗号（AEAD以外）を選択した場合、TLS 1.1以降において[IVはTLSレコードプロトコルの送信者がランダムに選ぶ](https://ja.wikipedia.org/wiki/初期化ベクトル "wikilink")\[26\]。ランダムなIVは、[BEAST攻撃への対策として有効である](https://ja.wikipedia.org/wiki/#BEAST攻撃 "wikilink")。一方、認証暗号で用いる共通鍵はTLSハンドシェイクプロトコルで共有されたmaster secretを用いる。

## バージョン

コンピュータの計算能力の向上とともに、認証の突破、暗号の解読、改竄も以前よりは容易に行えるようになり、セキュリティ確保のための技術も厳しさを増している。

**2017年現在では、TLS 1.2 以上のバージョンの実装が推奨され、TLS 1.1 以下のサポートを停止するサイトも出てきている。**\[27\]\[28\]\[29\]

| Defined |
| ------- |
| バージョン   |
| SSL 1.0 |
| SSL 2.0 |
| SSL 3.0 |
| TLS 1.0 |
| TLS 1.1 |
| TLS 1.2 |
| TLS 1.3 |

### SSL 1.0

[ネットスケープコミュニケーションズ](../Page/ネットスケープコミュニケーションズ.md "wikilink")社がSSLの最初のバージョンとして設計していたが、設計レビューの段階でプロトコル自体に大きな[脆弱性が発見され](https://ja.wikipedia.org/wiki/セキュリティホール#脆弱性 "wikilink")、破棄された。このため、2018年現在ではSSL 1.0を実装した製品はない。

### SSL 2.0

ネットスケープコミュニケーションズ社はSSL 1.0の問題を修正して再設計し、[1994年](../Page/1994年.md "wikilink")にSSL 2.0として発表した。また、同社の[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")である[Netscape Navigator](../Page/Netscape_Navigator_\(ネットスケープコミュニケーションズ\).md "wikilink") 1.1においてSSL 2.0を実装した。

その後、SSL 2.0にもいくつかの脆弱性が発見され、SSL 3.0において修正された。SSL 2.0の脆弱性のひとつは、ネゴシエーションの情報を改竄すると、提示する選択肢のうち最弱の[アルゴリズム](../Page/アルゴリズム.md "wikilink")を使わせることができ（ダウングレード攻撃）、[改竄](../Page/改竄.md "wikilink")を受けたことを検出できないというものである。さらに悪いことに、この脆弱性を利用すると、双方がSSL 3.0をサポートしていてもSSL 2.0で接続させることさえ可能になる。

SSL 3.0ではSSL 2.0との互換性を提供するにあたり、乱数領域を使った細工を加えることで、このような攻撃を検出する仕組みを組み込んだ。しかしこの細工が無効にされているサーバ環境も存在し、クライアントから見るとSSL 2.0を無効にしない限りこの脆弱性の影響を受ける可能性を否定できない\[30\]。SSL 3.0以降に対応した実装が十分に普及したものとして、[Internet Explorer 7や](../Page/Internet_Explorer.md "wikilink")[Mozilla Firefox 2](../Page/Mozilla_Firefox.md "wikilink")、[Opera 9などは](https://ja.wikipedia.org/wiki/Opera "wikilink")、初期状態でSSL 2.0を無効にしている\[31\]\[32\]\[33\]。この決定を受け、SSL 2.0しか対応していなかったサーバでも、SSL 3.0以降へ対応する動きが広まっている\[34\]。

SSL 2.0にはチェーン証明書がなく、[ルートCAから発行したSSLサーバ証明書しか使うことができない](../Page/ルート証明書.md "wikilink")。

2011年3月、RFC 6176 によってSSL 2.0の使用は禁止された。

### SSL 3.0

ネットスケープコミュニケーションズ社はSSL 2.0の問題を修正するとともに機能追加を行い、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")にSSL 3.0を発表した。また、Netscape Navigator 2.0においてSSL 3.0を実装した。SSL 3.0の仕様書については、2011年に[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")から歴史的文書という扱いでRFC 6101として公開された。

2014年10月にSSL 3.0の仕様上の脆弱性（[POODLE攻撃](https://ja.wikipedia.org/wiki/#POODLE攻撃 "wikilink")）が発見されたため、SSL 3.0への対応を打ち切り、TLS 1.0以降のみ対応への移行が望まれている。2015年6月、RFC 7568によってSSL 3.0の使用は禁止された。

**SSLについては、使うべきではない**。

### TLS 1.0

[IETFのTLSワーキンググループはRFC](../Page/Internet_Engineering_Task_Force.md "wikilink") 2246としてTLS 1.0を公表した。TLS 1.0の標準化作業は[1996年](../Page/1996年.md "wikilink")に開始され、年内に完了する予定だったが、いくつかの問題に阻まれ、公表は[1999年](../Page/1999年.md "wikilink")まで遅延した。

TLS 1.0が提供する機能はSSL 3.0とあまり変わらないが、アルゴリズムやルートCAの[自己署名証明書](../Page/自己署名証明書.md "wikilink")の取扱いなどの仕様の詳細が変更されたことに加え、これまであまり実装されていなかった選択肢のいくつかが必須と定められた。このため、TLS 1.0を実装した製品が普及するまでには、さらに数年を要した。

なおTLS 1.0はSSL 3.0より新しい規格であることを示すため、ネゴシエーションにおけるバージョン番号は3.1となっている。

### TLS 1.1

[2006年](../Page/2006年.md "wikilink")にRFC 4346としてTLS 1.1が制定された。TLS 1.0からの変更点は、新しく発見された攻撃手法に対する耐性の強化が中心である。特にCBC攻撃に対する耐性を上げるため、[初期化ベクトル](https://ja.wikipedia.org/wiki/初期化ベクトル "wikilink")を明示的に指定することにし、さらにパディングの処理も改善された。また、予期せぬ回線クローズ後に、セッションを再開できるようになった。共通鍵暗号アルゴリズムとして[AESが選択肢に加わった](../Page/Advanced_Encryption_Standard.md "wikilink")\[35\]。

ネゴシエーションにおけるバージョン番号は3.2となっている。

### TLS 1.2

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")8月にRFC 5246としてTLS 1.2が制定された。ハッシュのアルゴリズムに[SHA-2](https://ja.wikipedia.org/wiki/SHA-2 "wikilink")56が追加されたほか、[ブロック暗号](../Page/ブロック暗号.md "wikilink")について、従来の[CBCモードだけではなく](https://ja.wikipedia.org/wiki/暗号利用モード#CBC "wikilink")、[GCM](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink")、[CCMといった](https://ja.wikipedia.org/wiki/Counter_with_CBC-MAC "wikilink")[認証付き暗号](https://ja.wikipedia.org/wiki/認証付き暗号 "wikilink")を用いたcipher suiteが利用可能となった。また、AESに関する記述がRFC 5246自体に含まれるようになった。

ネゴシエーションにおけるバージョン番号は3.3となっている。

### TLS 1.3

新たなTLSのバージョンとしてTLS 1.3が提案されてきたが\[36\]、IETFは2018年3月23日に、ドラフト28を標準規格として承認し\[37\]\[38\]、同年8月10日にRFC 8446として公開した\[39\]。

TLS 1.2からの変更点としては、[データ圧縮](../Page/データ圧縮.md "wikilink")の非サポート、[forward secrecyではないcipher](https://ja.wikipedia.org/wiki/forward_secrecy "wikilink") suite（RSAのみを用いたもの）および[認証付き暗号](https://ja.wikipedia.org/wiki/認証付き暗号 "wikilink")ではないcipher suite（[CBCモードの](https://ja.wikipedia.org/wiki/暗号利用モード#CBC "wikilink")[ブロック暗号](../Page/ブロック暗号.md "wikilink")や[RC4](../Page/RC4.md "wikilink")を用いたもの）の廃止が挙げられる。なお名称をTLS 2.0やTLS 4等に変更することが検討されたが、最終的にTLS 1.3に落ち着いた。

## 暗号スイート

TLSではハンドシェイクプロトコルのClientHello・ServerHelloで、以後の通信で用いる暗号スイート (ciphersuite) を決定する。TLS 1.2を策定しているRFC 5246では、暗号スイートを以下のフォーマットで表現している：

`TLS_DHE_DSS_WITH_AES_256_CBC_SHA256`

これは次の意味である。

  - 鍵共有方式として以下のものを用いる：
      - EDH（Ephemeral Diffie-Hellman、後述）の通信に
      - [DSS署名したもの](https://ja.wikipedia.org/wiki/Digital_Signature_Algorithm "wikilink")
  - 認証暗号として平文にMACをつけた後に共通鍵暗号化する（いわゆるMAC-then-Encrypt (MtE) 型）のもので
      - 共通鍵暗号として[CBCモードの](https://ja.wikipedia.org/wiki/暗号利用モード#Cipher_Block_Chaining_\(CBC\) "wikilink")256ビット鍵[AESを用い](../Page/Advanced_Encryption_Standard.md "wikilink")、
      - MACとしては[SHA256ハッシュ関数をベースとした](https://ja.wikipedia.org/wiki/SHA-2 "wikilink")[HMAC](../Page/HMAC.md "wikilink")を用いる

TLS1.2では認証暗号としてMtE型のもののみならず、AES-GCMのような認証暗号専用に作られた暗号利用モードも用いる事ができるようになった。この場合MACはそもそも必要ない。

なお、RSA暗号とRSA署名を組み合わせる事で実現した鍵共有方式に対してはTLS_RSA_RSA_WITH…のようにRSAを2回書かず、TLS_RSA_WITH_…のように略記する。

鍵共有、共通鍵暗号、ハッシュ関数の全ての組み合わせが網羅されているわけではないので、同時に利用できない組み合わせも存在する。

### 鍵共有

SSL/TLS（の1つ以上のバージョンで）使用できる鍵共有方式は以下のとおりである。ここでDHは[Diffie-Hellmanの事である](../Page/ディフィー・ヘルマン鍵共有.md "wikilink")。なおDH-ANON、ECDH-ANONは[中間者攻撃](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")に対して脆弱であることから安全とはみなされていない。

  - **DH-ANON** (Anonymous DH)、**ECDH-ANON** (Anonymous ECDH) はそれぞれ、送信データに署名する事なくDH鍵共有、ECDH鍵共有を行う方式である。
  - **DHE-\*\*\***は**Ephemeral DH**と呼ばれるもので、鍵共有の際クライアント、サーバが、をランダムに選び、、を計算し、これらに署名文をつけた上で交換しあう方式である。、につける署名文を作成する署名方式は「\*\*\*」の部分に記載されたものを使う。**ECDHE-\*\*\***はDHEの楕円DH版である。
  - **DH-\*\*\***は**Fixed DH**もしくは**non-interactive DH**と呼ばれるもので、Diffie-Hellmanで用いるパラメータ（クライアントの、サーバの）がクライアントやサーバの公開鍵として認証局から公開鍵証明書を受け取っているケースのDiffie-Hellman鍵共有である。、に対する公開鍵証明書内の署名文を作成する署名方式は「\*\*\*」の部分に記載されたものを使う。**ECDH-\*\*\*** (**Fixed ECDH**) はFixed DHの楕円DH版である。
  - **RSA-\*\*\***はランダムに選んだ共有鍵をサーバの公開鍵でRSA暗号化し、暗号文を「\*\*\*」で指定された署名方式で署名したものをClientKeyExchangeにおいてクライアントがサーバに送る方式である。（ServerKeyExchangeでは何も送らない）。

いずれの鍵共有においても共有された鍵 (premaster secret) を用いた擬似ランダム関数にクライアントが選んだ乱数とサーバが選んだ乱数等を並べたものを入力する事で最終的なmaster secretを得る。これによりリプレイ攻撃を防いでいる。

これらの鍵共有方式の対応状況は以下のとおりである：

<table>
<caption>TLSの各バージョンで使用できる認証・鍵交換アルゴリズム</caption>
<thead>
<tr class="header">
<th><p>アルゴリズム</p></th>
<th><p>SSL 2.0</p></th>
<th><p>SSL 3.0</p></th>
<th><p>TLS 1.0</p></th>
<th><p>TLS 1.1</p></th>
<th><p>TLS 1.2</p></th>
<th><p>TLS 1.3</p></th>
<th><p>状況</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>TLS 1.2向けにRFCで定義済み</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>[40]</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>RFC草稿で提案中</p></td>
</tr>
</tbody>
</table>

を用いた TLS_PSK、を用いた TLS_SRP、[ケルベロス認証](../Page/ケルベロス認証.md "wikilink")を用いた KRB5 も存在する。

[独立国家共同体](../Page/独立国家共同体.md "wikilink")の[GOST規格](https://ja.wikipedia.org/wiki/GOST規格 "wikilink")によって規定された鍵共有アルゴリズムであるGOST R 34.10も提案されている（同じGOST規格による暗号化・改竄検出アリゴリズムとの組み合わせに限定）\[41\]。

### 認証暗号

#### 共通鍵暗号

認証暗号に用いる[共通鍵暗号](../Page/共通鍵暗号.md "wikilink")として以下のものがある。

<table>
<caption>TLS/SSLの各バージョンで使用できる暗号化アルゴリズム</caption>
<thead>
<tr class="header">
<th><p>暗号化</p></th>
<th><p>プロトコルバージョン</p></th>
<th><p>状況</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>種類</p></td>
<td><p>アルゴリズム</p></td>
<td><p>暗号強度 (bit)</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/ブロック暗号.md" title="wikilink">ブロック暗号</a><br />
（<a href="../Page/暗号利用モード.md" title="wikilink">暗号利用モード</a>）</p></td>
<td><p><a href="../Page/Advanced_Encryption_Standard.md" title="wikilink">AES</a> <a href="https://ja.wikipedia.org/wiki/Galois/Counter_Mode" title="wikilink">GCM</a>[42][43]</p></td>
<td><p>256, 128</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Advanced_Encryption_Standard.md" title="wikilink">AES</a> <a href="https://ja.wikipedia.org/wiki/Counter_with_CBC-MAC" title="wikilink">CCM</a>[44][45]</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Advanced_Encryption_Standard.md" title="wikilink">AES</a> <a href="https://ja.wikipedia.org/wiki/暗号利用モード#CBC" title="wikilink">CBC</a>[46]</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Camellia.md" title="wikilink">Camellia</a> <a href="https://ja.wikipedia.org/wiki/Galois/Counter_Mode" title="wikilink">GCM</a>[47][48]</p></td>
<td><p>256, 128</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Camellia.md" title="wikilink">Camellia</a> <a href="https://ja.wikipedia.org/wiki/暗号利用モード#CBC" title="wikilink">CBC</a>[49][50]</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/ARIA_(暗号)" title="wikilink">ARIA</a> <a href="https://ja.wikipedia.org/wiki/Galois/Counter_Mode" title="wikilink">GCM</a>[51][52]</p></td>
<td><p>256, 128</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/ARIA_(暗号)" title="wikilink">ARIA</a> <a href="https://ja.wikipedia.org/wiki/暗号利用モード#CBC" title="wikilink">CBC</a>[53][54]</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/SEED_(暗号).md" title="wikilink">SEED</a> <a href="https://ja.wikipedia.org/wiki/暗号利用モード#CBC" title="wikilink">CBC</a>[55][56]</p></td>
<td><p>128</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/トリプルDES.md" title="wikilink">3DES EDE</a> <a href="https://ja.wikipedia.org/wiki/暗号利用モード#CBC" title="wikilink">CBC</a>[57]</p></td>
<td><p>112</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/暗号利用モード#CTR" title="wikilink">CNT</a>[58]</p></td>
<td><p>256</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/International_Data_Encryption_Algorithm" title="wikilink">IDEA</a> <a href="https://ja.wikipedia.org/wiki/暗号利用モード#CBC" title="wikilink">CBC</a>[59][60]</p></td>
<td><p>128</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Data_Encryption_Standard.md" title="wikilink">DES</a> <a href="https://ja.wikipedia.org/wiki/暗号利用モード#CBC" title="wikilink">CBC</a>[61][62]</p></td>
<td><p>56</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>40[63]</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/RC2.md" title="wikilink">RC2</a> <a href="https://ja.wikipedia.org/wiki/暗号利用モード#CBC" title="wikilink">CBC</a>[64]</p></td>
<td><p>40[65]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/ストリーム暗号.md" title="wikilink">ストリーム暗号</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ChaCha20" title="wikilink">ChaCha20</a>+<a href="https://ja.wikipedia.org/wiki/Poly1305" title="wikilink">Poly1305</a>[66][67]</p></td>
<td><p>256</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/RC4.md" title="wikilink">RC4</a>[68]</p></td>
<td><p>128</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>40[69]</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>暗号化なし</p></td>
<td><p>Null[70]</p></td>
<td><p>-</p></td>
</tr>
</tbody>
</table>

[AES](../Page/Advanced_Encryption_Standard.md "wikilink") CBCはTLS 1.0を定義する RFC 2246 には含まれていないが、RFC 3268 で追加された。TLS 1.1を定義する RFC 4346 からは RFC 3268 が参照されており、さらにTLS 1.2では定義である RFC 5246 にAES CBCに関する記述が取り込まれた。また、[認証付き暗号](https://ja.wikipedia.org/wiki/認証付き暗号 "wikilink")による[AES](../Page/Advanced_Encryption_Standard.md "wikilink") [GCM](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink") (RFC 5288, RFC 5289)、[AES](../Page/Advanced_Encryption_Standard.md "wikilink") [CCM](https://ja.wikipedia.org/wiki/Counter_with_CBC-MAC "wikilink") (RFC 6655, RFC 7251) が追加されている。[IDEA](https://ja.wikipedia.org/wiki/International_Data_Encryption_Algorithm "wikilink") CBC、[DES](../Page/Data_Encryption_Standard.md "wikilink") CBCはTLS 1.2で廃止された（RFC 5469 に解説がある）。

[ブロック暗号](../Page/ブロック暗号.md "wikilink")の[CBCモードでの利用については](https://ja.wikipedia.org/wiki/暗号利用モード#CBC "wikilink")、TLS 1.0以前において[BEAST攻撃と呼ばれる攻撃が可能であることが明らかとなっており](https://ja.wikipedia.org/wiki/#BEAST攻撃 "wikilink")、クライアント側、サーバ側での対応が必要とされている。TLS 1.1以降ではこの攻撃への根本的な対処として[初期化ベクトル](https://ja.wikipedia.org/wiki/初期化ベクトル "wikilink")を明示的に指定し、パディングの処理が改善された。ブロック暗号であっても[GCM](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink")、[CCMなどの](https://ja.wikipedia.org/wiki/Counter_with_CBC-MAC "wikilink")[認証付き暗号](https://ja.wikipedia.org/wiki/認証付き暗号 "wikilink")を用いる場合にはこれらの攻撃を受けない。

[ストリーム暗号](../Page/ストリーム暗号.md "wikilink")である[RC4](../Page/RC4.md "wikilink")は前述のBEAST攻撃を受けることはないが、RC4には仕様上の脆弱性が存在する（[RC4攻撃](https://ja.wikipedia.org/wiki/#RC4攻撃 "wikilink")）。2015年2月、TLSのすべてのバージョンにおいてRC4の利用を禁止する RFC 7465 が公開された。ストリーム暗号である[ChaCha20](https://ja.wikipedia.org/wiki/ChaCha20 "wikilink")と認証のための[Poly1305](https://ja.wikipedia.org/wiki/Poly1305 "wikilink")を組み合わせたChaCha20+Poly1305が RFC 7905 として標準化されている。

いくつかの国家標準に基づく暗号化アルゴリズムもTLSで利用可能であり、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の[CRYPTREC](../Page/CRYPTREC.md "wikilink")による推奨暗号である[Camellia](../Page/Camellia.md "wikilink")（CBCモード：RFC 4132、RFC 5932、RFC 6367、GCM：RFC 6367）、[韓国の情報通信標準規格に採用されている](../Page/大韓民国.md "wikilink")[SEED](../Page/SEED_\(暗号\).md "wikilink")（CBCモード：RFC 4162）、[ARIA](https://ja.wikipedia.org/wiki/ARIA_\(暗号\) "wikilink")（CBCモードおよびGCM：RFC 6209）が追加されている。また、[独立国家共同体](../Page/独立国家共同体.md "wikilink")の[GOST規格](https://ja.wikipedia.org/wiki/GOST規格 "wikilink")によって規定された暗号化アルゴリズムであるGOST 28147-89も提案されている\[71\]。

SSLが設計された当時は、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")によって[高強度暗号アルゴリズムの輸出が規制されていた](https://ja.wikipedia.org/wiki/アメリカ合衆国からの暗号の輸出規制 "wikilink")。そのため、全世界で共通して利用できるアルゴリズムとして、DES・[RC2](../Page/RC2.md "wikilink")・RC4に関して暗号強度を40ビットに制限したものが導入されていた。これらはTLS 1.1以降では利用が禁止されている。

また、鍵共有のみを行い暗号化は行わないこと (NULL) も可能であるが、平文でのやりとりとなることから安全とはみなされていない。

#### MAC

TLS/SSLの各バージョンで使用できるMACの選択肢は以下のとおりである。下欄の「AEAD」（Authenticated Encryption with Associated Data、認証暗号）は、共通鍵暗号として認証暗号を選んでいるのでMACを用いない事を意味する。

<table>
<caption>TLS/SSLの各バージョンで使用できる改竄検出</caption>
<thead>
<tr class="header">
<th><p>アルゴリズム</p></th>
<th><p>SSL 2.0</p></th>
<th><p>SSL 3.0</p></th>
<th><p>TLS 1.0</p></th>
<th><p>TLS 1.1</p></th>
<th><p>TLS 1.2</p></th>
<th></th>
<th><p>状況</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/HMAC.md" title="wikilink">HMAC</a>-<a href="../Page/MD5.md" title="wikilink">MD5</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>TLS 1.2向けにRFCで定義済み</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/HMAC.md" title="wikilink">HMAC</a>-<a href="https://ja.wikipedia.org/wiki/SHA-1" title="wikilink">SHA1</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/HMAC.md" title="wikilink">HMAC</a>-<a href="https://ja.wikipedia.org/wiki/SHA-2" title="wikilink">SHA256/384</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/認証付き暗号" title="wikilink">AEAD</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[72]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>RFC草稿で提案中</p></td>
</tr>
<tr class="even">
<td><p>[73]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

[独立国家共同体](../Page/独立国家共同体.md "wikilink")の[GOST規格](https://ja.wikipedia.org/wiki/GOST規格 "wikilink")によって規定されたアルゴリズムであるGOST 28147-89に基づくMACおよび、GOST R 34.11も提案されている（同じGOST規格による鍵共有・暗号化アリゴリズムとの組み合わせに限定）\[74\]。

## 実装

### ウェブサイト

<table>
<caption>ウェブサイトにおけるTLS/SSLの対応状況</caption>
<thead>
<tr class="header">
<th><p>プロトコル</p></th>
<th><p>ウェブサイトにおけるサポート[75]</p></th>
<th><p>セキュリティ[76][77]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SSL 2.0</p></td>
<td><p>1.6%</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>SSL 3.0</p></td>
<td><p>6.7%</p></td>
<td><p>[78]</p></td>
</tr>
<tr class="odd">
<td><p>TLS 1.0</p></td>
<td><p>65.0%</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>TLS 1.1</p></td>
<td><p>75.1%</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>TLS 1.2</p></td>
<td><p>96.0%</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>TLS 1.3</p></td>
<td><p>18.4%</p></td>
<td></td>
</tr>
</tbody>
</table>

  - 注

### ウェブブラウザ

2016年4月現在、主要なウェブブラウザの最新版ではTLS 1.0、1.1、1.2のすべてが既定で有効であるが、過去のバージョンのOS向けなど、最新ではないがサポートが継続しているウェブブラウザのいくつかのバージョンではそうではない。

  - TLS 1.1、1.2に対応しているが既定で無効：Internet Explorer 10（Windows Server 2012向け）
  - TLS 1.1、1.2に未対応：Internet Explorer 9（Windows Vista / Server 2008向け）

既知の脆弱性のいくつかへの対応は十分ではない。

  - [POODLE攻撃への対応](https://ja.wikipedia.org/wiki/#POODLE攻撃 "wikilink")：いくつかのブラウザではTLS_FALLBACK_SCSVを実装済みでSSL 3.0へのフォールバックを抑止することが可能となっているが、これはクライアント側だけでなくサーバ側での対応も必要である。SSL 3.0そのものの無効化、"anti-POODLE record splitting"の実装、あるいはSSL 3.0におけるCBCモードのcipher suiteの無効化が根本的な対策となる。
      - Google Chrome：完了（バージョン33においてTLS_FALLBACK_SCSVを実装、バージョン39においてSSL 3.0へのフォールバックを無効化、バージョン40においてSSL 3.0を既定で無効化。バージョン44においてSSL 3.0のサポートを廃止）
      - Mozilla Firefox：完了（バージョン34においてSSL 3.0を既定で無効化およびSSL 3.0へのフォールバックを無効化、バージョン35においてTLS_FALLBACK_SCSVを実装。延長サポート版でもESR 31.3においてSSL 3.0を無効化およびTLS_FALLBACK_SCSVを実装。バージョン39においてSSL 3.0のサポートを廃止）
      - Internet Explorer：部分的（バージョン11のみ、2015年2月のアップデートにおいて保護モードにおけるSSL 3.0へのフォールバックを既定で無効化。2015年4月にSSL 3.0自体を既定で無効化。バージョン10以前では対策は講じられていない）
      - Opera：完了（バージョン20においてTLS_FALLBACK_SCSVを実装、バージョン25において"anti-POODLE record splitting"を実装、バージョン27においてSSL 3.0を既定で無効化。バージョン31においてSSL 3.0のサポートを廃止）
      - Safari：完了（[OS X v10.8以降およびiOS](https://ja.wikipedia.org/wiki/OS_X_Mountain_Lion "wikilink") 8.1以降のみ、POODLEへの対策としてSSL 3.0においてCBCモードのcipher suiteを無効化した。これによりPOODLEの影響を受けることはなくなるが、SSL 3.0においてCBCモードを無効化したことで、脆弱性が指摘されているRC4しか利用できなくなるという問題が生じている。[OS X v10.11およびiOS](https://ja.wikipedia.org/wiki/OS_X_El_Capitan "wikilink") 9においてSSL 3.0のサポートを廃止）
  - [RC4攻撃への対応](https://ja.wikipedia.org/wiki/#RC4攻撃 "wikilink")
      - Google Chromeでは、バージョン43以降はホストがRC4以外のアルゴリズムを用いたCipher Suiteに対応していない場合に限りRC4を用いたCipher Suiteがフォールバックとして利用されるようになった。バージョン48以降では、RC4を用いたCipher Suiteのすべてが既定で無効化された。
      - Firefoxでは、バージョン36以降はホストがRC4以外のアルゴリズムを用いたCipher Suiteに対応していない場合に限りRC4を用いたCipher Suiteがフォールバックとして利用されるようになった。バージョン44以降では、RC4を用いたCipher Suiteのすべてが既定で無効化された。
      - Operaでは、バージョン30以降はホストがRC4以外のアルゴリズムを用いたCipher Suiteに対応していない場合に限りRC4を用いたCipher Suiteがフォールバックとして利用されるようになった。バージョン35以降では、RC4を用いたCipher Suiteのすべてが既定で無効化された。
      - Windows 7 / Server 2008 R2およびWindows 8 / Server 2012向けのInternet Explorerでは、RC4の優先度を最低としている。Windows 8.1 / Server 2012 R2向けのInternet Explorer 11およびWindows Phone 8.1向けのInternet Explorer Mobile 11およびWindows 10向けのEdgeでは、ホストが他のアルゴリズムに非対応の場合のフォールバックを除きRC4を無効としている（Windows 7 / Server 2008 R2およびWindows 8 / Server 2012向けのInternet Explorerでもレジストリからフォールバックを除きRC4を無効化することが可能）。2016年4月の月例アップデートにおいて、Inter Explorer 11およびEdgeにおいてRC4を用いたCipher Suiteのすべてが既定で無効化される予定であったが延期されている。

<!-- end list -->

  - [FREAK攻撃への対応](https://ja.wikipedia.org/wiki/#FREAK "wikilink"):
      - [Android](../Page/Android.md "wikilink") 4以前の[標準ブラウザはFREAK攻撃に対して脆弱である](https://ja.wikipedia.org/wiki/Androidブラウザ "wikilink")。
      - Internet Explorer 11 MobileはFREAK攻撃に対して脆弱である。
      - Google Chrome（Windows版を除く）、Internet Explorer、Safari（デスクトップ版、iOS版）、Opera（Windows版を除く）はFREAK攻撃に対して対応済みである。
      - Mozilla Firefox、Google Chrome（Windows版）、Opera（Windows版）はFREAK攻撃の影響を受けない。

<div style="height:auto; overflow: auto; text-align: left">

</div>

### ライブラリ

TLS/SSLライブラリの多くは[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")である。

<table>
<caption>ライブラリにおけるTLS/SSLの対応状況</caption>
<thead>
<tr class="header">
<th><p>実装</p></th>
<th><p>SSL 2.0（安全ではない）</p></th>
<th><p>SSL 3.0（安全ではない）</p></th>
<th><p>TLS 1.0</p></th>
<th><p>TLS 1.1</p></th>
<th><p>TLS 1.2</p></th>
<th><p>TLS 1.3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Botan" title="wikilink">Botan</a></p></td>
<td></td>
<td><p>[79]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/GnuTLS" title="wikilink">GnuTLS</a></p></td>
<td><p>[80]</p></td>
<td><p>[81]</p></td>
<td></td>
<td></td>
<td></td>
<td><p>[82]</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>[83]</p></td>
<td><p>[84]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/LibreSSL" title="wikilink">LibreSSL</a></p></td>
<td><p>[85]</p></td>
<td><p>[86]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>[87]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>[88]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Network_Security_Services" title="wikilink">Network Security Services</a></p></td>
<td></td>
<td><p>[89]</p></td>
<td></td>
<td><p>[90]</p></td>
<td><p>[91]</p></td>
<td><p>[92]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/OpenSSL" title="wikilink">OpenSSL</a></p></td>
<td><p>[93]</p></td>
<td></td>
<td></td>
<td><p>[94]</p></td>
<td><p>[95]</p></td>
<td><p>[96]</p></td>
</tr>
<tr class="even">
<td><p>[97]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/SChannel" title="wikilink">SChannel XP/2003</a>[98]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/SChannel" title="wikilink">SChannel Vista/2008</a>[99]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/SChannel" title="wikilink">SChannel 7/2008R2</a>[100]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/SChannel" title="wikilink">SChannel 8/1012</a>[101]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/SChannel" title="wikilink">SChannel 8.1/2012R2, 10 v1507/v1511</a>[102]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/SChannel" title="wikilink">SChannel 10 v1607/2016</a>[103]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Secure Transport OS X v10.2-10.8 / iOS 1-4</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Secure Transport OS X v10.9-10.10 / iOS 5-8</p></td>
<td></td>
<td></td>
<td></td>
<td><p>[104]</p></td>
<td><p>[105]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Secure Transport OS X v10.11 / iOS 9</p></td>
<td></td>
<td><p>[106]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>SharkSSL</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/wolfSSL" title="wikilink">wolfSSL</a></p></td>
<td></td>
<td><p>[107]</p></td>
<td></td>
<td></td>
<td></td>
<td><p>[108]</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>実装</p></td>
<td><p>SSL 2.0（安全ではない）</p></td>
<td><p>SSL 3.0（安全ではない）</p></td>
<td><p>TLS 1.0</p></td>
<td><p>TLS 1.1</p></td>
<td><p>TLS 1.2</p></td>
<td><p>TLS 1.3</p></td>
</tr>
</tbody>
</table>

  - 注

## 課題

### バーチャルホスト

TLSは、TCP/IPネットワークでホスト名ベースの[バーチャルホスト](../Page/バーチャルホスト.md "wikilink")を構成する際に問題となる。TCP/IPでは通信を開始する前にホスト名を[解決し](https://ja.wikipedia.org/wiki/名前解決 "wikilink")、実際には[IPアドレス](../Page/IPアドレス.md "wikilink")とポート番号で接続先を識別している。このためTLSのネゴシエーションの時点では、バーチャルホストのうちどのホスト名を期待しているのか判断できず、ホスト名ごとに異なるサーバー証明書を使い分けることができない。

TLSの拡張機能を定義するRFC 6066では、ネゴシエーション時にホスト名を伝える手段として[Server Name Indication](https://ja.wikipedia.org/wiki/Server_Name_Indication "wikilink") (SNI) を規定している。用例としては、[HTTP](https://ja.wikipedia.org/wiki/HTTP "wikilink")の最新バージョンである[HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")においてTLSを利用する際はSNIの利用が必須とされている。

一方、証明書を使い分けず、1つの証明書を複数のバーチャルホストで使い回す方式も広く利用されている。[X.509](../Page/X.509.md "wikilink")証明書のフォーマットについて記述した[RFC5280](https://ja.wikipedia.org/wiki/RFC5280 "wikilink")では、発行先ホスト名を保持するsubjectAltNameはひとつの証明書に複数のエントリを作成できると規定している。これを利用して、ホストに収容されたすべてのバーチャルホストに対応したsubjectAltNameを保持する証明書をクライアントに提示すれば良い。

また、発行先ホスト名に[ワイルドカードを使う方法も考えられる](../Page/ワイルドカード_\(情報処理\).md "wikilink")。HTTP over SSL/TLS (HTTPS) を定義するRFC 2818は、ワイルドカードの適用について記述している。バーチャルホストの対象が、ひとつのドメイン名の中のホストであれば、この方法で対応できる場合もある。

どの方法も実装によって対応状況にバラつきがあり、環境によっては使えない可能性がある。なおIPアドレスベースのバーチャルホストであれば、ネゴシエーションの時点で確実にどのバーチャルホストを期待しているか判断できるので、問題なく証明書を使い分けることができる。

## TLS/SSLの既知の脆弱性

TLS/SSLに対する攻撃のうち主なものを以下に挙げる。2015年2月に、TLS/SSLに対する既知の攻撃についての情報をまとめたRFC 7457がIETFから公開されている。

### 暗号の危殆化を利用したもの

TLS 1.2ではすでに危殆化したRC4、MD5、SHA1が選択可能であり、この事が脆弱性の原因となっている。

MD5はすでに衝突が容易に見つかるレベルまで危殆化しているため、これを利用した**SLOTH攻撃** (CVE-2015-7575) が知られている。

SHA1もFreestart Collision\[109\]が見つかっており安全ではない。

#### RC4

RC4もTLSのすべてのバージョンにおいて利用を禁止するRFC 7465が公開された。[Mozilla](../Page/Mozilla.md "wikilink")および[マイクロソフト](../Page/マイクロソフト.md "wikilink")ではRC4を無効化することを推奨している\[110\]\[111\]\[112\]\[113\]。

[RC4](../Page/RC4.md "wikilink")そのものに対する攻撃法は多く報告されているが、TLS/SSLにおいてRC4を用いたCipher Suiteについては、その脆弱性に対処されており安全であると考えられていた。2011年には、ブロック暗号のCBCモードの取り扱いに関する脆弱性であったBEAST攻撃への対応策の一つとして、ストリーム暗号であるためその影響を受けないRC4に切り替えることが推奨されていた\[114\]。しかし、2013年にTLS/SSLでのRC4への効果的な攻撃が報告され、BEASTへの対応としてRC4を用いることは好ましくないとされた\[115\]。RC4に対する攻撃は、AlFardan、Bernstein、Paterson、Poettering、Schuldtによって報告された。新たに発見されたRC4の鍵テーブルにおける統計的な偏り\[116\]を利用し、平文の一部を回復可能であるというものである\[117\]\[118\]。この攻撃では、13 × 2<sup>20</sup>の暗号文を用いることで128ビットのRC4が解読可能であることが示され、2013年の[USENIX](../Page/USENIX.md "wikilink")セキュリティシンポジウムにおいて「実現可能」と評された\[119\]\[120\]。2013年現在では、[NSAのような機関であればTLS](../Page/アメリカ国家安全保障局.md "wikilink")/SSLを利用したとしてもRC4を解読可能であるとの疑惑がある\[121\]。

2015年現在ではクライアントのほとんどは既にBEASTへの対処が完了していることから、RC4はもはや最良の選択肢ではなくなっており、TLS 1.0以前においてもCBCモードを用いることがより良い選択肢となっている\[122\]。

### ダウングレード攻撃

#### FREAK および Logjam

かつて[アメリカ合衆国からの暗号の輸出規制](https://ja.wikipedia.org/wiki/アメリカ合衆国からの暗号の輸出規制 "wikilink")が厳しかった時期に、規制を回避するために一時的に512ビットのRSA鍵を生成して、そちらで通信を行うというような手法が存在した\[123\]。この手法については、一時的な公開鍵を[素因数分解](../Page/素因数分解.md "wikilink")することが可能であれば[中間者攻撃](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")が成立することが1998年時点で指摘されていたが\[124\]、コンピュータの性能向上、[クラウドコンピューティング](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink")の普及により素因数分解が個人レベルですら現実的となったこと、さらに[2015年](../Page/2015年.md "wikilink")には、[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")、[Safari](../Page/Safari.md "wikilink")、[Android](../Page/Android.md "wikilink")などでは**輸出用でない**暗号スイートでも512ビットの一時鍵を受け入れてしまう実装となっていたことが判明し、**FREAK** (Factoring RSA Export Keys)\[125\]として問題が再浮上している。

対策としては、すでに脆弱となっている輸出対応暗号の無効化、クライアント側では規格書通り、輸出暗号以外で一時的RSA鍵を使わないようにする\[126\]、ということが挙げられる。

2015年5月、**Logjam**と呼ばれる脆弱性が発見された。これも、FREAKと同様に輸出用の512ビットの一時鍵を受け入れてしまうものである\[127\]。FREAKとは異なり、LogjamはTLSプロトコル自体の脆弱性である。発見時点において、主要なブラウザのすべてがLogjamに対して脆弱である。

#### バージョンロールバック攻撃

**False Start**\[128\]（[Google Chromeで有効化された](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")\[129\]）やSnap StartといったTLS/SSLを高速化する変法は、攻撃者が一定条件下において本来利用可能なTLS/SSLのバージョンよりも低いバージョンでTLS/SSL接続を行うよう仕向けること\[130\]や、クライアントからサーバへ送られる利用可能なCipher Suiteの一覧を改竄し、より低い暗号強度やより弱い暗号化アルゴリズム・鍵交換アルゴリズムを使用するよう仕向けること\[131\]が可能であると報告されている。さらに、特定の環境においては、攻撃者がオフラインで暗号化に用いられた鍵を回復し、暗号化されたデータにアクセスすることも可能であることが[Association for Computing Machinery](../Page/Association_for_Computing_Machinery.md "wikilink") (ACM) のコンピュータセキュリティカンファレンスで報告された\[132\]。

### Mac-then-Encrypt型の認証暗号に関するもの

#### BEAST攻撃

2011年9月23日、暗号研究者のThai DuongとJuliano Rizzoが、**BEAST** (**Browser Exploit Against SSL/TLS**)\[133\] と呼ばれるTLS 1.0における[ブロック暗号](../Page/ブロック暗号.md "wikilink")の[CBCモードの取り扱いに関する脆弱性のコンセプトを](https://ja.wikipedia.org/wiki/暗号利用モード#CBC "wikilink")[Javaアプレット](../Page/Javaアプレット.md "wikilink")の[同一生成元ポリシー](https://ja.wikipedia.org/wiki/同一生成元ポリシー "wikilink")違反によって実証した\[134\]\[135\]。この脆弱性そのものは2002年にPhillip Rogawayによって発見されていた\[136\]が、2011年の発表までは実用的な[エクスプロイト](https://ja.wikipedia.org/wiki/エクスプロイト "wikilink")は報告されていなかった。

2006年に発表されたTLS 1.1においてBEASTへの脆弱性は修正されていたが、2011年の実証までTLS 1.1への対応はクライアント、サーバの双方でほとんど進んでいなかった。

Google ChromeおよびFirefoxはBEASTによる影響を直接的に受けることはないが\[137\]\[138\]、MozillaはTLS/SSLのためのライブラリである[Network Security Services](https://ja.wikipedia.org/wiki/Network_Security_Services "wikilink") (NSS) に対して、BEASTおよびそれに類似した[選択平文攻撃](https://ja.wikipedia.org/wiki/選択平文攻撃 "wikilink")に対するTLS 1.0以前で有効な対応策を2011年に施した。NSSは、[Mozilla FirefoxなどのMozillaのソフトウェアだけでなく](../Page/Mozilla_Firefox.md "wikilink")、[Google Chromeなど他のブラウザでも用いられているライブラリである](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")。NSSでのTLS 1.1以降への対応は2012年までずれこみ、FirefoxでTLS 1.1以降を既定で利用可能となったのは2014年のバージョン27である。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")は2012年1月10日にSecurity Bulletin MS12-006を発表し、Windowsで用いられているライブラリである[SChannel](https://ja.wikipedia.org/wiki/SChannel "wikilink")に対して修正を加えた\[139\]。[Windows 7以降では](../Page/Microsoft_Windows_7.md "wikilink")、TLS 1.1以降が利用可能である。

[アップル製品では](../Page/アップル_\(企業\).md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")ではv10.9においてTLS 1.1以降への対応およびTLS 1.0以前におけるBEAST脆弱性への対応がなされているが、v10.8以前では、TLS 1.1以降への対応、TLS 1.0以前におけるBEAST脆弱性への対応のいずれも行われていない。[iOSでは](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、5以降ではTLS 1.1以降が利用可能であるが、TLS 1.0以前におけるBEAST脆弱性への対応は行われていない。iOS 7ではじめてTLS 1.0以前におけるBEAST脆弱性への対応が行われた。

### パディング攻撃

TLSの初期のバージョンはパディングオラクル攻撃に対して脆弱であることが2002年に報告された。

#### Lucky Thirteen

2013年には、**Lucky Thirteen**攻撃（[英語版](https://ja.wikipedia.org/wiki/:en:Lucky_Thirteen_attack "wikilink")）と呼ばれる新たなパディング攻撃が報告されている。2014年現在では、多くの実装においてLucky Thirteen攻撃に対して対応済みである。

#### POODLE攻撃

2014年9月15日、[Google](../Page/Google.md "wikilink")の研究者によって、SSL 3.0の設計に脆弱性が存在することが発表された\[140\] ([CVE-2014-3566](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2014-3566))。これは、SSL 3.0においてブロック暗号を[CBCモードで使用した際に](https://ja.wikipedia.org/wiki/暗号利用モード#CBC "wikilink")[パディング攻撃が可能となるものであり](https://ja.wikipedia.org/wiki/#パディング攻撃 "wikilink")、**POODLE** (**Padding Oracle On Downgraded Legacy Encryption**) と名付けられた。平均してわずか256回のリクエストで暗号文の1バイトの解読が可能となる\[141\]\[142\]。CVE IDは[CVE-2014-3566](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2014-3566)である。

この脆弱性はSSL 3.0の仕様のみに存在するものでありTLS 1.0以降に影響はないが、主要なすべてのブラウザではTLSでのハンドシェイクが失敗した場合にSSL 3.0での接続にダウングレードする。そのため、攻撃者は[バージョンロールバック攻撃によってSSL](https://ja.wikipedia.org/wiki/#バージョンロールバック攻撃 "wikilink") 3.0での接続を行わせることでこの脆弱性を利用可能となる\[143\]\[144\]。

POODLE攻撃への根本的な対処法は、少なくともクライアント、サーバのどちらかでSSL 3.0を無効化することである。しかし、古いクライアント、サーバなどではTLS 1.0以降に対応していないため、互換性を考慮してSSL 3.0を無効化できない場合がある。そこで、POODLEの発見者は、TLS_FALLBACK_SCSV\[145\]の実装を推奨している。この実装によりTLSからSSL 3.0へのフォールバックが抑止されるが\[146\]\[147\]、これはクライアント側だけでなくサーバ側の対応も必要である。

[Google ChromeブラウザやGoogleサービスのサーバは既にTLS](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")_FALLBACK_SCSVに対応しており、加えて数か月以内にこれらクライアント、サーバからSSL 3.0のサポートを除去する予定である\[148\]。2014年11月リリースのバージョン39においてSSL 3.0へのフォールバックを、2015年1月リリースのバージョン40においてSSL 3.0そのものを既定で無効化している。

[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")もGoogle Chromeと同様にTLS_FALLBACK_SCSVを実装済みであるほか、バージョン25において"anti-POODLE record splitting"と呼ばれる異なる対策を実装した\[149\]。

Mozillaでは2014年12月リリースの[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") 34およびESR 31.3からSSL 3.0を無効化したほか、Firefox 35においてTLS_FALLBACK_SCSVをサポートした\[150\]。

マイクロソフトでは、グループポリシーからSSL 3.0を無効化する方法を公開しているほか\[151\]、10月29日にWindows Vista、Server 2003およびそれ以降のIEにおいてSSL 3.0を無効化する"Fix it"を公開し、数か月以内にIEおよびマイクロソフトのオンラインサービスにおいてSSL 3.0を既定で無効化する方針を表明した\[152\]。2015年2月のアップデートにおいて、IE 11の保護モードにおいてSSL 3.0へのフォールバックを既定で無効化した\[153\]。加えて、2015年4月にIE 11においてSSL 3.0自体を既定で無効化した\[154\]。

[Safari](../Page/Safari.md "wikilink")（OS X v10.8以降およびiOS 8.1以降）では、POODLEへの対策としてSSL 3.0においてCBCモードのcipher suiteを無効化した\[155\]\[156\]。これによりPOODLEの影響を受けることはなくなるが、SSL 3.0においてCBCモードを無効化したことで、脆弱性が指摘されている[RC4](../Page/RC4.md "wikilink")しか利用できなくなるという問題が生じている。

サーバ側では、[NSSが](https://ja.wikipedia.org/wiki/Network_Security_Services "wikilink")2014年10月3日にリリースされたバージョン3.17.1および10月27日にリリースされた3.16.2.3でTLS_FALLBACK_SCSVに対応したほか\[157\]\[158\]、2015年4月までにSSL 3.0を既定で無効化する予定である\[159\]。[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")は、10月15日リリースのバージョン1.0.1j、1.0.0、0.9.8zcでTLS_FALLBACK_SCSVに対応した\[160\]。[LibreSSL](https://ja.wikipedia.org/wiki/LibreSSL "wikilink")では、10月16日リリースのバージョン2.1.1でSSL 3.0を既定で無効化した\[161\]。

2014年12月8日に、SSL 3.0ではなくTLS 1.0から1.2に対して有効なPOODLE攻撃の変法が報告された。この変法はTLSの仕様においてサーバ側に要求されているパディングのチェックを正しく行わない実装において、SSL 3.0を無効にしていたとしてもPOODLE攻撃が可能となるというものである\[162\]。すなわち、SSL 3.0に対するものが仕様そのものの脆弱性であるのに対し、TLS 1.0以降に対するものは不適切な実装による脆弱性である。SSL Pulseでは、公開前の時点でHTTPS対応のサーバのうちおよそ10%がこの変法に対して脆弱であるとしている\[163\]。この変法のCVE IDは[CVE-2014-8730](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2014-8730)である。この変法では、SSL 3.0へダウングレードさせる必要がなくTLS 1.2のままで攻撃が可能であるなど、オリジナルのSSL 3.0に対するPOODLE攻撃よりも実行が容易であるとされる\[164\]。

### 圧縮サイドチャネル攻撃

TLS1.2では平文を圧縮した後に暗号化を施す。しかし圧縮後の平文のビット長さは圧縮前の平文に依存し、しかも暗号文のビット長は暗号化する文書＝圧縮後の平文のビット長に依存するので、暗号文長から平文の情報が攻撃者に漏れてしまう。この事実を利用した攻撃を**圧縮サイドチャネル攻撃**という。TLS1.2には以下の様な圧縮サイドチャネル攻撃が知られている。

#### CRIME攻撃

2012年にBEAST攻撃の報告者によって、TLSにおいてデータ圧縮が有効な場合において、本来第三者に対して秘密であるべきCookieの内容が回復可能となる**CRIME**（**Compression Ratio Info-leak Made Easy**, [英語版](https://ja.wikipedia.org/wiki/:en:CRIME "wikilink")）が報告された\[165\]\[166\]。ウェブサイトでのユーザ認証に使われているCookieの内容を回復されることで、[セッションハイジャック](https://ja.wikipedia.org/wiki/セッションハイジャック "wikilink")が可能となる。2012年9月にはMozilla FirefoxおよびGoogle ChromeにおいてCRIMEへの対応が実施された。また、マイクロソフトによればInternet ExplorerはCRIMEの影響を受けない。

CRIMEの報告者によって、CRIMEがTLS以外にもデータ圧縮を利用する[SPDY](https://ja.wikipedia.org/wiki/SPDY "wikilink")や[HTTPといったプロトコルにも広く適用可能であることが示されていたにもかかわらず](../Page/Hypertext_Transfer_Protocol.md "wikilink")、クライアント、サーバのいずれにおいてもTLSやSPDYに対する修正しか行われず、HTTPに対する修正は行われなかった。

#### BREACH攻撃

2013年に、HTTPでのデータ圧縮をターゲットとした**BREACH**（**Browser Reconnaissance and Exfiltration via Adaptive Compression of Hypertext**, [英語版](https://ja.wikipedia.org/wiki/:en:BREACH_\(security_exploit\) "wikilink")）と呼ばれるCRIME攻撃の変法が報告された。BREACH攻撃では、ログイントークン、メールアドレスなどの個人情報をわずか30秒で取得可能であり、不正なリンクを訪れさせたり、正当なウェブページに不正なコンテンツを挿入することも可能であった\[167\]。使用するアルゴリズム、Cipher Suiteを問わず、すべてのバージョンのTLS/SSLに対してBREACH攻撃は適用可能である\[168\]。TLSでのデータ圧縮やSPDYでのヘッダ圧縮を無効とすることで容易に回避可能であったCRIMEとは異なり、BREACHを回避するためにはHTTPでのデータ圧縮を無効にする必要があるが、通信速度の向上のためにほぼすべてのサーバがHTTPデータ圧縮を有効としている現状では、これを無効化することは現実的ではない\[169\]。

### その他

#### 再ネゴシエーション脆弱性

2009年11月4日、SSL 3.0以降の再ネゴシエーション機能を利用して、クライアントからのリクエストの先頭に[中間者が任意のデータを挿入できるという脆弱性が報告された](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")\[170\]\[171\]。プロトコル自体の脆弱性であり、すべての実装が影響を受ける。

この脆弱性への簡単な対策は、サーバにおいて再ネゴシエーションを禁止することである。根本対応としては、TLS Extensionを使った安全な再ネゴシエーション手順がRFC 5746として提案されている。この脆弱性を利用した中間者攻撃では、サーバがRFC 5746に対応しない限りクライアントは再ネゴシエーションが発生したことを検出できないので、クライアント側のみで対応することは不可能である。

#### 切り詰め攻撃

TLSでの切り詰め攻撃では、ユーザがウェブサービスからログアウトすることを妨害し、意図せずログインしたままとすることが可能である。ユーザからログアウト要求が送信されたときに、攻撃者が偽の[TCP](../Page/Transmission_Control_Protocol.md "wikilink") FINメッセージ（これ以上データを送信しない）を平文で挿入する。このメッセージを受けたサーバでは、ユーザから送られたログアウト要求を受け取らないため、ユーザの意図とは異なりログイン状態が維持される\[172\]。

2013年の報告\[173\]では、この攻撃への対応として、[Gmail](../Page/Gmail.md "wikilink")や[Hotmail](../Page/Hotmail.md "wikilink")などのウェブサービスでは、ログアウトが正常に完了した旨のページを表示するようになった。これにより、ログアウトしたか否かをユーザが確認することが可能となり、攻撃者によってログイン状態のアカウントを悪用される危険性が軽減される。

この攻撃では目標のコンピュータにマルウェアなどを導入する必要はないが、攻撃者が目標とサーバの間の回線に割り込むことが可能であること\[174\]と、目標のコンピュータに物理的にアクセス可能であることが求められる。

### 実装上の脆弱性をついたもの

#### ハートブリード

ハートブリード（）は、2014年に発覚した[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")ライブラリのバージョン1.0.1から1.0.1fの間で発見された深刻なセキュリティ脆弱性である。この脆弱性を利用することで、TLS/SSLによって保護されているはずの情報を盗むことが可能である。

このバグでは、インターネット上の誰もが、脆弱性のあるOpenSSLを利用しているシステムのメモリにアクセスすることが可能となり、サービスプロバイダの認証やデータの暗号化に用いられている秘密鍵、ユーザのアカウントおよびパスワード、実際にやり取りされたデータなどを取得できる。これにより、メッセンジャーサービス、電子メールの盗聴、データの盗難、なりすましなどが可能となる。

### ウェブサイトの統計

Trustworthy Internet Movementは、TLS/SSLに対する攻撃に対して脆弱なウェブサイトの統計を発表している。2019年8月における統計は以下の通りである\[175\]。

<table>
<caption><strong>TLS/SSLに対する攻撃に脆弱なウェブサイトの統計（括弧内は前月との差）</strong></caption>
<thead>
<tr class="header">
<th><p>攻撃</p></th>
<th><p>セキュリティ</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>安全ではない</p></td>
<td><p>状況による</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/#再ネゴシエーション脆弱性" title="wikilink">再ネゴシエーション脆弱性</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/#RC4攻撃" title="wikilink">RC4攻撃</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/#CRIME攻撃" title="wikilink">CRIME攻撃</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/#ハートブリード" title="wikilink">ハートブリード</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/OpenSSL#CCS_Injection_Vulnerability" title="wikilink">CCS Injection Vulnerability</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/#POODLE" title="wikilink">TLSへのPOODLE攻撃</a><br />
<small>SSL 3.0へのPOODLE攻撃は含まない</small></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/#ダウングレード攻撃" title="wikilink">プロトコルダウングレード</a></p></td>
<td></td>
</tr>
</tbody>
</table>

## 参考文献

  -
## 脚注

## 関連項目

  - [HTTPS](../Page/HTTPS.md "wikilink")
  - [Datagram Transport Layer Security](https://ja.wikipedia.org/wiki/Datagram_Transport_Layer_Security "wikilink")
  - [FTPS](../Page/FTPS.md "wikilink")
  - [SSH](../Page/Secure_Shell.md "wikilink")
  - [GnuTLS](https://ja.wikipedia.org/wiki/GnuTLS "wikilink")
  - [Network Security Services](https://ja.wikipedia.org/wiki/Network_Security_Services "wikilink")
  - [OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")
  - [フィッシング](../Page/フィッシング_\(詐欺\).md "wikilink")
  - [Extended Validation 証明書](../Page/Extended_Validation_証明書.md "wikilink") (EV SSL)
  - [認証局](../Page/認証局.md "wikilink")
  - [SSLオフロード](https://ja.wikipedia.org/wiki/SSLオフロード "wikilink")

## 外部リンク

### 標準化

  - 2018年9月時点での最新版
      - RFC 8446: "The Transport Layer Security (TLS) Protocol Version 1.3".
  - 過去の版
      - RFC 2246: "The TLS Protocol Version 1.0".
      - RFC 4346: "The Transport Layer Security (TLS) Protocol Version 1.1".
      - RFC 5246: "The Transport Layer Security (TLS) Protocol Version 1.2".
  - SSLは標準化されていない
      - This Internet Draft defines the now completely broken SSL 2.0.

      - RFC 6101: "The Secure Sockets Layer (SSL) Protocol Version 3.0".
  - TLS 1.0の拡張
      - RFC 2595: "Using TLS with IMAP, POP3 and ACAP". Specifies an extension to the IMAP, POP3 and ACAP services that allow the server and client to use transport-layer security to provide private, authenticated communication over the Internet.
      - RFC 2712: "Addition of [Kerberos](../Page/ケルベロス認証.md "wikilink") Cipher Suites to Transport Layer Security (TLS)". The 40-bit cipher suites defined in this memo appear only for the purpose of documenting the fact that those cipher suite codes have already been assigned.
      - RFC 2817: "Upgrading to TLS Within HTTP/1.1", explains how to use the [Upgrade mechanism in HTTP/1.1](https://ja.wikipedia.org/wiki/HTTP/1.1_Upgrade_header "wikilink") to initiate Transport Layer Security (TLS) over an existing TCP connection. This allows unsecured and secured HTTP traffic to share the same *well known* port (in this case, http: at 80 rather than https: at 443).
      - RFC 2818: "HTTP Over TLS", distinguishes secured traffic from insecure traffic by the use of a different 'server port'.
      - RFC 3207: "SMTP Service Extension for Secure SMTP over Transport Layer Security". Specifies an extension to the SMTP service that allows an SMTP server and client to use transport-layer security to provide private, authenticated communication over the Internet.
      - RFC 3268: "AES Ciphersuites for TLS". Adds [Advanced Encryption Standard](../Page/Advanced_Encryption_Standard.md "wikilink") (AES) cipher suites to the previously existing symmetric ciphers.
      - RFC 3546: "Transport Layer Security (TLS) Extensions", adds a mechanism for negotiating protocol extensions during session initialisation and defines some extensions. Made obsolete by RFC 4366.
      - RFC 3749: "Transport Layer Security Protocol Compression Methods", specifies the framework for compression methods and the [DEFLATE](../Page/Deflate.md "wikilink") compression method.
      - RFC 3943: "Transport Layer Security (TLS) Protocol Compression Using Lempel-Ziv-Stac (LZS)".
      - RFC 4132: "Addition of [Camellia](../Page/Camellia.md "wikilink") Cipher Suites to Transport Layer Security (TLS)".
      - RFC 4162: "Addition of [SEED](../Page/SEED_\(暗号\).md "wikilink") Cipher Suites to Transport Layer Security (TLS)".
      - RFC 4217: "Securing [FTP with TLS](../Page/FTPS.md "wikilink")".
      - RFC 4279: "Pre-Shared Key Ciphersuites for Transport Layer Security (TLS)", adds three sets of new cipher suites for the TLS protocol to support authentication based on pre-shared keys.
  - TLS 1.1の拡張
      - RFC 4347: "[Datagram Transport Layer Security](https://ja.wikipedia.org/wiki/Datagram_Transport_Layer_Security "wikilink")" specifies a TLS variant that works over datagram protocols (such as UDP).
      - RFC 4366: "Transport Layer Security (TLS) Extensions" describes both a set of specific extensions and a generic extension mechanism.
      - RFC 4492: "[Elliptic Curve Cryptography](../Page/楕円曲線暗号.md "wikilink") (ECC) Cipher Suites for Transport Layer Security (TLS)".
      - RFC 4680: "TLS Handshake Message for Supplemental Data".
      - RFC 4681: "TLS User Mapping Extension".
      - RFC 4785: "Pre-Shared Key (PSK) Ciphersuites with NULL Encryption for Transport Layer Security (TLS)".
      - RFC 5054: "Using the [Secure Remote Password](https://ja.wikipedia.org/wiki/Secure_remote_password_protocol "wikilink") (SRP) Protocol for TLS Authentication". Defines the [TLS-SRP](https://ja.wikipedia.org/wiki/TLS-SRP "wikilink") ciphersuites.
      - RFC 5077: "Transport Layer Security (TLS) Session Resumption without Server-Side State".
      - RFC 5081: "Using [OpenPGP](https://ja.wikipedia.org/wiki/OpenPGP "wikilink") Keys for Transport Layer Security (TLS) Authentication", obsoleted by RFC 6091.
  - TLS 1.2の拡張
      - RFC 5288: "AES [Galois Counter Mode](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink") (GCM) Cipher Suites for TLS".
      - RFC 5289: "TLS Elliptic Curve Cipher Suites with SHA-256/384 and AES Galois Counter Mode (GCM)".
      - RFC 5746: "Transport Layer Security (TLS) Renegotiation Indication Extension".
      - RFC 5878: "Transport Layer Security (TLS) Authorization Extensions".
      - RFC 5932: "Camellia Cipher Suites for TLS"
      - RFC 6066: "Transport Layer Security (TLS) Extensions: Extension Definitions", includes [Server Name Indication](https://ja.wikipedia.org/wiki/Server_Name_Indication "wikilink") and [OCSP](../Page/Online_Certificate_Status_Protocol.md "wikilink") stapling.
      - RFC 6091: "Using [OpenPGP](https://ja.wikipedia.org/wiki/OpenPGP "wikilink") Keys for Transport Layer Security (TLS) Authentication".
      - RFC 6176: "Prohibiting Secure Sockets Layer (SSL) Version 2.0".
      - RFC 6209: "Addition of the [ARIA](https://ja.wikipedia.org/wiki/ARIA_\(暗号\) "wikilink") Cipher Suites to Transport Layer Security (TLS)".
      - RFC 6347: "Datagram Transport Layer Security Version 1.2".
      - RFC 6367: "Addition of the Camellia Cipher Suites to Transport Layer Security (TLS)".
      - RFC 6460: "Suite B Profile for Transport Layer Security (TLS)".
      - RFC 6655: "AES-[CCM](https://ja.wikipedia.org/wiki/Counter_with_CBC-MAC "wikilink") Cipher Suites for Transport Layer Security (TLS)".
      - RFC 7027: "Elliptic Curve Cryptography (ECC) Brainpool Curves for Transport Layer Security (TLS)".
      - RFC 7251: "AES-CCM Elliptic Curve Cryptography (ECC) Cipher Suites for TLS".
      - RFC 7301: "Transport Layer Security (TLS) Application-Layer Protocol Negotiation Extension".
      - RFC 7366: "[Encrypt-then-MAC](https://ja.wikipedia.org/wiki/Encrypt-then-MAC "wikilink") for Transport Layer Security (TLS) and Datagram Transport Layer Security (DTLS)".
      - RFC 7465: "Prohibiting RC4 Cipher Suites".
      - RFC 7507: "TLS Fallback Signaling Cipher Suite Value (SCSV) for Preventing Protocol Downgrade Attacks".
      - RFC 7568: "Deprecating Secure Sockets Layer Version 3.0".
      - RFC 7627: "Transport Layer Security (TLS) Session Hash and Extended Master Secret Extension".
      - RFC 7685: "A Transport Layer Security (TLS) ClientHello Padding Extension".
      - RFC 7905: "ChaCha20-Poly1305 Cipher Suites for Transport Layer Security (TLS)".
      - RFC 7919: "Negotiated Finite Field Diffie-Hellman Ephemeral Parameters for Transport Layer Security (TLS)".
  - TLSを含むカプセル化
      - RFC 5216: "The [EAP](../Page/Extensible_Authentication_Protocol.md "wikilink")-TLS Authentication Protocol"
  - X.509 (PKIX)との関係性
      - RFC 6125: "Representation and Verification of Domain-Based Application Service Identity within Internet Public Key Infrastructure Using X.509 (PKIX) Certificates in the Context of Transport Layer Security (TLS)"
  - その他
      - RFC 7457: "Summarizing Known Attacks on Transport Layer Security (TLS) and Datagram TLS (DTLS)"
      - RFC 7525: "Recommendations for Secure Use of Transport Layer Security (TLS) and Datagram Transport Layer Security (DTLS)"

### IANA

  - [Transport Layer Security (TLS) Parameters](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml)
  - [Transport Layer Security (TLS) Extensions](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml)

### 日本の認証局ベンダー

  - [クロストラスト株式会社](https://crosstrust.co.jp/)
  - [株式会社コモドジャパン](https://comodo.jp/)
  - [サイバートラスト株式会社](https://www.cybertrust.ne.jp/)
  - [GMOグローバルサイン株式会社](https://jp.globalsign.com/)
  - [セコムトラストシステムズ株式会社](https://www.secomtrust.net/)
  - [デジサート・ジャパン合同会社](https://www.digicert.co.jp/)
  - [ジオトラスト](https://www.geotrust.co.jp/) - デジサート・ジャパン

[Category:Transport_Layer_Security](https://ja.wikipedia.org/wiki/Category:Transport_Layer_Security "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:セキュア通信](https://ja.wikipedia.org/wiki/Category:セキュア通信 "wikilink") [Category:電子商取引](https://ja.wikipedia.org/wiki/Category:電子商取引 "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  プロトコル名を含めた歴史については、Eric Rescorla著,「マスタリングTCP/IP SSL/TLS編」,オーム社開発局（2003年）ISBN 4-274-06542-1 の2章6節が詳しい。
2.  ただし、メールサーバーへの接続においてはTLS接続用のTCPポートにはじめからTLSで接続するSMTP over SSLと、通常のTCPポートにSMTP接続後にSTARTTLSコマンドによってセキュアな接続に切り替えるSTARTTLSという異なる接続方式があり、名称を使い分けることがある。詳しくは[\#アプリケーション層プロトコルへの適用](https://ja.wikipedia.org/wiki/#アプリケーション層プロトコルへの適用 "wikilink")の項目を参照されたい。
3.
4.
5.
6.
7.
8.
9.
10.
11. [RFC5246日本語訳「 TLS ハンドシェイク関連プロトコル」](https://www.ipa.go.jp/security/rfc/RFC5246-07JA.html)、IPA。2016年8月11日閲覧
12.
13.
14.
15.
16.
17.
18.
19.
20.
21. [RFC5246日本語訳「 8. 暗号技術的計算」](https://www.ipa.go.jp/security/rfc/RFC5246-08JA.html)、IPA。2016年8月11日閲覧
22.
23.
24. [RFC5246日本語訳「6. TLS レコードプロトコル」](https://www.ipa.go.jp/security/rfc/RFC5246-06JA.html)、IPA。2016年8月11日閲覧
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35. RFC 3268によって後付けでAESが追加されたTLS 1.0とは異なり、TLS 1.1を定義する RFC 4346 A.5節ではRFC 3268が参照され、AESが当初から追加されている
36. \[//tools.ietf.org/html/draft-ietf-tls-tls13-18 draft-ietf-tls-tls13-18 "[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink") The Transport Layer Security (TLS) Protocol Version 1.3"\]
37.
38.
39.
40.
41. \[//tools.ietf.org/html/draft-chudov-cryptopro-cptls-04 draft-chudov-cryptopro-cptls-04 - GOST 28147-89 Cipher Suites for Transport Layer Security (TLS)\]
42. RFC 5288, RFC 5289
43. GCM、CCMなどのAEAD（認証付き暗号モード）は、TLS 1.2以降のみで利用可能
44. RFC 6655, RFC 7251
45.
46.
47. RFC 6367
48.
49. RFC 5932およびRFC 6367
50.
51. RFC 6209
52.
53.
54.
55. RFC 4162
56.
57. CBCモードは、サイドチャネル攻撃への対処が不十分な実装では[Lucky Thirteen攻撃に対して脆弱である](https://ja.wikipedia.org/wiki/#パディング攻撃 "wikilink")
58.
59.
60. IDEA、DESはTLS 1.2で廃止された
61.
62.
63. 40ビットのセキュリティ強度を持つCipher Suiteは、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")による[高強度暗号アルゴリズムの輸出規制を回避するために設計された](https://ja.wikipedia.org/wiki/アメリカ合衆国からの暗号の輸出規制 "wikilink")。これらはTLS 1.1以降では利用が禁止されている。
64.
65.
66. RFC 7905
67.
68. RFC 7465 により、すべてのバージョンのTLSにおいてRC4の利用は禁止された（[RC4攻撃](https://ja.wikipedia.org/wiki/#RC4攻撃 "wikilink")）
69.
70. 認証のみで暗号化は行われない。
71.
72.
73.
74.
75. 2019年8月3日現在
76.
77.
78.
79.
80. 後方互換性の確保のため、SSL 2.0に非対応あるいは既定で無効の場合にもSSL 2.0 client helloはサポートされる。
81.
82.
83.
84.
85.
86.
87.
88.
89.
90.
91.
92.
93.
94.
95.
96.
97.
98. [TLS cipher suites in Microsoft Windows XP and 2003](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380512%28v=vs.85%29.aspx)
99. [SChannel Cipher Suites in Microsoft Windows Vista](http://msdn.microsoft.com/en-us/library/windows/desktop/ff468651%28v=vs.85%29.aspx)
100. [TLS Cipher Suites in SChannel for Windows 7, 2008R2, 8, 2012](http://msdn.microsoft.com/en-us/library/windows/desktop/aa374757%28v=vs.85%29.aspx)
101.
102.
103.
104.
105.
106.
107.
108.
109. [Freestart collision for full SHA-1](https://eprint.iacr.org/2015/967) *Marc Stevens and Pierre Karpman and Thomas Peyrin EUROCRYPT 2016*
110.
111.
112.
113. \[//tools.ietf.org/html/draft-popov-tls-prohibiting-rc4-02 draft-popov-tls-prohibiting-rc4-02\]
114. [security – Safest ciphers to use with the BEAST? (TLS 1.0 exploit) I've read that RC4 is immune – Server Fault](http://serverfault.com/questions/315042/)
115.
116.
117.
118.
119.
120.
121.
122.
123.
124. 前掲「マスタリングTCP/IP SSL/TLS編」、p. 191。
125. [暗号化通信に脆弱性「FREAK」が判明 - 盗聴や改ざんのおそれ](http://www.security-next.com/056462) Security NEXT、2015年3月5日閲覧。
126. [Only allow ephemeral RSA keys in export ciphersuites.](https://github.com/openssl/openssl/commit/ce325c60c74b0fa784f5872404b722e120e5cab0) OpenSSLのGithubツリー、2014年10月24日（2015年3月5日閲覧）
127.
128.
129.
130.
131.
132.
133.
134.
135.
136.
137.
138.
139.
140.
141.
142.
143.
144.
145. RFC 7507
146.
147.
148.
149.
150.
151.
152.
153.
154.
155. <http://support.apple.com/kb/HT6531>
156. <http://support.apple.com/kb/HT6541>
157.
158.
159.
160.
161.
162.
163.
164.
165.
166.
167.
168.
169.
170.
171.
172.
173.
174.
175.