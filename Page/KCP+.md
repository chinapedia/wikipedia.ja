> この記事は[KCP+](https://ja.wikipedia.org/wiki/KCP+)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Iida_G9.jpg "wikilink") [G9](https://ja.wikipedia.org/wiki/G9 "wikilink")（SOX01）\]\]

**KCP+**（ケイ・シー・ピー・プラス）は、**KDDI Common Platform +**（ケイディディアイ・コモン・プラットフォーム・プラス）の略で、[KDDI](../Page/KDDI.md "wikilink")と[クアルコム](https://ja.wikipedia.org/wiki/クアルコム "wikilink")により共同開発された[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")[携帯電話](../Page/携帯電話.md "wikilink")専用の共通[プラットフォームである](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。

クアルコムが[2004年](../Page/2004年.md "wikilink")5月に発表したCPU統合[チップセット](../Page/チップセット.md "wikilink")「MSM7500」（600MHz）に対応しており、KDDI並びに[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")の各au携帯電話の一部機種で利用されている。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の開発は、KDDIテクノロジー\[1\]と[東芝](https://ja.wikipedia.org/wiki/東芝 "wikilink")、[三洋電機](../Page/三洋電機.md "wikilink")が担当した\[2\]。

また、本項ではKCP+の発展版にあたるau携帯電話専用共通プラットフォームの**KCP3.x**（ケイ・シー・ピー さんてんえっくす）についても便宜上記述する。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:Comparison_KCPandKCPplus.svg "wikilink") 従来より[KDDI](../Page/KDDI.md "wikilink")は、端末のソフトウェア開発コストを削減することを目的に、通信キャリアとしては初めて、チップセットのライセンス契約をクアルコムと締結して、開発会社として参加メーカーが出向所属する形式をとり、KDDIとしての独自実装要求部分をすべての参加メーカーに見える形で開発を進めて「[KCP](https://ja.wikipedia.org/wiki/KCP "wikilink")（KDDI Common Platform）」として、クアルコムが開発した携帯電話向けの[チップセット](../Page/チップセット.md "wikilink")を搭載し、携帯電話における基本的なソフトウェアは[BREW](https://ja.wikipedia.org/wiki/BREW "wikilink")（←[REX OS](https://ja.wikipedia.org/wiki/REX_OS "wikilink")）上から拡張した共通プラットフォームを開発した。これにより、統一されたチップセットによる生産コストの低下、各メーカーごとに用意されてきたEメールソフトやEZwebブラウザ、その他サービスアプリなどをBREWアプリとして共通化された。

KCP+では、さらなる携帯電話の高機能化に伴う開発コストの削減を目指すために、共通化の範囲をBREW以外にも拡張し、[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")や無線通信制御、KCP+端末共通のデバイス、さらにはオペレーティングシステムの共通化が図られた。これにより、各メーカーは開発リソースを端末や画面デザイン、独自デバイスなど差別化機能に専念することが可能となるとしている\[3\]。

2008年4月当時、KDDIは、au携帯電話におけるこれからの新サービスは、順次KCP+上に開発していくことを表明していた\[4\]。

2011年春モデルの[SH011](https://ja.wikipedia.org/wiki/SH011 "wikilink")を以ってKCP+を搭載した音声端末の新規開発が終了した。

## KCP3.x

2010年5月にクアルコムのモバイル用プロセッサ「**[Snapdragon S1](https://ja.wikipedia.org/wiki/Snapdragon "wikilink")**」（QSD8650・1GHz）用に最適化された**KCP3.0**が発表され、同キャリア向けの[S004](https://ja.wikipedia.org/wiki/S004 "wikilink")および[T004](https://ja.wikipedia.org/wiki/T004 "wikilink")にそれぞれ搭載された。なお、機能面に関してはKCP+にほぼ準拠しているが基となるプラットフォームがこれまでのBREWから後発の[PT003](https://ja.wikipedia.org/wiki/PT003 "wikilink")に採用されている[Brew MPに変更となった](https://ja.wikipedia.org/wiki/Brew_Mobile_Platform "wikilink")。KCP+での共通化部分に加え、一部のハードウェアも共通化されている\[5\]。

また、2010年秋冬モデルの一部と2011年春モデルのWIN HIGH SPEED対応機種には**KCP3.1**が導入され、更に2011年夏モデル以降のWIN HIGH SPEED対応機種には**KCP3.2**が導入された。こちらはクイックアクセスメニューがセルフメニューに置き換わっているほか、モバイルアプリ版のSkype auに対応となった\[6\]。

2014年冬モデルの[MARVERA2 KYY09を以ってKCP](https://ja.wikipedia.org/wiki/MARVERA2_KYY09 "wikilink")+の系譜となるKCP3.xを搭載した音声端末の新規開発が終了した。

## 共通化された機能

KCP+で共通化された機能として以下のものがある。ただし、後でKCP+の標準機能として組み込まれたものもあるため、それ以前に発売された機種では対応していないものもある。

  - [マルチプレイウィンドウ](../Page/マルチタスク.md "wikilink")\[7\]
      - 二つのアプリケーションを同時に表示できる機能も持つ\[8\]。
      - 当初は標準で対応していたが、一部を除く2009年秋冬モデル以降より開発コスト等を削減する理由で2画面同時表示機能を省略している。
  - クイックアクセスメニュー
      - 上記のマルチプレイウィンドウを発展させた機能でユーザーが頻繁に使う機能だけが自動的に登録される。2009年夏モデルの[T002](https://ja.wikipedia.org/wiki/T002 "wikilink")および[biblio](https://ja.wikipedia.org/wiki/biblio "wikilink")で先行採用され、[CA004](https://ja.wikipedia.org/wiki/CA004 "wikilink")および[SH004](https://ja.wikipedia.org/wiki/SH004 "wikilink")を除き、[PLY](https://ja.wikipedia.org/wiki/PLY "wikilink")（[iida](https://ja.wikipedia.org/wiki/iida "wikilink")ブランド）を含む2009年秋冬モデル以降より正式採用となった。なお、クイックアクセスメニューと2画面同時表示機能が搭載された最後の機種は[CA003](https://ja.wikipedia.org/wiki/CA003 "wikilink")である。
  - [EV-DO Rev.Aまたは](https://ja.wikipedia.org/wiki/CDMA2000_1x#Rev.A "wikilink")[EV-DO Rev.A+](https://ja.wikipedia.org/wiki/CDMA2000_1x#Rev.A+（Multicarrier_Rev.A\(MC-Rev.A\)） "wikilink")\[9\]
      - 一部端末は[テレビ電話](https://ja.wikipedia.org/wiki/テレビ電話 "wikilink")機能に対応。
  - [アクロディア](https://ja.wikipedia.org/wiki/アクロディア "wikilink")製の[VIVID UI](https://ja.wikipedia.org/wiki/VIVID_UI "wikilink")\[10\]
  - [シャープ](../Page/シャープ.md "wikilink")開発のLC[フォント](../Page/フォント.md "wikilink")
      - W62T以降の東芝機はUni-Type\[11\]。一部のKCP3.X対応機種ではUni-Typeを選択できることもある。ダウンロードフォント対応。アウトラインフォント。
      - W62SHを除くKCP+対応のシャープ機はLCフォント・[太ゴシック](../Page/ゴシック体.md "wikilink")・[明朝体](../Page/明朝体.md "wikilink")の3種類から選択可能。（うち、太ゴシック・明朝体はアウトラインフォント。）
      - P001はイワタUD丸ゴシック。EZwebのVGA表示は非対応。
      - KCP3.X対応機種はLIM丸ゴシック体。しかし初期のころではLIM新ゴシック体がデフォルトだった。[Android](../Page/Android.md "wikilink")2.3 - 5.1で採用されていた[モトヤ](../Page/モトヤ.md "wikilink")シーダ・モトヤマルベリと同一。ダウンロードフォント対応。アウトラインフォント。
  - [日本語入力システム](../Page/日本語入力システム.md "wikilink")には[ジャストシステム](../Page/ジャストシステム.md "wikilink")の「[ATOK](../Page/ATOK.md "wikilink") for au + APOT」\[12\]
      - ソニー・エリクソン機は2008年冬モデル以前までが「[POBox](../Page/POBox.md "wikilink") Pro + [Advanced Wnn](https://ja.wikipedia.org/wiki/Wnn "wikilink")」、2009年春モデル以降より「POBox Pro 3.0E + [iWnn](https://ja.wikipedia.org/wiki/Wnn "wikilink")」あるいはそれ以降（搭載バージョンの詳細については当該記事を参照）。
      - シャープ機はW62SHのみ「[ケータイShoin](https://ja.wikipedia.org/wiki/FSKAREN "wikilink")6」、W64SH、SH001、E05SH、E06SH、SH004が「ケータイShoin7」、Sportio water beat、SH002が「ケータイShoin8」、SH003、SH005、SH006、SH007、SH008が「ケータイShoin9」。
      - SH009以降のシャープ機は「iWnn」。
  - [LISMO Port](https://ja.wikipedia.org/wiki/LISMO_Port "wikilink")\[13\]や[LISMO Videoへの対応](https://ja.wikipedia.org/wiki/LISMO_Video "wikilink")\[14\]
      - 法人専用端末（E00番台）は除く。
  - 「[着うたフルプラス](https://ja.wikipedia.org/wiki/着うたフルプラス "wikilink")」対応\[15\]
      - [AAC](../Page/AAC.md "wikilink")-LC・320kbps（最大[ビットレート](https://ja.wikipedia.org/wiki/ビットレート "wikilink")時）のオーディオ[コーデック](../Page/コーデック.md "wikilink")を用いる。法人専用端末（[E05SH](https://ja.wikipedia.org/wiki/E05SH "wikilink")・[E06SH](https://ja.wikipedia.org/wiki/E06SH "wikilink")）\[16\]と[CA002](https://ja.wikipedia.org/wiki/CA002 "wikilink")、[CA004](https://ja.wikipedia.org/wiki/CA004 "wikilink")を除く[W65T](https://ja.wikipedia.org/wiki/W65T "wikilink")、[Walkman Phone, Xmini (W65S)の](https://ja.wikipedia.org/wiki/Xmini "wikilink")2機種を含む2009年春モデル以降のKCP+対応機種より標準で対応。
  - EZアプリ「**[Full Game\!](https://ja.wikipedia.org/wiki/Full_Game! "wikilink")**（フル・ゲーム\!）」対応\[17\]
      - BREW4.0を基本に1アプリあたりの最大ファイル容量は既存の[EZアプリ(BREW)の](https://ja.wikipedia.org/wiki/BREW "wikilink")1アプリあたりの最大ファイル容量の約10倍の容量となった。また、従来の10倍以上のスピードで3D描画が可能。
  - 待ち受け画面への[ウィジェット](https://ja.wikipedia.org/wiki/ウィジェット "wikilink")（au oneガジェット）機能\[18\]
      - 当初は標準で対応していたが先述のマルチプレイウィンドウ機能同様、CA004およびSH004を除き、2009年夏モデルのT002およびbiblio、PLYを含む2009年秋冬モデル以降より開発コスト等を削減する理由でこの機能を省略した機種が登場している。\[19\]
  - 圧縮で発生する音のゆがみを補正し、原音に近づける高音質再現ポストデコードエンジン「**net K2**」の搭載\[20\]\[21\]
      - W56TおよびW54S、W54SA、E05SH、E06SHを除く2008年春モデル以降のKCP+対応機種より標準搭載。
  - EZwebブラウザ（Myriad Browser V7 (旧称：Purple Labs Mobile Browser ← [Openwave](https://ja.wikipedia.org/wiki/オープンウェーブ "wikilink") Mobile Browser)）
      - 操作の統一 （上下キーで1行スクロール・左右キーで1画面スクロール・メールキー/EZキーでページの戻る/進む）

## 問題点

最初期のKCP+採用端末は、キー操作時におけるレスポンスの低下\[22\]や、操作中の予期せぬ[フリーズ](../Page/フリーズ.md "wikilink")やリセット現象の発生など、携帯電話の基本的な性能さえ不安定であるという問題が指摘された\[23\]。既存のKCP+端末に対しても何度も不具合修正のアップデートが行われた。

KCP+端末同士では、端末メーカーの独自性を排除して、どの設定がどこの階層にあるのかなどといった[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")の統合が図られている。この副次的な影響により、それまでのKCPやさらに以前の端末などでメーカーが独自に改良した機能がある場合、統合・共通化により利便性が低下する、といったことがありうる。例えば東芝製のKCP端末では、Eメールにおいて送信先のメールアドレスを選択する際、それぞれアドレスにチェックマークをつけて一括選択する方式に対して、KCP+端末では、ひとつずつアドレスを選択していくというシステムがとられているため、メールアドレスの変更を知らせる時など、全員にメールを送信する際に効率性が低下してしまう、などである。

しかし、新しい技術が導入された黎明期や統合により起こりうる一時的な混乱と位置づけられ、現行機種での不具合の収束よりは、より新しい機種での改良、と形でキャリア側も誘導を図り、次第に事態は落ち着いた。

2009年春モデル以前の機種では[microSDHCメモリーカード](https://ja.wikipedia.org/wiki/SDメモリーカード#SDHCメモリーカード "wikilink")、タッチパネル等のインターフェイスにKCP+側のシステムが対応しておらず\[24\]、共通機能をメーカー間に水平展開するという開発手法におけるデメリットもまだ残されていたが、これらの問題は同年夏モデル以降の一部機種より順次解消されていった\[25\]。

KCP+内の[PCサイトビューアー](https://ja.wikipedia.org/wiki/フルブラウザ "wikilink")([Opera Mobile](https://ja.wikipedia.org/wiki/Opera_Mobile "wikilink"))には[Digest認証](https://ja.wikipedia.org/wiki/Digest認証 "wikilink")が行えないバグがあり、[Apache HTTP Serverに](../Page/Apache_HTTP_Server.md "wikilink")[パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")が投稿されている\[26\]。

## 採用端末

[2018年](../Page/2018年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")現在、以下の端末がKCP+、またはKCP3.xを採用している。

  - ◇は法人向けKCP+搭載機種
  - ★はKCP3.0・[Snapdragon S1](https://ja.wikipedia.org/wiki/Snapdragon "wikilink")（QSD8650・1GHz）搭載機種
  - ☆はKCP3.1・Snapdragon S1（QSD8650・1GHz）・WIN HIGH SPEED（EV-DO MC-Rev.A(EV-DO MC)）搭載機種
  - ◎はKCP3.2・Snapdragon S1（QSD8650・1GHz）・WIN HIGH SPEED（EV-DO MC-Rev.A(EV-DO MC)）搭載機種

<table>
<thead>
<tr class="header">
<th><p>メーカー</p></th>
<th><p>採用端末</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/カシオ計算機.md" title="wikilink">カシオ計算機</a><br />
（CA）</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/W62CA" title="wikilink">W62CA</a>、<a href="https://ja.wikipedia.org/wiki/W63CA" title="wikilink">W63CA</a>、<a href="https://ja.wikipedia.org/wiki/CA001" title="wikilink">CA001</a>、<a href="https://ja.wikipedia.org/wiki/CA002" title="wikilink">CA002</a>、<a href="https://ja.wikipedia.org/wiki/CA003" title="wikilink">CA003</a>、<a href="https://ja.wikipedia.org/wiki/CA004" title="wikilink">CA004</a>、<a href="https://ja.wikipedia.org/wiki/CA005" title="wikilink">CA005</a>、<a href="https://ja.wikipedia.org/wiki/CA006" title="wikilink">CA006</a>、<a href="https://ja.wikipedia.org/wiki/G&#39;zOne_TYPE-X" title="wikilink">G'zOne TYPE-X</a>(CAY01)、◎<a href="https://ja.wikipedia.org/wiki/CA007" title="wikilink">CA007</a></p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/日立製作所.md" title="wikilink">日立製作所</a>／<br />
<a href="https://ja.wikipedia.org/wiki/日立コンシューマエレクトロニクス" title="wikilink">日立CE</a><br />
（H(HI)）</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/W62H" title="wikilink">W62H</a>、<a href="https://ja.wikipedia.org/wiki/W63H" title="wikilink">W63H</a>、<a href="https://ja.wikipedia.org/wiki/H001" title="wikilink">H001</a>(HI001)、<a href="https://ja.wikipedia.org/wiki/Mobile_Hi-Vision_CAM_Wooo" title="wikilink">Mobile Hi-Vision CAM Wooo</a>(HIY01)、<a href="https://ja.wikipedia.org/wiki/beskey" title="wikilink">beskey</a>(HIY02)</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/三洋電機.md" title="wikilink">三洋電機</a>／<br />
京セラSANYOブランド<br />
（SA）</p></td>
<td><p><a href="../Page/W54SA.md" title="wikilink">W54SA</a>、<a href="https://ja.wikipedia.org/wiki/W61SA" title="wikilink">W61SA</a>、<a href="https://ja.wikipedia.org/wiki/W63SA" title="wikilink">W63SA</a>、<a href="https://ja.wikipedia.org/wiki/W64SA" title="wikilink">W64SA</a>、<a href="https://ja.wikipedia.org/wiki/SA001" title="wikilink">SA001</a>、<a href="https://ja.wikipedia.org/wiki/SA002" title="wikilink">SA002</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/パナソニック_モバイルコミュニケーションズ" title="wikilink">パナソニック</a><br />
（P(MA)）</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/P001" title="wikilink">P001</a>(MA001)</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/京セラ.md" title="wikilink">京セラ</a>（K(KY)）</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/K007" title="wikilink">K007</a>(KY007)、◎<a href="https://ja.wikipedia.org/wiki/K009" title="wikilink">K009</a>(KY009)、◎<a href="https://ja.wikipedia.org/wiki/K011" title="wikilink">K011</a>(KY011)、◎<a href="https://ja.wikipedia.org/wiki/MARVERA_KYY08" title="wikilink">MARVERA KYY08</a>、◎<a href="https://ja.wikipedia.org/wiki/MARVERA2_KYY09" title="wikilink">MARVERA2 KYY09</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/ソニーモバイルコミュニケーションズ" title="wikilink">ソニーモバイル</a>[27]<br />
（S(SO)）</p></td>
<td><p><a href="../Page/W54S.md" title="wikilink">W54S</a>、<a href="../Page/W61S.md" title="wikilink">W61S</a>、<a href="https://ja.wikipedia.org/wiki/フルチェンケータイ_re" title="wikilink">フルチェンケータイ re</a>(W63S)、<a href="https://ja.wikipedia.org/wiki/Xmini" title="wikilink">Walkman Phone, Xmini</a>(W65S)<br />
<a href="https://ja.wikipedia.org/wiki/S001" title="wikilink">S001</a>(SO001)、<a href="https://ja.wikipedia.org/wiki/Premier3" title="wikilink">Walkman Phone, Premier<sup>3</sup></a>(SOY01)、<a href="https://ja.wikipedia.org/wiki/G9" title="wikilink">G9</a>(SOX01)、<a href="https://ja.wikipedia.org/wiki/U1_(携帯電話)" title="wikilink">BRAVIA Phone U1</a>(SOY02)、<a href="https://ja.wikipedia.org/wiki/URBANO_BARONE" title="wikilink">URBANO BARONE</a>(SOY03)、<a href="https://ja.wikipedia.org/wiki/S003" title="wikilink">S003</a>(SO003)、★<a href="https://ja.wikipedia.org/wiki/S004" title="wikilink">S004</a>(SO004)、☆<a href="https://ja.wikipedia.org/wiki/S005" title="wikilink">S005</a>(SO005)、☆<a href="https://ja.wikipedia.org/wiki/S006" title="wikilink">S006</a>(SO006)、<a href="https://ja.wikipedia.org/wiki/URBANO_MOND" title="wikilink">URBANO MOND</a>(SOY04)、☆<a href="https://ja.wikipedia.org/wiki/G11" title="wikilink">G11</a>(SOX02)、◎<a href="https://ja.wikipedia.org/wiki/S007" title="wikilink">S007</a>(SO007)、◎<a href="https://ja.wikipedia.org/wiki/URBANO_AFFARE" title="wikilink">URBANO AFFARE</a>(SOY05)</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/シャープ.md" title="wikilink">シャープ</a><br />
（SH）</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/W62SH" title="wikilink">W62SH</a>、<a href="https://ja.wikipedia.org/wiki/W64SH" title="wikilink">W64SH</a><br />
<a href="https://ja.wikipedia.org/wiki/SH001" title="wikilink">SH001</a>、<a href="https://ja.wikipedia.org/wiki/SH002" title="wikilink">SH002</a>、<a href="https://ja.wikipedia.org/wiki/Sportio_water_beat" title="wikilink">Sportio water beat</a>(SHY01)、◇<a href="https://ja.wikipedia.org/wiki/E05SH" title="wikilink">E05SH</a>、◇<a href="https://ja.wikipedia.org/wiki/E06SH" title="wikilink">E06SH</a>、<a href="https://ja.wikipedia.org/wiki/SH003" title="wikilink">SH003</a>、<a href="https://ja.wikipedia.org/wiki/SH004" title="wikilink">SH004</a>、<a href="https://ja.wikipedia.org/wiki/SH005" title="wikilink">SH005</a>、<a href="https://ja.wikipedia.org/wiki/SH006" title="wikilink">SH006</a>、<a href="https://ja.wikipedia.org/wiki/SH007" title="wikilink">SH007</a>、<a href="https://ja.wikipedia.org/wiki/SH008" title="wikilink">SH008</a>、<a href="https://ja.wikipedia.org/wiki/SH009" title="wikilink">SH009</a>、<a href="https://ja.wikipedia.org/wiki/SH010" title="wikilink">SH010</a>、<a href="https://ja.wikipedia.org/wiki/SH011" title="wikilink">SH011</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/東芝" title="wikilink">東芝</a>／<br />
<a href="https://ja.wikipedia.org/wiki/富士通モバイルコミュニケーションズ" title="wikilink">富士通モバイルTOSHIBAブランド</a><br />
（T(TS)）</p></td>
<td><p><a href="../Page/W56T.md" title="wikilink">W56T</a>、<a href="https://ja.wikipedia.org/wiki/W61T" title="wikilink">W61T</a>、<a href="https://ja.wikipedia.org/wiki/W62T" title="wikilink">W62T</a>、<a href="https://ja.wikipedia.org/wiki/Sportio" title="wikilink">Sportio</a>、<a href="https://ja.wikipedia.org/wiki/W64T" title="wikilink">W64T</a>、<a href="https://ja.wikipedia.org/wiki/W65T" title="wikilink">W65T</a><br />
<a href="https://ja.wikipedia.org/wiki/T001" title="wikilink">T001</a>(TS001)、<a href="https://ja.wikipedia.org/wiki/T002" title="wikilink">T002</a>(TS002)、<a href="https://ja.wikipedia.org/wiki/biblio" title="wikilink">biblio</a>(TSY01)<br />
ドッツ・オブセッション、水玉で幸福いっぱい(TSX01) / 宇宙へ行くときのハンドバック(TSX02) / 私の犬のリンリン(TSX03)、<br />
<a href="https://ja.wikipedia.org/wiki/PLY" title="wikilink">PLY</a>(TSX04)、<a href="https://ja.wikipedia.org/wiki/T003" title="wikilink">T003</a>(TS003)、◇<a href="https://ja.wikipedia.org/wiki/E08T" title="wikilink">E08T</a>、★<a href="https://ja.wikipedia.org/wiki/T004" title="wikilink">REGZA Phone T004</a>(TS004)、<a href="https://ja.wikipedia.org/wiki/LIGHT_POOL" title="wikilink">LIGHT POOL</a>(TSX05)、<a href="https://ja.wikipedia.org/wiki/T005" title="wikilink">T005</a>(TS005)、☆<a href="https://ja.wikipedia.org/wiki/X-RAY_(携帯電話)" title="wikilink">X-RAY</a>(TSX06)、☆<a href="https://ja.wikipedia.org/wiki/T006" title="wikilink">T006</a>(TS006)、◎<a href="https://ja.wikipedia.org/wiki/T007" title="wikilink">T007</a>(TS007)、◎<a href="https://ja.wikipedia.org/wiki/T008" title="wikilink">T008</a>(TS008)</p></td>
</tr>
<tr class="odd">
<td><p>富士通モバイル<a href="../Page/富士通.md" title="wikilink">Fujitsuブランド</a><br />
（F(FJ)）</p></td>
<td><p>◇<a href="https://ja.wikipedia.org/wiki/E09F" title="wikilink">E09F</a>、◎<a href="https://ja.wikipedia.org/wiki/F001" title="wikilink">F001</a>(FJ001)</p></td>
</tr>
</tbody>
</table>

## 周辺機器

  - [au BOX](https://ja.wikipedia.org/wiki/au_BOX "wikilink")　パソコンがなくてもテレビがあれば、法人向け専用のE05SHとE06SHを除くKCP+採用の携帯電話に曲を転送する機能がある。

## 脚注

## 関連項目

  - [au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")
  - [KCP](https://ja.wikipedia.org/wiki/KCP "wikilink") - KDDIと米・クアルコムが共同開発したau携帯電話専用プラットフォーム、BREWを元に独自拡張した
  - [MOAP](../Page/MOAP.md "wikilink") - [NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")が中心となり開発した携帯電話用共通プラットフォーム
  - [オペレータパック](https://ja.wikipedia.org/wiki/オペレータパック "wikilink") - NTTドコモが[アクセスと共同開発した共通プラットフォーム](https://ja.wikipedia.org/wiki/ACCESS_\(企業\) "wikilink")、MOAPに代わって搭載されている
  - [Brew Mobile Platform（Brew MP）](https://ja.wikipedia.org/wiki/Brew_Mobile_Platform "wikilink") - 米・クアルコムが開発した[途上国](https://ja.wikipedia.org/wiki/途上国 "wikilink")・[新興国](https://ja.wikipedia.org/wiki/新興国 "wikilink")向け[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")対応モバイルプラットフォーム、KCP3.xの母体にもなっており、更に2012年夏モデルのau携帯電話「[PT003](https://ja.wikipedia.org/wiki/PT003 "wikilink")」に搭載されている

## 外部リンク

  - [au](http://www.au.kddi.com/)

[Category:携帯電話端末_(au_第三世代)](https://ja.wikipedia.org/wiki/Category:携帯電話端末_\(au_第三世代\) "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11. [LIM : 製品紹介 : Uni-Type受賞・メディア掲載・導入事例](http://www.lim.co.jp/products/media.html)
12.
13.
14.
15.
16. ただし[E08T](https://ja.wikipedia.org/wiki/E08T "wikilink")と[E09F](https://ja.wikipedia.org/wiki/E09F "wikilink")は例外として着うたフルおよび着うたフルプラスに対応している。
17.
18.
19. [「ふぉーんなハナシ・au秋冬モデルでさり気なく消えた（？）サービス」](http://plusd.itmedia.co.jp/mobile/articles/0910/20/news020.html) - [ITmedia](https://ja.wikipedia.org/wiki/ITmedia "wikilink") +Dモバイル(2009-10-20).[2009年](../Page/2009年.md "wikilink")[10月20日](../Page/10月20日.md "wikilink")閲覧。
20. [『ビクターの高音質化技術「net K2」がau携帯電話に採用』](http://www3.jvckenwood.com/press/2008/netk2-au.html) - [JVCケンウッド](https://ja.wikipedia.org/wiki/JVCケンウッド "wikilink")
21. [「net K2」](http://www.jvcmusic.co.jp/k2technology/netk2/index.html) - [JVCケンウッド・ビクターエンタテインメント](https://ja.wikipedia.org/wiki/JVCケンウッド・ビクターエンタテインメント "wikilink")（具体的な詳細については「K2 Post処理」の項を参照）
22.
23.
24.
25.
26.
27. 旧 [ソニー・エリクソン・モバイルコミュニケーションズ](https://ja.wikipedia.org/wiki/ソニー・エリクソン・モバイルコミュニケーションズ "wikilink")