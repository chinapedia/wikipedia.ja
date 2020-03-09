> この記事は[EDICOLOR](https://ja.wikipedia.org/wiki/EDICOLOR)から翻訳されています。


**EDICOLOR** （エディカラー）は、[キヤノンITソリューションズ](https://ja.wikipedia.org/wiki/キヤノンITソリューションズ "wikilink")が開発・販売していた[DTP](../Page/DTP.md "wikilink")ソフトウェアである。

## 概要

[Windowsと](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")との間で完全なクロスプラットフォーム互換性を実現しており、[仮想フォント](https://ja.wikipedia.org/wiki/仮想フォント "wikilink")によるレイアウトワークや、日本語組版（特に[縦組み](https://ja.wikipedia.org/wiki/縦組み "wikilink")処理）に強いという特徴を持つ。なお、公には発表されてはいないが[エフテル日東組版](https://ja.wikipedia.org/wiki/エフテル日東組版 "wikilink")はEDICOLORの機能限定版である。

Macintosh版の7.0以降はmacOS専用アプリケーションとなっており、[Classic Mac OSの環境では動作しない](../Page/Classic_Mac_OS.md "wikilink")。そのため、ベンダー側ではバージョン6および7系統の販売・サポートも継続している。なお、[Snow Leopardには非対応となっている](https://ja.wikipedia.org/wiki/Mac_OS_X_v10.6 "wikilink")。

最新バージョンは10（[2012年](../Page/2012年.md "wikilink")6月現在）。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[OpenType](../Page/OpenType.md "wikilink")に完全対応し、[パッケージ](https://ja.wikipedia.org/wiki/パッケージ "wikilink")には[イワタ](https://ja.wikipedia.org/wiki/イワタ "wikilink")の[フォント](../Page/フォント.md "wikilink")が添付されている。

2016年12月に販売・開発を終了し、2018年12月でサポートも終了した。

## 特徴

仮想フォント機構の搭載により、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")でなくアプリケーションのレベルで[フォント](../Page/フォント.md "wikilink")を管理しており、起動時に総ての実フォント・仮想フォント情報を読み込む。この理由もあって、起動時間は他のDTPツールと比してかなり長いが、これは使用しないフォントを外すことで短縮できる。

DTP業界全体としては[Adobe InDesign](../Page/Adobe_InDesign.md "wikilink")・[QuarkXPress](../Page/QuarkXPress.md "wikilink")などに比してシェアは微弱であるが、官公庁などでの使用実績が高い。また、[電算写植](https://ja.wikipedia.org/wiki/電算写植 "wikilink")レベルの綿密な日本語組版を要求する出版社などで使用されている。

### 日本語組版能力

Adobe InDesign・QuarkXPressなどの欧米原産ソフトと異なり、純日本製である。基本設計レベルで日本語組版に対応しているため、日本語[CTSによく見られる](https://ja.wikipedia.org/wiki/Computer_Typesetting_System "wikilink")[原稿用紙](https://ja.wikipedia.org/wiki/原稿用紙 "wikilink")のような文字枠（後に発売されたAdobe InDesignも、日本語版において同様のグリッド機能を実装することになる）を持ち、[禁則](https://ja.wikipedia.org/wiki/禁則 "wikilink")処理などもカスタマイズが可能。ただし細かい「ハウスルール」（出版社や媒体における組版ルールの微妙な差異）に関しては一部対応できない場合もあるため、この場合は他のレイアウトソフト同様手作業で「それらしく組み上げる」必要がある。 また、「日本語組版」に重きを置きすぎたためか、バージョン6.0までは[ウムラウト](https://ja.wikipedia.org/wiki/ウムラウト "wikilink")（[トレマ](https://ja.wikipedia.org/wiki/トレマ "wikilink")）や[アクサンテギュ](https://ja.wikipedia.org/wiki/アクサンテギュ "wikilink")などを付加した[1バイト](https://ja.wikipedia.org/wiki/1バイト "wikilink")文字が入力できない（シフトJIS以外の文字コード使用を想定していない）プログラムの構造になっていた（無理に入力しようとすると「半角カナ」に置き換わる）。なお、バージョン7.0以降ではUnicodeも扱うことができる。

### オールインワンパッケージ

EDICOLORはDTPに必要とされる機能を詰め込んだ**オールインワン**構成となっており、基本的には追加で[プラグイン](https://ja.wikipedia.org/wiki/プラグイン "wikilink")を購入する必要がない。

  - 表組機能
    例えばQuark XPress4.1以前では表を作成する機能を実装しておらず（6.0で導入された）、表組を行う場合は多数の罫線を組み合わせるか、サードパーティから販売されている専用のプラグイン（QuarkXPressの場合、特に[XTension](https://ja.wikipedia.org/wiki/XTension "wikilink")という）を購入することが必要になる。
    それに対してEDICOLORやInDesignは表組機能を標準で搭載している。両者の表組機能はそれぞれ全く違う指向性を持ち、EDICOLORは表枠内での複雑な体裁指定に優れ、逆にInDesignではページや段をまたがった表の作成、表内テキストの差し替え（訂正）などに弱い。表枠を「インラインオブジェクト」として文字枠内に流すこともできるが、修正作業が煩雑になるうえアプリケーションがエラーを起こし停止してしまうケースもある。
  - 外字
    日本語の書籍制作に当たっては、人名などで[JIS第](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")2水準外の[異体字](https://ja.wikipedia.org/wiki/異体字 "wikilink")や、また丸付き数字や記号類など、通常の[文字コード](../Page/文字コード.md "wikilink")にない文字が必要になることが多い。
    こういった文字は[外字](https://ja.wikipedia.org/wiki/外字 "wikilink")で対応することになる。一般にMacintoshDTPでは、サードパーティ製の外字フォントを購入して使用する。日本ではDTPセンタービブロスの発売している[ビブロス外字](https://ja.wikipedia.org/wiki/ビブロス外字 "wikilink")が絶大なシェアを持っている。
    EDICOLORには記号類用のシステム外字（SMI外字、SMI外字Plusを経て現在は「Edisys-OTF-Gaiji」）、記号と漢字を含む**EDI外字**が標準でバンドルされており、追加購入なしで書籍制作のニーズに応えることができる。
    このEDI外字にはEdiGaiMinIwataとEdiGaiGoIwataの2種類（バージョン7.0からはEdigai-OTF-MinIwata、同GoIwata）があるが、イワタエンジニアリングの制作した外字フォントで、それぞれ同社の[明朝体](https://ja.wikipedia.org/wiki/明朝体 "wikilink")と[ゴシック体](https://ja.wikipedia.org/wiki/ゴシック体 "wikilink")に合わせた書体デザインが行われている。これらの外字を扱う際は、「文字パレット」を表示させて任意の文字をクリックすることにより、自動的に入力した文字だけが外字フォントに置き換わるため、前記のビブロスフォントを利用する場合のように「外字部分を別のフォントに置き換える手作業」をする必要はない。
  - 自動ルビ振り
    [ルビ](https://ja.wikipedia.org/wiki/ルビ "wikilink")（振り仮名）処理は日本語の書籍を制作する上で大きな課題となり、その作業を簡素化すべく自動的にルビを振る、あるいはルビ振りを支援するソフトウェアが様々に開発されている。
    EDICOLORには**HummingBird**(ハミングバード)というルビ振りプラグインが標準で搭載されており、[常用漢字](../Page/常用漢字.md "wikilink")外や、[学年別漢字配当表](../Page/学年別漢字配当表.md "wikilink")の各学年ごと、といった細かい設定の元、かなりの高精度で自動的にルビ振り処理ができる。
    このルビ振りプラグインに搭載されている日本語解析プログラムは、キヤノンITソリューションズが販売している[RubyNavigation](https://ja.wikipedia.org/wiki/RubyNavigation "wikilink")というルビ振りアプリケーションと同等のものとされる。

### 仮想フォント

[仮想フォント](https://ja.wikipedia.org/wiki/仮想フォント "wikilink")機構とは、[コンピュータ](../Page/コンピュータ.md "wikilink")にインストールされていない[フォント](../Page/フォント.md "wikilink")を使って組版することを可能にするもので、Windows版でもOCFあるいはCIDのPostScriptフォントが扱えるようになり、これによってEDICOLORはWindows版とMacintosh版の間の完全な互換性を確保している。

原理的には、詰め情報を[AFMファイル](https://ja.wikipedia.org/wiki/AFMファイル "wikilink")から取得し、画面表示には代用書体を用いる。そのため仕様は不完全な[WYSIWYG](../Page/WYSIWYG.md "wikilink")となるが、フォント運用の[TCO](https://ja.wikipedia.org/wiki/TCO "wikilink")を低下させるのに役立つ。

## 製品名とその経緯

当初は住友金属工業株式会社（後に部門が切り離され、[住友金属システムソリューションズ](https://ja.wikipedia.org/wiki/住友金属システムソリューションズ "wikilink")に合流）から「SMI EDICOLOR」という製品名でリリースされていたが、住友金属システムソリューションズがキヤノンマーケティングジャパンに売却されたのに伴い名称変更された。

EDICOLORは、住友金属の大型DTP(CTS)システム[SMI EDIANの弟分という位置づけで](https://ja.wikipedia.org/wiki/Edian "wikilink")、当時パソコンDTPとしては珍しいカラー対応がなされていたためEDI**COLOR**の名を冠した。その後カラー対応は珍しいことではなくなったが、そのまま名称は定着している。

なお、バージョン1.0のリリース当時の定価は150万円であったという。その後大きく価格を下げ、10万円強で落ち着いている。

## 関連項目

  - [組版](https://ja.wikipedia.org/wiki/組版 "wikilink") - [DTP](../Page/DTP.md "wikilink") - [PostScript](../Page/PostScript.md "wikilink")
  - [QuarkXPress](../Page/QuarkXPress.md "wikilink")
  - [アドビシステムズ](../Page/アドビシステムズ.md "wikilink") - [InDesign](../Page/Adobe_InDesign.md "wikilink") - [PageMaker](https://ja.wikipedia.org/wiki/Adobe_PageMaker "wikilink") - [Illustlator](../Page/Adobe_Illustrator.md "wikilink")
  - [キヤノンITソリューションズ](https://ja.wikipedia.org/wiki/キヤノンITソリューションズ "wikilink") - [Edian](https://ja.wikipedia.org/wiki/Edian "wikilink") -[RubyNavigation](https://ja.wikipedia.org/wiki/RubyNavigation "wikilink")

## 外部リンク

  - [EDICOLOR 10 - キヤノンITソリューションズ](http://ps.canon-its.jp/ec/)

[Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink") [Category:キヤノン](https://ja.wikipedia.org/wiki/Category:キヤノン "wikilink")