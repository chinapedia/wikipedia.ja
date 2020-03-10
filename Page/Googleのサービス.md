> この記事は[Google](https://ja.wikipedia.org/wiki/Google)から翻訳されています。


**Googleのサービス**（グーグルのサービス）は、[Google](../Page/Google.md "wikilink")が提供する[ウェブサービス](https://ja.wikipedia.org/wiki/ウェブサービス "wikilink")、または[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")、[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink")[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")、[モバイル](https://ja.wikipedia.org/wiki/モバイル "wikilink")[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")を総じたもの。

## 検索機能

### 検索のシステム

Googleは、検索した文字列を含む[ウェブページ](../Page/ウェブページ.md "wikilink")の中で、適切と考えられるページを示すために、[ページランク](../Page/ページランク.md "wikilink")と呼ばれる[アルゴリズム](../Page/アルゴリズム.md "wikilink")を用いている。

ページランクアルゴリズムは、ウェブページの価値の指標（ページランク）を、そのページに[リンクしているページのページランクを加重した値に基づいて](../Page/ハイパーリンク.md "wikilink")、再帰的に計算するものである。つまり、ページランクアルゴリズム自体がウェブページの内容の有用性を評価しなくても、人間の作ったリンクの関係を利用することにより、人間の考えるウェブページの有用性とよく関連したランクを付けることができるのである。このアルゴリズムにより、利用者が有用と感じる検索結果を提供でき、高シェアの検索エンジンとなっていった。

また、Googleは、検索結果として表示する順番を決めるのに、ページランクに加えて、およそ百程度といわれる公開されていない基準も用いている。この多くの基準により、露骨な[検索エンジン最適化](../Page/検索エンジン最適化.md "wikilink")が施されているサイトが検索結果からほぼ一掃され、検索結果の品質を一定のレベルに保っている。公開されていない基準に関しては、コンピューターによる自動的な判定によるものではなく、人手により個別の判断がなされていると見られており、完全に人間の判断を排除したアルゴリズムではなくなっているという指摘もある。

ページランクを調べる方法としては、[Internet Explorerや](../Page/Internet_Explorer.md "wikilink")[Mozilla Firefox対応のGoogle](../Page/Mozilla_Firefox.md "wikilink") ツールバーをパソコンにインストールして表示する方法がある。ページランクは0-10までの11段階評価式となっており、日本以外では[アップルのトップページのランク](../Page/アップル_\(企業\).md "wikilink")10、日本のランク10のページとしては[慶應義塾大学](https://ja.wikipedia.org/wiki/慶應義塾大学 "wikilink")などがある（2006年11月時点）。

Googleは高品質の検索結果を提供するため、また、[WWWの](../Page/World_Wide_Web.md "wikilink")[インデックス化](https://ja.wikipedia.org/wiki/インデックス化 "wikilink")のために、1万台以上の[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")コンピュータを使用している。なお、使用している [ディストリビューションは](../Page/Linuxディストリビューション.md "wikilink")、コストパフォーマンスの追求のため、[Red Hat Linuxを独自にカスタマイズしたものである](../Page/Red_Hat_Linux.md "wikilink")。

インデックス化にはGooglebotという[クローラ](../Page/クローラ.md "wikilink")が用いられている。クローラは様々なページへのリンクを調査して、データベースに追加する新たなページを見つける。また、インデックス化されているページの更新も定期的に確認している。

このインデックスデータベースとウェブページのキャッシュのサイズは数[テラバイト](https://ja.wikipedia.org/wiki/テラバイト "wikilink")にも及ぶ。初期のクローラや[Webサーバ](../Page/Webサーバ.md "wikilink")は、ともに[Python](../Page/Python.md "wikilink")で書かれていた。現在では検索のメイン部分は[C++](../Page/C++.md "wikilink")によって書かれており、WebサーバにはGWSという専用のサーバソフトウェアが使われている。

なお、Googleのサーバに使われているコンピュータは当初、非常に安価（一般に市販されているコンピュータと同レベルかそれ以下）なものであった。近年では、より快適なレスポンスを実現するために、高価な[RAMディスク](https://ja.wikipedia.org/wiki/RAMディスク "wikilink")を使用したサーバを使用しており、必ずしも安価なサーバのみを使用しているわけではない。また、信頼性を高めるために徹底した多重化が図られている。Googleでは、非常に多くのサーバを使用している為に、毎日、故障した何十台ものコンピュータを交換・追加していたが、RAMディスクを使用するようになってからはハードディスクに起因する故障が激減した。なお、当初使用していたハードディスクを積んだサーバは[Gmail](https://ja.wikipedia.org/wiki/Gmail "wikilink")サービスに流用されていると見られている。

### アルゴリズムによる弊害

クローラを用いてウェブ全体からデータを集めて利用する検索エンジン（ロボット型検索エンジン）としては、初期のものとして[AltaVista](https://ja.wikipedia.org/wiki/AltaVista "wikilink")があり、その後、Googleが現れた。2004年5月31日には、[Yahoo\! JAPANの検索エンジンが](https://ja.wikipedia.org/wiki/Yahoo!_JAPAN "wikilink")、アメリカ本社開発のYahoo Search Technology（略されてYSTとも言われる）を使用したロボット型検索エンジンに切り替わった。

これは、各サイト間に貼られているリンクの質を解析し、その結果を元に各ウェブページにランクを付け、検索結果の表示順番を随時変更するという考え方により、Googleが、Googleが登場する以前の検索エンジンよりも検索キーワードに対して有用な検索結果を示せた為に、他でも類似の考えに基づいたロボット型検索エンジンが使用された結果である。

しかし、ウェブページに対する評価の主な方法は、そのウェブページに対して貼られているリンクの質や記述されている[HTMLの構造を解析するものであり](../Page/HyperText_Markup_Language.md "wikilink")、ウェブページの内容自体を評価するものではない。他の主なロボット型検索エンジンも、[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")時点では、ウェブページの内容自体の評価を検索結果の主な指標としてはいない。

そのため、多くのウェブサイト管理者は、サイトのランキング変化を観察したり、その変化の理由を知ることに興味を持つようになった。これらの事をきっかけに、検索結果の上位に掲載されるようウェブサイトをカスタマイズすることが商売になったり、検索結果上位を武器に単に他のサイトへ誘導を目的としたサイトや、ページランクを上げるためだけの意味の無いページなどが急増した。なお、ロボット型検索エンジンの特性を利用して、特定のウェブサイトを検索結果の上位に入れようとする行為自体は、Google登場以前にも行われていた。

これに対して、Googleを始めロボット型検索エンジンを使用する各社は、そのようなサイトに対しても適切な評価ができるように様々な工夫をしており、両者の攻防は続いている。詳しくは[検索エンジン最適化](../Page/検索エンジン最適化.md "wikilink")を参照のこと。

### 多言語への対応

現在、Googleが対応する言語の数は、64ヶ国語以上、128ヶ国語未満である。唯一[中国国内からのアクセスに限っては](../Page/中華人民共和国.md "wikilink")、検索が中国政府の検閲下となっており、中国政府に対して悪意があるとみなされるキーワード（「[天安門事件](https://ja.wikipedia.org/wiki/天安門事件 "wikilink")」など）は検索されないようになっている。中国版Yahoo\!や[AOL](https://ja.wikipedia.org/wiki/AOL "wikilink")など、中国に進出している検索エンジンは同様の処置が取られている。

### 「次の検索結果を表示しています」機能

**「脱出口システム/Escape Hatch」の次世代型モデル**として追加された検索結果ページ置換機能。提案者はMark Paskin。<ref><https://www.youtube.com/watch?v=J5RZOU6vK4Q>

「検索アルゴリズムの改善検証」</ref>

検索キーワードに間違いが含まれていると判断された場合、**「次の検索結果を表示しています/showing results for (xxxx) Search instead for (YYYY)」**という形でxxxxのキーワードの検索結果を表示するというもの。

(xxxxは、Googleが予測した修正後のキーワード、yyyyは元の検索キーワード)。ガイドラインにこの機能の掲載はない。

「もしかして:(**Did you mean:xxxx)**」機能の発展したより踏み込んだものと評するべきであろう。前述した「もしかして:」の場合、最初に間違ったキーワードの検索結果を表示して、修正後のキーワードのリンクを表示するだけなので、

正しいキーワードの検索結果をダイレクトに表示する現在のものとは仕様が異なる。現在は「もしかして：」機能よりも優先的にこのヘルプが発動するため、以前よりも表示の頻度が減ったといえる。

当初は、「就職しない」に対して「就職できない」を提案するなど、日本語の検索に関して適切でないキーワードを候補に挙げることが多かったため2004年11月に機能が削除されたが、2005年3月にはこの問題が改善された。

類似するものに、「○○も含めた検索結果を表示しています」があるが、2018年8月現在、少しでもGoogle側のサジェスト候補に反するものがあれば、「次の検索結果を表示しています」を表示していたこれ以前のサーチ結果と比較して、若干こちらの出現率が上昇した。

機械的な判断で検索者の意図した検索結果から離れてしまう事もあり、サジェストには「解除」「邪魔」(英語版ではstopほか)などのワードが並び、後述する「未指定」と並んでユーザーにはあまり快く思われていないのが現状であるが、エンジン開発者のひとりであるAmit singhalは、

「when you align google's interest with user's interest as we have aligned good things happen./我々のアイデアと検索者のニーズが合致した時、このような快い結果となるのです。」とこの機能を肯定的に評価している。

### 「キーワードの除外」機能

2014年半ばごろから散見されるようになった機能。複数のクエリの組み合わせで検索した際に、一つ、あるいは複数のクエリの上に打ち消し線が引かれ、ユーザーが入力したキーワードが無効化される。ガイドラインにこの機能の掲載はない。

ここでは長らく「未指定機能」としていたが、2018年7月10日ごろ、表示される文字列が「未指定」から「含まれない」に変更された為、暫定的に機能名を変更した。

機能の概要としては、「クエリを除外した検索結果が優先的に画面の上部に表示され、未指定/Missing:(リンクの下部に否定線のかけられたクエリ)とスニペット下に小さく表示され、一つ、あるいは複数の指定したクエリが無効化されてしまう」というものである。

出現する条件は不明だが、極端にヒット数が少ない場合、複数個の検索クエリを指定した場合に起こりやすい。2つ指定した場合、クエリが単一の場合でも、単語の一部のみを抽出して除外することもある。

おおそそが1ページ辺り1、2件程度ないし検索結果の改変が行われないが、多いときにはページの検索結果の大多数が「含まれない」のフィルターのかかったものとなる。

例を挙げると「周延」と検索した際の検索結果は約 1,420,000 件だが、これに「的」を追加して「周延的」とすると検索結果は約 1,360,000 件に減少するほか、

未指定: <s>的</s>とスニペット下に表示される記事（ヒット件数の水増しともとれる）が1ページ目に複数出現する。（これを回避するために「周延的」を囲って検索しても11万件もヒットする為、出現条件はエンジン側の独自のルーチンでなされている可能性が高い。）

指定した情報を求めるユーザーにとって、この機能はノイズとして機能しているものであり、完全一致検索などの強制力のある演算子を含まない限りはマイナーな情報になればなるほど意図した検索結果が必然的に導きづらくなるものである。

ダブルクォーテーションで任意のワードを囲い、クエリを検索結果に強制的に反映させることで、「次の検索結果を表示しています」、「未指定」のいずれも回避することができることがある。\[1\]。

指定した単語、文字のほとんどを除外された場合でも、未指定反映のされた検索結果には「入力したクエリと全く無関係なページ」「類似性のあるページ」「クエリを指定した場合に検索候補として表示されうるページ」のいずれも含まれえるため、この機能がどの程度検索結果に影響を及ぼしているかは未知数である。

なお、検索結果を改変するこの二つの機能を抑制するオプションは2018年12月10日現在、存在しない。

また、英語版Googleでは試験的な「指定した検索結果のみを表示する」機能が利用できる。

これは、「含まれない」が反映された検索結果の横に「クエリが含まれる検索結果のみを表示」というリンクがあるものであり、これをクリックすると「未指定」の結果を自動的に省いた検索結果のページに移行するものである。日本版では併記時点(2019年10月3日)は使用不可能。

### ウェブサイトのデザイン

Googleウェブサイトのトップページは、広告が掲載されていないなど、検索に不必要な情報が極力省かれたシンプルさが特徴である。Googleの人気が決定的なものになるに連れて、このトップページのシンプルさに対する評価も高まり、[AlltheWeb](https://ja.wikipedia.org/wiki/AlltheWeb "wikilink")など、これにならうようになった検索エンジンも現れた。

[ハロウィン](https://ja.wikipedia.org/wiki/ハロウィン "wikilink")、[クリスマス](https://ja.wikipedia.org/wiki/クリスマス "wikilink")、Google設立記念日、[オリンピック開催中など](../Page/近代オリンピック.md "wikilink")、何か特別な日には、トップページの「Google」の[ロゴが](https://ja.wikipedia.org/wiki/ロゴタイプ "wikilink")、その日に関係したものを使ってデザインされた「Google」のロゴ（通称:ホリデーロゴ）に替えられることがある。国限定だったりすることもある。また、ポップアップボックスも変化する。

ただし現在では、後述のiGoogleによって、シンプルなデザインとガジェットつきホームを選択できるようになっている。

### Google 画像検索

画像に付随するテキストや周辺のテキスト情報を利用して、画像を検索できる。画像をアップロードするか画像のURLをペーストして、類似した画像を検索する機能がある。

### Google ニュース

2002年9月には英語版が、2004年9月には日本語版ニュース検索サービスが開始された。このサービスは新聞社などのニュースサイトの記事を元に、最新ニュースを配信している。ニュースのトピックスのリンク先は各ニュースサイトとなっている。リンク先の記事の見出しや本文の一部などを利用しているが、Googleはリンク先サイトとは契約していない。

Google ニュースのトップページはカスタマイズが可能で、見たいニュース項目を選んだり、その表示数を調節したりできる。さらに、任意のキーワードを含むニュース項目を作ることもできる。そのほか、Google ニュースをキーワード別でメールに送信するGoogle アラートというサービスもある。

2009年12月現在、すべての言語が正式版である。

2004年4月頃、アメリカのGoogle ニュースを元に個人が[RSS](../Page/RSS.md "wikilink")を組んでウェブページで配信した所、その配信を行った個人に対しGoogleから苦情が出され、Google ニュースのRSS配信に関しては問題となった。しかし、Googleはユーザーの需要を考え、2005年8月10日から公式に英語版Google ニュースのRSS/[Atom配信を始めた](https://ja.wikipedia.org/wiki/Atom_\(ウェブコンテンツ配信\) "wikilink")。

### Google グループ

[ニュースグループ](../Page/ニュースグループ.md "wikilink")の検索機能。もともとはDeja.comの資産を買収したもので、その時点での[Usenet](https://ja.wikipedia.org/wiki/Usenet "wikilink")のニュースグループのデータ及び、その後に投稿されたデータを検索、閲覧できる。

### Google Scholar

[Google Scholarによる無料学術検索サービス](https://ja.wikipedia.org/wiki/Google_Scholar "wikilink")。他社の同様のサービスの多くは有料。

### 電卓機能

Google には、検索以外に、計算を行うことのできる「電卓機能」がある。

例えば、「1+1」を検索すると、その結果として「2」と表示される[1](https://www.google.co.jp/#q=1%2B1)。「\(i^i\)」のような高度な計算[2](https://www.google.co.jp/#q=i%5Ei%5Dや、単位換算%5Bhttps://www.google.co.jp/#q=3メートルは何フィート)[3](https://www.google.co.jp/#q=360km/hをm/sで)、[為替レート](../Page/為替レート.md "wikilink")換算の機能\[[https://www.google.co.jp/\#q=5万円をユーロで\]をも備えている](https://www.google.co.jp/#q=5万円をユーロで%5Dをも備えている)。

しかし、例外的に計算ではなく通常の検索が実行される場合がある。例えば「7-11」を計算させようとしても、「-4」とは表示されない。理由は[セブン-イレブン](../Page/セブン-イレブン.md "wikilink")が存在するためである。このようなときは、最後に「=」をつけて「7-11=」とすれば、検索しないで計算するようになる。また、この例の場合、「7- 11」や「7 -11」のように「-」の前後にスペースを入れることでも計算させることができる。

使用できる演算子としては次のようなものがある。

  - \+ または 足す または たす[4](https://www.google.co.jp/#q=2たす2)
  - \- または 引く または ひく[5](https://www.google.co.jp/#q=4ひく2)
  - \* または × または 掛ける または かける[6](https://www.google.co.jp/#q=3かける5)
  - / または ÷ または 割る または わる[7](https://www.google.co.jp/#q=6わる2)
  - √ または ルート[8](https://www.google.co.jp/#q=√3)
  - ^ または の_乗[9](https://www.google.co.jp/#q=3の3乗)

また、数学の定数や科学的な定数も答えてくれる。いくつか例を挙げると、

  - [万有引力定数](../Page/万有引力定数.md "wikilink") G[10](https://www.google.co.jp/#q=万有引力定数)
  - [重力加速度](../Page/重力加速度.md "wikilink") g[11](https://www.google.co.jp/#q=重力加速度)
  - [光速度](https://ja.wikipedia.org/wiki/光速度 "wikilink") c[12](https://www.google.co.jp/#q=光速度)
  - [プランク定数](../Page/プランク定数.md "wikilink") h[13](https://www.google.co.jp/#q=プランク定数)
  - [地球](https://ja.wikipedia.org/wiki/地球 "wikilink")の[質量](../Page/質量.md "wikilink")や[半径](../Page/半径.md "wikilink")に代表される既知の天体データ定数[14](https://www.google.co.jp/#q=月の半径)
  - [アボガドロ定数](../Page/アボガドロ定数.md "wikilink") N<sub>A</sub>[15](https://www.google.co.jp/#q=アボガドロ定数)
  - [ボルツマン定数](../Page/ボルツマン定数.md "wikilink") k[16](https://www.google.co.jp/#q=ボルツマン定数)
  - [円周率](https://ja.wikipedia.org/wiki/円周率 "wikilink") π[17](https://www.google.co.jp/#q=π)
  - [ネイピア数](../Page/ネイピア数.md "wikilink") e[18](https://www.google.co.jp/#q=e)

などがある。

これらの定数や単位換算を使用して実際に計算ができる。たとえば「4×円周率×地球の半径の2乗を畳で」と検索すると、地球の表面積が何[畳か計算させることができる](https://ja.wikipedia.org/wiki/畳_\(単位\) "wikilink")[19](https://www.google.co.jp/#q=4×円周率×地球の半径の2乗を畳で)。

さらにGoogleは「[生命、宇宙、そして万物についての究極の疑問の答え](https://ja.wikipedia.org/wiki/生命、宇宙、そして万物についての究極の疑問の答え "wikilink")」という質問に対しても回答してくれる[20](https://www.google.co.jp/#q=生命、宇宙、そして万物についての究極の疑問の答え)。

Google電卓機能と類似の機能を持つネット上の無料サイトとして、[Wolfram Alphaがある](https://ja.wikipedia.org/wiki/Wolfram_Alpha "wikilink")。こちらは[微分](../Page/微分.md "wikilink")[21](https://www.wolframalpha.com/input/?i=Derivative+of+gamma+function)、[積分](https://ja.wikipedia.org/wiki/積分 "wikilink")[22](https://www.wolframalpha.com/input/?i=integral+sin)、[定積分](https://ja.wikipedia.org/wiki/定積分 "wikilink")[23](https://www.wolframalpha.com/input/?i=integral+sin%28x%29+from+x%3D-pi+to+0)、[テイラー級数展開](https://ja.wikipedia.org/wiki/テイラー級数展開 "wikilink")\[[https://www.wolframalpha.com/input/?i=series+expansion+of+sin\]などの演算機能も実装しているが、2010年8月現在インターフェースは英語のみ](https://www.wolframalpha.com/input/?i=series+expansion+of+sin%5Dなどの演算機能も実装しているが、2010年8月現在インターフェースは英語のみ)。

### モバイル検索

携帯電話向けのページ検索も可能である。[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")の場合はドコモ非公式ページのみ検索できる。

### 検索演算子

検索語の前に「hogehoge:」を挿入することで、検索する範囲を狭めることができる。例えば、[日本国政府](https://ja.wikipedia.org/wiki/日本国政府 "wikilink")のウェブサイトのみから、題名に「ほげほげ」という単語が含まれる[PDF](https://ja.wikipedia.org/wiki/PDF "wikilink")ファイルを検索したい場合は「site:go.jp intitle:ほげほげ filetype:pdf」と入力して検索する。site: やintitle:、filetype: のほか、演算子の一覧は、公式のヘルプページを参照\[2\]。

  - "+" 多用されるため検索結果から無視される言葉（a how the whenなど）なども含めて検索する。
  - "OR" または。（例）[検索エンジン google OR yahoo](https://www.google.co.jp/#q=%E6%A4%9C%E7%B4%A2%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%B3+google+OR+yahoo)
  - "site:" 特定のサイト内だけに検索結果を制限する。（例）[site:ja.wikipedia.org google](https://www.google.co.jp/#q=site%3Aja.wikipedia.org+google)
  - ".." 数値範囲検索。（例） 1996..2010 FIFAワールドカップ
  - "allintitle:" すべての検索ワードがウェブページのタイトルに含まれているページを検索する。（例）[allintitle: google サービス](https://www.google.co.jp/#q=allintitle%3A+Google+サービス)
  - "intitle:" （例）[24](https://www.google.co.jp/#q=intitle%3Agoogle+search%20intitle:google%20search)。タイトルにgoogleが含まれていて、文中またはタイトルにsearchが含まれるページを検索する。コロンの後にスペースは入れない。
  - "allinurl:" 全ての検索ワードがURLに含まれているページだけを検索する。次の例だとこのページもヒットする。（例）[allinurl: wikipedia google](http://www.google.co.jp/search?q=allinurl%3A+wikipedia+google)
  - "inurl:" （例）[inurl:google search](https://www.google.co.jp/#q=inurl%3Agoogle%20search)。URLにgoogleが含まれていて、searchが文中またはURLに含まれているページを検索する。コロンの後にスペースは入れない。

<!-- end list -->

  - ヘルプ

<!-- end list -->

  - <https://support.google.com/websearch/answer/35890>
  - <https://support.google.com/websearch/answer/136861?hl=ja>

## Google日本（日本語）独自の検索機能

<https://www.google.co.jp> で出来る機能を紹介する。

### 路線検索

路線検索ができる。例えば[東京駅](https://ja.wikipedia.org/wiki/東京駅 "wikilink")から[大阪駅](https://ja.wikipedia.org/wiki/大阪駅 "wikilink")までの道のりを検索したい場合「東京から大阪」と検索すると、検索結果のトップに乗換情報が表示される。次の電車が出発するまでの残り時間がカウントダウン式に表示され、交通費も表示される。

### 会社情報検索、株価検索

「株価 ソニー」と検索すると、検索結果の先頭に「ソニー（株）の株価情報」のリンクが表示される。

なお、この機能を利用する為には、正式な会社名（（株）は省略できる）を入力しなければならない。

### 荷物検索

[ヤマト運輸](../Page/ヤマト運輸.md "wikilink")（[宅急便](../Page/宅急便.md "wikilink")）の伝票番号が検索できる。例えば12桁の「ヤマト \*\*\*\*\*\*\*\*\*\*\*\*」を検索すると、検索結果に「ヤマト運輸の荷物 \*\*\*\*-\*\*\*\*-\*\*\*\* を追跡」が返ってくる（\*は伝票番号）。その検索結果のリンクをクリックすると、ヤマト運輸のウェブサイトにて荷物の追跡が可能である。

  - その後、[佐川急便](../Page/佐川急便.md "wikilink")・[日本郵便](https://ja.wikipedia.org/wiki/日本郵便 "wikilink")の[ゆうパック](../Page/ゆうパック.md "wikilink")の12桁の伝票番号が、検索可能になった（佐川急便なら「佐川 \*\*\*\*\*\*\*\*\*\*\*\*」、ゆうパックなら「ゆうパック \*\*\*\*\*\*\*\*\*\*\*\*」を検索すると、検索結果の先頭に、宅急便同様の配送追跡結果が返ってくる）。

### プロ野球情報

「[野球](../Page/野球.md "wikilink")」と検索すると、プロ野球の試合結果やスケジュールが表示される。

### FIFAワールドカップ

「ワールドカップ」と検索すると、[FIFAワールドカップ](https://ja.wikipedia.org/wiki/FIFAワールドカップ "wikilink")の試合情報等がトップヒットで出てくる。

[2010 FIFAワールドカップでは](https://ja.wikipedia.org/wiki/2010_FIFAワールドカップ "wikilink")、最下部のGoogleの表示が『**Gooooooooooal \!**』と表示された。

## ウェブサービス

### Google マップ

[2004年](../Page/2004年.md "wikilink")、アメリカ、カナダ、英国のみで地図検索・表示機能を[Google マップとして公開した](https://ja.wikipedia.org/wiki/Google_マップ "wikilink")。[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")を使っていながら、まるで地図ソフトのように動作するのが特長である。2005年06月から全世界の概要地図が閲覧可能となった。

2004年10月に衛星写真閲覧ソフト会社のKeyholeを買収し、2005年4月よりアメリカの衛星写真も見えるようになった。ただし、アメリカの機密情報などを含んでいるために拡大できなかったり、モザイクがかかっている場所もある。表示される写真には、著作権の存在を示す為に、Googleのロゴが入っている。

その後2005年7月に、日本でもGoogle マップとGoogle ローカルのサービスをベータ版として開始した。Google マップでは地図情報（[ゼンリン](https://ja.wikipedia.org/wiki/ゼンリン "wikilink")と提携）とサテライト（衛星写真）がある。ただし、現在は一部を除いて、東京都や横浜市などの大都市のみ解像度が高く、他の地域は低解像度の表示しかできないが、徐々に高解像度な航空写真に差し替えが進んでいる。

また、Google ローカルでは、目的の場所（[タウンページ](../Page/タウンページ.md "wikilink")に載っている場所のみ）を検索し、結果をGoogle マップの地図上に示して表示してくれる。[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")など携帯電話でも利用可能である。

2005年10月に、Google マップとGoogle ローカルは統合され、サービスのブランド名はGoogle マップに統一された。

Googleマップ上に、手元の[GPS機器](../Page/グローバル・ポジショニング・システム.md "wikilink")（GPS付き[携帯電話](../Page/携帯電話.md "wikilink")でも可）で計測した位置情報をプロットすることも可能である。ただし、特定のフォーマット（\*.kml など）にデータを変換する必要があり、必要に応じてフリーソフトを使用する。GPSで計測した移動経路は水色で示される。

2007年2月28日には、アメリカ30都市の道路渋滞状況をリアルタイムで表示する機能が追加された。

2007年5月29日に、サンフランシスコやニューヨーク、ラスベガスの一部で、Street Viewが見られるようになった。これは、各都市の主要な道路から見た風景のパノラマ写真をGoogleマップ上で表示できるというもので、矢印をクリックすることで、移動したり方向転換したりできる。写真はGoogleの撮影班が1年がかりで撮影したものである。

2008年8月からは、日本でも[ストリートビューが見られるようになった](https://ja.wikipedia.org/wiki/Google_ストリートビュー "wikilink")。一部地域のみだが、東京23区などはほぼ網羅している。

### Gmail

[2004年](../Page/2004年.md "wikilink")[4月1日](../Page/4月1日.md "wikilink")に開始された[フリーメールサービス](https://ja.wikipedia.org/wiki/フリーメールサービス "wikilink")。[Webメール](https://ja.wikipedia.org/wiki/Webメール "wikilink")、[POP](../Page/Post_Office_Protocol.md "wikilink")、[IMAP](../Page/Internet_Message_Access_Protocol.md "wikilink")、[SMTPの各方式に対応し](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")、[電子メール](../Page/電子メール.md "wikilink")の転送もできる。サービス開始当時は招待状がなければ利用できなかったが、日本では[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[8月23日](../Page/8月23日.md "wikilink")より招待なしでも利用可能になった。Gmailモバイルの搭載により、携帯電話からでもアカウントが作成できるようになったが、氏名の入力から登録手続きが進めることができないという不具合が発生している。また、パソコン版でにおいても、希望するメールアドレスについての重複確認が正常に行えないという不具合が発生している。

[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")を採用していることで、操作性に優れている。各個人に対して2018年4月の時点では15[GB](../Page/ギガバイト.md "wikilink")\[3\]もの容量をほこり、今でも容量は増え続けている。メールの内容に応じた広告が表示されるのも特徴である。

### Google+

[2011年](../Page/2011年.md "wikilink")6月にテスト公開されたソーシャルネットワーキングサービス。[Facebook](https://ja.wikipedia.org/wiki/Facebook "wikilink")に対抗するものと位置付けられ、急速にユーザー数を拡大している。

### YouTube

Googleが提供する世界最大の動画共有サイト。2005年2月に設立し、2006年10月にGoogleに買収され、完全子会社となった。

動画再生はHTML5に対応しており、Flashが使えないモバイル端末でも、HTML5に対応したブラウザ上で再生できるようになっている。

### Google カレンダー

ウェブカレンダーシステム。[Gmail](https://ja.wikipedia.org/wiki/Gmail "wikilink")と連動している。自分自身のカレンダーをGoogleの検索結果に対してオープンにすることもできるし、仲間うちだけでグループウェア的に使用することもできる。公開されている専門カレンダーをオーバーラップ表示させることもできる。一番の特長としては、細かい時間設定で携帯電話/PCメール/デスクトップポップアップにアラートを飛ばせることが挙げられる。

### Google ドライブ

Googleの[オンラインストレージ](https://ja.wikipedia.org/wiki/オンラインストレージ "wikilink")サービス。ブラウザ上でさまざまなオフィスファイルを作成編集でき、保存することができる。

### Google 翻訳

### Google ブックス

### Google Play Music

[クラウド](https://ja.wikipedia.org/wiki/クラウド "wikilink")を利用した、音楽共有、保存サービス。 現在は英語版のみ。

### Blogger

[2003年](../Page/2003年.md "wikilink")2月に Pyra Labを買収し、運営している[多言語](../Page/多言語.md "wikilink")対応の[ブログ](../Page/ブログ.md "wikilink")サービスである。ブログ設定は[日本語](../Page/日本語.md "wikilink")を含め[英語](../Page/英語.md "wikilink")、[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink")、[ドイツ語](../Page/ドイツ語.md "wikilink")、[イタリア語](../Page/イタリア語.md "wikilink")、[ポルトガル語](https://ja.wikipedia.org/wiki/ポルトガル語 "wikilink")、[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")、[韓国語](https://ja.wikipedia.org/wiki/韓国語 "wikilink")に対応している。

### Google AdSense

Googleが行っているサイト運営者向けの[アフィリエイトプログラム](https://ja.wikipedia.org/wiki/成功報酬型広告 "wikilink")。申込型のサービスで、所定の手続きを経て認められれば、だれでも参加できる。クリック回数に応じて参加者にGoogleの売上げの一部が報酬として支払われる。

サイトの内容をGoogleのサーチエンジンで解析し、その内容を元に関連性の高い広告を配信する仕組みである。

以前は、報酬の支払いが、アメリカから[アメリカドルの小切手を送る方法がとられていて](../Page/アメリカ合衆国ドル.md "wikilink")、現金化する手数料が高いことや手続きが分かりにくいこともあり不評であった。これを受けて2005年8月から日本で銀行振り込みによる支払いが開始された。

クリスマス頃、一定の利益を上げた運営者には米Googleから、クリスマスプレゼントが届いている。

### Google 広告

Googleが行っている広告主向けの広告出稿サービス。Googleの検索結果やGoogle AdSenseを取り入れているサイト、また提携している複数のポータルサイトなどに、サイトの内容に適した広告を自動的に配信し表示する。[検索連動型広告](https://ja.wikipedia.org/wiki/検索連動型広告 "wikilink")と呼ばれるタイプ。

広告料はキーワードの組み合わせごとに1クリック単位でオークションによって決定する。また広告のクリック数が一定の割合を下回ってしまうと、その広告は表示されなくなってしまう。

このキーワードに対するオークション方式について、2005年2月に[ルイ・ヴィトン](https://ja.wikipedia.org/wiki/ルイ・ヴィトン "wikilink")がGoogleを訴え、結果として[商標](../Page/商標.md "wikilink")偽造、[不正競争](https://ja.wikipedia.org/wiki/不正競争防止法 "wikilink")、誤解を招くような広告が有罪となり、Googleに20万ユーロの罰金支払いが命じられた。この事件はGoogleの収入の多くが広告料である事や同業のYahoo\!も傘下のOvertureを通じて多額の収入を得るなどという状態であったため、検索エンジン業界に大きな影響を与えた。

### Google ウェブマスター ツール

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")7月より始められたベータ版のサービス(開始時の名称は　Google Sitemap)で、自分の管理するウェブサイトの更新やリンク構造などの情報をGoogleに送ることで、そのサイトの更新状態を早く検索結果に反映させたり、クロール（クローラーがサイトを調べること）を効率よく行わせることができる。そのほか、Googleにインデックスされたスパムサイトや、有料リンクの情報提供を行うことができる。また、いわゆる[グーグル八分](https://ja.wikipedia.org/wiki/グーグル八分 "wikilink")になった際の、再審査請求を行うこともできる。

### Google Analytics

2005年3月にGoogleが買収したUrchinなどの、通常だと1ヶ月400ドルするウェブ解析ソフトの無料提供を2005年11月より開始した。メインは効率の良いGoogle AdSenseの広告貼付を行うために解放しているが、Google AdSenseを利用していないウェブ管理者でも問題なく利用できる。なお、月間のデータ収集量には上限があるが、Google Adwordsの利用者は、上限なしで使用することができる。

### Google ビデオ

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[1月25日](../Page/1月25日.md "wikilink")より始められた動画検索、配信サービス。当初はアメリカのテレビ番組のみを配信するサービスだったが、後にはユーザーが投稿した動画など様々な動画を配信するようになった。

当初は、動画を再生するにはGoogle ビデオ専用のプラグイン「Google Video Viewer」をインストールする必要があった。しかし、動画のファイルフォーマットが[Flash Videoに変更されたため](https://ja.wikipedia.org/wiki/Flash_Video "wikilink")、[Adobe Flash Playerのみで動画が再生できるようになった](../Page/Adobe_Flash.md "wikilink")。一部であるが、[Windows Media Playerや](https://ja.wikipedia.org/wiki/Windows_Media_Player "wikilink")[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")、[PlayStation Portableなどで再生できるビデオ形式の動画を無料でダウンロードできるサービスも行っている](https://ja.wikipedia.org/wiki/PlayStation_Portable "wikilink")。

[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[1月9日](../Page/1月9日.md "wikilink")には動画コンテンツのダウンロード販売を行う「Google Video Store」を開始した。再生にはWindows専用のプレイヤー「Google Video Player」をインストールする必要があり、コンテンツの購入はアメリカ在住者に限られていたが、動画コンテンツの販売は[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")[8月15日](../Page/8月15日.md "wikilink")をもって終了し、それ以降は購入した動画コンテンツの視聴も一切不可能となっている。

[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[10月9日](../Page/10月9日.md "wikilink")に買収した子会社である [YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink") との最大の違いは、アップロード可能な動画のサイズや長さに全く制限が無いことであったが、[2009年](../Page/2009年.md "wikilink")[1月14日](../Page/1月14日.md "wikilink")に本サービスでの動画アップロード機能を廃止する旨が公表された[25](http://internet.watch.impress.co.jp/cda/news/2009/01/15/22105.html)。これに伴い、動画の公開は YouTube や [Picasa](https://ja.wikipedia.org/wiki/Picasa "wikilink")（Picasa ウェブアルバム）に一本化され、Google ビデオは YouTube や他の動画共有サイトの動画検索サービスを中心に展開することになった。

### Google Sites

[Google Sitesは](https://ja.wikipedia.org/wiki/Google_Sites "wikilink")、[Google Appsを利用した](https://ja.wikipedia.org/wiki/Google_Apps "wikilink")[Wiki](https://ja.wikipedia.org/wiki/Wiki "wikilink")およびWebページ作成ツール。

[Wixや](https://ja.wikipedia.org/wiki/Wix.com "wikilink")[WordPress](https://ja.wikipedia.org/wiki/WordPress "wikilink")と同様無料でWebページを作成することができるが、

無料版では、「Googleサイトの情報」がフッター（下部）に表示される。

また独自ドメインを設定できない。

1ユーザーあたり月額500円(年間6000円）の有料版もある\[4\]。

### Google Finance

[Google Financeは](https://ja.wikipedia.org/wiki/Google_Finance "wikilink")、2006年[3月21日](https://ja.wikipedia.org/wiki/3月21日 "wikilink")より始められた、株式市場情報を提供するベータ版のサービス。日本語のサービスは提供されていない。

[Flashを用いた柔軟なインタフェースを持ち](../Page/Adobe_Flash.md "wikilink")、役員の経歴やニュース記事と連動した（アメリカ市場などの）株価(および為替など)の推移を見ることができるなどの特徴がある。

#### 携帯電話での閲覧・記入

  - Google自体のモバイル版を使用
  - [Google Calendar Mobile Gateway](https://ja.wikipedia.org/wiki/Google_Calendar_Mobile_Gateway "wikilink")、あるいは[TAKE24/7](https://ja.wikipedia.org/wiki/TAKE24/7 "wikilink")などのWebアプリケーションを使用

### Google Patent Search

米国特許の検索サービス。

### Google URL Shortener

[2009年](../Page/2009年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")に開始した[短縮URL](https://ja.wikipedia.org/wiki/短縮URL "wikilink")サービス。Google URL Shortenerでは、Googleのインフラを利用した安定性と高速性に加え、Google検索のインデックスと同様に悪意のあるWebサイトのURLを検出し警告する安全性を謳っている。

## デスクトップアプリケーション

### Google Chrome

[Blinkを使用した](https://ja.wikipedia.org/wiki/Blink_\(レンダリングエンジン\) "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")。2008年9月2日にベータ版として公開され、同年12月12日に正式バージョンが公開された。[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") [XP](../Page/Microsoft_Windows_XP.md "wikilink")･[Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")･[7](../Page/Microsoft_Windows_7.md "wikilink")･[Mac](../Page/Macintosh.md "wikilink")･[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")上で作動する。

### Google 日本語入力

2009年12月3日にベータ版として公開された[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用の日本語入力ソフトウェア（[インプットメソッド](../Page/インプットメソッド.md "wikilink")）。 Googleは、主として[Windows向けに](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、以下のような[ローカルアプリケーション](https://ja.wikipedia.org/wiki/デスクトップアプリケーション "wikilink")（自分のコンピュータにインストールする必要があるアプリケーション）を提供している。

### Google ドライブ

Google ドライブのデスクトップアプリケーション版である。パソコンのファイルエクスプローラー上にはGoogle ドライブというクラウドストレージ専用のフォルダが作成され、通常のファイルエクスプローラーと同様の操作ができる。

### Picasa

2004年7月にPicasa社を買収し、配布されているデジタル写真管理ソフトである。画像のコントラストや明るさの変更、画像の回転や、画像の検索やソートする機能、CDやDVDに画像をバックアップする機能などを備えており、無料で利用できる。2005年9月20日にPicasa 2の日本語版がリリースされた。

2006年5月24日には、[Wine](https://ja.wikipedia.org/wiki/Wine "wikilink")を利用したPicasaのLinux版の提供も開始された。これは、Wineの改修をGoogleが[Code Weaversに依頼して作り上げたもので](https://ja.wikipedia.org/wiki/Code_Weavers "wikilink")、インストール時点で専用のWineが導入され、これにより、Windows版とほぼ同じ動作を実現している。

ここで開発されたWineのパッチはWineのソースツリーに対するパッチとして公開され、後々のリリースに含まれることになる。

### Google Earth

Google Earthは、世界中の地図や衛星写真を自由に閲覧できるソフト。これは[アメリカ航空宇宙局 (NASA)が配布している](../Page/アメリカ航空宇宙局.md "wikilink")「NASA World Wind」とほぼ同じ動作をしているが、NASA World Windと比較すると、低スペックのPCでも動くという特徴がある。

有料で[GPSとの連携や地図データから表計算ソフトへのデータエクスポート](../Page/グローバル・ポジショニング・システム.md "wikilink")、そして無料版に比べて高解像度の画像印刷が可能になるなどの機能を提供している。

[Windows 2000と](../Page/Microsoft_Windows_2000.md "wikilink")[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")（2005年6月28日からベータ版が配布され、2006年1月10日に正式版がリリース）、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")（2006年1月10日ベータ版配布開始）および [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") で動作する。

2006年9月14日より日本語版の配布が開始された。

Google Earth 上に特定の情報を重ねる「レイヤ機能」等が搭載されており、Google Earth の左側に表示されているレイヤの「建物の3D表示」で、建物が3Dで表示される。

世界各地の鮮明な衛星写真を全世界に提供しているので、各国の軍事施設や核関連施設などといった機密情報にあたるものも見ることができる。このため、テロリストへ重要情報を提供することになると、[インド](../Page/インド.md "wikilink")などが非難の声を上げている。

他にも[韓国](https://ja.wikipedia.org/wiki/韓国 "wikilink")が[日本海](../Page/日本海.md "wikilink")の名称に異議を唱えたりとしたが「内政の都合上の地理的な区分」は最終的には政治的な問題であるために玉虫色の対応をしている。

### Google Dashboard Widgets for Mac

Google Dashboard Widgets for Macは名前の示すままにmacOS（[Mac OS X v10.4以上](../Page/Mac_OS_X_v10.4.md "wikilink")）専用の[Dashboard](https://ja.wikipedia.org/wiki/Dashboard "wikilink")（ミニアプリケーション）である。2006年2月11日より公開されており、「Gmailボックス状況の同期」・「検索履歴の同期」の二つのWidgetからなる。

### Google SketchUp

Google SketchUpは、2006年3月に@Last Software社を買収し、配布されている3Dモデリングソフトである。簡単な立体物から、歴史的建造物のような複雑な構造物まで、オブジェクトを作画することができ、3次元的に回転させ裏側を見ることもできる。作成したデータはGoogle Earth上に表示できる。

### Google ツールバー

Google ツールバーは、[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 6.0以降で使用可能な検索用ツールバー。Googleの各種サービスをツールバーから直接利用できるほか、[ポップアップブロック](https://ja.wikipedia.org/wiki/ポップアップブロック "wikilink")などの機能も備えている。

なお、一部のフリーソフトをインストールすると必要がなくとも半強制的にインストールされる場合もあるので注意が必要である（インストーラの初期設定では当該フリーソフトと同時インストールされるので、不要な場合は自分で設定を変更する必要がある）。

ちなみに[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")の[WidgetにもGoogle](https://ja.wikipedia.org/wiki/ウィジェット "wikilink") Toolbarと呼ばれるものが存在するが、これはGoogleが公式に提供するものではなく、機能も公式版とは異なるものである。

当初はFirefox用のツールバーも提供されたが、2014年に提供が終了している。

  - Internet Explorer版
    Windows版でのみ使用可能。履歴を記憶したりキーワードをハイライトしたりできる検索機能、マウスオーバー辞書、PageRankの参照、ポップアップブロックなどを搭載している。
  - Mozilla Firefox版 <small>（サービス終了）</small>
    [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")の各OSに対応したFirefoxで利用可能。主な機能や設定画面の構造はInternet Explorerと同一だが、Firefoxに最適化された仕様となっているため細部の機能が異なる。
    2011年7月、Firefox 5 以降のバージョンには対応しないと発表\[5\]した。
      - IE版とFirefox版との違い
    <!-- end list -->
      - ポップアップブロック機能 - IE版のみの機能。Firefox版ではFirefoxそのものがポップアップブロック機能を有するためこの機能は省略されている。
      - [フィッシング詐欺警告機能](https://ja.wikipedia.org/wiki/フィッシング_\(詐欺\) "wikilink") - Firefox版のみの機能。Firefoxの1.5系列までで利用可能だった。Firefox 2.0ではこの機能が搭載されているためオプションは表示されない。
      - [フィードリーダー](https://ja.wikipedia.org/wiki/フィードリーダー "wikilink")機能 - IE版のGoogleツールバーバージョン4以降にも存在する機能だが、Firefox版の場合Firefoxのライブブックマークなどとも連携できるようになっている。Firefox 2.0に同等の機能が装備されたため、Firefox版Googleツールバーバージョン3以降はFirefox 2.0にインストールするとこの機能が無効化されるようになっていた。

## モバイルアプリケーション

### Google 検索

Googleで検索できるモバイルアプリケーション。テキストと音声検索機能と、ユーザーの行動に基づいて情報を表示するGoogle Now機能を備える。音声検索は、「Ok,Google」という音声コマンドにも対応している。Android版は、ホームスクリーンにウィジェットを配置できる。

マイマップを閲覧する「Google Maps Engine」というアプリケーションを別で提供している。

### Google マップ

検索、ルート検索、経路検索、ストリートビューなどのウェブ版の機能に加えて、カーナビ機能としてGoogle マップナビを搭載している。またGoogle Nowとの連携や、建物内の地図を閲覧するインドアビューで階を選択できるなど、モバイル版のみで使える機能がある。

### Google Earth

### Google Chrome

AndroidとiOSに対応したブラウザアプリケーション。予めGoogleのサーバーでデータ圧縮されたサイトを表示する「データ節約」機能や「音声検索」、外国語のサイトを母国語に翻訳する「翻訳」機能を備える。

HTML5に対応しており、サイト内に埋め込まれたHTML5ビデオを直接再生できるようになっている。

### Google 日本語入力

### Google 翻訳

カメラで撮影した写真から文字を読み取って翻訳するモバイル向け機能を持つ。

### YouTube

YouTubeをモバイル端末で見られるようにモバイルアプリケーションで提供されている。AndroidとiOSに対応する。

動画投稿者向けに、統計情報やチャンネルの管理ができる**YouTube Creator Studio**や、[Google TV向けの](https://ja.wikipedia.org/wiki/Google_TV "wikilink")**YouTube for TV**というアプリも提供されている。

### Google ドライブ

Google ドライブのモバイルアプリケーション版である。GoogleドキュメントやGoogleスプレッドシートでオフィスファイルを作成でき、作成したファイルはGoogle ドライブに保存される。

### Google ドキュメント

モバイル端末でドキュメントファイルを作成するためのアプリケーション。作成したファイルはGoogle ドライブに保存され、PDF形式でダウンロードできる。

### Google スプレッドシート

モバイル端末でスプレッドシートを作成するためのアプリケーション。作成したファイルはGoogle ドライブに保存され、PDF形式でダウンロードできる。

### Google スライド

モバイル端末でプレゼンテーションを作成するためのアプリケーション。

### Quickoffice

Googleドライブと連携するオフィスアプリケーション。

### Google Keep

カードで表示するメモアプリケーション。場所で通知するリマインダー機能を備えているのが特徴。

### Googleカレンダー

### Gmail

### Google ハングアウト

SMSやビデオチャットなどの機能を持つ、統合メッセージングアプリケーション。

### Google Play

Android向けのアプリケーションを提供するマーケットアプリケーション。

### Chromecast

端末をChromecastと接続するためのアプリケーション。

### My Tracks

GPSを使って、ウォーキング、ランニング、自転車などの走行記録をとるフィットネスアプリケーション。

### Find My Device

Android端末の場所を、別の端末やPCから探し出すアプリケーション。

### Googleカメラ

### Google TalkBack

端末の操作を補助するための、[視覚障がい者](https://ja.wikipedia.org/wiki/視覚障がい者 "wikilink")向けアプリケーション。

### Google Cloud print

### Quick, Draw\!

### Google Classroom

## 終了したサービス

### 検索機能

#### Google ディレクトリ

Googleの提供するディレクトリ検索サービス。もともとは「[Open Directory Project](https://ja.wikipedia.org/wiki/Open_Directory_Project "wikilink")」によって構築されたもので、それをGoogleが自社サービスに組み込んだもの。紹介文などの検索ができる。

2011年7月20日にサービス終了した。\[6\]

### ウェブサービス

#### Google Buzz

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[2月10日](../Page/2月10日.md "wikilink")にサービスが開始された、[ソーシャルサービス](https://ja.wikipedia.org/wiki/ソーシャルサービス "wikilink")。 [Twitter](https://ja.wikipedia.org/wiki/Twitter "wikilink")に類似しているが、文字数制限がない、他のサービス（[Google Buzzを参照](https://ja.wikipedia.org/wiki/Google_Buzz "wikilink")）の更新を[Google Buzz上に反映することができるなど](https://ja.wikipedia.org/wiki/Google_Buzz "wikilink")、[Twitter](https://ja.wikipedia.org/wiki/Twitter "wikilink")にはない機能もある。

同サービスはGoogle+に統合し、サービス終了した。投稿内容はアーカイブが作成され、Google ドライブに移動された\[7\]。

#### iGoogle（Google パーソナライズドホーム)

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[5月19日](../Page/5月19日.md "wikilink")（日本語版は[11月4日](../Page/11月4日.md "wikilink")）より始められたサービス。旧称Google パーソナライズドホーム。ニュースやGmail、ブックマーク、さまざまな[RSS](../Page/RSS.md "wikilink")フィードを[モジュール](https://ja.wikipedia.org/wiki/モジュール "wikilink")として、ユーザーが自分の[ウェブサイト](../Page/ウェブサイト.md "wikilink")に自由に配置できる。Google マップでも話題になったAjaxという技術が活用され、デベロッパーからも高い評価を得ている。

2005年12月14日からはGoogle Homepage APIが公開され、モジュールをユーザー自身が開発できるようになった。

2007年5月1日から現名称のiGoogleとなるとともに、テーマ選択等の新機能が追加されている。

2007年7月4日からは、iGoogleガジェットコンテストが行われ、締め切りの10月1日までに172作品が応募された。

2013年11月1日をもって、サービス終了した。

#### Google Page Creator

[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[2月23日](https://ja.wikipedia.org/wiki/2月23日 "wikilink")より始められたWeb作成サービス。ログインにはGmailのアカウントが必要である。100MBまでのWebサイトで、生成されるドメインは「http://\[Gmailのアカウント\].googlepages.com/」という形である。41種類のページデザインと4種類のレイアウトパターンがあり、直接htmlを書くことも可能。 2009年にサービス停止し、Google Sitesサービスに移行している。

#### Google Labs

[2002年](../Page/2002年.md "wikilink")[5月22日](../Page/5月22日.md "wikilink")より開始された、Googleが作成中の様々な新技術を公開するページ。当初は英語版のみであったが、後に多言語化されている。[Google マップ](https://ja.wikipedia.org/wiki/#Google_マップ "wikilink")、[iGoogle](https://ja.wikipedia.org/wiki/#iGoogle（Google_パーソナライズドホーム） "wikilink")、[Googleリーダー](https://ja.wikipedia.org/wiki/Googleリーダー "wikilink")など数多くのサービスがここから正式に採用されている。

ある単語がGoogleでどれだけ検索されているかをグラフ化したり、国や都市などでどの単語が最も多く検索されているかランキングしたりする[Google Trends](https://ja.wikipedia.org/wiki/Google_Trends "wikilink")、[Firefox用の拡張機能である](../Page/Mozilla_Firefox.md "wikilink")[Google Browser Syncなどがある](https://ja.wikipedia.org/wiki/Google_Browser_Sync "wikilink")。2006年10月5日、[Google Code Searchを公開した](https://ja.wikipedia.org/wiki/Google_Code_Search "wikilink")。

[2011年](../Page/2011年.md "wikilink")[7月20日](../Page/7月20日.md "wikilink")、GoogleはGoogle Labsを終了すると発表した\[8\]。2011年8月現在、Labs内の各プロジェクトについて開発継続するか終了するかの判断を行ない、整理している状態にある\[9\]。

#### Google ノートブック

ユーザーが、メモや、閲覧中のウェブサイトの情報などを書き留めておき、Googleアカウントに保存できるサービス。当初Google Labs内で英語のみで運用されていたが、[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")3月に正式運用開始、同時に多国語（日本語を含む）でのメニュー表示も可能となった。[2009年](../Page/2009年.md "wikilink")の初頭で、GoogleはGoogleノートブックの開発を中止することを宣告。[2011年](../Page/2011年.md "wikilink")9月にはサービス提供終了が発表\[10\]された。

#### Google Web Accelerator

[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")[5月4日](https://ja.wikipedia.org/wiki/5月4日 "wikilink")より開始されたサービス。これは、[Internet Explorer](../Page/Internet_Explorer.md "wikilink") (IE) または[Firefoxを利用するWindowsユーザーを対象に](../Page/Mozilla_Firefox.md "wikilink")、Googleが持つ巨大な[インターネット・キャッシュ](https://ja.wikipedia.org/wiki/インターネット・キャッシュ "wikilink")を使って接続を高速化するもの。目的のページに接続する前にいったんGoogleに対してリクエストを投げることで、Webアクセスを最適化する。具体的には、上記のGoogleネットワーク活用の他に「頻繁に閲覧されるページのキャッシュ」「前回見たページの状態から差分のみのダウンロード」「ページの先行読み込み」「Web接続の管理」「GoogleサーバからユーザーPC間の転送データの圧縮」といった工夫が行われている。

ダウンロード提供は既に終了されている。

#### Google Wave

2009年にテスト公開された[ソーシャルネットワーキングサービス](https://ja.wikipedia.org/wiki/ソーシャルネットワーキングサービス "wikilink")。2010年に正式公開されたが利用者が伸びず、わずか3ヶ月で開発が停止された。

#### Google Sync

パソコンやスマートフォンのデータを同期するサービス。2013年1月30日をもって、サービス終了した。

現在は、標準でGoogleアカウントから同期する機能がある。

#### Googleリーダー

Googleが無料提供していたWebベースのフィードリーダー。オンラインまたはオフラインでAtomおよびRSSのフィードを読むことができる。 事前の予告通り2013年7月1日にサービスは終了した。

### デスクトップアプリケーション

#### Google デスクトップ

2004年10月よりパソコンのファイルをCPUに掛ける負荷が少なく、時間も掛からず検索できる「Google デスクトップ」ツールの英語版が公開された。「Google デスクトップ」ツールを利用したいパソコンにインストールすることで動作し、検索結果はブラウザで表示される。

2005年3月には、日本語用のベータ版が公開され、その2か月後には正式版が公開された。2005年10月にはバージョン2.0へバージョンアップされ、サイドバー画面でニュースや新着メール、Windowsのタスク状況まで見られるようになった。しかし、このソフトウェアはファイルへのアクセスを非常に容易にすることから、簡単にパソコンの個人情報が流出する危険性があると指摘されている。

2006年8月にはバージョン4へバージョンアップし、[ガジェット](https://ja.wikipedia.org/wiki/ガジェット "wikilink")で機能を作成し、追加できるようになった。

2007年4月、[Mac OS X v10.4に対応したバージョンが公開された](../Page/Mac_OS_X_v10.4.md "wikilink")。

2011年9月、その役割を終えたとしてサービスを終了\[11\]した。

#### Google トーク

2005年8月24日からインスタントメッセンジャー[Google トークのベータ版を公開している](https://ja.wikipedia.org/wiki/Google_トーク "wikilink")。Windows Server 2003、Windows XP/2000/Vista/7に対応し、無料で利用できる。利用するにはGmailのアカウントが必要である。

専用のインスタントメッセンジャーソフトのほか、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の[iChat](https://ja.wikipedia.org/wiki/iChat "wikilink")など[XMPPプロトコルに対応したメッセンジャーソフト](https://ja.wikipedia.org/wiki/Extensible_Messaging_and_Presence_Protocol "wikilink")、GmailのWeb画面からも利用することが可能。

2013年5月をもって[Google+ ハングアウトと入れ替わる形でサービス終了](https://ja.wikipedia.org/wiki/Google+_ハングアウト "wikilink")。

#### Google パック

Googleや他の企業が提供するソフトを1つにまとめ、一括でインストールすることを可能にしたソフト。複数のソフトからユーザーが必要とするものを任意に選択し、インストールすることができる。また、Googleパックの管理画面から各ソフトバージョンアップを行うことが可能。

英語版は2006年1月6日に、日本語ベータ版は2006年7月7日に公開された。2011年9月に提供を終了した\[12\]。

#### Google Cloud Connect

[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") [Microsoft Office](../Page/Microsoft_Office.md "wikilink") 2003、2007、2010向けの[クラウドコンピューティング](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink")プラグイン。[Microsoft Wordドキュメント](../Page/Microsoft_Word.md "wikilink")、[PowerPointプレゼンテーション](https://ja.wikipedia.org/wiki/Microsoft_PowerPoint "wikilink")、[Excelスプレッドシートのファイルに対応し](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、[Google DocsフォーマットもしくはMicrosoft](https://ja.wikipedia.org/wiki/Google_Docs "wikilink") Officeフォーマットで[Google Docsへ自動的に保存や同期することができる](https://ja.wikipedia.org/wiki/Google_Docs "wikilink")。

「2回めの春の大掃除」と題された[2013年](../Page/2013年.md "wikilink")[3月13日](../Page/3月13日.md "wikilink")の発表で、同年[4月30日](../Page/4月30日.md "wikilink")に廃止されることとなった\[13\]。\[14\]。

### モバイルアプリケーション　

### Google+

Googleソーシャルネットワークサービスのモバイルアプリケーション。AndroidとiOS向けに提供されていた。モバイル端末で撮影した写真をGoogle+にバックアップする機能を持っていた。2019年4月12日に提供を終了した。

## 脚注

### 注釈

### 出典

## 関連項目

  - [Google](../Page/Google.md "wikilink")
  - [Google Authenticator](https://ja.wikipedia.org/wiki/Google_Authenticator "wikilink")

## 外部リンク

  - [Google のサービス](https://about.google/intl/ja/products/)
  - [Google ヘルプ](https://support.google.com/)

[Category:Googleのサービス](https://ja.wikipedia.org/wiki/Category:Googleのサービス "wikilink")

1.  ただし、絶対に「未指定」が回避されるわけではなく、完全一致オプションを適用し、-missing -未指定 -含まれない などを加えて設定したとしても表示されることがある。
2.  [ウェブ検索の精度を高める](https://support.google.com/websearch/answer/2466433) - Google検索 ヘルプ
3.
4.   発注業者比較なら【アイミツ】|accessdate=2018-04-05|website=imitsu.jp|language=ja}}
5.
6.  [Googleディレクトリ、サービス終了](http://ascii.jp/elem/000/000/621/621263/)
7.  [Google バズの廃止](https://support.google.com/mail/answer/1698228?hl=ja)
8.
9.
10.
11.
12.
13.
14.