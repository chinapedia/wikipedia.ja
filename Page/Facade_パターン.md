> この記事は[Facade ](https://ja.wikipedia.org/wiki/Facade_)から翻訳されています。


**Facade パターン**あるいは **Façade パターン**（ファサード・パターン）とは、[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink")（Gang of Four; 4人のギャングたち）によって定義された、[コンピュータ](../Page/コンピュータ.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。Facade（[ファサード](../Page/ファサード.md "wikilink")）とは「建物の正面」を意味する。異なるサブシステムを単純な操作だけを持ったFacade[クラスで結び](../Page/クラス_\(コンピュータ\).md "wikilink")、サブシステム間の独立性を高める事を目的とする。

## 概要

Facadeパターンの例として、サブシステムとしてのコンパイラーを考える。システムとしてのコンパイラーは字句解析器や構文解析器などから構成されている。これらの構成要素は、新たなコンパイラーやその他ソフトウェアを作成する上でサブシステムとして利用することが出来る。しかし、一般ユーザーにとってコンパイラーはソースコードからプログラムを生成するためのものであり、ソースコードをコンパイルできる機能があれば十分である。そこでサブシステムから一般ユーザーのために一般ユーザーが必要としているコンパイル機能だけを呼び出すクラスを提供する。ここで提供されたコンパイル機能を持つクラスがFacadeクラスである。Facadeクラスが提供された事により一般ユーザーはサブシステムの詳細を知る必要がなくなり、サブシステムの実装から解放されるのである。

## Facadeパターンの要件

  - Facadeクラスはあくまでサブシステム内部に仕事を投げるだけで複雑な実装は持たない。

<!-- end list -->

  -
    多様な機能の塊であるサブシステムから、サブシステムを利用するユーザーの用途に合わせた窓口(インターフェース)を提供するだけである。

<!-- end list -->

  - Facadeクラスをサブシステム自体が利用する事はない。

<!-- end list -->

  -
    Facadeクラスはあくまでサブシステム末端の窓口であるため、同じサブシステムから利用される事はない。

<!-- end list -->

  - Facadeパターンはサブシステムの直接使用を妨げない。

<!-- end list -->

  -
    Facadeクラスの利用は強制ではなく、必要であればサブシステムの機能を直接利用できる。言語によっては無名名前空間やPackageスコープによりサブシステムを利用者から隔離できるが、Facadeパターンはそのような制限はしない。

## クラス図

Facade パターンの[クラス図](../Page/クラス図.md "wikilink")を以下に挙げる。

[500px](https://ja.wikipedia.org/wiki/ファイル:Facade_UML_class_diagram.svg "wikilink")

## 適用例

[Java](https://ja.wikipedia.org/wiki/Java "wikilink") による適用例を以下に挙げる。

`driving.Car`

``` java
 package driving;
 class Car{
     private int speed;
     private int distance;
     Car(){
         this.speed = 0;
         this.distance = 0;
     }
     void setSpeed(int speed){
         this.speed = speed;
     }
     void run(int minutes){
         this.distance += minutes * this.speed;
     }
     int getDistance(){
         return this.distance;
     }
 }
```

`driving.Driver`

``` java
 package driving;
 class Driver{
     private Car car;
     Driver(Car car){
         this.car = car;
     }
     void pushPedal(int speed){
         this.car.setSpeed(speed);
     }
     void drive(int minutes){
         this.car.run(minutes);
     }
 }
```

`driving.DrivingSimulator`

``` java
 package driving;
 public class DrivingSimulator{
     public void simulate(){
         Car c    = new Car();
         Driver d = new Driver(c);
         d.pushPedal(700);
         d.drive(30);
         d.pushPedal(750);
         d.drive(20);
         System.out.println("The travel distance is " + c.getDistance() + " m.");
     }
 }
```

`FacadeTest`

``` java
 import driving.DrivingSimulator;
 public class FacadeTest{
     public static void main(String[] argv){
         new DrivingSimulator().simulate();
     }
 }
```

このソースコードの場合、クラス図の `Facade` にあたるのは `DrivingSimulator` である。 `Car` や `Driver` の各種メソッドの呼び出しが `DrivingSimulator#simulate()` の中にすべて集約されている。

## 関係するパターン

  - [Abstract Factory パターン](../Page/Abstract_Factory_パターン.md "wikilink"):Abstract Factory パターンは Facade パターンの具体例と言える。`ConcreteFactory` クラスが `Facade` クラスに相当する。

## 関連項目

  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")
  - [パッケージ (Java)](../Page/パッケージ_\(Java\).md "wikilink")

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")