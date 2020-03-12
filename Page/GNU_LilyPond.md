> この記事は[GNU LilyPond](https://ja.wikipedia.org/wiki/GNU_LilyPond)から翻訳されています。


**GNU LilyPond**（グニュー リリーポンド）は、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の[楽譜作成ソフトウェア](../Page/楽譜作成ソフトウェア.md "wikilink")である。

[GPL](../Page/GNU_General_Public_License.md "wikilink") ライセンスのもとに[フリーで公開されている](../Page/フリーソフトウェア.md "wikilink")。[C++](../Page/C++.md "wikilink") で記述され、[Scheme](../Page/Scheme.md "wikilink") ライブラリ ([GNU Guile](https://ja.wikipedia.org/wiki/GNU_Guile "wikilink")) でアセンブルされているが、ユーザ独自のカスタマイズや拡張も可能である。単純に音楽をテキストに記述して[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")することにより、（[PostScript](../Page/PostScript.md "wikilink") 経由で）[PDF](../Page/Portable_Document_Format.md "wikilink")、[SVGなどの形式で楽譜を出力できる](../Page/Scalable_Vector_Graphics.md "wikilink")。同時に[MIDI](../Page/MIDI.md "wikilink")ファイルを出力させることも可能である。

[Finale](../Page/Finale.md "wikilink")や[Sibelius](https://ja.wikipedia.org/wiki/Sibelius "wikilink")などのような楽譜作成ソフトウェアとは異なり、LilyPond自体は[GUIを持たない](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。しかしながら、出版にも耐えうるほどの質の高い楽譜を出力することができる。また、GUIをもつソフトウェアの中にも、[Rosegarden](../Page/Rosegarden.md "wikilink")や[NoteEdit](https://ja.wikipedia.org/wiki/NoteEdit "wikilink")、[Canorus](https://ja.wikipedia.org/wiki/Canorus "wikilink")、[Denemo](https://ja.wikipedia.org/wiki/Denemo "wikilink")、[Frescobaldi](https://ja.wikipedia.org/wiki/Frescobaldi "wikilink")のようにLilyPondの形式で出力できるものがある。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Fibonacci_composition.svg "wikilink")

手作業で版が作成されていた時代の浄書のルールを忠実に再現することによって質の高い楽譜を作ることが、LilyPondの目標のひとつである。近年の商用の楽譜作成ソフトウェアの品質の向上は著しいが、ときにLilyPondはそれらよりも質の高い楽譜を作ることができるといわれることもある。

[ミュートピアプロジェクト](https://ja.wikipedia.org/wiki/ミュートピアプロジェクト "wikilink")では、フリーの楽譜を配布することを目的としており、そのためにLilyPondを使用している。これは、コラボレーションによる音楽百科事典「」も同様である。Wikiの記事上のLilyPondに関する記事を直接編集するには、[MediaWiki](../Page/MediaWiki.md "wikilink")インタフェースのひとつであるを使うことができる。

## LilyPond のソースファイルの例

パーセント記号 (%) が書かれると、その行は以後コメントと見なされる。ここでは[可読性](https://ja.wikipedia.org/wiki/可読性 "wikilink")の向上のために `%%` と書かれている。

LilyPondにおいては、[音名](https://ja.wikipedia.org/wiki/音名 "wikilink")、[オクターヴ](../Page/オクターヴ.md "wikilink")、[音価](https://ja.wikipedia.org/wiki/音価 "wikilink")の順に記述される。オクターブを指定するためには、[引用符](../Page/引用符.md "wikilink") (') と[コンマ](../Page/コンマ.md "wikilink") (,) を使用し、それぞれが基準音から1オクターヴ上、1オクターヴ下を意味する。なお、デフォルトでは基準音は[中央ハ](https://ja.wikipedia.org/wiki/中央ハ "wikilink")の1オクターヴ下のハ音である。たとえば、 `a'4` と記述すればそれは440Hz付近のA音（イタリア音名：ラ）の四分音符を意味する。

LilyPondの特殊な文法の一つとして、括弧類の扱いがある。直感的には、`[d8 c]`と記述したくなるような場合、`d8[ c]`と記述するのが正しい。すなわち、これらの命令は常に音の命令の後に指定し、それぞれの音の属性として処理される。なお、この括弧 `[, ]` は、八分音符を桁で繋げる命令である。

LilyPondの入力方式には、絶対入力と相対入力の2つの方法がある。絶対入力の方法においては、音のオクターヴは毎回指定されなければならない。相対入力の方法においては、直前の音から最も近いオクターヴを基準にして自動的に選ばれる。すなわち、オクターヴを指定しなければ直前の音から見て上下[増四度](https://ja.wikipedia.org/wiki/増四度 "wikilink")以内の該当する音名の音が自動的に選択される。[減五度](https://ja.wikipedia.org/wiki/減五度 "wikilink")以上跳躍する場合に、直前の音から相対的に何オクターヴ上下するかを記述すればよい。たとえば、`c g`と記述した場合、G音はC音から見て[完全四度](https://ja.wikipedia.org/wiki/完全四度 "wikilink")下のものが選択される。[完全五度](https://ja.wikipedia.org/wiki/完全五度 "wikilink")上のものを選択させるには`c g'`と記述しなければならない。なお、ここの例では相対入力の方法で書かれている。

[文字コード](../Page/文字コード.md "wikilink")は[UTF-8](../Page/UTF-8.md "wikilink")のみが使用される。このため、一つのファイル内で[デンマーク語](../Page/デンマーク語.md "wikilink")、[ヘブライ語](../Page/ヘブライ語.md "wikilink")、[朝鮮語](../Page/朝鮮語.md "wikilink")などの文章を混在させることも可能である。なお、ソースファイルの最初の一行は、 [Emacs](../Page/Emacs.md "wikilink")に常にUTF-8で読み書きを行うようにする命令である。 Emacs以外の[テキストエディタ](../Page/テキストエディタ.md "wikilink")を使用する場合には、各自UTF-8を使用するように注意しなければならない。

``` latex
#!lilypond firebreathers.ly -*- coding: utf-8; -*-
%% Theme to "Fire Breathers", a homebrew NES game perpetually
%% under development.  Composed by Urpo Lankinen.

%% Note: The composer has made this source code available
%% to Wikipedia under the GFDL license.  Other versions outside
%% Wikipedia are typically under CC BY-SA license.

%% This file uses Finnish note names (for example, where
%% Americans use "F#" and "Bb", Finns use "Fis" and "B").
%% Dutch note names are used by default.
\include "suomi.ly"

%% Optional language upgrade helper.
\version "2.6.0"

%% The header block defines the titles and texts.
\header {
    title = "Theme to ``Fire Breathers!''"
    instrument = "For the 2A03 or SID"
    composer = "Urpo Lankinen"
    enteredby = "Urpo Lankinen"
    updatedby = "Jan Nieuwenhuizen"
    date = "June 2005"
}

Melody = \relative c'' {
   \clef treble
   \time 3/4
   \key a \minor

   %% The piece starts with a quarter-note partial bar, "\partial 4"
   %% tells so to LilyPond.
   \partial 4
   a4 | e'4.( d8[ c]) r8 | d4.( c8[ h]) r8 | a2. | e2
   a4 | e'4.( d8[ c]) r8 | d4.( e8[ f]) r8 | e2. | r2
   e4 |  f4.( e8[ d]) r8 | d4.( c8[ h]) r8 | a2. | e2
   a4 | e'4.( d8[ c]) r8 | d4.( c8[ h]) r8 | a2. ~ a2 r4 | \bar "|."
}

%% This is the second voice.
SecondVoice = \relative c {
   \clef bass
   \time 3/4
   \key a \minor

   \partial 4
    r4 | e2.              | d2.             | a2. | e2
    a4 | e'2.             | d2       f4     | e2. | r2.
       |  f2.             | d2.             | a2. | e2
    a4 | e'2.             | d2       h4     | a2. ~ a2 r4 | \bar "|."
}


%% Melodies, lyrics and chords can be assigned to a variable and then
%% be *reused* elsewhere.  Here are three different accompaniment
%% patterns, which are used throughout the accompaniment melody.
AccompA = \relative c { a4 e'8 a, e' a, | }
AccompB = \relative c { g4 d'8 g, d' g, | }
AccompC = \relative c { e,4 h'8 e, h' e, | }

Accompaniment = {
   \clef bass
   \time 3/4
   \key a \minor

   \partial 4
    r4 | \AccompA \AccompB \AccompA \AccompA
        \AccompA \AccompB \AccompA \AccompA
        \AccompC \AccompC \AccompA \AccompA
        \AccompA \AccompB \AccompA | a2 r4 | \bar "|."
}

%% The top level music definition.
<<
  \new Staff \Melody
  \new Staff \Accompaniment
  \new Staff \SecondVoice
>>
```

### 上記の出力結果

[Firebreathers.svg](https://ja.wikipedia.org/wiki/File:Firebreathers.svg "fig:Firebreathers.svg")

## 関連項目

  - [Denemo](https://ja.wikipedia.org/wiki/Denemo "wikilink") - LilyPondのGUI環境

  - [Frescobaldi](https://ja.wikipedia.org/wiki/Frescobaldi "wikilink") - LilyPondの[統合開発環境](../Page/統合開発環境.md "wikilink")

  - [ミュートピアプロジェクト](https://ja.wikipedia.org/wiki/ミュートピアプロジェクト "wikilink") - 著作権が切れた作品の楽譜を公開するプロジェクト

  - [Karaoke](https://ja.wikipedia.org/wiki/Karaoke "wikilink") - \*.kar ファイル（楽譜と歌詞付き）を配布する

  - \- [楽譜作成ソフトウェア](../Page/楽譜作成ソフトウェア.md "wikilink")

  - [Muse](../Page/Muse.md "wikilink") - MIDI の作成・再生フリーソフト

## 外部リンク

  - [LilyPond ... みんなの楽譜作成](http://lilypond.org/)（公式サイト）
  - [LilyPond ドキュメント](http://lilypond.web.fc2.com/)（有志による公式サイトの和訳。日本語訳されたドキュメントがある）
  - [LilyPond Forum](http://www.nabble.com/Gnu---Lilypond-f1718.html) - hosted by [Nabble](http://www.nabble.com) archiving LilyPond mailing lists into a searchable forum.
  - [The LilyPond Wiki](http://lilypondwiki.tuxfamily.org/index.php?title=Main_Page)
  - [Lilypond-based Musical Scores Archive](http://www.mutopiaproject.org/)
  - [Denemo, a GUI for LilyPond](http://www.gnu.org/software/denemo/denemo.html).
  - [Frescobaldi. LilyPondのためのエディタ](http://frescobaldi.org/).
  - [Musipedia, a collaborative music encyclopedia that uses LilyPond](http://www.musipedia.org/)
  - [<http://MusiciansWiki.com> - Wiki site for musicians with support for Lilypond input](http://musicianswiki.com)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:コンピュータミュージック](https://ja.wikipedia.org/wiki/Category:コンピュータミュージック "wikilink") [Category:音楽ソフトウェア](https://ja.wikipedia.org/wiki/Category:音楽ソフトウェア "wikilink")