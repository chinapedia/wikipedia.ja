> この記事は[FairPlay](https://ja.wikipedia.org/wiki/FairPlay)から翻訳されています。


**FairPlay**（フェアプレー）は、[QuickTime](../Page/QuickTime.md "wikilink")マルチメディア技術に内蔵され[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")、[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")、及び[iTunes Storeによって使用されているこの](https://ja.wikipedia.org/wiki/iTunes_Store "wikilink")[デジタル著作権管理](../Page/デジタル著作権管理.md "wikilink") (DRM : Digital Rights Management) 向けに[アップルが名付けた名称である](../Page/アップル_\(企業\).md "wikilink")。iTunesと共にiTunes Storeから購入したそれぞれのファイルはFairPlayと同時にエンコードされている。また同社の[携帯音楽プレーヤー](../Page/携帯音楽プレーヤー.md "wikilink")である[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")シリーズはこの方式の[ファイルをスムーズにシンクする](../Page/ファイル_\(コンピュータ\).md "wikilink")。

## 「FairPlay」の仕様 (v2)

  - パソコンでの再生：5台（コピーは無制限）
  - 全く同じ内容の音楽[CD作成](../Page/コンパクトディスク.md "wikilink")：7枚
  - [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")および対応携帯電話との同期：無制限
  - 純正iアプリケーションでの利用：可
  - ネットワークによる認証方式。解除、切り換えも可能。
  - 複数アカウントの共存が可能。

## 仕組み

FairPlayは公平かつ単純なDRM技術である。FairPlayで保護されたファイルは、暗号化されたAACオーディオストリームを含む正規のMP4コンテナファイルである。このAACは[AES暗号化とMD](../Page/Advanced_Encryption_Standard.md "wikilink")5ハッシュの組み合わせを使っており、AACの暗号化を解くために必要なマスターキーもMP4コンテナの中に暗号化されて含まれている。このマスターキーの暗号化を解くために必要とされる鍵は“ユーザキー”と呼ばれている。

iTunesでファイルを購入する際に、マスターキーを暗号化する為の新たなユーザキーがランダムに生成される。この生成されたキーはアップルの[サーバ](../Page/サーバ.md "wikilink")にアカウント情報と共に保存され、生成したiTunesにも送られる。受け取ったiTunesはユーザキーを、暗号化したキーデータベースへ登録する。このデータベースを使えばiTunesはマスターキーの暗号化を解く際に必要となったユーザキーを手に入れ、暗号化を解いたマスターキーを使ってオーディオトラックを再生出来るのである。

別のコンピュータ上から既存のアカウントで認証する場合、iTunesはそのコンピュータのユニークな識別子をアップルのサーバへ送り、アカウント情報と共に登録されたユーザキーを受け取る。このことによって、同一のアカウントで認証していれば別のコンピュータ上でも購入した楽曲を再生するために必要な全てのユーザキーを保持することができ、かつ認証できるコンピュータの数をアップルのサーバによって制限することを確実にしている。

コンピュータの認証を解除する場合、iTunesはアップルのサーバにコンピュータの識別子を削除するようにリクエストし、それと同時にiTunesのキーデータベースからユーザキーを削除する。

iPodもiTunesと同様に暗号化したキーデータベースを持っている。iPodへFairPlayで保護された楽曲をコピーする際、iTunesはiPodのキーデータベースにユーザキーをコピーする。iPodはそのユーザキーを用いて保護されたAACオーディオストリームを再生するようになっている。

これらの暗号化処理はQuickTimeとiTunesで固く施されているように見える。そしてデータベース自身も暗号化されているため編集が出来ないのである。

## 関連項目

  - [VLCメディアプレーヤー](../Page/VLCメディアプレーヤー.md "wikilink")

## 外部リンク

  - [Sourceforge.net（英語版）](http://sourceforge.net/)
  - [Sarovar.org（英語版）](http://sarovar.org/)

[Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:著作権管理技術](https://ja.wikipedia.org/wiki/Category:著作権管理技術 "wikilink")