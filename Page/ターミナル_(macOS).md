> この記事は[ターミナル \(macOS\)](https://ja.wikipedia.org/wiki/ターミナル_\(macOS\))から翻訳されています。


**ターミナル** (Terminal) は、[アップルの](../Page/アップル_\(企業\).md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")に標準で付属している[UNIX](../Page/UNIX.md "wikilink")[端末エミュレータ](../Page/端末エミュレータ.md "wikilink")。

直接入力した[UNIX](../Page/UNIX.md "wikilink")[コマンドを実行する他](https://ja.wikipedia.org/wiki/命令 "wikilink")、UNIXコマンドの実行を自動化する[Term](https://ja.wikipedia.org/wiki/Term "wikilink")ファイルを作成、実行することも可能である。

## 動作

ターミナルを起動すると、UNIXとしてのmacOSの標準[CLI](../Page/キャラクタユーザインタフェース.md "wikilink")[シェル](../Page/シェル.md "wikilink")が起動し、UNIXコマンドを打ち込むことができる。もちろん、UNIX用の[アプリケーションをインストールして](../Page/アプリケーションソフトウェア.md "wikilink")、実行することもできる（ただし、UNIX用のアプリケーションを[インストール](../Page/インストール.md "wikilink")するためには、[MacPorts](https://ja.wikipedia.org/wiki/MacPorts "wikilink")や[Xcode](../Page/Xcode.md "wikilink")といった開発環境のインストールが必要となる）。当初標準シェルは[tcsh](https://ja.wikipedia.org/wiki/tcsh "wikilink")だったが、その後[Panther(10.3)で](../Page/Mac_OS_X_v10.3.md "wikilink")[bash](https://ja.wikipedia.org/wiki/bash "wikilink")、[Catalina(10.15)で](https://ja.wikipedia.org/wiki/macOS_Catalina "wikilink")[zsh](https://ja.wikipedia.org/wiki/zsh "wikilink")に変更された\[1\]。

## AppleScriptからの呼び出し方法

[AppleScript](../Page/AppleScript.md "wikilink")から、ターミナルを使いUNIXコマンドを実行することも可能である。

使用例:

    tell application "Terminal"
        activate
        do script with command "（実行したいコマンド）"
    end tell

## Mac専用コマンド

ターミナルでは[GUI操作もCLIで使用できるように一部専用コマンドがある](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。また、普段は設定できない隠しコマンドも存在する。

  - openコマンド

openコマンドは、Finder上でダブルクリックをした時と同様に関連付けられたアプリによってファイルを開くことができる。 例:既存のテキストファイルを開く

    open hoge.txt

このように打ち込むと標準のテキストエディタによってhoge.txtというファイルが開かれる。

また-aオプションをつけることによって特定のアプリによって開くこともできる。

例:テキストエディットでファイルを開く

    open -a /Applications/TextEdit.app hoge.txt

[sudo](https://ja.wikipedia.org/wiki/sudo "wikilink")と併用することにより、アクセス権が無いファイルを開く事も可能である。

  - sayコマンド

sayコマンドは、ユニバーサルアクセス用に使用されるコマンドで、入力された引数の文字を読み上げる。（日本語にも対応\[2\]）

例:Wikipediaと言わせる。

    say Wikipedia

## 脚注

## 関連項目

  - [UNIX](../Page/UNIX.md "wikilink")
  - [キャラクタユーザインタフェース](../Page/キャラクタユーザインタフェース.md "wikilink")
  - [シェル](../Page/シェル.md "wikilink")
      - [tcsh](https://ja.wikipedia.org/wiki/tcsh "wikilink")
      - [Bash](../Page/Bash.md "wikilink")
      - [Z Shell](../Page/Z_Shell.md "wikilink")

[Category:端末エミュレータ](https://ja.wikipedia.org/wiki/Category:端末エミュレータ "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink")

1.  [Catalinaでデフォルトシェルが「zsh」に変わる、bashとの違いは? - 新・OS X ハッキング\!(241) ｜ マイナビニュース](https://news.mynavi.jp/article/osxhack-241/)
2.  macOS Sierra以降は日本語がデフォルト言語環境の場合、日本語音声が読み上げ時のデフォルトになっている。macOS Sierra以前の場合は、システム音声に日本語音声モジュール"*Kyoko*"を別途インストールすることで日本語での読み上げに対応可。