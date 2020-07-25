> この記事は[BLAST](https://ja.wikipedia.org/wiki/BLAST)から翻訳されています。


**BLAST** (**B**asic **L**ocal **A**lignment **S**earch **T**ool) は、[バイオインフォマティクス](../Page/バイオインフォマティクス.md "wikilink")で[DNAの](../Page/デオキシリボ核酸.md "wikilink")[塩基配列](../Page/塩基配列.md "wikilink")あるいは[タンパク質の](https://ja.wikipedia.org/wiki/蛋白質 "wikilink")[アミノ酸](https://ja.wikipedia.org/wiki/アミノ酸 "wikilink")配列の[シーケンスアライメントを行うための](../Page/シーケンスアラインメント.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")をいい、またそのアルゴリズムを[実装](../Page/実装.md "wikilink")した[プログラムをいう](../Page/プログラム_\(コンピュータ\).md "wikilink")。 BLAST を使って、手元にある[シーケンス](https://ja.wikipedia.org/wiki/シーケンス "wikilink")で、[シーケンスデータベース](https://ja.wikipedia.org/wiki/シーケンスデータベース "wikilink")もしくはライブラリに対して検索することにより、ある閾値以上のスコアで類似するシーケンス群を発見することができる。 BLAST は、バイオインフォマティクスで最も広く使われているプログラムの一つである。

## 概要

BLAST は、[バイオインフォマティクス](../Page/バイオインフォマティクス.md "wikilink")において、[DNAの](../Page/デオキシリボ核酸.md "wikilink")[塩基配列](../Page/塩基配列.md "wikilink")あるいは[タンパク質の](https://ja.wikipedia.org/wiki/蛋白質 "wikilink")[アミノ酸](https://ja.wikipedia.org/wiki/アミノ酸 "wikilink")配列の[シーケンス](https://ja.wikipedia.org/wiki/シーケンス "wikilink")で、ペアワイズの[シーケンスアライメントを行う](../Page/シーケンスアラインメント.md "wikilink")。 BLAST は、主にシーケンスの局所的アライメント（ローカルアライメント）を行うために使われる。 BLAST と同様にペアワイズアライメントを行うための[プログラムとしては](../Page/プログラム_\(コンピュータ\).md "wikilink")、他に [FASTA](../Page/FASTA.md "wikilink") などがある。 また、マルチプルアライメントを行うためのプログラムとしては、[Clustal](../Page/Clustal.md "wikilink") (ClustalW、ClustalX) などがある。

BLAST は、バイオインフォマティクスで最も広く使われているプログラムの一つである。 BLAST が広く使われている理由は、BLAST が処理速度を非常に重視していることにあるとみられる。 BLAST の[アルゴリズム](../Page/アルゴリズム.md "wikilink")は正確さより速度を重視している。 BLAST におけるこの速度重視によって、今日では膨大なデータが蓄積されている[ゲノム](../Page/ゲノム.md "wikilink")の[シーケンスデータベース](https://ja.wikipedia.org/wiki/シーケンスデータベース "wikilink")に対して検索を行うような場合において、BLAST アルゴリズムを実用的なものとしている。 BLAST が開発された後、BLAST より速いアルゴリズムがいくつか開発されている。 BLAST は、大まかなシーケンスマッチングを必要とする他のアルゴリズムの一部としてもよく使われている。

BLAST を使うことで、例えば、[ハツカネズミ](../Page/ハツカネズミ.md "wikilink")の未知の[遺伝子](https://ja.wikipedia.org/wiki/遺伝子 "wikilink")を発見したときに、[ヒト](../Page/ヒト.md "wikilink")がそのシーケンスと類似した遺伝子をもつかどうかを調べることができる。 ハツカネズミの未知のシーケンスで BLAST を使って、[ヒトゲノム](../Page/ヒトゲノム.md "wikilink")のシーケンス[データベース](../Page/データベース.md "wikilink")に対して検索を行うと、BLAST は類似性の高いシーケンス群を見つけ出す。

また、BLAST は次のような問いを考えるときに使うことができる。

  - 手元のタンパク質のアミノ酸配列は、どの[バクテリアと系統的に関係があるか](https://ja.wikipedia.org/wiki/真正細菌 "wikilink")?
  - 今シーケンシングして得られたDNAは、どの種に由来するか?
  - 自分が決定した構造（もしくは構造[モチーフ](https://ja.wikipedia.org/wiki/モチーフ "wikilink")）をもつタンパク質を記録した、他の遺伝子はあるか?

BLASTアルゴリズムおよびそのアルゴリズムを実装したプログラムは、次の人々によって開発された。

  - Stephen Altschul（[NCBI](https://ja.wikipedia.org/wiki/NCBI "wikilink"); 米国生物工学情報センター）
  - Warren Gish (NCBI)
  - David Lipman (NCBI)
  - Webb Miller（[ペンシルベニア州立大学](../Page/ペンシルベニア州立大学.md "wikilink")）
  - Gene Myers（[アリゾナ大学](../Page/アリゾナ大学.md "wikilink")）

BLASTアルゴリズムを実装したプログラムは複数存在する。 それぞれダウンロードして利用することができる。 オリジナルの実装は NCBI BLAST である。

  - NCBI BLAST <http://www.ncbi.nlm.nih.gov/BLAST/>
      - ライセンス: [パブリックドメイン](../Page/パブリックドメイン.md "wikilink")
      - 動作環境: [UNIX](../Page/UNIX.md "wikilink")/[Linux](../Page/Linux.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - WU-BLAST <http://blast.wustl.edu/>
      - ライセンス: 学術もしくは非営利の用途の場合は無料、商用利用の場合は有料
      - 動作環境: UNIX/Linux、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
  - FSA-BLAST <http://www.fsa-blast.org/>
      - ライセンス: [BSDライセンス](../Page/BSDライセンス.md "wikilink")
      - 動作環境: UNIX/Linux、[Power Mac](../Page/Power_Mac.md "wikilink") G5

BLASTは [NCBI](https://ja.wikipedia.org/wiki/NCBI "wikilink") ([GenBank](../Page/GenBank.md "wikilink")) や[DDBJ](../Page/DDBJ.md "wikilink")の[ウェブ上でも利用することができる](../Page/World_Wide_Web.md "wikilink")。

  - NCBI <http://www.ncbi.nlm.nih.gov/BLAST/>
  - DDBJ <http://www.ddbj.nig.ac.jp/search/blast-j.html>

BLASTのオリジナルの論文 "Altschul, SF, W Gish, W Miller, EW Myers, and DJ Lipman. Basic local alignment search tool. J Mol Biol 215(3):403-10, 1990." は、1990年代に非常に多くの論文で引用された。

## BLASTアルゴリズム

BLAST[アルゴリズム](../Page/アルゴリズム.md "wikilink")を実行する際には、2つの情報が必要である。 クエリ[シーケンス](https://ja.wikipedia.org/wiki/シーケンス "wikilink")（ターゲットシーケンスともいう）と[シーケンスデータベース](https://ja.wikipedia.org/wiki/シーケンスデータベース "wikilink")である。 BLASTアルゴリズムは、シーケンス[データベース](../Page/データベース.md "wikilink")中のシーケンス断片と類似するクエリシーケンス中のシーケンス断片を見つけ出す。 多くの場合、クエリシーケンスは、シーケンスデータベースと比べてデータ量が非常に小さい。 例えば、クエリシーケンスが千個程度の[ヌクレオチド](https://ja.wikipedia.org/wiki/ヌクレオチド "wikilink")（[核酸塩基](https://ja.wikipedia.org/wiki/核酸塩基 "wikilink")）であるのに対し、シーケンスデータベースは数億のヌクレオチドのデータをもっている場合がある。

BLASTアルゴリズムは、クエリシーケンスとシーケンスデータベースとの間で、高い閾値で[シーケンスアライメントを行う](../Page/シーケンスアラインメント.md "wikilink")。 その際には Smith-Waterman アルゴリズムに近似したヒューリスティクなアルゴリズムが使われる。 完全な Smith-Waterman アルゴリズムは、[NCBI](https://ja.wikipedia.org/wiki/NCBI "wikilink") [GenBank](../Page/GenBank.md "wikilink") のような大規模なシーケンスデータベースに対して検索を行う場合には、処理速度が非常に遅いことが問題となる。 BLASTアルゴリズムは、Smith-Waterman アルゴリズムより少し正確さで劣るが、50倍以上の処理速度を実現する。 このようにBLASTアルゴリズムは、高速でありかつ比較的正確であるという特徴がある。 こうした特徴が、BLASTアルゴリズムの重要な技術的革新性であり、またおそらく[バイオインフォマティクス](../Page/バイオインフォマティクス.md "wikilink")においてBLASTプログラムが最もよく使われている理由となっている。

BLASTアルゴリズムの実行は、概念的には次に述べるように3段階に分かれている。

  - 第1段階: クエリシーケンスを短い固定長データに分割した断片で、シーケンスデータベースを厳密に検索する。この固定長データの長さを W（ワード）とする。例えば、W = 3 で、クエリシーケンス AGTTAC に対してデータベース中に ACTTAG というシーケンスが存在した場合、BLASTアルゴリズムは、TTA という部分データが両シーケンスで共有されていると認識する。W のサイズは、特に指定しない場合、ヌクレオチドでは11、アミノ酸では3である。
  - 第2段階: BLASTアルゴリズムは、クエリシーケンスと、部分データを共有すると認識したデータベース中のシーケンス群に対して、ギャップを考慮しない単純なアライメントを行う。このギャップを考慮しないアライメントは、第1段階の W の長さの固定長での検索処理を、アライメントのスコアが高くなるように両方向に W（ワード）のサイズを拡張した処理である。この段階ではヌクレオチド（核酸塩基）やアミノ酸の挿入や欠損は考慮しない。先述の例では、AGTTAC と ACTTAG はそれぞれ TTA を共に含んでおり、ギャップを考慮しないアライメントは次のようになる。
      -
        `..AGTTAC..`
        `  | ||| `
        `..ACTTAG..`

第2段階で、ギャップを考慮せずに、スコアの高いアライメントが行えた場合、データベースのシーケンスデータは第3段階の処理対象となる。

  - 第3段階: BLASTアルゴリズムは、Smith-Waterman アルゴリズムの変形版アルゴリズムで、クエリシーケンスとデータベースのシーケンスの間で、ギャップを考慮したアライメントを行う。アライメントを行った後、統計的に有意なアライメント群がユーザに示される。

BLASTから派生したアルゴリズムがいくつか考案されている。

  - BLAT
    BLAT (**B**last **L**ike **A**lignment **T**ool) は、BLASTを上回る速度で処理を行うが、正確さにおいてはBLASTに 劣る。ヌクレオチドのシーケンスでゲノムデータベースへの検索を行う。
  - BLASTZ
    複数の大規模なゲノムデータベースや染色体データベースに対して検索を行うよう設計されたアルゴリズム。

### 並列処理・分散処理への対応

[並列処理](https://ja.wikipedia.org/wiki/並列処理 "wikilink")や[分散処理](https://ja.wikipedia.org/wiki/分散処理 "wikilink")の環境に対応したBLAST[アルゴリズム](../Page/アルゴリズム.md "wikilink")がいくつか考案されている。 こうしたアルゴリズムは一般に Parallel BLAST と呼ばれることがある。 Parallel BLAST は、[Pthreads](https://ja.wikipedia.org/wiki/Pthreads "wikilink")や[MPIの](../Page/Message_Passing_Interface.md "wikilink")[APIを使って実装される](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。 多くのコンピュータプラットフォームに移植され、[Linux](../Page/Linux.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[AIX](../Page/AIX.md "wikilink")などで利用可能である。 BLASTアルゴリズムを並列処理や分散処理に対応させる手法には次のようなものがある。

  - 分散クエリ
  - ハッシュテーブルの分割
  - 計算処理の並列化
  - [データベースの分割](https://ja.wikipedia.org/wiki/分割_\(データベース\) "wikilink")

## BLASTプログラム

BLAST[プログラムを利用するには](../Page/プログラム_\(コンピュータ\).md "wikilink")、プログラムをダウンロードして blastall コマンドラインユーティリティとして実行する方法と、[ウェブからアクセスする方法とがある](../Page/World_Wide_Web.md "wikilink")。

[NCBI](https://ja.wikipedia.org/wiki/NCBI "wikilink") ([GenBank](../Page/GenBank.md "wikilink")) や[DDBJ](../Page/DDBJ.md "wikilink")のウェブサイトでは、これらの機関が共同で構築している[塩基配列](../Page/塩基配列.md "wikilink")（および[アミノ酸](https://ja.wikipedia.org/wiki/アミノ酸 "wikilink")配列）の公共[シーケンスデータベース](https://ja.wikipedia.org/wiki/シーケンスデータベース "wikilink")に対して、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")でBLASTによる類似性検索を行うことができる。 この公共シーケンス[データベース](../Page/データベース.md "wikilink")は定期的に更新され、新たに配列決定が行われた生物のシーケンスのほとんどは、このデータベースに登録される。

BLASTには実際には複数のプログラムが含まれている。 blastall 実行ファイルには、blastp、blastn、blastx、tblastn、tblastx のプログラムが含まれている。 blastall をコマンドライン環境で実行する際は、-p オプションで実行するプログラムを指定する（例: blastall -p blastn）。 BLASTプログラムを実行する際、クエリシーケンスは[FASTA](../Page/FASTA.md "wikilink")フォーマットでプログラムに渡す。 次にBLASTに含まれているプログラムのうち主なものを示す。

  - blastp
    アミノ酸配列（[タンパク質の](https://ja.wikipedia.org/wiki/蛋白質 "wikilink")[シーケンス](https://ja.wikipedia.org/wiki/シーケンス "wikilink")）をクエリとして、ユーザが指定したアミノ酸配列データベースから類似するシーケンスを検索する。
  - blastn
    塩基配列（[ヌクレオチド](https://ja.wikipedia.org/wiki/ヌクレオチド "wikilink")のシーケンス）をクエリシーケンスとして、ユーザが指定した塩基配列データベースから類似するシーケンスを検索する。
  - blastx
    塩基配列のクエリシーケンスを、6フレームで翻訳して、アミノ酸配列データベースから類似するシーケンスを検索する。
  - tblastn
    アミノ酸配列をクエリとして、塩基配列データベースを6フレームで翻訳しながら、類似するシーケンスを検索する。
  - tblastx
    塩基配列のクエリシーケンスを、6フレームで翻訳して、アミノ酸配列に翻訳された塩基配列データベースから類似するシーケンスを検索する。このプログラムはBLASTのプログラムの中で最も処理速度が遅い。このプログラムの使用目的は、塩基配列のシーケンス間の非常に遠い関連性を発見することである。
  - PSI-BLAST
    アミノ酸配列をクエリとして、ユーザが指定したアミノ酸配列データベースから類似するシーケンスを検索する。最近開発されたBLASTプログラムの一つ。このプログラムはタンパク質の遠い系統的関連性を発見するために使われる。まず、クエリのアミノ酸配列と近い関連性をもつタンパク質の一覧を作成する。そしてこの一群のタンパク質を統合して「プロファイル」（平均化したシーケンスのようなもの）を作る。このプロファイルを使ってアミノ酸配列データベースに対する検索を行い、プロファイルのもととなったアミノ酸配列より多い件数のアミノ酸配列を見つける。見つかったアミノ酸配列でさらにプロファイルを作成する。この一連の処理を繰り返し行う。検索を行う際に関連するタンパク質を考慮するため、遠い系統的関連性を発見する場合に、PSI-BLAST は blastp よりもはるかに正確な処理を行う。
  - megablast
    megablastは大量のクエリシーケンスで高速な検索を行うプログラムである。BLAST でコマンドラインから逐次に検索を行う場合より、はるかに高速に実行することができる。megablastはクエリとして指定された複数のシーケンスを連結して長いシーケンスを作成して、シーケンスデータベースを検索し、処理結果として個別のアライメントと統計値を返す。

## 参考文献

  - Cynthia Gibas、Per Jambeck、水島洋 (監修・訳) 、明石浩史 (訳) 、 ま たぬき (訳) 『実践 バイオインフォマティクス』 [オライリー・ジャパン](../Page/オライリー・ジャパン.md "wikilink")、2002年 ISBN 4-87311-068-8 7章

## 外部リンク

  - [NCBI BLAST ウェブサイト](http://www.ncbi.nlm.nih.gov/BLAST/) - [米国生物工学情報センター (NCBI)](https://ja.wikipedia.org/wiki/NCBI "wikilink")
  - [NCBI BLAST チュートリアル](http://www.ncbi.nlm.nih.gov/Education/BLASTinfo/tut1.html)
  - [DDBJ (BLAST検索)](http://www.ddbj.nig.ac.jp/search/blast-j.html) - [日本DNAデータバンク (DDBJ)](../Page/DDBJ.md "wikilink")
  - [WU-BLAST](http://blast.wustl.edu/) - BLAST のもう一つの実装。ワシントン大学の Warren Gish などの人々が開発し維持管理している。
  - [FSA-BLAST](http://www.fsa-blast.org/) - 最近開発された BLAST のもう一つの実装。アルゴリズムを改良し、NCBI BLAST と同等の正確さでより高速に処理を行う。

<!-- end list -->

  - [Massively Parallel BLAST for the Blue Gene/L](http://www-users.cs.umn.edu/~rangwala/final_bglBLAST.pdf) - [Blue Gene/Lなどの](../Page/Blue_Gene.md "wikilink")[並列処理](https://ja.wikipedia.org/wiki/並列処理 "wikilink")環境のBLASTの論文 (PDF)
  - [BLAST HOWTO](http://wikiomics.org/wiki/BLAST) - [Wikiomics bioinformatics wiki](http://wikiomics.org) の文書
  - [A/G BLAST](http://developer.apple.com/darwin/projects/blast/) - [PowerPC](../Page/PowerPC.md "wikilink") G4/G5 [プロセサ](../Page/CPU.md "wikilink") の [Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") 向けの BLAST

[Category:バイオインフォマティクス・アルゴリズム](https://ja.wikipedia.org/wiki/Category:バイオインフォマティクス・アルゴリズム "wikilink")