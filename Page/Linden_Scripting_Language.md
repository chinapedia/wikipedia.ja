> この記事は[Linden Scripting Language](https://ja.wikipedia.org/wiki/Linden_Scripting_Language)から翻訳されています。


**Linden Scripting Language**(**LSL**)は[リンデン・ラボ](../Page/リンデン・ラボ.md "wikilink")が運営している仮想世界[Second Lifeでユーザが使用できる](https://ja.wikipedia.org/wiki/Second_Life "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。LSLによってSecond Life内のオブジェクトの挙動をコントロールすることができ、また[電子メール](../Page/電子メール.md "wikilink")、[XML-RPC](../Page/XML-RPC.md "wikilink")、[HTTPリクエスト送信によって外部](../Page/Hypertext_Transfer_Protocol.md "wikilink")[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")との通信も行なえる。

LSLは[C言語](../Page/C言語.md "wikilink")に近い文法構造を持ち、非常に[強い型付けの言語である](https://ja.wikipedia.org/wiki/型システム#強い型付けと弱い型付け "wikilink")。有限状態マシン（[有限オートマトン](https://ja.wikipedia.org/wiki/有限オートマトン "wikilink")）をモデルにした「状態(State)-[イベント駆動型スクリプト言語](../Page/イベント駆動型プログラミング.md "wikilink")」といえる。

## LSLの構造

スクリプトは[変数](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")、[関数定義](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")、1個以上の状態（ステート）、から構成される。各ステートには、そのステートにある場合に起こったイベントにどう反応するかが記述される。

基本データ型は[整数型](https://ja.wikipedia.org/wiki/整数型 "wikilink")、[浮動小数点実数型](../Page/浮動小数点数.md "wikilink")、[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")、キー([UUID](https://ja.wikipedia.org/wiki/汎用一意識別子 "wikilink"))、[ベクトル](https://ja.wikipedia.org/wiki/ベクトル "wikilink")(3次元位置、および[RGB](../Page/RGB.md "wikilink")色表現)、ローテーション([クォターニオン](https://ja.wikipedia.org/wiki/クォターニオン "wikilink"))がある。また、配列型や構造体に相当するものとして基本データ型を要素とする[リスト型がある](../Page/リスト_\(抽象データ型\).md "wikilink")。[組み込み関数は](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")2015年11月時点で430個あり、ユーザーは必要に応じてユーザー定義関数を定義することもできる。

## 実行環境

スクリプトは Second Life の仮想世界内に配置された椅子や壁といったオブジェクトの中に配置され、実行される。その点でスクリプトはオブジェクトと非常に密接に結び付けられる。システムはスクリプトにイベント（タイマー・移動・アバターとのチャット・電子メール・他のオブジェクトとの衝突など）を送信し、その結果スクリプトはステート遷移を起こしたり、他のオブジェクトやアバターとコミュニケーションを行うことになる。

スクリプトはオブジェクトに追加され次第開始される。そのオブジェクトが仮想世界内に配置されている限り、所有者がログインしていない状態でも実行は継続する。所有者がオブジェクトを撤去して自分のインベントリに移し、さらにオブジェクトを仮想世界内に再配置した場合でも、スクリプトの状態は保持されている。[ファイルや](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[データベース](../Page/データベース.md "wikilink")といった永続的なデータ記憶機構は用意されていないが、例えばHTTPリクエスト通信を利用して Second Life 外にデータを保存することはできる。

オブジェクトには複数のスクリプトを含めることができ、それらを並行して実行できる。単体のスクリプトで使用できるメモリ領域は64キロバイト以下に制限される。各スクリプトは[バイトコード](../Page/バイトコード.md "wikilink")の実行形式に[コンパイルされ](../Page/コンパイラ.md "wikilink")、リンデン・ラボのサーバ上の [Mono](../Page/Mono_\(ソフトウェア\).md "wikilink") を用いた[仮想機械](../Page/仮想機械.md "wikilink")で実行される。

いくつかの組み込み関数ではその負荷に応じて0.2秒～20秒の「遅延」が設定されており、高負荷となる関数の連続実行が制限される。さらに実行時間が掛かる処理はすべてイベントハンドラを使った非同期処理となる。これは一つの仮想世界シミュレーターのなかで、数千から数十万個のスクリプトが同時稼働するため、スクリプト実行者がシステム資源に過大な負担をかけないようにするためである。

## 基本となるLSLスクリプト

以下は定型で用意される基本となるスクリプト(一種の[Hello world](../Page/Hello_world.md "wikilink"))である。default というステートの中に state_entry、touch_start という2つのイベントが記述されている。各イベント発生時、「Hello, Avatar\!」「Touched.」とオブジェクトが発言する。

`default`
`{`
`    `<span style='color: #004c7f'>`state_entry`</span>`()`
`    {`
`        `<span style='color: #7f0026'>`llSay`</span>`(0, `<span style='color: #003300'>`"`<span style='color: #19197f'>`H`</span>`ello, `<span style='color: #19197f'>`A`</span>`vatar!"`</span>`);`
`    }`

`    `<span style='color: #004c7f'>`touch_start`</span>`(`<span style='color: #194c19'>`integer`</span>` total_number)`
`    {`
`        `<span style='color: #7f0026'>`llSay`</span>`(0, `<span style='color: #003300'>`"`<span style='color: #19197f'>`T`</span>`ouched."`</span>`);`
`    }`
`}`

## 非同期処理のサンプル

キーボード入力や、ファイル読み出しは、非同期処理で行う。指定したテキストファイル(ノートカード)の内容表示を行うサンプルを示す。

<span style='color: #194c19'>`integer`</span>` lsn;`

<span style='color: #194c19'>`string`</span>` filename;`
<span style='color: #194c19'>`integer`</span>` line;`
<span style='color: #194c19'>`key`</span>` read;`

`default`
`{`
`    `<span style='color: #004c7f'>`touch_start`</span>`(`<span style='color: #194c19'>`integer`</span>` total_number)`
`    {`
`        `<span style='color: #7f0026'>`llOwnerSay`</span>`(`<span style='color: #003300'>`"`<span style='color: #19197f'>`E`</span>`nter note name:"`</span>`);`
`        lsn = `<span style='color: #7f0026'>`llListen`</span>`(0,`<span style='color: #003300'>`""`</span>`,`<span style='color: #7f0026'>`llGetOwner`</span>`(),`<span style='color: #003300'>`""`</span>`);`
`    }`
`    `<span style='color: #004c7f'>`listen`</span>`(`<span style='color: #194c19'>`integer`</span>` channel, `<span style='color: #194c19'>`string`</span>` name, `<span style='color: #194c19'>`key`</span>` id, `<span style='color: #194c19'>`string`</span>` message)`
`    {`
`        `<span style='color: #0000cc'>`if`</span>`(channel==0 && id==`<span style='color: #7f0026'>`llGetOwner`</span>`()){`
`            `<span style='color: #7f0026'>`llListenRemove`</span>`(lsn);`
`            filename = message;`
`            `<span style='color: #0000cc'>`state`</span>` read_file;`
`        }`
`    }`
`}`

<span style='color: #0000cc'>`state`</span>` read_file`
`{`
`    `<span style='color: #004c7f'>`state_entry`</span>`()`
`    {`
`        `<span style='color: #0000cc'>`if`</span>`(`<span style='color: #7f0026'>`llGetInventoryKey`</span>`(filename)==`<span style='color: #19197f'>`NULL_KEY`</span>`){`
`            `<span style='color: #7f0026'>`llOwnerSay`</span>`(`<span style='color: #003300'>`"`<span style='color: #19197f'>`ERROR`</span>`: note is missing."`</span>`);`
`            `<span style='color: #0000cc'>`state`</span>` default;`
`        }`
`        line = 0;`
`        read = `<span style='color: #7f0026'>`llGetNotecardLine`</span>`(filename,line);`
`    }`
`    `<span style='color: #004c7f'>`dataserver`</span>`(`<span style='color: #194c19'>`key`</span>` requested, `<span style='color: #194c19'>`string`</span>` data)`
`    {`
`        `<span style='color: #0000cc'>`if`</span>`(requested==read){`
`            `<span style='color: #0000cc'>`if`</span>`(data==`<span style='color: #19197f'>`EOF`</span>`){`
`                filename = `<span style='color: #003300'>`""`</span>`;`
`                `<span style='color: #0000cc'>`state`</span>` default;`
`            }`
`            `<span style='color: #7f0026'>`llOwnerSay`</span>`(data);`
`            line++;`
`            read = `<span style='color: #7f0026'>`llGetNotecardLine`</span>`(filename,line);`
`        }`
`    }`
`}`

## 関連項目

  - [Second Life](https://ja.wikipedia.org/wiki/Second_Life "wikilink")
  - [リンデン・ラボ](../Page/リンデン・ラボ.md "wikilink")
  - [Mono](../Page/Mono_\(ソフトウェア\).md "wikilink")

## 外部リンク

  - [Second Life LSL ポータル](http://wiki.secondlife.com/wiki/LSL_Portal/ja) - リンデン・ラボが運営する公式 Wiki

[Category:セカンドライフ](https://ja.wikipedia.org/wiki/Category:セカンドライフ "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")