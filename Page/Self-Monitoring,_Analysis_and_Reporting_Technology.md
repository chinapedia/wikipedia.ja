> この記事は[Self-Monitoring, Analysis and Reporting Technology](https://ja.wikipedia.org/wiki/Self-Monitoring,_Analysis_and_Reporting_Technology)から翻訳されています。


**Self-Monitoring, Analysis and Reporting Technology** (セルフモニタリング・アナリシス・アンド・リポーティング・テクノロジー、略称: **S.M.A.R.T.**; スマート) は、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")と、[ソリッドステートドライブ](../Page/ソリッドステートドライブ.md "wikilink")の障害の早期発見・故障の予測を目的として[ディスクドライブ](../Page/ディスクドライブ.md "wikilink")に搭載されている機能である。

この機能は、各種の検査項目をリアルタイムに自己診断し、その状態を数値化する。ユーザーはその数値を各種のツール（後述）を用いることで知ることが出来る。全ての故障を予期することは出来ないが、安定した利用環境における経年劣化による故障を知るには非常に有効である。

## 検査項目 (属性)

各検査項目（属性）には、「現在の値」(Value)、「最悪（ワースト）値」(Worst)、「[閾値](https://ja.wikipedia.org/wiki/閾値 "wikilink")」(Threshold)、そして「生の値」(Data / Raw value) の4つの項目が設定されている。これらの値がどのような方法によって算出されているかは各[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")によって異なるため、一概にどの値がどうなっていれば良いとは言い切れないが、一般的に「生の値」が実際のエラー等の回数や時間や温度を示しており、「生の値」を正規化したものが「現在の値」、今までの「現在の値」のうち最も悪かった時の値が「最悪値」である。（「生の値」が明らかにおかしい値の場合はベンダー独自の内部形式であると考えられる）

「現在の値」は大きいほどよく悪くなると減少する。「現在の値」の最も良い時の値は100であることが多いがこれも製造者によって様々である。「閾値」はベンダーが定めた限界値で「現在の値」または「最悪値」が「閾値」を下回ることがあれば、データのバックアップやハードディスクの交換など必要な処置を施すべきであると考えられる。また Temperature (0xC2) やReallocated Sectors Count (0x05) など「生の値」が重要な項目も存在しており、「閾値」を下回らなくとも注意が必要な場合がある。

以下はS.M.A.R.T.によって報告される主な検査項目の一覧である。ATA仕様では属性のIDが何を示すかは規定していないためこの表は基本的にすべてベンダー独自の意味を解釈しているにすぎないことに注意すべきである。特に重要な項目については**太字**で注釈をつけた。ただし、HDDベンダーによって調査可能な検査項目は若干異なるため、必ずしも全ての項目を調査できるわけではない。また、HDDベンダーが独自の検査項目を設定していたり、IDが異なっていたり、独自の名称を設定している場合もあるが、それらについてはここでは網羅していない。

<table>
<caption><strong>S.M.A.R.T.検査項目一覧</strong></caption>
<thead>
<tr class="header">
<th><p>ID</p></th>
<th><p>項目名</p></th>
<th><p>理想値</p></th>
<th><p>詳細な説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>01<br />
0x01</strong></p></td>
<td><p><strong>Raw Read Error Rate</strong></p></td>
<td></td>
<td><p>この項目はハードディスクからデータを読み込む時に発生したエラーの割合を表す。現在値が閾値より低い場合、ハードディスク内の磁気ディスクまたは磁気ヘッドに異常がある。</p></td>
</tr>
<tr class="even">
<td><p>02<br />
0x02</p></td>
<td><p>Throughput Performance</p></td>
<td></td>
<td><p>ハードディスクの全体的な（<a href="../Page/スループット.md" title="wikilink">スループット</a>）処理能力。現在値が閾値以下の場合、高い確率でハードディスクに異常がある。</p></td>
</tr>
<tr class="odd">
<td><p>03<br />
0x03</p></td>
<td><p>Spin-Up Time</p></td>
<td></td>
<td><p>ハードディスクが通電回転を開始してから規定の回転数に達するまでにかかった平均時間。</p></td>
</tr>
<tr class="even">
<td><p>04<br />
0x04</p></td>
<td><p>Start/Stop Count</p></td>
<td></td>
<td><p>ハードディスクのスピンドルモーターが回転/停止した回数。</p></td>
</tr>
<tr class="odd">
<td><p><strong>05<br />
0x05</strong></p></td>
<td><p><strong>Reallocated Sectors Count</strong></p></td>
<td></td>
<td><p>代替処置（データを特別に予約した予備エリアに移動する）を施された不良セクタの数。</p></td>
</tr>
<tr class="even">
<td><p>06<br />
0x06</p></td>
<td><p>Read Channel Margin</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>07<br />
0x07</p></td>
<td><p>Seek Error Rate</p></td>
<td></td>
<td><p>磁気ヘッドが目的のデータの在るトラックへ移動しようとして失敗（シークエラー）した割合。ハードディスクの熱、サーボ機構の損傷などによって発生する。数値が低い場合、ハードディスクの表面やハードディスクの機械的なシステムに問題がある可能性がある。</p></td>
</tr>
<tr class="even">
<td><p>08<br />
0x08</p></td>
<td><p>Seek Time Performance</p></td>
<td></td>
<td><p>磁気ヘッドがシーク作業に要した平均時間。</p></td>
</tr>
<tr class="odd">
<td><p>09<br />
0x09</p></td>
<td><p>Power-On Hours</p></td>
<td></td>
<td><p>工場出荷状態からのハードディスクの通電時間の合計。閾値に対するこの値の減少は<a href="../Page/平均故障間隔.md" title="wikilink">MTBF（平均故障間隔）の減少を表す</a>。</p></td>
</tr>
<tr class="even">
<td><p><strong>10<br />
0x0A</strong></p></td>
<td><p><strong>Spin Retry Count</strong></p></td>
<td></td>
<td><p>ディスクを規定の速度までスピンアップしようと再試行を試みた回数。</p></td>
</tr>
<tr class="odd">
<td><p>11<br />
0x0B</p></td>
<td><p>Recalibration Retries または Calibration Retry Count</p></td>
<td></td>
<td><p>ハードディスクのキャリブレーション動作（熱によるオフトラック現象を自動的に補正する機能）を再試行（すでに一度キャリブレーションに失敗している状態で）しようとした回数。</p></td>
</tr>
<tr class="even">
<td><p>12<br />
0x0C</p></td>
<td><p>Device Power Cycle Count</p></td>
<td></td>
<td><p>ハードディスクの電源をON/OFFした回数。</p></td>
</tr>
<tr class="odd">
<td><p><strong>13<br />
0x0D</strong></p></td>
<td><p><strong>Soft Read Error Rate</strong></p></td>
<td></td>
<td><p>オフトラックの数。 数値が0でなければバックアップを取る。</p></td>
</tr>
<tr class="even">
<td><p>22<br />
0x16</p></td>
<td><p>Current Helium Level</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>170<br />
0xAA</p></td>
<td><p>Available Reserved Space</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>171<br />
0xAB</p></td>
<td><p>SSD Program Fail Count</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>172<br />
0xAC</p></td>
<td><p>SSD Erase Fail Count</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>173<br />
0xAD</p></td>
<td><p>SSD Wear Leveling Count</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>174<br />
0xAE</p></td>
<td><p>Unexpected power loss count</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>175<br />
0xAF</p></td>
<td><p>Power Loss Protection Failure</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>176<br />
0xB0</p></td>
<td><p>Erase Fail Count</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>177<br />
0xB1</p></td>
<td><p>Wear Range Delta</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>179<br />
0xB3</p></td>
<td><p>Used Reserved Block Count Total</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>180<br />
0xB4</p></td>
<td><p>Unused Reserved Block Count Total</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>181<br />
0xB5</p></td>
<td><p>Program Fail Count Total または Non-4K Aligned Access Count</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>182<br />
0xB6</p></td>
<td><p>Erase Fail Count</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>183<br />
0xB7</p></td>
<td><p>SATA Downshift Error Count または Runtime Bad Block</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>184<br />
0xB8</strong></p></td>
<td><p><strong>End-to-End error / IOEDC</strong></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>185<br />
0xB9</p></td>
<td><p>Head Stability</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>186<br />
0xBA</p></td>
<td><p>Induced Op-Vibration Detection</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><strong>187<br />
0xBB</strong></p></td>
<td><p><strong>Reported Uncorrectable Errors</strong></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>188<br />
0xBC</strong></p></td>
<td><p><strong>Command Timeout</strong></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>189<br />
0xBD</p></td>
<td><p>High Fly Writes</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>190<br />
0xBE</p></td>
<td><p>Temperature Difference または Airflow Temperature</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>191<br />
0xBF</p></td>
<td><p>G-sense Error Rate</p></td>
<td></td>
<td><p>衝撃によって引き起こされるプログラムエラーの頻度</p></td>
</tr>
<tr class="even">
<td><p>192<br />
0xC0</p></td>
<td><p>Power-off Retract Count または Emergency Retract Cycle Count (Fujitsu) または Unsafe Shutdown Count</p></td>
<td></td>
<td><p>ハードディスクの電源が切れ、磁気ヘッドが磁気ディスク表面から退避場所に退避した回数の合計。</p></td>
</tr>
<tr class="odd">
<td><p>193<br />
0xC1</p></td>
<td><p>Load Cycle Count または Load/Unload Cycle Count (Fujitsu)</p></td>
<td></td>
<td><p>ロード/アンロード機構によって磁気ヘッドが磁気ディスク表面から退避場所に退避し、その後再び磁気ディスク表面に戻った回数の合計。一般的な2.5型HDDのメーカー保証値は、2005年以降に登場したモデルでは大抵60万回程度。2004年以前のモデルでは30万回程度。</p></td>
</tr>
<tr class="even">
<td><p>194<br />
0xC2</p></td>
<td><p>Temperature または Temperature Celsius</p></td>
<td></td>
<td><p>ハードディスクの現在の温度。一般的に動作が保障されている最高温度は55℃である。</p></td>
</tr>
<tr class="odd">
<td><p>195<br />
0xC3</p></td>
<td><p>Hardware ECC recovered</p></td>
<td></td>
<td><p>ECC（Error Correction Code、<a href="https://ja.wikipedia.org/wiki/誤り訂正符号" title="wikilink">誤り訂正符号</a>）によって検知されたエラーの回数</p></td>
</tr>
<tr class="even">
<td><p><strong>196<br />
0xC4</strong></p></td>
<td><p><strong>Reallocation Event Count</strong></p></td>
<td></td>
<td><p>セクタの代替処理が発生した回数。仮に処理に失敗しても回数に加算される。</p></td>
</tr>
<tr class="odd">
<td><p><strong>197<br />
0xC5</strong></p></td>
<td><p><strong>Current Pending Sector Count</strong></p></td>
<td></td>
<td><p>現在異常があり、代替処理を待つセクタの総数。もし後で読み込みに成功したセクタがあれば、この値は減少する。</p></td>
</tr>
<tr class="even">
<td><p><strong>198<br />
0xC6</strong></p></td>
<td><p><strong>Off-Line Scan Uncorrectable Sector Count</strong></p></td>
<td></td>
<td><p>オフラインスキャン時に発見された、回復不可能なセクタの総数。この値が増加する場合は、磁気ディスクの表面に明確な問題がある。</p></td>
</tr>
<tr class="odd">
<td><p>199<br />
0xC7</p></td>
<td><p>UltraDMA CRC Error Count</p></td>
<td></td>
<td><p>UltraDMAモードでのデータ転送中に発生したCRCエラーの数。</p></td>
</tr>
<tr class="even">
<td><p>200<br />
0xC8</p></td>
<td><p>Write Error Rate (Multi Zone Error Rate)</p></td>
<td></td>
<td><p>データの書き込み中に発見されたエラーの総数。</p></td>
</tr>
<tr class="odd">
<td><p>201<br />
0xC9</p></td>
<td><p>Soft Read Error Rate または TA Counter Detected</p></td>
<td></td>
<td><p>プログラムが磁気ディスク表面からデータを読み込む際に発生したエラーの割合。</p></td>
</tr>
<tr class="even">
<td><p>202<br />
0xCA</p></td>
<td><p>Data Address Mark Error または TA Counter Increased</p></td>
<td></td>
<td><p>DAM（データアドレスマーク）に関するエラーの頻度を表す。</p></td>
</tr>
<tr class="odd">
<td><p>203<br />
0xC8</p></td>
<td><p>Run Out Cancel</p></td>
<td></td>
<td><p><a href="../Page/誤り検出訂正.md" title="wikilink">ECC</a>（誤り訂正符号）エラーの頻度を表す。</p></td>
</tr>
<tr class="even">
<td><p>204<br />
0xCC</p></td>
<td><p>Soft ECC Correction</p></td>
<td></td>
<td><p>ソフトウェアECCによって訂正されたエラーの総数。</p></td>
</tr>
<tr class="odd">
<td><p>205<br />
0xCD</p></td>
<td><p>Thermal Asperity Rate</p></td>
<td></td>
<td><p>サーマル・アスペリティ現象（磁気ヘッドが磁気媒体の突起に衝突して熱を生じ、データ検出を誤る可能性のある現象）によるエラーの総数。</p></td>
</tr>
<tr class="even">
<td><p>206<br />
0xCE</p></td>
<td><p>Flying Height</p></td>
<td></td>
<td><p>磁気ヘッドの浮上高。</p></td>
</tr>
<tr class="odd">
<td><p>207<br />
0xCF</p></td>
<td><p>Spin High Current</p></td>
<td></td>
<td><p>ドライブのスピンアップに使用した高電流量。</p></td>
</tr>
<tr class="even">
<td><p>208<br />
0xD0</p></td>
<td><p>Spin Buzz</p></td>
<td></td>
<td><p>バズルーチン（ヘッドがディスクに接触するのを避けるために、ヘッドをディスクに対して垂直方向に跳ね上げる処理。これが連続して発生するとブザーのような音が鳴る）を使用した数。</p></td>
</tr>
<tr class="odd">
<td><p>209<br />
0xD1</p></td>
<td><p>Offline Seek Performance</p></td>
<td></td>
<td><p>オフラインスキャン時に測定された、シーク機能の性能の値を表す。</p></td>
</tr>
<tr class="even">
<td><p>210<br />
0xD2</p></td>
<td><p>Vibration During Write</p></td>
<td></td>
<td><p>データの書き込み中に加わった大きな振動を表す。</p></td>
</tr>
<tr class="odd">
<td><p>211<br />
0xD3</p></td>
<td><p>Vibration During Read</p></td>
<td></td>
<td><p>データの読み込み中に加わった大きな振動を表す。</p></td>
</tr>
<tr class="even">
<td><p>212<br />
0xD4</p></td>
<td><p>Shock During Write</p></td>
<td></td>
<td><p>データの書き込み中に加わった大きな衝撃を表す。</p></td>
</tr>
<tr class="odd">
<td><p><strong>220<br />
0xDC</strong></p></td>
<td><p><strong>Disk Shift</strong></p></td>
<td></td>
<td><p>ディスク（プラッタ）が衝撃などにより当初の固定位置よりズレた距離。</p></td>
</tr>
<tr class="even">
<td><p>221<br />
0xDD</p></td>
<td><p>G-Sense Error Rate</p></td>
<td></td>
<td><p>ハードディスクに加えられた衝撃によって発生したエラーの割合。衝撃はハードディスクに内蔵された衝撃感知センサーによって感知されている。</p></td>
</tr>
<tr class="odd">
<td><p>222<br />
0xDE</p></td>
<td><p>Loaded Hours</p></td>
<td></td>
<td><p>一般的な作業時間中に引き起こされた磁気ヘッドアクチュエータの負荷の値を表す。</p></td>
</tr>
<tr class="even">
<td><p>223<br />
0xDF</p></td>
<td><p>Load/Unload Retry Count</p></td>
<td></td>
<td><p>ロード/アンロード機構によるロードまたはアンロード時に失敗して再試行した回数。</p></td>
</tr>
<tr class="odd">
<td><p>224<br />
0xE0</p></td>
<td><p>Load Friction</p></td>
<td></td>
<td><p>機械的なパーツの摩擦による磁気ヘッドアクチュエータの負荷の値を表す。</p></td>
</tr>
<tr class="even">
<td><p>225<br />
0xE1</p></td>
<td><p>Load/Unload Cycle Count</p></td>
<td></td>
<td><p>機械的なパーツの摩擦による磁気ヘッドアクチュエータの負荷の値を表す。</p></td>
</tr>
<tr class="odd">
<td><p>226<br />
0xE2</p></td>
<td><p>Load-in Time</p></td>
<td></td>
<td><p>磁気ヘッドアクチュエータがデータの読み込みによる負荷を受けていた時間の総合計。</p></td>
</tr>
<tr class="even">
<td><p>227<br />
0xE3</p></td>
<td><p>Torque Amplification Count</p></td>
<td></td>
<td><p>ディスク回転時のトルク増幅力の値を示す。</p></td>
</tr>
<tr class="odd">
<td><p>228<br />
0xE4</p></td>
<td><p>Power-Off Retract Count</p></td>
<td></td>
<td><p>電源を抜くなどしてハードディスクが強制的に停止し、磁気ヘッドが緊急退避した回数。ハードディスクに大きな負担を与える。一般的な2.5型HDDのメーカー保証値は2万回程度。</p></td>
</tr>
<tr class="even">
<td><p>230<br />
0xE6</p></td>
<td><p>GMR Head Amplitude (HDD) または Drive Life Protection Status (SSD)</p></td>
<td></td>
<td><p>GMR磁気ヘッドの動作中における震えの振幅。</p></td>
</tr>
<tr class="odd">
<td><p>231<br />
0xE7</p></td>
<td><p>Life Left (SSD) または Temperature</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>232<br />
0xE8</p></td>
<td><p>Endurance Remaining または Available Reserved Space</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>233<br />
0xE9</p></td>
<td><p>Media Wearout Indicator (SSD) または Power-On Hours</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>234<br />
0xEA</p></td>
<td><p>Average erase count AND Maximum Erase Count</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>235<br />
0xEB</p></td>
<td><p>Good Block Count AND System(Free) Block Count</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>240<br />
0xF0</p></td>
<td><p>Head Flying Hours または Transfer Error Rate (Fujitsu)</p></td>
<td></td>
<td><p>磁気ヘッドが位置決めをしている時間。</p></td>
</tr>
<tr class="odd">
<td><p>241<br />
0xF1</p></td>
<td><p>Total LBAs Written</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>242<br />
0xF2</p></td>
<td><p>Total LBAs Read</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>243<br />
0xF3</p></td>
<td><p>Total LBAs Written Expanded</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>244<br />
0xF4</p></td>
<td><p>Total LBAs Read Expanded</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>249<br />
0xF9</p></td>
<td><p>NAND Writes (1GiB)</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>250<br />
0xFA</p></td>
<td><p>Read Error Retry Rate</p></td>
<td></td>
<td><p>データを磁気ディスクから読み込む間に現れるエラーの頻度。</p></td>
</tr>
<tr class="odd">
<td><p>251<br />
0xFB</p></td>
<td><p>Minimum Spares Remaining</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>252<br />
0xFC</p></td>
<td><p>Newly Added Bad Flash Block</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>254<br />
0xFE</p></td>
<td><p>Free Fall Protection</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 各種のツール

多種多様なツールが存在しており、HDDベンダーから診断ツールが公開されている場合もある。以下は、主なツール等の製作・配布元である。

  - [Active SMART](http://www.ariolic.com/activesmart/index.html)（試用版あり、商品、Windows7対応）
  - [CrystalDiskInfo](https://ja.wikipedia.org/wiki/CrystalDiskInfo "wikilink")（Free、Windows 10対応、日本語）
  - [FromHDDtoSSD](http://www.iuec.co.jp/fromhddtossd2s/)（Free版あり、商品、Windows8対応、日本語）
  - [Hard Drive Inspector](http://altrixsoft.com/en/hddinsp/)（15日試用版あり、商品、Windows7対応）
  - [HDD Health](http://www.panterasoft.com/)（Free、Windows7x64で作動異常）
  - [HDD Health 日本語化](http://nihongo.syuro.com/)
  - [HDDlife](http://www.hddlife.com/)（試用版あり、商品、Windows7対応）
  - [HDD-SCAN](http://hdd-data.jp/software/hdd-scan/harddisk-technologies.html/)（Free、日本語）
  - [HDD SMART Analyzer](http://www.mijimari.com/hddanalyzer.htm)（Free、ver1.2.0からWindows7対応、日本語）
  - [HD Tune](http://www.hdtune.com/)（試用版あり商品、Windows7対応）
  - [Mam's S.M.A.R.T Reader](http://mam-mam.net/download/smart.html)
  - [PC-Doctor for Windows](http://www.pc-doctor.co.jp/)（商品、Windows7対応）
  - [SpeedFan](http://www.almico.com/speedfan.php)（Free）
  - [SpeedFan日本語化](http://www.water.sannet.ne.jp/scull/speedfan.html)（リンク切れ）
  - [ハードディスク・スマートチェッカー](http://mam-mam.net/hdsc/)（シェアウェア、Windows7x64非対応）
  - [SMARTReporter](http://web.archive.org/20030803234717/homepage.mac.com/julianmayer/) Apple Macintosh
  - [TechTool Pro 8](http://www.act2.com/ttp8/) Apple Macintosh（商品、日本語）
  - [smartmontools](http://smartmontools.sourceforge.net/) Unix
  - [ファイナルハードディスク診断3.0](http://www.finaldata.jp/hikkoshi/shindan/)（商品）

装置ベンダーとツールベンダーでデータの意味付けが異なることが多い。そのため、A社のHDDの状態についてB社のツールがエラー、障害あるいは劣化がある、あるいはないと表示したとしても、実際とは違うかもしれないので注意が必要である。

## 外部リンク

  - [S.M.A.R.T. attribute Meaning](http://www.ariolic.com/activesmart/smart-attributes/)
  - [Self-Monitoring, Analysis and Reporting Technology :: Attributes](http://smartlinux.sourceforge.net/smart/attributes.php)

[Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink") [Category:補助記憶装置](https://ja.wikipedia.org/wiki/Category:補助記憶装置 "wikilink")