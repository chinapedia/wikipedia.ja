> この記事は[Shift JIS](https://ja.wikipedia.org/wiki/Shift_JIS)から翻訳されています。


**Shift_JIS**（シフトジス）は、[コンピュータ](../Page/コンピュータ.md "wikilink")上で[日本語](../Page/日本語.md "wikilink")を含む[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")を表現するために用いられる[文字コード](../Page/文字コード.md "wikilink")の一つ。かつては[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")による独自拡張を含む文字コード群を指した[曖昧](https://ja.wikipedia.org/wiki/曖昧 "wikilink")な名称であったが、1997年に[標準化](https://ja.wikipedia.org/wiki/標準化 "wikilink")文書[JIS X 0208](https://ja.wikipedia.org/wiki/JIS_X_0208 "wikilink"):1997の附属書1で規定された。「Shift_JIS」は[IANAにおける登録名である](https://ja.wikipedia.org/wiki/Internet_Assigned_Numbers_Authority "wikilink")\[1\]。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")などの各ベンダーが実装するShift_JISの亜種については「[Microsoftコードページ932](https://ja.wikipedia.org/wiki/Microsoftコードページ932 "wikilink")」を参照。[Mac OSが実装する亜種については](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")「[MacJapanese](https://ja.wikipedia.org/wiki/MacJapanese "wikilink")」を参照。

## 構造

[JIS X 0201を](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")1バイトで、[JIS X 0208を](https://ja.wikipedia.org/wiki/JIS_X_0208 "wikilink")2バイトで符号化する可変幅文字符号化方式。  ただし、9区(8540<sub>16</sub>)から15区(889E<sub>16</sub>)までおよび85区(EB40<sub>16</sub>)から94区(EFFC<sub>16</sub>)まではJIS X 0208で空き領域とされており、文字は割り当てられていない。

## Shift_JISの誕生

[1980年代](../Page/1980年代.md "wikilink")、[パソコン用](../Page/パーソナルコンピュータ.md "wikilink")[16ビット](https://ja.wikipedia.org/wiki/16ビット "wikilink")[CPU](../Page/CPU.md "wikilink")の普及もあいまって、[漢字](../Page/漢字.md "wikilink")や[ひらがな](https://ja.wikipedia.org/wiki/ひらがな "wikilink")・[カタカナ](https://ja.wikipedia.org/wiki/カタカナ "wikilink")を表示可能な[ハードウェア](../Page/ハードウェア.md "wikilink")を備えたパソコンが続々と発売された。そのため、日本語を表現できる[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")が模索されていた（Shift_JISを「シフトJISコード」と呼んで[符号化文字集合](https://ja.wikipedia.org/wiki/文字集合 "wikilink")（文字コード）の面のみを考える議論があるが、ここでは文字符号化方式の面に焦点を当てる）。

文字符号化方式Shift_JISの設計者らは、先行してよく利用されていたJIS C 6220（現在の[JIS X 0201](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")）の[8ビット](https://ja.wikipedia.org/wiki/8ビット "wikilink")符号（以下「[英数字](https://ja.wikipedia.org/wiki/英数字 "wikilink")・[半角カナ](https://ja.wikipedia.org/wiki/半角カナ "wikilink")」）と、JIS C 6226（現在の[JIS X 0208](https://ja.wikipedia.org/wiki/JIS_X_0208 "wikilink")、以下「漢字」）の両文字集合を表現しようとした。また、ファイルの大きさや処理時間の短縮を図るため、[エスケープシーケンス](https://ja.wikipedia.org/wiki/エスケープシーケンス "wikilink")なしで混在可能にすることを企図した。

JIS C 6220とJIS C 6226の2つはともに、[ISO 2022で](https://ja.wikipedia.org/wiki/ISO/IEC_2022 "wikilink")[文字集合](https://ja.wikipedia.org/wiki/文字集合 "wikilink")を切り替えて利用する設計があった。ISO 2022に基づく文字符号化方式では、英数字、[半角カナ](https://ja.wikipedia.org/wiki/半角カナ "wikilink")、漢字はそれぞれ、8ビット符号空間の中のGL/GRという領域の1つを（ただし漢字は2回）使うことで表現できる。もし英数字と漢字の2つをエスケープシーケンスなしで混在したいなら、英数字をGL、漢字をGRに割り当てる方法がある。[EUC-JP](https://ja.wikipedia.org/wiki/EUC-JP "wikilink")は、おおよそそのように実装されている。

しかし、パソコンではすでに、JIS X 0201の8ビット符号、つまりGLに英数字、GRに1[バイトカタカナ](https://ja.wikipedia.org/wiki/バイト_\(情報\) "wikilink")（[半角カタカナ](https://ja.wikipedia.org/wiki/半角カタカナ "wikilink")）を割り当てた符号が普及していた。英数字と1バイトカタカナの2つを動かすことは、[文字化け](https://ja.wikipedia.org/wiki/文字化け "wikilink")の原因になるため避ける必要があった。そのため、ISO 2022の枠内の領域に漢字を混在させることは困難だった。

[1982年](../Page/1982年.md "wikilink")（[昭和](../Page/昭和.md "wikilink")57年）、漢字の[符号位置を複雑に移動](https://ja.wikipedia.org/wiki/符号点 "wikilink")（シフト）し、符号空間の隙間に押し込むShift_JISが誕生した。これを実現するためには、漢字の1バイト目として、ISO 2022において不使用のCR（-）領域に加え、ISO 2022におけるGR（-）領域に約3分の1残していた未使用領域の一部から捻出することとした。さらに2バイト目には、ISO 2022とは異なり、英数字・半角カナに使用済みの領域をも含む、GL、CR、GRにあたる各領域のほぼ全てを使う必要があった。ただし、GL（-）領域においては、JIS X 0201の記号に当たる部分は極力避けた。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")日本法人元会長の[古川享](https://ja.wikipedia.org/wiki/古川享 "wikilink")によると、Shift_JISの制定には[アスキー](https://ja.wikipedia.org/wiki/アスキー_\(企業\) "wikilink")、マイクロソフト（米）、[三菱電機](https://ja.wikipedia.org/wiki/三菱電機 "wikilink")、[マイクロソフトウェア・アソシエイツ](https://ja.wikipedia.org/wiki/マイクロソフトウェア・アソシエイツ "wikilink")、[デジタルリサーチ](https://ja.wikipedia.org/wiki/デジタルリサーチ "wikilink")（米）が関わり、特にアスキーの[山下良蔵](https://ja.wikipedia.org/wiki/山下良蔵 "wikilink")が中心となって行われたという\[2\]。これに対する異説として、[京都大学](../Page/京都大学.md "wikilink")助教授の[安岡孝一](https://ja.wikipedia.org/wiki/安岡孝一 "wikilink")は、マイクロソフトウェア・アソシエイツと三菱電機のみの共同開発だと主張していたが\[3\]、山下本人の発言\[4\]により安岡は自説を撤回する発言をしている\[5\]。また古くは**の訳書 (ISBN 4-7561-0783-4) の「UNIX人名事典」翻訳版加筆部分 (p.45) で、[深瀬弘恭](https://ja.wikipedia.org/wiki/深瀬弘恭 "wikilink")に「MS漢字コードの作者の一人」という紹介文が書かれていた。

## Shift_JISの実装

Shift_JISはマイクロソフトの[MS-DOS](../Page/MS-DOS.md "wikilink")に「MS漢字コード」（および後の[Microsoftコードページ932](https://ja.wikipedia.org/wiki/Microsoftコードページ932 "wikilink")）、デジタルリサーチの[CP/M-86](https://ja.wikipedia.org/wiki/CP/M-86 "wikilink")に「SJC-26」として採用された。両者はほぼ同じだが、[全角スペース](https://ja.wikipedia.org/wiki/全角スペース "wikilink")の扱いに違いがある。全角スペースにMS-DOSはを割り当てているが、CP/M-86は半角スペース2文字分と同等のを割り当てている。CP/M-86での実装は文字列からスペースを探索する処理が簡単になるという[プログラミング上の利点があった](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")。一方、MS-DOSは全角スペースに別のコードを割り当てることで、半角入力モードで[スペースキー](https://ja.wikipedia.org/wiki/スペースキー "wikilink")が2回押されたのか、全角入力モードでスペースキーが1回だけ押されたのかをプログラムが判別できるようにした。これは当時のアプリケーションソフト（[Multiplanなど](https://ja.wikipedia.org/wiki/Microsoft_Multiplan "wikilink")）でメニュー選択にスペースキーを使用していたためであった。また、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")では全角スペースと半角スペースの幅の比が2対1でない場合があるため、スペースの区別は[帳票](https://ja.wikipedia.org/wiki/帳票 "wikilink")設計に影響があった\[6\]。

## Shift_JISの標準化

Shift_JISは、[符号化文字集合とその文字符号化方式の両方を含む現実の問題を解決するための技術である](https://ja.wikipedia.org/wiki/文字集合 "wikilink")。それゆえ、JIS X 0208の文字集合を利用してはいるものの、ISO 2022の符号化の方針の範囲の外にある。しかし現在では、JIS X 0208:1997の附属書1に、「シフト符号化表現」という名前で仕様が定義されている。

JIS X 0208の拡張規格であるJIS X 0213では、[2000年](../Page/2000年.md "wikilink")（[平成](../Page/平成.md "wikilink")12年）制定の初版で附属書1としてShift_JISX0213が定められた。[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")（平成16年）改正時の10文字追加に伴って、Shift_JIS-2004と名称が変更された。

IANAでも「Shift_JIS」という名前が割り当てられている\[7\]。

## 利点と欠点

  - 利点

:\# 全角文字と、JIS X 0201で定義したいわゆる半角カナ文字を同一のコード体系で表現できる。

:\# 日本語環境においては、MS-DOSで日本語用文字コードとして採用されて以来、パソコンにおいて圧倒的な普及度があり、その他の文字符号化方式に比べてデータ交換可能性が高い。

  - 欠点

:\# 半角カナのための領域を確保した関係上、コードシークエンスが区点番号の「区」の区切りではない箇所で分断している。このため、コード番号を演算で求める際は煩雑な処理が必要である。

:\# 2バイト目に未満（[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")のコード領域）が現れる。このため、文字の区切りの判定に手間がかかる。ファイルや電文の先頭から文字コードの判定をする場合はよいが、後ろから判定をしようとすると、最悪の場合、先頭までたどらないといけないことがあるため、プログラムの作り方に工夫が必要になる。また、この領域に含まれる一部の文字の扱いのため、マルチバイトのEUC-JP、[UTF-8](https://ja.wikipedia.org/wiki/UTF-8 "wikilink")などに比べ、プログラミング上の扱いが難しい（[次項を参照](https://ja.wikipedia.org/wiki/#2バイト目が5C16等に成りうることによる問題 "wikilink")）。

:\# [JIS補助漢字が表現できない](https://ja.wikipedia.org/wiki/JIS_X_0212 "wikilink")。補助漢字の文字数はShift_JISのコード未登録部分に収まらない。

:\# 文字集合については実装ベンダがJIS X 0208で規定されていない機種依存の拡張を施していることが多く、こういった拡張部分に関してはデータ交換可能性が低い。

## 2バイト目が5C等になりうることによる問題

<table>
<caption><strong> 2バイト目にを持つ文字一覧</strong></caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>符号（16進）</p></th>
<th><p>読み・意味</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/ダッシュ_(記号)" title="wikilink">―</a></p></td>
<td><p>815C</p></td>
<td><p>ダッシュ</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/そ" title="wikilink">ソ</a></p></td>
<td><p>835C</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/片仮名" title="wikilink">片仮名</a>の「そ」</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Ы" title="wikilink">Ы</a></p></td>
<td><p>845C</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/キリル文字" title="wikilink">キリル文字</a>のウィ</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>875C</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoftコードページ932" title="wikilink">Windows環境ではローマ数字の</a>9。<br />
<a href="https://ja.wikipedia.org/wiki/MacJapanese" title="wikilink">Mac環境ではGB</a>（ギガバイト）。</p></td>
</tr>
<tr class="odd">
<td><p>噂</p></td>
<td><p>895C</p></td>
<td><p>うわさ。</p></td>
</tr>
<tr class="even">
<td><p>浬</p></td>
<td><p>8A5C</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/海里" title="wikilink">海里</a>。</p></td>
</tr>
<tr class="odd">
<td><p>欺</p></td>
<td><p>8B5C</p></td>
<td><p>ギ、あざむ（く）。詐<strong>欺</strong></p></td>
</tr>
<tr class="even">
<td><p>圭</p></td>
<td><p>8C5C</p></td>
<td><p>ケイ。人名。</p></td>
</tr>
<tr class="odd">
<td><p>構</p></td>
<td><p>8D5C</p></td>
<td><p>コウ、かま（える）。<strong>構</strong>造</p></td>
</tr>
<tr class="even">
<td><p>蚕</p></td>
<td><p>8E5C</p></td>
<td><p>サン、<a href="https://ja.wikipedia.org/wiki/カイコ" title="wikilink">かいこ</a>。養<strong>蚕</strong></p></td>
</tr>
<tr class="odd">
<td><p>十</p></td>
<td><p>8F5C</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/漢数字" title="wikilink">漢数字</a>の10。</p></td>
</tr>
<tr class="even">
<td><p>申</p></td>
<td><p>905C</p></td>
<td><p>シン、もう（す）、<a href="https://ja.wikipedia.org/wiki/干支" title="wikilink">さる</a>。<strong>申</strong>請</p></td>
</tr>
<tr class="odd">
<td><p>曾</p></td>
<td><p>915C</p></td>
<td><p>ソ、ひ。「曽」の印刷標準字体（正字体）。<strong>曾</strong>孫</p></td>
</tr>
<tr class="even">
<td><p>箪</p></td>
<td><p>925C</p></td>
<td><p>タン。<strong>箪</strong>笥、瓢<strong>箪</strong></p></td>
</tr>
<tr class="odd">
<td><p>貼</p></td>
<td><p>935C</p></td>
<td><p>チョウ、は（る）。<strong>貼</strong>付</p></td>
</tr>
<tr class="even">
<td><p>能</p></td>
<td><p>945C</p></td>
<td><p>ノウ、よ（く）。<strong>能</strong>力</p></td>
</tr>
<tr class="odd">
<td><p>表</p></td>
<td><p>955C</p></td>
<td><p>ヒョウ、あらわ（す）。<strong>表</strong>現</p></td>
</tr>
<tr class="even">
<td><p>暴</p></td>
<td><p>965C</p></td>
<td><p>ボウ、あば（れる）、あば（く）。<strong>暴</strong>力</p></td>
</tr>
<tr class="odd">
<td><p>予</p></td>
<td><p>975C</p></td>
<td><p>ヨ、あらかじ（め）。<strong>予</strong>備</p></td>
</tr>
<tr class="even">
<td><p>禄</p></td>
<td><p>985C</p></td>
<td><p>ロク。俸<strong>禄</strong></p></td>
</tr>
<tr class="odd">
<td><p>兔</p></td>
<td><p>995C</p></td>
<td><p>ト、<a href="../Page/ウサギ.md" title="wikilink">うさぎ</a>。「兎」の異体字</p></td>
</tr>
<tr class="even">
<td><p>喀</p></td>
<td><p>9A5C</p></td>
<td><p>キャク。<strong>喀</strong>血</p></td>
</tr>
<tr class="odd">
<td><p>媾</p></td>
<td><p>9B5C</p></td>
<td><p>コウ。<strong>媾</strong>和（講和の非書換え）</p></td>
</tr>
<tr class="even">
<td><p>彌</p></td>
<td><p>9C5C</p></td>
<td><p>ミ（<a href="https://ja.wikipedia.org/wiki/呉音" title="wikilink">呉</a>）、ビ（<a href="https://ja.wikipedia.org/wiki/漢音" title="wikilink">漢</a>）、や。弥生の「弥」の正字体。<br />
人名などに多く使われる（<a href="https://ja.wikipedia.org/wiki/和泉元彌" title="wikilink">和泉元彌</a>など）。</p></td>
</tr>
<tr class="odd">
<td><p>拿</p></td>
<td><p>9D5C</p></td>
<td><p>ダ。<strong>拿</strong>捕</p></td>
</tr>
<tr class="even">
<td><p>杤</p></td>
<td><p>9E5C</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/栃" title="wikilink">栃</a>の別体</p></td>
</tr>
<tr class="odd">
<td><p>歃</p></td>
<td><p>9F5C</p></td>
<td><p>ソウ（呉）、ショウ（漢）、すす（る）。</p></td>
</tr>
<tr class="even">
<td><p>濬</p></td>
<td><p>E05C</p></td>
<td><p>シュン、さら（う）。</p></td>
</tr>
<tr class="odd">
<td><p>畚</p></td>
<td><p>E15C</p></td>
<td><p>ホン、ふご。</p></td>
</tr>
<tr class="even">
<td><p>秉</p></td>
<td><p>E25C</p></td>
<td><p>ヘイ、と（る）。「兼」の字源とする漢字</p></td>
</tr>
<tr class="odd">
<td><p>綵</p></td>
<td><p>E35C</p></td>
<td><p>サイ、あや。</p></td>
</tr>
<tr class="even">
<td><p>臀</p></td>
<td><p>E45C</p></td>
<td><p>デン、しり。<strong>臀</strong>部</p></td>
</tr>
<tr class="odd">
<td><p>藹</p></td>
<td><p>E55C</p></td>
<td><p>アイ。和気<strong>藹</strong>々</p></td>
</tr>
<tr class="even">
<td><p>觸</p></td>
<td><p>E65C</p></td>
<td><p>ショク。<a href="https://ja.wikipedia.org/wiki/触" title="wikilink">触</a>の旧字体</p></td>
</tr>
<tr class="odd">
<td><p>軆</p></td>
<td><p>E75C</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/体" title="wikilink">体</a>の古字</p></td>
</tr>
<tr class="even">
<td><p>鐔</p></td>
<td><p>E85C</p></td>
<td><p>つば。刀の<strong>鐔</strong>（鍔）。</p></td>
</tr>
<tr class="odd">
<td><p>饅</p></td>
<td><p>E95C</p></td>
<td><p>マン。<strong>饅</strong>頭</p></td>
</tr>
<tr class="even">
<td><p>鷭</p></td>
<td><p>EA5C</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/バン_(鳥類)" title="wikilink">バン</a>。鳥の名。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>ED5C[8]</p></td>
<td><p>シュン。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>EE5C[9]</p></td>
<td><p>ギョク。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>FA5C[10]</p></td>
<td><p>コウ、わた。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>FB5C[11]</p></td>
<td><p>ギン。</p></td>
</tr>
</tbody>
</table>

Shift_JISでは、カタカナの「ソ」、漢字の「噂」など一部の文字の2バイト目に、（Shift_JISでは[円記号](https://ja.wikipedia.org/wiki/円記号 "wikilink")、ASCIIなどでは[バックスラッシュ](https://ja.wikipedia.org/wiki/バックスラッシュ "wikilink")）を使用している。多くのプログラミング言語（[C](../Page/C言語.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[Bourne Shellなど多数](https://ja.wikipedia.org/wiki/Bourne_Shell "wikilink")）では、このを[エスケープ文字](https://ja.wikipedia.org/wiki/エスケープ文字 "wikilink")としている。したがって、ソースコードや文字データの処理においてShift_JISを想定していないプログラミング環境では問題が起こる。この問題は、同じように2バイト目の範囲にを含む[Big5](../Page/Big5.md "wikilink")や、まれではあるが[GBK](https://ja.wikipedia.org/wiki/GBK "wikilink")などの[文字コード](../Page/文字コード.md "wikilink")でも発生しうる。

また、以外についても類似の問題が発生することがある。たとえば、[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")やMS-DOSなどの[シェル](../Page/シェル.md "wikilink")上で、2バイト目がになる文字（Shift_JISやASCIIでは[バーティカルバー](https://ja.wikipedia.org/wiki/バーティカルバー "wikilink")）を含む文字（−\[12\]、ポ、л、榎、掛、弓、芸、……）をファイル名に使用しようとすると、[パイプ記号と認識され](https://ja.wikipedia.org/wiki/パイプ_\(コンピュータ\) "wikilink")、正常にファイルが作成されなかったり、読み込みが不良になったりすることがある。

現在でも、シングルバイト文字コード前提のソフトウェアをShift_JIS環境で使用すると、改行などの動作やファイル名の処理などにしばしばこの問題がつきまとう。これらの文字は俗称として「だめ文字」あるいは「ダメ文字」と呼ばれることがある \[13\]。

この問題を回避する伝統的な方法として、ソースコード全体を[EUCコードやUTF](https://ja.wikipedia.org/wiki/EUC-JP "wikilink")-8などに変換してからコンパイルしたり実行したりする方法がある（例：Perl のencodingプラグマ）。あるいは「ソ」→「ソ\\」のように、2バイト目の直後にエスケープ文字のを記述し、「ダメ文字」を文字として正しく認識させる方法もある（例：[Perl](../Page/Perl.md "wikilink")のSjisソフトウェア\[14\]や[JavaScript](../Page/JavaScript.md "wikilink")）。あるいは文字または文字列として扱わず対象文字および内部表現形式を数値の配列として変換を行い、取り扱う際に文字に復号して扱う方法もある（例：PerlのEncodeモジュール\[15\]）。

  - 例
    マルチバイト非対応のアプリケーションやシステムでは、「構わない」という文字列は「高墲ﾈい」に文字化けする。
    {| class="wikitable" style="text-align:center;"

\! colspan="2" | 構 \! colspan="2" | わ \! colspan="2" | な \! colspan="2" | い |- | 8d | style="background: yellow;"| **5c** | 82 | ed | 82 | c8 | 82 | a2 |- | colspan="8" | ▼バックスラッシュにあたる**5c**が抜けた場合 |- | 8d | style="background: yellow;"|   | 82 | ed | 82 | c8 | 82 | a2 |- \! colspan="3" | 高 \! colspan="2" | 墲 \! ﾈ \! colspan="2" | い |}

  -
    「い」でデコードが再同期され、後の文字列は正常に表示される。また、同様に「芸能界」という文字列は「芸矧E」に文字化けする。
    {| class="wikitable" style="text-align:center;"

\! colspan="2" | 芸 \! colspan="2" | 能 \! colspan="2" | 界 |- | 8c | 7c | 94 | style="background: yellow;"| **5c** | 8A | 45 |- | colspan="6" | ▼バックスラッシュにあたる**5c**が抜けた場合 |- | 8C | 7c | 94 | style="background: yellow;"|   | 8A | 45 |- \! colspan="2" | 芸 \! colspan="3" | 矧 \! E |}

## コード空間における文字数制限

Shift_JISで（ISO 2022の94×94に相当する）2バイトコードの空間は、第1バイトが-ならびに-となっており、第2バイトが-ならびに-である。したがって、47×188=8836文字、さらに1バイトコードが158文字（スペースを含み、DELは数えず）であるため、計8994文字となる。

しかし第1バイトには以降も未使用域が続いているため、Microsoftコードページ932などの派生規格では-を動員する形で拡張している。この場合は60×188＋158＝計11438文字まで拡張できることになる。 たとえば、Shift_JIS-2004では、2バイト文字が11233文字、1バイト文字が158文字のため、合計11391文字を使用している。

## Shift_JISにおける「シフト」とは

Shift_JISの「[シフト](https://ja.wikipedia.org/wiki/シフト "wikilink")」とは、256×256の平面の中で文字を複雑に“ずらす”という意味の「シフト」である。

[ISO-2022-JP](https://ja.wikipedia.org/wiki/ISO-2022-JP "wikilink")は[指示シーケンス](https://ja.wikipedia.org/wiki/指示シーケンス "wikilink")で漢字と[アルファベットを切り替える符号化方式である](https://ja.wikipedia.org/wiki/ラテン文字 "wikilink")。また、EUC-JPは[補助漢字と半角カタカナを](https://ja.wikipedia.org/wiki/JIS_X_0212 "wikilink")[シングルシフト](https://ja.wikipedia.org/wiki/シングルシフト "wikilink")で一時的に切り替えて使う符号化方式である。これらの符号化方式で行われている、各文字集合の面を[シフトコードによって切り替える操作も](https://ja.wikipedia.org/wiki/漢字シフトコード "wikilink")「シフト」と呼ばれるが、Shift_JISの「シフト」はこれらとは異なる意味である。またビットをずらす操作（[ビットシフト](https://ja.wikipedia.org/wiki/ビットシフト "wikilink")）とも異なる。

## Shift_JISと区点番号

Shift_JISが符号化の対象にする文字集合は、JIS X 0208である。この符号化文字集合には、[区点番号](https://ja.wikipedia.org/wiki/区点番号 "wikilink")という概念が存在する。これは、94×94の文字表の行と列の番号の組である。

Shift_JISでは、-というように、JIS X 0208とはまったく違ったコード体系であるが、JIS X 0208を計算により変形したものであるため、区点番号を用いて文字のコードポイントを指し示すことが多い。内容については、JIS X 0208の1-94区と同じである。ただし、機種依存文字では、シフトJISの符号空間から逆成し、94区の下方にあたかも120区までが拡張しているかのように扱うことがある。95区以上は、ISO/IEC 2022に則ったJIS X 0208の構造では存在し得ないので、本来はおかしい。ベンダ独自の非公式な概念である。なお、[JIS X 0213の規格の一部である](https://ja.wikipedia.org/wiki/JIS_X_0213 "wikilink")**Shift_JISX0213符号化表現**においては、第1バイト以降を2面の文字に割り当てており、百何区というような存在しない区番号は登場しない。

## 「x-sjis」と「MS_Kanji」

「x-sjis」と「MS_Kanji」はともに、[HTMLドキュメントの](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink")「charset」の指定に「Shift_JIS」の別名として使うことが出来る。

「x-sjis」はIANAに「Shift_JIS」という名前を登録する前に、[Netscape Navigator](https://ja.wikipedia.org/wiki/Netscape_Navigator_\(ネットスケープコミュニケーションズ\) "wikilink") 2.0において使っていたエンコーディングの指定子名である。一部のHTML生成ソフトが自動でこの指定子を組み込んで使っている。そのため認識可能なブラウザがあるが、「Shift_JIS」に書き換えることを推奨している。

「MS_Kanji」はIANAにより「Shift_JIS」の別名として割り当てられている\[16\]。

## 脚注

## 関連項目

  - [アスキーアート\#日本での使用](https://ja.wikipedia.org/wiki/アスキーアート#日本での使用 "wikilink")
  - [文字化け](https://ja.wikipedia.org/wiki/文字化け "wikilink")

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink")

1.
2.  古川享 「[私のマイコン遍歴、日本のパソコン30年史、その1](http://furukawablog.spaces.live.com/Blog/cns!1pmWgsL289nm7Shn7cS0jHzA!2225.entry)」の2005年12月28日のコメント 『[古川享ブログ](http://furukawablog.spaces.live.com/)』 2005年12月28日
3.  安岡孝一 「[日本における最新文字コード事情](http://kanji.zinbun.kyoto-u.ac.jp/~yasuoka/publications/ISCIE2001.pdf)」『システム/制御/情報』、Vol. 45, [No. 9](http://www.iscie.or.jp/j/?%E3%80%8C%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0%2F%E5%88%B6%E5%BE%A1%2F%E6%83%85%E5%A0%B1%E3%80%8D%E7%AC%AC45%E5%B7%BB#na671586), pp. 528–535, 2001
    安岡孝一 「[シフトJISの誕生](http://slashdot.jp/~yasuoka/journal/334730)」 2005年12月22日
    安岡孝一 「[Re:古川享さんがシフトJIS誕生について書いています](http://slashdot.jp/comments.pl?sid=292835&cid=857031)」 2005年12月29日
    安岡孝一、安岡素子『文字符号の歴史 欧米と日本編』共立出版 2006年2月 ISBN 978-4-320-12102-7
4.  山下良蔵 「[私のマイコン遍歴、日本のパソコン30年史、その1](http://furukawablog.spaces.live.com/Blog/cns!1pmWgsL289nm7Shn7cS0jHzA!2225.entry)」の2006年9月21日のコメント 『[古川享ブログ](http://furukawablog.spaces.live.com/)』 2006年9月21日
5.  安岡孝一「[Re:古川享さんがシフトJIS誕生について書いています](http://slashdot.jp/comments.pl?sid=292835&cid=1028873)」 2006年9月29日
6.  西田憲正「Unix風の機能を持ち込んだ日本語MS-DOS2.0の機能と内部構造」『日経エレクトロニクス』 1983年12月19日号、pp.165-190。
7.
8.  Windows環境 (CP932) で該当。
9.
10.
11.
12. 817C。Windows環境では全角マイナス「－」が該当する。
13.
14. [Char-Sjis-1.08 - Native Encoding Support by Traditional Scripting - metacpan.org](https://metacpan.org/release/Char-Sjis)
15. [Encode-3.00 - character encodings in Perl - metacpan.org](https://metacpan.org/release/Encode)
16.