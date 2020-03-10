> この記事は[OpenCV](https://ja.wikipedia.org/wiki/OpenCV)から翻訳されています。


**OpenCV**（オープンシーヴィ、）とは[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が開発・公開した[オープンソース](../Page/オープンソース.md "wikilink")の[コンピュータビジョン](../Page/コンピュータビジョン.md "wikilink")向け[ライブラリ](../Page/ライブラリ.md "wikilink")\[1\]。2009年に[Willow Garage](https://ja.wikipedia.org/wiki/Willow_Garage "wikilink")（ウィロー・ガレージ）に開発が移管され、さらにその後[Itseez](https://ja.wikipedia.org/wiki/Itseez "wikilink")にメンテナンスが移管されたが、2016年5月にインテルがItseezを買収することが発表された\[2\]\[3\]。

## 概要

[画像処理](https://ja.wikipedia.org/wiki/画像処理 "wikilink")・画像解析および[機械学習](https://ja.wikipedia.org/wiki/機械学習 "wikilink")等の機能を持つ[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Python](../Page/Python.md "wikilink")、[MATLAB](https://ja.wikipedia.org/wiki/MATLAB "wikilink")用ライブラリ\[4\]。[プラットフォームとして](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[FreeBSD](../Page/FreeBSD.md "wikilink")等全ての[POSIX](../Page/POSIX.md "wikilink")に準拠した[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")[OS](../Page/オペレーティングシステム.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Android](https://ja.wikipedia.org/wiki/Android "wikilink")、[iOS等をサポートしている](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。

## 歴史

1999年にプロジェクト開始。最初のアルファ版が公開されたのは、国際会議CVPR 2000 (IEEE Conference on Computer Vision and Pattern Recognition 2000) である。2001年から2005年の間に5つのベータ版がリリースされた。1.0版がリリースされたのは2006年。

2008年にWillow Garageによるサポートを受け、開発状況が再び活発になった。2009年10月に2回目のメジャーバージョンアップが実施され、2.0版がリリースされた。OpenCV 2.4.4以降ではJavaが公式にサポートされている\[5\]。OpenCV 2.x系列は2018年2月に2.4.13.6 がリリースされており、3.x系列と同時にメンテナンスが続けられている\[6\]\[7\]\[8\]\[9\]。

2015年6月に3回目のメジャーバージョンアップとしてOpenCV 3.0が正式リリースされた。OpenCV 3.0では従来の[C言語](../Page/C言語.md "wikilink")関数形式のインターフェイスはレガシーAPI扱いとなりメンテナンスが終了しているため、代わりに[C++](../Page/C++.md "wikilink") APIを使うことが推奨されている\[10\]。2015年12月にリリースされたOpenCV 3.1では、[Google Summer of Code](https://ja.wikipedia.org/wiki/Google_Summer_of_Code "wikilink") 2015の成果物の取り込みなど、多数の機能が追加されている\[11\]。

2018年11月にOpenCV 4.0がリリースされた\[12\]。[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")規格準拠コンパイラが必須となり、またC言語APIは廃止された。

## 機能

実装分野は次の通り。

  - [画像処理](https://ja.wikipedia.org/wiki/画像処理 "wikilink") (Image Processing)
      - [勾配](https://ja.wikipedia.org/wiki/勾配 "wikilink")、[エッジ](https://ja.wikipedia.org/wiki/エッジ "wikilink")、コーナー (Gradients, Edges and Corners)

      - サンプリング、[補間](https://ja.wikipedia.org/wiki/補間 "wikilink")、[幾何変換](https://ja.wikipedia.org/wiki/幾何変換 "wikilink") (Sampling, Interpolation and Geometrical Transforms)

      - 演算 (Morphological Operations)

      - フィルタと色変換 (Filters and Color Conversion)

      - ピラミッドとその応用 (Pyramids and the Applications)

      - 画像分割、領域結合、[輪郭検出](https://ja.wikipedia.org/wiki/輪郭検出 "wikilink") (Image Segmentation, Connected Components and Contour Retrieval)

      - 画像と形状の[モーメント](../Page/モーメント.md "wikilink") (Image and Contour Moments)

      - 特殊な画像変換 (Special Image Transforms)

      - [ヒストグラム](../Page/ヒストグラム.md "wikilink") (Histograms)

      - [マッチング](https://ja.wikipedia.org/wiki/マッチング "wikilink") (Matching)

      - [ラベリング](https://ja.wikipedia.org/wiki/ラベリング "wikilink") (Labeling) : OpenCV 3.0以降
  - 構造解析 (Structural Analysis)
      - [輪郭](https://ja.wikipedia.org/wiki/輪郭 "wikilink")処理 (Contour Processing)
      - 計算[幾何](https://ja.wikipedia.org/wiki/幾何 "wikilink") (Computational Geometry)
      - 平面再分割 (Planar Subdivisions)
  - モーション解析と物体追跡 (Motion Analysis and Object Tracking)
      - 背景統計量の累積 (Accumulation of Background Statistics)
      - [モーションテンプレート](https://ja.wikipedia.org/wiki/モーションテンプレート "wikilink") (Motion Templates)
      - 物体追跡 (Object Tracking)
      - [オプティカルフロー](https://ja.wikipedia.org/wiki/オプティカルフロー "wikilink") (Optical Flow)
      - [推定器](https://ja.wikipedia.org/wiki/推定器 "wikilink") (Estimators)
  - [パターン認識](../Page/パターン認識.md "wikilink") (Pattern Recognition)
      - 物体検出 (Object Detection)
  - [カメラキャリブレーション](https://ja.wikipedia.org/wiki/カメラキャリブレーション "wikilink")と[3次元再構成](https://ja.wikipedia.org/wiki/3次元再構成 "wikilink") (Camera Calibration and 3D Reconstruction)
      - [カメラキャリブレーション](https://ja.wikipedia.org/wiki/カメラキャリブレーション "wikilink") (Camera Calibration)
      - 姿勢推定 (Pose Estimation)
      - [エピポーラ幾何](https://ja.wikipedia.org/wiki/エピポーラ幾何 "wikilink") (Epipolar Geometry)

<!-- end list -->

  - [機械学習](https://ja.wikipedia.org/wiki/機械学習 "wikilink")
      - [単純ベイズ分類器](https://ja.wikipedia.org/wiki/単純ベイズ分類器 "wikilink") (Naive Bayes Classifier)
      - [k近傍法](https://ja.wikipedia.org/wiki/k近傍法 "wikilink") (K Nearest Neighbors)
      - [サポートベクターマシン](../Page/サポートベクターマシン.md "wikilink") (SVM)
      - [決定木](https://ja.wikipedia.org/wiki/決定木 "wikilink") (Decision Trees)
      - [ブースティング](https://ja.wikipedia.org/wiki/ブースティング "wikilink") (Boosting)
      - [Random forest](https://ja.wikipedia.org/wiki/Random_forest "wikilink") (Random forest)
      - [EMアルゴリズム](https://ja.wikipedia.org/wiki/EMアルゴリズム "wikilink") (Expectation-Maximization)
      - [ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink") (Neural Networks)

<!-- end list -->

  - [ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")
      - シンプル[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (Simple GUI)
      - 画像の読み込みと保存 (Loading and Saving Images)
      - ビデオ入出力 (Video I/O)
      - [OpenGL](../Page/OpenGL.md "wikilink")/[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")相互運用

。

OpenCV 2.1\[13\]で[SSE拡張命令を使用した最適化コードが実装されている](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令 "wikilink")。OpenCV 3.0で[Intel IPPのサブセットがIPPCVとして寄贈され](https://ja.wikipedia.org/wiki/Intel_IPP "wikilink")、デフォルトで使用されるようになった\[14\]。そのほか、[Intel TBBや](https://ja.wikipedia.org/wiki/Intel_TBB "wikilink")[OpenMP](../Page/OpenMP.md "wikilink")を利用した並列化も実装されている。OpenCV 3.1ではクロスプラットフォームな[SIMD](https://ja.wikipedia.org/wiki/SIMD "wikilink")アクセラレーションのためのUniversal Intrinsicsが導入され\[15\]、従来からのSSE ([x86](https://ja.wikipedia.org/wiki/x86 "wikilink")) 命令のサポートに加え、[AVX](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令 "wikilink") (x86) 命令や[NEON](https://ja.wikipedia.org/wiki/NEON "wikilink") ([ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")) 命令のサポートも加わっている。

OpenCV 2.2\[16\]で[CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")を使ったアクセラレータであるgpuモジュール、OpenCV 2.4.3\[17\]で[OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")を使ったアクセラレータであるoclモジュールが追加された。gpuモジュールを有効にするためには、OpenCVを`WITH_CUDA=ON`構成でビルドする必要がある\[18\]。また、oclモジュールを有効にするためには、OpenCVを`WITH_OPENCL=ON`構成でビルドする必要がある\[19\]。なおOpenCV 2.4.11時点で、公式のWindows用ビルド済みバイナリではCUDAは有効にされていないが、OpenCLは有効にされている。またgpuモジュールおよびoclモジュールはともに、従来のCPUベースのOpenCV機能と比べて、対応するチャンネルフォーマットに関して制約がある。そのほか、gpuモジュールを使用するためには、CUDAに対応した[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")製[GPUを](../Page/Graphics_Processing_Unit.md "wikilink")、そしてoclモジュールを使用するためには、OpenCL 1.1に対応したハードウェアを用意する必要がある。

なお、OpenCV 3.0ではgpuモジュールはcudaモジュールに改称され、また独立したoclモジュールは廃止されてOpenCVの各モジュールに透過API (Transparent API, T-API) として分散・融合されている\[20\]。OpenCV 3.0にはOpenCLの相互運用を可能とするラッパーAPIも用意されており、OpenCL-C言語でカスタムカーネルを記述できるほか、OpenCL 1.2サポートを有効にしてOpenCVをビルドすることで、OpenCL 1.2対応のプラットフォームおよびデバイス上でOpenCL 1.2の機能（カーネルの分割コンパイル＆リンクなど）を使えるようになる\[21\]。また、オプションとしてOpenCL 2.0もしくは[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") () 拡張のShared Virtual Memoryもサポートしている\[22\]。

## 各種言語バインディング（ラッパー）

公式に提供されているOpenCV APIとして、C/C++用インターフェイスのほか、Java、Python、MATLABバインディングが存在するが、そのほかにも非公式の各種言語向けのラッパーが存在する。

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")用ラッパー
      - [JavaCV](https://github.com/bytedeco/javacv) - OpenCV, [FFmpeg](https://ja.wikipedia.org/wiki/FFmpeg "wikilink"), libdc1394, PGR FlyCapture, OpenKinect, videoInput, ARToolKitPlus のラッパー。バージョン1.0でOpenCV 3.0に対応。[GPL](../Page/GNU_General_Public_License.md "wikilink") v2ライセンスと[Apacheライセンス](https://ja.wikipedia.org/wiki/Apacheライセンス "wikilink")に対応。

<!-- end list -->

  - [.NET用ラッパー](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
      - [SharperCV](http://www.cs.ru.ac.za/research/groups/SharperCV/) - 商用利用不可、開発終了。
      - [OpenCVDotNet](http://code.google.com/p/opencvdotnet/) - [GPL](../Page/GNU_General_Public_License.md "wikilink") v2ライセンス、OpenCV 1.0対応、2007年のバージョン0.7を最後に更新停止。
      - [Emgu CV](http://www.emgu.com/wiki/index.php/Main_Page) - [GPL](../Page/GNU_General_Public_License.md "wikilink") v3ライセンスもしくは商用ライセンス、OpenCV 2.4.10/3.4.3/4.0.1に対応。[Mono](https://ja.wikipedia.org/wiki/Mono "wikilink")対応、[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリ対応。
      - [OpenCvSharp](https://github.com/shimat/opencvsharp) - [3条項BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")、OpenCV 2.4.10/3.1に対応。[Mono](https://ja.wikipedia.org/wiki/Mono "wikilink")対応。
      - [OpenCV.NET](https://bitbucket.org/horizongir/opencv.net) - [BSDスタイルライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink") (MIT)、[Mono](https://ja.wikipedia.org/wiki/Mono "wikilink")対応。

<!-- end list -->

  - その他
      - [ruby-opencv](https://github.com/ruby-opencv/ruby-opencv) - [Ruby](../Page/Ruby.md "wikilink") 1.9.3/2.xおよびOpenCV 2.4.10に対応。[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")。
      - [HSPCV](http://www.onionsoft.net/hsp/v33/doclib/hspcv.txt) - [Hot Soup Processor](https://ja.wikipedia.org/wiki/Hot_Soup_Processor "wikilink") 3.1以降およびOpenCV 1.0に対応。[Hot Soup Processorに付属](https://ja.wikipedia.org/wiki/Hot_Soup_Processor "wikilink")。BSDライセンス。

## 関連項目

  - [画像処理](https://ja.wikipedia.org/wiki/画像処理 "wikilink")
  - [顔認識](https://ja.wikipedia.org/wiki/顔認識 "wikilink")
  - [機械学習](https://ja.wikipedia.org/wiki/機械学習 "wikilink")
  - [:en:Mathematical morphology](https://ja.wikipedia.org/wiki/:en:Mathematical_morphology "wikilink")

<!-- end list -->

  - [アクセラレータ用](https://ja.wikipedia.org/wiki/ハードウェアアクセラレーション "wikilink")[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")
      - [CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")
      - [OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")

## 参照

## 外部リンク

  -
  - [OpenCV リファレンスマニュアル（日本語訳）とサンプルプログラム集](http://opencv.jp/)

  - [OpenCV Wiki](http://opencv.willowgarage.com/wiki/) - Willow GarageによるOpenCV Wiki

  - [OpenCV SourceForge](http://sourceforge.net/projects/opencvlibrary/)

  - [Introduction to programming with OpenCV](http://www.cs.iit.edu/~agam/cs512/lect-notes/opencv-intro/) - コードの例がある。

[Category:コンピュータビジョン](https://ja.wikipedia.org/wiki/Category:コンピュータビジョン "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.  [Intel Acquires Computer Vision for IOT, Automotive | Intel Newsroom](https://newsroom.intel.com/editorials/intel-acquires-computer-vision-for-iot-automotive/#gs.5cra62)
3.  [Intel acquires Itseez | opencv.org](https://opencv.org/intel-acquires-itseez/)
4.  [About | opencv.org](https://opencv.org/about/)
5.  [Introduction to Java Development — OpenCV 2.4.13.0 documentation](http://docs.opencv.org/2.4.13/doc/tutorials/introduction/desktop_java/java_dev_intro.html)
6.
7.  [OpenCV - Browse /opencv-win at SourceForge.net](http://sourceforge.net/projects/opencvlibrary/files/opencv-win/)
8.  [Tags · opencv/opencv | GitHub](https://github.com/opencv/opencv/tags)
9.  [Releases · opencv/opencv | GitHub](https://github.com/opencv/opencv/releases)
10. [OpenCV 3.0 Latest news and the Roadmap, Kirill Kornyakov, Itseez, ICVS 2013](http://www.slideshare.net/EugeneKhvedchenya/opencv-30-latest-news-and-the-roadmap)
11. [OpenCV 3.1 | OpenCV](http://opencv.org/opencv-3-1.html)
12. [OpenCV 4.0 - OpenCV library](https://opencv.org/opencv-4-0-0.html)
13. [OpenCV2.0 から OpenCV2.1 の変更点（ChangeLog） | OpenCV.jp](http://opencv.jp/opencv2-x-tips/changelog_from_20)
14. [OpenCV 3.0 | OpenCV](http://opencv.org/opencv-3-0.html)
15. [OpenCV: Universal intrinsics](https://docs.opencv.org/3.1.0/df/d91/group__core__hal__intrin.html)
16. [OpenCV 2.2 Released - ROS robotics news](http://www.ros.org/news/2010/12/opencv-22-released.html)
17. [OpenCV 2.4.3 released | OpenCV](http://opencv.org/opencv-2-4-3-released.html)
18. [GPU Module Introduction — OpenCV 2.4.11.0 documentation](http://docs.opencv.org/2.4.11/modules/gpu/doc/introduction.html)
19. [OpenCL Module Introduction — OpenCV 2.4.11.0 documentation](http://docs.opencv.org/2.4.11/modules/ocl/doc/introduction.html)
20. [OpenCV: OpenCV modules](http://docs.opencv.org/3.0.0/)
21. [opencv/opencl_core.hpp at 3.0.0 · Itseez/opencv - GitHub](https://github.com/Itseez/opencv/blob/3.0.0/modules/core/include/opencv2/core/opencl/runtime/opencl_core.hpp)
22. [opencv/ocl.cpp at 3.0.0 · Itseez/opencv - GitHub](https://github.com/Itseez/opencv/blob/3.0.0/modules/core/src/ocl.cpp)