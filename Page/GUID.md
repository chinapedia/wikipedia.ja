> この記事は[GUID](https://ja.wikipedia.org/wiki/GUID)から翻訳されています。


**GUID** () または**グローバル一意識別子**（ぐろーばるいちいしきべつし）は、[UUID](../Page/UUID.md "wikilink")の実装のひとつ、あるいは（事実上）UUIDの別名である。

UUIDの[マイクロソフト](../Page/マイクロソフト.md "wikilink")による実装を指すと解されることもあるが、[オラクルのデータベースや](../Page/Oracle_Database.md "wikilink")[NetIQ](https://ja.wikipedia.org/wiki/NetIQ "wikilink")の[eDirectory](https://ja.wikipedia.org/wiki/NetIQ_eDirectory "wikilink")（[ディレクトリ・サービス](../Page/ディレクトリ・サービス.md "wikilink")）、[GUIDパーティションテーブル](../Page/GUIDパーティションテーブル.md "wikilink")など、ほぼUUIDを指して、GUIDの語が使われることもある。

GUIDを生成するツールとして、[Microsoft Windows SDKに付属する](../Page/Microsoft_Windows_SDK.md "wikilink") *GuidGen* \[1\]などがある。GuidGenは[Microsoft Visual Studioのメニューから呼び出すこともできる](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。[Windows APIには](../Page/Windows_API.md "wikilink")`CoCreateGuid()`関数\[2\]および`UuidCreate()`関数\[3\]が用意されている。[.NET Frameworkには](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")`System.Guid.NewGuid()`メソッドが用意されている\[4\]。

## 構造

GUID は16バイト (128ビット) の2進数値で、以下のような[構造体](../Page/構造体.md "wikilink")で表現される。

`GUID STRUCT`
` Data1 dd`
` Data2 dw`
` Data3 dw`
` Data4 db 8`
`GUID ENDS`

`<guiddef.h>` における`GUID`構造体の定義は以下のとおり\[5\]。

``` c
typedef struct _GUID {
    unsigned long  Data1;
    unsigned short Data2;
    unsigned short Data3;
    unsigned char  Data4[8];
} GUID;
```

[Microsoft Windowsでは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")16ビット/32ビット/64ビットいずれのターゲットプラットフォーム（[CPU](../Page/CPU.md "wikilink")アーキテクチャ）においても、`short`型は常に16ビットであり、`long`型は常に32ビットである。

## テキスト表記

GUIDの表記には一般に以下のような[16進表記が使われる](../Page/十六進法.md "wikilink")。

  -
    `3F2504E0-4F89-11D3-9A0C-0305E82C3301`

このテキスト表記は以下のような32桁の構造を持つ。

1.  Data1 (8桁)
2.  ハイフン
3.  Data2 (4桁)
4.  ハイフン
5.  Data3 (4桁)
6.  ハイフン
7.  Data4 の最初の2アイテム (4桁)
8.  ハイフン
9.  Data4 の残りの6アイテム (12桁)

[波括弧](https://ja.wikipedia.org/wiki/括弧#波括弧｛｝ "wikilink") (ブレース) で囲んで表記することも多い。

  -
    `{3F2504E0-4F89-11D3-9A0C-0305E82C3301}`

## 使用例

  - [COMで用いられている](../Page/Component_Object_Model.md "wikilink")[オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")識別のための[クラスID](../Page/クラス_\(コンピュータ\).md "wikilink")、[インターフェイスIDなど](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")。
  - [MSBuild](https://ja.wikipedia.org/wiki/MSBuild "wikilink")で用いられているプロジェクトIDなど。

## 脚注

## 外部リンク

  - [Microsoft,GuidGenのダウンロードサイト](http://www.microsoft.com/downloads/details.aspx?FamilyId=94551F58-484F-4A8C-BB39-ADB270833AFC&displaylang=en)
  - [GuidGen](http://www.nowan.hu/guidgenerator.aspx)

[Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink")

1.  [Generate GUID using guidgen.exe – Syed's Blog](https://blogs.msdn.microsoft.com/syedab/2010/05/09/generate-guid-using-guidgen-exe/)
2.  [CoCreateGuid function (combaseapi.h) | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
3.  [UuidCreate function (rpcdce.h) | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate)
4.  [Guid.NewGuid Method (System) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.guid.newguid)
5.  [GUID | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/api/guiddef/ns-guiddef-guid)