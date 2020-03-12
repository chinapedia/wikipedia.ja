> この記事は[Exchangeable image file format](https://ja.wikipedia.org/wiki/Exchangeable_image_file_format)から翻訳されています。


[代替文=Exifの例](https://ja.wikipedia.org/wiki/ファイル:DigiKam_EXIF_information_screenshot.png "wikilink") **Exchangeable image file format**（エクスチェンジャブル・イメージ・ファイル・フォーマット）は、[富士フイルム](../Page/富士フイルム.md "wikilink")が開発し、当時の[日本電子工業振興協会 (JEIDA)で規格化された](../Page/電子情報技術産業協会.md "wikilink")、写真用の[メタデータ](../Page/メタデータ.md "wikilink")を含む[画像ファイルフォーマット](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")。[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")の画像の保存に使われる。略称は**Exif**で「エグジフ」（もしくは「イグジフ」）。

カメラの機種や撮影時の条件情報を画像に埋め込んでいて、ビューワや[フォトレタッチソフトなどで参照](../Page/写真編集.md "wikilink")、応用することができる。Exif2.2では**Exif Print**という規格を組み込んでおり、撮影時の条件情報を元に自動的に最適化を行って、的確な状態でプリント出力を可能にしている。また撮影者や著作権情報、コメントなど付随することが出来る。

対応画像形式は[JPEG](../Page/JPEG.md "wikilink")、[TIFF](../Page/Tagged_Image_File_Format.md "wikilink")、[JPEG XR](https://ja.wikipedia.org/wiki/JPEG_XR "wikilink")（[HD Photo](../Page/HD_Photo.md "wikilink")）。

## 記録されるメタデータ

以下のようなデータが記録される。撮影日時や場所を後から参照したりそれらによって写真を整理したり、適切なサイズでのプリント、撮影時のカメラの設定情報の参照などユーザーが使う上での利便性がある。

  - 撮影日時 -日付と秒までの時刻が付加される。
  - 位置情報（[ジオタグ](https://ja.wikipedia.org/wiki/ジオタギング "wikilink")） - [GPS付きカメラや携帯電子機器の場合](../Page/グローバル・ポジショニング・システム.md "wikilink")、GPSにより自動的に記録された[緯度](../Page/緯度.md "wikilink")・[経度](../Page/経度.md "wikilink")・[標高](../Page/標高.md "wikilink")などが記録される。また、GPS受信装置の付いていないカメラでも、GPSロガーという機器やスマートフォンの同様のアプリケーションを利用しカメラと一緒に持ち歩くことにより、後で写真に位置情報を付加することも可能。携帯電話やスマートフォンのカメラにおいてGPS機能が普及した一方、2019年現在においてもカメラでは上位機種においてもGPSは普及していない。カメラの起動からGPS観測までの速度やバッテリーへの影響などの観点から実用性が十分でないことが理由とみられる。
  - 撮影方向 -[電子コンパス](https://ja.wikipedia.org/wiki/電子コンパス "wikilink")付きのカメラやスマートフォンで撮影した場合に写真を撮影した際のカメラの方角の情報が付加される。
  - 撮影機器のメーカー名（製造・販売元）
  - 撮影機器のモデル名（[カメラ付き携帯電話](../Page/カメラ付き携帯電話.md "wikilink")・[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")の機種名など）
  - 画像全体の[解像度](../Page/解像度.md "wikilink")
  - 水平・垂直方向の単位あたり[解像度](../Page/分解能.md "wikilink")
  - [シャッター速度](https://ja.wikipedia.org/wiki/シャッター速度 "wikilink")
  - [絞り](../Page/絞り_\(光学\).md "wikilink")（[F値](../Page/F値.md "wikilink")）
  - [ISO感度](../Page/写真フィルム.md "wikilink")
  - [測光モード](../Page/TTL露出計.md "wikilink")
  - [フラッシュ使用の有無](../Page/閃光電球.md "wikilink")
  - 露光補正ステップ値
  - [焦点距離](../Page/焦点距離.md "wikilink")
  - [色空間](../Page/色空間.md "wikilink")（カラースペース）
  - [サムネイル](../Page/サムネイル.md "wikilink")（160×120画素）

## 問題点や対策

撮影時のGPSによる位置情報（緯度・経度）や撮影日時など、個人情報を特定できるおそれがある情報が含まれている。例えば、撮影された写真が観光地や市街地などではなく、自宅で撮影した場合はGPSによる緯度・経度がそのまま自宅の位置となる。例えば、[Twitter](../Page/Twitter.md "wikilink")や[ブログ](../Page/ブログ.md "wikilink")などで写真を公開した際、Exif情報が残ったままだと第三者がExif情報の位置情報から撮影時の緯度・経度で位置を特定され、事件の元になる危険性もある。iPhoneは、iPhoneからSNSへのアップロード時やメッセージへの添付の際に位置情報のみ削除される仕様になっている。一方条件やOSによって仕様はことなるため注意が必要である。

画像内に書かれている住所や名前など、「目に見える画像」に[モザイク処理](../Page/モザイク処理.md "wikilink")を入れても、「目に見えないExif情報」には位置データが残っていたり、Exif情報に含まれる[サムネイル](../Page/サムネイル.md "wikilink")情報にはモザイクがかけられておらず、住所や名前が観覧できてしまう場合もある。

対策としては、各撮影機器でGPS情報を付加しないように設定したり、アプリケーションでExif情報を参照し削除したりする事などがあげられる。また、スマートフォンでExifをアプリケーションを使わず簡易的かつ確実に削除する方法として、[PNG](https://ja.wikipedia.org/wiki/PNG "wikilink")がExifに対応していないのを逆手にとり、画像をスクリーンショット（通常スクリーンショットはPNGで記録されるため）しそれをアップロードする手段がある。一部のSNSやブログでは画像アップロード時に独自の変換を行うことでExif情報や、特に位置情報（ジオタグ）を消している所もある。また、Exif情報はソフトウェアなどで容易に変更可能なため、Exif情報として記録されているGPS情報を意図的に書き換えてあることもある。

撮影日時の情報は、UTCとタイムゾーンを組み合わせたものではなく、機種依存のローカルタイム（現地時刻）のみで記録され、タイムゾーン情報が記録されていないので、海外旅行や出張などタイムゾーンをまたいで移動、生活する際に問題となることもある。なお、タイムゾーン情報が記録できるカメラなどもあるが機種依存の機能であって、Exif共通の仕様ではタイムゾーン情報の付加には対応していない。

## 関連項目

  - [Extensible Metadata Platform](https://ja.wikipedia.org/wiki/Extensible_Metadata_Platform "wikilink")(XMP)
  - [ジオタグ](https://ja.wikipedia.org/wiki/ジオタギング "wikilink")

## 外部リンク

  - [Exif Print](http://www.cipa.jp/exifprint/index_j.html) - カメラ映像機器工業会
  - [JEITA 規格](https://www.jeita.or.jp/cgi-bin/standard/list.cgi?cateid=1&subcateid=4) - 一般社団法人電子情報技術産業協会 (JEITA)

[Category:デジタルカメラ](https://ja.wikipedia.org/wiki/Category:デジタルカメラ "wikilink") [Category:デジタル写真](https://ja.wikipedia.org/wiki/Category:デジタル写真 "wikilink") [Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:メタデータ](https://ja.wikipedia.org/wiki/Category:メタデータ "wikilink")