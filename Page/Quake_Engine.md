> この記事は[Quake Engine](https://ja.wikipedia.org/wiki/Quake_Engine)から翻訳されています。


**クエイクエンジン**（Quake Engine）とは[ファーストパーソン・シューティングゲーム](../Page/ファーストパーソン・シューティングゲーム.md "wikilink")、[Quake](../Page/Quake.md "wikilink")の為に[id Softwareによって開発された](https://ja.wikipedia.org/wiki/id_Software "wikilink")[グラフィックエンジン](https://ja.wikipedia.org/wiki/グラフィックエンジン "wikilink")である。同社による同系列のゲームエンジンは現在5世代目の[id TECH5までリリースされているが](https://ja.wikipedia.org/wiki/id_TECH5 "wikilink")、ここでは次世、次々世代代エンジンであるQuakeII、QuakeIIIエンジンと、[DOOM](../Page/DOOM.md "wikilink")の名を冠しているが、存在自体はQuakeエンジン系の後継となる[DOOM3](https://ja.wikipedia.org/wiki/DOOM3 "wikilink")エンジンまでを紹介する。

どのエンジンにも共通であるがconfig.cfgという.cfgファイル（物によってq3config.cfgなど名前が変わるが）にゲームの画質設定からキーコンフィグ、さらにはサーバーの設定までもすべて記録され、知識さえあればゲーム内オプションでは設定しきれない項目までアクセス出来るのが特徴の一つである。またこのコンフィグファイルは.txtファイルの拡張子を変えた物であり、誰でもアクセス可能である。そしてコンソールコマンドで「exec \*\*\*.cfg」と打ち込むだけで、即座にキーマップなどの設定を変更出来る柔軟性を誇っている。しかもこのコマンドすらキーに設定可能なので、ゲーム内で用意されているラジオチャットを1ボタンで発言出来るようにしたり、その発言ボタン自体の位置を変更するなども1ボタンで可能となっている。

もう一つのエンジン共通の特性は「内部フォントをビットマップ形式で持つ」という物である。そのためフォントを自在に設定出来るという柔軟性があるが（そのためQuakeではSeqence Complete\!という仕掛けを動かした時のメッセージの「q」が、Quakeのマークとなっていた）、それが逆に2バイト文字の導入を困難な物としているため（2バイト文字を使えるようにするには、すべての漢字を.bmpファイルで作らないといけないため、それだけでも膨大なファイル容量となってしまう）、Quakeエンジン採用ゲームには、一部の日本語表記対応ゲーム（[Soldier Of Fortune2](https://ja.wikipedia.org/wiki/Soldier_Of_Fortune2 "wikilink")、XBOX360版&パッチディスク適応後の[CALL OF DUTY4](https://ja.wikipedia.org/wiki/CALL_OF_DUTY4 "wikilink")）などはあるが、名前まで含めた完全日本語表記可能になっているゲームが存在しない。

## Quake Engine

1996年にリリースされた。id Tech 2とも呼ばれる。今までのFPSは[DOOM](../Page/DOOM.md "wikilink")のように「マップは3D、アイテムや敵キャラクターは2D、キャラクターの高低差とは無関係に攻撃がヒットする」というゲームシステムを用いて開発されてきた。しかし、Quake Engineは家庭用PCの性能の制約が厳しい[1990年代](../Page/1990年代.md "wikilink")後半において、「マップや敵やアイテムをフル3Dで描画し、当たり判定にキャラクター同士の高低差も考慮する」というゲームシステムを実現させた。まだ3Dに対応した家庭用グラフィックカード自体が出始めの頃で、高価で数少ない状況にあったにも関わらず、従来から行われていたCPUによるソフトウェアレンダリングの他に、CGワークステーションにおいて高品質な描画を実現していたOpenGLへの対応を行った点も先進的である。このOpenGLによる高品質な描画を体験するために、一部のQuakeプレイヤーがQuakeとセットで広告されていた[3dfx](../Page/3dfx.md "wikilink")社の[Voodoo](https://ja.wikipedia.org/wiki/Voodoo "wikilink")という3Dグラフィックカードを買い求める結果になった。Quake EngineのゲームシステムとOpenGL対応によるグラフィック描画品質の高さは、1996年当時としては非常に先進的であるとの評価を受けた。

グラフィックスの特色としては、レイトレーシングによって事前に作成されたディフューズ（拡散）ライトマップを、マップ描画時にディフューズ（拡散）テクスチャとブレンド（モジュレート）する事によって、静的ではあるものの、リアルな照明表現を実現している。他の恩恵として、縦方向への視点移動と、その立体感を生かした[グレネードランチャー](https://ja.wikipedia.org/wiki/グレネードランチャー "wikilink")のような武器、マップ構成を可能にしたというのも特徴である。

また、このエンジンはDOOMエンジン以上に柔軟にできており、シングル/マルチプレイ用のトータルコンバージョン[MODに限らず](https://ja.wikipedia.org/wiki/Mod_\(コンピューターゲーム\) "wikilink")、[Team Fortressのようにゲームシステム自体を変更してしまうMODにも対応していた事や](https://ja.wikipedia.org/wiki/Team_Fortress "wikilink")、現在ではスタンダードになる[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")プロトコルによるマルチプレイにも対応し、外部ソフトの助けや有料マッチングサービス無しに「電話代と電気代」だけでLAN対戦だけでなくオンライン対戦を可能にしたエンジンでもある。さらにネットコードを進化させたエンジンとして「Quake World」というMODも存在する。ただし[サーバーブラウザ](https://ja.wikipedia.org/wiki/サーバーブラウザ "wikilink")は内蔵されていない。

現在GPLライセンスの元オープンソース化されており、マップやモデルさえ作ればいわゆる「Quakeクローン」のゲームを作成可能である。

### 採用作品

  - [Hexen II](https://ja.wikipedia.org/wiki/Hexen_II "wikilink")
  - [Heretic](https://ja.wikipedia.org/wiki/Heretic "wikilink")
  - [Nexuiz](https://ja.wikipedia.org/wiki/Nexuiz "wikilink")

### 改造エンジン

  - [Goldsource](https://ja.wikipedia.org/wiki/Goldsource "wikilink")
      -
        日本ではHalf-Life Engineとして有名である。Quakeエンジン同様の柔軟性で[Counter-Strike](https://ja.wikipedia.org/wiki/Counter-Strike "wikilink")のような優秀なMODも出現した。
        さらに改造が加えられGoldsourceは[Source Engineとなる](../Page/Source_Engine.md "wikilink")。2バイト文字への対応など大きな変更がなされたが、コンフィグファイルの構造にQuakeエンジン系の名残が見られる。

## QuakeII Engine

1997年にリリース。新規エンジンではなくid Tech 2の強化版である。Quake主要スタッフの[ジョン・ロメロ](https://ja.wikipedia.org/wiki/ジョン・ロメロ "wikilink")の退社後、QuakeエンジンをベースにQuake Worldのネットコードを取り入れるなど、大幅に改良を図ったエンジンである。Quakeエンジンで導入されたレイトレーシングによる事前計算ライトマップ・システムを更に進化させ、レイトレーシングの他にラジオシティによる間接照明計算を加え、柔らかい照明や影の表現を可能とした。それと視界角度の調整（fov）を取り入れるようになった。Quakeエンジンでは取り入れられていたMS-DOSへのサポートはQuakeIIエンジンから無くなっている。ソフトウェアレンダリングモードは継続してサポート。

Quakeエンジンではライトマップはモノクロに限られていたが、QuakeIIエンジンへの進化としてカラー光源が扱えるようになった。そして、キャラクターモデル等のアニメーションに頂点モーフィングが導入され、Quakeエンジンと比べて滑らかなアニメーションが可能となった。そのため「キャラがしゃがむ」などの新しいモーションを取り入れられるようになっている。

その代償ではあるが1998年発売のUnrealほどでは無いのだが、ソフトウェアモード、OpenGLモード共に異常とも言える重さであった。

Quakeエンジンでのバグであったロケットジャンプ、ストレイフジャンプをQuakeIIエンジンでは仕様として取り入れるようになった。

QuakeIIエンジンもGPLライセンスの元オープンソース化されている。

### 採用作品

  - [SIN-罪-](https://ja.wikipedia.org/wiki/SIN-罪- "wikilink")
  - [Daikatana](https://ja.wikipedia.org/wiki/Daikatana "wikilink")
  - [Kingpin](https://ja.wikipedia.org/wiki/Kingpin "wikilink")
  - [Soldier of Fortune](https://ja.wikipedia.org/wiki/Soldier_of_Fortune "wikilink")

など。3Dゲームが一般的となってきたために採用作品は多い。

### 改造エンジン

  - Qfusion
      -
        [Warsow](../Page/Warsow.md "wikilink")のために開発されたQuakeII改造エンジン。QuakeIIIエンジン用のマップを読み込めるようになるなど、さらに柔軟性が増している。

## QuakeIII Engine

1999年リリース。id Tech 3とも呼ばれる、Quake III Arenaのために開発されたエンジン。ゲーム自体が1対1、もしくは少数対少数に特化した物となったため、それに合わせたチューニングがされている。Quake Engine初のサーバーブラウザー内蔵となった。

QuakeIIエンジンで導入されたライトマップ作成時のラジオシティ計算を今作では敢えてせずにレイトレーシングのみにする事で、シャープな照明と影が表現されるようになった。また、ソフトウェア処理によるごく限定的な頂点シェーダーが導入された事や、テクスチャのブレンドモードやクランプモード、スクロールなどを容易にコントロール出来る簡易シェーダーシステムが導入された事により、アーティストの自由度が大幅に向上した。また、起動時にガンマテーブルを1-bitぶんオーバーブライトする事により、下位1-bitを犠牲にしつつも擬似的に0.0-2.0の輝度の高ダイナミックレンジ表現が可能となった。

マップやオブジェクトの描画に関しては、Quake\&QuakeIIエンジンではイミディエートモードによる描画だったが、QuakeIIIエンジンからはCompiled Vertex Arrayが利用されるようになり（ハードウェアT\&Lサポート)、マップやキャラクター等の殆どの頂点情報はビデオカードのメモリ上に静的に配置され効率的に描画されるようになった反面、CPUによるキャラクターの頂点モーフィング計算が出来なくなったため、キャラクターのアニメーションは僅かに滑らかさが劣る物となった。しかしQuakeIII:Team Arenaでは頂点スキニングがサポートされたため（MD4モデル）、前作と比べてもアニメーションの質は格段に向上した。

QuakeIIIエンジンから完全なハードウェアT\&Lとなり、ソフトウェアレンダリングが不能となっている。そのためにOpenGLモードでの描写が出来ないグラフィックボードでは起動しなくなっている。

元のゲーム性から生まれた仕様により、大規模マップでの描写が苦手であり、QuakeIII用マップでも大規模マップになるとPCのパフォーマンスが優れていてもフレームレートが低下し始めるのに加え、フレームレートが125と333になるとなぜかジャンプ力が上がるというバグを抱えている。このバグはid software側や大会オフィシャル側でも公認となっており、ほとんどのプロゲーマーが最大fpsを125に設定していた。

3作連続でオープンソース化されており、現在[Open Arenaや](https://ja.wikipedia.org/wiki/Open_Arena "wikilink")[Urban Terrorといったゲームが利用中](https://ja.wikipedia.org/wiki/Urban_Terror "wikilink")。

### 採用作品

  - [Star Wars Jedi Knight II: Jedi Outcast](https://ja.wikipedia.org/wiki/Star_Wars_Jedi_Knight_II:_Jedi_Outcast "wikilink")
  - [Soldier of Fortune II](https://ja.wikipedia.org/wiki/Soldier_of_Fortune_II "wikilink")
  - [Star Trek Elite Force](https://ja.wikipedia.org/wiki/Star_Trek_Elite_Force "wikilink")
  - [Medal of Honor: Allied Assault](../Page/メダル・オブ・オナー_アライドアサルト.md "wikilink")（正確にはQuakeIII:Team Arenaエンジンベース）
  - [American McGee's Alice（邦題：アリス イン ナイトメア）](../Page/アリス_イン_ナイトメア.md "wikilink")

### 改造エンジン

  - [Return to Castle Wolfenstein用エンジン](https://ja.wikipedia.org/wiki/Return_to_Castle_Wolfenstein "wikilink")
      -
        正式な名前は無いのだが、元のQuakeIIIエンジンでは無く、大規模マップ用にチューニングがされている。

さらにこれを改造したものが

  - [Wolfenstein: Enemy Territory用エンジン](../Page/Wolfenstein:_Enemy_Territory.md "wikilink")
  - [コール オブ デューティ用エンジン](../Page/コール_オブ_デューティ.md "wikilink")
      -
        さらに改造を加えられていき、が、[コール オブ デューティ4 モダン・ウォーフェアに至るまでコンフィグファイルはQuakeエンジンと同じ記述法となっている](../Page/コール_オブ_デューティ4_モダン・ウォーフェア.md "wikilink")。

などである。

## DOOM3 Engine

2004年リリース。id Tech 4とも呼ばれる。このエンジンを最初に採用したのが[DOOM3](https://ja.wikipedia.org/wiki/DOOM3 "wikilink")となるため、DOOMエンジンと名付けられているが、実際にはフル3Dエンジンであるため初代のDOOMエンジンとは関係なく、Quakeエンジンの直系である。しかし大きな仕様変化があったため、QuakeIIIエンジンとはほぼ別物となっている。[Unreal Tournament 2003搭載の](../Page/Unreal_Tournament.md "wikilink")[Unreal Engine2や同年発売の](../Page/Unreal_Engine.md "wikilink")[Half-Life 2搭載のSource](../Page/ハーフライフ2.md "wikilink") Engineと共に、3Dグラフィックの基準を大幅に引き上げたエンジンでもある。

グラフィックスの特色としては、先ずピクセル単位のリアルタイム・ライティングの導入が挙げられる。光源としては、点光源、平行光源、投影光源が利用でき、反射モデルとしては拡散(Diffuse)と鏡面反射(Specular)がサポートされた。また、バンプマップが導入された事により、少ない頂点数でより迫力のある凹凸が表現出来るようになった。そして、もう一つ大きな特色として、ステンシル・シャドウ・ボリューム法によるリアルタイム・シャドウの導入が挙げられる。ステンシル・シャドウには多様なアルゴリズムが存在するが、Doom3エンジンでは、John Carmack氏が考案したものの米Creative社が特許を先行取得した「カーマック・リバース」というアルゴリズムが利用されている。その他の特色としては、高度な頂点スキニングの導入、逆運動学(Inverse Kinematics)による足運び計算などが挙げられる。

これらのグラフィックスを実現するためのテクスチャー量は1マップにつき500MB近くになり、当時[VRAM](../Page/VRAM.md "wikilink")512MBを実現していたグラフィックボードが無かったため「最高画質モードはどんなPCでも使えない」とまで言われた。ローエンドのグラフィックボードでもVRAM512MB以上搭載しているものが増えた現在では、ハードルは低くなったといえる。

そのためにQuake4のPoint Release 1.3以降にはこれらのダイナミックライティングを使わずに、アンビエントライティングという単一光源を使うという設定が付け加えられた。これによって陰に関する計算を短縮出来るために大幅な画質低下を代償とするが、大幅なパフォーマンス改善が出来るようになっている。

ゲームプレイ上の特徴として、[ヒットボックス](https://ja.wikipedia.org/wiki/ヒットボックス "wikilink")を採用せず、ポリゴン毎に当たり判定を設定するという物を採用し、よりリアルな戦闘を楽しめるようになっている（ただしマルチプレーでは当たり判定の処理が複雑になるのを防ぐため、今まで通りヒットボックスを採用）。

ネットコードが1フレーム1送信となり、サーバーとクライアント側で完全同期を計る（Source EngineならTick Rate100、QuakeIIIエンジンならsv_fps "125"設定）という形になったが、これがパケットロスやクライアントPCの処理落ち、サーバーPCの処理落ちなどに非常に弱いという弱点を持ってしまった（逆にそれらのないLAN対戦では完全な形で移動を可能にしている）。またトラフィックの影響とこのシステムの関係で、Quake4のポイントリリース1.4βまで最大フレームレートを60に制限せざるを得なかった。

### 採用ゲーム

  - [DOOM3](https://ja.wikipedia.org/wiki/DOOM3 "wikilink")
  - [Quake4](https://ja.wikipedia.org/wiki/Quake4 "wikilink")
  - [Enemy Territory: Quake Wars](../Page/Enemy_Territory:_Quake_Wars.md "wikilink")
  - [Prey](../Page/Prey.md "wikilink")

## 関連項目

  - [id Software](https://ja.wikipedia.org/wiki/id_Software "wikilink")

## 外部リンク

  - [Unofficial Quake Engine](http://www.quake-engine.com/default.aspx)

[Category:ゲームエンジン](https://ja.wikipedia.org/wiki/Category:ゲームエンジン "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")