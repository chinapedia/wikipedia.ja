> この記事は[EPICS](https://ja.wikipedia.org/wiki/EPICS)から翻訳されています。


**EPICS**（**Experimental Physics and Industrial Control System**）は、[加速器](https://ja.wikipedia.org/wiki/加速器 "wikilink")、[望遠鏡](https://ja.wikipedia.org/wiki/望遠鏡 "wikilink")、その他の大規模は[実験](../Page/実験.md "wikilink")用機器を運用する[分散制御システム](https://ja.wikipedia.org/wiki/分散制御システム "wikilink")を開発・実装するのに使われるソフトウェア環境である。EPICS は [SCADA](https://ja.wikipedia.org/wiki/SCADA "wikilink") の機能も提供する。このツールは、多数のコンピュータからなる[ネットワークで制御とフィードバックを行うシステムの開発の補助となるよう設計されている](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")。[アルゴンヌ国立研究所](https://ja.wikipedia.org/wiki/アルゴンヌ国立研究所 "wikilink")が[2004年](../Page/2004年.md "wikilink")に開発したもので、独自の[オープンソース](../Page/オープンソース.md "wikilink")ライセンスでリリースされている。

EPICS は、コンピュータ間の通信モデルとして[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")と[出版-購読型モデル](../Page/出版-購読型モデル.md "wikilink")を採用している。コンピュータ群（サーバまたは [Input Output](../Page/入出力.md "wikilink") Controller）が、付随する測定機器を使って実験データと制御データを収集する。この情報を **Channel Access** (CA) というプロトコルで別のコンピュータ群（クライアント）に送る。CA は広帯域のネットワークプロトコルであり、科学実験のような[リアルタイム性を要する応用に適している](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")。

## 概要

EPICS は IOC (Input Output Controller) 経由で実世界とインタフェースする。IOCとしては、一般的な[PCまたは](../Page/パーソナルコンピュータ.md "wikilink")[VMEバス](https://ja.wikipedia.org/wiki/VMEバス "wikilink")規格の組み込みプロセッサがあり、各種標準（[GPIB](https://ja.wikipedia.org/wiki/GPIB "wikilink")、[RS-232](../Page/RS-232.md "wikilink")、[IPキャリア](../Page/Internet_Protocol.md "wikilink")）で制御対象機器（[電動機](../Page/電動機.md "wikilink")、[熱電対](../Page/熱電対.md "wikilink")、[スイッチなど](../Page/開閉器.md "wikilink")）と接続したり、制御システム装置（[オシロスコープ](https://ja.wikipedia.org/wiki/オシロスコープ "wikilink")、[ネットワーク・アナライザなど](https://ja.wikipedia.org/wiki/ネットワーク・アナライザ_\(高周波回路\) "wikilink")）と接続する。IOC上にはレコード (record) の[データベース](../Page/データベース.md "wikilink")があり、個々のレコードがデバイスやデバイスの制御を表している。IOCの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")としては、高いリアルタイム性を求める場合は [VxWorks](../Page/VxWorks.md "wikilink") や [RTEMS](https://ja.wikipedia.org/wiki/RTEMS "wikilink") を使うが、他のシステムへの移植も進んでいる。ある程度のリアルタイム性でよい場合は、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") や [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") が使える。

ネットワーク上の他のコンピュータは、チャンネル (channel) という概念を通して IOC とやり取りする。例えば、[加速器](https://ja.wikipedia.org/wiki/加速器 "wikilink")に複数のセクターがあり、セクター間にシャッターがあるとする。一般に1つのシャッターには複数のチャンネルが対応する。シャッターの動きを起動する出力チャンネルと、シャッターの状態（閉じている、開いている、動作中など）を見る入力チャンネルと、シャッターの両側の温度や圧力を示すアナログの入力チャンネル群である。チャンネルには名前が付けられ、\[装置名\]:\[信号名\] の形式である（例えば、ACCELERATOR_RING:TEMP_PROBE_4 など）。

ほとんどの操作は、EDM (editor/display manager) または MEDM (Motif/EDM) といった独立した[GUIパッケージから直接行える](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。これらによって、ダイヤル、ゲージ、[テキストボックス](https://ja.wikipedia.org/wiki/テキストボックス "wikilink")、単純なアニメーションなどを組み合わせたGUI画面を生成できる。

EPICS とやり取りできるのはそのようなGUIソフトウェアだけではない。CA プロトコルを扱えるソフトウェアなら、レコードの値にアクセスできる。例えば、EPICSのウェブサイトには [MATLAB](https://ja.wikipedia.org/wiki/MATLAB "wikilink")、[LabVIEW](../Page/LabVIEW.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Tcl](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")、[ActiveX](../Page/ActiveX.md "wikilink") などで CA を扱えるようにする拡張パッケージがある。従って、EPICS で制御されている装置を起動するスクリプトを書くといったことも容易である。

## レコード型の例

EPICS のレコードにはいくつかの種類がある。ここでは主なものを挙げる。これら以外にもレコードはあるし、ユーザーが独自のレコード型を生成することもできる。

各レコードには複数のフィールド (field) があり、それぞれ役目を持っている。

  - AI、AO
    アナログ入出力レコード。[アナログ](../Page/アナログ.md "wikilink")の値を格納し、何らかの位置、温度、圧力などを表している。デバイスの生のデータとの相互変換がある程度可能（スケーリングやオフセットなど）。
  - BI、BO
    バイナリ入出力レコード。装置のステータスとコマンドを表すのに使われることが多い。
  - Calc、Calcout
    他のレコードにアクセスし、それらの値を使った計算ができるレコード。例えば、電流、入力電圧、出力電圧 などを使って、電動機の効率を百分率で表示するなど。
  - Stepper Motor
    [ステッピングモーター](../Page/ステッピングモーター.md "wikilink")の制御用レコード。加速度、速度、位置などで設定できる。

## レコード処理

EPICS におけるレコードには *scan time* が設定される必要があり、さもなくばデフォルトで *passive* とされる。passive のレコードは（PROCフィールドに書き込みしない限り）処理されない。一般にレコードは定期的に処理されるよう *scan time* が設定される（例えば0.1秒間隔など）。また、何らかのイベント発生時のみ処理されるようレコードを設定することもできる。

## EPICS を利用している主な施設

  - アジア
      - [J-PARC](https://ja.wikipedia.org/wiki/J-PARC "wikilink") - [高エネルギー加速器研究機構](../Page/高エネルギー加速器研究機構.md "wikilink")、[日本原子力研究開発機構](https://ja.wikipedia.org/wiki/日本原子力研究開発機構 "wikilink") （[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")）
      - [KEKB](https://ja.wikipedia.org/wiki/KEKB "wikilink") - 高エネルギー加速器研究機構 （日本）
      - [RIビームファクトリー](https://ja.wikipedia.org/wiki/RIビームファクトリー "wikilink") - [理化学研究所](https://ja.wikipedia.org/wiki/理化学研究所 "wikilink")　仁科加速器研究センター（日本）
      - [KSTAR](http://www.knfp.net/english/index1.html) - Korea Superconducting Tokamak Advanced Research （[大韓民国](https://ja.wikipedia.org/wiki/大韓民国 "wikilink")）
      - [BSRF (Beijing Synchrotron Radiation Laboratory)](http://www.ihep.ac.cn/bsrf/english/main/main.htm) and [BEPC II (Beijing Electron Positron Collider II)](http://www.ihep.ac.cn/BEPCII/index.html) - [高能物理研究所](http://www.ihep.cas.cn/)（[中国](https://ja.wikipedia.org/wiki/中国 "wikilink")）
  - オーストラリア
      - [Australian Synchrotron](http://www.synchrotron.org.au/content.asp?Document_ID=1) （[オーストラリア](../Page/オーストラリア.md "wikilink")）
  - ヨーロッパ
      - [ドイツ電子シンクロトロン](../Page/ドイツ電子シンクロトロン.md "wikilink") (DESY) （[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")）[1](http://www-kryo.desy.de/main/epics_main.html)
      - [Diamond Light Source](http://www.diamond.ac.uk/default.htm) - [ラザフォード・アップルトン研究所](https://ja.wikipedia.org/wiki/ラザフォード・アップルトン・ラボラトリー "wikilink") （[イングランド](../Page/イングランド.md "wikilink")）
      - [Swiss Light Source](http://www.sls.psi.ch/controls/) - ポールシェラー研究所 （[スイス](../Page/スイス.md "wikilink")）
      - [Berlin Electron Synchrotron (BESSY II)](http://www-csr.bessy.de/control/) （ドイツ）
  - 北アメリカ
      - [Advanced Light Source](http://csg.lbl.gov/CSG.html) - [ローレンス・バークレー国立研究所](https://ja.wikipedia.org/wiki/ローレンス・バークレー国立研究所 "wikilink") （[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")）
      - [Advanced Photon Source](http://www.aps.anl.gov/) - [アルゴンヌ国立研究所](https://ja.wikipedia.org/wiki/アルゴンヌ国立研究所 "wikilink") （アメリカ合衆国）
      - [Canadian Light Source Synchrotron](http://www.lightsource.ca/machine/controlinstrumentations.php) - [サスカチュワン大学](https://ja.wikipedia.org/wiki/サスカチュワン大学 "wikilink") （[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")）
      - [フェルミ研究所](https://ja.wikipedia.org/wiki/フェルミ研究所 "wikilink") （アメリカ合衆国）
      - [LIGO](https://ja.wikipedia.org/wiki/LIGO "wikilink") - [カリフォルニア工科大学](https://ja.wikipedia.org/wiki/カリフォルニア工科大学 "wikilink")、[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink") （アメリカ合衆国）
      - [Los Alamos Neutron Science Center (LANSCE)](http://lansce.lanl.gov/) - [ロスアラモス国立研究所](https://ja.wikipedia.org/wiki/ロスアラモス国立研究所 "wikilink") （アメリカ合衆国）
      - [National Superconducting Cyclotron Laboratory](http://www.nscl.msu.edu/) - [ミシガン州立大学](https://ja.wikipedia.org/wiki/ミシガン州立大学 "wikilink") （アメリカ合衆国）
      - [National Synchrotron Light Source](http://www.nsls.bnl.gov/) - [ブルックヘブン国立研究所](https://ja.wikipedia.org/wiki/ブルックヘブン国立研究所 "wikilink") （アメリカ合衆国）
      - [Spallation Neutron Source](http://neutrons.ornl.gov/) - [オークリッジ国立研究所](https://ja.wikipedia.org/wiki/オークリッジ国立研究所 "wikilink") （アメリカ合衆国）
      - [Stanford Synchrotron Radiation Laboratory](http://www-ssrl.slac.stanford.edu/) - [スタンフォード大学](../Page/スタンフォード大学.md "wikilink") （アメリカ合衆国）
          - [Stanford Linear Accelerator (SLAC)](http://www.slac.stanford.edu/comp/unix/package/epics/index.html)
      - [TJNAF](http://www.jlab.org/accel/controls/controls.html) - Thomas Jefferson National Accelerator Facility （アメリカ合衆国）
      - [TRIUMF](http://isacwserv.triumf.ca/) - [ブリティッシュコロンビア大学](https://ja.wikipedia.org/wiki/ブリティッシュコロンビア大学 "wikilink") （カナダ）
      - [W・M・ケック天文台](../Page/W・M・ケック天文台.md "wikilink") （アメリカ合衆国）[2](http://www2.keck.hawaii.edu/realpublic/epics/)

## 外部リンク

  - [EPICS website](http://www.aps.anl.gov/epics/)
  - [EPICS website Canada](http://www.epics.org)

[Category:制御工学](https://ja.wikipedia.org/wiki/Category:制御工学 "wikilink") [Category:素粒子物理学](https://ja.wikipedia.org/wiki/Category:素粒子物理学 "wikilink") [Category:ファクトリーオートメーション](https://ja.wikipedia.org/wiki/Category:ファクトリーオートメーション "wikilink")