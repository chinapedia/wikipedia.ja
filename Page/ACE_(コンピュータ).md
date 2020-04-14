> この記事は[ACE \(コンピュータ\)](https://ja.wikipedia.org/wiki/ACE_\(コンピュータ\))から翻訳されています。


**ACE**（エース、***A**utomatic **C**omputing **E**ngine*）は、[1946年](../Page/1946年.md "wikilink")に[アラン・チューリング](../Page/アラン・チューリング.md "wikilink")が設計した[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の初期の[コンピュータ](../Page/コンピュータ.md "wikilink")である。

1946年2月19日、チューリングは[国立物理学研究所](https://ja.wikipedia.org/wiki/イギリス国立物理学研究所 "wikilink")(NPL)運営委員会に世界初のプログラム内蔵式コンピュータの完全な設計に関する論文を提出した。他の同時期のコンピュータと異なり ACEはチューリングが単独で設計したもので、[EDVAC](../Page/EDVAC.md "wikilink")に関する[ジョン・フォン・ノイマン](../Page/ジョン・フォン・ノイマン.md "wikilink")の[草稿の影響を受けていない](https://ja.wikipedia.org/wiki/EDVACに関する報告書の第一草稿 "wikilink")。ただし、これに対して全く逆の解釈をとる者もいる。

NPLの数学部門にはコンピュータを実際に製作する能力がなかったため、通信研究所(TRE)に製作を依頼した。しかし、TREは戦後の電話網の復興に忙しく、世論もACE開発には批判的であった。このためチューリングは1947年にNPLを去った。しかし、ACEは国家プロジェクトであったため中止することもできず、[ジェームズ・H・ウィルキンソン](../Page/ジェームズ・H・ウィルキンソン.md "wikilink")がプロジェクトを引き継ぎ、がこれを補佐した。[1950年](../Page/1950年.md "wikilink")にはプロトタイプの **Pilot ACE** が完成し、[1957年](../Page/1957年.md "wikilink")にはようやく ACE が完成する。しかし、完成したときにはACEはすでに時代遅れとなっていた。

## 特徴

[Pilot_ACE3.jpg](https://ja.wikipedia.org/wiki/File:Pilot_ACE3.jpg "fig:Pilot_ACE3.jpg") **Pilot ACE**は約800本の[真空管](../Page/真空管.md "wikilink")から構成され、[水銀遅延線](https://ja.wikipedia.org/wiki/水銀遅延線 "wikilink")メモリを[主記憶装置](../Page/主記憶装置.md "wikilink")として使用した。メモリは当初 32[ビット](../Page/ビット.md "wikilink")×128[ワード](../Page/ワード.md "wikilink")であったが、後に 352ワードに拡張されている。また、4096ワードの[磁気ドラムメモリ](../Page/磁気ドラムメモリ.md "wikilink")が1954年に追加されている。基本動作周波数は 1MHzであり、当時のイギリスのコンピュータでは最速である。遅延線メモリを使用しているため、命令実行時間はその遅延に依存する。例えば加算は 64マイクロ秒から1024マイクロ秒までの時間がかかる可能性がある。チューリングの命令セットでは必ず次の命令のアドレスを指定するようになっており、これはつまりプログラムをアドレス順に命令を配置する現在の方法とは異なっていて、ある命令を実行するときにちょうど遅延線メモリからそのアドレスの内容が取り出せるように命令とデータを配置することで高速化を図る方式（最適タイミング方式）であった。

**ACE** は 48ビットワードである。約7000本の真空管と水銀遅延線メモリから構成されている。乗算時間は約448マイクロ秒である。チューリングの ACE に関する報告書は1945年には完成しており、詳細な回路図も含まれていた。開発費用は1万1200ポンドと見積もられていた。EDVAC にはない特徴として、サブルーチン呼び出しを実装していた点が挙げられる。また、*Abbreviated Computer Instructions* という初期のプログラミング言語もあった。

## その後の影響

Pilot ACE は、English Electric社によって製品化され DEUCE という名前で販売された。また、チューリングのもとにいた[ハリー・ハスキー](https://ja.wikipedia.org/wiki/ハリー・ハスキー "wikilink")は1950年代にアメリカで ACE のアーキテクチャを受け継いだ [Bendix G-15を発売した](../Page/Bendix_G-15.md "wikilink")。Bendix G-15の特徴のひとつに、磁気ドラムメモリの特定のトラックの一部分を使い、常にデータを読み出してはそれを書き戻すようにして、任意の容量の遅延線メモリのようにして使っていた、ということが挙げられる。これは最適タイミング方式を受け継いだものであった。G-15は日本に初めて輸入されたコンピュータでもあり、後の日本製コンピュータに影響を与えている。特に、最初の輸入先の\[1\]国鉄では、直後に設計され実用運用された座席予約システム[マルスの](../Page/マルス_\(システム\).md "wikilink")「MARS 1」への影響が大きいことが指摘されている\[2\]。

## 参考文献

  - 『甦るチューリング －コンピュータ科学に残された夢－』星野力（著）、[NTT出版](../Page/NTT出版.md "wikilink")（2002年）、ISBN 4-7571-0079-5
  - 『コンピュータの発明 エンジニアリングの軌跡』能澤徹（著）、テクノレビュー（2003年）、ISBN 4-902403-00-5
  - B. J. Copeland (Ed.), 2005. *Alan Turing's Automatic Computing Engine*. OUP, Oxford. ISBN 0-19-856593-3.
  - B. E. Carpenter, R. W. Doran, 1986. *A. M. Turing's ACE Report of 1946 and Other Papers*. MIT Press, Cambridge.
  - David M. Yates, 1997. *Turing's Legacy: A History of Computing at the National Physical Laboratory, 1945-1995*. Science Museum, London.
  - Simon H. Lavington, 1980. *Early British Computers: The Story of Vintage Computers and The People Who Built Them*. Manchester University Press.
  - J. H. Wilkinson, 1980. *Turing's Work at the National Physical Laboratory and the Construction of Pilot ACE, DEUCE and ACE*. In N. Metropolis, J. Howlett, G.-C. Rota, (Eds.), *A History of Computing in the Twentieth Century*, Academic Press, New York, 1980.

## 脚注

## 外部リンク

  - [Events in the history of NPL - ACE computer](http://www.npl.co.uk/about/historical_events/1952.html)

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:1940年代のコンピュータ](https://ja.wikipedia.org/wiki/Category:1940年代のコンピュータ "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink") [Category:真空管式コンピュータ](https://ja.wikipedia.org/wiki/Category:真空管式コンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink") [Category:イギリスの科学技術](https://ja.wikipedia.org/wiki/Category:イギリスの科学技術 "wikilink") [Category:アラン・チューリング](https://ja.wikipedia.org/wiki/Category:アラン・チューリング "wikilink")

1.  他にも三菱などに設置された
2.  『模倣から創造へ：国鉄座席予約システムMARS-1における技術革新』