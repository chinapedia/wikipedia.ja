> この記事は[SHA-3](https://ja.wikipedia.org/wiki/SHA-3)から翻訳されています。


**SHA-3**は、元は**Keccak** (あるいは)\[1\]\[2\]として知られた[暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")である。[SHAシリーズの代替という目的](../Page/Secure_Hash_Algorithm.md "wikilink")\[3\]からSHA-3という名があるが、その内部構造はSHA-2までの方式（[:en:Merkle–Damgård construction](https://ja.wikipedia.org/wiki/:en:Merkle–Damgård_construction "wikilink")）とは全く異なっている。[RadioGatún](https://ja.wikipedia.org/wiki/RadioGatún "wikilink")を基にし、Guido Bertoni、Joan Daemen、Michaël Peeters、Gilles Van Asscheによって設計された。

SHA-3は、2004年のCRYPTOにはじまる、[MD5](../Page/MD5.md "wikilink")への攻撃成功の確認\[4\]と[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")への攻撃の理論的確立\[5\]という急速に進んだ在来の関数の危殆化を動機とした、[アメリカ国立標準技術研究所](../Page/アメリカ国立標準技術研究所.md "wikilink")(NIST)によるこれらに類似した構造を持たないハッシュ関数を求めたコンペティションによるものである。しかしその後、[SHA-2](https://ja.wikipedia.org/wiki/SHA-2 "wikilink")への攻撃法の研究は進んだものの、2017年初頭時点では効率的な（有効な）攻撃法の報告はまだ無いことなどのため、結果としてSHA-2の代替の用意が重要ではなくなるなど、状況が変化している\[6\]。（なおその一方でSHA-1については、2017年2月には衝突攻撃（強衝突耐性の突破）の成功が現実に示され、SHA-2への移行は2017年現在、喫緊の要求となっている）

2012年10月2日、Keccakがコンペティションの勝者として選ばれ\[7\]、[2015年](../Page/2015年.md "wikilink")[8月5日](../Page/8月5日.md "wikilink")に正式版が **FIPS PUB 202** として公表された\[8\]。

Keccakはスポンジ構造（sponge construction、参: [:en:Sponge function](https://ja.wikipedia.org/wiki/:en:Sponge_function "wikilink")）\[9\]\[10\]を採用しており、メッセージのブロックは状態の初期ビットとの[XOR](https://ja.wikipedia.org/wiki/XOR "wikilink")を取ったのちに後述のブロック置換が行われる。SHA-3で用いられているバージョンでは、状態は64ビットのワード長の5×5アレイから構成され、総計で1600ビットである。設計者によれば、Keccakは[Intel Core 2で](../Page/Intel_Core_2.md "wikilink")12.5 cycles per byteの速度が出ると主張している\[11\]。また、ハードウェア実装では他のどの最終候補よりも高速であった\[12\]。

Keccakの設計者は、[認証付き暗号](https://ja.wikipedia.org/wiki/認証付き暗号 "wikilink")や特定のアーキテクチャにおいてより高速のハッシュ計算を実現する「木」構造のハッシュなど、標準化されていない関数の利用法を提唱している\[13\]。Keccakでは、[2の冪](../Page/2の冪.md "wikilink")で表現できる任意のワード長を使うことができる（最小のワード長は *w=2<sup>0</sup> = 1* であり、そのときの状態は25ビット）。小さい状態長は暗号研究でのテストに有用であり、中間的な状態長（*w*=4のとき100ビット、*w*=32のとき800ビット）は、実用的な軽量の代替実装として利用できる。

## ハッシュ関数の構造

[lang=ja](https://ja.wikipedia.org/wiki/File:SpongeConstruction.svg "fig:lang=ja")や[原像攻撃](https://ja.wikipedia.org/wiki/原像攻撃 "wikilink")に対して望む耐性の2倍必要である。\]\] Keccakはスポンジ構造を採用しており、入力が一定の比率で内部状態に「吸収」され、ハッシュ出力では同じ比率で「絞り出」される。

データの *r* ビットを吸収するときには、データと状態の先頭ビットの排他的論理和を取り、ブロック置換を行う。絞り出すときには、状態の先頭 *r* ビットを出力として生成し、さらなる出力が必要な時にはブロック置換を行う。

この機構の中心はハッシュ関数の「キャパシティ」であり、入力でも出力でも触れられることのない *c*=25*w*−*r* ビットの状態である。これは求められるセキュリティ強度に応じて調整可能であり、SHA-3では出力ハッシュ長を *n* ビットとしたとき *c*=2*n* と保守的な設定がなされている。そのため、1回のブロック置換ごとに吸収されるメッセージの長さ *r* は出力ハッシュ長に依存することとなり、224、256、384、512ビットの出力ハッシュ長に対して、*r* はそれぞれ1152、1088、832、576となる。[SHA-2](https://ja.wikipedia.org/wiki/SHA-2 "wikilink")シリーズと異なり、SHA-3の関数（固定長を出力する224、256、384、512バージョンおよび可変長出力のSHAKE128およびSHAKE256）は全て同じブロック置換関数を持つ。これらのハッシュ関数を区別するものはパディングとスポンジ関数のパラメータの差のみである。

ハッシュの計算においては、状態を 0 に初期化し、入力をパディングし、それを *r* ビットごとに分割する。入力を状態に吸収するには、*r* ビットごとに分割した入力と状態の排他的論理和を取ってからブロック置換を行う。 最終ブロック置換の後の、状態の先頭の *n* ビットが求めるハッシュ値である。*r* は常に *n* より大きいため、絞り出す過程において更なるブロック置換は不要である。

### パディング

メッセージを *r* ビットごとのブロックに分割するためにはパディングが必要である。SHA-3 では、ビットパターン 100....001 が採用されている。つまり、メッセージの後ろに、1つのビット1、その後に幾つかのビット0（0個から *r - 1* 個まで）、そして最後に1つのビット1を追加する。

パディングの最初と最後のビット1は必須であり、メッセージの長さがすでに *r* で割り切れる場合であっても追加される。\[14\]この場合、*100...001*である長さ *r* のブロックが追加される。 最後のメッセージブロックが *r-1* ビットの場合は、そのブロックに1を追加して *r* ビットとし、さらに*00...001*である長さ *r* のブロックが追加される。 このような処理は、ブロック数が増加するため無駄に見えるかもしれないが、安全性のために必要である。

もし最初のパディングビット1がない場合は、パディングが必要なメッセージのハッシュ値と、「パディングされたかのようなメッセージ」のハッシュ値が同じになってしまう（衝突）。

また、最後のビット1は、異なるレート（異なるハッシュ長）のバリアントに対して安全性を保障するために必要である（マルチレートパディング）。もし最後の1がなければ、一つの短いメッセージに対する2つのハッシュ値（例えば *r=1152* の場合と *r=1088* の場合）が同じになってしまう。

### ブロック置換

この置換は、ワード長を *w* としたとき、*5×5×w* ビットの状態を別の状態に変換する。 [2の冪](../Page/2の冪.md "wikilink")である任意の *w=2<sup>ℓ</sup>* に対して定義されているが、SHA-3においてはワード長は *w=64* (*ℓ= 6*) が使われる。

状態は5×5×*w*ビットのアレイで表現される。*A*\[*x*\]\[*y*\]\[*z*\] はリトルエンディアンに従うと (5*y* + *x*)×*w* + *z* 番目の入力ビットとなる。インデックス演算は、最初の2つの次元に対しては modulo 5、3つめの次元に対しては modulo *w* となる。

基本的なブロック置換関数は5つの副ラウンドからなる 12+2ℓ の繰り返しで構成される。それぞれの副ラウンドは単純なものである（代入形式で記述される場合、入力状態を *A*、出力状態を *A’* とする）。

  - *θ*
    5×*w*（*w* = 64のとき320）ごとの5ビットのカラムの[パリティ](../Page/パリティ.md "wikilink") (この場合、5ビットの排他的論理和) を計算し、さらに隣接する2つのカラムとの排他的論理和を取る。
    *A’*\[*x*\]\[*y*\]\[*z*\] = *A*\[*x*\]\[*y*\]\[*z*\] ⊕ parity(*A*\[*x*-1\]\[0...4\]\[*z*\]) ⊕ parity(*A*\[*x*+1\]\[0...4\]\[*z*−1\])
  - *ρ*
    25ワードごとに異なる[三角数](../Page/三角数.md "wikilink") 0, 1, 3, 6, 10, 15, .... で[ローテートする](https://ja.wikipedia.org/wiki/ビット演算#\(キャリーなし\)ローテート "wikilink")。
    *A*\[0\]\[0\]はローテートせず、出力*A’*にコピーする。それ以外すべての 0≤*t*≤23 に対して、*A’*\[*x*\]\[*y*\]\[*z*\] = *A*\[*x*\]\[*y*\]\[*z*−(*t*+1)(*t*+2)/2\] とする。このとき \(\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 0 & 1 \\ 2 & 3 \end{pmatrix}^t \begin{pmatrix} 1 \\ 0 \end{pmatrix}\) とする。
  - *π*
    25ワードを決まったパターンで置換する。
    *A’*\[*x*\]\[*y*\] = *A*\[*x*+3*y*\]\[*x*\]
  - *χ*
    *a* = *a* ⊕ (¬*b* & *c*) を用いてビット列を結合する。
    *A’*\[*x*\]\[*y*\] = *A*\[*x*\]\[*y*\] ⊕ (¬*A*\[*x*+1\]\[*y*\] & *A*\[*x*+2\]\[*y*\])
    SHA-3においてこの過程のみが非線形操作である。
  - *ι*
    ラウンド定数と状態ワードの排他的論理和を取る。
    ラウンド *i*<sub>*r*</sub> において、0≤*j*≤ℓ のとき *A*\[0\]\[0\]\[2<sup>*j*</sup>−1\] と degree-8 [LFSR](https://ja.wikipedia.org/wiki/線形帰還シフトレジスタ "wikilink") sequenceの *j*+7*i*<sub>*r*</sub> 番目の出力との排他的論理和を取る。これにより他の副ラウンドで保たれていた対称性が破られる。

## 修正

NISTによる公募の期間中、発見された問題への対処として応募者がアルゴリズムを修正することが許されていた。Keccakに加えられた修正は以下の通りである\[15\]\[16\]。

  - セキュリティ向上のためラウンド数が 12+ℓ から 12+2ℓ に増やされた
  - メッセージパディングが、複雑なものから上述のより単純なものに変更された
  - 比率 *r* が、可能な限り大きくされた

## 変更に関する論争

KeccakがSHA-3として選出された後、2013年2月のRSA Conferenceおよび2013年8月のCHESにおいて、NISTはSHA-3標準のセキュリティパラメータとして、キャパシティの大きさを応募時のものから変更するであろうと発表した\[17\]\[18\]。この変更が一時騒動をもたらした。

[ブルース・シュナイアー](https://ja.wikipedia.org/wiki/ブルース・シュナイアー "wikilink")は、アルゴリズムを受け入れるにあたって有害なものであるとしてこの決定を批判した。

一方、Paul Crowleyはこの決定に賛意を表明した。その内容を要約すると以下の通りである。

[ダニエル・バーンスタイン](../Page/ダニエル・バーンスタイン.md "wikilink")は、オリジナルのKeccakで提唱されていたようにキャパシティを576ビットに強化することを提唱した。

Keccakの設計チームは、新しいパラメータに賛意を表明しており、NISTによるパラメータ変更は、NISTのハッシュチームと自分たちによる議論の結果によるものであると表明した\[19\]。しかし、暗号コミュニティに対しては、すべての場合において512ビットのキャパシティを用いることを提唱している\[20\]。

2013年11月、NISTのJohn KelseyはCHESでの発表に対する反応から、近いうち正式に発表する草稿においては、キャパシティの値を応募時のものから変更しない方針であることを明らかにした\[21\]。この方針は、[2014年](../Page/2014年.md "wikilink")4月および5月に続けて公開されたFIPS 202の草稿\[22\]に反映された。また最終的に、キャパシティを含めたハッシュ関数全体は草稿より変更されなかった\[23\]\[24\]。

## ハッシュ値の例

  - SHA3-n および Keccak-n において、n = 224, 256, 384, 512 は出力ハッシュ長である。
  - 固定長出力の SHA-3 においては、メッセージの後、パディングの前に 2 ビット列 01 がメッセージに追加される。
  - キャパシティは出力ハッシュ長の2倍 *c*=2*n* である。
  - 比率は *r*=1600−*c* である。

（以下では、ハッシュ値は十六進法で示している）

空の入力に対するハッシュ値の例：

<span style="color: green;">`Keccak-224("")`
`0x f71837502ba8e10837bdd8d365adb85591895602fc552b48b7390abd`</span>
<span style="color: green;">`Keccak-256("")`
`0x c5d2460186f7233c927e7db2dcc703c0e500b653ca82273b7bfad8045d85a470`</span>
<span style="color: green;">`Keccak-384("")`
`0x 2c23146a63a29acf99e73b88f8c24eaa7dc60aa771780ccc006afbfa8fe2479b2dd2b21362337441ac12b515911957ff`</span>
<span style="color: green;">`Keccak-512("")`
`0x 0eab42de4c3ceb9235fc91acffe746b29c29a8c366b7c60e4e67c466f36a4304c00fa9caf9d87976ba469bcbe06713b435f091ef2769fb160cdab33d3670680e`</span>

<span style="color: green;">`SHA3-224("")`
`0x 6b4e03423667dbb73b6e15454f0eb1abd4597f9a1b078e3f5b5a6bc7`</span>
<span style="color: green;">`SHA3-256("")`
`0x a7ffc6f8bf1ed76651c14756a061d662f580ff4de43b49fa82d80a4b80f8434a`</span>
<span style="color: green;">`SHA3-384("")`
`0x 0c63a75b845e4f7d01107d852e4c2485c51a50aaaa94fc61995e71bbee983a2ac3713831264adb47fb6bd1e058d5f004`</span>
<span style="color: green;">`SHA3-512("")`
`0x a69f73cca23a9ac5c8b567dc185a756e97c982164fe25859e0d1dcc1475c80a615b2123af1f5f94c11e3e9402c3ac558f500199d95b6d3e301758586281dcd26`</span>

入力メッセージのわずかな違いも、出力されるハッシュ値に大きな変化を及ぼす。例えば、メッセージの最後にピリオドを加えた場合：

<span style="color: green;">`SHA3-224("The quick brown fox jumps over the lazy dog")`
`0x d15dadceaa4d5d7bb3b48f446421d542e08ad8887305e28d58335795`</span>
<span style="color: green;">`SHA3-224("The quick brown fox jumps over the lazy dog.")`
`0x 2d0708903833afabdd232a20201176e8b58c5be8a6fe74265ac54db0`</span>

SHA-3 においては、**SHAKE128** および **SHAKE256** と呼ばれる 2 つの可変長出力の関数も追加され、望みのセキュリティ強度に応じて利用可能となる。これらの関数ではキャパシティおよびパディングが SHA-3 のうち固定長を出力するものとは異なる。キャパシティは SHAKE128 では 256 ビット、SHAKE256 では 512 ビットである。メッセージの後、パディングの前に 4 ビット列 1111 がメッセージに追加され、出力は任意長に切りつめられる。追加ビット列のうち最初の 2 ビットは SHAKE と固定長出力の SHA-3 を区別するためのものである、続く 2 ビットは Sakura コーディングスキーム\[25\]のためのものであり、将来的な SHA-3 の拡張の際にそれと区別するためのものとなる。

## SHAシリーズの比較

## 実装ライブラリ

SHA-3をサポートしているライブラリは以下の通り。

  - [Botan](https://ja.wikipedia.org/wiki/Botan "wikilink")
  - [Bouncy Castle](https://ja.wikipedia.org/wiki/:en:Bouncy_Castle_\(cryptography\) "wikilink")
  - [cryptlib](https://ja.wikipedia.org/wiki/:en:Cryptlib "wikilink")
  - [Crypto++](https://ja.wikipedia.org/wiki/:en:Crypto++ "wikilink")
  - [Libgcrypt](https://ja.wikipedia.org/wiki/:en:Libgcrypt "wikilink")
  - [Nettle](https://ja.wikipedia.org/wiki/:en:Nettle_\(cryptographic_library\) "wikilink")
  - [OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")
  - [wolfSSL](https://ja.wikipedia.org/wiki/wolfSSL "wikilink")

## 脚注

## 外部リンク

  - [The Keccak web site](http://keccak.noekeon.org/)
  - [A Java implementation of Keccak](https://github.com/kocakosm/pitaya/blob/master/src/org/kocakosm/pitaya/security/Keccak.java)
  - [A Cryptol implementation of Keccak](http://plaintext.crypto.lo.gy/article/495/untwisted-a-cryptol-implementation-of-keccak-part-1)
  - [VHDL source code developed by the Cryptographic Engineering Research Group (CERG) at George Mason University](http://cryptography.gmu.edu/athena/index.php?id=source_codes)
  - [Erlang NIF implementation based on the NIST reference code](https://github.com/b/sha3)
  - [Keccak implemented in PureBasic](http://www.purebasic.fr/english/viewtopic.php?p=423810#p423810)

<!-- end list -->

1.
2.
3.  「当初の目的」としたほうが正確かもしれない。
4.
5.
6.
7.
8.
9.
10.
11. Keccak implementation overview Version 3.2 <http://keccak.noekeon.org/Keccak-implementation-3.2.pdf>
12.  Keccak is second only to Luffa, which did not advance to the final round.
13. NIST, [Third-Round Report of the SHA-3 Cryptographic Hash Algorithm Competition](http://nvlpubs.nist.gov/nistpubs/ir/2012/NIST.IR.7896.pdf), sections 5.1.2.1（「木」構造）, 6.2（認証付き暗号）, 7（将来標準化されるかもしれない「追加」）
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.