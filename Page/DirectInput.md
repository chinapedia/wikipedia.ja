> この記事は[DirectInput](https://ja.wikipedia.org/wiki/DirectInput)から翻訳されています。


**DirectInput**は[マイクロソフト](../Page/マイクロソフト.md "wikilink")によって開発された[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")「[Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")」のうちのひとつであり、[マウス](../Page/マウス_\(コンピュータ\).md "wikilink")、[キーボード](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink")、[ジョイスティック](../Page/ジョイスティック.md "wikilink")、[ゲームコントローラ](https://ja.wikipedia.org/wiki/ゲームコントローラ "wikilink")等を介してユーザーからの入力情報を収集するための[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。DirectInputはまたゲーム中の[入力機器](https://ja.wikipedia.org/wiki/入力機器 "wikilink")のボタンや座標を特定のアクションに割り当てる「アクションマッピング」のシステムを提供する。さらに「[フォースフィードバック](https://ja.wikipedia.org/wiki/フォースフィードバック "wikilink")」デバイスの入出力を扱う。

マイクロソフトはDirectX 9で[Xbox 360用コントローラーのための](../Page/Xbox_360.md "wikilink")[XInput](https://ja.wikipedia.org/wiki/XInput "wikilink")という新しい入力ライブラリを導入した。

DirectInputとXInputは通常のWin32[アプリケーションにも利点がある](../Page/アプリケーションソフトウェア.md "wikilink")。

  - アプリケーションはバックグラウンドでの動作中でも入力機器から情報を入手できる。
  - **フォースフィードバック**のような様々なタイプの入力機器を完全にサポートできる。
  - **アクションマッピング**機能によりアプリケーションはデータ生成にどのような種類の装置が必要であるかを知ることなく入力データを入手できる。

DirectInputはDirectXライブラリの一部であるが、DirectX 8から大きな変更がない。2005年のMeltdownでのプレゼンテーション[1](http://go.microsoft.com/fwlink/?linkid=50758&clcid=0x409)で[マイクロソフト](../Page/マイクロソフト.md "wikilink")は、新しいアプリケーションはキーボードとマウスを制御するのにDirectInputではなく[Windowsのメッセージループを活用して](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、Xbox 360のコントローラーでもDirectInputではなくXInputを使うように推奨した。

## 歴史

DirectInputはDirectXの一部であった。当初は実際はジョイスティックだけをサポートしており、マウスとキーボードの部分は標準Win32 APIの単なるラッパーであった。DirectXバージョン3.0よりキーボードとマウスがサポートされるようになり、ジョイスティックのサポートも改善した。DirectX 5.0ではジョイスティックのサポートを大幅に強化し、フォースフィードバックに対応し、ボタン数が増え、基盤となる[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")モデルが変更された。マウスでもボタン数が4から8に増えた。DirectX 7.0では長い間待望だった複数のマウスの接続が可能になり、ジョイスティックのように個別に操作できるようになったが、後にリリースされた[Windows XPではこの機能が動作しなくなった](../Page/Microsoft_Windows_XP.md "wikilink")（[Windows 98](../Page/Microsoft_Windows_98.md "wikilink")/[MEとDirectX](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink") 9の組み合わせでは引き続き動作していた）。DirectX 8.0はアクションマッピングや様々な異なる種類の装置を広くサポートする最後のメジャーバージョンアップとなった。

マイクロソフトは元々DirectInputを全ての入力機器を取り扱う方法として売り込んだが、現在ではこの方針は撤回されている。今ではマイクロソフトはDirectInputを使ってキーボードとマウスを制御することを推奨しておらず、Xbox 360コントローラー用の新しいXInputを推奨している。

## XInput

XInputは「次世代」コントローラーのための[APIであり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、Xbox 360の発売と共に導入され、Xbox 360コントローラーの全ての機能がWindows XP SP1以上で利用できるようになった。XInputはDirectInputよりもプログラムが劇的に簡単になる利点がある。XInputはDirectX 9以上から利用できる。

## DirectInputとXInputの比較

DirectInputはDirectX 8から大きな変更が無く、XInputは後のDirectX 9で導入され、2つのAPIの現状と将来には若干の混乱がある。現在はお互いにない特徴があり、そしていずれもDirectX 10で大きな変更はない。

Xbox 360用コントローラーとマイクロソフトのデフォルトのWindowsドライバの組み合わせにおいてDirectInputを使う場合、XInputと比較して以下の制約がある。

  - 左右のトリガーは単一のデジタルな方向として動作し、独立したアナログの軸としては動作しない。
  - 振動機能は利用できない。
  - ヘッドセットデバイスの確認ができない。

[MSDNによると](../Page/Microsoft_Developer_Network.md "wikilink")、以下のような説明および解決策が記載されている\[1\]\[2\]。

これはしかしながら、デュアルアナログスティックのあるゲームパッドやハンドルコントローラーなどのような様々なDirectInputコントローラーが既にトリガーやペダルに個々に割り当て済みであるという事実を無視していた。しかも多くのDirectInputデバイスには振動機能も搭載されていた。Xbox 360用コントローラーで振動機能をサポートし、デッドゾーンの検知や、(オプションとして)独立したトリガーをDirectInput経由で利用できる、[XBCD](http://matt-land.com/xbcd/)というドライバが存在している。これはDirectInputとXInputのAPIの違いによるものというよりはむしろ、マイクロソフトが提供するXbox 360用コントローラーのドライバは「意図的に」DirectInputでの機能を制限していることを示している。

現在XInputのAPIはDirectInputにはない制約もある。

  - **次世代**のコントローラーのみをサポートする。基本的にWindows用のドライバがあるXbox 360用のコントローラーに制限される。旧式のWindows用のコントローラーはサポートしていない。
  - 最大同時接続数4台。これはXboxからWindowsに持ち込まれた制約である。今のところ4つのコントローラーを必要とするPC用ゲームはまずないが、DirectInputにはこのような制限が無く、不合理な制限と考えられる。
  - キーボード、マウス及びマウス型デバイスの非サポート。DirectInputはこれらのデバイスに対しては推奨されないものとするマイクロソフトの意向を反映しているが、DirectInputでこれらのデバイスを利用すること自体は可能である。
  - 1コントローラーあたり、アナログ4軸、10ボタン、デジタル8方向のみをサポートする。XInputがサポートする軸とボタンの数はXbox 360用コントローラーと直接対応しているためである。対してDirectInputはアナログ8軸、128ボタン、フルレンジのPOV (ハットスイッチ) をサポートする。

DirectInputは従来から存在する規格のため、対応するドライバーが用意されているデバイスも豊富だが、XInputは後発のため、主要な対応デバイスとしてはXbox 360用の純正コントローラーおよび[Xbox One用の純正コントローラー](https://ja.wikipedia.org/wiki/Xbox_One "wikilink")\[3\]のみである。ただし、[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")製の各種コントローラーもDirectInput/XInput両対応の製品がいくつか発売されている\[4\] \[5\]。

[Windows 8で導入された](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリでは、XInput 1.4のみが使用可能であり、デスクトップアプリ向けのXInput (1.1/1.2/1.3, 9.1.0) およびDirectInputは使用できない\[6\]。XInput 1.4ではオーディオヘッドセットの問い合わせ機能が追加されている\[7\]。

## 脚注

## 関連項目

[Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")

[Category:DirectX](https://ja.wikipedia.org/wiki/Category:DirectX "wikilink")

1.  \[<https://docs.microsoft.com/ja-jp/previous-versions/direct-x/bb173051(v=vs.85>) XInput と DirectInput | Microsoft Docs\]
2.  [XInput and DirectInput - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/xinput/xinput-and-directinput)
3.  [XINPUT and Windows 8 | Games for Windows and the DirectX SDK blog](https://walbourn.github.io/xinput-and-windows-8/)
4.  [幅広いゲームが楽しめる、USBゲームパッド - JC-U3613Mシリーズ](http://www2.elecom.co.jp/peripheral/gamepad/jc-u3613m/)
5.  [F310 Gamepad - Logicool](http://gaming.logicool.co.jp/ja-jp/product/f310-gamepad)
6.  [XInput Versions - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/xinput/xinput-versions)
7.  [XInputGetAudioDeviceIds function (xinput.h) - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/api/xinput/nf-xinput-xinputgetaudiodeviceids)