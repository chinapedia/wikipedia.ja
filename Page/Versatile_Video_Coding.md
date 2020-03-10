> この記事は[Versatile Video Coding](https://ja.wikipedia.org/wiki/Versatile_Video_Coding)から翻訳されています。


**Versatile Video Coding** (**VVC**) (MPEG-I Part 3)は、**Joint Video Experts Team** (**JVET**)によって2020年中頃の完成を目指して開発されている未来の[動画圧縮](https://ja.wikipedia.org/wiki/動画圧縮 "wikilink")標準規格である\[1\]。JVETは[ISO/IEC JTC 1の](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")[MPEG](https://ja.wikipedia.org/wiki/MPEG "wikilink")ワーキンググループと[ITU-T](../Page/ITU-T.md "wikilink")のワーキンググループを統合したビデオ専門家チームである。時々、VVCはFVC (Future Video Coding)や**ITU-T H.266**とも呼ばれてきた。 [High Efficiency Video Coding](https://ja.wikipedia.org/wiki/High_Efficiency_Video_Coding "wikilink")（[HEVC](https://ja.wikipedia.org/wiki/HEVC "wikilink")、ITU-T [H.265](https://ja.wikipedia.org/wiki/H.265 "wikilink")あるいは[MPEG-H](https://ja.wikipedia.org/wiki/MPEG-H "wikilink") Part 2としても知られている）の後継になる予定である。

以前のH.26xとMPEG動画圧縮規格のようにVVCの[データ圧縮](../Page/データ圧縮.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")は[離散コサイン変換](../Page/離散コサイン変換.md "wikilink")(DCT)による符号化に基づいている。以前の規格で使われたタイプII DCT (DCT-II)に加えて、VVCはタイプVIII DCT (DCT-VIII)も使用する\[2\]。

## 構想

2015年8月、[MPEG](https://ja.wikipedia.org/wiki/MPEG "wikilink")とは、現行の圧縮技術を評価したり、次世代の動画圧縮標準規格に対する要求を研究するために Joint Video Exploration Team (JVET)を結成した。新しいアルゴリズムは、同等の視覚的品質に対して30%〜50%改善した圧縮率を目指すべきであり、ロスレス圧縮（画質の劣化がない圧縮）と主観的ロスレス圧縮（視聴者の視力的に画質の劣化がない圧縮）も対応する。新しいアルゴリズムは、360°ビデオだけでなく4Kから16Kまでの解像度に対応する。

VVCは、以下の要求に対応するべきである。

  - [YCbCr](https://ja.wikipedia.org/wiki/YCbCr "wikilink")。フォーマットは、4:4:4, 4:2:2, 4:2:0
  - YCbCrの1成分（Y,Cb,Crのどれか一つ）あたり10bitから16bit
  - [色空間](../Page/色空間.md "wikilink")BT.2100。広い色域と16stops（stopsはカメラの絞りの段数）より明るさの範囲が広いHDR（1000, 4000, 10000 [nitsの頂点輝度を持つ](https://ja.wikipedia.org/wiki/カンデラ毎平方メートル "wikilink")）に対応。
  - 補助チャンネル（深度、透明度など）
  - 可変かつ非整数のフレームレート。0Hzから120Hzまで対応。
  - 時間（フレームレート）と空間（解像度）に対してスケーラブルなビデオ圧縮
  - [SN比](../Page/SN比.md "wikilink")の良さ
  - 色域とダイナミックレンジの区別
  - 3Dステレオ動画とマルチビュー動画
  - パノラマ動画
  - 静止画像

エンコーディングの複雑さは、[HEVC](https://ja.wikipedia.org/wiki/HEVC "wikilink")(H.265)の5,6倍から最大10倍が予想され、圧縮アルゴリズムの品質に依存する。圧縮アルゴリズムの品質についてはVCCの標準規格の範囲外である。

VVCの開発は、VVC Test Model (VTM)を使って行われる\[3\]。VTMは、参照用のVVCのソースコードであり、最小限のコーディングツールから提供が始まった。さらなるコーディングツールはCore Experiments (CEs)でテストされた後に追加される。VTMの前身は Joint Exploration Model (JEM)であった。[HEVC](https://ja.wikipedia.org/wiki/HEVC "wikilink")の開発に使われた参照用コーデックを元にして作られた実験的なコーデックのソースコードである。

## 歴史

JVETは、2017年10月に最後の提案募集を行い、それとともに標準化作業を公式に開始した\[4\]。

VVC標準の最初の草案は、2018年4月に発行された\[5\]。

（放送関係者などのために放送技術や放送機材を扱う[見本市](../Page/見本市.md "wikilink")）において、VVCの試作実装が披露され、[HEVC](https://ja.wikipedia.org/wiki/HEVC "wikilink")よりも40%効率的に動画を圧縮すると述べた\[6\]。

最終的な標準規格は、2020年7月に承認されると予想されている\[7\]\[8\]。

### 現行スケジュール

  - 2017年10月 : 最後の提案募集
  - 2018年4月 : 受け取った提案の査定と標準規格の最初の草案\[9\]
  - 2019年7月 : 委員会草案（Committee Draft）についての投票が行われた。
  - 2019年10月 : 国際標準草案（Draft International Standard）についての投票が行われた。
  - 2020年7月 : 最終標準規格の完成（予定）

## ライセンス

HEVC([H.265](https://ja.wikipedia.org/wiki/H.265 "wikilink"))の実装をライセンスするときに見られた問題のリスクを減らすために Media Coding Industry Forum (MC-IF)と呼ばれる新しい組織がVVCのために創設された\[10\]\[11\]。しかしながら、MC-IFは標準化プロセスを超える公式な権力は持っていない。標準化プロセスは、未だに純粋に技術的なものである\[12\]。

## 関連項目

  - [H.265 / MPEG-H Part 2 / High Efficiency Video Coding / HEVC](https://ja.wikipedia.org/wiki/High_Efficiency_Video_Coding "wikilink")
  - [H.264 / MPEG-4 Advanced Video Coding / AVC](../Page/H.264.md "wikilink")
  - [H.262 / MPEG-2 Part 2 video](../Page/MPEG-2.md "wikilink")

## 出典

## 外部リンク

  - [VVC website at the Fraunhofer Heinrich Hertz Institute](https://jvet.hhi.fraunhofer.de/)
  - [Stand by for ITU H.266 compression](https://advanced-television.com/2018/02/01/stand-by-for-h-266-compression)
  - [Improvement of HEVC Intercoding Mode using multiple transforms](https://www.researchgate.net/publication/317197361_Improvement_of_HEVC_Inter-coding_Mode_Using_Multiple_Transforms)
  - [Transform competition for temporal prediction in video coding](https://www.researchgate.net/publication/323194130_Transform_Competition_for_Temporal_Prediction_in_Video_Coding)
  - [Adaptive transforms for inter-predicted residuals in post-HEVC video coding](https://www.researchgate.net/publication/312053838_Adaptive_Transforms_for_Inter-Predicted_Residuals_in_Post-HEVC_Video_Coding)
  - [Future Video Coding](https://mpeg.chiariglione.org/standards/exploration/future-video-coding)

[Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:映像技術](https://ja.wikipedia.org/wiki/Category:映像技術 "wikilink")

1.
2.
3.  <https://jvet.hhi.fraunhofer.de>
4.   MPEG|website=mpeg.chiariglione.org|access-date=2019-01-21}}
5.   MPEG|website=mpeg.chiariglione.org|access-date=2019-08-18}}
6.
7.   MPEG|website=mpeg.chiariglione.org|access-date=2019-01-21}}
8.
9.
10.
11.
12.