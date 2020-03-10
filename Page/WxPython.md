> この記事は[WxPython](https://ja.wikipedia.org/wiki/WxPython)から翻訳されています。


**wxPython**は[Python](../Page/Python.md "wikilink")で記述された[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")な[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")である。wxPythonはロビン・ダンが[HP-UX](../Page/HP-UX.md "wikilink")システム上でGUIを必要として生み出された。wxPythonは[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")と同[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")ライセンスが適用されている。これは[フリーソフトウェア財団と](https://ja.wikipedia.org/wiki/Free_Software_Foundation "wikilink")[Open Source Initiativeによって認可されたライセンスである](../Page/Open_Source_Initiative.md "wikilink")。

## 例

このサンプルは"[Hello world](../Page/Hello_world.md "wikilink")"モジュールである。wxPythonの二つのオブジェクト（windowオブジェクト,applicationオブジェクト）を通してメッセージを表示する。

``` python
#!/usr/bin/env python

import wx

class TestFrame(wx.Frame):
    def __init__(self, parent, ID, title):
        wx.Frame.__init__(self, parent, -1, title, pos=(0, 0), size=(320, 240))
        panel = wx.Panel(self, -1)
        text = wx.StaticText(panel, -1, "Hello, World!", wx.Point(10, 5), wx.Size(-1, -1))

class TestApp(wx.App):
    def OnInit(self):
        frame = TestFrame(None, -1, "Hello, world!")
        self.SetTopWindow(frame)
        frame.Show(True)
        return True

if __name__ == '__main__':
    app = TestApp()
    app.MainLoop()
```

## 関連項目

  - [wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")
  - [Tkinter](https://ja.wikipedia.org/wiki/Tkinter "wikilink")
  - [PyQt](https://ja.wikipedia.org/wiki/PyQt "wikilink")
  - [PyGTK](https://ja.wikipedia.org/wiki/PyGTK "wikilink")

## 外部リンク

  - [wxPythonオフィシャルサイト](http://www.wxpython.org/)
  - [wxWidgetsオフィシャルサイト](http://www.wxwidgets.org/)

[Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink") [Category:Pythonライブラリ](https://ja.wikipedia.org/wiki/Category:Pythonライブラリ "wikilink") [Category:1998年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1998年のソフトウェア "wikilink")