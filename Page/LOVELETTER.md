> この記事は[LOVELETTER](https://ja.wikipedia.org/wiki/LOVELETTER)から翻訳されています。


**LOVELETTER**（ラブレター）とは、[2000年](../Page/2000年.md "wikilink")に発見された[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")の一種（[ワーム](https://ja.wikipedia.org/wiki/コンピュータウイルス#ワーム "wikilink")）である。「**I LOVE YOU**」（アイラブユー）とも呼ばれる。

## 概要

作者は[フィリピン](https://ja.wikipedia.org/wiki/フィリピン "wikilink")の専門学校生であったが、ウイルス発見からまもなく[逮捕](../Page/逮捕.md "wikilink")されている。

### 感染方法

[電子メール](../Page/電子メール.md "wikilink")を介して感染を広げる。そのメールは題名が「*I Love you*」、本文は「*kindly check the attached LOVELETTER coming from me*（訳:このメールに付属しているラブレターをチェックしてください）」となっている。\[1\]メールには「**LOVE-LETTER-FOR-YOU.TXT.vbs**」というファイルが添付されており、これを実行すると感染する。

### 被害

感染すると、[Outlookの](https://ja.wikipedia.org/wiki/Microsoft_Outlook "wikilink")[アドレス帳](https://ja.wikipedia.org/wiki/アドレス帳 "wikilink")に登録された[メールアドレス](https://ja.wikipedia.org/wiki/メールアドレス "wikilink")すべてに、自動的に自分の複製を送りつける。このとき発信されるメールと添付ファイルは前述のとおりである、そして、拡張子が「vbs」「vbe」「js」「css」「wsh」「sct」「hta」「jpg」「jpeg」「mp2」「mp3」であるファイルをハードディスクの中から探し出し、自分の複製を上書きすることで破壊してしまう。さらに、勝手に悪意あるプログラムをダウンロードする機能もあるが、このダウンロード元サイトが閉鎖されており、この機能は実際は機能しないと報告されている。

### 特徴

このウイルスの特徴はいくつかあるが、特に[ラブレターを装うことにより](https://ja.wikipedia.org/wiki/恋文 "wikilink")[ソーシャル・エンジニアリング](../Page/ソーシャル・エンジニアリング.md "wikilink")的手法を用いていたことがあげられる。冷静に考えれば馬鹿らしいほどの手法であるが、これに引っかかる被害者が多かった。また、[Windowsが初期設定では](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[拡張子](../Page/拡張子.md "wikilink")を表示しない点をつき、**.TXT.vbs**という[二重拡張子によってウイルス本体](https://ja.wikipedia.org/wiki/拡張子#拡張子が引き起こす問題 "wikilink")（[VBScript](../Page/VBScript.md "wikilink")ファイル）を[テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")（.txtのファイル）であるかのように偽装していたことも、ビギナーを中心に感染を広げる原因となった。また[スクリプトウイルスの特徴として改変が容易であることから亜種が大量発生したことも](https://ja.wikipedia.org/wiki/コンピュータウイルス#ウイルスの種類 "wikilink")、流行の一因となった。

#### ソースの特徴

これといった高度な技術は使用されていない。

さらに、ソース全体に「未完成部分」が点在している。また、MAPI制御部分と 一部のサブルーチンの開発スタイル、ファンクションスペルの厳密性に、微妙なズレがあるため「二人以上の共同開発」という説がささやかれている。

上記にもある通り、Outlookに登録されたメールアドレスすべてに自分の複製を送りつける様になっているが、逆に言えば、Outlook以外の[メーラー](https://ja.wikipedia.org/wiki/メーラー "wikilink")や[Mac OS Xを使っている環境では](https://ja.wikipedia.org/wiki/macOS "wikilink")、感染や増殖をしないということである。他にも多数、環境に左右される不安定なソースが使用されている。

## 脚注

## 外部リンク

  - [LOVE LETTERとは](http://e-words.jp/w/LOVE20LETTER.html) IT用語辞典
  - [代表的なウイルスの動作と被害内容 LOVELETTER（ラブレター）](http://www.soumu.go.jp/joho_tsusin/security/kiso/k04_love.htm) [総務省](../Page/総務省.md "wikilink")
  - [I LOVE YOU ウイルスのソースを解析](http://www.nda.co.jp/memo/iloveyou/)[山崎はるかのメモ](https://ja.wikipedia.org/wiki/山崎晴可 "wikilink")
  - [メールで広まる「I Love You」マクロウイルスに注意](https://internet.watch.impress.co.jp/www/article/2000/0508/love.htm)INTERNET Watch

[Category:Windowsのウイルス](https://ja.wikipedia.org/wiki/Category:Windowsのウイルス "wikilink") [Category:コンピュータ・ワーム](https://ja.wikipedia.org/wiki/Category:コンピュータ・ワーム "wikilink") [Category:2000年](https://ja.wikipedia.org/wiki/Category:2000年 "wikilink")

1.  ソースの特性上、必ずこの文章であり、日本語文などの生成はできない。