> この記事は[Solaris](https://ja.wikipedia.org/wiki/Solaris)から翻訳されています。


**Solaris**（**ソラリス**）は[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")（サン）によって開発され、[UNIX](../Page/UNIX.md "wikilink")として[認証を受けた](../Page/Single_UNIX_Specification.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。2010年1月27日の[オラクルによるサン買収に伴い](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、現在の開発は同社が担っている。

[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")であるが、かつてコア部分（ONという：OS＋NETの略）は[OpenSolaris](../Page/OpenSolaris.md "wikilink")として[オープンソース](../Page/オープンソース.md "wikilink")化されたが、2010年8月以降、ONのソースコードの公開はされていない。

なお、公開されていたONのソースコードは、有志の手によって[illumos](https://ja.wikipedia.org/wiki/illumos "wikilink")プロジェクトとして[オープンソース](../Page/オープンソース.md "wikilink")化されたまま更新が続けられている。

## 概要

1990年代初頭、サンは[BSD](../Page/BSD.md "wikilink")ベースだった**[SunOS](../Page/SunOS.md "wikilink") 4**を [UNIX](../Page/UNIX.md "wikilink") [System V Release 4](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR4 "wikilink") (SVR4) ベースのものに置き換えた（SVR4は[AT\&T](../Page/AT&T.md "wikilink")とサンが共同で開発した）。 元々の名称は**SunOS 5.0**であったが、 **Solaris 2**という市場用の製品名もついていた。 遡ってSunOS 4.1.*x*も**Solaris 1**と呼ばれるようになったが、 ほとんどの場合Solarisという名前はSVR4ベースのSunOS 5.0以降のものにしか使われない。

SolarisはSunOSオペレーティングシステムに グラフィカル環境（[デスクトップ環境を参照](https://ja.wikipedia.org/wiki/#デスクトップ環境 "wikilink")）や [ONC+などのコンポーネントを加えたものとされている](../Page/Open_Network_Computing_Remote_Procedure_Call.md "wikilink")。 Solarisのリリース名にはSunOSのマイナーバージョン名が含まれていて、 例えば**Solaris 2.4**のコアにはSunOS 5.4が含まれている。 Solaris 2.6以降は"2."の部分がなくなっており、 Solaris 7はSunOS 5.7を、 最新の**Solaris 11**はSunOS 5.11をそれぞれコアとしている。

商業的な歴史については[UNIX戦争](../Page/UNIX戦争.md "wikilink")を参照。

## サポートされているアーキテクチャ

Solarisは[SPARC](../Page/SPARC.md "wikilink")アーキテクチャと[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャ（[AMD64/EM64Tを含む](https://ja.wikipedia.org/wiki/x64 "wikilink")）をサポートし、 両アーキテクチャで共通のコードベースを使用している。バージョン2.5.1では[PowerPC](../Page/PowerPC.md "wikilink")アーキテクチャ（[PReP](https://ja.wikipedia.org/wiki/PReP "wikilink")プラットフォーム）にも移植されたが、それ以降はリリースされていない。[Itanium](../Page/Itanium.md "wikilink")のサポートは一度は計画されたが、市場導入には至っていない。x86システムで[Linux](../Page/Linux.md "wikilink")の実行ファイルをネイティブに実行できるようにするため、Solaris 10にLinux [ABIを実装することが計画されている](../Page/Application_Binary_Interface.md "wikilink")。

Solarisは多数の[CPU](../Page/CPU.md "wikilink")を搭載した[SMPマシンに適していると評されることが多い](../Page/対称型マルチプロセッシング.md "wikilink")。またSolaris 7以降は一貫して[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink") SPARCアプリケーションをサポートしている。SolarisはサンのSPARCハードウェアと密接に統合されており、両者は互いに組み合わせで設計・販売されてきた。これにより信頼性の高いシステムを構築することができたが、PCハードウェアによるシステム（x86システム）に比較すると非常に高コストであった。とはいえ、x86システムもSolaris 2.1以降は一貫してサポートされてきており、また、Solaris 10からは[AMD64を中心に設計されているため](https://ja.wikipedia.org/wiki/x64 "wikilink")、AMD64アーキテクチャベースの64ビット CPUマシンを利用することもできる。

2009年の時点では、サンはハイエンドではSPARCサーバを中心としながら、ローエンドでは2〜16コアのAMD64ベースの[ワークステーション](../Page/ワークステーション.md "wikilink")や[サーバ](../Page/サーバ.md "wikilink")の販売にも重点をおいていた。

2012年の時点では、オラクルはハイエンドではSPARCサーバを中心としながら、Intel Xeonの[サーバ](../Page/サーバ.md "wikilink")も販売されている。

## デスクトップ環境

最初のSolarisの[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")はOpenWindowsだったが、 Solaris2.5で[CDEが採用され](../Page/Common_Desktop_Environment.md "wikilink")、 Solaris 10では[GNOME](../Page/GNOME.md "wikilink")ベースの[Java Desktop Systemとなっている](https://ja.wikipedia.org/wiki/Java_Desktop_System "wikilink")。 Solaris 11では、OpenSolarisと同様、通常のGNOMEデスクトップが採用された。 また、有料版だけでなく無料版にも、ATOKやリコーフォント等の商用ソフトウェアが入っている。

## ライセンス

Solaris 11においては、[Oracle Technology Network Developer License](http://www.oracle.com/technetwork/licenses/solaris-cluster-express-license-167852.html)を参照。

ソースコードは非公開。ただし、[OpenSolaris](../Page/OpenSolaris.md "wikilink")プロジェクトから派生した[illumos](https://ja.wikipedia.org/wiki/illumos "wikilink")プロジェクトでは、[Common Development and Distribution License](https://ja.wikipedia.org/wiki/Common_Development_and_Distribution_License "wikilink") (CDDL) の下オープンソースとして公開されている。CDDLは[OSIが承認したライセンスで](../Page/Open_Source_Initiative.md "wikilink")、公開されているソースコードは、使用料が無料であり、無保証で非独占的な利用が可能である。頒布にあたって、ソフトウェアを実行可能なコード形式で提供する場合は、CDDLに従ってソースコードの提供が義務づけられており、CDDLのコピーを添付しなくてはならない。ただし、[Free Software Foundationの](../Page/フリーソフトウェア財団.md "wikilink")[GPLと似ている部分があるが](../Page/GNU_General_Public_License.md "wikilink")、互換ではないと考えられている\[1\]。

OpenSolarisは2005年6月14日にSolarisの開発コードから誕生し、バイナリ版とソースコード版を無料でダウンロードできるようになった。すでに[Xenサポート等の新しい機能がOpenSolarisプロジェクトに追加されており](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")、サンは将来のSolarisはOpenSolarisから派生したものをリリースすると表明しており、実際にそうなった。

OS本体を無料化する一方で[パッチ](../Page/パッチ.md "wikilink")のダウンロードは一部が有料化されていた。

オラクルによるサン買収後の2010年4月に、90日の試用後\[2\]は商用利用では有償のサポート契約が必須、個人利用、開発用途では無料\[3\]となった。

2010年8月以降、ソースコードをオープンにしながらの開発をやめ、snv_147というバージョン以降のソースコードの公開は停止している。同時期にCDDLで公開されているSolarisのソースコードの一部をベースにある程度の互換性をもつコミュニティベースでオープンソースのillumos Projectが派生している。このライセンスはCDDLを中心にBSDLで配布されているモジュールも含む。

## バージョン

Solarisのバージョンは以下の通りである:

| Solarisのバージョン | SunOSのバージョン | リリース日                                                                                           | 主な特徴                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ------------- | ----------- | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2.0           | 5.0         | [1992年](../Page/1992年.md "wikilink")6月                                                          | 準備的なリリース。sun4cアーキテクチャしかサポートしなかった。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 2.1           | 5.1         | 1992年12月(SPARC), [1993年](../Page/1993年.md "wikilink")5月(x86)                                    | sun4/sun4mアーキテクチャのサポート追加。最初のx86版のリリース。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 2.2           | 5.2         | 1993年5月                                                                                         | sun4dアーキテクチャのサポート追加。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 2.3           | 5.3         | 1993年11月                                                                                        | OpenWindows 3.3が[NeWS](../Page/NeWS.md "wikilink")から[Display PostScriptへ変更](../Page/Display_PostScript.md "wikilink")。SunViewサポートの削除(SPARCのみ)。                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 2.4           | 5.4         | [1994年](../Page/1994年.md "wikilink")11月                                                         | SPARC/x86の最初の統合リリース。OSF/Motifランタイムをサポート。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 2.5           | 5.5         | [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")11月                                      | 最初のUltraSPARCのサポート。CDE, [NFSv3](../Page/Network_File_System.md "wikilink"), NFS/TCPのサポート。sun4([VME](../Page/VMEバス.md "wikilink"))のサポート削除。                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 2.5.1         | 5.5.1       | [1996年](../Page/1996年.md "wikilink")5月                                                          | PowerPCプラットフォームをサポートする唯一のリリース。Ultra Enterpriseサポート追加。ユーザID・グループID(uid_t, gid_t)の32ビット化。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 2.6           | 5.6         | [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")7月                                       | Kerberos 5, PAM, TrueType fonts, WebNFS, 大規模ファイルサポート。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 7             | 5.7         | [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")11月                                      | 64-bit UltraSPARCのサポート。メタデータのロギング機能(UFS logging)追加。[MCAサポートの終了](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")(Intelプラットフォーム)。                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 8             | 5.8         | [2000年](../Page/2000年.md "wikilink")2月                                                          | マルチパスI/O、IPv6、IPsec。[ロールベースアクセス制御](../Page/ロールベースアクセス制御.md "wikilink")(RBAC)を追加。sun4cアーキテクチャのサポート終了。最終リリースはSolaris 8 2/04。                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 9             | 5.9         | [2002年](../Page/2002年.md "wikilink")5月28日(SPARC), [2003年](../Page/2003年.md "wikilink")2月6日(x86) | iPlanet Directory Server, Resource Manager, [Solaris Volume Manager](../Page/Solaris_Volume_Manager.md "wikilink"), [拡張ファイル属性](https://ja.wikipedia.org/wiki/拡張ファイル属性 "wikilink"), Linux互換性サポートを追加。OpenWindowsの削除。sun4dアーキテクチャのサポート終了。最終リリースはSolaris 9 9/05。                                                                                                                                                                                                                                                                                                                                      |
| 10            | 5.10        | [2005年](../Page/2005年.md "wikilink")1月31日                                                       | x64(AMD64/EM64T)サポート, DTrace (Dynamic Tracing), Solaris Containers, Service Management Facility (SMF), [NFSv4](../Page/Network_File_System.md "wikilink"), 最小特権セキュリティモデルの追加。sun4mアーキテクチャとクロックが200MHz以下のUltraSPARC Iプロセッサのサポート終了。EISAデバイス/EISAベースPCのサポート終了。Java Desktop System([GNOME](../Page/GNOME.md "wikilink")ベース)をデフォルトのデスクトップとして採用。Solaris 10 1/06では、ブートローダとして[GRUBを採用](../Page/GNU_GRUB.md "wikilink")(x86)、[iSCSI](https://ja.wikipedia.org/wiki/iSCSI "wikilink")サポート追加。Solaris 10 6/06では[Zettabyte File System](https://ja.wikipedia.org/wiki/Zettabyte_File_System "wikilink")(ZFS)追加。 |
| 11            | 5.11        | [2011年](../Page/2011年.md "wikilink")11月9日                                                       | IPS（新パッケージマネージャ）、COMSTAR（iSCSIターゲット）、Crossbow（ネットワーク仮想化）、ZFSの強化（重複排除機能、暗号化など）、Solaris Containersの強化（リソースの仮想化機能や、制限機能の強化）、その他　(snv175)                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

Solaris 9までのバージョンはすでに販売されておらずサポートも終了している（Solaris 7は2008年8月まで、Solaris 8は2012年3月まで、Solaris 9は2014年10月までサポートされていた）。Solaris 10は2021年1月まで、Solaris 11は2034年11月までサポート予定。

各バージョンの詳細は\[4\](英文)を参照。 リリース履歴はSolaris 2 FAQ\[5\](英文)にも記載がある。 サポート終了日は\[6\](英文)を参照。

現行のSolarisの特徴的な機能として、 DTrace・Doors・Service Management Facility・Solaris Containers ・Solaris Multiplexed I/O・[Solaris Volume Manager](../Page/Solaris_Volume_Manager.md "wikilink")・[ZFSが挙げられる](https://ja.wikipedia.org/wiki/Zettabyte_File_System "wikilink")。

### Solaris 10のアップデート履歴

| アップデート名              | リリース日                                                     | 主な変更・追加点                                                                                                                              |
| -------------------- | --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Solaris 10 **3/05**  | [2005年](../Page/2005年.md "wikilink")3月                    | 予測的自己修復機能の追加、\[Java Desktop System Release 3|Java Desktop System、Unicode Version 4.0 サポートの追加、x86 システムにおける64 ビットのサポート及びSunVTS のサポートの追加 |
| Solaris 10 **1/06**  | [2006年](../Page/2006年.md "wikilink")1月                    | x86システムにおいてGRUBベースのブートへの変更、Sun Update Connectionの追加                                                                                   |
| Solaris 10 **6/06**  | 2006年6月                                                   | [ZFSの統合](https://ja.wikipedia.org/wiki/Zettabyte_File_System "wikilink")、PostgreSQL・RealPlayer等の標準添付、PDAサポートの追加。                      |
| Solaris 10 **11/06** | 2006年11月                                                  |                                                                                                                                       |
| Solaris 10 **8/07**  | [2007年](../Page/2007年.md "wikilink")8月                    |                                                                                                                                       |
| Solaris 10 **5/08**  | [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")5月 |                                                                                                                                       |
| Solaris 10 **10/08** | 2008年10月                                                  |                                                                                                                                       |
| Solaris 10 **05/09** | [2009年](../Page/2009年.md "wikilink")5月                    |                                                                                                                                       |
| Solaris 10 **10/09** | 2009年10月                                                  |                                                                                                                                       |
| Solaris 10 **9/10**  | [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")9月 |                                                                                                                                       |
| Solaris 10 **8/11**  | [2011年](../Page/2011年.md "wikilink")9月                    | Oracle Solaris 10 8/11 としてリリース。                                                                                                       |
| Solaris 10 **1/13**  | [2013年](../Page/2013年.md "wikilink")2月                    |                                                                                                                                       |

この他、開発・早期評価版であるSolaris Expressでのリリースを区切りとして追加または変更されている機能が多数ある。各リリースの詳細な概要説明は [Solaris 10の概要](http://docs.oracle.com/cd/E19253-01/819-0359/) を参照されたい。

### Solaris 11のアップデート履歴

| アップデート名      | リリース日                                   | 主な変更・追加点 |
| ------------ | --------------------------------------- | -------- |
| Solaris 11.1 | [2012年](../Page/2012年.md "wikilink")10月 |          |
| Solaris 11.2 | [2014年](../Page/2014年.md "wikilink")4月  |          |
| Solaris 11.3 | [2015年](../Page/2015年.md "wikilink")10月 |          |

2017年9月にオラクルが Solaris 開発の大半の社員を解雇したことが報道された\[7\]。Solaris 11が最後のバージョンとなり12はリリースされない予定。

## 開発リリース

Solarisのコードベースは1980年代後半に開発が開始されて以来、 絶え間ない改良が加えられてきた。 Solaris 10といった各々のバージョンは そのリリースの前後にメインの開発コードから切り放され、 リリース以降は派生プロジェクトとしてメンテナンスされる。 派生したプロジェクトに対する更新は 次の公式なメジャーリリースがあるまで年に数回行なわれる。

2006年では、開発版のSolarisはOpenSolarisから派生しており **Nevada**と名付けられている。

2003年に新しいSolarisの開発プロセスが導入され、 [**Solaris Express**](http://sun.com/solaris-express)という名前で 開発版の月ごとのスナップショットをダウンロードできるようになった。 これによりだれでも新しい機能を試したり、 OSの品質・安定性をテストできるようになり、 次期の公式Solarisリリースを促進させることとなった。

Solaris ExpressはOpenSolarisプロジェクトよりも前に開始されたため、 もともとはバイナリのみを提供するプログラムであったが、 現在ではOpenSolaris開発者向けの[**Solaris Express: Community Release**](http://www.opensolaris.org/os/downloads/on/)と呼ばれるバージョンが存在した（現在は配布をしていない）。

Solaris 11の機能先出し版として、2010年11月に、Solaris 11 Expressがリリースされている。

## illumos プロジェクト

[illumos](https://ja.wikipedia.org/wiki/illumos "wikilink")プロジェクトではオラクルがソースコード公開をしたら追従するSpork（先割れスプーン）と宣言しているが、illumos側は他の[オープンソース](../Page/オープンソース.md "wikilink")OSの様々な部分を取り入れており、事実上ONの最終公開バージョンであるバージョンsnv_147からのForkとなっている。

また一方で、最新版のSolaris 11にも時流に合わせて様々な機能（仮想化機能、ファイルシステム強化、パッケージシステム強化等）が追加されており、最新の技術潮流に合わせて強化が進められている。

そのため、同じ根をもつOracle Solarisとillumosは、徐々に差を開きつつあるといえる。

## 脚注

<references />

## 関連項目

  - [SunOS](../Page/SunOS.md "wikilink")
  - [SVR4](https://ja.wikipedia.org/wiki/SVR4 "wikilink")
  - [illumos](https://ja.wikipedia.org/wiki/illumos "wikilink")

## 外部リンク

  - [Solaris 11 公式サイト](https://www.oracle.com/jp/solaris/solaris11/)

[Category:System_V](https://ja.wikipedia.org/wiki/Category:System_V "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink") [Category:1992年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1992年のソフトウェア "wikilink")

1.
2.  現在のトライアルライセンスは、試用期間が30日間に限定されている。(2016年08月01日 時点)
3.
4.
5.
6.
7.  [Oracle staff report big layoffs across Solaris, SPARC teams • The Register](https://www.theregister.co.uk/2017/09/04/oracle_layoffs_solaris_sparc_teams/)