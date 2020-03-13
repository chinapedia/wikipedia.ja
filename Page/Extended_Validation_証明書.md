> この記事は[Extended Validation ](https://ja.wikipedia.org/wiki/Extended_Validation_)から翻訳されています。


**Extended Validation 証明書** \[1\] (**EV 証明書**とも) とは、発行者による主体者の審査に一定の基準を設けた[公開鍵証明書](../Page/公開鍵証明書.md "wikilink")である。[ウェブサイト](../Page/ウェブサイト.md "wikilink")の[認証](../Page/認証.md "wikilink")と[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")処理に使われる[SSL/TLS](../Page/Transport_Layer_Security.md "wikilink") (以下、単にSSL) サーバー用の[公開鍵証明書](../Page/公開鍵証明書.md "wikilink") (この場合、単に**EV SSL証明書**とも) のほか、電子メールやコード・サイニング用の公開鍵証明書がある。本記事では以下、SSL用の証明書を中心に記述している。

## 概要

[SSLの元来の考え方は](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")、SSL証明書の取得時にウェブサイトの管理者が[認証局](../Page/認証局.md "wikilink") (CA) の審査を経なければならなくすることで、デジタル証明書による[オンライントランザクションに信頼を与えることであった](../Page/オンライントランザクション処理.md "wikilink")。

しかし、ほとんどの[Webブラウザの](../Page/ウェブブラウザ.md "wikilink")[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")においては、安直な確認をした証明書と厳格な審査をした証明書とが区別されてこなかったため、混乱が生じることとなった。多くのWebブラウザではSSLで接続出来た場合に[南京錠](../Page/南京錠.md "wikilink")のアイコンが表示されるだけで、そのウェブサイトの持ち主がきちんと審査されたのかどうかは明確には判らなかった。その結果、[フィッシングサイトなど](../Page/フィッシング_\(詐欺\).md "wikilink")、悪意ある者たちによって自分のウェブサイトが信頼出来るものであるかのように見せかけるためにSSLが使われ始めるようになった。

EV SSL証明書は、次の点において利用者の信頼を回復することを目的としている。

1.  認証
2.  同定
3.  暗号

EVの指針を策定したのは、先行した認証局、インターネットソフトウェアやその他アプリケーションのベンダー、法律や[監査](../Page/監査.md "wikilink")の専門家らによって自発的組織として結成された [CA/Browser Forum](http://cabforum.org/) である。

独立した監査によりWebTrust指針（もしくはそれと同等）の認定の一部を満たしたCAだけがEV SSL証明書の発行を許される。EV証明書は以下のような詳細な発行要件に従って発行される。

  - ウェブサイト所有者が運用上および物理的に実在しているだけでなく、法的実在性も確立されていること
  - ウェブサイト所有者により、該当[URLに対する排他的な制御が確立されていること](../Page/Uniform_Resource_Locator.md "wikilink")
  - ウェブサイト所有者のための作業者の同定と責任、および、責任ある役員によって署名された法的義務を伴う文書の確認

利用者にとっての利点は、最新のWebブラウザを使った場合に、従来のSSL証明書より多くの情報をEV SSL証明書から取得して確認できることである。[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Internet Explorerは](../Page/Internet_Explorer.md "wikilink")、バージョン7で初のEV対応Webブラウザとなった。その後、主要なWebブラウザはEVに対応している。Internet Explorer 7ではEV証明書が検出されると、

  - [アドレスバー](https://ja.wikipedia.org/wiki/アドレスバー "wikilink")が緑色になる。
  - ウェブサイト所有者の名称や所在地の要約と、証明書を発行したCA名が交互に表示される専用のラベルが現れる。

なお、EV未対応のWebブラウザでは通常のSSLサイトとして表示されるため、互換性は保たれる。

Extended Validation (EV) の指針では、参加するCAに対するEV識別子の割当が要求されている。この識別子は、[独立した監査](http://cabforum.org/WebTrustAuditGuidlines.pdf)の完了とその他の条件の成立後に、EVをサポートするWebブラウザのベンダーに登録される。

なおEV SSLにおいては、URLの正当性をCAが担保する目的から、通常のSSLで使われるような[ワイルドカード証明書の発行は認められず](../Page/ワイルドカード_\(情報処理\).md "wikilink")、仮にそのような証明書を無理に発行したとしても、Webブラウザ側で受け入れを拒否される\[2\]。ただInternet Explorerにおいては、かつてワイルドカードを使用したEV SSL証明書を受け入れてしまう[脆弱性](../Page/脆弱性.md "wikilink")が存在した\[3\]。

上記のようにEV SSLはウェブサイト所有者の身元確認を強化したものだが、ウェブサイトの安全性を保障するものではない。所有者が悪意を持っているかもしれないし、ウェブサイトが第三者から乗っ取られる可能性も存在する。

## 対応ウェブブラウザ

主要ウェブブラウザにおけるEV SSLの対応状況は以下の通りである\[4\]。

  - [Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")：1.0以降
  - [Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")：3.0.0以降
  - [Internet Explorer](../Page/Internet_Explorer.md "wikilink")：7.0以降
  - [Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")：9.5以降
  - [Safari](../Page/Safari.md "wikilink")：3.2以降

### EV証明書表示位置の移動

セキュリティ研究者の調査により、アドレスバー上のEV証明書の緑色や組織名表示は、フィッシング等に対して利用者が安全な選択をするための意味のある保護対策とならないことが分かった\[5\]。そのためいくつかのブラウザはEV証明書表示をアドレスバーからページ情報へ移動している。

  - [Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink") : 77.0以降\[6\]
  - [Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink") : 70以降\[7\]

Edgeについてもマイクロソフトは、ウェブページが正当なものかを判断する際、EV証明書の緑色のバーの効果は限定的であるとしており\[8\]、バージョン44.17763時点でEV証明書であっても緑色で組織名が表示されるものとそうでないものがある。

## EV証明書の特定

EV証明書を特定する一貫した方法は存在しない。EV証明書であることを示すため、各証明書発行者ごとに別々な [オブジェクト識別子](https://ja.wikipedia.org/wiki/オブジェクト識別子 "wikilink") (OID) が証明書ポリシーの拡張フィールドにあり、それらは発行者の [CPS](https://ja.wikipedia.org/wiki/認証運用規程 "wikilink") (Certification Practice Statement) で文書化される。

<table>
<tbody>
<tr class="odd">
<td><p><strong>発行者</strong></p></td>
<td><p><strong><a href="https://ja.wikipedia.org/wiki/オブジェクト識別子" title="wikilink">OID</a></strong></p></td>
<td><p><strong>CPS</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/AffirmTrust" title="wikilink">AffirmTrust</a></p></td>
<td><p><code>1.3.6.1.4.1.34697.2.1</code><br />
<code>1.3.6.1.4.1.34697.2.2</code><br />
<code>1.3.6.1.4.1.34697.2.3</code><br />
<code>1.3.6.1.4.1.34697.2.4</code></p></td>
<td><p><a href="https://www.affirmtrust.com/wp-content/uploads/AffirmTrust-SSL-CPS-3.8.pdf">AffirmTrust CPS v1.1</a>, p. 4</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/A-Trust" title="wikilink">A-Trust</a></p></td>
<td><p><code>1.2.40.0.17.1.22</code></p></td>
<td><p><a href="https://www.a-trust.at/docs/CPS/a-sign-ssl-ev/a-sign-ssl-ev_cps.pdf">a.sign SSL EV CPS v1.3.4</a></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>2.16.578.1.26.1.3.3</code></p></td>
<td><p><a href="https://www.buypass.com/security/ca-documentation-legal/_/attachment/download/035994c1-4fb5-494f-ae9b-e06f6b24f34a:6301390b3c8d63a3c2477318e55026e4121b7b37/cpsVID_CL3_03.06.2019.pdf">Buypass Class 3 EV CPS</a>, p. 10</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Camerfirma" title="wikilink">Camerfirma</a></p></td>
<td><p><code>1.3.6.1.4.1.17326.10.14.2.1.2</code><br />
<code>1.3.6.1.4.1.17326.10.8.12.1.2</code></p></td>
<td><p><a href="http://docs.camerfirma.com/publico/DocumentosWeb/politicas/CPS_V_3_2_3.pdf">Camerfirma CPS v3.2.3</a></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>1.3.6.1.4.1.6449.1.2.1.5.1</code></p></td>
<td><p><a href="https://www.comodo.com/repository/EV_CPS_120806.pdf">Comodo EV CPS</a>, p. 28</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/DigiCert" title="wikilink">DigiCert</a></p></td>
<td><p><code>2.16.840.1.114412.2.1</code><br />
<code>2.16.840.1.114412.1.3.0.2</code></p></td>
<td><p><a href="https://www.digicert.com/DigiCert_EV-CPS.pdf">DigiCert EV CPS v. 1.0.3</a>, p. 56</p></td>
</tr>
<tr class="even">
<td><p>（現存せず[9]）</p></td>
<td><p><code>2.16.528.1.1001.1.1.1.12.6.1.1.1</code></p></td>
<td><p><a href="http://www.diginotar.com/Portals/0/General%20terms/DigiNotar_CPS_3.5_-_EN.pdf">DigiNotar CPS v 3.5</a>, p. 2</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/E-Tugra" title="wikilink">E-Tugra</a></p></td>
<td><p><code>2.16.792.3.0.4.1.1.4</code></p></td>
<td><p><a href="https://www.e-tugra.com.tr/en-us/CPS">E-Tugra Certification Practice Statement (CPS)</a>, p. 2</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Entrust" title="wikilink">Entrust</a></p></td>
<td><p><code>2.16.840.1.114028.10.1.2</code></p></td>
<td><p><a href="http://www.entrust.net/CPS/pdf/evssl_cps_english011107.pdf">Entrust EV CPS</a>, p. 37</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/ETSI" title="wikilink">ETSI</a></p></td>
<td><p><code>0.4.0.2042.1.4</code><br />
<code>0.4.0.2042.1.5</code></p></td>
<td><p><a href="https://www.etsi.org/deliver/etsi_ts/102000_102099/102042/02.04.01_60/ts_102042v020401p.pdf">ETSI TS 102 042 V2.4.1</a>, p. 18</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Firmaprofesional" title="wikilink">Firmaprofesional</a></p></td>
<td><p><code>1.3.6.1.4.1.13177.10.1.3.10</code></p></td>
<td><p><a href="https://www.firmaprofesional.com/images/pdfs/FP_CP_Gen_Servidor_Web_SSL_6.2-EN.pdf">SSL SECURE WEB SERVER CERTIFICATES</a>, p. 6</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/GeoTrust" title="wikilink">GeoTrust</a></p></td>
<td><p><code>1.3.6.1.4.1.14370.1.6</code></p></td>
<td><p>[//www.geotrust.com/resources/cps/pdfs/true_businessid_CPS_v2.6.pdf GeoTrust EV CPS v. 2.6], p. 28</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/GlobalSign" title="wikilink">GlobalSign</a></p></td>
<td><p><code>1.3.6.1.4.1.4146.1.1</code></p></td>
<td><p><a href="http://www.globalsign.com/repository/GlobalSign_CPS_v6.5.pdf">GlobalSign EV CPS v. 6.5</a>, p. 24</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/GoDaddy" title="wikilink">GoDaddy</a></p></td>
<td><p><code>2.16.840.1.114413.1.7.23.3</code></p></td>
<td><p><a href="https://certificates.godaddy.com/repository/StarfieldCP-CPS_V20.pdf">GoDaddy EV CPS v. 2.0</a>, p. 42</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>1.3.6.1.4.1.14777.6.1.1</code></p></td>
<td><p><a href="http://www.izenpe.com/s15-12020/en/contenidos/informacion/doc_especifica/en_def/adjuntos/PR_P_Documentaci%C3%B3n_Espec%C3%ADfica_SSL_Sede_EV_en.pdf">DOCUMENTACIÓN ESPECÍFICA PARA CERTIFICADOS DEL TIPO: SERVIDOR SEGURO SSL, SERVIDOR SEGURO EVV, SEDE ELECTRÓNICA Y SEDE ELECTRÓNICA EV</a>,</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Kamu_Sertifikasyon_Merkezi" title="wikilink">Kamu Sertifikasyon Merkezi</a></p></td>
<td><p><code>2.16.792.1.2.1.1.5.7.1.9</code></p></td>
<td><p><a href="http://www.kamusm.gov.tr/BilgiDeposu/KSM_CES_SUE/KamuSM_SSL_SMIME_SI-SUE.v2.pdf">TÜBİTAK BİLGEM Kamu Sertifikasyon Merkezi SSL Sİ/SUE</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Keynectis" title="wikilink">Keynectis</a></p></td>
<td><p><code>1.3.6.1.4.1.22234.2.5.2.3.1</code></p></td>
<td><p><a href="http://www.keynectis.com/static/content/common/pc-dpc/DSQ_NT_KEYNECTIS_EV_SSL_CA_CPS_20090504s.pdf">KEYNECTIS EV CA CPS v 0.3</a>, p. 10</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Network_Solutions" title="wikilink">Network Solutions</a></p></td>
<td><p><code>1.3.6.1.4.1.782.1.2.1.8.1</code></p></td>
<td><p><a href="http://www.networksolutions.com/legal/SSL-legal-repository-ev-cps.jsp">Network Solutions EV CPS v. 1.1</a>, 2.4.1</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>1.3.6.1.4.1.8024.0.2.100.1.2</code></p></td>
<td><p><a href="http://www.quovadisglobal.com/~/media/Files/Repository/QV_RCA2_CPCPS_V1_10.ashx">QuoVadis Root CA2 CP/CPS</a>, p. 34</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/セコムトラストシステムズ" title="wikilink">SECOM Trust Systems</a></p></td>
<td><p><code>1.2.392.200091.100.721.1</code></p></td>
<td><p><a href="https://repo1.secomtrust.net/spcpp/pfw/pfwevca/PfWEVCA-CPS.pdf">SECOM Trust Systems EV CPS</a> (in Japanese), p. 2</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>2.16.840.1.114414.1.7.23.3</code></p></td>
<td><p><a href="https://certificates.starfieldtech.com/repository/StarfieldCP-CPS_V20.pdf">Starfield EV CPS v. 2.0</a>, p. 42</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/StartCom_Certification_Authority.md" title="wikilink">StartCom Certification Authority</a></p></td>
<td><p><code>1.3.6.1.4.1.23223.2</code><br />
<code>1.3.6.1.4.1.23223.1.1.1</code></p></td>
<td><p><a href="https://www.startssl.com/?app=26">StartCom CPS</a>, no. 4</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>2.16.756.1.83.21.0</code></p></td>
<td><p><a href="http://www.swissdigicert.ch/sdcs/portal/open_pdf?file=deutsch%2F102_CPS_SDCS_EV_2_16_756_1_83_2_2_V2_1_de.pdf">Swisscom Root EV CA 2 CPS</a> (in German), p. 62</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><code>2.16.756.1.89.1.2.1.1</code></p></td>
<td><p><a href="http://repository.swisssign.com/SwissSign-Gold-CP-CPS-R4.pdf">SwissSign Gold CA-G2 CP/CPS</a>, p. 7</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><code>2.16.840.1.113733.1.7.48.1</code></p></td>
<td><p><a href="https://www.thawte.com/assets/documents/repository/cps/Thawte_CPS_3_3.pdf">Thawte EV CPS v. 3.3</a>, p. 95</p></td>
</tr>
<tr class="odd">
<td><p>*</p></td>
<td><p><code>2.16.840.1.114404.1.1.2.4.1</code></p></td>
<td><p><a href="https://www.securetrust.com/legal/SecureTrust_EV_CPS_1_1_1.pdf">SecureTrust EV CPS v1.1.1</a>, p. 5</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/VeriSign" title="wikilink">VeriSign</a></p></td>
<td><p><code>2.16.840.1.113733.1.7.23.6</code></p></td>
<td><p><a href="http://www.verisign.com/repository/CPS/VeriSignCPSv3.3.pdf">VeriSign EV CPS v. 3.3</a>, p. 87</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Verizon_Business" title="wikilink">Verizon Business</a>（旧<a href="https://ja.wikipedia.org/wiki/Cybertrust" title="wikilink">Cybertrust</a>）</p></td>
<td><p><code>1.3.6.1.4.1.6334.1.100.1</code></p></td>
<td><p><a href="http://cybertrust.omniroot.com/repository/Cybertrust_CPS_v_5_2.pdf">Cybertrust CPS v.5.2</a>, p. 20</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Wells_Fargo" title="wikilink">Wells Fargo</a></p></td>
<td><p><code>2.16.840.1.114171.500.9</code></p></td>
<td><p><a href="http://www.wellsfargo.com/cps">WellsSecure PKI CPS v. 12.1.2</a>, p. 14</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/WoSign" title="wikilink">WoSign</a></p></td>
<td><p><code>1.3.6.1.4.1.36305.2</code></p></td>
<td><p><a href="http://www.wosign.com/policy/wosign-policy-1-2-4.pdf">WoSign CPS V1.2.4</a>, p. 21</p></td>
</tr>
</tbody>
</table>

*\** 旧XRamp Security Services, Inc.

## 脚注

<references/>

## 関連項目

  - [Transport Layer Security](../Page/Transport_Layer_Security.md "wikilink")
  - [公開鍵証明書](../Page/公開鍵証明書.md "wikilink")
  - [ルート証明書](../Page/ルート証明書.md "wikilink")
  - [弁護士意見書](https://ja.wikipedia.org/wiki/弁護士意見書 "wikilink")

## 外部リンク

  - [CA/Browser Forum のウェブ・サイト (英語)](https://cabforum.org/)
  - [CA/Browser Extended Validation 指針1.5.0版 (英語)](https://cabforum.org/wp-content/uploads/EV-SSL-Certificate-Guidelines-Version-1.5.0.pdf)
  - [処理ソフトウェアの指針2.0版 (英語)](https://cabforum.org/wp-content/uploads/Recommendations-for-the-Processing-of-EV-SSL-Certificates.v.2.0.pdf)
  - [米弁護士協会 デジタル証明書ワーキング・グループ (英語)](http://mail.abanet.org/scripts/wa.exe?A0=st-cert&D=0&F=&H=0&O=T&S=&T=0)
  - [Entrust EV SSL証明書の情報 (英語)](http://www.entrust.net/ssl-certificates/extended-validation.htm)
  - [DigiCert EV SSL証明書の情報 (英語)](https://www.digicert.com/ev-ssl-certification.htm)
  - [Symantec（旧VeriSign）のExtended Validation SSL FAQ (英語)](https://www.symantec.com/theme.jsp?themeid=how-ssl-works&tabID=2&inid=vrsn_symc_ssl_FAQ)
  - [セコムトラストシステムズのEV SSL証明書の情報(日本語)](https://www.secomtrust.net/service/pfw/pfw_service/ev.html)
  - [グローバルサインのEV SSL証明書の情報(日本語)](https://jp.globalsign.com/service/ssl/ev.html)
  - [Netcraftの記事 (英語)](http://news.netcraft.com/archives/2008/02/17/extended_validation_ssl_certificates_now_1_year_old.html)

[Category:公開鍵基盤](https://ja.wikipedia.org/wiki/Category:公開鍵基盤 "wikilink") [Category:認証技術](https://ja.wikipedia.org/wiki/Category:認証技術 "wikilink") [Category:Transport_Layer_Security](https://ja.wikipedia.org/wiki/Category:Transport_Layer_Security "wikilink") [Category:電子商取引](https://ja.wikipedia.org/wiki/Category:電子商取引 "wikilink") [Category:ウェブブラウザ](https://ja.wikipedia.org/wiki/Category:ウェブブラウザ "wikilink")

1.  この **validation** という用語は、証明書関連でしばしば登場する [Certification path validation algorithm](https://ja.wikipedia.org/wiki/:en:Certification_path_validation_algorithm "wikilink") と紛らわしいが異なるものであるので注意。
2.  [Why can’t I get a Wildcard Extended Validation (EV) SSL Certificate?](http://www.networksolutions.com/support/why-can-t-i-get-a-wildcard-extended-validation-ev-ssl-certificate/) - Network Solutions
3.  [CVE-2014-2783](http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2014-2783) - National Vulnerability Database
4.
5.
6.
7.
8.
9.