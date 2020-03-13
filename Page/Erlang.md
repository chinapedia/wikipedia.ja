> この記事は[Erlang](https://ja.wikipedia.org/wiki/Erlang)から翻訳されています。


[LYME_software_bundle.svg](https://ja.wikipedia.org/wiki/File:LYME_software_bundle.svg "fig:LYME_software_bundle.svg") is -based}}\]\]

****（アーラン）は、[コンピュータ](../Page/コンピュータ.md "wikilink")において汎用的な用途に使うことができる[並行処理](https://ja.wikipedia.org/wiki/並行処理 "wikilink")指向の[プログラミング言語](../Page/プログラミング言語.md "wikilink")および実行環境。

## 概要

の[直列処理のサブセットの言語は](https://ja.wikipedia.org/wiki/逐次化 "wikilink")、[関数型言語](../Page/関数型言語.md "wikilink")であり、先行評価を行い、[変数への](../Page/変数_\(プログラミング\).md "wikilink")[代入は](../Page/変数_\(プログラミング\).md "wikilink")1回限りであり、[動的型付け](../Page/動的型付け.md "wikilink")である。 は[エリクソン](../Page/エリクソン.md "wikilink")により次の条件のシステムを構築できるよう設計された。

  - [分散化された環境](../Page/分散コンピューティング.md "wikilink")
  - 障害に耐性をもつ ([フォルトトレラント](https://ja.wikipedia.org/wiki/フォルトトレラント "wikilink"))
  - ある程度の[リアルタイム](../Page/リアルタイム.md "wikilink")性を備える
  - 無停止で稼働する

[ホットスワップ](../Page/ホットスワップ.md "wikilink")が可能であり、稼働中のシステムを停止すること無くの[プログラムを変更することができる](../Page/プログラム_\(コンピュータ\).md "wikilink")。は、当初はエリクソン社内部だけで使われる非公開の技術であったが、1998年に[オープンソース](../Page/オープンソース.md "wikilink")として公開された。エリクソンによるの[実装](../Page/実装.md "wikilink")は基本的には[インタプリタ](../Page/インタプリタ.md "wikilink")であるが、という[コンパイラ](../Page/コンパイラ.md "wikilink")も同社の実装に含まれている。ただしはが動作する全ての[プラットフォームで使えるわけではない](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。

においては、[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")の処理の[並行性](../Page/並行性.md "wikilink")はプログラム開発者（[プログラマ](../Page/プログラマ.md "wikilink")）にとって明瞭である。これに対し、ほとんどのプログラミング言語においては、マルチスレッドは複雑で誤りを犯しがちな分野である。 で「プロセス」([スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")) を生成し管理する手法はごく平凡な方法である。

## 命名

は[数学者](../Page/数学者.md "wikilink")の[アグナー・アーラン](../Page/アグナー・アーラン.md "wikilink")から名前をとって命名された。 一方で、エリクソン社内で非常によく使われたため「」にちなんで命名されたと一部の人々は思っている。 当時エリクソンのコンピュータ科学研究所の所長であったビャーネ・デッカーによれば、この名前に関する2重性については意図的なものだとのことである。

## 関数型言語

の[ソースコード](../Page/ソースコード.md "wikilink")の例を示す。

``` erlang
 -module(fact).
 -export([fac/1]).

 fac(0) -> 1;
 fac(N) when N > 0 -> N *fac(N-1).
```

次のソースコードはによる[クイックソート](../Page/クイックソート.md "wikilink")の[アルゴリズム](../Page/アルゴリズム.md "wikilink")の[実装](../Page/実装.md "wikilink")である。

``` erlang
 %% quicksort:qsort(List)
 %% Sort a list of items
 -module(quicksort).
 -export([qsort/1]).

 qsort([]) -> [];
 qsort([Pivot|Rest]) ->
     qsort([ X||X <- Rest, X < Pivot]) ++ [Pivot] ++ qsort([ Y||Y <- Rest, Y >=Pivot]).
```

この例では[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")`qsort`の[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")を行っている。 再帰呼び出しはソート処理の対象が無くなった時点で終了する。 [式](../Page/式_\(プログラミング\).md "wikilink")`[ X||X <- Rest, X < Pivot]`は「 `X`を`Rest`の要素として、`X`が`Pivot`より小さい全ての`X`を選択する。」と読むことができる。 このようにでは[リストを非常に簡単に扱うことができる](../Page/リスト_\(抽象データ型\).md "wikilink")。 では異なる2つの[データ型](../Page/データ型.md "wikilink")の値の間であらゆる論理式を評価できるため、式の評価は単純である。 例えば、`1 < a`は`true`を返す。

ただしにおける戻り値（`true`あるいは`false`）を返す基礎的なしくみを変更する必要がある場合には、比較関数を使うことができる。 例えば、`a < 1`が`true`と評価される比較順序により順序付けられた[リストが必要な場合などである](../Page/リスト_\(抽象データ型\).md "wikilink")。

次のソースコードでは[リストをリスト要素の長さを基準にしてソートする](../Page/リスト_\(抽象データ型\).md "wikilink")。

``` erlang
 -module(listsort).
 -export([by_length/1]).
  %% まずby_lengthが実行され　関数fun(A,B)という関数がＦに代入されてからqsortが実行される
  %% qSortは大小の比較関数としてby_lengthで定義したSmallerつまりＦを使っている
 by_length(Lists) ->
     F=fun(A,B) when is_list(A), is_list(B) ->
             length(A) < length(B)
         end,
     qsort(Lists, F).

  qsort([], _) -> [];
  qsort([Pivot|Rest], Smaller) ->
      qsort([ X||X <- Rest, Smaller(X, Pivot)], Smaller)
      ++ [Pivot] ++
      qsort([ Y||Y <- Rest, not(Smaller(Y, Pivot))], Smaller).
```

## 並行処理指向で分散処理指向の言語

の主な特長は、[並行処理](https://ja.wikipedia.org/wiki/並行処理 "wikilink")のサポートである。 における並行処理は、複数の「プロセス」を生成し、それらの間で通信を行うための、簡潔で強力な機能群によって支えられている。 なお、が提供する「プロセス」は、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")が提供する[プロセス](../Page/プロセス.md "wikilink")や[スレッドとは異なり](../Page/スレッド_\(コンピュータ\).md "wikilink")、の[仮想機械](../Page/仮想機械.md "wikilink")(VM)によって管理される。 「プロセス」の生成オーバーヘッドは約300[ワード](../Page/ワード.md "wikilink")程度に抑えられており、大量の「プロセス」を、性能を低下させずに生成できる。 ある[ベンチマーク](../Page/ベンチマーク.md "wikilink")では2000万個の「プロセス」を並行実行できることが示された\[1\]。

これ以降の記述ではにおける「プロセス」を括弧無しで言及する。

におけるプロセス間の通信は、[非共有かつ非同期のメッセージ転送システムによって行われる](https://ja.wikipedia.org/wiki/シェアード・ナッシング・アーキテクチャ "wikilink")。 のプロセスは全てそれぞれの「メールボックス」をもつ。 メールボックスには他のプロセスから受信したメッセージが格納される。 その後、メールボックスに格納されたメッセージがメールボックスを所有するプロセスによって処理される。 そのときのプロセスはメッセージを得るために`receive`という基本操作を行う。 メッセージを得る過程では[パターンマッチング](../Page/パターンマッチング.md "wikilink")が行われる。 まずメッセージ制御ルーティンが1番目のメッセージに対して各パターンがマッチするかどうか調べる。 2番目以降のメッセージに対しても同様のことを行う。 マッチングは、マッチするメッセージに出会うまで行われる。 メッセージが処理されると、メッセージはメールボックス[キューから除去され](../Page/キュー_\(コンピュータ\).md "wikilink")、プロセスは復帰して続きの処理を行う。 の構成要素は何であれメッセージとして使うことができる。 の基本要素である[整数](../Page/整数.md "wikilink")\[2\]、[浮動小数点数](../Page/浮動小数点数.md "wikilink")\[3\]、文字\[4\]、アトム\[5\]も、また[タプル](../Page/タプル.md "wikilink")\[6\]、[リスト](../Page/リスト_\(抽象データ型\).md "wikilink")\[7\]、さらには[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")\[8\]さえも、メッセージとして扱うことができる。

[ソースコード](../Page/ソースコード.md "wikilink")の例を示す。

``` erlang
  Pid=spawn(Mod, Func, Args)       % execute function Func as new process
  Pid=spawn(Node, Mod, Func, Args) % execute function Func in remote node Node

  Pid ! a_message      % send message to the process (asynchronously)

  receive              % receive message sent to this process
    a_message -> do_something;
    {data, Data_content} -> do_something_else();% This is a tuple of a type atom and some data
    {hello, Text} -> io:format("Got hello message:~s", [Text]);
    {goodbye, Text} -> io:format("Got goodbye message:~s", [Text])
  end.
```

では異なるノード (コンピュータ) に分散した複数のプロセスを互いに連携させて動作させるためのサポートも組み込みで備えている ([分散処理](https://ja.wikipedia.org/wiki/分散処理 "wikilink")) 。 プロセスは遠隔のノードに生成することができ、遠隔ノード上のプロセスとのプロセス間通信は透過的である。 すなわち、遠隔ノード上のプロセスとのプロセス間通信は、同じノード上のプロセスとのプロセス間通信と全く同じように行われる。

での並行処理では、エラー処理の基本的な方法をサポートしている。 あるプロセスが異常をきたすと、プロセスは手際良く終了し、そのプロセスを制御しているプロセス (何らかのアクションをとることができるプロセス) にメッセージを送信する。 このエラー処理の方法により、ソースコードの保守性を高め[複雑性](https://ja.wikipedia.org/wiki/複雑性 "wikilink")を低減することができる。

## 配布

[エリクソン](../Page/エリクソン.md "wikilink")はを[オープンソース](../Page/オープンソース.md "wikilink")として、1998年に公開した。 その意図は、特定企業からの独立性を確保することと、に対する人々の認知を高めることであった。 [ライブラリ](../Page/ライブラリ.md "wikilink")と[リアルタイム](../Page/リアルタイム.md "wikilink")[データベース](../Page/データベース.md "wikilink")「」と共に配布される [プログラミング言語](../Page/プログラミング言語.md "wikilink")の配布形式は、 (OTP) と呼ばれている。 エリクソンおよび数社の企業は、技術に対する商用サポートを提供している。

をオープンソースとして公開する方針を採ってからは、世界中のいくつもの企業によって採用されている。 ノベル・ネットワークス\[9\]、ティー・モバイル\[10\]などの企業がを採用している\[11\]。同社ではこれまで何十ものプロジェクトでを採用してきた。とりわけ大規模なものは非常にスケーラブルな AXD301 ATM スイッチのプロジェクトである。を採用しているエリクソン以外の組織としては、ノルテル\[12\]、ドイチェ・フルークズィヒャルング\[13\]（航空管制を担う[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")の政府組織）、ティー・モバイルなどが挙げられている。 2014年にはWhatsApp、ドワンゴ、LINEなどがErlangを採用していることを表明した。

2015年現在、は活発に開発が続けられており、定期的に新リリースを公開している。 は、いくつかの[UNIXに似たオペレーティングシステムおよび](../Page/Unix系.md "wikilink")[{{lang上で使うことができる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 関連項目

  - [並行計算](../Page/並行計算.md "wikilink")

  - [アクターモデル](../Page/アクターモデル.md "wikilink")

  - [ガード (プログラミング)](../Page/ガード_\(プログラミング\).md "wikilink")

  -
  - \- を使って開発された XMPP/Jabber インスタントメッセージング[サーバ](../Page/サーバ.md "wikilink")

  - \- で開発された十分な機能を備え高い性能を発揮する

  - [Riak](https://ja.wikipedia.org/wiki/Riak "wikilink") - アマゾン・ダイナモの論文に基づいて実装されている NoSQL データベース

[ウェブサーバ](https://ja.wikipedia.org/wiki/ウェブサーバ "wikilink")

  - — 高性能なベンチマークツール

## 脚注

<references/>

## 参考文献

  - 、2003年、「[](http://www.sics.se/~joe/thesis/armstrong_thesis_2003.pdf)」、博士論文 (Ph.D.) 、スウェーデン王立ストックホルム工科大学

## 外部リンク

  -
  - [](http://dmoz.org/Computers/Programming/Languages/Erlang/) - オープンディレクトリプロジェクト

  - [ ](http://erlangworld.web.fc2.com/) - 日本語によるの解説サイト

[Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:並行計算](https://ja.wikipedia.org/wiki/Category:並行計算 "wikilink")

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
11. 「[](http://www.erlang.org/faq/t1.html#AEN50)」に関してよく尋ねられる質問集。この資料によるとを最も大規模に採用している組織は[エリクソン](../Page/エリクソン.md "wikilink")社である。エリクソン社は電気通信システムの開発にを使っている。
12.
13.