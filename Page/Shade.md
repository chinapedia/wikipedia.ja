> この記事は[Shade](https://ja.wikipedia.org/wiki/Shade)から翻訳されています。


**Shade 3D**（シェード スリーディー）は、[フォーラムエイト](https://ja.wikipedia.org/wiki/フォーラムエイト "wikilink")が開発する[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")および[Windows用の統合型](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[3DCGソフトウェア](https://ja.wikipedia.org/wiki/3DCGソフトウェア "wikilink")。

かつては[エクス・ツールス](https://ja.wikipedia.org/wiki/エクス・ツールス "wikilink")（2003年まで）、[イーフロンティア](../Page/イーフロンティア.md "wikilink")（2013年まで）、Shade3D社（2018年まで）で開発された。

## 特徴

1986年の製品化以来30年以上の歴史を持つ。特に専門分野は設定されていない[オールインワン](../Page/オールインワン.md "wikilink")ソフトウェアであるが、しばしば建築パース制作、[イラストレーション](../Page/イラストレーション.md "wikilink")制作、教育機関での導入事例が取り上げられる。2004年時点でユーザ数は30万人超であり、そのほとんどが日本市場におけるものであった\[1\]。2014年10月、イーフロンティアはアクティブユーザー数が19万人居ると発表した\[2\]。

姉妹ソフトウェアとして3D住宅デザインソフト『Shade ドリームハウス』（Shade Home Designから改称）、ならびに『[機動戦士ガンダム](../Page/機動戦士ガンダム.md "wikilink")』を題材にした『ガンダムバーチャルモデラー プロ』（発売元は[バンダイ](../Page/バンダイ.md "wikilink")）が存在する。Shade ドリームハウスはShadeのような統合型3DCGソフトウェアではなく、Windows版のみであるが、互換性のあるファイルをやりとりできる。バーチャルモデラーはデフォルトで用意されているメカニックモデルにポーズを付けて1枚のCGを作るもので、形状の変更や新規作成の機能は省略されていたが、データに互換性があるためShadeでも扱うことが可能であった。

### モデリングの特徴

[竹ひご](https://ja.wikipedia.org/wiki/竹ひご "wikilink")細工のように3次元空間上で複数の[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")を接続して[モデリング](https://ja.wikipedia.org/wiki/モデリング "wikilink")する「[自由曲面](https://ja.wikipedia.org/wiki/自由曲面 "wikilink")」と呼ばれるモデリング方法が特徴的である。自由曲面は多様な[曲率](../Page/曲率.md "wikilink")の滑らかな[曲面](../Page/曲面.md "wikilink")を少ないコントロールポイントで作成できるため、機械や建築物といった幾何学的形状のモデリングに適しており、またベジェ曲線がベースであるため、[Illustratorなどの](../Page/Adobe_Illustrator.md "wikilink")[ドローソフト](../Page/ドローソフト.md "wikilink")に慣れた人にとっては親しみやすい。その一方で、自由曲面はベジェ曲線への慣れが必要であり、多くの[スプライン曲面](https://ja.wikipedia.org/wiki/スプライン曲面 "wikilink")と同様にメッシュ構造が格子状に限定され、また人体のような有機的形状のモデリングにおいて、ベジェ曲線の接線ハンドル同士が干渉してしわが発生しやすい短所がある。

過去にはこのような有機的形状での問題に対処する方法は少なかったが、バージョンを重ねるにつれ、[メタボール](../Page/メタボール.md "wikilink")や[ポリゴン](../Page/ポリゴン.md "wikilink")メッシュの[サブディビジョンサーフェス](https://ja.wikipedia.org/wiki/サブディビジョンサーフェス "wikilink")（細分割曲面）や面の押し出しなどの機能が強化され、幾何学的形状には自由曲面、有機的形状にはポリゴンメッシュやメタボールといった使い分けができるようになっている。

また、Ver.17からはNURBSモデリング機能が搭載され、3DCADのようなモデリングが可能になっている。

### レンダリングの特徴

グレードによって[レンダリング可能な最大サイズが制限されているものの](../Page/レンダリング_\(コンピュータ\).md "wikilink")、廉価な下位グレードでも[パストレーシング](https://ja.wikipedia.org/wiki/パストレーシング "wikilink")や[フォトンマッピング](https://ja.wikipedia.org/wiki/フォトンマッピング "wikilink")、[ラジオシティ](../Page/ラジオシティ.md "wikilink")といった写実的な照明計算を行う[大域照明に対応している](https://ja.wikipedia.org/wiki/グローバルイルミネーション "wikilink")。開発元イーフロンティアの[園田浩二](https://ja.wikipedia.org/wiki/園田浩二 "wikilink")によれば、Shadeは従来より静止画制作での利用が主であるため、標準設定で高品質なレンダリング結果を得られるよう調整されていた\[3\]。高画質志向の代償として時間がかかる傾向があったが、Shade 9以降では計算を間引いて高速化するイラディアンスキャッシュ機能を搭載、バージョンごとに最適化が重ねられている\[4\]。

[トゥーンレンダリング](../Page/トゥーンレンダリング.md "wikilink")や[立体視](../Page/立体視.md "wikilink")、[ビューカメラ](https://ja.wikipedia.org/wiki/ビューカメラ "wikilink")のような光軸調整による[あおり補正といった特殊なレンダリングにも対応する](../Page/あおり_\(写真\).md "wikilink")。

## 歴史

### 開発の歴史

Shadeシリーズが初めて製品化されたのは1986年に発売された[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用の『Shade PRO』である。1990年に改めてMacintosh用のソフトウェアとして『Shade III』が発売された後、1997年の機能限定版『Shade debut（シェード・デビュ）』を皮切りにWindows版が発売され、現在ではMacintosh版・Windows版が同時リリースされている。一時期[Linux](../Page/Linux.md "wikilink")版の開発も試験的に行われていたが、中止された。

2003年までは、福岡に本社があった[エクス・ツールス](https://ja.wikipedia.org/wiki/エクス・ツールス "wikilink")が開発・販売を行っていたが、同社が経営破綻したため、権利を譲渡された[イーフロンティア](../Page/イーフロンティア.md "wikilink")が開発・販売を継いだ。開発会社変更後の最初のメジャーバージョンアップとなったShade 7では、予定されていた新機能の搭載がいくつか見送られ、Shade 6に存在した機能が削減されたこともあった\[5\]。2003年にイーフロンティアは3D人体制作ソフトウェア『[Poser](../Page/Poser.md "wikilink")』の開発・発売を手がける米Curious Labs Inc.（現e frontier America Inc.）を買収し、PoserとShadeとのソフトウェア上での連携（PoserFusion）を実現すると共に、Shadeの日本国外での発売元としたが、2007年にPoserの所有権は米Smith Micro Softwareに譲渡された\[6\]。また、2006年にイーフロンティアは仏Eovia Europeのモデリングソフトウェア『[Amapi](https://ja.wikipedia.org/wiki/Amapi "wikilink")』を買収し、AmapiとShadeの連携を図ると発表したが、この計画は事実上頓挫した。2008年には建築CADメーカー10社と共同で、Shadeの技術を基にした部品データ向けのSPEEDフォーマットを発表。2009年には米Mirye Softwareから英語版Shadeの全世界販売を開始した。

初期の開発はほぼ[時枝敏也](https://ja.wikipedia.org/wiki/時枝敏也 "wikilink")1人によって行われた\[7\]。開発会社の変更や、チーム開発体制へ移行した後も、時枝はエグゼクティブチーフプログラマ、チーフエンジニアとしてShadeの開発や設計に携わっている。なお、時枝とイーフロンティア[最高技術責任者](../Page/最高技術責任者.md "wikilink")の[サニー・ウォン](https://ja.wikipedia.org/wiki/サニー・ウォン "wikilink")（Sunny Wong）は米国で開発を行っているため、過去にしばしば言われた「Shadeは純日本製」という表現は（開発会社は日本にあり、日本でも開発が行われているものの）厳密には正確ではない\[8\]。また、「Shadeの神様」という異名を持つ人物として[園田浩二](https://ja.wikipedia.org/wiki/園田浩二 "wikilink")がおり、Shadeでテレビコマーシャルなどの作品を制作し、イーフロンティアのチーフデザイナ、Shadeの[エバンジェリスト](https://ja.wikipedia.org/wiki/エバンジェリスト "wikilink")としてデモンストレーションなどの広報に携わっている\[9\]。Shadeの開発コンセプトには「箸のようなソフト」「簡単きれい」などがあり、2006年にはこれらの設計思想を主張してShade 8.5が[グッドデザイン賞](https://ja.wikipedia.org/wiki/グッドデザイン賞 "wikilink")（商品デザイン部門）を受賞した\[10\]。

イーフロンティアは2010年代に入り経営が悪化し、Shadeの開発販売権は大手[ビットコイン](https://ja.wikipedia.org/wiki/ビットコイン "wikilink")取引所[マウントゴックス](https://ja.wikipedia.org/wiki/マウントゴックス "wikilink")の経営者[マルク・カルプレス](https://ja.wikipedia.org/wiki/マルク・カルプレス "wikilink")が2013年に設立した株式会社Shade3Dに売却され\[11\]\[12\]、主要開発者も移籍して開発を継続し、イーフロンティア・米Mirye共に販売代理店契約を結ぶ形となった\[13\]。2014年9月にエクス・ツールス時代から経営に関わる笹渕正直が代表に就任した。その後2014年11月をもってイーフロンティア・米Miryeとの販売代理店契約は解除され、Shade3D社が直接販売する形になった\[14\]\[15\]。この件により資金繰りの悪化したイーフロンティアは同年12月に[民事再生法](../Page/民事再生法.md "wikilink")の適用を申請する\[16\]。

関係会社のマウントゴックスがビットコイン消失事件を起こし、2014年4月に[破産](../Page/破産.md "wikilink")したことから、Shade3D社は約3億円の貸付金の返済要求を負い\[17\]、親会社ティバンは約8億円の貸付金を返済できず2015年1月に破産\[18\]、カルプレスはShade3D社の事業買収に充てた約3億円の貸付金ほかを顧客預かり金から流用した[業務上横領](https://ja.wikipedia.org/wiki/業務上横領 "wikilink")容疑などで、2015年8月に逮捕\[19\]\[20\]、翌月起訴された\[21\]（2019年に横領容疑は無罪確定\[22\]）。Shade3D社は一連の事件によって信用不安に見舞われたが、2015年9月に[投資ファンド](../Page/投資ファンド.md "wikilink")運営のニューホライズンキャピタルから再建計画が発表され、ティバンとマウントゴックス側からShade3D社関連のすべての債権と株式が買い取られた\[23\]\[24\]\[25\]。

2018年8月にニューホライズンキャピタル社からフォーラムエイト社に全株式が譲渡され、フォーラムエイト社はShade3D社を完全子会社とした\[26\]。2019年1月にフォーラムエイトはShade3D社を吸収合併した\[27\]。

### ユーザの歴史

漫画家[くつぎけんいち](https://ja.wikipedia.org/wiki/くつぎけんいち "wikilink")が美少女CGキャラクタ（いわゆる[バーチャルアイドル](../Page/バーチャルアイドル.md "wikilink")）『[テライユキ](../Page/テライユキ.md "wikilink")』の制作にShadeを使用した。テライユキはテレビコマーシャルに出演するなど一般メディアに露出し、Shadeの広告にも起用された。1990年代末頃に端を発するバーチャルアイドルブームにより、多くのバーチャルアイドルがShadeを使用して制作され、当時の開発元のエクス・ツールス自身も「デジタルビューティ」としてこれらのキャラクタを後押しし、[ブルームーンスタジオ](https://ja.wikipedia.org/wiki/ブルームーンスタジオ "wikilink")の[沖孝智](https://ja.wikipedia.org/wiki/沖孝智 "wikilink")によるCGキャラクタ『[飛飛](https://ja.wikipedia.org/wiki/飛飛 "wikilink")（FeiFei、フェイフェイ）』が日本[サムスン](https://ja.wikipedia.org/wiki/サムスン "wikilink")の広告キャンペーンに起用されるなど、いくつかのキャラクタがコンピュータ・CG系の専門誌やテレビ・雑誌などの一般メディアに露出した\[28\]。ただし、Shadeは動画向きのソフトではなかったことから、テライユキや飛飛は、動画での活動を行う際に他のソフトへ移行している\[29\]。また、SFイラストレーターの[加藤直之](../Page/加藤直之.md "wikilink")もShadeを使用しており、『[宇宙の戦士](../Page/宇宙の戦士.md "wikilink")』の[パワードスーツ](../Page/パワードスーツ.md "wikilink")の模型化の際は自らShadeで形状設計を行ったほか、作品『[沈黙の美女](https://ja.wikipedia.org/wiki/加藤直之#沈黙の美女 "wikilink")』の形状データが一時期Shadeに同梱されていたことがある。また、漫画家では『[コブラ](../Page/コブラ_\(漫画\).md "wikilink")』の[寺沢武一](../Page/寺沢武一.md "wikilink")\[30\]や『[銃夢](../Page/銃夢.md "wikilink")』の[木城ゆきと](../Page/木城ゆきと.md "wikilink")、『[GANTZ](../Page/GANTZ.md "wikilink")』の[奥浩哉](../Page/奥浩哉.md "wikilink")も制作の一部にShadeを導入している\[31\]。

初期のShadeには有機的形状に適したモデリング方法が現在より少なく、自由曲面がもつ格子状の構造で有機的形状、特に人の頭部（顔面）をモデリングするノウハウがいくつか考案され、「地球儀型」「めがね型」「いちょう型」などの手法が書籍やコミュニティで受け伝われている。

## 機能

Shadeは統合型3DCGソフトウェアであり、[3DCG制作のモデリング](../Page/3次元コンピュータグラフィックス.md "wikilink")、材質設定、照明、アニメーション、レンダリングの工程をカバーしている。ただし、素材となる[テクスチャ画像の編集や](../Page/テクスチャマッピング.md "wikilink")、出力された映像の編集・合成には外部のソフトウェアを使う必要がある。

この節に記述された機能はバージョン15を参考にしており、一部はバージョンやグレードによっては未搭載または制限があり、また、この節の記述はすべての機能を網羅するものではないことに注意されたい。

### モデリング

Shadeの[モデリング](https://ja.wikipedia.org/wiki/モデリング "wikilink")には[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")が採用されており、ベジェ曲線の「線形状」から平面／[掃引体](https://ja.wikipedia.org/wiki/掃引体 "wikilink")／[回転体](../Page/回転体.md "wikilink")／[自由曲面](https://ja.wikipedia.org/wiki/自由曲面 "wikilink")を派生的に作成できる。そのほかには円／球といった[プリミティブ](https://ja.wikipedia.org/wiki/プリミティブ "wikilink")や、[ポリゴン](../Page/ポリゴン.md "wikilink")メッシュ、[メタボール](../Page/メタボール.md "wikilink")、[プラグイン](../Page/プラグイン.md "wikilink")機能による特殊属性を持った形状がある。

  - 線形状 - 3次元の3次ベジェ曲線。終端を閉じると同一平面上に面を形成できるほか、他の線形状で形成された同一平面上の面に穴をあけられる
  - 円／球 - パラメータによる位置と寸法の指定が可能なプリミティブ
  - 掃引体／回転体 - 線形状および円に対して適用可能な非破壊式のもの
  - 自由曲面 - 双3次ベジェ[曲面](../Page/曲面.md "wikilink")。曲線を線形状と同じように扱えて、出し入れできる
      - テキスト - テキスト[グリフのアウトライン化と立体化](../Page/字体.md "wikilink")
  - ポリゴンメッシュ - 3角、4角および5角形以上のポリゴン（n-ゴン）に対応
      - 角の丸め（[サブディビジョンサーフェス](https://ja.wikipedia.org/wiki/サブディビジョンサーフェス "wikilink")、細分割曲面） - ポリゴンメッシュを滑らかな曲面に細分割する非破壊式のもの。バージョン10.0.2以降では従来のドゥ・サビン（[Doo-Sabin](https://ja.wikipedia.org/wiki/:en:Doo–Sabin_subdivision_surface "wikilink")）法に加えてカトマル・クラーク（[Catmull-Clark](https://ja.wikipedia.org/wiki/:en:Catmull–Clark_subdivision_surface "wikilink")）法が使用可能\[32\]。バージョン15以降では[ピクサー](https://ja.wikipedia.org/wiki/ピクサー "wikilink")のOpenSubdivを採用し、稜線ごとにエッジの強さを設定可能
      - UVマップ - テクスチャ[UV](https://ja.wikipedia.org/wiki/UV "wikilink")座標の編集
      - [マジカルスケッチ](https://ja.wikipedia.org/wiki/マジカルスケッチ "wikilink") - フリーハンドの手描きにより有機的形状を作成する
      - スケッチモデラー - 2次元画像を元にして左右対称な形状を作成する。類似のものに[六角大王](../Page/六角大王.md "wikilink")がある
      - フォトモデラー - 複数角度から撮影された写真を元に形状を作成する
  - メタボール／メタキューブ／メタシリンダー／メタポリゴン／メタバイリニアサーフェス／メタバイキュービックサーフェス - 各形状をメタ方式またはブロブ方式により融合または反発させ、有機的な形状を作成する
      - メタパーティクルレンダラ - 特定のパートに含まれた球プリミティブをメタボールとして扱う
  - ヘアーサロン - ヘアー（曲面にテクスチャを張ったいわゆる短冊ヘアー）と[ファー](https://ja.wikipedia.org/wiki/ファー "wikilink")の生成。T4社によって開発された\[33\]

ほぼすべての形状とコントロールポイント、[ポリゴン](../Page/ポリゴン.md "wikilink")メッシュの頂点に対して直線移動／拡大縮小／回転／[せん断](https://ja.wikipedia.org/wiki/せん断 "wikilink")の基本操作を統一的に行えるほか、線形状（自由曲面）とポリゴンメッシュにはそれぞれ追加の形状編集機能が用意されている。

また、作成された形状は下の表のルールでほかの形状に変換できる。

<table>
<caption>形状の変換ルール（左が変換元、上が変換先）</caption>
<thead>
<tr class="header">
<th></th>
<th><p>線形状</p></th>
<th><p>掃引体／回転体</p></th>
<th><p>自由曲面</p></th>
<th><p>ポリゴンメッシュ</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>線形状</p></td>
<td><p>-</p></td>
<td><p>○（可逆）</p></td>
<td><p>○（4点選択<a href="http://shade.e-frontier.co.jp/maiko/029/q029.html">1</a>／<br />
曲線の差し込み）</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>円</p></td>
<td><p>○</p></td>
<td><p>○（可逆）</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>球</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>掃引体／回転体</p></td>
<td><p>○（復帰）</p></td>
<td><p>-</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>自由曲面</p></td>
<td><p>○（曲線の取り出し）</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>ポリゴンメッシュ</p></td>
<td><p>○</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>○（細分割曲面）</p></td>
</tr>
</tbody>
</table>

シーン内の全オブジェクトはブラウザによって一覧管理できる。また、オブジェクトは「パート」によって内包・階層化でき、またパートには座標変換のための[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")情報を設定できる。シーンの最下層には常に「ルートパート」と呼ばれるパートが存在する。

また、そのほかのモデリング支援として次のような機能を備えている。

  - ブーリアンレンダリング - レンダリング時のみ適用される非破壊式の[集合演算](https://ja.wikipedia.org/wiki/ブーリアン演算 "wikilink")
  - ブーリアンモデリング - ポリゴンメッシュ形状として出力する集合演算
  - 3Dプリントアシスタント - 対話式で[3Dプリント用データの修正](../Page/3Dプリンター.md "wikilink")・書き出しをする[ウィザード](../Page/ウィザード_\(ソフトウェア\).md "wikilink")
  - マスターオブジェクト - オブジェクトの参照コピー
  - リプリケーター - 線や曲面に沿って形状を複製配置する
  - マグネット - 指定位置付近のコントロールポイント（頂点）を滑らかに追従変形させる
  - ラティス変形／自由曲面変形／ツイスト変形／ケージ変形

Shadeは[サーフェスモデルを基本としつつ](https://ja.wikipedia.org/wiki/サーフェスモデリング "wikilink")、部分的に[ソリッドモデルの概念を取り入れている](https://ja.wikipedia.org/wiki/ソリッドモデリング "wikilink")。Shadeにおいて立体とは「形状表面の内側と外側が一意に定義できる形状\[34\]」とされており、空間を内包する閉じた形状が立体として扱われる。形状が立体として成立するのは暗黙であり何ら手順を要しないが、中身の詰まった形状（ソリッド）として扱うか否かはソリッド属性によって明示的に指定できる。

### 表面材質と光源

Shadeの表面材質は固定の[シェーディング](https://ja.wikipedia.org/wiki/シェーディング "wikilink")パラメータと任意数のマッピングレイヤーの複合である。表面材質はオブジェクトまたはパート、ポリゴンのフェイスグループに対して設定できる。特定部位に特徴的な表面材質を施す場合には、投影マッピングやブーリアンレンダリングによる[ステッカーマッピング](../Page/シール.md "wikilink")（[デカール](../Page/デカール.md "wikilink")マッピングとも呼ばれる）も行える。パートに設定された表面材質は下位階層に継承され、下位階層では任意のシェーディングパラメータを選択的に置き換えられる。

  - [拡散反射](../Page/拡散反射.md "wikilink") - 光を拡散的に反射する、いわゆる表面色、物体色
  - [光沢](../Page/光沢.md "wikilink") - 光源の[鏡面反射](../Page/鏡面反射.md "wikilink")をモデル化した[つや](../Page/鏡面ハイライト.md "wikilink")（局所鏡面反射）。1次光沢および2次光沢がある。Shade 9以降ではブリン（Blinn）鏡面反射モデルが採用されている\[35\]
  - [反射](../Page/反射.md "wikilink") - 周辺の景色が映り込む鏡のような反射（大域鏡面反射）
  - [透明](../Page/透明.md "wikilink") - [透過率](https://ja.wikipedia.org/wiki/透過率 "wikilink")（透過色）を設定する
  - [屈折](../Page/屈折.md "wikilink") - [屈折率](../Page/屈折率.md "wikilink")（相対屈折率\[36\]）を設定する
  - 荒さ - 梨地加工や[磨りガラス](https://ja.wikipedia.org/wiki/磨りガラス "wikilink")のように反射と屈折を拡散させる
  - [異方性反射](https://ja.wikipedia.org/wiki/異方性反射 "wikilink") - 繊維や金属のヘアライン加工でみられる異方性反射を表現する
  - [フレネル](../Page/フレネルの式.md "wikilink") - フレネル反射を表現する。光の入射角が浅くなるほど反射率が高くなり、屈折に伴い自然な反射と透過減衰が発生する
  - メタリック - 内蔵の環境マッピングによる擬似的な[金属光沢](../Page/金属光沢.md "wikilink")表現
  - [発光](../Page/発光.md "wikilink") - 外部照明によらない自発的な発光
      - ソフトグロー - 発光の度合いを視線方向を向いている面ほど強くする
  - バックライト - 裏面の拡散反射を表面に反映させる
  - [サブサーフェイス・スキャタリング](../Page/サブサーフェイス・スキャタリング.md "wikilink") - 肌や蝋、牛乳のような半透明な媒質内部での透過散乱を再現する
  - ボリュームレンダリング - 煙や色ガラスのような媒質の厚みで変化する透過を再現する
  - 疑似[コースティクス](../Page/コースティクス.md "wikilink") - 大域照明によらない擬似的な集光模様（コースティクス）
  - [収差](../Page/収差.md "wikilink") - 波長を考慮した[色収差](../Page/色収差.md "wikilink")と、RGB別に屈折率を変える擬似的な色収差

<!-- end list -->

  - レイヤーによるマッピング - 拡散反射／光沢／反射／透明／発光／バックライトおよび、[バンプ](../Page/バンプマッピング.md "wikilink")／法線／ディスプレイスメント／トリム／環境のマッピング、および上位レイヤーのマット
      - イメージマッピング - 画像またはムービー（[QuickTime](../Page/QuickTime.md "wikilink")／[AVI](https://ja.wikipedia.org/wiki/AVI "wikilink")）によるテクスチャ
      - ソリッドテクスチャ - 内蔵のプロシージャによる投影または3次元のテクスチャ

Shadeの一部の[光源](../Page/光源.md "wikilink")には明るさや色、[影](../Page/影.md "wikilink")の濃度やソフトネス（[ソフトシャドー](https://ja.wikipedia.org/wiki/ソフトシャドー "wikilink")に影響する）、ボリュームライトなどを設定できる。また、パストレーシング大域照明を使用している場合、表面材質の発光が[放射輝度](../Page/放射輝度.md "wikilink")に影響するため、発光する形状および発光テクスチャを副次的な光源として利用できる。

  - 無限遠光源 - [平行光源とも呼ばれる](https://ja.wikipedia.org/wiki/3次元コンピュータグラフィックス#ライティング（照光）\(Lighting\) "wikilink")、[太陽光](../Page/太陽光.md "wikilink")などの極めて遠距離（[無限遠](../Page/無限遠点.md "wikilink")）の光源をモデル化した光源
      - 環境光 - 周辺環境からの一様な散乱光や照り返しをモデル化した、閉塞を考慮しない光源。Shadeでは無限遠光源に付随して設定する。照明効果が一様なため、写実性を求めるならIBLや天空光が適する
  - 点光源／スポットライト - 光源オブジェクトによる光源
  - 線光源／面光源 - 線形状による曲線または面による光源
  - 配光 - IES配光データによる光源
  - [イメージ・ベースド・ライティング](https://ja.wikipedia.org/wiki/イメージ・ベースド・ライティング "wikilink")（IBL） - 背景画像による照明。[ハイダイナミックレンジ画像](../Page/ハイダイナミックレンジイメージ.md "wikilink")（HDRI）に対応。パストレーシング大域照明に用いられる
  - 天空光 - [天球](../Page/天球.md "wikilink")の上半球による照明。ラジオシティ大域照明に用いられる
  - フィジカルスカイ - 時刻や緯度・経度によって太陽方向や空の色合いを自動計算する

### アニメーション

Shadeのアニメーション機能は、[ジョイント](https://ja.wikipedia.org/wiki/ジョイント "wikilink")およびその応用である[ボーン](../Page/ボーン.md "wikilink")、[スキン](https://ja.wikipedia.org/wiki/スキン "wikilink")による変形と、それを時間軸に沿って制御するモーション[シーケンス](https://ja.wikipedia.org/wiki/シーケンス "wikilink")（モーション曲線および[キーフレーム](https://ja.wikipedia.org/wiki/キーフレーム "wikilink")補間）が基本となっている。カメラオブジェクトのモーション制御による[フライスルー](https://ja.wikipedia.org/wiki/フライスルー "wikilink")（[ウォークスルー](../Page/ウォークスルー.md "wikilink")）が行えるほか、音源オブジェクトによる3Dサウンド機能が備えられている。また、テクスチャおよび図形ウインドウのテンプレート（下絵）には、QuickTime／AVIムービーを使用できる。

  - ジョイント - 変形を行うパートの一種。ジョイント値と呼ばれるパラメータにより変形の度合いを調整する
      - 直線移動／回転／拡大縮小／均等拡大縮小ジョイント - 制限付きの平行移動／回転／拡大縮小
      - ボールジョイント - 無制限の平行移動と回転。単一のジョイント値では制御できず、もっぱらキーフレームアニメーションに用いる
      - パスジョイント - 線形状のパス（軌道）に沿った移動
          - パスコンストレインツ - 列車や[キャタピラのような連結された形状の方向制御](../Page/無限軌道.md "wikilink")
      - 変形ジョイント - 複数形状間の形状と表面材質の[モーフィング](../Page/モーフィング.md "wikilink")
      - スイッチジョイント - 複数形状の切り替え
      - 光源ジョイント - 光源の明るさの調整
  - [ボーン](../Page/ボーン.md "wikilink")（[スケルトン](https://ja.wikipedia.org/wiki/スケルトン "wikilink")） - ジョイントの階層化による多関節構造の作成。バージョン13.1以降は他ソフトと互換性の高い新ボーン機能を採用
      - [インバースキネマティクス](https://ja.wikipedia.org/wiki/3次元コンピュータグラフィックス#インバースキネマティクス（逆運動学）\(IK\(inverse_kinematics\)\) "wikilink")（IK） - 子ジョイントの変形に親ジョイントを追従させる
          - スマートキネマティクス - 特定のジョイントの向きや関節角度を拘束する
          - エイムコンストレインツ - 形状の向きをターゲットオブジェクトやカメラに追従させる
  - スキン - コントロールポイント（頂点）単位でジョイントの変形を適用する。適用率（重み付け）の設定やウエイトペイントも可能
  - モーションシーケンス - [タイムコード](https://ja.wikipedia.org/wiki/タイムコード "wikilink")または[フレーム数による時間軸に沿ったモーションシーケンスを扱う](../Page/コマ_\(映画・漫画\).md "wikilink")。モーションポイント（キーフレーム）の作成とモーション曲線の編集が行える
  - 3Dサウンド - シーン内に[音源](../Page/音源.md "wikilink")オブジェクトを配置して[立体音響](../Page/立体音響.md "wikilink")と[ドップラー効果](../Page/ドップラー効果.md "wikilink")を用いた音声を生成する

また、そのほかのアニメーション支援として次のような機能を備えている。

  - モーションエフェクト - 髪やアクセサリーなどの揺れを再現する
  - パーティクルフィジックス - 重力や風を考慮した[パーティクル](https://ja.wikipedia.org/wiki/パーティクル "wikilink")と衝突判定。T4社によって開発された\[37\]
  - PoserFusion - Poserのフィギュア形状とモーションの取り込み。ダイナミックヘアと[クロスシミュレーションが再現される](https://ja.wikipedia.org/wiki/3次元コンピュータグラフィックス#クロス\(Cloth\) "wikilink")

### レンダリング

Shadeは複数のレンダリング手法と[大域照明の手法をサポートしている](../Page/グローバル・イルミネーション.md "wikilink")。レンダリングは各色32ビット（128ビット[RGBA](https://ja.wikipedia.org/wiki/色空間#RGBA "wikilink")）のハイダイナミックレンジ画像を出力でき、レンダリングされた画像からは[RGB](../Page/RGB.md "wikilink")カラーチャンネルおよび不透明度（[αチャンネル](../Page/アルファチャンネル.md "wikilink")）、深度（[Z値](../Page/Zバッファ.md "wikilink")）、法線、形状IDなどの多様な情報を取得できるマルチパスレンダリングに対応する。レンダリングされる画像は内蔵の色補正機能やエフェクタプラグインによる後処理が行える。

また、マルチ[スレッドによる](../Page/スレッド_\(コンピュータ\).md "wikilink")[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")・[マルチコア](../Page/マルチコア.md "wikilink")並列レンダリング、「ShadeGrid」と呼ばれる複数台のコンピュータ[グリッドによる並列レンダリングが可能である](../Page/グリッド・コンピューティング.md "wikilink")。

  - [ワイヤーフレーム](../Page/ワイヤーフレーム.md "wikilink") - 単純な線によるレンダリング
  - ドラフトレイトレーシング - レイトレーシングから屈折などを省いて高速化したもの
  - [レイトレーシング](../Page/レイトレーシング.md "wikilink") - 反射や屈折などの表現が可能
  - [パストレーシング](https://ja.wikipedia.org/wiki/パストレーシング "wikilink") - レイトレーシングより高度な面光源照明や光源のソフトネスによるソフトシャドー、表面材質の荒さ、[被写界深度](../Page/被写界深度.md "wikilink")などの表現が可能
  - [トゥーンレンダラ](../Page/トゥーンレンダリング.md "wikilink") - 陰影付けや輪郭線をアニメ調に描き出す。[ベクタ画像の書き出しが可能](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")

大域照明は物体表面間での光の相互反射の照明効果を付け加える。

  - パストレーシング大域照明 - [拡散相互反射に加え](../Page/拡散反射.md "wikilink")、イメージ・ベースド・ライティング（IBL）などが可能
      - [イラディアンスキャッシュ](https://ja.wikipedia.org/wiki/イラディアンスキャッシュ "wikilink") - パストレーシング大域照明の計算を一部省略し補間することで高速化する
  - フォトンマッピング大域照明 - 拡散相互反射に加え、集光模様（コースティクス）の表現が可能
  - パストレーシング+フォトンマッピング大域照明 - 上記を組み合わせて間接光の到達性能などを向上させたもの
  - ラジオシティ大域照明 - [境界積分法](https://ja.wikipedia.org/wiki/境界積分法 "wikilink")を用いた拡散相互反射シミュレーション\[38\]。[オプトグラフ](https://ja.wikipedia.org/wiki/オプトグラフ "wikilink")社が開発したラジオシティ[ライブラリ](../Page/ライブラリ.md "wikilink")を使用している\[39\]

また、そのほかのレンダリング支援として次のような機能を備えている。

  - [シャドウマップ](https://ja.wikipedia.org/wiki/シャドウマップ "wikilink") - パストレーシングなどの[モンテカルロレイトレーシングを用いずにソフトシャドー](../Page/モンテカルロ法.md "wikilink")（一様なぼかしによるもの）を高速に表現できる
  - [モーションブラー](../Page/モーションブラー.md "wikilink") - 前後のサブフレームを合成し、[露出時間の長い撮影をシミュレートする](../Page/露出_\(写真\).md "wikilink")
  - フィールドレンダリング - [インターレース方式のレンダリング](../Page/走査.md "wikilink")。偶数または奇数フィールドの優先を指定できる
  - [平行投影](../Page/投影図.md "wikilink") - [パースペクティブのない投影](../Page/遠近法.md "wikilink")
  - あおり補正 - [二点透視のようなパースペクティブを可能にする](https://ja.wikipedia.org/wiki/遠近法#二点透視図法 "wikilink")
  - [魚眼レンズ](../Page/魚眼レンズ.md "wikilink")
  - [パノラマ](../Page/パノラマ.md "wikilink")レンダリング - 円柱／球／ライトプローブ／キューブマップ／バーティカルクロス形式でのパノラマまたは全球のレンダリング
  - QuickTime VR - オブジェクト／パノラマ／キュービック形式でのQuickTime VRムービー出力
  - 立体視レンダリング - [ステレオグラム](../Page/ステレオグラム.md "wikilink")および視差バリア方式の3D対応液晶用コンテンツのレンダリング

### その他

Shadeは[Python](../Page/Python.md "wikilink")言語によってシーンやオブジェクトほかの動作を制御できる。また、カスタムプラグインをC++言語によって開発するソフトウェア開発キットがある。

  - Python - Python言語による制御
  - プラグインSDK - [C++](../Page/C++.md "wikilink")言語によるカスタムプラグインの開発キット

## エディション/リリース履歴

エディションは以下に分かれている。

  - Professional版
  - Standard版 (旧advance、Personal\[40\])
  - Basic版 (旧spirit、Debut\[41\])

かつては静止画のみのmyShade (Windows版)/iShade (Mac版)や、[Unityゲームエンジン向けのShade](https://ja.wikipedia.org/wiki/Unity_\(ゲームエンジン\) "wikilink") 3D for Unity\[42\]も存在した。

|                                                                            |                                                                       |                                                      |         |
| -------------------------------------------------------------------------- | --------------------------------------------------------------------- | ---------------------------------------------------- | ------- |
| **バージョン**                                                                  | **製品ラインナップ**                                                          | **プラットフォーム**                                         | **発売日** |
| \-                                                                         | Shade Pro                                                             | [NEC PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink") | 1986年   |
| \-                                                                         | Shade                                                                 | [Macintosh](../Page/Macintosh.md "wikilink")         | 1990年   |
| \-                                                                         | Shade II Ver.1.4.2                                                    | Macintosh                                            | 1992年   |
| \-                                                                         | Shade III Ver.1.0                                                     | Macintosh                                            | 1994年   |
| ShadeIII Ver.1.1.0                                                         | Macintosh                                                             | 1994年                                                |         |
| ShadeIII Light Ver.1.1.0                                                   | Macintosh                                                             | 1994年                                                |         |
| Shade III Ver.1.2                                                          | Macintosh                                                             | 1996年                                                |         |
| Shade III Light Ver.1.2                                                    | Macintosh                                                             | 1996年                                                |         |
| 1                                                                          |                                                                       |                                                      |         |
| Shade Professional R1                                                      | Macintosh                                                             | 1996年12月                                             |         |
| Shade Personal R1                                                          | Macintosh                                                             | 1996年12月                                             |         |
| Shade debut                                                                | [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") | 1997年6月                                              |         |
| 2                                                                          |                                                                       |                                                      |         |
| Shade Professional R2                                                      | Macintosh                                                             | 1997年8月                                              |         |
| Shade Personal R2                                                          | Macintosh                                                             | 1997年8月                                              |         |
| Shade Personal Plus                                                        | Macintosh                                                             | 1998年4月                                              |         |
| Shade debut Plus                                                           | Windows                                                               | 1998年4月                                              |         |
| Shade Professional R2                                                      | Windows                                                               | 1998年8月                                              |         |
| iShade                                                                     | Macintosh                                                             | 1998年9月                                              |         |
| myShade                                                                    | Windows                                                               | 1998年11月                                             |         |
| 3                                                                          |                                                                       |                                                      |         |
| Shade Professional R3                                                      | Macintosh                                                             | 1998年12月                                             |         |
| Shade Personal R3                                                          | Macintosh                                                             | 1998年12月                                             |         |
| Shade Debut R3                                                             | Macintosh                                                             | 1998年12月                                             |         |
| Shade Professional R3                                                      | Windows                                                               | 1999年3月                                              |         |
| Shade Personal R3                                                          | Windows                                                               | 1999年3月                                              |         |
| Shade Debut R3                                                             | Windows                                                               | 1999年3月                                              |         |
| 4                                                                          |                                                                       |                                                      |         |
| Shade Professional R4                                                      | Macintosh/Windows                                                     | 1999年11月                                             |         |
| Shade Personal R4                                                          | Macintosh/Windows                                                     | 1999年11月                                             |         |
| Shade Debut R4                                                             | Macintosh/Windows                                                     | 1999年11月                                             |         |
| iShade 2/myShade 2                                                         | Macintosh/Windows                                                     | 1999年11月                                             |         |
| 5                                                                          |                                                                       |                                                      |         |
| Shade Professional R5                                                      | Macintosh/Windows                                                     | 2001年6月                                              |         |
| Shade Personal R5                                                          | Macintosh/Windows                                                     | 2001年6月                                              |         |
| Shade Debut R5                                                             | Macintosh/Windows                                                     | 2001年6月                                              |         |
| iShade 3/myShade 3                                                         | Macintosh/Windows                                                     | 2001年7月                                              |         |
| 6                                                                          |                                                                       |                                                      |         |
| Shade 6 professional                                                       | Macintosh/Windows                                                     | 2002年9月                                              |         |
| Shade 6 advance                                                            | Macintosh/Windows                                                     | 2002年9月                                              |         |
| Shade 6 spirit                                                             | Macintosh/Windows                                                     | 2002年6月                                              |         |
| iShade 6/myShade 6                                                         | Macintosh/Windows                                                     | 2002年12月                                             |         |
| 7                                                                          |                                                                       |                                                      |         |
| Shade 7 professional                                                       | Macintosh/Windows                                                     | 2004年3月                                              |         |
| Shade 7 standard                                                           | Macintosh/Windows                                                     | 2004年3月                                              |         |
| Shade 7 basic                                                              | Macintosh/Windows                                                     | 2003年12月                                             |         |
| 8                                                                          |                                                                       |                                                      |         |
| Shade 8 professional                                                       | Macintosh/Windows                                                     | 2005年7月                                              |         |
| Shade 8 standard                                                           | Macintosh/Windows                                                     | 2005年7月                                              |         |
| Shade 8 basic                                                              | Macintosh/Windows                                                     | 2005年7月                                              |         |
| 8.5                                                                        |                                                                       |                                                      |         |
| Shade 8.5 professional                                                     | Macintosh/Windows                                                     | 2006年3月                                              |         |
| Shade 8.5 standard                                                         | Macintosh/Windows                                                     | 2006年3月                                              |         |
| Shade 8.5 basic                                                            | Macintosh/Windows                                                     | 2006年3月                                              |         |
| 9                                                                          |                                                                       |                                                      |         |
| Shade 9 professional                                                       | Macintosh/Windows                                                     | 2006年12月                                             |         |
| Shade 9 standard                                                           | Macintosh/Windows                                                     | 2006年12月                                             |         |
| Shade 9 basic                                                              | Macintosh/Windows                                                     | 2006年12月                                             |         |
| iShade 9                                                                   | Macintosh/Windows                                                     | 2007年5月                                              |         |
| 10                                                                         |                                                                       |                                                      |         |
| Shade 10 professional                                                      | Macintosh/Windows                                                     | 2008年3月                                              |         |
| Shade 10 standard                                                          | Macintosh/Windows                                                     | 2008年3月                                              |         |
| Shade 10 basic                                                             | Macintosh/Windows                                                     | 2008年3月                                              |         |
| 10.5                                                                       |                                                                       |                                                      |         |
| Shade 10.5 professional                                                    | Macintosh/Windows                                                     | 2009年3月                                              |         |
| Shade 10.5 standard                                                        | Macintosh/Windows                                                     | 2009年3月                                              |         |
| Shade 10.5 basic                                                           | Macintosh/Windows                                                     | 2009年3月                                              |         |
| 11                                                                         |                                                                       |                                                      |         |
| Shade 11 Professional                                                      | Macintosh/Windows                                                     | 2009年12月                                             |         |
| Shade 11 Standard                                                          | Macintosh/Windows                                                     | 2009年12月                                             |         |
| Shade 11 Basic                                                             | Macintosh/Windows                                                     | 2009年12月                                             |         |
| 12                                                                         |                                                                       |                                                      |         |
| Shade 12 Professional                                                      | Macintosh/Windows                                                     | 2010年12月                                             |         |
| Shade 12 Standard                                                          | Macintosh/Windows                                                     | 2010年12月                                             |         |
| Shade 12 Basic                                                             | Macintosh/Windows                                                     | 2010年12月                                             |         |
| Shade 12 Basic feat. [巡音ルカ](https://ja.wikipedia.org/wiki/巡音ルカ "wikilink") | Macintosh/Windows                                                     | 2011年7月                                              |         |
| 13                                                                         |                                                                       |                                                      |         |
| Shade 13 Professional                                                      | Macintosh/Windows                                                     | 2012年3月\[43\]                                        |         |
| Shade 13 Standard                                                          | Macintosh/Windows                                                     | 2012年3月                                              |         |
| Shade 13 Basic                                                             | Macintosh/Windows                                                     | 2012年3月                                              |         |
| 14                                                                         |                                                                       |                                                      |         |
| Shade 3D Professional Ver.14                                               | Macintosh/Windows                                                     | 2013年7月                                              |         |
| Shade 3D Standard Ver.14                                                   | Macintosh/Windows                                                     | 2013年7月                                              |         |
| Shade 3D Basic Ver.14                                                      | Macintosh/Windows                                                     | 2013年7月                                              |         |
| 15                                                                         |                                                                       |                                                      |         |
| Shade 3D Professional Ver.15                                               | Macintosh/Windows                                                     | 2015年1月（バージョンアップ版先行発売）                               |         |
| Shade 3D Standard Ver.15                                                   | Macintosh/Windows                                                     | 2015年1月（バージョンアップ版先行発売）                               |         |
| Shade 3D Basic Ver.15                                                      | Macintosh/Windows                                                     | 2015年1月（バージョンアップ版先行発売）                               |         |
| 16                                                                         |                                                                       |                                                      |         |
| Shade 3D Professional Ver.16                                               | Macintosh/Windows                                                     | 2016年7月                                              |         |
| Shade 3D Standard Ver.16                                                   | Macintosh/Windows                                                     | 2016年7月                                              |         |
| Shade 3D Basic Ver.16                                                      | Macintosh/Windows                                                     | 2016年7月                                              |         |
| 17                                                                         |                                                                       |                                                      |         |
| Shade 3D Professional Ver.17                                               | Macintosh/Windows                                                     | 2017年7月                                              |         |
| Shade 3D Standard Ver.17                                                   | Macintosh/Windows                                                     | 2017年7月                                              |         |
| Shade 3D Basic Ver.17                                                      | Macintosh/Windows                                                     | 2017年7月                                              |         |
| 18                                                                         |                                                                       |                                                      |         |
| Shade 3D Professional Ver.18                                               | Macintosh/Windows                                                     | 2018年7月                                              |         |
| Shade 3D Standard Ver.18                                                   | Macintosh/Windows                                                     | 2018年7月                                              |         |
| Shade 3D Basic Ver.18                                                      | Macintosh/Windows                                                     | 2018年7月                                              |         |
| 19                                                                         |                                                                       |                                                      |         |
| Shade 3D Professional Ver.19                                               | Macintosh/Windows                                                     | 2018年11月                                             |         |
| Shade 3D Standard Ver.19                                                   | Macintosh/Windows                                                     | 2018年11月                                             |         |
| Shade 3D Basic Ver.19                                                      | Macintosh/Windows                                                     | 2018年11月                                             |         |
| 20                                                                         |                                                                       |                                                      |         |
| Shade 3D Professional Ver.20                                               | Macintosh/Windows                                                     | 2019年8月                                              |         |
| Shade 3D Standard Ver.20                                                   | Macintosh/Windows                                                     | 2019年8月                                              |         |
| Shade 3D Basic Ver.20                                                      | Macintosh/Windows                                                     | 2019年8月                                              |         |

## 搭載されているレンダラー

### 現行

  - Shade ラジオシティ
    Shade Professional R4以降に搭載されている\[44\]。[OptGraph](https://ja.wikipedia.org/wiki/OptGraph "wikilink")の技術を使用している\[45\]。

### 以前のもの

  - Shade 6 パストレーサー
    大垣真二 ([Redqueen](https://ja.wikipedia.org/wiki/Redqueen "wikilink")作者) が開発した 。
  - LUXOR (ネロ・グラフィックス) / Callisto (イーフロンティア←ライア)
    Shade 6～11のProfessional版に標準搭載されていた、フォトンマッピングを使用したGIレンダラー\[46\]。Standard版 (Advance版) 用にプラグインとして単体販売されていた。Maya版も存在した\[47\]\[48\]。
    元々[スタジオブルテリア](https://ja.wikipedia.org/wiki/スタジオブルテリア "wikilink")子会社のネロ・グラフィックスがShade 6用のLUXORの開発・販売を行った\[49\]\[50\]ものの、親会社が破産した\[51\]ため、ネロ・グラフィックスの代表取締役であった並木茂が2003年7月にライアを設立し、ライアがShade 7用のCallistoをリリースした。その後、イーフロンティアが開発元となってShade 8用のCALLISTO 2をリリースした\[52\]。

## 関連項目

  - [artist side](https://ja.wikipedia.org/wiki/artist_side "wikilink") - かつてイーフロンティアの運営していた3DCG投稿SNSサイト。

## 脚注

## 外部リンク

  - [Shade online](http://shade.e-frontier.co.jp/)

[Category:3DCGソフトウェア](https://ja.wikipedia.org/wiki/Category:3DCGソフトウェア "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink")

1.  [ASCII 24「エクス・ツールス、3DCGソフト『Shade 6 spirit』の発表会を開催」](http://ascii24.com/news/i/soft/article/2002/06/03/636238-000.html)、および[デジタルハリウッド2004年11月30日オープンカレッジレポート](http://www.dhw.co.jp/famous/opc_backnumber/report/041208/oc_repo041130.html)より出典。
2.  [3Dプリント対応機能を大幅強化--3DCGソフト「Shade 3D」最新版が11月発売へ](http://japan.cnet.com/sp/3dprinter/35055123/) CNET Japan 2014年10月15日
3.  [イーフロンティア「園田浩二が熱く語る、Shade 9の魅力とは」](http://www.e-frontier.co.jp/sonoda/)、および[ASCII 24「“神”が明かす『Shade 9』の魅力」](http://mac.ascii24.com/mac/interview/2006/12/28/666855-000.html)より出典。
4.  [Shade 13 イラディアンスキャッシュの性能向上](http://archive.shade3d.jp/13/product/new/251.html), イーフロンティア.
5.
6.  [Smith Micro Software社プレスリリース「Smith Micro Software Signs Definitive Agreement Acquiring E Frontier's 3D Graphic and Animation Software Solutions」](http://www.smithmicro.com/default.tpl?group=news_full&id1=414&id2=13)より出典。
7.  [Shade 8.5「開発者からのメッセージ」](http://shade.e-frontier.co.jp/85/message8.html)より出典。
8.  [BCN This Week 2003年6月30日 vol.996「Face」時枝敏也インタビュー](http://www.computernews.com/scripts/bcn/vb_Bridge3.dll?VBPROG=ShowWeeklyArticle&MEM=1&ImgTag=&Title=%83C%81%5B%83t%83%8D%83%93%83e%83B%83A%20Shade%8E%96%8B%C6%95%94%20%83G%83O%83%5B%83N%83e%83B%83u%83%60%81%5B%83t%83v%83%8D%83O%83%89%83%7D%81%5B&File=F:%5Cinetpub%5Cwwwroot%5Cbcn%5CWeekly%5CFace%5C20030630.htm)、および[「Shade 9一目瞭然」第11回](http://shade.e-frontier.co.jp/9/ichimoku/index.html)より出典。
9.  [BCN This Week 2007年2月5日 vol.1173「Face」園田浩二インタビュー](http://www.computernews.com/scripts/bcn/vb_Bridge3.dll?VBPROG=ShowWeeklyArticle&MEM=1&ImgTag=&Title=%83%43%81%5B%83%74%83%8D%83%93%83%65%83%42%83%41%81%40%8E%D0%92%B7%8E%BA%43%47%20%53%74%75%64%69%6F%20%8A%4A%90%DD%8F%80%94%F5%88%CF%88%F5%92%B7&File=F:\\inetpub\\wwwroot\\bcn\\Weekly\\Face\\20070205.htm)、および[「Shadeユーザー訪問記」第1回：園田浩二（前編）](http://shade.e-frontier.co.jp/houmon/001_sonoda_01.html)より出典。
10. [グッドデザイン賞ウェブサイト](http://www.g-mark.org/search/Detail?id=32192&sheet=designer)より出典。
11. [「オタク経営」が影落とすビットコインの拡大と凋落](http://jp.reuters.com/article/marketsNews/idJPL3N0NF27420140424), ロイター, 2014年4月24日.
12. [ビットコイン取引所トップ、２１日にも逮捕　３億円超流用の疑い　警視庁](http://www.sankeibiz.jp/compliance/news/150820/cpb1508201047001-n1.htm), *SankeiBiz*, 2015年8月20日.
13. [SHADE3D CO., LTD. CREATED TO DEVELOP AND MARKET ENGLISH VERSION OF POPULAR SHADE 3D GRAPHIC SOFTWARE](http://shade3d.jp/en/news/shade3drelease.html), Shade3D, 2014年9月30日.
14. [株式会社イーフロンティアとの販売代理店契約の終了とShade 3D ver.15 販売開始の延期について](http://shade3d.jp/news/detail/20141217.html), Shade3D, 2014年11月25日.
15. [End of the collaboration with our U.S publisher](http://shade3d.jp/en/news/18.html), Shade3D.
16. [イーフロンティア、民事再生法の適用を申請](http://game.watch.impress.co.jp/docs/news/20141215_680405.html), *GAME Watch*, 2014年12月15日.
17. [第2回債権者集会配付資料 報告書](https://www.mtgox.com/img/pdf/20141126_document.pdf), MTGOX, 2014年11月26日.
18. [ゴックス親会社も破産手続き開始決定 ビットコイン](http://www.asahi.com/articles/ASH2441QBH24ULFA00R.html), *朝日新聞デジタル*, 2015年2月4日.
19.
20. [会計担当者通さず流用拡大、不正会計で発覚遅れも　ビットコイン消失事件](http://www.sankei.com/affairs/news/150821/afr1508210003-n1.html), *産経ニュース*, 2015年8月21日.
21. [ビットコイン消失事件　業務上横領罪でカルプレス容疑者を起訴　「あとで返すつもりだった」と容疑を否認](http://www.sankei.com/affairs/news/150911/afr1509110050-n1.html), *産経ニュース*, 2015年9月11日.
22.
23. [ニューホライズン キャピタル、3DCGソフトウェアのShade3Dへ投資](http://ma-times.jp/21457.html), *M\&Aタイムス*, 経営戦略合同事務所, 2015年9月11日.
24. [Shade3D社に投資 国産唯一の3DCGソフトウェア「Shade」開発会社の再生と成長を支援](http://www.newhorizon.jp/news/pdf/20150911.pdf), ニューホライズンキャピタル, 2015年9月11日.
25. [第4回債権者集会配付資料 報告書](https://www.mtgox.com/img/pdf/20150909_report.pdf), MTGOX, 2015年9月9日.
26. [フォーラムエイト、国産3DCGソフトの株式会社Shade3Dの全株式を取得～3DVR事業の拡大を加速～](http://www.forum8.co.jp/forum8/press/press180829.htm)
27.
28. [エキサイトニュース総合研究所「『CGアイドル』の魅力に迫る」](http://media.excite.co.jp/News/weekly/040713/topics_p02.html)、および[イーフロンティア「デジタルビューティ」](http://content.e-frontier.co.jp/digitalbeauty/index.html)より出典。
29.
30. [Shadeユーザー訪問記 第18回：マンガ家 寺沢武一先生](http://archive.shade3d.jp/houmon/018_terasawa.html), イーフロンティア, 2010年12月14日.
31. [木城ゆきと公式ウェブサイト『ゆきとぴあ』](http://yukito.com/)内「ゆきとの書斎」、および[CONTENT PARADISE NEWS 2008年4月25日号「アーティストに聞く『3DCGだからこそ可能なリアルさを求めて』～マンガ家：奥浩哉先生」](http://www.contentparadise.com/static/jp_newsletter/20080425/index.html)より出典。
32. [Shade 10シリーズ用 10.0.2アップデータでの変更点](http://shade.e-frontier.co.jp/support/1002fixed-01.html)より出典。
33. [T4社「制作実績」](http://www.t4net.jp/products)より出典。
34. 同梱ユーザガイド（Shade R4／7／9／10）より引用。
35. [Shade online Free Talk「表面材質の、光沢1、光沢2、のスライダー」](http://shade-lounge.e-frontier.co.jp/modules/newbb/viewtopic.php?topic_id=985&forum=1)より出典。
36. Shade online：まいこのShade教室「[ミニ講座3 後半](http://shade.e-frontier.co.jp/maiko/lesson_003/l_003.html)」および「[ミニ講座5 後半](http://shade.e-frontier.co.jp/maiko/lesson_005/l_005.html)」より出典。
37.
38. [オプトグラフ社のウェブサイト](http://www.optgraph.com/)より出典。
39. [ASCII 24「エクス・ツールス、『Shade Personal R4』にラジオシティ機能を追加する『Shade R4 Radiosity Kit』を発売」](http://ascii24.com/news/i/soft/article/2000/04/07/608228-000.html)より出典。
40. [おかげさまでバージョン10を迎えました 生まれ変わった3DCGソフト！ 『Shade 10』シリーズ発売のお知らせ](http://www.e-frontier.co.jp/company/press/2008/20080118a.html) e-frontier 2008年1月18日
41.
42. ['Shade 3D for Unity' Now Free](http://www.awn.com/news/shade-3d-unity-now-free) Animation World Network 2012年10月26日
43. [イーフロンティア、3DCG作成ソフト「Shade 13」を発表 - ITmedia PC USER](http://www.itmedia.co.jp/pcuser/articles/1202/03/news058.html)
44. [Shadeの歴史を振り返る](http://archive.shade3d.jp/20th/history/history04.html) Shade 3D
45. [Shade 8.5 Read Me](http://mirye.net/2-uncategorised/50-shade-8-5-read-me) Mirye Software Publishing
46. [Shade 6 ユーザー発表会にて「Shade 6 advance/professional」を一般公開](http://news.mynavi.jp/news/2002/08/05/08.html) Mynavi Corporation 2002年8月5日
47. [LUXOR for MAYA](https://web.archive.org/web/20030408074621/http://www.ngc.co.jp/products/luxor/index.html) NGC Corporation
48. [What's new\!](https://web.archive.org/web/20030618051029/http://www.nero-graphics.co.jp/newsrelease/release_list.htm) ネロ・グラフィックス
49. [ネロ・グラフィックス、国産高性能レンダラーの開発に着手](http://ascii.jp/elem/000/000/316/316760/) ASCII 2000年9月5日
50. [ネロ・グラフィックス、3DCGコンテンツ制作事業でエクス・ツールスと業務提携](http://ascii.jp/elem/000/000/328/328590/) ASCII 2002年1月16日
51. [破産申立のお知らせ](https://web.archive.org/web/20030320114204/http://studiobt.com/) スタジオブルテリア 2003年3月3日
52. [CALLISTO 2 for Shade 8 standard発売のお知らせ](https://web.archive.org/web/20051214030336/http://www.e-frontier.co.jp/release/news/050722_p_call.html) イーフロンティア 2005年7月22日