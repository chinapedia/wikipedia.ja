> この記事は[Boost C++](https://ja.wikipedia.org/wiki/Boost_C++)から翻訳されています。


**Boost** （**ブースト**）とは、[C++](../Page/C++.md "wikilink")の先駆的な開発者のコミュニティ、およびそのコミュニティによって公開されている[オープンソース](../Page/オープンソース.md "wikilink")のソフトウェア[ライブラリ](../Page/ライブラリ.md "wikilink")のことを指す。コミュニティとしてのBoostはC++標準化委員会の委員により設立されており、現在でもその多くが構成員として留まっている。このような経緯もあり、BoostコミュニティはC++の標準化において大きな影響力を有している。実際に標準化委員会が発表した「[TR1](https://ja.wikipedia.org/wiki/C++_Technical_Report_1 "wikilink")」の2/3以上がBoostライブラリを基にしている。Random, Regex, Threadなどはいずれも[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")規格の標準ライブラリとして正式に導入・標準化されている。このことから、Boostは考案された新機能を標準化させる前の試験運用の場であるとも言える。

Boostで公開されるライブラリはコミュニティの公開レビューによって精選されている。Boostを使用して作成したプログラムは、商用、非商用を問わず無償の[Boost Software License](https://www.boost.org/users/license.html)の下でライセンスされる。

Boostは[テンプレートなどを活用して積極的に](../Page/テンプレート_\(プログラミング\).md "wikilink")[メタプログラミング](https://ja.wikipedia.org/wiki/メタプログラミング "wikilink")や[ジェネリックプログラミング](https://ja.wikipedia.org/wiki/ジェネリックプログラミング "wikilink")の技法を取り入れて行く傾向がある。そのためBoostライブラリの利用者にはC++の現代的な記述に慣れていることを要求される。

。

## 内容

Boostには次のような分野のライブラリが含まれている。ライブラリの一部はビルドが必要。

  - [アルゴリズム](https://ja.wikipedia.org/wiki/Standard_Template_Library#アルゴリズム "wikilink")
  - 並列プログラミング（非同期プログラミング）
      - [thread](https://www.boost.org/doc/libs/release/libs/thread/) - [スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")
      - [context](https://www.boost.org/doc/libs/release/libs/context/) - ユーザーレベル[コンテキストスイッチ](https://ja.wikipedia.org/wiki/コンテキストスイッチ "wikilink")
      - [coroutine](https://www.boost.org/doc/libs/release/libs/coroutine/) - [コルーチン](https://ja.wikipedia.org/wiki/コルーチン "wikilink")
      - [fiber](https://www.boost.org/doc/libs/release/libs/fiber/) - [ファイバー](https://ja.wikipedia.org/wiki/ファイバー_\(コンピュータ\) "wikilink")
      - [compute](https://www.boost.org/doc/libs/release/libs/compute/) - [OpenCL](../Page/OpenCL.md "wikilink")ベースのマルチコア[CPU](../Page/CPU.md "wikilink")/[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")演算プラットフォームインターフェイス
  - [コンテナ](../Page/コンテナ_\(データ型\).md "wikilink")
      - [array](https://www.boost.org/doc/libs/release/libs/array/) - STLコンテナ方式による固定長配列の管理
      - [Boost Graph Library (BGL)](https://www.boost.org/doc/libs/release/libs/graph/) - 総称的グラフコンテナ、コンポーネント、アルゴリズム
      - [multi-array](https://www.boost.org/doc/libs/release/libs/multi_array/) - N次元配列の生成の単純化
      - [multi-index containers](https://www.boost.org/doc/libs/release/libs/multi_index/) - 異なるソートとアクセス[セマンティクス](https://ja.wikipedia.org/wiki/セマンティクス "wikilink")を可能にするビルトインインデックスのあるコンテナ
      - [pointer containers](https://www.boost.org/doc/libs/release/libs/ptr_container/) - 値へのポインタを素直に管理できるようにする標準的なSTLコンテナをモデルにしたコンテナ
      - [property map](https://www.boost.org/doc/libs/release/libs/property_map/) - コンセプト的なインターフェイス仕様とキー値をオブジェクトにマップするための多目的インターフェイス
      - [variant](https://www.boost.org/doc/libs/release/libs/variant/) - コンパイル時に指定する型の集合から選べる型オブジェクトの効率的なストレージと、それにアクセスする型安全で総称的なスタックベースのオブジェクトコンテナ
  - 正当性と[テスト](https://ja.wikipedia.org/wiki/ソフトウェアテスト "wikilink")
      - [concept check](https://www.boost.org/doc/libs/release/libs/concept_check/) - 指定可能なテンプレートパラメータ（コンセプト）を制限できるようにする
      - [static assert](https://www.boost.org/doc/libs/release/libs/static_assert/) - コンパイル時アサートのサポート
      - [Boost Test Library](https://www.boost.org/doc/libs/release/libs/test/) - テストプログラムの作成、テストケースとテストスイートによるテストの構成、そしてそれらの実行制御のためのコンポーネントの組み合わせ。
  - [データ構造](../Page/データ構造.md "wikilink")
      - [dynamic_bitset](https://www.boost.org/doc/libs/release/libs/dynamic_bitset/dynamic_bitset.html) - 動的な`std::bitset-`に似たデータ構造
  - [関数オブジェクト](https://ja.wikipedia.org/wiki/関数オブジェクト "wikilink")と[高階プログラミング](../Page/高階関数.md "wikilink") （無名関数など）
      - [bind](https://www.boost.org/doc/libs/release/libs/bind/)と[mem_fn](https://www.boost.org/doc/libs/release/libs/bind/mem_fn.html) - 関数、関数オブジェクト、関数ポインタおよびメンバ関数のための汎用バインダ
      - [function](https://www.boost.org/doc/libs/release/libs/function/) - 遅延呼び出しのための関数オブジェクトのラッパ。[コールバックのための汎用的なメカニズムも提供される](../Page/コールバック_\(情報工学\).md "wikilink")。
      - [functional](https://www.boost.org/doc/libs/release/libs/functional/) - C++標準ライブラリで定義される関数オブジェクトのアダプタの強化。以下の内容を含む。
          - [function object traits](https://www.boost.org/doc/libs/release/libs/functional/function_traits.html)
          - [negators](https://www.boost.org/doc/libs/release/libs/functional/negators.html)
          - [binders](https://www.boost.org/doc/libs/release/libs/functional/binders.html)
          - [adapters for pointers to functions](https://www.boost.org/doc/libs/release/libs/functional/ptr_fun.html)
          - [adapters for pointers to member functions](https://www.boost.org/doc/libs/release/libs/functional/mem_fun.html)
      - [hash](https://www.boost.org/doc/libs/release/doc/html/hash.html) - C++ Technical Report 1 (TR1) で定義されているハッシュ関数オブジェクトの実装。ソートされていない連想コンテナのデフォルトのハッシュ関数として利用できる。
      - [lambda](https://www.boost.org/doc/libs/release/libs/lambda/) - [ラムダ抽象化の考え方で](../Page/ラムダ計算.md "wikilink")、小さい無名関数オブジェクトを定義できるようにして、プレースフォルダを使用して、特にアルゴリズムからの遅延呼び出しを使って、呼び出し地点でのこれらのオブジェクトの操作を可能とする。
      - [ref](https://www.boost.org/doc/libs/release/libs/core/ref.html) - 標準C++の参照の能力を強化するため、特にテンプレート関数で利用するための、ユーティリティクラステンプレートを提供する。
      - [result_of](https://www.boost.org/doc/libs/release/libs/utility/utility.htm#result_of) - 関数オブジェクトの戻り値の型を取り出す。関数の型を定義するのに役立つ。
      - [signals2](https://www.boost.org/doc/libs/release/libs/signals2/) - 管理されたシグナルとスロットのコールバック実装
  - [総称プログラミング](https://ja.wikipedia.org/wiki/総称プログラミング "wikilink")
  - [Graphs](../Page/グラフ_\(データ構造\).md "wikilink")
  - [入出力](../Page/入出力.md "wikilink")
  - 言語間サポート（[Python](../Page/Python.md "wikilink")用）
  - [イテレータ](https://ja.wikipedia.org/wiki/イテレータ#C++ "wikilink")
      - [iterators](https://www.boost.org/doc/libs/release/libs/iterator/)
      - [operators](https://www.boost.org/doc/libs/release/libs/utility/operators.htm) - ユーザー定義のイテレーターのための演算子をオーバーロードしてクラスが算術計算に適用できるようにするクラステンプレート。
      - [tokenizer](https://www.boost.org/doc/libs/release/libs/tokenizer/) - シーケンス内に含まれるトークンのセットをコンテナとして見えるようにしてイテレーターでアクセスできるようにする。
  - [数学](../Page/数学.md "wikilink")と計算
      - [QVM](https://www.boost.org/doc/libs/release/libs/qvm/doc/index.html) - [3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")プログラミングで多用される固定サイズの[クォータニオン](https://ja.wikipedia.org/wiki/クォータニオン "wikilink")、[ベクトル](https://ja.wikipedia.org/wiki/ベクトル "wikilink")、[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")
  - メモリ（[参照カウント](../Page/参照カウント.md "wikilink")による[スマートポインタなど](../Page/ガベージコレクション.md "wikilink")）
      - [pool](https://www.boost.org/doc/libs/release/libs/pool/) - 分割されたストレージベースのシンプルなメモリ管理スキームを提供する。
      - [smart_ptr](https://www.boost.org/doc/libs/release/libs/smart_ptr/) - 様々なポインタ管理方式による[スマートポインタクラステンプレートのコレクション](../Page/ガベージコレクション.md "wikilink")。
          - [scoped_ptr](https://www.boost.org/doc/libs/release/libs/smart_ptr/doc/html/smart_ptr.html#scoped_ptr) - ポインタ（単一のオブジェクト）を所有する。
          - [scoped_array](https://www.boost.org/doc/libs/release/libs/smart_ptr/doc/html/smart_ptr.html#scoped_array) - 配列用のscoped_ptr。
          - [shared_ptr](https://www.boost.org/doc/libs/release/libs/smart_ptr/doc/html/smart_ptr.html#shared_ptr) - 他のshared_ptrと共有できるポインタ。最後のshared_ptrが破棄されたときにポインタを破棄する。
          - [shared_array](https://www.boost.org/doc/libs/release/libs/smart_ptr/doc/html/smart_ptr.html#shared_array) - 配列用のshared_ptr。
          - [weak_ptr](https://www.boost.org/doc/libs/release/libs/smart_ptr/doc/html/smart_ptr.html#weak_ptr) - すでにshared_ptrで管理されているオブジェクトへの「弱い」参照を提供する。
          - [intrusive_ptr](https://www.boost.org/doc/libs/release/libs/smart_ptr/doc/html/smart_ptr.html#intrusive_ptr) - ポインタが提供する参照カウンタを使用するshared_ptrに似たクラス。
      - [utility](https://www.boost.org/doc/libs/release/libs/utility/utility.htm) - 以下のようなその他のクラス。
          - [base from member idiom](https://www.boost.org/doc/libs/release/libs/utility/doc/html/base_from_member.html) - 派生クラスのコンストラクタの初期化子でベースクラスのメンバを初期化する必要のあるクラスのための回避策を提供する。
          - [checked delete](https://www.boost.org/doc/libs/release/libs/core/doc/html/core/checked_delete.html) - 不完全な型へのポインタを使用してオブジェクトまたはオブジェクトの配列を破棄しようとする試みをチェックする。
          - [next and prior functions](https://www.boost.org/doc/libs/release/libs/iterator/doc/html/iterator/algorithms/next_prior.html) - 特に操作の結果が異なるイテレーターに保存されている必要がある（つまりオリジナルのイテレーターを変更できない）場合に、前方向または両方向のイテレーターをより簡単に操作できる。
          - [noncopyable](https://www.boost.org/doc/libs/release/libs/core/doc/html/core/noncopyable.html) - コピーコンストラクタと代入演算子を禁止できる。
          - [addressof](https://www.boost.org/doc/libs/release/libs/core/doc/html/core/addressof.html) - operator&()演算子のオーバーロードをバイパスしてオブジェクトの実際のアドレスを取得できるようにする。
          - [result_of](https://www.boost.org/doc/libs/release/libs/utility/utility.htm#result_of) - 関数の型を定義するのに役立つ。
  - その他
  - [構文解析](../Page/構文解析.md "wikilink")
  - プリプロセッサメタプログラミング
  - [文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")とテキスト処理（[正規表現](../Page/正規表現.md "wikilink")など）
      - [lexical_cast](https://www.boost.org/doc/libs/release/libs/lexical_cast/) - テキストとの型変換
      - [format](https://www.boost.org/doc/libs/release/libs/format/) - タイプセーフな引数のフォーマット文字列
      - [iostreams](https://www.boost.org/doc/libs/release/libs/iostreams/) - 新しい送受信フィルタフレームワークのためのC++ストリームとストリームバッファの補助
      - [regex](https://www.boost.org/doc/libs/release/libs/regex/), [xpressive](https://www.boost.org/doc/libs/release/libs/xpressive/) - 正規表現のサポート
      - [Spirit](https://ja.wikipedia.org/wiki/:en:Spirit_Parser_Framework "wikilink") - オブジェクト指向的な再帰的下向き構文解析ジェネレーターのフレームワーク。
      - [string algorithms](https://www.boost.org/doc/libs/release/libs/algorithm/string/) - 文字列に関する様々なアルゴリズムのコレクション。
      - [tokenizer](https://www.boost.org/doc/libs/release/libs/tokenizer/) - 文字列やその他の文字シーケンスを[トークンで分割できるようにする](../Page/字句解析.md "wikilink")。
      - [wave](https://www.boost.org/doc/libs/release/libs/wave/) - [C99](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")のプリプロセッサ機能の標準に準拠した実装。使いやすいインターフェイスでラップされている。
  - [テンプレートメタプログラミング](../Page/テンプレートメタプログラミング.md "wikilink")
      - [mpl](https://www.boost.org/doc/libs/release/libs/mpl/) - コンパイル時のアルゴリズム、シーケンス、メタ関数の、多目的で高レベルのメタプログラミングフレームワーク。
      - [static assert](https://www.boost.org/doc/libs/release/libs/static_assert/) - コンパイル時アサートのサポート
      - [type traits](https://www.boost.org/doc/libs/release/libs/type_traits/) - 基礎的な型の属性を定義するテンプレート。
  - 不完全なコンパイラの回避手段

## 線型代数

Boostには、[BLASのレベル](https://ja.wikipedia.org/wiki/Basic_Linear_Algebra_Subprograms "wikilink")1、2、3の各演算を実装した**uBLAS**という[線型代数](../Page/線型代数学.md "wikilink") (linear algebra) ライブラリがある。

  - 以下はベクトルと行列の乗算方法を表している。

<!-- end list -->

``` cpp
#include <boost/numeric/ublas/vector.hpp>
#include <boost/numeric/ublas/matrix.hpp>
#include <boost/numeric/ublas/io.hpp>

using namespace boost::numeric::ublas;

/* "y = Ax" example */
int main ()
{
  vector<double> x (2);
  x(0) = 1; x(1) = 2;

  matrix<double> A(2,2);
  A(0,0) = 0; A(0,1) = 1;
  A(1,0) = 2; A(1,1) = 3;

  vector<double> y = prod(A, x);

  std::cout << y << std::endl;
  return 0;
}
```

## 乱数生成

Boostはディストリビューション非依存の[擬似乱数](../Page/擬似乱数.md "wikilink")と、具体的な生成器を構築するために組み合わせる疑似乱数 (PRNG) に依存しない確率分布を提供する。

  - 以下は[メルセンヌ・ツイスタ](../Page/メルセンヌ・ツイスタ.md "wikilink")生成器を利用した[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")よりサンプルする方法を表している。

<!-- end list -->

``` cpp
#include <boost/random.hpp>
#include <ctime>

using namespace boost;

double SampleNormal(double mean, double sigma)
{
  // 1970年からの秒でシードを一度初期化した
  // メルセンヌ・ツイスタ乱数生成器の作成
  static mt19937 rng(static_cast<unsigned>(std::time(0)));

  // ガウス確率分布を選択
  normal_distribution<double> norm_dist(mean, sigma);

  // 関数の形で乱数生成器を分布にバインドする。
  variate_generator<mt19937&, normal_distribution<double> > normal_sampler(rng, norm_dist);

  // 分布からサンプルする。
  return normal_sampler();
}
```

詳細は[Boost Random Number Library](https://www.boost.org/doc/libs/release/libs/random/)を参照。

## テキストのパース

Boost.Spirit - [バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink")に出来るだけ近い[C++](../Page/C++.md "wikilink")のプログラム形式で直接パーサを記述するという、Boostにおける最も複雑なライブラリのひとつ。

  - カンマ区切りの数値を読み込むパーサの例。

<!-- end list -->

``` cpp
#include <boost/spirit/core.hpp>
#include <boost/spirit/actor/push_back_actor.hpp>
#include <iostream>
#include <vector>
#include <string>

using namespace std;
using namespace boost::spirit;

// Parser comma-separated numbers
bool parse_numbers(const char* str, vector<double>& v)
{
  return parse(str,
    // Start grammar
    (
      real_p[push_back_a(v)] >> *(',' >> real_p[push_back_a(v)])
    )
    ,
    // End grammar
    space_p).full;
}
```

詳細は [Spirit User's Guide](https://www.boost.org/doc/libs/release/libs/spirit/) を参照。

## 正規表現の利用

Boost.Regex - [正規表現](../Page/正規表現.md "wikilink")を利用するライブラリ。フィルタ・検索・パース・テキスト処理に必要な各種関数を持っている。

Supports [PCRE](https://ja.wikipedia.org/wiki/PCRE "wikilink"), POSIX [BRE](https://ja.wikipedia.org/wiki/BRE "wikilink") and [ERE](https://ja.wikipedia.org/wiki/ERE "wikilink")

  - テキストをパースするプログラムの例。

<!-- end list -->

``` cpp
#include <boost/regex.hpp>
#include <vector>
#include <string>

// Example program parsing the URL
int main(int argc, char** argv)
{
  // Check the number of parameters
  if (argc < 2) return 0;

  // container for the values
  std::vector<std::string> values;
  // Expression to parse
  boost::regex expression(
//       proto                 host               port
        "^(\?:([^:/\?#]+)://)\?(\\w+[^/\?#:]*)(\?::(\\d+))\?"
//       path                  file       parameters
        "(/\?(\?:[^\?#/]*/)*)\?([^\?#]*)\?(\\\?(.*))\?"
    );
  // The formation of the source string to parse (taken from command-line)
  std::string src(argv[1]);

  // Parse and filling the container
  if (boost::regex_split(std::back_inserter(values), src, expression))
  {
    // Output the result
    const char* names[] = {"Protocol", "Host", "Port", "Path", "File", "Parameters", NULL};
    for (int i = 0; names[i]; i++)
      printf("%s: %s\n", names[i], values[i].c_str());
  }
  return 0;
}
```

詳細は [Boost.Regex](https://www.boost.org/doc/libs/release/libs/regex/) を参照。

### 動的な正規表現と静的な正規表現

Boost.Xpressiveは、動的な正規表現と静的な正規表現を提供する。 以下のプログラムは「私は2052/10/30に生まれた。」という文字列に対し、年月日を抽出する正規表現である。どちらも出力結果は同じである。

#### 動的な正規表現

``` cpp
#include <iostream>
#include <string>
#include <boost/xpressive/xpressive.hpp>

using namespace boost::xpressive;


int main()
{
    std::string str = "私は2052/10/30に生まれた。";

    sregex rx = sregex::compile(R"((\d{1,4})/(\d{1,2})/(\d{1,2}))");
    smatch m;

    if(regex_search(str, m, rx)) {
        for(const auto& e: m) {
            std::cout << e << std::endl;
        }
    }

}
```

#### 静的な正規表現

``` cpp
#include <iostream>
#include <string>
#include <boost/xpressive/xpressive.hpp>

using namespace boost::xpressive;


int main()
{
    std::string str = "私は2052/10/30に生まれた。";

    mark_tag years(1), month(2), days(3);

    sregex rx =
        (years = repeat<1, 4>(_d)) >> '/' >>
        (month = repeat<1, 2>(_d)) >> '/' >>
        (days = repeat<1, 2>(_d));

    smatch m;
    if(regex_search(str, m, rx))
    {
        std::cout << m[0] << std::endl;
        std::cout << m[years] << std::endl;
        std::cout << m[month] << std::endl;
        std::cout << m[days] << std::endl;
    }


}
```

## グラフのアルゴリズム

Boost.Graph - [グラフ理論](../Page/グラフ理論.md "wikilink")の複数の視点および多数のアルゴリズムの形で、[グラフ概念の柔軟かつ効果的な実装を提供する](../Page/グラフ_\(データ構造\).md "wikilink")。

  - アルゴリズムの例：[トポロジカルソート](https://ja.wikipedia.org/wiki/トポロジカルソート "wikilink")

<!-- end list -->

``` cpp
#include <iostream>
#include <list>
#include <algorithm>
#include <boost/graph/adjacency_list.hpp>
#include <boost/graph/topological_sort.hpp>
#include <iterator>
#include <utility>

int main(int , char* [])
{
  using namespace boost;

  // Type of graph
  typedef adjacency_list<vecS, vecS, directedS,
    property<vertex_color_t, default_color_type> > Graph;
  // Handle vertices
  typedef boost::graph_traits<Graph>::vertex_descriptor Vertex;
  // Container for the chain of vertices
  typedef std::vector<Vertex> container;
  // Type of representation of arcs
  typedef std::pair<std::size_t,std::size_t> Pair;

  // Edges of the graph
  Pair edges[6] = {
    Pair(0,1), Pair(2,4),
    Pair(2,5),
    Pair(0,3), Pair(1,4),
    Pair(4,3)
  };
  // Count
  Graph G(edges, edges + 6, 6);
  // Dictionary to get a handle on the numbers of vertices vertices
  boost::property_map<Graph, vertex_index_t>::type id = get(vertex_index, G);
  // Container for storing the sorted vertices
  container c;

  // Execute algorithm
  topological_sort(G, std::back_inserter(c));

  // Output results: sorting descriptors of the graph in the container,
  // Get the serial number of vertices
  std::cout << "Topological check:";
  for (container::reverse_iterator ii = c.rbegin(); ii != c.rend(); ++ii)
    std::cout << id[*ii] << " ";
  std::cout << std::endl;

  return 0;
}
```

詳細は [The Boost Graph Library](https://www.boost.org/doc/libs/release/libs/graph/) を参照。

## マルチスレッド

スレッドを生成しているコードの例

``` cpp
#include <boost/thread/thread.hpp>
#include <iostream>
using namespace std;

void hello_world()
{
  cout << "Hello world, I'm a thread!" << endl;
}

int main()
{
  // hello_world関数を呼び出す新しいスレッドを起動する。
  boost::thread my_thread(&hello_world);
  // スレッドが終了するまで待つ。
  my_thread.join();

  return 0;
}
```

  - [Introduction to Boost.Threads](http://www.ddj.com/dept/cpp/184401518) in [Dr. Dobb's Journal](https://ja.wikipedia.org/wiki/Dr._Dobb's_Journal "wikilink").
  - Boost.Threads [API reference](https://www.boost.org/doc/libs/release/libs/thread/).
  - [threadpool library](http://threadpool.sourceforge.net) based on Boost.Thread

## 外部リンク

  - [Boost Webサイト（英語）](https://www.boost.org/)
      - [ライブラリ一覧（英語）](https://www.boost.org/doc/libs/)
  - [Let's Boost(日本語)](http://www.kmonos.net/alang/boost/)
  - [boostjp : Boost C++ Libraries日本語リファレンスサイト](https://boostjp.github.com/)

[Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:コンピュータに関連する組織](https://ja.wikipedia.org/wiki/Category:コンピュータに関連する組織 "wikilink")