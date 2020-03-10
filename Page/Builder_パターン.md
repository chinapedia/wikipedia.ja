> この記事は[Builder ](https://ja.wikipedia.org/wiki/Builder_)から翻訳されています。


**Builder パターン**（ビルダー・パターン）とは、[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink")（Gang of Four; 4人のギャングたち）によって定義された[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。 [オブジェクトの生成過程を](../Page/オブジェクト_\(プログラミング\).md "wikilink")[抽象化することによって](../Page/抽象化_\(計算機科学\).md "wikilink")、動的なオブジェクトの生成を可能にする。

## クラス図

Builder パターンの[クラス図](https://ja.wikipedia.org/wiki/クラス図 "wikilink")を以下に挙げる。

[center](https://ja.wikipedia.org/wiki/ファイル:Builder_UML_class_diagram.svg "wikilink")

## 利用例

[Java](https://ja.wikipedia.org/wiki/Java "wikilink") による利用例を以下に挙げる。このソースコードは [Java SE 5(J2SE 5.0)](../Page/Java_Platform,_Standard_Edition.md "wikilink") 以降のバージョンで動作する。

``` java
 enum Material{WOOD, CLAY, CONCRETE, SNOW}

 class Building{
     private Material base;
     private Material frame;
     private Material wall;
     void setBase(Material m){
         this.base = m;
     }
     void setFrame(Material m){
         this.frame = m;
     }
     void setWall(Material m){
         this.wall = m;
     }
     public String toString(){
         return "[Base:" + this.base + ", Frame:" + this.frame + ", Wall:" + this.wall + "]";
     }
 }

 interface Builder{
     void buildBase();
     void buildFrame();
     void buildWall();
     Building getResult();
 }

 class JapaneseHouseBuilder implements Builder{
     private Building building;
     JapaneseHouseBuilder(){
         this.building = new Building();
     }
     public void buildBase(){
         this.building.setBase(Material.CONCRETE);
     }
     public void buildFrame(){
         this.building.setFrame(Material.WOOD);
     }
     public void buildWall(){
         this.building.setWall(Material.CLAY);
     }
     public Building getResult(){
         return this.building;
     }
 }

 class KamakuraBuilder implements Builder{
     private Building building;
     KamakuraBuilder(){
         this.building = new Building();
     }
     public void buildBase(){
         this.building.setBase(Material.SNOW);
     }
     public void buildFrame(){
         this.building.setFrame(Material.SNOW);
     }
     public void buildWall(){
         this.building.setWall(Material.SNOW);
     }
     public Building getResult(){
         return this.building;
     }
 }

 class Director{
     private Builder builder;
     Director(Builder builder){
         this.builder = builder;
     }
     Building construct(){
         this.builder.buildBase();
         this.builder.buildFrame();
         this.builder.buildWall();
         return this.builder.getResult();
     }
 }

 public class BuilderTest{
     public static void main(String[] argv){
         Director d1 = new Director(new JapaneseHouseBuilder());
         Director d2 = new Director(new KamakuraBuilder());
         Building b1 = d1.construct();
         Building b2 = d2.construct();
         System.out.println(b1);
         System.out.println(b2);
     }
 }
```

このソースコードは、以下の結果を出力する。

``` text
[Base:CONCRETE, Frame:WOOD, Wall:CLAY]
[Base:SNOW, Frame:SNOW, Wall:SNOW]
```

`Director` (監督) の管理の元、それぞれの`Builder` (大工) が異なる`Building` (生成物) インスタンスを生成しているのが分かる。

## 関係するパターン

  - [Strategy パターン](https://ja.wikipedia.org/wiki/Strategy_パターン "wikilink"):`Builder` を Strategy パターンにおける `Context` として設計することにより、インスタンスの生成過程をより柔軟にすることができる。
    [Composite パターン](https://ja.wikipedia.org/wiki/Composite_パターン "wikilink"):`Composite` のような複雑な構造を持つインスタンスは、Builder パターンを応用することによって効率的に生成することができる。

## 関連項目

  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")