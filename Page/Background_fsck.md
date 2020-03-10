> この記事は[Background fsck](https://ja.wikipedia.org/wiki/Background_fsck)から翻訳されています。


**Background fsck**とは、[Soft updatesで以前マウントしていて](../Page/Soft_updates.md "wikilink")、意図しない停止をした[ファイルシステム](../Page/ファイルシステム.md "wikilink")に[mountされた状態のまま](https://ja.wikipedia.org/wiki/mount_\(UNIX\) "wikilink")[fsck](https://ja.wikipedia.org/wiki/fsck "wikilink")してファイルシステムを修復することである。

## 概要

ファイルシステムをアンマウント(unmount, 使用を止めて[マウントしていない状態にすること](https://ja.wikipedia.org/wiki/mount_\(UNIX\) "wikilink"))しないままシステムが停止してしまった場合、通常はファイルシステムの一貫性が壊れてしまい、ファイルシステムを[fsck](https://ja.wikipedia.org/wiki/fsck "wikilink")によって修復しなければ再びマウントして使用することはできなくなる。

しかし、[Soft updatesを使うとシステムがいつ停止してもファイルシステムの一貫性は基本的に壊れない](../Page/Soft_updates.md "wikilink")。 再起動後にfsckを実行しなくてもファイルシステムをそのままマウント(mount)して使用できる。 唯一起きる矛盾は、使用されていないはずの領域が使用されているとマークされて、その領域が無駄になることである。

**Background fsck**とは、この状態になったファイルシステムを使用しながら無駄な領域を解放することである。 従って、fsckといっても実際の役割は一種の[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")である。

## 手順

Background fsckではまず、[ファイルシステム](../Page/ファイルシステム.md "wikilink")のスナップショットを作成する。 そして、このスナップショットに対して[fsck](https://ja.wikipedia.org/wiki/fsck "wikilink")を実行し、ファイルシステムを修復する。 長時間停止することなくスナップショットを作成するために[コピーオンライト](../Page/コピーオンライト.md "wikilink")を用いているが、この際ファイルシステムの変更を行う可能性のある[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")はすべてブロックされ、その間だけ計算機が応答しなくなり「[フリーズ](../Page/フリーズ.md "wikilink")した」と認識されることがある。スナップショットの作成が完了した時点でブロックは解除されるので、電源を切るなど早計な手段に出るべきではない。

## スナップショット（副産物）

Background fsckの副産物としてスナップショット機能がある。 スナップショットはmksnap_ffsコマンドで簡単に作成できる。 これは一つのファイルシステムに対していくつも作成することが出来るので、[UFSの簡易バックアップ機構として用いることが出来る](https://ja.wikipedia.org/wiki/Unix_File_System "wikilink")。 実際、この手法でバックアップを行うportが存在する。

## 参考文献

  - McKusick, M. (2002). [Running "fsck" in the Background](http://www.usenix.org/publications/library/proceedings/bsdcon02/mckusick/mckusick_html/index.html)." *Proceedings of the BSDCon 2002.* 55-64.

## 外部リンク

  - [Information about Soft Updates, Snapshots, and Back-ground Fsck](http://www.mckusick.com/softdep/)
  - [FreeBSD UFS Snapshots Management Environment](http://people.freebsd.org/~rse/snapshot/)

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink")