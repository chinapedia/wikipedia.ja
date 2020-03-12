> この記事は[SUPER-UX](https://ja.wikipedia.org/wiki/SUPER-UX)から翻訳されています。


**SUPER-UX**は、[日本電気](../Page/日本電気.md "wikilink")（NEC）のベクトルスーパコンピュータ[SXシリーズ用](../Page/NEC_SX.md "wikilink")[UNIX](../Page/UNIX.md "wikilink")である。

当初のSXシリーズは、当時の他の日本製スパコンメーカ（富士通と日立）と同様、自社の[汎用機](../Page/メインフレーム.md "wikilink")（NECの場合は[ACOS](../Page/Advanced_Comprehensive_Operating_System.md "wikilink")）を高性能計算以外の処理に使う構成としていたこともあり、その汎用機用OSであるACOS\[1\]をベースとした[SX-OS](https://ja.wikipedia.org/wiki/SX-OS "wikilink")を使用していた。

しかしSX-3の頃には既にHPCでもUNIXの採用が世界的潮流であり、各国立大学の研究者やユーザからの強い要望があった。そのため、NECもUNIX系OSを採用し、SUPER-UXと名付けられた。

ベースは元々SystemV Release3で、4.3[BSD](../Page/BSD.md "wikilink")の機能とネットワーク関係強化をされたものだったが、安価/高性能ということでNECスパコンのシェアを大幅に上げたSX-4の対応においてSVR4.2MP対応され、[スレッド機能も使用できるようになり](../Page/スレッド_\(コンピュータ\).md "wikilink")、より並列度が上がるように、粒度を向上した 。他にも、HPC応用に適したギャングスケジュールなどの機能を持ち、旗艦システムの[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")をはじめ、各地のSXシリーズを採用した計算センタで運用されている。

近年のSXシリーズでは、「SPE」がSUPER-UXを実行する、という構成になっている（番号的には10にあたる、[SX-ACEまで](https://ja.wikipedia.org/wiki/NEC_SX-ACE "wikilink")）。11にあたる[SX-Aurora TSUBASAでは](https://ja.wikipedia.org/wiki/NEC_SX-Aurora_TSUBASA "wikilink")、管理側（「ベクトルホスト」とNECは呼んでいる）がx86系になったことから、Linuxに移行した。

## 注

<references/>

[Category:System_V](https://ja.wikipedia.org/wiki/Category:System_V "wikilink") [Category:NECのスーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:NECのスーパーコンピュータ "wikilink")

1.  NECはシステムの名称として、ハードウェアとOSの両方を「ACOS」と呼んでいる。