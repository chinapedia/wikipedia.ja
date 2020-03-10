> この記事は[OpenEXR](https://ja.wikipedia.org/wiki/OpenEXR)から翻訳されています。


**OpenEXR**（オープンイーエックスアール）は[ハイダイナミックレンジイメージ](https://ja.wikipedia.org/wiki/ハイダイナミックレンジイメージ "wikilink") (High-Dynamic-Range Image, HDRI) のための[画像](../Page/画像.md "wikilink")[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")で、[インダストリアル・ライト&マジック](https://ja.wikipedia.org/wiki/インダストリアル・ライト&マジック "wikilink") (ILM) によって作成された[ソフトウェアツール](https://ja.wikipedia.org/wiki/ソフトウェアツール "wikilink")の集合とともに、[オープン標準](https://ja.wikipedia.org/wiki/オープン標準 "wikilink")としてリリースされた。

OpenEXRは、[Artizen HDR](https://ja.wikipedia.org/wiki/Artizen_HDR "wikilink")、[オートデスク](https://ja.wikipedia.org/wiki/オートデスク "wikilink")の[Combustion](https://ja.wikipedia.org/wiki/Combustion "wikilink")、[Lustre](https://ja.wikipedia.org/wiki/Lustre "wikilink")、[Flame](https://ja.wikipedia.org/wiki/Flame "wikilink")、[smoke](https://ja.wikipedia.org/wiki/smoke "wikilink")、[Toxik](https://ja.wikipedia.org/wiki/Toxik "wikilink")、[Blender](../Page/Blender.md "wikilink")、[CinePaint](https://ja.wikipedia.org/wiki/CinePaint "wikilink")、[Houdini](https://ja.wikipedia.org/wiki/Houdini "wikilink")、[LightWave](../Page/LightWave.md "wikilink")、[modo](https://ja.wikipedia.org/wiki/modo "wikilink")、[After Effects](https://ja.wikipedia.org/wiki/After_Effects "wikilink") 7 Professional、[Mental Ray](https://ja.wikipedia.org/wiki/Mental_Ray "wikilink")、[PRMan](https://ja.wikipedia.org/wiki/PRMan "wikilink")、[Digital Fusion](https://ja.wikipedia.org/wiki/Digital_Fusion "wikilink")、[Nuke](https://ja.wikipedia.org/wiki/Nuke "wikilink")、[Shake](https://ja.wikipedia.org/wiki/Shake "wikilink")、[Photoshop](https://ja.wikipedia.org/wiki/Photoshop "wikilink") CS2、Pixel Image Editor、Filmlight Baselight、[Digital Vision](https://ja.wikipedia.org/wiki/Digital_Vision "wikilink") [Nucoda](https://ja.wikipedia.org/wiki/Nucoda "wikilink")、[Blackmagic Design](https://ja.wikipedia.org/wiki/ブラックマジックデザイン "wikilink") [DaVinci Resolveなどでサポートされている](https://ja.wikipedia.org/wiki/DaVinci_Resolve "wikilink")。

HDRデータの[可逆圧縮](../Page/可逆圧縮.md "wikilink")もサポートされている。

## 概要

OpenEXRの技術全容に関しては、ウェブサイト「OpenEXR.org」にて公開されている技術紹介を参照のこと。

OpenEXR、または単にEXRは、ILMによって開発されたラスターフォーマットであり、[VFX](../Page/VFX.md "wikilink")とアニメーション、両方のCG業界で非常に幅広く使用されている。

マルチ解像度と任意チャンネルのフォーマットのサポートが、OpenEXRを画像合成分野において魅力的なものにしている。OpenEXRは合成プロセスにおけるいくつかの苦痛な要素を軽減してくれる。OpenEXRはスペキュラー・ディフーズ・アルファ・RGB・ノーマル・その他様々なチャンネルをひとつのファイルに格納できるので、これらの情報を別々のファイルに保存する必要がない。またこの複数チャンネルの概念により、最終画像に前述のデータを「焼き込む」（bakeする）必要性が低減される。例えば、もしコンポジターが現在のスペキュラーレベルに不満を感じていた場合、後から特定のチャンネルを調整することで不満を解消できる。

OpenEXRの単純な[APIにより](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、ツール開発が容易になる。複数のプロダクションのパイプラインが同じであることなどないので、プロダクションのプロセスにおける問題を解決するカスタム・ツールがいつも必要とされてきた。これらのツールは、ある種の画像操作の問題に対処するためのものであることがこれまで何度も求められ続けてきた。OpenEXRのライブラリにより、膨大なヘッダー情報を管理しなければならないという苦痛が軽減され、タイルやチャンネルといった画像の属性に素早く簡単にアクセスすることが可能となる。

### 歴史

OpenEXRは[1999年](../Page/1999年.md "wikilink")にILMで生まれ、[2003年](../Page/2003年.md "wikilink")に公開された。

## 半精度浮動小数点数のサポート

OpenEXRは16ビットの[半精度浮動小数点数](https://ja.wikipedia.org/wiki/半精度浮動小数点数 "wikilink") (FP16) をサポートしている。32ビットの[単精度浮動小数点数](https://ja.wikipedia.org/wiki/単精度浮動小数点数 "wikilink") (FP32) と比べて表現可能な値の範囲（精度）は劣るが、[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")のHDR (High-Dynamic-Range) レンダリングには必要十分な精度を持ち、データ量を削減できるフォーマットとして採用されるケースが多い。OpenEXRのライブラリでは、`half`型として[C++](../Page/C++.md "wikilink")向けのクラスが提供されている\[1\]。

[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")が開発した[Cg言語においてサポートされている組み込み型のひとつ](../Page/Cg_\(プログラミング言語\).md "wikilink")`half`型は、OpenEXRの半精度浮動小数点数と互換性がある\[2\]。なお、FP16は[OpenGL](../Page/OpenGL.md "wikilink")や[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")でも[テクスチャフォーマットのひとつとしてサポートされている](https://ja.wikipedia.org/wiki/テクスチャマッピング "wikilink")。

## OpenEXRを使用した開発

## 脚注

## 関連項目

  - [ハイダイナミックレンジ合成](../Page/ハイダイナミックレンジ合成.md "wikilink")
  - [ハイダイナミックレンジイメージ](https://ja.wikipedia.org/wiki/ハイダイナミックレンジイメージ "wikilink")
  - [インダストリアル・ライト&マジック](https://ja.wikipedia.org/wiki/インダストリアル・ライト&マジック "wikilink")

## 外部リンク

  - [OpenEXR.com](http://www.openexr.com/)
  - [OpenEXR Documentation](http://www.openexr.com/documentation.html)
  - [OpenEXR Samples](http://www.openexr.com/samples.html)
  - [exrtools](http://scanline.ca/exrtools/)
  - [HDRSource HDR and OpenEXR Libraries](http://www.hdrsource.com/)
  - [(PDF)](http://www.openexr.com/TechnicalIntroduction.pdf)
  - [(PDF)](http://www.openexr.com/ReadingAndWritingImageFiles.pdf)

[Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.  [openexr/half.h at master · AcademySoftwareFoundation/openexr](https://github.com/AcademySoftwareFoundation/openexr/blob/master/IlmBase/Half/half.h)
2.  [3ds Max 2015 Help ヘルプ: OpenEXR ファイル](http://help.autodesk.com/view/3DSMAX/2015/JPN/?guid=GUID-F9274D48-77CA-435F-A604-6DD969FFCA6C)