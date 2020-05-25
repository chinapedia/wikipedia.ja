> この記事は[Simulink](https://ja.wikipedia.org/wiki/Simulink)から翻訳されています。


**Simulink**（シミュリンク）は[MathWorks](https://ja.wikipedia.org/wiki/MathWorks "wikilink")社によって開発された、[モデリング](https://ja.wikipedia.org/wiki/モデリング "wikilink")、[シミュレーション](../Page/シミュレーション.md "wikilink")、[解析](../Page/解析.md "wikilink")のためのマルチドメインシミュレーション及びダイナミックシステムである。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:Radar.gif "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Control_-_2.png "wikilink")

[MATLABプロダクトファミリ](http://jp.mathworks.com/products/)の一つであるが、[インストール](../Page/インストール.md "wikilink")されているMATLABの構成によってはSimulinkが構成されていない場合もある。

おもな[インタフェースはグラフィカルな](../Page/インタフェース_\(情報技術\).md "wikilink")[ブロックダイアグラム](https://ja.wikipedia.org/wiki/ブロックダイアグラム "wikilink")ツールと、カスタマイズ可能なブロック[ライブラリ](../Page/ライブラリ.md "wikilink")のセットである。 Simulinkは[MATLAB](../Page/MATLAB.md "wikilink")環境によって提供され、MATLABとともに動作する。 Simulinkはマルチドメインシミュレーションおよびデザインのために[制御理論](../Page/制御理論.md "wikilink")、[デジタル信号処理](../Page/デジタル信号処理.md "wikilink")などの分野で広く使われている。

専門分野ごとにブロックがまとめられたブロックセット (blockset) はMathWorks社によって多数用意されているが、ブロックセットによっては特定のToolboxが必要になることもある。たとえばデジタル信号処理で頻繁に使用する[DSP System Toolbox](http://jp.mathworks.com/products/dsp-system/index.html/)の場合、[Signal Processing Toolbox](http://jp.mathworks.com/products/signal/)が必須となる。

## アドオン製品

MathWorks社、[サードパーティー](../Page/サードパーティー.md "wikilink")の多くの[ハードウェア](../Page/ハードウェア.md "wikilink")または[ソフトウェア](../Page/ソフトウェア.md "wikilink")・プロダクトはSimulinkに利用できる。

### コード生成

MathWorksによる製品の[Simulink Coder](http://jp.mathworks.com/products/simulink-coder/index.html)を利用することで、Simulink上で作成したブロック線図モデルから、システムの[リアルタイム実施のために](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")、[C言語](../Page/C言語.md "wikilink")のコード（Cコード）を自動生成できる。 コードの効率と柔軟性が向上するため、迅速な繰り返しのためのその柔軟性と能力のために、[組み込みシステム](../Page/組み込みシステム.md "wikilink")デザイン作業のための一般的なツールであることに加え、広く使われている。

また、[Embedded Coder](http://jp.mathworks.com/products/embedded-coder/index.html)は組み込みシステム用の効率的なコードを生成する。

そして[アドオンは](https://ja.wikipedia.org/wiki/機能拡張 "wikilink")、[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")などの[マイコンを含む](../Page/マイクロコンピュータ.md "wikilink")、特定のEmbedded Targetをサポートする。

さらに、MathWorksによる[HDL Coder](http://jp.mathworks.com/products/hdl-coder/index.html)を使用することで、Simulinkのブロック線図モデルおよび[Stateflow](https://ja.wikipedia.org/wiki/Stateflow "wikilink")チャートから自動的に[VHDL](../Page/VHDL.md "wikilink")および[Verilog](../Page/Verilog.md "wikilink")が生成できる。

## 関連項目

  - Toolboxe及びアドオン
      - [Stateflow](https://ja.wikipedia.org/wiki/Stateflow "wikilink")
  - [PLECS](https://ja.wikipedia.org/wiki/PLECS "wikilink")
  - [LMS Imagine.Lab AMESim](https://ja.wikipedia.org/wiki/:en:AMESim "wikilink")
  - [LabVIEW](../Page/LabVIEW.md "wikilink")
  - [データフロープログラミング](../Page/データフロープログラミング.md "wikilink")
  - [フローベースプログラミング](https://ja.wikipedia.org/wiki/フローベースプログラミング "wikilink") (FBP)

## 脚注

## 外部リンク

  - [MathWorks日本語サイトの製品ページ](http://jp.mathworks.com/products/simulink/)
      - [MATLAB & Simulink Student Version (日本語版) 製品ページ](http://jp.mathworks.com/academia/student_version/)
      - [SimPowerSystems](http://jp.mathworks.com/products/simpower/)
  - [日本語マニュアル](http://jp.mathworks.com/help/index_ja_JP.html)
      - [日本語マニュアルのアーカイブ](http://jp.mathworks.com/help/doc-archives_ja_JP.html)
  - [MATLAB/Simulink関連日本語書籍一覧](http://jp.mathworks.com/support/books/)
  - [日本語サポートページ (日本語技術ヘルプは「リソースを探す\>製品を選ぶ」)](http://jp.mathworks.com/support/)
      - [日本語アクティベーション、インストール、およびスタートアップのトラブルシューティング](http://jp.mathworks.com/support/install-matlab.html)
  - [MATLAB EXPO JAPAN](http://www.matlabexpo.com/jp/)
  - [MATLAB Central（MATLABユーザコミュニティ）](http://jp.mathworks.com/matlabcentral/) - Simulinkに関しても取り扱っている

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")