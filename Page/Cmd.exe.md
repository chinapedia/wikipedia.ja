> この記事は[Cmd.exe](https://ja.wikipedia.org/wiki/Cmd.exe)から翻訳されています。


**cmd.exe**は[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")や[NT系Windows](../Page/Windows_NT系.md "wikilink")、[Windows CEに搭載されている](https://ja.wikipedia.org/wiki/Microsoft_Windows_CE "wikilink")[コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink")である。英語版のショートカットには「**Command Prompt**」、日本語版のショートカットには「**コマンド プロンプト**」という名称が付けられている\[1\]。[MS-DOS](../Page/MS-DOS.md "wikilink")から[Windows 9xに渡って用いられた](../Page/Windows_9x系.md "wikilink")[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")（および[DOSプロンプト](../Page/DOSプロンプト.md "wikilink")）と類似の機能を持つ。[Win32コンソール](https://ja.wikipedia.org/wiki/Win32コンソール "wikilink")[APIを利用して実装されている](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")。cmd.exeはWindowsコマンド\[2\]をプログラムコードとして対話的に入力・評価・実行できる[REPL](https://ja.wikipedia.org/wiki/REPL "wikilink")環境であり、またコマンドを記述したプログラムソースファイルは[バッチファイル](../Page/バッチファイル.md "wikilink")と呼ばれる。

64ビット版Windowsでは、64ビットのcmd.exeと、[WOW64](../Page/WOW64.md "wikilink")で実行される32ビットのcmd.exeがインストールされている。Windows 9x系のDOSプロンプトがMS-DOS仮想マシン上で動く16bitプログラムなのに対して、cmd.exeは32bitもしくは64bitで動作するコンソールプログラムである。

cmd.exeはCOMMAND.COMと比べ、相当に機能向上が図られている。一旦は[エスケープシーケンス](../Page/エスケープシーケンス.md "wikilink")の機能が削られたが、Windows 10 1607で復活\[3\]し、VT100互換のエスケープシーケンスが使用できるようになった。

## 新機能

WindowsにおいてコマンドプロンプトはCOMMAND.COMとある程度の互換性を持つが、次の拡張が施されている。

  - COMMAND.COMでの「[コマンドまたはファイル名が違います](https://ja.wikipedia.org/wiki/コマンドまたはファイル名が違います "wikilink")。」よりも詳細なメッセージを出力するようになった。OS/2ではシステムで選択された言語でエラーが表示され、そのメッセージは「システムメッセージファイル」より取得される。
  - 矢印キーを使ったコマンド履歴のスクロールをサポート。この機能はCOMMAND.COMでは外部コマンドのDOSKEYでサポートされていた。
  - ファイルやフォルダーパスのコマンドライン補完をサポート（既定ではキーに割り当てられている）
  - 「^」を[エスケープ文字](../Page/エスケープ文字.md "wikilink")として扱う。つまり、次のコマンドプロンプトで特別な意味を持つ文字の前にキャレットを付けることで、[リテラル](../Page/リテラル.md "wikilink")として扱うことができる。（例：`<`, `>`, `*`, `?`, `|`）
  - バッチ処理において変数の遅延展開をサポート（Windows 2000以降）

また、内部コマンドが次のように改善されている。

  - `DelTree`コマンド（ディレクトリとそれ以下のファイル・ディレクトリを削除）は`RD`コマンドに`/S`スイッチとして統合。
  - `SetLocal`コマンドや`EndLocal`コマンドで環境の[スコープ](../Page/スコープ.md "wikilink")を限定。例えば、SetLocalコマンド後にバッチファイルなどにより変更された環境変数は、EndLocalコマンドを実行するとSetLocalコマンド実行前の状態に復元される。
  - `Call`コマンドでバッチファイル内のサブルーチンの呼び出しをサポートした。COMMAND.COMでは外部バッチファイルの呼び出しのみをサポートしていた。
  - [C Shellと互換性があるファイル名修飾子](../Page/C_Shell.md "wikilink")（`%f`など）
  - [カレントディレクトリ](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")を変更した後から過去のカレントディレクトリに戻ることができる、`PushD`、`PopD`コマンド
  - `IF`コマンドで大文字・小文字を区別した文字列比較、数値比較、ブロック記述をサポート。
  - `SET`コマンドで数値の演算代入をサポート

## 後継および将来性

cmd.exeの後継は[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")/[.NET Coreをベースにオブジェクト指向言語として再構築された](https://ja.wikipedia.org/wiki/.NET_Core "wikilink")[PowerShell](../Page/PowerShell.md "wikilink")であり、Windowsコマンドと比べて高い柔軟性と記述性を持つ。いくつかのWindowsコマンドに関して互換エイリアスが用意されているなど、ある程度の互換性も持っているが、完全な上位互換ではなく、コマンドプロンプトとは依然として共存関係にある。[マイクロソフト](../Page/マイクロソフト.md "wikilink")はcmd.exe廃止の噂に関しては全面否定しており、例えばWindows自身をビルド＆テストするために自動化されたシステムにおいてcmd.exeに依存した多数のスクリプトが利用されていることなどから、将来的にWindowsから取り除かれることはないとしている\[4\]。

## Windowsエクスプローラーとの統合

[Windows 7の](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")[エクスプローラーでは](../Page/Windows_Explorer.md "wikilink")、[Shiftキー](https://ja.wikipedia.org/wiki/Shiftキー "wikilink")を押しながら[コンテキストメニュー](../Page/コンテキストメニュー.md "wikilink")を表示すると、「コマンド ウィンドウをここで開く」というメニューコマンドが出現する\[5\]。このコマンドを実行することで、指定フォルダーをカレントディレクトリに設定した状態でコマンドプロンプトを起動することができる。

[Windows 8.1では](https://ja.wikipedia.org/wiki/Windows_8.1 "wikilink")[スタートボタンを右クリックする](https://ja.wikipedia.org/wiki/スタートメニュー "wikilink")、または[Windowsキー](../Page/Windowsキー.md "wikilink")を押しながらXキーを押すことでシステムコマンドメニューが表示され、コマンドプロンプトを通常権限または管理者権限で起動することができる。

[Windows 10](https://ja.wikipedia.org/wiki/Windows_10 "wikilink") Creators Update (バージョン1703) では、既定のコマンドシェルが[PowerShell](../Page/PowerShell.md "wikilink")に置き換えられ、エクスプローラー上でShiftキーを押しながらコンテキストメニューを表示すると「PowerShell ウィンドウをここに開く」というメニューコマンドが出現するようになり、またシステムコマンドメニューにはコマンドプロンプトの代わりにPowerShellが表示されるようになった。ただし設定変更により従来通りコマンドプロンプトをシステムコマンドメニューに表示させることも可能である\[6\]。

## 文字コード

### コマンドプロンプトの文字コード

コマンドプロンプト（cmd.exe）自体が使用している文字コードは[Unicode](../Page/Unicode.md "wikilink") ([UTF-16](../Page/UTF-16.md "wikilink")) であり、（コマンドからの出力がUnicodeでありフォントがあれば）Unicode特有の文字を問題なく画面に表示することができる。ただし[バッチファイル](../Page/バッチファイル.md "wikilink")は[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")との互換性維持の観点から、Windowsのシステムロケール設定（「Unicode対応ではないプログラムの言語」のこと、表示言語とは異なる）と同じ「ANSIコードページ」でエンコードされているという前提で解釈される。例えばシステムロケール設定が日本語の場合、既定で[Microsoftコードページ932](../Page/Microsoftコードページ932.md "wikilink") (CP932, [Shift_JIS](../Page/Shift_JIS.md "wikilink")) が使われる。ただしバッチファイルからコマンドを実行して画面に出力する場合に文字コード変換が行われることはない。コマンドプロンプトで使用するANSIコードページはシステムロケール設定を変更する他、`chcp`コマンドによってコマンドプロンプトごとに一時的に変更することが可能であり、例えばコードページ65001に設定すると[UTF-8](../Page/UTF-8.md "wikilink")として解釈される。UTF-16LE（コードページ1200）はANSIコードページと互換性がないためサポートされない。

### 内部コマンドの文字コード

コマンドプロンプトに内蔵されている**内部コマンド** (`type`や`dir`など) はUnicode出力とANSIコードページ出力の両方に対応しており、単独で実行して画面に表示する場合はUnicodeで出力される。ただし内部コマンドの出力先が画面以外（[リダイレクトや](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")[パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")）である場合は、現在のANSIコードページに変換して出力する。この挙動は`cmd.exe`のデフォルト（`/A`オプション）設定時の動作であり、`/U` オプションを付けて起動することでUTF-16出力に変更することが可能\[7\]である。[バイトオーダーマーク](https://ja.wikipedia.org/wiki/バイトオーダーマーク "wikilink")(BOM) はテキストとして保存した場合に必要なものであるため付与されない。

### 外部コマンドの文字コード

Windowsでは[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")の一形態として、[コマンドラインインターフェイス](../Page/キャラクタユーザインタフェース.md "wikilink") (CLI) を持つ「[コンソールアプリケーション](https://ja.wikipedia.org/wiki/コンソールアプリケーション "wikilink")」があり、これは単独で動作させることができるだけでなくコマンドプロンプト上で動作させることもできる。これにより、ユーザーが**外部コマンド**として独自のコマンドを開発し、[リダイレクトや](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")[パイプを駆使してバッチ処理に応用することができる](../Page/パイプ_\(コンピュータ\).md "wikilink")。

外部コマンドが出力する文字コードはその外部コマンドの実装によって異なり、一般にコマンド開発者はCLIコマンドの出力をUnicodeモードで行なうか、MBCSモードで行なうかを選ぶことができる。例えば[C言語](../Page/C言語.md "wikilink")の場合は`_setmode()`[関数](../Page/サブルーチン.md "wikilink")\[8\]を呼び出すことで設定できる。[.NET Frameworkの場合は](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")`System.Console.OutputEncoding`[プロパティで設定できる](https://ja.wikipedia.org/wiki/プロパティ_\(プログラミング\) "wikilink")。`_setmode()`で設定可能なUnicodeモードは更に`_O_U16TEXT`モード、`_O_U8TEXT`モード、`_O_WTEXT`モードに細分化されるが、いずれであってもコマンドプロンプトはそれらを正しく解釈し、現在のコードページに関係なくUnicode出力として扱い正しく画面に表示する。MBCSモードで出力した場合は現在のコードページの設定に従って内部的にUnicodeに変換され画面に表示される。

なお、`ipconfig`など、Windowsに標準搭載されている外部コマンドは入出力をMBCSモードで行なっている。ただしシステムロケール設定に応じて表示言語を切り替えている。

仮にコマンドプロンプト上でUnicode入出力を行なう独自コマンドを開発する場合は、入出力をUnicodeモードで行なうことで実現できる。またバッチファイルによる読み取りを考慮する場合は、コマンドの入出力をUTF-8とし、バッチファイルをUTF-8で記述し、コードページを`chcp 65001`によってUTF-8に変更することでUnicodeの入出力に対応することができる。

## 脚注

## 関連項目

  - [キャラクタユーザインタフェース](../Page/キャラクタユーザインタフェース.md "wikilink") (CUI, CLI)
  - [シェル](../Page/シェル.md "wikilink")
  - [バッチファイル](../Page/バッチファイル.md "wikilink")
  - [PowerShell](../Page/PowerShell.md "wikilink")

## 外部リンク

  - [Cmd | Microsoft Docs](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/cmd)
  - [Command Prompt: frequently asked questions - Windows Help](https://web.archive.org/web/20150422041137/http://windows.microsoft.com/en-us/windows/command-prompt-faq), [Internet Archive](https://ja.wikipedia.org/wiki/Internet_Archive "wikilink")

[Category:Windowsのコマンド](https://ja.wikipedia.org/wiki/Category:Windowsのコマンド "wikilink") [Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:Windows_NT系](https://ja.wikipedia.org/wiki/Category:Windows_NT系 "wikilink") [Category:OS/2](https://ja.wikipedia.org/wiki/Category:OS/2 "wikilink")

1.  cmd.exeの実行ファイルのプロパティにおける「説明」欄は、英語版では「Windows Command Processor」、日本語版では「Windows コマンド プロセッサ」となっている。
2.  [Windows Commands | Microsoft Docs](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
3.
4.  [Rumors of Cmd’s death have been greatly exaggerated | Windows Command Line](https://devblogs.microsoft.com/commandline/rumors-of-cmds-death-have-been-greatly-exaggerated/)
5.  [Windowsスマートチューニング(72) Win 7編: ＜コマンドウィンドウをここで開く＞を常に表示し、コマンドプロンプトを簡単起動する | マイナビニュース](https://news.mynavi.jp/article/windows-72/)
6.  [コマンド プロンプトは PowerShell に置き換えられます](https://support.microsoft.com/ja-jp/help/4027690/windows-powershell-is-replacing-command-prompt)
7.  [Cmd | Microsoft Docs](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/cmd)
8.  [_setmode | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/c-runtime-library/reference/setmode)