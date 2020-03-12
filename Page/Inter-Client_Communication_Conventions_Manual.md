> この記事は[Inter-Client Communication Conventions Manual](https://ja.wikipedia.org/wiki/Inter-Client_Communication_Conventions_Manual)から翻訳されています。


**Inter-Client Communication Conventions Manual**（**ICCCM**、）とは、[X Window Systemの同一](../Page/X_Window_System.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")上の[クライアント間の相互運用に関する標準規格である](../Page/クライアント_\(コンピュータ\).md "wikilink")。[MITの](../Page/マサチューセッツ工科大学.md "wikilink") X Consortium により[1988年](../Page/1988年.md "wikilink")に検討開始された。バージョン 1.0 は[1989年](../Page/1989年.md "wikilink")7月、バージョン 2.0 は[1994年](../Page/1994年.md "wikilink")初めにリリースされている。

X は意図的に「方針ではなく機構 (mechanism, not policy\[1\])」を決めている。そのため、クライアント間の相互運用についての標準規格が必要となった。ICCCM は[カット・アンド・ペースト](https://ja.wikipedia.org/wiki/カット・アンド・ペースト "wikilink")のバッファ、[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")とのやり取り、セッション管理、共有資源の操作方法、デバイスにおける色の管理などを規定している。

ICCCM は曖昧で正しく実装が難しいことでよく知られている\[2\]。*The UNIX-Haters Handbook*という書籍の7章 "The X-Windows\[<small>ママ</small>\] Disaster" では、ICCCM を以下のように酷評している。

> In summary, ICCCM is a technological disaster: a toxic waste dump of broken protocols, backward compatibility nightmares, complex nonsolutions to obsolete nonproblems, a twisted mass of scabs and scar tissue intended to cover up the moral and intellectual depravity of the industry’s standard naked emperor.

  -
    （和訳）まとめると、ICCCM は技術的災難である。壊れたプロトコルのゴミ溜め、後方互換の悪夢、過去の問題とも言えない問題の解決とも言えない解決策、産業標準の裸の王様の道徳的かつ知的堕落を隠すためのカサブタの集合体である。

さらに、一部は既に古臭く、実装に適していない\[3\]。X のクライアント開発者の多くは[ウィジェット・ツールキット](../Page/ウィジェット・ツールキット.md "wikilink")や[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")を参照して作業し、直接 ICCCM を参照することはない。しかし、ICCCM を明確化し最新の状況向けに更新する試みとして [Extended Window Manager Hints](../Page/Extended_Window_Manager_Hints.md "wikilink") [1](http://standards.freedesktop.org/wm-spec/wm-spec-latest.html) (EWMH) があり、これは広く受け入れられている（また、必要に応じて拡張が続けられている）。

## 脚注

## 外部リンク

  - [Inter-Client Communication Conventions Manual, Version 2.0](http://tronche.com/gui/x/icccm/)

## 参考文献

  -
[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.
3.