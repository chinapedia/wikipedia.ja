> この記事は[Andrew File System](https://ja.wikipedia.org/wiki/Andrew_File_System)から翻訳されています。


**Andrew File System**（**AFS**）は、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の [Andrew Project](https://ja.wikipedia.org/wiki/Andrew_Project "wikilink") の一部として開発された[分散ファイルシステム](../Page/分散ファイルシステム.md "wikilink")である。Andrew とは、同大学の母体となる学校を作った二人のアンドリュー（[アンドリュー・カーネギー](../Page/アンドリュー・カーネギー.md "wikilink")と[アンドリュー・メロン](../Page/アンドリュー・メロン.md "wikilink")）に由来する。AFS は主に[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")で使用される。

## 特徴

AFS はそれまでのネットワーク対応の[ファイルシステム](../Page/ファイルシステム.md "wikilink")に比較して、特にセキュリティとスケーラビリティの面で優れていた。AFS は[ケルベロス認証](../Page/ケルベロス認証.md "wikilink")で認証を行い、ユーザおよびグループについてディレクトリ毎に[アクセス制御リスト](../Page/アクセス制御リスト.md "wikilink")を実装していた。各クライアントはファイルのキャッシュをローカルに保持して、同じファイルへのアクセスを高速化していた。またそれによって、サーバが故障したりネットワークに障害が発生しても、影響を限定することができた。

ファイルへのリード/ライト操作は、まずローカルなキャッシュに対して行う。ファイルの中身を更新してクローズしたとき、変更された箇所をサーバに書き戻す。キャッシュの一貫性は *callback* と呼ばれる機構によって保たれる。ファイルをキャッシュすると、サーバはそのことを覚えておき、更新が行われたら、他のクライアントに対してそれを通知する。いずれかのクライアント/サーバ/ネットワークで問題が発生したら、callback は失敗し、再試行される。callback の再試行とはステータスのチェックであり、必ずしもファイル自体を再度読む必要はない。

[ファイルロック](../Page/ファイルロック.md "wikilink")はファイル単位であるため、AFS は[データベース](../Page/データベース.md "wikilink")のような1つのファイル内のレコードを複数クライアントが更新するような形態での使用には適さない。これは、大学でのコンピュータ利用形態を考慮して決定した設計であった。このため、Andrew Project での[電子メール](../Page/電子メール.md "wikilink")システム Andrew Message System は1つのメッセージを1つのファイルにしており、メールボックスを1つのファイルにするような設定ではなかった。

AFS の重要な特徴として、ボリューム（Volume）と呼ばれるものがある。ディレクトリツリーと AFS のマウントポイント（他の AFS ボリュームへのリンク）から構成される（つまり、パーティションとは全く別個に構築される）。ボリュームは管理者が作成し、AFSセル（サーバグループ）の特定のパス名にリンクされる。作成されれば、ユーザはそれが物理的にはどこにあるのかを気にせずに、ディレクトリやファイルを作成できる。ボリュームにはクオータが設定され、利用可能なディスク容量が制限されている場合もある。管理者は、必要に応じてボリュームをサーバからサーバへ移動でき、それをユーザに通知する必要がない。ボリューム内のファイルを使っている最中でも移動可能である。

AFS ボリュームは、リードオンリーの複製を持たせることができる。リードオンリーのボリュームにアクセスする場合、クライアントがそのファイルを読み込むだけなら何の問題もない。読み込みの途中でそのサーバが使えなくなった場合、クライアントは別のコピーがないか探す。これはユーザには気づかれずに行われるので、管理者は必要に応じてそのようなコピーを複数のサーバに用意しておけばよい。AFS はリードオンリーの複製ボリュームが本来のリード/ライト可能なボリュームの複製時点の正確なコピーであることを保証する。

ファイル名空間は、Andrew ワークステーション上では「共有（*shared*）」と「ローカル（*local*）」に分離されている。共有ファイル名空間（通常 /afs にマウントされる）は、全ワークステーションで共通である。ローカル名前空間は各ワークステーション固有である。ローカルな部分には、立ち上げに必要な一時ファイルや共有名前空間へのシンボリックリンクなどだけが存在する。

AFS は[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の [Network File System](../Page/Network_File_System.md "wikilink") (NFS) バージョン4に影響を与えた。また、AFSの派生として、1989年に[DCEの一部として](../Page/Distributed_Computing_Environment.md "wikilink")[OSFが開発した](../Page/Open_Software_Foundation.md "wikilink") [DCE/DFS](../Page/DCE_Distributed_File_System.md "wikilink") がある。

## 実装

主な実装は3つ存在する。[トランザーク](https://ja.wikipedia.org/wiki/トランザーク "wikilink")版（[IBM](../Page/IBM.md "wikilink")）、[OpenAFS](../Page/OpenAFS.md "wikilink")、[Arla](https://ja.wikipedia.org/wiki/Arla "wikilink") である。ただしトランザーク版は既にサポートされていない。また、カーネギーメロン大学での後継ファイルシステムとして [Coda](../Page/Coda.md "wikilink") がある。

第四の実装として、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink") 2.6.10 で実装されたものがある\[1\]。[レッドハット](../Page/レッドハット.md "wikilink")が開発したものであり、まだ不完全である\[2\]。

## パーミッションの種類

アクセス制御リスト(ACL)には、次のようなパーミッションが設定される。

  - Lookup (l)
    AFS ディレクトリの内容をリスト表示でき、サブディレクトリにアクセス可能かどうかを調べることができる。
  - Insert (i)
    新規ファイルを追加したり、サブディレクトリを追加したりできる。
  - Delete (d)
    ファイルを削除したり、サブディレクトリを削除したりできる。
  - Administer (a)
    そのディレクトリの ACL を変更できる。ユーザは自身の[ホームディレクトリ](../Page/ホームディレクトリ.md "wikilink")についてはこのパーミッションを保持している（ユーザが間違ってACLから自分自身の設定を消してしまったとしても、Administer パーミッションは保持される）。

ファイルとサブディレクトリに関するパーミッションには、次のようなものがある。

  - Read (r)
    ファイルの内容を参照したり、サブディレクトリのリスト表示が可能。ファイルのリードアクセスをするには、通常の[UNIX](../Page/UNIX.md "wikilink")の[ファイルパーミッション](../Page/ファイルパーミッション.md "wikilink")も適切に設定しておく必要がある。
  - Write (w)
    ファイルを更新できる。やはり、同時にUNIXのファイルパーミッション設定が必要。
  - Lock (k)
    [flock](../Page/ファイルロック.md "wikilink") を使ったプログラムの実行が可能。

さらに AFS の ACL にはアプリケーション用設定もあり、通常のファイルアクセスには全く関係ない。

## 参考文献

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:カーネギーメロン大学](https://ja.wikipedia.org/wiki/Category:カーネギーメロン大学 "wikilink")

1.  [Linux kernel AFS documentation for 2.6.10](http://lxr.linux.no/source/Documentation/filesystems/afs.txt?v=2.6.10)
2.  [Linux kernel AFS documentation for the latest kernel version](http://lxr.linux.no/source/Documentation/filesystems/afs.txt)