> この記事は[Vrsn-end-of-zone-marker-dummy-record.root](https://ja.wikipedia.org/wiki/Vrsn-end-of-zone-marker-dummy-record.root)から翻訳されています。


**vrsn-end-of-zone-marker-dummy-record.root**とは、かつて使用されていた[DNSルートゾーン](https://ja.wikipedia.org/wiki/DNSルートゾーン "wikilink")の[ドメインネーム](https://ja.wikipedia.org/wiki/ドメインネーム "wikilink")リスト中にある、診断用マーカーである。ルートゾーンの末尾にあるため、[ルートネームサーバ](https://ja.wikipedia.org/wiki/ルートネームサーバ "wikilink")からのロードが不完全だとこのドメインは読み込まれない。このドメイン名が.rootを代表する[トップレベルドメイン](../Page/トップレベルドメイン.md "wikilink")だという主張もあるが、技術的にはそのような委任団体は存在しない。

[root zoneファイル](http://www.internic.net/zones/root.zone)によると、当初は**vrsn-end-of-zone-marker-dummy-record.root**だったが、2006年に**vrsn-end-of-zone-marker-dummy-record**に置き換わり、2006年後半に元の**vrsn-end-of-zone-marker-dummy-record.root**に戻った。

2010年に DNSSEC のルートサーバーへの導入に伴い、廃止された\[1\]\[2\]。 従来は **vrsn-end-of-zone-marker-dummy-record.root** エントリの存在の有無によって、DNSルートゾーンが最後まで読み込まれたかを確認していたが、 DNSSEC によりゾーンの完全性を確認できるようになり、不要となったためである。

過去には、ルートサーバーへのドメイン名のTXTレコードの問い合わせによって、存在を確認することができた。例えば、digコマンドで問い合わせするときは、

`dig vrsn-end-of-zone-marker-dummy-record.root in any`

Windowsの[nslookup](https://ja.wikipedia.org/wiki/nslookup "wikilink")コマンドで問い合わせするときは、

`nslookup -type=any vrsn-end-of-zone-marker-dummy-record.root`

と入力すればよかった。

このエントリは"plenus"という語を返した。"plenus"とは[ラテン語](../Page/ラテン語.md "wikilink")で"満たされた"とか"完全な"という意味である。これは、ゾーンファイルの末端を示す印であった。

また、.rootドメインは[Open Root Server Networkのルートゾーンで](https://ja.wikipedia.org/wiki/Open_Root_Server_Network "wikilink")**ORSN-END-OF-ZONE-MARKER-DUMMY-RECORD.ROOT**という形で見ることができる。このエントリは"europe"と返す。

## 脚注

[sv:Toppdomän\#Generiska toppdomäner](https://ja.wikipedia.org/wiki/sv:Toppdomän#Generiska_toppdomäner "wikilink")

[Category:疑似トップレベルドメイン](https://ja.wikipedia.org/wiki/Category:疑似トップレベルドメイン "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.