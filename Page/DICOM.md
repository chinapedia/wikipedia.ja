> この記事は[DICOM](https://ja.wikipedia.org/wiki/DICOM)から翻訳されています。


**DICOM**（ダイコム）とは、[CTや](../Page/コンピュータ断層撮影.md "wikilink")[MRI](../Page/核磁気共鳴画像法.md "wikilink")、[CRなどで撮影した](../Page/コンピュータX線撮影.md "wikilink")[医用画像の](../Page/医用画像処理.md "wikilink")[フォーマットと](../Page/ファイルフォーマット.md "wikilink")、それらを扱う医用画像機器間の[通信プロトコル](../Page/通信プロトコル.md "wikilink")を定義した[標準規格である](../Page/標準化.md "wikilink")。

名称は**Digital Imaging and COmmunications in Medicine**の略である。と[アメリカ電機工業会](https://ja.wikipedia.org/wiki/アメリカ電機工業会 "wikilink")が制定した規格で、異なる製造業者の医用画像機器間で画像転送を可能とすることを目的としている。2000年代初頭までは、DICOM規格に各社の独自規格を組み合わせた形式（方言）が使用されることも多く、当初の理念を実現できない状態が続いていた。昨今はこのような違反は減少し、可搬性の点で医療者が頭を悩ます頻度は減った。

## 画像規格としてのDICOM

撮影直後は[ビットマップ](https://ja.wikipedia.org/wiki/ビットマップ "wikilink")系の[RAWフォーマット](../Page/RAW画像.md "wikilink")、[サーバ](../Page/サーバ.md "wikilink")などへの短期保存時はRAWフォーマット、[連長圧縮](../Page/連長圧縮.md "wikilink")、[ロスレスJPEG](https://ja.wikipedia.org/wiki/Lossless_JPEG "wikilink")、など劣化しない[可逆フォーマット](../Page/可逆圧縮.md "wikilink")、長期保存時は[JPEG](../Page/JPEG.md "wikilink")など[非可逆フォーマット](../Page/非可逆圧縮.md "wikilink")、がそれぞれ多く用いられる。サーバから[ビューアへの配信時は通信効率向上のためJPEG系フォーマットが多用され](https://ja.wikipedia.org/wiki/画像ビューア "wikilink")、[JPEG 2000や独自フォーマットへ内包データを変換して配信する場面も見られる](../Page/JPEG_2000.md "wikilink")。医用画像の色深度は通常 1 byte に収まらず、バイトオーダーは[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")で記述される。

本規格は画像に限らず各種データが内包可能な[コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")で、ファイル内の[タグ情報に内包物のフォーマット名やデータ長を記載する](../Page/タギング_\(コンピュータ\).md "wikilink")。タグ情報が複数ある場合は、画像データも複数枚が内包されるマルチフレームである。[超音波診断装置などは画像に加えて心拍などの音声データを内包している場合もあり](../Page/超音波検査.md "wikilink")、音声とマルチフレームなどの画像を同時に再生し、音声付き動画データとして扱うことも可能である。

## 通信規格としてのDICOM

通信仕様は[RS-232](../Page/RS-232.md "wikilink")など[シリアルケーブル](https://ja.wikipedia.org/wiki/シリアルケーブル "wikilink")を用いた通信など広範な通信手段を網羅するため、[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")に準拠する。[インターネット](../Page/インターネット.md "wikilink")の普及により[RFC 1122に準拠した製品が一般化したために](https://ja.wikipedia.org/wiki/DARPAモデル "wikilink")、最新仕様は通信プロトコルを[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")を用いてカプセル化して大幅な仕様変更を回避したが、[パケット](../Page/パケット.md "wikilink")の[再構成などTCP](https://ja.wikipedia.org/wiki/IPv4#断片化と再構築 "wikilink")/IPが[ネットワークカード](../Page/ネットワークカード.md "wikilink")上の[ハードウェア](../Page/ハードウェア.md "wikilink")で行う処理を、カプセル化データは[ソフトウェア](../Page/ソフトウェア.md "wikilink")で実現するために[オーバーヘッドを生じ](https://ja.wikipedia.org/wiki/オーバーヘッド#派生 "wikilink")、[HTTP](https://ja.wikipedia.org/wiki/HTTP "wikilink")などの純粋にTCP/IPを用いた通信プロトコルに比べて負荷や速度などが大幅に劣る。このため一部製品は他社製品との通信はDICOMに準拠するが、自社製品間の通信は独自プロトコルを用いている場合も多く見受けられる。

## その他の仕様

[英語版に仕様書のリストが掲載されている](https://ja.wikipedia.org/wiki/:en:Digital_Imaging_and_Communications_in_Medicine#Parts_of_the_DICOM_Standard "wikilink")。印刷やデータ保存に関する規定、[個人情報](../Page/個人情報.md "wikilink")に関する[情報セキュリティ](https://ja.wikipedia.org/wiki/情報セキュリティ "wikilink")の仕様、DICOMフォーマットへの[Webアクセスに関する規定などがある](../Page/World_Wide_Web.md "wikilink")。

## 検討課題

「DICOM準拠」機器でも、メーカー間で画像フォーマットやテキストデータなどの扱いが異なる「メーカー方言」\[1\]が存在し、施設相互の運用に影響している\[2\]。

本規格は「人間の医療情報」の保存に特化しており、[競走馬](https://ja.wikipedia.org/wiki/競走馬 "wikilink")の[Ｘ線写真など動物の生体情報は適合せず](../Page/X線撮影.md "wikilink")、獣医畜産用途に改変したシステムの運用も散見される。

## 脚注

## 関連項目

  - [CT](../Page/コンピュータ断層撮影.md "wikilink")
  - [MRI](../Page/核磁気共鳴画像法.md "wikilink")
  - [CR](../Page/コンピュータX線撮影.md "wikilink")
  - [PET](https://ja.wikipedia.org/wiki/ポジトロン断層法 "wikilink")
  - [PDI](https://ja.wikipedia.org/wiki/PDI "wikilink")
  - [OsiriX](https://ja.wikipedia.org/wiki/OsiriX "wikilink")

## 外部リンク

  - [NEMA DICOM Homepage](http://medical.nema.org/)  - DICOM Homepage
  - [社団法人 日本画像医療システム工業会(JIRA) DICOMの世界](http://www.jira-net.or.jp/dicom/index.html) - DICOM 日本語訳
  - [コニカミノルタ　DICOMについて（PDF)](http://konicaminolta.jp/healthcare/attached/pdf/DICOM_04.pdf) - 解説

[Category:健康情報学](https://ja.wikipedia.org/wiki/Category:健康情報学 "wikilink") [Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")

1.  [ＦＡＱ　（ＰＭＡに関するよくある質問）](http://ctp.umin.jp/pmaFaqPage.html)
2.  [DICOM接続の問題点](http://www.ihe-j.org/file2/n30/IHEWS15-11.DICOM-Problem_kawamura.pdf)