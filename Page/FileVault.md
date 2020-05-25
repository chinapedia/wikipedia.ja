> この記事は[FileVault](https://ja.wikipedia.org/wiki/FileVault)から翻訳されています。


**FileVault**（ファイルヴォールト）とは、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")に搭載されているディスク暗号化機能である。[Mac OS X v10.3で初めて搭載され](../Page/Mac_OS_X_v10.3.md "wikilink")、[Mac OS X LionでバージョンアップされてFileVault](https://ja.wikipedia.org/wiki/Mac_OS_X_Lion "wikilink")2となった。[Vaultとは英語でアーチ状の堅固な建築物を意味する](../Page/ヴォールト.md "wikilink")。

## FileVault

[Mac OS X v10.3で搭載されたバージョン](../Page/Mac_OS_X_v10.3.md "wikilink")。ユーザーのホームディレクトリを、[AES-128を用いて暗号化することができる](../Page/Advanced_Encryption_Standard.md "wikilink")。ホームディレクトリは暗号化されたファイルとして保存され、ユーザのログイン時にマウントされる。初期のバージョンでは、単一の暗号化されたディスクイメージが使用されていたが、[Mac OS X v10.5以降のバージョンでは](../Page/Mac_OS_X_v10.5.md "wikilink")、細かく分割されたスパースバンドル\[1\]が使用され、OSの[Time Machine機能に対応した](../Page/Time_Machine_\(ソフトウェア\).md "wikilink")。

このバージョンでは、移行アシスタントを使用してユーザーデータを新しいマシンに移行させる時に、一度FileVaultを無効化(暗号化を解除)しなくてはならない。

## FileVault2

Mac OS X Lionで搭載されたバージョン。ディスク全体を暗号化することができる。FileVault2を有効にすると、ディスクが[XTS-AES 128](../Page/Advanced_Encryption_Standard.md "wikilink")\[2\]を用いて暗号化される。 パスワードを忘れたときのために復旧キーを設定できる。\[3\]

## 脚注

<references />

## 関連項目

  -
  - [BitLocker](https://ja.wikipedia.org/wiki/BitLocker "wikilink")(Windows Vista以降に搭載されているディスク暗号化機能)

  - [TrueCrypt](../Page/TrueCrypt.md "wikilink")(オープンソースのディスク暗号化ソフトウェア)

  - [LUKS](https://ja.wikipedia.org/wiki/LUKS "wikilink")（ディスク暗号化ソリューションの一つ）

  - [GNU Privacy Guard](../Page/GNU_Privacy_Guard.md "wikilink")（公開鍵暗号化方式による[電子メール](../Page/電子メール.md "wikilink")暗号化ソフトウエア）

  - [暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")

  - [Advanced Encryption Standard](../Page/Advanced_Encryption_Standard.md "wikilink")

  - [データの完全消去](https://ja.wikipedia.org/wiki/データの完全消去 "wikilink")

## 外部リンク

  - [OS X Lion：FileVault 2 について](http://support.apple.com/kb/HT4790?viewlocale=ja_JP)

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:セキュリティ技術](https://ja.wikipedia.org/wiki/Category:セキュリティ技術 "wikilink")

1.  8MBごとに分割されたファイルで構成されるディスクイメージで、単一の巨大なディスクイメージファイルに比べて効率的な取り扱い(バックアップ等)が可能。
2.  XEX (**X**or-Encrypt-Xor)-**T**CB(Tweakable CodeBlock Mode)-CT**S**(CipherText Stealing) の略である。
3.  復旧キーは、オンラインでAppleへ保管を依頼する事ができる。