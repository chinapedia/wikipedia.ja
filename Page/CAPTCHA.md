> この記事は[CAPTCHA](https://ja.wikipedia.org/wiki/CAPTCHA)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Captcha.png "wikilink") （キャプチャ）は [チャレンジ/レスポンス型テスト](https://ja.wikipedia.org/wiki/チャレンジ/レスポンス型テスト "wikilink")の一種で、応答者がコンピュータでないことを確認するために使われる。

[ウィキペディア](https://ja.wikipedia.org/wiki/ウィキペディア "wikilink")においても、ログインしていない状態のユーザ(IPユーザー)が[外部リンク](https://ja.wikipedia.org/wiki/外部リンク "wikilink")を追加する際、[スパム (メール)の防止のためこの種の](../Page/スパム_\(メール\).md "wikilink")[認証](../Page/認証.md "wikilink")が用いられる。外部リンクを追加しない場合にも濫用される。

この用語は[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の[ルイス・フォン・アン](https://ja.wikipedia.org/wiki/ルイス・フォン・アン "wikilink")、[マヌエル・ブラム](https://ja.wikipedia.org/wiki/マヌエル・ブラム "wikilink")、ニコラス・J・ホッパー、[IBM](../Page/IBM.md "wikilink")のジョン・ラングフォードによって[2000年](../Page/2000年.md "wikilink")に造られた。 という語は「」（[コンピュータ](../Page/コンピュータ.md "wikilink")と[人間](../Page/人間.md "wikilink")を区別する完全に自動化された公開[チューリングテスト](https://ja.wikipedia.org/wiki/チューリングテスト "wikilink")）の[バクロニム](https://ja.wikipedia.org/wiki/バクロニム "wikilink")である。

認知ソフトウェアに対抗するために難化が繰り返された結果、既に人間の認識が困難になるほど難化しており、本来の目的を果たせていない場合がある（「過剰な難化」の節を参照）。

## 概要

もっとも一般的な画像によるCAPTCHAの場合、次のように画像に記されている文字や数字を読み取ることができるか否かによって人間と機械を判別する。

1.  システムは、ランダムな文字や数字の列を画面に表示する。表示される文字は歪んでいたり一部が覆い隠されていたりして、機械が自動的に読み取ることは難しい。

2.  ユーザーは画面に描かれている文字の列を読み取り、同じ文字列をシステムに入力する。

3.  システムが表示した文字列とユーザーが打ち込んだ文字列が一致していれば、ユーザーは歪んだ画像を認識する能力を持っていると考えられる。システムはそのユーザーが人間であると推測する。

4.  システムにアクセスできる人間を日本語使用者に限定したい場合、画像の文字種を[ひらがな](../Page/平仮名.md "wikilink")・[カタカナに限定する](../Page/片仮名.md "wikilink")。

5.  応用として、画像の文字種で[アラビア数字](../Page/アラビア数字.md "wikilink")のみを入力させる場合、アラビア数字そのものではなく**読み方をひらがな・カタカナで表示する**（例：123456 → イチ に サン よん ご ロク）。

<!-- end list -->

  -
    アラビア数字だと、言語を問わずほとんどの人間が読めるが、ひらがな・カタカナまで読める日本国外人口はそれほど多くないため、日本国外からのアクセスを大幅に抑制できる。

コンピュータがテストを監督することから、人間が監督する標準的な[チューリングテスト](https://ja.wikipedia.org/wiki/チューリングテスト "wikilink")との対比として、 はときに**逆チューリングテスト**とも呼ばれる。

は日本語では「画像認証」とも呼ばれている。

## 起源

はもともと、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に[AltaVista](https://ja.wikipedia.org/wiki/AltaVista "wikilink")のアンドレイ・ブローダーとその同僚たちによって、[ボットが彼らの](../Page/インターネットボット.md "wikilink")[検索エンジン](../Page/検索エンジン.md "wikilink")に[URLを追加するのを防ぐために開発された](../Page/Uniform_Resource_Locator.md "wikilink")。彼らは画像を[OCRによる攻撃に耐えられるようにする方法を探していた](../Page/光学文字認識.md "wikilink")。[ブラザー工業](https://ja.wikipedia.org/wiki/ブラザー工業 "wikilink")の[スキャナの取扱説明書には](../Page/イメージスキャナ.md "wikilink")、OCRの結果を改善するためには均質な[活字面](https://ja.wikipedia.org/wiki/活字面 "wikilink")、無地の背景を用いるよう薦められていた。そこで彼らは取扱説明書に「OCR認識の結果を悪くする」と書いてある条件を真似て最初の  を作り出した。ブローダーによれば、 は検索エンジンへのスパム追加を95%削減できたという。

## 用途

は[ボットが種々のコンピュータのサービスを使うのを防ぐために使われる](../Page/インターネットボット.md "wikilink")。 応用用途として挙げられることとして、ボットがオンライン投票に参加したり、（後で[スパムを送るために使われるかもしれない](../Page/スパム_\(メール\).md "wikilink")）無料メールやサービスのアカウントに登録（一人が複数のアカウントに登録）するのを防ぐことなどがある。さらに最近では、ボットが生成するスパムを防ぐために、メールメッセージが配達される前に（未承認の）送り主が  テストの通過を要求することなどがある。

また、 は人間のリソースを使うこととなるが、この労力を「人間であることの確認」以外にも文書の[電子化](https://ja.wikipedia.org/wiki/電子化 "wikilink")に使うという  プロジェクトも行われている。

## 特徴

定義より、 は以下の特徴を持っている:

  - は**自動化**されている。テストを管理運用するにあたって人間の介在をほとんど、あるいは全く必要としない。これはテストにおける人間の管理や介入の必要性を避けることができ、コストや信頼性においても明らかに有益である。

  - 使用される[アルゴリズム](../Page/アルゴリズム.md "wikilink")は多くの場合**公開**される。ただし、[特許](https://ja.wikipedia.org/wiki/特許 "wikilink")によって妨げられるかもしれない。これが規定されているのは、 の突破には、[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")などの手法を用いて達成できるような単なる(秘密の)アルゴリズムの発見よりも、[人工知能](../Page/人工知能.md "wikilink")の分野における難問の解決法を要求する、ということが必要なためである。

## アクセシビリティ

視覚認識の問題に基づく  は、[視覚障害](https://ja.wikipedia.org/wiki/視覚障害 "wikilink")を持ったユーザが保護されたリソースにアクセスする際の妨げとなる。 は機械可読ではないように設計されているので、[スクリーンリーダ](https://ja.wikipedia.org/wiki/スクリーンリーダ "wikilink")のような支援ツールでも解釈できない。

しかし、 が視覚的である必要はない。 例えば[音声認識](../Page/音声認識.md "wikilink")のように、人工知能によって解くのが困難な問題であれば、 として使うことができる。ユーザが音声認識問題を選択できるような  の実装もある。しかしながら、音声（聴覚） の開発は画像（視覚） よりも後れを取っており、あまり普及はしていない。また、テキストの意味を理解させるような問題も  として用いることができる。例えば、[論理パズル](https://ja.wikipedia.org/wiki/論理パズル "wikilink")や常識・計算問題などである。

[W3Cによる論文](../Page/World_Wide_Web_Consortium.md "wikilink")\[1\]では  のアクセシビリティ上の問題点がいくつか示されている。

## 回避策

を回避するために、囮ウェブサイトでユーザを集め、彼らを騙して  の問題を解かせるという手法がとられることがある。

ユーザがスパマーの開設した囮ウェブサイトを訪れると、スパマーのサーバーは攻撃対象のサーバーにアクセスし、アカウント取得等の処理を開始する。そして攻撃対象の  をダウンロードし、囮ウェブサイトにアクセスするための  としてユーザに提示する。ユーザは、 が再利用されるとは知らずに、正しい回答を提供する。そしてスパマーはその回答を利用し、攻撃対象の  を突破することができる。

また、大量の人員を雇い、彼らに解かせるという手法もある。W3Cの論文\[2\]には、「そのようなオペレータは一時間に数百の  を解読できる」とある。一方、この手法は経済的に実行不能であるとする指摘もある\[3\]。

Moriらは[IEEE](../Page/IEEE.md "wikilink") CVPR'03において、最も有名な  の一つであるEZ-Gimpyを突破する手法を詳述した論文\[4\]を発表し、その手法は92%の確率で突破可能であると検証された。また、より複雑であまり広く普及していないGimpyプログラムが、同じ手法により33%の確率で突破された。しかし、彼らのアルゴリズムが実際に実装され、利用されているかどうかについては、現時点でははっきりしていない。

機械による解読も巧妙になってきている。[PWNtcha](http://sam.zoy.org/pwntcha/)のようなプロジェクトによって、広く普及していた  の解読精度が目覚ましく進歩し、結果として  を過剰に難化させることとなった。

文字認識技術や囮ウェブサイトによらず、既知の  画像のセッションIDを再利用するという手法もある\[5\]。

## 過剰な難化

視力に問題のない人にとってさえ、知能化が進む認知ソフトウェアに対抗して設計された新世代の  は解くことが著しく困難である。すでに無視できないほどの人数の認識能力を上回っており、結果として人間の応答すら遮断してしまっている。

を認識できなかった人々は応答を諦めているものと考えられ、そのような人々にとって過剰に難化した  は単なる障害でしかない。

## 脚注

## 関連項目

  - [認証](../Page/認証.md "wikilink")
  - [reCAPTCHA](https://ja.wikipedia.org/wiki/reCAPTCHA "wikilink")

## 外部リンク

  - [](http://www.captcha.net/)
  - [ の歴史](http://www2.parc.com/istl/projects/captcha/history.htm)

###  の実装

####

  - [](http://freshmeat.net/projects/pycaptcha/)  を実装する  モジュールのコレクション
  - [](http://captchas.net/sample/python/)

####

  - [](http://jcaptcha.sourceforge.net)
  - [](http://www.crt.realtors.org/projects/reCaptcha/)
  - [](http://simplecaptcha.sourceforge.net/)
  - [](http://www.standards-schmandards.com/index.php?2005/01/01/11-captcha)

#### PHP

  - [](http://www.phpclasses.org/browse/package/1768.html)
  - [](http://www.planet-source-code.com/vb/scripts/ShowCode.asp?txtCodeId=739&lngWId=8)
  - [](http://www.pscode.com/vb/scripts/ShowCode.asp?txtCodeId=762&lngWId=8)
  - [](http://php.webmaster-kit.com)
  - [](http://www.phpclasses.org/formsgeneration)
  - [](http://pear.php.net/package/Text_CAPTCHA)
  - [](http://www.ocr-research.org.ua)
  - [](http://www.cocoavillagepublishing.com/development/tools/php/scripts/)
  - [](http://www.captcha.ru/en/kcaptcha/)

####

  - [](http://search.cpan.org/search?dist=Authen-Captcha)
  - [](http://search.cpan.org/dist/GD-SecurityImage/)

####

  - [](http://www.u229.no/stuff/Captcha/)

####

  - [](http://www.codeproject.com/aspnet/CaptchaImage.asp)
  - [](http://www.codeproject.com/aspnet/CaptchaControl.asp)

####

  - [](http://captcha.rubyforge.org/)

####

  - [](http://www.squeaksource.com/SW2Captcha/)

###  サービス

  - <http://www.protectwebform.com/>
  - <http://captchas.net/>
  - <http://address-protector.com/>

###  突破

  - <http://www.captchacreator.com/>
  - [Breaking CAPTCHAs without using OCR](http://www.puremango.co.uk/cm_breaking_captcha_115.php) - OCRを用いない  の突破
  - [How spammers crack captchas using free porn.](http://www.boingboing.net/2004/01/27/solving_and_creating.html)
  - [Recognizing Objects in Adversarial Clutter: Breaking a Visual CAPTCHA](http://ieeexplore.ieee.org/iel5/8603/27265/01211347.pdf) Mori他。IEEEから刊行。IEEEの有償の会員のみが表示可能
  - [OCR Research Team defeats weak CAPTCHAs.](http://www.ocr-research.org.ua)
  - [Using AI to beat CAPTCHA and post comment spam](http://www.brains-N-brawn.com/aiCAPTCHA/)
  - [PWNtcha - CAPTCHA decoder](http://sam.zoy.org/pwntcha/)

[Category:人工知能](https://ja.wikipedia.org/wiki/Category:人工知能 "wikilink") [Category:認証技術](https://ja.wikipedia.org/wiki/Category:認証技術 "wikilink") [Category:頭字語](https://ja.wikipedia.org/wiki/Category:頭字語 "wikilink")

1.  [Inaccessibility of CAPTCHA](http://www.w3.org/TR/turingtest/)
2.
3.  [Petmail Design](http://petmail.lothar.com/design.html#auto34)
4.  [Breaking a Visual CAPTCHA](http://www.cs.berkeley.edu/~mori/gimpy/mori_gimpy.pdf)
5.  [Breaking CAPTCHA without OCR](http://www.puremango.co.uk/cm_breaking_CAPTCHA_115.php)