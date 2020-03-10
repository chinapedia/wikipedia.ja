> この記事は[ZN-1](https://ja.wikipedia.org/wiki/ZN-1)から翻訳されています。


ZN-1(COH-1002)は[ソニー](../Page/ソニー.md "wikilink") / [ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")が開発した[プレイステーション互換の](https://ja.wikipedia.org/wiki/PlayStation_\(ゲーム機\) "wikilink")[アーケードゲーム基板](../Page/アーケードゲーム基板.md "wikilink")である。プレイステーションの内部構成に加え、アーケードゲーム基板に必要な各種インターフェイスの追加、メインメモリの増設などを行っている。

他社からも同様なプレイステーション互換基板が出ており、[コナミ](https://ja.wikipedia.org/wiki/コナミ "wikilink")[GX700](https://ja.wikipedia.org/wiki/GX700 "wikilink")、[タイトー](https://ja.wikipedia.org/wiki/タイトー "wikilink")[FXシステム](https://ja.wikipedia.org/wiki/FXシステム "wikilink")、[ナムコ](https://ja.wikipedia.org/wiki/ナムコ "wikilink")[SYSTEM10](https://ja.wikipedia.org/wiki/SYSTEM10 "wikilink")などが存在する。また、CPUクロック、メモリ量等を増強した[ZN-2](https://ja.wikipedia.org/wiki/ZN-2 "wikilink")が存在する。

## スペック

[thumb](https://ja.wikipedia.org/wiki/画像:CXD8530CQ_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/画像:CXD8561Q_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/画像:CXD2925Q_01.jpg "wikilink")

  - CPU: [R3000](../Page/R3000.md "wikilink")カスタム 32bit[RISC](../Page/RISC.md "wikilink")
      - [クロック周波数](https://ja.wikipedia.org/wiki/クロック周波数 "wikilink"): 33.8688MHz(ZN-2は50MHz)
      - [メインメモリ](https://ja.wikipedia.org/wiki/メインメモリ "wikilink"): 2MB(ZN-2は2/4/ 8MB)
  - [コプロセッサ](https://ja.wikipedia.org/wiki/コプロセッサ "wikilink"): GTE(ジオメトリエンジン)
      - 演算能力: 最大150万[ポリゴン](../Page/ポリゴン.md "wikilink")/秒
      - 可変長の[固定小数点](https://ja.wikipedia.org/wiki/固定小数点 "wikilink")演算
  - [グラフィック](../Page/グラフィック.md "wikilink"): GPU、VRAM 2MB(ZN-2は2/4/8MB / プレイステーションは1MB)
      - [解像度](https://ja.wikipedia.org/wiki/解像度 "wikilink"): 256ドット×224ライン(ノン[インターレース](https://ja.wikipedia.org/wiki/インターレース "wikilink"))～640ドット×480ライン(インターレース)
      - 色: 最大1677万色
      - 表示画面: 1面
      - [スプライト描画性能](../Page/スプライト_\(映像技術\).md "wikilink"): 最大表示4000個(1/60秒)
      - ポリゴン: 表示能力36万ポリゴン/秒、[テクスチャマッピング](../Page/テクスチャマッピング.md "wikilink")、[グーローシェーディング](https://ja.wikipedia.org/wiki/グーローシェーディング "wikilink")、[半透明](https://ja.wikipedia.org/wiki/半透明 "wikilink")
  - [画像伸張エンジン](https://ja.wikipedia.org/wiki/画像伸張エンジン "wikilink"): MDEC(動画再生エンジン兼テクスチャ展開)
  - [音源チップ](https://ja.wikipedia.org/wiki/音源チップ "wikilink"): [SPU](../Page/SPU.md "wikilink")16bit PCM
      - [メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink"): 512KB
      - [サンプリング周波数](../Page/サンプリング周波数.md "wikilink"): 44kHz
      - 同時発音数: [ステレオ](../Page/ステレオ.md "wikilink")、24[チャンネル](https://ja.wikipedia.org/wiki/チャンネル "wikilink")
      - カプコンタイトルにおいては、PSX SPUは用いず、[QSound](https://ja.wikipedia.org/wiki/QSound "wikilink")チップを用いることもある。

## 構成

  - [JAMMA](https://ja.wikipedia.org/wiki/日本アミューズメントマシン工業協会 "wikilink")56ピンエッジ・コネクタ(電源、サウンド、1PLAYER / 2PLAYERコントローラインターフェイス)
  - 2PLAYER、3PLAYER用コントローラインターフェイス
  - スピーカー端子
  - ビデオ出力端子
  - アナログ入力端子
  - トラックボールインターフェイス
  - メモリカードインターフェイス
  - メインメモリ拡張コネクタ(場合により未実装)
  - 拡張ボード用コネクタ(96ピンコネクタ×2本)
  - 設定内容保存用EEPROM(AT28C16 16kbit)
  - GTE/MPU: CXD8530CQ
  - GPU: CXD8561BQ
  - SPU: CXD2925Q

## サブボード

テクモの[ギャロップレーサー](../Page/ギャロップレーサー.md "wikilink")2では、ZN-1にROMを搭載するためのサブ基板を接続している。このサブボードにはHDLCコントローラ(uPD72103)、Z80(Z084004)、音源(YMZ280B)、音源用D/Aコンバータ(YAC513M)などが搭載可能となっているが、ギャロップレーサー2では未実装となっている。

## 主なタイトル

  - [闘神伝](https://ja.wikipedia.org/wiki/闘神伝 "wikilink")2([カプコン](../Page/カプコン.md "wikilink") / [タカラ](../Page/タカラ_\(玩具メーカー\).md "wikilink"))
  - [ギャロップレーサー](../Page/ギャロップレーサー.md "wikilink")([テクモ](../Page/テクモ.md "wikilink"))
  - [スターグラディエイター](https://ja.wikipedia.org/wiki/スターグラディエイター "wikilink")(カプコン)
  - [ストリートファイターEX](https://ja.wikipedia.org/wiki/ストリートファイターEX "wikilink")(カプコン / [アリカ](../Page/アリカ.md "wikilink"))
  - [私立ジャスティス学園](https://ja.wikipedia.org/wiki/私立ジャスティス学園 "wikilink")(カプコン)
  - [デッド オア アライブ++](https://ja.wikipedia.org/wiki/デッド_オア_アライブ "wikilink")(テクモ)
  - [超鋼戦紀キカイオー](https://ja.wikipedia.org/wiki/超鋼戦紀キカイオー "wikilink")(カプコン)
  - [テトリス ザ・グランドマスター](../Page/テトリス_ザ・グランドマスター.md "wikilink")(カプコン / アリカ)
  - [ストライダー飛竜2](../Page/ストライダー飛竜2.md "wikilink")(カプコン)

[Category:アーケードゲーム基板](https://ja.wikipedia.org/wiki/Category:アーケードゲーム基板 "wikilink")