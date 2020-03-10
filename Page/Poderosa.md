> この記事は[Poderosa](https://ja.wikipedia.org/wiki/Poderosa)から翻訳されています。


**Poderosa**（ポデローザ）は、[Apache License](https://ja.wikipedia.org/wiki/Apache_License "wikilink")（[オープンソースソフトウェア](https://ja.wikipedia.org/wiki/オープンソースソフトウェア "wikilink")）で開発・公開している[タブ型リモートログオン](../Page/タブ_\(GUI\).md "wikilink")[クライアントで](../Page/クライアント_\(コンピュータ\).md "wikilink")、**Poderosa Terminal**は同一の作者が開発している有償のソフトウェア。

Poderosaは、[SSH](../Page/Secure_Shell.md "wikilink")・[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")・[Cygwin](../Page/Cygwin.md "wikilink")・Service for Unix・[シリアルの各](../Page/シリアルポート.md "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")に対応し、[.NET Frameworkが](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[インストール](../Page/インストール.md "wikilink")された[Windowsで使用できる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。Poderosa TerminalはmacOSでも使用可能。

以前は**VaraTerm**という[シェアウェア](../Page/シェアウェア.md "wikilink")であったが、後に現称の**Poderosa**としてオープンプロジェクトとしての開発方針に変更された。そして、[情報処理推進機構](https://ja.wikipedia.org/wiki/情報処理推進機構 "wikilink") (IPA) により、2005年度下期の[未踏ソフトウェア創造事業に採択された](https://ja.wikipedia.org/wiki/情報処理推進機構#未踏ソフトウェア創造事業 "wikilink")\[1\]。

2016年、描画エンジンのOpenGL化やWindows以外のプラットフォームでの稼働も視野に入れた形で商用製品としてリニューアルした。

## 特徴

  - 各接続セッションがタブで管理されている(画面分割表示も対応する)
  - SSH/SSH2の鍵暗号やバージョンの管理
  - 接続先毎に異なる設定を保存できる
  - SSH2[ポートフォワーディング](https://ja.wikipedia.org/wiki/ポートフォワーディング "wikilink")
      - SSH鍵作成ウィザードも利用できる
  - [xterm](https://ja.wikipedia.org/wiki/xterm "wikilink")や[VT102の略完全な](https://ja.wikipedia.org/wiki/VT100#後継シリーズ "wikilink")[エミュレーション](../Page/エミュレータ.md "wikilink")
  - .NET Framework 対応言語によるマクロのサポート
  - 開発者の岡嶋大介が設立したラガルト・テクノロジー社による有償サポート\[2\]
  - 2016年以降、同社の商用製品になった。

## 系統

バージョン3.x以前と4.xでは大きく異なり、開発[ブランチが分かれている](https://ja.wikipedia.org/wiki/ブランチ_\(ソフトウェア\) "wikilink")。

バージョン3.x以前は.NET Framework 1.1環境で動作する\[3\]。今後におけるバージョンアップの予定は無い。

バージョン4.0～4.3は.NET Framework 2.0環境で動作する。これまで統合されていたコンポーネントが別パッケージになっており、SSHポートフォワーディングツールなどは別途ダウンロードする必要が有る。端末ソフトのプロセス一つで複数のシェルウィンドウを取り扱えるようになった。

## 注釈

<references />

## 関連項目

  - [Secure Shell](../Page/Secure_Shell.md "wikilink")

      - [OpenSSH](https://ja.wikipedia.org/wiki/OpenSSH "wikilink")
      - [WinSCP](https://ja.wikipedia.org/wiki/WinSCP "wikilink")
      - [RLogin](https://ja.wikipedia.org/wiki/RLogin "wikilink")
      - [PuTTY](../Page/PuTTY.md "wikilink")
      - [Tera Term](../Page/Tera_Term.md "wikilink")

  -
## 外部リンク

  - [Poderosa Terminal – プロフェッショナルのためのSSHクライアント](https://ja.poderosa-terminal.com/) - 製品版

  - [Poderosa Project on sourceforge](http://poderosa.sourceforge.net/) - オープンソース版

  -
[Category:端末エミュレータ](https://ja.wikipedia.org/wiki/Category:端末エミュレータ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.  .NET 1.1sp1環境では動作が不安定であるので、.NET 1.1環境を用意する必要がある。