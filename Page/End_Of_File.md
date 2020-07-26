> この記事は[End Of File](https://ja.wikipedia.org/wiki/End_Of_File)から翻訳されています。


[コンピューティング](../Page/コンピューティング.md "wikilink")において、**End Of File**（エンド・オブ・ファイル、略称:**EOF**\[1\]）とは、[ファイルや](../Page/ファイル_\(コンピュータ\).md "wikilink")[ストリームにおいて](../Page/ストリーム_\(プログラミング\).md "wikilink")、それより先に読み出すデータが存在しない（終端である）ことを示す状態のことである。

[標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")では、[getchar](https://ja.wikipedia.org/wiki/getchar "wikilink")のような文字を読み取る関数は、ファイルやストリームの終端を読み取った時に、シンボル値（マクロ） `EOF` に等しい値を返す。`EOF` の実際の値は実装に依存するが（ただし、[GNU Cライブラリなど](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")、一般的には -1 が使用される\[2\]）、文字を示す全てのコードと異なる値で示される。fgets()は[ヌルポインタ](https://ja.wikipedia.org/wiki/ヌルポインタ "wikilink")が返るなど、同じ言語においても様々である。

データをシーケンシャルアクセスしていって、最後のデータまで読み込んだ場合（あるいは、さらに次のデータを読み込もうとした後に\[3\]）、EOFが発生する。[read](https://ja.wikipedia.org/wiki/read "wikilink")などのブロックを読み取る関数は、戻り値として読み取った[バイト数を返し](../Page/バイト_\(情報\).md "wikilink")、これが要求したバイト数よりも少ない場合は、EOFが発生したかエラーが発生したことを示す（どちらが発生したかは、`errno`を確認するか、`ferror`などの専用の関数を使用することで知ることができる）。

[データベース](../Page/データベース.md "wikilink")において与えられた条件に合うデータが存在しない場合、EOFとなる。EOFの判定方法は処理系により異なる。

## EOF文字

端末からの入力は、（デバイスが切断されない限り）実際には「終了」することはないが、端末に複数の「ファイル」を入力することができるように、入力の終了を示すためのキー配列が予約されている。[UNIX](../Page/UNIX.md "wikilink")では、キーストロークのEOFへの変換はターミナルドライバによって行われるため、プログラムはターミナルを他の入力ファイルと区別する必要がない。デフォルトでは、ドライバは行頭の[Control-DをEOFに変換する](https://ja.wikipedia.org/wiki/伝送終了文字 "wikilink")。実際のControl-D（ASCIIコード04）を入力ストリームに挿入するには、ユーザは"quote"コマンド文字 (通常はControl-V) を前に付ける。では、Control-Dの代わりにControl-\\を使用する。

[DOS](../Page/DOS_\(OS\).md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")、[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")や、多くの[DECオペレーティングシステム](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")（[RT-11](https://ja.wikipedia.org/wiki/RT-11 "wikilink")、[VMSなど](../Page/OpenVMS.md "wikilink")）では、端末からの読み込みでEOFが発生することはない。その代わり、プログラムはソースが端末（または他の「文字デバイス」）であることを認識し、予約された文字やシーケンスをEOFとして解釈する。一般的には、[ASCII](../Page/ASCII.md "wikilink")コード26の[Control-ZがEOFとして解釈される](https://ja.wikipedia.org/wiki/置換文字 "wikilink")。

一部のDOSシェル（[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")）やOSのユーティリティプログラム（[EDLIN](../Page/EDLIN.md "wikilink")など）を含むいくつかのMS-DOSプログラムは、テキストファイル内のControl-Zを意味のあるデータの終わりを示すものとして扱い、テキストファイルの書き込みの際にControl-Zを最後に追加する。これは次の2つの理由で行われた。

  - CP/Mとの後方互換性のため。CP/Mの[ファイルシステム](../Page/ファイルシステム.md "wikilink")では、128バイト長のレコードの倍数でしかファイルの長さを記録していなかったため、ファイルがレコードの途中で終わった場合、意味のあるデータの終わりをマークするためにControl-Zが使用されていた。MS-DOSのファイルシステム([FAT](../Page/File_Allocation_Table.md "wikilink"))では常にファイルの正確なバイト長を記録しているので、MS-DOSではこのようにする必要はなかった。
  - プログラムが入力を読み取る際に、端末とテキストファイルの両方で同じコードを使用することができるようにするため。

## テープマーク

ANSI X3.27-1969の[磁気テープ](../Page/磁気テープ.md "wikilink")規格では、ファイルの終わりは**テープマーク**(tape mark)で示されていた。これは、約3.5インチのテープのギャップに続けて、の場合は0x13（16進数）、の場合は17（8進数）という文字を含む1バイトで構成されていた\[4\]。**end-of-tape**は一般的に**EOT**と略され、2つのテープマークで示された。これは[IBM 360などで使用されていた規格である](https://ja.wikipedia.org/wiki/IBM_360 "wikilink")。テープの物理的な終了が迫っていることを知らせるために使用された反射ストリップは、EOTマーカーとも呼ばれていた。

## 脚注

<references/>

## 関連項目

  - [番兵](../Page/番兵.md "wikilink")

  - [伝送終了文字](https://ja.wikipedia.org/wiki/伝送終了文字 "wikilink")(Control-D)

  - [置換文字](https://ja.wikipedia.org/wiki/置換文字 "wikilink")(Control-Z)

  -
  - [ヒアドキュメント](https://ja.wikipedia.org/wiki/ヒアドキュメント "wikilink")

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink") [Category:ファイル_(コンピュータ)](https://ja.wikipedia.org/wiki/Category:ファイル_\(コンピュータ\) "wikilink")

1.
2.  <https://www.gnu.org/software/libc/manual/html_mono/libc.html#EOF-and-Errors>
3.  最後まで到達していても、次のデータを読み込もうとしてエラーになるまでは End of File にならない、という振舞はわかりにくい。 <http://c-faq.com/stdio/feof.html> を参考のこと。
4.  <https://www.loc.gov/marc/specifications/specexchtape2.html#mark>