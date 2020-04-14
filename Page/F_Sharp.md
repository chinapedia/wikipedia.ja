> この記事は[F Sharp](https://ja.wikipedia.org/wiki/F_Sharp)から翻訳されています。


**F\#**（エフ シャープ）は[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した[.NET Framework向けの](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[マルチパラダイムプログラミング言語](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")である。[Visual Studio 2010より標準開発言語として追加された](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。

## 概要

2002年から[マイクロソフトリサーチ](../Page/マイクロソフトリサーチ.md "wikilink")の () ら \[1\] によって[OCaml](../Page/OCaml.md "wikilink")をベースに開発が始められた。

OCamlから多くの要素を引き継いだ[関数型と](../Page/関数型言語.md "wikilink")[オブジェクト指向の](https://ja.wikipedia.org/wiki/オブジェクト指向プログラミング言語 "wikilink")[マルチパラダイムである](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")。[型安全](https://ja.wikipedia.org/wiki/型安全 "wikilink")であり、[型推論](../Page/型推論.md "wikilink")の機能をもつ。ただし、[オーバーロードをサポートしているため](../Page/多重定義.md "wikilink")、OCamlのもつ型推論の完全性を失っている。[C\#や](../Page/C_Sharp.md "wikilink")[Visual Basic .NETなどの](../Page/Visual_Basic_.NET.md "wikilink").NET言語と相互運用性があり、.NETクラスライブラリの利用・開発が可能であり、[Monoおよび](../Page/Mono_\(ソフトウェア\).md "wikilink")[Xamarin](https://ja.wikipedia.org/wiki/Xamarin "wikilink")を利用した[Android](../Page/Android.md "wikilink")アプリケーション開発もサポートされている\[2\]。以前は[Silverlight](https://ja.wikipedia.org/wiki/Silverlight "wikilink")を利用した[Windows Phone 7のアプリケーション開発もサポートされていた](https://ja.wikipedia.org/wiki/Windows_Phone_7 "wikilink")。

F\#のFはFunctional programming language（関数型プログラミング言語）および[System Fが由来](https://ja.wikipedia.org/wiki/System_F "wikilink") \[3\]である。

F\#の開発環境はVisual Studioの有償版製品（あるいは無償のCommunityエディション）に**[Visual F\#](https://ja.wikipedia.org/wiki/Microsoft_Visual_F_Sharp "wikilink")**として含まれているほか、Expressエディションで利用可能な無償ツールの配布もされている\[4\]\[5\]\[6\]\[7\]。Visual F\# Tools 4.1でをサポートするようになった。また、[Monoや](../Page/Mono_\(ソフトウェア\).md "wikilink")[.NET Core](https://ja.wikipedia.org/wiki/.NET_Core "wikilink")\[8\]\[9\]環境向けにもF\#コンパイラが移植されているため、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[Linux](../Page/Linux.md "wikilink")などでもF\#プログラムの開発および実行ができる。

OCaml互換の標準ライブラリを備えており、F\#とOCamlのどちらでもコンパイルできるコードを記述することも可能である。しかし[クラスの構文などはF](../Page/クラス_\(コンピュータ\).md "wikilink")\#とOCamlで異なっている。

## 構文

[OCaml](../Page/OCaml.md "wikilink")と互換性のある**冗語構文** () と、[Python](../Page/Python.md "wikilink")のようなインデント（[オフサイドルール](../Page/オフサイドルール.md "wikilink")）による**軽量構文** () の二種類の構文を利用できる。標準では軽量構文が有効になっている。

## 例

### Hello world

``` fsharp
(* これはコメント *)
// 1行コメント。
(* Hello world プログラム *)
printfn "Hello World!"
```

### [再帰](../Page/再帰.md "wikilink")による[階乗](../Page/階乗.md "wikilink")のプログラム

``` fsharp
let rec factorial n =
    match n with
    | 0 -> 1
    | _ -> n * factorial (n - 1)
```

### 再帰関数の例

``` fsharp
(* int リストの要素を再帰的にプリントする *)
let rec printList lst =
    match lst with
    | [] -> ()
    | h :: t ->
        printf "%d\n" h
        printList t

(* 上と同様だが任意の型の要素をプリントする *)
let rec printList2 l =
    match l with
    | []     -> ()
    | h :: t -> printfn "%A" h
                printList2 t

(* match の代りに function 式を利用する *)
let rec printList3 = function
    | []     -> ()
    | h :: t -> printfn "%A" h
                printList3 t

(* 高階関数を利用する *)
let printlist4 lst = List.iter (printfn "%A") lst
```

``` fsharp
(* フィボナッチ数列 *)
let rec fib n =
    match n with
    | 0 | 1 -> n
    | _ -> fib (n - 1) + fib (n - 2)

(* 遅延再帰シーケンス式によるフィボナッチ数列 *)
let rec fibs = Seq.cache <| seq { yield! [1; 1]
                                  for x, y in Seq.zip fibs <| Seq.skip 1 fibs -> x + y }

(* 遅延無限シーケンスによるフィボナッチ数列 *)
let fibSeq = Seq.unfold (fun (a,b) -> Some(a+b, (b, a+b))) (1,1)

(* 偶数のフィボナッチ数をプリントする *)
[1 .. 10]
|> List.map     fib
|> List.filter  (fun n -> (n % 2) = 0)
|> printList

(* 同じことをシーケンス式を利用する *)
[ for i in 1..10 do
    let r = fib i
    if r % 2 = 0 then yield r ]
|> printList
```

### Windows フォームを使用した例

``` fsharp
(* フォームの作成 *)
open System.Windows.Forms
let form = new Form(Visible=true, TopMost=true, Text="Welcome to F#")
(* フォーム テキストを決める *)
let x = 3 + (4 * 5)
do form.Text <- (if x = 23 then "Correct!" else "incorrect")
```

## F\#で書かれたソフトウェア

  - [IronJS](http://ironjs.wordpress.com/)

## 脚注

## 参考文献

  -
## 関連項目

  - [C\#](../Page/C_Sharp.md "wikilink")
  - [OCaml](../Page/OCaml.md "wikilink")
  - [関数型プログラミング言語](https://ja.wikipedia.org/wiki/関数型プログラミング言語 "wikilink")

## 外部リンク

  -
  - [Microsoft Research - F\#](http://research.microsoft.com/en-us/projects/fsharp/default.aspx)

  - [Try F\#](http://www.tryfsharp.org/)

  - [Don Syme's WebLog on F\# and Other Research Projects](http://blogs.msdn.com/dsyme/)

{{.NET}}

[Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.