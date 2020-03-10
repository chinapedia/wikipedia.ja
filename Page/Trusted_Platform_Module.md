> この記事は[Trusted Platform Module](https://ja.wikipedia.org/wiki/Trusted_Platform_Module)から翻訳されています。


**Trusted Platform Module** (TPM) とは、コンピュータにおいて、セキュリティに関する各種機能を備えたデバイスもしくはチップであり、国際標準規格（[ISO/IEC](https://ja.wikipedia.org/wiki/ISO/IEC "wikilink") 11889）のに則ったもの\[1\]\[2\]。主に専用チップとして実装されたディスクリートTPMと、CPU内部のセキュリティ領域で実行されるファームウェアTPMがある\[3\]。

## 概要

[RSA暗号](../Page/RSA暗号.md "wikilink")演算や[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")[ハッシュ演算といった機能を有しており](../Page/ハッシュ関数.md "wikilink")、チップ内で暗号化・復号、[デジタル署名](../Page/デジタル署名.md "wikilink")の生成・検証、[プラットフォームの完全性検証](../Page/プラットフォーム_\(コンピューティング\).md "wikilink") を行うことができる。また、TPMの内部でRSAの鍵ペア（[公開鍵](https://ja.wikipedia.org/wiki/公開鍵 "wikilink")と[秘密鍵](https://ja.wikipedia.org/wiki/秘密鍵 "wikilink")）を生成することができる。

TPMの仕様はTCG(Trusted Computing Group)という国際的な業界団体で策定されており、最新のバージョンは2.0である。1.2までは[RSAのみであったが](../Page/RSA暗号.md "wikilink")、2.0からは[AESや](../Page/Advanced_Encryption_Standard.md "wikilink")[ECDSAなどを含め多種多様な暗号アルゴリズムの処理をチップ内でできるようになり](https://ja.wikipedia.org/wiki/楕円曲線DSA "wikilink")、ソフトウェアが暗号ライブラリを負担する必要が大幅に無くなったため、暗号境界がより明瞭になった。

ノートPCだけではなく、デスクトップPCにもTPMは搭載されている。Windows OSとしては[Windows Vistaが初めて正式にサポートした](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")\[4\]。Intelチップを搭載した初期のMacintoshにもTPMチップを搭載したものがある\[5\]。

この技術は、さらに発展を遂げている。チップセット等の連携を強化した技術として、Intel [Trusted Execution Technology](https://ja.wikipedia.org/wiki/:en:Trusted_Execution_Technology "wikilink") がある。また、[仮想機械](../Page/仮想機械.md "wikilink")向けの命令仕様拡張も提案されている\[6\]。

組み込み用途向けとしては、SPIやI2Cなどのインタフェースを持つものがリリースされている。ピン数が少なくなるためコストが縮小するほか、インタフェースの簡素化など攻撃表面の縮小(Attack surface reduction)の概念と相性が良いという利点がある。近年、車の自動運転や[IoTなどで需要を伸ばしている分野である](https://ja.wikipedia.org/wiki/モノのインターネット "wikilink")。

Trusted Computing Groupは、特にディスクリートTPMについて、求められるセキュリティレベルを考慮すると、[耐タンパー性](https://ja.wikipedia.org/wiki/耐タンパー性 "wikilink")を備えているべきだとしている\[7\]。

## TPMの機能

TPMは以下の機能を提供する。

  - [RSA](../Page/RSA暗号.md "wikilink")
      - 演算
      - 鍵生成
      - 鍵格納
  - [SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")ハッシュ
      - ハッシュ値計算
      - ハッシュ値保管
  - [乱数生成](../Page/擬似乱数.md "wikilink")

TPM1.2から以下の機能が追加された。

  - カウンタ
      - 単純増加カウンタ
      - ティックカウンタ
  - オーナー権委任（パスワードは公開しない）
  - 不揮発性ストレージ保存機能

TPM2.0は機能や概念が一新され、以下が追加された。

  - シードとオブジェクトの概念
  - 認証形式の追加（[KDFによるセッション鍵生成](https://ja.wikipedia.org/wiki/:en:Key_derivation_function "wikilink")、Policy認証）
  - 認証と秘密通信の高速化

<!-- end list -->

  - アルゴリズムの大幅な追加
      - 各種ハッシュ演算(SHA256、SM3、HMAC、KDFなど)
      - 楕円曲線暗号(NIST curve P-256、SM2など)
      - AES(128bit～256bit、OFB、CTRなどの各種モード)
  - グループの複製(Key duplication)

<!-- end list -->

  - 不揮発性カウンタ
  - 不揮発性ビットフィールド

## TPMでできること

上記の機能を用いて、TPMでは以下のことを実現できる。

  - プラットフォームの完全性を計測し、OSやアプリケーションの[改竄](../Page/改竄.md "wikilink")を検知できる。
  - [公開鍵証明書](../Page/公開鍵証明書.md "wikilink")を用いた端末の個体識別、詐称困難な端末[認証](../Page/認証.md "wikilink")を実現する。
  - データ（ストレージ）を暗号化し、不正に持ち出した情報は復号させない。

## TPM利用時の注意点

TPMをハードウェアに搭載したからといって即座にシステム全体のセキュリティを担保できるわけではない。TPMを使用するシステムの要件定義からアプリケーションの実装まで全てを考慮しなければ、最終的に容易に破られるシステムができあがることになる。

チップ自体のスペックが高くないことや、内部ファームウェアがセキュアコーディングで書かれていること、インタフェースが低速であることが原因で、数百キロバイトを超えたデータの暗号／復号は時間がかかることに留意する必要がある。

TPMのファームウェアリビジョンによっては、対称鍵暗号コマンド(TPM2_EncryptDecrypt2)が実装されておらず、伝送系路上に乗る平文を暗号化できない場合がある。

## TPM利用技術

  - [BitLocker](https://ja.wikipedia.org/wiki/BitLocker "wikilink")

<!-- end list -->

  -
    [マイクロソフト](../Page/マイクロソフト.md "wikilink")のドライブ暗号化技術。TPMを利用したハードディスクドライブの暗号化が可能。ただし必ずしもTPMを用いなければならないわけではなく、[USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")キーに鍵を格納する方法や、パスワードで保護する方法がある\[8\]

<!-- end list -->

  - [Trusted HTTP-FUSE KNOPPIX](http://unit.aist.go.jp/itri/knoppix/http-fuse/)

<!-- end list -->

  -
    [産業技術総合研究所](https://ja.wikipedia.org/wiki/産業技術総合研究所 "wikilink")からリリースされている、HTTPブート[クノーピクスのTPM利用版](../Page/KNOPPIX.md "wikilink")。TPMのプラットフォーム検証技術を利用して、[ブート](../Page/ブート.md "wikilink")シーケンスが改ざんされていないかを監視することが可能

## 脚注

<references/>

## 関連項目

  - [次世代セキュアコンピューティングベース](../Page/次世代セキュアコンピューティングベース.md "wikilink")
  - [デジタル著作権管理](https://ja.wikipedia.org/wiki/デジタル著作権管理 "wikilink")

## 外部リンク

  - [Trusted Computing Group](http://www.trustedcomputinggroup.org/)
      - [TPM Work Group](http://www.trustedcomputinggroup.org/groups/tpm/)

[Category:セキュリティ技術](https://ja.wikipedia.org/wiki/Category:セキュリティ技術 "wikilink") [Category:情報セキュリティの規格と制度](https://ja.wikipedia.org/wiki/Category:情報セキュリティの規格と制度 "wikilink")

1.  [1](http://web.archive.org/web/20191225223523/http://e-words.jp/w/TPM.html)
2.  [2](http://web.archive.org/web/20191129065440/https://www.iso.org/standard/66510.html)
3.
4.  日経エレクトロニクス2007年10月8日号p101「初めてTPMに対応したWindows Vista」
5.  [アップル、「Intel Mac」にセキュリティチップ搭載](http://japan.cnet.com/news/tech/story/0,2000056025,20086162,00.htm)（2005年8月5日）
6.  [vTPM: Virtualizing the Trusted Platform Module](http://www.usenix.org/events/sec06/tech/berger.html), 15th [USENIX](../Page/USENIX.md "wikilink") Security Symposium Abstract, Pp. 305–320 of the Proceedings
7.  [3](http://web.archive.org/web/20190203202259/https://www.trustedcomputinggroup.org/wp-content/uploads/TPM-2.0-A-Brief-Introduction.pdf)
8.  [TPM機能が搭載されていないモデルでBitLockerドライブ暗号化を有効／無効にする方法](http://qa.support.sony.jp/solution/S1211130043944/?rt=support)