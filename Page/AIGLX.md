> この記事は[AIGLX](https://ja.wikipedia.org/wiki/AIGLX)から翻訳されています。


[Linux_graphics_drivers_DRI_current.svg](https://ja.wikipedia.org/wiki/File:Linux_graphics_drivers_DRI_current.svg "fig:Linux_graphics_drivers_DRI_current.svg") and **AIGLX** versus [direct rendering](https://ja.wikipedia.org/wiki/Direct_Rendering_Infrastructure "wikilink").\]\] [thumbとAIGLXの組合せによるデスクトップの回転中の画面](https://ja.wikipedia.org/wiki/ファイル:Fedora-Core-6-AIGLX.png "wikilink")\]\] **AIGLX**（Accelerated Indirect GLX）は[X.Org Foundationおよび](../Page/X.Org_Foundation.md "wikilink")[Fedora](../Page/Fedora.md "wikilink")のコミュニティによって開始された[オープンソース](../Page/オープンソース.md "wikilink")のプロジェクトである。3D[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")を実現する技術として知られているが、これは、もともと[シリコングラフィックス](../Page/シリコングラフィックス.md "wikilink")が90年代に開発したXサーバの[GLX](../Page/GLX.md "wikilink")拡張を、最近の[ビデオカード](../Page/ビデオカード.md "wikilink")が持つグラフィックアクセラレーションや[DRIにより高速化するものである](https://ja.wikipedia.org/wiki/ダイレクト・レンダリング・インフラストラクチャ "wikilink")。

## Xglとの関係

両者ともに3D[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")を実現することを念頭に開発されたという経緯があるため、同様の技術として見られることが多いが、実際には全く異なる設計に基づいている。

[Xgl](../Page/Xgl.md "wikilink")は[Xnest](../Page/Xnest.md "wikilink")のように他のXサーバの上で動き、[OpenGL](../Page/OpenGL.md "wikilink")のAPIを通じて可能な限り高速に2D描画および[GLX](../Page/GLX.md "wikilink")の処理を行うよう設計されている新しいXサーバであるが、AIGLXは、あくまでXサーバの拡張モジュールであり、従来からある[GLX](../Page/GLX.md "wikilink")を高速化し、3D[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")の実現のために、いくつかの機能要件を満たすよう拡張したものに過ぎない。したがって、技術として競合するものではなく、事実としてプロジェクト間でコードの交換をしたり、互換性を保つような協調作業が行われてきた。その結果、[Xgl](../Page/Xgl.md "wikilink")の最初の[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")である[Compiz](../Page/Compiz.md "wikilink")もAIGLX上で動作するようになった。

## 利用できる環境

[X11R7.1でサポートされている](../Page/X_Window_System.md "wikilink")。[GLX](../Page/GLX.md "wikilink")とは「Open**GL** Extension to the **X** Window System」の略語で、[X Window System上でOpenGLを実行する技術である](../Page/X_Window_System.md "wikilink")。

## プロプライエタリなドライバとAIGLX

[NVIDIA](../Page/NVIDIA.md "wikilink")や[ATI](https://ja.wikipedia.org/wiki/ATI "wikilink")などの[プロプライエタリな](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[ドライバはもともと独自にGLXを高速に描画するためのバックエンドを持っており](../Page/デバイスドライバ.md "wikilink")、すでにXサーバと共にインストールされているGLX拡張モジュールを置き換える形で機能するようになっている。一方、AIGLXは[XFree86](../Page/XFree86.md "wikilink")では[Mesaにより実装されていた](../Page/Mesa_3D.md "wikilink")[GLX](../Page/GLX.md "wikilink")を、より[Mesaの持つグラフィックアクセラレーション機構を活用できるように改良したものである](../Page/Mesa_3D.md "wikilink")。

[Compiz](../Page/Compiz.md "wikilink")などの[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")は視覚効果を実現するのに、texture_from_pixmapと呼ばれるOpenGL拡張に依存している。当初この拡張は[Mesaでしか実装されておらず](../Page/Mesa_3D.md "wikilink")、[プロプライエタリな](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[ドライバと共に](../Page/デバイスドライバ.md "wikilink")3D[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")を利用するには、ベンダーの対応を待つ必要があった。NVIDIAは2006年9月にリリースした9000シリーズ以降のドライバでこの拡張に対応している。

また、以上のような理由から、AIGLXをサポートしない古いXサーバ上でも、利用するアプリケーションの要求を満たすベンダ製のドライバを使うことで、AIGLXとほぼ同等の環境を実現することができる。

## 関連項目

  - [X Window System](../Page/X_Window_System.md "wikilink")
  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [Xgl](../Page/Xgl.md "wikilink")
  - [Compiz](../Page/Compiz.md "wikilink")
  - [Beryl](../Page/Beryl.md "wikilink")

## 外部リンク

  - [Fedora Project Wiki AIGLX Article](http://fedoraproject.org/wiki/RenderingProject/aiglx)（[英語](../Page/英語.md "wikilink")）
  - [Accelerated X flame wars\!—Maybe not](http://www.freesoftwaremagazine.com/articles/accelerated_x) — AIGLXとXglの違いについて解説した記事（英語）
  - [Installing AiglxOnFedora](http://fedoraproject.org/wiki/RenderingProject/AiglxOnFedora) Fedora Core 5へのAIGLXのインストールHOWTO（英語）

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")