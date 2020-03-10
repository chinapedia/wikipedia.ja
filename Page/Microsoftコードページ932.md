> この記事は[Microsoft932](https://ja.wikipedia.org/wiki/Microsoft932)から翻訳されています。


[lang=ja](https://ja.wikipedia.org/wiki/画像:Euler_diag_for_jp_charsets.svg "wikilink")\]\]

**Microsoft コードページ 932**（CP932）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")及び、[MS-DOS](../Page/MS-DOS.md "wikilink")の[OEM](../Page/OEM.md "wikilink")ベンダが[Shift_JIS](../Page/Shift_JIS.md "wikilink")を独自に拡張した[文字コード](../Page/文字コード.md "wikilink")である。また同時に、CP932はShift_JISの[Windowsアプリケーションにおける](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")「実装」を指す用語であるとも言える。

この項では、主にShift_JISにおけるマイクロソフトおよび各ベンダの独自拡張部分について言及する。ベンダ独自拡張部分以外の内容については、[Shift_JIS](../Page/Shift_JIS.md "wikilink")を参照されたい。

また、[マイクロソフト標準キャラクタセット](../Page/マイクロソフト標準キャラクタセット.md "wikilink")の項目も併せて参照されたい。

## CP932の呼称（別名）の整理

  - Windows-31J
    [Windows 3.1](../Page/Microsoft_Windows_3.x.md "wikilink") (J) のリリースに合わせて、マイクロソフトが [IBM](../Page/IBM.md "wikilink")と[日本電気](../Page/日本電気.md "wikilink") (NEC) のコードを統合して作った符号化文字集合。1993 年以降、マイクロソフトが自社のドキュメント等で「CP932」という用語を使って表している対象は、常にこの「Windows-31J」である。この名前は [IANA](../Page/Internet_Assigned_Numbers_Authority.md "wikilink") に登録されている。
  - MS932
    Java で、「IBM の[コードページ](../Page/コードページ.md "wikilink") 932」と「Windows-31J」を区別するための用語。Windows-31Jを指す。
  - CP932
    [MS-DOS](../Page/MS-DOS.md "wikilink")とWindowsにおける日本語コードページを表す用語。「Windows-31J」が制定されるまでは、OEMベンダによって文字集合が違う。
  - MS 漢字コード
    「CP932」とほぼ同じ意味の用語である。マイクロソフトが（Shift_JIS という符号化方式を）策定したという点や、マイクロソフトが（JIS X 0208という文字集合に対して）文字を独自に追加した点を強調したい場合に用いられる。また、単に「シフトJIS」のことを指している場合もある。
  - OEM コードページ 932
    Windows 3.1 日本語版の発売以前における、OEMベンダ各自の拡張を許した仕様の文字セット。

以下は、マイクロソフトから離れ、現在では公的機関からも認められた文字符号化方式を指す用語である。

  - シフトJIS
    [JIS X 0208符号化文字集合を一定の規則に従ってシフトした文字符号化方式](../Page/JIS_X_0208.md "wikilink")。具体的な内容はJIS X 0208:1997に「シフト符号化表現」として記載がある。しかし、文脈によってはベンダ拡張されたコードセットを指している場合もある。
  - Shift_JIS
    「シフトJIS」のIANA登録名。
  - SJIS
    **Shift_JIS**の短縮形。JavaではShift_JISと同義語。

## 構造

Shift_JISでは空き領域や未使用であった13区(8740<sub>16</sub> - 879E<sub>16</sub>)、89 - 92区(ED40<sub>16</sub> - EEFC<sub>16</sub>)、115 - 119区(FA40<sub>16</sub> - FC9E<sub>16</sub>)に合計845文字を追加。ただし同じ文字が互換性のため重複して含まれており実質447文字の追加である。また、95 - 114区(F040<sub>16</sub> - F9FC<sub>16</sub>)も利用者定義領域（外字領域）となっている。

## 歴史

### CP932 の誕生と発展

CP932が、現在の「Windows-31J」の形として完成に至るまでには複雑な経緯がある。

[1982年](../Page/1982年.md "wikilink")（JIS X 0208-1983策定の前年）、[JIS C 6226(JIS X 0208)を複雑にシフトさせた](../Page/JIS_X_0208.md "wikilink")[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")として[Shift_JIS](../Page/Shift_JIS.md "wikilink")が誕生した。この符号化方式（を利用した拡張[符号化文字集合](https://ja.wikipedia.org/wiki/文字集合#符号化文字集合 "wikilink")）は、マイクロソフトによりMS-DOSにおける標準日本語コードとして採用され、「**コードページ 932 (CP932)**」という管理番号を与えられた。

しかし、マイクロソフトは、MS-DOSにおける唯一の日本語用コードページである「CP932」を、[OEM](../Page/OEM.md "wikilink")メーカーの自由に任せていた。そのため、NECの[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")、IBMの[PS/55 シリーズ](https://ja.wikipedia.org/wiki/PS/55 "wikilink")、[富士通](../Page/富士通.md "wikilink")の[FMRシリーズ](../Page/FMRシリーズ.md "wikilink")などは全て、MS-DOSを搭載し文字符号化方式もShift_JISを採用しているコンピュータであるにもかかわらず、登録されている文字集合がバラバラだった。

以下、代表的な2つの実装を解説する。

#### IBM

1983年、IBMは、日本語処理に重点を置いたデスクトップコンピュータ「[マルチステーション5550](https://ja.wikipedia.org/wiki/マルチステーション5550 "wikilink")」を発売する際、利用する符号化文字集合を以下のように定めた。

  - Shift_JISをベースとする。
  - JIS C 6226が規定する94区 × 94点の領域に拡張文字追加を行なわない。
  - 95 - 114区をユーザ外字領域とする。
  - 115 - 119区にJIS C 6226に非登録の[DBCS-Host](https://ja.wikipedia.org/wiki/IBM漢字 "wikilink")\[1\]文字を登録することで、DBCS-Hostの文字セット全体を表現する。
  - 2バイト文字部分だけの符号化文字集合の名称をDBCS-PCとし、コードページ番号\[2\]として「301」を割り当てる。
  - 1バイト・2バイト文字全体の符号化文字集合のコードページ番号として「932」を割り当てる。

こうしてできたDBCS-PCは1990年発売の[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")にも引き継がれることとなる。

#### NEC PC-9800

一方NECは、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に PC-9800シリーズの漢字処理オプション提供を開始した。特に、[MS-DOS](../Page/MS-DOS.md "wikilink")および[CP/M-86](https://ja.wikipedia.org/wiki/CP/M-86 "wikilink")搭載機における[漢字ROM](https://ja.wikipedia.org/wiki/漢字ROM "wikilink")に収容する文字集合を以下のように定めた。

  - Shift_JISをベースとする。
  - [JIPS](../Page/JIPS.md "wikilink")\[3\]の9 - 13区の特殊文字領域をそのままの区点番号で配置。
  - JIS C 6226-1978 非漢字・第一水準漢字・第二水準漢字はそのままの字形で、そのままの区点番号に配置。
  - IBM のメインフレームの「IBM 漢字 (DBCS-Host)」の中でJIS C 6226に登録の無い漢字をIBMのDBCS-PCと同様の並びで89 - 92区に配置\[4\]。DBCS-PCと違い、115 - 119区ではなく、GL表現も可能なように追加文字全てを 94区内に全て配置した。

### OEMコードページの統合

マイクロソフトは1993年、Windows 3.1の日本語版を出すにあたり、「CP932の誕生と発展」節で述べたように多様化した「CP932」の仕様をOEMメーカーの自由に任せるという方針を撤回した。日本の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")市場で、特に大きなシェアを持つ上記2社の統合コードをWindowsにおける日本語標準コードとし、また、これを[IANAに](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")「Windows-31J」という名で登録した。IANA登録名の「**Windows-31J**」とは、読んで字のごとく、「**Windows3.1 Japanese**」を意味している。IBMはマイクロソフトによる「CP932」の統合を受けて、「Windows-31J」と各文字のコードポイントまで同一にした「**CP943**」を策定し、同社のOSである[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")、[DBMSである](../Page/データベース管理システム.md "wikilink")[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")などに搭載している。

統合の概要は以下のとおりである。

  - マイクロソフトによるIBM & NEC統合の概要

:\* ベースとなる符号化文字集合としてJIS X 0208-1990を採用。

:\* NECが9 - 13区に登録していた特殊文字の内、13区のものだけを継承。この 13区登録の 83文字のことを「**NEC特殊文字**」と命名。

:\* NECが89 - 92区に登録していた漢字と非漢字は全て継承。このエリアの374文字のことを「**NEC選定IBM拡張文字**」と命名。

:\* IBMが115 - 119区に登録していた漢字と非漢字も全て継承。このエリアの388文字のことを「**[IBM拡張文字](https://ja.wikipedia.org/wiki/IBM拡張文字 "wikilink")**」と命名。

上記の統合以後は、「CP932」と言えば、マイクロソフトの技術文書以外でも、一般的に「Windows-31J」を指すようになった。しかし、統合前の文字セットが全く利用されなくなったというわけではない。例として、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")では、「CP932」がIBMの「CP932」を指し、「MS932」が「Windows-31J」を指す。JDK 1.4.1以降では「MS932」の代わりに「Windows-31J」というキーワードでも「Windows-31J」文字セットを指定できるようになっている。

## Windows-31J に重複登録されたコード

前節で触れたように、「Windows-31J」はNECとIBMのそれぞれのコードを統合して（互換性を維持する形で）作られた経緯があるため文字の重複があり、大まかに言えば「NEC選定IBM拡張文字」と「IBM拡張文字」がほぼまるごと重複している。漢字部分についていえば、すべての漢字がきっかり2つずつ登録されている。

以下、拡張文字を（非符号化）文字集合として詳しく見ると、まずNEC選定IBM拡張は漢字360文字と小文字のローマ数字、およびで構成されるが、これらはすべてIBM拡張に含まれる。IBM拡張はこのNEC選定IBM拡張に、大文字のローマ数字との計14文字を加えたものである。そしてこの差分の14文字はすべてNEC特殊文字にも含まれており、NEC特殊文字はこの14文字と、IBM拡張・NEC選定IBM拡張のいずれにも含まれない69文字で構成される。したがってNEC選定IBM拡張文字とNEC特殊文字を合わせると、過不足のない拡張文字の集合の全体になる。また、これらのうちでJIS X 0208:1990と重複するのは非漢字のみであり、それは3重複である「￢」「∵」の2文字と、NEC特殊文字との2重複である「≒」「≡」「∫」「√」「⊥」「∠」「∩」「∪」の8文字である。なお、JIS X 0208:1990の持つこれら10文字の重複はすべて、JIS X 0208:1983の段階で追加された文字である。

### 重複文字が含まれる領域

重複文字が含まれる領域は以下の表のとおりである。

| 文字種名                         | コードポイント（16進数表記） | 区番号        | 重複文字数     |
| ---------------------------- | --------------- | ---------- | --------- |
| JIS X 0208の非漢字（1983年追加文字）の一部 | \-              | 2区         | 10文字      |
| NEC特殊文字                      | 8740 - 879C     | 13区        | 22文字      |
| NEC選定IBM拡張文字                 | ED40 - EEFC     | 89 - 92区   | 374文字（全部） |
| IBM拡張文字                      | FA40 - FC4B     | 115 - 119区 | 388文字（全部） |

### 文字コード変換時の重複文字の影響

文字コード変換を行う際には、この重複文字というのは厄介になる。別の文字コードから、「Windows-31J」に変換する場合に、重複するどちらの文字へと変換するべきかが問題になる。

それに関して、WindowsのAPIの仕様における優先順位は、以下のようになっている。

1.  [JIS X 0208-1990の登録文字である場合は](../Page/JIS_X_0208.md "wikilink")、これに統一
      - 例 : 「**√**（ルート）」、「**∵**（なぜならば）」、「**￢**（否定）」
2.  「NEC特殊文字」「IBM拡張文字」が重複する場合は、「NEC特殊文字」に統一
      - 例 : 「****（ナンバー）」 、「****（かっこかぶ）」、「****（大文字ローマ数字の3）」
3.  「NEC選定IBM拡張文字」「IBM拡張文字」が重複する場合は、「IBM拡張文字」に統一
      - 例 : 「****（たちざき）」 、「****（はしごだか）」 、「****（小文字ローマ数字の 3）」

この基準に従って、[Microsoft IME](../Page/Microsoft_IME.md "wikilink") によって、「（かっこかぶ）」を入力しようとした場合には、IBM 拡張文字のコードである FA58<sub>16進</sub> ではなく、NEC 特殊文字としてのコードである 878A<sub>16進</sub> が引き当てられる。

| 文字種別         | 文字数                    | Windows-31J変換後に残る文字数   |
| ------------ | ---------------------- | ---------------------- |
| NEC特殊文字      | 83文字（非漢字83文字）          | 74文字                   |
| NEC選定IBM拡張文字 | 374文字（非漢字14文字、漢字360文字） | 0文字                    |
| IBM拡張文字      | 388文字（非漢字28文字、漢字360文字） | 373文字                  |
| 合計           | \-                     | 447文字（非漢字87文字、漢字360文字） |

JIS X 0208-1990の登録文字10文字（「≒」「≡」「∫」「√」「⊥」「∠」「∵」「∩」「∪」「￢」）をJIS78を基準した場合の機種依存文字として扱う場合がある。 \[5\]\[6\]

## インターネット上での Windows-31J の利用について

IANAのcharset登録簿には「Windows-31J」が登録されているが、「限定された、または特殊な使用のためのもの」とされており、インターネット上で用いることが推奨されるまでには至っていない。ただし、文字符号化方式として[Shift_JIS](../Page/Shift_JIS.md "wikilink")を用いてデータを交換しあう二者間において、明示的に使用が合意されている場合は、Windows-31Jを使っても問題が無い。

[Unicode](../Page/Unicode.md "wikilink")範囲を完全に表現可能な[UTF-8](../Page/UTF-8.md "wikilink")等の文字符号化方式を用いてデータの交換をする場合は、話が若干ややこしくなる。IBM拡張文字等のWindows-31J独自追加の文字は、他の[JIS X 0208非登録の](../Page/JIS_X_0208.md "wikilink")[CJK統合漢字](../Page/CJK統合漢字.md "wikilink")に比べて、異機種（OS / アプリケーション）間でのデータ交換を、[文字化け](../Page/文字化け.md "wikilink")を起こしたりせずにデータのやり取りが正常に行える確率が高いからである。これについては、デスクトップOSとしてのWindowsの普及率が非常に高いことも理由の1つである。[機種依存文字](../Page/機種依存文字.md "wikilink")の項も併せて参照のこと。

とは言え、UTF-8などのようなUnicodeの登録文字を全て利用できる文字符号化方式を利用している場合であっても、あえてJIS X 0208登録文字だけを用いてデータ交換を行った方が、問題が起こりにくい。

また、Unicodeに変換した際、一部の文字がShift_JISとは異なるコードに割り当てられていることでの文字化けを起こすことがある。[Unicode\#波ダッシュ・全角チルダ問題](https://ja.wikipedia.org/wiki/Unicode#波ダッシュ・全角チルダ問題 "wikilink")および[波ダッシュ\#Unicodeに関連する問題](https://ja.wikipedia.org/wiki/波ダッシュ#Unicodeに関連する問題 "wikilink")を参照のこと。

## 後の文字集合への影響

### NEC特殊文字・IBM拡張文字

NEC特殊文字や IBM拡張文字はもともとベンダの独断で作られた文字セットであるが、これがデファクトスタンダードとしての影響力を持った結果として 現在では各種の公的な規格でも全部または一部が採用されている。

#### NEC特殊文字

  - Windows-31J
    全83文字を、13区に収録。
    「≒」「≡」「∫」「√」「⊥」「∠」「∵」「∩」「∪」の9文字は2区にも重複して収録。
    「∵」の1文字はさらに115区にも重複して収録。
  - [Unicode](../Page/Unicode.md "wikilink")
    83文字全てを基本多言語 (BMP) 面に収録。
  - [JIS X 0212](../Page/JIS_X_0212.md "wikilink")-1990
    「№」の1文字を2区81点に収録。
  - [JIS X 0213:2004](../Page/JIS_X_0213.md "wikilink")
    「≒」「≡」「∫」「√」「⊥」「∠」「∵」「∩」「∪」の9文字は2区に収録。
    「 (N-ARY SUMMATION)」の1文字は収録されていない。6区18点のギリシャ大文字シグマ「Σ」で代用できるため。
    上記以外の 73文字はWindows-31Jと同一区点（1 区）上に収録。

#### IBM拡張文字

  - Windows-31J
    全388文字を、2ないし 3重複して収録。
  - [Unicode](../Page/Unicode.md "wikilink")
    388文字全てを基本多言語面 (BMP) に収録。ただし、などその一部は[CJK互換漢字](https://ja.wikipedia.org/wiki/CJK互換漢字 "wikilink")としての採用であり、[統合漢字において別の字体を標準とするコードポイントに包摂されているものである](../Page/CJK統合漢字.md "wikilink")。Unicodeに基づいてこれらの字体を特定的に使用したい場合には、統合漢字の[IVSを用いることが推奨されている](../Page/異体字セレクタ.md "wikilink")。
  - [JIS X 0212](../Page/JIS_X_0212.md "wikilink")-1990
    全388文字中280文字を収録。
    このうち漢字部分は全360文字中279文字を収録。
  - [JIS X 0213:2004](../Page/JIS_X_0213.md "wikilink")
    全388文字中304文字を収録。
    このうち漢字部分は全360文字中276文字を収録。
  - [富士通](../Page/富士通.md "wikilink") [JEF](https://ja.wikipedia.org/wiki/JEF漢字コード "wikilink")
    388文字全てを収録。
  - NEC [JIPS](../Page/JIPS.md "wikilink")
    388文字全てを収録。
  - [日立製作所](../Page/日立製作所.md "wikilink") [KEIS](https://ja.wikipedia.org/wiki/KEIS "wikilink") (90)
    「＇」「＂」以外の386文字を収録。
  - IBM [DBCS-Host](https://ja.wikipedia.org/wiki/IBM漢字 "wikilink")
    388文字全てを収録。
  - [三菱電機](../Page/三菱電機.md "wikilink") [JSII](https://ja.wikipedia.org/wiki/JSII "wikilink")
    388文字全てを収録。
  - [日本ユニシス](https://ja.wikipedia.org/wiki/日本ユニシス "wikilink") [Lets-J](https://ja.wikipedia.org/wiki/Lets-J "wikilink")
    388文字中 328文字を収録。

### JIS X 0208以外の公的規格にて登録のあるNEC特殊文字一覧

#### JIS X 0212-1990に登録されているNEC特殊文字（全部）

#### JIS X 0213:2004 に登録されているNEC特殊文字（全部）

### JIS X 0208以外の公的規格にて登録のあるIBM拡張文字一覧

#### 人名用漢字（2004年改正）に登録されているIBM拡張文字（全部）

#### JIS X 0212-1990に登録されているIBM拡張文字（全部）

#### JIS X 0213:2004に登録されているIBM拡張文字（全部）

### CP932に定義されているが、JIS X 0212・JIS X 0213にない文字

JIS X 0213で字形が包摂されているものも含む。

  -

## CP932の利用者定義領域

CP932においては、95 - 114区までの1880文字の領域が「**利用者定義領域**（[外字](../Page/外字.md "wikilink")領域）」となっている。

Unicodeとの変換について、[Windows APIの仕様では](https://ja.wikipedia.org/wiki/Windows_API "wikilink")、[BMP面の](../Page/基本多言語面.md "wikilink")[私用領域](https://ja.wikipedia.org/wiki/外字#JIS_X_0221_\(Unicode\)における外字 "wikilink") 6400文字分の領域の先頭から1880文字目までと、95 - 114区の当領域を1対1の[写像変換](https://ja.wikipedia.org/wiki/写像変換 "wikilink")するようになっている。

## Windows-31J以外のベンダ拡張シフトJIS

### アップルコンピュータのシフトJIS

[アップルコンピュータは自社のコンピュータのOSとしてMS](../Page/アップル_\(企業\).md "wikilink")-DOSやCP/M-86を採用しなかったが、[Macintosh](../Page/Macintosh.md "wikilink")が用いる文字コードとしてシフトJISを利用した。

そのMacintosh（[漢字 Talk](https://ja.wikipedia.org/wiki/Mac_OS "wikilink") 7.1 以降）搭載のシフトJISの9 - 15区にはアップルコンピュータ独自の特殊文字が登録されている。このエリアには13区が含まれるため、Windows-31Jの「NEC特殊文字」領域と被っている。文字の例を挙げれば、NEC特殊文字の「」は Apple特殊文字の「」が同じ[コードポイント](https://ja.wikipedia.org/wiki/コードポイント "wikilink")に登録されている。さらに、117区に「縦書き用文字」が登録されている点も Windows-31J と異なる。IBM拡張文字の領域は存在しない\[7\]。この文字コードについては、[MacJapanese](../Page/MacJapanese.md "wikilink") を参照のこと。

漢字Talk 6以前のMacintosh では、NEC互換のシフトJISが使われており、13区のNEC特殊文字もMacintosh上で利用できた。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")標準[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の[Safari](../Page/Safari.md "wikilink")では、Mac用シフトJIS (MacJapanese) で表示するのか、Windows-31Jで表示するのかを選択できる。

### 富士通のシフトJIS

[富士通](../Page/富士通.md "wikilink")のMS-DOS搭載コンピュータのOEMコードページ932として使われる文字コードに、「R90」というものがある。これはFMRシリーズで利用された。この符号化文字集合の特徴は、87 - 93区に「[OASYS](../Page/OASYS.md "wikilink") 拡張文字」の領域を持つことである。ベースとなる文字集合は[JIS X 0208-1990であるが](../Page/JIS_X_0208.md "wikilink")、第一水準漢字の中で「78⇔83非入替文字」でない漢字（203文字）の字形をJIS C 6226-1978に合わせてある点に特色がある。なお、富士通のマニュアル等では、「R90」のことを「SJIS (R90)」と呼び、「Windows-31J」のことを「SJIS (MS)」と呼んで区別している。

### iモードのシフトJIS

[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")は標準日本語コードにシフトJISを採用している。この文字集合においては[JIS X 0208-1990を以下のように拡張している](../Page/JIS_X_0208.md "wikilink")。

  - 13区にPC-9800シリーズ用の特殊文字が搭載されている。NEC選定IBM 拡張文字は搭載されていない。
  - 112 - 114区に[絵文字](../Page/絵文字.md "wikilink")を登録している。この 112 - 114区というのは、CP932における 95 - 114区にある1880文字のユーザ外字登録領域の最後尾の位置に当たる。

### 京セラ・AH-K3001V のシフトJIS

[京セラ](../Page/京セラ.md "wikilink")の[PHS](../Page/PHS.md "wikilink")・[AH-K3001V](../Page/AH-K3001V.md "wikilink")の搭載するシフトJIS は、9 - 13区にPC-9800シリーズ用の特殊文字が搭載されている。

## 文字コード 5C と 7E の文字について

文字コード 5C と 7E については、 とも  X 0201 とも違う文字が登録されている。日本人の多くが「文字」と呼んでいるものは実は、「-31J 文字」であるということも言われている。（しかし少なくとも[IANA](https://ja.wikipedia.org/wiki/IANA "wikilink")における -31J の定義は  X 0201を用いるものである）

<table>
<thead>
<tr class="header">
<th></th>
<th><p>5C</p></th>
<th><p>7E</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>（<a href="../Page/バックスラッシュ.md" title="wikilink">バックスラッシュ</a>）</p></td>
<td><p>˜ （<a href="../Page/チルダ.md" title="wikilink">チルダ</a>）</p></td>
</tr>
<tr class="even">
<td><p>X 0201</p></td>
<td><p>¥ （<a href="../Page/円記号.md" title="wikilink">円記号</a>）</p></td>
<td><p>¯ （<a href="../Page/オーバーライン.md" title="wikilink">オーバーライン</a>）</p></td>
</tr>
<tr class="odd">
<td><p>-31J</p></td>
<td><p>¥ （円記号）</p></td>
<td><p>˜ （チルダ）</p></td>
</tr>
</tbody>
</table>

## マイクロソフトが規定するCP932に関連があるコード

Eメールで用いるために7ビットコードで「Windows-31J」の文字集合（=[マイクロソフト標準キャラクタセット](../Page/マイクロソフト標準キャラクタセット.md "wikilink")\[8\]）を表現した「[CP50220](https://ja.wikipedia.org/wiki/ISO-2022-JP#ISO-2022-JPと非標準的拡張使用 "wikilink")」や、GR領域にマイクロソフト標準キャラクタセットを表現した「[CP51932](https://ja.wikipedia.org/wiki/EUC-JP#EUC-JPの亜種 "wikilink")」というものがある。これらは、マイクロソフトの[Internet Explorerや](../Page/Internet_Explorer.md "wikilink")、[EmEditor](../Page/EmEditor.md "wikilink")、[秀丸エディタ](../Page/秀丸エディタ.md "wikilink")などのWindowsアプリケーションで利用されている。

| IE6.0における表記          | マイクロソフトのコードページ | 文字集合と符号化方式                                                                                           |
| -------------------- | -------------- | ---------------------------------------------------------------------------------------------------- |
| 日本語（シフト JIS）         | CP932          | マイクロソフト標準キャラクタセットをシフト符号化表現                                                                           |
| 日本語 (JIS)            | CP50220        | マイクロソフト標準キャラクタセットを[RFC1468符号化表現](../Page/ISO-2022-JP.md "wikilink")                                  |
| 日本語 (EUC)            | CP51932        | マイクロソフト標準キャラクタセットをGR表現\[9\]                                                                          |
| Unicode              | CP1200         | [Unicode](../Page/Unicode.md "wikilink")を[UTF-16](../Page/UTF-16.md "wikilink") (Little Endian) で符号化 |
| Unicode (Big-Endian) | CP1201         | UnicodeをUTF-16 (Big Endian) で符号化                                                                     |
| Unicode (UTF-8)      | CP65001        | Unicodeを[UTF-8](../Page/UTF-8.md "wikilink")で符号化                                                     |

Internet Explorer 6.0（日本語版）における表記と Microsoft コードページの対応

## 脚注

## 関連項目

  - [Shift_JIS](../Page/Shift_JIS.md "wikilink")

  - [マイクロソフト標準キャラクタセット](../Page/マイクロソフト標準キャラクタセット.md "wikilink")

  - [機種依存文字](../Page/機種依存文字.md "wikilink")

  - [IBM漢字](https://ja.wikipedia.org/wiki/IBM漢字 "wikilink")

  - [文字コード](../Page/文字コード.md "wikilink")

  - [Unicode](../Page/Unicode.md "wikilink")

  - [EUC-JP](../Page/EUC-JP.md "wikilink")

  - [ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")

  - [アスキーアート\#日本での使用](https://ja.wikipedia.org/wiki/アスキーアート#日本での使用 "wikilink")

  - [文字化け](../Page/文字化け.md "wikilink")

  - [Shift_JIS-2004](../Page/Shift_JIS-2004.md "wikilink")

  -
## 外部リンク

  - [Microsoft Windows Codepage 932](http://www.microsoft.com/globaldev/reference/dbcs/932.mspx) ([Web Archiveのキャッシュ](http://web.archive.org/web/20070123191209/http://www.microsoft.com/globaldev/reference/dbcs/932.mspx))
  - \[<http://msdn2.microsoft.com/ja-jp/library/system.text.encoding(vs.80>).aspx Microsoft .NET Framework クラスライブラリ Encoding クラス\]
  - [Windows-31J情報](http://www2d.biglobe.ne.jp/~msyk/charcode/cp932/index.html)
  - [通信で使って良い文字、悪い文字](http://www.kt.rim.or.jp/~aotaka/pc/character.htm)
  - [cp932 to Unicode table](http://unicode.org/Public/MAPPINGS/VENDORS/MICSFT/WINDOWS/CP932.TXT)

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink") [Category:Windowsコードページ](https://ja.wikipedia.org/wiki/Category:Windowsコードページ "wikilink")

1.  メインフレームにて搭載されている符号化文字集合。単に「[IBM漢字](https://ja.wikipedia.org/wiki/IBM漢字 "wikilink")」と呼ばれることも多い。IBM コードページ300という管理番号が割り振られている。日本語カナ版EBCDIC（IBMコードページ290）と組み合わせて IBMコードページ930 として用いられたり、日本語英小文字版EBCDIC（IBMコードページ1027）と組み合わせてIBMコードページ939として用いられることが多い。
2.  マイクロソフトおよびIBMは、それぞれ独自に「コードページ\#\#\#（\#は数字）」という形で、符号化文字集合を管理している。また、同じ番号のコードページ同士が同じ文字集合を指しているわけではない。
3.  [JIPS](../Page/JIPS.md "wikilink")は、NECが[1979年](../Page/1979年.md "wikilink")に開発した[メインフレーム](../Page/メインフレーム.md "wikilink")用の日本語処理システムの名前だが、ここではそのシステムで使われる[符号化文字集合を以ってJIPSと呼ぶ](https://ja.wikipedia.org/wiki/文字集合#符号化文字集合 "wikilink")。JIPSでは「[JIS C 6226-1978](../Page/JIS_X_0208.md "wikilink")」がGLに呼び出され、その9 - 13区に特殊文字が実装され、また、GR領域に「G1集合」と呼ばれる[拡張漢字](https://ja.wikipedia.org/wiki/拡張漢字 "wikilink")領域が実装されている。
4.  NECとしては、JIPSのG1集合を収める方が建前として良かったのかもしれない。しかし、CP/M-86やMS-DOSなどの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) 搭載機においては、符号化方式としてシフトJISが前提だった。G1集合部分を収めるには配置制約を大きく受けることになるため断念したものと考えられる。また、漢字ROM容量の都合上、G1集合部分を収めても利用することは不可能だったとも考えられる。
5.  [Shift_JIS(CP932)でCSVダウンロードできるかな?(Windows機種依存文字) | Chibineko](https://chibineko.jp/t/N1Y_brNaRdOZYb7OMUBiQw)
6.  [既存COBOL資産を有効活用した事例紹介](http://www.cobol.gr.jp/knowledge/material/180413_report/02.pdf)
7.  マイクロソフトはこのコードに対して、コードページ10001という管理番号を付与している。
8.  本節では、マイクロソフト標準キャラクタセットが [JIS X 0208](../Page/JIS_X_0208.md "wikilink") のコードポイントを拡張する形で表現されているものと仮定した場合の説明を行っている。
9.  マイクロソフトは「CP51932」のほかに「CP20932」という [EUC-JP](../Page/EUC-JP.md "wikilink") に似たコードページを有している。「CP20932」は上位バイト A0<sub>16進</sub> - FE<sub>16進</sub>、下位バイト 20<sub>16進</sub> - 7E<sub>16進</sub> という 2 バイトの組み合わせを利用することで[補助漢字を表現する](../Page/JIS_X_0212.md "wikilink")。eucJP-openとの対応においては、「CP51932」よりも「CP20932」の方が、[レパートリの一致度が高い](../Page/文字集合.md "wikilink")。