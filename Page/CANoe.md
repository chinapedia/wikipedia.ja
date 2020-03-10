> この記事は[CANoe](https://ja.wikipedia.org/wiki/CANoe)から翻訳されています。


**CANoe**は[Vectorの開発](https://ja.wikipedia.org/wiki/ベクター・インフォマティック "wikilink")・テストソフトウェアツール。このソフトウェアは、主に自動車メーカーおよび[電子制御ユニット](https://ja.wikipedia.org/wiki/エレクトロニックコントロールユニット "wikilink")（ECU）サプライヤがECUネットワークおよび個々のECUの開発、分析、シミュレーション、テスト、診断、起動に使用する。広範な用途と多数の[車両バスシステムに対応していることから](https://ja.wikipedia.org/wiki/ビークルバス "wikilink")、従来の自動車からハイブリッド車、電気自動車までのECU開発に特に適している。CANoeのシミュレーションおよびテスト機能はプログラミング言語[CAPLを使用して行われる](../Page/Communication_Access_Programming_Language.md "wikilink")。

CANoeは、[CAN](https://ja.wikipedia.org/wiki/Controller_Area_Network "wikilink")、、[FlexRay](https://ja.wikipedia.org/wiki/FlexRay "wikilink")、[イーサネット](../Page/イーサネット.md "wikilink")、[MOST](https://ja.wikipedia.org/wiki/Media_Oriented_Systems_Transport "wikilink")\[1\]バスシステム、および\[2\]、[CANopen](https://ja.wikipedia.org/wiki/CANopen "wikilink")\[3\]、\[4\]、\[5\]などのCANベースのプロトコルをサポートしている。

## 説明

In 1996 the first CANoe license was sold by Vector. Since then, the software has become established worldwide as a tool for ECU development. In addition to its primary use in automotive in-vehicle electronic networking, CANoe is also used in industries such as heavy trucks, rail transportation, special purpose vehicles, avionics, medical technology and many more.

New technologies based on IP architectures in the automotive industry \[6\] are supported by CANoe.\[7\] Beyond the scope of communication in a single car, CANoe is used in the development of cooperative systems via .\[8\]\[9\]

At the beginning of the development process for an ECU or ECU, CANoe is used to create simulation models that simulate the behavior of the ECUs. Throughout the further course of ECU development, these models serve as a base for analysis, testing and integration of the bus systems and ECUs. Data is displayed and evaluated in either raw or symbolic format. Back in 1992, Vector developed the DBC data format, which has become a de facto standard for exchanging CAN descriptions in the automotive field. Other relevant standards are supported for other bus systems, e.g.  for FlexRay, LDF for LIN, Fibex for SOME/IP, [EDS/DCF/XDD](https://ja.wikipedia.org/wiki/CANopen "wikilink") for CANopen.\[10\]

While CANoe can simulate the whole communication in a vehicle, it also includes a Test Feature Set, for creating automated test sequences. These automated test sequences can be controlled fully automated by usual CI tools (such as Jenkins etc). The Test Feature Set included in CANoe has a long history and is therefore available in variants; creation of test cases can be created in CAPL (Communication Access Programming Language - a C-like programming language), in XML, or in C\#. The tests can either be manually programmed or generated automatically by different generators.

CANoe's Ethernet option includes Ethernet Conformance Tests (TC8 test suite). CANoe's LIN option includes LIN Conformance slave tests.

## バージョン

Version 1.0 was released in 1996.\[11\] The latest version of CANoe is 12.0 SP2\[12\]. Program Levels Different variants of CANoe are available. They differ in functional scope (full, run, pex), supported bus systems (CAN, FlexRay, etc.) and supported higher protocols (SAE J1939, CANopen, etc.). The product supports the languages German, English and Japanese.

## 関連項目

  -
  -
## 参照

## 情報源

  - Pfeiffer, Ayre, Keydel: *Embedded Networking with CAN and CANopen*, RTC Books San Clemente, USA, 2003
  - Pfeiffer, Ayre, Keydel: *Embedded Networking with CAN and CANopen*, RTC Books, Japan, 2006 (jap)
  - Toshikatsu Suzuki (Senko Medical), Hiroyoshi Takahashi (VJ): *Developing a CANopen system for heart-lung machines*, CAN Newsletter, Nuremberg Germany, September 2009
  - Patrick E. Lanigan, Priya Narasimhan (ECE Department, Carnegie Mellon University), Thomas E. Fuhrman (GM R\&D): *Experiences with a CANoe-based Fault Injection Framework for AUTOSAR*, <http://www.ece.cmu.edu/~planigan/research/lanigan-dsn10.pdf>, downloaded September 30, 2010
  - Becker, Hübner, Hettich, Constabel, Eisenmann, Luka: *Dynamic and Partial FPGA Exploitation*, in Proceedings of the IEEE Vol. 95, No. 2, February 2007, <http://www.gstitt.ece.ufl.edu/courses/spring09/eel4930_5934/reading/pr.pdf>, downloaded September 30, 2010
  - Institute of Electrical Engineering, Beijing Fang Li, Lifang Wang and Chenglin Liao: *Evaluating the Communication Impact on Quality of Service in Steer-by-wire Systems*, IEEE Vehicle Power and Propulsion Conference (VPPC), September 3–5, 2008, Harbin, China, <https://web.archive.org/web/20110722014340/http://up.daneshpajooh.ir/pdf/ieee2008/Evaluating-the-Communication-Impact-on-Quality-of-Service-in-Steer-by-wire-Systems_www.daneshpajooh.ir.pdf>, downloaded September 30, 2010
  - Sandeep Neema, Gabor Karsai (Institute for Software Integrated Systems Vanderbilt University): *Embedded Control Systems Language for Distributed Processing (ECSL-DP)*, <http://w3.isis.vanderbilt.edu/Janos/CS388/Reading%20List/Papers/Automotive%20testbed%20report.pdf>, downloaded September 30, 2010
  - Jürgen Wölfle (Conti Temic): *Testing Concepts and Test Environments of a Tier 1 Supplier*, Vector Congress, Stuttgart, 2010

## 外部リンク

  - [CANoe ウェブサイト](https://www.vector.com/jp/ja/%E8%A3%BD%E5%93%81/products-a-z/software/canoe/)

[Category:CAE](https://ja.wikipedia.org/wiki/Category:CAE "wikilink") [Category:ネットワーク・アナライザ](https://ja.wikipedia.org/wiki/Category:ネットワーク・アナライザ "wikilink")

1.  [CANoe on the website of Vector Informatik GmbH](http://www.vector.com/vi_canoe_en.html), downloaded November 3rd, 2011
2.  [CANoe.J1939](http://www.vector.com/vi_canoe_j1939_en.html), downloaded November 3rd, 2011
3.  [CANopen solutions](http://www.canopen-solutions.com/canopen_index_en.html), downloaded November 3rd, 2011
4.  [Overview CAN-based avionics protocols on www.avionics-networking.com](http://www.avionics-networking.com/av_protocols_en.html), downloaded September 30th, 2010
5.  [Development, Simulation and test of ISOBUS systems](http://www.vector.com/vi_canoe_iso11783_en.html), downloaded November 3rd, 2011
6.  Neff, Dr.Matheus, Königseder (BMW), Singer (Freescale), Wagner (Broadcom): *Ethernet & IP as Automotive Bus System in the Scenario of Camera-based Advanced Driver Assistance Systems* in VDI-Reports 2132, 15.International Congress Electronic Systems for Motor Vehicles, Baden-Baden 2011, .
7.  [CANoe.IP](https://www.vector.com/vi_canoe_ip_en.html) : Development, Simulation and Test of Embedded Systems with CAN and Ethernet, downloaded November 3rd, 2011
8.  [ETSI plugtest in Helmond](http://www.ecomove-project.eu/news-events/news/ecomove-joining-etsi-plugtest-in-helmond/), downloaded November 3rd, 2011
9.  [Car2x Development](https://www.vector.com/vi_car2x_solutions_en.html), downloaded November 3rd, 2011
10.
11. [Company History Vector](http://www.vector.com/vi_company_history_en.html) , downloaded September 30th, 2010
12. [Version history of CANoe](https://www.vector.com/int/en/products/products-a-z/software/canoe/#c91696), downloaded August 2nd, 2017