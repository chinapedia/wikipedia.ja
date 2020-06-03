> この記事は[Lua](https://ja.wikipedia.org/wiki/Lua)から翻訳されています。


（ルア）は、の、主としてDepartment of Computer Science（[コンピュータ科学](https://ja.wikipedia.org/wiki/コンピュータ科学 "wikilink")科）and・or Computer Graphics Technology Group (Tecgraf) に属する、[Roberto Ierusalimschy](https://ja.wikipedia.org/wiki/ロベルト・イエルサリムスキー "wikilink"), Waldemar Celes, Luiz Henrique de Figueiredo らによって設計開発された[スクリプト言語](../Page/スクリプト言語.md "wikilink")およびその処理系の実装である。

[手続き型言語として](../Page/手続き型プログラミング.md "wikilink")、また、[プロトタイプベース](../Page/プロトタイプベース.md "wikilink")の[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")としても利用することができ、[関数型言語](../Page/関数型言語.md "wikilink")、データ駆動型としての要素も併せ持っている。

Luaという名前は、[ポルトガル語](https://ja.wikipedia.org/wiki/ポルトガル語 "wikilink")の[月](https://ja.wikipedia.org/wiki/月 "wikilink")に由来する。

## 概要

Luaは、[C言語](../Page/C言語.md "wikilink")のホストプログラムに組み込まれることを目的に設計されており、高速な動作と、高い移植性、組み込みの容易さが特徴である。いったん[バイトコード](../Page/バイトコード.md "wikilink")にコンパイルされ、Lua VMで実行される。**LuaJIT**は The Computer Language Benchmarks Game によると、変数に型のないスクリプト言語では最速の言語・処理系である\[1\]。

の2011年6月版では10番目に人気なプログラミング言語である\[2\]。2007年に人気が急上昇した\[3\]。2009年2月の調査で、ゲーム開発者がイベントスクリプト等の内部処理に利用する言語として、最も利用例が多いと報告されるなど、はゲーム産業での利用が広がっている\[4\]。

[MITライセンスのもと配布されているため商用プロダクトにも組み込みやすい点も高く評価されている](../Page/MIT_License.md "wikilink")。

## 特徴

Luaの特徴としては、汎用性が高いが比較的容易に実装が可能である、というものである。実際のところLuaは、オブジェクト指向などといった他の要素としての働きを明白にはサポートしていないが、サポートしていない範囲においても容易に拡張が可能である。また前述のような、動作の高速性や優れた移植性なども大きな特徴である。

文法的な特徴としては、[Pascal](../Page/Pascal.md "wikilink")によく似た構文を採用していること、[コルーチン](../Page/コルーチン.md "wikilink")（[協調的マルチタスク](https://ja.wikipedia.org/wiki/マルチタスク#ノンプリエンプティブ・マルチタスク "wikilink")）のサポート、数値型は[整数](../Page/整数.md "wikilink")と[浮動小数点数](../Page/浮動小数点数.md "wikilink")の区別がないこと、関数を変数として扱えることなどが挙げられる。

Luaはいわゆる[汎用スクリプト言語であり](https://ja.wikipedia.org/wiki/スクリプト言語#汎用動的言語 "wikilink")、特定の用途に限定されない性質を持つが、同じく汎用スクリプト言語である [Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")と比較して高速に動作する。これはLuaの理念である、簡素、高効率、高移植性を目指した実装の産物である。また、Luaにおけるテーブル（[連想配列](../Page/連想配列.md "wikilink")）の実装はかなり最適化されており、特にキーに数値のみを使用した場合は、単純な配列としてさらに高速に動作するようになる。

Lua 5.0以前はメモリ管理にマーク & スイープ方式の[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")が使用されていたが、Lua 5.1ではメモリ管理にインクリメンタル・ガベージコレクションが採用され、リアルタイム用途における性能の改善が図られている。ガベージコレクションの実装形態も Lua の高速動作および高リアルタイム性能に一役買っている。

## LuaJIT

Luaの[JITコンパイラである](../Page/実行時コンパイラ.md "wikilink") LuaJITがMike Pallにより開発されている。変数に型がないにもかかわらず、Javaよりも少し遅くなる程度の速度で動いている\[5\]。[静的単一代入](https://ja.wikipedia.org/wiki/静的単一代入 "wikilink")などをつかった高度な最適化が行われており、バイトコードを実行する場合と比べて、数倍から数100倍の高速化が期待できる\[6\]。

## Luaの歴史

### Lua

  - 1993年7月28日 - Lua 1.0 リリース。
  - 1995年2月7日 - Lua 2.1 リリース。
  - 1997年7月1日 - Lua 3.0 リリース。
  - 2000年11月6日 - Lua 4.0 リリース。
  - 2003年4月11日 - Lua 5.0 リリース。MITライセンスの採用。
  - 2006年2月21日 - Lua 5.1 リリース。インクリメンタルGCの採用。
  - 2008年8月22日 - Lua 5.1.4 リリース。
  - 2010年5月14日 - Lua 5.1.4-2 リリース。
  - 2011年12月16日 - Lua 5.2.0 リリース。[ビット演算](../Page/ビット演算.md "wikilink")ライブラリをサポート。
  - 2012年6月14日 - Lua 5.2.1 リリース。
  - 2013年3月27日 - Lua 5.2.2 リリース。
  - 2013年12月7日 - Lua 5.2.3 リリース。
  - 2015年1月6日 - Lua 5.3.0 リリース。整数型およびビット演算子のサポートなど。

### LuaJIT

  - 2005年9月8日 - LuaJIT 1.0.3 リリース。最初の公開版。
  - 2006年3月13日 - LuaJIT 1.1.0 リリース。Lua 5.1対応。
  - 2006年6月24日 - LuaJIT 1.1.2 リリース。
  - 2007年5月24日 - LuaJIT 1.1.3 リリース。
  - 2008年2月5日 - LuaJIT 1.1.4 リリース。
  - 2008年10月25日 - LuaJIT 1.1.5 リリース。
  - 2010年3月28日 - LuaJIT 1.1.6 リリース。
  - 2011年5月5日 - LuaJIT 1.1.7 リリース。
  - 2012年4月16日 - LuaJIT 1.1.8 リリース。
  - 2012年11月8日 - LuaJIT 2.0.0 リリース。
  - 2013年2月19日 - LuaJIT 2.0.1 リリース。
  - 2013年6月3日 - LuaJIT 2.0.2 リリース。
  - 2014年3月12日 - LuaJIT 2.0.3 リリース。
  - 2015年5月14日 - LuaJIT 2.0.4 リリース。
  - 2017年5月1日 - LuaJIT 2.0.5 リリース。

## コード例

### Hello World

``` lua
print("Hello World")
```

### [挿入ソート](../Page/挿入ソート.md "wikilink")

``` lua
-- `--´から行末までコメント
local a = {5, 3, 1, 4, 2} -- `{´と`}´はテーブルコンストラクタ
for i = 2, #a do -- `#´は長さ演算子であり、`#a´はテーブルaのサイズ（ここでは5）を返す
    for j = i, 2, -1 do
        if a[j - 1] <= a[j] then break end
        a[j], a[j - 1] = a[j - 1], a[j]
    end
end
```

### コルーチン

コルーチンは状態遷移を記述するのに便利である。

``` lua
-- Lua コルーチンによって非同期の状態遷移を同期的に記述する例。

-- 1を返している間は動作を続行中。0を返すと動作を完了。
function doAction()
  -- 4フレーム分だけ左へ移動。
  for i = 1, 4, 1 do
    print("Move Left " .. i)
    coroutine.yield(1)
  end
  -- 1フレーム分だけ一時停止。
  print("Pause")
  coroutine.yield(1)
  -- 3フレーム分だけ右へ移動。
  for i = 1, 3, 1 do
    print("Move Right " .. i)
    coroutine.yield(1)
  end
  print("End")
  return 0
end

local doActionAsync = coroutine.wrap(doAction)

-- コルーチンの動作テスト。
-- 実際にはフレームごとに1回だけ呼び出す。
while doActionAsync() ~= 0 do
end
```

### 正規表現

Luaは[POSIX](../Page/POSIX.md "wikilink")や[ECMAScript](../Page/ECMAScript.md "wikilink")標準の[正規表現](../Page/正規表現.md "wikilink")とは異なる独自のカスタムパターンマッチングをサポートする\[7\]。

``` lua
local myTable = {
  "Gnome,160,30",
  "Sylph,100,70",
  "Salamander,200,20",
  "Ondine,140,60",
}
for i = 1, #myTable do
  local name, hp, mp = string.match(myTable[i], "([^,]+)%,([^,]+)%,(.+)")
  print(string.format("Name = %q, HP = %d, MP = %d", name, tonumber(hp), tonumber(mp)))
end
```

## LuaとC/C++の相互運用

LuaにはC言語向けの相互運用[APIが用意されている](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")。LuaからC/C++の関数を呼び出すためには以下の方法を用いる。下記のコードはC/C++の関数をLua VMに登録し、Luaスクリプト側から呼び出している。

``` cpp
#include <cstdio>
#include <cstdlib>
#include <lua.h>
#include <lauxlib.h>

int my_add(lua_State* L) {
    const int x = (int)lua_tonumber(L, 1); // 第1引数の取得。
    const int y = (int)lua_tonumber(L, 2); // 第2引数の取得。
    lua_settop(L, 0); // スタックのクリア。
    const int ret = x + y; // C/C++ 側での演算。
    lua_pushnumber(L, ret); // 返却値をプッシュ。
    return 1;
}

int main(int argc, char* argv[]) {
    lua_State* L = luaL_newstate(); // Lua VM の初期化。
    luaL_openlibs(L); // Lua の標準ライブラリを使えるようにする。
    lua_register(L, "my_add", my_add); // Lua VM に C/C++ 関数を登録。
    // my_add 関数を呼び出す Lua スクリプトを実行。
    if (luaL_dostring(L, "print(my_add(5, 3))")) {
        lua_close(L); // Lua VM を閉じる。
        return EXIT_FAILURE; // エラー終了。
    }
    lua_close(L);
    return EXIT_SUCCESS;
}
```

逆に、C/C++からLuaの関数を呼び出す際にもスタック操作が必要となる。

``` cpp
#include <cstdio>
#include <cstdlib>
#include <lua.h>
#include <lauxlib.h>

int main(int argc, char* argv[]) {
    lua_State* L = luaL_newstate(); // Lua VM の初期化。
    // add_func 関数を定義する Lua スクリプトを実行。
    if (luaL_dostring(L, "function add_func(x, y) return x + y end")) {
        lua_close(L); // Lua VM を閉じる。
        return EXIT_FAILURE; // エラー終了。
    }
    lua_getglobal(L, "add_func"); // Lua のグローバルオブジェクトである「add_func」を取得し、スタックに積む。
    lua_pushinteger(L, 5); // 整数値の「5」を Lua スタックにプッシュ。
    lua_pushinteger(L, 3); // 整数値の「3」を Lua スタックにプッシュ。
    lua_call(L, 2, 1); // Lua 側で実装した add_func 関数を呼び出す。引数の数は2、結果の数は1。
    printf("Result: %d\n", lua_tointeger(L, -1)); // 結果を表示。
    lua_close(L);
    return EXIT_SUCCESS;
}
```

## 言語バインディングの例

Luaの他言語用バインディングは公式には提供されていないが、有志によるサードパーティ製ライブラリやツールがいくつか存在する。バインディングを使うと、前述のような煩雑なスタック操作を明示的に記述することなく、簡潔に相互運用できるようになる。

### C++

Luaを[C++](../Page/C++.md "wikilink")言語で記述されたホストプログラムへ組み込むための省力化ツール（コードジェネレーター）および言語バインディングとして、toLua\[8\]、 tolua++（Lua 5.2非対応）\[9\]、Luabind（Lua 5.2非対応）\[10\]、Selene\[11\]、Sol\[12\]、Sol2\[13\]などが開発されている。

以下にSol2を使った例を示す（[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")および[C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")の機能を利用するため、対応コンパイラが必要）。

  - LuaからC/C++の関数を呼び出す例:

<!-- end list -->

``` cpp
#include <iostream>
#include <sol.hpp>

int add(int x, int y) {
    return x + y;
}

int main() {
    // Luaの初期化
    sol::state lua;

    // Luaの標準ライブラリをすべて開く
    lua.open_libraries(sol::lib::base, sol::lib::coroutine, sol::lib::debug, sol::lib::debug,
        sol::lib::io, sol::lib::math, sol::lib::os,
        sol::lib::package, sol::lib::string, sol::lib::table, sol::lib::utf8);

    // LuaにC/C++の関数を登録
    lua["add"] = add;

    // Luaスクリプトの読み込み
    try {
        lua.safe_script_file("test.lua");
    } catch (const sol::error& e) {
        std::cout << e.what() << std::endl;
    }
}
```

C/C++の関数を呼び出すLuaスクリプト (test.lua):

``` lua
print(add(100, 200)) -- 「300」と表示される
```

  - C++からLuaの関数を呼び出す例:

<!-- end list -->

``` cpp
#include <iostream>
#include <sol.hpp>

int main() {
    // Luaの初期化
    sol::state lua;

    // Luaの標準ライブラリをすべて開く
    lua.open_libraries(sol::lib::base, sol::lib::coroutine, sol::lib::debug, sol::lib::debug,
        sol::lib::io, sol::lib::math, sol::lib::os,
        sol::lib::package, sol::lib::string, sol::lib::table, sol::lib::utf8);

    // Luaスクリプトの読み込み
    try {
        lua.safe_script_file("test.lua");
    } catch (const sol::error& e) {
        std::cout << e.what() << std::endl;
    }

    // Luaの関数を呼び出す
    sol::function_result ret = lua["add"](100, 200);

    // 結果を表示する
    std::cout << ret.get<int>() << std::endl;
}
```

C++から呼び出される関数を定義するLuaスクリプト (test.lua):

``` lua
function add(a, b)
    return a + b
end
```

### Java

[Luaj](http://www.luaj.org/luaj.html)という[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")向けの実装がある。[Luaj 3.0](http://www.luaj.org/luaj/3.0/README.html)は、Lua 5.2相当の仕様をJavaで実装しなおしたものであり、Javaのクラスからバインダ無しでインスタンスを生成したりメソッドを呼び出したりすることが可能である。そのほか、LuaのC APIを[JNI経由でJavaから利用可能にするJNLua](../Page/Java_Native_Interface.md "wikilink")\[14\]が存在する。

### .NET

[C\#や](../Page/C_Sharp.md "wikilink")[VB.NETといった](../Page/Visual_Basic_.NET.md "wikilink")[.NET Framework言語向けのバインディングとして](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、LunaRoad\[15\]が存在する。C\#で書かれたLua[インタプリタ](../Page/インタプリタ.md "wikilink")としてMoonSharp\[16\]が存在する。また、[DLR上に実装されたNeoLua](https://ja.wikipedia.org/wiki/Dynamic_Language_Runtime "wikilink")\[17\]が存在する。

## Luaを採用している製品

### ゲーム

  - [Blue Mars](https://ja.wikipedia.org/wiki/Blue_Mars "wikilink")
  - [CRYSIS](../Page/CRYSIS.md "wikilink")
  - [Far Cry](../Page/Far_Cry.md "wikilink")
  - [Factorio](https://ja.wikipedia.org/wiki/Factorio "wikilink")
  - [From the depths](https://ja.wikipedia.org/wiki/From_the_depths "wikilink")
  - [Garry's MOD](https://ja.wikipedia.org/wiki/Garry's_MOD "wikilink")
  - [Lost Wind](https://ja.wikipedia.org/wiki/Lost_Wind "wikilink")
  - [RagnarokOnline](https://ja.wikipedia.org/wiki/RagnarokOnline "wikilink")\[18\]
  - [Roblox](https://ja.wikipedia.org/wiki/Roblox "wikilink")
  - [Xenepic Online Revo](https://ja.wikipedia.org/wiki/Xenepic_Online_Revo "wikilink")
  - [ソニック・ザ・ヘッジホッグ (2006年のゲーム)](../Page/ソニック・ザ・ヘッジホッグ_\(2006年のゲーム\).md "wikilink")
  - [ソニック ワールドアドベンチャー](https://ja.wikipedia.org/wiki/ソニック_ワールドアドベンチャー "wikilink")（北米版のタイトルは[Sonic Unleashed](https://ja.wikipedia.org/wiki/Sonic_Unleashed "wikilink")）
  - [ティアーズ・トゥ・ティアラ 花冠の大地](../Page/ティアーズ・トゥ・ティアラ_花冠の大地.md "wikilink")
  - [THE IDOLM@STER 2](https://ja.wikipedia.org/wiki/THE_IDOLM@STER_2 "wikilink")
  - Warhammer Online:Age of Reckoning
  - [World of Warcraft](../Page/World_of_Warcraft.md "wikilink")
  - [カンパニー・オブ・ヒーローズ](../Page/カンパニー・オブ・ヒーローズ.md "wikilink")
  - [GRAVITY DAZE](https://ja.wikipedia.org/wiki/GRAVITY_DAZE "wikilink")
  - ニンテンドークラシックミニ ファミリーコンピューター (エミュレータシステム kachikachi のゲーム選択画面で使用)
  - [PHANTASY STAR ONLINE 2](https://ja.wikipedia.org/wiki/ファンタシースターオンライン2 "wikilink")
  - [ファイナルファンタジーXIV](https://ja.wikipedia.org/wiki/ファイナルファンタジーXIV "wikilink")\[19\]
  - [ドラゴンクエストX](https://ja.wikipedia.org/wiki/ドラゴンクエストX_目覚めし五つの種族_オンライン "wikilink")\[20\]

### ゲーム以外

  - [3DMLW](https://ja.wikipedia.org/wiki/3DMLW "wikilink")プラグイン

  - [Adobe Photoshop Lightroom](../Page/Adobe_Photoshop_Lightroom.md "wikilink")

  - [Aegisub](https://ja.wikipedia.org/wiki/Aegisub "wikilink")

  - [Anime Studio](https://ja.wikipedia.org/wiki/Anime_Studio "wikilink")

  - Apache mod_lua

  - Asterisk extensions.lua

  - [AviUtl](../Page/AviUtl.md "wikilink")

  - Computercraft - [Minecraft](https://ja.wikipedia.org/wiki/Minecraft "wikilink")の[MOD](https://ja.wikipedia.org/wiki/MOD "wikilink")

  - [FlashAir](https://ja.wikipedia.org/wiki/FlashAir "wikilink") - [無線LAN](../Page/無線LAN.md "wikilink")機能を搭載した[東芝](../Page/東芝.md "wikilink")製SDHC[メモリーカード](../Page/メモリーカード.md "wikilink")\[21\]

  - FLOW - 設定に使われている\[22\]

  - [LuaTeX](https://ja.wikipedia.org/wiki/LuaTeX "wikilink")

  - [MediaWiki](../Page/MediaWiki.md "wikilink")（[Scribunto拡張により](https://ja.wikipedia.org/wiki/mediawikiwiki:Extension:Scribunto "wikilink")）

  - [MySQL Proxy](https://ja.wikipedia.org/wiki/MySQL_Proxy "wikilink")

  - [Nginx](https://ja.wikipedia.org/wiki/Nginx "wikilink")

  - [nmap](https://ja.wikipedia.org/wiki/nmap "wikilink")

  - OpenResty\[23\]

  - [OpenWrt](https://ja.wikipedia.org/wiki/OpenWrt "wikilink")

  - osm2pgsql - [OpenStreetMap](https://ja.wikipedia.org/wiki/OpenStreetMap "wikilink")のデータを[PostGIS](https://ja.wikipedia.org/wiki/PostGIS "wikilink")に読み込むユーティリティ\[24\]

  -
  - [Redis](https://ja.wikipedia.org/wiki/Redis "wikilink")

  - [RigidChips](../Page/RigidChips.md "wikilink")

  - [Renoise](https://ja.wikipedia.org/wiki/Renoise "wikilink")

  - [Strata 3D](../Page/Strata_3D.md "wikilink")

  - [Tachyon](https://ja.wikipedia.org/wiki/Tachyon "wikilink")

  - TileMan\[25\]

  - [ヤマハ](../Page/ヤマハ.md "wikilink")の[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink") (RTX1200、RTX810、SRT100、NVR500、FWX120)\[26\]

  - [Vim](../Page/Vim.md "wikilink") - ビルド時に有効化することで拡張スクリプト内でLuaを使用できる、派生のNeovimではLuaJITが内部的に利用されており組み込まれている

  - [VLC Media Player](https://ja.wikipedia.org/wiki/VLC_Media_Player "wikilink")

  - [VOCALOID](../Page/VOCALOID.md "wikilink")3 - ユーザー側で歌唱合成用データを加工するエフェクタを自作できる\[27\]

  - [Wireshark](../Page/Wireshark.md "wikilink")

  - （ドキュメントはを参照）。

## 脚注

## 関連書籍

  -
  -
  -
  -
  -
  -
## 関連項目

  - [Squirrel](https://ja.wikipedia.org/wiki/Squirrel "wikilink")
  - [グルー言語](../Page/グルー言語.md "wikilink")
  - [Wikipedia:Lua](https://ja.wikipedia.org/wiki/Wikipedia:Lua "wikilink") - ウィキペディアにおけるLuaの解説ページ。
  - [SciTE](https://ja.wikipedia.org/wiki/SciTE "wikilink")

## 外部リンク

  -
  - [Lua 5.3 Reference Manual](https://www.lua.org/manual/5.3/) - 公式の言語リファレンスマニュアル

  - [Lua 5.3 リファレンスマニュアル](http://milkpot.sakura.ne.jp/lua/lua53_manual_ja.html) - 原著者に無断で日本語に訳した非公式のLua 5.3リファレンスマニュアル

  - [Lua言語の紹介 産業技術総合研究所](https://staff.aist.go.jp/yutaka.ueno/lua/docsjp.html)

  - [Luaj](https://sourceforge.net/projects/luaj/)

  - [Lua入門講座](http://starcode.web.fc2.com/)

  - [広井誠:「お気楽 Lua プログラミング超入門」](http://www.nct9.ne.jp/m_hiroi/light/lua.html)

  - [C/C++ 言語プログラマのための Lua 入門リファレンス](https://ifritjp.github.io/documents/lua/)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:仮想機械](https://ja.wikipedia.org/wiki/Category:仮想機械 "wikilink")

1.  [x64 Ubuntu:Intel®Q6600®one core Computer Language Benchmarks Game](http://shootout.alioth.debian.org/u64/which-programming-languages-are-fastest.php)
2.  [TIOBE Programming Community Index](http://www.tiobe.com/index.php/content/paperinfo/tpci/index.html)
3.  [The Lua Programming Language - TIOBE Software:The Coding Standards Company](http://www.tiobe.com/index.php/paperinfo/tpci/Lua.html)
4.  [Satori » The Engine Survey:General results](http://www.satori.org/2009/03/the-engine-survey-general-results/)
5.
6.  <http://luajit.org/performance.html>
7.  [スクリプト化可能なアプリケーションに Lua を組み込む](https://www.ibm.com/developerworks/jp/linux/library/l-embed-lua/)
8.  [toLua home page](http://webserver2.tecgraf.puc-rio.br/~celes/tolua/)
9.
10.
11. [jeremyong/Selene: Simple C++11 friendly header-only bindings to Lua](https://github.com/jeremyong/Selene)
12. [Rapptz/sol: A C++11 Lua wrapper](https://github.com/Rapptz/sol)
13. [ThePhD/sol2: Sol v2.0 - a C++ \<-\> Lua API wrapper with advanced features and top notch performance - is here, and it's great\! Documentation:](https://github.com/ThePhD/sol2)
14. [JNLua (Java Native Lua) | Google Code Archive - Long-term storage for Google Code Project Hosting.](https://code.google.com/archive/p/jnlua/)
15. [3F/LunaRoad: Lua C API for .NET :: LunaRoad represents flexible platform for work with Lua 5.1, 5.2, 5.3 ....](https://github.com/3F/LunaRoad)
16. [MoonSharp](http://www.moonsharp.org/)
17. [neolithos/neolua: A Lua implementation for the Dynamic Language Runtime (DLR).](https://github.com/neolithos/neolua)
18.
19. [「FFXIV:新生エオルゼア」プロデューサー吉田直樹氏インタビュー](http://game.watch.impress.co.jp/docs/interview/20121122_573208.html)
20. WEB+DB PRESS Vol.90 特集2 ドラゴンクエストX開発ノウハウ大公開 国民的RPGオンライン化へのチャレンジ
21. [FlashAir Developers - ドキュメント - APIガイド - Lua機能](https://flashair-developers.com/ja/documents/api/lua/)
22.
23.
24.
25.
26.
27. [ボーカロイドストア](http://shop.vocaloidstore.com)でAPIリファレンスを配布している。