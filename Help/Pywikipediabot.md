> この記事は[Help:Pywikipediabot](https://ja.wikipedia.org/wiki/Help:Pywikipediabot)から翻訳されています。


*In other languages:* [de](https://ja.wikipedia.org/wiki/:de:b:Python-Programmierung:_Pywikipediabot "wikilink") - [en](https://ja.wikipedia.org/wiki/mw:Manual:Pywikipediabot "wikilink") - [es](https://ja.wikipedia.org/wiki/mw:Manual:Pywikipediabot/es "wikilink") - [fr](https://ja.wikipedia.org/wiki/:fr:Aide:Pywikipedia "wikilink") - [hu](https://ja.wikipedia.org/wiki/:hu:Wikipédia:Pywikipedia "wikilink") - [it](https://ja.wikipedia.org/wiki/mw:Manual:Pywikipediabot/Basic_use/it "wikilink") - [ja](https://ja.wikipedia.org/wiki/Help:Pywikipediabot "wikilink") - [ko](https://ja.wikipedia.org/wiki/mw:Manual:Pywikipediabot/ko "wikilink") - [nl](https://ja.wikipedia.org/wiki/:nl:Help:Gebruik_van_bots "wikilink") - [pl](https://ja.wikipedia.org/wiki/mw:Manual:Pywikipediabot/Basic_use/pl "wikilink") - [pt](https://ja.wikipedia.org/wiki/:pt:Ajuda:Como_usar_bots "wikilink") - [ru](https://ja.wikipedia.org/wiki/:ru:Википедия:Pywikipedia-боты "wikilink") - [sv](https://ja.wikipedia.org/wiki/mw:Manual:Pywikipediabot/Basic_use/sv "wikilink") - [zh-hant](https://ja.wikipedia.org/wiki/mw:Manual:Pywikipediabot/zh-hant "wikilink")

-----

  -
    **pywikipediabotを準備するのに手助けがほしいなら[\#wikipedia-ja-bot](https://webchat.freenode.net/?channels=Wikipedia-ja-bot)@ freenode server（詳しくは[WP:CHATを参照](https://ja.wikipedia.org/wiki/WP:CHAT "wikilink")） にくるか[pywikipediabot mailing list](https://lists.wikimedia.org/mailman/listinfo/Pywikipedia-l)を使ってください。**

[Interwiki.png](https://ja.wikipedia.org/wiki/File:Interwiki.png "fig:Interwiki.png") **Pywikipediabot** (Python Wikipedia Robot Framework) は、ウィキペディアなどの[ウィキメディア財団](../Page/ウィキメディア財団.md "wikilink")のプロジェクトのための[Botスクリプトのセットです](https://ja.wikipedia.org/wiki/Wikipedia:Bot "wikilink")。多くの開発者によって[Python](../Page/Python.md "wikilink")言語で記述されています。このページでは、Botソフトウェアを使用したい人のためのおおまかな情報を提供します。

## セットアップ

### Pythonのインストール

pywikipediaを使うためには、Pythonバージョン2.4以上が必要です。Pythonバージョン2.3で動くコードも多いですが、2.3での動作確認は行われていません。ただし2011年1月現在、バージョン3には対応していません。

Pythonは、ほとんどのプラットフォーム（Unix、Linux、Mac、Windows）で使えます。

  - **Windows**にはActivePythonが便利ですが、やや遅いです。[ここ](https://www.activestate.com/products/python/)からダウンロードできます。
  - **Unix**には最初からPythonがインストールされているので、インストールする必要はありません（ただし、非常に古いバージョンのUnixの場合には、Pythonがインストールされていなかったり、Pythonのバージョンが古かったりする場合があります。その場合にはアップデートが必要です）。
  - **Mac**でMac OS Xを使っている場合は、インストールの必要はありません。
  - その他の場合、あるいはインストールされているバージョンが古い場合には、http://www.python.org/download/ からダウンロードしてインストールしてください。

### pywikipediaのダウンロード

最も簡単な方法は、[PyWikipediaBot PyWikipediaBot Nightlies](http://toolserver.org/~valhallasw/pywiki/)の「pywikipedia - The packages」からダウンロードすることです（ただしこのファイルは前日の時点での最新版です）。古いバージョンが必要な場合は[Sourceforge](http://sourceforge.net/projects/pywikipediabot/)からダウンロードできます。ダウンロードしたファイルを展開します。展開する場所は、できるだけ浅い位置のディレクトリが便利でしょう。

Mac OS Xの場合には、[ここにある説明](http://www.rubyrobot.org/tutorial/subversion-with-mac-os-x)をお読み下さい。ファイルは[ここ](http://svn.wikimedia.org/svnroot/pywikipedia/trunk/pywikipedia/)からダウンロードできます。"Check out"でコピーが可能です。

#### SVNを使ったダウンロード

（上記の前日の時点の最新バージョンではなく）最新のバージョンをダウンロードしたい場合には、[SVNが便利です](../Page/Apache_Subversion.md "wikilink")。SVNを使うと、日頃のバージョンアップも非常に簡単です。多くのUnixにはSVNが標準でインストールされています。Windowsの場合は [TortoiseSVN](http://tortoisesvn.net/downloads)を利用しましょう（[Microsoft Windows 7の場合は](../Page/Microsoft_Windows_7.md "wikilink")64ビット版がよいでしょう）。Mac OS Xの場合は[この説明](http://www.rubyrobot.org/tutorial/subversion-with-mac-os-x)を読んでください。

**Unix**などで、コマンドラインを使ってBotをチェックアウト（ダウンロード）するには、以下のコマンドを使用します：

<div class="plainlinks">

  -
    ` $ svn checkout  `<http://svn.wikimedia.org/svnroot/pywikipedia/trunk/pywikipedia/>`  pywikipedia `

次のようにファイルのスペルチェックを無効にすると時間短縮になります：

  -
    ` $ svn checkout --ignore-externals  `<http://svn.wikimedia.org/svnroot/pywikipedia/trunk/pywikipedia/>`  pywikipedia `

</div>

上のコマンドを実行すると、カレント作業ディレクトリ（Unixではpwdコマンドか変数$PWDで確認、Cygwinなど他の環境では環境設定で確認できます）に「pywikipedia」という名前で新しいディレクトリが作成されます。

コマンドラインを使ってダウンロードしたファイルを後日アップデートするには、作業ディレクトリをpywikipediaに移動してから、以下を打ちます。

  -
    `$ svn update`

**TortoiseSVN**など、コマンドラインツール以外では必要な情報はリポジトリのパスのみです：http://svn.wikimedia.org/svnroot/pywikipedia/trunk/pywikipedia/

#### Botのメーリングリスト

Botメーリングリストに登録するのは、良い考えでしょう（[こちらを参照](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/communication "wikilink")）。Botソフトウェアのファイルが更新されるたびにリストにメールが送られるので、新しいバージョンにアップデートする必要があるかどうか確認できます。

### アカウント取得

ボットの運用条件や注意事項については [Wikipedia:Bot](https://ja.wikipedia.org/wiki/Wikipedia:Bot "wikilink") を参照してください。

大規模な編集を行う場合は、Botのアカウントは通常の利用者と区別するため、専用のアカウントを取得しなければなりません。これは、Botフラグを付与することで最近更新されたページからBotの編集を隠すためです。ウェブブラウザを使ってあなた自身が手動で取得してください。利用者名は、通常「bot」の文字が後ろに付けられることが推奨されます。パスワードはあなた自身のアカウントと別のものがよいでしょう。

### user-config.py の設定

編集可能な環境変数の初期値は `config.py` にあります。これを直接書き換えるとSVNでのアップデートで支障が出ることがあるため、お勧めできません。値を変更する場合には、同じ階層に `user-config.py` を作成します。`user-config.py` だけで設定を上書きしていくことで、初期値に戻したい場合、削除することで対応できます。

#### アカウントに関する設定

以下の節では、アカウントに関する設定について説明しています。なお、`testfamily.py` というプログラムがある場合は、実行することで簡易設定を行うことができます。（説明省略）

##### ウィキペディアの場合

メモ帳などのテキストエディタを開きます。

以下のように打ちます：

``` python
 mylang = 'xx'
```

xx には、動作させる言語コードが入ります。日本語版では、"ja"が入ります。

このテキストファイルを`user-config.py`という名前で、ダウンロードしたpyファイルと一緒のフォルダに保存します。

複数の言語で動作させたいなら、コマンドライン引数の`-lang`パラメータで指定できるので、ここでは最もよく使う言語コードを指定しましょう。

`user-config.py`では、Botの利用者名を指定する必要があります。

ウィキペディア日本語版で動作させるとします。「ExampleBot」という利用者名でBotのアカウントを取得しているならば、以下のように`user-config.py`に追記します。

``` python
 usernames['wikipedia']['ja'] = u'ExampleBot'
```

利用者名の前の'u'は、Unicodeを表しています。詳しくは Python 自体のヘルプを見てください。

複数のwikiで動作させたいなら、以下のように複数の利用者名を指定できます。

``` python
 usernames['wikipedia']['de'] = u'BeispielBot'
 usernames['wikipedia']['en'] = u'ExampleBot'
 usernames['wiktionary']['de'] = u'BeispielBot'
```

管理者権限が必要なスクリプト(speedy_delete.py、redirect.py brokenなど)は、以下のように管理者権限を持つアカウントを追記します。

``` python
 sysopnames['wikipedia']['ja'] = u'SysopName'
```

##### ウィキペディア以外のウィキサイトの場合

メモ帳などのテキストエディタを開きます。

以下のように打ちます：

`mylang = 'xx'`

xx には、動作させる言語コードが入ります。日本語では、"ja"が入ります。

次に以下のように打ちます：

`family = 'sitename'`

"sitename"は、動作させるサイト名です。

wiktionary、wikibooks、wikiquoteなどや[ウィキメディア・プロジェクトではないwikitravelなども指定できます](https://ja.wikipedia.org/wiki/Wikipedia:ウィキメディア・プロジェクト "wikilink")。（familiesフォルダに一覧があります。）

Wikimedia Commonsで動作させるなら、"mylang"と"family"に'commons'を指定します。

``` python
 mylang='commons'
 family='commons'
 usernames['commons']['commons']='UserBot'
```

##### familyフォルダにウィキサイトが無い場合

ウィキが family フォルダのリストに無い場合は、適切な `_family.py` ファイルを作成する必要があります。作成に関する説明は省きますので、[meta:Pywikipedia bot on non-Wikimedia projectsを参照してください](https://ja.wikipedia.org/wiki/meta:Pywikipedia_bot_on_non-Wikimedia_projects "wikilink")。

この場合でも `user-config.py` の設定を行ないます。

ウィキ名 Memory Alpha (memoryalpha) の英語版 (en) で動作させるとします。「ExampleBot」という利用者名でBotのアカウントを取得しているならば、以下のように記述します:

``` python
 mylang = 'en'
 family = 'memoryalpha'
 usernames['memoryalpha']['en'] = u'ExampleBot'
```

このテキストファイルを`user-config.py`という名前で、ダウンロードしたpyファイルと一緒のフォルダに保存します。

#### その他の設定

当面は安全のため、ボットの速度を落としましょう。`user-config.py` に `put_throttle = 30` いう行を追加します。これはPywikipediaBotの編集間隔の秒数です。デフォルトは10です。

ウィキペディア日本語版では、どんなに早い場合でも10秒以上（毎分6回）の間隔を守らなくてはなりません。Botフラグ無し、かつ、大量編集する場合には60秒以上の間隔を求められます。編集間隔を60秒より大きい値にする場合には、`maxthrottle = 120` という行を追加します。これは編集間隔の最大値を制限し、この場合は120秒になります。

Botフレームワークがサポートしている[スキンは](https://ja.wikipedia.org/wiki/Help:オプション#外装 "wikilink")、Monobook のみです。デフォルトから変更しないようにしましょう。

### 命令実行のショートカット作成（Windowsユーザ向け）

Pywikipediabotをマイドキュメントのような階層の深いフォルダにインストールしているなら、Botを動作させるたびにcdコマンドでフォルダに移動するのは、非常に厄介な作業です。

Windowsでは、簡単にBotを動作させるためにコマンドプロンプトを開くショートカットを作成することができます。 以下のステップに従って作成します：

1.  pywikipediaがインストールされているフォルダを開く。
2.  右クリックのメニューから「新規作成 -\> ショートカット」をクリックする。
3.  "cmd.exe"を入力して、「次へ」をクリックする。
4.  ショートカット名には"Pywikipediabot"など相応しい名前を入力する。
5.  作成したショートカットを右クリックしてメニューを表示して、「プロパティ」をクリックします。
6.  「ショートカット」タブの「作業フォルダ」の項目に、Pywikipediabotがインストールされたディレクトリへの絶対パスを記述します。
7.  変更を保存して、ショートカット作成の完了です。

また、Pythonのパスも追加しておきましょう（例えばPythonを「C:\\Python」にインストールした場合、Windows XPの場合は「コントロールパネル」→「システム」→「詳細設定」→「環境変数」と進んで、「システム環境変数」の変数「Path」を「編集」で開いて、元の文字列の末尾に「;C:\\Python」と追加します）。

## 使い方

以上の手順でBotを使用する準備が出来ました。Botの実行には、OSのコマンドラインを使用します。

  - **Windows**では、コマンドプロンプト（cmd.exe）を使います。
  - **Mac**では、/Applications/UtilitiesにインストールされているTerminal.appを使います。
  - **Linux**または**Unix**系OSでは、[gnome-terminal](../Page/GNOME_端末.md "wikilink")、[Konsole](https://ja.wikipedia.org/wiki/Konsole "wikilink")、[xterm](https://ja.wikipedia.org/wiki/xterm "wikilink")、テキストモードコンソールなど何を使ってもいいです。

まず、Pywikipediabotをインストールしたディレクトリにコマンドで移動します。

`cd pywikipedia`

### 動作確認

まずは正しくインストールされているかどうかを確認するため、既存のプログラムを走らせて見ましょう。この段階では使用申請は必要ありません。これらの確認はウィキペディアでも可能ですが、出来るならば、[自分のパソコンに MediaWiki をインストール](https://www.mediawiki.org/wiki/Manual:Installation_guide/ja)して確認しましょう。

  - [login.py](https://ja.wikipedia.org/wiki/Help:Pywikipediabot/login.py "wikilink")
      -
        ボットをウィキペディアにログインさせるだけのプログラムです。ログインするプロジェクトとログイン名は先ほど作った「user-config.py」から自動で読み込まれます。パスワードはプログラム実行後に手で入力します。Botは、通常ログアウトされることがないので、パスワードを変更しない限りこのプログラムをもう一度実行する必要はありません。
            python login.py
        なお、使用申請していませんので、次のような警告がでるはずですが、今のところは気にする必要はありません。
          -
            Checked for running processes. 1 processes currently running, including the current process.
            Password for user XXXXXX on wikipedia:ja:
            Logging in to wikipedia:ja as XXXXXX
            WARNING: Your account on wikipedia:ja does not have a bot flag. Its edits will be visible in the recent changes and it may get blocked.
            Should be logged in now
        <!-- end list -->
            python login.py -test
        ログイン中のウィキ・ファミリーの名前と自分のアカウント名を調べてコンソールに出力します。
            python test.py
        先ほどの警告に加えて、次のように出力されます。
          -
            You are logged in on wikipedia:ja as XXXXXX.
  - サンドボックスの初期化
      -
        [Wikipedia:サンドボックスを初期化します](https://ja.wikipedia.org/wiki/Wikipedia:サンドボックス "wikilink")。なお**これは編集行為ですので、編集履歴がウィキペディアに残ります。**
            python clean_sandbox.py
        先ほどの警告に加えて、次のように出力されます。サーバーと交信するため、やや時間がかかります。
          -
            Sleeping for 7.1 seconds, 2009-02-17 22:49:24
            Changing page \[\[Wikipedia:サンドボックス|Wikipedia:サンドボックス\]\]
            Done.

## 使用申請

Botを運用するためには、コミュニティに許可を得る必要があります。許可の基準の厳しさはプロジェクトによって異なります。何の許可もなく自由に運用できるプロジェクトもありますが、ウィキペディア日本語版では、試験運用を行い有用で無害であることを証明して許可を得る必要があります。

### スクリプト

現在利用できるBotのリストと解説ページへのリンク ([mediawiki](https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/Scripts "wikilink"))：

<table>
<tbody>
<tr class="odd">
<td><p> </p></td>
<td><p>メインBotスクリプト</p></td>
<td><p> </p></td>
<td><p>その他のBotスクリプト</p></td>
<td><p> </p></td>
<td><p>補助プログラム</p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td></td>
<td><hr /></td>
<td></td>
<td><hr /></td>
<td></td>
<td><hr /></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/add_text.py" title="wikilink">add_text.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/add_text.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/category.py" title="wikilink">category.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/category.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/imagetransfer.py" title="wikilink">imagetransfer.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/imagetransfer.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/interwiki.py" title="wikilink">interwiki.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/interwiki.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/redirect.py" title="wikilink">redirect.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/redirect.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/replace.py" title="wikilink">replace.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/replace.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/solve_disambiguation.py" title="wikilink">solve_disambiguation.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/solve_disambiguation.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/table2wiki.py" title="wikilink">table2wiki.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/table2wiki.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/template.py" title="wikilink">template.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/template.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/upload.py" title="wikilink">upload.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/upload.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/weblinkchecker.py" title="wikilink">weblinkchecker.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/weblinkchecker.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/wikipedia.py" title="wikilink">wikipedia.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/wikipedia.py" title="wikilink">mediawiki</a>)</li>
</ul></td>
<td></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/blockpageschecker.py" title="wikilink">blockpageschecker.py</a></li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/catall.py" title="wikilink">catall.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/catall.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/clean_sandbox.py" title="wikilink">clean_sandbox.py</a></li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/copyright.py" title="wikilink">copyright.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/copyright.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/cosmetic_changes.py" title="wikilink">cosmetic_changes.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/cosmetic_changes.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/delete.py" title="wikilink">delete.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/delete.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/delinker.py" title="wikilink">delinker.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/delinker.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/editarticle.py" title="wikilink">editarticle.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/editarticle.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/featured.py" title="wikilink">featured.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/featured.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/fixing_redirects.py" title="wikilink">fixing_redirects.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/fixing_redirects.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/imagecopy.py" title="wikilink">imagecopy.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/imagecopy.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/imageharvest.py" title="wikilink">imageharvest.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/imageharvest.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/lonelypages.py" title="wikilink">lonelypages.py</a></li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/movepages.py" title="wikilink">movepages.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/movepages.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/pagefromfile.py" title="wikilink">pagefromfile.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/pagefromfile.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/protect.py" title="wikilink">protect.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/protect.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/warnfile.py" title="wikilink">warnfile.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/warnfile.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/welcome.py" title="wikilink">welcome.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/welcome.py" title="wikilink">mediawiki</a>)</li>
</ul></td>
<td></td>
<td><ul>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/user-config.py" title="wikilink">user-config.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/user-config.py" title="wikilink">mediawiki</a>)</li>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/login.py" title="wikilink">login.py</a>(<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/login.py" title="wikilink">mediawiki</a>)</li>
</ul>
<ul>
<li><a href="https://ja.wikipedia.org/wiki/Help:Pywikipediabot/version.py" title="wikilink">version.py</a> (<a href="https://ja.wikipedia.org/wiki/mw:Manual:Pywikibot/version.py" title="wikilink">mediawiki</a>)</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

### コマンドライン引数

ほとんどのBotスクリプトには独自のコマンドライン引数があり、それぞれのページまたはソースコード上で説明されています。反対に特筆が無い限り以下のコマンドライン引数は、全てのBotに存在します。

  - \-help
    共通のBot引数のリスト（このリスト）と、Bot特有のヘルプが表示されます。
  - \-lang:xx
    動作させる言語コードを`xx`で指定します。`user-config.py`での設定より優先されます。
  - \-family:xyz
    wikipedia、wiktionary、wikitravelなど動作させるウィキの種類を指定します。`user-config.py`での設定より優先されます。
  - \-log
    ログファイル出力を有効にします。ログはlogsディレクトリに保存されます。
  - \-log:xyz
    ログファイル出力を有効にします。ファイル名に`xyz`が使われます。
  - \-nolog
    ログファイル出力を無効にします。
  - \-putthrottle:nn
    Botがページ編集を保存してから、次の編集まで待機する時間を秒数で指定します。デフォルト値は0です。

例えば、`python [スクリプト名].py -family:wikipedia`で\[スクリプト名\]Botをウィキペディアで動作させます。`user-config.py`での設定より優先されます。

## バグ報告

バグ報告する時は、以下の内容を含めてください。：

  - 使用しているPyWikipediaBotのバージョン。最新のSVN改訂においてまだバグが存在するか確認することが推奨される。
  - 使用しているPython (python -v) のバージョンとWindows、Linux、Mac OS XなどOSの情報。
  - 正確な概要。
  - 問題と報告の完全な記述。
  - 使用したスクリプト、サイト名、言語などバグを再現するための詳細情報。
  - ログ出力。

新しいバグの報告は、SourceForgeの[bug tracker](http://sourceforge.net/tracker/?group_id=93107)で行います。

## 開発

もし、あなたがBotに、従来のBotには無い新機能を付けたいと思ったなら、誰かプログラマーに頼んでその機能を実装して貰うことが出来ます。或いは自分でBotを改造出来るなら、その方が良いでしょう。Pythonは良くできたプログラミング言語ですし、習得は難しくありません。あなたも挑戦してみましょう。

### Tips

このHelp:Pywikipediabotのページと、[wikipedia.pyのページには](https://ja.wikipedia.org/wiki/Help:Pywikipediatbot/wikipedia.py "wikilink")、あなたが自分のBotを書くに当たって、とても基本的なヒントの数々が記されています。

  - あなたのBotのuser-config.pyの設定を確認してください（[\#Configuring for Wikipediaも参照してください](https://ja.wikipedia.org/wiki/#Configuring_for_Wikipedia "wikilink")）
  - 以下のようにしてpywikipedia frameworkをインポートしてください:。

<!-- end list -->

``` python
import wikipedia
```

  - ページを取得するには次のようにしてください。pageNameのところには例えば、"Wikipedia:Bots"や"India"が入ります。

<!-- end list -->

``` python
site = wikipedia.getSite()
page = wikipedia.Page(site, u"pageName")
text = page.get(get_redirect = True)
```

  - ページを書き換えるには次のようにします。

<!-- end list -->

``` python
page.put(u"newText", u"Edit comment")
```

  - pywikipediaのファイルを見ると、様々な手法が見つけられます。replace.pyはpywikipedia入門者にとっても、読むのが比較的簡単でしょう。
  - 使用可能なPageメソッドは全てwikipedia.pyのファイルに記載されています。
  - 他の多くのBotでも利用されているbasic.pyを使うなら、ページの文章をどう編集するかを定義するだけで利用することが出来ます。
  - 反復処理を行うことで（[ループ (プログラミング)や](../Page/ループ_\(プログラミング\).md "wikilink")[イテレータ](../Page/イテレータ.md "wikilink")を参照）、複数のページに対して処理を行うことが出来ます。pagegenerators.pyを見て、複数のページを返すオブジェクトを確認してください。例えば、CategoryPageGeneratorを使って、[:Category:プログラミングのカテゴリの中の各ページに対して何かをするには](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink")、次のようにします。

<!-- end list -->

``` python
import catlib
import pagegenerators
site = wikipedia.getSite()
cat = catlib.Category(site,'Category:プログラミング')
gen = pagegenerators.CategorizedPageGenerator(cat)
for page in gen:
  # この部分で各ページに対して何か処理を行います。例えば次のように。
  text = page.get()
```

### 貢献するには

もし、あなたがBotを改造して、そのパッチをメンテナに投げたいと思ったなら、

1.  最新版にアップデートします（そうすることで、SVNのリポジトリに既にコミットされている改良点に、あなたの改造をマージします）。
2.  更新による変更の衝突を解決します（"====="等を[grep](https://ja.wikipedia.org/wiki/grep "wikilink")すればよいでしょう）。
3.  以下のように入力します。

<!-- end list -->

  -

        $ svn diff > svn.diff

あなたが変更しようとした部分のみが変更されているかどうか、diffを再確認してみてください。頭に"?"のついている行は削除されてしまいます。

もし直接、Pywikipediabotの開発者と連絡を取りたければ、svn.diffを開発者に対して投げることもできます。しかし、[Pywikipedia bug tracking system](http://sourceforge.net/tracker/?atid=603138&group_id=93107&func=browse)でパッチをチケットに添付する方が望ましいでしょう。

### 複数のアカウントでの実行

python wikipedia botを複数のアカウントで実行したくなることもあるでしょう。それには2つの方法があります。

#### Separate pywikipedia distributions

One can install completely separate instances of pywikipedia in different directories (1 for each account) and have diferent `user-config.py` files in each of them. However, when updating the installation *via* SVN, one needs to run `svn update` on each folder separately. Also, every installation takes some disk space, which might be a problem on accounts with limited quota.

#### One pywikipedia distribution with symbolic links

Let's assume user `foo` has a current SVN working copy of pywikipedia in `/home/foo/pywikipedia`. For each of the accounts, he creates a separate directory:

`foo@bar:~$ `**`mkdir``   ``foobot`**
`foo@bar:~$ `**`cd``   ``foobot`**

Pywikipedia needs then some symlinks to the main code tree created in the working directory:

`foo@bar:~/foobot$ `**`ln``   ``-s``   ``~/pywikipedia/families`**
`foo@bar:~/foobot$ `**`ln``   ``-s``   ``~/pywikipedia/userinterfaces`**

Then, `user-config.py` for this account must be created as described in [Configuration section](https://ja.wikipedia.org/wiki/#Configuration "wikilink") above.

Finally, the bot must be logged in the usual way:

`foo@bar:~/foobot$ `**`python``   ``~/pywikipedia/login.py`**

The working directory is ready. The scripts will however require a slight modification to run (the path to the pywikipedia tree must be added to Python's path).

`import sys, os`
`sys.path.append(os.environ['HOME'] + '/pywikipedia')`
`import wikipedia`

That's all. Updating to the newest version of pywikipedia on *all account at once* is now a matter of running `svn update` only in the `~/pywikipedia` directory.

## Botとプロキシ

[ここ](https://nl.wikipedia.org/wiki/Overleg_gebruiker:Andre_Engels#pywikipedia_proxy)に回避方法の草案が多分あるでしょう。

## 関連項目

  - [Wikipedia:Bot](https://ja.wikipedia.org/wiki/Wikipedia:Bot "wikilink")
  - [meta:Pywikipediabot general parameters](https://ja.wikipedia.org/wiki/meta:Pywikipediabot_general_parameters "wikilink")
  - [meta:Pywikipedia bot on non-Wikimedia projects](https://ja.wikipedia.org/wiki/meta:Pywikipedia_bot_on_non-Wikimedia_projects "wikilink")
  - [Botwiki](https://ja.wikipedia.org/wiki/botwiki: "wikilink")
  - [プロジェクト:Bot](https://ja.wikipedia.org/wiki/プロジェクト:Bot "wikilink")

## 参考

  - [:hu:Category:Egyedi fejlesztésű Pywikipedia-kódok](https://ja.wikipedia.org/wiki/:hu:Category:Egyedi_fejlesztésű_Pywikipedia-kódok "wikilink") - 英語/ハンガリー語によるbotの作り方等

[Category:Pywikipedia](https://ja.wikipedia.org/wiki/Category:Pywikipedia "wikilink")