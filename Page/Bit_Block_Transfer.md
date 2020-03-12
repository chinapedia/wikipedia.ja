> この記事は[Bit Block Transfer](https://ja.wikipedia.org/wiki/Bit_Block_Transfer)から翻訳されています。


**ビットブロック転送**（、ビット・ブロック・トランスファー）は、[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")における[画像](../Page/画像.md "wikilink")データ（[ビットマップ](../Page/ビットマップ画像.md "wikilink")）操作およびそれに関連するハードウェア機能のひとつである。ビットブロック転送の操作には少なくとも2つのビットマップを必要とし、転送の際にビット単位の[論理演算](../Page/論理演算.md "wikilink")（ラスターオペレーション）を伴うこともある 。

**BitBlt** (読みは「**ビットブリット**」) と略されるが、これを[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")やゲームの設定ファイルなどでBitB**i**t（lではなくてi）と表現してしまう間違いも。

## 概要

## ダブルバッファリング

[CPU](../Page/CPU.md "wikilink")から[VRAM](../Page/VRAM.md "wikilink")に対する直接アクセスは[CRTCからのアクセスの干渉などハードウェア的な制約が多いため](../Page/CRTC_\(LSI\).md "wikilink")、[メインメモリに対するアクセスよりも低速であることが多い](../Page/主記憶装置.md "wikilink")。 、画像操作の度に[VRAM](../Page/VRAM.md "wikilink")にアクセスを行うことは描画速度を低下させるばかりか、描画途中で画面の[フレームが切り替わってしまう状況を生じやすく](../Page/コマ_\(映画・漫画\).md "wikilink")、[ちらつき](https://ja.wikipedia.org/wiki/ちらつき "wikilink")（[フリッカー](../Page/フリッカー.md "wikilink")）、、カクつき（[スタッタリング](https://ja.wikipedia.org/wiki/スタッタリング "wikilink")）を発生させる原因となる。これらの問題の解決方法の一つとして、モニターに表示するための表画面となる画像データ領域をVRAMに、そして裏画面となる同サイズのデータ領域をメインメモリに確保しておき、画像操作は裏画面にて行ない、最終的に裏画面のデータを表画面に一括転送するという[ダブルバッファリング](https://ja.wikipedia.org/wiki/ダブルバッファリング "wikilink")手法がある。この転送時にビットブロック転送が利用される。[Windows API](../Page/Windows_API.md "wikilink")（[GDI](../Page/Graphics_Device_Interface.md "wikilink")）におけるBitBlt関数のように、グラフィックスデバイス（グラフィックスチップ、[GPU](../Page/Graphics_Processing_Unit.md "wikilink")）による[ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")機能を備えるものもある。[CPU](../Page/CPU.md "wikilink")の代わりに[DMAコントローラを用いてメインメモリから](../Page/Direct_Memory_Access.md "wikilink")[VRAM](../Page/VRAM.md "wikilink")に[ビットマップを転送するアーキテクチャ](../Page/ビットマップ画像.md "wikilink") も存在する。[Macintosh](../Page/Macintosh.md "wikilink")では「オフスクリーン描画」と呼ぶのが普通で、"Bit Block Transfer"や"BitBlt"という語句はめったに出てこない。

ダブルバッファリングの裏画面用に確保したメモリ領域は**オフスクリーン**、**オフスクリーンバッファ**あるいは**バックバッファ**と呼ぶ。またわかりやすく**仮想画面**と呼ぶこともある。

[Direct3D](../Page/Direct3D.md "wikilink")や[OpenGL](../Page/OpenGL.md "wikilink")などのグラフィックスハードウェアアクセラレーションに対応したAPIを利用してGPU上で画像処理を行なう場合は、メインメモリを介することなくVRAM上で直接画像データを高速に操作できるが、表画面に対する直接操作は依然としてちらつきの問題を生じるため、VRAM上に裏画面を用意しておき、フリップ（スワップ）機能を用いてダブルバッファリングを行なうのが通例である。同様に、メインメモリの一部をVRAMとしてGPUと共用する[オンボードグラフィックス](https://ja.wikipedia.org/wiki/オンボードグラフィックス "wikilink")などの環境であっても、ダブルバッファリングが必要である。

## 逸話

[サムネイル当初は](https://ja.wikipedia.org/wiki/ファイル:Smalltalk-76.png "wikilink")、[PARC](https://ja.wikipedia.org/wiki/PARC "wikilink")で開発された[Alto](../Page/Alto.md "wikilink")向けに開発された[Smalltalk](../Page/Smalltalk.md "wikilink")システムで、ポップアップするメニューやオーバーラップするウインドウを有する[GUIの効率化を図るためにダン](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")・インガルスらにより考案・実装されたものだが、後にマイクロコード化され、Altoの組み込みの機能としてSmalltalk以外のGUIシステムでも広く利用されるようになった。Smalltalkシステムでは、GUIウィジェットの通常描画の他にも、タートルグラフィックス、フォントの複数のスタイル（ボールド、イタリック、アンダーライン、取り消し線）の自動生成、あるいは、描画ツールでドット単位の部分編集を可能にする拡大表示、図形の回転処理などを行なう際などに活用された。なお、1979年時点でのSmalltalkでは隠れたウインドウの見える部分だけの描画更新処理は行なっていなかったのだが、おそらく前述マイクロコード化などのハードウェア支援も手伝って比較的に高速にウインドウ処理をこなすSmalltalkシステムのデモを見た[ビル・アトキンソン](https://ja.wikipedia.org/wiki/ビル・アトキンソン "wikilink")が思い込みで、不定形領域を対象にでき、しかもソフトウェアのみで部分的な再描画を行なっているものと誤解。その認識のまま、後に[アップル製](../Page/アップル_\(企業\).md "wikilink")[Lisaや](../Page/Lisa_\(コンピュータ\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")でGUI描画の中核を担う、“リージョン”の扱いと比較的高速な描画が可能な[QuickDraw](../Page/QuickDraw.md "wikilink")として、ついに完成させてしまったという逸話がある。

## 関連項目

  - [ダブルバッファリング](https://ja.wikipedia.org/wiki/ダブルバッファリング "wikilink")
  - [スプライト](../Page/スプライト_\(映像技術\).md "wikilink")
  - [Direct Memory Access](../Page/Direct_Memory_Access.md "wikilink")
  - [Blit](../Page/Blit.md "wikilink")
  - [コンポジット型ウィンドウマネージャ](https://ja.wikipedia.org/wiki/コンポジット型ウィンドウマネージャ "wikilink")
  - [:en:Bit blit](https://ja.wikipedia.org/wiki/:en:Bit_blit "wikilink")
  - [:en:Multiple buffering](https://ja.wikipedia.org/wiki/:en:Multiple_buffering "wikilink")

[Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink")