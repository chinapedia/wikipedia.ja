> この記事は[MIFARE](https://ja.wikipedia.org/wiki/MIFARE)から翻訳されています。


**MIFARE**（マイフェア）は、[NXPセミコンダクターズ](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink")（[フィリップス](../Page/フィリップス.md "wikilink")の半導体部門が独立）の非接触[ICカード](../Page/ICカード.md "wikilink")通信規格の一つ。

非接触ICカード、近接型ICカードとして世界でもっとも多く採用されているといわれている。12億個\[1\]のICカード用チップと、500万台のリーダが販売されている。NXPセミコンダクターズがこの技術に関する特許を保有し、同社の登録商標（日本においては第4151267号）である。

## 概要

MIFAREは非接触ICカードの国際規格「[ISO/IEC 14443](https://ja.wikipedia.org/wiki/ISO/IEC_14443 "wikilink") ([RFID](../Page/RFID.md "wikilink")) Type A」に基づいた技術である。ICカードとリーダの両方に適用される。

MIFAREと名づけられた非接触ICカードは4種類存在する。

  - MIFARE Standard (Classic) カード：ISO/IEC 14443-4の代わりにNXP独自のアルゴリズム非公開の認証と暗号化プロトコルを採用している。
  - MIFARE UltraLightカード：MIFARE Standardからセキュリティといくつかのコマンドを除いたもの。
  - MIFARE DESfireカード：ISO/IEC 14443-4(T=CL)準拠のICカード。NXP製のOSがROMに焼きこんである。
  - MIFARE Prox、MIFARE smartMX：ISO/IEC 14443-4 (T=CL)に準拠したICカード。

### MIFARE Standard / MIFARE UltraLight

MIFARE Standard と MIFARE UltraLightは、基本的には単なるメモリーカードである。メモリは、セグメントとブロックに分けられ、シンプルなセキュリティのメカニズムによってアクセス制御がなされている。ASICベースのため計算能力は限られている。しかし、安価で高信頼なため、電子マネー、社員証、交通機関や競技場のチケットなどとして用いられている。

MIFARE Standard 1kは、約768バイトのメモリを持ち、それが16のセクタに分かれている。これらのセクタは、AとBと呼ばれる二つの鍵でプロテクトされている。それぞれのセクタに対して、読み込み、書き込み、値の増減などの操作ができる。MIFARE Standard 4kは、3kBのメモリを持ち、それが40のセクタに分かれている。そのうち32のセクタがMIFARE Standard 1kのセクタと同じ容量で、残りの8つが倍の容量を持つ。MIFARE Standard miniのメモリ容量は320バイトで、5つのセクタを持つ。

MIFARE UltraLightは、わずか64バイトの容量で、セキュリティ機能もない。非常に安価なため、使い捨てのチケットとして用いられている。2006年ワールドカップでも使われた。

これらのカードはシンプルなため安価で、そのため大規模に普及した。

MIFARE Standardは、1994年に発売された非接触ICカードということもあり設計が古く、また独自の暗号化アルゴリズムに脆弱性が判明したため\[2\]MIFARE Classicに改名された。脆弱性に対応した代替品には、MIFARE Plusがある。

\=== MIFARE T=CL カード === MIFARE ProX と SmartMX は、[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を用いている。ハードウェア単体では動作せず、専用の[OSが必要になる](../Page/オペレーティングシステム.md "wikilink")。暗号計算（[トリプルDES](../Page/トリプルDES.md "wikilink")、[AES](../Page/Advanced_Encryption_Standard.md "wikilink")、[RSA暗号](../Page/RSA暗号.md "wikilink")等）のために[コプロセッサ](../Page/コプロセッサ.md "wikilink")が内蔵されていることが多い。処理速度や機能は接触型カードに匹敵する。実際、SmartMXシリーズには、接触型や接触/非接触両方の[インタフェースを備えたカードもある](../Page/インタフェース_\(情報技術\).md "wikilink")。ベンダ独自のOS、オープンOS（JavaCard等）両方に対応できる。

インストールされるソフトウェアによって、カードはさまざまな目的に使われるが、高いレベルのセキュリティが必要とされる場合に用いられることが多く（ICパスポート、クレジットカードなど）、[コモンクライテリア](../Page/コモンクライテリア.md "wikilink")など、第三者の認定をうけていることが多い。SmartMXは、[ドイツ連邦電子情報保安局によって](../Page/BSI_\(ドイツ\).md "wikilink")、コモンクライテリアのEAL5+認定を受けており、リバースエンジニアリング、故障利用攻撃、電力解析等への高い耐タンパー性を持つ。最終製品でこのような認証を取得するためには、チップ上で動作するOSも認証を取得する必要がある。

### MIFARE DESFire

The MIFARE DESFireは、MIFARE Standardとは異なり、マイクロプロセッサにDESFire OSというソフトウェアがプログラムされている。MIFARE Standard 4kとほぼ同等の機能をもつが、より高い柔軟性と、より強力なトリプルDESセキュリティを持ち、より高速で、T=CLの規格にも準拠している。カードとリーダライタの通信可能距離はリーダライタの電波強度やアンテナサイズに依存するが、およそ10cm程度。

### MIFARE DESFire8

DESFireの8kB版だが、他に以下のような特長がある。

  - ランダムUID
  - AES128暗号に対応
  - コモンクライテリアEAL4＋

2006年11月に発表された。

### MIFARE Plus

MIFARE Plus は、Mifare Classicの脆弱性に対処した代替となりうるカード。既存システムをより安全性の高い[オープン標準](../Page/オープン標準.md "wikilink")にアップグレードできるよう考慮されている。他に、以下のような特長がある。

  - ランダムUID（7バイト）
  - AES128暗号に対応
  - コモンクライテリアEAL4+

2008年3月に発表され、2008年第4四半期にサンプル出荷される。

## 歴史

MIFAREはもともとはMikronによって開発されたもので、MIFAREは「**MI**kron **FARE**-collection System」の略である。Mikronは、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")のAtmel、オランダのフィリップス、[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")の[シーメンス](../Page/シーメンス.md "wikilink")にMIFARE技術をライセンスした。1998年にフィリップス社によって買収された。

フィリップスによる買収の後、[日立製作所](../Page/日立製作所.md "wikilink")もMIFAREのライセンスを取得した。これは1999年に開始され2006年に終了したNTTの非接触IC[テレホンカード](../Page/テレホンカード.md "wikilink")の開発プロジェクトのためだった。NTTの非接触ICテレホンカード開発プロジェクトには3つの陣営が参加していた。[トーキン](https://ja.wikipedia.org/wiki/NECトーキン "wikilink")-[田村電機](../Page/サクサホールディングス.md "wikilink")-[シーメンス](../Page/シーメンス.md "wikilink")連合、日立製作所-フィリップス（技術サポートのみ）連合、[デンソー](https://ja.wikipedia.org/wiki/デンソー "wikilink")-[モトローラ](../Page/モトローラ.md "wikilink")（製造のみ）連合である。NTTは、MIFARE Classicのような、ワイヤードロジックによる小容量のものと大容量の2種類のチップを要求した。日立製作所は大容量バージョンのみを開発し、そのメモリ容量を小さくして小容量バージョンとした。シーメンスは保有するMIFAREテクノロジーを改良し、チップを開発した。モトローラはMIFAREのようなチップの開発を試みたが、最終的には断念した。当初、ICテレホンカードは100万枚/月の売り上げが見込まれていたが、最終的な売り上げは10万枚/月程度だった。

  - [1994年](../Page/1994年.md "wikilink") - MIFARE Standard 1k 非接触テクノロジが発表される
  - [1996年](../Page/1996年.md "wikilink") - 韓国ソウルの「バスカード（現在の[Uパス](https://ja.wikipedia.org/wiki/Uパス "wikilink")）」でMIFARE Standard 1kが用いられる
  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink") - トリプルDESコプロセッサ搭載のMIFARE PROが発表される
  - [1999年](../Page/1999年.md "wikilink") - PKIコプロセッサ搭載のMIFARE PROXが発表される
  - [2001年](../Page/2001年.md "wikilink") - MIFARE UltraLight が発表される
  - [2002年](../Page/2002年.md "wikilink") - マイクロプロセッサを用いた、MIFARE DESFireが発表される
  - [2004年](../Page/2004年.md "wikilink") - MIFARE DESFiireを用いるシステムで使用するMIFARE DESFiire SAMが発表される
  - [2006年](../Page/2006年.md "wikilink") - MIFARE DESFiire8が、AES128暗号対応の最初の製品として発表される
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")3月 - MIFARE PLUS が、MIFARE Classicの代替として発表される

## セキュリティ

2007年12月に行われた第24回カオスコミュニケーション会議 ([Chaos Communication Congress](https://ja.wikipedia.org/wiki/:en:Chaos_Communication_Congress "wikilink"))で、ヘンリック・プロッツとカーステン・ノールは [MIFARE Classic](https://ja.wikipedia.org/wiki/#MIFARE_Standard "wikilink") の脆弱性に関するプレゼンテーションを行った。彼らは MIFARE Classic のチップに対してリバースエンジニアリングを行い、MIFARE Classic のアルゴリズムを解析し、いくつかの脆弱性を発見した。彼らは、解析された暗号アルゴリズムの詳細とその脆弱性についての論文を2008年中に発表するとした。なお、この件は MIFARE Classic 以外のカードには無関係である。

2008年3月には、オランダの[ナイメーヘン](../Page/ナイメーヘン.md "wikilink")にある[ラドバウド大学](https://ja.wikipedia.org/wiki/ラドバウド大学 "wikilink") (Rdaboud University Nijmegen) のデジタルセキュリティ研究グループが、MIFARE Classicカードのプロトコルを解析することによって認証/暗号化アルゴリズムの特定に成功し、さらに鍵を効率的に特定できることを公表した。MIFARE Classic の鍵長は[48ビット](https://ja.wikipedia.org/wiki/48ビット "wikilink")なので、そのままでも[総当り攻撃](https://ja.wikipedia.org/wiki/総当り攻撃 "wikilink")可能であるが、アルゴリズムの脆弱性を利用すれば数分で特定できるという。鍵を特定できるとクローンカードを作成することができる\[3\]\[4\]。

この結果を受けて、オランダ自治省及びオランダ王国関係者は [Rijkspas](https://ja.wikipedia.org/wiki/:nl:Rijkspas "wikilink") の導入を2008年第4四半期から延期するか検討すると発表した\[5\]。

## 参考・脚注

## 関連項目

  - [ICカード](../Page/ICカード.md "wikilink")
  - [RFID](../Page/RFID.md "wikilink")
  - [NFC](../Page/近距離無線通信.md "wikilink")
  - [運転免許証](../Page/運転免許証.md "wikilink") - [taspo](https://ja.wikipedia.org/wiki/taspo "wikilink") - [在留カード](https://ja.wikipedia.org/wiki/在留カード "wikilink") - [住民基本台帳カード](../Page/住民基本台帳カード.md "wikilink") - [個人番号カード](https://ja.wikipedia.org/wiki/個人番号カード "wikilink")

## 外部リンク

  - [MIFARE.net](http://www.mifare.net/) - 公式サイト
  - [NXPセミコンダクターズ](http://www.jp.nxp.com/)
  - [Mifareとは？](http://developers.orangetags.jp/words/mifare)

[Category:ICカード](https://ja.wikipedia.org/wiki/Category:ICカード "wikilink") [Category:フィリップスの製品](https://ja.wikipedia.org/wiki/Category:フィリップスの製品 "wikilink")

1.  <http://www.atmarkit.co.jp/frfid/rensai/iccard/iccard03/nfc01.html>
2.  K. Nohl, Starbug and H. Plotz. "Mifare, little security, despite obscurity." Pre-sentation on the 24th Congress of the Chaos Computer Club (CCC), December 2007.
3.  <http://www.hrgeeks.com/2008/03/14/so-long-mifare-rf-id-system/>
4.  [「ICカードの暗号は数分で解読可能」――RFIDのセキュリティ懸念広がる](http://www.computerworld.jp/topics/563/100469)
5.  <http://www.minbzk.nl/actueel/110972/veel-chips-in>