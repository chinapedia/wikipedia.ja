> この記事は[Network File System](https://ja.wikipedia.org/wiki/Network_File_System)から翻訳されています。


**Network File System**(**NFS**)は主に[UNIX](../Page/UNIX.md "wikilink")で利用される[分散ファイルシステム](../Page/分散ファイルシステム.md "wikilink")およびその[プロトコルである](../Page/通信プロトコル.md "wikilink")。[1984年](../Page/1984年.md "wikilink")に[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")によって実質的な最初の規格となるNFS version 2 (NFS v2) が発表され、RFC 1094・RFC 1813・RFC 3530・RFC 5661・RFC 7530・RFC 7862 などによって定義されている。

## 概要

NFSは、ローカルに接続された[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")をネットワークを介してリモートの計算機に提供する分散ファイルシステムとそのプロトコルである。[マウントされたNFSボリュームは](https://ja.wikipedia.org/wiki/mount_\(UNIX\) "wikilink")、ネットワーク上にあることを意識せずローカルと同じように利用出来る。NFS v2, v3 では、[Network File System\#関連プロトコルで述べるように](https://ja.wikipedia.org/wiki/Network_File_System#関連プロトコル "wikilink")、ファイルロック機能やクォータ管理機能などはNFSプロトコル本体に含まれず、それぞれ別のプロトコルによって提供される。これらは NFS v4 ではプロトコル本体に含まれている。

### ポート番号

NFSのサービスは一般的に[TCPの](../Page/Transmission_Control_Protocol.md "wikilink")2049番ポートで提供される。NFS v4はTCPのみだが、NFS v3はTCPと[UDP](../Page/User_Datagram_Protocol.md "wikilink")（同じく2049番ポート）を使える。ボリュームを提供するNFSサーバとそれを利用するクライアント間の[遠隔手続き呼出し](../Page/遠隔手続き呼出し.md "wikilink") (RPC) には、NFSの一部として開発された[ONC RPCを利用している](../Page/Open_Network_Computing_Remote_Procedure_Call.md "wikilink")。NFSv3までは、ファイルロックやマウント要求等のONC RPCに使われるポート番号は[ポートマッパー](https://ja.wikipedia.org/wiki/ポートマッパー "wikilink")によって動的に割り当てられることが一般的であった。そのため、ポート番号を固定するオプションを持たない実装の場合、[ファイアウォール](../Page/ファイアウォール.md "wikilink")によるポート番号ベースの通信制御は困難であった。NFSv4からは、同等の機構がNFS本体に組み込まれ、サーバ-クライアント間の通信にはTCPの2049番ポートのみを利用するようになった。

## 歴史

### NFS version 1

NFS version 1 (NFS v1) は、サン・マイクロシステムズ内の実験にとどまり、対外的なリリースはされなかった。

### NFS version 2

NFS v2の仕様は1984年に発表され、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")にはNFS v2を初めて実装した[SunOS](https://ja.wikipedia.org/wiki/SunOS "wikilink") 2.0がリリースされた。その後[1989年](../Page/1989年.md "wikilink")3月には RFC 1094 が取りまとめられ標準化された。 NFS v2の開発にはRusty Sandberg, Bob Lyon, [Bill Joy](../Page/ビル・ジョイ.md "wikilink"), Steve Kleimanなどが参加していた。元々のNFS v2では通信に[UDPのみを利用することになっているが](../Page/User_Datagram_Protocol.md "wikilink")、これはファイルロック機能をNFSの枠組みの外で実装することでプロトコルを[ステートレスに保つのが目的であった](https://ja.wikipedia.org/wiki/ステートレス・プロトコル "wikilink")。

### NFS version 3

[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")6月に RFC 1813 で定義されたNFS v3では、主に以下の機能追加が行われた。

  - ファイルサイズおよび読み書き時に指定するオフセットの型を32bitから64bitに拡張し、4[GiB](https://ja.wikipedia.org/wiki/GiB "wikilink")以上のファイルをサポートした。
  - 書き込み性能を向上させるため、サーバへの非同期書き込みをサポートした。
  - ファイル属性を別途取得するプロシージャ呼び出しを省くために、多くのプロシージャでその返値にファイル属性を追加した。
  - ディレクトリを走査する時、そこに含まれるファイル名に加えファイルハンドルと属性を一度に取得できる*READDIRPLUS*プロシージャを追加した。

また、NFS v2の時点ですでに[TCPによる転送をサポートするベンダーが複数存在したことから](../Page/Transmission_Control_Protocol.md "wikilink")、サン・マイクロシステムズはNFS v3からTCP転送を仕様に追加した。これにより[WANを介したNFSがより安定して動作するようになった](../Page/Wide_Area_Network.md "wikilink")。

### NFS version 4

[AFSや](https://ja.wikipedia.org/wiki/Andrew_File_System "wikilink")[CIFS](https://ja.wikipedia.org/wiki/CIFS "wikilink")の存在を踏まえ、[2000年](../Page/2000年.md "wikilink")12月に RFC 3010 で、また[2003年](../Page/2003年.md "wikilink")4月に RFC 3530 で、さらに2015年3月に RFC 7530 で改定されたNFS v4では、性能の向上策、[Kerberos認証などの強力なセキュリティ](https://ja.wikipedia.org/wiki/ケルベロス認証 "wikilink")、またステートフルなプロトコルを導入した。NFS v4からはその開発主体が[Internet Engineering Task Forceへ移動し](../Page/Internet_Engineering_Task_Force.md "wikilink")、サン・マイクロシステムズに加え[ネットアップ](../Page/ネットアップ.md "wikilink")なども規格策定に携わった。

NFS version 4.1 は、2010年1月に RFC 5661 で公開された。

NFS version 4.2 は、2016年11月に RFC 7862 で公開された。

## 関連プロトコル

NFSに付随するプロトコルは次のようなものがある。

  - Network Lock Manager (NFS v2, v3)
    [UNIX System Vに追加された](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")[ファイルロック](../Page/ファイルロック.md "wikilink")機構
  - [クォータ](https://ja.wikipedia.org/wiki/クォータ "wikilink")情報の遠隔通知 (NFS v2, v3)
    NFSサーバが管理するクォータの状態をクライアントに通知するもので、*rquota*とも呼ばれる。なお、クォータ管理そのものはサーバの役割であり、クライアントはその情報を受け取っているだけである。
  - WebNFS (NFS v2, v3)
    [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")とNFSを統合し、ファイアウォールを介した利用を実現するNFS v2, v3の拡張

## アクセスコントロール

NFS v2およびNFS v3では、ユーザーのアクセス権限にUNIXの[ユーザー識別子および](https://ja.wikipedia.org/wiki/ユーザー識別子#ユーザー識別子 "wikilink")[グループ識別子をそのまま用いている](https://ja.wikipedia.org/wiki/ユーザー識別子#グループ識別子 "wikilink")。 デフォルトではクライアント側に設定された識別子番号がそのままNFSサーバに渡され、サーバはそれを見てアクセスを制御する。クライアントとサーバ間でグループ識別子を別々に管理している場合では、管理者が用意したサーバ側とクライアント側の識別子対応表を参照するか、クライアントが用意した[NISサーバあるいは専用のデーモン](https://ja.wikipedia.org/wiki/ネットワーク・インフォメーション・サービス "wikilink")*ugidd*をサーバが参照するように設定することでアクセスコントロールを行う。

NFS v4では、ユーザー識別子/グループ識別子を直接使うのではなく、文字列としてのユーザー名/グループ名を使用する。更に、[ケルベロス認証](https://ja.wikipedia.org/wiki/ケルベロス認証 "wikilink")を利用したユーザ名ベースのアクセスコントロールを新たにサポートした。

### root squash

一般的に、「NFSクライアント上での管理者特権が適切に管理されている」とは限らない\[1\]ため、管理者権限による無制限なアクセスをNFSクライアントに許可することは危険である。そのため、UNIXシステムでスーパーユーザを示す root (NFS v4) ユーザー識別子0 (NFS v2, v3) によるクライアントからのアクセスを、NFSサーバ側でより権限の低いユーザー識別子（例えば NFS v4 では nobody、NFS v2, v3 では65534や-2\[2\]など）に強制的に割り当てる*root_squash*という機能を標準で有効にするものが多い。

## 利用可能なプラットフォーム

[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に[SunOS](https://ja.wikipedia.org/wiki/SunOS "wikilink") 2.0に最初に実装された後、多くのUNIX系OSに実装された。その他にも[Mac OSや](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[Windows Server](../Page/Windows_Server.md "wikilink")、クライアント[Windowsの一部のエディション](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")、[AS/400](https://ja.wikipedia.org/wiki/AS/400 "wikilink")でも利用できる。Windowsでは[Services for UNIXがNFSサーバおよびクライアントの機能を提供している](https://ja.wikipedia.org/wiki/Services_for_UNIX "wikilink")。

## 注釈

## 関連項目

  - [Common Internet File System](https://ja.wikipedia.org/wiki/Common_Internet_File_System "wikilink")
  - [WebDAV](../Page/WebDAV.md "wikilink")
  - [ネットワークアタッチトストレージ](../Page/ネットワークアタッチトストレージ.md "wikilink") (NAS)
  - [TCP Wrapper](../Page/TCP_Wrapper.md "wikilink")

## 参考文献

  - RFC 1085

  - RFC 1813

  - RFC 3530

  -
  -   -
  -   -
### 各プラットフォームに関する情報

  - Linux
      -
  - FreeBSD
      -
  - Solaris
      -
[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:ファイル転送プロトコル](https://ja.wikipedia.org/wiki/Category:ファイル転送プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  「NFSクライアントからの『**管理者を自称**するユーザ』によるアクセスでも、それが『**真の管理者**ユーザ』とは限らず、実際には『**管理者を詐称**した一般ユーザ』によるアクセス、ということがあり得る」ということ。
2.  ユーザ識別子として伝統的に使用されていた「16ビット長の**符号あり**整数」としての"-2"は、「16ビット長の**符号なし**整数」「32ビット長以上の整数」における"65534"と同値となる。かつては識別子"-2"に"nobody"というユーザ名が割り当てられており、その後"nobody"のユーザ識別子は"65534"に変更された。今日のUNIX系システムでは、識別子"65534"や"-2"に対応するユーザ名は"nfsnobody"や"nobody4"などとされている。