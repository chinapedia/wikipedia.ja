> この記事は[SLAX](https://ja.wikipedia.org/wiki/SLAX)から翻訳されています。


**SLAX**（スラックス）とは、[Debian](../Page/Debian.md "wikilink")（[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")の一つ）をベースとした[チェコ](../Page/チェコ.md "wikilink")発の[Live CDである](../Page/Live_CD.md "wikilink")。Slax 9より前は、最も古くからある[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")（配布パッケージ）のひとつである[Slackware](../Page/Slackware.md "wikilink")をベースとしていた。

## 概要

日本国内では、[産業技術総合研究所](../Page/産業技術総合研究所.md "wikilink")が日本語化を行っている[Debian](../Page/Debian.md "wikilink")ベースの[KNOPPIX](../Page/KNOPPIX.md "wikilink")が有名だが、SLAXは[Slackware](../Page/Slackware.md "wikilink")のシンプルで素直な構成という特徴を活かして、シンプルさと軽快さに特徴がある。 KNOPPIXが色々な用途で使用できるように大量のアプリケーションが最初から用意されているため、現在ではCD-ROMに収まらないような巨大なサイズとなっているのに対し、SLAXはデスクトップOSとして必要十分なものにアプリケーションが限定されて用意されており、必要な機能を満たしながらコンパクトになっている。 さらに、多くのソフトウェアはモジュールとして配布されていて、簡単に追加が可能。

従来の1CD Linuxは、[CD-ROM](../Page/CD-ROM.md "wikilink")ドライブの遅さから、遅いという印象を持たれることがあるが、このSLAXは起動時間や反応時間が短いことからCD-ROM起動ということを感じられないほどの軽快さが特徴である。

現在、開発が進められているバージョン6では、[ファイルシステム](../Page/ファイルシステム.md "wikilink")に、以前より使用されていた[UnionFS](https://ja.wikipedia.org/wiki/UnionFS "wikilink")に代わり、[Aufs](https://ja.wikipedia.org/wiki/Aufs "wikilink")(Another unionFS)が採用されるのに伴い、モジュールファイル周辺に大幅な変更（バージョン5.xで使われていた.moファイルが.lzmファイルに変更された）が加えられ、uselivemod/unuselivemod コマンドも activate/deactivate に変更された。ちなみに、バージョン6は従来のCD用のiso形式に加えてUSBメモリ用のtar形式でも配布されている。

また、現在、開発者のTomas Mは、[KDE](../Page/KDE.md "wikilink")4.x.xと[FluxBox](https://ja.wikipedia.org/wiki/FluxBox "wikilink")1.x.xをデスクトップに採用したバージョン7に向けて作業しており、バージョン6は、安定したKDE3.5.8.を必要とする人のための、バージョン5とバージョン7の中間、ハイブリッドになる、としている。

Slax5はこれ以降メンテナンスしないと宣言されている。

## 種類

Slax5は公式に4バージョン存在する。

  - SLAX Standard Edition
      - 最もスタンダードなバージョン。
  - SLAX KillBill Edition
      - [wine](https://ja.wikipedia.org/wiki/wine "wikilink")や[Qemu](https://ja.wikipedia.org/wiki/Qemu "wikilink")などを加え、[Windowsのアプリケーションを動かせるようにしたもの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。
  - SLAX Server Edition
      - サーバ用のモジュールを加えたもの。
  - SLAX Frodo Edition
      - 他のバージョンの基礎部分。[X Window Systemなどは含まれていない](../Page/X_Window_System.md "wikilink")。
  - SLAX Popcorn Edition
      - [Xfce](../Page/Xfce.md "wikilink")を採用し、115MBまで縮小したもの。

## 日本語化

日本語化については、

  - [ライブCDの部屋](http://simosnet.com/livecdroom/)
  - [slax-ja](http://hatochan.dyndns.org/slax-ja/)

で、独自に行われている。

ライブCDの部屋版は、SLAXにアプリケーションを追加して汎用性を高める方向で特徴を出しており、slax-ja は、オリジナルのシンプルさを保ちながら日本語化を行っている。

slax-jaについては、Webからの無償ダウンロードだけではなく、埼玉のLinuxユーザーズグループである小江戸らぐ（日本語化作業者が主宰）から、[コミックマーケット](../Page/コミックマーケット.md "wikilink")や[オープンソースカンファレンス](https://ja.wikipedia.org/wiki/オープンソースカンファレンス "wikilink") Tokyoなどで、説明書を付けてDVDケース等にパッケージングしたものを有償で配布している。

## 派生版

[SlackwareFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:SlackwareFamilyTree1210.svg "fig:SlackwareFamilyTree1210.svg")

### Slax派生

※[Slax派生版一覧に掲載されたもの](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Slax-based "wikilink")

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>300MB以下[1]。SLAXから派生。</p></td>
</tr>
</tbody>
</table>

## 関連ディストリビューション

  - AliXe - フランス語版。ソフトウェアの変更やアップデートがされている。
  - Arudius - 情報保証や脆弱性評価のためのソフトを含んでいる。サイズはわずか210MBで、システム全てをRAM上で処理できる。
  - De-ICE.net - 侵入テストのターゲットとなるように設計されている。
  - GoblinX - デスクトップユーザー向け。カスタマイズされた[KDE](../Page/KDE.md "wikilink")や[Xfce](../Page/Xfce.md "wikilink")や[Enlightment](https://ja.wikipedia.org/wiki/Enlightment "wikilink")等のWMをウリにしている。
  - [Ophcrack](https://ja.wikipedia.org/wiki/Ophcrack "wikilink") - [Windows NTのパスワードのクラック用](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")。バージョン3.3.0以降はSLAXではなく、[Slitaz](https://ja.wikipedia.org/wiki/Slitaz "wikilink")ベース\[2\]。
  - SimpleSlax - 98MBに圧縮したSlax。Slax5.1.8をベースとしていて、最小限の、もしくは古いハードウェア向け。
  - SLAMPP - ホームサーバとして使えるようにアレンジされている。
  - Whax - 情報保証や[侵入テストのためのツールを含んでいる](https://ja.wikipedia.org/wiki/ペネトレーションテスト "wikilink")。なお、後継の[BackTrack](https://ja.wikipedia.org/wiki/BackTrack "wikilink")の最新版はSLAXではない。

## 脚注

## 関連項目

  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [Linuxライブディストリビューションの比較](../Page/Linuxライブディストリビューションの比較.md "wikilink")

## 外部リンク

  - [SLAXの本家サイト](http://www.slax.org/)
  - [SLAXの公式ブログ](http://blog.slax.org/category/slax-blog/)

<!-- end list -->

  - [slax-ja](http://hatochan.dyndns.org/slax-ja/)
  - [小江戸らぐ](http://hatochan.dyndns.org/koedolug/)

[Category:Slackware派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Slackware派生ディストリビューション "wikilink") [Category:LiveCD](https://ja.wikipedia.org/wiki/Category:LiveCD "wikilink")

1.
2.