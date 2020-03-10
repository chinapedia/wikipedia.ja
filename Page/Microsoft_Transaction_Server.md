> この記事は[Microsoft Transaction Server](https://ja.wikipedia.org/wiki/Microsoft_Transaction_Server)から翻訳されています。


**Microsoft Transaction Server**（**MTS**）は、他のアプリケーションに容易に[トランザクション](../Page/トランザクション.md "wikilink")を実装しサポートするサービスコンポーネントである。

## アーキテクチャ

MTSアーキテクチャは以下の要素から構成される。

  - MTS実行部 (mtxex.dll)
  - 各コンポーネントのFactoryラッパーとContextラッパー
  - MTSサーバコンポーネント
  - MTSクライアント
  - 補助システム:
      - [COMランタイムサービス](../Page/Component_Object_Model.md "wikilink")
      - [Service Control Manager](https://ja.wikipedia.org/wiki/:en:Service_Control_Manager "wikilink") (SCM)
      - Microsoft [Distributed Transaction Coordinator](https://ja.wikipedia.org/wiki/:en:Distributed_Transaction_Coordinator "wikilink") (MSDTC)
      - [Microsoft Message Queue](https://ja.wikipedia.org/wiki/:en:Microsoft_Message_Queuing "wikilink") (MSMQ)
      - COM-Transaction Integrator (COM-TI)
      - その他

MTS実行部の制御下で動作するCOMコンポーネントをMTSコンポーネントと呼ぶ。MTSコンポーネントは全て[DLLとして開発され](../Page/ダイナミックリンクライブラリ.md "wikilink")、1つ以上のCOMコンポーネントとして実装される。これらのコンポーネントがMTS実行部の管理下で展開され実行される。通常のCOMコンポーネントと同様、IClassFactory を実装したオブジェクトは、そのコンポーネントの新たなインスタンスを生成する Factory オブジェクトとして機能する。

MTSはFactoryラッパーオブジェクトとObjectラッパーを実際のMTSコンポーネントとそのクライアントの間に挿入する。従って、クライアントがMTSコンポーネントを呼び出すと、ラッパー（Factory と Object）が常にそれを横取りし、独自のインスタンス管理アルゴリズム Just In Time Activation (JITA) を呼び出しに注入する。そしてラッパーが実際のMTSコンポーネントを呼び出す。

さらに、コンポーネントの展開属性の情報に基づき、それらラッパーオブジェクト内でトランザクションロジックとセキュリティチェックも行われる。

MTSコンポーネントそれぞれに対応して、IObjectContext インタフェースを実装した Context オブジェクトが存在する。Context オブジェクトは、トランザクションに関する情報、セキュリティ情報、展開情報など、そのコンポーネントに固有の情報を保持する。MTSコンポーネントは IObjectContext インタフェースを通して Context オブジェクトを呼び出す。

MTSでは、クライアントからの呼び出しがコンテナに到達して初めて中間層の実際のMTSコンポーネントが生成される。コンポーネントは常に動作しているわけではないので、システムリソースを浪費しない（ただし、ラッパーとスケルトンは常に動作している）。

クライアントからの呼び出しが来ると、即座にMTSラッパープロセスがJITAというインスタンス管理アルゴリズムを起動する。実際のMTSコンポーネントは「ジャストインタイム」方式で生成され、ラッパーからの要求を処理する。そして応答をクライアントに返し、クライアントが SetComplete()/SetAbort() を呼び出すか、トランザクションが完了するか、クライアントがコンポーネントの Release() を呼び出したとき、実際のMTSコンポーネントが破壊される。つまりMTSはステートレスなコンポーネントモデルである。

サーバ上でクライアントが典型的なMTSコンポーネントのサービスを要求したとき、以下のように動作する。

1.  データベースのコネクションを確立する。
2.  コンポーネントの状態を Shared Property Manager または既存のオブジェクトかクライアントから読み取る。
3.  [ビジネスロジック](../Page/ビジネスロジック.md "wikilink")を実行する。
4.  コンポーネントの変化した状態を書き込み、必要ならデータベースに書き戻す。
5.  データベースのコネクションをクローズし解放する。

従って、高レイテンシのリソースを非同期リソースプールとして実装でき、その際にこの[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")サーバで与えられるステートレスな[JITアクティベーションを利用すべきである](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")。

## 外部リンク

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")