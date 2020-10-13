> この記事は[Ruby](https://ja.wikipedia.org/wiki/Ruby)から翻訳されています。


**Ruby**（ルビー）は、[まつもとゆきひろ](../Page/まつもとゆきひろ.md "wikilink")（通称: Matz）により開発された[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")[スクリプト言語](../Page/スクリプト言語.md "wikilink")（スクリプト言語とは[プログラミング言語](../Page/プログラミング言語.md "wikilink")の一分類）。

日本で開発されたプログラミング言語としては初めて[国際電気標準会議](../Page/国際電気標準会議.md "wikilink")（IEC）で国際規格に認証された事例となった\[1\]。

## 概要

Ruby は[1993年](../Page/1993年.md "wikilink")[2月24日](https://ja.wikipedia.org/wiki/2月24日 "wikilink")に生まれ、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")12月に[fj上で発表された](../Page/Fj_\(ニュースグループ\).md "wikilink")。名称の Ruby は、プログラミング言語 [Perl](../Page/Perl.md "wikilink") が6月の[誕生石](../Page/誕生石.md "wikilink")である Pearl（[真珠](../Page/真珠.md "wikilink")）と同じ発音をし、「Perlに続く」という意味で、6月の次の誕生石（7月）の[ルビー](../Page/ルビー.md "wikilink")から名付けられた\[2\]。競合言語として Perl の他に [Python](../Page/Python.md "wikilink") があり、「Matz（まつもと） が [Python](../Page/Python.md "wikilink") に満足していれば Ruby は生まれなかったであろう」と公式のリファレンスの用語集で言及されている\[3\]。

機能として、[クラス定義](../Page/クラス_\(コンピュータ\).md "wikilink")、[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")、強力な[正規表現](../Page/正規表現.md "wikilink")処理、[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")、[例外処理](../Page/例外処理.md "wikilink")、[イテレータ](../Page/イテレータ.md "wikilink")、[クロージャ](../Page/クロージャ.md "wikilink")、[Mixin](../Page/Mixin.md "wikilink")、[利用者定義演算子](https://ja.wikipedia.org/wiki/利用者定義演算子 "wikilink")などがある。Perl を代替可能であることが初期の段階から重視されている。Perlと同様に[グルー言語](../Page/グルー言語.md "wikilink")としての使い方が可能で、[C言語](../Page/C言語.md "wikilink")プログラムやライブラリを呼び出す[拡張モジュール](https://ja.wikipedia.org/wiki/拡張モジュール "wikilink")を組み込むことができる。

Ruby 処理系は、主に[インタプリタ](../Page/インタプリタ.md "wikilink")として実装されている（詳しくは[\#実装](https://ja.wikipedia.org/wiki/#実装 "wikilink")を参照）。

[可読性](../Page/可読性.md "wikilink")を重視した構文となっている。Ruby においては整数や文字列なども含めデータ型はすべてがオブジェクトであり、純粋な[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語といえる。

長らく言語仕様が明文化されず、まつもとによる実装が言語仕様に準ずるものとして扱われて来たが、2010年6月現在、[JRuby](https://ja.wikipedia.org/wiki/JRuby "wikilink") や Rubinius といった互換実装の作者を中心に機械実行可能な形で明文化する RubySpec という試みが行われている。公的規格としては2011年3月22日にJIS規格（JIS X 3017）が制定され、その後2012年4月1日に日本発のプログラム言語では初めてISO/IEC規格（ISO/IEC 30170）として承認された \[4\]。

[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")としてバージョン1.9.2までは [Rubyライセンス](https://ja.wikipedia.org/wiki/Rubyライセンス "wikilink")（Ruby License や Ruby'sと表記されることもある。[GPLか](../Page/GNU_General_Public_License.md "wikilink")[Artisticに似た独自ライセンスを選択する](https://ja.wikipedia.org/wiki/アーティスティック・ライセンス "wikilink")[デュアルライセンス](../Page/デュアルライセンス.md "wikilink")）で配布されていたが、バージョン1.9.3以降は[2-clause BSDLとのデュアルライセンスで配布されている](https://ja.wikipedia.org/wiki/BSDライセンス#二条項BSDライセンス "wikilink")\[5\]。

## 所縁のある地域

Rubyは日本の国産言語として知られており、特にRubyと所縁のある地域はRubyの聖地と呼ばれている。

  - [静岡県](../Page/静岡県.md "wikilink")[浜松市](https://ja.wikipedia.org/wiki/浜松市 "wikilink") - 開発者のまつもとゆきひろが[日本タイムシェア](https://ja.wikipedia.org/wiki/日本タイムシェア "wikilink")株式会社（現：[TIS](https://ja.wikipedia.org/wiki/TIS "wikilink")株式会社）の浜松市にあった研究所に勤務していた[1993年](../Page/1993年.md "wikilink")にRubyの開発を開始\[6\]
  - [愛知県](https://ja.wikipedia.org/wiki/愛知県 "wikilink")[名古屋市](../Page/名古屋市.md "wikilink") - 株式会社[トヨタケーラム](../Page/トヨタケーラム.md "wikilink")（現：株式会社[トヨタシステムズ](https://ja.wikipedia.org/wiki/トヨタシステムズ "wikilink")）在籍時、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")にRubyを[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")として公開\[7\]
  - [島根県](../Page/島根県.md "wikilink")[松江市](../Page/松江市.md "wikilink") - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")から島根県松江市に移り、同市の株式会社[ネットワーク応用通信研究所](../Page/ネットワーク応用通信研究所.md "wikilink")（NaCl）フェローとしてRubyの普及に尽力\[8\]

## 設計思想

開発者のまつもとゆきひろは、「Rubyの言語仕様策定において最も重視しているのはストレスなく[プログラミングを楽しむことである](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink") (*enjoy programming*)」と述べている。

ただし、まつもとによる明文化された言語仕様は存在しない。Perlのモットー「やり方はいろいろある (*There's More Than One Way To Do It; TMTOWTDI*)」は「多様性は善 (*Diversity is Good*)」というスローガンで Ruby に引き継がれてはいるものの最重要なものではないとも述べており、非推奨な手法も可能にするとともに、そのような手法を言語仕様により使いにくくすることによって自粛を促している。

## 実装

### 公式な実装

Rubyの公式な実装には、以下の二種類が存在する。

  - [MRI](https://ja.wikipedia.org/wiki/CRuby "wikilink")（Matz' Ruby Implementation）
    まつもとゆきひろによって開発されはじめたC言語による実装であり、最も広く使われている。狭義として、evalを中心とした部分が次で述べるYARVに更新される以前（1.8.x以前）のバージョンを指して言うこともある。JRuby などに対して CRuby と呼ばれることもある。また、JRuby などに対して、広義として YARV 以降も含んで言うこともある。
  - [YARV](https://ja.wikipedia.org/wiki/YARV "wikilink")
    1.9で採用された、MRIのevalをバイトコードを実行するタイプに置き換えたもの。（狭義の）MRIはソースコードを構文木にコンパイルした後、構文木を解釈する仮想機械であるevalで実行するインタプリタであるが、YARVはソースコードをバイトコードにコンパイルした後、バイトコードを解釈する仮想機械であるevalで実行するインタプリタである。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などのバイトコードとは違い、このバイトコードはファイルとしては生成されない（ファイルとして静的に外部化することを考慮した設計では基本的になく、シンボルを多用するなどしている）。なお「YARV」は、もともとは開発中におけるその仮想機械の名前だった。

### その他の実装

  - [JRuby](https://ja.wikipedia.org/wiki/JRuby "wikilink")
    [Java](https://ja.wikipedia.org/wiki/Java "wikilink") 言語による実装。純粋な Java で行われているため、プラットフォーム非依存の利用が可能。ほとんどの Ruby クラスが組み込みで提供されている。インタープリタ・[実行時コンパイラ](../Page/実行時コンパイラ.md "wikilink")・[事前コンパイラ](https://ja.wikipedia.org/wiki/事前コンパイラ "wikilink")の3種類が用意されている。事前コンパイラでは、Java バイトコードへ変換し、JRuby が無くても他の Java プラットフォーム上で動作させることが可能となる。
  - [IronRuby](../Page/IronRuby.md "wikilink")
    [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 上で Ruby を動作させる実装であり、.NET Framework のライブラリと連携させることができる。[JIT方式のバイトコードインタプリタ](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")。[共通言語基盤](../Page/共通言語基盤.md "wikilink")に準拠した実装（[Monoなど](../Page/Mono_\(ソフトウェア\).md "wikilink")）で動作するため、プラットフォーム非依存の利用も可能（ただし、ソースコードが .NET Framework のライブラリに依存している場合は Mono での動作は不可能）。
  -
    [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") 上で動作する Ruby 実装。[Cocoa](../Page/Cocoa.md "wikilink") を含む様々なフレームワークとの連携が可能。[RubyCocoa](https://ja.wikipedia.org/wiki/RubyCocoa "wikilink") の問題点を解決するために開発されている。
  -
    [仮想機械](../Page/仮想機械.md "wikilink")上で Ruby を実行する[JIT方式のバイトコードインタプリタ](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")。大部分が Ruby で実装されている。
  -
    [smalltalk](https://ja.wikipedia.org/wiki/smalltalk "wikilink")仮想マシン上で動作する実装[1](https://maglev.github.io/)。
  - [mruby](https://ja.wikipedia.org/wiki/mruby "wikilink")
    [組み込みシステム](../Page/組み込みシステム.md "wikilink")向けの軽量版。[家電製品](https://ja.wikipedia.org/wiki/家電製品 "wikilink")の他、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")、[ゲームなどでの使用を想定している](../Page/コンピュータゲーム.md "wikilink")。
  - その他
    [Parrot](../Page/Parrot.md "wikilink") 上で Ruby を動作させるための実装なども開発されている。

## 例

基本的なコード

``` ruby
# 文字列、数値を含め、全てがオブジェクトである
-199.abs                                       # 199
"ruby is cool".length                          # 12
"Rick".index("c")                              # 2
"Nice Day Isn't It?".split(//).uniq.sort.join  # " '?DINaceinsty"
```

### コレクション

[配列](../Page/配列.md "wikilink")の作成と使用法

``` ruby
a = [1, 'hi', 3.14, 1, 2, [4, 5]]

a[2]                      # 3.14
a.reverse                 # [[4, 5], 2, 1, 3.14, 'hi', 1]
a.flatten.uniq            # [1, 'hi', 3.14, 2, 4, 5]
```

[ハッシュの作成と使用法](../Page/ハッシュテーブル.md "wikilink")

``` ruby
hash = {'water' => 'wet', 'fire' => 'hot'}
hash = {water: 'wet', fire: 'hot'} # シンボルリテラルをキーとする場合、Ruby 1.9 からはこのような Javascript 風の表記ができる。
puts hash[:fire]       # 表示:  hot

hash.each do |key, value|
  puts "#{key} is #{value}"
end

# 表示:               water is wet
#                     fire is hot

hash.delete_if {|key, value| key == :water}   # Deletes :water => 'wet'
```

### 制御構造

ほかの言語でもよくみられるような制御構造を用いることができる。

``` ruby
if "fablic".length > 3
  puts 'ya'
else
  puts 'nop'
end
# 表示:         ya

list = [1, 2, 5, 13, 21]
for item in list
  puts item
end
# 表示:         1
#               2
#               5
#               13
#               21

n = 0
while n < 3
  puts 'foobar'
  n += 1
end
# 表示:         foobar
#               foobar
#               foobar
```

一部の制御構造は後述するイテレータで代替することができる。

### ブロック付きメソッド呼び出し

Ruby ではブロック付きメソッド呼び出しを用いるコードが好まれることが多い。これを用いると、ユーザー定義の[制御構造](../Page/制御構造.md "wikilink")や[コールバックなど様々な処理を簡潔に記述できるからである](../Page/コールバック_\(情報工学\).md "wikilink")。

ブロックとは波括弧

``` ruby
{
```

、

``` ruby
}
```

または

``` ruby
do
```

、

``` ruby
end
```

によって囲まれたコード列のことである。メソッド呼び出しの末尾に記述することが出来る。この2つは基本的に同一だが、結合の優先度が異なる。一行で書くときは波括弧が、複数行に渡る場合は

``` ruby
do
```

、

``` ruby
end
```

が使用される場合が多い。

``` ruby
# { ... }
method1 { puts "Hello, World!" }
# do ... end
method2 do
  puts "Hello, world!"
end
```

ブロック付きメソッド呼び出しが繰り返し処理を主な役割としていたことから、イテレータと呼ばれていた時期がある。しかし、実際には繰り返し処理にとどまらず、様々な使われ方をしているので、最近はブロック付きメソッド呼び出し全体の総称としてイテレータという名称を用いるのは適切でないと考えられている。\[9\]

#### 繰り返し処理

配列の各要素への繰り返し処理

``` ruby
list = [1, 2, 5, 13, 21]
list.map! {|item| item * 2} # listの各要素を2倍する処理
```

以下はブロックを使わずに同じことを行う場合

``` ruby
list = [1, 2, 5, 13, 21]
n = 0
while n < list.length
  list[n] *= 2
  n += 1
end
```

指定した回数の繰り返し処理

``` ruby
3.times { puts 'foobar' }       # 制御構造の項のwhileの例と同じ
```

#### 後処理の省力化

ブロックの内容を実行してから、決められた後処理を行うメソッドもある

``` ruby
File.open('file.txt', 'w+b') do |file|
  file.puts 'Wrote some text.'
end                             # file.txtはここで自動的に閉じられる
```

これは次の例と同様の処理を行う（`ensure` については[例外処理の項を参照](https://ja.wikipedia.org/wiki/#例外処理 "wikilink")）

``` ruby
begin
  file = File.open('file.txt', 'w+b')
  file.puts 'Wrote some text.'
ensure
  file.close
end
```

#### 本処理を後から指定

実際に行いたい処理をブロックで記述する。前項の後処理の省力化もこれの一例といえる。

``` ruby
def bfs(list)       #配列をツリーに見立てた処理
  until list.empty?
    unit = list.shift
    yield unit      #ブロックの内容を実行
    unit.each{|v| list.push v} if defined? unit.push
  end
end
bfs([0,1,[2,3],4,[5,[6,7,8]],9]) {|v| p v}
```

この例は、ツリーから要素と分枝をつぎつぎと取り出して取り出したものになんらかの処理を行うものである。メソッドの利用者は、なんらかの処理のみを記述すればよく、取り出しのアルゴリズムなど、本質的でない内容に意識を向ける必要がなくなる。

#### クロージャ

[クロージャ](../Page/クロージャ.md "wikilink")となるようなブロックの引数渡し

``` ruby
# オブジェクトのインスタンス変数（変数名の頭に@が付く）でブロックを記憶。
def remember(&p)
  @block = p
end
# nameを受け取るブロックを引数に、上記のメソッドを呼び出す。
remember {|name| puts "Hello, " + name + "!"}

# 後に必要になった時点でクロージャを呼び出す。
@block.call("John")
# 表示:"Hello, John!"
```

メソッドからクロージャを返す例

``` ruby
def create_set_and_get(value = 0)
  return proc {|x| value = x}, proc { value }
end

setter, getter = create_set_and_get
setter.call(21)
getter.call # => 21
```

### クラス

次のコードは`Person`という名前のクラスである。その中、まず`initialize`はオブジェクトを初期化するコンストラクタである。ほかに2つのメソッドがあり、1つは比較演算子である`<=>`を[オーバーライド](../Page/オーバーライド.md "wikilink")しており`Array#sort`によりプロパティ`age`でソートすることができる。もう1つのオーバーライド箇所の`to_s`メソッドは `Kernel#puts` での表示の形式を整える。`attr_reader`は Ruby における[メタプログラミング](../Page/メタプログラミング.md "wikilink")の例であり、`attr` はインスタンス変数の入出力を司る、いわゆる値を取得する `getter` メソッドや値を設定する `setter` メソッド（[アクセサ](https://ja.wikipedia.org/wiki/アクセサ "wikilink")）を定義する。`attr_reader`は `getter` メソッドのみの定義である。なおメソッド中では最後に評価された式が返り値となり、明示的な`return`は省略できる。

``` ruby
class Person
  def initialize(name, age)
    @name, @age = name, age
  end

  def <=>(person)
    @age <=> person.age
  end

  def to_s
    "#{@name} (#{@age})"
  end

  attr_reader :name, :age
end

group = [ Person.new("John", 20),
          Person.new("Markus", 63),
          Person.new("Ash", 16)
        ]

puts group.sort.reverse
```

結果は3つの名前が年の大きい順に表示される

`Markus (63)`
`John (20)`
`Ash (16)`

### 例外処理

例外はなにか不具合が起こったとき`raise`の呼び出しで発生させることができる。Ruby での例外は `Exception` クラスか、そのサブクラスのインスタンスである。

例外にはメッセージを追加することもできる

``` ruby
 raise "This is a message"
```

さらに例外のタイプも指定できる

``` ruby
 raise ArgumentError, "Illegal arguments!"
```

例外は`rescue`節で処理することができ、次のようにコードに`rescue`を付加するだけである

``` ruby
begin
  # 通常処理
rescue
  # 例外処理。引数を省略すると、StandardErrorのサブクラスの例外のみ処理する
rescue SomeError
  # 例外処理。SomeErrorの例外のみ処理する。
ensure
  # 例外の発生に関わらず必ず実行される処理
else
  # 例外が発生しなかったときに実行される処理
end
```

## Rubyの周辺技術

  - [分散オブジェクト](https://ja.wikipedia.org/wiki/分散オブジェクト "wikilink")を実現する [dRuby](https://ja.wikipedia.org/wiki/dRuby "wikilink")
  - Ruby スクリプトに埋め込むことができる文書形式[RD](../Page/Ruby_Document_format.md "wikilink")
  - Ruby によるRDを採用した[ウィキ](../Page/ウィキ.md "wikilink")、[RWiki](https://ja.wikipedia.org/wiki/RWiki "wikilink")
  - Ruby から[SDL](../Page/SDL.md "wikilink")ライブラリを扱えるようにする[Ruby/SDL](https://ja.wikipedia.org/wiki/Ruby/SDL "wikilink")
  - Ruby から [Delphi](../Page/Delphi.md "wikilink") を扱えるようにする Apollo
  - Ruby によるウェブアプリケーションフレームワーク [Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink")
  - Ruby の処理系の一つでRuby1.9以後の処理系として採用されている [YARV](https://ja.wikipedia.org/wiki/YARV "wikilink")
  - Ruby の統合開発環境 [RDE](https://www.vector.co.jp/soft/win95/prog/se209196.html)
  - Ruby のコードを Windows の[実行形式ファイルに変換する](../Page/実行ファイル.md "wikilink") [Exerb](https://ja.wikipedia.org/wiki/Exerb "wikilink")
  - Ruby 用のライブラリ管理システムである [RubyGems](https://ja.wikipedia.org/wiki/RubyGems "wikilink")
  - [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink") に組み込むための [mod ruby](https://ja.wikipedia.org/wiki/mod_ruby "wikilink")
  - サーバサイドで[HTMLへの埋め込み](../Page/HyperText_Markup_Language.md "wikilink") Ruby 文を実現する [eRuby](https://ja.wikipedia.org/wiki/eRuby "wikilink")
  - Ruby のコードをJavaScriptへ変換するコンパイラ　[Opal](https://opalrb.com/)
  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") の [ActiveX](../Page/ActiveX.md "wikilink") 環境で Ruby インタープリターを呼び出す [ActiveScriptRuby](https://ja.wikipedia.org/wiki/ActiveScriptRuby "wikilink")（[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 限定だがHTMLに埋めこんでクライアント上で動かすスクリプト言語として Rubyを指定できるようになる）
  - Ruby から [Win32API](../Page/Windows_API.md "wikilink") や[COMコンポーネントを呼び出すためのライブラリー](../Page/Component_Object_Model.md "wikilink") WIN32OLE
  - JavaScript や Flash 上で動く Ruby の処理系 [HotRuby](https://ja.wikipedia.org/wiki/HotRuby "wikilink")
  - Ruby による[ビヘイビア駆動開発](../Page/ビヘイビア駆動開発.md "wikilink")のためのフレームワーク [RSpec](https://ja.wikipedia.org/wiki/RSpec "wikilink")
  - Ruby で書かれた[ビルドツール](https://ja.wikipedia.org/wiki/ビルドツール "wikilink") [Rake](https://ja.wikipedia.org/wiki/Rake_\(ソフトウェア\) "wikilink")
  - Ruby で書かれたmacOS パッケージ管理システム [homebrew](https://ja.wikipedia.org/wiki/homebrew "wikilink")
  - Ruby から[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")を使用するための拡張ライブラリ [DXRuby](https://ja.wikipedia.org/wiki/DXRuby "wikilink")
  - Ruby プログラミングを視覚的直感的に開発可能とする、[Scratch (プログラミング言語)のRuby対応版](https://ja.wikipedia.org/wiki/Scratch_\(プログラミング言語\) "wikilink")（Rubyソースを生成するScratchとも言えるもの）とでも言うべきGUI型IDE [Smalruby](https://ja.wikipedia.org/wiki/Smalruby "wikilink")

## Rubyで開発されたアプリケーション

  - [tDiary](https://ja.wikipedia.org/wiki/tDiary "wikilink")

  - [影舞](https://ja.wikipedia.org/wiki/影舞 "wikilink")

  - [Hiki](https://ja.wikipedia.org/wiki/Hiki "wikilink")

  - [Chef](../Page/Chef_\(ソフトウェア\).md "wikilink")

  - [Vagrant](https://ja.wikipedia.org/wiki/Vagrant_\(ソフトウェア\) "wikilink")

  - [Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink")

      - [GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")
      - [Metasploit](https://ja.wikipedia.org/wiki/Metasploit "wikilink")
      - [Redmine](https://ja.wikipedia.org/wiki/Redmine "wikilink")
      - [Basecamp](https://ja.wikipedia.org/wiki/Basecamp "wikilink")
      - [RadiantCMS](https://ja.wikipedia.org/wiki/RadiantCMS "wikilink")

  - [qwikWeb](https://ja.wikipedia.org/wiki/qwikWeb "wikilink")

  - [WEBrick](https://ja.wikipedia.org/wiki/WEBrick "wikilink")

  -
  - [Phusion Passenger](https://ja.wikipedia.org/wiki/Phusion_Passenger "wikilink")

  - [Puppet](https://ja.wikipedia.org/wiki/Puppet_\(ソフトウェア\) "wikilink")

  - [mikutter](https://ja.wikipedia.org/wiki/mikutter "wikilink")

  - [Serverspec](https://ja.wikipedia.org/wiki/Serverspec "wikilink")

## Rubyを組み込んだアプリケーション

  - RPGツクールXP・RPGツクールVX
    株式会社エンターブレインから発売されているRPG制作ソフトシリーズのうち、[RPGツクールXP](../Page/RPGツクールXP.md "wikilink")と[RPGツクールVX](../Page/RPGツクールVX.md "wikilink")では、Ruby をツクール専用にカスタマイズした [RGSS](../Page/RGSS.md "wikilink")を搭載している。同シリーズの従来ソフトではあらかじめ用意された機能しか使えなかったが、RGSSにより戦闘などのシステムを一から構築する事が出来るようになった。
    [RPGツクールMV](https://ja.wikipedia.org/wiki/RPGツクールMV "wikilink")からは開発言語がJavaScriptに変更になった。

## エピソード

Ruby ではブロック構造を `end` で終える構文が採用されているが、開発者のまつもとゆきひろは他の構文が採用される可能性があったことを述べている。当時、[Emacs](../Page/Emacs.md "wikilink") 上で `end` で終える構文をオートインデントさせた例はあまりなく、Ruby 言語用の編集モードにオートインデント機能を持たせられるかどうかが問題になっていたためである\[10\]。実際には数日の試行でオートインデント可能であることがわかり、現在の構文になった。[C言語](../Page/C言語.md "wikilink")のような`{〜}`を使った構文も検討されていたが、結局これは採用されなかった\[11\]。

## 脚注

### 注釈

### 出典

## 参考文献

  - \- プログラム未経験者向けの入門書。

      -
      -
  -   -
      -
      -
      -
  -
  -
  -
## 関連項目

  - [Goby(Golang+Ruby)](https://ja.wikipedia.org/wiki/Goby\(Golang+Ruby\) "wikilink")
  - [Perl](../Page/Perl.md "wikilink")
  - [Python](../Page/Python.md "wikilink")
  - [スクリプト言語](../Page/スクリプト言語.md "wikilink")
  - [オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")

## 外部リンク

  -
  -
  - [JISC - JISX3017 プログラム言語Ruby](https://www.jisc.go.jp/app/jis/general/GnrJISNumberNameSearchList?show&jisStdNo=X3017)

[カテゴリ:オブジェクト指向言語](https://ja.wikipedia.org/wiki/カテゴリ:オブジェクト指向言語 "wikilink") [カテゴリ:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/カテゴリ:オープンソースソフトウェア "wikilink") [カテゴリ:スクリプト言語](https://ja.wikipedia.org/wiki/カテゴリ:スクリプト言語 "wikilink") [\*](https://ja.wikipedia.org/wiki/カテゴリ:Ruby "wikilink") [カテゴリ:1995年のソフトウェア](https://ja.wikipedia.org/wiki/カテゴリ:1995年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  [ Re: イテレータとfor文](http://blade.nagaokaut.ac.jp/cgi-bin/scat.rb/ruby/ruby-list/39878)
10. まつもとゆきひろは1988年に Emacs に触れて以来、Emacsを使い続けている。（、まつもとによる記述より）
11. まつもとゆきひろ 「探訪 Ruby 第6回」『Linux Magazine』56号、[株式会社アスキー](https://ja.wikipedia.org/wiki/株式会社アスキー "wikilink")、2004年。