> この記事は[VVVF](https://ja.wikipedia.org/wiki/VVVF)から翻訳されています。


**VVVFインバータ制御**（ブイブイブイエフインバータせいぎょ）とは、[交流電動機](https://ja.wikipedia.org/wiki/交流電動機 "wikilink")を、その特性に合わせて任意の[速度](../Page/速度.md "wikilink")、[回転数](https://ja.wikipedia.org/wiki/回転数 "wikilink")で動作させるために、（静止）[インバータ](../Page/インバータ.md "wikilink")を用いて任意の[周波数](../Page/周波数.md "wikilink")と[電圧](../Page/電圧.md "wikilink")を発生させる[制御](https://ja.wikipedia.org/wiki/制御 "wikilink")方式。これを一般に「インバータ方式」というが、[鉄道](../Page/鉄道.md "wikilink")関係ではそれを特に「VVVFインバータ方式」、あるいは「VVVF方式＝[可変電圧可変周波数方式](https://ja.wikipedia.org/wiki/可変電圧可変周波数制御 "wikilink")」と呼んでいる。VVVFは可変電圧可変周波数を[直訳](https://ja.wikipedia.org/wiki/直訳 "wikilink")した[和製英語](../Page/和製英語.md "wikilink")**(Variable Voltage Variable Frequency)**であり、 [英語圏](../Page/英語圏.md "wikilink")ではVFD**(variable-frequency drive)**と言われる\[1\]｡

## 解説

[交流](../Page/交流.md "wikilink")の周波数（[同期速度](../Page/同期速度.md "wikilink")）を追って回る交流モータを使う場合、従前は任意周波数の[電源](https://ja.wikipedia.org/wiki/電源 "wikilink")がなかなか得られず、[商用電源周波数](../Page/商用電源周波数.md "wikilink")（[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")では50 [Hzまたは](../Page/ヘルツ.md "wikilink")60 Hz）固定の電源で[起動](https://ja.wikipedia.org/wiki/起動 "wikilink")させるため、任意速度での運転ができなかった。商用周波数での同期速度付近でのみ運転可能で、起動[トルク](../Page/トルク.md "wikilink")が小さかったり、効率を落としたり、定常運転時は大出力交流モータを軽[負荷](https://ja.wikipedia.org/wiki/負荷 "wikilink")で使っていた。そうした経過で、その動作特性も、取り扱い法も商用周波数固定でのものが広く知られているだけで、回転数、周波数特性についてはほとんど記述がなく、知られていなかった。同期速度とは[回転磁界](https://ja.wikipedia.org/wiki/回転磁界 "wikilink")の速度で、[電機子](https://ja.wikipedia.org/wiki/電機子 "wikilink")構造が2･P極の場合、周波数f/Pとなる。小型機に一般的な4極構造ではf/（4/2）が同期速度。60 Hzであれば2極で60 rps（毎秒回転数）、4極で30 rps、6極で20 rpsが同期速度である。60を掛ける記述は[秒速](https://ja.wikipedia.org/wiki/秒速 "wikilink") - [分速](https://ja.wikipedia.org/wiki/分速 "wikilink")[単位](../Page/単位.md "wikilink")換算の[rpm（毎分回転数）表示である](https://ja.wikipedia.org/wiki/rpm_\(単位\) "wikilink")。

### トルクの電圧・周波数特性

[thumb](https://ja.wikipedia.org/wiki/ファイル:emf_3vf.gif "wikilink")

トルクの周波数特性としては、（電圧 V/周波数 f）<sup>2</sup> に比例し、さらに[誘導電動機](../Page/誘導電動機.md "wikilink")では、停動トルク\[2\]より微少な場合は[すべり周波数](https://ja.wikipedia.org/wiki/同期速度#滑り "wikilink") f<sub>s</sub> に比例する（一般的な「すべり率 S」ではなく「すべり周波数 f<sub>s</sub> 」であることに注意）。同期電動機では電機子磁界と[回転子](../Page/回転子.md "wikilink")磁界の角度 δに関して sin(δ/2)に比例する。
式表現すれば
τ＝K<sub>1</sub>･Φ･I　････････････K<sub>1</sub>,K<sub>2</sub>:比例定数、Φ:鎖交総磁束、I:電機子電流
　　≒K<sub>2</sub>･(V/f)^2･f<sub>s</sub>　･･････V:電圧、f：電源周波数、f<sub>s</sub>:スベリ周波数（ただし停動トルクよりかなり小さい領域）
　同期電動機では τ≒K･(V/f)^2･sin(δ/2)　･･････
すなわち V/f を一定にして（＝電圧と周波数を比例させて）ゼロから徐々に増やして起動すればよく、周波数に応じた任意の速度での運転ができる。

### 任意周波数電源をパワー半導体で構成

近年の[電力用半導体素子](https://ja.wikipedia.org/wiki/電力用半導体素子 "wikilink")の進歩により、任意周波数、任意電圧の交流電力を生成する[インバータ](../Page/インバータ.md "wikilink")（直流-交流変換器）が得られるようになり、交流モータの特性に合わせて、電機子誘起起電力+インピーダンス降下の電圧を供給して駆動することで任意の速度で運転できるようになった。電機子誘起起電力は磁界が一定であれば回転数：すなわち周波数に比例するから、供給電圧/周波数をほぼ一定にして速度制御することがVVVFインバータ制御の基本である。

初期のインバータ駆動では、半導体の容量が小さく、方形波駆動～数パルスで正弦波を近似していたが、さらに速度ゼロから徐々に起動させる低速大電力ではPWM方式などで正弦波に近付けて高調波の損失・悪影響を小さくして起動した。ところがGTOサイリスタなど大電力半導体のスイッチング速度が遅いため、速度を上げると1サイクル1パルスにも達して回転数と搬送波周波数が干渉するので、それを避けるため高速域では搬送波周波数を回転数の整数倍にした。これを「パルスモード」「同期モード」と呼び、低速部の整数倍関係のない動作を「非同期モード」と呼んでいる。

### 鉄道車両

[鉄道車両](../Page/鉄道車両.md "wikilink")ではこの電圧・周波数比例領域を特に「**V/f一定領域**（定引張力領域）」と呼んでおり、V/fを一定に保ちながら、一定トルクによる[加速](https://ja.wikipedia.org/wiki/加速 "wikilink")を行う。インバータの最大出力と最大電圧以降の高速領域は電圧一定で周波数を上げるので「**CVVF領域**（一定電圧可変周波数領域）」と呼ぶが、CVVF領域のうち、[電流](../Page/電流.md "wikilink")一定で加速を続ける領域は、誘導電動機であればすべり周波数を増やして加速するが、供給電力としては一定（＝電圧一定×電流一定）なので「**定出力領域**」と呼び、トルクは[回転速度](https://ja.wikipedia.org/wiki/回転速度 "wikilink")に[反比例](../Page/反比例.md "wikilink")する。停動トルク（脱出トルク）に近づくと、すべり周波数は増やせなくなり、周波数のみを増やす「**特性領域**」となり、トルクは回転速度の2乗に反比例するとともに出力も下がっていく。また、[トルク](../Page/トルク.md "wikilink")指令時において誘導電動機のトルク急変時でのトルク制御には、「**V/f一定・すべり周波数制御**｣と｢**ベクトル制御**｣があり、後者は電動機に流れる1次電流を、固定子側の界磁で磁束を発生させる励磁電流成分と回転子側に誘導電流として流れてトルクに寄与する90度位相の2次電流成分とに分けて、励磁電流を一定に保ちながらトルク指令に対応した2次電流を制御する方式であり、すべり周波数制御に比べて、トルク変化に対しての応答性が良く制御精度が向上している。

### 直流電動機制御との比較

[直流電動機](../Page/直流電動機.md "wikilink")制御との比較でいえば、「電機子誘起起電力（＝逆起電力）+内部[抵抗降下](../Page/電気抵抗.md "wikilink")」を直流電動機に加えて起動させるのが[抵抗制御](../Page/抵抗制御.md "wikilink")や[電機子チョッパ制御の基本であるから](https://ja.wikipedia.org/wiki/電気車の速度制御#チョッパ制御の仕組み "wikilink")、VVVFインバータ制御はそれに周波数と[位相](../Page/位相.md "wikilink")が加わるだけで基本は同様である。「定出力領域」と「特性領域」についても直流電動機の「弱界磁領域＝定出力領域」「特性領域」と変わらない。またV/f一定領域も定トルクに制御すれば抵抗制御直流電動機での「定引張力領域」と同様である。

### インバータの制御対象

インバータ制御の対象となる交流モータは、初期の[TGV](https://ja.wikipedia.org/wiki/TGV "wikilink")などでは[電磁石同期電動機](../Page/電磁石同期電動機.md "wikilink")が用いられているが、TGVの最新モデルでは[かご形三相誘導電動機](../Page/かご形三相誘導電動機.md "wikilink")に替わっている。日本ではかご形三相誘導電動機が圧倒的だが、近年は[永久磁石同期電動機](../Page/永久磁石同期電動機.md "wikilink")が用いられている車両が登場している。高効率を追求する[エアコン用として日本では近年](../Page/エア・コンディショナー.md "wikilink")[ブラシレス直流モータを使うようになった](https://ja.wikipedia.org/wiki/無整流子電動機 "wikilink")。また[家電用など小型機には](../Page/家庭用電気機械器具.md "wikilink")90度位相差の[二相交流](https://ja.wikipedia.org/wiki/二相交流 "wikilink")駆動があるが、多くは[三相交流](../Page/三相交流.md "wikilink")である。誘導電動機のすべり率Sは回転子での電力損割合なので、低速回転ほど損失率が増え効率が下がるので、低速回転になる[直接駆動モータ](https://ja.wikipedia.org/wiki/ダイレクトドライブ "wikilink")（DDM）ではスベリ回転のない同期電動機が選ばれることが多い。

## 脚注

## 注釈

## 関連項目

  - [電気車の速度制御](https://ja.wikipedia.org/wiki/電気車の速度制御 "wikilink")
  - [可変電圧可変周波数制御](https://ja.wikipedia.org/wiki/可変電圧可変周波数制御 "wikilink")

[Category:電動機](https://ja.wikipedia.org/wiki/Category:電動機 "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink") [Category:鉄道車両の制御方式](https://ja.wikipedia.org/wiki/Category:鉄道車両の制御方式 "wikilink")

1.  [可変電圧可変周波数制御\#概要](https://ja.wikipedia.org/wiki/可変電圧可変周波数制御#概要 "wikilink")を参照
2.  [停動トルク](http://www.orientalmotor.co.jp/tech/glossary/ta11/) - [オリエンタルモーター](https://ja.wikipedia.org/wiki/オリエンタルモーター "wikilink") \> セミナー技術情報 \> 用語解説（2015年版 / 2015年9月20日閲覧）