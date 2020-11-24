> この記事は[CPRM](https://ja.wikipedia.org/wiki/CPRM)から翻訳されています。


**CPRM**（）とは、「[コピー・ワンス](../Page/コピー・ワンス.md "wikilink")（1世代だけ録画可能）」の番組を録画する時に使われるコピー制御方式である。 録画に際しては、CPRMに対応した各種メディア（[DVD-R](https://ja.wikipedia.org/wiki/DVD-R "wikilink")・[DVD-RW](https://ja.wikipedia.org/wiki/DVD-RW "wikilink")・[DVD-RAM](../Page/DVD-RAM.md "wikilink")・[DVD-R DL](https://ja.wikipedia.org/wiki/DVD-R_DL "wikilink")）や機器（[DVDプレーヤー](../Page/DVDプレーヤー.md "wikilink")や[DVDレコーダー](../Page/DVDレコーダー.md "wikilink")、[DVDドライブなど](../Page/光学ドライブ.md "wikilink")）に加え、[ソフトが必要である](../Page/ライティングソフトウェア.md "wikilink")。 [SDメモリーカード](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")や[SD-Audio](../Page/SD-Audio.md "wikilink")及びSDカード対応の携帯電話の著作権コンテンツ保存（SDバインディング）にも採用されている。

## 概要

[4C Entity](https://ja.wikipedia.org/wiki/4C_Entity "wikilink")（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[IBM](../Page/IBM.md "wikilink")、[東芝](../Page/東芝.md "wikilink")、[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")が設立した団体）によって開発された。[DVD-Video](../Page/DVD-Video.md "wikilink")で採用されている[CSSの](../Page/Content_Scramble_System.md "wikilink")[暗号鍵](https://ja.wikipedia.org/wiki/暗号鍵 "wikilink")が破られたことに対する反省からさらにシステムを強化し、万一暗号鍵が破られても対処出来るようにしたものである。

## 実装

[2004年](../Page/2004年.md "wikilink")（平成16年）[4月5日](../Page/4月5日.md "wikilink")から[BS](../Page/放送衛星.md "wikilink")/[地上デジタルテレビ放送](../Page/地上デジタルテレビ放送.md "wikilink")に1回だけコピー可能な「[コピーワンス](../Page/コピー・ワンス.md "wikilink")」というコピー制御信号が加えられ、デジタル放送番組のデジタル録画をするためにはCPRMなどのコピー制御に対応しているレコーダーと録画用メディアが必要となった。コピーワンスのデジタル放送をCPRM方式デジタル録画した場合、CPRM対応のプレーヤーやパソコンであれば再生できるが、CPRM非対応のプレーヤーやパソコンでは再生できない。ただし、[DVD-RW](https://ja.wikipedia.org/wiki/DVD-RW "wikilink")、[DVD-RAM](../Page/DVD-RAM.md "wikilink")に関しては、プレーヤーが対応してかつ[VRモードで録画したものであればDVD](../Page/DVD-VR.md "wikilink")-Rよりも再生できることがある。

## 仕組み

CPRMは56Bitの[C2を使用している](https://ja.wikipedia.org/wiki/巡回群 "wikilink")。 固有のメディアIDを[BCA（Burst Cutting Area）と呼ばれるライティングソフトで書き込めないDVDの最内周部分領域に書き込み](https://ja.wikipedia.org/wiki/バーストカッティングエリア "wikilink")、[映像](https://ja.wikipedia.org/wiki/映像 "wikilink")データは[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")して記録する。[パソコンなどを使ってデータは](../Page/パーソナルコンピュータ.md "wikilink")[コピー](../Page/コピー.md "wikilink")できても、メディアIDを書き換えられないので復号できず、映像などを見ることは出来ない。この方式により録画されたメディアを再生する場合、たとえDVD-R・DVD-RW・DVD-RAM・DVD-R DLなどへの再生対応を謳っていてもその[再生機器](https://ja.wikipedia.org/wiki/再生機器 "wikilink")がCPRMに対応（データ復号を許されている、デバイスキーを機器が持っている）していなければ見ることが出来ない。CPRMに対応したAV機器は近年機種が増えているが、旧型の製品や日本独自の規格の為、海外メーカー製DVDプレーヤーなどではCPRMに非対応の製品が殆ど。（ただし、[2011年](../Page/2011年.md "wikilink")（平成23年）現在は殆ど対応している。ただし海外[ブルーレイディスク](https://ja.wikipedia.org/wiki/ブルーレイディスク "wikilink")プレーヤーの場合CPRMには対応していても地上デジタルなどを録画したBD-R/REなどの再生は不可能という機種も多い。）また、CPRMに対応したパソコンソフトによるメディア鑑賞の場合はインターネットを経由しての認証が必要になる。再生時はこのメディアIDと別のMKB（Media Key Block）によって作られる暗号鍵とAV機器の持つデバイスキーで復号が行われるが、万一暗号鍵が破られてもメディア側のMKBデータを更新してしまえば、そのメディアの復号が行えなくなり映像を見ることが出来なくなる。

## 弱点

CPRMのメディアをCPRMに対応したDVDプレーヤーやDVDレコーダーなどで再生する場合、[アナログ](../Page/アナログ.md "wikilink")のビデオ端子からは[CGMS-A](https://ja.wikipedia.org/wiki/CGMS-A "wikilink")として出力されるようになっている。[2007年](../Page/2007年.md "wikilink")（平成19年）[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")現在、家電量販店などのAV機器コーナーでは、[画像安定装置](https://ja.wikipedia.org/wiki/画像安定装置 "wikilink")などと称してCGMS-Aなどのアナログコピーガードが容易に除去出来る装置が公然と販売されており、複製を完全に防止する事は困難だと言われている。したがって、コピー抑止効果としては実質的に「デジタルのままではコピーできないが、アナログに変換すればコピー可能（=[アナログホール](https://ja.wikipedia.org/wiki/アナログホール "wikilink")）」であり、民生用デジタルオーディオ機器に採用されている[SCMS](../Page/SCMS.md "wikilink")によく似ている。

日本の[著作権法](../Page/著作権法.md "wikilink")は[1999年](../Page/1999年.md "wikilink")（平成11年）の改正でその著作物の著作権を有していないにも関わらず、[コピーガード](../Page/コピーガード.md "wikilink")を回避してコピーを作成する事は違法であるとされている。[2012年](../Page/2012年.md "wikilink")（平成24年）の改正で、暗号化を伴う技術的保護手段を回避しての複製は、私的複製の対象外で違法であり、技術的保護手段を回避するプログラム・装置を提供することについても規制され、刑罰の対象となる。

なお、アナログに変換することによる複製を防ぐため、2011年1月1日よりHDでのアナログ出力が禁止され、2014年1月1日より暗号化されたデジタル映像出力端子以外のアナログ映像出力端子が設置された機器の製造および販売が全面禁止されることがAACS Final Adopter Agreementで決定している。

## 対応ソフト

Windows標準搭載のメディアプレーヤーである[Windows Media Playerや](../Page/Windows_Media_Player.md "wikilink")[Windows Media Center](../Page/Windows_Media_Center.md "wikilink")、汎用性の高い[VLCメディアプレーヤー](../Page/VLCメディアプレーヤー.md "wikilink")などの一般的なメディアプレーヤーでCPRMの施されたメディアを再生することは今のところ不可能。ただし、デジタルコンテンツの広がりやPCの普及に伴って、PC上でこれらのコンテンツを再生するソフトウエアが出ている。[Windows上で対応が確認できているソフトとして以下のものが挙げられる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

  - [Corel](https://ja.wikipedia.org/wiki/Corel "wikilink") [WinDVD](../Page/WinDVD.md "wikilink")
  - [CyberLink](https://ja.wikipedia.org/wiki/CyberLink "wikilink") [PowerDVD](../Page/PowerDVD.md "wikilink")
  - [Enjoy DVDおよびEnjoy Blu-ray](../Page/ソースネクスト.md "wikilink")

## 関連項目

  - [著作権法](../Page/著作権法.md "wikilink")
      - [著作権](../Page/著作権.md "wikilink")
  - [コピーガード](../Page/コピーガード.md "wikilink")
  - [コピー・ワンス](../Page/コピー・ワンス.md "wikilink")
  - [Advanced Access Content System](../Page/Advanced_Access_Content_System.md "wikilink")（AACS）
  - [DVD-VR](../Page/DVD-VR.md "wikilink")
  - [SCMS](../Page/SCMS.md "wikilink")
  - [SD-Audio](../Page/SD-Audio.md "wikilink")
  - [SDメモリーカード](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")

## 外部リンク

  - [コピーコントロール「CPRM/CPPM」――その仕組みは?](http://www.itmedia.co.jp/news/0212/13/nj00_cprm.html)

[Category:著作権管理技術](https://ja.wikipedia.org/wiki/Category:著作権管理技術 "wikilink") [Category:DVD](https://ja.wikipedia.org/wiki/Category:DVD "wikilink")