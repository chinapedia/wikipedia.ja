> この記事は[MACCS](https://ja.wikipedia.org/wiki/MACCS)から翻訳されています。


**MACCS**（まっくす）とは**Molecular Design Limited**社（現在の**Elsevier MDL**社の前身）が[1979年](../Page/1979年.md "wikilink")に開発した世界初の商用化学構造データベースである。同社の化学反応データベース**REACCS**やその後継製品である、**MDL ISIS**, **MDL Chemscape**, **MDL Isentris**の中核となる技術はMACCS技術が応用されている。また、その長期間にわたる製品系列の存在から、MACCSのImport/Exportファイルである**MDL Molfile**は、**PDBファイル**等とともに[ケモインフォマティクス](../Page/ケモインフォマティクス.md "wikilink")領域におけるデータ交換フォーマットのデファクトスタンダードの一つとなっている。

## 製品系列

  - **MACCS**（1979年）
      -
        初めて商用化された**化学構造データベース**。スーパーミニコンあるいはメインフレーム上で動作し、グラフィック端末から出入力する。
    <!-- end list -->
      - **REACCS**（1982年）
          -
            MACCS技術を基に構築された初めて商用化された**化学反応データベース**。
      - **MACCS-II**（1984年）
          -
            化学構造のほかにTextの化合物属性を扱うようになる。
      - **MACCS-3D**（1988年）
          -
            **構造式**（2D）の他に**構造モデル**（3D）情報を扱えるようになる。
      - **MACCS-II DBMS Interface Module**（1989年）
          -
            Textの化合物属性の格納先として、RDBSであるOracleの管理下にあるデータと連携するようになる。
  - **MDL ISIS** （1991年）
      -
        **MACCS**/**REACCS**技術を基に開発された**クライアント・サーバ型**化学構造データベース。クライアント側は化学構造式エディターの**ISIS/Draw**、検索機能モジュールの**ISIS/Base**そしてサーバ側の**ISIS/Host**の3つの主要モジュールから構成される。**ISIS/Draw**は単独でMacまたはWindowsのDrawing Toolとしても利用が可能であり、**ISIS/Base**は**ISIS/Host**にくらべ検索機能が劣るが、Local側にスタンドアローンの化学データベースを作成することも可能。
    <!-- end list -->
      - **ISIS Object Library**（1994年）
          -
            **MDL ISIS**/**Base,Draw**のクライアント側ミドルウエア・コンポーネント。
      - 　**MDL Chemscape**/**Chime**（1996年）
          -
            MDL ISISをWeb Application化する為のサーバ側ミドルウエア（**Chemscape**）とWeb Browser Plug-in（**Chime**）。データのUploadが可能なPlug-Inは**Chime Pro**という名称で販売されている。
      - **MDL ISIS/host Relational Chemical Gateway**（1996年）
          -
            ISIS/Hostのデータ構造をOracle Data Cartridge技術でOracle Table内に実装する技術。これの機能による埋め込みSQL文を使用した化学構造検索を提供するモジュールは**ISIS/Direct**と呼ばれる。
      - **MDL Cheshire**
          -
            サーバ層、中間層、クライアント層の内の任意の層で動作するミドルウエアで化学構造式を操作する機能を与える。化学構造式を操作する為の多くの化学的オブジェクトを持つスクリプティング言語であり、多様な化学構造式の処理を可能とする。
  - **MDL Isentris**
      -
        Elsevier MDL社の最新化学データベースシステム。クライアント・サーバ方式を廃し、最新版はMicrosoft .NET/SOAP技術に基づく3階層アプリケーション群の総称である。データベース層にはMDL Direct、中間層にはMDL Core Interface、クライアント層には各[ワークフロー](../Page/ワークフロー.md "wikilink")アプリケーション群（Isentris Client\[MDL Base\]、Notebook、Plate Manager、Registration、Logisticsなど）という構成になっており、各ワークフローアプリケーション間の連携とデータの連携の強化を図る。
  - **MDL Assay Explorer**
      -
        Elsevier MDL社の化合物評価情報管理アプリケーションであり、構造式を含めたReport出力機能、Plate管理システムとの連携、Visual Basic for Applicationを内蔵することによる拡張性の高いアプリケーションである。

## ファイルフォーマット

### molfile

[拡張子](../Page/拡張子.md "wikilink")は**.mol**、[MIMEタイプは](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")**chemical/x-mdl-molfile**。行の幅がメインフレームの入力デバイスに由来する80文字に制限されている。1構造式あたり1ファイルで構成されるので、データのExport/Import用には次の項の**sdfile**などが利用される場合も多い。化学構造の[原子](https://ja.wikipedia.org/wiki/原子 "wikilink")を節、[結合を枝とする](../Page/化学結合.md "wikilink")[グラフ構造で表現され](../Page/グラフ理論.md "wikilink")、入力デバイスに書かれた節点の座標と原子の種別を表すアトムリストと、結合をアトムリストの2つの要素を指定して結合の種別と供に表す結合リストから構成される。3D構造を表すモデル型のmolファイルの場合は入力デバイスの2D座標ではなく、3次元座標が使用される。電荷、ラジカルなどは原子属性データとして原子リストとは別に保持される。molファイルにはいくつかのバージョンが存在し、モデル型が使用できないとか原子リストの上限数が違うなどの上位互換性が保障されていな機能があり、MDL社以外のプログラムが発生させるMDL molに準拠したファイルも定義が曖昧なものが存在するので、バージョンの注意が必要な場合もある。

### sdfile

拡張子は**.sdf**なのでSDFファイルと呼ばれることもある。MIMEタイプは**chemical/x-mdl-sdfile**。mol fileフォーマットを内含する構造になっており、それに続いてTextの化合物属性の見出しとその値が続くようになっている。レコードセパレーターとして"$$$$"が使用される。次の項の**rdfile**と異なり、1レコードに1構造式しか保持できない。

### rdfile

拡張子は**.rdf**なのでRDFファイルと呼ばれることもある。MIMEタイプは**chemical/x-mdl-rdfile**。1レコードあたり複数のmolfileを埋め込むことで、化学反応式を格納できるように拡張されたREACCSのExport/Importファイルである。データフォーマットの基本構造は見出し行（Field名）とその値の対で構成されている。

### skcfile

拡張子は**.skc**なのでSKCファイルと呼ばれることもある。ISIS/Drawの描画情報をBinaryデータとして格納したファイルである。

### ctfile

## 参考資料

  - Symyx社(旧Elsevier MDL社)ホームページ <http://www.mdl.com/>

## 関連項目

  - [化学データベース](https://ja.wikipedia.org/wiki/化学データベース "wikilink")
  - [ケモインフォマティクス](../Page/ケモインフォマティクス.md "wikilink")

[Category:化学データベース](https://ja.wikipedia.org/wiki/Category:化学データベース "wikilink")