> この記事は[Boot Camp](https://ja.wikipedia.org/wiki/Boot_Camp)から翻訳されています。


**Boot Camp**（**ブートキャンプ**）は、[アップルにより開発](../Page/アップル_\(企業\).md "wikilink")・配布されている[ソフトウェア](../Page/ソフトウェア.md "wikilink")。[Intel Macにおいて](../Page/Intel_Mac.md "wikilink")[Windowsの利用を可能とする](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 概要

[2006年](../Page/2006年.md "wikilink")に、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製[CPU](../Page/CPU.md "wikilink")搭載のMacを発売開始したアップルは、Intel Macにおける[Microsoft Windowsの起動を](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、積極的に支援も妨害もしないと表明していた。

Boot Campは、[2006年](../Page/2006年.md "wikilink")[4月5日](../Page/4月5日.md "wikilink")に[EFIでは起動出来ない](../Page/Unified_Extensible_Firmware_Interface.md "wikilink")[OSをサポートする為のCSM](../Page/オペレーティングシステム.md "wikilink") (Compatibility Support Module) 搭載と思われるFirmware Updateと共に、パブリックベータとして発表された。Boot Campとは[アメリカ軍](../Page/アメリカ軍.md "wikilink")における[新兵の基礎訓練を意味する](../Page/ブートキャンプ.md "wikilink")[スラング](../Page/スラング.md "wikilink")であり、ここでは[コンピュータ](../Page/コンピュータ.md "wikilink")の起動 ([boot](../Page/ブート.md "wikilink")) と掛けて使用されている。[2007年](../Page/2007年.md "wikilink")10月発売された[Mac OS X v10.5においてVersion](../Page/Mac_OS_X_v10.5.md "wikilink") 2.0が搭載された。

## 機能

Boot Campは、Intel Macの[ハードディスクに](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")を残したままWindowsを[インストール](../Page/インストール.md "wikilink")するための任意のサイズの[パーティション](../Page/パーティション.md "wikilink")を作成する機能や、Windowsのインストール後にIntel Macで使われている[無線LAN](../Page/無線LAN.md "wikilink")や[ビデオカード](../Page/ビデオカード.md "wikilink")の[ドライバをインストールするためのドライバ](../Page/デバイスドライバ.md "wikilink")[CD-R](../Page/CD-R.md "wikilink")を作成する機能を持つ。また、Intel Mac上でWindowsを動かすために必要な一連の作業を、あまり専門知識を持たない人にでも簡易に行えるようにするため、シンプルな[インタフェースを搭載している](../Page/インタフェース_\(情報技術\).md "wikilink")。従来、[インターネット](../Page/インターネット.md "wikilink")等で発表されていたIntel MacにおけるWindows起動方法は、いずれも複雑かつWindowsの使用[ライセンス](../Page/ライセンス.md "wikilink")に関して不明確な点が存在したため多くのMacユーザーは様子見状態で導入に踏み切れなかった。この機能がアップルによって発表されたことにより、これらの問題を解決する手段となり、高い互換性でWindowsを実行できる環境が整い、再起動のみでmacOSとのデュアルブート環境で使用できるようになった。

## 仮想化環境との違い

Boot camp環境は、仮想化ソフトウェアであるParallels Desktop for MacやVMware Fusionとは異なり、単純に起動時に各OSを選択できるシンプルなOSローダー機能が特徴である。仮想化ソフトウェアとの違いは、マイクロソフトのOSライセンスによっても影響がある。[Windows 8からライセンスポリシーが変更になり](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")、[Windows 7までは実質上ParallelsとVMware環境では](../Page/Microsoft_Windows_7.md "wikilink")1つのパッケージから2つのWindowsのライセンス発行が許されていた（Bootcamp環境でのライセンスのほか、仮想化環境での使用では、追加のライセンス認証が許可されていた）が、Windows 8以降では、DSP版とOEM版では基本的に1ライセンスに変更された。これにより、Bootcamp環境でライセンス認証したOSを、仮想環境から参照して起動するには、さらにもう1つライセンスが追加で必要となる。

## バージョン

  - 1.0.1 Beta（[2006年](../Page/2006年.md "wikilink")[6月29日](../Page/6月29日.md "wikilink")）
    最初に公開されたバージョン。ドライバ等の完成度も低く、動作はするものの問題が多かった。

  - 1.0.2 Beta（[2006年](../Page/2006年.md "wikilink")[7月12日](../Page/7月12日.md "wikilink")）
    バグフィクス版

  - 1.1 Beta（[2006年](../Page/2006年.md "wikilink")[8月18日](../Page/8月18日.md "wikilink")）
    最大の懸念事項であった[MacBook](../Page/MacBook.md "wikilink")における無線LANの解決、iSightの動作、キーボード問題の部分的解決など、ほぼ常用する部分においては動作するようになった。またインストールもより簡単になり、安定した。

  - 1.1.2 Beta（[2006年](../Page/2006年.md "wikilink")[10月30日](../Page/10月30日.md "wikilink")）
    いくつかのドライバの追加と、安定化が行われた。

  - 1.2 Beta（[2007年](../Page/2007年.md "wikilink")[3月29日](../Page/3月29日.md "wikilink")）
    [Windows Vistaをサポート](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。赤外線ポートドライバが提供され、[Apple Remoteが利用可能になった](../Page/Apple_Remote.md "wikilink")（ペアリングは不可）。タスクトレイ内にアイコンメニューが登場し、Windows側から参照できるメニューが搭載された（Boot Camp用ヘルプ、輝度調整、ブートローダー選択等）。

  - 1.3 Beta（[2007年](../Page/2007年.md "wikilink")[6月7日](../Page/6月7日.md "wikilink")）
    バックライトキーボード対応([MacBook Proのみ](../Page/MacBook_Pro.md "wikilink"))。各言語キーボードサポート強化、[Apple RemoteのペアリングがWindows側から操作可能になった他](../Page/Apple_Remote.md "wikilink")、ドライバ類を多数アップデート。

  - 1.4 Beta（[2007年](../Page/2007年.md "wikilink")[8月8日](../Page/8月8日.md "wikilink")）
    [iMac (Mid 2007)への対応と](https://ja.wikipedia.org/wiki/iMac#iMac_\(Mid_2007\) "wikilink")、各種グラフィックドライバがアップデートされた。

  - 2.0（[2007年](../Page/2007年.md "wikilink")[10月26日](../Page/10月26日.md "wikilink")）
    [Mac OS X v10.5に付属する正式版](../Page/Mac_OS_X_v10.5.md "wikilink")。

  - 2.1（[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[4月25日](../Page/4月25日.md "wikilink")）
    [Windows XP Service Pack 3](https://ja.wikipedia.org/wiki/Microsoft_Windows_XP#Service_Pack_3 "wikilink") (SP3) への対応、およびバグフィクス。

  - 3.0（[2009年](../Page/2009年.md "wikilink")[8月28日](../Page/8月28日.md "wikilink")）
    [Mac OS X v10.6に付属する正式版](../Page/Mac_OS_X_v10.6.md "wikilink")。ドライバのアップデートに加え、Windows側からMac OS X側の[HFSフォーマットのハードディスク内を閲覧可能になった](../Page/Hierarchical_File_System.md "wikilink")。他にもトラックパッドのタッチクリック対応、[Apple Cinema Displayの拡張機能のサポートなどが加えられ](../Page/Apple_Cinema_Display.md "wikilink")、[Windows 7のインストールにも対応](../Page/Microsoft_Windows_7.md "wikilink")。（正式対応ではない）

  - 3.1（[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[1月20日](../Page/1月20日.md "wikilink")）
    [Windows 7](../Page/Microsoft_Windows_7.md "wikilink")（Home Premium、Professional、および Ultimate）への正式対応とアップル製トラックパッド使用時に起こる問題の解決、Apple Wireless KeyboardおよびApple Magic Mouseのサポート。

  - 3.2（[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[11月19日](../Page/11月19日.md "wikilink")）
    ATI-Radeon HD 5870 graphics card, Apple USB Ethernet Adapter, MacBook Air SuperDrive のサポート。

    重要なバグフィックス。

  - 3.3（[2011年](../Page/2011年.md "wikilink")[8月24日](../Page/8月24日.md "wikilink")）
    新しいハードウェアのサポート。

    重要なバグフィックス。

    [Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、[Windows Vistaのサポートを終了](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。

  - 4.0（[2012年](../Page/2012年.md "wikilink")[6月20日](../Page/6月20日.md "wikilink")）
    すべてのバージョンの[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、[Windows Vistaのサポートを終了](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。

    Mac OS X 10.6 "Snow Leopard"、Mac OS X 10.7 "Lion" およびOS X 10.8 "Mountain Lion" でのみ対応。

    USBメディア内のISOイメージからのインストールをサポートを追加。

  - 5.0（[2013年](../Page/2013年.md "wikilink")[3月14日](https://ja.wikipedia.org/wiki/3月14日 "wikilink")）
    [Windows 8](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")（[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")）のサポート。

    3TBのHDDを搭載したMacのサポート。

    [32ビット](../Page/32ビット.md "wikilink")版[Windows 7のサポートを終了](../Page/Microsoft_Windows_7.md "wikilink")。

    Mountain Lion version 10.8.3以降のOS Xでのみ対応。

  - 5.1（[2014年](../Page/2014年.md "wikilink")[2月11日](../Page/2月11日.md "wikilink")）
    [Windows 8.1](https://ja.wikipedia.org/wiki/Microsoft_Windows_8.1 "wikilink")（[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")）および[Windows 8.1](https://ja.wikipedia.org/wiki/Microsoft_Windows_8.1 "wikilink") Pro（[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")）のサポート。

  - 5.1.2（[2014年](../Page/2014年.md "wikilink")[10月16日](../Page/10月16日.md "wikilink")）
    6.0（[2015年](../Page/2015年.md "wikilink")[8月13日](../Page/8月13日.md "wikilink")）
    [Windows 10](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")（[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")）のサポートを追加。

    [Windows 10は](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")版のみ対応で、公式対応は、下記の機種である。

      -
        **MacBook Pro:** MacBook Pro (Retina, 15-inch Mid 2015), MacBook Pro (Retina 13-inch Early 2015), MacBook Pro (Retina, 15-inch Mid 2014), MacBook Pro (Retina 13-inch Mid 2014), MacBook Pro (Retina 15-inch Late 2013), MacBook Pro (Retina 13-inch Late 2013), MacBook Pro(Retina, 15-inch Early 2013), MacBook Pro (Retina 13-inch Early 2013), MacBook Pro (Retina 13-inch Late 2012), MacBook Pro (Retina Mid 2012), MacBook Pro (13-inch Mid 2012), MacBook Pro (15-inch Mid 2012)
        **MacBook Air:** MacBook Air (13-inch Early 2015), MacBook Air (11-inch Early 2015), MacBook Air (13-inch Early 2014), MacBook Air (11-inch Early 2014), MacBook Air (13-inch Mid 2013), MacBook Air (11-inch Mid 2013), MacBook Air (13-inch Mid 2012), MacBook Air (11-inch Mid 2012)
        **MacBook:** MacBook (Retina, 12-inch, Early 2015)
        **iMac:** iMac (Retina 5K 27-inch, Late 2015), iMac (Retina 4K 21.5-inch Late 2015), iMac (21.5-inch Late 2015), iMac (Retina 5k 27-inch Mid 2015), iMac (Retina 5K 27-inch Late 2014), iMac (21.5-inch Mid 2014), iMac (27-inch Late 2013), iMac (21.5-inch Late 2013), iMac (27-inch Late 2012), iMac (21.5-inch Late 2012)
        **Mac mini:** Mac mini (Late 2014), Mac mini Server (Late 2012), Mac mini (Late 2012)
        **Mac Pro:** Mac Pro (Late 2013)

  - 6.0.1 ([2015年](../Page/2015年.md "wikilink")[12月8日](../Page/12月8日.md "wikilink"))

## 機能の詳細

  - 未対応問題

<!-- end list -->

  - Windows XPからMac側ハードディスクを利用できない(3.0から対応)。

<!-- end list -->

  - 1.1 Betaで対応した機能

<!-- end list -->

  - 日本語版のMacBookおよびMacBook Proでも[AirMac](../Page/AirMac.md "wikilink")による無線LAN接続利用が可能となった。
      - （インターナショナル版MacBook + 英語版WindowsXPでは動作可だった）
  - キーボードの一部機能（「ー」「ろ」「_」「\\」「|」「Fn」）が利用可能となった。
  - 「Fn」キー等と組み合わせて実現する機能（ディスプレイの光度調整、音量調整など）がほぼ使用可能になった。
  - ヘッドフォン端子を挿入した時に本体のスピーカーがoffになるようになった
  - [Mac Pro](../Page/Mac_Pro.md "wikilink")、[Intel Core 2 Duo搭載の](../Page/Intel_Core_2.md "wikilink")[iMac](https://ja.wikipedia.org/wiki/iMac "wikilink")に対応。
  - [iSight](https://ja.wikipedia.org/wiki/iSight "wikilink")（内蔵カメラ）が動作するようになった。
  - Windows XPで日時の同期が可能になった。
  - 「DEL」、「全角/半角」キー及び、タッチパッドの右ボタンが（そもそも存在しないため）選択できなかった。キーボード上「DELETE」キーは、「BackSpace」キーとして機能する。
      - （Appleキーボードの右アップルキーで右クリック等、他のキーで代用対応）
  - インストール時のパーティション作成ユーティリティが強化され、一般的なサイズがプリセットで用意され、パーティションの作成が容易になり、Windowsを任意のドライブにインストールすることができるようになった。
  - Delete、PrintScreen、NumLock、ScrollLockキーなど、Appleキーボードのサポートが強化された。

<!-- end list -->

  - 1.1.2 Betaで対応した機能

<!-- end list -->

  - Intel Core 2 Duo搭載のMacBook Proに対応。
  - タッチパッドの各種拡張機能が利用できるようになった。
      - （二本指でタッチすることによりスクロールする等。しかしやや不安定）
  - Apple USBモデムに対応した。
  - Apple国際キーボードのサポートが強化された。

<!-- end list -->

  - 1.2 Betaで対応した機能

<!-- end list -->

  - Windows Vista（32ビット版）に対応
  - トラックパッド、AppleTime（シンク）、オーディオデバイス、グラフィックス、モデム、iSightカメラなどのドライバを更新
  - Apple Remoteに対応
      - （iTunesやWindows Media Playerの操作が[リモコン](../Page/リモコン.md "wikilink")で操作可能になった。）
  - WindowsのシステムトレイアイコンからBoot Campの情報の表示、アクションの実行が可能になった。
  - マニュアル、WindowsのBoot Campオンラインヘルプの内容を更新

<!-- end list -->

  - 1.3 Betaで対応した機能

<!-- end list -->

  - バックライトキーボード対応（MacBook Proのみ）。
  - 様々な言語キーボードサポート強化など、ローカライズ強化
  - [Apple Remoteのベアリングに対応](../Page/Apple_Remote.md "wikilink")
  - グラフィックドライバをアップデート
  - Boot Campドライバインストーラをアップデート

<!-- end list -->

  - 2.0で対応した機能

<!-- end list -->

  - F11キーによるスクリーンショット機能の削除
  - タスクバーにおける画面輝度スライダーの削除

<!-- end list -->

  - 2.1で対応した機能

<!-- end list -->

  - Windows XP SP3対応
  - Windows Vista SP1対応
  - Windows Vista 64ビット版対応
  - Battery.sysがクラッシュするバグの修正

<!-- end list -->

  - 3.0で対応した機能

<!-- end list -->

  - WindowsからMac OS Xの領域の読み込みが可能。
  - Windows 7へのドライバのインストールに対応（正式対応ではない）

<!-- end list -->

  - 3.1で対応した機能

<!-- end list -->

  - Windows 7（32ビット、64ビット）に正式対応
  - アップル製トラックパッド使用時に起こる問題の解決
  - Apple Wireless KeyboardおよびApple Magic Mouseのサポート

<!-- end list -->

  - 3.2で対応した機能

<!-- end list -->

  - ATI-Radeon HD 5870 graphics card, Apple USB Ethernet Adapter, MacBook Air SuperDrive のサポートを追加。
  - 重大なバグの修正。

<!-- end list -->

  - 各種未対応機能への対応策
    キーボードについては、[AppleK](https://ja.wikipedia.org/wiki/AppleK "wikilink")や[KbdApple](../Page/KbdApple.md "wikilink")などMac系キーボードをWindowsで利用するためのドライバにより上記未対応をほぼ解決できる。

## 関連項目

  - [Parallels Desktop for Mac](../Page/Parallels_Desktop_for_Mac.md "wikilink")
  - [VMware](../Page/VMware.md "wikilink")

## 外部リンク

  - [Boot Camp](http://www.apple.com/jp/support/bootcamp/)

[Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink") [Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:2006年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2006年のソフトウェア "wikilink")