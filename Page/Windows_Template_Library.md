> この記事は[Windows Template Library](https://ja.wikipedia.org/wiki/Windows_Template_Library)から翻訳されています。


**Windows Template Library** (**WTL**) は[マイクロソフト](../Page/マイクロソフト.md "wikilink")による[Win32をラップ](https://ja.wikipedia.org/wiki/Windows_API "wikilink")（[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")）する[オブジェクト指向の](../Page/オブジェクト指向プログラミング.md "wikilink")[C++](../Page/C++.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")。WTLは[プログラマ](../Page/プログラマ.md "wikilink")が利用する[APIの](../Page/アプリケーションプログラミングインタフェース.md "wikilink")1つである。[MFCの軽量な代替として開発された](https://ja.wikipedia.org/wiki/Microsoft_Foundation_Class "wikilink")。WTLはマイクロソフトの[ATL](https://ja.wikipedia.org/wiki/Active_Template_Library "wikilink")（[COMや](../Page/Component_Object_Model.md "wikilink")[ActiveX](../Page/ActiveX.md "wikilink")のためのもう1つの軽量API）を拡張する。

## 概要

WTLは、小さくて高速なコードという大きな利点のあるATLに対して、アプリケーションや様々なUIコンポーネントの両方のために、より複雑なユーザーインターフェイスをサポートするようにATLを拡張するクラスのセットである。WTLのクラスは、ATLベースのアプリケーション、サーバ、コンポーネント、コントロールに対して、リッチなWin32ベースのUIを実装するための最適かつ簡単な方法であるように設計された。

WTLは、フレームやポップアップウィンドウを初めとして、[MDI](https://ja.wikipedia.org/wiki/Multiple_Document_Interface "wikilink")、標準・コモンコントロール、コモンダイアログ、プロパティシートやページ、[GDIオブジェクト](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink")、UIのアップデート、スクロールバーウィンドウ、スプリッターウィンドウ、コマンドバーなど、様々なユーザーインターフェイスの要素をサポートする。WTLのクラスは主にテンプレートであり、最小限のインスタンスデータとインライン関数を使う。これらはフレームワークとしてデザインされたものではないため、特定のアプリケーションモデルを強制せず、どのようなスタイルでも受け入れられる。クラスはフックやスレッドローカルのメモリ領域を利用しないのでこれらのテクニックの押しつけに制約されない。これらには従属関係が無く、ストレートな[SDKのコードと自由に混ぜることができる](https://ja.wikipedia.org/wiki/ソフトウェア開発キット "wikilink")。要するに、WTLは、より論理的でオブジェクト指向的なモデルをプログラマに提供しつつも、SDKによるプログラムと比べてもサイズとスピードでほとんど遜色のない非常に小さくて効率的なコードを出力する。

WTLの多くのAPIは標準のWin32と直接的に対応しており、多くのWindowsプログラマーにとってなじみの深いインターフェイスである。しかしながらマイクロソフトによる公式のドキュメントは存在せず、この問題に立ち向かうため"WTL Documentation"プロジェクト\[[http://www.viksoe.dk/code/wtldoc.htm\]がスタートしたが](http://www.viksoe.dk/code/wtldoc.htm%5Dがスタートしたが)、でもまだドキュメントは完全ではない。

## 歴史

マイクロソフトは2004年5月、[オープンソース](../Page/オープンソース.md "wikilink")ライセンスに基づいてWTLの[ソースコード](../Page/ソースコード.md "wikilink")を自由に利用できるようにした。マイクロソフトは[SourceForge.net](https://ja.wikipedia.org/wiki/SourceForge.net "wikilink")という[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上のオープンソースコードのためのリポジトリにソースコードを投稿し、[Common Public Licenseに基づいてリリースした](https://ja.wikipedia.org/wiki/Common_Public_License "wikilink")。このライブラリはバージョン7.5の時点で、[Microsoft Permissive Licenseとの](https://ja.wikipedia.org/wiki/シェアードソース "wikilink")[デュアルライセンス](../Page/デュアルライセンス.md "wikilink")でもあった[1](http://www.microsoft.com/resources/sharedsource/licensingbasics/permissivelicense.mspx)。

## プログラム例

[Hello worldを表示するプログラムである](../Page/Hello_world.md "wikilink")。

``` cpp
#include <windows.h>
//ATLヘッダ
#define _ATL_NO_AUTOMATIC_NAMESPACE
#include <atlbase.h>
#include <atlwin.h>
//WTLヘッダ
#define _WTL_NO_AUTOMATIC_NAMESPACE
#include <atlapp.h>
#include <atlcrack.h>

class HelloWindow : public ATL::CWindowImpl<HelloWindow>
{
public:
    // ウィンドウクラス名を登録
    DECLARE_WND_CLASS(TEXT("HelloWindow"));

private:
    // メッセージマップ
    BEGIN_MSG_MAP(HelloWindow)
        MSG_WM_PAINT(OnPaint)
        MSG_WM_DESTROY(OnDestroy)
    END_MSG_MAP()

    // 描画メッセージ
    void OnPaint(HDC)
    {
        WTL::CPaintDC dc(m_hWnd);
        dc.TextOut(10, 10, TEXT("Hello, world"), -1);
    }

    // ウィンドウが破棄されるメッセージ
    void OnDestroy()
    {
        PostQuitMessage(0);
    }
};

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int nCmdShow)
{
    // ウィンドウのインタンスを生成
    HelloWindow wnd;
    if (!wnd.Create(NULL, ATL::CWindow::rcDefault, TEXT("Hello, world"), WS_OVERLAPPEDWINDOW))
    {
        return -1;
    }

    // ウィンドウ表示
    wnd.ShowWindow(nCmdShow);
    wnd.UpdateWindow();

    // メッセージループ
    WTL::CMessageLoop msgLoop;
    return msgLoop.Run();
}
```

## 関連項目

  - [Active Template Library](https://ja.wikipedia.org/wiki/Active_Template_Library "wikilink")

## 外部リンク

  - [SourceForgeのWTLプロジェクト](http://sourceforge.net/projects/wtl/)
  - WTL 8.0 [マイクロソフトのダウンロードページ](http://www.microsoft.com/downloads/details.aspx?familyid=E5BA5BA4-6E6B-462A-B24C-61115E846F0C&displaylang=en)
  - [WTL Documentation](http://www.viksoe.dk/code/wtldoc.htm) - WTLプログラミングライブラリのドキュメント作成運動。
  - [Using the Windows Template Library Part 1](http://www.gamedev.net/reference/programming/features/wtl1/)、[Part 2](http://www.gamedev.net/reference/programming/features/wtl2/) - GameDev.net
  - [WTL for MFC Programmers](http://www.codeproject.com/wtl/wtl4mfc1.asp) - The Code Project – WTLを使い始めたいMFCプログラマーのための入門集。
  - [The WTL Wiki](http://wtl.wikispaces.com/) - WTLのためのwiki。

[Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")