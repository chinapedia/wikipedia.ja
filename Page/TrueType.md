> この記事は[TrueType](https://ja.wikipedia.org/wiki/TrueType)から翻訳されています。


**TrueType**（トゥルータイプ）は[デジタルフォントの規格である](../Page/フォント.md "wikilink")。[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") や [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") で標準的に利用されている。

## 規格

TrueType は、[アップルコンピュータが開発し](../Page/アップル_\(企業\).md "wikilink")、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に発表したスケーラブルフォントの規格で、補助目的のビットマップフォントを埋め込むこともできる。3次[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")で曲線を表現する [PostScriptフォント](https://ja.wikipedia.org/wiki/PostScriptフォント "wikilink")とは異なり、2次ベジェ曲線を接続したもので曲線を表現する\[1\]。

高度な[ヒンティング言語を実装したのも特徴で](https://ja.wikipedia.org/wiki/フォントヒンティング "wikilink")、さまざまなフォントサイズにおいてピクセル単位で表示を制御することができる。これにより、低解像度なディスプレイなどで不適切な表示が発生するのを避けることができる。

拡張子は「.TTF」と「.TTC」の2種類である。前者は単体のフォントファイルであり、後者は1つのファイルに、プロポーショナルフォントや等幅フォントなどの類似する複数のフォントファイルを収納したものである。

後継規格となる [OpenType](../Page/OpenType.md "wikilink") では PostScript (CFF) ベースと TrueType ベースでアウトラインの記述方式を選ぶことが可能だが、TrueType をベースとした場合、拡張子は「.TTF」もしくは「.TTC」と変わらない。

macOS では、拡張子「.DFONT」も使用されている。これは、[Mac OS 9](https://ja.wikipedia.org/wiki/Classic_Mac_OS#Mac_OS_9 "wikilink") までの TrueType におけるデータの扱い方を変えたものであり、それまで[リソースフォーク](https://ja.wikipedia.org/wiki/リソースフォーク "wikilink")にフォントデータを格納して「フォントスーツケース」という形で取り扱っていた（TrueType 以外の型式も同様であった）ものを、[データフォーク](https://ja.wikipedia.org/wiki/データフォーク "wikilink")側にフォントデータを移し変えたものである。また、フォントスーツケースで取り扱う TrueType は、macOS では FFIL 形式となる。いずれも1つのファイル（もしくはスーツケース）に複数のフォントの収録が可能だが、これらの型式は他の OS では対応していない。

## 経緯

もともと TrueType は、アップルが[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")の [PostScriptフォント](https://ja.wikipedia.org/wiki/PostScriptフォント "wikilink")に対抗するために開発したものであった。その後、アップルは[マイクロソフト](../Page/マイクロソフト.md "wikilink")に無償で技術供与をし、マイクロソフトは [Windows 3.1](../Page/Microsoft_Windows_3.x.md "wikilink") で TrueType の[ラスタライズ](https://ja.wikipedia.org/wiki/ラスタライズ "wikilink")エンジンを実装した\[2\]。その後、 [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") では TrueType は標準的なフォント形式となったが、アップルは PostScript と TrueType が両立するという形となった。

1995年には、OpenType の前身となる TrueType Open がマイクロソフトによって発表され、その後1996年には TrueType に加え PostScript フォントのアウトライン形式もサポートした OpenType が発表された。現在では Windows にバンドルされているフォントの多くが、TrueType アウトラインの OpenType フォントとなっている。

現在では [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") でも利用されるようになり、数多くの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")においても標準的に利用されている。

## 脚注

## 関連項目

  - [OpenType](../Page/OpenType.md "wikilink")
  - [FreeType](https://ja.wikipedia.org/wiki/FreeType "wikilink") - [フリーのフォントラスタライザ](https://ja.wikipedia.org/wiki/FLOSS "wikilink")。TrueType にも対応。

## 外部リンク

  - [TrueType™ Reference Manual - Apple Developer](https://developer.apple.com/fonts/TrueType-Reference-Manual/)（Apple による TrueType の規格書）

[Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink") [Category:書体](https://ja.wikipedia.org/wiki/Category:書体 "wikilink")

1.  PostScript フォントでは PostScript の curveto オペレータにより3次ベジェ曲線を使用できる。TrueType は「2次[B-スプライン曲線](https://ja.wikipedia.org/wiki/B-スプライン曲線 "wikilink")を使用している」との説明がインターネット上に多数見られるが、規格書には「2次B-スプライン曲線」とは書かれていない。https://developer.apple.com/fonts/TrueType-Reference-Manual/RM01/Chap1.html （ただし、仕様中で説明されているベジェ曲線の接続方法により作られる曲線は2次[B-スプライン曲線](https://ja.wikipedia.org/wiki/B-スプライン曲線 "wikilink")と一致する）
2.  [A brief history of TrueType - Microsoft Typography](https://www.microsoft.com/typography/TrueTypeHistory.mspx)