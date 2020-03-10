> この記事は[Solaris Volume Manager](https://ja.wikipedia.org/wiki/Solaris_Volume_Manager)から翻訳されています。


**Solaris Volume Manager**(**SVM**:siv-em と発音[1](http://blogs.sun.com/andresblog/entry/a_bit_of_svm_history))は [SUNが独自に追加した](../Page/サン・マイクロシステムズ.md "wikilink")[論理ボリュームマネージャ](../Page/論理ボリュームマネージャ.md "wikilink")(LVM)である。Solaris 9 から OS に統合されている。統合以前は Online:DiskSuite(Solaris 2.4 まで)、Solstice DiskSuite(Solaris 2.5 ～ Solaris 8) という名称であった。

システムディスクにおいては[SVR4](https://ja.wikipedia.org/wiki/SVR4 "wikilink")のディスク[パーティション](https://ja.wikipedia.org/wiki/パーティション "wikilink")の管理単位である1ディスク7パーティションの制約を越えることができず、システムディスクのパーティションを自由に設定できる他の商用UNIX管理者から、機能不足や役割不足を指摘されている。(Solaris 9 に付属の SVM 以降は、ソフトパーティションという機能で単一ディスクパーティションや論理ボリュームを、1000以上の数のパーティションに分割することが可能となっている。)

当然、LVM配下のBoot領域からのIPL動作もできないため、Boot領域もSVMの管理対象外である。

また、LVMの基本機能の一つである「外部ストレージへのアクセスパスを複数持ち、パス障害時にアクセス経路を切り替える」マルチパス機能を持っておらず、高可用クラスターとしての運用ができないなど、非常に中途半端で使用用途が限定されたものであったが、Solaris 2.6 向けにリリースされた DiskSuite 4.2 より Alternate Pathing としてサポートされている(このバージョンより 64bit カーネルがサポートされた)。

そのため、SUNサーバにてクラスターを組む際には、[VERITAS](../Page/VERITAS.md "wikilink") Volume ManagerやCluster Serverを別途購入し導入する必要がある。

※この技術情報は、SUN Japanからあるユーザへの公式な回答に基づいて書かれました。

## 関連項目

  - [論理ボリュームマネージャ](../Page/論理ボリュームマネージャ.md "wikilink")
  - [ファイルシステム](../Page/ファイルシステム.md "wikilink")
  - [VERITAS File System](https://ja.wikipedia.org/wiki/VERITAS_File_System "wikilink")
  - [Unix File System](https://ja.wikipedia.org/wiki/Unix_File_System "wikilink")
  - [ZFS](../Page/ZFS.md "wikilink")

[Category:補助記憶装置](https://ja.wikipedia.org/wiki/Category:補助記憶装置 "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink")