> この記事は[RenderMan](https://ja.wikipedia.org/wiki/RenderMan)から翻訳されています。


**RenderMan**（**レンダーマン**、旧PhotoRealistic RenderMan）は[ピクサー・アニメーション・スタジオ](https://ja.wikipedia.org/wiki/ピクサー・アニメーション・スタジオ "wikilink")によって開発された[レンダリング用のソフトの一群](../Page/レンダリング_\(コンピュータ\).md "wikilink")。

ピクサーは1986年、[ルーカスフィルム](../Page/ルーカスフィルム.md "wikilink")のコンピュータ・アニメーション部門を[スティーブ・ジョブズ](../Page/スティーブ・ジョブズ.md "wikilink")（[アップルの前CEO](../Page/アップル_\(企業\).md "wikilink")、アップルコンピュータ創業者の一人）らが買収して設立した会社であるが、RenderMan自体の開発はピクサー設立前から[コンピュータグラフィック](https://ja.wikipedia.org/wiki/コンピュータグラフィック "wikilink") (CG) 研究者である[エドウィン・キャットマル](../Page/エドウィン・キャットマル.md "wikilink")らによってなされていた。

元々の構想は、CG業界の標準となるレンダリング・[インタフェース言語の構築であり](../Page/インタフェース_\(情報技術\).md "wikilink")、その[シェーディング言語](https://ja.wikipedia.org/wiki/シェーディング言語 "wikilink")のフォーマットそのものがRenderManと呼ばれていた。その後、ピクサー・イメージ・コンピュータ (PIC) というピクサーが販売していた画像処理専用の高性能コンピュータ（スティーブ・ジョブズによると「顧客はある政府機関」）に搭載されていたレンダリングシステム「Reyes」を、RIB (RenderMan Interface Bytestream) フォーマットへの対応を中心に改良した物が「PhotoRealistic (PR) RenderMan」として商品化され、『[アビス](../Page/アビス.md "wikilink")』『[ターミネーター2](../Page/ターミネーター2.md "wikilink")』で使用された事で注目を浴びた。2005年には[Maya](../Page/Maya.md "wikilink")の[プラグイン](../Page/プラグイン.md "wikilink")として機能するRenderMan for Mayaが発売され、[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")による設定が可能になった。

現在も技術更新が継続されており、フォトリアリスティックな[3DCGを制作する上で役立つことから](../Page/3次元コンピュータグラフィックス.md "wikilink")、ピクサーのCGアニメーション作品は勿論の事、『[ジュラシック・パーク](../Page/ジュラシック・パーク.md "wikilink")』、『[スター・ウォーズ](https://ja.wikipedia.org/wiki/スター・ウォーズ "wikilink")』、『[ロード・オブ・ザ・リング](../Page/ロード・オブ・ザ・リング.md "wikilink")』などの[ハリウッド](../Page/ハリウッド.md "wikilink")による[VFX](../Page/VFX.md "wikilink")では不可欠なレンダリングツールの[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となって、随所で頻繁に使用されている。

この結果、映画産業への多大な技術的貢献が評価され、開発者のキャットマルらには[アカデミー賞](../Page/アカデミー賞.md "wikilink")が授与された\[1\]。

ピクサーが[ディズニー](https://ja.wikipedia.org/wiki/ディズニー "wikilink")に買収されたことによって、現在RenderManはディズニーの資産である。

## 対応アプリケーション

  - 公式
      - Maya\[2\] (RenderMan for Maya、旧RenderMan Studio←MTOR\[3\])
      - KATANA (RenderMan for KATANA)\[4\]
      - Houdini (RenderMan for Houdini)\[5\]\[6\]
  - [サードパーティー](../Page/サードパーティー.md "wikilink")（RenderMan 22以降対応）
      - Metasequoia\[7\]

### 過去の対応アプリケーション

#### RenderMan 21.x以前

RenderMan 22でライブレンダリングのためのインターフェースが旧来のRIB形式から新しいRILEYインターフェースへと変更され\[8\]\[9\]、商用顧客を優先するためとしてBlenderへの対応を後回しとした\[10\]。

  - 公式
      - Blender (RenderMan for Blender) - オープンソース。Pixarとコミュニティが共同で開発していた\[11\]。

#### RenderMan 20以前

昔はREYESレンダリング/RSLシェーダーのRenderMan仕様がVFX業界におけるレンダリングの[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")（事実上の標準）となっていたが、その後、モダンパストレーシングレンダラー/OSLシェーダーにとって代わられたため、RenderMan 20以前のREYESモードのみにしか対応していない[サードパーティー](../Page/サードパーティー.md "wikilink")製ソフトウェアも多い。

  - サードパーティー
      - NukeX/NukeStudio (PrmanRenderノード)\[12\]
  - サードパーティー (廃止)
      - Gaffer\[13\] (GafferRenderMan、廃止<ref>[Remove GafferRenderMan](https://github.com/GafferHQ/gaffer/commit/10875065e21370ee9ede5a7ef3b5799f4e3e4207)

`Image Engine Design 2017年9月22日`</ref>`)`

  -   - Cinema 4D\[14\] (Cineman、廃止\[15\])

  - サードパーティー (不明)

      - Silo
      - Ayam\[16\]
      - [AC3D](https://ja.wikipedia.org/wiki/AC3D "wikilink")\[17\]
      - solidThinking\[18\]
      - [K-3D](https://ja.wikipedia.org/wiki/K-3D "wikilink")\[19\]
      - [Wings 3D](https://ja.wikipedia.org/wiki/Wings_3D "wikilink")\[20\]
      - [Poser](../Page/Poser.md "wikilink")\[21\]

また、過去には、Power Animator用のATORプラグイン (Pixar)、Maya用のMayaManプラグイン (Animal Logic) やLiquidプラグイン（[オープンソース](../Page/オープンソース.md "wikilink")）、Rhinoceros用のRhinoManプラグイン (Brian Perry)、Lightwave用のLightManプラグイン (Timm Dapper)、3ds Max用のMaxManプラグイン (Animal Logic) やPaxRendusプラグイン (Archonus)、Softimage用のSoftManプラグイン (Animal Logic)、Poser用のPoserManなども存在していた。

## 互換レンダラー (RenderMan 20以前)

古くよりRenderManの仕様がとして公開されていたため、RenderManには多くの互換レンダーが存在した。しかし、PixarがRenderMan 21で旧来のRenderManの仕様であったREYESレンダリング及びRSLシェーダー言語を廃止したため、現在はこれら互換レンダラーとの互換性が低くなっている。RenderMan 20以前の互換レンダラーとして、SiTex GraphicsのAIRが現存している。

過去には、DGS Renderer（Digital Arts製）、SunART（[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")製）、[JrMan](https://ja.wikipedia.org/wiki/JrMan "wikilink") ([GPL](../Page/GNU_General_Public_License.md "wikilink"))、[Pixie](https://ja.wikipedia.org/wiki/Pixie_\(ソフトウェア\) "wikilink") ([LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink"))、Angel（Ian Stephenson作、無料）、[Aqsis](https://ja.wikipedia.org/wiki/Aqsis "wikilink")（[BSDライセンス](../Page/BSDライセンス.md "wikilink")）、RenderDotC (Dot C Software製)、[BMRT](https://ja.wikipedia.org/wiki/Blue_Moon_Rendering_Tools "wikilink")/Entropy (後のNVIDIA [Gelato](https://ja.wikipedia.org/wiki/Gelato_\(ソフトウェア\) "wikilink"))、[3Delight](https://ja.wikipedia.org/wiki/3Delight "wikilink") 12以前などの互換レンダラーも存在した\[22\]。なお、過去にPixarは、互換レンダラーの一つであるEntropyの開発元Exluna社を、RenderManの特許侵害等で訴え、販売差し止めにしている ([Blue Moon Rendering Tools参照](https://ja.wikipedia.org/wiki/Blue_Moon_Rendering_Tools "wikilink"))。

その他、変換ツールを使用することでRenderManとの互換性を確保したレンダラーも存在する。[NVIDIA](../Page/NVIDIA.md "wikilink")のGelatoは別途提供されたRibelato及びrsl2gslを用いることでRenderManとの互換性を確保していた\[23\]\[24\]。また、Side Effects Softwareの[Houdini](../Page/Houdini.md "wikilink")に搭載されているMantraレンダラーは、独自のVEX言語がRSLに近いほか、rmands / slo2otl.pyを通すことでRenderManとのシェーダーバイナリの互換性を確保していた\[25\]\[26\] (なお、Houdiniはsdl2otl.pyを通すことで3Delightとのシェーダーバイナリ互換性も確保している\[27\])。

なお、互換レンダラーであっても、コマンド名やコンパイル済みシェーダーの拡張子は衝突しないように異なったものとなっている。

<table>
<thead>
<tr class="header">
<th><p>レンダラー</p></th>
<th><p>公式対応ソフトウェア</p></th>
<th><p>レンダリング<br />
コマンド</p></th>
<th><p>対応シーン形式[28]</p></th>
<th><p>シェーダー<br />
コンパイラ</p></th>
<th><p>対応シェーダー[29]</p></th>
<th><p>シェーダーバイナリの拡張子</p></th>
<th><p>MIPMAP生成プログラム</p></th>
<th><p>フレームバッファー/フリップブック</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RenderMan 20以前互換レンダラー</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RenderMan 20以前<br />
（REYESモード）[30]</p></td>
<td><p>Maya[31][32][33]</p></td>
<td><p>'prman'[34]</p></td>
<td><p>RIB</p></td>
<td><p>'shader'[35]</p></td>
<td><p>RSL (.sl)</p></td>
<td><p>.slo[36][37]</p></td>
<td><p>'txmake'[38]</p></td>
<td><p>'it'[39]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/3Delight" title="wikilink">3Delight</a> 12以前<br />
（RSLモード）</p></td>
<td><p>Maya、3ds Max、Katana、DAZ Studio（搭載）、Softimage（廃止）[40][41][42]</p></td>
<td><p>'renderdl'[43]</p></td>
<td><p>RIB</p></td>
<td><p>'shaderdl'[44]</p></td>
<td><p>RSL (.sl)</p></td>
<td><p>.sdl[45][46]</p></td>
<td><p>'tdlmake'[47]</p></td>
<td><p>'i-display'[48]</p></td>
</tr>
<tr class="even">
<td><p>AIR</p></td>
<td><p>Maya[49][50]、<a href="../Page/Rhinoceros_3D.md" title="wikilink">Rhinoceros 3D</a>[51][52]、Houdini[53][54]、Massive[55]</p></td>
<td><p>'air'[56]</p></td>
<td><p>RIB</p></td>
<td><p>'shaded'[57]</p></td>
<td><p>RSL (.sl)</p></td>
<td><p>.slb[58]</p></td>
<td><p>'mktex'[59]</p></td>
<td><p>'airshow'[60]</p></td>
</tr>
<tr class="odd">
<td><p>Angel</p></td>
<td></td>
<td><p>'angel'[61]</p></td>
<td><p>RIB</p></td>
<td><p>'giles'[62]</p></td>
<td><p>RSL (.sl)</p></td>
<td><p>.slc[63]</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Aqsis" title="wikilink">Aqsis</a></p></td>
<td><p>Blender[64]</p></td>
<td><p>'aqsis'[65]</p></td>
<td><p>RIB</p></td>
<td><p>'aqsl'[66]</p></td>
<td><p>RSL (.sl)</p></td>
<td><p>.slx[67][68]</p></td>
<td><p>'teqser'[69]</p></td>
<td><p>'piqsl'[70]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Blue_Moon_Rendering_Tools" title="wikilink">BMRT</a></p></td>
<td></td>
<td><p>'rendrib'[71]</p></td>
<td><p>RIB</p></td>
<td><p>'slc'[72]</p></td>
<td><p>RSL (.sl)</p></td>
<td><p>.slc[73]</p></td>
<td><p>'mkmip'[74]</p></td>
<td><p>'iv'[75]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Blue_Moon_Rendering_Tools" title="wikilink">Entropy</a></p></td>
<td></td>
<td><p>'entropy'</p></td>
<td><p>RIB</p></td>
<td><p>'sle'</p></td>
<td><p>RSL (.sl)</p></td>
<td><p>.sle</p></td>
<td><p>'mkmip'</p></td>
<td><p>{{?}}</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Pixie_(ソフトウェア)" title="wikilink">Pixie</a></p></td>
<td></td>
<td><p>'rndr'[76]</p></td>
<td><p>RIB</p></td>
<td><p>'sdrc'[77]</p></td>
<td><p>RSL (.sl)</p></td>
<td><p>.sdr[78]</p></td>
<td><p>'texmake'[79]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>RenderDotC</p></td>
<td></td>
<td><p>'renderdc'[80]</p></td>
<td><p>RIB</p></td>
<td><p>'shaderdc'[81]</p></td>
<td><p>RSL (.sl)</p></td>
<td><p>.so/.dll[82]</p></td>
<td><p>'texdc'[83]</p></td>
<td><p>{{?}}</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/JrMan" title="wikilink">JrMan</a></p></td>
<td></td>
<td><p>'jrman'</p></td>
<td><p>RIB</p></td>
<td></td>
<td><p>RSL (.sl)</p></td>
<td></td>
<td><p>'mktxr'</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Houdini.md" title="wikilink">Houdini</a> Mantra<br />
(Micropolygonモード)</p></td>
<td><p>Houdini (搭載)</p></td>
<td><p>'mantra'</p></td>
<td><p>bgeo[84]、RIB[85][86]等</p></td>
<td><p>'vcc'[87]</p></td>
<td><p>VEX (.vfl)[88]、RSL (.sl)[89]</p></td>
<td><p>.otl</p></td>
<td><p>'icp'[90]</p></td>
<td><p>'mplay'[91]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Gelato_(ソフトウェア)" title="wikilink">NVIDIA Gelato</a></p></td>
<td><p>Maya[92]、3ds Max[93][94]</p></td>
<td><p>'gelato'</p></td>
<td><p>Pyg[95][96]、RIB (Ribelato経由)</p></td>
<td><p>'gslc'[97]</p></td>
<td><p>GSL (.gsl)、<br />
RSL (.sl、rsl2gsl経由)</p></td>
<td><p>.gso[98]</p></td>
<td><p>'maketx'[99]</p></td>
<td><p>'iv'[100]</p></td>
</tr>
<tr class="even">
<td><p>RIB及びOSL対応レンダラー</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RenderMan<br />
（旧RISモード）</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/#対応アプリケーション" title="wikilink">#対応アプリケーション</a>参照</p></td>
<td><p>'prman'</p></td>
<td><p>RIB</p></td>
<td><p>'oslc'[101]</p></td>
<td><p>OSL (.osl)[102]</p></td>
<td><p>.oso[103]</p></td>
<td><p>'txmake'</p></td>
<td><p>'it'</p></td>
</tr>
<tr class="even">
<td><p>3Delight 12以前<br />
（OSLモード）</p></td>
<td><p>RSLモードの項を参照</p></td>
<td><p>'renderdl'[104]</p></td>
<td><p>RIB[105]</p></td>
<td><p>'oslc'</p></td>
<td><p>OSL (.osl)[106]</p></td>
<td><p>.oso</p></td>
<td><p>'tdlmake'[107]</p></td>
<td><p>'i-display'[108]</p></td>
</tr>
<tr class="odd">
<td><p>RenderMan非互換レンダラー (参考)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Mental_ray" title="wikilink">NVIDIA Mental Ray</a></p></td>
<td><p>Maya（過去に搭載）、3ds Max（過去に搭載）、Softimage（搭載）など</p></td>
<td><p>'ray'</p></td>
<td><p>MI[109]</p></td>
<td><p>'ray -mslc'（廃止）[110]</p></td>
<td><p>MetaSL (.msl/.xmsl)[111]</p></td>
<td><p>.so/.dll[112]</p></td>
<td><p>'imf_copy'[113]</p></td>
<td><p>'imf_disp'[114]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Arnold_(ソフトウェア)" title="wikilink">Arnold</a></p></td>
<td><p>Maya（搭載）、3ds Max（搭載）など</p></td>
<td><p>'kick'[115]</p></td>
<td><p>ASS[116]</p></td>
<td><p>'oslc'<ref name="arnold-osl"><a href="https://support.solidangle.com/display/A5ARP/OSL+Shaders">OSL Shaders</a></p>
<p><code>Solid Angle</code></ref></p></td>
<td><p>OSL (.osl)[117]</p></td>
<td><p>.oso[118]</p></td>
<td><p>'maketx'[119]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3Delight<sup>NSI</sup>[120]</p></td>
<td><p>Maya、Katana</p></td>
<td><p>'renderdl'[121][122]</p></td>
<td><p>NSI[123]、USD (HydraNSI経由[124])</p></td>
<td><p>'oslc'[125]</p></td>
<td><p>OSL (.osl)[126]</p></td>
<td><p>.oso</p></td>
<td><p>'tdlmake'[127][128]</p></td>
<td><p>'i-display'[129]</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<references group="n"/>

### RSLシェーダー構築ツール

RenderManのMaya版にはRSLシェーダー構築ツールのSLIMが付属していた\[130\]。互換レンダラーでは、AIRレンダラーがVshadeを付属していた\[131\]。その他、単体のRSL構築ツールとしては、ShaderManやShrimpが存在した\[132\]。

## 関連項目

  - [エドウィン・キャットマル](../Page/エドウィン・キャットマル.md "wikilink")
  - [ピクサー・アニメーション・スタジオ](https://ja.wikipedia.org/wiki/ピクサー・アニメーション・スタジオ "wikilink")
  - [アカデミー賞](../Page/アカデミー賞.md "wikilink")
  - [ディズニー](https://ja.wikipedia.org/wiki/ディズニー "wikilink")
  - [コンピュータアニメーション](https://ja.wikipedia.org/wiki/コンピュータアニメーション "wikilink")
  - [3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")
  - [シェーダー](../Page/シェーダー.md "wikilink")
  - [シェーディング言語](https://ja.wikipedia.org/wiki/シェーディング言語 "wikilink")

## 脚注

## 外部リンク

  - [レンダーマン（ピクサー・アニメーション・スタジオ）](https://renderman.pixar.com/)

[Category:3DCGソフトウェア](https://ja.wikipedia.org/wiki/Category:3DCGソフトウェア "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink")

1.  [Awards](http://renderman.pixar.com/view/renderman-awards)
2.  [RenderMan for Maya](https://renderman.pixar.com/view/renderman4maya) Pixar
3.  [RenderMan Studio 2.0](http://renderman.pixar.com/resources/current/RenderMan/renderManStudio2.0.html) PIXAR
4.  [RenderMan for KATANA](https://renderman.pixar.com/view/renderman4katana) Pixar
5.  [RenderMan for Houdini](https://renderman.pixar.com/view/renderman4houdini) Pixar
6.  [Rendering with RenderMan](http://www.sidefx.com/docs/houdini15.0/render/renderman) Side Effects Software
7.  [バージョンアップ履歴](http://www.metaseq.net/jp/release_note.html) tetraface
8.
9.  [Look At RenderMan 22 and beyond](https://www.fxguide.com/featured/look-at-renderman-22-and-beyond/) fxguide 2018年5月2日
10. [General FAQ](https://renderman.pixar.com/general-faq) Pixar
11. [RenderMan for Blender](http://web.archive.org/web/20170310225800/https://renderman.pixar.com/view/renderman4blender) Pixar
12. [PrmanRender](http://help.thefoundry.co.uk/nuke/content/reference_guide/3d_nodes/prmanrender.html) Foundry
13. [Gaffer User Guide](http://web.archive.org/web/20160817015054/http://imageengine.github.io/gaffer/resources/documents/0.79.0/GafferUserGuide.pdf) [イメージエンジン](https://ja.wikipedia.org/wiki/イメージエンジン "wikilink")
14. [レンダリング - 究極のフォトリアリズムのために](http://web.archive.org/web/20170601155109/http://www.maxon.net/ja/products/cinema-4d-visualize/rendering.html) MAXON
15. [Modernizing and Moving Forward](https://www.maxon.net/en/news/maxon-blog/article/modernizing-and-moving-forward/) Maxon 2017年12月5日
16. [Links - RenderMan-compliant Modelers](http://www.dotcsw.com/links.html#modelers) Dot C Software
17.
18.
19.
20.
21.
22. [Links - RenderMan-compliant Renderers](http://www.dotcsw.com/links.html#renderers) Dot C Software
23. [Renderman FAQ](http://www.faqs.org/faqs/comp.graphics.rendering.renderman/RenderMan_FAQ_-_monthly_posting/) Larry Gritz
24. [NVIDIA Gelato Download](http://www.nvidia.co.uk/page/gelato_download.html) NVIDIA
25. 『Houdini On the Spot: Power User Tips and Techniques』 P.169 Craig Zerouni 2007年8月20日 ISBN 978-0240808628
26. [Rendering with RenderMan](http://www.sidefx.com/docs/houdini15.0/render/renderman) Side Effects Software
27.
28. 原則的にC++などの汎用プログラミング言語を除く
29.
30. 旧PhotoRealistic RenderMan (PRMan)
31. HoudiniやCinema 4D (Cineman) などで使うこともできた
32.
33.
34. 『Essential RenderMan』 Second Edition P.20 Ian Stephenson 2007年 ISBN 978-1846283444
35. 『Essential RenderMan』 Second Edition P.132 Ian Stephenson 2007年 ISBN 978-1846283444
36.
37.
38. [Manual page for TXMAKE(1)](https://renderman.pixar.com/resources/current/RenderMan/txmake.1.html) Pixar
39. ["it"](http://web.archive.org/web/20160120074306/https://renderman.pixar.com/resources/current/RenderMan/itFeatures.html) Pixar
40. HoudiniやCinema 4D (Cineman)やBlender (3Delight/Blenderアドオン)などで使うこともできる
41.
42.
43.
44.
45.
46.
47. [Optimizing Textures](https://documentation.3delightcloud.com/display/3DSP/Optimizing+Textures) The 3Delight Team
48. [3Delight 11.0 User’s Manual](https://documentation.3delightcloud.com/download/attachments/1376257/3Delight-UserManual.pdf?version=2&modificationDate=1415300631000&api=v2) P.7 The 3Delight Team
49. AIR Stream Maya-to-AIR plug-in
50. [AIR Stream Maya-to-AIR plug-in](http://www.sitexgraphics.com/html/air_stream.html) SiTex Graphics
51. RhinoAirプラグイン
52. [RhinoAir for Rhino 4 & 5](http://www.sitexgraphics.com/html/rhino.html) SiTex Graphics
53. [Houdini and AIR](http://www.sitexgraphics.com/html/houdini_and_air.html) SiTex Graphics
54. [Rendering with RenderMan](http://www.sidefx.com/docs/houdini15.0/render/renderman) Side Effects Software
55. [Massive](http://www.sitexgraphics.com/html/massive.html) SiTex Graphics
56.
57.
58.
59. [AIR User Manual](http://www.sitexgraphics.com/air.pdf) P.387 SiTex Graphics
60. [AIR User Manual](http://www.sitexgraphics.com/air.pdf) P.376 SiTex Graphics
61.
62.
63.
64. RIBMosaicアドオン
65.
66.
67.
68.
69. [Texture Optimizer: teqser](http://www.aqsis.org/documentation/user_manual/part_i/using_tools/texture_optimizer.html) The Aqsis Team
70. [Advanced Framebuffer: piqsl](http://www.aqsis.org/documentation/user_manual/part_i/using_tools/advanced_framebuffer.html) The Aqsis Team
71. 『Essential Renderman fast』 P.20 Ian Stephenson 2003年1月31日 ISBN 978-1852336080
72.
73.
74. [Making tiled TIFF files with mkmip](http://klee.cittastudi.di.unimi.it/~dan/grafica/doc/bmrt/doc/html/node5.html#SECTION00540000000000000000) Exluna, Inc.
75. 『Blue Moon Rendering Tools, User Manual - release 2.6』 P.43 Exluna 2000年
76. [rndr(1) - Linux man page](https://linux.die.net/man/1/rndr)
77. [sdrc(1) - Linux man page](https://linux.die.net/man/1/sdrc)
78.
79. [texmake(1) - Linux man page](http://linux.die.net/man/1/texmake)
80.
81.
82. 『The RenderMan Shading Language Guide』 P.26 Rudy Cortes、Saty Raghavachary 2007年 ISBN 978-1598632866
83. [Textures](http://www.dotcsw.com/doc/programs.html#Textures) Dot C Software
84. [Archive Generator render node](http://www.sidefx.com/docs/houdini/nodes/out/archive.html) Side Effects Software
85. [Delayed Read Archive VOP node](http://www.sidefx.com/docs/houdini/nodes/vop/DelayedReadArchive.html) Side Effects Software
86. 『Houdini On the Spot: Power User Tips and Techniques』 P.170 Craig Zerouni 2007年7月14日 ISBN 978-0240808628
87. 『Houdini On the Spot: Power User Tips and Techniques』 P.199 Craig Zerouni 2007年7月14日 ISBN 978-0240808628
88.
89.
90. [Image file formats](http://www.sidefx.com/docs/houdini15.0/io/formats/image_formats) Side Effects Software
91. [MPlay viewer](http://www.sidefx.com/docs/houdini15.0/mplay/_index) Side Effects Software
92. Mangoプラグイン
93. Amarettoプラグイン（Frantic Films製）
94. [映画業界向けのインタラクティブなライティング・ツール、NVIDIA Sorbetto™を発売](http://www.nvidia.co.jp/object/IO_24524.html) 2005年7月28日 NVIDIA
95. Pythonベース
96. [GelatoR 2.1 Technical Reference](http://film.download.nvidia.com/techref.pdf) P.53 NVIDIA
97. [GelatoR 2.1 Technical Reference](http://film.download.nvidia.com/techref.pdf) P.188-189 NVIDIA
98.
99. [GelatoR 2.1 Technical Reference](http://film.download.nvidia.com/techref.pdf) P.197 NVIDIA
100. [GelatoR 2.1 Technical Reference](http://film.download.nvidia.com/techref.pdf) P.178 NVIDIA
101. [OSL Patterns](https://rmanwiki.pixar.com/display/REN/OSL+Patterns) Pixar
102.
103.
104.
105.
106. [Batch Rendering (OSL)](https://documentation.3delightcloud.com/pages/viewpage.action?pageId=58195980) The 3Delight Team
107.
108.
109. 『Writing mental ray Shaders: A Perceptual Introduction』 P.19-20 Andy Kopra 2008年9月17日 ISBN 978-3211489642
110. [mental ray Release Notes](http://docs.autodesk.com/MENTALRAY/2014/ENU/mental-ray-help/files/relnotes/relnotes.html) Autodesk 2013年9月12日
111.
112. [Using and Writing Shaders](http://docs.autodesk.com/MENTALRAY/2015/ENU/mental-ray-help/files/manual/node99.html) Autodesk
113. [Image Copy: imf_copy](http://docs.autodesk.com/MENTALRAY/2013/JPN/mental-ray-help/files/manual/imf_copy.html) Autodesk
114. [Image Display: imf_disp](http://docs.autodesk.com/MENTALRAY/2013/JPN/mental-ray-help/files/manual/imf_disp.html) Autodesk
115. [Command Line Rendering (kick)](https://support.solidangle.com/pages/viewpage.action?pageId=8390077) Solid Angle
116.
117.
118.
119. [Maketx - Arnold for Maya User Guide](https://support.solidangle.com/display/AFMUG/Maketx) Solid Angle
120. 3Delight 13以降
121. [Rendering NSI file](https://documentation.3delightcloud.com/display/3DSP/Rendering+NSI+file) The 3Delight Team
122.
123.
124. [Company News](http://j-cube.jp/news/) J CUBE
125.
126. [The Nodal Scene Interface](https://documentation.3delightcloud.com/display/NSI/Introduction) The 3Delight Team
127.
128.
129. [Introduction](https://documentation.3delightcloud.com/display/3DSP/Introduction) The 3Delight Team
130. [A Brief Introduction To RenderMan](http://web.archive.org/web/20160829014857/https://renderman.pixar.com/view/brief-introduction-to-renderman) Pixar
131.
132.