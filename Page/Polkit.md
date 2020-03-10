> この記事は[Polkit](https://ja.wikipedia.org/wiki/Polkit)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:PolicyKit.png "wikilink") **Polkit**(旧名**PolicyKit**)とは、[Unix系](../Page/Unix系.md "wikilink")オペレーティングシステムで、システム全体の権限を制御するためのアプリケーション開発ツールキットである。このライブラリによって、特権を持たないプロセスが、特権を持つプロセスと通信することができるようになる。[sudo](https://ja.wikipedia.org/wiki/sudo "wikilink")のようなコマンドと比較すると、プロセス全体に対して特権を与えることはしない。しかし、1つのポリシーで、より細かなポリシーをシステム全体に対して適用できるという特徴がある。このライブラリは、[freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink")プロジェクトの一環で作られた。

PolicyKitは[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")では8.04より、[Fedora](../Page/Fedora.md "wikilink")では8より導入されている。

Ver0.105以降に名前をPolkitに変更した。\[1\]

このツールは様々なアプリケーションに取り込まれている。例えば、[libvirt](https://ja.wikipedia.org/wiki/libvirt "wikilink")や[virt-manager](https://ja.wikipedia.org/wiki/virt-manager "wikilink")から使うこともできる。また、SELinuxの持つセキュリティコンテキスト情報を[D-Bus](../Page/D-Bus.md "wikilink")より取得して、動作することもできる。

## 関連項目

  - [最小権限の原則](https://ja.wikipedia.org/wiki/最小権限の原則 "wikilink")

## 脚注

<references/>

  -
  -
## 外部リンク

  - [PolicyKit ライブラリリファレンスマニュアル](http://hal.freedesktop.org/docs/PolicyKit/)
  - [ソースコード](http://gitweb.freedesktop.org/?p=PolicyKit.git;a=summary)
  - [メンテナ (David Zeuthen) のブログ](http://blog.fubar.dk/)
  - Fedora等への組込み提案書
      - [ポリシーキット取り込み提案書(Fedora8)](http://fedoraproject.org/wiki/Releases/FeaturePolicyKit)
      - [virt-managerへのポリシーキット統合提案書(Fedora9)](http://fedoraproject.org/wiki/Features/VirtPolicyKit)

[Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink")

1.