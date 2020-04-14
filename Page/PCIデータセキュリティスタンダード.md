> この記事は[PCIデータセキュリティスタンダード](https://ja.wikipedia.org/wiki/PCIデータセキュリティスタンダード)から翻訳されています。


**PCIデータセキュリティスタンダード**（**PCI DSS**：Payment Card Industry Data Security Standard）は、 [クレジットカード](../Page/クレジットカード.md "wikilink")情報および取り引き情報を保護するために2004年12月、[JCB](../Page/ジェーシービー.md "wikilink")・[American Express](../Page/アメリカン・エキスプレス.md "wikilink")・[Discover](../Page/ディスカバーカード.md "wikilink")・[マスターカード](../Page/マスターカード.md "wikilink")・[VISAの国際ペイメントブランド](../Page/Visa.md "wikilink")5社が共同で策定した、クレジット業界におけるグローバル[セキュリティ基準である](../Page/コンピュータセキュリティ.md "wikilink")。 2016年4月28日に改訂版であるV3.2が発表された。このバージョンは2016年11月1日発効となる。 これに伴いV3.1は2016年10月31日に失効し、PCI SSCは、2016年4月28日付でPCI DSS v3.2の公開を行った。\[1\]

## 管理団体

上記5社が[PCI SSC](https://ja.pcisecuritystandards.org/)(Payment Card Industry Security Standards Council)を設立し、PCI関連基準の策定・維持、評価手順の確立、認定審査会社の教育・試験等を実施している。PCI SSCが管理する基準にはPCI DSSの他にPA-DSS(Payment Application DSS)、PTS(PIN Transaction Secutity)がある。

## 準拠性確認

PCI DSSはカード会員情報を格納、処理、又は伝送するすべてのメンバー機関、加盟店、サービスプロバイダに対して適用するとされており、その内、カード取扱件数が多い事業者はPCI SSCが認定する審査会社による準拠性確認が必要とされている。

認定審査機関は次の種類がある

  - QSA(Qualified Security Assessor) : 訪問審査を行い、PCIDSSの順守状況を確認・判定する。
  - ASV(Approved Scanning Vendors) : PCIDSS要件11.2に規定される、脆弱性スキャンサービスを提供するベンダー。
  - PFI(PCI Forensic Investigator)PCIDSS要件に規定されるフォレンジック調査を行う認定団体。
  - PA-QSA (P2PE) : P2PEアプリケーションを開発するベンダーに対してインタビュー、ドキュメント調査、システム設定調査などの審査を正式に行う。
  - P2PE QSA : PCI Point-to-Point Encryptionへの認定を調査する。

<!-- end list -->

  -

## 要件

PCI DSS（バージョン3.2）には、カード会員データおよび取り引き情報を保護するための12要件が規定されている。

  - 安全なネットワークの構築と維持
    要件1： カード会員データを保護するために、ファイアウォールをインストールして構成を維持する
    要件2： システムパスワードおよびその他のセキュリティパラメータにベンダ提供のデフォルト値を使用しない

<!-- end list -->

  - カード会員データの保護
    要件3： 保存されたカード会員データを保護する
    要件4： オープンな公共ネットワーク経由でカード会員データを伝送する場合、暗号化する

<!-- end list -->

  - 脆弱性管理プログラムの整備
    要件5： アンチウィルスソフトウェアまたはプログラムを使用し、定期的に更新する
    要件6： 安全性の高いシステムとアプリケーションを開発し、保守する

<!-- end list -->

  - 強固なアクセス制御手法の導入
    要件7： カード会員データへのアクセスを、業務上必要な範囲内に制限する
    要件8： コンピュータにアクセスできる各ユーザに一意の ID を割り当てる
    要件9： カード会員データへの物理アクセスを制限する

<!-- end list -->

  - ネットワークの定期的な監視およびテスト
    要件10： ネットワークリソースおよびカード会員データへのすべてのアクセスを追跡および監視する
    要件11： セキュリティシステムおよびプロセスを定期的にテストする

<!-- end list -->

  - 情報セキュリティポリシーの整備
    要件12： すべての担当者の情報セキュリティポリシーを整備する.

## 出展

<references />

## 関連項目

  - [情報セキュリティマネジメントシステム](../Page/情報セキュリティマネジメントシステム.md "wikilink") (ISMS)
  - [プライバシーマーク](../Page/プライバシーマーク.md "wikilink")

## 外部リンク

  - [Payment Card Industry Security Standards Council](https://ja.pcisecuritystandards.org/)
  - [日本カード情報セキュリティ協議会](http://www.jcdsc.org)
  - [Visa Asia Pacific](https://www.visa.co.jp/partner-with-us/pci-dss-compliance-information.html)
  - [JCB](http://www.jcb-global.com/pci/)
  - [BSIグループジャパン（英国規格協会）](http://www.bsigroup.jp/ja-jp/assessmentandcertification/managementsystem/standardsschemes/pcidss/)

[Category:クレジットカード](https://ja.wikipedia.org/wiki/Category:クレジットカード "wikilink") [Category:情報セキュリティの規格と制度](https://ja.wikipedia.org/wiki/Category:情報セキュリティの規格と制度 "wikilink") [Category:情報社会](https://ja.wikipedia.org/wiki/Category:情報社会 "wikilink")

1.