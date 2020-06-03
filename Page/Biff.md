> この記事は[Biff](https://ja.wikipedia.org/wiki/Biff)から翻訳されています。


**biff**とは、UNIXにおける[メールの到着を通知するシステムである](../Page/電子メール.md "wikilink")。

## 使用法

新しいメールメッセージが届けられたときに、**biff**はすぐにそれを読むことが出来るように受信者に知らせる。この通知には、メールの送信者名、件名と数行の本文が含まれており、メールの受信者がログインしている間、[tty](https://ja.wikipedia.org/wiki/tty "wikilink")に送られる。通知の際にはより確実にメールの着信を気づかせるために[ビープ音](../Page/ビープ音.md "wikilink")が鳴る。

以下のコマンドは通知を有効にする。

  -
    `biff y`

以下のコマンドは通知を無効にする。

  -
    `biff n`

## メカニズム

[MTAは通知プロセスを稼働させることに責任がある](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")。メールが配達されると、MTAは受信者名を**comsat**[デーモンに通知する](../Page/デーモン_\(ソフトウェア\).md "wikilink")。実質的な作業はここからcomsatによって行われる。comsatは、ユーザがどこに[ログインしているかを見つけてそこに通知を送る](https://ja.wikipedia.org/wiki/ログオン "wikilink")。comsatは、通知を送る前に、ttyのユーザ実行[許可ビットをチェックする](https://ja.wikipedia.org/wiki/パーミッション "wikilink")。それ以外では役に立たないこのビットはユーザがメールの通知を受けるかどうかの要望を示し、`biff y`によってセットされ、`biff n`によってクリアされる。

## 代替

実のところbiffはもはやあまり使われていない。画面に表示されている簡単によみがえらせることの出来ないような有用な情報を突然、予想外のbiffの通知テキストの塊で上書きされてしまうと煩わしいからである。現在のいくつかのMTAはcomsatをサポートせず、biffは使い物にならない。

しかし、メール受信通知の概念自体はオリジナルのbiffとcomsatがほぼ完全に捨てられたときでさえ、非常に人気があった。よって、多くのbiffの代替が存在し、そのいくつかは、xbiff、xlbiff、kbiff、gnubiff、wmbiffやxbuffyといった、biffに似た名前である。概念はUnixの世界を超え、[AOL](../Page/AOL.md "wikilink")の"You've got mail"という音声はしゃべるbiffとみなすことが出来る。

## 変種

3番目の動作モードを持つベンダー特有のバージョンがあった。それは、**y**と**n**に加えて、通知を端末に一切テキストを表示させずに一対のビープ音だけに低減させる**b**をセットすることが出来る。これはbiffの破壊性を低減した。しかし、あきらかに目立たなくなった。

## 発祥と名前について

**biff**は[BSD](../Page/BSD.md "wikilink")から発祥し、[バークレーの開発者によって知られていた](../Page/カリフォルニア大学バークレー校.md "wikilink")[犬](https://ja.wikipedia.org/wiki/犬 "wikilink")にちなんで名付けられた。

いくつかの文献[1](http://www.mcsr.olemiss.edu/unixhelp/didyou/biff.html)\[[http://www.unixguide.net/unix/faq/1.3.shtml\]は、郵便配達人に吠えていた犬であり、そこからメール通知システムの名前を選ぶことは自然の選択である、と記している](http://www.unixguide.net/unix/faq/1.3.shtml%5Dは、郵便配達人に吠えていた犬であり、そこからメール通知システムの名前を選ぶことは自然の選択である、と記している)。[ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")はこの説明を否定する\[[http://www.catb.org/jargon/html/B/biff.html\]が、少なくとも犬が存在していたことは間違いないようである](http://www.catb.org/jargon/html/B/biff.html%5Dが、少なくとも犬が存在していたことは間違いないようである)。

[ピーター・H. サルスの著した](https://ja.wikipedia.org/wiki/:en:Peter_H._Salus "wikilink")『UNIX の 1/4 世紀』 ISBN 4-7561-3659-1 や、BSD 系 OS の[マニュアル](../Page/Manページ.md "wikilink") biff(1) には、その犬は[1993年](../Page/1993年.md "wikilink")の8月に、15歳で亡くなったことが記されている。 \[1\] \[2\] \[3\]

また、この『UNIX の 1/4 世紀』には、犬の Biff と飼い主の Heidi Stettner を写した写真や、Biff がとても人に懐いた犬だったことや、多くの学生がボールを投げては Biff に取ってきてもらって楽しんでいたことなどが紹介されている。

そのほかに同書には、犬の Biff が郵便配達員に吠えかかっていたというのはデマにすぎないということ\[4\]や、[Bill Joy](../Page/ビル・ジョイ.md "wikilink") と、このコマンドの開発者である John Foderero の二人は、のちに biff というコマンドの名前について、"Be notified if mail arrives" (メールが届けば、お知らせしてくれる) という説明を考えつくために長時間を要したということなども、飼い主の Heidi Stettner から伝え聞いた話として紹介されている。

## 出典・参考文献

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:電子メール](https://ja.wikipedia.org/wiki/Category:電子メール "wikilink")

1.
2.  (訳:このコマンドは、Heidi Stettner の飼い犬から名づけられた。彼(その犬)は1993年の8月に、15歳で亡くなった。)
3.  (訳:"Biff" は、Heidi Stettner の飼い犬だった。彼(その犬)は、1993年の8月に、15歳で亡くなった。)
4.  (訳:Heidi によれば、Biff が郵便配達員に吠えていたという逸話は、悪趣味な作り話である。)