> この記事は[Mozilla Public License](https://ja.wikipedia.org/wiki/Mozilla_Public_License)から翻訳されています。


**Mozilla Public License** (**MPL**) は、[Mozilla Foundationによって作成された](../Page/Mozilla_Foundation.md "wikilink")[フリーソフトウェアライセンス](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス "wikilink")、オープンソースライセンスである。

## 概要

MPLは[修正BSDライセンスと](../Page/BSDライセンス.md "wikilink")[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) のハイブリッドと言えるライセンスで、[プロプライエタリとオープンソースの間のバランスを模索したものとなっている](../Page/プロプライエタリ・ソフトウェア.md "wikilink")\[1\]

初期の1.0から1.1、2.0と2度の改訂を経ており\[2\]、2012年1月に発表された2.0では、ライセンス文の簡素化、他ライセンスとの相互運用性の向上、特許保護を盛り込むことによるコード貢献者の権利侵害からの保護などが行われている\[3\]。

MPL 2.0は[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")、[Mozilla Thunderbirdをはじめとする](../Page/Mozilla_Thunderbird.md "wikilink")[Mozilla](../Page/Mozilla.md "wikilink")ソフトウェアで利用されている\[4\]。また、[Adobe Flexや](https://ja.wikipedia.org/wiki/Adobe_Flex "wikilink")[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink") 4.0以降（[LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink") 3以降との[デュアルライセンス](../Page/デュアルライセンス.md "wikilink")）にも利用されている\[5\]\[6\]\[7\]。以前のバージョンであるMPL 1.1は、[Common Development and Distribution Licenseのようなソフトウェア企業による派生ライセンスに広く用いられている](../Page/Common_Development_and_Distribution_License.md "wikilink")\[8\]。

## 利用条件

MPLは、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink") (FSF) による「[フリーソフトウェアライセンス](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス "wikilink")」\[9\]、[Open Source Initiative](../Page/Open_Source_Initiative.md "wikilink") (OSI) による「オープンソースライセンス」\[10\]の両方の承認を受けている。MPLでライセンスされた[ソースコード](../Page/ソースコード.md "wikilink")は、他のライセンスで保護されたファイルやプロプライエタリなファイルと組み合わせることが可能であるが、MPLで保護されたコードは永続的にMPLでライセンスされ続け、ソースコードの状態で利用可能であることが求められる\[11\]。これは、[MIT Licenseや](../Page/MIT_License.md "wikilink")[BSDライセンス](../Page/BSDライセンス.md "wikilink")において派生物をプロプライエタリにすることが可能なことや、GPLが派生物すべてをGPLでライセンスすることを求めていることと比較した時のMPLの大きな違いである。プロプライエタリなモジュールはプロプライエタリなままで、それ以外のコアモジュールはオープンソースを維持できることから、MPLはソフトウェア企業、オープンソースコミュニティ双方での利用が容易となっている\[12\]。

特許を含まない場合、MPLでライセンスされたコードの利用、改変、再頒布を自由に行うことができる。特許で保護されたコードの場合には、利用、譲渡、販売は可能であるが改変は特別な許可がない限り認められない。また、MPLでは被許諾者に対して貢献者の[商標](../Page/商標.md "wikilink")に関する権利は何ら付与されない\[13\]。

MPLの利用条件を順守するために、被許諾者には主に再頒布に関する責任が要求される。被許諾者は、MPLで保護されるソースコードすべてに対するアクセスあるいは提供手段を確保する必要がある。これは、成果物が実行ファイルであったりプロプライエタリなコードと組み合わせたものである場合も同様である。例外は、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL)、[GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink") (LGPL) あるいは [Affero GPL](https://ja.wikipedia.org/wiki/GNU_Affero_General_Public_License "wikilink") (AGPL) でライセンスされたコードと組み合わせた場合であり、この場合にはMPLの代わりにより厳格なGPLベースのライセンスを選択することが可能である\[14\]。

## 歴史

### MPL 1.0

[ネットスケープコミュニケーションズ](../Page/ネットスケープコミュニケーションズ.md "wikilink")では、自社製品である[Netscapeシリーズ](../Page/Netscapeシリーズ.md "wikilink")のソースコードを保護するために[Netscape Public License](https://ja.wikipedia.org/wiki/Netscape_Public_License "wikilink") (NPL) と呼ばれるライセンスを利用していた。NPLには、他者から提供されたコードであってもネットスケープの一存でプロプライエタリに変更できるという条項が含まれており、これはオープンソースコミュニティからの批判を受けることとなった。ネットスケープの弁護士であったは、NPLに代わるコピーレフトの理念に基づいた新たなライセンスを用意した。これがMPL 1.0であり、1998年に発表された。NPLでライセンスされていたNetscapeのソースコードはすべてMPLで再ライセンスされた。これにより、Netscapeシリーズをオープンソースで開発することで、競合相手である[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Internet Explorerとの競争を有利に進めることをネットスケープは狙っていた](../Page/Internet_Explorer.md "wikilink")\[15\]。

### MPL 1.1

MPL 1.0の発表から1年もしないうちに、貢献者からのコメントを受け付けた公開プロセスを経てベーカーと[Mozilla OrganizationはMPL](https://ja.wikipedia.org/wiki/Mozilla_Organization "wikilink") 1.0にいくつかの修正を加えたMPL 1.1を発表した\[16\]。この改訂では、特許の扱いに関する条件を明確にし、[マルチライセンスを許容するものであった](../Page/デュアルライセンス.md "wikilink")。これにより、GPLやLGPLなどより厳格なライセンスを好む開発者からの貢献が期待できることとなった\[17\]。

当初はNPLでライセンスされたコードを再ライセンスすることを意図していたMPLであるが、オープンソースコミュニティで広く用いられるようになり、MPL 1.1はFSFによるフリーソフトウェアライセンスおよびOSIによるオープンソースライセンスの承認を受けた\[18\]\[19\]。

MPL 1.1はソフトウェア企業などが独自のライセンスを作成する際の雛形とされることが多く、また、その構造、法的な精密さ、明確な利用条件などは、のちのGPL 3などにも強い影響を与えた\[20\]。

### MPL 2.0

MPL 1.1発表から10年以上が経過した2010年、MPL 2.0のための公開プロセスが開始された\[21\]。21か月に及ぶ作業により、MPLは簡素化され理解しやすくなり、GPLや[Apache Licenseとの互換性が向上し](../Page/Apache_License.md "wikilink")、特許保護を盛り込むことによるコード貢献者の権利侵害からの保護が加えられた\[22\]。

MPL 1.1に引き続き、MPL 2.0はFSFおよびOSIの承認を受けている\[23\]\[24\]。

## 他のライセンスとの互換性

強いコピーレフトライセンスとは違い、MPLでライセンスされたコードはそれ自体がMPLで保護されている限りは他のライセンス下のファイルと組み合わせることが可能である (MPL Section 3.3)\[25\]。MPLでは、ソースコードのファイルごとにMPL下のコードと他ライセンス下のコードを分けて扱っており、ソースコード全体をMPLでライセンスする必要はない\[26\]。

MPL 1.1では、GPLと互換性を保つことができない制限が存在した（これがMPL 2.0改訂の動機の一つである）。MPL 1.1には二次ライセンスに関する規定が存在していたが (MPL 1.1 Section 13)、MPL 1.1下のコードとGPL下のコードを法的にリンクすることはできず、これがFSFがMPL 1.1の使用を推奨しない理由となっていた\[27\]。これらの理由により、FirefoxをはじめとするMozillaソフトウェアは、MPL 1.1単独ではなくMPL 1.1/GPL 2.0/LGPL 2.1のトリプルライセンスで提供されていた\[28\]。

MPL 2.0は、[Apache Licenseおよび特別な留保がない限り](../Page/Apache_License.md "wikilink")「[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) 2.0、[GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink") (LPGL) 2.1、[Affero GPL](https://ja.wikipedia.org/wiki/GNU_Affero_General_Public_License "wikilink") (AGPL) 3.0およびそれ以降」と互換性がある\[29\]。MPL 1.1時代にトリプルライセンスで提供されていたMozillaソフトウェアはMPL 2.0単独でのライセンスに順次切り替えられているが、[Mozilla Application Suiteなど古いMozillaソフトウェアは現在でもトリプルライセンスで提供されている](../Page/Mozilla_Application_Suite.md "wikilink")。

## MPLを基としたライセンス

  - [AROS](https://ja.wikipedia.org/wiki/AROS "wikilink") Public License
  - [Celtx](https://ja.wikipedia.org/wiki/Celtx "wikilink") Public License\[30\]
  - [Common Development and Distribution License](../Page/Common_Development_and_Distribution_License.md "wikilink")
  - [Common Public Attribution License](https://ja.wikipedia.org/wiki/Common_Public_Attribution_License "wikilink")
  - [Erlang](https://ja.wikipedia.org/wiki/Erlang_\(programming_language\) "wikilink") Public License (based on MPL v1.0)\[31\]
  - [Firebird](https://ja.wikipedia.org/wiki/Firebird_\(database_server\) "wikilink") Initial Developer's Public License (based on MPL v1.1)\[32\]
  - [gSOAP Public License](https://ja.wikipedia.org/wiki/gSOAP_Public_License "wikilink")\[33\]
  - [OpenMRS](https://ja.wikipedia.org/wiki/OpenMRS "wikilink") Public License
  - [OpenELIS](https://ja.wikipedia.org/wiki/OpenELIS "wikilink") Public License
  - [SugarCRM](../Page/SugarCRM.md "wikilink") Public License
  - [Sun Public License](https://ja.wikipedia.org/wiki/Sun_Public_License "wikilink")
  - [Yahoo\!](../Page/Yahoo!.md "wikilink") Public License

## 脚注

## 外部リンク

  -   - [Mozilla Public License Version 2.0](https://www.mozilla.org/MPL/2.0/)
      - [Mozilla Public License Version 1.1](https://www.mozilla.org/MPL/1.1/)
      - [Mozilla Public License Version 1.0](https://www.mozilla.org/MPL/1.0/)

  - [Mozilla Public License, version 1.1](http://www.mozilla-japan.org/MPL/MPL-1.1J.html) - Mozilla Japanによる参考訳

  - [Mozillaパブリック・ライセンス1.1（MPL 1.1）](https://ja.osdn.net/projects/opensource/wiki/licenses%2FMozilla_Public_License_1.1) Open Source Group Japanによる参考訳

  - [Mozillaパブリック・ライセンス バージョン1.0](https://ja.osdn.net/projects/opensource/wiki/licenses%2FMozilla_Public_License_1.0)- Open Source Group Japanによる参考訳

[Category:Mozilla](https://ja.wikipedia.org/wiki/Category:Mozilla "wikilink") [Category:オープンソースライセンス](https://ja.wikipedia.org/wiki/Category:オープンソースライセンス "wikilink")

1.
2.
3.
4.
5.
6.  <http://standardsandfreedom.net/index.php/2013/01/24/the-meaning-of-the-4-0/>
7.  <https://www.libreoffice.org/download/license/>
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30. [CePL, version 1.3](http://www.celtx.com/CePL/)
31. [ERLANG PUBLIC LICENSE](http://www.erlang.org/EPLICENSE)
32. [Initial Developer's Public License](http://www.firebirdsql.org/en/initial-developer-s-public-license-version-1-0/)
33. [gSOAP Public License](http://www.cs.fsu.edu/~engelen/license.html)