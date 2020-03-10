> この記事は[Virt-manager](https://ja.wikipedia.org/wiki/Virt-manager)から翻訳されています。


[Libvirt_support.svg](https://ja.wikipedia.org/wiki/File:Libvirt_support.svg "fig:Libvirt_support.svg") and supports several [ハイパーバイザ](https://ja.wikipedia.org/wiki/ハイパーバイザ "wikilink")\]\]

**virt-manager**とは、[レッドハット](../Page/レッドハット.md "wikilink")社からリリースされた[仮想機械](../Page/仮想機械.md "wikilink")を[GUI上で管理運用を行う](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。ここでいう仮想機械とは[Xen](https://ja.wikipedia.org/wiki/Xen_\(仮想化ソフトウェア\) "wikilink")、[KVM](https://ja.wikipedia.org/wiki/Kernel-based_Virtual_Machine "wikilink")、[QEMU](https://ja.wikipedia.org/wiki/QEMU "wikilink")などの[仮想化](https://ja.wikipedia.org/wiki/仮想化 "wikilink")実装システムを使用してインストールされたゲストOS の事を指す。

virt-managerは主に[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")の[X Window System上で動作する](../Page/X_Window_System.md "wikilink")。仮想機械のホストOS内にこのソフトをインストールすることでゲストOSの[CPU](../Page/CPU.md "wikilink")や[メモリの使用状況についての詳細情報の表示をグラフで行い](../Page/主記憶装置.md "wikilink")、稼働中の仮想マシンの停止や再起動などの管理を行う。 [オープンソース](../Page/オープンソース.md "wikilink")ということもあって[CentOS](https://ja.wikipedia.org/wiki/CentOS "wikilink")や[Fedora](../Page/Fedora.md "wikilink")などではあらかじめインストールされている場合も多い。

0.5版から、ネットワーク越しのVMを管理するためのリモート接続機能が加わった。また、vnc-viewerが、[gtk-vnc](https://ja.wikipedia.org/wiki/gtk-vnc "wikilink")に切り替わった。

なお、本プロジェクトのメンテナは、Daniel Berrange氏、Hugh O. Brock氏、Jeremy Katz氏、Cole Robinson氏である。

## ソフトウェア構成

ソースコードは[Python](../Page/Python.md "wikilink")で記述されている。

本コードで使っているライブラリは、大まかに4種類に分かれる。すなわち、GUI, イベント通知, 仮想機械制御、及びその他のライブラリである。 GUI は UIビルダーツールの[Glade](https://ja.wikipedia.org/wiki/Glade "wikilink")や[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")で[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")されている。 そして、イベント通知では、[D-BUS](https://ja.wikipedia.org/wiki/D-BUS "wikilink")を用いており、Xのイベント検知(notification-daemon)、ハードウェアの構成変更の検知(hald)、およびvirt-managerそのものの[シングルトン](https://ja.wikipedia.org/wiki/シングルトン "wikilink")起動の管理を行っている。 仮想機械の管理は、[libvirt](https://ja.wikipedia.org/wiki/libvirt "wikilink") と呼ばれる [APIを使用することにより](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、どのような仮想機械でも管理できるように設計されており libvirt 上でのAPIが提供される限りは仮想機械の実装に関係なく対応できる。そして、仮想機械のインストールは、関連ツールである[virt-install](https://ja.wikipedia.org/wiki/virt-install "wikilink")をライブラリとして、用いている。 その他のライブラリとしては、仮想ネットワーク及び、VNCviewerがある。 まず、仮想ネットワークを取り扱うために、IPアドレス管理ツールIPyを内部クラスとして取り込んで使っている。 そして、VNC Viewerは、[gtk-vnc](https://ja.wikipedia.org/wiki/gtk-vnc "wikilink")を使っている。

## 関連ソフトウェア

リモート接続が出来るという観点では、まったく同じだが、Webブラウザで動くソフトウェアとして、[oVirt](https://ja.wikipedia.org/wiki/oVirt "wikilink")がある。virt-managerに比べてアクセス制御を役割毎に細かく設定できるという点が異なる。

## 外部リンク

  - [Virtual Machine Manager](http://virt-manager.org/)
  - [virt-manager](http://virt-manager.et.redhat.com/)
      - [開発予定表](http://virt-manager.et.redhat.com/page/Roadmap)
      - [ソースコード](http://virt-manager.et.redhat.com/scmrepo.html)
      - [版数履歴](http://virt-manager.et.redhat.com/download.html)
      - [画面例](http://virt-manager.et.redhat.com/screenshots.html)
      - [デイリービルド状況](http://builder.virt-manager.org/)
  - [gtk-vnc](http://gtk-vnc.sourceforge.net/)
  - [cobbler](http://cobbler.et.redhat.com/)
  - [IPy](http://software.inl.fr/trac/wiki/IPy)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink")