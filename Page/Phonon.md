> この記事は[Phonon](https://ja.wikipedia.org/wiki/Phonon)から翻訳されています。


**Phonon**（フォノン）は[Linux](../Page/Linux.md "wikilink")デスクトップ環境である[KDE](../Page/KDE.md "wikilink") 4向けに開発された[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")のマルチメディア[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。Phononは、[Unix系](../Page/Unix系.md "wikilink")デスクトップにおけるマルチメディア環境に関する諸問題を解決することを目的として開発された。

Phonon自体はマルチメディアフレームワークではないが、バックエンドを通じて[GStreamer](../Page/GStreamer.md "wikilink")や[Xine](../Page/Xine.md "wikilink")のような既存のフレームワークの橋渡しを行う機能を有し、開発者はPhononがサポートするあらゆるマルチメディアフレームワークに単一のAPIを通じてアクセス出来るようになる。これによって、フレームワークが放置されることやAPIの不安定性、KDEが単一のフレームワークに依存することなどの諸問題を回避できる。

また、[Unix系](../Page/Unix系.md "wikilink")のデスクトップ以外にも利用可能であり、現在[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Mac OS Xをサポートするためバックエンドの開発が進められている](https://ja.wikipedia.org/wiki/macOS "wikilink")。

Phononの使用例を挙げると、たとえば音声ファイルは以下にある数行の絶対パスで記述された[C++](../Page/C++.md "wikilink")コードのみで再生可能であり\[1\]、既存のオーディオフレームワークである[aRts](https://ja.wikipedia.org/wiki/aRts "wikilink")よりも少ないコードで済む\[2\]。 <code>

    MediaObject *media = new MediaObject(this);
    media->setCurrentSource("/home/username/music/filename.ogg");
    media->play();

</code> Phononは開発者による冗長かつ困難な作業を減らし、全てのマルチメディア機能を備えるわけではないが、メディアプレイヤーの一般的な機能を単純に実行することが出来るようになる\[3\]。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Phononsettings.png "wikilink")

## 機能

Phononは、様々なバックエンドと開発者がエンジン (*engine*) と呼んでいるシステムを橋渡しする。それぞれのエンジンはある特定のバックエンドと一緒に動作し、それぞれのバックエンドはPhononに再生、停止、シークなど基本的な機能をコントロールさせる。また、トラックのフェードなどの機能もサポートされる予定である\[4\]。

  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[4月23日](../Page/4月23日.md "wikilink")現在、[Unix系](../Page/Unix系.md "wikilink")のシステムでサポートされているバックエンドは[xine](https://ja.wikipedia.org/wiki/xine "wikilink")、[GStreamer](../Page/GStreamer.md "wikilink")、[VLC](https://ja.wikipedia.org/wiki/VLC_media_player "wikilink")、[MPlayer](../Page/MPlayer.md "wikilink")である<ref>

</ref>。

  - [Windowsでサポートされているバックエンドは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、[VLC](https://ja.wikipedia.org/wiki/VLC_media_player "wikilink")、[MPlayer](../Page/MPlayer.md "wikilink")である。
  - [Mac OS Xでサポートされているバックエンドは](https://ja.wikipedia.org/wiki/macOS "wikilink")[Quicktime](https://ja.wikipedia.org/wiki/Quicktime "wikilink")である。

Phononはマルチメディアフレームワークをリアルタイムで替えることが可能であり、ユーザーが音楽を聞いている間であってもわずかな時間で交代することが出来る。Phononを用いているシステム上の全てのアプリケーションに影響するため、フレームワークの変更は簡単になると見られている。

さらに、[Solidを利用しており](https://ja.wikipedia.org/wiki/Solid_\(KDE\) "wikilink")、ユーザーはヘッドセットや、スピーカー、マイクなどの機器をより制御できるようになる。例えば、ヘッドセットを用いて[インターネット電話](https://ja.wikipedia.org/wiki/インターネット電話 "wikilink")で会話している最中でも、音楽など別のサウンドはスピーカーから流すよう設定することが出来る。

## Trolltech

[Qt](../Page/Qt.md "wikilink")の開発元である[Trolltech](https://ja.wikipedia.org/wiki/Trolltech "wikilink")は、バージョン4.4のリリースでPhononを利用し、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")でオーディオ・ビデオを取り扱えるようになった。

## 脚注

## 関連項目

  - [KDELibs](../Page/KDELibs.md "wikilink")
  - [KMPlayer](../Page/KMPlayer.md "wikilink")

## 外部リンク

  - [Phonon公式ページ](http://phonon.kde.org/)

[Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink")

1.
2.
3.
4.