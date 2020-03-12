> この記事は[Diskeeper](https://ja.wikipedia.org/wiki/Diskeeper)から翻訳されています。


**Diskeeper**（ディスキーパー）は米Condusiv Technologies（旧Diskeeper Corporation、 Executive Software International）が開発している[Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[デフラグメンテーション](../Page/デフラグメンテーション.md "wikilink")ソフトである。

## 概要

ファイルの断片化を未然に防ぐ機能などを搭載した、高性能のデフラグメンテーション(以下デフラグ)ソフトである。Microsoft社より依頼を受けて開発された[NTFS](https://ja.wikipedia.org/wiki/NTFS "wikilink")向けデフラグプログラムが元になっており、Windows 2000, Windows XP, Windows Server 2003 のOS標準のデフラグ機能はDiskeeperの機能削減版となっている\[1\]。そのため、DiskeeperをインストールすることでOS標準のデフラグ機能を置き換え、制限されていたシステムファイルの断片化の解消などを行えるようになる。

Diskeeperは米（旧Diskeeper Corporation）が開発し、日本では相栄電器株式会社が販売元になっている。

### 歴史

  - 2009

Windows2000に対応した最後のバージョン。

Diskeeper 10より、32bit系Windows OSだけでなく、64bit系Windows OSにもネイティブで対応している。 Diskeeper 10の次のバージョンからはDiskeeper 2007と年号方式に変わった。2011年7月に発売された2012年度版となるバージョン16では、年号の下二桁が製品名となっている。 Diskeeper 2007は、Home, Professional, Pro Premier（ここまでがコンシュマー向け）, Server, EnterpriseServer（サーバOS向け）, Administrator（ネットワーク管理ツール）と多くのEditionが用意されている。 2007から[アクティベーション](../Page/アクティベーション.md "wikilink")が必須となり定期的にインターネット経由での認証が行われるようになった。 2010からはデフラグできるディスクの容量制限が廃止された。 また、12からはインターフェースが大幅に変更され、従来までProfessional/Serverエディションにのみ搭載されていたHyperFastテクノロジー（SSD最適化）が全エディションに搭載され、またコンピュータの起動時間を向上させるHyperBoot機能がHome/Professionalエディションに新搭載された。

## 機能

  - IntelliWrite（インテリライト）機能 : ファイルシステムのドライバとして動作し\[2\]、ファイル断片化を未然に防ぐ機能。
    自動デフラグ機能 : InvisiTaskingとリアルタイム・デフラグを組み合わせることで実現。これによりファイル断片化を、即時解消できるようになる機能。　
    I-FAAST機能 : ボリュームの論理的および物理的な性質の両面が考慮され、ファイルの順序が決められたうえで、ファイルへのアクセスと作成時間をスピードアップが可能となる機能。　
    ダッシュボード機能 :一目で、Diskeeperのメモリーリソースの使用状況や、ファイル断片化解消状況などが把握できる機能。
    Frag Shield : MFTとページファイルの断片化を阻止する機能。
    Microsoft Operations Manager（MOM）と System Center Operations Manager（SCOM）に対応 : ネットワーク上の多数のPC上のDiskeeperをMOMおよびSCOMでモニタできる。
    HyperFast機能 : [SSDの最適化機能](../Page/ソリッドステートドライブ.md "wikilink")。[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")の書き換え回数制限等、特性を考慮した特殊な方法でデフラグする。「with HyperFast」を含むEditionに搭載。

## それぞれのEdition

  - Home : 必要な最低限の機能（自動デフラグ機能、ブートタイムデフラグ機能、IntelliWrite機能）を搭載。ダッシュボード上にはアクティブリソースのグラフが表示されないので、ソフトが動作しているのかどうか分かりづらい場合がある。日本語版のみの制限として、Windowsの一部上位エディションには対応していない。完全に家庭用であり、Administrator Editionによる制御の対象外。
    Professional : Homeに搭載されている機能に加え、ダッシュボード上にアクティブリソースのグラフが表示できるようになったり、大容量のファイルがデフラグできるようになっている。またコマンドラインのサポート、Frag ShieldおよびI-FAASTが有効になっている。
    Pro Premier : Professionalに搭載されている機能に加え、テラバイト・ボリューム・エンジン(TVE)という大容量ボリューム、大容量ファイルを処理する専用のデフラグエンジンを搭載。バージョン12からProfessionalエディションに統合された。
    Server : 基本機能はPro Premierと同じだが、Windows Server系OSに対応。
    EnterpriseServer : 更なる大容量における性能を向上したタイタン・デフラグ･エンジン(TDE)を搭載。
    Administrator : ネットワーク上にあるDiskeeperを管理するツール。これ自体にはデフラグ機能はない。
    Lite : Diskeeperの無償配布版。現在もDiskeeper Lite 7.0.418.0が入手可能。機能は分析とデフラグのみ。デフラグエンジンはDiskeeper 7.0相当のため、新しいバージョンと比べるとデフラグの所要時間は長い。

## ローカライズの遅れ

もともと海外でのローカライズ作業のため、以前は海外での最新版リリースから日本語版が発売されるまでに時間がかかっていた。

Windows Vistaが発売された時点での本家の最新版は2007であったが、日本ではバージョン10だった。 ところが米Diskeeper Corporationは当時最新版である2007でのみVistaへの対応を行うと発表したため、相栄電器株式会社が日本語版が完成次第無償提供するという条件で英語版を発売するに至った。

しかし、2008以降は世界同時発売（日本語版含む）となったので、タイムラグ無しで最新版の入手が可能になった。

## 関連項目

  - [デフラグ (Windows)](../Page/デフラグ_\(Windows\).md "wikilink")

## 脚注・出典

## 外部リンク

  - [相栄電器](http://www.sohei.co.jp/)
  - [Diskeeper](http://www.diskeeper.com/)(英語)

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink")

1.
2.  [Inside Diskeeper 2010 with IntelliWrite (PDFファイル)](http://downloads.diskeeper.com/pdf/IntelliWrite_Technology_brief.pdf)