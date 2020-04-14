> この記事は[Fiat-Shamirヒューリスティック](https://ja.wikipedia.org/wiki/Fiat-Shamirヒューリスティック)から翻訳されています。


**Fiat-Shamirヒューリスティック**は、honest verifierかつパブリックコインな[対話証明](https://ja.wikipedia.org/wiki/対話証明 "wikilink")プロトコルを[ハッシュ関数](../Page/ハッシュ関数.md "wikilink")を用いる事で[証明文](https://ja.wikipedia.org/wiki/証明文 "wikilink")作成プロトコルや[電子署名](../Page/電子署名.md "wikilink")方式に変換する方法。

対話証明プロトコルから証明文作成プロトコルを作成する方法は以下の通り:

対話証明プロトコルにおける、verifierからの送信メッセージ(**チャレンジ**)の代わりに、その時点までのverifierのviewのハッシュ値を用いる。証明プロトコル終了時点における、verifierのviewと送信したハッシュ値の組の列が証明文である。

より厳密には、対話証明プロトコル\((P(w),V)(x)\)から、作られた証明文作成プロトコルは以下の通り。

  -
    Set \(v\gets x\)
    While(1){
      -
        Set \(c\gets H(v)\)
        \(r\gets\)(cを送信した時の\(P(x,w)\)のレスポンス)
        If(\(r=\mathbf{end}\)) break;
        else \(v\gets v\mid\mid(c,r)\)
    }
    Return v

こうして作成された証明文vが正当なものであるかどうかを検証するには、まずverifierのviewのハッシュ値からチャレンジを作成し、次に証明プロトコルとしての検証操作をおこなう。証明プロトコルとしての検証を通れば証明文は正当であるとみなす。

対話証明プロトコルから署名方式を作成する方法もほぼ同様である。 チャレンジとして、viewのハッシュ値の代わりに、viewと署名したいメッセージとの[コンカチネーション](https://ja.wikipedia.org/wiki/コンカチネーション "wikilink")のハッシュ値を用いる。 証明プロトコル終了時点における、verifierのviewとハッシュ値の組の列が署名文である。

より厳密には、対話証明プロトコル\((P(w),V)(x)\)から作られた署名アルゴリズムは以下の通り。

  -
    Input 署名したい文章 M
    Set \(v\gets x\)
    While(1){
      -
        Set \(c\gets H(v,M)\)
        \(r\gets\)(cを送信した時の\(P(x,w)\)のレスポンス)
        If(\(r=\mathbf{end}\)) break;
        else \(v\gets v\mid\mid(c,r)\)
    }
    Return v

こうして作成された署名文vが正当なものであるかどうかを検証するには、まずverifierのviewと署名したいメッセージとのコンカチネーションのハッシュ値からチャレンジを作成し、次に証明プロトコルとしての検証操作をおこなう。証明プロトコルとしての検証を通れば署名文は正当であるとみなす。

## 関連項目

  - [暗号理論](../Page/暗号理論.md "wikilink")
  - [ランダム・オラクル](https://ja.wikipedia.org/wiki/ランダム・オラクル "wikilink")
  - [ゼロ知識証明](../Page/ゼロ知識証明.md "wikilink")
  - [電子署名](../Page/電子署名.md "wikilink")
  - [Shnorr署名](https://ja.wikipedia.org/wiki/Shnorr署名 "wikilink")

[ru:Протокол Фиата — Шамира](https://ja.wikipedia.org/wiki/ru:Протокол_Фиата_—_Шамира "wikilink")

[Category:暗号技術](https://ja.wikipedia.org/wiki/Category:暗号技術 "wikilink")