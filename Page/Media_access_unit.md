> この記事は[Media access unit](https://ja.wikipedia.org/wiki/Media_access_unit)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:IBM_8226_Multistation_Access_Unit.JPG "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:IBM_8228_Multistation_Access_Unit.JPG "wikilink") **メディアアクセスユニット** （ **MAU** ）は、 **マルチ** **ステーション** **アクセスユニット** （ **MAU**または**MSAU** ）とも呼ばれる。 ステーションを論理リングに接続するために内部的に配線された[トークンリング](../Page/トークンリング.md "wikilink")ネットワークとして、スタートポロジ内の複数のネットワークステーションを接続する集線装置\[1\]。

[トークン・パッシング](https://ja.wikipedia.org/wiki/トークン・パッシング "wikilink")リングは、1997年の時点でIBMネットワーキング製品の主流であった。その後、[スイッチド・ネットワーク](https://ja.wikipedia.org/wiki/スイッチド・ネットワーク "wikilink")に置き換えられていった。

## 長所と短所

### 電源不要のパッシブネットワーキング

[thumb](https://ja.wikipedia.org/wiki/ファイル:8228_setup_aid.JPG "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:8226_relays.JPG "wikilink") IBMが実装したパッシブトークンリングMAUの大部分は、電力を必要とせずに動作している。代わりに、パッシブMAUは一連のリレーを使用し、データが通過するときに自動的に調整される。これが、トークンリングが一般的にリレーを使用して、切断されたポートまたは障害が発生したポートを終端する理由であった。 電力が必要ないIBM 8228マルチステーションアクセスユニットは、ユニットが移動された後にリレーを再調整するために「IBM 8228 Setup Aid」ツールを使用し、リレーを適切な状態にする\[2\]。

MAUが電力なしで動作する利点は、コンセントのないエリアに配置できることであった。欠点は、内部リレーに過剰な力がかかるたびに調整する必要があった。

IBM 8226 MAUは電源を必要とし、主にLEDに使用します。リレーはユニット内で引き続き使用されるため、プライミングは必要なかった\[3\]。

### 帯域幅

理論的には、このネットワーキングテクノロジーは、（リング全周が数km）広い地理的領域をサポートしていた。 但し、すべてのステーションで帯域幅が共有されているため、実際には、より狭いエリアにまたがる個別のネットワークがブリッジを使用して結合されていた。 このブリッジネットワークテクノロジーは、高帯域幅の[スイッチド・ネットワーク](https://ja.wikipedia.org/wiki/スイッチド・ネットワーク "wikilink")に取って代わられた\[4\]。

{{-}}

## 耐障害性

マルチステーションアクセスユニットには、動作していないステーションを短絡させるためのリレーが含まれている。 複数のMAUを、リングイン、リングアウトコネクタを介してより大きなリングに接続できる\[5\]。

MAUは「ボックス内のリング」とも呼ばれ、トークンリングのリングを構成するために使用されていたループが、このデバイスに統合された。 トークンリングでは、リングでリンクが切断されると、ネットワーク全体がダウンする。但し、MAUを使用する事で、壊れた回路は1ms以内に閉じる。リング上のステーションは、ネットワーク全体を無効にすることなく、コードを外すことができる。

## 関連項目

  - [ローカルエリアネットワーク](https://ja.wikipedia.org/wiki/ローカルエリアネットワーク "wikilink")
  - [トークンリング](../Page/トークンリング.md "wikilink")
  - [トークン・パッシング](https://ja.wikipedia.org/wiki/トークン・パッシング "wikilink")

## 脚注

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:ネットワークハードウェア](https://ja.wikipedia.org/wiki/Category:ネットワークハードウェア "wikilink")

1.  <http://ps-2.kev009.com/ohlandl/books/TR_Networks_Intro_Planning_Guide_Chpt1.pdf>
2.  <http://www.mcamafia.de/mcapage0/8228tool.htm>
3.  <ftp://public.dhe.ibm.com/networking/nswww/neteam/998pg/c822602.pdf>
4.
5.